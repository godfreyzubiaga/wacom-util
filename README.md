# Wacom Signature Pad Integration

Simple Wacom Signature pad integration to your web apps.

## Installation

`npm i wacom-util`

## Implementation

### ReactJS

```Typescript
import React, { useState } from 'react';
import { showWacomSignPad } from 'wacom-util';

const App = () => {
  const [signature, setSignature] = useState('');

  const captureSignature = (signatureText) => {
    alert('Signature Captured!');
    setSignature(signatureText);
  };

  return (
    <div>
      <button
        type="button"
        id="signButton"
        value="Start demo"
        onClick={() => showWacomSignPad(captureSignature)}
      >
        Sign
      </button>
      <div>{!!signature && <img src={signature} alt="Signature" />}</div>
    </div>
  );
};

export default App;
```

## LICENSE

MIT license, Copyright (c) 2022 Godfrey Zubiaga
