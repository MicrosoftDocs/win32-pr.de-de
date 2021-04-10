---
title: Upgradeeditionwithlicenermethod-Methode der MDM_WindowsLicensing-Klasse
description: Methode zum Bereitstellen einer Lizenz für ein Editions Upgrade von Windows 10 Mobile-Geräten. Siehe auch Upgrade editionwithlicense.
ms.assetid: 1a57fb71-eea6-41bf-bc44-6d3a816096a4
keywords:
- Upgradeeditionwithlicenermethod-Methode
- Upgradeeditionwithlicenermethod-Methode, MDM_WindowsLicensing-Klasse
- MDM_WindowsLicensing-Klasse, upgradeeditionwithlicenermethod-Methode
topic_type:
- apiref
api_name:
- MDM_WindowsLicensing.UpgradeEditionWithLicenseMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b336ee4128aa520ecd463c3607254526c7c3dc7d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956855"
---
# <a name="upgradeeditionwithlicensemethod-method-of-the-mdm_windowslicensing-class"></a><span data-ttu-id="cc3b2-107">Upgradeeditionwithlicenermethod-Methode der MDM- \_ windowslicensing-Klasse</span><span class="sxs-lookup"><span data-stu-id="cc3b2-107">UpgradeEditionWithLicenseMethod method of the MDM\_WindowsLicensing class</span></span>

<span data-ttu-id="cc3b2-108">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="cc3b2-108">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="cc3b2-109">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="cc3b2-109">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="cc3b2-110">Methode zum Bereitstellen einer Lizenz für ein Editions Upgrade von Windows 10 Mobile-Geräten.</span><span class="sxs-lookup"><span data-stu-id="cc3b2-110">Method for providing a license for an edition upgrade of Windows 10 mobile devices.</span></span> <span data-ttu-id="cc3b2-111">Siehe auch [Upgrade editionwithlicense](/windows/client-management/mdm/windowslicensing-csp).</span><span class="sxs-lookup"><span data-stu-id="cc3b2-111">See also, [UpgradeEditionWithLicense](/windows/client-management/mdm/windowslicensing-csp).</span></span>

## <a name="syntax"></a><span data-ttu-id="cc3b2-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="cc3b2-112">Syntax</span></span>


```mof
uint32 UpgradeEditionWithLicenseMethod(
  [in] string param
);
```



## <a name="parameters"></a><span data-ttu-id="cc3b2-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="cc3b2-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc3b2-114">*param* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cc3b2-114">*param* \[in\]</span></span>
<span data-ttu-id="cc3b2-115"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="cc3b2-115"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="cc3b2-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cc3b2-116">Requirements</span></span>



| <span data-ttu-id="cc3b2-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cc3b2-117">Requirement</span></span> | <span data-ttu-id="cc3b2-118">Wert</span><span class="sxs-lookup"><span data-stu-id="cc3b2-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc3b2-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cc3b2-119">Minimum supported client</span></span><br/> | <span data-ttu-id="cc3b2-120">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cc3b2-120">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="cc3b2-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cc3b2-121">Minimum supported server</span></span><br/> | <span data-ttu-id="cc3b2-122">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="cc3b2-122">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="cc3b2-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="cc3b2-123">Namespace</span></span><br/>                | <span data-ttu-id="cc3b2-124">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="cc3b2-124">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="cc3b2-125">MOF</span><span class="sxs-lookup"><span data-stu-id="cc3b2-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cc3b2-126"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="cc3b2-126"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="cc3b2-127">DLL</span><span class="sxs-lookup"><span data-stu-id="cc3b2-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cc3b2-128"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cc3b2-128"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc3b2-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cc3b2-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc3b2-130">**MDM- \_ windowslicensing**</span><span class="sxs-lookup"><span data-stu-id="cc3b2-130">**MDM\_WindowsLicensing**</span></span>](mdm-windowslicensing.md)
</dt> <dt>

[<span data-ttu-id="cc3b2-131">Verwenden von PowerShell-Skripts mit dem WMI-Bridge Anbieter</span><span class="sxs-lookup"><span data-stu-id="cc3b2-131">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

