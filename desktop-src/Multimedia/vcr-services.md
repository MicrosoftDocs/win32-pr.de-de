---
title: VCR-Dienste
description: VCR-Dienste
ms.assetid: 140220f7-df7b-46e2-8374-e1200d873f3b
keywords:
- Video System Control Architecture (VISCA)
- VISCA (Video System Control Architecture)
- MCI VISCA-Treiber
- VISCA-Treiber
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0397e56c589c357edc9e0be1999b51d358f8caced60117af5c20c7954a1edb49
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119804520"
---
# <a name="vcr-services"></a>VCR-Dienste

Windows bietet VCR-Dienste über einen Gerätetreiber, der auf dem MCI-Befehlssatz für VCRs basiert. In diesem Abschnitt wird der VISCA-Treiber (Video System Control Architecture) von MCI beschrieben, und es wird erläutert, wie dieser zum Steuern eines VCR verwendet wird.

Der *Vcr-Gerätetyp* steuert VCRs. Eine Liste der von VCR-Geräten erkannten MCI-Befehle finden Sie unter [VCR-Befehlssatz.](vcr-command-set.md)

## <a name="the-mci-visca-driver"></a>Der MCI VISCA-Treiber

Der MCI VISCA-Treiber steuert Viska-kompatible VCRs, z. B. CVD-1000 VDeck. Der VISCA-Treiber steuert den Bandtransport, Kanal tuner und VCR-Eingabe- und -Ausgabekanäle.

## <a name="searching-and-positioning-with-a-vcr"></a>Suchen und Positionieren mit einem VCR

Der VISCA-Treiber verwendet zwei Methoden zum Nachverfolgen der Videobandbewegung innerhalb des VCR-Bandtransports: *Zeitcodeinformationen* und *Bandzähler.* Timecodeinformationen sind Zeitsteuerungsinformationen, die im Video aufgezeichnet wurden. Die meisten VCRs ermöglichen die Aufzeichnung von Zeitcodes, ohne Audio- und Videospuren zu zerstören. Bandzähler schätzen die Menge des Videobands, das über den Videobandkopf verläuft, um eine Position zu erhalten.

Sowohl Zeitcodeinformationen als auch Bandzähler erhöhen sich, wenn das Videoband von Anfang zu Ende wechselt. Aufgrund seiner Genauigkeit ist die Verwendung von Zeitcodeinformationen zum Positionieren eines Videotapes fast immer der Verwendung von Bandzählern vorzuziehen.

Die MCI-Befehlsflags zum Angeben von Positionierungsinformationen werden als Zeitabhängigkeiten ausgedrückt: "zeitformat", "duration", "from", "to" und "seek". (Außerdem gibt der [**Befehl status**](status.md) "position" seinen Zeitwert im aktuellen Zeitformat zurück.)

Der VISCA-Treiber verwendet den [**festgelegten**](set.md) Befehl "Zeitmodus", um den Typ der Positionierung auszuwählen, der mit einem Videotape verwendet werden soll. Wenn der Zeitmodus auf "timecode"  festgelegt ist, verwenden die Statusbefehle "position" und **"time** format" den Zeitcode im Videotape. Wenn der Zeitmodus auf "counter" festgelegt ist, verwenden die **Statusbefehle** "position" und **"time** format" (Zeitformat festlegen) Leistungsindikatoren.

Eine Anwendung kann den Zeitmodus auf "detect" festlegen, wenn es keine Rolle spielt, dass zwei Quellen von Positionsinformationen verfügbar sind. Im Erkennungsmodus verwendet der VISCA-Treiber Zeitcodeinformationen für die Positionierung, wenn eine der folgenden Bedingungen auftritt:

-   Die Zeitcodeinformationen sind vorhanden, wenn der Treiber geöffnet wird.
-   Sie ändern ein Videoband mit dem festgelegten **Befehl** "Door Open", und Zeitcodeinformationen sind im Videotape vorhanden.
-   Der [**Befehl**](set.md) "Zeitmodus festlegen" wird erneut ausgegeben.

Wenn keine Zeitcodeinformationen gefunden werden können, verwendet der Treiber die Bandzähler.

Um die aktuelle Positionierungsmethode zu bestimmen, geben Sie den [**Statusbefehl**](status.md) "Zeittyp" aus, der entweder "timecode" oder "counter" zurückgibt. Sie können den aktuellen Positionierungsmodus  auch mithilfe des Statusbefehls "Zeitmodus" identifizieren, der "timecode", "counter" oder "detect" zurückgibt.

