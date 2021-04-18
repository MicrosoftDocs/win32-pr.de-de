---
title: Ein in der Warteschlange vorhandenes Modell ist veraltet.
description: Ein in der Warteschlange vorhandenes Modell ist veraltet.
ms.assetid: 271CD4F7-0992-47DB-AF5A-B77570EF681A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5713009cd5cd3a575d0d634f81fce7a289d1c1c
ms.sourcegitcommit: 46376be61d3fa308f9b1a06d7e2fa122a39755af
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "106338097"
---
# <a name="queued-present-model-is-being-deprecated"></a>Ein in der Warteschlange vorhandenes Modell ist veraltet.

## <a name="platforms"></a>Plattformen

**Clients** – nach Windows 8  
**Server** – nach Windows Server 2012  


## <a name="description"></a>BESCHREIBUNG

In der Windows-Version nach Windows 8 geben diese APIs E \_ notimpl zurück:

-   Dwmsetpresentparameters
-   Dwmsetdxframeduration
-   Dwmmodifypreviousdxframeduration

Außerdem akzeptiert diese API nur den NULL-Wert für den HWND-Parameter:

-   Dwmgetcompositiontiminginfo

Die Unterstützung von dwmgetcompositiontiminginfo mit HWND! = NULL wird beendet, und die zugehörige Funktionalität wird entfernt. Wenn ein nicht-NULL-Wert für HWND angegeben wird, gibt diese API E \_ invalidArg zurück.

Außerdem wird die Verwendung der dwmgetcompositiontiminginfo-API davon abgeraten, und es wird empfohlen, dass Entwickler zum DXGI-Flip-Modell und der zugehörigen DX-Statistik-API wechseln.

## <a name="manifestation"></a>Ausstrahlung

Anwendungen, die das in der Warteschlange stehende Modell verwenden, funktionieren nicht ordnungsgemäß. Die genaue Manifestation hängt von der jeweiligen Anwendung ab, kann jedoch von einer falschen Präsentationszeit bis hin zu einer unerwarteten Beendigung der Anwendung reichen. In der Praxis erwarten wir nicht, dass es sich um solche Anwendungen handelt. Dieses Modell wurde von Vista Media Player verwendet, das nicht unter Windows 8 (und möglicherweise dem alten Zune-Player) verwendet wird. Zurzeit sind keine Informationen zu anderen Anwendungen vorhanden, die dieses Modell tatsächlich verwenden.

## <a name="solution"></a>Lösung

Entwickler müssen den DXGI-Modus für die Flip-Darstellung anstelle der in der Warteschlange befindlichen Zeit (verfügbar in der DX9-Laufzeit seit Windows 7 und in Version DX10 und DX11-Laufzeiten in Windows 8) verwenden.

## <a name="tests"></a>Tests

Führen Sie allgemeine Tests aus, um sicherzustellen, dass Eingangsbox-Windows-Komponenten und wichtige Produkte weiterhin unter der nächsten Version von Windows funktionieren

 

 




