---
description: Die in der folgenden Tabelle aufgeführten Netzwerkmonitor Funktionen können verwendet werden, um entweder Parser oder Experten zu entwickeln.
ms.assetid: 26eb4f99-a8dc-43a2-abb9-9577518b6f2f
title: Allgemeine Funktionen für Experten und Parser
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6776260610c2decb0ecf91b6373d301937d899b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345006"
---
# <a name="expert-and-parser-common-functions"></a>Allgemeine Funktionen für Experten und Parser

Die in der folgenden Tabelle aufgeführten Netzwerkmonitor Funktionen können verwendet werden, um entweder [*Parser*](p.md) oder [*Experten*](e.md)zu entwickeln.



| Funktion                                                               | BESCHREIBUNG                                                                         |
|------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [Compareadressen](compareaddresses.md)                               | Vergleicht zwei angegebene Adressen.                                                       |
| [Compareframedebug](compareframedestaddress.md)                 | Vergleicht eine angegebene Adresse mit der Zieladresse eines Frames.                     |
| [Compareframesourceaddress](compareframesourceaddress.md)             | Vergleicht eine angegebene Adresse mit der Quelladresse eines Frames.                          |
| [FilterAddObject](filteraddobject.md)                                 | Fügt einem Filter ein einzelnes-Objekt hinzu.                                                   |
| [Findpropertyinstance](findpropertyinstance.md)                       | Sucht die erste Instanz einer bestimmten Eigenschaft.                                       |
| [Findpropertyinstancerestart](findpropertyinstancerestart.md)         | Sucht die nächste Instanz einer bestimmten Eigenschaft.                                        |
| [Getcapturecomment](getcapturecomment.md)                             | Ruft den Kommentar einer Erfassung ab.                                                 |
| [Getcapturecommentfromfilename](getcapturecommentfromfilename.md)     | Ruft den Kommentar einer Erfassung aus der Erfassungs Datei ab.                           |
| [Getcapturemactype](getcapturemactype.md)                             | Ruft den Mac-Typ der Erfassung ab.                                              |
| [Getcapturetimestamp](getcapturetimestamp.md)                         | Ruft den Erfassungs Timeout Stempel ab.                                                |
| [Getcapturetotalframes](getcapturetotalframes.md)                     | Ruft die Gesamtrahmen der Erfassung ab.                                          |
| [Getenabledprotokolle](getenabledprotocols.md)                         | Ruft eine Liste aller Protokolle ab, die als aktiviert markiert sind.                            |
| [GetFrame](getframe.md)                                               | Ruft ein Handle für einen angegebenen Frame ab.                                                |
| [Getframecapturehandle](getframecapturehandle.md)                     | Ruft ein Handle für eine angegebene Erfassung ab.                                              |
| [Getframedstaddressoffset](getframedstaddressoffset.md)               | Ruft den Ziel Adress Offset für einen angegebenen Frame ab.                         |
| [Getframefromframehandle](getframefromframehandle.md)                 | Ruft einen Frame für ein bestimmtes Frame Handle ab.                                         |
| [GetFrameLength](getframelength.md)                                   | Ruft die Länge eines angegebenen Frames ab.                                              |
| [Getframemacheaderlength](getframemacheaderlength.md)                 | Ruft die Länge des Mac-Headers für einen angegebenen Frame ab.                           |
| [Getframemactype](getframemactype.md)                                 | Ruft den Mac-Typ für einen angegebenen Frame ab.                                           |
| [Getframennummer](getframenumber.md)                                   | Gibt die Nummer eines angegebenen Frames zurück.                                                |
| [Getframerecognizedata](getframerecognizedata.md)                     | Ruft die Protokoll Bezeichner (und deren Offsets) aller erkannten Protokolle ab. |
| [Getframesrcaddressoffset](getframesrcaddressoffset.md)               | Ruft den Offset an die Quelladresse eines angegebenen Frames ab.                        |
| [Getframestoredlength](getframestoredlength.md)                       | Ruft die Länge eines angegebenen Frames ab.                                              |
| [Getframetimestamp](getframetimestamp.md)                             | Ruft den Zeitstempel eines angegebenen Frames ab.                                          |
| [Getpreviousprojecoloffsetbyname](getpreviousprotocoloffsetbyname.md) | Ruft die vorherige Instanz eines angegebenen Protokolls ab.                                |
| [GetProperty](getproperty.md)                                         | Ruft eine Eigenschaft mit einem angegebenen Namen ab.                                             |
| [GetPropertyInfo](getpropertyinfo.md)                                 | Ruft die Informationen einer bestimmten Eigenschaft ab.                                   |
| [Getpropertytext](getpropertytext.md)                                 | Ruft den Text einer bestimmten Eigenschaft ab.                                             |
| [GetProtocolFromName](getprotocolfromname.md)                         | Ruft ein bestimmtes Protokoll anhand des Namens ab.                                              |
| [Getprotocolinfo](getprotocolinfo.md)                                 | Verwendet das Protokoll Handle zum Abrufen von Protokoll bezogenen Daten.                        |
| [Getprotocolstarstarte-THandle](getprotocolstartoffsethandle.md)       | Ruft den Offset eines angegebenen Protokolls ab.                                           |
| [Mactypedeadresssstype](mactypetoaddresstype.md)                       | Konvertiert einen Mac-Typ in einen Adresstyp.                                             |
| [Modifyframe](modifyframe.md)                                         | Aktualisiert einen vorhandenen Frame mit neuen Daten.                                            |



 

Weitere Informationen zu Funktionen und Strukturen, die nur von Experten verwendet werden, sowie zu Funktionen und Strukturen, die nur von-Parser verwendet werden, finden Sie in den in der folgenden Tabelle aufgeführten Themen.



| Weitere Informationen über                                          | Siehe                                                                                                |
|---------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| Expertenspezifische Funktionen, die Sie zum Entwickeln von Experten-DLLs verwenden können. | [Expertenfunktionen, Strukturen und Enumerationen](expert-functions-structures-and-enumerations.md) |
| Parserspezifische Funktionen, die Sie zum Entwickeln von Parser-DLLs verwenden können. | [Parser-Funktionen und-Strukturen](parser-functions-and-structures.md)                             |



 

 

 



