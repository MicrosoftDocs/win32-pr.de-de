---
title: TRBN_THUMBPOSCHANGING Benachrichtigungs Code (kommctrl. h)
description: Benachrichtigt, dass sich die Position des Zieh Punkts auf einer TrackBar ändert. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 0876e026-bc07-409d-b174-b97ed704fc11
keywords:
- Windows-Steuerelemente für TRBN_THUMBPOSCHANGING Benachrichtigungs
topic_type:
- apiref
api_name:
- TRBN_THUMBPOSCHANGING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f23722b68f28a5157948ac6277858193366242fe
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "103961405"
---
# <a name="trbn_thumbposchanging-notification-code"></a>Trbn- \_ thumbposchanging-Benachrichtigungs Code

Benachrichtigt, dass sich die Position des Zieh Punkts auf einer TrackBar ändert. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.


```C++
TRBN_THUMBPOSCHANGING

    lpNMTrbThumbPosChanging = (NMTRBTHUMBPOSCHANGING*) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**nmtrbthumbposchanging**](/windows/win32/api/commctrl/ns-commctrl-nmtrbthumbposchanging) -Struktur. Der Aufrufer ist dafür verantwortlich, diese Struktur zuzuordnen und seine Member festzulegen, einschließlich der Member der enthaltenen [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) -Struktur.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, um zu verhindern, dass der Ziehpunkt an die angegebene Position verschoben wird.

## <a name="remarks"></a>Bemerkungen

Senden Sie diese Benachrichtigung an Clients, die nicht auf " [**WM \_ HScroll**](wm-hscroll.md) "-oder " [**WM \_ VScroll**](wm-vscroll.md) "-Nachrichten lauschen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





