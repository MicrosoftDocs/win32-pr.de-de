---
title: LVM_INSERTCOLUMN Meldung (kommstrg. h)
description: Fügt eine neue Spalte in ein Listenansicht-Steuerelement ein. Sie können diese Nachricht explizit oder mithilfe des ListView \_ InsertColumn-Makros senden.
ms.assetid: 1326e38e-bb45-4d0d-b5bc-ec684b3b92ef
keywords:
- Windows-Steuerelemente für LVM_INSERTCOLUMN Meldung
topic_type:
- apiref
api_name:
- LVM_INSERTCOLUMN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8be89ff0b4ef417a715085582544112cb90cb6b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518647"
---
# <a name="lvm_insertcolumn-message"></a>LVM- \_ InsertColumn-Meldung

Fügt eine neue Spalte in ein Listenansicht-Steuerelement ein. Sie können diese Nachricht explizit oder mithilfe des [**ListView \_ InsertColumn**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertcolumn) -Makros senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Index der neuen Spalte.

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**LVCOLUMN**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) -Struktur, die die Attribute der neuen Spalte enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den Index der neuen Spalte zurück, wenn erfolgreich, andernfalls-1.

## <a name="remarks"></a>Bemerkungen

Spalten sind nur in der Berichtsansicht (Details) sichtbar.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





