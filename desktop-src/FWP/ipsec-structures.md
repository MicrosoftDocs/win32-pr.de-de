---
title: IPSec-Strukturen
description: IPSec-Strukturen
ms.assetid: FF1FE626-B9F9-4091-8B82-BEB9D229B93D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd268fda1ee98ec80d20d8c75625d4f68526c741
ms.sourcegitcommit: cb844c9ab17577ce171fd7b03add668645867bc7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/27/2020
ms.locfileid: "106339261"
---
# <a name="ipsec-structures"></a>IPSec-Strukturen

## <a name="in-this-section"></a>In diesem Abschnitt

-   [**IPSec- \_ Adresse \_ INFO0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_address_info0)
-   [**IPSec- \_ Aggregate \_ Drop \_ Packet \_ STATISTICS0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_aggregate_drop_packet_statistics0)
-   [**IPSec- \_ Aggregate \_ Drop \_ Packet \_ STATISTICS1**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_aggregate_drop_packet_statistics1)
-   [**IPSec- \_ Aggregat- \_ sa \_ STATISTICS0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_aggregate_sa_statistics0)
-   [**IPSec \_ AH \_ Drop \_ Packet \_ STATISTICS0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_ah_drop_packet_statistics0)
-   [**IPSec \_ -Authentifizierung \_ und \_ Chiffre \_ TRANSFORM0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_auth_and_cipher_transform0)
-   [**IPSec-Authentifizierung \_ \_ TRANSFORM0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_auth_transform0)
-   [**IPSec-Authentifizierung \_ \_ \_ ID0 Transformation**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_auth_transform_id0)
-   [**IPSec- \_ Chiffre \_ TRANSFORM0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_cipher_transform0)
-   [**IPSec- \_ Chiffre \_ Transformation \_ ID0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_cipher_transform_id0)
-   [**IPSec- \_ DoSP \_ OPTIONS0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_dosp_options0)
-   [**IPSec- \_ DoSP \_ STATE0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_dosp_state0)
-   [**IPSec- \_ DoSP State-Aufzählung \_ \_ \_ TEMPLATE0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_dosp_state_enum_template0)
-   [**IPSec- \_ DoSP \_ STATISTICS0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_dosp_statistics0)
-   [**IPSec \_ ESP \_ Drop \_ Packet \_ STATISTICS0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_esp_drop_packet_statistics0)
-   [**IPSec- \_ GETSPI0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_getspi0)
-   [**IPSec- \_ GETSPI1**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_getspi1)
-   [**IPSec- \_ ID0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_id0)
-   [**IPSec- \_ Schlüssel \_ MANAGER0**](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_key_manager0)
-   [**IPSec- \_ Schlüssel- \_ Manager \_ CALLBACKS0**](/windows/desktop/api/fwpmu/ns-fwpmu-ipsec_key_manager_callbacks0)
-   [**IPSec-Schlüssel \_ \_ POLICY0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_keying_policy0)
-   [**IPSec-Schlüssel \_ \_ Richtlinie1**](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_keying_policy1)
-   [**IPSec- \_ keymodule \_ STATE0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_keymodule_state0)
-   [**IPSec- \_ PROPOSAL0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_proposal0)
-   [**IPSec- \_ sa0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa0)
-   [**IPSec \_ \_ \_ -sa-Authentifizierung und \_ Chiffre \_ INFORMATION0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_auth_and_cipher_information0)
-   [**IPSec-SA-Authentifizierung \_ \_ \_ INFORMATION0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_auth_information0)
-   [**IPSec- \_ sa \_ BUNDLE0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_bundle0)
-   [**IPSec- \_ sa \_ BUNDLE1**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_bundle1)
-   [**IPSec- \_ sa- \_ Chiffre \_ INFORMATION0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_cipher_information0)
-   [**IPSec- \_ sa \_ CONTEXT0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_context0)
-   [**IPSec- \_ sa \_ CONTEXT1**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_context1)
-   [**IPSec- \_ sa- \_ Kontext \_ CHANGE0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_context_change0)
-   [**IPSec-SA-Kontext-Aufzählung \_ \_ \_ \_ TEMPLATE0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_context_enum_template0)
-   [**IPSec- \_ sa- \_ Kontext \_ SUBSCRIPTION0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_context_subscription0)
-   [**IPSec- \_ sa \_ DETAILS0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_details0)
-   [**IPSec- \_ sa \_ DETAILS1**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_details1)
-   [**IPSec-SA-Aufzählung \_ \_ \_ TEMPLATE0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_enum_template0)
-   [**IPSec- \_ sa im \_ Leerlauf \_ TIMEOUT0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_idle_timeout0)
-   [**IPSec- \_ sa \_ LIFETIME0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_lifetime0)
-   [**IPSec- \_ STATISTICS0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_statistics0)
-   [**IPSec- \_ STATISTICS1**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_statistics1)
-   [**IPSec- \_ sa \_ TRANSFORM0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_transform0)
-   [**IPSec- \_ TOKEN0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_token0)
-   [**IPSec- \_ TRAFFIC0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_traffic0)
-   [**IPSec- \_ TRAFFIC1**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_traffic1)
-   [**IPSec- \_ Datenverkehr \_ STATISTICS0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_traffic_statistics0)
-   [**IPSec- \_ Datenverkehr \_ STATISTICS1**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_traffic_statistics1)
-   [**IPSec- \_ Transport \_ POLICY0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_transport_policy0)
-   [**IPSec- \_ Transport \_ Richtlinie1**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_transport_policy1)
-   [**IPSec- \_ Transport \_ POLICY2**](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_transport_policy2)
-   [**IPSec- \_ Tunnel \_ ENDPOINT0**](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_tunnel_endpoint0)
-   [**IPSec- \_ Tunnel \_ ENDPOINTS0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_tunnel_endpoints0)
-   [**IPSec- \_ Tunnel \_ ENDPOINTS1**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_tunnel_endpoints1)
-   [**IPSec- \_ Tunnel \_ ENDPOINTS2**](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_tunnel_endpoints2)
-   [**IPSec- \_ Tunnel \_ POLICY0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_tunnel_policy0)
-   [**IPSec- \_ Tunnel \_ Richtlinie1**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_tunnel_policy1)
-   [**IPSec- \_ Tunnel \_ POLICY2**](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_tunnel_policy2)
-   [**IPSec \_ V4- \_ UDP- \_ ENCAPSULATION0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_v4_udp_encapsulation0)
-   [**IPSec \_ Virtual \_ if \_ Tunnel \_ INFO0**](/windows/win32/api/fwptypes/ns-fwptypes-ipsec_virtual_if_tunnel_info0)

 

 




