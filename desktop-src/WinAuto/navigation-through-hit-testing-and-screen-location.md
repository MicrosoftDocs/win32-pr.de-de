---
title: Navigation durch Treffer Tests und Bildschirmposition
description: Um die untergeordneten Elemente eines Objekts zu suchen oder die Größe eines Objekts zu ermitteln, können Clients auf dem Bildschirm auf Testpunkte zugreifen.
ms.assetid: ba08814f-87bc-4b47-8b61-179a48d5092f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c26d055246e038611e881bd353bcc865c5e77136
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341443"
---
# <a name="navigation-through-hit-testing-and-screen-location"></a>Navigation durch Treffer Tests und Bildschirmposition

Um die untergeordneten Elemente eines Objekts zu suchen oder die Größe eines Objekts zu ermitteln, können Clients auf dem Bildschirm auf Testpunkte zugreifen. Es stehen zwei Methoden zur Verfügung:

-   [**IAccessible:: accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**IAccessible:: accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)

## <a name="using-iaccessibleacchittest"></a>Verwenden von IAccessible:: accHitTest

Um zu ermitteln, ob sich ein Punkt innerhalb eines Objekts innerhalb seines untergeordneten Elements befindet, wird die [**IAccessible:: accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest) -Methode des übergeordneten Objekts aufgerufen, und die Bildschirm Koordinaten des Punkts, der auf Treffer getestet werden soll, werden übergeben. In der folgenden Liste werden einige typische Szenarien beschrieben:

-   Wenn die untergeordneten Elemente des Objekts sich an einem angegebenen Punkt überlappen, ruft [**IAccessible:: accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest) das oberste untergeordnete Element ab, das visuell angezeigt wird, um den Bereich zu belegen.
-   Wenn ein Fenster ein untergeordnetes Element abdeckt oder wenn das untergeordnete Element durch das übergeordnete Element abgeschnitten wird, wird beim durch Klicken auf den abgedeckten Punkt das untergeordnete Element abgerufen, auch wenn es nicht sichtbar ist.
-   Wenn das am angegebenen Punkt gefundene untergeordnete Element ein Barrierefreies Objekt ist, und nicht auf ein untergeordnetes Element, gibt die Methode die [**IDispatch**](idispatch-interface.md) -Schnittstelle des untergeordneten Elements zurück.

## <a name="using-iaccessibleacclocation"></a>Verwenden von IAccessible:: accLocation

Um die Bildschirmposition eines Objekts oder eines der untergeordneten Elemente des Objekts abzurufen, wird " [**IAccessible:: accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)" aufgerufen. Diese Methode gibt die Koordinaten des umgebenden Rechtecks des angegebenen Objekts zurück. Wenn das Objekt nicht wie ein Rechteck geformt ist, gibt die Methode die Koordinaten des kleinsten Rechtecks zurück, das das gesamte Objekt umfasst.

Die folgende Abbildung zeigt die Beziehung zwischen dem Bereich eines nicht rechteckigen Objekts und seinem umschließenden Rechteck.

![Abbildung der Darstellung eines nicht rechteckigen Objekts (eines Kreises) und seines umschließenden Rechtecks.](images/region.gif)

> [!Note]  
> [**IAccessible:: accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest) ist präziser als [**IAccessible:: accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation) , da Clients den Speicherort von Objekten auf Pixel-für-Pixel-Basis anstelle von Begrenzungs Rechtecke ermitteln können. Diese Genauigkeit ist beispielsweise hilfreich, wenn eine Anwendung Informationen durch Nachverfolgung der Position des Mauszeigers sammelt.

 

 

 




