---
description: Listet die vom Sicherheitskonfigurations-Toolset bereitgestellten Unterstützungsfunktionen auf.
ms.assetid: 5a771014-1706-490f-8540-ec516652cb83
title: Sicherheits Verwaltungsfunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f5c17efd55b1dbb806295ac0a83763257ffcc97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867639"
---
# <a name="security-management-functions"></a>Sicherheits Verwaltungsfunktionen

Dieser Abschnitt enthält Themen zu den folgenden Funktionsgruppen:

-   [Anlagen Rückruf Funktionen](#attachment-callback-functions)
-   [Anlagen-Engine-Funktionen](#attachment-engine-functions)
-   [LSA-Richtlinien Funktionen](#lsa-policy-functions)
    -   [Richtlinien Funktionen](#lsa-policy-functions)
    -   [Kontofunktionen](#account-functions)
    -   [Vertrauenswürdige Domänen Funktionen](#trusted-domain-functions)
    -   [Private Datenfunktionen](#private-data-functions)
    -   [Sonstige Funktionen](#miscellaneous-functions)
-   [Verwaltete Dienst Kontofunktionen](#managed-service-account-functions)
-   [Kenn Wort Filter Funktionen](#password-filter-functions)
-   [Sicherere Funktionen](#safer-functions)

## <a name="attachment-callback-functions"></a>Anlagen Rückruf Funktionen

Die folgenden Unterstützungsfunktionen werden vom Sicherheitskonfigurations-Toolset bereitgestellt und können von Anlagen-Engines und Erweiterungs-Snap-Ins verwendet werden, um Konfigurationsdaten zu lesen und zu schreiben.



| Rückruffunktion                                         | BESCHREIBUNG                                                                                 |
|-----------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [**Kostenlose pfsce- \_ \_ Informationen**](/windows/win32/api/scesvc/nc-scesvc-pfsce_free_info)<br/>   | Wird verwendet, um Arbeitsspeicher freizugeben, der von diesen Unterstützungsfunktionen zugeordnet<br/>                        |
| [**pfsce- \_ Protokoll \_ Informationen**](/windows/win32/api/scesvc/nc-scesvc-pfsce_log_info)<br/>     | Wird verwendet, um eine Meldung in der Konfigurations Protokolldatei oder der Analyseprotokoll Datei zu protokollieren.<br/>          |
| [**pfsce- \_ Abfrage \_ Informationen**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info)<br/> | Wird verwendet, um die Konfigurations-und Analyse Informationen für einen bestimmten Dienst abzufragen.<br/> |
| [**pfsce- \_ festgelegte \_ Informationen**](/windows/win32/api/scesvc/nc-scesvc-pfsce_set_info)<br/>     | Wird verwendet, um Konfigurations-und Analyse Informationen für einen bestimmten Dienst festzulegen.<br/>       |



 

## <a name="attachment-engine-functions"></a>Anlagen-Engine-Funktionen



| Funktion                                                              | BESCHREIBUNG                                                                                                                                                                                       |
|-----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Scesvpetachmentanalysis**](scesvcattachmentanalyze.md)<br/> | Wird von der Anlage-Engine-dll implementiert. Die Sicherheitskonfigurations-Engine ruft diese Funktion auf, wenn das System analysiert wird.<br/>                                                           |
| [**Scesvalisitachmentconfig**](scesvcattachmentconfig.md)<br/>   | Wird von der Anlage-Engine-dll implementiert. Die Sicherheitskonfigurations-Engine ruft diese Funktion auf, wenn das System konfiguriert ist.<br/>                                                         |
| [**Scesvertachmentupdate**](scesvcattachmentupdate.md)<br/>   | Wird von der Anlage-Engine-dll implementiert. Die Sicherheitskonfigurations-Engine ruft diese Funktion auf, wenn Sie eine Konfigurations Aktualisierungs Anforderung von der Erweiterungs-Snap-in-Erweiterung empfängt.<br/> |



 

## <a name="lsa-policy-functions"></a>LSA-Richtlinien Funktionen

Die folgenden Themen enthalten Referenzinformationen für die Richtlinien für die [*Lokale Sicherheits Autorität*](/windows/desktop/SecGloss/l-gly) (LSA).



| Thema                               | BESCHREIBUNG                                                                                                                                                                                   |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Richtlinien Funktionen<br/>         | Detailfunktionen, die verwendet werden, um das lokale [**Richtlinien**](policy-object.md) Objekt zu öffnen und globale Richtlinien Informationen festzulegen oder abzurufen.<br/>                                                  |
| Kontofunktionen<br/>        | Detailfunktionen, die zum Verwalten von Konto Berechtigungen und zum Erstellen und Löschen von Benutzerkonten verwendet werden.<br/>                                                                                       |
| Vertrauenswürdige Domänen Funktionen<br/> | Detailfunktionen zum Erstellen und löschen vertrauenswürdiger Domänen Beziehungen und zum Festlegen und Abrufen von Informationen zu diesen vertrauenswürdigen Domänen.<br/>                                          |
| Private Datenfunktionen<br/>   | Verwenden Sie keine privaten LSA-Datenfunktionen. Verwenden Sie stattdessen die Funktionen " [**CryptProtectData**](/windows/desktop/api/dpapi/nf-dpapi-cryptprotectdata) " und " [**CryptUnprotectData**](/windows/desktop/api/dpapi/nf-dpapi-cryptunprotectdata) ".<br/> |
| Sonstige Funktionen<br/>  | Details, die nicht an anderer Stelle beschrieben werden.<br/>                                                                                                                                         |



 

### <a name="policy-functions"></a>Richtlinien Funktionen

Die folgenden Funktionen zählen Benutzerkonten und vertrauenswürdige Domänen auf, empfangen Richtlinien-Änderungs Benachrichtigungen und Such Kontonamen und SIDs.



| Funktion                                                                                          | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Lsaenumerateaccounpwithuserright**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumerateaccountswithuserright)<br/>         | Listet alle Konten auf, die über eine angegebene Benutzer Berechtigung verfügen.<br/>                                                                                                                                                                                                                                                                         |
| [**Lsaenumeratetrusteddomainsex**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumeratetrusteddomainsex)<br/>                   | Listet die vertrauenswürdigen Domänen auf.<br/>                                                                                                                                                                                                                                                                                                            |
| [**Lsalookupnames**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalookupnames)<br/>                                               | Ordnet die angegebenen Namen ihren SIDs zu. Gibt die SID als RID/Domänen-SID-paar zurück.<br/>                                                                                                                                                                                                                                                         |
| [**LsaLookupNames2**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalookupnames2)<br/>                                             | Ordnet die angegebenen Namen ihren SIDs zu. Gibt die SID als ein einzelnes Element zurück.<br/>                                                                                                                                                                                                                                                               |
| [**Lsalookupprivilegevalue**](/windows/desktop/api/ntlsa/nf-ntlsa-lsalookupprivilegevalue)<br/>                             | Ruft den lokalen [*eindeutigen Bezeichner*](/windows/desktop/SecGloss/l-gly) (LUID) ab, der von der [*lokalen Sicherheits Autorität (Local Security Authority*](/windows/desktop/SecGloss/l-gly) , LSA) zum Darstellen des angegebenen Berechtigungs namens verwendet wird.<br/> |
| [**Lsalookupsids**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalookupsids)<br/>                                                 | Ordnet die angegebenen Kontonamen ihren SIDs zu.<br/>                                                                                                                                                                                                                                                                                            |
| [**Lsaregisterpolicychangenotifizierung**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaregisterpolicychangenotification)<br/>     | Registriert ein Ereignis Objekt, um Benachrichtigungen zu empfangen, wenn sich die Informationen der lokalen Richtlinie ändern.<br/>                                                                                                                                                                                                                                              |
| [**Lsaunregisterpolicychangenotifizierung**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaunregisterpolicychangenotification)<br/> | Hebt die Registrierung eines Ereignis Objekts auf, das Richtlinien Änderungs Benachrichtigungen empfängt.<br/>                                                                                                                                                                                                                                                                 |



 

### <a name="account-functions"></a>Kontofunktionen

Mit den folgenden Funktionen werden Berechtigungen für ein Konto hinzugefügt, aufgelistet und gelöscht.



| Funktion                                                                  | BESCHREIBUNG                                                                                                  |
|---------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**Lsaaddaccountrghts**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaaddaccountrights)<br/>             | Fügen Sie einem Konto Berechtigungen hinzu. Wenn das Konto nicht bereits vorhanden ist, wird es erstellt.<br/>              |
| [**Lsaenumerateaccountrghts**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumerateaccountrights)<br/> | Listet die Berechtigungen auf, die einem Konto erteilt wurden.<br/>                                                  |
| [**Lsaremuveaccountrghts**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaremoveaccountrights)<br/>       | Entfernen Sie Berechtigungen aus einem Konto. Wenn alle Berechtigungen entfernt werden, wird das Konto gelöscht.<br/> |



 

### <a name="trusted-domain-functions"></a>Vertrauenswürdige Domänen Funktionen

Die folgenden Funktionen erstellen, auflisten und löschen vertrauenswürdiger Domänen und festlegen und Abrufen von Informationen zu vertrauenswürdigen Domänen.



| Funktion                                                                                                                                                    | BESCHREIBUNG                                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [**Lsacreatetrusteddomainex**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsacreatetrusteddomainex)<br/>                                                                                     | Erstellt ein neues [**treuhänddomain**](trusteddomain-object.md) -Objekt.<br/>            |
| [**Lsadeletetreuddomain**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsadeletetrusteddomain)<br/>                                                                                         | Entfernt ein [**Treuhänder-Domänen**](trusteddomain-object.md) Objekt.<br/>                |
| [**Lsaenumeratetrusteddomains**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumeratetrusteddomains)<br/> [**Lsaenumeratetrusteddomainsex**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumeratetrusteddomainsex)<br/> | Listet die Domänen auf, die derzeit vom lokalen System als vertrauenswürdig eingestuft werden.<br/>                  |
| [**Lsaopentrusteddomainbyname**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaopentrusteddomainbyname)<br/>                                                                                 | Öffnet ein Handle für ein " [**Treuhänder Domain**](trusteddomain-object.md) "-Objekt.<br/>      |
| [**Lsaquerytreuhänddomaininfo**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaquerytrusteddomaininfo)<br/>                                                                                   | Ruft Informationen zu einer vertrauenswürdigen Domäne ab. Die Domäne wird durch sid angegeben.<br/>  |
| [**LsaQueryTrustedDomainInfoByName**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaquerytrusteddomaininfobyname)<br/>                                                                       | Ruft Informationen zu einer vertrauenswürdigen Domäne ab. Die Domäne wird anhand des Namens angegeben.<br/> |
| [**Lsasettrusteddomaininfobyname**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsasettrusteddomaininfobyname)<br/>                                                                           | Legt Informationen für eine vertrauenswürdige Domäne fest. Die Domäne wird anhand des Namens angegeben.<br/>        |
| [**Lsasettrusteddomaininformation**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsasettrusteddomaininformation)<br/>                                                                         | Legt Informationen für eine vertrauenswürdige Domäne fest. Die Domäne wird durch sid angegeben.<br/>         |



 

### <a name="private-data-functions"></a>Private Datenfunktionen

Verwenden Sie keine privaten LSA-Datenfunktionen. Verwenden Sie stattdessen die Funktionen " [**CryptProtectData**](/windows/desktop/api/dpapi/nf-dpapi-cryptprotectdata) " und " [**CryptUnprotectData**](/windows/desktop/api/dpapi/nf-dpapi-cryptunprotectdata) ".



| Funktion                                                            | BESCHREIBUNG                                 |
|---------------------------------------------------------------------|---------------------------------------------|
| [**Lsarelteveprivatedata**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaretrieveprivatedata)<br/> | Ruft eine Zeichenfolge ab und entschlüsselt sie.<br/> |
| [**Lsastoreprivatedata**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsastoreprivatedata)<br/>       | Verschlüsselt und speichert eine Zeichenfolge.<br/>    |



 

### <a name="miscellaneous-functions"></a>Sonstige Funktionen

Die LSA-Richtlinien-API verfügt über die folgenden drei Funktionen, die in keine der anderen Kategorien der LSA-Richtlinien Funktionen passen.



| Funktion                                                          | BESCHREIBUNG                                                                                                                       |
|-------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [**Lsaclose**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaclose)<br/>                           | Schließt ein Handle für ein [**Richtlinien**](policy-object.md) Objekt oder ein " [**Treuhänder-Domain**](trusteddomain-object.md) "-Objekt.<br/> |
| [**Lsafreememory**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsafreememory)<br/>                 | Gibt einen von einer LSA-Funktion zugewiesenen Puffer frei.<br/>                                                                           |
| [**Lsantstatustowinerror**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsantstatustowinerror)<br/> | Konvertiert einen **NTSTATUS** -Wert in einen Windows-Fehlercode.<br/>                                                                |



 

## <a name="managed-service-account-functions"></a>Verwaltete Dienst Kontofunktionen

Die folgenden Funktionen werden verwendet, um verwaltete Dienst Konten zu erstellen, aufzulisten, zu suchen und zu löschen.



| Funktion                                                                      | BESCHREIBUNG                                                                                                                 |
|-------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| [**NetAddServiceAccount**](/windows/desktop/api/Lmaccess/nf-lmaccess-netaddserviceaccount)<br/>               | Erstellt ein verwaltetes Dienst Konto.<br/>                                                                               |
| [**NetEnumerateServiceAccounts**](/windows/desktop/api/Lmaccess/nf-lmaccess-netenumerateserviceaccounts)<br/> | Listet die Server Konten auf dem angegebenen Server auf.<br/>                                                          |
| [**NetIsServiceAccount**](/windows/desktop/api/Lmaccess/nf-lmaccess-netisserviceaccount)<br/>                 | Testet, ob das angegebene Dienst Konto im Netlogon-Speicher auf dem angegebenen Server vorhanden ist.<br/>                |
| [**NetRemoveServiceAccount**](/windows/desktop/api/Lmaccess/nf-lmaccess-netremoveserviceaccount)<br/>         | Löscht das angegebene Dienst Konto aus der [Active Directory](/windows/desktop/AD/active-directory-domain-services) -Datenbank.<br/> |



 

## <a name="password-filter-functions"></a>Kenn Wort Filter Funktionen

Die folgenden Kenn [*Wortfilter*](/windows/desktop/SecGloss/p-gly) Funktionen werden von benutzerdefinierten Kenn Wortfilter-DLLs implementiert, um die Kenn Wort Filterung und Kenn Wort Änderungs Benachrichtigung bereitzustellen



| Funktion                                                            | BESCHREIBUNG                                                     |
|---------------------------------------------------------------------|-----------------------------------------------------------------|
| [**Initializechangenotify**](/windows/desktop/api/Ntsecapi/nc-ntsecapi-psam_init_notification_routine)<br/> | Gibt an, dass eine Kenn Wortfilter-DLL initialisiert wird.<br/> |
| [**Passwordchangenotify**](/windows/desktop/api/Ntsecapi/nc-ntsecapi-psam_password_notification_routine)<br/>     | Gibt an, dass ein Kennwort geändert wurde.<br/>          |
| [**Passwordfilter**](/windows/desktop/api/Ntsecapi/nc-ntsecapi-psam_password_filter_routine)<br/>                 | Überprüft ein neues Kennwort auf der Grundlage von Kenn Wort Richtlinien.<br/>   |



 

## <a name="safer-functions"></a>Sicherere Funktionen

Die folgenden sichereren Funktionen können verwendet werden, um die sicherere Ebene einer ausführbaren Datei zu überprüfen und Ereignisse zu protokollieren.



| Funktion                                                         | BESCHREIBUNG                                                                                                                                                                          |
|------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Safercloselevel**](/windows/desktop/api/WinSafer/nf-winsafer-safercloselevel)                       | Schließt ein sicheres \_ Stufen \_ handle, das mit der [**SaferIdentifyLevel**](/windows/desktop/api/WinSafer/nf-winsafer-saferidentifylevel) -Funktion oder der [**saferkreatelevel**](/windows/desktop/api/WinSafer/nf-winsafer-safercreatelevel) -Funktion geöffnet wurde.<br/> |
| [**Safercompute"fromlevel"**](/windows/desktop/api/WinSafer/nf-winsafer-safercomputetokenfromlevel) | Schränkt ein Token mithilfe von Einschränkungen ein, die von einem Handle der sichereren Ebene angegeben werden \_ \_ .<br/>                                                                                                 |
| [**Saferkreatelevel**](/windows/desktop/api/WinSafer/nf-winsafer-safercreatelevel)                     | Öffnet ein Handle für die sicherere \_ Ebene \_ .<br/>                                                                                                                                             |
| [**Safergetlevelinformation**](/windows/desktop/api/WinSafer/nf-winsafer-safergetlevelinformation)     | Ruft Informationen zu einer Richtlinien Ebene ab.<br/>                                                                                                                               |
| [**Safergetpolicyinformation**](/windows/desktop/api/WinSafer/nf-winsafer-safergetpolicyinformation)   | Ruft Informationen zu einer Richtlinie ab.<br/>                                                                                                                                     |
| [**SaferIdentifyLevel**](/windows/desktop/api/WinSafer/nf-winsafer-saferidentifylevel)                 | Ruft Informationen zu einer Ebene ab.<br/>                                                                                                                                      |
| [**Saferiisexecutablefiletype**](/windows/desktop/api/WinSafer/nf-winsafer-saferiisexecutablefiletype) | Bestimmt, ob eine angegebene Datei eine ausführbare Datei ist.<br/>                                                                                                                |
| [**Saferrecorabventlogentry**](/windows/desktop/api/WinSafer/nf-winsafer-saferrecordeventlogentry)     | Sendet eine Meldung an das Ereignisprotokoll.<br/>                                                                                                                                         |
| [**Safersetlevelinformation**](/windows/desktop/api/WinSafer/nf-winsafer-safersetlevelinformation)     | Legt die Informationen zu einer Richtlinien Ebene fest.<br/>                                                                                                                                |
| [**Safersetpolicyinformation**](/windows/desktop/api/WinSafer/nf-winsafer-safergetlevelinformation)    | Legt die globalen Richtlinien Steuerelemente fest.<br/>                                                                                                                                          |



 

 

