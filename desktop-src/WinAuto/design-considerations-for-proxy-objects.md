---
title: Entwurfsüberlegungen für Proxyobjekte
description: Der Entwurf von Proxyobjekten und barrierefreien Objekten hängt vom Entwurf der Benutzeroberflächenelemente des Servers ab. Unabhängig vom Entwurf muss ein Benutzeroberflächenelement sein Proxyobjekt direkt benachrichtigen, bevor es zerstört wird, damit das Proxyobjekt Aufrufe von Clients entsprechend verarbeitet.
ms.assetid: 83a9ff66-2fe6-4589-a187-cdaf207b02b8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0cd96056f89e1efc18da3e299a76e92c85166efd7067e54f972a69eb8786d57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118830071"
---
# <a name="design-considerations-for-proxy-objects"></a>Entwurfsüberlegungen für Proxyobjekte

Der Entwurf von Proxyobjekten und barrierefreien Objekten hängt vom Entwurf der Benutzeroberflächenelemente des Servers ab. Unabhängig vom Entwurf muss ein Benutzeroberflächenelement sein Proxyobjekt direkt benachrichtigen, bevor es zerstört wird, damit das Proxyobjekt Aufrufe von Clients entsprechend verarbeitet.

In der folgenden Liste werden zwei Entwurfsmöglichkeiten beschrieben:

-   Platzieren Sie den Code, der die [**IAccessible-Schnittstelle**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) implementiert, im selben Modul wie den Code, der das Benutzeroberflächenelement implementiert, wenn der Benutzeroberflächencode leicht erweiterbar ist. In diesem Fall ist der Proxy in dem Sinne "einfach", dass er nur die Lebensdauer des barrierefreien Objekts überwacht, Aufrufe an das barrierefreie Objekt weiterlädt und die Ergebnisse zurücksingt.
-   Platzieren Sie den Code, der [**IAccessible implementiert,**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) im selben Modul wie den Code, der das Proxyobjekt implementiert. In diesem Fall verwendet das barrierefreie Objekt interne Funktionen, um Informationen zum Benutzeroberflächenelement zu erhalten.

## <a name="trackbar-controls"></a>Trackbar-Steuerelemente

Verwenden Sie beim Implementieren von Trackbar-Steuerelementen **tbs \_ REVERSED** im Trackleistenstil, um aussagekräftigere Informationen zu liefern. Dieser Stil kehrt die von [**IAccessible::get \_ accValue verwendete Skalierung um.**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue)

Bei vertikalen Trackbars ohne diesen Stil gibt [**IAccessible::get \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue) null (0) zurück, wenn sich der Trackbar-Strich am oberen Rand des Steuerelements befindet. Die Werte erhöhen sich, wenn Sie den Daumen nach unten schieben. Mit **dem TBS \_ REVERSED-Stil** gibt **IAccessible::get \_ accValue** hundert (100) zurück, wenn sich der Trackleistenfinger oben befindet. Die Zahlen verringern sich, wenn Sie den Trackbar- Thumb nach unten bewegen.

Bei horizontalen Trackbars ohne diesen Stil wird null (0) zurückgegeben, wenn sich der Trackleistenfinger am linken Ende des Steuerelements befindet. Die Werte erhöhen sich, wenn Sie den Trackbar- Thumb nach rechts verschieben. Beim **TBS \_ REVERSED-Format** gibt [**IAccessible::get \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue) hundert (100) zurück, wenn sich der Trackleistenfinger links befindet. Die Werte verringern sich, wenn Sie den Trackleistenfinger nach rechts verschieben.

 

 




