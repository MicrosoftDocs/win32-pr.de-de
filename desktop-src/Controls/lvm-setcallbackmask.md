---
title: LVM_SETCALLBACKMASK Meldung (kommstrg. h)
description: Ändert die Rückruf Maske für ein Listenansicht-Steuerelement. Sie können diese Nachricht explizit oder mithilfe des ListView- \_ Makros SetCallbackMask senden.
ms.assetid: d7828bab-9897-408c-99ca-fad42b431be8
keywords:
- Windows-Steuerelemente für LVM_SETCALLBACKMASK Meldung
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
ms.openlocfilehash: ef6dd46228c4e4aeada30f469a77f9e67aff3a37
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103363"
---
# <a name="lvm_setcallbackmask-message"></a>LVM- \_ SetCallbackMask-Meldung

Ändert die Rückruf Maske für ein Listenansicht-Steuerelement. Sie können diese Nachricht explizit oder mithilfe des [**ListView-Makros \_ SetCallbackMask**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setcallbackmask) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der Wert der Rückruf Maske. Die Bits der Maske geben die Element Zustände oder-Bilder an, für die die Anwendung die aktuellen Zustandsdaten speichert. Dieser Wert kann eine beliebige Kombination der folgenden Konstanten sein:



| Wert                                                                                                                                                                           | Bedeutung                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| <span id="LVIS_CUT"></span><span id="lvis_cut"></span><dl> <dt>**LVIS- \_ Ausschneiden**</dt> </dl>                                  | Das Element ist für einen Ausschneide-und Einfügevorgang gekennzeichnet.<br/>                                       |
| <span id="LVIS_DROPHILITED"></span><span id="lvis_drophilited"></span><dl> <dt>**LVIS wurde \_ beendet.**</dt> </dl>          | Das Element wird als Drag & Drop-Ziel hervorgehoben.<br/>                                      |
| <span id="LVIS_FOCUSED"></span><span id="lvis_focused"></span><dl> <dt>**LVIS \_ fokussiert**</dt> </dl>                      | Das Element hat den Fokus.<br/>                                                                 |
| <span id="LVIS_SELECTED"></span><span id="lvis_selected"></span><dl> <dt>**LVIS \_ ausgewählt**</dt> </dl>                   | Das Element ist ausgewählt. <br/>                                                                  |
| <span id="LVIS_OVERLAYMASK"></span><span id="lvis_overlaymask"></span><dl> <dt>**LVIS \_ overlaymask**</dt> </dl>          | Die Anwendung speichert den Abbild Listen Index des aktuellen Überlagerungs Bilds für jedes Element.<br/> |
| <span id="LVIS_STATEIMAGEMASK"></span><span id="lvis_stateimagemask"></span><dl> <dt>**LVIS- \_ Status-magemask**</dt> </dl> | Die Anwendung speichert den Abbild Listen Index des aktuellen Status Bilds für jedes Element. <br/>  |



 

</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .

## <a name="remarks"></a>Bemerkungen

Bei der *Rückruf Maske* eines Listenansicht-Steuer Elements handelt es sich um einen Satz von Bitflags, die die Element Zustände angeben, für die die Anwendung und nicht das Steuerelement die aktuellen Daten speichert. Die Rückruf Maske gilt für alle Elemente des Steuer Elements, im Gegensatz zur Rückruf Element Bezeichnung, die für ein bestimmtes Element gilt. Die Rückruf Maske ist standardmäßig 0 (null), was bedeutet, dass das Listenansicht-Steuerelement alle Element Zustandsinformationen speichert. Nachdem Sie ein Listenansicht-Steuerelement erstellt und seine Elemente initialisiert haben, können Sie die **LVM- \_ SetCallbackMask** -Nachricht senden, um die Rückruf Maske zu ändern. Um die aktuelle Rückruf Maske abzurufen, senden Sie die [**LVM \_ GetCallbackMask**](lvm-getcallbackmask.md) -Nachricht.

Weitere Informationen zu Überlagerungs Bildern und Zustands Bildern finden Sie unter [Hinzufügen List-View Bildlisten](using-list-view-controls.md).

Weitere Informationen zu List-View-Rückrufen finden Sie unter [Rückruf Elemente und Rückruf Maske](list-view-controls-overview.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**LVN \_ getdispinfo**](lvn-getdispinfo.md)
</dt> </dl>

 

 





