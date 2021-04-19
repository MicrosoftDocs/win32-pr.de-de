---
description: In diesem Thema wird beschrieben, wie Sie die Schnittstellen auf Seitenebene verwenden, die den Zugriff auf den Inhalt einer Seite in einem XPS-OM ermöglichen.
ms.assetid: 7127ee28-eca9-4e0e-a27a-9051eb105b27
title: Arbeiten mit XPS-OM-Seiten Schnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8350409f2f436cc4ec2293e735c3f020b49bea68
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373124"
---
# <a name="working-with-xps-om-page-interfaces"></a><span data-ttu-id="cd293-103">Arbeiten mit XPS-OM-Seiten Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="cd293-103">Working with XPS OM Page Interfaces</span></span>

<span data-ttu-id="cd293-104">In diesem Thema wird beschrieben, wie Sie die Schnittstellen auf Seitenebene verwenden, die den Zugriff auf den Inhalt einer Seite in einem XPS-OM ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="cd293-104">This topic describes how to use the page-level interfaces that provide access to the contents of a page in an XPS OM.</span></span>



| <span data-ttu-id="cd293-105">Schnittstellen Name</span><span class="sxs-lookup"><span data-stu-id="cd293-105">Interface name</span></span>                                                                                                                                                                              | <span data-ttu-id="cd293-106">Logische untergeordnete Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="cd293-106">Logical child interfaces</span></span>                                                                                                                                                                                            | <span data-ttu-id="cd293-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cd293-107">Description</span></span>                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cd293-108">**Ixpsompage**</span><span class="sxs-lookup"><span data-stu-id="cd293-108">**IXpsOMPage**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage)<br/>                                                                                                                                                 | [<span data-ttu-id="cd293-109">**Ixpsomcanvas**</span><span class="sxs-lookup"><span data-stu-id="cd293-109">**IXpsOMCanvas**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas)<br/> [<span data-ttu-id="cd293-110">**Ixpsomglyphs**</span><span class="sxs-lookup"><span data-stu-id="cd293-110">**IXpsOMGlyphs**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs)<br/> [<span data-ttu-id="cd293-111">**Ixpsompath**</span><span class="sxs-lookup"><span data-stu-id="cd293-111">**IXpsOMPath**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath)<br/>                                                                         | <span data-ttu-id="cd293-112">Das Stamm Objekt des Seiteninhalts.</span><span class="sxs-lookup"><span data-stu-id="cd293-112">The root object of the page contents.</span></span><br/> <span data-ttu-id="cd293-113">Dieses Objekt stellt einen Dokument Teil dar.</span><span class="sxs-lookup"><span data-stu-id="cd293-113">This object represents a document part.</span></span><br/>                                                |
| [<span data-ttu-id="cd293-114">**Ixpsomshareable**</span><span class="sxs-lookup"><span data-stu-id="cd293-114">**IXpsOMShareable**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomshareable)<br/>                                                                                                                                       | [<span data-ttu-id="cd293-115">**Ixpsomvisual**</span><span class="sxs-lookup"><span data-stu-id="cd293-115">**IXpsOMVisual**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual)<br/> [<span data-ttu-id="cd293-116">**Ixpsommatrixtransform**</span><span class="sxs-lookup"><span data-stu-id="cd293-116">**IXpsOMMatrixTransform**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsommatrixtransform)<br/> [<span data-ttu-id="cd293-117">**Ixpsomgeometry**</span><span class="sxs-lookup"><span data-stu-id="cd293-117">**IXpsOMGeometry**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometry)<br/> [<span data-ttu-id="cd293-118">**Ixpsombrush**</span><span class="sxs-lookup"><span data-stu-id="cd293-118">**IXpsOMBrush**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsombrush)<br/> | <span data-ttu-id="cd293-119">Schnittstellen, die von der [**ixpsomshareable**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomshareable) -Schnittstelle abgeleitet werden, können in einem Ressourcenverzeichnis gespeichert und freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="cd293-119">Interfaces that derive from the [**IXpsOMShareable**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomshareable) interface can be stored in a resource dictionary and shared.</span></span><br/> |
| [<span data-ttu-id="cd293-120">**Ixpsomremotediktattionaryresource**</span><span class="sxs-lookup"><span data-stu-id="cd293-120">**IXpsOMRemoteDictionaryResource**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomremotedictionaryresource)<br/> [<span data-ttu-id="cd293-121">**Ixpsomremotediktattionaryresourcecollection**</span><span class="sxs-lookup"><span data-stu-id="cd293-121">**IXpsOMRemoteDictionaryResourceCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomremotedictionaryresourcecollection)<br/> | [<span data-ttu-id="cd293-122">**Ixpsomdictionary**</span><span class="sxs-lookup"><span data-stu-id="cd293-122">**IXpsOMDictionary**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdictionary)<br/>                                                                                                                                                             | <span data-ttu-id="cd293-123">Enthält ein Ressourcen Wörterbuch.</span><span class="sxs-lookup"><span data-stu-id="cd293-123">Contains a resource dictionary.</span></span><br/>                                                                                                         |
| [<span data-ttu-id="cd293-124">**Ixpsomdictionary**</span><span class="sxs-lookup"><span data-stu-id="cd293-124">**IXpsOMDictionary**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdictionary)<br/>                                                                                                                                     | <span data-ttu-id="cd293-125">Keine</span><span class="sxs-lookup"><span data-stu-id="cd293-125">None</span></span><br/>                                                                                                                                                                                                     | <span data-ttu-id="cd293-126">Verweist auf die Ressourcen, die von anderen Objekten gemeinsam genutzt werden.</span><span class="sxs-lookup"><span data-stu-id="cd293-126">References the resources that are shared by other objects.</span></span><br/>                                                                              |
| [<span data-ttu-id="cd293-127">**Ixpsomstoryfragmentsresource**</span><span class="sxs-lookup"><span data-stu-id="cd293-127">**IXpsOMStoryFragmentsResource**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomstoryfragmentsresource)<br/>                                                                                                             | <span data-ttu-id="cd293-128">Keine</span><span class="sxs-lookup"><span data-stu-id="cd293-128">None</span></span><br/>                                                                                                                                                                                                     | <span data-ttu-id="cd293-129">Bietet Zugriff auf den Inhalt des Ressourcenstreams des StoryFragments-Teils des Dokuments.</span><span class="sxs-lookup"><span data-stu-id="cd293-129">Provides access to the content of the resource stream of the StoryFragments part of the document.</span></span><br/>                                       |



 

