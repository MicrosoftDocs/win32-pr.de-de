---
description: In diesem Thema wird beschrieben, wann und wie eine H. 264/AVC REMUX-MFT-und MP4-Senke verwendet wird.
ms.assetid: 1DD236D9-775B-4417-BC49-BF52A6B3C8AD
title: Verwendung von H. 264/AVC REMUX MFT und MP4-Senke
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 132c582fa16eae56c4fec8809caa4bd501469e16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368261"
---
# <a name="when-and-how-to-use-h264avc-remux-mft-and-mp4-sink"></a>Verwendung von H. 264/AVC REMUX MFT und MP4-Senke

In diesem Thema wird beschrieben, wann und wie eine H. 264/AVC REMUX-MFT-und MP4-Senke verwendet wird.

## <a name="when-to-use-h264avc-remux-mft"></a>Verwendung von H. 264/AVC REMUX MFT

Das MPEG-4-Dateiformat erfordert, dass jede komprimierte Stichprobe ein primäres Bild mit nal-Einheiten in der richtigen Reihenfolge enthält. (Informationen hierzu finden Sie in der Definition der Reihenfolge der primär Bild-und obligatorischen nal-Einheiten im Abschnitt 7.4.1.2.3, in der **Reihenfolge der NAL-Einheiten und in den codierten Bildern und der Zuordnung zu Zugriffs Einheiten** der H. 264 AVC-Spezifikation.) Außerdem ist es erforderlich, dass jedes komprimierte Beispiel einem Präsentationszeit Stempel, dem Decodieren des Zeitstempels und der Stichproben Dauer zugeordnet ist.

In vielen Szenarios, in denen Anwendungen H. 264/AVC-Videos in einem MPEG-4-Datei Container aufzeichnen müssen, erfüllt die komprimierte Stichprobe möglicherweise nicht die oben genannten Anforderungen. Beispielsweise kann eine komprimierte Stichprobe keinen kompletten primär Bild enthalten, oder es ist kein richtiger Präsentationszeit Stempel zugeordnet. Einige Anwendungsbeispiele sind:

-   Schreiben Sie das "H. 264/AVC Streaming Elementary Video" in den MPEG-4-Datei Container.
-   Zeichnen Sie die Kamera mit dem H. 264/AVC-elementaren Video im MPEG-4-Datei Container auf.
-   Aufzeichnen der H. 264/AVC-Videokonferenz im MPEG-4-Datei Container.
-   Verketten von zwei H. 264/AVC-Videos in MPEG-2 TS oder MP4 und Schreiben in den MPEG-4-Datei Container mit korrekten Zeitstempeln.
-   REMUX H. 264/AVC-Video vom AVCHD-, MPEG-2 TS/PS-Dateiformat in das MPEG-4-Dateiformat.
-   Kürzen der H. 264/AVC-Videodatei ohne Transcoding.

In diesem Fall muss die Anwendung eine H. 264/AVC REMUX-MFT verwenden, um die komprimierten Samples zu konvertieren, die kein vollständiges primär Bild enthalten, bevor Sie in den MPEG-4-Datei Container geschrieben werden.

## <a name="how-to-use-h264avc-remux-mft-and-mp4-sink"></a>Verwenden von H. 264/AVC REMUX MFT und MP4-Senke

Legen Sie den Medientyp für die Quell Ausgabe auf **mfvideoformat \_ H264 \_ es** fest. Dies bedeutet, dass jedes Beispiel kein vollständiges primär Bild enthalten kann. Legen Sie den Eingabe Medientyp der MP4-Senke auf **mfvideoformat \_ H264** fest. Daher ist der Eingabe Medientyp von h. 264/AVC REMUX MFT **mfvideoformat \_ H264 \_ es** , und der Ausgabe Medientyp von h. 264/AVC REMUX MFT ist **mfvideoformat \_ H264**, der automatisch in den topologieresolver eingefügt wird.

Die Stichproben Dauer wird von H. 264/AVC REMUX ignoriert, da die Stichproben Dauer für ein Beispiel, das keinen kompletten primär Bild enthält, keine klare Bedeutung hat. Stattdessen wird die Stichproben Dauer aus der Framerate berechnet. Die Framerate wird aus dem Sequenz Parameter berechnet. Wenn die Informationen nicht im Sequence-Parameter vorhanden sind, wird die Framerate aus den Parametern im Eingabe Medientyp berechnet. Wenn keine Frameraten Informationen verfügbar sind, wird die Standardbildrate von 29,97 fps verwendet.

H. 264/AVC REMUX MFT linear interpoliert die Decodierungs Zeitstempel (DTS) für jedes komprimierte Bild entsprechend der Framerate. H. 264/AVC REMUX MFT berücksichtigt die Eingabe Präsentationszeit Stempel (PTS) in Eingabe Beispielen und übergibt sie an die Ausgabe, sofern Sie vorhanden sind. Sie führt die PTS-Interpolation gemäß der Framerate, den vorherigen PTS und der Bild Ausgabe Reihenfolge durch den decodierten Bild Puffer Prozess (DBP) durch, wie in **Anhang C. 4.5.3-bumpingprozess** der H. 264 AVC-Spezifikation angegeben. Jede Ausgabe Stichprobe aus dem H. 264/AVC REMUX-MFT muss über PTS, DTS und eine Stichproben Dauer verfügen. H. 264/AVC REMUX MFT identifiziert auch die IDR-Bilder im Bitstrom und legt sie als Clean Point mit dem MF-Attribut des [mfsampleextension- \_ cleanpoints](mfsampleextension-cleanpoint-attribute.md)fest.

Derzeit kann die "H. 264/AVC REMUX"-MFT maximal 64 reorderframe verarbeiten. Wenn die Anzahl der neu bestellten Frames den Wert 64 mit einem langfristigen Verweis Rahmen überschreitet, Interpolieren die H. 264/AVC REMUX-MFT einen falschen Punkt für diesen Frame und gibt diesen Frame zu einem falschen Zeitpunkt aus.

Um eine h. 264/AVC REMUX-MFT zu instanziieren, legen Sie die richtigen Eingabe-und Ausgabemedien Typen in der H. 264/AVC REMUX-MFT fest, legen Sie den Eingabe Medientyp für die MP4-Senke fest, und beheben Sie die Topologie.

Der folgende Beispielcode zeigt, wie die H. 264/AVC REMUX-MFT und die MP4-Senke initialisiert werden.

Für H. 264/AVC REMUX MFT,


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

Für MP4-Senke:


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

 

 



