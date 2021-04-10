---
title: So erhalten Sie eine Writer-Statistik
description: So erhalten Sie eine Writer-Statistik
ms.assetid: 81d7f567-0d99-4199-9248-1a497dc2eaab
keywords:
- Advanced Systems Format (ASF), Writer Statistics
- ASF (Advanced Systems Format), Writer Statistics
- Writer-Statistik, Informationen zu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8c6620a2410b08d4d605c4dc116366c24b1e52c
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2020
ms.locfileid: "103948510"
---
# <a name="to-get-writer-statistics"></a>So erhalten Sie eine Writer-Statistik

Der Writer kann statistische Informationen zu Schreibvorgängen bereitstellen. Es gibt zwei Methoden zum Sammeln von Writer-Statistiken: [**iwmbeschreiteradvanced:: getstatistics**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-getstatistics) und [**IWMWriterAdvanced3:: getstatisticsex**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced3-getstatisticsex). Die von **getstatisticsex** abgerufenen Informationen sind spezifischer als die von **getstatistics** abgerufenen Informationen.

Beide Methoden füllen Strukturen mit statistischen Informationen auf. **Getstatistics** verwendet die [**WM \_ Writer \_ Statistics**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_writer_statistics) -Struktur, und **getstatisticsex** verwendet die " [**WM \_ Writer \_ Statistics \_ Ex**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_writer_statistics_ex) "-Struktur. " **Getstatisticsex** " dupliziert die von " **getstatistics**" erhaltenen Daten nicht. Um möglichst umfassende Informationen zu erhalten, sollten Sie beide Methoden aufzurufen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Iwmschreiteradvanced-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced)
</dt> <dt>

[**IWMWriterAdvanced3-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced3)
</dt> <dt>

[**Schreiben von ASF-Dateien**](writing-asf-files.md)
</dt> </dl>

 

 




