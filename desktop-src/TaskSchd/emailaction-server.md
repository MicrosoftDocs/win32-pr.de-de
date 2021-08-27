---
title: EmailAction.Server(Eigenschaft)
description: Für die Skripterstellung ruft den Namen des SMTP-Servers ab, über den Sie E-Mails senden, oder legt diesen fest.
ms.assetid: a6e03144-ae3e-4c4c-aad8-884be5ab324f
keywords:
- Servereigenschafts-Taskplaner
- Servereigenschaft Taskplaner , EmailAction-Objekt
- EmailAction-Taskplaner , Servereigenschaft
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
ms.openlocfilehash: 3348b067698cfdcf3c7dbb95a97b6dd23f0f0cb7ca9225d70a9bb3d4ce2a93b4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100260"
---
# <a name="emailactionserver-property"></a>EmailAction.Server(Eigenschaft)

\[Dieses Objekt wird nicht mehr unterstützt. Verwenden Sie IExecAction mit dem [**PowerShell-Cmdlet Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) als Problemumgehung.\]

Für die Skripterstellung ruft den Namen des SMTP-Servers ab, über den Sie E-Mails senden, oder legt diesen fest.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```VB
EmailAction.Server As String
```



## <a name="property-value"></a>Eigenschaftswert

Der Name des Servers, von dem Sie E-Mails senden.

## <a name="remarks"></a>Hinweise

Stellen Sie sicher, dass der SMTP-Server, der die E-Mail sendet, ordnungsgemäß eingerichtet ist. E-Mail wird mithilfe der NTLM-Authentifizierung für Windows SMTP-Server gesendet. Dies bedeutet, dass die Sicherheitsanmeldeinformationen, die zum Ausführen der Aufgabe verwendet werden, auch über Berechtigungen auf dem SMTP-Server verfügen müssen, um E-Mails zu senden. Wenn der SMTP-Server ein nicht Windows serverbasierter Server ist, wird die E-Mail gesendet, wenn der Server anonymen Zugriff zulässt. Informationen zum Einrichten des SMTP-Servers finden Sie unter [SMTP-Servereinrichtung.](https://www.microsoft.com/technet/prodtechnol/WindowsServer2003/Library/IIS/e4cf06f5-9a36-474b-ba78-3f287a2b88f2.mspx?mfr=true)Informationen zum Verwalten von SMTP-Servereinstellungen finden Sie unter [SMTP-Verwaltung](/previous-versions/windows/it-pro/windows-server-2003/cc758258(v=ws.10)).

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

 

