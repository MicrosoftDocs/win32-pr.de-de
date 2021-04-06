---
title: LVM_GETITEM Meldung (kommstrg. h)
description: Ruft einige oder alle der Attribute eines Listen Ansichts Elements ab. Sie können diese Nachricht explizit oder mithilfe des ListView \_ GetItem-Makros senden.
ms.assetid: 684ad96a-2c3b-4148-b66c-41f8322500bb
keywords:
- Windows-Steuerelemente für LVM_GETITEM Meldung
topic_type:
- apiref
api_name:
- LVM_GETITEM
- LVM_GETITEMA
- LVM_GETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c19632567db5e37059b1b028a8ec1fc9385268cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742993"
---
# <a name="lvm_getitem-message"></a>LVM- \_ GetItem-Nachricht

Ruft einige oder alle der Attribute eines Listen Ansichts Elements ab. Sie können diese Nachricht explizit oder mithilfe des [**ListView \_ GetItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitem) -Makros senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**lvitem**](/windows/win32/api/commctrl/ns-commctrl-lvitema) -Struktur, die die Informationen angibt, die abgerufen werden sollen, und Informationen über das Listen Ansichts Element empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .

## <a name="remarks"></a>Bemerkungen

Wenn die **LVM \_ GetItem** -Nachricht gesendet wird, identifizieren die **iItem** -und **iSubItem** -Member das Element oder Unterelement, über das Informationen abgerufen werden sollen, und das **Masken** Element gibt an, welche Attribute abgerufen werden sollen. Eine Liste möglicher Werte finden Sie in der Beschreibung der [**lvitem**](/windows/win32/api/commctrl/ns-commctrl-lvitema) -Struktur.

Wenn das lvif- \_ textflag im **Mask** -Member der [**lvitem**](/windows/win32/api/commctrl/ns-commctrl-lvitema) -Struktur festgelegt ist, muss der **pszText** -Member auf einen gültigen Puffer zeigen, und das **cchtextmax** -Element muss auf die Anzahl der Zeichen in diesem Puffer festgelegt werden. Anwendungen sollten nicht davon ausgehen, dass der Text notwendigerweise in den angegebenen Puffer eingefügt wird. Das-Steuerelement kann stattdessen den **pszText** -Member der-Struktur ändern, sodass er auf den neuen Text verweist, anstatt ihn in den Puffer zu platzieren.

Wenn das **Masken** Element den lvif- \_ Zustandswert angibt, muss der **statemask** -Member die abzurufenden Element Zustands Bits angeben. Bei **der Ausgabe** enthält das statusmember die Werte der angegebenen Zustands Bits.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **LVM \_ Getitemw** (Unicode) und **LVM \_ getitema** (ANSI)<br/>                   |



 

 





