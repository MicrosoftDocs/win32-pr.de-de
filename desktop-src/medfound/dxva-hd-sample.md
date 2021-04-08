---
description: Zeigt, wie Microsoft DirectX Video Acceleration High Definition (DXVA-HD) verwendet wird.
ms.assetid: dfd5cf5c-7d6e-4894-8d9b-41ef0293b3d3
title: DXVA-HD-Beispiel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71ae1945a98bc668aa12cc6cdf8d9e4693cbde27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861803"
---
# <a name="dxva-hd-sample"></a><span data-ttu-id="bafd6-103">DXVA-HD-Beispiel</span><span class="sxs-lookup"><span data-stu-id="bafd6-103">DXVA-HD Sample</span></span>

<span data-ttu-id="bafd6-104">Zeigt, wie Microsoft DirectX Video Acceleration High Definition (DXVA-HD) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="bafd6-104">Shows how to use Microsoft DirectX Video Acceleration High Definition (DXVA-HD).</span></span>

<span data-ttu-id="bafd6-105">Bei diesem Beispiel handelt es sich im Wesentlichen um einen Port des [DXVA2 \_ videoproc](dxva2-videoproc-sample.md)-Beispiels.</span><span class="sxs-lookup"><span data-stu-id="bafd6-105">This sample is essentially a port of the [DXVA2\_VideoProc Sample](dxva2-videoproc-sample.md).</span></span> <span data-ttu-id="bafd6-106">Sie verfügt über die gleichen grundlegenden Funktionen, und die meisten Tastaturbefehle sind identisch.</span><span class="sxs-lookup"><span data-stu-id="bafd6-106">It has the same basic functions, and most of the keyboard commands are the same.</span></span>

<span data-ttu-id="bafd6-107">Das Beispiel generiert Programm gesteuert Videos mit einem primären Stream und einem substream.</span><span class="sxs-lookup"><span data-stu-id="bafd6-107">The sample programmatically generates video with a primary stream and a substream.</span></span> <span data-ttu-id="bafd6-108">Der primäre Stream zeigt SMPTE-Farb leisten an.</span><span class="sxs-lookup"><span data-stu-id="bafd6-108">The primary stream displays SMPTE color bars.</span></span> <span data-ttu-id="bafd6-109">Der unter Datenstrom wird mithilfe von Luma-Schlüssel auf dem primären Stream gemischt.</span><span class="sxs-lookup"><span data-stu-id="bafd6-109">The substream is alpha-blended onto the primary stream using luma keying.</span></span> <span data-ttu-id="bafd6-110">Der Benutzer kann die Videoverarbeitungs Parameter ändern, einschließlich des planaren Alpha Werts, der Quell-und Ziel Rechtecke, Farbanpassungen und Farbraum.</span><span class="sxs-lookup"><span data-stu-id="bafd6-110">The user can change the video processing parameters, including the planar alpha value, source and destination rectangles, color adjustments, and color space.</span></span> <span data-ttu-id="bafd6-111">In der folgenden Abbildung wird das Video gezeigt, das generiert wird.</span><span class="sxs-lookup"><span data-stu-id="bafd6-111">The following image shows that video that is generated.</span></span>

![Screenshot des Beispiels "DXVA-HD"](images/dxva-hd-sample.png)

## <a name="apis-demonstrated"></a><span data-ttu-id="bafd6-113">Gezeigte APIs</span><span class="sxs-lookup"><span data-stu-id="bafd6-113">APIs Demonstrated</span></span>

<span data-ttu-id="bafd6-114">In diesem Beispiel werden die folgenden DXVA-HD-Schnittstellen veranschaulicht:</span><span class="sxs-lookup"><span data-stu-id="bafd6-114">This sample demonstrates the following DXVA-HD interfaces:</span></span>

-   [<span data-ttu-id="bafd6-115">**Idxvahd- \_ Gerät**</span><span class="sxs-lookup"><span data-stu-id="bafd6-115">**IDXVAHD\_Device**</span></span>](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_device)
-   [<span data-ttu-id="bafd6-116">**Idxvahd \_ videoprocessor**</span><span class="sxs-lookup"><span data-stu-id="bafd6-116">**IDXVAHD\_VideoProcessor**</span></span>](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_videoprocessor)

## <a name="requirements"></a><span data-ttu-id="bafd6-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bafd6-117">Requirements</span></span>



| <span data-ttu-id="bafd6-118">Produkt</span><span class="sxs-lookup"><span data-stu-id="bafd6-118">Product</span></span>                                                        | <span data-ttu-id="bafd6-119">Version</span><span class="sxs-lookup"><span data-stu-id="bafd6-119">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="bafd6-120">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="bafd6-120">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="bafd6-121">Windows 7</span><span class="sxs-lookup"><span data-stu-id="bafd6-121">Windows 7</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="bafd6-122">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="bafd6-122">Downloading the Sample</span></span>

<span data-ttu-id="bafd6-123">Dieses Beispiel ist im [GitHub-Repository für klassische Windows-Beispiele](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/DXVA_HD)verfügbar.</span><span class="sxs-lookup"><span data-stu-id="bafd6-123">This sample is available in the [Windows classic samples github repository](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/DXVA_HD).</span></span>

## <a name="related-topics"></a><span data-ttu-id="bafd6-124">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="bafd6-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bafd6-125">DXVA-HD</span><span class="sxs-lookup"><span data-stu-id="bafd6-125">DXVA-HD</span></span>](dxva-hd.md)
</dt> <dt>

[<span data-ttu-id="bafd6-126">Media Foundation-SDK-Beispiele</span><span class="sxs-lookup"><span data-stu-id="bafd6-126">Media Foundation SDK Samples</span></span>](media-foundation-sdk-samples.md)
</dt> </dl>

 

 



