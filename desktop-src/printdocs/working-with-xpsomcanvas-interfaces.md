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
# <a name="working-with-xps-om-canvas-and-visual-interfaces"></a><span data-ttu-id="ae07d-103">Arbeiten mit XPS OM-Canvas und visuellen Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="ae07d-103">Working with XPS OM Canvas and Visual Interfaces</span></span>

<span data-ttu-id="ae07d-104">In diesem Thema wird beschrieben, wie die Canvas-bezogenen Schnittstellen der XPS-Dokument-API in einem XPS-OM verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ae07d-104">This topic describes how to use the canvas-related interfaces of the XPS Document API in an XPS OM.</span></span>

| <span data-ttu-id="ae07d-105">Schnittstellen Name</span><span class="sxs-lookup"><span data-stu-id="ae07d-105">Interface name</span></span>                                  | <span data-ttu-id="ae07d-106">Logische untergeordnete Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="ae07d-106">Logical child interfaces</span></span>                                                                                                                    | <span data-ttu-id="ae07d-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ae07d-107">Description</span></span>                                                                                                                                                                                                             |
|-------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ae07d-108">**Ixpsomvisual**</span><span class="sxs-lookup"><span data-stu-id="ae07d-108">**IXpsOMVisual**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual)<br/> | [<span data-ttu-id="ae07d-109">**Ixpsomcanvas**</span><span class="sxs-lookup"><span data-stu-id="ae07d-109">**IXpsOMCanvas**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas)<br/> [<span data-ttu-id="ae07d-110">**Ixpsomglyphs**</span><span class="sxs-lookup"><span data-stu-id="ae07d-110">**IXpsOMGlyphs**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs)<br/> [<span data-ttu-id="ae07d-111">**Ixpsompath**</span><span class="sxs-lookup"><span data-stu-id="ae07d-111">**IXpsOMPath**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath)<br/> | <span data-ttu-id="ae07d-112">Die Basisklasse der Schnittstellen, die visuelle Objekte definieren, z. b. Text und Grafiken.</span><span class="sxs-lookup"><span data-stu-id="ae07d-112">The base class of the interfaces that define visual objects, such as text and graphics.</span></span><br/> <span data-ttu-id="ae07d-113">Visuelle Objekte können in einer [**ixpsomvisualcollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualcollection) -Schnittstelle gesammelt werden.</span><span class="sxs-lookup"><span data-stu-id="ae07d-113">Visual objects can be collected in an [**IXpsOMVisualCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualcollection) interface.</span></span><br/> |
| [<span data-ttu-id="ae07d-114">**Ixpsomcanvas**</span><span class="sxs-lookup"><span data-stu-id="ae07d-114">**IXpsOMCanvas**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas)<br/> | [<span data-ttu-id="ae07d-115">**Ixpsomcanvas**</span><span class="sxs-lookup"><span data-stu-id="ae07d-115">**IXpsOMCanvas**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas)<br/> [<span data-ttu-id="ae07d-116">**Ixpsomglyphs**</span><span class="sxs-lookup"><span data-stu-id="ae07d-116">**IXpsOMGlyphs**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs)<br/> [<span data-ttu-id="ae07d-117">**Ixpsompath**</span><span class="sxs-lookup"><span data-stu-id="ae07d-117">**IXpsOMPath**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath)<br/> | <span data-ttu-id="ae07d-118">Eine Auflistung von visuellen Objekten, die als einzelnes visuelles Objekt behandelt werden kann.</span><span class="sxs-lookup"><span data-stu-id="ae07d-118">A collection of visual objects that can be treated as a single visual object.</span></span><br/>                                                                                                                                |

