---
description: Evrpresenter-Beispiel
ms.assetid: 791a9816-4c40-4683-8b32-22f73d7fe84d
title: Evrpresenter-Beispiel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bde85de152c41f348b1aae74a8c0d67ca746cab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127889"
---
# <a name="evrpresenter-sample"></a><span data-ttu-id="e5375-103">Evrpresenter-Beispiel</span><span class="sxs-lookup"><span data-stu-id="e5375-103">EVRPresenter Sample</span></span>

<span data-ttu-id="e5375-104">Zeigt, wie ein benutzerdefinierter Presenter für den [erweiterten Videorenderer](enhanced-video-renderer.md) (EVR) implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="e5375-104">Shows how to implement a custom presenter for the [Enhanced Video Renderer](enhanced-video-renderer.md) (EVR).</span></span> <span data-ttu-id="e5375-105">Der benutzerdefinierte Presenter kann entweder mit dem DirectShow-EVR-Filter oder der Microsoft Media Foundation EVR-Senke verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e5375-105">The custom presenter can be used with either the DirectShow EVR filter or the Microsoft Media Foundation EVR sink.</span></span>

## <a name="apis-demonstrated"></a><span data-ttu-id="e5375-106">Gezeigte APIs</span><span class="sxs-lookup"><span data-stu-id="e5375-106">APIs Demonstrated</span></span>

<span data-ttu-id="e5375-107">In diesem Beispiel werden die folgenden Media Foundation Schnittstellen veranschaulicht:</span><span class="sxs-lookup"><span data-stu-id="e5375-107">This sample demonstrates the following Media Foundation interfaces:</span></span>

-   [<span data-ttu-id="e5375-108">**IMF-staatink**</span><span class="sxs-lookup"><span data-stu-id="e5375-108">**IMFClockStateSink**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink)
-   [<span data-ttu-id="e5375-109">**Imfratesupport**</span><span class="sxs-lookup"><span data-stu-id="e5375-109">**IMFRateSupport**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)
-   [<span data-ttu-id="e5375-110">**Imftopologyservicelookupclient**</span><span class="sxs-lookup"><span data-stu-id="e5375-110">**IMFTopologyServiceLookupClient**</span></span>](/windows/desktop/api/evr/nn-evr-imftopologyservicelookupclient)
-   [<span data-ttu-id="e5375-111">**IMF videoabviceid**</span><span class="sxs-lookup"><span data-stu-id="e5375-111">**IMFVideoDeviceID**</span></span>](/windows/desktop/api/evr/nn-evr-imfvideodeviceid)
-   [<span data-ttu-id="e5375-112">**IMF videodisplaycontrol**</span><span class="sxs-lookup"><span data-stu-id="e5375-112">**IMFVideoDisplayControl**</span></span>](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol)
-   [<span data-ttu-id="e5375-113">**IMF videopresenter**</span><span class="sxs-lookup"><span data-stu-id="e5375-113">**IMFVideoPresenter**</span></span>](/windows/desktop/api/evr/nn-evr-imfvideopresenter)

## <a name="usage"></a><span data-ttu-id="e5375-114">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="e5375-114">Usage</span></span>

<span data-ttu-id="e5375-115">Das Ereignis evrpresenter erstellt eine DLL, bei der es sich um einen com-Server für den Presenter handelt.</span><span class="sxs-lookup"><span data-stu-id="e5375-115">The EVRPresenter sample builds a DLL that is a COM server for the presenter.</span></span> <span data-ttu-id="e5375-116">Bevor Sie den benutzerdefinierten Presenter verwenden, müssen Sie die dll registrieren.</span><span class="sxs-lookup"><span data-stu-id="e5375-116">Before using the custom presenter, you must register the DLL.</span></span>

<span data-ttu-id="e5375-117">So verwenden Sie dieses Beispiel in Media Foundation:</span><span class="sxs-lookup"><span data-stu-id="e5375-117">To use this sample in Media Foundation:</span></span>

