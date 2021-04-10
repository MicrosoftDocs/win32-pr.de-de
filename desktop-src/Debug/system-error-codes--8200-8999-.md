---
description: Beschreibt die in der Header Datei "Winerror. h" definierten Fehlercodes 8200-8999 und ist für Entwickler bestimmt.
ms.assetid: f16fdfa3-b080-47ee-a7dd-241fe2d24278
title: System Fehler Codes (8200-8999) (Winerror. h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: 7500ae4c178999de8052b0858089604652dc5237
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214158"
---
# <a name="system-error-codes-8200-8999"></a>System Fehler Codes (8200-8999)

> [!NOTE]
> Diese Informationen sind für Entwickler gedacht, die Systemfehler Debuggen. Bei anderen Fehlern, wie z. b. Problemen mit Windows Update, finden Sie eine Liste der Ressourcen auf der Seite [Fehlercodes](system-error-codes.md) .

In der folgenden Liste werden die [Systemfehler Codes](system-error-codes.md) für die Fehler 8200 bis 8999 beschrieben. Sie werden von der [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) -Funktion zurückgegeben, wenn viele Funktionen fehlschlagen. Um den Beschreibungstext für den Fehler in Ihrer Anwendung abzurufen, verwenden Sie die [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) -Funktion mit dem Flag " **Format \_ Message \_ from \_ System** ".

<dl> <dt>

<span id="ERROR_DS_NOT_INSTALLED"></span><span id="error_ds_not_installed"></span>**Fehler- \_ DS \_ nicht \_ installiert**
</dt> <dd> <dl> <dt>

8200 (0x2008)
</dt> <dt>



Fehler beim Installieren des Verzeichnis Dienstanbieter. Weitere Informationen finden Sie im Ereignisprotokoll.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MEMBERSHIP_EVALUATED_LOCALLY"></span><span id="error_ds_membership_evaluated_locally"></span>**Fehler- \_ DS- \_ Mitgliedschaft \_ \_ lokal ausgewertet**
</dt> <dd> <dl> <dt>

8201 (0x2009)
</dt> <dt>



Der Verzeichnisdienst hat die Gruppenmitgliedschaften lokal ausgewertet.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_ATTRIBUTE_OR_VALUE"></span><span id="error_ds_no_attribute_or_value"></span>**Fehler- \_ DS \_ kein \_ Attribut \_ oder \_ Wert**
</dt> <dd> <dl> <dt>

8202 (0x200a)
</dt> <dt>



Das angegebene Verzeichnisdienst Attribut oder der angegebene Wert ist nicht vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INVALID_ATTRIBUTE_SYNTAX"></span><span id="error_ds_invalid_attribute_syntax"></span>**Fehler- \_ DS \_ ungültige \_ Attribut \_ Syntax.**
</dt> <dd> <dl> <dt>

8203 (0x200b)
</dt> <dt>



Die für den Verzeichnisdienst angegebene Attribut Syntax ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ATTRIBUTE_TYPE_UNDEFINED"></span><span id="error_ds_attribute_type_undefined"></span>**Fehler \_ DS \_ - \_ Attributtyp nicht \_ definiert**
</dt> <dd> <dl> <dt>

8204 (0x200c)
</dt> <dt>



Der für den Verzeichnisdienst angegebene Attributtyp ist nicht definiert.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ATTRIBUTE_OR_VALUE_EXISTS"></span><span id="error_ds_attribute_or_value_exists"></span>**Fehler- \_ DS- \_ Attribut oder- \_ \_ Wert \_ vorhanden**
</dt> <dd> <dl> <dt>

8205 (0x200d)
</dt> <dt>



Das angegebene Verzeichnisdienst Attribut oder der angegebene Wert ist bereits vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_BUSY"></span><span id="error_ds_busy"></span>**Fehler- \_ DS \_ ausgelastet**
</dt> <dd> <dl> <dt>

8206 (0x200e)
</dt> <dt>



Der Verzeichnisdienst ist ausgelastet.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_UNAVAILABLE"></span><span id="error_ds_unavailable"></span>**Fehler- \_ DS nicht \_ verfügbar**
</dt> <dd> <dl> <dt>

8207 (0x200f)
</dt> <dt>



Der Verzeichnisdienst ist nicht verfügbar.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_RIDS_ALLOCATED"></span><span id="error_ds_no_rids_allocated"></span>**Fehler " \_ DS \_ keine \_ RIDs \_ zugeordnet"**
</dt> <dd> <dl> <dt>

8208 (0x2010)
</dt> <dt>



Der Verzeichnisdienst kann keinen relativen Bezeichner zuweisen.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_MORE_RIDS"></span><span id="error_ds_no_more_rids"></span>**Fehler- \_ DS \_ keine \_ weiteren \_ RIDs**
</dt> <dd> <dl> <dt>

8209 (0x2011)
</dt> <dt>



Der Verzeichnisdienst hat den Pool relativer Bezeichner ausgeschöpft.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INCORRECT_ROLE_OWNER"></span><span id="error_ds_incorrect_role_owner"></span>**Fehler \_ DS \_ falscher \_ Rollen \_ Besitzer**
</dt> <dd> <dl> <dt>

8210 (0x2012)
</dt> <dt>



Der angeforderte Vorgang konnte nicht ausgeführt werden, da der Verzeichnisdienst nicht der Master für diese Art von Vorgang ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_RIDMGR_INIT_ERROR"></span><span id="error_ds_ridmgr_init_error"></span>**Fehler \_ DS \_ ridmgr- \_ Init- \_ Fehler**
</dt> <dd> <dl> <dt>

8211 (0x2013)
</dt> <dt>



Der Verzeichnisdienst konnte das Subsystem, das relative Bezeichner ordnet, nicht initialisieren.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OBJ_CLASS_VIOLATION"></span><span id="error_ds_obj_class_violation"></span>**Fehler- \_ DS- \_ obj- \_ Klassen \_ Verletzung**
</dt> <dd> <dl> <dt>

8212 (0x2014)
</dt> <dt>



Der angeforderte Vorgang erfüllte mindestens eine Einschränkung, die der Klasse des-Objekts zugeordnet ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_ON_NON_LEAF"></span><span id="error_ds_cant_on_non_leaf"></span>**Fehler " \_ DS" \_ auf " \_ \_ nicht \_ Blatt"**
</dt> <dd> <dl> <dt>

8213 (0x2015)
</dt> <dt>



Der Verzeichnisdienst kann den angeforderten Vorgang nur für ein Blatt Objekt ausführen.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_ON_RDN"></span><span id="error_ds_cant_on_rdn"></span>**Fehler " \_ DS" \_ \_ bei \_ RDN**
</dt> <dd> <dl> <dt>

8214 (0x2016)
</dt> <dt>



Der Verzeichnisdienst kann den angeforderten Vorgang nicht für das RDN-Attribut eines Objekts ausführen.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_MOD_OBJ_CLASS"></span><span id="error_ds_cant_mod_obj_class"></span>**Error \_ DS \_ cant \_ mod \_ obj- \_ Klasse**
</dt> <dd> <dl> <dt>

8215 (0x2017)
</dt> <dt>



Der Verzeichnisdienst hat einen Versuch erkannt, die Objektklasse eines Objekts zu ändern.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CROSS_DOM_MOVE_ERROR"></span><span id="error_ds_cross_dom_move_error"></span>**Fehler-DS-DOM-Verschiebungs \_ \_ \_ \_ \_ Fehler**
</dt> <dd> <dl> <dt>

8216 (0x2018)
</dt> <dt>



Der angeforderte Domänen übergreifende Verschiebungs Vorgang konnte nicht ausgeführt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_GC_NOT_AVAILABLE"></span><span id="error_ds_gc_not_available"></span>**Fehler- \_ DS- \_ GC \_ nicht \_ verfügbar**
</dt> <dd> <dl> <dt>

8217 (0x2019)
</dt> <dt>



Es kann keine Verbindung mit dem globalen Katalogserver hergestellt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_SHARED_POLICY"></span><span id="error_shared_policy"></span>**fehlerfrei \_ gegebene \_ Richtlinie**
</dt> <dd> <dl> <dt>

8218 (0x201a)
</dt> <dt>



Das Policy-Objekt ist freigegeben und kann nur am Stamm geändert werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_POLICY_OBJECT_NOT_FOUND"></span><span id="error_policy_object_not_found"></span>**das Fehler \_ Richtlinien \_ Objekt wurde \_ nicht \_ gefunden.**
</dt> <dd> <dl> <dt>

8219 (0x201b)
</dt> <dt>



Das Richtlinien Objekt ist nicht vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_POLICY_ONLY_IN_DS"></span><span id="error_policy_only_in_ds"></span>**\_nur Fehler \_ Richtlinie \_ in \_ DS**
</dt> <dd> <dl> <dt>

8220 (0x201c)
</dt> <dt>



Die angeforderten Richtlinien Informationen befinden sich nur im Verzeichnisdienst.


</dt> </dl> </dd> <dt>

<span id="ERROR_PROMOTION_ACTIVE"></span><span id="error_promotion_active"></span>**Fehler bei herauf Stufung \_ \_ aktiv**
</dt> <dd> <dl> <dt>

8221 (0x201d)
</dt> <dt>



Eine Domänen Controller-herauf Stufung ist zurzeit aktiv.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_PROMOTION_ACTIVE"></span><span id="error_no_promotion_active"></span>**Fehler "keine herauf Stufung \_ \_ \_ aktiv"**
</dt> <dd> <dl> <dt>

8222 (0x201e)
</dt> <dt>



Eine Domänen Controller-herauf Stufung ist zurzeit nicht aktiv.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OPERATIONS_ERROR"></span><span id="error_ds_operations_error"></span>**Fehler \_ DS- \_ Vorgangs \_ Fehler**
</dt> <dd> <dl> <dt>

8224 (0x2020)
</dt> <dt>



Ein Vorgangs Fehler ist aufgetreten.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_PROTOCOL_ERROR"></span><span id="error_ds_protocol_error"></span>**Fehler- \_ DS- \_ Protokoll \_ Fehler**
</dt> <dd> <dl> <dt>

8225 (0x2021)
</dt> <dt>



Es ist ein Protokollfehler aufgetreten.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_TIMELIMIT_EXCEEDED"></span><span id="error_ds_timelimit_exceeded"></span>**Fehler bei ' \_ \_ timelimit ' \_ überschritten.**
</dt> <dd> <dl> <dt>

8226 (0x2022)
</dt> <dt>



Das Zeitlimit für diese Anforderung wurde überschritten.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SIZELIMIT_EXCEEDED"></span><span id="error_ds_sizelimit_exceeded"></span>**Fehler " \_ DS \_ SizeLimit" \_ überschritten.**
</dt> <dd> <dl> <dt>

8227 (0x2023)
</dt> <dt>



Die Größenbeschränkung für diese Anforderung wurde überschritten.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ADMIN_LIMIT_EXCEEDED"></span><span id="error_ds_admin_limit_exceeded"></span>**Fehler- \_ DS- \_ Administrator \_ Limit \_ überschritten**
</dt> <dd> <dl> <dt>

8228 (0x2024)
</dt> <dt>



Der administrative Grenzwert für diese Anforderung wurde überschritten.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_COMPARE_FALSE"></span><span id="error_ds_compare_false"></span>**Fehler- \_ DS- \_ Vergleich \_ false**
</dt> <dd> <dl> <dt>

8229 (0x2025)
</dt> <dt>



Die Vergleichs Antwort war ' false '.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_COMPARE_TRUE"></span><span id="error_ds_compare_true"></span>**Fehler- \_ DS mit \_ \_ true vergleichen**
</dt> <dd> <dl> <dt>

8230 (0x2026)
</dt> <dt>



Die Vergleichs Antwort war "true".


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_AUTH_METHOD_NOT_SUPPORTED"></span><span id="error_ds_auth_method_not_supported"></span>**Fehler-DS-Authentifizierungs \_ \_ \_ Methode \_ \_ wird nicht unterstützt.**
</dt> <dd> <dl> <dt>

8231 (0x2027)
</dt> <dt>



Die angeforderte Authentifizierungsmethode wird vom Server nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_STRONG_AUTH_REQUIRED"></span><span id="error_ds_strong_auth_required"></span>**Fehler \_ DS \_ starke Authentifizierung \_ \_ erforderlich.**
</dt> <dd> <dl> <dt>

8232 (0x2028)
</dt> <dt>



Für diesen Server ist eine sicherere Authentifizierungsmethode erforderlich.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INAPPROPRIATE_AUTH"></span><span id="error_ds_inappropriate_auth"></span>**Fehler- \_ DS- \_ ungeeignete Authentifizierung \_**
</dt> <dd> <dl> <dt>

8233 (0x2029)
</dt> <dt>



Nicht geeignete Authentifizierung.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_AUTH_UNKNOWN"></span><span id="error_ds_auth_unknown"></span>**Fehler \_ DS-Authentifizierung \_ \_ unbekannt**
</dt> <dd> <dl> <dt>

8234 (0x202a)
</dt> <dt>



Der Authentifizierungsmechanismus ist unbekannt.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_REFERRAL"></span><span id="error_ds_referral"></span>**Fehler- \_ DS- \_ Referenz**
</dt> <dd> <dl> <dt>

8235 (0x202b)
</dt> <dt>



Vom Server wurde eine Referenz zurückgegeben.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_UNAVAILABLE_CRIT_EXTENSION"></span><span id="error_ds_unavailable_crit_extension"></span>**Fehler- \_ DS nicht \_ Verfügbare \_ Crit- \_ Erweiterung**
</dt> <dd> <dl> <dt>

8236 (0x202c)
</dt> <dt>



Die angeforderte kritische Erweiterung wird vom Server nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CONFIDENTIALITY_REQUIRED"></span><span id="error_ds_confidentiality_required"></span>**Fehler- \_ DS- \_ Vertraulichkeit \_ erforderlich**
</dt> <dd> <dl> <dt>

8237 (0x202d)
</dt> <dt>



Für diese Anforderung ist eine sichere Verbindung erforderlich.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INAPPROPRIATE_MATCHING"></span><span id="error_ds_inappropriate_matching"></span>**Fehler- \_ DS- \_ ungeeignet \_**
</dt> <dd> <dl> <dt>

8238 (0x202e)
</dt> <dt>



Ungeeignete Übereinstimmung.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CONSTRAINT_VIOLATION"></span><span id="error_ds_constraint_violation"></span>**Fehler-DS-Einschränkungs \_ \_ \_ Verletzung**
</dt> <dd> <dl> <dt>

8239 (0x202f)
</dt> <dt>



Eine Einschränkungs Verletzung ist aufgetreten.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_SUCH_OBJECT"></span><span id="error_ds_no_such_object"></span>**Fehler- \_ DS ist \_ kein \_ solches \_ Objekt**
</dt> <dd> <dl> <dt>

8240 (0x2030)
</dt> <dt>



Ein solches Objekt ist auf dem Server nicht vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ALIAS_PROBLEM"></span><span id="error_ds_alias_problem"></span>**Fehler- \_ DS- \_ Alias \_ Problem**
</dt> <dd> <dl> <dt>

8241 (0x2031)
</dt> <dt>



Es liegt ein Alias Problem vor.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INVALID_DN_SYNTAX"></span><span id="error_ds_invalid_dn_syntax"></span>**Fehler- \_ DS \_ ungültige \_ DN- \_ Syntax**
</dt> <dd> <dl> <dt>

8242 (0x2032)
</dt> <dt>



Es wurde eine ungültige DN-Syntax angegeben.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_IS_LEAF"></span><span id="error_ds_is_leaf"></span>**Fehler- \_ DS \_ ist \_ Blatt**
</dt> <dd> <dl> <dt>

8243 (0x2033)
</dt> <dt>



Das-Objekt ist ein Blatt Objekt.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ALIAS_DEREF_PROBLEM"></span><span id="error_ds_alias_deref_problem"></span>**Fehler- \_ DS- \_ Alias- \_ Deref- \_ Problem**
</dt> <dd> <dl> <dt>

8244 (0x2034)
</dt> <dt>



Es gibt ein Alias Dereferenzierungsproblem.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_UNWILLING_TO_PERFORM"></span><span id="error_ds_unwilling_to_perform"></span>**Fehler- \_ DS ist \_ nicht \_ zur \_ Ausführung bereit**
</dt> <dd> <dl> <dt>

8245 (0x2035)
</dt> <dt>



Der Server kann die Anforderung nicht verarbeiten.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_LOOP_DETECT"></span><span id="error_ds_loop_detect"></span>**Fehler- \_ DS- \_ Schleifen \_ Erkennung**
</dt> <dd> <dl> <dt>

8246 (0x2036)
</dt> <dt>



Eine-Schleife wurde erkannt.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAMING_VIOLATION"></span><span id="error_ds_naming_violation"></span>**Fehler- \_ DS- \_ Benennungs \_ Verletzung**
</dt> <dd> <dl> <dt>

8247 (0x2037)
</dt> <dt>



Es gibt eine Benennungs Verletzung.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OBJECT_RESULTS_TOO_LARGE"></span><span id="error_ds_object_results_too_large"></span>**Fehler- \_ DS- \_ Objekt \_ Ergebnisse \_ zu \_ groß**
</dt> <dd> <dl> <dt>

8248 (0x2038)
</dt> <dt>



Das Resultset ist zu groß.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_AFFECTS_MULTIPLE_DSAS"></span><span id="error_ds_affects_multiple_dsas"></span>**Fehler- \_ DS wirkt sich auf \_ \_ mehrere \_ DSAs aus**
</dt> <dd> <dl> <dt>

8249 (0x2039)
</dt> <dt>



Der Vorgang wirkt sich auf mehrere DSAs aus.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SERVER_DOWN"></span><span id="error_ds_server_down"></span>**Fehler \_ DS- \_ Server \_ nach unten**
</dt> <dd> <dl> <dt>

8250 (0x203a)
</dt> <dt>



Der Server ist nicht funktionstüchtig.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_LOCAL_ERROR"></span><span id="error_ds_local_error"></span>**Fehler- \_ DS \_ local- \_ Fehler**
</dt> <dd> <dl> <dt>

8251 (0x203b)
</dt> <dt>



Ein lokaler Fehler ist aufgetreten.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ENCODING_ERROR"></span><span id="error_ds_encoding_error"></span>**Fehler- \_ DS- \_ Codierungs \_ Fehler**
</dt> <dd> <dl> <dt>

8252 (0x203c)
</dt> <dt>



Es ist ein Codierungsfehler aufgetreten.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DECODING_ERROR"></span><span id="error_ds_decoding_error"></span>**Fehler \_ DS- \_ Decodierungs \_ Fehler**
</dt> <dd> <dl> <dt>

8253 (0x203d)
</dt> <dt>



Ein Decodierungs Fehler ist aufgetreten.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_FILTER_UNKNOWN"></span><span id="error_ds_filter_unknown"></span>**Fehler- \_ DS- \_ Filter \_ unbekannt**
</dt> <dd> <dl> <dt>

8254 (0x203e)
</dt> <dt>



Der Suchfilter kann nicht erkannt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_PARAM_ERROR"></span><span id="error_ds_param_error"></span>**Fehler \_ DS- \_ param- \_ Fehler**
</dt> <dd> <dl> <dt>

8255 (0x203f)
</dt> <dt>



Mindestens ein Parameter ist unzulässig.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NOT_SUPPORTED"></span><span id="error_ds_not_supported"></span>**Fehler- \_ DS \_ nicht \_ unterstützt**
</dt> <dd> <dl> <dt>

8256 (0x2040)
</dt> <dt>



Die angegebene Methode wird nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_RESULTS_RETURNED"></span><span id="error_ds_no_results_returned"></span>**Fehler " \_ DS \_ keine \_ Ergebnisse \_ zurückgegeben"**
</dt> <dd> <dl> <dt>

8257 (0x2041)
</dt> <dt>



Es wurden keine Ergebnisse zurückgegeben.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CONTROL_NOT_FOUND"></span><span id="error_ds_control_not_found"></span>**Fehler- \_ DS- \_ Steuerelement \_ nicht \_ gefunden**
</dt> <dd> <dl> <dt>

8258 (0x2042)
</dt> <dt>



Das angegebene Steuerelement wird vom Server nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CLIENT_LOOP"></span><span id="error_ds_client_loop"></span>**Fehler- \_ DS- \_ Client \_ Schleife**
</dt> <dd> <dl> <dt>

8259 (0x2043)
</dt> <dt>



Vom Client wurde eine Verweis Schleife erkannt.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_REFERRAL_LIMIT_EXCEEDED"></span><span id="error_ds_referral_limit_exceeded"></span>**Fehler- \_ DS- \_ Verweis \_ Limit \_ überschritten**
</dt> <dd> <dl> <dt>

8260 (0x2044)
</dt> <dt>



Das Limit für den voreingestellten Verweis wurde überschritten.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SORT_CONTROL_MISSING"></span><span id="error_ds_sort_control_missing"></span>**Fehler der \_ DS- \_ Sortier \_ Steuerung \_ fehlt.**
</dt> <dd> <dl> <dt>

8261 (0x2045)
</dt> <dt>



Die Suche erfordert ein SORT-Steuerelement.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OFFSET_RANGE_ERROR"></span><span id="error_ds_offset_range_error"></span>**Fehler- \_ DS- \_ Offset \_ Bereichs \_ Fehler**
</dt> <dd> <dl> <dt>

8262 (0x2046)
</dt> <dt>



Die Suchergebnisse überschreiten den angegebenen Offset Bereich.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_RIDMGR_DISABLED"></span><span id="error_ds_ridmgr_disabled"></span>**Fehler \_ DS \_ ridmgr \_ deaktiviert**
</dt> <dd> <dl> <dt>

8263 (0x2047)
</dt> <dt>



Der Verzeichnisdienst hat festgestellt, dass das Subsystem, von dem relative Bezeichner zugewiesen werden, deaktiviert ist. Dies kann als Schutzmechanismus auftreten, wenn das System festlegt, dass ein signifikanter Anteil relativer Bezeichner (RIDs) erschöpft ist. <https://go.microsoft.com/fwlink/p/?linkid=228610>Die empfohlenen Diagnose Schritte und das Verfahren zum erneuten Aktivieren der Kontoerstellung finden Sie unter.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ROOT_MUST_BE_NC"></span><span id="error_ds_root_must_be_nc"></span>**Fehler \_ DS-Stamm \_ \_ muss \_ \_ NC sein**
</dt> <dd> <dl> <dt>

8301 (0x206d)
</dt> <dt>



Das Stamm Objekt muss den Anfang eines Namens Kontexts aufweisen. Das Stamm Objekt kann kein instanziertes übergeordnetes Element aufweisen.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ADD_REPLICA_INHIBITED"></span><span id="error_ds_add_replica_inhibited"></span>**Fehler- \_ DS \_ Add Replica- \_ Replikat \_**
</dt> <dd> <dl> <dt>

8302 (0x206e)
</dt> <dt>



Der Vorgang Replikat hinzufügen kann nicht ausgeführt werden. Der namens Kontext muss beschreibbar sein, damit das Replikat erstellt werden kann.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ATT_NOT_DEF_IN_SCHEMA"></span><span id="error_ds_att_not_def_in_schema"></span>**Fehler " \_ DS- \_ ATT \_ nicht def" \_ \_ im \_ Schema**
</dt> <dd> <dl> <dt>

8303 (0x206f)
</dt> <dt>



Ein Verweis auf ein Attribut, das nicht im Schema definiert ist, ist aufgetreten.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MAX_OBJ_SIZE_EXCEEDED"></span><span id="error_ds_max_obj_size_exceeded"></span>**Fehler \_ DS \_ Maximale \_ obj- \_ Größe \_ überschritten**
</dt> <dd> <dl> <dt>

8304 (0x2070)
</dt> <dt>



Die maximale Größe eines Objekts wurde überschritten.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OBJ_STRING_NAME_EXISTS"></span><span id="error_ds_obj_string_name_exists"></span>**Fehler \_ DS \_ obj \_ Zeichen folgen \_ Name ist \_ vorhanden.**
</dt> <dd> <dl> <dt>

8305 (0x2071)
</dt> <dt>



Es wurde versucht, ein Objekt mit einem Namen, der bereits verwendet wird, dem Verzeichnis hinzuzufügen.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_RDN_DEFINED_IN_SCHEMA"></span><span id="error_ds_no_rdn_defined_in_schema"></span>**Fehler \_ - \_ DS \_ \_ \_ im \_ Schema ist kein RDN definiert.**
</dt> <dd> <dl> <dt>

8306 (0x2072)
</dt> <dt>



Es wurde versucht, ein Objekt einer Klasse hinzuzufügen, für die im Schema kein RDN definiert ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_RDN_DOESNT_MATCH_SCHEMA"></span><span id="error_ds_rdn_doesnt_match_schema"></span>**Fehler \_ DS \_ RDN \_ stimmt nicht \_ mit \_ Schema identisch**
</dt> <dd> <dl> <dt>

8307 (0x2073)
</dt> <dt>



Es wurde versucht, ein Objekt mithilfe eines RDN hinzuzufügen, der nicht dem im Schema definierten RDN entspricht.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_REQUESTED_ATTS_FOUND"></span><span id="error_ds_no_requested_atts_found"></span>**Fehler \_ DS \_ keine \_ angeforderten \_ ATTS \_ gefunden.**
</dt> <dd> <dl> <dt>

8308 (0x2074)
</dt> <dt>



Keines der angeforderten Attribute wurde für die Objekte gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_USER_BUFFER_TO_SMALL"></span><span id="error_ds_user_buffer_to_small"></span>**Fehler " \_ DS- \_ Benutzer \_ Puffer \_ zu \_ klein"**
</dt> <dd> <dl> <dt>

8309 (0x2075)
</dt> <dt>



Der Benutzer Puffer ist zu klein.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ATT_IS_NOT_ON_OBJ"></span><span id="error_ds_att_is_not_on_obj"></span>**Fehler " \_ DS \_ ATT" \_ befindet sich \_ nicht \_ im \_ obj.**
</dt> <dd> <dl> <dt>

8310 (0x2076)
</dt> <dt>



Das im-Vorgang angegebene-Attribut ist für das-Objekt nicht vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ILLEGAL_MOD_OPERATION"></span><span id="error_ds_illegal_mod_operation"></span>**Fehler DS unzulässiger \_ \_ mod- \_ \_ Vorgang**
</dt> <dd> <dl> <dt>

8311 (0x2077)
</dt> <dt>



Ungültiger Änderungs Vorgang. Ein Aspekt der Änderung ist nicht zulässig.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OBJ_TOO_LARGE"></span><span id="error_ds_obj_too_large"></span>**Fehler " \_ DS \_ obj" \_ zu \_ groß.**
</dt> <dd> <dl> <dt>

8312 (0x2078)
</dt> <dt>



Das angegebene Objekt ist zu groß.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_BAD_INSTANCE_TYPE"></span><span id="error_ds_bad_instance_type"></span>**Fehler \_ DS fehlerhafter \_ \_ \_ Instanztyp**
</dt> <dd> <dl> <dt>

8313 (0x2079)
</dt> <dt>



Der angegebene Instanztyp ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MASTERDSA_REQUIRED"></span><span id="error_ds_masterdsa_required"></span>**Fehler- \_ DS- \_ MasterDSA \_ erforderlich**
</dt> <dd> <dl> <dt>

8314 (0x207a)
</dt> <dt>



Der Vorgang muss an einer Master-DSA ausgeführt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OBJECT_CLASS_REQUIRED"></span><span id="error_ds_object_class_required"></span>**Fehler- \_ DS- \_ Objekt \_ Klasse \_ erforderlich**
</dt> <dd> <dl> <dt>

8315 (0x207b)
</dt> <dt>



Das Objektklassen Attribut muss angegeben werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MISSING_REQUIRED_ATT"></span><span id="error_ds_missing_required_att"></span>**Fehler- \_ DS \_ fehlendes \_ Erforderliches \_ ATT**
</dt> <dd> <dl> <dt>

8316 (0x207c)
</dt> <dt>



Ein erforderliches Attribut fehlt.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ATT_NOT_DEF_FOR_CLASS"></span><span id="error_ds_att_not_def_for_class"></span>**Fehler \_ DS- \_ ATT \_ nicht \_ DEF \_ für \_ Klasse**
</dt> <dd> <dl> <dt>

8317 (0x207d)
</dt> <dt>



Es wurde versucht, ein Objekt so zu ändern, dass es ein Attribut enthält, das für seine Klasse nicht zulässig ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ATT_ALREADY_EXISTS"></span><span id="error_ds_att_already_exists"></span>**Fehler \_ DS- \_ ATT ist \_ bereits \_ vorhanden.**
</dt> <dd> <dl> <dt>

8318 (0x207e)
</dt> <dt>



Das angegebene Attribut ist für das Objekt bereits vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_ADD_ATT_VALUES"></span><span id="error_ds_cant_add_att_values"></span>**Fehler \_ DS Fehler beim \_ \_ Hinzufügen von \_ ATT- \_ Werten**
</dt> <dd> <dl> <dt>

8320 (0x2080)
</dt> <dt>



Das angegebene Attribut ist nicht vorhanden oder weist keine Werte auf.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SINGLE_VALUE_CONSTRAINT"></span><span id="error_ds_single_value_constraint"></span>**Fehler- \_ DS- \_ Einschränkung mit einem \_ Wert \_**
</dt> <dd> <dl> <dt>

8321 (0x2081)
</dt> <dt>



Für ein Attribut, das nur über einen Wert verfügen kann, wurden mehrere Werte angegeben.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_RANGE_CONSTRAINT"></span><span id="error_ds_range_constraint"></span>**Fehler- \_ DS- \_ Bereichs \_ Einschränkung**
</dt> <dd> <dl> <dt>

8322 (0x2082)
</dt> <dt>



Ein Wert für das-Attribut war nicht im zulässigen Wertebereich.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ATT_VAL_ALREADY_EXISTS"></span><span id="error_ds_att_val_already_exists"></span>**Fehler \_ DS \_ ATT \_ Val ist \_ bereits \_ vorhanden.**
</dt> <dd> <dl> <dt>

8323 (0x2083)
</dt> <dt>



Der angegebene Wert ist bereits vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_REM_MISSING_ATT"></span><span id="error_ds_cant_rem_missing_att"></span>**Fehler DS-Fehler " \_ DS nicht \_ \_ \_ vorhanden \_ ".**
</dt> <dd> <dl> <dt>

8324 (0x2084)
</dt> <dt>



Das Attribut kann nicht entfernt werden, weil es für das Objekt nicht vorhanden ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_REM_MISSING_ATT_VAL"></span><span id="error_ds_cant_rem_missing_att_val"></span>**Fehler \_ " \_ DS \_ \_ \_ \_**
</dt> <dd> <dl> <dt>

8325 (0x2085)
</dt> <dt>



Der Attribut Wert kann nicht entfernt werden, weil er im Objekt nicht vorhanden ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ROOT_CANT_BE_SUBREF"></span><span id="error_ds_root_cant_be_subref"></span>**Fehler "DS-Stamm" darf kein unter Bericht \_ \_ \_ \_ sein \_ .**
</dt> <dd> <dl> <dt>

8326 (0x2086)
</dt> <dt>



Das angegebene Stamm Objekt kann kein unter Bericht sein.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_CHAINING"></span><span id="error_ds_no_chaining"></span>**Fehler- \_ DS \_ keine \_ Verkettung**
</dt> <dd> <dl> <dt>

8327 (0x2087)
</dt> <dt>



Verkettung ist nicht zulässig.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_CHAINED_EVAL"></span><span id="error_ds_no_chained_eval"></span>**Fehler- \_ DS \_ keine \_ verkettete \_ Eval**
</dt> <dd> <dl> <dt>

8328 (0x2088)
</dt> <dt>



Verkettete Auswertung ist nicht zulässig.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_PARENT_OBJECT"></span><span id="error_ds_no_parent_object"></span>**Fehler " \_ DS \_ kein über \_ geordnetes \_ Objekt"**
</dt> <dd> <dl> <dt>

8329 (0x2089)
</dt> <dt>



Der Vorgang konnte nicht ausgeführt werden, da das übergeordnete Objekt instanziiert oder gelöscht wurde.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_PARENT_IS_AN_ALIAS"></span><span id="error_ds_parent_is_an_alias"></span>**Fehler- \_ DS über \_ geordnetes Element \_ ist \_ ein \_ Alias**
</dt> <dd> <dl> <dt>

8330 (0x208a)
</dt> <dt>



Ein übergeordnetes Element, das ein Alias ist, ist nicht zulässig. Aliase sind Blattobjekte.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_MIX_MASTER_AND_REPS"></span><span id="error_ds_cant_mix_master_and_reps"></span>**Fehler \_ -DS-Fehler beim \_ \_ Mischen von \_ Master \_ und \_ Reps**
</dt> <dd> <dl> <dt>

8331 (0x208b)
</dt> <dt>



Das Objekt und das übergeordnete Element müssen denselben Typ aufweisen, entweder sowohl Master als auch beide Replikate.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CHILDREN_EXIST"></span><span id="error_ds_children_exist"></span>**Fehler DS untergeordnete Elemente \_ \_ \_ vorhanden**
</dt> <dd> <dl> <dt>

8332 (0x208c)
</dt> <dt>



Der Vorgang kann nicht ausgeführt werden, da untergeordnete Objekte vorhanden sind. Dieser Vorgang kann nur für ein Blatt Objekt ausgeführt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OBJ_NOT_FOUND"></span><span id="error_ds_obj_not_found"></span>**Fehler " \_ DS \_ obj" \_ nicht \_ gefunden.**
</dt> <dd> <dl> <dt>

8333 (0x208d)
</dt> <dt>



Das Verzeichnis Objekt wurde nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ALIASED_OBJ_MISSING"></span><span id="error_ds_aliased_obj_missing"></span>**Fehler \_ beim \_ Alias "Aliasing \_ obj". \_**
</dt> <dd> <dl> <dt>

8334 (0x208e)
</dt> <dt>



Das Alias Objekt fehlt.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_BAD_NAME_SYNTAX"></span><span id="error_ds_bad_name_syntax"></span>**Fehler DS-Syntax für ungültigen \_ \_ \_ Namen \_**
</dt> <dd> <dl> <dt>

8335 (0x208f)
</dt> <dt>



Der Objektname weist eine ungültige Syntax auf.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ALIAS_POINTS_TO_ALIAS"></span><span id="error_ds_alias_points_to_alias"></span>**Fehler- \_ DS- \_ Alias \_ verweist \_ auf \_ Alias**
</dt> <dd> <dl> <dt>

8336 (0x2090)
</dt> <dt>



Es ist nicht zulässig, dass ein Alias auf einen anderen Alias verweist.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_DEREF_ALIAS"></span><span id="error_ds_cant_deref_alias"></span>**Fehler \_ DS \_ cant \_ Deref- \_ Alias**
</dt> <dd> <dl> <dt>

8337 (0x2091)
</dt> <dt>



Der Alias kann nicht dereferenziert werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OUT_OF_SCOPE"></span><span id="error_ds_out_of_scope"></span>**Fehler- \_ DS \_ außerhalb des Gültigkeits \_ \_ Bereichs**
</dt> <dd> <dl> <dt>

8338 (0x2092)
</dt> <dt>



Der Vorgang liegt außerhalb des Gültigkeits Bereichs.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OBJECT_BEING_REMOVED"></span><span id="error_ds_object_being_removed"></span>**Fehler- \_ DS- \_ Objekt \_ wird \_ entfernt.**
</dt> <dd> <dl> <dt>

8339 (0x2093)
</dt> <dt>



Der Vorgang kann nicht fortgesetzt werden, da das Objekt gerade entfernt wird.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_DELETE_DSA_OBJ"></span><span id="error_ds_cant_delete_dsa_obj"></span>**Fehler \_ DS \_ , \_ \_ DSA- \_ obj nicht löschen**
</dt> <dd> <dl> <dt>

8340 (0x2094)
</dt> <dt>



Das DSA-Objekt kann nicht gelöscht werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_GENERIC_ERROR"></span><span id="error_ds_generic_error"></span>**Fehler \_ DS \_ allgemeiner \_ Fehler**
</dt> <dd> <dl> <dt>

8341 (0x2095)
</dt> <dt>



Ein Verzeichnisdienst Fehler ist aufgetreten.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DSA_MUST_BE_INT_MASTER"></span><span id="error_ds_dsa_must_be_int_master"></span>**Fehler \_ DS \_ DSA \_ muss \_ \_ int \_ Master sein.**
</dt> <dd> <dl> <dt>

8342 (0x2096)
</dt> <dt>



Der Vorgang kann nur auf einem internen Master-DSA-Objekt ausgeführt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CLASS_NOT_DSA"></span><span id="error_ds_class_not_dsa"></span>**Fehler- \_ DS- \_ Klasse \_ nicht \_ DSA**
</dt> <dd> <dl> <dt>

8343 (0x2097)
</dt> <dt>



Das Objekt muss aus der Klasse DSA bestehen.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INSUFF_ACCESS_RIGHTS"></span><span id="error_ds_insuff_access_rights"></span>**Fehler \_ DS \_ sichert \_ Zugriffs \_ Rechte**
</dt> <dd> <dl> <dt>

8344 (0x2098)
</dt> <dt>



Unzureichende Zugriffsrechte zum Ausführen des Vorgangs.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ILLEGAL_SUPERIOR"></span><span id="error_ds_illegal_superior"></span>**Fehler-DS unzulässig. \_ \_ \_**
</dt> <dd> <dl> <dt>

8345 (0x2099)
</dt> <dt>



Das Objekt kann nicht hinzugefügt werden, da das übergeordnete Element nicht in der Liste der möglichen Vorgesetzten enthalten ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ATTRIBUTE_OWNED_BY_SAM"></span><span id="error_ds_attribute_owned_by_sam"></span>**Fehler- \_ DS- \_ Attribut \_ im Besitz \_ von \_ Sam**
</dt> <dd> <dl> <dt>

8346 (0x209a)
</dt> <dt>



Der Zugriff auf das-Attribut ist nicht zulässig, da das-Attribut im Besitz der Sicherheits Konten Verwaltung (Security Accounts Manager, Sam) ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_TOO_MANY_PARTS"></span><span id="error_ds_name_too_many_parts"></span>**Fehler- \_ DS- \_ Name \_ zu \_ viele \_ Teile**
</dt> <dd> <dl> <dt>

8347 (0x209b)
</dt> <dt>



Der Name enthält zu viele Teile.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_TOO_LONG"></span><span id="error_ds_name_too_long"></span>**Fehler- \_ DS- \_ Name \_ zu \_ lang**
</dt> <dd> <dl> <dt>

8348 (0x209c)
</dt> <dt>



Der Name ist zu lang.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_VALUE_TOO_LONG"></span><span id="error_ds_name_value_too_long"></span>**Fehler \_ DS- \_ namens \_ Wert \_ zu \_ lang**
</dt> <dd> <dl> <dt>

8349 (0x209d)
</dt> <dt>



Der Name-Wert ist zu lang.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_UNPARSEABLE"></span><span id="error_ds_name_unparseable"></span>**Fehler " \_ DS- \_ Name" \_ kann nicht analysiert werden.**
</dt> <dd> <dl> <dt>

8350 (0x209e)
</dt> <dt>



Der Verzeichnisdienst hat einen Fehler beim Auswerten eines Namens gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_TYPE_UNKNOWN"></span><span id="error_ds_name_type_unknown"></span>**Fehler beim \_ DS- \_ \_ Namenstyp \_ unbekannt**
</dt> <dd> <dl> <dt>

8351 (0x209f)
</dt> <dt>



Der Verzeichnisdienst kann den Attributtyp für einen Namen nicht erhalten.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NOT_AN_OBJECT"></span><span id="error_ds_not_an_object"></span>**Fehler- \_ DS ist \_ kein \_ \_ Objekt.**
</dt> <dd> <dl> <dt>

8352 (0x20a0)
</dt> <dt>



Der Name identifiziert kein Objekt. der Name identifiziert einen Phantom.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SEC_DESC_TOO_SHORT"></span><span id="error_ds_sec_desc_too_short"></span>**Fehler " \_ DS \_ Sek. \_ \_ zu \_ kurz"**
</dt> <dd> <dl> <dt>

8353 (0x20a1)
</dt> <dt>



Die Sicherheits Beschreibung ist zu kurz.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SEC_DESC_INVALID"></span><span id="error_ds_sec_desc_invalid"></span>**Fehler \_ DS \_ Sek., \_ \_ Ungültiger Fehler**
</dt> <dd> <dl> <dt>

8354 (0x20a2)
</dt> <dt>



Die Sicherheits Beschreibung ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_DELETED_NAME"></span><span id="error_ds_no_deleted_name"></span>**Fehler " \_ DS \_ kein \_ gelöschter \_ Name"**
</dt> <dd> <dl> <dt>

8355 (0x20a3)
</dt> <dt>



Fehler beim Erstellen des Namens für das gelöschte Objekt.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SUBREF_MUST_HAVE_PARENT"></span><span id="error_ds_subref_must_have_parent"></span>**Fehler-DS-unter Bericht \_ \_ \_ muss \_ übergeordnetes Element aufweisen \_**
</dt> <dd> <dl> <dt>

8356 (0x20a4)
</dt> <dt>



Das übergeordnete Element eines neuen unter Berichts muss vorhanden sein.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NCNAME_MUST_BE_NC"></span><span id="error_ds_ncname_must_be_nc"></span>**Fehler \_ ' \_ NCName ' \_ muss ' \_ NC ' sein \_ .**
</dt> <dd> <dl> <dt>

8357 (0x20a5)
</dt> <dt>



Das Objekt muss ein namens Kontext sein.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_ADD_SYSTEM_ONLY"></span><span id="error_ds_cant_add_system_only"></span>**Fehler DS-Fehler beim \_ \_ \_ Hinzufügen des \_ Systems \_ .**
</dt> <dd> <dl> <dt>

8358 (0x20a6)
</dt> <dt>



Es ist nicht zulässig, ein Attribut hinzuzufügen, das im Besitz des Systems ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CLASS_MUST_BE_CONCRETE"></span><span id="error_ds_class_must_be_concrete"></span>**Fehler- \_ DS- \_ Klasse \_ muss \_ \_ konkret sein**
</dt> <dd> <dl> <dt>

8359 (0x20a7)
</dt> <dt>



Die Klasse des Objekts muss strukturell sein. eine abstrakte Klasse kann nicht instanziiert werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INVALID_DMD"></span><span id="error_ds_invalid_dmd"></span>**Fehler- \_ DS \_ ungültige \_ DMD**
</dt> <dd> <dl> <dt>

8360 (0x20a8)
</dt> <dt>



Das Schema Objekt konnte nicht gefunden werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OBJ_GUID_EXISTS"></span><span id="error_ds_obj_guid_exists"></span>**Fehler \_ DS \_ obj- \_ GUID \_ vorhanden**
</dt> <dd> <dl> <dt>

8361 (0x20a9)
</dt> <dt>



Ein lokales Objekt mit dieser GUID ("Dead" oder "Alive") ist bereits vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NOT_ON_BACKLINK"></span><span id="error_ds_not_on_backlink"></span>**Fehler- \_ DS \_ nicht \_ auf \_ Backlink**
</dt> <dd> <dl> <dt>

8362 (0x20aa)
</dt> <dt>



Der Vorgang kann nicht für einen backbackink ausgeführt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_CROSSREF_FOR_NC"></span><span id="error_ds_no_crossref_for_nc"></span>**Fehler " \_ DS \_ No \_ CrossRef" \_ für \_ NC**
</dt> <dd> <dl> <dt>

8363 (0x20ab)
</dt> <dt>



Der Querverweis für den angegebenen Namens Kontext konnte nicht gefunden werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SHUTTING_DOWN"></span><span id="error_ds_shutting_down"></span>**Fehler-DS wird herunter \_ \_ \_ Gefahren**
</dt> <dd> <dl> <dt>

8364 (0x20ac)
</dt> <dt>



Der Vorgang konnte nicht ausgeführt werden, da der Verzeichnisdienst heruntergefahren wird.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_UNKNOWN_OPERATION"></span><span id="error_ds_unknown_operation"></span>**Fehler \_ DS \_ unbekannter \_ Vorgang**
</dt> <dd> <dl> <dt>

8365 (0x20ad)
</dt> <dt>



Das Verzeichnis Service Request ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INVALID_ROLE_OWNER"></span><span id="error_ds_invalid_role_owner"></span>**Fehler \_ DS \_ ungültiger \_ Rollen \_ Besitzer**
</dt> <dd> <dl> <dt>

8366 (0x20ae)
</dt> <dt>



Das Rollen Besitzer Attribut konnte nicht gelesen werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_COULDNT_CONTACT_FSMO"></span><span id="error_ds_couldnt_contact_fsmo"></span>**Fehler- \_ DS \_ konnte keine \_ Verbindung mit \_ dem Dienst**
</dt> <dd> <dl> <dt>

8367 (0x20af)
</dt> <dt>



Der angeforderte FSMO-Vorgang konnte nicht ausgeführt werden. Der aktuelle FSMO-Inhaber war nicht erreichbar.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CROSS_NC_DN_RENAME"></span><span id="error_ds_cross_nc_dn_rename"></span>**Fehler- \_ DS- \_ Kreuz NC-DN- \_ \_ \_ Umbenennung**
</dt> <dd> <dl> <dt>

8368 (0x20b0)
</dt> <dt>



Die Änderung eines DN in einem Benennungs Kontext ist nicht zulässig.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_MOD_SYSTEM_ONLY"></span><span id="error_ds_cant_mod_system_only"></span>**Fehler \_ DS \_ nicht \_ \_ nur System \_ Fehler**
</dt> <dd> <dl> <dt>

8369 (0x20b1)
</dt> <dt>



Das Attribut kann nicht geändert werden, da es im Besitz des Systems ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_REPLICATOR_ONLY"></span><span id="error_ds_replicator_only"></span>**nur Fehler- \_ DS- \_ Replikator \_**
</dt> <dd> <dl> <dt>

8370 (0x20b2)
</dt> <dt>



Diese Funktion kann nur vom Replikator durchgeführt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OBJ_CLASS_NOT_DEFINED"></span><span id="error_ds_obj_class_not_defined"></span>**Fehler \_ DS \_ obj- \_ Klasse \_ nicht \_ definiert**
</dt> <dd> <dl> <dt>

8371 (0x20b3)
</dt> <dt>



Die angegebene Klasse ist nicht definiert.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OBJ_CLASS_NOT_SUBCLASS"></span><span id="error_ds_obj_class_not_subclass"></span>**Fehler \_ DS \_ obj- \_ Klasse \_ nicht \_ Unterklasse**
</dt> <dd> <dl> <dt>

8372 (0x20b4)
</dt> <dt>



Die angegebene Klasse ist keine Unterklasse.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_REFERENCE_INVALID"></span><span id="error_ds_name_reference_invalid"></span>**Fehler \_ DS- \_ namens \_ Verweis \_ ungültig**
</dt> <dd> <dl> <dt>

8373 (0x20b5)
</dt> <dt>



Der namens Verweis ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CROSS_REF_EXISTS"></span><span id="error_ds_cross_ref_exists"></span>**Fehler \_ DS-Querverweis ist \_ \_ \_ vorhanden.**
</dt> <dd> <dl> <dt>

8374 (0x20b6)
</dt> <dt>



Ein Querverweis ist bereits vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_DEL_MASTER_CROSSREF"></span><span id="error_ds_cant_del_master_crossref"></span>**Fehler- \_ DS-del-Master- \_ \_ \_ \_ CrossRef**
</dt> <dd> <dl> <dt>

8375 (0x20b7)
</dt> <dt>



Es ist nicht zulässig, einen Master-Querverweis zu löschen.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SUBTREE_NOTIFY_NOT_NC_HEAD"></span><span id="error_ds_subtree_notify_not_nc_head"></span>**Fehler- \_ DS- \_ Teilstruktur \_ Benachrichtigung \_ nicht NC- \_ \_ Kopfzeile**
</dt> <dd> <dl> <dt>

8376 (0x20b8)
</dt> <dt>



Teilstruktur Benachrichtigungen werden nur auf NC-Köpfen unterstützt.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NOTIFY_FILTER_TOO_COMPLEX"></span><span id="error_ds_notify_filter_too_complex"></span>**Fehler- \_ DS \_ Benachrichtigungs \_ Filter \_ zu \_ Komplex**
</dt> <dd> <dl> <dt>

8377 (0x20b9)
</dt> <dt>



Der Benachrichtigungs Filter ist zu komplex.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DUP_RDN"></span><span id="error_ds_dup_rdn"></span>**Fehler \_ DS \_ DUP \_ RDN**
</dt> <dd> <dl> <dt>

8378 (0x20ba)
</dt> <dt>



Fehler beim Aktualisieren des Schemas: doppelter RDN.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DUP_OID"></span><span id="error_ds_dup_oid"></span>**Fehler \_ DS \_ - \_ OID-OID**
</dt> <dd> <dl> <dt>

8379 (0x20bb)
</dt> <dt>



Fehler beim Aktualisieren des Schemas: doppelte OID.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DUP_MAPI_ID"></span><span id="error_ds_dup_mapi_id"></span>**Fehler \_ DS \_ DUP- \_ MAPI- \_ ID**
</dt> <dd> <dl> <dt>

8380 (0x20bc)
</dt> <dt>



Fehler beim Aktualisieren des Schemas: doppelter MAPI-Bezeichner.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DUP_SCHEMA_ID_GUID"></span><span id="error_ds_dup_schema_id_guid"></span>**Fehler- \_ DS-Schema-ID- \_ \_ \_ \_ GUID**
</dt> <dd> <dl> <dt>

8381 (0x20bd)
</dt> <dt>



Fehler beim Aktualisieren des Schemas: doppelte Schema-ID-GUID.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DUP_LDAP_DISPLAY_NAME"></span><span id="error_ds_dup_ldap_display_name"></span>**Fehler "DS", \_ \_ LDAP- \_ \_ Anzeige \_ Name**
</dt> <dd> <dl> <dt>

8382 (0x20be)
</dt> <dt>



Fehler beim Aktualisieren des Schemas: doppelter LDAP-Anzeige Name.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SEMANTIC_ATT_TEST"></span><span id="error_ds_semantic_att_test"></span>**Fehler- \_ DS \_ Semantic ATT- \_ \_ Test**
</dt> <dd> <dl> <dt>

8383 (0x20bf)
</dt> <dt>



Fehler beim Aktualisieren des Schemas: Bereich-kleiner als oberer Bereich.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SYNTAX_MISMATCH"></span><span id="error_ds_syntax_mismatch"></span>**Fehler- \_ DS- \_ Syntax Konflikt \_**
</dt> <dd> <dl> <dt>

8384 (0x20c0)
</dt> <dt>



Fehler beim Aktualisieren des Schemas: Syntax stimmt nicht überein.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_EXISTS_IN_MUST_HAVE"></span><span id="error_ds_exists_in_must_have"></span>**Fehler \_ - \_ DS \_ in \_ muss vorhanden \_ sein**
</dt> <dd> <dl> <dt>

8385 (0x20c1)
</dt> <dt>



Fehler beim Löschen des Schemas: das Attribut wird in "muss enthalten" verwendet.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_EXISTS_IN_MAY_HAVE"></span><span id="error_ds_exists_in_may_have"></span>**\_der Fehler DS ist \_ \_ in \_ möglicherweise vorhanden \_ .**
</dt> <dd> <dl> <dt>

8386 (0x20c2)
</dt> <dt>



Fehler beim Löschen des Schemas: das Attribut wird in "Mai" verwendet.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NONEXISTENT_MAY_HAVE"></span><span id="error_ds_nonexistent_may_have"></span>**\_nicht vorhandene Fehler-DS \_ \_ verfügen möglicherweise \_ über**
</dt> <dd> <dl> <dt>

8387 (0x20c3)
</dt> <dt>



Fehler beim Aktualisieren des Schemas: das Attribut in "May-" ist nicht vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NONEXISTENT_MUST_HAVE"></span><span id="error_ds_nonexistent_must_have"></span>**\_ \_ nicht vorhandener Fehler-DS \_ muss \_**
</dt> <dd> <dl> <dt>

8388 (0x20c4)
</dt> <dt>



Fehler beim Aktualisieren des Schemas: das Attribut in "" darf nicht vorhanden sein.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_AUX_CLS_TEST_FAIL"></span><span id="error_ds_aux_cls_test_fail"></span>**Fehler \_ DS \_ aux \_ CLS- \_ Test \_ fehlgeschlagen**
</dt> <dd> <dl> <dt>

8389 (0x20c5)
</dt> <dt>



Fehler beim Aktualisieren des Schemas: die Klasse in der Liste der aux-Klassen ist nicht vorhanden oder keine Erweiterungs Klasse.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NONEXISTENT_POSS_SUP"></span><span id="error_ds_nonexistent_poss_sup"></span>**Fehler \_ DS \_ nicht vorhandener \_ Poss \_ SUP**
</dt> <dd> <dl> <dt>

8390 (0x20c6)
</dt> <dt>



Fehler beim Aktualisieren des Schemas: Klasse in Poss-Vorgesetzten ist nicht vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SUB_CLS_TEST_FAIL"></span><span id="error_ds_sub_cls_test_fail"></span>**Fehler- \_ DS \_ unter \_ CLS- \_ Test \_ fehlgeschlagen**
</dt> <dd> <dl> <dt>

8391 (0x20c7)
</dt> <dt>



Fehler beim Aktualisieren des Schemas: die Klasse in der Liste der Unterklassen ist nicht vorhanden oder entspricht nicht den Hierarchie Regeln.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_BAD_RDN_ATT_ID_SYNTAX"></span><span id="error_ds_bad_rdn_att_id_syntax"></span>**Fehler \_ DS fehlerhafte RDN-Fehler- \_ \_ \_ ID- \_ \_ Syntax**
</dt> <dd> <dl> <dt>

8392 (0x20c8)
</dt> <dt>



Fehler beim Aktualisieren des Schemas: RDN-ATT-ID weist falsche Syntax auf.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_EXISTS_IN_AUX_CLS"></span><span id="error_ds_exists_in_aux_cls"></span>**Fehler \_ - \_ DS \_ in \_ aux \_ CLS**
</dt> <dd> <dl> <dt>

8393 (0x20c9)
</dt> <dt>



Fehler beim Löschen des Schemas: die Klasse wird als Hilfsklasse verwendet.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_EXISTS_IN_SUB_CLS"></span><span id="error_ds_exists_in_sub_cls"></span>**Fehler \_ - \_ DS \_ in \_ Sub \_ CLS**
</dt> <dd> <dl> <dt>

8394 (0x20ca)
</dt> <dt>



Fehler beim Löschen des Schemas: die Klasse wird als Unterklasse verwendet.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_EXISTS_IN_POSS_SUP"></span><span id="error_ds_exists_in_poss_sup"></span>**Fehler \_ - \_ DS \_ im \_ Poss- \_ SUP**
</dt> <dd> <dl> <dt>

8395 (0x20cb)
</dt> <dt>



Fehler beim Löschen des Schemas: die Klasse wird als "Poss Superior" verwendet.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_RECALCSCHEMA_FAILED"></span><span id="error_ds_recalcschema_failed"></span>**Fehler bei \_ DS \_ recalcschema. \_**
</dt> <dd> <dl> <dt>

8396 (0x20cc)
</dt> <dt>



Fehler beim Neuberechnen des Überprüfungs Caches durch Schema Aktualisierung.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_TREE_DELETE_NOT_FINISHED"></span><span id="error_ds_tree_delete_not_finished"></span>**Fehler "DS-Struktur \_ \_ Löschen" \_ \_ nicht \_ abgeschlossen**
</dt> <dd> <dl> <dt>

8397 (0x20cd)
</dt> <dt>



Das Löschen der Struktur ist nicht abgeschlossen. Die Anforderung muss erneut erfolgen, damit das Löschen der Struktur fortgesetzt werden kann.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_DELETE"></span><span id="error_ds_cant_delete"></span>**Fehler \_ DS \_ nicht \_ Löschen**
</dt> <dd> <dl> <dt>

8398 (0x20ce)
</dt> <dt>



Der angeforderte Löschvorgang konnte nicht ausgeführt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ATT_SCHEMA_REQ_ID"></span><span id="error_ds_att_schema_req_id"></span>**Fehler \_ - \_ \_ ID: DS-Schema- \_ req- \_ ID**
</dt> <dd> <dl> <dt>

8399 (0x20cf)
</dt> <dt>



Der Bearbeiter-Klassen Bezeichner für den Schema Daten Satz kann nicht gelesen werden


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_BAD_ATT_SCHEMA_SYNTAX"></span><span id="error_ds_bad_att_schema_syntax"></span>**Fehler \_ DS ungültige \_ ATT- \_ \_ Schema \_ Syntax**
</dt> <dd> <dl> <dt>

8400 (0x20d0)
</dt> <dt>



Das Attribut Schema weist eine ungültige Syntax auf.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_CACHE_ATT"></span><span id="error_ds_cant_cache_att"></span>**Fehler " \_ DS- \_ cant- \_ Cache \_ "**
</dt> <dd> <dl> <dt>

8401 (0x20d1)
</dt> <dt>



Das Attribut konnte nicht zwischengespeichert werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_CACHE_CLASS"></span><span id="error_ds_cant_cache_class"></span>**Fehler- \_ DS-Klasse für den \_ \_ Cache \_**
</dt> <dd> <dl> <dt>

8402 (0x20d2)
</dt> <dt>



Die Klasse konnte nicht zwischengespeichert werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_REMOVE_ATT_CACHE"></span><span id="error_ds_cant_remove_att_cache"></span>**Fehler \_ DS Fehler beim \_ Entfernen des ATT- \_ \_ \_ Caches.**
</dt> <dd> <dl> <dt>

8403 (0x20d3)
</dt> <dt>



Das Attribut konnte nicht aus dem Cache entfernt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_REMOVE_CLASS_CACHE"></span><span id="error_ds_cant_remove_class_cache"></span>**Fehler \_ DS Fehler beim \_ Entfernen des \_ \_ Klassen \_ Caches.**
</dt> <dd> <dl> <dt>

8404 (0x20d4)
</dt> <dt>



Die Klasse konnte nicht aus dem Cache entfernt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_RETRIEVE_DN"></span><span id="error_ds_cant_retrieve_dn"></span>**Fehler " \_ DS-DN nicht \_ \_ abgerufen \_ "**
</dt> <dd> <dl> <dt>

8405 (0x20d5)
</dt> <dt>



Das Distinguished Name-Attribut konnte nicht gelesen werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MISSING_SUPREF"></span><span id="error_ds_missing_supref"></span>**Fehler \_ DS \_ fehlende \_ supref**
</dt> <dd> <dl> <dt>

8406 (0x20d6)
</dt> <dt>



Im Verzeichnisdienst wurde kein übergeordneter Verweis konfiguriert. Der Verzeichnisdienst kann daher keine Verweise auf Objekte außerhalb dieser Gesamtstruktur ausgeben.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_RETRIEVE_INSTANCE"></span><span id="error_ds_cant_retrieve_instance"></span>**Fehler \_ DS-Instanz konnte nicht \_ \_ abgerufen \_ werden**
</dt> <dd> <dl> <dt>

8407 (0x20d7)
</dt> <dt>



Das Instanztyp Attribut konnte nicht abgerufen werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CODE_INCONSISTENCY"></span><span id="error_ds_code_inconsistency"></span>**Fehler \_ \_ Code Inkonsistenzen \_**
</dt> <dd> <dl> <dt>

8408 (0x20d8)
</dt> <dt>



Ein interner Fehler ist aufgetreten.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DATABASE_ERROR"></span><span id="error_ds_database_error"></span>**Fehler- \_ DS- \_ Daten Bank \_ Fehler**
</dt> <dd> <dl> <dt>

8409 (0x20d9)
</dt> <dt>



Ein Datenbankfehler ist aufgetreten.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_GOVERNSID_MISSING"></span><span id="error_ds_governsid_missing"></span>**Fehler \_ DS \_ governdssid \_ fehlt.**
</dt> <dd> <dl> <dt>

8410 (0x20da)
</dt> <dt>



Das Attribut ' governsID ' fehlt.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MISSING_EXPECTED_ATT"></span><span id="error_ds_missing_expected_att"></span>**Fehler- \_ DS \_ fehlen \_ Erwartetes \_ ATT**
</dt> <dd> <dl> <dt>

8411 (0x20db)
</dt> <dt>



Ein erwartetes Attribut fehlt.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NCNAME_MISSING_CR_REF"></span><span id="error_ds_ncname_missing_cr_ref"></span>**Fehler \_ DS \_ NCName \_ fehlt \_ CR \_ Ref**
</dt> <dd> <dl> <dt>

8412 (0x20dc)
</dt> <dt>



Im angegebenen Namens Kontext fehlt ein Querverweis.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SECURITY_CHECKING_ERROR"></span><span id="error_ds_security_checking_error"></span>**Fehler bei \_ DS- \_ Sicherheits \_ Überprüfung \_**
</dt> <dd> <dl> <dt>

8413 (0x20dd)
</dt> <dt>



Ein Sicherheits Überprüfungs Fehler ist aufgetreten.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SCHEMA_NOT_LOADED"></span><span id="error_ds_schema_not_loaded"></span>**Fehler- \_ DS- \_ Schema \_ nicht \_ geladen**
</dt> <dd> <dl> <dt>

8414 (0x20de)
</dt> <dt>



Das Schema wurde nicht geladen.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SCHEMA_ALLOC_FAILED"></span><span id="error_ds_schema_alloc_failed"></span>**Fehler bei \_ DS- \_ Schema \_ Zuweisung \_ .**
</dt> <dd> <dl> <dt>

8415 (0x20df)
</dt> <dt>



Fehler bei der Schema Zuordnung. Überprüfen Sie, ob auf dem Computer wenig Arbeitsspeicher verfügbar ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ATT_SCHEMA_REQ_SYNTAX"></span><span id="error_ds_att_schema_req_syntax"></span>**Fehler-DS-Error- \_ \_ Schema- \_ \_ req- \_ Syntax**
</dt> <dd> <dl> <dt>

8416 (0x20e0)
</dt> <dt>



Fehler beim Abrufen der erforderlichen Syntax für das Attribut Schema.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_GCVERIFY_ERROR"></span><span id="error_ds_gcverify_error"></span>**Fehler \_ DS \_ gcverify- \_ Fehler**
</dt> <dd> <dl> <dt>

8417 (0x20e1)
</dt> <dt>



Fehler bei der Überprüfung des globalen Katalogs. Der globale Katalog ist nicht verfügbar, oder der Vorgang wird nicht unterstützt. Ein Teil des Verzeichnisses ist zurzeit nicht verfügbar.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_SCHEMA_MISMATCH"></span><span id="error_ds_dra_schema_mismatch"></span>**Fehler \_ DS- \_ DRA- \_ Schema \_ Konflikt**
</dt> <dd> <dl> <dt>

8418 (0x20e2)
</dt> <dt>



Fehler beim Replikations Vorgang aufgrund eines Schema Konflikts zwischen den beteiligten Servern.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_FIND_DSA_OBJ"></span><span id="error_ds_cant_find_dsa_obj"></span>**Fehler \_ DS \_ - \_ \_ DSA- \_ obj nicht gefunden**
</dt> <dd> <dl> <dt>

8419 (0x20E3)
</dt> <dt>



Das DSA-Objekt konnte nicht gefunden werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_FIND_EXPECTED_NC"></span><span id="error_ds_cant_find_expected_nc"></span>**Fehler " \_ DS nicht \_ gefunden" \_ \_ erwartet \_ .**
</dt> <dd> <dl> <dt>

8420 (0x20e4)
</dt> <dt>



Der namens Kontext konnte nicht gefunden werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_FIND_NC_IN_CACHE"></span><span id="error_ds_cant_find_nc_in_cache"></span>**Fehler \_ DS \_ - \_ \_ NC konnte \_ im \_ Cache nicht gefunden werden.**
</dt> <dd> <dl> <dt>

8421 (0x20e5)
</dt> <dt>



Der namens Kontext konnte im Cache nicht gefunden werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_RETRIEVE_CHILD"></span><span id="error_ds_cant_retrieve_child"></span>**Fehler DS nicht untergeordnetes Element \_ \_ \_ Abrufen \_**
</dt> <dd> <dl> <dt>

8422 (0x20e6)
</dt> <dt>



Das untergeordnete Objekt konnte nicht abgerufen werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SECURITY_ILLEGAL_MODIFY"></span><span id="error_ds_security_illegal_modify"></span>**Fehler-DS-Sicherheit unzulässige \_ \_ \_ \_ Änderung**
</dt> <dd> <dl> <dt>

8423 (0x20e7)
</dt> <dt>



Die Änderung ist aus Sicherheitsgründen nicht zulässig.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_REPLACE_HIDDEN_REC"></span><span id="error_ds_cant_replace_hidden_rec"></span>**Fehler DS-Fehler beim \_ \_ Ersetzen des \_ \_ verborgenen \_ rec**
</dt> <dd> <dl> <dt>

8424 (0x20e8)
</dt> <dt>



Der Vorgang kann den verborgenen Datensatz nicht ersetzen.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_BAD_HIERARCHY_FILE"></span><span id="error_ds_bad_hierarchy_file"></span>**Fehler \_ DS ungültige \_ \_ Hierarchie \_ Datei.**
</dt> <dd> <dl> <dt>

8425 (0x20e9)
</dt> <dt>



Die Hierarchie Datei ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_BUILD_HIERARCHY_TABLE_FAILED"></span><span id="error_ds_build_hierarchy_table_failed"></span>**Fehler bei \_ DS-buildhierarchie- \_ \_ \_ Tabelle \_**
</dt> <dd> <dl> <dt>

8426 (0x20ea)
</dt> <dt>



Fehler beim Erstellen der Hierarchie Tabelle.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CONFIG_PARAM_MISSING"></span><span id="error_ds_config_param_missing"></span>**Fehler \_ DS- \_ Konfigurationsparameter \_ \_ fehlt.**
</dt> <dd> <dl> <dt>

8427 (0x20eb)
</dt> <dt>



Der Verzeichnis Konfigurationsparameter fehlt in der Registrierung.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_COUNTING_AB_INDICES_FAILED"></span><span id="error_ds_counting_ab_indices_failed"></span>**Fehler \_ beim \_ zählen der ab- \_ \_ Indizes \_ .**
</dt> <dd> <dl> <dt>

8428 (0x20ec)
</dt> <dt>



Der Versuch, die Adressbuch Indizes zu zählen, ist fehlgeschlagen.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_HIERARCHY_TABLE_MALLOC_FAILED"></span><span id="error_ds_hierarchy_table_malloc_failed"></span>**Fehler bei \_ DS- \_ Hierarchie \_ Tabelle \_ malloc \_ .**
</dt> <dd> <dl> <dt>

8429 (0x20ed)
</dt> <dt>



Die Zuordnung der Hierarchie Tabelle ist fehlgeschlagen.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INTERNAL_FAILURE"></span><span id="error_ds_internal_failure"></span>**Interner Fehler bei \_ DS \_ \_**
</dt> <dd> <dl> <dt>

8430 (0x20ee)
</dt> <dt>



Der Verzeichnisdienst hat einen internen Fehler ermittelt.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_UNKNOWN_ERROR"></span><span id="error_ds_unknown_error"></span>**\_unbekannter Fehler DS. \_ \_**
</dt> <dd> <dl> <dt>

8431 (0x20ef)
</dt> <dt>



Unbekannter Fehler beim Verzeichnisdienst.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ROOT_REQUIRES_CLASS_TOP"></span><span id="error_ds_root_requires_class_top"></span>**Fehler-DS-Stamm \_ \_ \_ erfordert \_ Klasse \_ Top**
</dt> <dd> <dl> <dt>

8432 (0x20f 0)
</dt> <dt>



Ein Stamm Objekt erfordert die Klasse "Top".


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_REFUSING_FSMO_ROLES"></span><span id="error_ds_refusing_fsmo_roles"></span>**Fehler- \_ DS lehnt die Rollen für die \_ \_ \_ Rollen Schutz**
</dt> <dd> <dl> <dt>

8433 (0x20f 1)
</dt> <dt>



Dieser Verzeichnisserver wird heruntergefahren und kann nicht in den Besitz neuer Gleit Komma Rollen für den Einzel Master Besitz gelangen.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MISSING_FSMO_SETTINGS"></span><span id="error_ds_missing_fsmo_settings"></span>**Fehler- \_ DS \_ fehlende \_ \_ Einstellungen für den Anmelde Namen**
</dt> <dd> <dl> <dt>

8434 (0x20f 2)
</dt> <dt>



Der Verzeichnisdienst weist keine obligatorischen Konfigurationsinformationen auf und kann den Besitz von Rollen Rollen mit nur einem Master nicht ermitteln.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_UNABLE_TO_SURRENDER_ROLES"></span><span id="error_ds_unable_to_surrender_roles"></span>**Fehler \_ DS \_ beim \_ überlassen von \_ \_ Rollen nicht möglich**
</dt> <dd> <dl> <dt>

8435 (0x20f 3)
</dt> <dt>



Der Verzeichnisdienst konnte den Besitz von mindestens einer Gleit Komma Rolle für den Einzel Master nicht auf andere Server übertragen.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_GENERIC"></span><span id="error_ds_dra_generic"></span>**Fehler "DS", \_ \_ \_ generisch**
</dt> <dd> <dl> <dt>

8436 (0x20f 4)
</dt> <dt>



Fehler beim Replikations Vorgang.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_INVALID_PARAMETER"></span><span id="error_ds_dra_invalid_parameter"></span>**Fehler \_ DS- \_ DRA- \_ ungültiger \_ Parameter**
</dt> <dd> <dl> <dt>

8437 (0x20f 5)
</dt> <dt>



Für diesen Replikations Vorgang wurde ein ungültiger Parameter angegeben.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_BUSY"></span><span id="error_ds_dra_busy"></span>**Fehler- \_ DS- \_ DRA \_ ausgelastet**
</dt> <dd> <dl> <dt>

8438 (0x20f 6)
</dt> <dt>



Der Verzeichnisdienst ist zu stark ausgelastet, um den Replikations Vorgang zu diesem Zeitpunkt abzuschließen.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_BAD_DN"></span><span id="error_ds_dra_bad_dn"></span>**Fehler \_ DS DRA-fehlerhafter \_ \_ \_ DN**
</dt> <dd> <dl> <dt>

8439 (0x20f 7)
</dt> <dt>



Der für diesen Replikations Vorgang angegebene Distinguished Name ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_BAD_NC"></span><span id="error_ds_dra_bad_nc"></span>**Fehler DS-DRA-fehlerhafter \_ \_ \_ \_ NC**
</dt> <dd> <dl> <dt>

8440 (0x20f 8)
</dt> <dt>



Der für diesen Replikations Vorgang angegebene Benennungs Kontext ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_DN_EXISTS"></span><span id="error_ds_dra_dn_exists"></span>**Fehler \_ DS- \_ DRA- \_ DN \_ vorhanden**
</dt> <dd> <dl> <dt>

8441 (0x20f 9)
</dt> <dt>



Der für diesen Replikations Vorgang angegebene Distinguished Name ist bereits vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_INTERNAL_ERROR"></span><span id="error_ds_dra_internal_error"></span>**Fehler \_ DS \_ ( \_ interner DRA- \_ Fehler)**
</dt> <dd> <dl> <dt>

8442 (0x20fa)
</dt> <dt>



Im Replikationssystem ist ein interner Fehler aufgetreten.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_INCONSISTENT_DIT"></span><span id="error_ds_dra_inconsistent_dit"></span>**Fehler \_ DS- \_ DRA- \_ inkonsistente \_ dit**
</dt> <dd> <dl> <dt>

8443 (0x20fb)
</dt> <dt>



Beim Replikations Vorgang ist eine Daten Bank Inkonsistenz aufgetreten


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_CONNECTION_FAILED"></span><span id="error_ds_dra_connection_failed"></span>**Fehler \_ bei \_ dsdra- \_ Verbindungs \_ Fehler.**
</dt> <dd> <dl> <dt>

8444 (0x20fc)
</dt> <dt>



Der für diesen Replikations Vorgang angegebene Server konnte nicht kontaktiert werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_BAD_INSTANCE_TYPE"></span><span id="error_ds_dra_bad_instance_type"></span>**Fehler DS-DRA-fehlerhafter \_ \_ \_ \_ \_ Instanztyp**
</dt> <dd> <dl> <dt>

8445 (0x20fd)
</dt> <dt>



Beim Replikations Vorgang ist ein Objekt mit einem ungültigen Instanztyp aufgetreten.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_OUT_OF_MEM"></span><span id="error_ds_dra_out_of_mem"></span>**Fehler- \_ DS- \_ DRA \_ nicht \_ \_ genügend Arbeitsspeicher**
</dt> <dd> <dl> <dt>

8446 (0x20fe)
</dt> <dt>



Der Replikations Vorgang konnte keinen Arbeitsspeicher zuordnen.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_MAIL_PROBLEM"></span><span id="error_ds_dra_mail_problem"></span>**Fehler \_ DS- \_ DRA-Mail- \_ \_ Problem**
</dt> <dd> <dl> <dt>

8447 (0x20ff)
</dt> <dt>



Beim Replikations Vorgang ist ein Fehler im e-Mail-System aufgetreten.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_REF_ALREADY_EXISTS"></span><span id="error_ds_dra_ref_already_exists"></span>**Fehler \_ DS- \_ DRA-Ref ist \_ \_ bereits \_ vorhanden.**
</dt> <dd> <dl> <dt>

8448 (0x2100)
</dt> <dt>



Die Replikations Verweis Informationen für den Zielserver sind bereits vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_REF_NOT_FOUND"></span><span id="error_ds_dra_ref_not_found"></span>**Fehler \_ DS- \_ DRA- \_ ref \_ nicht \_ gefunden**
</dt> <dd> <dl> <dt>

8449 (0x2101)
</dt> <dt>



Die Replikations Verweis Informationen für den Zielserver sind nicht vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_OBJ_IS_REP_SOURCE"></span><span id="error_ds_dra_obj_is_rep_source"></span>**Fehler " \_ DS \_ DRA \_ obj" \_ ist \_ Rep \_ Source.**
</dt> <dd> <dl> <dt>

8450 (0x2102)
</dt> <dt>



Der Benennungs Kontext kann nicht entfernt werden, da er auf einen anderen Server repliziert wird.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_DB_ERROR"></span><span id="error_ds_dra_db_error"></span>**Fehler \_ DS- \_ DRA-DB- \_ \_ Fehler**
</dt> <dd> <dl> <dt>

8451 (0x2103)
</dt> <dt>



Beim Replikations Vorgang ist ein Datenbankfehler aufgetreten.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_NO_REPLICA"></span><span id="error_ds_dra_no_replica"></span>**Fehler- \_ DS \_ DRA \_ kein \_ Replikat**
</dt> <dd> <dl> <dt>

8452 (0x2104)
</dt> <dt>



Der namens Kontext wird gerade entfernt oder nicht vom angegebenen Server repliziert.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_ACCESS_DENIED"></span><span id="error_ds_dra_access_denied"></span>**Fehler \_ DS- \_ DRA- \_ Zugriff \_ verweigert**
</dt> <dd> <dl> <dt>

8453 (0x2105)
</dt> <dt>



Der Replikations Zugriff wurde verweigert.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_NOT_SUPPORTED"></span><span id="error_ds_dra_not_supported"></span>**Fehler- \_ DS- \_ DRA \_ nicht \_ unterstützt**
</dt> <dd> <dl> <dt>

8454 (0x2106)
</dt> <dt>



Der angeforderte Vorgang wird von dieser Version des Verzeichnis Dienstanbieter nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_RPC_CANCELLED"></span><span id="error_ds_dra_rpc_cancelled"></span>**Fehler \_ DS- \_ DRA- \_ RPC \_ abgebrochen**
</dt> <dd> <dl> <dt>

8455 (0x2107)
</dt> <dt>



Der Remote Prozedur Rückruf für die Replikation wurde abgebrochen.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_SOURCE_DISABLED"></span><span id="error_ds_dra_source_disabled"></span>**Fehler \_ DS- \_ DRA- \_ Quelle \_ deaktiviert**
</dt> <dd> <dl> <dt>

8456 (0x2108)
</dt> <dt>



Der Quell Server lehnt zurzeit Replikations Anforderungen ab.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_SINK_DISABLED"></span><span id="error_ds_dra_sink_disabled"></span>**Fehler \_ DS- \_ DRA- \_ Senke \_ deaktiviert**
</dt> <dd> <dl> <dt>

8457 (0x2109)
</dt> <dt>



Der Zielserver lehnt zurzeit Replikations Anforderungen ab.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_NAME_COLLISION"></span><span id="error_ds_dra_name_collision"></span>**Fehler \_ DS- \_ DRA- \_ namens \_ Konflikt**
</dt> <dd> <dl> <dt>

8458 (0x210a)
</dt> <dt>



Der Replikations Vorgang ist aufgrund eines Konflikts von Objektnamen fehlgeschlagen.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_SOURCE_REINSTALLED"></span><span id="error_ds_dra_source_reinstalled"></span>**Fehler \_ DS- \_ DRA- \_ Quelle \_ neu installiert**
</dt> <dd> <dl> <dt>

8459 (0x210b)
</dt> <dt>



Die Replikations Quelle wurde neu installiert.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_MISSING_PARENT"></span><span id="error_ds_dra_missing_parent"></span>**Fehler \_ DS- \_ DRA \_ fehlt über \_ geordnetes Element**
</dt> <dd> <dl> <dt>

8460 (0x210c)
</dt> <dt>



Der Replikations Vorgang ist fehlgeschlagen, da ein erforderliches übergeordnetes Objekt fehlt.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_PREEMPTED"></span><span id="error_ds_dra_preempted"></span>**Fehler \_ DS- \_ DRA \_ vorzeitig entfernt**
</dt> <dd> <dl> <dt>

8461 (0x210d)
</dt> <dt>



Der Replikations Vorgang wurde vorzeitig entfernt.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_ABANDON_SYNC"></span><span id="error_ds_dra_abandon_sync"></span>**Fehler \_ DS- \_ DRA- \_ \_ Synchronisierung abbrechen**
</dt> <dd> <dl> <dt>

8462 (0x210e)
</dt> <dt>



Der Versuch der Replikations Synchronisierung wurde aufgrund fehlender Updates abgebrochen.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_SHUTDOWN"></span><span id="error_ds_dra_shutdown"></span>**Fehler \_ DS- \_ DRA- \_ Herunterfahren**
</dt> <dd> <dl> <dt>

8463 (0x210f)
</dt> <dt>



Der Replikations Vorgang wurde beendet, da das System heruntergefahren wird.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_INCOMPATIBLE_PARTIAL_SET"></span><span id="error_ds_dra_incompatible_partial_set"></span>**Fehler- \_ DS- \_ \_ inkompatible \_ partielle \_ Teilmenge**
</dt> <dd> <dl> <dt>

8464 (0x2110)
</dt> <dt>



Fehler beim Synchronisierungs Versuch, weil der Ziel-DC derzeit darauf wartet, neue partielle Attribute aus der Quelle zu synchronisieren. Diese Bedingung ist normal, wenn eine aktuelle Schema Änderung den partiellen Attribut Satz geändert hat. Der partielle Ziel Attribut Satz ist keine Teilmenge des partiellen Quell partiellen Attributs.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_SOURCE_IS_PARTIAL_REPLICA"></span><span id="error_ds_dra_source_is_partial_replica"></span>**Fehler \_ DS- \_ DRA- \_ Quelle \_ ist \_ partielles \_ Replikat**
</dt> <dd> <dl> <dt>

8465 (0x2111)
</dt> <dt>



Fehler beim Replikations Synchronisierungs Versuch, weil ein Master Replikat versucht hat, eine Synchronisierung von einem Teil


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_EXTN_CONNECTION_FAILED"></span><span id="error_ds_dra_extn_connection_failed"></span>**Fehler bei der Verbindungsfehler- \_ \_ Verbindungs- \_ \_ Verbindungs \_ Fehler.**
</dt> <dd> <dl> <dt>

8466 (0x2112)
</dt> <dt>



Der für diesen Replikations Vorgang angegebene Server wurde kontaktiert, aber der Server konnte keinen zusätzlichen Server kontaktieren, um den Vorgang abzuschließen.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INSTALL_SCHEMA_MISMATCH"></span><span id="error_ds_install_schema_mismatch"></span>**Fehler " \_ DS- \_ Installations Schema nicht \_ \_ übereinstimmen"**
</dt> <dd> <dl> <dt>

8467 (0x2113)
</dt> <dt>



Die Version des Verzeichnisdienst Schemas der Quell Gesamtstruktur ist nicht mit der Version des Verzeichnis Dienstanbieter auf diesem Computer kompatibel.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DUP_LINK_ID"></span><span id="error_ds_dup_link_id"></span>**Fehler \_ DS \_ DUP- \_ Link- \_ ID**
</dt> <dd> <dl> <dt>

8468 (0x2114)
</dt> <dt>



Fehler beim Aktualisieren des Schemas: Es ist bereits ein Attribut mit demselben Link Bezeichner vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_ERROR_RESOLVING"></span><span id="error_ds_name_error_resolving"></span>**Fehler \_ beim \_ Auflösen des Namens "DS" \_ \_**
</dt> <dd> <dl> <dt>

8469 (0x2115)
</dt> <dt>



Namens Übersetzung: generischer Verarbeitungsfehler.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_ERROR_NOT_FOUND"></span><span id="error_ds_name_error_not_found"></span>**Fehler \_ DS- \_ namens \_ Fehler \_ nicht \_ gefunden.**
</dt> <dd> <dl> <dt>

8470 (0x2116)
</dt> <dt>



Namens Übersetzung: der Name oder unzureichende Rechte zum Anzeigen des Namens konnte nicht gefunden werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_ERROR_NOT_UNIQUE"></span><span id="error_ds_name_error_not_unique"></span>**Fehler \_ DS- \_ namens \_ Fehler ist \_ nicht \_ eindeutig.**
</dt> <dd> <dl> <dt>

8471 (0x2117)
</dt> <dt>



Namens Übersetzung: der Eingabe Name ist mehreren Ausgabe Namen zugeordnet.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_ERROR_NO_MAPPING"></span><span id="error_ds_name_error_no_mapping"></span>**Fehler \_ DS \_ - \_ Name \_ keine \_ Zuordnung**
</dt> <dd> <dl> <dt>

8472 (0x2118)
</dt> <dt>



Namens Übersetzung: der Eingabe Name wurde gefunden, aber nicht das zugehörige Ausgabeformat.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_ERROR_DOMAIN_ONLY"></span><span id="error_ds_name_error_domain_only"></span>**Fehler \_ DS- \_ Name \_ Fehler \_ Domäne \_**
</dt> <dd> <dl> <dt>

8473 (0x2119)
</dt> <dt>



Namens Übersetzung: Es konnte nicht vollständig aufgelöst werden. es wurde nur die Domäne gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_ERROR_NO_SYNTACTICAL_MAPPING"></span><span id="error_ds_name_error_no_syntactical_mapping"></span>**Fehler \_ DS- \_ namens \_ Fehler \_ keine \_ syntaktische \_ Zuordnung**
</dt> <dd> <dl> <dt>

8474 (0x211a)
</dt> <dt>



Namens Übersetzung: Es kann keine rein syntaktische Zuordnung auf dem Client ausgeführt werden, ohne dass die Verbindung übertragen wird.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CONSTRUCTED_ATT_MOD"></span><span id="error_ds_constructed_att_mod"></span>**Fehler- \_ DS, \_ erstellt, \_ ATT \_ mod**
</dt> <dd> <dl> <dt>

8475 (0x211b)
</dt> <dt>



Die Änderung eines konstruierten Attributs ist nicht zulässig.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_WRONG_OM_OBJ_CLASS"></span><span id="error_ds_wrong_om_obj_class"></span>**Fehler \_ DS \_ falsche \_ OM \_ obj- \_ Klasse**
</dt> <dd> <dl> <dt>

8476 (0x211c)
</dt> <dt>



Die angegebene OM-Object-Klasse ist für ein Attribut mit der angegebenen Syntax falsch.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_REPL_PENDING"></span><span id="error_ds_dra_repl_pending"></span>**Fehler \_ DS- \_ DRA- \_ repl steht \_ aus.**
</dt> <dd> <dl> <dt>

8477 (0x211d)
</dt> <dt>



Die Replikations Anforderung wurde gepostet. warten auf Antwort.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DS_REQUIRED"></span><span id="error_ds_ds_required"></span>**Fehler- \_ DS- \_ DS \_ erforderlich**
</dt> <dd> <dl> <dt>

8478 (0x211e)
</dt> <dt>



Der angeforderte Vorgang erfordert einen Verzeichnisdienst, und keiner war verfügbar.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INVALID_LDAP_DISPLAY_NAME"></span><span id="error_ds_invalid_ldap_display_name"></span>**Fehler- \_ DS \_ ungültiger \_ LDAP- \_ Anzeige \_ Name.**
</dt> <dd> <dl> <dt>

8479 (0x211f)
</dt> <dt>



Der LDAP-Anzeige Name der Klasse oder des Attributs enthält nicht-ASCII-Zeichen.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NON_BASE_SEARCH"></span><span id="error_ds_non_base_search"></span>**Fehler- \_ DS, \_ nicht \_ Basis \_ Suche**
</dt> <dd> <dl> <dt>

8480 (0x2120)
</dt> <dt>



Der angeforderte Suchvorgang wird nur für Basis suchen unterstützt.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_RETRIEVE_ATTS"></span><span id="error_ds_cant_retrieve_atts"></span>**Fehler \_ beim \_ \_ Abrufen von \_ ATTS.**
</dt> <dd> <dl> <dt>

8481 (0x2121)
</dt> <dt>



Bei der Suche konnten keine Attribute aus der Datenbank abgerufen werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_BACKLINK_WITHOUT_LINK"></span><span id="error_ds_backlink_without_link"></span>**Fehler- \_ DS- \_ Backlink \_ ohne \_ Verknüpfung**
</dt> <dd> <dl> <dt>

8482 (0x2122)
</dt> <dt>



Beim Schema Aktualisierungs Vorgang wurde versucht, ein abwärts Verknüpfungs Attribut hinzuzufügen, das über keinen entsprechenden Forward-Link verfügt.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_EPOCH_MISMATCH"></span><span id="error_ds_epoch_mismatch"></span>**Fehler \_ DS- \_ Epochen Konflikt \_**
</dt> <dd> <dl> <dt>

8483 (0x2123)
</dt> <dt>



Quelle und Ziel einer Domänen übergreifenden Verschiebung stimmen nicht mit der Epochen Nummer des Objekts überein. Entweder die Quelle oder das Ziel hat nicht die neueste Version des Objekts.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SRC_NAME_MISMATCH"></span><span id="error_ds_src_name_mismatch"></span>**Fehler \_ DS- \_ src- \_ namens \_ Konflikt**
</dt> <dd> <dl> <dt>

8484 (0x2124)
</dt> <dt>



Quelle und Ziel einer Domänen übergreifenden Verschiebung stimmen nicht mit dem aktuellen Namen des Objekts überein. Entweder die Quelle oder das Ziel hat nicht die neueste Version des Objekts.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SRC_AND_DST_NC_IDENTICAL"></span><span id="error_ds_src_and_dst_nc_identical"></span>**Fehler \_ DS \_ src \_ und \_ DST \_ NC \_ identisch**
</dt> <dd> <dl> <dt>

8485 (0x2125)
</dt> <dt>



Quelle und Ziel für den Domänen übergreifenden Verschiebungs Vorgang sind identisch. Der Aufrufer sollte anstelle eines Domänen übergreifenden Verschiebungs Vorgangs einen lokalen Verschiebungs Vorgang verwenden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DST_NC_MISMATCH"></span><span id="error_ds_dst_nc_mismatch"></span>**Fehler \_ DS \_ DST- \_ NC \_ -Konflikt**
</dt> <dd> <dl> <dt>

8486 (0x2126)
</dt> <dt>



Quelle und Ziel für eine Domänen übergreifende Verschiebung sind nicht in den Benennungs Kontexten in der Gesamtstruktur zu finden. Entweder die Quelle oder das Ziel hat nicht die neueste Version des Partitions Containers.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NOT_AUTHORITIVE_FOR_DST_NC"></span><span id="error_ds_not_authoritive_for_dst_nc"></span>**Fehler- \_ DS \_ nicht \_ autoritative \_ für \_ DST \_ NC**
</dt> <dd> <dl> <dt>

8487 (0x2127)
</dt> <dt>



Das Ziel einer Domänen übergreifenden Verschiebung ist für den Ziel namens Kontext nicht autoritativ.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SRC_GUID_MISMATCH"></span><span id="error_ds_src_guid_mismatch"></span>**Fehler- \_ DS- \_ src- \_ GUID-Konflikt \_**
</dt> <dd> <dl> <dt>

8488 (0x2128)
</dt> <dt>



Quelle und Ziel einer Domänen übergreifenden Verschiebung stimmen nicht mit der Identität des Quell Objekts überein. Entweder die Quelle oder das Ziel hat nicht die neueste Version des Quell Objekts.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_MOVE_DELETED_OBJECT"></span><span id="error_ds_cant_move_deleted_object"></span>**Fehler \_ DS Fehler beim \_ Verschieben des \_ \_ gelöschten \_ Objekts.**
</dt> <dd> <dl> <dt>

8489 (0x2129)
</dt> <dt>



Ein Objekt, das über Domänen übergreifend verschoben wird, ist bereits bekannt, dass es vom Zielserver gelöscht wird. Der Quell Server verfügt nicht über die aktuelle Version des Quell Objekts.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_PDC_OPERATION_IN_PROGRESS"></span><span id="error_ds_pdc_operation_in_progress"></span>**Fehler \_ DS \_ PDC \_ - \_ Vorgang \_ wird ausgeführt.**
</dt> <dd> <dl> <dt>

8490 (0x212a)
</dt> <dt>



Es wird bereits ein anderer Vorgang ausgeführt, der exklusiven Zugriff auf den PDC-FSMO erfordert.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CROSS_DOMAIN_CLEANUP_REQD"></span><span id="error_ds_cross_domain_cleanup_reqd"></span>**Fehler \_ - \_ DS \_ -Domänen übergreifende \_ Bereinigungs \_ -reqd**
</dt> <dd> <dl> <dt>

8491 (0x212b)
</dt> <dt>



Ein Domänen übergreifender Verschiebungs Vorgang ist fehlgeschlagen, sodass zwei Versionen des verschogenen Objekts vorhanden sind, jeweils eine in den Quell-und Zieldomänen. Das Zielobjekt muss entfernt werden, um das System in einen konsistenten Zustand zu versetzen.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ILLEGAL_XDOM_MOVE_OPERATION"></span><span id="error_ds_illegal_xdom_move_operation"></span>**Fehler DS unzulässiger xdom-Verschiebungs \_ \_ \_ \_ \_ Vorgang**
</dt> <dd> <dl> <dt>

8492 (0x212c)
</dt> <dt>



Dieses Objekt kann nicht über Domänen Grenzen hinweg verschoben werden, da Domänen übergreifende Verschiebungen für diese Klasse nicht zulässig sind oder das Objekt einige besondere Merkmale hat, z. b.: Vertrauensstellungs Konto oder eingeschränkte RID, wodurch die Verschiebung verhindert wird.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_WITH_ACCT_GROUP_MEMBERSHPS"></span><span id="error_ds_cant_with_acct_group_membershps"></span>**Fehler-DS-Fehler \_ \_ \_ mit \_ Acct- \_ Gruppen \_ mitgliedungen**
</dt> <dd> <dl> <dt>

8493 (0x212d)
</dt> <dt>



Objekte können nicht mithilfe von Mitgliedschaften über Domänen Grenzen hinweg verschoben werden, wenn Sie verschoben wurden. Dies würde die Mitgliedschaftsbedingungen der Konto Gruppe verletzen. Entfernen Sie das Objekt aus allen Konto Gruppenmitgliedschaften, und wiederholen Sie den Vorgang.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NC_MUST_HAVE_NC_PARENT"></span><span id="error_ds_nc_must_have_nc_parent"></span>**Fehler- \_ DS- \_ NC \_ muss \_ über \_ \_ geordnetes NC-Element verfügen**
</dt> <dd> <dl> <dt>

8494 (0x212e)
</dt> <dt>



Ein namens Kontext Kopf muss das unmittelbare untergeordnete Element eines anderen namens Kontext Kopfes und nicht eines inneren Knotens sein.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CR_IMPOSSIBLE_TO_VALIDATE"></span><span id="error_ds_cr_impossible_to_validate"></span>**Fehler \_ DS \_ CR \_ kann nicht überprüft \_ \_ werden.**
</dt> <dd> <dl> <dt>

8495 (0x212f)
</dt> <dt>



Das Verzeichnis kann den vorgeschlagenen namens Kontext Namen nicht validieren, weil er kein Replikat des Namens Kontexts oberhalb des vorgeschlagenen namens Kontexts enthält. Stellen Sie sicher, dass die Domänen Namen-Master Rolle von einem Server gespeichert wird, der als globaler Katalogserver konfiguriert ist, und dass der Server mit seinen Replikations Partnern auf dem neuesten Stand ist. (Gilt nur für Windows 2000 Domain Naming Masters.)


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DST_DOMAIN_NOT_NATIVE"></span><span id="error_ds_dst_domain_not_native"></span>**Fehler \_ DS \_ DST- \_ Domäne \_ nicht \_ nativ**
</dt> <dd> <dl> <dt>

8496 (0x2130)
</dt> <dt>



Die Zieldomäne muss sich im einheitlichen Modus befinden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MISSING_INFRASTRUCTURE_CONTAINER"></span><span id="error_ds_missing_infrastructure_container"></span>**Fehler \_ DS \_ fehlender \_ Infrastruktur \_ Container**
</dt> <dd> <dl> <dt>

8497 (0x2131)
</dt> <dt>



Der Vorgang kann nicht ausgeführt werden, da der Server über keinen Infrastruktur Container in der relevanten Domäne verfügt.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_MOVE_ACCOUNT_GROUP"></span><span id="error_ds_cant_move_account_group"></span>**Fehler-DS-Fehler beim \_ \_ Verschieben der \_ \_ Konto \_ Gruppe**
</dt> <dd> <dl> <dt>

8498 (0x2132)
</dt> <dt>



Domänen übergreifende Verschiebung von nicht leeren Konto Gruppen ist nicht zulässig.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_MOVE_RESOURCE_GROUP"></span><span id="error_ds_cant_move_resource_group"></span>**Fehler DS-Fehler beim \_ \_ Verschieben der \_ \_ Ressourcen \_ Gruppe.**
</dt> <dd> <dl> <dt>

8499 (0x2133)
</dt> <dt>



Die Domänen übergreifende Verschiebung von nicht leeren Ressourcengruppen ist nicht zulässig.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INVALID_SEARCH_FLAG"></span><span id="error_ds_invalid_search_flag"></span>**Fehler- \_ DS \_ ungültiges \_ \_ suchflag**
</dt> <dd> <dl> <dt>

8500 (0x2134)
</dt> <dt>



Die Suchflags für das Attribut sind ungültig. Das ANR-Bit ist nur für Attribute von Unicode-oder Teletex-Zeichen folgen gültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_TREE_DELETE_ABOVE_NC"></span><span id="error_ds_no_tree_delete_above_nc"></span>**Fehler \_ DS \_ keine \_ Struktur \_ \_ über " \_ NC" Löschen**
</dt> <dd> <dl> <dt>

8501 (0x2135)
</dt> <dt>



Struktur Löschungen, die bei einem Objekt beginnen, das einen NC-Head als Nachfolger hat, sind nicht zulässig.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_COULDNT_LOCK_TREE_FOR_DELETE"></span><span id="error_ds_couldnt_lock_tree_for_delete"></span>**Fehler " \_ DS" \_ konnte \_ für \_ den \_ \_ Löschvorgang nicht gesperrt werden.**
</dt> <dd> <dl> <dt>

8502 (0x2136)
</dt> <dt>



Der Verzeichnisdienst konnte eine Struktur in Vorbereitung auf das Löschen einer Struktur nicht sperren, weil die Struktur verwendet wurde.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_COULDNT_IDENTIFY_OBJECTS_FOR_TREE_DELETE"></span><span id="error_ds_couldnt_identify_objects_for_tree_delete"></span>**Fehler- \_ DS \_ konnte \_ \_ Objekte für Struktur \_ \_ \_ Löschung nicht identifizieren**
</dt> <dd> <dl> <dt>

8503 (0x2137)
</dt> <dt>



Der Verzeichnisdienst konnte die Liste der Objekte, die gelöscht werden sollen, nicht identifizieren, während ein Baum gelöscht wird.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SAM_INIT_FAILURE"></span><span id="error_ds_sam_init_failure"></span>**Fehler \_ DS \_ Sam \_ Init \_ -Fehler**
</dt> <dd> <dl> <dt>

8504 (0x2138)
</dt> <dt>



Fehler bei der Initialisierung des Sicherheits Konten-Managers aufgrund des folgenden Fehlers: %1. Fehler Status: 0x %2. Fahren Sie dieses System herunter, und starten Sie den Verzeichnisdienst-Wiederherstellungs Modus neu. Ausführliche Informationen finden Sie im Ereignisprotokoll.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SENSITIVE_GROUP_VIOLATION"></span><span id="error_ds_sensitive_group_violation"></span>**\_Verletzung der \_ Verletzung der sensiblen \_ Gruppe \_ für Fehler**
</dt> <dd> <dl> <dt>

8505 (0x2139)
</dt> <dt>



Nur ein Administrator kann die Mitgliedschafts Liste einer administrativen Gruppe ändern.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_MOD_PRIMARYGROUPID"></span><span id="error_ds_cant_mod_primarygroupid"></span>**Fehler \_ DS \_ cant \_ mod \_ primaryGroupId**
</dt> <dd> <dl> <dt>

8506 (0x213a)
</dt> <dt>



Die primäre Gruppen-ID eines Domänen Controller Kontos kann nicht geändert werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ILLEGAL_BASE_SCHEMA_MOD"></span><span id="error_ds_illegal_base_schema_mod"></span>**Fehler-DS ungültiges \_ \_ \_ Basis \_ Schema \_ mod.**
</dt> <dd> <dl> <dt>

8507 (0x213b)
</dt> <dt>



Es wurde versucht, das Basis Schema zu ändern.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NONSAFE_SCHEMA_CHANGE"></span><span id="error_ds_nonsafe_schema_change"></span>**Fehler- \_ DS \_ nicht sichere \_ Schema \_ Änderung**
</dt> <dd> <dl> <dt>

8508 (0x213c)
</dt> <dt>



Das Hinzufügen eines neuen obligatorischen Attributs zu einer vorhandenen Klasse, das Löschen eines obligatorischen Attributs aus einer vorhandenen Klasse oder das Hinzufügen eines optionalen Attributs zur besonderen Klasse Top, das kein Backwardlink-Attribut ist (direkt oder durch Vererbung, z. b. durch das Hinzufügen oder Löschen einer Hilfsklasse), ist nicht zulässig.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SCHEMA_UPDATE_DISALLOWED"></span><span id="error_ds_schema_update_disallowed"></span>**Fehler \_ DS \_ Schema \_ Update nicht \_ zulässig**
</dt> <dd> <dl> <dt>

8509 (0x213d)
</dt> <dt>



Die Schema Aktualisierung ist auf diesem Domänen Controller nicht zulässig, da der Domänen Controller nicht der Schema-Rollen Besitzer ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_CREATE_UNDER_SCHEMA"></span><span id="error_ds_cant_create_under_schema"></span>**Fehler " \_ DS nicht \_ \_ \_ unter \_ Schema erstellen"**
</dt> <dd> <dl> <dt>

8510 (0x213e)
</dt> <dt>



Ein Objekt dieser Klasse kann nicht unter dem Schema Container erstellt werden. Sie können nur Attribut Schema-und Klassen Schema Objekte unter dem Schema Container erstellen.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INSTALL_NO_SRC_SCH_VERSION"></span><span id="error_ds_install_no_src_sch_version"></span>**Fehler \_ DS \_ install \_ No \_ src \_ Sch \_ Version**
</dt> <dd> <dl> <dt>

8511 (0x213f)
</dt> <dt>



Die Replikat-/unterordnungsinstallation konnte das objectVersion-Attribut für den Schema Container auf dem Quell Domänen Controller nicht abrufen. Entweder fehlt das-Attribut im Schema Container, oder die angegebenen Anmelde Informationen verfügen nicht über die Berechtigung zum Lesen.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INSTALL_NO_SCH_VERSION_IN_INIFILE"></span><span id="error_ds_install_no_sch_version_in_inifile"></span>**Fehler \_ DS \_ install \_ No \_ Sch \_ Version \_ in \_ IniFile**
</dt> <dd> <dl> <dt>

8512 (0x2140)
</dt> <dt>



Die Replikat-/unterordnungsinstallation konnte das objectVersion-Attribut im Schema Abschnitt der Datei schema.ini im Verzeichnis "System32" nicht lesen.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INVALID_GROUP_TYPE"></span><span id="error_ds_invalid_group_type"></span>**\_ \_ ungültiger \_ \_ Gruppentyp für Fehler-DS**
</dt> <dd> <dl> <dt>

8513 (0x2141)
</dt> <dt>



Der angegebene Gruppentyp ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_NEST_GLOBALGROUP_IN_MIXEDDOMAIN"></span><span id="error_ds_no_nest_globalgroup_in_mixeddomain"></span>**Fehler \_ DS \_ No \_ Nest \_ Global Group \_ in \_ mixeddomain**
</dt> <dd> <dl> <dt>

8514 (0x2142)
</dt> <dt>



Globale Gruppen in einer gemischten Domäne können nicht geschachtelt werden, wenn die Gruppe für die Sicherheit aktiviert ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_NEST_LOCALGROUP_IN_MIXEDDOMAIN"></span><span id="error_ds_no_nest_localgroup_in_mixeddomain"></span>**Fehler \_ DS \_ No \_ Nest \_ localgroup \_ in \_ mixeddomain**
</dt> <dd> <dl> <dt>

8515 (0x2143)
</dt> <dt>



Lokale Gruppen in einer gemischten Domäne können nicht geschachtelt werden, wenn die Gruppe für die Sicherheit aktiviert ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_GLOBAL_CANT_HAVE_LOCAL_MEMBER"></span><span id="error_ds_global_cant_have_local_member"></span>**Fehler \_ DS \_ Global \_ nicht \_ über \_ lokale \_ Member verfügen**
</dt> <dd> <dl> <dt>

8516 (0x2144)
</dt> <dt>



Eine globale Gruppe kann keine lokale Gruppe als Mitglied haben.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_GLOBAL_CANT_HAVE_UNIVERSAL_MEMBER"></span><span id="error_ds_global_cant_have_universal_member"></span>**Fehler- \_ DS \_ Global \_ cant \_ haben \_ universellen \_ Member**
</dt> <dd> <dl> <dt>

8517 (0x2145)
</dt> <dt>



Eine globale Gruppe kann keine universelle Gruppe als Mitglied haben.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_UNIVERSAL_CANT_HAVE_LOCAL_MEMBER"></span><span id="error_ds_universal_cant_have_local_member"></span>**Fehler "DS Universal" darf kein \_ \_ \_ \_ \_ Lokales \_ Mitglied sein.**
</dt> <dd> <dl> <dt>

8518 (0x2146)
</dt> <dt>



Eine universelle Gruppe kann keine lokale Gruppe als Mitglied haben.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_GLOBAL_CANT_HAVE_CROSSDOMAIN_MEMBER"></span><span id="error_ds_global_cant_have_crossdomain_member"></span>**Fehler- \_ DS \_ Global \_ cant \_ hat \_ crossdomain- \_ Member**
</dt> <dd> <dl> <dt>

8519 (0x2147)
</dt> <dt>



Eine globale Gruppe darf kein Domänen übergreifendes Element aufweisen.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_LOCAL_CANT_HAVE_CROSSDOMAIN_LOCAL_MEMBER"></span><span id="error_ds_local_cant_have_crossdomain_local_member"></span>**Fehler \_ DS \_ local darf nicht \_ \_ über \_ crossdomain \_ local \_ Member verfügen**
</dt> <dd> <dl> <dt>

8520 (0x2148)
</dt> <dt>



Eine lokale Gruppe kann keine andere Domänen übergreifende lokale Gruppe als Mitglied haben.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_HAVE_PRIMARY_MEMBERS"></span><span id="error_ds_have_primary_members"></span>**Fehler- \_ DS \_ haben \_ primäre \_ Member**
</dt> <dd> <dl> <dt>

8521 (0x2149)
</dt> <dt>



Eine Gruppe mit primären Mitgliedern kann nicht in eine Gruppe mit aktivierter Sicherheit geändert werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_STRING_SD_CONVERSION_FAILED"></span><span id="error_ds_string_sd_conversion_failed"></span>**Fehler bei DS-Zeichen folgen- \_ \_ SD- \_ \_ Konvertierung \_**
</dt> <dd> <dl> <dt>

8522 (0x214a)
</dt> <dt>



Die Schema Cache Auslastung konnte die Standard-SD-Zeichenfolge für ein Klassen Schema Objekt nicht konvertieren.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAMING_MASTER_GC"></span><span id="error_ds_naming_master_gc"></span>**Fehler \_ DS- \_ Benennungs \_ Master- \_ GC**
</dt> <dd> <dl> <dt>

8523 (0x214b)
</dt> <dt>



Nur DSAs, die als globale Katalogserver konfiguriert sind, sollten die Domänen Namen-Master-FSMO-Rolle enthalten dürfen. (Gilt nur für Windows 2000-Server.)


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DNS_LOOKUP_FAILURE"></span><span id="error_ds_dns_lookup_failure"></span>**Fehler \_ DS \_ DNS- \_ Lookup \_ -Fehler**
</dt> <dd> <dl> <dt>

8524 (0x214c)
</dt> <dt>



Der DSA-Vorgang kann aufgrund eines Fehlers bei der DNS-Suche nicht fortgesetzt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_COULDNT_UPDATE_SPNS"></span><span id="error_ds_couldnt_update_spns"></span>**Fehler- \_ DS \_ konnte \_ \_ SPNs nicht aktualisieren.**
</dt> <dd> <dl> <dt>

8525 (0x214d)
</dt> <dt>



Beim Verarbeiten einer Änderung des DNS-Host Namens für ein Objekt konnten die Werte des Dienst Prinzipal namens nicht synchron aufbewahrt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_RETRIEVE_SD"></span><span id="error_ds_cant_retrieve_sd"></span>**Fehler "DS" konnte \_ \_ \_ SD nicht abrufen \_**
</dt> <dd> <dl> <dt>

8526 (0x214e)
</dt> <dt>



Das sicherheitsbeschreibungerattribut konnte nicht gelesen werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_KEY_NOT_UNIQUE"></span><span id="error_ds_key_not_unique"></span>**Fehler- \_ DS- \_ Schlüssel \_ nicht \_ eindeutig**
</dt> <dd> <dl> <dt>

8527 (0x214f)
</dt> <dt>



Das angeforderte Objekt wurde nicht gefunden, aber es wurde ein Objekt mit diesem Schlüssel gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_WRONG_LINKED_ATT_SYNTAX"></span><span id="error_ds_wrong_linked_att_syntax"></span>**Fehler \_ DS \_ falsche \_ verknüpfte \_ ATT- \_ Syntax**
</dt> <dd> <dl> <dt>

8528 (0x2150)
</dt> <dt>



Die Syntax des hinzugefügten verknüpften Attributs ist falsch. Forward-Links können nur Syntax 2.5.5.1, 2.5.5.7 und 2.5.5.14 aufweisen, und Backlinks können nur Syntax 2.5.5.1 aufweisen.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SAM_NEED_BOOTKEY_PASSWORD"></span><span id="error_ds_sam_need_bootkey_password"></span>**Fehler- \_ DS \_ Sam \_ benötigt \_ bootkey- \_ Kennwort**
</dt> <dd> <dl> <dt>

8529 (0x2151)
</dt> <dt>



Der Sicherheits Konto-Manager muss das Start Kennwort erhalten.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SAM_NEED_BOOTKEY_FLOPPY"></span><span id="error_ds_sam_need_bootkey_floppy"></span>**Fehler- \_ DS \_ Sam \_ benötigt \_ bootkey- \_ Diskette**
</dt> <dd> <dl> <dt>

8530 (0x2152)
</dt> <dt>



Der Sicherheits Konto-Manager muss den Start Schlüssel von der Diskette erhalten.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_START"></span><span id="error_ds_cant_start"></span>**Fehler \_ DS \_ nicht \_ starten**
</dt> <dd> <dl> <dt>

8531 (0x2153)
</dt> <dt>



Der Verzeichnisdienst kann nicht gestartet werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INIT_FAILURE"></span><span id="error_ds_init_failure"></span>**Fehler \_ DS- \_ Init \_ -Fehler**
</dt> <dd> <dl> <dt>

8532 (0x2154)
</dt> <dt>



Verzeichnisdienste konnten nicht gestartet werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_PKT_PRIVACY_ON_CONNECTION"></span><span id="error_ds_no_pkt_privacy_on_connection"></span>**Fehler- \_ DS \_ keine \_ Pkt- \_ Datenschutz \_ bei \_ Verbindung**
</dt> <dd> <dl> <dt>

8533 (0x2155)
</dt> <dt>



Die Verbindung zwischen Client und Server erfordert den Datenschutz des Pakets oder besser.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SOURCE_DOMAIN_IN_FOREST"></span><span id="error_ds_source_domain_in_forest"></span>**Fehler- \_ DS- \_ Quell \_ Domäne \_ in der \_ Gesamtstruktur**
</dt> <dd> <dl> <dt>

8534 (0x2156)
</dt> <dt>



Die Quell Domäne befindet sich möglicherweise nicht in derselben Gesamtstruktur wie das Ziel.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DESTINATION_DOMAIN_NOT_IN_FOREST"></span><span id="error_ds_destination_domain_not_in_forest"></span>**Fehler- \_ DS- \_ Ziel \_ Domäne \_ nicht \_ in \_ Gesamtstruktur**
</dt> <dd> <dl> <dt>

8535 (0x2157)
</dt> <dt>



Die Zieldomäne muss sich in der Gesamtstruktur befinden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DESTINATION_AUDITING_NOT_ENABLED"></span><span id="error_ds_destination_auditing_not_enabled"></span>**Fehler- \_ DS- \_ Ziel Überwachung \_ \_ nicht \_ aktiviert**
</dt> <dd> <dl> <dt>

8536 (0x2158)
</dt> <dt>



Der Vorgang erfordert, dass die Überwachung der Zieldomäne aktiviert ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_FIND_DC_FOR_SRC_DOMAIN"></span><span id="error_ds_cant_find_dc_for_src_domain"></span>**Fehler \_ DS \_ - \_ \_ DC \_ für src \_ - \_ Domäne nicht gefunden.**
</dt> <dd> <dl> <dt>

8537 (0x2159)
</dt> <dt>



Der Vorgang konnte einen DC für die Quell Domäne nicht finden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SRC_OBJ_NOT_GROUP_OR_USER"></span><span id="error_ds_src_obj_not_group_or_user"></span>**Fehler \_ DS \_ src \_ obj \_ nicht \_ Gruppe \_ oder \_ Benutzer**
</dt> <dd> <dl> <dt>

8538 (0x215 a)
</dt> <dt>



Das Quell Objekt muss eine Gruppe oder ein Benutzer sein.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SRC_SID_EXISTS_IN_FOREST"></span><span id="error_ds_src_sid_exists_in_forest"></span>**Fehler \_ DS- \_ src-sid ist \_ \_ \_ in der \_ Gesamtstruktur vorhanden**
</dt> <dd> <dl> <dt>

8539 (0x215 b)
</dt> <dt>



Die SID des Quell Objekts ist bereits in der Ziel Gesamtstruktur vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SRC_AND_DST_OBJECT_CLASS_MISMATCH"></span><span id="error_ds_src_and_dst_object_class_mismatch"></span>**Fehler \_ DS \_ src \_ und \_ DST- \_ Objekt \_ Klasse stimmen nicht \_ überein.**
</dt> <dd> <dl> <dt>

8540 (0x215 c)
</dt> <dt>



Das Quell-und das Zielobjekt müssen denselben Typ aufweisen.


</dt> </dl> </dd> <dt>

<span id="ERROR_SAM_INIT_FAILURE"></span><span id="error_sam_init_failure"></span>**Fehler \_ Sam \_ Init \_ -Fehler**
</dt> <dd> <dl> <dt>

8541 (0x215 d)
</dt> <dt>



Fehler bei der Initialisierung des Sicherheits Konten-Managers aufgrund des folgenden Fehlers: %1. Fehler Status: 0x %2. Klicken Sie auf OK, um das System herunterzufahren und in den abgesicherten Modus zu starten. Ausführliche Informationen finden Sie im Ereignisprotokoll.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_SCHEMA_INFO_SHIP"></span><span id="error_ds_dra_schema_info_ship"></span>**Fehler \_ DS- \_ DRA- \_ Schema \_ Info \_ Versand**
</dt> <dd> <dl> <dt>

8542 (0x215 e)
</dt> <dt>



Die Schema Informationen konnten nicht in die Replikations Anforderung eingeschlossen werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_SCHEMA_CONFLICT"></span><span id="error_ds_dra_schema_conflict"></span>**Fehler \_ DS- \_ DRA- \_ Schema \_ Konflikt**
</dt> <dd> <dl> <dt>

8543 (0x215 f)
</dt> <dt>



Der Replikations Vorgang konnte aufgrund einer Schema Inkompatibilität nicht abgeschlossen werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_EARLIER_SCHEMA_CONFLICT"></span><span id="error_ds_dra_earlier_schema_conflict"></span>**Fehler \_ DS- \_ DRA- \_ \_ Schema \_ Konflikt**
</dt> <dd> <dl> <dt>

8544 (0x2160)
</dt> <dt>



Der Replikations Vorgang konnte aufgrund einer vorherigen Schema Inkompatibilität nicht abgeschlossen werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_OBJ_NC_MISMATCH"></span><span id="error_ds_dra_obj_nc_mismatch"></span>**Fehler \_ DS \_ DRA \_ obj \_ NC \_ -Konflikt**
</dt> <dd> <dl> <dt>

8545 (0x2161)
</dt> <dt>



Das Replikations Update konnte nicht angewendet werden, da entweder die Quelle oder das Ziel noch keine Informationen zu einem letzten Domänen übergreifenden Verschiebungs Vorgang erhalten hat.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NC_STILL_HAS_DSAS"></span><span id="error_ds_nc_still_has_dsas"></span>**Fehler \_ DS \_ NC \_ \_ weist weiterhin \_ DSAs auf.**
</dt> <dd> <dl> <dt>

8546 (0x2162)
</dt> <dt>



Die angeforderte Domäne konnte nicht gelöscht werden, da Domänen Controller vorhanden sind, die noch diese Domäne hosten.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_GC_REQUIRED"></span><span id="error_ds_gc_required"></span>**Fehler- \_ DS- \_ GC \_ erforderlich**
</dt> <dd> <dl> <dt>

8547 (0x2163)
</dt> <dt>



Der angeforderte Vorgang kann nur auf einem globalen Katalogserver ausgeführt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_LOCAL_MEMBER_OF_LOCAL_ONLY"></span><span id="error_ds_local_member_of_local_only"></span>**Fehler \_ DS \_ lokaler \_ Member \_ von \_ \_ nur lokal**
</dt> <dd> <dl> <dt>

8548 (0x2164)
</dt> <dt>



Eine lokale Gruppe kann nur Mitglied anderer lokaler Gruppen in der gleichen Domäne sein.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_FPO_IN_UNIVERSAL_GROUPS"></span><span id="error_ds_no_fpo_in_universal_groups"></span>**Fehler " \_ DS \_ Nein" \_ \_ in \_ universellen \_ Gruppen**
</dt> <dd> <dl> <dt>

8549 (0x2165)
</dt> <dt>



Fremde Sicherheits Prinzipale können nicht zu universellen Gruppen gehören.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_ADD_TO_GC"></span><span id="error_ds_cant_add_to_gc"></span>**Fehler \_ DS \_ nicht \_ \_ zum \_ GC hinzufügen**
</dt> <dd> <dl> <dt>

8550 (0x2166)
</dt> <dt>



Das Attribut darf aufgrund von Sicherheitsgründen nicht in den GC repliziert werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_CHECKPOINT_WITH_PDC"></span><span id="error_ds_no_checkpoint_with_pdc"></span>**Fehler- \_ DS kein Prüfpunkt \_ \_ \_ mit \_ PDC**
</dt> <dd> <dl> <dt>

8551 (0x2167)
</dt> <dt>



Der Prüfpunkt mit dem PDC konnte nicht übernommen werden, weil derzeit zu viele Änderungen verarbeitet werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SOURCE_AUDITING_NOT_ENABLED"></span><span id="error_ds_source_auditing_not_enabled"></span>**Fehler der DS-Quell Überwachung ist \_ \_ \_ \_ nicht \_ aktiviert.**
</dt> <dd> <dl> <dt>

8552 (0x2168)
</dt> <dt>



Der Vorgang erfordert, dass die Überwachung der Quell Domäne aktiviert ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_CREATE_IN_NONDOMAIN_NC"></span><span id="error_ds_cant_create_in_nondomain_nc"></span>**Fehler "DS-Fehler \_ \_ \_ \_ beim Erstellen in \_ nicht-Domäne \_ "**
</dt> <dd> <dl> <dt>

8553 (0x2169)
</dt> <dt>



Sicherheits Prinzipal Objekte können nur innerhalb von Domänen namens Kontexten erstellt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INVALID_NAME_FOR_SPN"></span><span id="error_ds_invalid_name_for_spn"></span>**Fehler \_ DS \_ ungültiger \_ Name \_ für \_ SPN**
</dt> <dd> <dl> <dt>

8554 (0x216a)
</dt> <dt>



Ein Dienst Prinzipal Name (Service Principal Name, SPN) konnte nicht erstellt werden, da der angegebene Hostname nicht das erforderliche Format hat.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_FILTER_USES_CONTRUCTED_ATTRS"></span><span id="error_ds_filter_uses_contructed_attrs"></span>**Fehler- \_ DS- \_ Filter verwendet die \_ \_ Konstanten \_ .**
</dt> <dd> <dl> <dt>

8555 (0x216b)
</dt> <dt>



Es wurde ein Filter mit konstruierten Attributen übermittelt.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_UNICODEPWD_NOT_IN_QUOTES"></span><span id="error_ds_unicodepwd_not_in_quotes"></span>**Fehler \_ DS \_ unicodePwd \_ nicht \_ in \_ Anführungszeichen**
</dt> <dd> <dl> <dt>

8556 (0x216c)
</dt> <dt>



Der unicodePwd-Attribut Wert muss in doppelte Anführungszeichen eingeschlossen werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MACHINE_ACCOUNT_QUOTA_EXCEEDED"></span><span id="error_ds_machine_account_quota_exceeded"></span>**Fehler \_ DS- \_ Computer \_ Konto \_ Kontingent \_ überschritten**
</dt> <dd> <dl> <dt>

8557 (0x216d)
</dt> <dt>



Der Computer konnte nicht der Domäne hinzugefügt werden. Sie haben die maximale Anzahl von Computer Konten überschritten, die Sie in dieser Domäne erstellen dürfen. Wenden Sie sich an Ihren Systemadministrator, um dieses Limit zurückzusetzen oder zu erhöhen.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MUST_BE_RUN_ON_DST_DC"></span><span id="error_ds_must_be_run_on_dst_dc"></span>**Fehler- \_ DS \_ muss auf dem \_ \_ \_ \_ DST \_ -Domänen Controller ausgeführt werden**
</dt> <dd> <dl> <dt>

8558 (0x216e)
</dt> <dt>



Aus Sicherheitsgründen muss der Vorgang auf dem Ziel-DC ausgeführt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SRC_DC_MUST_BE_SP4_OR_GREATER"></span><span id="error_ds_src_dc_must_be_sp4_or_greater"></span>**Fehler \_ DS \_ src \_ DC \_ muss \_ \_ SP4 \_ oder \_ höher sein.**
</dt> <dd> <dl> <dt>

8559 (0x216f)
</dt> <dt>



Aus Sicherheitsgründen muss der Quell Domänen Controller NT4SP4 oder höher sein.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_TREE_DELETE_CRITICAL_OBJ"></span><span id="error_ds_cant_tree_delete_critical_obj"></span>**Fehler \_ DS-Struktur \_ \_ \_ Löschen \_ kritisch \_ obj**
</dt> <dd> <dl> <dt>

8560 (0x2170)
</dt> <dt>



Wichtige Verzeichnisdienst-System Objekte können während Struktur Lösch Vorgängen nicht gelöscht werden. Das Löschen der Struktur wurde möglicherweise teilweise durchgeführt.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INIT_FAILURE_CONSOLE"></span><span id="error_ds_init_failure_console"></span>**Fehler- \_ DS init-Fehler \_ \_ \_ Konsole**
</dt> <dd> <dl> <dt>

8561 (0x2171)
</dt> <dt>



Verzeichnisdienste konnten aufgrund des folgenden Fehlers nicht gestartet werden: %1. Fehler Status: 0x %2. Klicken Sie auf OK, um das System herunterzufahren. Zur weiteren Systemdiagnose können Sie die Wiederherstellungskonsole verwenden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SAM_INIT_FAILURE_CONSOLE"></span><span id="error_ds_sam_init_failure_console"></span>**Fehler \_ DS \_ Sam \_ Init-Fehler \_ \_ Konsole**
</dt> <dd> <dl> <dt>

8562 (0x2172)
</dt> <dt>



Fehler bei der Initialisierung des Sicherheits Konten-Managers aufgrund des folgenden Fehlers: %1. Fehler Status: 0x %2. Klicken Sie auf OK, um das System herunterzufahren. Zur weiteren Systemdiagnose können Sie die Wiederherstellungskonsole verwenden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_FOREST_VERSION_TOO_HIGH"></span><span id="error_ds_forest_version_too_high"></span>**Fehler-DS-Gesamtstruktur \_ \_ \_ Version \_ zu \_ hoch**
</dt> <dd> <dl> <dt>

8563 (0x2173)
</dt> <dt>



Die Version des Betriebssystems ist nicht kompatibel mit der aktuellen AD DS Gesamtstruktur Funktionsebene oder AD LDS Konfigurationssatz-Funktionsebene. Sie müssen ein Upgrade auf eine neue Version des Betriebssystems durchführen, bevor dieser Server zu einem AD DS Domänen Controller werden kann, oder Sie können eine AD LDS Instanz in dieser AD DS Gesamtstruktur oder AD LDS Konfigurationssatz hinzufügen.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DOMAIN_VERSION_TOO_HIGH"></span><span id="error_ds_domain_version_too_high"></span>**Fehler- \_ DS- \_ Domänen \_ Version \_ zu \_ hoch**
</dt> <dd> <dl> <dt>

8564 (0x2174)
</dt> <dt>



Die installierte Version des Betriebssystems ist mit der aktuellen Domänen Funktionsebene nicht kompatibel. Sie müssen ein Upgrade auf eine neue Version des Betriebssystems ausführen, bevor dieser Server als Domänen Controller in dieser Domäne verwendet werden kann.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_FOREST_VERSION_TOO_LOW"></span><span id="error_ds_forest_version_too_low"></span>**Fehler-DS-Gesamtstruktur \_ \_ \_ Version \_ zu \_ niedrig**
</dt> <dd> <dl> <dt>

8565 (0x2175)
</dt> <dt>



Die auf diesem Server installierte Version des Betriebssystems unterstützt nicht mehr die aktuelle AD DS-Gesamtstruktur Funktionsebene oder AD LDS Konfigurationssatz-Funktionsebene. Sie müssen die Funktionsebene der AD DS-Gesamtstruktur oder die AD LDS Konfigurationssatz-Funktionsebene erhöhen, bevor dieser Server ein AD DS Domänen Controller oder eine AD LDS Instanz in dieser Gesamtstruktur oder diesem Konfigurationssatz werden kann.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DOMAIN_VERSION_TOO_LOW"></span><span id="error_ds_domain_version_too_low"></span>**Fehler- \_ DS- \_ Domänen \_ Version \_ zu \_ niedrig**
</dt> <dd> <dl> <dt>

8566 (0x2176)
</dt> <dt>



Die auf diesem Server installierte Version des Betriebssystems unterstützt die aktuelle Domänen Funktionsebene nicht mehr. Sie müssen die Domänen Funktionsebene erhöhen, bevor dieser Server als Domänen Controller in dieser Domäne verwendet werden kann.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INCOMPATIBLE_VERSION"></span><span id="error_ds_incompatible_version"></span>**Fehler- \_ DS \_ inkompatible \_ Version**
</dt> <dd> <dl> <dt>

8567 (0x2177)
</dt> <dt>



Die auf diesem Server installierte Version des Betriebssystems ist nicht mit der Funktionsebene der Domäne oder der Gesamtstruktur kompatibel.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_LOW_DSA_VERSION"></span><span id="error_ds_low_dsa_version"></span>**Fehler \_ DS \_ niedrige \_ DSA- \_ Version**
</dt> <dd> <dl> <dt>

8568 (0x2178)
</dt> <dt>



Die Funktionsebene der Domäne (oder Gesamtstruktur) kann nicht auf den angeforderten Wert fest gegeben werden, weil mindestens ein Domänen Controller in der Domäne (oder Gesamtstruktur) vorhanden ist, die sich auf einer niedrigeren inkompatiblen Funktionsebene befinden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_BEHAVIOR_VERSION_IN_MIXEDDOMAIN"></span><span id="error_ds_no_behavior_version_in_mixeddomain"></span>**Fehler \_ DS \_ keine \_ Verhaltens \_ Version \_ in \_ mixeddomain**
</dt> <dd> <dl> <dt>

8569 (0x2179)
</dt> <dt>



Die Gesamtstruktur Funktionsebene kann nicht auf den angeforderten Wert fest liegen, da sich eine oder mehrere Domänen noch im gemischten Domänen Modus befinden. Alle Domänen in der Gesamtstruktur müssen sich im einheitlichen Modus befinden, damit Sie die Gesamtstruktur Funktionsebene erhöhen können.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NOT_SUPPORTED_SORT_ORDER"></span><span id="error_ds_not_supported_sort_order"></span>**Fehler- \_ DS \_ nicht \_ unterstützte \_ Sortier \_ Reihenfolge**
</dt> <dd> <dl> <dt>

8570 (0x217a)
</dt> <dt>



Die angeforderte Sortierreihenfolge wird nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_NOT_UNIQUE"></span><span id="error_ds_name_not_unique"></span>**Fehler \_ DS- \_ Name \_ nicht \_ eindeutig**
</dt> <dd> <dl> <dt>

8571 (0x217b)
</dt> <dt>



Der angeforderte Name ist bereits als eindeutiger Bezeichner vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MACHINE_ACCOUNT_CREATED_PRENT4"></span><span id="error_ds_machine_account_created_prent4"></span>**Fehler \_ DS- \_ Computer \_ Konto \_ erstellt \_ PRENT4**
</dt> <dd> <dl> <dt>

8572 (0x217c)
</dt> <dt>



Das Computer Konto wurde vor dem Computer Konto erstellt. Das Konto muss neu erstellt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OUT_OF_VERSION_STORE"></span><span id="error_ds_out_of_version_store"></span>**Fehler- \_ DS \_ aus dem \_ \_ Versions \_ Speicher**
</dt> <dd> <dl> <dt>

8573 (0x217d)
</dt> <dt>



Die Datenbank befindet sich außerhalb des Versionsspeicher.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INCOMPATIBLE_CONTROLS_USED"></span><span id="error_ds_incompatible_controls_used"></span>**Fehler- \_ DS- \_ kompatible Steuer \_ Elemente \_ verwendet**
</dt> <dd> <dl> <dt>

8574 (0x217e)
</dt> <dt>



Der Vorgang kann nicht fortgesetzt werden, da mehrere widersprüchliche Steuerelemente verwendet wurden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_REF_DOMAIN"></span><span id="error_ds_no_ref_domain"></span>**Fehler \_ DS \_ keine \_ Verweis \_ Domäne**
</dt> <dd> <dl> <dt>

8575 (0x217f)
</dt> <dt>



Es wurde keine gültige Sicherheits beschreibungerverweisdomäne für diese Partition gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_RESERVED_LINK_ID"></span><span id="error_ds_reserved_link_id"></span>**Fehler \_ DS \_ reservierte \_ Link- \_ ID**
</dt> <dd> <dl> <dt>

8576 (0x2180)
</dt> <dt>



Fehler beim Aktualisieren des Schemas: der Link Bezeichner ist reserviert.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_LINK_ID_NOT_AVAILABLE"></span><span id="error_ds_link_id_not_available"></span>**Fehler \_ DS- \_ Link- \_ ID \_ nicht \_ verfügbar**
</dt> <dd> <dl> <dt>

8577 (0x2181)
</dt> <dt>



Fehler beim Aktualisieren des Schemas: Es sind keine Link Bezeichner verfügbar.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_AG_CANT_HAVE_UNIVERSAL_MEMBER"></span><span id="error_ds_ag_cant_have_universal_member"></span>**Fehler der DS-Verfügbarkeits Gruppe ( \_ \_ \_ \_ \_ Universal \_ Member).**
</dt> <dd> <dl> <dt>

8578 (0x2182)
</dt> <dt>



Eine Konto Gruppe kann keine universelle Gruppe als Mitglied haben.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MODIFYDN_DISALLOWED_BY_INSTANCE_TYPE"></span><span id="error_ds_modifydn_disallowed_by_instance_type"></span>**Fehler \_ DS- \_ modififydn \_ \_ durch \_ \_ Instanztyp unzulässig**
</dt> <dd> <dl> <dt>

8579 (0x2183)
</dt> <dt>



Umbenennen oder Verschieben von Vorgängen für namens Kontext Köpfe oder schreibgeschützte Objekte sind nicht zulässig.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_OBJECT_MOVE_IN_SCHEMA_NC"></span><span id="error_ds_no_object_move_in_schema_nc"></span>**Fehler \_ ' \_ keine \_ Objekt \_ Verschiebung ' \_ in \_ Schema \_ NC**
</dt> <dd> <dl> <dt>

8580 (0x2184)
</dt> <dt>



Verschiebe Vorgänge für Objekte im Schema namens Kontext sind nicht zulässig.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MODIFYDN_DISALLOWED_BY_FLAG"></span><span id="error_ds_modifydn_disallowed_by_flag"></span>**Fehler \_ DS- \_ modififydn ist \_ \_ durch \_ Flag unzulässig.**
</dt> <dd> <dl> <dt>

8581 (0x2185)
</dt> <dt>



Für das Objekt wurde ein Systemflag festgelegt, und das Objekt kann nicht verschoben oder umbenannt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MODIFYDN_WRONG_GRANDPARENT"></span><span id="error_ds_modifydn_wrong_grandparent"></span>**Fehler \_ DS \_ MODIFYDN \_ falsches über \_ geordnetes Element**
</dt> <dd> <dl> <dt>

8582 (0x2186)
</dt> <dt>



Dieses Objekt ist nicht berechtigt, seinen übergeordneten übergeordneten Container zu ändern. Die Verschiebung ist für dieses Objekt nicht zulässig, aber auf gleich geordnete Container beschränkt.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_ERROR_TRUST_REFERRAL"></span><span id="error_ds_name_error_trust_referral"></span>**Fehler- \_ DS- \_ namens \_ Fehler \_ Vertrauensstellungs \_ Referenz**
</dt> <dd> <dl> <dt>

8583 (0x2187)
</dt> <dt>



Das vollständige auflösen ist nicht möglich, es wird ein Verweis auf eine andere Gesamtstruktur generiert.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_SUPPORTED_ON_STANDARD_SERVER"></span><span id="error_not_supported_on_standard_server"></span>**Fehler \_ \_ wird \_ auf \_ Standard \_ Server nicht unterstützt.**
</dt> <dd> <dl> <dt>

8584 (0x2188)
</dt> <dt>



Die angeforderte Aktion wird auf dem Standard Server nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_ACCESS_REMOTE_PART_OF_AD"></span><span id="error_ds_cant_access_remote_part_of_ad"></span>**Fehler \_ DS \_ - \_ Zugriff \_ \_ auf Remote Teil \_ von \_ AD**
</dt> <dd> <dl> <dt>

8585 (0x2189)
</dt> <dt>



Auf eine Partition des Verzeichnis Dienstanbieter, die sich auf einem Remote Server befindet, konnte nicht zugegriffen werden. Stellen Sie sicher, dass mindestens ein Server für die betreffende Partition ausgeführt wird.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CR_IMPOSSIBLE_TO_VALIDATE_V2"></span><span id="error_ds_cr_impossible_to_validate_v2"></span>**Fehler \_ DS \_ CR \_ kann nicht überprüft werden \_ \_ \_ v2**
</dt> <dd> <dl> <dt>

8586 (0x218 a)
</dt> <dt>



Das Verzeichnis kann den vorgeschlagenen namens Kontext (oder Partitionsnamen) nicht validieren, weil er kein Replikat enthält und keine Verbindung mit einem Replikat des Namens Kontexts oberhalb des vorgeschlagenen namens Kontexts aufnehmen kann. Stellen Sie sicher, dass der übergeordnete Benennungs Kontext ordnungsgemäß in DNS registriert ist, und dass mindestens ein Replikat dieses Namens Kontexts durch den Domänen Namen Master erreichbar ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_THREAD_LIMIT_EXCEEDED"></span><span id="error_ds_thread_limit_exceeded"></span>**Fehler- \_ DS- \_ Thread \_ Limit \_ überschritten**
</dt> <dd> <dl> <dt>

8587 (0x218 b)
</dt> <dt>



Der Thread Grenzwert für diese Anforderung wurde überschritten.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NOT_CLOSEST"></span><span id="error_ds_not_closest"></span>**Fehler- \_ DS ist \_ nicht \_ am nächsten**
</dt> <dd> <dl> <dt>

8588 (0x218 c)
</dt> <dt>



Der globale Katalogserver befindet sich nicht am nächstgelegenen Standort.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_DERIVE_SPN_WITHOUT_SERVER_REF"></span><span id="error_ds_cant_derive_spn_without_server_ref"></span>**Fehler- \_ DS konnte \_ \_ \_ keinen SPN \_ ohne \_ Server \_ Verweis ableiten.**
</dt> <dd> <dl> <dt>

8589 (0x218 d)
</dt> <dt>



Die DS kann keinen Dienst Prinzipal Namen (SPN) ableiten, mit dem der Zielserver gegenseitig authentifiziert werden kann, da das zugehörige Server Objekt in der lokalen DS-Datenbank kein serverReference-Attribut aufweist.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SINGLE_USER_MODE_FAILED"></span><span id="error_ds_single_user_mode_failed"></span>**Fehler \_ beim \_ Einzel \_ Benutzermodus im Einzelbenutzer \_ Modus \_ .**
</dt> <dd> <dl> <dt>

8590 (0x218 e)
</dt> <dt>



Der Verzeichnisdienst konnte nicht in den Einzelbenutzermodus wechseln.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NTDSCRIPT_SYNTAX_ERROR"></span><span id="error_ds_ntdscript_syntax_error"></span>**Fehler \_ DS \_ ntdscript- \_ Syntax \_ Fehler**
</dt> <dd> <dl> <dt>

8591 (0x218 f)
</dt> <dt>



Der Verzeichnisdienst kann das Skript aufgrund eines Syntax Fehlers nicht analysieren.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NTDSCRIPT_PROCESS_ERROR"></span><span id="error_ds_ntdscript_process_error"></span>**Fehler \_ DS \_ ntdscript- \_ Prozess \_ Fehler**
</dt> <dd> <dl> <dt>

8592 (0x2190)
</dt> <dt>



Der Verzeichnisdienst kann das Skript aufgrund eines Fehlers nicht verarbeiten.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DIFFERENT_REPL_EPOCHS"></span><span id="error_ds_different_repl_epochs"></span>**Fehler- \_ DS \_ unterschiedlicher \_ repl- \_ Epochen**
</dt> <dd> <dl> <dt>

8593 (0x2191)
</dt> <dt>



Der Verzeichnisdienst kann den angeforderten Vorgang nicht ausführen, da sich die beteiligten Server unterschiedlichen Replikations Epochen befinden (in der Regel im Zusammenhang mit einem Domänen umbenennen, der gerade ausgeführt wird).


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRS_EXTENSIONS_CHANGED"></span><span id="error_ds_drs_extensions_changed"></span>**Fehler- \_ DS \_ DRS- \_ Erweiterungen \_ geändert**
</dt> <dd> <dl> <dt>

8594 (0x2192)
</dt> <dt>



Die Verzeichnisdienst Bindung muss aufgrund einer Änderung der Server Erweiterungs Informationen erneut ausgehandelt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_REPLICA_SET_CHANGE_NOT_ALLOWED_ON_DISABLED_CR"></span><span id="error_ds_replica_set_change_not_allowed_on_disabled_cr"></span>**Fehler \_ \_ \_ \_ bei der Änderung der Replikat Gruppe \_ \_ für den \_ \_ deaktivierten \_ CR**
</dt> <dd> <dl> <dt>

8595 (0x2193)
</dt> <dt>



Der Vorgang ist für einen deaktivierten Kreuz Verweis nicht zulässig.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_MSDS_INTID"></span><span id="error_ds_no_msds_intid"></span>**Fehler- \_ DS \_ keine \_ msDS \_ -initid**
</dt> <dd> <dl> <dt>

8596 (0x2194)
</dt> <dt>



Fehler beim Aktualisieren des Schemas: Es sind keine Werte für MSDS-IntID verfügbar.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DUP_MSDS_INTID"></span><span id="error_ds_dup_msds_intid"></span>**Fehler \_ DS \_ DUP \_ msDS \_ -initid**
</dt> <dd> <dl> <dt>

8597 (0x2195)
</dt> <dt>



Fehler beim Aktualisieren des Schemas: doppelte MSDS-initid. Wiederholen Sie den Vorgang.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_EXISTS_IN_RDNATTID"></span><span id="error_ds_exists_in_rdnattid"></span>**Fehler \_ - \_ DS \_ in \_ rDNAttID**
</dt> <dd> <dl> <dt>

8598 (0x2196)
</dt> <dt>



Fehler beim Löschen des Schemas: das Attribut wird in rDNAttID verwendet.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_AUTHORIZATION_FAILED"></span><span id="error_ds_authorization_failed"></span>**Fehler bei \_ DS- \_ Autorisierung. \_**
</dt> <dd> <dl> <dt>

8599 (0x2197)
</dt> <dt>



Der Verzeichnisdienst konnte die Anforderung nicht autorisieren.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INVALID_SCRIPT"></span><span id="error_ds_invalid_script"></span>**Fehler- \_ DS \_ ungültiges \_ Skript**
</dt> <dd> <dl> <dt>

8600 (0x2198)
</dt> <dt>



Der Verzeichnisdienst kann das Skript nicht verarbeiten, da er ungültig ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_REMOTE_CROSSREF_OP_FAILED"></span><span id="error_ds_remote_crossref_op_failed"></span>**Fehler \_ bei \_ Remote- \_ CrossRef- \_ op \_ -Fehler.**
</dt> <dd> <dl> <dt>

8601 (0x2199)
</dt> <dt>



Fehler beim Remote Vorgang zum Erstellen eines quer Verweises auf dem Domänen Namen-Master-Hauptschlüssel. Der Fehler des Vorgangs liegt in den erweiterten Daten.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CROSS_REF_BUSY"></span><span id="error_ds_cross_ref_busy"></span>**Fehler- \_ DS- \_ Querverweis \_ \_ ausgelastet**
</dt> <dd> <dl> <dt>

8602 (0x219a)
</dt> <dt>



Ein Querverweis wird lokal mit dem gleichen Namen verwendet.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_DERIVE_SPN_FOR_DELETED_DOMAIN"></span><span id="error_ds_cant_derive_spn_for_deleted_domain"></span>**Fehler-DS konnte keinen \_ \_ \_ \_ SPN \_ für \_ Gelöschte \_ Domäne ableiten.**
</dt> <dd> <dl> <dt>

8603 (0x219b)
</dt> <dt>



Die DS kann keinen Dienst Prinzipal Namen (Service Principal Name, SPN) ableiten, mit dem der Zielserver gegenseitig authentifiziert werden kann, da die Domäne des Servers aus der Gesamtstruktur gelöscht wurde.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_DEMOTE_WITH_WRITEABLE_NC"></span><span id="error_ds_cant_demote_with_writeable_nc"></span>**Fehler \_ DS \_ \_ \_ kann nicht mit \_ Beschreib barem \_ NC herabgestuft werden.**
</dt> <dd> <dl> <dt>

8604 (0x219c)
</dt> <dt>



Beschreibbare NCS verhindern, dass dieser Domänen Controller herabgestuft wird.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DUPLICATE_ID_FOUND"></span><span id="error_ds_duplicate_id_found"></span>**Fehler \_ DS \_ doppelte \_ ID \_ gefunden.**
</dt> <dd> <dl> <dt>

8605 (0x219d)
</dt> <dt>



Das angeforderte Objekt hat einen nicht eindeutigen Bezeichner und kann nicht abgerufen werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INSUFFICIENT_ATTR_TO_CREATE_OBJECT"></span><span id="error_ds_insufficient_attr_to_create_object"></span>**Fehler- \_ DS \_ unzureichende \_ attr \_ zum Erstellen des \_ \_ Objekts**
</dt> <dd> <dl> <dt>

8606 (0x219e)
</dt> <dt>



Zum Erstellen eines Objekts wurden unzureichende Attribute angegeben. Dieses Objekt ist möglicherweise nicht vorhanden, weil es möglicherweise gelöscht wurde und bereits eine Garbage Collection durchgeführt wurde.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_GROUP_CONVERSION_ERROR"></span><span id="error_ds_group_conversion_error"></span>**Fehler- \_ DS- \_ Gruppen \_ Konvertierungs \_ Fehler**
</dt> <dd> <dl> <dt>

8607 (0x219f)
</dt> <dt>



Die Gruppe kann aufgrund von Attribut Einschränkungen für den angeforderten Gruppentyp nicht konvertiert werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_MOVE_APP_BASIC_GROUP"></span><span id="error_ds_cant_move_app_basic_group"></span>**Fehler-DS-Fehler beim \_ \_ Verschieben der APP- \_ \_ \_ Basis \_ Gruppe**
</dt> <dd> <dl> <dt>

8608 (0x21a0)
</dt> <dt>



Die Domänen übergreifende Verschiebung von nicht leeren grundlegenden Anwendungs Gruppen ist nicht zulässig.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_MOVE_APP_QUERY_GROUP"></span><span id="error_ds_cant_move_app_query_group"></span>**Fehler-DS-Fehler beim \_ \_ Verschieben der APP- \_ \_ \_ Abfrage \_ Gruppe**
</dt> <dd> <dl> <dt>

8609 (0x21a1)
</dt> <dt>



Domänen übergreifende Verschiebung von nicht leeren Abfrage basierten Anwendungs Gruppen ist nicht zulässig.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ROLE_NOT_VERIFIED"></span><span id="error_ds_role_not_verified"></span>**Fehler- \_ DS- \_ Rolle \_ nicht \_ überprüft**
</dt> <dd> <dl> <dt>

8610 (0x21a2)
</dt> <dt>



Der Besitz der Rolle der Rolle konnte nicht überprüft werden, da die zugehörige Verzeichnis Partition mit mindestens einem Replikations Partner nicht erfolgreich repliziert wurde.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_WKO_CONTAINER_CANNOT_BE_SPECIAL"></span><span id="error_ds_wko_container_cannot_be_special"></span>**Fehler der \_ DS- \_ WKO- \_ Container \_ darf nicht \_ \_ speziell sein**
</dt> <dd> <dl> <dt>

8611 (0x21a3)
</dt> <dt>



Der Zielcontainer für eine Umleitung eines bekannten Objekt Containers darf nicht bereits ein spezieller Container sein.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DOMAIN_RENAME_IN_PROGRESS"></span><span id="error_ds_domain_rename_in_progress"></span>**Fehler \_ \_ \_ beim Umbenennen \_ der Domäne in \_ Bearbeitung**
</dt> <dd> <dl> <dt>

8612 (0x21a4)
</dt> <dt>



Der Verzeichnisdienst kann den angeforderten Vorgang nicht ausführen, weil ein Domänen Umbenennungs Vorgang durchgeführt wird.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_EXISTING_AD_CHILD_NC"></span><span id="error_ds_existing_ad_child_nc"></span>**Fehler \_ DS \_ vorhandenes untergeordnetes \_ AD- \_ \_ NC**
</dt> <dd> <dl> <dt>

8613 (0x21a5)
</dt> <dt>



Der Verzeichnisdienst hat eine untergeordnete Partition unter dem angeforderten Partitionsnamen erkannt. Die Partitions Hierarchie muss in einer Top-Down-Methode erstellt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_REPL_LIFETIME_EXCEEDED"></span><span id="error_ds_repl_lifetime_exceeded"></span>**Fehler \_ der \_ repl- \_ Lebensdauer \_ überschritten.**
</dt> <dd> <dl> <dt>

8614 (0x21a6)
</dt> <dt>



Der Verzeichnisdienst kann nicht mit diesem Server repliziert werden, weil die Zeit seit der letzten Replikation mit diesem Server die Tombstone-Lebensdauer überschritten hat.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DISALLOWED_IN_SYSTEM_CONTAINER"></span><span id="error_ds_disallowed_in_system_container"></span>**Fehler- \_ DS \_ \_ in \_ System \_ Container nicht zulässig**
</dt> <dd> <dl> <dt>

8615 (0x21a7)
</dt> <dt>



Der angeforderte Vorgang ist für ein Objekt im System Container nicht zulässig.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_LDAP_SEND_QUEUE_FULL"></span><span id="error_ds_ldap_send_queue_full"></span>**Fehler- \_ DS \_ LDAP- \_ Sende Warteschlange \_ \_ voll**
</dt> <dd> <dl> <dt>

8616 (0x21a8)
</dt> <dt>



Die LDAP-Server-netzwerksendewarteschlange wurde aufgefüllt, da der Client die Ergebnisse seiner Anforderungen nicht schnell genug verarbeitet. Es werden keine weiteren Anforderungen verarbeitet, bis der Client abfängt. Wenn der Client nicht abfängt, wird er getrennt.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_OUT_SCHEDULE_WINDOW"></span><span id="error_ds_dra_out_schedule_window"></span>**Fehler DS-DRA-Timeout- \_ \_ \_ \_ \_ Zeit Plan Fenster**
</dt> <dd> <dl> <dt>

8617 (0x21a9)
</dt> <dt>



Die geplante Replikation wurde nicht durchgeführt, da das System ausgelastet war, um die Anforderung innerhalb des Zeit Plan Fensters auszuführen. Die Replikations Warteschlange ist überlastet Reduzieren Sie die Anzahl der Partner, oder verringern Sie die geplante Replikations Häufigkeit.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_POLICY_NOT_KNOWN"></span><span id="error_ds_policy_not_known"></span>**Fehler- \_ DS- \_ Richtlinie \_ nicht \_ bekannt**
</dt> <dd> <dl> <dt>

8618 (0x21aa)
</dt> <dt>



Zu diesem Zeitpunkt kann nicht ermittelt werden, ob die branchreplikations Richtlinie auf dem Hub-Domänen Controller verfügbar ist. Wiederholen Sie den Vorgang zu einem späteren Zeitpunkt, um Replikations Latenzen zu berücksichtigen.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SITE_SETTINGS_OBJECT"></span><span id="error_no_site_settings_object"></span>**Fehler " \_ kein \_ Standort \_ Einstellungs \_ Objekt"**
</dt> <dd> <dl> <dt>

8619 (0x21ab)
</dt> <dt>



Das Standort Einstellungs Objekt für den angegebenen Standort ist nicht vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SECRETS"></span><span id="error_no_secrets"></span>**Fehler \_ keine \_ geheimen Schlüssel**
</dt> <dd> <dl> <dt>

8620 (0x21ac)
</dt> <dt>



Der lokale Konto Speicher enthält kein geheimes Material für das angegebene Konto.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_WRITABLE_DC_FOUND"></span><span id="error_no_writable_dc_found"></span>**Fehler " \_ kein \_ Beschreib barer \_ DC \_ gefunden".**
</dt> <dd> <dl> <dt>

8621 (0x21ad)
</dt> <dt>



Es konnte kein Beschreib barer Domänen Controller in der Domäne gefunden werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_SERVER_OBJECT"></span><span id="error_ds_no_server_object"></span>**Fehler " \_ DS \_ kein \_ Server \_ Objekt"**
</dt> <dd> <dl> <dt>

8622 (0x21ae)
</dt> <dt>



Das Server Objekt für den Domänen Controller ist nicht vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_NTDSA_OBJECT"></span><span id="error_ds_no_ntdsa_object"></span>**Fehler " \_ DS \_ kein \_ NTDSA- \_ Objekt"**
</dt> <dd> <dl> <dt>

8623 (0x21af)
</dt> <dt>



Das NTDS-Einstellungs Objekt für den Domänen Controller ist nicht vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NON_ASQ_SEARCH"></span><span id="error_ds_non_asq_search"></span>**Fehler " \_ DS \_ nicht- \_ ASQ- \_ Suche"**
</dt> <dd> <dl> <dt>

8624 (0x21b0)
</dt> <dt>



Der angeforderte Suchvorgang wird für ASQ-suchen nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_AUDIT_FAILURE"></span><span id="error_ds_audit_failure"></span>**Fehler bei DS-Überwachungs Fehler \_ \_ \_**
</dt> <dd> <dl> <dt>

8625 (0x21b1)
</dt> <dt>



Für den Vorgang konnte kein erforderliches Überwachungs Ereignis generiert werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INVALID_SEARCH_FLAG_SUBTREE"></span><span id="error_ds_invalid_search_flag_subtree"></span>**Fehler \_ DS \_ ungültige \_ \_ suchflag- \_ Unterstruktur.**
</dt> <dd> <dl> <dt>

8626 (0x21b2)
</dt> <dt>



Die Suchflags für das Attribut sind ungültig. Das Teilstruktur-indexbit ist nur für einwertige Attribute gültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INVALID_SEARCH_FLAG_TUPLE"></span><span id="error_ds_invalid_search_flag_tuple"></span>**Fehler- \_ DS \_ ungültiges \_ \_ suchflag- \_ Tupel.**
</dt> <dd> <dl> <dt>

8627 (0x21b3)
</dt> <dt>



Die Suchflags für das Attribut sind ungültig. Das tupelindexbit ist nur für Attribute von Unicode-Zeichen folgen gültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_HIERARCHY_TABLE_TOO_DEEP"></span><span id="error_ds_hierarchy_table_too_deep"></span>**Fehler- \_ DS- \_ Hierarchie \_ Tabelle \_ zu \_ tief**
</dt> <dd> <dl> <dt>

8628 (0x21b4)
</dt> <dt>



Die Adressbücher sind zu tief geschachtelt. Fehler beim Erstellen der Hierarchie Tabelle.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_CORRUPT_UTD_VECTOR"></span><span id="error_ds_dra_corrupt_utd_vector"></span>**Fehler \_ DS-Vektor für beschädigte \_ \_ \_ Utd- \_ Vektor**
</dt> <dd> <dl> <dt>

8629 (0x21b5)
</dt> <dt>



Der angegebene Aktualitäts Vektor ist beschädigt.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_SECRETS_DENIED"></span><span id="error_ds_dra_secrets_denied"></span>**Fehler \_ DS \_ DRA- \_ Geheimnisse \_ verweigert**
</dt> <dd> <dl> <dt>

8630 (0x21b6)
</dt> <dt>



Die Anforderung zum Replizieren von geheimen Schlüsseln wird verweigert.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_RESERVED_MAPI_ID"></span><span id="error_ds_reserved_mapi_id"></span>**Fehler- \_ DS \_ reservierte \_ MAPI- \_ ID**
</dt> <dd> <dl> <dt>

8631 (0x21b7)
</dt> <dt>



Fehler beim Aktualisieren des Schemas: der MAPI-Bezeichner ist reserviert.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MAPI_ID_NOT_AVAILABLE"></span><span id="error_ds_mapi_id_not_available"></span>**Fehler \_ DS- \_ MAPI- \_ ID \_ nicht \_ verfügbar**
</dt> <dd> <dl> <dt>

8632 (0x21b8)
</dt> <dt>



Fehler beim Aktualisieren des Schemas: Es sind keine MAPI-Bezeichner verfügbar.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_MISSING_KRBTGT_SECRET"></span><span id="error_ds_dra_missing_krbtgt_secret"></span>**Fehler- \_ DS in \_ DRA \_ fehlt \_ krbtgt \_ Secret**
</dt> <dd> <dl> <dt>

8633 (0x21b9)
</dt> <dt>



Der Replikations Vorgang ist fehlgeschlagen, da die erforderlichen Attribute des lokalen krbtgt-Objekts fehlen.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DOMAIN_NAME_EXISTS_IN_FOREST"></span><span id="error_ds_domain_name_exists_in_forest"></span>**Fehler \_ DS \_ Domänen \_ Name ist \_ \_ in der \_ Gesamtstruktur vorhanden.**
</dt> <dd> <dl> <dt>

8634 (0x21ba)
</dt> <dt>



Der Domänen Name der vertrauenswürdigen Domäne ist bereits in der Gesamtstruktur vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_FLAT_NAME_EXISTS_IN_FOREST"></span><span id="error_ds_flat_name_exists_in_forest"></span>**Fehler \_ DS \_ - \_ flatname ist \_ \_ in der \_ Gesamtstruktur vorhanden.**
</dt> <dd> <dl> <dt>

8635 (0x21bb)
</dt> <dt>



Der flatname der vertrauenswürdigen Domäne ist bereits in der Gesamtstruktur vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_USER_PRINCIPAL_NAME"></span><span id="error_invalid_user_principal_name"></span>**Fehler bei \_ ungültigem \_ Benutzer \_ Prinzipal \_ Namen**
</dt> <dd> <dl> <dt>

8636 (0x21bc)
</dt> <dt>



Der Benutzer Prinzipal Name (User Principal Name, UPN) ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OID_MAPPED_GROUP_CANT_HAVE_MEMBERS"></span><span id="error_ds_oid_mapped_group_cant_have_members"></span>**Fehler \_ DS-OID zugeordnete \_ Gruppe darf \_ \_ \_ \_ keine \_ Mitglieder aufweisen.**
</dt> <dd> <dl> <dt>

8637 (0x21bd)
</dt> <dt>



OID zugeordnete Gruppen dürfen keine Member aufweisen.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OID_NOT_FOUND"></span><span id="error_ds_oid_not_found"></span>**Fehler- \_ DS- \_ OID \_ nicht \_ gefunden.**
</dt> <dd> <dl> <dt>

8638 (0x21be)
</dt> <dt>



Die angegebene OID wurde nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_RECYCLED_TARGET"></span><span id="error_ds_dra_recycled_target"></span>**Fehler \_ DS \_ \_ \_**
</dt> <dd> <dl> <dt>

8639 (0x21bf)
</dt> <dt>



Der Replikations Vorgang ist fehlgeschlagen, da das Zielobjekt, auf das durch einen Linkwert verwiesen wird,


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DISALLOWED_NC_REDIRECT"></span><span id="error_ds_disallowed_nc_redirect"></span>**Fehler- \_ DS \_ unzulässige \_ NC- \_ Umleitung**
</dt> <dd> <dl> <dt>

8640 (0x21c0)
</dt> <dt>



Beim Umleitungs Vorgang ist ein Fehler aufgetreten, da sich das Zielobjekt in einem anderen NC als der Domänen-NC des aktuellen Domänen Controllers befindet.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_HIGH_ADLDS_FFL"></span><span id="error_ds_high_adlds_ffl"></span>**Fehler \_ DS \_ High \_ ADLDS \_ FFL**
</dt> <dd> <dl> <dt>

8641 (0x21c1)
</dt> <dt>



Die Funktionsebene des AD LDS Konfigurations Satzes kann nicht auf den angeforderten Wert gesenkt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_HIGH_DSA_VERSION"></span><span id="error_ds_high_dsa_version"></span>**Fehler \_ DS \_ High \_ DSA- \_ Version**
</dt> <dd> <dl> <dt>

8642 (0x21c2)
</dt> <dt>



Die Funktionsebene der Domäne (oder Gesamtstruktur) kann nicht auf den angeforderten Wert gesenkt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_LOW_ADLDS_FFL"></span><span id="error_ds_low_adlds_ffl"></span>**Fehler \_ DS \_ niedrige \_ ADLDS- \_ FFL**
</dt> <dd> <dl> <dt>

8643 (0x21c3)
</dt> <dt>



Die Funktionsebene des AD LDS Konfigurations Satzes kann nicht auf den angeforderten Wert festgelegt werden, da mindestens eine ADLDS-Instanz vorhanden ist, die sich auf einer niedrigeren inkompatiblen Funktionsebene befindet.


</dt> </dl> </dd> <dt>

<span id="ERROR_DOMAIN_SID_SAME_AS_LOCAL_WORKSTATION"></span><span id="error_domain_sid_same_as_local_workstation"></span>**Fehler \_ Domänen- \_ sid identisch mit der \_ \_ \_ lokalen \_ Arbeitsstation**
</dt> <dd> <dl> <dt>

8644 (0x21c4)
</dt> <dt>



Der Domänen Beitritt kann nicht abgeschlossen werden, da die SID der Domäne, die Sie beitreten wollten, mit der SID dieses Computers identisch ist. Dies ist ein Symptom für eine nicht ordnungsgemäß geklonte Betriebssystem Installation. Sie sollten systreup auf diesem Computer ausführen, um eine neue Computer-SID zu generieren. Unter <https://go.microsoft.com/fwlink/p/?linkid=168895> finden Sie weitere Informationen.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_UNDELETE_SAM_VALIDATION_FAILED"></span><span id="error_ds_undelete_sam_validation_failed"></span>**Fehler beim Wiederherstellen der \_ \_ Sam- \_ \_ Validierung \_**
</dt> <dd> <dl> <dt>

8645 (0x21c5)
</dt> <dt>



Der Vorgang zum Wiederherstellen ist fehlgeschlagen, weil der SAM-Kontoname oder der zusätzliche SAM-Konto Name des nicht gelöschten Objekts mit einem vorhandenen Live Objekt in Konflikt steht.


</dt> </dl> </dd> <dt>

<span id="ERROR_INCORRECT_ACCOUNT_TYPE"></span><span id="error_incorrect_account_type"></span>**\_fehlerhafter \_ \_ Kontotyp**
</dt> <dd> <dl> <dt>

8646 (0x21c6)
</dt> <dt>



Das System ist für das angegebene Konto nicht autorisierend und kann daher den Vorgang nicht durchführen. Wiederholen Sie den Vorgang mithilfe des Anbieters, der diesem Konto zugeordnet ist. Wenn es sich hierbei um einen Online Anbieter handelt, verwenden Sie die Online Website des Anbieters.


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

 

 




