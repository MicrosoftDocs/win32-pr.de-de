---
description: Beschreibt die in der Header Datei "Winerror. h" definierten Fehlercodes 12000-1599 und ist für Entwickler bestimmt.
ms.assetid: bb3c658d-96db-495a-a0dc-e93949c3835d
title: System Fehler Codes (12000-15999) (Winerror. h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: 8cac8adf6d8a4cf8f60fe978eb6f99f5efc1b9fe
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483323"
---
# <a name="system-error-codes-12000-15999"></a>System Fehler Codes (12000-15999)

> [!NOTE]
> Diese Informationen sind für Entwickler gedacht, die Systemfehler Debuggen. Bei anderen Fehlern, wie z. b. Problemen mit Windows Update, finden Sie eine Liste der Ressourcen auf der Seite [Fehlercodes](system-error-codes.md) .

In der folgenden Liste werden die [Systemfehler Codes](system-error-codes.md) (Fehler 12000 bis 15999) beschrieben. Sie werden von der [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) -Funktion zurückgegeben, wenn viele Funktionen fehlschlagen. Um den Beschreibungstext für den Fehler in Ihrer Anwendung abzurufen, verwenden Sie die [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) -Funktion mit dem Flag " **Format \_ Message \_ from \_ System** ".

<dl> <dt>

<span id="ERROR_INTERNET__"></span><span id="error_internet__"></span>**Fehler \_ \_Internet \** _
</dt> <dd> <dl> <dt>

12000-12175 (0x2ee0)
</dt> <dt>



Weitere Informationen finden Sie unter [Internet-Fehler Codes](../wininet/wininet-errors.md) und Wininet. h.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_QM_POLICY_EXISTS"></span><span id="error_ipsec_qm_policy_exists"></span>_ *Fehler \_ IPSec- \_ qm- \_ Richtlinie \_ vorhanden**
</dt> <dd> <dl> <dt>

13000 (0x32c8)
</dt> <dt>



Die angegebene Schnellmodus-Richtlinie ist bereits vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_QM_POLICY_NOT_FOUND"></span><span id="error_ipsec_qm_policy_not_found"></span>**Fehler bei \_ IPSec- \_ qm- \_ Richtlinie \_ nicht \_ gefunden.**
</dt> <dd> <dl> <dt>

13001 (0x32c9)
</dt> <dt>



Die angegebene Schnellmodus-Richtlinie wurde nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_QM_POLICY_IN_USE"></span><span id="error_ipsec_qm_policy_in_use"></span>**Fehler \_ \_ \_ \_ beim \_ Verwenden der IPSec-qm-Richtlinie.**
</dt> <dd> <dl> <dt>

13002 (0x32ca)
</dt> <dt>



Die angegebene Schnellmodus-Richtlinie wird verwendet.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_MM_POLICY_EXISTS"></span><span id="error_ipsec_mm_policy_exists"></span>**Fehler \_ IPSec \_ mm- \_ Richtlinie \_ vorhanden**
</dt> <dd> <dl> <dt>

13003 (0x32cb)
</dt> <dt>



Die angegebene Hauptmodusrichtlinie ist bereits vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_MM_POLICY_NOT_FOUND"></span><span id="error_ipsec_mm_policy_not_found"></span>**Fehler bei \_ IPSec \_ mm- \_ Richtlinie \_ nicht \_ gefunden.**
</dt> <dd> <dl> <dt>

13004 (0x32cc)
</dt> <dt>



Die angegebene Hauptmodusrichtlinie wurde nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_MM_POLICY_IN_USE"></span><span id="error_ipsec_mm_policy_in_use"></span>**Fehler \_ bei IPSec \_ mm- \_ Richtlinie wird \_ \_ verwendet**
</dt> <dd> <dl> <dt>

13005 (0x32cd)
</dt> <dt>



Die angegebene Hauptmodusrichtlinie wird verwendet.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_MM_FILTER_EXISTS"></span><span id="error_ipsec_mm_filter_exists"></span>**Fehler \_ IPSec \_ mm- \_ Filter \_ vorhanden**
</dt> <dd> <dl> <dt>

13006 (0x32ce)
</dt> <dt>



Der angegebene Hauptmodusfilter ist bereits vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_MM_FILTER_NOT_FOUND"></span><span id="error_ipsec_mm_filter_not_found"></span>**Fehler \_ IPSec \_ mm- \_ Filter wurde \_ nicht \_ gefunden.**
</dt> <dd> <dl> <dt>

13007 (0x32cf)
</dt> <dt>



Der angegebene Hauptmodusfilter wurde nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_TRANSPORT_FILTER_EXISTS"></span><span id="error_ipsec_transport_filter_exists"></span>**\_IPSec- \_ Transport \_ Filter ist \_ bereits vorhanden.**
</dt> <dd> <dl> <dt>

13008 (0x32d0)
</dt> <dt>



Der angegebene Transportmodus-Filter ist bereits vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_TRANSPORT_FILTER_NOT_FOUND"></span><span id="error_ipsec_transport_filter_not_found"></span>**Fehler beim \_ IPSec- \_ Transport \_ Filter \_ nicht \_ gefunden.**
</dt> <dd> <dl> <dt>

13009 (0x32d1)
</dt> <dt>



Der angegebene Transportmodus-Filter ist nicht vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_MM_AUTH_EXISTS"></span><span id="error_ipsec_mm_auth_exists"></span>**Fehler bei \_ IPSec-mm-Authentifizierung \_ \_ . \_**
</dt> <dd> <dl> <dt>

13010 (0x32d2)
</dt> <dt>



Die angegebene hauptmodusauthentifizierungsliste ist vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_MM_AUTH_NOT_FOUND"></span><span id="error_ipsec_mm_auth_not_found"></span>**Fehler bei \_ IPSec-mm-Authentifizierung \_ \_ \_ nicht \_ gefunden.**
</dt> <dd> <dl> <dt>

13011 (0x32d3)
</dt> <dt>



Die angegebene hauptmodusauthentifizierungsliste wurde nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_MM_AUTH_IN_USE"></span><span id="error_ipsec_mm_auth_in_use"></span>**Fehler \_ bei IPSec mm-Authentifizierung wird \_ \_ \_ \_ verwendet.**
</dt> <dd> <dl> <dt>

13012 (0x32d4)
</dt> <dt>



Die angegebene hauptmodusauthentifizierungsliste wird verwendet.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_DEFAULT_MM_POLICY_NOT_FOUND"></span><span id="error_ipsec_default_mm_policy_not_found"></span>**Fehler \_ IPSec- \_ Standard- \_ mm- \_ Richtlinie \_ nicht \_ gefunden**
</dt> <dd> <dl> <dt>

13013 (0x32d5)
</dt> <dt>



Die angegebene standardmäßige Hauptmodus-Richtlinie wurde nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_DEFAULT_MM_AUTH_NOT_FOUND"></span><span id="error_ipsec_default_mm_auth_not_found"></span>**Fehler bei \_ IPSec-Standard-mm-Authentifizierung \_ \_ \_ \_ nicht \_ gefunden.**
</dt> <dd> <dl> <dt>

13014 (0x32d6)
</dt> <dt>



Die angegebene Standard Authentifizierung im hauptmodusmodus wurde nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_DEFAULT_QM_POLICY_NOT_FOUND"></span><span id="error_ipsec_default_qm_policy_not_found"></span>**Fehler bei \_ IPSec- \_ Standard- \_ \_ Richtlinie "qm \_ \_ "**
</dt> <dd> <dl> <dt>

13015 (0x32d7)
</dt> <dt>



Die angegebene standardmäßige Schnellmodus-Richtlinie wurde nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_TUNNEL_FILTER_EXISTS"></span><span id="error_ipsec_tunnel_filter_exists"></span>**Fehler \_ IPSec- \_ Tunnel \_ Filter \_ vorhanden**
</dt> <dd> <dl> <dt>

13016 (0x32d8)
</dt> <dt>



Der angegebene Tunnel Modus-Filter ist vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_TUNNEL_FILTER_NOT_FOUND"></span><span id="error_ipsec_tunnel_filter_not_found"></span>**Fehler beim \_ IPSec- \_ Tunnel \_ Filter wurde \_ nicht \_ gefunden.**
</dt> <dd> <dl> <dt>

13017 (0x32d9)
</dt> <dt>



Der angegebene Tunnel Modus-Filter wurde nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_MM_FILTER_PENDING_DELETION"></span><span id="error_ipsec_mm_filter_pending_deletion"></span>**Fehler \_ IPSec \_ mm \_ Filter \_ ausstehende \_ Löschung**
</dt> <dd> <dl> <dt>

13018 (0x32da)
</dt> <dt>



Der Hauptmodusfilter steht für den Löschvorgang aus.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_TRANSPORT_FILTER_PENDING_DELETION"></span><span id="error_ipsec_transport_filter_pending_deletion"></span>**Fehler beim \_ Löschen des IPSec- \_ Transport \_ Filters \_ \_ .**
</dt> <dd> <dl> <dt>

13019 (0x32db)
</dt> <dt>



Das Löschen des Transport Filters steht aus.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_TUNNEL_FILTER_PENDING_DELETION"></span><span id="error_ipsec_tunnel_filter_pending_deletion"></span>**Fehler bei \_ IPSec- \_ Tunnel \_ Filter \_ ausstehende \_ Löschung**
</dt> <dd> <dl> <dt>

13020 (0x32dc)
</dt> <dt>



Das Löschen des Tunnel Filters steht aus.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_MM_POLICY_PENDING_DELETION"></span><span id="error_ipsec_mm_policy_pending_deletion"></span>**Fehler beim \_ Löschen der IPSec \_ mm- \_ Richtlinie \_ \_ .**
</dt> <dd> <dl> <dt>

13021 (0x32dd)
</dt> <dt>



Die Hauptmodusrichtlinie steht für den Löschvorgang aus.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_MM_AUTH_PENDING_DELETION"></span><span id="error_ipsec_mm_auth_pending_deletion"></span>**Fehler beim \_ Löschen der IPSec mm-Authentifizierung \_ \_ . \_ \_**
</dt> <dd> <dl> <dt>

13022 (0x32de)
</dt> <dt>



Das hauptmodusauthentifizierungs-Bundle steht für den Löschvorgang aus.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_QM_POLICY_PENDING_DELETION"></span><span id="error_ipsec_qm_policy_pending_deletion"></span>**Fehler beim \_ Löschen der IPSec- \_ qm- \_ Richtlinie \_ \_ .**
</dt> <dd> <dl> <dt>

13023 (0x32df)
</dt> <dt>



Das Löschen der Schnellmodus-Richtlinie steht aus.


</dt> </dl> </dd> <dt>

<span id="WARNING_IPSEC_MM_POLICY_PRUNED"></span><span id="warning_ipsec_mm_policy_pruned"></span>**Warnung bei \_ IPSec- \_ mm- \_ Richtlinie \_ wurde gelöscht**
</dt> <dd> <dl> <dt>

13024 (0x32e0)
</dt> <dt>



Die Hauptmodus-Richtlinie wurde erfolgreich hinzugefügt, einige der angeforderten Angebote werden jedoch nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="WARNING_IPSEC_QM_POLICY_PRUNED"></span><span id="warning_ipsec_qm_policy_pruned"></span>**Warnung bei \_ IPSec- \_ qm- \_ Richtlinie \_ wurde gelöscht**
</dt> <dd> <dl> <dt>

13025 (0x32e1)
</dt> <dt>



Die Schnellmodus-Richtlinie wurde erfolgreich hinzugefügt, einige der angeforderten Angebote werden jedoch nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_NEG_STATUS_BEGIN"></span><span id="error_ipsec_ike_neg_status_begin"></span>**Fehler \_ IPSec \_ IKE \_ NETg \_ Status \_ Begin**
</dt> <dd> <dl> <dt>

13800 (0x35e8)
</dt> <dt>



Fehler \_ IPSec \_ IKE \_ NETg \_ Status \_ Begin


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_AUTH_FAIL"></span><span id="error_ipsec_ike_auth_fail"></span>**Fehler bei \_ IPSec- \_ IKE-Authentifizierung \_ . \_**
</dt> <dd> <dl> <dt>

13801 (0x35e9)
</dt> <dt>



Die Anmelde Informationen für die IKE-Authentifizierung sind unzulässig.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_ATTRIB_FAIL"></span><span id="error_ipsec_ike_attrib_fail"></span>**Fehler bei \_ IPSec \_ IKE \_ atzb \_**
</dt> <dd> <dl> <dt>

13802 (0x35ea)
</dt> <dt>



IKE-Sicherheits Attribute sind nicht zulässig.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_NEGOTIATION_PENDING"></span><span id="error_ipsec_ike_negotiation_pending"></span>**Fehler bei \_ IPSec- \_ IKE- \_ Aushandlung \_ Ausstehend**
</dt> <dd> <dl> <dt>

13803 (0x35eb)
</dt> <dt>



Die IKE-Aushandlung wird ausgeführt.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_GENERAL_PROCESSING_ERROR"></span><span id="error_ipsec_ike_general_processing_error"></span>**Fehler bei \_ IPSec- \_ IKE \_ allgemeine \_ Verarbeitungs \_ Fehler**
</dt> <dd> <dl> <dt>

13804 (0x35ec)
</dt> <dt>



Allgemeiner Verarbeitungsfehler.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_TIMED_OUT"></span><span id="error_ipsec_ike_timed_out"></span>**Fehler bei \_ IPSec- \_ IKE. \_ \_**
</dt> <dd> <dl> <dt>

13805 (0x35ed)
</dt> <dt>



Timeout bei der Aushandlung.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_NO_CERT"></span><span id="error_ipsec_ike_no_cert"></span>**Fehler \_ IPSec \_ IKE \_ kein \_ Zertifikat**
</dt> <dd> <dl> <dt>

13806 (0x35ee)
</dt> <dt>



IKE konnte ein gültiges Computer Zertifikat nicht finden. Wenden Sie sich an den Netzwerk Sicherheits Administrator, um ein gültiges Zertifikat im entsprechenden Zertifikat Speicher zu installieren.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_SA_DELETED"></span><span id="error_ipsec_ike_sa_deleted"></span>**Fehler \_ IPSec- \_ IKE- \_ sa \_ gelöscht**
</dt> <dd> <dl> <dt>

13807 (0x35ef)
</dt> <dt>



Die IKE-SA wurde vor dem Abschluss des Vorgangs von Peer gelöscht.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_SA_REAPED"></span><span id="error_ipsec_ike_sa_reaped"></span>**Fehler beim Wiedergeben von \_ IPSec- \_ IKE. \_ \_**
</dt> <dd> <dl> <dt>

13808 (0x35f 0)
</dt> <dt>



Die IKE-SA wurde vor Abschluss der Einrichtung gelöscht.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_MM_ACQUIRE_DROP"></span><span id="error_ipsec_ike_mm_acquire_drop"></span>**Fehler \_ IPSec \_ IKE \_ mm \_ Abrufen \_**
</dt> <dd> <dl> <dt>

13809 (0x35f 1)
</dt> <dt>



Die Aushandlungs Anforderung ist zu lang in der Warteschlange.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_QM_ACQUIRE_DROP"></span><span id="error_ipsec_ike_qm_acquire_drop"></span>**Fehler beim Abrufen von " \_ IPSec \_ IKE \_ qm \_ \_ ".**
</dt> <dd> <dl> <dt>

13810 (0x35f 2)
</dt> <dt>



Die Aushandlungs Anforderung ist zu lang in der Warteschlange.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_QUEUE_DROP_MM"></span><span id="error_ipsec_ike_queue_drop_mm"></span>**Fehler beim \_ Löschen der IPSec- \_ IKE- \_ Warteschlange \_ \_**
</dt> <dd> <dl> <dt>

13811 (0x35f 3)
</dt> <dt>



Die Aushandlungs Anforderung ist zu lang in der Warteschlange.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_QUEUE_DROP_NO_MM"></span><span id="error_ipsec_ike_queue_drop_no_mm"></span>**Fehler \_ IPSec \_ IKE \_ Queue \_ Drop \_ No \_ mm**
</dt> <dd> <dl> <dt>

13812 (0x35f 4)
</dt> <dt>



Die Aushandlungs Anforderung ist zu lang in der Warteschlange.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_DROP_NO_RESPONSE"></span><span id="error_ipsec_ike_drop_no_response"></span>**Fehler \_ IPSec \_ IKE \_ Drop \_ No \_ Response**
</dt> <dd> <dl> <dt>

13813 (0x35f 5)
</dt> <dt>



Keine Antwort vom Peer.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_MM_DELAY_DROP"></span><span id="error_ipsec_ike_mm_delay_drop"></span>**Fehler \_ IPSec \_ IKE \_ mm \_ Delay \_ Drop**
</dt> <dd> <dl> <dt>

13814 (0x35f 6)
</dt> <dt>



Die Aushandlung hat zu lange gedauert.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_QM_DELAY_DROP"></span><span id="error_ipsec_ike_qm_delay_drop"></span>**Fehler bei \_ IPSec \_ IKE \_ qm \_ Delay \_ Drop**
</dt> <dd> <dl> <dt>

13815 (0x35f 7)
</dt> <dt>



Die Aushandlung hat zu lange gedauert.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_ERROR"></span><span id="error_ipsec_ike_error"></span>**Fehler \_ IPSec- \_ IKE- \_ Fehler**
</dt> <dd> <dl> <dt>

13816 (0x35f 8)
</dt> <dt>



Unbekannter Fehler.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_CRL_FAILED"></span><span id="error_ipsec_ike_crl_failed"></span>**Fehler bei \_ IPSec- \_ IKE- \_ CRL. \_**
</dt> <dd> <dl> <dt>

13817 (0x35f 9)
</dt> <dt>



Fehler bei der Zertifikat Sperr Überprüfung.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_KEY_USAGE"></span><span id="error_ipsec_ike_invalid_key_usage"></span>**Fehler \_ IPSec \_ IKE \_ ungültige \_ Schlüssel \_ Verwendung**
</dt> <dd> <dl> <dt>

13818 (0x35fa)
</dt> <dt>



Ungültige Zertifikat Schlüssel Verwendung.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_CERT_TYPE"></span><span id="error_ipsec_ike_invalid_cert_type"></span>**Fehler \_ IPSec \_ IKE \_ ungültiger \_ CERT- \_ Typ**
</dt> <dd> <dl> <dt>

13819 (0x35fb)
</dt> <dt>



Ungültiger Zertifikattyp.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_NO_PRIVATE_KEY"></span><span id="error_ipsec_ike_no_private_key"></span>**Fehler \_ IPSec \_ IKE \_ kein \_ privater \_ Schlüssel**
</dt> <dd> <dl> <dt>

13820 (0x35fc)
</dt> <dt>



Fehler bei der IKE-Aushandlung, weil das verwendete Computer Zertifikat keinen privaten Schlüssel besitzt. Für IPSec-Zertifikate ist ein privater Schlüssel erforderlich. Wenden Sie sich an den Netzwerk Sicherheitsadministrator, um durch ein Zertifikat mit einem privaten Schlüssel zu ersetzen.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_SIMULTANEOUS_REKEY"></span><span id="error_ipsec_ike_simultaneous_rekey"></span>**Fehler beim \_ \_ \_ gleichzeitigen \_ erneuten Schlüssel für IPSec-IKE**
</dt> <dd> <dl> <dt>

13821 (0x35fd)
</dt> <dt>



Gleichzeitige rekeys wurden erkannt.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_DH_FAIL"></span><span id="error_ipsec_ike_dh_fail"></span>**Fehler \_ IPSec \_ IKE \_ dh \_ fehlschlägt**
</dt> <dd> <dl> <dt>

13822 (0x35fe)
</dt> <dt>



Fehler bei der Diffie-Hellman Berechnung.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_CRITICAL_PAYLOAD_NOT_RECOGNIZED"></span><span id="error_ipsec_ike_critical_payload_not_recognized"></span>**Fehler " \_ IPSec \_ IKE \_ Critical Payload" wurde \_ \_ nicht \_ erkannt.**
</dt> <dd> <dl> <dt>

13823 (0x35ff)
</dt> <dt>



Sie wissen nicht, wie Sie eine kritische Nutzlast verarbeiten.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_HEADER"></span><span id="error_ipsec_ike_invalid_header"></span>**Fehler " \_ IPSec \_ IKE- \_ ungültige \_ Kopfzeile"**
</dt> <dd> <dl> <dt>

13824 (0x3600)
</dt> <dt>



Ungültiger Header.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_NO_POLICY"></span><span id="error_ipsec_ike_no_policy"></span>**Fehler \_ IPSec \_ IKE \_ keine \_ Richtlinie**
</dt> <dd> <dl> <dt>

13825 (0x3601)
</dt> <dt>



Keine Richtlinie konfiguriert.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_SIGNATURE"></span><span id="error_ipsec_ike_invalid_signature"></span>**Fehler bei \_ IPSec \_ IKE \_ ungültige \_ Signatur.**
</dt> <dd> <dl> <dt>

13826 (0x3602)
</dt> <dt>



Fehler beim Überprüfen der Signatur.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_KERBEROS_ERROR"></span><span id="error_ipsec_ike_kerberos_error"></span>**Fehler bei \_ IPSec- \_ IKE- \_ Kerberos- \_ Fehler**
</dt> <dd> <dl> <dt>

13827 (0x3603)
</dt> <dt>



Fehler beim Authentifizieren mithilfe von Kerberos.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_NO_PUBLIC_KEY"></span><span id="error_ipsec_ike_no_public_key"></span>**Fehler \_ IPSec \_ IKE \_ kein \_ öffentlicher \_ Schlüssel**
</dt> <dd> <dl> <dt>

13828 (0x3604)
</dt> <dt>



Das Zertifikat des Peers enthielt keinen öffentlichen Schlüssel.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR"></span><span id="error_ipsec_ike_process_err"></span>**Fehler \_ IPSec- \_ IKE- \_ Prozess \_ Err**
</dt> <dd> <dl> <dt>

13829 (0x3605)
</dt> <dt>



Fehler beim Verarbeiten der Fehler Nutzlast.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_SA"></span><span id="error_ipsec_ike_process_err_sa"></span>**Fehler \_ IPSec \_ IKE \_ Prozess \_ Err \_ sa**
</dt> <dd> <dl> <dt>

13830 (0x3606)
</dt> <dt>



Fehler beim Verarbeiten der SA-Nutzlast.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_PROP"></span><span id="error_ipsec_ike_process_err_prop"></span>**Fehler \_ IPSec \_ IKE \_ Process \_ Err \_ Prop**
</dt> <dd> <dl> <dt>

13831 (0x3607)
</dt> <dt>



Fehler beim Verarbeiten der nutzungsnutzlast.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_TRANS"></span><span id="error_ipsec_ike_process_err_trans"></span>**Fehler \_ IPSec \_ IKE- \_ Prozess \_ Err \_ Trans**
</dt> <dd> <dl> <dt>

13832 (0x3608)
</dt> <dt>



Fehler beim Verarbeiten der Transform-Nutzlast.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_KE"></span><span id="error_ipsec_ike_process_err_ke"></span>**Fehler \_ IPSec \_ IKE- \_ Prozess \_ Err \_ KE**
</dt> <dd> <dl> <dt>

13833 (0x3609)
</dt> <dt>



Fehler beim Verarbeiten der KE-Nutzlast.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_ID"></span><span id="error_ipsec_ike_process_err_id"></span>**Fehler bei \_ IPSec \_ IKE- \_ Prozess-Err- \_ \_ ID**
</dt> <dd> <dl> <dt>

13834 (0x360a)
</dt> <dt>



Fehler beim Verarbeiten der ID-Nutzlast.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_CERT"></span><span id="error_ipsec_ike_process_err_cert"></span>**Fehler \_ IPSec \_ IKE \_ Process \_ Err \_ CERT**
</dt> <dd> <dl> <dt>

13835 (0x360b)
</dt> <dt>



Fehler beim Verarbeiten der Zertifikat Nutzlast.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_CERT_REQ"></span><span id="error_ipsec_ike_process_err_cert_req"></span>**Fehler \_ IPSec \_ IKE \_ Process \_ Err \_ CERT \_ req**
</dt> <dd> <dl> <dt>

13836 (0x360c)
</dt> <dt>



Fehler beim Verarbeiten der Nutzlast von Zertifikat Anforderungen.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_HASH"></span><span id="error_ipsec_ike_process_err_hash"></span>**Fehler \_ IPSec \_ IKE \_ Prozess \_ Err- \_ Hash**
</dt> <dd> <dl> <dt>

13837 (0x360d)
</dt> <dt>



Fehler beim Verarbeiten der Hash Nutzlast.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_SIG"></span><span id="error_ipsec_ike_process_err_sig"></span>**Fehler \_ IPSec \_ IKE- \_ Prozess \_ Err \_ sig**
</dt> <dd> <dl> <dt>

13838 (0x360e)
</dt> <dt>



Fehler beim Verarbeiten der Signatur Nutzlast.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_NONCE"></span><span id="error_ipsec_ike_process_err_nonce"></span>**Fehler \_ IPSec- \_ IKE- \_ Prozess \_ Err \_ Nonce**
</dt> <dd> <dl> <dt>

13839 (0x360f)
</dt> <dt>



Fehler beim Verarbeiten der Nonce-Nutzlast.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_NOTIFY"></span><span id="error_ipsec_ike_process_err_notify"></span>**Fehler bei \_ IPSec- \_ IKE- \_ Prozess- \_ \_ Benachrichtigung Benachrichtigen**
</dt> <dd> <dl> <dt>

13840 (0x3610)
</dt> <dt>



Fehler beim Verarbeiten der Nutzlast benachrichtigen.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_DELETE"></span><span id="error_ipsec_ike_process_err_delete"></span>**Fehler \_ IPSec \_ IKE- \_ Prozess \_ Err \_ Delete**
</dt> <dd> <dl> <dt>

13841 (0x3611)
</dt> <dt>



Fehler beim Verarbeiten von Lösch Nutzlast.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_VENDOR"></span><span id="error_ipsec_ike_process_err_vendor"></span>**Fehler \_ IPSec \_ IKE \_ Process \_ Err- \_ Hersteller**
</dt> <dd> <dl> <dt>

13842 (0x3612)
</dt> <dt>



Fehler beim Verarbeiten der VendorID-Nutzlast.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_PAYLOAD"></span><span id="error_ipsec_ike_invalid_payload"></span>**Fehler bei \_ IPSec- \_ IKE \_ ungültige \_ Nutzlast.**
</dt> <dd> <dl> <dt>

13843 (0x3613)
</dt> <dt>



Ungültige Nutzlast empfangen.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_LOAD_SOFT_SA"></span><span id="error_ipsec_ike_load_soft_sa"></span>**Fehler \_ IPSec \_ IKE \_ Load \_ Soft \_ sa**
</dt> <dd> <dl> <dt>

13844 (0x3614)
</dt> <dt>



Soft-SA geladen.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_SOFT_SA_TORN_DOWN"></span><span id="error_ipsec_ike_soft_sa_torn_down"></span>**Fehler "IPSec", Soft-SA, wurde \_ \_ \_ \_ \_ \_ abgebrochen.**
</dt> <dd> <dl> <dt>

13845 (0x3615)
</dt> <dt>



Weiche SA wurde abgebrochen.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_COOKIE"></span><span id="error_ipsec_ike_invalid_cookie"></span>**Fehler bei \_ IPSec \_ IKE \_ ungültiges \_ Cookie.**
</dt> <dd> <dl> <dt>

13846 (0x3616)
</dt> <dt>



Ungültiges Cookie empfangen.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_NO_PEER_CERT"></span><span id="error_ipsec_ike_no_peer_cert"></span>**Fehler \_ IPSec \_ IKE \_ kein \_ Peer \_ Zertifikat**
</dt> <dd> <dl> <dt>

13847 (0x3617)
</dt> <dt>



Der Peer konnte ein gültiges Computer Zertifikat nicht senden.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PEER_CRL_FAILED"></span><span id="error_ipsec_ike_peer_crl_failed"></span>**Fehler bei \_ IPSec- \_ IKE- \_ Peer- \_ CRL \_ .**
</dt> <dd> <dl> <dt>

13848 (0x3618)
</dt> <dt>



Fehler bei der Zertifizierungs Sperr Überprüfung des Peer Zertifikats.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_POLICY_CHANGE"></span><span id="error_ipsec_ike_policy_change"></span>**Fehler bei \_ IPSec- \_ IKE- \_ Richtlinie \_ ändern**
</dt> <dd> <dl> <dt>

13849 (0x3619)
</dt> <dt>



Die neue Richtlinie hat eine SAS für eine alte Richtlinie ungültig gemacht.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_NO_MM_POLICY"></span><span id="error_ipsec_ike_no_mm_policy"></span>**Fehler \_ IPSec \_ IKE \_ keine \_ mm- \_ Richtlinie**
</dt> <dd> <dl> <dt>

13850 (0x361a)
</dt> <dt>



Es gibt keine verfügbare IKE-Hauptmodus-Richtlinie.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_NOTCBPRIV"></span><span id="error_ipsec_ike_notcbpriv"></span>**Fehler \_ IPSec \_ IKE \_ notcbpriv**
</dt> <dd> <dl> <dt>

13851 (0x361b)
</dt> <dt>



TCB-Berechtigung konnte nicht aktiviert werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_SECLOADFAIL"></span><span id="error_ipsec_ike_secloadfail"></span>**Fehler \_ IPSec \_ IKE \_ secloadfail**
</dt> <dd> <dl> <dt>

13852 (0x361c)
</dt> <dt>



SECURITY.DLL konnte nicht geladen werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_FAILSSPINIT"></span><span id="error_ipsec_ike_failsspinit"></span>**Fehler \_ IPSec \_ IKE \_ failsspinit**
</dt> <dd> <dl> <dt>

13853 (0x361d)
</dt> <dt>



Fehler beim Abrufen der dispatchadresse der Sicherheits Funktions Tabelle von SSPI.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_FAILQUERYSSP"></span><span id="error_ipsec_ike_failqueryssp"></span>**Fehler \_ IPSec \_ IKE \_ failqueryssp**
</dt> <dd> <dl> <dt>

13854 (0x361e)
</dt> <dt>



Fehler beim Abfragen des Kerberos-Pakets zum Abrufen der maximalen Tokengröße.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_SRVACQFAIL"></span><span id="error_ipsec_ike_srvacqfail"></span>**Fehler \_ IPSec \_ IKE \_ srvacqfail**
</dt> <dd> <dl> <dt>

13855 (0x361f)
</dt> <dt>



Fehler beim Abrufen der Anmelde Informationen des Kerberos-Servers für den ISAKMP- \_ /fehleripsec- \_ IKE-Dienst. Die Kerberos-Authentifizierung funktioniert nicht. Der wahrscheinlichste Grund hierfür ist fehlende Domänen Mitgliedschaft. Dies ist normal, wenn der Computer Mitglied einer Arbeitsgruppe ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_SRVQUERYCRED"></span><span id="error_ipsec_ike_srvquerycred"></span>**Fehler \_ IPSec \_ IKE \_ srvquerykred**
</dt> <dd> <dl> <dt>

13856 (0x3620)
</dt> <dt>



Der SSPI-Prinzipal Name für den ISAKMP- \_ /fehleripsec- \_ IKE-Dienst ([**querykredentialsattributes**](/windows/win32/api/sspi/nf-sspi-querycredentialsattributesa)) konnte nicht ermittelt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_GETSPIFAIL"></span><span id="error_ipsec_ike_getspifail"></span>**Fehler \_ IPSec \_ IKE \_ getspifail**
</dt> <dd> <dl> <dt>

13857 (0x3621)
</dt> <dt>



Fehler beim Abrufen des neuen SPI für den eingehenden Datenverkehr vom IPSec-Treiber. Die häufigste Ursache hierfür ist, dass der Treiber nicht über den richtigen Filter verfügt. Überprüfen Sie die Richtlinie zum Überprüfen der Filter.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_FILTER"></span><span id="error_ipsec_ike_invalid_filter"></span>**Fehler \_ IPSec \_ IKE \_ ungültiger \_ Filter**
</dt> <dd> <dl> <dt>

13858 (0x3622)
</dt> <dt>



Der angegebene Filter ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_OUT_OF_MEMORY"></span><span id="error_ipsec_ike_out_of_memory"></span>**Fehler bei \_ IPSec \_ IKE nicht genügend Arbeits \_ \_ \_ Speicher.**
</dt> <dd> <dl> <dt>

13859 (0x3623)
</dt> <dt>



Die Speicherbelegung hat einen Fehler erzeugt.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_ADD_UPDATE_KEY_FAILED"></span><span id="error_ipsec_ike_add_update_key_failed"></span>**Fehler beim \_ IPSec- \_ IKE- \_ \_ Update \_ Schlüssel hinzufügen \_ .**
</dt> <dd> <dl> <dt>

13860 (0x3624)
</dt> <dt>



Fehler beim Hinzufügen der Sicherheits Zuordnung zum IPSec-Treiber. Die häufigste Ursache hierfür ist, dass die IKE-Aushandlung zu lange gedauert hat. Wenn das Problem weiterhin besteht, verringern Sie die Last auf dem fehlerhaften Computer.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_POLICY"></span><span id="error_ipsec_ike_invalid_policy"></span>**\_ungültige IPSec- \_ IKE- \_ \_ Richtlinie**
</dt> <dd> <dl> <dt>

13861 (0x3625 starten)
</dt> <dt>



Ungültige Richtlinie.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_UNKNOWN_DOI"></span><span id="error_ipsec_ike_unknown_doi"></span>**Fehler \_ IPSec \_ IKE \_ unbekannt \_**
</dt> <dd> <dl> <dt>

13862 (0x3626)
</dt> <dt>



Ungültiger doi.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_SITUATION"></span><span id="error_ipsec_ike_invalid_situation"></span>**Fehler bei \_ IPSec- \_ IKE ( \_ ungültige \_ Situation)**
</dt> <dd> <dl> <dt>

13863 (0x3627)
</dt> <dt>



Ungültige Situation.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_DH_FAILURE"></span><span id="error_ipsec_ike_dh_failure"></span>**Fehler bei \_ IPSec- \_ IKE- \_ dh \_ -Fehler**
</dt> <dd> <dl> <dt>

13864 (0x3628)
</dt> <dt>



Diffie-Hellman Fehler.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_GROUP"></span><span id="error_ipsec_ike_invalid_group"></span>**Fehler bei \_ IPSec \_ IKE \_ ungültige \_ Gruppe.**
</dt> <dd> <dl> <dt>

13865 (0x3629)
</dt> <dt>



Ungültige Diffie-Hellman Gruppe.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_ENCRYPT"></span><span id="error_ipsec_ike_encrypt"></span>**Fehler beim \_ Verschlüsseln der IPSec- \_ IKE. \_**
</dt> <dd> <dl> <dt>

13866 (0x362a)
</dt> <dt>



Fehler beim Verschlüsseln der Nutzlast.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_DECRYPT"></span><span id="error_ipsec_ike_decrypt"></span>**Fehler \_ IPSec \_ IKE \_ entschlüsseln**
</dt> <dd> <dl> <dt>

13867 (0x362b)
</dt> <dt>



Fehler beim Entschlüsseln von Nutzlast.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_POLICY_MATCH"></span><span id="error_ipsec_ike_policy_match"></span>**\_IPSec- \_ IKE- \_ Richtlinien \_ Übereinstimmung**
</dt> <dd> <dl> <dt>

13868 (0x362c)
</dt> <dt>



Fehler bei Richtlinien Übereinstimmung.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_UNSUPPORTED_ID"></span><span id="error_ipsec_ike_unsupported_id"></span>**Fehler " \_ IPSec \_ IKE \_ nicht unterstützte \_ ID"**
</dt> <dd> <dl> <dt>

13869 (0x362d)
</dt> <dt>



Nicht unterstützte ID.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_HASH"></span><span id="error_ipsec_ike_invalid_hash"></span>**Fehler bei \_ IPSec- \_ IKE ( \_ ungültiger \_ Hash)**
</dt> <dd> <dl> <dt>

13870 (0x362e)
</dt> <dt>



Fehler bei der Hash Überprüfung.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_HASH_ALG"></span><span id="error_ipsec_ike_invalid_hash_alg"></span>**Fehler \_ IPSec \_ IKE \_ ungültige \_ \_ HashAlg**
</dt> <dd> <dl> <dt>

13871 (0x362f)
</dt> <dt>



Ungültiger Hash Algorithmus.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_HASH_SIZE"></span><span id="error_ipsec_ike_invalid_hash_size"></span>**Fehler bei \_ IPSec \_ IKE \_ ungültige \_ \_ Hashgröße**
</dt> <dd> <dl> <dt>

13872 (0x3630)
</dt> <dt>



Ungültige Hashgröße.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_ENCRYPT_ALG"></span><span id="error_ipsec_ike_invalid_encrypt_alg"></span>**Fehler \_ IPSec \_ IKE \_ ungültig \_ verschlüsseln ( \_ ALG)**
</dt> <dd> <dl> <dt>

13873 (0x3631)
</dt> <dt>



Ungültiger Verschlüsselungsalgorithmus.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_AUTH_ALG"></span><span id="error_ipsec_ike_invalid_auth_alg"></span>**Fehler \_ IPSec \_ IKE \_ ungültige \_ auth \_ alg**
</dt> <dd> <dl> <dt>

13874 (0x3632)
</dt> <dt>



Ungültiger Authentifizierungsalgorithmus.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_SIG"></span><span id="error_ipsec_ike_invalid_sig"></span>**Fehler \_ IPSec \_ IKE \_ ungültige \_ sig**
</dt> <dd> <dl> <dt>

13875 (0x3633)
</dt> <dt>



Ungültige Zertifikat Signatur.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_LOAD_FAILED"></span><span id="error_ipsec_ike_load_failed"></span>**Fehler beim \_ Laden der IPSec- \_ IKE. \_ \_**
</dt> <dd> <dl> <dt>

13876 (0x3634)
</dt> <dt>



Fehler beim Laden.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_RPC_DELETE"></span><span id="error_ipsec_ike_rpc_delete"></span>**Fehler \_ IPSec \_ IKE \_ RPC \_ Delete**
</dt> <dd> <dl> <dt>

13877 (0x3635)
</dt> <dt>



Gelöscht per RPC-Aufruf.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_BENIGN_REINIT"></span><span id="error_ipsec_ike_benign_reinit"></span>**Fehler \_ IPSec- \_ IKE ist \_ fehlerhaft \_**
</dt> <dd> <dl> <dt>

13878 (0x3636)
</dt> <dt>



Temporärer Zustand, der zum Ausführen der erneuten Initialisierung erstellt wird. Dies ist kein echter Fehler.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_RESPONDER_LIFETIME_NOTIFY"></span><span id="error_ipsec_ike_invalid_responder_lifetime_notify"></span>**Fehler bei \_ IPSec- \_ IKE- \_ Benachrichtigung für ungültige \_ Antwort \_ \_ Liste**
</dt> <dd> <dl> <dt>

13879 (0x3637)
</dt> <dt>



Der in der Benachrichtigungs Lebensdauer-Benachrichtigung empfangene Lebensdauer Wert liegt unterhalb des konfigurierten Mindestwerts von Windows 2000. Korrigieren Sie die Richtlinie auf dem Peer Computer.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_MAJOR_VERSION"></span><span id="error_ipsec_ike_invalid_major_version"></span>**Fehler bei \_ IPSec \_ IKE \_ ungültige \_ Haupt \_ Version.**
</dt> <dd> <dl> <dt>

13880 (0x3638)
</dt> <dt>



Der Empfänger kann die im-Header angegebene Version von IKE nicht verarbeiten.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_CERT_KEYLEN"></span><span id="error_ipsec_ike_invalid_cert_keylen"></span>**Fehler \_ IPSec \_ IKE \_ ungültige \_ CERT \_ keylen.**
</dt> <dd> <dl> <dt>

13881 (0x3639)
</dt> <dt>



Die Schlüssellänge im Zertifikat ist zu klein für konfigurierte Sicherheitsanforderungen.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_MM_LIMIT"></span><span id="error_ipsec_ike_mm_limit"></span>**Fehler \_ IPSec \_ IKE \_ mm \_ Limit**
</dt> <dd> <dl> <dt>

13882 (0x363a)
</dt> <dt>



Die maximal zulässige Anzahl von festgelegten mm-SAS-überschritten.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_NEGOTIATION_DISABLED"></span><span id="error_ipsec_ike_negotiation_disabled"></span>**Fehler bei der \_ IPSec- \_ IKE- \_ Aushandlung \_ deaktiviert**
</dt> <dd> <dl> <dt>

13883 (0x363b)
</dt> <dt>



IKE hat eine Richtlinie zum Deaktivieren der Aushandlung erhalten.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_QM_LIMIT"></span><span id="error_ipsec_ike_qm_limit"></span>**\_IPSec- \_ IKE- \_ qm- \_ Grenzwert (Fehler)**
</dt> <dd> <dl> <dt>

13884 (0x363c)
</dt> <dt>



Die maximale schnellmodusbeschränkung für den Hauptmodus wurde erreicht. Der neue Hauptmodus wird gestartet.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_MM_EXPIRED"></span><span id="error_ipsec_ike_mm_expired"></span>**Fehler \_ IPSec \_ IKE \_ mm ist \_ abgelaufen.**
</dt> <dd> <dl> <dt>

13885 (0x363d)
</dt> <dt>



Die Lebensdauer der Hauptmodus-SA ist abgelaufen


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PEER_MM_ASSUMED_INVALID"></span><span id="error_ipsec_ike_peer_mm_assumed_invalid"></span>**Fehler \_ IPSec \_ IKE- \_ Peer \_ mm hat \_ \_ ungültig angenommen.**
</dt> <dd> <dl> <dt>

13886 (0x363e)
</dt> <dt>



Der Hauptmodus-SA ist ungültig, da der Peer nicht mehr antwortet.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_CERT_CHAIN_POLICY_MISMATCH"></span><span id="error_ipsec_ike_cert_chain_policy_mismatch"></span>**Fehler bei \_ IPSec-Richtlinien für die \_ \_ Zertifikat \_ Ketten \_ Richtlinie \_ .**
</dt> <dd> <dl> <dt>

13887 (0x363f)
</dt> <dt>



Das Zertifikat wird nicht zu einem vertrauenswürdigen Stamm in der IPSec-Richtlinie verkettet


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_UNEXPECTED_MESSAGE_ID"></span><span id="error_ipsec_ike_unexpected_message_id"></span>**Fehler " \_ IPSec \_ IKE \_ unerwartete Nachrichten- \_ \_ ID"**
</dt> <dd> <dl> <dt>

13888 (0x3640)
</dt> <dt>



Unerwartete Nachrichten-ID empfangen.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_AUTH_PAYLOAD"></span><span id="error_ipsec_ike_invalid_auth_payload"></span>**Fehler bei \_ IPSec- \_ IKE \_ ungültige Authentifizierungs \_ \_ Nutzlast.**
</dt> <dd> <dl> <dt>

13889 (0x3641)
</dt> <dt>



Es wurden ungültige Authentifizierungs Angebote empfangen.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_DOS_COOKIE_SENT"></span><span id="error_ipsec_ike_dos_cookie_sent"></span>**Fehler \_ IPSec- \_ IKE- \_ DOS- \_ Cookie \_ gesendet**
</dt> <dd> <dl> <dt>

13890 (0x3642)
</dt> <dt>



An Initiator gesendete DOS-Cookie benachrichtigen.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_SHUTTING_DOWN"></span><span id="error_ipsec_ike_shutting_down"></span>**Fehler beim Herunterfahren der \_ IPSec- \_ IKE. \_ \_**
</dt> <dd> <dl> <dt>

13891 (0x3643)
</dt> <dt>



Der IKE-Dienst wird heruntergefahren.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_CGA_AUTH_FAILED"></span><span id="error_ipsec_ike_cga_auth_failed"></span>**Fehler bei \_ IPSec \_ IKE \_ CGA-Authentifizierung \_ . \_**
</dt> <dd> <dl> <dt>

13892 (0x3644)
</dt> <dt>



Die Bindung zwischen der CGA-Adresse und dem Zertifikat konnte nicht überprüft werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_NATOA"></span><span id="error_ipsec_ike_process_err_natoa"></span>**Fehler \_ IPSec \_ IKE- \_ Prozess \_ Err \_ NatOA**
</dt> <dd> <dl> <dt>

13893 (0x3645)
</dt> <dt>



Fehler beim Verarbeiten der NatOA-Nutzlast.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_MM_FOR_QM"></span><span id="error_ipsec_ike_invalid_mm_for_qm"></span>**Fehler \_ IPSec \_ IKE \_ ungültige \_ mm \_ für \_ qm**
</dt> <dd> <dl> <dt>

13894 (0x3646)
</dt> <dt>



Die Parameter des Hauptmodus sind für diesen Schnellmodus ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_QM_EXPIRED"></span><span id="error_ipsec_ike_qm_expired"></span>**Fehler \_ IPSec \_ IKE \_ qm ist \_ abgelaufen.**
</dt> <dd> <dl> <dt>

13895 (0x3647)
</dt> <dt>



Der Schnellmodus-SA war vom IPSec-Treiber abgelaufen.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_TOO_MANY_FILTERS"></span><span id="error_ipsec_ike_too_many_filters"></span>**Fehler \_ IPSec \_ IKE \_ zu \_ viele \_ Filter**
</dt> <dd> <dl> <dt>

13896 (0x3648)
</dt> <dt>



Es wurden zu viele dynamisch hinzugefügte IKEEXT-Filter erkannt.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_NEG_STATUS_END"></span><span id="error_ipsec_ike_neg_status_end"></span>**Fehler \_ IPSec \_ IKE \_ NETg \_ Status \_ Ende**
</dt> <dd> <dl> <dt>

13897 (0x3649)
</dt> <dt>



Fehler \_ IPSec \_ IKE \_ NETg \_ Status \_ Ende


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_KILL_DUMMY_NAP_TUNNEL"></span><span id="error_ipsec_ike_kill_dummy_nap_tunnel"></span>**Fehler \_ IPSec \_ IKE \_ Kill \_ Dummy- \_ NAP- \_ Tunnel**
</dt> <dd> <dl> <dt>

13898 (0x364a)
</dt> <dt>



NAP-reauth war erfolgreich und muss den Dummy-NAP-IKEv2-Tunnel löschen.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INNER_IP_ASSIGNMENT_FAILURE"></span><span id="error_ipsec_ike_inner_ip_assignment_failure"></span>**Fehler bei \_ IPSec \_ \_ -internen \_ IP- \_ Zuweisungs \_ Fehlern**
</dt> <dd> <dl> <dt>

13899 (0x364b)
</dt> <dt>



Fehler beim Zuweisen der inneren IP-Adresse zum Initiator im Tunnel Modus.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_REQUIRE_CP_PAYLOAD_MISSING"></span><span id="error_ipsec_ike_require_cp_payload_missing"></span>**Fehler \_ IPSec \_ IKE \_ erfordert keine \_ CP- \_ Nutzlast \_**
</dt> <dd> <dl> <dt>

13900 (0x364c)
</dt> <dt>



Erforderliche Konfigurations Nutzlast fehlt.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_KEY_MODULE_IMPERSONATION_NEGOTIATION_PENDING"></span><span id="error_ipsec_key_module_impersonation_negotiation_pending"></span>**Fehler bei der \_ IPSec-Schlüsselmodul-Identitätswechsel \_ \_ \_ \_ Aushandlung \_ Ausstehend**
</dt> <dd> <dl> <dt>

13901 (0x364d)
</dt> <dt>



Eine Aushandlung, die als Sicherheitsprinzip ausgeführt wird, das die Verbindung ausgegeben hat, wird gerade ausgeführt.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_COEXISTENCE_SUPPRESS"></span><span id="error_ipsec_ike_coexistence_suppress"></span>**Fehler \_ IPSec- \_ IKE- \_ Koexistenz unter \_ drücken**
</dt> <dd> <dl> <dt>

13902 (0x364e)
</dt> <dt>



Die SA wurde aufgrund von ikev1/AuthIP-koexistenzunterdrücküberprüfung gelöscht.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_RATELIMIT_DROP"></span><span id="error_ipsec_ike_ratelimit_drop"></span>**Fehler \_ IPSec \_ IKE \_ ratelimit \_ Drop**
</dt> <dd> <dl> <dt>

13903 (0x364f)
</dt> <dt>



Die eingehende SA-Anforderung wurde aufgrund der Peer-IP-Adress Raten Begrenzung gelöscht.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PEER_DOESNT_SUPPORT_MOBIKE"></span><span id="error_ipsec_ike_peer_doesnt_support_mobike"></span>**Fehler \_ IPSec \_ IKE- \_ Peer \_ \_ unterstützt \_ MOBIKE nicht**
</dt> <dd> <dl> <dt>

13904 (0x3650)
</dt> <dt>



Der Peer unterstützt MOBIKE nicht.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_AUTHORIZATION_FAILURE"></span><span id="error_ipsec_ike_authorization_failure"></span>**Fehler bei \_ IPSec- \_ IKE- \_ Autorisierung \_**
</dt> <dd> <dl> <dt>

13905 (0x3651)
</dt> <dt>



Die Einrichtung der Sicherheitszuordnung ist nicht autorisiert.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_STRONG_CRED_AUTHORIZATION_FAILURE"></span><span id="error_ipsec_ike_strong_cred_authorization_failure"></span>**Fehler beim \_ \_ \_ \_ \_ Autorisierungs \_ Fehler bei IPSec-IKE (Strong).**
</dt> <dd> <dl> <dt>

13906 (0x3652)
</dt> <dt>



Die Einrichtung der SA ist nicht autorisiert, da es keine ausreichend starken PKINIT-basierten Anmelde Informationen gibt.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_AUTHORIZATION_FAILURE_WITH_OPTIONAL_RETRY"></span><span id="error_ipsec_ike_authorization_failure_with_optional_retry"></span>**Fehler \_ bei IPSec- \_ IKE- \_ Autorisierung \_ \_ mit \_ optionalem \_ Wiederholungsversuch**
</dt> <dd> <dl> <dt>

13907 (0x3653)
</dt> <dt>



Die Einrichtung der Sicherheitszuordnung ist nicht autorisiert. Möglicherweise müssen Sie aktualisierte oder andere Anmelde Informationen eingeben, z. b. eine Smartcard.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_STRONG_CRED_AUTHORIZATION_AND_CERTMAP_FAILURE"></span><span id="error_ipsec_ike_strong_cred_authorization_and_certmap_failure"></span>**Fehler bei \_ IPSec \_ -IKE \_ \_ -Autorisierung (Strong) \_ \_ und \_ certmap- \_ Fehler**
</dt> <dd> <dl> <dt>

13908 (0x3654)
</dt> <dt>



Die Einrichtung der SA ist nicht autorisiert, da es keine ausreichend starken PKINIT-basierten Anmelde Informationen gibt. Dies kann sich auf den Fehler bei der Zuordnung von Zertifikaten für das SA-Konto beziehen.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_NEG_STATUS_EXTENDED_END"></span><span id="error_ipsec_ike_neg_status_extended_end"></span>**Fehler \_ IPSec \_ IKE \_ NETg \_ Status \_ erweitert \_**
</dt> <dd> <dl> <dt>

13909 (0x3655)
</dt> <dt>



Fehler \_ IPSec \_ IKE \_ NETg \_ Status \_ erweitert \_


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_BAD_SPI"></span><span id="error_ipsec_bad_spi"></span>**Fehler \_ IPSec \_ Bad \_ SPI**
</dt> <dd> <dl> <dt>

13910 (0x3656)
</dt> <dt>



Die SPI im Paket entspricht keiner gültigen IPSec-SA.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_SA_LIFETIME_EXPIRED"></span><span id="error_ipsec_sa_lifetime_expired"></span>**Fehler bei IPSec-SA-Gültigkeits \_ \_ \_ Dauer \_**
</dt> <dd> <dl> <dt>

13911 (0x3657)
</dt> <dt>



Das Paket wurde über eine IPSec-SA empfangen, deren Lebensdauer abgelaufen ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_WRONG_SA"></span><span id="error_ipsec_wrong_sa"></span>**Fehler \_ IPSec \_ falsche \_ sa**
</dt> <dd> <dl> <dt>

13912 (0x3658)
</dt> <dt>



Das Paket wurde über eine IPSec-SA empfangen, die nicht den Paket Merkmalen entspricht.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_REPLAY_CHECK_FAILED"></span><span id="error_ipsec_replay_check_failed"></span>**Fehler beim \_ \_ \_ Überprüfen der IPSec-Wiedergabe \_**
</dt> <dd> <dl> <dt>

13913 (0x3659)
</dt> <dt>



Fehler bei der Wiedergabe Überprüfung der Paket Sequenznummer.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_INVALID_PACKET"></span><span id="error_ipsec_invalid_packet"></span>**Fehler bei \_ IPSec \_ ungültiges \_ Paket.**
</dt> <dd> <dl> <dt>

13914 (0x365a)
</dt> <dt>



Der IPSec-Header und/oder-Nachspann im Paket ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_INTEGRITY_CHECK_FAILED"></span><span id="error_ipsec_integrity_check_failed"></span>**Fehler bei der \_ IPSec- \_ Integritäts \_ Überprüfung \_ .**
</dt> <dd> <dl> <dt>

13915 (0x365b)
</dt> <dt>



Fehler bei der IPSec-Integritäts Überprüfung.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_CLEAR_TEXT_DROP"></span><span id="error_ipsec_clear_text_drop"></span>**Fehler beim \_ \_ Löschen von \_ Text in IPSec \_ .**
</dt> <dd> <dl> <dt>

13916 (0x365c)
</dt> <dt>



IPSec hat ein Klartext-Paket gelöscht.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_AUTH_FIREWALL_DROP"></span><span id="error_ipsec_auth_firewall_drop"></span>**Fehler beim \_ Löschen der IPSec-Authentifizierungs \_ \_ Firewall \_ .**
</dt> <dd> <dl> <dt>

13917 (0x365d)
</dt> <dt>



IPSec hat ein eingehender ESP-Paket im authentifizierten Firewallmodus gelöscht. Diese Ablage ist unbedenklich.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_THROTTLE_DROP"></span><span id="error_ipsec_throttle_drop"></span>**Fehler bei der \_ IPSec- \_ Drosselung \_**
</dt> <dd> <dl> <dt>

13918 (0x365e)
</dt> <dt>



IPSec hat ein Paket aufgrund der DOS-Drosselung gelöscht.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_DOSP_BLOCK"></span><span id="error_ipsec_dosp_block"></span>**Fehler \_ IPSec- \_ DoSP- \_ Block**
</dt> <dd> <dl> <dt>

13925 (0x3665)
</dt> <dt>



Der IPSec-DOS-Schutz entsprach einer expliziten blockregel.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_DOSP_RECEIVED_MULTICAST"></span><span id="error_ipsec_dosp_received_multicast"></span>**Fehler \_ IPSec- \_ DoSP- \_ \_ Multicast empfangen**
</dt> <dd> <dl> <dt>

13926 (0x3666)
</dt> <dt>



IPSec-DOS-Schutz hat ein IPSec-spezifisches Multicast Paket empfangen, das nicht zulässig ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_DOSP_INVALID_PACKET"></span><span id="error_ipsec_dosp_invalid_packet"></span>**Fehler bei \_ IPSec- \_ DoSP- \_ Paket ist ungültig \_ .**
</dt> <dd> <dl> <dt>

13927 (0x3667)
</dt> <dt>



Der IPSec-DOS-Schutz hat ein falsch formatiertes Paket empfangen.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_DOSP_STATE_LOOKUP_FAILED"></span><span id="error_ipsec_dosp_state_lookup_failed"></span>**Fehler bei der \_ IPSec- \_ DoSP- \_ Status \_ Suche \_ .**
</dt> <dd> <dl> <dt>

13928 (0x3668)
</dt> <dt>



Der IPSec-DOS-Schutz konnte den Status nicht nachschlagen.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_DOSP_MAX_ENTRIES"></span><span id="error_ipsec_dosp_max_entries"></span>**Fehler bei \_ IPSec- \_ DoSP- \_ maximalen \_ Einträgen**
</dt> <dd> <dl> <dt>

13929 (0x3669)
</dt> <dt>



Der IPSec-DOS-Schutz konnte den Status nicht erstellen, da die maximale Anzahl von Einträgen, die von der Richtlinie zugelassen werden, erreicht


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_DOSP_KEYMOD_NOT_ALLOWED"></span><span id="error_ipsec_dosp_keymod_not_allowed"></span>**Fehler \_ IPSec \_ DoSP \_ keymod ist \_ nicht \_ zulässig.**
</dt> <dd> <dl> <dt>

13930 (0x366a)
</dt> <dt>



IPSec-DOS-Schutz hat ein IPSec-Aushandlungs Paket für ein Schlüssel Verwaltungsmodul empfangen, das von der Richtlinie nicht zugelassen wird.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_DOSP_NOT_INSTALLED"></span><span id="error_ipsec_dosp_not_installed"></span>**Fehler beim \_ Installieren von IPSec- \_ DoSP. \_ \_**
</dt> <dd> <dl> <dt>

13931 (0x366b)
</dt> <dt>



IPSec-DOS-Schutz wurde nicht aktiviert.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_DOSP_MAX_PER_IP_RATELIMIT_QUEUES"></span><span id="error_ipsec_dosp_max_per_ip_ratelimit_queues"></span>**Fehler \_ IPSec \_ DoSP \_ Max \_ pro \_ IP- \_ \_ Warteschlangen**
</dt> <dd> <dl> <dt>

13932 (0x366c)
</dt> <dt>



Der IPSec-DOS-Schutz konnte eine interne IP-Raten Limit-Warteschlange nicht erstellen, da die von der Richtlinie zugelassene maximale Anzahl von Warteschlangen erreicht wurde.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_SECTION_NOT_FOUND"></span><span id="error_sxs_section_not_found"></span>**Fehler \_ SxS- \_ Abschnitt \_ nicht \_ gefunden.**
</dt> <dd> <dl> <dt>

14000 (0x36b0)
</dt> <dt>



Der angeforderte Abschnitt war im Aktivierungs Kontext nicht vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_CANT_GEN_ACTCTX"></span><span id="error_sxs_cant_gen_actctx"></span>**Fehler \_ SxS \_ cant \_ gen \_ ActCtx**
</dt> <dd> <dl> <dt>

14001 (0x36b1)
</dt> <dt>



Die Anwendung konnte nicht gestartet werden, da die Seite-an-Seite-Konfiguration nicht korrekt ist. Ausführlichere Informationen finden Sie im Anwendungs Ereignisprotokoll, oder verwenden Sie das Befehlszeilen sxstrace.exe-Tool.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_INVALID_ACTCTXDATA_FORMAT"></span><span id="error_sxs_invalid_actctxdata_format"></span>**Fehler \_ SxS \_ ungültiges \_ actctxdata- \_ Format.**
</dt> <dd> <dl> <dt>

14002 (0x36b2)
</dt> <dt>



Das Datenformat der Anwendungs Bindung ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_ASSEMBLY_NOT_FOUND"></span><span id="error_sxs_assembly_not_found"></span>**Fehler \_ SxS- \_ Assembly \_ nicht \_ gefunden.**
</dt> <dd> <dl> <dt>

14003 (0x36b3)
</dt> <dt>



Die Assembly, auf die verwiesen wird, ist nicht auf dem System installiert.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_MANIFEST_FORMAT_ERROR"></span><span id="error_sxs_manifest_format_error"></span>**Fehler im \_ SxS- \_ Manifest- \_ Format \_ .**
</dt> <dd> <dl> <dt>

14004 (0x36b4)
</dt> <dt>



Die Manifest-Datei beginnt nicht mit den erforderlichen Tags und Formatierungsinformationen.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_MANIFEST_PARSE_ERROR"></span><span id="error_sxs_manifest_parse_error"></span>**Fehler beim Analysieren des Fehler \_ SxS- \_ Manifests. \_ \_**
</dt> <dd> <dl> <dt>

14005 (0x36b5)
</dt> <dt>



Die Manifest-Datei enthält mindestens einen Syntax Fehler.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_ACTIVATION_CONTEXT_DISABLED"></span><span id="error_sxs_activation_context_disabled"></span>**Fehler \_ SxS- \_ Aktivierungs \_ Kontext \_ deaktiviert**
</dt> <dd> <dl> <dt>

14006 (0x36b6)
</dt> <dt>



Die Anwendung hat versucht, einen deaktivierten Aktivierungs Kontext zu aktivieren.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_KEY_NOT_FOUND"></span><span id="error_sxs_key_not_found"></span>**Fehler \_ SxS- \_ Schlüssel wurde \_ nicht \_ gefunden.**
</dt> <dd> <dl> <dt>

14007 (0x36b7)
</dt> <dt>



Der angeforderte Suchschlüssel wurde in keinem aktiven Aktivierungs Kontext gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_VERSION_CONFLICT"></span><span id="error_sxs_version_conflict"></span>**Fehler \_ SxS- \_ Versions \_ Konflikt**
</dt> <dd> <dl> <dt>

14008 (0x36b8)
</dt> <dt>



Eine Komponenten Version, die für die Anwendung erforderlich ist, steht in Konflikt mit einer anderen bereits aktiven Komponenten Version.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_WRONG_SECTION_TYPE"></span><span id="error_sxs_wrong_section_type"></span>**Fehler \_ SxS- \_ falscher \_ Abschnitts \_ Typ**
</dt> <dd> <dl> <dt>

14009 (0x36b9)
</dt> <dt>



Der vom Typ angeforderte Aktivierungs Kontext Abschnitt entspricht nicht der verwendeten Abfrage-API.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_THREAD_QUERIES_DISABLED"></span><span id="error_sxs_thread_queries_disabled"></span>**Fehler \_ SxS- \_ Thread \_ Abfragen \_ deaktiviert**
</dt> <dd> <dl> <dt>

14010 (0x36ba)
</dt> <dt>



Fehlende Systemressourcen erfordern, dass die isolierte Aktivierung für den aktuellen Ausführungs Thread deaktiviert ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_PROCESS_DEFAULT_ALREADY_SET"></span><span id="error_sxs_process_default_already_set"></span>**Fehler \_ SxS- \_ Prozess \_ Standard ist \_ bereits \_ festgelegt.**
</dt> <dd> <dl> <dt>

14011 (0x36bb)
</dt> <dt>



Fehler beim Festlegen des Standard Aktivierungs Kontexts für den Prozess, weil der standardmäßige Aktivierungs Kontext der Prozesse bereits festgelegt wurde.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_UNKNOWN_ENCODING_GROUP"></span><span id="error_sxs_unknown_encoding_group"></span>**Fehler \_ SxS \_ unbekannte \_ Codierungs \_ Gruppe**
</dt> <dd> <dl> <dt>

14012 (0x36bc)
</dt> <dt>



Der angegebene Codierungs Gruppen Bezeichner wurde nicht erkannt.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_UNKNOWN_ENCODING"></span><span id="error_sxs_unknown_encoding"></span>**Fehler \_ SxS \_ unbekannte \_ Codierung.**
</dt> <dd> <dl> <dt>

14013 (0x36bd)
</dt> <dt>



Die angeforderte Codierung wird nicht erkannt.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_INVALID_XML_NAMESPACE_URI"></span><span id="error_sxs_invalid_xml_namespace_uri"></span>**Fehler \_ SxS \_ ungültiger \_ XML- \_ Namespace- \_ URI.**
</dt> <dd> <dl> <dt>

14014 (0x36be)
</dt> <dt>



Das Manifest enthält einen Verweis auf einen ungültigen URI.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_ROOT_MANIFEST_DEPENDENCY_NOT_INSTALLED"></span><span id="error_sxs_root_manifest_dependency_not_installed"></span>**Fehler \_ SxS-Stamm \_ \_ Manifest- \_ Abhängigkeit \_ nicht \_ installiert**
</dt> <dd> <dl> <dt>

14015 (0x36bf)
</dt> <dt>



Das Anwendungs Manifest enthält einen Verweis auf eine abhängige Assembly, die nicht installiert ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_LEAF_MANIFEST_DEPENDENCY_NOT_INSTALLED"></span><span id="error_sxs_leaf_manifest_dependency_not_installed"></span>**Fehler \_ SxS- \_ Blatt \_ Manifest- \_ Abhängigkeit \_ nicht \_ installiert**
</dt> <dd> <dl> <dt>

14016 (0x36c0)
</dt> <dt>



Das Manifest für eine Assembly, die von der Anwendung verwendet wird, verfügt über einen Verweis auf eine abhängige Assembly, die nicht installiert ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_INVALID_ASSEMBLY_IDENTITY_ATTRIBUTE"></span><span id="error_sxs_invalid_assembly_identity_attribute"></span>**Fehler \_ SxS \_ ungültiges Attribut für Assemblyidentität. \_ \_ \_**
</dt> <dd> <dl> <dt>

14017 (0x36c1)
</dt> <dt>



Das Manifest enthält ein ungültiges Attribut für die Assemblyidentität.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_MANIFEST_MISSING_REQUIRED_DEFAULT_NAMESPACE"></span><span id="error_sxs_manifest_missing_required_default_namespace"></span>**Fehler im \_ SxS- \_ Manifest \_ fehlt der \_ erforderliche \_ Standard \_ Namespace.**
</dt> <dd> <dl> <dt>

14018 (0x36c2)
</dt> <dt>



Im Manifest fehlt die erforderliche Standard Namespace Spezifikation für das Assemblyelement.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_MANIFEST_INVALID_REQUIRED_DEFAULT_NAMESPACE"></span><span id="error_sxs_manifest_invalid_required_default_namespace"></span>**Fehler \_ SxS- \_ Manifest \_ ungültiger \_ Erforderlicher \_ Standard \_ Namespace**
</dt> <dd> <dl> <dt>

14019 (0x36c3)
</dt> <dt>



Im Manifest ist ein Standard Namespace für das Assembly-Element angegeben, aber sein Wert ist nicht "urn: Schemas-Microsoft-com: ASM. v1".


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_PRIVATE_MANIFEST_CROSS_PATH_WITH_REPARSE_POINT"></span><span id="error_sxs_private_manifest_cross_path_with_reparse_point"></span>**Fehler \_ SxS \_ - \_ Kreuz Pfad des privaten Manifests \_ \_ mit Analyse \_ \_ \_ Punkt**
</dt> <dd> <dl> <dt>

14020 (0x36c4)
</dt> <dt>



Das überprüfte private Manifest hat einen Pfad mit einem nicht unterstützten Analyse Punkt überschritten.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_DUPLICATE_DLL_NAME"></span><span id="error_sxs_duplicate_dll_name"></span>**Fehler \_ SxS \_ doppelte \_ dll- \_ Name**
</dt> <dd> <dl> <dt>

14021 (0x36c5)
</dt> <dt>



Bei mindestens zwei Komponenten, auf die direkt oder indirekt durch das Anwendungs Manifest verwiesen wird, sind Dateien mit demselben Namen vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_DUPLICATE_WINDOWCLASS_NAME"></span><span id="error_sxs_duplicate_windowclass_name"></span>**Fehler \_ SxS \_ doppelte \_ WindowClass- \_ Name**
</dt> <dd> <dl> <dt>

14022 (0x36c6)
</dt> <dt>



Mindestens zwei Komponenten, auf die direkt oder indirekt durch das Anwendungs Manifest verwiesen wird, verfügen über Fenster Klassen mit demselben Namen.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_DUPLICATE_CLSID"></span><span id="error_sxs_duplicate_clsid"></span>**Fehler \_ SxS \_ doppelte \_ CLSID**
</dt> <dd> <dl> <dt>

14023 (0x36c7)
</dt> <dt>



Mindestens zwei Komponenten, auf die direkt oder indirekt durch das Anwendungs Manifest verwiesen wird, verfügen über die gleichen com-Server-CLSIDs.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_DUPLICATE_IID"></span><span id="error_sxs_duplicate_iid"></span>**Fehler \_ SxS \_ doppelte \_ IID.**
</dt> <dd> <dl> <dt>

14024 (0x36c8)
</dt> <dt>



Mindestens zwei Komponenten, auf die direkt oder indirekt durch das Anwendungs Manifest verwiesen wird, haben Proxys für die gleichen com-Schnittstellen-IIDs.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_DUPLICATE_TLBID"></span><span id="error_sxs_duplicate_tlbid"></span>**Fehler \_ SxS \_ doppelte \_ TLBID**
</dt> <dd> <dl> <dt>

14025 (0x36c9)
</dt> <dt>



Mindestens zwei Komponenten, auf die direkt oder indirekt durch das Anwendungs Manifest verwiesen wird, verfügen über die gleichen com-Typbibliotheks-tlgebote.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_DUPLICATE_PROGID"></span><span id="error_sxs_duplicate_progid"></span>**Fehler \_ SxS \_ doppelte \_ ProgID**
</dt> <dd> <dl> <dt>

14026 (0x36ca)
</dt> <dt>



Mindestens zwei Komponenten, auf die direkt oder indirekt durch das Anwendungs Manifest verwiesen wird, verfügen über dieselben com-ProgIDs.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_DUPLICATE_ASSEMBLY_NAME"></span><span id="error_sxs_duplicate_assembly_name"></span>**Fehler \_ SxS \_ doppelte \_ AssemblyName \_**
</dt> <dd> <dl> <dt>

14027 (0x36cb)
</dt> <dt>



Mindestens zwei Komponenten, auf die direkt oder indirekt durch das Anwendungs Manifest verwiesen wird, sind unterschiedliche Versionen derselben Komponente, die nicht zulässig sind.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_FILE_HASH_MISMATCH"></span><span id="error_sxs_file_hash_mismatch"></span>**Fehler bei \_ SxS- \_ Datei \_ Hash \_ Konflikt.**
</dt> <dd> <dl> <dt>

14028 (0x36cc)
</dt> <dt>



Die Datei einer Komponente entspricht nicht den Überprüfungs Informationen, die im Komponenten Manifest vorhanden sind.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_POLICY_PARSE_ERROR"></span><span id="error_sxs_policy_parse_error"></span>**Fehler beim \_ Analysieren der SxS- \_ Richtlinie. \_ \_**
</dt> <dd> <dl> <dt>

14029 (0x36cd)
</dt> <dt>



Das Richtlinien Manifest enthält mindestens einen Syntax Fehler.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_MISSINGQUOTE"></span><span id="error_sxs_xml_e_missingquote"></span>**Fehler \_ SxS \_ XML \_ E \_ missingquote**
</dt> <dd> <dl> <dt>

14030 (0x36ce)
</dt> <dt>



Manifeste-Analysefehler: Es wurde ein Zeichenfolgenliteral erwartet, aber es wurde kein öffnendes Anführungszeichen gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_COMMENTSYNTAX"></span><span id="error_sxs_xml_e_commentsyntax"></span>**Fehler \_ SxS \_ XML \_ E \_ commentsyntax**
</dt> <dd> <dl> <dt>

14031 (0x36cf)
</dt> <dt>



Fehler beim Analysieren der Manifeste: in einem Kommentar wurde eine falsche Syntax verwendet.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_BADSTARTNAMECHAR"></span><span id="error_sxs_xml_e_badstartnamechar"></span>**Fehler \_ SxS \_ XML \_ E \_ badstartnamechar**
</dt> <dd> <dl> <dt>

14032 (0x36d0)
</dt> <dt>



Fehler beim Analysieren der Manifeste: ein Name wurde mit einem ungültigen Zeichen gestartet.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_BADNAMECHAR"></span><span id="error_sxs_xml_e_badnamechar"></span>**Fehler \_ SxS \_ XML \_ E \_ badnamechar**
</dt> <dd> <dl> <dt>

14033 (0x36d1)
</dt> <dt>



Fehler beim Analysieren der Manifeste: ein Name enthielt ein ungültiges Zeichen.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_BADCHARINSTRING"></span><span id="error_sxs_xml_e_badcharinstring"></span>**Fehler \_ SxS \_ XML \_ E \_ badcharinstring**
</dt> <dd> <dl> <dt>

14034 (0x36d2)
</dt> <dt>



Fehler beim Analysieren der Manifeste: ein zeichenfolgenal enthielt ein ungültiges Zeichen.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_XMLDECLSYNTAX"></span><span id="error_sxs_xml_e_xmldeclsyntax"></span>**Fehler \_ SxS \_ XML \_ E \_ xmldeclsyntax**
</dt> <dd> <dl> <dt>

14035 (0x36d3)
</dt> <dt>



Fehler beim Analysieren der Manifeste: Ungültige Syntax für eine XML-Deklaration.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_BADCHARDATA"></span><span id="error_sxs_xml_e_badchardata"></span>**Fehler \_ SxS \_ XML \_ E \_ badchardata**
</dt> <dd> <dl> <dt>

14036 (0x36d4)
</dt> <dt>



Fehler beim Analysieren der Manifeste: im Text Inhalt wurde ein ungültiges Zeichen gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_MISSINGWHITESPACE"></span><span id="error_sxs_xml_e_missingwhitespace"></span>**Fehler \_ SxS \_ XML \_ E \_ missingwhitespace**
</dt> <dd> <dl> <dt>

14037 (0x36d5)
</dt> <dt>



Fehler beim Analysieren der Manifeste: erforderlicher Leerraum fehlte.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_EXPECTINGTAGEND"></span><span id="error_sxs_xml_e_expectingtagend"></span>**Fehler \_ SxS \_ XML \_ E \_ expectingtagend**
</dt> <dd> <dl> <dt>

14038 (0x36d6)
</dt> <dt>



Fehler beim Analysieren der Manifeste: das Zeichen ">" wurde erwartet.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_MISSINGSEMICOLON"></span><span id="error_sxs_xml_e_missingsemicolon"></span>**Fehler \_ SxS \_ XML \_ E \_ missingsemikolon**
</dt> <dd> <dl> <dt>

14039 (0x36d7)
</dt> <dt>



Fehler beim Analysieren der Manifeste: ein Semikolon wurde erwartet.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_UNBALANCEDPAREN"></span><span id="error_sxs_xml_e_unbalancedparen"></span>**Fehler \_ SxS \_ XML \_ E \_ unbalancedparser**
</dt> <dd> <dl> <dt>

14040 (0x36d8)
</dt> <dt>



Fehler beim Analysieren der Manifeste: Klammern sind nicht ausgeglichen.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_INTERNALERROR"></span><span id="error_sxs_xml_e_internalerror"></span>**Fehler \_ SxS \_ XML \_ E \_ InternalError**
</dt> <dd> <dl> <dt>

14041 (0x36d9)
</dt> <dt>



Fehler beim Analysieren der Manifeste: Interner Fehler.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_UNEXPECTED_WHITESPACE"></span><span id="error_sxs_xml_e_unexpected_whitespace"></span>**Fehler \_ SxS \_ XML \_ E \_ unerwartetes \_ Leerzeichen**
</dt> <dd> <dl> <dt>

14042 (0x36da)
</dt> <dt>



Fehler beim Analysieren der Manifeste: an dieser Stelle ist kein Leerzeichen zulässig.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_INCOMPLETE_ENCODING"></span><span id="error_sxs_xml_e_incomplete_encoding"></span>**Fehler \_ SxS \_ XML \_ E \_ unvollständige \_ Codierung**
</dt> <dd> <dl> <dt>

14043 (0x36db)
</dt> <dt>



Fehler beim Analysieren der Manifeste: das Dateiende wurde in einem ungültigen Zustand für die aktuelle Codierung erreicht.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_MISSING_PAREN"></span><span id="error_sxs_xml_e_missing_paren"></span>**Fehler \_ SxS \_ XML \_ E \_ fehlende \_ Parser**
</dt> <dd> <dl> <dt>

14044 (0x36dc)
</dt> <dt>



Fehler beim Analysieren der Manifeste: Klammer fehlt.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_EXPECTINGCLOSEQUOTE"></span><span id="error_sxs_xml_e_expectingclosequote"></span>**Fehler \_ SxS \_ XML \_ E \_ expectingclosequote**
</dt> <dd> <dl> <dt>

14045 (0x36dd)
</dt> <dt>



Fehler beim Analysieren der Manifeste: ein einzelnes oder doppeltes Schließ Endes Anführungszeichen ( \\ "or \\ ") fehlt.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_MULTIPLE_COLONS"></span><span id="error_sxs_xml_e_multiple_colons"></span>**Fehler \_ SxS \_ XML \_ E \_ mehrere \_ Doppelpunkte**
</dt> <dd> <dl> <dt>

14046 (0x36de)
</dt> <dt>



Fehler beim Analysieren der Manifeste: mehrere Doppelpunkte sind in einem Namen nicht zulässig.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_INVALID_DECIMAL"></span><span id="error_sxs_xml_e_invalid_decimal"></span>**Fehler \_ SxS \_ XML \_ E \_ ungültiges \_ Dezimalzeichen**
</dt> <dd> <dl> <dt>

14047 (0x36df)
</dt> <dt>



Fehler beim Analysieren der Manifeste: Ungültiges Zeichen für Dezimalzahl.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_INVALID_HEXIDECIMAL"></span><span id="error_sxs_xml_e_invalid_hexidecimal"></span>**Fehler \_ SxS \_ XML \_ E \_ ungültiges \_ hexadezimal**
</dt> <dd> <dl> <dt>

14048 (0x36e0)
</dt> <dt>



Fehler beim Analysieren der Manifeste: Ungültiges Zeichen für hexadezimale Ziffer.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_INVALID_UNICODE"></span><span id="error_sxs_xml_e_invalid_unicode"></span>**Fehler \_ SxS \_ XML \_ E \_ ungültige \_ Unicode**
</dt> <dd> <dl> <dt>

14049 (0x36e1)
</dt> <dt>



Fehler beim Analysieren der Manifeste: Ungültiger Unicode-Zeichen Wert für diese Plattform.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_WHITESPACEORQUESTIONMARK"></span><span id="error_sxs_xml_e_whitespaceorquestionmark"></span>**Fehler \_ SxS \_ XML \_ E \_ whitespaceorfrag Mark**
</dt> <dd> <dl> <dt>

14050 (0x36e2)
</dt> <dt>



Fehler beim Analysieren der Manifeste: Es wird ein Leerzeichen oder "?" erwartet.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_UNEXPECTEDENDTAG"></span><span id="error_sxs_xml_e_unexpectedendtag"></span>**Fehler \_ SxS \_ XML \_ E \_ unexpectedendtag**
</dt> <dd> <dl> <dt>

14051 (0x36e3)
</dt> <dt>



Fehler beim Analysieren der Manifeste: an dieser Stelle wurde kein Endtag erwartet.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_UNCLOSEDTAG"></span><span id="error_sxs_xml_e_unclosedtag"></span>**Fehler \_ SxS \_ XML \_ E \_ unclosedtag**
</dt> <dd> <dl> <dt>

14052 (0x36e4)
</dt> <dt>



Fehler beim Analysieren der Manifeste: die folgenden Tags wurden nicht geschlossen: %1.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_DUPLICATEATTRIBUTE"></span><span id="error_sxs_xml_e_duplicateattribute"></span>**Fehler \_ SxS \_ XML \_ E \_ duplicateattribute**
</dt> <dd> <dl> <dt>

14053 (0x36e5)
</dt> <dt>



Fehler beim Analysieren der Manifeste: doppeltes Attribut.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_MULTIPLEROOTS"></span><span id="error_sxs_xml_e_multipleroots"></span>**Fehler \_ SxS \_ XML \_ E \_ multipleroots**
</dt> <dd> <dl> <dt>

14054 (0x36e6)
</dt> <dt>



Fehler beim Analysieren der Manifeste: in einem XML-Dokument ist nur ein Element der obersten Ebene zulässig.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_INVALIDATROOTLEVEL"></span><span id="error_sxs_xml_e_invalidatrootlevel"></span>**Fehler \_ SxS \_ XML \_ E \_ invalidatrootlevel**
</dt> <dd> <dl> <dt>

14055 (0x36e7)
</dt> <dt>



Fehler beim Analysieren der Manifeste: auf oberster Ebene des Dokuments ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_BADXMLDECL"></span><span id="error_sxs_xml_e_badxmldecl"></span>**Fehler \_ SxS \_ XML \_ E \_ badxmldecl**
</dt> <dd> <dl> <dt>

14056 (0x36e8)
</dt> <dt>



Fehler beim Analysieren der Manifeste: Ungültige XML-Deklaration.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_MISSINGROOT"></span><span id="error_sxs_xml_e_missingroot"></span>**Fehler \_ SxS \_ XML \_ E \_ missingroot**
</dt> <dd> <dl> <dt>

14057 (0x36e9)
</dt> <dt>



Fehler beim Analysieren der Manifeste: das XML-Dokument muss ein Element der obersten Ebene aufweisen.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_UNEXPECTEDEOF"></span><span id="error_sxs_xml_e_unexpectedeof"></span>**Fehler \_ SxS \_ XML \_ E \_ unexpectedeof**
</dt> <dd> <dl> <dt>

14058 (0x36ea)
</dt> <dt>



Fehler beim Analysieren der Manifeste: Unerwartetes Dateiende.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_BADPEREFINSUBSET"></span><span id="error_sxs_xml_e_badperefinsubset"></span>**Fehler \_ SxS \_ XML \_ E \_ badperefinsubset**
</dt> <dd> <dl> <dt>

14059 (0x36eb)
</dt> <dt>



Fehler beim Analysieren der Manifeste: Parameter Entitäten können nicht innerhalb von Markup Deklarationen in einer internen Teilmenge verwendet werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_UNCLOSEDSTARTTAG"></span><span id="error_sxs_xml_e_unclosedstarttag"></span>**Fehler \_ SxS \_ XML \_ E \_ unclosedstarttag**
</dt> <dd> <dl> <dt>

14060 (0x36ec)
</dt> <dt>



Fehler beim Analysieren der Manifeste: das Element wurde nicht geschlossen.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_UNCLOSEDENDTAG"></span><span id="error_sxs_xml_e_unclosedendtag"></span>**Fehler \_ SxS \_ XML \_ E \_ unclosedendtag**
</dt> <dd> <dl> <dt>

14061 (0x36ed)
</dt> <dt>



Fehler beim Analysieren der Manifeste: das Endelement hat das Zeichen ' > ' fehlt.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_UNCLOSEDSTRING"></span><span id="error_sxs_xml_e_unclosedstring"></span>**Fehler \_ SxS \_ XML \_ E \_ unclosedstring**
</dt> <dd> <dl> <dt>

14062 (0x36ee)
</dt> <dt>



Fehler beim Analysieren der Manifeste: ein Zeichenfolgenliteral wurde nicht geschlossen.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_UNCLOSEDCOMMENT"></span><span id="error_sxs_xml_e_unclosedcomment"></span>**Fehler \_ SxS \_ XML \_ E \_ unclosedcomment**
</dt> <dd> <dl> <dt>

14063 (0x36ef)
</dt> <dt>



Fehler beim Analysieren der Manifeste: ein Kommentar wurde nicht geschlossen.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_UNCLOSEDDECL"></span><span id="error_sxs_xml_e_uncloseddecl"></span>**Fehler \_ SxS \_ XML \_ E \_ uncloseddecl**
</dt> <dd> <dl> <dt>

14064 (0x36f 0)
</dt> <dt>



Fehler beim Analysieren der Manifeste: eine Deklaration wurde nicht geschlossen.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_UNCLOSEDCDATA"></span><span id="error_sxs_xml_e_unclosedcdata"></span>**Fehler \_ SxS \_ XML \_ E \_ unclosedcdata**
</dt> <dd> <dl> <dt>

14065 (0x36f 1)
</dt> <dt>



Fehler beim Analysieren der Manifeste: ein CDATA-Abschnitt wurde nicht geschlossen.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_RESERVEDNAMESPACE"></span><span id="error_sxs_xml_e_reservednamespace"></span>**Fehler \_ SxS \_ XML \_ E \_ reservednamespace**
</dt> <dd> <dl> <dt>

14066 (0x36f 2)
</dt> <dt>



Fehler beim Analysieren der Manifeste: das Namespace Präfix darf nicht mit der reservierten Zeichenfolge "XML" beginnen.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_INVALIDENCODING"></span><span id="error_sxs_xml_e_invalidencoding"></span>**Fehler \_ SxS \_ XML \_ E \_ invalidencoding**
</dt> <dd> <dl> <dt>

14067 (0x36f 3)
</dt> <dt>



Fehler beim Analysieren der Manifeste: das System unterstützt die angegebene Codierung nicht.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_INVALIDSWITCH"></span><span id="error_sxs_xml_e_invalidswitch"></span>**Fehler \_ SxS \_ XML \_ E \_ invalidswitch**
</dt> <dd> <dl> <dt>

14068 (0x36f 4)
</dt> <dt>



Fehler beim Analysieren der Manifeste: der Wechsel von der aktuellen Codierung zur angegebenen Codierung wird nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_BADXMLCASE"></span><span id="error_sxs_xml_e_badxmlcase"></span>**Fehler \_ SxS \_ XML \_ E \_ badxmlcase**
</dt> <dd> <dl> <dt>

14069 (0x36f 5)
</dt> <dt>



Fehler beim Analysieren der Manifeste: der Name "XML" ist reserviert und muss in Kleinbuchstaben vorliegen.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_INVALID_STANDALONE"></span><span id="error_sxs_xml_e_invalid_standalone"></span>**Fehler \_ SxS \_ XML \_ E \_ ungültiges \_ eigenständiges**
</dt> <dd> <dl> <dt>

14070 (0x36f 6)
</dt> <dt>



Fehler beim Analysieren der Manifeste: das eigenständige Attribut muss den Wert "yes" oder "No" aufweisen.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_UNEXPECTED_STANDALONE"></span><span id="error_sxs_xml_e_unexpected_standalone"></span>**Fehler \_ SxS \_ XML \_ E \_ unerwartet \_ eigenständig**
</dt> <dd> <dl> <dt>

14071 (0x36f 7)
</dt> <dt>



Fehler beim Analysieren der Manifeste: das eigenständige Attribut kann nicht in externen Entitäten verwendet werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_INVALID_VERSION"></span><span id="error_sxs_xml_e_invalid_version"></span>**Fehler \_ SxS \_ XML \_ E \_ ungültige \_ Version.**
</dt> <dd> <dl> <dt>

14072 (0x36f 8)
</dt> <dt>



Fehler beim Analysieren der Manifeste: Ungültige Versionsnummer.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_MISSINGEQUALS"></span><span id="error_sxs_xml_e_missingequals"></span>**Fehler \_ SxS \_ XML \_ E \_ missingequals**
</dt> <dd> <dl> <dt>

14073 (0x36f 9)
</dt> <dt>



Fehler beim Analysieren der Manifeste: Fehlendes Gleichheitszeichen zwischen Attribut und Attribut Wert.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_PROTECTION_RECOVERY_FAILED"></span><span id="error_sxs_protection_recovery_failed"></span>**Fehler beim Wiederherstellen des \_ SxS- \_ Schutzes. \_ \_**
</dt> <dd> <dl> <dt>

14074 (0x36fa)
</dt> <dt>



Fehler beim assemblyschutz: die angegebene Assembly kann nicht wieder hergestellt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_PROTECTION_PUBLIC_KEY_TOO_SHORT"></span><span id="error_sxs_protection_public_key_too_short"></span>**Fehler \_ SxS- \_ Schutz \_ öffentlicher \_ Schlüssel \_ zu \_ kurz**
</dt> <dd> <dl> <dt>

14075 (0x36fb)
</dt> <dt>



Fehler beim assemblyschutz: der öffentliche Schlüssel für eine Assembly war zu kurz, um zugelassen zu werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_PROTECTION_CATALOG_NOT_VALID"></span><span id="error_sxs_protection_catalog_not_valid"></span>**Fehler \_ SxS \_ - \_ Schutz \_ Katalog \_ ungültig**
</dt> <dd> <dl> <dt>

14076 (0x36fc)
</dt> <dt>



Fehler beim assemblyschutz: der Katalog für eine Assembly ist ungültig oder entspricht nicht dem Assemblymanifest.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_UNTRANSLATABLE_HRESULT"></span><span id="error_sxs_untranslatable_hresult"></span>**Fehler \_ SxS \_ nicht übersetz bares \_ HRESULT**
</dt> <dd> <dl> <dt>

14077 (0x36fd)
</dt> <dt>



Ein HRESULT konnte nicht in einen entsprechenden Win32-Fehlercode übersetzt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_PROTECTION_CATALOG_FILE_MISSING"></span><span id="error_sxs_protection_catalog_file_missing"></span>**Fehler " \_ SxS \_ Protection \_ catalog \_ file" \_ fehlt.**
</dt> <dd> <dl> <dt>

14078 (0x36fe)
</dt> <dt>



Fehler beim assemblyschutz: der Katalog für eine Assembly fehlt.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_MISSING_ASSEMBLY_IDENTITY_ATTRIBUTE"></span><span id="error_sxs_missing_assembly_identity_attribute"></span>**Fehler \_ SxS \_ fehlende \_ Assembly- \_ Identitäts \_ Attribut**
</dt> <dd> <dl> <dt>

14079 (0x36ff)
</dt> <dt>



In der angegebenen Assemblyidentität fehlt mindestens ein Attribut, das in diesem Kontext vorhanden sein muss.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_INVALID_ASSEMBLY_IDENTITY_ATTRIBUTE_NAME"></span><span id="error_sxs_invalid_assembly_identity_attribute_name"></span>**Fehler \_ SxS \_ Ungültiger assemblyidentitäts- \_ \_ \_ Attribut \_ Name**
</dt> <dd> <dl> <dt>

14080 (0x3700)
</dt> <dt>



Die angegebene Assemblyidentität verfügt über einen oder mehrere Attributnamen, die Zeichen enthalten, die in XML-Namen nicht zulässig sind.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_ASSEMBLY_MISSING"></span><span id="error_sxs_assembly_missing"></span>**Fehler \_ SxS- \_ Assembly \_ fehlt.**
</dt> <dd> <dl> <dt>

14081 (0x3701)
</dt> <dt>



Die Assembly, auf die verwiesen wird, wurde nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_CORRUPT_ACTIVATION_STACK"></span><span id="error_sxs_corrupt_activation_stack"></span>**Fehler \_ SxS \_ beschädigte \_ Aktivierungs \_ Stapel**
</dt> <dd> <dl> <dt>

14082 (0x3702)
</dt> <dt>



Der Aktivierungs Kontext-Aktivierungs Stapel für den Ausführungs Thread der Ausführung ist beschädigt.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_CORRUPTION"></span><span id="error_sxs_corruption"></span>**Fehler \_ SxS-Beschädigung \_**
</dt> <dd> <dl> <dt>

14083 (0x3703)
</dt> <dt>



Die anwendungsisolations-Metadaten für diesen Prozess oder Thread sind beschädigt.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_EARLY_DEACTIVATION"></span><span id="error_sxs_early_deactivation"></span>**Fehler \_ SxS \_ frühe \_ Deaktivierung**
</dt> <dd> <dl> <dt>

14084 (0x3704)
</dt> <dt>



Der aktivierte Aktivierungs Kontext ist nicht der zuletzt aktivierte Aktivierungs Kontext.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_INVALID_DEACTIVATION"></span><span id="error_sxs_invalid_deactivation"></span>**Fehler \_ SxS \_ - \_ Deaktivierung ist ungültig.**
</dt> <dd> <dl> <dt>

14085 (0x3705)
</dt> <dt>



Der aktivierte Aktivierungs Kontext ist für den aktuellen Ausführungs Thread nicht aktiv.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_MULTIPLE_DEACTIVATION"></span><span id="error_sxs_multiple_deactivation"></span>**Fehler \_ SxS \_ Multiple \_ Deactivation**
</dt> <dd> <dl> <dt>

14086 (0x3706)
</dt> <dt>



Der aktivierte Aktivierungs Kontext wurde bereits deaktiviert.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_PROCESS_TERMINATION_REQUESTED"></span><span id="error_sxs_process_termination_requested"></span>**Fehler beim Beenden des \_ SxS- \_ Prozesses. \_ \_**
</dt> <dd> <dl> <dt>

14087 (0x3707)
</dt> <dt>



Eine Komponente, die von der Isolations Funktion verwendet wird, hat das Beenden des Prozesses angefordert.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_RELEASE_ACTIVATION_CONTEXT"></span><span id="error_sxs_release_activation_context"></span>**Fehler \_ SxS \_ - \_ releaseaktivierungs- \_ Kontext**
</dt> <dd> <dl> <dt>

14088 (0x3708)
</dt> <dt>



Eine Kernelmoduskomponente gibt einen Verweis auf einen Aktivierungs kontextfrei.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_SYSTEM_DEFAULT_ACTIVATION_CONTEXT_EMPTY"></span><span id="error_sxs_system_default_activation_context_empty"></span>**Fehler \_ SxS- \_ System \_ Standard \_ Aktivierungs \_ Kontext \_ leer**
</dt> <dd> <dl> <dt>

14089 (0x3709)
</dt> <dt>



Der Aktivierungs Kontext der Standardassembly des Systems konnte nicht generiert werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_INVALID_IDENTITY_ATTRIBUTE_VALUE"></span><span id="error_sxs_invalid_identity_attribute_value"></span>**Fehler \_ SxS \_ ungültiger \_ Identitäts \_ Attribut \_ Wert.**
</dt> <dd> <dl> <dt>

14090 (0x370a)
</dt> <dt>



Der Wert eines Attributs in einer Identität liegt nicht innerhalb des gültigen Bereichs.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_INVALID_IDENTITY_ATTRIBUTE_NAME"></span><span id="error_sxs_invalid_identity_attribute_name"></span>**Fehler \_ SxS \_ ungültiger \_ Identitäts \_ Attribut \_ Name.**
</dt> <dd> <dl> <dt>

14091 (0x370b)
</dt> <dt>



Der Name eines Attributs in einer Identität liegt nicht innerhalb des gültigen Bereichs.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_IDENTITY_DUPLICATE_ATTRIBUTE"></span><span id="error_sxs_identity_duplicate_attribute"></span>**Fehler \_ SxS- \_ Identität \_ dupliziertes \_ Attribut**
</dt> <dd> <dl> <dt>

14092 (0x370c)
</dt> <dt>



Eine Identität enthält zwei Definitionen für dasselbe Attribut.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_IDENTITY_PARSE_ERROR"></span><span id="error_sxs_identity_parse_error"></span>**Fehler beim Analysieren der Fehler \_ SxS- \_ Identität \_ \_**
</dt> <dd> <dl> <dt>

14093 (0x370d)
</dt> <dt>



Die Identitäts Zeichenfolge ist falsch formatiert. Dies kann auf ein nach gestelltes Komma, mehr als zwei unbenannte Attribute, den fehlenden Attributnamen oder den fehlenden Attribut Wert zurückzuführen sein.


</dt> </dl> </dd> <dt>

<span id="ERROR_MALFORMED_SUBSTITUTION_STRING"></span><span id="error_malformed_substitution_string"></span>**fehlerhafte Ersetzungs \_ \_ \_ Zeichenfolge**
</dt> <dd> <dl> <dt>

14094 (0x370e)
</dt> <dt>



Eine Zeichenfolge mit lokalisiertem austauschbaren Inhalt ist falsch formatiert. Auf ein Dollarzeichen ($) wurde etwas anderes als eine linke Klammer oder ein anderes Dollarzeichen gefolgt, oder es wurde keine Rechte Klammer gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_INCORRECT_PUBLIC_KEY_TOKEN"></span><span id="error_sxs_incorrect_public_key_token"></span>**Fehler \_ SxS \_ falsches \_ öffentliches \_ Schlüssel \_ Token.**
</dt> <dd> <dl> <dt>

14095 (0x370f)
</dt> <dt>



Das öffentliche Schlüssel Token entspricht nicht dem angegebenen öffentlichen Schlüssel.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNMAPPED_SUBSTITUTION_STRING"></span><span id="error_unmapped_substitution_string"></span>**nicht zugeordnete Ersetzungs \_ \_ \_ Zeichenfolge**
</dt> <dd> <dl> <dt>

14096 (0x3710)
</dt> <dt>



Eine Ersatz Zeichenfolge hatte keine Zuordnung.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_ASSEMBLY_NOT_LOCKED"></span><span id="error_sxs_assembly_not_locked"></span>**Fehler \_ SxS- \_ Assembly \_ nicht \_ gesperrt**
</dt> <dd> <dl> <dt>

14097 (0x3711))
</dt> <dt>



