---
description: Die sourcelistclearmediadisk-Methode des Product-Objekts entfernt einen angegebenen Datenträger aus der Gruppe der registrierten Datenträger für ein Produkt. Akzeptiert DiskId als Parameter. Diese Methode ruft msisourcelistclearmediadisk auf.
ms.assetid: 7eec644e-5127-4c17-a8bd-6b0eb091c8aa
title: Product. sourcelistclearmediadisk-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.SourceListClearMediaDisk
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: a607591f45208854118b0f97849cd7072e484bee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366933"
---
# <a name="productsourcelistclearmediadisk-method"></a><span data-ttu-id="e7c1a-105">Product. sourcelistclearmediadisk-Methode</span><span class="sxs-lookup"><span data-stu-id="e7c1a-105">Product.SourceListClearMediaDisk method</span></span>

<span data-ttu-id="e7c1a-106">Die **sourcelistclearmediadisk** -Methode des [**Product**](product-object.md) -Objekts entfernt einen angegebenen Datenträger aus der Gruppe der registrierten Datenträger für ein Produkt.</span><span class="sxs-lookup"><span data-stu-id="e7c1a-106">The **SourceListClearMediaDisk** method of the [**Product**](product-object.md) object removes a specified disk from the set of registered disks for a product.</span></span> <span data-ttu-id="e7c1a-107">Akzeptiert *DiskId* als Parameter.</span><span class="sxs-lookup"><span data-stu-id="e7c1a-107">Accepts *Diskid* as a parameter.</span></span> <span data-ttu-id="e7c1a-108">Diese Methode ruft [**msisourcelistclearmediadisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearmediadiska)auf.</span><span class="sxs-lookup"><span data-stu-id="e7c1a-108">This method calls [**MsiSourceListClearMediaDisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearmediadiska).</span></span>

## <a name="syntax"></a><span data-ttu-id="e7c1a-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="e7c1a-109">Syntax</span></span>


```JScript
Product.SourceListClearMediaDisk(
  Diskid
)
```



## <a name="parameters"></a><span data-ttu-id="e7c1a-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="e7c1a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7c1a-111">*DiskId*</span><span class="sxs-lookup"><span data-stu-id="e7c1a-111">*Diskid*</span></span> 
</dt> <dd>

<span data-ttu-id="e7c1a-112">Dieser Parameter gibt die ID des zu entfernenden Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="e7c1a-112">This parameter provides the ID of the disk to remove.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7c1a-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e7c1a-113">Return value</span></span>

<span data-ttu-id="e7c1a-114">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="e7c1a-114">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7c1a-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e7c1a-115">Requirements</span></span>



| <span data-ttu-id="e7c1a-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e7c1a-116">Requirement</span></span> | <span data-ttu-id="e7c1a-117">Wert</span><span class="sxs-lookup"><span data-stu-id="e7c1a-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7c1a-118">Version</span><span class="sxs-lookup"><span data-stu-id="e7c1a-118">Version</span></span><br/> | <span data-ttu-id="e7c1a-119">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="e7c1a-119">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="e7c1a-120">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e7c1a-120">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="e7c1a-121">Windows Installer 3,0 oder höher unter Windows Server 2003, Windows XP und Windows 2000</span><span class="sxs-lookup"><span data-stu-id="e7c1a-121">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="e7c1a-122">DLL</span><span class="sxs-lookup"><span data-stu-id="e7c1a-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="e7c1a-123"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e7c1a-123"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="e7c1a-124">IID</span><span class="sxs-lookup"><span data-stu-id="e7c1a-124">IID</span></span><br/>     | <span data-ttu-id="e7c1a-125">IID \_ iproduct ist definiert als 000c10a0-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="e7c1a-125">IID\_IProduct is defined as 000C10A0-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                          |



## <a name="see-also"></a><span data-ttu-id="e7c1a-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e7c1a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7c1a-127">**Product**</span><span class="sxs-lookup"><span data-stu-id="e7c1a-127">**Product**</span></span>](product-object.md)
</dt> <dt>

[<span data-ttu-id="e7c1a-128">**Msisourcelistclearmediadisk**</span><span class="sxs-lookup"><span data-stu-id="e7c1a-128">**MsiSourceListClearMediaDisk**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistclearmediadiska)
</dt> <dt>

[<span data-ttu-id="e7c1a-129">Wird in Windows Installer 2,0 und früher nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e7c1a-129">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




