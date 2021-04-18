---
title: IPSec-Funktionen
description: IPSec-Funktionen
ms.assetid: db656c58-7776-44c4-a7ce-c38e59b37c74
keywords:
- IPSec-Funktionen der Windows-Filter Plattform-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 261e767888b4581587ee550bf240c929f6db4531
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106338061"
---
# <a name="ipsec-functions"></a><span data-ttu-id="1a8fd-104">IPSec-Funktionen</span><span class="sxs-lookup"><span data-stu-id="1a8fd-104">IPsec Functions</span></span>

<span data-ttu-id="1a8fd-105">Die Funktionen der Windows-Filter Plattform (WFP), die mit der Internet Protokoll Sicherheit (IPSec) interagieren, lauten wie folgt.</span><span class="sxs-lookup"><span data-stu-id="1a8fd-105">The Windows Filtering Platform (WFP) functions that interact with Internet Protocol Security (IPsec) are as follows.</span></span>

-   <span data-ttu-id="1a8fd-106">"F":</span><span class="sxs-lookup"><span data-stu-id="1a8fd-106">FwpmIPsecTunnelAdd:</span></span>
    -   <span data-ttu-id="1a8fd-107">[**FwpmIPsecTunnelAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneladd0) (Windows Vista)</span><span class="sxs-lookup"><span data-stu-id="1a8fd-107">[**FwpmIPsecTunnelAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneladd0) (Windows Vista)</span></span>
    -   <span data-ttu-id="1a8fd-108">[**FwpmIPsecTunnelAdd1**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneladd1) (Windows 7)</span><span class="sxs-lookup"><span data-stu-id="1a8fd-108">[**FwpmIPsecTunnelAdd1**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneladd1) (Windows 7)</span></span>
    -   <span data-ttu-id="1a8fd-109">[**FwpmIPsecTunnelAdd2**](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmipsectunneladd2) (Windows 8)</span><span class="sxs-lookup"><span data-stu-id="1a8fd-109">[**FwpmIPsecTunnelAdd2**](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmipsectunneladd2) (Windows 8)</span></span>
