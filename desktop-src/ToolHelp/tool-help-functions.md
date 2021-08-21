---
title: Toolhilfefunktionen
description: Listet die Funktionen der Toolhilfsbibliothek auf.
ms.assetid: 83732bd6-f4cf-409d-ad17-86503d408dc3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d73cc425f415c9cea8af9290743fb1afbb51182f8c03e7ec087ca95948fd2ebc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119058218"
---
# <a name="tool-help-functions"></a>Toolhilfefunktionen

Die folgenden Funktionen sind Teil der Toolhilfebibliothek.



| Funktion                                                           | Beschreibung                                                                                                      |
|--------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [**CreateToolhelp32Snapshot**](/windows/desktop/api/TlHelp32/nf-tlhelp32-createtoolhelp32snapshot)       | Erstellt eine Momentaufnahme der angegebenen Prozesse sowie der Heaps, Module und Threads, die von diesen Prozessen verwendet werden. |
| [**Heap32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32first)                                 | Ruft Informationen zum ersten Block eines Heaps ab, der von einem Prozess zugeordnet wurde.                      |
| [**Heap32ListFirst**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32listfirst)                         | Ruft Informationen zum ersten Heap ab, der von einem angegebenen Prozess zugeordnet wurde.                       |
| [**Heap32ListNext**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32listnext)                           | Ruft Informationen zum nächsten Heap ab, der von einem Prozess zugeordnet wurde.                                  |
| [**Heap32Weiter**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next)                                   | Ruft Informationen zum nächsten Block eines Heaps ab, der von einem Prozess zugeordnet wurde.                       |
| [**Module32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32first)                             | Ruft Informationen zum ersten Modul ab, das einem Prozess zugeordnet ist.                                          |
| [**Module32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32next)                               | Ruft Informationen zum nächsten Modul ab, das einem Prozess oder Thread zugeordnet ist.                                 |
| [**Process32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32first)                           | Ruft Informationen zum ersten Prozess ab, der in einer Systemmomentaufnahme aufgetreten ist.                                  |
| [**Process32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32next)                             | Ruft Informationen zum nächsten Prozess ab, der in einer Systemmomentaufnahme aufgezeichnet wird.                                      |
| [**Thread32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32first)                             | Ruft Informationen zum ersten Thread eines Prozesses ab, der in einer Systemmomentaufnahme gefunden wurde.                    |
| [**Thread32Weiter**](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32next)                               | Ruft Informationen zum nächsten Thread eines Prozesses ab, der in der Systemspeichermomentaufnahme gefunden wird.            |
| [**Toolhelp32ReadProcessMemory**](/windows/desktop/api/TlHelp32/nf-tlhelp32-toolhelp32readprocessmemory) | Kopiert Arbeitsspeicher, der einem anderen Prozess zugeordnet ist, in einen von der Anwendung bereitgestellten Puffer.                                  |



 

 

 




