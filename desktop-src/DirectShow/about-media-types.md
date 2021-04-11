---
description: Informationen zu Medientypen
ms.assetid: 9984ba36-4e43-4886-a073-34b330274c9c
title: Informationen zu Medientypen (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3289a37e95bf5dbd1e5c277b5799a2c7c8c90586
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "104351229"
---
# <a name="about-media-types-directshow"></a>Informationen zu Medientypen (DirectShow)

Da DirectShow modular aufgebaut ist, ist es erforderlich, das Format der Daten an jedem Punkt im Filter Diagramm zu beschreiben. Nehmen Sie beispielsweise die AVI-Wiedergabe. Daten werden als Stream von Riff Blöcken in das Diagramm eingegeben. Diese werden in Video-und Audiodatenströme analysiert. Der Videostream besteht aus Video Frames, die wahrscheinlich komprimiert sind. Nach der Decodierung ist der Videostream eine Reihe von nicht komprimierten Bitmaps. Der Audiodatenstrom durchläuft einen ähnlichen Prozess.

Medientypen: Funktionsweise von DirectShow-Formaten

Der *Medientyp* ist eine universelle und erweiterbare Methode, um digitale Medienformate zu beschreiben. Wenn zwei Filter eine Verbindung herstellen, stimmen Sie einem Medientyp zu. Der Medientyp gibt an, welche Art von Daten der Upstream-Filter für den downstreamfilter bereitstellt, und das physische Layout der Daten. Wenn zwei Filter einem Medientyp nicht zustimmen können, wird keine Verbindung hergestellt.

Bei manchen Anwendungen müssen Sie sich keine Gedanken über die Medientypen machen. Bei der Wiedergabe von Dateien verarbeitet DirectShow beispielsweise alle Details. Andere Arten von Anwendungen müssen möglicherweise direkt mit Medientypen arbeiten.

Medientypen werden mithilfe der [**am- \_ \_ Medientyp**](/windows/win32/api/strmif/ns-strmif-am_media_type) Struktur definiert. Diese Struktur enthält die folgenden Informationen:

-   **Haupttyp**: der Haupttyp ist eine GUID, die die Gesamtkategorie der Daten definiert. Zu den Haupttypen zählen Video, Audiodaten, nicht analysierte Bytestream, MIDI-Daten usw.
-   **Untertyp**: der Untertyp ist eine andere GUID, die das Format weiter definiert. Im Video Haupttyp gibt es z. b. Untertypen für RGB-24, RGB-32, UYVY usw. In Audiodaten gibt es PCM-Audiodaten, MPEG-1-Nutzlast und andere. Der Untertyp bietet mehr Informationen als der Haupttyp, aber er definiert nicht alles über das Format. Beispielsweise definieren Video Untertypen nicht die Bildgröße oder die Framerate. Diese werden durch den unten beschriebenen Format Block definiert.
-   **Format Block**: der Format Block ist ein Datenblock, der das Format ausführlich beschreibt. Der Format Block wird getrennt von der [**am- \_ \_ Medientyp**](/windows/win32/api/strmif/ns-strmif-am_media_type) Struktur zugeordnet. Der **pbformat** -Member der **am \_ \_ Medientyp** -Struktur verweist auf den Format Block.

    Der **pbformat** -Member ist typisiert **void \** _, weil das Layout des Format Blocks abhängig vom Medientyp geändert wird. Beispielsweise verwendet PCM-Audiodaten eine [_ *WaveFormatEx* *](/previous-versions/dd757713(v=vs.85)) -Struktur. Video verwendet verschiedene Strukturen, einschließlich [**videoinfoheader**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) und [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2). Der **Format Type** -Member der [**am \_ \_ Medientyp**](/windows/win32/api/strmif/ns-strmif-am_media_type) -Struktur ist eine GUID, die angibt, welche Struktur im Format Block enthalten ist. Jeder Format Struktur wird eine GUID zugewiesen. Der **cbformat** -Member gibt die Größe des Format Blocks an. Überprüfen Sie diese Werte immer, bevor Sie den **pbformat** -Zeiger dereferenzieren.

Wenn der Format Block ausgefüllt ist, enthalten der Haupttyp und der Untertyp redundante Informationen. Der Haupttyp und der Untertyp stellen jedoch eine bequeme Möglichkeit zum Identifizieren von Formaten ohne einen kompletten Format Block dar. Sie können z. b. ein generisches 24-Bit-RGB-Format (mediasubtype \_ RGB24) angeben, ohne alle Informationen zu kennen, die für die [**videoinfoheader**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) -Struktur erforderlich sind, wie z. b. die Bildgröße und die Framerate.

Ein Filter kann z. b. den folgenden Code verwenden, um einen Medientyp zu überprüfen:


```C++
HRESULT CheckMediaType(AM_MEDIA_TYPE *pmt)
{
    if (pmt == NULL) return E_POINTER;

    // Check the major type. We're looking for video.
    if (pmt->majortype != MEDIATYPE_Video)
    {
        return VFW_E_INVALIDMEDIATYPE;
    }

    // Check the subtype. We're looking for 24-bit RGB.
    if (pmt->subtype != MEDIASUBTYPE_RGB24)
    {
        return VFW_E_INVALIDMEDIATYPE;
    }

    // Check the format type and the size of the format block.
    if ((pmt->formattype == FORMAT_VideoInfo) &&
         (pmt->cbFormat >= sizeof(VIDEOINFOHEADER) &&
         (pmt->pbFormat != NULL))
    {
        // Now it's safe to coerce the format block pointer to the
        // correct structure, as defined by the formattype GUID.
        VIDEOINFOHEADER *pVIH = (VIDEOINFOHEADER*)pmt->pbFormat;
    
        // Examine pVIH (not shown). If it looks OK, return S_OK.
        return S_OK;
    }

    return VFW_E_INVALIDMEDIATYPE;
}
```



Die [**am \_ \_ Medientyp**](/windows/win32/api/strmif/ns-strmif-am_media_type) -Struktur enthält auch einige optionale Felder. Diese können verwendet werden, um zusätzliche Informationen bereitzustellen, aber es sind keine Filter erforderlich, um Sie zu verwenden:

-   **lsamplesize**. Wenn dieses Feld ungleich 0 (null) ist, wird die Größe der einzelnen Stichproben definiert. Wenn Sie 0 (null) ist, gibt Sie an, dass sich die Stichprobengröße von Sample in Sample ändern kann.
-   **bfixedsizesamples**. Wenn dieses boolesche Flag " **true**" ist, bedeutet dies, dass der Wert in " **lsamplesize** " gültig ist. Andernfalls sollten Sie " **lsamplesize**" ignorieren.
-   **btemporalcompression**. Wenn dieses boolesche Flag **false** ist, bedeutet dies, dass es sich bei allen Frames um Keyframes handelt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Das Filter Diagramm und dessen Komponenten](the-filter-graph-and-its-components.md)
</dt> </dl>

 

 
