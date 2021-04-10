---
description: Geräte Formate
ms.assetid: 591437e4-21ef-42f1-a752-7f50440cbd63
title: Geräte Formate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbcd1b611075191e522cf00d959f120abfb3baa9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104125762"
---
# <a name="device-formats"></a>Geräte Formate

Bei einer Audioanwendung hat der Vorteil, dass eine Audio-API auf höherer Ebene wie DirectSound oder die Windows Multimedia **waveoutxxx** -Funktionen verwendet werden soll, dass die API automatisch zwischen den streamformaten konvertiert, die von der Anwendung verwendet werden, und den vom Audiogerät verwendeten Formaten. Im Gegensatz dazu sind die Kern-audioapis restriktiver, da Sie erfordern, dass Anwendungsdaten Ströme Formate verwenden, die mit den vom Gerät verwendeten Formaten identisch sind. Daher müssen Anwendungen, die die kernaudioapis verwenden, um Audiostreams wiederzugeben oder zu aufzeichnen, möglicherweise einige oder alle Konvertierungen zwischen streamformaten ausführen.

Eine Anwendung, die WASAPI zum Verwalten von Datenströmen im freigegebenen Modus verwendet, kann das Audiomodul verwenden, um nur begrenzte Formatkonvertierungen auszuführen. Die Audioengine kann zwischen einer standardmäßigen PCM-Stichprobengröße, die von der Anwendung verwendet wird, und den Gleit Komma Beispielen, die von der Engine für die interne Verarbeitung verwendet werden, konvertieren. Allerdings muss das Format für einen Anwendungsstream in der Regel die gleiche Anzahl von Kanälen und die gleiche Stichprobenrate wie das vom Gerät verwendete Streamformat aufweisen.

Wenn eine Anwendung ein Gerät im exklusiven Modus verwendet, muss die Anwendung ein Streamformat verwenden, das von der Audiohardware explizit unterstützt wird. Im exklusiven Modus tauschen die Anwendung und das Gerät Audiodaten direkt, ohne Eingriff durch die Audioengine.

Viele Audiogeräte unterstützen sowohl PCM-als auch nicht-PCM-Streamingformate. Die Audioengine kann jedoch nur PCM-Streams mischen. Folglich können nur exklusive streamingdatenströme nicht-PCM-Formate aufweisen. Außerdem werden nur nicht-PCM-Formate mit fester Daten Rate im exklusiven Modus unterstützt. Ein Beispiel für ein nicht-PCM-Format mit fester Geschwindigkeit ist ein "48-kHz Windows Media Audio Professional (WMA Pro)"-Audiostream, der über einen Digital Form-Link (S/PDIF) mit einer digitalen Sony/ Weitere Informationen zur Verwendung von WMA pro-Streams über S/PDIF finden Sie in der folgenden Dokumentation:

