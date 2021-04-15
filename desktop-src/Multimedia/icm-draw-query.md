---
title: ICM_DRAW_QUERY Meldung (VFW. h)
description: Die ICM \_ - \_ Abfrage Nachricht fragt einen renderingtreiber ab, um zu bestimmen, ob Daten in einem bestimmten Format gerendert werden können. Sie können diese Nachricht explizit oder mithilfe des icdrawquery-Makros senden.
ms.assetid: b829a04b-c1be-47c6-96e9-a6dc6f802811
keywords:
- ICM_DRAW_QUERY-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- ICM_DRAW_QUERY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27266484cffa503583df32b60c6e8a0c04f344f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477256"
---
# <a name="icm_draw_query-message"></a>ICM \_ - \_ Abfrage Nachricht zeichnen

Die **ICM \_ - \_ Abfrage** Nachricht fragt einen renderingtreiber ab, um zu bestimmen, ob Daten in einem bestimmten Format gerendert werden können. Sie können diese Nachricht explizit oder mithilfe des [**icdrawquery**](/windows/desktop/api/Vfw/nf-vfw-icdrawquery) -Makros senden.


```C++
ICM_DRAW_QUERY 
wParam = (DWORD_PTR) (LPVOID) lpbiInput; 
lParam = 0; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiinput*
</dt> <dd>

Zeiger auf eine [**BitmapInfo**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) -Struktur, die das Eingabeformat enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt ICERR \_ OK zurück, wenn der Treiber die Daten im angegebenen Format oder im angegebenen Format von ICERR badformat Renderen kann \_ .

## <a name="remarks"></a>Bemerkungen

Diese Meldung unterscheidet sich von der [**ICM \_ Draw \_ Begin**](icm-draw-begin.md) -Meldung darin, dass der Treiber allgemein abgefragt wird. **ICM \_ Zeichnen \_ Begin** bestimmt, ob der Treiber die Daten unter bestimmten Bedingungen unter Verwendung des angegebenen Formats zeichnen kann, z. b. durch Streckung des Bilds.

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

 

