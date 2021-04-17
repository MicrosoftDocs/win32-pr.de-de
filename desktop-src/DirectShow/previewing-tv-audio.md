---
description: Vorschau der TV-Audiodatei
ms.assetid: 25da8bcc-51c1-49f0-b4b5-885ff4f254d8
title: Vorschau der TV-Audiodatei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1cc63583c946d47ed744eacd51f0939ec852d53
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481483"
---
# <a name="previewing-tv-audio"></a>Vorschau der TV-Audiodatei

Zum Anzeigen einer Vorschau der TV-Audiodaten leiten Sie die Audiodecoder-PIN auf dem Querbalken Filter an die audiotuner-Pin weiter. Zum stumm schalten der Audiodatei leiten Sie die PIN des Audiodecoders an-1 weiter, wie im folgenden Diagramm dargestellt. (Crossbar-Filter werden in [Arbeiten mit Kreuz leisten](working-with-crossbars.md)beschrieben.)

![Routing der Audiodecoder-PIN](images/vidcap07.png)

Die grundlegende Vorgehensweise sieht wie folgt aus:

1.  Verwenden Sie die [**ICaptureGraphBuilder2:: findinterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) -Methode, um den Querbalken Filter zu suchen.
2.  Verwenden Sie die [**iamcrossbar:: get \_ crossbarpininfo**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-get_crossbarpininfo) -Methode, um die Eingabe-und Ausgabe Pins des quer Zieh Filters aufzuzählen. Suchen Sie nach einem Audiodecoder-Ausgabepin und einer audiotuner-Eingabe-PIN.
3.  Wenn Sie die richtigen Pins gefunden haben, können Sie [**iamcrossbar:: Route**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-route) zum Weiterleiten der Pins anrufen. Wenn dies nicht der Grund ist, überprüfen Sie Upstream nach einer anderen quer Leiste, und wiederholen
4.  Zum stumm schalten der Audiodatei leiten Sie die PIN des Audiodecoders an-1 weiter.

Die meisten TV-Tuner verwenden einen einzelnen Querbalken Filter, einige verwenden jedoch zwei Kreuz leisten Filter. Daher müssen Sie möglicherweise nach einer zweiten quer Leiste suchen, wenn der erste Fehler auftritt.

> [!Note]  
> Im Gegensatz zu dem, was Sie möglicherweise erwartet haben, ist kein audioerfassungs Filter oder audiorenderer erforderlich, um eine Vorschau der Audiodatei anzuzeigen, da zwischen der gatewaykarte und der Soundkarte eine physische Verbindung besteht.

 

Der folgende Code zeigt diese Schritte ausführlicher. Im folgenden finden Sie eine Hilfsfunktion, die einen Querbalken Filter nach einem angegebenen Pin-Typ durchsucht:


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



Die Next-Funktion versucht, die Audiodatei zu aktivieren oder zu stumm schalten, abhängig vom Wert des *bactivate* -Parameters. Es durchsucht den angegebenen Querbalken Filter nach den erforderlichen Pins. Wenn Sie nicht gefunden werden kann, wird ein Fehlercode zurückgegeben.


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



Die Next-Funktion durchsucht das Filter Diagramm nach einem Querbalken Filter. Wenn ein solcher gefunden wird, versucht er, das Audiogerät zu aktivieren oder zu stumm schalten (mit der vorherigen Funktion). Wenn bei diesem Vorgang ein Fehler auftritt, durchsucht die Methode Upstream nach einer zweiten quer Leiste und versucht es erneut. Eine allgemeinere Methode zum Verwalten mehrerer Crossbar-Filter in einem Diagramm finden Sie in der ccrossbar-Klasse in der amcap-Beispielanwendung.


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



Der folgende Code zeigt, wie diese Funktionen aufgerufen werden:


```C++
// Build the analog TV graph (not shown).
// Activate the audio.
hr = ActivateAudio(pBuild, pCap, TRUE);
// Later, mute the audio.
hr = ActivateAudio(pBuild, pCap, FALSE);
```



Beachten Sie, dass diese Beispiel Funktionen viele der gleichen Funktionsaufrufe wiederholen. Sie zählen z. b. jedes Mal die Crossbar-Pins. In einer echten Anwendung können Sie einige dieser Informationen zwischenspeichern.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Analog zum Fernsehgerät](analog-television-audio.md)
</dt> <dt>

[Arbeiten mit quer leisten](working-with-crossbars.md)
</dt> </dl>

 

 



