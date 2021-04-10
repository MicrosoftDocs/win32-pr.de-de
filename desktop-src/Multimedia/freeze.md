---
title: Freeze-Befehl
description: Der Freeze-Befehl friert Videoeingaben oder Video Ausgaben auf einem VCR oder deaktiviert die Video Beschaffung im Frame Puffer. Dieser Befehl wird von Digital Video, Video Overlay und VCR-Geräten erkannt.
ms.assetid: 49f3ab98-e893-402a-be78-6140af3b81df
keywords:
- Freeze-Befehl Windows Multimedia
topic_type:
- apiref
api_name:
- freeze
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7b63fbb2d888fc1ca315c0b511bcb18224c8168
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040080"
---
# <a name="freeze-command"></a>Freeze-Befehl

Der Freeze-Befehl friert Videoeingaben oder Video Ausgaben auf einem VCR oder deaktiviert die Video Beschaffung im Frame Puffer. Dieser Befehl wird von Digital Video, Video Overlay und VCR-Geräten erkannt.

Um diesen Befehl zu senden, wenden Sie die [**mciSendString**](/previous-versions//dd757161(v=vs.85)) -Funktion mit dem festgelegten *lpszcommand* -Parameter wie folgt an.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("freeze %s %s %s"), 
  lpszDeviceID, 
  lpszFreezeFlags, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszde viceid*
</dt> <dd>

Der Bezeichner eines MCI-Geräts. Dieser Bezeichner oder Alias wird zugewiesen, wenn das Gerät geöffnet wird.

</dd> <dt>

<span id="lpszFreezeFlags"></span><span id="lpszfreezeflags"></span><span id="LPSZFREEZEFLAGS"></span>*lpszfrezeflags*
</dt> <dd>

Flag, das angibt, was fixiert werden soll. In der folgenden Tabelle werden die Gerätetypen aufgelistet, die den **Freeze** -Befehl und die von den einzelnen Typen verwendeten Flags erkennen.



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
<td>at- <em>Rechteck</em></td>
<td>außerhalb</td>
</tr>
<tr class="even">
<td>overlay</td>
<td>at- <em>Rechteck</em></td>

</tr>
<tr class="odd">
<td>VCR</td>
<td><ul>
<li>Feld</li>
<li>frame</li>
</ul></td>
<td><ul>
<li>input</li>
<li>output</li>
</ul></td>
</tr>
</tbody>
</table>



 

In der folgenden Tabelle werden die Flags aufgelistet, die im *lpszfrezeflags* -Parameter und deren Bedeutung angegeben werden können.



| Wert          | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| at- *Rechteck* | Gibt den Bereich an, der fixiert wird. Bei Video Überlagerungs Geräten wird die Video Erfassung in dieser Region deaktiviert. Bei Digital Video-Geräten wird das Sperr Masken Bit für die Pixel innerhalb des Rechtecks aktiviert (es sei denn, das Flag "outside" ist angegeben). Das Rechteck ist relativ zum Video Puffer Ursprung und wird als *x1 y1 x2 Y2* angegeben. Die Koordinaten *x1 y1* geben die linke obere Ecke des Rechtecks an, und die Koordinaten *x2 Y2* geben die Breite und Höhe an. |
| Feld          | Friert das erste Feld ein. Standardmäßig wird ein Feld angenommen (wenn weder ein Frame noch ein Feld angegeben ist).                                                                                                                                                                                                                                                                                                                                                                                               |
| frame          | Friert den gesamten Frame und zeigt beide Felder an.                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| input          | Friert den aktuellen Frame des Eingabe Bilds, unabhängig davon, ob er angehalten oder ausgeführt wird.                                                                                                                                                                                                                                                                                                                                                                                                                |
| output         | Friert den aktuellen Frame der Ausgabe vom VCR. Wenn VCR beim Ausgeben von Freeze wiedergegeben wird, wird der aktuelle Frame eingefroren und das VCR angehalten. Wenn VCR angehalten wird, wenn dieser Befehl ausgegeben wird, wird der aktuelle Frame fixiert. Das [fixierte](unfreeze.md) Bild verbleibt auf dem Ausgabegerät, bis ein Befehl zum Aufheben der Fixierung ausgegeben wird. Wenn weder "Input" noch "Output" angegeben ist, wird "Output" angenommen.                                                                                    |
| außerhalb        | Gibt an, dass der Bereich außerhalb des Bereichs, der mit dem Flag "at" angegeben wurde, eingefroren ist.                                                                                                                                                                                                                                                                                                                                                                                                           |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszflags*
</dt> <dd>

Kann "wait", "notify" oder beides sein. Für Digital Video-und VCR-Geräte kann auch "Test" angegeben werden. Weitere Informationen zu diesen Flags finden Sie [unter warte-, Benachrichtigungs-und testflags](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.

## <a name="remarks"></a>Bemerkungen

Bei der Verwendung mit VCR-Geräten ist dieser Befehl für Frame Karten vorgesehen.

Verwenden Sie zum angeben irregulärer Erwerbs Regionen mit dem Flag "at" eine Reihe von Freeze-und [Fixierung aufheben](unfreeze.md) -Befehlen. Einige Video Überlagerungs Geräte schränken die Komplexität des Erwerbs Bereichs ein.

Dieser Befehl wird nur unterstützt, wenn [ein Befehl zum Funktionsbefehl mit](capability.md) dem Flag "kann eingefroren" den Wert " **true**" zurückgibt.

## <a name="examples"></a>Beispiele

Der folgende Befehl deaktiviert die Video Erfassung in einem 100-Pixel-Quadrat in der oberen linken Ecke des Video Puffers.

``` syntax
freeze vboard at 0 0 100 100
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

[Fixierung aufheben](unfreeze.md)
</dt> </dl>

 

