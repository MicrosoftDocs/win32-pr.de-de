---
description: Suchen von Audioencoder-Ausgabetypen
ms.assetid: cd47d45b-ea47-4dec-867e-d51145d7f084
title: Suchen von Audioencoder-Ausgabetypen (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f80dd5aa5204887472e08c6ec5ff375a99b8788924ed0848764cde9ba4b5b97
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120061574"
---
# <a name="finding-audio-encoder-output-types-microsoft-media-foundation"></a>Suchen von Audioencoder-Ausgabetypen (Microsoft Media Foundation)

Da Sie ein Audioencoder-Ausgabeformat verwenden müssen, das vom Audioencoder aufzählt wird, müssen Sie eine Möglichkeit haben, das Format zu finden, das ihren Anforderungen am besten entspricht. Die Anzahl der Kanäle, Bits pro Stichprobe und die Abtastrate der ausgabe, die Sie auswählen, müssen mit den Werten für den von Ihnen komprimierten Inhalt übereinstimmen. Der Encoder unterstützt jedoch möglicherweise mehrere Typen innerhalb dieser Einschränkungen.

Der entscheidende Faktor für die Auswahl eines Typs ist die Bitrate des codierten Streams. Sie möchten einen Medientyp suchen, der Ihrer Eingabe entspricht und über eine Bitrate verfügt, die so nah wie möglich an einem Zielwert liegt. Wenn Sie vbr-Ausgabetypen mit nur einem Durchlauf aufzählen, ist es der Qualitätswert, der den verwendeten Typ bestimmt. Weitere Informationen zu Qualitätswerten in enumerationierten Ausgabetypen finden Sie unter [Aufzählen von Audiotypen für bestimmte Codierungsmodi.](enumeratingaudiotypesforspecificencodingmodes.md)

> [!Note]  
>    Der Audioencoder listet einige Typen auf, bei denen es sich um Duplikate anderer Typen handelt. Diese Duplikate sind für Formate vorhanden, bei denen die Anzahl der Pakete pro Sekunde nicht den Anforderungen für die Speicherung in ASF-Dateien entspricht, wenn sie mit Video synchronisiert werden. Audiodaten, die mit Videos in einer ASF-Datei synchronisiert werden, müssen 3 oder mehr Pakete pro Sekunde für Bitraten unter 32000 und 5 oder mehr Pakete pro Sekunde für Bitraten aufweisen, die größer oder gleich 32000 sind.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Konfigurieren der Audiocodierung](configuringaudioencoding.md)
</dt> <dt>

[Aufzählen von Audiotypen für bestimmte Codierungsmodi](enumeratingaudiotypesforspecificencodingmodes.md)
</dt> </dl>

 

 



