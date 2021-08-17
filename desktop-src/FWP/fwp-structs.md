---
title: WFP-Strukturen
description: Die Windows WFP-API-Strukturen (Filtering Platform) sind wie folgt.
ms.assetid: e957132f-417b-40c1-afe3-5aec0e2192f7
keywords:
- Windows Filtern von Aufzählungstypen der Plattform-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20b1bd45efbe1a93ddeb0c95161aa52764bf1812ecc5f8e914e01317b657f251
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119069170"
---
# <a name="wfp-structures"></a>WFP-Strukturen

Die Windows WFP-API-Strukturen (Filtering Platform) sind wie folgt.

Verwaltungsstrukturen

-   [**FWPM \_ ACTION0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_action0)
-   [**FWPM \_ CALLOUT0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_callout0)
-   [**FWPM \_ CALLOUT \_ CHANGE0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_callout_change0)
-   [**FWPM \_ CALLOUT \_ ENUM \_ TEMPLATE0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_callout_enum_template0)
-   [**FWPM \_ CALLOUT \_ SUBSCRIPTION0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_callout_subscription0)
-   [**FWPM \_ CLASSIFY \_ OPTION0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_classify_option0)
-   [**FWPM \_ KLASSIFIZIEREN \_ VON OPTIONEN0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_classify_options0)
-   [**FWPM \_ CONNECTION0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_connection0)
-   [**FWPM \_ CONNECTION \_ ENUM \_ TEMPLATE0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_connection_enum_template0)
-   [**\_ \_ FWPM-VERBINDUNGSABONNEMENT0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_connection_subscription0)
-   [**FWPM \_ DISPLAY \_ DATA0**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwpm_display_data0)
-   [**FWPM \_ FIELD0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_field0)
-   [**FWPM \_ FILTER0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_filter0)
-   [**FWPM \_ FILTER \_ CHANGE0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_filter_change0)
-   [**\_FWPM-FILTERBEDINGUNG0 \_**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_filter_condition0)
-   [**FWPM \_ FILTER \_ ENUM \_ TEMPLATE0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_filter_enum_template0)
-   [**\_ \_ FWPM-FILTERABONNEMENT0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_filter_subscription0)
-   [**FWPM \_ LAYER0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_layer0)
-   [**FWPM \_ LAYER \_ ENUM \_ TEMPLATE0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_layer_enum_template0)
-   [**FWPM \_ LAYER \_ STATISTICS0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_layer_statistics0)
-   FWPM \_ \_ NET-EREIGNIS:
    -   [**FWPM \_ NET \_ EVENT0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event0) (Windows Vista)
    -   [**FWPM \_ NET \_ EVENT1**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event1) (Windows 7)
    -   [**FWPM \_ NET \_ EVENT2**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event2) (Windows 8)
-   [**FWPM \_ \_ NET-EREIGNISFUNKTION \_ \_ ALLOW0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_capability_allow0)
-   [**FWPM \_ \_ NET-EREIGNISFUNKTION \_ \_ DROP0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_capability_drop0)
-   [**FWPM \_ \_ NET-EREIGNIS \_ CLASSIFY \_ ALLOW0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_classify_allow0)
-   ABLAGE VON FWPM \_ \_ NET-EREIGNISKLASSIFIZIERUNG: \_ \_
    -   [**FWPM \_ NET \_ EVENT \_ CLASSIFY \_ DROP0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_classify_drop0) (Windows Vista)
    -   [**FWPM \_ NET \_ EVENT \_ CLASSIFY \_ DROP1**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_classify_drop1) (Windows 7 und höher)
    -   [**FWPM \_ NET \_ EVENT \_ CLASSIFY \_ DROP2**](/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_net_event_classify_drop2) (Windows 8)
-   [**FWPM \_ \_ NET-EREIGNIS \_ CLASSIFY \_ DROP \_ MAC0**](/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_net_event_classify_drop_mac0)
-   [**FWPM \_ NET \_ EVENT \_ ENUM \_ TEMPLATE0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_enum_template0)
-   FWPM \_ \_ NET-EREIGNISHEADER: \_
    -   [**FWPM \_ NET \_ EVENT \_ HEADER0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_header0) (Windows Vista)
    -   [**FWPM \_ NET \_ EVENT \_ HEADER1**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_header1) (Windows 7)
    -   [**FWPM \_ NET \_ EVENT \_ HEADER2**](/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_net_event_header2) (Windows 8)
