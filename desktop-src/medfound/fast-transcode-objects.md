---
description: In diesem Thema wurde beschrieben, wie sie die Transcodierungs-API zum Codieren einer Mediendatei verwendet.
ms.assetid: 52b27359-b319-41a0-88e8-d23567420e92
title: Verwenden der Transcodierungs-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72e32ea24ebd4803319713be5fe7789cf41c3a99733338bdfe5ad69baf7396bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118742478"
---
# <a name="using-the-transcode-api"></a>Verwenden der Transcodierungs-API

In diesem Thema wurde beschrieben, wie sie die Transcodierungs-API zum Codieren einer Mediendatei verwendet.

-   [Übersicht](#overview)
-   [Erstellen einer Medienquelle](#creating-a-media-source)
-   [Erstellen eines Transcodierungsprofils](#creating-a-transcode-profile)
    -   [Audioattribute](#audio-attributes)
    -   [Videoattribute](#video-attributes)
    -   [Containerattribute](#container-attributes)
-   [Erstellen einer Transcodierungstopologie](#creating-a-transcode-topology)
-   [Ausführen der Codierungssitzung](#running-the-encoding-session)
-   [Zugehörige Themen](#related-topics)

## <a name="overview"></a>Übersicht

Vor der Verwendung der Transcodierungs-API muss die Anwendung über die folgenden Informationen verfügen:

-   Der Pfad oder die URL zu einer vorhandenen Mediendatei, die erneut codiert wird.
-   Der Name der Ausgabedatei.
-   Der Containertyp für die Ausgabedatei, z. B. MP4 oder Advanced Streaming Format (ASF).
-   Das Codierungsformat. Diese Informationen umfassen die Medientypen, die die codierten Audio- und Videostreams beschreiben.

Um die Transcodierungs-API zu verwenden, führt eine Anwendung die folgenden Schritte aus.

1.  Erstellen Sie eine Medienquelle, um die Quelldatei zu lesen.
2.  Erstellen Sie ein Transcodierungsprofil. Fügen Sie Attribute hinzu, die den Audiostream, den Videostream und den Dateicontainer beschreiben.
3.  Verwenden Sie das Transcodierungsprofil, um eine Codierungstopologie zu erstellen. (Weitere Informationen zu Topologien finden Sie unter [Informationen zu Topologien.)](about-topologies.md)
4.  Legen Sie die Topologie für die [Mediensitzung fest.](media-session.md)
5.  Starten Sie die Mediensitzung, und warten Sie auf das [MESessionEnded-Ereignis.](mesessionended.md)

Im weiteren Verlauf dieses Themas werden diese Schritte ausführlicher beschrieben.

## <a name="creating-a-media-source"></a>Erstellen einer Medienquelle

Eine Medienquelle ist ein Objekt, das die Quelldatei liest und analysiert. Verwenden Sie zum Erstellen einer Medienquelle den [Quellre resolver](source-resolver.md). Beispielcode finden Sie im Thema [Verwenden des Quellre resolvers](using-the-source-resolver.md).

## <a name="creating-a-transcode-profile"></a>Erstellen eines Transcodierungsprofils

Ein *Transcodierungsprofil* beschreibt das Format und die Einstellungen, die zum Codieren der Ausgabedatei verwendet werden. Das Transcodierungsprofil enthält drei Sätze von Attributen:

-   Audioattribute: Beschreiben Sie das Zielaudioformat und die Audioencodereinstellungen.
-   Videoattribute: Beschreiben Sie das Zielvideoformat und die Videoencodereinstellungen.
-   Containerattribute: Definieren Sie den Typ des Dateicontainers sowie einige globale Codierungseinstellungen.

Rufen Sie zum Erstellen eines Transcodierungsprofils die [**MFCreateTranscodeProfile-Funktion**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodeprofile) auf. Diese Funktion gibt einen Zeiger auf die [**INTERFACESTranscodeProfile-Schnittstelle**](/windows/desktop/api/mfidl/nn-mfidl-imftranscodeprofile) zurück. Das anfängliche Profilobjekt ist leer. sie enthält keine Attribute. Im nächsten Schritt fügen Sie die Attribute hinzu, die das Profil definieren.

### <a name="audio-attributes"></a>Audioattribute

Rufen Sie ZUM Hinzufügen von Attributen für den Audiodatenstrom [**DIEDRTranscodeProfile::SetAudioAttributes auf.**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setaudioattributes) Diese Attribute geben an, wie der Audiostream codiert wird. Wenn die Ausgabedatei keinen Audiostream enthält, sollten Sie diese Attribute weglassen.

Audioattribute lassen sich in zwei Kategorien unterteilen:

-   Attribute, die das Format des codierten Streams angeben
-   Attribute, die andere Codierungsparameter angeben.

Formatattribute sind einfach Medientypattribute, wie im Abschnitt [Audiomedientypen beschrieben.](audio-media-types.md) Der genaue Satz von Formatattributen hängt vom Encoder ab. (Siehe [Unterstützte Medienformate in Media Foundation](supported-media-formats-in-media-foundation.md).) Im Folgenden finden Sie eine Liste der typischen Audioformatattribute:



| Formatattribut                                                                         | Beschreibung                                                      |
|------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| [MF \_ \_ MT-UNTERTYP](mf-mt-subtype-attribute.md)                                           | Der Untertyp. Weitere Informationen [finden Sie unter Audio Subtype GUIDs ( Untertyp-GUIDs für Audio).](audio-subtype-guids.md) |
| [MF \_ MT AUDIO \_ \_ \_ NUM-KANÄLE](mf-mt-audio-num-channels-attribute.md)                   | Die Anzahl der Audiokanäle.                                    |
| [MF \_ \_ MT-AUDIOBEISPIELE \_ \_ PRO \_ SEKUNDE](mf-mt-audio-samples-per-second-attribute.md)      | Die Anzahl der Audiobeispiele pro Sekunde.                          |
| [MF MT AUDIO BLOCK ALIGNMENT (MF \_ \_ MT-AUDIOBLOCKAUSRICHTUNG) \_ \_](mf-mt-audio-block-alignment-attribute.md)             | Die Blockausrichtung.                                             |
| [MF \_ MT \_ AUDIO \_ AVG \_ BYTES \_ PER \_ SECOND](mf-mt-audio-avg-bytes-per-second-attribute.md) | Die durchschnittliche Anzahl von Bytes pro Sekunde (die codierte Bitrate).   |



 

Die folgenden Codierungsparameter sind definiert.



| Codierungsparameter                                                             | Beschreibung                                                                |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [MF \_ TRANSCODE \_ DONOT \_ INSERT \_ ENCODER](mf-transcode-donot-insert-encoder.md) | Verhindert, dass die Transcodierungs-API einen Encoder für den Audiostream einfüge. |
| [MF \_ TRANSCODE \_ ENCODINGPROFILE](mf-transcode-encodingprofile.md)             | Gibt die Gerätekonformitätsvorlage an. (Gilt nur für ASF-Dateien.)    |
| [\_ \_ MF-TRANSCODIERUNGSQUALITÄTVSSPEED](mf-transcode-qualityvsspeed.md)               | Gibt den Vor- und Abkniff zwischen Codierungsqualität und Geschwindigkeit an.                |



 

Sie müssen die Formatattribute festlegen. Die Codierungsparameter sind optional.

Eine Möglichkeit, ein Format zu finden, das mit dem Encoder kompatibel ist, besteht im Aufrufen der [**MFTranscodeGetAudioOutputAvailableTypes-Funktion.**](/windows/desktop/api/mfidl/nf-mfidl-mftranscodegetaudiooutputavailabletypes) Der gewünschte Encoder wird durch den Untertyp angegeben. Die Funktion gibt eine Auflistung von Medientypen für diesen Encoder zurück. Sie können einen Typ aus der Liste auswählen und die Attribute in das Profil kopieren. Beispielcode, der diesen Ansatz verwendet, finden Sie unter [Tutorial: Codieren einer WMA-Datei.](tutorial--converting-an-mp3-file-to-a-wma-file.md)

### <a name="video-attributes"></a>Videoattribute

Rufen Sie ZUM Hinzufügen von Attributen für den Videostream [**DIETRANSCODEProfile::SetVideoAttributes auf.**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setvideoattributes) Diese Attribute geben an, wie der Videostream codiert wird. Wenn die Ausgabedatei keinen Videostream enthält, sollten Sie diese Attribute weglassen.

Wie bei Audioattributen fallen die Videoattribute in zwei Kategorien:

-   Attribute, die das Format des codierten Streams angeben
-   Attribute, die andere Codierungsparameter angeben.

Formatattribute sind Medientypattribute, wie im Abschnitt [Videomedientypen beschrieben.](video-media-types.md) Im Folgenden finden Sie eine Liste der typischen Videoformatattribute:



| Formatattribut                                                       | Beschreibung                                                      |
|------------------------------------------------------------------------|------------------------------------------------------------------|
| [MF \_ \_ MT-UNTERTYP](mf-mt-subtype-attribute.md)                         | Der Untertyp. Weitere Informationen [finden Sie unter Video Subtype GUIDs](video-subtype-guids.md). |
| [MF \_ MT \_ FRAME \_ RATE](mf-mt-frame-rate-attribute.md)                  | Die Bildfrequenz.                                                  |
| [MF \_ MT \_ FRAME \_ SIZE](mf-mt-frame-size-attribute.md)                  | Die Framegröße.                                                  |
| [**MF \_ MT \_ AVG \_ BITRATE**](mf-mt-avg-bitrate-attribute.md)            | Die durchschnittliche Bitrate.                                            |
| [SEITENVERHÄLTNIS DES MF \_ \_ \_ MT-PIXELS \_](mf-mt-pixel-aspect-ratio-attribute.md) | Das Pixel-Seitenverhältnis.                                          |



 

Die folgenden Codierungsparameter sind definiert.



| Codierungsparameter                                                             | Beschreibung                                                                |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [MF \_ TRANSCODE \_ DONOT \_ INSERT \_ ENCODER](mf-transcode-donot-insert-encoder.md) | Verhindert, dass die Transcodierungs-API einen Encoder für den Videostream einfüge. |
| [MF \_ TRANSCODE \_ ENCODINGPROFILE](mf-transcode-encodingprofile.md)             | Gibt die Gerätekonformitätsvorlage an. (Gilt nur für ASF-Dateien.)    |
| [MF \_ TRANSCODE \_ QUALITYVSSPEED](mf-transcode-qualityvsspeed.md)               | Gibt den Vor- und Abkniff zwischen Codierungsqualität und Geschwindigkeit an.                |



 

Sie müssen die Formatattribute festlegen. Die Codierungsparameter sind optional.

### <a name="container-attributes"></a>Containerattribute

Containerattribute definieren Merkmale der Ausgabedatei auf Dateiebene. Rufen Sie ZUM Festlegen von Containerattributen [**DEN WERT FÜR DIETRANSCODEProfile::SetContainerAttributes auf.**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes) Die folgenden Attribute werden definiert.



| attribute                                                                          | Beschreibung                                                                                                                                            |
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ANPASSEN DES \_ MF-TRANSCODIERUNGSPROFILS \_ \_](mf-transcode-adjust-profile.md)                  | Definiert die Streameinstellungen, die für die Transcodierungstopologie verwendet werden. Sie können die Flags so festlegen, dass sie die Eingabequelleneinstellungen verwenden, oder benutzerdefinierte Streamattribute verwenden. |
| [MF \_ TRANSCODE \_ CONTAINERTYPE](mf-transcode-containertype.md)                     | Gibt das Dateiformat der Ausgabedatei an, z. B. MP4 oder ASF. Basierend auf diesem Wert wird der Topologie die entsprechende Mediensenke hinzugefügt.            |
| [\_MF-TRANSCODIERUNG \_ \_ ÜBERSPRINGT \_ METADATENÜBERTRAGUNG](mf-transcode-skip-metadata-transfer.md) | Gibt an, ob Metadaten aus der Quelle in die Ausgabedatei kopiert werden.                                                                               |
| [MF \_ TRANSCODE \_ TOPOLOGYMODE](mf-transcode-topologymode.md)                       | Gibt an, ob hardwarebasierte Codecs während der Transcodierung verwendet werden können.                                                                                |
| [MFT \_ FIELDOFUSE \_ \_ UNLOCK-Attribut](mft-fieldofuse-unlock-attribute.md)          | Entsperrt einen Codec mit Nutzungseinschränkungen. Weitere Informationen finden Sie unter [Verwendungseinschränkungen.](field-of-use-restrictions.md)              |



 

Das [MF \_ TRANSCODE \_ CONTAINERTYPE-Attribut](mf-transcode-containertype.md) ist erforderlich. Die anderen Containerattribute sind optional.

## <a name="creating-a-transcode-topology"></a>Erstellen einer Transcodierungstopologie

Die Transcodierungstopologie ist eine Teiltopologie, die die Medienquelle, die entsprechenden Codecs und die Mediensenke enthält. Rufen Sie zum Erstellen der Transcodierungstopologie die [**MFCreateTranscodeTopology-Funktion**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodetopology) auf. Diese Funktion verwendet die folgenden Parameter als Eingabe:

-   Ein Zeiger auf die [**BENUTZEROBERFLÄCHEMediaSource-Schnittstelle**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) der Medienquelle.
-   Der Name der Ausgabedatei.
-   Ein Zeiger auf die [**BENUTZEROBERFLÄCHETranscodeProfile-Schnittstelle**](/windows/desktop/api/mfidl/nn-mfidl-imftranscodeprofile) des Transcodierungsprofils.

Die Funktion gibt einen Zeiger auf [**dieTOPOLOGYTopology-Schnittstelle**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) zurück.

## <a name="running-the-encoding-session"></a>Ausführen der Codierungssitzung

Nachdem Sie die Topologie erstellt haben, können Sie die Datei codieren. Sie können das Profil zu diesem Zeitpunkt verwerfen.

1.  Rufen [**Sie MFCreateMediaSession auf,**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) um die Mediensitzung zu erstellen.
2.  Rufen [**Sie ZUM FESTLEGEN DERMEDIASESSION::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) auf, um die Topologie für die Mediensitzung festzugeben.
3.  Rufen [**Sie ZUM STARTEN DERMEDIASESSION::Start auf,**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) um die Codierungssitzung zu starten.
4.  Warten Sie auf das [MESessionEnded-Ereignis.](mesessionended.md)
5.  Rufen [**Sie ZUM SCHLIEßEN DIEMEDIASESSION::Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) auf, um die Mediensitzung zu schließen.
6.  Warten Sie auf das [MESessionClosed-Ereignis.](mesessionclosed.md)
7.  Rufen [**Sie DEN AUFRUF VON DURCHMEDIASOURCE::Shutdown auf.**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown)
8.  Rufen [**Sie DEN AUFRUF VON DERMEDIASESSION::Shutdown auf.**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown)

Die meiste Zeit für die Codierung liegt zwischen den Schritten 3 und 4.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Transcodierungs-API](transcode-api.md)
</dt> <dt>

[Informationen zur Mediensitzung](about-the-media-session.md)
</dt> </dl>

 

 



