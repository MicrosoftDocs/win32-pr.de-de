---
title: Emailaction. Attachments (Eigenschaft)
description: Dient zum Abrufen oder Festlegen eines Arrays von Anhängen, das mit der e-Mail-Nachricht gesendet wird.
ms.assetid: 59bcb8c4-8b8c-4f09-94d6-3a65f1e8c0a8
keywords:
- Eigenschaften Taskplaner "Anlagen"
- Anlagen Eigenschaft Taskplaner, emailaction-Objekt
- Emailaction-Objekt Taskplaner, Eigenschaft "Anhänge"
topic_type:
- apiref
api_name:
- EmailAction.Attachments
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ae620321f9dca7a5c38decf7de661d713989c88
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741904"
---
# <a name="emailactionattachments-property"></a>Emailaction. Attachments (Eigenschaft)

\[Dieses Objekt wird nicht mehr unterstützt. Verwenden Sie "IExecAction" mit dem PowerShell-Cmdlet " [**Send-Mail Message**](/powershell/module/microsoft.powershell.utility/send-mailmessage) " als Problem Umgehung.\]

Dient zum Abrufen oder Festlegen eines Arrays von Anhängen, das mit der e-Mail-Nachricht gesendet wird.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```VB
EmailAction.Attachments As String
```



## <a name="property-value"></a>Eigenschaftswert

Ein Array von Anlagen, das mit der e-Mail-Nachricht gesendet wird.

## <a name="remarks"></a>Bemerkungen

Es können maximal acht Anhänge im Array von Anlagen vorliegen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                    |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                    |
| Ende des Supports (Server)<br/>    | Windows Server 2008 R2<br/>                                                       |
| Typbibliothek<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Emailaction**](emailaction.md)
</dt> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