-   FEHLER BEI FWPM \_ NET \_ EVENT \_ IKEEXT \_ \_ EM:
    -   [**FWPM \_ NET \_ EVENT \_ IKEEXT \_ EM \_ FAILURE0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_ikeext_em_failure0) (Windows Vista)
    -   [**FWPM \_ NET \_ EVENT \_ IKEEXT \_ EM \_ FAILURE1**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_ikeext_em_failure1) (Windows 7 und höher)
-   FEHLER BEI FWPM \_ \_ NET-EREIGNIS \_ IKEEXT \_ \_ MM:
    -   [**FWPM \_ NET \_ EVENT \_ IKEEXT \_ MM \_ FAILURE0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_ikeext_mm_failure0) (Windows Vista)
    -   [**FWPM \_ NET \_ EVENT \_ IKEEXT \_ MM \_ FAILURE1**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_ikeext_mm_failure1) (Windows 7 und höher)
-   [**FWPM \_ NET \_ EVENT \_ IKEEXT \_ QM \_ FAILURE0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_ikeext_qm_failure0)
-   [**FWPM \_ NET \_ EVENT \_ IPSEC \_ DOSP \_ DROP0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_ipsec_dosp_drop0)
-   [**FWPM \_ NET \_ EVENT \_ IPSEC \_ KERNEL \_ DROP0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_ipsec_kernel_drop0)
-   [**FWPM \_ \_ \_ NET-EREIGNISABONNEMENT0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_subscription0)
-   [**\_FWPM-ANBIETER0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider0)
-   [**FWPM \_ PROVIDER \_ CHANGE0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider_change0)
-   \_FWPM-ANBIETERKONTEXT: \_
    -   [**FWPM \_ PROVIDER \_ CONTEXT0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider_context0) (Windows Vista)
    -   [**FWPM \_ PROVIDER \_ CONTEXT1**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider_context1) (Windows 7)
    -   FWPM \_ PROVIDER \_ CONTEXT2 (Windows 8)
-   [**KONTEXTÄNDERUNG \_ DES FWPM-ANBIETERKONTEXTS0 \_ \_**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider_context_change0)
-   [**FWPM \_ PROVIDER \_ CONTEXT \_ ENUM \_ TEMPLATE0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider_context_enum_template0)
-   [**\_ \_ \_ FWPM-ANBIETERKONTEXTABONNEMENT0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider_context_subscription0)
-   [**FWPM \_ PROVIDER \_ ENUM \_ TEMPLATE0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider_enum_template0)
-   [**\_ \_ FWPM-ANBIETERABONNEMENT0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider_subscription0)
-   [**FWPM \_ SESSION0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_session0)
-   [**FWPM \_ SESSION \_ ENUM \_ TEMPLATE0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_session_enum_template0)
-   [**FWPM \_ STATISTICS0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_statistics0)
-   [**\_FWPM-UNTEREBENE0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_sublayer0)
-   [**FWPM \_ SUBLAYER \_ CHANGE0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_sublayer_change0)
-   [**\_FWPM-UNTERSCHICHT-ENUMERATIONSVORLAGE0 \_ \_**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_sublayer_enum_template0)
-   [**\_ \_ FWPM-UNTEREBENENABONNEMENT0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_sublayer_subscription0)
-   [**\_ \_ FWPM-SYSTEMPORTS0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_system_ports0)
-   [**\_FWPM-SYSTEMPORTS \_ \_ NACH \_ TYP0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_system_ports_by_type0)
-   [**FWPM \_ VSWITCH \_ EVENT0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_vswitch_event0)
-   [**FWPM \_ \_ VSWITCH-EREIGNISABONNEMENT0 \_**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_vswitch_event_subscription0)

Gemeinsame Strukturen