Die Komponente muss vor dem Ausführen der Anforderung gesperrt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_COMPONENT_STORE_CORRUPT"></span><span id="error_sxs_component_store_corrupt"></span>**Fehler \_ SxS- \_ Komponenten \_ Speicher \_ beschädigt**
</dt> <dd> <dl> <dt>

14098 (0x3712)
</dt> <dt>



Der Komponenten Speicher ist beschädigt.


</dt> </dl> </dd> <dt>

<span id="ERROR_ADVANCED_INSTALLER_FAILED"></span><span id="error_advanced_installer_failed"></span>**Fehler beim \_ Advanced \_ Installer \_**
</dt> <dd> <dl> <dt>

14099 (0x3713)
</dt> <dt>



Ein erweiterter Installer konnte während der Einrichtung oder Wartung nicht ausgeführt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_XML_ENCODING_MISMATCH"></span><span id="error_xml_encoding_mismatch"></span>**Fehler bei der \_ XML- \_ Codierung. \_**
</dt> <dd> <dl> <dt>

14100 (0x3714)
</dt> <dt>



Die Zeichencodierung in der XML-Deklaration entsprach nicht der im Dokument verwendeten Codierung.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_MANIFEST_IDENTITY_SAME_BUT_CONTENTS_DIFFERENT"></span><span id="error_sxs_manifest_identity_same_but_contents_different"></span>**Fehler \_ SxS- \_ Manifest- \_ Identität identisch, \_ \_ aber \_ \_ andere Inhalte**
</dt> <dd> <dl> <dt>

