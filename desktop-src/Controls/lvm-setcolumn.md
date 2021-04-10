---
title: LVM_SETCOLUMN Meldung (kommstrg. h)
description: Legt die Attribute einer Listen Ansichts Spalte fest. Sie können diese Nachricht explizit oder mithilfe des ListView- \_ Makros SetColumn senden.
ms.assetid: 8ca1c269-fd86-4561-940d-b75f8ca2b731
keywords:
- Windows-Steuerelemente für LVM_SETCOLUMN Meldung
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
ms.openlocfilehash: 7251da70c7ac1e2cb7bbcf7b3e220a2f6cdf055f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956504"
---
# <a name="lvm_setcolumn-message"></a>LVM- \_ SetColumn-Nachricht

Legt die Attribute einer Listen Ansichts Spalte fest. Sie können diese Nachricht explizit oder mithilfe des [**ListView-Makros \_ SetColumn**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setcolumn) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der Index der Spalte.

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**LVCOLUMN**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) -Struktur, die die neuen Spalten Attribute enthält. Der **Mask** -Member gibt an, welche Spalten Attribute festgelegt werden sollen. Wenn das **Mask** -Element den "lvcf" \_ -Textwert angibt, ist das **pszText** -Element die Adresse einer auf NULL endenden Zeichenfolge, und der **cchtextmax** -Member wird ignoriert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **LVM \_ Setcolumnw** (Unicode) und **LVM \_ setcolumnw** (ANSI)<br/>               |



 

 