-   [<span data-ttu-id="1a8fd-110">**FwpmIPsecTunnelDeleteByKey0**</span><span class="sxs-lookup"><span data-stu-id="1a8fd-110">**FwpmIPsecTunnelDeleteByKey0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneldeletebykey0)
-   [<span data-ttu-id="1a8fd-111">**IPSec-Schlüssel- \_ \_ Manager- \_ Schlüssel \_ Diktat \_ CHECK0**</span><span class="sxs-lookup"><span data-stu-id="1a8fd-111">**IPSEC\_KEY\_MANAGER\_KEY\_DICTATION\_CHECK0**</span></span>](/windows/desktop/api/Fwpmu/nc-fwpmu-ipsec_key_manager_key_dictation_check0)
-   [<span data-ttu-id="1a8fd-112">**IPSec- \_ Schlüssel- \_ Manager \_ \_ Key0 vorschreiben**</span><span class="sxs-lookup"><span data-stu-id="1a8fd-112">**IPSEC\_KEY\_MANAGER\_DICTATE\_KEY0**</span></span>](/windows/desktop/api/Fwpmu/nc-fwpmu-ipsec_key_manager_dictate_key0)
-   [<span data-ttu-id="1a8fd-113">**IPSec- \_ Schlüssel- \_ Manager \_ Benachrichtigen \_ Key0**</span><span class="sxs-lookup"><span data-stu-id="1a8fd-113">**IPSEC\_KEY\_MANAGER\_NOTIFY\_KEY0**</span></span>](/windows/desktop/api/fwpmu/nc-fwpmu-ipsec_key_manager_notify_key0)
-   [<span data-ttu-id="1a8fd-114">**IPSec- \_ sa- \_ Kontext \_ CALLBACK0**</span><span class="sxs-lookup"><span data-stu-id="1a8fd-114">**IPSEC\_SA\_CONTEXT\_CALLBACK0**</span></span>](/windows/win32/api/fwpmu/nc-fwpmu-ipsec_sa_context_callback0)
-   [<span data-ttu-id="1a8fd-115">**IPsecDospGetSecurityInfo0**</span><span class="sxs-lookup"><span data-stu-id="1a8fd-115">**IPsecDospGetSecurityInfo0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecdospgetsecurityinfo0)
-   [<span data-ttu-id="1a8fd-116">**IPsecDospGetStatistics0**</span><span class="sxs-lookup"><span data-stu-id="1a8fd-116">**IPsecDospGetStatistics0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecdospgetstatistics0)
-   [<span data-ttu-id="1a8fd-117">**IPsecDospSetSecurityInfo0**</span><span class="sxs-lookup"><span data-stu-id="1a8fd-117">**IPsecDospSetSecurityInfo0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecdospsetsecurityinfo0)
-   [<span data-ttu-id="1a8fd-118">**IPsecDospStateCreateEnumHandle0**</span><span class="sxs-lookup"><span data-stu-id="1a8fd-118">**IPsecDospStateCreateEnumHandle0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecdospstatecreateenumhandle0)
-   [<span data-ttu-id="1a8fd-119">**IPsecDospStateDestroyEnumHandle0**</span><span class="sxs-lookup"><span data-stu-id="1a8fd-119">**IPsecDospStateDestroyEnumHandle0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecdospstatedestroyenumhandle0)
-   [<span data-ttu-id="1a8fd-120">**IPsecDospStateEnum0**</span><span class="sxs-lookup"><span data-stu-id="1a8fd-120">**IPsecDospStateEnum0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecdospstateenum0)
-   <span data-ttu-id="1a8fd-121">Ipsecgetstatistics:</span><span class="sxs-lookup"><span data-stu-id="1a8fd-121">IPsecGetStatistics:</span></span>
    -   <span data-ttu-id="1a8fd-122">[**IPsecGetStatistics0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecgetstatistics0) (Windows Vista)</span><span class="sxs-lookup"><span data-stu-id="1a8fd-122">[**IPsecGetStatistics0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecgetstatistics0) (Windows Vista)</span></span>
    -   <span data-ttu-id="1a8fd-123">[**IPsecGetStatistics1**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecgetstatistics1) (Windows 7 und höher)</span><span class="sxs-lookup"><span data-stu-id="1a8fd-123">[**IPsecGetStatistics1**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecgetstatistics1) (Windows 7 and later)</span></span>
-   [<span data-ttu-id="1a8fd-124">**IPsecKeyManagerAddAndRegister0**</span><span class="sxs-lookup"><span data-stu-id="1a8fd-124">**IPsecKeyManagerAddAndRegister0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipseckeymanageraddandregister0)
-   [<span data-ttu-id="1a8fd-125">**IPsecKeyManagersGet0**</span><span class="sxs-lookup"><span data-stu-id="1a8fd-125">**IPsecKeyManagersGet0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipseckeymanagersget0)
-   [<span data-ttu-id="1a8fd-126">**IPsecKeyManagerGetSecurityInfoByKey0**</span><span class="sxs-lookup"><span data-stu-id="1a8fd-126">**IPsecKeyManagerGetSecurityInfoByKey0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipseckeymanagergetsecurityinfobykey0)
-   [<span data-ttu-id="1a8fd-127">**IPsecKeyManagerSetSecurityInfoByKey0**</span><span class="sxs-lookup"><span data-stu-id="1a8fd-127">**IPsecKeyManagerSetSecurityInfoByKey0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipseckeymanagersetsecurityinfobykey0)
-   [<span data-ttu-id="1a8fd-128">**IPsecKeyManagerUnregisterAndDelete0**</span><span class="sxs-lookup"><span data-stu-id="1a8fd-128">**IPsecKeyManagerUnregisterAndDelete0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipseckeymanagerunregisteranddelete0)
-   <span data-ttu-id="1a8fd-129">Ipsecsacontextaddinbound:</span><span class="sxs-lookup"><span data-stu-id="1a8fd-129">IPsecSaContextAddInbound:</span></span>
    -   <span data-ttu-id="1a8fd-130">[**IPsecSaContextAddInbound0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddinbound0) (Windows Vista)</span><span class="sxs-lookup"><span data-stu-id="1a8fd-130">[**IPsecSaContextAddInbound0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddinbound0) (Windows Vista)</span></span>
    -   <span data-ttu-id="1a8fd-131">[**IPsecSaContextAddInbound1**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddinbound1) (Windows 7 und höher)</span><span class="sxs-lookup"><span data-stu-id="1a8fd-131">[**IPsecSaContextAddInbound1**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddinbound1) (Windows 7 and later)</span></span>
