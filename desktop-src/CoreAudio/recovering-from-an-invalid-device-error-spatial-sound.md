---
description: Wiederherstellen nach einem Invalid-Device Fehler (räumlicher Sound)
title: Wiederherstellen nach einem Invalid-Device Fehler (räumlicher Sound)
ms.topic: article
ms.date: 10/29/2020
ms.openlocfilehash: 1ec4f040aff10f2d118b20c489e74d792c907113
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127424"
---
# <a name="recovering-from-an-invalid-device-error-spatial-sound"></a><span data-ttu-id="ef9fd-103">Wiederherstellen nach einem Invalid-Device Fehler (räumlicher Sound)</span><span class="sxs-lookup"><span data-stu-id="ef9fd-103">Recovering from an Invalid-Device Error (Spatial Sound)</span></span>

<span data-ttu-id="ef9fd-104">Viele der Methoden der räumlichen Audio-API von Microsoft, wie z. b. [ispatialaudioclient](/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient), [ispatialaudioobjectrenderstream](/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobjectrenderstream)und [ispatialaudioobject](/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobject), geben Fehlercodes zurück, wenn das audioendpunktgerät, das die Client Anwendung verwendet, ungültig wird oder das räumliche audiorenderingformat für den Endpunkt geändert wird.</span><span class="sxs-lookup"><span data-stu-id="ef9fd-104">Many of the methods of the Microsoft Spatial Audio API, such as [ISpatialAudioClient](/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient), [ISpatialAudioObjectRenderStream](/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobjectrenderstream), and [ISpatialAudioObject](/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobject), return error codes if the audio endpoint device that the client application is using becomes invalid or the spatial audio rendering format is changed on the endpoint.</span></span> <span data-ttu-id="ef9fd-105">Diese Fehlercodes geben an, dass das Endpunkt Gerät getrennt wurde oder dass die Audiohardware oder die zugehörigen Hardware Ressourcen neu konfiguriert, deaktiviert, entfernt, der räumliche Audiomodus geändert oder anderweitig nicht zur Verwendung zur Verfügung gestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="ef9fd-105">These error codes indicates that the endpoint device has been unplugged, or that the audio hardware or associated hardware resources have been reconfigured, disabled, removed, spatial audio mode is changed or otherwise made unavailable for use.</span></span> <span data-ttu-id="ef9fd-106">Häufig kann die Anwendung nach diesem Fehler wieder hergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="ef9fd-106">Frequently, the application can recover from this error.</span></span>

<span data-ttu-id="ef9fd-107">Fehlercodes, die auf einen ungültigen Gerätefehler hinweisen, sind folgende:</span><span class="sxs-lookup"><span data-stu-id="ef9fd-107">Error codes that indicate an invalid-device error include the following:</span></span>

- <span data-ttu-id="ef9fd-108">SPTLAUDCLNT_E_DESTROYED</span><span class="sxs-lookup"><span data-stu-id="ef9fd-108">SPTLAUDCLNT_E_DESTROYED</span></span>
- <span data-ttu-id="ef9fd-109">AUDCLNT_E_DEVICE_INVALIDATED</span><span class="sxs-lookup"><span data-stu-id="ef9fd-109">AUDCLNT_E_DEVICE_INVALIDATED</span></span>
- <span data-ttu-id="ef9fd-110">AUDCLNT_E_RESOURCES_INVALIDATED</span><span class="sxs-lookup"><span data-stu-id="ef9fd-110">AUDCLNT_E_RESOURCES_INVALIDATED</span></span>
- <span data-ttu-id="ef9fd-111">AUDCLNT_E_UNSUPPORTED_FORMAT</span><span class="sxs-lookup"><span data-stu-id="ef9fd-111">AUDCLNT_E_UNSUPPORTED_FORMAT</span></span>
- <span data-ttu-id="ef9fd-112">SPTLAUDCLNT_E_INTERNAL</span><span class="sxs-lookup"><span data-stu-id="ef9fd-112">SPTLAUDCLNT_E_INTERNAL</span></span>

## <a name="strategies-for-handling-invalid-device-errors"></a><span data-ttu-id="ef9fd-113">Strategien für die Behandlung von Fehlern bei ungültigen Geräten</span><span class="sxs-lookup"><span data-stu-id="ef9fd-113">Strategies for handling invalid-device errors</span></span>

<span data-ttu-id="ef9fd-114">Die empfohlene Strategie für die Wiederherstellung nach einem Fehler aufgrund eines ungültigen Geräts hängt davon ab, ob die Anwendung automatisch ein bestimmtes Gerät basierend auf internen Anforderungen auswählt oder ob der Benutzer ein Gerät explizit aus einer Liste der verfügbaren Geräte auswählen kann.</span><span class="sxs-lookup"><span data-stu-id="ef9fd-114">The recommended strategy for recovering from an invalid-device error depends on whether the application automatically selects a specific device based on internal requirements or it allows the user to explicitly select a device from a list of available devices.</span></span> 

### <a name="default-audio-device"></a><span data-ttu-id="ef9fd-115">Standardaudiogerät</span><span class="sxs-lookup"><span data-stu-id="ef9fd-115">Default audio device</span></span>

