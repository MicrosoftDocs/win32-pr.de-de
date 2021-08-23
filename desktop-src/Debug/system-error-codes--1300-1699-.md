---
description: Beschreibt die Fehlercodes 1300-1699, die in der WinError.h-Headerdatei definiert sind und für Entwickler vorgesehen sind.
ms.assetid: 7b04a2ba-7bf9-4bff-93c8-cbb0060e069d
title: Systemfehlercodes (1300-1699) (WinError.h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: 7aeb1c3642331db8ed3215d55a6d77e1e7b2a98c3859a5eb64a1d5b60350d24a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119310920"
---
# <a name="system-error-codes-1300-1699"></a>Systemfehlercodes (1300-1699)

> [!NOTE]
> Diese Informationen sind für Entwickler gedacht, die Systemfehler debuggen. Für andere Fehler, z. B. Probleme mit Windows Update, finden Sie eine Liste der Ressourcen auf der [Seite Fehlercodes.](system-error-codes.md)

In der folgenden Liste werden [die Systemfehlercodes für](system-error-codes.md) die Fehler 1300 bis 1699 beschrieben. Sie werden von der [**GetLastError-Funktion zurückgegeben,**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) wenn viele Funktionen fehlschlagen. Verwenden Sie zum Abrufen des Beschreibungstexts für den Fehler in Ihrer Anwendung die [**Funktion FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) mit dem **Flag FORMAT MESSAGE FROM \_ \_ \_ SYSTEM.**

<dl> <dt>

<span id="ERROR_NOT_ALL_ASSIGNED"></span><span id="error_not_all_assigned"></span>**FEHLER \_ NICHT \_ ALLE \_ ZUGEWIESEN**
</dt> <dd> <dl> <dt>

1300 (0x514)
</dt> <dt>



Nicht alle Berechtigungen oder Gruppen, auf die verwiesen wird, werden dem Aufrufer zugewiesen.


</dt> </dl> </dd> <dt>

<span id="ERROR_SOME_NOT_MAPPED"></span><span id="error_some_not_mapped"></span>**FEHLER \_ EINIGE \_ NICHT \_ ZUGEORDNET**
</dt> <dd> <dl> <dt>

1301 (0x515)
</dt> <dt>



Einige Zuordnungen zwischen Kontonamen und Sicherheits-IDs wurden nicht durchgeführt.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_QUOTAS_FOR_ACCOUNT"></span><span id="error_no_quotas_for_account"></span>**FEHLER: \_ \_ KEINE \_ KONTINGENTE FÜR \_ KONTO**
</dt> <dd> <dl> <dt>

1302 (0x516)
</dt> <dt>



Für dieses Konto sind keine Systemkontingentgrenzen festgelegt.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOCAL_USER_SESSION_KEY"></span><span id="error_local_user_session_key"></span>**FEHLER: \_ LOKALER \_ \_ \_ BENUTZERSITZUNGSSCHLÜSSEL**
</dt> <dd> <dl> <dt>

1303 (0x517)
</dt> <dt>



Es ist kein Verschlüsselungsschlüssel verfügbar. Ein bekannter Verschlüsselungsschlüssel wurde zurückgegeben.


</dt> </dl> </dd> <dt>

<span id="ERROR_NULL_LM_PASSWORD"></span><span id="error_null_lm_password"></span>**FEHLER \_ NULL \_ LM \_ PASSWORD**
</dt> <dd> <dl> <dt>

1304 (0x518)
</dt> <dt>



Das Kennwort ist zu komplex, um in ein LAN-Manager-Kennwort konvertiert zu werden. Das zurückgegebene LAN-Manager-Kennwort ist eine **NULL-Zeichenfolge.**


</dt> </dl> </dd> <dt>

<span id="ERROR_UNKNOWN_REVISION"></span><span id="error_unknown_revision"></span>**FEHLER \_ UNBEKANNTE \_ REVISION**
</dt> <dd> <dl> <dt>

1305 (0x519)
</dt> <dt>



Die Revisionsebene ist unbekannt.


</dt> </dl> </dd> <dt>

<span id="ERROR_REVISION_MISMATCH"></span><span id="error_revision_mismatch"></span>**\_FEHLERREVISIONSKONFLIKT \_**
</dt> <dd> <dl> <dt>

1306 (0x51A)
</dt> <dt>



Gibt an, dass zwei Revisionsebenen nicht kompatibel sind.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_OWNER"></span><span id="error_invalid_owner"></span>**FEHLER: \_ UNGÜLTIGER \_ BESITZER**
</dt> <dd> <dl> <dt>

1307 (0x51B)
</dt> <dt>



Diese Sicherheits-ID wird möglicherweise nicht als Besitzer dieses Objekts zugewiesen.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PRIMARY_GROUP"></span><span id="error_invalid_primary_group"></span>**FEHLER: \_ \_ UNGÜLTIGE PRIMÄRE \_ GRUPPE**
</dt> <dd> <dl> <dt>

1308 (0x51C)
</dt> <dt>



Diese Sicherheits-ID wird möglicherweise nicht als primäre Gruppe eines Objekts zugewiesen.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_IMPERSONATION_TOKEN"></span><span id="error_no_impersonation_token"></span>**FEHLER: \_ \_ KEIN IDENTITÄTSWECHSELTOKEN \_**
</dt> <dd> <dl> <dt>

1309 (0x51D)
</dt> <dt>



Es wurde versucht, ein Identitätswechseltoken von einem Thread zu verwenden, der derzeit nicht die Identität eines Clients antänd.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_DISABLE_MANDATORY"></span><span id="error_cant_disable_mandatory"></span>**ERROR \_ CANT \_ DISABLE \_ MANDATORY**
</dt> <dd> <dl> <dt>

1310 (0x51E)
</dt> <dt>



Die Gruppe ist möglicherweise nicht deaktiviert.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_LOGON_SERVERS"></span><span id="error_no_logon_servers"></span>**FEHLER: \_ \_ KEINE \_ ANMELDESERVER**
</dt> <dd> <dl> <dt>

1311 (0x51F)
</dt> <dt>



Derzeit sind keine Anmeldeserver verfügbar, um die Anmeldeanforderung zu verwalten.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SUCH_LOGON_SESSION"></span><span id="error_no_such_logon_session"></span>**FEHLER: \_ \_ KEINE SOLCHE \_ \_ ANMELDESITZUNG**
</dt> <dd> <dl> <dt>

1312 (0x520)
</dt> <dt>



Eine angegebene Anmeldesitzung ist nicht vorhanden. Es wurde möglicherweise bereits beendet.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SUCH_PRIVILEGE"></span><span id="error_no_such_privilege"></span>**FEHLER: \_ KEINE \_ SOLCHE \_ BERECHTIGUNG**
</dt> <dd> <dl> <dt>

1313 (0x521)
</dt> <dt>



Eine angegebene Berechtigung ist nicht vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRIVILEGE_NOT_HELD"></span><span id="error_privilege_not_held"></span>**FEHLERBERECHTIGUNG \_ \_ NICHT \_ GEHALTEN**
</dt> <dd> <dl> <dt>

1314 (0x522)
</dt> <dt>



Dem Client fehlt ein erforderliches Privileg.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_ACCOUNT_NAME"></span><span id="error_invalid_account_name"></span>**FEHLER: \_ \_ UNGÜLTIGER \_ KONTONAME**
</dt> <dd> <dl> <dt>

1315 (0x523)
</dt> <dt>



Der bereitgestellte Name ist kein ordnungsgemäßer Kontoname.


</dt> </dl> </dd> <dt>

<span id="ERROR_USER_EXISTS"></span><span id="error_user_exists"></span>**FEHLER: \_ DER BENUTZER \_ IST VORHANDEN**
</dt> <dd> <dl> <dt>

1316 (0x524)
</dt> <dt>



Das angegebene Konto ist bereits vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SUCH_USER"></span><span id="error_no_such_user"></span>**FEHLER: \_ \_ KEIN SOLCHER \_ BENUTZER**
</dt> <dd> <dl> <dt>

1317 (0x525)
</dt> <dt>



Das angegebene Konto ist nicht vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_GROUP_EXISTS"></span><span id="error_group_exists"></span>**FEHLERGRUPPE \_ \_ VORHANDEN**
</dt> <dd> <dl> <dt>

1318 (0x526)
</dt> <dt>



Die angegebene Gruppe ist bereits vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SUCH_GROUP"></span><span id="error_no_such_group"></span>**FEHLER \_ KEINE \_ SOLCHE \_ GRUPPE**
</dt> <dd> <dl> <dt>

1319 (0x527)
</dt> <dt>



Die angegebene Gruppe ist nicht vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_MEMBER_IN_GROUP"></span><span id="error_member_in_group"></span>**ERROR \_ MEMBER \_ IN \_ GROUP**
</dt> <dd> <dl> <dt>

1320 (0x528)
</dt> <dt>



Entweder ist das angegebene Benutzerkonto bereits Mitglied der angegebenen Gruppe, oder die angegebene Gruppe kann nicht gelöscht werden, da sie ein Mitglied enthält.


</dt> </dl> </dd> <dt>

<span id="ERROR_MEMBER_NOT_IN_GROUP"></span><span id="error_member_not_in_group"></span>**FEHLERMITGLIED \_ \_ NICHT IN \_ \_ GRUPPE**
</dt> <dd> <dl> <dt>

1321 (0x529)
</dt> <dt>



Das angegebene Benutzerkonto ist kein Mitglied des angegebenen Gruppenkontos.


</dt> </dl> </dd> <dt>

<span id="ERROR_LAST_ADMIN"></span><span id="error_last_admin"></span>**FEHLER \_ LETZTER \_ ADMINISTRATOR**
</dt> <dd> <dl> <dt>

1322 (0x52A)
</dt> <dt>



Dieser Vorgang ist nicht möglich, da er dazu führen kann, dass ein Verwaltungskonto deaktiviert oder gelöscht wird oder sich nicht anmelden kann.


</dt> </dl> </dd> <dt>

<span id="ERROR_WRONG_PASSWORD"></span><span id="error_wrong_password"></span>**FEHLER: \_ \_ FALSCHES KENNWORT**
</dt> <dd> <dl> <dt>

1323 (0x52B)
</dt> <dt>



Das Kennwort kann nicht aktualisiert werden. Der als aktuelles Kennwort bereitgestellte Wert ist falsch.


</dt> </dl> </dd> <dt>

<span id="ERROR_ILL_FORMED_PASSWORD"></span><span id="error_ill_formed_password"></span>**FEHLER: \_ NICHT \_ GEBILDETES \_ KENNWORT**
</dt> <dd> <dl> <dt>

1324 (0x52C)
</dt> <dt>



Das Kennwort kann nicht aktualisiert werden. Der für das neue Kennwort bereitgestellte Wert enthält Werte, die in Kennwörtern nicht zulässig sind.


</dt> </dl> </dd> <dt>

<span id="ERROR_PASSWORD_RESTRICTION"></span><span id="error_password_restriction"></span>**FEHLER: \_ \_ KENNWORTEINSCHRÄNKUNG**
</dt> <dd> <dl> <dt>

1325 (0x52D)
</dt> <dt>



Das Kennwort kann nicht aktualisiert werden. Der für das neue Kennwort bereitgestellte Wert erfüllt nicht die Längen-, Komplexitäts- oder Verlaufsanforderungen der Domäne.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOGON_FAILURE"></span><span id="error_logon_failure"></span>**FEHLER \_ BEI DER \_ ANMELDUNG**
</dt> <dd> <dl> <dt>

1326 (0x52E)
</dt> <dt>



Der Benutzername oder das Kennwort ist falsch.


</dt> </dl> </dd> <dt>

<span id="ERROR_ACCOUNT_RESTRICTION"></span><span id="error_account_restriction"></span>**\_ \_ FEHLERKONTOEINSCHRÄNKUNG**
</dt> <dd> <dl> <dt>

1327 (0x52F)
</dt> <dt>



Kontoeinschränkungen verhindern, dass sich dieser Benutzer anmelden kann. Beispiel: Leere Kennwörter sind nicht zulässig, die Anmeldezeiten sind begrenzt, oder es wurde eine Richtlinieneinschränkung erzwungen.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_LOGON_HOURS"></span><span id="error_invalid_logon_hours"></span>**FEHLER \_ \_ UNGÜLTIGE \_ ANMELDESTUNDEN**
</dt> <dd> <dl> <dt>

1328 (0x530)
</dt> <dt>



Für Ihr Konto gelten Zeiteinschränkungen, mit denen Sie sich derzeit nicht anmelden können.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_WORKSTATION"></span><span id="error_invalid_workstation"></span>**FEHLER: \_ UNGÜLTIGE \_ ARBEITSSTATION**
</dt> <dd> <dl> <dt>

1329 (0x531)
</dt> <dt>



Dieser Benutzer darf sich nicht bei diesem Computer anmelden.


</dt> </dl> </dd> <dt>

<span id="ERROR_PASSWORD_EXPIRED"></span><span id="error_password_expired"></span>**\_FEHLERKENNWORT \_ ABGELAUFEN**
</dt> <dd> <dl> <dt>

1330 (0x532)
</dt> <dt>



Das Kennwort für dieses Konto ist abgelaufen.


</dt> </dl> </dd> <dt>

<span id="ERROR_ACCOUNT_DISABLED"></span><span id="error_account_disabled"></span>**FEHLERKONTO \_ \_ DEAKTIVIERT**
</dt> <dd> <dl> <dt>

1331 (0x533)
</dt> <dt>



Dieser Benutzer kann sich nicht anmelden, da dieses Konto derzeit deaktiviert ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_NONE_MAPPED"></span><span id="error_none_mapped"></span>**FEHLER: \_ KEINE \_ ZUORDNUNG**
</dt> <dd> <dl> <dt>

1332 (0x534)
</dt> <dt>



Es wurde keine Zuordnung zwischen Kontonamen und Sicherheits-IDs vorgenommen.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_LUIDS_REQUESTED"></span><span id="error_too_many_luids_requested"></span>**FEHLER: \_ ZU \_ VIELE \_ LUIDS \_ ANGEFORDERT**
</dt> <dd> <dl> <dt>

1333 (0x535)
</dt> <dt>



Zu viele lokale Benutzerbezeichner (LUIDs) wurden gleichzeitig angefordert.


</dt> </dl> </dd> <dt>

<span id="ERROR_LUIDS_EXHAUSTED"></span><span id="error_luids_exhausted"></span>**\_FEHLER-LUIDS \_ ERSCHÖPFT**
</dt> <dd> <dl> <dt>

1334 (0x536)
</dt> <dt>



Es sind keine lokalen Benutzerbezeichner (LUIDs) mehr verfügbar.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SUB_AUTHORITY"></span><span id="error_invalid_sub_authority"></span>**FEHLER: \_ UNGÜLTIGE \_ UNTERGEORDNETE \_ AUTORITÄT**
</dt> <dd> <dl> <dt>

1335 (0x537)
</dt> <dt>



Der Teil der Unterautorität einer Sicherheits-ID ist für diese spezielle Verwendung ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_ACL"></span><span id="error_invalid_acl"></span>**FEHLER: \_ UNGÜLTIGE \_ ACL**
</dt> <dd> <dl> <dt>

1336 (0x538)
</dt> <dt>



Die Struktur der Zugriffssteuerungsliste (Access Control List, ACL) ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SID"></span><span id="error_invalid_sid"></span>**FEHLER: \_ UNGÜLTIGE \_ SID**
</dt> <dd> <dl> <dt>

1337 (0x539)
</dt> <dt>



Die Sicherheits-ID-Struktur ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SECURITY_DESCR"></span><span id="error_invalid_security_descr"></span>**FEHLER: \_ UNGÜLTIGER \_ \_ SICHERHEITS-DESCR**
</dt> <dd> <dl> <dt>

1338 (0x53A)
</dt> <dt>



Die Sicherheitsbeschreibungsstruktur ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_INHERITANCE_ACL"></span><span id="error_bad_inheritance_acl"></span>**FEHLER: \_ UNGÜLTIGE \_ VERERBUNGS-ACL \_**
</dt> <dd> <dl> <dt>

1340 (0x53C)
</dt> <dt>



Die geerbte Zugriffssteuerungsliste (Access Control List, ACL) oder der Zugriffssteuerungseintrag (ACE) konnte nicht erstellt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVER_DISABLED"></span><span id="error_server_disabled"></span>**FEHLERSERVER \_ \_ DEAKTIVIERT**
</dt> <dd> <dl> <dt>

1341 (0x53D)
</dt> <dt>



Der Server ist derzeit deaktiviert.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVER_NOT_DISABLED"></span><span id="error_server_not_disabled"></span>**FEHLERSERVER \_ \_ NICHT \_ DEAKTIVIERT**
</dt> <dd> <dl> <dt>

1342 (0x53E)
</dt> <dt>



Der Server ist derzeit aktiviert.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_ID_AUTHORITY"></span><span id="error_invalid_id_authority"></span>**FEHLER: \_ \_ UNGÜLTIGE \_ ID-AUTORITÄT**
</dt> <dd> <dl> <dt>

1343 (0x53F)
</dt> <dt>



Der angegebene Wert war ein ungültiger Wert für eine Bezeichnerautorität.


</dt> </dl> </dd> <dt>

<span id="ERROR_ALLOTTED_SPACE_EXCEEDED"></span><span id="error_allotted_space_exceeded"></span>**FEHLER \_ ZUGEWIESENER \_ SPEICHERPLATZ \_ ÜBERSCHRITTEN**
</dt> <dd> <dl> <dt>

1344 (0x540)
</dt> <dt>



Für Sicherheitsupdates ist kein Arbeitsspeicher mehr verfügbar.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_GROUP_ATTRIBUTES"></span><span id="error_invalid_group_attributes"></span>**FEHLER: \_ UNGÜLTIGE \_ \_ GRUPPENATTRIBUTE**
</dt> <dd> <dl> <dt>

1345 (0x541)
</dt> <dt>



Die angegebenen Attribute sind ungültig oder nicht mit den Attributen für die gruppe als Ganzes kompatibel.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_IMPERSONATION_LEVEL"></span><span id="error_bad_impersonation_level"></span>**FEHLER BEI \_ UNGÜLTIGER \_ \_ IDENTITÄTSWECHSELEBENE**
</dt> <dd> <dl> <dt>

1346 (0x542)
</dt> <dt>



Entweder wurde eine geforderte Identitätswechselebene nicht geliefert, oder die gelieferte Identitätswechselebene ist unzulässig.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_OPEN_ANONYMOUS"></span><span id="error_cant_open_anonymous"></span>**FEHLER \_ CANT \_ OPEN \_ ANONYMOUS**
</dt> <dd> <dl> <dt>

1347 (0x543)
</dt> <dt>



Ein Sicherheitstoken auf anonymer Ebene kann nicht geöffnet werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_VALIDATION_CLASS"></span><span id="error_bad_validation_class"></span>**ERROR \_ BAD \_ VALIDATION \_ CLASS**
</dt> <dd> <dl> <dt>

1348 (0x544)
</dt> <dt>



Die angeforderte Validierungsinformationsklasse war ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_TOKEN_TYPE"></span><span id="error_bad_token_type"></span>**FEHLER: \_ UNGÜLTIGER \_ \_ TOKENTYP**
</dt> <dd> <dl> <dt>

1349 (0x545)
</dt> <dt>



Der Typ des Tokens ist für die versuchte Verwendung ungeeignet.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SECURITY_ON_OBJECT"></span><span id="error_no_security_on_object"></span>**FEHLER \_ KEINE SICHERHEIT FÜR \_ \_ \_ OBJEKT**
</dt> <dd> <dl> <dt>

1350 (0x546)
</dt> <dt>



Für ein Objekt ohne zugeordnete Sicherheit kann kein Sicherheitsvorgang ausgeführt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_ACCESS_DOMAIN_INFO"></span><span id="error_cant_access_domain_info"></span>**FEHLER: \_ KANN NICHT AUF \_ \_ \_ DOMÄNENINFORMATIONEN ZUGREIFEN**
</dt> <dd> <dl> <dt>

1351 (0x547)
</dt> <dt>



Konfigurationsinformationen konnten nicht vom Domänencontroller gelesen werden, weil der Computer nicht verfügbar ist oder der Zugriff verweigert wurde.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SERVER_STATE"></span><span id="error_invalid_server_state"></span>**FEHLER: \_ UNGÜLTIGER \_ \_ SERVERSTATUS**
</dt> <dd> <dl> <dt>

1352 (0x548)
</dt> <dt>



Der Server des Sicherheitskonto-Managers (SAM) oder der lokalen Sicherheitsautorität (LSA) befand sich im falschen Zustand, um den Sicherheitsvorgang auszuführen.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_DOMAIN_STATE"></span><span id="error_invalid_domain_state"></span>**FEHLER: \_ UNGÜLTIGER \_ \_ DOMÄNENSTATUS**
</dt> <dd> <dl> <dt>

1353 (0x549)
</dt> <dt>



Die Domäne befand sich im falschen Zustand, um den Sicherheitsvorgang auszuführen.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_DOMAIN_ROLE"></span><span id="error_invalid_domain_role"></span>**FEHLER: \_ UNGÜLTIGE \_ \_ DOMÄNENROLLE**
</dt> <dd> <dl> <dt>

1354 (0x54A)
</dt> <dt>



Dieser Vorgang ist nur für den primären Domänencontroller der Domäne zulässig.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SUCH_DOMAIN"></span><span id="error_no_such_domain"></span>**FEHLER: \_ KEINE \_ SOLCHE \_ DOMÄNE**
</dt> <dd> <dl> <dt>

1355 (0x54B)
</dt> <dt>



Die angegebene Domäne ist entweder nicht vorhanden oder konnte nicht kontaktiert werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DOMAIN_EXISTS"></span><span id="error_domain_exists"></span>**FEHLERDOMÄNE \_ \_ VORHANDEN**
</dt> <dd> <dl> <dt>

1356 (0x54C)
</dt> <dt>



Die angegebene Domäne ist bereits vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DOMAIN_LIMIT_EXCEEDED"></span><span id="error_domain_limit_exceeded"></span>**\_ \_ FEHLERDOMÄNENLIMIT \_ ÜBERSCHRITTEN**
</dt> <dd> <dl> <dt>

1357 (0x54D)
</dt> <dt>



Es wurde versucht, den Grenzwert für die Anzahl der Domänen pro Server zu überschreiten.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNAL_DB_CORRUPTION"></span><span id="error_internal_db_corruption"></span>**FEHLER: \_ INTERNE \_ \_ DATENBANKBESCHÄDIGUNG**
</dt> <dd> <dl> <dt>

1358 (0x54E)
</dt> <dt>



Der angeforderte Vorgang kann aufgrund eines schwerwiegenden Medienfehlers oder einer Datenstrukturbeschädigung auf dem Datenträger nicht abgeschlossen werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNAL_ERROR"></span><span id="error_internal_error"></span>**\_INTERNER \_ FEHLER**
</dt> <dd> <dl> <dt>

1359 (0x54F)
</dt> <dt>



Interner Fehler.


</dt> </dl> </dd> <dt>

<span id="ERROR_GENERIC_NOT_MAPPED"></span><span id="error_generic_not_mapped"></span>**FEHLER \_ GENERISCH \_ NICHT \_ ZUGEORDNET**
</dt> <dd> <dl> <dt>

1360 (0x550)
</dt> <dt>



Generische Zugriffstypen waren in einer Zugriffsmaske enthalten, die bereits nicht generischen Typen zugeordnet werden sollte.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_DESCRIPTOR_FORMAT"></span><span id="error_bad_descriptor_format"></span>**FEHLER: \_ UNGÜLTIGES \_ DESKRIPTORFORMAT \_**
</dt> <dd> <dl> <dt>

1361 (0x551)
</dt> <dt>



Eine Sicherheitsbeschreibung hat nicht das richtige Format (absolut oder selbst relativ).


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_LOGON_PROCESS"></span><span id="error_not_logon_process"></span>**FEHLER \_ BEIM \_ \_ ANMELDEVORGANG**
</dt> <dd> <dl> <dt>

1362 (0x552)
</dt> <dt>



Die angeforderte Aktion ist nur für die Verwendung durch Anmeldeprozesse eingeschränkt. Der aufrufende Prozess wurde nicht als Anmeldevorgang registriert.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOGON_SESSION_EXISTS"></span><span id="error_logon_session_exists"></span>**FEHLER \_ BEI \_ ANMELDESITZUNG \_ VORHANDEN**
</dt> <dd> <dl> <dt>

1363 (0x553)
</dt> <dt>



Eine neue Anmeldesitzung kann nicht mit einer ID gestartet werden, die bereits verwendet wird.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SUCH_PACKAGE"></span><span id="error_no_such_package"></span>**FEHLER: \_ KEIN \_ SOLCHES \_ PAKET**
</dt> <dd> <dl> <dt>

1364 (0x554)
</dt> <dt>



Ein angegebenes Authentifizierungspaket ist unbekannt.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_LOGON_SESSION_STATE"></span><span id="error_bad_logon_session_state"></span>**FEHLER: \_ FEHLERHAFTER \_ \_ ANMELDESITZUNGSSTATUS \_**
</dt> <dd> <dl> <dt>

1365 (0x555)
</dt> <dt>



Die Anmeldesitzung befindet sich nicht in einem Zustand, der mit dem angeforderten Vorgang konsistent ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOGON_SESSION_COLLISION"></span><span id="error_logon_session_collision"></span>**FEHLER: \_ \_ \_ SITZUNGSKONFLIKT BEI DER ANMELDUNG**
</dt> <dd> <dl> <dt>

1366 (0x556)
</dt> <dt>



Die Anmeldesitzungs-ID wird bereits verwendet.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_LOGON_TYPE"></span><span id="error_invalid_logon_type"></span>**FEHLER: \_ UNGÜLTIGER \_ \_ ANMELDETYP**
</dt> <dd> <dl> <dt>

1367 (0x557)
</dt> <dt>



Eine Anmeldeanforderung enthielt einen ungültigen Anmeldetypwert.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_IMPERSONATE"></span><span id="error_cannot_impersonate"></span>**FEHLER \_ KANN KEINE IDENTITÄT \_ ANNEHMEN**
</dt> <dd> <dl> <dt>

1368 (0x558)
</dt> <dt>



Die Identität kann nicht mithilfe einer Named Pipe angenommen werden, bis Daten aus dieser Pipe gelesen wurden.


</dt> </dl> </dd> <dt>

<span id="ERROR_RXACT_INVALID_STATE"></span><span id="error_rxact_invalid_state"></span>**ERROR \_ RXACT \_ INVALID \_ STATE**
</dt> <dd> <dl> <dt>

1369 (0x559)
</dt> <dt>



Der Transaktionsstatus einer Registrierungsunterstruktur ist mit dem angeforderten Vorgang nicht kompatibel.


</dt> </dl> </dd> <dt>

<span id="ERROR_RXACT_COMMIT_FAILURE"></span><span id="error_rxact_commit_failure"></span>**FEHLER \_ \_ RXACT-COMMITFEHLER \_**
</dt> <dd> <dl> <dt>

1370 (0x55A)
</dt> <dt>



Es wurde eine interne Sicherheitsdatenbankbeschädigung festgestellt.


</dt> </dl> </dd> <dt>

<span id="ERROR_SPECIAL_ACCOUNT"></span><span id="error_special_account"></span>**ERROR \_ SPECIAL \_ ACCOUNT**
</dt> <dd> <dl> <dt>

1371 (0x55B)
</dt> <dt>



Dieser Vorgang kann nicht für integrierte Konten ausgeführt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_SPECIAL_GROUP"></span><span id="error_special_group"></span>**ERROR \_ SPECIAL \_ GROUP**
</dt> <dd> <dl> <dt>

1372 (0x55C)
</dt> <dt>



Dieser Vorgang kann für diese integrierte spezielle Gruppe nicht ausgeführt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_SPECIAL_USER"></span><span id="error_special_user"></span>**ERROR \_ SPECIAL \_ USER**
</dt> <dd> <dl> <dt>

1373 (0x55D)
</dt> <dt>



Dieser Vorgang kann für diesen integrierten speziellen Benutzer nicht ausgeführt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_MEMBERS_PRIMARY_GROUP"></span><span id="error_members_primary_group"></span>**PRIMÄRE GRUPPE "FEHLERMITGLIEDER" \_ \_ \_**
</dt> <dd> <dl> <dt>

1374 (0x55E)
</dt> <dt>



Der Benutzer kann nicht aus einer Gruppe entfernt werden, da die Gruppe derzeit die primäre Gruppe des Benutzers ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOKEN_ALREADY_IN_USE"></span><span id="error_token_already_in_use"></span>**\_BEREITS \_ \_ VERWENDETES FEHLERTOKEN \_**
</dt> <dd> <dl> <dt>

1375 (0x55F)
</dt> <dt>



Das Token wird bereits als primäres Token verwendet.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SUCH_ALIAS"></span><span id="error_no_such_alias"></span>**FEHLER: \_ KEIN \_ SOLCHER \_ ALIAS**
</dt> <dd> <dl> <dt>

1376 (0x560)
</dt> <dt>



Die angegebene lokale Gruppe ist nicht vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_MEMBER_NOT_IN_ALIAS"></span><span id="error_member_not_in_alias"></span>**FEHLERMEMBER \_ \_ NICHT IM \_ \_ ALIAS**
</dt> <dd> <dl> <dt>

1377 (0x561)
</dt> <dt>



Der angegebene Kontoname ist kein Mitglied der Gruppe.


</dt> </dl> </dd> <dt>

<span id="ERROR_MEMBER_IN_ALIAS"></span><span id="error_member_in_alias"></span>**ERROR \_ MEMBER \_ IN \_ ALIAS**
</dt> <dd> <dl> <dt>

1378 (0x562)
</dt> <dt>



Der angegebene Kontoname ist bereits Mitglied der Gruppe.


</dt> </dl> </dd> <dt>

<span id="ERROR_ALIAS_EXISTS"></span><span id="error_alias_exists"></span>**\_ \_ FEHLERALIAS VORHANDEN**
</dt> <dd> <dl> <dt>

1379 (0x563)
</dt> <dt>



Die angegebene lokale Gruppe ist bereits vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOGON_NOT_GRANTED"></span><span id="error_logon_not_granted"></span>**\_FEHLERANMELDUNG \_ NICHT \_ GEWÄHRT**
</dt> <dd> <dl> <dt>

1380 (0x564)
</dt> <dt>



Anmeldefehler: Dem Benutzer wurde der angeforderte Anmeldetyp auf diesem Computer nicht gewährt.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_SECRETS"></span><span id="error_too_many_secrets"></span>**FEHLER \_ ZU \_ VIELE \_ GEHEIMNISSE**
</dt> <dd> <dl> <dt>

1381 (0x565)
</dt> <dt>



Die maximale Anzahl von Geheimnissen, die in einem einzelnen System gespeichert werden können, wurde überschritten.


</dt> </dl> </dd> <dt>

<span id="ERROR_SECRET_TOO_LONG"></span><span id="error_secret_too_long"></span>**FEHLERGEHEIMNIS \_ \_ ZU \_ LANG**
</dt> <dd> <dl> <dt>

1382 (0x566)
</dt> <dt>



Die Länge eines Geheimnisses überschreitet die maximal zulässige Länge.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNAL_DB_ERROR"></span><span id="error_internal_db_error"></span>**FEHLER \_ INTERNER \_ \_ DATENBANKFEHLER**
</dt> <dd> <dl> <dt>

1383 (0x567)
</dt> <dt>



Die Datenbank der lokalen Sicherheitsautorität enthält eine interne Inkonsistenz.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_CONTEXT_IDS"></span><span id="error_too_many_context_ids"></span>**FEHLER \_ ZU \_ VIELE \_ \_ KONTEXT-IDS**
</dt> <dd> <dl> <dt>

1384 (0x568)
</dt> <dt>



Während eines Anmeldeversuchs hat sich der Sicherheitskontext des Benutzers zu viele Sicherheits-IDs angesammelt.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOGON_TYPE_NOT_GRANTED"></span><span id="error_logon_type_not_granted"></span>**\_ \_ \_ FEHLERANMELDUNGSTYP NICHT \_ GEWÄHRT**
</dt> <dd> <dl> <dt>

1385 (0x569)
</dt> <dt>



Anmeldefehler: Dem Benutzer wurde der angeforderte Anmeldetyp auf diesem Computer nicht gewährt.


</dt> </dl> </dd> <dt>

<span id="ERROR_NT_CROSS_ENCRYPTION_REQUIRED"></span><span id="error_nt_cross_encryption_required"></span>**FEHLER \_ \_ NT-KREUZVERSCHLÜSSELUNG \_ \_ ERFORDERLICH**
</dt> <dd> <dl> <dt>

1386 (0x56A)
</dt> <dt>



Ein kreuzverschlüsseltes Kennwort ist erforderlich, um ein Benutzerkennwort zu ändern.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SUCH_MEMBER"></span><span id="error_no_such_member"></span>**ERROR \_ NO \_ SUCH \_ MEMBER**
</dt> <dd> <dl> <dt>

1387 (0x56B)
</dt> <dt>



Ein Mitglied konnte der lokalen Gruppe nicht hinzugefügt oder daraus entfernt werden, da das Element nicht vorhanden ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_MEMBER"></span><span id="error_invalid_member"></span>**ERROR \_ INVALID \_ MEMBER**
</dt> <dd> <dl> <dt>

1388 (0x56C)
</dt> <dt>



Ein neues Mitglied konnte keiner lokalen Gruppe hinzugefügt werden, da das Element den falschen Kontotyp auf hat.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_SIDS"></span><span id="error_too_many_sids"></span>**FEHLER \_ ZU \_ VIELE \_ SIDS**
</dt> <dd> <dl> <dt>

1389 (0x56D)
</dt> <dt>



Es wurden zu viele Sicherheits-IDs angegeben.


</dt> </dl> </dd> <dt>

<span id="ERROR_LM_CROSS_ENCRYPTION_REQUIRED"></span><span id="error_lm_cross_encryption_required"></span>**FEHLER \_ \_ LM-KREUZVERSCHLÜSSELUNG \_ \_ ERFORDERLICH**
</dt> <dd> <dl> <dt>

1390 (0x56E)
</dt> <dt>



Ein kreuzverschlüsseltes Kennwort ist erforderlich, um dieses Benutzerkennwort zu ändern.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_INHERITANCE"></span><span id="error_no_inheritance"></span>**FEHLER: \_ KEINE \_ VERERBUNG**
</dt> <dd> <dl> <dt>

1391 (0x56F)
</dt> <dt>



Gibt an, dass eine ACL keine vererbbaren Komponenten enthält.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_CORRUPT"></span><span id="error_file_corrupt"></span>**FEHLERDATEI \_ \_ BESCHÄDIGT**
</dt> <dd> <dl> <dt>

1392 (0x570)
</dt> <dt>



Die Datei oder das Verzeichnis ist beschädigt und nicht lesbar.


</dt> </dl> </dd> <dt>

<span id="ERROR_DISK_CORRUPT"></span><span id="error_disk_corrupt"></span>**FEHLER \_ DATENTRÄGER \_ BESCHÄDIGT**
</dt> <dd> <dl> <dt>

1393 (0x571)
</dt> <dt>



Die Datenträgerstruktur ist beschädigt und nicht lesbar.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_USER_SESSION_KEY"></span><span id="error_no_user_session_key"></span>**FEHLER: \_ KEIN \_ \_ \_ BENUTZERSITZUNGSSCHLÜSSEL**
</dt> <dd> <dl> <dt>

1394 (0x572)
</dt> <dt>



Für die angegebene Anmeldesitzung ist kein Benutzersitzungsschlüssel vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_LICENSE_QUOTA_EXCEEDED"></span><span id="error_license_quota_exceeded"></span>**\_ \_ FEHLERLIZENZKONTINGENT \_ ÜBERSCHRITTEN**
</dt> <dd> <dl> <dt>

1395 (0x573)
</dt> <dt>



Der Dienst, auf den zugegriffen wird, ist für eine bestimmte Anzahl von Verbindungen lizenziert. Zu diesem Zeitpunkt können keine weiteren Verbindungen mit dem Dienst hergestellt werden, da bereits so viele Verbindungen vorhanden sind, wie der Dienst akzeptieren kann.


</dt> </dl> </dd> <dt>

<span id="ERROR_WRONG_TARGET_NAME"></span><span id="error_wrong_target_name"></span>**FEHLER: \_ \_ FALSCHER \_ ZIELNAME**
</dt> <dd> <dl> <dt>

1396 (0x574)
</dt> <dt>



Der Name des Zielkontos ist falsch.


</dt> </dl> </dd> <dt>

<span id="ERROR_MUTUAL_AUTH_FAILED"></span><span id="error_mutual_auth_failed"></span>**FEHLER \_ FEHLER BEI DER GEGENSEITIGEN \_ AUTHENTIFIZIERUNG \_**
</dt> <dd> <dl> <dt>

1397 (0x575)
</dt> <dt>



Fehler bei der gegenseitigen Authentifizierung. Das Kennwort des Servers ist auf dem Domänencontroller veraltet.


</dt> </dl> </dd> <dt>

<span id="ERROR_TIME_SKEW"></span><span id="error_time_skew"></span>**\_ \_ FEHLERZEITABWEICHUNG**
</dt> <dd> <dl> <dt>

1398 (0x576)
</dt> <dt>



Es gibt einen Zeit- und/oder Datumsunterschied zwischen Client und Server.


</dt> </dl> </dd> <dt>

<span id="ERROR_CURRENT_DOMAIN_NOT_ALLOWED"></span><span id="error_current_domain_not_allowed"></span>**FEHLER \_ AKTUELLE DOMÄNE NICHT \_ \_ \_ ZULÄSSIG**
</dt> <dd> <dl> <dt>

1399 (0x577)
</dt> <dt>



Dieser Vorgang kann nicht für die aktuelle Domäne ausgeführt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_WINDOW_HANDLE"></span><span id="error_invalid_window_handle"></span>**FEHLER: \_ UNGÜLTIGES \_ \_ FENSTERHANDLE**
</dt> <dd> <dl> <dt>

1400 (0x578)
</dt> <dt>



Ungültiges Fensterhandle.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_MENU_HANDLE"></span><span id="error_invalid_menu_handle"></span>**FEHLER: \_ UNGÜLTIGES \_ \_ MENÜHANDLE**
</dt> <dd> <dl> <dt>

1401 (0x579)
</dt> <dt>



Ungültiges Menühandle.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_CURSOR_HANDLE"></span><span id="error_invalid_cursor_handle"></span>**FEHLER: \_ UNGÜLTIGES \_ \_ CURSORHANDLE**
</dt> <dd> <dl> <dt>

1402 (0x57A)
</dt> <dt>



Ungültiges Cursorhandle.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_ACCEL_HANDLE"></span><span id="error_invalid_accel_handle"></span>**FEHLER: \_ UNGÜLTIGES \_ \_ ACCEL-HANDLE**
</dt> <dd> <dl> <dt>

1403 (0x57B)
</dt> <dt>



Ungültiges Zugriffstasten-Tabellenhandle.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_HOOK_HANDLE"></span><span id="error_invalid_hook_handle"></span>**FEHLER: \_ UNGÜLTIGES \_ \_ HOOKHANDLE**
</dt> <dd> <dl> <dt>

1404 (0x57C)
</dt> <dt>



Ungültiges Hookhandle.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_DWP_HANDLE"></span><span id="error_invalid_dwp_handle"></span>**FEHLER: \_ UNGÜLTIGES \_ \_ DWP-HANDLE**
</dt> <dd> <dl> <dt>

1405 (0x57D)
</dt> <dt>



Ungültiges Handle für eine Positionsstruktur mit mehreren Fenstern.


</dt> </dl> </dd> <dt>

<span id="ERROR_TLW_WITH_WSCHILD"></span><span id="error_tlw_with_wschild"></span>**FEHLER \_ TLW \_ MIT \_ WSCHILD**
</dt> <dd> <dl> <dt>

1406 (0x57E)
</dt> <dt>



Ein untergeordnetes Fenster der obersten Ebene kann nicht erstellt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_FIND_WND_CLASS"></span><span id="error_cannot_find_wnd_class"></span>**\_FEHLER: \_ \_ WND-KLASSE NICHT GEFUNDEN \_**
</dt> <dd> <dl> <dt>

1407 (0x57F)
</dt> <dt>



Die Fensterklasse wurde nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINDOW_OF_OTHER_THREAD"></span><span id="error_window_of_other_thread"></span>**FEHLERFENSTER \_ \_ EINES ANDEREN \_ \_ THREADS**
</dt> <dd> <dl> <dt>

1408 (0x580)
</dt> <dt>



Ungültiges Fenster; sie gehört zu einem anderen Thread.


</dt> </dl> </dd> <dt>

<span id="ERROR_HOTKEY_ALREADY_REGISTERED"></span><span id="error_hotkey_already_registered"></span>**FEHLER \_ HOTKEY \_ BEREITS \_ REGISTRIERT**
</dt> <dd> <dl> <dt>

1409 (0x581)
</dt> <dt>



Der hot-Schlüssel ist bereits registriert.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLASS_ALREADY_EXISTS"></span><span id="error_class_already_exists"></span>**\_ERROR-KLASSE \_ IST BEREITS \_ VORHANDEN**
</dt> <dd> <dl> <dt>

1410 (0x582)
</dt> <dt>



Die Klasse ist bereits vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLASS_DOES_NOT_EXIST"></span><span id="error_class_does_not_exist"></span>**DIE \_ ERROR-KLASSE \_ IST NICHT \_ \_ VORHANDEN.**
</dt> <dd> <dl> <dt>

1411 (0x583)
</dt> <dt>



Die Klasse ist nicht vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLASS_HAS_WINDOWS"></span><span id="error_class_has_windows"></span>**\_ERROR-KLASSE \_ VERFÜGT ÜBER \_ WINDOWS**
</dt> <dd> <dl> <dt>

1412 (0x584)
</dt> <dt>



Die Klasse verfügt weiterhin über geöffnete Fenster.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_INDEX"></span><span id="error_invalid_index"></span>**FEHLER: \_ UNGÜLTIGER \_ INDEX**
</dt> <dd> <dl> <dt>

1413 (0x585)
</dt> <dt>



Ungültiger Index.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_ICON_HANDLE"></span><span id="error_invalid_icon_handle"></span>**FEHLER: \_ UNGÜLTIGES \_ \_ SYMBOLHANDLE**
</dt> <dd> <dl> <dt>

1414 (0x586)
</dt> <dt>



Ungültiges Symbolhandle.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRIVATE_DIALOG_INDEX"></span><span id="error_private_dialog_index"></span>**ERROR \_ PRIVATE \_ DIALOG \_ INDEX**
</dt> <dd> <dl> <dt>

1415 (0x587)
</dt> <dt>



Verwenden von privaten DIALOG-Fensterwörtern.


</dt> </dl> </dd> <dt>

<span id="ERROR_LISTBOX_ID_NOT_FOUND"></span><span id="error_listbox_id_not_found"></span>**\_ \_ FEHLERLISTEBOX-ID \_ NICHT \_ GEFUNDEN**
</dt> <dd> <dl> <dt>

1416 (0x588)
</dt> <dt>



Der Listenfeldbezeichner wurde nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_WILDCARD_CHARACTERS"></span><span id="error_no_wildcard_characters"></span>**FEHLER: \_ KEINE \_ \_ PLATZHALTERZEICHEN**
</dt> <dd> <dl> <dt>

1417 (0x589)
</dt> <dt>



Es wurden keine Platzhalter gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLIPBOARD_NOT_OPEN"></span><span id="error_clipboard_not_open"></span>**FEHLER: \_ ZWISCHENABLAGE \_ NICHT \_ GEÖFFNET**
</dt> <dd> <dl> <dt>

1418 (0x58A)
</dt> <dt>



Für den Thread ist keine Zwischenablage geöffnet.


</dt> </dl> </dd> <dt>

<span id="ERROR_HOTKEY_NOT_REGISTERED"></span><span id="error_hotkey_not_registered"></span>**FEHLER \_ HOTKEY \_ NICHT \_ REGISTRIERT**
</dt> <dd> <dl> <dt>

1419 (0x58B)
</dt> <dt>



Der Hot-Schlüssel ist nicht registriert.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINDOW_NOT_DIALOG"></span><span id="error_window_not_dialog"></span>**DIALOGFELD \_ \_ "FEHLERFENSTER \_ NICHT"**
</dt> <dd> <dl> <dt>

1420 (0x58C)
</dt> <dt>



Das Fenster ist kein gültiges Dialogfeld.


</dt> </dl> </dd> <dt>

<span id="ERROR_CONTROL_ID_NOT_FOUND"></span><span id="error_control_id_not_found"></span>**\_ \_ FEHLERSTEUERUNGS-ID \_ NICHT \_ GEFUNDEN**
</dt> <dd> <dl> <dt>

1421 (0x58D)
</dt> <dt>



Die Steuerelement-ID wurde nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_COMBOBOX_MESSAGE"></span><span id="error_invalid_combobox_message"></span>**FEHLER: \_ UNGÜLTIGE \_ \_ COMBOBOX-MELDUNG**
</dt> <dd> <dl> <dt>

1422 (0x58E)
</dt> <dt>



Ungültige Meldung für ein Kombinationsfeld, da es kein Bearbeitungssteuerelement besitzt.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINDOW_NOT_COMBOBOX"></span><span id="error_window_not_combobox"></span>**FEHLERFENSTER \_ \_ NICHT \_ COMBOBOX**
</dt> <dd> <dl> <dt>

1423 (0x58F)
</dt> <dt>



Das Fenster ist kein Kombinationsfeld.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_EDIT_HEIGHT"></span><span id="error_invalid_edit_height"></span>**FEHLER: \_ UNGÜLTIGE \_ \_ BEARBEITUNGSHÖHE**
</dt> <dd> <dl> <dt>

1424 (0x590)
</dt> <dt>



Die Höhe muss kleiner als 256 sein.


</dt> </dl> </dd> <dt>

<span id="ERROR_DC_NOT_FOUND"></span><span id="error_dc_not_found"></span>**FEHLER \_ DC \_ NICHT \_ GEFUNDEN**
</dt> <dd> <dl> <dt>

1425 (0x591)
</dt> <dt>



Ungültiges Gerätekontexthandle (DC).


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_HOOK_FILTER"></span><span id="error_invalid_hook_filter"></span>**FEHLER: \_ UNGÜLTIGER \_ \_ HOOKFILTER**
</dt> <dd> <dl> <dt>

1426 (0x592)
</dt> <dt>



Ungültiger Hookprozedurtyp.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_FILTER_PROC"></span><span id="error_invalid_filter_proc"></span>**FEHLER: \_ UNGÜLTIGE \_ \_ FILTERPROZITÄT**
</dt> <dd> <dl> <dt>

1427 (0x593)
</dt> <dt>



Ungültige Hookprozedur.


</dt> </dl> </dd> <dt>

<span id="ERROR_HOOK_NEEDS_HMOD"></span><span id="error_hook_needs_hmod"></span>**\_ \_ FEHLERHOOK BENÖTIGT \_ HMOD**
</dt> <dd> <dl> <dt>

1428 (0x594)
</dt> <dt>



Ein nichtlokaler Hook kann ohne Modulhand handle nicht festgelegt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_GLOBAL_ONLY_HOOK"></span><span id="error_global_only_hook"></span>**ERROR \_ GLOBAL \_ ONLY \_ HOOK**
</dt> <dd> <dl> <dt>

1429 (0x595)
</dt> <dt>



Diese Hookprozedur kann nur global festgelegt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_JOURNAL_HOOK_SET"></span><span id="error_journal_hook_set"></span>**HOOKSET \_ FÜR \_ FEHLERJOURNAL \_**
</dt> <dd> <dl> <dt>

1430 (0x596)
</dt> <dt>



Die Journalhookprozedur ist bereits installiert.


</dt> </dl> </dd> <dt>

<span id="ERROR_HOOK_NOT_INSTALLED"></span><span id="error_hook_not_installed"></span>**\_ \_ FEHLERHOOK NICHT \_ INSTALLIERT**
</dt> <dd> <dl> <dt>

1431 (0x597)
</dt> <dt>



Die Hookprozedur ist nicht installiert.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_LB_MESSAGE"></span><span id="error_invalid_lb_message"></span>**FEHLER: \_ \_ UNGÜLTIGE \_ LB-MELDUNG**
</dt> <dd> <dl> <dt>

1432 (0x598)
</dt> <dt>



Ungültige Meldung für das Listenfeld für die Einzelauswahl.


</dt> </dl> </dd> <dt>

<span id="ERROR_SETCOUNT_ON_BAD_LB"></span><span id="error_setcount_on_bad_lb"></span>**FEHLER: \_ SETCOUNT \_ FÜR BAD \_ \_ LB**
</dt> <dd> <dl> <dt>

1433 (0x599)
</dt> <dt>



LB \_ SETCOUNT wird an nicht verzögertes Listenfeld gesendet.


</dt> </dl> </dd> <dt>

<span id="ERROR_LB_WITHOUT_TABSTOPS"></span><span id="error_lb_without_tabstops"></span>**FEHLER \_ LB \_ OHNE \_ TABSTOPPS**
</dt> <dd> <dl> <dt>

1434 (0x59A)
</dt> <dt>



Dieses Listenfeld unterstützt keine Tabstopps.


</dt> </dl> </dd> <dt>

<span id="ERROR_DESTROY_OBJECT_OF_OTHER_THREAD"></span><span id="error_destroy_object_of_other_thread"></span>**ERROR \_ DESTROY \_ OBJECT \_ OF \_ OTHER \_ THREAD**
</dt> <dd> <dl> <dt>

1435 (0x59B)
</dt> <dt>



Das von einem anderen Thread erstellte Objekt kann nicht zerstört werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_CHILD_WINDOW_MENU"></span><span id="error_child_window_menu"></span>**MENÜ \_ "FEHLER IM \_ UNTERGEORDNETEN \_ FENSTER"**
</dt> <dd> <dl> <dt>

1436 (0x59C)
</dt> <dt>



Untergeordnete Fenster können keine Menüs haben.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SYSTEM_MENU"></span><span id="error_no_system_menu"></span>**FEHLER: \_ \_ MENÜ "KEIN \_ SYSTEM"**
</dt> <dd> <dl> <dt>

1437 (0x59D)
</dt> <dt>



Das Fenster verfügt nicht über ein Systemmenü.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_MSGBOX_STYLE"></span><span id="error_invalid_msgbox_style"></span>**FEHLER: \_ \_ UNGÜLTIGER MSGBOX-STIL \_**
</dt> <dd> <dl> <dt>

1438 (0x59E)
</dt> <dt>



Ungültiger Meldungsfeldstil.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SPI_VALUE"></span><span id="error_invalid_spi_value"></span>**FEHLER \_ UNGÜLTIGER \_ \_ SPI-WERT**
</dt> <dd> <dl> <dt>

1439 (0x59F)
</dt> <dt>



Ungültiger systemweiter Parameter \_ \* (SPI).


</dt> </dl> </dd> <dt>

<span id="ERROR_SCREEN_ALREADY_LOCKED"></span><span id="error_screen_already_locked"></span>**FEHLERBILDSCHIRM \_ \_ BEREITS \_ GESPERRT**
</dt> <dd> <dl> <dt>

1440 (0x5A0)
</dt> <dt>



Bildschirm bereits gesperrt.


</dt> </dl> </dd> <dt>

<span id="ERROR_HWNDS_HAVE_DIFF_PARENT"></span><span id="error_hwnds_have_diff_parent"></span>**\_FEHLER-HWNDS \_ VERFÜGEN ÜBER \_ ÜBERGEORDNETES \_ DIFF-ELEMENT**
</dt> <dd> <dl> <dt>

1441 (0x5A1)
</dt> <dt>



Alle Handles für Fenster in einer Positionsstruktur mit mehreren Fenstern müssen das gleiche übergeordnete Element haben.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_CHILD_WINDOW"></span><span id="error_not_child_window"></span>**FEHLER \_ NICHT \_ UNTERGEORDNETES \_ FENSTER**
</dt> <dd> <dl> <dt>

1442 (0x5A2)
</dt> <dt>



Das Fenster ist kein untergeordnetes Fenster.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_GW_COMMAND"></span><span id="error_invalid_gw_command"></span>**FEHLER: \_ UNGÜLTIGER \_ \_ GW-BEFEHL**
</dt> <dd> <dl> <dt>

1443 (0x5A3)
</dt> <dt>



Ungültiger \_ \* GW-Befehl.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_THREAD_ID"></span><span id="error_invalid_thread_id"></span>**FEHLER: \_ \_ UNGÜLTIGE \_ THREAD-ID**
</dt> <dd> <dl> <dt>

1444 (0x5A4)
</dt> <dt>



Ungültiger Threadbezeichner.


</dt> </dl> </dd> <dt>

<span id="ERROR_NON_MDICHILD_WINDOW"></span><span id="error_non_mdichild_window"></span>**FEHLERFENSTER \_ \_ "NICHT MDICHILD" \_**
</dt> <dd> <dl> <dt>

1445 (0x5A5)
</dt> <dt>



Eine Nachricht kann nicht aus einem Fenster, das kein MDI-Fenster (Multiple Document Interface) ist, verarbeiten.


</dt> </dl> </dd> <dt>

<span id="ERROR_POPUP_ALREADY_ACTIVE"></span><span id="error_popup_already_active"></span>**FEHLER \_ POPUP \_ BEREITS \_ AKTIV**
</dt> <dd> <dl> <dt>

1446 (0x5A6)
</dt> <dt>



Das Popupmenü ist bereits aktiv.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SCROLLBARS"></span><span id="error_no_scrollbars"></span>**FEHLER: \_ KEINE \_ SCROLLLEISTEN**
</dt> <dd> <dl> <dt>

1447 (0x5A7)
</dt> <dt>



Das Fenster verfügt nicht über Bildlaufleisten.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SCROLLBAR_RANGE"></span><span id="error_invalid_scrollbar_range"></span>**FEHLER: \_ \_ UNGÜLTIGER \_ SCROLLLEISTENBEREICH**
</dt> <dd> <dl> <dt>

1448 (0x5A8)
</dt> <dt>



Der Scrollleistenbereich darf nicht größer als MAXLONG sein.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SHOWWIN_COMMAND"></span><span id="error_invalid_showwin_command"></span>**FEHLER: \_ \_ UNGÜLTIGER SHOWWIN-BEFEHL \_**
</dt> <dd> <dl> <dt>

1449 (0x5A9)
</dt> <dt>



Das Fenster kann nicht wie angegeben angezeigt oder entfernt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SYSTEM_RESOURCES"></span><span id="error_no_system_resources"></span>**FEHLER: \_ \_ KEINE \_ SYSTEMRESSOURCEN**
</dt> <dd> <dl> <dt>

1450 (0x5AA)
</dt> <dt>



Es sind nicht genügend Systemressourcen vorhanden, um den angeforderten Dienst fertig zu stellen.


</dt> </dl> </dd> <dt>

<span id="ERROR_NONPAGED_SYSTEM_RESOURCES"></span><span id="error_nonpaged_system_resources"></span>**FEHLER: \_ NICHT AUSPAGEIERTE \_ \_ SYSTEMRESSOURCEN**
</dt> <dd> <dl> <dt>

1451 (0x5AB)
</dt> <dt>



Es sind nicht genügend Systemressourcen vorhanden, um den angeforderten Dienst fertig zu stellen.


</dt> </dl> </dd> <dt>

<span id="ERROR_PAGED_SYSTEM_RESOURCES"></span><span id="error_paged_system_resources"></span>**SYSTEMRESSOURCEN \_ MIT \_ FEHLERSEITE \_**
</dt> <dd> <dl> <dt>

1452 (0x5AC)
</dt> <dt>



Es sind nicht genügend Systemressourcen vorhanden, um den angeforderten Dienst fertig zu stellen.


</dt> </dl> </dd> <dt>

<span id="ERROR_WORKING_SET_QUOTA"></span><span id="error_working_set_quota"></span>**FEHLER BEIM \_ \_ \_ WORKINGSETKONTINGENT**
</dt> <dd> <dl> <dt>

1453 (0x5AD)
</dt> <dt>



Unzureichendes Kontingent zum Abschließen des angeforderten Diensts.


</dt> </dl> </dd> <dt>

<span id="ERROR_PAGEFILE_QUOTA"></span><span id="error_pagefile_quota"></span>**FEHLER: \_ \_ PAGEFILE-KONTINGENT**
</dt> <dd> <dl> <dt>

1454 (0x5AE)
</dt> <dt>



Unzureichendes Kontingent zum Abschließen des angeforderten Diensts.


</dt> </dl> </dd> <dt>

<span id="ERROR_COMMITMENT_LIMIT"></span><span id="error_commitment_limit"></span>**\_ \_ FEHLERBINDUNGSLIMIT**
</dt> <dd> <dl> <dt>

1455 (0x5AF)
</dt> <dt>



Die Auslagerungsdatei ist zu klein, um diesen Vorgang abschließen zu können.


</dt> </dl> </dd> <dt>

<span id="ERROR_MENU_ITEM_NOT_FOUND"></span><span id="error_menu_item_not_found"></span>**\_ \_ FEHLERMENÜELEMENT NICHT \_ \_ GEFUNDEN**
</dt> <dd> <dl> <dt>

1456 (0x5B0)
</dt> <dt>



Ein Menüelement wurde nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_KEYBOARD_HANDLE"></span><span id="error_invalid_keyboard_handle"></span>**FEHLER: \_ \_ UNGÜLTIGES \_ TASTATURHAND HANDLE**
</dt> <dd> <dl> <dt>

1457 (0x5B1)
</dt> <dt>



Ungültiges Tastaturlayouthand handle.


</dt> </dl> </dd> <dt>

<span id="ERROR_HOOK_TYPE_NOT_ALLOWED"></span><span id="error_hook_type_not_allowed"></span>**\_ \_ FEHLERHOOKTYP \_ NICHT \_ ZULÄSSIG**
</dt> <dd> <dl> <dt>

1458 (0x5B2)
</dt> <dt>



Hooktyp nicht zulässig.


</dt> </dl> </dd> <dt>

<span id="ERROR_REQUIRES_INTERACTIVE_WINDOWSTATION"></span><span id="error_requires_interactive_windowstation"></span>**FEHLER \_ ERFORDERT \_ INTERAKTIVE \_ WINDOWSTATION**
</dt> <dd> <dl> <dt>

1459 (0x5B3)
</dt> <dt>



Für diesen Vorgang ist eine interaktive Fensterstation erforderlich.


</dt> </dl> </dd> <dt>

<span id="ERROR_TIMEOUT"></span><span id="error_timeout"></span>**\_FEHLERZEITÜBERSCHREITUNG**
</dt> <dd> <dl> <dt>

1460 (0x5B4)
</dt> <dt>



Dieser Vorgang wurde wegen Zeitüberschreitung zurückgegeben.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_MONITOR_HANDLE"></span><span id="error_invalid_monitor_handle"></span>**FEHLER: \_ UNGÜLTIGES \_ MONITORHAND \_ HANDLE**
</dt> <dd> <dl> <dt>

1461 (0x5B5)
</dt> <dt>



Ungültiges Monitorhandle.


</dt> </dl> </dd> <dt>

<span id="ERROR_INCORRECT_SIZE"></span><span id="error_incorrect_size"></span>**FEHLER: \_ FALSCHE \_ GRÖßE**
</dt> <dd> <dl> <dt>

1462 (0x5B6)
</dt> <dt>



Falsches Größenargument.


</dt> </dl> </dd> <dt>

<span id="ERROR_SYMLINK_CLASS_DISABLED"></span><span id="error_symlink_class_disabled"></span>**ERROR \_ SYMLINK \_ CLASS \_ DISABLED**
</dt> <dd> <dl> <dt>

1463 (0x5B7)
</dt> <dt>



Dem symbolischen Link kann nicht gefolgt werden, da sein Typ deaktiviert ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_SYMLINK_NOT_SUPPORTED"></span><span id="error_symlink_not_supported"></span>**FEHLER \_ SYMLINK \_ WIRD NICHT \_ UNTERSTÜTZT**
</dt> <dd> <dl> <dt>

1464 (0x5B8)
</dt> <dt>



Diese Anwendung unterstützt den aktuellen Vorgang für symbolische Verknüpfungen nicht.


</dt> </dl> </dd> <dt>

<span id="ERROR_XML_PARSE_ERROR"></span><span id="error_xml_parse_error"></span>**ERROR \_ XML \_ PARSE \_ ERROR**
</dt> <dd> <dl> <dt>

1465 (0x5B9)
</dt> <dt>



Windows konnte die angeforderten XML-Daten nicht analysieren.


</dt> </dl> </dd> <dt>

<span id="ERROR_XMLDSIG_ERROR"></span><span id="error_xmldsig_error"></span>**FEHLER: \_ \_ XMLDSIG-FEHLER**
</dt> <dd> <dl> <dt>

1466 (0x5BA)
</dt> <dt>



Beim Verarbeiten einer digitalen XML-Signatur ist ein Fehler aufgetreten.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESTART_APPLICATION"></span><span id="error_restart_application"></span>**FEHLER \_ BEIM \_ NEUSTARTEN DER ANWENDUNG**
</dt> <dd> <dl> <dt>

1467 (0x5BB)
</dt> <dt>



Diese Anwendung muss neu gestartet werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_WRONG_COMPARTMENT"></span><span id="error_wrong_compartment"></span>**FEHLER \_ IN FALSCHEM \_ DEPOT**
</dt> <dd> <dl> <dt>

1468 (0x5BC)
</dt> <dt>



Der Aufrufer hat die Verbindungsanforderung im falschen Routingde depot vorgenommen.


</dt> </dl> </dd> <dt>

<span id="ERROR_AUTHIP_FAILURE"></span><span id="error_authip_failure"></span>**FEHLER: \_ \_ AUTHIP-FEHLER**
</dt> <dd> <dl> <dt>

1469 (0x5BD)
</dt> <dt>



Beim Versuch, eine Verbindung mit dem Remotehost herzustellen, ist ein AuthIP-Fehler vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_NVRAM_RESOURCES"></span><span id="error_no_nvram_resources"></span>**FEHLER \_ KEINE \_ \_ NVRAM-RESSOURCEN**
</dt> <dd> <dl> <dt>

1470 (0x5BE)
</dt> <dt>



Es sind nicht genügend NVRAM-Ressourcen vorhanden, um den angeforderten Dienst abzuschließen. Möglicherweise ist ein Neustart erforderlich.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_GUI_PROCESS"></span><span id="error_not_gui_process"></span>**FEHLER \_ NICHT \_ \_ GUI-PROZESS**
</dt> <dd> <dl> <dt>

1471 (0x5BF)
</dt> <dt>



Der angeforderte Vorgang kann nicht abgeschlossen werden, da der angegebene Prozess kein GUI-Prozess ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVENTLOG_FILE_CORRUPT"></span><span id="error_eventlog_file_corrupt"></span>**\_FEHLER: \_ EREIGNISPROTOKOLLDATEI \_ BESCHÄDIGT**
</dt> <dd> <dl> <dt>

1500 (0x5DC)
</dt> <dt>



Die Ereignisprotokolldatei ist beschädigt.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVENTLOG_CANT_START"></span><span id="error_eventlog_cant_start"></span>**FEHLER: \_ EVENTLOG \_ CANT \_ START**
</dt> <dd> <dl> <dt>

1501 (0x5DD)
</dt> <dt>



Es konnte keine Ereignisprotokolldatei geöffnet werden, sodass der Ereignisprotokollierungsdienst nicht gestartet wurde.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_FILE_FULL"></span><span id="error_log_file_full"></span>**\_ \_ FEHLERPROTOKOLLDATEI \_ VOLLSTÄNDIG**
</dt> <dd> <dl> <dt>

1502 (0x5DE)
</dt> <dt>



Die Ereignisprotokolldatei ist voll.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVENTLOG_FILE_CHANGED"></span><span id="error_eventlog_file_changed"></span>**\_FEHLER: \_ EREIGNISPROTOKOLLDATEI \_ GEÄNDERT**
</dt> <dd> <dl> <dt>

1503 (0x5DF)
</dt> <dt>



Die Ereignisprotokolldatei hat sich zwischen Lesevorgängen geändert.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_TASK_NAME"></span><span id="error_invalid_task_name"></span>**FEHLER: \_ UNGÜLTIGER \_ \_ AUFGABENNAME**
</dt> <dd> <dl> <dt>

1550 (0x60E)
</dt> <dt>



Der angegebene Aufgabenname ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_TASK_INDEX"></span><span id="error_invalid_task_index"></span>**FEHLER: \_ UNGÜLTIGER \_ \_ TASKINDEX**
</dt> <dd> <dl> <dt>

1551 (0x60F)
</dt> <dt>



Der angegebene Aufgabenindex ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_THREAD_ALREADY_IN_TASK"></span><span id="error_thread_already_in_task"></span>**\_FEHLERTHREAD \_ BEREITS IM \_ \_ TASK**
</dt> <dd> <dl> <dt>

1552 (0x610)
</dt> <dt>



Der angegebene Thread wird bereits einer Aufgabe beitreten.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_SERVICE_FAILURE"></span><span id="error_install_service_failure"></span>**FEHLER BEIM \_ INSTALLIEREN \_ DES \_ DIENSTS**
</dt> <dd> <dl> <dt>

1601 (0x641)
</dt> <dt>



Auf den Windows Installer-Dienst konnte nicht zugegriffen werden. Dies kann auftreten, wenn der Windows Installer nicht ordnungsgemäß installiert ist. Wenden Sie sich an Ihr Supportpersonal, um Unterstützung zu erhalten.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_USEREXIT"></span><span id="error_install_userexit"></span>**FEHLER \_ BEI DER INSTALLATION VON \_ USEREXIT**
</dt> <dd> <dl> <dt>

1602 (0x642)
</dt> <dt>



Der Benutzer hat die Installation abgebrochen.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_FAILURE"></span><span id="error_install_failure"></span>**FEHLER BEI \_ DER INSTALLATION \_**
</dt> <dd> <dl> <dt>

1603 (0x643)
</dt> <dt>



Schwerwiegender Fehler bei der Installation.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_SUSPEND"></span><span id="error_install_suspend"></span>**FEHLER \_ BEIM INSTALLIEREN VON \_ "SUSPEND"**
</dt> <dd> <dl> <dt>

1604 (0x644)
</dt> <dt>



Installation angehalten, unvollständig.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNKNOWN_PRODUCT"></span><span id="error_unknown_product"></span>**FEHLER \_ \_ UNBEKANNTES PRODUKT**
</dt> <dd> <dl> <dt>

1605 (0x645)
</dt> <dt>



Diese Aktion ist nur für Produkte gültig, die derzeit installiert sind.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNKNOWN_FEATURE"></span><span id="error_unknown_feature"></span>**\_ \_ FEHLER: UNBEKANNTES FEATURE**
</dt> <dd> <dl> <dt>

1606 (0x646)
</dt> <dt>



Feature-ID nicht registriert.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNKNOWN_COMPONENT"></span><span id="error_unknown_component"></span>**\_FEHLER UNBEKANNTE \_ KOMPONENTE**
</dt> <dd> <dl> <dt>

1607 (0x647)
</dt> <dt>



Komponenten-ID nicht registriert.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNKNOWN_PROPERTY"></span><span id="error_unknown_property"></span>**ERROR \_ UNKNOWN \_ PROPERTY**
</dt> <dd> <dl> <dt>

1608 (0x648)
</dt> <dt>



Unbekannte Eigenschaft.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_HANDLE_STATE"></span><span id="error_invalid_handle_state"></span>**FEHLER: \_ UNGÜLTIGER \_ \_ HANDLEZUSTAND**
</dt> <dd> <dl> <dt>

1609 (0x649)
</dt> <dt>



Das Handle befindet sich in einem ungültigen Zustand.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_CONFIGURATION"></span><span id="error_bad_configuration"></span>**FEHLER: \_ FEHLERHAFTE \_ KONFIGURATION**
</dt> <dd> <dl> <dt>

1610 (0x64A)
</dt> <dt>



Die Konfigurationsdaten für dieses Produkt sind beschädigt. Wenden Sie sich an Ihre Supportmitarbeiter.


</dt> </dl> </dd> <dt>

<span id="ERROR_INDEX_ABSENT"></span><span id="error_index_absent"></span>**FEHLERINDEX \_ \_ NICHT VORHANDEN**
</dt> <dd> <dl> <dt>

1611 (0x64B)
</dt> <dt>



Komponentenqualifizierer nicht vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_SOURCE_ABSENT"></span><span id="error_install_source_absent"></span>**FEHLER \_ BEI DER INSTALLATION DER QUELLE \_ \_ ABSENT**
</dt> <dd> <dl> <dt>

1612 (0x64C)
</dt> <dt>



Die Installationsquelle für dieses Produkt ist nicht verfügbar. Vergewissern Sie sich, dass die Quelle vorhanden ist und Sie darauf zugreifen können.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_PACKAGE_VERSION"></span><span id="error_install_package_version"></span>**FEHLER BEI \_ \_ DER \_ PAKETINSTALLATIONSVERSION**
</dt> <dd> <dl> <dt>

1613 (0x64D)
</dt> <dt>



Dieses Installationspaket kann nicht vom Windows Installer-Dienst installiert werden. Sie müssen ein Windows Service Pack installieren, das eine neuere Version des Windows Installer-Diensts enthält.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRODUCT_UNINSTALLED"></span><span id="error_product_uninstalled"></span>**FEHLER \_ PRODUKT \_ DEINSTALLIERT**
</dt> <dd> <dl> <dt>

1614 (0x64E)
</dt> <dt>



Produkt wird deinstalliert.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_QUERY_SYNTAX"></span><span id="error_bad_query_syntax"></span>**FEHLER: \_ FEHLERHAFTE \_ \_ ABFRAGESYNTAX**
</dt> <dd> <dl> <dt>

1615 (0x64F)
</dt> <dt>



SQL Abfragesyntax ungültig oder nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_FIELD"></span><span id="error_invalid_field"></span>**FEHLER \_ UNGÜLTIGES \_ FELD**
</dt> <dd> <dl> <dt>

1616 (0x650)
</dt> <dt>



Das Datensatzfeld ist nicht vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_REMOVED"></span><span id="error_device_removed"></span>**FEHLER \_ GERÄT \_ ENTFERNT**
</dt> <dd> <dl> <dt>

1617 (0x651)
</dt> <dt>



Das Gerät wurde entfernt.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_ALREADY_RUNNING"></span><span id="error_install_already_running"></span>**FEHLER: \_ INSTALLATION \_ WIRD BEREITS \_ AUSGEFÜHRT**
</dt> <dd> <dl> <dt>

1618 (0x652)
</dt> <dt>



Eine andere Installation wird bereits in Bearbeitung. Schließen Sie diese Installation ab, bevor Sie mit dieser Installation fortfahren.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_PACKAGE_OPEN_FAILED"></span><span id="error_install_package_open_failed"></span>**FEHLER BEIM \_ ÖFFNEN \_ DES \_ \_ INSTALLATIONSPAKETS.**
</dt> <dd> <dl> <dt>

1619 (0x653)
</dt> <dt>



Dieses Installationspaket konnte nicht geöffnet werden. Vergewissern Sie sich, dass das Paket vorhanden ist und Sie darauf zugreifen können, oder wenden Sie sich an den Anwendungsanbieter, um sicherzustellen, dass es sich um ein gültiges Paket Windows Installer handelt.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_PACKAGE_INVALID"></span><span id="error_install_package_invalid"></span>**FEHLER \_ BEIM INSTALLIEREN DES \_ \_ PAKETS UNGÜLTIG**
</dt> <dd> <dl> <dt>

1620 (0x654)
</dt> <dt>



Dieses Installationspaket konnte nicht geöffnet werden. Wenden Sie sich an den Anwendungsanbieter, um zu überprüfen, ob es sich um ein gültiges Windows Installer-Paket handelt.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_UI_FAILURE"></span><span id="error_install_ui_failure"></span>**FEHLER BEIM \_ INSTALLIEREN DER \_ \_ BENUTZEROBERFLÄCHE**
</dt> <dd> <dl> <dt>

1621 (0x655)
</dt> <dt>



Fehler beim Starten der Benutzeroberfläche Windows Installer-Diensts. Wenden Sie sich an Ihre Supportmitarbeiter.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_LOG_FAILURE"></span><span id="error_install_log_failure"></span>**FEHLER BEIM \_ INSTALLIEREN \_ DES PROTOKOLLS \_**
</dt> <dd> <dl> <dt>

1622 (0x656)
</dt> <dt>



Fehler beim Öffnen der Installationsprotokolldatei. Vergewissern Sie sich, dass der angegebene Protokolldateispeicherort vorhanden ist und Sie in die Datei schreiben können.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_LANGUAGE_UNSUPPORTED"></span><span id="error_install_language_unsupported"></span>**FEHLER \_ BEIM INSTALLIEREN DER SPRACHE NICHT \_ \_ UNTERSTÜTZT**
</dt> <dd> <dl> <dt>

1623 (0x657)
</dt> <dt>



Die Sprache dieses Installationspakets wird vom System nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_TRANSFORM_FAILURE"></span><span id="error_install_transform_failure"></span>**FEHLER BEIM \_ INSTALLIEREN DES \_ \_ TRANSFORMATIONSFEHLERS**
</dt> <dd> <dl> <dt>

1624 (0x658)
</dt> <dt>



Fehler beim Anwenden von Transformationen. Überprüfen Sie, ob die angegebenen Transformationspfade gültig sind.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_PACKAGE_REJECTED"></span><span id="error_install_package_rejected"></span>**FEHLER \_ BEIM ABLEHNEN DES \_ \_ INSTALLATIONSPAKETS**
</dt> <dd> <dl> <dt>

1625 (0x659)
</dt> <dt>



Diese Installation ist durch die Systemrichtlinie unzulässig. Wenden Sie sich an Ihren Systemadministrator.


</dt> </dl> </dd> <dt>

<span id="ERROR_FUNCTION_NOT_CALLED"></span><span id="error_function_not_called"></span>**FEHLERFUNKTION \_ \_ NICHT \_ AUFGERUFEN**
</dt> <dd> <dl> <dt>

1626 (0x65A)
</dt> <dt>



Die Funktion konnte nicht ausgeführt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_FUNCTION_FAILED"></span><span id="error_function_failed"></span>**FEHLER \_ BEI \_ FUNKTIONSFEHLER**
</dt> <dd> <dl> <dt>

1627 (0x65B)
</dt> <dt>



Fehler bei der Funktion während der Ausführung.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_TABLE"></span><span id="error_invalid_table"></span>**FEHLER: \_ UNGÜLTIGE \_ TABELLE**
</dt> <dd> <dl> <dt>

1628 (0x65C)
</dt> <dt>



Ungültige oder unbekannte Tabelle angegeben.


</dt> </dl> </dd> <dt>

<span id="ERROR_DATATYPE_MISMATCH"></span><span id="error_datatype_mismatch"></span>**\_FEHLER: \_ DATENTYPKONFLIKT**
</dt> <dd> <dl> <dt>

1629 (0x65D)
</dt> <dt>



Die bereitgestellten Daten sind vom falschen Typ.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNSUPPORTED_TYPE"></span><span id="error_unsupported_type"></span>**FEHLER: \_ NICHT UNTERSTÜTZTER \_ TYP**
</dt> <dd> <dl> <dt>

1630 (0x65E)
</dt> <dt>



Daten dieses Typs werden nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="ERROR_CREATE_FAILED"></span><span id="error_create_failed"></span>**FEHLER \_ BEIM ERSTELLEN \_**
</dt> <dd> <dl> <dt>

1631 (0x65F)
</dt> <dt>



Der Windows Installer-Dienst konnte nicht gestartet werden. Wenden Sie sich an Ihre Supportmitarbeiter.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_TEMP_UNWRITABLE"></span><span id="error_install_temp_unwritable"></span>**FEHLER: \_ \_ INSTALLATION VON TEMP \_ UNWRITABLE**
</dt> <dd> <dl> <dt>

1632 (0x660)
</dt> <dt>



Der Ordner Temp befindet sich auf einem Laufwerk, das voll ist oder auf das nicht zugegriffen werden kann. Geben Sie Speicherplatz auf dem Laufwerk frei, oder vergewissern Sie sich, dass Sie über schreibberechtigungen für den Ordner Temp verfügen.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_PLATFORM_UNSUPPORTED"></span><span id="error_install_platform_unsupported"></span>**FEHLER \_ BEIM INSTALLIEREN DER PLATTFORM NICHT \_ \_ UNTERSTÜTZT**
</dt> <dd> <dl> <dt>

1633 (0x661)
</dt> <dt>



Dieses Installationspaket wird von diesem Prozessortyp nicht unterstützt. Wenden Sie sich an Ihren Produkthersteller.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_NOTUSED"></span><span id="error_install_notused"></span>**FEHLER: \_ INSTALLATION \_ NICHTVERWENDT**
</dt> <dd> <dl> <dt>

1634 (0x662)
</dt> <dt>



Die Komponente wird auf diesem Computer nicht verwendet.


</dt> </dl> </dd> <dt>

<span id="ERROR_PATCH_PACKAGE_OPEN_FAILED"></span><span id="error_patch_package_open_failed"></span>**FEHLER BEIM \_ ÖFFNEN \_ DES \_ \_ PATCHPAKETS**
</dt> <dd> <dl> <dt>

1635 (0x663)
</dt> <dt>



Dieses Updatepaket konnte nicht geöffnet werden. Vergewissern Sie sich, dass das Updatepaket vorhanden ist und Sie darauf zugreifen können, oder wenden Sie sich an den Anwendungsanbieter, um sicherzustellen, dass es sich um ein gültiges Updatepaket Windows Installer handelt.


</dt> </dl> </dd> <dt>

<span id="ERROR_PATCH_PACKAGE_INVALID"></span><span id="error_patch_package_invalid"></span>**FEHLER \_ \_ PATCHPAKET \_ UNGÜLTIG**
</dt> <dd> <dl> <dt>

1636 (0x664)
</dt> <dt>



Dieses Updatepaket konnte nicht geöffnet werden. Wenden Sie sich an den Anwendungsanbieter, um sicherzustellen, dass es sich um ein gültiges Windows Installer-Updatepaket handelt.


</dt> </dl> </dd> <dt>

<span id="ERROR_PATCH_PACKAGE_UNSUPPORTED"></span><span id="error_patch_package_unsupported"></span>**FEHLER \_ \_ PATCHPAKET \_ NICHT UNTERSTÜTZT**
</dt> <dd> <dl> <dt>

1637 (0x665)
</dt> <dt>



Dieses Updatepaket kann nicht vom Installationsinstallationsdienst Windows verarbeitet werden. Sie müssen ein Windows Service Pack installieren, das eine neuere Version des Windows Installer-Diensts enthält.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRODUCT_VERSION"></span><span id="error_product_version"></span>**FEHLER \_ \_ PRODUKTVERSION**
</dt> <dd> <dl> <dt>

1638 (0x666)
</dt> <dt>



Eine andere Version dieses Produkts ist bereits installiert. Die Installation dieser Version kann nicht fortgesetzt werden. Um die vorhandene Version dieses Produkts zu konfigurieren oder zu entfernen, verwenden Sie auf der Seite Software Systemsteuerung.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_COMMAND_LINE"></span><span id="error_invalid_command_line"></span>**FEHLER: \_ \_ UNGÜLTIGE \_ BEFEHLSZEILE**
</dt> <dd> <dl> <dt>

1639 (0x667)
</dt> <dt>



Ungültiges Befehlszeilenargument. Ausführliche Befehlszeilenhilfen Windows sie im Sdk für den Installer.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_REMOTE_DISALLOWED"></span><span id="error_install_remote_disallowed"></span>**FEHLER \_ BEI \_ \_ REMOTEINSTALLIEREN NICHT VERFÜGBAR**
</dt> <dd> <dl> <dt>

1640 (0x668)
</dt> <dt>



Nur Administratoren verfügen über die Berechtigung zum Hinzufügen, Entfernen oder Konfigurieren von Serversoftware während einer Remotesitzung mit Terminaldiensten. Wenn Sie Software auf dem Server installieren oder konfigurieren möchten, wenden Sie sich an Ihren Netzwerkadministrator.


</dt> </dl> </dd> <dt>

<span id="ERROR_SUCCESS_REBOOT_INITIATED"></span><span id="error_success_reboot_initiated"></span>**FEHLER: \_ \_ NEUSTART ERFOLGREICH \_ INITIIERT**
</dt> <dd> <dl> <dt>

1641 (0x669)
</dt> <dt>



Der angeforderte Vorgang wurde erfolgreich abgeschlossen. Das System wird neu gestartet, damit die Änderungen wirksam werden können.


</dt> </dl> </dd> <dt>

<span id="ERROR_PATCH_TARGET_NOT_FOUND"></span><span id="error_patch_target_not_found"></span>**\_ \_ FEHLERPATCHZIEL NICHT \_ \_ GEFUNDEN**
</dt> <dd> <dl> <dt>

1642 (0x66A)
</dt> <dt>



Das Upgrade kann nicht vom Windows Installer-Dienst installiert werden, da das zu aktualisierende Programm möglicherweise fehlt oder das Upgrade eine andere Version des Programms aktualisiert. Vergewissern Sie sich, dass das zu aktualisierende Programm auf Ihrem Computer vorhanden ist und dass Sie über das richtige Upgrade verfügen.


</dt> </dl> </dd> <dt>

<span id="ERROR_PATCH_PACKAGE_REJECTED"></span><span id="error_patch_package_rejected"></span>**\_ \_ FEHLERPATCHPAKET \_ ABGELEHNT**
</dt> <dd> <dl> <dt>

1643 (0x66B)
</dt> <dt>



Das Updatepaket ist durch die Softwareeinschränkungsrichtlinie nicht zulässig.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_TRANSFORM_REJECTED"></span><span id="error_install_transform_rejected"></span>**FEHLER \_ BEIM INSTALLIEREN DER TRANSFORMATION \_ \_ ABGELEHNT**
</dt> <dd> <dl> <dt>

1644 (0x66C)
</dt> <dt>



Eine oder mehrere Anpassungen sind durch die Softwareeinschränkungsrichtlinie nicht zulässig.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_REMOTE_PROHIBITED"></span><span id="error_install_remote_prohibited"></span>**FEHLER \_ BEI REMOTEINSTALLATION \_ \_ UNZULÄSSIG**
</dt> <dd> <dl> <dt>

1645 (0x66D)
</dt> <dt>



Der Windows Installer lässt die Installation von einem Remotedesktopverbindung nicht zu.


</dt> </dl> </dd> <dt>

<span id="ERROR_PATCH_REMOVAL_UNSUPPORTED"></span><span id="error_patch_removal_unsupported"></span>**\_ \_ FEHLERPATCHENTFERNUNG NICHT \_ UNTERSTÜTZT**
</dt> <dd> <dl> <dt>

1646 (0x66E)
</dt> <dt>



Die Deinstallation des Updatepakets wird nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNKNOWN_PATCH"></span><span id="error_unknown_patch"></span>**FEHLER \_ UNBEKANNTER \_ PATCH**
</dt> <dd> <dl> <dt>

1647 (0x66F)
</dt> <dt>



Das Update wird nicht auf dieses Produkt angewendet.


</dt> </dl> </dd> <dt>

<span id="ERROR_PATCH_NO_SEQUENCE"></span><span id="error_patch_no_sequence"></span>**FEHLERPATCH \_ \_ KEINE \_ SEQUENZ**
</dt> <dd> <dl> <dt>

1648 (0x670)
</dt> <dt>



Es konnte keine gültige Sequenz für den Satz von Updates gefunden werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_PATCH_REMOVAL_DISALLOWED"></span><span id="error_patch_removal_disallowed"></span>**FEHLER \_ BEIM ENTFERNEN VON \_ \_ PATCHES NICHT ZULÄSSIG**
</dt> <dd> <dl> <dt>

1649 (0x671)
</dt> <dt>



Das Entfernen von Updates wurde durch die Richtlinie nicht zugelassen.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PATCH_XML"></span><span id="error_invalid_patch_xml"></span>**FEHLER: \_ UNGÜLTIGER \_ \_ PATCH-XML-CODE**
</dt> <dd> <dl> <dt>

1650 (0x672)
</dt> <dt>



Die XML-Updatedaten sind ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_PATCH_MANAGED_ADVERTISED_PRODUCT"></span><span id="error_patch_managed_advertised_product"></span>**VOM \_ FEHLERPATCH \_ \_ VERWALTETES \_ ANGEKÜNDIGTES PRODUKT**
</dt> <dd> <dl> <dt>

1651 (0x673)
</dt> <dt>



Windows Das Installationsprogramm lässt keine Aktualisierung von verwalteten angekündigten Produkten zu. Vor dem Anwenden des Updates muss mindestens ein Feature des Produkts installiert werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_SERVICE_SAFEBOOT"></span><span id="error_install_service_safeboot"></span>**FEHLER BEIM \_ INSTALLIEREN \_ DES \_ DIENSTS SAFEBOOT**
</dt> <dd> <dl> <dt>

1652 (0x674)
</dt> <dt>



Auf den Windows Installer-Dienst kann im Tresor-Modus nicht zugegriffen werden. Versuchen Sie es erneut, wenn sich Ihr Computer nicht im Tresor Modus befindet oder Sie die Systemwiederherstellung verwenden können, um den Computer wieder in einen früheren guten Zustand zu versetzen.


</dt> </dl> </dd> <dt>

<span id="ERROR_FAIL_FAST_EXCEPTION"></span><span id="error_fail_fast_exception"></span>**FEHLERFEHLER \_ \_ FAST \_ AUSNAHME**
</dt> <dd> <dl> <dt>

1653 (0x675)
</dt> <dt>



Es ist eine Fail-Fast-Ausnahme aufgetreten. Ausnahmehandler werden nicht aufgerufen, und der Prozess wird sofort beendet.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_REJECTED"></span><span id="error_install_rejected"></span>**FEHLER \_ BEI DER INSTALLATION \_ ABGELEHNT**
</dt> <dd> <dl> <dt>

1654 (0x676)
</dt> <dt>



Die App, die Sie ausführen möchten, wird für diese Version von Windows nicht unterstützt.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>WinError.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Systemfehlercodes](system-error-codes.md)
</dt> </dl>

 

 




