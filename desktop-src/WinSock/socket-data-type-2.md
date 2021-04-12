---
description: In Winsock-Anwendungen ist ein socketdeskriptor kein Dateideskriptor und muss mit den Winsock-Funktionen verwendet werden.
ms.assetid: bc434b35-9231-4b03-bc8f-cf59aaeb821e
title: Socket-Datentyp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea031032e0d05abc02f7c3c948477c7fe9a1d1de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347068"
---
# <a name="socket-data-type"></a>Socket-Datentyp

In Winsock-Anwendungen ist ein socketdeskriptor kein Dateideskriptor und muss mit den Winsock-Funktionen verwendet werden.

In Unix wird ein socketdeskriptor durch einen Standarddatei Deskriptor dargestellt. Folglich kann ein socketdeskriptor unter UNIX an jede der standardmäßigen Datei-e/a-Funktionen (z. b. lesen und schreiben) weitergegeben werden.

Außerdem sind alle Handles in UNIX, einschließlich Sockethandles, kleine, nicht negative ganze Zahlen, und einige Anwendungen treffen Annahmen, dass dies zutrifft.

Windows Sockets-Handles haben keine Einschränkungen, außer dass der Wert ungültiger \_ Socket kein gültiger Socket ist. Sockethandles können einen beliebigen Wert im Bereich 0 bis zu einem ungültigen \_ Socket – 1 annehmen.

Da der **socketyp** nicht signiert ist, kann das Kompilieren von vorhandenem Quellcode aus, z. b. eine UNIX-Umgebung, zu Compilerwarnungen zu nicht übereinstimmenden, nicht signierten Datentyp Konflikten führen.

Dies bedeutet beispielsweise, dass die Überprüfung auf Fehler bei Rückgabe der [**Socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) -und [**Accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept) -Funktionen nicht durchgeführt werden soll, indem der Rückgabewert mit – 1 verglichen wird, oder ob der Wert negativ ist (sowohl gängige als auch rechtliche Ansätze in Unix). Stattdessen sollte eine Anwendung die \_ in der Header Datei " *Winsock2. h* " definierte Manifest-Konstante mit ungültigem Socket verwenden. Beispiel:

Typischer BSD-Unix-Stil


```C++
s = socket(...);
if (s == -1)    /* or s < 0 */
    {/*...*/}
```



Bevorzugter Stil


```C++
s = socket(...);
if (s == INVALID_SOCKET)
    {/*...*/}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Portieren von Socketanwendungen auf Winsock](porting-socket-applications-to-winsock.md)
</dt> <dt>

[Überlegungen zur Winsock-Programmierung](winsock-programming-considerations.md)
</dt> </dl>

 

 



