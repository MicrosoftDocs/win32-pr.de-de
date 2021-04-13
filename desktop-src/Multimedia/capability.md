---
title: Funktionsbefehl
description: Der Funktionsbefehl fordert Informationen zu einer bestimmten Funktion eines Geräts an. Dieser Befehl wird von allen MCI-Geräten erkannt.
ms.assetid: 1b470473-0de6-41ba-9f6e-41f0b13ceaeb
keywords:
- Funktionsbefehl Windows-Multimedia
topic_type:
- apiref
api_name:
- capability
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a6ac87b98fb8d748a5baf2665cc5a63230b6a98
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475708"
---
# <a name="capability-command"></a>Funktionsbefehl

Der Funktionsbefehl fordert Informationen zu einer bestimmten Funktion eines Geräts an. Dieser Befehl wird von allen MCI-Geräten erkannt.

Um diesen Befehl zu senden, wenden Sie die [**mciSendString**](/previous-versions//dd757161(v=vs.85)) -Funktion mit dem festgelegten *lpszcommand* -Parameter wie folgt an.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("capability %s %s %s"), 
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

Flag, das eine Geräte Funktion identifiziert. In der folgenden Tabelle sind die Gerätetypen aufgeführt **, die den Funktionsbefehl und** die von den einzelnen Typen verwendeten Flags erkennen:



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Wert</th>
<th>Typ</th>
<th>Typ</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>CDAudio</td>
<td><ul>
<li>kann Auswerfen</li>
<li>kann abspielen</li>
<li>kann aufzeichnen</li>
<li>kann speichern</li>
<li>Verbund Gerät</li>
</ul></td>
<td><ul>
<li>Gerätetyp</li>
<li>hat Audiodaten</li>
<li>hat Video</li>
<li>verwendet Dateien</li>
</ul></td>
</tr>
<tr class="even">
<td>Digitalvideo</td>
<td><ul>
<li>kann Auswerfen</li>
<li>Einfrieren möglich</li>
<li>Sperre möglich</li>
<li>kann abspielen</li>
<li>kann aufzeichnen</li>
<li>kann umkehren</li>
<li>kann speichern</li>
<li>kann gestreckt werden</li>
<li>kann Eingaben ausdehnen</li>
<li>kann testen</li>
</ul></td>
<td><ul>
<li>Verbund Gerät</li>
<li>Gerätetyp</li>
<li>hat Audiodaten</li>
<li>hat noch</li>
<li>hat Video</li>
<li>maximale Wiedergabe Rate</li>
<li>minimale Wiedergabe Rate</li>
<li>verwendet Dateien</li>
<li>verwendet Paletten</li>
<li>Windows</li>
</ul></td>
</tr>
<tr class="odd">
<td>overlay</td>
<td><ul>
<li>kann Auswerfen</li>
<li>Einfrieren möglich</li>
<li>kann abspielen</li>
<li>kann aufzeichnen</li>
<li>kann speichern</li>
<li>kann gestreckt werden</li>
</ul></td>
<td><ul>
<li>Verbund Gerät</li>
<li>Gerätetyp</li>
<li>hat Audiodaten</li>
<li>hat Video</li>
<li>verwendet Dateien</li>
<li>Windows</li>
</ul></td>
</tr>
<tr class="even">
<td>sequencer</td>
<td><ul>
<li>kann Auswerfen</li>
<li>kann abspielen</li>
<li>kann aufzeichnen</li>
<li>kann speichern</li>
<li>Verbund Gerät</li>
</ul></td>
<td><ul>
<li>Gerätetyp</li>
<li>hat Audiodaten</li>
<li>hat Video</li>
<li>verwendet Dateien</li>
</ul></td>
</tr>
<tr class="odd">
<td>VCR</td>
<td><ul>
<li>kann die Länge erkennen</li>
<li>kann Auswerfen</li>
<li>Einfrieren möglich</li>
<li>kann Quellen überwachen</li>
<li>kann abspielen</li>
<li>kann vorab</li>
<li>Vorschau möglich</li>
<li>kann aufzeichnen</li>
<li>kann umkehren</li>
<li>kann speichern</li>
<li>kann testen</li>
</ul></td>
<td><ul>
<li>Takt Inkrement-Rate</li>
<li>Verbund Gerät</li>
<li>Gerätetyp</li>
<li>hat Audiodaten</li>
<li>hat Uhr</li>
<li>hat Zeitcode</li>
<li>hat Video</li>
<li>Anzahl der Markierungen</li>
<li>Genauigkeit suchen</li>
<li>verwendet Dateien</li>
</ul></td>
</tr>
<tr class="even">
<td>Videodisk</td>
<td><ul>
<li>kann Auswerfen</li>
<li>kann abspielen</li>
<li>kann aufzeichnen</li>
<li>kann umkehren</li>
<li>kann speichern</li>
<li>CAV</li>
<li>CLV</li>
<li>Verbund Gerät</li>
</ul></td>
<td><ul>
<li>Gerätetyp</li>
<li>schnelle Wiedergabe Rate</li>
<li>hat Audiodaten</li>
<li>hat Video</li>
<li>normale Wiedergabe Rate</li>
<li>Langsame Wiedergabe Rate</li>
<li>verwendet Dateien</li>
</ul></td>
</tr>
<tr class="odd">
<td>waveaudiodatei</td>
<td><ul>
<li>kann Auswerfen</li>
<li>kann abspielen</li>
<li>kann aufzeichnen</li>
<li>kann speichern</li>
<li>Verbund Gerät</li>
<li>Gerätetyp</li>
</ul></td>
<td><ul>
<li>hat Audiodaten</li>
<li>hat Video</li>
<li>inputs</li>
<li>outputs</li>
<li>verwendet Dateien</li>
</ul></td>
</tr>
</tbody>
</table>



 

In der folgenden Tabelle werden die Flags aufgelistet, die im *lpszrequest* -Parameter und deren Bedeutung angegeben werden können:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Flags</th>
<th>Bedeutung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>kann die Länge erkennen</td>
<td>Gibt " <strong>true</strong> " zurück, wenn das Gerät die Länge des Mediums erkennen kann.</td>
</tr>
<tr class="even">
<td>kann Auswerfen</td>
<td>Gibt " <strong>true</strong> " zurück, wenn das Gerät das Medium auswerfen kann.</td>
</tr>
<tr class="odd">
<td>Einfrieren möglich</td>
<td>Gibt " <strong>true</strong> " zurück, wenn das Gerät Daten im Frame Puffer Einfrieren kann.</td>
</tr>
<tr class="even">
<td>Sperre möglich</td>
<td>Gibt " <strong>true</strong> " zurück, wenn das Gerät Daten Sperren kann.</td>
</tr>
<tr class="odd">
<td>kann Quellen überwachen</td>
<td>Gibt " <strong>true</strong> " zurück, wenn das Gerät unabhängig von der aktuellen Eingabeauswahl eine Eingabe (Quelle) an die überwachte Ausgabe übergeben kann.</td>
</tr>
<tr class="even">
<td>kann abspielen</td>
<td>Gibt <strong>true</strong> zurück, wenn das Gerät wiedergegeben werden kann.</td>
</tr>
<tr class="odd">
<td>kann vorab</td>
<td>Gibt <strong>true</strong> zurück, wenn das Gerät das &quot; ein Vorlauf ausgeführt- &quot; Flag <a href="cue.md"></a> mit dem Hinweis Befehl unterstützt.</td>
</tr>
<tr class="even">
<td>Vorschau möglich</td>
<td>Gibt <strong>true</strong> zurück, wenn das Gerät Vorschau Versionen unterstützt.</td>
</tr>
<tr class="odd">
<td>kann aufzeichnen</td>
<td>Gibt <strong>true</strong> zurück, wenn das Gerät eine Aufzeichnung unterstützt.</td>
</tr>
<tr class="even">
<td>kann umkehren</td>
<td>Gibt <strong>true</strong> zurück, wenn das Gerät in umgekehrter Richtung wiedergegeben werden kann</td>
</tr>
<tr class="odd">
<td>kann speichern</td>
<td>Gibt " <strong>true</strong> " zurück, wenn das Gerät Daten speichern kann.</td>
</tr>
<tr class="even">
<td>kann gestreckt werden</td>
<td>Gibt " <strong>true</strong> " zurück, wenn das Gerät Frames zum Ausfüllen eines angegebenen Anzeige Rechtecks erweitern kann.</td>
</tr>
<tr class="odd">
<td>kann Eingaben ausdehnen</td>
<td>Gibt " <strong>true</strong> " zurück, wenn die Größe eines Bilds beim Digitalisieren des Geräts im Frame Puffer geändert werden kann.</td>
</tr>
<tr class="even">
<td>kann testen</td>
<td>Gibt <strong>true</strong> zurück, wenn das Gerät das Test Schlüsselwort erkennt.</td>
</tr>
<tr class="odd">
<td>CAV</td>
<td>In Kombination mit anderen Elementen gibt dieses Flag an, dass die Rückgabe Informationen für Videodisks im CAV-Format gelten. Dies ist die Standardeinstellung, wenn keine Video Disk eingefügt wird.</td>
</tr>
<tr class="even">
<td>Takt Inkrement-Rate</td>
<td>Gibt die Anzahl der untergeordneten Bereiche zurück, die die externe Uhr pro Sekunde unterstützt. Wenn die externe Uhr eine millisekundenuhr ist, ist der Rückgabewert 1000. Wenn der Rückgabewert 0 (null) ist, wird keine Uhr unterstützt.</td>
</tr>
<tr class="odd">
<td>clv</td>
<td>In Kombination mit anderen Elementen gibt dieses Flag an, dass die Rückgabe Informationen auf Videodisks im CLV-Format zutreffen.</td>
</tr>
<tr class="even">
<td>Verbund Gerät</td>
<td>Gibt <strong>true</strong> zurück, wenn das Gerät einen Elementnamen (Dateiname) unterstützt.</td>
</tr>
<tr class="odd">
<td>Gerätetyp</td>
<td>Gibt einen Gerätetyp Namen zurück, bei dem es sich um einen der folgenden Typen handeln kann:
<ul>
<li>CDAudio</li>
<li>Hütte</li>
<li>Digitalvideo</li>
<li>andere</li>
<li>overlay</li>
<li>Scanner</li>
<li>sequencer</li>
<li>VCR</li>
<li>Videodisk</li>
<li>waveaudiodatei</li>
</ul></td>
</tr>
<tr class="even">
<td>schnelle Wiedergabe Rate</td>
<td>Gibt die schnelle Wiedergabe Rate in Frames pro Sekunde zurück, oder 0 (null), wenn das Gerät nicht schnell wiedergegeben werden kann.</td>
</tr>
<tr class="odd">
<td>hat Audiodaten</td>
<td>Gibt " <strong>true</strong> " zurück, wenn das Gerät Audiowiedergabe unterstützt.</td>
</tr>
<tr class="even">
<td>hat Uhr</td>
<td>Gibt " <strong>true</strong> " zurück, wenn das Gerät eine Uhr hat.</td>
</tr>
<tr class="odd">
<td>hat noch</td>
<td>Gibt " <strong>true</strong> " zurück, wenn das Gerät Dateien mit einem einzelnen Bild effizienter behandelt als Bewegungsvideo Dateien.</td>
</tr>
<tr class="even">
<td>hat Zeitcode</td>
<td>Gibt " <strong>true</strong> " zurück, wenn das Gerät Timecode unterstützen kann oder unbekannt ist.</td>
</tr>
<tr class="odd">
<td>hat Video</td>
<td>Gibt <strong>true</strong> zurück, wenn das Gerät Video unterstützt.</td>
</tr>
<tr class="even">
<td>inputs</td>
<td>Gibt die Gesamtzahl der Eingabegeräte zurück.</td>
</tr>
<tr class="odd">
<td>maximale Wiedergabe Rate</td>
<td>Gibt die maximale Wiedergabe Rate in Frames pro Sekunde für das Gerät zurück.</td>
</tr>
<tr class="even">
<td>minimale Wiedergabe Rate</td>
<td>Gibt die minimale Wiedergabe Rate (in Frames pro Sekunde) für das Gerät zurück.</td>
</tr>
<tr class="odd">
<td>normale Wiedergabe Rate</td>
<td>Gibt die normale Wiedergabe Rate in Frames pro Sekunde für das Gerät zurück.</td>
</tr>
<tr class="even">
<td>Anzahl der Markierungen</td>
<td>Gibt die maximale Anzahl von Markierungen zurück, die verwendet werden können. NULL gibt an, dass Marken nicht unterstützt werden.</td>
</tr>
<tr class="odd">
<td>outputs</td>
<td>Gibt die Gesamtanzahl der Ausgabegeräte zurück.</td>
</tr>
<tr class="even">
<td>Genauigkeit suchen</td>
<td>Gibt die erwartete Genauigkeit einer Suche in Frames zurück. 0 gibt an, dass das Gerät Frame genau ist, 1 gibt an, dass das Gerät erwartet, dass es sich innerhalb eines Rahmens der bestimmten Suchposition befindet, usw.</td>
</tr>
<tr class="odd">
<td>Langsame Wiedergabe Rate</td>
<td>Gibt die langsame Wiedergabe Rate in Frames pro Sekunde zurück, oder 0 (null), wenn das Gerät nicht langsam wiedergegeben werden kann.</td>
</tr>
<tr class="even">
<td>verwendet Dateien</td>
<td>Gibt <strong>true</strong> zurück, wenn der von einem Verbund Gerät verwendete Datenspeicher eine Datei ist.</td>
</tr>
<tr class="odd">
<td>verwendet Paletten</td>
<td>Gibt " <strong>true</strong> " zurück, wenn das Gerät Paletten verwendet.</td>
</tr>
<tr class="even">
<td>Windows</td>
<td>Gibt die Anzahl der gleichzeitigen Anzeige Fenster zurück, die vom Gerät unterstützt werden können.</td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszflags*
</dt> <dd>

Kann "wait", "notify" oder beides sein. Für Digital Video-und VCR-Geräte kann auch "Test" angegeben werden. Weitere Informationen zu diesen Flags finden Sie [unter warte-, Benachrichtigungs-und testflags](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt Informationen im *lpszreturnstring* -Parameter der [**mciSendString**](/previous-versions//dd757161(v=vs.85)) -Funktion zurück. Die Informationen hängen vom Anforderungstyp ab.

## <a name="examples"></a>Beispiele

Mit dem folgenden Befehl wird der Gerätetyp des Geräts "mysound" zurückgegeben.

``` syntax
capability mysound device type
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

[STI](cue.md)
</dt> </dl>

 

