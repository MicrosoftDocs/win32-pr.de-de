---
description: Jede ASF-Datei enthält mindestens einen Datenstrom. Das ASF-Profilobjekt stellt eine Auflistung von ASF-Streams dar. Für die ASF-Codierung müssen Sie die Datenströme erstellen und konfigurieren, die Sie codieren möchten.
ms.assetid: cc89e8bc-58ff-48e2-9668-0dcd6cfd25e1
title: Erstellen und Konfigurieren von ASF-Streams
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58c780de3fa0abb5db29e3e5e5ed049b78aca7898966e8f7e8595b504804da91
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118743238"
---
# <a name="creating-and-configuring-asf-streams"></a>Erstellen und Konfigurieren von ASF-Streams

Jede ASF-Datei enthält mindestens einen Datenstrom. Das [ASF-Profilobjekt](asf-profile.md) stellt eine Auflistung von ASF-Streams dar. Für die ASF-Codierung müssen Sie die Datenströme erstellen und konfigurieren, die Sie codieren möchten.

Eine Anwendung kann die folgenden Aufgaben mit dem ASF-Profilobjekt ausführen:

-   Hinzufügen oder Entfernen eines Streams.
-   Rufen Sie die Konfigurationseinstellungen eines Streams ab.
-   Konfigurieren sie Nutzlasterweiterungen.
-   Fügen Sie ein ASF-Objekt für gegenseitigen Ausschluss hinzu, entfernen oder ändern Sie es.

Dieses Thema enthält folgende Abschnitte:

