---
title: BCM_SETDROPDOWNSTATE Meldung (kommstrg. h)
description: Legt den Dropdown-Zustand für eine Schaltfläche mit dem Dropdown Menü Style tbstyle fest \_ . Senden Sie diese Nachricht explizit oder mithilfe des \_ setdropdownstate-Makros der Schaltfläche.
ms.assetid: 725deff4-0bcb-497d-a6cf-e9c98b05f16e
keywords:
- Windows-Steuerelemente für BCM_SETDROPDOWNSTATE Meldung
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
ms.openlocfilehash: fc44ec58d40e047708591121f81c84f327ca47c1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103634"
---
# <a name="bcm_setdropdownstate-message"></a>BCM \_ setdropdownstate-Meldung

Legt den Dropdown-Zustand für eine Schaltfläche mit dem [**\_ Dropdown Menü Style tbstyle**](toolbar-control-and-button-styles.md)fest. Senden Sie diese Nachricht explizit oder mithilfe des [**\_ setdropdownstate**](/windows/desktop/api/Commctrl/nf-commctrl-button_setdropdownstate) -Makros der Schaltfläche.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* \[ in\]
</dt> <dd>

Ein **boolescher** Wert  , der für den Status von BST \_ dropdownpushübertragung true ist, andernfalls **false** .

</dd> <dt>

*lParam* 
</dt> <dd>

Muss Null sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[Schaltflächenstile](button-styles.md)
</dt> <dt>

**Licher**
</dt> <dt>

[Schaltflächentypen](button-types-and-styles.md)
</dt> </dl>

 

 