14101 (0x3715)
</dt> <dt>



Die Identitäten der Manifeste sind identisch, aber ihre Inhalte unterscheiden sich.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_IDENTITIES_DIFFERENT"></span><span id="error_sxs_identities_different"></span>**Fehler \_ SxS- \_ Identitäten \_ anders**
</dt> <dd> <dl> <dt>

14102 (0x3716)
</dt> <dt>



Die Komponenten Identitäten unterscheiden sich.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_ASSEMBLY_IS_NOT_A_DEPLOYMENT"></span><span id="error_sxs_assembly_is_not_a_deployment"></span>**Fehler \_ SxS \_ - \_ Assembly \_ ist \_ keine \_ Bereitstellung**
</dt> <dd> <dl> <dt>

14103 (0x3717)
</dt> <dt>



Die Assembly ist keine Bereitstellung.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_FILE_NOT_PART_OF_ASSEMBLY"></span><span id="error_sxs_file_not_part_of_assembly"></span>**Fehler \_ SxS- \_ Datei ist \_ nicht \_ Teil \_ der \_ Assembly.**
</dt> <dd> <dl> <dt>

14104 (0x3718)
</dt> <dt>



Die Datei ist kein Teil der Assembly.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_MANIFEST_TOO_BIG"></span><span id="error_sxs_manifest_too_big"></span>**Fehler \_ SxS- \_ Manifest \_ zu \_ groß**
</dt> <dd> <dl> <dt>

