---
title: Aufzeichnung
description: Aufzeichnung
ms.assetid: 0026eb1d-5be1-4090-801b-f1c65c179f42
keywords:
- MCI_RECORD Befehl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27033dde148a6f99a1168eea4d6c0a97aea82881638ccb6d6f5535632e897148
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119805510"
---
# <a name="recording"></a>Aufzeichnung

Die allgemeine MCI-Spezifikation unterstützt die Aufzeichnung mit Digitalvideo-, VOICE-Sequencer-, Video-Cassette-Aufzeichnungs- (VCR) und Waveform-Audiogeräten. Allerdings implementieren derzeit nur Waveform-Audio- und VCR-Geräte Aufzeichnungsfunktionen. Sie können aufgezeichnete Informationen in eine vorhandene Datei oder einen vorhandenen Datensatz in eine neue Datei einfügen oder überschreiben. Öffnen Sie zum Aufzeichnen in einer vorhandenen Datei wie gewohnt ein Waveform-Audio-Gerät und eine Datei. Geben Sie zum Aufzeichnen in einer neuen Datei beim Öffnen des Geräts "new" als Gerätenamen an, wenn Sie die Befehlszeichenfolgenschnittstelle verwenden. Wenn Sie die Befehlsmeldungsschnittstelle verwenden, geben Sie einen Dateinamen der Länge 0 (null) an.

Wenn MCI eine neue Datei für die Aufzeichnung erstellt, wird das Datenformat auf ein vom Gerätetreiber angegebenes Standardformat festgelegt. Um ein anderes Format als das Standardformat zu verwenden, können Sie den Befehl [**set**](set.md) ([**MCI \_ SET**](mci-set.md)) verwenden.

Verwenden Sie zum Starten der Aufzeichnung den [**Befehl record**](record.md) (oder [**MCI \_ RECORD**](mci-record.md) und die [**MCI RECORD \_ \_ PARMS-Struktur).**](mci-record-parms.md)

Wenn Sie im Einfügemodus eine vorhandene Datei aufzeichnen, können Sie die Flags "from" (MCI FROM) und \_ "to" (MCI TO) des Datensatzbefehls verwenden, um Start- und Endpositionen für die Aufzeichnung \_ anzugeben.  Wenn Sie z. B. in einer Datei aufzeichnen, die 20 Sekunden lang ist, mit der Aufzeichnung beginnen und die Aufzeichnung bei 5 Sekunden beginnen und die Aufzeichnung bei 10 Sekunden beenden, ist die resultierende Datei 25 Sekunden lang. Die Datei enthält ein 5-Sekunden-Segment, das 5 Sekunden in die ursprüngliche Aufzeichnung eingefügt wird.

Wenn Sie den Überschreibungsmodus für eine vorhandene Datei aufzeichnen, können Sie die Flags "from" und "to" verwenden, um Start- und Endorte des abschnitts anzugeben, der überschrieben wird. Wenn Sie z. B. eine Aufzeichnung in einer Datei mit einer Länge von 20 Sekunden erstellen und mit der Aufzeichnung mit 5 Sekunden beginnen und die Aufzeichnung mit 10 Sekunden beenden, verfügen Sie immer noch über eine Aufzeichnung von 20 Sekunden, aber der Abschnitt, der bei 5 Sekunden beginnt und bei 10 Sekunden endet, wurde ersetzt.

Wenn Sie keinen Endspeicherort angeben, wird [](stop.md) die Aufzeichnung fortgesetzt, bis Sie einen Stoppbefehl [**(MCI \_ STOP**](mci-stop.md)) senden oder bis dem Treiber der freie Speicherplatz auf dem Datenträger nicht mehr zur Verfügung steht. Wenn Sie in einer neuen Datei aufzeichnen, können Sie das Flag "from" weglassen oder auf 0 (null) festlegen, um die Aufzeichnung am Anfang einer neuen Datei zu starten. Sie können einen Endspeicherort angeben, um die Aufzeichnung bei der Aufzeichnung in einer neuen Datei zu beenden.

Der [**Befehl record**](record.md) ist manchmal innerhalb von nur einer Sekunde des Startorts genau, z. B. bei VCR-Geräten. Um eine genauere Aufzeichnung zu erhalten, sollten Sie den [**Befehl cue**](cue.md) ([**MCI \_ CUE**](mci-cue.md)) verwenden. Dieser Befehl wird von digital-video-, VCR- und waveform-audio-Geräten erkannt. Weitere Informationen zur Aufzeichnung mit VCR-Geräten finden Sie unter [VCR-Dienste.](vcr-services.md)

## <a name="saving-a-recorded-file"></a>Speichern einer aufgezeichneten Datei

Wenn die Aufzeichnung abgeschlossen [](save.md) ist, verwenden Sie den Speicherbefehl (oder [**MCI \_ SAVE**](mci-save.md) und die [**MCI \_ SAVE \_ PARMS-Struktur),**](mci-save-parms.md) um die Aufzeichnung vor dem Schließen des Geräts zu speichern.

> [!Note]  
> Wenn Sie das Gerät schließen, ohne es zu speichern, gehen die aufgezeichneten Daten verloren.

 

## <a name="checking-input-levels-pcm-only"></a>Überprüfen von Eingabeebenen (nur PCM)

Verwenden Sie den Befehl [**status**](status.md) ([**MCI \_ STATUS**](mci-status.md)), um die Stufe des Eingabesignals vor der Aufzeichnung auf einem PCM-Waveform-Audioeingabegerät (Pulse Code WaveForm) zu erhalten. Geben Sie das Flag "level" an (oder das MCI STATUS ITEM-Flag, und legen Sie das \_ \_ **dwItem-Element** der [**MCI \_ STATUS \_ PARMS-Struktur**](mci-status-parms.md) auf MCI \_ WAVE STATUS LEVEL \_ \_ fest). Die durchschnittliche Eingabesignalstufe wird zurückgegeben. Der Wert des linken Kanals befindet sich im hochwertigen Wort, und der Rechte- oder Monokanalwert befindet sich im niedrigwertigen Wort.

Die Eingabeebene wird als Wert ohne Vorzeichen dargestellt. Bei 8-Bit-Beispielen liegt dieser Wert im Bereich von 0 bis 127 (0x7F). Bei 16-Bit-Beispielen liegt sie im Bereich von 0 bis 32.767 (0x7FFF).

 

 




