# react-native-flash

Simple API to turn on and off flash in react native

[![npm version](https://img.shields.io/npm/v/@mertozyilmazz/react-native-flash.svg?style=flat-square)](https://www.npmjs.com/package/@mertozyilmazz/react-native-flash)
[![npm downloads](https://img.shields.io/npm/dm/@mertozyilmazz/react-native-flash.svg?style=flat-square)](https://www.npmjs.com/package/@mertozyilmazz/react-native-flash)

## Installation

    npm install @mertozyilmazz/react-native-flash
	or
	yarn add @mertozyilmazz/react-native-flash

## Usage

In your `*.js`:

```javascript
	import Flash from '@mertozyilmazz/react-native-flash'

	Flash.turnOnFlash() // turn on flash

	Flash.turnOffFlash() // turn off flash

	/*Has flash checks if the phone has flash available.
		Since all communication between react native and native modules is asychrounous, it takes a success callback, and failure callback. atm both callbacks are necessary.

		*/
	Flash.hasFlash(function(){
		Flash.turnOnFlash()
	},function(){
		alert("You do not have flash")
	})
})
```