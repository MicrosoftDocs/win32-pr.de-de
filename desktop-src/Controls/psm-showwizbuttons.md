---
title: PSM_SHOWWIZBUTTONS-Nachricht (Prsht.h)
description: Zeigt Schaltflächen in einem Assistenten an oder blendet sie aus. Sie können diese Nachricht explizit oder mithilfe des \_ PropSheet-Makros ShowWizButtons senden.
ms.assetid: 669c4e51-cac1-40e1-8f23-afae0e41fc9b
keywords:
- PSM_SHOWWIZBUTTONS Windows-Steuerelemente für Nachrichten
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
ms.openlocfilehash: 86bbad4d6f0ce8a084709c04110d093e4d79b806226bdc1fa651278b4054fa8d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088480"
---
# <a name="psm_showwizbuttons-message"></a>PSM \_ SHOWWIZBUTTONS-Nachricht

Zeigt Schaltflächen in einem Assistenten an oder blendet sie aus. Sie können diese Nachricht explizit oder mithilfe des [**\_ PropSheet-Makros ShowWizButtons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_showwizbuttons) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Mindestens einer der folgenden Werte, der angibt, welche Eigenschaftenblattschaltflächen angezeigt werden sollen. Wenn ein Schaltflächenwert sowohl in diesem Parameter als auch in *lParam* enthalten ist, wird er angezeigt.



| Wert                                                                                                                                                                                 | Bedeutung                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| <span id="PSWIZB_BACK"></span><span id="pswizb_back"></span><dl> <dt>**PSWIBESTAND \_ ZURÜCK**</dt> </dl>                               | Die Schaltfläche **Zurück.**<br/>                                                            |
| <span id="PSWIZB_CANCEL"></span><span id="pswizb_cancel"></span><dl> <dt>**PSWI WIEDER \_ ABBRECHEN**</dt> </dl>                         | Die Schaltfläche **Abbrechen.**<br/>                                                          |
| <span id="PSWIZB_DISABLEDFINISH"></span><span id="pswizb_disabledfinish"></span><dl> <dt>**PSWIATUR \_ DISABLEDFINISH**</dt> </dl> | Die Schaltfläche **Fertig stellen.**<br/>                                                          |
| <span id="PSWIZB_FINISH"></span><span id="pswizb_finish"></span><dl> <dt>**PSWIFABRIK \_ FINISH**</dt> </dl>                         | Die Schaltfläche **Fertig stellen.**<br/>                                                          |
| <span id="PSWIZB_NEXT"></span><span id="pswizb_next"></span><dl> <dt>**PSWIEINANDER \_ WEITER**</dt> </dl>                               | Die Schaltfläche **Weiter.**<br/>                                                            |
| <span id="PSWIZB_SHOW"></span><span id="pswizb_show"></span><dl> <dt>**PSWIBLEND \_ SHOW**</dt> </dl>                               | Legen Sie nur dieses Flag (definiert als 0) fest, um alle in *lParam* angegebenen Schaltflächen auszublenden.<br/> |
| <span id="PSWIZB_RESTORE"></span><span id="pswizb_restore"></span><dl> <dt>**\_PSWIWIEDERHERSTELLUNG**</dt> </dl>                      | Nicht implementiert.<br/>                                                                |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Mindestens einer der in *wParam* verwendeten Werte, der angibt, welche Schaltflächen von diesem Aufruf betroffen sind. Wenn ein Schaltflächenwert in diesem Parameter, aber nicht in *wParam* angezeigt wird, wird die Schaltfläche ausgeblendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Hinweise

Assistenten zeigen drei oder vier Schaltflächen unter jeder Seite an. Diese Meldung wird verwendet, um anzugeben, welche Schaltflächen sichtbar sind. Assistenten zeigen normalerweise **Zurück,** **Abbrechen** und entweder die Schaltfläche **Weiter** oder **Fertig stellen** an. Die Schaltfläche **Abbrechen** ist immer sichtbar.

Legen Sie in der Regel **PSWIEINANDER \_ FERTIG STELLEN** oder **PSWIRAFF \_ DEAKTIVIERTFINISH** fest, um die Schaltfläche **Weiter** durch die Schaltfläche **Fertig stellen** zu ersetzen. Um die Schaltflächen **Weiter** und **Fertig stellen** gleichzeitig anzuzeigen, legen Sie beim Erstellen des Assistenten das **PSH \_ WIZARDHASFINISH-Flag** im **dwFlags-Member** der [**PROPSHEETHEADER-Struktur**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2) fest. Auf jeder Seite werden dann alle vier Schaltflächen angezeigt: **Zurück,** **Weiter,** **Abbrechen** und **Fertig stellen.**

Wenn Sie das [**\_ PropSheet-Makro ShowWizButtons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_showwizbuttons) verwenden, um diese Nachricht zu senden, wird sie veröffentlicht. Sie können [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) jederzeit verwenden, um **PSM \_ SHOWWIZBUTTONS** zu senden.

Wenn Ihr Benachrichtigungshandler [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) verwendet, um eine **PSM \_ SHOWWIZBUTTONS-Nachricht** zu senden, tun Sie nichts, was sich auf den Fensterfokus auswirkt, bis der Handler zurückgegeben wurde. Wenn Sie beispielsweise [**MessageBox**](/windows/desktop/api/winuser/nf-winuser-messagebox) sofort nach der Verwendung von **PostMessage** aufrufen, um **PSM \_ SHOWWIZBUTTONS** zu senden, erhält das Meldungsfeld den Fokus. Da gesendete Nachrichten erst übermittelt werden, wenn sie den Kopf der Nachrichtenwarteschlange erreichen, wird die **PSM \_ SHOWWIZBUTTONS-Nachricht** erst zugestellt, nachdem der Assistent den Fokus auf das Meldungsfeld verloren hat. Daher kann das Eigenschaftenblatt den Fokus für die Schaltflächen nicht ordnungsgemäß festlegen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |



 

