---
title: LVM_ARRANGE (Commctrl.h)
description: Ordnet Elemente in der Symbolansicht an. Sie können diese Nachricht explizit oder mithilfe des Makros ListView \_ Arrange senden.
ms.assetid: f7dbcdd2-3cc9-4bae-827e-8bac3b49486c
keywords:
- LVM_ARRANGE von Windows-Steuerelementen
topic_type:
- apiref
api_name:
- LVM_ARRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98d7e3595c276815af8708a54d6e81c2a40192d8d07e6cbce514481723799d04
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062650"
---
# <a name="lvm_arrange-message"></a>LVM \_ ARRANGE-Nachricht

Ordnet Elemente in der Symbolansicht an. Sie können diese Nachricht explizit oder mithilfe des [**Makros ListView \_ Arrange**](/windows/desktop/api/Commctrl/nf-commctrl-listview_arrange) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Einer der folgenden Werte, der die Ausrichtung angibt:



| Wert                                                                                                                                                            | Bedeutung                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| <span id="LVA_ALIGNLEFT"></span><span id="lva_alignleft"></span><dl> <dt>**LVA \_ ALIGNLEFT**</dt> </dl>    | Nicht implementiert. Wenden Sie stattdessen [**den LVS \_ ALIGNLEFT-Stil**](list-view-window-styles.md) an.<br/> |
| <span id="LVA_ALIGNTOP"></span><span id="lva_aligntop"></span><dl> <dt>**LVA \_ ALIGNTOP**</dt> </dl>       | Nicht implementiert. Wenden Sie stattdessen [**den LVS \_ ALIGNTOP-Stil**](list-view-window-styles.md) an.<br/>   |
| <span id="LVA_DEFAULT"></span><span id="lva_default"></span><dl> <dt>**LVA \_ DEFAULT**</dt> </dl>          | Richtet Elemente entsprechend den aktuellen Ausrichtungsstilen des Listenansicht-Steuerelements aus (Standardwert).<br/>           |
| <span id="LVA_SNAPTOGRID"></span><span id="lva_snaptogrid"></span><dl> <dt>**\_LVA-SNAPTOGRID**</dt> </dl> | Ausrichtung aller Symbole an der nächsten Rasterposition.<br/>                                                             |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Muss Null sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE zurück,** wenn erfolgreich; andernfalls **FALSE**.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





