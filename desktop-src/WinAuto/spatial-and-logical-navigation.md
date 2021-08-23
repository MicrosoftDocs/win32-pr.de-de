---
title: Räumliche und logische Navigation
description: Clients rufen Informationen zu einem Objekt ab, das sich räumlich oder logisch in der Nähe eines anderen Objekts innerhalb desselben Containers befindet, indem sie IAccessible accNavigate aufrufen und eine der Navigationskonstanten angeben.
ms.assetid: a1ebb50e-76cf-472d-bb0f-3f5bf5ed30d5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d762352c41f2adc764ac40c052632922a25ca995b9f2ec2f5008c668d0332bfd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052502"
---
# <a name="spatial-and-logical-navigation"></a>Räumliche und logische Navigation

Clients rufen Informationen zu einem Objekt ab, das sich räumlich oder logisch in der Nähe eines anderen Objekts innerhalb desselben Containers befindet, indem [**sie IAccessible::accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) aufrufen und eine der [Navigationskonstanten](navigation-constants.md)angeben.

Bei *der räumlichen Navigation* navigieren Clients basierend auf seiner Position auf dem Bildschirm zu einem Objekt. Clients navigieren vom aktuellen Objekt nach oben, unten, links oder rechts, um Informationen zu einem anderen Objekt innerhalb desselben Containers abzurufen.

Mit *der logischen Navigation* navigieren Clients zu dem Objekt, das einem anderen Objekt logisch vorausgeht oder einem anderen Objekt folgt, wie vom Server bestimmt. Clients navigieren auf zwei Arten zu allen untergeordneten Objekten eines Objekts:

-   Starten Sie die Navigation mit [**NAVDIR \_ FIRSTCHILD,**](navigation-constants.md) und rufen Sie dann wiederholt die -Methode mit [**NAVDIR \_ NEXT**](navigation-constants.md)auf.
-   Starten Sie die Navigation mit [**NAVDIR \_ LASTCHILD,**](navigation-constants.md) und rufen Sie die -Methode wiederholt mit [**NAVDIR \_ PREVIOUS**](navigation-constants.md)auf.

Unabhängig von der Richtung besucht die Navigation jedes sichtbare untergeordnete Element, das zum übergeordneten Objekt gehört. Unsichtbare untergeordnete Elemente können mit logischer Navigation übersprungen werden. Darüber hinaus wird jedes untergeordnete Element nur einmal besucht, und die Navigation führt keine Schleife durch. Das heißt, die Methode schlägt fehl, wenn ein Client versucht, vor dem ersten Objekt oder nach dem letzten Objekt zu navigieren.

Räumliche und logische Navigation sind verknüpft. In einer horizontalen Symbolleiste sollte beispielsweise der Aufruf der -Methode mit [**NAVDIR \_ RIGHT**](navigation-constants.md) die gleichen Ergebnisse wie der Aufruf der -Methode mit [**NAVDIR \_ NEXT**](navigation-constants.md)erzeugen.

Das Startobjekt der Navigation ist entweder das objekt selbst oder eines der untergeordneten Elemente **des Objekts, es sei denn, entweder** [**NAVDIR \_ FIRSTCHILD**](navigation-constants.md) oder [**NAVDIR \_ LASTCHILD**](navigation-constants.md) ist angegeben. In diesem Fall muss die Navigation vom Objekt selbst beginnen.

Wenn ein Client von einem barrierefreien Objekt zu einem nebengeordneten Benutzeroberflächenelement navigiert oder der **lVal-Member** von *varStart* **CHILDID \_ SELF** ist und das angegebene Flag in *navDir* ein beliebiges Navigationsflag mit Ausnahme von [**NAVDIR \_ FIRSTCHILD**](navigation-constants.md) oder [**NAVDIR \_ LASTCHILD**](navigation-constants.md)ist, ist das Ergebnis in *pvarEnd* entweder eine untergeordnete ID oder eine [**IDispatch-Schnittstelle.**](idispatch-interface.md) Wenn *pvarEnd* eine untergeordnete ID enthält, müssen Clients zunächst einen Zeiger auf die [**IAccessible-Schnittstelle**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) des übergeordneten Elements abrufen, um von diesem Benutzeroberflächenelement zu navigieren oder weitere Informationen dazu zu erhalten. Um das übergeordnete Objekt abzurufen, rufen Clients die [**IAccessible::get \_ accParent-Eigenschaft**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) des gleichgeordneten Objekts oder des Startobjekts der Navigation auf.

Beachten Sie, dass Clients über Informationen zu allen unverankerten Objekten verfügen müssen, indem sie die [**EnumChildWindows-Funktion**](/windows/desktop/api/winuser/nf-winuser-enumchildwindows) aufrufen. Da ein unverankerte Objekt nicht auf sein übergeordnetes Objekt abgeschnitten wird, verfügen Clients auf dem Bildschirm nicht über Informationen über die hierarchische Beziehung zwischen zwei Objekten in der Nähe.

Die folgende Grafik ist ein Beispiel für ein unverankerte Objekt, das nicht auf das übergeordnete Objekt abgeschnitten wird.

![Screenshot des geöffneten Fensters über einem größeren Microsoft Developer Studio-Fenster](images/floatob.gif)

## <a name="establishing-the-order-in-logical-navigation"></a>Festlegen der Reihenfolge in der logischen Navigation

In der logischen Navigation richten die Entwickler, die die Objekte entwerfen, die Beziehungen zwischen ihnen ein. Die logische Navigation ist stärker subjektiv als die räumliche Navigation. Außerdem ist die Reihenfolge in der logischen Navigation nicht mit der Reihenfolge identisch, die mit untergeordneten IDs verwendet wird.

Für Objekte mit Bildschirmspeicherorten sollten Serverentwickler die Navigationsreihenfolge so einrichten, wie die meisten Benutzer dies als logisch betrachten würden. In englischsprachigen Ländern/Regionen bedeutet dies beispielsweise eine Reihenfolge von links nach rechts, von oben nach unten.

Die logische Navigationsreihenfolge muss parallele Tastaturnavigationsreihenfolge sein. Beispielsweise enthält ein Dialogfeld die Schaltflächen **OK** und **Abbrechen** und einige Bearbeitungssteuerelemente. Ein Client, der [**IAccessible::accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) aufruft, um zum nächsten oder vorherigen Objekt in diesem Dialogfeld zu navigieren, wechselt in der gleichen Reihenfolge wie ein Benutzer, der DIE TAB-TASTE oder UMSCHALT+TAB drückt, um den Fokus zwischen Elementen zu verschieben.

Für Objekte ohne definierte Bildschirmspeicherorte wird die logische Reihenfolge von Serverentwicklern festgelegt, und Cliententwickler sollten keine Annahmen darüber treffen. Beispielsweise ist es akzeptabel, dass nicht sichtbare Objekte, z. B. Objekte, die nur vorübergehend ausgeblendet sind, mit sichtbaren Objekten durchsetzt werden.

 

 