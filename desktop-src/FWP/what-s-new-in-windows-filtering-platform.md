---
title: Neuerungen bei Windows Filterplattform
description: Windows 8 und Windows Server 2012 werden neue Windows Programmierelemente für die Filterplattform eingeführt.
ms.assetid: 7529F155-3DBC-4C22-A780-B6311C455E85
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77e12c1e7add7568b931aabe43f3ab91763df2d5ab12ad448d3683afe13baa3c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119766660"
---
# <a name="whats-new-in-windows-filtering-platform"></a>Neuerungen bei Windows Filterplattform

Windows 8 und Windows Server 2012 werden neue Windows Programmierelemente für die Filterplattform eingeführt. Neue Funktionen umfassen Folgendes:

-   *Layer 2-Filterung:* Ermöglicht den Zugriff auf die L2-Ebene (MAC), sodass der Datenverkehr auf dieser Ebene gefiltert werden kann.
-   *vSwitch-Filterung:* Ermöglicht die Überprüfung und/oder Änderung von Paketen, die einen vSwitch durchlaufen. WFP-Filter oder -Aufrufe können beim ein- und ausgehenden vSwitch verwendet werden.
-   *App-Containerverwaltung:* Ermöglicht den Zugriff auf Informationen zu App-Containern und Konnektivitätsproblemen bei der Netzwerkisolation.
-   *IPsec-Updates:* Erweiterte IPsec-Funktionalität, einschließlich Überwachung des Verbindungszustands, Zertifikatauswahl und Schlüsselverwaltung.

Das Windows Driver Kit enthält auch Informationen zu [WFP-Änderungen für Windows 8](/windows-hardware/drivers/network/wfp-changes-for-windows-8).

## <a name="windows-8-api-updates"></a>Windows 8 API-Updates

Viele neue APIs wurden für Windows 8 und Windows Server 2012 hinzugefügt.

## <a name="new-functions"></a>Neue Funktionen

-   [**FWPM \_ \_ NET-EREIGNISRÜCKRUF1 \_**](/windows/desktop/api/fwpmu/nc-fwpmu-fwpm_net_event_callback1)
-   [**FwpmConnectionCreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmconnectioncreateenumhandle0)
-   [**FwpmConnectionDestroyEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmconnectiondestroyenumhandle0)
-   [**FwpmConnectionEnum0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmconnectionenum0)
-   [**FwpmConnectionGetById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmconnectiongetbyid0)
-   [**FwpmConnectionGetSecurityInfo0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmconnectiongetsecurityinfo0)
-   [**FwpmConnectionSetSecurityInfo0**](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmconnectionsetsecurityinfo0)
-   [**FwpmConnectionSubscribe0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmconnectionsubscribe0)
-   [**FwpmConnectionSubscriptionsGet0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmconnectionsubscriptionsget0)
-   [**FwpmConnectionUnsubscribe0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmconnectionunsubscribe0)
-   [**FwpmIPsecTunnelAdd2**](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmipsectunneladd2)
-   [**FwpmNetEventEnum2**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum2)
-   [**FwpmNetEventSubscribe1**](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmneteventsubscribe1)
-   [**FwpmProviderContextAdd2**](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmprovidercontextadd2)
-   [**FwpmProviderContextEnum2**](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmprovidercontextenum2)
-   [**FwpmProviderContextGetById2**](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmprovidercontextgetbyid2)
-   [**FwpmProviderContextGetByKey2**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextgetbykey2)
-   [**FwpmvSwitchEventsGetSecurityInfo0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmvswitcheventsgetsecurityinfo0)
-   [**FwpmvSwitchEventsSetSecurityInfo0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmvswitcheventssetsecurityinfo0)
-   [**FwpmvSwitchEventSubscribe0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmvswitcheventsubscribe0)
-   [**FwpmvSwitchEventUnsubscribe0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmvswitcheventunsubscribe0)
-   [**IkeextSaEnum2**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsaenum2)
-   [**IkeextSaGetById2**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsagetbyid2)
-   [**IPSEC \_ KEY \_ MANAGER \_ KEY \_ DICTATION \_ CHECK0**](/windows/desktop/api/Fwpmu/nc-fwpmu-ipsec_key_manager_key_dictation_check0)
-   [**\_ \_ IPSEC-SCHLÜSSEL-MANAGER: \_ DIKTIEREN DES \_ SCHLÜSSELS0**](/windows/desktop/api/Fwpmu/nc-fwpmu-ipsec_key_manager_dictate_key0)
-   [**IPSEC \_ KEY \_ MANAGER \_ NOTIFY \_ KEY0**](/windows/desktop/api/fwpmu/nc-fwpmu-ipsec_key_manager_notify_key0)
-   [**IPSEC \_ SA \_ CONTEXT \_ CALLBACK0**](/windows/win32/api/fwpmu/nc-fwpmu-ipsec_sa_context_callback0)
-   [**IPsecKeyManagerAddAndRegister0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipseckeymanageraddandregister0)
-   [**IPsecKeyManagerGetSecurityInfoByKey0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipseckeymanagergetsecurityinfobykey0)
-   [**IPsecKeyManagerSetSecurityInfoByKey0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipseckeymanagersetsecurityinfobykey0)
-   [**IPsecKeyManagersGet0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipseckeymanagersget0)
-   [**IPsecKeyManagerUnregisterAndDelete0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipseckeymanagerunregisteranddelete0)
-   [**IPsecSaContextSubscribe0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextsubscribe0)
-   [**IPsecSaContextSubscriptionsGet0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextsubscriptionsget0)
-   [**IPsecSaContextUnsubscribe0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextunsubscribe0)
-   [**NetworkIsolationDiagnoseConnectFailureAndGetInfo**](/previous-versions/windows/desktop/api/netfw/nf-netfw-networkisolationdiagnoseconnectfailureandgetinfo)
-   [**NetworkIsolationEnumAppContainers**](/previous-versions/windows/desktop/api/netfw/nf-netfw-networkisolationenumappcontainers)
-   [**NetworkIsolationEnumerateAppContainerRules**](/previous-versions/windows/desktop/api/netfw/nf-netfw-networkisolationenumerateappcontainerrules)
-   [**NetworkIsolationFreeAppContainers**](/previous-versions/windows/desktop/api/netfw/nf-netfw-networkisolationfreeappcontainers)
-   [**NetworkIsolationGetAppContainerConfig**](/windows/desktop/api/networkisolation/nf-networkisolation-networkisolationgetappcontainerconfig)
-   [**NetworkIsolationRegisterForAppContainerChanges**](/previous-versions/windows/desktop/api/netfw/nf-netfw-networkisolationregisterforappcontainerchanges)
-   [**NetworkIsolationSetAppContainerConfig**](/previous-versions/windows/desktop/api/netfw/nf-netfw-networkisolationsetappcontainerconfig)
-   [**NetworkIsolationSetupAppContainerBinaries**](/windows/desktop/api/networkisolation/nf-networkisolation-networkisolationsetupappcontainerbinaries)
-   [**PAC \_ CHANGES \_ CALLBACK \_ FN**](/windows/desktop/api/networkisolation/nc-networkisolation-pac_changes_callback_fn)

