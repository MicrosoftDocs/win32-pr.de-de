---
description: Suchen von Audioencoder-Ausgabetypen
ms.assetid: cd47d45b-ea47-4dec-867e-d51145d7f084
title: Suchen von audioencoderausgabetypen (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5389274cca1178ebc0ae03e21f7a804f73a5db48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346464"
---
# <a name="finding-audio-encoder-output-types-microsoft-media-foundation"></a>Suchen von audioencoderausgabetypen (Microsoft Media Foundation)

Da Sie ein audiocodierungsausgabeformat verwenden müssen, das vom Audioencoder aufgelistet wird, müssen Sie über eine Möglichkeit verfügen, das Format zu finden, das für Ihre Anforderungen am besten geeignet ist. Die Anzahl der Kanäle, Bits pro Stichprobe und die Samplingrate der Ausgabe, die Sie auswählen, müssen mit den Werten für den von Ihnen komprimierte Inhalt identisch sein. Der Encoder unterstützt jedoch möglicherweise mehrere Typen innerhalb dieser Einschränkungen.

Der entscheidende Faktor für die Auswahl eines Typs ist die Bitrate des codierten Streams. Sie möchten einen Medientyp suchen, der mit Ihrer Eingabe übereinstimmt und eine Bitrate hat, die so nah wie möglich an einem Zielwert ist. Wenn Sie die VBR-Ausgabetypen mit einem Durchlauf auflisten, ist dies der Qualitäts Wert, der den Typ bestimmt, den Sie verwenden. Weitere Informationen zu Qualitätswerten in Enumerationstypen finden Sie unter Auflisten [von Audiotypen für bestimmte Codierungs Modi](enumeratingaudiotypesforspecificencodingmodes.md).

> [!Note]  
>    Der Audioencoder listet einige Typen auf, bei denen es sich um Duplikate anderer Typen handelt. Diese Duplikate sind für Formate vorhanden, in denen die Anzahl der Pakete pro Sekunde nicht den Anforderungen für die Speicherung in ASF-Dateien entspricht, wenn Sie mit Video synchronisiert werden. Audiodaten, die mit einem Video in einer ASF-Datei synchronisiert werden, müssen mindestens 3 Pakete pro Sekunde für Bitraten unter 32000 und mindestens 5 Pakete pro Sekunde für Bitraten größer oder gleich 32000 aufweisen.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Konfigurieren der Audiocodierung](configuringaudioencoding.md)
</dt> <dt>

[Auflisten von Audiotypen für bestimmte Codierungs Modi](enumeratingaudiotypesforspecificencodingmodes.md)
</dt> </dl>

 

 



