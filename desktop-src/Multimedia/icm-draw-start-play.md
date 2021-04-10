---
title: ICM_DRAW_START_PLAY Meldung (VFW. h)
description: Die ICM \_ Draw \_ -Wiedergabe Meldung "Start" \_ stellt die Start-und Endzeit eines Wiedergabe Vorgangs für einen renderingtreiber bereit. Sie können diese Nachricht explizit oder mithilfe des icdrawstartplay-Makros senden.
ms.assetid: 27c4c06e-6510-43dc-a754-fe44144796f5
keywords:
- ICM_DRAW_START_PLAY-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- ICM_DRAW_START_PLAY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eefea0f6344fb598fac1f0413bba5c377c5914e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103450"
---
# <a name="icm_draw_start_play-message"></a>ICM \_ Draw \_ - \_ Wiedergabe Nachricht starten

Die **ICM \_ Draw \_ \_** -Wiedergabe Meldung "Start" stellt die Start-und Endzeit eines Wiedergabe Vorgangs für einen renderingtreiber bereit. Sie können diese Nachricht explizit oder mithilfe des [**icdrawstartplay**](/windows/desktop/api/Vfw/nf-vfw-icdrawstartplay) -Makros senden.


```C++
ICM_DRAW_START_PLAY 
wParam = (DWORD_PTR) lFrom; 
lParam = (DWORD_PTR) lTo; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lFrom"></span><span id="lfrom"></span><span id="LFROM"></span>*lfrom*
</dt> <dd>

Startzeit.

</dd> <dt>

<span id="lTo"></span><span id="lto"></span><span id="LTO"></span>*lTo*
</dt> <dd>

Endzeit.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Nachricht geht vor allen Frame Daten vor, die an den renderingtreiber gesendet werden.

Einheiten für *lfrom* und *LTO* werden mit der [**ICM \_ Draw \_ Begin**](icm-draw-begin.md) -Meldung angegeben. Bei Videodaten ist dies normalerweise eine Frame Nummer. Weitere Informationen zur Wiedergabe Rate finden Sie unter den **dwtrate** -und **dwscale** -Membern der [**icdrawbegin**](/windows/desktop/api/Vfw/ns-vfw-icdrawbegin) -Struktur.

Wenn die Endzeit kleiner als die Startzeit ist, wird die Wiedergabe Richtung umgekehrt.

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

 

 