## <a name="new-structures"></a>Neue Strukturen

-   [**\_IKEEXT-AUTHENTIFIZIERUNGSMETHODE2 \_**](/windows/win32/api/iketypes/ns-iketypes-ikeext_authentication_method2)
-   [**IKEEXT \_ CERT \_ EKUS0**](/windows/win32/api/iketypes/ns-iketypes-ikeext_cert_ekus0)
-   [**\_IKEEXT-ZERTIFIKATNAME0 \_**](/windows/win32/api/iketypes/ns-iketypes-ikeext_cert_name0)
-   [**IKEEXT \_ CERTIFICATE \_ AUTHENTICATION2**](/windows/win32/api/iketypes/ns-iketypes-ikeext_certificate_authentication2)
-   [**IKEEXT \_ CERTIFICATE \_ CRITERIA0**](/windows/win32/api/iketypes/ns-iketypes-ikeext_certificate_criteria0)
-   [**IKEEXT \_ EM \_ POLICY2**](/windows/win32/api/iketypes/ns-iketypes-ikeext_em_policy2)
-   [**IKEEXT \_ KERBEROS \_ AUTHENTICATION1**](/windows/win32/api/iketypes/ns-iketypes-ikeext_kerberos_authentication1)
-   [**IKEEXT \_ POLICY2**](/windows/win32/api/iketypes/ns-iketypes-ikeext_policy2)
-   [**\_ \_ IPSEC-SCHLÜSSEL-MANAGER0**](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_key_manager0)
-   [**IPSEC \_ KEY \_ MANAGER \_ CALLBACKS0**](/windows/desktop/api/fwpmu/ns-fwpmu-ipsec_key_manager_callbacks0)
-   [**\_ \_ IPSEC-SCHLÜSSELRICHTLINIE1**](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_keying_policy1)
-   [**IPSEC \_ SA \_ CONTEXT \_ CHANGE0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_context_change0)
-   [**IPSEC \_ SA \_ CONTEXT \_ SUBSCRIPTION0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_context_subscription0)
-   [**\_ \_ IPSEC-TRANSPORTRICHTLINIE2**](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_transport_policy2)
-   [**IPSEC \_ TUNNEL \_ ENDPOINT0**](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_tunnel_endpoint0)
-   [**\_ \_ IPSEC-TUNNELENDPUNKTE2**](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_tunnel_endpoints2)
-   [**\_ \_ IPSEC-TUNNELRICHTLINIE2**](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_tunnel_policy2)
-   [**FWPM \_ CONNECTION0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_connection0)
-   [**FWPM \_ CONNECTION \_ ENUM \_ TEMPLATE0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_connection_enum_template0)
-   [**\_ \_ FWPM-VERBINDUNGSABONNEMENT0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_connection_subscription0)
-   [**FWPM \_ NET \_ EVENT2**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event2)
-   [**FWPM \_ \_ NET-EREIGNISFUNKTION \_ \_ ALLOW0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_capability_allow0)
-   [**FWPM \_ \_ NET-EREIGNISFUNKTION \_ \_ DROP0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_capability_drop0)
-   [**FWPM \_ \_ NET-EREIGNIS \_ CLASSIFY \_ ALLOW0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_classify_allow0)
-   [**FWPM \_ \_ NET-EREIGNIS \_ CLASSIFY \_ DROP2**](/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_net_event_classify_drop2)
-   [**FWPM \_ \_ NET-EREIGNIS \_ CLASSIFY \_ DROP \_ MAC0**](/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_net_event_classify_drop_mac0)
-   [**FWPM \_ \_ NET-EREIGNISHEADER2 \_**](/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_net_event_header2)
-   [**\_FWPM-ANBIETER \_ CONTEXT2**](/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_provider_context2)
-   [**FWPM \_ VSWITCH \_ EVENT0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_vswitch_event0)
-   [**FWPM \_ \_ VSWITCH-EREIGNISABONNEMENT0 \_**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_vswitch_event_subscription0)

