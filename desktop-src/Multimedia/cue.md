---
title: Befehl "Hinweis"
description: Der Hinweis Befehl bereitet die Wiedergabe oder Aufzeichnung vor. Mit Digital Video-, VCR-und Waveform-Audiogeräten wird dieser Befehl erkannt.
ms.assetid: 94fa0d0c-d5c9-4ef1-bb7d-22dfb09a7689
keywords:
- Hinweis Befehl Windows Multimedia
topic_type:
- apiref
api_name:
- cue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1dd71f06a71c8aff4752fc31d750a3612564eb8a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859313"
---
# <a name="cue-command"></a>Befehl "Hinweis"

Der Hinweis Befehl bereitet die Wiedergabe oder Aufzeichnung vor. Mit Digital Video-, VCR-und Waveform-Audiogeräten wird dieser Befehl erkannt.

Um diesen Befehl zu senden, wenden Sie die [**mciSendString**](/previous-versions//dd757161(v=vs.85)) -Funktion mit dem festgelegten *lpszcommand* -Parameter wie folgt an.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("cue %s %s %s"), 
  lpszDeviceID, 
  lpszInOutTo, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszde viceid*
</dt> <dd>

Der Bezeichner eines MCI-Geräts. Dieser Bezeichner oder Alias wird zugewiesen, wenn das Gerät geöffnet wird.

</dd> <dt>

<span id="lpszInOutTo"></span><span id="lpszinoutto"></span><span id="LPSZINOUTTO"></span>*lpszinoutto*
</dt> <dd>

Flag, mit dem ein Gerät für die Wiedergabe oder Aufzeichnung vorbereitet wird. In der folgenden Tabelle sind die Gerätetypen aufgeführt **, die den Hinweis Befehl und** die von den einzelnen Typen verwendeten Flags erkennen.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Wert</th>
<th>Position (Cue)</th>
<th>Position (Cue)</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Digitalvideo</td>
<td><ul>
<li>input</li>
<li>noshow</li>
</ul></td>
<td><ul>
<li>output</li>
<li>an <em>Position</em></li>
</ul></td>
</tr>
<tr class="even">
<td>VCR</td>
<td><ul>
<li>von <em>Position</em></li>
<li>input</li>
<li>output</li>
</ul></td>
<td><ul>
<li>ein Vorlauf ausgeführt</li>
<li>reverse</li>
<li>an <em>Position</em></li>
</ul></td>
</tr>
<tr class="odd">
<td>waveaudiodatei</td>
<td>input</td>
<td>output</td>
</tr>
</tbody>
</table>



 

In der folgenden Tabelle werden die Flags aufgelistet, die im *lpszinoutto* -Parameter und deren Bedeutung angegeben werden können.



| Wert           | Bedeutung                                                                                                                                                                                                                                                                                                        |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| von *Position* | Gibt an, wohin begonnen werden soll.                                                                                                                                                                                                                                                                                      |
| input           | Bereitet die Aufzeichnung vor. Für Digital Video-Geräte kann dieses Flag weggelassen werden, wenn die aktuelle Präsentations Quelle bereits die externe Eingabe ist.                                                                                                                                                                  |
| noshow          | Bereitet das Abspielen eines Frames vor, ohne es anzuzeigen. Wenn dieses Flag angegeben wird, zeigt die Anzeige weiterhin das Bild im Frame Puffer an, auch wenn der entsprechende Frame nicht die aktuelle Position ist. Mit einem nachfolgenden Hinweis Befehl ohne dieses Flag und ohne das Flag "to" wird der aktuelle Frame angezeigt. |
| output          | Bereitet das Abspielen vor. Wenn weder "Input" noch "Output" angegeben ist, lautet die Standardeinstellung "Output".                                                                                                                                                                                                           |
| ein Vorlauf ausgeführt         | Verschiebt die Entfernung des vorab *-und des-Punkts*. Der-Punkt ist die aktuelle Position oder die durch das Flag "from" angegebene Position.                                                                                                                                                                            |
| reverse         | Gibt an, dass die Wiedergabe Richtung rückwärts (rückwärts) ist.                                                                                                                                                                                                                                                             |
| an *Position*   | Verschiebt den Arbeitsbereich an die angegebene Position. Bei VCR-Geräten gibt dieses Flag an, wo der Vorgang beendet werden soll.                                                                                                                                                                                                             |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszflags*
</dt> <dd>

Kann "wait", "notify" oder beides sein. Für Digital Video-und VCR-Geräte kann auch "Test" angegeben werden. Weitere Informationen zu diesen Flags finden Sie [unter warte-, Benachrichtigungs-und testflags](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.

## <a name="remarks"></a>Bemerkungen

Obwohl es nicht erforderlich ist, kann die Verzögerung vor dem Starten oder aufzeichnen auf einigen Geräten die Verzögerung verringern, bevor das Gerät die Aktion startet.

Dieser Befehl schlägt fehl, wenn die Wiedergabe oder Aufzeichnung ausgeführt wird oder wenn das Gerät angehalten wurde.

Wenn Sie die Wiedergabe (mit dem Hinweis "Output") übernehmen, wird der Befehl "Befehl" mit dem Flag "from", "to" oder "Reverse" durch Ausgeben des [Befehls Befehls abgeb](play.md) Rochen.

Beim Durchsuchen der Aufzeichnung (mit der "Input"-Eingabe) wird der "Befehl"-Befehl ausgegeben, wenn der [Datensatz](record.md) -Befehl mit dem Flag "from", "to" oder "Initialize" ausgegeben wird.

## <a name="examples"></a>Beispiele

Der folgende Befehl bereitet das "mysound"-Gerät für die Aufzeichnung vor.

``` syntax
cue mysound input
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

[Theater](play.md)
</dt> <dt>

[record](record.md)
</dt> </dl>

 

