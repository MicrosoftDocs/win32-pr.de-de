---
title: Verifyhealthmethod-Methode der MDM_HealthAttestation-Klasse
description: Methode, mit der das Gerät benachrichtigt wird, dass eine Integritäts Zertifikat Überprüfung vorbereitet werden soll. Siehe auch verifyhealth.
ms.assetid: f5b11081-c664-4525-8f36-5f17c21e7f22
keywords:
- Verifyhealthmethod-Methode
- Verifyhealthmethod-Methode, MDM_HealthAttestation-Klasse
- MDM_HealthAttestation-Klasse, verifyhealthmethod-Methode
topic_type:
- apiref
api_name:
- MDM_HealthAttestation.VerifyHealthMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d90d71d3758059706d4ea598e7012433220feb27
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342006"
---
# <a name="verifyhealthmethod-method-of-the-mdm_healthattestation-class"></a><span data-ttu-id="548e1-107">Verifyhealthmethod-Methode der MDM \_ healthattestation-Klasse</span><span class="sxs-lookup"><span data-stu-id="548e1-107">VerifyHealthMethod method of the MDM\_HealthAttestation class</span></span>

<span data-ttu-id="548e1-108">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="548e1-108">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="548e1-109">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="548e1-109">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="548e1-110">Methode, mit der das Gerät benachrichtigt wird, dass eine Integritäts Zertifikat Überprüfung vorbereitet werden soll.</span><span class="sxs-lookup"><span data-stu-id="548e1-110">Method to notify the device to prepare a health certificate verification request.</span></span> <span data-ttu-id="548e1-111">Siehe auch [verifyhealth](/windows/client-management/mdm/healthattestation-csp).</span><span class="sxs-lookup"><span data-stu-id="548e1-111">See also, [VerifyHealth](/windows/client-management/mdm/healthattestation-csp).</span></span>

## <a name="syntax"></a><span data-ttu-id="548e1-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="548e1-112">Syntax</span></span>


```mof
uint32 VerifyHealthMethod();
```



## <a name="parameters"></a><span data-ttu-id="548e1-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="548e1-113">Parameters</span></span>

<span data-ttu-id="548e1-114">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="548e1-114">This method has no parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="548e1-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="548e1-115">Requirements</span></span>



| <span data-ttu-id="548e1-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="548e1-116">Requirement</span></span> | <span data-ttu-id="548e1-117">Wert</span><span class="sxs-lookup"><span data-stu-id="548e1-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="548e1-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="548e1-118">Minimum supported client</span></span><br/> | <span data-ttu-id="548e1-119">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="548e1-119">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="548e1-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="548e1-120">Minimum supported server</span></span><br/> | <span data-ttu-id="548e1-121">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="548e1-121">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="548e1-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="548e1-122">Namespace</span></span><br/>                | <span data-ttu-id="548e1-123">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="548e1-123">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="548e1-124">MOF</span><span class="sxs-lookup"><span data-stu-id="548e1-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="548e1-125"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="548e1-125"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="548e1-126">DLL</span><span class="sxs-lookup"><span data-stu-id="548e1-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="548e1-127"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="548e1-127"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="548e1-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="548e1-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="548e1-129">**MDM- \_ healthattestation**</span><span class="sxs-lookup"><span data-stu-id="548e1-129">**MDM\_HealthAttestation**</span></span>](mdm-healthattestation.md)
</dt> <dt>

[<span data-ttu-id="548e1-130">Verwenden von PowerShell-Skripts mit dem WMI-Bridge Anbieter</span><span class="sxs-lookup"><span data-stu-id="548e1-130">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

