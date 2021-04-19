---
description: Die sourcelistforceresolution-Methode löscht die "LastUsedSource"-Eigenschaft.
ms.assetid: 554bc321-51d8-4595-b79c-7975bad8c555
title: Product. sourcelistforceresolution-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.SourceListForceResolution
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 668a74d2327dad918f1f2389bc163dcfde198c2d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372174"
---
# <a name="productsourcelistforceresolution-method"></a><span data-ttu-id="f8736-103">Product. sourcelistforceresolution-Methode</span><span class="sxs-lookup"><span data-stu-id="f8736-103">Product.SourceListForceResolution method</span></span>

<span data-ttu-id="f8736-104">Die **sourcelistforceresolution** -Methode löscht die "LastUsedSource"-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="f8736-104">The **SourceListForceResolution** method clears the LastUsedSource property.</span></span> <span data-ttu-id="f8736-105">Dadurch wird das Installationsprogramm gezwungen, die Quell Liste nach einer gültigen Produkt Quelle zu durchsuchen, wenn eine Quelle das nächste Mal benötigt wird, z. b. wenn das Installationsprogramm eine Installation oder eine Neuinstallation ausführt oder wenn der Pfad erforderlich ist, damit eine Komponente von der Quelle ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="f8736-105">This forces the installer to search the source list for a valid product source the next time a source is required, such as when the installer performs an installation or a reinstallation, or when the path is required for a component set to run from the source.</span></span>

<span data-ttu-id="f8736-106">Diese Methode ruft [**msisourcelistforceresolution**](/windows/desktop/api/Msi/nf-msi-msisourcelistforceresolutiona)auf.</span><span class="sxs-lookup"><span data-stu-id="f8736-106">This method calls [**MsiSourceListForceResolution**](/windows/desktop/api/Msi/nf-msi-msisourcelistforceresolutiona).</span></span>

## <a name="syntax"></a><span data-ttu-id="f8736-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="f8736-107">Syntax</span></span>


```JScript
Product.SourceListForceResolution()
```



## <a name="parameters"></a><span data-ttu-id="f8736-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="f8736-108">Parameters</span></span>

<span data-ttu-id="f8736-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="f8736-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f8736-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f8736-110">Return value</span></span>

<span data-ttu-id="f8736-111">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="f8736-111">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8736-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f8736-112">Requirements</span></span>



| <span data-ttu-id="f8736-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f8736-113">Requirement</span></span> | <span data-ttu-id="f8736-114">Wert</span><span class="sxs-lookup"><span data-stu-id="f8736-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8736-115">Version</span><span class="sxs-lookup"><span data-stu-id="f8736-115">Version</span></span><br/> | <span data-ttu-id="f8736-116">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="f8736-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="f8736-117">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="f8736-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="f8736-118">Windows Installer 3,0 oder höher unter Windows Server 2003, Windows XP und Windows 2000</span><span class="sxs-lookup"><span data-stu-id="f8736-118">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="f8736-119">DLL</span><span class="sxs-lookup"><span data-stu-id="f8736-119">DLL</span></span><br/>     | <dl> <span data-ttu-id="f8736-120"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f8736-120"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="f8736-121">IID</span><span class="sxs-lookup"><span data-stu-id="f8736-121">IID</span></span><br/>     | <span data-ttu-id="f8736-122">IID \_ iproduct ist definiert als 000c10a0-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="f8736-122">IID\_IProduct is defined as 000C10A0-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                          |



## <a name="see-also"></a><span data-ttu-id="f8736-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f8736-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8736-124">**Product**</span><span class="sxs-lookup"><span data-stu-id="f8736-124">**Product**</span></span>](product-object.md)
</dt> <dt>

[<span data-ttu-id="f8736-125">**Msisourcelistforceresolution**</span><span class="sxs-lookup"><span data-stu-id="f8736-125">**MsiSourceListForceResolution**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistforceresolutiona)
</dt> <dt>

[<span data-ttu-id="f8736-126">Wird in Windows Installer 2,0 und früher nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f8736-126">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




