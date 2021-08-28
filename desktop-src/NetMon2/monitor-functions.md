---
description: In diesem Abschnitt werden die Hilfsfunktionen beschrieben, die Sie zum Entwickeln benutzerdefinierter Monitore verwenden können.
ms.assetid: 2c019183-9823-4e34-bb41-cf35f2731b8f
title: Überwachen von Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f4a46aff05c9d8775edf5bb233cb18f288dc7ba4d65ba0300370ee7ede3a2ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119677100"
---
# <a name="monitor-functions"></a>Überwachen von Funktionen

In diesem Abschnitt werden die Hilfsfunktionen beschrieben, die Sie zum Entwickeln benutzerdefinierter Monitore verwenden können.



| Funktion                                       | BESCHREIBUNG                                                                                                                                                      |
|------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [DllGetMonitorObject](dllgetmonitorobject.md) | Erstellt eine Instanz des Monitors.                                                                                                                              |
| [HTMLValueToUnicode](htmlvaluetounicode.md)   | Konvertiert eine \_ HTML-CP-UTF8-Versionszeichenfolge in Unicode.                                                                                                             |
| [LoadDWORD](loaddword.md)                     | Lädt **ein DWORD** aus einer HTML-Konfigurationszeichenfolge.                                                                                                             |
| [LoadIPAddresses](loadipaddresses.md)         | Lädt eine IP-Adressliste aus einer HTML-TEXTAREA-Konfigurationszeichenfolge.                                                                                             |
| [LoadIPXAddresses](loadipxaddresses.md)       | Lädt eine IPX-Adressliste aus einer HTML-TEXTAREA-Konfigurationszeichenfolge.                                                                                            |
| [LoadMACAddresses](loadmacaddresses.md)       | Lädt eine MAC-Adressliste aus einer HTML-TEXTAREA-Konfigurationszeichenfolge.                                                                                             |
| [LoadStringAddr](loadstringaddr.md)           | Transformiert eine Zeichenfolge (z. B. "157.54.32.45") in eine **DWORD-Adresse.**                                                                                             |
| [LoadTCHAR](loadtchar.md)                     | Sucht nach einem angeforderten Variablennamen in der Konfigurationszeichenfolge und weist ausreichend Speicherplatz zu (mithilfe von **HeapAllocMemory**), um ihn zu speichern, zu kopieren und zurückgibt. |
| [OnLoadingDLL](onloadingdll.md)               | Gibt an, dass das Laden der DLL begonnen hat. McSVC ruft diese Funktion auf, wenn die Monitor-DLL zum ersten Mal geladen wird.                                                     |



 

 

 



