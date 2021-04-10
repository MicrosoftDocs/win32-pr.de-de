---
title: RPC-Strukturen
description: In diesem Abschnitt werden die Strukturen erläutert, die von Microsoft RPC definiert und verwendet werden.
ms.assetid: 8d2f31f6-21d3-402c-b84b-960a2d03ff40
keywords:
- Remote Prozedur Aufruf RPC, Referenz, Strukturen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b94d03209af8b14f87cd8b15929389b6eb524833
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729401"
---
# <a name="rpc-structures"></a>RPC-Strukturen

In diesem Abschnitt werden die Strukturen erläutert, die von Microsoft RPC definiert und verwendet werden.

-   [**NDR \_ sContext**](/previous-versions/aa374336(v=vs.80))
-   [**GUID**](/windows/win32/api/guiddef/ns-guiddef-guid)
-   [**Informationen zu NDR- \_ Benutzer \_ Mars Hall \_**](/windows/win32/api/Rpcndr/ns-rpcndr-ndr_user_marshal_info)
-   [**NDR- \_ Benutzer \_ Mars Hall \_ Info \_ Level1**](/windows/win32/api/Rpcndr/ns-rpcndr-ndr_user_marshal_info_level1)
-   [**Informationen zur asynchronen RPC- \_ \_ Benachrichtigung \_**](/windows/win32/api/Rpcasync/ns-rpcasync-rpc_async_notification_info)
-   [**asynchroner RPC- \_ \_ Status**](/windows/win32/api/Rpcasync/ns-rpcasync-rpc_async_state)
-   [**RPC- \_ Bindungs \_ handle- \_ Optionen \_ v1**](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_binding_handle_options_v1)
-   [**RPC- \_ Bindungs \_ handle- \_ Sicherheit \_ v1**](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_binding_handle_security_v1_a)
-   [**RPC- \_ Bindungs \_ handle- \_ Vorlage \_ v1**](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_binding_handle_template_v1_a)
-   [**RPC- \_ Bindungs \_ Vektor**](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_binding_vector)
-   [**RPC-C-opt-Cookie-Authentifizierungs \_ \_ \_ \_ \_ Deskriptor**](/windows/win32/api/Rpcdcep/ns-rpcdcep-rpc_c_opt_cookie_auth_descriptor)
-   [**RPC- \_ Aufruf \_ Attribute \_ v1**](/windows/win32/api/rpcasync/ns-rpcasync-rpc_call_attributes_v1_a)
-   [**RPC- \_ Aufruf \_ Attribute \_ v2**](/windows/win32/api/rpcasync/ns-rpcasync-rpc_call_attributes_v2_a)
-   [**RPC- \_ Aufruf- \_ lokale \_ Adresse \_ v1**](/windows/win32/api/Rpcasync/ns-rpcasync-rpc_call_local_address_v1)
-   [**RPC- \_ Client \_ Schnittstelle**](/windows/win32/api/RpcdceP/ns-rpcdcep-rpc_client_interface)
-   [**RPC-Verteilungs \_ \_ Tabelle**](/windows/win32/api/RpcdceP/ns-rpcdcep-rpc_dispatch_table)
-   [**RPC- \_ EE- \_ info-Parameter \_**](/windows/win32/api/rpcasync/ns-rpcasync-rpc_ee_info_param)
-   [**RPC- \_ Endpunkt \_ Vorlage**](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_endpoint_template)
-   [**RPC-Fehler-Aufzählungs \_ \_ \_ handle**](/windows/win32/api/rpcasync/ns-rpcasync-rpc_error_enum_handle)
-   [**Erweiterte RPC- \_ \_ Fehler \_ Informationen**](/windows/win32/api/rpcasync/ns-rpcasync-rpc_extended_error_info)
-   [**RPC- \_ http- \_ Transport \_ Anmelde Informationen**](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_http_transport_credentials_a)
-   [**RPC- \_ http- \_ Transport Anmelde Informationen \_ \_ v2**](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_http_transport_credentials_v2_a)
-   [**RPC- \_ http- \_ Transport Anmelde Informationen \_ \_ v3**](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_http_transport_credentials_v3_a)
-   [**RPC- \_ if- \_ ID**](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_if_id)
-   [**RPC- \_ if- \_ ID- \_ Vektor**](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_if_id_vector)
-   [**RPC- \_ Schnittstellen \_ Vorlage**](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_interface_template)
-   [**RPC- \_ Richtlinie**](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_policy)
-   [**RPC- \_ protabq- \_ Vektor**](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_protseq_vector)
-   [**RPC- \_ Sicherheits- \_ QoS**](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_security_qos)
-   [**RPC- \_ Sicherheits- \_ QoS \_ v2**](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_security_qos_v2_a)
-   [**RPC- \_ Sicherheits- \_ QoS \_ v3**](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_security_qos_v3_a)
-   [**RPC- \_ Sicherheits- \_ QoS \_ v4**](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_security_qos_v4_a)
-   [**RPC- \_ Sicherheits- \_ QoS \_ V5**](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_security_qos_v5_a)
-   [**RPC- \_ Statistik \_ Vektor**](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_stats_vector)
-   [**SEK \_ . WinNT-Authentifizierungs \_ \_ Identität**](/windows/win32/api/Rpcdce/ns-rpcdce-sec_winnt_auth_identity_a)
-   [**UUID**](./rpcdce/ns-rpcdce-uuid.md)
-   [**UUID- \_ Vektor**](/windows/win32/api/rpcdce/ns-rpcdce-uuid_vector)

 

 