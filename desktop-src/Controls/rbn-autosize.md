---
title: RBN_AUTOSIZE Benachrichtigungs Code (kommctrl. h)
description: Wird von einem Grund leisten-Steuerelement gesendet, das mit der automatischen Größenanpassung von RB erstellt wird, \_ Wenn sich der grundbalken automatisch ändert. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: d174fe99-13cc-404c-9dc5-d5a93e9807a2
keywords:
- Windows-Steuerelemente für RBN_AUTOSIZE Benachrichtigungs
topic_type:
- apiref
api_name:
- RBN_AUTOSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18ecfac5a4f84d69d444c25a24956cb911fd90a4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340376"
---
# <a name="rbn_autosize-notification-code"></a>RBN- \_ Benachrichtigungs Code für automatische Größe

Wird von einem Grund leisten-Steuerelement gesendet, das mit der automatischen [**\_ Größenanpassung von RB**](rebar-control-styles.md) erstellt wird, wenn sich der grundbalken automatisch ändert. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.


```C++
RBN_AUTOSIZE

    lpnmas = (LPNMRBAUTOSIZE) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**nmrbauumsize**](/windows/win32/api/commctrl/ns-commctrl-nmrbautosize) -Struktur, die Informationen über den Vorgang zum Ändern der Größe enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert für diese Benachrichtigung wird nicht verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





