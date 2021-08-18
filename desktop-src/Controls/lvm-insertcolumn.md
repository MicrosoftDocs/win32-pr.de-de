---
title: LVM_INSERTCOLUMN (Commctrl.h)
description: Fügt eine neue Spalte in ein Listenansicht-Steuerelement ein. Sie können diese Nachricht explizit oder mithilfe des \_ InsertColumn-Makros ListView senden.
ms.assetid: 1326e38e-bb45-4d0d-b5bc-ec684b3b92ef
keywords:
- LVM_INSERTCOLUMN meldungssteuerelemente Windows
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
ms.openlocfilehash: c5c2316ed2a74c82cd4530eff2d71d4771f4042b903c7ee17fc62886009ed5b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019238"
---
# <a name="lvm_insertcolumn-message"></a>LVM \_ INSERTCOLUMN-Meldung

Fügt eine neue Spalte in ein Listenansicht-Steuerelement ein. Sie können diese Nachricht explizit oder mithilfe des [**\_ InsertColumn-Makros ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertcolumn) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Index der neuen Spalte.

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**LVCOLUMN-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) die die Attribute der neuen Spalte enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg den Index der neuen Spalte zurück, andernfalls -1.

## <a name="remarks"></a>Hinweise

Spalten sind nur in der Berichtsansicht (Details) sichtbar.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





