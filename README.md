`adsalonwmp` is an internal video annotation web tool that crowdsources data for the [Wesleyan Media Project](https://mediaproject.wesleyan.edu/).

This is a [Next.js](https://nextjs.org/) project bootstrapped with [`create-next-app`](https://github.com/vercel/next.js/tree/canary/packages/create-next-app).



## Usage

For an extensive user guide and documentation, please check out the following documents:

- [User Guide](https://docs.google.com/document/d/1N5uHkGX4boBQyj82vzMRa_v3SJmHPs_KBj1AEabEao0/edit?usp=sharing) - learn how to navigate the tool

- [Documentation](https://docs.google.com/document/d/1z_uooKfthy-TI4LMEwd2Sj5CkCwCkRZJSUHF08o2_3E/edit?usp=sharing) - learn more about AdSalon features


## Documentation

### Variables

Variable | Description
--- | --- 
`axios` | call axios.post() to send data to server
`query` | call axios.post() to send data to server
`reference` | call axios.post() to send data to server

### States

State | Initial Value | Description
--- | --- | --- 
`start`, `setStart(*String*)` | 00:00:00 | user marked start time in HH:MM:DD
`startSec`, `setStartSec(*Number*)` | 0 | user marked start time in seconds
`stop`, `setStop(*String*)` | 00:00:00 | user marked stop time in HH:MM:DD
`stopSec`, `setStopSec(*Number*)` | 0 | user marked stop time in seconds
`pressed`, `setPressed(*Boolean*)` | false | flag that turns true when user submits data
`submitted`, `setSubmitted(*Boolean*)` | false | flag that turns true when post request to server is successful
`error`, `setError(*Boolean*)` | false | flag that turns true when server post request to server is bad
`resCode`, `setResCode(*String*)` | "" | server response code
`resText, setResText(*String*)` | "" | server response message

### Methods

Method | Description
--- | --- 
`createClip()` | async function that posts ClipSchema to server
`handleSeek()` | event handler function that seeks to suggested time within video
`handleStart()` | event handler function that updates `start` and `startSec` variables
`handleStop()` | event handler function that updates `stop` and `stop` variables
`handleSubmit(e)` | event handler function that verifies then calls `createClip()`

