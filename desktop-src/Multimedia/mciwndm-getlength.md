---
title: MCIWNDM_GETLENGTH Meldung (VFW. h)
description: Die mciwndm \_ GetLength-Nachricht Ruft die Länge des Inhalts oder der Datei ab, die derzeit von einem MCI-Gerät verwendet wird. Sie können diese Nachricht explizit oder mit dem mciwndgetlength-Makro senden.
ms.assetid: bee4d9fc-78eb-4577-98bb-d6c2d9acbb7f
keywords:
- MCIWNDM_GETLENGTH-Nachricht (Multimedia)
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
ms.openlocfilehash: 2347647fcff0beb87be12b7f6a05790b97f36d51
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475528"
---
# <a name="mciwndm_getlength-message"></a>Mciwndm \_ GetLength-Nachricht

Die **mciwndm \_ GetLength** -Nachricht Ruft die Länge des Inhalts oder der Datei ab, die derzeit von einem MCI-Gerät verwendet wird. Sie können diese Nachricht explizit oder mit dem [**mciwndgetlength**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetlength) -Makro senden.


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
| Header<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Mciwndgetlength**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetlength)
</dt> </dl>

 

 





