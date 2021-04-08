---
title: Integrierte Modul Bezeichner für die Schlüssel Erstellung ("f")
description: Die Bezeichner für die Schlüssel, die in die Windows-Filter Plattform (WFP) integriert sind, werden jeweils durch eine GUID dargestellt.
ms.assetid: ba3aaf0f-5524-4d61-bb74-e4714b11b2a9
topic_type:
- apiref
api_name:
- FWPM_KEYING_MODULE_IKE
- FWPM_KEYING_MODULE_IKEV2
- FWPM_KEYING_MODULE_AUTHIP
api_location:
- fwpmu.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc9e6feb726a62de02130d64cef27cd9078395b3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957137"
---
# <a name="built-in-keying-module-identifiers"></a><span data-ttu-id="21cdd-103">Integrierte Schlüssel für das Erstellen von Schlüssel Bezeichner</span><span class="sxs-lookup"><span data-stu-id="21cdd-103">Built-in Keying Module Identifiers</span></span>

<span data-ttu-id="21cdd-104">Die Bezeichner für die Schlüssel, die in die Windows-Filter Plattform (WFP) integriert sind, werden jeweils durch eine GUID dargestellt.</span><span class="sxs-lookup"><span data-stu-id="21cdd-104">The identifiers for the keying modules that are built in to the Windows Filtering Platform (WFP) are each represented by a GUID.</span></span>

<span data-ttu-id="21cdd-105">Diese Bezeichner werden wie folgt definiert.</span><span class="sxs-lookup"><span data-stu-id="21cdd-105">These identifiers are defined as follows.</span></span>

<dl> <dt>

<span data-ttu-id="21cdd-106"><span id="FWPM_KEYING_MODULE_IKE"></span><span id="fwpm_keying_module_ike"></span>**WKE-Modul für die Schlüssel Erstellung \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="21cdd-106"><span id="FWPM_KEYING_MODULE_IKE"></span><span id="fwpm_keying_module_ike"></span>**FWPM\_KEYING\_MODULE\_IKE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="21cdd-107">Internetschlüsselaustausch (IKE)-Schlüssel-Modul.</span><span class="sxs-lookup"><span data-stu-id="21cdd-107">Internet Key Exchange (IKE) keying module.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="21cdd-108"><span id="FWPM_KEYING_MODULE_IKEV2"></span><span id="fwpm_keying_module_ikev2"></span>**Swpm-Schlüssel \_ \_ Modul \_ IKEV2**</span><span class="sxs-lookup"><span data-stu-id="21cdd-108"><span id="FWPM_KEYING_MODULE_IKEV2"></span><span id="fwpm_keying_module_ikev2"></span>**FWPM\_KEYING\_MODULE\_IKEV2**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="21cdd-109">Internetschlüsselaustausch Version 2 (IKEv2)-Schlüssel-Modul.</span><span class="sxs-lookup"><span data-stu-id="21cdd-109">Internet Key Exchange version 2 (IKEv2) keying module.</span></span>

> [!Note]  
> <span data-ttu-id="21cdd-110">Nur unter Windows Server 2008 R2 und Windows 7 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="21cdd-110">Available only on Windows Server 2008 R2 and Windows 7.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="21cdd-111"><span id="FWPM_KEYING_MODULE_AUTHIP"></span><span id="fwpm_keying_module_authip"></span>**das Schlüssel \_ \_ -/verschlüsselermodulmodul \_ AuthIP**</span><span class="sxs-lookup"><span data-stu-id="21cdd-111"><span id="FWPM_KEYING_MODULE_AUTHIP"></span><span id="fwpm_keying_module_authip"></span>**FWPM\_KEYING\_MODULE\_AUTHIP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="21cdd-112">AuthIP-Schlüsselmodul.</span><span class="sxs-lookup"><span data-stu-id="21cdd-112">AuthIP keying module.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="21cdd-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="21cdd-113">Requirements</span></span>



| <span data-ttu-id="21cdd-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="21cdd-114">Requirement</span></span> | <span data-ttu-id="21cdd-115">Wert</span><span class="sxs-lookup"><span data-stu-id="21cdd-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="21cdd-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="21cdd-116">Minimum supported client</span></span><br/> | <span data-ttu-id="21cdd-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="21cdd-117">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="21cdd-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="21cdd-118">Minimum supported server</span></span><br/> | <span data-ttu-id="21cdd-119">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="21cdd-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="21cdd-120">Header</span><span class="sxs-lookup"><span data-stu-id="21cdd-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="21cdd-121"><dt>"F"</dt></span><span class="sxs-lookup"><span data-stu-id="21cdd-121"><dt>Fwpmu.h</dt></span></span> </dl> |



 

 





