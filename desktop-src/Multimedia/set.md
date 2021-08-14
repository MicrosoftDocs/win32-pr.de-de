---
title: set-Befehl
description: Mit dem Befehl set werden Steuerungseinstellungen für das Gerät eingerichtet. CD-Audio-, Digital-Video-, WAVE Sequencer-, VCR-, Videodisc-, Videoüberlagerungs- und Waveform-Audiogeräte erkennen diesen Befehl.
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
ms.openlocfilehash: 75f407a1e360cfbd6407f7ada29192addece7f7a968a2437326dc091fe0d9522
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118371012"
---
# <a name="set-command"></a>set-Befehl

> [!NOTE]
> Voreingenommene Kommunikation Microsoft unterstützt eine vielfältige und inklusionsorientierte Umgebung.  In diesem Dokument gibt es Verweise auf das Wort "slave". Der [Microsoft Style Guide for Bias-Free Communications](https://github.com/MicrosoftDocs/microsoft-style-guide/blob/master/styleguide/bias-free-communication.md) erkennt dies als Ausschlusswort.  Diese Formulierung wird verwendet, da es sich derzeit um die Formulierung handelt, die in den Befehlen verwendet wird. Aus Konsistenzgründen enthält dieses Dokument dieses Wort. Wenn dieses Wort in den Befehlen geändert wird, korrigieren wir dieses Dokument in Übereinstimmung.


Mit dem Befehl set werden Steuerungseinstellungen für das Gerät eingerichtet. CD-Audio-, Digital-Video-, WAVE Sequencer-, VCR-, Videodisc-, Videoüberlagerungs- und Waveform-Audiogeräte erkennen diesen Befehl.

Um diesen Befehl zu senden, rufen Sie die [**mciSendString-Funktion**](/previous-versions//dd757161(v=vs.85)) auf, wobei der *lpszCommand-Parameter* wie folgt festgelegt ist.

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

Flag zum Einrichten von Steuerelementeinstellungen. In der folgenden Tabelle sind Gerätetypen aufgeführt, die den **set-Befehl** und die von den einzelnen Typen verwendeten Flags erkennen.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Gerätetyp</th>
<th>Befehlsflags</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>cdaudio</td>
<td><ul>
<li>Audio all off</li>
<li>audio all on</li>
<li>Audio ausgelassen</li>
<li>audio left on</li>
<li>Audio direkt ausgeschaltet</li>
<li>Audio direkt eingeschaltet</li>
<li>Tür geschlossen</li>
<li>Door Open</li>
<li>Zeitformat (Millisekunden)</li>
<li>zeitformat msf</li>
<li>zeitformat tmsf</li>
</ul></td>
</tr>
<tr class="even">
<td>digitalvideo</td>
<td><ul>
<li>Audio all off</li>
<li>audio all on</li>
<li>Audio ausgelassen</li>
<li>audio left on</li>
<li>Audio direkt ausgeschaltet</li>
<li>Audio direkt eingeschaltet</li>
<li>Tür geschlossen</li>
<li>Door Open</li>
<li><em>Dateiformat</em></li>
<li>Suchen sie genau nach</li>
<li>Suchen sie genau aus</li>
<li><em>Geschwindigkeitsfaktor</em></li>
<li><em>Format</em> des Dateiformats "still"</li>
<li>Zeitformatrahmen</li>
<li>Zeitformat (Millisekunden)</li>
<li>Video aus</li>
<li>Video zu</li>
</ul></td>
</tr>
<tr class="odd">
<td>overlay</td>
<td><ul>
<li>Audio all off</li>
<li>audio all on</li>
<li>Audio ausgelassen</li>
<li>audio left on</li>
<li>Audio direkt ausgeschaltet</li>
<li>Audio direkt eingeschaltet</li>
<li>Tür geschlossen</li>
<li>Door Open</li>
<li>Video aus</li>
<li>Video zu</li>
</ul></td>
</tr>
<tr class="even">
<td>sequencer</td>
<td><ul>
<li>Audio all off</li>
<li>audio all on</li>
<li>Audio ausgelassen</li>
<li>audio left on</li>
<li>Audio direkt ausgeschaltet</li>
<li>Audio direkt eingeschaltet</li>
<li>Tür geschlossen</li>
<li>Door Open</li>
<li>master MASTERS</li>
<li>master none</li>
<li>Master-SMPTE</li>
<li><em>Offsetzeit</em></li>
<li>Portzuordnung</li>
<li>Port "None"</li>
<li>Port <em>port_number</em></li>
<li>Untergeordnete Datei</li>
<li>Slave-NSDR</li>
<li>Slave None</li>
<li>Slave-SMPTE</li>
<li>tempo <em>tempo_value</em></li>
<li>Zeitformat (Millisekunden)</li>
<li>Zeitformat SMPTE <em>fps</em></li>
<li>Zeitformat SMPTE 30 drop</li>
<li>Zeitformattitelzeiger</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Vcr</strong></td>
<td><ul>
<li>Datensatz zusammenstellen auf</li>
<li>Datensatz ausstellen</li>
<li>Audio all off</li>
<li>audio all on</li>
<li>Audio ausgelassen</li>
<li>audio left on</li>
<li>Audio direkt ausgeschaltet</li>
<li>Audio direkt eingeschaltet</li>
<li><em>Uhrzeit</em></li>
<li>Indikatorformat</li>
<li><em>Zählerwert</em></li>
<li>Tür geschlossen</li>
<li>Tür geöffnet</li>
<li>Indexzähler</li>
<li>Indexdatum</li>
<li>Indexzeit</li>
<li>Indexzeit</li>
<li>codelength <em>duration</em></li>
<li><em>Pausen-Timeout</em></li>
<li>Postrolldauer:</li>
<li><em>duration</em></li>
<li>Einschalten</li>
<li>Ausschalten</li>
<li>Dauer der <em>Vorabrolldauer</em></li>
<li>Datensatzformat SP</li>
<li>Datensatzformat LP</li>
<li>Datensatzformat EP</li>
<li><em>Geschwindigkeitsfaktor</em></li>
<li>Zeitformatrahmen</li>
<li>Zeitformat hms</li>
<li>Zeitformat millisekunden</li>
<li>Zeitformat msf</li>
<li>Zeitformat SMPTE <em>fps</em></li>
<li>Zeitformat SMPTE 30 drop</li>
<li>Zeitformat tmsf</li>
<li>Zeitmoduszähler</li>
<li>Erkennung im Zeitmodus</li>
<li>Zeitmodus-Zeitcode</li>
<li>Nachverfolgung plus</li>
<li>Nachverfolgung minus</li>
<li>Nachverfolgen der Zurücksetzung</li>
</ul></td>
</tr>
<tr class="even">
<td>videodisc</td>
<td><ul>
<li>Audio all off</li>
<li>Audio all on</li>
<li>Audio links</li>
<li>audio left on</li>
<li>Audio von Rechts nach rechts</li>
<li>Audio direkt ein</li>
<li>Tür geschlossen</li>
<li>Tür geöffnet</li>
<li>Zeitformatrahmen</li>
<li>Zeitformat hms</li>
<li>Zeitformat millisekunden</li>
<li>Zeitformatspur</li>
<li>Video off</li>
<li>Video zu</li>
</ul></td>
</tr>
<tr class="odd">
<td>Waveaudio</td>
<td><ul>
<li>Ganze <em>Ausrichtungszahl</em></li>
<li>beliebige Eingaben</li>
<li>beliebige Ausgabe</li>
<li>Audio all off</li>
<li>Audio all on</li>
<li>Audio links</li>
<li>audio left on</li>
<li>Audio von Rechts nach rechts</li>
<li>Audio direkt ein</li>
<li>bitspersample <em>bit_count</em></li>
<li>bytespersec <em>byte_rate</em></li>
<li>Kanäle <em>channel_count</em></li>
<li>Tür geschlossen</li>
<li>Tür geöffnet</li>
<li>Formattag pcm</li>
<li>Tagtag <em>formatieren</em></li>
<li><em>Eingabe-Ganzzahl</em></li>
<li>Ganzzahlige <em>Ausgabe</em></li>
<li>samplespersec <em>integer</em></li>
<li>Bytes im Zeitformat</li>
<li>Zeitformat millisekunden</li>
<li>Zeitformatbeispiele</li>
</ul></td>
</tr>
</tbody>
</table>



 

In der folgenden Tabelle sind die Flags, die im **lpszSetting-Parameter** angegeben werden können, und ihre Bedeutungen aufgeführt.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Wert</th>
<th>Bedeutung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Ganze <em>Ausrichtungszahl</em></td>
<td>Legt die Ausrichtung von Datenblöcken relativ zum Anfang der Daten fest, die an das Waveform-Audio-Gerät übergeben werden. Die Datei wird in diesem Format gespeichert.</td>
</tr>
<tr class="even">
<td>beliebige Eingaben</td>
<td>Verwenden Sie alle Eingaben, die das aktuelle Format bei der Aufzeichnung unterstützen. Dies ist die Standardeinstellung.</td>
</tr>
<tr class="odd">
<td>beliebige Ausgabe</td>
<td>Verwenden Sie bei der Wiedergabe eine beliebige Ausgabe, die das aktuelle Format unterstützt. Dies ist die Standardoption.</td>
</tr>
<tr class="even">
<td>Datensatz zusammenstellen auf <br/> Datensatz ausstellen <br/></td>
<td>Im Assemblermodus werden alle Spuren gemäß der Definition des Geräts aufgezeichnet. Die meisten VCRs befinden sich standardmäßig im Assemblermodus.</td>
</tr>
<tr class="odd">
<td>Audio all off <br/> Audio all on <br/></td>
<td>Deaktiviert oder aktiviert die Audioausgabe. Videoüberlagerungsgeräte, der MCISEQ-Sequencer und das MCIWAVE-Waveform-Audiogerät unterstützen dieses Flag nicht.</td>
</tr>
<tr class="even">
<td>Audio links <br/> audio left on <br/> Audio von Rechts nach rechts <br/> Audio direkt ein <br/></td>
<td>Deaktiviert oder aktiviert die Ausgabe im linken oder rechten Audiokanal. Videoüberlagerungsgeräte, der MCISEQ-Sequencer und das MCIWAVE-Waveform-Audiogerät unterstützen dieses Flag nicht.</td>
</tr>
<tr class="odd">
<td>bitspersample <em>bit_count</em></td>
<td>Legt die Anzahl der Bits pro PCM-Beispiel (Pulse Code Cod) fest, das abgespielt oder aufgezeichnet wurde. Die Datei wird in diesem Format gespeichert.</td>
</tr>
<tr class="even">
<td>bytespersec <em>byte_rate</em></td>
<td>Legt die durchschnittliche Anzahl der pro Sekunde abgespielten oder aufgezeichneten Bytes fest. Die Datei wird in diesem Format gespeichert.</td>
</tr>
<tr class="odd">
<td>kanäle <em>channel_count</em></td>
<td>Legt die Kanäle für Wiedergabe und Aufzeichnung fest. Die Datei wird in diesem Format gespeichert.</td>
</tr>
<tr class="even">
<td><em>Uhrzeit</em></td>
<td>Legt die Zeit für die externe Uhr auf <em>time fest.</em> Das Format wird als long-Ganzzahl ohne Vorzeichen angegeben.</td>
</tr>
<tr class="odd">
<td>Indikatorformat</td>
<td>Legen Sie das Zeitformat für den Leistungsindikator fest, wie vom <a href="status.md">Statusindikator</a> &quot; &quot; zurückgegeben. Informationen zu anwendbaren Typen finden Sie unter dem Befehl set time format ( <strong>Festlegen</strong> des &quot; &quot; Zeitformats).</td>
</tr>
<tr class="even">
<td><em>Indikatorwert</em></td>
<td>Legt den VCR-Indikator auf den angegebenen Wert fest. Der Wert muss im aktuellen Indikatorformat angegeben werden. Weitere Informationen finden Sie unter dem Befehl <strong>set</strong> &quot; counter format &quot; .</td>
</tr>
<tr class="odd">
<td>Tür geschlossen</td>
<td>Zieht die Taskleiste zurück und schließt die Tür, wenn möglich. Bei VCRs lädt das Band automatisch.</td>
</tr>
<tr class="even">
<td>Door Open</td>
<td>Öffnet die Tür und wirft nach Möglichkeit die Taskleiste oder das Band aus.</td>
</tr>
<tr class="odd">
<td><em>Dateiformat</em></td>
<td>Gibt ein Dateiformat an, das für <a href="save.md">Speicher-</a> oder <a href="capture.md">Erfassungsbefehle</a> verwendet wird. Wenn dies nicht angegeben wird, wird möglicherweise standardmäßig ein vom Gerätetreiber definiertes Format verwendet. Wenn das angegebene Dateiformat mit dem aktuell ausgewählten Algorithmus und der Qualität in Konflikt steht, werden sie in die Standardwerte für das Dateiformat geändert. Die folgenden Dateiformate werden definiert:
<ul>
<li>avi: Gibt das AVI-Format an.</li>
<li>avss: Gibt das AVSS-Format an.</li>
<li>dib: Gibt das DIB-Format an.</li>
<li>jfif: Gibt das JFIF-Format an.</li>
<li>jpeg: Gibt das JPEG-Format an.</li>
<li>mpeg: Gibt das MPEG-Format an.</li>
<li>rdib: Gibt das RLE DIB-Format an.</li>
<li>rjpeg: Gibt das RJPEG-Format an.</li>
</ul></td>
</tr>
<tr class="even">
<td>format tag pcm</td>
<td>Legt den Formattyp zum Wiedergeben und Aufzeichnen auf PCM fest. Die Datei wird in diesem Format gespeichert.</td>
</tr>
<tr class="odd">
<td><em>Formattagtag</em></td>
<td>Legt den Formattyp für Wiedergabe und Aufzeichnung fest. Die Datei wird in diesem Format gespeichert.</td>
</tr>
<tr class="even">
<td>Indexzeitcode <br/> Indexzähler <br/> Indexdatum <br/> Indexzeit <br/></td>
<td>Legt den aktuellen Anzeigebildschirm auf dem VCR fest.</td>
</tr>
<tr class="odd">
<td><em>Eingabe-Ganzzahl</em></td>
<td>Legt den als Eingabe verwendeten Audiokanal fest.</td>
</tr>
<tr class="even">
<td><em>Längendauer</em></td>
<td>Legt die vom Benutzer angegebene Länge des Bandes im VCR fest. Diese Länge wird vom <a href="status.md">Befehl status</a> length zurückgegeben und für die Kompatibilität mit &quot; Anwendungen &quot; bereitgestellt, für die dieser Befehl eine gültige Länge zurückgeben muss.</td>
</tr>
<tr class="odd">
<td>master masters</td>
<td>Legt den SEQUENCER als Synchronisierungsquelle fest. Die Synchronisierungsdaten werden im FORMAT FORMAT DER Synchronisierung gesendet. Der MCISEQ-Sequencer unterstützt dieses Flag nicht.</td>
</tr>
<tr class="even">
<td>master none</td>
<td>Verhindert das Senden von Synchronisierungsdaten durch den CSV-Sequencer. Der MCISEQ-Sequencer unterstützt dieses Flag nicht.</td>
</tr>
<tr class="odd">
<td>master smpte</td>
<td>Legt den SEQUENCER als Synchronisierungsquelle fest. Synchronisierungsdaten werden im SMPTE-Format (Society of Motion Picture and Tv Engineers) gesendet. Der MCISEQ-Sequencer unterstützt dieses Flag nicht.</td>
</tr>
<tr class="even">
<td><em>Offsetzeit</em></td>
<td>Legt die SMPTE-Offsetzeit fest. <em></em> Der Offset ist die Anfangszeit einer SMPTE-basierten Sequenz. Die <em>Zeit</em> wird als <em>hh</em>ausgedrückt: <em>mm</em>: <em>ss</em>: <em>ff</em>, wobei <em>hh</em> Stunden, <em>mm</em> Minuten, <em>ss</em> Sekunden und <em>ff</em> Frames ist.</td>
</tr>
<tr class="odd">
<td><em>Ausgabe ganze Zahl</em></td>
<td>Legt den als Ausgabe verwendeten Audiokanal fest.</td>
</tr>
<tr class="even">
<td><em>Timeout</em> anhalten</td>
<td>Legt die maximale Dauer eines <a href="pause.md">Pausenbefehls</a> in Millisekunden fest. Der <em>Timeoutwert</em> 0 gibt an, dass kein Timeout auftritt.</td>
</tr>
<tr class="odd">
<td><em>Dauer</em> der Postrolls</td>
<td>Legt die Länge im aktuellen Zeitformat fest, die benötigt wird, um den VCR-Transport zu unterbrechen, wenn ein <a href="stop.md">Befehl zum Beenden</a> oder <strong>Anhalten</strong> ausgegeben wird.</td>
</tr>
<tr class="even">
<td>Portzuordnung</td>
<td>Legt die MAPPER-Schnittstelle als Port fest, der die MELDUNGEN empfängt. Dieser Befehl schlägt fehl, wenn der MAPPer oder ein benötigter Port von einer anderen Anwendung verwendet wird.</td>
</tr>
<tr class="odd">
<td>Port "None"</td>
<td>Deaktiviert das Senden von SMS-Nachrichten. Mit diesem Befehl wird auch ein PORTS geschlossen.</td>
</tr>
<tr class="even">
<td>port <em>port_number</em></td>
<td>Legt den PORTS FEST, der die MELDUNGEN empfängt. Dieser Befehl schlägt fehl, wenn der Port, den Sie öffnen möchten, von einer anderen Anwendung verwendet wird.</td>
</tr>
<tr class="odd">
<td>Einschalten <br/> Ausschalten <br/></td>
<td>Legt die Ein- oder Ausschalten des Geräts fest.</td>
</tr>
<tr class="even">
<td><em>Dauer</em> des Vorabrollings</td>
<td>Legt die Länge im aktuellen Zeitformat fest, die zur Stabilisierung der VCR-Ausgabe erforderlich ist.</td>
</tr>
<tr class="odd">
<td>Datensatzformat SP <br/> Datensatzformat LP <br/> Datensatzformat EP <br/></td>
<td>Legt den Aufzeichnungsmodus für den VCR auf SP für die Standardwiedergabe, EP für erweiterte Wiedergabe oder LP für lange Wiedergabe fest. Diese Werte sind nicht VHS-spezifisch. Sie werden drei geeigneten Modi mit anderen Bandformaten zugeordnet. Beispielsweise wird SP der schnellsten Aufzeichnung mit der höchsten Qualität zugeordnet.</td>
</tr>
<tr class="even">
<td>samplespersec <em>integer</em></td>
<td>Legt die Abtastrate für Wiedergabe und Aufzeichnung fest. Die Datei wird in diesem Format gespeichert.</td>
</tr>
<tr class="odd">
<td>Suchen sie genau nach<br/> Suchen sie genau aus <br/></td>
<td>Wählt einen von zwei Suchmodi aus. Wenn &quot; seek genau auf festgelegt &quot; ist, wird seek immer in den angegebenen Frame verschoben. Wenn &quot; seek genau deaktiviert &quot; ist, wechselt seek zum nächstgelegenen Keyframe vor dem angegebenen Frame.</td>
</tr>
<tr class="even">
<td>Untergeordnete Datei</td>
<td>Legt fest, dass der SEQUENCEr Dateidaten als Synchronisierungsquelle verwendet. Dies ist die Standardeinstellung.</td>
</tr>
<tr class="odd">
<td>Slave Slave Slave</td>
<td>Legt den SEQUENCEr für die Verwendung eingehenderSKRIPT-Daten für die Synchronisierungsquelle fest. Der Sequencer erkennt Synchronisierungsdaten im formatierten formatiert. Der MCISEQ-Sequencer unterstützt dieses Flag nicht.</td>
</tr>
<tr class="even">
<td>Slave none</td>
<td>Legt fest, dass der SEQUENCEr die Synchronisierung ignoriert.</td>
</tr>
<tr class="odd">
<td>slave smpte</td>
<td>Legt den SEQUENCEr für die Verwendung eingehenderSKRIPT-Daten für die Synchronisierungsquelle fest. Der Sequencer erkennt Synchronisierungsdaten im SMPTE-Format. Der MCISEQ-Sequencer unterstützt dieses Flag nicht.</td>
</tr>
<tr class="even">
<td>Geschwindigkeitsfaktor</td>
<td>Legt die relative Geschwindigkeit der Video- und Audiowiedergabe aus dem Arbeitsbereich fest. Faktor ist das Verhältnis zwischen der nominalen Bildfrequenz und der gewünschten Bildfrequenz, wobei die nominale Bildfrequenz als 1000 festgelegt ist. (Eine Rate von 500 ist halb normale Geschwindigkeit, 2000 ist doppelt normale Geschwindigkeit und so weiter.) Wenn Die Geschwindigkeit auf 0 (null) gesetzt wird, wird das Video so schnell wie möglich abspielt, ohne Frames und ohne Audio zu löschen.</td>
</tr>
<tr class="odd">
<td>Format des Dateiformats <em>"still"</em></td>
<td>Gibt das Dateiformat an, das für Erfassungsbefehle verwendet wird.</td>
</tr>
<tr class="even">
<td>Tempo tempo_value</td>
<td>Legt das Tempo der Sequenz gemäß dem aktuellen Zeitformat fest. Bei einer PPQN-basierten Datei wird die tempo_value als Takte pro Minute interpretiert. Bei einer SMPTE-basierten Datei wird die tempo_value als Frames pro Sekunde interpretiert.</td>
</tr>
<tr class="odd">
<td>Bytes im Zeitformat</td>
<td>In einem PCM-Dateiformat legt das Zeitformat auf Bytes fest. Alle Positionsinformationen werden nach diesem Befehl als Bytes angegeben.</td>
</tr>
<tr class="even">
<td>Zeitformatrahmen</td>
<td>Legt das Zeitformat auf Frames fest. Alle Befehle, die Positionswerte verwenden, setzen Frames voraus. Wenn das Gerät geöffnet wird, ist Frames der Standardmodus. Wird von Videodiscs im CAV-Format unterstützt.</td>
</tr>
<tr class="odd">
<td>Zeitformat hms</td>
<td>Legt das Zeitformat auf Stunden, Minuten und Sekunden fest. Alle Befehle, die Positionswerte verwenden, setzen HMS voraus. HMS ist das Standardformat für CLV-Videodiscs. Geben Sie einen HMS-Wert als hh:mm:ss an, wobei hh stunden, mm minuten und ss Sekunden ist. Sie können ein Feld weglassen, wenn es und alle folgenden Felder 0 (null) sind. Beispielsweise sind 3, 3:0 und 3:0:0 alle gültige Möglichkeiten, drei Stunden auszudrücken. <br/></td>
</tr>
<tr class="even">
<td>Zeitformat millisekunden</td>
<td>Legt das Zeitformat auf Millisekunden fest. Alle Befehle, die Positionswerte verwenden, nehmen Millisekunden an. Sie können Millisekunden als &quot; ms abkürzen. &quot; Für Sequencergeräte legt die Sequenzdatei das Standardformat auf PPQN oder SMPTE fest. Videoüberlagerungsgeräte unterstützen dieses Flag nicht.<br/></td>
</tr>
<tr class="odd">
<td>zeitformat msf</td>
<td>Legt das Zeitformat auf Minuten, Sekunden und Frames fest. Alle Befehle, die Positionswerte verwenden, setzen MSF voraus (das Standardformat für CD-Audio). Geben Sie einen MSF-Wert als mm:ss:ff an, wobei mm Minuten, ss Sekunden und ff Frames ist. Sie können ein Feld weglassen, wenn es und alle folgenden Felder 0 (null) sind. Beispielsweise sind 3, 3:0 und 3:0:0 gültige Möglichkeiten, 3 Minuten auszudrücken.<br/> Die MSF-Felder haben die folgenden maximalen Werte:<br/>
<ul>
<li>Minuten 99</li>
<li>Sekunden 59</li>
<li>Frames 74</li>
</ul></td>
</tr>
<tr class="even">
<td>Zeitformatbeispiele</td>
<td>Legt das Zeitformat auf Beispiele fest. Alle Positionsinformationen werden als Beispiele nach diesem Befehl angegeben.</td>
</tr>
<tr class="odd">
<td>Zeitformat smpte 24<br/> Zeitformat smpte 25<br/> Zeitformat smpte 30<br/></td>
<td>Legt das Zeitformat auf eine SMPTE-Framerate fest. Legt für VCRs das Zeitformat auf hh:mm:ss:ff fest, wobei die rechtlichen Werte 00:00:00:00 bis 23:59:59:xx sind und xx eins kleiner als die Frames pro Sekunde ist, wie durch die Zahl 24, 25 oder 30 angegeben, wie im Flag angegeben. Bei der Eingabe werden Doppelpunkte (:) sind erforderlich, um die Komponenten zu trennen. Die am wenigsten signifikanten Einheiten können weggelassen werden, wenn sie 00 sind. Beispielsweise ist 02:00 identisch mit 02:00:00:00. Alle Befehle, die Positionswerte verwenden, nehmen das SMPTE-Format an.<br/> Die Sequenzdatei legt das Standardformat auf PPQN oder SMPTE fest.<br/></td>
</tr>
<tr class="even">
<td>Zeitformat smpte 30 drop</td>
<td>Legt das Zeitformat auf SMPTE 30 Drop Frame Rate fest. Bei VCRs ist dies mit SMPTE 30 identisch, mit der Ausnahme, dass bestimmte Zeitcodepositionen aus dem Format gelöscht werden, damit die aufgezeichneten Zeitcodepositionen für jeden Frame (bei der NTSC-Framerate von 29,97 FPS) der Echtzeit (bei 30 Fps) entsprechen. Die gelöschten Zeitcodepositionen lauten wie folgt: zwei pro Minute für die ersten neun der zehn Minuten aufgezeichneten Inhalte. Um 01:04:59:29 wäre die nächste Timecodeposition beispielsweise 01:05:00:02 und nicht 01:05:00:00. Alle Befehle, die Positionswerte verwenden, nehmen das SMPTE-Format an.<br/> Die Sequenzdatei legt das Standardformat auf PPQN oder SMPTE fest.<br/></td>
</tr>
<tr class="odd">
<td>Musikzeiger im Zeitformat</td>
<td>Legt das Zeitformat auf einen Songzeiger fest (16 Notizen). Alle Befehle, die Positionswerte verwenden, setzen Songzeigereinheiten voraus. Dieses Flag ist nur für eine Sequenz vom Divisionstyp PPQN gültig.</td>
</tr>
<tr class="even">
<td>Zeitformat tmsf</td>
<td>Legt das Zeitformat auf Spuren, Minuten, Sekunden und Frames fest. Alle Befehle, die Positionswerte verwenden, setzen TMSF voraus. Geben Sie einen TMSF-Wert als tt:mm:ss:ff an, wobei tt für tracks, mm für minutes, ss für seconds und ff für frames steht. Sie können ein Feld weglassen, wenn es und alle folgenden Felder 0 (null) sind. Beispielsweise sind 3, 3:0, 3:0:0 und 3:0:0:0 alle gültige Möglichkeiten zum Ausdrücken von Track 3. <br/> Die TMSF-Felder haben die folgenden maximalen Werte:<br/>
<ul>
<li>Tracks 99</li>
<li>Minuten 90</li>
<li>Sekunden 59</li>
<li>Frames 74</li>
</ul></td>
</tr>
<tr class="odd">
<td>Zeitformatspur</td>
<td>Legt das Positionsformat auf Tracks fest. Alle Befehle, die Positionswerte verwenden, nehmen Spuren an.</td>
</tr>
<tr class="even">
<td>Zeitmoduszähler</td>
<td>Legt den Positionsinformationsmodus für die Verwendung der VCR-Leistungsindikatoren fest.</td>
</tr>
<tr class="odd">
<td>Erkennung im Zeitmodus</td>
<td>Legt den Positionsinformationsmodus basierend auf der Erkennung von Zeitcodeinformationen auf dem Band fest. Wenn Zeitcodeinformationen erkannt werden, wird der Zeittyp auf timecode festgelegt. Andernfalls wird der Zeittyp &quot; &quot; auf counter &quot; &quot; festgelegt. &quot;Erkennen &quot; ist ein spezieller Modus. Wenn der Treiber geöffnet wird, ein neues Band eingefügt oder der Zeitmodusbefehl ausgegeben wird, überprüft der Treiber den auf dem Band verfügbaren aktuellen Zeitmodus und legt den Zeittyp entweder auf den Zeitcode oder den Zähler &quot; &quot; &quot; &quot; &quot; &quot; &quot; &quot; fest. Sobald &quot; der Zeittyp festgelegt ist, ändert der Treiber ihn erst, wenn eine der oben genannten &quot; Bedingungen erneut auftritt.<br/></td>
</tr>
<tr class="even">
<td>Zeitmodus-Zeitcode</td>
<td>Legt den Positionsinformationsmodus fest, um &quot; &quot; Zeitcodeinformationen auf dem Band zu verwenden.</td>
</tr>
<tr class="odd">
<td>Nachverfolgung plus <br/> Nachverfolgungs-Minus <br/> Nachverfolgungsrücksetzung <br/></td>
<td>Passt die Geschwindigkeit des Videobandtransports in feinen Schritten an. Verwenden Sie die &quot; &quot; Nachverfolgungsflags, wenn ein lautes Bild von einem VCR abgerufen wird. &quot;Die Nachverfolgung plus &quot; erhöht die Transportgeschwindigkeit. &quot;Die Nachverfolgung &quot; abzüglich verringert die Transportgeschwindigkeit. &quot;Die Nachverfolgungszurücksetzung &quot; gibt die Nachverfolgungsanpassung auf 0 (null) zurück.</td>
</tr>
<tr class="even">
<td>Video aus</td>
<td>Deaktiviert die Videoausgabe.</td>
</tr>
<tr class="odd">
<td>Video zu</td>
<td>Aktiviert die Videoausgabe.</td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Kann "wait", "notify" oder beides sein. Für DigitalVideo- und VCR-Geräte kann auch "Test" angegeben werden. Weitere Informationen zu diesen Flags finden Sie unter [Die Warte-, Benachrichtigungs- und Testflags.](the-wait-notify-and-test-flags.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn der Fehler erfolgreich war, oder andernfalls ein Fehler.

## <a name="remarks"></a>Hinweise

Mehrere Eigenschaften von Waveform-Audiodaten werden definiert, wenn die Datei zum Speichern der Daten erstellt wird. Diese Eigenschaften beschreiben, wie die Daten innerhalb der Datei strukturiert sind und können nach Beginn der Aufzeichnung nicht mehr geändert werden. In der folgenden Liste werden diese Eigenschaften identifiziert:

-   Ausrichtung
-   bitspersample
-   bytespersec
-   channels
-   Formattag
-   samplespersec

## <a name="examples"></a>Beispiele

Der folgende Befehl legt das Zeitformat auf Millisekunden und das Waveform-Audio-Format auf 8 Bit, Mono, 11 kHz fest.

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

[Mci](mci.md)
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

 