-   [**FWP \_ BYTE \_ ARRAY6**](/windows/win32/api/fwptypes/ns-fwptypes-fwp_byte_array6)
-   [**FWP \_ BYTE \_ ARRAY16**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwp_byte_array16)
-   [**\_FWP-BYTE-BLOB \_**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwp_byte_blob)
-   [**\_ \_ FWP-BEDINGUNGSWERT0**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwp_condition_value0)
-   [**FWP \_ RANGE0**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwp_range0)
-   [**\_FWP-ÜBEREINSTIMMUNGSTYP \_**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_match_type)
-   [**FWP \_ \_ V4-ADDR \_ UND \_ -MASKE**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwp_v4_addr_and_mask)
-   [**FWP \_ \_ V6-ADDR \_ UND \_ -MASKE**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwp_v6_addr_and_mask)
-   [**FWP \_ VALUE0**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwp_value0)

IKE/AuthIP-Strukturen

-   \_IKEEXT-AUTHENTIFIZIERUNGSMETHODE: \_
    -   [**IKEEXT \_ AUTHENTICATION \_ METHOD0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_authentication_method0) (Windows Vista)
    -   [**IKEEXT \_ AUTHENTICATION \_ METHOD1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_authentication_method1) (Windows 7)
    -   [**IKEEXT \_ AUTHENTICATION \_ METHOD2**](/windows/win32/api/iketypes/ns-iketypes-ikeext_authentication_method2) (Windows 8)
-   [**IKEEXT \_ CERT \_ EKUS0**](/windows/win32/api/iketypes/ns-iketypes-ikeext_cert_ekus0)
-   [**\_IKEEXT-ZERTIFIKATNAME0 \_**](/windows/win32/api/iketypes/ns-iketypes-ikeext_cert_name0)
-   [**IKEEXT \_ CERT \_ ROOT \_ CONFIG0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_cert_root_config0)
-   \_IKEEXT-ZERTIFIKATAUTHENTIFIZIERUNG: \_
    -   [**IKEEXT \_ CERTIFICATE \_ AUTHENTICATION0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_certificate_authentication0) (Windows Vista)
    -   [**IKEEXT \_ CERTIFICATE \_ AUTHENTICATION1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_certificate_authentication1) (Windows 7)
    -   [**IKEEXT \_ CERTIFICATE \_ AUTHENTICATION2**](/windows/win32/api/iketypes/ns-iketypes-ikeext_certificate_authentication2) (Windows 8)
-   IKEEXT \_ CERTIFICATE CREDENTIAL \_ (IKEEXT-ZERTIFIKATANMELDEINFORMATIONEN):
    -   [**IKEEXT \_ CERTIFICATE \_ CREDENTIAL0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_certificate_credential0) (Windows Vista)
    -   [**IKEEXT \_ CERTIFICATE \_ CREDENTIAL1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_certificate_credential1) (Windows 7 und höher)
-   [**IKEEXT \_ CERTIFICATE \_ CRITERIA0**](/windows/win32/api/iketypes/ns-iketypes-ikeext_certificate_criteria0)
-   [**IKEEXT \_ CIPHER \_ ALGORITHM0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_cipher_algorithm0)
-   ALLGEMEINE \_ \_ IKEEXT-STATISTIKEN:
    -   [**IKEEXT \_ COMMON \_ STATISTICS0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_common_statistics0) (Windows Vista)
    -   [**IKEEXT \_ COMMON \_ STATISTICS1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_common_statistics1) (Windows 7 und höher)
-   [**IKEEXT \_ COOKIE \_ PAIR0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_cookie_pair0)
-   \_IKEEXT-ANMELDEINFORMATIONEN:
    -   [**IKEEXT \_ CREDENTIAL0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_credential0) (Windows Vista)
    -   [**IKEEXT \_ CREDENTIAL1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_credential1) (Windows 7 und höher)
-   IKEEXT \_ CREDENTIAL PAIR (IKEEXT-ANMELDEINFORMATIONSPAAR): \_
    -   [**IKEEXT \_ CREDENTIAL \_ PAIR0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_credential_pair0) (Windows Vista)
    -   [**IKEEXT \_ CREDENTIAL \_ PAIR1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_credential_pair1) (Windows 7 und höher)
-   \_IKEEXT-ANMELDEINFORMATIONEN:
    -   [**IKEEXT \_ CREDENTIALS0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_credentials0) (Windows Vista)
    -   [**IKEEXT \_ CREDENTIALS1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_credentials1) (Windows 7 und höher)
