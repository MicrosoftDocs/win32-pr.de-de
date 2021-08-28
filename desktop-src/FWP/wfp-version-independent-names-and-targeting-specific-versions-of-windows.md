---
title: WFP Version-Independent- und Zielversionen von Windows
description: In vielen Fällen stellt die WFP-API (Windows Filtering Platform) mehrere Versionen einer Funktion oder Struktur bereit.
ms.assetid: FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: baf5fbef08c3284d94eb215e0cce2fc44fc9b827b686e531057db22b60020132
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119766670"
---
# <a name="wfp-version-independent-names-and-targeting-specific-versions-of-windows"></a>WFP Version-Independent- und Zielversionen von Windows

In vielen Fällen stellt die WFP-API (Windows Filtering Platform) mehrere Versionen einer Funktion oder Struktur bereit.

Die meisten Daten- und Funktionsnamen in der WFP-API enden mit einer Versionsnummer wie "0" oder "1", auch wenn nur eine Version vorhanden ist.

## <a name="version-mapping-in-fwpvih"></a>Versionszuordnung in "fwpvi.h"

Die Headerdatei fwpvi.h ist ab dem Windows 7 SDK und WDK enthalten. Diese Headerdatei ordnet den versionslosen API-Namen der Version zu, die für die Verwendung mit einem bestimmten Betriebssystem geeignet ist.

Hier sehen Sie beispielsweise einen kurzen Auszug aus der Version von fwpvi.h, die im Windows 8 SDK enthalten ist.


```C++
#define FwpmNetEventCreateEnumHandle FwpmNetEventCreateEnumHandle0
#if (NTDDI_VERSION >= NTDDI_WIN8)
#define FwpmNetEventEnum FwpmNetEventEnum2
#elif (NTDDI_VERSION >= NTDDI_WIN7)
#define FwpmNetEventEnum FwpmNetEventEnum1
#else
#define FwpmNetEventEnum FwpmNetEventEnum0
#endif
```



Wie oben gezeigt, gibt es nur eine Version von **FwpmNetEventCreateEnumHandle** – [**FwpmNetEventCreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventcreateenumhandle0) – daher ruft jeder Aufruf von **FwpmNetEventCreateEnumHandle** immer **FwpmNetEventCreateEnumHandle0** auf, unabhängig vom Zielbetriebssystem.

Es gibt jedoch drei Versionen von **FwpmNetEventEnum:** [**FwpmNetEventEnum0,**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum0) [**FwpmNetEventEnum1**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum1)und [**FwpmNetEventEnum2.**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum2) Die Headerdatei fwpvi.h stellt sicher, dass bei einem Aufruf von **FwpmNetEventEnum** die Version aufgerufen wird, die am besten für das Zielbetriebssystem geeignet ist:

-   [**FwpmNetEventEnum2**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum2) für Windows 8 (oder höher)
-   [**FwpmNetEventEnum1**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum1) für Windows 7 als Ziel
-   [**FwpmNetEventEnum0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum0) für frühere Betriebssysteme (z.B. Windows Vista oder Windows Vista mit Service Pack 1 (SP1))

## <a name="calling-version-independent-functions-and-structures"></a>Aufrufen von Version-Independent Funktionen und Strukturen

WFP-Entwicklern, die auf ein bestimmtes Betriebssystem oder eine bestimmte WDK-Version abzielen, wird empfohlen, immer für die versionsunabhängigen Makros zu programmieren. Dadurch wird automatisch die neueste Version ausgewählt, die in dem Betriebssystem unterstützt wird, das Sie als Ziel verwenden. Die Verwendung der neuesten Headerdateien wird empfohlen, auch wenn sie auf ein früheres Betriebssystem ausgerichtet sind. Dadurch wird sichergestellt, dass die neueste unterstützte Version verwendet wird, und sie kann auch die Verwaltung und Aktualisierung Ihres Codes vereinfachen.

Die [WFP-API-Referenzdokumentation](fwp-reference.md) beschreibt jede Version einer nummerierten API. Wenn mehrere Versionen vorhanden sind, wird das Zielbetriebssystem notiert. Entwickler möchten jedoch im Allgemeinen die versionsunabhängigen (nummerlosen) APIs aufrufen und das Zielbetriebssystem angeben (z. B. **NTDDI \_ WIN6** für Windows Vista oder **NTDDI \_ WIN8** für Windows 8).

Um eine ordnungsgemäße Behandlung von Funktionen sicherzustellen, die unterschiedliche Parameter in verschiedenen Versionen verwenden, können Sie bedingte Blöcke wie `#if (NTDDI_VERSION >= NTDDI_WIN7)` einschließen.

 

 




