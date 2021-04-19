---
description: Verwenden der WDDM-Erfassung in DirectShow
ms.assetid: 57ee86b0-50bc-4992-94d4-f290f83d2afc
title: Verwenden der WDDM-Erfassung in DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7926af70a3b7f1c4ba67c791d98c9928c3809b89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360655"
---
# <a name="using-wddm-capture-in-directshow"></a><span data-ttu-id="65e7f-103">Verwenden der WDDM-Erfassung in DirectShow</span><span class="sxs-lookup"><span data-stu-id="65e7f-103">Using WDDM Capture in DirectShow</span></span>

<span data-ttu-id="65e7f-104">Dieses Thema gilt für Windows Vista und höher.</span><span class="sxs-lookup"><span data-stu-id="65e7f-104">This topic applies to Windows Vista and later.</span></span>

<span data-ttu-id="65e7f-105">Einige Videokarten verfügen über integrierte Funktionen für die Videoaufzeichnung.</span><span class="sxs-lookup"><span data-stu-id="65e7f-105">Some video cards have integrated video capture functionality.</span></span> <span data-ttu-id="65e7f-106">Auf diesen Karten werden erfasste Videorahmen in den Videospeicher (VRAM) eingefügt.</span><span class="sxs-lookup"><span data-stu-id="65e7f-106">On these cards, captured video frames are placed in video memory (VRAM).</span></span> <span data-ttu-id="65e7f-107">Vor Windows Vista gab es keinen Standardmechanismus für die Verarbeitung der Frames, während Sie im VRAM verbleibt.</span><span class="sxs-lookup"><span data-stu-id="65e7f-107">Prior to Windows Vista, there was no standard mechanism for processing the frames while they remained in VRAM.</span></span> <span data-ttu-id="65e7f-108">Stattdessen mussten die Daten in den Systemspeicher kopiert, verarbeitet und dann zur Anzeige wieder in den VRAM kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="65e7f-108">Instead, the data had to be copied into system memory, processed, and then copied back to VRAM for display.</span></span> <span data-ttu-id="65e7f-109">In Windows Vista unterstützt DirectShow nun einen Mechanismus, um die Video Frames im VRAM in der gesamten Verarbeitungs Pipeline zu halten, von der Erfassung bis zum anzeigen.</span><span class="sxs-lookup"><span data-stu-id="65e7f-109">In Windows Vista, DirectShow now supports a mechanism for keeping the video frames in VRAM throughout the processing pipeline, from capture to display.</span></span>

<span data-ttu-id="65e7f-110">Der ksproxy-Filter bestimmt, ob der Treiber die VRAM-Oberflächen Erfassung unterstützt, indem er den Treiber für die bevorzugte ksproperty- \_ \_ Erfassungs \_ Oberflächen Eigenschaft abfragt.</span><span class="sxs-lookup"><span data-stu-id="65e7f-110">The KsProxy filter determines if the driver supports VRAM surface capture by querying the driver for the KSPROPERTY\_PREFERRED\_CAPTURE\_SURFACE property.</span></span> <span data-ttu-id="65e7f-111">(Diese Eigenschaft ist in der Dokumentation zum Windows-Treiberkit dokumentiert.) Wenn der Treiber die VRAM-Oberflächen Erfassung unterstützt, ordnet ksproxy eine spezielle Art von Medien Beispiel zu, das einen Zeiger auf eine Direct3D-Oberfläche enthält.</span><span class="sxs-lookup"><span data-stu-id="65e7f-111">(This property is documented in the Windows Driver Kit documentation.) If the driver supports VRAM surface capture, KsProxy allocates a special kind of media sample that holds a pointer to a Direct3D surface.</span></span>

<span data-ttu-id="65e7f-112">Anschließend bestimmt ksproxy, ob der Downstream-Filter die DirectX-Video Beschleunigung (DXVA) 2,0 unterstützt, wie folgt:</span><span class="sxs-lookup"><span data-stu-id="65e7f-112">Next, KsProxy determines whether the downstream filter supports DirectX Video Acceleration (DXVA) 2.0, as follows:</span></span>

1.  <span data-ttu-id="65e7f-113">Ksproxy fragt die downstreameingabepin für die **IMF GetService** -Schnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="65e7f-113">KsProxy queries the downstream input pin for the **IMFGetService** interface.</span></span>
2.  <span data-ttu-id="65e7f-114">Wenn die PIN " **IMF**" verfügbar macht, ruft "ksproxy" **IMF GetService:: GetService** für die **IDirect3DDeviceManager** -Schnittstelle auf.</span><span class="sxs-lookup"><span data-stu-id="65e7f-114">If the pin exposes **IMFGetService**, KsProxy calls **IMFGetService::GetService** for the **IDirect3DDeviceManager** interface.</span></span> <span data-ttu-id="65e7f-115">Der Dienst Bezeichner ist der Mr- \_ Video \_ Acceleration \_ Service.</span><span class="sxs-lookup"><span data-stu-id="65e7f-115">The service identier is MR\_VIDEO\_ACCELERATION\_SERVICE.</span></span>

