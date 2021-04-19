---
description: Die ProductInfo-Eigenschaft ist eine schreibgeschützte Eigenschaft, die den Wert des angegebenen Attributs für ein installiertes oder veröffentlichtes Produkt zurückgibt.
ms.assetid: 144cbba7-ec2b-44cd-acc8-868c210ccebd
title: Installer. ProductInfo-Eigenschaft ("oemupgex. h")
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ProductInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 03ad741dd1c92fe68caccc4582738e54032750e9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354803"
---
# <a name="installerproductinfo-property"></a><span data-ttu-id="3bdd7-103">Installer. ProductInfo-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="3bdd7-103">Installer.ProductInfo property</span></span>

<span data-ttu-id="3bdd7-104">Die **productinfo** -Eigenschaft ist eine schreibgeschützte Eigenschaft, die den Wert des angegebenen Attributs für ein installiertes oder veröffentlichtes Produkt zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="3bdd7-104">The **ProductInfo** property is a read-only property that returns the value of the specified attribute for an installed or published product.</span></span>

<span data-ttu-id="3bdd7-105">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="3bdd7-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="3bdd7-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="3bdd7-106">Syntax</span></span>


```JScript
propVal = Installer.ProductInfo
```



## <a name="property-value"></a><span data-ttu-id="3bdd7-107">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="3bdd7-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="3bdd7-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3bdd7-108">Remarks</span></span>

<span data-ttu-id="3bdd7-109">Die **productinfo** -Eigenschaft ("localpackage") gibt nicht notwendigerweise einen Pfad zum zwischengespeicherten Paket zurück.</span><span class="sxs-lookup"><span data-stu-id="3bdd7-109">The **ProductInfo** property ("LocalPackage") does not necessarily return a path to the cached package.</span></span> <span data-ttu-id="3bdd7-110">Wartungsmodus-Installationen sollten nicht über das localpackage aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="3bdd7-110">Maintenance mode installations should be not be invoked from the LocalPackage.</span></span> <span data-ttu-id="3bdd7-111">Das zwischengespeicherte Paket ist nur für die interne Verwendung vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="3bdd7-111">The cached package is for internal uses only.</span></span>

## <a name="requirements"></a><span data-ttu-id="3bdd7-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3bdd7-112">Requirements</span></span>



| <span data-ttu-id="3bdd7-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3bdd7-113">Requirement</span></span> | <span data-ttu-id="3bdd7-114">Wert</span><span class="sxs-lookup"><span data-stu-id="3bdd7-114">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3bdd7-115">Version</span><span class="sxs-lookup"><span data-stu-id="3bdd7-115">Version</span></span><br/> | <span data-ttu-id="3bdd7-116">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="3bdd7-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="3bdd7-117">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="3bdd7-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="3bdd7-118">Windows Installer 3,0 oder höher unter Windows Server 2003 oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="3bdd7-118">Windows Installer 3.0 or later on Windows Server 2003 or Windows XP.</span></span><br/> |
| <span data-ttu-id="3bdd7-119">Header</span><span class="sxs-lookup"><span data-stu-id="3bdd7-119">Header</span></span><br/>  | <dl> <span data-ttu-id="3bdd7-120"><dt>"Oemupgex. h"</dt></span><span class="sxs-lookup"><span data-stu-id="3bdd7-120"><dt>Oemupgex.h</dt></span></span> </dl>                                                                                                                                                                                 |
| <span data-ttu-id="3bdd7-121">DLL</span><span class="sxs-lookup"><span data-stu-id="3bdd7-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="3bdd7-122"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3bdd7-122"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                    |
| <span data-ttu-id="3bdd7-123">IID</span><span class="sxs-lookup"><span data-stu-id="3bdd7-123">IID</span></span><br/>     | <span data-ttu-id="3bdd7-124">IID \_ iinstaller ist definiert als 000c1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="3bdd7-124">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                         |



## <a name="see-also"></a><span data-ttu-id="3bdd7-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3bdd7-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3bdd7-126">**Msigetproductinfo**</span><span class="sxs-lookup"><span data-stu-id="3bdd7-126">**MsiGetProductInfo**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa)
</dt> <dt>

[<span data-ttu-id="3bdd7-127">**Msigetuserinfo**</span><span class="sxs-lookup"><span data-stu-id="3bdd7-127">**MsiGetUserInfo**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetuserinfoa)
</dt> <dt>

[<span data-ttu-id="3bdd7-128">Wird in Windows Installer 2,0 und früher nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3bdd7-128">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




