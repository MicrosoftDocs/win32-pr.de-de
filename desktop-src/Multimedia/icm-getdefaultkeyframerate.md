---
title: ICM_GETDEFAULTKEYFRAMERATE Nachricht (Vfw.h)
description: Die ICM \_ GETDEFAULTKEYFRAMERATE-Nachricht fragt einen Videokomprimierungstreiber nach seinem standardmäßigen (oder bevorzugten) Keyframeabstand ab. Sie können diese Nachricht explizit oder mithilfe des ICGetDefaultejFrameRate-Makros senden.
ms.assetid: 2ebe37cc-3ec2-4b52-bd8f-71c44b704647
keywords:
- ICM_GETDEFAULTKEYFRAMERATE nachricht Windows Multimedia
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
ms.openlocfilehash: bff21682f08dfdcda120f5efb5f7f8629a9e93e21faaf27ff4ee9ee59da8c762
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120038700"
---
# <a name="icm_getdefaultkeyframerate-message"></a>\_ICM GETDEFAULTKEYFRAMERATE-Meldung

Die **ICM \_ GETDEFAULTKEYFRAMERATE-Nachricht** fragt einen Videokomprimierungstreiber nach seinem standardmäßigen (oder bevorzugten) Keyframeabstand ab. Sie können diese Nachricht explizit oder mithilfe des [**ICGetDefaultejFrameRate-Makros**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultkeyframerate) senden.


```C++
ICM_GETDEFAULTKEYFRAMERATE 
wParam = (DWORD_PTR) (LPVOID) &dwICValue; 
lParam = 0; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="dwICValue"></span><span id="dwicvalue"></span><span id="DWICVALUE"></span>*dwICValue*
</dt> <dd>

Adresse, die den bevorzugten Keyframeabstand enthalten soll.

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

 

 





