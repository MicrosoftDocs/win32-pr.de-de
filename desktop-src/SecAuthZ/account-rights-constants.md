---
description: Konto Rechte bestimmen den Typ der Anmeldung, die von einem Benutzerkonto durchgeführt werden kann. Ein Administrator weist Benutzer-und Gruppenkonten Konto Rechte zu. Jedes Benutzerkonto verfügt über die Berechtigungen, die dem Benutzer und den Gruppen gewährt werden, zu denen der Benutzer gehört.
ms.assetid: 42139d33-2d56-4d29-998f-5512bb795d44
title: Konto Rechte Konstanten (nttscapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d5b16b75af89773df969ec78b771986b0a73dfb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215693"
---
# <a name="account-rights-constants"></a>Konto Rechte Konstanten

Konto Rechte bestimmen den Typ der Anmeldung, die von einem Benutzerkonto durchgeführt werden kann. Ein Administrator weist Benutzer-und Gruppenkonten Konto Rechte zu. Zu den Konto rechten jedes Benutzers gehören die Berechtigungen, die dem Benutzer erteilt wurden, und die Gruppen, zu denen der Benutzer gehört.

Ein Systemadministrator kann die Funktionen der [*lokalen Sicherheits Autorität (Local Security Authority*](/windows/desktop/SecGloss/l-gly) , LSA) verwenden, um mit Konto rechten zu arbeiten. Mit den Funktionen [**lsaaddaccounzghts**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaaddaccountrights) und [**lsareporveaccounzghts**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaremoveaccountrights) werden Konto Rechte eines Kontos hinzugefügt oder entfernt. Mit der [**lsaenumerateaccountrghts**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaenumerateaccountrights) -Funktion werden die Konto Rechte aufgelistet, die von einem angegebenen Konto gehalten werden. Die [**lsaenumerateaccountenwithuserright**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaenumerateaccountswithuserright) -Funktion Listet die Konten auf, die ein bestimmtes Konto Recht enthalten.

Die folgenden Konto Recht Konstanten werden verwendet, um die Anmelde Fähigkeit eines Kontos zu steuern. Die [**LogonUser**](/windows/desktop/api/winbase/nf-winbase-logonusera) -Funktion oder die [**LsaLogonUser**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsalogonuser) -Funktion schlägt fehl, wenn das angemeldete Konto nicht über die erforderlichen Konto Rechte für den Typ der ausgeführten Anmeldung verfügt.



| Konstante/Wert                                                                                                                                                                                                                                                                                                                           | BESCHREIBUNG                                                                                            |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------|
| <span id="SE_BATCH_LOGON_NAME"></span><span id="se_batch_logon_name"></span><dl> <dt>**SE \_ Text für den Batch \_ Anmelde \_ Namen**</dt> <dt>("Setup-logonright")</dt> </dl>                                                                         | Erforderlich, damit sich ein Konto mithilfe des Batch-Anmelde Typs anmelden können.<br/>                               |
| <span id="SE_DENY_BATCH_LOGON_NAME"></span><span id="se_deny_batch_logon_name"></span><dl> <dt>**SE \_ Text für den \_ Batch \_ Anmelde \_ Namen ablehnen**</dt> <dt>("Setup Batch logonright")</dt> </dl>                                                     | Verweigert einem Konto explizit das Recht, sich mithilfe des Batch-Anmelde Typs anzumelden.<br/>                |
| <span id="SE_DENY_INTERACTIVE_LOGON_NAME"></span><span id="se_deny_interactive_logon_name"></span><dl> <dt>**SE \_ Den Text für den \_ interaktiven \_ Anmelde \_ Namen ablehnen**</dt> <dt>("syinteractivelogonright")</dt> </dl>                             | Verweigert einem Konto explizit das Recht, sich mithilfe des interaktiven Anmelde Typs anzumelden.<br/>          |
| <span id="SE_DENY_NETWORK_LOGON_NAME"></span><span id="se_deny_network_logon_name"></span><dl> <dt>**SE \_ Text für den \_ Netzwerk \_ Anmelde \_ Namen verweigern**</dt> <dt>("" "" "*" "" ""</dt> </dl>                                             | Verweigert einem Konto explizit das Recht, sich mithilfe des Netzwerk Anmelde Typs anzumelden.<br/>              |
| <span id="SE_DENY_REMOTE_INTERACTIVE_LOGON_NAME"></span><span id="se_deny_remote_interactive_logon_name"></span><dl> <dt>**SE \_ Ablehnen des Texts für den \_ Remote \_ interaktiven \_ Anmelde \_ Namen**</dt> <dt>("" "" "" "" "" "</dt> , </dl> | Verweigert einem Konto explizit das Recht, sich Remote mithilfe des interaktiven Anmelde Typs anzumelden.<br/> |
| <span id="SE_DENY_SERVICE_LOGON_NAME"></span><span id="se_deny_service_logon_name"></span><dl> <dt>**SE \_ Text für den \_ \_ Anmelde \_ Namen des Diensts verweigern**</dt> <dt>("" ""</dt> </dl>                                             | Verweigert einem Konto explizit das Recht, sich mithilfe des Dienst Anmelde Typs anzumelden.<br/>              |
| <span id="SE_INTERACTIVE_LOGON_NAME"></span><span id="se_interactive_logon_name"></span><dl> <dt>**SE \_ Interaktiver \_ Anmelde \_ Name**</dt> <dt>Text ("SeInteractiveLogonRight")</dt> </dl>                                                 | Erforderlich, damit sich ein Konto mithilfe des interaktiven Anmelde Typs anmelden muss.<br/>                         |
| <span id="SE_NETWORK_LOGON_NAME"></span><span id="se_network_logon_name"></span><dl> <dt>**SE \_ Textfeld für den Netzwerk \_ Anmelde \_ Namen**</dt> <dt>("SeNetworkLogonRight")</dt> </dl>                                                                 | Erforderlich, damit sich ein Konto mithilfe des Netzwerk Anmelde Typs anmelden muss.<br/>                             |
| <span id="SE_REMOTE_INTERACTIVE_LOGON_NAME"></span><span id="se_remote_interactive_logon_name"></span><dl> <dt>**SE \_ Text für den \_ interaktiven Remote \_ Anmelde \_ Namen**</dt> <dt>("seremoteinteractivelogonright")</dt> </dl>                     | Erforderlich, damit sich ein Konto mithilfe des interaktiven Anmelde Typs Remote anmelden können.<br/>                |
| <span id="SE_SERVICE_LOGON_NAME"></span><span id="se_service_logon_name"></span><dl> <dt>**SE \_ Dienst \_ Anmelde \_ Name**</dt> <dt>Text ("SeServiceLogonRight")</dt> </dl>                                                                 | Erforderlich, damit sich ein Konto mit dem Anmeldetyp des Diensts anmelden muss.<br/>                             |



## <a name="remarks"></a>Bemerkungen

Die SE \_ Deny-Rechte überschreiben die entsprechenden Konto Rechte. Ein Administrator kann einem Konto ein SE \_ Deny-Recht zuweisen, um alle Anmelde Rechte außer Kraft zu setzen, die ein Konto möglicherweise aufgrund einer Gruppenmitgliedschaft besitzt. Beispielsweise können Sie allen Benutzern den Namen des Benutzer Zugriffs für die SE- \_ Netzwerk Anmeldung zuweisen, \_ \_ den Administratoren jedoch den \_ Namen des Netzwerk Anmelde namens "SE Deny" zuweisen \_ \_ \_ , um die Remote Verwaltung von Computern zu verhindern.

Alle LSA-Funktionen, die in der obigen Einführung erwähnt werden, unterstützen sowohl Konto Rechte als auch [Berechtigungen](privilege-constants.md). Anders als bei Berechtigungen werden Konto Rechte jedoch nicht von den Funktionen [**LookupPrivilegeValue**](/windows/desktop/api/Winbase/nf-winbase-lookupprivilegevaluea) und [**lookupprivilegilegename**](/windows/desktop/api/Winbase/nf-winbase-lookupprivilegenamea) unterstützt. Die Funktion [**GetTokenInformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-gettokeninformation) erhält Informationen zu Konto rechten, wenn tokenGroups und nicht tokenprivileges als Wert des *tokeninformationclass* -Parameters angegeben wird.

Die vorangehenden Konto Recht Konstanten werden als Zeichen folgen in "nttscapi. h" definiert. Beispielsweise ist die Konstante für den \_ interaktiven \_ Anmelde Namen von SE \_ als "SeInteractiveLogonRight" definiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Ntabcapi. h</dt> </dl> |



 

