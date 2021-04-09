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
# <a name="filtering-sublayer-identifiers"></a><span data-ttu-id="a2907-103">Filtern von subebenenbezeichgern</span><span class="sxs-lookup"><span data-stu-id="a2907-103">Filtering Sublayer Identifiers</span></span>

<span data-ttu-id="a2907-104">Die subebenenbezeichner der Windows-Filter Plattform (WFP) werden jeweils durch eine GUID dargestellt.</span><span class="sxs-lookup"><span data-stu-id="a2907-104">The Windows Filtering Platform (WFP) sublayer identifiers are each represented by a GUID.</span></span>

<span data-ttu-id="a2907-105">Diese Bezeichner werden wie folgt definiert.</span><span class="sxs-lookup"><span data-stu-id="a2907-105">These identifiers are defined as follows.</span></span>

<dl> <dt>

<span data-ttu-id="a2907-106"><span id="FWPM_SUBLAYER_EDGE_TRAVERSAL________________________FWPM_SUBLAYER_TEREDO"></span><span id="fwpm_sublayer_edge_traversal________________________fwpm_sublayer_teredo"></span>**Edge-Traversierung der WPM \_ -Subschicht \_ \_ /- \_ unterebenenteredo \_**</span><span class="sxs-lookup"><span data-stu-id="a2907-106"><span id="FWPM_SUBLAYER_EDGE_TRAVERSAL________________________FWPM_SUBLAYER_TEREDO"></span><span id="fwpm_sublayer_edge_traversal________________________fwpm_sublayer_teredo"></span>**FWPM\_SUBLAYER\_EDGE\_TRAVERSAL / FWPM\_SUBLAYER\_TEREDO**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a2907-107">Edge-Traversale-Filter werden dieser Unterschicht hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a2907-107">Edge traversal filters are added to this sublayer.</span></span>

> [!Note]  
> <span data-ttu-id="a2907-108">Verwenden Sie für Windows 7 und höher die Edgeausnahme der Unterschicht der Windows- **\_ Subschicht \_ \_**.</span><span class="sxs-lookup"><span data-stu-id="a2907-108">For Windows 7 and later, use **FWPM\_SUBLAYER\_EDGE\_TRAVERSAL**.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="a2907-109"><span id="FWPM_SUBLAYER_INSPECTION"></span><span id="fwpm_sublayer_inspection"></span>**Überprüfung der \_ untergeordneten Schicht \_**</span><span class="sxs-lookup"><span data-stu-id="a2907-109"><span id="FWPM_SUBLAYER_INSPECTION"></span><span id="fwpm_sublayer_inspection"></span>**FWPM\_SUBLAYER\_INSPECTION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a2907-110">Dies ist die niedrigste gewichtete Unterschicht.</span><span class="sxs-lookup"><span data-stu-id="a2907-110">This is the lowest weighted sublayer.</span></span> <span data-ttu-id="a2907-111">Sie wird nur für Inspektions Filter verwendet.</span><span class="sxs-lookup"><span data-stu-id="a2907-111">It is used only for inspection filters.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a2907-112"><span id="FWPM_SUBLAYER_IPSEC_DOSP"></span><span id="fwpm_sublayer_ipsec_dosp"></span>**\_ \_ IPSec-DoSP der WPM-Unterschicht \_**</span><span class="sxs-lookup"><span data-stu-id="a2907-112"><span id="FWPM_SUBLAYER_IPSEC_DOSP"></span><span id="fwpm_sublayer_ipsec_dosp"></span>**FWPM\_SUBLAYER\_IPSEC\_DOSP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a2907-113">IPSec-DOS-Schutzfilter werden dieser Unterschicht hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a2907-113">IPsec DoS Protection filters are added to this sublayer.</span></span>

> [!Note]  
> <span data-ttu-id="a2907-114">Nur unter Windows Vista mit SP1, Windows Server 2008 und höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a2907-114">Available only on Windows Vista with SP1, Windows Server 2008, and later.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="a2907-115"><span id="FWPM_SUBLAYER_IPSEC_FORWARD_OUTBOUND_TUNNEL"></span><span id="fwpm_sublayer_ipsec_forward_outbound_tunnel"></span>**WPM- \_ Subschicht- \_ IPSec \_ Forward- \_ Tunnel für Ausgeh \_ enden Datenverkehr**</span><span class="sxs-lookup"><span data-stu-id="a2907-115"><span id="FWPM_SUBLAYER_IPSEC_FORWARD_OUTBOUND_TUNNEL"></span><span id="fwpm_sublayer_ipsec_forward_outbound_tunnel"></span>**FWPM\_SUBLAYER\_IPSEC\_FORWARD\_OUTBOUND\_TUNNEL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a2907-116">Der untergeordneten Ebene werden Filter Filter für ausgehenden IPSec-Tunnel hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a2907-116">IPsec forward outbound tunnel filters are added to this sublayer.</span></span>

