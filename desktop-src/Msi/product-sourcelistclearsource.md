---
description: Die sourcelistclearsource-Methode entfernt eine Netzwerk-oder URL-Quelle. Akzeptiert Typ, den Quelltyp und SourcePath, den Quellpfad, als Parameter, die entfernt werden sollen. Diese Methode ruft das msisourcelistclearsource-Element auf.
ms.assetid: a55676d4-795d-4ffe-8621-ef47c16a936c
title: Product. sourcelistclearsource-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.SourceListClearSource
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 4988d0ba9003e087b6aeac58ae5587727067e01c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358293"
---
# <a name="productsourcelistclearsource-method"></a><span data-ttu-id="00c3c-105">Product. sourcelistclearsource-Methode</span><span class="sxs-lookup"><span data-stu-id="00c3c-105">Product.SourceListClearSource method</span></span>

<span data-ttu-id="00c3c-106">Die **sourcelistclearsource** -Methode entfernt eine Netzwerk-oder URL-Quelle.</span><span class="sxs-lookup"><span data-stu-id="00c3c-106">The **SourceListClearSource** method removes a network or URL source.</span></span> <span data-ttu-id="00c3c-107">Akzeptiert *Typ*, den Quelltyp und *SourcePath*, den Quellpfad, als Parameter, die entfernt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="00c3c-107">Accepts *Type*, the source type, and *SourcePath*, the source path, as parameters to be removed.</span></span> <span data-ttu-id="00c3c-108">Diese Methode ruft das [**msisourcelistclearsource**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearsourcea)-Element auf.</span><span class="sxs-lookup"><span data-stu-id="00c3c-108">This method calls the [**MsiSourceListClearSource**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearsourcea).</span></span>

## <a name="syntax"></a><span data-ttu-id="00c3c-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="00c3c-109">Syntax</span></span>


```JScript
Product.SourceListClearSource(
  Type,
  SourcePath
)
```



## <a name="parameters"></a><span data-ttu-id="00c3c-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="00c3c-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00c3c-111">*Type*</span><span class="sxs-lookup"><span data-stu-id="00c3c-111">*Type*</span></span> 
</dt> <dd>

<span data-ttu-id="00c3c-112">Typ der zu entfernenden Quelle: msisourcetype \_ Network oder msisourcetype \_ URL.</span><span class="sxs-lookup"><span data-stu-id="00c3c-112">Type of source to be removed: MSISOURCETYPE\_NETWORK or MSISOURCETYPE\_URL.</span></span>

</dd> <dt>

<span data-ttu-id="00c3c-113">*SourcePath*</span><span class="sxs-lookup"><span data-stu-id="00c3c-113">*SourcePath*</span></span> 
</dt> <dd>

<span data-ttu-id="00c3c-114">Der Pfad zur Quelle, die entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="00c3c-114">Path to the source to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00c3c-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="00c3c-115">Return value</span></span>

<span data-ttu-id="00c3c-116">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="00c3c-116">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="00c3c-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="00c3c-117">Requirements</span></span>



| <span data-ttu-id="00c3c-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="00c3c-118">Requirement</span></span> | <span data-ttu-id="00c3c-119">Wert</span><span class="sxs-lookup"><span data-stu-id="00c3c-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="00c3c-120">Version</span><span class="sxs-lookup"><span data-stu-id="00c3c-120">Version</span></span><br/> | <span data-ttu-id="00c3c-121">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="00c3c-121">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="00c3c-122">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="00c3c-122">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="00c3c-123">Windows Installer 3,0 oder höher unter Windows Server 2003, Windows XP und Windows 2000</span><span class="sxs-lookup"><span data-stu-id="00c3c-123">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="00c3c-124">DLL</span><span class="sxs-lookup"><span data-stu-id="00c3c-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="00c3c-125"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="00c3c-125"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="00c3c-126">IID</span><span class="sxs-lookup"><span data-stu-id="00c3c-126">IID</span></span><br/>     | <span data-ttu-id="00c3c-127">IID \_ iproduct ist definiert als 000c10a0-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="00c3c-127">IID\_IProduct is defined as 000C10A0-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                          |



## <a name="see-also"></a><span data-ttu-id="00c3c-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="00c3c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00c3c-129">**Product**</span><span class="sxs-lookup"><span data-stu-id="00c3c-129">**Product**</span></span>](product-object.md)
</dt> <dt>

[<span data-ttu-id="00c3c-130">**Msisourcelistclearsource**</span><span class="sxs-lookup"><span data-stu-id="00c3c-130">**MsiSourceListClearSource**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistclearsourcea)
</dt> <dt>

[<span data-ttu-id="00c3c-131">Wird in Windows Installer 2,0 und früher nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="00c3c-131">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




