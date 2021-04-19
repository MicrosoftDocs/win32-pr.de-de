---
description: Jede ASF-Datei enthält mindestens einen Stream. Das ASF-Profil Objekt stellt eine Auflistung von ASF-Streams dar. Bei der ASF-Codierung müssen Sie die Datenströme erstellen und konfigurieren, die Sie codieren möchten.
ms.assetid: cc89e8bc-58ff-48e2-9668-0dcd6cfd25e1
title: Erstellen und Konfigurieren von ASF-Streams
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8eabce588022dd66947f34e4dcd9db61f26448b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344640"
---
# <a name="creating-and-configuring-asf-streams"></a>Erstellen und Konfigurieren von ASF-Streams

Jede ASF-Datei enthält mindestens einen Stream. Das [ASF-Profil](asf-profile.md) Objekt stellt eine Auflistung von ASF-Streams dar. Bei der ASF-Codierung müssen Sie die Datenströme erstellen und konfigurieren, die Sie codieren möchten.

Eine Anwendung kann die folgenden Aufgaben mit dem Objekt "ASF-Profil" ausführen:

-   Hinzufügen oder Entfernen eines Streams.
-   Abrufen der Konfigurationseinstellungen eines Streams.
-   Konfigurieren Sie Nutz Last Erweiterungen.
-   Fügen Sie ein gegenseitiges ASF-Ausschluss Objekt hinzu, entfernen oder ändern Sie es.

Dieses Thema enthält folgende Abschnitte:

