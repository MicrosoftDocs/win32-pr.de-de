---
title: dowipeer Method-Methode der MDM_RemoteWipe-Klasse
description: Hiermit wird das Gerät ausgelöst, um die Remote Löschung zu starten.
ms.assetid: dc25dc09-6a74-4c08-b452-b1d83085bb41
keywords:
- dowipeer Method-Methode
- dowipeer Method-Methode, MDM_RemoteWipe-Klasse
- MDM_RemoteWipe-Klasse, dowipeer Method-Methode
topic_type:
- apiref
api_name:
- MDM_RemoteWipe.doWipeMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f31dcc9dde2fe51ca0d8677df8b27637edd06c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475285"
---
# <a name="dowipemethod-method-of-the-mdm_remotewipe-class"></a><span data-ttu-id="10cd5-106">dowipeer Method-Methode der MDM \_ RemoteWipe-Klasse</span><span class="sxs-lookup"><span data-stu-id="10cd5-106">doWipeMethod method of the MDM\_RemoteWipe class</span></span>

<span data-ttu-id="10cd5-107">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="10cd5-107">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="10cd5-108">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="10cd5-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="10cd5-109">Hiermit wird das Gerät ausgelöst, um die Remote Löschung zu starten.</span><span class="sxs-lookup"><span data-stu-id="10cd5-109">Triggers the device to start the remote wipe.</span></span> <span data-ttu-id="10cd5-110">Siehe auch [dowipe](/windows/client-management/mdm/remotewipe-csp).</span><span class="sxs-lookup"><span data-stu-id="10cd5-110">See also, [doWipe](/windows/client-management/mdm/remotewipe-csp).</span></span>

## <a name="syntax"></a><span data-ttu-id="10cd5-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="10cd5-111">Syntax</span></span>


```mof
uint32 doWipeMethod(
  [in] string param
);
```



## <a name="parameters"></a><span data-ttu-id="10cd5-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="10cd5-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10cd5-113">*param* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="10cd5-113">*param* \[in\]</span></span>
<span data-ttu-id="10cd5-114"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="10cd5-114"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="10cd5-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="10cd5-115">Requirements</span></span>



| <span data-ttu-id="10cd5-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="10cd5-116">Requirement</span></span> | <span data-ttu-id="10cd5-117">Wert</span><span class="sxs-lookup"><span data-stu-id="10cd5-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10cd5-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="10cd5-118">Minimum supported client</span></span><br/> | <span data-ttu-id="10cd5-119">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="10cd5-119">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="10cd5-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="10cd5-120">Minimum supported server</span></span><br/> | <span data-ttu-id="10cd5-121">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="10cd5-121">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="10cd5-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="10cd5-122">Namespace</span></span><br/>                | <span data-ttu-id="10cd5-123">Root \\ CIMv2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="10cd5-123">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="10cd5-124">MOF</span><span class="sxs-lookup"><span data-stu-id="10cd5-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="10cd5-125"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="10cd5-125"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="10cd5-126">DLL</span><span class="sxs-lookup"><span data-stu-id="10cd5-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="10cd5-127"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="10cd5-127"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10cd5-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="10cd5-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10cd5-129">**MDM- \_ Remotelöschung**</span><span class="sxs-lookup"><span data-stu-id="10cd5-129">**MDM\_RemoteWipe**</span></span>](mdm-remotewipe.md)
</dt> <dt>

[<span data-ttu-id="10cd5-130">Verwenden von PowerShell-Skripts mit dem WMI-Bridge Anbieter</span><span class="sxs-lookup"><span data-stu-id="10cd5-130">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

