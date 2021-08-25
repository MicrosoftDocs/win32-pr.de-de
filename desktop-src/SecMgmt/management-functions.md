---
description: Listet die Vom Sicherheitskonfigurationstoolsatz bereitgestellten Unterstützungsfunktionen auf.
ms.assetid: 5a771014-1706-490f-8540-ec516652cb83
title: Sicherheitsverwaltungsfunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72df5c905207b707a21a97842c62385969fb2ac2d32279b9c7fa9f5a32c4fbbd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117968936"
---
# <a name="security-management-functions"></a>Sicherheitsverwaltungsfunktionen

Dieser Abschnitt enthält Themen für die folgenden Gruppen von Funktionen:

-   [Rückruffunktionen für Anlagen](#attachment-callback-functions)
-   [Funktionen der Anlagen-Engine](#attachment-engine-functions)
-   [LSA-Richtlinienfunktionen](#lsa-policy-functions)
    -   [Richtlinienfunktionen](#lsa-policy-functions)
    -   [Kontofunktionen](#account-functions)
    -   [Funktionen für vertrauenswürdige Domänen](#trusted-domain-functions)
    -   [Private Datenfunktionen](#private-data-functions)
    -   [Sonstige Funktionen](#miscellaneous-functions)
-   [Verwaltete Dienstkontofunktionen](#managed-service-account-functions)
-   [Kennwortfilterfunktionen](#password-filter-functions)
-   [Sicherere Funktionen](#safer-functions)

## <a name="attachment-callback-functions"></a>Rückruffunktionen für Anlagen

Die folgenden Unterstützungsfunktionen werden vom Sicherheitskonfigurationstoolsatz bereitgestellt und können von Anlagen-Engines und Erweiterungs-Snap-Ins verwendet werden, um Konfigurationsdaten zu lesen und zu schreiben.



| Rückruffunktion                                         | Beschreibung                                                                                 |
|-----------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [**PFSCE \_ FREE \_ INFO**](/windows/win32/api/scesvc/nc-scesvc-pfsce_free_info)<br/>   | Wird verwendet, um von diesen Unterstützungsfunktionen zugeordneten Arbeitsspeicher frei zu geben.<br/>                        |
| [**\_PFSCE-PROTOKOLLINFORMATIONEN \_**](/windows/win32/api/scesvc/nc-scesvc-pfsce_log_info)<br/>     | Wird zum Protokollieren von Nachrichten in der Konfigurations- oder Analyseprotokolldatei verwendet.<br/>          |
| [**\_PFSCE-ABFRAGEINFORMATIONEN \_**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info)<br/> | Wird zum Abfragen der Konfigurations- und Analyseinformationen für einen bestimmten Dienst verwendet.<br/> |
| [**PFSCE \_ SET \_ INFO**](/windows/win32/api/scesvc/nc-scesvc-pfsce_set_info)<br/>     | Wird zum Festlegen von Konfigurations- und Analyseinformationen für einen bestimmten Dienst verwendet.<br/>       |



 

## <a name="attachment-engine-functions"></a>Funktionen der Anlagen-Engine



| Funktion                                                              | Beschreibung                                                                                                                                                                                       |
|-----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SceSvcAttachmentAnalyze**](scesvcattachmentanalyze.md)<br/> | Wird von der Anlagen-Engine-DLL implementiert. Die Sicherheitskonfigurations-Engine ruft diese Funktion auf, wenn das System analysiert wird.<br/>                                                           |
| [**SceSvcAttachmentConfig**](scesvcattachmentconfig.md)<br/>   | Wird von der Anlagen-Engine-DLL implementiert. Die Sicherheitskonfigurations-Engine ruft diese Funktion auf, wenn das System konfiguriert ist.<br/>                                                         |
| [**SceSvcAttachmentUpdate**](scesvcattachmentupdate.md)<br/>   | Wird von der Anlagen-Engine-DLL implementiert. Die Sicherheitskonfigurations-Engine ruft diese Funktion auf, wenn sie eine Anforderung zur Konfigurationsaktualisierung von der Snap-In-Erweiterung für Anlagen empfängt.<br/> |



 

## <a name="lsa-policy-functions"></a>LSA-Richtlinienfunktionen

Die folgenden Themen enthalten Referenzinformationen zu den Richtlinienfunktionen der lokalen Sicherheitsstelle (Local [*Security Authority,*](/windows/desktop/SecGloss/l-gly) LSA).



| Thema                               | Beschreibung                                                                                                                                                                                   |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Richtlinienfunktionen<br/>         | Detailfunktionen, die zum Öffnen des lokalen [**Richtlinienobjekts**](policy-object.md) und zum Festlegen oder Abrufen globaler Richtlinieninformationen verwendet werden.<br/>                                                  |
| Kontofunktionen<br/>        | Detailsfunktionen, die zum Verwalten von Kontoberechtigungen und zum Erstellen und Löschen von Benutzerkonten verwendet werden.<br/>                                                                                       |
| Funktionen für vertrauenswürdige Domänen<br/> | Detailfunktionen zum Erstellen und Löschen vertrauenswürdiger Domänenbeziehungen sowie zum Festlegen und Abrufen von Informationen zu diesen vertrauenswürdigen Domänen.<br/>                                          |
| Private Datenfunktionen<br/>   | Verwenden Sie nicht die privaten LSA-Datenfunktionen. Verwenden Sie stattdessen die [**Funktionen CryptProtectData**](/windows/desktop/api/dpapi/nf-dpapi-cryptprotectdata) und [**CryptUnprotectData.**](/windows/desktop/api/dpapi/nf-dpapi-cryptunprotectdata)<br/> |
| Sonstige Funktionen<br/>  | Detailsfunktionen, die an anderer Stelle nicht beschrieben werden.<br/>                                                                                                                                         |



 

### <a name="policy-functions"></a>Richtlinienfunktionen

Die folgenden Funktionen aufzählen Benutzerkonten und vertrauenswürdige Domänen, empfangen Richtlinienänderungsbenachrichtigungen und suchen Kontonamen und SIDs.



| Funktion                                                                                          | Beschreibung                                                                                                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**LsaEnumerateAccountsWithUserRight**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumerateaccountswithuserright)<br/>         | Enumeriert alle Konten, die über eine angegebene Benutzerberechtigung verfügen.<br/>                                                                                                                                                                                                                                                                         |
| [**LsaEnumerateTrustedDomainsEx**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumeratetrusteddomainsex)<br/>                   | Enumeriert die vertrauenswürdigen Domänen.<br/>                                                                                                                                                                                                                                                                                                            |
| [**LsaLookupNames**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalookupnames)<br/>                                               | Karten die angegebenen Namen in ihre SIDs ein. Gibt die SID als RID-/Domänen-SID-Paar zurück.<br/>                                                                                                                                                                                                                                                         |
| [**LsaLookupNames2**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalookupnames2)<br/>                                             | Karten die angegebenen Namen in ihre SIDs ein. Gibt die SID als einzelnes Element zurück.<br/>                                                                                                                                                                                                                                                               |
| [**LsaLookupPrivilegeValue**](/windows/desktop/api/ntlsa/nf-ntlsa-lsalookupprivilegevalue)<br/>                             | Ruft den [*lokal eindeutigen Bezeichner*](/windows/desktop/SecGloss/l-gly) (LUID) ab, der von der lokalen Sicherheitsstelle [*(Local Security Authority,*](/windows/desktop/SecGloss/l-gly) LSA) verwendet wird, um den angegebenen Berechtigungsnamen anzugeben.<br/> |
| [**LsaLookupSids**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalookupsids)<br/>                                                 | Karten die angegebenen Kontonamen ihren SIDs.<br/>                                                                                                                                                                                                                                                                                            |
| [**LsaRegisterPolicyChangeNotification**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaregisterpolicychangenotification)<br/>     | Registriert ein Ereignisobjekt, um Benachrichtigungen zu empfangen, wenn sich die lokalen Richtlinieninformationen ändern.<br/>                                                                                                                                                                                                                                              |
| [**LsaUnregisterPolicyChangeNotification**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaunregisterpolicychangenotification)<br/> | Aufheben der Registrierung eines Ereignisobjekts, das Richtlinienänderungsbenachrichtigungen empfängt.<br/>                                                                                                                                                                                                                                                                 |



 

### <a name="account-functions"></a>Kontofunktionen

Mit den folgenden Funktionen werden Berechtigungen für ein Konto hinzugefügt, aufzählt und gelöscht.



| Funktion                                                                  | Beschreibung                                                                                                  |
|---------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**LsaAddAccountRights**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaaddaccountrights)<br/>             | Hinzufügen von Berechtigungen zu einem Konto. Wenn das Konto noch nicht vorhanden ist, wird es erstellt.<br/>              |
| [**LsaEnumerateAccountRights**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumerateaccountrights)<br/> | Enumerieren Sie die Berechtigungen, die einem Konto erteilt wurden.<br/>                                                  |
| [**LsaRemoveAccountRights**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaremoveaccountrights)<br/>       | Entfernen Sie Berechtigungen aus einem Konto. Wenn alle Berechtigungen entfernt werden, wird das Konto gelöscht.<br/> |



 

### <a name="trusted-domain-functions"></a>Funktionen für vertrauenswürdige Domänen

Die folgenden Funktionen erstellen, aufzählen und löschen vertrauenswürdige Domänen und legen vertrauenswürdige Domäneninformationen fest und rufen sie ab.



| Funktion                                                                                                                                                    | Beschreibung                                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [**LsaCreateTrustedDomainEx**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsacreatetrusteddomainex)<br/>                                                                                     | Erstellt ein neues [**TrustedDomain-Objekt.**](trusteddomain-object.md)<br/>            |
| [**LsaDeleteTrustedDomain**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsadeletetrusteddomain)<br/>                                                                                         | Entfernt ein [**TrustedDomain-Objekt.**](trusteddomain-object.md)<br/>                |
| [**LsaEnumerateTrustedDomains**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumeratetrusteddomains)<br/> [**LsaEnumerateTrustedDomainsEx**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumeratetrusteddomainsex)<br/> | Enumeriert die Domänen, die derzeit vom lokalen System als vertrauenswürdig eingestuft werden.<br/>                  |
| [**LsaOpenTrustedDomainByName**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaopentrusteddomainbyname)<br/>                                                                                 | Öffnet ein Handle für ein [**TrustedDomain-Objekt.**](trusteddomain-object.md)<br/>      |
| [**LsaQueryTrustedDomainInfo**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaquerytrusteddomaininfo)<br/>                                                                                   | Ruft Informationen zu einer vertrauenswürdigen Domäne ab. Die Domäne wird durch SID angegeben.<br/>  |
| [**LsaQueryTrustedDomainInfoByName**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaquerytrusteddomaininfobyname)<br/>                                                                       | Ruft Informationen zu einer vertrauenswürdigen Domäne ab. Die Domäne wird durch den Namen angegeben.<br/> |
| [**LsaSetTrustedDomainInfoByName**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsasettrusteddomaininfobyname)<br/>                                                                           | Legt Informationen für eine vertrauenswürdige Domäne fest. Die Domäne wird durch den Namen angegeben.<br/>        |
| [**LsaSetTrustedDomainInformation**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsasettrusteddomaininformation)<br/>                                                                         | Legt Informationen für eine vertrauenswürdige Domäne fest. Die Domäne wird durch SID angegeben.<br/>         |



 

### <a name="private-data-functions"></a>Private Datenfunktionen

Verwenden Sie nicht die privaten LSA-Datenfunktionen. Verwenden Sie stattdessen die [**Funktionen CryptProtectData**](/windows/desktop/api/dpapi/nf-dpapi-cryptprotectdata) und [**CryptUnprotectData.**](/windows/desktop/api/dpapi/nf-dpapi-cryptunprotectdata)



| Funktion                                                            | Beschreibung                                 |
|---------------------------------------------------------------------|---------------------------------------------|
| [**LsaRetri browsePrivateData**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaretrieveprivatedata)<br/> | Ruft eine Zeichenfolge ab und entschlüsselt sie.<br/> |
| [**LsaStorePrivateData**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsastoreprivatedata)<br/>       | Verschlüsselt und speichert eine Zeichenfolge.<br/>    |



 

### <a name="miscellaneous-functions"></a>Sonstige Funktionen

Die LSA-Richtlinien-API verfügt über die folgenden drei Funktionen, die nicht in eine der anderen Kategorien von LSA Policy-Funktionen passen.



| Funktion                                                          | Beschreibung                                                                                                                       |
|-------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [**LsaClose**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaclose)<br/>                           | Schließt ein Handle für ein [**Policy-Objekt**](policy-object.md) oder ein [**TrustedDomain-Objekt.**](trusteddomain-object.md)<br/> |
| [**LsaFreeMemory**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsafreememory)<br/>                 | Gibt einen Puffer frei, der von einer LSA-Funktion zugeordnet wird.<br/>                                                                           |
| [**LsaNtStatusToWinError**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsantstatustowinerror)<br/> | Konvertiert einen **NTSTATUS-Wert** in einen Windows Fehlercode.<br/>                                                                |



 

## <a name="managed-service-account-functions"></a>Verwaltete Dienstkontofunktionen

Die folgenden Funktionen werden verwendet, um verwaltete Dienstkonten zu erstellen, aufzählen, zu suchen und zu löschen.



| Funktion                                                                      | Beschreibung                                                                                                                 |
|-------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| [**NetAddServiceAccount**](/windows/desktop/api/Lmaccess/nf-lmaccess-netaddserviceaccount)<br/>               | Erstellt ein verwaltetes Dienstkonto.<br/>                                                                               |
| [**NetEnumerateServiceAccounts**](/windows/desktop/api/Lmaccess/nf-lmaccess-netenumerateserviceaccounts)<br/> | Enumeriert die Serverkonten auf dem angegebenen Server.<br/>                                                          |
| [**NetIsServiceAccount**](/windows/desktop/api/Lmaccess/nf-lmaccess-netisserviceaccount)<br/>                 | Testet, ob das angegebene Dienstkonto im Netlogon-Speicher auf dem angegebenen Server vorhanden ist.<br/>                |
| [**NetRemoveServiceAccount**](/windows/desktop/api/Lmaccess/nf-lmaccess-netremoveserviceaccount)<br/>         | Löscht das angegebene Dienstkonto aus der [Active Directory-Datenbank.](/windows/desktop/AD/active-directory-domain-services)<br/> |



 

## <a name="password-filter-functions"></a>Kennwortfilterfunktionen

Die folgenden [*Kennwortfilterfunktionen*](/windows/desktop/SecGloss/p-gly) werden von benutzerdefinierten Kennwortfilter-DLLs implementiert, um Kennwortfilterung und Kennwortänderungsbenachrichtigungen zu ermöglichen.



| Funktion                                                            | Beschreibung                                                     |
|---------------------------------------------------------------------|-----------------------------------------------------------------|
| [**InitializeChangeNotify**](/windows/desktop/api/Ntsecapi/nc-ntsecapi-psam_init_notification_routine)<br/> | Gibt an, dass eine Kennwortfilter-DLL initialisiert wird.<br/> |
| [**PasswordChangeNotify**](/windows/desktop/api/Ntsecapi/nc-ntsecapi-psam_password_notification_routine)<br/>     | Gibt an, dass ein Kennwort geändert wurde.<br/>          |
| [**PasswordFilter**](/windows/desktop/api/Ntsecapi/nc-ntsecapi-psam_password_filter_routine)<br/>                 | Überprüft ein neues Kennwort basierend auf der Kennwortrichtlinie.<br/>   |



 

## <a name="safer-functions"></a>Sicherere Funktionen

Die folgenden sichereren Funktionen können verwendet werden, um die sicherere Ebene von ausführbaren Dateien zu überprüfen und Ereignisse zu protokollieren.



| Funktion                                                         | Beschreibung                                                                                                                                                                          |
|------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SaferCloseLevel**](/windows/desktop/api/WinSafer/nf-winsafer-safercloselevel)                       | Schließt ein SAFER \_ LEVEL \_ HANDLE, das mithilfe der [**SaferIdentifyLevel-Funktion**](/windows/desktop/api/WinSafer/nf-winsafer-saferidentifylevel) oder der [**SaferCreateLevel-Funktion geöffnet**](/windows/desktop/api/WinSafer/nf-winsafer-safercreatelevel) wurde.<br/> |
| [**SaferComputeTokenFromLevel**](/windows/desktop/api/WinSafer/nf-winsafer-safercomputetokenfromlevel) | Schränkt ein Token mithilfe von Einschränkungen ein, die durch ein SAFER \_ LEVEL \_ HANDLE angegeben werden.<br/>                                                                                                 |
| [**SaferCreateLevel**](/windows/desktop/api/WinSafer/nf-winsafer-safercreatelevel)                     | Öffnet ein \_ SICHERERES \_ LEVEL-HANDLE.<br/>                                                                                                                                             |
| [**SaferGetLevelInformation**](/windows/desktop/api/WinSafer/nf-winsafer-safergetlevelinformation)     | Ruft Informationen zu einer Richtlinienebene ab.<br/>                                                                                                                               |
| [**SaferGetPolicyInformation**](/windows/desktop/api/WinSafer/nf-winsafer-safergetpolicyinformation)   | Ruft Informationen zu einer Richtlinie ab.<br/>                                                                                                                                     |
| [**SaferIdentifyLevel**](/windows/desktop/api/WinSafer/nf-winsafer-saferidentifylevel)                 | Ruft Informationen zu einer Ebene ab.<br/>                                                                                                                                      |
| [**SaferiIsExecutableFileType**](/windows/desktop/api/WinSafer/nf-winsafer-saferiisexecutablefiletype) | Bestimmt, ob eine angegebene Datei eine ausführbare Datei ist.<br/>                                                                                                                |
| [**SaferRecordEventLogEntry**](/windows/desktop/api/WinSafer/nf-winsafer-saferrecordeventlogentry)     | Sendet eine Nachricht an das Ereignisprotokoll.<br/>                                                                                                                                         |
| [**SaferSetLevelInformation**](/windows/desktop/api/WinSafer/nf-winsafer-safersetlevelinformation)     | Legt die Informationen zu einer Richtlinienebene fest.<br/>                                                                                                                                |
| [**SaferSetPolicyInformation**](/windows/desktop/api/WinSafer/nf-winsafer-safergetlevelinformation)    | Legt die globalen Richtliniensteuerelemente fest.<br/>                                                                                                                                          |



 

 

