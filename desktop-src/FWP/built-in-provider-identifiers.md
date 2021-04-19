---
title: Integrierte Anbieter Bezeichner ("f")
description: Die Bezeichner für die Anbieter, die in die Windows-Filter Plattform (WFP) integriert sind, werden jeweils durch eine GUID dargestellt.
ms.assetid: 61bc1e2d-f6ee-45db-892f-c49680d27072
topic_type:
- apiref
api_name:
- FWPM_PROVIDER_IKEEXT
- FWPM_PROVIDER_IPSEC_DOS_CONFIG
- FWPM_PROVIDER_TCP_CHIMNEY_OFFLOAD
- FWPM_PROVIDER_TCP_TEMPLATES
api_location:
- fwpmu.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 060f6d63d703d7c91e5538b7bfdd8758ee2e1cde
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106344089"
---
# <a name="built-in-provider-identifiers"></a><span data-ttu-id="319a5-103">Integrierte Anbieter Bezeichner</span><span class="sxs-lookup"><span data-stu-id="319a5-103">Built-in Provider Identifiers</span></span>

<span data-ttu-id="319a5-104">Die Bezeichner für die Anbieter, die in die Windows-Filter Plattform (WFP) integriert sind, werden jeweils durch eine GUID dargestellt.</span><span class="sxs-lookup"><span data-stu-id="319a5-104">The identifiers for the providers that are built in to the Windows Filtering Platform (WFP) are each represented by a GUID.</span></span>

<span data-ttu-id="319a5-105">Diese Bezeichner werden wie folgt definiert.</span><span class="sxs-lookup"><span data-stu-id="319a5-105">These identifiers are defined as follows.</span></span>

<dl> <dt>

<span data-ttu-id="319a5-106"><span id="FWPM_PROVIDER_IKEEXT"></span><span id="fwpm_provider_ikeext"></span>**swpm- \_ Anbieter \_ ikeext**</span><span class="sxs-lookup"><span data-stu-id="319a5-106"><span id="FWPM_PROVIDER_IKEEXT"></span><span id="fwpm_provider_ikeext"></span>**FWPM\_PROVIDER\_IKEEXT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="319a5-107">{10ad9216-CCDE-456c-8b16-e9b04e60a90b}</span><span class="sxs-lookup"><span data-stu-id="319a5-107">{10ad9216-ccde-456c-8b16-e9f04e60a90b}</span></span>
</dt> <dt>



<span data-ttu-id="319a5-108">Wird verwendet, um alle von IKE/AuthIP hinzugefügten Filter zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="319a5-108">Used to identify all the filters added by IKE/AuthIP.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="319a5-109"><span id="FWPM_PROVIDER_IPSEC_DOS_CONFIG"></span><span id="fwpm_provider_ipsec_dos_config"></span>**\_ \_ IPSec- \_ DOS- \_ Konfiguration des WPM-Anbieters**</span><span class="sxs-lookup"><span data-stu-id="319a5-109"><span id="FWPM_PROVIDER_IPSEC_DOS_CONFIG"></span><span id="fwpm_provider_ipsec_dos_config"></span>**FWPM\_PROVIDER\_IPSEC\_DOS\_CONFIG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="319a5-110">{3c6c0519-c05c-4bb9-8338-2327814ce8bf}</span><span class="sxs-lookup"><span data-stu-id="319a5-110">{3c6c0519-c05c-4bb9-8338-2327814ce8bf}</span></span>
</dt> <dt>



<span data-ttu-id="319a5-111">Wird verwendet, um alle vom IPSec-DOS-Schutz hinzugefügten Filter zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="319a5-111">Used to identify all the filters added by IPsec DoS Protection.</span></span>

> [!Note]  
> <span data-ttu-id="319a5-112">Nur unter Windows 7 und Windows Server 2008 R2 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="319a5-112">Available only on Windows 7 and Windows Server 2008 R2.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="319a5-113"><span id="FWPM_PROVIDER_TCP_CHIMNEY_OFFLOAD"></span><span id="fwpm_provider_tcp_chimney_offload"></span>**\_TCP-Chimney- \_ \_ \_ Abladung des WPM-Anbieters**</span><span class="sxs-lookup"><span data-stu-id="319a5-113"><span id="FWPM_PROVIDER_TCP_CHIMNEY_OFFLOAD"></span><span id="fwpm_provider_tcp_chimney_offload"></span>**FWPM\_PROVIDER\_TCP\_CHIMNEY\_OFFLOAD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="319a5-114">{896aa19e-9a34-4bcb-ae79-beb9127c84 B9}</span><span class="sxs-lookup"><span data-stu-id="319a5-114">{896aa19e-9a34-4bcb-ae79-beb9127c84b9}</span></span>
</dt> <dt>



<span data-ttu-id="319a5-115">Dient zum Identifizieren aller von der TCP-Chimney-Abladung hinzugefügten Filter.</span><span class="sxs-lookup"><span data-stu-id="319a5-115">Used to identify all the filters added by TCP Chimney Offload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="319a5-116"><span id="FWPM_PROVIDER_TCP_TEMPLATES"></span><span id="fwpm_provider_tcp_templates"></span>**TCP-Vorlagen für den WPM- \_ Anbieter \_ \_**</span><span class="sxs-lookup"><span data-stu-id="319a5-116"><span id="FWPM_PROVIDER_TCP_TEMPLATES"></span><span id="fwpm_provider_tcp_templates"></span>**FWPM\_PROVIDER\_TCP\_TEMPLATES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="319a5-117">{76cfcd30-3394-432D-bed3-441ae50e63c3}</span><span class="sxs-lookup"><span data-stu-id="319a5-117">{76cfcd30-3394-432d-bed3-441ae50e63c3}</span></span>
</dt> <dt>



<span data-ttu-id="319a5-118">Wird verwendet, um alle von TCP-Vorlagen hinzugefügten Filter zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="319a5-118">Used to identify all the filters added by TCP templates.</span></span>

> [!Note]  
> <span data-ttu-id="319a5-119">Nur unter Windows 8 und Windows Server 2012 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="319a5-119">Available only on Windows 8 and Windows Server 2012.</span></span>

 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="319a5-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="319a5-120">Requirements</span></span>



| <span data-ttu-id="319a5-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="319a5-121">Requirement</span></span> | <span data-ttu-id="319a5-122">Wert</span><span class="sxs-lookup"><span data-stu-id="319a5-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="319a5-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="319a5-123">Minimum supported client</span></span><br/> | <span data-ttu-id="319a5-124">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="319a5-124">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="319a5-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="319a5-125">Minimum supported server</span></span><br/> | <span data-ttu-id="319a5-126">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="319a5-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="319a5-127">Header</span><span class="sxs-lookup"><span data-stu-id="319a5-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="319a5-128"><dt>"F"</dt></span><span class="sxs-lookup"><span data-stu-id="319a5-128"><dt>Fwpmu.h</dt></span></span> </dl> |



 

 





