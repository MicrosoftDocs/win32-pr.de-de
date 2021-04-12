---
description: Die in der folgenden Tabelle aufgeführten Funktionen sind Einstiegspunkte für parserdlls. Die Funktionen sind die Einstiegspunkte für Aufrufe vom Betriebssystem und Netzwerkmonitor.
ms.assetid: 67811ddb-1961-4306-a62f-b9fd2d2d2b55
title: Export Funktionen der Parser-DLL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 929541a1eda60740fe219352fee285a5a34a89df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393406"
---
# <a name="parser-dll-export-functions"></a>Export Funktionen der Parser-DLL

Die in der folgenden Tabelle aufgeführten Funktionen sind Einstiegspunkte für parserdlls. Die Funktionen sind die Einstiegspunkte für Aufrufe vom Betriebssystem und Netzwerkmonitor.



| Funktion                                           | BESCHREIBUNG                                                                                                                                                    |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [DllMain-Parser](dllmain-parser.md)               | Gibt an, dass die Parser-DLL geladen oder entladen wurde. Das Betriebssystem Ruft die **DllMain-parserfunktion** auf, wenn ein Prozess die dll lädt oder entlädt. |
| [Attachproperties](attachproperties.md)           | Benachrichtigt den Parser, alle Eigenschaften anzufügen, die in einem Frame vorhanden sind.                                                                                            |
| [Registrierung aufheben](deregister.md)                       | Benachrichtigt den Parser, eine Bereinigung durchzusetzen.                                                                                                                               |
| [Formatproperties](formatproperties.md)           | Benachrichtigt den Parser, alle Eigenschaften Instanzen in zu übernehmen und den **szpropertytext** -Member jeder **propertyinst** -Struktur zu erstellen.                       |
| [Erkenzeframe](recognizeframe.md)               | Bestimmt, ob der Parser die nicht verarbeiteten Frame Daten mit dem angegebenen Protokoll interpretieren kann.                                                            |
| [Parser registrieren](register-parser.md)             | Bestimmt grundlegende Informationen über den Parser in der dll. Netzwerkmonitor Ruft die **Register Parser** -Funktion auf.                                          |
| ["Parameserautoinstallinfo"](parserautoinstallinfo.md) | Installiert einen Parser automatisch.                                                                                                                               |



 

Netzwerkmonitor stellt Strukturen und Hilfsfunktionen bereit, die der Parser abrufen kann.



| Weitere Informationen über                          | Siehe                                                                          |
|-----------------------------------------------------|------------------------------------------------------------------------------|
| Hilfsfunktionen, die von Experten und Parser aufgerufen werden können. | [Allgemeine Funktionen für Experten und Parser](expert-and-parser-common-functions.md) |
| Hilfsfunktionen, die nur von den Parser aufgerufen werden können.        | [Parser-Funktionen](parser-functions.md)                                     |
| Strukturen, die von Parserfunktionen verwendet werden.               | [Parserstrukturen](parser-structures.md)                                   |



 

 

 



