---
title: PSM_CANCELTOCLOSE (Prsht.h)
description: Wird von einer Anwendung gesendet, wenn seit der letzten PSN APPLY-Benachrichtigung Änderungen vorgenommen wurden, \_ die nicht abgebrochen werden können. Sie können diese Nachricht explizit oder mithilfe des Makros PropSheet \_ CancelToClose senden.
ms.assetid: 0a4b6176-7ddb-469f-8ebf-a31e533a8690
keywords:
- PSM_CANCELTOCLOSE meldungssteuerelemente Windows
topic_type:
- apiref
api_name:
- PSM_CANCELTOCLOSE
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65c37c46e1232d8f99b8666e86058a13b840fbc975d94355d75ef40a810ee23c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118169816"
---
# <a name="psm_canceltoclose-message"></a>PSM \_ CANCELTOCLOSE-Nachricht

Wird von einer Anwendung gesendet, wenn seit der letzten [PSN \_ APPLY-Benachrichtigung](psn-apply.md) Änderungen vorgenommen wurden, die nicht abgebrochen werden können. Sie können diese Nachricht explizit oder mithilfe des [**Makros PropSheet \_ CancelToClose**](/windows/desktop/api/Prsht/nf-prsht-propsheet_canceltoclose) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Muss Null sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Muss Null sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Hinweise

**PSM \_ CANCELTOCLOSE** deaktiviert die **Schaltfläche Abbrechen** und ändert den Text der **Schaltfläche OK** in "Schließen".

Die meisten Eigenschaftenblätter warten auf nicht rückgängig gemachte Änderungen, bis eine PSN \_ APPLY-Benachrichtigung empfangen wird. In einigen Fällen kann ein Eigenschaftenblatt jedoch nicht rückgängig gemachte Änderungen außerhalb der standardmäßigen PSN \_ APPLY/PSN \_ RESET-Sequenz vornehmen. Ein Beispiel ist ein Eigenschaftenblatt, das eine **Schaltfläche Bearbeiten** enthält, die zum Anzeigen eines Unterdialogfelds zum Bearbeiten einer Eigenschaft verwendet wird. Wenn der Benutzer auf **OK klickt,** um die Änderung zu übermitteln, stehen auf der Eigenschaftenblattseite mehrere Optionen zur Verfügung.

-   Er kann die Änderungen aufzeichnen, aber warten, bis er eine PSN APPLY-Benachrichtigung \_ erhält, um sie anzuwenden. Dies ist der bevorzugte Ansatz.
-   Sie kann die Änderungen direkt nach dem Beenden des Unterdialogfelds übernehmen, aber merken Sie sich die ursprünglichen Einstellungen. Diese Einstellungen können verwendet werden, um den ursprünglichen Zustand wiederherzustellen, wenn eine PSN \_ RESET-Benachrichtigung empfangen wird.
-   Sie kann die Änderungen sofort anwenden und nicht versuchen, die ursprünglichen Einstellungen wiederherzustellen, wenn eine [PSN-RESET-Benachrichtigung \_ empfangen](psn-reset.md) wird. Dieser Ansatz wird nicht empfohlen, kann aber erforderlich sein, wenn die Änderungen zu weit reichen, damit die anderen beiden Optionen praktikabel sind.

Bei der dritten Option sollten Anwendungen eine **PSM \_ CANCELTOCLOSE-Nachricht** an das Eigenschaftenblatt senden. Sie gibt dem Benutzer an, dass die mit dem Unterdialogfeld vorgenommenen Änderungen nicht durch Klicken auf die Schaltfläche Abbrechen **rückgängig gemacht werden** können.

> [!Note]  
> This message is not supported when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |



 

 





