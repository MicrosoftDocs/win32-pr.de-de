---
description: In diesem Thema werden die SaveAdd-Methoden der Image-Klasse aufgelistet. Eine umfassende Liste der Methoden für die Image-Klasse finden Sie unter Image methods.
ms.assetid: e597f6e6-6e07-4afb-8905-26e4af961685
title: Image. SaveAdd-Methoden (gdiplusheaders. h)
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: a2b65c6fe56507538f092edc7128497de5cb2f00
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979313"
---
# <a name="imagesaveadd-methods"></a><span data-ttu-id="43737-104">Image. SaveAdd-Methoden</span><span class="sxs-lookup"><span data-stu-id="43737-104">Image.SaveAdd methods</span></span>

<span data-ttu-id="43737-105">In diesem Thema werden die SaveAdd-Methoden der [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) -Klasse aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="43737-105">This topic lists the SaveAdd methods of the [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) class.</span></span> <span data-ttu-id="43737-106">Eine umfassende Liste der Methoden für die **Image** -Klasse finden Sie unter [Image Methods](-gdiplus-class-image-methods.md).</span><span class="sxs-lookup"><span data-stu-id="43737-106">For a complete list of methods for the **Image** class, see [Image Methods](-gdiplus-class-image-methods.md).</span></span>

### <a name="overload-list"></a><span data-ttu-id="43737-107">Überladeliste</span><span class="sxs-lookup"><span data-stu-id="43737-107">Overload list</span></span>



| <span data-ttu-id="43737-108">Methode</span><span class="sxs-lookup"><span data-stu-id="43737-108">Method</span></span>                                                                                               | <span data-ttu-id="43737-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="43737-109">Description</span></span>                                                                                                                                                                                                                                                                            |
|:-----------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="43737-110">[**SaveAdd (EncoderParameters \* )**](/previous-versions//ms535408(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="43737-110">[**SaveAdd(EncoderParameters\*)**](/previous-versions//ms535408(v=vs.85))</span></span>                  | <span data-ttu-id="43737-111">Die [**Image:: SaveAdd**](/previous-versions//ms535408(v=vs.85)) -Methode fügt einen Frame zu einer Datei oder einem Stream hinzu, der in einem vorherigen Aufrufder **Save** -Methode angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="43737-111">The [**Image::SaveAdd**](/previous-versions//ms535408(v=vs.85)) method adds a frame to a file or stream specified in a previous call to the **Save** method.</span></span> <span data-ttu-id="43737-112">Mit dieser Methode speichern Sie ausgewählte Rahmen eines Bilds mit mehreren Rahmen in einem anderen Bild mit mehreren Rahmen.</span><span class="sxs-lookup"><span data-stu-id="43737-112">Use this method to save selected frames from a multiple-frame image to another multiple-frame image.</span></span><br/> |
| <span data-ttu-id="43737-113">[**SaveAdd (Image \* , EncoderParameters \* )**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters))</span><span class="sxs-lookup"><span data-stu-id="43737-113">[**SaveAdd(Image\*,EncoderParameters\*)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters))</span></span> | <span data-ttu-id="43737-114">Die [**Image:: SaveAdd**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters)) -Methode fügt einen Frame zu einer Datei oder einem Stream hinzu, der in einem vorherigen Aufrufder **Save** -Methode angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="43737-114">The [**Image::SaveAdd**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters)) method adds a frame to a file or stream specified in a previous call to the **Save** method.</span></span><br/>                                                                                             |



## <a name="requirements"></a><span data-ttu-id="43737-115">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="43737-115">Requirements</span></span>



| <span data-ttu-id="43737-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="43737-116">Requirement</span></span> | <span data-ttu-id="43737-117">Wert</span><span class="sxs-lookup"><span data-stu-id="43737-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="43737-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="43737-118">Minimum supported client</span></span><br/> | <span data-ttu-id="43737-119">Nur Windows XP, Windows 2000 Professional \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="43737-119">Windows XP, Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="43737-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="43737-120">Minimum supported server</span></span><br/> | <span data-ttu-id="43737-121">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="43737-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="43737-122">Produkt</span><span class="sxs-lookup"><span data-stu-id="43737-122">Product</span></span><br/>                  | <span data-ttu-id="43737-123">GDI+ 1,0</span><span class="sxs-lookup"><span data-stu-id="43737-123">GDI+ 1.0</span></span><br/>                                                                                             |
| <span data-ttu-id="43737-124">Header</span><span class="sxs-lookup"><span data-stu-id="43737-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="43737-125"><dt>Gdiplusheaders. h (Include gdiplus. h)</dt></span><span class="sxs-lookup"><span data-stu-id="43737-125"><dt>Gdiplusheaders.h (include Gdiplus.h)</dt></span></span> </dl> |
| <span data-ttu-id="43737-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="43737-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="43737-127"><dt>Gdiplus. lib</dt></span><span class="sxs-lookup"><span data-stu-id="43737-127"><dt>Gdiplus.lib</dt></span></span> </dl>                          |



 

 