Der **Statusbefehl** "counter" ruft den aktuellen Bandzählerwert ab, unabhängig von der aktuellen Positionierungsmethode. Sie können diesen Indikator jedoch nur mit dem Befehl [**"counter"**](set.md) festlegen.

Der VISCA-Treiber kann das systemeigene Zeitcodeformat, das  auf einem Videoband aufgezeichnet wurde, mithilfe der Befehle "Timecodetyp" und "Bildfrequenz" abrufen.  Wenn der Timecodetyp beispielsweise "smpte" und die Framerate 25 ist, ist das systemeigene Zeitcodeformat, das auf dem Videoband aufgezeichnet wird, SMPTE 25.

Der VISCA-Treiber kann die Zählerauflösung auch mithilfe des Statusbefehls **"Counter** resolution" abrufen, der "Sekunden" oder "Frames" zurückgibt. Das Zählerformat kann weiterhin auf SMPTE 30 festgelegt werden, aber der Rückgabewert gibt nur einen Frame von 0 zurück. Wenn der aktuelle Zeittyp counter ist, gilt diese Auflösung  auch für den Wert, der vom Status "position" zurückgegeben wird.

## <a name="capturing-frames"></a>Erfassen von Frames

Frameerfassungsbefehle stellen Noch-Bilder für ein *Frame-Capture-Gerät zur Verfügung.* Ein Frame-Capture-Gerät ist ein separater Hardwareteil, der das Videobild lesen und speichern kann. Der VISCA-Treiber unterstützt den [**Befehl freeze**](freeze.md) ([**MCI \_ FREEZE**](mci-freeze.md)), um ein Standbild für die Erfassung zu stabil zu machen. Außerdem kann der [**Befehl unfreeze**](unfreeze.md) ([**MCI \_ UNFREEZE**](mci-unfreeze.md)) verwendet werden, um den Bandtransport nach einem **Freeze-Befehl neu zu** starten.

Der **Freeze-Befehl** bietet ein hochwertiges, stabilisiertes, zeitbasiertes, korrigiertes Bild für ein Frameerfassungsgerät. Dieser Befehl ist vorhanden, da ein Gerät möglicherweise nicht immer sein Ausgabebild mit maximaler Qualität während der Wiedergabe oder während des Anhaltens liefert. ein solches Videobild ist nicht für die Erfassung geeignet.

Der **Befehl unfreeze** entsperrt den Bandtransport und setzt den transport-Modus vor dem **Freeze-Befehl** wieder in Kraft.

Wenn Ihre Anwendung ein Videobild im VCR  aufzeichnen muss, verwenden Sie den Befehl "input" einfrieren oder den [**Cue**](cue.md) -Befehl ([**MCI \_ CUE**](mci-cue.md)), um das Bild zu erfassen.

## <a name="selecting-inputs"></a>Auswählen von Eingaben

Der VISCA-Treiber unterstützt drei Eingabetypen: Video, Audio und Zeitcode. Die Videoeingaben umfassen zwei Standardkanäle (Zeilen 1 und 2), einen SVideo-Kanal, einen Hilfskanal und einen Kanal von einem internen Tuner. Die Audioeingaben umfassen zwei Standardkanäle (Zeilen 1 und 2) und einen Kanal von einem internen Tuner. Die Zeitcodeeingabe ist für den VCR intern.

Die normalen Ausgaben tragen die aktuell ausgewählten Eingaben, wenn der VCR aufzeichnen oder wenn der Bandtransport beendet wird, und sie tragen den Inhalt des Videobands, wenn der Bandtransport abspielt oder angehalten wird. Die überwachten Ausgaben enthalten die gleichen Informationen wie die normalen Ausgaben sowie aktuelle Zeitcode- und Kanalinformationen.

Wenn die entsprechenden externen Eingaben mit Ihrem VCR verbunden sind und Sie entschieden haben, was Sie aufzeichnen möchten, können Sie die zu notierenden Eingaben auswählen. Wenn Sie beispielsweise die Audioeingaben "svideo" und "line 1" aufzeichnen oder anzeigen möchten, verwenden Sie die Befehle [**setvideo**](setvideo.md) ([**MCI \_ SETVIDEO**](mci-setvideo.md)) und [**setaudio**](setaudio.md) ([**MCI \_ SETAUDIO**](mci-setaudio.md)), um diese Eingabequellen auszuwählen. Sie können diese Auswahl mithilfe des Befehls [**status**](status.md) ([**MCI \_ STATUS**](mci-status.md)) überprüfen.