## <a name="new-enumerated-types"></a>Neue aufzählte Typen

-   [**FWP \_ \_ VSWITCH-NETZWERKTYP \_**](/windows/win32/api/fwptypes/ne-fwptypes-fwp_vswitch_network_type)
-   [**FWPM \_ \_ APPC-NETZWERKFUNKTIONSTYP \_ \_**](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_appc_network_capability_type)
-   [**\_FWPM-VERBINDUNGSEREIGNISTYP \_ \_**](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_connection_event_type)
-   [**FWPM \_ \_ VSWITCH-EREIGNISTYP \_**](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_vswitch_event_type)
-   [**IKEEXT \_ CERT \_ CRITERIA \_ NAME \_ TYPE**](/windows/win32/api/iketypes/ne-iketypes-ikeext_cert_criteria_name_type)
-   [**IPSEC \_ SA \_ CONTEXT \_ EVENT \_ TYPE0**](/windows/desktop/api/Ipsectypes/ne-ipsectypes-ipsec_sa_context_event_type0)

## <a name="new-filtering-layer-identifiers"></a>Neue Filterebenenbezeichner

[**Filtern von Ebenenbezeichnern:**](management-filtering-layer-identifiers-.md)

-   FWPM \_ LAYER \_ INBOUND \_ MAC \_ FRAME \_ ETHERNET
-   FWPM \_ LAYER \_ OUTBOUND \_ MAC \_ FRAME \_ ETHERNET
-   FWPM \_ LAYER \_ INBOUND \_ MAC \_ FRAME \_ NATIVE
-   FWPM \_ LAYER \_ OUTBOUND \_ MAC \_ FRAME \_ NATIVE
-   FWPM \_ LAYER \_ INGRESS \_ VSWITCH \_ ETHERNET
-   AUSGEHENDES \_ \_ \_ VSWITCH-ETHERNET AUF FWPM-EBENE \_
-   FWPM \_ LAYER \_ INGRESS \_ VSWITCH \_ TRANSPORT \_ V4/FWPM \_ LAYER \_ INGRESS \_ VSWITCH \_ TRANSPORT \_ V6
-   FWPM \_ LAYER \_ EGRESS \_ VSWITCH \_ TRANSPORT \_ V4/FWPM \_ LAYER \_ EGRESS \_ VSWITCH \_ TRANSPORT \_ V6

## <a name="new-filtering-condition-identifiers"></a>Neue Filterbedingungsbezeichner

[**Filterbedingungsbezeichner:**](filtering-condition-identifiers-.md)

