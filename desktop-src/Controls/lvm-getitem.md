---
title: LVM_GETITEM Meldung (Commctrl.h)
description: Ruft einige oder alle Attribute eines Listenansichtselements ab. Sie können diese Nachricht explizit oder mithilfe des ListView \_ GetItem-Makros senden.
ms.assetid: 684ad96a-2c3b-4148-b66c-41f8322500bb
keywords:
- LVM_GETITEM Windows-Steuerelemente für Nachrichten
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
ms.openlocfilehash: 05338abce0396c5cc527c8a1c04176b3b59243a684c66a263cb190d59ac68b98
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088900"
---
# <a name="lvm_getitem-message"></a>LVM \_ GETITEM-Nachricht

Ruft einige oder alle Attribute eines Listenansichtselements ab. Sie können diese Nachricht explizit oder mithilfe des [**ListView \_ GetItem-Makros**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitem) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**LVITEM-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-lvitema) die die abzurufenden Informationen angibt und Informationen über das Listenansichtselement empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE** zurück, wenn erfolgreich, **andernfalls FALSE.**

## <a name="remarks"></a>Hinweise

Wenn die **LVM \_ GETITEM-Nachricht** gesendet wird, identifizieren die **Elemente iItem** und **iSubItem** das Element oder Unterelement, zu dem Informationen abgerufen werden sollen, und der **Maskenmember** gibt an, welche Attribute abgerufen werden sollen. Eine Liste der möglichen Werte finden Sie in der Beschreibung der [**LVITEM-Struktur.**](/windows/win32/api/commctrl/ns-commctrl-lvitema)

Wenn das LVIF \_ TEXT-Flag im **Maskenmember** der [**LVITEM-Struktur**](/windows/win32/api/commctrl/ns-commctrl-lvitema) festgelegt ist, muss der **pszText-Member** auf einen gültigen Puffer zeigen, und das **cchTextMax-Element** muss auf die Anzahl der Zeichen in diesem Puffer festgelegt werden. Anwendungen sollten nicht davon ausgehen, dass der Text notwendigerweise im angegebenen Puffer platziert wird. Das Steuerelement kann stattdessen den **pszText-Member** der -Struktur so ändern, dass er auf den neuen Text verweist, anstatt ihn im Puffer zu platzieren.

Wenn der **Maskenmember** den LVIF \_ STATE-Wert angibt, muss der **stateMask-Member** die abzurufenden Elementzustandsbits angeben. Bei der Ausgabe enthält der **Zustandsmember** die Werte der angegebenen Zustandsbits.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **LVM \_ GETITEMW** (Unicode) und **LVM \_ GETITEMA** (ANSI)<br/>                   |



 

 





