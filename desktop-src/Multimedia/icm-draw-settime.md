---
title: ICM_DRAW_SETTIME-Nachricht (Vfw.h)
description: Der ICM \_ DRAW \_ SETTIME stellt Synchronisierungsinformationen für einen Renderingtreiber bereit, der die Zeitsteuerung von Zeichnungsframes verarbeitet.
ms.assetid: 211e8ecc-ef36-4598-aa1d-cb0a06e64f14
keywords:
- ICM_DRAW_SETTIME nachricht Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_DRAW_SETTIME
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62c291b736b0138386c235703c29fffdae470d011f55284e8aaac4c4cfd604a4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119691140"
---
# <a name="icm_draw_settime-message"></a>\_ICM DRAW \_ SETTIME-Nachricht

Der **ICM \_ DRAW \_ SETTIME** stellt Synchronisierungsinformationen für einen Renderingtreiber bereit, der die Zeitsteuerung von Zeichnungsframes verarbeitet. Die Synchronisierungsinformationen sind die Beispielnummer des zu zeichnende Frames. Sie können diese Nachricht explizit oder mithilfe des [**ICDrawSetTime-Makros**](/windows/desktop/api/Vfw/nf-vfw-icdrawsettime) senden.


```C++
ICM_DRAW_SETTIME 
wParam = (DWORD_PTR) lpTime; 
lParam = 0; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lpTime"></span><span id="lptime"></span><span id="LPTIME"></span>*lpTime*
</dt> <dd>

Beispielnummer des zu rendernde Rahmens.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt ICERR \_ OK zurück, wenn erfolgreich, oder andernfalls ein Fehler.

## <a name="remarks"></a>Hinweise

In der Regel vergleicht der Treiber den angegebenen Wert mit der Framenummer, die der Zeit seiner internen Uhr zugeordnet ist, und versucht, die beiden zu synchronisieren, wenn der Unterschied signifikant ist.

Verwenden Sie diese Meldung, wenn die Hardware eine eigene asynchrone Dekomprimierung, zeitliche Steuerung und Zeichnung ausführt und die Hardware von einem externen Synchronisierungssignal abhängig ist (die Hardware wird nicht als Synchronisierungsmaster verwendet).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Videokomprimierungs-Manager](video-compression-manager.md)
</dt> <dt>

[Videokomprimierungsmeldungen](video-compression-messages.md)
</dt> </dl>

 

 





