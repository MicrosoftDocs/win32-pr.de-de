---
title: Arbeiten mit Writer-senken
description: Arbeiten mit Writer-senken
ms.assetid: 1ad28684-47d2-4ddb-bf18-22310f0392a0
keywords:
- Advanced Systems Format (ASF), Writer-senken
- ASF (Advanced Systems Format), Writer-senken
- Advanced Systems Format (ASF), senken
- ASF (Advanced Systems Format), senken
- senken, Writer-senken
- Writer-senken, Informationen zu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d5b690d9e1ab25d15f7c1e8612bf20e32f87c81
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "103723368"
---
# <a name="working-with-writer-sinks"></a>Arbeiten mit Writer-senken

Das Writer-Objekt des SDK für den Windows Media-Format verarbeitet Eingabemedien Daten in einen Bit-Stream. Allerdings stellt das Writer-Objekt den Bitstream nicht an das endgültige Ziel (entweder an eine Datei oder an einen Netzwerk Speicherort) bereit. Wenn Sie den ASF-Inhalt in ein verwendbares Format schreiben möchten, müssen Sie Writer-senken verwenden.

Das Writer-Objekt unterstützt drei Arten von senken: Datei senken, Netzwerk senken und pushsenken. Eine File-Senke schreibt ASF-Inhalte in eine ASF-Datei auf dem Datenträger. Eine Netzwerk Senke überträgt ASF-Inhalte über eine Netzwerkadresse. Eine Push-Senke liefert Daten an einen Server, auf dem Windows Media Services ausgeführt wird, sodass der Server den Inhalt für die gewünschte Zielgruppe verfügbar machen kann. Sie können auch eigene senken zur Bereitstellung von ASF-Daten auf die gleiche Weise erstellen, die für Ihre Anwendung erforderlich ist. Weitere Informationen zu Netzwerk senken und pushsenken finden Sie unter [Senden von ASF-Daten über ein Netzwerk](sending-asf-data-over-a-network.md). Im restlichen Teil dieses Abschnitts werden Writer-senken erläutert.

Sie können einen oder mehrere senken für jede Instanz des verwendeten Writers konfigurieren. Jede Senke verarbeitet nur ein einzelnes Ziel. Wenn Sie z. b. drei Dateien gleichzeitig schreiben möchten, müssen Sie jeweils eine separate Datei-Senke erstellen und konfigurieren.

In den folgenden Abschnitten wird die Verwendung von Writer-senken beschrieben.



| `Section`                                                                      | BESCHREIBUNG                                                                      |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [Hinzufügen von senken zum Writer](adding-sinks-to-the-writer.md)                 | Hier wird beschrieben, wie dem Writer senken hinzugefügt werden.                                        |
| [Auflisten von senken](enumerating-sinks.md)                                   | Beschreibt, wie die senken aufgelistet werden, die dem Writer hinzugefügt wurden.         |
| [Erhalten von Fehlermeldungen aus einer Senke](getting-error-messages-from-a-sink.md) | Beschreibt das Konfigurieren von senken, um Statusmeldungen an Ihre Anwendung zu übermitteln. |
| [Verwenden von Dateisenken](using-file-sinks.md)                                     | Beschreibt, wie eine Writer-Datei-Senke zum Erstellen einer ASF-Datei auf dem Datenträger verwendet wird.           |
| [Verwenden von benutzerdefinierten senken](using-custom-sinks.md)                                 | Hier wird beschrieben, wie Sie Ihre eigenen benutzerdefinierten senken zum Übermitteln von ASF-Daten erstellen und verwenden.       |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Iwmschreiteradvanced-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced)
</dt> <dt>

[**Iwmschreitersink-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink)
</dt> <dt>

[**Schreiben von ASF-Dateien**](writing-asf-files.md)
</dt> </dl>

 

 




