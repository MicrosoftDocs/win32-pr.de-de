---
description: Die \_ hinzugefügte WM-Tablet- \_ Nachricht wird gesendet, wenn Windows ein Tablet-Gerät hinzugefügt wird.
ms.assetid: 74323b34-2364-47eb-b8ac-b97546e43b32
title: WM_TABLET_ADDED Meldung (tpcshrd. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a721f83cbab3c520a5502fa2f1262de9a26b25a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346931"
---
# <a name="wm_tablet_added-message"></a>\_Hinzugefügte WM-Tablette \_

Die **\_ \_ hinzugefügte WM-Tablet** -Nachricht wird gesendet, wenn Windows ein Tablet-Gerät hinzugefügt wird.


```C++
#define WM_TABLET_DEFBASE  0x02C0
#define WM_TABLET_ADDED    (WM_TABLET_DEFBASE + 8)      
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der Index des hinzugefügten Tablettgeräts.

</dd> <dt>

*lParam* 
</dt> <dd>

Nicht verwendet.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Nachricht wird an alle Fenster der obersten Ebene im System gesendet, darunter deaktivierte oder nicht sichtbare, nicht im Besitz befindliche Fenster, überlappende Fenster und Popup Fenster. die Meldung wird jedoch nicht an untergeordnete Fenster gesendet.

Die Indizes, die in *wParam* übergeben werden, sind mit dem Index verknüpft, der von der [**itabletmanager:: gettablet**](/previous-versions/windows/desktop/legacy/aa373683(v=vs.85)) -Methode verwendet wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                        |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                            |
| Header<br/>                   | <dl> <dt>Tpcshrd. h</dt> </dl> |



 

 
