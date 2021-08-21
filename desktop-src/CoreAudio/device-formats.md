---
description: Geräteformate
ms.assetid: 591437e4-21ef-42f1-a752-7f50440cbd63
title: Geräteformate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 332f3ecd4b30213328552077bdef040a63e31992deaf217b77838dd0cd0797f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957339"
---
# <a name="device-formats"></a>Geräteformate

Bei einer Audioanwendung besteht der Vorteil der Verwendung einer audio-API auf höherer Ebene, z. B. DirectSound oder der Windows-Multimediafunktionen **waveOutXxx,** in der automatischen Konvertierung zwischen den von der Anwendung verwendeten Streamformaten und den vom Audiogerät verwendeten Formaten. Im Gegensatz dazu sind die Kernaudio-APIs restriktiver, da anwendungsstreams Formate verwenden müssen, die mit den vom Gerät verwendeten Formaten identisch sind oder eng mit diesen verknüpft sind. Daher müssen Anwendungen, die die Kernaudio-APIs zum Wieder- oder Aufzeichnen von Audiostreams verwenden, möglicherweise einige oder alle Konvertierungen zwischen Streamformaten machen.

Eine Anwendung, die WASAPI zum Verwalten von Streams im freigegebenen Modus verwendet, kann sich darauf verlassen, dass die Audio-Engine nur eingeschränkte Formatkonvertierungen durchführen kann. Die Audio-Engine kann zwischen einer pcm-Standardbeispielgröße, die von der Anwendung verwendet wird, und den Gleitkommabeispielen konvertieren, die die Engine für die interne Verarbeitung verwendet. Das Format für einen Anwendungsstream muss jedoch in der Regel die gleiche Anzahl von Kanälen und die gleiche Abtastrate wie das vom Gerät verwendete Streamformat haben.

Wenn eine Anwendung ein Gerät im exklusiven Modus verwendet, muss die Anwendung ein Datenstromformat verwenden, das von der Audiohardware explizit unterstützt wird. Im exklusiven Modus tauschen Anwendung und Gerät Audiodaten direkt aus, ohne dass die Audio-Engine eingreifen muss.

Viele Audiogeräte unterstützen sowohl PCM- als auch Nicht-PCM-Streamformate. Die Audio-Engine kann jedoch nur PCM-Streams mischen. Daher können nur Streams im exklusiven Modus Nicht-PCM-Formate haben. Darüber hinaus werden nur Nicht-PCM-Formate mit festen Datenraten im exklusiven Modus unterstützt. Ein Beispiel für ein Nicht-PCM-Format mit festem Rate ist ein 48-kHz-Windows Media Audio Professional(WMA Pro)-Audiostream, der einen Link der digitalen Schnittstelle (S/PDIF) mit 48 kHz in digitaler Form durchläuft, ohne decodiert zu werden. Weitere Informationen zur Verwendung von WMA Pro Streams über S/PDIF finden Sie in der folgenden Dokumentation:

