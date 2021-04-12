---
description: Beschreibt die in der Header Datei "Winerror. h" definierten Fehlercodes 1300-1699 und ist für Entwickler bestimmt.
ms.assetid: 7b04a2ba-7bf9-4bff-93c8-cbb0060e069d
title: System Fehler Codes (1300-1699) (Winerror. h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: 8fa0cbc312c8d82879322f0bc0c79533ddb961ce
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483318"
---
# <a name="system-error-codes-1300-1699"></a>System Fehler Codes (1300-1699)

> [!NOTE]
> Diese Informationen sind für Entwickler gedacht, die Systemfehler Debuggen. Bei anderen Fehlern, wie z. b. Problemen mit Windows Update, finden Sie eine Liste der Ressourcen auf der Seite [Fehlercodes](system-error-codes.md) .

In der folgenden Liste werden die [Systemfehler Codes](system-error-codes.md) für die Fehler 1300 bis 1699 beschrieben. Sie werden von der [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) -Funktion zurückgegeben, wenn viele Funktionen fehlschlagen. Um den Beschreibungstext für den Fehler in Ihrer Anwendung abzurufen, verwenden Sie die [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) -Funktion mit dem Flag " **Format \_ Message \_ from \_ System** ".

<dl> <dt>

<span id="ERROR_NOT_ALL_ASSIGNED"></span><span id="error_not_all_assigned"></span>**Fehler \_ nicht \_ alle \_ zugewiesen**
</dt> <dd> <dl> <dt>

1300 (0x514)
</dt> <dt>



Nicht alle Berechtigungen oder Gruppen, auf die verwiesen wird, werden dem Aufrufer zugewiesen.


</dt> </dl> </dd> <dt>

<span id="ERROR_SOME_NOT_MAPPED"></span><span id="error_some_not_mapped"></span>**Fehler \_ " \_ nicht \_ zugeordnet"**
</dt> <dd> <dl> <dt>

1301 (0x515)
</dt> <dt>



Es wurde keine Zuordnung zwischen Kontonamen und Sicherheits-IDs vorgenommen.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_QUOTAS_FOR_ACCOUNT"></span><span id="error_no_quotas_for_account"></span>**Fehler " \_ keine \_ Kontingente \_ für \_ Konto"**
</dt> <dd> <dl> <dt>

1302 (0x516)
</dt> <dt>



Für dieses Konto sind keine System Kontingent Limits festgelegt.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOCAL_USER_SESSION_KEY"></span><span id="error_local_user_session_key"></span>**Fehler beim \_ lokalen \_ Benutzer \_ Sitzungs \_ Schlüssel.**
</dt> <dd> <dl> <dt>

1303 (0x517)
</dt> <dt>



Es ist kein Verschlüsselungsschlüssel verfügbar. Es wurde ein bekannter Verschlüsselungsschlüssel zurückgegeben.


</dt> </dl> </dd> <dt>

<span id="ERROR_NULL_LM_PASSWORD"></span><span id="error_null_lm_password"></span>**Fehler \_ NULL \_ LM- \_ Kennwort**
</dt> <dd> <dl> <dt>

1304 (0x518)
</dt> <dt>



Das Kennwort ist zu komplex, um in ein LAN-Manager-Kennwort konvertiert zu werden. Das zurückgegebene LAN Manager-Kennwort ist eine **null** -Zeichenfolge.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNKNOWN_REVISION"></span><span id="error_unknown_revision"></span>**Unbekannter Fehler. \_ \_**
</dt> <dd> <dl> <dt>

1305 (0x519)
</dt> <dt>



Die Revisions Ebene ist unbekannt.


</dt> </dl> </dd> <dt>

<span id="ERROR_REVISION_MISMATCH"></span><span id="error_revision_mismatch"></span>**Fehler \_ Revision nicht übereinstimmende \_**
</dt> <dd> <dl> <dt>

1306 (0x51A)
</dt> <dt>



Gibt an, dass zwei Revisions Ebenen nicht kompatibel sind.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_OWNER"></span><span id="error_invalid_owner"></span>**Fehler \_ ungültiger \_ Besitzer**
</dt> <dd> <dl> <dt>

1307 (0x51B)
</dt> <dt>



Diese Sicherheits-ID kann nicht als Besitzer dieses Objekts zugewiesen werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PRIMARY_GROUP"></span><span id="error_invalid_primary_group"></span>**Fehler \_ ungültige \_ primäre \_ Gruppe**
</dt> <dd> <dl> <dt>

1308 (0x51C)
</dt> <dt>



Diese Sicherheits-ID darf nicht als primäre Gruppe eines Objekts zugewiesen werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_IMPERSONATION_TOKEN"></span><span id="error_no_impersonation_token"></span>**Fehler \_ ohne Identitätswechsel \_ \_ Token**
</dt> <dd> <dl> <dt>

1309 (0x51D)
</dt> <dt>



Es wurde versucht, einen Identitätswechsel Token von einem Thread auszuführen, der derzeit nicht die Identität eines Clients annimmt.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_DISABLE_MANDATORY"></span><span id="error_cant_disable_mandatory"></span>**Fehler \_ beim \_ Deaktivieren \_ obligatorisch.**
</dt> <dd> <dl> <dt>

1310 (0x51E)
</dt> <dt>



Die Gruppe ist möglicherweise nicht deaktiviert.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_LOGON_SERVERS"></span><span id="error_no_logon_servers"></span>**Fehler \_ keine \_ Anmelde \_ Server**
</dt> <dd> <dl> <dt>

1311 (0x51F)
</dt> <dt>



Zurzeit stehen keine Anmelde Server zur Verfügung, um die Anmelde Anforderung zu bedienen.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SUCH_LOGON_SESSION"></span><span id="error_no_such_logon_session"></span>**Fehler \_ keine \_ solche \_ Anmelde \_ Sitzung.**
</dt> <dd> <dl> <dt>

1312 (0x520)
</dt> <dt>



Eine angegebene Anmeldesitzung ist nicht vorhanden. Möglicherweise wurde Sie bereits beendet.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SUCH_PRIVILEGE"></span><span id="error_no_such_privilege"></span>**Fehler \_ keine \_ solche \_ Berechtigung**
</dt> <dd> <dl> <dt>

1313 (0x521)
</dt> <dt>



Es ist kein bestimmtes Privileg vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRIVILEGE_NOT_HELD"></span><span id="error_privilege_not_held"></span>**Fehler \_ Berechtigungen \_ nicht \_ gespeichert**
</dt> <dd> <dl> <dt>

1314 (0x522)
</dt> <dt>



Dem Client fehlt ein erforderliches Privileg.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_ACCOUNT_NAME"></span><span id="error_invalid_account_name"></span>**\_ungültiger \_ \_ Kontoname.**
</dt> <dd> <dl> <dt>

1315 (0x523)
</dt> <dt>



Der angegebene Name ist kein ordnungsgemäß formatierter Kontoname.


</dt> </dl> </dd> <dt>

<span id="ERROR_USER_EXISTS"></span><span id="error_user_exists"></span>**Fehler \_ Benutzer ist \_ vorhanden.**
</dt> <dd> <dl> <dt>

1316 (0x524)
</dt> <dt>



Das angegebene Konto ist bereits vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SUCH_USER"></span><span id="error_no_such_user"></span>**Fehler " \_ kein \_ solcher \_ Benutzer"**
</dt> <dd> <dl> <dt>

1317 (0x525)
</dt> <dt>



Das angegebene Konto ist nicht vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_GROUP_EXISTS"></span><span id="error_group_exists"></span>**Fehler \_ Gruppe \_ vorhanden**
</dt> <dd> <dl> <dt>

1318 (0x526)
</dt> <dt>



Die angegebene Gruppe ist bereits vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SUCH_GROUP"></span><span id="error_no_such_group"></span>**Fehler " \_ keine \_ solche \_ Gruppe"**
</dt> <dd> <dl> <dt>

1319 (0x527)
</dt> <dt>



Die angegebene Gruppe ist nicht vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_MEMBER_IN_GROUP"></span><span id="error_member_in_group"></span>**Fehler \_ Mitglied \_ in \_ Gruppe**
</dt> <dd> <dl> <dt>

1320 (0x528)
</dt> <dt>



Das angegebene Benutzerkonto ist bereits ein Mitglied der angegebenen Gruppe, oder die angegebene Gruppe kann nicht gelöscht werden, weil Sie ein Mitglied enthält.


</dt> </dl> </dd> <dt>

<span id="ERROR_MEMBER_NOT_IN_GROUP"></span><span id="error_member_not_in_group"></span>**Fehler \_ Mitglied \_ nicht \_ in \_ Gruppe**
</dt> <dd> <dl> <dt>

1321 (0x529)
</dt> <dt>



Das angegebene Benutzerkonto ist kein Mitglied des angegebenen Gruppen Kontos.


</dt> </dl> </dd> <dt>

<span id="ERROR_LAST_ADMIN"></span><span id="error_last_admin"></span>**\_Letzter \_ Administrator des Fehlers**
</dt> <dd> <dl> <dt>

1322 (0x52A)
</dt> <dt>



Dieser Vorgang ist unzulässig, da dies dazu führen könnte, dass ein Verwaltungskonto deaktiviert, gelöscht oder nicht mehr angemeldet werden kann.


</dt> </dl> </dd> <dt>

<span id="ERROR_WRONG_PASSWORD"></span><span id="error_wrong_password"></span>**\_falsches \_ Kennwort für Fehler**
</dt> <dd> <dl> <dt>

1323 (0x52B)
</dt> <dt>



Das Kennwort kann nicht aktualisiert werden. Der als Aktuelles Kennwort angegebene Wert ist falsch.


</dt> </dl> </dd> <dt>

<span id="ERROR_ILL_FORMED_PASSWORD"></span><span id="error_ill_formed_password"></span>**Fehler \_ Haft \_ geformtes \_ Kennwort**
</dt> <dd> <dl> <dt>

1324 (0x52C)
</dt> <dt>



Das Kennwort kann nicht aktualisiert werden. Der für das neue Kennwort angegebene Wert enthält Werte, die in Kenn Wörtern nicht zulässig sind.


</dt> </dl> </dd> <dt>

<span id="ERROR_PASSWORD_RESTRICTION"></span><span id="error_password_restriction"></span>**Einschränkung des Fehler \_ Kennworts \_**
</dt> <dd> <dl> <dt>

1325 (0x52d)
</dt> <dt>



Das Kennwort kann nicht aktualisiert werden. Der für das neue Kennwort angegebene Wert entspricht nicht den Anforderungen für die Länge, Komplexität oder den Verlauf der Domäne.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOGON_FAILURE"></span><span id="error_logon_failure"></span>**Fehler beim \_ anmelden. \_**
</dt> <dd> <dl> <dt>

1326 (0x52E)
</dt> <dt>



Der Benutzername oder das Kennwort ist falsch.


</dt> </dl> </dd> <dt>

<span id="ERROR_ACCOUNT_RESTRICTION"></span><span id="error_account_restriction"></span>**Einschränkung des Fehler \_ Kontos \_**
</dt> <dd> <dl> <dt>

1327 (0x52F)
</dt> <dt>



Konto Einschränkungen verhindern, dass dieser Benutzer sich anmeldet. Beispiel: leere Kenn Wörter sind nicht zulässig, Anmeldezeiten sind beschränkt, oder es wurde eine Richtlinien Einschränkung erzwungen.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_LOGON_HOURS"></span><span id="error_invalid_logon_hours"></span>**Fehler \_ ungültige \_ Anmelde \_ Zeiten.**
</dt> <dd> <dl> <dt>

1328 (0x530)
</dt> <dt>



Ihr Konto verfügt über Zeitbeschränkungen, mit denen Sie sich momentan nicht anmelden.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_WORKSTATION"></span><span id="error_invalid_workstation"></span>**Fehler \_ ungültige \_ Arbeitsstation**
</dt> <dd> <dl> <dt>

1329 (0x531)
</dt> <dt>



Dieser Benutzer darf sich nicht bei diesem Computer anmelden.


</dt> </dl> </dd> <dt>

<span id="ERROR_PASSWORD_EXPIRED"></span><span id="error_password_expired"></span>**Fehler \_ Kennwort \_ abgelaufen**
</dt> <dd> <dl> <dt>

1330 (0x532)
</dt> <dt>



Das Kennwort für dieses Konto ist abgelaufen.


</dt> </dl> </dd> <dt>

<span id="ERROR_ACCOUNT_DISABLED"></span><span id="error_account_disabled"></span>**Fehler \_ Konto \_ deaktiviert**
</dt> <dd> <dl> <dt>

1331 (0x533)
</dt> <dt>



Dieser Benutzer kann sich nicht anmelden, da dieses Konto zurzeit deaktiviert ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_NONE_MAPPED"></span><span id="error_none_mapped"></span>**Fehler " \_ keine \_ zugeordnet"**
</dt> <dd> <dl> <dt>

1332 (0x534)
</dt> <dt>



Es wurde keine Zuordnung zwischen den Kontonamen und den Sicherheits-IDs vorgenommen.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_LUIDS_REQUESTED"></span><span id="error_too_many_luids_requested"></span>**Fehler \_ zu \_ viele \_ LUIDs \_ angefordert.**
</dt> <dd> <dl> <dt>

1333 (0x535)
</dt> <dt>



Es wurden zu viele lokale Benutzer-IDs (LUIDs) gleichzeitig angefordert.


</dt> </dl> </dd> <dt>

<span id="ERROR_LUIDS_EXHAUSTED"></span><span id="error_luids_exhausted"></span>**Fehler- \_ LUIDs \_ aufgebraucht**
</dt> <dd> <dl> <dt>

1334 (0x536)
</dt> <dt>



Es sind keine weiteren lokalen Benutzer-IDs (LUIDs) verfügbar.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SUB_AUTHORITY"></span><span id="error_invalid_sub_authority"></span>**Fehler \_ ungültige \_ untergeordnete \_ Autorität.**
</dt> <dd> <dl> <dt>

1335 (0x537)
</dt> <dt>



Der Teil der untergeordneten Instanz einer Sicherheits-ID ist für diese bestimmte Verwendung ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_ACL"></span><span id="error_invalid_acl"></span>**\_ungültige \_ ACL.**
</dt> <dd> <dl> <dt>

1336 (0x538)
</dt> <dt>



Die Struktur der Zugriffs Steuerungs Liste (ACL) ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SID"></span><span id="error_invalid_sid"></span>**Fehler \_ ungültige \_ SID.**
</dt> <dd> <dl> <dt>

1337 (0x539)
</dt> <dt>



Die Struktur der Sicherheits-ID ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SECURITY_DESCR"></span><span id="error_invalid_security_descr"></span>**Fehler \_ ungültige \_ Sicherheits- \_ descr**
</dt> <dd> <dl> <dt>

1338 (0x53A)
</dt> <dt>



Die Sicherheits deskriptorstruktur ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_INHERITANCE_ACL"></span><span id="error_bad_inheritance_acl"></span>**fehlerhafter \_ \_ Vererbungs- \_ ACL**
</dt> <dd> <dl> <dt>

1340 (0x53c)
</dt> <dt>



Die geerbte Zugriffs Steuerungs Liste (Access Control List, ACL) oder der Zugriffs Steuerungs Eintrag (ACE) konnte nicht erstellt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVER_DISABLED"></span><span id="error_server_disabled"></span>**Fehler \_ Server \_ deaktiviert**
</dt> <dd> <dl> <dt>

1341 (0x53D)
</dt> <dt>



Der Server ist zurzeit deaktiviert.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVER_NOT_DISABLED"></span><span id="error_server_not_disabled"></span>**Fehler \_ Server \_ nicht \_ deaktiviert**
</dt> <dd> <dl> <dt>

1342 (0x53E)
</dt> <dt>



Der Server ist zurzeit aktiviert.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_ID_AUTHORITY"></span><span id="error_invalid_id_authority"></span>**\_ungültige \_ ID- \_ Autorität.**
</dt> <dd> <dl> <dt>

1343 (0x53F)
</dt> <dt>



Der angegebene Wert war ein ungültiger Wert für eine bezeichnerzertifizierungs Stelle.


</dt> </dl> </dd> <dt>

<span id="ERROR_ALLOTTED_SPACE_EXCEEDED"></span><span id="error_allotted_space_exceeded"></span>**nicht \_ zugewiesener \_ Speicherplatz \_ überschritten**
</dt> <dd> <dl> <dt>

1344 (0x540)
</dt> <dt>



Für Aktualisierungen der Sicherheitsinformationen ist kein Arbeitsspeicher mehr verfügbar.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_GROUP_ATTRIBUTES"></span><span id="error_invalid_group_attributes"></span>**Fehler bei \_ ungültigen \_ Gruppen \_ Attributen.**
</dt> <dd> <dl> <dt>

1345 (0x541)
</dt> <dt>



Die angegebenen Attribute sind ungültig oder nicht kompatibel mit den Attributen für die Gruppe als Ganzes.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_IMPERSONATION_LEVEL"></span><span id="error_bad_impersonation_level"></span>**fehlerhafte Identitätswechsel \_ \_ \_ Ebene**
</dt> <dd> <dl> <dt>

1346 (0x542)
</dt> <dt>



Entweder wurde eine geforderte Identitätswechselebene nicht geliefert, oder die gelieferte Identitätswechselebene ist unzulässig.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_OPEN_ANONYMOUS"></span><span id="error_cant_open_anonymous"></span>**Fehler \_ beim \_ Öffnen von \_ anonym.**
</dt> <dd> <dl> <dt>

1347 (0x543)
</dt> <dt>



Ein Sicherheits Token der anonymen Ebene kann nicht geöffnet werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_VALIDATION_CLASS"></span><span id="error_bad_validation_class"></span>**Fehler \_ hafte \_ Validierungs \_ Klasse**
</dt> <dd> <dl> <dt>

1348 (0x544)
</dt> <dt>



Die angeforderte Validierungs Informations Klasse war ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_TOKEN_TYPE"></span><span id="error_bad_token_type"></span>**fehlerhafter \_ \_ \_ Tokentyp**
</dt> <dd> <dl> <dt>

1349 (0x545)
</dt> <dt>



Der Tokentyp ist für die versuchte Verwendung ungeeignet.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SECURITY_ON_OBJECT"></span><span id="error_no_security_on_object"></span>**Fehler \_ \_ \_ bei der Sicherheit des \_ Objekts.**
</dt> <dd> <dl> <dt>

1350 (0x546)
</dt> <dt>



Ein Sicherheits Vorgang für ein Objekt ohne zugeordnete Sicherheit kann nicht ausgeführt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_ACCESS_DOMAIN_INFO"></span><span id="error_cant_access_domain_info"></span>**Fehler \_ beim \_ Zugriff auf \_ Domänen \_ Informationen.**
</dt> <dd> <dl> <dt>

1351 (0x547)
</dt> <dt>



Die Konfigurationsinformationen konnten nicht vom Domänen Controller gelesen werden, weil der Computer nicht verfügbar ist oder der Zugriff verweigert wurde.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SERVER_STATE"></span><span id="error_invalid_server_state"></span>**Fehler \_ ungültiger \_ Server \_ Status**
</dt> <dd> <dl> <dt>

1352 (0x548)
</dt> <dt>



Der Sicherheits Konto-Manager (Sam) oder der lokale Sicherheits Autorität (Local Security Authority, LSA) befand sich im falschen Zustand, um den Sicherheits Vorgang auszuführen.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_DOMAIN_STATE"></span><span id="error_invalid_domain_state"></span>**\_ungültiger \_ Domänen \_ Status**
</dt> <dd> <dl> <dt>

1353 (0x549)
</dt> <dt>



Die Domäne befand sich im falschen Zustand, um den Sicherheits Vorgang auszuführen.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_DOMAIN_ROLE"></span><span id="error_invalid_domain_role"></span>**\_ungültige \_ Domänen \_ Rolle.**
</dt> <dd> <dl> <dt>

1354 (0x54A)
</dt> <dt>



Dieser Vorgang ist nur für den primären Domänen Controller der Domäne zulässig.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SUCH_DOMAIN"></span><span id="error_no_such_domain"></span>**Fehler bei \_ keiner \_ solchen \_ Domäne**
</dt> <dd> <dl> <dt>

1355 (0x54b)
</dt> <dt>



Die angegebene Domäne ist entweder nicht vorhanden, oder es konnte keine Verbindung mit ihr hergestellt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DOMAIN_EXISTS"></span><span id="error_domain_exists"></span>**Fehler \_ Domäne \_ vorhanden**
</dt> <dd> <dl> <dt>

1356 (0x54C)
</dt> <dt>



Die angegebene Domäne ist bereits vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DOMAIN_LIMIT_EXCEEDED"></span><span id="error_domain_limit_exceeded"></span>**Fehler \_ Domänen \_ Limit \_ überschritten**
</dt> <dd> <dl> <dt>

1357 (0x54d)
</dt> <dt>



Es wurde versucht, den Grenzwert für die Anzahl von Domänen pro Server zu überschreiten.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNAL_DB_CORRUPTION"></span><span id="error_internal_db_corruption"></span>**Fehler bei \_ interner \_ DB- \_ Datenbank.**
</dt> <dd> <dl> <dt>

1358 (0x54e)
</dt> <dt>



Der angeforderte Vorgang kann aufgrund eines schwerwiegenden Medien Fehlers oder einer Beschädigung der Datenstruktur auf dem Datenträger nicht durchgeführt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNAL_ERROR"></span><span id="error_internal_error"></span>**\_Interner Fehler \_**
</dt> <dd> <dl> <dt>

1359 (0x54f)
</dt> <dt>



Interner Fehler.


</dt> </dl> </dd> <dt>

<span id="ERROR_GENERIC_NOT_MAPPED"></span><span id="error_generic_not_mapped"></span>**Fehler \_ generisch \_ nicht \_ zugeordnet**
</dt> <dd> <dl> <dt>

1360 (0x550)
</dt> <dt>



Generische Zugriffs Typen waren in einer Zugriffs Maske enthalten, die bereits nicht generischen Typen zugeordnet werden sollte.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_DESCRIPTOR_FORMAT"></span><span id="error_bad_descriptor_format"></span>**fehlerhaftes \_ \_ \_ deskriptorformat**
</dt> <dd> <dl> <dt>

1361 (0x551)
</dt> <dt>



Eine Sicherheits Beschreibung weist nicht das richtige Format auf (absolut oder selbst bezogen).


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_LOGON_PROCESS"></span><span id="error_not_logon_process"></span>**Fehler \_ beim \_ Anmelde \_ Vorgang.**
</dt> <dd> <dl> <dt>

1362 (0x552)
</dt> <dt>



Die angeforderte Aktion ist nur für die Verwendung durch Anmelde Prozesse eingeschränkt. Der aufrufende Prozess ist nicht als Anmeldevorgang registriert.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOGON_SESSION_EXISTS"></span><span id="error_logon_session_exists"></span>**Fehler \_ Anmelde \_ Sitzung ist \_ vorhanden.**
</dt> <dd> <dl> <dt>

1363 (0x553)
</dt> <dt>



Es kann keine neue Anmelde Sitzung mit einer bereits verwendeten ID gestartet werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SUCH_PACKAGE"></span><span id="error_no_such_package"></span>**Fehler " \_ kein \_ solches \_ Paket"**
</dt> <dd> <dl> <dt>

1364 (0x554)
</dt> <dt>



Ein angegebenes Authentifizierungs Paket ist unbekannt.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_LOGON_SESSION_STATE"></span><span id="error_bad_logon_session_state"></span>**Fehler bei fehlerhafter \_ \_ Anmelde \_ Sitzung \_ .**
</dt> <dd> <dl> <dt>

1365 (0x555)
</dt> <dt>



Die Anmelde Sitzung befindet sich nicht in einem Zustand, der mit dem angeforderten Vorgang konsistent ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOGON_SESSION_COLLISION"></span><span id="error_logon_session_collision"></span>**Fehler beim \_ Protokollierung der \_ Sitzung. \_**
</dt> <dd> <dl> <dt>

1366 (0x556)
</dt> <dt>



Die Anmelde Sitzungs-ID wird bereits verwendet.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_LOGON_TYPE"></span><span id="error_invalid_logon_type"></span>**\_ungültiger \_ \_ Anmeldetyp.**
</dt> <dd> <dl> <dt>

1367 (0x557)
</dt> <dt>



Eine Anmelde Anforderung enthielt einen ungültigen anmeldetypwert.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_IMPERSONATE"></span><span id="error_cannot_impersonate"></span>**Fehler beim Annehmen der Identität \_ \_**
</dt> <dd> <dl> <dt>

1368 (0x558)
</dt> <dt>



Die Identität kann nicht mithilfe einer Named Pipe angenommen werden, bis die Daten aus dieser Pipe gelesen wurden.


</dt> </dl> </dd> <dt>

<span id="ERROR_RXACT_INVALID_STATE"></span><span id="error_rxact_invalid_state"></span>**Fehler " \_ rxact" ist \_ ungültig. \_**
</dt> <dd> <dl> <dt>

1369 (0x559)
</dt> <dt>



Der Transaktionsstatus einer Registrierungs Unterstruktur ist mit dem angeforderten Vorgang nicht kompatibel.


</dt> </dl> </dd> <dt>

<span id="ERROR_RXACT_COMMIT_FAILURE"></span><span id="error_rxact_commit_failure"></span>**Fehler beim \_ rxact- \_ Commit. \_**
</dt> <dd> <dl> <dt>

1370 (0x55a)
</dt> <dt>



Es ist eine interne Beschädigung der Sicherheitsdatenbank aufgetreten.


</dt> </dl> </dd> <dt>

<span id="ERROR_SPECIAL_ACCOUNT"></span><span id="error_special_account"></span>**\_Sonderkonto für Fehler \_**
</dt> <dd> <dl> <dt>

1371 (0x55b)
</dt> <dt>



Dieser Vorgang kann nicht für integrierte Konten durchgeführt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_SPECIAL_GROUP"></span><span id="error_special_group"></span>**Fehler \_ spezielle \_ Gruppe**
</dt> <dd> <dl> <dt>

1372 (0x55c)
</dt> <dt>



Dieser Vorgang kann für diese integrierte spezielle Gruppe nicht durchgeführt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_SPECIAL_USER"></span><span id="error_special_user"></span>**\_spezieller Fehler \_ Benutzer**
</dt> <dd> <dl> <dt>

1373 (0x55D)
</dt> <dt>



Dieser Vorgang kann für diesen integrierten speziellen Benutzer nicht durchgeführt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_MEMBERS_PRIMARY_GROUP"></span><span id="error_members_primary_group"></span>**Fehler \_ Mitglieder \_ primäre \_ Gruppe**
</dt> <dd> <dl> <dt>

1374 (0x55E)
</dt> <dt>



Der Benutzer kann nicht aus einer Gruppe entfernt werden, da es sich bei der Gruppe derzeit um die primäre Gruppe des Benutzers handelt.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOKEN_ALREADY_IN_USE"></span><span id="error_token_already_in_use"></span>**das Fehler \_ Token wird \_ bereits \_ \_ verwendet.**
</dt> <dd> <dl> <dt>

1375 (0x55f)
</dt> <dt>



Das Token wird bereits als primäres Token verwendet.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SUCH_ALIAS"></span><span id="error_no_such_alias"></span>**Fehler " \_ kein \_ solcher \_ Alias"**
</dt> <dd> <dl> <dt>

1376 (0x560)
</dt> <dt>



Die angegebene lokale Gruppe ist nicht vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_MEMBER_NOT_IN_ALIAS"></span><span id="error_member_not_in_alias"></span>**\_fehlermember \_ nicht \_ im \_ Alias**
</dt> <dd> <dl> <dt>

1377 (0x561)
</dt> <dt>



Der angegebene Kontoname ist kein Mitglied der Gruppe.


</dt> </dl> </dd> <dt>

<span id="ERROR_MEMBER_IN_ALIAS"></span><span id="error_member_in_alias"></span>**\_fehlermember \_ in \_ Alias**
</dt> <dd> <dl> <dt>

1378 (0x562)
</dt> <dt>



Der angegebene Kontoname ist bereits Mitglied der Gruppe.


</dt> </dl> </dd> <dt>

<span id="ERROR_ALIAS_EXISTS"></span><span id="error_alias_exists"></span>**\_fehleralias \_ vorhanden**
</dt> <dd> <dl> <dt>

1379 (0x563)
</dt> <dt>



Die angegebene lokale Gruppe ist bereits vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOGON_NOT_GRANTED"></span><span id="error_logon_not_granted"></span>**Fehler \_ Anmeldung \_ nicht \_ erteilt**
</dt> <dd> <dl> <dt>

1380 (0x564)
</dt> <dt>



Anmeldefehler: dem Benutzer wurde der angeforderte Anmeldetyp auf diesem Computer nicht erteilt.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_SECRETS"></span><span id="error_too_many_secrets"></span>**Fehler bei \_ zu \_ vielen \_ geheimen Schlüsseln.**
</dt> <dd> <dl> <dt>

1381 (0x565)
</dt> <dt>



Die maximale Anzahl von Geheimnissen, die in einem einzelnen System gespeichert werden können, wurde überschritten.


</dt> </dl> </dd> <dt>

<span id="ERROR_SECRET_TOO_LONG"></span><span id="error_secret_too_long"></span>**Fehler \_ Geheimnis \_ zu \_ lang**
</dt> <dd> <dl> <dt>

1382 (0x566)
</dt> <dt>



Die Länge eines geheimen Schlüssels überschreitet die maximal zulässige Länge.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNAL_DB_ERROR"></span><span id="error_internal_db_error"></span>**Fehler \_ interner \_ DB- \_ Fehler.**
</dt> <dd> <dl> <dt>

1383 (0x567)
</dt> <dt>



Die Datenbank der lokalen Sicherheits Autorität enthält interne Inkonsistenzen.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_CONTEXT_IDS"></span><span id="error_too_many_context_ids"></span>**Fehler \_ zu \_ viele \_ Kontext- \_ IDs.**
</dt> <dd> <dl> <dt>

1384 (0x568)
</dt> <dt>



Während eines Anmelde Versuchs hat der Sicherheitskontext des Benutzers zu viele Sicherheits-IDs gesammelt.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOGON_TYPE_NOT_GRANTED"></span><span id="error_logon_type_not_granted"></span>**Fehler \_ \_ Anmeldetyp \_ nicht \_ erteilt**
</dt> <dd> <dl> <dt>

1385 (0x569)
</dt> <dt>



Anmeldefehler: dem Benutzer wurde der angeforderte Anmeldetyp auf diesem Computer nicht erteilt.


</dt> </dl> </dd> <dt>

<span id="ERROR_NT_CROSS_ENCRYPTION_REQUIRED"></span><span id="error_nt_cross_encryption_required"></span>**Fehler bei \_ NT- \_ Kreuz \_ Verschlüsselung \_ erforderlich**
</dt> <dd> <dl> <dt>

1386 (0x56A)
</dt> <dt>



Ein Kreuz verschlüsseltes Kennwort ist erforderlich, um ein Benutzer Kennwort zu ändern.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SUCH_MEMBER"></span><span id="error_no_such_member"></span>**Fehler " \_ kein \_ solcher \_ Member"**
</dt> <dd> <dl> <dt>

1387 (0x56B)
</dt> <dt>



Ein Mitglied konnte der lokalen Gruppe nicht hinzugefügt oder daraus entfernt werden, da das Element nicht vorhanden ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_MEMBER"></span><span id="error_invalid_member"></span>**\_ungültiger \_ Member**
</dt> <dd> <dl> <dt>

1388 (0x56C)
</dt> <dt>



Ein neuer Member konnte einer lokalen Gruppe nicht hinzugefügt werden, weil der Member den falschen Kontotyp aufweist.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_SIDS"></span><span id="error_too_many_sids"></span>**Fehler \_ zu \_ viele \_ SIDs.**
</dt> <dd> <dl> <dt>

1389 (0x56D)
</dt> <dt>



Es wurden zu viele Sicherheits-IDs angegeben.


</dt> </dl> </dd> <dt>

<span id="ERROR_LM_CROSS_ENCRYPTION_REQUIRED"></span><span id="error_lm_cross_encryption_required"></span>**Fehler \_ LM- \_ Kreuz \_ Verschlüsselung \_ erforderlich**
</dt> <dd> <dl> <dt>

1390 (0x56E)
</dt> <dt>



Ein Kreuz verschlüsseltes Kennwort ist erforderlich, um dieses Benutzer Kennwort zu ändern.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_INHERITANCE"></span><span id="error_no_inheritance"></span>**Fehler \_ keine \_ Vererbung**
</dt> <dd> <dl> <dt>

1391 (0x56f)
</dt> <dt>



Gibt an, dass eine ACL keine vererbbaren Komponenten enthält.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_CORRUPT"></span><span id="error_file_corrupt"></span>**Fehler \_ Datei \_ beschädigt**
</dt> <dd> <dl> <dt>

1392 (0x570)
</dt> <dt>



Die Datei oder das Verzeichnis ist beschädigt und kann nicht gelesen werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DISK_CORRUPT"></span><span id="error_disk_corrupt"></span>**Fehler Datenträger \_ \_ beschädigt**
</dt> <dd> <dl> <dt>

1393 (0x571)
</dt> <dt>



Die Datenträger Struktur ist beschädigt und kann nicht gelesen werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_USER_SESSION_KEY"></span><span id="error_no_user_session_key"></span>**Fehler " \_ kein \_ Benutzer \_ Sitzungs \_ Schlüssel"**
</dt> <dd> <dl> <dt>

1394 (0x572)
</dt> <dt>



Es ist kein Benutzer Sitzungsschlüssel für die angegebene Anmelde Sitzung vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_LICENSE_QUOTA_EXCEEDED"></span><span id="error_license_quota_exceeded"></span>**Fehler \_ Lizenz \_ Kontingent \_ überschritten**
</dt> <dd> <dl> <dt>

1395 (0x573)
</dt> <dt>



Der Dienst, auf den zugegriffen wird, ist für eine bestimmte Anzahl von Verbindungen lizenziert. Zurzeit können keine weiteren Verbindungen mit dem Dienst hergestellt werden, da bereits so viele Verbindungen vorhanden sind, wie der Dienst annehmen kann.


</dt> </dl> </dd> <dt>

<span id="ERROR_WRONG_TARGET_NAME"></span><span id="error_wrong_target_name"></span>**\_falscher \_ \_ Zielname für Fehler**
</dt> <dd> <dl> <dt>

1396 (0x574)
</dt> <dt>



Der Name des Ziel Kontos ist falsch.


</dt> </dl> </dd> <dt>

<span id="ERROR_MUTUAL_AUTH_FAILED"></span><span id="error_mutual_auth_failed"></span>**Fehler bei \_ gegenseitiger Authentifizierung \_ . \_**
</dt> <dd> <dl> <dt>

1397 (0x575)
</dt> <dt>



Gegenseitige Authentifizierung ist fehlgeschlagen. Das Server Kennwort ist auf dem Domänen Controller veraltet.


</dt> </dl> </dd> <dt>

<span id="ERROR_TIME_SKEW"></span><span id="error_time_skew"></span>**Fehler \_ Zeit \_ Abweichung**
</dt> <dd> <dl> <dt>

1398 (0x576)
</dt> <dt>



Zwischen dem Client und dem Server liegt ein Zeit-und/oder Datums Unterschied vor.


</dt> </dl> </dd> <dt>

<span id="ERROR_CURRENT_DOMAIN_NOT_ALLOWED"></span><span id="error_current_domain_not_allowed"></span>**Fehler die \_ aktuelle \_ Domäne ist \_ nicht \_ zulässig.**
</dt> <dd> <dl> <dt>

1399 (0x577)
</dt> <dt>



Dieser Vorgang kann für die aktuelle Domäne nicht ausgeführt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_WINDOW_HANDLE"></span><span id="error_invalid_window_handle"></span>**Fehler bei \_ ungültigem \_ Fenster \_ handle.**
</dt> <dd> <dl> <dt>

1400 (0x578)
</dt> <dt>



Ungültiges Fenster handle.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_MENU_HANDLE"></span><span id="error_invalid_menu_handle"></span>**Fehler bei \_ ungültigem \_ Menü \_ handle.**
</dt> <dd> <dl> <dt>

1401 (0x579)
</dt> <dt>



Ungültiges Menü handle.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_CURSOR_HANDLE"></span><span id="error_invalid_cursor_handle"></span>**Fehler bei \_ ungültigem \_ Cursor \_ handle.**
</dt> <dd> <dl> <dt>

1402 (0x57A)
</dt> <dt>



Ungültiges Cursor handle.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_ACCEL_HANDLE"></span><span id="error_invalid_accel_handle"></span>**\_ungültiger \_ Accel- \_ handle.**
</dt> <dd> <dl> <dt>

1403 (0x57B)
</dt> <dt>



Ungültiges Zugriffstasten-Tabellen handle.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_HOOK_HANDLE"></span><span id="error_invalid_hook_handle"></span>**Fehler \_ ungültiges \_ Hook- \_ handle.**
</dt> <dd> <dl> <dt>

1404 (0x57c)
</dt> <dt>



Ungültiges Hook-handle.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_DWP_HANDLE"></span><span id="error_invalid_dwp_handle"></span>**\_ungültiger \_ DWP- \_ handle.**
</dt> <dd> <dl> <dt>

1405 (0x57D)
</dt> <dt>



Ungültiges Handle für eine Positions Struktur mit mehreren Fenstern.


</dt> </dl> </dd> <dt>

<span id="ERROR_TLW_WITH_WSCHILD"></span><span id="error_tlw_with_wschild"></span>**Fehler- \_ TLW \_ mit \_ wschild**
</dt> <dd> <dl> <dt>

1406 (0x57e)
</dt> <dt>



Ein untergeordnetes Fenster der obersten Ebene kann nicht erstellt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_FIND_WND_CLASS"></span><span id="error_cannot_find_wnd_class"></span>**Fehler \_ beim \_ Suchen der \_ WND- \_ Klasse.**
</dt> <dd> <dl> <dt>

1407 (0x57f)
</dt> <dt>



Die Fenster Klasse kann nicht gefunden werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINDOW_OF_OTHER_THREAD"></span><span id="error_window_of_other_thread"></span>**Fehler \_ Fenster \_ des \_ anderen \_ Threads**
</dt> <dd> <dl> <dt>

1408 (0x580)
</dt> <dt>



Ungültiges Fenster Sie gehört zu einem anderen Thread.


</dt> </dl> </dd> <dt>

<span id="ERROR_HOTKEY_ALREADY_REGISTERED"></span><span id="error_hotkey_already_registered"></span>**Fehler \_ Hotkey \_ bereits \_ registriert**
</dt> <dd> <dl> <dt>

1409 (0x581)
</dt> <dt>



Die Hot-Taste ist bereits registriert.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLASS_ALREADY_EXISTS"></span><span id="error_class_already_exists"></span>**die Fehler \_ Klasse ist \_ bereits \_ vorhanden.**
</dt> <dd> <dl> <dt>

1410 (0x582)
</dt> <dt>



Die Klasse ist bereits vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLASS_DOES_NOT_EXIST"></span><span id="error_class_does_not_exist"></span>**die Fehler \_ Klasse \_ ist \_ nicht \_ vorhanden.**
</dt> <dd> <dl> <dt>

1411 (0x583)
</dt> <dt>



Die Klasse ist nicht vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLASS_HAS_WINDOWS"></span><span id="error_class_has_windows"></span>**Error- \_ Klasse \_ hat \_ Windows**
</dt> <dd> <dl> <dt>

1412 (0x584)
</dt> <dt>



Die Klasse hat weiterhin geöffnete Fenster.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_INDEX"></span><span id="error_invalid_index"></span>**\_ungültiger \_ Index**
</dt> <dd> <dl> <dt>

1413 (0x585)
</dt> <dt>



Ungültiger Index.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_ICON_HANDLE"></span><span id="error_invalid_icon_handle"></span>**Fehler bei \_ ungültigem \_ Symbol \_ handle.**
</dt> <dd> <dl> <dt>

1414 (0x586)
</dt> <dt>



Ungültiges Symbol handle.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRIVATE_DIALOG_INDEX"></span><span id="error_private_dialog_index"></span>**Fehler beim \_ privaten \_ Dialog Feld \_ Index**
</dt> <dd> <dl> <dt>

1415 (0x587)
</dt> <dt>



Verwenden von privaten Dialog Feld Fenster Wörtern.


</dt> </dl> </dd> <dt>

<span id="ERROR_LISTBOX_ID_NOT_FOUND"></span><span id="error_listbox_id_not_found"></span>**Fehler \_ ListBox- \_ ID wurde \_ nicht \_ gefunden.**
</dt> <dd> <dl> <dt>

1416 (0x588)
</dt> <dt>



Der Listenfeld Bezeichner wurde nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_WILDCARD_CHARACTERS"></span><span id="error_no_wildcard_characters"></span>**Fehler \_ keine Platzhalter \_ \_ Zeichen**
</dt> <dd> <dl> <dt>

1417 (0x589)
</dt> <dt>



Es wurden keine Platzhalter gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLIPBOARD_NOT_OPEN"></span><span id="error_clipboard_not_open"></span>**Fehler \_ Zwischenablage \_ nicht \_ geöffnet**
</dt> <dd> <dl> <dt>

1418 (0x58a)
</dt> <dt>



Für den Thread ist keine Zwischenablage geöffnet.


</dt> </dl> </dd> <dt>

<span id="ERROR_HOTKEY_NOT_REGISTERED"></span><span id="error_hotkey_not_registered"></span>**Fehler \_ Hotkey \_ nicht \_ registriert**
</dt> <dd> <dl> <dt>

1419 (0x58b)
</dt> <dt>



Die Hot-Taste ist nicht registriert.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINDOW_NOT_DIALOG"></span><span id="error_window_not_dialog"></span>**Fehler \_ Fenster \_ nicht \_ Dialogfeld**
</dt> <dd> <dl> <dt>

1420 (0x58c)
</dt> <dt>



Das Fenster ist kein gültiges Dialogfeld Fenster.


</dt> </dl> </dd> <dt>

<span id="ERROR_CONTROL_ID_NOT_FOUND"></span><span id="error_control_id_not_found"></span>**Fehler \_ Steuerungs- \_ ID wurde \_ nicht \_ gefunden.**
</dt> <dd> <dl> <dt>

1421 (0x58d)
</dt> <dt>



Die Kontroll-ID wurde nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_COMBOBOX_MESSAGE"></span><span id="error_invalid_combobox_message"></span>**Fehler \_ ungültige \_ ComboBox- \_ Nachricht.**
</dt> <dd> <dl> <dt>

1422 (0x58e)
</dt> <dt>



Ungültige Meldung für ein Kombinations Feld, weil Sie nicht über ein Bearbeitungs Steuerelement verfügt.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINDOW_NOT_COMBOBOX"></span><span id="error_window_not_combobox"></span>**Fehler \_ Fenster \_ nicht \_ ComboBox**
</dt> <dd> <dl> <dt>

1423 (0x58f)
</dt> <dt>



Das Fenster ist kein Kombinations Feld.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_EDIT_HEIGHT"></span><span id="error_invalid_edit_height"></span>**Fehler \_ beim \_ Bearbeiten der \_ Höhe.**
</dt> <dd> <dl> <dt>

1424 (0x590)
</dt> <dt>



Die Höhe muss kleiner als 256 sein.


</dt> </dl> </dd> <dt>

<span id="ERROR_DC_NOT_FOUND"></span><span id="error_dc_not_found"></span>**Fehler Domänen Controller \_ \_ nicht \_ gefunden**
</dt> <dd> <dl> <dt>

1425 (0x591)
</dt> <dt>



Ungültiges Handle des Geräte Kontexts (DC).


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_HOOK_FILTER"></span><span id="error_invalid_hook_filter"></span>**\_ungültiger \_ Hook- \_ Filter**
</dt> <dd> <dl> <dt>

1426 (0x592)
</dt> <dt>



Ungültiger Hook-Prozedurtyp.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_FILTER_PROC"></span><span id="error_invalid_filter_proc"></span>**Fehler \_ ungültige Filter Prozedur. \_ \_**
</dt> <dd> <dl> <dt>

1427 (0x593)
</dt> <dt>



Ungültige Hook-Prozedur.


</dt> </dl> </dd> <dt>

<span id="ERROR_HOOK_NEEDS_HMOD"></span><span id="error_hook_needs_hmod"></span>**der Fehler \_ Hook \_ benötigt \_ hMod.**
</dt> <dd> <dl> <dt>

1428 (0x594)
</dt> <dt>



Der nicht lokale Hook kann nicht ohne ein Modul handle festgelegt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_GLOBAL_ONLY_HOOK"></span><span id="error_global_only_hook"></span>**Fehler beim globalen reinen Fehler \_ \_ \_**
</dt> <dd> <dl> <dt>

1429 (0x595)
</dt> <dt>



Diese Hook-Prozedur kann nur global festgelegt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_JOURNAL_HOOK_SET"></span><span id="error_journal_hook_set"></span>**Fehler \_ Journal- \_ Hook- \_ Satz**
</dt> <dd> <dl> <dt>

1430 (0x596)
</dt> <dt>



Die Journal Hook-Prozedur ist bereits installiert.


</dt> </dl> </dd> <dt>

<span id="ERROR_HOOK_NOT_INSTALLED"></span><span id="error_hook_not_installed"></span>**Fehler \_ Hook \_ nicht \_ installiert**
</dt> <dd> <dl> <dt>

1431 (0x597)
</dt> <dt>



Die Hook-Prozedur ist nicht installiert.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_LB_MESSAGE"></span><span id="error_invalid_lb_message"></span>**Fehler \_ ungültige \_ lb- \_ Nachricht.**
</dt> <dd> <dl> <dt>

1432 (0x598)
</dt> <dt>



Ungültige Meldung für das Listenfeld für die Einzel Auswahl.


</dt> </dl> </dd> <dt>

<span id="ERROR_SETCOUNT_ON_BAD_LB"></span><span id="error_setcount_on_bad_lb"></span>**Fehler \_ bei SetCount bei fehlerhafter \_ \_ \_ lb**
</dt> <dd> <dl> <dt>

1433 (0x599)
</dt> <dt>



\_Die an das nicht verzögerte Listenfeld gesendete lb-SetCount.


</dt> </dl> </dd> <dt>

<span id="ERROR_LB_WITHOUT_TABSTOPS"></span><span id="error_lb_without_tabstops"></span>**Fehler- \_ lb \_ ohne \_ Tabstopps**
</dt> <dd> <dl> <dt>

1434 (0x59a)
</dt> <dt>



Dieses Listenfeld unterstützt keine Tabstopps.


</dt> </dl> </dd> <dt>

<span id="ERROR_DESTROY_OBJECT_OF_OTHER_THREAD"></span><span id="error_destroy_object_of_other_thread"></span>**Fehler \_ beim \_ zerstören \_ des Objekts eines \_ anderen \_ Threads.**
</dt> <dd> <dl> <dt>

1435 (0x59b)
</dt> <dt>



Das von einem anderen Thread erstellte Objekt kann nicht zerstört werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_CHILD_WINDOW_MENU"></span><span id="error_child_window_menu"></span>**Menü "Fehler untergeordneter \_ \_ Fenster" \_**
</dt> <dd> <dl> <dt>

1436 (0x59c)
</dt> <dt>



Untergeordnete Fenster dürfen keine Menüs enthalten.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SYSTEM_MENU"></span><span id="error_no_system_menu"></span>**Fehler " \_ kein \_ System" \_**
</dt> <dd> <dl> <dt>

1437 (0x59d)
</dt> <dt>



Das Fenster verfügt über kein Systemmenü.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_MSGBOX_STYLE"></span><span id="error_invalid_msgbox_style"></span>**\_ungültiger \_ MsgBox- \_ Stil.**
</dt> <dd> <dl> <dt>

1438 (0x59e)
</dt> <dt>



Ungültiger Stil für Meldungs Feld.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SPI_VALUE"></span><span id="error_invalid_spi_value"></span>**\_ungültiger \_ SPI- \_ Wert**
</dt> <dd> <dl> <dt>

1439 (0x59f)
</dt> <dt>



Ungültiger systemweite (SPI \_ \* )-Parameter.


</dt> </dl> </dd> <dt>

<span id="ERROR_SCREEN_ALREADY_LOCKED"></span><span id="error_screen_already_locked"></span>**der Fehler \_ Bildschirm ist \_ bereits \_ gesperrt.**
</dt> <dd> <dl> <dt>

1440 (0x5a0)
</dt> <dt>



Der Bildschirm ist bereits gesperrt.


</dt> </dl> </dd> <dt>

<span id="ERROR_HWNDS_HAVE_DIFF_PARENT"></span><span id="error_hwnds_have_diff_parent"></span>**Fehler \_ HWNDs \_ verfügen über ein über \_ \_ geordnetes Element**
</dt> <dd> <dl> <dt>

1441 (0x5a1)
</dt> <dt>



Alle Handles für Windows in einer Positions Struktur mit mehreren Fenstern müssen über das gleiche übergeordnete Element verfügen.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_CHILD_WINDOW"></span><span id="error_not_child_window"></span>**Fehler \_ nicht untergeordnetes \_ \_ Fenster**
</dt> <dd> <dl> <dt>

1442 (0x5a2)
</dt> <dt>



Das Fenster ist kein untergeordnetes Fenster.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_GW_COMMAND"></span><span id="error_invalid_gw_command"></span>**Fehler \_ ungültiger \_ GW- \_ Befehl.**
</dt> <dd> <dl> <dt>

1443 (0x5a3)
</dt> <dt>



Ungültiger GW- \_ \* Befehl.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_THREAD_ID"></span><span id="error_invalid_thread_id"></span>**Fehler \_ ungültige \_ Thread- \_ ID.**
</dt> <dd> <dl> <dt>

1444 (0x5a4)
</dt> <dt>



Ungültiger Thread Bezeichner.


</dt> </dl> </dd> <dt>

<span id="ERROR_NON_MDICHILD_WINDOW"></span><span id="error_non_mdichild_window"></span>**\_nicht- \_ MDIChild-Fehler \_ Fenster**
</dt> <dd> <dl> <dt>

1445 (0x5a5)
</dt> <dt>



Eine Nachricht kann nicht von einem Fenster verarbeitet werden, das kein MDI-Fenster (Multiple Document Interface) ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_POPUP_ALREADY_ACTIVE"></span><span id="error_popup_already_active"></span>**Fehler- \_ Popup ist \_ bereits \_ aktiv.**
</dt> <dd> <dl> <dt>

1446 (0x5a6)
</dt> <dt>



Das Popup Menü ist bereits aktiv.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SCROLLBARS"></span><span id="error_no_scrollbars"></span>**Fehler \_ keine \_ Scrollleisten**
</dt> <dd> <dl> <dt>

1447 (0x5a7)
</dt> <dt>



Das Fenster verfügt über keine Scrollleisten.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SCROLLBAR_RANGE"></span><span id="error_invalid_scrollbar_range"></span>**\_ungültiger \_ ScrollBar- \_ Bereich.**
</dt> <dd> <dl> <dt>

1448 (0x5a8)
</dt> <dt>



Der Schiebe Leistenbereich darf nicht größer sein als MAXLONG.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SHOWWIN_COMMAND"></span><span id="error_invalid_showwin_command"></span>**Fehler \_ ungültiger \_ ShowWin- \_ Befehl.**
</dt> <dd> <dl> <dt>

1449 (0x5a9)
</dt> <dt>



Das Fenster kann nicht in der angegebenen Weise angezeigt oder entfernt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SYSTEM_RESOURCES"></span><span id="error_no_system_resources"></span>**Fehler \_ keine \_ System \_ Ressourcen**
</dt> <dd> <dl> <dt>

1450 (0x5aa)
</dt> <dt>



Es sind nicht genügend Systemressourcen vorhanden, um den angeforderten Dienst abzuschließen.


</dt> </dl> </dd> <dt>

<span id="ERROR_NONPAGED_SYSTEM_RESOURCES"></span><span id="error_nonpaged_system_resources"></span>**nicht auslagerbare \_ \_ System \_ Ressourcen**
</dt> <dd> <dl> <dt>

1451 (0x5ab)
</dt> <dt>



Es sind nicht genügend Systemressourcen vorhanden, um den angeforderten Dienst abzuschließen.


</dt> </dl> </dd> <dt>

<span id="ERROR_PAGED_SYSTEM_RESOURCES"></span><span id="error_paged_system_resources"></span>**Fehler beim auslageres \_ \_ System \_ Ressourcen.**
</dt> <dd> <dl> <dt>

1452 (0x5ac)
</dt> <dt>



Es sind nicht genügend Systemressourcen vorhanden, um den angeforderten Dienst abzuschließen.


</dt> </dl> </dd> <dt>

<span id="ERROR_WORKING_SET_QUOTA"></span><span id="error_working_set_quota"></span>**Fehler beim \_ Arbeits \_ Satz \_ Kontingent.**
</dt> <dd> <dl> <dt>

1453 (0x5ad)
</dt> <dt>



Nicht genügend Kontingent zum Durchführen des angeforderten Dienstanbieter.


</dt> </dl> </dd> <dt>

<span id="ERROR_PAGEFILE_QUOTA"></span><span id="error_pagefile_quota"></span>**Fehlerseiten \_ Datei- \_ Kontingent**
</dt> <dd> <dl> <dt>

1454 (0x5ae)
</dt> <dt>



Nicht genügend Kontingent zum Durchführen des angeforderten Dienstanbieter.


</dt> </dl> </dd> <dt>

<span id="ERROR_COMMITMENT_LIMIT"></span><span id="error_commitment_limit"></span>**Fehler \_ Verpflichtungs \_ Limit**
</dt> <dd> <dl> <dt>

1455 (0x5af)
</dt> <dt>



Die Auslagerungs Datei ist zu klein, um diesen Vorgang abzuschließen.


</dt> </dl> </dd> <dt>

<span id="ERROR_MENU_ITEM_NOT_FOUND"></span><span id="error_menu_item_not_found"></span>**Fehler \_ Menü \_ Element wurde \_ nicht \_ gefunden.**
</dt> <dd> <dl> <dt>

1456 (0x5b0)
</dt> <dt>



Ein Menü Element wurde nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_KEYBOARD_HANDLE"></span><span id="error_invalid_keyboard_handle"></span>**Fehler bei \_ ungültigem \_ Tastatur \_ handle.**
</dt> <dd> <dl> <dt>

1457 (0x5b1)
</dt> <dt>



Ungültiges Tastaturlayout-handle.


</dt> </dl> </dd> <dt>

<span id="ERROR_HOOK_TYPE_NOT_ALLOWED"></span><span id="error_hook_type_not_allowed"></span>**Fehler- \_ Hook- \_ Typ \_ nicht \_ zulässig**
</dt> <dd> <dl> <dt>

1458 (0x5b2)
</dt> <dt>



Der Hooks ist nicht zulässig.


</dt> </dl> </dd> <dt>

<span id="ERROR_REQUIRES_INTERACTIVE_WINDOWSTATION"></span><span id="error_requires_interactive_windowstation"></span>**Fehler \_ erfordert \_ interaktive \_ Fenster Station**
</dt> <dd> <dl> <dt>

1459 (0x5b3)
</dt> <dt>



Für diesen Vorgang ist eine interaktive Fenster Station erforderlich.


</dt> </dl> </dd> <dt>

<span id="ERROR_TIMEOUT"></span><span id="error_timeout"></span>**Fehler \_ Timeout**
</dt> <dd> <dl> <dt>

1460 (0x5b4)
</dt> <dt>



Dieser Vorgang wurde wegen Zeitüberschreitung zurückgegeben.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_MONITOR_HANDLE"></span><span id="error_invalid_monitor_handle"></span>**Fehler bei \_ ungültigem \_ Monitor \_ handle.**
</dt> <dd> <dl> <dt>

1461 (0x5b5)
</dt> <dt>



Ungültiges Monitor handle.


</dt> </dl> </dd> <dt>

<span id="ERROR_INCORRECT_SIZE"></span><span id="error_incorrect_size"></span>**Fehler \_ hafte \_ Größe**
</dt> <dd> <dl> <dt>

1462 (0x5b6)
</dt> <dt>



Falsches Größen Argument.


</dt> </dl> </dd> <dt>

<span id="ERROR_SYMLINK_CLASS_DISABLED"></span><span id="error_symlink_class_disabled"></span>**Fehler- \_ symlink- \_ Klasse \_ deaktiviert**
</dt> <dd> <dl> <dt>

1463 (0x5b7)
</dt> <dt>



Die symbolische Verknüpfung kann nicht befolgt werden, da ihr Typ deaktiviert ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_SYMLINK_NOT_SUPPORTED"></span><span id="error_symlink_not_supported"></span>**Fehler \_ symlink \_ \_ wird nicht unterstützt.**
</dt> <dd> <dl> <dt>

1464 (0x5b8)
</dt> <dt>



Diese Anwendung unterstützt nicht den aktuellen Vorgang auf symbolischen Verknüpfungen.


</dt> </dl> </dd> <dt>

<span id="ERROR_XML_PARSE_ERROR"></span><span id="error_xml_parse_error"></span>**Fehler beim \_ Analysieren der XML-Analyse. \_ \_**
</dt> <dd> <dl> <dt>

1465 (0x5b9)
</dt> <dt>



Die angeforderten XML-Daten konnten von Windows nicht analysiert werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_XMLDSIG_ERROR"></span><span id="error_xmldsig_error"></span>**Fehler bei \_ XMLDSIG. \_**
</dt> <dd> <dl> <dt>

1466 (0x5ba)
</dt> <dt>



Fehler beim Verarbeiten einer digitalen XML-Signatur.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESTART_APPLICATION"></span><span id="error_restart_application"></span>**Fehler beim \_ Neustart der \_ Anwendung**
</dt> <dd> <dl> <dt>

1467 (0x5bb)
</dt> <dt>



Diese Anwendung muss neu gestartet werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_WRONG_COMPARTMENT"></span><span id="error_wrong_compartment"></span>**Fehler beim \_ falschen Depot \_**
</dt> <dd> <dl> <dt>

1468 (0x5bc)
</dt> <dt>



Der Aufrufer hat die Verbindungsanforderung im falschen Routing Depot vorgenommen.


</dt> </dl> </dd> <dt>

<span id="ERROR_AUTHIP_FAILURE"></span><span id="error_authip_failure"></span>**Fehler \_ AuthIP- \_ Fehler**
</dt> <dd> <dl> <dt>

1469 (0x5bd)
</dt> <dt>



AuthIP-Fehler beim Versuch, eine Verbindung mit dem Remote Host herzustellen.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_NVRAM_RESOURCES"></span><span id="error_no_nvram_resources"></span>**Fehler \_ keine \_ NVRAM- \_ Ressourcen**
</dt> <dd> <dl> <dt>

1470 (0x5be)
</dt> <dt>



Für den angeforderten Dienst sind nicht genügend NVRAM-Ressourcen vorhanden. Möglicherweise ist ein Neustart erforderlich.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_GUI_PROCESS"></span><span id="error_not_gui_process"></span>**Fehler \_ nicht \_ GUI- \_ Prozess**
</dt> <dd> <dl> <dt>

1471 (0x5bf)
</dt> <dt>



Der angeforderte Vorgang kann nicht abgeschlossen werden, da es sich beim angegebenen Prozess nicht um einen GUI-Prozess handelt.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVENTLOG_FILE_CORRUPT"></span><span id="error_eventlog_file_corrupt"></span>**fehlerhafte \_ Ereignisprotokoll \_ Datei \_**
</dt> <dd> <dl> <dt>

1500 (0x5dc)
</dt> <dt>



Die Ereignisprotokoll Datei ist beschädigt.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVENTLOG_CANT_START"></span><span id="error_eventlog_cant_start"></span>**Fehler beim \_ Starten von EventLog. \_ \_**
</dt> <dd> <dl> <dt>

1501 (0x5dd)
</dt> <dt>



Es konnte keine Ereignisprotokoll Datei geöffnet werden, sodass der Ereignis Protokollierungs Dienst nicht gestartet wurde.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_FILE_FULL"></span><span id="error_log_file_full"></span>**Fehler \_ Protokoll \_ Datei \_ voll**
</dt> <dd> <dl> <dt>

1502 (0x5de)
</dt> <dt>



Die Ereignisprotokolldatei ist voll.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVENTLOG_FILE_CHANGED"></span><span id="error_eventlog_file_changed"></span>**Fehler beim \_ Ändern der Ereignisprotokoll \_ Datei \_ .**
</dt> <dd> <dl> <dt>

1503 (0x5df)
</dt> <dt>



Die Ereignisprotokoll Datei wurde zwischen Lesevorgängen geändert.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_TASK_NAME"></span><span id="error_invalid_task_name"></span>**Fehler \_ ungültiger \_ \_ Taskname.**
</dt> <dd> <dl> <dt>

1550 (0x60E)
</dt> <dt>



Der angegebene TaskName ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_TASK_INDEX"></span><span id="error_invalid_task_index"></span>**Fehler bei \_ ungültigem \_ Task \_ Index.**
</dt> <dd> <dl> <dt>

1551 (0x60F)
</dt> <dt>



Der angegebene Task Index ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_THREAD_ALREADY_IN_TASK"></span><span id="error_thread_already_in_task"></span>**\_der Fehler Thread ist \_ bereits \_ in der \_ Aufgabe**
</dt> <dd> <dl> <dt>

1552 (0x610)
</dt> <dt>



Der angegebene Thread wird bereits einer Aufgabe beitreten.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_SERVICE_FAILURE"></span><span id="error_install_service_failure"></span>**Fehler beim \_ Installieren des \_ Dienst \_ Fehlers.**
</dt> <dd> <dl> <dt>

1601 (0x641)
</dt> <dt>



Auf den Windows Installer Dienst konnte nicht zugegriffen werden. Dies kann vorkommen, wenn die Windows Installer nicht ordnungsgemäß installiert ist. Wenden Sie sich an den Support, um Hilfe zu erhalten.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_USEREXIT"></span><span id="error_install_userexit"></span>**Fehler beim \_ Installieren von \_ Userexit.**
</dt> <dd> <dl> <dt>

1602 (0x642)
</dt> <dt>



Benutzer hat die Installation abgebrochen.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_FAILURE"></span><span id="error_install_failure"></span>**Fehler bei der \_ Installation. \_**
</dt> <dd> <dl> <dt>

1603 (0x643)
</dt> <dt>



Schwerwiegender Fehler bei der Installation.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_SUSPEND"></span><span id="error_install_suspend"></span>**Fehler beim \_ Installieren von \_ Suspend**
</dt> <dd> <dl> <dt>

1604 (0x644)
</dt> <dt>



Die Installation wurde angehalten, unvollständig.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNKNOWN_PRODUCT"></span><span id="error_unknown_product"></span>**Unbekannter Fehler. \_ \_**
</dt> <dd> <dl> <dt>

1605 (0x645)
</dt> <dt>



Diese Aktion ist nur für Produkte gültig, die zurzeit installiert sind.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNKNOWN_FEATURE"></span><span id="error_unknown_feature"></span>**Unbekannter Fehler. \_ \_**
</dt> <dd> <dl> <dt>

1606 (0x646)
</dt> <dt>



Die Funktions-ID ist nicht registriert.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNKNOWN_COMPONENT"></span><span id="error_unknown_component"></span>**\_unbekannter Fehler \_ Komponente.**
</dt> <dd> <dl> <dt>

1607 (0x647)
</dt> <dt>



Die Komponenten-ID ist nicht registriert.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNKNOWN_PROPERTY"></span><span id="error_unknown_property"></span>**\_unbekannter Fehler \_ Eigenschaft.**
</dt> <dd> <dl> <dt>

1608 (0x648)
</dt> <dt>



Unbekannte Eigenschaft.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_HANDLE_STATE"></span><span id="error_invalid_handle_state"></span>**Fehler bei \_ ungültigem \_ handle- \_ Status**
</dt> <dd> <dl> <dt>

1609 (0x649)
</dt> <dt>



Das Handle befindet sich in einem ungültigen Zustand.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_CONFIGURATION"></span><span id="error_bad_configuration"></span>**Fehler \_ hafte \_ Konfiguration**
</dt> <dd> <dl> <dt>

1610 (0x64a)
</dt> <dt>



Die Konfigurationsdaten für dieses Produkt sind beschädigt. Wenden Sie sich an das Support Personal.


</dt> </dl> </dd> <dt>

<span id="ERROR_INDEX_ABSENT"></span><span id="error_index_absent"></span>**Fehler \_ Index \_ fehlt.**
</dt> <dd> <dl> <dt>

1611 (0x64b)
</dt> <dt>



Komponenten Qualifizierer ist nicht vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_SOURCE_ABSENT"></span><span id="error_install_source_absent"></span>**Fehler beim \_ Installieren der \_ Quelle. \_**
</dt> <dd> <dl> <dt>

1612 (0x64c)
</dt> <dt>



Die Installationsquelle für dieses Produkt ist nicht verfügbar. Vergewissern Sie sich, dass die Quelle vorhanden ist und Sie darauf zugreifen können.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_PACKAGE_VERSION"></span><span id="error_install_package_version"></span>**Fehler beim \_ Installieren der \_ Paket \_ Version.**
</dt> <dd> <dl> <dt>

1613 (0x64d)
</dt> <dt>



Dieses Installationspaket kann nicht vom Windows Installer-Dienst installiert werden. Sie müssen eine Windows-Service Pack installieren, die eine neuere Version des Windows Installer Dienstanbieter enthält.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRODUCT_UNINSTALLED"></span><span id="error_product_uninstalled"></span>**Fehler \_ Produkt \_ deinstalliert**
</dt> <dd> <dl> <dt>

1614 (0x64e)
</dt> <dt>



Produkt wird deinstalliert.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_QUERY_SYNTAX"></span><span id="error_bad_query_syntax"></span>**Syntax für ungültige \_ \_ Abfrage Fehler \_**
</dt> <dd> <dl> <dt>

1615 (0x64f)
</dt> <dt>



Die SQL-Abfrage Syntax ist ungültig oder nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_FIELD"></span><span id="error_invalid_field"></span>**\_ungültiges \_ Feld für Fehler**
</dt> <dd> <dl> <dt>

1616 (0x650)
</dt> <dt>



Das Daten Satz Feld ist nicht vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_REMOVED"></span><span id="error_device_removed"></span>**Fehler \_ Gerät \_ entfernt**
</dt> <dd> <dl> <dt>

1617 (0x651)
</dt> <dt>



Das Gerät wurde entfernt.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_ALREADY_RUNNING"></span><span id="error_install_already_running"></span>**Fehler \_ Installation wird \_ bereits \_ ausgeführt.**
</dt> <dd> <dl> <dt>

1618 (0x652)
</dt> <dt>



Es wird bereits eine andere Installation ausgeführt. Schließen Sie diese Installation ab, bevor Sie mit der Installation fortfahren.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_PACKAGE_OPEN_FAILED"></span><span id="error_install_package_open_failed"></span>**Fehler \_ beim \_ Öffnen des Pakets beim \_ Öffnen \_ .**
</dt> <dd> <dl> <dt>

1619 (0x653)
</dt> <dt>



Dieses Installationspaket konnte nicht geöffnet werden. Vergewissern Sie sich, dass das Paket vorhanden ist und Sie darauf zugreifen können, oder wenden Sie sich an den Hersteller der Anwendung, um zu überprüfen, ob dies ein gültiges Windows Installer Paket


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_PACKAGE_INVALID"></span><span id="error_install_package_invalid"></span>**Fehler beim \_ Installieren des \_ Pakets. \_**
</dt> <dd> <dl> <dt>

1620 (0x654)
</dt> <dt>



Dieses Installationspaket konnte nicht geöffnet werden. Wenden Sie sich an den Hersteller der Anwendung, um sicherzustellen, dass dies ein gültiges Windows Installer Paket ist


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_UI_FAILURE"></span><span id="error_install_ui_failure"></span>**Fehler beim \_ Installieren des \_ Benutzer \_ Oberflächen Fehlers**
</dt> <dd> <dl> <dt>

1621 (0x655)
</dt> <dt>



Fehler beim Starten der Benutzeroberfläche des Windows Installer Dienstanbieter. Wenden Sie sich an das Support Personal.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_LOG_FAILURE"></span><span id="error_install_log_failure"></span>**Fehler beim \_ Installieren des \_ Protokolls \_**
</dt> <dd> <dl> <dt>

1622 (0x656)
</dt> <dt>



Fehler beim Öffnen der Installationsprotokoll Datei. Vergewissern Sie sich, dass der angegebene Speicherort der Protokolldatei vorhanden ist und Sie darauf schreiben können.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_LANGUAGE_UNSUPPORTED"></span><span id="error_install_language_unsupported"></span>**Fehler beim \_ Installieren der \_ Sprache \_ nicht unterstützt**
</dt> <dd> <dl> <dt>

1623 (0x657)
</dt> <dt>



Die Sprache dieses Installationspakets wird von Ihrem System nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_TRANSFORM_FAILURE"></span><span id="error_install_transform_failure"></span>**Fehler beim \_ Installieren der \_ Transformation. \_**
</dt> <dd> <dl> <dt>

1624 (0x658)
</dt> <dt>



Fehler beim Anwenden von Transformationen. Überprüfen Sie, ob die angegebenen Transformationspfade gültig sind.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_PACKAGE_REJECTED"></span><span id="error_install_package_rejected"></span>**Fehler beim \_ Installieren des \_ Pakets. \_**
</dt> <dd> <dl> <dt>

1625 (0x659)
</dt> <dt>



Diese Installation ist durch die System Richtlinie unzulässig. Wenden Sie sich an Ihren Systemadministrator.


</dt> </dl> </dd> <dt>

<span id="ERROR_FUNCTION_NOT_CALLED"></span><span id="error_function_not_called"></span>**Fehler \_ Funktion \_ nicht \_ aufgerufen**
</dt> <dd> <dl> <dt>

1626 (0x65a)
</dt> <dt>



Die Funktion konnte nicht ausgeführt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_FUNCTION_FAILED"></span><span id="error_function_failed"></span>**Fehler bei Fehler \_ Funktion \_**
</dt> <dd> <dl> <dt>

1627 (0x65b)
</dt> <dt>



Fehler bei der Ausführung der Funktion.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_TABLE"></span><span id="error_invalid_table"></span>**Fehler \_ ungültige \_ Tabelle**
</dt> <dd> <dl> <dt>

1628 (0x65c)
</dt> <dt>



Es wurde eine ungültige oder unbekannte Tabelle angegeben.


</dt> </dl> </dd> <dt>

<span id="ERROR_DATATYPE_MISMATCH"></span><span id="error_datatype_mismatch"></span>**Fehler bei \_ DataType-Konflikt. \_**
</dt> <dd> <dl> <dt>

1629 (0x65d)
</dt> <dt>



Die bereitgestellten Daten haben einen falschen Typ.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNSUPPORTED_TYPE"></span><span id="error_unsupported_type"></span>**\_nicht unterstützter Typ des Fehlers. \_**
</dt> <dd> <dl> <dt>

1630 (0x65e)
</dt> <dt>



Daten dieses Typs werden nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="ERROR_CREATE_FAILED"></span><span id="error_create_failed"></span>**Fehler beim \_ erstellen. \_**
</dt> <dd> <dl> <dt>

1631 (0x65f)
</dt> <dt>



Der Windows Installer-Dienst konnte nicht gestartet werden. Wenden Sie sich an das Support Personal.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_TEMP_UNWRITABLE"></span><span id="error_install_temp_unwritable"></span>**Fehler beim Installieren der temporären \_ \_ \_ nicht Schreib baren Datei**
</dt> <dd> <dl> <dt>

1632 (0x660)
</dt> <dt>



Der Temp-Ordner befindet sich auf einem Laufwerk, das voll ist oder nicht zugänglich ist. Geben Sie Speicherplatz auf dem Laufwerk frei, oder überprüfen Sie, ob Sie über Schreibberechtigungen für den temporären Ordner verfügen.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_PLATFORM_UNSUPPORTED"></span><span id="error_install_platform_unsupported"></span>**Fehler beim \_ Installieren der \_ Plattform \_ nicht unterstützt**
</dt> <dd> <dl> <dt>

1633 (0x661)
</dt> <dt>



Dieses Installationspaket wird von diesem Prozessortyp nicht unterstützt. Wenden Sie sich an Ihren Produkthersteller.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_NOTUSED"></span><span id="error_install_notused"></span>**Fehler beim \_ Installieren von \_ notused**
</dt> <dd> <dl> <dt>

1634 (0x662)
</dt> <dt>



Die Komponente wird auf diesem Computer nicht verwendet.


</dt> </dl> </dd> <dt>

<span id="ERROR_PATCH_PACKAGE_OPEN_FAILED"></span><span id="error_patch_package_open_failed"></span>**Fehler beim \_ Öffnen des Patch- \_ Pakets \_ \_**
</dt> <dd> <dl> <dt>

1635 (0x663)
</dt> <dt>



Dieses Update Paket konnte nicht geöffnet werden. Vergewissern Sie sich, dass das Update Paket vorhanden ist und Sie darauf zugreifen können, oder wenden Sie sich an den Hersteller der Anwendung, um zu überprüfen, ob es sich um ein gültiges Windows Installer Update


</dt> </dl> </dd> <dt>

<span id="ERROR_PATCH_PACKAGE_INVALID"></span><span id="error_patch_package_invalid"></span>**Fehler beim \_ Patch- \_ Paket \_ ungültig**
</dt> <dd> <dl> <dt>

1636 (0x664)
</dt> <dt>



Dieses Update Paket konnte nicht geöffnet werden. Wenden Sie sich an den Hersteller der Anwendung, um zu überprüfen, ob es sich um ein gültiges Windows Installer Update


</dt> </dl> </dd> <dt>

<span id="ERROR_PATCH_PACKAGE_UNSUPPORTED"></span><span id="error_patch_package_unsupported"></span>**Fehler beim \_ Patch- \_ Paket \_ nicht unterstützt**
</dt> <dd> <dl> <dt>

1637 (0x665)
</dt> <dt>



Dieses Update Paket kann nicht vom Windows Installer-Dienst verarbeitet werden. Sie müssen eine Windows-Service Pack installieren, die eine neuere Version des Windows Installer Dienstanbieter enthält.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRODUCT_VERSION"></span><span id="error_product_version"></span>**Fehler \_ Produkt \_ Version**
</dt> <dd> <dl> <dt>

1638 (0x666)
</dt> <dt>



Eine andere Version dieses Produkts ist bereits installiert. Die Installation dieser Version kann nicht fortgesetzt werden. Um die vorhandene Version dieses Produkts zu konfigurieren oder zu entfernen, verwenden Sie die Option Software in der Systemsteuerung.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_COMMAND_LINE"></span><span id="error_invalid_command_line"></span>**Fehler \_ ungültige \_ Befehls \_ Zeile.**
</dt> <dd> <dl> <dt>

1639 (0x667)
</dt> <dt>



Ungültiges Befehlszeilenargument. Ausführliche Hilfe zur Befehlszeile finden Sie im Windows Installer SDK.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_REMOTE_DISALLOWED"></span><span id="error_install_remote_disallowed"></span>**Fehler beim \_ Installieren von \_ Remote. \_**
</dt> <dd> <dl> <dt>

1640 (0x668)
</dt> <dt>



Nur Administratoren verfügen über die Berechtigung zum Hinzufügen, entfernen oder Konfigurieren von Server Software während einer Terminal Dienste-Remote Sitzung. Wenn Sie Software auf dem Server installieren oder konfigurieren möchten, wenden Sie sich an Ihren Netzwerkadministrator.


</dt> </dl> </dd> <dt>

<span id="ERROR_SUCCESS_REBOOT_INITIATED"></span><span id="error_success_reboot_initiated"></span>**Fehler \_ beim \_ Neustart \_ wurde initiiert.**
</dt> <dd> <dl> <dt>

1641 (0x669)
</dt> <dt>



Der angeforderte Vorgang wurde erfolgreich abgeschlossen. Das System wird neu gestartet, damit die Änderungen wirksam werden können.


</dt> </dl> </dd> <dt>

<span id="ERROR_PATCH_TARGET_NOT_FOUND"></span><span id="error_patch_target_not_found"></span>**Das \_ \_ fehlerpatchziel wurde \_ nicht \_ gefunden.**
</dt> <dd> <dl> <dt>

1642 (0x66a)
</dt> <dt>



Das Upgrade kann nicht vom Windows Installer-Dienst installiert werden, weil das zu Aktualisier Ende Programm möglicherweise fehlt, oder das Upgrade kann eine andere Version des Programms aktualisieren. Vergewissern Sie sich, dass das zu Aktualisier Ende Programm auf dem Computer vorhanden ist und dass Sie über das richtige Upgrade verfügen.


</dt> </dl> </dd> <dt>

<span id="ERROR_PATCH_PACKAGE_REJECTED"></span><span id="error_patch_package_rejected"></span>**Fehler beim \_ Patch- \_ Paket \_ abgelehnt**
</dt> <dd> <dl> <dt>

1643 (0x66b)
</dt> <dt>



Das Update Paket ist von der Software Einschränkungs Richtlinie nicht zulässig.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_TRANSFORM_REJECTED"></span><span id="error_install_transform_rejected"></span>**Fehler beim \_ Installieren der \_ Transformation. \_**
</dt> <dd> <dl> <dt>

1644 (0x66c)
</dt> <dt>



Eine oder mehrere Anpassungen sind von der Software Einschränkungs Richtlinie nicht zulässig.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_REMOTE_PROHIBITED"></span><span id="error_install_remote_prohibited"></span>**Fehler beim \_ Installieren der \_ Remote Installation. \_**
</dt> <dd> <dl> <dt>

1645 (0x66D)
</dt> <dt>



In der Windows Installer ist die Installation von einem Remotedesktopverbindung nicht zulässig.


</dt> </dl> </dd> <dt>

<span id="ERROR_PATCH_REMOVAL_UNSUPPORTED"></span><span id="error_patch_removal_unsupported"></span>**Entfernen des Fehler \_ Patches \_ \_ nicht unterstützt**
</dt> <dd> <dl> <dt>

1646 (0x66E)
</dt> <dt>



Die Installation des Update Pakets wird nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNKNOWN_PATCH"></span><span id="error_unknown_patch"></span>**Unbekannter Fehler beim \_ \_ Patch.**
</dt> <dd> <dl> <dt>

1647 (0x66f)
</dt> <dt>



Das Update wird nicht auf dieses Produkt angewendet.


</dt> </dl> </dd> <dt>

<span id="ERROR_PATCH_NO_SEQUENCE"></span><span id="error_patch_no_sequence"></span>**Fehler \_ Patch \_ keine \_ Sequenz**
</dt> <dd> <dl> <dt>

1648 (0x670)
</dt> <dt>



Für den Satz von Updates konnte keine gültige Sequenz gefunden werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_PATCH_REMOVAL_DISALLOWED"></span><span id="error_patch_removal_disallowed"></span>**Fehler beim Entfernen des Fehler \_ Patches. \_ \_**
</dt> <dd> <dl> <dt>

1649 (0x671)
</dt> <dt>



Das Entfernen von Updates wurde durch die Richtlinie nicht zugelassen.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PATCH_XML"></span><span id="error_invalid_patch_xml"></span>**Fehler \_ ungültige \_ Patch- \_ XML.**
</dt> <dd> <dl> <dt>

1650 (0x672)
</dt> <dt>



Die XML-Update Daten sind ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_PATCH_MANAGED_ADVERTISED_PRODUCT"></span><span id="error_patch_managed_advertised_product"></span>**Fehler \_ Patch für \_ verwaltete \_ angekündigte \_ Produkte**
</dt> <dd> <dl> <dt>

1651 (0x673)
</dt> <dt>



Windows Installer lässt keine Aktualisierung von verwalteten angekündigten Produkten zu. Vor dem Anwenden des Updates muss mindestens eine Produkt Funktion installiert werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_SERVICE_SAFEBOOT"></span><span id="error_install_service_safeboot"></span>**Fehler beim \_ Installieren von \_ Dienst- \_ SafeBoot**
</dt> <dd> <dl> <dt>

1652 (0x674)
</dt> <dt>



Der Windows Installer-Dienst ist im abgesicherten Modus nicht verfügbar. Versuchen Sie es erneut, wenn sich Ihr Computer nicht im abgesicherten Modus befindet, oder Sie können die System Wiederherstellung verwenden, um den Computer in einen früheren Zustand zurückzukehren.


</dt> </dl> </dd> <dt>

<span id="ERROR_FAIL_FAST_EXCEPTION"></span><span id="error_fail_fast_exception"></span>**Fehler \_ bei \_ schneller \_ Ausnahme bei Fehler.**
</dt> <dd> <dl> <dt>

1653 (0x675)
</dt> <dt>



Es ist eine fehlerhafte Ausnahme aufgetreten. Ausnahmehandler werden nicht aufgerufen, und der Prozess wird sofort beendet.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_REJECTED"></span><span id="error_install_rejected"></span>**Fehler \_ Installation \_ abgelehnt**
</dt> <dd> <dl> <dt>

1654 (0x676)
</dt> <dt>



Die APP, die Sie ausführen möchten, wird in dieser Windows-Version nicht unterstützt.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Winerror. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[System Fehler Codes](system-error-codes.md)
</dt> </dl>

 

 




