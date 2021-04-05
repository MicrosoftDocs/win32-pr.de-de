---
title: NM_CLICK (Symbolleisten-) Benachrichtigungs Code (kommstrg. h)
description: Wird von einem ToolBar-Steuerelement gesendet, wenn der Benutzer mit der linken Maustaste auf ein Element klickt. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: fa43c9bc-db2a-4460-b193-2b4694d06d83
keywords:
- NM_CLICK (Symbolleiste) Benachrichtigungs Code Windows-Steuerelemente
topic_type:
- apiref
api_name:
- NM_CLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca31e3553327c94d371617d016a85395519c211d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859339"
---
# <a name="nm_click-toolbar-notification-code"></a>NM \_ Click (Symbolleisten)-Benachrichtigungs Code

Wird von einem ToolBar-Steuerelement gesendet, wenn der Benutzer mit der linken Maustaste auf ein Element klickt. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.


```C++
NM_CLICK

    lpnm = (LPNMMOUSE) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**nmmouse**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) -Struktur, die zusätzliche Informationen zu dieser Benachrichtigung enthält. Der **dwitemspec** -Member enthält den Index des Abschnitts, auf den geklickt wurde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, um anzugeben, dass der Maus Klick behandelt wurde, und unterdrückt die Standard Verarbeitung durch das System. Gibt **false** zurück, um die Standard Verarbeitung des Click zuzulassen.

## <a name="remarks"></a>Bemerkungen

Wenn Sie mit der linken Maustaste auf ein Element klicken, sendet die Symbolleiste eine [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Nachricht, bei der der auf das übergeordnete Fenster [ \_ geklickt](bn-clicked.md) hat. Die nm- \_ Click-Benachrichtigung wird nach der **WM- \_ Befehls** Meldung gesendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

