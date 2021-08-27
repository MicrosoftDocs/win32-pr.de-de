---
title: status-Befehl
description: Der Befehl status fordert Statusinformationen von einem Gerät an. Dieser Befehl wird von allen Geräten erkannt.
ms.assetid: 39961bd7-866d-450d-9fbf-347a8f508481
keywords:
- Statusbefehl Windows Multimedia
topic_type:
- apiref
api_name:
- status
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd209ed04e51671ce7d9c8a7ae88a79073836c2e
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2021
ms.locfileid: "122626115"
---
# <a name="status-command"></a>status-Befehl

> [!NOTE]
> Voreingenommene Kommunikation Microsoft unterstützt eine vielfältige und inklusionsorientierte Umgebung.  In diesem Dokument gibt es Verweise auf das Wort "slave". Der [Microsoft Style Guide for Bias-Free Communications](https://github.com/MicrosoftDocs/microsoft-style-guide/blob/master/styleguide/bias-free-communication.md) erkennt dies als Ausschlusswort.  Diese Formulierung wird verwendet, da es sich derzeit um die Formulierung handelt, die in den Befehlen verwendet wird. Aus Konsistenzgründen enthält dieses Dokument dieses Wort. Wenn dieses Wort in den Befehlen geändert wird, korrigieren wir dieses Dokument in Übereinstimmung.

Der Befehl status fordert Statusinformationen von einem Gerät an. Dieser Befehl wird von allen Geräten erkannt.

Um diesen Befehl zu senden, rufen Sie die [**mciSendString-Funktion**](/previous-versions//dd757161(v=vs.85)) auf, wobei der *lpszCommand-Parameter* wie folgt festgelegt ist.

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

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Bezeichner eines MCI-Geräts. Dieser Bezeichner oder Alias wird zugewiesen, wenn das Gerät geöffnet wird.

</dd> <dt>

<span id="lpszRequest"></span><span id="lpszrequest"></span><span id="LPSZREQUEST"></span>*lpszRequest*
</dt> <dd>

Flag zum Anfordern von Statusinformationen. In der folgenden Tabelle sind Gerätetypen aufgeführt, die den **Statusbefehl** und die von den einzelnen Typen verwendeten Flags erkennen.



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Gerätetyp</th>
<th>Anforderungsflags</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>cdaudio</td>
<td><ul>
<li>cdaudio type track <em>number</em></li>
<li>Aktuelle Spur</li>
<li>length</li>
<li><em>Längenverfolgungsnummer</em></li>
<li>Medien vorhanden</li>
<li>Modus</li>
<li>Anzahl von Spuren</li>
<li>position</li>
<li>Position track <em>number</em></li>
<li>ready</li>
<li>Startposition</li>
<li>Zeitformat</li>
</ul></td>
</tr>
<tr class="even">
<td>digitalvideo</td>
<td><ul>
<li>Audio</li>
<li>Audioausrichtung</li>
<li>audio bitspersample</li>
<li>Audiounterbrechungen</li>
<li>Audiobytespersec</li>
<li>Audioeingabe</li>
<li>Audiodatensatz</li>
<li>Audioquelle</li>
<li>Audiobeispielepersec</li>
<li>Audiostream</li>
<li>Bass</li>
<li>bitsperpel</li>
<li>Helligkeit</li>
<li>color</li>
<li>Kontrast</li>
<li>Aktuelle Spur</li>
<li>Laufwerk <em>mit</em> Speicherplatz</li>
<li>Dateiabschluss</li>
<li>Dateiformat</li>
<li>Dateimodus</li>
<li>forward</li>
<li>Übersprungene Frames</li>
<li>Gamma</li>
<li>input</li>
<li>Linkes Volume</li>
<li>length</li>
<li><em>Längenverfolgungsnummer</em></li>
<li>Medien vorhanden</li>
<li>Modus</li>
<li>Überwachen</li>
<li>monitor-Methode</li>
<li>Nominale</li>
<li>Nominale Bildfrequenz</li>
<li>Nominale Datensatzbildrate</li>
<li>Anzahl von Spuren</li>
<li>output</li>
<li>Palettenhandle</li>
<li>Pausenmodus</li>
<li>Wiedergabegeschwindigkeit</li>
<li>position</li>
<li>Position track <em>number</em></li>
<li>ready</li>
<li>Aufzeichnen der Bildfrequenz</li>
<li><em>Referenzrahmen</em></li>
<li>Reservierte Größe</li>
<li>Richtiges Volume</li>
<li>Suchen sie genau</li>
<li>Schärfe</li>
<li>Smpte</li>
<li>Geschwindigkeit</li>
<li>Startposition</li>
<li>Dateiformat "still"</li>
<li>Zeitformat</li>
<li>Farbton</li>
<li>Höhen</li>
<li>Ungespeicherten</li>
<li>video</li>
<li>Videoschlüsselindex</li>
<li>Videoschlüsselfarbe</li>
<li>Videodatensatz</li>
<li>Videoquelle</li>
<li>Videoquellnummer</li>
<li>Videostream</li>
<li>Volume</li>
<li>Fensterhand handle</li>
<li>Fenster sichtbar</li>
<li>Minimiertes Fenster</li>
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
<li>Fensterhand handle</li>
</ul></td>
</tr>
<tr class="even">
<td>sequencer</td>
<td><ul>
<li>Aktuelle Spur</li>
<li>Divisionstyp</li>
<li>length</li>
<li>length track <em>number</em> master</li>
<li>Medien vorhanden</li>
<li>Modus</li>
<li>Anzahl der Spuren</li>
<li>offset</li>
<li>port</li>
<li>position</li>
<li><em>Positionsverfolgungsnummer</em></li>
<li>ready</li>
<li>Sklave</li>
<li>Startposition</li>
<li>tempo</li>
<li>Zeitformat</li>
</ul></td>
</tr>
<tr class="odd">
<td>Vcr</td>
<td><ul>
<li>Assemblerdatensatz</li>
<li>Audiomonitor</li>
<li>Audiomonitornummer</li>
<li>Audiodatensatz</li>
<li>Audiodatensatz-Tracknummer <em></em></li>
<li>Audioquelle</li>
<li>Audioquellennummer</li>
<li>Kanal</li>
<li>Channel-Tunernummer <em></em></li>
<li>clock</li>
<li>Clock-ID</li>
<li>Zähler</li>
<li>Indikatorformat</li>
<li>Zählerauflösung</li>
<li>Aktuelle Spur</li>
<li>Bildrate</li>
<li>Index</li>
<li>Index auf</li>
<li>length</li>
<li><em>Längenverfolgungsnummer</em></li>
<li>Medien vorhanden</li>
<li>Medientyp</li>
<li>Modus</li>
<li>Anzahl von Audiospuren</li>
<li>Anzahl der Spuren</li>
<li>Anzahl von Videospuren</li>
<li><em>Pausen-Timeout</em></li>
<li>Wiedergabeformat</li>
<li>position</li>
<li>position start</li>
<li><em>Positionsverfolgungsnummer</em></li>
<li><em>Postrolldauer</em></li>
<li>Einschalten</li>
<li>Dauer der <em>Vorabroll</em></li>
<li>ready</li>
<li>Datensatzformat</li>
<li>Geschwindigkeit</li>
<li>Zeitformat</li>
<li>Zeitmodus</li>
<li>Zeittyp</li>
<li>Vorhandener Zeitcode</li>
<li>Timecodedatensatz</li>
<li>Timecodetyp</li>
<li>Tunernummer</li>
<li>Videomonitor</li>
<li>Videomonitornummer</li>
<li>Videoaufzeichnung</li>
<li>Videoaufzeichnungs-Tracknummer <em></em></li>
<li>Videoquelle</li>
<li>Videoquellennummer</li>
<li>Schreibschutz</li>
</ul></td>
</tr>
<tr class="even">
<td>videodisc</td>
<td><ul>
<li>Aktuelle Spur</li>
<li>Datenträgergröße</li>
<li>forward</li>
<li>length</li>
<li><em>Längenverfolgungsnummer</em></li>
<li>Medien vorhanden</li>
<li>Medientyp</li>
<li>Modus</li>
<li>Anzahl der Spuren</li>
<li>position</li>
<li><em>Positionsverfolgungsnummer</em></li>
<li>ready</li>
<li>Seite</li>
<li>Geschwindigkeit</li>
<li>Startposition</li>
<li>Zeitformat</li>
</ul></td>
</tr>
<tr class="odd">
<td>Waveaudio</td>
<td><ul>
<li>Ausrichtung</li>
<li>bitspersample</li>
<li>bytespersec</li>
<li>channels</li>
<li>Aktuelle Spur</li>
<li>Formattag</li>
<li>input</li>
<li>length</li>
<li><em>Längenverfolgungsnummer</em></li>
<li>Level</li>
<li>Medien vorhanden</li>
<li>Modus</li>
<li>Anzahl der Spuren</li>
<li>output</li>
<li>position</li>
<li><em>Positionsverfolgungsnummer</em></li>
<li>ready</li>
<li>samplespersec</li>
<li>Startposition</li>
<li>Zeitformat</li>
</ul></td>
</tr>
</tbody>
</table>



 

In der folgenden Tabelle sind die Flags, die im **lpszRequest-Parameter** angegeben werden können, und ihre Bedeutungen aufgeführt.



<table>
<colgroup>
<col  />
<col  />
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
<td>Gibt die Blockausrichtung der Daten in Bytes zurück.</td>
</tr>
<tr class="even">
<td>Assemblerdatensatz</td>
<td>Gibt <strong>TRUE zurück,</strong> wenn das Gerät auf die Aufzeichnung im Assemblermodus festgelegt ist.</td>
</tr>
<tr class="odd">
<td>Audio</td>
<td>Gibt &quot; abhängig vom letzten &quot; &quot; &quot; <a href="setaudio.md">setaudio</a> &quot; &quot; &quot; &quot; on- oder off-Befehl ein oder aus zurück. Sie gibt &quot; &quot; zurück, wenn einer oder beide Sprecher aktiviert sind, &quot; &quot; andernfalls .</td>
</tr>
<tr class="even">
<td>Audioausrichtung</td>
<td>Gibt die Ausrichtung von Datenblöcken relativ zum Anfang der Eingabe waveform-audio-Daten zurück.</td>
</tr>
<tr class="odd">
<td>AudiobitsPersample</td>
<td>Gibt die Anzahl der Bits pro Stichprobe zurück, die das Gerät für die Aufzeichnung verwendet. Dieses Flag gilt nur für Geräte, die den &quot; pcm-Algorithmus &quot; unterstützen.</td>
</tr>
<tr class="even">
<td>Audiounterbrechungen</td>
<td>Gibt zurück, wie oft der Audioteil der letzten AVI-Sequenz aufgebrochen ist. Das System zählt eine Audiopause, wenn es versucht, Audiodaten in den Gerätetreiber zu schreiben, und entdeckt, dass der Treiber bereits alle verfügbaren Daten abgespielt hat. Dieses Flag wird nur vom MCIAVI-Treiber für digitale Videos erkannt. Sie ist nur für die Leistungsauswertung bestimmt. Der Rückgabewert ist schwer zu interpretieren.</td>
</tr>
<tr class="odd">
<td>Audiobytespersec</td>
<td>Gibt die durchschnittliche Anzahl von Bytes pro Sekunde zurück, die für die Aufzeichnung verwendet werden.</td>
</tr>
<tr class="even">
<td>Audioeingabe</td>
<td>Gibt die ungefähre sofortige Audioebene des analogen Eingabeaudiosignals zurück. Ein Wert größer als 1000 impliziert Clippingverzerrung. Einige Geräte können diesen Wert nur bei der Audioaufzeichnung zurückgeben. Dem Wert ist kein <a href="set.md">set- oder</a> <a href="setaudio.md">setaudio-Befehl</a> zugeordnet.</td>
</tr>
<tr class="odd">
<td>Audiomonitor</td>
<td>Gibt &quot; die Ausgabe oder einen der &quot; gültigen Quelleingabetypen zurück. Weitere Informationen finden Sie unter dem <strong>Befehl setaudio</strong> &quot; &quot; monitor.</td>
</tr>
<tr class="even">
<td>Audiomonitornummer</td>
<td>Gibt die überwachte Videonummer des Typs zurück, der vom <strong>Statusaudiomonitor</strong> &quot; angegeben &quot; wird. Weitere Informationen finden Sie unter dem <a href="setaudio.md">Befehl setaudio.</a></td>
</tr>
<tr class="odd">
<td>Audiodatensatz</td>
<td>Gibt &quot; ein oder aus &quot; &quot; &quot; zurück, was den durch <strong>setaudio record festgelegten Zustand</strong> &quot; &quot; wiedergibt.</td>
</tr>
<tr class="even">
<td>Audiodatensatz-Tracknummer <em></em></td>
<td>Gibt <strong>TRUE zurück,</strong> wenn der VCR für die Aufzeichnung von Audio festgelegt ist. Wenn keine Spurnummer angegeben wird, wird der Standardwert 1 angenommen.</td>
</tr>
<tr class="odd">
<td>Audiobeispielepersec</td>
<td>Gibt die Anzahl der aufgezeichneten Stichproben pro Sekunde zurück.</td>
</tr>
<tr class="even">
<td>Audioquelle</td>
<td>Gibt die aktuelle Audiodisiererquelle zurück: &quot; &quot; links, &quot; &quot; rechts, &quot; Durchschnitt oder &quot; &quot; &quot; Stereo.</td>
</tr>
<tr class="odd">
<td>Audioquellennummer</td>
<td>Gibt die Audioquellennummer des Typs zurück, der von der <strong>Statusaudioquelle</strong> &quot; zurückgegeben &quot; wird. Weitere Informationen finden Sie unter dem <a href="setaudio.md">Befehl setaudio.</a></td>
</tr>
<tr class="even">
<td>Audiostream</td>
<td>Gibt die aktuelle Audiostreamnummer zurück.</td>
</tr>
<tr class="odd">
<td>Bass</td>
<td>Gibt die aktuelle Audioebene zurück.</td>
</tr>
<tr class="even">
<td>bitsperpel</td>
<td>Gibt die Anzahl der Bits pro Pixel zum Speichern erfasster oder aufgezeichneter Daten zurück.</td>
</tr>
<tr class="odd">
<td>bitspersample</td>
<td>Gibt die Bits pro Stichprobe zurück.</td>
</tr>
<tr class="even">
<td>Helligkeit</td>
<td>Gibt die aktuelle Video-Helligkeitsstufe zurück.</td>
</tr>
<tr class="odd">
<td>bytespersec</td>
<td>Gibt die durchschnittliche Anzahl der pro Sekunde abgespielten oder aufgezeichneten Bytes zurück.</td>
</tr>
<tr class="even">
<td>cdaudio type track <em>number</em></td>
<td>Gibt den Typ der angegebenen Tracknummer zurück. Dies kann Audio &quot; &quot; oder andere &quot; sein.&quot;</td>
</tr>
<tr class="odd">
<td>Kanal</td>
<td>Gibt den ganzzahligen Wert des Kanals zurück, der für den Tuner festgelegt ist.</td>
</tr>
<tr class="even">
<td>Channel-Tunernummer <em></em></td>
<td>Wenn &quot; die Tunernummer angegeben wird, wird der aktuell ausgewählte Kanal auf der &quot; <em></em> logischen Tunernummer zurückgegeben. <em></em> Beachten Sie, dass es mehrere logische Tuner geben kann.</td>
</tr>
<tr class="odd">
<td>channels</td>
<td>Gibt die Anzahl der festgelegten Kanäle zurück (1 für Mono, 2 für Stereo).</td>
</tr>
<tr class="even">
<td>clock</td>
<td>Gibt die externe Zeit zurück. Die Zeit muss eine lange ganze Zahl ohne Vorzeichen sein, die die Gesamtinkrementwerte ausgibt. Weitere Informationen finden Sie unter dem <a href="capability.md">Befehl für die Inkrementrate</a> &quot; der &quot; Funktionsuhr.</td>
</tr>
<tr class="odd">
<td>Clock-ID</td>
<td>Gibt eine eindeutige ganze Zahl zurück, die die Uhr identifiziert.</td>
</tr>
<tr class="even">
<td>color</td>
<td>Gibt die aktuelle Farbebene zurück.</td>
</tr>
<tr class="odd">
<td>Kontrast</td>
<td>Gibt die aktuelle Kontrastebene zurück.</td>
</tr>
<tr class="even">
<td>Zähler</td>
<td>Gibt die Zählerposition im aktuellen Indikatorformat zurück.</td>
</tr>
<tr class="odd">
<td>Indikatorformat</td>
<td>Gibt das aktuelle Zählerformat zurück. Weitere Informationen finden Sie im Befehl <a href="set.md">set</a> &quot; counter &quot; format.</td>
</tr>
<tr class="even">
<td>Zählerauflösung</td>
<td>Gibt &quot; Frames oder Sekunden &quot; &quot; &quot; zurück, die die Auflösung des Indikators angeben. Dies ist nicht identisch mit der Genauigkeit.</td>
</tr>
<tr class="odd">
<td>Aktuelle Spur</td>
<td>Gibt die aktuelle Spur zurück. Der MCISEQ-Sequencer gibt 1 zurück.</td>
</tr>
<tr class="even">
<td>Datenträgergröße</td>
<td>Gibt entweder 8 oder 12 zurück, was die Größe des geladenen Datenträgers in Zoll angibt.</td>
</tr>
<tr class="odd">
<td>Laufwerk <em>für</em> Speicherplatz</td>
<td>Gibt den ungefähren Speicherplatz im aktuellen Zeitformat zurück, <a href="reserve.md"></a> der durch einen Reservebefehl für das angegebene Laufwerk ermittelt werden <em>kann.</em> Das <em>Laufwerk</em> wird in der Regel als ein einzelner Buchstabe oder ein einzelner Buchstabe gefolgt von einem Doppelpunkt (:). Einige Geräte verwenden jedoch möglicherweise einen Pfad.</td>
</tr>
<tr class="even">
<td>Divisionstyp</td>
<td>Gibt einen der folgenden Dateidivisionstypen zurück:
<ul>
<li>PPQN</li>
<li>SMPTE 24-Frame</li>
<li>SMPTE 25-Frame</li>
<li>SMPTE 30-Dropframe</li>
<li>SMPTE 30-Frame</li>
</ul>
<br/> Verwenden Sie diese Informationen, um das Format der FORMATDATEI und die Bedeutung von Geschwindigkeits- und Positionsinformationen zu bestimmen.<br/></td>
</tr>
<tr class="odd">
<td>Dateiabschluss</td>
<td>Gibt den geschätzten Prozentsatz <a href="capture.md"></a> <a href="load.md">zurück,</a>in <a href="copy.md"></a>dem ein Lade-, <a href="save.md">Speicher-,</a>Erfassungs-, Ausschneide-, Kopier-, <a href="delete.md"></a>Lösch-, <a href="paste.md"></a>Einfüge- oder <a href="undo.md">Rückgängig-Vorgang</a> durchgeführt wurde. <a href="cut.md"></a> (Anwendungen können damit einen visuellen Fortschrittsindikator bereitstellen.)</td>
</tr>
<tr class="even">
<td>Dateiformat</td>
<td>Gibt das aktuelle Dateiformat für <a href="record.md">Datensatz- oder</a> <strong>Speicherbefehle</strong> zurück.</td>
</tr>
<tr class="odd">
<td>Dateimodus</td>
<td>Gibt &quot; das &quot; Laden, &quot; &quot; Speichern, Bearbeiten oder im &quot; &quot; &quot; Leerlauf &quot; zurück. Während eines <a href="load.md"><strong>Ladevorgang</strong></a> wird das Laden &quot; von &quot; zurückgegeben. Während <a href="https://www.bing.com/search?q=<strong>save</strong>"><strong>der Speicher-</strong></a> <a href="capture.md"><strong>und Erfassungsvorgänge</strong></a> wird das Speichern &quot; von &quot; zurückgegeben. Während <a href="cut.md"><strong>der Ausschneide-,</strong></a> <a href="delete.md"><strong>Kopier-, Lösch-,</strong></a>Einfüge- oder <a href="undo.md"><strong>Rückgängig-Vorgänge</strong></a> wird die Bearbeitung von <a href="copy.md"><strong></strong></a> <a href="paste.md"><strong></strong></a> &quot; &quot; zurückgegeben.</td>
</tr>
<tr class="even">
<td>Formattag</td>
<td>Gibt das Formattag zurück.</td>
</tr>
<tr class="odd">
<td>forward</td>
<td>Gibt <strong>TRUE zurück,</strong> wenn die Wiedergaberichtung vorwärts ist oder wenn das Gerät nicht abspielt.</td>
</tr>
<tr class="even">
<td>Bildrate</td>
<td>Gibt die Anzahl der Frames pro Sekunde zurück, die das Gerät standardmäßig verwendet. NTSC-Geräte geben 30, PAL 25 und so weiter zurück.</td>
</tr>
<tr class="odd">
<td>Frames übersprungen</td>
<td>Gibt die Anzahl der Frames zurück, die nicht gezeichnet wurden, als die letzte AVI-Sequenz abgespielt wurde. Dieses Flag wird nur vom MCIAVI-Treiber für digitale Videos erkannt. Sie ist nur für die Leistungsauswertung bestimmt. Der Rückgabewert ist schwer zu interpretieren.</td>
</tr>
<tr class="even">
<td>Gamma</td>
<td>Gibt den Wert zurück, der mit <a href="setvideo.md"><strong>setvideo</strong></a> &quot; gamma auf den Wert festgelegt &quot; <em>wurde.</em></td>
</tr>
<tr class="odd">
<td>Index</td>
<td>Gibt die aktuelle Indexanzeige zurück. Weitere Informationen finden Sie im Befehl <a href="set.md"><strong>set</strong></a> &quot; &quot; index.</td>
</tr>
<tr class="even">
<td>Index auf</td>
<td>Gibt <strong>TRUE zurück,</strong> wenn der Index ein on ist.</td>
</tr>
<tr class="odd">
<td>input</td>
<td>Gibt den Eingabesatz zurück. Wenn keines festgelegt ist, gibt der zurückgegebene Fehler an, dass ein beliebiges Gerät verwendet werden kann. Bei Geräten mit digitalem Video ändert das Flag für &quot; &quot; Dasbenen, &quot; &quot; Treble, &quot; &quot; Lautstärke, &quot; &quot; Helligkeit, &quot; &quot; Farbe, &quot; &quot; Kontrast, &quot; &quot; Gamma, &quot; &quot; &quot; &quot; Schärfe oder Tönung so, dass es nur für die Eingabe gilt. Dies ist die Standardeinstellung beim Überwachen der Eingabe.</td>
</tr>
<tr class="even">
<td>Linkes Volume</td>
<td>Gibt das Volume zurück, das für den linken Audiokanal festgelegt wurde.</td>
</tr>
<tr class="odd">
<td>length</td>
<td>Gibt die Gesamtlänge des Mediums im aktuellen Zeitformat zurück. Bei PPQN-Dateien wird die Länge in Musikzeigereinheiten zurückgegeben. Bei SMPTE-Dateien wird sie als <em>hh:mm:ss:ff</em>zurückgegeben, wobei <em>hh</em> stunden, <em>mm minuten,</em> <em>ss</em> Sekunden und <em>ff</em> Frames ist. Bei VCR-Geräten beträgt die Länge 2 Stunden (es sei denn, die Länge wurde mit dem <a href="https://www.bing.com/search?q=<strong>set</strong>"><strong>Set-Befehl explizit</strong></a> geändert).</td>
</tr>
<tr class="even">
<td><em>Längenverfolgungsnummer</em></td>
<td>Gibt die Länge der Spur in Zeit oder Frames zurück, die durch die Zahl <em>angegeben wird.</em> Bei PPQN-Dateien wird die Länge in Musikzeigereinheiten zurückgegeben. Bei SMPTE-Dateien wird sie als <em>hh:mm:ss:ff</em>zurückgegeben, wobei <em>hh</em> stunden, <em>mm minuten,</em> <em>ss</em> Sekunden und <em>ff</em> Frames ist.<br/></td>
</tr>
<tr class="odd">
<td>Level</td>
<td>Gibt den aktuellen PCM-Audiobeispielwert zurück.</td>
</tr>
<tr class="even">
<td>master</td>
<td>Gibt abhängig vom Typ des Synchronisierungssets , none oder &quot; &quot; &quot; &quot; &quot; smpte &quot; zurück.</td>
</tr>
<tr class="odd">
<td>Medien vorhanden</td>
<td>Gibt <strong>TRUE zurück,</strong> wenn das Medium in das Gerät eingefügt wird, andernfalls <strong>FALSE.</strong> Sequencer-, Video overlay-, digital-video- und waveform-audio-Geräte geben <strong>TRUE zurück.</strong></td>
</tr>
<tr class="even">
<td>Medientyp</td>
<td>Gibt den Medientyp zurück. Für VCRS ist &quot; &quot; dies 8mm, &quot; vhs, &quot; &quot; svhs, &quot; &quot; &quot; beta, &quot; &quot; Hi8, &quot; edbeta &quot; oder andere &quot; &quot; . Bei videodiscs ist dies abhängig vom Typ von &quot; &quot; &quot; &quot; &quot; videodisc CAV, CLV oder &quot; andere .</td>
</tr>
<tr class="odd">
<td>Modus</td>
<td>Gibt den aktuellen Modus des Geräts zurück. Alle Geräte können die nicht &quot; bereiten &quot; , &quot; angehaltenen &quot; , &quot; &quot; wiedergabe- und &quot; beendeten Werte &quot; zurückgeben. Einige Geräte können die zusätzlichen offenen &quot; &quot; , &quot; geparkten &quot; , &quot; Aufzeichnungs- &quot; und &quot; Suchwerte &quot; zurückgeben.</td>
</tr>
<tr class="even">
<td>Überwachen</td>
<td>Gibt die &quot; Datei oder die Eingabe &quot; &quot; &quot; zurück. Der zurückgegebene Wert gibt die aktuelle Präsentationsquelle an.</td>
</tr>
<tr class="odd">
<td>monitor-Methode</td>
<td>Gibt &quot; &quot; pre, &quot; post oder direct &quot; &quot; &quot; zurück. Der zurückgegebene Wert gibt die Methode an, die für die Eingabeüberwachung verwendet wird.</td>
</tr>
<tr class="even">
<td>Nominale</td>
<td>Das Element ändert die Flags für Denk-, &quot; &quot; &quot; &quot; &quot; &quot; &quot; &quot; &quot; &quot; &quot; &quot; &quot; &quot; &quot; Helligkeits-, Farb-, Kontrast-, Gamma-, Schärfe-, Tönungs-, Treble- und &quot; Lautstärkeflags, &quot; &quot; um den nominalen Wert anstelle der aktuellen Einstellung zurück zu geben.</td>
</tr>
<tr class="odd">
<td>nominale Bildfrequenz</td>
<td>Gibt die nominale Framerate zurück, die der Datei zugeordnet ist. Die Einheiten werden in Frames pro Sekunde multipliziert mit 1000.</td>
</tr>
<tr class="even">
<td>Nominale Bildfrequenz des Datensatzes</td>
<td>Gibt die nominale Bildfrequenz zurück, die dem Eingabevideosignal zugeordnet ist. Die Einheiten werden in Frames pro Sekunde multipliziert mit 1000.</td>
</tr>
<tr class="odd">
<td>Anzahl von Audiospuren</td>
<td>Gibt die Anzahl der Audiospuren auf dem Medium zurück.</td>
</tr>
<tr class="even">
<td>Anzahl der Spuren</td>
<td>Gibt die Anzahl der Spuren auf dem Medium zurück. Die MCISEQ- und MCIWAVE-Geräte geben wie die meisten VCR-Geräte 1 zurück. Dieses Flag wird vom MCIPIONR-Gerät nicht unterstützt.</td>
</tr>
<tr class="odd">
<td>Anzahl von Videospuren</td>
<td>Gibt die Anzahl der Videospuren auf den Medien zurück.</td>
</tr>
<tr class="even">
<td>offset</td>
<td>Gibt den Offset einer SMPTE-basierten Datei zurück. Der Offset ist die Startzeit einer SMPTE-basierten Sequenz. Die Zeit wird als <em>hh:mm:ss:ff</em>zurückgegeben, wobei <em>hh</em> stunden, <em>mm</em> minuten, <em>ss</em> sekunden und <em>ff</em> Frames ist.</td>
</tr>
<tr class="odd">
<td>output</td>
<td>Gibt die aktuell festgelegte Ausgabe zurück. Wenn keine Ausgabe festgelegt ist, gibt der zurückgegebene Fehler an, dass jedes Gerät verwendet werden kann. Ändert für Digitalvideogeräte das &quot; &quot; &quot; Farbflag , Treble &quot; , &quot; &quot; &quot; &quot; Volume, &quot; &quot; Helligkeit, Farbe, &quot; &quot; Kontrast, &quot; &quot; Gamma, &quot; Schärfe oder &quot; &quot; Tönung, &quot; sodass es nur für die Ausgabe gilt. Dies ist die Standardeinstellung beim Überwachen einer Datei.</td>
</tr>
<tr class="even">
<td>Pausenmodus</td>
<td>Gibt &quot; die Aufzeichnung &quot; zurück, wenn das Gerät während der Aufzeichnung angehalten wird. Die &quot; Wiedergabe &quot; wird zurückgegeben, wenn das Gerät während der Wiedergabe angehalten wird. Der Fehler &quot; Aktion kann im aktuellen Modus nicht angewendet &quot; werden, wenn das Gerät nicht angehalten ist, wird zurückgegeben.</td>
</tr>
<tr class="odd">
<td>Timeout anhalten</td>
<td>Gibt die maximale Dauer eines <a href="pause.md"><strong>Pausenbefehls</strong></a> in Millisekunden zurück.</td>
</tr>
<tr class="even">
<td>Wiedergabeformat</td>
<td>Gibt einen Code zurück, der das Format angibt, in dem die Videoaufzeichnung wiedergegeben wird, sofern erkennbar: &quot; lp , ep , sp oder andere &quot; &quot; &quot; &quot; &quot; &quot; &quot; . Weitere Informationen finden Sie unter &quot; Dem &quot; Datensatzformatflag.</td>
</tr>
<tr class="odd">
<td>Wiedergabegeschwindigkeit</td>
<td>Gibt einen Wert zurück, der angibt, wie genau die tatsächliche Wiedergabezeit der letzten AVI-Sequenz mit der Zielwiedergabezeit übereinstimmt. Der Wert 1000 gibt an, dass die Zielzeit und die tatsächliche Zeit identisch waren. Der Wert 2000 würde z. B. angeben, dass die WIEDERGABE der AVI-Sequenz doppelt so lange gedauert hat, wie sie sollte. Dieses Flag wird nur vom MCIAVI-Treiber für digitale Videos erkannt. Sie ist nur für die Leistungsauswertung vorgesehen. Der Rückgabewert ist schwer zu interpretieren.</td>
</tr>
<tr class="even">
<td>port</td>
<td>Gibt die der Sequenz zugewiesene PORTS-Nummer zurück.</td>
</tr>
<tr class="odd">
<td>position</td>
<td>Gibt die aktuelle Position zurück. Bei PPQN-Dateien wird die Position in Songzeigereinheiten zurückgegeben. Für SMPTE-Dateien wird sie als <em>hh:mm:ss:ff</em>zurückgegeben, wobei <em>hh</em> stunden, <em>mm</em> minuten, ss sekunden und <em>ff</em> Frames ist.<br/></td>
</tr>
<tr class="even">
<td>position start</td>
<td>Gibt die Position des Anfangs der verwendbaren Medien zurück.</td>
</tr>
<tr class="odd">
<td>Position track <em>number</em></td>
<td>Gibt die Position des Beginns der <em>Durchnummer</em>angegebenen Spur zurück. Bei PPQN-Dateien wird das Zeitformat in Einheiten für Songzeiger zurückgegeben. Für SMPTE-Dateien wird sie als <em>hh:mm:ss:ff</em>zurückgegeben, wobei <em>hh</em> stunden, <em>mm</em> minuten, <em>ss</em> sekunden und <em>ff</em> Frames ist. Der MCISEQ-Sequencer gibt 0 (null) zurück. Dieses Flag wird vom MCIPIONR-Gerät nicht unterstützt. Das MCIWAVE-Gerät gibt 0 (null) zurück.</td>
</tr>
<tr class="even">
<td>Dauer der Postrolls</td>
<td>Gibt die Länge des Videobands im aktuellen Zeitformat zurück, die erforderlich ist, um den VCR-Transport zu unterbrechen, wenn ein Befehl zum <a href="stop.md"><strong>Beenden</strong></a> oder <a href="pause.md"><strong>Anhalten</strong></a> ausgegeben wird.</td>
</tr>
<tr class="odd">
<td>Einschalten</td>
<td>Gibt <strong>TRUE</strong> zurück, wenn die Stromversorgung des VCR eingeschaltet ist.</td>
</tr>
<tr class="even">
<td>Dauer des Vorabrolls</td>
<td>Gibt die Länge der Videoaufzeichnung im aktuellen Zeitformat zurück, die erforderlich ist, um die VCR-Ausgabe zu stabilieren.</td>
</tr>
<tr class="odd">
<td>ready</td>
<td>Gibt <strong>TRUE</strong> zurück, wenn das Gerät bereit ist, einen anderen Befehl zu akzeptieren.</td>
</tr>
<tr class="even">
<td>Datensatzformat</td>
<td>Gibt einen Code zurück, der das Format angibt, in dem die Videoaufzeichnung aufgezeichnet wird. Die aktuellen Rückgabetypen sind &quot; &quot; lp, &quot; &quot; ep, &quot; sp oder andere &quot; &quot; &quot; . Diese Formate sind nicht VHS-spezifisch und können auf jeden VCR angewendet werden, der über mehrere auswählbare Aufzeichnungsformate verfügt. Der &quot; Typ sp ist das schnellste &quot; Aufzeichnungsformat mit der höchsten Qualität und wird standardmäßig für VCRs im Einzelformat verwendet.</td>
</tr>
<tr class="odd">
<td>Aufzeichnen der Bildfrequenz</td>
<td>Gibt die Bildfrequenz in Frames pro Sekunde multipliziert mit 1000 zurück, die für die Komprimierung verwendet wird.</td>
</tr>
<tr class="even">
<td><em>Referenzframe</em></td>
<td>Gibt die Framenummer für das nächste Keyframebild zurück, das dem angegebenen <em>Frame</em>vorangestellt ist.</td>
</tr>
<tr class="odd">
<td>Reservierte Größe</td>
<td>Gibt die Größe des reservierten Arbeitsbereichs im aktuellen Zeitformat zurück. Die Größe entspricht der ungefähren Zeit, die zum Wiedergeben der komprimierten Daten aus einem vollständigen Arbeitsbereich dauern würde. Wenn kein reservierter Speicherplatz vorhanden ist, wird 0 zurückgegeben. Dieses Flag gibt die ungefähre Größe zurück, da der genaue Speicherplatz für komprimierte Daten im Allgemeinen erst vorhergesagt werden kann, nachdem die Daten komprimiert wurden.</td>
</tr>
<tr class="even">
<td>Richtiges Volume</td>
<td>Gibt den Volumesatz für den richtigen Audiokanal zurück.</td>
</tr>
<tr class="odd">
<td>samplespersec</td>
<td>Gibt die Anzahl der wiedergegebenen oder aufgezeichneten Stichproben pro Sekunde zurück.</td>
</tr>
<tr class="even">
<td>Suchen sie genau</td>
<td>Gibt &quot; ein oder aus &quot; &quot; &quot; zurück, das angibt, ob das &quot; &quot; Suchflag genau festgelegt ist.</td>
</tr>
<tr class="odd">
<td>Schärfe</td>
<td>Gibt den aktuellen Schärfegrad des Geräts zurück.</td>
</tr>
<tr class="even">
<td>Seite</td>
<td>Gibt 1 oder 2 zurück, um anzugeben, welche Seite der videodisc geladen wird.</td>
</tr>
<tr class="odd">
<td>Sklave</td>
<td>Gibt &quot; abhängig vom Typ des Synchronisierungssatzes die Datei , die Datei , die Datei &quot; , keine oder &quot; &quot; &quot; &quot; &quot; Smpte &quot; zurück.</td>
</tr>
<tr class="even">
<td>Smpte</td>
<td>Gibt den SMPTE-Zeitcode zurück, der der aktuellen Position im Arbeitsbereich zugeordnet ist. Dies ist eine Zeichenfolge mit dem Format <em>dd:dd:dd:dd,</em>wobei jeder <em>d</em> eine Ziffer von 0 bis 9 kennzeichnet. Wenn die Arbeitsbereichsdaten keine Timecodedaten enthalten, gibt dieses Flag 00:00:00:00 zurück.</td>
</tr>
<tr class="odd">
<td>Geschwindigkeit</td>
<td>Gibt die aktuelle Geschwindigkeit des Geräts in Frames pro Sekunde zurück (oder in demselben Format, das vom Befehl <a href="https://www.bing.com/search?q=<strong>set</strong>"><strong>"set</strong></a> speed" verwendet &quot; &quot; wird). Der MCIPIONR-Videodisc-Player unterstützt dieses Flag nicht.</td>
</tr>
<tr class="even">
<td>Startposition</td>
<td>Gibt die Anfangsposition des Mediums zurück.</td>
</tr>
<tr class="odd">
<td>Dateiformat "still"</td>
<td>Gibt das aktuelle Dateiformat für den <a href="capture.md"><strong>Aufzeichnungsbefehl</strong></a> zurück.</td>
</tr>
<tr class="even">
<td>strecken</td>
<td>Gibt <strong>TRUE</strong> zurück, wenn Stretching aktiviert ist.</td>
</tr>
<tr class="odd">
<td>tempo</td>
<td>Gibt das aktuelle Tempo einer CAB-Sequenz im aktuellen Zeitformat zurück. Bei Dateien im PPQN-Format liegt das Tempo in Takten pro Minute. Bei Dateien mit dem SMPTE-Format liegt das Tempo in Frames pro Sekunde.</td>
</tr>
<tr class="even">
<td>Zeitformat</td>
<td>Gibt das aktuelle Zeitformat zurück. Weitere Informationen finden Sie unter den Zeitformaten im <a href="set.md"><strong>Set-Befehl.</strong></a></td>
</tr>
<tr class="odd">
<td>Zeitmodus</td>
<td>Gibt den aktuellen Positionszeitmodus zurück. Es kann &quot; , timecode oder counter erkannt &quot; &quot; &quot; &quot; &quot; werden.</td>
</tr>
<tr class="even">
<td>zeittyp</td>
<td>Gibt die aktuelle Positionszeit zurück, die verwendet wird: &quot; timecode &quot; oder counter &quot; &quot; .</td>
</tr>
<tr class="odd">
<td>timecode present</td>
<td>Gibt <strong>TRUE</strong> zurück, wenn der Zeitcode an der aktuellen Position auf dem Band aufgezeichnet wurde. Der Zeitcode muss von der aktuellen Position entfernt werden. Möglicherweise muss ein VCR abgespielt werden, um diese Bedingung zu überprüfen.</td>
</tr>
<tr class="even">
<td>Timecodedatensatz</td>
<td>Gibt <strong>TRUE zurück,</strong> wenn der VCR auf den Zeitcode aufzeichnen festgelegt ist.</td>
</tr>
<tr class="odd">
<td>Timecodetyp</td>
<td>Gibt &quot; smpte, &quot; &quot; smpte &quot; drop, other &quot; oder none &quot; &quot; &quot; zurück. Beachten Sie, dass die Frames pro Sekunde über den Befehl status frame rate ermittelt werden können, und die Genauigkeit des Geräts kann durch den Befehl &quot; &quot; <a href="capability.md"><strong>capability</strong></a> &quot; seek accuracy zurückgegeben &quot; werden.</td>
</tr>
<tr class="even">
<td>Farbton</td>
<td>Gibt die aktuelle Videotonebene zurück.</td>
</tr>
<tr class="odd">
<td>Höhen</td>
<td>Gibt den aktuellen Audio-Treble-Level zurück.</td>
</tr>
<tr class="even">
<td>Tunernummer</td>
<td>Gibt die aktuelle logische Tunernummer zurück.</td>
</tr>
<tr class="odd">
<td>Ungespeicherten</td>
<td>Gibt <strong>TRUE zurück,</strong> wenn im Arbeitsbereich aufgezeichnete Daten gespeichert sind, die möglicherweise durch <a href="delete.md"><strong></strong></a>einen Befehl zum <a href="close.md"><strong>Schließen,</strong></a> <a href="load.md"><strong>Laden,</strong></a> <a href="record.md"><strong>Aufzeichnen,</strong></a> <a href="reserve.md"><strong>Reservieren,</strong></a>Ausschneiden, <a href="cut.md"><strong></strong></a>Löschen oder Einfügen <a href="paste.md"><strong>verloren</strong></a> gehen. Gibt <strong>andernfalls FALSE</strong> zurück.</td>
</tr>
<tr class="even">
<td>video</td>
<td>Gibt &quot; ein oder aus zurück und gibt den durch den &quot; &quot; &quot; <a href="setvideo.md"><strong>Setvideo-Befehl festgelegten Zustand</strong></a> wieder.</td>
</tr>
<tr class="odd">
<td>Videoschlüsselfarbe</td>
<td>Gibt den Wert für die Schlüsselfarbe zurück.</td>
</tr>
<tr class="even">
<td>Videoschlüsselindex</td>
<td>Gibt den Wert für den Schlüsselindex zurück.</td>
</tr>
<tr class="odd">
<td>Videomonitor</td>
<td>Gibt &quot; die Ausgabe oder einen der &quot; gültigen Quelleingabetypen zurück. Weitere Informationen finden Sie im Befehl <a href="setvideo.md"><strong>setvideo</strong></a> &quot; &quot; monitor.</td>
</tr>
<tr class="even">
<td>Videomonitornummer</td>
<td>Gibt die überwachte Videonummer des Typs zurück, der vom &quot; Statusvideomonitor zurückgegeben &quot; wird. Weitere Informationen finden Sie unter dem <a href="setvideo.md">Befehl setvideo.</a></td>
</tr>
<tr class="odd">
<td>Videoaufzeichnung</td>
<td>Gibt &quot; ein oder aus zurück und gibt den aktuellen Zustand &quot; &quot; &quot; wieder, der durch <a href="setvideo.md"><strong>setvideo</strong></a> &quot; record festgelegt &quot; wurde.</td>
</tr>
<tr class="even">
<td>Videoaufzeichnungs-Tracknummer <em></em></td>
<td>Gibt <strong>TRUE zurück,</strong> wenn der VCR für die Aufzeichnung von Videos festgelegt ist. Wenn keine Spurnummer angegeben wird, wird der Standardwert 1 angenommen.</td>
</tr>
<tr class="odd">
<td>Videoquelle</td>
<td>Gibt den Videoquellentyp zurück. Weitere Informationen finden Sie unter dem <a href="setvideo.md"><strong>Befehl setvideo.</strong></a></td>
</tr>
<tr class="even">
<td>Videoquellennummer</td>
<td>Gibt eine Zahl zurück, die der Videoquelle des zu verwendenden Typs entspricht. Beispielsweise wird 2 zurückgegeben, wenn die zweite NTSC-Videoquelleneingabe verwendet wird.</td>
</tr>
<tr class="odd">
<td>Videostream</td>
<td>Gibt die aktuelle Videostreamnummer zurück.</td>
</tr>
<tr class="even">
<td>Volume</td>
<td>Gibt das durchschnittliche Volumen an den linken und rechten Lautsprecher zurück. Dadurch wird ein Fehler zurückgegeben, wenn das Gerät nicht abgespielt oder das Volume nicht festgelegt wurde.</td>
</tr>
<tr class="odd">
<td>Fensterhand handle</td>
<td>Gibt den ASCII-Dezimalwert für das Fensterhand handle im niedrigen Wort des Rückgabewerts zurück.</td>
</tr>
<tr class="even">
<td>Fenster maximiert</td>
<td>Gibt <strong>TRUE zurück,</strong> wenn das Fenster maximiert ist.</td>
</tr>
<tr class="odd">
<td>Minimiertes Fenster</td>
<td>Gibt <strong>TRUE zurück,</strong> wenn das Fenster minimiert ist.</td>
</tr>
<tr class="even">
<td>Fenster sichtbar</td>
<td>Gibt <strong>TRUE zurück,</strong> wenn das Fenster nicht ausgeblendet ist.</td>
</tr>
<tr class="odd">
<td>Schreibschutz</td>
<td>Gibt <strong>TRUE zurück,</strong> wenn das Gerät erkennt, dass es nicht aufzeichnen kann (d. h., wenn der Schreibschutz ein on ist). Wenn er aufzeichnen kann oder nicht bestimmen kann, ob er aufzeichnen kann (ohne tatsächlich zu schreiben), gibt der Treiber <strong>FALSE zurück.</strong></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Kann "wait", "notify" oder beides sein. Für digital-video- und VCR-Geräte kann auch "test" angegeben werden. Weitere Informationen zu diesen Flags finden Sie unter [Die Warte-, Benachrichtigungs- und Testflags](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt Informationen im *lpszReturnString-Parameter* von [**mciSendString zurück.**](/previous-versions//dd757161(v=vs.85)) Die Informationen hängen vom Anforderungstyp ab.

## <a name="remarks"></a>Hinweise

Vor dem Ausführen von Befehlen, die Positionswerte verwenden, sollten Sie das gewünschte Zeitformat mit dem [Set-Befehl](set.md) festlegen.

## <a name="examples"></a>Beispiele

Der folgende Befehl gibt den aktuellen Modus des "mysound"-Geräts zurück.

``` syntax
status mysound mode
```

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>       |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[MCI-Befehlszeichenfolgen](mci-command-strings.md)
</dt> <dt>

[capability](capability.md)
</dt> <dt>

[Erfassen](capture.md)
</dt> <dt>

[close](close.md)
</dt> <dt>

[Schneiden](cut.md)
</dt> <dt>

[delete](delete.md)
</dt> <dt>

[Laden](load.md)
</dt> <dt>

[pause](pause.md)
</dt> <dt>

[Einfügen](paste.md)
</dt> <dt>

[record](record.md)
</dt> <dt>

[Reserve](reserve.md)
</dt> <dt>

[Speichern](save.md)
</dt> <dt>

[set](set.md)
</dt> <dt>

[Setaudio](setaudio.md)
</dt> <dt>

[setvideo](setvideo.md)
</dt> <dt>

[stop](stop.md)
</dt> <dt>

[Rückgängig](undo.md)
</dt> </dl>

 

