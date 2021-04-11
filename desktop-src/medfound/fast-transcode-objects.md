---
description: In diesem Thema wird beschrieben, wie Sie die transcodieren-API verwenden, um eine Mediendatei zu codieren.
ms.assetid: 52b27359-b319-41a0-88e8-d23567420e92
title: Verwenden der transcode-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bb97dd61ef75e71a82b522b65b682f861022bcf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127888"
---
# <a name="using-the-transcode-api"></a>Verwenden der transcode-API

In diesem Thema wird beschrieben, wie Sie die transcodieren-API verwenden, um eine Mediendatei zu codieren.

-   [Übersicht](#overview)
-   [Erstellen einer Medienquelle](#creating-a-media-source)
-   [Erstellen eines transcode-Profils](#creating-a-transcode-profile)
    -   [Audioattribute](#audio-attributes)
    -   [Video Attribute](#video-attributes)
    -   [Container Attribute](#container-attributes)
-   [Erstellen einer transcode-Topologie](#creating-a-transcode-topology)
-   [Ausführen der Codierungs Sitzung](#running-the-encoding-session)
-   [Zugehörige Themen](#related-topics)

## <a name="overview"></a>Übersicht

Vor der Verwendung der transcodieren-API muss die Anwendung über die folgenden Informationen verfügen:

-   Der Pfad oder die URL zu einer vorhandenen Mediendatei, die erneut codiert wird.
-   Der Name der Ausgabedatei.
-   Der Containertyp für die Ausgabedatei, z. b. MP4 oder Advanced Streaming Format (ASF).
-   Das Codierungsformat. Zu diesen Informationen gehören die Medientypen, die die codierten Audiodaten und Videostreams beschreiben.

Um die transcodieren-API zu verwenden, führt eine Anwendung die folgenden Schritte aus.

1.  Erstellen Sie eine Medienquelle, um die Quelldatei zu lesen.
2.  Erstellen Sie ein transcodieren-Profil. Fügen Sie Attribute hinzu, die den Audiostream, den Videostream und den Datei Container beschreiben.
3.  Verwenden Sie das transcodieren-Profil, um eine Codierungs Topologie zu erstellen. (Weitere Informationen zu Topologien finden Sie unter Informationen [zu Topologien](about-topologies.md).)
4.  Legen Sie die Topologie für die [Medien Sitzung](media-session.md)fest.
5.  Starten Sie die Medien Sitzung, und warten Sie auf das Ereignis [mesessionend](mesessionended.md) .

Im restlichen Teil dieses Themas werden diese Schritte ausführlicher beschrieben.

## <a name="creating-a-media-source"></a>Erstellen einer Medienquelle

Eine Medienquelle ist ein Objekt, das die Quelldatei liest und analysiert. Verwenden Sie zum Erstellen einer Medienquelle den [quellresolver](source-resolver.md). Beispielcode finden Sie im Thema [Verwenden des Quell Resolvers](using-the-source-resolver.md).

## <a name="creating-a-transcode-profile"></a>Erstellen eines transcode-Profils

Ein *transcodieren-Profil* beschreibt das Format und die Einstellungen, die zum Codieren der Ausgabedatei verwendet werden. Das transcodieren-Profil enthält drei Sätze von Attributen:

-   Audioattribute: Beschreibt die Ziel Einstellungen für das Audioformat und den Audioencoder.
-   Video Attribute: beschreiben Sie die Ziel Videoformat-und Video Encoder-Einstellungen.
-   Container Attribute: Hiermit werden der Typ des Datei Containers sowie einige globale Codierungs Einstellungen definiert.

Um ein transcodieren-Profil zu erstellen, rufen Sie die Funktion " [**mfkreatetranscodeprofile**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodeprofile) " auf. Diese Funktion gibt einen Zeiger auf die [**imftranscodeprofile**](/windows/desktop/api/mfidl/nn-mfidl-imftranscodeprofile) -Schnittstelle zurück. Das anfängliche Profil Objekt ist leer. Sie enthält keine Attribute. Der nächste Schritt besteht darin, die Attribute hinzuzufügen, die das Profil definieren.

### <a name="audio-attributes"></a>Audioattribute

Um dem Audiodatenstrom Attribute hinzuzufügen, müssen Sie [**imftranscodeprofile:: setaudioattribute**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setaudioattributes)aufrufen. Diese Attribute geben an, wie der Audiostream codiert wird. Wenn die Ausgabedatei keinen Audiostream enthält, lassen Sie diese Attribute aus.

Audioattribute werden in zwei Kategorien unterteilt:

-   Attribute, die das Format des codierten Streams angeben
-   Attribute, die andere Codierungs Parameter angeben.

Format Attribute sind einfache Medientyp Attribute, wie im Abschnitt [audiomedientypen](audio-media-types.md)beschrieben. Der genaue Satz von Format Attributen hängt vom Encoder ab. (Informationen hierzu finden Sie [unter Unterstützte Medienformate in Media Foundation](supported-media-formats-in-media-foundation.md).) Im folgenden finden Sie eine Liste mit typischen audioformatattributen:



| Format-Attribut                                                                         | BESCHREIBUNG                                                      |
|------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| [MF- \_ MT- \_ Untertyp](mf-mt-subtype-attribute.md)                                           | Der Untertyp. Siehe [audiountertyp-GUIDs](audio-subtype-guids.md). |
| [MF \_ \_ -MT- \_ audionum- \_ Kanäle](mf-mt-audio-num-channels-attribute.md)                   | Die Anzahl der audiochannels.                                    |
| [MF \_ \_ -MT- \_ Audiobeispiele \_ pro \_ Sekunde](mf-mt-audio-samples-per-second-attribute.md)      | Die Anzahl von Audiobeispielen pro Sekunde.                          |
| [MF \_ \_ -MT- \_ Audioblock \_ Ausrichtung](mf-mt-audio-block-alignment-attribute.md)             | Die Block Ausrichtung.                                             |
| [MF \_ \_ -MT-audiodurchschn. \_ \_ Byte \_ pro \_ Sekunde](mf-mt-audio-avg-bytes-per-second-attribute.md) | Die durchschnittliche Anzahl von Bytes pro Sekunde (die codierte Bitrate).   |



 

Die folgenden Codierungs Parameter sind definiert.



| Codierungs Parameter                                                             | BESCHREIBUNG                                                                |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [MF- \_ transcode- \_ \_ Anfüge- \_ Encoder](mf-transcode-donot-insert-encoder.md) | Verhindert, dass die transcodieren-API einen Encoder für den Audiodatenstrom einfügt. |
| [MF- \_ transcode- \_ Codierungs Profil](mf-transcode-encodingprofile.md)             | Gibt die Konformitäts Vorlage für Geräte an. (Gilt nur für ASF-Dateien.)    |
| [MF- \_ transcode \_ qualityvsspeed](mf-transcode-qualityvsspeed.md)               | Gibt den Kompromiss zwischen Codierungsqualität und Geschwindigkeit an.                |



 

Sie müssen die Format Attribute festlegen. Die Codierungs Parameter sind optional.

Eine Möglichkeit, ein Format zu finden, das mit dem Encoder kompatibel ist, besteht darin, die Funktion [**mftranscodegetaudiooutputavailabletypes**](/windows/desktop/api/mfidl/nf-mfidl-mftranscodegetaudiooutputavailabletypes) aufzurufen. Der gewünschte Encoder wird durch den Untertyp angegeben. Die-Funktion gibt eine Auflistung von Medientypen für diesen Encoder zurück. Sie können einen Typ aus der Liste auswählen und die Attribute in das Profil kopieren. Beispielsweise Code, in dem dieser Ansatz verwendet wird, finden Sie unter [Tutorial: Codieren einer WMA-Datei](tutorial--converting-an-mp3-file-to-a-wma-file.md).

### <a name="video-attributes"></a>Video Attribute

Um Attribute für den Videostream hinzuzufügen, müssen Sie [**imftranscodeprofile:: setvideoattribute**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setvideoattributes)aufrufen. Diese Attribute geben an, wie der Videostream codiert wird. Wenn die Ausgabedatei keinen Videostream enthält, lassen Sie diese Attribute aus.

Wie bei audioattributen werden die Video Attribute in zwei Kategorien unterteilt:

-   Attribute, die das Format des codierten Streams angeben
-   Attribute, die andere Codierungs Parameter angeben.

Format Attribute sind Medientyp Attribute, wie im Abschnitt [Video Medientypen](video-media-types.md)beschrieben. Im folgenden finden Sie eine Liste mit typischen Videoformat Attributen:



| Format-Attribut                                                       | BESCHREIBUNG                                                      |
|------------------------------------------------------------------------|------------------------------------------------------------------|
| [MF- \_ MT- \_ Untertyp](mf-mt-subtype-attribute.md)                         | Der Untertyp. Siehe [Video Untertyp-GUIDs](video-subtype-guids.md). |
| [MF- \_ MT- \_ Frame \_ Rate](mf-mt-frame-rate-attribute.md)                  | Die Framerate.                                                  |
| [MF- \_ MT- \_ Frame \_ Größe](mf-mt-frame-size-attribute.md)                  | Die Frame Größe.                                                  |
| [**MF-mittlere mittlere \_ \_ \_ Bitrate**](mf-mt-avg-bitrate-attribute.md)            | Die durchschnittliche Bitrate.                                            |
| [Verhältnis der MF- \_ MT- \_ Pixel \_ Seite \_](mf-mt-pixel-aspect-ratio-attribute.md) | Das Pixel Seitenverhältnis.                                          |



 

Die folgenden Codierungs Parameter sind definiert.



| Codierungs Parameter                                                             | BESCHREIBUNG                                                                |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [MF- \_ transcode- \_ \_ Anfüge- \_ Encoder](mf-transcode-donot-insert-encoder.md) | Verhindert, dass die transcodieren-API einen Encoder für den Videostream einfügt. |
| [MF- \_ transcode- \_ Codierungs Profil](mf-transcode-encodingprofile.md)             | Gibt die Konformitäts Vorlage für Geräte an. (Gilt nur für ASF-Dateien.)    |
| [MF- \_ transcode \_ qualityvsspeed](mf-transcode-qualityvsspeed.md)               | Gibt den Kompromiss zwischen Codierungsqualität und Geschwindigkeit an.                |



 

Sie müssen die Format Attribute festlegen. Die Codierungs Parameter sind optional.

### <a name="container-attributes"></a>Container Attribute

Container Attribute definieren Eigenschaften auf Dateiebene der Ausgabedatei. Um Container Attribute festzulegen, müssen Sie [**imftranscodeprofile:: setcontainerattribute**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes)aufrufen. Die folgenden Attribute sind definiert.



| Attribut                                                                          | BESCHREIBUNG                                                                                                                                            |
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [\_transcode- \_ Anpassungs \_ Profil für MF](mf-transcode-adjust-profile.md)                  | Definiert die Datenstrom Einstellungen, die für die transcodieren-Topologie verwendet werden sollen. Sie können die Flags so festlegen, dass die Eingabe Quell Einstellungen verwendet oder benutzerdefinierte streamattribute verwendet werden. |
| [MF- \_ transcode- \_ ContainerType](mf-transcode-containertype.md)                     | Gibt das Dateiformat der Ausgabedatei an, z. b. MP4 oder ASF. Basierend auf diesem Wert wird der Topologie die entsprechende Medien Senke hinzugefügt.            |
| [MF- \_ transcode \_ Skip- \_ \_ metadatenübertragung](mf-transcode-skip-metadata-transfer.md) | Gibt an, ob Metadaten aus der Quelle in die Ausgabedatei kopiert werden.                                                                               |
| [MF- \_ transcode- \_ topologymode](mf-transcode-topologymode.md)                       | Gibt an, ob während der Transcodierung hardwarebasierte Codecs verwendet werden dürfen.                                                                                |
| [MFT \_ fieldofuse \_ Unlock- \_ Attribut](mft-fieldofuse-unlock-attribute.md)          | Entsperrt einen Codec mit Einschränkungen für das Feld. Weitere Informationen finden Sie unter [Einschränkungen](field-of-use-restrictions.md)für das Feld "Verwendung".              |



 

Das MF-Attribut " [ \_ \_ ContainerType](mf-transcode-containertype.md) " ist erforderlich. Die anderen Container Attribute sind optional.

## <a name="creating-a-transcode-topology"></a>Erstellen einer transcode-Topologie

Die transcodieren-Topologie ist eine partielle Topologie, die die Medienquelle, die entsprechenden Codecs und die Medien Senke enthält. Um die transcodieren-Topologie zu erstellen, rufen Sie die [**mfkreatetranscodetopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodetopology) -Funktion auf. Diese Funktion übernimmt die folgenden Parameter als Eingabe:

-   Ein Zeiger auf die [**imfmediasource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) -Schnittstelle der Medienquelle.
-   Der Name der Ausgabedatei.
-   Ein Zeiger auf die [**imftranscodeprofile**](/windows/desktop/api/mfidl/nn-mfidl-imftranscodeprofile) -Schnittstelle des transcodieren-Profils.

Die-Funktion gibt einen Zeiger auf die [**imftopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) -Schnittstelle zurück.

## <a name="running-the-encoding-session"></a>Ausführen der Codierungs Sitzung

Nachdem Sie die Topologie erstellt haben, können Sie die Datei codieren. Sie können das Profil zu diesem Zeitpunkt verwerfen.

1.  Rufen Sie [**mfkreatemediasession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) auf, um die Medien Sitzung zu erstellen.
2.  Wenden Sie [**imfmediasession:: settopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) an, um die Topologie für die Medien Sitzung festzulegen.
3.  Zum Starten der Codierungs Sitzung wird [**imfmediasession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) aufgerufen.
4.  Warten Sie auf das Ereignis [mesessionend](mesessionended.md) .
5.  [**Imfmediasession:: Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) wird aufgerufen, um die Medien Sitzung zu schließen.
6.  Warten Sie auf das Ereignis [mesessionclosed](mesessionclosed.md) .
7.  Nennen Sie [**imfmediasource:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown).
8.  Rückrufe [**imfmediasession:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown).

Der meiste Zeitaufwand für die Codierung erfolgt zwischen den Schritten 3 und 4.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Transcode-API](transcode-api.md)
</dt> <dt>

[Informationen zur Medien Sitzung](about-the-media-session.md)
</dt> </dl>

 

 



