# react-electron-menu

[![NPM version](https://badge.fury.io/js/react-electron-menu.svg)](http://badge.fury.io/js/react-electron-menu)
[![Build Status](https://travis-ci.org/SamyPesse/react-electron-menu.png?branch=master)](https://travis-ci.org/SamyPesse/react-electron-menu)

This modules provides a react API to create and manage electron's menus.

### Installation

```
$ npm install react-electron-menu --save
```

### Usage

This module provides 3 types of menu: `WindowMenu`, `ContextMenu` and `AppMenu`.

##### `WindowMenu`

This menu type is displayed only for the currently focused window.

```js
const React = require('react');
const { render } = require('react-dom');
const { WindowMenu, MenuItem } = require('react-electron-menu');
const { remote } = require('electron');

render(
    <Provider electron={remote}>
        <WindowMenu>
            <MenuItem label="File">
                <Menu>
                    <MenuItem label="Open ..." onClick={...} />
                </Menu>
            </MenuItem>
        </WindowMenu>
    </Provider>,
    document.body
)
```