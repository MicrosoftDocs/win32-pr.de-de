---
title: XPS OM Canvas und visuelle Schnittstellen
description: In diesem Thema wird beschrieben, wie die canvasbezogenen Schnittstellen der XPS-Dokument-API in einem XPS OM verwendet werden.
ms.assetid: 368b8c47-9803-42ee-a3a8-681bf55315ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97f7214a06779d997331f57a22ae29217e5cabdd635d0c3feac85bd8a3070065
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118469269"
---
# <a name="working-with-xps-om-canvas-and-visual-interfaces"></a>Arbeiten mit XPS OM Canvas und visuellen Schnittstellen

In diesem Thema wird beschrieben, wie die canvasbezogenen Schnittstellen der XPS-Dokument-API in einem XPS OM verwendet werden.

| Schnittstellenname                                  | Logische untergeordnete Schnittstellen                                                                                                                    | BESCHREIBUNG                                                                                                                                                                                                             |
|-------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IXpsOMVisual**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual)<br/> | [**IXpsOMCanvas**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas)<br/> [**IXpsOMGlyphs**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs)<br/> [**IXpsOMPath**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath)<br/> | Die Basisklasse der Schnittstellen, die visuelle Objekte definieren, z. B. Text und Grafiken.<br/> Visuelle Objekte können in einer [**IXpsOMVisualCollection-Schnittstelle gesammelt**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualcollection) werden.<br/> |
| [**IXpsOMCanvas**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas)<br/> | [**IXpsOMCanvas**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas)<br/> [**IXpsOMGlyphs**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs)<br/> [**IXpsOMPath**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath)<br/> | Eine Auflistung visueller Objekte, die als einzelnes visuelles Objekt behandelt werden können.<br/>                                                                                                                                |

[**IXpsOMVisual**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual) ist die Basisschnittstelle. Die sichtbaren Objekte einer Seite erben davon. [**IXpsOMCanvas**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas) erbt von [**IXpsOMVisual**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual) und ermöglicht es, viele andere visuelle Elemente zu gruppisieren und als einzelnes visuelles Element zu verwenden. Beispielsweise können Sie eine [**IXpsOMCanvas-Schnittstelle**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas) verwenden, um ein Seitenbanner zu erstellen, das eine Sammlung von Text- und grafischen Elementen enthält. Ein solches Banner kann ein Logo, das Unternehmenslogo und die Unternehmensadresse enthalten. Sie können alle diese Elemente in der [**IXpsOMVisualCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualcollection) einer [**IXpsOMCanvas-Schnittstelle**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas) platzieren und dann eine einzelne Transformation auf das [**IXpsOMCanvas-Objekt**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas) anwenden, um die Größe auf eine bestimmte Seite zu ändern. Dies ist viel einfacher als das Berechnen und Anwenden einer Transformation auf jede einzelne visuelle Komponente im Banner.

Sie können auch einen Zeichenbereich verwenden, um die Größe des Seiteninhalts an die aktuelle Seitengröße zu ändern. Platzieren Sie hierzu alle Inhalte der Seite in einem einzelnen Zeichenbereich, und wenden Sie dann die entsprechende Transformation an, um den Zeichenbereich an die aktuelle Seitengröße zu passen. Dies ist auch viel einfacher, als die Größe jedes visuellen Elements in der Auflistung von Visuals auf der Seite zu ändern.

## <a name="move-page-contents-to-a-canvas"></a>Verschieben von Seiteninhalten in einen Zeichenbereich

Im folgenden Codebeispiel wird der Inhalt einer Seite in einen Zeichenbereich verschiebt.

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
  <dt>[**IXpsOMCanvas-Schnittstelle**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas)</dt>
  <dt>[**IXpsOMVisual Interface**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual)</dt>
  <dt>[**IXpsOMVisualCollection-Schnittstelle**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualcollection)</dt>
</dl>
