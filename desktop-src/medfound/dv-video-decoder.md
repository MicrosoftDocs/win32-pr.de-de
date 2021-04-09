---
description: Der Media Foundation DV-Video Decoder ist eine Media Foundation Transformation, die das DV-Video decodiert.
ms.assetid: 97e5ba52-92fc-49e4-9c22-6f61bfda2003
title: DV-Video Decoder
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed277c3e4dd1aaa031d4dcf4694c7c3051fe37ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749257"
---
# <a name="dv-video-decoder"></a><span data-ttu-id="bcb9d-103">DV-Video Decoder</span><span class="sxs-lookup"><span data-stu-id="bcb9d-103">DV Video Decoder</span></span>

<span data-ttu-id="bcb9d-104">Der Media Foundation DV-Video Decoder ist eine [Media Foundation Transformation](media-foundation-transforms.md) , die das DV-Video decodiert.</span><span class="sxs-lookup"><span data-stu-id="bcb9d-104">The Media Foundation DV video decoder is a [Media Foundation Transform](media-foundation-transforms.md) that decodes DV video.</span></span>

<span data-ttu-id="bcb9d-105">Der DV-Video Decoder unterstützt die folgenden Eingabetypen:</span><span class="sxs-lookup"><span data-stu-id="bcb9d-105">The DV video decoder supports the following input types:</span></span>



| <span data-ttu-id="bcb9d-106">Subtype</span><span class="sxs-lookup"><span data-stu-id="bcb9d-106">Subtype</span></span>                 | <span data-ttu-id="bcb9d-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bcb9d-107">Description</span></span>                  |
|-------------------------|------------------------------|
| <span data-ttu-id="bcb9d-108">**MF-Format ( \_ DVC)**</span><span class="sxs-lookup"><span data-stu-id="bcb9d-108">**MFVideoFormat\_DVC**</span></span>  | <span data-ttu-id="bcb9d-109">DVC/DV-Video</span><span class="sxs-lookup"><span data-stu-id="bcb9d-109">DVC/DV Video</span></span>                 |
| <span data-ttu-id="bcb9d-110">**MF-Format ( \_ dvhd)**</span><span class="sxs-lookup"><span data-stu-id="bcb9d-110">**MFVideoFormat\_DVHD**</span></span> | <span data-ttu-id="bcb9d-111">HD-dvcr (1125-60 oder 1250-50)</span><span class="sxs-lookup"><span data-stu-id="bcb9d-111">HD-DVCR (1125-60 or 1250-50)</span></span> |
| <span data-ttu-id="bcb9d-112">**MF-Format ( \_ DVSD)**</span><span class="sxs-lookup"><span data-stu-id="bcb9d-112">**MFVideoFormat\_DVSD**</span></span> | <span data-ttu-id="bcb9d-113">SDL-dvcr (525-60 oder 625-50)</span><span class="sxs-lookup"><span data-stu-id="bcb9d-113">SDL-DVCR (525-60 or 625-50)</span></span>  |
| <span data-ttu-id="bcb9d-114">**MF-Format \_ dvsl**</span><span class="sxs-lookup"><span data-stu-id="bcb9d-114">**MFVideoFormat\_DVSL**</span></span> | <span data-ttu-id="bcb9d-115">SD-dvcr (525-60 oder 625-50)</span><span class="sxs-lookup"><span data-stu-id="bcb9d-115">SD-DVCR (525-60 or 625-50)</span></span>   |



 

<span data-ttu-id="bcb9d-116">Es unterstützt einen einzelnen Ausgabetyp:</span><span class="sxs-lookup"><span data-stu-id="bcb9d-116">It supports a single output type:</span></span>



| <span data-ttu-id="bcb9d-117">Subtype</span><span class="sxs-lookup"><span data-stu-id="bcb9d-117">Subtype</span></span>             | <span data-ttu-id="bcb9d-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bcb9d-118">Description</span></span> |
|---------------------|-------------|
| <span data-ttu-id="bcb9d-119">MF-Format \_ im YUY2</span><span class="sxs-lookup"><span data-stu-id="bcb9d-119">MFVideoFormat\_YUY2</span></span> | <span data-ttu-id="bcb9d-120">Im YUY2-Video</span><span class="sxs-lookup"><span data-stu-id="bcb9d-120">YUY2 video</span></span>  |



 

## <a name="requirements"></a><span data-ttu-id="bcb9d-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bcb9d-121">Requirements</span></span>



| <span data-ttu-id="bcb9d-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bcb9d-122">Requirement</span></span> | <span data-ttu-id="bcb9d-123">Wert</span><span class="sxs-lookup"><span data-stu-id="bcb9d-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bcb9d-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bcb9d-124">Minimum supported client</span></span><br/> | <span data-ttu-id="bcb9d-125">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bcb9d-125">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="bcb9d-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bcb9d-126">Minimum supported server</span></span><br/> | <span data-ttu-id="bcb9d-127">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bcb9d-127">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="bcb9d-128">DLL</span><span class="sxs-lookup"><span data-stu-id="bcb9d-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bcb9d-129"><dt>Mfdvdec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bcb9d-129"><dt>Mfdvdec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bcb9d-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bcb9d-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bcb9d-131">Codec-Objekte</span><span class="sxs-lookup"><span data-stu-id="bcb9d-131">Codec Objects</span></span>](codecobjects.md)
</dt> <dt>

[<span data-ttu-id="bcb9d-132">Unterstützte Medienformate in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="bcb9d-132">Supported Media Formats in Media Foundation</span></span>](supported-media-formats-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="bcb9d-133">Video Medientypen</span><span class="sxs-lookup"><span data-stu-id="bcb9d-133">Video Media Types</span></span>](video-media-types.md)
</dt> </dl>

 

 




