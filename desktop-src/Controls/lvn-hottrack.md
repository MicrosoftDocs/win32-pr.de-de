---
title: LVN_HOTTRACK Benachrichtigungs Code (kommctrl. h)
description: Wird von einem Listenansicht-Steuerelement gesendet, wenn der Benutzer die Maus über ein Element bewegt. Dieser Benachrichtigungs Code wird nur von Listenansicht-Steuerelementen gesendet, die über den erweiterten LVS \_ Ex \_ trackselect-Listen Ansichts Stil verfügen. Sie wird in Form einer WM- \_ Benachrichtigungs Meldung gesendet.
ms.assetid: 6bbfe6b8-9b67-49e4-9481-65abe98608bb
keywords:
- Windows-Steuerelemente für LVN_HOTTRACK Benachrichtigungs
topic_type:
- apiref
api_name:
- LVN_HOTTRACK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c677b69fa21cdbe3680442304f6745cfb3a907de
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859345"
---
# <a name="lvn_hottrack-notification-code"></a>LVN \_ HotTrack-Benachrichtigungs Code

Wird von einem Listenansicht-Steuerelement gesendet, wenn der Benutzer die Maus über ein Element bewegt. Dieser Benachrichtigungs Code wird nur von Listenansicht-Steuerelementen gesendet, die über den erweiterten [**LVS \_ Ex \_ trackselect**](extended-list-view-styles.md) -Listen Ansichts Stil verfügen. Sie wird in Form einer [**WM- \_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.


```C++
LVN_HOTTRACK

    lpnmlv = (LPNMLISTVIEW) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) -Struktur, die Informationen zu diesem Benachrichtigungs Code enthält. Die Member **iItem**, **iSubItem** und **ptaction** dieser Struktur enthalten Informationen über das Element. Die empfangende Anwendung kann den **iItem** -Member ändern, um das Element anzugeben, das ausgewählt wird. Wenn **iItem** auf-1 festgelegt ist, wird kein Element ausgewählt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

0 (null) zurückgeben, damit die Listenansicht den normalen Track-Prozess ausführen kann. Wenn die Anwendung einen Wert ungleich 0 (null) zurückgibt, wird das Element nicht ausgewählt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





