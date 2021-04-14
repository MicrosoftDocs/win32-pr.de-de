---
title: TBN_DRAGOVER Benachrichtigungs Code (kommctrl. h)
description: Gibt an, ob eine TB- \_ markbutton-Nachricht für eine Schaltfläche gesendet werden soll, die gezogen wird. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 2bb5c52e-0c90-4662-8ffd-045ecc7ed7e5
keywords:
- Windows-Steuerelemente für TBN_DRAGOVER Benachrichtigungs
topic_type:
- apiref
api_name:
- TBN_DRAGOVER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfa02aa8fabf89ea27fce628d3d63165255bbd66
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475903"
---
# <a name="tbn_dragover-notification-code"></a>TBN- \_ DragOver-Benachrichtigungs Code

Gibt an, ob eine [**TB- \_ markbutton**](tb-markbutton.md) -Nachricht für eine Schaltfläche gesendet werden soll, die gezogen wird. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.


```C++
TBN_DRAGOVER

    lpnmtb = (NMTBHOTITEM*) lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**nmtbhutitem**](/windows/win32/api/commctrl/ns-commctrl-nmtbhotitem) -Struktur, die angibt, auf welches Element gezogen wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

**False** , wenn die Symbolleiste eine TB- \_ markbutton-Nachricht senden soll; andernfalls **true**.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





