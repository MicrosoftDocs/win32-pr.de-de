---
title: RPC-Strukturen
description: In diesem Abschnitt werden die von Microsoft RPC definierten und verwendeten Strukturen erläutert.
ms.assetid: 8d2f31f6-21d3-402c-b84b-960a2d03ff40
keywords:
- Remoteprozeduraufruf RPC , Referenz, Strukturen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c59552f775b56519620e46c610bef234fba488d4d6e0a7dfe7d4266e7ae2c50e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120018211"
---
# <a name="rpc-structures"></a>RPC-Strukturen

In diesem Abschnitt werden die von Microsoft RPC definierten und verwendeten Strukturen erläutert.

-   [**NDR \_ SCONTEXT**](/previous-versions/aa374336(v=vs.80))
-   [**GUID**](/windows/win32/api/guiddef/ns-guiddef-guid)
-   [**MARSHALLINFORMATIONEN \_ FÜR NDR-BENUTZER \_ \_**](/windows/win32/api/Rpcndr/ns-rpcndr-ndr_user_marshal_info)
-   [**NDR \_ USER \_ MARSHAL \_ INFO \_ LEVEL1**](/windows/win32/api/Rpcndr/ns-rpcndr-ndr_user_marshal_info_level1)
-   [**RPC \_ ASYNC \_ NOTIFICATION \_ INFO**](/windows/win32/api/Rpcasync/ns-rpcasync-rpc_async_notification_info)
-   [**RPC \_ ASYNC \_ STATE**](/windows/win32/api/Rpcasync/ns-rpcasync-rpc_async_state)
-   [**\_ \_ RPC-BINDUNGSHANDLEOPTIONEN \_ \_ V1**](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_binding_handle_options_v1)
-   [**\_ \_ RPC-BINDUNGSHANDLESICHERHEIT \_ \_ V1**](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_binding_handle_security_v1_a)
-   [**\_ \_ RPC-BINDUNGSHANDLEVORLAGE \_ \_ V1**](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_binding_handle_template_v1_a)
-   [**\_ \_ RPC-BINDUNGSVEKTOR**](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_binding_vector)
-   [**RPC \_ C \_ OPT \_ COOKIE \_ AUTH \_ DESCRIPTOR**](/windows/win32/api/Rpcdcep/ns-rpcdcep-rpc_c_opt_cookie_auth_descriptor)
-   [**\_RPC-AUFRUFATTRIBUTE \_ \_ V1**](/windows/win32/api/rpcasync/ns-rpcasync-rpc_call_attributes_v1_a)
-   [**\_RPC-AUFRUFATTRIBUTE \_ \_ V2**](/windows/win32/api/rpcasync/ns-rpcasync-rpc_call_attributes_v2_a)
-   [**RPC \_ CALL \_ LOCAL \_ ADDRESS \_ V1**](/windows/win32/api/Rpcasync/ns-rpcasync-rpc_call_local_address_v1)
-   [**\_ \_ RPC-CLIENTSCHNITTSTELLE**](/windows/win32/api/RpcdceP/ns-rpcdcep-rpc_client_interface)
-   [**RPC \_ DISPATCH \_ TABLE**](/windows/win32/api/RpcdceP/ns-rpcdcep-rpc_dispatch_table)
-   [**RPC \_ EE \_ INFO \_ PARAM**](/windows/win32/api/rpcasync/ns-rpcasync-rpc_ee_info_param)
-   [**\_ \_ RPC-ENDPUNKTVORLAGE**](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_endpoint_template)
-   [**RPC \_ ERROR \_ ENUM \_ HANDLE**](/windows/win32/api/rpcasync/ns-rpcasync-rpc_error_enum_handle)
-   [**RPC \_ EXTENDED \_ ERROR \_ INFO**](/windows/win32/api/rpcasync/ns-rpcasync-rpc_extended_error_info)
-   [**\_ \_ \_ RPC-HTTP-TRANSPORTANMELDEINFORMATIONEN**](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_http_transport_credentials_a)
-   [**RPC \_ HTTP \_ TRANSPORT \_ CREDENTIALS \_ V2**](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_http_transport_credentials_v2_a)
-   [**RPC \_ HTTP \_ TRANSPORT \_ CREDENTIALS \_ V3**](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_http_transport_credentials_v3_a)
-   [**RPC \_ \_ IF-ID**](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_if_id)
-   [**RPC \_ IF \_ ID \_ VECTOR**](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_if_id_vector)
-   [**\_ \_ RPC-SCHNITTSTELLENVORLAGE**](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_interface_template)
-   [**\_RPC-RICHTLINIE**](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_policy)
-   [**RPC \_ PROTSEQ \_ VECTOR**](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_protseq_vector)
-   [**\_ \_ RPC-SICHERHEITS-QOS**](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_security_qos)
-   [**RPC \_ SECURITY \_ QOS \_ V2**](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_security_qos_v2_a)
-   [**RPC \_ SECURITY \_ QOS \_ V3**](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_security_qos_v3_a)
-   [**RPC \_ SECURITY \_ QOS \_ V4**](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_security_qos_v4_a)
-   [**RPC \_ SECURITY \_ QOS \_ V5**](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_security_qos_v5_a)
-   [**\_ \_ RPC-STATISTIKVEKTOR**](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_stats_vector)
-   [**\_SEC \_ WINNT-AUTHENTIFIZIERUNGSIDENTITÄT \_**](/windows/win32/api/Rpcdce/ns-rpcdce-sec_winnt_auth_identity_a)
-   [**UUID**](./rpcdce/ns-rpcdce-uuid.md)
-   [**UUID \_ VECTOR**](/windows/win32/api/rpcdce/ns-rpcdce-uuid_vector)

 

 