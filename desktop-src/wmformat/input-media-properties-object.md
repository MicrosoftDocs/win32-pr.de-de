---
title: Eigenschaften Objekt für Eingabemedien
description: Eigenschaften Objekt für Eingabemedien
ms.assetid: e7aa6c99-b6b3-4e5b-869d-3387f70dad87
keywords:
- Windows Media-Format-SDK, Eingabemedien Eigenschaften Objekte
- Advanced Systems Format (ASF), Eingabemedien Eigenschaften Objekte
- ASF (Advanced Systems Format), Eingabemedien Eigenschaften Objekte
- Objekte, Eigenschaften von Eingabemedien Eigenschaften
- Eigenschaften der Eingabemedien Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: beddda23ab7be86c3cb522edb8e811978c0c9ed9
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "103857995"
---
# <a name="input-media-properties-object"></a><span data-ttu-id="4393f-108">Eigenschaften Objekt für Eingabemedien</span><span class="sxs-lookup"><span data-stu-id="4393f-108">Input Media Properties Object</span></span>

<span data-ttu-id="4393f-109">Ein vom Writer-Objekt erstelltes Eigenschaften Objekt für Eingabemedien unterstützt die folgenden Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="4393f-109">An input media properties object created by the writer object supports the following interfaces.</span></span> <span data-ttu-id="4393f-110">Auf diese Schnittstellen wird durch Aufrufen von **QueryInterface** für eine der Schnittstellen des Writer-Objekts zugegriffen.</span><span class="sxs-lookup"><span data-stu-id="4393f-110">These interfaces are accessed by a call to **QueryInterface** on one of the interfaces of the writer object.</span></span>



| <span data-ttu-id="4393f-111">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="4393f-111">Interface</span></span>                                        | <span data-ttu-id="4393f-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4393f-112">Description</span></span>                                                                                                |
|--------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4393f-113">**Iwminputmedia-Eigenschaften**</span><span class="sxs-lookup"><span data-stu-id="4393f-113">**IWMInputMediaProps**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops) | <span data-ttu-id="4393f-114">Ruft die Eigenschaften eines Eingabestreams ab.</span><span class="sxs-lookup"><span data-stu-id="4393f-114">Retrieves the properties of an input stream.</span></span>                                                               |
| [<span data-ttu-id="4393f-115">**Iwmmedia-Eigenschaften**</span><span class="sxs-lookup"><span data-stu-id="4393f-115">**IWMMediaProps**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops)           | <span data-ttu-id="4393f-116">Wird als Basisschnittstelle für die anderen Schnittstellen der Medien Eigenschaft verwendet (Eingabe, Ausgabe und Video).</span><span class="sxs-lookup"><span data-stu-id="4393f-116">Used as the base interface for the other media-property interfaces (input, output, and video).</span></span>             |
| [<span data-ttu-id="4393f-117">**Iwmvideomedia-Eigenschaften**</span><span class="sxs-lookup"><span data-stu-id="4393f-117">**IWMVideoMediaProps**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nn-wmsdkidl-iwmvideomediaprops) | <span data-ttu-id="4393f-118">Verwaltet die Eigenschaften eines Videostreams.</span><span class="sxs-lookup"><span data-stu-id="4393f-118">Manages the properties of a video stream.</span></span> <span data-ttu-id="4393f-119">Dies ist eine optionale Schnittstelle, die nur für Videostreams verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="4393f-119">This is an optional interface, available only for video streams.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="4393f-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4393f-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4393f-121">**Objekte**</span><span class="sxs-lookup"><span data-stu-id="4393f-121">**Objects**</span></span>](objects.md)
</dt> <dt>

[<span data-ttu-id="4393f-122">**Writer-Objekt**</span><span class="sxs-lookup"><span data-stu-id="4393f-122">**Writer Object**</span></span>](writer-object.md)
</dt> </dl>

 

 




