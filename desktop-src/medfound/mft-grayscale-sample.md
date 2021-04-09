---
description: Zeigt, wie ein Videoeffekt als Media Foundation Transformation (MFT) implementiert wird.
ms.assetid: ad7d20bc-5eab-4390-a48b-5ea8e97ead7d
title: MFT_Grayscale Beispiel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 273c562eb5985d0a329c434a8e4aa44119744496
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130509"
---
# <a name="mft_grayscale-sample"></a><span data-ttu-id="69eb4-103">Beispiel für MFT \_ Grayscale</span><span class="sxs-lookup"><span data-stu-id="69eb4-103">MFT\_Grayscale Sample</span></span>

<span data-ttu-id="69eb4-104">Zeigt, wie ein Videoeffekt als Media Foundation Transformation (MFT) implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="69eb4-104">Shows how to implement a video effect as a Media Foundation Transform (MFT).</span></span> <span data-ttu-id="69eb4-105">Das Graustufen-MFT konvertiert das YUV-Video in Graustufen, indem die Chroma-Werte im Video auf neutral festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="69eb4-105">The grayscale MFT converts YUV video to grayscale by setting the chroma values in the video to neutral.</span></span> <span data-ttu-id="69eb4-106">Die MFT akzeptiert unkomprimierte Videos in den Formaten "UYVY", "im YUY2" oder "NV12".</span><span class="sxs-lookup"><span data-stu-id="69eb4-106">The MFT accepts uncompressed video in UYVY, YUY2, or NV12 formats.</span></span>

## <a name="apis-demonstrated"></a><span data-ttu-id="69eb4-107">Gezeigte APIs</span><span class="sxs-lookup"><span data-stu-id="69eb4-107">APIs Demonstrated</span></span>

<span data-ttu-id="69eb4-108">In diesem Beispiel werden die folgenden Microsoft Media Foundation Schnittstellen veranschaulicht:</span><span class="sxs-lookup"><span data-stu-id="69eb4-108">This sample demonstrates the following Microsoft Media Foundation interfaces:</span></span>

-   [<span data-ttu-id="69eb4-109">**IMF-Transformation**</span><span class="sxs-lookup"><span data-stu-id="69eb4-109">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

## <a name="usage"></a><span data-ttu-id="69eb4-110">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="69eb4-110">Usage</span></span>

<span data-ttu-id="69eb4-111">Das Beispiel MFT \_ Grayscale erstellt eine DLL, bei der es sich um einen com-Server für die MFT handelt.</span><span class="sxs-lookup"><span data-stu-id="69eb4-111">The MFT\_GrayScale sample builds a DLL that is a COM server for the MFT.</span></span> <span data-ttu-id="69eb4-112">Vor der Verwendung von MFT müssen Sie die dll registrieren.</span><span class="sxs-lookup"><span data-stu-id="69eb4-112">Before using the MFT, you must register the DLL.</span></span>

<span data-ttu-id="69eb4-113">Führen Sie das [playbackfx-Beispiel](/previous-versions//bb970336(v=vs.85))aus, um die verwendete Graustufen-MFT anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="69eb4-113">To see the grayscale MFT in use, run the [PlaybackFX Sample](/previous-versions//bb970336(v=vs.85)).</span></span> <span data-ttu-id="69eb4-114">Sie können auch das Tool topoedit verwenden, um eine Topologie zu erstellen, die das Graustufen-MFT enthält.</span><span class="sxs-lookup"><span data-stu-id="69eb4-114">You can also use the TopoEdit tool to build a topology that includes the grayscale MFT.</span></span> <span data-ttu-id="69eb4-115">Weitere Informationen zu topoedit finden Sie unter [topoedit](topoedit.md).</span><span class="sxs-lookup"><span data-stu-id="69eb4-115">For more information about TopoEdit, see [TopoEdit](topoedit.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="69eb4-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="69eb4-116">Requirements</span></span>



| <span data-ttu-id="69eb4-117">Produkt</span><span class="sxs-lookup"><span data-stu-id="69eb4-117">Product</span></span>                                                        | <span data-ttu-id="69eb4-118">Version</span><span class="sxs-lookup"><span data-stu-id="69eb4-118">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="69eb4-119">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="69eb4-119">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="69eb4-120">Windows 7</span><span class="sxs-lookup"><span data-stu-id="69eb4-120">Windows 7</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="69eb4-121">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="69eb4-121">Downloading the Sample</span></span>

<span data-ttu-id="69eb4-122">Dieses Beispiel ist im [GitHub-Repository für klassische Windows-Beispiele](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/mft_grayscale)verfügbar.</span><span class="sxs-lookup"><span data-stu-id="69eb4-122">This sample is available in the [Windows classic samples github repository](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/mft_grayscale).</span></span>

## <a name="related-topics"></a><span data-ttu-id="69eb4-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="69eb4-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="69eb4-124">Informationen zu YUV-Videos</span><span class="sxs-lookup"><span data-stu-id="69eb4-124">About YUV Video</span></span>](about-yuv-video.md)
</dt> <dt>

[<span data-ttu-id="69eb4-125">Media Foundation-SDK-Beispiele</span><span class="sxs-lookup"><span data-stu-id="69eb4-125">Media Foundation SDK Samples</span></span>](media-foundation-sdk-samples.md)
</dt> <dt>

[<span data-ttu-id="69eb4-126">Media Foundation Transformationen</span><span class="sxs-lookup"><span data-stu-id="69eb4-126">Media Foundation Transforms</span></span>](media-foundation-transforms.md)
</dt> <dt>

[<span data-ttu-id="69eb4-127">MFT \_ Audiodelay-Beispiel</span><span class="sxs-lookup"><span data-stu-id="69eb4-127">MFT\_AudioDelay Sample</span></span>](mft-audiodelay-sample.md)
</dt> <dt>

[<span data-ttu-id="69eb4-128">Schreiben eines benutzerdefinierten MFT</span><span class="sxs-lookup"><span data-stu-id="69eb4-128">Writing a Custom MFT</span></span>](writing-a-custom-mft.md)
</dt> </dl>

 

 
