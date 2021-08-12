---
title: NAP-Fehlerkonstanten (WinError.h)
description: Die folgenden NAP-Fehlerkonstanten sind in WinError.h definiert.
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
ms.openlocfilehash: 411500ea5f0fc3ba0f1d4067a6befe902a81af3154c91e76c36425c289616eb8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118620839"
---
# <a name="nap-error-constants"></a>NAP-Fehlerkonstanten

> [!Note]  
> Die Netzwerkzugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die folgenden NAP-Fehlerkonstanten sind in WinError.h definiert.

<dl> <dt>

<span id="NAP_E_INVALID_PACKET"></span><span id="nap_e_invalid_packet"></span>**NAP \_ E \_ INVALID \_ PACKET**
</dt> <dd> <dl> <dt>

\_HRESULT \_ TYPEDEF \_ (0x80270001L)
</dt> <dt>



Das [**NAP-SoH-Paket**](/windows/win32/api/naptypes/ns-naptypes-soh) ist ungültig.


</dt> </dl> </dd> <dt>

<span id="NAP_E_MISSING_SOH"></span><span id="nap_e_missing_soh"></span>**NAP \_ E \_ MISSING \_ SOH**
</dt> <dd> <dl> <dt>

\_HRESULT \_ TYPEDEF \_ (0x80270002L)
</dt> <dt>



Ein [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) fehlte im NAP-Paket.


</dt> </dl> </dd> <dt>

<span id="NAP_E_CONFLICTING_ID"></span><span id="nap_e_conflicting_id"></span>**IN \_ \_ KONFLIKTSTEHENDE \_ NAP E-ID**
</dt> <dd> <dl> <dt>

\_HRESULT \_ TYPEDEF \_ (0x80270003L)
</dt> <dt>



Die Entitäts-ID steht in Konflikt mit einer bereits registrierten Entitäts-ID.


</dt> </dl> </dd> <dt>

<span id="NAP_E_NO_CACHED_SOH"></span><span id="nap_e_no_cached_soh"></span>**NAP \_ E \_ NO \_ CACHED \_ SOH**
</dt> <dd> <dl> <dt>

\_HRESULT \_ TYPEDEF \_ (0x80270004L)
</dt> <dt>



Es ist kein zwischengespeichertes [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) vorhanden.


</dt> </dl> </dd> <dt>

<span id="NAP_E_STILL_BOUND"></span><span id="nap_e_still_bound"></span>**NAP \_ E \_ NOCH \_ GEBUNDEN**
</dt> <dd> <dl> <dt>

\_HRESULT \_ TYPEDEF \_ (0x80270005L)
</dt> <dt>



Die Entität ist weiterhin an das NAP-System gebunden.


</dt> </dl> </dd> <dt>

<span id="NAP_E_NOT_REGISTERED"></span><span id="nap_e_not_registered"></span>**NAP \_ E \_ NICHT \_ REGISTRIERT**
</dt> <dd> <dl> <dt>

\_HRESULT \_ TYPEDEF \_ (0x80270006L)
</dt> <dt>



Die Entität ist nicht beim NAP-System registriert.


</dt> </dl> </dd> <dt>

<span id="NAP_E_NOT_INITIALIZED"></span><span id="nap_e_not_initialized"></span>**NAP \_ E \_ NICHT \_ INITIALISIERT**
</dt> <dd> <dl> <dt>

\_HRESULT \_ TYPEDEF \_ (0x80270007L)
</dt> <dt>



Die Entität wird nicht mit dem NAP-System initialisiert.


</dt> </dl> </dd> <dt>

<span id="NAP_E_MISMATCHED_ID"></span><span id="nap_e_mismatched_id"></span>**NICHT \_ \_ ÜBEREINSTIMMENDE \_ NAP E-ID**
</dt> <dd> <dl> <dt>

\_HRESULT \_ TYPEDEF \_ (0x80270008L)
</dt> <dt>



Die Korrelations-IDs in der [**SoH-Anforderung**](/windows/win32/api/naptypes/ns-naptypes-soh) und **der SoH-Antwort** stimmen nicht überein.


</dt> </dl> </dd> <dt>

<span id="NAP_E_NOT_PENDING"></span><span id="nap_e_not_pending"></span>**NAP \_ E \_ NOT \_ PENDING**
</dt> <dd> <dl> <dt>

\_HRESULT \_ TYPEDEF \_ (0x80270009L)
</dt> <dt>



Der Abschluss wurde für eine Anforderung angegeben, die derzeit nicht aussteht.


</dt> </dl> </dd> <dt>

