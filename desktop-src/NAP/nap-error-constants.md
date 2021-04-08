---
title: NAP-Fehler Konstanten (Winerror. h)
description: Die folgenden NAP-Fehler Konstanten werden in WinError. h definiert.
ms.assetid: b2fba990-75d9-4153-8058-c01e97700d00
topic_type:
- apiref
api_name:
- NAP_E_INVALID_PACKET
- NAP_E_MISSING_SOH
- NAP_E_CONFLICTING_ID
- NAP_E_NO_CACHED_SOH
- NAP_E_STILL_BOUND
- NAP_E_NOT_REGISTERED
- NAP_E_NOT_INITIALIZED
- NAP_E_MISMATCHED_ID
- NAP_E_NOT_PENDING
- NAP_E_ID_NOT_FOUND
- NAP_E_MAXSIZE_TOO_SMALL
- NAP_E_SERVICE_NOT_RUNNING
- NAP_S_CERT_ALREADY_PRESENT
- NAP_E_ENTITY_DISABLED
- NAP_E_NETSH_GROUPPOLICY_ERROR
- NAP_E_TOO_MANY_CALLS
- NAP_E_SHV_CONFIG_EXISTED
- NAP_E_SHV_CONFIG_NOT_FOUND
- NAP_E_SHV_TIMEOUT
api_location:
- WinError.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b871d6f00174f05ab580aad54395851fa70af877
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956964"
---
# <a name="nap-error-constants"></a>NAP-Fehler Konstanten

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die folgenden NAP-Fehler Konstanten werden in WinError. h definiert.

<dl> <dt>

<span id="NAP_E_INVALID_PACKET"></span><span id="nap_e_invalid_packet"></span>**\_ \_ Ungültiges NAP- \_ Paket**
</dt> <dd> <dl> <dt>

\_HRESULT- \_ typedef \_ (0x80270001l)
</dt> <dt>



Das NAP- [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) -Paket ist ungültig.


</dt> </dl> </dd> <dt>

<span id="NAP_E_MISSING_SOH"></span><span id="nap_e_missing_soh"></span>**NAP \_ E \_ fehlt \_ SoH**
</dt> <dd> <dl> <dt>

\_HRESULT- \_ typedef \_ (0x80270002l)
</dt> <dt>



Im NAP-Paket fehlte ein [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) .


</dt> </dl> </dd> <dt>

<span id="NAP_E_CONFLICTING_ID"></span><span id="nap_e_conflicting_id"></span>**in \_ \_ Konflikt stehende \_ ID für NAP**
</dt> <dd> <dl> <dt>

\_HRESULT- \_ typedef \_ (0x80270003l)
</dt> <dt>



Die Entitäts-ID steht in Konflikt mit einer bereits registrierten Entitäts-ID.


</dt> </dl> </dd> <dt>

<span id="NAP_E_NO_CACHED_SOH"></span><span id="nap_e_no_cached_soh"></span>**NAP \_ E \_ kein \_ zwischengespeichertes \_ SoH**
</dt> <dd> <dl> <dt>

\_HRESULT- \_ typedef \_ (0x80270004l)
</dt> <dt>



Es ist kein zwischengespeichertes [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) vorhanden.


</dt> </dl> </dd> <dt>

<span id="NAP_E_STILL_BOUND"></span><span id="nap_e_still_bound"></span>**NAP \_ E \_ trotzdem \_ gebunden**
</dt> <dd> <dl> <dt>

\_HRESULT- \_ typedef \_ (0x80270005l)
</dt> <dt>



Die Entität ist weiterhin an das NAP-System gebunden.


</dt> </dl> </dd> <dt>

<span id="NAP_E_NOT_REGISTERED"></span><span id="nap_e_not_registered"></span>**NAP \_ E \_ nicht \_ registriert**
</dt> <dd> <dl> <dt>

\_HRESULT- \_ typedef \_ (0x80270006l)
</dt> <dt>



Die Entität ist nicht beim NAP-System registriert.


</dt> </dl> </dd> <dt>

<span id="NAP_E_NOT_INITIALIZED"></span><span id="nap_e_not_initialized"></span>**NAP \_ E \_ nicht \_ Initialisiert**
</dt> <dd> <dl> <dt>

\_HRESULT- \_ typedef \_ (0x80270007l)
</dt> <dt>



Die Entität ist nicht mit dem NAP-System initialisiert.


</dt> </dl> </dd> <dt>

<span id="NAP_E_MISMATCHED_ID"></span><span id="nap_e_mismatched_id"></span>**nicht \_ \_ übereinstimmende NAP- \_ ID**
</dt> <dd> <dl> <dt>

\_HRESULT- \_ typedef \_ (0x80270008l)
</dt> <dt>



Die Korrelations-IDs in der [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) -Anforderung und **SoH** -Antwort stimmen nicht ab.


</dt> </dl> </dd> <dt>

