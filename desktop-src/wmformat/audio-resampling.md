---
title: Audioprobennahme
description: Audioprobennahme
ms.assetid: ec6ad6b2-1d35-4ac4-9a1e-3fc9c053000c
keywords:
- Windows Media-Format-SDK, audioresampling
- Windows Media-Format-SDK, neusampling von Audiodaten
- Advanced Systems Format (ASF), audioresampling
- ASF (Advanced Systems Format), audioresampling
- Advanced Systems Format (ASF), Resampling von Audiodaten
- ASF (Advanced Systems Format), Resampling von Audiodaten
- audioprobennahme
- Neuberechnung von Audioinformationen, Informationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 608272a7e531d7380991a705d391e6226a6758d1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309987"
---
# <a name="audio-resampling"></a>Audioprobennahme

Jedes komprimierte Format eines Audiocodecs hat eine bestimmte Samplingrate und eine bestimmte Stichprobengröße. Diese müssen nicht den Einstellungen des Eingabe Formats oder des Ausgabeformats entsprechen. Wenn ein Eingabeformat andere Einstellungen als das im Profil beschriebene komprimierte Format aufweist, wird das audioverfahren während des Codierungs Vorgangs vom Writer neu erstellt, um das komprimierte Format abzugleichen. Nur bestimmte Formate werden vom Writer als Eingabe akzeptiert. Wenn Sie die Eingabeformate für einen komprimierten Audiostream auflisten, können alle abgerufenen Formate neu erstellt werden, sodass Sie dem Format im Profil entsprechen.

Wenn Sie komprimierte Audiodaten lesen, wird der Inhalt vom Reader entsprechend dem Ausgabeformat neu erstellt. Sie müssen eines der Ausgabeformate verwenden, die vom Reader aufgelistet werden, damit Sie sicherstellen können, dass die Audiodaten in den Ausgabe Formateinstellungen erneut erstellt werden können.

Jede erneute Stichprobe wirkt sich potenziell auf die Audioqualität aus. Wenn möglich, sollten Sie Eingabe-und Ausgabeformate mit Einstellungen verwenden, die dem komprimierten Format entsprechen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Funktionen zum Schreiben von Dateien**](file-writing-features.md)
</dt> <dt>

[**Arbeiten mit Eingaben**](working-with-inputs.md)
</dt> <dt>

[**Arbeiten mit Ausgaben**](working-with-outputs.md)
</dt> </dl>

 

 




