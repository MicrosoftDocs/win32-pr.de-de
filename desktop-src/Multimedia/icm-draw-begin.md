---
title: ICM_DRAW_BEGIN Meldung (VFW. h)
description: Mit der ICM \_ Draw \_ Begin-Meldung wird ein renderingertreiber benachrichtigt, um das Zeichnen von Daten vorzubereiten.
ms.assetid: e5ecd7dd-376b-422c-bbb8-4e7c41e3cac8
keywords:
- ICM_DRAW_BEGIN-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- ICM_DRAW_BEGIN
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db7b9e20a0b0621038e1c7e092a871a6727566cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956971"
---
# <a name="icm_draw_begin-message"></a>ICM- \_ Zeichnungs \_ anfangs Nachricht

Mit der **ICM \_ Draw \_ Begin** -Meldung wird ein renderingertreiber benachrichtigt, um das Zeichnen von Daten vorzubereiten.


```C++
ICM_DRAW_BEGIN 
wParam = (DWORD) (LPVOID) &icdrwBgn; 
lParam = sizeof(ICDRAW); 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="icdrwBgn"></span><span id="icdrwbgn"></span><span id="ICDRWBGN"></span>*icdrwbgn*
</dt> <dd>

Zeiger auf eine [**icdrawbegin**](/windows/desktop/api/Vfw/ns-vfw-icdrawbegin) -Struktur, die das Eingabeformat enthält.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*LParam*
</dt> <dd>

Größe von **icdrawbegin**(in Bytes).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt ICERR \_ OK zurück, wenn der Treiber das Zeichnen der Daten auf den Bildschirm auf die angegebene Art und Weise unterstützt, oder andernfalls ein Fehlercode. Folgende Fehler Werte sind möglich:



| Wert               | Bedeutung                                                                       |
|---------------------|-------------------------------------------------------------------------------|
| ICERR \_ badformat    | Ein Eingabe-oder Ausgabeformat wird nicht unterstützt.                                      |
| ICERR \_ NotSupported | Der Treiber wird nicht direkt auf den Bildschirm gezeichnet oder unterstützt diese Meldung nicht. |



 

## <a name="remarks"></a>Bemerkungen

Wenn Sie möchten, dass der Treiber Daten in einen Puffer dekomprimiert, senden Sie die [**ICM \_ dekomprimieren \_ Begin**](icm-decompress-begin.md) -Nachricht.

Die **ICM \_ Draw- \_ Begin** -und [**ICM \_ Draw \_**](icm-draw-end.md) -Meldungen werden nicht geschachtelt. Wenn der Treiber den **ICM- \_ Zeichnen- \_ Anfang** erhält, bevor die Dekomprimierung mit dem **ICM- \_ Zeichnungs \_ Ende** beendet wird, sollte die Dekomprimierung mit neuen Parametern neu gestartet

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

 

 