-   [Erstellen eines neuen Streams](#creating-a-new-stream)
-   [Zuweisen von streamnummern](#assigning-stream-numbers)
-   [Festlegen von Leaky-Bucket-Werten](#setting-leaky-bucket-values)
-   [Nutz Last Erweiterungen](#payload-extensions)
-   [Hinzufügen eines Datenstroms zum Profil](#adding-a-stream-to-the-profile)
-   [Zugehörige Themen](#related-topics)

## <a name="creating-a-new-stream"></a>Erstellen eines neuen Streams

Ein ASF-Profil Objekt muss Konfigurationseinstellungen für mindestens einen ASF-Stream enthalten. Jeder Stream wird durch ein Daten *Strom-Konfigurations* Objekt dargestellt, das die [**imfasf streamconfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) -Schnittstelle verfügbar macht. Die Informationen im Datenstrom-Konfigurationsobjekt entsprechen dem Stream Properties-Objekt und den erweiterten Stream Properties-Objekten im ASF-Dateiheader. (Siehe [Struktur der ASF-Datei](asf-file-structure.md).)

Um einem ASF-Profil einen Stream hinzuzufügen, führen Sie die folgenden Schritte aus:

1.  Erstellen Sie ein leeres Stream-Datenstrom-Konfigurationsobjekt.
2.  Konfigurieren Sie den Stream gemäß den Anforderungen der Anwendung.
3.  Fügen Sie den Stream zum Profil hinzu.

Um einen Stream für das Profil zu erstellen, rufen Sie [**imfasfprofile:: kreatestream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-createstream) auf, um ein leeres Datenstrom-Konfigurationsobjekt zu erstellen und den Zeiger im *ppIStream* -Parameter zu empfangen. " **Foratestream** " muss den Typ des zu erstellenden Streams kennen. Die gängigsten Typen von Streams, die in ASF-Dateien verwendet werden, sind Audiodaten und Videodaten Ströme. In Media Foundation werden die Streamtypen durch das Medientyp Objekt gekennzeichnet, das die [**IMF MediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) -Schnittstelle verfügbar macht. Der Haupttyp des Medientyps definiert die Kategorie des Datenstroms für digitale Medien, z. b. Audiodaten oder Videos. Der Untertyp definiert das Format des Haupt Typs. Der von " **kreatestream** " festgelegte erste Medientyp kann mit dem "Stream Configuration"-Objekt geändert werden. Um den Medientyp für den Stream abzurufen, rufen Sie [**imfasfstreamconfig:: getmediatype**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getmediatype) auf, oder rufen Sie den Haupttyp " [**imfasfstreamconfig:: getstreamtype**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getstreamtype)" ab. Der erste Medientyp für einen Datenstrom kann durch einen neuen konfigurierten Medientyp ersetzt werden, indem [**imfasfstreamconfig:: setmediatype**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-setmediatype)aufgerufen wird.

Wenn eine Anwendung ein Profil aus einem gültigen Präsentations Deskriptor erstellt, indem Sie [**mfcreateasfprofilefrompresentationdescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofilefrompresentationdescriptor)aufrufen. Die Funktion legt automatisch die Datenstrom-Konfigurationsobjekte für jeden der Streams fest und legt Sie für das Profil fest. Die Datenstrom-Medientypen werden basierend auf den Datenstrom Deskriptoren festgelegt, die dem Präsentations Deskriptor zugeordnet sind.

## <a name="assigning-stream-numbers"></a>Zuweisen von streamnummern

Streams aller Typen müssen eine streamnummer zugewiesen werden. Streamnummern müssen nicht sequenziell sein, müssen jedoch zwischen 1 und 127 liegen. Um streamnummern zuzuweisen, nennen Sie [**imfasfstreamconfig:: setstreamnumber**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-setstreamnumber). Zum Abrufen des Datenstrom Nummern Aufrufes [**imfasfstreamconfig:: getstreamnumber**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getstreamnumber).

> [!Note]  
> Eine streamnummer unterscheidet sich von einem streamindex, den Sie verwenden, wenn Sie Datenströme in einem Profil mithilfe von [**imfasf profile:: GetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstream)erhalten. Der streamindex ist eine Zahl, die dem Stream vom Profil Objekt zugewiesen wird. Streamindexe liegen zwischen 0 und eins kleiner als die Anzahl von Datenströmen, die von [**imfasfprofile:: getstreamcount**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstreamcount)abgerufen wurden. Sie können auch einen Stream aus dem Profil anhand der streamnummer abrufen, indem Sie [**imfasfprofile:: getstreambynumber**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstreambynumber)aufrufen.

 

## <a name="setting-leaky-bucket-values"></a>Festlegen von Leaky-Bucket-Werten

Jedem Datenstrom-Konfigurationsobjekt, das einen Stream darstellt, müssen die Werte für die Parameter "Leaky Bucket", "Bitrate" und "Puffer Fenster

Diese Werte sind für die Anwendung über das [**MF \_ asfstreamconfig \_ LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) -Attribut und das [**MF \_ asfstreamconfig \_ LEAKYBUCKET2**](mf-asfstreamconfig-leakybucket2-attribute.md) -Attribut verfügbar. Bei der Datei Codierung sind die tatsächlichen Werte vom Codierungstyp abhängig und werden vom Encoder festgelegt. Wenn Sie bereits über einen konfigurierten Encoder verfügen und der Ausgabetyp für den Encoder festgelegt ist, muss die Anwendung den Encoder nach den Parametern für den Leaky-Bucket Abfragen und die Werte in diesen Attributen festlegen.

Wenn Sie die Komponenten der Pipeline Schicht verwenden und die Datenströme für die ASF-Medien Senke konfigurieren, haben Sie wahrscheinlich keinen konfigurierten Encoder. In diesem Fall müssen Sie den Encoder nach dem Medientyp Aushandlungen Abfragen und den aktualisierten Wert in der Eigenschaft [**mfpkey \_ asfstreamsink \_ korrigiert \_ leakybucket**](mfpkey-asfstreamsink-corrected-leakybucket-property.md) des Eigenschaften Speichers der ASF-Medien Senke festlegen. Der Encoding-Eigenschaften Speicher wird durch die des ContentInfo-Objekts abgerufen, das dem Profil zugeordnet ist. Die aktualisierten Werte werden automatisch in den Attributwerten für den Leaky-Bucket des Streams widergespiegelt. Allgemeine Informationen zu Lecks und zum Ermitteln des Lecks-bucketwerts aus dem Encoder finden Sie unter The [Leaky Bucket Buffer Model](the-leaky-bucket-buffer-model.md).

## <a name="payload-extensions"></a>Nutz Last Erweiterungen

Mediendaten für die Streams werden dem ASF-Datenobjekt vom [ASF Multiplexer](asf-multiplexer.md)als [Medien Beispiele](media-samples.md) hinzugefügt. Diese Medien Beispiele können Nutz Last Erweiterungs Daten enthalten: SMPTE Time Code Data, Non-Square Pixel Page Ratio, Sample Duration, und wenn das Beispiel dieses enthält, ein Video Keyframe. Eine Liste der unterstützten Nutz Last Erweiterungs Typen finden Sie unter die [GUIDs der ASF-Nutz Last Erweiterung](asf-payload-extension-guids.md).

Ein Datenstrom muss so konfiguriert werden, dass er die Nutz Last Erweiterung annimmt, damit der Multiplexer während der Stichproben Generierung die ergänzenden Daten den einzelnen Beispielen für diesen Stream hinzufügen kann.

Rufen Sie zum Abrufen der Gesamtanzahl der für den Stream festgelegten Nutz Last Erweiterungen [**imfasfstreamconfig:: getpayloadextensioncount**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getpayloadextensioncount) auf, und Listen Sie die Liste dann durch Aufrufen von [**imfasfstreamconfig:: getpayloadextension**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getpayloadextension)auf. Um die Nutz Last Erweiterung für den Stream hinzuzufügen, nennen Sie [**imfasfstreamconfig:: addpayloadextension**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-addpayloadextension). Dadurch werden den einzelnen Medien Beispielen, die für den Stream generiert werden, zusätzliche Daten hinzugefügt.

Um vorhandene Nutz Last Erweiterungen zu entfernen, die dem Stream zugeordnet sind, müssen Sie [**imfasfstreamconfig:: removeallpayloadextensions**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-removeallpayloadextensions)aufrufen.

## <a name="adding-a-stream-to-the-profile"></a>Hinzufügen eines Datenstroms zum Profil

Nachdem ein Stream konfiguriert wurde, müssen Sie [**imfasfprofile:: setStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-setstream) aufrufen, um den Stream zum Profil hinzuzufügen.

Um einen vorhandenen Stream im Profil zu entfernen, nennen Sie [**imfasfprofile:: removestream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-removestream).

Das konfigurierte Profil muss für das ContentInfo-Objekt festgelegt werden, indem [**imfasfcontentinfo:: setprofile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile)aufgerufen wird. Wenn Sie Änderungen an einem vorhandenen Stream vornehmen, müssen Sie ihn erneut zum Profil hinzufügen und das Profil für das ContentInfo-Objekt festlegen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ASF-Profil](asf-profile.md)
</dt> <dt>

[Unterstützung von ASF in Media Foundation](asf-support-in-media-foundation.md)
</dt> <dt>

[Wmcontainer-ASF-Komponenten](wmcontainer-asf-components.md)
</dt> </dl>

 

 