14105 (0x3719)
</dt> <dt>



Die Größe des Manifests überschreitet den zulässigen Höchstwert.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_SETTING_NOT_REGISTERED"></span><span id="error_sxs_setting_not_registered"></span>**Fehler \_ SxS- \_ Einstellung \_ nicht \_ registriert**
</dt> <dd> <dl> <dt>

14106 (0x371a)
</dt> <dt>



Die Einstellung ist nicht registriert.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_TRANSACTION_CLOSURE_INCOMPLETE"></span><span id="error_sxs_transaction_closure_incomplete"></span>**Fehler beim \_ Abschluss der SxS- \_ Transaktion \_ \_ unvollständig.**
</dt> <dd> <dl> <dt>

14107 (0x371b)
</dt> <dt>



Mindestens ein erforderliches Mitglied der Transaktion ist nicht vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_SMI_PRIMITIVE_INSTALLER_FAILED"></span><span id="error_smi_primitive_installer_failed"></span>**Fehler bei \_ SMI- \_ primitiver \_ Installer \_**
</dt> <dd> <dl> <dt>

14108 (0x371c)
</dt> <dt>



Der SMI-primitive Installer ist während des Setups oder der Wartung fehlgeschlagen.


</dt> </dl> </dd> <dt>

<span id="ERROR_GENERIC_COMMAND_FAILED"></span><span id="error_generic_command_failed"></span>**Fehler beim \_ generischen \_ Befehl. \_**
</dt> <dd> <dl> <dt>

