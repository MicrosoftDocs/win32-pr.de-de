---
title: EN_PARAGRAPHEXPANDED Benachrichtigungs Code (RichEdit. h)
description: Benachrichtigt das übergeordnete Element eines Rich-Edit-Steuer Elements, dass eine Gliederung erweitert wurde. Ein Rich Edit-Steuerelement sendet diesen Benachrichtigungs Code in Form einer WM-Benachrichtigungs \_ Meldung.
ms.assetid: D33EB118-FC79-4284-820B-3424F13722C4
keywords:
- Windows-Steuerelemente für EN_PARAGRAPHEXPANDED Benachrichtigungs
topic_type:
- apiref
api_name:
- EN_PARAGRAPHEXPANDEDC
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f862260c0653d23b0b53649a2c05e59820e3808
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476980"
---
# <a name="en_paragraphexpanded-notification-code"></a>EN \_ paragrapherweiterter Benachrichtigungs Code

Benachrichtigt das übergeordnete Element eines Rich-Edit-Steuer Elements, dass eine Gliederung erweitert wurde. Ein Rich Edit-Steuerelement sendet diesen Benachrichtigungs Code in Form einer WM-Benachrichtigungs Meldung. [**\_**](wm-notify.md)


```C++
EN_PARAGRAPHEXPANDED

    lpnmhdr = (LPNMHDR) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Eine [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) -Struktur.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



 

 





