---
title: LVM_SETITEM Meldung (Commctrl.h)
description: Legt einige oder alle Attribute eines Listenansichtselements fest. Sie können LVM \_ SETITEM auch senden, um den Text eines Unteritems festzulegen. Sie können diese Nachricht explizit oder mithilfe des ListView \_ SetItem-Makros senden.
ms.assetid: f1189b5d-bce7-4569-b4b9-bd750d7ef505
keywords:
- LVM_SETITEM Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- LVM_SETITEM
- LVM_SETITEMA
- LVM_SETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83ccc47c27ff05e75ba2633e18363c3e26e844c359b54d009101512fc837b668
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019158"
---
# <a name="lvm_setitem-message"></a>LVM \_ SETITEM-Nachricht

Legt einige oder alle Attribute eines Listenansichtselements fest. Sie können LVM \_ SETITEM auch senden, um den Text eines Unteritems festzulegen. Sie können diese Nachricht explizit oder mithilfe des [**ListView \_ SetItem-Makros**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitem) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**LVITEM-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-lvitema) die die neuen Elementattribute enthält. Die **Elemente iItem** und **iSubItem** identifizieren das Element oder Unterelement, und der **Maskenmember** gibt an, welche Attribute festgelegt werden sollen. Wenn der **Maskenmember** den LVIF \_ TEXT-Wert angibt, ist der **pszText-Member** die Adresse einer auf NULL endenden Zeichenfolge, und der **cchTextMax-Member** wird ignoriert. Wenn der **Maskenmember** den LVIF \_ STATE-Wert angibt, gibt der **stateMask-Member** an, welche Elementzustände geändert werden sollen, und das **Zustandselement** enthält die Werte für diese Zustände.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE** zurück, wenn erfolgreich, **andernfalls FALSE.**

## <a name="remarks"></a>Hinweise

Um die Attribute eines Listenansichtselements festzulegen, legen Sie das **iItem-Element** der [**LVITEM-Struktur**](/windows/win32/api/commctrl/ns-commctrl-lvitema) auf den Index des Elements und das **iSubItem-Element** auf 0 (null) fest. Für ein Element können Sie die **Member state,** **pszText,** **iImage** und **lParam** der **LVITEM-Struktur** festlegen.

Um den Text eines Unteritems festzulegen, legen Sie die Elemente **iItem** und **iSubItem** fest, um das bestimmte Unteritem anzugeben, und verwenden Sie das **pszText-Element,** um den Text anzugeben. Alternativ können Sie das [**ListView \_ SetItemText-Makro**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemtext) verwenden, um den Text eines Unteritems festzulegen. Sie können den **Zustand** oder die **lParam-Member** für Unteritems nicht festlegen, da untere Elemente nicht über diese Attribute verfügen. In Version 4.70 und höher können Sie das **iImage-Element** für Unteritems festlegen. Das Unterelementbild wird angezeigt, wenn das Listenansichtssteuerelement über den erweiterten [**LVS \_ EX \_ SUBITEMIMAGES-Stil**](extended-list-view-styles.md) verfügt. Frühere Versionen ignorieren das Unteritemimage.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **LVM \_ SETITEMW** (Unicode) und **LVM \_ SETITEMA** (ANSI)<br/>                   |



 

 





