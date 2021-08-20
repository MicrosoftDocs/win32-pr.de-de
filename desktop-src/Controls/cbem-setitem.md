---
title: CBEM_SETITEM (Commctrl.h)
description: Legt die Attribute für ein Element in einem ComboBoxEx-Steuerelement fest.
ms.assetid: 752df8ea-fd5e-47fa-b729-d019bdde0904
keywords:
- CBEM_SETITEM von Windows-Steuerelementen
topic_type:
- apiref
api_name:
- CBEM_SETITEM
- CBEM_SETITEMA
- CBEM_SETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b1010c090283a47404ee93ef5f3bc1cf2d5ffe71a646d6d734cb443152bdd64
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119527930"
---
# <a name="cbem_setitem-message"></a>CBEM \_ SETITEM-Nachricht

Legt die Attribute für ein Element in einem ComboBoxEx-Steuerelement fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**COMBOBOXEXITEM-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) die die zu setzenden Elementinformationen enthält. Wenn die Nachricht gesendet wird, muss das **Maskenelement** der -Struktur so festgelegt werden, dass angegeben wird, welche Attribute gültig sind, und das **iItem-Element** muss den nullbasierten Index des zu ändernden Elements angeben. Durch Festlegen **des iItem-Elements** auf -1 wird das im Bearbeitungssteuerelement angezeigte Element geändert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg einen Wert ungleich 0 (null) oder andernfalls 0 (null) zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **CBEM \_ SETITEMW** (Unicode) und **CBEM \_ SETITEMA** (ANSI)<br/>                 |



 

 





