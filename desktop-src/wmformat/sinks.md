---
title: Senken
description: Senken
ms.assetid: 6781a326-a30a-4d4d-96db-332d0f681a31
keywords:
- Windows Media-Format-SDK, senken
- Windows Media-Format-SDK, Datei senken
- Advanced Systems Format (ASF), senken
- ASF (Advanced Systems Format), senken
- Advanced Systems Format (ASF), Datei senken
- ASF (Advanced Systems Format), Datei senken
- Windows Media-Format-SDK, netzwerksenken
- Windows Media-Format-SDK, pushsenken
- Advanced Systems Format (ASF), netzwerksenken
- ASF (Advanced Systems Format), Netzwerk senken
- Advanced Systems Format (ASF), pushsenken
- ASF (Advanced Systems Format), pushsenken
- senken, Informationen zu
- Datei senken, Informationen zu
- Netzwerk senken
- pushsenken
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a62548f159172f58d4f52b0289c5adbfef02f55
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104038580"
---
# <a name="sinks"></a>Senken

Das Writer-Objekt des Windows Media Format SDK übermittelt verarbeitete Inhalte an senken. Jede Senke ist ein Objekt, das Daten bereitstellt. Der Übermittlungs Punkt hängt vom Typ der Senke ab. Es gibt drei Arten von senken: Datei senken, Netzwerk senken und pushsenken.

## <a name="file-sinks"></a>Datei senken

Datei senken schreiben ASF-Inhalte in eine Datei auf einem lokalen Laufwerk oder auf einem Netzwerklaufwerk. Wenn Sie das Writer-Objekt verwenden, um eine Datei zu schreiben, ohne explizit eine File-Senke hinzuzufügen, erstellt der Writer einen für Sie mit dem Namen, den Sie an [**iwmwriter:: setoutputfilename**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setoutputfilename)übergeben. Sie können einem Writer-Objekt mehrere Datei senken zuweisen, um den Inhalt in mehreren Dateien gleichzeitig zu schreiben.

Mithilfe einer Datei Senke können Sie zahlreiche Aspekte der Datei steuern. Die folgenden Funktionen sind über eine Datei Senke verfügbar.

-   Überwachung von Datei Statistiken. Sie können die Dateigröße und-Dauer während der Erstellung überwachen.
-   Erstellung von Teil Inhalts Dateien. Datei senken können so konfiguriert werden, dass mit dem Schreiben von Inhalten zu einem bestimmten Zeitpunkt begonnen und das Schreiben zu einem bestimmten Zeitpunkt beendet wird. Dies ermöglicht es Ihnen, mehrere Dateien zu erstellen, die verschiedene Abschnitte desselben Inhalts in demselben Schreib Durchlauf enthalten.

## <a name="network-sinks"></a>Netzwerk senken

Netzwerk senken übertragen Inhalte an eine Netzwerkadresse. Das Lesen von Clients kann eine Verbindung mit der Adresse herstellen, um die Übertragung zu empfangen

## <a name="push-sinks"></a>Pushsenken

Pushsenken übermitteln Inhalte vom Writer an einen Server, auf dem Windows Media Services ausgeführt wird. Pushsenken werden in der Regel in Szenarien verwendet, in denen ein Computer Live Inhalte codiert und an einen oder mehrere Server zur breiten Verteilung übergibt. Durch die Verwendung einer Push-Senke können Sie Computern bestimmte Aufgaben zuordnen, um Bandbreite zu sparen und die Leistung der einzelnen Server zu verarbeiten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Funktionen zum Schreiben von Dateien**](file-writing-features.md)
</dt> <dt>

[**Arbeiten mit Writer-senken**](working-with-writer-sinks.md)
</dt> </dl>

 

 




