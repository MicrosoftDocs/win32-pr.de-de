---
title: Vmmouterbutton-Enumeration (vpccominterfaces. h)
description: Gibt die Maustaste an.
ms.assetid: d09e63cb-9dc5-424f-b130-c0b0dd07fe11
keywords:
- Virtueller PC der vmmouerbutton-Enumeration
topic_type:
- apiref
api_name:
- VMMouseButton
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18744af5a4f8068b9bb371cb15e06c365561f2cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478309"
---
# <a name="vmmousebutton-enumeration"></a><span data-ttu-id="d2b4b-104">Vmmouerbutton-Enumeration</span><span class="sxs-lookup"><span data-stu-id="d2b4b-104">VMMouseButton enumeration</span></span>

<span data-ttu-id="d2b4b-105">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d2b4b-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="d2b4b-106">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="d2b4b-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="d2b4b-107">Gibt die Maustaste an.</span><span class="sxs-lookup"><span data-stu-id="d2b4b-107">Specifies the mouse button.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2b4b-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="d2b4b-108">Syntax</span></span>


```C++
typedef enum  { 
  vmMouseButton_Left    = 1,
  vmMouseButton_Right   = 2,
  vmMouseButton_Center  = 3
} VMMouseButton;
```



## <a name="constants"></a><span data-ttu-id="d2b4b-109">Konstanten</span><span class="sxs-lookup"><span data-stu-id="d2b4b-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="d2b4b-110"><span id="vmMouseButton_Left"></span><span id="vmmousebutton_left"></span><span id="VMMOUSEBUTTON_LEFT"></span>**vmmouabschalt Schaltfläche \_ Links**</span><span class="sxs-lookup"><span data-stu-id="d2b4b-110"><span id="vmMouseButton_Left"></span><span id="vmmousebutton_left"></span><span id="VMMOUSEBUTTON_LEFT"></span>**vmMouseButton\_Left**</span></span>
</dt> <dd>

<span data-ttu-id="d2b4b-111">Die linke Maustaste.</span><span class="sxs-lookup"><span data-stu-id="d2b4b-111">The left mouse button.</span></span>

</dd> <dt>

<span data-ttu-id="d2b4b-112"><span id="vmMouseButton_Right"></span><span id="vmmousebutton_right"></span><span id="VMMOUSEBUTTON_RIGHT"></span>**vmmouabschaltfläche \_ Rechts**</span><span class="sxs-lookup"><span data-stu-id="d2b4b-112"><span id="vmMouseButton_Right"></span><span id="vmmousebutton_right"></span><span id="VMMOUSEBUTTON_RIGHT"></span>**vmMouseButton\_Right**</span></span>
</dt> <dd>

<span data-ttu-id="d2b4b-113">Die rechte Maustaste.</span><span class="sxs-lookup"><span data-stu-id="d2b4b-113">The right mouse button.</span></span>

</dd> <dt>

<span data-ttu-id="d2b4b-114"><span id="vmMouseButton_Center"></span><span id="vmmousebutton_center"></span><span id="VMMOUSEBUTTON_CENTER"></span>**vmmouonbutton- \_ Center**</span><span class="sxs-lookup"><span data-stu-id="d2b4b-114"><span id="vmMouseButton_Center"></span><span id="vmmousebutton_center"></span><span id="VMMOUSEBUTTON_CENTER"></span>**vmMouseButton\_Center**</span></span>
</dt> <dd>

<span data-ttu-id="d2b4b-115">Die Mitte-Maustaste.</span><span class="sxs-lookup"><span data-stu-id="d2b4b-115">The center mouse button.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d2b4b-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d2b4b-116">Requirements</span></span>



| <span data-ttu-id="d2b4b-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d2b4b-117">Requirement</span></span> | <span data-ttu-id="d2b4b-118">Wert</span><span class="sxs-lookup"><span data-stu-id="d2b4b-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2b4b-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d2b4b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d2b4b-120">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d2b4b-120">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d2b4b-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d2b4b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d2b4b-122">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="d2b4b-122">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="d2b4b-123">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="d2b4b-123">End of client support</span></span><br/>    | <span data-ttu-id="d2b4b-124">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d2b4b-124">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="d2b4b-125">Produkt</span><span class="sxs-lookup"><span data-stu-id="d2b4b-125">Product</span></span><br/>                  | <span data-ttu-id="d2b4b-126">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="d2b4b-126">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="d2b4b-127">Header</span><span class="sxs-lookup"><span data-stu-id="d2b4b-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="d2b4b-128"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="d2b4b-128"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d2b4b-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d2b4b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2b4b-130">**Ivmmouse**</span><span class="sxs-lookup"><span data-stu-id="d2b4b-130">**IVMMouse**</span></span>](ivmmouse.md)
</dt> </dl>

 