Standardmäßig zeigt der Monitor genau an, was als Ausgabe angezeigt wird. Manchmal möchten Sie jedoch eine Quelle während der Aufzeichnung von einer anderen anzeigen. Dies ist eine gängige Vorgehensweise bei der Verwendung des Tuners. Sie können z. B. Channel 4 ansehen, während Sie Channel 7 aufzeichnen. In diesem Fall verfügen Sie über zwei logische Tunereingaben. Sie können den VCR mit den folgenden Befehlen einrichten:

## <a name="to-review-one-source-while-recording-from-another"></a>So überprüfen Sie eine Quelle während der Aufzeichnung von einer anderen

1.  Verwenden Sie [**den Befehl settuner**](settuner.md) ([**MCI \_ SETTUNER**](mci-settuner.md)), um die Kanäle auszuwählen, die sie ansehen und aufzeichnen.
2.  Verwenden Sie **den Befehl setvideo,** um die Videoaufzeichnungsquelle auszuwählen.
3.  Verwenden Sie [**den Befehl setaudio,**](setaudio.md) um die Audioaufzeichnungsquelle auszuwählen.
4.  Verwenden Sie [**den Befehl setvideo,**](setvideo.md) um die Channel 4-Videoeingabe an die überwachte Ausgabe weiter zu routen, um sie auf dem Bildschirm anzuzeigen.
5.  Verwenden Sie [**den Befehl setaudio,**](setaudio.md) um die Audioeingabe von Channel 4 an die überwachte Ausgabe weiter zu routen, um die Audiowiedergabe auszuführen.
6.  Überprüfen Sie Ihre Auswahl mithilfe des [**Statusbefehls.**](status.md)

Der VISCA-Treiber unterstützt auch einen speziellen Eingabetyp für Audio und Video namens *stumm.* Stummschalten ermöglicht die Auswahl von "Keine Eingabe", was bei der Aufzeichnung eines leeren Signals nützlich ist.

## <a name="selecting-recording-tracks"></a>Auswählen von Aufzeichnungsspuren

Auf einem Videoband gibt es drei Arten von Aufzeichnungsspuren: Video, Audio und Zeitcode. Sie verfügen nur über eine Video- oder Zeitcodespur, aber Sie können mehrere Audiospuren verwenden. Wenn Sie dies tun, machen Sie Track 1 zur Hauptaudiospur.

Der VISCA-Treiber unterstützt zwei Betriebsmodi: Zusammenstellen und Einfügen. Im *Assemblermodus* werden alle Spuren ausgewählt, um aufgezeichnet zu werden. Im *Einfügemodus* können Spuren unabhängig für die Aufzeichnung ausgewählt werden. Die meisten VCRs befinden sich standardmäßig im Assemblermodus. Verwenden Sie [**den Befehl set**](set.md) ([**MCI \_ SET**](mci-set.md)), um diese Modi zu ändern.

## <a name="recording-and-editing"></a>Aufzeichnung und Bearbeitung

Der [**Befehl record**](record.md) ([**MCI \_ RECORD**](mci-record.md)) bietet eine einfache Aufzeichnung und ist auf ca. 1 Sekunde der Anfangsposition genau. Verwenden Sie den Befehl [**cue**](cue.md) ([**MCI \_ CUE**](mci-cue.md)), um die Aufzeichnung genauer zu machen, oder wenn Sie erwarten, den Videoinhalt zu bearbeiten, während Sie mehrere Karten gleichzeitig ausführen.

Der **Cue-Befehl** bereitet das Gerät für die Aufzeichnung oder Wiedergabe vor. Verwenden Sie den **Befehl cue** "input", um das Gerät für die Aufzeichnung vorzubereiten. Der **Cue-Befehl** ist erforderlich, da eine Anwendung wissen muss, wann das Gerät zum Ausführen des Befehls bereit ist (und da es einige Minuten dauern kann, sich auf ein Play [**vorzubereiten**](play.md) ([**MCI \_ PLAY**](mci-play.md)) oder einen Aufzeichnungsbefehl). 

Der VCR bereitet sich auf die Aufzeichnung oder Wiedergabe vor, indem er nach dem  *In-Point sucht,* bei dem es sich um die aktuelle Position oder die Position handelt, die mithilfe des Befehls "from" angegeben wird. Wenn das Flag "preroll" jedoch mit dem **Cue-Befehl** angegeben wird, positioniert sich der VCR selbst in der Vorabrolldistanz vom In-Point- Das Flag "Preroll" gibt auch an, dass der VCR einen beliebigen anwendbaren Bearbeitungsmodus verwendet. Daher ist es wichtig, dass Sie "Preroll" verwenden, insbesondere wenn Sie die genaueste Aufzeichnung wünschen. (Verwenden Sie [**den Befehl capability**](capability.md) ([**MCI \_ GETDEVCAPS**](mci-getdevcaps.md)) mit dem Flag "can preroll", um zu überprüfen, ob der Vorabrollmodus unterstützt wird.)