-   Die Beschreibung des-Tags für das Wave \_ \_ -Format WMA \_ SPDIF Wave-Format in der Windows DDK-Dokumentation.
-   Das Whitepaper "audiotreiberunterstützung für das WMA pro-Over-S/PDIF-Format" auf der Website mit den [audiogerätetechnologien für Windows](https://www.microsoft.com/whdc/device/audio/default.mspx) .

WASAPI verwendet eine **WaveFormatEx** -oder **WAVEFORMATEXTENSIBLE** -Struktur, um ein Streamformat anzugeben. Eine **WAVEFORMATEXTENSIBLE** -Struktur ist effektiv eine **WaveFormatEx** -Struktur, die erweitert wurde, um einen größeren Bereich von Formaten zu beschreiben. Jedes Format, das von einer eigenständigen **WaveFormatEx** -Struktur beschrieben werden kann, kann auch durch eine **WAVEFORMATEXTENSIBLE** -Struktur beschrieben werden.

Der erste Member der **WAVEFORMATEXTENSIBLE** -Struktur ist eine **WaveFormatEx** -Struktur. Der Inhalt einer **WaveFormatEx** -Struktur zeigt an, ob es sich um eine eigenständige **WaveFormatEx** -Struktur oder einen Teil einer **WAVEFORMATEXTENSIBLE** -Struktur handelt.

Eine eigenständige **WaveFormatEx** -Struktur kann ein Format mit einem oder zwei Kanälen und einer Stichprobengröße, die ein Vielfaches von 8 Bits ist, adäquat beschreiben. Eine **WaveFormatEx** -Struktur kann nicht die Zuordnung von Kanälen zu Redner Positionen angeben. Obwohl **WaveFormatEx** die Größe des Containers für die einzelnen Audiobeispiele angibt, kann es nicht die Anzahl der Genauigkeits Bits in einem Beispiel angeben (z. b. 20 Bits der Genauigkeit in einem 24-Bit-Container). Im Gegensatz dazu kann die **WAVEFORMATEXTENSIBLE** -Struktur sowohl die Zuordnung von Kanälen zu Referenten als auch die Anzahl der Genauigkeits Bits in jedem Beispiel angeben.

Weitere Informationen zu **WaveFormatEx** und **WAVEFORMATEXTENSIBLE** finden Sie in der Windows-DDK-Dokumentation.

Ab Windows 7 wurde das **WAVEFORMATEXTENSIBLE** -Gerät so erweitert, dass es Geräte Formate zum Übertragen von codiertem Audiodaten über eine mit IEC 61937 kompatible Schnittstelle darstellt. Weitere Informationen zur neuen Struktur finden Sie unter [darstellen von Formaten für IEC 61937-Übertragungen](representing-formats-for-iec-61937-transmissions.md).

### <a name="specifying-the-device-format"></a>Angeben des Geräte Formats

Die folgenden WASAPI-Methoden verwenden die **Wellen FORMATEX** -und **WAVEFORMATEXTENSIBLE** -Strukturen, um Streamingformate zu beschreiben:

-   [**Iaudioclient:: getmixformat**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getmixformat)
-   [**Iaudioclient:: isformatsupported**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-isformatsupported)
-   [**Iaudioclient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize)

Die **getmixformat** -Methode ruft das Streamformat ab, das die Audioengine für die interne Verarbeitung von Streams im freigegebenen Modus verwendet. Die-Methode verwendet immer eine **WAVEFORMATEXTENSIBLE** -Struktur anstelle einer eigenständigen **WaveFormatEx** -Struktur, um das Format anzugeben.

Die **isformatsupported** -Methode gibt an, ob ein audioendpunktgerät ein bestimmtes Streamformat unterstützt. Der Aufrufer muss angeben, ob das Stream-Format für die Verwendung im freigegebenen Modus oder im exklusiven Modus vorgesehen ist. Bei Formaten im freigegebenen Modus fragt die-Methode die Audioengine ab, um zu bestimmen, ob Sie das angegebene Format unterstützt. Bei Formaten im exklusiven Modus fragt die Methode den Gerätetreiber ab. Einige Gerätetreiber melden, dass Sie ein 1-Kanal-oder 2-Kanal-PCM-Format unterstützen, wenn das Format durch eine eigenständige **WaveFormatEx** -Struktur angegeben wird, aber das gleiche Format ablehnen, wenn es durch eine **WAVEFORMATEXTENSIBLE** -Struktur angegeben wird. Um zuverlässige Ergebnisse von diesen Treibern zu erhalten, sollten Anwendungen im exklusiven Modus für jedes 1-Kanal-oder 2-Kanal-PCM-Format für die Verwendung von **isformatsupported** zweimal aufgerufen werden – ein-Befehl sollte eine eigenständige **WaveFormatEx** -Struktur verwenden, um das Format anzugeben, und der andere-Befehl sollte eine **WAVEFORMATEXTENSIBLE** -Struktur verwenden, um das gleiche Format anzugeben.

Nachdem eine Anwendung **getmixformat** oder **isformatsupported** verwendet hat, um ein entsprechendes Format für einen Stream im freigegebenen Modus oder im exklusiven Modus zu finden, kann die Anwendung die **initialisieren** -Methode aufrufen, um einen Stream mit diesem Format zu initialisieren. Eine Anwendung, die versucht, einen Stream im freigegebenen Modus mit einem Format zu initialisieren, das nicht mit dem Mischungs Format identisch ist, das von der **getmixformat** -Methode abgerufen wurde, aber die gleiche Anzahl von Kanälen und die gleiche Stichprobenrate wie das Mischungs Format aufweist, ist wahrscheinlich erfolgreich. Vor dem Aufrufen von **Initialize** kann die Anwendung **isformatsupported** aufrufen, um zu überprüfen, ob die **Initialisierung** das Format akzeptiert.

Das Mischungs Format, das die Audioengine für die interne Verarbeitung von Streams im freigegebenen Modus verwendet, ist eng mit dem Streamformat verknüpft, das vom audioendpunktgerät im freigegebenen Modus verwendet wird. Über die Windows-Multimedia-Systemsteuerung Mmsys.cpl kann der Benutzer das Streamformat auswählen, das von einem audioendpunktgerät verwendet wird, wenn es im freigegebenen Modus betrieben wird. Die Schritte lauten wie folgt:

1.  Öffnen Sie zum Ausführen Mmsys.cpl ein Eingabe Aufforderungs Fenster, und geben Sie den folgenden Befehl ein:

    **Steuerelement mmsys.cpl**

    Alternativ dazu können Sie Mmsys.cpl ausführen, indem Sie mit der rechten Maustaste auf das Redner Symbol im Benachrichtigungsbereich klicken, der sich auf der rechten Seite der Taskleiste befindet, und entweder **Geräte wieder** geben oder **Geräte aufzeichnen** auswählen.

2.  Wählen Sie nach dem Öffnen des Fensters Mmsys.cpl in der Liste der Wiedergabe Geräte oder der Liste der Aufzeichnungsgeräte ein Gerät aus, und klicken Sie auf **Eigenschaften**.
3.  Wenn das Fenster Eigenschaften geöffnet wird, klicken Sie auf **erweitert**, und wählen Sie in der Liste der verfügbaren Formate in dem Feld mit der Bezeichnung **Standardformat** ein Format aus.

Nehmen Sie beispielsweise an, dass der Benutzer das folgende Standardformat aus der Liste der verfügbaren Formate für ein Wiedergabe Gerät auswählt:

**2 Channel, 16 Bit, 44100 Hz (CD-Qualität)**

Dies ist das Format, das das Gerät anschließend verwendet, wenn es im freigegebenen Modus betrieben wird. In Windows Vista verwendet die Audioengine eine etwas geänderte Version dieses Formats für die interne Verarbeitung von Streams im freigegebenen Modus. Die Audioengine verwendet ein Format mit der gleichen Anzahl von Kanälen (zwei) und derselben Samplingrate (44100 Hz), konvertiert jedoch vor der Verarbeitung Beispiele in Gleit Komma Zahlen. Die Audioengine konvertiert die Gleit Komma Beispiele in der Ausgabe Mischung in 16-Bit-Ganzzahlen, bevor Sie auf dem Gerät wiedergegeben werden.

Eine Anwendung kann die [**pkey \_ Audioengine \_ deviceformat**](pkey-audioengine-deviceformat.md) -Eigenschaft eines audioendpunkts Abfragen, um das Format für den freigegebenen Modus abzurufen, den der Benutzer für das Gerät ausgewählt hat. Informationen zum Abfragen der Eigenschaften eines Geräts finden Sie unter [Geräteeigenschaften](device-properties.md).

Einige Anwendungen finden das Format, das von der **pkey \_ Audioengine \_ deviceformat** -Eigenschaft eines Geräts angegeben wurde, als geeignetes Format zum Öffnen eines Streams im exklusiven Modus auf dem Gerät. Andere Anwendungen, die Datenströme im exklusiven Modus verwalten, verfügen möglicherweise über zusätzliche Anforderungen, die eine komplexe formataushandlung mit dem Gerät vorschreiben. In der Regel erstellt eine dieser Anwendungen eine Liste geeigneter Formate mit den bevorzugten Formaten am Anfang der Liste. Die Anwendung ruft dann iterativ **isformatsupported** mit jedem aufeinander folgenden Format in der Liste ab, beginnend am Anfang der Liste, bis ein vom Gerät unterstütztes Format gefunden wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Audioendpunktgeräte](audio-endpoint-devices.md)
</dt> </dl>

 

 



