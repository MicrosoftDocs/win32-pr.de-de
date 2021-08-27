---
title: LVM_SETCALLBACKMASK (Commctrl.h)
description: Ändert die Rückrufmaske für ein Listenansicht-Steuerelement. Sie können diese Nachricht explizit oder mithilfe des \_ ListView-Makros SetCallbackMask senden.
ms.assetid: d7828bab-9897-408c-99ca-fad42b431be8
keywords:
- LVM_SETCALLBACKMASK meldungssteuerelemente Windows
topic_type:
- apiref
api_name:
- LVM_SETCALLBACKMASK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79e33b106eb0c59f83e40b9f170dd017fcdda412072ed51a26572fcf368f5215
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088850"
---
# <a name="lvm_setcallbackmask-message"></a>LVM \_ SETCALLBACKMASK-Nachricht

Ändert die Rückrufmaske für ein Listenansicht-Steuerelement. Sie können diese Nachricht explizit oder mithilfe des [**\_ ListView-Makros SetCallbackMask**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setcallbackmask) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der Wert der Rückrufmaske. Die Bits der Maske geben die Elementzustände oder Bilder an, für die die Anwendung die aktuellen Zustandsdaten speichert. Dieser Wert kann eine beliebige Kombination der folgenden Konstanten sein:



| Wert                                                                                                                                                                           | Bedeutung                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| <span id="LVIS_CUT"></span><span id="lvis_cut"></span><dl> <dt>**LVIS \_ CUT**</dt> </dl>                                  | Das Element ist für einen Ausschneide- und Einfügevorgang markiert.<br/>                                       |
| <span id="LVIS_DROPHILITED"></span><span id="lvis_drophilited"></span><dl> <dt>**LVIS \_ DROPHILITED**</dt> </dl>          | Das Element wird als Drag & Drop-Ziel hervorgehoben.<br/>                                      |
| <span id="LVIS_FOCUSED"></span><span id="lvis_focused"></span><dl> <dt>**\_LVIS-FOKUS**</dt> </dl>                      | Das Element hat den Fokus.<br/>                                                                 |
| <span id="LVIS_SELECTED"></span><span id="lvis_selected"></span><dl> <dt>**LVIS \_ SELECTED**</dt> </dl>                   | Das Element ist ausgewählt. <br/>                                                                  |
| <span id="LVIS_OVERLAYMASK"></span><span id="lvis_overlaymask"></span><dl> <dt>**LVIS \_ OVERLAYMASK**</dt> </dl>          | Die Anwendung speichert den Bildlistenindex des aktuellen Überlagerungsbilds für jedes Element.<br/> |
| <span id="LVIS_STATEIMAGEMASK"></span><span id="lvis_stateimagemask"></span><dl> <dt>**LVIS \_ STATEIMAGEMASK**</dt> </dl> | Die Anwendung speichert den Bildlistenindex des aktuellen Statusbilds für jedes Element. <br/>  |



 

</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE zurück,** wenn erfolgreich, andernfalls **FALSE.**

## <a name="remarks"></a>Hinweise

Die *Rückrufmaske eines* Listenansichtssteuerelements ist ein Satz von Bitflags, die die Elementzustände angeben, für die die Anwendung anstelle des -Steuerelements die aktuellen Daten speichert. Die Rückrufmaske gilt für alle Elemente des Steuerelements, im Gegensatz zur Rückrufelementbezeichnung, die für ein bestimmtes Element gilt. Die Rückrufmaske ist standardmäßig 0 (null), d. h., das Listenansicht-Steuerelement speichert alle Elementzustandsinformationen. Nachdem Sie ein Listenansicht-Steuerelement erstellt und dessen Elemente initialisiert haben, können Sie die **LVM \_ SETCALLBACKMASK-Nachricht** senden, um die Rückrufmaske zu ändern. Um die aktuelle Rückrufmaske abzurufen, senden Sie die [**LVM \_ GETCALLBACKMASK-Nachricht.**](lvm-getcallbackmask.md)

Weitere Informationen zu Überlagerungsbildern und Zustandsbildern finden Sie unter [Hinzufügen List-View Bildlisten.](using-list-view-controls.md)

Weitere Informationen zu Rückrufen in Listenansichten finden Sie unter [Rückrufelemente und die Rückrufmaske.](list-view-controls-overview.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**LVN \_ GETDISPINFO**](lvn-getdispinfo.md)
</dt> </dl>

 

 





