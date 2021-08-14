---
title: Arbeiten mit Writer-Senken
description: Arbeiten mit Writer-Senken
ms.assetid: 1ad28684-47d2-4ddb-bf18-22310f0392a0
keywords:
- Advanced Systems Format (ASF), Writer-Senken
- ASF (Advanced Systems Format), Writer-Senken
- Advanced Systems Format (ASF), Senken
- ASF (Advanced Systems Format), Senken
- sinks,writer sinks
- Writer-Senken, Informationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 407e5bf2e87bfbf3084d19f75170a12be693d804d4d902f919096dca5aeab057
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118194867"
---
# <a name="working-with-writer-sinks"></a>Arbeiten mit Writer-Senken

Das Writer-Objekt des Windows Media Format SDK verarbeitet Eingabemediendaten in einen Bitstream. Das Writer-Objekt übermittelt den Bitstream jedoch nicht an das endgültige Ziel (entweder an eine Datei oder einen Netzwerkspeicherort). Um den ASF-Inhalt in ein verwendbares Format zu schreiben, müssen Sie Writer-Senken verwenden.

Das Writer-Objekt unterstützt drei Arten von Senken: Dateisenken, Netzwerksenken und Pushsenken. Eine Dateisenke schreibt ASF-Inhalt in eine ASF-Datei auf dem Datenträger. Eine Netzwerksenke überträgt ASF-Inhalte von einer Netzwerkadresse. Eine Pushsenke übermittelt Daten an einen Server, auf dem Windows Media-Dienste ausgeführt wird, sodass der Server den Inhalt für die gewünschte Zielgruppe verfügbar machen kann. Sie können auch eigene Senken erstellen, um ASF-Daten auf beliebige Weise bereitzustellen, die von Ihrer Anwendung benötigt wird. Informationen zu Netzwerksenken und Pushsenken finden Sie unter [Senden von ASF-Daten über ein Netzwerk.](sending-asf-data-over-a-network.md) Im weiteren Verlauf dieses Abschnitts werden Writersenken erläutert.

Sie können eine oder mehrere Senken für jede Instanz des verwendeten Writers konfigurieren. Jede Senke verarbeitet nur ein einzelnes Ziel. Wenn Sie beispielsweise drei Dateien gleichzeitig schreiben möchten, müssen Sie jeweils eine separate Dateisenke erstellen und konfigurieren.

In den folgenden Abschnitten wird die Verwendung von Writer-Senken beschrieben.



| `Section`                                                                      | BESCHREIBUNG                                                                      |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [Hinzufügen von Senken zum Writer](adding-sinks-to-the-writer.md)                 | Beschreibt das Hinzufügen von Senken zum Writer.                                        |
| [Aufzählen von Senken](enumerating-sinks.md)                                   | Beschreibt, wie die Senken aufgezählt werden, die dem Writer hinzugefügt wurden.         |
| [Abrufen von Fehlermeldungen aus einer Senke](getting-error-messages-from-a-sink.md) | Beschreibt, wie Senken konfiguriert werden, um Statusmeldungen an Ihre Anwendung zu übermitteln. |
| [Verwenden von Dateisenken](using-file-sinks.md)                                     | Beschreibt, wie eine Writerdateisenke verwendet wird, um eine ASF-Datei auf dem Datenträger zu erstellen.           |
| [Verwenden von benutzerdefinierten Senken](using-custom-sinks.md)                                 | Beschreibt, wie Sie ihre eigenen benutzerdefinierten Senken erstellen und verwenden, um ASF-Daten bereitzustellen.       |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IWMWriterErweiterte Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced)
</dt> <dt>

[**IWMWriterSink-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink)
</dt> <dt>

[**Schreiben von ASF-Dateien**](writing-asf-files.md)
</dt> </dl>

 

 