-   Die Beschreibung des Waveformattags \_ WAVE FORMAT \_ WMA \_ BERIF in der Windows DDK-Dokumentation.
-   Das Whitepaper "Audio Driver Support for the WMA Pro-over-S/PDIF Format" auf der Website [Audio Device Technologies for Windows.](https://www.microsoft.com/whdc/device/audio/default.mspx)

WASAPI verwendet eine **WAVEFORMATEX- oder** **WAVEFORMATEXTENSIBLE-Struktur,** um ein Streamformat anzugeben. Eine **WAVEFORMATEXTENSIBLE-Struktur** ist effektiv eine **WAVEFORMATEX-Struktur,** die erweitert wurde, um eine größere Bandbreite von Formaten zu beschreiben. Jedes Format, das von einer eigenständigen **WAVEFORMATEX-Struktur** beschrieben werden kann, kann auch durch eine **WAVEFORMATEXTENSIBLE-Struktur beschrieben** werden.

Das erste Member der **WAVEFORMATEXTENSIBLE-Struktur** ist eine **WAVEFORMATEX-Struktur.** Der Inhalt einer **WAVEFORMATEX-Struktur** gibt an, ob es sich um eine eigenständige **WAVEFORMATEX-Struktur** oder um einen Teil einer **WAVEFORMATEXTENSIBLE-Struktur** handelt.

Eine eigenständige **WAVEFORMATEX-Struktur** kann ein Format mit einem oder zwei Kanälen und einer Stichprobengröße, die ein Vielfaches von 8 Bits ist, angemessen beschreiben. Allein kann eine **WAVEFORMATEX-Struktur** die Zuordnung von Kanälen zu Sprecherpositionen nicht angeben. Obwohl **WAVEFORMATEX** die Größe des Containers für jedes Audiobeispiel angibt, kann es nicht die Anzahl von Genauigkeitsbits in einem Beispiel angeben (z. B. 20 Bits Genauigkeit in einem 24-Bit-Container). Im Gegensatz dazu kann die **WAVEFORMATEXTENSIBLE-Struktur** sowohl die Zuordnung von Kanälen zu Sprechern als auch die Anzahl der Genauigkeitsbits in den einzelnen Stichproben angeben.

Weitere Informationen zu **WAVEFORMATEX und** **WAVEFORMATEXTENSIBLE** finden Sie in der Windows DDK-Dokumentation.

Ab Windows 7 wurde **WAVEFORMATEXTENSIBLE** erweitert, um Geräteformate für die Übertragung codierter Audiodaten über eine IEC 61937-kompatible Schnittstelle zu repräsentieren. Informationen zur neuen -Struktur finden Sie unter [Darstellen von Formaten für IEC 61937 Transmissions](representing-formats-for-iec-61937-transmissions.md).

### <a name="specifying-the-device-format"></a>Angeben des Geräteformats

Die folgenden WASAPI-Methoden verwenden die **STRUKTUREN WAVEFORMATEX und** **WAVEFORMATEXTENSIBLE,** um Streamformate zu beschreiben:

-   [**IAudioClient::GetMixFormat**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getmixformat)
-   [**IAudioClient::IsFormatSupported**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-isformatsupported)
-   [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize)

Die **GetMixFormat-Methode** ruft das Streamformat ab, das die Audio-Engine für die interne Verarbeitung von Datenströmen im freigegebenen Modus verwendet. Die -Methode verwendet immer eine **WAVEFORMATEXTENSIBLE-Struktur** anstelle einer eigenständigen **WAVEFORMATEX-Struktur,** um das Format anzugeben.

Die **IsFormatSupported-Methode** gibt an, ob ein Audioendpunktgerät ein bestimmtes Streamformat unterstützt. Der Aufrufer muss angeben, ob das Streamformat für die Verwendung im freigegebenen Modus oder im exklusiven Modus vorgesehen ist. Bei Formaten im freigegebenen Modus fragt die -Methode die Audio-Engine ab, um zu bestimmen, ob sie das angegebene Format unterstützt. Bei Formaten im exklusiven Modus fragt die -Methode den Gerätetreiber ab. Einige Gerätetreiber melden, dass sie ein 1- oder 2-Kanal-PCM-Format unterstützen, wenn das Format durch eine eigenständige **WAVEFORMATEX-Struktur** angegeben ist, aber das gleiche Format ablehnen, wenn es durch eine **WAVEFORMATEXTENSIBLE-Struktur** angegeben wird. Um zuverlässige Ergebnisse von diesen Treibern zu erhalten, sollten Anwendungen im exklusiven Modus **IsFormatSupported** zweimal für jedes 1- oder 2-Kanal-PCM-Format aufrufen. Ein Aufruf sollte eine eigenständige **WAVEFORMATEX-Struktur** verwenden, um das Format anzugeben, und der andere Aufruf sollte eine **WAVEFORMATEXTENSIBLE-Struktur** verwenden, um das gleiche Format anzugeben.

Nachdem eine Anwendung **GetMixFormat** oder **IsFormatSupported** verwendet hat, um ein geeignetes Format für einen Stream im freigegebenen oder exklusiven Modus zu finden, kann die Anwendung die **Initialize-Methode** aufrufen, um einen Stream mit diesem Format zu initialisieren. Eine Anwendung, die versucht, einen Stream im freigegebenen Modus mit einem Format zu initialisieren, das nicht mit dem von der **GetMixFormat-Methode** erhaltenen Mischungsformat identisch ist, aber über die gleiche Anzahl von Kanälen und die gleiche Abtastrate wie das Mischungsformat verfügt, ist wahrscheinlich erfolgreich. Vor dem **Aufruf von Initialize** kann die Anwendung **IsFormatSupported** aufrufen, um zu überprüfen, **ob Initialize** das Format akzeptiert.

Das Mischungsformat, das die Audio-Engine für die interne Verarbeitung von Datenströmen im freigegebenen Modus verwendet, ist eng mit dem Streamformat verknüpft, das das Audioendpunktgerät im freigegebenen Modus verwendet, ist aber nicht unbedingt identisch. Über die Windows Multimedia-Systemsteuerung Mmsys.cpl der Benutzer das Streamformat auswählen, das ein Audioendpunktgerät verwendet, wenn es im freigegebenen Modus arbeitet. Die Schritte lauten wie folgt:

1.  Öffnen Sie zum Mmsys.cpl ein Eingabeaufforderungsfenster, und geben Sie den folgenden Befehl ein:

    **mmsys.cpl**

    Alternativ können Sie Mmsys.cpl ausführen, indem Sie im Benachrichtigungsbereich rechts auf der Taskleiste mit der rechten Maustaste auf  das Lautsprechersymbol klicken und entweder Wiedergabegeräte oder **Aufzeichnungsgeräte auswählen.**

2.  Nachdem das Mmsys.cpl geöffnet wurde, wählen Sie ein Gerät aus der Liste der Wiedergabegeräte oder der Liste der Aufzeichnungsgeräte aus, und klicken Sie auf **Eigenschaften.**
3.  Wenn das Eigenschaftenfenster geöffnet wird, klicken Sie auf **Erweitert,** und wählen Sie ein Format aus der Liste der verfügbaren Formate im Feld **Standardformat aus.**

Angenommen, der Benutzer wählt das folgende Standardformat aus der Liste der verfügbaren Formate für ein Wiedergabegerät aus:

**2 Kanal, 16 Bit, 44100 Hz (CD-Qualität)**

Dies ist das Format, das das Gerät später verwendet, wenn es im freigegebenen Modus arbeitet. In Windows Vista verwendet die Audio-Engine eine leicht geänderte Version dieses Formats für die interne Verarbeitung von Streams im freigegebenen Modus. Die Audio-Engine verwendet ein Format mit der gleichen Anzahl von Kanälen (zwei) und derselben Abtastrate (44100 Hz), konvertiert jedoch Stichproben in Gleitkommazahlen, bevor sie verarbeitet werden. Die Audio-Engine konvertiert die Gleitkommabeispiele in der Ausgabemischung in 16-Bit-Ganzzahlen, bevor sie über das Gerät abspielt.

Eine Anwendung kann die [**PKEY \_ AudioEngine \_ DeviceFormat-Eigenschaft**](pkey-audioengine-deviceformat.md) eines Audioendpunktgeräts abfragen, um das Vom Benutzer für das Gerät ausgewählte Format im freigegebenen Modus zu erhalten. Informationen zum Abfragen der Eigenschaften eines Geräts finden Sie unter [Geräteeigenschaften](device-properties.md).

Einige Anwendungen finden das von der **PKEY \_ AudioEngine \_ DeviceFormat-Eigenschaft** eines Geräts angegebene Format möglicherweise als geeignetes Format zum Öffnen eines Streams im exklusiven Modus auf dem Gerät. Für andere Anwendungen, die Streams im exklusiven Modus verwalten, gelten möglicherweise zusätzliche Anforderungen, die eine komplexe Formataushandlung mit dem Gerät ersingen. In der Regel erstellt eine dieser Anwendungen eine Liste geeigneter Formate mit den bevorzugten Formaten am Anfang der Liste. Die Anwendung ruft dann iterativ **IsFormatSupported** mit jedem nachfolgenden Format in der Liste ab dem Anfang der Liste auf, bis sie ein Format findet, das vom Gerät unterstützt wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Audioendpunktgeräte](audio-endpoint-devices.md)
</dt> </dl>

 

 



