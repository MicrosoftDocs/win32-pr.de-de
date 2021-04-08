---
title: ICM_DRAW Meldung (VFW. h)
description: Mit der ICM \_ Draw-Nachricht wird ein renderingertreiber benachrichtigt, um einen Datenrahmen zu dekomprimieren und auf dem Bildschirm zu zeichnen.
ms.assetid: eceb42c6-d91a-45b7-98dc-e0944df3e558
keywords:
- ICM_DRAW-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- ICM_DRAW
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0840c6df2c69f4d3e45600cf8599c214b36200a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741169"
---
# <a name="icm_draw-message"></a>ICM- \_ Zeichnungs Meldung

Mit der **ICM \_ Draw** -Nachricht wird ein renderingertreiber benachrichtigt, um einen Datenrahmen zu dekomprimieren und auf dem Bildschirm zu zeichnen.


```C++
ICM_DRAW 
wParam = (DWORD) (LPVOID) &icdraw; 
lParam = sizeof(ICDRAW); 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*
</dt> <dd>

Zeiger auf eine [**icdraw**](/windows/desktop/api/Vfw/ns-vfw-icdraw) -Struktur.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*LParam*
</dt> <dd>

Größe von [**icdraw**](/windows/desktop/api/Vfw/ns-vfw-icdraw)(in Bytes).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei erfolgreicher Ausführung von ICERR \_ OK oder andernfalls einen Fehler zurück.

## <a name="remarks"></a>Bemerkungen

Wenn das icdraw- \_ updateflag im **dwFlags** -Member von [**icdraw**](/windows/desktop/api/Vfw/ns-vfw-icdraw)festgelegt wird, ist der zum Zeichnen verwendete Bildschirm ungültig und muss aktualisiert werden. Der Umfang der Aktualisierung hängt vom Inhalt des **lpdata** -Members ab.

Wenn **lpdata** **null** ist, sollte der Treiber das gesamte Ziel Rechteck mit dem aktuellen Bild aktualisieren. Wenn der Treiber eine Kopie des Abbilds in einem Offscreen-Puffer verwaltet, kann diese Meldung fehlschlagen. Wenn **lpdata** nicht **null** ist, sollte der Treiber die Daten zeichnen und sicherstellen, dass das gesamte Ziel aktualisiert wird.

Wenn das icdraw- \_ hurryup-Flag in **dwFlags** festgelegt ist, möchte die aufrufende Anwendung, dass der Treiber so schnell wie möglich fortgesetzt werden kann. möglicherweise wird der Bildschirm nicht sogar aktualisiert.

Wenn das icdraw- \_ vorab-Flag in **dwFlags** festgelegt ist, handelt es sich bei diesem Videoframe um vorläufige Informationen, die nach Möglichkeit nicht angezeigt werden sollten. Wenn z. b. "Play" von Frame 10 gestartet werden soll und Frame 0 der nächste vorherige Keyframe ist, haben die Rahmen 0 bis 9 das icdraw- \_ vorab Zeichen festgelegt.

Wenn Sie möchten, dass der Treiber Daten in einen Puffer dekomprimieren soll, senden Sie die [**ICM \_ dekomprimieren**](icm-decompress.md) -Nachricht.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Videokomprimierungs-Manager](video-compression-manager.md)
</dt> <dt>

[Video Komprimierungs Meldungen](video-compression-messages.md)
</dt> </dl>

 

 





