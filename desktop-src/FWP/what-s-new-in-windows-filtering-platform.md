---
title: Neues in der Windows-Filter Plattform
description: Windows 8 und Windows Server 2012 führen neue Programmier Elemente für die Windows-Filter Plattform ein.
ms.assetid: 7529F155-3DBC-4C22-A780-B6311C455E85
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85b5e441eff3242b530401235b085a1486527b98
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/18/2020
ms.locfileid: "104339877"
---
# <a name="whats-new-in-windows-filtering-platform"></a>Neues in der Windows-Filter Plattform

Windows 8 und Windows Server 2012 führen neue Programmier Elemente für die Windows-Filter Plattform ein. Zu den neuen Funktionen gehören die folgenden:

-   *Layer 2-Filterung*: ermöglicht den Zugriff auf die L2-Ebene (Mac), sodass der Datenverkehr auf dieser Ebene gefiltert werden kann.
-   *vSwitch-Filterung*: ermöglicht das überprüfen und/oder Ändern von Paketen, die einen Vswitch durchlaufen. WFP-Filter oder-Legenden können bei der eingehenden und ausgehenden Vswitch-Daten verwendet werden.
-   *Verwaltung von App*-Containern: ermöglicht den Zugriff auf Informationen zu app-Containern und Verbindungsproblemen bei der Netzwerk Isolation.
-   *IPSec-Updates*: Erweiterte IPsec-Funktionalität, einschließlich Verbindungsstatus Überwachung, Zertifikat Auswahl und Schlüsselverwaltung.

Das Windows-Treiberkit enthält auch Informationen zu [WFP-Änderungen für Windows 8](/windows-hardware/drivers/network/wfp-changes-for-windows-8).

## <a name="windows-8-api-updates"></a>Windows 8-API-Updates

Für Windows 8 und Windows Server 2012 wurden viele neue APIs hinzugefügt.

## <a name="new-functions"></a>Neue Funktionen

-   [**F- \_ net- \_ Ereignis \_ CALLBACK1**](/windows/desktop/api/fwpmu/nc-fwpmu-fwpm_net_event_callback1)
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
-   [**IPSec-Schlüssel- \_ \_ Manager- \_ Schlüssel \_ Diktat \_ CHECK0**](/windows/desktop/api/Fwpmu/nc-fwpmu-ipsec_key_manager_key_dictation_check0)
-   [**IPSec- \_ Schlüssel- \_ Manager \_ \_ Key0 vorschreiben**](/windows/desktop/api/Fwpmu/nc-fwpmu-ipsec_key_manager_dictate_key0)
-   [**IPSec- \_ Schlüssel- \_ Manager \_ Benachrichtigen \_ Key0**](/windows/desktop/api/fwpmu/nc-fwpmu-ipsec_key_manager_notify_key0)
-   [**IPSec- \_ sa- \_ Kontext \_ CALLBACK0**](/windows/win32/api/fwpmu/nc-fwpmu-ipsec_sa_context_callback0)
-   [**IPsecKeyManagerAddAndRegister0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipseckeymanageraddandregister0)
-   [**IPsecKeyManagerGetSecurityInfoByKey0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipseckeymanagergetsecurityinfobykey0)
-   [**IPsecKeyManagerSetSecurityInfoByKey0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipseckeymanagersetsecurityinfobykey0)
-   [**IPsecKeyManagersGet0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipseckeymanagersget0)
-   [**IPsecKeyManagerUnregisterAndDelete0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipseckeymanagerunregisteranddelete0)
-   [**IPsecSaContextSubscribe0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextsubscribe0)
-   [**IPsecSaContextSubscriptionsGet0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextsubscriptionsget0)
-   [**IPsecSaContextUnsubscribe0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextunsubscribe0)
-   [**Networkisolationdiagnoseconnectfailureandgetinfo**](/previous-versions/windows/desktop/api/netfw/nf-netfw-networkisolationdiagnoseconnectfailureandgetinfo)
-   [**Networkisolationeinumappcontainers**](/previous-versions/windows/desktop/api/netfw/nf-netfw-networkisolationenumappcontainers)
-   [**Networkisolationenumerateappcontainerrules**](/previous-versions/windows/desktop/api/netfw/nf-netfw-networkisolationenumerateappcontainerrules)
-   [**Networkisolationfreappcontainers**](/previous-versions/windows/desktop/api/netfw/nf-netfw-networkisolationfreeappcontainers)
-   [**Networkisolationgetappcontainerconfig**](/windows/desktop/api/networkisolation/nf-networkisolation-networkisolationgetappcontainerconfig)
-   [**Networkisolationregisterforappcontainerchanges**](/previous-versions/windows/desktop/api/netfw/nf-netfw-networkisolationregisterforappcontainerchanges)
-   [**Networkisolationabtappcontainerconfig**](/previous-versions/windows/desktop/api/netfw/nf-netfw-networkisolationsetappcontainerconfig)
-   [**Networkisolationsetupappcontainerbinaries**](/windows/desktop/api/networkisolation/nf-networkisolation-networkisolationsetupappcontainerbinaries)
-   [**PAC- \_ Änderungs \_ Rückruf- \_ FN**](/windows/desktop/api/networkisolation/nc-networkisolation-pac_changes_callback_fn)

