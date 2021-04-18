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
# <a name="capturing-tv-audio"></a><span data-ttu-id="a08c0-103">TV-Audiodatei</span><span class="sxs-lookup"><span data-stu-id="a08c0-103">Capturing TV Audio</span></span>

<span data-ttu-id="a08c0-104">Verwenden Sie den [audioerfassungs Filter](audio-capture-filter.md), um Audiodaten aus dem analogen Fernsehgerät in einer Datei zu erfassen.</span><span class="sxs-lookup"><span data-stu-id="a08c0-104">To capture audio from analog television to a file, use the [Audio Capture Filter](audio-capture-filter.md).</span></span> <span data-ttu-id="a08c0-105">Verwenden Sie den Enumerator "System Geräte", um den audioerfassungs Filter zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="a08c0-105">Use the System Device Enumerator to create the Audio Capture Filter.</span></span> <span data-ttu-id="a08c0-106">Es gibt möglicherweise mehrere audioerfassungs Geräte auf dem System des Benutzers. der Benutzer muss das Gerät auswählen, das die Soundkarte darstellt.</span><span class="sxs-lookup"><span data-stu-id="a08c0-106">There may be several audio capture devices on the user's system; the user must select the device that represents the sound card.</span></span>

<span data-ttu-id="a08c0-107">Verbinden Sie die Ausgabe-PIN der Audioerfassung mit dem MUX-Filter:</span><span class="sxs-lookup"><span data-stu-id="a08c0-107">Connect the audio capture output pin to the mux filter:</span></span>


```C++
hr = pBuild->RenderStream(
   &PIN_CATEGORY_CAPTURE, // Capture pin.
   &MEDIATYPE_Audio,      // Audio media type.
   pAudioCap,             // Pointer to the audio capture filter.
   NULL,                  // Optional audio compressor filter.
   pMux);                 // Pointer to the mux filter.
```



<span data-ttu-id="a08c0-108">Die Eingabe Pins müssen mit nichts verbunden sein.</span><span class="sxs-lookup"><span data-stu-id="a08c0-108">The input pins do not have to be connected to anything.</span></span> <span data-ttu-id="a08c0-109">Jede Eingabe-PIN stellt eine physische Eingabe auf dem audioerfassungs Gerät dar.</span><span class="sxs-lookup"><span data-stu-id="a08c0-109">Each input pin represents a physical input on the audio capture device.</span></span> <span data-ttu-id="a08c0-110">Verwenden Sie die [**IAMAudioInputMixer**](/windows/desktop/api/Strmif/nn-strmif-iamaudioinputmixer) -Schnittstelle, um die Eingabe zu aktivieren, die den Audiostream vom Tuner empfängt.</span><span class="sxs-lookup"><span data-stu-id="a08c0-110">Use the [**IAMAudioInputMixer**](/windows/desktop/api/Strmif/nn-strmif-iamaudioinputmixer) interface to enable the input that receives the audio stream from the tuner.</span></span> <span data-ttu-id="a08c0-111">Die Eingabe Pins werden anhand des Namens identifiziert, z. b. "Zeile in" oder "CD-Audiodatei".</span><span class="sxs-lookup"><span data-stu-id="a08c0-111">The input pins are identified by name, such as "Line In" or "CD Audio."</span></span> <span data-ttu-id="a08c0-112">Leider können sich die Namen von einem Gerät zur nächsten ändern.</span><span class="sxs-lookup"><span data-stu-id="a08c0-112">Unfortunately, the names can change from one device to the next.</span></span> <span data-ttu-id="a08c0-113">Außerdem verwenden verschiedene TV-Tuner-Karten andere Eingaben für die Soundkarte.</span><span class="sxs-lookup"><span data-stu-id="a08c0-113">Also, different TV tuner cards use different inputs to the sound card.</span></span> <span data-ttu-id="a08c0-114">Daher ist es dem Benutzer zu entnehmen, welche Eingabe verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a08c0-114">Therefore, it is up to the user to identify which input to use.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="a08c0-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a08c0-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a08c0-116">Analog zum Fernsehgerät</span><span class="sxs-lookup"><span data-stu-id="a08c0-116">Analog Television Audio</span></span>](analog-television-audio.md)
</dt> <dt>

[<span data-ttu-id="a08c0-117">Audioerfassung</span><span class="sxs-lookup"><span data-stu-id="a08c0-117">Audio Capture</span></span>](audio-capture.md)
</dt> </dl>

 

 



