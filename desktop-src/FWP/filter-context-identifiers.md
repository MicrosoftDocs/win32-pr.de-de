---
title: Filtern von Kontext bezeichgern ("f")
description: Bezeichner für die Filter Kontexte, die in die Windows-Filter Plattform integriert sind.
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
ms.openlocfilehash: c09968f1ab68016405f22460409e83cfd826b716
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340004"
---
# <a name="filter-context-identifiers"></a><span data-ttu-id="324b8-103">Filtern von Kontext bezeichlern</span><span class="sxs-lookup"><span data-stu-id="324b8-103">Filter Context Identifiers</span></span>

<span data-ttu-id="324b8-104">Die Bezeichner für die Filter Kontexte, die in die Windows-Filter Plattform integriert sind, werden wie folgt definiert.</span><span class="sxs-lookup"><span data-stu-id="324b8-104">The identifiers for the filter contexts that are built in to the Windows Filtering Platform are defined as follows.</span></span>

<dl> <dt>

<span data-ttu-id="324b8-105"><span id="FWPM_CONTEXT_IPSEC_INBOUND_PASSTHRU__FWPM_CONTEXT_IPSEC_INBOUND_PERSIST_CONNECTION_SECURITY___FWPM_CONTEXT_IPSEC_INBOUND_RESERVED"></span><span id="fwpm_context_ipsec_inbound_passthru__fwpm_context_ipsec_inbound_persist_connection_security___fwpm_context_ipsec_inbound_reserved"></span>**swpm- \_ Kontext- \_ IPSec-eingehende \_ \_ passthru, f- \_ Kontext-IPSec eingehende Beibehaltung der \_ \_ \_ \_ Verbindungs \_ Sicherheit, swpm- \_ Kontext \_ IPSec \_ eingehende \_ reserviert**</span><span class="sxs-lookup"><span data-stu-id="324b8-105"><span id="FWPM_CONTEXT_IPSEC_INBOUND_PASSTHRU__FWPM_CONTEXT_IPSEC_INBOUND_PERSIST_CONNECTION_SECURITY___FWPM_CONTEXT_IPSEC_INBOUND_RESERVED"></span><span id="fwpm_context_ipsec_inbound_passthru__fwpm_context_ipsec_inbound_persist_connection_security___fwpm_context_ipsec_inbound_reserved"></span>**FWPM\_CONTEXT\_IPSEC\_INBOUND\_PASSTHRU, FWPM\_CONTEXT\_IPSEC\_INBOUND\_PERSIST\_CONNECTION\_SECURITY, FWPM\_CONTEXT\_IPSEC\_INBOUND\_RESERVED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="324b8-106">IPsec-Transport Filter Kontexte in eingehender Schicht.</span><span class="sxs-lookup"><span data-stu-id="324b8-106">IPsec transport filter contexts in inbound layer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="324b8-107"><span id="FWPM_CONTEXT_IPSEC_OUTBOUND_NEGOTIATE_DISCOVER__FWPM_CONTEXT_IPSEC_OUTBOUND_SUPPRESS_NEGOTIATION"></span><span id="fwpm_context_ipsec_outbound_negotiate_discover__fwpm_context_ipsec_outbound_suppress_negotiation"></span>**swpm- \_ Kontext- \_ IPSec \_ ausgehende \_ Aushandlungen Ermittlung \_ , f-Kontext- \_ \_ IPSec \_ ausgehende Aushandlung unterdrücken der \_ \_ Aushandlung**</span><span class="sxs-lookup"><span data-stu-id="324b8-107"><span id="FWPM_CONTEXT_IPSEC_OUTBOUND_NEGOTIATE_DISCOVER__FWPM_CONTEXT_IPSEC_OUTBOUND_SUPPRESS_NEGOTIATION"></span><span id="fwpm_context_ipsec_outbound_negotiate_discover__fwpm_context_ipsec_outbound_suppress_negotiation"></span>**FWPM\_CONTEXT\_IPSEC\_OUTBOUND\_NEGOTIATE\_DISCOVER, FWPM\_CONTEXT\_IPSEC\_OUTBOUND\_SUPPRESS\_NEGOTIATION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="324b8-108">IPsec-Transport Filter Kontexte in der ausgehenden Schicht.</span><span class="sxs-lookup"><span data-stu-id="324b8-108">IPsec transport filter contexts in outbound layer.</span></span>