## <a name="new-structures"></a>Neue Strukturen

-   [**Ikeext- \_ Authentifizierung \_ Methode2**](/windows/win32/api/iketypes/ns-iketypes-ikeext_authentication_method2)
-   [**Ikeext \_ CERT \_ EKUS0**](/windows/win32/api/iketypes/ns-iketypes-ikeext_cert_ekus0)
-   [**Ikeext \_ CERT \_ NAME0**](/windows/win32/api/iketypes/ns-iketypes-ikeext_cert_name0)
-   [**Ikeext- \_ Zertifikat \_ fügen**](/windows/win32/api/iketypes/ns-iketypes-ikeext_certificate_authentication2)
-   [**Ikeext- \_ Zertifikat \_ CRITERIA0**](/windows/win32/api/iketypes/ns-iketypes-ikeext_certificate_criteria0)
-   [**Ikeext \_ EM \_ POLICY2**](/windows/win32/api/iketypes/ns-iketypes-ikeext_em_policy2)
-   [**Ikeext \_ Kerberos \_ AUTHENTICATION1**](/windows/win32/api/iketypes/ns-iketypes-ikeext_kerberos_authentication1)
-   [**Ikeext \_ POLICY2**](/windows/win32/api/iketypes/ns-iketypes-ikeext_policy2)
-   [**IPSec- \_ Schlüssel \_ MANAGER0**](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_key_manager0)
-   [**IPSec- \_ Schlüssel- \_ Manager \_ CALLBACKS0**](/windows/desktop/api/fwpmu/ns-fwpmu-ipsec_key_manager_callbacks0)
-   [**IPSec-Schlüssel \_ \_ Richtlinie1**](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_keying_policy1)
-   [**IPSec- \_ sa- \_ Kontext \_ CHANGE0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_context_change0)
-   [**IPSec- \_ sa- \_ Kontext \_ SUBSCRIPTION0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_context_subscription0)
-   [**IPSec- \_ Transport \_ POLICY2**](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_transport_policy2)
-   [**IPSec- \_ Tunnel \_ ENDPOINT0**](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_tunnel_endpoint0)
-   [**IPSec- \_ Tunnel \_ ENDPOINTS2**](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_tunnel_endpoints2)
-   [**IPSec- \_ Tunnel \_ POLICY2**](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_tunnel_policy2)
-   [**\_CONNECTION0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_connection0)
-   [**WPM- \_ Verbindungs Aufzählung \_ \_ TEMPLATE0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_connection_enum_template0)
-   [**Verbindung mit der \_ SUBSCRIPTION0-Verbindung \_**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_connection_subscription0)
-   [**F \_ \_ EVENT2**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event2)
-   [**BPM \_ net- \_ Ereignis \_ Funktion \_ ALLOW0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_capability_allow0)
-   [**BPM \_ net- \_ Ereignis \_ Funktion \_ DROP0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_capability_drop0)
-   [**F/a \_ - \_ Ereignis \_ Klassifizierung \_ ALLOW0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_classify_allow0)
-   [**F/a \_ - \_ Ereignis \_ Klassifizierung \_ DROP2**](/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_net_event_classify_drop2)
-   [**Löschen eines f \_ - \_ \_ \_ \_ MAC0**](/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_net_event_classify_drop_mac0)
-   [**F- \_ net- \_ Ereignis \_ HEADER2**](/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_net_event_header2)
-   [**Swpm- \_ Anbieter \_ CONTEXT2**](/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_provider_context2)
-   [**Fwpm- \_ vSwitch \_ EVENT0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_vswitch_event0)
-   [**Fwpm \_ vSwitch- \_ Ereignis \_ SUBSCRIPTION0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_vswitch_event_subscription0)

