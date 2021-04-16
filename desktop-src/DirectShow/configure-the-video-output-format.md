---
description: Konfigurieren des Video Ausgabeformats
ms.assetid: 1969072e-575e-49b4-88db-4c7e7a5a1c37
title: Konfigurieren des Video Ausgabeformats
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d09ac64d7f43e6c39377277544867491a93a6f3e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104557878"
---
# <a name="configure-the-video-output-format"></a>Konfigurieren des Video Ausgabeformats

> [!Note]  
> Die in diesem Thema beschriebene Funktionalität ist veraltet. Um das Ausgabeformat eines Aufzeichnungs Geräts zu konfigurieren, muss eine Anwendung die [**am \_ \_ Medientyp**](/windows/win32/api/strmif/ns-strmif-am_media_type) -Struktur verwenden, die von [**iamstreamconfig:: GetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getformat) im *PMT* -Parameter zurückgegeben wird.

 

Ein Erfassungsgerät kann verschiedene Ausgabeformate unterstützen. Ein Gerät kann z. b. 16-Bit-RGB, 32-Bit RGB und yuyv unterstützen. Innerhalb jedes dieser Formate kann das Gerät einen Bereich von Frame Größen unterstützen.

In einem WDM-Gerät wird die [**iamstreamconfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) -Schnittstelle verwendet, um zu melden, welche Formate das Gerät unterstützt, und um das Format festzulegen. (Verwenden Sie für ältere VFW-Geräte das Dialogfeld VFW des Video Formats, wie in [Dialogfeldern zum Anzeigen der Vfw-Erfassung](display-vfw-capture-dialog-boxes.md)beschrieben.) Die **iamstreamconfig** -Schnittstelle wird in der Erfassungs-PIN, der Vorschau-PIN oder beiden der Erfassungs Filter verfügbar gemacht. Verwenden Sie die [**ICaptureGraphBuilder2:: findinterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) -Methode, um den Schnittstellen Zeiger zu erhalten:


```C++
IAMStreamConfig *pConfig = NULL;
hr = pBuild->FindInterface(
    &PIN_CATEGORY_PREVIEW, // Preview pin.
    0,    // Any media type.
    pCap, // Pointer to the capture filter.
    IID_IAMStreamConfig, (void**)&pConfig);
```



Das Gerät verfügt über eine Liste der von ihm unterstützten Medientypen. Für jeden Medientyp stellt das Gerät auch eine Reihe von Funktionen bereit. Dazu zählen der Bereich der Frame Größen, die für dieses Format verfügbar sind, wie gut das Gerät das Bildstrecken oder verkleinern kann, und der Bereich der Frameraten.

Um die Anzahl der Medientypen abzurufen, müssen Sie die [**iamstreamconfig:: getnumoffunktionalitäten**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getnumberofcapabilities) -Methode aufrufen. Die-Methode gibt zwei Werte zurück:

-   Die Anzahl der Medientypen.
-   Die Größe der-Struktur, die die Funktions Informationen enthält.

Der Größen Wert ist erforderlich, da die [**iamstreamconfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) -Schnittstelle sowohl für Audiodaten als auch für Video verwendet wird (und auf andere Medientypen erweitert werden kann). Für das Video werden die Funktionen mithilfe der [**\_ videolstream \_ - \_ Konfigurations**](/windows/win32/api/strmif/ns-strmif-video_stream_config_caps) Ober Struktur beschrieben, während die Audiostruktur die Struktur der [**audiodatenstream-Konfigurations Ober \_ \_ \_ Grenzen**](/windows/win32/api/strmif/ns-strmif-audio_stream_config_caps) verwendet.

Um die Medientypen aufzulisten, müssen Sie die [**iamstreamconfig:: getstreamcaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) -Methode mit einem NULL basierten Index aufrufen. Die **getstreamcaps** -Methode gibt einen Medientyp und die entsprechende Funktionsstruktur zurück:


```C++
int iCount = 0, iSize = 0;
hr = pConfig->GetNumberOfCapabilities(&iCount, &iSize);

// Check the size to make sure we pass in the correct structure.
if (iSize == sizeof(VIDEO_STREAM_CONFIG_CAPS))
{
    // Use the video capabilities structure.

    for (int iFormat = 0; iFormat < iCount; iFormat++)
    {
        VIDEO_STREAM_CONFIG_CAPS scc;
        AM_MEDIA_TYPE *pmtConfig;
        hr = pConfig->GetStreamCaps(iFormat, &pmtConfig, (BYTE*)&scc);
        if (SUCCEEDED(hr))
        {
            /* Examine the format, and possibly use it. */

            // Delete the media type when you are done.
            DeleteMediaType(pmtConfig);
        }
}
```



Beachten Sie, wie die-Strukturen für die [**getstreamcaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) -Methode zugeordnet werden. Die-Methode ordnet die Medientyp Struktur zu, während der Aufrufer die Funktionsstruktur ordnet. Wandelt die Funktionsstruktur in einen Byte Array Zeiger um. Nachdem Sie den Medientyp abgeschlossen haben, löschen Sie die [**am \_ - \_ Medientyp**](/windows/win32/api/strmif/ns-strmif-am_media_type) Struktur zusammen mit dem Format Block des Medientyps.

