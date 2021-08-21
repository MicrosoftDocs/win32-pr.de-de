---
title: ICM_GETQUALITY (Vfw.h)
description: Die ICM \_ GETQUALITY-Nachricht fragt einen Videokomprimierungstreiber ab, um die aktuelle Qualitätseinstellung zurück zu geben.
ms.assetid: 8da99a26-7b2a-4118-89e1-7485915cbdc9
keywords:
- ICM_GETQUALITY-Nachricht Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_GETQUALITY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cef214fe36c713e63659fcbd4dde2021c8d410b36ea9f5525ed54c76c5c4b6a7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119495860"
---
# <a name="icm_getquality-message"></a>\_ICM GETQUALITY-Nachricht

Die **ICM \_ GETQUALITY-Nachricht** fragt einen Videokomprimierungstreiber ab, um die aktuelle Qualitätseinstellung zurück zu geben.


```C++
ICM_GETQUALITY 
wParam = (DWORD) (LPVOID) &dwICValue; 
lParam = 0; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="dwICValue"></span><span id="dwicvalue"></span><span id="DWICVALUE"></span>*dwICValue*
</dt> <dd>

Adresse, die den aktuellen Qualitätswert enthalten soll. Die Qualitätswerte liegen zwischen 0 und 10.000.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt ICERR \_ OK zurück, wenn der Treiber diese Meldung unterstützt, andernfalls ICERR \_ UNSUPPORTED.

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

 

 





