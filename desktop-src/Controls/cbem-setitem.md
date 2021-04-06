---
title: CBEM_SETITEM Meldung (kommstrg. h)
description: Legt die Attribute für ein Element in einem ComboBoxEx-Steuerelement fest.
ms.assetid: 752df8ea-fd5e-47fa-b729-d019bdde0904
keywords:
- Windows-Steuerelemente für CBEM_SETITEM Meldung
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
ms.openlocfilehash: 50ae19287e3e30810b1d8c558be9b6153a86ab6b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743400"
---
# <a name="cbem_setitem-message"></a>CBEM-Element \_ Nachricht

Legt die Attribute für ein Element in einem ComboBoxEx-Steuerelement fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) -Struktur, die die festzulegenden Element Informationen enthält. Wenn die Nachricht gesendet wird, muss der **Mask** -Member der Struktur festgelegt werden, um anzugeben, welche Attribute gültig sind, und der **iItem** -Member muss den NULL basierten Index des zu ändernden Elements angeben. Wenn Sie den **iItem** -Member auf-1 festlegen, wird das im Bearbeitungs Steuerelement angezeigte Element geändert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg einen Wert ungleich 0 (null) zurück, andernfalls NULL.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **CBEM \_** "CBEM" (Unicode) und " **CBEM \_** " (ANSI)<br/>                 |



 

 





