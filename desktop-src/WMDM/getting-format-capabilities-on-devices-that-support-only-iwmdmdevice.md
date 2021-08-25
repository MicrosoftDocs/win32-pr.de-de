---
title: Abrufen von Formatfunktionen über IWMDMDevice
description: Abrufen von Formatfunktionen auf Geräten, die nur IWMDMDevice unterstützen
ms.assetid: bff079a1-d192-4e53-9b1d-9ad3b5dcca51
keywords:
- Windows Medien Geräte-Manager, Gerätefunktionen
- Geräte-Manager,Gerätefunktionen
- Programmierhandbuch,Gerätefunktionen
- Desktopanwendungen, Gerätefunktionen
- Erstellen von Windows Media Geräte-Manager-Anwendungen, Gerätefunktionen
- Schreiben von Dateien auf Geräte, Gerätefunktionen
- IWMDMDevice-Methode
- Windows Media Geräte-Manager,IWMDMDevice-Methode
- Geräte-Manager,IWMDMDevice-Methode
- Programmierhandbuch,IWMDMDevice-Methode
- Desktopanwendungen, IWMDMDevice-Methode
- Erstellen Windows Media Geräte-Manager-Anwendungen, IWMDMDevice-Methode
- Schreiben von Dateien auf Geräte, IWMDMDevice-Methode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3fe71969b48ded5616ee34e90a3420a77f468dfd9fb7f2cf0c6d14168a6fbb2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119957524"
---
# <a name="getting-format-capabilities-through-iwmdmdevice"></a>Abrufen von Formatfunktionen über IWMDMDevice

Die empfohlene Methode zum Abfragen der Wiedergabefunktionen eines Geräts ist [**IWMDMDevice3::GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability). Wenn ein Gerät diese Methode jedoch nicht unterstützt, kann die Anwendung stattdessen [**IWMDMDevice::GetFormatSupport**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-getformatsupport) aufrufen, um ein Array unterstützter Audioformate als [**\_ WAVEFORMATEX-Strukturen**](-waveformatex.md) und MIME-Formate als Zeichenfolgen vom Gerät abzurufen.

Die folgenden Schritte zeigen, wie eine Anwendung diese Methode verwenden kann, um ein Gerät nach unterstützten Formaten abzufragen:

1.  Rufen **Sie GetFormatSupport** auf, um Arrays von Audio- und Mime-Formaten abzurufen.
2.  Durchlaufen Sie die abgerufenen Audioformate, und untersuchen Sie jede [**\_ WAVEFORMATEX-Struktur,**](-waveformatex.md) um ein akzeptables Audioformat zu finden.
3.  Durchlaufen Sie die abgerufenen MIME-Formatzeichenfolgen (falls gewünscht), um einen akzeptablen Dateityp zu finden. Das SDK definiert keine Konstanten für MIME-Formate. Sie sollten Branchenstandardwerte verwenden (die Sie auf der website iana.org finden). Ein Gerät sollte die spezifischen MIME-Typen auflisten, die es unterstützt.

Der folgende C++-Code veranschaulicht das Abrufen von Formatfunktionen von einem Gerät mithilfe von **GetFormatSupport.**


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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Ermitteln von Geräteformatfunktionen**](discovering-device-format-capabilities.md)
</dt> <dt>

[**Abrufen von Formatfunktionen auf Geräten, die IWMDMDevice3 unterstützen**](getting-format-capabilities-on-devices-that-support-iwmdmdevice3.md)
</dt> </dl>

 

 




