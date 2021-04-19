---
title: SET-Befehl
description: Mit dem SET-Befehl werden Steuerungseinstellungen für das Gerät festgelegt. CD-Audiodateien, Digital Video, MIDI Sequencer, VCR, Videodisk, Video-Overlay und Waveform-Audiogeräte erkennen diesen Befehl.
ms.assetid: 1ec4d84e-372a-4b6d-b694-f5afb41f90b2
keywords:
- SET-Befehl Windows Multimedia
topic_type:
- apiref
api_name:
- set
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 914743db038b0cae32b53fa79b7696ddba1ad05b
ms.sourcegitcommit: 8276af9231bdbf5a7334299f0d13fc8ff069a065
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/12/2021
ms.locfileid: "106363823"
---
# <a name="set-command"></a>SET-Befehl

> [!NOTE]
> Bias-freie Kommunikation Microsoft unterstützt eine unterschiedlichste und inklusive Umgebung.  In diesem Dokument sind Verweise auf das Wort "Slave" vorhanden. Im [Stil Handbuch von Microsoft für die Bias-Free-Kommunikation](https://github.com/MicrosoftDocs/microsoft-style-guide/blob/master/styleguide/bias-free-communication.md) wird dies als ausschließendes Wort erkannt.  Dieser Wortlaut wird verwendet, da es sich zurzeit um den in den Befehlen verwendeten Wortlaut handelt. Aus Konsistenz Gründen enthält dieses Dokument dieses Wort. Wenn dieses Wort in den Befehlen geändert wird, korrigieren wir dieses Dokument als Ausrichtung.


Mit dem SET-Befehl werden Steuerungseinstellungen für das Gerät festgelegt. CD-Audiodateien, Digital Video, MIDI Sequencer, VCR, Videodisk, Video-Overlay und Waveform-Audiogeräte erkennen diesen Befehl.

Um diesen Befehl zu senden, wenden Sie die [**mciSendString**](/previous-versions//dd757161(v=vs.85)) -Funktion mit dem festgelegten *lpszcommand* -Parameter wie folgt an.

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

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszde viceid*
</dt> <dd>

Der Bezeichner eines MCI-Geräts. Dieser Bezeichner oder Alias wird zugewiesen, wenn das Gerät geöffnet wird.

</dd> <dt>

<span id="lpszSetting"></span><span id="lpszsetting"></span><span id="LPSZSETTING"></span>*lpszsetting*
</dt> <dd>

Flag zum Einrichten von Steuerungseinstellungen. In der folgenden Tabelle werden die Gerätetypen aufgelistet, die den **Set** -Befehl und die von den einzelnen Typen verwendeten Flags erkennen.



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
<td>CDAudio</td>
<td><ul>
<li>audioalles aus</li>
<li>alles audioon</li>
<li>Audiodaten ausgelassen</li>
<li>Audiodatei Links</li>
<li>Audiodaten direkt aus</li>
<li>Audiodaten direkt am</li>
<li>Tür geschlossen</li>
<li>Tür geöffnet</li>
<li>Zeitformat (Millisekunden)</li>
<li>Zeitformat MSF</li>
<li>Zeitformat-TMSF</li>
</ul></td>
</tr>
<tr class="even">
<td>Digitalvideo</td>
<td><ul>
<li>audioalles aus</li>
<li>alles audioon</li>
<li>Audiodaten ausgelassen</li>
<li>Audiodatei Links</li>
<li>Audiodaten direkt aus</li>
<li>Audiodaten direkt am</li>
<li>Tür geschlossen</li>
<li>Tür geöffnet</li>
<li>Dateiformat <em>Format</em></li>
<li>genau suchen</li>
<li>genau suchen</li>
<li>Geschwindigkeits <em>Faktor</em></li>
<li>immer noch Dateiformat <em>Format</em></li>
<li>Zeitformat Rahmen</li>
<li>Zeitformat (Millisekunden)</li>
<li>Video aus</li>
<li>Video zum</li>
</ul></td>
</tr>
<tr class="odd">
<td>overlay</td>
<td><ul>
<li>audioalles aus</li>
<li>alles audioon</li>
<li>Audiodaten ausgelassen</li>
<li>Audiodatei Links</li>
<li>Audiodaten direkt aus</li>
<li>Audiodaten direkt am</li>
<li>Tür geschlossen</li>
<li>Tür geöffnet</li>
<li>Video aus</li>
<li>Video zum</li>
</ul></td>
</tr>
<tr class="even">
<td>sequencer</td>
<td><ul>
<li>audioalles aus</li>
<li>alles audioon</li>
<li>Audiodaten ausgelassen</li>
<li>Audiodatei Links</li>
<li>Audiodaten direkt aus</li>
<li>Audiodaten direkt am</li>
<li>Tür geschlossen</li>
<li>Tür geöffnet</li>
<li>Master-MIDI</li>
<li>Master-None</li>
<li>Master-SMPTE</li>
<li>Offset <em>Zeit</em></li>
<li>Port-Mapper</li>
<li>Port None</li>
<li>Port <em>port_number</em></li>
<li>Slave-Datei</li>
<li>Slave (MIDI)</li>
<li>Slave None</li>
<li>Slave-SMPTE</li>
<li><em>tempo_value</em> in Tempo</li>
<li>Zeitformat (Millisekunden)</li>
<li>Zeitformat-SMPTE- <em>fps</em></li>
<li>Zeitformat SMPTE 30 Drop</li>
<li>Zeiger für Zeitformat Titel</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>VCR</strong></td>
<td><ul>
<li>Datensatz Assemblieren auf</li>
<li>Datensatz aus Assemblieren</li>
<li>audioalles aus</li>
<li>alles audioon</li>
<li>Audiodaten ausgelassen</li>
<li>Audiodatei Links</li>
<li>Audiodaten direkt aus</li>
<li>Audiodaten direkt am</li>
<li><em>Uhrzeit</em></li>
<li>Counter-Format</li>
<li><em>Leistungswert</em></li>
<li>Tür geschlossen</li>
<li>Tür geöffnet</li>
<li>Index Indikator</li>
<li>Index Datum</li>
<li>Index Zeit</li>
<li>Index Zeit</li>
<li>codelta ength- <em>Dauer</em></li>
<li><em>Timeout</em> für Pause</li>
<li>Postroll Dauer-</li>
<li><em>duration</em></li>
<li>Einschalten</li>
<li>Ausschalten</li>
<li><em>Dauer der</em> Vorabversion</li>
<li>Daten Satz Format SP</li>
<li>Daten Satz Format-LP</li>
<li>Daten Satz Format EP</li>
<li>Geschwindigkeits <em>Faktor</em></li>
<li>Zeitformat Rahmen</li>
<li>Zeitformat (HMS)</li>
<li>Zeitformat (Millisekunden)</li>
<li>Zeitformat MSF</li>
<li>Zeitformat-SMPTE- <em>fps</em></li>
<li>Zeitformat SMPTE 30 Drop</li>
<li>Zeitformat-TMSF</li>
<li>Zeit Modus-Counter</li>
<li>Zeit Modus-Erkennung</li>
<li>Zeit Modus-Zeitcode</li>
<li>Nachverfolgung Plus</li>
<li>Nachverfolgung minus</li>
<li>Nachverfolgung zurücksetzen</li>
</ul></td>
</tr>
<tr class="even">
<td>Videodisk</td>
<td><ul>
<li>audioalles aus</li>
<li>alles audioon</li>
<li>Audiodaten ausgelassen</li>
<li>Audiodatei Links</li>
<li>Audiodaten direkt aus</li>
<li>Audiodaten direkt am</li>
<li>Tür geschlossen</li>
<li>Tür geöffnet</li>
<li>Zeitformat Rahmen</li>
<li>Zeitformat (HMS)</li>
<li>Zeitformat (Millisekunden)</li>
<li>Zeitformat Verfolgung</li>
<li>Video aus</li>
<li>Video zum</li>
</ul></td>
</tr>
<tr class="odd">
<td>waveaudiodatei</td>
<td><ul>
<li>Ausrichtungs <em>Ganzzahl</em></li>
<li>beliebige Eingabe</li>
<li>beliebige Ausgabe</li>
<li>audioalles aus</li>
<li>alles audioon</li>
<li>Audiodaten ausgelassen</li>
<li>Audiodatei Links</li>
<li>Audiodaten direkt aus</li>
<li>Audiodaten direkt am</li>
<li>BitsPerSample- <em>BIT_COUNT</em></li>
<li>bytespersec- <em>byte_rate</em></li>
<li>Kanäle <em>channel_count</em></li>
<li>Tür geschlossen</li>
<li>Tür geöffnet</li>
<li>Formattag PCM</li>
<li>tagtag <em></em> formatieren</li>
<li>Eingabe <em>Ganzzahl</em></li>
<li>Ausgabe <em>Ganzzahl</em></li>
<li>samplespersec- <em>Ganzzahl</em></li>
<li>Zeitformat (Bytes)</li>
<li>Zeitformat (Millisekunden)</li>
<li>Zeitformat Beispiele</li>
</ul></td>
</tr>
</tbody>
</table>



 

In der folgenden Tabelle werden die Flags aufgelistet, die im **lpszsetting** -Parameter und deren Bedeutung angegeben werden können.



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
<td>Ausrichtungs <em>Ganzzahl</em></td>
<td>Legt die Ausrichtung von Datenblöcken relativ zum Beginn von Daten fest, die an das Waveform-Audiogerät übermittelt werden. Die Datei wird in diesem Format gespeichert.</td>
</tr>
<tr class="even">
<td>beliebige Eingabe</td>
<td>Verwenden Sie alle Eingaben, die beim Aufzeichnen das aktuelle Format unterstützen. Dies ist die Standardeinstellung.</td>
</tr>
<tr class="odd">
<td>beliebige Ausgabe</td>
<td>Verwenden Sie bei der Wiedergabe jede Ausgabe, die das aktuelle Format unterstützt. Dies ist die Standardoption.</td>
</tr>
<tr class="even">
<td>Datensatz Assemblieren auf <br/> Datensatz aus Assemblieren <br/></td>
<td>Im Assemblierungs Modus werden alle Spuren gemäß der Definition des Geräts aufgezeichnet. Die meisten VCRs befinden sich standardmäßig im assemblierungsmodus.</td>
</tr>
<tr class="odd">
<td>audioalles aus <br/> alles audioon <br/></td>
<td>Deaktiviert oder aktiviert die Audioausgabe. Dieses Flag wird von Video Überlagerungs Geräten, dem mciseq-Sequencer und dem MCIWave Waveform-Audiogerät nicht unterstützt.</td>
</tr>
<tr class="even">
<td>Audiodaten ausgelassen <br/> Audiodatei Links <br/> Audiodaten direkt aus <br/> Audiodaten direkt am <br/></td>
<td>Deaktiviert oder aktiviert die Ausgabe entweder auf den linken oder den rechten Audiokanal. Dieses Flag wird von Video Überlagerungs Geräten, dem mciseq-Sequencer und dem MCIWave Waveform-Audiogerät nicht unterstützt.</td>
</tr>
<tr class="odd">
<td>BitsPerSample- <em>BIT_COUNT</em></td>
<td>Legt die Anzahl von Bits pro PCM (Pulse Code-Modulation) fest, die abgespielt oder aufgezeichnet werden. Die Datei wird in diesem Format gespeichert.</td>
</tr>
<tr class="even">
<td>bytespersec- <em>byte_rate</em></td>
<td>Legt die durchschnittliche Anzahl der wiedergegebenen oder aufgezeichneten Bytes pro Sekunde fest. Die Datei wird in diesem Format gespeichert.</td>
</tr>
<tr class="odd">
<td>Kanäle <em>channel_count</em></td>
<td>Legt die Kanäle für die Wiedergabe und Aufzeichnung fest. Die Datei wird in diesem Format gespeichert.</td>
</tr>
<tr class="even">
<td><em>Uhrzeit</em></td>
<td>Legt die Zeit für die externe Uhr auf die <em>Zeit fest.</em> Das Format wird als lange ganze Zahl ohne Vorzeichen angegeben.</td>
</tr>
<tr class="odd">
<td>Counter-Format</td>
<td>Legen Sie das Zeitformat des Zählers fest, wie vom <a href="status.md">Status</a> -Counter zurückgegeben &quot; &quot; . Informationen zu den entsprechenden Typen finden Sie unter dem Befehl <strong>Set</strong> &quot; Time Format &quot; .</td>
</tr>
<tr class="even">
<td><em>Leistungswert</em></td>
<td>Legt den VCR-Leistungsindikators auf den angegebenen Wert fest. Der Wert muss im aktuellen Leistungswert Format angegeben werden. Weitere Informationen finden Sie unter dem Befehl <strong>Set</strong> &quot; Counter Format &quot; .</td>
</tr>
<tr class="odd">
<td>Tür geschlossen</td>
<td>Zieht die Leiste zurück und schließt die Tür, wenn möglich. Bei VCRs lädt das Band automatisch.</td>
</tr>
<tr class="even">
<td>Tür geöffnet</td>
<td>Öffnet die Tür und fügt, wenn möglich, die Leiste oder das Band ein.</td>
</tr>
<tr class="odd">
<td>Dateiformat <em>Format</em></td>
<td>Gibt ein Dateiformat an, das für Befehle zum <a href="save.md">Speichern</a> oder <a href="capture.md">erfassen</a> verwendet wird. Wenn der Wert nicht angegeben wird, wird standardmäßig ein Gerätetreiber definiertes Format festgelegt. Wenn das angegebene Dateiformat mit dem aktuell ausgewählten Algorithmus und der ausgewählten Qualität in Konflikt steht, werden diese in die Standardwerte für das Dateiformat geändert. Die folgenden Dateiformate sind definiert:
<ul>
<li>AVI: gibt das AVI-Format an.</li>
<li>avss: gibt das avss-Format an.</li>
<li>DIB: gibt das DIB-Format an.</li>
<li>jff: gibt das jff-Format an.</li>
<li>JPEG: gibt das JPEG-Format an.</li>
<li>MPEG: gibt das MPEG-Format an.</li>
<li>rdib: gibt das RLE-DIB-Format an.</li>
<li>rjpeg: gibt das rjpeg-Format an.</li>
</ul></td>
</tr>
<tr class="even">
<td>Formattag PCM</td>
<td>Legt den Formattyp für die Wiedergabe und Aufzeichnung auf PCM fest. Die Datei wird in diesem Format gespeichert.</td>
</tr>
<tr class="odd">
<td>tagtag <em></em> formatieren</td>
<td>Legt den Formattyp für die Wiedergabe und Aufzeichnung fest. Die Datei wird in diesem Format gespeichert.</td>
</tr>
<tr class="even">
<td>Index Zeit Code <br/> Index Indikator <br/> Index Datum <br/> Index Zeit <br/></td>
<td>Legt den aktuellen Anzeige Bildschirm auf dem VCR fest.</td>
</tr>
<tr class="odd">
<td>Eingabe <em>Ganzzahl</em></td>
<td>Legt den Audiokanal fest, der als Eingabe verwendet wird.</td>
</tr>
<tr class="even">
<td>Längen <em>Dauer</em></td>
<td>Legt die vom Benutzer angegebene Länge des Bands in der VCR fest. Diese Länge wird durch den Befehl " <a href="status.md">Status</a> Länge" zurückgegeben &quot; &quot; und wird aus Gründen der Kompatibilität mit Anwendungen bereitgestellt, die erfordern, dass dieser Befehl eine gültige Länge zurückgibt.</td>
</tr>
<tr class="odd">
<td>Master-MIDI</td>
<td>Legt den MIDI-Sequencer als Synchronisierungs Quelle fest. Synchronisierungs Daten werden im Format "MIDI" gesendet. Das Flag wird von mciseq Sequencer nicht unterstützt.</td>
</tr>
<tr class="even">
<td>Master-None</td>
<td>Verhindert, dass der MIDI-Sequencer Synchronisierungs Daten sendet. Das Flag wird von mciseq Sequencer nicht unterstützt.</td>
</tr>
<tr class="odd">
<td>Master-SMPTE</td>
<td>Legt den MIDI-Sequencer als Synchronisierungs Quelle fest. Synchronisierungs Daten werden in SMPTE (Society of Motion Picture and TV Engineers)-Format gesendet. Das Flag wird von mciseq Sequencer nicht unterstützt.</td>
</tr>
<tr class="even">
<td>Offset <em>Zeit</em></td>
<td>Legt die SMPTE-Offset <em>Zeit</em>fest. Der Offset ist die Anfangszeit einer SMPTE-basierten Sequenz. Die <em>Zeit</em> wird als <em>HH</em>: <em>mm</em>: <em>SS</em>: <em>FF</em>ausgedrückt, wobei <em>HH</em> Stunden, <em>mm</em> den Wert Minutes, <em>SS</em> den Wert Sekunden und <em>FF</em> ein Rahmen ist.</td>
</tr>
<tr class="odd">
<td>Ausgabe <em>Ganzzahl</em></td>
<td>Legt den Audiokanal fest, der als Ausgabe verwendet wird.</td>
</tr>
<tr class="even">
<td><em>Timeout</em> für Pause</td>
<td>Legt die maximale Dauer eines <a href="pause.md">Pause</a> -Befehls in Millisekunden fest. Ein <em>Timeout</em> Wert von 0 (null) gibt an, dass kein Timeout auftritt.</td>
</tr>
<tr class="odd">
<td><em>Dauer des</em> postrollbacks</td>
<td>Legt die Länge im aktuellen Zeitformat fest, die zum Bremsen des VCR-Transports erforderlich ist, wenn <strong>ein Befehl zum</strong> <a href="stop.md">Beenden oder anhalten</a> ausgegeben wird.</td>
</tr>
<tr class="even">
<td>Port-Mapper</td>
<td>Legt den MIDI-Mapper als Port fest, der die MIDI-Nachrichten empfängt. Bei diesem Befehl tritt ein Fehler auf, wenn der von ihm benötigte MIDI-Mapper oder Port von einer anderen Anwendung verwendet wird.</td>
</tr>
<tr class="odd">
<td>Port None</td>
<td>Deaktiviert das Senden von MIDI-Nachrichten. Dieser Befehl schließt außerdem einen MIDI-Port.</td>
</tr>
<tr class="even">
<td>Port <em>port_number</em></td>
<td>Legt den zum Empfangen der MIDI-Nachrichten empfangenden MIDI-Port Dieser Befehl schlägt fehl, wenn der Port, den Sie öffnen möchten, von einer anderen Anwendung verwendet wird.</td>
</tr>
<tr class="odd">
<td>Einschalten <br/> Ausschalten <br/></td>
<td>Legt den Geräte Strom auf ein oder aus fest.</td>
</tr>
<tr class="even">
<td><em>Dauer der</em> Vorabversion</td>
<td>Legt die Länge des aktuellen Zeit Formats fest, das zur Stabilisierung der VCR-Ausgabe benötigt wird.</td>
</tr>
<tr class="odd">
<td>Daten Satz Format SP <br/> Daten Satz Format-LP <br/> Daten Satz Format EP <br/></td>
<td>Legt den Aufzeichnungsmodus für VCR auf SP für Standard Wiedergabe, EP für erweitertes spielen oder LP für langes spielen fest. Diese Werte sind nicht als VHS-spezifisch vorgesehen. Sie werden drei geeigneten Modi mit anderen Band Formaten zugeordnet. Beispielsweise wird SP der schnellsten, qualitativ hochwertigen Aufzeichnung zugeordnet.</td>
</tr>
<tr class="even">
<td>samplespersec- <em>Ganzzahl</em></td>
<td>Legt die Stichprobenrate für die Wiedergabe und Aufzeichnung fest. Die Datei wird in diesem Format gespeichert.</td>
</tr>
<tr class="odd">
<td>genau suchen<br/> genau suchen <br/></td>
<td>Wählt einen von zwei Suchmodi aus. Wenn &quot; Sie die Suche genau durchführen &quot; , wechselt Seek immer zum angegebenen Frame. Bei einer &quot; genauen Suche &quot; wird die Suche zum nächsten Keyframe vor dem angegebenen Frame verschoben.</td>
</tr>
<tr class="even">
<td>Slave-Datei</td>
<td>Legt fest, dass der MIDI-Sequencer Datei Daten als Synchronisierungs Quelle verwendet. Dies ist die Standardeinstellung.</td>
</tr>
<tr class="odd">
<td>Slave (MIDI)</td>
<td>Legt fest, dass der MIDI-Sequencer eingehende MIDI-Daten für die Synchronisierungs Quelle verwendet. Die Synchronisierungs Daten werden vom Sequencer mit dem Format "MIDI" erkannt. Das Flag wird von mciseq Sequencer nicht unterstützt.</td>
</tr>
<tr class="even">
<td>Slave None</td>
<td>Legt fest, dass die Synchronisierung ignoriert wird.</td>
</tr>
<tr class="odd">
<td>Slave-SMPTE</td>
<td>Legt fest, dass der MIDI-Sequencer eingehende MIDI-Daten für die Synchronisierungs Quelle verwendet. Der Sequencer erkennt Synchronisierungs Daten mit dem SMPTE-Format. Das Flag wird von mciseq Sequencer nicht unterstützt.</td>
</tr>
<tr class="even">
<td>Geschwindigkeitsfaktor</td>
<td>Legt die relative Geschwindigkeit der Video-und Audiowiedergabe aus dem Arbeitsbereich fest. Der Faktor ist das Verhältnis zwischen der nominalen Frame Rate und der gewünschten Framerate, bei der die nominale frametrate als 1000 festgelegt wird. (Eine Rate von 500 ist die halb normale Geschwindigkeit, 2000 ist die doppelte normale Geschwindigkeit usw.) Wenn Sie die Geschwindigkeit auf NULL festlegen, wird das Video so schnell wie möglich abgespielt, ohne Frames und ohne Audiodaten zu löschen.</td>
</tr>
<tr class="odd">
<td>immer noch Dateiformat <em>Format</em></td>
<td>Gibt das für Aufzeichnungs Befehle verwendete Dateiformat an.</td>
</tr>
<tr class="even">
<td>tempo_value in Tempo</td>
<td>Legt das Tempo der Sequenz entsprechend dem aktuellen Zeitformat fest. Bei einer ppqn-basierten Datei wird die tempo_value als Beats pro Minute interpretiert. Bei einer SMPTE-basierten Datei wird die tempo_value als Frames pro Sekunde interpretiert.</td>
</tr>
<tr class="odd">
<td>Zeitformat (Bytes)</td>
<td>In einem PCM-Dateiformat wird das Zeitformat auf Bytes festgelegt. Alle Positionsinformationen werden nach diesem Befehl als Bytes angegeben.</td>
</tr>
<tr class="even">
<td>Zeitformat Rahmen</td>
<td>Legt das Zeitformat auf Frames fest. Alle Befehle, die Positionswerte verwenden, setzen Frames voraus. Wenn das Gerät geöffnet ist, ist Frames der Standardmodus. Wird von Videodisks unter Verwendung des CAV-Formats unterstützt.</td>
</tr>
<tr class="odd">
<td>Zeitformat (HMS)</td>
<td>Legt das Zeitformat auf Stunden, Minuten und Sekunden fest. Alle Befehle, die Positionswerte verwenden, gehen von "HMS" aus. HMS ist das Standardformat für CLV-Videodisks. Geben Sie einen HMS-Wert als hh: mm: SS an, wobei HH Stunden, mm den Wert Minutes und SS den Wert Sekunden hat. Sie können ein Feld weglassen, wenn es und alle folgenden Felder NULL sind. Beispielsweise sind 3, 3:0 und 3:0:0 alle gültigen Möglichkeiten, um 3 Stunden auszudrücken. <br/></td>
</tr>
<tr class="even">
<td>Zeitformat (Millisekunden)</td>
<td>Legt das Zeitformat auf Millisekunden fest. Alle Befehle, die Positionswerte verwenden, nehmen Millisekunden an. Sie können Millisekunden als &quot; MS abkürzen &quot; . Bei Sequencer-Geräten legt die Sequenz Datei das Standardformat auf ppqn oder SMPTE fest. Das Flag wird von Video Überlagerungs Geräten nicht unterstützt.<br/></td>
</tr>
<tr class="odd">
<td>Zeitformat MSF</td>
<td>Legt das Zeitformat auf Minuten, Sekunden und Frames fest. Bei allen Befehlen, die Positionswerte verwenden, wird MSF (das Standardformat für CD-Audiodaten) angenommen. Geben Sie einen MSF-Wert als mm: SS: FF an, wobei mm für Minuten, SS für Sekunden und FF für Frames steht. Sie können ein Feld weglassen, wenn es und alle folgenden Felder NULL sind. Beispielsweise sind 3, 3:0 und 3:0:0 gültige Möglichkeiten, um 3 Minuten auszudrücken.<br/> Die MSF-Felder haben die folgenden maximalen Werte:<br/>
<ul>
<li>Minuten 99</li>
<li>Sekunden 59</li>
<li>Frames 74</li>
</ul></td>
</tr>
<tr class="even">
<td>Zeitformat Beispiele</td>
<td>Legt das Zeitformat auf Samples fest. Alle Positionsinformationen werden als Beispiele angegeben, die diesem Befehl folgen.</td>
</tr>
<tr class="odd">
<td>Zeitformat SMPTE 24<br/> Uhrzeit Format SMPTE 25<br/> Uhrzeit Format SMPTE 30<br/></td>
<td>Legt das Zeitformat auf eine SMPTE-Frame Rate fest. Für VCRs wird das Zeitformat auf HH: mm: SS: FF festgelegt, wobei die zulässigen Werte 00:00:00:00 bis 23:59:59: XX und XX kleiner als die Frames pro Sekunde sind, wie in der Zahl 24, 25 oder 30 angegeben, wie im-Flag angegeben. Bei Eingabe Doppelpunkte (:) sind erforderlich, um die Komponenten zu trennen. Die am wenigsten wichtigen Einheiten können ausgelassen werden, wenn Sie 00 sind. Beispielsweise ist 02:00 identisch mit 02:00:00:00. Bei allen Befehlen, die Positionswerte verwenden, wird das SMPTE-Format angenommen.<br/> Die Sequenz Datei legt das Standardformat auf ppqn oder SMPTE fest.<br/></td>
</tr>
<tr class="even">
<td>Zeitformat SMPTE 30 Drop</td>
<td>Legt das Zeitformat auf SMPTE 30 Drop Frame Rate fest. Für VCRs, identisch mit SMPTE 30, mit der Ausnahme, dass bestimmte Zeit Code Positionen aus dem Format gelöscht werden, damit die aufgezeichneten Zeit Code Positionen für jeden Frame (mit der NTSC-frametrate von 29,97 fps) der Echt Zeit (bei 30 fps) entsprechen. Die gelöschten Zeit Code Positionen lauten wie folgt: zwei Minuten pro Minute für die ersten neun von zehn Minuten aufgezeichneten Inhalts. Beispielsweise wäre bei 01:04:59:29 die nächste Zeit Code Position 01:05:00:02, nicht 01:05:00:00. Bei allen Befehlen, die Positionswerte verwenden, wird das SMPTE-Format angenommen.<br/> Die Sequenz Datei legt das Standardformat auf ppqn oder SMPTE fest.<br/></td>
</tr>
<tr class="odd">
<td>Zeiger für Zeitformat Titel</td>
<td>Legt das Zeitformat auf einen Song Zeiger fest (sechzehnte Notizen). Bei allen Befehlen, die Positionswerte verwenden, wird von den Song Zeiger Einheiten ausgegangen. Dieses Flag ist nur für eine Sequenz des Divisions Typs "ppqn" gültig.</td>
</tr>
<tr class="even">
<td>Zeitformat-TMSF</td>
<td>Legt das Zeitformat auf nachverfolgt, Minuten, Sekunden und Frames fest. Alle Befehle, die Positionswerte verwenden, setzen TMSF voraus. Geben Sie einen TMSF-Wert als TT: mm: SS: FF an, wobei TT nachverfolgt, mm den Wert Minutes, SS den Wert Sekunden und FF ein Rahmen ist. Sie können ein Feld weglassen, wenn es und alle folgenden Felder NULL sind. Beispielsweise sind 3, 3:0, 3:0:0 und 3:0:0:0 alle gültigen Methoden zum Ausdrücken von Track 3. <br/> Die TMSF-Felder haben die folgenden maximalen Werte:<br/>
<ul>
<li>Nachverfolgt 99</li>
<li>Minuten 90</li>
<li>Sekunden 59</li>
<li>Frames 74</li>
</ul></td>
</tr>
<tr class="odd">
<td>Zeitformat Verfolgung</td>
<td>Legt das Positions Format auf "verfolgt" fest. Alle Befehle, die Positionswerte verwenden, werden nachverfolgt.</td>
</tr>
<tr class="even">
<td>Zeit Modus-Counter</td>
<td>Legt den Positions Informationsmodus für die Verwendung der VCR-Indikatoren fest.</td>
</tr>
<tr class="odd">
<td>Zeit Modus-Erkennung</td>
<td>Legt den Positions Informationsmodus basierend auf der Erkennung von Zeitcode-Informationen auf dem Band fest. Wenn Zeit Code Informationen erkannt werden, wird der Zeittyp auf &quot; Zeitcode festgelegt &quot; . andernfalls wird der Zeittyp auf Counter festgelegt &quot; &quot; . &quot;"Erkennen" &quot; ist ein spezieller Modus. Wenn der Treiber geöffnet wird, ein neues Band eingefügt oder der &quot; Zeit Modus- &quot; Befehl ausgegeben wird, überprüft der Treiber den aktuellen auf dem Band verfügbaren Zeit Modus und legt den &quot; Zeittyp &quot; auf &quot; Zeitcode &quot; oder Counter fest &quot; &quot; . Sobald &quot; der Typ &quot; festgelegt ist, ändert der Treiber ihn erst, wenn eine der oben genannten Bedingungen erneut auftritt.<br/></td>
</tr>
<tr class="even">
<td>Zeit Modus-Zeitcode</td>
<td>Legt den Positions Informationsmodus für die Verwendung &quot; von Zeit Code &quot; Informationen auf dem Band fest.</td>
</tr>
<tr class="odd">
<td>Nachverfolgung Plus <br/> Nachverfolgung minus <br/> Nachverfolgung zurücksetzen <br/></td>
<td>Passt die Geschwindigkeit des Videoband-Transports in fein Inkrementen an. Verwenden Sie &quot; die &quot; nachverfolgungsflags, wenn ein lautes Bild von einem VCR abgerufen wird. &quot;Die Nachverfolgung Plus &quot; erhöht die Transportgeschwindigkeit. &quot;Durch die Nachverfolgung minus wird &quot; die Transportgeschwindigkeit verringert. &quot;Beim Zurücksetzen &quot; der Nachverfolgung wird die nach Verfolgungs Anpassung an 0</td>
</tr>
<tr class="even">
<td>Video aus</td>
<td>Deaktiviert die Videoausgabe.</td>
</tr>
<tr class="odd">
<td>Video zum</td>
<td>Aktiviert die Videoausgabe.</td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszflags*
</dt> <dd>

Kann "wait", "notify" oder beides sein. Für Digital Video-und VCR-Geräte kann auch "Test" angegeben werden. Weitere Informationen zu diesen Flags finden Sie [unter warte-, Benachrichtigungs-und testflags](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.

## <a name="remarks"></a>Bemerkungen

Wenn die Datei zum Speichern der Daten erstellt wird, werden mehrere Eigenschaften von Waveform-Audiodaten definiert. Diese Eigenschaften beschreiben, wie die Daten innerhalb der Datei strukturiert sind und nicht geändert werden können, wenn die Aufzeichnung beginnt. Die folgenden Eigenschaften werden in der folgenden Liste aufgeführt:

-   Ausrichtung
-   BitsPerSample
-   bytespersec
-   channels
-   Tag formatieren
-   samplespersec

## <a name="examples"></a>Beispiele

Mit dem folgenden Befehl wird das Zeitformat auf Millisekunden festgelegt, und das Waveform-Audioformat wird auf 8 Bit, Mono, 11 kHz festgelegt.

``` syntax
set mysound time format ms bitspersample 8 channels 1 samplespersec 11025
```

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[MCI-Befehls Zeichenfolgen](mci-command-strings.md)
</dt> <dt>

[einver](capture.md)
</dt> <dt>

[pause](pause.md)
</dt> <dt>

[Speichern](save.md)
</dt> <dt>

[stop](stop.md)
</dt> </dl>

 

