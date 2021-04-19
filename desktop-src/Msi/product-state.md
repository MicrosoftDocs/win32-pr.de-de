---
description: Die State-Eigenschaft gibt den Installationsstatus dieser Instanz des Produkts zurück.
ms.assetid: ae4c7a43-d4af-4e06-a3f8-d7c2d0715d84
title: Product. State (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.State
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 64d2f5d39a516fc4a0c00b8e18c159e1f2496e22
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368657"
---
# <a name="productstate-property"></a><span data-ttu-id="0a6cc-103">Product. State (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="0a6cc-103">Product.State property</span></span>

<span data-ttu-id="0a6cc-104">Die **State** -Eigenschaft gibt den Installationsstatus dieser Instanz des Produkts zurück.</span><span class="sxs-lookup"><span data-stu-id="0a6cc-104">The **State** property returns the installation state of this instance of the product.</span></span>

<span data-ttu-id="0a6cc-105">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="0a6cc-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a6cc-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="0a6cc-106">Syntax</span></span>


```JScript
propVal = Product.State
```



## <a name="property-value"></a><span data-ttu-id="0a6cc-107">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="0a6cc-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="0a6cc-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0a6cc-108">Remarks</span></span>

<span data-ttu-id="0a6cc-109">Diese Eigenschaft gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="0a6cc-109">This property returns one of the following values.</span></span>



| <span data-ttu-id="0a6cc-110">Installationsstatus</span><span class="sxs-lookup"><span data-stu-id="0a6cc-110">Installation State</span></span>       | <span data-ttu-id="0a6cc-111">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="0a6cc-111">Meaning</span></span>                                |
|--------------------------|----------------------------------------|
| <span data-ttu-id="0a6cc-112">InstallState ( \_ Standard)</span><span class="sxs-lookup"><span data-stu-id="0a6cc-112">INSTALLSTATE\_DEFAULT</span></span>    | <span data-ttu-id="0a6cc-113">Die lokal installierte Instanz des Produkts.</span><span class="sxs-lookup"><span data-stu-id="0a6cc-113">Instance of product installed locally.</span></span> |
| <span data-ttu-id="0a6cc-114">InstallState \_ angekündigt</span><span class="sxs-lookup"><span data-stu-id="0a6cc-114">INSTALLSTATE\_ADVERTISED</span></span> | <span data-ttu-id="0a6cc-115">Die Instanz des angekündigten Produkts.</span><span class="sxs-lookup"><span data-stu-id="0a6cc-115">Instance of product advertised.</span></span>        |
| <span data-ttu-id="0a6cc-116">InstallState \_ unbekannt</span><span class="sxs-lookup"><span data-stu-id="0a6cc-116">INSTALLSTATE\_UNKNOWN</span></span>    | <span data-ttu-id="0a6cc-117">Unbekannte Produkt Instanz.</span><span class="sxs-lookup"><span data-stu-id="0a6cc-117">Instance of product unknown.</span></span>           |



 

## <a name="requirements"></a><span data-ttu-id="0a6cc-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0a6cc-118">Requirements</span></span>



| <span data-ttu-id="0a6cc-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0a6cc-119">Requirement</span></span> | <span data-ttu-id="0a6cc-120">Wert</span><span class="sxs-lookup"><span data-stu-id="0a6cc-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a6cc-121">Version</span><span class="sxs-lookup"><span data-stu-id="0a6cc-121">Version</span></span><br/> | <span data-ttu-id="0a6cc-122">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="0a6cc-122">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="0a6cc-123">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="0a6cc-123">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="0a6cc-124">Windows Installer 3,0 oder höher unter Windows Server 2003, Windows XP und Windows 2000</span><span class="sxs-lookup"><span data-stu-id="0a6cc-124">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="0a6cc-125">DLL</span><span class="sxs-lookup"><span data-stu-id="0a6cc-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="0a6cc-126"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0a6cc-126"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="0a6cc-127">IID</span><span class="sxs-lookup"><span data-stu-id="0a6cc-127">IID</span></span><br/>     | <span data-ttu-id="0a6cc-128">IID \_ iproduct ist definiert als 000c10a0-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="0a6cc-128">IID\_IProduct is defined as 000C10A0-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                          |



## <a name="see-also"></a><span data-ttu-id="0a6cc-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0a6cc-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a6cc-130">**Product**</span><span class="sxs-lookup"><span data-stu-id="0a6cc-130">**Product**</span></span>](product-object.md)
</dt> <dt>

[<span data-ttu-id="0a6cc-131">Wird in Windows Installer 2,0 und früher nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0a6cc-131">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




