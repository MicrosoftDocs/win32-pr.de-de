---
title: Das aktuelle Modell in der Warteschlange ist veraltet.
description: Das aktuelle Modell in der Warteschlange ist veraltet.
ms.assetid: 271CD4F7-0992-47DB-AF5A-B77570EF681A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7cb1d4d07a824c2c6f9d0136259aec98b89c53e1320ceb6402241f881e312fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118211345"
---
# <a name="queued-present-model-is-being-deprecated"></a>Das aktuelle Modell in der Warteschlange ist veraltet.

## <a name="platforms"></a>Plattformen

**Clients** – Nach Windows 8  
**Server** – Nach Windows Server 2012  


## <a name="description"></a>Beschreibung

Im Windows Release nach Windows 8 geben diese APIs E \_ NOTIMPL zurück:

-   DwmSetPresentParameters
-   DwmSetDxFrameDuration
-   DwmModifyPreviousDxFrameDuration

Darüber hinaus akzeptiert diese API nur den NULL-Wert für den hwnd-Parameter:

-   DwmGetCompositionTimingInfo

Wir beenden die Unterstützung von DwmGetCompositionTimingInfo mit hwnd != NULL und entfernen die zugehörige Funktionalität. Wenn für hwnd ein Wert ungleich NULL angegeben wird, gibt diese API E \_ INVALIDARG zurück.

Wir raten auch von der Verwendung der DwmGetCompositionTimingInfo-API ab und empfehlen Entwicklern, zum DXGI-Flip-Modell und der zugehörigen DX Present Statistics-API zu wechseln.

## <a name="manifestation"></a>Manifestation

Anwendungen, die das in der Warteschlange enthaltene Modell verwenden, funktionieren nicht ordnungsgemäß. Der genaue Ablauf hängt von der jeweiligen Anwendung ab, kann aber von einem falschen Präsentationszeitpunkt bis zum unerwarteten Beenden der Anwendung reichen. In der Praxis erwarten wir nicht, dass viele (falls vorhanden) solche Anwendungen angezeigt werden. Dieses Modell wurde vom Vista-Medienplayer verwendet, der nicht auf Windows 8 (und möglicherweise auf dem alten Zune Player) verwendet wird. Zurzeit haben wir keine Informationen zu anderen Anwendungen, die dieses Modell tatsächlich verwenden.

## <a name="solution"></a>Lösung

Entwickler müssen den DXGI-Flip-Präsentationsmodus anstelle der in der Warteschlange vorhandenen (verfügbar in der DX9-Runtime seit Windows 7 und auf DX10- und DX11-Runtimes in Windows 8) verwenden.

## <a name="tests"></a>Tests

Führen Sie allgemeine Tests aus, um sicherzustellen, dass der Posteingang Windows Komponenten und Hauptprodukte weiterhin mit der nächsten Version von Windows funktioniert.

 

 




