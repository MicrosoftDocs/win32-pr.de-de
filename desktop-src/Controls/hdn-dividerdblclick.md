---
title: HDN_DIVIDERDBLCLICK Benachrichtigungs Code (kommctrl. h)
description: Benachrichtigt das übergeordnete Fenster eines Header Steuer Elements, dass der Benutzer auf den unter Teiler des-Steuer Elements Doppel geklickt hat. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: b722196a-23ae-49c3-b0a2-8fe0d1e33b26
keywords:
- Windows-Steuerelemente für HDN_DIVIDERDBLCLICK Benachrichtigungs
topic_type:
- apiref
api_name:
- HDN_DIVIDERDBLCLICK
- HDN_DIVIDERDBLCLICKA
- HDN_DIVIDERDBLCLICKW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0129096139a4d698f25de543a2628b473bfd66e2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104041020"
---
# <a name="hdn_dividerdblclick-notification-code"></a>Hdn \_ dividerdblclick-Benachrichtigungs Code

Benachrichtigt das übergeordnete Fenster eines Header Steuer Elements, dass der Benutzer auf den unter Teiler des-Steuer Elements Doppel geklickt hat. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.


```C++
HDN_DIVIDERDBLCLICK

    pNMHeader = (LPNMHEADER) lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) -Struktur, die Informationen über das Header Steuerelement und das Element enthält, auf das Doppel geklickt wurde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **Hdn \_ Dividerdblclickw** (Unicode) und **Hdn \_ dividerdblclicka** (ANSI)<br/>   |



 

 





