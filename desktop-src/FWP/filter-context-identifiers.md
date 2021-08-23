---
title: Filtern von Kontextbezeichnern (Fwpmu.h)
description: Bezeichner für die Filterkontexte, die in die Windows Filterplattform integriert sind.
ms.assetid: bcfae832-5386-43c5-b916-89577765ee5d
topic_type:
- apiref
api_name:
- FWPM_CONTEXT_IPSEC_INBOUND_PASSTHRU, FWPM_CONTEXT_IPSEC_INBOUND_PERSIST_CONNECTION_SECURITY, FWPM_CONTEXT_IPSEC_INBOUND_RESERVED
- FWPM_CONTEXT_IPSEC_OUTBOUND_NEGOTIATE_DISCOVER, FWPM_CONTEXT_IPSEC_OUTBOUND_SUPPRESS_NEGOTIATION
- FWPM_CONTEXT_ALE_SET_CONNECTION_REQUIRE_IPSEC_SECURITY, FWPM_CONTEXT_ALE_SET_CONNECTION_LAZY_SD_EVALUATION
- FWPM_CONTEXT_ALE_SET_CONNECTION_REQUIRE_IPSEC_ENCRYPTION, FWPM_CONTEXT_ALE_SET_CONNECTION_ALLOW_FIRST_INBOUND_PKT_UNENCRYPTED, FWPM_CONTEXT_ALE_ALLOW_AUTH_FW
- FWPM_CONTEXT_TCP_CHIMNEY_OFFLOAD_ENABLE, FWPM_CONTEXT_TCP_CHIMNEY_OFFLOAD_DISABLE
- FWPM_CONTEXT_RPC_AUDIT_ENABLED
api_location:
- fwpmu.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fdc7d9914a9b6089ace87e7e9b942499d8e65dc7705bf524f74cddf96ee419d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118951269"
---
# <a name="filter-context-identifiers"></a>Filtern von Kontextbezeichnern

Die Bezeichner für die Filterkontexte, die in die Windows Filterplattform integriert sind, werden wie folgt definiert.

<dl> <dt>

<span id="FWPM_CONTEXT_IPSEC_INBOUND_PASSTHRU__FWPM_CONTEXT_IPSEC_INBOUND_PERSIST_CONNECTION_SECURITY___FWPM_CONTEXT_IPSEC_INBOUND_RESERVED"></span><span id="fwpm_context_ipsec_inbound_passthru__fwpm_context_ipsec_inbound_persist_connection_security___fwpm_context_ipsec_inbound_reserved"></span>**FWPM \_ CONTEXT \_ IPSEC \_ INBOUND \_ PASSTHRU, FWPM \_ CONTEXT \_ IPSEC \_ INBOUND \_ PERSIST \_ CONNECTION \_ SECURITY, FWPM \_ CONTEXT \_ IPSEC \_ INBOUND \_ RESERVED**
</dt> <dd> <dl> <dt>



IPsec-Transportfilterkontexte in eingehender Ebene.


</dt> </dl> </dd> <dt>

<span id="FWPM_CONTEXT_IPSEC_OUTBOUND_NEGOTIATE_DISCOVER__FWPM_CONTEXT_IPSEC_OUTBOUND_SUPPRESS_NEGOTIATION"></span><span id="fwpm_context_ipsec_outbound_negotiate_discover__fwpm_context_ipsec_outbound_suppress_negotiation"></span>**FWPM \_ CONTEXT \_ IPSEC \_ OUTBOUND \_ NEGOTIATE \_ DISCOVER, FWPM \_ CONTEXT \_ IPSEC \_ OUTBOUND \_ SUPPRESS \_ NEGOTIATION**
</dt> <dd> <dl> <dt>



IPsec-Transportfilterkontexte in der ausgehenden Ebene.

> [!Note]  
> Verwenden Windows 7 **den FWPM-KONTEXT \_ \_ IPSEC \_ OUTBOUND SUPPRESS \_ \_ NEGOTIATION**.

 


</dt> </dl> </dd> <dt>

<span id="FWPM_CONTEXT_ALE_SET_CONNECTION_REQUIRE_IPSEC_SECURITY__FWPM_CONTEXT_ALE_SET_CONNECTION_LAZY_SD_EVALUATION"></span><span id="fwpm_context_ale_set_connection_require_ipsec_security__fwpm_context_ale_set_connection_lazy_sd_evaluation"></span>**FWPM \_ CONTEXT \_ ALE \_ SET \_ CONNECTION \_ REQUIRE \_ IPSEC \_ SECURITY, FWPM \_ CONTEXT \_ ALE \_ SET \_ CONNECTION \_ LAZY \_ SD \_ EVALUATION**
</dt> <dd> <dl> <dt>



Filterkontexte, die in der ALE-Verbindungsschicht verwendet werden.


</dt> </dl> </dd> <dt>

<span id="FWPM_CONTEXT_ALE_SET_CONNECTION_REQUIRE_IPSEC_ENCRYPTION__FWPM_CONTEXT_ALE_SET_CONNECTION_ALLOW_FIRST_INBOUND_PKT_UNENCRYPTED__FWPM_CONTEXT_ALE_ALLOW_AUTH_FW"></span><span id="fwpm_context_ale_set_connection_require_ipsec_encryption__fwpm_context_ale_set_connection_allow_first_inbound_pkt_unencrypted__fwpm_context_ale_allow_auth_fw"></span>**FWPM \_ CONTEXT \_ ALE \_ SET \_ CONNECTION \_ REQUIRE \_ IPSEC \_ ENCRYPTION, FWPM \_ CONTEXT \_ ALE \_ SET \_ CONNECTION \_ ALLOW \_ FIRST \_ INBOUND \_ PKT \_ UNENCRYPTED, FWPM \_ CONTEXT \_ ALE \_ ALLOW \_ AUTH \_ FW**
</dt> <dd> <dl> <dt>



Filterkontexte, die in der ALE-Verbindungs- oder Accept-Ebene verwendet werden.

> [!Note]  
> Verwenden Windows 7 **FWPM \_ CONTEXT \_ ALE \_ SET CONNECTION ALLOW FIRST \_ \_ \_ \_ INBOUND \_ PKT \_ UNENCRYPTED** oder **FWPM \_ CONTEXT \_ ALE ALLOW \_ \_ AUTH \_ FW**.

 


</dt> </dl> </dd> <dt>

<span id="FWPM_CONTEXT_TCP_CHIMNEY_OFFLOAD_ENABLE__FWPM_CONTEXT_TCP_CHIMNEY_OFFLOAD_DISABLE"></span><span id="fwpm_context_tcp_chimney_offload_enable__fwpm_context_tcp_chimney_offload_disable"></span>**FWPM \_ CONTEXT \_ TCP \_ CHIMNEY \_ OFFLOAD \_ ENABLE, FWPM \_ CONTEXT \_ TCP \_ CHIMNEY \_ OFFLOAD \_ DISABLE**
</dt> <dd> <dl> <dt>



Kontexte, die von den TCP Chimney Offload-Rückrufen verwendet werden.


</dt> </dl> </dd> <dt>

<span id="FWPM_CONTEXT_RPC_AUDIT_ENABLED"></span><span id="fwpm_context_rpc_audit_enabled"></span>**FWPM CONTEXT RPC AUDIT ENABLED (RPC-ÜBERWACHUNG \_ IM FWPM-KONTEXT \_ \_ \_ AKTIVIERT)**
</dt> <dd> <dl> <dt>



Kontexte, die in der RPC-Überwachungsunterschicht verwendet werden.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Fwpmu.h</dt> </dl> |



 

 





