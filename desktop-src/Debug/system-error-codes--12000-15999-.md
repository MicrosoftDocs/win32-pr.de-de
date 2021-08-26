---
description: Beschreibt die Fehlercodes 12000-1599, die in der WinError.h-Headerdatei definiert sind und für Entwickler bestimmt sind.
ms.assetid: bb3c658d-96db-495a-a0dc-e93949c3835d
title: Systemfehlercodes (12000-15999) (WinError.h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: aa250eb26db3a2dfefda4c8b31bb2bbfd5e5d6415ea50d7279121fb09302c7ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120058990"
---
# <a name="system-error-codes-12000-15999"></a>Systemfehlercodes (12000-15999)

> [!NOTE]
> Diese Informationen sind für Entwickler bestimmt, die Systemfehler debuggen. Für andere Fehler, z. B. Probleme mit Windows Update, finden Sie auf der Seite [Fehlercodes](system-error-codes.md) eine Liste mit Ressourcen.

In der folgenden Liste werden [Systemfehlercodes](system-error-codes.md) (Fehler 12000 bis 15999) beschrieben. Sie werden von der [**GetLastError-Funktion**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) zurückgegeben, wenn viele Funktionen fehlschlagen. Um den Beschreibungstext für den Fehler in Ihrer Anwendung abzurufen, verwenden Sie die [**FormatMessage-Funktion**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) mit dem **FORMAT MESSAGE FROM \_ \_ \_ SYSTEM-Flag.**

<dl> <dt>

<span id="ERROR_INTERNET__"></span><span id="error_internet__"></span>**FEHLER \_ INTERNET\_\***
</dt> <dd> <dl> <dt>

12000 bis 12175 (0x2EE0)
</dt> <dt>



Siehe [Internetfehlercodes](../wininet/wininet-errors.md) und WinInet.h.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_QM_POLICY_EXISTS"></span><span id="error_ipsec_qm_policy_exists"></span>**\_FEHLER: \_ IPSEC-QM-RICHTLINIE \_ \_ VORHANDEN**
</dt> <dd> <dl> <dt>

13000 (0x32C8)
</dt> <dt>



Die angegebene Schnellmodusrichtlinie ist bereits vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_QM_POLICY_NOT_FOUND"></span><span id="error_ipsec_qm_policy_not_found"></span>**\_FEHLER: \_ IPSEC-QM-RICHTLINIE \_ \_ NICHT \_ GEFUNDEN**
</dt> <dd> <dl> <dt>

13001 (0x32C9)
</dt> <dt>



Die angegebene Schnellmodusrichtlinie wurde nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_QM_POLICY_IN_USE"></span><span id="error_ipsec_qm_policy_in_use"></span>**FEHLER BEI VERWENDUNG DER \_ \_ IPSEC-QM-RICHTLINIE \_ \_ \_**
</dt> <dd> <dl> <dt>

13002 (0x32CA)
</dt> <dt>



Die angegebene Schnellmodusrichtlinie wird verwendet.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_MM_POLICY_EXISTS"></span><span id="error_ipsec_mm_policy_exists"></span>**\_FEHLER: \_ IPSEC-MM-RICHTLINIE \_ \_ VORHANDEN**
</dt> <dd> <dl> <dt>

13003 (0x32CB)
</dt> <dt>



Die angegebene Richtlinie für den Hauptmodus ist bereits vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_MM_POLICY_NOT_FOUND"></span><span id="error_ipsec_mm_policy_not_found"></span>**FEHLER \_ IPSEC \_ \_ MM-RICHTLINIE \_ NICHT \_ GEFUNDEN**
</dt> <dd> <dl> <dt>

13004 (0x32CC)
</dt> <dt>



Die angegebene Richtlinie für den Hauptmodus wurde nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_MM_POLICY_IN_USE"></span><span id="error_ipsec_mm_policy_in_use"></span>**FEHLER \_ BEI VERWENDUNG DER IPSEC-MM-RICHTLINIE \_ \_ \_ \_**
</dt> <dd> <dl> <dt>

13005 (0x32CD)
</dt> <dt>



Die angegebene Richtlinie für den Hauptmodus wird verwendet.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_MM_FILTER_EXISTS"></span><span id="error_ipsec_mm_filter_exists"></span>**\_FEHLER: \_ IPSEC-MM-FILTER \_ \_ VORHANDEN**
</dt> <dd> <dl> <dt>

13006 (0x32CE)
</dt> <dt>



Der angegebene Hauptmodusfilter ist bereits vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_MM_FILTER_NOT_FOUND"></span><span id="error_ipsec_mm_filter_not_found"></span>**FEHLER \_ IPSEC \_ \_ MM-FILTER \_ NICHT \_ GEFUNDEN**
</dt> <dd> <dl> <dt>

13007 (0x32CF)
</dt> <dt>



Der angegebene Hauptmodusfilter wurde nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_TRANSPORT_FILTER_EXISTS"></span><span id="error_ipsec_transport_filter_exists"></span>**\_FEHLER: \_ IPSEC-TRANSPORTFILTER \_ \_ VORHANDEN**
</dt> <dd> <dl> <dt>

13008 (0x32D0)
</dt> <dt>



Der angegebene Transportmodusfilter ist bereits vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_TRANSPORT_FILTER_NOT_FOUND"></span><span id="error_ipsec_transport_filter_not_found"></span>**FEHLER \_ \_ IPSEC-TRANSPORTFILTER \_ \_ NICHT \_ GEFUNDEN**
</dt> <dd> <dl> <dt>

13009 (0x32D1)
</dt> <dt>



Der angegebene Transportmodusfilter ist nicht vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_MM_AUTH_EXISTS"></span><span id="error_ipsec_mm_auth_exists"></span>**FEHLER \_ IPSEC \_ MM \_ AUTH \_ EXISTS**
</dt> <dd> <dl> <dt>

13010 (0x32D2)
</dt> <dt>



Die angegebene Authentifizierungsliste im Hauptmodus ist vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_MM_AUTH_NOT_FOUND"></span><span id="error_ipsec_mm_auth_not_found"></span>**FEHLER \_ IPSEC \_ \_ MM-AUTHENTIFIZIERUNG \_ NICHT \_ GEFUNDEN**
</dt> <dd> <dl> <dt>

13011 (0x32D3)
</dt> <dt>



Die angegebene Authentifizierungsliste im Hauptmodus wurde nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_MM_AUTH_IN_USE"></span><span id="error_ipsec_mm_auth_in_use"></span>**FEHLER BEI VERWENDUNG DER \_ IPSEC \_ \_ MM-AUTHENTIFIZIERUNG \_ \_**
</dt> <dd> <dl> <dt>

13012 (0x32D4)
</dt> <dt>



Die angegebene Authentifizierungsliste im Hauptmodus wird verwendet.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_DEFAULT_MM_POLICY_NOT_FOUND"></span><span id="error_ipsec_default_mm_policy_not_found"></span>**FEHLER \_ \_ IPSEC-STANDARD-MM-RICHTLINIE \_ \_ NICHT \_ \_ GEFUNDEN**
</dt> <dd> <dl> <dt>

13013 (0x32D5)
</dt> <dt>



Die angegebene Standardrichtlinie für den Hauptmodus wurde nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_DEFAULT_MM_AUTH_NOT_FOUND"></span><span id="error_ipsec_default_mm_auth_not_found"></span>**FEHLER \_ \_ IPSEC-STANDARD-MM-AUTHENTIFIZIERUNG \_ \_ NICHT \_ \_ GEFUNDEN**
</dt> <dd> <dl> <dt>

13014 (0x32D6)
</dt> <dt>



Die angegebene Standardauthentifizierungsliste für den Hauptmodus wurde nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_DEFAULT_QM_POLICY_NOT_FOUND"></span><span id="error_ipsec_default_qm_policy_not_found"></span>**\_FEHLER: \_ IPSEC-STANDARD-QM-RICHTLINIE \_ \_ NICHT \_ \_ GEFUNDEN**
</dt> <dd> <dl> <dt>

13015 (0x32D7)
</dt> <dt>



Die angegebene Standardrichtlinie für den Schnellmodus wurde nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_TUNNEL_FILTER_EXISTS"></span><span id="error_ipsec_tunnel_filter_exists"></span>**\_FEHLER: \_ IPSEC-TUNNELFILTER \_ \_ VORHANDEN**
</dt> <dd> <dl> <dt>

13016 (0x32D8)
</dt> <dt>



Der angegebene Tunnelmodusfilter ist vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_TUNNEL_FILTER_NOT_FOUND"></span><span id="error_ipsec_tunnel_filter_not_found"></span>**FEHLER \_ \_ IPSEC-TUNNELFILTER NICHT \_ \_ \_ GEFUNDEN**
</dt> <dd> <dl> <dt>

13017 (0x32D9)
</dt> <dt>



Der angegebene Tunnelmodusfilter wurde nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_MM_FILTER_PENDING_DELETION"></span><span id="error_ipsec_mm_filter_pending_deletion"></span>**FEHLER \_ BEIM LÖSCHEN DES IPSEC-MM-FILTERS \_ \_ \_ \_**
</dt> <dd> <dl> <dt>

13018 (0x32DA)
</dt> <dt>



Für den Filter Hauptmodus steht das Löschen aus.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_TRANSPORT_FILTER_PENDING_DELETION"></span><span id="error_ipsec_transport_filter_pending_deletion"></span>**FEHLER \_ BEIM LÖSCHEN DES IPSEC-TRANSPORTFILTERS \_ \_ \_ \_**
</dt> <dd> <dl> <dt>

13019 (0x32DB)
</dt> <dt>



Das Löschen des Transportfilters steht aus.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_TUNNEL_FILTER_PENDING_DELETION"></span><span id="error_ipsec_tunnel_filter_pending_deletion"></span>**FEHLER BEIM LÖSCHEN \_ DES IPSEC-TUNNELFILTERS \_ \_ \_ \_**
</dt> <dd> <dl> <dt>

13020 (0x32DC)
</dt> <dt>



Das Löschen des Tunnelfilters steht aus.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_MM_POLICY_PENDING_DELETION"></span><span id="error_ipsec_mm_policy_pending_deletion"></span>**FEHLER \_ IPSEC \_ \_ MM-RICHTLINIE \_ – LÖSCHEN AUSSTEHEND \_**
</dt> <dd> <dl> <dt>

13021 (0x32DD)
</dt> <dt>



Das Löschen der Richtlinie für den Hauptmodus steht aus.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_MM_AUTH_PENDING_DELETION"></span><span id="error_ipsec_mm_auth_pending_deletion"></span>**FEHLER BEIM LÖSCHEN DER \_ IPSEC \_ \_ MM-AUTHENTIFIZIERUNG \_ \_**
</dt> <dd> <dl> <dt>

13022 (0x32DE)
</dt> <dt>



Das Hauptmodus-Authentifizierungspaket steht vor dem Löschen.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_QM_POLICY_PENDING_DELETION"></span><span id="error_ipsec_qm_policy_pending_deletion"></span>**FEHLER \_ IPSEC \_ QM POLICY \_ \_ PENDING \_ DELETION**
</dt> <dd> <dl> <dt>

13023 (0x32DF)
</dt> <dt>



Das Löschen der Richtlinie für den Schnellmodus steht aus.


</dt> </dl> </dd> <dt>

<span id="WARNING_IPSEC_MM_POLICY_PRUNED"></span><span id="warning_ipsec_mm_policy_pruned"></span>**WARNUNG \_ IPSEC \_ MM POLICY \_ \_ PRUNED**
</dt> <dd> <dl> <dt>

13024 (0x32E0)
</dt> <dt>



Die Richtlinie für den Hauptmodus wurde erfolgreich hinzugefügt, einige der angeforderten Angebote werden jedoch nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="WARNING_IPSEC_QM_POLICY_PRUNED"></span><span id="warning_ipsec_qm_policy_pruned"></span>**WARNUNG \_ IPSEC \_ QM POLICY \_ \_ PRUNED**
</dt> <dd> <dl> <dt>

13025 (0x32E1)
</dt> <dt>



Die Richtlinie für den Schnellmodus wurde erfolgreich hinzugefügt, einige der angeforderten Angebote werden jedoch nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_NEG_STATUS_BEGIN"></span><span id="error_ipsec_ike_neg_status_begin"></span>**ERROR \_ IPSEC \_ IKE \_ NEG \_ STATUS \_ BEGIN**
</dt> <dd> <dl> <dt>

13800 (0x35E8)
</dt> <dt>



ERROR \_ IPSEC \_ IKE \_ NEG \_ STATUS \_ BEGIN


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_AUTH_FAIL"></span><span id="error_ipsec_ike_auth_fail"></span>**FEHLER: FEHLER BEI \_ IPSEC-IKE-AUTHENTIFIZIERUNG \_ \_ \_**
</dt> <dd> <dl> <dt>

13801 (0x35E9)
</dt> <dt>



Anmeldeinformationen für die IKE-Authentifizierung sind nicht akzeptabel.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_ATTRIB_FAIL"></span><span id="error_ipsec_ike_attrib_fail"></span>**FEHLER \_ \_ IPSEC-IKE-ATTRIB-FEHLER \_ \_**
</dt> <dd> <dl> <dt>

13802 (0x35EA)
</dt> <dt>



IKE-Sicherheitsattribute sind nicht akzeptabel.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_NEGOTIATION_PENDING"></span><span id="error_ipsec_ike_negotiation_pending"></span>**FEHLER \_ \_ IPSEC-IKE-AUSHANDLUNG \_ \_ AUSSTEHEND**
</dt> <dd> <dl> <dt>

13803 (0x35EB)
</dt> <dt>



IKE-Aushandlung wird in Bearbeitung.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_GENERAL_PROCESSING_ERROR"></span><span id="error_ipsec_ike_general_processing_error"></span>**FEHLER: \_ ALLGEMEINER \_ IPSEC-IKE-VERARBEITUNGSFEHLER \_ \_ \_**
</dt> <dd> <dl> <dt>

13804 (0x35EC)
</dt> <dt>



Allgemeiner Verarbeitungsfehler.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_TIMED_OUT"></span><span id="error_ipsec_ike_timed_out"></span>**\_FEHLER: \_ IPSEC-IKE-TIME \_ \_ OUT**
</dt> <dd> <dl> <dt>

13805 (0x35ED)
</dt> <dt>



Time out der Aushandlung.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_NO_CERT"></span><span id="error_ipsec_ike_no_cert"></span>**FEHLER: \_ IPSEC \_ IKE \_ NO \_ CERT**
</dt> <dd> <dl> <dt>

13806 (0x35EE)
</dt> <dt>



IKE konnte das gültige Computerzertifikat nicht finden. Wenden Sie sich an Ihren Netzwerksicherheitsadministrator, um ein gültiges Zertifikat in der entsprechenden Zertifikatsverwaltung Store.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_SA_DELETED"></span><span id="error_ipsec_ike_sa_deleted"></span>**\_FEHLER: \_ IPSEC-IKE-SA \_ \_ GELÖSCHT**
</dt> <dd> <dl> <dt>

13807 (0x35EF)
</dt> <dt>



IKE SA wurde nach Peer gelöscht, bevor die Einrichtung abgeschlossen wurde.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_SA_REAPED"></span><span id="error_ipsec_ike_sa_reaped"></span>**\_FEHLER: \_ IPSEC-IKE-SA \_ WURDE ERNEUT \_ VERWENDET**
</dt> <dd> <dl> <dt>

13808 (0x35F0)
</dt> <dt>



IKE SA wurde vor Abschluss der Einrichtung gelöscht.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_MM_ACQUIRE_DROP"></span><span id="error_ipsec_ike_mm_acquire_drop"></span>**FEHLER: \_ IPSEC \_ IKE \_ MM ACQUIRE \_ \_ DROP**
</dt> <dd> <dl> <dt>

13809 (0x35F1)
</dt> <dt>



Die Aushandlungsanforderung wurde zu lange in der Warteschlange gespeichert.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_QM_ACQUIRE_DROP"></span><span id="error_ipsec_ike_qm_acquire_drop"></span>**FEHLER: \_ IPSEC \_ IKE \_ QM ACQUIRE \_ \_ DROP**
</dt> <dd> <dl> <dt>

13810 (0x35F2)
</dt> <dt>



Die Aushandlungsanforderung wurde zu lange in der Warteschlange gespeichert.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_QUEUE_DROP_MM"></span><span id="error_ipsec_ike_queue_drop_mm"></span>**FEHLER: \_ IPSEC \_ IKE QUEUE \_ DROP \_ \_ MM**
</dt> <dd> <dl> <dt>

13811 (0x35F3)
</dt> <dt>



Die Aushandlungsanforderung wurde zu lange in der Warteschlange gespeichert.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_QUEUE_DROP_NO_MM"></span><span id="error_ipsec_ike_queue_drop_no_mm"></span>**FEHLER: \_ LÖSCHEN DER \_ IPSEC-IKE-WARTESCHLANGE \_ \_ OHNE \_ \_ MM**
</dt> <dd> <dl> <dt>

13812 (0x35F4)
</dt> <dt>



Die Aushandlungsanforderung wurde zu lange in der Warteschlange gespeichert.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_DROP_NO_RESPONSE"></span><span id="error_ipsec_ike_drop_no_response"></span>**FEHLER \_ IPSEC \_ IKE \_ DROP NO \_ \_ RESPONSE**
</dt> <dd> <dl> <dt>

13813 (0x35F5)
</dt> <dt>



Keine Antwort vom Peer.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_MM_DELAY_DROP"></span><span id="error_ipsec_ike_mm_delay_drop"></span>**FEHLER: \_ IPSEC \_ IKE \_ MM DELAY \_ \_ DROP**
</dt> <dd> <dl> <dt>

13814 (0x35F6)
</dt> <dt>



Die Aushandlung hat zu lange ge dauern.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_QM_DELAY_DROP"></span><span id="error_ipsec_ike_qm_delay_drop"></span>**FEHLER: \_ IPSEC \_ IKE \_ QM DELAY \_ \_ DROP**
</dt> <dd> <dl> <dt>

13815 (0x35F7)
</dt> <dt>



Die Aushandlung hat zu lange ge dauern.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_ERROR"></span><span id="error_ipsec_ike_error"></span>**\_FEHLER: \_ IPSEC-IKE-FEHLER \_**
</dt> <dd> <dl> <dt>

13816 (0x35F8)
</dt> <dt>



Unbekannter Fehler.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_CRL_FAILED"></span><span id="error_ipsec_ike_crl_failed"></span>**FEHLER: \_ FEHLER BEI DER \_ IPSEC-IKE-ZERTIFIKATSPERRLISTE \_ \_**
</dt> <dd> <dl> <dt>

13817 (0x35F9)
</dt> <dt>



Fehler bei der Zertifikatsperrprüfung.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_KEY_USAGE"></span><span id="error_ipsec_ike_invalid_key_usage"></span>**FEHLER: \_ UNGÜLTIGE \_ IPSEC-IKE-SCHLÜSSELVERWENDUNG \_ \_ \_**
</dt> <dd> <dl> <dt>

13818 (0x35FA)
</dt> <dt>



Ungültige Zertifikatschlüsselverwendung.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_CERT_TYPE"></span><span id="error_ipsec_ike_invalid_cert_type"></span>**FEHLER: \_ UNGÜLTIGER \_ \_ \_ IPSEC-IKE-ZERTIFIKATTYP \_**
</dt> <dd> <dl> <dt>

13819 (0x35FB)
</dt> <dt>



Ungültiger Zertifikattyp.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_NO_PRIVATE_KEY"></span><span id="error_ipsec_ike_no_private_key"></span>**\_FEHLER: \_ IPSEC-IKE \_ KEIN PRIVATER \_ \_ SCHLÜSSEL**
</dt> <dd> <dl> <dt>

13820 (0x35FC)
</dt> <dt>



Fehler bei der IKE-Aushandlung, weil das verwendete Computerzertifikat über keinen privaten Schlüssel verfügt. IPsec-Zertifikate erfordern einen privaten Schlüssel. Wenden Sie sich an Sicherheitsadministrator, um durch ein Zertifikat mit einem privaten Schlüssel zu ersetzen.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_SIMULTANEOUS_REKEY"></span><span id="error_ipsec_ike_simultaneous_rekey"></span>**FEHLER: \_ IPSEC \_ IKE \_ – \_ GLEICHZEITIGER ERNEUTER SCHLÜSSEL**
</dt> <dd> <dl> <dt>

13821 (0x35FD)
</dt> <dt>



Gleichzeitige Neuschlüssel wurden erkannt.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_DH_FAIL"></span><span id="error_ipsec_ike_dh_fail"></span>**FEHLER: \_ IPSEC \_ IKE \_ DH \_ FAIL**
</dt> <dd> <dl> <dt>

13822 (0x35FE)
</dt> <dt>



Fehler bei Diffie-Hellman Berechnung.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_CRITICAL_PAYLOAD_NOT_RECOGNIZED"></span><span id="error_ipsec_ike_critical_payload_not_recognized"></span>**FEHLER: \_ KRITISCHE \_ IPSEC-IKE-NUTZLAST \_ \_ NICHT \_ \_ ERKANNT**
</dt> <dd> <dl> <dt>

13823 (0x35FF)
</dt> <dt>



Sie wissen nicht, wie kritische Nutzlasten zu verarbeiten sind.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_HEADER"></span><span id="error_ipsec_ike_invalid_header"></span>**FEHLER: \_ UNGÜLTIGER \_ IPSEC-IKE-HEADER \_ \_**
</dt> <dd> <dl> <dt>

13824 (0x3600)
</dt> <dt>



Ungültiger Header.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_NO_POLICY"></span><span id="error_ipsec_ike_no_policy"></span>**\_FEHLER: \_ IPSEC-IKE \_ KEINE \_ RICHTLINIE**
</dt> <dd> <dl> <dt>

13825 (0x3601)
</dt> <dt>



Es wurde keine Richtlinie konfiguriert.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_SIGNATURE"></span><span id="error_ipsec_ike_invalid_signature"></span>**FEHLER: \_ UNGÜLTIGE \_ IPSEC-IKE-SIGNATUR \_ \_**
</dt> <dd> <dl> <dt>

13826 (0x3602)
</dt> <dt>



Fehler beim Überprüfen der Signatur.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_KERBEROS_ERROR"></span><span id="error_ipsec_ike_kerberos_error"></span>**\_FEHLER: \_ IPSEC-IKE-KERBEROS-FEHLER \_ \_**
</dt> <dd> <dl> <dt>

13827 (0x3603)
</dt> <dt>



Fehler beim Authentifizieren mit Kerberos.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_NO_PUBLIC_KEY"></span><span id="error_ipsec_ike_no_public_key"></span>**\_FEHLER: \_ IPSEC-IKE \_ KEIN ÖFFENTLICHER \_ \_ SCHLÜSSEL**
</dt> <dd> <dl> <dt>

13828 (0x3604)
</dt> <dt>



Das Zertifikat des Peers hat keinen öffentlichen Schlüssel.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR"></span><span id="error_ipsec_ike_process_err"></span>**\_FEHLER: \_ IPSEC-IKE-PROZESS \_ \_ ERR**
</dt> <dd> <dl> <dt>

13829 (0x3605)
</dt> <dt>



Fehlerverarbeitungsfehlernutzlast.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_SA"></span><span id="error_ipsec_ike_process_err_sa"></span>**\_FEHLER: \_ IPSEC-IKE-PROZESS \_ \_ ERR \_ SA**
</dt> <dd> <dl> <dt>

13830 (0x3606)
</dt> <dt>



Fehler beim Verarbeiten der SA-Nutzlast.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_PROP"></span><span id="error_ipsec_ike_process_err_prop"></span>**\_FEHLER: \_ IPSEC-IKE-PROZESS \_ \_ ERR \_ PROP**
</dt> <dd> <dl> <dt>

13831 (0x3607)
</dt> <dt>



Fehlerverarbeitung: Vorschlagsnutzlast.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_TRANS"></span><span id="error_ipsec_ike_process_err_trans"></span>**FEHLER: \_ IPSEC \_ IKE \_ PROCESS \_ ERR \_ TRANS**
</dt> <dd> <dl> <dt>

13832 (0x3608)
</dt> <dt>



Fehler beim Verarbeiten der Transformationsnutzlast.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_KE"></span><span id="error_ipsec_ike_process_err_ke"></span>**\_FEHLER: \_ IPSEC-IKE-PROZESS \_ \_ ERR \_ KE**
</dt> <dd> <dl> <dt>

13833 (0x3609)
</dt> <dt>



Fehler beim Verarbeiten der KE-Nutzlast.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_ID"></span><span id="error_ipsec_ike_process_err_id"></span>**\_FEHLER: \_ IPSEC-IKE-PROZESS- \_ \_ ERR-ID \_**
</dt> <dd> <dl> <dt>

13834 (0x360A)
</dt> <dt>



Fehler bei der Verarbeitung der ID-Nutzlast.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_CERT"></span><span id="error_ipsec_ike_process_err_cert"></span>**\_FEHLER: \_ IPSEC-IKE-PROZESS \_ \_ – \_ ERR-ZERTIFIKAT**
</dt> <dd> <dl> <dt>

13835 (0x360B)
</dt> <dt>



Fehler beim Verarbeiten der Zertifikatnutzlast.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_CERT_REQ"></span><span id="error_ipsec_ike_process_err_cert_req"></span>**FEHLER: \_ IPSEC \_ IKE \_ PROCESS \_ ERR \_ CERT \_ REQ**
</dt> <dd> <dl> <dt>

13836 (0x360C)
</dt> <dt>



Fehler beim Verarbeiten der Zertifikatanforderungsnutzlast.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_HASH"></span><span id="error_ipsec_ike_process_err_hash"></span>**\_FEHLER: \_ IPSEC-IKE-PROZESS \_ \_ – ERR-HASH \_**
</dt> <dd> <dl> <dt>

13837 (0x360D)
</dt> <dt>



Fehler beim Verarbeiten der Hashnutzlast.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_SIG"></span><span id="error_ipsec_ike_process_err_sig"></span>**FEHLER: \_ IPSEC \_ IKE \_ PROCESS \_ ERR \_ SIG**
</dt> <dd> <dl> <dt>

13838 (0x360E)
</dt> <dt>



Fehler beim Verarbeiten der Signaturnutzlast.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_NONCE"></span><span id="error_ipsec_ike_process_err_nonce"></span>**\_FEHLER: \_ IPSEC-IKE-PROZESS \_ \_ ERR \_ NONCE**
</dt> <dd> <dl> <dt>

13839 (0x360F)
</dt> <dt>



Fehler beim Verarbeiten der Nonce-Nutzlast.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_NOTIFY"></span><span id="error_ipsec_ike_process_err_notify"></span>**\_FEHLER: \_ IPSEC-IKE-PROZESS \_ \_ : ERR-BENACHRICHTIGUNG \_**
</dt> <dd> <dl> <dt>

13840 (0x3610)
</dt> <dt>



Fehlerverarbeitung Benachrichtigungsnutzlast.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_DELETE"></span><span id="error_ipsec_ike_process_err_delete"></span>**FEHLER \_ BEIM LÖSCHEN DES IPSEC-IKE-PROZESSES \_ \_ \_ \_**
</dt> <dd> <dl> <dt>

13841 (0x3611)
</dt> <dt>



Fehler beim Verarbeiten der Löschnutzlast.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_VENDOR"></span><span id="error_ipsec_ike_process_err_vendor"></span>**FEHLER: \_ ANBIETER DES \_ IPSEC-IKE-PROZESSES \_ \_ \_**
</dt> <dd> <dl> <dt>

13842 (0x3612)
</dt> <dt>



Fehler beim Verarbeiten der VendorId-Nutzlast.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_PAYLOAD"></span><span id="error_ipsec_ike_invalid_payload"></span>**FEHLER: \_ UNGÜLTIGE \_ IPSEC-IKE-NUTZLAST \_ \_**
</dt> <dd> <dl> <dt>

13843 (0x3613)
</dt> <dt>



Ungültige Nutzlast empfangen.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_LOAD_SOFT_SA"></span><span id="error_ipsec_ike_load_soft_sa"></span>**FEHLER: \_ IPSEC \_ IKE \_ LOAD SOFT \_ \_ SA**
</dt> <dd> <dl> <dt>

13844 (0x3614)
</dt> <dt>



Soft SA geladen.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_SOFT_SA_TORN_DOWN"></span><span id="error_ipsec_ike_soft_sa_torn_down"></span>**FEHLER: \_ IPSEC \_ IKE \_ SOFT SA \_ \_ TORN \_ DOWN**
</dt> <dd> <dl> <dt>

13845 (0x3615)
</dt> <dt>



Soft SA torn down.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_COOKIE"></span><span id="error_ipsec_ike_invalid_cookie"></span>**FEHLER: \_ UNGÜLTIGES \_ IPSEC-IKE-COOKIE \_ \_**
</dt> <dd> <dl> <dt>

13846 (0x3616)
</dt> <dt>



Ungültiges Cookie empfangen.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_NO_PEER_CERT"></span><span id="error_ipsec_ike_no_peer_cert"></span>**FEHLER: \_ IPSEC \_ IKE \_ NO PEER \_ \_ CERT**
</dt> <dd> <dl> <dt>

13847 (0x3617)
</dt> <dt>



Fehler beim Senden eines gültigen Computerzertifikats durch den Peer.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PEER_CRL_FAILED"></span><span id="error_ipsec_ike_peer_crl_failed"></span>**FEHLER: \_ FEHLER BEI DER \_ IPSEC-IKE-PEER-ZERTIFIKATSPERRLISTE \_ \_ \_**
</dt> <dd> <dl> <dt>

13848 (0x3618)
</dt> <dt>



Fehler bei der Überprüfung der Zertifizierungssperrung des Peerzertifikats.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_POLICY_CHANGE"></span><span id="error_ipsec_ike_policy_change"></span>**\_FEHLER: \_ IPSEC-IKE-RICHTLINIENÄNDERUNG \_ \_**
</dt> <dd> <dl> <dt>

13849 (0x3619)
</dt> <dt>



Neue Richtlinie hat SAs ungültig gemacht, die mit der alten Richtlinie gebildet wurden.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_NO_MM_POLICY"></span><span id="error_ipsec_ike_no_mm_policy"></span>**FEHLER: \_ IPSEC \_ IKE \_ NO MM \_ \_ POLICY**
</dt> <dd> <dl> <dt>

13850 (0x361A)
</dt> <dt>



Es ist keine IKE-Richtlinie für den Hauptmodus verfügbar.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_NOTCBPRIV"></span><span id="error_ipsec_ike_notcbpriv"></span>**FEHLER: \_ IPSEC \_ IKE \_ NOTCBPRIV**
</dt> <dd> <dl> <dt>

13851 (0x361B)
</dt> <dt>



Fehler beim Aktivieren der TCB-Berechtigung.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_SECLOADFAIL"></span><span id="error_ipsec_ike_secloadfail"></span>**FEHLER: \_ IPSEC \_ IKE \_ SECLOADFAIL**
</dt> <dd> <dl> <dt>

13852 (0x361C)
</dt> <dt>



Fehler beim Laden SECURITY.DLL.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_FAILSSPINIT"></span><span id="error_ipsec_ike_failsspinit"></span>**\_FEHLER: \_ IPSEC-IKE \_ SCHLÄGT FEHLSPINIT**
</dt> <dd> <dl> <dt>

13853 (0x361D)
</dt> <dt>



Fehler beim Abrufen der Dispatchadresse der Sicherheitsfunktionstabelle aus SSPI.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_FAILQUERYSSP"></span><span id="error_ipsec_ike_failqueryssp"></span>**FEHLER: \_ IPSEC \_ IKE \_ FAILQUERYSSP**
</dt> <dd> <dl> <dt>

13854 (0x361E)
</dt> <dt>



Fehler beim Abfragen des Kerberos-Pakets zum Abrufen der maximalen Tokengröße.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_SRVACQFAIL"></span><span id="error_ipsec_ike_srvacqfail"></span>**\_FEHLER: \_ IPSEC-IKE \_ SRVACQFAIL**
</dt> <dd> <dl> <dt>

13855 (0x361F)
</dt> <dt>



Fehler beim Abrufen der Kerberos-Serveranmeldeinformationen für den \_ ISAKMP/ERROR-IPSEC-IKE-Dienst. \_ Die Kerberos-Authentifizierung funktioniert nicht. Der wahrscheinlichste Grund dafür ist die fehlende Domänenmitgliedschaft. Dies ist normal, wenn Ihr Computer Mitglied einer Arbeitsgruppe ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_SRVQUERYCRED"></span><span id="error_ipsec_ike_srvquerycred"></span>**FEHLER: \_ IPSEC \_ IKE \_ SRVQUERYCRED**
</dt> <dd> <dl> <dt>

13856 (0x3620)
</dt> <dt>



Fehler beim Ermitteln des SSPI-Prinzipalnamens für den \_ ISAKMP/ERROR-IPSEC-IKE-Dienst \_ ([**QueryCredentialsAttributes**](/windows/win32/api/sspi/nf-sspi-querycredentialsattributesa)).


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_GETSPIFAIL"></span><span id="error_ipsec_ike_getspifail"></span>**FEHLER: \_ IPSEC \_ IKE \_ GETSPIFAIL**
</dt> <dd> <dl> <dt>

13857 (0x3621)
</dt> <dt>



Fehler beim Abrufen der neuen SPI für die eingehende SA vom IPsec-Treiber. Die häufigste Ursache dafür ist, dass der Treiber nicht über den richtigen Filter verfügt. Überprüfen Sie Ihre Richtlinie, um die Filter zu überprüfen.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_FILTER"></span><span id="error_ipsec_ike_invalid_filter"></span>**FEHLER: \_ UNGÜLTIGER \_ IPSEC-IKE-FILTER \_ \_**
</dt> <dd> <dl> <dt>

13858 (0x3622)
</dt> <dt>



Der gegebene Filter ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_OUT_OF_MEMORY"></span><span id="error_ipsec_ike_out_of_memory"></span>**\_FEHLER: \_ IPSEC-IKE \_ NICHT GENÜGEND \_ \_ ARBEITSSPEICHER**
</dt> <dd> <dl> <dt>

13859 (0x3623)
</dt> <dt>



Die Speicherbelegung hat einen Fehler erzeugt.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_ADD_UPDATE_KEY_FAILED"></span><span id="error_ipsec_ike_add_update_key_failed"></span>**FEHLER: FEHLER BEIM HINZUFÜGEN DES \_ AKTUALISIERUNGSSCHLÜSSELS DURCH IPSEC \_ IKE \_ \_ \_ \_**
</dt> <dd> <dl> <dt>

13860 (0x3624)
</dt> <dt>



Fehler beim Hinzufügen der Sicherheits association zum IPsec-Treiber. Die häufigste Ursache dafür ist, dass die IKE-Aushandlung zu lange ge dauerte. Wenn das Problem weiterhin besteht, verringern Sie die Last auf dem fehlerhaften Computer.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_POLICY"></span><span id="error_ipsec_ike_invalid_policy"></span>**\_FEHLER: \_ IPSEC-IKE \_ UNGÜLTIGE \_ RICHTLINIE**
</dt> <dd> <dl> <dt>

13861 (0x3625)
</dt> <dt>



Ungültige Richtlinie.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_UNKNOWN_DOI"></span><span id="error_ipsec_ike_unknown_doi"></span>**FEHLER: \_ IPSEC \_ IKE \_ UNKNOWN \_ DOI**
</dt> <dd> <dl> <dt>

13862 (0x3626)
</dt> <dt>



Ungültige DOI.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_SITUATION"></span><span id="error_ipsec_ike_invalid_situation"></span>**FEHLER: \_ UNGÜLTIGE \_ IPSEC-IKE-SITUATION \_ \_**
</dt> <dd> <dl> <dt>

13863 (0x3627)
</dt> <dt>



Ungültige Situation.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_DH_FAILURE"></span><span id="error_ipsec_ike_dh_failure"></span>**\_FEHLER: \_ IPSEC-IKE \_ \_ DH-FEHLER**
</dt> <dd> <dl> <dt>

13864 (0x3628)
</dt> <dt>



Diffie-Hellman fehler.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_GROUP"></span><span id="error_ipsec_ike_invalid_group"></span>**\_FEHLER: \_ IPSEC-IKE \_ UNGÜLTIGE \_ GRUPPE**
</dt> <dd> <dl> <dt>

13865 (0x3629)
</dt> <dt>



Ungültige Diffie-Hellman Gruppe.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_ENCRYPT"></span><span id="error_ipsec_ike_encrypt"></span>**FEHLER: \_ IPSEC \_ IKE \_ ENCRYPT**
</dt> <dd> <dl> <dt>

13866 (0x362A)
</dt> <dt>



Fehler beim Verschlüsseln der Nutzlast.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_DECRYPT"></span><span id="error_ipsec_ike_decrypt"></span>**\_FEHLER: \_ IPSEC-IKE-ENTSCHLÜSSELUNG \_**
</dt> <dd> <dl> <dt>

13867 (0x362B)
</dt> <dt>



Fehler beim Entschlüsseln der Nutzlast.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_POLICY_MATCH"></span><span id="error_ipsec_ike_policy_match"></span>**FEHLER: \_ ÜBEREINSTIMMUNG MIT \_ IPSEC-IKE-RICHTLINIE \_ \_**
</dt> <dd> <dl> <dt>

13868 (0x362C)
</dt> <dt>



Richtlinien-Übereinstimmungsfehler.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_UNSUPPORTED_ID"></span><span id="error_ipsec_ike_unsupported_id"></span>**FEHLER: \_ NICHT UNTERSTÜTZTE \_ IPSEC-IKE-ID \_ \_**
</dt> <dd> <dl> <dt>

13869 (0x362D)
</dt> <dt>



Nicht unterstützte ID.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_HASH"></span><span id="error_ipsec_ike_invalid_hash"></span>**FEHLER: \_ UNGÜLTIGER \_ IPSEC-IKE-HASH \_ \_**
</dt> <dd> <dl> <dt>

13870 (0x362E)
</dt> <dt>



Fehler bei der Hashüberprüfung.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_HASH_ALG"></span><span id="error_ipsec_ike_invalid_hash_alg"></span>**FEHLER: \_ IPSEC \_ IKE \_ INVALID HASH \_ \_ ALG**
</dt> <dd> <dl> <dt>

13871 (0x362F)
</dt> <dt>



Ungültiger Hashalgorithmus.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_HASH_SIZE"></span><span id="error_ipsec_ike_invalid_hash_size"></span>**FEHLER: \_ UNGÜLTIGE \_ IPSEC-IKE-HASHGRÖßE \_ \_ \_**
</dt> <dd> <dl> <dt>

13872 (0x3630)
</dt> <dt>



Ungültige Hashgröße.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_ENCRYPT_ALG"></span><span id="error_ipsec_ike_invalid_encrypt_alg"></span>**FEHLER: \_ IPSEC \_ IKE INVALID \_ ENCRYPT \_ \_ ALG**
</dt> <dd> <dl> <dt>

13873 (0x3631)
</dt> <dt>



Ungültiger Verschlüsselungsalgorithmus.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_AUTH_ALG"></span><span id="error_ipsec_ike_invalid_auth_alg"></span>**FEHLER: \_ IPSEC \_ IKE \_ INVALID \_ AUTH \_ ALG**
</dt> <dd> <dl> <dt>

13874 (0x3632)
</dt> <dt>



Ungültiger Authentifizierungsalgorithmus.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_SIG"></span><span id="error_ipsec_ike_invalid_sig"></span>**FEHLER: \_ IPSEC \_ IKE INVALID \_ \_ SIG**
</dt> <dd> <dl> <dt>

13875 (0x3633)
</dt> <dt>



Ungültige Zertifikatsignatur.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_LOAD_FAILED"></span><span id="error_ipsec_ike_load_failed"></span>**FEHLER BEIM \_ \_ IPSEC-IKE-LADEFEHLER \_ \_**
</dt> <dd> <dl> <dt>

13876 (0x3634)
</dt> <dt>



Fehler beim Laden.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_RPC_DELETE"></span><span id="error_ipsec_ike_rpc_delete"></span>**FEHLER: \_ IPSEC \_ IKE \_ RPC \_ DELETE**
</dt> <dd> <dl> <dt>

13877 (0x3635)
</dt> <dt>



Wurde per RPC-Aufruf gelöscht.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_BENIGN_REINIT"></span><span id="error_ipsec_ike_benign_reinit"></span>**FEHLER: \_ IPSEC \_ IKE \_ BENIGN \_ REINIT**
</dt> <dd> <dl> <dt>

13878 (0x3636)
</dt> <dt>



Temporärer Zustand, der erstellt wurde, um die Neuinialisierung durchzuführen. Dies ist kein echter Fehler.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_RESPONDER_LIFETIME_NOTIFY"></span><span id="error_ipsec_ike_invalid_responder_lifetime_notify"></span>**FEHLER \_ IPSEC \_ IKE \_ INVALID \_ RESPONDER LIFETIME \_ \_ NOTIFY**
</dt> <dd> <dl> <dt>

13879 (0x3637)
</dt> <dt>



Der wert für die Lebensdauer, der in Der Antwort-Benachrichtigung über die Lebensdauer empfangen wird, liegt unter dem Windows 2000 konfigurierten Mindestwert. Korrigieren Sie die Richtlinie auf dem Peercomputer.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_MAJOR_VERSION"></span><span id="error_ipsec_ike_invalid_major_version"></span>**FEHLER: \_ IPSEC \_ IKE \_ \_ UNGÜLTIGE \_ HAUPTVERSION**
</dt> <dd> <dl> <dt>

13880 (0x3638)
</dt> <dt>



Der Empfänger kann die im Header angegebene Version von IKE nicht verarbeiten.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_CERT_KEYLEN"></span><span id="error_ipsec_ike_invalid_cert_keylen"></span>**FEHLER: \_ IPSEC \_ IKE \_ INVALID \_ CERT \_ KEYLEN**
</dt> <dd> <dl> <dt>

13881 (0x3639)
</dt> <dt>



Die Schlüssellänge im Zertifikat ist für konfigurierte Sicherheitsanforderungen zu klein.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_MM_LIMIT"></span><span id="error_ipsec_ike_mm_limit"></span>**\_FEHLER: \_ IPSEC-IKE-MM-GRENZWERT \_ \_**
</dt> <dd> <dl> <dt>

13882 (0x363A)
</dt> <dt>



Die maximale Anzahl der eingerichteten MM-SAs für das Peering wurde überschritten.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_NEGOTIATION_DISABLED"></span><span id="error_ipsec_ike_negotiation_disabled"></span>**\_FEHLER: \_ IPSEC-IKE-AUSHANDLUNG \_ \_ DEAKTIVIERT**
</dt> <dd> <dl> <dt>

13883 (0x363B)
</dt> <dt>



IKE hat eine Richtlinie empfangen, die die Aushandlung deaktiviert.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_QM_LIMIT"></span><span id="error_ipsec_ike_qm_limit"></span>**\_FEHLER: \_ IPSEC-GRENZWERT FÜR IKE \_ QM \_**
</dt> <dd> <dl> <dt>

13884 (0x363C)
</dt> <dt>



Das maximale Limit für den Schnellmodus für den Hauptmodus wurde erreicht. Der neue Hauptmodus wird gestartet.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_MM_EXPIRED"></span><span id="error_ipsec_ike_mm_expired"></span>**FEHLER: \_ IPSEC \_ IKE \_ MM \_ ABGELAUFEN**
</dt> <dd> <dl> <dt>

13885 (0x363D)
</dt> <dt>



Die SA-Lebensdauer im Hauptmodus ist abgelaufen, oder der Peer hat einen Löschmodus im Hauptmodus gesendet.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PEER_MM_ASSUMED_INVALID"></span><span id="error_ipsec_ike_peer_mm_assumed_invalid"></span>**\_FEHLER: \_ IPSEC-IKE-PEER \_ MM WURDE ALS UNGÜLTIG \_ \_ \_ ANGENOMMEN**
</dt> <dd> <dl> <dt>

13886 (0x363E)
</dt> <dt>



Die Hauptmodus-SA wird als ungültig angesehen, da der Peer nicht mehr reagiert hat.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_CERT_CHAIN_POLICY_MISMATCH"></span><span id="error_ipsec_ike_cert_chain_policy_mismatch"></span>**\_FEHLER: \_ IPSEC-IKE-ZERTIFIKATKETTENRICHTLINIE \_ \_ NICHT \_ \_ ÜBEREINSTIMMEND**
</dt> <dd> <dl> <dt>

13887 (0x363F)
</dt> <dt>



Das Zertifikat wird nicht mit einem vertrauenswürdigen Stamm in der IPsec-Richtlinie verkettet.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_UNEXPECTED_MESSAGE_ID"></span><span id="error_ipsec_ike_unexpected_message_id"></span>**FEHLER: \_ UNERWARTETE \_ IPSEC-IKE-NACHRICHTEN-ID \_ \_ \_**
</dt> <dd> <dl> <dt>

13888 (0x3640)
</dt> <dt>



Unerwartete Nachrichten-ID empfangen.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_AUTH_PAYLOAD"></span><span id="error_ipsec_ike_invalid_auth_payload"></span>**\_FEHLER: \_ IPSEC-IKE \_ \_ UNGÜLTIGE AUTHENTIFIZIERUNGSNUTZLAST \_**
</dt> <dd> <dl> <dt>

13889 (0x3641)
</dt> <dt>



Ungültige Authentifizierungsangebote erhalten.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_DOS_COOKIE_SENT"></span><span id="error_ipsec_ike_dos_cookie_sent"></span>**\_FEHLER: \_ IPSEC-IKE-DOS-COOKIE \_ \_ \_ GESENDET**
</dt> <dd> <dl> <dt>

13890 (0x3642)
</dt> <dt>



DoS-Cookie an Initiator gesendet.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_SHUTTING_DOWN"></span><span id="error_ipsec_ike_shutting_down"></span>**\_FEHLER: \_ IPSEC-IKE \_ WIRD \_ HERUNTERGEFAHREN**
</dt> <dd> <dl> <dt>

13891 (0x3643)
</dt> <dt>



Der IKE-Dienst wird heruntergefahren.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_CGA_AUTH_FAILED"></span><span id="error_ipsec_ike_cga_auth_failed"></span>**FEHLER: \_ FEHLER BEI DER \_ IPSEC-IKE-CGA-AUTHENTIFIZIERUNG \_ \_ \_**
</dt> <dd> <dl> <dt>

13892 (0x3644)
</dt> <dt>



Die Bindung zwischen CGA-Adresse und Zertifikat konnte nicht überprüft werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_NATOA"></span><span id="error_ipsec_ike_process_err_natoa"></span>**\_FEHLER: \_ IPSEC-IKE-PROZESS \_ \_ ERR \_ -FEHLER**
</dt> <dd> <dl> <dt>

13893 (0x3645)
</dt> <dt>



Fehler beim Verarbeiten der NatOA-Nutzlast.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_MM_FOR_QM"></span><span id="error_ipsec_ike_invalid_mm_for_qm"></span>**FEHLER: \_ IPSEC \_ IKE \_ INVALID MM \_ FOR \_ \_ QM**
</dt> <dd> <dl> <dt>

13894 (0x3646)
</dt> <dt>



Parameter des Hauptmodus sind für diesen Schnellmodus ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_QM_EXPIRED"></span><span id="error_ipsec_ike_qm_expired"></span>**FEHLER: \_ IPSEC \_ IKE \_ QM IST \_ ABGELAUFEN**
</dt> <dd> <dl> <dt>

13895 (0x3647)
</dt> <dt>



Die Schnellmodus-SA ist vom IPsec-Treiber abgelaufen.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_TOO_MANY_FILTERS"></span><span id="error_ipsec_ike_too_many_filters"></span>**\_FEHLER: \_ IPSEC-IKE \_ ZU VIELE \_ \_ FILTER**
</dt> <dd> <dl> <dt>

13896 (0x3648)
</dt> <dt>



Es wurden zu viele dynamisch hinzugefügte IKEEXT-Filter erkannt.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_NEG_STATUS_END"></span><span id="error_ipsec_ike_neg_status_end"></span>**FEHLER: \_ ENDE DES \_ IPSEC-IKE-NEGSTATUS \_ \_ \_**
</dt> <dd> <dl> <dt>

13897 (0x3649)
</dt> <dt>



FEHLER: \_ ENDE DES \_ IPSEC-IKE-NEGSTATUS \_ \_ \_


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_KILL_DUMMY_NAP_TUNNEL"></span><span id="error_ipsec_ike_kill_dummy_nap_tunnel"></span>**FEHLER: \_ IPSEC \_ IKE \_ KILL \_ DUMMY \_ NAP \_ TUNNEL**
</dt> <dd> <dl> <dt>

13898 (0x364A)
</dt> <dt>



Die ERNEUTE NAP-Authentifizierung war erfolgreich und muss den Dummy-NAP-Tunnel IKEv2 löschen.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INNER_IP_ASSIGNMENT_FAILURE"></span><span id="error_ipsec_ike_inner_ip_assignment_failure"></span>**FEHLER: \_ FEHLER BEI DER \_ IPSEC-IKE-ZUWEISUNG \_ \_ DER INNEREN \_ \_ IP-ADRESSE**
</dt> <dd> <dl> <dt>

13899 (0x364B)
</dt> <dt>



Fehler beim Zuweisen der inneren IP-Adresse zum Initiator im Tunnelmodus.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_REQUIRE_CP_PAYLOAD_MISSING"></span><span id="error_ipsec_ike_require_cp_payload_missing"></span>**\_FEHLER: \_ IPSEC-IKE \_ ERFORDERT FEHLENDE \_ \_ \_ CP-NUTZLAST**
</dt> <dd> <dl> <dt>

13900 (0x364C)
</dt> <dt>



Konfigurationsnutzlast fehlt erforderlich.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_KEY_MODULE_IMPERSONATION_NEGOTIATION_PENDING"></span><span id="error_ipsec_key_module_impersonation_negotiation_pending"></span>**FEHLER \_ AUSSTEHEND DER IDENTITÄTSWECHSELAUSHANDLUNG DES \_ \_ \_ \_ IPSEC-SCHLÜSSELMODULS \_**
</dt> <dd> <dl> <dt>

13901 (0x364D)
</dt> <dt>



Eine Aushandlung, die als Sicherheitsprinzip ausgeführt wird, der die Verbindung ausgestellt hat, wird ausgeführt.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_COEXISTENCE_SUPPRESS"></span><span id="error_ipsec_ike_coexistence_suppress"></span>**\_FEHLER: \_ IPSEC-IKE-KOEXISTENZ \_ \_ UNTERDRÜCKEN**
</dt> <dd> <dl> <dt>

13902 (0x364E)
</dt> <dt>



SA wurde aufgrund einer Überprüfung der IKEv1/AuthIP-Koexistenz gelöscht.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_RATELIMIT_DROP"></span><span id="error_ipsec_ike_ratelimit_drop"></span>**\_FEHLER: \_ IPSEC-IKE-RATELIMIT-DROP \_ \_**
</dt> <dd> <dl> <dt>

13903 (0x364F)
</dt> <dt>



Eingehende SA-Anforderungen wurden aufgrund einer Peer-IP-Adressratenbegrenzung verworfen.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PEER_DOESNT_SUPPORT_MOBIKE"></span><span id="error_ipsec_ike_peer_doesnt_support_mobike"></span>**FEHLER: \_ DER \_ IPSEC-IKE-PEER \_ \_ UNTERSTÜTZT \_ \_ MOIKE NICHT.**
</dt> <dd> <dl> <dt>

13904 (0x3650)
</dt> <dt>



Der Peer unterstützt MOGUL nicht.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_AUTHORIZATION_FAILURE"></span><span id="error_ipsec_ike_authorization_failure"></span>**FEHLER: \_ \_ IPSEC-IKE-AUTORISIERUNGSFEHLER \_ \_**
</dt> <dd> <dl> <dt>

13905 (0x3651)
</dt> <dt>



Die Einrichtung der Sicherheitszuordnung ist nicht autorisiert.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_STRONG_CRED_AUTHORIZATION_FAILURE"></span><span id="error_ipsec_ike_strong_cred_authorization_failure"></span>**\_FEHLER: \_ IPSEC-IKE-AUTORISIERUNGSFEHLER \_ \_ MIT \_ STARKER \_ CRED-BERECHTIGUNG**
</dt> <dd> <dl> <dt>

13906 (0x3652)
</dt> <dt>



Sa-Einrichtung ist nicht autorisiert, da es keine ausreichend starken PKINIT-basierten Anmeldeinformationen gibt.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_AUTHORIZATION_FAILURE_WITH_OPTIONAL_RETRY"></span><span id="error_ipsec_ike_authorization_failure_with_optional_retry"></span>**FEHLER \_ BEI \_ IPSEC-IKE-AUTORISIERUNGSFEHLER \_ \_ MIT \_ \_ \_ OPTIONALER WIEDERHOLUNG**
</dt> <dd> <dl> <dt>

13907 (0x3653)
</dt> <dt>



Die Einrichtung der Sicherheitszuordnung ist nicht autorisiert. Möglicherweise müssen Sie aktualisierte oder andere Anmeldeinformationen eingeben, z. B. eine Smartcard.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_STRONG_CRED_AUTHORIZATION_AND_CERTMAP_FAILURE"></span><span id="error_ipsec_ike_strong_cred_authorization_and_certmap_failure"></span>**\_FEHLER: \_ IPSEC-IKE-AUTORISIERUNG \_ \_ MIT \_ STARKER CRED-BERECHTIGUNG \_ UND FEHLER BEI \_ CERTMAP \_**
</dt> <dd> <dl> <dt>

13908 (0x3654)
</dt> <dt>



Sa-Einrichtung ist nicht autorisiert, da es keine ausreichend starken PKINIT-basierten Anmeldeinformationen gibt. Dies kann mit einem Fehler bei der Zertifikat-zu-Konto-Zuordnung für die SA in Zusammenhang stehen.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_NEG_STATUS_EXTENDED_END"></span><span id="error_ipsec_ike_neg_status_extended_end"></span>**FEHLER: \_ IPSEC \_ IKE \_ NEG STATUS \_ EXTENDED \_ \_ END**
</dt> <dd> <dl> <dt>

13909 (0x3655)
</dt> <dt>



FEHLER: \_ IPSEC \_ IKE \_ NEG STATUS \_ EXTENDED \_ \_ END


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_BAD_SPI"></span><span id="error_ipsec_bad_spi"></span>**FEHLER: \_ FEHLERHAFTER \_ IPSEC-SPI \_**
</dt> <dd> <dl> <dt>

13910 (0x3656)
</dt> <dt>



Die SPI im Paket passt nicht zu einer gültigen IPsec-SA.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_SA_LIFETIME_EXPIRED"></span><span id="error_ipsec_sa_lifetime_expired"></span>**FEHLER: \_ \_ IPSEC-SA-GÜLTIGKEITSDAUER \_ \_ ABGELAUFEN**
</dt> <dd> <dl> <dt>

13911 (0x3657)
</dt> <dt>



Das Paket wurde für eine IPsec-SA empfangen, deren Lebensdauer abgelaufen ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_WRONG_SA"></span><span id="error_ipsec_wrong_sa"></span>**FEHLER: \_ IPSEC \_ WRONG \_ SA**
</dt> <dd> <dl> <dt>

13912 (0x3658)
</dt> <dt>



Das Paket wurde für eine IPsec-SA empfangen, die nicht mit den Paketmerkmalen übereinstimmen.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_REPLAY_CHECK_FAILED"></span><span id="error_ipsec_replay_check_failed"></span>**FEHLER: \_ FEHLER BEI DER \_ IPSEC-WIEDERGABEPRÜFUNG \_ \_**
</dt> <dd> <dl> <dt>

13913 (0x3659)
</dt> <dt>



Fehler bei der Wiedergabe der Paketsequenznummer.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_INVALID_PACKET"></span><span id="error_ipsec_invalid_packet"></span>**FEHLER: \_ UNGÜLTIGES \_ IPSEC-PAKET \_**
</dt> <dd> <dl> <dt>

13914 (0x365A)
</dt> <dt>



IPsec-Header und/oder Nachspann im Paket sind ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_INTEGRITY_CHECK_FAILED"></span><span id="error_ipsec_integrity_check_failed"></span>**FEHLER: \_ FEHLER BEI DER \_ IPSEC-INTEGRITÄTSPRÜFUNG \_ \_**
</dt> <dd> <dl> <dt>

13915 (0x365B)
</dt> <dt>



Fehler bei der IPsec-Integritätsprüfung.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_CLEAR_TEXT_DROP"></span><span id="error_ipsec_clear_text_drop"></span>**FEHLER: \_ LÖSCHEN VON \_ IPSEC-KLARTEXT \_ \_**
</dt> <dd> <dl> <dt>

13916 (0x365C)
</dt> <dt>



IPsec hat ein Klartextpaket gelöscht.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_AUTH_FIREWALL_DROP"></span><span id="error_ipsec_auth_firewall_drop"></span>**FEHLER \_ BEIM DROP DER IPSEC-AUTHENTIFIZIERUNGSFIREWALL \_ \_ \_**
</dt> <dd> <dl> <dt>

13917 (0x365D)
</dt> <dt>



IPsec hat ein eingehendes ESP-Paket im authentifizierten Firewallmodus gelöscht. Dieser Rückgang ist unbedenklich.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_THROTTLE_DROP"></span><span id="error_ipsec_throttle_drop"></span>**FEHLER: \_ \_ IPSEC-DROSSELUNGSABBRUCH \_**
</dt> <dd> <dl> <dt>

13918 (0x365E)
</dt> <dt>



IPsec hat ein Paket aufgrund einer DoS-Drosselung gelöscht.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_DOSP_BLOCK"></span><span id="error_ipsec_dosp_block"></span>**\_FEHLER: \_ IPSEC-DOSP-BLOCK \_**
</dt> <dd> <dl> <dt>

13925 (0x3665)
</dt> <dt>



IPsec DoS Protection hat eine explizite Blockregel verwendet.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_DOSP_RECEIVED_MULTICAST"></span><span id="error_ipsec_dosp_received_multicast"></span>**FEHLER: \_ IPSEC \_ DOSP \_ HAT \_ MULTICAST EMPFANGEN**
</dt> <dd> <dl> <dt>

13926 (0x3666)
</dt> <dt>



IPsec DoS Protection hat ein IPsec-spezifisches Multicastpaket empfangen, das nicht zulässig ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_DOSP_INVALID_PACKET"></span><span id="error_ipsec_dosp_invalid_packet"></span>**FEHLER: \_ UNGÜLTIGES \_ IPSEC-DOSP-PAKET \_ \_**
</dt> <dd> <dl> <dt>

13927 (0x3667)
</dt> <dt>



IPsec DoS Protection hat ein falsch formatiertes Paket empfangen.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_DOSP_STATE_LOOKUP_FAILED"></span><span id="error_ipsec_dosp_state_lookup_failed"></span>**FEHLER: \_ FEHLER BEI \_ DER IPSEC-DOSP-ZUSTANDSSUCHE \_ \_ \_**
</dt> <dd> <dl> <dt>

13928 (0x3668)
</dt> <dt>



IPsec DoS Protection konnte den Status nicht suchen.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_DOSP_MAX_ENTRIES"></span><span id="error_ipsec_dosp_max_entries"></span>**FEHLER: \_ MAXIMALE \_ IPSEC-DOSP-EINTRÄGE \_ \_**
</dt> <dd> <dl> <dt>

13929 (0x3669)
</dt> <dt>



IPsec DoS Protection konnte den Zustand nicht erstellen, da die maximale Anzahl von Einträgen, die von der Richtlinie zugelassen werden, erreicht wurde.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_DOSP_KEYMOD_NOT_ALLOWED"></span><span id="error_ipsec_dosp_keymod_not_allowed"></span>**FEHLER: \_ IPSEC \_ DOSP \_ KEYMOD \_ NICHT \_ ZULÄSSIG**
</dt> <dd> <dl> <dt>

13930 (0x366A)
</dt> <dt>



IPsec DoS Protection hat ein IPsec-Aushandlungspaket für ein Schlüsselmodul erhalten, das von der Richtlinie nicht zugelassen wird.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_DOSP_NOT_INSTALLED"></span><span id="error_ipsec_dosp_not_installed"></span>**FEHLER: \_ IPSEC \_ DOSP \_ NICHT \_ INSTALLIERT**
</dt> <dd> <dl> <dt>

13931 (0x366B)
</dt> <dt>



IPsec DoS Protection wurde nicht aktiviert.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_DOSP_MAX_PER_IP_RATELIMIT_QUEUES"></span><span id="error_ipsec_dosp_max_per_ip_ratelimit_queues"></span>**FEHLER: \_ IPSEC \_ DOSP \_ \_ MAX. PRO \_ \_ IP-RATELIMIT-WARTESCHLANGE \_**
</dt> <dd> <dl> <dt>

13932 (0x366C)
</dt> <dt>



IPsec DoS Protection konnte keine Warteschlange für interne IP-Warteschlangenraten erstellen, da die maximale Anzahl von Warteschlangen, die von der Richtlinie zugelassen werden, erreicht wurde.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_SECTION_NOT_FOUND"></span><span id="error_sxs_section_not_found"></span>**FEHLER \_ IM SXS-ABSCHNITT \_ NICHT \_ \_ GEFUNDEN**
</dt> <dd> <dl> <dt>

14000 (0x36B0)
</dt> <dt>



Der angeforderte Abschnitt war im Aktivierungskontext nicht vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_CANT_GEN_ACTCTX"></span><span id="error_sxs_cant_gen_actctx"></span>**FEHLER: \_ SXS \_ CANT \_ GEN \_ ACTCTX**
</dt> <dd> <dl> <dt>

14001 (0x36B1)
</dt> <dt>



Die Anwendung konnte nicht gestartet werden, da die Konfiguration der Anwendung nicht korrekt ist. Weitere Informationen finden Sie im Anwendungsereignisprotokoll, oder verwenden Sie sxstrace.exe Befehlszeilentool.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_INVALID_ACTCTXDATA_FORMAT"></span><span id="error_sxs_invalid_actctxdata_format"></span>**FEHLER: \_ SXS \_ UNGÜLTIGES \_ ACTCTXDATA-FORMAT \_**
</dt> <dd> <dl> <dt>

14002 (0x36B2)
</dt> <dt>



Das Datenformat der Anwendungsbindung ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_ASSEMBLY_NOT_FOUND"></span><span id="error_sxs_assembly_not_found"></span>**FEHLER: \_ \_ SXS-ASSEMBLY NICHT \_ \_ GEFUNDEN**
</dt> <dd> <dl> <dt>

14003 (0x36B3)
</dt> <dt>



Die Assembly, auf die verwiesen wird, ist nicht auf Ihrem System installiert.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_MANIFEST_FORMAT_ERROR"></span><span id="error_sxs_manifest_format_error"></span>**FEHLER: \_ \_ SXS-MANIFESTFORMATFEHLER \_ \_**
</dt> <dd> <dl> <dt>

14004 (0x36B4)
</dt> <dt>



Die Manifestdatei beginnt nicht mit den erforderlichen Tag- und Formatinformationen.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_MANIFEST_PARSE_ERROR"></span><span id="error_sxs_manifest_parse_error"></span>**FEHLER BEIM \_ ANALYSIEREN DES SXS-MANIFESTS \_ \_ \_**
</dt> <dd> <dl> <dt>

14005 (0x36B5)
</dt> <dt>



Die Manifestdatei enthält mindestens einen Syntaxfehler.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_ACTIVATION_CONTEXT_DISABLED"></span><span id="error_sxs_activation_context_disabled"></span>**FEHLER: \_ \_ SXS-AKTIVIERUNGSKONTEXT \_ \_ DEAKTIVIERT**
</dt> <dd> <dl> <dt>

14006 (0x36B6)
</dt> <dt>



Die Anwendung hat versucht, einen deaktivierten Aktivierungskontext zu aktivieren.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_KEY_NOT_FOUND"></span><span id="error_sxs_key_not_found"></span>**FEHLER: \_ \_ SXS-SCHLÜSSEL NICHT \_ \_ GEFUNDEN**
</dt> <dd> <dl> <dt>

14007 (0x36B7)
</dt> <dt>



Der angeforderte Suchschlüssel wurde in einem aktiven Aktivierungskontext nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_VERSION_CONFLICT"></span><span id="error_sxs_version_conflict"></span>**FEHLER: \_ \_ SXS-VERSIONSKONFLIKT \_**
</dt> <dd> <dl> <dt>

14008 (0x36B8)
</dt> <dt>



Eine komponentenversion, die von der Anwendung benötigt wird, steht in Konflikt mit einer anderen bereits aktiven Komponentenversion.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_WRONG_SECTION_TYPE"></span><span id="error_sxs_wrong_section_type"></span>**FEHLER \_ SXS \_ FALSCHER \_ \_ ABSCHNITTSTYP**
</dt> <dd> <dl> <dt>

14009 (0x36B9)
</dt> <dt>



Der vom Typ angeforderte Aktivierungskontextabschnitt passt nicht zur verwendeten Abfrage-API.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_THREAD_QUERIES_DISABLED"></span><span id="error_sxs_thread_queries_disabled"></span>**FEHLER \_ BEI DEAKTIVIERTEN SXS-THREADABFRAGEN \_ \_ \_**
</dt> <dd> <dl> <dt>

14010 (0x36BA)
</dt> <dt>



Das Fehlen von Systemressourcen erfordert, dass die isolierte Aktivierung für den aktuellen Ausführungsthread deaktiviert ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_PROCESS_DEFAULT_ALREADY_SET"></span><span id="error_sxs_process_default_already_set"></span>**FEHLER: \_ STANDARD FÜR SXS-PROZESS \_ BEREITS \_ \_ \_ FESTGELEGT**
</dt> <dd> <dl> <dt>

14011 (0x36BB)
</dt> <dt>



Fehler beim Festlegen des Standardaktivierungskontexts für den Prozess, da der Standardaktivierungskontext des Prozesses bereits festgelegt wurde.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_UNKNOWN_ENCODING_GROUP"></span><span id="error_sxs_unknown_encoding_group"></span>**FEHLER: \_ SXS \_ UNKNOWN ENCODING \_ \_ GROUP**
</dt> <dd> <dl> <dt>

14012 (0x36BC)
</dt> <dt>



Der angegebene Codierungsgruppenbezeichner wird nicht erkannt.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_UNKNOWN_ENCODING"></span><span id="error_sxs_unknown_encoding"></span>**FEHLER: \_ SXS UNKNOWN \_ \_ ENCODING**
</dt> <dd> <dl> <dt>

14013 (0x36BD)
</dt> <dt>



Die angeforderte Codierung wird nicht erkannt.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_INVALID_XML_NAMESPACE_URI"></span><span id="error_sxs_invalid_xml_namespace_uri"></span>**FEHLER: \_ SXS \_ UNGÜLTIGER \_ \_ XML-NAMESPACE-URI \_**
</dt> <dd> <dl> <dt>

14014 (0x36BE)
</dt> <dt>



Das Manifest enthält einen Verweis auf einen ungültigen URI.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_ROOT_MANIFEST_DEPENDENCY_NOT_INSTALLED"></span><span id="error_sxs_root_manifest_dependency_not_installed"></span>**FEHLER: \_ \_ SXS-STAMMMANIFESTABHÄNGIGKEIT \_ \_ NICHT \_ \_ INSTALLIERT**
</dt> <dd> <dl> <dt>

14015 (0x36BF)
</dt> <dt>



Das Anwendungsmanifest enthält einen Verweis auf eine abhängige Assembly, die nicht installiert ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_LEAF_MANIFEST_DEPENDENCY_NOT_INSTALLED"></span><span id="error_sxs_leaf_manifest_dependency_not_installed"></span>**FEHLER: \_ SXS LEAF MANIFEST DEPENDENCY NOT INSTALLED (SXS-BLATTMANIFESTABHÄNGIGKEIT \_ \_ NICHT \_ \_ \_ INSTALLIERT)**
</dt> <dd> <dl> <dt>

14016 (0x36C0)
</dt> <dt>



Das Manifest für eine von der Anwendung verwendete Assembly verfügt über einen Verweis auf eine abhängige Assembly, die nicht installiert ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_INVALID_ASSEMBLY_IDENTITY_ATTRIBUTE"></span><span id="error_sxs_invalid_assembly_identity_attribute"></span>**FEHLER: \_ SXS \_ UNGÜLTIGES \_ \_ ASSEMBLYIDENTITÄTSATTRIBUT \_**
</dt> <dd> <dl> <dt>

14017 (0x36C1)
</dt> <dt>



Das Manifest enthält ein ungültiges Attribut für die Assemblyidentität.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_MANIFEST_MISSING_REQUIRED_DEFAULT_NAMESPACE"></span><span id="error_sxs_manifest_missing_required_default_namespace"></span>**FEHLER: \_ \_ SXS-MANIFEST \_ FEHLT \_ ERFORDERLICHER \_ \_ STANDARDNAMESPACE**
</dt> <dd> <dl> <dt>

14018 (0x36C2)
</dt> <dt>



Im Manifest fehlt die erforderliche Standardnamespacespezifikation für das Assemblyelement.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_MANIFEST_INVALID_REQUIRED_DEFAULT_NAMESPACE"></span><span id="error_sxs_manifest_invalid_required_default_namespace"></span>**FEHLER: \_ \_ SXS-MANIFEST \_ \_ UNGÜLTIGER ERFORDERLICHER \_ \_ STANDARDNAMESPACE**
</dt> <dd> <dl> <dt>

14019 (0x36C3)
</dt> <dt>



Für das Manifest ist ein Standardnamespace für das Assemblyelement angegeben, aber der Wert ist nicht "urn:schemas-microsoft-com:asm.v1".


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_PRIVATE_MANIFEST_CROSS_PATH_WITH_REPARSE_POINT"></span><span id="error_sxs_private_manifest_cross_path_with_reparse_point"></span>**FEHLER: \_ SXS \_ PRIVATE MANIFEST CROSS PATH WITH \_ \_ \_ \_ \_ REPARSE \_ POINT**
</dt> <dd> <dl> <dt>

14020 (0x36C4)
</dt> <dt>



Der private Manifest-Test hat einen Pfad mit einem nicht unterstützten Reparsepunkt überschritten.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_DUPLICATE_DLL_NAME"></span><span id="error_sxs_duplicate_dll_name"></span>**FEHLER: \_ DOPPELTER SXS-DLL-NAME \_ \_ \_**
</dt> <dd> <dl> <dt>

14021 (0x36C5)
</dt> <dt>



Zwei oder mehr Komponenten, auf die direkt oder indirekt vom Anwendungsmanifest verwiesen wird, verfügen über Dateien mit demselben Namen.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_DUPLICATE_WINDOWCLASS_NAME"></span><span id="error_sxs_duplicate_windowclass_name"></span>**FEHLER: \_ SXS \_ DUPLICATE \_ WINDOWCLASS \_ NAME**
</dt> <dd> <dl> <dt>

14022 (0x36C6)
</dt> <dt>



Zwei oder mehr Komponenten, auf die direkt oder indirekt vom Anwendungsmanifest verwiesen wird, verfügen über Fensterklassen mit demselben Namen.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_DUPLICATE_CLSID"></span><span id="error_sxs_duplicate_clsid"></span>**FEHLER: \_ SXS \_ DUPLICATE \_ CLSID**
</dt> <dd> <dl> <dt>

14023 (0x36C7)
</dt> <dt>



Zwei oder mehr Komponenten, auf die direkt oder indirekt vom Anwendungsmanifest verwiesen wird, verfügen über dieselben COM-Server-CLSIDs.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_DUPLICATE_IID"></span><span id="error_sxs_duplicate_iid"></span>**FEHLER: \_ SXS \_ DUPLICATE \_ IID**
</dt> <dd> <dl> <dt>

14024 (0x36C8)
</dt> <dt>



Zwei oder mehr Komponenten, auf die direkt oder indirekt vom Anwendungsmanifest verwiesen wird, verfügen über Proxys für die gleichen COM-Schnittstellen-IIDs.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_DUPLICATE_TLBID"></span><span id="error_sxs_duplicate_tlbid"></span>**FEHLER: \_ SXS \_ DUPLICATE \_ TLBID**
</dt> <dd> <dl> <dt>

14025 (0x36C9)
</dt> <dt>



Zwei oder mehr Komponenten, auf die direkt oder indirekt vom Anwendungsmanifest verwiesen wird, verfügen über die gleichen COM-Typbibliotheks-TLBIDs.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_DUPLICATE_PROGID"></span><span id="error_sxs_duplicate_progid"></span>**FEHLER: \_ SXS \_ DUPLICATE \_ PROGID**
</dt> <dd> <dl> <dt>

14026 (0x36CA)
</dt> <dt>



Zwei oder mehr Komponenten, auf die direkt oder indirekt vom Anwendungsmanifest verwiesen wird, verfügen über die gleichen COM-ProgIDs.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_DUPLICATE_ASSEMBLY_NAME"></span><span id="error_sxs_duplicate_assembly_name"></span>**FEHLER: \_ NAME DER DOPPELTEN SXS-ASSEMBLY \_ \_ \_**
</dt> <dd> <dl> <dt>

14027 (0x36CB)
</dt> <dt>



Zwei oder mehr Komponenten, auf die direkt oder indirekt vom Anwendungsmanifest verwiesen wird, sind unterschiedliche Versionen derselben Komponente, die nicht zulässig sind.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_FILE_HASH_MISMATCH"></span><span id="error_sxs_file_hash_mismatch"></span>**FEHLER: \_ \_ SXS-DATEIHASHKONFLIKT \_ \_**
</dt> <dd> <dl> <dt>

14028 (0x36CC)
</dt> <dt>



Die Datei einer Komponente passt nicht zu den Überprüfungsinformationen, die im Komponentenmanifest vorhanden sind.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_POLICY_PARSE_ERROR"></span><span id="error_sxs_policy_parse_error"></span>**FEHLER BEIM \_ ANALYSIEREN DER SXS-RICHTLINIE \_ \_ \_**
</dt> <dd> <dl> <dt>

14029 (0x36CD)
</dt> <dt>



Das Richtlinienmanifest enthält mindestens einen Syntaxfehler.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_MISSINGQUOTE"></span><span id="error_sxs_xml_e_missingquote"></span>**FEHLER \_ SXS \_ XML E \_ \_ MISSINGQUOTE**
</dt> <dd> <dl> <dt>

14030 (0x36CE)
</dt> <dt>



Manifestparsenfehler: Es wurde ein Zeichenfolgenliteral erwartet, aber es wurde kein öffnende Anführungszeichen gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_COMMENTSYNTAX"></span><span id="error_sxs_xml_e_commentsyntax"></span>**FEHLER \_ SXS \_ XML E \_ \_ COMMENTSYNTAX**
</dt> <dd> <dl> <dt>

14031 (0x36CF)
</dt> <dt>



Manifestparsenfehler: In einem Kommentar wurde eine falsche Syntax verwendet.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_BADSTARTNAMECHAR"></span><span id="error_sxs_xml_e_badstartnamechar"></span>**FEHLER \_ SXS \_ XML E \_ \_ BADSTARTNAMECHAR**
</dt> <dd> <dl> <dt>

14032 (0x36D0)
</dt> <dt>



Manifestparsenfehler: Ein Name wurde mit einem ungültigen Zeichen gestartet.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_BADNAMECHAR"></span><span id="error_sxs_xml_e_badnamechar"></span>**FEHLER \_ SXS \_ XML E \_ \_ BADNAMECHAR**
</dt> <dd> <dl> <dt>

14033 (0x36D1)
</dt> <dt>



Manifestparsenfehler: Ein Name enthielt ein ungültiges Zeichen.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_BADCHARINSTRING"></span><span id="error_sxs_xml_e_badcharinstring"></span>**FEHLER \_ SXS \_ XML E \_ \_ BADCHARINSTRING**
</dt> <dd> <dl> <dt>

14034 (0x36D2)
</dt> <dt>



Manifestparsenfehler: Ein Zeichenfolgenliteral enthielt ein ungültiges Zeichen.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_XMLDECLSYNTAX"></span><span id="error_sxs_xml_e_xmldeclsyntax"></span>**FEHLER \_ SXS \_ XML E \_ \_ XMLDECLSYNTAX**
</dt> <dd> <dl> <dt>

14035 (0x36D3)
</dt> <dt>



Manifestparsenfehler: Ungültige Syntax für eine XML-Deklaration.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_BADCHARDATA"></span><span id="error_sxs_xml_e_badchardata"></span>**FEHLER \_ SXS \_ XML E \_ \_ BADCHARDATA**
</dt> <dd> <dl> <dt>

14036 (0x36D4)
</dt> <dt>



Manifestparsenfehler: Im Textinhalt wurde ein ungültiges Zeichen gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_MISSINGWHITESPACE"></span><span id="error_sxs_xml_e_missingwhitespace"></span>**FEHLER \_ SXS \_ XML E \_ \_ MISSINGWHITESPACE**
</dt> <dd> <dl> <dt>

14037 (0x36D5)
</dt> <dt>



Manifestparsenfehler: Erforderlicher Leerraum fehlte.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_EXPECTINGTAGEND"></span><span id="error_sxs_xml_e_expectingtagend"></span>**FEHLER \_ SXS \_ XML E \_ \_ EXPECTINGTAGED**
</dt> <dd> <dl> <dt>

14038 (0x36D6)
</dt> <dt>



Manifestparsenfehler: Das Zeichen ">" wurde erwartet.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_MISSINGSEMICOLON"></span><span id="error_sxs_xml_e_missingsemicolon"></span>**FEHLER \_ SXS \_ XML E \_ \_ MISSINGSEMICOLON**
</dt> <dd> <dl> <dt>

14039 (0x36D7)
</dt> <dt>



Manifestparsenfehler: Ein Semikolonzeichen wurde erwartet.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_UNBALANCEDPAREN"></span><span id="error_sxs_xml_e_unbalancedparen"></span>**FEHLER \_ SXS \_ XML E \_ \_ UNBALANCEDPAREN**
</dt> <dd> <dl> <dt>

14040 (0x36D8)
</dt> <dt>



Manifestparsenfehler: Unausgewogene Klammern.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_INTERNALERROR"></span><span id="error_sxs_xml_e_internalerror"></span>**FEHLER \_ SXS \_ XML E \_ \_ INTERNALERROR**
</dt> <dd> <dl> <dt>

14041 (0x36D9)
</dt> <dt>



Manifestparsenfehler: Interner Fehler.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_UNEXPECTED_WHITESPACE"></span><span id="error_sxs_xml_e_unexpected_whitespace"></span>**FEHLER: \_ SXS \_ XML E UNEXPECTED \_ \_ \_ WHITESPACE**
</dt> <dd> <dl> <dt>

14042 (0x36DA)
</dt> <dt>



Manifestparsenfehler: Leerraum ist an dieser Position nicht zulässig.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_INCOMPLETE_ENCODING"></span><span id="error_sxs_xml_e_incomplete_encoding"></span>**FEHLER: \_ SXS \_ XML E \_ \_ UNVOLLSTÄNDIGE \_ CODIERUNG**
</dt> <dd> <dl> <dt>

14043 (0x36DB)
</dt> <dt>



Manifestparsfehler: Das Ende der Datei wurde für die aktuelle Codierung in einem ungültigen Zustand erreicht.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_MISSING_PAREN"></span><span id="error_sxs_xml_e_missing_paren"></span>**FEHLER \_ SXS \_ XML E MISSING \_ \_ \_ PAREN**
</dt> <dd> <dl> <dt>

14044 (0x36DC)
</dt> <dt>



Manifestparsenfehler: Fehlende Klammer.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_EXPECTINGCLOSEQUOTE"></span><span id="error_sxs_xml_e_expectingclosequote"></span>**FEHLER \_ SXS \_ XML E \_ \_ EXPECTINGCLOSEQUOTE**
</dt> <dd> <dl> <dt>

14045 (0x36DD)
</dt> <dt>



Manifestparsenfehler: Ein einzelnes oder doppeltes schließende Anführungszeichen ( \\ ' oder \\ ") fehlt.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_MULTIPLE_COLONS"></span><span id="error_sxs_xml_e_multiple_colons"></span>**FEHLER: \_ SXS \_ XML E MULTIPLE \_ \_ \_ COLONS**
</dt> <dd> <dl> <dt>

14046 (0x36DE)
</dt> <dt>



Manifestparsenfehler: Mehrere Doppelpunkte sind in einem Namen nicht zulässig.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_INVALID_DECIMAL"></span><span id="error_sxs_xml_e_invalid_decimal"></span>**FEHLER \_ SXS \_ XML E INVALID \_ \_ \_ DECIMAL**
</dt> <dd> <dl> <dt>

14047 (0x36DF)
</dt> <dt>



Manifestparsenfehler: Ungültiges Zeichen für Dezimalziffer.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_INVALID_HEXIDECIMAL"></span><span id="error_sxs_xml_e_invalid_hexidecimal"></span>**FEHLER \_ SXS \_ XML E INVALID \_ \_ \_ HEXIDECIMAL**
</dt> <dd> <dl> <dt>

14048 (0x36E0)
</dt> <dt>



Manifestparsenfehler: Ungültiges Zeichen für Hexadezimalziffer.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_INVALID_UNICODE"></span><span id="error_sxs_xml_e_invalid_unicode"></span>**FEHLER \_ SXS \_ XML E INVALID \_ \_ \_ UNICODE**
</dt> <dd> <dl> <dt>

14049 (0x36E1)
</dt> <dt>



Manifestparsenfehler: Ungültiger Unicode-Zeichenwert für diese Plattform.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_WHITESPACEORQUESTIONMARK"></span><span id="error_sxs_xml_e_whitespaceorquestionmark"></span>**FEHLER \_ SXS \_ XML E \_ \_ WHITESPACEORQUESTIONMARK**
</dt> <dd> <dl> <dt>

14050 (0x36E2)
</dt> <dt>



Manifestparsenfehler: Leerraum oder "?" werden erwartet.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_UNEXPECTEDENDTAG"></span><span id="error_sxs_xml_e_unexpectedendtag"></span>**FEHLER \_ SXS \_ XML E \_ \_ UNEXPECTEDENDTAG**
</dt> <dd> <dl> <dt>

14051 (0x36E3)
</dt> <dt>



Manifestparsenfehler: Das Endtag wurde an diesem Speicherort nicht erwartet.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_UNCLOSEDTAG"></span><span id="error_sxs_xml_e_unclosedtag"></span>**FEHLER \_ SXS \_ XML E \_ \_ UNCLOSEDTAG**
</dt> <dd> <dl> <dt>

14052 (0x36E4)
</dt> <dt>



Manifestparsenfehler: Die folgenden Tags wurden nicht geschlossen: %1.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_DUPLICATEATTRIBUTE"></span><span id="error_sxs_xml_e_duplicateattribute"></span>**FEHLER: \_ SXS \_ XML E \_ \_ DUPLICATEATTRIBUTE**
</dt> <dd> <dl> <dt>

14053 (0x36E5)
</dt> <dt>



Manifestparsenfehler: Doppeltes Attribut.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_MULTIPLEROOTS"></span><span id="error_sxs_xml_e_multipleroots"></span>**FEHLER \_ SXS \_ XML E \_ \_ MULTIPLEROOTS**
</dt> <dd> <dl> <dt>

14054 (0x36E6)
</dt> <dt>



Manifestparsenfehler: In einem XML-Dokument ist nur ein Element der obersten Ebene zulässig.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_INVALIDATROOTLEVEL"></span><span id="error_sxs_xml_e_invalidatrootlevel"></span>**FEHLER \_ SXS \_ XML E \_ \_ INVALIDATROOTLEVEL**
</dt> <dd> <dl> <dt>

14055 (0x36E7)
</dt> <dt>



Manifestparsenfehler: Ungültig auf der obersten Ebene des Dokuments.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_BADXMLDECL"></span><span id="error_sxs_xml_e_badxmldecl"></span>**FEHLER \_ SXS \_ XML E \_ \_ BADXMLDECL**
</dt> <dd> <dl> <dt>

14056 (0x36E8)
</dt> <dt>



Manifestparsenfehler: Ungültige XML-Deklaration.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_MISSINGROOT"></span><span id="error_sxs_xml_e_missingroot"></span>**FEHLER \_ SXS \_ XML E \_ \_ MISSINGROOT**
</dt> <dd> <dl> <dt>

14057 (0x36E9)
</dt> <dt>



Manifestparsenfehler: Das XML-Dokument muss über ein Element der obersten Ebene verfügen.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_UNEXPECTEDEOF"></span><span id="error_sxs_xml_e_unexpectedeof"></span>**FEHLER \_ SXS \_ XML E \_ \_ UNEXPECTEDEOF**
</dt> <dd> <dl> <dt>

14058 (0x36EA)
</dt> <dt>



Manifestparsenfehler: Unerwartetes Dateiende.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_BADPEREFINSUBSET"></span><span id="error_sxs_xml_e_badperefinsubset"></span>**FEHLER \_ SXS \_ XML E \_ \_ BADPEREFINSUBSET**
</dt> <dd> <dl> <dt>

14059 (0x36EB)
</dt> <dt>



Manifestparsenfehler: Parameterentitäten können nicht innerhalb von Markupdeklarationen in einer internen Teilmenge verwendet werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_UNCLOSEDSTARTTAG"></span><span id="error_sxs_xml_e_unclosedstarttag"></span>**FEHLER \_ SXS \_ XML E \_ \_ UNCLOSEDSTARTTAG**
</dt> <dd> <dl> <dt>

14060 (0x36EC)
</dt> <dt>



Manifestparsenfehler: Das Element wurde nicht geschlossen.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_UNCLOSEDENDTAG"></span><span id="error_sxs_xml_e_unclosedendtag"></span>**FEHLER \_ SXS \_ XML E \_ \_ UNCLOSEDENDTAG**
</dt> <dd> <dl> <dt>

14061 (0x36ED)
</dt> <dt>



Manifestparsenfehler: Dem End-Element fehlte das Zeichen ">".


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_UNCLOSEDSTRING"></span><span id="error_sxs_xml_e_unclosedstring"></span>**FEHLER: \_ SXS \_ XML E \_ \_ UNCLOSEDSTRING**
</dt> <dd> <dl> <dt>

14062 (0x36EE)
</dt> <dt>



Manifestparsenfehler: Ein Zeichenfolgenliteral wurde nicht geschlossen.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_UNCLOSEDCOMMENT"></span><span id="error_sxs_xml_e_unclosedcomment"></span>**FEHLER \_ SXS \_ XML E \_ \_ UNCLOSEDCOMMENT**
</dt> <dd> <dl> <dt>

14063 (0x36EF)
</dt> <dt>



Manifestparsierungsfehler: Ein Kommentar wurde nicht geschlossen.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_UNCLOSEDDECL"></span><span id="error_sxs_xml_e_uncloseddecl"></span>**FEHLER \_ SXS \_ XML E \_ \_ UNCLOSEDDECL**
</dt> <dd> <dl> <dt>

14064 (0x36F0)
</dt> <dt>



Manifestparsenfehler: Eine Deklaration wurde nicht geschlossen.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_UNCLOSEDCDATA"></span><span id="error_sxs_xml_e_unclosedcdata"></span>**FEHLER \_ SXS \_ XML E \_ \_ UNCLOSEDCDATA**
</dt> <dd> <dl> <dt>

14065 (0x36F1)
</dt> <dt>



Manifestparsenfehler: Ein CDATA-Abschnitt wurde nicht geschlossen.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_RESERVEDNAMESPACE"></span><span id="error_sxs_xml_e_reservednamespace"></span>**FEHLER: \_ SXS \_ XML E \_ \_ RESERVEDNAMESPACE**
</dt> <dd> <dl> <dt>

14066 (0x36F2)
</dt> <dt>



Manifestparsenfehler: Das Namespacepräfix darf nicht mit der reservierten Zeichenfolge "xml" beginnen.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_INVALIDENCODING"></span><span id="error_sxs_xml_e_invalidencoding"></span>**FEHLER \_ SXS \_ XML E \_ \_ INVALIDENCODING**
</dt> <dd> <dl> <dt>

14067 (0x36F3)
</dt> <dt>



Manifestparsenfehler: Das System unterstützt die angegebene Codierung nicht.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_INVALIDSWITCH"></span><span id="error_sxs_xml_e_invalidswitch"></span>**FEHLER \_ SXS \_ XML E \_ \_ INVALIDSWITCH**
</dt> <dd> <dl> <dt>

14068 (0x36F4)
</dt> <dt>



Manifestparsfehler: Wechsel von der aktuellen Codierung zur angegebenen Codierung wird nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_BADXMLCASE"></span><span id="error_sxs_xml_e_badxmlcase"></span>**FEHLER \_ SXS \_ XML E \_ \_ BADXMLCASE**
</dt> <dd> <dl> <dt>

14069 (0x36F5)
</dt> <dt>



Manifestparsenfehler: Der Name "xml" ist reserviert und muss in Kleinbuchstaben vorliegen.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_INVALID_STANDALONE"></span><span id="error_sxs_xml_e_invalid_standalone"></span>**FEHLER \_ SXS \_ XML E INVALID \_ \_ \_ STANDALONE**
</dt> <dd> <dl> <dt>

14070 (0x36F6)
</dt> <dt>



Manifestparsenfehler: Das eigenständige Attribut muss den Wert "yes" oder "no" aufweisen.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_UNEXPECTED_STANDALONE"></span><span id="error_sxs_xml_e_unexpected_standalone"></span>**FEHLER \_ SXS \_ XML E UNEXPECTED \_ \_ \_ STANDALONE**
</dt> <dd> <dl> <dt>

14071 (0x36F7)
</dt> <dt>



Manifestparsenfehler: Das eigenständige Attribut kann nicht in externen Entitäten verwendet werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_INVALID_VERSION"></span><span id="error_sxs_xml_e_invalid_version"></span>**FEHLER \_ SXS \_ XML E \_ \_ UNGÜLTIGE \_ VERSION**
</dt> <dd> <dl> <dt>

14072 (0x36F8)
</dt> <dt>



Manifestparsenfehler: Ungültige Versionsnummer.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_MISSINGEQUALS"></span><span id="error_sxs_xml_e_missingequals"></span>**FEHLER \_ SXS \_ XML E \_ \_ MISSINGEQUALS**
</dt> <dd> <dl> <dt>

14073 (0x36F9)
</dt> <dt>



Manifestparsenfehler: Fehlendes Gleichheitszeichen zwischen Attribut und Attributwert.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_PROTECTION_RECOVERY_FAILED"></span><span id="error_sxs_protection_recovery_failed"></span>**FEHLER BEI \_ DER WIEDERHERSTELLUNG VON SXS \_ PROTECTION \_ \_**
</dt> <dd> <dl> <dt>

14074 (0x36FA)
</dt> <dt>



Assemblyschutzfehler: Die angegebene Assembly kann nicht wiederhergestellt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_PROTECTION_PUBLIC_KEY_TOO_SHORT"></span><span id="error_sxs_protection_public_key_too_short"></span>**FEHLER: \_ ÖFFENTLICHER SXS \_ \_ \_ PROTECTION-SCHLÜSSEL \_ ZU \_ KURZ**
</dt> <dd> <dl> <dt>

14075 (0x36FB)
</dt> <dt>



Assemblyschutzfehler: Der öffentliche Schlüssel für eine Assembly war zu kurz, um zugelassen zu werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_PROTECTION_CATALOG_NOT_VALID"></span><span id="error_sxs_protection_catalog_not_valid"></span>**FEHLER: \_ SXS \_ \_ PROTECTION-KATALOG \_ UNGÜLTIG \_**
</dt> <dd> <dl> <dt>

14076 (0x36FC)
</dt> <dt>



Assembly protection error (Assemblyschutzfehler): Der Katalog für eine Assembly ist ungültig oder passt nicht zum Manifest der Assembly.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_UNTRANSLATABLE_HRESULT"></span><span id="error_sxs_untranslatable_hresult"></span>**FEHLER: \_ SXS \_ UNTRANSLATABLE \_ HRESULT**
</dt> <dd> <dl> <dt>

14077 (0x36FD)
</dt> <dt>



Ein HRESULT konnte nicht in einen entsprechenden Win32-Fehlercode übersetzt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_PROTECTION_CATALOG_FILE_MISSING"></span><span id="error_sxs_protection_catalog_file_missing"></span>**FEHLER: \_ SXS \_ \_ PROTECTION-KATALOGDATEI \_ \_ FEHLT**
</dt> <dd> <dl> <dt>

14078 (0x36FE)
</dt> <dt>



Assembly protection error (Assemblyschutzfehler): Der Katalog für eine Assembly fehlt.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_MISSING_ASSEMBLY_IDENTITY_ATTRIBUTE"></span><span id="error_sxs_missing_assembly_identity_attribute"></span>**FEHLER: \_ SXS \_ MISSING ASSEMBLY IDENTITY \_ \_ \_ ATTRIBUTE**
</dt> <dd> <dl> <dt>

14079 (0x36FF)
</dt> <dt>



In der angegebenen Assemblyidentität fehlt mindestens ein Attribut, das in diesem Kontext vorhanden sein muss.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_INVALID_ASSEMBLY_IDENTITY_ATTRIBUTE_NAME"></span><span id="error_sxs_invalid_assembly_identity_attribute_name"></span>**FEHLER: \_ SXS \_ UNGÜLTIGER \_ \_ \_ ASSEMBLYIDENTITÄTSATTRIBUTNAME \_**
</dt> <dd> <dl> <dt>

14080 (0x3700)
</dt> <dt>



Die angegebene Assemblyidentität verfügt über einen oder mehrere Attributnamen, die Zeichen enthalten, die in XML-Namen nicht zulässig sind.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_ASSEMBLY_MISSING"></span><span id="error_sxs_assembly_missing"></span>**FEHLER: \_ \_ SXS-ASSEMBLY \_ FEHLT**
</dt> <dd> <dl> <dt>

14081 (0x3701)
</dt> <dt>



Die Assembly, auf die verwiesen wird, wurde nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_CORRUPT_ACTIVATION_STACK"></span><span id="error_sxs_corrupt_activation_stack"></span>**FEHLER: \_ SXS \_ BESCHÄDIGTER \_ \_ AKTIVIERUNGSSTAPEL**
</dt> <dd> <dl> <dt>

14082 (0x3702)
</dt> <dt>



Der Aktivierungskontext-Aktivierungsstapel für den ausgeführten Ausführungsthread ist beschädigt.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_CORRUPTION"></span><span id="error_sxs_corruption"></span>**FEHLER: \_ SXS-BESCHÄDIGUNG \_**
</dt> <dd> <dl> <dt>

14083 (0x3703)
</dt> <dt>



Die Anwendungsisolationsmetadaten für diesen Prozess oder Thread sind beschädigt.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_EARLY_DEACTIVATION"></span><span id="error_sxs_early_deactivation"></span>**FEHLER: \_ SXS \_ EARLY \_ DEACTIVATION**
</dt> <dd> <dl> <dt>

14084 (0x3704)
</dt> <dt>



Der aktivierungskontext, der deaktiviert wird, ist nicht der zuletzt aktivierte.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_INVALID_DEACTIVATION"></span><span id="error_sxs_invalid_deactivation"></span>**FEHLER: \_ UNGÜLTIGE SXS-DEAKTIVIERUNG \_ \_**
</dt> <dd> <dl> <dt>

14085 (0x3705)
</dt> <dt>



Der aktivierungskontext, der deaktiviert wird, ist für den aktuellen Ausführungsthread nicht aktiv.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_MULTIPLE_DEACTIVATION"></span><span id="error_sxs_multiple_deactivation"></span>**FEHLER: \_ SXS \_ MULTIPLE \_ DEACTIVATION**
</dt> <dd> <dl> <dt>

14086 (0x3706)
</dt> <dt>



Der aktivierungskontext, der deaktiviert wird, wurde bereits deaktiviert.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_PROCESS_TERMINATION_REQUESTED"></span><span id="error_sxs_process_termination_requested"></span>**FEHLER BEIM \_ BEENDEN DES SXS-PROZESSES \_ \_ \_ ANGEFORDERT**
</dt> <dd> <dl> <dt>

14087 (0x3707)
</dt> <dt>



Eine komponente, die von der Isolationseinrichtung verwendet wird, hat angefordert, den Prozess zu beenden.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_RELEASE_ACTIVATION_CONTEXT"></span><span id="error_sxs_release_activation_context"></span>**FEHLER BEIM \_ SXS-RELEASEAKTIVIERUNGSKONTEXT \_ \_ \_**
</dt> <dd> <dl> <dt>

14088 (0x3708)
</dt> <dt>



Eine Kernelmoduskomponente gibt einen Verweis auf einen Aktivierungskontext frei.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_SYSTEM_DEFAULT_ACTIVATION_CONTEXT_EMPTY"></span><span id="error_sxs_system_default_activation_context_empty"></span>**FEHLER: \_ \_ STANDARDAKTIVIERUNGSKONTEXT DES SXS-SYSTEMS \_ \_ \_ \_ LEER**
</dt> <dd> <dl> <dt>

14089 (0x3709)
</dt> <dt>



Der Aktivierungskontext der Standard-Assembly des Systems konnte nicht generiert werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_INVALID_IDENTITY_ATTRIBUTE_VALUE"></span><span id="error_sxs_invalid_identity_attribute_value"></span>**FEHLER: \_ UNGÜLTIGER SXS-IDENTITÄTSATTRIBUTWERT \_ \_ \_ \_**
</dt> <dd> <dl> <dt>

14090 (0x370A)
</dt> <dt>



Der Wert eines Attributs in einer Identität liegt nicht innerhalb des rechtlichen Bereichs.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_INVALID_IDENTITY_ATTRIBUTE_NAME"></span><span id="error_sxs_invalid_identity_attribute_name"></span>**FEHLER: \_ SXS \_ \_ UNGÜLTIGER \_ IDENTITÄTSATTRIBUTNAME \_**
</dt> <dd> <dl> <dt>

14091 (0x370B)
</dt> <dt>



Der Name eines Attributs in einer Identität liegt nicht innerhalb des rechtlichen Bereichs.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_IDENTITY_DUPLICATE_ATTRIBUTE"></span><span id="error_sxs_identity_duplicate_attribute"></span>**FEHLER: \_ SXS \_ IDENTITY \_ DUPLICATE \_ ATTRIBUTE**
</dt> <dd> <dl> <dt>

14092 (0x370C)
</dt> <dt>



Eine Identität enthält zwei Definitionen für das gleiche Attribut.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_IDENTITY_PARSE_ERROR"></span><span id="error_sxs_identity_parse_error"></span>**FEHLER \_ BEIM ANALYSIEREN DER SXS-IDENTITÄT \_ \_ \_**
</dt> <dd> <dl> <dt>

14093 (0x370D)
</dt> <dt>



Die Identitätszeichenfolge ist falsch formatiert. Dies kann auf ein nach folgendes Komma, mehr als zwei unbenannte Attribute, fehlender Attributname oder fehlender Attributwert zurück führen.


</dt> </dl> </dd> <dt>

<span id="ERROR_MALFORMED_SUBSTITUTION_STRING"></span><span id="error_malformed_substitution_string"></span>**FEHLER: \_ FALSCH FORMATIERTE \_ ERSETZUNGSZEICHENFOLGE \_**
</dt> <dd> <dl> <dt>

14094 (0x370E)
</dt> <dt>



Eine Zeichenfolge, die lokalisierten substituierbaren Inhalt enthält, wurde falsch formatiert. Entweder folgt auf ein Dollarzeichen ($) etwas anderes als eine linke Klammer oder ein anderes Dollarzeichen, oder die rechte Klammer einer Ersetzung wurde nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_INCORRECT_PUBLIC_KEY_TOKEN"></span><span id="error_sxs_incorrect_public_key_token"></span>**FEHLER: \_ SXS: \_ FALSCHES \_ \_ ÖFFENTLICHES \_ SCHLÜSSELTOKEN**
</dt> <dd> <dl> <dt>

14095 (0x370F)
</dt> <dt>



Das Öffentliche Schlüsseltoken entspricht nicht dem angegebenen öffentlichen Schlüssel.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNMAPPED_SUBSTITUTION_STRING"></span><span id="error_unmapped_substitution_string"></span>**FEHLER: \_ NICHT ZUGEORDNETE \_ ERSETZUNGSZEICHENFOLGE \_**
</dt> <dd> <dl> <dt>

14096 (0x3710)
</dt> <dt>



Eine Ersetzungszeichenfolge hatte keine Zuordnung.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_ASSEMBLY_NOT_LOCKED"></span><span id="error_sxs_assembly_not_locked"></span>**FEHLER: \_ \_ SXS-ASSEMBLY NICHT \_ \_ GESPERRT**
</dt> <dd> <dl> <dt>

14097 (0x3711)
</dt> <dt>



Die Komponente muss gesperrt werden, bevor die Anforderung gestellt wird.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_COMPONENT_STORE_CORRUPT"></span><span id="error_sxs_component_store_corrupt"></span>**FEHLER: \_ BESCHÄDIGTER SXS-KOMPONENTENSPEICHER \_ \_ \_**
</dt> <dd> <dl> <dt>

14098 (0x3712)
</dt> <dt>



Der Komponentenspeicher wurde beschädigt.


</dt> </dl> </dd> <dt>

<span id="ERROR_ADVANCED_INSTALLER_FAILED"></span><span id="error_advanced_installer_failed"></span>**FEHLER BEIM \_ \_ ERWEITERTEN \_ INSTALLATIONSPROGRAMM FEHLGESCHLAGEN**
</dt> <dd> <dl> <dt>

14099 (0x3713)
</dt> <dt>



Fehler bei einem erweiterten Installationsprogramm während des Setups oder der Wartung.


</dt> </dl> </dd> <dt>

<span id="ERROR_XML_ENCODING_MISMATCH"></span><span id="error_xml_encoding_mismatch"></span>**FEHLER: \_ \_ XML-CODIERUNGSKONFLIKT \_**
</dt> <dd> <dl> <dt>

14100 (0x3714)
</dt> <dt>



Die Zeichencodierung in der XML-Deklaration passte nicht zur im Dokument verwendeten Codierung.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_MANIFEST_IDENTITY_SAME_BUT_CONTENTS_DIFFERENT"></span><span id="error_sxs_manifest_identity_same_but_contents_different"></span>**FEHLER: \_ SXS \_ MANIFEST IDENTITY SAME BUT CONTENTS \_ \_ \_ \_ \_ DIFFERENT**
</dt> <dd> <dl> <dt>

14101 (0x3715)
</dt> <dt>



Die Identitäten der Manifeste sind identisch, aber ihre Inhalte unterscheiden sich.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_IDENTITIES_DIFFERENT"></span><span id="error_sxs_identities_different"></span>**FEHLER: \_ SXS \_ IDENTITIES \_ DIFFERENT**
</dt> <dd> <dl> <dt>

14102 (0x3716)
</dt> <dt>



Die Komponentenidentitäten unterscheiden sich.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_ASSEMBLY_IS_NOT_A_DEPLOYMENT"></span><span id="error_sxs_assembly_is_not_a_deployment"></span>**FEHLER: \_ \_ SXS-ASSEMBLY IST KEINE \_ \_ \_ \_ BEREITSTELLUNG**
</dt> <dd> <dl> <dt>

14103 (0x3717)
</dt> <dt>



Die Assembly ist keine Bereitstellung.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_FILE_NOT_PART_OF_ASSEMBLY"></span><span id="error_sxs_file_not_part_of_assembly"></span>**FEHLER \_ BEI SXS-DATEI, \_ DIE NICHT TEIL DER ASSEMBLY \_ \_ \_ \_ IST**
</dt> <dd> <dl> <dt>

14104 (0x3718)
</dt> <dt>



Die Datei ist kein Teil der Assembly.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_MANIFEST_TOO_BIG"></span><span id="error_sxs_manifest_too_big"></span>**FEHLER: \_ \_ SXS-MANIFEST ZU \_ \_ GROß**
</dt> <dd> <dl> <dt>

14105 (0x3719)
</dt> <dt>



Die Größe des Manifests überschreitet den maximal zulässigen Wert.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_SETTING_NOT_REGISTERED"></span><span id="error_sxs_setting_not_registered"></span>**FEHLER \_ BEI \_ NICHT \_ REGISTRIERTER SXS-EINSTELLUNG \_**
</dt> <dd> <dl> <dt>

14106 (0x371A)
</dt> <dt>



Die Einstellung ist nicht registriert.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_TRANSACTION_CLOSURE_INCOMPLETE"></span><span id="error_sxs_transaction_closure_incomplete"></span>**FEHLER: \_ \_ SXS-TRANSAKTIONSABSCHLUSS \_ \_ UNVOLLSTÄNDIG**
</dt> <dd> <dl> <dt>

14107 (0x371B)
</dt> <dt>



Mindestens ein erforderlicher Member der Transaktion ist nicht vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_SMI_PRIMITIVE_INSTALLER_FAILED"></span><span id="error_smi_primitive_installer_failed"></span>**FEHLER \_ BEIM \_ \_ INSTALLATIONSPROGRAMM FÜR SMI PRIMITIVE \_**
</dt> <dd> <dl> <dt>

14108 (0x371C)
</dt> <dt>



Fehler beim Installationsprogramm für den primitiven SMI-Installer während des Setups oder der Wartung.


</dt> </dl> </dd> <dt>

<span id="ERROR_GENERIC_COMMAND_FAILED"></span><span id="error_generic_command_failed"></span>**\_FEHLER BEIM GENERISCHEN \_ BEFEHL \_**
</dt> <dd> <dl> <dt>

14109 (0x371D)
</dt> <dt>



Eine generische ausführbare Befehlsdatei hat ein Ergebnis zurückgegeben, das auf einen Fehler hinweist.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_FILE_HASH_MISSING"></span><span id="error_sxs_file_hash_missing"></span>**FEHLER: \_ \_ SXS-DATEIHASH \_ \_ FEHLT**
</dt> <dd> <dl> <dt>

14110 (0x371E)
</dt> <dt>



Einer Komponente fehlen Dateiüberprüfungsinformationen in ihrem Manifest.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_CHANNEL_PATH"></span><span id="error_evt_invalid_channel_path"></span>**FEHLER \_ EVT \_ UNGÜLTIGER \_ \_ KANALPFAD**
</dt> <dd> <dl> <dt>

15000 (0x3A98)
</dt> <dt>



Der angegebene Kanalpfad ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_QUERY"></span><span id="error_evt_invalid_query"></span>**FEHLER \_ EVT \_ INVALID \_ QUERY**
</dt> <dd> <dl> <dt>

15001 (0x3A99)
</dt> <dt>



Die angegebene Abfrage ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_PUBLISHER_METADATA_NOT_FOUND"></span><span id="error_evt_publisher_metadata_not_found"></span>**FEHLER \_ EVT \_ PUBLISHER METADATA NOT \_ \_ \_ FOUND**
</dt> <dd> <dl> <dt>

15002 (0x3A9A)
</dt> <dt>



Die Herausgebermetadaten können in der Ressource nicht gefunden werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_EVENT_TEMPLATE_NOT_FOUND"></span><span id="error_evt_event_template_not_found"></span>**\_FEHLER: \_ EVT-EREIGNISVORLAGE \_ \_ NICHT \_ GEFUNDEN**
</dt> <dd> <dl> <dt>

15003 (0x3A9B)
</dt> <dt>



Die Vorlage für eine Ereignisdefinition wurde in der Ressource nicht gefunden (Fehler = %1).


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_PUBLISHER_NAME"></span><span id="error_evt_invalid_publisher_name"></span>**FEHLER \_ EVT \_ UNGÜLTIGER \_ \_ HERAUSGEBERNAME**
</dt> <dd> <dl> <dt>

15004 (0x3A9C)
</dt> <dt>



Der angegebene Herausgebername ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_EVENT_DATA"></span><span id="error_evt_invalid_event_data"></span>**FEHLER \_ EVT \_ \_ UNGÜLTIGE \_ EREIGNISDATEN**
</dt> <dd> <dl> <dt>

15005 (0x3A9D)
</dt> <dt>



Die vom Herausgeber ausgelösten Ereignisdaten sind nicht mit der Ereignisvorlagendefinition im Manifest des Herausgebers kompatibel.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_CHANNEL_NOT_FOUND"></span><span id="error_evt_channel_not_found"></span>**\_FEHLER: \_ EVT-KANAL \_ NICHT \_ GEFUNDEN**
</dt> <dd> <dl> <dt>

15007 (0x3A9F)
</dt> <dt>



Der angegebene Kanal wurde nicht gefunden. Überprüfen Sie die Kanalkonfiguration.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_MALFORMED_XML_TEXT"></span><span id="error_evt_malformed_xml_text"></span>**FEHLER \_ EVT \_ MALFORMED \_ XML \_ TEXT**
</dt> <dd> <dl> <dt>

15008 (0x3AA0)
</dt> <dt>



Der angegebene XML-Text war nicht wohlgeformt. Weitere Informationen finden Sie unter Erweiterter Fehler.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_SUBSCRIPTION_TO_DIRECT_CHANNEL"></span><span id="error_evt_subscription_to_direct_channel"></span>**\_FEHLER: \_ EVT-ABONNEMENT \_ FÜR DIREKTEN \_ \_ KANAL**
</dt> <dd> <dl> <dt>

15009 (0x3AA1)
</dt> <dt>



Der Aufrufer versucht, einen direkten Kanal zu abonnieren, was nicht zulässig ist. Die Ereignisse für einen direkten Kanal werden direkt in eine Protokolldatei übertragen und können nicht abonniert werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_CONFIGURATION_ERROR"></span><span id="error_evt_configuration_error"></span>**FEHLER \_ BEI \_ EVT-KONFIGURATIONSFEHLER \_**
</dt> <dd> <dl> <dt>

15010 (0x3AA2)
</dt> <dt>



Konfigurationsfehler.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_QUERY_RESULT_STALE"></span><span id="error_evt_query_result_stale"></span>**FEHLER \_ EVT \_ QUERY RESULT \_ \_ STALE**
</dt> <dd> <dl> <dt>

15011 (0x3AA3)
</dt> <dt>



Das Abfrageergebnis ist veraltet/ungültig. Dies kann daran liegt, dass das Protokoll gelöscht oder ein Rollback nach dem Erstellen des Abfrageergebnisses erfolgt ist. Benutzer sollten diesen Code verarbeiten, indem sie das Abfrageergebnisobjekt freigeben und die Abfrage erneut erstellen.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_QUERY_RESULT_INVALID_POSITION"></span><span id="error_evt_query_result_invalid_position"></span>**\_FEHLER: \_ EVT-ABFRAGEERGEBNIS \_ \_ UNGÜLTIGE \_ POSITION**
</dt> <dd> <dl> <dt>

15012 (0x3AA4)
</dt> <dt>



Das Abfrageergebnis befindet sich derzeit an einer ungültigen Position.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_NON_VALIDATING_MSXML"></span><span id="error_evt_non_validating_msxml"></span>**FEHLER: \_ EVT \_ NICHT \_ ÜBERPRÜFENDER \_ MSXML**
</dt> <dd> <dl> <dt>

15013 (0x3AA5)
</dt> <dt>



Registrierte MSXML unterstützt keine Validierung.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_ALREADYSCOPED"></span><span id="error_evt_filter_alreadyscoped"></span>**FEHLER \_ EVT \_ FILTER \_ ALREADYSCOPED**
</dt> <dd> <dl> <dt>

15014 (0x3AA6)
</dt> <dt>



Auf einen Ausdruck kann nur dann eine Änderung des Bereichsvorgangs folgen, wenn er selbst zu einem Knotensatz ausgewertet wird und nicht bereits Teil einer anderen Änderung des Bereichsvorgangs ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_NOTELTSET"></span><span id="error_evt_filter_noteltset"></span>**FEHLER \_ EVT \_ FILTER \_ NOTELTSET**
</dt> <dd> <dl> <dt>

15015 (0x3AA7)
</dt> <dt>



Ein Schrittvorgang kann nicht aus einem Begriff ausgeführt werden, der keinen Elementsatz darstellt.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_INVARG"></span><span id="error_evt_filter_invarg"></span>**\_FEHLER: \_ EVT-FILTER \_ INVARG**
</dt> <dd> <dl> <dt>

15016 (0x3AA8)
</dt> <dt>



Linksseitige Argumente für binäre Operatoren müssen Attribute, Knoten oder Variablen sein, und rechte Argumente müssen Konstanten sein.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_INVTEST"></span><span id="error_evt_filter_invtest"></span>**\_FEHLER: \_ EVT-FILTER \_ INVTEST**
</dt> <dd> <dl> <dt>

15017 (0x3AA9)
</dt> <dt>



Ein Schrittvorgang muss entweder einen Knotentest umfassen, oder im Fall eines Prädikats kann ein algebraischer Ausdruck ausgewertet werden, mit dem jeder Knoten in der durch den vorausgehenden Knotensatz identifizierten Knotenmenge getestet werden kann.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_INVTYPE"></span><span id="error_evt_filter_invtype"></span>**\_FEHLER: \_ EVT-FILTER \_ INVTYPE**
</dt> <dd> <dl> <dt>

15018 (0x3AAA)
</dt> <dt>



Dieser Datentyp wird derzeit nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_PARSEERR"></span><span id="error_evt_filter_parseerr"></span>**\_FEHLER: \_ EVT-FILTERPARSER \_**
</dt> <dd> <dl> <dt>

15019 (0x3AAB)
</dt> <dt>



An Position %1!d! ist ein Syntaxfehler aufgetreten.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_UNSUPPORTEDOP"></span><span id="error_evt_filter_unsupportedop"></span>**FEHLER \_ EVT \_ FILTER \_ UNSUPPORTEDOP**
</dt> <dd> <dl> <dt>

15020 (0x3AAC)
</dt> <dt>



Dieser Operator wird von dieser Implementierung des Filters nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_UNEXPECTEDTOKEN"></span><span id="error_evt_filter_unexpectedtoken"></span>**ERROR \_ EVT \_ FILTER \_ UNEXPECTEDTOKEN**
</dt> <dd> <dl> <dt>

15021 (0x3AAD)
</dt> <dt>



Das gefundene Token war unerwartet.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_OPERATION_OVER_ENABLED_DIRECT_CHANNEL"></span><span id="error_evt_invalid_operation_over_enabled_direct_channel"></span>**\_FEHLER: \_ UNGÜLTIGER \_ EVT-VORGANG \_ ÜBER \_ \_ AKTIVIERTEN DIREKTEN \_ KANAL**
</dt> <dd> <dl> <dt>

15022 (0x3AAE)
</dt> <dt>



Der angeforderte Vorgang kann nicht über einen aktivierten direkten Kanal ausgeführt werden. Der Kanal muss zuerst deaktiviert werden, bevor der angeforderte Vorgang ausgeführt wird.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_CHANNEL_PROPERTY_VALUE"></span><span id="error_evt_invalid_channel_property_value"></span>**FEHLER \_ EVT \_ UNGÜLTIGER \_ \_ \_ KANALEIGENSCHAFTSWERT**
</dt> <dd> <dl> <dt>

15023 (0x3AAF)
</dt> <dt>



Channeleigenschaft %1!s! enthält einen ungültigen Wert. Der Wert weist einen ungültigen Typ auf, liegt außerhalb des gültigen Bereichs, kann nicht aktualisiert werden oder wird von diesem Kanaltyp nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_PUBLISHER_PROPERTY_VALUE"></span><span id="error_evt_invalid_publisher_property_value"></span>**FEHLER \_ EVT \_ UNGÜLTIGER \_ \_ \_ VERLEGEREIGENSCHAFTSWERT**
</dt> <dd> <dl> <dt>

15024 (0x3AB0)
</dt> <dt>



Publisher %1!s! enthält einen ungültigen Wert. Der Wert hat einen ungültigen Typ, liegt außerhalb des gültigen Bereichs, kann nicht aktualisiert werden oder wird von diesem Herausgebertyp nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_CHANNEL_CANNOT_ACTIVATE"></span><span id="error_evt_channel_cannot_activate"></span>**\_FEHLER: \_ EVT-KANAL \_ KANN NICHT AKTIVIERT \_ WERDEN**
</dt> <dd> <dl> <dt>

15025 (0x3AB1)
</dt> <dt>



Der Kanal kann nicht aktiviert werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_TOO_COMPLEX"></span><span id="error_evt_filter_too_complex"></span>**FEHLER \_ BEIM \_ EVT-FILTER \_ ZU \_ KOMPLEX**
</dt> <dd> <dl> <dt>

15026 (0x3AB2)
</dt> <dt>



Der xpath-Ausdruck hat die unterstützte Komplexität überschritten. Bitte vereinheitlichen Sie sie, oder teilen Sie sie in zwei oder mehr einfache Ausdrücke auf.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_MESSAGE_NOT_FOUND"></span><span id="error_evt_message_not_found"></span>**FEHLER \_ EVT \_ MESSAGE NOT \_ \_ FOUND**
</dt> <dd> <dl> <dt>

15027 (0x3AB3)
</dt> <dt>



Die Nachrichtenressource ist vorhanden, aber die Nachricht wurde in der Zeichenfolgen-/Meldungstabelle nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_MESSAGE_ID_NOT_FOUND"></span><span id="error_evt_message_id_not_found"></span>**FEHLER \_ EVT \_ MESSAGE ID NOT \_ \_ \_ FOUND**
</dt> <dd> <dl> <dt>

15028 (0x3AB4)
</dt> <dt>



Die Nachrichten-ID für die gewünschte Nachricht wurde nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_UNRESOLVED_VALUE_INSERT"></span><span id="error_evt_unresolved_value_insert"></span>**FEHLER \_ BEIM EINFÜGEN EINES NICHT \_ \_ AUFGELÖSTEN \_ WERTS**
</dt> <dd> <dl> <dt>

15029 (0x3AB5)
</dt> <dt>



Die Ersetzungszeichenfolge für den Einfügeindex (%1) wurde nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_UNRESOLVED_PARAMETER_INSERT"></span><span id="error_evt_unresolved_parameter_insert"></span>**FEHLER \_ BEIM EINFÜGEN DES NICHT \_ \_ AUFGELÖSTEN PARAMETERS \_ EVT**
</dt> <dd> <dl> <dt>

15030 (0x3AB6)
</dt> <dt>



Die Beschreibungszeichenfolge für den Parameterverweis (%1) wurde nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_MAX_INSERTS_REACHED"></span><span id="error_evt_max_inserts_reached"></span>**FEHLER \_ EVT \_ MAX \_ INSERTS \_ ERREICHT**
</dt> <dd> <dl> <dt>

15031 (0x3AB7)
</dt> <dt>



Die maximale Anzahl von Ersetzungen wurde erreicht.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_EVENT_DEFINITION_NOT_FOUND"></span><span id="error_evt_event_definition_not_found"></span>**FEHLER \_ \_ EVT-EREIGNISDEFINITION \_ \_ NICHT \_ GEFUNDEN**
</dt> <dd> <dl> <dt>

15032 (0x3AB8)
</dt> <dt>



Die Ereignisdefinition wurde für die Ereignis-ID (%1) nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_MESSAGE_LOCALE_NOT_FOUND"></span><span id="error_evt_message_locale_not_found"></span>**FEHLER \_ EVT \_ MESSAGE \_ LOCALE NOT \_ \_ FOUND**
</dt> <dd> <dl> <dt>

15033 (0x3AB9)
</dt> <dt>



Die lokale Ressource für die gewünschte Nachricht ist nicht vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_VERSION_TOO_OLD"></span><span id="error_evt_version_too_old"></span>**FEHLER \_ \_ EVT-VERSION \_ ZU \_ ALT**
</dt> <dd> <dl> <dt>

15034 (0x3ABA)
</dt> <dt>



Die Ressource ist zu alt, um kompatibel zu sein.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_VERSION_TOO_NEW"></span><span id="error_evt_version_too_new"></span>**FEHLER \_ \_ EVT-VERSION \_ ZU \_ NEU**
</dt> <dd> <dl> <dt>

15035 (0x3ABB)
</dt> <dt>



Die Ressource ist zu neu, um kompatibel zu sein.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_CANNOT_OPEN_CHANNEL_OF_QUERY"></span><span id="error_evt_cannot_open_channel_of_query"></span>**FEHLER \_ BEIM ÖFFNEN DES \_ \_ \_ ABFRAGEKANALS \_ DURCH \_ EVT**
</dt> <dd> <dl> <dt>

15036 (0x3ABC)
</dt> <dt>



Der Kanal am Index %1!d! der Abfrage kann nicht geöffnet werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_PUBLISHER_DISABLED"></span><span id="error_evt_publisher_disabled"></span>**FEHLER \_ EVT \_ PUBLISHER \_ DISABLED**
</dt> <dd> <dl> <dt>

15037 (0x3ABD)
</dt> <dt>



Der Herausgeber wurde deaktiviert, und seine Ressource ist nicht verfügbar. Dies tritt in der Regel auf, wenn der Herausgeber gerade deinstalliert oder aktualisiert wird.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_OUT_OF_RANGE"></span><span id="error_evt_filter_out_of_range"></span>**FEHLER \_ EVT \_ FILTER OUT OF \_ \_ \_ RANGE**
</dt> <dd> <dl> <dt>

15038 (0x3ABE)
</dt> <dt>



Es wurde versucht, einen numerischen Typ zu erstellen, der sich außerhalb seines gültigen Bereichs befindet.


</dt> </dl> </dd> <dt>

<span id="ERROR_EC_SUBSCRIPTION_CANNOT_ACTIVATE"></span><span id="error_ec_subscription_cannot_activate"></span>**FEHLER: \_ \_ EC-ABONNEMENT \_ KANN NICHT AKTIVIERT \_ WERDEN**
</dt> <dd> <dl> <dt>

15080 (0x3AE8)
</dt> <dt>



Das Abonnement kann nicht aktiviert werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_EC_LOG_DISABLED"></span><span id="error_ec_log_disabled"></span>**FEHLER \_ EC \_ LOG \_ DISABLED**
</dt> <dd> <dl> <dt>

15081 (0x3AE9)
</dt> <dt>



Das Protokoll des Abonnements befindet sich im Deaktiviert-Zustand und kann nicht zum Weitergeleitet von Ereignissen verwendet werden. Das Protokoll muss zuerst aktiviert werden, bevor das Abonnement aktiviert werden kann.


</dt> </dl> </dd> <dt>

<span id="ERROR_EC_CIRCULAR_FORWARDING"></span><span id="error_ec_circular_forwarding"></span>**FEHLER BEI \_ \_ EC-ZIRKELWEITERLEITUNG \_**
</dt> <dd> <dl> <dt>

15082 (0x3AEA)
</dt> <dt>



Beim Weiterleiten von Ereignissen vom lokalen Computer an sich selbst darf die Abfrage des Abonnements kein Zielprotokoll des Abonnements enthalten.


</dt> </dl> </dd> <dt>

<span id="ERROR_EC_CREDSTORE_FULL"></span><span id="error_ec_credstore_full"></span>**FEHLER \_ EC \_ CREDSTORE \_ FULL**
</dt> <dd> <dl> <dt>

15083 (0x3AEB)
</dt> <dt>



Der Anmeldeinformationsspeicher, der zum Speichern von Anmeldeinformationen verwendet wird, ist voll.


</dt> </dl> </dd> <dt>

<span id="ERROR_EC_CRED_NOT_FOUND"></span><span id="error_ec_cred_not_found"></span>**FEHLER \_ EC \_ CRED NOT \_ \_ FOUND**
</dt> <dd> <dl> <dt>

15084 (0x3AEC)
</dt> <dt>



Die von diesem Abonnement verwendeten Anmeldeinformationen finden Sie nicht im Anmeldeinformationsspeicher.


</dt> </dl> </dd> <dt>

<span id="ERROR_EC_NO_ACTIVE_CHANNEL"></span><span id="error_ec_no_active_channel"></span>**FEHLER \_ EC NO ACTIVE \_ \_ \_ CHANNEL**
</dt> <dd> <dl> <dt>

15085 (0x3AED)
</dt> <dt>



Für die Abfrage wurde kein aktiver Kanal gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_MUI_FILE_NOT_FOUND"></span><span id="error_mui_file_not_found"></span>**FEHLER: \_ \_ DATEI "ERROR" WURDE NICHT \_ \_ GEFUNDEN.**
</dt> <dd> <dl> <dt>

15100 (0x3AFC)
</dt> <dt>



Fehler beim Ressourcenlader beim Suchen nach DER DATEI.


</dt> </dl> </dd> <dt>

<span id="ERROR_MUI_INVALID_FILE"></span><span id="error_mui_invalid_file"></span>**ERROR \_ MUI \_ INVALID \_ FILE**
</dt> <dd> <dl> <dt>

15101 (0x3AFD)
</dt> <dt>



Fehler beim Laden der LOAD-Datei durch das Ressourcenlader, da die Datei die Überprüfung nicht bestehen konnte.


</dt> </dl> </dd> <dt>

<span id="ERROR_MUI_INVALID_RC_CONFIG"></span><span id="error_mui_invalid_rc_config"></span>**\_FEHLER: \_ \_ UNGÜLTIGE \_ RC-KONFIGURATION**
</dt> <dd> <dl> <dt>

15102 (0x3AFE)
</dt> <dt>



Das RC-Manifest ist mit Garbage Data, einer nicht unterstützten Version oder einem fehlenden erforderlichen Element beschädigt.


</dt> </dl> </dd> <dt>

<span id="ERROR_MUI_INVALID_LOCALE_NAME"></span><span id="error_mui_invalid_locale_name"></span>**\_FEHLER: \_ \_ UNGÜLTIGER \_ LOCALE-NAME**
</dt> <dd> <dl> <dt>

15103 (0x3AFF)
</dt> <dt>



Das RC-Manifest hat einen ungültigen Kulturnamen.


</dt> </dl> </dd> <dt>

<span id="ERROR_MUI_INVALID_ULTIMATEFALLBACK_NAME"></span><span id="error_mui_invalid_ultimatefallback_name"></span>**FEHLER \_ INVALID \_ \_ ULTIMATEFALLBACK \_ NAME**
</dt> <dd> <dl> <dt>

15104 (0x3B00)
</dt> <dt>



Das RC-Manifest hat einen ungültigen ultimatefallback-Namen.


</dt> </dl> </dd> <dt>

<span id="ERROR_MUI_FILE_NOT_LOADED"></span><span id="error_mui_file_not_loaded"></span>**FEHLER: \_ DIE DATEI WURDE NICHT \_ \_ \_ GELADEN.**
</dt> <dd> <dl> <dt>

15105 (0x3B01)
</dt> <dt>



Der RESSOURCENLADER-Cache hat den EINTRAG ZUM LADEN NICHT geladen.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_ENUM_USER_STOP"></span><span id="error_resource_enum_user_stop"></span>**FEHLER: \_ \_ RESSOURCEN-ENUMER \_ \_ BENUTZERSTOPP**
</dt> <dd> <dl> <dt>

15106 (0x3B02)
</dt> <dt>



Die Ressourcenenumeration wurde vom Benutzer beendet.


</dt> </dl> </dd> <dt>

<span id="ERROR_MUI_INTLSETTINGS_UILANG_NOT_INSTALLED"></span><span id="error_mui_intlsettings_uilang_not_installed"></span>**FEHLER: \_ \_ INTLSETTINGS \_ UILANG \_ NICHT \_ INSTALLIERT**
</dt> <dd> <dl> <dt>

15107 (0x3B03)
</dt> <dt>



Fehler bei der Installation der Benutzeroberflächensprache.


</dt> </dl> </dd> <dt>

<span id="ERROR_MUI_INTLSETTINGS_INVALID_LOCALE_NAME"></span><span id="error_mui_intlsettings_invalid_locale_name"></span>**FEHLER \_ \_ INTLSETTINGS \_ \_ UNGÜLTIGER \_ LOCALE-NAME**
</dt> <dd> <dl> <dt>

15108 (0x3B04)
</dt> <dt>



Fehler bei der Locale-Installation.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_RUNTIME_NO_DEFAULT_OR_NEUTRAL_RESOURCE"></span><span id="error_mrm_runtime_no_default_or_neutral_resource"></span>**FEHLER: \_ MRM \_ RUNTIME KEINE \_ \_ \_ STANDARDRESSOURCE \_ ODER NEUTRALE \_ RESSOURCE**
</dt> <dd> <dl> <dt>

15110 (0x3B06)
</dt> <dt>



Eine Ressource hat keinen Standardwert oder neutralen Wert.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_INVALID_PRICONFIG"></span><span id="error_mrm_invalid_priconfig"></span>**FEHLER: \_ MRM \_ INVALID \_ PRICONFIG**
</dt> <dd> <dl> <dt>

15111 (0x3B07)
</dt> <dt>



Ungültige PRI-Konfigurationsdatei.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_INVALID_FILE_TYPE"></span><span id="error_mrm_invalid_file_type"></span>**\_FEHLER: \_ UNGÜLTIGER \_ MRM-DATEITYP \_**
</dt> <dd> <dl> <dt>

15112 (0x3B08)
</dt> <dt>



Ungültiger Dateityp.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_UNKNOWN_QUALIFIER"></span><span id="error_mrm_unknown_qualifier"></span>**\_FEHLER: \_ UNBEKANNTER \_ MRM-QUALIFIZIERER**
</dt> <dd> <dl> <dt>

15113 (0x3B09)
</dt> <dt>



Unbekannter Qualifizierer.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_INVALID_QUALIFIER_VALUE"></span><span id="error_mrm_invalid_qualifier_value"></span>**FEHLER \_ MRM \_ \_ UNGÜLTIGER \_ QUALIFIZIERERWERT**
</dt> <dd> <dl> <dt>

15114 (0x3B0A)
</dt> <dt>



Ungültiger Qualifiziererwert.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_NO_CANDIDATE"></span><span id="error_mrm_no_candidate"></span>**FEHLER \_ MRM \_ NO \_ CANDIDATE**
</dt> <dd> <dl> <dt>

15115 (0x3B0B)
</dt> <dt>



Es wurde kein Kandidat gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_NO_MATCH_OR_DEFAULT_CANDIDATE"></span><span id="error_mrm_no_match_or_default_candidate"></span>**FEHLER \_ \_ MRM: KEINE ÜBEREINSTIMMUNG ODER \_ \_ \_ \_ STANDARDKANDIDAT**
</dt> <dd> <dl> <dt>

15116 (0x3B0C)
</dt> <dt>



ResourceMap oder NamedResource verfügt über ein Element, das keine Standardressource oder neutrale Ressource enthält.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_RESOURCE_TYPE_MISMATCH"></span><span id="error_mrm_resource_type_mismatch"></span>**FEHLER: \_ \_ \_ \_ MRM-RESSOURCENTYPKONFLIKT**
</dt> <dd> <dl> <dt>

15117 (0x3B0D)
</dt> <dt>



Ungültiger ResourceCandidate-Typ.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_DUPLICATE_MAP_NAME"></span><span id="error_mrm_duplicate_map_name"></span>**FEHLER \_ MRM \_ DUPLICATE MAP \_ \_ NAME**
</dt> <dd> <dl> <dt>

15118 (0x3B0E)
</dt> <dt>



Doppelte Ressourcenzuordnung.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_DUPLICATE_ENTRY"></span><span id="error_mrm_duplicate_entry"></span>**\_FEHLER: \_ MRM- DOPPELTER \_ EINTRAG**
</dt> <dd> <dl> <dt>

15119 (0x3B0F)
</dt> <dt>



Doppelter Eintrag.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_INVALID_RESOURCE_IDENTIFIER"></span><span id="error_mrm_invalid_resource_identifier"></span>**FEHLER \_ \_ MRM: UNGÜLTIGER \_ \_ RESSOURCENBEZEICHNER**
</dt> <dd> <dl> <dt>

15120 (0x3B10)
</dt> <dt>



Ungültiger Ressourcenbezeichner.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_FILEPATH_TOO_LONG"></span><span id="error_mrm_filepath_too_long"></span>**\_FEHLER: \_ MRM-DATEIPFAD \_ ZU \_ LANG**
</dt> <dd> <dl> <dt>

15121 (0x3B11)
</dt> <dt>



Dateipfad zu lang.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_UNSUPPORTED_DIRECTORY_TYPE"></span><span id="error_mrm_unsupported_directory_type"></span>**\_FEHLER: \_ NICHT UNTERSTÜTZTER \_ MRM-VERZEICHNISTYP \_**
</dt> <dd> <dl> <dt>

15122 (0x3B12)
</dt> <dt>



Nicht unterstützter Verzeichnistyp.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_INVALID_PRI_FILE"></span><span id="error_mrm_invalid_pri_file"></span>**FEHLER \_ MRM \_ \_ UNGÜLTIGE \_ PRI-DATEI**
</dt> <dd> <dl> <dt>

15126 (0x3B16)
</dt> <dt>



Ungültige PRI-Datei.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_NAMED_RESOURCE_NOT_FOUND"></span><span id="error_mrm_named_resource_not_found"></span>**FEHLER \_ MRM \_ NAMENS RESSOURCE NICHT \_ \_ \_ GEFUNDEN**
</dt> <dd> <dl> <dt>

15127 (0x3B17)
</dt> <dt>



NamedResource nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_MAP_NOT_FOUND"></span><span id="error_mrm_map_not_found"></span>**\_FEHLER: \_ MRM-ZUORDNUNG \_ NICHT \_ GEFUNDEN**
</dt> <dd> <dl> <dt>

15135 (0x3B1F)
</dt> <dt>



ResourceMap nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_UNSUPPORTED_PROFILE_TYPE"></span><span id="error_mrm_unsupported_profile_type"></span>**\_FEHLER: \_ NICHT UNTERSTÜTZTER \_ MRM-PROFILTYP \_**
</dt> <dd> <dl> <dt>

15136 (0x3B20)
</dt> <dt>



Nicht unterstützter MRT-Profiltyp.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_INVALID_QUALIFIER_OPERATOR"></span><span id="error_mrm_invalid_qualifier_operator"></span>**\_FEHLER: \_ UNGÜLTIGER \_ MRM-QUALIFIZIEREROPERATOR \_**
</dt> <dd> <dl> <dt>

15137 (0x3B21)
</dt> <dt>



Ungültiger Qualifiziereroperator.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_INDETERMINATE_QUALIFIER_VALUE"></span><span id="error_mrm_indeterminate_qualifier_value"></span>**ERROR \_ MRM \_ INDETERMINATE \_ QUALIFIER \_ VALUE**
</dt> <dd> <dl> <dt>

15138 (0x3B22)
</dt> <dt>



Der Qualifiziererwert kann nicht bestimmt werden, oder der Qualifiziererwert wurde nicht festgelegt.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_AUTOMERGE_ENABLED"></span><span id="error_mrm_automerge_enabled"></span>**FEHLER \_ MRM \_ AUTOMERGE \_ AKTIVIERT**
</dt> <dd> <dl> <dt>

15139 (0x3B23)
</dt> <dt>



Automerge ist in der PRI-Datei aktiviert.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_TOO_MANY_RESOURCES"></span><span id="error_mrm_too_many_resources"></span>**FEHLER: \_ MRM \_ ZU VIELE \_ \_ RESSOURCEN**
</dt> <dd> <dl> <dt>

15140 (0x3B24)
</dt> <dt>



Zu viele ressourcendefiniert für das Paket.


</dt> </dl> </dd> <dt>

<span id="ERROR_MCA_INVALID_CAPABILITIES_STRING"></span><span id="error_mca_invalid_capabilities_string"></span>**ERROR \_ MCA \_ INVALID \_ CAPABILITIES \_ STRING**
</dt> <dd> <dl> <dt>

15200 (0x3B60)
</dt> <dt>



Der Monitor hat eine DDC/CI-Funktionenzeichenfolge zurückgegeben, die nicht der SPEZIFIKATION ACCESS.bus 3.0, DDC/CI 1.1 oder MCCS 2 Revision 1 entspricht.


</dt> </dl> </dd> <dt>

<span id="ERROR_MCA_INVALID_VCP_VERSION"></span><span id="error_mca_invalid_vcp_version"></span>**FEHLER \_ MCA \_ INVALID \_ VCP \_ VERSION**
</dt> <dd> <dl> <dt>

15201 (0x3B61)
</dt> <dt>



Der VCP-Version (0xDF) des Monitors hat einen ungültigen Versionswert zurückgegeben.


</dt> </dl> </dd> <dt>

<span id="ERROR_MCA_MONITOR_VIOLATES_MCCS_SPECIFICATION"></span><span id="error_mca_monitor_violates_mccs_specification"></span>**FEHLER \_ MCA \_ MONITOR VERLETZT \_ \_ \_ MCCS-SPEZIFIKATION**
</dt> <dd> <dl> <dt>

15202 (0x3B62)
</dt> <dt>



Der Monitor entspricht nicht der MCCS-Spezifikation, die er unterstützt.


</dt> </dl> </dd> <dt>

<span id="ERROR_MCA_MCCS_VERSION_MISMATCH"></span><span id="error_mca_mccs_version_mismatch"></span>**FEHLER: \_ MCA \_ \_ MCCS-VERSIONSKONFLIKT \_**
</dt> <dd> <dl> <dt>

15203 (0x3B63)
</dt> <dt>



Die MCCS-Version in der \_ McCS-Ver-Funktion eines Monitors stimmt nicht mit der MCCS-Version überein, die der Monitor meldet, wenn der VCP-Code der VCP-Version (0xDF) verwendet wird.


</dt> </dl> </dd> <dt>

<span id="ERROR_MCA_UNSUPPORTED_MCCS_VERSION"></span><span id="error_mca_unsupported_mccs_version"></span>**FEHLER \_ MCA \_ NICHT UNTERSTÜTZTE \_ MCCS-VERSION \_**
</dt> <dd> <dl> <dt>

15204 (0x3B64)
</dt> <dt>



Die Überwachungskonfigurations-API funktioniert nur mit Monitoren, die die MCCS 1.0-, MCCS 2.0- oder MCCS 2.0 Revision 1-Spezifikation unterstützen.


</dt> </dl> </dd> <dt>

<span id="ERROR_MCA_INTERNAL_ERROR"></span><span id="error_mca_internal_error"></span>**INTERNER \_ \_ MCA-FEHLER \_**
</dt> <dd> <dl> <dt>

15205 (0x3B65)
</dt> <dt>



Interner Fehler bei der Überwachungskonfigurations-API.


</dt> </dl> </dd> <dt>

<span id="ERROR_MCA_INVALID_TECHNOLOGY_TYPE_RETURNED"></span><span id="error_mca_invalid_technology_type_returned"></span>**FEHLER \_ MCA \_ UNGÜLTIGER \_ \_ TECHNOLOGIETYP \_ ZURÜCKGEGEBEN**
</dt> <dd> <dl> <dt>

15206 (0x3B66)
</dt> <dt>



Der Monitor hat einen ungültigen Überwachungstechnologietyp zurückgegeben. CRT, Soll und CSV (TFT) sind Beispiele für Überwachungstechnologietypen. Dieser Fehler impliziert, dass der Monitor gegen die MCCS 2.0- oder MCCS 2.0 Revision 1-Spezifikation verstoßen hat.


</dt> </dl> </dd> <dt>

<span id="ERROR_MCA_UNSUPPORTED_COLOR_TEMPERATURE"></span><span id="error_mca_unsupported_color_temperature"></span>**FEHLER \_ \_ MCA– NICHT UNTERSTÜTZTE \_ \_ FARBTEMPERATUR**
</dt> <dd> <dl> <dt>

15207 (0x3B67)
</dt> <dt>



Der Aufrufer von [**SetMonitorColorTemperature**](/windows/win32/api/highlevelmonitorconfigurationapi/nf-highlevelmonitorconfigurationapi-setmonitorcolortemperature) hat eine Farbtemperatur angegeben, die vom aktuellen Monitor nicht unterstützt wurde. Dieser Fehler impliziert, dass der Monitor gegen die MCCS 2.0- oder MCCS 2.0 Revision 1-Spezifikation verstoßen hat.


</dt> </dl> </dd> <dt>

<span id="ERROR_AMBIGUOUS_SYSTEM_DEVICE"></span><span id="error_ambiguous_system_device"></span>**FEHLER \_ \_ MEHRDEUTIGES \_ SYSTEMGERÄT**
</dt> <dd> <dl> <dt>

15250 (0x3B92)
</dt> <dt>



Das angeforderte Systemgerät kann nicht identifiziert werden, weil mehrere nicht unterscheidbare Geräte möglicherweise den Identifikationskriterien entsprechen.


</dt> </dl> </dd> <dt>

<span id="ERROR_SYSTEM_DEVICE_NOT_FOUND"></span><span id="error_system_device_not_found"></span>**FEHLER: \_ \_ SYSTEMGERÄT \_ NICHT \_ GEFUNDEN**
</dt> <dd> <dl> <dt>

15299 (0x3BC3)
</dt> <dt>



Das angeforderte Systemgerät wurde nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_HASH_NOT_SUPPORTED"></span><span id="error_hash_not_supported"></span>**\_FEHLERHASH \_ WIRD NICHT \_ UNTERSTÜTZT**
</dt> <dd> <dl> <dt>

15300 (0x3BC4)
</dt> <dt>



Die Hashgenerierung für die angegebene Hashversion und den Hashtyp ist auf dem Server nicht aktiviert.


</dt> </dl> </dd> <dt>

<span id="ERROR_HASH_NOT_PRESENT"></span><span id="error_hash_not_present"></span>**\_FEHLERHASH \_ NICHT \_ VORHANDEN**
</dt> <dd> <dl> <dt>

15301 (0x3BC5)
</dt> <dt>



Der vom Server angeforderte Hash ist nicht verfügbar oder nicht mehr gültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_SECONDARY_IC_PROVIDER_NOT_REGISTERED"></span><span id="error_secondary_ic_provider_not_registered"></span>**FEHLER \_ SEKUNDÄRER \_ \_ IC-ANBIETER \_ NICHT \_ REGISTRIERT**
</dt> <dd> <dl> <dt>

15321 (0x3BD9)
</dt> <dt>



Die sekundäre Interruptcontrollerinstanz, die den angegebenen Interrupt verwaltet, ist nicht registriert.


</dt> </dl> </dd> <dt>

<span id="ERROR_GPIO_CLIENT_INFORMATION_INVALID"></span><span id="error_gpio_client_information_invalid"></span>**FEHLER: \_ \_ GPIO-CLIENTINFORMATIONEN \_ \_ UNGÜLTIG**
</dt> <dd> <dl> <dt>

15322 (0x3BDA)
</dt> <dt>



Die vom GPIO-Clienttreiber bereitgestellten Informationen sind ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_GPIO_VERSION_NOT_SUPPORTED"></span><span id="error_gpio_version_not_supported"></span>**FEHLER \_ \_ GPIO-VERSION \_ NICHT \_ UNTERSTÜTZT**
</dt> <dd> <dl> <dt>

15323 (0x3BDB)
</dt> <dt>



Die vom GPIO-Clienttreiber angegebene Version wird nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="ERROR_GPIO_INVALID_REGISTRATION_PACKET"></span><span id="error_gpio_invalid_registration_packet"></span>**FEHLER: \_ \_ GPIO: UNGÜLTIGES \_ \_ REGISTRIERUNGSPAKET**
</dt> <dd> <dl> <dt>

15324 (0x3BDC)
</dt> <dt>



Das vom GPIO-Clienttreiber bereitgestellte Registrierungspaket ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_GPIO_OPERATION_DENIED"></span><span id="error_gpio_operation_denied"></span>**\_FEHLER: \_ GPIO-VORGANG \_ VERWEIGERT**
</dt> <dd> <dl> <dt>

15325 (0x3BDD)
</dt> <dt>



Der angeforderte Vorgang wird für das angegebene Handle nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="ERROR_GPIO_INCOMPATIBLE_CONNECT_MODE"></span><span id="error_gpio_incompatible_connect_mode"></span>**FEHLER: \_ INKOMPATIBLER \_ GPIO-VERBINDUNGSMODUS \_ \_**
</dt> <dd> <dl> <dt>

15326 (0x3BDE)
</dt> <dt>



Der angeforderte Verbindungsmodus steht in Konflikt mit einem vorhandenen Modus auf mindestens einem der angegebenen Pins.


</dt> </dl> </dd> <dt>

<span id="ERROR_GPIO_INTERRUPT_ALREADY_UNMASKED"></span><span id="error_gpio_interrupt_already_unmasked"></span>**FEHLER \_ GPIO \_ INTERRUPT ALREADY \_ \_ UNMASKED**
</dt> <dd> <dl> <dt>

15327 (0x3BDF)
</dt> <dt>



Der Interrupt, für den die Maskierung angefordert wird, wird nicht maskiert.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_SWITCH_RUNLEVEL"></span><span id="error_cannot_switch_runlevel"></span>**FEHLER: \_ \_ RUNLEVEL KANN \_ NICHT UMGESCHALTET WERDEN**
</dt> <dd> <dl> <dt>

15400 (0x3C28)
</dt> <dt>



Der angeforderte Switch auf Ausführungsebene kann nicht erfolgreich abgeschlossen werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_RUNLEVEL_SETTING"></span><span id="error_invalid_runlevel_setting"></span>**FEHLER: \_ \_ UNGÜLTIGE RUNLEVEL-EINSTELLUNG \_**
</dt> <dd> <dl> <dt>

15401 (0x3C29)
</dt> <dt>



Der Dienst verfügt über eine ungültige Einstellung für die Ausführungsebene. Die Ausführungsebene für einen Dienst darf nicht höher als die Ausführungsebene der abhängigen Dienste sein.


</dt> </dl> </dd> <dt>

<span id="ERROR_RUNLEVEL_SWITCH_TIMEOUT"></span><span id="error_runlevel_switch_timeout"></span>**\_FEHLER: \_ RUNLEVEL-SWITCH-TIMEOUT \_**
</dt> <dd> <dl> <dt>

15402 (0x3C2A)
</dt> <dt>



Der angeforderte Switch auf Ausführungsebene kann nicht erfolgreich abgeschlossen werden, da mindestens ein Dienst innerhalb des angegebenen Timeouts nicht beendet oder neu gestartet wird.


</dt> </dl> </dd> <dt>

<span id="ERROR_RUNLEVEL_SWITCH_AGENT_TIMEOUT"></span><span id="error_runlevel_switch_agent_timeout"></span>**FEHLER: \_ RUNLEVEL \_ SWITCH AGENT \_ \_ TIMEOUT**
</dt> <dd> <dl> <dt>

15403 (0x3C2B)
</dt> <dt>



Ein Switch-Agent auf Ausführungsebene hat nicht innerhalb des angegebenen Timeouts reagiert.


</dt> </dl> </dd> <dt>

<span id="ERROR_RUNLEVEL_SWITCH_IN_PROGRESS"></span><span id="error_runlevel_switch_in_progress"></span>**FEHLER \_ BEIM \_ RUNLEVEL-SWITCH \_ IN \_ BEARBEITUNG**
</dt> <dd> <dl> <dt>

15404 (0x3C2C)
</dt> <dt>



Derzeit wird ein Switch auf Ausführungsebene ausgeführt.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICES_FAILED_AUTOSTART"></span><span id="error_services_failed_autostart"></span>**FEHLER \_ BEIM \_ AUTOMATISCHEN START VON \_ DIENSTEN**
</dt> <dd> <dl> <dt>

15405 (0x3C2D)
</dt> <dt>



Mindestens ein Dienst konnte während der Dienststartphase eines Switches auf Ausführungsebene nicht gestartet werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_COM_TASK_STOP_PENDING"></span><span id="error_com_task_stop_pending"></span>**FEHLER \_ COM TASK STOP \_ \_ \_ PENDING**
</dt> <dd> <dl> <dt>

15501 (0x3C8D)
</dt> <dt>



Die Anforderung zum Beenden der Aufgabe kann nicht sofort abgeschlossen werden, da der Task mehr Zeit zum Herunterfahren benötigt.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_OPEN_PACKAGE_FAILED"></span><span id="error_install_open_package_failed"></span>**FEHLER BEIM \_ INSTALLIEREN \_ DES \_ GEÖFFNETEN \_ PAKETS**
</dt> <dd> <dl> <dt>

15600 (0x3CF0)
</dt> <dt>



Das Paket konnte nicht geöffnet werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_PACKAGE_NOT_FOUND"></span><span id="error_install_package_not_found"></span>**FEHLER \_ BEIM INSTALLIEREN DES \_ \_ PAKETS WURDE NICHT \_ GEFUNDEN**
</dt> <dd> <dl> <dt>

15601 (0x3CF1)
</dt> <dt>



Das Paket wurde nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_INVALID_PACKAGE"></span><span id="error_install_invalid_package"></span>**FEHLER \_ BEIM INSTALLIEREN EINES \_ UNGÜLTIGEN \_ PAKETS**
</dt> <dd> <dl> <dt>

15602 (0x3CF2)
</dt> <dt>



Paketdaten sind ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_RESOLVE_DEPENDENCY_FAILED"></span><span id="error_install_resolve_dependency_failed"></span>**FEHLER BEI \_ DER INSTALLATION \_ DES \_ FEHLERS FEHLER BEIM AUFLÖSEN DER \_ ABHÄNGIGKEIT.**
</dt> <dd> <dl> <dt>

15603 (0x3CF3)
</dt> <dt>



Paket mit fehlerhaften Updates, Abhängigkeits- oder Konfliktvalidierung.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_OUT_OF_DISK_SPACE"></span><span id="error_install_out_of_disk_space"></span>**FEHLER \_ BEI DER INSTALLATION DES \_ \_ \_ SPEICHERPLATZES AUF DEM \_ DATENTRÄGER**
</dt> <dd> <dl> <dt>

15604 (0x3CF4)
</dt> <dt>



Auf ihrem Computer ist nicht genügend Speicherplatz vorhanden. Geben Sie Speicherplatz frei, und versuchen Sie es erneut.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_NETWORK_FAILURE"></span><span id="error_install_network_failure"></span>**FEHLER BEIM \_ INSTALLIEREN \_ EINES \_ NETZWERKFEHLERS**
</dt> <dd> <dl> <dt>

15605 (0x3CF5)
</dt> <dt>



Beim Herunterladen Ihres Produkts ist ein Problem vor worden.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_REGISTRATION_FAILURE"></span><span id="error_install_registration_failure"></span>**FEHLER BEIM \_ INSTALLIEREN \_ DES \_ REGISTRIERUNGSFEHLERS**
</dt> <dd> <dl> <dt>

15606 (0x3CF6)
</dt> <dt>



Das Paket konnte nicht registriert werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_DEREGISTRATION_FAILURE"></span><span id="error_install_deregistration_failure"></span>**FEHLER \_ BEIM INSTALLIEREN DES \_ \_ REGISTRIERUNGSFEHLERS**
</dt> <dd> <dl> <dt>

15607 (0x3CF7)
</dt> <dt>



Die Registrierung des Pakets konnte nicht aufgehoben werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_CANCEL"></span><span id="error_install_cancel"></span>**FEHLER BEIM \_ ABBRECHEN \_ DER INSTALLATION**
</dt> <dd> <dl> <dt>

15608 (0x3CF8)
</dt> <dt>



Der Benutzer hat die Installationsanforderung abgebrochen.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_FAILED"></span><span id="error_install_failed"></span>**FEHLER \_ BEI DER \_ INSTALLATION**
</dt> <dd> <dl> <dt>

15609 (0x3CF9)
</dt> <dt>



Fehler bei der Installation. Wenden Sie sich an Ihren Softwarehersteller.


</dt> </dl> </dd> <dt>

<span id="ERROR_REMOVE_FAILED"></span><span id="error_remove_failed"></span>**FEHLER \_ BEIM ENTFERNEN \_**
</dt> <dd> <dl> <dt>

15610 (0x3CFA)
</dt> <dt>



Fehler beim Entfernen. Wenden Sie sich an Ihren Softwarehersteller.


</dt> </dl> </dd> <dt>

<span id="ERROR_PACKAGE_ALREADY_EXISTS"></span><span id="error_package_already_exists"></span>**FEHLERPAKET \_ \_ IST BEREITS \_ VORHANDEN**
</dt> <dd> <dl> <dt>

15611 (0x3CFB)
</dt> <dt>



Das bereitgestellte Paket ist bereits installiert, und die Neuinstallation des Pakets wurde blockiert. Weitere Informationen finden AppXDeployment-Server Ereignisprotokoll.


</dt> </dl> </dd> <dt>

<span id="ERROR_NEEDS_REMEDIATION"></span><span id="error_needs_remediation"></span>**FEHLER \_ MUSS \_ BEHEBT WERDEN**
</dt> <dd> <dl> <dt>

15612 (0x3CFC)
</dt> <dt>



Die Anwendung kann nicht gestartet werden. Versuchen Sie, die Anwendung erneut zu installieren, um das Problem zu beheben.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_PREREQUISITE_FAILED"></span><span id="error_install_prerequisite_failed"></span>**FEHLER BEI \_ FEHLER BEI DER INSTALLATION DER ERFORDERLICHEN \_ \_ KOMPONENTEN**
</dt> <dd> <dl> <dt>

15613 (0x3CFD)
</dt> <dt>



Eine Voraussetzung für eine Installation konnte nicht erfüllt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_PACKAGE_REPOSITORY_CORRUPTED"></span><span id="error_package_repository_corrupted"></span>**\_ \_ \_ FEHLERPAKETREPOSITORY BESCHÄDIGT**
</dt> <dd> <dl> <dt>

15614 (0x3CFE)
</dt> <dt>



Das Paketrepository ist beschädigt.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_POLICY_FAILURE"></span><span id="error_install_policy_failure"></span>**FEHLER BEIM \_ INSTALLIEREN \_ DER \_ RICHTLINIE**
</dt> <dd> <dl> <dt>

15615 (0x3CFF)
</dt> <dt>



Um diese Anwendung zu installieren, benötigen Sie entweder eine Windows-Lizenz oder ein Sideloading-fähiges System.


</dt> </dl> </dd> <dt>

<span id="ERROR_PACKAGE_UPDATING"></span><span id="error_package_updating"></span>**\_ \_ FEHLERPAKETAKTUALISIERUNG**
</dt> <dd> <dl> <dt>

15616 (0x3D00)
</dt> <dt>



Die Anwendung kann nicht gestartet werden, da sie gerade aktualisiert wird.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEPLOYMENT_BLOCKED_BY_POLICY"></span><span id="error_deployment_blocked_by_policy"></span>**FEHLERBEREITSTELLUNG \_ \_ DURCH RICHTLINIE \_ \_ BLOCKIERT**
</dt> <dd> <dl> <dt>

15617 (0x3D01)
</dt> <dt>



Der Paketbereitstellungsvorgang wird durch die Richtlinie blockiert. Wenden Sie sich an den Systemadministrator.


</dt> </dl> </dd> <dt>

<span id="ERROR_PACKAGES_IN_USE"></span><span id="error_packages_in_use"></span>**FEHLERPAKETE \_ \_ IN \_ VERWENDUNG**
</dt> <dd> <dl> <dt>

15618 (0x3D02)
</dt> <dt>



Das Paket konnte nicht installiert werden, da ressourcen, die es ändert, derzeit verwendet werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_RECOVERY_FILE_CORRUPT"></span><span id="error_recovery_file_corrupt"></span>**FEHLER: \_ \_ WIEDERHERSTELLUNGSDATEI \_ BESCHÄDIGT**
</dt> <dd> <dl> <dt>

15619 (0x3D03)
</dt> <dt>



Das Paket konnte nicht wiederhergestellt werden, da die für die Wiederherstellung erforderlichen Daten beschädigt wurden.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_STAGED_SIGNATURE"></span><span id="error_invalid_staged_signature"></span>**FEHLER: \_ \_ UNGÜLTIGE GE STAGED \_ SIGNATURE**
</dt> <dd> <dl> <dt>

15620 (0x3D04)
</dt> <dt>



Die Signatur ist ungültig. Für die Registrierung im Entwicklermodus müssen AppxSignature.p7x und AppxBlockMap.xml gültig sein oder nicht vorhanden sein.


</dt> </dl> </dd> <dt>

<span id="ERROR_DELETING_EXISTING_APPLICATIONDATA_STORE_FAILED"></span><span id="error_deleting_existing_applicationdata_store_failed"></span>**FEHLER BEIM \_ LÖSCHEN \_ DES VORHANDENEN \_ APPLICATIONDATA \_ STORE \_**
</dt> <dd> <dl> <dt>

15621 (0x3D05)
</dt> <dt>



Fehler beim Löschen der zuvor vorhandenen Anwendungsdaten des Pakets.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_PACKAGE_DOWNGRADE"></span><span id="error_install_package_downgrade"></span>**FEHLER \_ BEIM \_ HERABSTUFEN DES \_ INSTALLATIONSPAKETS**
</dt> <dd> <dl> <dt>

15622 (0x3D06)
</dt> <dt>



Das Paket konnte nicht installiert werden, da bereits eine höhere Version dieses Pakets installiert ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_SYSTEM_NEEDS_REMEDIATION"></span><span id="error_system_needs_remediation"></span>**FEHLERSYSTEM \_ \_ MUSS \_ ABHILFEMAßNAHMEN BEHEBEN**
</dt> <dd> <dl> <dt>

15623 (0x3D07)
</dt> <dt>



Es wurde ein Fehler in einer Systembin binär erkannt. Versuchen Sie, den PC zu aktualisieren, um das Problem zu beheben.


</dt> </dl> </dd> <dt>

<span id="ERROR_APPX_INTEGRITY_FAILURE_CLR_NGEN"></span><span id="error_appx_integrity_failure_clr_ngen"></span>**\_FEHLER: \_ APPX-INTEGRITÄTSFEHLER \_ \_ CLR \_ NGEN**
</dt> <dd> <dl> <dt>

15624 (0x3D08)
</dt> <dt>



Eine beschädigte CLR-NGEN-Binärdatei wurde auf dem System erkannt.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESILIENCY_FILE_CORRUPT"></span><span id="error_resiliency_file_corrupt"></span>**\_FEHLERRESILIENZDATEI \_ \_ BESCHÄDIGT**
</dt> <dd> <dl> <dt>

15625 (0x3D09)
</dt> <dt>



Der Vorgang konnte nicht fortgesetzt werden, da die für die Wiederherstellung erforderlichen Daten beschädigt wurden.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_FIREWALL_SERVICE_NOT_RUNNING"></span><span id="error_install_firewall_service_not_running"></span>**FEHLER \_ BEIM INSTALLIEREN DES \_ \_ \_ FIREWALLDIENSTS, DER NICHT AUSGEFÜHRT \_ WIRD**
</dt> <dd> <dl> <dt>

15626 (0x3D0A)
</dt> <dt>



Das Paket konnte nicht installiert werden, da der Windows Firewalldienst nicht ausgeführt wird. Aktivieren Sie den Windows Firewalldienst, und wiederholen Sie den Vorgang.


</dt> </dl> </dd> <dt>

<span id="APPMODEL_ERROR_NO_PACKAGE"></span><span id="appmodel_error_no_package"></span>**APPMODEL-FEHLER \_ \_ KEIN \_ PAKET**
</dt> <dd> <dl> <dt>

15700 (0x3D54)
</dt> <dt>



Der Prozess verfügt über keine Paketidentität.


</dt> </dl> </dd> <dt>

<span id="APPMODEL_ERROR_PACKAGE_RUNTIME_CORRUPT"></span><span id="appmodel_error_package_runtime_corrupt"></span>**\_APPMODEL-FEHLERPAKET \_ RUNTIME \_ \_ BESCHÄDIGT**
</dt> <dd> <dl> <dt>

15701 (0x3D55)
</dt> <dt>



Die Paketlaufzeitinformationen sind beschädigt.


</dt> </dl> </dd> <dt>

<span id="APPMODEL_ERROR_PACKAGE_IDENTITY_CORRUPT"></span><span id="appmodel_error_package_identity_corrupt"></span>**APPMODEL ERROR \_ \_ PACKAGE IDENTITY CORRUPT (APPMODEL-FEHLERPAKETIDENTITÄT \_ \_ BESCHÄDIGT)**
</dt> <dd> <dl> <dt>

15702 (0x3D56)
</dt> <dt>



Die Paketidentität ist beschädigt.


</dt> </dl> </dd> <dt>

<span id="APPMODEL_ERROR_NO_APPLICATION"></span><span id="appmodel_error_no_application"></span>**APPMODEL-FEHLER \_ \_ KEINE \_ ANWENDUNG**
</dt> <dd> <dl> <dt>

15703 (0x3D57)
</dt> <dt>



Der Prozess verfügt über keine Anwendungsidentität.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_LOAD_STORE_FAILED"></span><span id="error_state_load_store_failed"></span>**FEHLER: \_ FEHLER BEIM LADEN DES \_ \_ SPEICHERS FÜR \_ DEN ZUSTAND**
</dt> <dd> <dl> <dt>

15800 (0x3DB8)
</dt> <dt>



Fehler beim Laden des Zustandsspeichers.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_GET_VERSION_FAILED"></span><span id="error_state_get_version_failed"></span>**FEHLERSTATUS \_ \_ FEHLER BEIM \_ GET-VERSION-FEHLER \_**
</dt> <dd> <dl> <dt>

15801 (0x3DB9)
</dt> <dt>



Fehler beim Abrufen der Statusversion für die Anwendung.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_SET_VERSION_FAILED"></span><span id="error_state_set_version_failed"></span>**FEHLER \_ BEI FEHLER BEI DER \_ \_ \_ STATUSSATZVERSION**
</dt> <dd> <dl> <dt>

15802 (0x3DBA)
</dt> <dt>



Fehler beim Festlegen der Statusversion für die Anwendung.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_STRUCTURED_RESET_FAILED"></span><span id="error_state_structured_reset_failed"></span>**FEHLER \_ BEIM STRUKTURIERTEN \_ ZURÜCKSETZEN DES \_ \_ ZUSTANDS FEHLGESCHLAGEN**
</dt> <dd> <dl> <dt>

15803 (0x3DBB)
</dt> <dt>



Fehler beim Zurücksetzen des strukturierten Zustands der Anwendung.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_OPEN_CONTAINER_FAILED"></span><span id="error_state_open_container_failed"></span>**FEHLER \_ BEIM STATUS DES \_ \_ GEÖFFNETEN \_ CONTAINERS**
</dt> <dd> <dl> <dt>

15804 (0x3DBC)
</dt> <dt>



Der Zustands-Manager konnte den Container nicht öffnen.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_CREATE_CONTAINER_FAILED"></span><span id="error_state_create_container_failed"></span>**FEHLER \_ BEIM ERSTELLEN EINES CONTAINERS MIT \_ \_ \_ FEHLERZUSTAND**
</dt> <dd> <dl> <dt>

15805 (0x3DBD)
</dt> <dt>



Der Zustands-Manager konnte den Container nicht erstellen.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_DELETE_CONTAINER_FAILED"></span><span id="error_state_delete_container_failed"></span>**FEHLER \_ BEIM LÖSCHEN DES CONTAINERS MIT DEM STATUS \_ \_ \_ "FEHLER"**
</dt> <dd> <dl> <dt>

15806 (0x3DBE)
</dt> <dt>



Der Zustands-Manager konnte den Container nicht löschen.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_READ_SETTING_FAILED"></span><span id="error_state_read_setting_failed"></span>**FEHLER \_ BEI \_ FEHLERZUSTANDSLESEEINSTELLUNG \_ \_**
</dt> <dd> <dl> <dt>

15807 (0x3DBF)
</dt> <dt>



Der Zustands-Manager konnte die Einstellung nicht lesen.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_WRITE_SETTING_FAILED"></span><span id="error_state_write_setting_failed"></span>**FEHLER BEI \_ DER \_ SCHREIBEINSTELLUNG FÜR \_ DEN \_ STATUS**
</dt> <dd> <dl> <dt>

15808 (0x3DC0)
</dt> <dt>



Fehler beim Schreiben der Einstellung durch den Zustands-Manager.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_DELETE_SETTING_FAILED"></span><span id="error_state_delete_setting_failed"></span>**FEHLER BEI \_ DER EINSTELLUNG ZUM LÖSCHEN DES \_ \_ \_ ZUSTANDS**
</dt> <dd> <dl> <dt>

15809 (0x3DC1)
</dt> <dt>



Fehler beim Löschen der Einstellung durch den Zustands-Manager.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_QUERY_SETTING_FAILED"></span><span id="error_state_query_setting_failed"></span>**FEHLER BEI \_ DER \_ ABFRAGEEINSTELLUNG "ERROR \_ \_ STATE"**
</dt> <dd> <dl> <dt>

15810 (0x3DC2)
</dt> <dt>



Fehler beim Abfragen der Einstellung durch den Zustands-Manager.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_READ_COMPOSITE_SETTING_FAILED"></span><span id="error_state_read_composite_setting_failed"></span>**FEHLER BEIM \_ LESEN \_ DER ZUSAMMENGESETZTEN EINSTELLUNG \_ \_ \_ "FEHLER"**
</dt> <dd> <dl> <dt>

15811 (0x3DC3)
</dt> <dt>



Fehler beim Lesen der zusammengesetzten Einstellung durch den Zustands-Manager.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_WRITE_COMPOSITE_SETTING_FAILED"></span><span id="error_state_write_composite_setting_failed"></span>**FEHLER BEIM \_ SCHREIBEN \_ DER ZUSAMMENGESETZTEN EINSTELLUNG FÜR DEN \_ \_ \_ FEHLERZUSTAND**
</dt> <dd> <dl> <dt>

15812 (0x3DC4)
</dt> <dt>



Fehler beim Schreiben der zusammengesetzten Einstellung durch den Zustands-Manager.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_ENUMERATE_CONTAINER_FAILED"></span><span id="error_state_enumerate_container_failed"></span>**FEHLER \_ BEIM \_ AUFZÄHLEN DES \_ CONTAINERS \_**
</dt> <dd> <dl> <dt>

15813 (0x3DC5)
</dt> <dt>



Der Zustands-Manager konnte die Container nicht aufzählen.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_ENUMERATE_SETTINGS_FAILED"></span><span id="error_state_enumerate_settings_failed"></span>**FEHLER \_ BEIM \_ AUFZÄHLEN VON \_ EINSTELLUNGEN MIT FEHLERZUSTAND \_**
</dt> <dd> <dl> <dt>

15814 (0x3DC6)
</dt> <dt>



Fehler beim Aufzählen der Einstellungen durch den Zustands-Manager.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_COMPOSITE_SETTING_VALUE_SIZE_LIMIT_EXCEEDED"></span><span id="error_state_composite_setting_value_size_limit_exceeded"></span>**ERROR \_ STATE \_ COMPOSITE \_ SETTING \_ VALUE \_ SIZE \_ LIMIT \_ EXCEEDED**
</dt> <dd> <dl> <dt>

15815 (0x3DC7)
</dt> <dt>



Die Größe des zusammengesetzten Einstellungswerts des Zustands-Managers hat den Grenzwert überschritten.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_SETTING_VALUE_SIZE_LIMIT_EXCEEDED"></span><span id="error_state_setting_value_size_limit_exceeded"></span>**\_ \_ FEHLERZUSTAND: EINSTELLUNG DES \_ WERTS \_ \_ GRÖßENBESCHRÄNKUNG \_ ÜBERSCHRITTEN**
</dt> <dd> <dl> <dt>

15816 (0x3DC8)
</dt> <dt>



Die Größe des Einstellungswerts für den Zustands-Manager hat den Grenzwert überschritten.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_SETTING_NAME_SIZE_LIMIT_EXCEEDED"></span><span id="error_state_setting_name_size_limit_exceeded"></span>**\_ \_ FEHLERSTATUSEINSTELLUNG \_ \_ NAMENSGRÖßENBESCHRÄNKUNG \_ \_ ÜBERSCHRITTEN**
</dt> <dd> <dl> <dt>

15817 (0x3DC9)
</dt> <dt>



Die Länge des Namens der Zustands-Manager-Einstellung hat den Grenzwert überschritten.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_CONTAINER_NAME_SIZE_LIMIT_EXCEEDED"></span><span id="error_state_container_name_size_limit_exceeded"></span>**\_ \_ FEHLERZUSTAND: \_ GRÖßENBESCHRÄNKUNG FÜR \_ \_ CONTAINERNAMEN \_ ÜBERSCHRITTEN**
</dt> <dd> <dl> <dt>

15818 (0x3DCA)
</dt> <dt>



Die Länge des Zustands-Manager-Containernamens hat den Grenzwert überschritten.


</dt> </dl> </dd> <dt>

<span id="ERROR_API_UNAVAILABLE"></span><span id="error_api_unavailable"></span>**\_FEHLER-API \_ NICHT VERFÜGBAR**
</dt> <dd> <dl> <dt>

15841 (0x3DE1)
</dt> <dt>



Diese API kann nicht im Kontext des Anwendungstyps des Aufrufers verwendet werden.


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

 

 
