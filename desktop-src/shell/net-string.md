---
description: Stellen Sie Netzwerkadresstypen dar. Verwenden Sie eine oder mehrere (als bitweise Kombination) der folgenden Konstanten, um eine Netzwerkadressmaske für die Verwendung mit dem Makro NetAddr \_ SetAllowType zu erstellen.
title: NET_STRING (Iphlpapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 4144dac9-772c-49cb-b924-e852fb4c81c7
api_name:
- NET_STRING_IPV4_ADDRESS
- NET_STRING_IPV4_SERVICE
- NET_STRING_IPV4_NETWORK
- NET_STRING_IPV6_ADDRESS
- NET_STRING_IPV6_ADDRESS_NO_SCOPE
- NET_STRING_IPV6_SERVICE
- NET_STRING_IPV6_SERVICE_NO_SCOPE
- NET_STRING_IPV6_NETWORK
- NET_STRING_NAMED_ADDRESS
- NET_STRING_NAMED_SERVICE
- NET_STRING_IP_ADDRESS
- NET_STRING_IP_ADDRESS_NO_SCOPE
- NET_STRING_IP_SERVICE
- NET_STRING_IP_SERVICE_NO_SCOPE
- NET_STRING_IP_NETWORK
- NET_STRING_ANY_ADDRESS
- NET_STRING_ANY_ADDRESS_NO_SCOPE
- NET_STRING_ANY_SERVICE
- NET_STRING_ANY_SERVICE_NO_SCOPE
api_type:
- HeaderDef
api_location:
- Iphlpapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: a7d1a09e6165e77ee5419da47419a65e3995ce0ffedb8a6fb71f01fb9c63dde5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120111220"
---
# <a name="net_string"></a>NET \_ STRING

Stellen Sie Netzwerkadresstypen dar. Verwenden Sie eine oder mehrere (als bitweise Kombination) der folgenden Konstanten, um eine Netzwerkadressmaske für die Verwendung mit dem [**Makro NetAddr \_ SetAllowType**](/windows/desktop/api/Shellapi/nf-shellapi-netaddr_setallowtype)zu erstellen.



| Konstante                                                                                                                                                                                                                   | Beschreibung                                                                                                                                                                    |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="NET_STRING_IPV4_ADDRESS"></span><span id="net_string_ipv4_address"></span><dl> <dt>**NET \_ STRING \_ IPV4 \_ ADDRESS**</dt> </dl>                              | Die Zeichenfolge identifiziert einen IPv4-Host/Router mithilfe einer Literaladresse (Port oder Präfix nicht zulässig).<br/>                                                                       |
| <span id="NET_STRING_IPV4_SERVICE"></span><span id="net_string_ipv4_service"></span><dl> <dt>**NET \_ STRING \_ IPV4-DIENST \_**</dt> </dl>                              | Die Zeichenfolge identifiziert einen IPv4-Dienst mithilfe einer Literaladresse (Port erforderlich, Präfix nicht zulässig).<br/>                                                                    |
| <span id="NET_STRING_IPV4_NETWORK"></span><span id="net_string_ipv4_network"></span><dl> <dt>**NET \_ STRING \_ IPV4 \_ NETWORK**</dt> </dl>                              | Die Zeichenfolge identifiziert ein IPv4-Netzwerk (Präfix erforderlich; Port nicht zulässig).<br/>                                                                                          |
| <span id="NET_STRING_IPV6_ADDRESS"></span><span id="net_string_ipv6_address"></span><dl> <dt>**NET \_ STRING \_ IPV6 \_ ADDRESS**</dt> </dl>                              | Die Zeichenfolge identifiziert einen IPv6-Host/Router mithilfe einer Literaladresse (Port oder Präfix nicht zulässig; bereichs-id zulässig).<br/>                                                     |
| <span id="NET_STRING_IPV6_ADDRESS_NO_SCOPE"></span><span id="net_string_ipv6_address_no_scope"></span><dl> <dt>**NET \_ STRING \_ IPV6 \_ ADDRESS \_ NO \_ SCOPE**</dt> </dl> | Die Zeichenfolge identifiziert einen IPv6-Host/Router mithilfe einer Literaladresse, bei der der Schnittstellenkontext bereits bekannt ist (Port oder Präfix nicht zulässig; Bereichs-ID nicht zulässig).<br/>    |
| <span id="NET_STRING_IPV6_SERVICE"></span><span id="net_string_ipv6_service"></span><dl> <dt>**NET \_ STRING \_ IPV6-DIENST \_**</dt> </dl>                              | Die Zeichenfolge identifiziert einen IPv6-Dienst mithilfe einer Literaladresse (Port erforderlich; Präfix nicht zulässig; Bereichs-ID zulässig).<br/>                                                  |
| <span id="NET_STRING_IPV6_SERVICE_NO_SCOPE"></span><span id="net_string_ipv6_service_no_scope"></span><dl> <dt>**NET \_ STRING \_ IPV6 \_ SERVICE \_ NO \_ SCOPE**</dt> </dl> | Die Zeichenfolge identifiziert einen IPv6-Dienst mithilfe einer Literaladresse, bei der der Schnittstellenkontext bereits bekannt ist (Port erforderlich, Präfix nicht zulässig, Bereichs-ID nicht zulässig).<br/> |
| <span id="NET_STRING_IPV6_NETWORK"></span><span id="net_string_ipv6_network"></span><dl> <dt>**NET \_ STRING \_ IPV6 \_ NETWORK**</dt> </dl>                              | Die Zeichenfolge identifiziert ein IPv6-Netzwerk (Präfix erforderlich; Port oder Bereichs-ID nicht zulässig).<br/>                                                                              |
| <span id="NET_STRING_NAMED_ADDRESS"></span><span id="net_string_named_address"></span><dl> <dt>**NET \_ STRING \_ NAMED \_ ADDRESS**</dt> </dl>                           | Die Zeichenfolge identifiziert einen Internethost mithilfe des DNS (Port oder Präfix oder Bereichs-ID nicht zulässig).<br/>                                                                       |
| <span id="NET_STRING_NAMED_SERVICE"></span><span id="net_string_named_service"></span><dl> <dt>**NET \_ STRING \_ NAMED \_ SERVICE**</dt> </dl>                           | Die Zeichenfolge identifiziert einen Internetdienst mit dns (Port erforderlich; Präfix oder Bereichs-ID nicht zulässig).<br/>                                                                |
| <span id="NET_STRING_IP_ADDRESS"></span><span id="net_string_ip_address"></span><dl> <dt>**NET \_ STRING \_ IP \_ ADDRESS**</dt> </dl>                                    | NET \_ STRING \_ IPV4 \_ ADDRESS \| NET \_ STRING \_ IPV6 \_ ADDRESS.<br/>                                                                                                           |
| <span id="NET_STRING_IP_ADDRESS_NO_SCOPE"></span><span id="net_string_ip_address_no_scope"></span><dl> <dt>**NET \_ STRING \_ IP \_ ADDRESS \_ NO \_ SCOPE**</dt> </dl>       | NET \_ STRING \_ IPV4 \_ ADDRESS \| NET \_ STRING \_ IPV6 \_ ADDRESS \_ NO \_ SCOPE. <br/>                                                                                               |
| <span id="NET_STRING_IP_SERVICE"></span><span id="net_string_ip_service"></span><dl> <dt>**NET \_ STRING \_ IP \_ SERVICE**</dt> </dl>                                    | NET \_ STRING \_ IPV4 \_ SERVICE \| NET \_ STRING \_ IPV6 \_ SERVICE.<br/>                                                                                                           |
| <span id="NET_STRING_IP_SERVICE_NO_SCOPE"></span><span id="net_string_ip_service_no_scope"></span><dl> <dt>**NET \_ STRING \_ IP \_ SERVICE \_ NO \_ SCOPE**</dt> </dl>       | NET \_ STRING \_ NAMED \_ ADDRESS \| NET \_ STRING \_ IP \_ ADDRESS \_ NO \_ SCOPE.<br/>                                                                                                 |
| <span id="NET_STRING_IP_NETWORK"></span><span id="net_string_ip_network"></span><dl> <dt>**NET \_ STRING \_ IP \_ NETWORK**</dt> </dl>                                    | NET \_ STRING \_ IPV4 \_ NETWORK \| NET \_ STRING \_ IPV6 \_ NETWORK.<br/>                                                                                                           |
| <span id="NET_STRING_ANY_ADDRESS"></span><span id="net_string_any_address"></span><dl> <dt>**NET \_ STRING \_ ANY \_ ADDRESS**</dt> </dl>                                 | NET \_ STRING \_ NAMED \_ ADDRESS \| NET \_ STRING \_ IP \_ ADDRESS.<br/>                                                                                                            |
| <span id="NET_STRING_ANY_ADDRESS_NO_SCOPE"></span><span id="net_string_any_address_no_scope"></span><dl> <dt>**NET \_ STRING \_ ANY \_ ADDRESS \_ NO \_ SCOPE**</dt> </dl>    | NET \_ STRING \_ NAMED \_ ADDRESS \| NET \_ STRING \_ IP \_ ADDRESS \_ NO \_ SCOPE.<br/>                                                                                                 |
| <span id="NET_STRING_ANY_SERVICE"></span><span id="net_string_any_service"></span><dl> <dt>**NET \_ STRING \_ ANY \_ SERVICE**</dt> </dl>                                 | NET \_ STRING \_ NAMED \_ SERVICE \| NET \_ STRING \_ IP \_ SERVICE.<br/>                                                                                                            |
| <span id="NET_STRING_ANY_SERVICE_NO_SCOPE"></span><span id="net_string_any_service_no_scope"></span><dl> <dt>**NET \_ STRING \_ ANY \_ SERVICE \_ NO \_ SCOPE**</dt> </dl>    | NET \_ STRING \_ NAMED \_ ADDRESS \| NET \_ STRING \_ IP \_ ADDRESS \_ NO \_ SCOPE.<br/>                                                                                                 |



## <a name="remarks"></a>Hinweise

Diese Werte werden in Iphlpapi.h definiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Iphlpapi.h</dt> </dl> |



 

 




