---
description: Streamattribute
ms.assetid: 83b64ad8-2552-41d1-bc61-20361831020b
title: Streamattribute
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a25de9ae6cf769268b3868d36bac2e293cfd8d60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527824"
---
# <a name="stream-attributes"></a><span data-ttu-id="94e88-103">Streamattribute</span><span class="sxs-lookup"><span data-stu-id="94e88-103">Stream Attributes</span></span>

<span data-ttu-id="94e88-104">Die folgenden Attribute gelten für Mediendaten Ströme.</span><span class="sxs-lookup"><span data-stu-id="94e88-104">The following attributes apply to media streams.</span></span> <span data-ttu-id="94e88-105">Um die Attribute aus einem Medien Beispiel zu erhalten, verwenden Sie die [**imfmediasourceex:: getstreamattributormethode**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) .</span><span class="sxs-lookup"><span data-stu-id="94e88-105">To get the attributes from a media sample, use the [**IMFMediaSourceEx::GetStreamAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) method.</span></span>



| <span data-ttu-id="94e88-106">Attribut</span><span class="sxs-lookup"><span data-stu-id="94e88-106">Attribute</span></span>                                                                                   | <span data-ttu-id="94e88-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="94e88-107">Description</span></span>                                   |
|---------------------------------------------------------------------------------------------|-----------------------------------------------|
| [<span data-ttu-id="94e88-108">MF-Erweiterung " \_ cameraextrinsics"</span><span class="sxs-lookup"><span data-stu-id="94e88-108">MFStreamExtension\_CameraExtrinsics</span></span>](mfstreamextension-cameraextrinsics.md)               | <span data-ttu-id="94e88-109">Die Kamera ist extra insics für den Datenstrom.</span><span class="sxs-lookup"><span data-stu-id="94e88-109">The camera extrinsics for the stream.</span></span>         |
| [<span data-ttu-id="94e88-110">MF-Erweiterung \_ pinholecameraintrinsics</span><span class="sxs-lookup"><span data-stu-id="94e88-110">MFStreamExtension\_PinholeCameraIntrinsics</span></span>](mfstreamextension-pinholecameraintrinsics.md) | <span data-ttu-id="94e88-111">Die systeminternen Funktionen der pinloch Kamera für den Datenstrom.</span><span class="sxs-lookup"><span data-stu-id="94e88-111">The pinhole camera intrinsics for the stream.</span></span> |



 

<span data-ttu-id="94e88-112">Nicht jeder Mediendaten Strom enthält jedes hier aufgeführte Attribut.</span><span class="sxs-lookup"><span data-stu-id="94e88-112">Not every media stream contains every attribute listed here.</span></span> <span data-ttu-id="94e88-113">In einigen Fällen gilt ein Attribut nur für bestimmte Arten von Daten.</span><span class="sxs-lookup"><span data-stu-id="94e88-113">In some cases, an attribute applies only to certain kinds of data.</span></span>

## <a name="related-topics"></a><span data-ttu-id="94e88-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="94e88-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="94e88-115">**IMF Sample**</span><span class="sxs-lookup"><span data-stu-id="94e88-115">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)
</dt> <dt>

[<span data-ttu-id="94e88-116">Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="94e88-116">Media Foundation Attributes</span></span>](media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="94e88-117">Medien Beispiele</span><span class="sxs-lookup"><span data-stu-id="94e88-117">Media Samples</span></span>](media-samples.md)
</dt> </dl>

 

 



