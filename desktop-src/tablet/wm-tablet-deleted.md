---
description: Die vom WM- \_ Tablet \_ gelöschte Nachricht wird gepostet, wenn ein Tablet-Gerät aus Windows entfernt wird.
ms.assetid: af5be7f0-a213-49a1-800e-c922281522c8
title: WM_TABLET_DELETED Meldung (tpcshrd. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da8ade03d199f8ee7a258b9db2aeea039fd725e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106354467"
---
# <a name="wm_tablet_deleted-message"></a>Vom WM- \_ Tablet \_ gelöschte Nachricht

Die vom **WM- \_ Tablet \_ Gelöschte** Nachricht wird gepostet, wenn ein Tablet-Gerät aus Windows entfernt wird.


```C++
#define WM_TABLET_DEFBASE   0x02C0
#define WM_TABLET_DELETED   (WM_TABLET_DEFBASE + 9)     
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der Index des zu entfernenden Tablet-Geräts.

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



 

 