<span data-ttu-id="65e7f-116">Beide Schnittstellen sind in der Media Foundation SDK-Dokumentation dokumentiert.</span><span class="sxs-lookup"><span data-stu-id="65e7f-116">Both of these interfaces are documented in the Media Foundation SDK documentation.</span></span>

<span data-ttu-id="65e7f-117">Wenn der Downstream-Filter DXVA 2,0 nicht unterstützt, ordnet ksproxy einen zusätzlichen Systemspeicher Puffer zu.</span><span class="sxs-lookup"><span data-stu-id="65e7f-117">If the downstream filter does not support DXVA 2.0, KsProxy allocates an additional system memory buffer.</span></span> <span data-ttu-id="65e7f-118">Dieser Puffer wird verwendet, um die Video Frames aus VRAM in den Systemspeicher zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="65e7f-118">It uses this buffer to copy the video frames from VRAM to system memory.</span></span> <span data-ttu-id="65e7f-119">Die [**imediasample:: getpointer**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getpointer) -Methode des Medien Beispiels gibt einen Zeiger auf diesen Systemspeicher Puffer zurück.</span><span class="sxs-lookup"><span data-stu-id="65e7f-119">The media sample's [**IMediaSample::GetPointer**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getpointer) method returns a pointer to this system memory buffer.</span></span>

<span data-ttu-id="65e7f-120">Wenn der Downstream-Filter jedoch DXVA 2,0 unterstützt, weist ksproxy keinen Systemspeicher Puffer zu.</span><span class="sxs-lookup"><span data-stu-id="65e7f-120">However, if the downstream filter does support DXVA 2.0, then KsProxy does not allocate a system memory buffer.</span></span> <span data-ttu-id="65e7f-121">In diesem Fall gibt die **getpointer** -Methode E \_ notimpl zurück.</span><span class="sxs-lookup"><span data-stu-id="65e7f-121">In that case, the **GetPointer** method returns E\_NOTIMPL.</span></span> <span data-ttu-id="65e7f-122">Stattdessen wird erwartet, dass der Downstream-Filter direkt auf die Direct3D-Oberfläche des Beispiels zugreift.</span><span class="sxs-lookup"><span data-stu-id="65e7f-122">Instead, the downstream filter is expected to access the sample's Direct3D surface directly.</span></span> <span data-ttu-id="65e7f-123">Es gibt zwei Möglichkeiten für den downstreamfilter, einen Zeiger auf die-Oberfläche zu erhalten. beide sind gleichwertig:</span><span class="sxs-lookup"><span data-stu-id="65e7f-123">There are two ways for the downstream filter to get a pointer to the surface, both of them equivalent:</span></span>

-   <span data-ttu-id="65e7f-124">Fragen Sie das Beispiel nach der **imfgetservice** -Schnittstelle ab, und nennen Sie **GetService** für die **IDirect3DSurface9** -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="65e7f-124">Query the sample for the **IMFGetService** interface and call **GetService** for the **IDirect3DSurface9** interface.</span></span> <span data-ttu-id="65e7f-125">Der Dienst Bezeichner ist der Mr- \_ Puffer \_ Dienst.</span><span class="sxs-lookup"><span data-stu-id="65e7f-125">The service identifier is MR\_BUFFER\_SERVICE.</span></span>
-   <span data-ttu-id="65e7f-126">Fragen Sie das Beispiel nach der [**IMediaSample2Config**](/windows/desktop/api/Strmif/nn-strmif-imediasample2config) -Schnittstelle ab, und nennen Sie [**IMediaSample2Config:: getSurface**](/windows/desktop/api/Strmif/nf-strmif-imediasample2config-getsurface).</span><span class="sxs-lookup"><span data-stu-id="65e7f-126">Query the sample for the [**IMediaSample2Config**](/windows/desktop/api/Strmif/nn-strmif-imediasample2config) interface and call [**IMediaSample2Config::GetSurface**](/windows/desktop/api/Strmif/nf-strmif-imediasample2config-getsurface).</span></span>

## <a name="related-topics"></a><span data-ttu-id="65e7f-127">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="65e7f-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="65e7f-128">Erweiterte Erfassungs Themen</span><span class="sxs-lookup"><span data-stu-id="65e7f-128">Advanced Capture Topics</span></span>](advanced-capture-topics.md)
</dt> </dl>

 

 