<span data-ttu-id="ae07d-119">[**Ixpsomvisual**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual) ist die Basisschnittstelle. die sichtbaren Objekte einer Seite erben von ihr.</span><span class="sxs-lookup"><span data-stu-id="ae07d-119">[**IXpsOMVisual**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual) is the base interface; the visible objects of a page inherit from it.</span></span> <span data-ttu-id="ae07d-120">[**Ixpsomcanvas**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas) erbt von [**ixpsomvisual**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual) und ermöglicht, dass viele andere visuelle Elemente gruppiert und als einzelnes visuelles Element bearbeitet werden können.</span><span class="sxs-lookup"><span data-stu-id="ae07d-120">[**IXpsOMCanvas**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas) inherits from [**IXpsOMVisual**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual) and enables many other visual elements to be grouped and acted upon as a single visual element.</span></span> <span data-ttu-id="ae07d-121">Beispielsweise können Sie eine [**ixpsomcanvas**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas) -Schnittstelle verwenden, um ein Seitenbanner zu erstellen, das eine Sammlung von Text-und grafischen Elementen enthält.</span><span class="sxs-lookup"><span data-stu-id="ae07d-121">For example, you could use an [**IXpsOMCanvas**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas) interface to create a page banner that contains a collection of text and graphical elements.</span></span> <span data-ttu-id="ae07d-122">Ein solches Banner kann ein Logo, den Unternehmens Slogan und die Unternehmens Adresse enthalten.</span><span class="sxs-lookup"><span data-stu-id="ae07d-122">Such a banner might contain a logo, the company slogan, and the company address.</span></span> <span data-ttu-id="ae07d-123">Sie können alle diese Elemente in der [**ixpsomvisualcollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualcollection) einer [**ixpsomcanvas**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas) -Schnittstelle platzieren und dann eine einzelne Transformation auf das [**ixpsomcanvas**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas) -Objekt anwenden, um die Größe zu einer bestimmten Seite zu ändern.</span><span class="sxs-lookup"><span data-stu-id="ae07d-123">You could place all these elements into the [**IXpsOMVisualCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualcollection) of an [**IXpsOMCanvas**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas) interface, and then apply a single transform to the [**IXpsOMCanvas**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas) object to resize it to a particular page.</span></span> <span data-ttu-id="ae07d-124">Dies ist viel einfacher als das berechnen und Anwenden einer Transformation auf jede einzelne visuelle Komponente im Banner.</span><span class="sxs-lookup"><span data-stu-id="ae07d-124">This is much simpler than computing and applying a transform to each individual visual component in the banner.</span></span>

<span data-ttu-id="ae07d-125">Sie können auch einen Zeichenbereich verwenden, um die Größe des Seiteninhalts an die aktuelle Seitengröße anzupassen.</span><span class="sxs-lookup"><span data-stu-id="ae07d-125">You can also use a canvas to resize the page contents to fit the current page size.</span></span> <span data-ttu-id="ae07d-126">Um dies zu erreichen, platzieren Sie den gesamten Inhalt der Seite in einem einzelnen Canvas, und wenden Sie dann die entsprechende Transformation an, um den Zeichenbereich an die aktuelle Seitengröße anzupassen.</span><span class="sxs-lookup"><span data-stu-id="ae07d-126">To accomplish this, place all contents of the page into a single canvas, then apply the appropriate transform to fit the canvas to the current page size.</span></span> <span data-ttu-id="ae07d-127">Dies ist auch viel einfacher als das Ändern der Größe jedes visuellen Elements in der Auflistung der visuellen Elemente auf der Seite.</span><span class="sxs-lookup"><span data-stu-id="ae07d-127">This is also much simpler than trying to resize each visual element in the collection of visuals in the page.</span></span>

## <a name="move-page-contents-to-a-canvas"></a><span data-ttu-id="ae07d-128">Verschieben von Seiten Inhalten in eine Canvas</span><span class="sxs-lookup"><span data-stu-id="ae07d-128">Move page contents to a canvas</span></span>

<span data-ttu-id="ae07d-129">Im folgenden Codebeispiel wird der Inhalt einer Seite in eine Canvas verschoben.</span><span class="sxs-lookup"><span data-stu-id="ae07d-129">The following code example moves the contents of a page to a canvas.</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="ae07d-130">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ae07d-130">Related topics</span></span>

<dl> 
  <span data-ttu-id="ae07d-131"><dt>[**Ixpsomcanvas-Schnitt**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas)</dt>Stelle
  <dt>[**ixpsomvisual Interface**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual)</dt>
  <dt>[**ixpsomvisualcollection-Schnittstelle**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualcollection)</dt>
</span><span class="sxs-lookup"><span data-stu-id="ae07d-131"><dt>[**IXpsOMCanvas Interface**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas)</dt>
  <dt>[**IXpsOMVisual Interface**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual)</dt>
  <dt>[**IXpsOMVisualCollection Interface**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualcollection)</dt>
</span></span></dl>
