---
description: Bei Adaptive Differential Pulse Code Modulation (ADPCM) handelt es sich um ein Ersetztes Komprimierungs Format, das für XAudio2 implementiert wird, um zusätzliche Features zum Angeben der Größe des Komprimierungs Beispiel Blocks bereitzustellen.
ms.assetid: ae8a0a3e-293c-8193-d252-046d79771cfb
title: Übersicht über ADPCM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fb918a611cb0840b2f02dfb13b547b795fb3304
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106358574"
---
# <a name="adpcm-overview"></a>Übersicht über ADPCM

Bei Adaptive Differential Pulse Code Modulation (ADPCM) handelt es sich um ein Ersetztes Komprimierungs Format, das für XAudio2 implementiert wird, um zusätzliche Features zum Angeben der Größe des Komprimierungs Beispiel Blocks bereitzustellen. Bei einem Verlust behafchten Komprimierungs Format werden einige Daten während der Komprimierung geändert und verloren gegangen. Für ADPCM können Komprimierungs Verhältnisse von bis zu 4:1 erreicht werden.

Die Implementierung von ADPCM für XAudio2 bietet zusätzliche Features zum Angeben der Größe des Komprimierungs Beispiel Blocks. Mit ADPCM kann der audiodesigner eine Einstellung auswählen, die eine angemessene Gefährdung zwischen Größe, Qualität und Auflösung darstellt (zum Platzieren von Schleifen Punkten).

XAudio2 verwendet eine geänderte Version des Microsoft ADPCM-Codecs, die die erweiterte Datenformatierung unterstützt, die zum Bereitstellen von benutzerdefinierten Beispiel Blockgrößen erforderlich ist. Aus diesem Grund können XAudio2-Audiodaten nicht von Audiomodulen abgespielt werden, die diese Version des ADPCM-Codecs nicht unterstützen.

> [!Note]  
> Derzeit ist die ADPCM-Komprimierung nur für Windows verfügbar, einschließlich XNA Game Studio Express für Windows-bereit Stellungen.

 

## <a name="adpcm-encoding"></a>ADPCM-Codierung

Audiodaten werden mit dem Befehlszeilen Tool adpcmencode in ADPCM codiert.

-   Adpcmencode

    Verwenden Sie das Befehlszeilen Tool **adpcmencode** , um Audiodateien als ADPCM für die Verwendung mit XAudio2 zu codieren.

## <a name="adpcm-decoding"></a>ADPCM-Decodierung

Software Decodierung von ADPCM wird in XAudio2 unterstützt.

-   XAudio2

    Um ADPCM-codierte Daten in XAudio2 zu verwenden, müssen Sie eine **ADPCMWAVEFORMAT** -Struktur mit ADPCM-spezifischen Werten initialisieren und Sie als Argument an [**IXAudio2:: kreatesourcevoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice) übergeben, wenn Sie eine Quellsprache erstellen. Ein Beispiel für das Laden und Wiedergeben eines Sounds in XAudio2 finden [Sie unter Gewusst wie: Wiedergabe eines Sounds mit XAudio2](how-to--play-a-sound-with-xaudio2.md).

## <a name="samplesperblock"></a>Samplesperblock

Die ADPCM-Komprimierung funktioniert, indem Sie die Wellenform in Blöcke aufteilen und die Variation der Wellenform-Beispiele in jedem Block Vorhersagen. Die Größe der Blöcke wird in den Beispielen gemessen. Die kleinste Blockgröße ist 32 Samples, und die höchste ist 512 Stichproben.

Größere Blöcke ermöglichen eine bessere Komprimierung, was zu kleineren Dateigrößen führt, aber auf Kosten der Ton Qualität und-Auflösung für das Ausrichten von Schleifen Punkten.

Im Allgemeinen führt das Ändern des samplesperblock-Werts zu diesen vor-und Nachteile:



| Wenn samplesperblock...      | Dateikomprimierung | Sound Qualität | Schleifen Punkt Auflösung |
|----------------------------|------------------|---------------|-----------------------|
| Erhöht (max. 512)  | Erhöht        | Ticks     | Ticks             |
| Wird verringert (bis zu min. 32) | Ticks        | Erhöht     | Erhöht             |



 

## <a name="restrictions"></a>Beschränkungen

Da ADPCM Beispiel Blöcke verwendet, die nacheinander ausgerichtet sind, kann eine mit ADPCM komprimierte Welle einen nicht abgeschlossenen, partiellen Block am Ende haben. Der ADPCM-Decoder generiert Ruhe für den Rest dieses partiellen Blocks, wodurch die Wellen Schleife nahtlos verhindert wird.

Der Wert des *samplesperblock* -Parameters wirkt sich auf die Auflösung aus, mit der Sie wellendaten und Schleifenpunkte ausrichten können.

Wenn Sie versuchen, die Komprimierung auf eine nicht ausgerichtete Welle anzuwenden, erhalten Sie eine Fehlermeldung oder eine Warnung, je nachdem, ob die Welle in Schleifen Wiedergabe Ereignissen verwendet wird. Es ist nicht möglich, eine Welle zu komprimieren, die in Schleifen Wiedergabe Ereignissen verwendet wird. Entfernen Sie Sie aus den Schleifen Wiedergabe Ereignissen, und wenden Sie die Komprimierung erneut an.

Wenn Sie die-Welle ausschließlich im nicht-Schleifen Modus verwenden, gilt die Einschränkung der Beispiel Block Ausrichtung nicht.

## <a name="adpcm-file-structure"></a>ADPCM-Dateistruktur

Eine ADPCM-Datei ist eine Standard-Riff Datei mit den folgenden Blocktypen.



| Block FCC     | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| RIFF          | Der Standard-Riff Block, der einen Dateityp mit dem Wert Wave in den ersten vier Bytes seines Daten Abschnitts und die anderen Blöcke in der Datei im Rest des Daten Abschnitts enthält.                                                                                                                                                                                                                                                                 |
| fmt           | Enthält den Format Header der ADPCM-Datei. Die Daten in diesem Block entsprechen einer **ADPCMWAVEFORMAT** -Struktur.                                                                                                                                                                                                                                                                                                                             |
| Daten          | Enthält die codierten ADPCM-Audiodaten. Wenn Sie ADPCM in XAudio2 verwenden, müssen Sie den Inhalt des Datensegments in einem Puffer lesen und als **paudiodata** -Member einer [**XAudio2- \_ Puffer**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) Struktur an eine Quell Stimme übergeben. Sie müssen den Inhalt des Datensegments nicht in Byte austauschen.                                                                                                                            |
| SMPL und wsmp | Optionale Blocktypen, die die Schleifen Informationen für die ADPCM-Datei enthalten. Wenn Sie ADPCM in XAudio2 verwenden, werden die in den SMPL-oder wsmp-Blöcken enthaltenen Werte verwendet, um die **loopbeginlooplength** -und **loopCount** -Elemente der [**XAudio2- \_ Puffer**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) Struktur aufzufüllen. Auf der Xbox 360 müssen Sie die aus einem SMPL-Block geladenen Daten in Byte austauschen, um den Byte Reihenfolge-Unterschied zwischen Windows und Xbox 360 zu berücksichtigen. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Programmierhandbuch](programming-guide.md)
</dt> </dl>

 

 
