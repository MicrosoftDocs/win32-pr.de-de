---
title: LVM_SETCOLUMN-Nachricht (Commctrl.h)
description: Legt die Attribute einer Listenansichtsspalte fest. Sie können diese Nachricht explizit oder mithilfe des ListView \_ SetColumn-Makros senden.
ms.assetid: 8ca1c269-fd86-4561-940d-b75f8ca2b731
keywords:
- LVM_SETCOLUMN Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- LVM_SETCOLUMN
- LVM_SETCOLUMNW
- LVM_SETCOLUMNW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cca00e62d941a753c70e0dd31c1af4003fe639d49503be7009fe5a010febf0c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019218"
---
# <a name="lvm_setcolumn-message"></a>LVM \_ SETCOLUMN-Nachricht

Legt die Attribute einer Listenansichtsspalte fest. Sie können diese Nachricht explizit oder mithilfe des [**ListView \_ SetColumn-Makros**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setcolumn) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Index der Spalte.

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**LVCOLUMN-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) die die neuen Spaltenattribute enthält. Der **Maskenmember** gibt an, welche Spaltenattribute festgelegt werden sollen. Wenn der **Maskenmember** den LVCF \_ TEXT-Wert angibt, ist der **pszText-Member** die Adresse einer auf NULL endenden Zeichenfolge, und der **cchTextMax-Member** wird ignoriert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE** zurück, wenn erfolgreich, **andernfalls FALSE.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **LVM \_ SETCOLUMNW** (Unicode) und **LVM \_ SETCOLUMNW** (ANSI)<br/>               |



 

 





