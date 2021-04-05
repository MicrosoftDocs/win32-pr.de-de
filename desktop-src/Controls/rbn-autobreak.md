---
title: RBN_AUTOBREAK Meldung (kommstrg. h)
description: Benachrichtigt das übergeordnete Element einer übergeordneten Leiste, dass eine Unterbrechung in der Leiste angezeigt wird. Das übergeordnete Element bestimmt, ob die Unterbrechung vorgenommen werden soll. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: b7a63027-6cfa-4d5a-9ea6-fdd8b4fb6864
keywords:
- Windows-Steuerelemente für RBN_AUTOBREAK Meldung
topic_type:
- apiref
api_name:
- RBN_AUTOBREAK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d614277d89578cb66e528ba16656ed55681ebbcf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859277"
---
# <a name="rbn_autobreak-message"></a>RBN- \_ Meldung zum autobreak

Benachrichtigt das übergeordnete Element einer übergeordneten [Leiste](rebar-controls.md) , dass eine Unterbrechung in der Leiste angezeigt wird. Das übergeordnete Element bestimmt, ob die Unterbrechung vorgenommen werden soll. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.


```C++
RBN_AUTOBREAK

    pnmRebarAutoBreak = (LPNMREBARAUTOBREAK) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**nmrebarautobreak**](/windows/win32/api/commctrl/ns-commctrl-nmrebarautobreak) -Struktur, die Informationen über den Benachrichtigungs Code enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert für diese Benachrichtigung wird nicht verwendet.

## <a name="remarks"></a>Bemerkungen

Der Wert im **fautobreak** -Member der [**nmrebarautobreak**](/windows/win32/api/commctrl/ns-commctrl-nmrebarautobreak) -Struktur gibt an, ob eine Unterbrechung in der Info Leiste auftreten soll.

Geben Sie Comctl32.dll Version 6 im Manifest an, um diesen Benachrichtigungs Code zu verwenden. Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen](cookbook-overview.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