-   [**IKEEXT \_ EAP \_ AUTHENTICATION0**](/windows/win32/api/iketypes/ns-iketypes-ikeext_eap_authentication0)
-   IKEEXT \_ \_ EM-RICHTLINIE:
    -   [**IKEEXT \_ EM \_ POLICY0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_em_policy0) (Windows Vista)
    -   [**IKEEXT \_ EM \_ POLICY1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_em_policy1) (Windows 7)
    -   [**IKEEXT \_ EM \_ POLICY2**](/windows/win32/api/iketypes/ns-iketypes-ikeext_em_policy2) (Windows 8)
-   [**IKEEXT \_ INTEGRITY \_ ALGORITHM0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_integrity_algorithm0)
-   IKEEXT \_ \_ IP-VERSIONSSPEZIFISCHE \_ \_ ALLGEMEINE \_ STATISTIKEN:
    -   [**IKEEXT \_ \_IP-VERSIONSPEZIFISCH \_ COMMON \_ \_ STATISTICS0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_ip_version_specific_common_statistics0) (Windows Vista)
    -   [**IKEEXT \_ SPEZIFISCHE \_ IP-VERSION \_ COMMON \_ \_ STATISTICS1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_ip_version_specific_common_statistics1) (Windows 7 und höher)
-   IKEEXT \_ \_ IP-VERSIONSSPEZIFISCHE \_ \_ \_ KEYMODULE-STATISTIKEN:
    -   [**IKEEXT \_ \_IP-VERSIONSPEZIFISCH \_ \_ KEYMODULE \_ STATISTICS0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_ip_version_specific_keymodule_statistics0) (Windows Vista)
    -   [**IKEEXT \_ \_IP-VERSIONSPEZIFISCH \_ \_ KEYMODULE \_ STATISTICS1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_ip_version_specific_keymodule_statistics1) (Windows 7 und höher)
-   [**IKEEXT \_ IPV6 \_ CGA \_ AUTHENTICATION0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_ipv6_cga_authentication0)
-   IKEEXT \_ KEYMODULE \_ STATISTICS:
    -   [**IKEEXT \_ KERBEROS \_ AUTHENTICATION0**](/windows/win32/api/iketypes/ns-iketypes-ikeext_kerberos_authentication0) (Windows Vista und Windows 7)
    -   [**IKEEXT \_ KERBEROS \_ AUTHENTICATION1**](/windows/win32/api/iketypes/ns-iketypes-ikeext_kerberos_authentication1) (Windows 8)
-   -   IKEEXT \_ KEYMODULE \_ STATISTICS:
    -   [**IKEEXT \_ KEYMODULE \_ STATISTICS0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_keymodule_statistics0) (Windows Vista)
    -   [**IKEEXT \_ KEYMODULE \_ STATISTICS1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_keymodule_statistics1) (Windows 7 und höher)
-   [**IKEEXT \_ NAME \_ CREDENTIAL0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_name_credential0)
-   [**IKEEXT \_ NTLM \_ V2 \_ AUTHENTICATION0**](/windows/win32/api/iketypes/ns-iketypes-ikeext_ntlm_v2_authentication0)
-   \_IKEEXT-RICHTLINIE:
    -   [**IKEEXT \_ POLICY0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_policy0) (Windows Vista)
    -   [**IKEEXT \_ POLICY1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_policy1) (Windows 7)
    -   [**IKEEXT \_ POLICY2**](/windows/win32/api/iketypes/ns-iketypes-ikeext_policy2) (Windows 8)
-   AUTHENTIFIZIERUNG \_ MIT VORINSTALLIERTEM \_ IKEEXT-SCHLÜSSEL: \_
    -   [**IKEEXT \_ VORINSTALLIERTE \_ \_ SCHLÜSSELAUTHENTIFIZIERUNG0**](/windows/win32/api/iketypes/ns-iketypes-ikeext_preshared_key_authentication0) (Windows Vista)
    -   [**IKEEXT \_ PRESHARED \_ KEY \_ AUTHENTICATION1**](/windows/win32/api/iketypes/ns-iketypes-ikeext_preshared_key_authentication1) (Windows 7 und höher)
