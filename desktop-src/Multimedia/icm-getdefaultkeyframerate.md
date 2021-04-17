---
title: ICM_GETDEFAULTKEYFRAMERATE Meldung (VFW. h)
description: Die ICM \_ getdefaultkeyframerate-Nachricht fragt einen Video Komprimierungs Treiber nach dem standardmäßigen (oder bevorzugten) Schlüssel Frame Abstand ab. Sie können diese Nachricht explizit oder mithilfe des icgetdefaulteyframerate-Makros senden.
ms.assetid: 2ebe37cc-3ec2-4b52-bd8f-71c44b704647
keywords:
- ICM_GETDEFAULTKEYFRAMERATE-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- ICM_GETDEFAULTKEYFRAMERATE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e64f2796ca1c2de10222330217a0e1deb7883baa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391968"
---
# <a name="icm_getdefaultkeyframerate-message"></a>ICM \_ getdefaultkeyframerate-Meldung

Die **ICM \_ getdefaultkeyframerate** -Nachricht fragt einen Video Komprimierungs Treiber nach dem standardmäßigen (oder bevorzugten) Schlüssel Frame Abstand ab. Sie können diese Nachricht explizit oder mithilfe des [**icgetdefaulteyframerate**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultkeyframerate) -Makros senden.


```C++
ICM_GETDEFAULTKEYFRAMERATE 
wParam = (DWORD_PTR) (LPVOID) &dwICValue; 
lParam = 0; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="dwICValue"></span><span id="dwicvalue"></span><span id="DWICVALUE"></span>*dwicvalue*
</dt> <dd>

Adresse, die den bevorzugten Schlüssel Frame Abstand enthalten soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt ICERR \_ OK zurück, wenn der Treiber diese Nachricht unterstützt oder wenn ICERR \_ andernfalls nicht unterstützt wird.

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

 

 





