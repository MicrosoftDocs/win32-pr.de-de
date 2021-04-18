---
title: TVM_SETAUTOSCROLLINFO Meldung (kommstrg. h)
description: Legt Informationen fest, die zum Bestimmen von Auto Bild Lauf Merkmalen verwendet werden. Sie können diese Nachricht explizit oder mithilfe des TreeView- \_ Makros "seetautoscrollinfo" senden.
ms.assetid: de55933f-1caa-4193-84de-0486c41e8f1f
keywords:
- Windows-Steuerelemente für TVM_SETAUTOSCROLLINFO Meldung
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
ms.openlocfilehash: faa1f7920d2ec8c443b2ec5f1ff9189c22c5f21e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338136"
---
# <a name="tvm_setautoscrollinfo-message"></a>TVM- \_ Meldung "abtautoscrollinfo"

Legt Informationen fest, die zum Bestimmen von Auto Bild Lauf Merkmalen verwendet werden. Sie können diese Nachricht explizit oder mithilfe des [**TreeView-Makros " \_ seetautoscrollinfo**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setautoscrollinfo) " senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* \[ in\]
</dt> <dd>

Gibt Pixel pro Sekunde an. Der Offset für den Bildlauf wird durch den *wParam* dividiert, um die Gesamtdauer des automatischen Bildlaufs zu bestimmen.

</dd> <dt>

*LPARAM* \[ in\]
</dt> <dd>

Gibt das umzeichnungs Zeitintervall an. Zeichnen Sie bei jedem abgefragten Intervall neu, bis der Artikel in der Ansicht angezeigt wird. Bei Angabe von *wParam* wird der Speicherort des Elements berechnet und ein Repaint-Vorgang durchgeführt. Legen Sie diesen Wert fest, um einen Smooth Scroll zu erstellen

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück.

## <a name="remarks"></a>Bemerkungen

AutoScroll-Informationen werden verwendet, um einen Bildlauf in einem nicht sichtbaren Element durchführen. Das Steuerelement muss über den erweiterten [**\_ \_ autohscroll**](tree-view-control-window-extended-styles.md) -Stil "TVs" verfügen. Weitere Informationen zu erweiterten Stilen finden Sie unter Tree-View Steuerelement erweiterter Stile.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