-   [**IKEEXT \_ PROPOSAL0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_proposal0)
-   [**RESERVIERTE \_ \_ IKEEXT-AUTHENTIFIZIERUNG0**](/windows/win32/api/iketypes/ns-iketypes-ikeext_reserved_authentication0)
-   DETAILS ZUR \_ IKEEXT-SA: \_
    -   [**IKEEXT \_ SA \_ DETAILS0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_sa_details0) (Windows Vista)
    -   [**IKEEXT \_ SA \_ DETAILS1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_sa_details1) (Windows 7 und höher)
-   [**IKEEXT \_ SA \_ ENUM \_ TEMPLATE0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_sa_enum_template0)
-   IKEEXT \_ STATISTICS:
    -   [**IKEEXT \_ STATISTICS0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_statistics0) (Windows Vista)
    -   [**IKEEXT \_ STATISTICS1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_statistics1) (Windows 7 und höher)
-   [**IKEEXT \_ TRAFFIC0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_traffic0)

IPsec-Strukturen

-   [**\_ \_ IPSEC-ADRESSINFORMATIONEN0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_address_info0)
-   IPSEC \_ AGGREGATE DROP PACKET STATISTICS (IPSEC-AGGREGIERTE DROP \_ \_ \_ PACKET-STATISTIK):
    -   [**IPSEC \_ AGGREGATE \_ DROP \_ PACKET \_ STATISTICS0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_aggregate_drop_packet_statistics0) (Windows Vista)
    -   [**IPSEC \_ AGGREGATE \_ DROP \_ PACKET \_ STATISTICS1**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_aggregate_drop_packet_statistics1) (Windows 7 und höher)
-   [**IPSEC \_ AGGREGATE \_ SA \_ STATISTICS0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_aggregate_sa_statistics0)
-   [**IPSEC \_ AH \_ DROP \_ PACKET \_ STATISTICS0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_ah_drop_packet_statistics0)
-   [**\_IPSEC-AUTHENTIFIZIERUNG \_ UND \_ \_ VERSCHLÜSSELUNGSTRANSFORMATION0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_auth_and_cipher_transform0)
-   [**IPSEC \_ AUTH \_ TRANSFORM0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_auth_transform0)
-   [**IPSEC \_ AUTH \_ TRANSFORM \_ ID0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_auth_transform_id0)
-   [**IPSEC \_ CIPHER \_ TRANSFORM0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_cipher_transform0)
-   [**IPSEC \_ CIPHER \_ TRANSFORM \_ ID0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_cipher_transform_id0)
-   [**\_ \_ IPSEC-DOSP-OPTIONEN0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_dosp_options0)
-   [**IPSEC \_ DOSP \_ STATE0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_dosp_state0)
-   [**IPSEC \_ DOSP \_ STATE \_ ENUM \_ TEMPLATE0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_dosp_state_enum_template0)
-   [**IPSEC \_ DOSP \_ STATISTICS0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_dosp_statistics0)
-   [**IPSEC \_ ESP \_ DROP \_ PACKET \_ STATISTICS0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_esp_drop_packet_statistics0)
-   IPSEC \_ GETSPI:
    -   [**IPSEC \_ GETSPI0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_getspi0) (Windows Vista)
    -   [**IPSEC \_ GETSPI1**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_getspi1) (Windows 7 und höher)
-   [**IPSEC \_ ID0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_id0)
-   [**\_ \_ IPSEC-SCHLÜSSEL-MANAGER0**](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_key_manager0)
-   [**IPSEC \_ KEY \_ MANAGER \_ CALLBACKS0**](/windows/desktop/api/fwpmu/ns-fwpmu-ipsec_key_manager_callbacks0)
-   \_ \_ IPSEC-SCHLÜSSELRICHTLINIE:
    -   [**IPSEC \_ KEYING \_ POLICY0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_keying_policy0) (Windows Vista und Windows 7)
    -   [**IPSEC \_ KEYING \_ POLICY1**](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_keying_policy1) (Windows 8)
-   [**IPSEC \_ KEYMODULE \_ STATE0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_keymodule_state0)
-   [**\_IPSEC-VORSCHLAG0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_proposal0)
-   [**IPSEC \_ SA0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa0)
-   [**IPSEC \_ \_ SA-AUTHENTIFIZIERUNG \_ UND \_ \_ VERSCHLÜSSELUNGSINFORMATIONEN0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_auth_and_cipher_information0)
-   [**IPSEC \_ SA \_ AUTH \_ INFORMATION0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_auth_information0)
-   IPSEC \_ SA \_ BUNDLE:
    -   [**IPSEC \_ SA \_ BUNDLE0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_bundle0) (Windows Vista)
    -   [**IPSEC \_ SA \_ BUNDLE1**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_bundle1) (Windows 7 und höher)
