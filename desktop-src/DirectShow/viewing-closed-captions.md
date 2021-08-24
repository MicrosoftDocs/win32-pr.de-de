---
description: Anzeigen von Untertiteln
ms.assetid: 86c0c553-af35-4ad1-8918-63d9e4577c73
title: Anzeigen von Untertiteln
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f52288b1c4fa5c43f7e0419d81bd9727a4db86848d368b600e1d713c53dc1593
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119903430"
---
# <a name="viewing-closed-captions"></a>Anzeigen von Untertiteln

Zur Unterstützung von Untertiteln im analogen Fernsehgerät macht der Erfassungsfilter eine Stecknadel verfügbar, die entweder VBI- oder Untertiteldaten liefert. Die Stecknadel hat eine der folgenden Pinkategorien:

-   VBI-Pin (PIN \_ CATEGORY \_ VBI). Stellt einen Stream von VBI-Wellenformbeispielen zur Verfügung. Diese werden an einen Decoderfilter übergeben, der die Untertiteldaten extrahiert.
-   CC-Pin (PIN \_ CATEGORY \_ CC). Liefert Bytepaare mit Untertiteln, die aus den Zeilen-21-Daten extrahiert wurden.
-   Hardwareslicing CC-Pin (PINNAME \_ VIDEO \_ CC \_ CAPTURE).

Um eine Vorschau von Untertiteln anzuzeigen, rufen Sie [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) mit der Kategorie VBI-Pin auf. Wenn dies fehlschlägt, rufen Sie es erneut mit der Kategorie CC auf.


```C++
hr = pBuild->RenderStream(&PIN_CATEGORY_VBI, 0, pCap, 0, 0);
if (FAILED(hr))
{
    hr = pBuild->RenderStream(&PIN_CATEGORY_CC, 0, pCap, 0, 0);
}
```



Das folgende Diagramm zeigt ein typisches Filterdiagramm zum Anzeigen von Untertiteln.

![Vorschaudiagramm für Untertitel](images/vidcap08.png)

In diesem Diagramm werden die folgenden Filter für die Anzeige von Untertiteln verwendet:

-   [Tee/Sink-to-Sink Converter](tee-sink-to-sink-converter.md). Akzeptiert die VBI-Informationen aus dem Erfassungsfilter und teilt sie für jeden datendienst, der im Signal vorhanden ist, in separate Datenströme auf. Microsoft stellt VBI-Codecs für Untertitel,TS und World Standard Teletext (WST) zur Verfügung.
-   [CC-Decoder](cc-decoder-filter.md). Decodiert CC-Daten aus den erfassten VBI-Waveforms, die vom Erfassungsfilter bereitgestellt werden.
-   [Zeile 21-Decoder](line-21-decoder-filter.md). Übersetzt die CC-Bytepaare und zeichnet den Beschriftungstext auf Bitmaps. Der Downstreamfilter (in diesem Fall der Overlay-Mixer) überlagert die Bitmaps auf dem Video.

Die RenderStream Graph Methode [](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) des Capture-Generators fügt diese Filter automatisch hinzu. Wenn der Erfassungsfilter über einen CC-Pin anstelle eines VBI-Pins verfügt, wird der CC-Pin direkt mit dem Filter Line 21 Decoder verbunden.

> [!Note]  
> Wenn Sie den Filter Video Mixing Renderer (VMR) für das Rendering verwenden, verwenden Sie den Filter 21-Decoder von Zeile 2. Dieser Filter verfügt über die gleiche Funktionalität wie der Line 21-Decoder, aber die CLSID ist CLSID \_ Line21Decoder2.

 

> [!Note]  
> Der CC-Decoderfilter wurde in Windows Vista entfernt. Neue Anwendungen sollten den Filter VBICodec verwenden, der in der Dokumentation zu Microsoft TV Technologies dokumentiert ist.

 

Wenn das Erfassungsgerät einen Videoport verwendet, verfügt der Erfassungsfilter möglicherweise über einen Videoport-VBI-Pin (PIN \_ CATEGORY \_ VIDEOPORT \_ VBI). Dieser Pin muss mit dem VBI Surface [Allocator-Filter](vbi-surface-allocator.md) verbunden sein, der Oberflächen zuordnt, die die erfassten VBI-Daten aufnehmen. Die [**RenderStream-Methode**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) fügt diesen Filter hinzu, wenn er erforderlich ist. Das folgende Diagramm zeigt ein Filterdiagramm mit der VBI-Oberflächenzuweisung.

![Vorschaudiagramm mit Untertiteln mit vbi-Oberflächenbeschriftung](images/vidcap09.png)

### <a name="enabling-and-disabling-the-captions"></a>Aktivieren und Deaktivieren der Untertitel

Verwenden Sie zum Steuern der Beschriftungsanzeige die [**IAMLine21Decoder-Schnittstelle**](/previous-versions/windows/desktop/api/il21dec/nn-il21dec-iamline21decoder) im Filter Line 21-Decoder. Beispielsweise können Sie die Beschriftungsanzeige wie folgt mithilfe der [**IAMLine21Decoder::SetServiceState-Methode**](/previous-versions/windows/desktop/api/il21dec/nf-il21dec-iamline21decoder-setservicestate) deaktivieren:


```C++
// Use the FindInterface method to find the interface.
IAMLine21Decoder *pLine21 = NULL;
hr = pBuild->FindInterface(
    &LOOK_DOWNSTREAM_ONLY, // Look downstream from pCap 
    NULL,                  // No particular media type
    pCap,                  // Pointer to the capture filter.
    IID_IAMLine21Decoder, (void**)&pLine21);
if (SUCCEEDED(hr))
{
    pLine21->SetServiceState(AM_L21_CCSTATE_Off);
    // (Use AM_L21_CCSTATE_On to enable.)
    pLine21->Release();
}
```



In diesem Beispiel wird die [**ICaptureGraphBuilder2::FindInterface-Methode**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) verwendet, um die [**IAMLine21Decoder-Schnittstelle zu**](/previous-versions/windows/desktop/api/il21dec/nn-il21dec-iamline21decoder) suchen. Der erste Parameter für **FindInterface** ist&**LOOK DOWNSTREAM \_ \_ ONLY,** der angibt, dass nach dem Erfassungsfilter *(pCap)* nachgeschaltet gesucht werden soll.

### <a name="capturing-closed-caption-bitmaps"></a>Erfassen von Untertitelbitmaps

Sie können die Beschriftungsbitmaps in einer Datei erfassen. Fügen Sie dazu den Abschnitt zum Schreiben von Dateien des Filterdiagramms hinzu, wie unter Erfassen von [Videos in einer Datei beschrieben.](capturing-video-to-a-file.md) Rendern Sie dann den CC- oder VBI-Pin im Muxfilter:


```C++
hr = pBuild->RenderStream(&PIN_CATEGORY_VBI, 0, pCap, 0, pMux);
if (FAILED(hr))
{
    hr = pBuild->RenderStream(&PIN_CATEGORY_CC, 0, pCap, 0, pMux);
}
```



Wenn Sie das Video auch erfassen, wird eine Datei mit zwei separaten Videostreams erstellt. Es werden keine Videos mit Untertiteln erfasst, die über dem Bild überlagert sind.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Untertitel und Teletext](closed-captions-and-teletext.md)
</dt> </dl>

 

 



