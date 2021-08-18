---
title: EmailAction.Body (Eigenschaft)
description: Für die Skripterstellung ruft den Text der E-Mail ab, die die E-Mail enthält, oder legt diesen fest.
ms.assetid: 0015c2b9-9278-407b-b3cf-492f2d95bcb6
keywords:
- Texteigenschafts-Taskplaner
- Body-Eigenschaft Taskplaner , EmailAction-Objekt
- EmailAction-Taskplaner , Body-Eigenschaft
topic_type:
- apiref
api_name:
- EmailAction.Body
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57daf8d16da9f77a88d91a23cfaea88d1c3e27adb09a0d502b447b5987fce2ac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100380"
---
# <a name="emailactionbody-property"></a>EmailAction.Body (Eigenschaft)

\[Dieses Objekt wird nicht mehr unterstützt. Verwenden Sie IExecAction mit dem [**PowerShell-Cmdlet Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) als Problemumgehung.\]

Für die Skripterstellung ruft den Text der E-Mail ab, die die E-Mail enthält, oder legt diesen fest.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```VB
EmailAction.Body As String
```



## <a name="property-value"></a>Eigenschaftswert

Der Text der E-Mail, die die E-Mail enthält.

## <a name="remarks"></a>Hinweise

Beim Festlegen dieses Eigenschaftswerts kann der Wert Text sein, der aus einer Ressourcendatei .dll wird. Eine spezialisierte Zeichenfolge wird verwendet, um auf den Text aus der Ressourcendatei zu verweisen. Das Format der Zeichenfolge ist $(@ Dll , ResourceID ), wobei DLL der Pfad zur .dll-Datei ist, die die Ressource enthält, und ResourceID der Bezeichner für den \[ \] \[ \] \[ \] \[ \] Ressourcentext ist. Wenn Sie diesen Eigenschaftswert beispielsweise auf $(@ %SystemRoot% System32ResourceName.dll, -101) festlegen, wird die -Eigenschaft auf den Wert des Ressourcentexts mit einem Bezeichner gleich \\ \\ -101 in der Datei %SystemRoot% \\ System32 \\ResourceName.dll festgelegt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                          |
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

 

