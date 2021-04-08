---
title: TCN_SELCHANGE Benachrichtigungs Code (kommctrl. h)
description: Benachrichtigt das übergeordnete Fenster eines Registerkarten-Steuer Elements, dass sich die derzeit ausgewählte Registerkarte geändert hat. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: f40e30f6-169b-4381-a300-12c3befb5fc5
keywords:
- Windows-Steuerelemente für TCN_SELCHANGE Benachrichtigungs
topic_type:
- apiref
api_name:
- TCN_SELCHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8578ac9fee7754b1ae27c05c6ec1b15636090040
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739864"
---
# <a name="tcn_selchange-notification-code"></a>TCN \_ selChange-Benachrichtigungs Code

Benachrichtigt das übergeordnete Fenster eines Registerkarten-Steuer Elements, dass sich die derzeit ausgewählte Registerkarte geändert hat. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.


```C++
TCN_SELCHANGE 

    lpnmhdr = (LPNMHDR) lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) -Struktur, die zusätzliche Informationen zu dieser Benachrichtigung enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Bemerkungen

Um die aktuell ausgewählte Registerkarte zu ermitteln, verwenden Sie das [**tabstrg \_ getcurrsel**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getcursel) -Makro.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[TCN \_ selchanging](tcn-selchanging.md)
</dt> </dl>

 

 





