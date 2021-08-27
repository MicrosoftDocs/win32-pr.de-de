---
description: In Winsock-Anwendungen ist ein Socketdeskriptor kein Dateideskriptor und muss mit den Winsock-Funktionen verwendet werden.
ms.assetid: bc434b35-9231-4b03-bc8f-cf59aaeb821e
title: Socketdatentyp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a95f890a14f68a0422ec91d31cb09735e2c85ab15cad52f9bd40499cee1167c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121240"
---
# <a name="socket-data-type"></a>Socketdatentyp

In Winsock-Anwendungen ist ein Socketdeskriptor kein Dateideskriptor und muss mit den Winsock-Funktionen verwendet werden.

In UNIX wird ein Socketdeskriptor durch einen Standarddateideskriptor dargestellt. Daher kann ein Socketdeskriptor für UNIX an eine der standardmäßigen Datei-E/A-Funktionen (z. B. Lesen und Schreiben) übergeben werden.

Darüber hinaus sind alle Handles in UNIX, einschließlich Sockethandles, kleine, nicht negative ganze Zahlen, und einige Anwendungen nehmen an, dass dies zutrifft.

Windows Sockethandles haben keine Einschränkungen, mit dem Anderen, dass der Wert INVALID \_ SOCKET kein gültiger Socket ist. Sockethandles können einen beliebigen Wert im Bereich von 0 bis INVALID \_ SOCKET-1 übernehmen.

Da der **SOCKET-Typ** nicht signiert ist, kann das Kompilieren von vorhandenem Quellcode beispielsweise aus einer UNIX-Umgebung zu Compilerwarnungen bei Nichtübereinstimmungen zwischen signierten und nicht signierten Datentypen führen.

Dies bedeutet beispielsweise, dass die [](/windows/desktop/api/Winsock2/nf-winsock2-socket) Überprüfung [](/windows/desktop/api/Winsock2/nf-winsock2-accept) auf Fehler, wenn die Socket- und Accept-Funktionen zurückgeben, nicht durchgeführt werden sollte, indem der Rückgabewert mit –1 verglichen wird oder ob der Wert negativ ist (sowohl gängige als auch rechtliche Ansätze in UNIX). Stattdessen sollte eine Anwendung die Manifestkonst constant INVALID \_ SOCKET verwenden, wie in der *Winsock2.h-Headerdatei* definiert. Beispiel:

Typischer BSD UNIX Stil


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

[Portieren von Socketanwendungen zu Winsock](porting-socket-applications-to-winsock.md)
</dt> <dt>

[Überlegungen zur Winsock-Programmierung](winsock-programming-considerations.md)
</dt> </dl>

 

 



