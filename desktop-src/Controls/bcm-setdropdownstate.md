---
title: BCM_SETDROPDOWNSTATE (Commctrl.h)
description: Legt den Dropdownzustand für eine Schaltfläche mit dem Format TBSTYLE \_ DROPDOWN fest. Senden Sie diese Nachricht explizit oder mithilfe des \_ Button SetDropDownState-Makros.
ms.assetid: 725deff4-0bcb-497d-a6cf-e9c98b05f16e
keywords:
- BCM_SETDROPDOWNSTATE meldungssteuerelemente Windows
topic_type:
- apiref
api_name:
- BCM_SETDROPDOWNSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 989b4a04502a730c06a906be28a6915a4e604ff22c4b4e5ae9a4b85c8b464f81
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117833631"
---
# <a name="bcm_setdropdownstate-message"></a>BCM \_ SETDROPDOWNSTATE-Meldung

Legt den Dropdownzustand für eine Schaltfläche mit dem Format [**TBSTYLE \_ DROPDOWN fest.**](toolbar-control-and-button-styles.md) Senden Sie diese Nachricht explizit oder mithilfe des [**\_ Button SetDropDownState-Makros.**](/windows/desktop/api/Commctrl/nf-commctrl-button_setdropdownstate)

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* \[ In\]
</dt> <dd>

Eine **BOOL,** die **true für** den Status von BST \_ DROPDOWNPUSHED ist, **andernfalls FALSE.**

</dd> <dt>

*lParam* 
</dt> <dd>

Muss Null sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE zurück,** wenn erfolgreich, andernfalls **FALSE.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

**Referenz**
</dt> <dt>

[Schaltflächenstile](button-styles.md)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Schaltflächentypen](button-types-and-styles.md)
</dt> </dl>

 

 





