---
title: Tool Hilfefunktionen
description: Listet die Funktionen der Tool Hilfe Bibliothek auf.
ms.assetid: 83732bd6-f4cf-409d-ad17-86503d408dc3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54f9d95598f9b48343ea9731e1a826fb147a73a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037467"
---
# <a name="tool-help-functions"></a>Tool Hilfefunktionen

Die folgenden Funktionen sind Teil der Tool Hilfe Bibliothek.



| Funktion                                                           | BESCHREIBUNG                                                                                                      |
|--------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [**CreateToolhelp32Snapshot**](/windows/desktop/api/TlHelp32/nf-tlhelp32-createtoolhelp32snapshot)       | Erstellt eine Momentaufnahme der angegebenen Prozesse sowie die Heaps, Module und Threads, die von diesen Prozessen verwendet werden. |
| [**Heap32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32first)                                 | Ruft Informationen zum ersten Block eines Heaps ab, der von einem Prozess zugeordnet wurde.                      |
| [**Heap32ListFirst**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32listfirst)                         | Ruft Informationen zum ersten Heap ab, der durch einen angegebenen Prozess zugeordnet wurde.                       |
| [**Heap32ListNext**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32listnext)                           | Ruft Informationen über den nächsten Heap ab, der von einem Prozess zugeordnet wurde.                                  |
| [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next)                                   | Ruft Informationen über den nächsten Block eines Heaps ab, der von einem Prozess zugeordnet wurde.                       |
| [**Module32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32first)                             | Ruft Informationen zum ersten Modul ab, das einem Prozess zugeordnet ist.                                          |
| [**Module32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32next)                               | Ruft Informationen zum nächsten Modul ab, das einem Prozess oder Thread zugeordnet ist.                                 |
| [**Process32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32first)                           | Ruft Informationen zum ersten Prozess ab, der in einer System Momentaufnahme aufgetreten ist.                                  |
| [**Process32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32next)                             | Ruft Informationen zum nächsten Prozess ab, der in einer System Momentaufnahme aufgezeichnet wurde.                                      |
| [**Thread32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32first)                             | Ruft Informationen über den ersten Thread eines Prozesses ab, der in einer System Momentaufnahme aufgetreten ist.                    |
| [**Thread32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32next)                               | Ruft Informationen über den nächsten Thread eines Prozesses ab, der in der Momentaufnahme des System Speichers aufgetreten ist.            |
| [**Toolhelp32ReadProcessMemory**](/windows/desktop/api/TlHelp32/nf-tlhelp32-toolhelp32readprocessmemory) | Kopiert Speicher, der einem anderen Prozess zugeordnet ist, in einen von der Anwendung bereitgestellten Puffer.                                  |



 

 

 




