---
title: MCIWNDM_GETLENGTH (Vfw.h)
description: Die MCIWNDM GETLENGTH-Nachricht ruft die Länge des Inhalts oder der Datei ab, der bzw. die derzeit von \_ einem MCI-Gerät verwendet wird. Sie können diese Nachricht explizit oder mithilfe des MCIWndGetLength-Makros senden.
ms.assetid: bee4d9fc-78eb-4577-98bb-d6c2d9acbb7f
keywords:
- MCIWNDM_GETLENGTH-Nachricht Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_GETLENGTH
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 334d9a4a62171a62cbd0fc914be2d9a81ed901eab6d3893170cb8dabd2426a36
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118374187"
---
# <a name="mciwndm_getlength-message"></a>MCIWNDM \_ GETLENGTH-Nachricht

Die **MCIWNDM \_ GETLENGTH-Nachricht** ruft die Länge des Inhalts oder der Datei ab, der bzw. die derzeit von einem MCI-Gerät verwendet wird. Sie können diese Nachricht explizit oder mithilfe des [**MCIWndGetLength-Makros**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetlength) senden.


```C++
MCIWNDM_GETLENGTH 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Rückgabewert

Gibt die Länge zurück. Die Einheiten für die Länge hängen vom aktuellen Zeitformat ab.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**MCIWndGetLength**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetlength)
</dt> </dl>

 

 