> [!Note]  
> <span data-ttu-id="324b8-109">Verwenden Sie für Windows 7 den **Kontext der \_ \_ IPSec-unter \_ \_ Unterdrückung \_ für den WPM-Kontext**.</span><span class="sxs-lookup"><span data-stu-id="324b8-109">For Windows 7, use **FWPM\_CONTEXT\_IPSEC\_OUTBOUND\_SUPPRESS\_NEGOTIATION**.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="324b8-110"><span id="FWPM_CONTEXT_ALE_SET_CONNECTION_REQUIRE_IPSEC_SECURITY__FWPM_CONTEXT_ALE_SET_CONNECTION_LAZY_SD_EVALUATION"></span><span id="fwpm_context_ale_set_connection_require_ipsec_security__fwpm_context_ale_set_connection_lazy_sd_evaluation"></span>**Verbindung mit dem WPM- \_ Kontext- \_ Satz- \_ Satz \_ \_ erfordert \_ IPSec- \_ Sicherheit, swpm- \_ Kontext- \_ \_ mset-Verbindung verzögert \_ \_ \_ SD \_ Evaluation**</span><span class="sxs-lookup"><span data-stu-id="324b8-110"><span id="FWPM_CONTEXT_ALE_SET_CONNECTION_REQUIRE_IPSEC_SECURITY__FWPM_CONTEXT_ALE_SET_CONNECTION_LAZY_SD_EVALUATION"></span><span id="fwpm_context_ale_set_connection_require_ipsec_security__fwpm_context_ale_set_connection_lazy_sd_evaluation"></span>**FWPM\_CONTEXT\_ALE\_SET\_CONNECTION\_REQUIRE\_IPSEC\_SECURITY, FWPM\_CONTEXT\_ALE\_SET\_CONNECTION\_LAZY\_SD\_EVALUATION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="324b8-111">Filter Kontexte, die in der ALE-Verbindungs Ebene verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="324b8-111">Filter contexts used in the ALE connect layer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="324b8-112"><span id="FWPM_CONTEXT_ALE_SET_CONNECTION_REQUIRE_IPSEC_ENCRYPTION__FWPM_CONTEXT_ALE_SET_CONNECTION_ALLOW_FIRST_INBOUND_PKT_UNENCRYPTED__FWPM_CONTEXT_ALE_ALLOW_AUTH_FW"></span><span id="fwpm_context_ale_set_connection_require_ipsec_encryption__fwpm_context_ale_set_connection_allow_first_inbound_pkt_unencrypted__fwpm_context_ale_allow_auth_fw"></span>**die Verbindung mit dem WPM-Kontext für die Verbindungs Herstellung erfordert die IPSec-Verschlüsselung, die Verbindung des WPM-Kontext-e-in- \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ Verbindung zulassen des \_ \_ ersten eingehenden \_ \_ Pkt \_ unverschlüsselt \_ \_ \_ \_ \_ .**</span><span class="sxs-lookup"><span data-stu-id="324b8-112"><span id="FWPM_CONTEXT_ALE_SET_CONNECTION_REQUIRE_IPSEC_ENCRYPTION__FWPM_CONTEXT_ALE_SET_CONNECTION_ALLOW_FIRST_INBOUND_PKT_UNENCRYPTED__FWPM_CONTEXT_ALE_ALLOW_AUTH_FW"></span><span id="fwpm_context_ale_set_connection_require_ipsec_encryption__fwpm_context_ale_set_connection_allow_first_inbound_pkt_unencrypted__fwpm_context_ale_allow_auth_fw"></span>**FWPM\_CONTEXT\_ALE\_SET\_CONNECTION\_REQUIRE\_IPSEC\_ENCRYPTION, FWPM\_CONTEXT\_ALE\_SET\_CONNECTION\_ALLOW\_FIRST\_INBOUND\_PKT\_UNENCRYPTED, FWPM\_CONTEXT\_ALE\_ALLOW\_AUTH\_FW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="324b8-113">Filter Kontexte, die in der ALE Connect-oder Accept-Ebene verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="324b8-113">Filter contexts used in the ALE connect or accept layer.</span></span>