1.  <span data-ttu-id="e5375-118">Erstellen Sie das Beispiel.</span><span class="sxs-lookup"><span data-stu-id="e5375-118">Build the sample.</span></span>
2.  <span data-ttu-id="e5375-119">Regsvr32-EvrPresenter.dll.</span><span class="sxs-lookup"><span data-stu-id="e5375-119">Regsvr32 EvrPresenter.dll.</span></span>
3.  <span data-ttu-id="e5375-120">Erstellen Sie das [MF Player-Beispiel](/previous-versions//bb970516(v=vs.85))und führen Sie es aus.</span><span class="sxs-lookup"><span data-stu-id="e5375-120">Build and run the [MFPlayer Sample](/previous-versions//bb970516(v=vs.85)).</span></span>
4.  <span data-ttu-id="e5375-121">Wählen Sie im Menü **Datei** die Option Datei **Öffnen** aus.</span><span class="sxs-lookup"><span data-stu-id="e5375-121">From the **File** menu, select **Open** File.</span></span>
5.  <span data-ttu-id="e5375-122">Wählen Sie im Dialogfeld **Datei öffnen** die Option **Custom EVR Presenter aus.**</span><span class="sxs-lookup"><span data-stu-id="e5375-122">In the **Open File** dialog box, select **Custom EVR Presenter.**</span></span>
6.  <span data-ttu-id="e5375-123">Wählen Sie eine Datei für die Wiedergabe aus.</span><span class="sxs-lookup"><span data-stu-id="e5375-123">Select a file for playback.</span></span>

<span data-ttu-id="e5375-124">So verwenden Sie dieses Beispiel in DirectShow:</span><span class="sxs-lookup"><span data-stu-id="e5375-124">To use this sample in DirectShow:</span></span>

1.  <span data-ttu-id="e5375-125">Erstellen Sie das Beispiel.</span><span class="sxs-lookup"><span data-stu-id="e5375-125">Build the sample.</span></span>
2.  <span data-ttu-id="e5375-126">Registrieren Sie EvrPresenter.dll.</span><span class="sxs-lookup"><span data-stu-id="e5375-126">Register EvrPresenter.dll.</span></span>
3.  <span data-ttu-id="e5375-127">Erstellen Sie das Beispiel evrplayer, und führen Sie es aus.</span><span class="sxs-lookup"><span data-stu-id="e5375-127">Build and run the EVRPlayer sample.</span></span> <span data-ttu-id="e5375-128">Dieses Beispiel ist in den DirectShow-Beispielen in der Windows SDK enthalten.</span><span class="sxs-lookup"><span data-stu-id="e5375-128">This sample is included with the DirectShow samples in the Windows SDK.</span></span>
4.  <span data-ttu-id="e5375-129">Wählen Sie im Menü **Datei** die Option **EVR Presenter** aus.</span><span class="sxs-lookup"><span data-stu-id="e5375-129">From the **File** menu, select **EVR Presenter**.</span></span>
5.  <span data-ttu-id="e5375-130">Wählen Sie eine Datei für die Wiedergabe aus.</span><span class="sxs-lookup"><span data-stu-id="e5375-130">Select a file for playback.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5375-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e5375-131">Requirements</span></span>



| <span data-ttu-id="e5375-132">Produkt</span><span class="sxs-lookup"><span data-stu-id="e5375-132">Product</span></span>                                                        | <span data-ttu-id="e5375-133">Version</span><span class="sxs-lookup"><span data-stu-id="e5375-133">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="e5375-134">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="e5375-134">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="e5375-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e5375-135">Windows 7</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="e5375-136">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="e5375-136">Downloading the Sample</span></span>

<span data-ttu-id="e5375-137">Dieses Beispiel ist im [GitHub-Repository für klassische Windows-Beispiele](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/AudioClip)verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e5375-137">This sample is available in the [Windows classic samples github repository](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/AudioClip).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e5375-138">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e5375-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e5375-139">Erweiterter Videorenderer</span><span class="sxs-lookup"><span data-stu-id="e5375-139">Enhanced Video Renderer</span></span>](enhanced-video-renderer.md)
</dt> <dt>

[<span data-ttu-id="e5375-140">Schreiben von EVR Presenter</span><span class="sxs-lookup"><span data-stu-id="e5375-140">How to Write an EVR Presenter</span></span>](how-to-write-an-evr-presenter.md)
</dt> <dt>

[<span data-ttu-id="e5375-141">Media Foundation-SDK-Beispiele</span><span class="sxs-lookup"><span data-stu-id="e5375-141">Media Foundation SDK Samples</span></span>](media-foundation-sdk-samples.md)
</dt> </dl>

 

 
