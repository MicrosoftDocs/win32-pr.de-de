---
title: LVM_SETIMAGELIST Meldung (kommstrg. h)
description: Weist einem Listenansicht-Steuerelement eine Bildliste zu. Sie können diese Nachricht explizit oder mithilfe des ListView \_ SetImageList-Makros senden.
ms.assetid: 5241065b-85e4-412e-9868-fd5b15ff7c17
keywords:
- Windows-Steuerelemente für LVM_SETIMAGELIST Meldung
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
ms.openlocfilehash: 779d31fd781a72dbdfbc4738e091482ca4a08528
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949420"
---
# <a name="lvm_setimagelist-message"></a>LVM \_ SetImageList-Nachricht

Weist einem Listenansicht-Steuerelement eine Bildliste zu. Sie können diese Nachricht explizit oder mithilfe des [**ListView \_ SetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setimagelist) -Makros senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Typ der Bildliste. Dieser Parameter kann einen der folgenden Werte aufweisen:



| Wert                                                                                                                                                                     | Bedeutung                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| <span id="LVSIL_NORMAL"></span><span id="lvsil_normal"></span><dl> <dt>**lvsil \_ Normal**</dt> </dl>                | Bildliste mit großen Symbolen.<br/>  |
| <span id="LVSIL_SMALL"></span><span id="lvsil_small"></span><dl> <dt>**lvsil \_ Small**</dt> </dl>                   | Bildliste mit kleinen Symbolen.<br/>  |
| <span id="LVSIL_STATE"></span><span id="lvsil_state"></span><dl> <dt>**Zustand "lvsil" \_**</dt> </dl>                   | Bildliste mit Zustands Bildern.<br/> |
| <span id="LVSIL_GROUPHEADER"></span><span id="lvsil_groupheader"></span><dl> <dt>**lvsil- \_ GroupHeader**</dt> </dl> | Bildliste für Gruppen Kopfzeile.<br/>  |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Handle der zuzuweisenden Bildliste.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt das Handle für die Bildliste zurück, die zuvor dem Steuerelement zugeordnet war, wenn erfolgreich, andernfalls **null** .

## <a name="remarks"></a>Bemerkungen

Die aktuelle Bildliste wird zerstört, wenn das Listenansicht-Steuerelement zerstört wird, es sei denn, der LVS-Stil " [**\_ shareimagelists**](list-view-window-styles.md) " ist festgelegt. Wenn Sie diese Meldung verwenden, um eine Bildliste durch einen anderen zu ersetzen, muss Ihre Anwendung alle anderen Bildlisten explizit zerstören als die aktuelle.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





