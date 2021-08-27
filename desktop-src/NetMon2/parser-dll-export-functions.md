---
description: Die in der folgenden Tabelle aufgeführten Funktionen sind Einstiegspunkte für Parser-DLLs. Die Funktionen sind die Einstiegspunkte für Aufrufe vom Betriebssystem und Netzwerkmonitor.
ms.assetid: 67811ddb-1961-4306-a62f-b9fd2d2d2b55
title: Parser-DLL-Exportfunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94c04eb57cf5d5f76b60bca43fc5ed47ae641182efc74b21c8b41fa5d909af6b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037030"
---
# <a name="parser-dll-export-functions"></a>Parser-DLL-Exportfunktionen

Die in der folgenden Tabelle aufgeführten Funktionen sind Einstiegspunkte für Parser-DLLs. Die Funktionen sind die Einstiegspunkte für Aufrufe vom Betriebssystem und Netzwerkmonitor.



| Funktion                                           | Beschreibung                                                                                                                                                    |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [DllMain-Parser](dllmain-parser.md)               | Gibt der Parser-DLL an, dass sie geladen oder entladen wird. Das Betriebssystem ruft die **DllMain Parser-Funktion auf,** wenn ein Prozess die DLL lädt oder entlädt. |
| [AttachProperties](attachproperties.md)           | Benachrichtigt den Parser, alle Eigenschaften, die in einem Frame vorhanden sind, anfügen zu müssen.                                                                                            |
| [Registrierung aufheben](deregister.md)                       | Benachrichtigt den Parser über die Bereinigung.                                                                                                                               |
| [FormatProperties](formatproperties.md)           | Benachrichtigt den Parser, alle Eigenschafteninstanzen in zu übernehmen und den **szPropertyText-Member** jeder **PROPERTYINST-Struktur zu** erstellen.                       |
| [RecognizeFrame](recognizeframe.md)               | Bestimmt, ob der Parser die nicht verarbeiteten Framedaten mit dem angegebenen Protokoll interpretieren kann.                                                            |
| [Registrieren des Parsers](register-parser.md)             | Bestimmt grundlegende Informationen zum Parser innerhalb der DLL. Netzwerkmonitor ruft die **Register Parser-Funktion** auf.                                          |
| [ParserAutoInstallInfo](parserautoinstallinfo.md) | Installiert automatisch einen Parser.                                                                                                                               |



 

Netzwerkmonitor stellt Strukturen und Hilfsfunktionen zur Verfügung, die der Parser aufrufen kann.



| Weitere Informationen über                          | Siehe                                                                          |
|-----------------------------------------------------|------------------------------------------------------------------------------|
| Hilfsfunktionen, die Experten und Parser aufrufen können. | [Allgemeine Funktionen von Experten und Parsern](expert-and-parser-common-functions.md) |
| Hilfsfunktionen, die nur Parser aufrufen können.        | [Parserfunktionen](parser-functions.md)                                     |
| Strukturen, die von Parserfunktionen verwendet werden.               | [Parserstrukturen](parser-structures.md)                                   |



 

 

 



