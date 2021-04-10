---
title: Storeingestallmethod-Methode der MDM_EnterpriseModernAppManagement_AppInstallation01_01-Klasse
description: Methode zum Ausführen einer App-Installation und einer Lizenz aus dem Windows Store. Siehe auch storeingestall.
ms.assetid: 4f8aff47-ad16-4fe5-85be-7ddb55ddff24
keywords:
- Storeingestallmethod-Methode
- Storeingestallmethod-Methode, MDM_EnterpriseModernAppManagement_AppInstallation01_01-Klasse
- MDM_EnterpriseModernAppManagement_AppInstallation01_01-Klasse, storeingestallmethod-Methode
topic_type:
- apiref
api_name:
- MDM_EnterpriseModernAppManagement_AppInstallation01_01.StoreInstallMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c4ae34e8502b7d408a7fb4d96fb9c2c4fadb509
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956865"
---
# <a name="storeinstallmethod-method-of-the-mdm_enterprisemodernappmanagement_appinstallation01_01-class"></a><span data-ttu-id="3a5b9-107">Storeinstallmethod-Methode der MDM \_ enterprismodernappmanagement \_ AppInstallation01 \_ 01-Klasse</span><span class="sxs-lookup"><span data-stu-id="3a5b9-107">StoreInstallMethod method of the MDM\_EnterpriseModernAppManagement\_AppInstallation01\_01 class</span></span>

<span data-ttu-id="3a5b9-108">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="3a5b9-108">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="3a5b9-109">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="3a5b9-109">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="3a5b9-110">Methode zum Ausführen einer App-Installation und einer Lizenz aus dem Windows Store.</span><span class="sxs-lookup"><span data-stu-id="3a5b9-110">Method to perform an install of an app and a license from the Windows Store.</span></span> <span data-ttu-id="3a5b9-111">Siehe auch [storeingestall](/windows/client-management/mdm/enterprisemodernappmanagement-csp).</span><span class="sxs-lookup"><span data-stu-id="3a5b9-111">See also, [StoreInstall](/windows/client-management/mdm/enterprisemodernappmanagement-csp).</span></span>

## <a name="syntax"></a><span data-ttu-id="3a5b9-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="3a5b9-112">Syntax</span></span>


```mof
uint32 StoreInstallMethod(
  [in] string param
);
```



## <a name="parameters"></a><span data-ttu-id="3a5b9-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="3a5b9-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a5b9-114">*param* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3a5b9-114">*param* \[in\]</span></span>
<span data-ttu-id="3a5b9-115"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="3a5b9-115"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="3a5b9-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3a5b9-116">Requirements</span></span>



| <span data-ttu-id="3a5b9-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3a5b9-117">Requirement</span></span> | <span data-ttu-id="3a5b9-118">Wert</span><span class="sxs-lookup"><span data-stu-id="3a5b9-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a5b9-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3a5b9-119">Minimum supported client</span></span><br/> | <span data-ttu-id="3a5b9-120">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3a5b9-120">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3a5b9-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3a5b9-121">Minimum supported server</span></span><br/> | <span data-ttu-id="3a5b9-122">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="3a5b9-122">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="3a5b9-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="3a5b9-123">Namespace</span></span><br/>                | <span data-ttu-id="3a5b9-124">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="3a5b9-124">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="3a5b9-125">MOF</span><span class="sxs-lookup"><span data-stu-id="3a5b9-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3a5b9-126"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="3a5b9-126"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="3a5b9-127">DLL</span><span class="sxs-lookup"><span data-stu-id="3a5b9-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3a5b9-128"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3a5b9-128"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a5b9-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3a5b9-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a5b9-130">**MDM \_ enterprinappmanagement \_ AppInstallation01 \_ 01**</span><span class="sxs-lookup"><span data-stu-id="3a5b9-130">**MDM\_EnterpriseModernAppManagement\_AppInstallation01\_01**</span></span>](mdm-enterprisemodernappmanagement-appinstallation01-01.md)
</dt> <dt>

[<span data-ttu-id="3a5b9-131">Verwenden von PowerShell-Skripts mit dem WMI-Bridge Anbieter</span><span class="sxs-lookup"><span data-stu-id="3a5b9-131">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

