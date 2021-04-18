---
title: PSM_SHOWWIZBUTTONS Meldung (prsht. h)
description: Blendet Schaltflächen in einem Assistenten ein oder aus. Sie können diese Nachricht explizit oder mithilfe des propsheet- \_ showwitzbuttons-Makros senden.
ms.assetid: 669c4e51-cac1-40e1-8f23-afae0e41fc9b
keywords:
- Windows-Steuerelemente für PSM_SHOWWIZBUTTONS Meldung
topic_type:
- apiref
api_name:
- PSM_SHOWWIZBUTTONS
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22e8d1fc54d556240ef3fa6d6b6185a669978b84
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106337496"
---
# <a name="psm_showwizbuttons-message"></a>PSM- \_ showwizbuttons-Meldung

Blendet Schaltflächen in einem Assistenten ein oder aus. Sie können diese Nachricht explizit oder mithilfe des [**propsheet- \_ showwitzbuttons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_showwizbuttons) -Makros senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Einer oder mehrere der folgenden Werte, die angeben, welche Eigenschaften Blatt Schaltflächen angezeigt werden sollen. Wenn ein Schaltflächen Wert sowohl in diesem Parameter als auch in *LPARAM* enthalten ist, wird er angezeigt.



| Wert                                                                                                                                                                                 | Bedeutung                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| <span id="PSWIZB_BACK"></span><span id="pswizb_back"></span><dl> <dt>**pswizb \_ zurück**</dt> </dl>                               | Die Schaltfläche " **zurück** ".<br/>                                                            |
| <span id="PSWIZB_CANCEL"></span><span id="pswizb_cancel"></span><dl> <dt>**pswizb- \_ Abbruch**</dt> </dl>                         | Die Schaltfläche " **Abbrechen** ".<br/>                                                          |
| <span id="PSWIZB_DISABLEDFINISH"></span><span id="pswizb_disabledfinish"></span><dl> <dt>**pswizb \_ disabledfinish**</dt> </dl> | Die Schaltfläche **Fertig** stellen.<br/>                                                          |
| <span id="PSWIZB_FINISH"></span><span id="pswizb_finish"></span><dl> <dt>**pswizb- \_ Fertigstellen**</dt> </dl>                         | Die Schaltfläche **Fertig** stellen.<br/>                                                          |
| <span id="PSWIZB_NEXT"></span><span id="pswizb_next"></span><dl> <dt>**pswizb \_ als nächstes**</dt> </dl>                               | Die Schaltfläche **weiter** .<br/>                                                            |
| <span id="PSWIZB_SHOW"></span><span id="pswizb_show"></span><dl> <dt>**pswizb- \_ Anzeige**</dt> </dl>                               | Legen Sie nur dieses Flag (definiert als null) fest, um alle in *LPARAM* angegebenen Schaltflächen auszublenden.<br/> |
| <span id="PSWIZB_RESTORE"></span><span id="pswizb_restore"></span><dl> <dt>**pswizb- \_ Wiederherstellung**</dt> </dl>                      | Nicht implementiert.<br/>                                                                |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Mindestens einer der in *wParam* verwendeten Werte, der angibt, welche Schaltflächen von diesem-Befehl betroffen sind. Wenn ein Schaltflächen Wert in diesem Parameter, aber nicht in *wParam* angezeigt wird, wird die Schaltfläche ausgeblendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Bemerkungen

Assistenten zeigen unter jeder Seite entweder drei oder vier Schaltflächen an. Diese Meldung wird verwendet, um anzugeben, welche Schaltflächen sichtbar sind. Assistenten werden normalerweise **zurück**, **Abbrechen** und entweder eine Schaltfläche " **weiter** " oder " **Fertig** stellen" angezeigt. Die Schaltfläche **Abbrechen** ist immer sichtbar.

Legen Sie in der Regel **pswizb- \_ Fertig** stellen oder **pswizb \_ disabledfinish** fest, um die Schaltfläche **weiter** durch die Schaltfläche **Fertig** stellen zu ersetzen Wenn Sie die Schaltflächen " **weiter** " und " **Fertig** stellen" gleichzeitig anzeigen möchten, legen Sie beim Erstellen des Assistenten das Flag " **PSH \_ wizardhasfinish** " im **dwFlags** -Member der [**propsheeder**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2) -Struktur fest. Auf jeder Seite werden dann alle vier Schaltflächen angezeigt: **zurück**, **weiter**, **Abbrechen** und **Fertig** stellen.

Wenn Sie das [**propsheet- \_ showwitzbuttons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_showwizbuttons) -Makro verwenden, um diese Nachricht zu senden, wird Sie gepostet. Zu einem beliebigen Zeitpunkt können Sie [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) verwenden, um **PSM \_ showwitzbuttons** zu senden.

Wenn Ihr Benachrichtigungs Handler [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) verwendet, um eine **PSM- \_ showwitzbuttons** -Nachricht zu senden, sollten Sie keine Auswirkungen auf den Fenster Fokus haben, bis der Handler zurückkehrt. Wenn Sie z. b. [**MessageBox**](/windows/desktop/api/winuser/nf-winuser-messagebox) sofort nach dem Verwenden von **PostMessage** zum Senden von **PSM- \_ showwitzbuttons** aufzurufen, erhält das Meldungs Feld den Fokus. Da bereitgestellte Nachrichten erst übermittelt werden, wenn Sie den Anfang der Nachrichten Warteschlange erreichen, wird die **PSM- \_ showwitzbuttons** -Nachricht erst zugestellt, wenn der Fokus auf das Meldungs Feld verschoben wurde. Folglich kann das Eigenschaften Blatt den Fokus nicht ordnungsgemäß für die Schaltflächen festlegen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

