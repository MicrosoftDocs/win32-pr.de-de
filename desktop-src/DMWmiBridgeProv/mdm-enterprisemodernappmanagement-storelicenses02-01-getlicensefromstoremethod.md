---
title: Getlicenabfromstoremethod-Methode der MDM_EnterpriseModernAppManagement_StoreLicenses02_01-Klasse
description: Methode zum erhalten einer Lizenz aus dem Store. Siehe auch "getlicenabfromstore".
ms.assetid: 4cf8a979-60c1-4ec1-968e-5a90cc671ebf
keywords:
- Getlicenabfromstoremethod-Methode
- Getlicenabfromstoremethod-Methode, MDM_EnterpriseModernAppManagement_StoreLicenses02_01-Klasse
- MDM_EnterpriseModernAppManagement_StoreLicenses02_01-Klasse, getlicenabfromstoremethod-Methode
topic_type:
- apiref
api_name:
- MDM_EnterpriseModernAppManagement_StoreLicenses02_01.GetLicenseFromStoreMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8751546bfb57e5c9bf34db97ee6b59dd7e1f580
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104973"
---
# <a name="getlicensefromstoremethod-method-of-the-mdm_enterprisemodernappmanagement_storelicenses02_01-class"></a><span data-ttu-id="cac73-107">Getlicenabfromstoremethod-Methode der MDM \_ enterprismodernappmanagement \_ StoreLicenses02 \_ 01-Klasse</span><span class="sxs-lookup"><span data-stu-id="cac73-107">GetLicenseFromStoreMethod method of the MDM\_EnterpriseModernAppManagement\_StoreLicenses02\_01 class</span></span>

<span data-ttu-id="cac73-108">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="cac73-108">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="cac73-109">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="cac73-109">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="cac73-110">Methode zum erhalten einer Lizenz aus dem Store.</span><span class="sxs-lookup"><span data-stu-id="cac73-110">Method for getting a license from the store.</span></span> <span data-ttu-id="cac73-111">Siehe auch " [getlicenabfromstore](/windows/client-management/mdm/enterprisemodernappmanagement-csp)".</span><span class="sxs-lookup"><span data-stu-id="cac73-111">See also, [GetLicenseFromStore](/windows/client-management/mdm/enterprisemodernappmanagement-csp).</span></span>

## <a name="syntax"></a><span data-ttu-id="cac73-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="cac73-112">Syntax</span></span>


```mof
uint32 GetLicenseFromStoreMethod(
  [in] string param
);
```



## <a name="parameters"></a><span data-ttu-id="cac73-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="cac73-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cac73-114">*param* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cac73-114">*param* \[in\]</span></span>
<span data-ttu-id="cac73-115"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="cac73-115"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="cac73-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cac73-116">Requirements</span></span>



| <span data-ttu-id="cac73-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cac73-117">Requirement</span></span> | <span data-ttu-id="cac73-118">Wert</span><span class="sxs-lookup"><span data-stu-id="cac73-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cac73-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cac73-119">Minimum supported client</span></span><br/> | <span data-ttu-id="cac73-120">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cac73-120">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="cac73-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cac73-121">Minimum supported server</span></span><br/> | <span data-ttu-id="cac73-122">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="cac73-122">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="cac73-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="cac73-123">Namespace</span></span><br/>                | <span data-ttu-id="cac73-124">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="cac73-124">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="cac73-125">MOF</span><span class="sxs-lookup"><span data-stu-id="cac73-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cac73-126"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="cac73-126"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="cac73-127">DLL</span><span class="sxs-lookup"><span data-stu-id="cac73-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cac73-128"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cac73-128"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cac73-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cac73-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cac73-130">**MDM \_ enterprinappmanagement \_ StoreLicenses02 \_ 01**</span><span class="sxs-lookup"><span data-stu-id="cac73-130">**MDM\_EnterpriseModernAppManagement\_StoreLicenses02\_01**</span></span>](mdm-enterprisemodernappmanagement-storelicenses02-01.md)
</dt> <dt>

[<span data-ttu-id="cac73-131">Verwenden von PowerShell-Skripts mit dem WMI-Bridge Anbieter</span><span class="sxs-lookup"><span data-stu-id="cac73-131">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

