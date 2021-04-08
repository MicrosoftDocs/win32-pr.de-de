---
description: Beispiel für Ball Filter
ms.assetid: 80a6db64-ef13-46a2-8f2a-e39095e874b2
title: Beispiel für Ball Filter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93b80301b233f0c1e74933c93fe86a0e1878458e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103860473"
---
# <a name="ball-filter-sample"></a><span data-ttu-id="aaaec-103">Beispiel für Ball Filter</span><span class="sxs-lookup"><span data-stu-id="aaaec-103">Ball Filter Sample</span></span>

## <a name="description"></a><span data-ttu-id="aaaec-104">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="aaaec-104">Description</span></span>

<span data-ttu-id="aaaec-105">Der Kugel Filter ist ein Video Quell Filter, der ein Bild eines Sprung-Balls erzeugt.</span><span class="sxs-lookup"><span data-stu-id="aaaec-105">The Ball Filter is a video source filter that produces an image of a bouncing ball.</span></span> <span data-ttu-id="aaaec-106">Dieses Beispiel veranschaulicht die Format Aushandlung und die Verwendung der Quell Filter-Basisklassen [**CSource**](csource.md) und [**csourcestream**](csourcestream.md).</span><span class="sxs-lookup"><span data-stu-id="aaaec-106">This sample illustrates format negotiation and the use of the source filter base classes [**CSource**](csource.md) and [**CSourceStream**](csourcestream.md).</span></span>

<span data-ttu-id="aaaec-107">Der Code in "f. h" und "f. cpp" verwaltet die Filter Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="aaaec-107">The code in Fball.h and Fball.cpp manages the filter interfaces.</span></span> <span data-ttu-id="aaaec-108">Diese beiden Dateien enthalten ungefähr den minimalen Code, der für einen Quell Filter erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="aaaec-108">Those two files contain approximately the minimum code required for a source filter.</span></span> <span data-ttu-id="aaaec-109">Die Dateien Ball. h und Ball. cpp enthalten den Code, der die Kugel springt.</span><span class="sxs-lookup"><span data-stu-id="aaaec-109">The Ball.h and Ball.cpp files contain the code that bounces the ball.</span></span>

<span data-ttu-id="aaaec-110">Dieser Filter verfügt über ein einzelnes Ausgabepin, das einen Videostream bereitstellt, der eine Kugel im Frame aufspringt.</span><span class="sxs-lookup"><span data-stu-id="aaaec-110">This filter has a single output pin, which provides a video stream that shows a ball bouncing around in the frame.</span></span> <span data-ttu-id="aaaec-111">Der Kugel Filter akzeptiert auch Qualitäts Verwaltungsanforderungen des downstreamfilters, die eine einfache Qualitäts Verwaltungs Strategie veranschaulichen.</span><span class="sxs-lookup"><span data-stu-id="aaaec-111">The Ball filter also accepts quality management requests from the downstream filter, which illustrates a simple quality management strategy.</span></span> <span data-ttu-id="aaaec-112">Dieser Filter implementiert die [**iqualitycontrol**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) -Schnittstelle zu diesem Zweck.</span><span class="sxs-lookup"><span data-stu-id="aaaec-112">This filter implements the [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) interface for that purpose.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="aaaec-113">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="aaaec-113">Downloading the Sample</span></span>

<span data-ttu-id="aaaec-114">Zum Herunterladen der DirectShow SDK-Beispiele installieren Sie die neueste Version der [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="aaaec-114">To download the DirectShow SDK samples, install the latest version of the [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span>

<span data-ttu-id="aaaec-115">Dieses Beispiel wird unter folgendem Pfad installiert: \[ *SDK Root* \] \\ Samples \\ Multimedia \\ DirectShow \\ Filters \\ Ball.</span><span class="sxs-lookup"><span data-stu-id="aaaec-115">This sample is installed under the following path: \[*SDK Root*\]\\Samples\\Multimedia\\DirectShow\\Filters\\Ball.</span></span>

## <a name="related-topics"></a><span data-ttu-id="aaaec-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="aaaec-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aaaec-117">DirectShow-Beispiele</span><span class="sxs-lookup"><span data-stu-id="aaaec-117">DirectShow Samples</span></span>](directshow-samples.md)
</dt> </dl>

 

 



