---
description: DirectX-Video Beschleunigung 2,0
ms.assetid: acb73b20-89fa-4a48-be4a-846715a239b0
title: DirectX-Video Beschleunigung 2,0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec3ae813d3c81ebcf753dcaa273cc9f9149eaab5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214313"
---
# <a name="directx-video-acceleration-20"></a><span data-ttu-id="b8031-103">DirectX-Video Beschleunigung 2,0</span><span class="sxs-lookup"><span data-stu-id="b8031-103">DirectX Video Acceleration 2.0</span></span>

<span data-ttu-id="b8031-104">Die DirectX-Video Beschleunigung (DXVA) ist eine API und ein entsprechendes DDI für die Verwendung der Hardwarebeschleunigung zum beschleunigen der Video-Codec-Verarbeitung.</span><span class="sxs-lookup"><span data-stu-id="b8031-104">DirectX Video Acceleration (DXVA) is an API and a corresponding DDI for using hardware-acceleration to speed up video codec processing.</span></span> <span data-ttu-id="b8031-105">Software Codecs und Software-Video Prozessoren können mithilfe von DXVA bestimmte CPU-intensive Vorgänge an die GPU auslagern.</span><span class="sxs-lookup"><span data-stu-id="b8031-105">Software codecs and software video processors can use DXVA to offload certain CPU-intensive operations to the GPU.</span></span> <span data-ttu-id="b8031-106">Beispielsweise kann ein Software Decoder die umgekehrte diskrete Kosinus Transformation (IDCT) in die GPU auslagern.</span><span class="sxs-lookup"><span data-stu-id="b8031-106">For example, a software decoder can offload the inverse discrete cosine transform (iDCT) to the GPU.</span></span>

<span data-ttu-id="b8031-107">In diesem Abschnitt werden die folgenden Themen behandelt:</span><span class="sxs-lookup"><span data-stu-id="b8031-107">This section contains the following topics.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="b8031-108">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="b8031-108">In this section</span></span>



| <span data-ttu-id="b8031-109">Thema</span><span class="sxs-lookup"><span data-stu-id="b8031-109">Topic</span></span>                                                                                             | <span data-ttu-id="b8031-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b8031-110">Description</span></span>                                                                                                                                                                                                      |
|---------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b8031-111">Informationen zu DXVA 2,0</span><span class="sxs-lookup"><span data-stu-id="b8031-111">About DXVA 2.0</span></span>](about-dxva-2-0.md)<br/>                                                   | <span data-ttu-id="b8031-112">Übersicht über DXVA 2 und seine Beziehung zu DXVA 1.</span><span class="sxs-lookup"><span data-stu-id="b8031-112">Overview of DXVA 2 and its relation to DXVA 1.</span></span><br/>                                                                                                                                                        |
| [<span data-ttu-id="b8031-113">Direct3D Device Manager</span><span class="sxs-lookup"><span data-stu-id="b8031-113">Direct3D Device Manager</span></span>](direct3d-device-manager.md)<br/>                                 | <span data-ttu-id="b8031-114">Mit dem Microsoft Direct3D-Geräte-Manager können zwei oder mehr Objekte dasselbe Microsoft Direct3D 9-Gerät gemeinsam verwenden.</span><span class="sxs-lookup"><span data-stu-id="b8031-114">The Microsoft Direct3D device manager enables two or more objects to share the same Microsoft Direct3D 9 device.</span></span><br/>                                                                                      |
| [<span data-ttu-id="b8031-115">Unterstützung von DXVA 2,0 in DirectShow</span><span class="sxs-lookup"><span data-stu-id="b8031-115">Supporting DXVA 2.0 in DirectShow</span></span>](supporting-dxva-2-0-in-directshow.md)<br/>             | <span data-ttu-id="b8031-116">In diesem Thema wird beschrieben, wie DirectX Video Acceleration (DXVA) 2,0 in einem DirectShow-Decoderfilter unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="b8031-116">This topic describes how to support DirectX Video Acceleration (DXVA) 2.0 in a DirectShow decoder filter.</span></span><br/>                                                                                             |
| [<span data-ttu-id="b8031-117">Unterstützung von DXVA 2,0 in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b8031-117">Supporting DXVA 2.0 in Media Foundation</span></span>](supporting-dxva-2-0-in-media-foundation.md)<br/> | <span data-ttu-id="b8031-118">In diesem Thema wird beschrieben, wie die DirectX-Video Beschleunigung (DXVA) 2,0 in einer Media Foundation Transformation (MFT) mit Direct3D 9 unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="b8031-118">This topic describes how to support DirectX Video Acceleration (DXVA) 2.0 in a Media Foundation transform (MFT) using Direct3D 9</span></span><br/>                                                                      |
| [<span data-ttu-id="b8031-119">DXVA-Video Verarbeitung</span><span class="sxs-lookup"><span data-stu-id="b8031-119">DXVA Video Processing</span></span>](dxva-video-processing.md)<br/>                                     | <span data-ttu-id="b8031-120">Die DXVA-Videoverarbeitung kapselt die Funktionen der Grafikhardware, die für die Verarbeitung von nicht komprimierten Videobildern verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b8031-120">DXVA video processing encapsulates the functions of the graphics hardware that are devoted to processing uncompressed video images.</span></span> <span data-ttu-id="b8031-121">Die Video Verarbeitungsdienste umfassen Deinterlacing und Video Mischung.</span><span class="sxs-lookup"><span data-stu-id="b8031-121">Video processing services include deinterlacing and video mixing.</span></span><br/> |
| [<span data-ttu-id="b8031-122">DXVA-HD</span><span class="sxs-lookup"><span data-stu-id="b8031-122">DXVA-HD</span></span>](dxva-hd.md)<br/>                                                                 | <span data-ttu-id="b8031-123">Microsoft DirectX Video Acceleration High Definition (DXVA-HD) ist eine API für die hardwarebeschleunigte Video Verarbeitung.</span><span class="sxs-lookup"><span data-stu-id="b8031-123">Microsoft DirectX Video Acceleration High Definition (DXVA-HD) is an API for hardware-accelerated video processing.</span></span> <br/>                                                                                  |



 

## <a name="related-topics"></a><span data-ttu-id="b8031-124">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b8031-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b8031-125">Media Foundation-Programmier Handbuch</span><span class="sxs-lookup"><span data-stu-id="b8031-125">Media Foundation Programming Guide</span></span>](media-foundation-programming-guide.md)
</dt> <dt>

[<span data-ttu-id="b8031-126">DXVA 1-Spezifikation</span><span class="sxs-lookup"><span data-stu-id="b8031-126">DXVA 1 Specification</span></span>](/windows-hardware/drivers/display/directx-video-acceleration)
</dt> </dl>

 

 
