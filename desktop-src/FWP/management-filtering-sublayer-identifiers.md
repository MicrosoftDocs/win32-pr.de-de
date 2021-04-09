---
title: Filtern von subebenenbezeichgern ("f")
description: WFP API Management filtert untergeordnete bezeichnerkonstanten.
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
ms.openlocfilehash: e015d590c19395987bbd47d1c3c4b918296ab5f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859144"
---
# <a name="filtering-sublayer-identifiers"></a>Filtern von subebenenbezeichgern

Die subebenenbezeichner der Windows-Filter Plattform (WFP) werden jeweils durch eine GUID dargestellt.

Diese Bezeichner werden wie folgt definiert.

<dl> <dt>

<span id="FWPM_SUBLAYER_EDGE_TRAVERSAL________________________FWPM_SUBLAYER_TEREDO"></span><span id="fwpm_sublayer_edge_traversal________________________fwpm_sublayer_teredo"></span>**Edge-Traversierung der WPM \_ -Subschicht \_ \_ /- \_ unterebenenteredo \_**
</dt> <dd> <dl> <dt>



Edge-Traversale-Filter werden dieser Unterschicht hinzugefügt.

> [!Note]  
> Verwenden Sie für Windows 7 und höher die Edgeausnahme der Unterschicht der Windows- **\_ Subschicht \_ \_**.

 


</dt> </dl> </dd> <dt>

<span id="FWPM_SUBLAYER_INSPECTION"></span><span id="fwpm_sublayer_inspection"></span>**Überprüfung der \_ untergeordneten Schicht \_**
</dt> <dd> <dl> <dt>



Dies ist die niedrigste gewichtete Unterschicht. Sie wird nur für Inspektions Filter verwendet.


</dt> </dl> </dd> <dt>

<span id="FWPM_SUBLAYER_IPSEC_DOSP"></span><span id="fwpm_sublayer_ipsec_dosp"></span>**\_ \_ IPSec-DoSP der WPM-Unterschicht \_**
</dt> <dd> <dl> <dt>



IPSec-DOS-Schutzfilter werden dieser Unterschicht hinzugefügt.

> [!Note]  
> Nur unter Windows Vista mit SP1, Windows Server 2008 und höher verfügbar.

 


</dt> </dl> </dd> <dt>

<span id="FWPM_SUBLAYER_IPSEC_FORWARD_OUTBOUND_TUNNEL"></span><span id="fwpm_sublayer_ipsec_forward_outbound_tunnel"></span>**WPM- \_ Subschicht- \_ IPSec \_ Forward- \_ Tunnel für Ausgeh \_ enden Datenverkehr**
</dt> <dd> <dl> <dt>



Der untergeordneten Ebene werden Filter Filter für ausgehenden IPSec-Tunnel hinzugefügt.

> [!Note]  
> Nur unter Windows 7, Windows Server 2008 R2 und höher verfügbar.

 


</dt> </dl> </dd> <dt>

<span id="FWPM_SUBLAYER_IPSEC_TUNNEL"></span><span id="fwpm_sublayer_ipsec_tunnel"></span>**\_ \_ IPSec-Tunnel für die Subschicht der WPM \_**
</dt> <dd> <dl> <dt>



IPSec-Tunnel Filter werden dieser Unterschicht hinzugefügt.


</dt> </dl> </dd> <dt>

<span id="FWPM_SUBLAYER_LIPS"></span><span id="fwpm_sublayer_lips"></span>**\_subebenenlips der WPM \_**
</dt> <dd> <dl> <dt>



Dieser Unterebene werden ältere IPSec-Filter hinzugefügt.


</dt> </dl> </dd> <dt>

<span id="FWPM_SUBLAYER_RPC_AUDIT"></span><span id="fwpm_sublayer_rpc_audit"></span>**WPM- \_ Subschicht- \_ RPC- \_ Überwachung**
</dt> <dd> <dl> <dt>



RPC-Überwachungs Filter werden dieser Unterschicht hinzugefügt. Diese Filter überwachen eingehende RPC-Aufrufe als Teil von C2 und Common Criteria-Konformität.


</dt> </dl> </dd> <dt>

<span id="FWPM_SUBLAYER_SECURE_SOCKET"></span><span id="fwpm_sublayer_secure_socket"></span>**sicherer Socket der WPM- \_ Subschicht \_ \_**
</dt> <dd> <dl> <dt>



Dieser Unterschicht werden Secure Socket-Filter hinzugefügt.


</dt> </dl> </dd> <dt>

<span id="FWPM_SUBLAYER_TCP_CHIMNEY_OFFLOAD"></span><span id="fwpm_sublayer_tcp_chimney_offload"></span>**\_ \_ TCP-Chimney- \_ \_ Abladung der WPM-Unterschicht**
</dt> <dd> <dl> <dt>



TCP-Chimney-Ablade Filter werden dieser Unterschicht hinzugefügt.


</dt> </dl> </dd> <dt>

<span id="FWPM_SUBLAYER_TCP_TEMPLATES______________________"></span><span id="fwpm_sublayer_tcp_templates______________________"></span>**TCP-Vorlagen für die WPM- \_ Unterschicht \_ \_** 
</dt> <dd> <dl> <dt>



TCP-Vorlagen Filter werden dieser Unterschicht hinzugefügt.

> [!Note]  
> Nur unter Windows 8, Windows Server 2012 und höher verfügbar.

 


</dt> </dl> </dd> <dt>

<span id="FWPM_SUBLAYER_UNIVERSAL"></span><span id="fwpm_sublayer_universal"></span>**uwpm- \_ Subschicht \_ universell**
</dt> <dd> <dl> <dt>



Diese Unterschicht hostet alle Filter, die keiner der anderen untergeordneten Ebenen zugewiesen sind.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>"F"</dt> </dl> |



 

 





