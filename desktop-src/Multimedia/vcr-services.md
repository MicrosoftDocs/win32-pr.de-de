---
title: VCR-Dienste
description: VCR-Dienste
ms.assetid: 140220f7-df7b-46e2-8374-e1200d873f3b
keywords:
- Video Systemsteuerungs-Architektur (VISCA)
- VISCA (Video System Control-Architektur)
- MCI-VISCA-Treiber
- VISCA-Treiber
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77d884c38d224182db7eef8db0f0cd80b14e3a08
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856551"
---
# <a name="vcr-services"></a>VCR-Dienste

Windows stellt VCR-Dienste über einen Gerätetreiber bereit, der auf dem MCI-Befehlssatz für VCRs basiert. In diesem Abschnitt wird der MCI-VISCA-Treiber (Video System Control Architecture) beschrieben und erläutert, wie er zum Steuern von VCR verwendet werden kann.

Der *VCR* -Gerätetyp steuert VCRs. Eine Liste der von VCR-Geräten erkannten MCI-Befehle finden Sie unter [VCR-Befehlssatz](vcr-command-set.md).

## <a name="the-mci-visca-driver"></a>Der MCI-VISCA-Treiber

Der MCI-VISCA-Treiber steuert die mit VISCA kompatiblen VCRs, wie z. b. CVD-1000 vkarten. Der VISCA-Treiber steuert den Band Transport, die channeltuners und die VCR-Eingabe-und-Ausgabekanäle.

## <a name="searching-and-positioning-with-a-vcr"></a>Suchen und positionieren mit einem VCR

Der VISCA-Treiber verwendet zwei Methoden zum Nachverfolgen der videobandbewegung innerhalb des VCR-Band Transports: *Zeit Code Informationen* und *Band Zähler*. Zeit Code Informationen sind Zeit Steuerungsinformationen, die auf dem Videotape aufgezeichnet wurden. Bei den meisten VCRs können Timecodes aufgezeichnet werden, ohne dass Audio-und Videospuren zerstört werden. Band Indikatoren schätzen die Menge an Videobändern, die hinter dem Video bandkopf bewegt werden, um eine Position zu erhalten.

Sowohl Zeit Code Informationen als auch Band Zähler erhöhen sich, wenn sich das Video Band von Anfang bis Ende verschiebt. Aufgrund ihrer Genauigkeit ist die Verwendung von Zeit Code Informationen zum Positionieren eines Videobands fast immer der Verwendung von Band Indikatoren vorzuziehen.

Die MCI-Befehlsflags zum Angeben von Positionsinformationen werden als Zeit Abhängigkeiten ausgedrückt: "Zeitformat", "Duration", "from", "to" und "Seek". (Außerdem gibt der [**Status**](status.md) Befehl "Position" den Zeitwert im aktuellen Zeitformat zurück.)

Der VISCA-Treiber verwendet den Befehl "Zeit Modus" [**festlegen**](set.md) , um die Art der Positionierung auszuwählen, die mit einem Videotape verwendet werden soll. Wenn der Zeit Modus auf "Zeitcode" festgelegt ist, **verwenden die Befehle "Position" und** " **set** " für "Zeitformat" den Zeit Code auf dem Videotape. Wenn der Zeit Modus auf "Counter" festgelegt ist, **verwenden die Befehle** "Position" und " **festgelegt** " Zeitformat "Indikatoren".

Eine Anwendung kann den Zeit Modus auf "erkennen" festlegen, wenn es keine Rolle spielt, dass es möglicherweise zwei Quellen mit Positionsinformationen gibt. Im Erkennungs Modus verwendet der VISCA-Treiber Zeit Code Informationen zur Positionierung, wenn eine der folgenden Bedingungen zutrifft:

-   Die Zeit Code Informationen sind beim Öffnen des Treibers vorhanden.
-   Sie ändern ein Videoband mit dem Befehl "Door **Open",** und auf dem Videoband sind Zeit Code Informationen vorhanden.
-   Der Befehl "Zeit Modus [**festlegen**](set.md) " wird neu ausgestellt.

Wenn keine Zeitcode-Informationen gefunden werden können, verwendet der Treiber die Band Zähler.

Um die aktuelle Positionierungs Methode zu ermitteln, geben Sie den [**Status**](status.md) des "Time Type"-Befehls ein, der entweder "Timecode" oder "Counter" zurückgibt. Sie können auch den aktuellen Positions Modus mithilfe des Befehls **Status** "Zeit Modus" identifizieren, der "Timecode", "Counter" oder "Detect" zurückgibt.

