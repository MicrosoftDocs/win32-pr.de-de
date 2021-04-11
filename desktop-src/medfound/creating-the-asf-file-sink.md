---
description: Die ASF-Datei Senke ist eine Implementierung von imfmediasink, die von Media Foundation bereitgestellt wird, die eine Anwendung zum Archivieren von ASF-Mediendaten in einer Datei verwenden kann. Weitere Informationen zum Objektmodell der ASF-Medien senken und zur allgemeinen Verwendung finden Sie unter ASF-Medien senken.
ms.assetid: 991f3345-a6b4-45c2-a89d-3c13c70b6bbc
title: Erstellen der ASF-Datei-Senke
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c43625bcbc581b4967d4db99cef71a0fc779f070
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127944"
---
# <a name="creating-the-asf-file-sink"></a>Erstellen der ASF-Datei-Senke

Die ASF-Datei Senke ist eine Implementierung von [**imfmediasink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) , die von Media Foundation bereitgestellt wird, die eine Anwendung zum Archivieren von ASF-Mediendaten in einer Datei verwenden kann. Weitere Informationen zum Objektmodell und zur allgemeinen Verwendung von ASF Medien senken finden Sie unter [ASF-Medien senken](asf-media-sinks.md).

Es gibt zwei Möglichkeiten zum Erstellen einer Instanz der ASF-Datei-Senke. Sie können [**mfkreateasfmediasink**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink) oder [**mfkreateasfmediasinkaktivierungs**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate)aufrufen.

Wenn Sie [**mfkreateasfmediasink**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink)aufrufen, müssen Sie für die Ausgabedatei einen Bytestream angeben, in den die Senke den ASF-Inhalt während einer Codierungs Sitzung schreibt. Der angegebene Bytestream muss über suchbare und beschreibbare Funktionen verfügen. andernfalls schlägt der **mfkreateasfmediasink** -Aufruf mit dem Fehlercode "E Fail" fehl \_ . Dieser Befehl erstellt ein in-Process-dateisink-Objekt und gibt einen Zeiger auf die [**imfmediasink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) -Schnittstelle der File-Senke zurück.

Wenn Sie [**mfkreateasfmediasinkaktivierungs**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate)aufrufen, müssen Sie die URL der Ausgabedatei angeben, in die die dateisenke Mediendaten schreiben soll. In diesem Fall erstellt die Datei Senke intern den Bytestream. Die-Funktion gibt einen Zeiger auf die [**imfaktivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) -Schnittstelle der File-Senke zurück. Beschreibung

Wenn Ihre Codierungs Topologie wie folgt entworfen wurde, sollten Sie [**mfkreateasfmediasinkaktivierungs**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate) -anstelle von [**mfkreateasfmediasink**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink)verwenden:

-   Die Codierungs Topologie gilt für den geschützten Medien Pfad (PMP), und die Datei-Senke wird außerhalb des Prozesses verwendet.
-   Der Ausgabe Knoten der Topologie wird mithilfe des zurückgegebenen Zeigers auf das Aktivierungs Objekt der Datei Senke erstellt, und Ihre Anwendung verfolgt die Streams in der Datei Senke nach streamnummern.
    > [!Note]  
    > Sie können die Datei Senke durch Aufrufen von [**imfaktivate:: activateobject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject)aktivieren. Sie müssen das Objekt jedoch nicht explizit aktivieren. Die Medien Sitzung verfolgt das Aktivierungs Objekt und aktiviert die Datei Senke automatisch während der Codierungs Sitzung.

     

-   Die Datenstrom Informationen werden im ContentInfo-Objekt konfiguriert. Wird im nächsten unter Abschnitt ausgeblendet.

Nach dem Erstellen der ASF-Datei-Senke muss Sie vor dem Erstellen der Topologie konfiguriert werden. Die Datei Senke muss die folgenden Informationen kennen, um die Ausgabedatei zu generieren.

-   Grundlegende streaminformationen
-   Codierungs Modus-Informationen
-   Metadaten

Die File Sink implementiert das [Objekt "ASF ContentInfo](asf-contentinfo-object.md) " und macht die [**imfasfcontentinfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) -Schnittstelle verfügbar, sodass eine Anwendung Sie verwenden kann, um Informationen zu den Streams und der Codierung festzulegen. Abhängig von der Funktion, die Sie zum Erstellen der Datei Senke aufgerufen haben, gibt es zwei Möglichkeiten, einen Verweis auf die **imfasfcontentinfo** -Schnittstelle zu erhalten.

-   Wenn Sie die [**mfcreateasfmediasink**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink) -Funktion aufrufen, muss die Anwendung die [**imfasfcontentinfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) -Schnittstelle Abfragen, indem Sie **imfmediasink:: QueryInterface** für die zurückgegebene Datei-Senke aufruft.
-   Wenn Sie [**mfkreateasfmediasinkaktivierungs**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate)aufrufen, erwartet diese Funktion, dass Sie vor dem-Aufrufen über ein vollständig konfiguriertes ContentInfo-Objekt verfügen. Zu diesem Zweck müssen Sie ein leeres ContentInfo-Objekt erstellen, indem Sie [**mfcreateasfcontentinfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) aufrufen und es dann mit allen erforderlichen Informationen konfigurieren. Übergeben Sie das konfigurierte ContentInfo-Objekt an das **mfkreateasfmediasinkaktivierungs** -Objekt, um einen Zeiger auf das senkenaktivierungs-Objekt zu erhalten. Sie können die Datei Senke nicht mithilfe des zurückgegebenen Aktivierungs Objekts aktivieren und dann alle Datenstrom-oder Codierungsinformationen ändern.

Informationen zum Konfigurieren von senkendatenströmen und bestimmten Eigenschaften finden Sie in den folgenden Themen:

-   [Hinzufügen von streaminformationen zur ASF-Datei-Senke](adding-stream-information-to-the-asf-file-sink.md)
-   [Festlegen von Eigenschaften in der Datei Senke](setting-properties-in-the-file-sink.md)
-   [Hinzufügen von Metadaten zur Datei Senke](adding-metadata-to-the-file-sink.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ASF-Medien senken](asf-media-sinks.md)
</dt> <dt>

[Komponenten der Pipeline Schicht-ASF](pipeline-layer-asf-components.md)
</dt> <dt>

[Unterstützung von ASF in Media Foundation](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



