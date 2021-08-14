---
title: Verwenden von Skriptbefehlen
description: Verwenden von Skriptbefehlen
ms.assetid: be8a2d22-35cb-4b8d-ad00-e8a45bb85b39
keywords:
- Windows Medienformat-SDK, Skriptbefehle
- Advanced Systems Format (ASF), Skriptbefehle
- ASF (Advanced Systems Format), Skriptbefehle
- Skripts, Befehle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88b77de3e892d4f7b479822442a2637849df3d4bcd56273deb952246fba14f28
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118195786"
---
# <a name="using-script-commands"></a>Verwenden von Skriptbefehlen

Das Windows Media Format SDK unterstützt die Verwendung von Skriptbefehlen, um Anwendungsaktionen in ASF-Dateien zu kommunizieren. Jeder Skriptbefehl besteht aus zwei Zeichenfolgen. Die erste Zeichenfolge ist der Befehlstyp, die zweite die Befehlsdaten. Beispielsweise können Sie den Skripttyp "URL" verwenden und eine gültige Internet-URL als Befehlsdaten übergeben. Wenn eine Leseanwendung, die Skriptbefehle vom Typ "URL" unterstützt, diesen Befehl empfängt, wird die angegebene Adresse in einem Browserfenster geöffnet.

Das Windows Media Format SDK bietet zwei Optionen für die Bereitstellung von Skripts in ASF-Dateien. Sie können einen Skriptstream erstellen oder Skriptbefehle in den Header der Datei eingeben. Skriptstreams sind nützlich, da die Skriptbefehle in der Reihenfolge der Präsentationszeit übermittelt werden. Wenn Sie Skriptbefehle im Dateiheader verwenden, muss Ihre Anwendung alle Skriptbefehle abrufen, bevor die Wiedergabe gestartet wird. Sie müssen die Präsentationszeiten von Skriptbefehlen nachverfolgen und zum richtigen Zeitpunkt darauf reagieren.

In den folgenden Abschnitten wird beschrieben, wie Skriptbefehle in eine ASF-Datei enthalten sind.



| `Section`                                                                                                                | BESCHREIBUNG                                                  |
|------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| [So verwenden Sie einen Skriptstream](to-use-a-script-stream.md)                                                                   | Beschreibt, wie Skriptbefehle in einen Skriptstream enthalten sind. |
| [So fügen Sie dem Header Skriptdaten hinzu](to-add-script-data-to-the-header.md)                                               | Beschreibt das Hinzufügen von Skriptbefehlen in den Dateiheader. |
| [Verwenden von Skriptbefehlen, die von Windows Media Player](using-script-commands-supported-by-windows-media-player.md) | Beschreibt die Skriptbefehle, die von Windows Media Player.  |



 

> [!Note]  
> In früheren Versionen des Windows Media Format SDK wurden Skriptstreams verwendet, um Webadressen zu öffnen, die dem Inhalt einer ASF-Datei entspricht. Sie können jetzt Webstreams verwenden, um mit synchronisierten Webseiten zu arbeiten. Weitere Informationen. siehe [Web Streams](web-streams.md).

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Skriptbefehle**](script-commands.md)
</dt> <dt>

[**Programmierhandbuch**](programming-guide.md)
</dt> </dl>

 

 




