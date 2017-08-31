# react-simple-timefield

Simple React time input field.

[![Build Status](https://travis-ci.org/antonfisher/react-simple-timefield.svg?branch=master)](https://travis-ci.org/antonfisher/react-simple-timefield)
[![npm](https://img.shields.io/npm/v/react-simple-timefield.svg)](https://www.npmjs.com/package/react-simple-timefield)
![status](https://img.shields.io/badge/status-beta-lightgray.svg)

[![Demo](docs/demo.gif)](https://antonfisher.com/react-simple-timefield/)

[Demo](https://antonfisher.com/react-simple-timefield/)

## Installation
```bash
npm install --save react-simple-timefield
```

## Usage
```jsx
import TimeField from 'react-simple-timefield';
...
<TimeField
    value={time}                  // required, format '00:00' or '00:00:00'
    onChange={this.onTimeChange}  // required
    showSeconds                   // default: false
/>
```

## Real world example
```jsx
import TimeField from 'react-simple-timefield';

class App extends React.Component {
  constructor(...args) {
    super(...args);

    this.state = {
      time: '12:34'
    };

    this.onTimeChange = this.onTimeChange.bind(this);
  }

  onTimeChange(time) {
    this.setState({time});
  }
  
  render() {
    const {time} = this.state;
  
    return (
      <section>
        <TimeField value={time} onChange={this.onTimeChange} />
        <TimeField
          value={time}
          onChange={this.onTimeChange}
          style={{color: '#333'}}
        />
       </section>
    );
  }
}
```

## Changelog
* 1.1.0 Added `showSeconds` property
* 1.0.0 Initial release

## Contributing
```bash
# run development mode
cd demo
npm run dev

# run demo build
cd demo
npm run build

# run main build
npm run build

# run lint
npm run lint
```

## Todo
- [x] Support full time format with seconds
- [ ] Material UI support
- [ ] Tests

## License
MIT License. Free use and change. 