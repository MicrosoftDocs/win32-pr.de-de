---
description: Die Context-Eigenschaft gibt den Kontext dieses Patches zurück.
ms.assetid: 09c92b0b-44f3-4355-8171-03da8ba32757
title: Patch. Context-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.Context
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 7a6495b199046a361910741545a7178050621ccd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370552"
---
# <a name="patchcontext-property"></a><span data-ttu-id="94a0e-103">Patch. Context-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="94a0e-103">Patch.Context property</span></span>

<span data-ttu-id="94a0e-104">Die **context** -Eigenschaft gibt den Kontext dieses Patches zurück.</span><span class="sxs-lookup"><span data-stu-id="94a0e-104">The **Context** property returns the context of this patch.</span></span>

<span data-ttu-id="94a0e-105">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="94a0e-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="94a0e-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="94a0e-106">Syntax</span></span>


```JScript
propVal = Patch.Context
```



## <a name="property-value"></a><span data-ttu-id="94a0e-107">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="94a0e-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="94a0e-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="94a0e-108">Remarks</span></span>

<span data-ttu-id="94a0e-109">Diese Eigenschaft gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="94a0e-109">This property returns one of the following values.</span></span>



| <span data-ttu-id="94a0e-110">Kontext</span><span class="sxs-lookup"><span data-stu-id="94a0e-110">Context</span></span>                        | <span data-ttu-id="94a0e-111">Wert</span><span class="sxs-lookup"><span data-stu-id="94a0e-111">Value</span></span> | <span data-ttu-id="94a0e-112">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="94a0e-112">Meaning</span></span>                        |
|--------------------------------|-------|--------------------------------|
| <span data-ttu-id="94a0e-113">msiinstallcontext \_ usermanaged</span><span class="sxs-lookup"><span data-stu-id="94a0e-113">MSIINSTALLCONTEXT\_USERMANAGED</span></span> | <span data-ttu-id="94a0e-114">1</span><span class="sxs-lookup"><span data-stu-id="94a0e-114">1</span></span>     | <span data-ttu-id="94a0e-115">Patch unter verwaltetem Kontext.</span><span class="sxs-lookup"><span data-stu-id="94a0e-115">Patch under managed context.</span></span>   |
| <span data-ttu-id="94a0e-116">msiinstallcontext- \_ Benutzer</span><span class="sxs-lookup"><span data-stu-id="94a0e-116">MSIINSTALLCONTEXT\_USER</span></span>        | <span data-ttu-id="94a0e-117">2</span><span class="sxs-lookup"><span data-stu-id="94a0e-117">2</span></span>     | <span data-ttu-id="94a0e-118">Patch unter nicht verwaltetem Kontext.</span><span class="sxs-lookup"><span data-stu-id="94a0e-118">Patch under unmanaged context.</span></span> |
| <span data-ttu-id="94a0e-119">msiinstallcontext- \_ Computer</span><span class="sxs-lookup"><span data-stu-id="94a0e-119">MSIINSTALLCONTEXT\_MACHINE</span></span>     | <span data-ttu-id="94a0e-120">4</span><span class="sxs-lookup"><span data-stu-id="94a0e-120">4</span></span>     | <span data-ttu-id="94a0e-121">Patch unter Computer Kontext.</span><span class="sxs-lookup"><span data-stu-id="94a0e-121">Patch under machine context.</span></span>   |



 

## <a name="requirements"></a><span data-ttu-id="94a0e-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="94a0e-122">Requirements</span></span>



| <span data-ttu-id="94a0e-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="94a0e-123">Requirement</span></span> | <span data-ttu-id="94a0e-124">Wert</span><span class="sxs-lookup"><span data-stu-id="94a0e-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="94a0e-125">Version</span><span class="sxs-lookup"><span data-stu-id="94a0e-125">Version</span></span><br/> | <span data-ttu-id="94a0e-126">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="94a0e-126">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="94a0e-127">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="94a0e-127">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="94a0e-128">Windows Installer 3,0 oder höher unter Windows Server 2003, Windows XP und Windows 2000</span><span class="sxs-lookup"><span data-stu-id="94a0e-128">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="94a0e-129">DLL</span><span class="sxs-lookup"><span data-stu-id="94a0e-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="94a0e-130"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="94a0e-130"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="94a0e-131">IID</span><span class="sxs-lookup"><span data-stu-id="94a0e-131">IID</span></span><br/>     | <span data-ttu-id="94a0e-132">IID \_ iPatch ist definiert als 000c10a1-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="94a0e-132">IID\_IPatch is defined as 000C10A1-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="94a0e-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="94a0e-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94a0e-134">**Patch-Objekt**</span><span class="sxs-lookup"><span data-stu-id="94a0e-134">**Patch Object**</span></span>](patch-object.md)
</dt> <dt>

[<span data-ttu-id="94a0e-135">Wird in Windows Installer 2,0 und früher nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="94a0e-135">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




