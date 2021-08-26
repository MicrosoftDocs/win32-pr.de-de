---
title: SMPTE-Zeitcodeunterstützung
description: SMPTE-Zeitcodeunterstützung
ms.assetid: 047bda0d-142d-4eed-9b59-c0c36b97ed45
keywords:
- Windows Medienformat-SDK, SMPTE-Zeitcodes
- Advanced Systems Format (ASF), SMPTE-Zeitcodes
- ASF (Advanced Systems Format), SMPTE-Zeitcodes
- Windows Media Format SDK, IWMReaderTimecode-Schnittstelle
- Advanced Systems Format (ASF), IWMReaderTimecode-Schnittstelle
- ASF (Advanced Systems Format), IWMReaderTimecode-Schnittstelle
- SMPTE-Zeitcodes, Informationen
- IWMReaderTimecode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b19e3d7a85c797a3b0247bedb2359b4b40b60e8d4f243f14e2c94175bb1e2740
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119929610"
---
# <a name="smpte-time-code-support"></a>SMPTE-Zeitcodeunterstützung

Das Windows Media Format SDK bietet eingeschränkte Unterstützung für SMPTE-Zeitcode, bei dem es sich um ein Standardzeitcodeformat für Filme und Fernsehsendungen handelt. Sie können SMPTE-Zeitcodedaten mit Beispielen als Dateneinheitserweiterungen enthalten. Der Datenteil der Erweiterung ist eine [**WMT \_ TIMECODE \_ EXTENSION \_ DATA-Struktur,**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_timecode_extension_data) die die Informationen aus dem ursprünglichen SMPTE-Zeitstempel enthält.

Für die Verwaltung von SMPTE-Zeitcode in Ihren ASF-Dateien gelten Leistungslimits. Jedes Beispiel mit einem zugeordneten SMPTE-Zeitstempel erfordert den Transport der 14 Bytes in der Zeitstempelstruktur. In einem Streamingszenario kann diese erhöhte Bandbreitenanforderung schwerwiegende Folgen haben. Daher wird empfohlen, dass SMPTE-Zeitcodes nur während des Videobearbeitungsprozesses in ASF-Dateien beibehalten werden, was in der Regel mit lokalen Dateien erfolgt. Wenn die endgültige Datei erstellt wird, sollten Sie die Dateneinheitserweiterungen entfernen.

Sie können SMPTE-Zeitstempel wie jede andere Dateneinheitserweiterung lesen, aber die Leseobjekte bieten integrierte Unterstützung für die Suche nach SMPTE-Zeitcode. Um nach SMPTE-Zeitstempeln suchen zu können, müssen Sie die Datei zunächst nach SMPTE-Zeitcode indizieren. Sie können den Indexer so konfigurieren, dass Zeitcodes indiziert werden, indem Sie die [**IWMIndexer2::Configure-Methode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmindexer2-configure) verwenden.

Mit dem asynchronen Reader können Sie mithilfe der Methoden [**der IWMReaderTimecode-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadertimecode) und der [**IWMReaderAdvanced3::StartAtPosition-Methode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced3-startatposition) durch eine Datei mit SMPTE-Zeitstempeln navigieren. Verwenden Sie mit dem synchronen Reader [**IWMSyncReader2::SetRangeByTimecode.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader2-setrangebytimecode)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**ASF-Dateifeatures**](asf-file-features.md)
</dt> <dt>

[**Konfigurieren von Dateneinheitserweiterung en**](configuring-data-unit-extensions.md)
</dt> </dl>

 

 




