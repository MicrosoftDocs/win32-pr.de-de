---
description: Adaptive Differential Pulse Code Loss (ADPCM) ist ein Verlustkomprimierungsformat, das für XAudio2 implementiert wird, um zusätzliche Features zum Angeben der Größe des Komprimierungsbeispielblocks bereitzustellen.
ms.assetid: ae8a0a3e-293c-8193-d252-046d79771cfb
title: Übersicht über ADPCM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e1be1155d6d9f5a542b605c497ce28aa34191c0ac129582c18ec4a47b9f510f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118962719"
---
# <a name="adpcm-overview"></a>Übersicht über ADPCM

Adaptive Differential Pulse Code Loss (ADPCM) ist ein Verlustkomprimierungsformat, das für XAudio2 implementiert wird, um zusätzliche Features zum Angeben der Größe des Komprimierungsbeispielblocks bereitzustellen. Mit einem Verlustkomprimierungsformat werden einige Daten während der Komprimierung geändert und verloren. ADPCM kann Komprimierungsverhältnisse von bis zu 4:1 erreichen.

Die Implementierung von ADPCM für XAudio2 bietet zusätzliche Features zum Angeben der Größe des Komprimierungsbeispielblocks. Mit ADPCM kann der Audio-Designer eine Einstellung auswählen, die eine geeignete Kompromittierung zwischen Größe, Qualität und Auflösung (für die Platzierung von Schleifenpunkten) darstellt.

XAudio2 verwendet eine geänderte Version des Microsoft ADPCM-Codecs, der die erweiterte Datenformatierung unterstützt, die erforderlich ist, um benutzerdefinierte Beispielblockgrößen bereitzustellen. Aus diesem Grund können XAudio2-Audiodaten nicht von Audio-Engines wiedergegeben werden, die diese Version des ADPCM-Codecs nicht unterstützen.

> [!Note]  
> Derzeit ist die ADPCM-Komprimierung nur für Windows verfügbar, einschließlich XNA Game Studio Express für Windows Bereitstellungen.

 

## <a name="adpcm-encoding"></a>ADPCM-Codierung

Audiodaten werden mithilfe des Befehlszeilentools AdpcmEncode in ADPCM codiert.

-   AdpcmEncode

    Verwenden Sie das Befehlszeilentool **AdpcmEncode,** um Audiodateien als ADPCM für die Verwendung mit XAudio2 zu codieren.

## <a name="adpcm-decoding"></a>ADPCM-Decodierung

Die Softwaredecodierung von ADPCM wird in XAudio2 unterstützt.

-   XAudio2

    Um ADPCM-codierte Daten in XAudio2 zu verwenden, müssen Sie eine **ADPCMWAVEFORMAT-Struktur** mit ADPCM-spezifischen Werten initialisieren und als Argument an [**IXAudio2::CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice) übergeben, wenn Sie eine Quellstimme erstellen. Ein Beispiel für das Laden und Wiedergeben eines Sounds in XAudio2 finden Sie unter [Vorgehensweise: Wiedergeben eines Sounds mit XAudio2.](how-to--play-a-sound-with-xaudio2.md)

## <a name="samplesperblock"></a>SamplesPerBlock

Die ADPCM-Komprimierung wird verwendet, indem die Wellenform in Blöcke aufgeteilt und die Variation der Wellenformbeispiele innerhalb der einzelnen Blöcke vorhergesagt wird. Die Größe der Blöcke wird in Stichproben gemessen. Die kleinste Blockgröße beträgt 32 Stichproben, und die höchste ist 512 Stichproben.

Größere Blöcke ermöglichen eine bessere Komprimierung, was zu kleineren Dateigrößen führt, aber auf Kosten der Soundqualität und -auflösung für die Ausrichtung von Schleifenpunkten.

Im Allgemeinen führt das Ändern des SamplesPerBlock-Werts zu diesen Kompromissen:



| Wenn SamplesPerBlock...      | Dateikomprimierung | Soundqualität | Schleifenpunktauflösung |
|----------------------------|------------------|---------------|-----------------------|
| Erhöhungen (bis zu maximal 512)  | Erhöht        | Verringert     | Verringert             |
| Verringert (auf mindestens 32) | Verringert        | Erhöht     | Erhöht             |



 

## <a name="restrictions"></a>Beschränkungen

Da ADPCM Beispielblöcke verwendet, die nacheinander ausgerichtet sind, verfügt eine mit ADPCM komprimierte Welle möglicherweise über einen nicht abgeschlossenen, partiellen Block an dessen Ende. Der ADPCM-Decoder generiert Stille für den Rest dieses Teilblocks, wodurch die Welle nicht nahtlos durchlaufen wird.

Der Wert des *Parameters SamplesPerBlock* wirkt sich auf die Auflösung aus, mit der Sie Wellendaten und Schleifenpunkte ausrichten können.

Wenn Sie versuchen, die Komprimierung auf eine nicht ausgerichtete Welle anzuwenden, erhalten Sie einen Fehler oder eine Warnung, je nachdem, ob die Welle in Schleifenwiedergabeereignissen verwendet wird. Sie können eine Welle, die in Schleifenwiedergabeereignissen verwendet wird, nicht komprimieren. Entfernen Sie sie aus den Schleifenwiedergabeereignissen, und wenden Sie die Komprimierung erneut an.

Wenn Sie die Welle ausschließlich im Nicht-Schleifenmodus verwenden, gilt die Einschränkung für die Ausrichtung von Beispielblöcken nicht.

## <a name="adpcm-file-structure"></a>ADPCM-Dateistruktur

Eine ADPCM-Datei ist eine STANDARDMÄßIGE TEXTDATEI mit den folgenden Blocktypen.



| Block-FCC     | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| RIFF          | StandardmäßigerWERT-Block, der einen Dateityp mit dem Wert WAVE in den ersten vier Bytes des Datenabschnitts und die anderen Blöcke in der Datei im restlichen Datenabschnitt enthält.                                                                                                                                                                                                                                                                 |
| Fmt           | Enthält den Formatheader für die ADPCM-Datei. Die Daten in diesem Block entsprechen einer **ADPCMWAVEFORMAT-Struktur.**                                                                                                                                                                                                                                                                                                                             |
| data          | Enthält die codierten ADPCM-Audiodaten. Wenn Sie ADPCM in XAudio2 verwenden, müssen Sie den Inhalt des Datenblöckes in einen Puffer lesen und an eine Quellstimme als **pAudioData-Member** einer [**XAUDIO2 \_ BUFFER-Struktur**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) übergeben. Sie müssen den Inhalt des Datenabschnitts nicht per Byte austauschen.                                                                                                                            |
| smpl und wsmp | Optionale Blocktypen, die die Schleifeninformationen für die ADPCM-Datei enthalten. Wenn Sie ADPCM in XAudio2 verwenden, werden die in den Smpl- oder wsmp-Blöcken enthaltenen Werte verwendet, um die **LoopBeginLoopLength-** und **LoopCount-Member** der [**XAUDIO2 \_ BUFFER-Struktur**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) aufzufüllen. Auf der Xbox 360 müssen Sie die aus einem SMPL-Block geladenen Daten byte tauschen, um den Unterschied zwischen Windows und Xbox 360 zu berücksichtigen. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Programmierhandbuch](programming-guide.md)
</dt> </dl>

 

 