## <a name="new-enumerated-types"></a>Neue Enumerationstypen

-   [**FWP- \_ vSwitch- \_ \_ Netzwerktyp**](/windows/win32/api/fwptypes/ne-fwptypes-fwp_vswitch_network_type)
-   [**atwpm- \_ APPC- \_ Netzwerk \_ \_ Funktionstyp**](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_appc_network_capability_type)
-   [**\_ \_ Typ der Ereignis Ereignis Verbindung \_**](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_connection_event_type)
-   [**fwpm \_ vSwitch \_ - \_ Ereignistyp**](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_vswitch_event_type)
-   [**ikeext \_ CERT \_ - \_ Kriterienname- \_ Typ**](/windows/win32/api/iketypes/ne-iketypes-ikeext_cert_criteria_name_type)
-   [**IPSec- \_ sa- \_ Kontext \_ Ereignis \_ TYPE0**](/windows/desktop/api/Ipsectypes/ne-ipsectypes-ipsec_sa_context_event_type0)

## <a name="new-filtering-layer-identifiers"></a>Neue filterebenenbezeichner

[**Filtern von ebenenbezeichlern:**](management-filtering-layer-identifiers-.md)

-   fwpm- \_ Schicht \_ eingehender Mac- \_ \_ Frame \_ Ethernet
-   \_ \_ ausgehender \_ Mac- \_ Frame \_ der fwpm-Ebene
-   fwpm- \_ Schicht, \_ eingehender Mac- \_ \_ Frame \_
-   \_ \_ ausgehender \_ Mac- \_ Frame \_ der fwpm-Ebene
-   fwpm- \_ Schicht \_ Ingress \_ vSwitch \_ Ethernet
-   fwpm- \_ Schicht, \_ ausgehender \_ vSwitch \_ Ethernet
-   Fwpm- \_ Schicht \_ Eingangs \_ -vSwitch \_ \_ -Transport V4/fwpm- \_ Schicht Eingangs- \_ \_ vSwitch- \_ Transport \_ V6
-   Fwpm- \_ Schicht \_ ausgehender \_ vSwitch \_ \_ -Transport V4/fwpm- \_ Schicht \_ ausgehender \_ vSwitch- \_ Transport \_ V6

## <a name="new-filtering-condition-identifiers"></a>Neue Filter Bedingungs Bezeichner

[**Filtern von Bedingungs bezeichlern:**](filtering-condition-identifiers-.md)

