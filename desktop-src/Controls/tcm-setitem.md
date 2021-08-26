---
title: TCM_SETITEM Meldung (Commctrl.h)
description: Legt einige oder alle Attribute einer Registerkarte fest. Sie können diese Nachricht explizit oder mithilfe des \_ TabCtrl SetItem-Makros senden.
ms.assetid: 1d9c6607-d8ec-4644-a714-22bc2677aa78
keywords:
- TCM_SETITEM Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- TCM_SETITEM
- TCM_SETITEMA
- TCM_SETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c27f93e2743e5676c0fcca932cfa1936bb72667ef4fa4a5334eaae3e78d2be08
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876325"
---
# <a name="tcm_setitem-message"></a>TCM \_ SETITEM-Meldung

Legt einige oder alle Attribute einer Registerkarte fest. Sie können diese Nachricht explizit oder mithilfe des [**\_ TabCtrl SetItem-Makros**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setitem) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Index des Elements.

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**TCITEM-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-tcitema) die die neuen Elementattribute enthält. Der **Maskenmember** gibt an, welche Attribute festgelegt werden sollen. Wenn der **Maskenmember** den TCIF \_ TEXT-Wert angibt, ist der **pszText-Member** die Adresse einer auf NULL endenden Zeichenfolge, und der **cchTextMax-Member** wird ignoriert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE** zurück, wenn erfolgreich, **andernfalls FALSE.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **TCM \_ SETITEMW** (Unicode) und **TCM \_ SETITEMA** (ANSI)<br/>                   |



 

 





