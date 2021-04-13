---
title: ICM_GETDEFAULTQUALITY Meldung (VFW. h)
description: Die ICM \_ getdefaultquality-Meldung fragt einen Video Komprimierungs Treiber ab, um die Standardeinstellung für die Qualität bereitzustellen. Sie können diese Nachricht explizit oder mithilfe des icgetdefaultquality-Makros senden.
ms.assetid: bba7f451-52c2-4684-a7c9-e4b05cb946c5
keywords:
- ICM_GETDEFAULTQUALITY-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- ICM_GETDEFAULTQUALITY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4350539851ca720e3538d297f955a56fedfc4a5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475699"
---
# <a name="icm_getdefaultquality-message"></a>ICM \_ getdefaultquality-Meldung

Die **ICM \_ getdefaultquality** -Meldung fragt einen Video Komprimierungs Treiber ab, um die Standardeinstellung für die Qualität bereitzustellen. Sie können diese Nachricht explizit oder mithilfe des [**icgetdefaultquality**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultquality) -Makros senden.


```C++
ICM_GETDEFAULTQUALITY 
wParam = (DWORD_PTR) (LPVOID) &dwICValue; 
lParam = 0; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="dwICValue"></span><span id="dwicvalue"></span><span id="DWICVALUE"></span>*dwicvalue*
</dt> <dd>

Adresse, die den Standardwert für die Qualität enthalten soll. Qualitätswerte liegen im Bereich von 0 bis 10.000.

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

 

 





