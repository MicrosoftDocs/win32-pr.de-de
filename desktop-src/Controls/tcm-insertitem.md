---
title: TCM_INSERTITEM Meldung (kommstrg. h)
description: Fügt eine neue Registerkarte in ein Registerkarten-Steuerelement ein. Sie können diese Nachricht explizit oder mithilfe des tabctrl \_ InsertItem-Makros senden.
ms.assetid: e547c49a-699c-4137-8680-20391d138d54
keywords:
- Windows-Steuerelemente für TCM_INSERTITEM Meldung
topic_type:
- apiref
api_name:
- TCM_INSERTITEM
- TCM_INSERTITEMA
- TCM_INSERTITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58002006944a221571e37c37d25259d0aaa74fc4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106343873"
---
# <a name="tcm_insertitem-message"></a>TCM \_ InsertItem-Nachricht

Fügt eine neue Registerkarte in ein Registerkarten-Steuerelement ein. Sie können diese Nachricht explizit oder mithilfe des [**tabctrl \_ InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_insertitem) -Makros senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Index der neuen Registerkarte.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) -Struktur, die die Attribute der Registerkarte angibt. Die Member **dwstate** und **dwstatemask** dieser Struktur werden von dieser Nachricht ignoriert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den Index der neuen Registerkarte zurück, wenn erfolgreich, andernfalls-1.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **TCM \_ Insertitemw** (Unicode) und **TCM \_ insertitema** (ANSI)<br/>             |



 

 





