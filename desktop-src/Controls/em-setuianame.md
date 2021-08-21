---
title: EM_SETUIANAME (Richedit.h)
description: Legt den Namen eines Rich-Edit-Steuerelements für Benutzeroberflächenautomatisierung (UIA) fest.
ms.assetid: 60506FEE-9708-4668-8846-42B0B696DD9A
keywords:
- EM_SETUIANAME von Windows-Steuerelementen
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
ms.openlocfilehash: 603d59b7bf246ee8ed7987d42399281ac1b0520ef27e206f2f8eeddf8f363d87
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118412325"
---
# <a name="em_setuianame-message"></a>EM \_ SETUIANAME-Meldung

Legt den Namen eines Rich-Edit-Steuerelements für Benutzeroberflächenautomatisierung (UIA) fest.


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

Ein Zeiger auf die auf NULL beendete Namenszeichenfolge.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

TRUE, wenn der Name für UIA erfolgreich festgelegt wurde, andernfalls FALSE.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



 

 





