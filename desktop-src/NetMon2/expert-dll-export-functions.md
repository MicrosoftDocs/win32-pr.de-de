---
description: Die folgenden Funktionen sind die Einstiegspunkte für Experten-DLLs und für Aufrufe vom Betriebssystem und Netzwerkmonitor.
ms.assetid: 1c0dcf6f-7f80-424b-9e6a-5a8b6a5b176f
title: Experten-DLL-Exportfunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4327b36990ac377595b31b55ebc0ed57157fd8d411f690aff3378293f35e39e6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119911130"
---
# <a name="expert-dll-export-functions"></a>Experten-DLL-Exportfunktionen

Die folgenden Funktionen sind die Einstiegspunkte für Experten-DLLs und für Aufrufe vom Betriebssystem und Netzwerkmonitor.



| Funktion                                   | Beschreibung                                                                                                                                                              |
|--------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DllMain Expert**](dllmain-expert.md)   | Gibt an, dass die Experten-DLL geladen oder entladen wurde. Wenn ein Prozess die DLL lädt oder entlädt, ruft das Betriebssystem die [**DllMain-Funktion**](/windows/desktop/Dlls/dllmain) auf. |
| [**Registrieren eines Experten**](register-expert.md) | Bestimmt grundlegende Informationen über den Experten innerhalb der DLL. Netzwerkmonitor ruft die **Register-Funktion** auf.                                                           |
| [**Konfigurieren**](configure.md)             | Konfiguriert den Experten innerhalb der DLL. Netzwerkmonitor ruft die [**Configure-Funktion auf.**](configure.md)                                                                 |
| [**Ausführung**](run.md)                         | Startet den Experten innerhalb der DLL. Netzwerkmonitor ruft die [**Run-Funktion auf.**](run.md)                                                                                 |



 

Netzwerkmonitor stellt auch Strukturen, Enumerationen und Hilfsfunktionen bereit, die der Experte aufrufen kann.



| Informationen über                                      | Finden Sie unter                                                                          |
|------------------------------------------------------------|------------------------------------------------------------------------------|
| Hilfsfunktionen, die von Experten und Parsern aufgerufen werden können | [Allgemeine Funktionen für Experten und Parser](expert-and-parser-common-functions.md) |
| Hilfsfunktionen, die nur von Experten aufgerufen werden           | [Expertenfunktionen](expert-functions.md)                                     |
| Strukturen, die von Expertenfunktionen verwendet werden               | [Expertenstrukturen](expert-structures.md)                                   |
| Enumerationen, die von Expertenstrukturen und -funktionen verwendet werden       | [Expertenenumerationen](expert-enumerations.md)                               |



 

 

 