Der **Status** "Counter"-Befehl ruft unabhängig von der aktuellen Positions Methode den aktuellen bandzählerwert ab. Allerdings können Sie diesen gegen Schreibvorgang nur mit dem Befehl "Counter" [**festlegen**](set.md) .

Der VISCA-Treiber kann das systemeigene Zeit Code Format, das auf einem videtape aufgezeichnet wurde, **mithilfe der Befehle** "timecodetyp" und " **Status** " Frame Rate "" abrufen. Wenn z. b. der Zeitcode-Typ "SMPTE" und die Framerate den Wert 25 aufweisen, ist das auf dem Videoband aufgezeichnete Native Zeit Code Format SMPTE 25.

Der VISCA-Treiber kann die Auflösung des Zählers auch abrufen, indem er den **Status** "Counter Resolution" verwendet, der "seconds" oder "Frames" zurückgibt. Das Leistungsmodell kann weiterhin auf SMPTE 30 festgelegt werden, aber der Rückgabewert gibt nur einen Frame von 0 zurück. Wenn der aktuelle Zeittyp "Counter" ist, gilt diese Auflösung auch für den Wert, der durch den **Status** "Position" zurückgegeben wird.

## <a name="capturing-frames"></a>Aufzeichnen von Frames

Frame Erfassungs Befehle stellen weiterhin Bilder für ein *Frame Erfassungsgerät* bereit. Bei einem Frame Erfassungsgerät handelt es sich um eine separate Hardware, die das Video Bild lesen und speichern kann. Der VISCA-Treiber unterstützt den [**Freeze**](freeze.md) -Befehl ([**MCI \_ Freeze**](mci-freeze.md)), um ein Image für die Erfassung zu stabilisieren. Außerdem kann der [**Befehl zum Aufheben der Fixierung (**](unfreeze.md) [**MCI- \_ Sperrung**](mci-unfreeze.md)) verwendet werden, um den Band Transport nach einem **Freeze** -Befehl neu zu starten.

Der **Freeze** -Befehl bietet ein hochwertiges, stabilisiertes –-Image für ein Frame Erfassungsgerät. Dieser Befehl ist vorhanden, weil ein Gerät bei der Wiedergabe oder bei angehaltenen Ausführung möglicherweise nicht immer sein Maximum-Quality-Ausgabe Image bereitstellt. ein solches Video Bild eignet sich nicht für die Erfassung.

Der **Befehl zum Aufheben der Fixierung** entsperrt den Band Transport und setzt den Transportmodus fort, der vor dem **Freeze** -Befehl wirksam ist.

Wenn Ihre Anwendung ein Video Bild auf der VCR aufzeichnen muss, verwenden Sie den **Befehl "Input" fixieren** oder den [**Hinweis**](cue.md) ([**MCI \_**](mci-cue.md)-Hinweis), um das Image aufzuzeichnen.

## <a name="selecting-inputs"></a>Auswählen von Eingaben

Der VISCA-Treiber unterstützt drei Eingabetypen: Video, Audiodaten und Timecode. Zu den Videoeingaben gehören zwei Standardkanäle (Zeilen 1 und 2), ein SVideo-Kanal, ein hilfsanchannel und ein Kanal von einem internen Tuner. Die Audioeingaben umfassen zwei Standardkanäle (Zeilen 1 und 2) und einen Kanal von einem internen Tuner. Die Zeitcode-Eingabe ist für den VCR intern.

Die normalen Ausgaben enthalten die aktuell ausgewählten Eingaben, wenn die VCR-Aufzeichnung erfolgt oder der Band Transport angehalten wird, und Sie tragen den Inhalt des Videobands, wenn der Band Transport wiedergegeben oder angehalten wird. Die überwachten Ausgaben enthalten die gleichen Informationen wie die normalen Ausgaben sowie aktuelle Zeit Code-und Kanalinformationen.

Wenn Sie davon ausgehen, dass die entsprechenden externen Eingaben mit Ihrem VCR verbunden sind und Sie festgelegt haben, was Sie aufzeichnen möchten, können Sie die zu zeichnenden Eingaben auswählen. Wenn Sie z. b. das Video "SVideo" und die Audioeingaben "Zeile 1" aufzeichnen oder anzeigen möchten, verwenden Sie die Befehle [**setvideo**](setvideo.md) ([**MCI \_ setvideo**](mci-setvideo.md)) und [**SetAudio(**](setaudio.md) [**MCI \_ SetAudio)**](mci-setaudio.md), um diese Eingabe Quellen auszuwählen. Sie können diese Auswahl mithilfe des Befehls [**Status**](status.md) ([**MCI- \_ Status**](mci-status.md)) überprüfen.

