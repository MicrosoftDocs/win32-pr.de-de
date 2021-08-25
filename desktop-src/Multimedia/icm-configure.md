---
title: ICM_CONFIGURE (Vfw.h)
description: Die ICM CONFIGURE benachrichtigt einen Videokomprimierungstreiber, um das Konfigurationsdialogfeld anzuzeigen, oder fragt einen Videokomprimierungstreiber ab, um zu ermitteln, ob er über ein \_ Konfigurationsdialogfeld verfügt.
ms.assetid: 9760788e-fa66-44d7-bda6-aa9536143774
keywords:
- ICM_CONFIGURE-Nachricht Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_CONFIGURE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7bc2d9176415c22a1b79a8dc08ee84db1c77fbd6665f89f615b38d3c60538d51
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119785000"
---
# <a name="icm_configure-message"></a>\_ICM CONFIGURE-Nachricht

Die **ICM \_ CONFIGURE** benachrichtigt einen Videokomprimierungstreiber, um das Konfigurationsdialogfeld anzuzeigen, oder fragt einen Videokomprimierungstreiber ab, um zu ermitteln, ob er über ein Konfigurationsdialogfeld verfügt. Sie können diese Nachricht explizit oder mithilfe des [**ICConfigure-Makros**](/windows/desktop/api/Vfw/nf-vfw-icconfigure) senden.


```C++
ICM_CONFIGURE 
wParam = (DWORD_PTR) (UINT_PTR) hwnd; 
lParam = 0; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="hwnd"></span><span id="HWND"></span>*Hwnd*
</dt> <dd>

Handle für das übergeordnete Fenster des angezeigten Dialogfelds. Sie können ermitteln, ob ein Treiber über ein Konfigurationsdialogfeld verfügt, indem Sie in diesem Parameter 1 angeben, wie im [**ICQueryConfigure-Makro.**](/windows/desktop/api/Vfw/nf-vfw-icqueryconfigure)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt ICERR \_ OK zurück, wenn der Treiber diese Meldung unterstützt, andernfalls ICERR \_ UNSUPPORTED.

## <a name="remarks"></a>Hinweise

Diese Meldung ist anders als die FÜR die Hardwarekonfiguration verwendete [**DRV \_ CONFIGURE-Meldung.**](drv-configure.md) Im Dialogfeld für diese Meldung sollte der Benutzer den internen Zustand festlegen und bearbeiten können, auf den die [**\_ getstate ICM**](icm-getstate.md) und setstate ICM [**verweist. \_**](icm-setstate.md) Mit diesem Dialogfeld kann der Benutzer z. B. Parameter ändern, die sich auf die Qualitätsstufe und andere ähnliche Komprimierungsoptionen beeinflussen.

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

 

 





