---
title: CBEM_GETITEM Nachricht (Commctrl.h)
description: Ruft Elementinformationen für ein bestimmtes ComboBoxEx-Element ab.
ms.assetid: 2df07ae8-fa84-487c-a4a7-90244dfdb40e
keywords:
- CBEM_GETITEM Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- CBEM_GETITEM
- CBEM_GETITEMA
- CBEM_GETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dcf4dadf72a9f1fab679599c01c8fd0c6ca3541f2f77a5e8c52a740828966034
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119528060"
---
# <a name="cbem_getitem-message"></a>CBEM \_ GETITEM-Nachricht

Ruft Elementinformationen für ein bestimmtes ComboBoxEx-Element ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**COMBOBOXEXITEM-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) die die Elementinformationen empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg einen Wert ungleich 0 (null) zurück. Andernfalls wird 0 (null) zurückgegeben.

## <a name="remarks"></a>Hinweise

Wenn die Nachricht gesendet wird, müssen die **Elemente iItem** und **mask** der Struktur festgelegt werden, um den Index des Zielelements und den Typ der abzurufenden Informationen anzugeben. Andere Member werden nach Bedarf festgelegt. Um z. B. Text abzurufen, müssen Sie das CBEIF \_ TEXT-Flag in **der Maske** festlegen und **cchTextMax** einen Wert zuweisen. Wenn Sie das **iItem-Element** auf -1 festlegen, wird das im Bearbeitungssteuerelement angezeigte Element abgerufen.

Wenn das CBEIF \_ TEXT-Flag im **Maskenmember** der [**COMBOBOXEXITEM-Struktur**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) festgelegt ist, kann das Steuerelement den **pszText-Member** der -Struktur so ändern, dass er auf den neuen Text verweist, anstatt den Puffer mit dem angeforderten Text aufzufüllen. Anwendungen sollten nicht davon ausgehen, dass der Text immer im angeforderten Puffer platziert wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **CBEM \_ GETITEMW** (Unicode) und **CBEM \_ GETITEMA** (ANSI)<br/>                 |



 

 





