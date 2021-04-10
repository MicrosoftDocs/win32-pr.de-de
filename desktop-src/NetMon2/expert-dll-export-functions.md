---
description: Die folgenden Funktionen sind die Einstiegspunkte für Experten-DLLs und für Aufrufe des Betriebssystems und Netzwerkmonitor.
ms.assetid: 1c0dcf6f-7f80-424b-9e6a-5a8b6a5b176f
title: Export Funktionen der Experten-dll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 923611521b98619b357eb2de93ee2269caf9c838
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958730"
---
# <a name="expert-dll-export-functions"></a>Export Funktionen der Experten-dll

Die folgenden Funktionen sind die Einstiegspunkte für Experten-DLLs und für Aufrufe des Betriebssystems und Netzwerkmonitor.



| Funktion                                   | BESCHREIBUNG                                                                                                                                                              |
|--------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DllMain-Experte**](dllmain-expert.md)   | Gibt an, dass die Experten-dll geladen oder entladen wurde. Wenn ein Prozess die dll lädt oder entlädt, ruft das Betriebssystem die [**DllMain**](/windows/desktop/Dlls/dllmain) -Funktion auf. |
| [**Experte registrieren**](register-expert.md) | Bestimmt grundlegende Informationen zum Experten innerhalb der dll. Netzwerkmonitor Ruft die **Register** -Funktion auf.                                                           |
| [**Konfigurieren**](configure.md)             | Konfiguriert den Experten innerhalb der dll. Netzwerkmonitor Ruft die [**configure**](configure.md) -Funktion auf.                                                                 |
| [**Ausführen**](run.md)                         | Startet den Experten innerhalb der dll. Netzwerkmonitor Ruft die [**Run**](run.md) -Funktion auf.                                                                                 |



 

Netzwerkmonitor bietet auch Strukturen, Enumerationen und Hilfsfunktionen, die der Experte anrufen kann.



| Informationen über                                      | Finden Sie unter                                                                          |
|------------------------------------------------------------|------------------------------------------------------------------------------|
| Hilfsfunktionen, die von Experten und Parser aufgerufen werden können | [Allgemeine Funktionen für Experten und Parser](expert-and-parser-common-functions.md) |
| Hilfsfunktionen, die nur von Experten aufgerufen werden           | [Expertenfunktionen](expert-functions.md)                                     |
| Von Expertenfunktionen verwendete Strukturen               | [Expertenstrukturen](expert-structures.md)                                   |
| Von expertenstrukturen und Funktionen verwendete Enumerationen       | [Expertenenumerationen](expert-enumerations.md)                               |



 

 

 
