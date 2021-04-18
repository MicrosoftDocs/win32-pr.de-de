---
description: Die Context-Eigenschaft gibt den Kontext dieses Produkts zurück.
ms.assetid: aa772a95-eb4e-45af-9788-9833d62139e8
title: Product. Context-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.Context
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 8334ca57d552681afeb77d0b213eca8b92bc1234
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358647"
---
# <a name="productcontext-property"></a><span data-ttu-id="23371-103">Product. Context-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="23371-103">Product.Context property</span></span>

<span data-ttu-id="23371-104">Die **context** -Eigenschaft gibt den Kontext dieses Produkts zurück.</span><span class="sxs-lookup"><span data-stu-id="23371-104">The **Context** property returns the context of this product.</span></span>

<span data-ttu-id="23371-105">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="23371-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="23371-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="23371-106">Syntax</span></span>


```JScript
propVal = Product.Context
```



## <a name="property-value"></a><span data-ttu-id="23371-107">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="23371-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="23371-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="23371-108">Remarks</span></span>

<span data-ttu-id="23371-109">Diese Eigenschaft kann einen der folgenden Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="23371-109">This property can return one of the following values.</span></span>



| <span data-ttu-id="23371-110">Kontext</span><span class="sxs-lookup"><span data-stu-id="23371-110">Context</span></span>                        | <span data-ttu-id="23371-111">Wert</span><span class="sxs-lookup"><span data-stu-id="23371-111">Value</span></span> | <span data-ttu-id="23371-112">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="23371-112">Meaning</span></span>                           |
|--------------------------------|-------|-----------------------------------|
| <span data-ttu-id="23371-113">msiinstallcontext \_ usermanaged</span><span class="sxs-lookup"><span data-stu-id="23371-113">MSIINSTALLCONTEXT\_USERMANAGED</span></span> | <span data-ttu-id="23371-114">1</span><span class="sxs-lookup"><span data-stu-id="23371-114">1</span></span>     | <span data-ttu-id="23371-115">Produkte unter verwaltetem Kontext.</span><span class="sxs-lookup"><span data-stu-id="23371-115">Products under managed context.</span></span>   |
| <span data-ttu-id="23371-116">msiinstallcontext- \_ Benutzer</span><span class="sxs-lookup"><span data-stu-id="23371-116">MSIINSTALLCONTEXT\_USER</span></span>        | <span data-ttu-id="23371-117">2</span><span class="sxs-lookup"><span data-stu-id="23371-117">2</span></span>     | <span data-ttu-id="23371-118">Produkte im nicht verwalteten Kontext.</span><span class="sxs-lookup"><span data-stu-id="23371-118">Products under unmanaged context.</span></span> |
| <span data-ttu-id="23371-119">msiinstallcontext- \_ Computer</span><span class="sxs-lookup"><span data-stu-id="23371-119">MSIINSTALLCONTEXT\_MACHINE</span></span>     | <span data-ttu-id="23371-120">4</span><span class="sxs-lookup"><span data-stu-id="23371-120">4</span></span>     | <span data-ttu-id="23371-121">Produkte im Computer Kontext.</span><span class="sxs-lookup"><span data-stu-id="23371-121">Products under machine context.</span></span>   |



 

## <a name="requirements"></a><span data-ttu-id="23371-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="23371-122">Requirements</span></span>



| <span data-ttu-id="23371-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="23371-123">Requirement</span></span> | <span data-ttu-id="23371-124">Wert</span><span class="sxs-lookup"><span data-stu-id="23371-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="23371-125">Version</span><span class="sxs-lookup"><span data-stu-id="23371-125">Version</span></span><br/> | <span data-ttu-id="23371-126">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="23371-126">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="23371-127">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="23371-127">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="23371-128">Windows Installer 3,0 oder höher unter Windows Server 2003, Windows XP und Windows 2000</span><span class="sxs-lookup"><span data-stu-id="23371-128">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="23371-129">DLL</span><span class="sxs-lookup"><span data-stu-id="23371-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="23371-130"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="23371-130"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="23371-131">IID</span><span class="sxs-lookup"><span data-stu-id="23371-131">IID</span></span><br/>     | <span data-ttu-id="23371-132">IID \_ iproduct ist definiert als 000c10a0-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="23371-132">IID\_IProduct is defined as 000C10A0-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                          |



## <a name="see-also"></a><span data-ttu-id="23371-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="23371-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23371-134">**Product**</span><span class="sxs-lookup"><span data-stu-id="23371-134">**Product**</span></span>](product-object.md)
</dt> <dt>

[<span data-ttu-id="23371-135">Wird in Windows Installer 2,0 und früher nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="23371-135">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




