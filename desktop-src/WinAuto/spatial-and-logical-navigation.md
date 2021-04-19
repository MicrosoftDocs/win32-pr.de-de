---
title: Räumliche und logische Navigation
description: Clients rufen Informationen zu einem Objekt, das räumlich oder logisch in der Nähe eines anderen Objekts innerhalb desselben Containers ist, durch Aufrufen von "ibarrierefreie accNavigate" und Angeben einer der Navigations Konstanten ab.
ms.assetid: a1ebb50e-76cf-472d-bb0f-3f5bf5ed30d5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b9e49772a267e49d723a04005dcbc8a369510b3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106338679"
---
# <a name="spatial-and-logical-navigation"></a>Räumliche und logische Navigation

Clients rufen Informationen zu einem Objekt, das räumlich oder logisch in der Nähe eines anderen Objekts innerhalb desselben Containers ist, durch Aufrufen von [**IAccessible:: accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) und Angeben einer der [Navigations Konstanten](navigation-constants.md)ab.

Mit *räumlichen Navigations* Clients navigieren Sie auf dem Bildschirm zu einem Objekt. Clients Navigieren nach oben, unten, Links oder rechts vom aktuellen Objekt, um Informationen über ein anderes Objekt innerhalb desselben Containers abzurufen.

Bei der *logischen Navigation* navigieren Clients zu dem Objekt, das einem anderen, vom Server festgelegten Objekt logisch voransteht oder diesem folgt. Clients Navigieren auf zweierlei Weise zu allen untergeordneten Elementen des Objekts:

-   Starten Sie die Navigation mit [**navDir \_ FirstChild**](navigation-constants.md) , und klicken Sie dann wiederholt mit [**navDir \_ Next**](navigation-constants.md)auf die-Methode.
-   Starten Sie die Navigation mit [**navDir \_ LastChild**](navigation-constants.md) , und nennen Sie die Methode wiederholt mit [**navDir \_ Previous**](navigation-constants.md).

Unabhängig von der Richtung besucht die Navigation jedes sichtbare untergeordnete Element, das zu dem übergeordneten Objekt gehört. Unsichtbare untergeordnete Elemente können mit logischer Navigation übersprungen werden. Außerdem wird jedes untergeordnete Element nur einmal besucht, und die Navigation führt nicht zu einer Schleife. Das heißt, die Methode schlägt fehl, wenn ein Client versucht, vor dem ersten oder nach dem letzten Objekt zu navigieren.

Räumliche und logische Navigation sind miteinander verknüpft. Beispielsweise sollte in einer horizontalen Symbolleiste das Aufrufen der-Methode mit [**navDir \_ right**](navigation-constants.md) die gleichen Ergebnisse wie das Aufrufen der-Methode mit [**navDir \_ Next**](navigation-constants.md)erzielen.

Das Start Objekt der Navigation ist entweder das Objekt, das es **selbst oder eines der unter** geordneten Elemente des Objekts ist, mit dem Unterschied, dass entweder [**navDir \_ FirstChild**](navigation-constants.md) oder [**navDir \_ LastChild**](navigation-constants.md) angegeben wird. in diesem Fall muss die Navigation mit dem Objekt selbst beginnen.

Wenn ein Client von einem zugänglichen Objekt zu einem gleich geordneten Benutzeroberflächen Element navigiert oder wenn das **LVAL** -Element von *varstart* auf **childID \_ Self** und das angegebene Flag in *navDir* ein beliebiges Navigationsflag mit Ausnahme von [**navDir \_ FirstChild**](navigation-constants.md) oder [**navDir \_ LastChild**](navigation-constants.md)ist, ist das Ergebnis in *pvarend* entweder eine untergeordnete ID oder eine [**IDispatch**](idispatch-interface.md) -Schnittstelle. Wenn *pvarend* eine untergeordnete ID enthält, müssen Clients zuerst einen Zeiger auf die [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstelle des übergeordneten Elements abrufen, um von diesem Benutzeroberflächen Element zu navigieren oder weitere Informationen darüber zu erhalten. Um das übergeordnete Objekt zu erhalten, rufen Clients die [**IAccessible:: get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) -Eigenschaft des neben geordneten Objekts oder das Start Objekt der Navigation auf.

Beachten Sie, dass Clients Informationen zu allen gleitenden Objekten erhalten müssen, indem Sie die [**enumchildwindows**](/windows/desktop/api/winuser/nf-winuser-enumchildwindows) -Funktion aufrufen. Da ein Gleit Komma Objekt nicht auf das übergeordnete Objekt zugeschnitten ist, haben Clients keine Informationen über die hierarchische Beziehung zwischen zwei Objekten auf dem Bildschirm.

Die folgende Grafik ist ein Beispiel für ein Gleit Komma Objekt, das nicht auf das übergeordnete Element zugeschnitten ist.

![Screenshot des geöffneten Fensters, das über einem größeren Microsoft Developer Studio-Fenster schwebt](images/floatob.gif)

## <a name="establishing-the-order-in-logical-navigation"></a>Festlegen der Reihenfolge in der logischen Navigation

Bei der logischen Navigation stellen die Entwickler, die die Objekte entwerfen, die Beziehungen zwischen ihnen her. Die logische Navigation ist subjektiver als die räumliche Navigation. Außerdem ist die Reihenfolge in der logischen Navigation nicht mit der Reihenfolge identisch, in der die untergeordneten IDs verwendet werden.

Bei Objekten, die über Bildschirm Positionen verfügen, sollten Server Entwickler die Navigations Reihenfolge so einrichten, dass Sie logisch in Erwägung gezogen werden. In englischsprachigen Ländern bzw. Regionen bedeutet dies beispielsweise eine von links nach rechts und von oben nach unten sorordnete Reihenfolge.

Die logische Navigations Reihenfolge muss eine parallele Tastaturnavigation haben. Ein Dialogfeld enthält z. b. die Schaltflächen **OK** und **Abbrechen** und einige Bearbeitungs Steuerelemente. Ein Client, der [**IAccessible:: accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) aufruft, um zum nächsten oder vorherigen Objekt in diesem Dialogfeld zu navigieren, wird in derselben Reihenfolge verschoben wie ein Benutzer mit der Tab-Taste oder UMSCHALT + TAB, um den Fokus zwischen Elementen zu verschieben.

Bei Objekten, die nicht über definierte Bildschirm Positionen verfügen, wird die logische Reihenfolge von Server Entwicklern bestimmt, und Client Entwickler sollten keine Annahmen darüber treffen. Beispielsweise ist es zulässig, dass nicht sichtbare Objekte, wie z. b. Objekte, die nur vorübergehend ausgeblendet sind, mit sichtbaren Objekten vermischt werden.

 

 