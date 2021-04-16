---
description: Anzeigen von Untertiteln
ms.assetid: 86c0c553-af35-4ad1-8918-63d9e4577c73
title: Anzeigen von Untertiteln
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82ff2d6d213259ccce6e9b02272d0c9db3ad7b71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104571083"
---
# <a name="viewing-closed-captions"></a>Anzeigen von Untertiteln

Zur Unterstützung von Untertiteln im analogen Fernsehen macht der Erfassungs Filter eine PIN verfügbar, die entweder VBI-oder Closed Caption-Daten bereitstellt. Die PIN weist eine der folgenden Pin-Kategorien auf:

-   VBI-PIN (PIN- \_ Kategorie \_ VBI). Bietet einen Stream von VBI-Wellenform-Beispielen. Diese werden an einen Decoderfilter übermittelt, der die Untertitel Daten extrahiert.
-   CC-PIN (PIN- \_ Kategorie \_ CC). Übermittelt aus den Zeilen 21 Daten extrahierte Byte-Paare mit geschlossener Beschriftung.
-   Hardware aufteilen CC-PIN (Pinname \_ Video \_ CC \_ Capture).

Um Untertitel in der Vorschau anzuzeigen, nennen Sie [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) mit der VBI-Pin-Kategorie, und wenn dies nicht der Fall ist, nennen Sie es erneut mit der Kategorie cc.


```C++
hr = pBuild->RenderStream(&PIN_CATEGORY_VBI, 0, pCap, 0, 0);
if (FAILED(hr))
{
    hr = pBuild->RenderStream(&PIN_CATEGORY_CC, 0, pCap, 0, 0);
}
```



Das folgende Diagramm zeigt ein typisches Filter Diagramm zum Anzeigen von Untertiteln.

![Vorschau Diagramm für Untertitel](images/vidcap08.png)

In diesem Diagramm werden die folgenden Filter für die Anzeige von Closed Caption verwendet:

-   [Tee/Sink-zu-Sink-Konverter](tee-sink-to-sink-converter.md). Akzeptiert die VBI-Informationen aus dem Erfassungs Filter und teilt Sie für jeden der Datendienste, die im Signal vorhanden sind, in separate Streams auf. Microsoft stellt VBI-Codecs für Closed Caption, nabts und World Standard Teletext (WST) zur Verfügung.
-   [CC-Decoder](cc-decoder-filter.md). Decodiert cc-Daten aus den vom Erfassungs Filter bereitgestellten VBI-Wellen Formularen.
-   [Zeile 21-Decoder](line-21-decoder-filter.md). Übersetzt die CC-Byte-Paare und zeichnet den Beschriftungs Text auf Bitmaps. Der Downstream-Filter (in diesem Fall der Überlagerungs-Mixer) überlagert die Bitmaps auf dem Video.

Die [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) -Methode des Capture Graph-Generators fügt diese Filter automatisch hinzu. Wenn der Erfassungs Filter über eine CC-Pin anstelle einer VBI-Pin verfügt, wird die CC-Pin direkt mit dem-Decoderfilter für die Linie 21 verbunden.

> [!Note]  
> Wenn Sie den Filter für Video Mischungs-Renderer (VMR) zum Rendern verwenden, verwenden Sie den Codierer-Filter 2. Dieser Filter verfügt über die gleiche Funktionalität wie der Line 21-Decoder, aber die CLSID ist CLSID \_ Line21Decoder2.

 

> [!Note]  
> Der CC-Decoderfilter wurde in Windows Vista entfernt. Neue Anwendungen sollten den vbicodec-Filter verwenden, der in der Dokumentation zu Microsoft TV-Technologien dokumentiert ist.

 

Wenn das Erfassungsgerät einen Videoport verwendet, hat der Erfassungs Filter möglicherweise eine Video Port-VBI-PIN (PIN- \_ Kategorie \_ Videoport \_ VBI). Diese PIN muss mit dem [VBI-Oberflächen zuordnerfilter](vbi-surface-allocator.md) verbunden werden, der die erfassten VBI-Daten mithilfe von Oberflächen zuordnet. Die [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) -Methode fügt diesen Filter hinzu, wenn dies erforderlich ist. Das folgende Diagramm zeigt ein Filter Diagramm mit der VBI-Oberflächen Zuweisung.

![Untertitel des Vorschau Diagramms mit VBI Surface-Zuweisung](images/vidcap09.png)

### <a name="enabling-and-disabling-the-captions"></a>Aktivieren und Deaktivieren der Beschriftungen

Um die Untertitelanzeige zu steuern, verwenden Sie die [**IAMLine21Decoder**](/previous-versions/windows/desktop/api/il21dec/nn-il21dec-iamline21decoder) -Schnittstelle im Decoder-Filter für Linien 21. Beispielsweise können Sie die Beschriftungs Anzeige mithilfe der [**IAMLine21Decoder:: SetServiceState**](/previous-versions/windows/desktop/api/il21dec/nf-il21dec-iamline21decoder-setservicestate) -Methode wie folgt deaktivieren:


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



In diesem Beispiel wird die [**ICaptureGraphBuilder2:: findinterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) -Methode verwendet, um die [**IAMLine21Decoder**](/previous-versions/windows/desktop/api/il21dec/nn-il21dec-iamline21decoder) -Schnittstelle zu suchen. Der erste Parameter für die **findinterface-Schnittstelle** ist **&\_ \_ nur** downstreamwert, der angibt, dass Downstream aus dem Erfassungs Filter (*pcap*) gesucht werden soll.

### <a name="capturing-closed-caption-bitmaps"></a>Erfassen von Bitmaps für geschlossene Beschriftungen

Sie können die Beschriftungs Bitmaps in einer Datei erfassen. Fügen Sie hierzu den Abschnitt zum Schreiben von Dateien des Filter Diagramms hinzu, wie unter [Erfassen von Videos in einer Datei](capturing-video-to-a-file.md)beschrieben. Anschließend können Sie die CC-oder VBI-PIN mit dem MUX-Filter Rendering:


```C++
hr = pBuild->RenderStream(&PIN_CATEGORY_VBI, 0, pCap, 0, pMux);
if (FAILED(hr))
{
    hr = pBuild->RenderStream(&PIN_CATEGORY_CC, 0, pCap, 0, pMux);
}
```



Wenn Sie auch das Video erfassen, wird eine Datei mit zwei separaten Videostreams erstellt. Videos mit Beschriftungen, die oberhalb des Bilds überlagert sind, werden nicht erfasst.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Untertitel und Teletext](closed-captions-and-teletext.md)
</dt> </dl>

 

 



