---
title: Checkapplicabilitymethod-Methode der MDM_WindowsLicensing-Klasse
description: Überprüft, ob der eingegebene Product Key für ein Editions Upgrade, eine Aktivierung oder Änderung einer Product Key von Windows 10 für Desktop Geräte verwendet werden kann. Siehe auch Check Anwendbarkeit.
ms.assetid: b28ea397-72dd-4c10-a9fb-53087c3b654c
keywords:
- Checkapplicabilitymethod-Methode
- Checkapplicabilitymethod-Methode, MDM_WindowsLicensing-Klasse
- MDM_WindowsLicensing-Klasse, checkapplicabilitymethod-Methode
topic_type:
- apiref
api_name:
- MDM_WindowsLicensing.CheckApplicabilityMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eae08c4a13d036a7d1185a3d53dee846ea460e53
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104942"
---
# <a name="checkapplicabilitymethod-method-of-the-mdm_windowslicensing-class"></a><span data-ttu-id="6ff8e-107">Checkapplicabilitymethod-Methode der MDM \_ windowslicensing-Klasse</span><span class="sxs-lookup"><span data-stu-id="6ff8e-107">CheckApplicabilityMethod method of the MDM\_WindowsLicensing class</span></span>

<span data-ttu-id="6ff8e-108">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="6ff8e-108">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="6ff8e-109">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="6ff8e-109">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="6ff8e-110">Überprüft, ob der eingegebene Product Key für ein Editions Upgrade, eine Aktivierung oder Änderung einer Product Key von Windows 10 für Desktop Geräte verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="6ff8e-110">Checks if the entered product key can be used for an edition upgrade, activation or changing a product key of Windows 10 for desktop devices.</span></span> <span data-ttu-id="6ff8e-111">Siehe auch [Check Anwendbarkeit](/windows/client-management/mdm/windowslicensing-csp).</span><span class="sxs-lookup"><span data-stu-id="6ff8e-111">See also, [CheckApplicability](/windows/client-management/mdm/windowslicensing-csp).</span></span>

## <a name="syntax"></a><span data-ttu-id="6ff8e-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="6ff8e-112">Syntax</span></span>


```mof
uint32 CheckApplicabilityMethod(
  [in] string param
);
```



## <a name="parameters"></a><span data-ttu-id="6ff8e-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="6ff8e-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ff8e-114">*param* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6ff8e-114">*param* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ff8e-115">Der Product Key.</span><span class="sxs-lookup"><span data-stu-id="6ff8e-115">The product key.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ff8e-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6ff8e-116">Return value</span></span>

<span data-ttu-id="6ff8e-117">TRUE oder FALSE</span><span class="sxs-lookup"><span data-stu-id="6ff8e-117">TRUE or FALSE</span></span>

## <a name="requirements"></a><span data-ttu-id="6ff8e-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6ff8e-118">Requirements</span></span>



| <span data-ttu-id="6ff8e-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6ff8e-119">Requirement</span></span> | <span data-ttu-id="6ff8e-120">Wert</span><span class="sxs-lookup"><span data-stu-id="6ff8e-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ff8e-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6ff8e-121">Minimum supported client</span></span><br/> | <span data-ttu-id="6ff8e-122">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6ff8e-122">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6ff8e-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6ff8e-123">Minimum supported server</span></span><br/> | <span data-ttu-id="6ff8e-124">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="6ff8e-124">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="6ff8e-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="6ff8e-125">Namespace</span></span><br/>                | <span data-ttu-id="6ff8e-126">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="6ff8e-126">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="6ff8e-127">MOF</span><span class="sxs-lookup"><span data-stu-id="6ff8e-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6ff8e-128"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="6ff8e-128"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="6ff8e-129">DLL</span><span class="sxs-lookup"><span data-stu-id="6ff8e-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6ff8e-130"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6ff8e-130"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ff8e-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6ff8e-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ff8e-132">**MDM- \_ windowslicensing**</span><span class="sxs-lookup"><span data-stu-id="6ff8e-132">**MDM\_WindowsLicensing**</span></span>](mdm-windowslicensing.md)
</dt> <dt>

[<span data-ttu-id="6ff8e-133">Verwenden von PowerShell-Skripts mit dem WMI-Bridge Anbieter</span><span class="sxs-lookup"><span data-stu-id="6ff8e-133">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

