---
title: Aufzeichnung
description: Aufzeichnung
ms.assetid: 0026eb1d-5be1-4090-801b-f1c65c179f42
keywords:
- MCI_RECORD-Befehl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4248b2d4bbdd984ad23a772f0adca04581afca1d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106338367"
---
# <a name="recording"></a>Aufzeichnung

Die allgemeine MCI-Spezifikation unterstützt das Aufzeichnen mit Digital Video-, MIDI Sequencer-, Video-Kassettenrecorder (VCR)-und Waveform-Audiogeräten. Allerdings implementieren derzeit nur Waveform-Audiodaten und VCR-Geräte Aufzeichnungsfunktionen. Sie können aufgezeichnete Informationen in eine vorhandene Datei oder einen vorhandenen Datensatz in eine neue Datei einfügen oder überschreiben. Um eine vorhandene Datei aufzuzeichnen, öffnen Sie wie gewohnt ein Waveform-Audiogerät und eine Datei. Wenn Sie das Gerät öffnen, geben Sie beim Öffnen des Geräts "New" als Gerätenamen an, wenn Sie die Befehlszeilenschnittstelle verwenden. Wenn Sie die befehlsnachrichten Schnittstelle verwenden, geben Sie einen Dateinamen mit der Länge 0 (null) an.

Wenn MCI eine neue Datei für die Aufzeichnung erstellt, wird das Datenformat auf ein vom Gerätetreiber festgelegtes Standardformat festgelegt. Wenn Sie ein anderes Format als das Standardformat verwenden möchten, können Sie den [**Set**](set.md) ([**MCI \_ set**](mci-set.md))-Befehl verwenden.

Um mit der Aufzeichnung zu beginnen, verwenden Sie den [**Datensatz**](record.md) -Befehl (oder den [**MCI- \_ Datensatz**](mci-record.md) und die Struktur der [**MCI- \_ Daten Satz \_**](mci-record-parms.md) Struktur).

Wenn Sie im Einfügemodus eine vorhandene Datei aufzeichnen, können Sie die \_ Start-und Endpositionen für die Aufzeichnung mithilfe der Flags "from" (MCI from) und "to" (MCI \_ to) des **Daten Satz** Befehls angeben. Wenn Sie z. b. in einer Datei aufzeichnen, die 20 Sekunden lang ist, und Sie mit der Aufzeichnung von 5 Sekunden beginnen und die Aufzeichnung bei 10 Sekunden beenden, ist die resultierende Datei 25 Sekunden lang. Die Datei enthält ein 5-Sekunden-Segment, das 5 Sekunden in die ursprüngliche Aufzeichnung eingefügt wird.

Wenn Sie den Überschreibungs Modus für eine vorhandene Datei aufzeichnen, können Sie die Flags "from" und "to" verwenden, um die Start-und Endpositionen des Abschnitts anzugeben, der überschrieben wird. Wenn Sie z. b. in einer Datei aufzeichnen, die 20 Sekunden lang ist, und Sie mit der Aufzeichnung von 5 Sekunden beginnen und die Aufzeichnung bei 10 Sekunden beenden, haben Sie immer noch eine Aufzeichnung von 20 Sekunden, aber der Abschnitt, der mit 5 Sekunden beginnt und mit 10 Sekunden endet, wird ersetzt.

Wenn Sie keinen endspeicherort angeben, wird die Aufzeichnung fortgesetzt, bis Sie einen Befehl zum [**Beenden**](stop.md) ([**MCI- \_ Beenden**](mci-stop.md)) senden oder bis der freie Speicherplatz für den Treiber nicht mehr zur Verfügung steht. Wenn Sie in einer neuen Datei aufzeichnen, können Sie das Flag "from" weglassen oder es auf NULL festlegen, um die Aufzeichnung am Anfang einer neuen Datei zu starten. Sie können einen endspeicherort angeben, um die Aufzeichnung beim Aufzeichnen in eine neue Datei zu beenden.

Der [**Datensatz**](record.md) -Befehl ist manchmal nur innerhalb von 1 Sekunde des Start Speicher Orts, z. b. bei VCR-Geräten, genau. Um [**die Daten**](cue.md) genauer aufzuzeichnen, sollten Sie den Hinweis Befehl ([**MCI- \_ Hinweis)**](mci-cue.md)verwenden. Dieser Befehl wird von Digital-Video-, VCR-und Waveform-Audiogeräten erkannt. Weitere Informationen zum Aufzeichnen von VCR-Geräten finden Sie unter [VCR-Dienste](vcr-services.md).

## <a name="saving-a-recorded-file"></a>Speichern einer aufgezeichneten Datei

Wenn die Aufzeichnung abgeschlossen ist, verwenden Sie den Befehl [**Speichern**](save.md) (oder [**MCI- \_ Speicher**](mci-save.md) und die MCI-Struktur zum [**Speichern von \_ \_ Parametern**](mci-save-parms.md) ), um die Aufzeichnung vor dem Schließen des Geräts zu speichern.

> [!Note]  
> Wenn Sie das Gerät schließen, ohne zu speichern, gehen die aufgezeichneten Daten verloren.

 

## <a name="checking-input-levels-pcm-only"></a>Überprüfen von Eingabe Ebenen (nur PCM)

Um die Ebene des Eingabe Signals vor der Aufzeichnung auf einem PCM (Pulse Code Modulation) Waveform-Audioeingabegerät zu erhalten, verwenden Sie den Befehl [**Status**](status.md) ([**MCI- \_ Status**](mci-status.md)). Geben Sie das Flag "Level" (oder das MCI \_ \_ -statuselementflag) an, und legen Sie das Element " **dwitem** " der [**MCI- \_ \_ statusparametestruktur**](mci-status-parms.md) auf MCI \_ Wave \_ Status \_ Level fest. Die durchschnittliche Eingabe Signalebene wird zurückgegeben. Der linke channelwert befindet sich im höherwertigen Wort, und der Right-oder Mono-Channel-Wert ist das nieder wertige Wort.

Die Eingabe Ebene wird als Wert ohne Vorzeichen dargestellt. Bei 8-Bit-Stichproben liegt dieser Wert im Bereich von 0 bis 127 (0x7f). Für 16-Bit-Beispiele liegt der Bereich zwischen 0 und 32.767 (0x7FFF).

 

 




