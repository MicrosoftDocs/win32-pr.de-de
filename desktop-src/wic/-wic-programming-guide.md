---
title: WIC-Programmier Handbuch
description: Beschreibt die Verwendung der WIC-APIs.
ms.assetid: ed7987f0-5983-4bb5-8640-0830a87c8f2e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bb6675ef7f5c065d2d3e00ab470cb334af25525
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104393678"
---
# <a name="wic-programming-guide"></a><span data-ttu-id="3524c-103">WIC-Programmier Handbuch</span><span class="sxs-lookup"><span data-stu-id="3524c-103">WIC programming guide</span></span>

<span data-ttu-id="3524c-104">Dieser Abschnitt enthält konzeptionelle Themen, in denen die Verwendung der WIC-APIs (Windows Imaging Component) beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="3524c-104">This section contains conceptual topics that describe how to use the Windows Imaging Component (WIC) APIs.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="3524c-105">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="3524c-105">In this section</span></span>



| <span data-ttu-id="3524c-106">Thema</span><span class="sxs-lookup"><span data-stu-id="3524c-106">Topic</span></span>                                                                                 | <span data-ttu-id="3524c-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3524c-107">Description</span></span>                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3524c-108">Übersicht über die Windows Imaging-Komponente</span><span class="sxs-lookup"><span data-stu-id="3524c-108">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)<br/> | <span data-ttu-id="3524c-109">Der WIC bietet ein erweiterbares Framework zum Arbeiten mit Bildern und Bild Metadaten.</span><span class="sxs-lookup"><span data-stu-id="3524c-109">The WIC provides an extensible framework for working with images and image metadata.</span></span><br/>                                                                                                                       |
| [<span data-ttu-id="3524c-110">WIC-API-Übersicht</span><span class="sxs-lookup"><span data-stu-id="3524c-110">WIC API Overview</span></span>](-wic-api.md)<br/>                                           | <span data-ttu-id="3524c-111">Der WIC stellt eine Component Object Model (com)-basierte API für die Verwendung in C und C++ bereit.</span><span class="sxs-lookup"><span data-stu-id="3524c-111">The WIC provides a Component Object Model (COM) based API for use in C and C++.</span></span><br/>                                                                                                                            |
| [<span data-ttu-id="3524c-112">Decodieren digitaler Images</span><span class="sxs-lookup"><span data-stu-id="3524c-112">Decoding Digital Images</span></span>](-wic-decoder-portal.md)<br/>                         | <span data-ttu-id="3524c-113">Dieser Abschnitt enthält konzeptionelle und Vorgehensweisen, in denen WIC-BitmapDecoder beschrieben werden, die beim Decodieren digitaler Images verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3524c-113">This section contains conceptual and how-to topics that describe WIC bitmap decoders which are used in decoding digital images.</span></span><br/>                                                                            |
| [<span data-ttu-id="3524c-114">Verwenden von Bilddaten</span><span class="sxs-lookup"><span data-stu-id="3524c-114">Using Image Data</span></span>](-wic-bitmapsources-portal.md)<br/>                          | <span data-ttu-id="3524c-115">Dieser Abschnitt enthält konzeptionelle und Vorgehensweisen zum Beschreiben von WIC-bitmapquellen und deren Bearbeitung.</span><span class="sxs-lookup"><span data-stu-id="3524c-115">This section contains conceptual and how-to topics that describe WIC bitmap sources and how to manipulate them.</span></span><br/>                                                                                            |
| [<span data-ttu-id="3524c-116">Codieren von Bilddaten</span><span class="sxs-lookup"><span data-stu-id="3524c-116">Encoding Image Data</span></span>](encoding-bitmaps-to-digital-images.md)<br/>              | <span data-ttu-id="3524c-117">Dieser Abschnitt enthält konzeptionelle und Vorgehensweisen, in denen WIC-Bitmap-Encoder beschrieben werden, die zum Codieren digitaler Images verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3524c-117">This section contains conceptual and how-to topics that describe WIC bitmap encoders which are used to encode digital images.</span></span><br/>                                                                              |
| [<span data-ttu-id="3524c-118">Native WIC-Codecs</span><span class="sxs-lookup"><span data-stu-id="3524c-118">Native WIC Codecs</span></span>](native-wic-codecs.md)<br/>                                 | <span data-ttu-id="3524c-119">Dieser Abschnitt enthält Informationen zu den systemeigenen, in WIC verfügbaren Codecs für die Bildverarbeitung.</span><span class="sxs-lookup"><span data-stu-id="3524c-119">This section contains information about the native imaging codecs available in WIC.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="3524c-120">Verarbeiten von Bild Metadaten</span><span class="sxs-lookup"><span data-stu-id="3524c-120">Processing Image Metadata</span></span>](-wic-metadata-portal.md)<br/>                      | <span data-ttu-id="3524c-121">Dieser Abschnitt enthält konzeptionelle Themen, in denen das WIC-Metadatensystem beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="3524c-121">This section contains conceptual topics that describe the WIC metadata system.</span></span><br/>                                                                                                                             |
| [<span data-ttu-id="3524c-122">JPEG YCbCr-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="3524c-122">JPEG YCbCr Support</span></span>](jpeg-ycbcr-support.md)<br/>                               | <span data-ttu-id="3524c-123">Ab Windows 8.1 unterstützt der JPEG-Codec der [Windows Imaging Component (WIC)](-wic-about-windows-imaging-codec.md) das Lesen und Schreiben von Bilddaten in der nativen Yc<sub>b</sub>c<sub>r</sub> -Form.</span><span class="sxs-lookup"><span data-stu-id="3524c-123">Starting with Windows 8.1, the [Windows Imaging Component (WIC)](-wic-about-windows-imaging-codec.md) JPEG codec supports reading and writing image data in its native YC<sub>b</sub>C<sub>r</sub> form.</span></span> <br/> |
| [<span data-ttu-id="3524c-124">Farbverwaltung</span><span class="sxs-lookup"><span data-stu-id="3524c-124">Color Management</span></span>](-wic-colormanagement.md)<br/>                               | <span data-ttu-id="3524c-125">WIC vereinfacht die Farbverwaltung durch die Bereitstellung der [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) -Schnittstelle und der [**iwiccolortransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="3524c-125">WIC simplifies color management by providing the [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) interface and the [**IWICColorTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform) interface.</span></span><br/>          |
| [<span data-ttu-id="3524c-126">Komponentenentwicklung</span><span class="sxs-lookup"><span data-stu-id="3524c-126">Component Development</span></span>](-wic-component-development.md)<br/>                    | <span data-ttu-id="3524c-127">Die WIC ist eine erweiterbare Plattform, die eine Low-Level-API für digitale Images bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="3524c-127">The WIC is an extensible platform that provides low-level API for digital images.</span></span><br/>                                                                                                                          |



 

## <a name="see-also"></a><span data-ttu-id="3524c-128">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="3524c-128">See Also</span></span>

[<span data-ttu-id="3524c-129">WIC-Referenz</span><span class="sxs-lookup"><span data-stu-id="3524c-129">WIC Reference</span></span>](-wic-codec-reference.md)


[<span data-ttu-id="3524c-130">WIC-Beispiele</span><span class="sxs-lookup"><span data-stu-id="3524c-130">WIC Samples</span></span>](-wic-samples.md)


 

 