14109 (0x371d)
</dt> <dt>



Eine generische Befehlsdatei hat ein Ergebnis zurückgegeben, das einen Fehler angibt.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_FILE_HASH_MISSING"></span><span id="error_sxs_file_hash_missing"></span>**Fehler \_ SxS \_ - \_ Dateihash \_ fehlt.**
</dt> <dd> <dl> <dt>

14110 (0x371e)
</dt> <dt>



In einer Komponente fehlen Informationen zur Dateiüberprüfung im Manifest.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_CHANNEL_PATH"></span><span id="error_evt_invalid_channel_path"></span>**Fehler beim Auftreten eines \_ \_ ungültigen \_ Kanal \_ Pfads.**
</dt> <dd> <dl> <dt>

15000 (0x3a98)
</dt> <dt>



Der angegebene Kanalpfad ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_QUERY"></span><span id="error_evt_invalid_query"></span>**Fehler beim Auftreten einer \_ \_ ungültigen \_ Abfrage**
</dt> <dd> <dl> <dt>

15001 (0x3a99)
</dt> <dt>



Die angegebene Abfrage ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_PUBLISHER_METADATA_NOT_FOUND"></span><span id="error_evt_publisher_metadata_not_found"></span>**Fehler beim Auftreten von \_ \_ Verleger \_ Metadaten \_ nicht \_ gefunden.**
</dt> <dd> <dl> <dt>

