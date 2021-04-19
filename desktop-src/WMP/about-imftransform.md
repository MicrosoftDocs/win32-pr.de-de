---
title: Informationen über IMF Transform
description: Informationen über IMF Transform
ms.assetid: 889f2d82-148a-4a7e-b78c-37ec86b37e0b
keywords:
- Windows Media Player-Plug-ins, Schnittstellen
- Plug-ins, Schnittstellen
- Plug-Ins für die digitale Signalverarbeitung, Schnittstellen
- DSP-Plug-ins, Schnittstellen
- Schnittstellen, DSP-Plug-ins
- Windows Media Player-Plug-ins, IMF Transform-Schnittstelle
- Plug-ins, IMF Transform-Schnittstelle
- Plug-Ins für die digitale Signalverarbeitung, IMF Transform-Schnittstelle
- DSP-Plug-ins, IMF Transform-Schnittstelle
- IMF Transform-Schnittstelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5eb58ab84070a8cb9390e4525b9b642f15a29f14
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341836"
---
# <a name="about-imftransform"></a><span data-ttu-id="f6d64-113">Informationen über IMF Transform</span><span class="sxs-lookup"><span data-stu-id="f6d64-113">About IMFTransform</span></span>

<span data-ttu-id="f6d64-114">Die **IMF Transform** -Schnittstelle ist eine der Schnittstellen, die von einem DSP-Plug-in mit zwei Modi implementiert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="f6d64-114">The **IMFTransform** interface is one of the interfaces that must be implemented by a dual-mode DSP plug-in.</span></span> <span data-ttu-id="f6d64-115">Windows Media Player Ruft die Methoden der **imftransform** -Schnittstelle auf, um Daten für das Plug-in bereitzustellen und verarbeitete Daten vom Plug-in abzurufen.</span><span class="sxs-lookup"><span data-stu-id="f6d64-115">Windows Media Player calls the methods of the **IMFTransform** interface to provide data to the plug-in and to retrieve processed data back from the plug-in.</span></span> <span data-ttu-id="f6d64-116">Eine umfassende Dokumentation der **IMF Transform** -Schnittstelle finden Sie im Abschnitt Media Foundation des Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="f6d64-116">For complete documentation of the **IMFTransform** interface, see the Media Foundation section of the Windows SDK.</span></span>

<span data-ttu-id="f6d64-117">Die Methoden von **IMF Transform** können wie folgt kategorisiert werden.</span><span class="sxs-lookup"><span data-stu-id="f6d64-117">The methods of **IMFTransform** can be categorized as follows.</span></span>

## <a name="methods-that-handle-format-negotiation"></a><span data-ttu-id="f6d64-118">Methoden, die die Format Aushandlung behandeln</span><span class="sxs-lookup"><span data-stu-id="f6d64-118">Methods That Handle Format Negotiation</span></span>

<span data-ttu-id="f6d64-119">Windows Media Player Ruft die folgenden Methoden auf, um Informationen zu den vom Plug-in unterstützten Datenformaten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="f6d64-119">Windows Media Player calls the following methods to get information about the data formats supported by the plug-in.</span></span>

-   <span data-ttu-id="f6d64-120">**Getstreamcount**</span><span class="sxs-lookup"><span data-stu-id="f6d64-120">**GetStreamCount**</span></span>
-   <span data-ttu-id="f6d64-121">**Getstreamlimits**</span><span class="sxs-lookup"><span data-stu-id="f6d64-121">**GetStreamLimits**</span></span>
-   <span data-ttu-id="f6d64-122">**Getinputstreaminfo**</span><span class="sxs-lookup"><span data-stu-id="f6d64-122">**GetInputStreamInfo**</span></span>
-   <span data-ttu-id="f6d64-123">**Getoutputstreaminfo**</span><span class="sxs-lookup"><span data-stu-id="f6d64-123">**GetOutputStreamInfo**</span></span>
-   <span data-ttu-id="f6d64-124">**Getinputavailabletype**</span><span class="sxs-lookup"><span data-stu-id="f6d64-124">**GetInputAvailableType**</span></span>
-   <span data-ttu-id="f6d64-125">**Getoutputavailabletype**</span><span class="sxs-lookup"><span data-stu-id="f6d64-125">**GetOutputAvailableType**</span></span>
-   <span data-ttu-id="f6d64-126">**"Ttinputtype"**</span><span class="sxs-lookup"><span data-stu-id="f6d64-126">**SetInputType**</span></span>
-   <span data-ttu-id="f6d64-127">**Setoutputtype**</span><span class="sxs-lookup"><span data-stu-id="f6d64-127">**SetOutputType**</span></span>
-   <span data-ttu-id="f6d64-128">**GetAttributes**</span><span class="sxs-lookup"><span data-stu-id="f6d64-128">**GetAttributes**</span></span>
-   <span data-ttu-id="f6d64-129">**Getinputstreamattribute**</span><span class="sxs-lookup"><span data-stu-id="f6d64-129">**GetInputStreamAttributes**</span></span>
-   <span data-ttu-id="f6d64-130">**Getoutputstreamattribute**</span><span class="sxs-lookup"><span data-stu-id="f6d64-130">**GetOutputStreamAttributes**</span></span>
-   <span data-ttu-id="f6d64-131">**Getstreamids**</span><span class="sxs-lookup"><span data-stu-id="f6d64-131">**GetStreamIDs**</span></span>

