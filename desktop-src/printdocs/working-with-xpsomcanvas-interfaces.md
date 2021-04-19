---
title: XPS-OM-Canvas und visuelle Schnittstellen
description: In diesem Thema wird beschrieben, wie die Canvas-bezogenen Schnittstellen der XPS-Dokument-API in einem XPS-OM verwendet werden.
ms.assetid: 368b8c47-9803-42ee-a3a8-681bf55315ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93a3acc8fbc85298e21d039898d4ae7d38fbb272
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314753"
---
# <a name="working-with-xps-om-canvas-and-visual-interfaces"></a>Arbeiten mit XPS OM-Canvas und visuellen Schnittstellen

In diesem Thema wird beschrieben, wie die Canvas-bezogenen Schnittstellen der XPS-Dokument-API in einem XPS-OM verwendet werden.

| Schnittstellen Name                                  | Logische untergeordnete Schnittstellen                                                                                                                    | Beschreibung                                                                                                                                                                                                             |
|-------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Ixpsomvisual**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual)<br/> | [**Ixpsomcanvas**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas)<br/> [**Ixpsomglyphs**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs)<br/> [**Ixpsompath**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath)<br/> | Die Basisklasse der Schnittstellen, die visuelle Objekte definieren, z. b. Text und Grafiken.<br/> Visuelle Objekte können in einer [**ixpsomvisualcollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualcollection) -Schnittstelle gesammelt werden.<br/> |
| [**Ixpsomcanvas**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas)<br/> | [**Ixpsomcanvas**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas)<br/> [**Ixpsomglyphs**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs)<br/> [**Ixpsompath**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath)<br/> | Eine Auflistung von visuellen Objekten, die als einzelnes visuelles Objekt behandelt werden kann.<br/>                                                                                                                                |

[**Ixpsomvisual**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual) ist die Basisschnittstelle. die sichtbaren Objekte einer Seite erben von ihr. [**Ixpsomcanvas**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas) erbt von [**ixpsomvisual**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual) und ermöglicht, dass viele andere visuelle Elemente gruppiert und als einzelnes visuelles Element bearbeitet werden können. Beispielsweise können Sie eine [**ixpsomcanvas**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas) -Schnittstelle verwenden, um ein Seitenbanner zu erstellen, das eine Sammlung von Text-und grafischen Elementen enthält. Ein solches Banner kann ein Logo, den Unternehmens Slogan und die Unternehmens Adresse enthalten. Sie können alle diese Elemente in der [**ixpsomvisualcollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualcollection) einer [**ixpsomcanvas**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas) -Schnittstelle platzieren und dann eine einzelne Transformation auf das [**ixpsomcanvas**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas) -Objekt anwenden, um die Größe zu einer bestimmten Seite zu ändern. Dies ist viel einfacher als das berechnen und Anwenden einer Transformation auf jede einzelne visuelle Komponente im Banner.

Sie können auch einen Zeichenbereich verwenden, um die Größe des Seiteninhalts an die aktuelle Seitengröße anzupassen. Um dies zu erreichen, platzieren Sie den gesamten Inhalt der Seite in einem einzelnen Canvas, und wenden Sie dann die entsprechende Transformation an, um den Zeichenbereich an die aktuelle Seitengröße anzupassen. Dies ist auch viel einfacher als das Ändern der Größe jedes visuellen Elements in der Auflistung der visuellen Elemente auf der Seite.

## <a name="move-page-contents-to-a-canvas"></a>Verschieben von Seiten Inhalten in eine Canvas

Im folgenden Codebeispiel wird der Inhalt einer Seite in eine Canvas verschoben.

```C++
    HRESULT                   hr = S_OK;

    IXpsOMVisualCollection    *pageVisuals;
    IXpsOMVisualCollection    *canvasVisuals;
    IXpsOMVisual              *oneVisual;
    IXpsOMCanvas              *newPageCanvas;

    UINT32 numVisuals = 0;
    UINT32 thisVisual;

    // get the page's visual collection
    // and how many objects it contains
    hr = page->GetVisuals( &pageVisuals );
    hr = pageVisuals->GetCount ( &numVisuals );

    // create the new canvas object and
    // its (empty) visual collection
    hr = xpsFactory->CreateCanvas ( &newPageCanvas );
    hr = newPageCanvas->GetVisuals ( &canvasVisuals );

    // go through the page's list of visual objects,
    //  move each one from the page's list to the canvas' list
    //  release the local pointer
    //  remove it from the page's collection
    thisVisual = 0;
    while (thisVisual < numVisuals) {
        hr = pageVisuals->GetAt (0, &oneVisual);
        hr = canvasVisuals->Append (oneVisual);
        hr = pageVisuals->RemoveAt (0);
        thisVisual++;
    }
    // the page's visual collection should be empty
    hr = pageVisuals->GetCount (&numVisuals);
    _ASSERT (0 == numVisuals);

    // add the new canvas to the page's visual collection
    pageVisuals->Append ( newPageCanvas );

```

## <a name="related-topics"></a>Zugehörige Themen

<dl> 
  <dt>[**Ixpsomcanvas-Schnitt**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas)</dt>Stelle
  <dt>[**ixpsomvisual Interface**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual)</dt>
  <dt>[**ixpsomvisualcollection-Schnittstelle**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualcollection)</dt>
</dl>