15002 (0x3a9a)
</dt> <dt>



Die Verleger Metadaten wurden in der Ressource nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_EVENT_TEMPLATE_NOT_FOUND"></span><span id="error_evt_event_template_not_found"></span>**Fehler \_ Ereignis Vorlage "Fehler Ereignis" wurde \_ \_ \_ nicht \_ gefunden.**
</dt> <dd> <dl> <dt>

15003 (0x3a9b)
</dt> <dt>



Die Vorlage für eine Ereignis Definition wurde in der Ressource nicht gefunden (Fehler = %1).


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_PUBLISHER_NAME"></span><span id="error_evt_invalid_publisher_name"></span>**\_ \_ ungültiger \_ Herausgeber \_ Name**
</dt> <dd> <dl> <dt>

15004 (0x3a9c)
</dt> <dt>



Der angegebene Herausgeber Name ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_EVENT_DATA"></span><span id="error_evt_invalid_event_data"></span>**Fehler beim Auftreten von \_ \_ ungültigen \_ Ereignis \_ Daten.**
</dt> <dd> <dl> <dt>

15005 (0x3a9d)
</dt> <dt>



Die Ereignisdaten, die vom Verleger ausgelöst werden, sind nicht mit der Definition der Ereignis Vorlage im Manifest des Verlegers kompatibel.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_CHANNEL_NOT_FOUND"></span><span id="error_evt_channel_not_found"></span>**Fehler beim \_ EVT- \_ Kanal \_ nicht \_ gefunden.**
</dt> <dd> <dl> <dt>

15007 (0x3a9f)
</dt> <dt>



Der angegebene Kanal konnte nicht gefunden werden. Überprüfen Sie die Kanal Konfiguration.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_MALFORMED_XML_TEXT"></span><span id="error_evt_malformed_xml_text"></span>**fehlerhafter \_ \_ XML- \_ \_ Text Fehler.**
</dt> <dd> <dl> <dt>

15008 (0x3aa0)
</dt> <dt>



Der angegebene XML-Text war nicht wohl geformt. Weitere Informationen finden Sie unter Erweiterter Fehler.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_SUBSCRIPTION_TO_DIRECT_CHANNEL"></span><span id="error_evt_subscription_to_direct_channel"></span>**Fehler " \_ evt"- \_ Abonnement \_ für \_ direkten \_ Kanal**
</dt> <dd> <dl> <dt>

15009 (0x3aa1)
</dt> <dt>



Der Aufrufer versucht, einen direkten Kanal zu abonnieren, der nicht zulässig ist. Die Ereignisse für einen direkten Kanal gelangen direkt in eine Protokolldatei und können nicht abonniert werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_CONFIGURATION_ERROR"></span><span id="error_evt_configuration_error"></span>**Fehler bei \_ EVT- \_ Konfigurations \_ Fehler**
</dt> <dd> <dl> <dt>

15010 (0x3aa2)
</dt> <dt>



Konfigurationsfehler.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_QUERY_RESULT_STALE"></span><span id="error_evt_query_result_stale"></span>**Fehler beim auslassen der \_ \_ Abfrage \_ Ergebnisse \_**
</dt> <dd> <dl> <dt>

15011 (0x3aa3)
</dt> <dt>



Das Abfrageergebnis ist veraltet/ungültig. Dies kann darauf zurückzuführen sein, dass das Protokoll gelöscht oder ein Rollback ausgeführt wird, nachdem das Abfrageergebnis erstellt wurde. Benutzer sollten diesen Code behandeln, indem Sie das Abfrageergebnis Objekt freigeben und die Abfrage erneut ausstellen.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_QUERY_RESULT_INVALID_POSITION"></span><span id="error_evt_query_result_invalid_position"></span>**Fehler bei der \_ \_ Abfrage \_ Ergebnis \_ ungültige \_ Position**
</dt> <dd> <dl> <dt>

15012 (0x3aa4)
</dt> <dt>



Das Abfrageergebnis ist zurzeit an einer ungültigen Position.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_NON_VALIDATING_MSXML"></span><span id="error_evt_non_validating_msxml"></span>**Fehler beim \_ \_ nicht \_ Validieren von \_ MSXML.**
</dt> <dd> <dl> <dt>

15013 (0x3aa5)
</dt> <dt>



Registrierte MSXML unterstützt keine Validierung.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_ALREADYSCOPED"></span><span id="error_evt_filter_alreadyscoped"></span>**Fehler beim Filtern von " \_ \_ \_ alread-scoped".**
</dt> <dd> <dl> <dt>

15014 (0x3aa6)
</dt> <dt>



Auf einen Ausdruck kann nur eine Änderung des Bereichs Vorgangs folgen, wenn er selbst zu einer Knotengruppe ausgewertet wird und nicht bereits Teil einer anderen Änderung des Bereichs Vorgangs ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_NOTELTSET"></span><span id="error_evt_filter_noteltset"></span>**Fehler beim \_ \_ Filtern von \_ noteltset.**
</dt> <dd> <dl> <dt>

15015 (0x3aa7)
</dt> <dt>



Ein Schritt Vorgang kann nicht von einem Begriff durchgeführt werden, der keinen Element Satz darstellt.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_INVARG"></span><span id="error_evt_filter_invarg"></span>**Fehler " \_ EVT Filter"- \_ Filter \_**
</dt> <dd> <dl> <dt>

15016 (0x3aa8)
</dt> <dt>



Linke Seiten Argumente für binäre Operatoren müssen entweder Attribute, Knoten oder Variablen sein, und Rechte Argumente müssen Konstanten sein.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_INVTEST"></span><span id="error_evt_filter_invtest"></span>**Fehler beim \_ \_ Filter zum Filtern \_ .**
</dt> <dd> <dl> <dt>

15017 (0x3aa9)
</dt> <dt>



Ein Schritt Vorgang muss entweder einen Knoten Test oder, im Falle eines Prädikats, einen algebraischen Ausdruck einschließen, mit dem jeder Knoten in der Knotengruppe, der durch den vorangehenden Knoten Satz identifiziert wird, getestet werden kann.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_INVTYPE"></span><span id="error_evt_filter_invtype"></span>**\_ \_ Fehlertyp \_ Filtertyp Filtern**
</dt> <dd> <dl> <dt>

15018 (0x3aaa)
</dt> <dt>



Dieser Datentyp wird derzeit nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_PARSEERR"></span><span id="error_evt_filter_parseerr"></span>**Fehler beim \_ \_ Filtern der \_ parameterr**
</dt> <dd> <dl> <dt>

15019 (0x3aab)
</dt> <dt>



Syntax Fehler an Position %1! d!.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_UNSUPPORTEDOP"></span><span id="error_evt_filter_unsupportedop"></span>**Fehler beim Filtern von " \_ \_ \_ unsupportedop".**
</dt> <dd> <dl> <dt>

15020 (0x3aac)
</dt> <dt>



Dieser Operator wird von dieser Implementierung des Filters nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_UNEXPECTEDTOKEN"></span><span id="error_evt_filter_unexpectedtoken"></span>**Fehler beim Filtern von " \_ \_ \_ unexpectedtoken".**
</dt> <dd> <dl> <dt>

15021 (0x3aad)
</dt> <dt>



Unerwartetes Token.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_OPERATION_OVER_ENABLED_DIRECT_CHANNEL"></span><span id="error_evt_invalid_operation_over_enabled_direct_channel"></span>**Fehler durch \_ \_ ungültigen \_ Vorgang \_ über \_ aktiviertem \_ direkt \_ Kanal**
</dt> <dd> <dl> <dt>

15022 (0x3aae)
</dt> <dt>



Der angeforderte Vorgang kann nicht über einen aktivierten direkten Kanal ausgeführt werden. Der Kanal muss zuerst deaktiviert werden, bevor der angeforderte Vorgang durchgeführt wird.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_CHANNEL_PROPERTY_VALUE"></span><span id="error_evt_invalid_channel_property_value"></span>**Error \_ EVT \_ ungültiger \_ \_ channeleigenschafts \_ Wert.**
</dt> <dd> <dl> <dt>

15023 (0x3aaf)
</dt> <dt>



Kanal Eigenschaft %1! s! enthält einen ungültigen Wert. Der Wert weist einen ungültigen Typ auf, liegt außerhalb des gültigen Bereichs, kann nicht aktualisiert werden oder wird von diesem Kanaltyp nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_PUBLISHER_PROPERTY_VALUE"></span><span id="error_evt_invalid_publisher_property_value"></span>**Error \_ EVT \_ ungültiger \_ Verleger \_ Eigenschafts \_ Wert.**
</dt> <dd> <dl> <dt>

15024 (0x3ab0)
</dt> <dt>



Verleger Eigenschaft %1! s! enthält einen ungültigen Wert. Der Wert weist einen ungültigen Typ auf, liegt außerhalb des gültigen Bereichs, kann nicht aktualisiert werden oder wird von diesem Typ von Verleger nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_CHANNEL_CANNOT_ACTIVATE"></span><span id="error_evt_channel_cannot_activate"></span>**\_fehlerevt- \_ Kanal \_ kann nicht \_ aktiviert werden.**
</dt> <dd> <dl> <dt>

15025 (0x3ab1)
</dt> <dt>



Der Kanal kann nicht aktiviert werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_TOO_COMPLEX"></span><span id="error_evt_filter_too_complex"></span>**Fehler beim \_ \_ Filter \_ zu \_ Komplex.**
</dt> <dd> <dl> <dt>

15026 (0x3ab2)
</dt> <dt>



Der XPath-Ausdruck hat unterstützte Komplexität überschritten. Fügen Sie Sie ein, oder Teilen Sie Sie in zwei oder mehr einfache Ausdrücke auf.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_MESSAGE_NOT_FOUND"></span><span id="error_evt_message_not_found"></span>**Fehler \_ Meldung "evt" wurde \_ \_ nicht \_ gefunden.**
</dt> <dd> <dl> <dt>

15027 (0x3ab3)
</dt> <dt>



die Nachrichten Ressource ist vorhanden, aber die Nachricht wurde nicht in der Zeichenfolge/Nachrichten Tabelle gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_MESSAGE_ID_NOT_FOUND"></span><span id="error_evt_message_id_not_found"></span>**Fehler- \_ EVT-nach \_ richten- \_ ID \_ nicht \_ gefunden.**
</dt> <dd> <dl> <dt>

15028 (0x3ab4)
</dt> <dt>



Die Nachrichten-ID für die gewünschte Nachricht wurde nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_UNRESOLVED_VALUE_INSERT"></span><span id="error_evt_unresolved_value_insert"></span>**Fehler beim Einfügen von nicht aufgelösten \_ \_ \_ Werten. \_**
</dt> <dd> <dl> <dt>

15029 (0x3ab5)
</dt> <dt>



Die Ersetzungs Zeichenfolge für den Einfügeindex (%1) wurde nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_UNRESOLVED_PARAMETER_INSERT"></span><span id="error_evt_unresolved_parameter_insert"></span>**Fehler beim \_ Einfügen nicht \_ aufgelöster \_ Parameter \_ .**
</dt> <dd> <dl> <dt>

15030 (0x3ab6)
</dt> <dt>



Die Beschreibungs Zeichenfolge für den Parameter Verweis (%1) wurde nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_MAX_INSERTS_REACHED"></span><span id="error_evt_max_inserts_reached"></span>**\_Maximale Anzahl von \_ \_ Einfügungen des \_ Fehlers**
</dt> <dd> <dl> <dt>

15031 (0x3ab7)
</dt> <dt>



Die maximal zulässige Anzahl von Ersetzungen wurde erreicht.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_EVENT_DEFINITION_NOT_FOUND"></span><span id="error_evt_event_definition_not_found"></span>**Fehler \_ Ereignis- \_ Ereignis \_ Definition \_ nicht \_ gefunden.**
</dt> <dd> <dl> <dt>

15032 (0x3ab8)
</dt> <dt>



Die Ereignis Definition für die Ereignis-ID (%1) wurde nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_MESSAGE_LOCALE_NOT_FOUND"></span><span id="error_evt_message_locale_not_found"></span>**Fehler beim \_ EVT-Nachrichten Gebiets Schema \_ \_ \_ nicht \_ gefunden.**
</dt> <dd> <dl> <dt>

15033 (0x3ab9)
</dt> <dt>



Die Gebiets Schema spezifische Ressource für die gewünschte Nachricht ist nicht vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_VERSION_TOO_OLD"></span><span id="error_evt_version_too_old"></span>**Fehler- \_ EVT- \_ Version \_ zu \_ alt**
</dt> <dd> <dl> <dt>

15034 (0x3aba)
</dt> <dt>



Die Ressource ist zu alt, um kompatibel zu sein.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_VERSION_TOO_NEW"></span><span id="error_evt_version_too_new"></span>**Fehler- \_ EVT- \_ Version \_ zu \_ neu**
</dt> <dd> <dl> <dt>

15035 (0x3abb)
</dt> <dt>



Die Ressource ist zu neu, um kompatibel zu sein.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_CANNOT_OPEN_CHANNEL_OF_QUERY"></span><span id="error_evt_cannot_open_channel_of_query"></span>**Fehler \_ EVT \_ kann \_ den \_ Kanal \_ der \_ Abfrage nicht öffnen.**
</dt> <dd> <dl> <dt>

15036 (0x3abc)
</dt> <dt>



Der Kanal bei Index %1! d! der Abfrage kann nicht geöffnet werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_PUBLISHER_DISABLED"></span><span id="error_evt_publisher_disabled"></span>**Fehler beim \_ Deaktivieren des \_ Verlegers \_**
</dt> <dd> <dl> <dt>

15037 (0x3abd)
</dt> <dt>



Der Verleger wurde deaktiviert, und die zugehörige Ressource ist nicht verfügbar. Dies tritt normalerweise auf, wenn der Verleger gerade deinstalliert oder aktualisiert wird.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_OUT_OF_RANGE"></span><span id="error_evt_filter_out_of_range"></span>**Fehler beim \_ \_ Filtern \_ \_ im \_ Bereich.**
</dt> <dd> <dl> <dt>

15038 (0x3abe)
</dt> <dt>



Es wurde versucht, einen numerischen Typ zu erstellen, der außerhalb des gültigen Bereichs liegt.


</dt> </dl> </dd> <dt>

<span id="ERROR_EC_SUBSCRIPTION_CANNOT_ACTIVATE"></span><span id="error_ec_subscription_cannot_activate"></span>**Fehler beim Aktivieren des \_ EC- \_ Abonnements \_ \_**
</dt> <dd> <dl> <dt>

15080 (0x3ae8)
</dt> <dt>



Das Abonnement kann nicht aktiviert werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_EC_LOG_DISABLED"></span><span id="error_ec_log_disabled"></span>**Fehler- \_ EC- \_ Protokoll \_ deaktiviert**
</dt> <dd> <dl> <dt>

15081 (0x3ae9)
</dt> <dt>



Das Protokoll des Abonnements befindet sich im deaktivierten Zustand und kann nicht zum Weiterleiten von Ereignissen an verwendet werden. Das Protokoll muss zuerst aktiviert werden, bevor das Abonnement aktiviert werden kann.


</dt> </dl> </dd> <dt>

<span id="ERROR_EC_CIRCULAR_FORWARDING"></span><span id="error_ec_circular_forwarding"></span>**Fehler bei \_ EC- \_ Kreis \_ Weiterleitung**
</dt> <dd> <dl> <dt>

15082 (0x3aea)
</dt> <dt>



Beim Weiterleiten von Ereignissen vom lokalen Computer an sich selbst kann die Abfrage des Abonnements kein Ziel Protokoll des Abonnements enthalten.


</dt> </dl> </dd> <dt>

<span id="ERROR_EC_CREDSTORE_FULL"></span><span id="error_ec_credstore_full"></span>**Fehler beim Aufrufen von " \_ EC- \_ Speicher" \_**
</dt> <dd> <dl> <dt>

15083 (0x3aeb)
</dt> <dt>



Der Anmelde Informationsspeicher, der zum Speichern der Anmelde Informationen verwendet wird, ist voll.


</dt> </dl> </dd> <dt>

<span id="ERROR_EC_CRED_NOT_FOUND"></span><span id="error_ec_cred_not_found"></span>**Fehler beim Aufrufen der "EC"-Funktion. \_ \_ \_ \_**
</dt> <dd> <dl> <dt>

15084 (0x3aec)
</dt> <dt>



Die von diesem Abonnement verwendeten Anmelde Informationen können im Anmelde Informationsspeicher nicht gefunden werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_EC_NO_ACTIVE_CHANNEL"></span><span id="error_ec_no_active_channel"></span>**Fehler- \_ EC \_ ohne \_ aktiven \_ Kanal**
</dt> <dd> <dl> <dt>

15085 (0x3aed)
</dt> <dt>



Es wurde kein aktiver Kanal für die Abfrage gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_MUI_FILE_NOT_FOUND"></span><span id="error_mui_file_not_found"></span>**Fehler- \_ MUI- \_ Datei wurde \_ nicht \_ gefunden.**
</dt> <dd> <dl> <dt>

15100 (0x3afc)
</dt> <dt>



Der Ressourcen Lader konnte die MUI-Datei nicht finden.


</dt> </dl> </dd> <dt>

<span id="ERROR_MUI_INVALID_FILE"></span><span id="error_mui_invalid_file"></span>**\_ungültige fehlermui- \_ \_ Datei**
</dt> <dd> <dl> <dt>

15101 (0x3afd)
</dt> <dt>



Fehler beim Laden der MUI-Datei durch das Ressourcen Lade Modul, weil die Überprüfung der Datei fehlgeschlagen ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_MUI_INVALID_RC_CONFIG"></span><span id="error_mui_invalid_rc_config"></span>**Fehler- \_ MUI \_ ungültige \_ RC- \_ Konfiguration.**
</dt> <dd> <dl> <dt>

15102 (0x3afe)
</dt> <dt>



Das RC-Manifest ist mit Garbage Data oder nicht unterstützter Version beschädigt, oder das erforderliche Element ist nicht vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_MUI_INVALID_LOCALE_NAME"></span><span id="error_mui_invalid_locale_name"></span>**\_ \_ Ungültiger Name für \_ Fehler-MUI \_**
</dt> <dd> <dl> <dt>

15103 (0x3aff)
</dt> <dt>



Das RC-Manifest hat einen ungültigen Kultur Namen.


</dt> </dl> </dd> <dt>

