---
description: Erfahren Sie mehr über das Erstellen der ASF-Dateisenke, mit der eine Anwendung ASF-Mediendaten in einer Datei archivieren kann.
ms.assetid: 991f3345-a6b4-45c2-a89d-3c13c70b6bbc
title: Erstellen der ASF-Dateisenke
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 510ed3aeb3082277fa3a8bb4c814c1a82f92dd3da8815ffdbd70e4ef87d0d4f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118743258"
---
# <a name="creating-the-asf-file-sink"></a>Erstellen der ASF-Dateisenke

Die ASF-Dateisenke ist eine Implementierung von [**DURCHFMediaSink Media Foundation**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) die eine Anwendung verwenden kann, um ASF-Mediendaten in einer Datei zu archivieren. Informationen zum Objektmodell und zur allgemeinen Verwendung von ASF-Mediensenken finden Sie unter [ASF-Mediensenken.](asf-media-sinks.md)

Es gibt zwei Möglichkeiten, eine Instanz der ASF-Dateisenke zu erstellen. Sie können [**MFCreateASFMediaSink oder**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink) [**MFCreateASFMediaSinkActivate aufrufen.**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate)

Wenn Sie [**MFCreateASFMediaSink**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink)aufrufen, müssen Sie einen Bytestream für die Ausgabedatei angeben, in den die Senke den ASF-Inhalt während einer Codierungssitzung schreibt. Der angegebene Bytestream muss über suchbare und beschreibbare Funktionen verfügen. Andernfalls schlägt der **MFCreateASFMediaSink-Aufruf** mit dem Fehlercode E \_ FAIL fehl. Dieser Aufruf erstellt ein prozessinternes Dateisenkenobjekt und gibt einen Zeiger auf die [**BERMEDIASink-Schnittstelle**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) der Dateisenke zurück.

Wenn Sie [**MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate)aufrufen, müssen Sie die URL der Ausgabedatei angeben, in die die Dateisenke Mediendaten schreibt. In diesem Fall erstellt die Dateisenke intern den Bytestream. Die Funktion gibt einen Zeiger auf die [**BERActivate-Schnittstelle**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) der Dateisenke zurück. Beschreibung

Ziehen [**Sie MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate) anstelle von [**MFCreateASFMediaSink**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink)in Betracht, wenn Ihre Codierungstopologie wie folgt entworfen wurde:

-   Die Codierungstopologie ist für den geschützten Medienpfad (PMP) und die Dateisenke wird out-of-process verwendet.
-   Der Ausgabeknoten der Topologie wird mithilfe des zurückgegebenen Zeigers auf das Activate-Objekt der Dateisenke erstellt, und Ihre Anwendung verfolgt die Datenströme in der Dateisenke anhand von Datenstromnummern nach.
    > [!Note]  
    > Sie können die Dateisenke aktivieren, indem Sie [**DENKActivate::ActivateObject aufrufen.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) Sie müssen das Objekt jedoch nicht explizierend aktivieren. Die Mediensitzung verfolgt das Aktivierungsobjekt und aktiviert die Dateisenke während der Codierungssitzung automatisch.

     

-   Die Streaminformationen werden im ContentInfo-Objekt konfiguriert. Im nächsten Unterabschnitt wird dies nicht angezeigt.

Nach dem Erstellen der ASF-Dateisenke muss sie vor dem Erstellen der Topologie konfiguriert werden. Die Dateisenke muss die folgenden Informationen kennen, um die Ausgabedatei zu generieren.

-   Grundlegende Streaminformationen
-   Informationen zum Codierungsmodus
-   Metadaten

Die Dateisenke implementiert das [ASF ContentInfo-Objekt](asf-contentinfo-object.md) und macht die [**IMFASFContentInfo-Schnittstelle**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) verfügbar, damit eine Anwendung damit Informationen im Zusammenhang mit den Streams und der Codierung festlegen kann. Abhängig von der Funktion, die Sie zum Erstellen der Dateisenke aufgerufen haben, gibt es zwei Möglichkeiten, einen Verweis auf die **IMFASFContentInfo-Schnittstelle zu** erhalten.

-   Wenn Sie die [**MFCreateASFMediaSink-Funktion**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink) aufrufen, muss die Anwendung die [**IMFASFContentInfo-Schnittstelle**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) abfragen, indem SIE FÜR DIE zurückgegebene Dateisenke **DURCH AUFRUFEN VONGEMEDIASink::QueryInterface.**
-   Wenn Sie [**MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate)aufrufen, erwartet diese Funktion, dass Sie vor dem Aufruf über ein vollständig konfiguriertes ContentInfo-Objekt verfügen. Hierzu müssen Sie ein leeres ContentInfo-Objekt erstellen, indem Sie [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) aufrufen und es dann mit allen erforderlichen Informationen konfigurieren. Übergeben Sie das konfigurierte ContentInfo-Objekt an **MFCreateASFMediaSinkActivate,** um einen Zeiger auf das Senkenaktivierungsobjekt zu empfangen. Sie können die Dateisenke nicht mithilfe des zurückgegebenen Aktivierungsobjekts aktivieren und dann Datenstrom- oder Codierungsinformationen ändern.

Informationen zum Konfigurieren von Senkenstreams und bestimmten Eigenschaften finden Sie in den folgenden Themen:

-   [Hinzufügen von Streaminformationen zur ASF-Dateisenke](adding-stream-information-to-the-asf-file-sink.md)
-   [Festlegen von Eigenschaften in der Dateisenke](setting-properties-in-the-file-sink.md)
-   [Hinzufügen von Metadaten zur Dateisenke](adding-metadata-to-the-file-sink.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ASF-Mediensenken](asf-media-sinks.md)
</dt> <dt>

[ASF-Komponenten auf Pipelineebene](pipeline-layer-asf-components.md)
</dt> <dt>

[ASF-Unterstützung in Media Foundation](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



