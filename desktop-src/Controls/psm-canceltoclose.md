---
title: PSM_CANCELTOCLOSE Meldung (prsht. h)
description: Wird von einer Anwendung gesendet, wenn Sie Änderungen seit der letzten Überprüfung von PSN-Benachrichtigungen durchgeführt hat \_ , die nicht abgebrochen werden können. Sie können diese Nachricht explizit oder mithilfe des propsheet \_ canceldeclose-Makros senden.
ms.assetid: 0a4b6176-7ddb-469f-8ebf-a31e533a8690
keywords:
- Windows-Steuerelemente für PSM_CANCELTOCLOSE Meldung
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
ms.openlocfilehash: ec1377801fddeeb52badee55869ace7e9c2277c4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105278"
---
# <a name="psm_canceltoclose-message"></a>PSM \_ cancelumclose-Nachricht

Wird von einer Anwendung gesendet, wenn Sie Änderungen seit der letzten Überprüfung von [PSN \_ ](psn-apply.md) -Benachrichtigungen durchgeführt hat, die nicht abgebrochen werden können. Sie können diese Nachricht explizit oder mithilfe des [**propsheet \_ canceldeclose**](/windows/desktop/api/Prsht/nf-prsht-propsheet_canceltoclose) -Makros senden.

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

## <a name="remarks"></a>Bemerkungen

**PSM \_ Canceldeclose** deaktiviert die Schaltfläche **Abbrechen** und ändert den Text der Schaltfläche **OK** in "Close".

Die meisten Eigenschaften Blätter warten auf das Durchführen von nicht rückgängig zu machenden Änderungen, bis eine Benachrichtigung über das \_ In einigen Fällen kann ein Eigenschaften Blatt jedoch nicht rückgängig zu machende Änderungen außerhalb der standardmäßigen "PSN \_ Apply/PSN Reset"- \_ Sequenz vornehmen. Ein Beispiel hierfür ist ein Eigenschaften Blatt, das eine **Bearbeitungs** Schaltfläche enthält, die zum Anzeigen eines unter Dialogfelds zum Bearbeiten einer Eigenschaft verwendet wird. Wenn der Benutzer auf **OK** klickt, um die Änderung zu übermitteln, verfügt die Seite Eigenschaften Blatt über mehrere Optionen.

-   Die Änderungen können aufgezeichnet werden, aber warten Sie, bis Sie eine PSN- \_ Benachrichtigungs Benachrichtigung erhalten, um Sie anzuwenden. Dies ist der bevorzugte Ansatz.
-   Sie kann die Änderungen sofort nach dem Beenden des unter Dialogfelds anwenden, aber merken Sie sich die ursprünglichen Einstellungen. Diese Einstellungen können verwendet werden, um den ursprünglichen Status wiederherzustellen, wenn eine \_ Benachrichtigung zum Zurücksetzen von PSN empfangen wird.
-   Die Änderungen können sofort angewendet werden, und es wird nicht versucht, die ursprünglichen Einstellungen wiederherzustellen, wenn eine Benachrichtigung zum [ \_ Zurücksetzen von PSN](psn-reset.md) empfangen wird. Diese Vorgehensweise wird nicht empfohlen, kann jedoch notwendig sein, wenn die Änderungen zu weitreichend sind, damit die beiden anderen Optionen praktikabel sind.

Bei der dritten Option sollten Anwendungen eine **PSM \_ canceldeclose** -Nachricht an das Eigenschaften Blatt senden. Es zeigt dem Benutzer an, dass die mit dem unter Dialogfeld vorgenommenen Änderungen nicht durch Klicken auf die Schaltfläche **Abbrechen** rückgängig gemacht werden können.

> [!Note]  
> Diese Meldung wird nicht unterstützt, wenn der Aero Wizard Style ([**PSH \_ aerowizard**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)) verwendet wird.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

 





