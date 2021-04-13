---
title: Emailaction. Server-Eigenschaft
description: Bei der Skripterstellung wird der Name des SMTP-Servers abgerufen oder festgelegt, den Sie zum Senden von e-Mail verwenden.
ms.assetid: a6e03144-ae3e-4c4c-aad8-884be5ab324f
keywords:
- Taskplaner der Server Eigenschaft
- Server Eigenschaft Taskplaner, emailaction-Objekt
- Emailaction-Objekt Taskplaner, Server Eigenschaft
topic_type:
- apiref
api_name:
- EmailAction.Server
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0fefcc5e33727d6b4ad0bcd60e48432c68422105
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340768"
---
# <a name="emailactionserver-property"></a>Emailaction. Server-Eigenschaft

\[Dieses Objekt wird nicht mehr unterstützt. Verwenden Sie "IExecAction" mit dem PowerShell-Cmdlet " [**Send-Mail Message**](/powershell/module/microsoft.powershell.utility/send-mailmessage) " als Problem Umgehung.\]

Bei der Skripterstellung wird der Name des SMTP-Servers abgerufen oder festgelegt, den Sie zum Senden von e-Mail verwenden.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```VB
EmailAction.Server As String
```



## <a name="property-value"></a>Eigenschaftswert

Der Name des Servers, der zum Senden von e-Mails verwendet wird.

## <a name="remarks"></a>Bemerkungen

Stellen Sie sicher, dass der SMTP-Server, der die e-Mail sendet, korrekt eingerichtet ist. E-Mail wird mithilfe der NTLM-Authentifizierung für Windows-SMTP-Server gesendet. Dies bedeutet, dass die zum Ausführen der Aufgabe verwendeten Sicherheits Anmelde Informationen auch über Berechtigungen auf dem SMTP-Server verfügen müssen, um eine e-Mail zu senden. Wenn es sich beim SMTP-Server um einen nicht auf Windows basierenden Server handelt, wird die e-Mail gesendet, wenn der Server den anonymen Zugriff zulässt. Weitere Informationen zum Einrichten des SMTP-Servers finden Sie unter [SMTP-Server Setup](https://www.microsoft.com/technet/prodtechnol/WindowsServer2003/Library/IIS/e4cf06f5-9a36-474b-ba78-3f287a2b88f2.mspx?mfr=true). Weitere Informationen zum Verwalten von SMTP-Servereinstellungen finden Sie unter [SMTP-Verwaltung](/previous-versions/windows/it-pro/windows-server-2003/cc758258(v=ws.10)).

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

 

