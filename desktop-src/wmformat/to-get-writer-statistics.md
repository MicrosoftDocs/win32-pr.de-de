---
title: So erhalten Sie Writer-Statistiken
description: So erhalten Sie Writer-Statistiken
ms.assetid: 81d7f567-0d99-4199-9248-1a497dc2eaab
keywords:
- Advanced Systems Format (ASF), Writer-Statistiken
- ASF (Advanced Systems Format), Writer-Statistiken
- Writer-Statistik,About
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1cedd96f1e94b8d3c9499fe08e3eeebb2100e866b141b756483cfb07bb7cb0c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119083965"
---
# <a name="to-get-writer-statistics"></a>So erhalten Sie Writer-Statistiken

Der Writer kann statistische Informationen zu Schreibvorgängen bereitstellen. Es gibt zwei Methoden zum Sammeln von Writerstatistiken: [**IWMWriterAdvanced::GetStatistics**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-getstatistics) und [**IWMWriterAdvanced3::GetStatisticsEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced3-getstatisticsex). Die von **GetStatisticsEx** abgerufenen Informationen sind spezifischer als die von **GetStatistics abgerufenen Informationen.**

Beide Methoden füllen Strukturen mit statistischen Informationen auf. **GetStatistics verwendet** die [**WM WRITER \_ \_ STATISTICS-Struktur**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_writer_statistics) und **GetStatisticsEx** die [**WM WRITER STATISTICS \_ \_ \_ EX-Struktur.**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_writer_statistics_ex) **GetStatisticsEx** dupliziert die von **GetStatistics erhaltenen Daten nicht.** Um die vollständigsten Informationen zu erhalten, sollten Sie beide Methoden aufrufen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IWMWriterAdvanced-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced)
</dt> <dt>

[**IWMWriterAdvanced3-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced3)
</dt> <dt>

[**Schreiben von ASF-Dateien**](writing-asf-files.md)
</dt> </dl>

 

 