<span data-ttu-id="ef9fd-116">Wenn die Anwendung automatisch das Standardgerät auswählt, führen Sie die folgenden Schritte aus, um die Wiederherstellung auszuführen.</span><span class="sxs-lookup"><span data-stu-id="ef9fd-116">If the application automatically selects the default device, use the following steps to recover.</span></span>

1. <span data-ttu-id="ef9fd-117">Geben Sie die Schnittstelle [ispatialaudioobjectrenderstream](/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobjectrenderstream) und [ispatialaudioclient](/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) sowie alle anderen räumlichen Audioschnittstellen, die zum Rendern verwendet werden, frei.</span><span class="sxs-lookup"><span data-stu-id="ef9fd-117">Release the [ISpatialAudioObjectRenderStream](/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobjectrenderstream) and [ISpatialAudioClient](/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) interface and any other spatial audio interfaces that are used for rendering.</span></span> 
1. <span data-ttu-id="ef9fd-118">Bitten Sie [immdeviceenumerator:: getdefaultaudioendpoint](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) , um das aktuelle Standardaudiogerät abzurufen.</span><span class="sxs-lookup"><span data-stu-id="ef9fd-118">Call [IMMDeviceEnumerator::GetDefaultAudioEndpoint](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) to get the current default audio device.</span></span>
1. <span data-ttu-id="ef9fd-119">Versuchen Sie, **ispatialaudioclient** auf dem Audiogerät zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="ef9fd-119">Attempt to activate **ISpatialAudioClient** on the audio device.</span></span>
1. <span data-ttu-id="ef9fd-120">Aktivieren Sie **ispatialaudioobjectrenderstream**.</span><span class="sxs-lookup"><span data-stu-id="ef9fd-120">Activate **ISpatialAudioObjectRenderStream**.</span></span> 

### <a name="specifically-selected-audio-device"></a><span data-ttu-id="ef9fd-121">Speziell ausgewähltes Audiogerät</span><span class="sxs-lookup"><span data-stu-id="ef9fd-121">Specifically selected audio device</span></span>

<span data-ttu-id="ef9fd-122">Wenn die Anwendung ein bestimmtes Audiogerät auswählt, führen Sie die folgenden Schritte aus, um die Wiederherstellung auszuführen.</span><span class="sxs-lookup"><span data-stu-id="ef9fd-122">If the application selects a specific audio device, use the following steps to recover.</span></span>

1. <span data-ttu-id="ef9fd-123">Geben Sie die ispatialaudioobjectrenderstream-Schnittstelle und alle anderen räumlichen Audioschnittstellen, die zum Rendern verwendet werden, aber nicht " **ispatialaudioclient**" frei.</span><span class="sxs-lookup"><span data-stu-id="ef9fd-123">Release the ISpatialAudioObjectRenderStream interface and any other spatial audio interfaces that are used for rendering, but don't release **ISpatialAudioClient**.</span></span>
1. <span data-ttu-id="ef9fd-124">Verwenden Sie die aktuelle **ispatialaudioclient** -Instanz, um **ispatialaudioobjectrenderstream** zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="ef9fd-124">Use the current **ISpatialAudioClient** instance to activate **ISpatialAudioObjectRenderStream**.</span></span>

<span data-ttu-id="ef9fd-125">Beachten Sie, dass die gleichen Schritte für beide oben aufgeführten Strategien auf Anwendungen angewendet werden können, die die [ispatialaudioobjectrenderstreamformetadata](/windows/win32/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudioobjectrenderstreamformetadata) -Schnittstelle oder die [ispatialaudioobjectrenderstreamforhrtf](/windows/win32/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectrenderstreamforhrtf) -Schnittstelle verwenden.</span><span class="sxs-lookup"><span data-stu-id="ef9fd-125">Note that for both strategies listed above, the same steps can be applied to applications that use the [ISpatialAudioObjectRenderStreamForMetadata](/windows/win32/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudioobjectrenderstreamformetadata) or [ISpatialAudioObjectRenderStreamForHrtf](/windows/win32/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectrenderstreamforhrtf) interfaces.</span></span> <span data-ttu-id="ef9fd-126">Ersetzen Sie einfach **ispatialaudioobjectrenderstream** in den obigen Schritten durch die Metadaten oder die HRTF-Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="ef9fd-126">Simply replace **ISpatialAudioObjectRenderStream** in the above steps with the metadata or Hrtf interfaces.</span></span>


## <a name="related-topics"></a><span data-ttu-id="ef9fd-127">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ef9fd-127">Related topics</span></span>

<dl> <span data-ttu-id="ef9fd-128"><dt>Wieder 
[herstellen nach einem Invalid-Device Fehler](recovering-from-an-invalid-device-error.md) 
 Daten [Strom Verwaltung](stream-management.md)
</dt> </span><span class="sxs-lookup"><span data-stu-id="ef9fd-128"><dt>
[Recovering from an Invalid-Device Error](recovering-from-an-invalid-device-error.md)
[Stream Management](stream-management.md)
</dt> </span></span></dl>

 

 



