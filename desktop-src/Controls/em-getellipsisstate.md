---
title: EM_GETELLIPSISSTATE Meldung (RichEdit. h)
description: Ruft den aktuellen Ellipsen Zustand ab.
ms.assetid: D02AE225-F5BF-401A-9877-55C68946CDBE
keywords:
- Windows-Steuerelemente für EM_GETELLIPSISSTATE Meldung
topic_type:
- apiref
api_name:
- EM_GETELLIPSISSTATE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 905bc8ecc180189f46e896aa0d9aaa3ba88b3f0b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476833"
---
# <a name="em_getellipsisstate-message"></a>EM \_ getellipsisstate-Meldung

Ruft den aktuellen Ellipsen Zustand ab.


```C++
#define EM_GETELLIPSISSTATE       (WM_USER + 322)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Nicht verwendet; muss 0 (null) sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Nicht verwendet; muss 0 (null) sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist true, wenn ein Auslassungs Zeichen angezeigt wird, andernfalls false.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**EM \_ getellipsismode**](em-getellipsismode.md)
</dt> <dt>

[**EM/ \_ tellipsismode**](em-setellipsismode.md)
</dt> </dl>

 

 





