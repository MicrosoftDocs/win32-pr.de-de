---
title: Changeproductkeymethod-Methode der MDM_WindowsLicensing-Klasse
description: Mit dieser Methode wird eine Product Key für Windows 10-Desktop Geräte installiert. Punkt nicht neu starten. Siehe auch changeproductkey.
ms.assetid: 1d9e3243-2ca4-427b-bda2-d33e1e70c80d
keywords:
- Changeproductkeymethod-Methode
- Changeproductkeymethod-Methode, MDM_WindowsLicensing-Klasse
- MDM_WindowsLicensing-Klasse, changeproductkeymethod-Methode
topic_type:
- apiref
api_name:
- MDM_WindowsLicensing.ChangeProductKeyMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e00345fb0e23655b457e0540c70289a169c54ea
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478045"
---
# <a name="changeproductkeymethod-method-of-the-mdm_windowslicensing-class"></a><span data-ttu-id="62c97-108">Changeproductkeymethod-Methode der MDM \_ windowslicensing-Klasse</span><span class="sxs-lookup"><span data-stu-id="62c97-108">ChangeProductKeyMethod method of the MDM\_WindowsLicensing class</span></span>

<span data-ttu-id="62c97-109">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="62c97-109">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="62c97-110">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="62c97-110">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="62c97-111">Mit dieser Methode wird eine Product Key für Windows 10-Desktop Geräte installiert.</span><span class="sxs-lookup"><span data-stu-id="62c97-111">This method installs a product key for Windows 10 desktop devices.</span></span> <span data-ttu-id="62c97-112">Punkt nicht neu starten.</span><span class="sxs-lookup"><span data-stu-id="62c97-112">Dot not reboot.</span></span> <span data-ttu-id="62c97-113">Siehe auch [changeproductkey](/windows/client-management/mdm/windowslicensing-csp)</span><span class="sxs-lookup"><span data-stu-id="62c97-113">See also [ChangeProductKey](/windows/client-management/mdm/windowslicensing-csp)</span></span>

## <a name="syntax"></a><span data-ttu-id="62c97-114">Syntax</span><span class="sxs-lookup"><span data-stu-id="62c97-114">Syntax</span></span>


```mof
uint32 ChangeProductKeyMethod(
  [in] string param
);
```



## <a name="parameters"></a><span data-ttu-id="62c97-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="62c97-115">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62c97-116">*param* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="62c97-116">*param* \[in\]</span></span>
<span data-ttu-id="62c97-117"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="62c97-117"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="62c97-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="62c97-118">Requirements</span></span>



| <span data-ttu-id="62c97-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="62c97-119">Requirement</span></span> | <span data-ttu-id="62c97-120">Wert</span><span class="sxs-lookup"><span data-stu-id="62c97-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62c97-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="62c97-121">Minimum supported client</span></span><br/> | <span data-ttu-id="62c97-122">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="62c97-122">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="62c97-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="62c97-123">Minimum supported server</span></span><br/> | <span data-ttu-id="62c97-124">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="62c97-124">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="62c97-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="62c97-125">Namespace</span></span><br/>                | <span data-ttu-id="62c97-126">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="62c97-126">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="62c97-127">MOF</span><span class="sxs-lookup"><span data-stu-id="62c97-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="62c97-128"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="62c97-128"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="62c97-129">DLL</span><span class="sxs-lookup"><span data-stu-id="62c97-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="62c97-130"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="62c97-130"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62c97-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="62c97-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62c97-132">**MDM- \_ windowslicensing**</span><span class="sxs-lookup"><span data-stu-id="62c97-132">**MDM\_WindowsLicensing**</span></span>](mdm-windowslicensing.md)
</dt> </dl>

 

