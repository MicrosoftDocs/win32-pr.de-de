---
title: So erhalten Sie Leseleistungsstatistiken
description: So erhalten Sie Leseleistungsstatistiken
ms.assetid: 996abfe6-1444-48ab-8c34-ba923c4cd511
keywords:
- Advanced Systems Format (ASF), Readerleistungsstatistiken
- ASF (Advanced Systems Format), Readerleistungsstatistiken
- Advanced Systems Format (ASF), asynchrone Reader
- ASF (Advanced Systems Format), asynchrone Reader
- Advanced Systems Format (ASF), Leistungsstatistiken
- ASF (Advanced Systems Format), Leistungsstatistiken
- asynchrone Reader,Leistungsstatistiken
- Leistung, Readerstatistiken
- Leistung,asynchrone Reader
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2397e575d67a699c4f211d872b53632e728fc2240b396d7475c8bb6b243fe445
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119084262"
---
# <a name="to-get-reader-performance-statistics"></a>So erhalten Sie Leseleistungsstatistiken

Beim lokalen Lesen von Dateien mit dem asynchronen Reader ist es nicht erforderlich, die Leistung von Lesevorgängen zu überprüfen. Wenn Ihre Anwendung jedoch aus einer Streamingquelle liest, können Leistungsstatistiken sehr wichtig sein. Ihre Anwendung kann auf Änderungen der Wiedergabeleistung reagieren, um die bestmögliche Endbenutzererfahrung sicherzustellen.

Die Leistungsinformationen, die Sie vom Reader abrufen können, umfassen die folgenden Statistiken:

-   Die aktuelle Bandbreite der Verbindung.
-   Die Anzahl der vom Server empfangenen Pakete.
-   Die Anzahl verloren gegangener Pakete, die wiederhergestellt wurden.
-   Die Anzahl verloren gegangener Pakete, die nicht wiederhergestellt wurden.
-   Der Prozentsatz der Gesamtzahl der gesendeten Pakete, die empfangen wurden.

Führen Sie die folgenden Schritte aus, um Leseleistungsstatistiken zu erhalten.

1.  Erstellen Sie vor beginn der Wiedergabe eine [**WM \_ READER \_ STATISTICS-Struktur.**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_reader_statistics) Sie müssen das **cbSize-Member** auf sizeof(WM \_ READER \_ STATISTICS) festlegen.
2.  Rufen Sie einen Zeiger auf die [**IWMReaderAdvanced-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced) des Readerobjekts ab, indem **Sie IWMReader::QueryInterface aufrufen.**
3.  Führen Sie während der Wiedergabe häufig Aufrufe an [**IWMReaderAdvanced::GetStatistics**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getstatistics) aus, um die Leistung zu überwachen. Übergeben Sie ihre **WM \_ READER \_ STATISTICS-Struktur** bei jedem Aufruf, und untersuchen Sie die entsprechenden Member.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Lesen von Dateien mit dem asynchronen Reader**](reading-files-with-the-asynchronous-reader.md)
</dt> </dl>

 

 