Sie können das Gerät so konfigurieren, dass es ein in der [**getstreamcaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) -Methode zurück gegebenes Format verwendet. Nennen Sie einfach [**iamstreamconfig:: SetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-setformat) mit dem Medientyp:


```C++
hr = pConfig->SetFormat(pmtConfig);
```



Wenn die PIN nicht verbunden ist, wird versucht, dieses Format zu verwenden, wenn eine Verbindung hergestellt wird. Wenn die PIN bereits verbunden ist, wird versucht, die Verbindung unter Verwendung des neuen Formats wiederherzustellen. In beiden Fällen ist es möglich, dass der Downstream-Filter das Format ablehnt.

Sie können den Medientyp auch ändern, bevor Sie ihn an die [**SetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-setformat) -Methode übergeben. An dieser Stelle kommt die Struktur der [**Video Daten \_ Strom-Konfigurations Ober \_ \_ Grenzen**](/windows/win32/api/strmif/ns-strmif-video_stream_config_caps) ins Spiel. Es beschreibt alle gültigen Möglichkeiten, den Medientyp zu ändern. Um diese Informationen verwenden zu können, müssen Sie die Details dieses bestimmten Medientyps verstehen.

Nehmen wir beispielsweise an, dass [**getstreamcaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) ein 24-Bit-RGB-Format mit einer Frame Größe von 320 x 240 Pixel zurückgibt. Sie erhalten diese Informationen, indem Sie den Haupttyp, den Untertyp und den Format Block des Medientyps untersuchen:


```C++
if ((pmtConfig.majortype == MEDIATYPE_Video) &&
    (pmtConfig.subtype == MEDIASUBTYPE_RGB24) &&
    (pmtConfig.formattype == FORMAT_VideoInfo) &&
    (pmtConfig.cbFormat >= sizeof (VIDEOINFOHEADER)) &&
    (pmtConfig.pbFormat != NULL))
{
    VIDEOINFOHEADER *pVih = (VIDEOINFOHEADER*)pmtConfig.pbFormat;
    // pVih contains the detailed format information.
    LONG lWidth = pVih->bmiHeader.biWidth;
    LONG lHeight = pVih->bmiHeader.biHeight;
}
```



Die Struktur der [**\_ \_ videostreamkonfigurationscaps \_**](/windows/win32/api/strmif/ns-strmif-video_stream_config_caps) gibt die minimale und maximale Breite und Höhe an, die für diesen Medientyp verwendet werden kann. Außerdem erhalten Sie die "Schritt"-Größe, mit der die Inkremente definiert werden, um die Sie die Breite oder Höhe anpassen können. Das Gerät könnte z. b. Folgendes zurückgeben:

-   Minoutputsize: 160 x 120
-   Maxoutputsize: 320 x 240
-   Outputgranularityx: 8 Pixel (horizontale Schrittgröße)
-   Outputgranularityy: 8 Pixel (vertikale Schrittgröße)

Wenn Sie diese Zahlen haben, können Sie die Breite auf alles im Bereich festlegen (160, 168, 176,... 304, 312, 320) und die Höhe auf alles im Bereich (120, 128, 136,... 104, 112, 120). Dieser Prozess wird anhand des folgenden Diagramms veranschaulicht.

![Video Formatgrößen](images/strmcap3.png)

Um eine neue Frame Größe festzulegen, ändern Sie [**die \_ am \_ Medientyp**](/windows/win32/api/strmif/ns-strmif-am_media_type) -Struktur, die in [**getstreamcaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps)zurückgegeben wird, direkt.


```C++
pVih->bmiHeader.biWidth = 160;
pVih->bmiHeader.biHeight = 120;
pVih->bmiHeader.biSizeImage = DIBSIZE(pVih->bmiHeader);
```



Übergeben Sie den Medientyp dann an die [**SetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-setformat) -Methode, wie zuvor beschrieben.

Die **minframeinterval** -und **maxframeinterval** -Member von [**Videodaten Strom- \_ \_ Konfigurations \_ Caps**](/windows/win32/api/strmif/ns-strmif-video_stream_config_caps) sind die Mindest-und höchst Länge jedes Video Rahmens, den Sie wie folgt in die Frameraten umwandeln können:

`frames per second = 10,000,000 / frame duration`

Um eine bestimmte Framerate anzufordern, ändern Sie den Wert von **avgtimeperframe** in der [**videoinfoheader**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) -oder [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) -Struktur im Medientyp. Das Gerät unterstützt möglicherweise nicht alle möglichen Werte zwischen dem minimal-und Maximalwert, sodass der Treiber den nächstgelegenen Wert verwendet. Um festzustellen, welchen Wert der Treiber tatsächlich verwendet hat, müssen Sie [**iamstreamconfig:: GetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getformat) aufrufen, nachdem Sie [**SetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-setformat)aufgerufen haben.

Einige Treiber melden möglicherweise **maxlonglong** (0x7FFFFFFFFFFFFFFF) als Wert von **maxframeinterval**, was bedeutet, dass es keine maximale Dauer gibt. Möglicherweise möchten Sie jedoch eine minimale Frame Rate in der Anwendung erzwingen, z. b. 1 fps.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zu Medientypen](about-media-types.md)
</dt> <dt>

[Konfigurieren eines Video Erfassungs Geräts](configuring-a-video-capture-device.md)
</dt> </dl>

 

 



