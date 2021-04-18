---
title: Video Eingabeformate
description: Video Eingabeformate
ms.assetid: 0f1ec15d-328e-4c07-bf58-fd4ecb483549
keywords:
- Windows Media-Format-SDK, Videoeingabe Formate
- Advanced Systems Format (ASF), Videoeingabe Formate
- ASF (Advanced Systems Format), Videoeingabe Formate
- Videoeingabe Formate
- Windows Media-Format-SDK, Videoformate
- Advanced Systems Format (ASF), Videoformate
- ASF (Advanced Systems Format), Videoformate
- Videoformate
- Windows Media Video 9-Codec, Video Eingabeformate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c5113ee3cbd9c9235104f858968db20ebc29e3a
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2020
ms.locfileid: "106339052"
---
# <a name="video-input-formats"></a><span data-ttu-id="57615-112">Video Eingabeformate</span><span class="sxs-lookup"><span data-stu-id="57615-112">Video Input Formats</span></span>

<span data-ttu-id="57615-113">Der Writer akzeptiert die folgenden Videoformate als Eingabe, die mit dem Windows Media Video 9-Codec komprimiert werden sollen:</span><span class="sxs-lookup"><span data-stu-id="57615-113">The writer accepts the following video formats as input to be compressed using the Windows Media Video 9 codec:</span></span>

-   <span data-ttu-id="57615-114">wmmediasubtype \_ IYUV</span><span class="sxs-lookup"><span data-stu-id="57615-114">WMMEDIASUBTYPE\_IYUV</span></span>
-   <span data-ttu-id="57615-115">Wmmediasubtype \_ I420</span><span class="sxs-lookup"><span data-stu-id="57615-115">WMMEDIASUBTYPE\_I420</span></span>
-   <span data-ttu-id="57615-116">Wmmediasubtype \_ YV12</span><span class="sxs-lookup"><span data-stu-id="57615-116">WMMEDIASUBTYPE\_YV12</span></span>
-   <span data-ttu-id="57615-117">Wmmediasubtype \_ im YUY2</span><span class="sxs-lookup"><span data-stu-id="57615-117">WMMEDIASUBTYPE\_YUY2</span></span>
-   <span data-ttu-id="57615-118">wmmediasubtype \_ UYVY</span><span class="sxs-lookup"><span data-stu-id="57615-118">WMMEDIASUBTYPE\_UYVY</span></span>
-   <span data-ttu-id="57615-119">wmmediasubtype \_ yvyu</span><span class="sxs-lookup"><span data-stu-id="57615-119">WMMEDIASUBTYPE\_YVYU</span></span>
-   <span data-ttu-id="57615-120">Wmmediasubtype \_ YVU9</span><span class="sxs-lookup"><span data-stu-id="57615-120">WMMEDIASUBTYPE\_YVU9</span></span>
-   <span data-ttu-id="57615-121">Wmmediasubtype \_ RGB32</span><span class="sxs-lookup"><span data-stu-id="57615-121">WMMEDIASUBTYPE\_RGB32</span></span>
-   <span data-ttu-id="57615-122">Wmmediasubtype \_ RGB24</span><span class="sxs-lookup"><span data-stu-id="57615-122">WMMEDIASUBTYPE\_RGB24</span></span>
-   <span data-ttu-id="57615-123">Wmmediasubtype \_ RGB565</span><span class="sxs-lookup"><span data-stu-id="57615-123">WMMEDIASUBTYPE\_RGB565</span></span>
-   <span data-ttu-id="57615-124">Wmmediasubtype \_ RGB555</span><span class="sxs-lookup"><span data-stu-id="57615-124">WMMEDIASUBTYPE\_RGB555</span></span>
-   <span data-ttu-id="57615-125">Wmmediasubtype \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="57615-125">WMMEDIASUBTYPE\_RGB8</span></span>

<span data-ttu-id="57615-126">Sie sollten immer [**iwmwriter:: getinputformatcount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-getinputformatcount) und [**iwmwriter:: getinputformat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputformat) verwenden, um die verfügbaren Eingabeformate aufzulisten und das Eingabemedien-Eigenschaften Objekt für das gewünschte Format zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="57615-126">You should always use [**IWMWriter::GetInputFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-getinputformatcount) and [**IWMWriter::GetInputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputformat) to enumerate the available input formats and to obtain the input media properties object for the desired format.</span></span> <span data-ttu-id="57615-127">Die Eigenschaften der Video Eingabemedien-Eigenschaften müssen so geändert werden, dass Sie die Frame Größe und die Framerate der Eingabemedien widerspiegeln.</span><span class="sxs-lookup"><span data-stu-id="57615-127">Video input media properties objects must be changed to reflect the frame size and frame rate of your input media.</span></span>

## <a name="related-topics"></a><span data-ttu-id="57615-128">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="57615-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="57615-129">**Medientyp-IDs**</span><span class="sxs-lookup"><span data-stu-id="57615-129">**Media Type Identifiers**</span></span>](media-type-identifiers.md)
</dt> <dt>

[<span data-ttu-id="57615-130">**Medientypen**</span><span class="sxs-lookup"><span data-stu-id="57615-130">**Media Types**</span></span>](media-types.md)
</dt> </dl>

 

 




