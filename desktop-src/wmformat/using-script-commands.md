---
title: Verwenden von Skript Befehlen
description: Verwenden von Skript Befehlen
ms.assetid: be8a2d22-35cb-4b8d-ad00-e8a45bb85b39
keywords:
- Windows Media-Format-SDK, Skript Befehle
- Advanced Systems Format (ASF), Skript Befehle
- ASF (Advanced Systems Format), Skript Befehle
- Skripts, Befehle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad2e840a677e58a1be528e84e4ed1b4be7fe3619
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037045"
---
# <a name="using-script-commands"></a>Verwenden von Skript Befehlen

Das Windows Media-Format-SDK unterstützt die Verwendung von Skript Befehlen, um Anwendungs Aktionen in ASF-Dateien zu kommunizieren. Jeder Skript Befehl besteht aus zwei Zeichen folgen, wobei es sich bei der ersten Zeichenfolge um den Befehlstyp handelt, bei dem es sich um die Befehlsdaten handelt. Beispielsweise können Sie den Skripttyp "URL" verwenden und eine gültige Internet-URL als Befehlsdaten übergeben. Wenn eine Leseanwendung, die Skript Befehle vom Typ "URL" unterstützt, diesen Befehl empfängt, wird die angegebene Adresse in einem Browserfenster geöffnet.

Das Windows Media-Format SDK bietet zwei Optionen zum Bereitstellen von Skripts in ASF-Dateien. Sie können einen Skript Datenstrom erstellen oder Skript Befehle in den Header der Datei einschließen. Skript Datenströme sind hilfreich, da die Skript Befehle in der Präsentationszeit sortiert werden. Wenn Sie Skript Befehle im Dateiheader verwenden, muss die Anwendung alle Skript Befehle abrufen, bevor die Wiedergabe gestartet wird. Sie müssen die Präsentations Zeiten von Skript Befehlen nachverfolgen und zum richtigen Zeitpunkt auf Sie reagieren.

In den folgenden Abschnitten wird beschrieben, wie Skript Befehle in eine ASF-Datei eingeschlossen werden.



| `Section`                                                                                                                | BESCHREIBUNG                                                  |
|------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| [So verwenden Sie einen Skript Datenstrom](to-use-a-script-stream.md)                                                                   | Beschreibt das Einschließen von Skript Befehlen in einen Skript Datenstrom. |
| [So fügen Sie dem Header Skript Daten hinzu](to-add-script-data-to-the-header.md)                                               | Beschreibt das Einschließen von Skript Befehlen in den Dateiheader. |
| [Verwenden von Skript Befehlen, die von Windows Media Player unterstützt werden](using-script-commands-supported-by-windows-media-player.md) | Beschreibt die Skript Befehle, die von Windows Media Player verwendet werden.  |



 

> [!Note]  
> In früheren Versionen des Windows Media Format SDK wurden Skript Datenströme verwendet, um Webadressen zu öffnen, die dem Inhalt einer ASF-Datei entsprechen. Sie können jetzt Webstreams verwenden, um mit synchronisierten Webseiten zu arbeiten. Weitere Informationen. siehe [Webstreams](web-streams.md).

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Skriptbefehle**](script-commands.md)
</dt> <dt>

[**Programmierhandbuch**](programming-guide.md)
</dt> </dl>

 

 