-   [Erstellen eines neuen Streams](#creating-a-new-stream)
-   [Zuweisen von Streamnummern](#assigning-stream-numbers)
-   [Festlegen von "Leaky Bucket"-Werten](#setting-leaky-bucket-values)
-   [Nutzlasterweiterungen](#payload-extensions)
-   [Hinzufügen eines Streams zum Profil](#adding-a-stream-to-the-profile)
-   [Zugehörige Themen](#related-topics)

## <a name="creating-a-new-stream"></a>Erstellen eines neuen Streams

Ein ASF-Profilobjekt muss Konfigurationseinstellungen für mindestens einen ASF-Datenstrom enthalten. Jeder Stream wird durch ein *Streamkonfigurationsobjekt* dargestellt, das die [**IMFASFStreamConfig-Schnittstelle**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) verfügbar macht. Die Informationen im Streamkonfigurationsobjekt entsprechen dem Streameigenschaftenobjekt und den Objekten für erweiterte Streameigenschaften im ASF-Dateiheader. (Siehe [ASF-Dateistruktur](asf-file-structure.md).)

Führen Sie die folgenden Schritte aus, um einem ASF-Profil einen Stream hinzuzufügen:

1.  Erstellen Sie ein leeres Streamstreamkonfigurationsobjekt.
2.  Konfigurieren Sie den Stream gemäß den Anforderungen der Anwendung.
3.  Fügen Sie den Datenstrom dem Profil hinzu.

Um einen Stream für das Profil zu erstellen, rufen [**Sie IMFASFProfile::CreateStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-createstream) auf, um ein leeres Streamkonfigurationsobjekt zu erstellen und den Zeiger im *ppIStream-Parameter* zu empfangen. **CreateStream** muss den Typ des zu erstellende Streams kennen. Die gängigsten Arten von Streams, die in ASF-Dateien verwendet werden, sind Audio- und Videostreams. In Media Foundation werden die Streamtypen durch das Medientypobjekt gekennzeichnet, das die [**INTERFACESMediaType-Schnittstelle**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) verfügbar macht. Der Haupttyp des Medientyps definiert die Kategorie des digitalen Mediendatenstroms, z. B. Audio oder Video. Der Untertyp definiert das Format des Haupttyps. Der von **CreateStream** festgelegte anfängliche Medientyp kann mithilfe des Streamkonfigurationsobjekts geändert werden. Um den Medientyp für den Stream abzurufen, rufen Sie [**IMFASFStreamConfig::GetMediaType**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getmediatype) auf, oder rufen Sie den Haupttyp [**IMFASFStreamConfig::GetStreamType**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getstreamtype)auf. Der anfängliche Medientyp für einen Stream kann durch einen neuen konfigurierten Medientyp ersetzt werden, indem [**IMFASFStreamConfig::SetMediaType**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-setmediatype)aufgerufen wird.

Wenn eine Anwendung ein Profil aus einem gültigen Präsentationsdeskriptor erstellt, indem [**MFCreateASFProfileFromPresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofilefrompresentationdescriptor)aufgerufen wird. Die Funktion legt automatisch die Streamkonfigurationsobjekte für jeden Datenstrom fest und legt sie im Profil fest. Die Streammedientypen werden basierend auf den Streamdeskriptoren festgelegt, die dem Präsentationsdeskriptor zugeordnet sind.

## <a name="assigning-stream-numbers"></a>Zuweisen von Streamnummern

Streams aller Typen muss eine Streamnummer zugewiesen werden. Streamnummern müssen nicht sequenziell sein, sondern im Bereich von 1 bis 127 liegen. Um Streamnummern zuzuweisen, rufen Sie [**IMFASFStreamConfig::SetStreamNumber auf.**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-setstreamnumber) Um den Aufruf der Streamnummer abzurufen, [**imfasfStreamConfig::GetStreamNumber**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getstreamnumber).

> [!Note]  
> Eine Streamnummer unterscheidet sich von einem Streamindex, den Sie beim Abrufen von Datenströmen in einem Profil mit [**IMFASFProfile::GetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstream)verwenden. Der Streamindex ist eine Zahl, die dem Stream vom Profilobjekt zugewiesen wird. Streamindizes liegen zwischen 0 und 1 kleiner als die Anzahl von Streams, die von [**IMFASFProfile::GetStreamCount**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstreamcount)abgerufen werden. Sie können auch einen Stream aus dem Profil nach Streamnummer abrufen, indem [**Sie IMFASFProfile::GetStreamByNumber**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstreambynumber)aufrufen.

 

## <a name="setting-leaky-bucket-values"></a>Festlegen von "Leaky Bucket"-Werten

Jedem Datenstromkonfigurationsobjekt, das einen Stream darstellt, müssen parameter, bit rate und buffer window -Werte zugeordnet sein.

Diese Werte sind für die Anwendung über das [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET1-Attribut**](mf-asfstreamconfig-leakybucket1-attribute.md) und das [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET2-Attribut**](mf-asfstreamconfig-leakybucket2-attribute.md) verfügbar. Bei der Dateicodierung hängen die tatsächlichen Werte vom Typ der Codierung ab und werden vom Encoder festgelegt. Wenn Sie bereits über einen konfigurierten Encoder verfügen und der Ausgabetyp für den Encoder festgelegt ist, muss die Anwendung den Encoder nach den Parametern für den verlustbewerten Bucket abfragen und die Werte in diesen Attributen festlegen.

Wenn Sie die Komponenten der Pipelineebene verwenden und die Streams für die ASF-Mediensenke konfigurieren, verfügen Sie wahrscheinlich nicht über einen konfigurierten Encoder. In diesem Fall müssen Sie den Nachmedientyp des Encoders abfragen und den aktualisierten Wert in der [**MFPKEY \_ ASFSTREAMSINK \_ CORRECTED \_ LEAKYBUCKET-Eigenschaft**](mfpkey-asfstreamsink-corrected-leakybucket-property.md) des Eigenschaftenspeichers der ASF-Mediensenke festlegen. Der Codierungseigenschaftenspeicher wird über den des ContentInfo-Objekts abgerufen, das dem Profil zugeordnet ist. Die aktualisierten Werte werden automatisch in den Attributwerten des datenverlustbesendigen Buckets des Streams widergespiegelt. Allgemeine Informationen zu leaky-Buckets und zum Abrufen des Werts für den verlustbeleckten Bucket aus dem Encoder finden Sie unter The Leaky Bucket Buffer Model ( [The Leaky Bucket Buffer Model).](the-leaky-bucket-buffer-model.md)

## <a name="payload-extensions"></a>Nutzlasterweiterungen

Mediendaten für die Streams werden dem ASF-Datenobjekt als [Medienbeispiele](media-samples.md) vom [ASF Multiplexer](asf-multiplexer.md)hinzugefügt. Diese Medienbeispiele können Nutzlasterweiterungsdaten enthalten: SMPTE-Zeitcodedaten, seitenfremdes Pixelverhältnis, Samplingdauer und, wenn das Beispiel sie enthält, einen Videoschlüsselrahmen. Eine Liste der unterstützten Nutzlasterweiterungstypen finden Sie unter [ASF-Nutzlasterweiterungs-GUIDs.](asf-payload-extension-guids.md)

Ein Stream muss so konfiguriert werden, dass die Nutzlasterweiterung akzeptiert wird, damit der Multiplexer während der Generierung der Stichproben die ergänzenden Daten jedem Beispiel für diesen Stream hinzufügen kann.

Um die Gesamtzahl der im Stream festgelegten Nutzlasterweiterungen abzurufen, rufen [**Sie IMFASFStreamConfig::GetPayloadExtensionCount**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getpayloadextensioncount) auf, und listen Sie dann die Liste auf, indem Sie [**IMFASFStreamConfig::GetPayloadExtension**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getpayloadextension)aufrufen. Um eine Nutzlasterweiterung für den Stream hinzuzufügen, rufen Sie [**IMFASFStreamConfig::AddPayloadExtension**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-addpayloadextension)auf. Dadurch werden zusätzliche Daten zu einzelnen Medienbeispielen hinzugefügt, die für den Stream generiert werden.

Um vorhandene Nutzlasterweiterungen zu entfernen, die dem Stream zugeordnet sind, rufen Sie [**IMFASFStreamConfig::RemoveAllPayloadExtensions**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-removeallpayloadextensions)auf.

## <a name="adding-a-stream-to-the-profile"></a>Hinzufügen eines Streams zum Profil

Nachdem ein Stream konfiguriert wurde, rufen Sie [**IMFASFProfile::SetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-setstream) auf, um den Stream dem Profil hinzuzufügen.

Um einen vorhandenen Stream im Profil zu entfernen, rufen Sie [**IMFASFProfile::RemoveStream auf.**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-removestream)

Das konfigurierte Profil muss für das ContentInfo-Objekt durch Aufrufen von [**IMFASFContentInfo::SetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile)festgelegt werden. Wenn Sie Änderungen an einem vorhandenen Stream vornehmen, müssen Sie ihn erneut dem Profil hinzufügen und das Profil für das ContentInfo-Objekt festlegen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ASF-Profil](asf-profile.md)
</dt> <dt>

[ASF-Unterstützung in Media Foundation](asf-support-in-media-foundation.md)
</dt> <dt>

[WMContainer ASF-Komponenten](wmcontainer-asf-components.md)
</dt> </dl>

 

 



