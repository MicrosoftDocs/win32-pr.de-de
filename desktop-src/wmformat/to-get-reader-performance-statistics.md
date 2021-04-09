---
title: So erhalten Sie Leistungsstatistiken für Leser
description: So erhalten Sie Leistungsstatistiken für Leser
ms.assetid: 996abfe6-1444-48ab-8c34-ba923c4cd511
keywords:
- Advanced Systems Format (ASF), Reader-Leistungsstatistik
- ASF (Advanced Systems Format), Reader-Leistungsstatistik
- Advanced Systems Format (ASF), asynchrone Leser
- ASF (Advanced Systems Format), asynchrone Leser
- Advanced Systems Format (ASF), Leistungsstatistik
- ASF (Advanced Systems Format), Leistungsstatistik
- asynchrone Leser, Leistungsstatistiken
- Leistung, Leser Statistik
- Leistung, asynchrone Leser
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5484b211f2c2d1e9ad4cf9aac3773c7946757c2
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "103858003"
---
# <a name="to-get-reader-performance-statistics"></a>So erhalten Sie Leistungsstatistiken für Leser

Wenn Dateien lokal mit dem asynchronen Reader gelesen werden, ist es nicht erforderlich, die Leistung von Lesevorgängen zu überprüfen. Wenn Ihre Anwendung jedoch aus einer Streamingquelle liest, kann die Leistungsstatistik sehr wichtig sein. Ihre Anwendung kann auf Änderungen der Wiedergabe Leistung reagieren, um die bestmögliche Endbenutzer Leistung zu gewährleisten.

Die Leistungsinformationen, die Sie aus dem Reader abrufen können, umfassen die folgenden Statistiken:

-   Die aktuelle Bandbreite der Verbindung.
-   Die Anzahl der vom Server empfangenen Pakete.
-   Die Anzahl verlorener Pakete, die wieder hergestellt wurden.
-   Die Anzahl verlorener Pakete, die nicht wieder hergestellt wurden.
-   Der Prozentsatz der empfangenen Gesamtzahl der gesendeten Pakete.

Führen Sie die folgenden Schritte aus, um Leistungsstatistiken für Leser zu erhalten.

1.  Erstellen Sie vor der Wiedergabe eine Statistik für die [**WM-Reader- \_ \_ Statistik**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_reader_statistics) . Sie müssen das **CBSIZE** -Member auf sizeof (WM \_ Reader \_ Statistics) festlegen.
2.  Abrufen eines Zeigers auf die [**iwmreaderadvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced) -Schnittstelle des Reader-Objekts durch Aufrufen von **iwmreader:: QueryInterface**.
3.  Führen Sie während der Wiedergabe häufig Aufrufe von [**iwmreaderadvanced:: getstatistics**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getstatistics) aus, um die Leistung zu überwachen. Übergeben Sie Ihre **WM- \_ Reader- \_ Statistik** Struktur mit jedem-Befehl, und untersuchen Sie die entsprechenden Member.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Lesen von Dateien mit dem asynchronen Reader**](reading-files-with-the-asynchronous-reader.md)
</dt> </dl>

 

 




