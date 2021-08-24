---
title: Filtern von Unterschichtbezeichnern (Fwpmu.h)
description: WFP API Management filtert Unterlayerbezeichnerkonstatoren.
ms.assetid: 4c8dbe35-e84b-4490-bf7a-7ff8b94e2022
topic_type:
- apiref
api_name:
- FWPM_SUBLAYER_EDGE_TRAVERSAL / FWPM_SUBLAYER_TEREDO
- FWPM_SUBLAYER_INSPECTION
- FWPM_SUBLAYER_IPSEC_DOSP
- FWPM_SUBLAYER_IPSEC_FORWARD_OUTBOUND_TUNNEL
- FWPM_SUBLAYER_IPSEC_TUNNEL
- FWPM_SUBLAYER_LIPS
- FWPM_SUBLAYER_RPC_AUDIT
- FWPM_SUBLAYER_SECURE_SOCKET
- FWPM_SUBLAYER_TCP_CHIMNEY_OFFLOAD
- FWPM_SUBLAYER_TCP_TEMPLATES
- FWPM_SUBLAYER_UNIVERSAL
api_location:
- fwpmu.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d597fa1b75f6c965da9cf8d71bcc3e729d0b0b2f4f4220c984a1be8c94c09d39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119068880"
---
# <a name="filtering-sublayer-identifiers"></a>Filtern von Unterschichtbezeichnern

Die Windows-Unterschichtbezeichner der Filterplattform (WFP) werden jeweils durch eine GUID dargestellt.

Diese Bezeichner werden wie folgt definiert.

<dl> <dt>

<span id="FWPM_SUBLAYER_EDGE_TRAVERSAL________________________FWPM_SUBLAYER_TEREDO"></span><span id="fwpm_sublayer_edge_traversal________________________fwpm_sublayer_teredo"></span>**FWPM \_ SUBLAYER \_ EDGE \_ TRAVERSAL/FWPM \_ SUBLAYER \_ TEREDO**
</dt> <dd> <dl> <dt>



Edgedurchlauffilter werden dieser Unterschicht hinzugefügt.

> [!Note]  
> Für Windows 7 und höher verwenden Sie **FWPM \_ SUBLAYER \_ EDGE \_ TRAVERSAL**.

 


</dt> </dl> </dd> <dt>

<span id="FWPM_SUBLAYER_INSPECTION"></span><span id="fwpm_sublayer_inspection"></span>**\_FWPM-UNTERSCHICHTUNTERSUCHUNG \_**
</dt> <dd> <dl> <dt>



Dies ist die unterste gewichtete Unterschicht. Es wird nur für Überprüfungsfilter verwendet.


</dt> </dl> </dd> <dt>

<span id="FWPM_SUBLAYER_IPSEC_DOSP"></span><span id="fwpm_sublayer_ipsec_dosp"></span>**\_ \_ IPSEC-DOSP FÜR FWPM-UNTERSCHICHT \_**
</dt> <dd> <dl> <dt>



IPsec DoS Protection-Filter werden dieser Unterschicht hinzugefügt.

> [!Note]  
> Nur auf Windows Vista mit SP1, Windows Server 2008 und höher verfügbar.

 


</dt> </dl> </dd> <dt>

<span id="FWPM_SUBLAYER_IPSEC_FORWARD_OUTBOUND_TUNNEL"></span><span id="fwpm_sublayer_ipsec_forward_outbound_tunnel"></span>**\_FWPM-UNTERLAYER \_ IPSEC \_ FORWARD \_ OUTBOUND \_ TUNNEL**
</dt> <dd> <dl> <dt>



IPsec-Tunnelfilter für ausgehenden Datenverkehr werden dieser Unterschicht hinzugefügt.

> [!Note]  
> Nur unter Windows 7, Windows Server 2008 R2 und höher verfügbar.

 


</dt> </dl> </dd> <dt>

<span id="FWPM_SUBLAYER_IPSEC_TUNNEL"></span><span id="fwpm_sublayer_ipsec_tunnel"></span>**IPSEC-TUNNEL \_ FÜR FWPM-UNTERSCHICHT \_ \_**
</dt> <dd> <dl> <dt>



IPsec-Tunnelfilter werden dieser Unterschicht hinzugefügt.


</dt> </dl> </dd> <dt>

<span id="FWPM_SUBLAYER_LIPS"></span><span id="fwpm_sublayer_lips"></span>**\_FWPM-UNTERSCHICHTEN \_**
</dt> <dd> <dl> <dt>



Legacy-IPsec-Filter werden dieser Unterschicht hinzugefügt.


</dt> </dl> </dd> <dt>

<span id="FWPM_SUBLAYER_RPC_AUDIT"></span><span id="fwpm_sublayer_rpc_audit"></span>**RPC-ÜBERWACHUNG \_ FÜR FWPM-UNTERSCHICHT \_ \_**
</dt> <dd> <dl> <dt>



RPC-Überwachungsfilter werden dieser Unterschicht hinzugefügt. Diese Filter überwachen eingehende RPC-Aufrufe im Rahmen von C2 und der Einhaltung gängiger Kriterien.


</dt> </dl> </dd> <dt>

<span id="FWPM_SUBLAYER_SECURE_SOCKET"></span><span id="fwpm_sublayer_secure_socket"></span>**SICHERER SOCKET FÜR \_ FWPM-UNTERSCHICHT \_ \_**
</dt> <dd> <dl> <dt>



Secure Socket-Filter werden dieser Unterschicht hinzugefügt.


</dt> </dl> </dd> <dt>

<span id="FWPM_SUBLAYER_TCP_CHIMNEY_OFFLOAD"></span><span id="fwpm_sublayer_tcp_chimney_offload"></span>**\_TCP-CHIMNEY-AUSLADUNG \_ DER FWPM-UNTERSCHICHT \_ \_**
</dt> <dd> <dl> <dt>



TCP-Chimney-Ausladungsfilter werden dieser Unterschicht hinzugefügt.


</dt> </dl> </dd> <dt>

<span id="FWPM_SUBLAYER_TCP_TEMPLATES______________________"></span><span id="fwpm_sublayer_tcp_templates______________________"></span>**TCP-VORLAGEN FÜR \_ FWPM-UNTERSCHICHT \_ \_** 
</dt> <dd> <dl> <dt>



TCP-Vorlagenfilter werden dieser Unterschicht hinzugefügt.

> [!Note]  
> Nur für Windows 8, Windows Server 2012 und höher verfügbar.

 


</dt> </dl> </dd> <dt>

<span id="FWPM_SUBLAYER_UNIVERSAL"></span><span id="fwpm_sublayer_universal"></span>**FWPM \_ SUBLAYER \_ UNIVERSAL**
</dt> <dd> <dl> <dt>



Diese Unterschicht hostet alle Filter, die keinen der anderen Unterschichten zugewiesen sind.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Fwpmu.h</dt> </dl> |



 

 





