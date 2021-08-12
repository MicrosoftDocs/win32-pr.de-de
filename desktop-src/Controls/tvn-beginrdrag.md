---
title: TVN_BEGINRDRAG Benachrichtigungscode (Commctrl.h)
description: Benachrichtigt das übergeordnete Fenster eines Strukturansichtssteuerelements über die Initiierung eines Drag & Drop-Vorgangs mit der rechten Maustaste. Dieser Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet.
ms.assetid: 4a61d8b5-ceb9-46a3-95ef-27e843e8c986
keywords:
- TVN_BEGINRDRAG Benachrichtigungscode Windows-Steuerelemente
topic_type:
- apiref
api_name:
- TVN_BEGINRDRAG
- TVN_BEGINRDRAGA
- TVN_BEGINRDRAGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f7ce3fb92f39097c51cf54d707fac4341bc2a4c098b5abb0b36abcbd47f5744
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118669174"
---
# <a name="tvn_beginrdrag-notification-code"></a>TVN \_ BEGINRDRAG-Benachrichtigungscode

Benachrichtigt das übergeordnete Fenster eines Strukturansichtssteuerelements über die Initiierung eines Drag & Drop-Vorgangs mit der rechten Maustaste. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
TVN_BEGINRDRAG 

    pnmtv = (LPNMTREEVIEW) lParam 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**NMTREEVIEW-Struktur.**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) Der **itemNew-Member** ist eine [**TVITEM-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-tvitema) die gültige Informationen in den **Membern hItem,** **state** und **lParam** über das zu ziehende Element enthält. Das **ptDrag-Element** gibt die aktuellen Bildschirmkoordinaten der Maus an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert wird ignoriert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **TVN \_ BEGINRDRAGW** (Unicode) und **TVN \_ BEGINRDRAGA** (ANSI)<br/>             |



 

 





