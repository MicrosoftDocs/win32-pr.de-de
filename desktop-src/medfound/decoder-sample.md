---
description: Zeigt, wie ein Decoder für Microsoft Media Foundation geschrieben wird.
ms.assetid: 941e5400-e679-41f4-9830-3548dc6037aa
title: Decoder-Beispiel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dd7586534876cfa7f530e675b0342a92bf46b8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958649"
---
# <a name="decoder-sample"></a><span data-ttu-id="59978-103">Decoder-Beispiel</span><span class="sxs-lookup"><span data-stu-id="59978-103">Decoder Sample</span></span>

<span data-ttu-id="59978-104">Zeigt, wie ein Decoder für Microsoft Media Foundation geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="59978-104">Shows how to write a decoder for Microsoft Media Foundation.</span></span>

<span data-ttu-id="59978-105">In diesem Beispiel wird ein Mock-MPEG-1-Video Decoder implementiert, der den Zeit Code für jeden Videorahmen anzeigt.</span><span class="sxs-lookup"><span data-stu-id="59978-105">This sample implements a mock MPEG-1 video decoder that displays the time code for each video frame.</span></span> <span data-ttu-id="59978-106">Der MPEG-1-Bitstream wird nicht tatsächlich decodiert.</span><span class="sxs-lookup"><span data-stu-id="59978-106">It does not actually decode the MPEG-1 bitstream.</span></span> <span data-ttu-id="59978-107">Die folgende Abbildung zeigt die Videoausgabe des Decoders.</span><span class="sxs-lookup"><span data-stu-id="59978-107">The following image shows the video output from the decoder.</span></span>

![Screenshot eines Video Frames vom Decoder](images/decodersample.png)

> [!Note]  
> <span data-ttu-id="59978-109">Vor der Windows SDK für Windows 7 war dieses Beispiel als Teil des [MPEG1Source](mpeg1source-sample.md)-Beispiels enthalten.</span><span class="sxs-lookup"><span data-stu-id="59978-109">Prior to the Windows SDK for Windows 7, this sample was included as part of the [MPEG1Source Sample](mpeg1source-sample.md).</span></span>

 

## <a name="apis-demonstrated"></a><span data-ttu-id="59978-110">Gezeigte APIs</span><span class="sxs-lookup"><span data-stu-id="59978-110">APIs Demonstrated</span></span>

<span data-ttu-id="59978-111">In diesem Beispiel werden die folgenden Media Foundation Schnittstellen veranschaulicht:</span><span class="sxs-lookup"><span data-stu-id="59978-111">This sample demonstrates the following Media Foundation interfaces:</span></span>

-   [<span data-ttu-id="59978-112">**IMF-Transformation**</span><span class="sxs-lookup"><span data-stu-id="59978-112">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

## <a name="requirements"></a><span data-ttu-id="59978-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="59978-113">Requirements</span></span>



| <span data-ttu-id="59978-114">Produkt</span><span class="sxs-lookup"><span data-stu-id="59978-114">Product</span></span>                                                        | <span data-ttu-id="59978-115">Version</span><span class="sxs-lookup"><span data-stu-id="59978-115">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="59978-116">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="59978-116">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="59978-117">Windows 7</span><span class="sxs-lookup"><span data-stu-id="59978-117">Windows 7</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="59978-118">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="59978-118">Downloading the Sample</span></span>

<span data-ttu-id="59978-119">Dieses Beispiel ist im [GitHub-Repository für klassische Windows-Beispiele](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/Decoder)verfügbar.</span><span class="sxs-lookup"><span data-stu-id="59978-119">This sample is available in the [Windows classic samples github repository](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/Decoder).</span></span>

## <a name="related-topics"></a><span data-ttu-id="59978-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="59978-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="59978-121">Media Foundation-SDK-Beispiele</span><span class="sxs-lookup"><span data-stu-id="59978-121">Media Foundation SDK Samples</span></span>](media-foundation-sdk-samples.md)
</dt> <dt>

[<span data-ttu-id="59978-122">Media Foundation Transformationen</span><span class="sxs-lookup"><span data-stu-id="59978-122">Media Foundation Transforms</span></span>](media-foundation-transforms.md)
</dt> <dt>

[<span data-ttu-id="59978-123">Schreiben eines benutzerdefinierten MFT</span><span class="sxs-lookup"><span data-stu-id="59978-123">Writing a Custom MFT</span></span>](writing-a-custom-mft.md)
</dt> </dl>

 

 



