---
title: ICM_DRAW_START_PLAY (Vfw.h)
description: Die ICM DRAW START PLAY-Meldung gibt die Start- und Endzeiten eines Wiedergabevorgang \_ \_ für einen \_ Renderingtreiber an. Sie können diese Nachricht explizit oder mithilfe des ICDrawStartPlay-Makros senden.
ms.assetid: 27c4c06e-6510-43dc-a754-fe44144796f5
keywords:
- ICM_DRAW_START_PLAY von Windows Multimedia
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
ms.openlocfilehash: 57caf05182f01ef1e6aec6939946a23ca0acf6f3f82ec29be04ec7e3a49cb782
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117987235"
---
# <a name="icm_draw_start_play-message"></a>\_ICM DRAW \_ START \_ PLAY-Meldung

Die **ICM DRAW START \_ \_ \_ PLAY-Meldung** gibt die Start- und Endzeiten eines Wiedergabevorgang für einen Renderingtreiber an. Sie können diese Nachricht explizit oder mithilfe des [**ICDrawStartPlay-Makros**](/windows/desktop/api/Vfw/nf-vfw-icdrawstartplay) senden.


```C++
ICM_DRAW_START_PLAY 
wParam = (DWORD_PTR) lFrom; 
lParam = (DWORD_PTR) lTo; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lFrom"></span><span id="lfrom"></span><span id="LFROM"></span>*lFrom*
</dt> <dd>

Startzeit.

</dd> <dt>

<span id="lTo"></span><span id="lto"></span><span id="LTO"></span>*Lto*
</dt> <dd>

Endzeit.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Diese Meldung geht allen Framedaten voraus, die an den Renderingtreiber gesendet werden.

Einheiten für *lFrom und* *lTo* werden mit der folgenden DRAW [**\_ BEGIN ICM \_ angegeben.**](icm-draw-begin.md) Bei Videodaten ist dies normalerweise eine Framenummer. Weitere Informationen zur Wiedergaberate finden Sie unter **den dwRate-** und **dwScale-Membern** der [**ICDRAWBEGIN-Struktur.**](/windows/desktop/api/Vfw/ns-vfw-icdrawbegin)

Wenn die Endzeit kleiner als die Startzeit ist, wird die Wiedergaberichtung umgekehrt.

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

 

 





