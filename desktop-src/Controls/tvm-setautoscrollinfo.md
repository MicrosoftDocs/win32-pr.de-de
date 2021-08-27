---
title: TVM_SETAUTOSCROLLINFO (Commctrl.h)
description: Legt Informationen fest, die zum Bestimmen der Merkmale des automatischen Bildlaufs verwendet werden. Sie können diese Nachricht explizit oder mithilfe des \_ TreeView-Makros SetAutoScrollInfo senden.
ms.assetid: de55933f-1caa-4193-84de-0486c41e8f1f
keywords:
- TVM_SETAUTOSCROLLINFO meldungssteuerelemente Windows
topic_type:
- apiref
api_name:
- TVM_SETAUTOSCROLLINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8840045900fdbd63930219d199889cde018406779426cd767b49ab41a399efc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060160"
---
# <a name="tvm_setautoscrollinfo-message"></a>TVM \_ SETAUTOSCROLLINFO-Meldung

Legt Informationen fest, die zum Bestimmen der Merkmale des automatischen Bildlaufs verwendet werden. Sie können diese Nachricht explizit oder mithilfe des [**\_ TreeView-Makros SetAutoScrollInfo**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setautoscrollinfo) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* \[ In\]
</dt> <dd>

Gibt Pixel pro Sekunde an. Der offset, der gescrollt werden soll, wird durch *den wParam* geteilt, um die Gesamtdauer des automatischen Bildlaufs zu bestimmen.

</dd> <dt>

*lParam* \[ In\]
</dt> <dd>

Gibt das neu gezeichnete Zeitintervall an. In jedem elasierten Intervall neu gezeichnet, bis das Element in die Ansicht gescrollt wird. Bei *wParam* wird die Position des Elements berechnet, und es wird ein Neupaint angezeigt. Legen Sie diesen Wert fest, um einen reibungslosen Bildlauf zu erstellen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE zurück.**

## <a name="remarks"></a>Hinweise

Informationen zur automatischen Registrierung werden verwendet, um einen Bildlauf für ein nichtvisibles Element in die Ansicht zu durchführen. Das Steuerelement muss den erweiterten [**TVS \_ EX \_ AUTOHSCROLL-Stil**](tree-view-control-window-extended-styles.md) haben. Informationen zu erweiterten Stilen finden Sie unter Tree-View Von Steuerelementen erweiterte Stile.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





