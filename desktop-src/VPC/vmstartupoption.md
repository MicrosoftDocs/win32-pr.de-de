---
title: Vmstartupoption-Enumeration (vpccominterfaces. h)
description: Gibt die Startoption an.
ms.assetid: ac4de9a7-7fc7-4361-89dd-e7da8f5dbb92
keywords:
- Vmstartupoption-Enumeration virtueller PC
topic_type:
- apiref
api_name:
- VMStartupOption
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7dc4a3bbcc1c82c57dfe144f818c29b403fd83a5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476539"
---
# <a name="vmstartupoption-enumeration"></a><span data-ttu-id="82601-104">Vmstartupoption-Enumeration</span><span class="sxs-lookup"><span data-stu-id="82601-104">VMStartupOption enumeration</span></span>

<span data-ttu-id="82601-105">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="82601-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="82601-106">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="82601-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="82601-107">Gibt die Startoption an.</span><span class="sxs-lookup"><span data-stu-id="82601-107">Specifies the start-up option.</span></span>

## <a name="syntax"></a><span data-ttu-id="82601-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="82601-108">Syntax</span></span>


```C++
typedef enum  { 
  vmStartupOption_Normal                      = 0,
  vmStartupOption_FixParentTimestampMismatch  = 1
} VMStartupOption;
```



## <a name="constants"></a><span data-ttu-id="82601-109">Konstanten</span><span class="sxs-lookup"><span data-stu-id="82601-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="82601-110"><span id="vmStartupOption_Normal"></span><span id="vmstartupoption_normal"></span><span id="VMSTARTUPOPTION_NORMAL"></span>**vmstartupoption \_ Normal**</span><span class="sxs-lookup"><span data-stu-id="82601-110"><span id="vmStartupOption_Normal"></span><span id="vmstartupoption_normal"></span><span id="VMSTARTUPOPTION_NORMAL"></span>**vmStartupOption\_Normal**</span></span>
</dt> <dd>

<span data-ttu-id="82601-111">Starten Sie normal.</span><span class="sxs-lookup"><span data-stu-id="82601-111">Start normally.</span></span>

</dd> <dt>

<span data-ttu-id="82601-112"><span id="vmStartupOption_FixParentTimestampMismatch"></span><span id="vmstartupoption_fixparenttimestampmismatch"></span><span id="VMSTARTUPOPTION_FIXPARENTTIMESTAMPMISMATCH"></span>**vmstartupoption \_ fixparameenttimestampmismatch**</span><span class="sxs-lookup"><span data-stu-id="82601-112"><span id="vmStartupOption_FixParentTimestampMismatch"></span><span id="vmstartupoption_fixparenttimestampmismatch"></span><span id="VMSTARTUPOPTION_FIXPARENTTIMESTAMPMISMATCH"></span>**vmStartupOption\_FixParentTimestampMismatch**</span></span>
</dt> <dd>

<span data-ttu-id="82601-113">Korrigieren Sie den nicht übereinstimmenden übergeordneten Zeitstempel.</span><span class="sxs-lookup"><span data-stu-id="82601-113">Fix the parent timestamp mismatch.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="82601-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="82601-114">Requirements</span></span>



| <span data-ttu-id="82601-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="82601-115">Requirement</span></span> | <span data-ttu-id="82601-116">Wert</span><span class="sxs-lookup"><span data-stu-id="82601-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="82601-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="82601-117">Minimum supported client</span></span><br/> | <span data-ttu-id="82601-118">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="82601-118">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="82601-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="82601-119">Minimum supported server</span></span><br/> | <span data-ttu-id="82601-120">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="82601-120">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="82601-121">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="82601-121">End of client support</span></span><br/>    | <span data-ttu-id="82601-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="82601-122">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="82601-123">Produkt</span><span class="sxs-lookup"><span data-stu-id="82601-123">Product</span></span><br/>                  | <span data-ttu-id="82601-124">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="82601-124">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="82601-125">Header</span><span class="sxs-lookup"><span data-stu-id="82601-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="82601-126"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="82601-126"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82601-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="82601-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82601-128">**Ivmvirtualmachine:: Startup2**</span><span class="sxs-lookup"><span data-stu-id="82601-128">**IVMVirtualMachine::Startup2**</span></span>](ivmvirtualmachine-startup2.md)
</dt> </dl>

 

