---
title: Addlicenermethod-Methode der MDM_EnterpriseModernAppManagement_StoreLicenses02_01-Klasse
description: Methode zum Hinzufügen einer Lizenz. Siehe auch addlicense.
ms.assetid: 325d284d-10ac-4786-8b04-8184ac43b53f
keywords:
- Addlicengmethod-Methode
- Addlicenermethod-Methode, MDM_EnterpriseModernAppManagement_StoreLicenses02_01-Klasse
- MDM_EnterpriseModernAppManagement_StoreLicenses02_01-Klasse, addlicenermethod-Methode
topic_type:
- apiref
api_name:
- MDM_EnterpriseModernAppManagement_StoreLicenses02_01.AddLicenseMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87f104f4e74d0200cc9d00b9f116232aa5308738
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106344083"
---
# <a name="addlicensemethod-method-of-the-mdm_enterprisemodernappmanagement_storelicenses02_01-class"></a><span data-ttu-id="1b82b-107">Addlicenermethod-Methode der MDM \_ enterprismodernappmanagement \_ StoreLicenses02 \_ 01-Klasse</span><span class="sxs-lookup"><span data-stu-id="1b82b-107">AddLicenseMethod method of the MDM\_EnterpriseModernAppManagement\_StoreLicenses02\_01 class</span></span>

<span data-ttu-id="1b82b-108">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="1b82b-108">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="1b82b-109">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="1b82b-109">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="1b82b-110">Methode zum Hinzufügen einer Lizenz.</span><span class="sxs-lookup"><span data-stu-id="1b82b-110">Method for adding license.</span></span> <span data-ttu-id="1b82b-111">Siehe auch [addlicense](/windows/client-management/mdm/enterprisemodernappmanagement-csp).</span><span class="sxs-lookup"><span data-stu-id="1b82b-111">See also, [AddLicense](/windows/client-management/mdm/enterprisemodernappmanagement-csp).</span></span>

## <a name="syntax"></a><span data-ttu-id="1b82b-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="1b82b-112">Syntax</span></span>


```mof
uint32 AddLicenseMethod(
  [in] string param
);
```



## <a name="parameters"></a><span data-ttu-id="1b82b-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="1b82b-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b82b-114">*param* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1b82b-114">*param* \[in\]</span></span>
<span data-ttu-id="1b82b-115"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="1b82b-115"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="1b82b-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1b82b-116">Requirements</span></span>



| <span data-ttu-id="1b82b-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1b82b-117">Requirement</span></span> | <span data-ttu-id="1b82b-118">Wert</span><span class="sxs-lookup"><span data-stu-id="1b82b-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b82b-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1b82b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="1b82b-120">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1b82b-120">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1b82b-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1b82b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="1b82b-122">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="1b82b-122">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="1b82b-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="1b82b-123">Namespace</span></span><br/>                | <span data-ttu-id="1b82b-124">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="1b82b-124">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="1b82b-125">MOF</span><span class="sxs-lookup"><span data-stu-id="1b82b-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1b82b-126"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="1b82b-126"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="1b82b-127">DLL</span><span class="sxs-lookup"><span data-stu-id="1b82b-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1b82b-128"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1b82b-128"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1b82b-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1b82b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b82b-130">**MDM \_ enterprinappmanagement \_ StoreLicenses02 \_ 01**</span><span class="sxs-lookup"><span data-stu-id="1b82b-130">**MDM\_EnterpriseModernAppManagement\_StoreLicenses02\_01**</span></span>](mdm-enterprisemodernappmanagement-storelicenses02-01.md)
</dt> <dt>

[<span data-ttu-id="1b82b-131">Verwenden von PowerShell-Skripts mit dem WMI-Bridge Anbieter</span><span class="sxs-lookup"><span data-stu-id="1b82b-131">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

