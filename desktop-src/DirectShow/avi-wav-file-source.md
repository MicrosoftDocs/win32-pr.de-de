---
description: AVI/WAV-Datei Quelle
ms.assetid: b8abf5d8-ba7f-441d-beef-9f85859318d5
title: AVI/WAV-Datei Quelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef659d880ef570176f94ac91875291ea9d200cf5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106344336"
---
# <a name="aviwav-file-source"></a>AVI/WAV-Datei Quelle

(Veraltet. Verwenden Sie für AVI-und WAV-Dateien die [Datei Quelle (Async)](file-source--async--filter.md) und den [avi-Splitter](avi-splitter-filter.md) -oder [Wave-Parser](wave-parser-filter.md).)

Der Quell Filter der AVI/WAV-Datei liest AVI-und WAV-Quelldateien und generiert die entsprechenden Ausgabe Pins für den Dateityp.

Bei WAV-Dateien erstellt der Filter eine audioausgabepin, die einen Audiostream erzeugt, der mit einem audiorenderingfilter oder einem Beteiligten audiotransformier Filter verbunden werden kann.

Für AVI-Dateien erstellt der Filter eine Videoausgabe-PIN, die einen komprimierten AVI-Stream erzeugt, der für den AVI-Codec-Filter geeignet ist, sowie eine audioausgabepin, die einen Audiostream erzeugt, der für einen audiorenderingfilter oder einen dazwischen liegenden audiotransformier

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> </dl>

 

 



