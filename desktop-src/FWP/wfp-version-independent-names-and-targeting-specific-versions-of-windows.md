---
title: WFP-Version-Independent Namen und für bestimmte Versionen von Windows
description: In vielen Fällen stellt die Windows-Filter Plattform-API (WFP) mehr als eine Version einer Funktion oder Struktur bereit.
ms.assetid: FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41be83a50b4786aa4b98cd7f8dd7405a33fe94be
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341218"
---
# <a name="wfp-version-independent-names-and-targeting-specific-versions-of-windows"></a>WFP-Version-Independent Namen und für bestimmte Versionen von Windows

In vielen Fällen stellt die Windows-Filter Plattform-API (WFP) mehr als eine Version einer Funktion oder Struktur bereit.

Die meisten Daten-und Funktionsnamen in der WFP-API enden mit einer Versionsnummer, z. b. "0" oder "1", auch wenn nur eine Version vorhanden ist.

## <a name="version-mapping-in-fwpvih"></a>Versions Zuordnung in "f. h"

Die Header Datei "swpvi. h" ist ab dem Windows 7 SDK und dem WDK enthalten. Diese Header Datei ordnet den Namen der versionlosen API der Version zu, die für die Verwendung mit einem bestimmten Betriebssystem geeignet ist.

Hier ist beispielsweise ein kurzer Auszug aus der Version von "f. h", die im Windows 8 SDK enthalten ist.


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



Wie oben gezeigt, gibt es nur eine Version von **fwpmneteventkreateenumhandle** – [**FwpmNetEventCreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventcreateenumhandle0) – daher wird jeder **fwpmneteventkreateenumhandle** -Befehl immer **FwpmNetEventCreateEnumHandle0** aufrufen, unabhängig vom Ziel des Betriebssystems.

Es gibt jedoch drei Versionen von von " **f**", " [**FwpmNetEventEnum0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum0)", " [**FwpmNetEventEnum1**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum1)" und " [**FwpmNetEventEnum2**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum2)". Die Header Datei "fwpvi. h" stellt sicher, dass ein Aufrufen von **fwpmneteventerum** die Version aufruft, die für das Ziel Betriebssystem am besten geeignet ist:

-   [**FwpmNetEventEnum2**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum2) für Windows 8 (oder höher)
-   [**FwpmNetEventEnum1**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum1) für Windows 7 ist Ziel
-   [**FwpmNetEventEnum0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum0) für frühere Betriebssysteme (z. b. Windows Vista oder Windows Vista mit Service Pack 1 (SP1))

## <a name="calling-version-independent-functions-and-structures"></a>Aufrufen von Version-Independent-Funktionen und-Strukturen

Für WFP-Entwickler, die auf ein bestimmtes Betriebssystem oder eine WDK-Version abzielen, wird empfohlen, immer für Versions unabhängige Makros zu programmieren. Dadurch wird automatisch die aktuellste Version ausgewählt, die im Ziel Betriebssystem unterstützt wird. Die Verwendung der neuesten Header Dateien wird empfohlen, selbst wenn ein älteres Betriebssystem als Ziel verwendet wird. Dadurch wird sichergestellt, dass die neueste unterstützte Version verwendet wird, und Sie können den Code leichter verwalten und aktualisieren.

In der [WFP-API-Referenz Dokumentation](fwp-reference.md) werden die einzelnen Versionen einer nummerierten API beschrieben. Wenn mehr als eine Version vorhanden ist, wird das Ziel Betriebssystem notiert. Entwickler möchten jedoch in der Regel die Versions unabhängigen (zahllosen) APIs aufzurufen und das Ziel Betriebssystem angeben (z. b. **ntddi \_ WIN6** für Windows Vista oder **ntddi \_ WIN8** für Windows 8).

Um die ordnungsgemäße Handhabung von Funktionen sicherzustellen, die verschiedene Parameter in verschiedenen Versionen verwenden, können Sie bedingte Blöcke wie einschließen `#if (NTDDI_VERSION >= NTDDI_WIN7)` .

 

 




