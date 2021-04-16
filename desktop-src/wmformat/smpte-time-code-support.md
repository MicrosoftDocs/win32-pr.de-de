---
title: SMPTE-Zeit Code Unterstützung
description: SMPTE-Zeit Code Unterstützung
ms.assetid: 047bda0d-142d-4eed-9b59-c0c36b97ed45
keywords:
- Windows Media-Format-SDK, SMPTE-Zeit Codes
- Advanced Systems Format (ASF), SMPTE-Zeit Codes
- ASF (Advanced Systems Format), SMPTE-Zeit Codes
- Windows Media-Format-SDK, iwmreadertimecode-Schnittstelle
- Advanced Systems Format (ASF), iwmreadertimecode-Schnittstelle
- ASF (Advanced Systems Format), iwmreadertimecode-Schnittstelle
- SMPTE-Zeit Codes, Informationen zu
- Iwmreadertimecode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ecf8ef9da7d0fb0ee7d973cf21129f307066bc9
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104516610"
---
# <a name="smpte-time-code-support"></a>SMPTE-Zeit Code Unterstützung

Das Windows Media-Format SDK bietet eingeschränkte Unterstützung für SMPTE-Zeit Code, d. h. ein Standardmäßiges Zeit Code Format für Filme und Fernsehen. Sie können SMPTE-Zeit Code Daten mit Beispielen als Erweiterungen für Dateneinheiten einschließen. Der Datenteil der Erweiterung ist eine [**WMT-Zeit \_ Code \_ Erweiterungs \_ Daten**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_timecode_extension_data) Struktur, die die Informationen aus dem ursprünglichen SMPTE-Zeitstempel enthält.

Die Wartung von SMPTE-Zeit Code in ihren ASF-Dateien umfasst Leistungs Limits. Jede Stichprobe mit einem zugeordneten SMPTE-Zeitstempel erfordert den Transport der 14 Bytes in der Zeitstempel Struktur. In einem Streamingszenario könnte diese größere Bandbreiten Anforderung katastrophal sein. Daher wird empfohlen, dass SMPTE-Zeit Codes bei der Videobearbeitung nur in ASF-Dateien persistent gespeichert werden. Dies erfolgt in der Regel mit lokalen Dateien. Wenn die endgültige Datei erstellt wurde, sollten Sie die Dateneinheiten Erweiterungen entfernen.

Sie können SMPTE-Zeitstempel so lesen, wie Sie jede andere Erweiterung für Dateneinheiten lesen würden, aber die Lese Objekte bieten integrierte Unterstützung für die Suche nach SMPTE-Zeit Code. Um nach SMPTE-Zeitstempeln suchen zu können, müssen Sie zunächst die Datei nach SMPTE-Zeit Code indizieren. Sie können den Indexer so konfigurieren, dass Zeit Codes mithilfe der [**IWMIndexer2:: Configure**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmindexer2-configure) -Methode indiziert werden.

Mithilfe des asynchronen Readers können Sie mithilfe der Methoden der [**iwmreadertimecode**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadertimecode) -Schnittstelle und der [**IWMReaderAdvanced3:: startatposition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced3-startatposition) -Methode von SMPTE-Zeitstempeln aus in einer Datei navigieren. Verwenden Sie [**IWMSyncReader2:: setrangebytimecode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader2-setrangebytimecode)mit dem synchronen Reader.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Funktionen der ASF-Datei**](asf-file-features.md)
</dt> <dt>

[**Konfigurieren von Dateneinheitserweiterung en**](configuring-data-unit-extensions.md)
</dt> </dl>

 

 




