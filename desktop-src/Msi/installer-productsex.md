---
description: Gibt ein RecordList-Objekt zurück, das die Liste der Produkte auflistet.
ms.assetid: 30735b9f-091b-4915-9b07-9688c9be2d26
title: Installer. productsex (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ProductsEx
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 17d5e8290ab61b85fa8269f8b23f3cdabd30e012
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354221"
---
# <a name="installerproductsex-property"></a><span data-ttu-id="04654-103">Installer. productsex (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="04654-103">Installer.ProductsEx property</span></span>

<span data-ttu-id="04654-104">Die **productsex** -Eigenschaft gibt ein [**RecordList**](recordlist-object.md) -Objekt zurück, das die Liste der Produkte auflistet.</span><span class="sxs-lookup"><span data-stu-id="04654-104">The **ProductsEx** property returns a [**RecordList**](recordlist-object.md) object that enumerates the list of products.</span></span> <span data-ttu-id="04654-105">Diese Eigenschaft ruft " [**msienumschlag productsex**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa)" auf.</span><span class="sxs-lookup"><span data-stu-id="04654-105">This property calls [**MsiEnumProductsEx**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa).</span></span>

<span data-ttu-id="04654-106">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="04654-106">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="04654-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="04654-107">Syntax</span></span>


```JScript
propVal = Installer.ProductsEx
```



## <a name="property-value"></a><span data-ttu-id="04654-108">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="04654-108">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="04654-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="04654-109">Requirements</span></span>



| <span data-ttu-id="04654-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="04654-110">Requirement</span></span> | <span data-ttu-id="04654-111">Wert</span><span class="sxs-lookup"><span data-stu-id="04654-111">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04654-112">Version</span><span class="sxs-lookup"><span data-stu-id="04654-112">Version</span></span><br/> | <span data-ttu-id="04654-113">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="04654-113">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="04654-114">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="04654-114">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="04654-115">Windows Installer 3,0 oder höher unter Windows Server 2003 oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="04654-115">Windows Installer 3.0 or later on Windows Server 2003 or Windows XP.</span></span><br/> |
| <span data-ttu-id="04654-116">DLL</span><span class="sxs-lookup"><span data-stu-id="04654-116">DLL</span></span><br/>     | <dl> <span data-ttu-id="04654-117"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="04654-117"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                    |
| <span data-ttu-id="04654-118">IID</span><span class="sxs-lookup"><span data-stu-id="04654-118">IID</span></span><br/>     | <span data-ttu-id="04654-119">IID \_ iinstaller ist definiert als 000c1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="04654-119">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                         |



## <a name="see-also"></a><span data-ttu-id="04654-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="04654-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04654-121">**Installationsprogramm**</span><span class="sxs-lookup"><span data-stu-id="04654-121">**Installer**</span></span>](installer-object.md)
</dt> <dt>

[<span data-ttu-id="04654-122">**Msienumschlag**</span><span class="sxs-lookup"><span data-stu-id="04654-122">**MsiEnumProductsEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msienumproductsexa)
</dt> <dt>

[<span data-ttu-id="04654-123">**Produkt**</span><span class="sxs-lookup"><span data-stu-id="04654-123">**Product**</span></span>](product-object.md)
</dt> <dt>

[<span data-ttu-id="04654-124">Wird in Windows Installer 2,0 und früher nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="04654-124">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




