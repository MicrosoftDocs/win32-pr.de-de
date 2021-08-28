---
title: LVM_SETIMAGELIST (Commctrl.h)
description: Weist einem Listenansicht-Steuerelement eine Bildliste zu. Sie können diese Nachricht explizit oder mithilfe des \_ ListView-Makros SetImageList senden.
ms.assetid: 5241065b-85e4-412e-9868-fd5b15ff7c17
keywords:
- LVM_SETIMAGELIST von Windows-Steuerelementen
topic_type:
- apiref
api_name:
- LVM_SETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4151f7d6e3736e6fe28faa28bc258fb4f85bfb57622b1ec77c02ed83ea187941
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119919960"
---
# <a name="lvm_setimagelist-message"></a>LVM \_ SETIMAGELIST-Meldung

Weist einem Listenansicht-Steuerelement eine Bildliste zu. Sie können diese Nachricht explizit oder mithilfe des [**\_ ListView-Makros SetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setimagelist) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Typ der Bildliste. Dieser Parameter kann einen der folgenden Werte haben:



| Wert                                                                                                                                                                     | Bedeutung                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| <span id="LVSIL_NORMAL"></span><span id="lvsil_normal"></span><dl> <dt>**LVSIL \_ NORMAL**</dt> </dl>                | Bildliste mit großen Symbolen.<br/>  |
| <span id="LVSIL_SMALL"></span><span id="lvsil_small"></span><dl> <dt>**LVSIL \_ SMALL**</dt> </dl>                   | Bildliste mit kleinen Symbolen.<br/>  |
| <span id="LVSIL_STATE"></span><span id="lvsil_state"></span><dl> <dt>**LVSIL \_ STATE**</dt> </dl>                   | Bildliste mit Zustandsbildern.<br/> |
| <span id="LVSIL_GROUPHEADER"></span><span id="lvsil_groupheader"></span><dl> <dt>**LVSIL \_ GROUPHEADER**</dt> </dl> | Bildliste für Gruppenheader.<br/>  |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Handle für die bildliste, die zugewiesen werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt das Handle an die Imageliste zurück, die dem Steuerelement zuvor zugeordnet war, sofern erfolgreich, **andernfalls NULL.**

## <a name="remarks"></a>Hinweise

Die aktuelle Bildliste wird zerstört, wenn das Listenansicht-Steuerelement zerstört wird, es sei denn, [**der LVS \_ SHAREIMAGELISTS-Stil**](list-view-window-styles.md) ist festgelegt. Wenn Sie diese Meldung verwenden, um eine Bildliste durch eine andere zu ersetzen, muss Ihre Anwendung explizit alle Bildlisten zerstören, die nicht die aktuelle Bildliste sind.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





