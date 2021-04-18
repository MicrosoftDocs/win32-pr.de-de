---
description: Die ASF-Medien Senke ist die letzte Komponente in der Codierungs Pipeline, die es einer Anwendung ermöglicht, eine ASF-Datei zu schreiben.
ms.assetid: 65bb8822-5eb0-46a3-ab9e-c55ae466e982
title: ASF-Medien senken
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d6bcd3e6b91403185342607e8c4374eb32069c7
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106365234"
---
# <a name="asf-media-sinks"></a>ASF-Medien senken

Die ASF-Medien Senke ist die letzte Komponente in der Codierungs Pipeline, die es einer Anwendung ermöglicht, eine ASF-Datei zu schreiben.

Media Foundation bietet zwei Arten von ASF-Medien senken:

-   Die *ASF-Datei-Senke* wird zum Archivieren von ASF-Mediendaten in einer Datei verwendet.
-   Mit der *ASF-streamingsenke* werden ASF-Inhalte in einem Bytestream geschrieben, der über das Netzwerk gestreamt werden kann.

ASF-Medien senken enthalten mindestens einen streamsenken, der die Daten darstellt, die für jeden Stream in der Ausgabe-ASF-Datei geschrieben werden sollen. Zum Codieren von Anwendungen, die unter Windows Vista ausgeführt werden, müssen Sie die Codierungs Topologie manuell konfigurieren, indem Sie die ASF-Medien Senke erstellen und konfigurieren und Sie dann der Topologie hinzufügen. Wenn Sie in Windows 7 die fast-transcodieren-Objekte zum Erstellen der Topologie verwenden, ist es nicht möglich, die Medien Senke direkt zu erstellen, und die Anwendung ruft keine Methoden für die Medien Senke oder einen der streamsenken auf. Die schnellen transcodieren-Objekte instanziieren die erforderlichen Medien senken und fügen Sie der Topologie hinzu, bevor ein Verweis auf die aufruferanwendung zurückgegeben wird. Bei schnellen transcodeobjekten gibt es jedoch einige Einschränkungen, die je nach Codierungstyp zutreffen.

-   [ASF-Medien-Sink-Objektmodell](#asf-media-sink-object-model)
-   [ASF-Datei Senke](#asf-file-sink)
-   [Zugehörige Themen](#related-topics)

## <a name="asf-media-sink-object-model"></a>ASF-Medien-Sink-Objektmodell

ASF-Medien senken implementieren die [**imfmediasink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) -Schnittstelle und machen die folgenden Schnittstellen verfügbar. Eine Anwendung kann einen Verweis auf diese Schnittstellen abrufen, indem Sie [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) auf der ASF-Medien Senke aufrufen, die Sie zum Erstellen von Ausgabe Beispielen verwendet.



| Schnittstelle                                                  | BESCHREIBUNG                                                                                                                                                                                            |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Imfmediasink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink)                       | Erforderlich für alle Medien senken.                                                                                                                                                                          |
| [**Imffinalizablemediasink**](/windows/desktop/api/mfidl/nn-mfidl-imffinalizablemediasink) | Wird von der ASF-Datei-Senke implementiert, die den generierten Medieninhalt in eine Datei schreibt. Sie können die Methoden auf dieser Schnittstelle verwenden, um Daten zu leeren und das ASF-Header Objekt der endgültigen Ausgabedatei zu aktualisieren. |
| [**IMF-staatink**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink)             | Empfängt Zustands Änderungs Benachrichtigungen von der Präsentations Uhr.                                                                                                                                       |
| [**Imfasf ContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo)             | Das Objekt "ASF ContentInfo" ist ein wmcontainersetobjekt, das hauptsächlich Informationen des ASF-Header Objekts speichert Diese dient zum Erstellen von ASF-Medien senken.                                                     |
| [**IMF-Metadaten**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata)                         | Wird verwendet, um die Metadaten für die ASF-Datei zu beschreiben.                                                                                                                                                        |
| [**IMFMetadataProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider)         | Ruft eine Auflistung von Metadaten entweder für eine gesamte Präsentation oder für einen Datenstrom in der Präsentation ab.                                                                                          |



 

## <a name="asf-file-sink"></a>ASF-Datei Senke

Die ASF-Datei Senke ist eine Implementierung von [**imfmediasink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) , die von Media Foundation bereitgestellt wird, die eine Anwendung zum Archivieren von ASF-Mediendaten in einer Datei verwenden kann.

Wenn Sie die Pipeline Schicht Objekte verwenden, um eine neue ASF-Datei zu schreiben, müssen Sie Methoden für die dateisenke oder einen der zugehörigen streamsenken erstellen, konfigurieren und aufzurufen. Nachdem Sie die Datei Senke konfiguriert haben, können Sie Sie der Codierungs Pipeline hinzufügen.

Im folgenden finden Sie die allgemeinen Schritte zum Verwenden der ASF-Datei-Senke:

1.  Erstellen Sie die Datei-Senke in-Process oder out-of-Process.
2.  Konfigurieren Sie die Datei Senke für alle Streams, Codierungs Eigenschaften und Metadateninformationen.
3.  Ordnen Sie die Datei Senke dem Knoten Ausgabe Topologie zu, indem Sie entweder die streamsenken aufzählen oder die streamnummern in der Senke nachverfolgen.

Die folgenden Themen enthalten ausführliche Informationen zum Arbeiten mit der ASF-Datei-Senke:

-   [Erstellen der ASF-Datei-Senke](creating-the-asf-file-sink.md)
-   [Hinzufügen von streaminformationen zur ASF-Datei-Senke](adding-stream-information-to-the-asf-file-sink.md)
-   [Festlegen von Eigenschaften in der Datei Senke](setting-properties-in-the-file-sink.md)
-   [Hinzufügen von Metadaten zur Datei Senke](adding-metadata-to-the-file-sink.md)
-   [Das Leaky Bucket-Puffer Modell](the-leaky-bucket-buffer-model.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Komponenten der Pipeline Schicht-ASF](pipeline-layer-asf-components.md)
</dt> <dt>

[Unterstützung von ASF in Media Foundation](asf-support-in-media-foundation.md)
</dt> </dl>

 

 