> [!Note]  
> <span data-ttu-id="a2907-117">Nur unter Windows 7, Windows Server 2008 R2 und höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a2907-117">Available only on Windows 7, Windows Server 2008 R2, and later.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="a2907-118"><span id="FWPM_SUBLAYER_IPSEC_TUNNEL"></span><span id="fwpm_sublayer_ipsec_tunnel"></span>**\_ \_ IPSec-Tunnel für die Subschicht der WPM \_**</span><span class="sxs-lookup"><span data-stu-id="a2907-118"><span id="FWPM_SUBLAYER_IPSEC_TUNNEL"></span><span id="fwpm_sublayer_ipsec_tunnel"></span>**FWPM\_SUBLAYER\_IPSEC\_TUNNEL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a2907-119">IPSec-Tunnel Filter werden dieser Unterschicht hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a2907-119">IPsec tunnel filters are added to this sublayer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a2907-120"><span id="FWPM_SUBLAYER_LIPS"></span><span id="fwpm_sublayer_lips"></span>**\_subebenenlips der WPM \_**</span><span class="sxs-lookup"><span data-stu-id="a2907-120"><span id="FWPM_SUBLAYER_LIPS"></span><span id="fwpm_sublayer_lips"></span>**FWPM\_SUBLAYER\_LIPS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a2907-121">Dieser Unterebene werden ältere IPSec-Filter hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a2907-121">Legacy IPsec filters are added to this sublayer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a2907-122"><span id="FWPM_SUBLAYER_RPC_AUDIT"></span><span id="fwpm_sublayer_rpc_audit"></span>**WPM- \_ Subschicht- \_ RPC- \_ Überwachung**</span><span class="sxs-lookup"><span data-stu-id="a2907-122"><span id="FWPM_SUBLAYER_RPC_AUDIT"></span><span id="fwpm_sublayer_rpc_audit"></span>**FWPM\_SUBLAYER\_RPC\_AUDIT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a2907-123">RPC-Überwachungs Filter werden dieser Unterschicht hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a2907-123">RPC audit filters are added to this sublayer.</span></span> <span data-ttu-id="a2907-124">Diese Filter überwachen eingehende RPC-Aufrufe als Teil von C2 und Common Criteria-Konformität.</span><span class="sxs-lookup"><span data-stu-id="a2907-124">These filters audit RPC incoming calls as part of C2 and common criteria compliance.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a2907-125"><span id="FWPM_SUBLAYER_SECURE_SOCKET"></span><span id="fwpm_sublayer_secure_socket"></span>**sicherer Socket der WPM- \_ Subschicht \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a2907-125"><span id="FWPM_SUBLAYER_SECURE_SOCKET"></span><span id="fwpm_sublayer_secure_socket"></span>**FWPM\_SUBLAYER\_SECURE\_SOCKET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a2907-126">Dieser Unterschicht werden Secure Socket-Filter hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a2907-126">Secure socket filters are added to this sublayer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a2907-127"><span id="FWPM_SUBLAYER_TCP_CHIMNEY_OFFLOAD"></span><span id="fwpm_sublayer_tcp_chimney_offload"></span>**\_ \_ TCP-Chimney- \_ \_ Abladung der WPM-Unterschicht**</span><span class="sxs-lookup"><span data-stu-id="a2907-127"><span id="FWPM_SUBLAYER_TCP_CHIMNEY_OFFLOAD"></span><span id="fwpm_sublayer_tcp_chimney_offload"></span>**FWPM\_SUBLAYER\_TCP\_CHIMNEY\_OFFLOAD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a2907-128">TCP-Chimney-Ablade Filter werden dieser Unterschicht hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a2907-128">TCP Chimney Offload filters are added to this sublayer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a2907-129"><span id="FWPM_SUBLAYER_TCP_TEMPLATES______________________"></span><span id="fwpm_sublayer_tcp_templates______________________"></span>**TCP-Vorlagen für die WPM- \_ Unterschicht \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a2907-129"><span id="FWPM_SUBLAYER_TCP_TEMPLATES______________________"></span><span id="fwpm_sublayer_tcp_templates______________________"></span>**FWPM\_SUBLAYER\_TCP\_TEMPLATES**</span></span> 
</dt> <dd> <dl> <dt>



<span data-ttu-id="a2907-130">TCP-Vorlagen Filter werden dieser Unterschicht hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a2907-130">TCP template filters are added to this sublayer.</span></span>

> [!Note]  
> <span data-ttu-id="a2907-131">Nur unter Windows 8, Windows Server 2012 und höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a2907-131">Available only on Windows 8, Windows Server 2012, and later.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="a2907-132"><span id="FWPM_SUBLAYER_UNIVERSAL"></span><span id="fwpm_sublayer_universal"></span>**uwpm- \_ Subschicht \_ universell**</span><span class="sxs-lookup"><span data-stu-id="a2907-132"><span id="FWPM_SUBLAYER_UNIVERSAL"></span><span id="fwpm_sublayer_universal"></span>**FWPM\_SUBLAYER\_UNIVERSAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a2907-133">Diese Unterschicht hostet alle Filter, die keiner der anderen untergeordneten Ebenen zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="a2907-133">This sublayer hosts all filters that are not assigned to any of the other sublayers.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a2907-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a2907-134">Requirements</span></span>



| <span data-ttu-id="a2907-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a2907-135">Requirement</span></span> | <span data-ttu-id="a2907-136">Wert</span><span class="sxs-lookup"><span data-stu-id="a2907-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a2907-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a2907-137">Minimum supported client</span></span><br/> | <span data-ttu-id="a2907-138">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a2907-138">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="a2907-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a2907-139">Minimum supported server</span></span><br/> | <span data-ttu-id="a2907-140">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a2907-140">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="a2907-141">Header</span><span class="sxs-lookup"><span data-stu-id="a2907-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="a2907-142"><dt>"F"</dt></span><span class="sxs-lookup"><span data-stu-id="a2907-142"><dt>Fwpmu.h</dt></span></span> </dl> |



 

 





