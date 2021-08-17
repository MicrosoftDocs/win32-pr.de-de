---
description: In diesem Thema wird beschrieben, wann und wie eine H.264/AVC Remux MFT- und MP4-Senke verwendet wird.
ms.assetid: 1DD236D9-775B-4417-BC49-BF52A6B3C8AD
title: Verwendung von H.264/AVC Remux MFT und MP4-Senke
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6ce5b6d63a21e7a9d6b75acd29690cdeaeba5b0105dcf8d45fe0c93e6b768f3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119357950"
---
# <a name="when-and-how-to-use-h264avc-remux-mft-and-mp4-sink"></a>Verwendung von H.264/AVC Remux MFT und MP4-Senke

In diesem Thema wird beschrieben, wann und wie eine H.264/AVC Remux MFT- und MP4-Senke verwendet wird.

## <a name="when-to-use-h264avc-remux-mft"></a>Verwendung von H.264/AVC Remux MFT

Das MPEG-4-Dateiformat erfordert, dass jedes komprimierte Beispiel ein primäres Bild mit NAL-Einheiten in der richtigen Reihenfolge enthält. (Informationen finden Sie in abschnitt 7.4.1.2.3, Order **of NAL units and coded pictures** and association to access units (Reihenfolge von NAL-Einheiten und codierten Bildern und Zuordnung zu Zugriffseinheiten) in Abschnitt 7.4.1.2.3 der H.264 AVC-Spezifikation.) Außerdem ist es erforderlich, dass jede komprimierte Stichprobe einem Präsentationszeitstempel, einem Decodierungszeitstempel und einer Stichprobendauer zugeordnet ist.

In vielen Szenarien, in denen Anwendungen H.264/AVC-Video in einem MPEG-4-Dateicontainer aufzeichnen müssen, erfüllt das komprimierte Beispiel möglicherweise nicht die oben genannten Anforderungen. Beispielsweise enthält ein komprimiertes Beispiel möglicherweise kein vollständiges primäres Bild oder es ist kein korrekter Präsentationszeitstempel zugeordnet. Einige Anwendungsbeispiele sind:

-   Schreiben Sie H.264/AVC streaming elementary video in den MPEG-4-Dateicontainer.
-   Zeichnen Sie die Kamera auf, die ein elementares H.264/AVC-Video im MPEG-4-Dateicontainer erfasst hat.
-   Zeichnen Sie die H.264/AVC-Videokonferenz im MPEG-4-Dateicontainer auf.
-   Verketten Sie zwei H.264/AVC-Videos in MPEG-2 TS oder MP4, und schreiben Sie mit den richtigen Zeitstempeln in den MPEG-4-Dateicontainer.
-   Remux H.264/AVC-Video von AVCHD, MPEG-2 TS/PS-Dateiformat in MPEG-4-Dateiformat.
-   Kürzen Sie die H.264/AVC-Videodatei ohne Transcodierung.

In diesem Fall muss die Anwendung H.264/AVC remux MFT verwenden, um die komprimierten Beispiele zu konvertieren, die kein vollständiges primäres Bild enthalten, bevor sie in den MPEG-4-Dateicontainer geschrieben werden.

## <a name="how-to-use-h264avc-remux-mft-and-mp4-sink"></a>Verwenden der H.264/AVC Remux MFT- und MP4-Senke

Legen Sie den Quellausgabemedientyp auf **MFVideoFormat \_ H264 \_ ES** fest. Dies bedeutet, dass jedes Beispiel möglicherweise kein vollständiges primäres Bild enthält. Legen Sie den Eingabemedientyp der MP4-Senke **auf MFVideoFormat \_ H264 fest.** Daher ist der Eingabemedientyp von H.264/AVC remux MFT **MFVideoFormat \_ H264 \_ ES** und der Ausgabemedientyp von H.264/AVC remux MFT **MFVideoFormat \_ H264**, der automatisch in den Topologiere konfliktlöser eingefügt wird.

