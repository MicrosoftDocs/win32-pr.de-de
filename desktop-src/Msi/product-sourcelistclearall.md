---
description: Die sourcelistclearall-Methode das Product-Objekt entfernt alle Quellen für das Produkt. Der Typ der zu entfernenden Quelle kann angegeben werden.
ms.assetid: c8a63b54-7be6-424a-8653-0182b561faab
title: Product. sourcelistclearall-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.SourceListClearAll
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 4c921bd45b1acbac40444e4d11bb67d589149c45
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357580"
---
# <a name="productsourcelistclearall-method"></a><span data-ttu-id="24a11-104">Product. sourcelistclearall-Methode</span><span class="sxs-lookup"><span data-stu-id="24a11-104">Product.SourceListClearAll method</span></span>

<span data-ttu-id="24a11-105">Die **sourcelistclearall** -Methode das [**Product**](product-object.md) -Objekt entfernt alle Quellen für das Produkt.</span><span class="sxs-lookup"><span data-stu-id="24a11-105">The **SourceListClearAll** method the [**Product**](product-object.md) object removes all sources for the product.</span></span> <span data-ttu-id="24a11-106">Der Typ der zu entfernenden Quelle kann angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="24a11-106">The type of source to remove can be specified.</span></span>

## <a name="syntax"></a><span data-ttu-id="24a11-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="24a11-107">Syntax</span></span>


```JScript
Product.SourceListClearAll(
  Type
)
```



## <a name="parameters"></a><span data-ttu-id="24a11-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="24a11-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24a11-109">*Type*</span><span class="sxs-lookup"><span data-stu-id="24a11-109">*Type*</span></span> 
</dt> <dd>

<span data-ttu-id="24a11-110">Typ der zu entfernenden Quelle: msisourcetype- \_ Medien, msisourcetype- \_ Netzwerk oder msisourcetype- \_ URL.</span><span class="sxs-lookup"><span data-stu-id="24a11-110">Type of source to be removed: MSISOURCETYPE\_MEDIA, MSISOURCETYPE\_NETWORK or MSISOURCETYPE\_URL.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="24a11-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="24a11-111">Return value</span></span>

<span data-ttu-id="24a11-112">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="24a11-112">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="24a11-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="24a11-113">Requirements</span></span>



| <span data-ttu-id="24a11-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="24a11-114">Requirement</span></span> | <span data-ttu-id="24a11-115">Wert</span><span class="sxs-lookup"><span data-stu-id="24a11-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="24a11-116">Version</span><span class="sxs-lookup"><span data-stu-id="24a11-116">Version</span></span><br/> | <span data-ttu-id="24a11-117">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="24a11-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="24a11-118">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="24a11-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="24a11-119">Windows Installer 3,0 oder höher unter Windows Server 2003, Windows XP und Windows 2000</span><span class="sxs-lookup"><span data-stu-id="24a11-119">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="24a11-120">DLL</span><span class="sxs-lookup"><span data-stu-id="24a11-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="24a11-121"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="24a11-121"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="24a11-122">IID</span><span class="sxs-lookup"><span data-stu-id="24a11-122">IID</span></span><br/>     | <span data-ttu-id="24a11-123">IID \_ iproduct ist definiert als 000c10a0-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="24a11-123">IID\_IProduct is defined as 000C10A0-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                          |



## <a name="see-also"></a><span data-ttu-id="24a11-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="24a11-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24a11-125">**Product**</span><span class="sxs-lookup"><span data-stu-id="24a11-125">**Product**</span></span>](product-object.md)
</dt> <dt>

[<span data-ttu-id="24a11-126">**Msisourcelistclearsource**</span><span class="sxs-lookup"><span data-stu-id="24a11-126">**MsiSourceListClearSource**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistclearsourcea)
</dt> <dt>

[<span data-ttu-id="24a11-127">Wird in Windows Installer 2,0 und früher nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="24a11-127">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




