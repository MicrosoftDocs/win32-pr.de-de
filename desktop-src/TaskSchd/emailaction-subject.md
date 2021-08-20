---
title: EmailAction.Subject-Eigenschaft
description: Ruft für die Skripterstellung den Betreff der E-Mail ab oder legt dieses fest.
ms.assetid: ea398af1-9ae6-4bcf-9618-bb840b15127e
keywords:
- Subject-Eigenschaft Taskplaner
- Subject-Eigenschaft Taskplaner , EmailAction-Objekt
- EmailAction-Objekt Taskplaner , Subject-Eigenschaft
topic_type:
- apiref
api_name:
- EmailAction.Subject
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7474fa4b7a6de59fd59a98c27a4877ab10c1acb6beac3c1682fccd05702aa275
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117943787"
---
# <a name="emailactionsubject-property"></a>EmailAction.Subject-Eigenschaft

\[Dieses Objekt wird nicht mehr unterstützt. Verwenden Sie IExecAction mit dem [**PowerShell-Cmdlet Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage?view=powershell-7&preserve-view=true) als Problemumgehung.\]

Ruft für die Skripterstellung den Betreff der E-Mail ab oder legt dieses fest.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```VB
EmailAction.Subject As String
```



## <a name="property-value"></a>Eigenschaftswert

Der Betreff der E-Mail-Nachricht.

## <a name="remarks"></a>Hinweise

Beim Festlegen dieses Eigenschaftswerts kann der Wert Text sein, der aus einer Ressource .dll Datei abgerufen wird. Eine spezialisierte Zeichenfolge wird verwendet, um auf den Text aus der Ressourcendatei zu verweisen. Das Format der Zeichenfolge lautet $(@ \[ Dll \] , \[ ResourceID ), wobei DLL \] der Pfad zu der .dll Datei mit der Ressource und \[ \] \[ ResourceID \] der Bezeichner für den Ressourcentext ist. Wenn Sie diesen Eigenschaftswert beispielsweise auf $(@ %SystemRoot% \\ System32 \\ResourceName.dll, -101) festlegen, wird die Eigenschaft auf den Wert des Ressourcentexts mit einem Bezeichner festgelegt, der in der %SystemRoot% \\ System32-ResourceName.dll-Datei gleich -101 \\ ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                    |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                    |
| Ende des Supports (Server)<br/>    | Windows Server 2008 R2<br/>                                                       |
| Typbibliothek<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**EmailAction**](emailaction.md)
</dt> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