<span id="NAP_E_ID_NOT_FOUND"></span><span id="nap_e_id_not_found"></span>**\_ \_ NAP-E-ID \_ NICHT \_ GEFUNDEN**
</dt> <dd> <dl> <dt>

\_HRESULT \_ TYPEDEF \_ (0x8027000AL)
</dt> <dt>



Die ID der NAP-Komponente wurde nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="NAP_E_MAXSIZE_TOO_SMALL"></span><span id="nap_e_maxsize_too_small"></span>**NAP \_ E \_ MAXSIZE \_ ZU \_ KLEIN**
</dt> <dd> <dl> <dt>

\_HRESULT \_ TYPEDEF \_ (0x8027000BL)
</dt> <dt>



Die maximale Verbindungsgröße ist für ein SoH-Paket zu klein.


</dt> </dl> </dd> <dt>

<span id="NAP_E_SERVICE_NOT_RUNNING"></span><span id="nap_e_service_not_running"></span>**NAP \_ \_ E-DIENST \_ WIRD NICHT \_ AUSGEFÜHRT**
</dt> <dd> <dl> <dt>

\_HRESULT \_ TYPEDEF \_ (0x8027000CL)
</dt> <dt>



Der NapAgent-Dienst wird nicht ausgeführt.


</dt> </dl> </dd> <dt>

<span id="NAP_S_CERT_ALREADY_PRESENT"></span><span id="nap_s_cert_already_present"></span>**NAP \_ S \_ CERT BEREITS \_ \_ VORHANDEN**
</dt> <dd> <dl> <dt>

\_HRESULT \_ TYPEDEF \_ (0x0027000DL) 
</dt> <dt>



Ein Zertifikat ist bereits im Zertifikatspeicher vorhanden.


</dt> </dl> </dd> <dt>

<span id="NAP_E_ENTITY_DISABLED"></span><span id="nap_e_entity_disabled"></span>**NAP \_ E \_ ENTITY \_ DISABLED**
</dt> <dd> <dl> <dt>

\_HRESULT \_ TYPEDEF \_ (0x8027000EL)
</dt> <dt>



Die Entität ist mit dem NapAgent-Dienst deaktiviert.


</dt> </dl> </dd> <dt>

<span id="NAP_E_NETSH_GROUPPOLICY_ERROR"></span><span id="nap_e_netsh_grouppolicy_error"></span>**NAP \_ E \_ NETSH \_ GROUPPOLICY \_ ERROR**
</dt> <dd> <dl> <dt>

\_HRESULT \_ TYPEDEF \_ (0x8027000FL)
</dt> <dt>



Gruppenrichtlinie ist nicht konfiguriert.


</dt> </dl> </dd> <dt>

<span id="NAP_E_TOO_MANY_CALLS"></span><span id="nap_e_too_many_calls"></span>**NAP \_ E ZU VIELE \_ \_ \_ AUFRUFE**
</dt> <dd> <dl> <dt>

\_HRESULT \_ TYPEDEF \_ (0x80270010L)
</dt> <dt>



Zu viele gleichzeitige Aufrufe.


</dt> </dl> </dd> <dt>

<span id="NAP_E_SHV_CONFIG_EXISTED"></span><span id="nap_e_shv_config_existed"></span>**NAP \_ E \_ SHV \_ CONFIG \_ EXISTED**
</dt> <dd> <dl> <dt>

\_HRESULT \_ TYPEDEF \_ (0x80270011L)
</dt> <dt>



Die SHV-Konfiguration ist bereits vorhanden.

> [!Note]  
> Wird in Windows 7 oder höher unterstützt.

 


</dt> </dl> </dd> <dt>

<span id="NAP_E_SHV_CONFIG_NOT_FOUND"></span><span id="nap_e_shv_config_not_found"></span>**NAP \_ E \_ \_ SHV-KONFIGURATION NICHT \_ \_ GEFUNDEN**
</dt> <dd> <dl> <dt>

\_HRESULT \_ TYPEDEF \_ (0x80270012L)
</dt> <dt>



Die SHV-Konfiguration wurde nicht gefunden.

> [!Note]  
> Wird in Windows 7 oder höher unterstützt.

 


</dt> </dl> </dd> <dt>

<span id="NAP_E_SHV_TIMEOUT"></span><span id="nap_e_shv_timeout"></span>**NAP \_ E \_ SHV \_ TIMEOUT**
</dt> <dd> <dl> <dt>

\_HRESULT \_ TYPEDEF \_ (0x80270013L)
</dt> <dt>



SHV-Timetimetime für die Anforderung.

> [!Note]  
> Wird in Windows 7 oder höher unterstützt.

 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>WinError.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**NAP-Konstanten**](nap-constants.md)
</dt> </dl>

 

 