<span id="ERROR_MUI_INVALID_ULTIMATEFALLBACK_NAME"></span><span id="error_mui_invalid_ultimatefallback_name"></span>**Fehler \_ MUI \_ ungültiger \_ ultimatefallbackname. \_**
</dt> <dd> <dl> <dt>

15104 (0x3b00)
</dt> <dt>



Das RC-Manifest weist einen ungültigen ultimatefallback-Namen auf.


</dt> </dl> </dd> <dt>

<span id="ERROR_MUI_FILE_NOT_LOADED"></span><span id="error_mui_file_not_loaded"></span>**die \_ fehlermui- \_ Datei wurde \_ nicht \_ geladen.**
</dt> <dd> <dl> <dt>

15105 (0x3b01)
</dt> <dt>



Der Ressourcen Lade Cache hat keinen geladenen MUI-Eintrag.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_ENUM_USER_STOP"></span><span id="error_resource_enum_user_stop"></span>**Fehler \_ Ressourcen- \_ Enum- \_ Benutzer \_ Beendigung**
</dt> <dd> <dl> <dt>

15106 (0x3b02)
</dt> <dt>



Die Ressourcen Aufzählung wurde vom Benutzer beendet.


</dt> </dl> </dd> <dt>

<span id="ERROR_MUI_INTLSETTINGS_UILANG_NOT_INSTALLED"></span><span id="error_mui_intlsettings_uilang_not_installed"></span>**Fehler \_ MUI \_ intlsettings \_ uilang \_ nicht \_ installiert**
</dt> <dd> <dl> <dt>

15107 (0x3b03)
</dt> <dt>



Fehler beim Installieren der Benutzeroberflächen Sprache.


</dt> </dl> </dd> <dt>

<span id="ERROR_MUI_INTLSETTINGS_INVALID_LOCALE_NAME"></span><span id="error_mui_intlsettings_invalid_locale_name"></span>**Error \_ MUI \_ intlsettings \_ Ungültiger Gebiets Schema \_ \_ Name**
</dt> <dd> <dl> <dt>

15108 (0x3b04)
</dt> <dt>



Fehler bei der Gebiets Schema Installation.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_RUNTIME_NO_DEFAULT_OR_NEUTRAL_RESOURCE"></span><span id="error_mrm_runtime_no_default_or_neutral_resource"></span>**Fehler \_ MRM \_ Runtime \_ keine \_ standardmäßige \_ oder \_ neutrale \_ Ressource**
</dt> <dd> <dl> <dt>

15110 (0x3b06)
</dt> <dt>



Eine Ressource weist keinen standardmäßigen oder neutralen Wert auf.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_INVALID_PRICONFIG"></span><span id="error_mrm_invalid_priconfig"></span>**Fehler \_ MRM \_ ungültige \_ priconfig.**
</dt> <dd> <dl> <dt>

15111 (0x3b07)
</dt> <dt>



Ungültige PRI-Konfigurationsdatei.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_INVALID_FILE_TYPE"></span><span id="error_mrm_invalid_file_type"></span>**Fehler bei \_ MRM \_ ungültiger \_ \_ Dateityp.**
</dt> <dd> <dl> <dt>

15112 (0x3b08)
</dt> <dt>



Ungültiger Dateityp.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_UNKNOWN_QUALIFIER"></span><span id="error_mrm_unknown_qualifier"></span>**Fehler \_ MRM \_ unbekannter \_ Qualifizierer**
</dt> <dd> <dl> <dt>

15113 (0x3b09)
</dt> <dt>



Unbekannter Qualifizierer.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_INVALID_QUALIFIER_VALUE"></span><span id="error_mrm_invalid_qualifier_value"></span>**Fehler bei \_ MRM \_ ungültiger \_ qualifiziererwert \_**
</dt> <dd> <dl> <dt>

15114 (0x3b0a)
</dt> <dt>



Ungültiger qualifiziererwert.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_NO_CANDIDATE"></span><span id="error_mrm_no_candidate"></span>**Fehler \_ MRM \_ Nein \_ Candidate**
</dt> <dd> <dl> <dt>

15115 (0x3b0b)
</dt> <dt>



Es wurde kein Kandidat gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_NO_MATCH_OR_DEFAULT_CANDIDATE"></span><span id="error_mrm_no_match_or_default_candidate"></span>**Fehler \_ MRM \_ keine Entsprechung \_ \_ oder \_ Standard \_ Kandidat**
</dt> <dd> <dl> <dt>

15116 (0x3b0c)
</dt> <dt>



ResourceMap oder namedresource verfügt über ein Element, das nicht über eine Standard-oder neutrale Ressource verfügt.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_RESOURCE_TYPE_MISMATCH"></span><span id="error_mrm_resource_type_mismatch"></span>**Fehler bei der \_ MRM- \_ Ressourcen \_ Typen \_ Konflikt**
</dt> <dd> <dl> <dt>

15117 (0x3b0d)
</dt> <dt>



Ungültiger resourcecandidate-Typ.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_DUPLICATE_MAP_NAME"></span><span id="error_mrm_duplicate_map_name"></span>**Fehler \_ MRM \_ doppelter Zuordnungs \_ \_ Name.**
</dt> <dd> <dl> <dt>

15118 (0x3b0e)
</dt> <dt>



Doppelte Ressourcen Zuordnung.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_DUPLICATE_ENTRY"></span><span id="error_mrm_duplicate_entry"></span>**Fehler beim \_ \_ doppelten \_ Eintrag von MRM.**
</dt> <dd> <dl> <dt>

15119 (0x3b0f)
</dt> <dt>



Doppelter Eintrag.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_INVALID_RESOURCE_IDENTIFIER"></span><span id="error_mrm_invalid_resource_identifier"></span>**Fehler bei \_ MRM, \_ ungültiger \_ Ressourcen \_ Bezeichner**
</dt> <dd> <dl> <dt>

15120 (0x3b10)
</dt> <dt>



Ungültiger Ressourcen Bezeichner.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_FILEPATH_TOO_LONG"></span><span id="error_mrm_filepath_too_long"></span>**Fehler beim \_ MRM- \_ Dateipfad \_ zu \_ lang.**
</dt> <dd> <dl> <dt>

15121 (0x3b11)
</dt> <dt>



Der Dateipfad ist zu lang.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_UNSUPPORTED_DIRECTORY_TYPE"></span><span id="error_mrm_unsupported_directory_type"></span>**Fehler \_ MRM \_ nicht unterstützter \_ \_ Verzeichnistyp**
</dt> <dd> <dl> <dt>

15122 (0x3b12)
</dt> <dt>



Nicht unterstützter Verzeichnistyp.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_INVALID_PRI_FILE"></span><span id="error_mrm_invalid_pri_file"></span>**Fehler bei \_ MRM, \_ ungültige \_ pri- \_ Datei**
</dt> <dd> <dl> <dt>

15126 (0x3b16)
</dt> <dt>



Ungültige PRI-Datei.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_NAMED_RESOURCE_NOT_FOUND"></span><span id="error_mrm_named_resource_not_found"></span>**Fehler \_ MRM \_ benannte \_ Ressource \_ nicht \_ gefunden**
</dt> <dd> <dl> <dt>

15127 (0x3b17)
</dt> <dt>



"Namedresource" wurde nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_MAP_NOT_FOUND"></span><span id="error_mrm_map_not_found"></span>**Fehler \_ MRM-Zuordnung wurde \_ \_ nicht \_ gefunden.**
</dt> <dd> <dl> <dt>

15135 (0x3b1f)
</dt> <dt>



ResourceMap nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_UNSUPPORTED_PROFILE_TYPE"></span><span id="error_mrm_unsupported_profile_type"></span>**Fehler \_ MRM \_ nicht unterstützter \_ \_ Profiltyp**
</dt> <dd> <dl> <dt>

15136 (0x3b20)
</dt> <dt>



Nicht unterstützter MRT-Profiltyp.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_INVALID_QUALIFIER_OPERATOR"></span><span id="error_mrm_invalid_qualifier_operator"></span>**Fehler bei \_ MRM \_ ungültiger \_ qualifiziereroperator \_**
</dt> <dd> <dl> <dt>

15137 (0x3b21)
</dt> <dt>



Ungültiger qualifiziereroperator.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_INDETERMINATE_QUALIFIER_VALUE"></span><span id="error_mrm_indeterminate_qualifier_value"></span>**Fehler beim \_ unbestimmten Wert von MRM- \_ \_ Qualifizierer \_**
</dt> <dd> <dl> <dt>

15138 (0x3b22)
</dt> <dt>



Der qualifiziererwert oder der qualifiziererwert konnte nicht festgelegt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_AUTOMERGE_ENABLED"></span><span id="error_mrm_automerge_enabled"></span>**Fehler beim \_ Aktivieren von MRM \_ AutoMerge. \_**
</dt> <dd> <dl> <dt>

15139 (0x3b23)
</dt> <dt>



AutoMerge ist in der PRI-Datei aktiviert.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_TOO_MANY_RESOURCES"></span><span id="error_mrm_too_many_resources"></span>**Fehler \_ MRM \_ zu \_ viele \_ Ressourcen**
</dt> <dd> <dl> <dt>

15140 (0x3b24)
</dt> <dt>



Es wurden zu viele Ressourcen für das Paket definiert.


</dt> </dl> </dd> <dt>

<span id="ERROR_MCA_INVALID_CAPABILITIES_STRING"></span><span id="error_mca_invalid_capabilities_string"></span>**Fehler bei \_ MCA \_ ungültige Funktions \_ \_ Zeichenfolge**
</dt> <dd> <dl> <dt>

15200 (0x3b60)
</dt> <dt>



Der Monitor hat eine DDC/CI-Funktions Zeichenfolge zurückgegeben, die nicht der Spezifikation "Access. Bus 3,0", "DDC/CI 1,1" oder "MCCS 2 Revision 1" entsprach.


</dt> </dl> </dd> <dt>

<span id="ERROR_MCA_INVALID_VCP_VERSION"></span><span id="error_mca_invalid_vcp_version"></span>**Fehler bei \_ MCA, \_ ungültige \_ VCP- \_ Version.**
</dt> <dd> <dl> <dt>

15201 (0x3b61)
</dt> <dt>



Der VCP-Code der VCP-Version (0xDF) des Monitors hat einen ungültigen Versions Wert zurückgegeben.


</dt> </dl> </dd> <dt>

<span id="ERROR_MCA_MONITOR_VIOLATES_MCCS_SPECIFICATION"></span><span id="error_mca_monitor_violates_mccs_specification"></span>**Fehler \_ MCA- \_ Monitor \_ verstößt gegen \_ MCCS- \_ Spezifikation**
</dt> <dd> <dl> <dt>

15202 (0x3b62)
</dt> <dt>



Der Monitor entspricht nicht der MCCS-Spezifikation, die er vorgibt, Sie zu unterstützen.


</dt> </dl> </dd> <dt>

<span id="ERROR_MCA_MCCS_VERSION_MISMATCH"></span><span id="error_mca_mccs_version_mismatch"></span>**Fehler bei \_ MCA- \_ MCCS- \_ Versions \_ Konflikt**
</dt> <dd> <dl> <dt>

15203 (0x3b63)
</dt> <dt>



Die MCCS-Version in der MCCS ver-Funktion eines Monitors \_ entspricht nicht der MCCS-Version, die der Monitor meldet, wenn der VCP-Code (0xDF) verwendet wird.


</dt> </dl> </dd> <dt>

<span id="ERROR_MCA_UNSUPPORTED_MCCS_VERSION"></span><span id="error_mca_unsupported_mccs_version"></span>**Fehler \_ MCA, \_ nicht unterstützte \_ MCCS- \_ Version**
</dt> <dd> <dl> <dt>

15204 (0x3b64)
</dt> <dt>



Die Monitor Konfigurations-API funktioniert nur mit Monitoren, die die MCCs 1,0 Specification, MCCS 2,0 Specification oder die MCCS 2,0 Revision 1-Spezifikation unterstützen.


</dt> </dl> </dd> <dt>

<span id="ERROR_MCA_INTERNAL_ERROR"></span><span id="error_mca_internal_error"></span>**Fehler bei \_ MCA- \_ interner \_ Fehler**
</dt> <dd> <dl> <dt>

15205 (0x3b65)
</dt> <dt>



Interner Fehler bei der Monitor Konfigurations-API.


</dt> </dl> </dd> <dt>

<span id="ERROR_MCA_INVALID_TECHNOLOGY_TYPE_RETURNED"></span><span id="error_mca_invalid_technology_type_returned"></span>**Fehler bei \_ MCA- \_ ungültigem \_ \_ technologientyp \_ zurückgegeben**
</dt> <dd> <dl> <dt>

15206 (0x3b66)
</dt> <dt>



Der Monitor hat einen ungültigen Monitor-Technologietyp zurückgegeben. CRT, Plasma und LCD (TFT) sind Beispiele für Überwachungstechnologie Typen. Dieser Fehler impliziert, dass der Monitor die MCCS 2,0-oder MCCS 2,0 Revision 1-Spezifikation verletzt hat.


</dt> </dl> </dd> <dt>

<span id="ERROR_MCA_UNSUPPORTED_COLOR_TEMPERATURE"></span><span id="error_mca_unsupported_color_temperature"></span>**Fehler bei \_ MCA \_ nicht unterstützte \_ Farb \_ Temperatur**
</dt> <dd> <dl> <dt>

15207 (0x3b67)
</dt> <dt>



Der Aufrufer von [**setmonitorcolortemperatur**](/windows/win32/api/highlevelmonitorconfigurationapi/nf-highlevelmonitorconfigurationapi-setmonitorcolortemperature) hat eine Farbtemperatur angegeben, die vom aktuellen Monitor nicht unterstützt wurde. Dieser Fehler impliziert, dass der Monitor die MCCS 2,0-oder MCCS 2,0 Revision 1-Spezifikation verletzt hat.


</dt> </dl> </dd> <dt>

<span id="ERROR_AMBIGUOUS_SYSTEM_DEVICE"></span><span id="error_ambiguous_system_device"></span>**Fehler \_ mehrdeutiges \_ System \_ Gerät**
</dt> <dd> <dl> <dt>

15250 (0x3b92)
</dt> <dt>



Das angeforderte System Gerät kann nicht identifiziert werden, weil mehrere indizierbare Geräte möglicherweise den Identifikations Kriterien entsprechen.


</dt> </dl> </dd> <dt>

<span id="ERROR_SYSTEM_DEVICE_NOT_FOUND"></span><span id="error_system_device_not_found"></span>**Fehler \_ System \_ Gerät \_ nicht \_ gefunden.**
</dt> <dd> <dl> <dt>

15299 (0x3bc3)
</dt> <dt>



Das angeforderte System Gerät wurde nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_HASH_NOT_SUPPORTED"></span><span id="error_hash_not_supported"></span>**Fehler \_ Hash \_ \_ wird nicht unterstützt.**
</dt> <dd> <dl> <dt>

15300 (0x3bc4)
</dt> <dt>



Die Hash Generierung für die angegebene Hash Version und den Hashtyp ist auf dem Server nicht aktiviert.


</dt> </dl> </dd> <dt>

<span id="ERROR_HASH_NOT_PRESENT"></span><span id="error_hash_not_present"></span>**Fehler \_ Hash \_ nicht \_ vorhanden**
</dt> <dd> <dl> <dt>

15301 (0x3bc5)
</dt> <dt>



Der vom Server angeforderte Hash ist nicht verfügbar oder nicht mehr gültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_SECONDARY_IC_PROVIDER_NOT_REGISTERED"></span><span id="error_secondary_ic_provider_not_registered"></span>**Fehler \_ beim sekundären \_ IC- \_ Anbieter \_ nicht \_ registriert**
</dt> <dd> <dl> <dt>

15321 (0x3bd9)
</dt> <dt>



Die sekundäre interruptcontrollerinstanz, die den angegebenen Interrupt verwaltet, ist nicht registriert.


</dt> </dl> </dd> <dt>

<span id="ERROR_GPIO_CLIENT_INFORMATION_INVALID"></span><span id="error_gpio_client_information_invalid"></span>**Fehler bei \_ GPIO- \_ Client \_ Informationen \_ ungültig.**
</dt> <dd> <dl> <dt>

15322 (0x3bda)
</dt> <dt>



Die vom GPIO-Client Treiber bereitgestellten Informationen sind ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_GPIO_VERSION_NOT_SUPPORTED"></span><span id="error_gpio_version_not_supported"></span>**Fehler- \_ GPIO- \_ Version \_ \_ wird nicht unterstützt**
</dt> <dd> <dl> <dt>

15323 (0x3bdb)
</dt> <dt>



Die vom GPIO-Client Treiber angegebene Version wird nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="ERROR_GPIO_INVALID_REGISTRATION_PACKET"></span><span id="error_gpio_invalid_registration_packet"></span>**Fehler beim \_ GPIO- \_ \_ Registrierungs \_ Paket.**
</dt> <dd> <dl> <dt>

15324 (0x3bdc)
</dt> <dt>



Das vom GPIO-Client Treiber bereitgestellte Registrierungspaket ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_GPIO_OPERATION_DENIED"></span><span id="error_gpio_operation_denied"></span>**Fehler beim \_ GPIO- \_ Vorgang. \_**
</dt> <dd> <dl> <dt>

15325 (0x3bdd)
</dt> <dt>



Der angeforderte Vorgang wird für das angegebene Handle nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="ERROR_GPIO_INCOMPATIBLE_CONNECT_MODE"></span><span id="error_gpio_incompatible_connect_mode"></span>**Fehler beim \_ GPIO- \_ inkompatiblen \_ Verbindungs \_ Modus.**
</dt> <dd> <dl> <dt>

15326 (0x3bde)
</dt> <dt>



Der angeforderte Verbindungs Modus steht in Konflikt mit einem vorhandenen Modus auf einem oder mehreren der angegebenen Pins.


</dt> </dl> </dd> <dt>

<span id="ERROR_GPIO_INTERRUPT_ALREADY_UNMASKED"></span><span id="error_gpio_interrupt_already_unmasked"></span>**Fehler beim \_ GPIO- \_ Interrupt ist \_ bereits \_ aufgehoben.**
</dt> <dd> <dl> <dt>

15327 (0x3bdf)
</dt> <dt>



Der für die Maskierung angeforderte Interrupt ist nicht maskiert.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_SWITCH_RUNLEVEL"></span><span id="error_cannot_switch_runlevel"></span>**Fehler \_ beim \_ Umschalten von \_ Runlevel.**
</dt> <dd> <dl> <dt>

15400 (0x3c28)
</dt> <dt>



Der angeforderte Schalter auf Lauf Ebene kann nicht erfolgreich abgeschlossen werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_RUNLEVEL_SETTING"></span><span id="error_invalid_runlevel_setting"></span>**Fehler \_ ungültige \_ Runlevel- \_ Einstellung.**
</dt> <dd> <dl> <dt>

15401 (0x3c29)
</dt> <dt>



Der Dienst hat eine ungültige Einstellung für die Lauf Ebene. Die Lauf Ebene für einen Dienst darf nicht höher sein als die Lauf Ebene der abhängigen Dienste.


</dt> </dl> </dd> <dt>

<span id="ERROR_RUNLEVEL_SWITCH_TIMEOUT"></span><span id="error_runlevel_switch_timeout"></span>**Timeout für Fehler bei \_ Runlevel- \_ Switch \_**
</dt> <dd> <dl> <dt>

15402 (0x3c2a)
</dt> <dt>



Der angeforderte Schalter auf Lauf Ebene kann nicht erfolgreich abgeschlossen werden, da ein oder mehrere Dienste innerhalb des angegebenen Timeouts nicht beendet oder neu gestartet werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_RUNLEVEL_SWITCH_AGENT_TIMEOUT"></span><span id="error_runlevel_switch_agent_timeout"></span>**\_Timeout für Switch-Agent- \_ \_ \_ Timeout für Fehler**
</dt> <dd> <dl> <dt>

15403 (0x3c2b)
</dt> <dt>



Ein Switch-Agent auf Lauf Ebene hat innerhalb des angegebenen Timeouts nicht reagiert.


</dt> </dl> </dd> <dt>

<span id="ERROR_RUNLEVEL_SWITCH_IN_PROGRESS"></span><span id="error_runlevel_switch_in_progress"></span>**Fehler \_ beim Ausführen \_ \_ des \_ Fehlers "Runlevel"**
</dt> <dd> <dl> <dt>

