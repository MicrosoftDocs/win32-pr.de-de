---
description: Aufzeichnen von TV-Audio
ms.assetid: c0c62a8e-ab16-4617-936c-b64e6e3865b4
title: Aufzeichnen von TV-Audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d699533480bdeaaa528e362c0773e9df8100fda3dc2195a65c055ae7f7d5bb1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119641010"
---
# <a name="capturing-tv-audio"></a>Aufzeichnen von TV-Audio

Verwenden Sie den [Audioaufnahmefilter](audio-capture-filter.md), um Audiodaten von analogem Fernsehgerät in einer Datei zu erfassen. Verwenden Sie den Systemgeräte-Enumerator, um den Audioaufnahmefilter zu erstellen. Es können mehrere Audioaufnahmegeräte auf dem System des Benutzers vorhanden sein. der Benutzer muss das Gerät auswählen, das die Soundkarte darstellt.

Verbinden den Audioaufnahme-Ausgabepin an den Mux-Filter an:


```C++
hr = pBuild->RenderStream(
   &PIN_CATEGORY_CAPTURE, // Capture pin.
   &MEDIATYPE_Audio,      // Audio media type.
   pAudioCap,             // Pointer to the audio capture filter.
   NULL,                  // Optional audio compressor filter.
   pMux);                 // Pointer to the mux filter.
```



Die Eingabepins müssen nicht mit etwas verbunden werden. Jeder Eingabepin stellt eine physische Eingabe auf dem Audioaufnahmegerät dar. Verwenden Sie die [**IAMAudioInputMixer-Schnittstelle,**](/windows/desktop/api/Strmif/nn-strmif-iamaudioinputmixer) um die Eingabe zu aktivieren, die den Audiostream vom Tuner empfängt. Die Eingabepins werden anhand des Namens identifiziert, z. B. "Line In" oder "CD Audio". Leider können sich die Namen von einem Gerät zum nächsten ändern. Außerdem verwenden verschiedene TV-Tunerkarten unterschiedliche Eingaben für die Soundkarte. Daher muss der Benutzer selbst bestimmen, welche Eingabe verwendet werden soll.


```C++
IEnumPins *pEnum = NULL;
hr = pAudioCap->EnumPins(&pEnum);
if (SUCCEEDED(hr))
{
    IPin *pPin = NULL;
    while (S_OK == pEnum->Next(1, &pPin, NULL))
    {
        IAMAudioInputMixer *pMix;
        hr = pPin->QueryInterface(IID_IAMAudioInputMixer, (void**)&pMix);
        if (SUCCEEDED(hr))
        {
            // Use IPin::QueryPinInfo to get the pin name.
            pPin->Release();
            if (...) // If the user selects this pin:
            {
                pMix->put_Enable(TRUE);
                pMix->put_MixLevel(1.0);
                pMix->Release();
                break;
            }
            pMix->Release();
        }
    }
}
pEnum->Release();
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Analoge Fernsehaudio](analog-television-audio.md)
</dt> <dt>

[Audioaufnahme](audio-capture.md)
</dt> </dl>

 

 



