---
description: Beschreibt die in der Header Datei "Winerror. h" definierten Fehlercodes 9000-11999 und ist für Entwickler bestimmt.
ms.assetid: 27fe3fee-4ae3-43f1-a1f2-91c935e9851b
title: System Fehler Codes (9000-11999) (Winerror. h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: 01eb071962d8d0f5beb801067ce1d72adc796bad
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748377"
---
# <a name="system-error-codes-9000-11999"></a>System Fehler Codes (9000-11999)

> [!NOTE]
> Diese Informationen sind für Entwickler gedacht, die Systemfehler Debuggen. Bei anderen Fehlern, wie z. b. Problemen mit Windows Update, finden Sie eine Liste der Ressourcen auf der Seite [Fehlercodes](system-error-codes.md) .

In der folgenden Liste werden die [Systemfehler Codes](system-error-codes.md) (Fehler 9000 bis 11999) beschrieben. Sie werden von der [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) -Funktion zurückgegeben, wenn viele Funktionen fehlschlagen. Um den Beschreibungstext für den Fehler in Ihrer Anwendung abzurufen, verwenden Sie die [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) -Funktion mit dem Flag " **Format \_ Message \_ from \_ System** ".

<dl> <dt>

<span id="DNS_ERROR_RCODE_FORMAT_ERROR"></span><span id="dns_error_rcode_format_error"></span>**DNS- \_ Fehler \_ RCODE- \_ Format \_ Fehler**
</dt> <dd> <dl> <dt>

9001 (0x2329)
</dt> <dt>



Der DNS-Server kann das Format nicht interpretieren.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RCODE_SERVER_FAILURE"></span><span id="dns_error_rcode_server_failure"></span>**DNS- \_ Fehler \_ RCODE- \_ Server Fehler \_**
</dt> <dd> <dl> <dt>

9002 (0x232a)
</dt> <dt>



DNS-Server Fehler


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RCODE_NAME_ERROR"></span><span id="dns_error_rcode_name_error"></span>**DNS- \_ Fehler \_ RCODE- \_ namens \_ Fehler**
</dt> <dd> <dl> <dt>

9003 (0x232b)
</dt> <dt>



Der DNS-Name ist nicht vorhanden.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RCODE_NOT_IMPLEMENTED"></span><span id="dns_error_rcode_not_implemented"></span>**DNS- \_ Fehler- \_ RCODE \_ nicht \_ implementiert**
</dt> <dd> <dl> <dt>

9004 (0x232c)
</dt> <dt>



Die DNS-Anforderung wird vom Namen Server nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RCODE_REFUSED"></span><span id="dns_error_rcode_refused"></span>**DNS- \_ Fehler \_ RCODE wurde \_ verweigert.**
</dt> <dd> <dl> <dt>

9005 (0x232d)
</dt> <dt>



Der DNS-Vorgang wurde verweigert.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RCODE_YXDOMAIN"></span><span id="dns_error_rcode_yxdomain"></span>**DNS- \_ Fehler \_ RCODE \_ yxdomain**
</dt> <dd> <dl> <dt>

9006 (0x232e)
</dt> <dt>



Der DNS-Name, der nicht vorhanden sein sollte, ist vorhanden.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RCODE_YXRRSET"></span><span id="dns_error_rcode_yxrrset"></span>**DNS- \_ Fehler \_ RCODE \_ yxrrset**
</dt> <dd> <dl> <dt>

9007 (0x232f)
</dt> <dt>



Der DNS-RR-Satz, der nicht vorhanden sein sollte, ist vorhanden.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RCODE_NXRRSET"></span><span id="dns_error_rcode_nxrrset"></span>**DNS- \_ Fehler \_ RCODE \_ nxrrset**
</dt> <dd> <dl> <dt>

9008 (0x2330)
</dt> <dt>



Der DNS-RR-Satz, der vorhanden sein sollte, ist nicht vorhanden.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RCODE_NOTAUTH"></span><span id="dns_error_rcode_notauth"></span>**DNS- \_ Fehler \_ RCODE \_ notauth**
</dt> <dd> <dl> <dt>

9009 (0x2331)
</dt> <dt>



DNS-Server ist für die Zone nicht autorisierend.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RCODE_NOTZONE"></span><span id="dns_error_rcode_notzone"></span>**DNS- \_ Fehler \_ RCODE \_ notzone**
</dt> <dd> <dl> <dt>

9010 (0x2332)
</dt> <dt>



Der DNS-Name in Update oder Prereq ist nicht in der Zone.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RCODE_BADSIG"></span><span id="dns_error_rcode_badsig"></span>**DNS- \_ Fehler \_ RCODE \_ BadSig**
</dt> <dd> <dl> <dt>

9016 (0x2338)
</dt> <dt>



Fehler beim Überprüfen der DNS-Signatur.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RCODE_BADKEY"></span><span id="dns_error_rcode_badkey"></span>**DNS- \_ Fehler \_ RCODE \_ badkey**
</dt> <dd> <dl> <dt>

9017 (0x2339)
</dt> <dt>



Ungültiger DNS-Schlüssel.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RCODE_BADTIME"></span><span id="dns_error_rcode_badtime"></span>**DNS- \_ Fehler \_ RCODE \_ badtime**
</dt> <dd> <dl> <dt>

9018 (0x233a)
</dt> <dt>



Gültigkeit der DNS-Signatur ist abgelaufen.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_KEYMASTER_REQUIRED"></span><span id="dns_error_keymaster_required"></span>**DNS- \_ Fehler \_ keymaster \_ erforderlich**
</dt> <dd> <dl> <dt>

9101 (0x238d)
</dt> <dt>



Dieser Vorgang kann nur von dem DNS-Server durchgeführt werden, der als Schlüssel Master für die Zone fungiert.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NOT_ALLOWED_ON_SIGNED_ZONE"></span><span id="dns_error_not_allowed_on_signed_zone"></span>**DNS- \_ Fehler ist \_ \_ \_ in der \_ signierten \_ Zone nicht zulässig.**
</dt> <dd> <dl> <dt>

9102 (0x238e)
</dt> <dt>



Dieser Vorgang ist für eine signierte oder signierte Zone nicht zulässig.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NSEC3_INCOMPATIBLE_WITH_RSA_SHA1"></span><span id="dns_error_nsec3_incompatible_with_rsa_sha1"></span>**DNS- \_ Fehler \_ NSEC3 nicht \_ kompatibel \_ mit \_ RSA \_ SHA1**
</dt> <dd> <dl> <dt>

9103 (0x238f)
</dt> <dt>



NSEC3 ist nicht kompatibel mit dem RSA-SHA-1-Algorithmus. Wählen Sie einen anderen Algorithmus aus, oder verwenden Sie nsec.

Dieser Wert wurde auch als **DNS- \_ Fehler \_ ungültig \_ NSEC3 \_ Parameter** bezeichnet.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NOT_ENOUGH_SIGNING_KEY_DESCRIPTORS"></span><span id="dns_error_not_enough_signing_key_descriptors"></span>**DNS- \_ Fehler \_ nicht \_ genug \_ Signatur \_ Schlüssel \_ Deskriptoren**
</dt> <dd> <dl> <dt>

9104 (0x2390)
</dt> <dt>



Die Zone verfügt nicht über genügend Signatur Schlüssel. Es muss mindestens ein Schlüssel Signatur Schlüssel (Key Signing Key, KSK) und mindestens ein Zonen Signatur Schlüssel (ZSK) vorhanden sein.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_UNSUPPORTED_ALGORITHM"></span><span id="dns_error_unsupported_algorithm"></span>**\_ \_ nicht unterstützter DNS-Fehler \_ Algorithmus**
</dt> <dd> <dl> <dt>

9105 (0x2391)
</dt> <dt>



Der angegebene Algorithmus wird nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_INVALID_KEY_SIZE"></span><span id="dns_error_invalid_key_size"></span>**DNS- \_ Fehler \_ ungültige \_ Schlüssel \_ Größe**
</dt> <dd> <dl> <dt>

9106 (0x2392)
</dt> <dt>



Die angegebene Schlüsselgröße wird nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_SIGNING_KEY_NOT_ACCESSIBLE"></span><span id="dns_error_signing_key_not_accessible"></span>**der DNS- \_ Fehler \_ Signatur \_ Schlüssel ist \_ nicht \_ verfügbar.**
</dt> <dd> <dl> <dt>

9107 (0x2393)
</dt> <dt>



Der DNS-Server kann auf mindestens einen der Signatur Schlüssel für eine Zone nicht zugreifen. Die Zonen Signierung ist erst dann betriebsbereit, wenn der Fehler behoben wurde.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_KSP_DOES_NOT_SUPPORT_PROTECTION"></span><span id="dns_error_ksp_does_not_support_protection"></span>**DNS- \_ Fehler \_ KSP \_ bietet \_ keine \_ Unterstützung \_ für den Schutz**
</dt> <dd> <dl> <dt>

9108 (0x2394)
</dt> <dt>



Der angegebene Schlüsselspeicher Anbieter unterstützt nicht DPAPI + +-Datenschutz. Die Zonen Signierung ist erst dann betriebsbereit, wenn der Fehler behoben wurde.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_UNEXPECTED_DATA_PROTECTION_ERROR"></span><span id="dns_error_unexpected_data_protection_error"></span>**\_unerwarteter DNS-Fehler beim \_ \_ Schutz von Daten \_ \_ .**
</dt> <dd> <dl> <dt>

9109 (0x2395)
</dt> <dt>



Ein unerwarteter DPAPI + +-Fehler ist aufgetreten. Die Zonen Signierung ist erst dann betriebsbereit, wenn der Fehler behoben wurde.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_UNEXPECTED_CNG_ERROR"></span><span id="dns_error_unexpected_cng_error"></span>**\_ \_ unerwarteter \_ CNG- \_ Fehler bei DNS-Fehler**
</dt> <dd> <dl> <dt>

9110 (0x2396)
</dt> <dt>



Ein unerwarteter Kryptografiefehler ist aufgetreten. Die Zonen Signierung ist möglicherweise erst funktionstüchtig, wenn dieser Fehler behoben wurde.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_UNKNOWN_SIGNING_PARAMETER_VERSION"></span><span id="dns_error_unknown_signing_parameter_version"></span>**DNS- \_ Fehler bei \_ unbekannter \_ Signatur \_ Parameter \_ Version.**
</dt> <dd> <dl> <dt>

9111 (0x2397)
</dt> <dt>



Der DNS-Server hat einen Signatur Schlüssel mit einer unbekannten Version gefunden. Die Zonen Signierung ist erst dann betriebsbereit, wenn der Fehler behoben wurde.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_KSP_NOT_ACCESSIBLE"></span><span id="dns_error_ksp_not_accessible"></span>**DNS- \_ Fehler- \_ KSP \_ nicht \_ verfügbar**
</dt> <dd> <dl> <dt>

9112 (0x2398)
</dt> <dt>



Der angegebene Schlüsseldienst Anbieter kann nicht vom DNS-Server geöffnet werden.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_TOO_MANY_SKDS"></span><span id="dns_error_too_many_skds"></span>**DNS- \_ Fehler \_ zu \_ viele \_ SKDS**
</dt> <dd> <dl> <dt>

9113 (0x2399)
</dt> <dt>



Der DNS-Server kann keine weiteren Signatur Schlüssel mit dem angegebenen Algorithmus und dem KSK-Flagwert für diese Zone akzeptieren.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_INVALID_ROLLOVER_PERIOD"></span><span id="dns_error_invalid_rollover_period"></span>**DNS- \_ Fehler bei \_ ungültigem \_ rolloverzeitraum \_**
</dt> <dd> <dl> <dt>

9114 (0x239a)
</dt> <dt>



Der angegebene rolloverzeitraum ist ungültig.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_INVALID_INITIAL_ROLLOVER_OFFSET"></span><span id="dns_error_invalid_initial_rollover_offset"></span>**DNS- \_ Fehler beim \_ \_ anfänglichen \_ rolloveroffset. \_**
</dt> <dd> <dl> <dt>

9115 (0x239b)
</dt> <dt>



Der angegebene anfängliche rolloveroffset ist ungültig.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_ROLLOVER_IN_PROGRESS"></span><span id="dns_error_rollover_in_progress"></span>**DNS \_ - \_ fehlerrollover wird ausgeführt \_ \_**
</dt> <dd> <dl> <dt>

9116 (0x239c)
</dt> <dt>



Der angegebene Signatur Schlüssel ist bereits im Prozess des Rollbacks von Schlüsseln.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_STANDBY_KEY_NOT_PRESENT"></span><span id="dns_error_standby_key_not_present"></span>**DNS- \_ Fehler \_ Standby- \_ Schlüssel \_ nicht \_ vorhanden**
</dt> <dd> <dl> <dt>

9117 (0x239d)
</dt> <dt>



Der angegebene Signatur Schlüssel hat keine Standby-Taste, die widerrufen werden kann.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NOT_ALLOWED_ON_ZSK"></span><span id="dns_error_not_allowed_on_zsk"></span>**DNS- \_ Fehler ist \_ \_ \_ für \_ ZSK nicht zulässig.**
</dt> <dd> <dl> <dt>

9118 (0x239e)
</dt> <dt>



Dieser Vorgang ist für einen Zonen Signatur Schlüssel (ZSK) nicht zulässig.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NOT_ALLOWED_ON_ACTIVE_SKD"></span><span id="dns_error_not_allowed_on_active_skd"></span>**DNS- \_ Fehler ist \_ \_ \_ für \_ aktive \_ SKD nicht zulässig.**
</dt> <dd> <dl> <dt>

9119 (0x239f)
</dt> <dt>



Dieser Vorgang ist für einen aktiven Signatur Schlüssel nicht zulässig.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_ROLLOVER_ALREADY_QUEUED"></span><span id="dns_error_rollover_already_queued"></span>**DNS \_ - \_ fehlerrollover bereits in die \_ \_ Warteschlange eingereiht**
</dt> <dd> <dl> <dt>

9120 (0x23a0)
</dt> <dt>



Der angegebene Signatur Schlüssel befindet sich bereits in der Warteschlange für einen Rollover.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NOT_ALLOWED_ON_UNSIGNED_ZONE"></span><span id="dns_error_not_allowed_on_unsigned_zone"></span>**DNS- \_ Fehler \_ in nicht \_ \_ \_ signierter \_ Zone nicht zulässig.**
</dt> <dd> <dl> <dt>

9121 (0x23a1)
</dt> <dt>



Dieser Vorgang ist in einer nicht signierten Zone nicht zulässig.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_BAD_KEYMASTER"></span><span id="dns_error_bad_keymaster"></span>**DNS- \_ Fehler fehlerhafter \_ \_ keymaster**
</dt> <dd> <dl> <dt>

9122 (0x23a2)
</dt> <dt>



Dieser Vorgang konnte nicht abgeschlossen werden, da der DNS-Server, der als aktueller Schlüssel Master für diese Zone aufgeführt ist, nicht oder falsch konfiguriert ist. Beheben Sie das Problem auf dem aktuellen Schlüssel Master für diese Zone, oder verwenden Sie einen anderen DNS-Server, um die Schlüssel Master Rolle zu übernehmen.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_INVALID_SIGNATURE_VALIDITY_PERIOD"></span><span id="dns_error_invalid_signature_validity_period"></span>**DNS- \_ Fehler \_ ungültige \_ Signatur \_ Gültigkeits \_ Dauer.**
</dt> <dd> <dl> <dt>

9123 (0x23a3)
</dt> <dt>



Der angegebene Gültigkeits Zeitraum der Signatur ist ungültig.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_INVALID_NSEC3_ITERATION_COUNT"></span><span id="dns_error_invalid_nsec3_iteration_count"></span>**DNS- \_ Fehler \_ ungültige \_ NSEC3 \_ iterations \_ Anzahl**
</dt> <dd> <dl> <dt>

9124 (0x23a4)
</dt> <dt>



Die angegebene Anzahl von NSEC3 Iterationen ist höher als die zulässige Mindestschlüssellänge in der Zone.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_DNSSEC_IS_DISABLED"></span><span id="dns_error_dnssec_is_disabled"></span>**DNS- \_ Fehler \_ DNSSEC \_ ist \_ deaktiviert.**
</dt> <dd> <dl> <dt>

9125 (0x23a5)
</dt> <dt>



Dieser Vorgang konnte nicht abgeschlossen werden, da der DNS-Server mit deaktivierten DNSSEC-Funktionen konfiguriert wurde. Aktivieren Sie DNSSEC auf dem DNS-Server.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_INVALID_XML"></span><span id="dns_error_invalid_xml"></span>**DNS- \_ Fehler \_ ungültiges \_ XML.**
</dt> <dd> <dl> <dt>

9126 (0x23a6)
</dt> <dt>



Dieser Vorgang konnte nicht abgeschlossen werden, da der empfangene XML-Datenstrom leer oder syntaktisch ungültig ist.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NO_VALID_TRUST_ANCHORS"></span><span id="dns_error_no_valid_trust_anchors"></span>**DNS- \_ Fehler \_ keine \_ gültigen \_ Vertrauens \_ Anker**
</dt> <dd> <dl> <dt>

9127 (0x23a7)
</dt> <dt>



Dieser Vorgang wurde abgeschlossen, aber es wurden keine Vertrauensanker hinzugefügt, da alle empfangenen Vertrauensanker entweder ungültig, nicht unterstützt, abgelaufen sind oder in weniger als 30 Tagen nicht gültig werden.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_ROLLOVER_NOT_POKEABLE"></span><span id="dns_error_rollover_not_pokeable"></span>**DNS \_ - \_ fehlerrollover nicht in den \_ \_ Besitz**
</dt> <dd> <dl> <dt>

9128 (0x23a8)
</dt> <dt>



Der angegebene Signatur Schlüssel wartet nicht auf das Update der Eltern-DS.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NSEC3_NAME_COLLISION"></span><span id="dns_error_nsec3_name_collision"></span>**DNS- \_ Fehler \_ NSEC3 \_ namens \_ Konflikt**
</dt> <dd> <dl> <dt>

9129 (0x23a9)
</dt> <dt>



Hash Kollision während der NSEC3-Signierung erkannt. Geben Sie einen anderen vom Benutzer bereitgestellten Salt an, oder verwenden Sie einen zufällig generierten Salt-Typ, und versuchen Sie erneut, die Zone zu signieren.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NSEC_INCOMPATIBLE_WITH_NSEC3_RSA_SHA1"></span><span id="dns_error_nsec_incompatible_with_nsec3_rsa_sha1"></span>**DNS- \_ Fehler \_ nsec nicht \_ kompatibel \_ mit \_ NSEC3 \_ RSA \_ SHA1**
</dt> <dd> <dl> <dt>

9130 (0x23aa)
</dt> <dt>



Nsec ist nicht kompatibel mit dem NSEC3-RSA-SHA-1-Algorithmus. Wählen Sie einen anderen Algorithmus aus, oder verwenden Sie NSEC3.


</dt> </dl> </dd> <dt>

<span id="DNS_INFO_NO_RECORDS"></span><span id="dns_info_no_records"></span>**DNS- \_ Info \_ keine \_ Datensätze**
</dt> <dd> <dl> <dt>

9501 (0x251d)
</dt> <dt>



Bei der DNS-Abfrage wurden keine Einträge gefunden.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_BAD_PACKET"></span><span id="dns_error_bad_packet"></span>**DNS \_ - \_ Fehler \_ Paket**
</dt> <dd> <dl> <dt>

9502 (0x251e)
</dt> <dt>



Ungültiges DNS-Paket.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NO_PACKET"></span><span id="dns_error_no_packet"></span>**DNS- \_ Fehler " \_ kein \_ Paket"**
</dt> <dd> <dl> <dt>

9503 (0x251f)
</dt> <dt>



Kein DNS-Paket.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RCODE"></span><span id="dns_error_rcode"></span>**DNS- \_ Fehler- \_ RCODE**
</dt> <dd> <dl> <dt>

9504 (0x2520)
</dt> <dt>



DNS-Fehler, überprüfen Sie RCODE.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_UNSECURE_PACKET"></span><span id="dns_error_unsecure_packet"></span>**unsichere DNS- \_ Fehler \_ \_ Paket**
</dt> <dd> <dl> <dt>

9505 (0x2521)
</dt> <dt>



Ungesichertes DNS-Paket.


</dt> </dl> </dd> <dt>

<span id="DNS_REQUEST_PENDING"></span><span id="dns_request_pending"></span>**ausstehende DNS- \_ Anforderung \_**
</dt> <dd> <dl> <dt>

9506 (0x2522)
</dt> <dt>



Die DNS-Abfrage Anforderung steht aus.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_INVALID_TYPE"></span><span id="dns_error_invalid_type"></span>**\_ \_ Ungültiger DNS- \_ Fehlertyp**
</dt> <dd> <dl> <dt>

9551 (0x254f)
</dt> <dt>



Ungültiger DNS-Typ.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_INVALID_IP_ADDRESS"></span><span id="dns_error_invalid_ip_address"></span>**DNS \_ \_ -Fehler ungültige \_ IP- \_ Adresse**
</dt> <dd> <dl> <dt>

9552 (0x2550)
</dt> <dt>



Ungültige IP-Adresse.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_INVALID_PROPERTY"></span><span id="dns_error_invalid_property"></span>**\_Fehler bei \_ Ungültiger DNS- \_ Eigenschaft**
</dt> <dd> <dl> <dt>

9553 (0x2551)
</dt> <dt>



Ungültige Eigenschaft.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_TRY_AGAIN_LATER"></span><span id="dns_error_try_again_later"></span>**DNS \_ - \_ Fehler \_ später erneut versuchen \_**
</dt> <dd> <dl> <dt>

9554 (0x2552)
</dt> <dt>



Versuchen Sie den DNS-Vorgang später erneut.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NOT_UNIQUE"></span><span id="dns_error_not_unique"></span>**DNS- \_ Fehler ist \_ nicht \_ eindeutig.**
</dt> <dd> <dl> <dt>

9555 (0x2553)
</dt> <dt>



Der Datensatz für den angegebenen Namen und Typ ist nicht eindeutig.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NON_RFC_NAME"></span><span id="dns_error_non_rfc_name"></span>**DNS- \_ Fehler \_ nicht RFC- \_ \_ Name**
</dt> <dd> <dl> <dt>

9556 (0x2554)
</dt> <dt>



Der DNS-Name entspricht nicht den RFC-Spezifikationen.


</dt> </dl> </dd> <dt>

<span id="DNS_STATUS_FQDN"></span><span id="dns_status_fqdn"></span>**DNS- \_ Status- \_ FQDN**
</dt> <dd> <dl> <dt>

9557 (0x2555)
</dt> <dt>



Der DNS-Name ist ein voll qualifizierter DNS-Name.


</dt> </dl> </dd> <dt>

<span id="DNS_STATUS_DOTTED_NAME"></span><span id="dns_status_dotted_name"></span>**DNS- \_ Status Punkt \_ \_ Name**
</dt> <dd> <dl> <dt>

9558 (0x2556)
</dt> <dt>



Der DNS-Name ist gepunktet (mehrfach Bezeichnung).


</dt> </dl> </dd> <dt>

<span id="DNS_STATUS_SINGLE_PART_NAME"></span><span id="dns_status_single_part_name"></span>**DNS- \_ Status \_ einzelner \_ Teil \_ Name**
</dt> <dd> <dl> <dt>

9559 (0x2557)
</dt> <dt>



Der DNS-Name ist ein einteilige Name.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_INVALID_NAME_CHAR"></span><span id="dns_error_invalid_name_char"></span>**DNS- \_ Fehler \_ ungültiger \_ Name \_ Char**
</dt> <dd> <dl> <dt>

9560 (0x2558)
</dt> <dt>



Der DNS-Name enthält ein ungültiges Zeichen.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NUMERIC_NAME"></span><span id="dns_error_numeric_name"></span>**\_ \_ numerischer \_ Name des DNS-Fehlers**
</dt> <dd> <dl> <dt>

9561 (0x2559)
</dt> <dt>



Der DNS-Name ist vollständig numerisch.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NOT_ALLOWED_ON_ROOT_SERVER"></span><span id="dns_error_not_allowed_on_root_server"></span>**DNS-Fehler ist auf dem Stamm \_ \_ \_ \_ \_ \_ Server nicht zulässig.**
</dt> <dd> <dl> <dt>

9562 (0x255 a)
</dt> <dt>



Der angeforderte Vorgang ist auf einem DNS-Stamm Server nicht zulässig.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NOT_ALLOWED_UNDER_DELEGATION"></span><span id="dns_error_not_allowed_under_delegation"></span>**DNS \_ - \_ Fehler \_ \_ bei \_ Delegierung nicht zulässig.**
</dt> <dd> <dl> <dt>

9563 (0x255 b)
</dt> <dt>



Der Datensatz konnte nicht erstellt werden, da dieser Teil des DNS-Namespace an einen anderen Server delegiert wurde.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_CANNOT_FIND_ROOT_HINTS"></span><span id="dns_error_cannot_find_root_hints"></span>**DNS-Fehler beim finden von Stamm \_ \_ \_ \_ hinweisen nicht gefunden \_**
</dt> <dd> <dl> <dt>

9564 (0x255 c)
</dt> <dt>



Der DNS-Server konnte einen Satz von Stamm hinweisen nicht finden.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_INCONSISTENT_ROOT_HINTS"></span><span id="dns_error_inconsistent_root_hints"></span>**DNS- \_ Fehler \_ inkonsistente Stamm \_ \_ Hinweise**
</dt> <dd> <dl> <dt>

9565 (0x255 d)
</dt> <dt>



Der DNS-Server hat Stamm Hinweise gefunden, aber er war für alle Adapter nicht konsistent.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_DWORD_VALUE_TOO_SMALL"></span><span id="dns_error_dword_value_too_small"></span>**DNS- \_ Fehler \_ DWORD- \_ Wert \_ zu \_ klein**
</dt> <dd> <dl> <dt>

9566 (0x255 e)
</dt> <dt>



Der angegebene Wert ist für diesen Parameter zu klein.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_DWORD_VALUE_TOO_LARGE"></span><span id="dns_error_dword_value_too_large"></span>**DNS- \_ Fehler \_ DWORD-Wert ist \_ \_ zu \_ groß.**
</dt> <dd> <dl> <dt>

9567 (0x255 f)
</dt> <dt>



Der angegebene Wert ist zu groß für diesen Parameter.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_BACKGROUND_LOADING"></span><span id="dns_error_background_loading"></span>**DNS- \_ Fehler beim \_ Laden im Hintergrund \_**
</dt> <dd> <dl> <dt>

9568 (0x2560)
</dt> <dt>



Dieser Vorgang ist nicht zulässig, wenn der DNS-Server Zonen im Hintergrund lädt. Versuchen Sie es später noch mal.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NOT_ALLOWED_ON_RODC"></span><span id="dns_error_not_allowed_on_rodc"></span>**DNS- \_ Fehler ist \_ auf dem \_ \_ \_ RODC nicht zulässig.**
</dt> <dd> <dl> <dt>

9569 (0x2561)
</dt> <dt>



Der angeforderte Vorgang ist für einen DNS-Server, der auf einem schreibgeschützten Domänen Controller ausgeführt wird, nicht zulässig.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NOT_ALLOWED_UNDER_DNAME"></span><span id="dns_error_not_allowed_under_dname"></span>**DNS- \_ Fehler ist \_ \_ \_ unter \_ dname nicht zulässig.**
</dt> <dd> <dl> <dt>

9570 (0x2562)
</dt> <dt>



Unterhalb eines dname-Einsatzes dürfen keine Daten vorhanden sein.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_DELEGATION_REQUIRED"></span><span id="dns_error_delegation_required"></span>**DNS- \_ Fehler \_ Delegierung \_ erforderlich**
</dt> <dd> <dl> <dt>

9571 (0x2563)
</dt> <dt>



Dieser Vorgang erfordert die Delegierung von Anmelde Informationen.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_INVALID_POLICY_TABLE"></span><span id="dns_error_invalid_policy_table"></span>**\_ \_ ungültige \_ Richtlinien \_ Tabelle für DNS-Fehler**
</dt> <dd> <dl> <dt>

9572 (0x2564)
</dt> <dt>



Die Richtlinien Tabelle für die Namensauflösung ist beschädigt. Die DNS-Auflösung schlägt fehl, bis Sie korrigiert wird. Wenden Sie sich an den Netzwerkadministrator.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_ZONE_DOES_NOT_EXIST"></span><span id="dns_error_zone_does_not_exist"></span>**die DNS- \_ Fehler \_ Zone \_ ist \_ nicht \_ vorhanden.**
</dt> <dd> <dl> <dt>

9601 (0x2581)
</dt> <dt>



Die DNS-Zone ist nicht vorhanden.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NO_ZONE_INFO"></span><span id="dns_error_no_zone_info"></span>**DNS- \_ Fehler \_ ohne \_ Zonen \_ Informationen**
</dt> <dd> <dl> <dt>

9602 (0x2582)
</dt> <dt>



Es sind keine DNS-Zonen Informationen verfügbar.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_INVALID_ZONE_OPERATION"></span><span id="dns_error_invalid_zone_operation"></span>**DNS- \_ Fehler \_ ungültiger \_ Zonen \_ Vorgang.**
</dt> <dd> <dl> <dt>

9603 (0x2583)
</dt> <dt>



Ungültiger Vorgang für die DNS-Zone.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_ZONE_CONFIGURATION_ERROR"></span><span id="dns_error_zone_configuration_error"></span>**DNS- \_ Fehler \_ Zonen- \_ Konfigurations \_ Fehler**
</dt> <dd> <dl> <dt>

9604 (0x2584)
</dt> <dt>



Ungültige DNS-Zonen Konfiguration.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_ZONE_HAS_NO_SOA_RECORD"></span><span id="dns_error_zone_has_no_soa_record"></span>**DNS- \_ Fehler \_ Zone \_ weist \_ keinen SOA- \_ \_ Datensatz auf.**
</dt> <dd> <dl> <dt>

9605 (0x2585)
</dt> <dt>



Die DNS-Zone hat keinen Start-of-Authority-Datensatz (SOA).


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_ZONE_HAS_NO_NS_RECORDS"></span><span id="dns_error_zone_has_no_ns_records"></span>**DNS- \_ Fehler \_ Zone \_ enthält \_ keine NS- \_ \_ Einträge.**
</dt> <dd> <dl> <dt>

9606 (0x2586)
</dt> <dt>



Die DNS-Zone hat keinen Name Server-Datensatz (NS).


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_ZONE_LOCKED"></span><span id="dns_error_zone_locked"></span>**DNS- \_ Fehler \_ Zone \_ gesperrt**
</dt> <dd> <dl> <dt>

9607 (0x2587)
</dt> <dt>



Die DNS-Zone ist gesperrt.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_ZONE_CREATION_FAILED"></span><span id="dns_error_zone_creation_failed"></span>**Fehler beim Erstellen der DNS- \_ Fehler \_ Zone \_ \_**
</dt> <dd> <dl> <dt>

9608 (0x2588)
</dt> <dt>



Fehler beim Erstellen der DNS-Zone.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_ZONE_ALREADY_EXISTS"></span><span id="dns_error_zone_already_exists"></span>**DNS- \_ Fehler \_ Zone \_ bereits \_ vorhanden**
</dt> <dd> <dl> <dt>

9609 (0x2589)
</dt> <dt>



Die DNS-Zone ist bereits vorhanden.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_AUTOZONE_ALREADY_EXISTS"></span><span id="dns_error_autozone_already_exists"></span>**DNS \_ - \_ fehlerautozone ist \_ bereits \_ vorhanden.**
</dt> <dd> <dl> <dt>

9610 (0x258a)
</dt> <dt>



Die automatische DNS-Zone ist bereits vorhanden.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_INVALID_ZONE_TYPE"></span><span id="dns_error_invalid_zone_type"></span>**DNS- \_ Fehler \_ ungültiger \_ \_ Zonentyp.**
</dt> <dd> <dl> <dt>

9611 (0x258b)
</dt> <dt>



Ungültiger DNS-Zonentyp.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_SECONDARY_REQUIRES_MASTER_IP"></span><span id="dns_error_secondary_requires_master_ip"></span>**DNS \_ \_ -Fehler Sekundär \_ erfordert \_ Master \_ -IP**
</dt> <dd> <dl> <dt>

9612 (0x258c)
</dt> <dt>



Die sekundäre DNS-Zone erfordert die Master-IP-Adresse


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_ZONE_NOT_SECONDARY"></span><span id="dns_error_zone_not_secondary"></span>**DNS- \_ Fehler \_ Zone \_ nicht \_ Sekundär**
</dt> <dd> <dl> <dt>

9613 (0x258d)
</dt> <dt>



DNS-Zone ist nicht sekundär.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NEED_SECONDARY_ADDRESSES"></span><span id="dns_error_need_secondary_addresses"></span>**DNS- \_ Fehler bei \_ Bedarf \_ Sekundär \_ Adressen**
</dt> <dd> <dl> <dt>

9614 (0x258e)
</dt> <dt>



Sekundäre IP-Adresse erforderlich.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_WINS_INIT_FAILED"></span><span id="dns_error_wins_init_failed"></span>**DNS \_ - \_ Fehler \_ WINS \_ -Initialisierungsfehler**
</dt> <dd> <dl> <dt>

9615 (0x258f)
</dt> <dt>



Fehler bei der WINS-Initialisierung.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NEED_WINS_SERVERS"></span><span id="dns_error_need_wins_servers"></span>**DNS- \_ Fehler bei \_ WINS- \_ \_ Servern**
</dt> <dd> <dl> <dt>

9616 (0x2590)
</dt> <dt>



Sie benötigen WINS-Server.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NBSTAT_INIT_FAILED"></span><span id="dns_error_nbstat_init_failed"></span>**DNS- \_ Fehler \_ bei NBSTAT- \_ Init \_ .**
</dt> <dd> <dl> <dt>

9617 (0x2591)
</dt> <dt>



Fehler beim nbtstat-Initialisierungs Rückruf.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_SOA_DELETE_INVALID"></span><span id="dns_error_soa_delete_invalid"></span>**DNS- \_ Fehler- \_ SOA- \_ Löschung \_ ungültig**
</dt> <dd> <dl> <dt>

9618 (0x2592)
</dt> <dt>



Ungültiges Löschen von Autoritäts Anfang (SOA).


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_FORWARDER_ALREADY_EXISTS"></span><span id="dns_error_forwarder_already_exists"></span>**die DNS- \_ Fehler \_ Weiterleitung ist \_ bereits \_ vorhanden.**
</dt> <dd> <dl> <dt>

9619 (0x2593)
</dt> <dt>



Für diesen Namen ist bereits eine bedingte Weiterleitungs Zone vorhanden.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_ZONE_REQUIRES_MASTER_IP"></span><span id="dns_error_zone_requires_master_ip"></span>**DNS \_ \_ -Fehler Zone \_ erfordert \_ Master \_ -IP**
</dt> <dd> <dl> <dt>

9620 (0x2594)
</dt> <dt>



Diese Zone muss mit mindestens einer Master-DNS-Server-IP-Adresse konfiguriert werden.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_ZONE_IS_SHUTDOWN"></span><span id="dns_error_zone_is_shutdown"></span>**DNS- \_ Fehler \_ Zone \_ wird \_ heruntergefahren**
</dt> <dd> <dl> <dt>

9621 (0x2595)
</dt> <dt>



Der Vorgang kann nicht ausgeführt werden, da diese Zone heruntergefahren wird.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_ZONE_LOCKED_FOR_SIGNING"></span><span id="dns_error_zone_locked_for_signing"></span>**DNS \_ - \_ Fehler \_ Zone \_ für \_ Signierung gesperrt**
</dt> <dd> <dl> <dt>

9622 (0x2596)
</dt> <dt>



Dieser Vorgang kann nicht ausgeführt werden, da die Zone derzeit signiert wird. Versuchen Sie es später noch mal.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_PRIMARY_REQUIRES_DATAFILE"></span><span id="dns_error_primary_requires_datafile"></span>**DNS- \_ Fehler \_ primär \_ erfordert \_ DataFile**
</dt> <dd> <dl> <dt>

9651 (0x25b3)
</dt> <dt>



Die primäre DNS-Zone erfordert "DataFile".


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_INVALID_DATAFILE_NAME"></span><span id="dns_error_invalid_datafile_name"></span>**DNS- \_ Fehler \_ ungültiger \_ DataFile- \_ Name.**
</dt> <dd> <dl> <dt>

9652 (0x25b4)
</dt> <dt>



Ungültiger Datendatei-Name für die DNS-Zone.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_DATAFILE_OPEN_FAILURE"></span><span id="dns_error_datafile_open_failure"></span>**\_Fehler beim \_ Öffnen der Daten \_ Datei \_ im DNS-Fehler**
</dt> <dd> <dl> <dt>

9653 (0x25b5)
</dt> <dt>



Fehler beim Öffnen der Datendatei für die DNS-Zone.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_FILE_WRITEBACK_FAILED"></span><span id="dns_error_file_writeback_failed"></span>**Fehler beim Rück Schreiben der DNS- \_ Fehler \_ Datei. \_ \_**
</dt> <dd> <dl> <dt>

9654 (0x25b6)
</dt> <dt>



Fehler beim Schreiben der Datendatei für die DNS-Zone.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_DATAFILE_PARSING"></span><span id="dns_error_datafile_parsing"></span>**DNS- \_ Fehler \_ Datendatei \_ -Verarbeitung**
</dt> <dd> <dl> <dt>

9655 (0x25b7)
</dt> <dt>



Fehler beim Lesen der Datendatei für die DNS-Zone.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RECORD_DOES_NOT_EXIST"></span><span id="dns_error_record_does_not_exist"></span>**der DNS- \_ Fehler \_ Daten Satz \_ ist \_ nicht \_ vorhanden.**
</dt> <dd> <dl> <dt>

9701 (0x25e5)
</dt> <dt>



Der DNS-Datensatz ist nicht vorhanden.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RECORD_FORMAT"></span><span id="dns_error_record_format"></span>**DNS- \_ Fehler \_ Daten Satz \_ Format**
</dt> <dd> <dl> <dt>

9702 (0x25e6)
</dt> <dt>



Fehler im DNS-Daten Satz Format.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NODE_CREATION_FAILED"></span><span id="dns_error_node_creation_failed"></span>**Fehler bei der DNS- \_ Fehler \_ Knoten \_ Erstellung \_**
</dt> <dd> <dl> <dt>

9703 (0x25e7)
</dt> <dt>



Fehler bei der Knoten Erstellung in DNS.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_UNKNOWN_RECORD_TYPE"></span><span id="dns_error_unknown_record_type"></span>**Unbekannter DNS- \_ Fehler \_ \_ Daten Satz \_ .**
</dt> <dd> <dl> <dt>

9704 (0x25e8)
</dt> <dt>



Unbekannter DNS-Daten eingabentyp.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RECORD_TIMED_OUT"></span><span id="dns_error_record_timed_out"></span>**Timeout beim DNS- \_ Fehler \_ Daten Satz. \_ \_**
</dt> <dd> <dl> <dt>

9705 (0x25e9)
</dt> <dt>



Timeout beim DNS-Datensatz.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NAME_NOT_IN_ZONE"></span><span id="dns_error_name_not_in_zone"></span>**DNS- \_ Fehler \_ Name \_ nicht \_ in \_ Zone**
</dt> <dd> <dl> <dt>

9706 (0x25ea)
</dt> <dt>



Der Name ist nicht in der DNS-Zone.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_CNAME_LOOP"></span><span id="dns_error_cname_loop"></span>**DNS- \_ Fehler \_ CNAME- \_ Schleife**
</dt> <dd> <dl> <dt>

9707 (0x25eb)
</dt> <dt>



CNAME-Schleife erkannt.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NODE_IS_CNAME"></span><span id="dns_error_node_is_cname"></span>**DNS- \_ Fehler \_ Knoten ist " \_ \_ CNAME"**
</dt> <dd> <dl> <dt>

9708 (0x25ec)
</dt> <dt>



Knoten ist ein CNAME-DNS-Datensatz.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_CNAME_COLLISION"></span><span id="dns_error_cname_collision"></span>**DNS- \_ Fehler \_ CNAME- \_ Kollision**
</dt> <dd> <dl> <dt>

9709 (0x25ed)
</dt> <dt>



Für den angegebenen Namen ist bereits ein CNAME-Datensatz vorhanden.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RECORD_ONLY_AT_ZONE_ROOT"></span><span id="dns_error_record_only_at_zone_root"></span>**DNS- \_ Fehler \_ Daten Satz \_ nur \_ in \_ Zonenstamm \_**
</dt> <dd> <dl> <dt>

9710 (0x25ee)
</dt> <dt>



Nur in DNS-Zonen Stamm aufzeichnen.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RECORD_ALREADY_EXISTS"></span><span id="dns_error_record_already_exists"></span>**DNS- \_ Fehler \_ Daten Satz ist \_ bereits \_ vorhanden**
</dt> <dd> <dl> <dt>

9711 (0x25ef)
</dt> <dt>



Der DNS-Datensatz ist bereits vorhanden.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_SECONDARY_DATA"></span><span id="dns_error_secondary_data"></span>**sekundäre DNS- \_ Fehler \_ \_ Daten**
</dt> <dd> <dl> <dt>

9712 (0x25f 0)
</dt> <dt>



Daten der sekundären DNS-Zone.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NO_CREATE_CACHE_DATA"></span><span id="dns_error_no_create_cache_data"></span>**DNS- \_ Fehler \_ No \_ Create \_ Cache \_ Data**
</dt> <dd> <dl> <dt>

9713 (0x25f 1)
</dt> <dt>



Es konnten keine DNS-Cache Daten erstellt werden.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NAME_DOES_NOT_EXIST"></span><span id="dns_error_name_does_not_exist"></span>**der DNS- \_ Fehler \_ Name \_ ist \_ nicht \_ vorhanden.**
</dt> <dd> <dl> <dt>

9714 (0x25f 2)
</dt> <dt>



Der DNS-Name ist nicht vorhanden.


</dt> </dl> </dd> <dt>

<span id="DNS_WARNING_PTR_CREATE_FAILED"></span><span id="dns_warning_ptr_create_failed"></span>**Fehler beim Erstellen der DNS- \_ Warnung \_ ptr. \_ \_**
</dt> <dd> <dl> <dt>

9715 (0x25f)
</dt> <dt>



Der Zeiger (PTR)-Datensatz konnte nicht erstellt werden.


</dt> </dl> </dd> <dt>

<span id="DNS_WARNING_DOMAIN_UNDELETED"></span><span id="dns_warning_domain_undeleted"></span>**DNS- \_ Warn \_ Domäne \_ nicht gelöscht**
</dt> <dd> <dl> <dt>

9716 (0x25f 4)
</dt> <dt>



Die DNS-Domäne wurde wieder hergestellt.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_DS_UNAVAILABLE"></span><span id="dns_error_ds_unavailable"></span>**DNS- \_ Fehler- \_ DS nicht \_ verfügbar**
</dt> <dd> <dl> <dt>

9717 (0x25f)
</dt> <dt>



Der Verzeichnisdienst ist nicht verfügbar.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_DS_ZONE_ALREADY_EXISTS"></span><span id="dns_error_ds_zone_already_exists"></span>**DNS- \_ Fehler- \_ DS- \_ Zone \_ bereits \_ vorhanden**
</dt> <dd> <dl> <dt>

9718 (0x25f 6)
</dt> <dt>



Die DNS-Zone ist im Verzeichnisdienst bereits vorhanden.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NO_BOOTFILE_IF_DS_ZONE"></span><span id="dns_error_no_bootfile_if_ds_zone"></span>**DNS- \_ Fehler \_ keine \_ BootFile, \_ Wenn DS- \_ \_ Zone**
</dt> <dd> <dl> <dt>

9719 (0x25f)
</dt> <dt>



Der DNS-Server erstellt oder liest die Startdatei für die integrierte DNS-Zone des Verzeichnis Dienstanbieter nicht.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NODE_IS_DNAME"></span><span id="dns_error_node_is_dname"></span>**DNS- \_ Fehler \_ Knoten ist " \_ \_ DName"**
</dt> <dd> <dl> <dt>

9720 (0x25f 8)
</dt> <dt>



Knoten ist ein DNS-Datensatz mit dname.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_DNAME_COLLISION"></span><span id="dns_error_dname_collision"></span>**DNS- \_ Fehler \_ dname- \_ Kollision**
</dt> <dd> <dl> <dt>

9721 (0x25f)
</dt> <dt>



Für den angegebenen Namen ist bereits ein DNAME-Datensatz vorhanden.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_ALIAS_LOOP"></span><span id="dns_error_alias_loop"></span>**DNS \_ - \_ fehleralias \_ Schleife**
</dt> <dd> <dl> <dt>

9722 (0x25fa)
</dt> <dt>



Eine Alias Schleife wurde mit CNAME-oder dname-Einträgen erkannt.


</dt> </dl> </dd> <dt>

<span id="DNS_INFO_AXFR_COMPLETE"></span><span id="dns_info_axfr_complete"></span>**DNS- \_ Info- \_ AXFR \_ fertiggestellt**
</dt> <dd> <dl> <dt>

9751 (0x2617)
</dt> <dt>



DNS AXFR (Zonen Übertragung) ist fertiggestellt.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_AXFR"></span><span id="dns_error_axfr"></span>**DNS- \_ Fehler \_ AXFR**
</dt> <dd> <dl> <dt>

9752 (0x2618)
</dt> <dt>



Fehler bei der DNS-Zonen Übertragung.


</dt> </dl> </dd> <dt>

<span id="DNS_INFO_ADDED_LOCAL_WINS"></span><span id="dns_info_added_local_wins"></span>**DNS- \_ Info \_ hinzugefügter \_ lokaler \_ WINS**
</dt> <dd> <dl> <dt>

9753 (0x2619)
</dt> <dt>



Lokaler WINS-Server wurde hinzugefügt.


</dt> </dl> </dd> <dt>

<span id="DNS_STATUS_CONTINUE_NEEDED"></span><span id="dns_status_continue_needed"></span>**DNS- \_ Status \_ fortsetzen \_ erforderlich**
</dt> <dd> <dl> <dt>

9801 (0x2649)
</dt> <dt>



Der sichere Aktualisierungs Vorgang muss die Aktualisierungs Anforderung fortsetzen.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NO_TCPIP"></span><span id="dns_error_no_tcpip"></span>**DNS- \_ Fehler \_ No \_ tcpip**
</dt> <dd> <dl> <dt>

9851 (0x267b)
</dt> <dt>



Das TCP/IP-Netzwerkprotokoll ist nicht installiert.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NO_DNS_SERVERS"></span><span id="dns_error_no_dns_servers"></span>**DNS- \_ Fehler \_ keine DNS- \_ \_ Server**
</dt> <dd> <dl> <dt>

9852 (0x267c)
</dt> <dt>



Für das lokale System sind keine DNS-Server konfiguriert.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_DP_DOES_NOT_EXIST"></span><span id="dns_error_dp_does_not_exist"></span>**DNS- \_ Fehler- \_ DP \_ ist \_ nicht \_ vorhanden.**
</dt> <dd> <dl> <dt>

9901 (0x26ad)
</dt> <dt>



Die angegebene Verzeichnis Partition ist nicht vorhanden.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_DP_ALREADY_EXISTS"></span><span id="dns_error_dp_already_exists"></span>**DNS- \_ Fehler- \_ DP \_ bereits \_ vorhanden**
</dt> <dd> <dl> <dt>

9902 (0x26ae)
</dt> <dt>



Die angegebene Verzeichnis Partition ist bereits vorhanden.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_DP_NOT_ENLISTED"></span><span id="dns_error_dp_not_enlisted"></span>**DNS- \_ Fehler- \_ DP \_ nicht \_ eingetragen**
</dt> <dd> <dl> <dt>

9903 (0x26af)
</dt> <dt>



Dieser DNS-Server ist nicht in der angegebenen Verzeichnis Partition eingetragen.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_DP_ALREADY_ENLISTED"></span><span id="dns_error_dp_already_enlisted"></span>**DNS- \_ Fehler- \_ DP \_ bereits \_ eingetragen**
</dt> <dd> <dl> <dt>

9904 (0x26b0)
</dt> <dt>



Dieser DNS-Server ist bereits in der angegebenen Verzeichnis Partition eingetragen.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_DP_NOT_AVAILABLE"></span><span id="dns_error_dp_not_available"></span>**DNS- \_ Fehler- \_ DP \_ nicht \_ verfügbar**
</dt> <dd> <dl> <dt>

9905 (0x26b1)
</dt> <dt>



Die Verzeichnis Partition ist zurzeit nicht verfügbar. Bitte warten Sie einige Minuten, und versuchen Sie es erneut.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_DP_FSMO_ERROR"></span><span id="dns_error_dp_fsmo_error"></span>**DNS- \_ Fehler bei \_ DP- \_ \_ Fehler**
</dt> <dd> <dl> <dt>

9906 (0x26b2)
</dt> <dt>



Der Vorgang ist fehlgeschlagen, da die Domänen Namen-Master-Rolle nicht erreicht werden konnte. Der Domänen Controller mit der FSMO-Rolle "Domänen Namen Master" ist nicht in der Lage, die Anforderung zu bedienen, oder er führt nicht Windows Server 2003 oder höher aus.


</dt> </dl> </dd> <dt>

<span id="WSAEINTR"></span><span id="wsaeintr"></span>**Wsaeingabe**
</dt> <dd> <dl> <dt>

10004 (0x2714)
</dt> <dt>



Ein Blockierungs Vorgang wurde durch einen wsacancelblockingstatement-Aufrufvorgang unterbrochen.


</dt> </dl> </dd> <dt>

<span id="WSAEBADF"></span><span id="wsaebadf"></span>**Wsaebadf**
</dt> <dd> <dl> <dt>

10009 (0x2719)
</dt> <dt>



Das angegebene Datei Handle ist ungültig.


</dt> </dl> </dd> <dt>

<span id="WSAEACCES"></span><span id="wsaeacces"></span>**WSAEACCES**
</dt> <dd> <dl> <dt>

10013 (0x271d)
</dt> <dt>



Es wurde versucht, auf einen Socket auf eine Weise zuzugreifen, die durch seine Zugriffsberechtigungen unzulässig ist.


</dt> </dl> </dd> <dt>

<span id="WSAEFAULT"></span><span id="wsaefault"></span>**Wsaefault**
</dt> <dd> <dl> <dt>

10014 (0x271e)
</dt> <dt>



Das System hat bei dem Versuch, ein Zeigerargument in einem-Befehl zu verwenden, eine ungültige Zeiger Adresse erkannt.


</dt> </dl> </dd> <dt>

<span id="WSAEINVAL"></span><span id="wsaeinval"></span>**Wsaabval**
</dt> <dd> <dl> <dt>

10022 (0x2726)
</dt> <dt>



Ein ungültiges Argument wurde angegeben.


</dt> </dl> </dd> <dt>

<span id="WSAEMFILE"></span><span id="wsaemfile"></span>**Wsaemfile**
</dt> <dd> <dl> <dt>

10024 (0x2728)
</dt> <dt>



Zu viele geöffnete Sockets.


</dt> </dl> </dd> <dt>

<span id="WSAEWOULDBLOCK"></span><span id="wsaewouldblock"></span>**WSAEWOULDBLOCK**
</dt> <dd> <dl> <dt>

10035 (0x2733)
</dt> <dt>



Ein nicht blockierender Socketvorgang konnte nicht sofort abgeschlossen werden.


</dt> </dl> </dd> <dt>

<span id="WSAEINPROGRESS"></span><span id="wsaeinprogress"></span>**Wsaeingabe Progress**
</dt> <dd> <dl> <dt>

10036 (0x2734)
</dt> <dt>



Ein Blockierungsvorgang wird momentan ausgeführt.


</dt> </dl> </dd> <dt>

<span id="WSAEALREADY"></span><span id="wsaealready"></span>**Wsaebereits**
</dt> <dd> <dl> <dt>

10037 (0x2735)
</dt> <dt>



Es wurde versucht, für einen nicht blockierenden Socket, für den bereits ein Vorgang ausgeführt wurde, einen weiteren Vorgang auszuführen.


</dt> </dl> </dd> <dt>

<span id="WSAENOTSOCK"></span><span id="wsaenotsock"></span>**Wsaumotsock**
</dt> <dd> <dl> <dt>

10038 (0x2736)
</dt> <dt>



Es wurde versucht, einen Vorgang für etwas auszuführen, das kein Socket ist.


</dt> </dl> </dd> <dt>

<span id="WSAEDESTADDRREQ"></span><span id="wsaedestaddrreq"></span>**WSAEDESTADDRREQ**
</dt> <dd> <dl> <dt>

10039 (0x2737)
</dt> <dt>



Eine erforderliche Adresse wurde bei einem Vorgang für einen Socket ausgelassen.


</dt> </dl> </dd> <dt>

<span id="WSAEMSGSIZE"></span><span id="wsaemsgsize"></span>**Wsaemsgsize**
</dt> <dd> <dl> <dt>

10040 (0x2738)
</dt> <dt>



Eine Nachricht, die über einen Datagrammsocket gesendet wurde, war für den internen Nachrichtenpuffer oder ein anderes Netzwerklimit zu groß, oder der Puffer für den Datagrammempfang war für das Datagramm zu klein.


</dt> </dl> </dd> <dt>

<span id="WSAEPROTOTYPE"></span><span id="wsaeprototype"></span>**WSAEPROTOTYPE**
</dt> <dd> <dl> <dt>

10041 (0x2739)
</dt> <dt>



Im Socket-Funktions Aufrufwert wurde ein Protokoll angegeben, das die Semantik des angeforderten Sockettyps nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="WSAENOPROTOOPT"></span><span id="wsaenoprotoopt"></span>**Wsaumoproumopt**
</dt> <dd> <dl> <dt>

10042 (0x273a)
</dt> <dt>



Eine unbekannte, ungültige oder nicht unterstützte Option oder Ebene wurde in einem getsockopt-oder setsockopt-Befehl angegeben.


</dt> </dl> </dd> <dt>

<span id="WSAEPROTONOSUPPORT"></span><span id="wsaeprotonosupport"></span>**Wsaeprotonosupport**
</dt> <dd> <dl> <dt>

10043 (0x273b)
</dt> <dt>



Das angeforderte Protokoll wurde nicht im System konfiguriert, oder es ist keine Implementierung vorhanden.


</dt> </dl> </dd> <dt>

<span id="WSAESOCKTNOSUPPORT"></span><span id="wsaesocktnosupport"></span>**Wsaesocktnosupport**
</dt> <dd> <dl> <dt>

10044 (0x273c)
</dt> <dt>



In dieser Adressfamilie ist die Unterstützung für den angegebenen Sockettyp nicht vorhanden.


</dt> </dl> </dd> <dt>

<span id="WSAEOPNOTSUPP"></span><span id="wsaeopnotsupp"></span>**WSAEOPNOTSUPP**
</dt> <dd> <dl> <dt>

10045 (0x273d)
</dt> <dt>



Der versuchte Vorgang wird für den Typ des Objekts, auf das verwiesen wird, nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="WSAEPFNOSUPPORT"></span><span id="wsaepfnosupport"></span>**Wsaepf NoSupport**
</dt> <dd> <dl> <dt>

10046 (0x273e)
</dt> <dt>



Die Protokollfamilie wurde nicht im System konfiguriert, oder es ist keine Implementierung vorhanden.


</dt> </dl> </dd> <dt>

<span id="WSAEAFNOSUPPORT"></span><span id="wsaeafnosupport"></span>**WSAEAFNOSUPPORT**
</dt> <dd> <dl> <dt>

10047 (0x273f)
</dt> <dt>



Es wurde eine Adresse verwendet, die nicht mit dem angeforderten Protokoll kompatibel ist.


</dt> </dl> </dd> <dt>

<span id="WSAEADDRINUSE"></span><span id="wsaeaddrinuse"></span>**WSAEADDRINUSE**
</dt> <dd> <dl> <dt>

10048 (0x2740)
</dt> <dt>



Only one usage of each socket address (protocol/network address/port) is normally permitted.


</dt> </dl> </dd> <dt>

<span id="WSAEADDRNOTAVAIL"></span><span id="wsaeaddrnotavail"></span>**Wsaeaddrnotavail**
</dt> <dd> <dl> <dt>

10049 (0x2741)
</dt> <dt>



Die angeforderte Adresse ist im Kontext nicht gültig.


</dt> </dl> </dd> <dt>

<span id="WSAENETDOWN"></span><span id="wsaenetdown"></span>**Wsaaufetdown**
</dt> <dd> <dl> <dt>

10050 (0x2742)
</dt> <dt>



Bei einem Socketvorgang war das Netzwerk inaktiv.


</dt> </dl> </dd> <dt>

<span id="WSAENETUNREACH"></span><span id="wsaenetunreach"></span>**Wsaumetunreach**
</dt> <dd> <dl> <dt>

10051 (0x2743)
</dt> <dt>



Es wurde versucht, ein Socketvorgang in ein nicht erreichbares Netzwerk auszuführen.


</dt> </dl> </dd> <dt>

<span id="WSAENETRESET"></span><span id="wsaenetreset"></span>**Wsaenetreset**
</dt> <dd> <dl> <dt>

10052 (0x2744)
</dt> <dt>



Die Verbindung wurde unterbrochen, weil eine Keep-Alive-Aktivität einen Fehler erkannt hat, während der Vorgang ausgeführt wurde.


</dt> </dl> </dd> <dt>

<span id="WSAECONNABORTED"></span><span id="wsaeconnaborted"></span>**WSAECONNABORTED**
</dt> <dd> <dl> <dt>

10053 (0x2745)
</dt> <dt>



Eine hergestellte Verbindung wurde durch die Software auf dem Hostcomputer abgebrochen.


</dt> </dl> </dd> <dt>

<span id="WSAECONNRESET"></span><span id="wsaeconnreset"></span>**WSAECONNRESET**
</dt> <dd> <dl> <dt>

10054 (0x2746)
</dt> <dt>



An existing connection was forcibly closed by the remote host.


</dt> </dl> </dd> <dt>

<span id="WSAENOBUFS"></span><span id="wsaenobufs"></span>**WSAENOBUFS**
</dt> <dd> <dl> <dt>

10055 (0x2747)
</dt> <dt>



Ein Vorgang für einen Socket konnte nicht durchgeführt werden, da das System nicht genügend Pufferspeicher hatte oder weil eine Warteschlange voll war.


</dt> </dl> </dd> <dt>

<span id="WSAEISCONN"></span><span id="wsaeisconn"></span>**Wsaeisconn**
</dt> <dd> <dl> <dt>

10056 (0x2748)
</dt> <dt>



Eine Verbindungsanforderung wurde an einem bereits verbundenen Socket vorgenommen.


</dt> </dl> </dd> <dt>

<span id="WSAENOTCONN"></span><span id="wsaenotconn"></span>**Wsaumotconn**
</dt> <dd> <dl> <dt>

10057 (0x2749)
</dt> <dt>



Eine Anforderung zum Senden oder Empfangen von Daten war unzulässig, weil der Socket nicht verbunden ist und (beim Senden über einen Datagrammsocket mithilfe eines sendto-Aufrufs) keine Adresse bereitgestellt wurde.


</dt> </dl> </dd> <dt>

<span id="WSAESHUTDOWN"></span><span id="wsaeshutdown"></span>**WSAESHUTDOWN**
</dt> <dd> <dl> <dt>

10058 (0x274a)
</dt> <dt>



Eine Anforderung zum Senden oder Empfangen von Daten wurde nicht zugelassen, da der Socket in die entsprechende Richtung bereits durch einen vorangegangenen shutdown-Aufruf heruntergefahren wurde.


</dt> </dl> </dd> <dt>

<span id="WSAETOOMANYREFS"></span><span id="wsaetoomanyrefs"></span>**Wsaetoomanyrefs**
</dt> <dd> <dl> <dt>

10059 (0x274b)
</dt> <dt>



Zu viele Verweise auf ein Kernel Objekt.


</dt> </dl> </dd> <dt>

<span id="WSAETIMEDOUT"></span><span id="wsaetimedout"></span>**WSAETIMEDOUT**
</dt> <dd> <dl> <dt>

10060 (0x274c)
</dt> <dt>



Ein Verbindungsversuch ist fehlgeschlagen, weil die verbundene Partei nach einem bestimmten Zeitraum nicht ordnungsgemäß reagiert hat, oder eine Verbindung konnte nicht hergestellt werden, da der verbundene Host nicht reagiert hat.


</dt> </dl> </dd> <dt>

<span id="WSAECONNREFUSED"></span><span id="wsaeconnrefused"></span>**Wsaeconnabgelehnte**
</dt> <dd> <dl> <dt>

10061 (0x274d)
</dt> <dt>



Es konnte keine Verbindung hergestellt werden, da diese vom Zielcomputer aktiv verweigert wurde.


</dt> </dl> </dd> <dt>

<span id="WSAELOOP"></span><span id="wsaeloop"></span>**Wsaeloop**
</dt> <dd> <dl> <dt>

10062 (0x274e)
</dt> <dt>



Der Name kann nicht übersetzt werden.


</dt> </dl> </dd> <dt>

<span id="WSAENAMETOOLONG"></span><span id="wsaenametoolong"></span>**Wsaenametoolong**
</dt> <dd> <dl> <dt>

10063 (0x274f)
</dt> <dt>



Die namens Komponente oder der Name ist zu lang.


</dt> </dl> </dd> <dt>

<span id="WSAEHOSTDOWN"></span><span id="wsaehostdown"></span>**Wsaehostdown**
</dt> <dd> <dl> <dt>

10064 (0x2750)
</dt> <dt>



Ein Socketvorgang ist fehlgeschlagen, da der Zielhost ausgefallen ist.


</dt> </dl> </dd> <dt>

<span id="WSAEHOSTUNREACH"></span><span id="wsaehostunreach"></span>**Wsaehostunreach**
</dt> <dd> <dl> <dt>

10065 (0x2751)
</dt> <dt>



Versuch eines Socketvorgangs für einen nicht erreichbaren Host.


</dt> </dl> </dd> <dt>

<span id="WSAENOTEMPTY"></span><span id="wsaenotempty"></span>**Wsaenotempty**
</dt> <dd> <dl> <dt>

10066 (0x2752)
</dt> <dt>



Ein nicht leeres Verzeichnis kann nicht entfernt werden.


</dt> </dl> </dd> <dt>

<span id="WSAEPROCLIM"></span><span id="wsaeproclim"></span>**Wsaeproclim**
</dt> <dd> <dl> <dt>

10067 (0x2753)
</dt> <dt>



Eine Windows Sockets-Implementierung kann eine Beschränkung für die Anzahl der Anwendungen aufweisen, die Sie gleichzeitig verwenden können.


</dt> </dl> </dd> <dt>

<span id="WSAEUSERS"></span><span id="wsaeusers"></span>**Wsaeusers**
</dt> <dd> <dl> <dt>

10068 (0x2754)
</dt> <dt>



Das Kontingent ist abgelaufen.


</dt> </dl> </dd> <dt>

<span id="WSAEDQUOT"></span><span id="wsaedquot"></span>**Wsaedquot**
</dt> <dd> <dl> <dt>

10069 (0x2755)
</dt> <dt>



Nicht genügend Datenträger Kontingent.


</dt> </dl> </dd> <dt>

<span id="WSAESTALE"></span><span id="wsaestale"></span>**Wsaestale**
</dt> <dd> <dl> <dt>

10070 (0x2756)
</dt> <dt>



Der Datei Handle-Verweis ist nicht mehr verfügbar.


</dt> </dl> </dd> <dt>

<span id="WSAEREMOTE"></span><span id="wsaeremote"></span>**Wsaeremote**
</dt> <dd> <dl> <dt>

10071 (0x2757)
</dt> <dt>



Das Element ist nicht lokal verfügbar.


</dt> </dl> </dd> <dt>

<span id="WSASYSNOTREADY"></span><span id="wsasysnotready"></span>**Wsasysnotready**
</dt> <dd> <dl> <dt>

10091 (0x276b)
</dt> <dt>



WSAStartup funktioniert zurzeit nicht, da das zugrunde liegende System, das zur Bereitstellung von Netzwerkdiensten verwendet wird, zurzeit nicht verfügbar ist.


</dt> </dl> </dd> <dt>

<span id="WSAVERNOTSUPPORTED"></span><span id="wsavernotsupported"></span>**Wsavernotsupported**
</dt> <dd> <dl> <dt>

10092 (0x276c)
</dt> <dt>



Die angeforderte Windows Sockets-Version wird nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="WSANOTINITIALISED"></span><span id="wsanotinitialised"></span>**Wsanotinitialisiert**
</dt> <dd> <dl> <dt>

10093 (0x276d)
</dt> <dt>



Entweder hat die Anwendung nicht WSAStartup aufgerufen, oder WSAStartup ist fehlgeschlagen.


</dt> </dl> </dd> <dt>

<span id="WSAEDISCON"></span><span id="wsaediscon"></span>**Wsaediscon**
</dt> <dd> <dl> <dt>

10101 (0x2775)
</dt> <dt>



Wird von WSARecv oder WSARecvFrom zurückgegeben, um anzugeben, dass die Remote Partei eine ordnungsgemäße Herunterfahr Sequenz initiiert hat.


</dt> </dl> </dd> <dt>

<span id="WSAENOMORE"></span><span id="wsaenomore"></span>**Wsaeromore**
</dt> <dd> <dl> <dt>

10102 (0x2776)
</dt> <dt>



Von WSALookupServiceNext können keine weiteren Ergebnisse zurückgegeben werden.


</dt> </dl> </dd> <dt>

<span id="WSAECANCELLED"></span><span id="wsaecancelled"></span>**Wsaecancelled**
</dt> <dd> <dl> <dt>

10103 (0x2777)
</dt> <dt>



Es wurde ein WSALookupServiceEnd aufgerufen, während dieser Rückruf noch verarbeitet wurde. Der-Rückruf wurde abgebrochen.


</dt> </dl> </dd> <dt>

<span id="WSAEINVALIDPROCTABLE"></span><span id="wsaeinvalidproctable"></span>**Wsaeinvalidproctable**
</dt> <dd> <dl> <dt>

10104 (0x2778)
</dt> <dt>



Die Prozedur "calltable" ist ungültig.


</dt> </dl> </dd> <dt>

<span id="WSAEINVALIDPROVIDER"></span><span id="wsaeinvalidprovider"></span>**Wsaeinvalidprovider**
</dt> <dd> <dl> <dt>

10105 (0x2779)
</dt> <dt>



Der angeforderte Dienstanbieter ist ungültig.


</dt> </dl> </dd> <dt>

<span id="WSAEPROVIDERFAILEDINIT"></span><span id="wsaeproviderfailedinit"></span>**Wsaeproviderfailedinit**
</dt> <dd> <dl> <dt>

10106 (0x277a)
</dt> <dt>



Der angeforderte Dienstanbieter konnte nicht geladen oder initialisiert werden.


</dt> </dl> </dd> <dt>

<span id="WSASYSCALLFAILURE"></span><span id="wsasyscallfailure"></span>**WSASYSCALLFAILURE**
</dt> <dd> <dl> <dt>

10107 (0x277b)
</dt> <dt>



Fehler beim System Aufruf.


</dt> </dl> </dd> <dt>

<span id="WSASERVICE_NOT_FOUND"></span><span id="wsaservice_not_found"></span>**wsaservice \_ nicht \_ gefunden.**
</dt> <dd> <dl> <dt>

10108 (0x277c)
</dt> <dt>



Dieser Dienst ist nicht bekannt. Der Dienst wurde im angegebenen Namespace nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="WSATYPE_NOT_FOUND"></span><span id="wsatype_not_found"></span>**wsatype \_ nicht \_ gefunden**
</dt> <dd> <dl> <dt>

10109 (0x277d)
</dt> <dt>



Die angegebene Klasse wurde nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="WSA_E_NO_MORE"></span><span id="wsa_e_no_more"></span>**WSA \_ E \_ nicht \_ mehr**
</dt> <dd> <dl> <dt>

10110 (0x277e)
</dt> <dt>



Von WSALookupServiceNext können keine weiteren Ergebnisse zurückgegeben werden.


</dt> </dl> </dd> <dt>

<span id="WSA_E_CANCELLED"></span><span id="wsa_e_cancelled"></span>**WSA \_ E \_ abgebrochen**
</dt> <dd> <dl> <dt>

10111 (0x277f)
</dt> <dt>



Es wurde ein WSALookupServiceEnd aufgerufen, während dieser Rückruf noch verarbeitet wurde. Der-Rückruf wurde abgebrochen.


</dt> </dl> </dd> <dt>

<span id="WSAEREFUSED"></span><span id="wsaerefused"></span>**Wsaerefused**
</dt> <dd> <dl> <dt>

10112 (0x2780)
</dt> <dt>



Eine Datenbankabfrage ist fehlgeschlagen, da Sie aktiv abgelehnt wurde.


</dt> </dl> </dd> <dt>

<span id="WSAHOST_NOT_FOUND"></span><span id="wsahost_not_found"></span>**wsahost \_ nicht \_ gefunden.**
</dt> <dd> <dl> <dt>

11001 (0x2af9)
</dt> <dt>



Ein solcher Host ist nicht bekannt.


</dt> </dl> </dd> <dt>

<span id="WSATRY_AGAIN"></span><span id="wsatry_again"></span>**wsatry \_ erneut**
</dt> <dd> <dl> <dt>

11002 (0x2afa)
</dt> <dt>



Hierbei handelt es sich in der Regel um einen temporären Fehler, der während der Auflösung von Hostnamen auftritt und einen Hinweis darauf liefert, dass der lokale Server keine Antwort von einem autorisierenden Server erhalten hat.


</dt> </dl> </dd> <dt>

<span id="WSANO_RECOVERY"></span><span id="wsano_recovery"></span>**wsano- \_ Wiederherstellung**
</dt> <dd> <dl> <dt>

11003 (0x2afb)
</dt> <dt>



Beim Datenbankaufruf ist ein nicht behebbarer Fehler aufgetreten.


</dt> </dl> </dd> <dt>

<span id="WSANO_DATA"></span><span id="wsano_data"></span>**wsano- \_ Daten**
</dt> <dd> <dl> <dt>

11004 (0x2afc)
</dt> <dt>



Der angeforderte Name ist gültig, aber es wurden keine Daten vom angeforderten Typ gefunden.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_RECEIVERS"></span><span id="wsa_qos_receivers"></span>**WSA- \_ QoS- \_ Empfänger**
</dt> <dd> <dl> <dt>

11005 (0x2afd)
</dt> <dt>



Mindestens eine Reserve ist eingetroffen.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_SENDERS"></span><span id="wsa_qos_senders"></span>**WSA- \_ QoS- \_ Sender**
</dt> <dd> <dl> <dt>

11006 (0x2afe)
</dt> <dt>



Mindestens ein Pfad ist eingetroffen.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_NO_SENDERS"></span><span id="wsa_qos_no_senders"></span>**WSA \_ QoS \_ No \_ Absenders**
</dt> <dd> <dl> <dt>

11007 (0x2aff)
</dt> <dt>



Es sind keine Absender vorhanden.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_NO_RECEIVERS"></span><span id="wsa_qos_no_receivers"></span>**WSA- \_ QoS \_ keine \_ Empfänger**
</dt> <dd> <dl> <dt>

11008 (0x2b00)
</dt> <dt>



Es sind keine Empfänger vorhanden.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_REQUEST_CONFIRMED"></span><span id="wsa_qos_request_confirmed"></span>**WSA- \_ QoS- \_ Anforderung \_ bestätigt**
</dt> <dd> <dl> <dt>

11009 (0x2b01)
</dt> <dt>



Reserve wurde bestätigt.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_ADMISSION_FAILURE"></span><span id="wsa_qos_admission_failure"></span>**WSA- \_ QoS- \_ Eintritts \_ Fehler**
</dt> <dd> <dl> <dt>

11010 (0x2b02)
</dt> <dt>



Fehler aufgrund fehlender Ressourcen.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_POLICY_FAILURE"></span><span id="wsa_qos_policy_failure"></span>**Fehler bei WSA- \_ QoS- \_ Richtlinie \_**
</dt> <dd> <dl> <dt>

11011 (0x2b03)
</dt> <dt>



Aus administrativen Gründen abgelehnt-ungültige Anmelde Informationen.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_BAD_STYLE"></span><span id="wsa_qos_bad_style"></span>**Ungültiger WSA- \_ QoS- \_ \_ Stil**
</dt> <dd> <dl> <dt>

11012 (0x2b04)
</dt> <dt>



Unbekannter oder in Konflikt stehender Stil.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_BAD_OBJECT"></span><span id="wsa_qos_bad_object"></span>**Ungültiges WSA- \_ QoS- \_ \_ Objekt**
</dt> <dd> <dl> <dt>

11013 (0x2b05)
</dt> <dt>



Problem mit einem Teil des FILTERSPEC-oder ProviderSpecific-Puffers im Allgemeinen.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_TRAFFIC_CTRL_ERROR"></span><span id="wsa_qos_traffic_ctrl_error"></span>**WSA- \_ QoS- \_ Datenverkehr \_ STRG- \_ Fehler**
</dt> <dd> <dl> <dt>

11014 (0x2b06)
</dt> <dt>



Problem mit einem Teil der Flowspec.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_GENERIC_ERROR"></span><span id="wsa_qos_generic_error"></span>**allgemeiner WSA- \_ QoS- \_ \_ Fehler**
</dt> <dd> <dl> <dt>

11015 (0x2b07)
</dt> <dt>



Allgemeiner QOS-Fehler.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_ESERVICETYPE"></span><span id="wsa_qos_eservicetype"></span>**WSA \_ QoS \_ eservicetype**
</dt> <dd> <dl> <dt>

11016 (0x2b08)
</dt> <dt>



In der Flowspec wurde ein ungültiger oder unbekannter Diensttyp gefunden.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_EFLOWSPEC"></span><span id="wsa_qos_eflowspec"></span>**WSA- \_ QoS- \_ eflowspec**
</dt> <dd> <dl> <dt>

11017 (0x2b09)
</dt> <dt>



In der QoS-Struktur wurde eine ungültige oder inkonsistente Flowspec gefunden.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_EPROVSPECBUF"></span><span id="wsa_qos_eprovspecbuf"></span>**WSA \_ QoS \_ eprovspecbuf**
</dt> <dd> <dl> <dt>

11018 (0x2b0a)
</dt> <dt>



Ungültiger QoS-Anbieter spezifischer Puffer.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_EFILTERSTYLE"></span><span id="wsa_qos_efilterstyle"></span>**WSA \_ QoS \_ efilterstyle**
</dt> <dd> <dl> <dt>

11019 (0x2b0b)
</dt> <dt>



Es wurde ein ungültiger QoS-Filter Stil verwendet.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_EFILTERTYPE"></span><span id="wsa_qos_efiltertype"></span>**WSA- \_ QoS \_ efiltertype**
</dt> <dd> <dl> <dt>

11020 (0x2b0c)
</dt> <dt>



Es wurde ein ungültiger QoS-Filtertyp verwendet.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_EFILTERCOUNT"></span><span id="wsa_qos_efiltercount"></span>**WSA- \_ QoS- \_ efiltercount**
</dt> <dd> <dl> <dt>

11021 (0x2b0d)
</dt> <dt>



Im FLOWDESCRIPTOR wurde eine falsche Anzahl von QoS-FILTERSPECs angegeben.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_EOBJLENGTH"></span><span id="wsa_qos_eobjlength"></span>**WSA- \_ QoS \_ eobjlength**
</dt> <dd> <dl> <dt>

11022 (0x2b0e)
</dt> <dt>



Im anbieterspezifischen QoS-Puffer wurde ein Objekt mit einem ungültigen objectlength-Feld angegeben.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_EFLOWCOUNT"></span><span id="wsa_qos_eflowcount"></span>**WSA- \_ QoS- \_ eflowcount**
</dt> <dd> <dl> <dt>

11023 (0x2b0f)
</dt> <dt>



In der QoS-Struktur wurde eine falsche Anzahl von Fluss Deskriptoren angegeben.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_EUNKOWNPSOBJ"></span><span id="wsa_qos_eunkownpsobj"></span>**WSA \_ QoS \_ eunkownpsobj**
</dt> <dd> <dl> <dt>

11024 (0x2b10)
</dt> <dt>



Ein unbekanntes Objekt wurde im QoS-anbieterspezifischen Puffer gefunden.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_EPOLICYOBJ"></span><span id="wsa_qos_epolicyobj"></span>**WSA \_ QoS \_ epolicyobj**
</dt> <dd> <dl> <dt>

11025 (0x2b11)
</dt> <dt>



Ein ungültiges Richtlinien Objekt wurde im QoS-anbieterspezifischen Puffer gefunden.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_EFLOWDESC"></span><span id="wsa_qos_eflowdesc"></span>**WSA \_ QoS \_ eflowde**
</dt> <dd> <dl> <dt>

11026 (0x2b12)
</dt> <dt>



In der Liste der flowdeskriptoren wurde ein ungültiger QoS-Datenfluss Deskriptor gefunden.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_EPSFLOWSPEC"></span><span id="wsa_qos_epsflowspec"></span>**WSA \_ QoS \_ epsflowspec**
</dt> <dd> <dl> <dt>

11027 (0x2b13)
</dt> <dt>



Im QoS-anbieterspezifischen Puffer wurde eine ungültige oder inkonsistente Flowspec gefunden.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_EPSFILTERSPEC"></span><span id="wsa_qos_epsfilterspec"></span>**WSA \_ QoS \_ epsfilterspec**
</dt> <dd> <dl> <dt>

11028 (0x2b14)
</dt> <dt>



Im QoS-anbieterspezifischen Puffer wurde eine ungültige FILTERSPEC gefunden.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_ESDMODEOBJ"></span><span id="wsa_qos_esdmodeobj"></span>**WSA \_ QoS \_ esdmodeobj**
</dt> <dd> <dl> <dt>

11029 (0x2b15)
</dt> <dt>



Ein ungültiges Shape-Verwerfungs Modus-Objekt wurde im QoS-anbieterspezifischen Puffer gefunden.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_ESHAPERATEOBJ"></span><span id="wsa_qos_eshaperateobj"></span>**WSA \_ QoS \_ eshaperateobj**
</dt> <dd> <dl> <dt>

11030 (0x2b16)
</dt> <dt>



Ein ungültiges Strukturierungs Raten Objekt wurde im QoS-anbieterspezifischen Puffer gefunden.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_RESERVED_PETYPE"></span><span id="wsa_qos_reserved_petype"></span>**reservierter "WSA \_ QoS"- \_ Peer- \_ Typ**
</dt> <dd> <dl> <dt>

11031 (0x2b17)
</dt> <dt>



Ein reserviertes Policy-Element wurde im QoS-anbieterspezifischen Puffer gefunden.


</dt> </dl> </dd> <dt>

<span id="WSA_SECURE_HOST_NOT_FOUND"></span><span id="wsa_secure_host_not_found"></span>**der sichere WSA- \_ \_ Host wurde \_ nicht \_ gefunden.**
</dt> <dd> <dl> <dt>

11032 (0x2b18)
</dt> <dt>



Ein solcher Host ist nicht sicher bekannt.


</dt> </dl> </dd> <dt>

<span id="WSA_IPSEC_NAME_POLICY_ERROR"></span><span id="wsa_ipsec_name_policy_error"></span>**WSA- \_ IPSec- \_ namens \_ Richtlinien \_ Fehler**
</dt> <dd> <dl> <dt>

11033 (0x2b19)
</dt> <dt>



Die namensbasierte IPSec-Richtlinie konnte nicht hinzugefügt werden.


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

 

 




