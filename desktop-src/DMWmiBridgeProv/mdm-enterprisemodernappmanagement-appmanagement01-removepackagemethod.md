---
title: Removepackagemethod-Methode der MDM_EnterpriseModernAppManagement_AppManagement01-Klasse
description: Methode zum Entfernen von Paketen. Siehe auch RemovePackage.
ms.assetid: 0f48fd9c-5a3f-48e5-a954-e937e79af049
keywords:
- Removepackagemethod-Methode
- Removepackagemethod-Methode, MDM_EnterpriseModernAppManagement_AppManagement01-Klasse
- MDM_EnterpriseModernAppManagement_AppManagement01-Klasse, removepackagemethod-Methode
topic_type:
- apiref
api_name:
- MDM_EnterpriseModernAppManagement_AppManagement01.RemovePackageMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c2cdeb2c1a8dfaebdde73e52b2910da180b638c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106343865"
---
# <a name="removepackagemethod-method-of-the-mdm_enterprisemodernappmanagement_appmanagement01-class"></a><span data-ttu-id="0c3d7-107">Removepackagemethod-Methode der MDM \_ enterprismodernappmanagement \_ AppManagement01-Klasse</span><span class="sxs-lookup"><span data-stu-id="0c3d7-107">RemovePackageMethod method of the MDM\_EnterpriseModernAppManagement\_AppManagement01 class</span></span>

<span data-ttu-id="0c3d7-108">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="0c3d7-108">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="0c3d7-109">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="0c3d7-109">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="0c3d7-110">Methode zum Entfernen von Paketen.</span><span class="sxs-lookup"><span data-stu-id="0c3d7-110">Method for removing packages.</span></span> <span data-ttu-id="0c3d7-111">Siehe auch [RemovePackage](/windows/client-management/mdm/enterprisemodernappmanagement-csp).</span><span class="sxs-lookup"><span data-stu-id="0c3d7-111">See also [RemovePackage](/windows/client-management/mdm/enterprisemodernappmanagement-csp).</span></span>

## <a name="syntax"></a><span data-ttu-id="0c3d7-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="0c3d7-112">Syntax</span></span>


```mof
uint32 RemovePackageMethod(
  [in] string param
);
```



## <a name="parameters"></a><span data-ttu-id="0c3d7-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="0c3d7-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c3d7-114">*param* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0c3d7-114">*param* \[in\]</span></span>
<span data-ttu-id="0c3d7-115"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="0c3d7-115"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="0c3d7-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0c3d7-116">Requirements</span></span>



| <span data-ttu-id="0c3d7-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0c3d7-117">Requirement</span></span> | <span data-ttu-id="0c3d7-118">Wert</span><span class="sxs-lookup"><span data-stu-id="0c3d7-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c3d7-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0c3d7-119">Minimum supported client</span></span><br/> | <span data-ttu-id="0c3d7-120">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0c3d7-120">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0c3d7-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0c3d7-121">Minimum supported server</span></span><br/> | <span data-ttu-id="0c3d7-122">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="0c3d7-122">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="0c3d7-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="0c3d7-123">Namespace</span></span><br/>                | <span data-ttu-id="0c3d7-124">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="0c3d7-124">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="0c3d7-125">MOF</span><span class="sxs-lookup"><span data-stu-id="0c3d7-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0c3d7-126"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="0c3d7-126"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="0c3d7-127">DLL</span><span class="sxs-lookup"><span data-stu-id="0c3d7-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0c3d7-128"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0c3d7-128"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0c3d7-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0c3d7-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c3d7-130">**MDM \_ enterprigenmodernappmanagement \_ AppManagement01**</span><span class="sxs-lookup"><span data-stu-id="0c3d7-130">**MDM\_EnterpriseModernAppManagement\_AppManagement01**</span></span>](mdm-enterprisemodernappmanagement-appmanagement01.md)
</dt> </dl>

 