Standardmäßig zeigt der Monitor genau an, was als Ausgabe angezeigt wird. Manchmal können Sie jedoch eine Quelle anzeigen, während Sie von einer anderen aufgezeichnet wird. Dies ist eine gängige Vorgehensweise bei der Verwendung des Tuners. Beispielsweise können Sie Channel 4 ansehen, während Sie Channel 7 aufzeichnen. In diesem Fall verfügen Sie über zwei logische Tuner-Eingaben. Sie können VCR mithilfe der folgenden Befehle einrichten:

## <a name="to-review-one-source-while-recording-from-another"></a>So überprüfen Sie eine Quelle beim Aufzeichnen von einer anderen Quelle

1.  Verwenden Sie den Befehl [**settuner**](settuner.md) ([**MCI \_ settuner**](mci-settuner.md)), um die zu überwachenden und aufzuzeichnen Kanäle auszuwählen.
2.  Verwenden Sie den Befehl **setvideo** , um die Video aufzeichnungsquelle auszuwählen.
3.  Verwenden Sie den Befehl [**SetAudio,**](setaudio.md) um die audioaufzeichnungs Quelle auszuwählen.
4.  Verwenden Sie den Befehl [**setvideo**](setvideo.md) , um die Videoeingabe für Channel 4 an die überwachte Ausgabe weiterzuleiten, um Sie auf dem Bildschirm anzuzeigen.
5.  Verwenden Sie den Befehl [**SetAudio,**](setaudio.md) um die Audioeingabe Channel 4 an die überwachte Ausgabe weiterzuleiten, um das Audiomaterial wiederzugeben.
6.  Überprüfen Sie Ihre Auswahl mit dem [**Status**](status.md) Befehl.

Der VISCA-Treiber unterstützt auch einen speziellen Eingabetyp für Audiodaten und Videos namens *stumm*. Stumm ermöglicht die Auswahl von "keine Eingabe", was beim Aufzeichnen eines leeren Signals hilfreich ist.

## <a name="selecting-recording-tracks"></a>Auswählen von Aufzeichnungs Spuren

Auf einem Videotape gibt es drei Typen von Aufzeichnungs Titeln: Video, Audiodaten und Timecode. Sie haben nur eine Video-oder Zeitcode-Spur, aber Sie können mehr als einen Audiotitel verwenden. Wenn Sie dies tun, machen Sie nachverfolgen 1 die Haupt Audiospur.

Der VISCA-Treiber unterstützt zwei Betriebsmodi: Assemblieren und einfügen. Im Assemblierungs *Modus* werden alle Spuren ausgewählt, damit Sie aufgezeichnet werden. Im *Einfügemodus* können Spuren unabhängig für die Aufzeichnung ausgewählt werden. Die meisten VCRs befinden sich standardmäßig im assemblierungsmodus. Verwenden Sie den [**Set**](set.md) ([**MCI \_ set**](mci-set.md))-Befehl, um diese Modi zu ändern.

## <a name="recording-and-editing"></a>Aufzeichnen und bearbeiten

Der [**Datensatz**](record.md) -Befehl ([**MCI- \_ Datensatz**](mci-record.md)) stellt eine einfache Aufzeichnung bereit und ist auf ungefähr eine Sekunde der Anfangsposition genau. Wenn Sie einen genaueren Datensatz ausführen möchten oder wenn Sie davon ausgehen, dass Sie den Videoinhalt bearbeiten möchten, während gleichzeitig mehrere Karten verwendet werden, sollten [**Sie den Hinweis**](cue.md) ([**MCI- \_ Hinweis)**](mci-cue.md)verwenden.

