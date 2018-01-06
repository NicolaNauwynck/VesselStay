# Vessel Overview API

Get an overview of expected and in port stays for the ports of Antwerp and Zeebrugge.

| This documentation applies to v1.0 of this API | 
| -------- |


## Purpose of this API

**Port+** combines data from different sources in one database to build one dataset of vessels with their relevant stay information.

With this API you are able to get a realtime overview of all the expected and in port vessels for the ports of Antwerp and Zeebrugge. When a vessel is expected the known IN vessel will be returned. When a vessel is in-port the active voyage of that time will be returned.



## Contents of this repository
  
```
/
  /doc            technical documentation about the use of this API
  /src            sample source code to call this API (coming soon)
```

## More information
`
For in-port voyages the active voyage is determined based on the following logic: if a voyage is active (not yet docked) than this is the active voyage, if the voyage is docked the next voyage will be returned from the API (if the next voyage is known).


Following key information is available through the API:
- Stay number
- Active voyage number
- Location from where the voyage is moving (entry point or berth location)
- Location to where the voyage is moving (berth lcoation or exit point  )

- Information about vessel (imo number, name)
- Information about the responsible agent of the voyage
- ET and AT Information about the following passagepoints (if available), these can be used to apply custom expected and in-port logic: 
  - Zeebrugge haven
  - Coördinatiepunt
  - Hansweert
  - Vlissingen rede
  - Petroleum instellingen zuid
  - Albertkanaal
  - Terneuzen sluis
  - Noordlandbrug
  - Sas van Gent

Following business rules are applied for Antwerp:

A vessel is expected when it ?

A vessel is in port when it ?


Following business rules are applied for Zeebrugge:

A vessel is expected when it has not yet passed "Strekdam"

A vessel is in port when it has passed "Strekdam"

