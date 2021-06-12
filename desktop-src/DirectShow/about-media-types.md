---
description: Erfahren Sie mehr über Medientypen in DirectShow. Der Medientyp ist eine universelle und erweiterbare Möglichkeit, digitale Medienformate zu beschreiben.
ms.assetid: 9984ba36-4e43-4886-a073-34b330274c9c
title: Informationen zu Medientypen (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7b1489543b33f5eeb2c288add48148b37f31915
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2021
ms.locfileid: "112010893"
---
# <a name="about-media-types-directshow"></a>Informationen zu Medientypen (DirectShow)

Da DirectShow modular aufgebaut ist, ist es erforderlich, das Format der Daten an jedem Punkt im Filterdiagramm zu beschreiben. Betrachten Sie beispielsweise die AVI-Wiedergabe. Daten werden in den Graphen als Stream vonUNK-Blocken übertragen. Diese werden in Video- und Audiostreams analysiert. Der Videostream besteht aus Videoframes, die wahrscheinlich komprimiert sind. Nach der Decodierung besteht der Videostream aus einer Reihe nicht komprimierter Bitmaps. Der Audiostream durchläuft einen ähnlichen Prozess.

Medientypen: Wie DirectShow Formate darstellt

Der *Medientyp ist* eine universelle und erweiterbare Möglichkeit, digitale Medienformate zu beschreiben. Wenn zwei Filter eine Verbindung herstellen, stimmen sie einem Medientyp zu. Der Medientyp gibt an, welche Art von Daten der Upstreamfilter an den Downstreamfilter liefert, und das physische Layout der Daten. Wenn sich zwei Filter nicht auf einen Medientyp einigen können, wird keine Verbindung hergestellt.

Bei einigen Anwendungen müssen Sie sich keine Gedanken über Medientypen machen. Bei der Dateiwiedergabe verarbeitet DirectShow beispielsweise alle Details. Andere Arten von Anwendungen müssen möglicherweise direkt mit Medientypen arbeiten.

Medientypen werden mithilfe der [**AM \_ MEDIA \_ TYPE-Struktur**](/windows/win32/api/strmif/ns-strmif-am_media_type) definiert. Diese Struktur enthält die folgenden Informationen:

-   **Haupttyp:** Der Haupttyp ist eine GUID, die die Gesamtkategorie der Daten definiert. Zu den Haupttypen zählen Video, Audio, nicht geparster Bytestream, DANN-Daten usw.
-   **Untertyp:** Der Untertyp ist eine weitere GUID, die das Format weiter definiert. Innerhalb des Haupttyps des Videos gibt es beispielsweise Untertypen für RGB-24, RGB-32, UY RGB usw. In audio gibt es PCM-Audio, MPEG-1-Nutzlast und andere. Der Untertyp stellt mehr Informationen als der Haupttyp zur Verfügung, definiert jedoch nicht alles über das Format. Videountertypen definieren z. B. weder die Bildgröße noch die Bildfrequenz. Diese werden durch den Formatblock definiert, der unten beschrieben wird.
-   **Formatblock:** Der Formatblock ist ein Datenblock, der das Format im Detail beschreibt. Der Formatblock wird getrennt von der [**AM \_ MEDIA \_ TYPE-Struktur**](/windows/win32/api/strmif/ns-strmif-am_media_type) zugeordnet. Der **pbFormat-Member** der **AM MEDIA \_ \_ TYPE-Struktur** zeigt auf den Formatblock.

    Der **pbFormat-Member** ist vom Typ **void \** _ , da sich das Layout des Formatblocks je nach Medientyp ändert. PCM-Audio verwendet beispielsweise eine [*_WAVEFORMATEX-Struktur.* *](/previous-versions/dd757713(v=vs.85)) Video verwendet verschiedene Strukturen, einschließlich [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) und [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2). Der **formattype-Member** der [**AM MEDIA \_ \_ TYPE-Struktur**](/windows/win32/api/strmif/ns-strmif-am_media_type) ist eine GUID, die angibt, welche Struktur im Formatblock enthalten ist. Jeder Formatstruktur wird eine GUID zugewiesen. Der **cbFormat-Member** gibt die Größe des Formatblocks an. Überprüfen Sie diese Werte immer, bevor Sie den **pbFormat-Zeiger** deferencieren.

Wenn der Formatblock ausgefüllt ist, enthalten Haupttyp und Untertyp redundante Informationen. Der Haupttyp und Untertyp bieten jedoch eine bequeme Möglichkeit, Formate ohne einen vollständigen Formatblock zu identifizieren. Beispielsweise können Sie ein generisches 24-Bit-RGB-Format (MEDIASUBTYPE RGB24) angeben, ohne alle Informationen zu kennen, die für die \_ [**VIDEOINFOHEADER-Struktur**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) erforderlich sind, z. B. Bildgröße und Bildfrequenz.

Beispielsweise kann ein Filter den folgenden Code verwenden, um einen Medientyp zu überprüfen:


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



Die [**AM \_ MEDIA \_ TYPE-Struktur**](/windows/win32/api/strmif/ns-strmif-am_media_type) enthält auch einige optionale Felder. Diese können verwendet werden, um zusätzliche Informationen zur Verfügung zu stellen, aber Filter sind nicht erforderlich, um sie zu verwenden:

-   **lSampleSize**. Wenn dieses Feld nicht 0 (null) ist, wird die Größe der einzelnen Stichproben definiert. Wenn der Wert 0 (null) ist, bedeutet dies, dass sich die Stichprobengröße von Stichproben in Stichproben ändern kann.
-   **bFixedSizeSamples**. Wenn dieses boolesche Flag **TRUE ist,** bedeutet dies, dass der Wert in **lSampleSize** gültig ist. Andernfalls sollten Sie **lSampleSize ignorieren.**
-   **bTemporalCompression**. Wenn dieses boolesche Flag **FALSE ist,** bedeutet dies, dass alle Frames Keyframes sind.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Das Filterdiagramm und seine Komponenten](the-filter-graph-and-its-components.md)
</dt> </dl>

 

 