-   MAC-ADRESSE DER \_ FWPM-BEDINGUNGSSCHNITTSTELLE \_ \_ \_
-   LOKALE ADRESSE DER \_ FWPM-BEDINGUNG \_ FÜR MAC \_ \_
-   \_FWPM-BEDINGUNG \_ \_ MAC-REMOTEADRESSE \_
-   \_FWPM-BEDINGUNG \_ – TYP \_ "ETHER"
-   \_VLAN-ID DER FWPM-BEDINGUNG \_ \_
-   \_ \_ FWPM-BEDINGUNGS-NDIS-PORT \_
-   \_FWPM-BEDINGUNG \_ NDIS-MEDIENTYP \_ \_
-   PHYSISCHER \_ \_ FWPM-BEDINGUNGS-NDIS-MEDIENTYP \_ \_ \_
-   \_FWPM-BEDINGUNG \_ \_ L2-FLAGS
-   \_FWPM-BEDINGUNG \_ \_ MAC– LOKALER \_ \_ ADRESSTYP
-   FWPM-BEDINGUNG \_ \_ \_ MAC-REMOTEADRESSENTYP \_ \_
-   \_ALE-PAKET-ID \_ FÜR FWPM-BEDINGUNG \_ \_
-   FWPM-BEDINGUNG \_ \_ \_ MAC-QUELLADRESSE \_
-   FWPM-BEDINGUNG \_ \_ \_ MAC-ZIELADRESSE \_
-   \_FWPM-BEDINGUNG \_ \_ MAC-QUELLADRESSENTYP \_ \_
-   FWPM-BEDINGUNG \_ \_ \_ MAC-ZIELADRESSENTYP \_ \_
-   FWPM-BEDINGUNG: \_ \_ \_ IP-QUELLPORT \_
-   FWPM-BEDINGUNG \_ \_ \_ IP-ZIELPORT \_
-   \_ \_ VSWITCH-ID für FWPM-BEDINGUNG \_
-   \_ \_ VSWITCH-NETZWERKTYP FÜR FWPM-BEDINGUNG \_ \_
-   FWPM-BEDINGUNG: \_ \_ VSWITCH-QUELLSCHNITTSTELLEN-ID \_ \_ \_
-   FWPM-BEDINGUNG: \_ \_ VSWITCH-ZIELSCHNITTSTELLEN-ID \_ \_ \_
-   VM-ID der \_ \_ FWPM-BEDINGUNGS-VSWITCH-QUELLE \_ \_ \_
-   FWPM-BEDINGUNG \_ \_ VSWITCH-ZIEL-VM-ID \_ \_ \_
-   TYP DER \_ \_ VSWITCH-QUELLSCHNITTSTELLE FÜR FWPM-BEDINGUNG \_ \_ \_
-   NETZWERK-ID DES \_ \_ VSWITCH-MANDANTEN FÜR FWPM-BEDINGUNG \_ \_ \_

## <a name="new-filtering-condition-flags"></a>Neue Filterbedingungsflags

[**Filterbedingungsflags:**](filtering-condition-flags-.md)

-   \_ \_ FWP-BEDINGUNGSFLAG \_ IST \_ \_ PROXYVERBINDUNG
-   \_ \_ FWP-BEDINGUNGSFLAG \_ IST \_ APPCONTAINER \_ LOOPBACK
-   \_ \_ FWP-BEDINGUNGSFLAG \_ IST NICHT \_ \_ APPCONTAINER \_ LOOPBACK
-   \_ \_ FWP-BEDINGUNGSFLAG \_ WIRD RICHTLINIEN \_ \_ \_ AUTORISIERT.
-   FWP-BEDINGUNG \_ \_ L2 \_ IST \_ SYSTEMEIGENES \_ ETHERNET
-   FWP-BEDINGUNG \_ \_ L2 \_ IS \_ WIFI
-   FWP-BEDINGUNG \_ \_ L2 \_ IST \_ MOBILES \_ BREITBAND
-   FWP-BEDINGUNG \_ \_ \_ L2: DIREKTE \_ \_ \_ WLAN-DATEN
-   FWP-BEDINGUNG \_ \_ L2 \_ IST \_ VM2VM
-   \_FWP-BEDINGUNG \_ L2 \_ IST FALSCH \_ FORMATIERTES \_ PAKET
-   FWP-BEDINGUNG \_ \_ L2 \_ IST \_ \_ IP-FRAGMENTGRUPPE \_
-   FWP-BEDINGUNG \_ \_ L2, \_ FALLS CONNECTOR \_ \_ VORHANDEN

## <a name="windows-7-updates-to-the-windows-filtering-platform"></a>Windows 7 updates to the Windows Filtering Platform

Das Dokument [What es New in Windows Filtering Platform]() (Neuigkeiten in Windows Filterplattform) enthält viele der Updates, die für Windows 7 vorgenommen wurden. Informationen finden Sie auch im Windows Driver Kit für [WFP-Änderungen für Windows 7.](/windows-hardware/drivers/network/wfp-changes-for-windows-7)

 

 