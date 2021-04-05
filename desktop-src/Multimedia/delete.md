---
title: DELETE-Befehl
description: Der DELETE-Befehl löscht ein Daten Segment aus einer Datei. Digital-Video-und Waveform-Audiogeräte erkennen diesen Befehl.
ms.assetid: 9cf084f6-d64e-4487-9407-b68502b7cec9
keywords:
- DELETE-Befehl Windows Multimedia
topic_type:
- apiref
api_name:
- delete
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e356d4972384e676f2e521bd2ca102bb21d7ef2c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859223"
---
# <a name="delete-command"></a>DELETE-Befehl

Der DELETE-Befehl löscht ein Daten Segment aus einer Datei. Digital-Video-und Waveform-Audiogeräte erkennen diesen Befehl.

Um diesen Befehl zu senden, wenden Sie die [**mciSendString**](/previous-versions//dd757161(v=vs.85)) -Funktion mit dem festgelegten *lpszcommand* -Parameter wie folgt an.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("delete %s %s %s"), 
  lpszDeviceID, 
  lpszPosition, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszde viceid*
</dt> <dd>

Der Bezeichner eines MCI-Geräts. Dieser Bezeichner oder Alias wird zugewiesen, wenn das Gerät geöffnet wird.

</dd> <dt>

<span id="lpszPosition"></span><span id="lpszposition"></span><span id="LPSZPOSITION"></span>*lpszposition*
</dt> <dd>

Flag, das ein zu löschende Daten Segment identifiziert. In der folgenden Tabelle werden die Gerätetypen aufgelistet, die den **Delete** -Befehl und die von den einzelnen Typen verwendeten Flags erkennen.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Wert</th>
<th>Bedeutung</th>
<th>Bedeutung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Digitalvideo</td>
<td><ul>
<li>at- <em>Rechteck</em></li>
<li>Audiostream- <em>Stream</em></li>
<li>von <em>Position</em></li>
</ul></td>
<td><ul>
<li>an <em>Position</em></li>
<li><em>videostreamstream</em></li>
</ul></td>
</tr>
<tr class="even">
<td>waveaudiodatei</td>
<td>von <em>Position</em></td>
<td>an <em>Position</em></td>
</tr>
</tbody>
</table>



 

In der folgenden Tabelle werden die Flags aufgelistet, die im *lpszposition* -Parameter und deren Bedeutung angegeben werden können.



| Wert                 | Bedeutung                                                                                                                                                                                                                                      |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| at- *Rechteck*        | Gibt den Teil jedes gelöschten Frames an. Wenn der Wert nicht weggelassen wird, wird standardmäßig der gesamte Frame verwendet. Wenn dieses Element angegeben wird, werden Rahmen nicht gelöscht. Stattdessen wird der Bereich innerhalb des Rechtecks schwarz.                                          |
| Audiostream- *Stream* | Gibt den Audiodatenstrom im Arbeitsbereich an, der vom Befehl betroffen ist. Wenn Sie dieses Flag verwenden und Video auch löschen möchten, müssen Sie auch das Flag "Videostream" verwenden. (Wenn keines der Flags angegeben ist, werden alle Audio-und Videostreams gelöscht.) |
| von *Position*       | Gibt die Position an, an der der Löschvorgang beginnt. Wenn dieses Flag weggelassen wird, beginnt der Löschvorgang an der aktuellen Position.                                                                                                                       |
| an *Position*         | Gibt die Position an, an der der Löschvorgang endet. Wenn dieses Flag weggelassen wird, wird der Löschvorgang bis zum Ende des Inhalts oder Arbeitsbereichs fortgesetzt.                                                                                                       |
| *videostreamstream* | Gibt den Videostream im Arbeitsbereich an, der vom Befehl betroffen ist. Wenn Sie dieses Flag verwenden und auch Audiodaten löschen möchten, müssen Sie auch das Flag "Audiostream" verwenden. (Wenn keines der Flags angegeben ist, werden alle Audio-und Videostreams gelöscht.)     |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszflags*
</dt> <dd>

Kann "wait", "notify" oder beides sein. Für Digital Video-und VCR-Geräte kann auch "Test" angegeben werden. Weitere Informationen zu diesen Flags finden Sie [unter warte-, Benachrichtigungs-und testflags](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.

## <a name="remarks"></a>Bemerkungen

Vor dem Ausgeben von Befehlen, die Positionswerte verwenden, sollten Sie das gewünschte Zeitformat mithilfe des [Set](set.md) -Befehls festlegen.

## <a name="examples"></a>Beispiele

Der folgende Befehl löscht die Waveform-Audiodaten von 1 Millisekunde bis 900 Millisekunden (vorausgesetzt, das Uhrzeit Format ist auf Millisekunden festgelegt).

``` syntax
delete mysound from 1 to 900
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

[set](set.md)
</dt> </dl>

 

