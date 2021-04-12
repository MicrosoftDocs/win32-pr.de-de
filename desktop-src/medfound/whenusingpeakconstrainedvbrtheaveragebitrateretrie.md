---
description: Wenn ich VBR mit hoher Auslastung verwende, ist die durchschnittliche Bitrate, die vom Codec-Objekt abgerufen wird, größer als die Spitzen Bitrate.
ms.assetid: 5fc344f8-4492-4878-802a-94606c5f33e0
title: Wenn ich VBR mit hoher Auslastung verwende, ist die durchschnittliche Bitrate, die vom Codec-Objekt abgerufen wird, größer als die Spitzen Bitrate. Wie ist das möglich?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa2bb2e09f5210baf8817553377fc832b9826b4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344839"
---
# <a name="when-i-use-peak-constrained-vbr-the-average-bit-rate-retrieved-from-the-codec-object-is-larger-than-the-peak-bit-rate-how-is-that-possible"></a>Wenn ich VBR mit hoher Auslastung verwende, ist die durchschnittliche Bitrate, die vom Codec-Objekt abgerufen wird, größer als die Spitzen Bitrate. Wie ist das möglich?

Die Beziehung zwischen der durchschnittlichen Bitrate und der Spitzen Bitrate wird häufig falsch verstanden. Die Spitzen Bitrate beschreibt eine Puffer Einschränkung über einen Zeitraum, der durch das Hauptpuffer Fenster angegeben wird. Die durchschnittliche Bitrate für die zweistufige VBR (uneingeschränkt oder mit hoher Einschränkung) ist die durchschnittliche Bits pro Sekunde während der Dauer der Datei.

Die tatsächliche Bitrate, die für eine Zeitspanne gleich dem Puffer Fenster verwendet [wird, kann die doppelte](the-leaky-bucket-buffer-model.md)Bitrate erreichen. Dies liegt daran, dass der Puffer, der als Anzahl von Bits definiert ist, die gleich der Bitrate für das Puffer Fenster (in Sekunden) ist, mit konstanter Geschwindigkeit geleert wird.

Beispielsweise erstellt der Encoder in einer Sekunde eines 56-Kbit/s-Streams Stichproben mit einer Gesamtgröße von 59 KB. Somit werden 56 KB Daten aus dem Puffer in dieser Sekunde entfernt, wobei 3 KB im Puffer belassen werden. Wenn der Stream über ein Puffer Fenster von drei Sekunden und somit eine Gesamt Puffergröße von 168 KB verfügt, dauert das Ausfüllen des Puffers fast 40 Sekunden. Die durchschnittliche Bitrate für den Datenstrom (wenn seine Dauer kleiner ist als die Zeitspanne, die zum Ausfüllen des Puffers benötigt wird) beträgt 59 Kbit/s, auch wenn die Bitrate auf 56 Kbit/s festgelegt ist.

Dasselbe Phänomen gilt für Einschränkungen der Spitzen Bitrate. Bei kurzen Inhalten kann die durchschnittliche Bitrate, die nach Abschluss der Codierung vom Codec-Objekt berechnet wird, größer als die Spitzen Bitrate sein.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Häufig gestellte Fragen](frequentlyaskedquestions.md)
</dt> </dl>

 

 



