---
description: Stellen Sie Netzwerk Adresstypen dar. Verwenden Sie mindestens eine (als bitweise Kombination) der folgenden Konstanten, um eine Netzwerk Adress Maske zu erstellen, die mit dem Makro netaddr-Typ "netaddr" verwendet werden soll \_ .
title: NET_STRING (iphlpapi. h)
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
ms.openlocfilehash: 41ebe1cb844ec36ef13c8f8fe143d46dd9ac51b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104993774"
---
# <a name="net_string"></a>NET- \_ Zeichenfolge

Stellen Sie Netzwerk Adresstypen dar. Verwenden Sie mindestens eine (als bitweise Kombination) der folgenden Konstanten, um eine Netzwerk Adress Maske zu erstellen, die mit dem Makro [**netaddr- \_ Typ "netaddr**](/windows/desktop/api/Shellapi/nf-shellapi-netaddr_setallowtype)" verwendet werden soll.



| Konstante                                                                                                                                                                                                                   | BESCHREIBUNG                                                                                                                                                                    |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="NET_STRING_IPV4_ADDRESS"></span><span id="net_string_ipv4_address"></span><dl> <dt>**NET \_ String- \_ IPv4- \_ Adresse**</dt> </dl>                              | Die Zeichenfolge identifiziert einen IPv4-Host/-Router mit Literaladresse (Port oder Präfix nicht zulässig).<br/>                                                                       |
| <span id="NET_STRING_IPV4_SERVICE"></span><span id="net_string_ipv4_service"></span><dl> <dt>**NET \_ String- \_ IPv4- \_ Dienst**</dt> </dl>                              | Die Zeichenfolge identifiziert einen IPv4-Dienst mithilfe der Literaladresse (Port erforderlich, Präfix nicht zulässig).<br/>                                                                    |
| <span id="NET_STRING_IPV4_NETWORK"></span><span id="net_string_ipv4_network"></span><dl> <dt>**NET \_ String- \_ IPv4- \_ Netzwerk**</dt> </dl>                              | Die Zeichenfolge identifiziert ein IPv4-Netzwerk (Präfix erforderlich; Port nicht zulässig).<br/>                                                                                          |
| <span id="NET_STRING_IPV6_ADDRESS"></span><span id="net_string_ipv6_address"></span><dl> <dt>**IPv6-Adresse für NET \_ String \_ \_**</dt> </dl>                              | Die Zeichenfolge identifiziert einen IPv6-Host/-Router mit Literaladresse (Port oder Präfix nicht zulässig; Bereichs-ID zulässig).<br/>                                                     |
| <span id="NET_STRING_IPV6_ADDRESS_NO_SCOPE"></span><span id="net_string_ipv6_address_no_scope"></span><dl> <dt>**IPv6-Adressbereich für NET- \_ Zeichenfolge \_ \_ \_ nicht \_**</dt> </dl> | Die Zeichenfolge identifiziert einen IPv6-Host/-Router mithilfe der Literaladresse, bei der der Schnittstellen Kontext bereits bekannt ist (Port oder Präfix nicht zulässig; Bereichs-ID nicht zulässig).<br/>    |
| <span id="NET_STRING_IPV6_SERVICE"></span><span id="net_string_ipv6_service"></span><dl> <dt>**NET \_ String- \_ IPv6- \_ Dienst**</dt> </dl>                              | Die Zeichenfolge identifiziert einen IPv6-Dienst unter Verwendung der Literaladresse (Port erforderlich, Präfix nicht zulässig; Bereichs-ID zulässig).<br/>                                                  |
| <span id="NET_STRING_IPV6_SERVICE_NO_SCOPE"></span><span id="net_string_ipv6_service_no_scope"></span><dl> <dt>**IPv6-Dienst für NET- \_ Zeichen folgen \_ \_ \_ ohne \_ Bereich**</dt> </dl> | Die Zeichenfolge identifiziert einen IPv6-Dienst mithilfe der Literaladresse, bei der der Schnittstellen Kontext bereits bekannt ist (Port erforderlich, Präfix nicht zulässig; Bereichs-ID nicht zulässig).<br/> |
| <span id="NET_STRING_IPV6_NETWORK"></span><span id="net_string_ipv6_network"></span><dl> <dt>**\_Netzwerk-Zeichenfolge \_ IPv6- \_ Netzwerk**</dt> </dl>                              | Die Zeichenfolge identifiziert ein IPv6-Netzwerk (Präfix erforderlich; Port oder Bereichs-ID nicht zulässig).<br/>                                                                              |
| <span id="NET_STRING_NAMED_ADDRESS"></span><span id="net_string_named_address"></span><dl> <dt>**benannte Adresse der NET- \_ Zeichenfolge \_ \_**</dt> </dl>                           | Die Zeichenfolge identifiziert einen Internet Host mithilfe des DNS (Port, Präfix oder Bereichs-ID nicht zulässig).<br/>                                                                       |
| <span id="NET_STRING_NAMED_SERVICE"></span><span id="net_string_named_service"></span><dl> <dt>**benannte Dienst für NET- \_ Zeichenfolge \_ \_**</dt> </dl>                           | Die Zeichenfolge identifiziert einen Internet Dienst mithilfe von DNS (Port erforderlich, Präfix oder Bereichs-ID nicht zulässig).<br/>                                                                |
| <span id="NET_STRING_IP_ADDRESS"></span><span id="net_string_ip_address"></span><dl> <dt>**NET \_ String \_ -IP- \_ Adresse**</dt> </dl>                                    | NET \_ String \_ IPv4 \_ Address \| net \_ String \_ IPv6- \_ Adresse.<br/>                                                                                                           |
| <span id="NET_STRING_IP_ADDRESS_NO_SCOPE"></span><span id="net_string_ip_address_no_scope"></span><dl> <dt>**NET \_ String \_ -IP- \_ Adresse \_ ohne \_ Bereich**</dt> </dl>       | NET \_ String \_ IPv4 \_ Address \| net \_ String \_ IPv6 \_ Address \_ No \_ Scope. <br/>                                                                                               |
| <span id="NET_STRING_IP_SERVICE"></span><span id="net_string_ip_service"></span><dl> <dt>**NET \_ String \_ -IP- \_ Dienst**</dt> </dl>                                    | NET \_ String \_ IPv4 \_ Service \| net \_ String \_ IPv6- \_ Dienst.<br/>                                                                                                           |
| <span id="NET_STRING_IP_SERVICE_NO_SCOPE"></span><span id="net_string_ip_service_no_scope"></span><dl> <dt>**NET \_ String \_ -IP- \_ Dienst \_ ohne \_ Bereich**</dt> </dl>       | NET \_ -Zeichenfolge mit dem \_ Namen \_ Address \| net \_ String \_ IP \_ Address \_ No \_ Scope.<br/>                                                                                                 |
| <span id="NET_STRING_IP_NETWORK"></span><span id="net_string_ip_network"></span><dl> <dt>**\_Netzwerk Zeichen folgen \_ -IP- \_ Netzwerk**</dt> </dl>                                    | Netzwerk-Zeichen folgen- \_ \_ IPv4- \_ Netzwerk \| \_ Zeichenfolge \_ IPv6- \_ Netzwerk.<br/>                                                                                                           |
| <span id="NET_STRING_ANY_ADDRESS"></span><span id="net_string_any_address"></span><dl> <dt>**beliebige Adresse für NET- \_ Zeichenfolge \_ \_**</dt> </dl>                                 | NET \_ -Zeichenfolge mit dem \_ Namen \_ Address \| net \_ String \_ IP \_ Address.<br/>                                                                                                            |
| <span id="NET_STRING_ANY_ADDRESS_NO_SCOPE"></span><span id="net_string_any_address_no_scope"></span><dl> <dt>**NET \_ String \_ Any \_ Address \_ No \_ Scope**</dt> </dl>    | NET \_ -Zeichenfolge mit dem \_ Namen \_ Address \| net \_ String \_ IP \_ Address \_ No \_ Scope.<br/>                                                                                                 |
| <span id="NET_STRING_ANY_SERVICE"></span><span id="net_string_any_service"></span><dl> <dt>**NET \_ String \_ beliebiger \_ Dienst**</dt> </dl>                                 | NET \_ -Zeichenfolge mit dem \_ Namen \_ Service \| net \_ String \_ IP \_ Service.<br/>                                                                                                            |
| <span id="NET_STRING_ANY_SERVICE_NO_SCOPE"></span><span id="net_string_any_service_no_scope"></span><dl> <dt>**NET \_ String \_ beliebiger \_ Dienst \_ keinen \_ Bereich**</dt> </dl>    | NET \_ -Zeichenfolge mit dem \_ Namen \_ Address \| net \_ String \_ IP \_ Address \_ No \_ Scope.<br/>                                                                                                 |



## <a name="remarks"></a>Bemerkungen

Diese Werte werden in iphlpapi. h definiert.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Iphlpapi. h</dt> </dl> |



 

 




