---
description: Vorschau von TV-Audio
ms.assetid: 25da8bcc-51c1-49f0-b4b5-885ff4f254d8
title: Vorschau von TV-Audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e6b67e33ffd6f051363e8851afbc31b9f38bed17790687db615b679f6a80a63
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119748314"
---
# <a name="previewing-tv-audio"></a>Vorschau von TV-Audio

Um eine Vorschau von TV-Audio anzuzeigen, routen Sie den Audiodecoder-Pin am Kreuzleistenfilter an den Audio tuner-Pin. Um das Audio zu stummschalten, routen Sie den Audiodecoder-Pin an -1, wie im folgenden Diagramm dargestellt. (Kreuzleistenfilter werden unter [Arbeiten mit Übergreifenden Leisten beschrieben.)](working-with-crossbars.md)

![Weiterleiten des Audiodecoder-Pins](images/vidcap07.png)

Der grundlegende Ansatz lautet wie folgt:

1.  Verwenden Sie [**die ICaptureGraphBuilder2::FindInterface-Methode,**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) um den Kreuzleistenfilter zu suchen.
2.  Verwenden Sie [**die IAMCrossbar::get \_ CrossbarPinInfo-Methode,**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-get_crossbarpininfo) um die Eingabe- und Ausgabepins des Kreuzleistenfilters zu aufzählen. Suchen Sie nach einem Audiodecoder-Ausgabepin und einem Audio-Tuner-Eingabepin.
3.  Wenn Sie die richtigen Stecknadeln finden, rufen Sie [**IAMCrossbar::Route auf,**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-route) um die Stecknadeln weiter zu routen. Falls nicht, suchen Sie upstream nach einer anderen Querleiste, und wiederholen Sie den Vorgang.
4.  Um das Audio zu stummschalten, routen Sie den Audiodecoder-Pin an -1.

Die meisten TV-Tuner verwenden einen einzelnen Kreuzleistenfilter, aber einige verwenden zwei Kreuzleistenfilter. Daher müssen Sie möglicherweise nach einer zweiten Querleiste suchen, wenn die erste fehlschlägt.

> [!Note]  
> Im Gegensatz zu dem, was Sie erwarten, ist kein Audioaufnahmefilter oder Audiorenderer erforderlich, um die Audiovorschau anzuzeigen, da eine physische Verbindung zwischen der Tunerkarte und der Soundkarte besteht.

 

Im folgenden Code werden diese Schritte ausführlicher dargestellt. Zunächst sehen Sie hier eine Hilfsfunktion, die einen Kreuzleistenfilter nach einem angegebenen Stecknadeltyp durchsucht:


```C++
HRESULT FindCrossbarPin(
    IAMCrossbar *pXBar,                 // Pointer to the crossbar.
    PhysicalConnectorType PhysicalType, // Pin type to match.
    PIN_DIRECTION Dir,                  // Pin direction.
    long *pIndex)       // Receives the index of the pin, if found.
{
    BOOL bInput = (Dir == PINDIR_INPUT ? TRUE : FALSE);

    // Find out how many pins the crossbar has.
    long cOut, cIn;
    HRESULT hr = pXBar->get_PinCounts(&cOut, &cIn);
    if (FAILED(hr)) return hr;
    // Enumerate pins and look for a matching pin.
    long count = (bInput ? cIn : cOut);
    for (long i = 0; i < count; i++)
    {
        long iRelated = 0;
        long ThisPhysicalType = 0;
        hr = pXBar->get_CrossbarPinInfo(bInput, i, &iRelated,
            &ThisPhysicalType);
        if (SUCCEEDED(hr) && ThisPhysicalType == PhysicalType)
        {
            // Found a match, return the index.
            *pIndex = i;
            return S_OK;
        }
    }
    // Did not find a matching pin.
    return E_FAIL;
}
```



Die nächste Funktion versucht, die Audiodaten abhängig vom Wert des *bActivate-Parameters zu* aktivieren oder zu stummschalten. Er durchsucht den angegebenen Kreuzleistenfilter nach den erforderlichen Stecknadeln. Wenn sie nicht finden können, wird ein Fehlercode zurückgegeben.


```C++
HRESULT ConnectAudio(IAMCrossbar *pXBar, BOOL bActivate)
{
    // Look for the Audio Decoder output pin.
    long i = 0;
    HRESULT hr = FindCrossbarPin(pXBar, PhysConn_Audio_AudioDecoder,
        PINDIR_OUTPUT, &i);
    if (SUCCEEDED(hr))
    {
        if (bActivate)  // Activate the audio. 
        {
            // Look for the Audio Tuner input pin.
            long j = 0;
            hr = FindCrossbarPin(pXBar, PhysConn_Audio_Tuner, 
                PINDIR_INPUT, &j);
            if (SUCCEEDED(hr))
            {
                return pXBar->Route(i, j);
            }
        }
        else  // Mute the audio
        {
            return pXBar->Route(i, -1);
        }
    }
    return E_FAIL;
}
```



Die nächste Funktion durchsucht das Filterdiagramm nach einem Kreuzleistenfilter. Wenn ein Audio gefunden wird, wird versucht, die Audiodatei zu aktivieren oder zu stummschalten (mithilfe der vorherigen Funktion). Wenn dieser Vorgang fehlschlägt, durchsucht die Methode upstream nach einer zweiten Querleiste und versucht es erneut. Einen allgemeineren Ansatz zum Verwalten mehrerer Kreuzleistenfilter in einem Diagramm finden Sie in der CCrossbar-Klasse in der AmCap-Beispielanwendung.


```C++
HRESULT ActivateAudio(ICaptureGraphBuilder2 *pBuild, IBaseFilter *pSrc,
  BOOL bActivate)
{
    // Search upstream for a crossbar.
    IAMCrossbar *pXBar1 = NULL;
    HRESULT hr = pBuild->FindInterface(&LOOK_UPSTREAM_ONLY, NULL, pSrc,
        IID_IAMCrossbar, (void**)&pXBar1);
    if (SUCCEEDED(hr)) 
    {
        hr = ConnectAudio(pXBar1, bActivate);
        if (FAILED(hr))
        {
            // Look for another crossbar.
            IBaseFilter *pF = NULL;
            hr = pXBar1->QueryInterface(IID_IBaseFilter, (void**)&pF);
            if (SUCCEEDED(hr)) 
            {
                // Search upstream for another one.
                IAMCrossbar *pXBar2 = NULL;
                hr = pBuild->FindInterface(&LOOK_UPSTREAM_ONLY, NULL, pF,
                    IID_IAMCrossbar, (void**)&pXBar2);
                pF->Release();
                if (SUCCEEDED(hr))
                {
                    hr = ConnectAudio(pXBar2, bActivate);
                    pXBar2->Release();
                }
            }
        }
        pXBar1->Release();
    }
    return hr;
}
```



Der folgende Code zeigt, wie sie diese Funktionen aufrufen:


```C++
// Build the analog TV graph (not shown).
// Activate the audio.
hr = ActivateAudio(pBuild, pCap, TRUE);
// Later, mute the audio.
hr = ActivateAudio(pBuild, pCap, FALSE);
```



Beachten Sie, dass diese Beispielfunktionen viele der gleichen Funktionsaufrufe wiederholen. Beispielsweise werden die Leistenpins jedes Mal aufzählt. In einer echten Anwendung können Sie einige dieser Informationen zwischenspeichern.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Analoge Fernsehaudiodaten](analog-television-audio.md)
</dt> <dt>

[Arbeiten mit Übergreifenden Leisten](working-with-crossbars.md)
</dt> </dl>

 

 