15404 (0x3c2c)
</dt> <dt>



Zurzeit wird ein Switch auf Lauf Ebene ausgeführt.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICES_FAILED_AUTOSTART"></span><span id="error_services_failed_autostart"></span>**Fehler \_ Dienste \_ beim \_ Autostart**
</dt> <dd> <dl> <dt>

15405 (0x3c2d)
</dt> <dt>



Mindestens ein Dienst konnte während der Dienst Startphase eines Schalters auf Lauf Ebene nicht gestartet werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_COM_TASK_STOP_PENDING"></span><span id="error_com_task_stop_pending"></span>**Fehler bei \_ com- \_ Task \_ Beendigung \_ Ausstehend**
</dt> <dd> <dl> <dt>

15501 (0x3c8d)
</dt> <dt>



Die Anforderung zum Beenden der Aufgabe kann nicht sofort abgeschlossen werden, da die Aufgabe mehr Zeit zum Herunterfahren benötigt.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_OPEN_PACKAGE_FAILED"></span><span id="error_install_open_package_failed"></span>**Fehler beim \_ Installieren des \_ geöffneten \_ Pakets \_**
</dt> <dd> <dl> <dt>

15600 (0x3cf0)
</dt> <dt>



Das Paket konnte nicht geöffnet werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_PACKAGE_NOT_FOUND"></span><span id="error_install_package_not_found"></span>**Fehler beim \_ Installieren des \_ Pakets \_ nicht \_ gefunden.**
</dt> <dd> <dl> <dt>

15601 (0x3cf1)
</dt> <dt>



Das Paket wurde nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_INVALID_PACKAGE"></span><span id="error_install_invalid_package"></span>**Fehler beim \_ Installieren des \_ ungültigen \_ Pakets**
</dt> <dd> <dl> <dt>

15602 (0x3cf2)
</dt> <dt>



Die Paketdaten sind ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_RESOLVE_DEPENDENCY_FAILED"></span><span id="error_install_resolve_dependency_failed"></span>**Fehler beim \_ Installieren der \_ \_ Abhängigkeits Abhängigkeit \_ .**
</dt> <dd> <dl> <dt>

15603 (0x3cf3)
</dt> <dt>



Paketfehler bei Updates, Abhängigkeits-oder Konflikt Überprüfung.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_OUT_OF_DISK_SPACE"></span><span id="error_install_out_of_disk_space"></span>**Fehler beim \_ installieren \_ von nicht genügend \_ \_ Speicher \_ Platz.**
</dt> <dd> <dl> <dt>

15604 (0x3cf4)
</dt> <dt>



Auf dem Computer ist nicht genügend Speicherplatz vorhanden. Geben Sie Speicherplatz frei, und wiederholen Sie den Vorgang.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_NETWORK_FAILURE"></span><span id="error_install_network_failure"></span>**Fehler beim \_ Installieren des \_ Netzwerk \_ Fehlers.**
</dt> <dd> <dl> <dt>

15605 (0x3cf5)
</dt> <dt>



Beim Herunterladen des Produkts ist ein Problem aufgetreten.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_REGISTRATION_FAILURE"></span><span id="error_install_registration_failure"></span>**Fehler beim \_ Installieren der \_ Registrierung. \_**
</dt> <dd> <dl> <dt>

15606 (0x3cf6)
</dt> <dt>



Das Paket konnte nicht registriert werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_DEREGISTRATION_FAILURE"></span><span id="error_install_deregistration_failure"></span>**Fehler beim Installieren der Registrierungs Registrierung. \_ \_ \_**
</dt> <dd> <dl> <dt>

15607 (0x3cf7)
</dt> <dt>



Die Registrierung des Pakets konnte nicht aufgehoben werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_CANCEL"></span><span id="error_install_cancel"></span>**Fehler bei \_ Installation \_ Abbrechen**
</dt> <dd> <dl> <dt>

15608 (0x3cf8)
</dt> <dt>



Der Benutzer hat die Installations Anforderung abgebrochen.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_FAILED"></span><span id="error_install_failed"></span>**Fehler bei der \_ Installation. \_**
</dt> <dd> <dl> <dt>

15609 (0x3cf9)
</dt> <dt>



Fehler bei der Installation. Wenden Sie sich an den Softwarehersteller.


</dt> </dl> </dd> <dt>

<span id="ERROR_REMOVE_FAILED"></span><span id="error_remove_failed"></span>**Fehler beim \_ entfernen. \_**
</dt> <dd> <dl> <dt>

15610 (0x3cfa)
</dt> <dt>



Fehler beim Entfernen. Wenden Sie sich an den Softwarehersteller.


</dt> </dl> </dd> <dt>

<span id="ERROR_PACKAGE_ALREADY_EXISTS"></span><span id="error_package_already_exists"></span>**das Fehler \_ Paket ist \_ bereits \_ vorhanden.**
</dt> <dd> <dl> <dt>

15611 (0x3cfb)
</dt> <dt>



Das bereitgestellte Paket ist bereits installiert, und die erneute Installation des Pakets wurde blockiert. Weitere Informationen finden Sie im Ereignisprotokoll AppXDeployment-Server.


</dt> </dl> </dd> <dt>

<span id="ERROR_NEEDS_REMEDIATION"></span><span id="error_needs_remediation"></span>**Fehler \_ \_ Behebung erforderlich**
</dt> <dd> <dl> <dt>

15612 (0x3cfc)
</dt> <dt>



Die Anwendung kann nicht gestartet werden. Installieren Sie die Anwendung neu, um das Problem zu beheben.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_PREREQUISITE_FAILED"></span><span id="error_install_prerequisite_failed"></span>**Fehler beim \_ Installieren der \_ erforderlichen Komponente. \_**
</dt> <dd> <dl> <dt>

15613 (0x3cfd)
</dt> <dt>



Eine Voraussetzung für eine Installation konnte nicht erfüllt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_PACKAGE_REPOSITORY_CORRUPTED"></span><span id="error_package_repository_corrupted"></span>**Fehler \_ Paketrepository \_ \_ beschädigt**
</dt> <dd> <dl> <dt>

15614 (0x3cfe)
</dt> <dt>



Das Paketrepository ist beschädigt.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_POLICY_FAILURE"></span><span id="error_install_policy_failure"></span>**Fehler beim \_ Installieren der \_ Richtlinie \_ .**
</dt> <dd> <dl> <dt>

15615 (0x3cff)
</dt> <dt>



Um diese Anwendung zu installieren, benötigen Sie entweder eine Windows-Entwicklerlizenz oder ein System mit Sideloading.


</dt> </dl> </dd> <dt>

<span id="ERROR_PACKAGE_UPDATING"></span><span id="error_package_updating"></span>**Fehler \_ Paket \_ Aktualisierung**
</dt> <dd> <dl> <dt>

15616 (0x3d00)
</dt> <dt>



Die Anwendung kann nicht gestartet werden, da Sie zurzeit aktualisiert wird.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEPLOYMENT_BLOCKED_BY_POLICY"></span><span id="error_deployment_blocked_by_policy"></span>**Fehler \_ Bereitstellung \_ blockiert \_ durch \_ Richtlinie**
</dt> <dd> <dl> <dt>

15617 (0x3d01)
</dt> <dt>



Der Paket Bereitstellungs Vorgang wird durch die Richtlinie blockiert. Wenden Sie sich an Ihren Systemadministrator.


</dt> </dl> </dd> <dt>

<span id="ERROR_PACKAGES_IN_USE"></span><span id="error_packages_in_use"></span>**\_verwendete Fehler \_ Pakete \_**
</dt> <dd> <dl> <dt>

15618 (0x3d02)
</dt> <dt>



Das Paket konnte nicht installiert werden, da die von ihm modifizierenden Ressourcen zurzeit verwendet werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_RECOVERY_FILE_CORRUPT"></span><span id="error_recovery_file_corrupt"></span>**Fehler \_ Wiederherstellungs \_ Datei \_ beschädigt**
</dt> <dd> <dl> <dt>

15619 (0x3d03)
</dt> <dt>



Das Paket konnte nicht wieder hergestellt werden, da die erforderlichen Daten für die Wiederherstellung beschädigt wurden.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_STAGED_SIGNATURE"></span><span id="error_invalid_staged_signature"></span>**Fehler bei der \_ \_ gestaffelten \_ Signatur.**
</dt> <dd> <dl> <dt>

15620 (0x3d04)
</dt> <dt>



Die Signatur ist ungültig. Zum Registrieren im Entwicklermodus müssen appxsignature. P7X "und AppxBlockMap.xml gültig sein oder nicht vorhanden sein.


</dt> </dl> </dd> <dt>

<span id="ERROR_DELETING_EXISTING_APPLICATIONDATA_STORE_FAILED"></span><span id="error_deleting_existing_applicationdata_store_failed"></span>**Fehler beim \_ Löschen des \_ vorhandenen \_ ApplicationData- \_ Speicher \_ .**
</dt> <dd> <dl> <dt>

15621 (0x3d05)
</dt> <dt>



Beim Löschen der bereits vorhandenen Anwendungsdaten des Pakets ist ein Fehler aufgetreten.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_PACKAGE_DOWNGRADE"></span><span id="error_install_package_downgrade"></span>**Fehler beim \_ Installieren des \_ \_ paketdowngrades**
</dt> <dd> <dl> <dt>

15622 (0x3d06)
</dt> <dt>



Das Paket konnte nicht installiert werden, da bereits eine höhere Version dieses Pakets installiert ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_SYSTEM_NEEDS_REMEDIATION"></span><span id="error_system_needs_remediation"></span>**Fehler \_ System \_ muss wieder hergestellt werden \_**
</dt> <dd> <dl> <dt>

15623 (0x3d07)
</dt> <dt>



Ein Fehler in einer System Binärdatei wurde erkannt. Versuchen Sie, den PC zu aktualisieren, um das Problem zu beheben.


</dt> </dl> </dd> <dt>

<span id="ERROR_APPX_INTEGRITY_FAILURE_CLR_NGEN"></span><span id="error_appx_integrity_failure_clr_ngen"></span>**Fehler beim \_ AppX- \_ Integritäts Fehler \_ \_ CLR \_ ngen**
</dt> <dd> <dl> <dt>

15624 (0x3d08)
</dt> <dt>



Auf dem System wurde eine beschädigte CLR ngen-Binärdatei erkannt.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESILIENCY_FILE_CORRUPT"></span><span id="error_resiliency_file_corrupt"></span>**\_ \_ fehlerresilienzdatei \_ beschädigt**
</dt> <dd> <dl> <dt>

15625 (0x3d09)
</dt> <dt>



Der Vorgang konnte nicht fortgesetzt werden, da die erforderlichen Daten für die Wiederherstellung beschädigt wurden.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_FIREWALL_SERVICE_NOT_RUNNING"></span><span id="error_install_firewall_service_not_running"></span>**Fehler beim \_ Installieren des firewalldienstanbieter. \_ \_ \_ \_**
</dt> <dd> <dl> <dt>

15626 (0x3d0a)
</dt> <dt>



Das Paket konnte nicht installiert werden, da der Windows-Firewall-Dienst nicht ausgeführt wird. Aktivieren Sie den Windows-Firewall-Dienst, und versuchen Sie es erneut


</dt> </dl> </dd> <dt>

<span id="APPMODEL_ERROR_NO_PACKAGE"></span><span id="appmodel_error_no_package"></span>**appmodel- \_ Fehler " \_ kein \_ Paket"**
</dt> <dd> <dl> <dt>

15700 (0x3d54)
</dt> <dt>



Der Prozess hat keine Paket Identität.


</dt> </dl> </dd> <dt>

<span id="APPMODEL_ERROR_PACKAGE_RUNTIME_CORRUPT"></span><span id="appmodel_error_package_runtime_corrupt"></span>**\_Fehler Paket Laufzeit des appmodel \_ \_ \_ beschädigt**
</dt> <dd> <dl> <dt>

15701 (0x3d55)
</dt> <dt>



Die Paket Laufzeitinformationen sind beschädigt.


</dt> </dl> </dd> <dt>

<span id="APPMODEL_ERROR_PACKAGE_IDENTITY_CORRUPT"></span><span id="appmodel_error_package_identity_corrupt"></span>**Identität des appmodel- \_ Fehler \_ Pakets ist \_ \_ beschädigt.**
</dt> <dd> <dl> <dt>

15702 (0x3d56)
</dt> <dt>



Die Paket Identität ist beschädigt.


</dt> </dl> </dd> <dt>

<span id="APPMODEL_ERROR_NO_APPLICATION"></span><span id="appmodel_error_no_application"></span>**appmodel- \_ Fehler " \_ keine \_ Anwendung"**
</dt> <dd> <dl> <dt>

15703 (0x3d57)
</dt> <dt>



Der Prozess hat keine Anwendungs Identität.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_LOAD_STORE_FAILED"></span><span id="error_state_load_store_failed"></span>**Fehler beim Laden des Fehler \_ Zustands. \_ \_ \_**
</dt> <dd> <dl> <dt>

15800 (0x3db8)
</dt> <dt>



Fehler beim Laden des Zustands Speicher.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_GET_VERSION_FAILED"></span><span id="error_state_get_version_failed"></span>**Fehler \_ Status beim \_ get- \_ Version \_ .**
</dt> <dd> <dl> <dt>

15801 (0x3db9)
</dt> <dt>



Fehler beim Abrufen der Zustands Version für die Anwendung.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_SET_VERSION_FAILED"></span><span id="error_state_set_version_failed"></span>**Fehler \_ Zustands \_ Satz- \_ Version \_ fehlgeschlagen**
</dt> <dd> <dl> <dt>

15802 (0x3dba)
</dt> <dt>



Fehler beim Festlegen der Zustands Version für die Anwendung.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_STRUCTURED_RESET_FAILED"></span><span id="error_state_structured_reset_failed"></span>**Fehler \_ beim \_ strukturierten \_ Zurücksetzen des Fehler Zustands \_**
</dt> <dd> <dl> <dt>

15803 (0x3dbb)
</dt> <dt>



Fehler beim Zurücksetzen des strukturierten Zustands der Anwendung.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_OPEN_CONTAINER_FAILED"></span><span id="error_state_open_container_failed"></span>**Fehler \_ Status beim \_ Öffnen des \_ Containers \_ .**
</dt> <dd> <dl> <dt>

15804 (0x3dbc)
</dt> <dt>



Der Zustands-Manager konnte den Container nicht öffnen.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_CREATE_CONTAINER_FAILED"></span><span id="error_state_create_container_failed"></span>**Fehler \_ Status beim \_ Erstellen des \_ Containers \_ .**
</dt> <dd> <dl> <dt>

15805 (0x3dbd)
</dt> <dt>



Fehler beim Erstellen des Containers durch den Zustands-Manager.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_DELETE_CONTAINER_FAILED"></span><span id="error_state_delete_container_failed"></span>**Fehler \_ beim \_ Löschen des \_ Containers \_ .**
</dt> <dd> <dl> <dt>

15806 (0x3dbe)
</dt> <dt>



Der Status-Manager konnte den Container nicht löschen.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_READ_SETTING_FAILED"></span><span id="error_state_read_setting_failed"></span>**Fehler beim Lesen des Fehler \_ Zustands. \_ \_ \_**
</dt> <dd> <dl> <dt>

15807 (0x3dbf)
</dt> <dt>



Fehler beim Lesen der Einstellung durch den Zustands-Manager.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_WRITE_SETTING_FAILED"></span><span id="error_state_write_setting_failed"></span>**Fehler beim Schreiben des Fehler \_ Zustands. \_ \_ \_**
</dt> <dd> <dl> <dt>

15808 (0x3dc0)
</dt> <dt>



Fehler beim Schreiben der Einstellung durch den Zustands-Manager.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_DELETE_SETTING_FAILED"></span><span id="error_state_delete_setting_failed"></span>**Fehler beim Löschen des Fehler \_ Zustands. \_ \_ \_**
</dt> <dd> <dl> <dt>

15809 (0x3dc1)
</dt> <dt>



Fehler beim Löschen der Einstellung durch den Zustands-Manager.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_QUERY_SETTING_FAILED"></span><span id="error_state_query_setting_failed"></span>**Fehler beim Festlegen der Fehler \_ Status \_ Abfrage. \_ \_**
</dt> <dd> <dl> <dt>

15810 (0x3dc2)
</dt> <dt>



Die Einstellung konnte vom Zustands-Manager nicht abgefragt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_READ_COMPOSITE_SETTING_FAILED"></span><span id="error_state_read_composite_setting_failed"></span>**Fehler \_ Status beim Lesen der zusammen \_ \_ gesetzten \_ Einstellung \_**
</dt> <dd> <dl> <dt>

15811 (0x3dc3)
</dt> <dt>



Fehler beim Lesen der zusammengesetzten Einstellung durch den Zustands-Manager.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_WRITE_COMPOSITE_SETTING_FAILED"></span><span id="error_state_write_composite_setting_failed"></span>**Fehler \_ Status beim \_ Schreiben zusammen \_ gesetzter \_ Einstellung \_**
</dt> <dd> <dl> <dt>

15812 (0x3dc4)
</dt> <dt>



Fehler beim Schreiben der zusammengesetzten Einstellung durch den Zustands-Manager.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_ENUMERATE_CONTAINER_FAILED"></span><span id="error_state_enumerate_container_failed"></span>**Fehler \_ beim \_ Aufzählen des \_ Containers \_ für den Fehlerstatus**
</dt> <dd> <dl> <dt>

15813 (0x3dc5)
</dt> <dt>



Der Zustands-Manager konnte die Container nicht aufzählen.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_ENUMERATE_SETTINGS_FAILED"></span><span id="error_state_enumerate_settings_failed"></span>**Fehler \_ beim \_ Aufzählen von \_ Einstellungen \_ .**
</dt> <dd> <dl> <dt>

15814 (0x3dc6)
</dt> <dt>



Der Zustands-Manager konnte die Einstellungen nicht auflisten.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_COMPOSITE_SETTING_VALUE_SIZE_LIMIT_EXCEEDED"></span><span id="error_state_composite_setting_value_size_limit_exceeded"></span>**Fehler \_ Status-zusammen \_ gesetzte \_ Einstellung \_ Wert \_ Größen \_ Limit \_ überschritten**
</dt> <dd> <dl> <dt>

15815 (0x3dc7)
</dt> <dt>



Die Größe des zusammengesetzten Einstellungs Werts für den Zustands-Manager hat das Limit überschritten.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_SETTING_VALUE_SIZE_LIMIT_EXCEEDED"></span><span id="error_state_setting_value_size_limit_exceeded"></span>**Fehler \_ Zustands \_ Einstellung \_ Wert für \_ Größen \_ Beschränkung \_ überschritten**
</dt> <dd> <dl> <dt>

15816 (0x3dc8)
</dt> <dt>



Die Größe des Zustands-Manager-Einstellungs Werts hat das Limit überschritten.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_SETTING_NAME_SIZE_LIMIT_EXCEEDED"></span><span id="error_state_setting_name_size_limit_exceeded"></span>**Einstellung für die \_ namens Größe des Fehler Zustands wurde \_ \_ \_ \_ \_ überschritten.**
</dt> <dd> <dl> <dt>

15817 (0x3dc9)
</dt> <dt>



Die Länge des Zustands-Manager-Einstellungs namens hat das Limit überschritten.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_CONTAINER_NAME_SIZE_LIMIT_EXCEEDED"></span><span id="error_state_container_name_size_limit_exceeded"></span>**Größe des Fehler \_ Zustands für \_ Container \_ Name \_ \_ \_ überschritten**
</dt> <dd> <dl> <dt>

15818 (0x3dca)
</dt> <dt>



Die Länge des Zustands-Manager-Container namens hat das Limit überschritten.


</dt> </dl> </dd> <dt>

<span id="ERROR_API_UNAVAILABLE"></span><span id="error_api_unavailable"></span>**Fehler- \_ API nicht \_ verfügbar**
</dt> <dd> <dl> <dt>

15841 (0x3de 1)
</dt> <dt>



Diese API kann nicht im Kontext des Anwendungs Typs des Aufrufers verwendet werden.


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

 

 
