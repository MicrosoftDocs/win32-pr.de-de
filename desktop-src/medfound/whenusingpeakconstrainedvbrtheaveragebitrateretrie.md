---
description: Wenn ich vbr mit maximaler Auslastung verwende, ist die durchschnittliche Bitrate, die vom Codecobjekt abgerufen wird, größer als die Spitzenbitrate.
ms.assetid: 5fc344f8-4492-4878-802a-94606c5f33e0
title: Wenn ich vbr mit maximaler Auslastung verwende, ist die durchschnittliche Bitrate, die vom Codecobjekt abgerufen wird, größer als die Spitzenbitrate. Wie ist dies möglich?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa27e1a03c12f854486c65d7959c66f6592da4c3fea84936ee671a911f7fa46d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120011950"
---
# <a name="when-i-use-peak-constrained-vbr-the-average-bit-rate-retrieved-from-the-codec-object-is-larger-than-the-peak-bit-rate-how-is-that-possible"></a>Wenn ich vbr mit maximaler Auslastung verwende, ist die durchschnittliche Bitrate, die vom Codecobjekt abgerufen wird, größer als die Spitzenbitrate. Wie ist dies möglich?

Die Beziehung zwischen der durchschnittlichen Bitrate und der Spitzenbitrate wird häufig falsch verstanden. Die Spitzenbitrate beschreibt eine Puffereinschränkung über einen Zeitraum, der vom Spitzenpufferfenster angegeben wird. Die durchschnittliche Bitrate für VBR mit zwei Durchlauf (uneingeschränkt oder spitzenbeschränkt) ist die durchschnittliche Bitrate pro Sekunde über die Dauer der Datei.

Wie unter [The Leaky Bucket Buffer Model (The Leaky Bucket Buffer Model)](the-leaky-bucket-buffer-model.md)beschrieben, kann die tatsächliche Bitrate, die über einen bestimmten Zeitraum gleich dem Pufferfenster verwendet wird, die doppelte Bitrate erreichen. Dies liegt daran, dass der Puffer, der als Anzahl von Bits definiert ist, die der Bitrate entspricht, mit der das Pufferfenster (in Sekunden) entspricht, mit konstanter Rate geleert wird.

Beispielsweise erstellt der Encoder in einer Sekunde eines Streams mit 56 KBit/s Stichproben von insgesamt 59 Kb. Daher werden in dieser Sekunde 56 KB Daten aus dem Puffer entfernt, sodass 3 KB im Puffer bleiben. Wenn der Stream ein Pufferfenster von drei Sekunden und somit eine Gesamtpuffergröße von 168 Kb hat, dauert es fast 40 Sekunden, bis der Puffer gefüllt ist. Die durchschnittliche Bitrate für den Stream (wenn die Dauer kleiner als die Zeit ist, die zum Füllen des Puffers benötigt wird) beträgt 59 KBit/s, obwohl die Bitrate auf 56 KBit/s festgelegt ist.

Dasselbe Gilt gilt für Einschränkungen der Spitzenbitrate. Bei kurzen Inhalten kann die durchschnittliche Bitrate, die vom Codecobjekt nach Abschluss der Codierung berechnet wird, größer als die Spitzenbitrate sein.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Häufig gestellte Fragen](frequentlyaskedquestions.md)
</dt> </dl>

 

 



