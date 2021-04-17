---
title: Upgradeeditionwithproductkeymethod-Methode der MDM_WindowsLicensing-Klasse
description: Gibt eine Product Key für ein Editions Upgrade von Windows 10 Desktop-Geräten ein. Siehe auch Upgrade editionwithproductkey.
ms.assetid: 6576fb5c-210c-4979-8c01-ed8f78e72c2c
keywords:
- Upgradeeditionwithproductkeymethod-Methode
- Upgradeeditionwithproductkeymethod-Methode, MDM_WindowsLicensing-Klasse
- MDM_WindowsLicensing-Klasse, upgradeeditionwithproductkeymethod-Methode
topic_type:
- apiref
api_name:
- MDM_WindowsLicensing.UpgradeEditionWithProductKeyMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85824fc6fac9e5a15bf2bc890215afcbd0958680
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478042"
---
# <a name="upgradeeditionwithproductkeymethod-method-of-the-mdm_windowslicensing-class"></a><span data-ttu-id="7bec9-107">Upgradeeditionwithproductkeymethod-Methode der MDM- \_ windowslicensing-Klasse</span><span class="sxs-lookup"><span data-stu-id="7bec9-107">UpgradeEditionWithProductKeyMethod method of the MDM\_WindowsLicensing class</span></span>

<span data-ttu-id="7bec9-108">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="7bec9-108">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="7bec9-109">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="7bec9-109">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="7bec9-110">Gibt eine Product Key für ein Editions Upgrade von Windows 10 Desktop-Geräten ein.</span><span class="sxs-lookup"><span data-stu-id="7bec9-110">Enters a product key for an edition upgrade of Windows 10 desktop devices.</span></span> <span data-ttu-id="7bec9-111">Siehe auch [Upgrade editionwithproductkey](/windows/client-management/mdm/windowslicensing-csp).</span><span class="sxs-lookup"><span data-stu-id="7bec9-111">See also, [UpgradeEditionWithProductKey](/windows/client-management/mdm/windowslicensing-csp).</span></span>

## <a name="syntax"></a><span data-ttu-id="7bec9-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="7bec9-112">Syntax</span></span>


```mof
uint32 UpgradeEditionWithProductKeyMethod(
  [in] string param
);
```



## <a name="parameters"></a><span data-ttu-id="7bec9-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="7bec9-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7bec9-114">*param* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7bec9-114">*param* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7bec9-115">Der Product Key.</span><span class="sxs-lookup"><span data-stu-id="7bec9-115">The product key.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7bec9-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7bec9-116">Requirements</span></span>



| <span data-ttu-id="7bec9-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7bec9-117">Requirement</span></span> | <span data-ttu-id="7bec9-118">Wert</span><span class="sxs-lookup"><span data-stu-id="7bec9-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7bec9-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7bec9-119">Minimum supported client</span></span><br/> | <span data-ttu-id="7bec9-120">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7bec9-120">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7bec9-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7bec9-121">Minimum supported server</span></span><br/> | <span data-ttu-id="7bec9-122">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="7bec9-122">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="7bec9-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="7bec9-123">Namespace</span></span><br/>                | <span data-ttu-id="7bec9-124">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="7bec9-124">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="7bec9-125">MOF</span><span class="sxs-lookup"><span data-stu-id="7bec9-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7bec9-126"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="7bec9-126"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="7bec9-127">DLL</span><span class="sxs-lookup"><span data-stu-id="7bec9-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7bec9-128"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7bec9-128"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7bec9-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7bec9-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7bec9-130">**MDM- \_ windowslicensing**</span><span class="sxs-lookup"><span data-stu-id="7bec9-130">**MDM\_WindowsLicensing**</span></span>](mdm-windowslicensing.md)
</dt> <dt>

[<span data-ttu-id="7bec9-131">Verwenden von PowerShell-Skripts mit dem WMI-Bridge Anbieter</span><span class="sxs-lookup"><span data-stu-id="7bec9-131">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