> [!Note]  
> <span data-ttu-id="324b8-114">Verwenden Sie für Windows 7 den **Kontext- \_ WLAN-Satz Verbindung mit dem \_ \_ \_ \_ \_ ersten \_ eingehenden \_ Pkt \_ zulassen** , oder verwenden Sie den **swpm-Kontext, um \_ \_ \_ \_ auth \_ FW zuzulassen**.</span><span class="sxs-lookup"><span data-stu-id="324b8-114">For Windows 7, use **FWPM\_CONTEXT\_ALE\_SET\_CONNECTION\_ALLOW\_FIRST\_INBOUND\_PKT\_UNENCRYPTED** or **FWPM\_CONTEXT\_ALE\_ALLOW\_AUTH\_FW**.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="324b8-115"><span id="FWPM_CONTEXT_TCP_CHIMNEY_OFFLOAD_ENABLE__FWPM_CONTEXT_TCP_CHIMNEY_OFFLOAD_DISABLE"></span><span id="fwpm_context_tcp_chimney_offload_enable__fwpm_context_tcp_chimney_offload_disable"></span>**f/a- \_ Kontext der TCP-Chimney- \_ \_ \_ Abladung \_ aktivieren, swpm- \_ Kontext \_ TCP \_ Chimney \_ Offload \_ Deaktivieren**</span><span class="sxs-lookup"><span data-stu-id="324b8-115"><span id="FWPM_CONTEXT_TCP_CHIMNEY_OFFLOAD_ENABLE__FWPM_CONTEXT_TCP_CHIMNEY_OFFLOAD_DISABLE"></span><span id="fwpm_context_tcp_chimney_offload_enable__fwpm_context_tcp_chimney_offload_disable"></span>**FWPM\_CONTEXT\_TCP\_CHIMNEY\_OFFLOAD\_ENABLE, FWPM\_CONTEXT\_TCP\_CHIMNEY\_OFFLOAD\_DISABLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="324b8-116">Kontexte, die von den TCP-Chimney-Ablade Aufrufen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="324b8-116">Contexts used by the TCP Chimney Offload callouts.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="324b8-117"><span id="FWPM_CONTEXT_RPC_AUDIT_ENABLED"></span><span id="fwpm_context_rpc_audit_enabled"></span>**WPM- \_ Kontext-RPC-Überwachung \_ \_ \_ aktiviert**</span><span class="sxs-lookup"><span data-stu-id="324b8-117"><span id="FWPM_CONTEXT_RPC_AUDIT_ENABLED"></span><span id="fwpm_context_rpc_audit_enabled"></span>**FWPM\_CONTEXT\_RPC\_AUDIT\_ENABLED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="324b8-118">In der RPC-Überwachungs Unterschicht verwendete Kontexte.</span><span class="sxs-lookup"><span data-stu-id="324b8-118">Contexts used in the RPC audit sublayer.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="324b8-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="324b8-119">Requirements</span></span>



| <span data-ttu-id="324b8-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="324b8-120">Requirement</span></span> | <span data-ttu-id="324b8-121">Wert</span><span class="sxs-lookup"><span data-stu-id="324b8-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="324b8-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="324b8-122">Minimum supported client</span></span><br/> | <span data-ttu-id="324b8-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="324b8-123">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="324b8-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="324b8-124">Minimum supported server</span></span><br/> | <span data-ttu-id="324b8-125">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="324b8-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="324b8-126">Header</span><span class="sxs-lookup"><span data-stu-id="324b8-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="324b8-127"><dt>"F"</dt></span><span class="sxs-lookup"><span data-stu-id="324b8-127"><dt>Fwpmu.h</dt></span></span> </dl> |



 

 