> [!Note]  
> Wenn Sie mithilfe von "from"- und "to"-Positionen aufzeichnen, wird die Position "from" in die Bearbeitung einbezogen, und die Position "to" nicht.

 

Weitere Informationen zur Aufzeichnung finden Sie unter [Aufzeichnung von](recording.md).

## <a name="using-the-clock-while-editing"></a>Verwenden der Uhr während der Bearbeitung

Bei der Bearbeitung möchten Sie möglicherweise Segmente von einem VCR zu einem anderen aufzeichnen. Sie können die Aufzeichnung zu einem bestimmten Zeitpunkt und an einer bestimmten Position auf einem VCR beginnen, während ein anderer zur gleichen Zeit und Position abspielt, indem Sie eine Aktion (Wiedergabe oder Aufzeichnung), eine Position und eine Uhrzeit für jeden VCR angeben.

Beide VCRs müssen dieselbe Uhr für diese Art der Bearbeitung verwenden. die Uhr hilft, beide Geräte zu synchronisieren. Sie können ermitteln, ob zwei VCRs dieselbe Uhr verwenden, indem Sie den Befehl [**status**](status.md) ([**MCI \_ STATUS**](mci-status.md)) mit dem Flag "clock id" verwenden, um die einzelnen VCR-Abfragen auszuführen. Wenn die vom Statusbefehl zurückgegebenen **Identifikationsnummern** identisch sind, verwenden die Geräte dieselbe Uhr. Als freigegebene Ressource kann die Uhr mit mehreren VCRs verbunden werden. Der VISCA-Treiber unterstützt nur eine freigegebene Uhr.

Sie können die Taktauflösung auch mithilfe des **Befehls** "Taktinkrementrate" bestimmen. Dieser Befehl gibt die Anzahl von Schritten zurück, die die Uhr pro Sekunde unterstützt. Wenn die Uhr beispielsweise alle Millisekunden aktualisiert wird, gibt der Befehl 1000 als Taktinkrementrate zurück. Der Vorteil der Verwendung der Inkrementrate besteht darin, dass die Rate als ganze Zahl ausgedrückt wird. Andernfalls ist das Inkrement ein Gleitkommawert (mit einfacher oder doppelter Genauigkeit). Als ganze Zahl ist die Bearbeitung der Inkrementrate ein einfacher Vorgang und nicht anfällig für Rundungsfehler. Sie können die Uhr mithilfe des Befehls [**set**](set.md) ([**MCI \_ SET**](mci-set.md)) mit dem Flag "clock 0" (null) zurücksetzen.

Wenn Sie einen [**Wiedergabebefehl**](play.md) ([**MCI \_ PLAY**](mci-play.md)), [**record**](record.md) ([**MCI \_ RECORD**](mci-record.md)) oder [**seek**](seek.md) [**(MCI \_ SEEK**](mci-seek.md)) ausgeben, können Sie angeben, wann der Befehl ausgeführt werden soll. Die Merkmale der verwendeten VCRs bestimmen, wann die einzelnen VCR gestartet werden sollen. Bei der zeitlichen Steuerung muss die Menge an Vorabrolls berücksichtigt werden, die für jedes Gerät erforderlich sind, sowie die Zeit, die zum Ausführen der MCI-Befehle zum Einrichten der Bearbeitungssitzung benötigt wird. Rufen Sie hierzu die Uhrzeit ab, und fügen Sie ein Warteintervall von 5 bis 10 Sekunden hinzu. (Das Warteintervall muss lang genug sein, damit die Vorrolling und alle ausstehenden MCI-Befehle die Ausführung beenden können.)

Um sicherzustellen, dass die Wartezeit lang genug ist, platzieren Sie den **Datensatzbefehl** zuletzt in Ihrer Anwendung, und überprüfen Sie die Zeit unmittelbar davor. Wenn das Intervall zu kurz ist, starten Sie den **Wiedergabebefehl** neu. Alternativ können Sie die Zeit unmittelbar nach dem letzten Befehl des Skripts überprüfen, um sicherzustellen, dass genügend Zeit zum Senden und Abschließen aller Befehle vorhanden ist.

 

 