## <a name="related-topics"></a><span data-ttu-id="cd293-130">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="cd293-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cd293-131">**Ixpsomdictionary-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="cd293-131">**IXpsOMDictionary Interface**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdictionary)
</dt> <dt>

[<span data-ttu-id="cd293-132">**Ixpsomdocumentstructureresource**</span><span class="sxs-lookup"><span data-stu-id="cd293-132">**IXpsOMDocumentStructureResource**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentstructureresource)
</dt> <dt>

[<span data-ttu-id="cd293-133">**Ixpsompage-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="cd293-133">**IXpsOMPage Interface**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage)
</dt> <dt>

[<span data-ttu-id="cd293-134">**Ixpsomremotediktattionaryresource-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="cd293-134">**IXpsOMRemoteDictionaryResource Interface**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomremotedictionaryresource)
</dt> <dt>

[<span data-ttu-id="cd293-135">**Ixpsomremotediktattionaryresourcecollection-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="cd293-135">**IXpsOMRemoteDictionaryResourceCollection Interface**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomremotedictionaryresourcecollection)
</dt> <dt>

[<span data-ttu-id="cd293-136">**Ixpsomstoryfragmentsresource-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="cd293-136">**IXpsOMStoryFragmentsResource Interface**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomstoryfragmentsresource)
</dt> </dl>

 

 




