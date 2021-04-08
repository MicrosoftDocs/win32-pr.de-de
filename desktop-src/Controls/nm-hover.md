---
title: NM_HOVER Benachrichtigungs Code (kommctrl. h)
description: Wird von einem Steuerelement gesendet, wenn mit dem Mauszeiger auf ein Element gezeigt wird. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 0eef3e88-c1f0-4f9c-9ccf-580d8e464157
keywords:
- Windows-Steuerelemente für NM_HOVER Benachrichtigungs
topic_type:
- apiref
api_name:
- NM_HOVER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69344b1aae78ebee99b86c78f4442df20f66187a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739928"
---
# <a name="nm_hover-notification-code"></a>NM- \_ Hover-Benachrichtigungs Code

Wird von einem Steuerelement gesendet, wenn mit dem Mauszeiger auf ein Element gezeigt wird. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.


```C++
NM_HOVER

    lpnmh = (LPNMHDR) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) -Struktur, die zusätzliche Informationen zu dieser Benachrichtigung enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Sofern nicht anders angegeben, wird NULL zurückgegeben, damit das Steuerelement den Mauszeiger Normal verarbeiten kann, oder ungleich NULL, um zu verhindern, dass der Mauszeiger verarbeitet wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





