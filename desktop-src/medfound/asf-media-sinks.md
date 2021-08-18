---
description: Die ASF-Mediensenke ist die letzte Komponente in der Codierungspipeline, die es einer Anwendung ermöglicht, eine ASF-Datei zu schreiben.
ms.assetid: 65bb8822-5eb0-46a3-ab9e-c55ae466e982
title: ASF-Mediensenken
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50af8530b1c2b8d9131243cafa67e841289cbbe0691cfcb499b57df68b60b141
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118744211"
---
# <a name="asf-media-sinks"></a>ASF-Mediensenken

Die ASF-Mediensenke ist die letzte Komponente in der Codierungspipeline, die es einer Anwendung ermöglicht, eine ASF-Datei zu schreiben.

Media Foundation stellt zwei Arten von ASF-Mediensenken bereit:

-   *Die ASF-Dateisenke* wird verwendet, um ASF-Mediendaten in einer Datei zu archivieren.
-   *Die ASF-Streamingsenke* wird verwendet, um ASF-Inhalte in einen Bytestream zu schreiben, der über das Netzwerk gestreamt werden kann.

ASF-Mediensenken enthalten mindestens eine Streamsenke, die die Daten darstellt, die für jeden Stream in der ASF-Ausgabedatei geschrieben werden sollen. Für Codierungsanwendungen, die auf Windows Vista ausgeführt werden, müssen Sie die Codierungstopologie manuell konfigurieren, indem Sie die ASF-Mediensenke erstellen und konfigurieren und sie dann der Topologie hinzufügen. Wenn Sie in Windows 7 die objekte für die schnelle Transcodierung verwenden, um die Topologie zu erstellen, haben Sie die Mediensenke nicht direkt erstellt, und die Anwendung ruft keine Methoden in der Mediensenke oder einer der Streamsenken auf. Die schnellen Transcodierungsobjekte instanziieren die erforderlichen Mediensenken und fügen sie der Topologie hinzu, bevor ein Verweis auf die Aufrufende Anwendung zurückgegeben wird. Für schnelle Transcodierungsobjekte gelten jedoch einige Einschränkungen, die vom Typ der Codierung abhängen.

-   [ASF-Mediensenkenobjektmodell](#asf-media-sink-object-model)
-   [ASF-Dateisenke](#asf-file-sink)
-   [Zugehörige Themen](#related-topics)

## <a name="asf-media-sink-object-model"></a>ASF-Mediensenkenobjektmodell

ASF-Mediensenken implementieren die [**INTERFACESMediaSink-Schnittstelle**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) und machen die folgenden Schnittstellen verfügbar. Eine Anwendung kann einen Verweis auf diese Schnittstellen abrufen, indem [**sie QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) für die ASF-Mediensenke aufruft, die sie zum Generieren von Ausgabebeispielen verwendet.



| Schnittstelle                                                  | BESCHREIBUNG                                                                                                                                                                                            |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WFMEDIASink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink)                       | Erforderlich für alle Mediensenken.                                                                                                                                                                          |
| [**PAULOFinalizableMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imffinalizablemediasink) | Wird von der ASF-Dateisenke implementiert, die den generierten Medieninhalt in eine Datei schreibt. Sie können die Methoden auf dieser Schnittstelle verwenden, um Daten zu leeren und das ASF-Headerobjekt der endgültigen Ausgabedatei zu aktualisieren. |
| [**ÜBER DIE UHRClockStateSink**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink)             | Empfängt Statusänderungsbenachrichtigungen von der Präsentationsuhr.                                                                                                                                       |
| [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo)             | Das ASF ContentInfo-Objekt ist ein WMContainer-Objekt auf Ebene, in dem hauptsächlich ASF-Headerobjektinformationen gespeichert werden. Dies wird verwendet, um ASF-Mediensenken zu erstellen.                                                     |
| [**VERINNUNGMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata)                         | Wird verwendet, um die Metadaten für die ASF-Datei zu beschreiben.                                                                                                                                                        |
| [**PILLARMetadataProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider)         | Ruft eine Auflistung von Metadaten ab, entweder für eine gesamte Präsentation oder für einen Stream in der Präsentation.                                                                                          |



 

## <a name="asf-file-sink"></a>ASF-Dateisenke

Die ASF-Dateisenke ist eine Implementierung von [**VONMEDIASink,**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) die von Media Foundation bereitgestellt wird, die eine Anwendung zum Archivieren von ASF-Mediendaten in einer Datei verwenden kann.

Sie müssen Methoden für die Dateisenke oder eine ihrer Streamsenken erstellen, konfigurieren und aufrufen, wenn Sie die Pipelineebenenobjekte verwenden, um eine neue ASF-Datei zu schreiben. Nach dem Konfigurieren der Dateisenke können Sie sie der Codierungspipeline hinzufügen.

Hier sind die allgemeinen Schritte für die Verwendung der ASF-Dateisenke:

1.  Erstellen Sie die Dateisenke in-process oder out-of-process.
2.  Konfigurieren Sie die Dateisenke mit allen Datenströmen, Codierungseigenschaften und Metadateninformationen.
3.  Ordnen Sie die Dateisenke dem Ausgabetopologieknoten zu, indem Sie entweder die Streamsenken aufzählen oder die Datenstromnummern mit in der Senke nachverfolgen.

Die folgenden Themen enthalten ausführliche Informationen zum Arbeiten mit der ASF-Dateisenke:

-   [Erstellen der ASF-Dateisenke](creating-the-asf-file-sink.md)
-   [Hinzufügen von Streaminformationen zur ASF-Dateisenke](adding-stream-information-to-the-asf-file-sink.md)
-   [Festlegen von Eigenschaften in der Dateisenke](setting-properties-in-the-file-sink.md)
-   [Hinzufügen von Metadaten zur Dateisenke](adding-metadata-to-the-file-sink.md)
-   [Das Puffermodell "Leaky Bucket"](the-leaky-bucket-buffer-model.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ASF-Komponenten auf Pipelineebene](pipeline-layer-asf-components.md)
</dt> <dt>

[ASF-Unterstützung in Media Foundation](asf-support-in-media-foundation.md)
</dt> </dl>

 

 
