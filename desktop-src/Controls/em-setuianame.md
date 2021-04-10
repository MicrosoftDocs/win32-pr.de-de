---
title: EM_SETUIANAME Meldung (RichEdit. h)
description: Legt den Namen eines Rich-Edit-Steuer Elements für die Benutzeroberflächen Automatisierung (UIA) fest.
ms.assetid: 60506FEE-9708-4668-8846-42B0B696DD9A
keywords:
- Windows-Steuerelemente für EM_SETUIANAME Meldung
topic_type:
- apiref
api_name:
- EM_SETUIANAME
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0102b792a9eccfc6116acc3a534b00fb64b7ee5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956634"
---
# <a name="em_setuianame-message"></a>EM * \_ tuianame-Meldung

Legt den Namen eines Rich-Edit-Steuer Elements für die Benutzeroberflächen Automatisierung (UIA) fest.


```C++
#define EM_SETUIANAME       (WM_USER + 320)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Nicht verwendet; muss 0 (null) sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf die NULL-terminierte namens Zeichenfolge.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

TRUE, wenn der Name für die UIA erfolgreich festgelegt wurde, andernfalls false.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



 

 





