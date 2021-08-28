---
title: Capability-Befehl
description: Der Befehl capability fordert Informationen zu einer bestimmten Funktion eines Geräts an. Dieser Befehl wird von allen MCI-Geräten erkannt.
ms.assetid: 1b470473-0de6-41ba-9f6e-41f0b13ceaeb
keywords:
- Capability-Befehl Windows Multimedia
topic_type:
- apiref
api_name:
- capability
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44e57a793f799214753f50504d80bce7051fba14
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122469157"
---
# <a name="capability-command"></a>Capability-Befehl

Der Befehl capability fordert Informationen zu einer bestimmten Funktion eines Geräts an. Dieser Befehl wird von allen MCI-Geräten erkannt.

Um diesen Befehl zu senden, rufen Sie die [**mciSendString-Funktion**](/previous-versions//dd757161(v=vs.85)) mit dem *lpszCommand-Parameter* auf, der wie folgt festgelegt ist.

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

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Bezeichner eines MCI-Geräts. Dieser Bezeichner oder Alias wird zugewiesen, wenn das Gerät geöffnet wird.

</dd> <dt>

<span id="lpszRequest"></span><span id="lpszrequest"></span><span id="LPSZREQUEST"></span>*lpszRequest*
</dt> <dd>

Flag, das eine Gerätefunktion identifiziert. In der folgenden Tabelle sind Gerätetypen aufgeführt, die den **Funktionsbefehl** und die von den einzelnen Typen verwendeten Flags erkennen:




| Wert | Typ | Typ | 
|-------|------|------|
| cdaudio | <ul><li>kann auswerfen</li><li>can play</li><li>kann aufzeichnen</li><li>kann speichern.</li><li>Verbundgerät</li></ul> | <ul><li>Gerätetyp</li><li>verfügt über Audio</li><li>hat Video</li><li>verwendet Dateien.</li></ul> | 
| digitalvideo | <ul><li>kann auswerfen</li><li>kann einfrieren</li><li>kann sperren</li><li>can play</li><li>kann aufzeichnen</li><li>kann umgekehrt werden.</li><li>kann speichern.</li><li>kann gestreckt werden</li><li>kann Die Eingabe strecken</li><li>kann testen</li></ul> | <ul><li>Verbundgerät</li><li>Gerätetyp</li><li>verfügt über Audio</li><li>hat noch</li><li>hat Video</li><li>Maximale Wiedergaberate</li><li>Minimale Wiedergaberate</li><li>verwendet Dateien.</li><li>verwendet Paletten.</li><li>Windows</li></ul> | 
| overlay | <ul><li>kann auswerfen</li><li>kann einfrieren</li><li>can play</li><li>kann aufzeichnen</li><li>kann speichern.</li><li>kann gestreckt werden</li></ul> | <ul><li>Verbundgerät</li><li>Gerätetyp</li><li>verfügt über Audio</li><li>hat Video</li><li>verwendet Dateien.</li><li>Windows</li></ul> | 
| sequencer | <ul><li>kann auswerfen</li><li>can play</li><li>kann aufzeichnen</li><li>kann speichern.</li><li>Verbundgerät</li></ul> | <ul><li>Gerätetyp</li><li>verfügt über Audio</li><li>hat Video</li><li>verwendet Dateien.</li></ul> | 
| Vcr | <ul><li>kann Länge erkennen</li><li>kann auswerfen</li><li>kann einfrieren</li><li>kann Quellen überwachen.</li><li>can play</li><li>can preroll</li><li>kann in der Vorschau angezeigt werden.</li><li>kann aufzeichnen</li><li>kann umgekehrt werden.</li><li>kann speichern.</li><li>kann testen</li></ul> | <ul><li>Taktinkrementrate</li><li>Verbundgerät</li><li>Gerätetyp</li><li>verfügt über Audio</li><li>hat Uhr</li><li>hat Zeitcode</li><li>hat Video</li><li>Anzahl der Markierungen</li><li>Suchgenauigkeit</li><li>verwendet Dateien.</li></ul> | 
| videodisc | <ul><li>kann auswerfen</li><li>can play</li><li>kann aufzeichnen</li><li>kann umgekehrt werden.</li><li>kann speichern.</li><li>CAV</li><li>CLV</li><li>Verbundgerät</li></ul> | <ul><li>Gerätetyp</li><li>Schnelle Wiedergaberate</li><li>verfügt über Audio</li><li>hat Video</li><li>Normale Wiedergaberate</li><li>Langsame Wiedergaberate</li><li>verwendet Dateien</li></ul> | 
| Waveaudio | <ul><li>kann auswerfen</li><li>kann wiedergegeben werden</li><li>kann aufzeichnen</li><li>kann gespeichert werden</li><li>Verbundgerät</li><li>Gerätetyp</li></ul> | <ul><li>verfügt über Audio</li><li>hat Video</li><li>inputs</li><li>outputs</li><li>verwendet Dateien</li></ul> | 




 

Die folgende Tabelle enthält die Flags, die im *lpszRequest-Parameter* angegeben werden können, und ihre Bedeutungen:




| Flags | Bedeutung | 
|-------|---------|
| kann die Länge erkennen | Gibt <strong>TRUE</strong> zurück, wenn das Gerät die Länge des Mediums erkennen kann. | 
| kann auswerfen | Gibt <strong>TRUE</strong> zurück, wenn das Gerät die Medien auswerfen kann. | 
| kann einfrieren | Gibt <strong>TRUE</strong> zurück, wenn das Gerät Daten im Framepuffer einfrieren kann. | 
| kann gesperrt werden | Gibt <strong>TRUE</strong> zurück, wenn das Gerät Daten sperren kann. | 
| kann Quellen überwachen. | Gibt <strong>TRUE</strong> zurück, wenn das Gerät unabhängig von der aktuellen Eingabeauswahl eine Eingabe (Quelle) an die überwachte Ausgabe übergeben kann. | 
| kann wiedergegeben werden | Gibt <strong>TRUE</strong> zurück, wenn das Gerät wiedergegeben werden kann. | 
| kann vorabrolliert werden | Gibt <strong>TRUE</strong> zurück, wenn das Gerät das Flag "preroll" mit dem <a href="cue.md">Cue-Befehl</a> unterstützt. | 
| kann eine Vorschau anzeigen | Gibt <strong>TRUE</strong> zurück, wenn das Gerät Vorschauversionen unterstützt. | 
| kann aufzeichnen | Gibt <strong>TRUE</strong> zurück, wenn das Gerät die Aufzeichnung unterstützt. | 
| kann umkehren | Gibt <strong>TRUE</strong> zurück, wenn das Gerät umgekehrt wiedergegeben werden kann. | 
| kann gespeichert werden | Gibt <strong>TRUE</strong> zurück, wenn das Gerät Daten speichern kann. | 
| kann gestreckt werden | Gibt <strong>TRUE</strong> zurück, wenn das Gerät Frames strecken kann, um ein bestimmtes Anzeigerechteck zu füllen. | 
| eingabe kann gestreckt werden | Gibt <strong>TRUE</strong> zurück, wenn das Gerät die Größe eines Bilds beim Digitalisieren in den Framepuffer ändern kann. | 
| kann testen | Gibt <strong>TRUE</strong> zurück, wenn das Gerät das Testschlüsselwort erkennt. | 
| Cav | In Kombination mit anderen Elementen gibt dieses Flag an, dass die Rückgabeinformationen für videodiscs im CAV-Format gelten. Dies ist die Standardeinstellung, wenn keine videodisc eingefügt wird. | 
| Taktinkrementrate | Gibt die Anzahl von Unterteilungen zurück, die die externe Uhr pro Sekunde unterstützt. Wenn die externe Uhr eine Millisekunde ist, ist der Rückgabewert 1000. Wenn der Rückgabewert 0 ist, wird keine Uhr unterstützt. | 
| clv | In Kombination mit anderen Elementen gibt dieses Flag an, dass die Rückgabeinformationen für videodiscs im CLV-Format gelten. | 
| Verbundgerät | Gibt <strong>TRUE</strong> zurück, wenn das Gerät einen Elementnamen (Dateiname) unterstützt. | 
| Gerätetyp | Gibt einen Gerätetypnamen zurück, der einer der folgenden sein kann:<ul><li>cdaudio</li><li>Dat</li><li>digitalvideo</li><li>Andere</li><li>overlay</li><li>Scanner</li><li>sequencer</li><li>Vcr</li><li>videodisc</li><li>Waveaudio</li></ul> | 
| Schnelle Wiedergaberate | Gibt die schnelle Wiedergaberate in Frames pro Sekunde oder 0 (null) zurück, wenn das Gerät nicht schnell wiedergegeben werden kann. | 
| verfügt über Audio | Gibt <strong>TRUE</strong> zurück, wenn das Gerät die Audiowiedergabe unterstützt. | 
| verfügt über eine Uhr | Gibt <strong>TRUE</strong> zurück, wenn das Gerät über eine Uhr verfügt. | 
| hat noch | Gibt <strong>TRUE</strong> zurück, wenn das Gerät Dateien mit einem einzelnen Bild effizienter behandelt als Bewegungsvideodateien. | 
| hat timecode | Gibt <strong>TRUE</strong> zurück, wenn das Gerät zeitcode unterstützen kann oder unbekannt ist. | 
| hat Video | Gibt <strong>TRUE</strong> zurück, wenn das Gerät Video unterstützt. | 
| inputs | Gibt die Gesamtzahl der Eingabegeräte zurück. | 
| Maximale Wiedergaberate | Gibt die maximale Wiedergaberate in Frames pro Sekunde für das Gerät zurück. | 
| Mindestwiedergaberate | Gibt die minimale Wiedergaberate in Frames pro Sekunde für das Gerät zurück. | 
| Normale Wiedergaberate | Gibt die normale Wiedergaberate für das Gerät in Frames pro Sekunde zurück. | 
| Anzahl der Markierungen | Gibt die maximale Anzahl von Markierungen zurück, die verwendet werden können. Null gibt an, dass Markierungen nicht unterstützt werden. | 
| outputs | Gibt die Gesamtzahl der Ausgabegeräte zurück. | 
| Suchgenauigkeit | Gibt die erwartete Genauigkeit einer Suche in Frames zurück. 0 gibt an, dass das Gerät framegenau ist, 1 gibt an, dass das Gerät erwartet, dass es sich innerhalb eines Frames der angegebenen Suchposition befindet, und so weiter. | 
| Langsame Wiedergaberate | Gibt die langsame Wiedergaberate in Frames pro Sekunde zurück oder 0 (null), wenn das Gerät nicht langsam wiedergibt. | 
| verwendet Dateien. | Gibt <strong>TRUE zurück,</strong> wenn der von einem Verbundgerät verwendete Datenspeicher eine Datei ist. | 
| verwendet Paletten. | Gibt <strong>TRUE zurück,</strong> wenn das Gerät Paletten verwendet. | 
| Windows | Gibt die Anzahl gleichzeitiger Anzeigefenster zurück, die das Gerät unterstützen kann. | 




 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Kann "wait", "notify" oder beides sein. Für digital-video- und VCR-Geräte kann auch "test" angegeben werden. Weitere Informationen zu diesen Flags finden Sie unter [Die Warte-, Benachrichtigungs- und Testflags](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt Informationen im *lpszReturnString-Parameter* der [**mciSendString-Funktion**](/previous-versions//dd757161(v=vs.85)) zurück. Die Informationen hängen vom Anforderungstyp ab.

## <a name="examples"></a>Beispiele

Der folgende Befehl gibt den Gerätetyp des "mysound"-Geräts zurück.

``` syntax
capability mysound device type
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

[Hinweis](cue.md)
</dt> </dl>

 

