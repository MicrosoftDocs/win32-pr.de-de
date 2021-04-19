---
title: Status Befehl
description: Mit dem Status Befehl werden Statusinformationen von einem Gerät angefordert. Alle Geräte erkennen diesen Befehl.
ms.assetid: 39961bd7-866d-450d-9fbf-347a8f508481
keywords:
- Status Befehl Windows-Multimedia
topic_type:
- apiref
api_name:
- status
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14ab184ddaca16d0ea96b86a6b062f1e66e2eee2
ms.sourcegitcommit: 8276af9231bdbf5a7334299f0d13fc8ff069a065
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/12/2021
ms.locfileid: "106361735"
---
# <a name="status-command"></a>Status Befehl

> [!NOTE]
> Bias-freie Kommunikation Microsoft unterstützt eine unterschiedlichste und inklusive Umgebung.  In diesem Dokument sind Verweise auf das Wort "Slave" vorhanden. Im [Stil Handbuch von Microsoft für die Bias-Free-Kommunikation](https://github.com/MicrosoftDocs/microsoft-style-guide/blob/master/styleguide/bias-free-communication.md) wird dies als ausschließendes Wort erkannt.  Dieser Wortlaut wird verwendet, da es sich zurzeit um den in den Befehlen verwendeten Wortlaut handelt. Aus Konsistenz Gründen enthält dieses Dokument dieses Wort. Wenn dieses Wort in den Befehlen geändert wird, korrigieren wir dieses Dokument als Ausrichtung.

Mit dem Status Befehl werden Statusinformationen von einem Gerät angefordert. Alle Geräte erkennen diesen Befehl.

Um diesen Befehl zu senden, wenden Sie die [**mciSendString**](/previous-versions//dd757161(v=vs.85)) -Funktion mit dem festgelegten *lpszcommand* -Parameter wie folgt an.

``` syntax
_stprintf_s(
  lpszCommand,
  TEXT("status %s %s %s"),
  lpszDeviceID,
  lpszRequest,
  lpszFlags
);
      
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszde viceid*
</dt> <dd>

Der Bezeichner eines MCI-Geräts. Dieser Bezeichner oder Alias wird zugewiesen, wenn das Gerät geöffnet wird.

</dd> <dt>

<span id="lpszRequest"></span><span id="lpszrequest"></span><span id="LPSZREQUEST"></span>*lpszrequest*
</dt> <dd>

Flag zum Anfordern von Statusinformationen. In der folgenden Tabelle werden die Gerätetypen aufgelistet, die den **Status** Befehl und die von den einzelnen Typen verwendeten Flags erkennen.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Gerätetyp</th>
<th>Anforderungs Flags</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>CDAudio</td>
<td><ul>
<li>CDAudio-typspur <em>Nummer</em></li>
<li>aktuelle Spur</li>
<li>length</li>
<li>Länge der <em>Nachverfolgung</em></li>
<li>Medien vorhanden</li>
<li>Modus</li>
<li>Anzahl der Spuren</li>
<li>position</li>
<li>Positions <em>Nummer</em></li>
<li>ready</li>
<li>Startposition</li>
<li>Zeitformat</li>
</ul></td>
</tr>
<tr class="even">
<td>Digitalvideo</td>
<td><ul>
<li>Audio</li>
<li>Audioausrichtung</li>
<li>AudioBitsPerSample</li>
<li>audioumbrüche</li>
<li>audiobytespersec</li>
<li>Audioeingabe</li>
<li>audiodatensatz</li>
<li>Audioquelle</li>
<li>Audiodatei (samplespersec)</li>
<li>Audiodatenstrom</li>
<li>Barsch</li>
<li>BitsPerPel</li>
<li>Helligkeit</li>
<li>color</li>
<li>Kontrast</li>
<li>aktuelle Spur</li>
<li><em>Festplatten Speicherplatz</em></li>
<li>Datei Abschluss</li>
<li>Dateiformat</li>
<li>Dateimodus</li>
<li>forward</li>
<li>Übersprungene Frames</li>
<li>Gamma</li>
<li>input</li>
<li>Linkes Volume</li>
<li>length</li>
<li>Länge der <em>Nachverfolgung</em></li>
<li>Medien vorhanden</li>
<li>Modus</li>
<li>Überwachen</li>
<li>Monitor-Methode</li>
<li>ell</li>
<li>Nominale Bildrate</li>
<li>Nominale Daten Satz Rahmenrate</li>
<li>Anzahl der Spuren</li>
<li>output</li>
<li>Palettenhandle</li>
<li>Pausenmodus</li>
<li>Wiedergabegeschwindigkeit</li>
<li>position</li>
<li>Positions <em>Nummer</em></li>
<li>ready</li>
<li>Frame Frequenz aufzeichnen</li>
<li>Verweis <em>Rahmen</em></li>
<li>reservierte Größe</li>
<li>richtiges Volume</li>
<li>genau suchen</li>
<li>Schärfe</li>
<li>SMPTE</li>
<li>Geschwindigkeit</li>
<li>Startposition</li>
<li>immer noch Dateiformat</li>
<li>Zeitformat</li>
<li>Tönungs</li>
<li>Höhen</li>
<li>nicht gespeicherte</li>
<li>video</li>
<li>Video Schlüssel Index</li>
<li>Farbe des Video Schlüssels</li>
<li>Videodaten Satz</li>
<li>Videoquelle</li>
<li>Video Quellnummer</li>
<li>Videostream</li>
<li>Volume</li>
<li>Fenster handle</li>
<li>Fenster sichtbar</li>
<li>Fenster minimiert</li>
<li>Fenster maximiert</li>
</ul></td>
</tr>
<tr class="odd">
<td>overlay</td>
<td><ul>
<li>Medien vorhanden</li>
<li>Modus</li>
<li>Anzahl der Spuren</li>
<li>ready</li>
<li>strecken</li>
<li>Fenster handle</li>
</ul></td>
</tr>
<tr class="even">
<td>sequencer</td>
<td><ul>
<li>aktuelle Spur</li>
<li>Divisions Typ</li>
<li>length</li>
<li>Längen Spur- <em>Zahlen</em> Master</li>
<li>Medien vorhanden</li>
<li>Modus</li>
<li>Anzahl der Spuren</li>
<li>offset</li>
<li>port</li>
<li>position</li>
<li>Positions <em>Nummer</em></li>
<li>ready</li>
<li>Sklaverei</li>
<li>Startposition</li>
<li>Lern</li>
<li>Zeitformat</li>
</ul></td>
</tr>
<tr class="odd">
<td>VCR</td>
<td><ul>
<li>Datensatz Assemblieren</li>
<li>audiomonitor</li>
<li>audiomonitornummer</li>
<li>audiodatensatz</li>
<li><em>Anzahl</em> der Audiodaten Satz-Spuren</li>
<li>Audioquelle</li>
<li>audioquellnummer</li>
<li>Kanal</li>
<li>Kanal-Tuner- <em>Nummer</em></li>
<li>clock</li>
<li>Takt-ID</li>
<li>Zähler</li>
<li>Counter-Format</li>
<li>Auflösung von Zählern</li>
<li>aktuelle Spur</li>
<li>Framerate</li>
<li>Index</li>
<li>Index für</li>
<li>length</li>
<li>Länge der <em>Nachverfolgung</em></li>
<li>Medien vorhanden</li>
<li>Medientyp</li>
<li>Modus</li>
<li>Anzahl von Audiospuren</li>
<li>Anzahl der Spuren</li>
<li>Anzahl der Videospuren</li>
<li><em>Timeout</em> für Pause</li>
<li>Wiedergabe Format</li>
<li>position</li>
<li>Positions Anfang</li>
<li>Positions <em>Nummer</em></li>
<li>Postroll <em>Dauer</em></li>
<li>Einschalten</li>
<li>Vorabversion <em></em></li>
<li>ready</li>
<li>Daten Satz Format</li>
<li>Geschwindigkeit</li>
<li>Zeitformat</li>
<li>Zeit Modus</li>
<li>Uhrzeittyp</li>
<li>Zeit Code vorhanden</li>
<li>Zeitcode-Datensatz</li>
<li>timecodetyp</li>
<li>Nummer des Tuners</li>
<li>Videomonitor</li>
<li>Videomonitor Nummer</li>
<li>Videodaten Satz</li>
<li><em>Nummer</em> der Videodaten Satz Verfolgung</li>
<li>Videoquelle</li>
<li>Video Quellnummer</li>
<li>schreibgeschützt</li>
</ul></td>
</tr>
<tr class="even">
<td>Videodisk</td>
<td><ul>
<li>aktuelle Spur</li>
<li>Größe der Festplatte</li>
<li>forward</li>
<li>length</li>
<li>Länge der <em>Nachverfolgung</em></li>
<li>Medien vorhanden</li>
<li>Medientyp</li>
<li>Modus</li>
<li>Anzahl der Spuren</li>
<li>position</li>
<li>Positions <em>Nummer</em></li>
<li>ready</li>
<li>Seite</li>
<li>Geschwindigkeit</li>
<li>Startposition</li>
<li>Zeitformat</li>
</ul></td>
</tr>
<tr class="odd">
<td>waveaudiodatei</td>
<td><ul>
<li>Ausrichtung</li>
<li>BitsPerSample</li>
<li>bytespersec</li>
<li>channels</li>
<li>aktuelle Spur</li>
<li>Tag formatieren</li>
<li>input</li>
<li>length</li>
<li>Länge der <em>Nachverfolgung</em></li>
<li>Level</li>
<li>Medien vorhanden</li>
<li>Modus</li>
<li>Anzahl der Spuren</li>
<li>output</li>
<li>position</li>
<li>Positions <em>Nummer</em></li>
<li>ready</li>
<li>samplespersec</li>
<li>Startposition</li>
<li>Zeitformat</li>
</ul></td>
</tr>
</tbody>
</table>



 

In der folgenden Tabelle werden die Flags aufgelistet, die im **lpszrequest** -Parameter und deren Bedeutung angegeben werden können.



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
<td>Ausrichtung</td>
<td>Gibt die Block Ausrichtung der Daten in Bytes zurück.</td>
</tr>
<tr class="even">
<td>Datensatz Assemblieren</td>
<td>Gibt <strong>true</strong> zurück, wenn das Gerät auf assemblierungsmodusaufzeichnung festgelegt ist.</td>
</tr>
<tr class="odd">
<td>Audio</td>
<td>Gibt ein- &quot; &quot; oder &quot; ausschalten &quot; abhängig vom letzten Befehl " <a href="setaudio.md">setaudioon</a> &quot; " &quot; &quot; oder "Off" &quot; . Es wird ein zurückgegeben &quot; &quot; , wenn entweder oder beide Redner aktiviert sind, &quot; &quot; andernfalls.</td>
</tr>
<tr class="even">
<td>Audioausrichtung</td>
<td>Gibt die Ausrichtung von Datenblöcken relativ zum Anfang der Eingabe-Waveform-Audiodaten zurück.</td>
</tr>
<tr class="odd">
<td>AudioBitsPerSample</td>
<td>Gibt die Anzahl der Bits pro Stichprobe zurück, die vom Gerät für die Aufzeichnung verwendet werden. Dieses Flag gilt nur für Geräte, die den PCM-Algorithmus unterstützen &quot; &quot; .</td>
</tr>
<tr class="even">
<td>audioumbrüche</td>
<td>Gibt die Häufigkeit zurück, mit der der Audioteil der letzten AVI-Sequenz abgebrochen wurde. Das System zählt immer dann eine audiopause, wenn versucht wird, Audiodaten in den Gerätetreiber zu schreiben und feststellt, dass der Treiber bereits alle verfügbaren Daten wiedergegeben hat. Dieses Flag wird nur vom MCIAVI Digital-Video-Treiber erkannt. Es ist nur für die Leistungs Auswertung gedacht. der Rückgabewert ist schwierig zu interpretieren.</td>
</tr>
<tr class="odd">
<td>audiobytespersec</td>
<td>Gibt die durchschnittliche Anzahl der Bytes zurück, die pro Sekunde für die Aufzeichnung verwendet werden.</td>
</tr>
<tr class="even">
<td>Audioeingabe</td>
<td>Gibt die ungefähre sofortige Audioebene des analogen eingabeaudiosignals zurück. Ein Wert größer als 1000 impliziert clippingverzerrung. Einige Geräte können diesen Wert nur beim Aufzeichnen von Audiodaten zurückgeben. Dem Wert ist kein <a href="set.md">Set</a> -oder <a href="setaudio.md">setaudiobefehl</a> zugeordnet.</td>
</tr>
<tr class="odd">
<td>audiomonitor</td>
<td>Gibt &quot; &quot; die Ausgabe oder einen der gültigen Quell Eingabetypen zurück. Weitere Informationen finden Sie unter dem Befehl " <strong>setaudiomonitor</strong> " &quot; &quot; .</td>
</tr>
<tr class="even">
<td>audiomonitornummer</td>
<td>Gibt die überwachte Video Nummer des Typs zurück, der vom <strong>Status</strong> &quot; -audiomonitor angegeben wird &quot; . Weitere Informationen finden Sie unter dem Befehl <a href="setaudio.md">SetAudio.</a></td>
</tr>
<tr class="odd">
<td>audiodatensatz</td>
<td>Gibt &quot; ein &quot; oder &quot; aus zurück &quot; , das den durch <strong>setaudiodatensatz</strong> festgelegten Status widerspiegelt &quot; &quot; .</td>
</tr>
<tr class="even">
<td><em>Anzahl</em> der Audiodaten Satz-Spuren</td>
<td>Gibt " <strong>true</strong> " zurück, wenn der VCR zum Aufzeichnen von Audiodaten festgelegt ist Wenn keine Nachverfolgung angegeben ist, wird der Standardwert 1 angenommen.</td>
</tr>
<tr class="odd">
<td>Audiodatei (samplespersec)</td>
<td>Gibt die Anzahl der Stichproben pro Sekunde zurück, die aufgezeichnet wurden.</td>
</tr>
<tr class="even">
<td>Audioquelle</td>
<td>Gibt die aktuelle audiodigitalisierungs Quelle zurück: &quot; left &quot; , &quot; right &quot; , &quot; Average &quot; oder &quot; Stereo &quot; .</td>
</tr>
<tr class="odd">
<td>audioquellnummer</td>
<td>Gibt die audioquellnummer des Typs zurück, der von der <strong>statusaudioquelle</strong> zurückgegeben wird &quot; &quot; . Weitere Informationen finden Sie unter dem Befehl <a href="setaudio.md">SetAudio.</a></td>
</tr>
<tr class="even">
<td>Audiodatenstrom</td>
<td>Gibt die aktuelle audiostreamnummer zurück.</td>
</tr>
<tr class="odd">
<td>Barsch</td>
<td>Gibt die aktuelle audiobass-Ebene zurück.</td>
</tr>
<tr class="even">
<td>BitsPerPel</td>
<td>Gibt die Anzahl von Bits pro Pixel zum Speichern erfasster oder aufgezeichneter Daten zurück.</td>
</tr>
<tr class="odd">
<td>BitsPerSample</td>
<td>Gibt die Bits pro Stichprobe zurück.</td>
</tr>
<tr class="even">
<td>Helligkeit</td>
<td>Gibt die aktuelle videohelligkeits Ebene zurück.</td>
</tr>
<tr class="odd">
<td>bytespersec</td>
<td>Gibt die durchschnittliche Anzahl von Bytes pro Sekunde wiedergegeben oder aufgezeichnet zurück.</td>
</tr>
<tr class="even">
<td>CDAudio-typspur <em>Nummer</em></td>
<td>Gibt den Typ der angegebenen Nachverfolgung zurück. Hierbei kann es sich um &quot; Audiodaten &quot; oder &quot; andere handeln.&quot;</td>
</tr>
<tr class="odd">
<td>Kanal</td>
<td>Gibt den ganzzahligen Wert des Kanals zurück, der für den Tuner festgelegt wurde.</td>
</tr>
<tr class="even">
<td>Kanal-Tuner- <em>Nummer</em></td>
<td>Wenn eine &quot; Tuner- &quot; <em>Nummer</em> angegeben wird, wird der aktuell ausgewählte Kanal für die logische Tuner- <em>Nummer</em> zurückgegeben. Beachten Sie, dass es mehrere logische Tuner geben kann.</td>
</tr>
<tr class="odd">
<td>channels</td>
<td>Gibt die Anzahl der festgelegten Kanäle zurück (1 für Mono, 2 für Stereo).</td>
</tr>
<tr class="even">
<td>clock</td>
<td>Gibt die externe Zeit zurück. Die Zeit muss eine lange ganze Zahl ohne Vorzeichen sein, die die Gesamt Inkremente ausdrückt. Weitere Informationen finden Sie im Befehl <a href="capability.md">Capability</a> &quot; Clock Inkrement Rate &quot; .</td>
</tr>
<tr class="odd">
<td>Takt-ID</td>
<td>Gibt eine eindeutige Ganzzahl zurück, die die Uhr identifiziert.</td>
</tr>
<tr class="even">
<td>color</td>
<td>Gibt die aktuelle Farb Ebene zurück.</td>
</tr>
<tr class="odd">
<td>Kontrast</td>
<td>Gibt die aktuelle Kontrast Ebene zurück.</td>
</tr>
<tr class="even">
<td>Zähler</td>
<td>Gibt die Gegenposition im aktuellen Leistungs Zählers zurück.</td>
</tr>
<tr class="odd">
<td>Counter-Format</td>
<td>Gibt das aktuelle Leistungs Zähl Format zurück. Weitere Informationen finden Sie unter dem Befehl <a href="set.md">Set</a> &quot; Counter Format &quot; .</td>
</tr>
<tr class="even">
<td>Auflösung von Zählern</td>
<td>Gibt &quot; Frames &quot; oder &quot; Sekunden zurück &quot; , die die Auflösung des Zählers angeben. Dies ist nicht mit der Genauigkeit identisch.</td>
</tr>
<tr class="odd">
<td>aktuelle Spur</td>
<td>Gibt den aktuellen Titel zurück. Der mcist-Sequencer gibt 1 zurück.</td>
</tr>
<tr class="even">
<td>Größe der Festplatte</td>
<td>Gibt entweder 8 oder 12 zurück, was die Größe der geladenen CD in Zoll angibt.</td>
</tr>
<tr class="odd">
<td><em>Festplatten Speicherplatz</em></td>
<td>Gibt den ungefähren Speicherplatz im aktuellen Zeitformat zurück, der durch einen <a href="reserve.md">Reserve</a> Befehl für das angegebene Laufwerk abgerufen werden kann <em>.</em> Das <em>Laufwerk</em> wird in der Regel als einzelner Buchstabe oder als einzelner Buchstabe angegeben, gefolgt von einem Doppelpunkt (:). Einige Geräte verwenden jedoch möglicherweise einen Pfad.</td>
</tr>
<tr class="even">
<td>Divisions Typ</td>
<td>Gibt einen der folgenden Typen von Datei Teilungen zurück:
<ul>
<li>Ppqn</li>
<li>SMPTE 24-Frame</li>
<li>SMPTE 25-Frame</li>
<li>SMPTE 30-Ablage Rahmen</li>
<li>SMPTE 30-Frame</li>
</ul>
<br/> Verwenden Sie diese Informationen, um das Format der Datei "MIDI" und die Bedeutung von "Tempo" und Positionsinformationen zu bestimmen.<br/></td>
</tr>
<tr class="odd">
<td>Datei Abschluss</td>
<td>Gibt den geschätzten Prozentsatz für das <a href="load.md">Laden</a>, <a href="save.md">Speichern</a>, <a href="capture.md">erfassen</a>, <a href="cut.md">Ausschneiden</a>, <a href="copy.md">Kopieren</a>, <a href="delete.md">Löschen</a>, <a href="paste.md">Einfügen</a>oder Rückgängigmachen fort. <a href="undo.md"></a> (Anwendungen können dies verwenden, um einen visuellen Indikator für den Fortschritt bereitzustellen.)</td>
</tr>
<tr class="even">
<td>Dateiformat</td>
<td>Gibt das aktuelle Dateiformat für <a href="record.md">Daten Satz</a> -oder <strong>Speicher</strong> Befehle zurück.</td>
</tr>
<tr class="odd">
<td>Dateimodus</td>
<td>Gibt das &quot; Laden &quot; , &quot; speichern &quot; , &quot; Bearbeiten oder im Leerlauf zurück &quot; &quot; &quot; . Während eines <a href="load.md"><strong>Lade</strong></a> Vorgangs wird das Laden zurückgegeben &quot; &quot; . Während der <a href="https://www.bing.com/search?q=<strong>save</strong>"><strong>Speicher</strong></a> -und <a href="capture.md"><strong>Aufzeichnungs</strong></a> Vorgänge wird das Speichern zurückgegeben &quot; &quot; . Beim <a href="cut.md"><strong>Ausschneiden</strong></a>, <a href="copy.md"><strong>Kopieren</strong></a>, <a href="delete.md"><strong>Löschen</strong></a>, <a href="paste.md"><strong>Einfügen</strong></a>oder Rückgängigmachen wird die Bearbeitung zurückgegeben <a href="undo.md"><strong></strong></a> &quot; &quot; .</td>
</tr>
<tr class="even">
<td>Tag formatieren</td>
<td>Gibt das Formattag zurück.</td>
</tr>
<tr class="odd">
<td>forward</td>
<td>Gibt <strong>true</strong> zurück, wenn die Wiedergabe Richtung vorwärts ist oder wenn das Gerät nicht wiedergegeben wird.</td>
</tr>
<tr class="even">
<td>Framerate</td>
<td>Gibt die Anzahl von Frames pro Sekunde zurück, die vom Gerät standardmäßig verwendet werden. Von NTSC-Geräten werden 30, PAL 25 usw. zurückgegeben.</td>
</tr>
<tr class="odd">
<td>Übersprungene Frames</td>
<td>Gibt die Anzahl der Frames zurück, die beim Abspielen der letzten AVI-Sequenz nicht gezeichnet wurden. Dieses Flag wird nur vom MCIAVI Digital-Video-Treiber erkannt. Es ist nur für die Leistungs Auswertung gedacht. der Rückgabewert ist schwierig zu interpretieren.</td>
</tr>
<tr class="even">
<td>Gamma</td>
<td>Gibt den Wert zurück, der mit <a href="setvideo.md"><strong>setvideo</strong></a> &quot; Gamma auf Value festgelegt wurde &quot; <em></em>.</td>
</tr>
<tr class="odd">
<td>Index</td>
<td>Gibt die aktuelle Index Anzeige zurück. Weitere Informationen finden Sie unter dem Befehl <a href="set.md"><strong>Set</strong></a> &quot; Index &quot; .</td>
</tr>
<tr class="even">
<td>Index für</td>
<td>Gibt <strong>true</strong> zurück, wenn der Index on ist.</td>
</tr>
<tr class="odd">
<td>input</td>
<td>Gibt den Eingabe Satz zurück. Wenn kein Wert festgelegt ist, gibt der zurückgegebene Fehler an, dass ein beliebiges Gerät verwendet werden kann. Bei Digital Video-Geräten werden die Flags "Bass", "Höhen", "Volume", "Helligkeit", "Farbe", " &quot; &quot; Kontrast", "Gamma", " &quot; Schärfe" &quot; &quot; &quot; &quot; oder " &quot; &quot; &quot; &quot; &quot; &quot; &quot; Tönungs" so geändert, &quot; &quot; &quot; &quot; dass Sie nur Dies ist die Standardeinstellung, wenn die Eingabe überwacht wird.</td>
</tr>
<tr class="even">
<td>Linkes Volume</td>
<td>Gibt das für den linken Audiokanal festgelegte Volume zurück.</td>
</tr>
<tr class="odd">
<td>length</td>
<td>Gibt die Gesamtlänge des Mediums im aktuellen Zeitformat zurück. Bei ppqn-Dateien wird die Länge in Song Zeiger Einheiten zurückgegeben. Für SMPTE-Dateien wird dieser Wert als <em>hh: mm: SS: FF</em>zurückgegeben, wobei <em>HH</em> Stunden, <em>mm</em> den Wert Minutes, <em>SS</em> den Wert seconds und <em>FF</em> ein Rahmen ist. Bei VCR-Geräten beträgt die Länge 2 Stunden (es sei denn, die Länge wurde explizit mit dem <a href="https://www.bing.com/search?q=<strong>set</strong>"><strong>Set</strong></a> -Befehl geändert).</td>
</tr>
<tr class="even">
<td>Länge der <em>Nachverfolgung</em></td>
<td>Gibt die Länge der Spur (in Zeit oder Rahmen) zurück, die durch <em>Number</em>angegeben wird. Bei ppqn-Dateien wird die Länge in Song Zeiger Einheiten zurückgegeben. Für SMPTE-Dateien wird dieser Wert als <em>hh: mm: SS: FF</em>zurückgegeben, wobei <em>HH</em> Stunden, <em>mm</em> den Wert Minutes, <em>SS</em> den Wert seconds und <em>FF</em> ein Rahmen ist.<br/></td>
</tr>
<tr class="odd">
<td>Level</td>
<td>Gibt den aktuellen PCM-audiobeispielwert zurück.</td>
</tr>
<tr class="even">
<td>master</td>
<td>Gibt " &quot; MIDI", "None" oder " &quot; &quot; &quot; &quot; SMPTE" &quot; abhängig vom Typ des Synchronisierungs Satzes zurück.</td>
</tr>
<tr class="odd">
<td>Medien vorhanden</td>
<td>Gibt " <strong>true</strong> " zurück, wenn das Medium in das Gerät eingefügt wird, andernfalls " <strong>false</strong> ". Sequencer-, Video-Overlay-, Digital Video-und Waveform-Audiogeräte geben " <strong>true</strong>" zurück.</td>
</tr>
<tr class="even">
<td>Medientyp</td>
<td>Gibt den Typ des Mediums zurück. Bei VCRs sind dies &quot; 8mm &quot; , &quot; VHS &quot; , &quot; SVHS &quot; , &quot; Beta &quot; , &quot; Hi8 &quot; , &quot; edbeta &quot; oder &quot; andere &quot; . Bei Video Disks handelt es sich hierbei um &quot; CAV &quot; , &quot; CLV &quot; oder &quot; andere &quot; , abhängig vom Typ der Videodisk.</td>
</tr>
<tr class="odd">
<td>Modus</td>
<td>Gibt den aktuellen Modus des Geräts zurück. Alle Geräte können die Werte "nicht bereit", "angehalten", "wieder &quot; Gabe" &quot; und " &quot; &quot; &quot; &quot; &quot; angehalten &quot; " Einige Geräte können die zusätzlichen &quot; Werte für geöffnete, geöffnetes &quot; &quot; &quot; , &quot; aufzeichnen &quot; und &quot; Suchen &quot; zurückgeben.</td>
</tr>
<tr class="even">
<td>Überwachen</td>
<td>Gibt die &quot; Datei &quot; oder die Eingabe zurück &quot; &quot; . Der zurückgegebene Wert gibt die aktuelle Präsentations Quelle an.</td>
</tr>
<tr class="odd">
<td>Monitor-Methode</td>
<td>Gibt &quot; Pre &quot; , &quot; Post &quot; oder &quot; Direct zurück &quot; . Der zurückgegebene Wert gibt die für die Eingabe Überwachung verwendete Methode an.</td>
</tr>
<tr class="even">
<td>ell</td>
<td>Das Element ändert die Flags "Bass", "Helligkeit", "Color", "Contrast", "Gamma", "Schärding", "Tönungs", "Treble" und "Volume", sodass &quot; &quot; &quot; &quot; &quot; &quot; &quot; &quot; &quot; &quot; &quot; &quot; &quot; &quot; &quot; &quot; &quot; &quot; anstelle der aktuellen Einstellung der</td>
</tr>
<tr class="odd">
<td>Nominale Bildrate</td>
<td>Gibt die nominale Frame Rate zurück, die der Datei zugeordnet ist. Die Einheiten werden in Frames pro Sekunde multipliziert mit 1000.</td>
</tr>
<tr class="even">
<td>Nominale Daten Satz Rahmenrate</td>
<td>Gibt die nominale Frame Rate zurück, die mit dem Eingabe Videosignal verknüpft ist. Die Einheiten werden in Frames pro Sekunde multipliziert mit 1000.</td>
</tr>
<tr class="odd">
<td>Anzahl von Audiospuren</td>
<td>Gibt die Anzahl der Audiospuren auf den Medien zurück.</td>
</tr>
<tr class="even">
<td>Anzahl der Spuren</td>
<td>Gibt die Anzahl der Spuren auf den Medien zurück. Die Geräte mcite q und MCIWave geben 1 zurück, wie die meisten VCR-Geräte. Dieses Flag wird vom mcipionr-Gerät nicht unterstützt.</td>
</tr>
<tr class="odd">
<td>Anzahl der Videospuren</td>
<td>Gibt die Anzahl der Videospuren auf den Medien zurück.</td>
</tr>
<tr class="even">
<td>offset</td>
<td>Gibt den Offset einer SMPTE-basierten Datei zurück. Der Offset ist die Startzeit einer SMPTE-basierten Sequenz. Die Zeit wird als <em>hh: mm: SS: FF</em>zurückgegeben, <em>wobei HH</em> Stunden, <em>mm</em> den Wert Minutes, <em>SS</em> den Wert Sekunden und <em>FF</em> ein Rahmen ist.</td>
</tr>
<tr class="odd">
<td>output</td>
<td>Gibt die aktuell festgelegte Ausgabe zurück. Wenn keine Ausgabe festgelegt ist, gibt der zurückgegebene Fehler an, dass ein beliebiges Gerät verwendet werden kann. Bei Digital Video-Geräten werden die Flags "Bass", "Höhen", "Volume", "Helligkeit", "Farbe", " &quot; &quot; Kontrast", "Gamma", " &quot; Schärfe" &quot; &quot; &quot; &quot; oder " &quot; &quot; &quot; &quot; &quot; &quot; &quot; Tönungs" so geändert, &quot; &quot; &quot; &quot; dass Sie nur Dies ist die Standardeinstellung beim Überwachen einer Datei.</td>
</tr>
<tr class="even">
<td>Pausenmodus</td>
<td>Gibt eine Aufzeichnung zurück, &quot; &quot; Wenn das Gerät während der Aufzeichnung angehalten wird. Die Wiedergabe wird zurückgegeben, &quot; &quot; Wenn das Gerät während der Wiedergabe angehalten wird. Sie gibt die Fehler Aktion zurück, die &quot; im aktuellen Modus nicht anwendbar &quot; ist, wenn das Gerät nicht angehalten wurde.</td>
</tr>
<tr class="odd">
<td>Timeout für Pause</td>
<td>Gibt die maximale Dauer eines <a href="pause.md"><strong>Pause</strong></a> -Befehls in Millisekunden zurück.</td>
</tr>
<tr class="even">
<td>Wiedergabe Format</td>
<td>Gibt einen Code zurück, der das Format angibt, in dem das Videoband wiedergegeben wird, wenn es erkennbar ist: &quot; LP &quot; , &quot; EP &quot; , &quot; SP &quot; oder &quot; andere &quot; . Weitere Informationen finden Sie unter Flag für das &quot; Daten Satz Format &quot; .</td>
</tr>
<tr class="odd">
<td>Wiedergabegeschwindigkeit</td>
<td>Gibt einen Wert zurück, der angibt, wie genau die tatsächliche Wiedergabezeit der letzten AVI-Sequenz mit der Ziel Wiedergabezeit übereinstimmt. Der Wert 1000 gibt an, dass die Zielzeit und die tatsächliche zeitgleich sind. Der Wert 2000 gibt z. b. an, dass die AVI-Sequenz zweimal so lange gedauert hat, wie Sie vorhanden sein sollte. Dieses Flag wird nur vom MCIAVI Digital-Video-Treiber erkannt. Es ist nur für die Leistungs Auswertung gedacht. der Rückgabewert ist schwierig zu interpretieren.</td>
</tr>
<tr class="even">
<td>port</td>
<td>Gibt die der Sequenz zugewiesene Nummer des MIDI-Ports zurück.</td>
</tr>
<tr class="odd">
<td>position</td>
<td>Gibt die aktuelle Position zurück. Bei ppqn-Dateien wird die Position in den Zeiger Einheiten des Titels zurückgegeben. Für SMPTE-Dateien wird dieser Wert als <em>hh: mm: SS: FF</em>zurückgegeben, wobei <em>HH</em> Stunden, <em>mm</em> den Wert Minutes, SS den Wert seconds und <em>FF</em> ein Rahmen ist.<br/></td>
</tr>
<tr class="even">
<td>Positions Anfang</td>
<td>Gibt die Position des Starts der verwendbaren Medien zurück.</td>
</tr>
<tr class="odd">
<td>Positions <em>Nummer</em></td>
<td>Gibt die Position des Starts der Spur zurück, die durch <em>Number</em>angegeben wird. Bei ppqn-Dateien wird das Zeitformat in den zeigerpointer-Einheiten zurückgegeben. Für SMPTE-Dateien wird dieser Wert als <em>hh: mm: SS: FF</em>zurückgegeben, wobei <em>HH</em> Stunden, <em>mm</em> den Wert Minutes, <em>SS</em> den Wert seconds und <em>FF</em> ein Rahmen ist. Der mcist-Sequencer gibt 0 (null) zurück. Dieses Flag wird vom mcipionr-Gerät nicht unterstützt. Das MCIWave-Gerät gibt NULL zurück.</td>
</tr>
<tr class="even">
<td>Postroll Dauer</td>
<td>Gibt die Länge von Videotape im aktuellen Zeitformat zurück, das zum Abbremsen des VCR-Transports erforderlich ist, <a href="pause.md"><strong></strong></a> wenn ein Befehl zum <a href="stop.md"><strong>Beenden oder anhalten</strong></a> ausgegeben wird.</td>
</tr>
<tr class="odd">
<td>Einschalten</td>
<td>Gibt " <strong>true</strong> " zurück, wenn die VCR-Stromversorgung eingeschaltet ist.</td>
</tr>
<tr class="even">
<td>Vorabversion</td>
<td>Gibt die Länge von Videotape im aktuellen Zeitformat zurück, das zum stabilisieren der VCR-Ausgabe benötigt wird.</td>
</tr>
<tr class="odd">
<td>ready</td>
<td>Gibt " <strong>true</strong> " zurück, wenn das Gerät bereit ist, einen anderen Befehl zu akzeptieren.</td>
</tr>
<tr class="even">
<td>Daten Satz Format</td>
<td>Gibt einen Code zurück, der das Format angibt, in dem das Videoband aufgezeichnet wird. Die aktuellen Rückgabe Typen sind &quot; LP &quot; , &quot; EP &quot; , &quot; SP &quot; oder &quot; andere &quot; . Diese Formate sind nicht für die VHS spezifisch und können auf alle VCR angewendet werden, die über mehrere auswählbare Aufzeichnungs Formate verfügen. Der &quot; SP &quot; -Typ ist das schnellste, qualitativ hochwertige Aufzeichnungsformat und wird als Standardeinstellung für VCRs mit einem einzelnen Format verwendet.</td>
</tr>
<tr class="odd">
<td>Frame Frequenz aufzeichnen</td>
<td>Gibt die für die Komprimierung verwendete Frame Rate in Frames pro Sekunde multipliziert mit 1000 zurück.</td>
</tr>
<tr class="even">
<td>Verweis <em>Rahmen</em></td>
<td>Gibt die Frame Nummer für das nächste Keyframe-Bild zurück, das dem angegebenen <em>Frame</em>vorangestellt ist.</td>
</tr>
<tr class="odd">
<td>reservierte Größe</td>
<td>Gibt die Größe des reservierten Arbeitsbereichs im aktuellen Zeitformat zurück. Die Größe entspricht der ungefähren Zeit, die für die Wiedergabe der komprimierten Daten aus einem vollständigen Arbeitsbereich benötigt wird. Wenn kein reservierter Speicherplatz vorhanden ist, wird NULL zurückgegeben. Dieses Flag gibt die ungefähre Größe zurück, da der genaue Speicherplatz für komprimierte Daten im allgemeinen erst vorhergesagt werden kann, nachdem die Daten komprimiert wurden.</td>
</tr>
<tr class="even">
<td>richtiges Volume</td>
<td>Gibt das für den rechten Audiokanal festgelegte Volume zurück.</td>
</tr>
<tr class="odd">
<td>samplespersec</td>
<td>Gibt die Anzahl der Stichproben pro Sekunde zurück, die abgespielt oder aufgezeichnet wurden.</td>
</tr>
<tr class="even">
<td>genau suchen</td>
<td>Gibt &quot; ein &quot; oder &quot; aus zurück und gibt an &quot; , ob das &quot; suchgenau- &quot; Flag festgelegt ist.</td>
</tr>
<tr class="odd">
<td>Schärfe</td>
<td>Gibt die aktuelle Schärfe Ebene des Geräts zurück.</td>
</tr>
<tr class="even">
<td>Seite</td>
<td>Gibt 1 oder 2 zurück, um anzugeben, welche Seite der Video Platte geladen wird.</td>
</tr>
<tr class="odd">
<td>Sklaverei</td>
<td>Gibt " &quot; file", "MIDI", "None" oder " &quot; &quot; &quot; &quot; &quot; &quot; SMPTE" &quot; abhängig vom Typ des Synchronisierungs Satzes zurück.</td>
</tr>
<tr class="even">
<td>SMPTE</td>
<td>Gibt den SMPTE-Zeit Code zurück, der der aktuellen Position im Arbeitsbereich zugeordnet ist. Dies ist eine Zeichenfolge mit dem Format <em>DD: DD: DD: DD</em>, wobei jede <em>d</em> eine Ziffer zwischen 0 und 9 bezeichnet. Wenn die Arbeitsbereichs Daten keine Zeitcode-Daten enthalten, gibt dieses Flag 00:00:00:00 zurück.</td>
</tr>
<tr class="odd">
<td>Geschwindigkeit</td>
<td>Gibt die aktuelle Geschwindigkeit des Geräts in Frames pro Sekunde zurück (oder im gleichen Format, das vom Befehl <a href="https://www.bing.com/search?q=<strong>set</strong>"><strong>Set</strong></a> &quot; Speed verwendet wird &quot; ). Der mcipionr-Videodisk-Player unterstützt dieses Flag nicht.</td>
</tr>
<tr class="even">
<td>Startposition</td>
<td>Gibt die Anfangsposition der Medien zurück.</td>
</tr>
<tr class="odd">
<td>immer noch Dateiformat</td>
<td>Gibt das aktuelle Dateiformat für den <a href="capture.md"><strong>Aufzeichnungs</strong></a> Befehl zurück.</td>
</tr>
<tr class="even">
<td>strecken</td>
<td>Gibt <strong>true</strong> zurück, wenn die Streckung aktiviert ist.</td>
</tr>
<tr class="odd">
<td>Lern</td>
<td>Gibt das aktuelle Tempo einer MIDI-Sequenz im aktuellen Zeitformat zurück. Für Dateien mit dem ppqn-Format liegt das Tempo in den Beats pro Minute. Für Dateien mit dem SMPTE-Format wird das Tempo in Frames pro Sekunde angezeigt.</td>
</tr>
<tr class="even">
<td>Zeitformat</td>
<td>Gibt das aktuelle Zeitformat zurück. Weitere Informationen finden Sie unter den Zeitformaten im <a href="set.md"><strong>Set</strong></a> -Befehl.</td>
</tr>
<tr class="odd">
<td>Zeit Modus</td>
<td>Gibt den aktuellen Positions Zeit Modus zurück. Es kann &quot; erkannt &quot; , &quot; Zeitcode &quot; oder Counter sein &quot; &quot; .</td>
</tr>
<tr class="even">
<td>Uhrzeittyp</td>
<td>Gibt die aktuelle Positions Zeit zurück, die verwendet wird: &quot; Zeitcode &quot; oder &quot; counter &quot; .</td>
</tr>
<tr class="odd">
<td>Zeit Code vorhanden</td>
<td>Gibt <strong>true</strong> zurück, wenn der Zeitcode an der aktuellen Position auf dem Band aufgezeichnet wurde. Der Zeitcode muss von der aktuellen Position aus fortfahren. Möglicherweise muss ein VCR wiedergegeben werden, um diese Bedingung zu überprüfen.</td>
</tr>
<tr class="even">
<td>Zeitcode-Datensatz</td>
<td>Gibt " <strong>true</strong> " zurück, wenn die VCR auf "Timecode aufzeichnen" festgelegt ist</td>
</tr>
<tr class="odd">
<td>timecodetyp</td>
<td>Gibt &quot; SMPTE &quot; , &quot; SMPTE Drop &quot; , &quot; other &quot; oder &quot; None zurück &quot; . Beachten Sie, dass die Frames pro Sekunde über den Befehl "Status-Frame Rate" abgerufen werden können &quot; &quot; . die Genauigkeit des Geräts kann vom Befehl " <a href="capability.md"><strong>Capability</strong></a> Seek Accuracy" zurückgegeben werden &quot; &quot; .</td>
</tr>
<tr class="even">
<td>Tönungs</td>
<td>Gibt die aktuelle Video-tint-Ebene zurück.</td>
</tr>
<tr class="odd">
<td>Höhen</td>
<td>Gibt die aktuelle audiotreble-Ebene zurück.</td>
</tr>
<tr class="even">
<td>Nummer des Tuners</td>
<td>Gibt die aktuelle logische-Tuner-Nummer zurück.</td>
</tr>
<tr class="odd">
<td>nicht gespeicherte</td>
<td>Gibt " <strong>true</strong> " zurück, wenn im Arbeitsbereich aufgezeichnete Daten verloren gehen, die als Ergebnis eines Befehls zum <a href="close.md"><strong>Schließen</strong></a>, <a href="load.md"><strong>Laden</strong></a>, <a href="record.md"><strong>aufzeichnen</strong></a>, <a href="reserve.md"><strong>reservieren</strong></a>, <a href="cut.md"><strong>Ausschneiden</strong></a>, <a href="delete.md"><strong>Löschen</strong></a>oder <a href="paste.md"><strong>Einfügen</strong></a> verloren gehen. Gibt andernfalls <strong>false</strong> zurück.</td>
</tr>
<tr class="even">
<td>video</td>
<td>Gibt &quot; ein &quot; oder &quot; aus zurück &quot; , das den vom <a href="setvideo.md"><strong>setvideo</strong></a> -Befehl festgelegten Status widerspiegelt.</td>
</tr>
<tr class="odd">
<td>Farbe des Video Schlüssels</td>
<td>Gibt den Wert für die Schlüsselfarbe zurück.</td>
</tr>
<tr class="even">
<td>Video Schlüssel Index</td>
<td>Gibt den Wert für den Schlüssel Index zurück.</td>
</tr>
<tr class="odd">
<td>Videomonitor</td>
<td>Gibt &quot; &quot; die Ausgabe oder einen der gültigen Quell Eingabetypen zurück. Weitere Informationen finden Sie unter dem Befehl " <a href="setvideo.md"><strong>setvideo</strong></a> &quot; Monitor" &quot; .</td>
</tr>
<tr class="even">
<td>Videomonitor Nummer</td>
<td>Gibt die überwachte Video Nummer des vom Status Videomonitor zurückgegebenen Typs zurück &quot; &quot; . Weitere Informationen finden Sie unter dem Befehl <a href="setvideo.md">setvideo</a> .</td>
</tr>
<tr class="odd">
<td>Videodaten Satz</td>
<td>Gibt &quot; ein &quot; oder &quot; aus &quot; dem aktuellen Zustand zurück, der durch den <a href="setvideo.md"><strong>setvideo</strong></a> -Datensatz festgelegt wird &quot; &quot; .</td>
</tr>
<tr class="even">
<td><em>Nummer</em> der Videodaten Satz Verfolgung</td>
<td>Gibt " <strong>true</strong> " zurück, wenn VCR auf "Video aufzeichnen" festgelegt ist. Wenn keine Nachverfolgung angegeben ist, wird der Standardwert 1 angenommen.</td>
</tr>
<tr class="odd">
<td>Videoquelle</td>
<td>Gibt den Typ der Videoquelle zurück. Weitere Informationen finden Sie unter dem Befehl <a href="setvideo.md"><strong>setvideo</strong></a> .</td>
</tr>
<tr class="even">
<td>Video Quellnummer</td>
<td>Gibt eine Zahl zurück, die der Videoquelle des verwendeten Typs entspricht. Er gibt beispielsweise 2 zurück, wenn die zweite NTSC-Video Quell Eingabe verwendet wird.</td>
</tr>
<tr class="odd">
<td>Videostream</td>
<td>Gibt die aktuelle videostreamnummer zurück.</td>
</tr>
<tr class="even">
<td>Volume</td>
<td>Gibt das durchschnittliche Volume für den linken und den rechten Redner zurück. Dadurch wird ein Fehler zurückgegeben, wenn das Gerät nicht wiedergegeben wurde oder kein Volume festgelegt wurde.</td>
</tr>
<tr class="odd">
<td>Fenster handle</td>
<td>Gibt den ASCII-Dezimalwert für das Fenster Handle in dem nieder wertigen Wort des Rückgabewerts zurück.</td>
</tr>
<tr class="even">
<td>Fenster maximiert</td>
<td>Gibt " <strong>true</strong> " zurück, wenn das Fenster maximiert ist.</td>
</tr>
<tr class="odd">
<td>Fenster minimiert</td>
<td>Gibt <strong>true</strong> zurück, wenn das Fenster minimiert wird.</td>
</tr>
<tr class="even">
<td>Fenster sichtbar</td>
<td>Gibt " <strong>true</strong> " zurück, wenn das Fenster nicht ausgeblendet ist.</td>
</tr>
<tr class="odd">
<td>schreibgeschützt</td>
<td>Gibt <strong>true</strong> zurück, wenn das Gerät erkennt, dass es nicht aufzeichnen kann (d. h., wenn der Schreibschutz auf ON fest liegt). Wenn er aufzeichnen kann, oder wenn er nicht ermitteln kann, ob er aufzeichnen kann (ohne tatsächlich zu schreiben), gibt der Treiber <strong>false</strong>zurück.</td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszflags*
</dt> <dd>

Kann "wait", "notify" oder beides sein. Für Digital Video-und VCR-Geräte kann auch "Test" angegeben werden. Weitere Informationen zu diesen Flags finden Sie [unter warte-, Benachrichtigungs-und testflags](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt Informationen im *lpszreturnstring* -Parameter von [**mciSendString**](/previous-versions//dd757161(v=vs.85))zurück. Die Informationen hängen vom Anforderungstyp ab.

## <a name="remarks"></a>Bemerkungen

Vor dem Ausgeben von Befehlen, die Positionswerte verwenden, sollten Sie das gewünschte Zeitformat mithilfe des [Set](set.md) -Befehls festlegen.

## <a name="examples"></a>Beispiele

Mit dem folgenden Befehl wird der aktuelle Modus des Geräts "mysound" zurückgegeben.

``` syntax
status mysound mode
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

[capability](capability.md)
</dt> <dt>

[einver](capture.md)
</dt> <dt>

[close](close.md)
</dt> <dt>

[Schnitts](cut.md)
</dt> <dt>

[delete](delete.md)
</dt> <dt>

[Laden](load.md)
</dt> <dt>

[pause](pause.md)
</dt> <dt>

[kle](paste.md)
</dt> <dt>

[record](record.md)
</dt> <dt>

[Reserve](reserve.md)
</dt> <dt>

[Speichern](save.md)
</dt> <dt>

[set](set.md)
</dt> <dt>

[setaudiodatei](setaudio.md)
</dt> <dt>

[setvideo](setvideo.md)
</dt> <dt>

[stop](stop.md)
</dt> <dt>

[Rückgängig](undo.md)
</dt> </dl>

 