-   <span data-ttu-id="1a8fd-132">Ipsecsacontextaddoutbound:</span><span class="sxs-lookup"><span data-stu-id="1a8fd-132">IPsecSaContextAddOutbound:</span></span>
    -   <span data-ttu-id="1a8fd-133">[**IPsecSaContextAddOutbound0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddoutbound0) (Windows Vista)</span><span class="sxs-lookup"><span data-stu-id="1a8fd-133">[**IPsecSaContextAddOutbound0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddoutbound0) (Windows Vista)</span></span>
    -   <span data-ttu-id="1a8fd-134">[**IPsecSaContextAddOutbound1**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddoutbound1) (Windows 7 und höher)</span><span class="sxs-lookup"><span data-stu-id="1a8fd-134">[**IPsecSaContextAddOutbound1**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddoutbound1) (Windows 7 and later)</span></span>
-   <span data-ttu-id="1a8fd-135">Ipsecsacontextcreate:</span><span class="sxs-lookup"><span data-stu-id="1a8fd-135">IPsecSaContextCreate:</span></span>
    -   <span data-ttu-id="1a8fd-136">[**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0) (Windows Vista)</span><span class="sxs-lookup"><span data-stu-id="1a8fd-136">[**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0) (Windows Vista)</span></span>
    -   <span data-ttu-id="1a8fd-137">[**IPsecSaContextCreate1**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate1) (Windows 7 und höher)</span><span class="sxs-lookup"><span data-stu-id="1a8fd-137">[**IPsecSaContextCreate1**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate1) (Windows 7 and later)</span></span>
-   [<span data-ttu-id="1a8fd-138">**IPsecSaContextCreateEnumHandle0**</span><span class="sxs-lookup"><span data-stu-id="1a8fd-138">**IPsecSaContextCreateEnumHandle0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreateenumhandle0)
-   [<span data-ttu-id="1a8fd-139">**IPsecSaContextDeleteById0**</span><span class="sxs-lookup"><span data-stu-id="1a8fd-139">**IPsecSaContextDeleteById0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextdeletebyid0)
-   [<span data-ttu-id="1a8fd-140">**IPsecSaContextDestroyEnumHandle0**</span><span class="sxs-lookup"><span data-stu-id="1a8fd-140">**IPsecSaContextDestroyEnumHandle0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextdestroyenumhandle0)
-   <span data-ttu-id="1a8fd-141">Ipsecsacontextenum:</span><span class="sxs-lookup"><span data-stu-id="1a8fd-141">IPsecSaContextEnum:</span></span>
    -   <span data-ttu-id="1a8fd-142">[**IPsecSaContextEnum0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextenum0) (Windows Vista)</span><span class="sxs-lookup"><span data-stu-id="1a8fd-142">[**IPsecSaContextEnum0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextenum0) (Windows Vista)</span></span>
    -   <span data-ttu-id="1a8fd-143">[**IPsecSaContextEnum1**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextenum1) (Windows 7 und höher)</span><span class="sxs-lookup"><span data-stu-id="1a8fd-143">[**IPsecSaContextEnum1**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextenum1) (Windows 7 and later)</span></span>
-   [<span data-ttu-id="1a8fd-144">**IPsecSaContextExpire0**</span><span class="sxs-lookup"><span data-stu-id="1a8fd-144">**IPsecSaContextExpire0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextexpire0)
-   <span data-ttu-id="1a8fd-145">Ipsecsacontextgetbyid:</span><span class="sxs-lookup"><span data-stu-id="1a8fd-145">IPsecSaContextGetById:</span></span>
    -   <span data-ttu-id="1a8fd-146">[**IPsecSaContextGetById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetbyid0) (Windows Vista)</span><span class="sxs-lookup"><span data-stu-id="1a8fd-146">[**IPsecSaContextGetById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetbyid0) (Windows Vista)</span></span>
    -   <span data-ttu-id="1a8fd-147">[**IPsecSaContextGetById1**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetbyid1) (Windows 7 und höher)</span><span class="sxs-lookup"><span data-stu-id="1a8fd-147">[**IPsecSaContextGetById1**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetbyid1) (Windows 7 and later)</span></span>
