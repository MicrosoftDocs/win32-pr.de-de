---
description: Kontorechte bestimmen den Anmeldetyp, den ein Benutzerkonto ausführen kann. Ein Administrator weist Benutzer- und Gruppenkonten Kontorechte zu. Zu den Kontorechten jedes Benutzers gehören die rechte, die dem Benutzer und den Gruppen gewährt werden, zu denen der Benutzer gehört.
ms.assetid: 42139d33-2d56-4d29-998f-5512bb795d44
title: Kontorechtekonst constants (Ntsecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4285561761908308f67585544bef6c87d2f0ebbaa25de9989f53fcab051b79b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117785368"
---
# <a name="account-rights-constants"></a>Kontorechtekonst constants

Kontorechte bestimmen den Anmeldetyp, den ein Benutzerkonto ausführen kann. Ein Administrator weist Benutzer- und Gruppenkonten Kontorechte zu. Zu den Kontorechten jedes Benutzers gehören diejenigen, die dem Benutzer und den Gruppen gewährt werden, zu denen der Benutzer gehört.

Ein Systemadministrator kann die [*Funktionen der lokalen Sicherheitsstelle (Local Security Authority,*](/windows/desktop/SecGloss/l-gly) LSA) verwenden, um mit Kontorechten zu arbeiten. Mit [**den Funktionen LsaAddAccountRights**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaaddaccountrights) und [**LsaRemoveAccountRights**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaremoveaccountrights) werden Kontorechte zu einem Konto hinzugefügt oder daraus entfernt. Die [**LsaEnumerateAccountRights-Funktion**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaenumerateaccountrights) aufzählt die Kontorechte eines angegebenen Kontos. Die [**LsaEnumerateAccountsWithUserRight-Funktion**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaenumerateaccountswithuserright) enumeriert die Konten, die ein angegebenes Kontorecht besitzen.

Die folgenden Kontorechtkonst constants werden verwendet, um die Anmeldefähigkeit eines Kontos zu steuern. Die [**LogonUser-**](/windows/desktop/api/winbase/nf-winbase-logonusera) oder [**LsaLogonUser-Funktionen**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsalogonuser) führen zu einem Fehler, wenn das angemeldete Konto nicht über die Kontorechte verfügt, die für den Anmeldetyp erforderlich sind.



| Konstante/Wert                                                                                                                                                                                                                                                                                                                           | Beschreibung                                                                                            |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------|
| <span id="SE_BATCH_LOGON_NAME"></span><span id="se_batch_logon_name"></span><dl> <dt>**SE \_ BATCH \_ LOGON \_ NAME**</dt> <dt>TEXT("SeBatchLogonRight")</dt> </dl>                                                                         | Erforderlich, damit sich ein Konto mithilfe des Batchanmeldungstyps anmelden kann.<br/>                               |
| <span id="SE_DENY_BATCH_LOGON_NAME"></span><span id="se_deny_batch_logon_name"></span><dl> <dt>**SE \_ DENY \_ BATCH \_ LOGON \_ NAME**</dt> <dt>TEXT("SeDenyBatchLogonRight")</dt> </dl>                                                     | Verweigert einem Konto explizit das Recht zur Anmeldung mithilfe des Batchanmeldungstyps.<br/>                |
| <span id="SE_DENY_INTERACTIVE_LOGON_NAME"></span><span id="se_deny_interactive_logon_name"></span><dl> <dt>**SE \_ DENY \_ INTERACTIVE \_ LOGON \_ NAME**</dt> <dt>TEXT("SeDenyInteractiveLogonRight")</dt> </dl>                             | Verweigert einem Konto explizit das Recht, sich mithilfe des interaktiven Anmeldetyps anmelden zu können.<br/>          |
| <span id="SE_DENY_NETWORK_LOGON_NAME"></span><span id="se_deny_network_logon_name"></span><dl> <dt>**SE \_ DENY \_ NETWORK \_ LOGON \_ NAME**</dt> <dt>TEXT("SeDenyNetworkLogonRight")</dt> </dl>                                             | Verweigert einem Konto explizit das Recht, sich mithilfe des Netzwerkanmeldungstyps zu anmelden.<br/>              |
| <span id="SE_DENY_REMOTE_INTERACTIVE_LOGON_NAME"></span><span id="se_deny_remote_interactive_logon_name"></span><dl> <dt>**SE \_ DENY \_ REMOTE \_ INTERACTIVE \_ LOGON \_ NAME**</dt> <dt>TEXT("SeDenyRemoteInteractiveLogonRight")</dt> </dl> | Verweigert einem Konto explizit das Recht, sich mithilfe des interaktiven Anmeldetyps remote anmelden zu können.<br/> |
| <span id="SE_DENY_SERVICE_LOGON_NAME"></span><span id="se_deny_service_logon_name"></span><dl> <dt>**SE \_ DENY \_ SERVICE \_ LOGON \_ NAME**</dt> <dt>TEXT("SeDenyServiceLogonRight")</dt> </dl>                                             | Verweigert einem Konto explizit das Recht, sich mithilfe des Dienstanmeldungstyps zu anmelden.<br/>              |
| <span id="SE_INTERACTIVE_LOGON_NAME"></span><span id="se_interactive_logon_name"></span><dl> <dt>**SE \_ INTERACTIVE \_ LOGON \_ NAME**</dt> <dt>TEXT("SeInteractiveLogonRight")</dt> </dl>                                                 | Erforderlich, damit sich ein Konto mit dem interaktiven Anmeldetyp anmelden kann.<br/>                         |
| <span id="SE_NETWORK_LOGON_NAME"></span><span id="se_network_logon_name"></span><dl> <dt>**SE \_ NETWORK \_ LOGON \_ NAME**</dt> <dt>TEXT("SeNetworkLogonRight")</dt> </dl>                                                                 | Erforderlich, damit sich ein Konto mit dem Netzwerkanmeldungstyp anmelden kann.<br/>                             |
| <span id="SE_REMOTE_INTERACTIVE_LOGON_NAME"></span><span id="se_remote_interactive_logon_name"></span><dl> <dt>**SE \_ REMOTE \_ INTERACTIVE \_ LOGON \_ NAME**</dt> <dt>TEXT("SeRemoteInteractiveLogonRight")</dt> </dl>                     | Erforderlich, damit sich ein Konto remote mithilfe des interaktiven Anmeldetyps anmelden kann.<br/>                |
| <span id="SE_SERVICE_LOGON_NAME"></span><span id="se_service_logon_name"></span><dl> <dt>**SE \_ SERVICE \_ LOGON \_ NAME**</dt> <dt>TEXT("SeServiceLogonRight")</dt> </dl>                                                                 | Erforderlich, damit sich ein Konto mithilfe des Dienstanmeldungstyps anmelden kann.<br/>                             |



## <a name="remarks"></a>Hinweise

Die SE \_ DENY-Rechte setzen die entsprechenden Kontorechte außer Kraft. Ein Administrator kann einem Konto ein SE DENY-Recht zuweisen, um alle Anmelderechte außer Kraft zu setzen, die ein Konto als Ergebnis einer \_ Gruppenmitgliedschaft haben kann. Sie können z. B. das SE-NETZWERKANMELDUNGSNAME-Recht jedem zuweisen, aber administratoren das \_ \_ SE-Recht \_ \_ \_ NETZWERKANMELDUNGSNAME \_ VERWEIGERN zuweisen, um die Remoteverwaltung von \_ Computern zu verhindern.

Alle in der obigen Einführung erwähnten LSA-Funktionen unterstützen sowohl Kontorechte als [auch Berechtigungen.](privilege-constants.md) Im Gegensatz zu Berechtigungen werden Kontorechte jedoch nicht von den [**Funktionen LookupPrivilegeValue**](/windows/desktop/api/Winbase/nf-winbase-lookupprivilegevaluea) und [**LookupPrivilegeName**](/windows/desktop/api/Winbase/nf-winbase-lookupprivilegenamea) unterstützt. Die [**GetTokenInformation-Funktion**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-gettokeninformation) erhält Informationen zu Kontorechten, wenn TokenGroups und nicht TokenPrivileges als Wert des *TokenInformationClass-Parameters angegeben* wird.

Die oben genannten Kontorechtkonst constants werden als Zeichenfolgen in Ntsecapi.h definiert. Beispielsweise ist die SE \_ INTERACTIVE \_ LOGON \_ NAME-Konstante als "SeInteractiveLogonRight" definiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Ntsecapi.h</dt> </dl> |



 

