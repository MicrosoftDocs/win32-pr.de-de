---
title: ICM_CONFIGURE Meldung (VFW. h)
description: In der ICM-Konfigurations \_ Meldung wird ein Video Komprimierungs Treiber benachrichtigt, um das Konfigurations Dialogfeld anzuzeigen oder einen Video Komprimierungs Treiber zu Fragen
ms.assetid: 9760788e-fa66-44d7-bda6-aa9536143774
keywords:
- ICM_CONFIGURE-Nachricht (Multimedia)
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
ms.openlocfilehash: 9faae26fcf132abfa424b0db7a88670735d30727
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342868"
---
# <a name="icm_configure-message"></a>ICM- \_ Konfigurations Meldung

In der **ICM- \_ Konfigurations** Meldung wird ein Video Komprimierungs Treiber benachrichtigt, um das Konfigurations Dialogfeld anzuzeigen oder einen Video Komprimierungs Treiber zu Fragen Sie können diese Nachricht explizit oder mithilfe des [**icconfigure**](/windows/desktop/api/Vfw/nf-vfw-icconfigure) -Makros senden.


```C++
ICM_CONFIGURE 
wParam = (DWORD_PTR) (UINT_PTR) hwnd; 
lParam = 0; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="hwnd"></span><span id="HWND"></span>*HWND*
</dt> <dd>

Handle für das übergeordnete Fenster des angezeigten Dialog Felds. Sie können feststellen, ob ein Treiber über ein Konfigurations Dialogfeld verfügt, indem Sie 1 in diesem Parameter angeben, wie im [**icqueryconfigure**](/windows/desktop/api/Vfw/nf-vfw-icqueryconfigure) -Makro.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt ICERR \_ OK zurück, wenn der Treiber diese Nachricht unterstützt oder wenn ICERR \_ andernfalls nicht unterstützt wird.

## <a name="remarks"></a>Bemerkungen

Diese Meldung unterscheidet sich von der für die Hardwarekonfiguration verwendeten drv-Konfigurations Nachricht. [**\_**](drv-configure.md) Im Dialogfeld für diese Meldung soll der Benutzer den internen Zustand festlegen und bearbeiten können, auf den die ICM-Meldungen " [**\_ GetState**](icm-getstate.md) " und " [**ICM \_ SetState**](icm-setstate.md) " verweisen. Mithilfe dieses Dialog Felds kann der Benutzer beispielsweise die Parameter ändern, die die Qualitätsstufe und andere ähnliche Komprimierungs Optionen beeinträchtigen.

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

 

 