Die Beispieldauer wird von der H.264/AVC-Remux ignoriert, da die Stichprobendauer für ein Beispiel, das kein vollständiges primäres Bild enthält, keine klare Bedeutung hat. Stattdessen wird die Stichprobendauer anhand der Framerate berechnet. Die Framerate wird aus dem Sequenzparameter berechnet. Wenn die Informationen im Sequenzparameter nicht vorhanden sind, wird die Framerate aus den Parametern im Eingabemedientyp berechnet. Wenn keine Bildfrequenzinformationen verfügbar sind, wird die Standardbildrate von 29,97 fps verwendet.

H.264/AVC remux MFT interpoliert die Decodierungszeitstempel (Decoding Time Stamps, DTS) für jedes komprimierte Bild gemäß der Bildfrequenz linear. H.264/AVC remux MFT verwendet die Eingabepräsentations-Zeitstempel (Input Presentation Time Stamps, PTS) in Eingabebeispielen und übergibt sie an die Ausgabe, sofern vorhanden. Die PTS-Interpolation wird entsprechend der Bildfrequenz, dem vorherigen PTS und der Bildausgabe reihenfolge durch dbP-Bumping (Decoded Picture Buffering) durchgeführt, wie in Anhang **C.4.5.3 Bumping** process of the H.264 AVC specification (H.264-AVC-Spezifikation) angegeben. Jedes Ausgabebeispiel aus H.264/AVC remux MFT muss PTS, DTS und Stichprobendauer haben. H.264/AVC remux MFT identifiziert auch die IDR-Bilder im Bitstream und legt sie mit dem [MF-Attribut von MFSampleExtension \_ CleanPoint](mfsampleextension-cleanpoint-attribute.md)als bereinigten Punkt fest.

Derzeit kann H.264/AVC remux MFT maximal 64 neu angeordnete Frames verarbeiten. Wenn die Anzahl der neu angeordneten Frames 64 überschreitet und ein langfristiger Referenzrahmen vorhanden ist, interpoliert H.264/AVC remux MFT einen falschen PTS für diesen Frame und gibt diesen Frame zu einem falschen Zeitpunkt aus.

Legen Sie zum Instanziieren eines H.264/AVC-Remux MFT die richtigen Eingabe- und Ausgabemedientypen für H.264/AVC remux MFT fest, legen Sie den Eingabemedientyp für die MP4-Senke fest, und lösen Sie die Topologie auf.

Der folgende Beispielcode zeigt, wie die H.264/AVC remux MFT- und MP4-Senke initialisiert wird.

Für H.264/AVC remux MFT:


```C++
hr = CoCreateInstance(
            CLSID_CMSH264RemuxMFT,
            NULL,
            CLSCTX_INPROC_SERVER,
            IID_IMFTransform,
            (void**) &pIMFTransform
            );
```



Es ist keine weitere Konfiguration erforderlich.

Für die MP4-Senke:


```C++
IMFByteStream*  pMFBSOutputFile = NULL;
hr = MFCreateFile(
    MF_ACCESSMODE_READWRITE,
    MF_OPENMODE_DELETE_IF_EXIST,
    MF_FILEFLAGS_NONE,
    m_pszOutputFile,
    &pMFBSOutputFile);
if(FAILED(hr))
{
    Log(L"ERROR>> Failed to create output file for MP4 Sink (hr=0x%x)", hr);
    break;
}

hr = MFCreateMPEG4MediaSink(
    pMFBSOutputFile,
    (guidMajorType == MFMediaType_Video) ? pMediaType : NULL,  // pMediaType comes from the output type of the remux MFT
    (guidMajorType == MFMediaType_Audio) ? pMediaType : NULL,
    &m_pMediaSink);
if(FAILED(hr))
{
    Log(L"ERROR>> Failed to create MP4 Sink (hr=0x%x)", hr);
    break;
}
hr = m_pMediaSink->GetStreamSinkByIndex(0, &pStream);
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Unterstützte Medienformate in Media Foundation](supported-media-formats-in-media-foundation.md)
</dt> </dl>

 

 



