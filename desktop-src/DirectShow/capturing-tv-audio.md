---
description: TV-Audiodatei
ms.assetid: c0c62a8e-ab16-4617-936c-b64e6e3865b4
title: TV-Audiodatei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 138ce631aedf12ddfb52be92d08ffb47da0cbdec
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106344791"
---
# <a name="capturing-tv-audio"></a>TV-Audiodatei

Verwenden Sie den [audioerfassungs Filter](audio-capture-filter.md), um Audiodaten aus dem analogen Fernsehgerät in einer Datei zu erfassen. Verwenden Sie den Enumerator "System Geräte", um den audioerfassungs Filter zu erstellen. Es gibt möglicherweise mehrere audioerfassungs Geräte auf dem System des Benutzers. der Benutzer muss das Gerät auswählen, das die Soundkarte darstellt.

Verbinden Sie die Ausgabe-PIN der Audioerfassung mit dem MUX-Filter:


```C++
hr = pBuild->RenderStream(
   &PIN_CATEGORY_CAPTURE, // Capture pin.
   &MEDIATYPE_Audio,      // Audio media type.
   pAudioCap,             // Pointer to the audio capture filter.
   NULL,                  // Optional audio compressor filter.
   pMux);                 // Pointer to the mux filter.
```



Die Eingabe Pins müssen mit nichts verbunden sein. Jede Eingabe-PIN stellt eine physische Eingabe auf dem audioerfassungs Gerät dar. Verwenden Sie die [**IAMAudioInputMixer**](/windows/desktop/api/Strmif/nn-strmif-iamaudioinputmixer) -Schnittstelle, um die Eingabe zu aktivieren, die den Audiostream vom Tuner empfängt. Die Eingabe Pins werden anhand des Namens identifiziert, z. b. "Zeile in" oder "CD-Audiodatei". Leider können sich die Namen von einem Gerät zur nächsten ändern. Außerdem verwenden verschiedene TV-Tuner-Karten andere Eingaben für die Soundkarte. Daher ist es dem Benutzer zu entnehmen, welche Eingabe verwendet werden soll.


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

[Analog zum Fernsehgerät](analog-television-audio.md)
</dt> <dt>

[Audioerfassung](audio-capture.md)
</dt> </dl>

 

 



