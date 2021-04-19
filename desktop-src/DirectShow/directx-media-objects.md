---
description: DirectX-Medienobjekte
ms.assetid: e4424740-31b9-4317-8791-6a9aebb0c7e6
title: DirectX-Medienobjekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2119fc8cce602bc1cc085886edd6852320aca180
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106367267"
---
# <a name="directx-media-objects"></a><span data-ttu-id="1958a-103">DirectX-Medienobjekte</span><span class="sxs-lookup"><span data-stu-id="1958a-103">DirectX Media Objects</span></span>

> [!Note]  
> <span data-ttu-id="1958a-104">DMOS wurden durch [Media Foundation Transformationen](/windows/desktop/medfound/media-foundation-transforms) (MFTs) abgelöst.</span><span class="sxs-lookup"><span data-stu-id="1958a-104">DMOs have been superseded by [Media Foundation Transforms](/windows/desktop/medfound/media-foundation-transforms) (MFTs).</span></span> <span data-ttu-id="1958a-105">Die DMO-Schnittstellen werden weiterhin unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1958a-105">The DMO interfaces are still supported.</span></span> <span data-ttu-id="1958a-106">Wenn Sie jedoch einen benutzerdefinierten Codec oder ein Plug-in für die Audio-/Videoverarbeitung schreiben, sollten Sie es als MFT implementieren.</span><span class="sxs-lookup"><span data-stu-id="1958a-106">However, if you are writing a custom codec or audio/video processing plug-in, you should consider implementing it as an MFT.</span></span>

 

<span data-ttu-id="1958a-107">Bei DirectX Media Objects (DMOs) handelt es sich um COM-basierte datenstreamingkomponenten.</span><span class="sxs-lookup"><span data-stu-id="1958a-107">DirectX Media Objects (DMOs) are COM-based data-streaming components.</span></span> <span data-ttu-id="1958a-108">In gewisser Hinsicht ähneln DMOS Microsoft DirectShow-filtern.</span><span class="sxs-lookup"><span data-stu-id="1958a-108">In some respects, DMOs are similar to Microsoft DirectShow filters.</span></span> <span data-ttu-id="1958a-109">Wie DirectShow-Filter übernehmen DMOS Eingabedaten und verwenden Sie, um Ausgabedaten zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="1958a-109">Like DirectShow filters, DMOs take input data and use it to produce output data.</span></span> <span data-ttu-id="1958a-110">Die Anwendungs Programmierschnittstellen (Application Programming Interfaces, APIs) für DMOS sind jedoch viel einfacher als die entsprechenden APIs für DirectShow.</span><span class="sxs-lookup"><span data-stu-id="1958a-110">However, the application programming interfaces (APIs) for DMOs are much simpler than the corresponding APIs for DirectShow.</span></span> <span data-ttu-id="1958a-111">Demzufolge sind DMOS einfacher zu erstellen, zu testen und zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="1958a-111">As a result, DMOs are easier to create, test, and use.</span></span> <span data-ttu-id="1958a-112">DMOS können in vielen Szenarien verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="1958a-112">DMOs can be used in many scenarios:</span></span>

-   <span data-ttu-id="1958a-113">Anwendungen, die auf DirectShow basieren, können DMOS über einen DirectShow-Filter verwenden, der als [DMO-Wrapper](dmo-wrapper-filter.md) Filter bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="1958a-113">Applications based on DirectShow can use DMOs through a DirectShow filter called the [DMO Wrapper](dmo-wrapper-filter.md) filter.</span></span> <span data-ttu-id="1958a-114">Der Unterschied zwischen Filtern und DMOS ist für die Anwendung transparent.</span><span class="sxs-lookup"><span data-stu-id="1958a-114">The distinction between filters and DMOs is transparent to the application.</span></span> <span data-ttu-id="1958a-115">Die Anwendung ruft die DMO-APIs nicht direkt auf.</span><span class="sxs-lookup"><span data-stu-id="1958a-115">The application does not directly call the DMO APIs.</span></span>
-   <span data-ttu-id="1958a-116">Anwendungen, die auf Microsoft DirectSound basieren, können Audioeffekt-DMOS verwenden.</span><span class="sxs-lookup"><span data-stu-id="1958a-116">Applications based on Microsoft DirectSound can use audio effect DMOs.</span></span> <span data-ttu-id="1958a-117">Die Anwendung wird erneut von den DMO-APIs auf niedriger Ebene durch die DirectSound-APIs auf höherer Ebene geschützt.</span><span class="sxs-lookup"><span data-stu-id="1958a-117">Again, the application is shielded from the low-level DMO APIs by the higher-level DirectSound APIs.</span></span>
-   <span data-ttu-id="1958a-118">Anwendungen können DMOS direkt verwenden.</span><span class="sxs-lookup"><span data-stu-id="1958a-118">Applications can use DMOs directly.</span></span>

<span data-ttu-id="1958a-119">Wenn Sie also ein DMO schreiben, erstellen Sie eine-Komponente, die in einer Vielzahl von Anwendungen verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="1958a-119">Thus, by writing a DMO, you create a component that can be used in a wide range of applications.</span></span> <span data-ttu-id="1958a-120">Diese Dokumentation enthält die folgenden Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="1958a-120">This documentation contains the following sections:</span></span>

-   [<span data-ttu-id="1958a-121">Informationen zu DMOS</span><span class="sxs-lookup"><span data-stu-id="1958a-121">About DMOs</span></span>](about-dmos.md)
-   [<span data-ttu-id="1958a-122">Verwenden von dmos</span><span class="sxs-lookup"><span data-stu-id="1958a-122">Using DMOs</span></span>](using-dmos.md)
-   [<span data-ttu-id="1958a-123">Schreiben eines DMO</span><span class="sxs-lookup"><span data-stu-id="1958a-123">Writing a DMO</span></span>](writing-a-dmo.md)
-   [<span data-ttu-id="1958a-124">Medien Parameter</span><span class="sxs-lookup"><span data-stu-id="1958a-124">Media Parameters</span></span>](media-parameters.md)
-   [<span data-ttu-id="1958a-125">DMO-Referenz</span><span class="sxs-lookup"><span data-stu-id="1958a-125">DMO Reference</span></span>](dmo-reference.md)

## <a name="related-topics"></a><span data-ttu-id="1958a-126">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1958a-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1958a-127">DirectShow</span><span class="sxs-lookup"><span data-stu-id="1958a-127">DirectShow</span></span>](directshow.md)
</dt> </dl>

 

 
