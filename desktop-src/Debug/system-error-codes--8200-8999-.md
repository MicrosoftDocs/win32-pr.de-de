---
description: Beschreibt die fehlercodes 8200-8999, die in der WinError.h-Headerdatei definiert sind und für Entwickler bestimmt sind.
ms.assetid: f16fdfa3-b080-47ee-a7dd-241fe2d24278
title: Systemfehlercodes (8200-8999) (WinError.h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: e9fd65025c3d51575cb0ece83cba14e0c62980d11a60ec6cb351919b6c7714c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119572960"
---
# <a name="system-error-codes-8200-8999"></a>Systemfehlercodes (8200-8999)

> [!NOTE]
> Diese Informationen sind für Entwickler bestimmt, die Systemfehler debuggen. Für andere Fehler, z. B. Probleme mit Windows Update, finden Sie auf der Seite [Fehlercodes](system-error-codes.md) eine Liste mit Ressourcen.

In der folgenden Liste werden [Systemfehlercodes](system-error-codes.md) für die Fehler 8200 bis 8999 beschrieben. Sie werden von der [**GetLastError-Funktion**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) zurückgegeben, wenn viele Funktionen fehlschlagen. Um den Beschreibungstext für den Fehler in Ihrer Anwendung abzurufen, verwenden Sie die [**FormatMessage-Funktion**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) mit dem **FORMAT MESSAGE FROM \_ \_ \_ SYSTEM-Flag.**

<dl> <dt>

<span id="ERROR_DS_NOT_INSTALLED"></span><span id="error_ds_not_installed"></span>**FEHLER \_ DS \_ NICHT \_ INSTALLIERT**
</dt> <dd> <dl> <dt>

8200 (0x2008)
</dt> <dt>



Fehler beim Installieren des Verzeichnisdiensts. Weitere Informationen finden Sie im Ereignisprotokoll.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MEMBERSHIP_EVALUATED_LOCALLY"></span><span id="error_ds_membership_evaluated_locally"></span>**FEHLER \_ BEI LOKALER AUSWERTUNG DER DS-MITGLIEDSCHAFT \_ \_ \_**
</dt> <dd> <dl> <dt>

8201 (0x2009)
</dt> <dt>



Der Verzeichnisdienst hat Gruppenmitgliedschaften lokal ausgewertet.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_ATTRIBUTE_OR_VALUE"></span><span id="error_ds_no_attribute_or_value"></span>**FEHLER \_ DS \_ KEIN ATTRIBUT ODER \_ \_ \_ WERT**
</dt> <dd> <dl> <dt>

8202 (0x200A)
</dt> <dt>



Das angegebene Verzeichnisdienstattribut oder der angegebene Wert ist nicht vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INVALID_ATTRIBUTE_SYNTAX"></span><span id="error_ds_invalid_attribute_syntax"></span>**FEHLER \_ \_ DS: UNGÜLTIGE \_ \_ ATTRIBUTSYNTAX**
</dt> <dd> <dl> <dt>

8203 (0x200B)
</dt> <dt>



Die für den Verzeichnisdienst angegebene Attributsyntax ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ATTRIBUTE_TYPE_UNDEFINED"></span><span id="error_ds_attribute_type_undefined"></span>**\_FEHLER: \_ DS-ATTRIBUTTYP \_ \_ UNDEFINED**
</dt> <dd> <dl> <dt>

8204 (0x200C)
</dt> <dt>



Der für den Verzeichnisdienst angegebene Attributtyp ist nicht definiert.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ATTRIBUTE_OR_VALUE_EXISTS"></span><span id="error_ds_attribute_or_value_exists"></span>**FEHLER: \_ DS-ATTRIBUT \_ ODER \_ \_ -WERT \_ VORHANDEN**
</dt> <dd> <dl> <dt>

8205 (0x200D)
</dt> <dt>



Das angegebene Verzeichnisdienstattribut oder der angegebene Wert ist bereits vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_BUSY"></span><span id="error_ds_busy"></span>**FEHLER \_ DS \_ AUSGELASTET**
</dt> <dd> <dl> <dt>

8206 (0x200E)
</dt> <dt>



Der Verzeichnisdienst ist ausgelastet.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_UNAVAILABLE"></span><span id="error_ds_unavailable"></span>**FEHLER \_ DS \_ NICHT VERFÜGBAR**
</dt> <dd> <dl> <dt>

8207 (0x200F)
</dt> <dt>



Der Verzeichnisdienst ist nicht verfügbar.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_RIDS_ALLOCATED"></span><span id="error_ds_no_rids_allocated"></span>**FEHLER \_ DS \_ KEINE \_ ZUGEORDNETEN RIDS \_**
</dt> <dd> <dl> <dt>

8208 (0x2010)
</dt> <dt>



Der Verzeichnisdienst kann keinen relativen Bezeichner zuweisen.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_MORE_RIDS"></span><span id="error_ds_no_more_rids"></span>**FEHLER \_ \_ DS: KEINE \_ \_ RIDS MEHR**
</dt> <dd> <dl> <dt>

8209 (0x2011)
</dt> <dt>



Der Verzeichnisdienst hat den Pool relativer Bezeichner erschöpft.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INCORRECT_ROLE_OWNER"></span><span id="error_ds_incorrect_role_owner"></span>**FEHLER \_ \_ DS: FALSCHER \_ \_ ROLLENBESITZER**
</dt> <dd> <dl> <dt>

8210 (0x2012)
</dt> <dt>



Der angeforderte Vorgang konnte nicht ausgeführt werden, da der Verzeichnisdienst nicht der Master für diesen Vorgangstyp ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_RIDMGR_INIT_ERROR"></span><span id="error_ds_ridmgr_init_error"></span>**FEHLER \_ DS \_ RIDMGR \_ INIT \_ ERROR**
</dt> <dd> <dl> <dt>

8211 (0x2013)
</dt> <dt>



Der Verzeichnisdienst konnte das Subsystem, das relative Bezeichner zuordnet, nicht initialisieren.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OBJ_CLASS_VIOLATION"></span><span id="error_ds_obj_class_violation"></span>**FEHLER: \_ \_ \_ \_ DS-OBJ-KLASSENVERLETZUNG**
</dt> <dd> <dl> <dt>

8212 (0x2014)
</dt> <dt>



Der angeforderte Vorgang hat mindestens eine Einschränkung, die der Klasse des -Objekts zugeordnet ist, nicht erfüllt.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_ON_NON_LEAF"></span><span id="error_ds_cant_on_non_leaf"></span>**FEHLER \_ DS \_ CANT \_ ON NON \_ \_ LEAF**
</dt> <dd> <dl> <dt>

8213 (0x2015)
</dt> <dt>



Der Verzeichnisdienst kann den angeforderten Vorgang nur für ein Blattobjekt ausführen.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_ON_RDN"></span><span id="error_ds_cant_on_rdn"></span>**FEHLER \_ DS \_ CANT \_ ON \_ RDN**
</dt> <dd> <dl> <dt>

8214 (0x2016)
</dt> <dt>



Der Verzeichnisdienst kann den angeforderten Vorgang nicht für das RDN-Attribut eines Objekts ausführen.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_MOD_OBJ_CLASS"></span><span id="error_ds_cant_mod_obj_class"></span>**ERROR \_ DS \_ CANT \_ MOD \_ OBJ \_ CLASS**
</dt> <dd> <dl> <dt>

8215 (0x2017)
</dt> <dt>



Der Verzeichnisdienst hat einen Versuch erkannt, die Objektklasse eines Objekts zu ändern.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CROSS_DOM_MOVE_ERROR"></span><span id="error_ds_cross_dom_move_error"></span>**FEHLER \_ DS \_ CROSS DOM MOVE \_ \_ \_ ERROR**
</dt> <dd> <dl> <dt>

8216 (0x2018)
</dt> <dt>



Der angeforderte domänenübergreifende Verschiebungsvorgang konnte nicht ausgeführt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_GC_NOT_AVAILABLE"></span><span id="error_ds_gc_not_available"></span>**\_FEHLER: \_ DS-GC \_ NICHT \_ VERFÜGBAR**
</dt> <dd> <dl> <dt>

8217 (0x2019)
</dt> <dt>



Der globale Katalogserver kann nicht kontaktiert werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_SHARED_POLICY"></span><span id="error_shared_policy"></span>**FEHLER \_ BEI \_ FREIGEGEBENER RICHTLINIE**
</dt> <dd> <dl> <dt>

8218 (0x201A)
</dt> <dt>



Das Richtlinienobjekt wird freigegeben und kann nur im Stamm geändert werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_POLICY_OBJECT_NOT_FOUND"></span><span id="error_policy_object_not_found"></span>**\_ \_ FEHLERRICHTLINIENOBJEKT NICHT \_ \_ GEFUNDEN**
</dt> <dd> <dl> <dt>

8219 (0x201B)
</dt> <dt>



Das Richtlinienobjekt ist nicht vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_POLICY_ONLY_IN_DS"></span><span id="error_policy_only_in_ds"></span>**FEHLERRICHTLINIE \_ \_ NUR IN \_ \_ DS**
</dt> <dd> <dl> <dt>

8220 (0x201C)
</dt> <dt>



Die angeforderten Richtlinieninformationen befinden sich nur im Verzeichnisdienst.


</dt> </dl> </dd> <dt>

<span id="ERROR_PROMOTION_ACTIVE"></span><span id="error_promotion_active"></span>**FEHLER \_ HERAUFSTUFUNG \_ AKTIV**
</dt> <dd> <dl> <dt>

8221 (0x201D)
</dt> <dt>



Eine Heraufstufung des Domänencontrollers ist derzeit aktiv.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_PROMOTION_ACTIVE"></span><span id="error_no_promotion_active"></span>**FEHLER \_ KEINE \_ HERAUFSTUFUNG \_ AKTIV**
</dt> <dd> <dl> <dt>

8222 (0x201E)
</dt> <dt>



Eine Heraufstufung des Domänencontrollers ist derzeit nicht aktiv.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OPERATIONS_ERROR"></span><span id="error_ds_operations_error"></span>**FEHLER \_ BEI \_ DS-VORGÄNGEN \_**
</dt> <dd> <dl> <dt>

8224 (0x2020)
</dt> <dt>



Ein Betriebsfehler ist aufgetreten.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_PROTOCOL_ERROR"></span><span id="error_ds_protocol_error"></span>**FEHLER \_ BEIM \_ DS-PROTOKOLLFEHLER \_**
</dt> <dd> <dl> <dt>

8225 (0x2021)
</dt> <dt>



Es ist ein Protokollfehler aufgetreten.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_TIMELIMIT_EXCEEDED"></span><span id="error_ds_timelimit_exceeded"></span>**FEHLER \_ DS \_ TIMELIMIT \_ ÜBERSCHRITTEN**
</dt> <dd> <dl> <dt>

8226 (0x2022)
</dt> <dt>



Das Zeitlimit für diese Anforderung wurde überschritten.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SIZELIMIT_EXCEEDED"></span><span id="error_ds_sizelimit_exceeded"></span>**FEHLER \_ DS \_ SIZELIMIT \_ ÜBERSCHRITTEN**
</dt> <dd> <dl> <dt>

8227 (0x2023)
</dt> <dt>



Die Größenbeschränkung für diese Anforderung wurde überschritten.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ADMIN_LIMIT_EXCEEDED"></span><span id="error_ds_admin_limit_exceeded"></span>**\_FEHLER: \_ DS-ADMINISTRATORLIMIT \_ \_ ÜBERSCHRITTEN**
</dt> <dd> <dl> <dt>

8228 (0x2024)
</dt> <dt>



Der Verwaltungsgrenzwert für diese Anforderung wurde überschritten.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_COMPARE_FALSE"></span><span id="error_ds_compare_false"></span>**FEHLER \_ DS \_ COMPARE \_ FALSE**
</dt> <dd> <dl> <dt>

8229 (0x2025)
</dt> <dt>



Die Vergleichsantwort war "false".


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_COMPARE_TRUE"></span><span id="error_ds_compare_true"></span>**FEHLER \_ DS \_ COMPARE \_ TRUE**
</dt> <dd> <dl> <dt>

8230 (0x2026)
</dt> <dt>



Die Vergleichsantwort war "true".


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_AUTH_METHOD_NOT_SUPPORTED"></span><span id="error_ds_auth_method_not_supported"></span>**\_FEHLER: \_ DS-AUTHENTIFIZIERUNGSMETHODE \_ WIRD NICHT \_ \_ UNTERSTÜTZT**
</dt> <dd> <dl> <dt>

8231 (0x2027)
</dt> <dt>



Die angeforderte Authentifizierungsmethode wird vom Server nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_STRONG_AUTH_REQUIRED"></span><span id="error_ds_strong_auth_required"></span>**FEHLER \_ DS \_ STRONG \_ AUTH \_ ERFORDERLICH**
</dt> <dd> <dl> <dt>

8232 (0x2028)
</dt> <dt>



Für diesen Server ist eine sicherere Authentifizierungsmethode erforderlich.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INAPPROPRIATE_AUTH"></span><span id="error_ds_inappropriate_auth"></span>**FEHLER: \_ DS \_ : \_ UNGEEIGNETE AUTHENTIFIZIERUNG**
</dt> <dd> <dl> <dt>

8233 (0x2029)
</dt> <dt>



Ungeeignete Authentifizierung.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_AUTH_UNKNOWN"></span><span id="error_ds_auth_unknown"></span>**FEHLER \_ DS \_ AUTH \_ UNKNOWN**
</dt> <dd> <dl> <dt>

8234 (0x202A)
</dt> <dt>



Der Authentifizierungsmechanismus ist unbekannt.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_REFERRAL"></span><span id="error_ds_referral"></span>**FEHLER \_ \_ DS-EMPFEHLUNG**
</dt> <dd> <dl> <dt>

8235 (0x202B)
</dt> <dt>



Vom Server wurde eine Referenz zurückgegeben.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_UNAVAILABLE_CRIT_EXTENSION"></span><span id="error_ds_unavailable_crit_extension"></span>**FEHLER: \_ NICHT \_ VERFÜGBARE \_ CRIT-ERWEITERUNG FÜR DS \_**
</dt> <dd> <dl> <dt>

8236 (0x202C)
</dt> <dt>



Der Server unterstützt die angeforderte kritische Erweiterung nicht.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CONFIDENTIALITY_REQUIRED"></span><span id="error_ds_confidentiality_required"></span>**FEHLER \_ \_ DS-VERTRAULICHKEIT \_ ERFORDERLICH**
</dt> <dd> <dl> <dt>

8237 (0x202D)
</dt> <dt>



Diese Anforderung erfordert eine sichere Verbindung.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INAPPROPRIATE_MATCHING"></span><span id="error_ds_inappropriate_matching"></span>**FEHLER: \_ DS – \_ UNGEEIGNETER \_ ABGLEICH**
</dt> <dd> <dl> <dt>

8238 (0x202E)
</dt> <dt>



Ungeeigneter Abgleich.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CONSTRAINT_VIOLATION"></span><span id="error_ds_constraint_violation"></span>**\_FEHLER: \_ DS-EINSCHRÄNKUNGSVERLETZUNG \_**
</dt> <dd> <dl> <dt>

8239 (0x202F)
</dt> <dt>



Eine Einschränkungsverletzung ist aufgetreten.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_SUCH_OBJECT"></span><span id="error_ds_no_such_object"></span>**FEHLER \_ DS \_ KEIN \_ SOLCHES \_ OBJEKT**
</dt> <dd> <dl> <dt>

8240 (0x2030)
</dt> <dt>



Ein solches Objekt ist auf dem Server nicht vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ALIAS_PROBLEM"></span><span id="error_ds_alias_problem"></span>**\_FEHLER: \_ DS-ALIASPROBLEM \_**
</dt> <dd> <dl> <dt>

8241 (0x2031)
</dt> <dt>



Es liegt ein Aliasproblem vor.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INVALID_DN_SYNTAX"></span><span id="error_ds_invalid_dn_syntax"></span>**FEHLER \_ DS \_ \_ UNGÜLTIGE DN-SYNTAX \_**
</dt> <dd> <dl> <dt>

8242 (0x2032)
</dt> <dt>



Es wurde eine ungültige dn-Syntax angegeben.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_IS_LEAF"></span><span id="error_ds_is_leaf"></span>**FEHLER \_ DS \_ IS \_ LEAF**
</dt> <dd> <dl> <dt>

8243 (0x2033)
</dt> <dt>



Das -Objekt ist ein Blattobjekt.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ALIAS_DEREF_PROBLEM"></span><span id="error_ds_alias_deref_problem"></span>**FEHLER \_ DS \_ ALIAS \_ DEREF \_ PROBLEM**
</dt> <dd> <dl> <dt>

8244 (0x2034)
</dt> <dt>



Es liegt ein Aliasdeferencing-Problem vor.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_UNWILLING_TO_PERFORM"></span><span id="error_ds_unwilling_to_perform"></span>**FEHLER \_ BEIM AUSFÜHREN VON DS-FEHLERN \_ \_ \_**
</dt> <dd> <dl> <dt>

8245 (0x2035)
</dt> <dt>



Der Server ist nicht bereit, die Anforderung zu verarbeiten.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_LOOP_DETECT"></span><span id="error_ds_loop_detect"></span>**FEHLER \_ BEIM ERKENNEN EINER DS-SCHLEIFE \_ \_**
</dt> <dd> <dl> <dt>

8246 (0x2036)
</dt> <dt>



Eine Schleife wurde erkannt.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAMING_VIOLATION"></span><span id="error_ds_naming_violation"></span>**\_FEHLER: \_ DS-BENENNUNGSVERLETZUNG \_**
</dt> <dd> <dl> <dt>

8247 (0x2037)
</dt> <dt>



Es liegt ein Namensverstoß vor.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OBJECT_RESULTS_TOO_LARGE"></span><span id="error_ds_object_results_too_large"></span>**\_FEHLER: \_ DS-OBJEKTERGEBNISSE \_ \_ ZU \_ GROß**
</dt> <dd> <dl> <dt>

8248 (0x2038)
</dt> <dt>



Das Ergebnis ist zu groß.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_AFFECTS_MULTIPLE_DSAS"></span><span id="error_ds_affects_multiple_dsas"></span>**FEHLER \_ DS \_ WIRKT SICH AUF \_ MEHRERE \_ DSAS AUS**
</dt> <dd> <dl> <dt>

8249 (0x2039)
</dt> <dt>



Der Vorgang wirkt sich auf mehrere DSAs aus.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SERVER_DOWN"></span><span id="error_ds_server_down"></span>**\_FEHLER: \_ DS-SERVER \_ NICHT VERFÜGBAR**
</dt> <dd> <dl> <dt>

8250 (0x203A)
</dt> <dt>



Der Server ist nicht funktionstüchtig.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_LOCAL_ERROR"></span><span id="error_ds_local_error"></span>**FEHLER \_ BEIM LOKALEN \_ DS-FEHLER \_**
</dt> <dd> <dl> <dt>

8251 (0x203B)
</dt> <dt>



Ein lokaler Fehler ist aufgetreten.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ENCODING_ERROR"></span><span id="error_ds_encoding_error"></span>**\_FEHLER: \_ DS-CODIERUNGSFEHLER \_**
</dt> <dd> <dl> <dt>

8252 (0x203C)
</dt> <dt>



Es ist ein Codierungsfehler aufgetreten.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DECODING_ERROR"></span><span id="error_ds_decoding_error"></span>**FEHLER \_ BEI DER \_ DS-DECODIERUNG \_**
</dt> <dd> <dl> <dt>

8253 (0x203D)
</dt> <dt>



Ein Decodierungsfehler ist aufgetreten.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_FILTER_UNKNOWN"></span><span id="error_ds_filter_unknown"></span>**FEHLER \_ DS \_ FILTER \_ UNKNOWN**
</dt> <dd> <dl> <dt>

8254 (0x203E)
</dt> <dt>



Der Suchfilter kann nicht erkannt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_PARAM_ERROR"></span><span id="error_ds_param_error"></span>**FEHLER \_ BEIM \_ DS-PARAM \_**
</dt> <dd> <dl> <dt>

8255 (0x203F)
</dt> <dt>



Mindestens ein Parameter ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NOT_SUPPORTED"></span><span id="error_ds_not_supported"></span>**FEHLER \_ DS \_ NICHT \_ UNTERSTÜTZT**
</dt> <dd> <dl> <dt>

8256 (0x2040)
</dt> <dt>



Die angegebene Methode wird nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_RESULTS_RETURNED"></span><span id="error_ds_no_results_returned"></span>**FEHLER \_ DS \_ KEINE ERGEBNISSE \_ \_ ZURÜCKGEGEBEN**
</dt> <dd> <dl> <dt>

8257 (0x2041)
</dt> <dt>



Es wurden keine Ergebnisse zurückgegeben.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CONTROL_NOT_FOUND"></span><span id="error_ds_control_not_found"></span>**FEHLER \_ \_ DS-STEUERELEMENT \_ NICHT \_ GEFUNDEN**
</dt> <dd> <dl> <dt>

8258 (0x2042)
</dt> <dt>



Das angegebene Steuerelement wird vom Server nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CLIENT_LOOP"></span><span id="error_ds_client_loop"></span>**FEHLER \_ BEI DS-CLIENTSCHLEIFE \_ \_**
</dt> <dd> <dl> <dt>

8259 (0x2043)
</dt> <dt>



Vom Client wurde eine Empfehlungsschleife erkannt.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_REFERRAL_LIMIT_EXCEEDED"></span><span id="error_ds_referral_limit_exceeded"></span>**\_FEHLER: \_ DS-EMPFEHLUNGSLIMIT \_ \_ ÜBERSCHRITTEN**
</dt> <dd> <dl> <dt>

8260 (0x2044)
</dt> <dt>



Das vordefinierte Verweislimit wurde überschritten.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SORT_CONTROL_MISSING"></span><span id="error_ds_sort_control_missing"></span>**FEHLER \_ BEIM DS-SORTIERSTEUERSTEUERSTEUERT \_ NICHT \_ \_ VORHANDEN**
</dt> <dd> <dl> <dt>

8261 (0x2045)
</dt> <dt>



Die Suche erfordert ein SORT-Steuerelement.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OFFSET_RANGE_ERROR"></span><span id="error_ds_offset_range_error"></span>**\_FEHLER: \_ DS-OFFSETBEREICHSFEHLER \_ \_**
</dt> <dd> <dl> <dt>

8262 (0x2046)
</dt> <dt>



Die Suchergebnisse überschreiten den angegebenen Offsetbereich.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_RIDMGR_DISABLED"></span><span id="error_ds_ridmgr_disabled"></span>**FEHLER \_ DS \_ RIDMGR \_ DEAKTIVIERT**
</dt> <dd> <dl> <dt>

8263 (0x2047)
</dt> <dt>



Der Verzeichnisdienst hat festgestellt, dass das Subsystem, das relative Bezeichner zuteilt, deaktiviert ist. Dies kann als Schutzmechanismus auftreten, wenn das System feststellt, dass ein großer Teil der relativen Bezeichner (RIDs) erschöpft ist. Die <https://go.microsoft.com/fwlink/p/?linkid=228610> empfohlenen Diagnoseschritte und das Verfahren zum erneuten Aktivieren der Kontoerstellung finden Sie unter .


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ROOT_MUST_BE_NC"></span><span id="error_ds_root_must_be_nc"></span>**FEHLER \_ DS \_ ROOT MUSS NC \_ \_ \_ SEIN**
</dt> <dd> <dl> <dt>

8301 (0x206D)
</dt> <dt>



Das Stammobjekt muss der Kopf eines Namenskontexts sein. Das Stammobjekt darf kein instanziiertes übergeordnetes Objekt haben.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ADD_REPLICA_INHIBITED"></span><span id="error_ds_add_replica_inhibited"></span>**FEHLER \_ BEIM HINZUFÜGEN EINES \_ REPLIKATS \_ \_ IN DS**
</dt> <dd> <dl> <dt>

8302 (0x206E)
</dt> <dt>



Der Vorgang zum Hinzufügen eines Replikats kann nicht ausgeführt werden. Der Namenskontext muss schreibbar sein, um das Replikat zu erstellen.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ATT_NOT_DEF_IN_SCHEMA"></span><span id="error_ds_att_not_def_in_schema"></span>**FEHLER \_ DS \_ ATT \_ NICHT DEF \_ \_ IM \_ SCHEMA**
</dt> <dd> <dl> <dt>

8303 (0x206F)
</dt> <dt>



Ein Verweis auf ein Attribut, das nicht im Schema definiert ist, ist aufgetreten.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MAX_OBJ_SIZE_EXCEEDED"></span><span id="error_ds_max_obj_size_exceeded"></span>**FEHLER \_ DS \_ MAX \_ OBJ SIZE \_ \_ EXCEEDED**
</dt> <dd> <dl> <dt>

8304 (0x2070)
</dt> <dt>



Die maximale Größe eines Objekts wurde überschritten.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OBJ_STRING_NAME_EXISTS"></span><span id="error_ds_obj_string_name_exists"></span>**FEHLER \_ DS \_ OBJ \_ STRING NAME \_ \_ EXISTS**
</dt> <dd> <dl> <dt>

8305 (0x2071)
</dt> <dt>



Es wurde versucht, dem Verzeichnis ein Objekt mit einem Namen hinzuzufügen, der bereits verwendet wird.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_RDN_DEFINED_IN_SCHEMA"></span><span id="error_ds_no_rdn_defined_in_schema"></span>**FEHLER \_ DS \_ KEIN \_ RDN IM SCHEMA \_ \_ \_ DEFINIERT**
</dt> <dd> <dl> <dt>

8306 (0x2072)
</dt> <dt>



Es wurde versucht, ein Objekt einer Klasse hinzuzufügen, für die kein RDN im Schema definiert ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_RDN_DOESNT_MATCH_SCHEMA"></span><span id="error_ds_rdn_doesnt_match_schema"></span>**FEHLER \_ DS \_ RDN \_ ENTSPRICHT SCHEMA \_ \_ NICHT**
</dt> <dd> <dl> <dt>

8307 (0x2073)
</dt> <dt>



Es wurde versucht, ein Objekt mithilfe eines RDN hinzuzufügen, das nicht dem im Schema definierten RDN entspricht.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_REQUESTED_ATTS_FOUND"></span><span id="error_ds_no_requested_atts_found"></span>**FEHLER \_ DS \_ KEINE \_ ANGEFORDERTEN \_ ATTS \_ GEFUNDEN**
</dt> <dd> <dl> <dt>

8308 (0x2074)
</dt> <dt>



Keines der angeforderten Attribute wurde für die -Objekte gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_USER_BUFFER_TO_SMALL"></span><span id="error_ds_user_buffer_to_small"></span>**\_FEHLER: \_ DS-BENUTZERPUFFER \_ \_ AUF \_ KLEIN**
</dt> <dd> <dl> <dt>

8309 (0x2075)
</dt> <dt>



Der Benutzerpuffer ist zu klein.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ATT_IS_NOT_ON_OBJ"></span><span id="error_ds_att_is_not_on_obj"></span>**FEHLER \_ DS \_ ATT \_ IS NOT \_ \_ ON \_ OBJ**
</dt> <dd> <dl> <dt>

8310 (0x2076)
</dt> <dt>



Das im -Vorgang angegebene Attribut ist im -Objekt nicht vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ILLEGAL_MOD_OPERATION"></span><span id="error_ds_illegal_mod_operation"></span>**FEHLER: \_ UNGÜLTIGER \_ \_ DS-MOD-VORGANG \_**
</dt> <dd> <dl> <dt>

8311 (0x2077)
</dt> <dt>



Unzulässiger Änderungsvorgang. Ein Aspekt der Änderung ist nicht zulässig.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OBJ_TOO_LARGE"></span><span id="error_ds_obj_too_large"></span>**FEHLER \_ DS \_ OBJ \_ ZU \_ GROß**
</dt> <dd> <dl> <dt>

8312 (0x2078)
</dt> <dt>



Das angegebene Objekt ist zu groß.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_BAD_INSTANCE_TYPE"></span><span id="error_ds_bad_instance_type"></span>**FEHLER \_ DS – \_ \_ FEHLERHAFTER \_ INSTANZTYP**
</dt> <dd> <dl> <dt>

8313 (0x2079)
</dt> <dt>



Der angegebene Instanztyp ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MASTERDSA_REQUIRED"></span><span id="error_ds_masterdsa_required"></span>**FEHLER \_ DS \_ MASTERDSA \_ ERFORDERLICH**
</dt> <dd> <dl> <dt>

8314 (0x207A)
</dt> <dt>



Der Vorgang muss in einem Master-DSA ausgeführt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OBJECT_CLASS_REQUIRED"></span><span id="error_ds_object_class_required"></span>**FEHLER \_ \_ DS-OBJEKTKLASSE \_ \_ ERFORDERLICH**
</dt> <dd> <dl> <dt>

8315 (0x207B)
</dt> <dt>



Das Objektklassenattribut muss angegeben werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MISSING_REQUIRED_ATT"></span><span id="error_ds_missing_required_att"></span>**FEHLER \_ DS \_ FEHLENDER \_ \_ ERFORDERLICHER ATT**
</dt> <dd> <dl> <dt>

8316 (0x207C)
</dt> <dt>



Ein erforderliches Attribut fehlt.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ATT_NOT_DEF_FOR_CLASS"></span><span id="error_ds_att_not_def_for_class"></span>**FEHLER \_ DS \_ ATT \_ NOT DEF \_ \_ FOR \_ CLASS**
</dt> <dd> <dl> <dt>

8317 (0x207D)
</dt> <dt>



Es wurde versucht, ein Objekt so zu ändern, dass es ein Attribut enthält, das für seine Klasse nicht legal ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ATT_ALREADY_EXISTS"></span><span id="error_ds_att_already_exists"></span>**FEHLER \_ DS \_ ATT \_ IST BEREITS \_ VORHANDEN**
</dt> <dd> <dl> <dt>

8318 (0x207E)
</dt> <dt>



Das angegebene Attribut ist bereits im -Objekt vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_ADD_ATT_VALUES"></span><span id="error_ds_cant_add_att_values"></span>**FEHLER \_ DS \_ KANN KEINE \_ \_ ATT-WERTE \_ HINZUFÜGEN**
</dt> <dd> <dl> <dt>

8320 (0x2080)
</dt> <dt>



Das angegebene Attribut ist nicht vorhanden oder verfügt über keine Werte.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SINGLE_VALUE_CONSTRAINT"></span><span id="error_ds_single_value_constraint"></span>**\_FEHLER: \_ DS-EINSCHRÄNKUNG \_ FÜR EINEN EINZELNEN \_ WERT**
</dt> <dd> <dl> <dt>

8321 (0x2081)
</dt> <dt>



Für ein Attribut, das nur einen Wert haben kann, wurden mehrere Werte angegeben.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_RANGE_CONSTRAINT"></span><span id="error_ds_range_constraint"></span>**FEHLER \_ \_ DS-BEREICHSEINSCHRÄNKUNG \_**
</dt> <dd> <dl> <dt>

8322 (0x2082)
</dt> <dt>



Ein Wert für das Attribut lag nicht im zulässigen Wertebereich.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ATT_VAL_ALREADY_EXISTS"></span><span id="error_ds_att_val_already_exists"></span>**FEHLER \_ DS \_ ATT \_ VAL IST BEREITS \_ \_ VORHANDEN**
</dt> <dd> <dl> <dt>

8323 (0x2083)
</dt> <dt>



Der angegebene Wert ist bereits vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_REM_MISSING_ATT"></span><span id="error_ds_cant_rem_missing_att"></span>**FEHLER \_ DS \_ CANT \_ REM MISSING \_ \_ ATT**
</dt> <dd> <dl> <dt>

8324 (0x2084)
</dt> <dt>



Das Attribut kann nicht entfernt werden, da es im -Objekt nicht vorhanden ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_REM_MISSING_ATT_VAL"></span><span id="error_ds_cant_rem_missing_att_val"></span>**FEHLER \_ DS \_ CANT \_ REM MISSING \_ \_ ATT \_ VAL**
</dt> <dd> <dl> <dt>

8325 (0x2085)
</dt> <dt>



Der Attributwert kann nicht entfernt werden, da er im -Objekt nicht vorhanden ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ROOT_CANT_BE_SUBREF"></span><span id="error_ds_root_cant_be_subref"></span>**FEHLER \_ DS \_ ROOT \_ CANT BE \_ \_ SUBREF**
</dt> <dd> <dl> <dt>

8326 (0x2086)
</dt> <dt>



Das angegebene Stammobjekt darf keine Unterref sein.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_CHAINING"></span><span id="error_ds_no_chaining"></span>**FEHLER \_ DS \_ KEINE \_ VERKETTUNG**
</dt> <dd> <dl> <dt>

8327 (0x2087)
</dt> <dt>



Das Verketten ist nicht zulässig.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_CHAINED_EVAL"></span><span id="error_ds_no_chained_eval"></span>**FEHLER \_ DS \_ KEIN \_ VERKETTETER \_ EVAL**
</dt> <dd> <dl> <dt>

8328 (0x2088)
</dt> <dt>



Verkettete Auswertung ist nicht zulässig.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_PARENT_OBJECT"></span><span id="error_ds_no_parent_object"></span>**FEHLER \_ DS \_ KEIN \_ ÜBERGEORDNETES \_ OBJEKT**
</dt> <dd> <dl> <dt>

8329 (0x2089)
</dt> <dt>



Der Vorgang konnte nicht ausgeführt werden, da das übergeordnete Objekt instanziiert oder gelöscht wurde.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_PARENT_IS_AN_ALIAS"></span><span id="error_ds_parent_is_an_alias"></span>**FEHLER: \_ ÜBERGEORDNETES \_ DS-ELEMENT \_ IST EIN \_ \_ ALIAS**
</dt> <dd> <dl> <dt>

8330 (0x208A)
</dt> <dt>



Ein übergeordnetes Element, das ein Alias ist, ist nicht zulässig. Aliase sind Blattobjekte.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_MIX_MASTER_AND_REPS"></span><span id="error_ds_cant_mix_master_and_reps"></span>**FEHLER \_ DS \_ KANN MASTER UND \_ \_ \_ \_ REPS NICHT KOMBINIEREN**
</dt> <dd> <dl> <dt>

8331 (0x208B)
</dt> <dt>



Das Objekt und das übergeordnete Element müssen denselben Typ haben, entweder beide Master oder beide Replikate.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CHILDREN_EXIST"></span><span id="error_ds_children_exist"></span>**FEHLER: \_ DS \_ CHILDREN \_ EXIST**
</dt> <dd> <dl> <dt>

8332 (0x208C)
</dt> <dt>



Der Vorgang kann nicht ausgeführt werden, da untergeordnete Objekte vorhanden sind. Dieser Vorgang kann nur für ein Blattobjekt ausgeführt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OBJ_NOT_FOUND"></span><span id="error_ds_obj_not_found"></span>**FEHLER \_ DS \_ OBJ \_ NICHT \_ GEFUNDEN**
</dt> <dd> <dl> <dt>

8333 (0x208D)
</dt> <dt>



Verzeichnisobjekt nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ALIASED_OBJ_MISSING"></span><span id="error_ds_aliased_obj_missing"></span>**FEHLER \_ DS \_ ALIASED \_ OBJ \_ MISSING**
</dt> <dd> <dl> <dt>

8334 (0x208E)
</dt> <dt>



Das Aliasobjekt fehlt.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_BAD_NAME_SYNTAX"></span><span id="error_ds_bad_name_syntax"></span>**ERROR \_ DS \_ BAD \_ NAME \_ SYNTAX**
</dt> <dd> <dl> <dt>

8335 (0x208F)
</dt> <dt>



Der Objektname hat eine fehlerhafte Syntax.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ALIAS_POINTS_TO_ALIAS"></span><span id="error_ds_alias_points_to_alias"></span>**\_FEHLER: \_ DS-ALIAS \_ VERWEIST AUF \_ \_ ALIAS**
</dt> <dd> <dl> <dt>

8336 (0x2090)
</dt> <dt>



Ein Alias darf nicht auf einen anderen Alias verweisen.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_DEREF_ALIAS"></span><span id="error_ds_cant_deref_alias"></span>**FEHLER \_ DS \_ CANT \_ DEREF \_ ALIAS**
</dt> <dd> <dl> <dt>

8337 (0x2091)
</dt> <dt>



Der Alias kann nicht dereferenziert werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OUT_OF_SCOPE"></span><span id="error_ds_out_of_scope"></span>**FEHLER \_ "DS \_ OUT OF \_ \_ SCOPE"**
</dt> <dd> <dl> <dt>

8338 (0x2092)
</dt> <dt>



Der Vorgang liegt nicht im Gültigkeitsbereich.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OBJECT_BEING_REMOVED"></span><span id="error_ds_object_being_removed"></span>**FEHLER \_ BEIM ENTFERNEN DES DS-OBJEKTS \_ \_ \_**
</dt> <dd> <dl> <dt>

8339 (0x2093)
</dt> <dt>



Der Vorgang kann nicht fortgesetzt werden, da das Objekt gerade entfernt wird.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_DELETE_DSA_OBJ"></span><span id="error_ds_cant_delete_dsa_obj"></span>**FEHLER \_ DS \_ KANN \_ \_ DSA OBJ NICHT \_ LÖSCHEN**
</dt> <dd> <dl> <dt>

8340 (0x2094)
</dt> <dt>



Das DSA-Objekt kann nicht gelöscht werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_GENERIC_ERROR"></span><span id="error_ds_generic_error"></span>**FEHLER: \_ GENERISCHER \_ DS-FEHLER \_**
</dt> <dd> <dl> <dt>

8341 (0x2095)
</dt> <dt>



Ein Verzeichnisdienstfehler ist aufgetreten.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DSA_MUST_BE_INT_MASTER"></span><span id="error_ds_dsa_must_be_int_master"></span>**FEHLER: \_ DS \_ DSA \_ MUSS \_ \_ INT MASTER \_ SEIN**
</dt> <dd> <dl> <dt>

8342 (0x2096)
</dt> <dt>



Der Vorgang kann nur für ein internes DSA-Masterobjekt ausgeführt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CLASS_NOT_DSA"></span><span id="error_ds_class_not_dsa"></span>**FEHLER \_ \_ DS-KLASSE \_ NICHT \_ DSA**
</dt> <dd> <dl> <dt>

8343 (0x2097)
</dt> <dt>



Das Objekt muss der DSA-Klasse sein.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INSUFF_ACCESS_RIGHTS"></span><span id="error_ds_insuff_access_rights"></span>**FEHLER: \_ DS \_ INSUFF-ZUGRIFFSRECHTE \_ \_**
</dt> <dd> <dl> <dt>

8344 (0x2098)
</dt> <dt>



Unzureichende Zugriffsrechte zum Ausführen des Vorgangs.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ILLEGAL_SUPERIOR"></span><span id="error_ds_illegal_superior"></span>**FEHLER \_ DS \_ ILLEGAL \_ SUPERIOR**
</dt> <dd> <dl> <dt>

8345 (0x2099)
</dt> <dt>



Das -Objekt kann nicht hinzugefügt werden, da das übergeordnete Element nicht in der Liste der möglichen Übergeordneten aufgeführt ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ATTRIBUTE_OWNED_BY_SAM"></span><span id="error_ds_attribute_owned_by_sam"></span>**FEHLER \_ \_ DS-ATTRIBUT \_ IM BESITZ \_ VON \_ SAM**
</dt> <dd> <dl> <dt>

8346 (0x209A)
</dt> <dt>



Der Zugriff auf das Attribut ist nicht zulässig, da das Attribut im Besitz des Security Accounts Manager (SAM) ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_TOO_MANY_PARTS"></span><span id="error_ds_name_too_many_parts"></span>**\_FEHLER: \_ DS-NAME \_ ZU VIELE \_ \_ TEILE**
</dt> <dd> <dl> <dt>

8347 (0x209B)
</dt> <dt>



Der Name besteht zu viele Teile.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_TOO_LONG"></span><span id="error_ds_name_too_long"></span>**FEHLER \_ \_ DS-NAME \_ ZU \_ LANG**
</dt> <dd> <dl> <dt>

8348 (0x209C)
</dt> <dt>



Der Name ist zu lang.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_VALUE_TOO_LONG"></span><span id="error_ds_name_value_too_long"></span>**\_FEHLER: \_ DS-NAME-WERT \_ \_ ZU \_ LANG**
</dt> <dd> <dl> <dt>

8349 (0x209D)
</dt> <dt>



Der Name-Wert ist zu lang.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_UNPARSEABLE"></span><span id="error_ds_name_unparseable"></span>**FEHLER \_ DS \_ NAME \_ UNPARSEABLE**
</dt> <dd> <dl> <dt>

8350 (0x209E)
</dt> <dt>



Der Verzeichnisdienst hat beim Parsing eines Namens einen Fehler festgestellt.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_TYPE_UNKNOWN"></span><span id="error_ds_name_type_unknown"></span>**FEHLER \_ \_ DS-NAMENSTYP \_ \_ UNBEKANNT**
</dt> <dd> <dl> <dt>

8351 (0x209F)
</dt> <dt>



Der Verzeichnisdienst kann den Attributtyp für einen Namen nicht erhalten.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NOT_AN_OBJECT"></span><span id="error_ds_not_an_object"></span>**FEHLER \_ DS \_ KEIN \_ \_ OBJEKT**
</dt> <dd> <dl> <dt>

8352 (0x20A0)
</dt> <dt>



Der Name identifiziert kein Objekt. der Name identifiziert ein Phantom.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SEC_DESC_TOO_SHORT"></span><span id="error_ds_sec_desc_too_short"></span>**FEHLER \_ DS \_ SEC \_ DESC ZU \_ \_ KURZ**
</dt> <dd> <dl> <dt>

8353 (0x20A1)
</dt> <dt>



Die Sicherheitsbeschreibung ist zu kurz.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SEC_DESC_INVALID"></span><span id="error_ds_sec_desc_invalid"></span>**FEHLER \_ DS \_ SEC \_ DESC \_ UNGÜLTIG**
</dt> <dd> <dl> <dt>

8354 (0x20A2)
</dt> <dt>



Die Sicherheitsbeschreibung ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_DELETED_NAME"></span><span id="error_ds_no_deleted_name"></span>**FEHLER \_ DS \_ NO \_ DELETED \_ NAME**
</dt> <dd> <dl> <dt>

8355 (0x20A3)
</dt> <dt>



Fehler beim Erstellen des Namens für das gelöschte Objekt.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SUBREF_MUST_HAVE_PARENT"></span><span id="error_ds_subref_must_have_parent"></span>**FEHLER \_ \_ DS-UNTERREF \_ MUSS ÜBER \_ ÜBERGEORDNETES ELEMENT \_ VERFÜGEN**
</dt> <dd> <dl> <dt>

8356 (0x20A4)
</dt> <dt>



Das übergeordnete Element einer neuen Unterref muss vorhanden sein.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NCNAME_MUST_BE_NC"></span><span id="error_ds_ncname_must_be_nc"></span>**FEHLER \_ DS \_ NCNAME \_ MUSS NC \_ \_ SEIN**
</dt> <dd> <dl> <dt>

8357 (0x20A5)
</dt> <dt>



Das Objekt muss ein Namenskontext sein.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_ADD_SYSTEM_ONLY"></span><span id="error_ds_cant_add_system_only"></span>**FEHLER \_ DS \_ KANN NUR SYSTEM \_ \_ \_ HINZUFÜGEN**
</dt> <dd> <dl> <dt>

8358 (0x20A6)
</dt> <dt>



Es ist nicht zulässig, ein Attribut hinzuzufügen, das sich im Besitz des Systems befindet.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CLASS_MUST_BE_CONCRETE"></span><span id="error_ds_class_must_be_concrete"></span>**FEHLER \_ \_ DS-KLASSE \_ MUSS \_ KONKRETES \_ SEIN**
</dt> <dd> <dl> <dt>

8359 (0x20A7)
</dt> <dt>



Die Klasse des Objekts muss strukturell sein. Sie können keine abstrakte Klasse instanziieren.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INVALID_DMD"></span><span id="error_ds_invalid_dmd"></span>**FEHLER \_ DS \_ \_ UNGÜLTIGE DMD**
</dt> <dd> <dl> <dt>

8360 (0x20A8)
</dt> <dt>



Das Schemaobjekt wurde nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OBJ_GUID_EXISTS"></span><span id="error_ds_obj_guid_exists"></span>**FEHLER \_ DS \_ OBJ \_ GUID \_ VORHANDEN**
</dt> <dd> <dl> <dt>

8361 (0x20A9)
</dt> <dt>



Ein lokales Objekt mit dieser GUID (dead oder alive) ist bereits vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NOT_ON_BACKLINK"></span><span id="error_ds_not_on_backlink"></span>**FEHLER \_ "DS \_ NOT ON \_ \_ BACKLINK"**
</dt> <dd> <dl> <dt>

8362 (0x20AA)
</dt> <dt>



Der Vorgang kann nicht für einen Backlink ausgeführt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_CROSSREF_FOR_NC"></span><span id="error_ds_no_crossref_for_nc"></span>**FEHLER \_ DS \_ NO \_ CROSSREF FOR \_ \_ NC**
</dt> <dd> <dl> <dt>

8363 (0x20AB)
</dt> <dt>



Der Querverweis für den angegebenen Namenskontext wurde nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SHUTTING_DOWN"></span><span id="error_ds_shutting_down"></span>**FEHLER \_ BEIM \_ HERUNTERFAHREN VON DS \_**
</dt> <dd> <dl> <dt>

8364 (0x20AC)
</dt> <dt>



Der Vorgang konnte nicht ausgeführt werden, da der Verzeichnisdienst heruntergefahren wird.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_UNKNOWN_OPERATION"></span><span id="error_ds_unknown_operation"></span>**FEHLER \_ DS \_ UNBEKANNTER \_ VORGANG**
</dt> <dd> <dl> <dt>

8365 (0x20AD)
</dt> <dt>



Die Verzeichnisdienstanforderung ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INVALID_ROLE_OWNER"></span><span id="error_ds_invalid_role_owner"></span>**FEHLER \_ DS \_ UNGÜLTIGER \_ \_ ROLLENBESITZER**
</dt> <dd> <dl> <dt>

8366 (0x20AE)
</dt> <dt>



Das Rollenbesitzerattribut konnte nicht gelesen werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_COULDNT_CONTACT_FSMO"></span><span id="error_ds_couldnt_contact_fsmo"></span>**FEHLER: \_ DS \_ KONNTE \_ \_ FSMO NICHT KONTAKTIEREN**
</dt> <dd> <dl> <dt>

8367 (0x20AF)
</dt> <dt>



Der angeforderte FSMO-Vorgang konnte nicht ausgeführt werden. Der aktuelle FSMO-Inhaber war nicht erreichbar.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CROSS_NC_DN_RENAME"></span><span id="error_ds_cross_nc_dn_rename"></span>**\_FEHLER: \_ DS-NC-ÜBERGREIFENDE \_ \_ DN-UMBENENNUNG \_**
</dt> <dd> <dl> <dt>

8368 (0x20B0)
</dt> <dt>



Das Ändern eines DN in einem Namenskontext ist nicht zulässig.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_MOD_SYSTEM_ONLY"></span><span id="error_ds_cant_mod_system_only"></span>**FEHLER \_ DS \_ CANT \_ MOD SYSTEM \_ \_ ONLY**
</dt> <dd> <dl> <dt>

8369 (0x20B1)
</dt> <dt>



Das Attribut kann nicht geändert werden, da es im Besitz des Systems ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_REPLICATOR_ONLY"></span><span id="error_ds_replicator_only"></span>**FEHLER \_ NUR DS \_ REPLICATOR \_**
</dt> <dd> <dl> <dt>

8370 (0x20B2)
</dt> <dt>



Nur der Replikator kann diese Funktion ausführen.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OBJ_CLASS_NOT_DEFINED"></span><span id="error_ds_obj_class_not_defined"></span>**FEHLER \_ DS \_ \_ OBJ-KLASSE \_ NICHT \_ DEFINIERT**
</dt> <dd> <dl> <dt>

8371 (0x20B3)
</dt> <dt>



Die angegebene Klasse ist nicht definiert.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OBJ_CLASS_NOT_SUBCLASS"></span><span id="error_ds_obj_class_not_subclass"></span>**FEHLER \_ DS \_ \_ OBJ-KLASSE \_ NICHT \_ UNTERKLASSE**
</dt> <dd> <dl> <dt>

8372 (0x20B4)
</dt> <dt>



Die angegebene Klasse ist keine Unterklasse.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_REFERENCE_INVALID"></span><span id="error_ds_name_reference_invalid"></span>**FEHLER \_ \_ DS-NAMENSVERWEIS \_ \_ UNGÜLTIG**
</dt> <dd> <dl> <dt>

8373 (0x20B5)
</dt> <dt>



Der Namensverweis ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CROSS_REF_EXISTS"></span><span id="error_ds_cross_ref_exists"></span>**FEHLER \_ DS \_ CROSS REF \_ \_ EXISTS**
</dt> <dd> <dl> <dt>

8374 (0x20B6)
</dt> <dt>



Ein Querverweis ist bereits vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_DEL_MASTER_CROSSREF"></span><span id="error_ds_cant_del_master_crossref"></span>**FEHLER \_ DS \_ CANT \_ DEL MASTER \_ \_ CROSSREF**
</dt> <dd> <dl> <dt>

8375 (0x20B7)
</dt> <dt>



Es ist nicht zulässig, einen Master-Querverweis zu löschen.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SUBTREE_NOTIFY_NOT_NC_HEAD"></span><span id="error_ds_subtree_notify_not_nc_head"></span>**FEHLER \_ DS \_ SUBTREE \_ NOTIFY NOT NC \_ \_ \_ HEAD**
</dt> <dd> <dl> <dt>

8376 (0x20B8)
</dt> <dt>



Unterstrukturbenachrichtigungen werden nur auf NC-Kopf angezeigt.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NOTIFY_FILTER_TOO_COMPLEX"></span><span id="error_ds_notify_filter_too_complex"></span>**FEHLER \_ BEIM DS-BENACHRICHTIGUNGSFILTER \_ ZU \_ \_ \_ KOMPLEX**
</dt> <dd> <dl> <dt>

8377 (0x20B9)
</dt> <dt>



Der Benachrichtigungsfilter ist zu komplex.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DUP_RDN"></span><span id="error_ds_dup_rdn"></span>**FEHLER \_ DS \_ DUP \_ RDN**
</dt> <dd> <dl> <dt>

8378 (0x20BA)
</dt> <dt>



Fehler beim Schemaupdate: dupliziertes RDN.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DUP_OID"></span><span id="error_ds_dup_oid"></span>**\_FEHLER: \_ DS-DUP-OID \_**
</dt> <dd> <dl> <dt>

8379 (0x20BB)
</dt> <dt>



Fehler beim Schemaupdate: doppelte OID.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DUP_MAPI_ID"></span><span id="error_ds_dup_mapi_id"></span>**\_FEHLER: \_ DS-DUP-MAPI-ID \_ \_**
</dt> <dd> <dl> <dt>

8380 (0x20BC)
</dt> <dt>



Fehler beim Schemaupdate: Doppelter MAPI-Bezeichner.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DUP_SCHEMA_ID_GUID"></span><span id="error_ds_dup_schema_id_guid"></span>**\_FEHLER: \_ DS-DUP-SCHEMA-ID-GUID \_ \_ \_**
</dt> <dd> <dl> <dt>

8381 (0x20BD)
</dt> <dt>



Fehler beim Schemaupdate: Doppelte Schema-ID-GUID.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DUP_LDAP_DISPLAY_NAME"></span><span id="error_ds_dup_ldap_display_name"></span>**\_FEHLER: \_ DS-DUP-LDAP-ANZEIGENAME \_ \_ \_**
</dt> <dd> <dl> <dt>

8382 (0x20BE)
</dt> <dt>



Fehler beim Schemaupdate: Doppelter LDAP-Anzeigename.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SEMANTIC_ATT_TEST"></span><span id="error_ds_semantic_att_test"></span>**FEHLER \_ BEIM \_ DS-SEMANTISCHEN \_ \_ ATT-TEST**
</dt> <dd> <dl> <dt>

8383 (0x20BF)
</dt> <dt>



Fehler beim Schemaupdate: Bereich-kleiner als Bereich oben.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SYNTAX_MISMATCH"></span><span id="error_ds_syntax_mismatch"></span>**FEHLER: \_ NICHT ÜBEREINSTIMMENDE DS-SYNTAX \_ \_**
</dt> <dd> <dl> <dt>

8384 (0x20C0)
</dt> <dt>



Fehler beim Schemaupdate: Syntaxkonflikt.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_EXISTS_IN_MUST_HAVE"></span><span id="error_ds_exists_in_must_have"></span>**FEHLER \_ DS \_ IN MUSS \_ VORHANDEN \_ \_ SEIN**
</dt> <dd> <dl> <dt>

8385 (0x20C1)
</dt> <dt>



Fehler beim Löschen des Schemas: Das Attribut wird in must-contain verwendet.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_EXISTS_IN_MAY_HAVE"></span><span id="error_ds_exists_in_may_have"></span>**FEHLER \_ "DS \_ \_ EXISTS" IN \_ KANN \_ FOLGENDES HABEN:**
</dt> <dd> <dl> <dt>

8386 (0x20C2)
</dt> <dt>



Fehler beim Löschen des Schemas: Das Attribut wird in "may-contain" verwendet.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NONEXISTENT_MAY_HAVE"></span><span id="error_ds_nonexistent_may_have"></span>**FEHLER \_ "DS \_ NICHT VORHANDEN" HAT \_ MÖGLICHERWEISE \_**
</dt> <dd> <dl> <dt>

8387 (0x20C3)
</dt> <dt>



Fehler beim Schemaupdate: Das Attribut in may-contain ist nicht vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NONEXISTENT_MUST_HAVE"></span><span id="error_ds_nonexistent_must_have"></span>**FEHLER \_ "DS \_ NICHT VORHANDEN" \_ MUSS \_**
</dt> <dd> <dl> <dt>

8388 (0x20C4)
</dt> <dt>



Fehler beim Schemaupdate: Das Attribut in must-contain ist nicht vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_AUX_CLS_TEST_FAIL"></span><span id="error_ds_aux_cls_test_fail"></span>**FEHLER \_ BEIM DS \_ AUX \_ \_ CLS-TESTFEHLER \_**
</dt> <dd> <dl> <dt>

8389 (0x20C5)
</dt> <dt>



Fehler beim Schemaupdate: Die Klasse in der aux-Klassenliste ist nicht vorhanden oder ist keine Hilfsklasse.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NONEXISTENT_POSS_SUP"></span><span id="error_ds_nonexistent_poss_sup"></span>**FEHLER \_ DS \_ NONEXISTENT \_ POSS \_ SUP**
</dt> <dd> <dl> <dt>

8390 (0x20C6)
</dt> <dt>



Fehler beim Schemaupdate: Die Klasse in poss-superiors ist nicht vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SUB_CLS_TEST_FAIL"></span><span id="error_ds_sub_cls_test_fail"></span>**FEHLER \_ BEIM DS \_ SUB \_ \_ CLS-TESTFEHLER \_**
</dt> <dd> <dl> <dt>

8391 (0x20C7)
</dt> <dt>



Fehler beim Schemaupdate: Die Klasse in der Unterklasse der Liste ist nicht vorhanden oder erfüllt keine Hierarchieregeln.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_BAD_RDN_ATT_ID_SYNTAX"></span><span id="error_ds_bad_rdn_att_id_syntax"></span>**FEHLER \_ \_ DS: SYNTAX FÜR FEHLERHAFTE \_ \_ RDN-ATT-ID \_ \_**
</dt> <dd> <dl> <dt>

8392 (0x20C8)
</dt> <dt>



Fehler beim Schemaupdate: Rdn-Att-Id hat falsche Syntax.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_EXISTS_IN_AUX_CLS"></span><span id="error_ds_exists_in_aux_cls"></span>**FEHLER \_ "DS" \_ IST IN \_ \_ \_ AUX-CLS VORHANDEN**
</dt> <dd> <dl> <dt>

8393 (0x20C9)
</dt> <dt>



Fehler beim Löschen des Schemas: Die -Klasse wird als Hilfsklasse verwendet.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_EXISTS_IN_SUB_CLS"></span><span id="error_ds_exists_in_sub_cls"></span>**FEHLER \_ "DS" \_ IST IN \_ \_ \_ SUB-CLS VORHANDEN**
</dt> <dd> <dl> <dt>

8394 (0x20CA)
</dt> <dt>



Fehler beim Löschen des Schemas: Die -Klasse wird als Unterklasse verwendet.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_EXISTS_IN_POSS_SUP"></span><span id="error_ds_exists_in_poss_sup"></span>**FEHLER \_ DS \_ IST IN \_ \_ POSS SUP \_ VORHANDEN**
</dt> <dd> <dl> <dt>

8395 (0x20CB)
</dt> <dt>



Fehler beim Löschen des Schemas: Die -Klasse wird als poss-überlegen verwendet.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_RECALCSCHEMA_FAILED"></span><span id="error_ds_recalcschema_failed"></span>**FEHLER \_ BEI DS \_ RECALCSCHEMA \_**
</dt> <dd> <dl> <dt>

8396 (0x20CC)
</dt> <dt>



Fehler beim Schemaupdate beim Neuberechnen des Validierungscaches.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_TREE_DELETE_NOT_FINISHED"></span><span id="error_ds_tree_delete_not_finished"></span>**FEHLER \_ BEIM LÖSCHEN DER DS-STRUKTUR NICHT \_ \_ \_ \_ ABGESCHLOSSEN**
</dt> <dd> <dl> <dt>

8397 (0x20CD)
</dt> <dt>



Das Löschen der Struktur ist nicht abgeschlossen. Die Anforderung muss erneut gestellt werden, um mit dem Löschen der Struktur fortzufahren.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_DELETE"></span><span id="error_ds_cant_delete"></span>**FEHLER \_ DS \_ CANT \_ DELETE**
</dt> <dd> <dl> <dt>

8398 (0x20CE)
</dt> <dt>



Der angeforderte Löschvorgang konnte nicht ausgeführt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ATT_SCHEMA_REQ_ID"></span><span id="error_ds_att_schema_req_id"></span>**\_FEHLER: \_ DS \_ ATT-SCHEMA-REQ-ID \_ \_**
</dt> <dd> <dl> <dt>

8399 (0x20CF)
</dt> <dt>



Der Governs-Klassenbezeichner für den Schemadatensatz kann nicht gelesen werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_BAD_ATT_SCHEMA_SYNTAX"></span><span id="error_ds_bad_att_schema_syntax"></span>**FEHLER \_ \_ DS: FEHLERHAFTE \_ ATT-SCHEMASYNTAX \_ \_**
</dt> <dd> <dl> <dt>

8400 (0x20D0)
</dt> <dt>



Das Attributschema hat eine fehlerhafte Syntax.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_CACHE_ATT"></span><span id="error_ds_cant_cache_att"></span>**FEHLER \_ DS \_ CANT \_ CACHE \_ ATT**
</dt> <dd> <dl> <dt>

8401 (0x20D1)
</dt> <dt>



Das Attribut konnte nicht zwischengespeichert werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_CACHE_CLASS"></span><span id="error_ds_cant_cache_class"></span>**FEHLER \_ DS \_ CANT \_ \_ CACHE-KLASSE**
</dt> <dd> <dl> <dt>

8402 (0x20D2)
</dt> <dt>



Die -Klasse konnte nicht zwischengespeichert werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_REMOVE_ATT_CACHE"></span><span id="error_ds_cant_remove_att_cache"></span>**FEHLER: \_ DS \_ KANN \_ ATT CACHE \_ NICHT \_ ENTFERNEN**
</dt> <dd> <dl> <dt>

8403 (0x20D3)
</dt> <dt>



Das Attribut konnte nicht aus dem Cache entfernt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_REMOVE_CLASS_CACHE"></span><span id="error_ds_cant_remove_class_cache"></span>**FEHLER: \_ DS \_ KANN \_ KLASSENCACHE \_ NICHT \_ ENTFERNEN**
</dt> <dd> <dl> <dt>

8404 (0x20D4)
</dt> <dt>



Die -Klasse konnte nicht aus dem Cache entfernt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_RETRIEVE_DN"></span><span id="error_ds_cant_retrieve_dn"></span>**FEHLER: \_ DS \_ KANN \_ \_ DN NICHT ABRUFEN**
</dt> <dd> <dl> <dt>

8405 (0x20D5)
</dt> <dt>



Das Distinguished Name-Attribut konnte nicht gelesen werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MISSING_SUPREF"></span><span id="error_ds_missing_supref"></span>**FEHLER \_ DS \_ FEHLENDE \_ SUPREF**
</dt> <dd> <dl> <dt>

8406 (0x20D6)
</dt> <dt>



Im Verzeichnisdienst wurde kein übergeordneter Verweis konfiguriert. Der Verzeichnisdienst kann daher keine Verweise auf Objekte außerhalb dieser Gesamtstruktur aus geben.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_RETRIEVE_INSTANCE"></span><span id="error_ds_cant_retrieve_instance"></span>**FEHLER: \_ DS \_ CANT \_ RETRIEVE \_ INSTANCE**
</dt> <dd> <dl> <dt>

8407 (0x20D7)
</dt> <dt>



Das Instanztypattribut konnte nicht abgerufen werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CODE_INCONSISTENCY"></span><span id="error_ds_code_inconsistency"></span>**FEHLER \_ BEI \_ DS-CODEINKONSISTENZ \_**
</dt> <dd> <dl> <dt>

8408 (0x20D8)
</dt> <dt>



Ein interner Fehler ist aufgetreten.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DATABASE_ERROR"></span><span id="error_ds_database_error"></span>**FEHLER \_ \_ DS-DATENBANKFEHLER \_**
</dt> <dd> <dl> <dt>

8409 (0x20D9)
</dt> <dt>



Es ist ein Datenbankfehler aufgetreten.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_GOVERNSID_MISSING"></span><span id="error_ds_governsid_missing"></span>**FEHLER \_ DS \_ GOVERNSID \_ FEHLT**
</dt> <dd> <dl> <dt>

8410 (0x20DA)
</dt> <dt>



Das Attribut GOVERNSID fehlt.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MISSING_EXPECTED_ATT"></span><span id="error_ds_missing_expected_att"></span>**FEHLER \_ DS \_ FEHLT \_ \_ ERWARTETER ATT**
</dt> <dd> <dl> <dt>

8411 (0x20DB)
</dt> <dt>



Ein erwartetes Attribut fehlt.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NCNAME_MISSING_CR_REF"></span><span id="error_ds_ncname_missing_cr_ref"></span>**FEHLER \_ DS \_ NCNAME \_ MISSING CR \_ \_ REF**
</dt> <dd> <dl> <dt>

8412 (0x20DC)
</dt> <dt>



Im angegebenen Namenskontext fehlt ein Querverweis.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SECURITY_CHECKING_ERROR"></span><span id="error_ds_security_checking_error"></span>**FEHLER \_ BEI DS-SICHERHEITSÜBERPRÜFUNGSFEHLER \_ \_ \_**
</dt> <dd> <dl> <dt>

8413 (0x20DD)
</dt> <dt>



Es ist ein Sicherheitsüberprüfungsfehler aufgetreten.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SCHEMA_NOT_LOADED"></span><span id="error_ds_schema_not_loaded"></span>**\_FEHLER: \_ DS-SCHEMA \_ WURDE NICHT \_ GELADEN**
</dt> <dd> <dl> <dt>

8414 (0x20DE)
</dt> <dt>



Das Schema wird nicht geladen.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SCHEMA_ALLOC_FAILED"></span><span id="error_ds_schema_alloc_failed"></span>**FEHLER: \_ FEHLER BEIM ALLOC DES DS-SCHEMAS \_ \_ \_**
</dt> <dd> <dl> <dt>

8415 (0x20DF)
</dt> <dt>



Fehler bei der Schemazuordnung. Überprüfen Sie, ob auf dem Computer nicht genügend Arbeitsspeicher verfügbar ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ATT_SCHEMA_REQ_SYNTAX"></span><span id="error_ds_att_schema_req_syntax"></span>**FEHLER: \_ DS \_ \_ ATT-SCHEMA-REQ-SYNTAX \_ \_**
</dt> <dd> <dl> <dt>

8416 (0x20E0)
</dt> <dt>



Fehler beim Abrufen der erforderlichen Syntax für das Attributschema.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_GCVERIFY_ERROR"></span><span id="error_ds_gcverify_error"></span>**FEHLER: \_ DS \_ GCVERIFY-FEHLER \_**
</dt> <dd> <dl> <dt>

8417 (0x20E1)
</dt> <dt>



Fehler bei der globalen Katalogüberprüfung. Der globale Katalog ist nicht verfügbar oder unterstützt den Vorgang nicht. Ein Teil des Verzeichnisses ist derzeit nicht verfügbar.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_SCHEMA_MISMATCH"></span><span id="error_ds_dra_schema_mismatch"></span>**\_FEHLER: \_ DS-DRA-SCHEMAKONFLIKT \_ \_**
</dt> <dd> <dl> <dt>

8418 (0x20E2)
</dt> <dt>



Fehler beim Replikationsvorgang aufgrund eines Schemakonflikts zwischen den beteiligten Servern.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_FIND_DSA_OBJ"></span><span id="error_ds_cant_find_dsa_obj"></span>**FEHLER \_ DS \_ KANN \_ \_ DSA OBJ NICHT \_ FINDEN**
</dt> <dd> <dl> <dt>

8419 (0x20E3)
</dt> <dt>



Das DSA-Objekt wurde nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_FIND_EXPECTED_NC"></span><span id="error_ds_cant_find_expected_nc"></span>**FEHLER \_ DS \_ KANN ERWARTETEN NC \_ NICHT \_ \_ FINDEN**
</dt> <dd> <dl> <dt>

8420 (0x20E4)
</dt> <dt>



Der Namenskontext wurde nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_FIND_NC_IN_CACHE"></span><span id="error_ds_cant_find_nc_in_cache"></span>**FEHLER \_ DS \_ KANN NC NICHT IM CACHE \_ \_ \_ \_ FINDEN**
</dt> <dd> <dl> <dt>

8421 (0x20E5)
</dt> <dt>



Der Namenskontext konnte nicht im Cache gefunden werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_RETRIEVE_CHILD"></span><span id="error_ds_cant_retrieve_child"></span>**FEHLER \_ DS \_ CANT \_ RETRIEVE \_ CHILD**
</dt> <dd> <dl> <dt>

8422 (0x20E6)
</dt> <dt>



Das untergeordnete Objekt konnte nicht abgerufen werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SECURITY_ILLEGAL_MODIFY"></span><span id="error_ds_security_illegal_modify"></span>**FEHLER: \_ DS \_ SECURITY ILLEGAL \_ \_ MODIFY**
</dt> <dd> <dl> <dt>

8423 (0x20E7)
</dt> <dt>



Die Änderung war aus Sicherheitsgründen nicht zulässig.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_REPLACE_HIDDEN_REC"></span><span id="error_ds_cant_replace_hidden_rec"></span>**FEHLER \_ DS \_ KANN \_ AUSGEBLENDETES REC NICHT \_ \_ ERSETZEN**
</dt> <dd> <dl> <dt>

8424 (0x20E8)
</dt> <dt>



Der Vorgang kann den ausgeblendeten Datensatz nicht ersetzen.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_BAD_HIERARCHY_FILE"></span><span id="error_ds_bad_hierarchy_file"></span>**FEHLER \_ DS \_ : FEHLERHAFTE \_ \_ HIERARCHIEDATEI**
</dt> <dd> <dl> <dt>

8425 (0x20E9)
</dt> <dt>



Die Hierarchiedatei ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_BUILD_HIERARCHY_TABLE_FAILED"></span><span id="error_ds_build_hierarchy_table_failed"></span>**FEHLER: \_ FEHLER BEI DER \_ DS-BUILDHIERARCHIETABELLE \_ \_ \_**
</dt> <dd> <dl> <dt>

8426 (0x20EA)
</dt> <dt>



Fehler beim Erstellen der Hierarchietabelle.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CONFIG_PARAM_MISSING"></span><span id="error_ds_config_param_missing"></span>**\_FEHLER: \_ DS-KONFIGURATIONSPARAM \_ \_ FEHLT**
</dt> <dd> <dl> <dt>

8427 (0x20EB)
</dt> <dt>



Der Verzeichniskonfigurationsparameter fehlt in der Registrierung.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_COUNTING_AB_INDICES_FAILED"></span><span id="error_ds_counting_ab_indices_failed"></span>**FEHLER \_ BEI DER \_ DS-ZÄHLUNG \_ VON \_ AB-INDIZES \_**
</dt> <dd> <dl> <dt>

8428 (0x20EC)
</dt> <dt>



Fehler beim Zählen der Adressbuchindizes.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_HIERARCHY_TABLE_MALLOC_FAILED"></span><span id="error_ds_hierarchy_table_malloc_failed"></span>**FEHLER: \_ FEHLER BEI DER \_ DS-HIERARCHIETABELLE \_ \_ MALLOC \_**
</dt> <dd> <dl> <dt>

8429 (0x20ED)
</dt> <dt>



Fehler beim Zuweisen der Hierarchietabelle.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INTERNAL_FAILURE"></span><span id="error_ds_internal_failure"></span>**FEHLER \_ INTERNER \_ DS-FEHLER \_**
</dt> <dd> <dl> <dt>

8430 (0x20EE)
</dt> <dt>



Beim Verzeichnisdienst ist ein interner Fehler aufgetreten.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_UNKNOWN_ERROR"></span><span id="error_ds_unknown_error"></span>**FEHLER \_ DS \_ UNBEKANNTER \_ FEHLER**
</dt> <dd> <dl> <dt>

8431 (0x20EF)
</dt> <dt>



Der Verzeichnisdienst hat einen unbekannten Fehler festgestellt.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ROOT_REQUIRES_CLASS_TOP"></span><span id="error_ds_root_requires_class_top"></span>**\_FEHLER: \_ DS-STAMM \_ ERFORDERT KLASSE \_ \_ "TOP"**
</dt> <dd> <dl> <dt>

8432 (0x20F0)
</dt> <dt>



Ein Stammobjekt erfordert die Klasse "top".


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_REFUSING_FSMO_ROLES"></span><span id="error_ds_refusing_fsmo_roles"></span>**FEHLER \_ BEI \_ DS- UND \_ FSMO-ROLLEN \_**
</dt> <dd> <dl> <dt>

8433 (0x20F1)
</dt> <dt>



Dieser Verzeichnisserver wird heruntergefahren und kann keine neuen Gleitkomma-Einzelmaster-Vorgangsrollen übernehmen.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MISSING_FSMO_SETTINGS"></span><span id="error_ds_missing_fsmo_settings"></span>**FEHLER \_ DS \_ FEHLENDE \_ \_ FSMO-EINSTELLUNGEN**
</dt> <dd> <dl> <dt>

8434 (0x20F2)
</dt> <dt>



Dem Verzeichnisdienst fehlen obligatorische Konfigurationsinformationen, und der Besitz von Gleitkomma-Einzelmaster-Vorgangsrollen kann nicht bestimmt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_UNABLE_TO_SURRENDER_ROLES"></span><span id="error_ds_unable_to_surrender_roles"></span>**FEHLER \_ DS \_ KANN ROLLEN NICHT \_ \_ \_ VERTAUSCHEN**
</dt> <dd> <dl> <dt>

8435 (0x20F3)
</dt> <dt>



Der Verzeichnisdienst konnte den Besitz einer oder mehrerer gleitender Einzelmaster-Vorgangsrollen nicht auf andere Server übertragen.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_GENERIC"></span><span id="error_ds_dra_generic"></span>**FEHLER \_ DS \_ DRA \_ GENERIC**
</dt> <dd> <dl> <dt>

8436 (0x20F4)
</dt> <dt>



Fehler beim Replikationsvorgang.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_INVALID_PARAMETER"></span><span id="error_ds_dra_invalid_parameter"></span>**ERROR \_ DS \_ DRA \_ INVALID \_ PARAMETER**
</dt> <dd> <dl> <dt>

8437 (0x20F5)
</dt> <dt>



Für diesen Replikationsvorgang wurde ein ungültiger Parameter angegeben.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_BUSY"></span><span id="error_ds_dra_busy"></span>**FEHLER \_ \_ DS-DRA \_ AUSGELASTET**
</dt> <dd> <dl> <dt>

8438 (0x20F6)
</dt> <dt>



Der Verzeichnisdienst ist zu stark ausgelastet, um den Replikationsvorgang zu diesem Zeitpunkt abzuschließen.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_BAD_DN"></span><span id="error_ds_dra_bad_dn"></span>**FEHLER \_ DS \_ DRA \_ BAD \_ DN**
</dt> <dd> <dl> <dt>

8439 (0x20F7)
</dt> <dt>



Der für diesen Replikationsvorgang angegebene Distinguished Name ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_BAD_NC"></span><span id="error_ds_dra_bad_nc"></span>**FEHLER \_ DS \_ DRA \_ BAD \_ NC**
</dt> <dd> <dl> <dt>

8440 (0x20F8)
</dt> <dt>



Der für diesen Replikationsvorgang angegebene Namenskontext ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_DN_EXISTS"></span><span id="error_ds_dra_dn_exists"></span>**FEHLER \_ DS \_ DRA \_ DN \_ EXISTS**
</dt> <dd> <dl> <dt>

8441 (0x20F9)
</dt> <dt>



Der für diesen Replikationsvorgang angegebene Distinguished Name ist bereits vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_INTERNAL_ERROR"></span><span id="error_ds_dra_internal_error"></span>**INTERNER FEHLER DER \_ \_ DS-DRA \_ \_**
</dt> <dd> <dl> <dt>

8442 (0x20FA)
</dt> <dt>



Beim Replikationssystem ist ein interner Fehler aufgetreten.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_INCONSISTENT_DIT"></span><span id="error_ds_dra_inconsistent_dit"></span>**FEHLER \_ DS \_ DRA \_ INKONSISTENTE \_ DIT**
</dt> <dd> <dl> <dt>

8443 (0x20FB)
</dt> <dt>



Beim Replikationsvorgang ist eine Datenbankinkonsistenz aufgetreten.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_CONNECTION_FAILED"></span><span id="error_ds_dra_connection_failed"></span>**FEHLER \_ BEI DER \_ DS-DRA-VERBINDUNG \_ \_**
</dt> <dd> <dl> <dt>

8444 (0x20FC)
</dt> <dt>



Der für diesen Replikationsvorgang angegebene Server konnte nicht kontaktiert werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_BAD_INSTANCE_TYPE"></span><span id="error_ds_dra_bad_instance_type"></span>**ERROR \_ DS \_ DRA \_ BAD \_ INSTANCE \_ TYPE**
</dt> <dd> <dl> <dt>

8445 (0x20FD)
</dt> <dt>



Beim Replikationsvorgang wurde ein Objekt mit einem ungültigen Instanztyp gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_OUT_OF_MEM"></span><span id="error_ds_dra_out_of_mem"></span>**FEHLER \_ DS \_ DRA \_ OUT OF \_ \_ MEM**
</dt> <dd> <dl> <dt>

8446 (0x20FE)
</dt> <dt>



Beim Replikationsvorgang konnte kein Speicher belegt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_MAIL_PROBLEM"></span><span id="error_ds_dra_mail_problem"></span>**FEHLER \_ BEI \_ DS-DRA-E-MAIL-PROBLEM \_ \_**
</dt> <dd> <dl> <dt>

8447 (0x20FF)
</dt> <dt>



Beim Replikationsvorgang ist ein Fehler mit dem E-Mail-System aufgetreten.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_REF_ALREADY_EXISTS"></span><span id="error_ds_dra_ref_already_exists"></span>**\_FEHLER: \_ DS-DRA-REF \_ IST BEREITS \_ \_ VORHANDEN**
</dt> <dd> <dl> <dt>

8448 (0x2100)
</dt> <dt>



Die Replikationsverweisinformationen für den Zielserver sind bereits vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_REF_NOT_FOUND"></span><span id="error_ds_dra_ref_not_found"></span>**\_FEHLER: \_ DS-DRA-REF \_ \_ NICHT \_ GEFUNDEN**
</dt> <dd> <dl> <dt>

8449 (0x2101)
</dt> <dt>



Die Replikationsverweisinformationen für den Zielserver sind nicht vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_OBJ_IS_REP_SOURCE"></span><span id="error_ds_dra_obj_is_rep_source"></span>**FEHLER \_ DS \_ DRA \_ OBJ \_ IS REP \_ \_ SOURCE**
</dt> <dd> <dl> <dt>

8450 (0x2102)
</dt> <dt>



Der Namenskontext kann nicht entfernt werden, da er auf einen anderen Server repliziert wird.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_DB_ERROR"></span><span id="error_ds_dra_db_error"></span>**FEHLER \_ BEI \_ DS-DRA-DATENBANKFEHLER \_ \_**
</dt> <dd> <dl> <dt>

8451 (0x2103)
</dt> <dt>



Beim Replikationsvorgang ist ein Datenbankfehler aufgetreten.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_NO_REPLICA"></span><span id="error_ds_dra_no_replica"></span>**FEHLER \_ DS \_ DRA \_ NO \_ REPLICA**
</dt> <dd> <dl> <dt>

8452 (0x2104)
</dt> <dt>



Der Namenskontext wird gerade entfernt oder nicht vom angegebenen Server repliziert.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_ACCESS_DENIED"></span><span id="error_ds_dra_access_denied"></span>**FEHLER \_ DS \_ DRA \_ ACCESS \_ DENIED**
</dt> <dd> <dl> <dt>

8453 (0x2105)
</dt> <dt>



Der Replikationszugriff wurde verweigert.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_NOT_SUPPORTED"></span><span id="error_ds_dra_not_supported"></span>**FEHLER \_ \_ DS-DRA \_ WIRD NICHT \_ UNTERSTÜTZT**
</dt> <dd> <dl> <dt>

8454 (0x2106)
</dt> <dt>



Der angeforderte Vorgang wird von dieser Version des Verzeichnisdiensts nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_RPC_CANCELLED"></span><span id="error_ds_dra_rpc_cancelled"></span>**FEHLER \_ DS \_ DRA \_ RPC \_ CANCELLED**
</dt> <dd> <dl> <dt>

8455 (0x2107)
</dt> <dt>



Der Replikations-Remoteprozeduraufruf wurde abgebrochen.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_SOURCE_DISABLED"></span><span id="error_ds_dra_source_disabled"></span>**\_FEHLER: \_ DS-DRA-QUELLE \_ \_ DEAKTIVIERT**
</dt> <dd> <dl> <dt>

8456 (0x2108)
</dt> <dt>



Der Quellserver lehnt derzeit Replikationsanforderungen ab.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_SINK_DISABLED"></span><span id="error_ds_dra_sink_disabled"></span>**\_FEHLER: \_ DS-DRA-SENKE \_ \_ DEAKTIVIERT**
</dt> <dd> <dl> <dt>

8457 (0x2109)
</dt> <dt>



Der Zielserver lehnt derzeit Replikationsanforderungen ab.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_NAME_COLLISION"></span><span id="error_ds_dra_name_collision"></span>**FEHLER: \_ \_ \_ \_ DS-DRA-NAMENSKONFLIKT**
</dt> <dd> <dl> <dt>

8458 (0x210A)
</dt> <dt>



Der Replikationsvorgang ist aufgrund eines Konflikts von Objektnamen fehlgeschlagen.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_SOURCE_REINSTALLED"></span><span id="error_ds_dra_source_reinstalled"></span>**\_FEHLER: \_ DS-DRA-QUELLE \_ \_ NEU INSTALLIERT**
</dt> <dd> <dl> <dt>

8459 (0x210B)
</dt> <dt>



Die Replikationsquelle wurde neu installiert.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_MISSING_PARENT"></span><span id="error_ds_dra_missing_parent"></span>**FEHLER \_ BEI \_ FEHLENDEM ÜBERGEORDNETEM DSDRA-ELEMENT \_ \_**
</dt> <dd> <dl> <dt>

8460 (0x210C)
</dt> <dt>



Fehler beim Replikationsvorgang, weil ein erforderliches übergeordnetes Objekt fehlt.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_PREEMPTED"></span><span id="error_ds_dra_preempted"></span>**FEHLER \_ \_ DSDRA VORZEITIG \_ BEHOBEN**
</dt> <dd> <dl> <dt>

8461 (0x210D)
</dt> <dt>



Der Replikationsvorgang wurde vorzeitig beendet.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_ABANDON_SYNC"></span><span id="error_ds_dra_abandon_sync"></span>**FEHLER \_ DS \_ DRA \_ ABANDON \_ SYNC**
</dt> <dd> <dl> <dt>

8462 (0x210E)
</dt> <dt>



Der Replikationssynchronisierungsversuch wurde aufgrund fehlender Updates abgebrochen.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_SHUTDOWN"></span><span id="error_ds_dra_shutdown"></span>**FEHLER \_ DS \_ DRA \_ SHUTDOWN**
</dt> <dd> <dl> <dt>

8463 (0x210F)
</dt> <dt>



Der Replikationsvorgang wurde beendet, weil das System heruntergefahren wird.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_INCOMPATIBLE_PARTIAL_SET"></span><span id="error_ds_dra_incompatible_partial_set"></span>**FEHLER \_ \_ DSDRA \_ INKOMPATIBLE \_ \_ TEILMENGE**
</dt> <dd> <dl> <dt>

8464 (0x2110)
</dt> <dt>



Fehler beim Synchronisierungsversuch, weil der Zieldomänencontroller derzeit darauf wartet, neue Teilattribute aus der Quelle zu synchronisieren. Diese Bedingung ist normal, wenn eine kürzliche Schemaänderung den partiellen Attributsatz geändert hat. Der partielle Zielattributsatz ist keine Teilmenge des Quellteilattributsets.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_SOURCE_IS_PARTIAL_REPLICA"></span><span id="error_ds_dra_source_is_partial_replica"></span>**\_FEHLER: \_ DS-DRA-QUELLE \_ \_ IST \_ \_ TEILREPLIKAT**
</dt> <dd> <dl> <dt>

8465 (0x2111)
</dt> <dt>



Fehler beim Replikationssynchronisierungsversuch, weil ein Masterreplikat versucht hat, die Synchronisierung von einem teilreplikaten Replikat durchzuführen.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_EXTN_CONNECTION_FAILED"></span><span id="error_ds_dra_extn_connection_failed"></span>**FEHLER: \_ FEHLER BEI \_ DER DS DRA \_ \_ EXTN-VERBINDUNG \_**
</dt> <dd> <dl> <dt>

8466 (0x2112)
</dt> <dt>



Der für diesen Replikationsvorgang angegebene Server wurde kontaktiert, aber dieser Server konnte keinen zusätzlichen Server kontaktieren, der zum Abschließen des Vorgangs erforderlich ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INSTALL_SCHEMA_MISMATCH"></span><span id="error_ds_install_schema_mismatch"></span>**FEHLER: \_ NICHT \_ ÜBEREINSTIMMENDE DS-INSTALLATION \_ DES \_ SCHEMAS**
</dt> <dd> <dl> <dt>

8467 (0x2113)
</dt> <dt>



Die Version des Verzeichnisdienstschemas der Quellstruktur ist nicht mit der Version des Verzeichnisdiensts auf diesem Computer kompatibel.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DUP_LINK_ID"></span><span id="error_ds_dup_link_id"></span>**\_FEHLER: \_ DS-DUP-LINK-ID \_ \_**
</dt> <dd> <dl> <dt>

8468 (0x2114)
</dt> <dt>



Fehler beim Schemaupdate: Ein Attribut mit demselben Linkbezeichner ist bereits vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_ERROR_RESOLVING"></span><span id="error_ds_name_error_resolving"></span>**FEHLER \_ BEIM AUFLÖSEN DES DS-NAMENS \_ \_ \_**
</dt> <dd> <dl> <dt>

8469 (0x2115)
</dt> <dt>



Namensübersetzung: Generischer Verarbeitungsfehler.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_ERROR_NOT_FOUND"></span><span id="error_ds_name_error_not_found"></span>**FEHLER \_ DS NAME ERROR NOT FOUND (FEHLER BEIM DS-NAMEN \_ NICHT \_ \_ \_ GEFUNDEN)**
</dt> <dd> <dl> <dt>

8470 (0x2116)
</dt> <dt>



Namensübersetzung: Der Name wurde nicht oder nicht richtig zum Einsingen des Namens finden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_ERROR_NOT_UNIQUE"></span><span id="error_ds_name_error_not_unique"></span>**FEHLER \_ DS NAME ERROR NOT UNIQUE (FEHLER BEIM DS-NAMEN \_ NICHT \_ \_ \_ EINDEUTIG)**
</dt> <dd> <dl> <dt>

8471 (0x2117)
</dt> <dt>



Namensübersetzung: Eingabename, der mehr als einem Ausgabenamen zugeordnet ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_ERROR_NO_MAPPING"></span><span id="error_ds_name_error_no_mapping"></span>**FEHLER \_ \_ DS-NAME: \_ FEHLER KEINE \_ \_ ZUORDNUNG**
</dt> <dd> <dl> <dt>

8472 (0x2118)
</dt> <dt>



Namensübersetzung: Der Eingabename wurde gefunden, aber nicht das zugeordnete Ausgabeformat.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_ERROR_DOMAIN_ONLY"></span><span id="error_ds_name_error_domain_only"></span>**FEHLER \_ NUR \_ DS-NAMENSFEHLERDOMÄNE \_ \_ \_**
</dt> <dd> <dl> <dt>

8473 (0x2119)
</dt> <dt>



Namensübersetzung: Die Lösung kann nicht vollständig behoben werden, es wurde nur die Domäne gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_ERROR_NO_SYNTACTICAL_MAPPING"></span><span id="error_ds_name_error_no_syntactical_mapping"></span>**FEHLER \_ \_ DS-NAME: \_ FEHLER KEINE \_ \_ SYNTAKTISCHE \_ ZUORDNUNG**
</dt> <dd> <dl> <dt>

8474 (0x211A)
</dt> <dt>



Namensübersetzung: Es ist nicht möglich, eine rein syntaktische Zuordnung auf dem Client durchzuführen, ohne an das Netzwerk zu gehen.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CONSTRUCTED_ATT_MOD"></span><span id="error_ds_constructed_att_mod"></span>**FEHLER \_ DS \_ CONSTRUCTED \_ ATT \_ MOD**
</dt> <dd> <dl> <dt>

8475 (0x211B)
</dt> <dt>



Die Änderung eines konstruierten Attributs ist nicht zulässig.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_WRONG_OM_OBJ_CLASS"></span><span id="error_ds_wrong_om_obj_class"></span>**FEHLER \_ DS \_ FALSCHE OM \_ \_ OBJ-KLASSE \_**
</dt> <dd> <dl> <dt>

8476 (0x211C)
</dt> <dt>



Die angegebene OM-Object-Class ist für ein Attribut mit der angegebenen Syntax falsch.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_REPL_PENDING"></span><span id="error_ds_dra_repl_pending"></span>**FEHLER \_ DS \_ DRA \_ REPL \_ AUSSTEHEND**
</dt> <dd> <dl> <dt>

8477 (0x211D)
</dt> <dt>



Die Replikationsanforderung wurde gesendet. Warten auf Antwort.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DS_REQUIRED"></span><span id="error_ds_ds_required"></span>**FEHLER \_ DS \_ DS \_ ERFORDERLICH**
</dt> <dd> <dl> <dt>

8478 (0x211E)
</dt> <dt>



Für den angeforderten Vorgang ist ein Verzeichnisdienst erforderlich, und keiner war verfügbar.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INVALID_LDAP_DISPLAY_NAME"></span><span id="error_ds_invalid_ldap_display_name"></span>**FEHLER \_ DS \_ UNGÜLTIGER \_ \_ LDAP-ANZEIGENAME \_**
</dt> <dd> <dl> <dt>

8479 (0x211F)
</dt> <dt>



Der LDAP-Anzeigename der Klasse oder des Attributs enthält Nicht-ASCII-Zeichen.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NON_BASE_SEARCH"></span><span id="error_ds_non_base_search"></span>**FEHLER \_ \_ DS– NICHT \_ \_ BASISSUCHE**
</dt> <dd> <dl> <dt>

8480 (0x2120)
</dt> <dt>



Der angeforderte Suchvorgang wird nur für Basissuchen unterstützt.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_RETRIEVE_ATTS"></span><span id="error_ds_cant_retrieve_atts"></span>**FEHLER: \_ DS \_ KANN \_ \_ ATTS NICHT ABRUFEN**
</dt> <dd> <dl> <dt>

8481 (0x2121)
</dt> <dt>



Bei der Suche konnten keine Attribute aus der Datenbank abgerufen werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_BACKLINK_WITHOUT_LINK"></span><span id="error_ds_backlink_without_link"></span>**\_FEHLER: \_ DS-BACKLINK \_ OHNE \_ LINK**
</dt> <dd> <dl> <dt>

8482 (0x2122)
</dt> <dt>



Beim Schemaaktualisierungsvorgang wurde versucht, ein Attribut für eine Rückwärtsverknüpfung hinzuzufügen, das über keinen entsprechenden Vorwärtslink verfügt.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_EPOCH_MISMATCH"></span><span id="error_ds_epoch_mismatch"></span>**FEHLER \_ DS \_ EPOCH \_ MISMATCH**
</dt> <dd> <dl> <dt>

8483 (0x2123)
</dt> <dt>



Quelle und Ziel einer domänenübergreifenden Bewegung stimmen nicht mit der Epochennummer des Objekts überein. Quelle oder Ziel verfügen nicht über die neueste Version des Objekts.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SRC_NAME_MISMATCH"></span><span id="error_ds_src_name_mismatch"></span>**FEHLER: \_ NICHT \_ ÜBEREINSTIMMENDE DS-SRC-NAMEN \_ \_**
</dt> <dd> <dl> <dt>

8484 (0x2124)
</dt> <dt>



Quelle und Ziel einer domänenübergreifenden Bewegung stimmen nicht mit dem aktuellen Namen des Objekts überein. Quelle oder Ziel verfügen nicht über die neueste Version des Objekts.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SRC_AND_DST_NC_IDENTICAL"></span><span id="error_ds_src_and_dst_nc_identical"></span>**FEHLER \_ DS \_ SRC \_ UND \_ DST NC \_ \_ IDENTISCH**
</dt> <dd> <dl> <dt>

8485 (0x2125)
</dt> <dt>



Quelle und Ziel für den domänenübergreifenden Verschieben sind identisch. Der Aufrufer sollte den lokalen Move-Vorgang anstelle des domänenübergreifenden Verschiebens verwenden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DST_NC_MISMATCH"></span><span id="error_ds_dst_nc_mismatch"></span>**FEHLER \_ DS \_ DST NC \_ \_ MISMATCH**
</dt> <dd> <dl> <dt>

8486 (0x2126)
</dt> <dt>



Quelle und Ziel für eine domänenübergreifende Bewegung sind sich in den Benennungskontexten in der Gesamtstruktur nicht im Vertrag. Quelle oder Ziel verfügen nicht über die neueste Version des Partitionscontainers.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NOT_AUTHORITIVE_FOR_DST_NC"></span><span id="error_ds_not_authoritive_for_dst_nc"></span>**FEHLER \_ DS \_ NICHT \_ AUTORITATIV \_ FÜR \_ DST \_ NC**
</dt> <dd> <dl> <dt>

8487 (0x2127)
</dt> <dt>



Das Ziel einer domänenübergreifenden Bewegung ist für den Zielnamenskontext nicht autoritativ.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SRC_GUID_MISMATCH"></span><span id="error_ds_src_guid_mismatch"></span>**FEHLER: \_ NICHT ÜBEREINSTIMMENDE \_ DS-SRC-GUID \_ \_**
</dt> <dd> <dl> <dt>

8488 (0x2128)
</dt> <dt>



Quelle und Ziel einer domänenübergreifenden Bewegung stimmen nicht mit der Identität des Quellobjekts überein. Quelle oder Ziel verfügen nicht über die neueste Version des Quellobjekts.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_MOVE_DELETED_OBJECT"></span><span id="error_ds_cant_move_deleted_object"></span>**FEHLER: \_ DS \_ KANN \_ GELÖSCHTES \_ OBJEKT NICHT \_ VERSCHIEBEN**
</dt> <dd> <dl> <dt>

8489 (0x2129)
</dt> <dt>



Es ist bereits bekannt, dass das Objekt, das domänenübergreifend verschoben wird, vom Zielserver gelöscht wurde. Der Quellserver verfügt nicht über die neueste Version des Quellobjekts.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_PDC_OPERATION_IN_PROGRESS"></span><span id="error_ds_pdc_operation_in_progress"></span>**FEHLER \_ BEIM \_ DS-PDC-VORGANG \_ \_ WIRD \_ DURCHGEFÜHRT**
</dt> <dd> <dl> <dt>

8490 (0x212A)
</dt> <dt>



Ein weiterer Vorgang, der exklusiven Zugriff auf PDC FSMO erfordert, wird bereits durchgeführt.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CROSS_DOMAIN_CLEANUP_REQD"></span><span id="error_ds_cross_domain_cleanup_reqd"></span>**\_FEHLER: \_ \_ DOMÄNENÜBERGREIFENDER \_ BEREINIGUNGS-REQD \_**
</dt> <dd> <dl> <dt>

8491 (0x212B)
</dt> <dt>



Fehler beim domänenübergreifenden Verschieben, bei dem zwei Versionen des verschobenen Objekts vorhanden sind – jeweils eine in der Quell- und Zieldomäne. Das Zielobjekt muss entfernt werden, um den konsistenten Zustand des Systems wiederherzustellen.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ILLEGAL_XDOM_MOVE_OPERATION"></span><span id="error_ds_illegal_xdom_move_operation"></span>**FEHLER: \_ UNGÜLTIGER \_ \_ DS-XDOM-MOVE-VORGANG \_ \_**
</dt> <dd> <dl> <dt>

8492 (0x212C)
</dt> <dt>



Dieses Objekt kann nicht über Domänengrenzen verschoben werden, weil domänenübergreifende Verschiebebewegungen für diese Klasse nicht möglich sind oder das Objekt über einige besondere Merkmale verfügt, z. B. ein Vertrauenskonto oder eingeschränkte RID, die das Verschieben verhindern.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_WITH_ACCT_GROUP_MEMBERSHPS"></span><span id="error_ds_cant_with_acct_group_membershps"></span>**FEHLER \_ DS \_ CANT \_ WITH \_ ACCT GROUP \_ \_ MEMBERSHPS**
</dt> <dd> <dl> <dt>

8493 (0x212D)
</dt> <dt>



Objekte mit Mitgliedschaften können nicht wie nach dem Verschieben über Domänengrenzen hinweg verschoben werden. Dies würde die Mitgliedschaftsbedingungen der Kontogruppe verletzen. Entfernen Sie das -Objekt aus allen Kontogruppenmitgliedschaften, und wiederholen Sie den Vorgang.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NC_MUST_HAVE_NC_PARENT"></span><span id="error_ds_nc_must_have_nc_parent"></span>**FEHLER \_ DS \_ NC MUSS ÜBER \_ \_ \_ ÜBERGEORDNETES NC \_ VERFÜGEN**
</dt> <dd> <dl> <dt>

8494 (0x212E)
</dt> <dt>



Ein Benennungskontextkopf muss das unmittelbar untergeordnete Untergeordnete eines anderen Namenskontextkopfs sein, nicht eines inneren Knotens.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CR_IMPOSSIBLE_TO_VALIDATE"></span><span id="error_ds_cr_impossible_to_validate"></span>**FEHLER: \_ DS \_ CR KANN NICHT \_ ÜBERPRÜFT \_ \_ WERDEN**
</dt> <dd> <dl> <dt>

8495 (0x212F)
</dt> <dt>



Das Verzeichnis kann den vorgeschlagenen Namenskontextnamen nicht überprüfen, da es kein Replikat des Namenskontexts oberhalb des vorgeschlagenen Namenskontexts enthält. Stellen Sie sicher, dass die Masterrolle für Domänennamen von einem Server gehalten wird, der als globaler Katalogserver konfiguriert ist, und dass der Server mit seinen Replikationspartnern auf dem neuesten Stand ist. (Gilt nur für Windows 2000-Domänennamenmaster.)


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DST_DOMAIN_NOT_NATIVE"></span><span id="error_ds_dst_domain_not_native"></span>**FEHLER \_ DS \_ DST DOMAIN NOT NATIVE (DS-DST-DOMÄNE \_ NICHT \_ \_ NATIV)**
</dt> <dd> <dl> <dt>

8496 (0x2130)
</dt> <dt>



Die Zieldomäne muss sich im nativ-Modus befinden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MISSING_INFRASTRUCTURE_CONTAINER"></span><span id="error_ds_missing_infrastructure_container"></span>**FEHLER \_ DS \_ \_ FEHLENDER \_ INFRASTRUKTURCONTAINER**
</dt> <dd> <dl> <dt>

8497 (0x2131)
</dt> <dt>



Der Vorgang kann nicht ausgeführt werden, da der Server über keinen Infrastrukturcontainer in der für Sie wichtigen Domäne verfügt.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_MOVE_ACCOUNT_GROUP"></span><span id="error_ds_cant_move_account_group"></span>**FEHLER: \_ DS \_ KANN \_ KONTOGRUPPE \_ NICHT \_ VERSCHIEBEN**
</dt> <dd> <dl> <dt>

8498 (0x2132)
</dt> <dt>



Domänenübergreifendes Verschieben nicht leerer Kontogruppen ist nicht zulässig.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_MOVE_RESOURCE_GROUP"></span><span id="error_ds_cant_move_resource_group"></span>**FEHLER: \_ DS \_ KANN \_ RESSOURCENGRUPPE \_ NICHT \_ VERSCHIEBEN**
</dt> <dd> <dl> <dt>

8499 (0x2133)
</dt> <dt>



Domänenübergreifendes Verschieben nicht leerer Ressourcengruppen ist nicht zulässig.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INVALID_SEARCH_FLAG"></span><span id="error_ds_invalid_search_flag"></span>**FEHLER \_ DS \_ UNGÜLTIGES \_ \_ SUCHFLAG**
</dt> <dd> <dl> <dt>

8500 (0x2134)
</dt> <dt>



Die Suchflags für das Attribut sind ungültig. Das ANR-Bit ist nur für Attribute von Unicode- oder Teletex-Zeichenfolgen gültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_TREE_DELETE_ABOVE_NC"></span><span id="error_ds_no_tree_delete_above_nc"></span>**FEHLER \_ \_ DS: KEINE \_ \_ STRUKTURLÖSCHUNG \_ OBERHALB DES \_ NC**
</dt> <dd> <dl> <dt>

8501 (0x2135)
</dt> <dt>



Strukturlöschungen, die bei einem Objekt beginnen, das über einen NC-Kopf als Nachfolger verfügt, sind nicht zulässig.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_COULDNT_LOCK_TREE_FOR_DELETE"></span><span id="error_ds_couldnt_lock_tree_for_delete"></span>**FEHLER \_ DS \_ COULDNT \_ LOCK TREE FOR \_ \_ \_ DELETE**
</dt> <dd> <dl> <dt>

8502 (0x2136)
</dt> <dt>



Der Verzeichnisdienst konnte eine Struktur nicht sperren, um eine Struktur zu löschen, da die Struktur verwendet wurde.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_COULDNT_IDENTIFY_OBJECTS_FOR_TREE_DELETE"></span><span id="error_ds_couldnt_identify_objects_for_tree_delete"></span>**FEHLER \_ DS \_ COULDNT IDENTIFY \_ OBJECTS FOR TREE \_ \_ \_ \_ DELETE**
</dt> <dd> <dl> <dt>

8503 (0x2137)
</dt> <dt>



Beim Versuch, eine Struktur zu löschen, konnte der Verzeichnisdienst die Liste der zu löschenden Objekte nicht identifizieren.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SAM_INIT_FAILURE"></span><span id="error_ds_sam_init_failure"></span>**FEHLER \_ DS \_ SAM \_ INIT \_ FAILURE**
</dt> <dd> <dl> <dt>

8504 (0x2138)
</dt> <dt>



Fehler bei der Initialisierung des Sicherheitskonten-Managers aufgrund des folgenden Fehlers: %1. Fehlerstatus: 0x%2. Fahren Sie dieses System herunter, und starten Sie den Verzeichnisdienst-Wiederherstellungsmodus neu. Ausführlichere Informationen finden Sie im Ereignisprotokoll.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SENSITIVE_GROUP_VIOLATION"></span><span id="error_ds_sensitive_group_violation"></span>**FEHLER: \_ VERLETZUNG EINER \_ SENSIBLEN \_ DS-GRUPPE \_**
</dt> <dd> <dl> <dt>

8505 (0x2139)
</dt> <dt>



Nur ein Administrator kann die Mitgliedschaftsliste einer Administrativen Gruppe ändern.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_MOD_PRIMARYGROUPID"></span><span id="error_ds_cant_mod_primarygroupid"></span>**FEHLER \_ DS \_ CANT \_ MOD \_ PRIMARYGROUPID**
</dt> <dd> <dl> <dt>

8506 (0x213A)
</dt> <dt>



Die primäre Gruppen-ID eines Domänencontrollerkontos kann nicht geändert werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ILLEGAL_BASE_SCHEMA_MOD"></span><span id="error_ds_illegal_base_schema_mod"></span>**FEHLER: \_ DS \_ ILLEGAL BASE SCHEMA \_ \_ \_ MOD**
</dt> <dd> <dl> <dt>

8507 (0x213B)
</dt> <dt>



Es wird versucht, das Basisschema zu ändern.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NONSAFE_SCHEMA_CHANGE"></span><span id="error_ds_nonsafe_schema_change"></span>**FEHLER: \_ NICHT SICHERE SCHEMAÄNDERUNG FÜR DS \_ \_ \_**
</dt> <dd> <dl> <dt>

8508 (0x213C)
</dt> <dt>



Das Hinzufügen eines neuen obligatorischen Attributs zu einer vorhandenen Klasse, das Löschen eines obligatorischen Attributs aus einer vorhandenen Klasse oder das Hinzufügen eines optionalen Attributs zur speziellen Klasse Top, das kein Backlinkattribut ist (direkt oder durch Vererbung, z. B. durch Hinzufügen oder Löschen einer Hilfsklasse), ist nicht zulässig.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SCHEMA_UPDATE_DISALLOWED"></span><span id="error_ds_schema_update_disallowed"></span>**\_FEHLER: \_ DS-SCHEMAUPDATE \_ \_ NICHT VERFÜGBAR**
</dt> <dd> <dl> <dt>

8509 (0x213D)
</dt> <dt>



Schemaupdates sind auf diesem Domänencontroller nicht zulässig, da der Domänencontroller nicht der FSMO-Rollenbesitzer des Schemas ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_CREATE_UNDER_SCHEMA"></span><span id="error_ds_cant_create_under_schema"></span>**FEHLER \_ DS \_ KANN NICHT UNTER SCHEMA ERSTELLT \_ \_ \_ WERDEN**
</dt> <dd> <dl> <dt>

8510 (0x213E)
</dt> <dt>



Ein Objekt dieser Klasse kann nicht unter dem Schemacontainer erstellt werden. Sie können nur Attribute-Schema- und Klassenschemaobjekte unter dem Schemacontainer erstellen.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INSTALL_NO_SRC_SCH_VERSION"></span><span id="error_ds_install_no_src_sch_version"></span>**FEHLER \_ DS \_ INSTALL NO \_ \_ SRC SCH \_ \_ VERSION**
</dt> <dd> <dl> <dt>

8511 (0x213F)
</dt> <dt>



Bei der Replikat-/untergeordneten Installation konnte das objectVersion-Attribut für den Schemacontainer auf dem Quelldomänencontroller nicht erhalten werden. Entweder fehlt das Attribut im Schemacontainer, oder die angegebenen Anmeldeinformationen verfügen nicht über die Berechtigung zum Lesen.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INSTALL_NO_SCH_VERSION_IN_INIFILE"></span><span id="error_ds_install_no_sch_version_in_inifile"></span>**FEHLER \_ DS \_ INSTALL NO SCH VERSION IN \_ \_ \_ \_ \_ INIFILE**
</dt> <dd> <dl> <dt>

8512 (0x2140)
</dt> <dt>



Bei der Replikat-/untergeordneten Installation konnte das objectVersion-Attribut im Abschnitt SCHEMA der Datei schema.ini im Verzeichnis system32 nicht gelesen werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INVALID_GROUP_TYPE"></span><span id="error_ds_invalid_group_type"></span>**FEHLER \_ DS \_ UNGÜLTIGER \_ \_ GRUPPENTYP**
</dt> <dd> <dl> <dt>

8513 (0x2141)
</dt> <dt>



Der angegebene Gruppentyp ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_NEST_GLOBALGROUP_IN_MIXEDDOMAIN"></span><span id="error_ds_no_nest_globalgroup_in_mixeddomain"></span>**FEHLER \_ DS \_ NO NEST \_ \_ GLOBALGROUP IN \_ \_ MIXEDDOMAIN**
</dt> <dd> <dl> <dt>

8514 (0x2142)
</dt> <dt>



Globale Gruppen können nicht in einer gemischten Domäne geschachtelt werden, wenn die Gruppe sicherheits aktiviert ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_NEST_LOCALGROUP_IN_MIXEDDOMAIN"></span><span id="error_ds_no_nest_localgroup_in_mixeddomain"></span>**FEHLER \_ DS \_ NO NEST \_ \_ LOCALGROUP IN \_ \_ MIXEDDOMAIN**
</dt> <dd> <dl> <dt>

8515 (0x2143)
</dt> <dt>



Lokale Gruppen können nicht in einer gemischten Domäne geschachtelt werden, wenn die Gruppe sicherheitsgefädigend ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_GLOBAL_CANT_HAVE_LOCAL_MEMBER"></span><span id="error_ds_global_cant_have_local_member"></span>**FEHLER \_ DS \_ GLOBAL \_ CANT HAVE LOCAL \_ \_ \_ MEMBER**
</dt> <dd> <dl> <dt>

8516 (0x2144)
</dt> <dt>



Eine globale Gruppe darf keine lokale Gruppe als Mitglied haben.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_GLOBAL_CANT_HAVE_UNIVERSAL_MEMBER"></span><span id="error_ds_global_cant_have_universal_member"></span>**FEHLER \_ DS \_ GLOBAL \_ CANT HAVE UNIVERSAL \_ \_ \_ MEMBER**
</dt> <dd> <dl> <dt>

8517 (0x2145)
</dt> <dt>



Eine globale Gruppe darf keine universelle Gruppe als Mitglied haben.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_UNIVERSAL_CANT_HAVE_LOCAL_MEMBER"></span><span id="error_ds_universal_cant_have_local_member"></span>**FEHLER: \_ DS \_ UNIVERSAL KANN KEIN \_ \_ \_ LOKALES MITGLIED \_ HABEN**
</dt> <dd> <dl> <dt>

8518 (0x2146)
</dt> <dt>



Eine universelle Gruppe darf keine lokale Gruppe als Mitglied haben.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_GLOBAL_CANT_HAVE_CROSSDOMAIN_MEMBER"></span><span id="error_ds_global_cant_have_crossdomain_member"></span>**FEHLER \_ DS \_ GLOBAL \_ CANT HAVE \_ \_ CROSSDOMAIN \_ MEMBER**
</dt> <dd> <dl> <dt>

8519 (0x2147)
</dt> <dt>



Eine globale Gruppe darf kein domänenübergreifendes Mitglied haben.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_LOCAL_CANT_HAVE_CROSSDOMAIN_LOCAL_MEMBER"></span><span id="error_ds_local_cant_have_crossdomain_local_member"></span>**FEHLER \_ DS \_ LOCAL \_ CANT HAVE \_ \_ CROSSDOMAIN LOCAL \_ \_ MEMBER**
</dt> <dd> <dl> <dt>

8520 (0x2148)
</dt> <dt>



Eine lokale Gruppe darf keine andere domänenübergreifende lokale Gruppe als Mitglied haben.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_HAVE_PRIMARY_MEMBERS"></span><span id="error_ds_have_primary_members"></span>**FEHLER \_ DS \_ MIT PRIMÄREN \_ \_ MEMBERN**
</dt> <dd> <dl> <dt>

8521 (0x2149)
</dt> <dt>



Eine Gruppe mit primären Mitgliedern kann nicht in eine gruppe mit deaktivierter Sicherheit geändert werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_STRING_SD_CONVERSION_FAILED"></span><span id="error_ds_string_sd_conversion_failed"></span>**FEHLER BEI \_ DER KONVERTIERUNG DER DS STRING \_ \_ SD \_ \_**
</dt> <dd> <dl> <dt>

8522 (0x214A)
</dt> <dt>



Beim Laden des Schemacaches konnte die Zeichenfolgen-Standard-SD für ein Klassenschemaobjekt nicht konvertiert werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAMING_MASTER_GC"></span><span id="error_ds_naming_master_gc"></span>**FEHLER: \_ DS \_ NAMING MASTER \_ \_ GC**
</dt> <dd> <dl> <dt>

8523 (0x214B)
</dt> <dt>



Nur DSAs, die als globale Katalogserver konfiguriert sind, dürfen die FSMO-Rolle "Domänenbenennungsmaster" enthalten. (Gilt nur für Windows 2000 Server.)


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DNS_LOOKUP_FAILURE"></span><span id="error_ds_dns_lookup_failure"></span>**\_FEHLER: \_ DS-DNS-LOOKUPFEHLER \_ \_**
</dt> <dd> <dl> <dt>

8524 (0x214C)
</dt> <dt>



Der DSA-Vorgang kann aufgrund eines DNS-Suchfehlers nicht fortgesetzt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_COULDNT_UPDATE_SPNS"></span><span id="error_ds_couldnt_update_spns"></span>**FEHLER: \_ DS \_ KONNTE \_ \_ SPNS NICHT AKTUALISIEREN**
</dt> <dd> <dl> <dt>

8525 (0x214D)
</dt> <dt>



Beim Verarbeiten einer Änderung am DNS-Hostnamen für ein Objekt konnten die Werte des Dienstprinzipalnamens nicht synchron gehalten werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_RETRIEVE_SD"></span><span id="error_ds_cant_retrieve_sd"></span>**FEHLER: \_ DS \_ CANT \_ RETRIEVE \_ SD**
</dt> <dd> <dl> <dt>

8526 (0x214E)
</dt> <dt>



Das Security Descriptor-Attribut konnte nicht gelesen werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_KEY_NOT_UNIQUE"></span><span id="error_ds_key_not_unique"></span>**\_FEHLER: \_ DS-SCHLÜSSEL \_ NICHT \_ EINDEUTIG**
</dt> <dd> <dl> <dt>

8527 (0x214F)
</dt> <dt>



Das angeforderte Objekt wurde nicht gefunden, aber ein Objekt mit diesem Schlüssel wurde gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_WRONG_LINKED_ATT_SYNTAX"></span><span id="error_ds_wrong_linked_att_syntax"></span>**FEHLER \_ DS \_ FALSCHE \_ VERKNÜPFTE \_ \_ ATT-SYNTAX**
</dt> <dd> <dl> <dt>

8528 (0x2150)
</dt> <dt>



Die Syntax des hinzugefügten verknüpften Attributs ist falsch. Weiterleitungslinks können nur die Syntax 2.5.5.1, 2.5.5.7 und 2.5.5.14 aufweisen, und Backlinks können nur die Syntax 2.5.5.1 aufweisen.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SAM_NEED_BOOTKEY_PASSWORD"></span><span id="error_ds_sam_need_bootkey_password"></span>**FEHLER: \_ DS \_ SAM NEED \_ \_ BOOTKEY \_ PASSWORD**
</dt> <dd> <dl> <dt>

8529 (0x2151)
</dt> <dt>



Der Sicherheitskonto-Manager muss das Startkennwort abrufen.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SAM_NEED_BOOTKEY_FLOPPY"></span><span id="error_ds_sam_need_bootkey_floppy"></span>**FEHLER \_ DS \_ SAM NEED \_ \_ BOOTKEY \_ FLOPPY**
</dt> <dd> <dl> <dt>

8530 (0x2152)
</dt> <dt>



Der Sicherheitskonto-Manager muss den Startschlüssel von der Diskette abrufen.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_START"></span><span id="error_ds_cant_start"></span>**FEHLER \_ DS \_ CANT \_ START**
</dt> <dd> <dl> <dt>

8531 (0x2153)
</dt> <dt>



Der Verzeichnisdienst kann nicht gestartet werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INIT_FAILURE"></span><span id="error_ds_init_failure"></span>**FEHLER \_ DS \_ INIT \_ FAILURE**
</dt> <dd> <dl> <dt>

8532 (0x2154)
</dt> <dt>



Verzeichnisdienste konnten nicht gestartet werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_PKT_PRIVACY_ON_CONNECTION"></span><span id="error_ds_no_pkt_privacy_on_connection"></span>**FEHLER \_ DS \_ NO \_ PKT PRIVACY ON \_ \_ \_ CONNECTION**
</dt> <dd> <dl> <dt>

8533 (0x2155)
</dt> <dt>



Die Verbindung zwischen Client und Server erfordert Paketdatenschutz oder besser.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SOURCE_DOMAIN_IN_FOREST"></span><span id="error_ds_source_domain_in_forest"></span>**FEHLER \_ BEI DER \_ DS-QUELLDOMÄNE \_ \_ IN DER \_ GESAMTSTRUKTUR**
</dt> <dd> <dl> <dt>

8534 (0x2156)
</dt> <dt>



Die Quelldomäne befindet sich möglicherweise nicht in derselben Gesamtstruktur wie das Ziel.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DESTINATION_DOMAIN_NOT_IN_FOREST"></span><span id="error_ds_destination_domain_not_in_forest"></span>**FEHLER \_ \_ DS-ZIELDOMÄNE \_ NICHT IN \_ \_ \_ GESAMTSTRUKTUR**
</dt> <dd> <dl> <dt>

8535 (0x2157)
</dt> <dt>



Die Zieldomäne muss sich in der Gesamtstruktur befinden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DESTINATION_AUDITING_NOT_ENABLED"></span><span id="error_ds_destination_auditing_not_enabled"></span>**FEHLER \_ \_ DS-ZIELÜBERWACHUNG \_ \_ NICHT \_ AKTIVIERT**
</dt> <dd> <dl> <dt>

8536 (0x2158)
</dt> <dt>



Für den Vorgang muss die Überwachung der Zieldomäne aktiviert sein.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_FIND_DC_FOR_SRC_DOMAIN"></span><span id="error_ds_cant_find_dc_for_src_domain"></span>**FEHLER: \_ DS \_ KANN DC \_ FÜR \_ \_ \_ \_ SRC-DOMÄNE NICHT FINDEN**
</dt> <dd> <dl> <dt>

8537 (0x2159)
</dt> <dt>



Der Vorgang konnte keinen Domänencontroller für die Quelldomäne finden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SRC_OBJ_NOT_GROUP_OR_USER"></span><span id="error_ds_src_obj_not_group_or_user"></span>**FEHLER \_ DS \_ SRC \_ OBJ \_ NICHT GRUPPE \_ \_ ODER \_ BENUTZER**
</dt> <dd> <dl> <dt>

8538 (0x215A)
</dt> <dt>



Das Quellobjekt muss eine Gruppe oder ein Benutzer sein.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SRC_SID_EXISTS_IN_FOREST"></span><span id="error_ds_src_sid_exists_in_forest"></span>**\_FEHLER: \_ DS-SRC-SID \_ IST IN \_ \_ \_ GESAMTSTRUKTUR VORHANDEN**
</dt> <dd> <dl> <dt>

8539 (0x215B)
</dt> <dt>



Die SID des Quellobjekts ist bereits in der Zielstruktur vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SRC_AND_DST_OBJECT_CLASS_MISMATCH"></span><span id="error_ds_src_and_dst_object_class_mismatch"></span>**ERROR \_ DS \_ SRC \_ AND \_ DST \_ OBJECT \_ CLASS \_ MISMATCH**
</dt> <dd> <dl> <dt>

8540 (0x215C)
</dt> <dt>



Quell- und Zielobjekt müssen denselben Typ aufweisen.


</dt> </dl> </dd> <dt>

<span id="ERROR_SAM_INIT_FAILURE"></span><span id="error_sam_init_failure"></span>**FEHLER \_ BEIM \_ SAM-INIT-FEHLER \_**
</dt> <dd> <dl> <dt>

8541 (0x215D)
</dt> <dt>



Fehler bei der Initialisierung des Sicherheitskonten-Managers aufgrund des folgenden Fehlers: %1. Fehlerstatus: 0x%2. Klicken Sie auf OK, um das System herunterzufahren und in Tresor Modus neu zu starten. Ausführliche Informationen finden Sie im Ereignisprotokoll.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_SCHEMA_INFO_SHIP"></span><span id="error_ds_dra_schema_info_ship"></span>**ERROR \_ DS \_ DRA \_ SCHEMA \_ INFO \_ SHIP**
</dt> <dd> <dl> <dt>

8542 (0x215E)
</dt> <dt>



Schemainformationen konnten nicht in die Replikationsanforderung eingeschlossen werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_SCHEMA_CONFLICT"></span><span id="error_ds_dra_schema_conflict"></span>**ERROR \_ DS \_ DRA \_ SCHEMA \_ CONFLICT**
</dt> <dd> <dl> <dt>

8543 (0x215F)
</dt> <dt>



Der Replikationsvorgang konnte aufgrund einer Schemainkompatibilität nicht abgeschlossen werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_EARLIER_SCHEMA_CONFLICT"></span><span id="error_ds_dra_earlier_schema_conflict"></span>**ERROR \_ DS \_ DRA \_ EARLIER \_ SCHEMA \_ CONFLICT**
</dt> <dd> <dl> <dt>

8544 (0x2160)
</dt> <dt>



Der Replikationsvorgang konnte aufgrund einer früheren Schemainkompatibilität nicht abgeschlossen werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_OBJ_NC_MISMATCH"></span><span id="error_ds_dra_obj_nc_mismatch"></span>**FEHLER \_ DS \_ DRA \_ OBJ \_ NC \_ MISMATCH**
</dt> <dd> <dl> <dt>

8545 (0x2161)
</dt> <dt>



Das Replikationsupdate konnte nicht angewendet werden, da entweder die Quelle oder das Ziel noch keine Informationen zu einem kürzlichen domänenübergreifenden Verschiebevorgang erhalten hat.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NC_STILL_HAS_DSAS"></span><span id="error_ds_nc_still_has_dsas"></span>**FEHLER \_ DS \_ NC WEIST WEITERHIN \_ \_ \_ DSAS AUF**
</dt> <dd> <dl> <dt>

8546 (0x2162)
</dt> <dt>



Die angeforderte Domäne konnte nicht gelöscht werden, da noch Domänencontroller vorhanden sind, die diese Domäne hosten.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_GC_REQUIRED"></span><span id="error_ds_gc_required"></span>**FEHLER \_ BEI DER \_ DS-GC \_ ERFORDERLICH**
</dt> <dd> <dl> <dt>

8547 (0x2163)
</dt> <dt>



Der angeforderte Vorgang kann nur auf einem globalen Katalogserver ausgeführt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_LOCAL_MEMBER_OF_LOCAL_ONLY"></span><span id="error_ds_local_member_of_local_only"></span>**FEHLER \_ DS \_ LOCAL MEMBER OF LOCAL \_ \_ \_ \_ ONLY**
</dt> <dd> <dl> <dt>

8548 (0x2164)
</dt> <dt>



Eine lokale Gruppe kann nur Mitglied anderer lokaler Gruppen in derselben Domäne sein.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_FPO_IN_UNIVERSAL_GROUPS"></span><span id="error_ds_no_fpo_in_universal_groups"></span>**FEHLER \_ DS \_ NO \_ FPO IN UNIVERSAL \_ \_ \_ GROUPS**
</dt> <dd> <dl> <dt>

8549 (0x2165)
</dt> <dt>



Fremdsicherheitsprinzipale dürfen keine Mitglieder universeller Gruppen sein.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_ADD_TO_GC"></span><span id="error_ds_cant_add_to_gc"></span>**FEHLER \_ DS \_ CANT \_ ADD TO \_ \_ GC**
</dt> <dd> <dl> <dt>

8550 (0x2166)
</dt> <dt>



Das Attribut kann aus Sicherheitsgründen nicht in die GC repliziert werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_CHECKPOINT_WITH_PDC"></span><span id="error_ds_no_checkpoint_with_pdc"></span>**FEHLER \_ DS \_ KEIN \_ PRÜFPUNKT MIT \_ \_ PDC**
</dt> <dd> <dl> <dt>

8551 (0x2167)
</dt> <dt>



Der Prüfpunkt mit dem PDC konnte nicht verwendet werden, da derzeit zu viele Änderungen verarbeitet werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SOURCE_AUDITING_NOT_ENABLED"></span><span id="error_ds_source_auditing_not_enabled"></span>**\_FEHLER: \_ DS-QUELLÜBERWACHUNG \_ \_ NICHT \_ AKTIVIERT**
</dt> <dd> <dl> <dt>

8552 (0x2168)
</dt> <dt>



Für den Vorgang muss die Überwachung der Quelldomäne aktiviert sein.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_CREATE_IN_NONDOMAIN_NC"></span><span id="error_ds_cant_create_in_nondomain_nc"></span>**FEHLER \_ DS \_ CANT \_ CREATE IN \_ \_ NONDOMAIN \_ NC**
</dt> <dd> <dl> <dt>

8553 (0x2169)
</dt> <dt>



Sicherheitsprinzipalobjekte können nur innerhalb von Domänennamenskontexten erstellt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INVALID_NAME_FOR_SPN"></span><span id="error_ds_invalid_name_for_spn"></span>**FEHLER \_ DS \_ UNGÜLTIGER \_ NAME FÜR \_ \_ SPN**
</dt> <dd> <dl> <dt>

8554 (0x216A)
</dt> <dt>



Ein Dienstprinzipalname (Service Principal Name, SPN) konnte nicht erstellt werden, da der angegebene Hostname nicht im erforderlichen Format vorliegt.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_FILTER_USES_CONTRUCTED_ATTRS"></span><span id="error_ds_filter_uses_contructed_attrs"></span>**\_FEHLER-DS-FILTER \_ \_ VERWENDET \_ CONTRUCTED \_ ATTRS**
</dt> <dd> <dl> <dt>

8555 (0x216B)
</dt> <dt>



Ein Filter wurde übergeben, der konstruierte Attribute verwendet.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_UNICODEPWD_NOT_IN_QUOTES"></span><span id="error_ds_unicodepwd_not_in_quotes"></span>**FEHLER \_ DS \_ UNICODEPWD \_ NICHT IN \_ \_ ANFÜHRUNGSZEICHEN**
</dt> <dd> <dl> <dt>

8556 (0x216C)
</dt> <dt>



Der UnicodePwd-Attributwert muss in doppelte Anführungszeichen eingeschlossen werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MACHINE_ACCOUNT_QUOTA_EXCEEDED"></span><span id="error_ds_machine_account_quota_exceeded"></span>**FEHLER: \_ \_ DS-COMPUTERKONTOKONTINGENT \_ \_ \_ ÜBERSCHRITTEN**
</dt> <dd> <dl> <dt>

8557 (0x216D)
</dt> <dt>



Ihr Computer konnte nicht in die Domäne eingebunden werden. Sie haben die maximale Anzahl von Computerkonten überschritten, die Sie in dieser Domäne erstellen dürfen. Wenden Sie sich an Ihren Systemadministrator, um dieses Limit zurückzusetzen oder zu erhöhen.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MUST_BE_RUN_ON_DST_DC"></span><span id="error_ds_must_be_run_on_dst_dc"></span>**FEHLER \_ DS \_ MUSS AUF \_ \_ \_ \_ \_ DST-DC AUSGEFÜHRT WERDEN**
</dt> <dd> <dl> <dt>

8558 (0x216E)
</dt> <dt>



Aus Sicherheitsgründen muss der Vorgang auf dem Zieldomänencontroller ausgeführt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SRC_DC_MUST_BE_SP4_OR_GREATER"></span><span id="error_ds_src_dc_must_be_sp4_or_greater"></span>**FEHLER \_ DS \_ SRC \_ DC MUSS \_ \_ \_ SP4 ODER \_ \_ GRÖßER SEIN**
</dt> <dd> <dl> <dt>

8559 (0x216F)
</dt> <dt>



Aus Sicherheitsgründen muss der Quelldomänencontroller NT4SP4 oder höher sein.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_TREE_DELETE_CRITICAL_OBJ"></span><span id="error_ds_cant_tree_delete_critical_obj"></span>**FEHLER: \_ DS \_ CANT \_ TREE DELETE \_ CRITICAL \_ \_ OBJ**
</dt> <dd> <dl> <dt>

8560 (0x2170)
</dt> <dt>



Kritische Directory Service System-Objekte können während Strukturlöschvorgängen nicht gelöscht werden. Das Löschen der Struktur wurde möglicherweise teilweise durchgeführt.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INIT_FAILURE_CONSOLE"></span><span id="error_ds_init_failure_console"></span>**\_ \_ FEHLER-DS-INIT-FEHLERKONSOLE \_ \_**
</dt> <dd> <dl> <dt>

8561 (0x2171)
</dt> <dt>



Verzeichnisdienste konnten aufgrund des folgenden Fehlers nicht gestartet werden: %1. Fehlerstatus: 0x%2. Klicken Sie auf OK, um das System herunterzufahren. Zur weiteren Systemdiagnose können Sie die Wiederherstellungskonsole verwenden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SAM_INIT_FAILURE_CONSOLE"></span><span id="error_ds_sam_init_failure_console"></span>**ERROR \_ DS \_ SAM \_ INIT \_ FAILURE \_ CONSOLE**
</dt> <dd> <dl> <dt>

8562 (0x2172)
</dt> <dt>



Fehler bei der Initialisierung des Sicherheitskonten-Managers aufgrund des folgenden Fehlers: %1. Fehlerstatus: 0x%2. Klicken Sie auf OK, um das System herunterzufahren. Zur weiteren Systemdiagnose können Sie die Wiederherstellungskonsole verwenden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_FOREST_VERSION_TOO_HIGH"></span><span id="error_ds_forest_version_too_high"></span>**FEHLER: \_ \_ \_ DS-GESAMTSTRUKTURVERSION \_ ZU \_ HOCH**
</dt> <dd> <dl> <dt>

8563 (0x2173)
</dt> <dt>



Die Version des Betriebssystems ist mit der aktuellen AD DS Gesamtstrukturfunktionsebene oder AD LDS Configuration Set-Funktionsebene nicht kompatibel. Sie müssen ein Upgrade auf eine neue Version des Betriebssystems durchführen, bevor dieser Server ein AD DS Domänencontroller werden oder eine AD LDS-Instanz in dieser AD DS Gesamtstruktur oder AD LDS Konfigurationssatz hinzufügen kann.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DOMAIN_VERSION_TOO_HIGH"></span><span id="error_ds_domain_version_too_high"></span>**FEHLER BEI \_ \_ \_ DS-DOMÄNENVERSION \_ ZU \_ HOCH**
</dt> <dd> <dl> <dt>

8564 (0x2174)
</dt> <dt>



Die Version des installierten Betriebssystems ist mit der aktuellen Domänenfunktionsebene nicht kompatibel. Sie müssen ein Upgrade auf eine neue Version des Betriebssystems durchführen, bevor dieser Server zu einem Domänencontroller in dieser Domäne werden kann.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_FOREST_VERSION_TOO_LOW"></span><span id="error_ds_forest_version_too_low"></span>**FEHLER: \_ \_ \_ DS-GESAMTSTRUKTURVERSION \_ ZU \_ NIEDRIG**
</dt> <dd> <dl> <dt>

8565 (0x2175)
</dt> <dt>



Die auf diesem Server installierte Version des Betriebssystems unterstützt nicht mehr die aktuelle Funktionsebene AD DS Gesamtstruktur oder AD LDS Funktionsebene des Konfigurationssatzes. Sie müssen die Funktionsebene AD DS Gesamtstruktur oder AD LDS-Konfigurationssatz erhöhen, bevor dieser Server zu einem AD DS-Domänencontroller oder einer AD LDS-Instanz in dieser Gesamtstruktur oder Konfigurationsmenge werden kann.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DOMAIN_VERSION_TOO_LOW"></span><span id="error_ds_domain_version_too_low"></span>**FEHLER: \_ \_ DS-DOMÄNENVERSION \_ \_ ZU \_ NIEDRIG**
</dt> <dd> <dl> <dt>

8566 (0x2176)
</dt> <dt>



Die auf diesem Server installierte Version des Betriebssystems unterstützt die aktuelle Domänenfunktionsebene nicht mehr. Sie müssen die Domänenfunktionsebene heraufstufen, bevor dieser Server zu einem Domänencontroller in dieser Domäne werden kann.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INCOMPATIBLE_VERSION"></span><span id="error_ds_incompatible_version"></span>**FEHLER \_ DS \_ INKOMPATIBLE \_ VERSION**
</dt> <dd> <dl> <dt>

8567 (0x2177)
</dt> <dt>



Die auf diesem Server installierte Version des Betriebssystems ist mit der Funktionsebene der Domäne oder Gesamtstruktur nicht kompatibel.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_LOW_DSA_VERSION"></span><span id="error_ds_low_dsa_version"></span>**FEHLER \_ DS \_ LOW \_ DSA \_ VERSION**
</dt> <dd> <dl> <dt>

8568 (0x2178)
</dt> <dt>



Die Funktionsebene der Domäne (oder Gesamtstruktur) kann nicht auf den angeforderten Wert erhöht werden, da mindestens ein Domänencontroller in der Domäne (oder Gesamtstruktur) auf einer niedrigeren inkompatiblen Funktionsebene vorhanden ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_BEHAVIOR_VERSION_IN_MIXEDDOMAIN"></span><span id="error_ds_no_behavior_version_in_mixeddomain"></span>**FEHLER \_ \_ DS: KEINE \_ \_ VERHALTENSVERSION IN \_ \_ MIXEDDOMAIN**
</dt> <dd> <dl> <dt>

8569 (0x2179)
</dt> <dt>



Die Gesamtstrukturfunktionsebene kann nicht auf den angeforderten Wert erhöht werden, da sich mindestens eine Domäne noch im gemischten Domänenmodus befindet. Alle Domänen in der Gesamtstruktur müssen sich im einheitlichen Modus befinden, damit Sie die Gesamtstrukturfunktionsebene erhöhen können.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NOT_SUPPORTED_SORT_ORDER"></span><span id="error_ds_not_supported_sort_order"></span>**FEHLER \_ DS \_ NICHT UNTERSTÜTZTE \_ \_ \_ SORTIERREIHENFOLGE**
</dt> <dd> <dl> <dt>

8570 (0x217A)
</dt> <dt>



Die angeforderte Sortierreihenfolge wird nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_NOT_UNIQUE"></span><span id="error_ds_name_not_unique"></span>**\_FEHLER: \_ DS-NAME \_ NICHT \_ EINDEUTIG**
</dt> <dd> <dl> <dt>

8571 (0x217B)
</dt> <dt>



Der angeforderte Name ist bereits als eindeutiger Bezeichner vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MACHINE_ACCOUNT_CREATED_PRENT4"></span><span id="error_ds_machine_account_created_prent4"></span>**\_FEHLER: \_ DS-COMPUTERKONTO \_ \_ ERSTELLT \_ PRENT4**
</dt> <dd> <dl> <dt>

8572 (0x217C)
</dt> <dt>



Das Computerkonto wurde vor NT4 erstellt. Das Konto muss neu erstellt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OUT_OF_VERSION_STORE"></span><span id="error_ds_out_of_version_store"></span>**FEHLER \_ DS \_ AUßERHALB DES \_ \_ \_ VERSIONSSPEICHERS**
</dt> <dd> <dl> <dt>

8573 (0x217D)
</dt> <dt>



Die Datenbank befindet sich außerhalb des Versionsspeichers.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INCOMPATIBLE_CONTROLS_USED"></span><span id="error_ds_incompatible_controls_used"></span>**FEHLER \_ BEI \_ VERWENDUNG VON INKOMPATIBLEN \_ DS-STEUERELEMENTEN \_**
</dt> <dd> <dl> <dt>

8574 (0x217E)
</dt> <dt>



Der Vorgang kann nicht fortgesetzt werden, da mehrere in Konfliktstehende Steuerelemente verwendet wurden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_REF_DOMAIN"></span><span id="error_ds_no_ref_domain"></span>**FEHLER \_ DS \_ NO REF \_ \_ DOMAIN**
</dt> <dd> <dl> <dt>

8575 (0x217F)
</dt> <dt>



Eine gültige Sicherheitsbeschreibungsverweisdomäne für diese Partition wurde nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_RESERVED_LINK_ID"></span><span id="error_ds_reserved_link_id"></span>**ERROR \_ DS \_ RESERVED \_ LINK \_ ID**
</dt> <dd> <dl> <dt>

8576 (0x2180)
</dt> <dt>



Fehler beim Schemaupdate: Der Linkbezeichner ist reserviert.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_LINK_ID_NOT_AVAILABLE"></span><span id="error_ds_link_id_not_available"></span>**\_FEHLER: \_ DS-LINK-ID \_ \_ NICHT \_ VERFÜGBAR**
</dt> <dd> <dl> <dt>

8577 (0x2181)
</dt> <dt>



Fehler beim Schemaupdate: Es sind keine Linkbezeichner verfügbar.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_AG_CANT_HAVE_UNIVERSAL_MEMBER"></span><span id="error_ds_ag_cant_have_universal_member"></span>**ERROR \_ DS \_ AG \_ CANT \_ HAVE \_ UNIVERSAL \_ MEMBER**
</dt> <dd> <dl> <dt>

8578 (0x2182)
</dt> <dt>



Eine Kontogruppe kann keine universelle Gruppe als Mitglied haben.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MODIFYDN_DISALLOWED_BY_INSTANCE_TYPE"></span><span id="error_ds_modifydn_disallowed_by_instance_type"></span>**FEHLER \_ DS \_ MODIFYDN \_ NICHT ZULÄSSIG NACH \_ \_ \_ INSTANZTYP**
</dt> <dd> <dl> <dt>

8579 (0x2183)
</dt> <dt>



Umbenennen oder Verschieben von Vorgängen zum Benennen von Kontextköpfen oder schreibgeschützten Objekten sind nicht zulässig.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_OBJECT_MOVE_IN_SCHEMA_NC"></span><span id="error_ds_no_object_move_in_schema_nc"></span>**FEHLER \_ DS \_ NO OBJECT MOVE IN SCHEMA \_ \_ \_ \_ \_ NC**
</dt> <dd> <dl> <dt>

8580 (0x2184)
</dt> <dt>



Verschiebungsvorgänge für Objekte im Schemabenennungskontext sind nicht zulässig.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MODIFYDN_DISALLOWED_BY_FLAG"></span><span id="error_ds_modifydn_disallowed_by_flag"></span>**FEHLER \_ DS \_ MODIFYDN \_ NICHT ZULÄSSIG DURCH \_ \_ FLAG**
</dt> <dd> <dl> <dt>

8581 (0x2185)
</dt> <dt>



Ein Systemflag wurde für das -Objekt festgelegt und lässt nicht zu, dass das Objekt verschoben oder umbenannt wird.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MODIFYDN_WRONG_GRANDPARENT"></span><span id="error_ds_modifydn_wrong_grandparent"></span>**FEHLER \_ DS \_ MODIFYDN \_ WRONG \_ ÜBERL**
</dt> <dd> <dl> <dt>

8582 (0x2186)
</dt> <dt>



Dieses Objekt darf seinen Überlterncontainer nicht ändern. Verschiebungen sind für dieses Objekt nicht unzulässig, sondern auf gleichgeordnete Container beschränkt.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_ERROR_TRUST_REFERRAL"></span><span id="error_ds_name_error_trust_referral"></span>**FEHLER \_ DS \_ NAME ERROR TRUST \_ \_ \_ REFERRAL**
</dt> <dd> <dl> <dt>

8583 (0x2187)
</dt> <dt>



Eine vollständige Auflösung ist nicht möglich. Es wird ein Verweis auf eine andere Gesamtstruktur generiert.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_SUPPORTED_ON_STANDARD_SERVER"></span><span id="error_not_supported_on_standard_server"></span>**FEHLER \_ \_ \_ AUF \_ \_ STANDARDSERVER NICHT UNTERSTÜTZT**
</dt> <dd> <dl> <dt>

8584 (0x2188)
</dt> <dt>



Die angeforderte Aktion wird auf dem Standardserver nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_ACCESS_REMOTE_PART_OF_AD"></span><span id="error_ds_cant_access_remote_part_of_ad"></span>**FEHLER \_ DS \_ CANT \_ ACCESS REMOTE PART OF \_ \_ \_ \_ AD**
</dt> <dd> <dl> <dt>

8585 (0x2189)
</dt> <dt>



Auf eine Partition des Verzeichnisdiensts auf einem Remoteserver konnte nicht zugegriffen werden. Stellen Sie sicher, dass mindestens ein Server für die betreffende Partition ausgeführt wird.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CR_IMPOSSIBLE_TO_VALIDATE_V2"></span><span id="error_ds_cr_impossible_to_validate_v2"></span>**FEHLER \_ DS \_ CR \_ \_ UNMÖGLICH, \_ V2 ZU ÜBERPRÜFEN \_**
</dt> <dd> <dl> <dt>

8586 (0x218A)
</dt> <dt>



Das Verzeichnis kann den vorgeschlagenen Namen des Namenskontexts (oder des Partitionsnamens) nicht überprüfen, da es weder ein Replikat enthält noch ein Replikat des Namenskontexts über dem vorgeschlagenen Namenskontext kontaktieren kann. Stellen Sie sicher, dass der übergeordnete Namenskontext ordnungsgemäß im DNS registriert ist und mindestens ein Replikat dieses Namenskontexts vom Domänenbenennungsmaster erreichbar ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_THREAD_LIMIT_EXCEEDED"></span><span id="error_ds_thread_limit_exceeded"></span>**FEHLER \_ BEIM ÜBERSCHREITEN DES DS-THREADLIMITS \_ \_ \_**
</dt> <dd> <dl> <dt>

8587 (0x218B)
</dt> <dt>



Das Threadlimit für diese Anforderung wurde überschritten.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NOT_CLOSEST"></span><span id="error_ds_not_closest"></span>**FEHLER \_ DS \_ NICHT AM \_ NÄCHSTEN**
</dt> <dd> <dl> <dt>

8588 (0x218C)
</dt> <dt>



Der globale Katalogserver befindet sich nicht am nächstgelegenen Standort.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_DERIVE_SPN_WITHOUT_SERVER_REF"></span><span id="error_ds_cant_derive_spn_without_server_ref"></span>**FEHLER \_ DS \_ KANN \_ \_ SPN OHNE \_ \_ \_ SERVER-REF NICHT ABLEITEN**
</dt> <dd> <dl> <dt>

8589 (0x218D)
</dt> <dt>



Der DS kann keinen Dienstprinzipalnamen (Service Principal Name, SPN) ableiten, mit dem der Zielserver gegenseitig authentifiziert werden kann, da das entsprechende Serverobjekt in der lokalen DS-Datenbank über kein serverReference-Attribut verfügt.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SINGLE_USER_MODE_FAILED"></span><span id="error_ds_single_user_mode_failed"></span>**FEHLER: \_ FEHLER \_ IM DS-EINZELBENUTZERMODUS \_ \_ \_**
</dt> <dd> <dl> <dt>

8590 (0x218E)
</dt> <dt>



Der Verzeichnisdienst konnte nicht in den Einzelbenutzermodus wechseln.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NTDSCRIPT_SYNTAX_ERROR"></span><span id="error_ds_ntdscript_syntax_error"></span>**FEHLER: \_ DS \_ NTDSCRIPT-SYNTAXFEHLER \_ \_**
</dt> <dd> <dl> <dt>

8591 (0x218F)
</dt> <dt>



Der Verzeichnisdienst kann das Skript aufgrund eines Syntaxfehlers nicht analysieren.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NTDSCRIPT_PROCESS_ERROR"></span><span id="error_ds_ntdscript_process_error"></span>**FEHLER \_ BEIM DS \_ NTDSCRIPT-PROZESSFEHLER \_ \_**
</dt> <dd> <dl> <dt>

8592 (0x2190)
</dt> <dt>



Der Verzeichnisdienst kann das Skript aufgrund eines Fehlers nicht verarbeiten.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DIFFERENT_REPL_EPOCHS"></span><span id="error_ds_different_repl_epochs"></span>**FEHLER \_ DS \_ VERSCHIEDENE \_ \_ REPL-EPOCHEN**
</dt> <dd> <dl> <dt>

8593 (0x2191)
</dt> <dt>



Der Verzeichnisdienst kann den angeforderten Vorgang nicht ausführen, da die beteiligten Server unterschiedliche Replikationszeit epochen aufweisen (was in der Regel mit einer gerade ausgeführten Umbenennung der Domäne zusammenhängt).


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRS_EXTENSIONS_CHANGED"></span><span id="error_ds_drs_extensions_changed"></span>**\_FEHLER: \_ DS-DRS-ERWEITERUNGEN \_ \_ GEÄNDERT**
</dt> <dd> <dl> <dt>

8594 (0x2192)
</dt> <dt>



Die Verzeichnisdienstbindung muss aufgrund einer Änderung der Servererweiterungsinformationen neu ausgehandelt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_REPLICA_SET_CHANGE_NOT_ALLOWED_ON_DISABLED_CR"></span><span id="error_ds_replica_set_change_not_allowed_on_disabled_cr"></span>**FEHLER: \_ ÄNDERUNG DER \_ DS-REPLIKATGRUPPE \_ \_ FÜR \_ \_ \_ \_ DEAKTIVIERTE \_ CR NICHT ZULÄSSIG**
</dt> <dd> <dl> <dt>

8595 (0x2193)
</dt> <dt>



Der Vorgang ist für eine deaktivierte Kreuzverweis nicht zulässig.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_MSDS_INTID"></span><span id="error_ds_no_msds_intid"></span>**FEHLER \_ DS \_ NO \_ MSDS \_ INTID**
</dt> <dd> <dl> <dt>

8596 (0x2194)
</dt> <dt>



Fehler beim Schemaupdate: Es sind keine Werte für msDS-IntId verfügbar.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DUP_MSDS_INTID"></span><span id="error_ds_dup_msds_intid"></span>**FEHLER \_ DS \_ DUP \_ MSDS \_ INTID**
</dt> <dd> <dl> <dt>

8597 (0x2195)
</dt> <dt>



Fehler beim Schemaupdate: MsDS-INtId duplizieren. Wiederholen Sie den Vorgang.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_EXISTS_IN_RDNATTID"></span><span id="error_ds_exists_in_rdnattid"></span>**FEHLER \_ DS \_ EXISTS IN \_ \_ RDNATTID**
</dt> <dd> <dl> <dt>

8598 (0x2196)
</dt> <dt>



Fehler beim Löschen des Schemas: Das Attribut wird in rDNAttID verwendet.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_AUTHORIZATION_FAILED"></span><span id="error_ds_authorization_failed"></span>**FEHLER \_ FEHLER BEI DER DS-AUTORISIERUNG \_ \_**
</dt> <dd> <dl> <dt>

8599 (0x2197)
</dt> <dt>



Der Verzeichnisdienst konnte die Anforderung nicht autorisieren.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INVALID_SCRIPT"></span><span id="error_ds_invalid_script"></span>**FEHLER \_ \_ DS: UNGÜLTIGES \_ SKRIPT**
</dt> <dd> <dl> <dt>

8600 (0x2198)
</dt> <dt>



Der Verzeichnisdienst kann das Skript nicht verarbeiten, da es ungültig ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_REMOTE_CROSSREF_OP_FAILED"></span><span id="error_ds_remote_crossref_op_failed"></span>**FEHLER: \_ FEHLER BEI \_ DS-REMOTE \_ \_ CROSSREF-OP \_**
</dt> <dd> <dl> <dt>

8601 (0x2199)
</dt> <dt>



Fehler beim Remoteerstellungs-Querverweisvorgang auf dem Domänenbenennungsmaster-FSMO. Der Fehler des Vorgangs liegt in den erweiterten Daten vor.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CROSS_REF_BUSY"></span><span id="error_ds_cross_ref_busy"></span>**FEHLER \_ DS \_ CROSS REF \_ \_ BUSY**
</dt> <dd> <dl> <dt>

8602 (0x219A)
</dt> <dt>



Ein Querverweis wird lokal mit dem gleichen Namen verwendet.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_DERIVE_SPN_FOR_DELETED_DOMAIN"></span><span id="error_ds_cant_derive_spn_for_deleted_domain"></span>**FEHLER: \_ DS \_ KANN \_ \_ SPN \_ FÜR \_ GELÖSCHTE \_ DOMÄNE NICHT ABLEITEN**
</dt> <dd> <dl> <dt>

8603 (0x219B)
</dt> <dt>



Der DS kann keinen Dienstprinzipalnamen (Service Principal Name, SPN) ableiten, mit dem der Zielserver gegenseitig authentifiziert werden kann, da die Domäne des Servers aus der Gesamtstruktur gelöscht wurde.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_DEMOTE_WITH_WRITEABLE_NC"></span><span id="error_ds_cant_demote_with_writeable_nc"></span>**FEHLER \_ DS \_ CANT \_ DEMOTE \_ WITH \_ WRITEABLE \_ NC**
</dt> <dd> <dl> <dt>

8604 (0x219C)
</dt> <dt>



Schreibbare NCs verhindern, dass dieser Domänencontroller herabgestuft wird.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DUPLICATE_ID_FOUND"></span><span id="error_ds_duplicate_id_found"></span>**FEHLER: \_ DOPPELTE \_ \_ DS-ID \_ GEFUNDEN**
</dt> <dd> <dl> <dt>

8605 (0x219D)
</dt> <dt>



Das angeforderte Objekt verfügt über einen nicht eindeutigen Bezeichner und kann nicht abgerufen werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INSUFFICIENT_ATTR_TO_CREATE_OBJECT"></span><span id="error_ds_insufficient_attr_to_create_object"></span>**FEHLER \_ DS \_ INSUFFICIENT \_ ATTR TO CREATE \_ \_ \_ OBJECT**
</dt> <dd> <dl> <dt>

8606 (0x219E)
</dt> <dt>



Es wurden nicht genügend Attribute zum Erstellen eines Objekts angegeben. Dieses Objekt ist möglicherweise nicht vorhanden, da es möglicherweise gelöscht und bereits garbage collected wurde.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_GROUP_CONVERSION_ERROR"></span><span id="error_ds_group_conversion_error"></span>**FEHLER BEI \_ DER \_ \_ DS-GRUPPENKONVERTIERUNG \_**
</dt> <dd> <dl> <dt>

8607 (0x219F)
</dt> <dt>



Die Gruppe kann aufgrund von Attributeinschränkungen für den angeforderten Gruppentyp nicht konvertiert werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_MOVE_APP_BASIC_GROUP"></span><span id="error_ds_cant_move_app_basic_group"></span>**FEHLER: \_ DS \_ CANT \_ MOVE APP \_ BASIC \_ \_ GROUP**
</dt> <dd> <dl> <dt>

8608 (0x21A0)
</dt> <dt>



Domänenübergreifendes Verschieben von nicht leeren Basisanwendungsgruppen ist nicht zulässig.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_MOVE_APP_QUERY_GROUP"></span><span id="error_ds_cant_move_app_query_group"></span>**FEHLER: \_ DS \_ CANT \_ MOVE APP \_ QUERY \_ \_ GROUP**
</dt> <dd> <dl> <dt>

8609 (0x21A1)
</dt> <dt>



Domänenübergreifendes Verschieben von nicht leeren abfragebasierten Anwendungsgruppen ist nicht zulässig.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ROLE_NOT_VERIFIED"></span><span id="error_ds_role_not_verified"></span>**FEHLER \_ \_ DS-ROLLE \_ NICHT \_ ÜBERPRÜFT**
</dt> <dd> <dl> <dt>

8610 (0x21A2)
</dt> <dt>



Der Besitz der FSMO-Rolle konnte nicht überprüft werden, da die Verzeichnispartition nicht erfolgreich mit mindestens einem Replikationspartner repliziert wurde.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_WKO_CONTAINER_CANNOT_BE_SPECIAL"></span><span id="error_ds_wko_container_cannot_be_special"></span>**\_FEHLER: \_ DS-WKO-CONTAINER \_ KANN NICHT \_ \_ \_ SONDERBAR SEIN**
</dt> <dd> <dl> <dt>

8611 (0x21A3)
</dt> <dt>



Der Zielcontainer für eine Umleitung eines bekannten Objektcontainers darf nicht bereits ein spezieller Container sein.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DOMAIN_RENAME_IN_PROGRESS"></span><span id="error_ds_domain_rename_in_progress"></span>**FEHLER \_ BEIM \_ \_ UMBENENNEN DER DS-DOMÄNE \_ IN \_ BEARBEITUNG**
</dt> <dd> <dl> <dt>

8612 (0x21A4)
</dt> <dt>



Der Verzeichnisdienst kann den angeforderten Vorgang nicht ausführen, da gerade ein Domänenbenennungsvorgang ausgeführt wird.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_EXISTING_AD_CHILD_NC"></span><span id="error_ds_existing_ad_child_nc"></span>**FEHLER \_ DS \_ EXISTING AD CHILD \_ \_ \_ NC**
</dt> <dd> <dl> <dt>

8613 (0x21A5)
</dt> <dt>



Der Verzeichnisdienst hat eine untergeordnete Partition unterhalb des angeforderten Partitionsnamens erkannt. Die Partitionshierarchie muss in einer Top-Down-Methode erstellt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_REPL_LIFETIME_EXCEEDED"></span><span id="error_ds_repl_lifetime_exceeded"></span>**FEHLER: ÜBERSCHREITUNG DER \_ \_ DS-REPL-LEBENSDAUER \_ \_**
</dt> <dd> <dl> <dt>

8614 (0x21A6)
</dt> <dt>



Der Verzeichnisdienst kann nicht mit diesem Server repliziert werden, da die Zeit seit der letzten Replikation mit diesem Server die Tombstonelebensdauer überschritten hat.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DISALLOWED_IN_SYSTEM_CONTAINER"></span><span id="error_ds_disallowed_in_system_container"></span>**FEHLER \_ DS \_ IM \_ \_ \_ SYSTEMCONTAINER NICHT ZULÄSSIG**
</dt> <dd> <dl> <dt>

8615 (0x21A7)
</dt> <dt>



Der angeforderte Vorgang ist für ein Objekt unter dem Systemcontainer nicht zulässig.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_LDAP_SEND_QUEUE_FULL"></span><span id="error_ds_ldap_send_queue_full"></span>**FEHLER: \_ DS \_ LDAP SEND QUEUE \_ \_ \_ FULL**
</dt> <dd> <dl> <dt>

8616 (0x21A8)
</dt> <dt>



Die Netzwerk-Sendewarteschlange der LDAP-Server ist aufgefüllt, da der Client die Ergebnisse seiner Anforderungen nicht schnell genug verarbeitet. Es werden keine weiteren Anforderungen verarbeitet, bis der Client aufholt. Wenn der Client nicht aufholt, wird er getrennt.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_OUT_SCHEDULE_WINDOW"></span><span id="error_ds_dra_out_schedule_window"></span>**FEHLER \_ BEIM \_ DS-DRA \_ \_ OUT-ZEITPLANFENSTER \_**
</dt> <dd> <dl> <dt>

8617 (0x21A9)
</dt> <dt>



Die geplante Replikation wurde nicht durchgeführt, da das System zu ausgelastet war, um die Anforderung innerhalb des Zeitplanfensters auszuführen. Die Replikationswarteschlange ist überladen. Erwägen Sie, die Anzahl der Partner zu verringern oder die Häufigkeit der geplanten Replikation zu verringern.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_POLICY_NOT_KNOWN"></span><span id="error_ds_policy_not_known"></span>**FEHLER \_ BEI \_ DS-RICHTLINIE \_ NICHT \_ BEKANNT**
</dt> <dd> <dl> <dt>

8618 (0x21AA)
</dt> <dt>



Derzeit kann nicht ermittelt werden, ob die Branchreplikationsrichtlinie auf dem Hubdomänencontroller verfügbar ist. Versuchen Sie es zu einem späteren Zeitpunkt erneut, um Replikationslatenzen zu berücksichtigen.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SITE_SETTINGS_OBJECT"></span><span id="error_no_site_settings_object"></span>**FEHLER: \_ OBJEKT \_ \_ "KEINE STANDORTEINSTELLUNGEN" \_**
</dt> <dd> <dl> <dt>

8619 (0x21AB)
</dt> <dt>



Das Standorteinstellungsobjekt für den angegebenen Standort ist nicht vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SECRETS"></span><span id="error_no_secrets"></span>**FEHLER \_ KEINE \_ GEHEIMNISSE**
</dt> <dd> <dl> <dt>

8620 (0x21AC)
</dt> <dt>



Der lokale Kontospeicher enthält kein Geheimnismaterial für das angegebene Konto.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_WRITABLE_DC_FOUND"></span><span id="error_no_writable_dc_found"></span>**FEHLER: \_ KEIN \_ BESCHREIBBARER \_ DOMÄNENCONTROLLER \_ GEFUNDEN**
</dt> <dd> <dl> <dt>

8621 (0x21AD)
</dt> <dt>



Ein beschreibbarer Domänencontroller in der Domäne wurde nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_SERVER_OBJECT"></span><span id="error_ds_no_server_object"></span>**FEHLER \_ DS \_ KEIN \_ \_ SERVEROBJEKT**
</dt> <dd> <dl> <dt>

8622 (0x21AE)
</dt> <dt>



Das Serverobjekt für den Domänencontroller ist nicht vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_NTDSA_OBJECT"></span><span id="error_ds_no_ntdsa_object"></span>**FEHLER \_ DS \_ KEIN \_ NTDSA-OBJEKT \_**
</dt> <dd> <dl> <dt>

8623 (0x21AF)
</dt> <dt>



Das NTDS-Einstellungen-Objekt für den Domänencontroller ist nicht vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NON_ASQ_SEARCH"></span><span id="error_ds_non_asq_search"></span>**ERROR \_ DS \_ NON \_ ASQ \_ SEARCH**
</dt> <dd> <dl> <dt>

8624 (0x21B0)
</dt> <dt>



Der angeforderte Suchvorgang wird für ASQ-Suchvorgänge nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_AUDIT_FAILURE"></span><span id="error_ds_audit_failure"></span>**FEHLER \_ DS \_ AUDIT \_ FAILURE**
</dt> <dd> <dl> <dt>

8625 (0x21B1)
</dt> <dt>



Ein erforderliches Überwachungsereignis konnte für den Vorgang nicht generiert werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INVALID_SEARCH_FLAG_SUBTREE"></span><span id="error_ds_invalid_search_flag_subtree"></span>**FEHLER \_ \_ DS: UNGÜLTIGES \_ \_ SUCHFLAG \_ UNTERSTRUKTUR**
</dt> <dd> <dl> <dt>

8626 (0x21B2)
</dt> <dt>



Die Suchflags für das Attribut sind ungültig. Das Teilstrukturindexbit ist nur für Einwertattribute gültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INVALID_SEARCH_FLAG_TUPLE"></span><span id="error_ds_invalid_search_flag_tuple"></span>**ERROR \_ DS \_ INVALID \_ SEARCH \_ FLAG \_ TUPLE**
</dt> <dd> <dl> <dt>

8627 (0x21B3)
</dt> <dt>



Die Suchflags für das Attribut sind ungültig. Das Tupelindexbit ist nur für Attribute von Unicode-Zeichenfolgen gültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_HIERARCHY_TABLE_TOO_DEEP"></span><span id="error_ds_hierarchy_table_too_deep"></span>**FEHLER: \_ \_ DS-HIERARCHIETABELLE \_ \_ ZU \_ TIEF**
</dt> <dd> <dl> <dt>

8628 (0x21B4)
</dt> <dt>



Die Adressbücher sind zu tief geschachtelt. Fehler beim Erstellen der Hierarchietabelle.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_CORRUPT_UTD_VECTOR"></span><span id="error_ds_dra_corrupt_utd_vector"></span>**ERROR \_ DS \_ DRA \_ CORRUPT \_ UTD \_ VECTOR**
</dt> <dd> <dl> <dt>

8629 (0x21B5)
</dt> <dt>



Der angegebene Aktualitätsvektor ist beschädigt.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_SECRETS_DENIED"></span><span id="error_ds_dra_secrets_denied"></span>**FEHLER \_ DS \_ DRA \_ SECRETS \_ DENIED**
</dt> <dd> <dl> <dt>

8630 (0x21B6)
</dt> <dt>



Die Anforderung zum Replizieren von Geheimnissen wird abgelehnt.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_RESERVED_MAPI_ID"></span><span id="error_ds_reserved_mapi_id"></span>**ERROR \_ DS \_ RESERVED \_ MAPI \_ ID**
</dt> <dd> <dl> <dt>

8631 (0x21B7)
</dt> <dt>



Fehler beim Schemaupdate: Der MAPI-Bezeichner ist reserviert.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MAPI_ID_NOT_AVAILABLE"></span><span id="error_ds_mapi_id_not_available"></span>**FEHLER: \_ DS \_ \_ MAPI-ID \_ NICHT \_ VERFÜGBAR**
</dt> <dd> <dl> <dt>

8632 (0x21B8)
</dt> <dt>



Fehler beim Schemaupdate: Es sind keine MAPI-Bezeichner verfügbar.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_MISSING_KRBTGT_SECRET"></span><span id="error_ds_dra_missing_krbtgt_secret"></span>**FEHLER \_ DS \_ DRA \_ \_ FEHLENDES KRBTGT-GEHEIMNIS \_**
</dt> <dd> <dl> <dt>

8633 (0x21B9)
</dt> <dt>



Fehler beim Replikationsvorgang, weil die erforderlichen Attribute des lokalen krbtgt-Objekts fehlen.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DOMAIN_NAME_EXISTS_IN_FOREST"></span><span id="error_ds_domain_name_exists_in_forest"></span>**FEHLER \_ DS \_ DOMAIN NAME EXISTS IN \_ \_ \_ \_ FOREST**
</dt> <dd> <dl> <dt>

8634 (0x21BA)
</dt> <dt>



Der Domänenname der vertrauenswürdigen Domäne ist bereits in der Gesamtstruktur vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_FLAT_NAME_EXISTS_IN_FOREST"></span><span id="error_ds_flat_name_exists_in_forest"></span>**FEHLER: \_ DER \_ DS-FLATNAME \_ \_ IST IN DER \_ GESAMTSTRUKTUR VORHANDEN. \_**
</dt> <dd> <dl> <dt>

8635 (0x21BB)
</dt> <dt>



Der flache Name der vertrauenswürdigen Domäne ist bereits in der Gesamtstruktur vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_USER_PRINCIPAL_NAME"></span><span id="error_invalid_user_principal_name"></span>**FEHLER: \_ UNGÜLTIGER \_ \_ BENUTZERPRINZIPALNAME \_**
</dt> <dd> <dl> <dt>

8636 (0x21BC)
</dt> <dt>



Der Benutzerprinzipalname (User Principal Name, UPN) ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OID_MAPPED_GROUP_CANT_HAVE_MEMBERS"></span><span id="error_ds_oid_mapped_group_cant_have_members"></span>**ERROR \_ DS \_ OID \_ MAPPED \_ GROUP \_ CANT \_ HAVE \_ MEMBERS**
</dt> <dd> <dl> <dt>

8637 (0x21BD)
</dt> <dt>



OID-zugeordnete Gruppen dürfen keine Mitglieder haben.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OID_NOT_FOUND"></span><span id="error_ds_oid_not_found"></span>**\_FEHLER: \_ DS-OID \_ NICHT \_ GEFUNDEN**
</dt> <dd> <dl> <dt>

8638 (0x21BE)
</dt> <dt>



Die angegebene OID wurde nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_RECYCLED_TARGET"></span><span id="error_ds_dra_recycled_target"></span>**ERROR \_ DS \_ DRA \_ RECYCLED \_ TARGET**
</dt> <dd> <dl> <dt>

8639 (0x21BF)
</dt> <dt>



Fehler beim Replikationsvorgang, weil das Zielobjekt, auf das ein Linkwert verweist, wiederverwendet wird.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DISALLOWED_NC_REDIRECT"></span><span id="error_ds_disallowed_nc_redirect"></span>**FEHLER \_ DS \_ NICHT \_ ZUGELASSENE \_ NC-UMLEITUNG**
</dt> <dd> <dl> <dt>

8640 (0x21C0)
</dt> <dt>



Fehler beim Umleitungsvorgang, weil sich das Zielobjekt in einem NC befindet, der sich vom Domänen-NC des aktuellen Domänencontrollers unterscheidet.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_HIGH_ADLDS_FFL"></span><span id="error_ds_high_adlds_ffl"></span>**FEHLER \_ DS \_ HIGH \_ ADLDS \_ FFL**
</dt> <dd> <dl> <dt>

8641 (0x21C1)
</dt> <dt>



Die Funktionsebene des AD LDS Konfigurationssatzes kann nicht auf den angeforderten Wert herabgesetzt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_HIGH_DSA_VERSION"></span><span id="error_ds_high_dsa_version"></span>**FEHLER \_ DS \_ HIGH \_ DSA \_ VERSION**
</dt> <dd> <dl> <dt>

8642 (0x21C2)
</dt> <dt>



Die Funktionsebene der Domäne (oder Gesamtstruktur) kann nicht auf den angeforderten Wert herabgesetzt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_LOW_ADLDS_FFL"></span><span id="error_ds_low_adlds_ffl"></span>**FEHLER \_ DS \_ LOW \_ ADLDS \_ FFL**
</dt> <dd> <dl> <dt>

8643 (0x21C3)
</dt> <dt>



Die Funktionsebene des AD LDS Konfigurationssatzes kann nicht auf den angeforderten Wert erhöht werden, da mindestens eine ADLDS-Instanz auf einer niedrigeren inkompatiblen Funktionsebene vorhanden ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_DOMAIN_SID_SAME_AS_LOCAL_WORKSTATION"></span><span id="error_domain_sid_same_as_local_workstation"></span>**\_ \_ FEHLERDOMÄNEN-SID \_ IDENTISCH \_ MIT LOKALER \_ \_ ARBEITSSTATION**
</dt> <dd> <dl> <dt>

8644 (0x21C4)
</dt> <dt>



Der Domänenbeitritt kann nicht abgeschlossen werden, da die SID der Domäne, der Sie beitreten wollten, mit der SID dieses Computers identisch war. Dies ist ein Symptom für eine nicht ordnungsgemäß geklonte Betriebssysteminstallation. Sie sollten sysprep auf diesem Computer ausführen, um eine neue Computer-SID zu generieren. Unter <https://go.microsoft.com/fwlink/p/?linkid=168895> finden Sie weitere Informationen.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_UNDELETE_SAM_VALIDATION_FAILED"></span><span id="error_ds_undelete_sam_validation_failed"></span>**FEHLER \_ \_ DS UNDELETE \_ SAM VALIDATION \_ \_ FAILED**
</dt> <dd> <dl> <dt>

8645 (0x21C5)
</dt> <dt>



Fehler beim Wiederherstellen des Vorgangs, weil der Sam-Kontoname oder der zusätzliche Sam-Kontoname des objekts, das nicht gelöscht wird, mit einem vorhandenen Liveobjekt in Konflikt tritt.


</dt> </dl> </dd> <dt>

<span id="ERROR_INCORRECT_ACCOUNT_TYPE"></span><span id="error_incorrect_account_type"></span>**FEHLER: \_ FALSCHER \_ \_ KONTOTYP**
</dt> <dd> <dl> <dt>

8646 (0x21C6)
</dt> <dt>



Das System ist für das angegebene Konto nicht autoritativ und kann daher den Vorgang nicht abschließen. Wiederholen Sie den Vorgang mithilfe des Anbieters, der diesem Konto zugeordnet ist. Wenn es sich um einen Onlineanbieter handelt, verwenden Sie die Onlinewebsite des Anbieters.


</dt> </dl> </dd> </dl>


## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>WinError.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Systemfehlercodes](system-error-codes.md)
</dt> </dl>

 

 