Der **Hinweis Befehl bereitet** das Gerät für die Aufzeichnung oder das Abspielen vor. Verwenden Sie **den Befehl "Input",** um das Gerät für die Aufzeichnung vorzubereiten. Der **Hinweis Befehl ist** erforderlich, da eine Anwendung wissen muss, wann das Gerät bereit ist, den Befehl auszuführen (und dass es einige Minuten dauern kann, bis ein [**Wiedergabe**](play.md) Befehl ([**MCI \_ Play**](mci-play.md)) oder ein **Datensatz** -Befehl vorbereitet wird.

Die VCR bereitet sich selbst für die Aufzeichnung oder Wiedergabe vor, indem Sie den *-Punkt* sucht, der die aktuelle Position oder die mit dem **Befehl "from** " angegebene Position ist. Wenn das Flag "ein Vorlauf ausgeführt" jedoch mit dem Befehl " **Cue** " angegeben wird, positioniert sich der VCR selbst mit der Vorabversion des vorpunkts. Das Flag "Preroll" gibt auch an, dass der VCR jeden anwendbaren Bearbeitungsmodus verwendet. Daher ist es wichtig, dass Sie "Preroll" verwenden, insbesondere, wenn Sie die genaueste Aufzeichnung wünschen. (Verwenden Sie den Befehl " [**Funktion**](capability.md) " ([**MCI \_ getdevcaps**](mci-getdevcaps.md)) mit dem Flag "kann vorab", um zu überprüfen, ob der vorab Modus unterstützt wird.)

> [!Note]  
> Wenn Sie mithilfe von "from"-und "to"-Positionen aufzeichnen, ist die Position "von" in der Bearbeitung enthalten, und die Position "an" ist nicht.

 

Weitere Informationen zum Aufzeichnen finden Sie unter [Aufzeichnung](recording.md).

## <a name="using-the-clock-while-editing"></a>Verwenden der Uhr beim Bearbeiten

Beim bearbeiten können Sie Segmente von einem VCR zu einem anderen aufzeichnen. Sie können mit der Aufzeichnung zu einem bestimmten Zeitpunkt und an einer bestimmten Position in einer VCR beginnen, während eine andere gleichzeitig mit der gleichen Zeit und Position beginnt, indem Sie eine Aktion (Wiedergabe oder Datensatz), eine Position und eine Uhrzeit für jede VCR-Datei angibt.

Beide VCRs müssen für diese Art der Bearbeitung dieselbe Uhr verwenden. die Uhr unterstützt Sie bei der Synchronisierung beider Geräte. Mithilfe des Befehls [**Status**](status.md) ([**MCI- \_ Status**](mci-status.md)) und dem Flag "Clock ID" können Sie ermitteln, ob zwei VCRs dieselbe Uhr verwenden, um die einzelnen VCR abzufragen. Wenn die vom **Status** Befehl zurückgegebenen Identifikationsnummern identisch sind, verwenden die Geräte dieselbe Uhr. Als freigegebene Ressource kann die Uhr mit mehreren VCRs verbunden werden. Der VISCA-Treiber unterstützt nur eine gemeinsame Uhr.

Sie können die Takt Auflösung auch mit dem Befehl **Status** "Uhr Inkrement Rate" ermitteln. Dieser Befehl gibt die Anzahl der Inkremente zurück, die die Uhr pro Sekunde unterstützt. Wenn die Uhr beispielsweise alle Millisekunden aktualisiert wird, gibt der Befehl 1000 als Takt Inkrement-Rate zurück. Der Vorteil der Verwendung der Inkrement-Rate besteht darin, dass die Rate als ganze Zahl ausgedrückt wird. Andernfalls wäre das Inkrement ein Gleit Komma Wert (mit einfacher oder doppelter Genauigkeit). Als ganze Zahl ist die Bearbeitung der Inkrement-Rate ein einfacher Vorgang und nicht anfällig für Rundungsfehler. Sie können die Uhr zurücksetzen, indem Sie den [**Set**](set.md) ([**MCI \_ set**](mci-set.md))-Befehl mit dem Flag "Clock 0" (null) verwenden.

Wenn Sie einen [**Wiedergabe**](play.md) Befehl ([**MCI \_ Play**](mci-play.md)), einen [**Datensatz**](record.md) (MCI-[**\_ Datensatz**](mci-record.md)) oder einen [**Seek**](seek.md) -Befehl ([**MCI \_ Seek**](mci-seek.md)) ausgeben, können Sie angeben, wann der Befehl ausgeführt werden soll. Die Merkmale des verwendeten VCRs bestimmen, wann die einzelnen VCR gestartet werden sollen. Die zeitliche Steuerung muss die Menge der vorab Befehle berücksichtigen, die für jedes Gerät erforderlich sind, sowie die Zeitspanne, die benötigt wird, um die MCI-Befehle abzuschließen, die zum Einrichten der Bearbeitungs Sitzung verwendet werden. Rufen Sie hierzu die Uhrzeit ab, und fügen Sie ein Wartezeit von 5 bis 10 Sekunden hinzu. (Das warte Intervall muss lang genug sein, damit das vorab-und alle ausstehenden MCI-Befehle ausgeführt werden können.)

Um sicherzustellen, dass die Wartezeit lange genug ist, platzieren Sie den Befehl " **Record** " zuletzt in der Anwendung, und überprüfen Sie die Zeit unmittelbar vor der Zeit. Wenn das Intervall zu kurz ist, starten Sie den **Wiedergabe** Befehl neu. Sie können auch die Uhrzeit direkt nach dem letzten Befehl des Skripts überprüfen, um sicherzustellen, dass genügend Zeit zum Senden und Ausführen aller Befehle vorhanden ist.

 

 