<span id="NAP_E_NOT_PENDING"></span><span id="nap_e_not_pending"></span>**NAP \_ E \_ nicht \_ Ausstehend**
</dt> <dd> <dl> <dt>

\_HRESULT- \_ typedef \_ (0x80270009l)
</dt> <dt>



Der Abschluss wurde für eine Anforderung angegeben, die derzeit nicht aussteht.


</dt> </dl> </dd> <dt>

<span id="NAP_E_ID_NOT_FOUND"></span><span id="nap_e_id_not_found"></span>**NAP- \_ E- \_ ID \_ nicht \_ gefunden.**
</dt> <dd> <dl> <dt>

\_HRESULT- \_ typedef \_ (0x8027000al)
</dt> <dt>



Die ID der NAP-Komponente wurde nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="NAP_E_MAXSIZE_TOO_SMALL"></span><span id="nap_e_maxsize_too_small"></span>**NAP \_ E \_ MaxSize \_ zu \_ klein**
</dt> <dd> <dl> <dt>

\_HRESULT- \_ typedef \_ (0x8027000bl)
</dt> <dt>



Die maximale Größe der Verbindung ist zu klein für ein SoH-Paket.


</dt> </dl> </dd> <dt>

<span id="NAP_E_SERVICE_NOT_RUNNING"></span><span id="nap_e_service_not_running"></span>**NAP- \_ E- \_ Dienst wird \_ nicht \_ ausgeführt**
</dt> <dd> <dl> <dt>

\_HRESULT- \_ typedef \_ (0x8027000cl)
</dt> <dt>



Der NAPAgent-Dienst wird nicht ausgeführt.


</dt> </dl> </dd> <dt>

<span id="NAP_S_CERT_ALREADY_PRESENT"></span><span id="nap_s_cert_already_present"></span>**das NAP- \_ \_ Zertifikat ist \_ bereits \_ vorhanden.**
</dt> <dd> <dl> <dt>

\_HRESULT- \_ typedef \_ (0x0027000dl) 
</dt> <dt>



Im Zertifikat Speicher ist bereits ein Zertifikat vorhanden.


</dt> </dl> </dd> <dt>

<span id="NAP_E_ENTITY_DISABLED"></span><span id="nap_e_entity_disabled"></span>**NAP- \_ E- \_ Entität \_ deaktiviert**
</dt> <dd> <dl> <dt>

\_HRESULT- \_ typedef \_ (0x8027000el)
</dt> <dt>



Die Entität ist mit dem NAPAgent-Dienst deaktiviert.


</dt> </dl> </dd> <dt>

<span id="NAP_E_NETSH_GROUPPOLICY_ERROR"></span><span id="nap_e_netsh_grouppolicy_error"></span>**NAP \_ E \_ netsh \_ GroupPolicy- \_ Fehler**
</dt> <dd> <dl> <dt>

\_HRESULT- \_ typedef \_ (0x8027000fl)
</dt> <dt>



Gruppenrichtlinie ist nicht konfiguriert.


</dt> </dl> </dd> <dt>

<span id="NAP_E_TOO_MANY_CALLS"></span><span id="nap_e_too_many_calls"></span>**NAP- \_ E \_ zu \_ viele \_ Aufrufe**
</dt> <dd> <dl> <dt>

\_HRESULT- \_ typedef \_ (0x80270010l)
</dt> <dt>



Zu viele gleichzeitige Aufrufe.


</dt> </dl> </dd> <dt>

<span id="NAP_E_SHV_CONFIG_EXISTED"></span><span id="nap_e_shv_config_existed"></span>**NAP- \_ E- \_ SHV- \_ Konfiguration \_ vorhanden**
</dt> <dd> <dl> <dt>

\_HRESULT- \_ typedef \_ (0x80270011l)
</dt> <dt>



Die SHV-Konfiguration ist bereits vorhanden.

> [!Note]  
> Unterstützt in Windows 7 oder höher.

 


</dt> </dl> </dd> <dt>

<span id="NAP_E_SHV_CONFIG_NOT_FOUND"></span><span id="nap_e_shv_config_not_found"></span>**NAP- \_ E- \_ SHV- \_ Konfiguration \_ nicht \_ gefunden**
</dt> <dd> <dl> <dt>

\_HRESULT- \_ typedef \_ (0x80270012l)
</dt> <dt>



Die SHV-Konfiguration wurde nicht gefunden.

> [!Note]  
> Unterstützt in Windows 7 oder höher.

 


</dt> </dl> </dd> <dt>

<span id="NAP_E_SHV_TIMEOUT"></span><span id="nap_e_shv_timeout"></span>**NAP- \_ E- \_ SHV- \_ Timeout**
</dt> <dd> <dl> <dt>

\_HRESULT- \_ typedef \_ (0x80270013l)
</dt> <dt>



Bei SHV ist für die Anforderung ein Timeout aufgetreten.

> [!Note]  
> Unterstützt in Windows 7 oder höher.

 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Winerror. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**NAP-Konstanten**](nap-constants.md)
</dt> </dl>

 

 





