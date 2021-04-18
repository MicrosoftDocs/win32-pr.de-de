---
description: Die Sources-Eigenschaft listet alle Quellen für die Produkt Instanz auf.
ms.assetid: 26602099-d0e0-4269-91d9-82943859811a
title: Product. Sources (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.Sources
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: a82363f6a61ebb9c441dfcfeeeafe3760e63c462
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371660"
---
# <a name="productsources-property"></a><span data-ttu-id="c9441-103">Product. Sources (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="c9441-103">Product.Sources property</span></span>

<span data-ttu-id="c9441-104">Die **Sources** -Eigenschaft listet alle Quellen für die Produkt Instanz auf.</span><span class="sxs-lookup"><span data-stu-id="c9441-104">The **Sources** property enumerates all the sources for the product instance.</span></span> <span data-ttu-id="c9441-105">Diese Eigenschaft ruft " [**msisourcelistenumschlag sources**](/windows/desktop/api/Msi/nf-msi-msisourcelistenumsourcesa) " auf und gibt das Array von Zeichen folgen zurück. der Quelltyp wird als Argument akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="c9441-105">This property calls [**MsiSourceListEnumSources**](/windows/desktop/api/Msi/nf-msi-msisourcelistenumsourcesa) and returns the array of strings, and accepts the source type as argument.</span></span> <span data-ttu-id="c9441-106">Der Quelltyp kann das msisourcetype- \_ Netzwerk oder die msisourcetype- \_ URL sein.</span><span class="sxs-lookup"><span data-stu-id="c9441-106">The source type can be MSISOURCETYPE\_NETWORK or MSISOURCETYPE\_URL.</span></span>

<span data-ttu-id="c9441-107">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="c9441-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9441-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="c9441-108">Syntax</span></span>


```JScript
propVal = Product.Sources
```



## <a name="property-value"></a><span data-ttu-id="c9441-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="c9441-109">Property value</span></span>

<span data-ttu-id="c9441-110">Der Typ der aufzuzählenden Quelle.</span><span class="sxs-lookup"><span data-stu-id="c9441-110">The type of source to enumerate.</span></span> <span data-ttu-id="c9441-111">Der Wert kann *msiinstallsourcetymessetwork* (1) oder *msiinstallsourcetypeurl* (2) sein.</span><span class="sxs-lookup"><span data-stu-id="c9441-111">The value can be *msiInstallSourceTypeNetwork* (1) or *msiInstallSourceTypeURL* (2).</span></span>

## <a name="requirements"></a><span data-ttu-id="c9441-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c9441-112">Requirements</span></span>



| <span data-ttu-id="c9441-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c9441-113">Requirement</span></span> | <span data-ttu-id="c9441-114">Wert</span><span class="sxs-lookup"><span data-stu-id="c9441-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9441-115">Version</span><span class="sxs-lookup"><span data-stu-id="c9441-115">Version</span></span><br/> | <span data-ttu-id="c9441-116">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="c9441-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="c9441-117">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="c9441-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="c9441-118">Windows Installer 3,0 oder höher unter Windows Server 2003, Windows XP und Windows 2000</span><span class="sxs-lookup"><span data-stu-id="c9441-118">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="c9441-119">DLL</span><span class="sxs-lookup"><span data-stu-id="c9441-119">DLL</span></span><br/>     | <dl> <span data-ttu-id="c9441-120"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c9441-120"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="c9441-121">IID</span><span class="sxs-lookup"><span data-stu-id="c9441-121">IID</span></span><br/>     | <span data-ttu-id="c9441-122">IID \_ iproduct ist definiert als 000c10a0-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="c9441-122">IID\_IProduct is defined as 000C10A0-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                          |



## <a name="see-also"></a><span data-ttu-id="c9441-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c9441-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9441-124">**Product**</span><span class="sxs-lookup"><span data-stu-id="c9441-124">**Product**</span></span>](product-object.md)
</dt> <dt>

[<span data-ttu-id="c9441-125">**Msisourcelistenumschlag Quellen**</span><span class="sxs-lookup"><span data-stu-id="c9441-125">**MsiSourceListEnumSources**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistenumsourcesa)
</dt> <dt>

[<span data-ttu-id="c9441-126">Wird in Windows Installer 2,0 und früher nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c9441-126">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




