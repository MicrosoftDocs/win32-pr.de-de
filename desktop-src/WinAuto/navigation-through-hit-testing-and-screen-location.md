---
title: Navigation durch Treffertests und Bildschirmposition
description: Clients können Testpunkte auf dem Bildschirm erreichen, um die untergeordneten Elemente eines Objekts zu finden oder die Größe eines Objekts zu bestimmen.
ms.assetid: ba08814f-87bc-4b47-8b61-179a48d5092f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34911b13a4c9bad2bfd79cb32d5654265878568ad00475ade08a87a23150b49f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118828272"
---
# <a name="navigation-through-hit-testing-and-screen-location"></a>Navigation durch Treffertests und Bildschirmposition

Clients können Testpunkte auf dem Bildschirm erreichen, um die untergeordneten Elemente eines Objekts zu finden oder die Größe eines Objekts zu bestimmen. Es sind zwei Methoden verfügbar:

-   [**IAccessible::accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**IAccessible::accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)

## <a name="using-iaccessibleacchittest"></a>Verwenden von IAccessible::accHitTest

Clients rufen die [**IAccessible::accHitTest-Methode**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest) des übergeordneten Objekts auf und übergeben die Bildschirmkoordinaten des punkts, der getestet werden soll, um zu ermitteln, ob sich ein Punkt innerhalb eines Objekts, innerhalb seines untergeordneten Objekts oder keiner davon befindet. In der folgenden Liste werden einige typische Szenarien beschrieben:

-   Wenn sich die untergeordneten Elemente des Objekts an einem angegebenen Punkt überschneiden, ruft [**IAccessible::accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest) das oberste untergeordnete Element ab, das visuell den Raum belegt.
-   Wenn ein Fenster ein untergeordnetes Element verdeckt oder das untergeordnete Element vom übergeordneten Element abgeschnitten wird, wird das untergeordnete Element beim Treffertest vom abgedeckten Punkt abgerufen, obwohl es nicht sichtbar ist.
-   Wenn das untergeordnete Element, das am angegebenen Punkt gefunden wird, ein barrierefreies Objekt ist, im Gegensatz zu einem untergeordneten Element, gibt die Methode die [**IDispatch-Schnittstelle**](idispatch-interface.md) des untergeordneten Elements zurück.

## <a name="using-iaccessibleacclocation"></a>Verwenden von IAccessible::accLocation

Clients rufen [**IAccessible::accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)auf, um die Bildschirmposition eines Objekts oder eines untergeordneten Objekts abzurufen. Diese Methode gibt die Koordinaten des umgrenzenden Rechtecks des angegebenen Objekts zurück. Wenn das Objekt nicht wie ein Rechteck gestaltet ist, gibt die Methode die Koordinaten des kleinsten Rechtecks zurück, das das gesamte Objekt umfasst.

Die folgende Abbildung zeigt die Beziehung zwischen dem Bereich eines nicht rechteckigen Objekts und seinem umschließenden Rechteck.

![Abbildung, die den Bereich eines nicht ectangular-Objekts (einen Kreis) und sein umschließendes Rechteck zeigt.](images/region.gif)

> [!Note]  
> [**IAccessible::accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest) ist präziser als [**IAccessible::accLocation,**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation) da Clients damit die Position von Objekten pixelweise bestimmen können, anstatt mit umgrenzten Rechtecke. Diese Genauigkeit ist beispielsweise nützlich, wenn eine Anwendung Informationen sammelt, indem sie die Position des Mauszeigers nachverfolgung.

 

 

 




