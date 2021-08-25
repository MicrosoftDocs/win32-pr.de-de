---
title: ICM_ABOUT-Nachricht (Vfw.h)
description: Die ICM \_ ABOUT-Meldung benachrichtigt einen Videokomprimierungstreiber, sein Dialogfeld "About" anzuzeigen, oder fragt einen Videokomprimierungstreiber ab, um festzustellen, ob er über ein Dialogfeld "About" verfügt. Sie können diese Nachricht explizit oder mithilfe des ICAbout-Makros senden.
ms.assetid: 6eca69a3-0463-48e6-befb-5003b7515e7d
keywords:
- ICM_ABOUT nachricht Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_ABOUT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bf47ff93ef1986d805b2cb37697fdf4d86876c5552fe6aeffb00ff172673018
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119785070"
---
# <a name="icm_about-message"></a>\_ICM ABOUT-Nachricht

Die **ICM \_ ABOUT-Meldung** benachrichtigt einen Videokomprimierungstreiber, sein Dialogfeld "About" anzuzeigen, oder fragt einen Videokomprimierungstreiber ab, um festzustellen, ob er über ein Dialogfeld "About" verfügt. Sie können diese Nachricht explizit oder mithilfe des [**ICAbout-Makros**](/windows/desktop/api/Vfw/nf-vfw-icabout) senden.


```C++
ICM_ABOUT 
wParam = (DWORD_PTR) (UINT_PTR) hwnd; 
lParam = 0; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="hwnd"></span><span id="HWND"></span>*Hwnd*
</dt> <dd>

Handle für das übergeordnete Fenster des angezeigten Dialogfelds. Sie können auch ermitteln, ob ein Treiber über ein Dialogfeld "About" verfügt, indem Sie in diesem Parameter -1 angeben, wie im [**ICQueryAbout-Makro.**](/windows/desktop/api/Vfw/nf-vfw-icqueryabout) Der Treiber gibt ICERR \_ OK zurück, wenn er über ein About-Dialogfeld oder andernfalls ICERR \_ UNSUPPORTED verfügt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt ICERR \_ OK zurück, wenn der Treiber diese Meldung unterstützt, andernfalls ICERR \_ UNSUPPORTED.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Videokomprimierungs-Manager](video-compression-manager.md)
</dt> <dt>

[Videokomprimierungsmeldungen](video-compression-messages.md)
</dt> </dl>

 

 





