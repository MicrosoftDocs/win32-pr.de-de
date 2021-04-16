---
title: Befehl "Aktualisieren"
description: Der Update-Befehl zeichnet den aktuellen Frame in den angegebenen Gerätekontext (DC). Dieser Befehl wird von Digital-Video-Geräten erkannt.
ms.assetid: 51a83262-91d5-4852-ad17-bd62c14417b1
keywords:
- Update Befehl Windows-Multimedia
topic_type:
- apiref
api_name:
- update
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cb0fc96d404efd8e2f657985ffa5a8861d3b4f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518962"
---
# <a name="update-command"></a>Befehl "Aktualisieren"

Der Update-Befehl zeichnet den aktuellen Frame in den angegebenen Gerätekontext (DC). Dieser Befehl wird von Digital-Video-Geräten erkannt.

Um diesen Befehl zu senden, wenden Sie die [**mciSendString**](/previous-versions//dd757161(v=vs.85)) -Funktion mit dem festgelegten *lpszcommand* -Parameter wie folgt an.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("update %s %s %s"), 
  lpszDeviceID, 
  lpszHDC, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszde viceid*
</dt> <dd>

Der Bezeichner eines MCI-Geräts. Dieser Bezeichner oder Alias wird zugewiesen, wenn das Gerät geöffnet wird.

</dd> <dt>

<span id="lpszHDC"></span><span id="lpszhdc"></span><span id="LPSZHDC"></span>*lpszhdc*
</dt> <dd>

Handle eines DC. In der folgenden Tabelle sind die Gerätetypen aufgeführt, die den **Update** -Befehl und die von den einzelnen Typen verwendeten Flags erkennen.



| Wert        | Bedeutung                       | Bedeutung         |
|--------------|-------------------------------|-----------------|
| Digitalvideo | HDC *hdc* HDC *bei* *Rect* | HDC *hdc* zeichnen |



 

In der folgenden Tabelle werden die Flags aufgelistet, die im **lpszhdc** -Parameter und deren Bedeutung angegeben werden können.



| Wert               | Bedeutung                                                                                                |
|---------------------|--------------------------------------------------------------------------------------------------------|
| HDC- *hdc*           | Gibt das Handle des zu zeichnenden Domänen Controllers an.                                                               |
| HDC- *hdc* bei *Rect* | Gibt das Clippingrechteck relativ zum Client Rechteck an.                                     |
| HDC *hdc* zeichnen     | Zeichnet den DC, wenn die Anwendung eine [**WM \_**](/windows/desktop/gdi/wm-paint) -Zeichnungs Nachricht empfängt, die für einen Domänen Controller gedacht ist. |



 

Um das Handle des DC anzugeben, verwenden Sie die Zeichenfolge "HDC", gefolgt von einer ASCII-Darstellung des Handles. Das Rechteck wird als **x1 y1 x2 Y2** angegeben. Die Koordinaten **x1 y1** geben die linke obere Ecke des Rechtecks an, und die Koordinaten **x2 Y2** geben die Breite und Höhe an.

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszflags*
</dt> <dd>

Kann "wait", "notify" oder beides sein. Für Digital Video-Geräte kann auch "Test" angegeben werden. Weitere Informationen zu diesen Flags finden Sie [unter warte-, Benachrichtigungs-und testflags](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.

## <a name="examples"></a>Beispiele

Der folgende Befehl aktualisiert das gesamte Anzeige Fenster, das vom "Movie"-Gerät verwendet wird. Die Zahl 203 ist ein Handle für einen Domänen Controller, der von der [**BeginPaint**](/windows/desktop/api/winuser/nf-winuser-beginpaint) -Funktion abgerufen wird.

``` syntax
update movie hdc 203
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
</dt> </dl>

 