-   Mac-Adresse der WPM-Bedingungs \_ \_ Schnittstelle \_ \_
-   \_ \_ lokale MAC-Adresse für \_ Mac \_
-   \_ \_ Mac- \_ Remote \_ Adresse für den WPM-Zustand
-   \_Typ der Bedingung \_ \_
-   \_ \_ VLAN-ID für fwpm-Bedingung \_
-   \_ \_ NDIS-Port der bwpm-Bedingung \_
-   \_ \_ Dateityp für den NDIS- \_ \_ Medientyp
-   \_ \_ Typ der physischen NDIS- \_ \_ \_ Medientyp
-   WPM- \_ Bedingung \_ L2- \_ Flags
-   \_ \_ lokale MAC-Adresse für \_ den Mac- \_ \_ Typ
-   \_ \_ Mac- \_ Remote \_ \_ Adresstyp für die Schutz Bedingung
-   ID des WPM-Bedingungs- \_ \_ \_ ID-Pakets \_
-   \_ \_ Mac- \_ Quell \_ Adresse für die lwpm-Bedingung
-   \_ \_ Mac- \_ Ziel \_ Adresse der bwpm-Bedingung
-   \_Typ der Mac- \_ \_ Quell \_ Adresse \_ für die Bedingung
-   \_Typ der Mac- \_ \_ Ziel \_ Adresse \_ der bwpm-Bedingung
-   \_ \_ IP- \_ Quellport für die IP-Adresse der Bedingung \_
-   \_ \_ IP- \_ \_ Zielport der BPM-Bedingung
-   fwpm-Bedingungs- \_ \_ vSwitch- \_ ID
-   fwpm-Bedingungs- \_ \_ vSwitch- \_ \_ Netzwerktyp
-   fwpm-Bedingungs- \_ \_ vSwitch \_ Quell \_ Schnittstellen- \_ ID
-   fwpm-Bedingungs- \_ \_ vSwitch- \_ Ziel \_ Schnittstellen- \_ ID
-   fwpm-Bedingungs- \_ \_ vSwitch \_ Quell- \_ VM- \_ ID
-   fwpm-Bedingungs- \_ \_ vSwitch- \_ Ziel-VM- \_ \_ ID
-   \_ \_ Typ der Vswitch- \_ Quell \_ Schnittstelle \_ für fwpm-Bedingung
-   \_ \_ \_ Netzwerk- \_ \_ ID des Vswitch-Mandanten für fwpm

## <a name="new-filtering-condition-flags"></a>Neue filterbedingungs-Flags

[**Filter Bedingungs Flags:**](filtering-condition-flags-.md)

-   das Flag der SWP- \_ Bedingung \_ ist eine \_ \_ Proxy \_ Verbindung.
-   Das BWP-Bedingungs Kennzeichen \_ \_ ist " \_ \_ appcontainer \_ Loopback".
-   das Flag der BWP- \_ Bedingung \_ \_ ist \_ kein \_ appcontainer- \_ Loopback.
-   das Flag der SWP- \_ Bedingung \_ ist die \_ \_ \_ Autorisierung der Richtlinie \_
-   Die f- \_ Bedingung \_ L2 \_ ist \_ natives \_ Ethernet.
-   F WP- \_ Bedingung \_ L2 \_ ist \_ WiFi
-   F WP- \_ Bedingung \_ L2 \_ ist \_ mobiles \_ Breitband
-   F WP- \_ Bedingung \_ L2 \_ ist \_ WiFi Direct- \_ \_ Daten
-   F- \_ Bedingung \_ L2 \_ ist \_ VM2VM
-   Die f- \_ Bedingung \_ L2 \_ ist \_ falsch \_ formatiertes Paket.
-   \_ \_ \_ \_ SWP-Bedingung L2 ist IP- \_ \_ fragmentgruppe
-   SWP- \_ Bedingung \_ L2, \_ Wenn \_ Connector \_ vorhanden ist

## <a name="windows-7-updates-to-the-windows-filtering-platform"></a>Windows 7-Updates für die Windows-Filter Plattform

Im Dokument [Neues in der Windows-Filter Plattform]() werden viele der für Windows 7 vorgenommenen Updates ausführlich erläutert. Informationen finden Sie auch im Windows-Treiberkit unter [WFP-Änderungen für Windows 7](/windows-hardware/drivers/network/wfp-changes-for-windows-7).

 

 