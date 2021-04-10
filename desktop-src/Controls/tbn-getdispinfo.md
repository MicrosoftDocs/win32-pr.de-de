---
title: TBN_GETDISPINFO Benachrichtigungs Code (kommctrl. h)
description: Ruft Anzeigeinformationen für ein Symbolleisten Element ab. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: ed6e4141-2bf8-4a92-8349-f3833c87fcf3
keywords:
- Windows-Steuerelemente für TBN_GETDISPINFO Benachrichtigungs
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5f3a0a47adfe7f172f7a4d0e4c9139b67aef01d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105027"
---
# <a name="tbn_getdispinfo-notification-code"></a>TBN- \_ getdispinfo-Benachrichtigungs Code

Ruft Anzeigeinformationen für ein Symbolleisten Element ab. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.


```C++
TBN_GETDISPINFO 

    lptbdi = (LPNMTBDISPINFO) lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**nmtbdispinfo**](/windows/desktop/api/Commctrl/ns-commctrl-nmtbdispinfoa) -Struktur. Der **idcommand** -Member gibt den Befehls Bezeichner des Elements an, das **LPARAM** -Element enthält die Anwendungs definierten Daten des Elements, und der **dwMask** -Member gibt an, welche Informationen angefordert werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert wird vom-Steuerelement ignoriert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **TBN \_ Getdispinfow** (Unicode) und **TBN \_ getdispinfoa** (ANSI)<br/>           |



 

 





