---
title: ICM_DRAW_GETTIME Meldung (VFW. h)
description: Die ICM \_ Draw \_ GetTime-Nachricht fordert einen renderingtreiber an, der die zeitliche Steuerung der Zeichnungsrahmen steuert, um den aktuellen Wert der internen Uhr zurückzugeben. Sie können diese Nachricht explizit oder mithilfe des icdrawgettime-Makros senden.
ms.assetid: 77f0a322-c0bc-4cfe-a3d0-7633cf8d682a
keywords:
- ICM_DRAW_GETTIME-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- ICM_DRAW_GETTIME
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f756a76408d01cb72ee1762f14bb8a5eab19e475
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338552"
---
# <a name="icm_draw_gettime-message"></a>ICM \_ Zeichnen \_ GetTime-Meldung

Die **ICM \_ Draw \_ GetTime** -Nachricht fordert einen renderingtreiber an, der die zeitliche Steuerung der Zeichnungsrahmen steuert, um den aktuellen Wert der internen Uhr zurückzugeben. Sie können diese Nachricht explizit oder mithilfe des [**icdrawgettime**](/windows/desktop/api/Vfw/nf-vfw-icdrawgettime) -Makros senden.


```C++
ICM_DRAW_GETTIME 
wParam = (DWORD_PTR) (LPVOID) lplTime; 
lParam = 0; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lplTime"></span><span id="lpltime"></span><span id="LPLTIME"></span>*lpltime*
</dt> <dd>

Adresse, die die aktuelle Uhrzeit enthalten soll. Der Rückgabewert muss in Samples angegeben werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei erfolgreicher Ausführung von ICERR \_ OK oder andernfalls einen Fehler zurück.

## <a name="remarks"></a>Bemerkungen

Diese Meldung wird in der Regel von Hardware unterstützt, die eine eigene asynchrone Dekomprimierung, zeitliche Steuerung und Zeichnung ausführt. Die Nachricht kann auch gesendet werden, wenn die Hardware als Synchronisierungs Master verwendet wird.

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

 

 





