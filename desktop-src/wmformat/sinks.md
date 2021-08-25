---
title: Senken
description: Senken
ms.assetid: 6781a326-a30a-4d4d-96db-332d0f681a31
keywords:
- Windows Medienformat-SDK, Senken
- Windows Medienformat-SDK, Dateisenken
- Advanced Systems Format (ASF),sinks
- ASF (Advanced Systems Format), sinks
- Advanced Systems Format (ASF), Dateisenken
- ASF (Advanced Systems Format), Dateisenken
- Windows Medienformat-SDK, Netzwerksenken
- Windows Medienformat-SDK, Pushsenken
- Advanced Systems Format (ASF), Netzwerksenken
- ASF (Advanced Systems Format), Netzwerksenken
- Advanced Systems Format (ASF), Pushenken
- ASF (Advanced Systems Format), Pushenken
- sinks,about
- Dateisenken, Informationen
- Netzwerksenken
- Pushsenken
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb72479a231c3db508efcea7db54528c0b1bf9635afba8b842a4c23add0456cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807900"
---
# <a name="sinks"></a>Senken

Das Writer-Objekt des Windows Media Format SDK stellt verarbeiteten Inhalt an Senken bereit. Jede Senke ist ein Objekt, das Daten liefert. Der Zeitpunkt der Übermittlung hängt vom Typ der Senke ab. Es gibt drei Arten von Senken: Dateisenken, Netzwerksenken und Pushsenken.

## <a name="file-sinks"></a>Dateisenken

Dateisenken schreiben ASF-Inhalt in eine Datei auf einem lokalen Laufwerk oder Netzwerklaufwerk. Wenn Sie das Writer-Objekt verwenden, um eine Datei zu schreiben, ohne explizit eine Dateisenke hinzufügen zu müssen, erstellt der Writer eine Datei mit dem Namen, den Sie [**an IWMWriter::SetOutputFilename übergeben.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setoutputfilename) Sie können einem Writerobjekt mehrere Dateisenken zuweisen, um den Inhalt in mehreren Dateien gleichzeitig zu schreiben.

Mithilfe einer Dateisenke können Sie viele Aspekte der Datei steuern. Die folgenden Features sind über eine Dateisenke verfügbar.

-   Überwachung von Dateistatistiken. Sie können die Dateigröße und -dauer überwachen, während sie erstellt wird.
-   Partielle Inhaltsdateierstellung. Dateisenken können so konfiguriert werden, dass sie zu einem bestimmten Zeitpunkt mit dem Schreiben von Inhalten beginnen und das Schreiben zu einem bestimmten Zeitpunkt beenden. Dadurch können Sie mehrere Dateien erstellen, die verschiedene Abschnitte desselben Inhalts im gleichen Schreibpass enthalten.

## <a name="network-sinks"></a>Netzwerksenken

Netzwerksenken übertragen Inhalte an eine Netzwerkadresse. Leseclients können eine Verbindung mit der Adresse herstellen, um die Übertragung zu empfangen.

## <a name="push-sinks"></a>Pushen von Senken

Pushsenken senden Inhalt vom Writer an einen Server, auf dem Windows Media-Dienste. Pushsenken werden in der Regel in Szenarien verwendet, in denen ein Computer Liveinhalte codiert und zur breiten Verteilung an einen oder mehrere Server übermittelt. Mithilfe einer Pushsenke können Sie Computer für bestimmte Aufgaben verwenden, um Bandbreite und Verarbeitungsleistung auf jedem Server zu sparen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Funktionen zum Schreiben von Dateien**](file-writing-features.md)
</dt> <dt>

[**Arbeiten mit Writer-Senken**](working-with-writer-sinks.md)
</dt> </dl>

 

 