## <a name="methods-that-specify-or-retrieve-state-information"></a><span data-ttu-id="f6d64-132">Methoden zum angeben oder Abrufen von Zustandsinformationen</span><span class="sxs-lookup"><span data-stu-id="f6d64-132">Methods That Specify or Retrieve State Information</span></span>

<span data-ttu-id="f6d64-133">Windows Media Player Ruft die folgenden Methoden auf, um Werte zu erhalten, die sich auf den aktuellen Status des Plug-ins beziehen, oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="f6d64-133">Windows Media Player calls the following methods to get or set values related to the current state of the plug-in.</span></span>

-   <span data-ttu-id="f6d64-134">**"Ttinputtype"**</span><span class="sxs-lookup"><span data-stu-id="f6d64-134">**SetInputType**</span></span>
-   <span data-ttu-id="f6d64-135">**Setoutputtype**</span><span class="sxs-lookup"><span data-stu-id="f6d64-135">**SetOutputType**</span></span>
-   <span data-ttu-id="f6d64-136">**Getinputcurrenttype**</span><span class="sxs-lookup"><span data-stu-id="f6d64-136">**GetInputCurrentType**</span></span>
-   <span data-ttu-id="f6d64-137">**Getoutputcurrenttype**</span><span class="sxs-lookup"><span data-stu-id="f6d64-137">**GetOutputCurrentType**</span></span>
-   <span data-ttu-id="f6d64-138">**Getinputstatus**</span><span class="sxs-lookup"><span data-stu-id="f6d64-138">**GetInputStatus**</span></span>
-   <span data-ttu-id="f6d64-139">**Addinputstreams**</span><span class="sxs-lookup"><span data-stu-id="f6d64-139">**AddInputStreams**</span></span>
-   <span data-ttu-id="f6d64-140">**Delta Input Streams**</span><span class="sxs-lookup"><span data-stu-id="f6d64-140">**DeleteInputStreams**</span></span>
-   <span data-ttu-id="f6d64-141">**Getoutputstatus**</span><span class="sxs-lookup"><span data-stu-id="f6d64-141">**GetOutputStatus**</span></span>
-   <span data-ttu-id="f6d64-142">**Setoutputbounds**</span><span class="sxs-lookup"><span data-stu-id="f6d64-142">**SetOutputBounds**</span></span>

> [!Note]  
> <span data-ttu-id="f6d64-143">**Setinputtype** und **setoutputtype** werden sowohl für die Format Aushandlung als auch für das angeben und Abrufen von Zustandsinformationen verwendet.</span><span class="sxs-lookup"><span data-stu-id="f6d64-143">**SetInputType** and **SetOutputType** are used both for format negotiation and for specifying and retrieving state information.</span></span>

 

## <a name="methods-that-handle-buffering-and-processing-data"></a><span data-ttu-id="f6d64-144">Methoden, die die Pufferung und Verarbeitung von Daten verarbeiten</span><span class="sxs-lookup"><span data-stu-id="f6d64-144">Methods That Handle Buffering and Processing Data</span></span>

<span data-ttu-id="f6d64-145">Windows Media Player Ruft die folgenden Methoden auf, um die verschiedenen Prozesse zu initiieren, die das Plug-in für die digitale Signalverarbeitung durchführt.</span><span class="sxs-lookup"><span data-stu-id="f6d64-145">Windows Media Player calls the following methods to initiate the various processes that the plug-in performs to do the digital signal processing.</span></span>

-   <span data-ttu-id="f6d64-146">**ProcessInput**</span><span class="sxs-lookup"><span data-stu-id="f6d64-146">**ProcessInput**</span></span>
-   <span data-ttu-id="f6d64-147">**ProcessOutput**</span><span class="sxs-lookup"><span data-stu-id="f6d64-147">**ProcessOutput**</span></span>
-   <span data-ttu-id="f6d64-148">**ProcessMessage**</span><span class="sxs-lookup"><span data-stu-id="f6d64-148">**ProcessMessage**</span></span>
-   <span data-ttu-id="f6d64-149">**ProcessEvent**</span><span class="sxs-lookup"><span data-stu-id="f6d64-149">**ProcessEvent**</span></span>

## <a name="related-topics"></a><span data-ttu-id="f6d64-150">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f6d64-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f6d64-151">**Erforderliche Schnittstellen**</span><span class="sxs-lookup"><span data-stu-id="f6d64-151">**Required Interfaces**</span></span>](required-interfaces.md)
</dt> </dl>

 

 




