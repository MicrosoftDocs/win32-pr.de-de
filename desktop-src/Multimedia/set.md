---
title: Befehl "set"
description: Mit dem Befehl set werden Steuerungseinstellungen für das Gerät festgelegt. CD-Audio, digital-video, RADAR sequencer, VCR, videodisc, video-overlay und waveform-audio erkennen diesen Befehl.
ms.assetid: 1ec4d84e-372a-4b6d-b694-f5afb41f90b2
keywords:
- Set-Befehl Windows Multimedia
topic_type:
- apiref
api_name:
- set
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1fc9263ace043f938c8d793b2ceef5ad70264bb1
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479486"
---
# <a name="set-command"></a>Befehl "set"

> [!NOTE]
> Bias-free Communication Microsoft unterstützt eine vielfältige und inklusionsbasierte Umgebung.  In diesem Dokument gibt es Verweise auf das Wort "slave". Microsoft Style [Guide for Bias-Free Communications](https://github.com/MicrosoftDocs/microsoft-style-guide/blob/master/styleguide/bias-free-communication.md) erkennt dies als Ausschlusswort.  Diese Formulierung wird verwendet, da sie derzeit in den Befehlen verwendet wird. Zur Konsistenz enthält dieses Dokument dieses Wort. Wenn dieses Wort in den Befehlen geändert wird, korrigieren wir dieses Dokument so, dass es ausgerichtet ist.


Mit dem Befehl set werden Steuerungseinstellungen für das Gerät festgelegt. CD-Audio, digital-video, RADAR sequencer, VCR, videodisc, video-overlay und waveform-audio erkennen diesen Befehl.

Um diesen Befehl zu senden, rufen Sie die [**mciSendString-Funktion**](/previous-versions//dd757161(v=vs.85)) mit dem *lpszCommand-Parameter* auf, der wie folgt festgelegt ist.

``` syntax
_stprintf_s(
  lpszCommand,
  TEXT("set %s %s %s"),
  lpszDeviceID,
  lpszSetting,
  lpszFlags
);
      
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Bezeichner eines MCI-Geräts. Dieser Bezeichner oder Alias wird zugewiesen, wenn das Gerät geöffnet wird.

</dd> <dt>

<span id="lpszSetting"></span><span id="lpszsetting"></span><span id="LPSZSETTING"></span>*lpszSetting*
</dt> <dd>

Flag zum Einrichten von Steuerelementeinstellungen. In der folgenden Tabelle sind die Gerätetypen aufgeführt, die den **Set-Befehl** und die von den einzelnen Typen verwendeten Flags erkennen.




| Gerätetyp | Befehlsflags | 
|-------------|---------------|
| cdaudio | <ul><li>Audio all off</li><li>Audio all on</li><li>Audio links</li><li>audio left on</li><li>Audio von Rechts nach rechts</li><li>Audio direkt ein</li><li>Tür geschlossen</li><li>Tür geöffnet</li><li>Zeitformat millisekunden</li><li>Zeitformat msf</li><li>Zeitformat tmsf</li></ul> | 
| digitalvideo | <ul><li>Audio all off</li><li>Audio all on</li><li>Audio links</li><li>audio left on</li><li>Audio von Rechts nach rechts</li><li>Audio direkt ein</li><li>Tür geschlossen</li><li>Tür geöffnet</li><li>Dateiformatformat <em></em></li><li>Suchen nach genau am</li><li>Genau aussuchen</li><li><em>Geschwindigkeitsfaktor</em></li><li>Format des Dateiformats <em>"still"</em></li><li>Zeitformatrahmen</li><li>Zeitformat millisekunden</li><li>Video off</li><li>Video zu</li></ul> | 
| overlay | <ul><li>Audio all off</li><li>Audio all on</li><li>Audio links</li><li>audio left on</li><li>Audio von Rechts nach rechts</li><li>Audio direkt ein</li><li>Tür geschlossen</li><li>Tür geöffnet</li><li>Video off</li><li>Video zu</li></ul> | 
| sequencer | <ul><li>Audio all off</li><li>Audio all on</li><li>Audio links</li><li>audio left on</li><li>Audio von Rechts nach rechts</li><li>Audio direkt ein</li><li>Tür geschlossen</li><li>Tür geöffnet</li><li>master MASTERS</li><li>master none</li><li>master SMPTE</li><li><em>Offsetzeit</em></li><li>Portzuordnung</li><li>port none</li><li>Port <em>port_number</em></li><li>Slave-Datei</li><li>Slave SLAVE SLAVE</li><li>Slave none</li><li>Slave SMPTE</li><li>Tempo <em>tempo_value</em></li><li>Zeitformat millisekunden</li><li>Zeitformat SMPTE <em>fps</em></li><li>Zeitformat SMPTE 30 drop</li><li>Musikzeiger im Zeitformat</li></ul> | 
| <strong>Vcr</strong> | <ul><li>Datensatz zusammenstellen auf</li><li>Datensatz ausstellen</li><li>Audio all off</li><li>Audio all on</li><li>Audio links</li><li>audio left on</li><li>Audio von Rechts nach rechts</li><li>Audio direkt ein</li><li>Uhrzeit <em></em></li><li>Indikatorformat</li><li><em>Indikatorwert</em></li><li>Tür geschlossen</li><li>Door Open</li><li>Indexzähler</li><li>Indexdatum</li><li>Indexzeit</li><li>Indexzeit</li><li>codelength <em>duration</em></li><li><em>Timeout</em> anhalten</li><li>Dauer der Postrolls:</li><li><em>duration</em></li><li>Einschalten</li><li>Ausschalten</li><li><em>Dauer</em> der Vorabrollingdauer</li><li>Datensatzformat SP</li><li>Datensatzformat LP</li><li>Datensatzformat EP</li><li><em>Geschwindigkeitsfaktor</em></li><li>Zeitformatrahmen</li><li>Zeitformat hms</li><li>Zeitformat (Millisekunden)</li><li>zeitformat msf</li><li>Zeitformat SMPTE <em>fps</em></li><li>Zeitformat SMPTE 30 drop</li><li>zeitformat tmsf</li><li>Zeitmoduszähler</li><li>Zeitmoduserkennung</li><li>Time mode timecode (Zeitcode im Zeitmodus)</li><li>Nachverfolgung plus</li><li>Nachverfolgungs-Minus</li><li>Nachverfolgungsrücksetzung</li></ul> | 
| videodisc | <ul><li>Audio all off</li><li>audio all on</li><li>Audio ausgelassen</li><li>audio left on</li><li>Audio direkt ausgeschaltet</li><li>Audio direkt eingeschaltet</li><li>Tür geschlossen</li><li>Door Open</li><li>Zeitformatrahmen</li><li>Zeitformat hms</li><li>Zeitformat (Millisekunden)</li><li>Zeitformatspur</li><li>Video aus</li><li>Video zu</li></ul> | 
| Waveaudio | <ul><li><em>Ganzzahlige</em> Ausrichtung</li><li>Beliebige Eingabe</li><li>beliebige Ausgabe</li><li>Audio all off</li><li>audio all on</li><li>Audio ausgelassen</li><li>audio left on</li><li>Audio direkt ausgeschaltet</li><li>Audio direkt eingeschaltet</li><li>bitspersample <em>bit_count</em></li><li>bytespersec <em>byte_rate</em></li><li>kanäle <em>channel_count</em></li><li>Tür geschlossen</li><li>Door Open</li><li>format tag pcm</li><li>Tagtag <em>formatieren</em></li><li><em>Eingabe-Ganzzahl</em></li><li><em>Ausgabe ganze Zahl</em></li><li>samplespersec <em>integer</em></li><li>Zeitformat byte</li><li>Zeitformat (Millisekunden)</li><li>Zeitformatbeispiele</li></ul> | 




 

Die folgende Tabelle enthält die Flags, die im **lpszSetting-Parameter** angegeben werden können, und ihre Bedeutungen.




| Wert | Bedeutung | 
|-------|---------|
| <em>Ganzzahlige</em> Ausrichtung | Legt die Ausrichtung von Datenblöcken relativ zum Anfang der Daten fest, die an das Waveform-Audio-Gerät übergeben werden. Die Datei wird in diesem Format gespeichert. | 
| Beliebige Eingabe | Verwenden Sie bei der Aufzeichnung eine beliebige Eingabe, die das aktuelle Format unterstützt. Dies ist die Standardeinstellung. | 
| beliebige Ausgabe | Verwenden Sie bei der Wiedergabe eine beliebige Ausgabe, die das aktuelle Format unterstützt. Dies ist die Standardoption. | 
| Datensatz zusammenstellen auf <br /> Datensatz ausstellen <br /> | Im Assemblermodus werden alle Spuren gemäß der Definition des Geräts aufgezeichnet. Die meisten VCRs befinden sich standardmäßig im Assemblermodus. | 
| Audio all off <br /> audio all on <br /> | Deaktiviert oder aktiviert die Audioausgabe. Videoüberlagerungsgeräte, der MCISEQ-Sequencer und das MCIWAVE Waveform-Audio-Gerät unterstützen dieses Flag nicht. | 
| Audio ausgelassen <br /> audio left on <br /> Audio direkt ausgeschaltet <br /> Audio direkt eingeschaltet <br /> | Deaktiviert oder aktiviert die Ausgabe an den linken oder rechten Audiokanal. Videoüberlagerungsgeräte, der MCISEQ-Sequencer und das MCIWAVE Waveform-Audio-Gerät unterstützen dieses Flag nicht. | 
| bitspersample <em>bit_count</em> | Legt die Anzahl der Bits pro pcm -Beispiel (Pulse Code Pulse) fest, das wiedergegeben oder aufgezeichnet wird. Die Datei wird in diesem Format gespeichert. | 
| bytespersec <em>byte_rate</em> | Legt die durchschnittliche Anzahl der wiedergegebenen oder aufgezeichneten Bytes pro Sekunde fest. Die Datei wird in diesem Format gespeichert. | 
| Kanäle <em>channel_count</em> | Legt die Kanäle für die Wiedergabe und Aufzeichnung fest. Die Datei wird in diesem Format gespeichert. | 
| Uhrzeit <em></em> | Legt die Zeit für die externe Uhr auf die Uhrzeit <em>fest.</em> Das Format wird als lange ganze Zahl ohne Vorzeichen angegeben. | 
| Indikatorformat | Legen Sie das Zeitformat für den Zähler so fest, wie es vom <a href="status.md">Status "Counter"</a> zurückgegeben wird. Informationen zu anwendbaren Typen finden Sie im Befehl <strong>"Zeitformat</strong> festlegen". | 
| <em>Zählerwert</em> | Legt den VCR-Indikator auf den angegebenen Wert fest. Der Wert muss im aktuellen Indikatorformat angegeben werden. Weitere Informationen finden Sie im <strong>Befehl</strong> set "counter format". | 
| Tür geschlossen | Entfernt die Taskleiste und schließt nach Möglichkeit die Tür. Bei VCRs lädt das Band automatisch. | 
| Tür geöffnet | Öffnet die Tür und wirft nach Möglichkeit die Leiste oder das Band aus. | 
| Dateiformatformat <em></em> | Gibt ein Dateiformat an, das für Speicher- <a href="save.md">oder</a> <a href="capture.md">Erfassungsbefehle verwendet</a> wird. Wenn dies nicht angegeben wird, wird möglicherweise standardmäßig ein vom Gerätetreiber definiertes Format verwendet. Wenn das angegebene Dateiformat mit dem aktuell ausgewählten Algorithmus und der Qualität in Konflikt steht, werden sie in die Standardwerte für das Dateiformat geändert. Die folgenden Dateiformate sind definiert:<ul><li>avi: Gibt das AVI-Format an.</li><li>avss: Gibt das AVSS-Format an.</li><li>dib: Gibt das DIB-Format an.</li><li>jfif: Gibt das JFIF-Format an.</li><li>jpeg: Gibt das JPEG-Format an.</li><li>mpeg: Gibt das MPEG-Format an.</li><li>rdib: Gibt das RLE-DIB-Format an.</li><li>rjpeg: Gibt das RJPEG-Format an.</li></ul> | 
| Formattag pcm | Legt den Formattyp für die Wiedergabe und Aufzeichnung auf PCM fest. Die Datei wird in diesem Format gespeichert. | 
| Tagtag <em>formatieren</em> | Legt den Formattyp für die Wiedergabe und Aufzeichnung fest. Die Datei wird in diesem Format gespeichert. | 
| Indexzeitcode <br /> Indexzähler <br /> Indexdatum <br /> Indexzeit <br /> | Legt den aktuellen Anzeigebildschirm auf dem VCR fest. | 
| <em>Eingabe-Ganzzahl</em> | Legt den Audiokanal fest, der als Eingabe verwendet wird. | 
| <em>Längendauer</em> | Legt die vom Benutzer angegebene Länge des Bandes im VCR fest. Diese Länge wird durch den <a href="status.md">Statusbefehl</a> "length" zurückgegeben und aus Kompatibilitäts- und Kompatibilitätsgelangen mit Anwendungen bereitgestellt, für die dieser Befehl eine gültige Länge zurückgeben muss. | 
| master- | Legt denSKRIPT-Sequencer als Synchronisierungsquelle fest. Synchronisierungsdaten werden im FORMAT DEST-Formats gesendet. Der MCISEQ-Sequencer unterstützt dieses Flag nicht. | 
| master none | Verhindert, dass derENDE-Sequencer Synchronisierungsdaten sendet. Der MCISEQ-Sequencer unterstützt dieses Flag nicht. | 
| master smpte | Legt denSKRIPT-Sequencer als Synchronisierungsquelle fest. Synchronisierungsdaten werden im SMPTE-Format (Society of Motion Picture and Tv Engineers) gesendet. Der MCISEQ-Sequencer unterstützt dieses Flag nicht. | 
| <em>Offsetzeit</em> | Legt die SMPTE-Offsetzeit <em>fest.</em> Der Offset ist die Anfangszeit einer SMPTE-basierten Sequenz. Die <em>Zeit</em> wird als <em>hh</em>ausgedrückt: <em>mm</em>: <em>ss</em>: <em>ff</em>, wobei <em>hh</em> stunden, <em>mm minuten,</em> <em>ss</em> sekunden und <em>ff</em> Frames sind. | 
| Ganzzahlige <em>Ausgabe</em> | Legt den Audiokanal fest, der als Ausgabe verwendet wird. | 
| <em>Pausen-Timeout</em> | Legt die maximale Dauer eines Pausenbefehls in <a href="pause.md">Millisekunden</a> fest. Der <em>Timeoutwert</em> 0 (null) gibt an, dass kein Timeout auftritt. | 
| Dauer des <em>Postrolls</em> | Legt die Länge im aktuellen Zeitformat fest, die erforderlich ist, um den VCR-Transport zu unterbrechen, wenn ein Befehl <a href="stop.md">zum</a> Beenden oder Anhalten ausgegeben wird. <strong></strong> | 
| Portzuordnung | Legt die MAPPer-Funktion für die DANN-Zuordnung als Port fest, der die DANN-Nachrichten empfängt. Dieser Befehl schlägt fehl, wenn die MAPPer-Datei oder ein port, den sie benötigt, von einer anderen Anwendung verwendet wird. | 
| port none | Deaktiviert das Senden vonBENACHRICHTIGUNG-Nachrichten. Mit diesem Befehl wird auch ein DANN-Port geschlossen. | 
| Port <em>port_number</em> | Legt den DANN-Port fest, der die FEHLERMELDUNG-Nachrichten empfängt. Dieser Befehl schlägt fehl, wenn der Port, den Sie öffnen möchten, von einer anderen Anwendung verwendet wird. | 
| Einschalten <br /> Ausschalten <br /> | Legt die Ein- oder Ausschalten des Geräts fest. | 
| Dauer der <em>Vorabrolldauer</em> | Legt die Länge im aktuellen Zeitformat fest, die zum Stabilieren der VCR-Ausgabe erforderlich ist. | 
| Datensatzformat SP <br /> Datensatzformat LP <br /> Datensatzformat EP <br /> | Legt den Aufzeichnungsmodus für den VCR auf SP für standard play, EP für erweiterte Wiedergabe oder LP für lange Wiedergabe fest. Diese Werte sind nicht als VHS-spezifisch gedacht. Sie sind drei geeigneten Modi mit anderen Bandformaten zuordnen. Sp wird z. B. der schnellsten Aufzeichnung mit der höchsten Qualität angezeigt. | 
| samplespersec <em>integer</em> | Legt die Abtastrate für Wiedergabe und Aufzeichnung fest. Die Datei wird in diesem Format gespeichert. | 
| Suchen nach genau am<br /> Genau aussuchen <br /> | Wählt einen von zwei Suchmodi aus. Bei "Genau suchen nach" wird seek immer zum angegebenen Frame bewegt. Bei "Genau suchen aus" wird seek zum nächstgelegenen Keyframe vor dem angegebenen Frame bewegt. | 
| Slave-Datei | Legt fest, dass der SEQUENCEr Dateidaten als Synchronisierungsquelle verwendet. Dies ist die Standardeinstellung. | 
| slave slave slave | Legt den SEQUENCEr für die Verwendung eingehenderSKRIPT-Daten für die Synchronisierungsquelle fest. Der Sequencer erkennt Synchronisierungsdaten im FORMAT DEST-Formats. Der MCISEQ-Sequencer unterstützt dieses Flag nicht. | 
| Slave none | Legt fest, dass der SEQUENCEr die Synchronisierung ignoriert. | 
| Slave-Smpte | Legt den SEQUENCEr für die Verwendung eingehenderSKRIPT-Daten für die Synchronisierungsquelle fest. Der Sequencer erkennt Synchronisierungsdaten im SMPTE-Format. Der MCISEQ-Sequencer unterstützt dieses Flag nicht. | 
| Geschwindigkeitsfaktor | Legt die relative Geschwindigkeit der Video- und Audiowiedergabe aus dem Arbeitsbereich fest. Faktor ist das Verhältnis zwischen der nominalen Bildfrequenz und der gewünschten Bildfrequenz, wobei die nominale Framerate als 1000 festgelegt ist. (Eine Rate von 500 ist halb normale Geschwindigkeit, 2000 ist doppelt normale Geschwindigkeit und so weiter.) Wenn Die Geschwindigkeit auf 0 (null) gesetzt wird, wird das Video so schnell wie möglich abspielt, ohne Frames und ohne Audio zu löschen. | 
| Format des Dateiformats <em>"still"</em> | Gibt das Dateiformat an, das für Erfassungsbefehle verwendet wird. | 
| Tempo tempo_value | Legt das Tempo der Sequenz gemäß dem aktuellen Zeitformat fest. Für eine PPQN-basierte Datei wird die tempo_value als Takte pro Minute interpretiert. Bei einer SMPTE-basierten Datei wird die tempo_value als Frames pro Sekunde interpretiert. | 
| Bytes im Zeitformat | In einem PCM-Dateiformat legt das Zeitformat auf Bytes fest. Alle Positionsinformationen werden nach diesem Befehl als Bytes angegeben. | 
| Zeitformatrahmen | Legt das Zeitformat auf Frames fest. Alle Befehle, die Positionswerte verwenden, setzen Frames voraus. Wenn das Gerät geöffnet wird, ist Frames der Standardmodus. Wird von Videodiscs im CAV-Format unterstützt. | 
| Zeitformat hms | Legt das Zeitformat auf Stunden, Minuten und Sekunden fest. Alle Befehle, die Positionswerte verwenden, setzen HMS voraus. HMS ist das Standardformat für CLV-Videodiscs. Geben Sie einen HMS-Wert als hh:mm:ss an, wobei hh stunden, mm minuten und ss Sekunden ist. Sie können ein Feld weglassen, wenn es und alle folgenden Felder 0 (null) sind. Beispielsweise sind 3, 3:0 und 3:0:0 alle gültige Möglichkeiten, drei Stunden auszudrücken. <br /> | 
| Zeitformat millisekunden | Legt das Zeitformat auf Millisekunden fest. Alle Befehle, die Positionswerte verwenden, nehmen Millisekunden an. Sie können Millisekunden als "ms" abkürzen. Für Sequencergeräte legt die Sequenzdatei das Standardformat auf PPQN oder SMPTE fest. Videoüberlagerungsgeräte unterstützen dieses Flag nicht.<br /> | 
| Zeitformat msf | Legt das Zeitformat auf Minuten, Sekunden und Frames fest. Alle Befehle, die Positionswerte verwenden, setzen MSF voraus (das Standardformat für CD-Audio). Geben Sie einen MSF-Wert als mm:ss:ff an, wobei mm Minuten, ss Sekunden und ff Frames ist. Sie können ein Feld weglassen, wenn es und alle folgenden Felder 0 (null) sind. Beispielsweise sind 3, 3:0 und 3:0:0 gültige Möglichkeiten, 3 Minuten auszudrücken.<br /> Die MSF-Felder haben die folgenden maximalen Werte:<br /><ul><li>Minuten 99</li><li>Sekunden 59</li><li>Frames 74</li></ul> | 
| Zeitformatbeispiele | Legt das Zeitformat auf Beispiele fest. Alle Positionsinformationen werden als Beispiele nach diesem Befehl angegeben. | 
| Zeitformat smpte 24<br /> Zeitformat smpte 25<br /> Zeitformat smpte 30<br /> | Legt das Zeitformat auf eine SMPTE-Framerate fest. Legt für VCRs das Zeitformat auf hh:mm:ss:ff fest, wobei die rechtlichen Werte 00:00:00:00 bis 23:59:59:xx sind und xx eins kleiner als die Frames pro Sekunde ist, wie durch die Zahl 24, 25 oder 30 angegeben, wie im Flag angegeben. Bei der Eingabe werden Doppelpunkte (:) sind erforderlich, um die Komponenten zu trennen. Die am wenigsten signifikanten Einheiten können weggelassen werden, wenn sie 00 sind. Beispielsweise ist 02:00 identisch mit 02:00:00:00. Alle Befehle, die Positionswerte verwenden, nehmen das SMPTE-Format an.<br /> Die Sequenzdatei legt das Standardformat auf PPQN oder SMPTE fest.<br /> | 
| Zeitformat smpte 30 drop | Legt das Zeitformat auf SMPTE 30 Drop Frame Rate fest. Bei VCRs ist dies mit SMPTE 30 identisch, mit der Ausnahme, dass bestimmte Zeitcodepositionen aus dem Format gelöscht werden, damit die aufgezeichneten Zeitcodepositionen für jeden Frame (bei der NTSC-Framerate von 29,97 FPS) der Echtzeit (bei 30 Fps) entsprechen. Timecodepositionen, die verworfen werden, lauten wie folgt: zwei pro Minute für die ersten neun von zehn Minuten aufgezeichneten Inhalten. Um 01:04:59:29 wäre die nächste Timecodeposition beispielsweise 01:05:00:02 und nicht 01:05:00:00. Alle Befehle, die Positionswerte verwenden, nehmen das SMPTE-Format an.<br /> Die Sequenzdatei legt das Standardformat auf PPQN oder SMPTE fest.<br /> | 
| Musikzeiger im Zeitformat | Legt das Zeitformat auf einen Songzeiger fest (16 Notizen). Alle Befehle, die Positionswerte verwenden, setzen Songzeigereinheiten voraus. Dieses Flag ist nur für eine Sequenz vom Divisionstyp PPQN gültig. | 
| Zeitformat tmsf | Legt das Zeitformat auf Spuren, Minuten, Sekunden und Frames fest. Alle Befehle, die Positionswerte verwenden, setzen TMSF voraus. Geben Sie einen TMSF-Wert als tt:mm:ss:ff an, wobei tt für tracks, mm für minutes, ss für seconds und ff für frames steht. Sie können ein Feld weglassen, wenn es und alle folgenden Felder 0 (null) sind. Beispielsweise sind 3, 3:0, 3:0:0 und 3:0:0:0 alle gültige Möglichkeiten zum Ausdrücken von Track 3. <br /> Die TMSF-Felder haben die folgenden maximalen Werte:<br /><ul><li>Tracks 99</li><li>Minuten 90</li><li>Sekunden 59</li><li>Frames 74</li></ul> | 
| Zeitformatspur | Legt das Positionsformat auf Tracks fest. Alle Befehle, die Positionswerte verwenden, nehmen Spuren an. | 
| Zeitmoduszähler | Legt den Positionsinformationsmodus für die Verwendung der VCR-Leistungsindikatoren fest. | 
| Erkennung im Zeitmodus | Legt den Positionsinformationsmodus basierend auf der Erkennung von Zeitcodeinformationen auf dem Band fest. Wenn Zeitcodeinformationen erkannt werden, wird der Zeittyp auf "timecode" festgelegt. Andernfalls wird der Zeittyp auf "counter" festgelegt. "Detect" ist ein spezieller Modus. Wenn der Treiber geöffnet wird, ein neues Band eingefügt oder der Befehl "Zeitmodus" ausgegeben wird, überprüft der Treiber den auf dem Band verfügbaren aktuellen Zeitmodus und legt den "Zeittyp" entweder auf "Timecode" oder "Counter" fest. Sobald der "Zeittyp" festgelegt ist, ändert der Treiber ihn erst, wenn eine der oben genannten Bedingungen erneut auftritt.<br /> | 
| Zeitmodus-Zeitcode | Legt den Positionsinformationsmodus fest, um "Timecode"-Informationen auf dem Band zu verwenden. | 
| Nachverfolgung plus <br /> Nachverfolgung minus <br /> Nachverfolgen der Zurücksetzung <br /> | Passt die Geschwindigkeit des Videobandtransports in feinen Schritten an. Verwenden Sie die Nachverfolgungsflags, wenn ein lautes Bild von einem VCR erhalten wird. "Tracking plus" erhöht die Transportgeschwindigkeit. "Tracking minus" verringert die Transportgeschwindigkeit. "Nachverfolgungszurücksetzung" gibt die Nachverfolgungsanpassung auf 0 (null) zurück. | 
| Video off | Deaktiviert die Videoausgabe. | 
| Video zu | Aktiviert die Videoausgabe. | 




 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Kann "wait", "notify" oder beides sein. Für digital-video- und VCR-Geräte kann auch "test" angegeben werden. Weitere Informationen zu diesen Flags finden Sie unter [Die Warte-, Benachrichtigungs- und Testflags](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn erfolgreich, andernfalls ein Fehler.

## <a name="remarks"></a>Hinweise

Mehrere Eigenschaften von Waveform-Audiodaten werden definiert, wenn die Datei zum Speichern der Daten erstellt wird. Diese Eigenschaften beschreiben, wie die Daten innerhalb der Datei strukturiert sind und nicht mehr geändert werden können, sobald die Aufzeichnung beginnt. In der folgenden Liste sind diese Eigenschaften aufgeführt:

-   Ausrichtung
-   bitspersample
-   bytespersec
-   channels
-   Formattag
-   samplespersec

## <a name="examples"></a>Beispiele

Der folgende Befehl legt das Zeitformat auf Millisekunden und das Waveform-Audioformat auf 8 Bit, Mono und 11 kHz fest.

``` syntax
set mysound time format ms bitspersample 8 channels 1 samplespersec 11025
```

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>       |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[MCI-Befehlszeichenfolgen](mci-command-strings.md)
</dt> <dt>

[Erfassen](capture.md)
</dt> <dt>

[pause](pause.md)
</dt> <dt>

[Speichern](save.md)
</dt> <dt>

[stop](stop.md)
</dt> </dl>

 