-   <span data-ttu-id="1a8fd-148">Ipsecsacontextgetspi:</span><span class="sxs-lookup"><span data-stu-id="1a8fd-148">IPsecSaContextGetSpi:</span></span>
    -   <span data-ttu-id="1a8fd-149">[**IPsecSaContextGetSpi0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetspi0) (Windows Vista)</span><span class="sxs-lookup"><span data-stu-id="1a8fd-149">[**IPsecSaContextGetSpi0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetspi0) (Windows Vista)</span></span>
    -   <span data-ttu-id="1a8fd-150">[**IPsecSaContextGetSpi1**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetspi1) (Windows 7 und höher)</span><span class="sxs-lookup"><span data-stu-id="1a8fd-150">[**IPsecSaContextGetSpi1**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetspi1) (Windows 7 and later)</span></span>
-   [<span data-ttu-id="1a8fd-151">**IPsecSaContextSetSpi0**</span><span class="sxs-lookup"><span data-stu-id="1a8fd-151">**IPsecSaContextSetSpi0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextsetspi0)
-   [<span data-ttu-id="1a8fd-152">**IPsecSaContextSubscribe0**</span><span class="sxs-lookup"><span data-stu-id="1a8fd-152">**IPsecSaContextSubscribe0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextsubscribe0)
-   [<span data-ttu-id="1a8fd-153">**IPsecSaContextSubscriptionsGet0**</span><span class="sxs-lookup"><span data-stu-id="1a8fd-153">**IPsecSaContextSubscriptionsGet0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextsubscriptionsget0)
-   [<span data-ttu-id="1a8fd-154">**IPsecSaContextUpdate0**</span><span class="sxs-lookup"><span data-stu-id="1a8fd-154">**IPsecSaContextUpdate0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextupdate0)
-   [<span data-ttu-id="1a8fd-155">**IPsecSaContextUpdate0**</span><span class="sxs-lookup"><span data-stu-id="1a8fd-155">**IPsecSaContextUpdate0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextupdate0)
-   [<span data-ttu-id="1a8fd-156">**IPsecSaCreateEnumHandle0**</span><span class="sxs-lookup"><span data-stu-id="1a8fd-156">**IPsecSaCreateEnumHandle0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacreateenumhandle0)
-   [<span data-ttu-id="1a8fd-157">**IPsecSaDbGetSecurityInfo0**</span><span class="sxs-lookup"><span data-stu-id="1a8fd-157">**IPsecSaDbGetSecurityInfo0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsadbgetsecurityinfo0)
-   [<span data-ttu-id="1a8fd-158">**IPsecSaDbSetSecurityInfo0**</span><span class="sxs-lookup"><span data-stu-id="1a8fd-158">**IPsecSaDbSetSecurityInfo0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsadbsetsecurityinfo0)
-   [<span data-ttu-id="1a8fd-159">**IPsecSaDestroyEnumHandle0**</span><span class="sxs-lookup"><span data-stu-id="1a8fd-159">**IPsecSaDestroyEnumHandle0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsadestroyenumhandle0)
-   <span data-ttu-id="1a8fd-160">Ipsecsaaufumum:</span><span class="sxs-lookup"><span data-stu-id="1a8fd-160">IPsecSaEnum:</span></span>
    -   <span data-ttu-id="1a8fd-161">[**IPsecSaEnum0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsaenum0) (Windows Vista)</span><span class="sxs-lookup"><span data-stu-id="1a8fd-161">[**IPsecSaEnum0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsaenum0) (Windows Vista)</span></span>
    -   <span data-ttu-id="1a8fd-162">[**IPsecSaEnum1**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsaenum1) (Windows 7 und höher)</span><span class="sxs-lookup"><span data-stu-id="1a8fd-162">[**IPsecSaEnum1**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsaenum1) (Windows 7 and later)</span></span>

 

 