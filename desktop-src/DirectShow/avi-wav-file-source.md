---
description: AVI/WAV-Dateiquelle
ms.assetid: b8abf5d8-ba7f-441d-beef-9f85859318d5
title: AVI/WAV-Dateiquelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de8c99de9eed21afa716c4f3ee81a5d1cc4e9731739526f7c9531c758b30a22a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119689360"
---
# <a name="aviwav-file-source"></a>AVI/WAV-Dateiquelle

(Veraltet. Verwenden Sie für AVI- und WAV-Dateien die [Dateiquelle (Async)](file-source--async--filter.md) und den [AVI-Splitter](avi-splitter-filter.md) oder [WAVE-Parser](wave-parser-filter.md).)

Der Filter "AVI/WAV-Dateiquelle" liest DIE UND WAV-Quelldateien und generiert die entsprechenden Ausgabepins für den Dateityp.

Für WAV-Dateien erstellt der Filter einen Audioausgabepin, der einen Audiostream erzeugt, der mit einem Audiorenderingfilter oder einem intervening audio transform filter verbunden werden kann.

Für AVI-Dateien erstellt der Filter einen Videoausgabepin, der einen komprimierten AVI-Stream erzeugt, der für den AVI-Codecfilter geeignet ist, und einen Audioausgabepin, der einen Audiostream erzeugt, der für einen Audiorenderingfilter oder einen intervening audio transform filter geeignet ist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> </dl>

 

 



