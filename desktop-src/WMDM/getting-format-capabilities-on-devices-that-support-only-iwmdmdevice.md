---
title: Erhalten von Formatfunktionen mithilfe von iwmdmdevice
description: Erhalten von Format Funktionen auf Geräten, die nur iwmdmdevice unterstützen
ms.assetid: bff079a1-d192-4e53-9b1d-9ad3b5dcca51
keywords:
- Windows Media Device Manager, Gerätefunktionen
- Device Manager, Gerätefunktionen
- Programmier Handbuch, Gerätefunktionen
- Desktop Anwendungen, Gerätefunktionen
- Erstellen von Windows Media Device Manager-Anwendungen, Gerätefunktionen
- Schreiben von Dateien auf Geräte, Gerätefunktionen
- Iwmdmdevice-Methode
- Windows Media Device Manager, iwmdmdevice-Methode
- Device Manager, iwmdmdevice-Methode
- Programmier Handbuch, iwmdmdevice-Methode
- Desktop Anwendungen, iwmdmdevice-Methode
- Erstellen von Windows Media Device Manager-Anwendungen, iwmdmdevice-Methode
- Schreiben von Dateien auf Geräte, iwmdmdevice-Methode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a923919611b40197b1deed30e781042e008ef41
ms.sourcegitcommit: b95a94ffffda33f9ebbdd41787c01866444b4cf4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/27/2019
ms.locfileid: "104313847"
---
# <a name="getting-format-capabilities-through-iwmdmdevice"></a><span data-ttu-id="c753b-116">Erhalten von Formatfunktionen mithilfe von iwmdmdevice</span><span class="sxs-lookup"><span data-stu-id="c753b-116">Getting format capabilities through IWMDMDevice</span></span>

<span data-ttu-id="c753b-117">Die empfohlene Methode zum Abfragen eines Geräts für die Wiedergabe Funktionen ist [**IWMDMDevice3:: getformatcapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability).</span><span class="sxs-lookup"><span data-stu-id="c753b-117">The recommended method for querying a device for its playback capabilities is [**IWMDMDevice3::GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability).</span></span> <span data-ttu-id="c753b-118">Wenn ein Gerät diese Methode jedoch nicht unterstützt, kann die Anwendung stattdessen [**iwmdmdevice:: getformatsupport**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-getformatsupport) aufrufen, um ein Array unterstützter Audioformate als [**\_ Wellen FORMATEX**](-waveformatex.md) -Strukturen und MIME-Formate als Zeichen folgen vom Gerät abzurufen.</span><span class="sxs-lookup"><span data-stu-id="c753b-118">However, if a device does not support this method, the application instead can call [**IWMDMDevice::GetFormatSupport**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-getformatsupport) to retrieve an array of supported audio formats as [**\_WAVEFORMATEX**](-waveformatex.md) structures and MIME formats as strings from the device.</span></span>

<span data-ttu-id="c753b-119">Die folgenden Schritte zeigen, wie eine Anwendung diese Methode verwenden kann, um ein Gerät nach unterstützten Formaten abzufragen:</span><span class="sxs-lookup"><span data-stu-id="c753b-119">The following steps show how an application can use this method to query a device for supported formats:</span></span>

1.  <span data-ttu-id="c753b-120">Rufen Sie **getformatsupport** auf, um Arrays aus Audioformaten und MIME-Formaten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="c753b-120">Call **GetFormatSupport** to retrieve arrays of both audio and mime formats.</span></span>
2.  <span data-ttu-id="c753b-121">Durchlaufen Sie die abgerufenen Audioformate, und untersuchen Sie jede [**\_ WaveFormatEx**](-waveformatex.md) -Struktur, um ein akzeptables Audioformat zu finden.</span><span class="sxs-lookup"><span data-stu-id="c753b-121">Loop through the retrieved audio formats and examine each [**\_WAVEFORMATEX**](-waveformatex.md) structure to try to find an acceptable audio format</span></span>
3.  <span data-ttu-id="c753b-122">Durchlaufen Sie ggf. die abgerufenen MIME-Format Zeichenfolgen, um einen akzeptablen Dateityp zu suchen.</span><span class="sxs-lookup"><span data-stu-id="c753b-122">Loop through the retrieved MIME format strings (if desired) to find an acceptable file type.</span></span> <span data-ttu-id="c753b-123">Das SDK definiert keine Konstanten für MIME-Formate. Sie sollten die Industriestandard Werte verwenden (die sich auf der IANA.org-Website befinden).</span><span class="sxs-lookup"><span data-stu-id="c753b-123">The SDK does not define constants for MIME formats; you should use industry standard values (which can be found at the iana.org Web site).</span></span> <span data-ttu-id="c753b-124">Ein Gerät sollte die spezifischen MIME-Typen auflisten, die es unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c753b-124">A device should list the specific MIME types that it supports.</span></span>

<span data-ttu-id="c753b-125">Der folgende C++-Code veranschaulicht das Abrufen von Formatfunktionen von einem Gerät mithilfe von **getformatsupport**.</span><span class="sxs-lookup"><span data-stu-id="c753b-125">The following C++ code demonstrates retrieving format capabilities from a device, using **GetFormatSupport**.</span></span>


```C++
// Function to print out device caps for a device 
// that supports only IWMDMDevice.
void CWMDMController::GetCaps(IWMDMDevice* pDevice)
{
    HRESULT hr = S_OK;

    // Get all capabilities for audio and mime support.
    _WAVEFORMATEX* pAudioFormats;
    LPWSTR* pMimeFormats;
    UINT numAudioFormats = 0;
    UINT numMimeFormats = 0;
    hr = pDevice->GetFormatSupport(
        &pAudioFormats,
        &numAudioFormats,
        &pMimeFormats,
        &numMimeFormats);
    if (FAILED(hr)) return;

    // Print out audio format data.
    if (numAudioFormats > 0)
    {
        // TODO: Display a banner for the supported audio-format listing.
    }
    else
    {
        // TODO: Display a message indicating that no audio formats are supported.
    }
    for (int i = 0; i < numAudioFormats; i++)
    {
       // TODO: For each valid audio format, display the max channel, 
       // max samples/second, avg. bytes/sec, block alignment, and 
       // max bits/sample values.
    }

    // Print out MIME formats.
    if (numMimeFormats > 0)
        // TODO: Display a banner to precede the MIME format listing.
    else
        // TODO: Display a banner indicating that no MIME formats are supported.
    for (i = 0; i < numMimeFormats; i++)
    {
        // TODO: Display the specified MIME format.
    }
    return;
}
```



## <a name="related-topics"></a><span data-ttu-id="c753b-126">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c753b-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c753b-127">**Ermitteln der Funktionen des Geräte Formats**</span><span class="sxs-lookup"><span data-stu-id="c753b-127">**Discovering Device Format Capabilities**</span></span>](discovering-device-format-capabilities.md)
</dt> <dt>

[<span data-ttu-id="c753b-128">**Erhalten von Format Funktionen auf Geräten, die IWMDMDevice3 unterstützen**</span><span class="sxs-lookup"><span data-stu-id="c753b-128">**Getting Format Capabilities on Devices That Support IWMDMDevice3**</span></span>](getting-format-capabilities-on-devices-that-support-iwmdmdevice3.md)
</dt> </dl>

 

 




