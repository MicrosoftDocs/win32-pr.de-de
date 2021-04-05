---
title: TVN_SELCHANGED Benachrichtigungs Code (kommctrl. h)
description: Benachrichtigt das übergeordnete Fenster eines Strukturansicht-Steuer Elements, dass sich die Auswahl von einem Element in ein anderes geändert hat. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 682170d3-5843-4d92-afeb-c37f3502ed5d
keywords:
- Windows-Steuerelemente für TVN_SELCHANGED Benachrichtigungs
topic_type:
- apiref
api_name:
- TVN_SELCHANGED
- TVN_SELCHANGEDA
- TVN_SELCHANGEDW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a564ec039e179d03dda9edc19d6de3412cd5361a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859231"
---
# <a name="tvn_selchanged-notification-code"></a>Geänderter TVN- \_ Benachrichtigungs Code

Benachrichtigt das übergeordnete Fenster eines Strukturansicht-Steuer Elements, dass sich die Auswahl von einem Element in ein anderes geändert hat. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.


```C++
TVN_SELCHANGED 

    pnmtv = (LPNMTREEVIEW) lParam 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**nmtreeview**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) -Struktur. Die **itemold** -und **itemnew** -Member der **nmtreeview** -Struktur sind [**tvitem**](/windows/win32/api/commctrl/ns-commctrl-tvitema) -Strukturen, die Informationen über das zuvor ausgewählte Element und das neu ausgewählte Element enthalten. Nur die Member " **Mask**", " **Hitem**", " **State**" und " **LPARAM** " sind gültig. Die " **Status Ask** "-Member der **tvitem** -Strukturen, die von **itemold** und **itemnew** angegeben werden, sind bei der Eingabe nicht definiert. Der **Action** -Member der **nmtreeview** -Struktur gibt den Typ der Aktion an, die bewirkt hat, dass die Auswahl geändert wurde. Es kann sich um einen der folgenden Werte handeln:



| Anforderung | Wert |
|-----------------|-------------------|
| TVC- \_ bykeyboard | Per Tastatureingabe.   |
| TVC- \_ bymouse    | Per Mausklick. |
| TVC \_ unbekannt    | Unbekannt          |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert wird ignoriert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **TVN \_ Selchangedw** (Unicode) und **TVN \_ selchangeda** (ANSI)<br/>             |



 

 





