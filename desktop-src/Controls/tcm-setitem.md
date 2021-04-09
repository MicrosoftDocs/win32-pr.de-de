---
title: TCM_SETITEM Meldung (kommstrg. h)
description: Legt einige oder alle Attribute einer Registerkarte fest. Sie können diese Nachricht explizit oder mithilfe des tabctrl-Elements tabctrl senden \_ .
ms.assetid: 1d9c6607-d8ec-4644-a714-22bc2677aa78
keywords:
- Windows-Steuerelemente für TCM_SETITEM Meldung
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
ms.openlocfilehash: ee86cd0737c3c50c89a97d3881e2cdfd3850f481
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739888"
---
# <a name="tcm_setitem-message"></a>TCM-Element \_ Nachricht

Legt einige oder alle Attribute einer Registerkarte fest. Sie können diese Nachricht explizit oder mithilfe des [**tabctrl-Elements \_ tabctrl**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setitem) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der Index des Elements.

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) -Struktur, die die neuen Element Attribute enthält. Der **Mask** -Member gibt an, welche Attribute festgelegt werden sollen. Wenn das **Mask** -Element den tcif \_ -Textwert angibt, ist das **pszText** -Element die Adresse einer auf NULL endenden Zeichenfolge, und der **cchtextmax** -Member wird ignoriert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **TCM \_** "S" (Unicode) und " **TCM \_** " (ANSI)<br/>                   |



 

 