-   [**IPSEC \_ SA \_ CIPHER \_ INFORMATION0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_cipher_information0)
-   \_IPSEC-SA-KONTEXT: \_
    -   [**IPSEC \_ SA \_ CONTEXT0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_context0) (Windows Vista)
    -   [**IPSEC \_ SA \_ CONTEXT1**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_context1) (Windows 7 und höher)
-   [**IPSEC \_ SA \_ CONTEXT \_ CHANGE0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_context_change0)
-   [**IPSEC \_ SA \_ CONTEXT ENUM \_ TEMPLATE0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_context_enum_template0)
-   [**IPSEC \_ SA \_ CONTEXT \_ SUBSCRIPTION0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_context_subscription0)
-   \_IPSEC-SA-DETAILS: \_
    -   [**IPSEC \_ SA \_ DETAILS0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_details0) (Windows Vista)
    -   [**IPSEC \_ SA \_ DETAILS1**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_details1) (Windows 7 und höher)
-   [**IPSEC \_ SA \_ ENUM \_ TEMPLATE0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_enum_template0)
-   [**IPSEC \_ SA \_ IDLE \_ TIMEOUT0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_idle_timeout0)
-   [**IPSEC \_ SA \_ LIFETIME0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_lifetime0)
-   [**IPSEC \_ SA \_ TRANSFORM0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_transform0)
-   \_IPSEC-STATISTIK:
    -   [**IPSEC \_ STATISTICS0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_statistics0) (Windows Vista)
    -   [**IPSEC \_ STATISTICS1**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_statistics1) (Windows 7 und höher)
-   [**IPSEC \_ TOKEN0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_token0)
-   \_IPSEC-DATENVERKEHR:
    -   [**IPSEC \_ TRAFFIC0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_traffic0) (Windows Vista)
    -   [**IPSEC \_ TRAFFIC1**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_traffic1) (Windows 7 und höher)
-   \_ \_ IPSEC-DATENVERKEHRSSTATISTIKEN:
    -   [**IPSEC \_ TRAFFIC \_ STATISTICS0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_traffic_statistics0) (Windows Vista)
    -   [**IPSEC \_ TRAFFIC \_ STATISTICS1**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_traffic_statistics1) (Windows 7 und höher)
-   \_ \_ IPSEC-TRANSPORTRICHTLINIE:
    -   [**IPSEC \_ TRANSPORT \_ POLICY0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_transport_policy0) (Windows Vista)
    -   [**IPSEC \_ TRANSPORT \_ POLICY1**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_transport_policy1) (Windows 7)
    -   [**IPSEC \_ TRANSPORT \_ POLICY2**](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_transport_policy2) (Windows 8)
-   [**IPSEC \_ TUNNEL \_ ENDPOINT0**](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_tunnel_endpoint0)
-   \_ \_ IPSEC-TUNNELENDPUNKTE:
    -   [**IPSEC \_ TUNNEL \_ ENDPOINTS0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_tunnel_endpoints0) (Windows Vista)
    -   [**IPSEC \_ \_TUNNELENDPUNKTE1**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_tunnel_endpoints1) (Windows 7)
    -   [**IPSEC \_ TUNNEL \_ ENDPOINTS2**](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_tunnel_endpoints2) (Windows 8)
-   \_ \_ IPSEC-TUNNELRICHTLINIE:
    -   [**IPSEC \_ TUNNEL \_ POLICY0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_tunnel_policy0) (Windows Vista)
    -   [**IPSEC \_ TUNNEL \_ POLICY1**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_tunnel_policy1) (Windows 7)
    -   [**IPSEC \_ TUNNEL \_ POLICY2**](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_tunnel_policy2) (Windows 8)
-   [**IPSEC \_ V4 \_ \_ UDP-KAPSELUNG0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_v4_udp_encapsulation0)
-   [**IPSEC \_ VIRTUAL \_ IF \_ TUNNEL \_ INFO0**](/windows/win32/api/fwptypes/ns-fwptypes-ipsec_virtual_if_tunnel_info0)

 

 




