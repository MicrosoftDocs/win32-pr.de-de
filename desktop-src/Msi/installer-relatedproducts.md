---
description: Die schreibgeschützte RelatedProducts-Eigenschaft gibt ein stringlist-Objekt zurück, das den Satz aller Produkte auflistet, die für den aktuellen Benutzer und Computer mit einer angegebenen UpgradeCode-Eigenschaft in der Eigenschaften Tabelle installiert oder angekündigt wurden.
ms.assetid: 0316e536-ccd4-4d7a-9c49-66e6c4a07f1c
title: Installer. RelatedProducts (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.RelatedProducts
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: fb30be6ea5250a90ef8aa18065e9be679946e503
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361678"
---
# <a name="installerrelatedproducts-property"></a><span data-ttu-id="8b9a7-103">Installer. RelatedProducts (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="8b9a7-103">Installer.RelatedProducts property</span></span>

<span data-ttu-id="8b9a7-104">Die schreibgeschützte **RelatedProducts** -Eigenschaft gibt ein [**stringlist**](stringlist-object.md) -Objekt zurück, das den Satz aller Produkte auflistet, die für den aktuellen Benutzer und Computer mit einer angegebenen [**UpgradeCode**](upgradecode.md) -Eigenschaft in der [Eigenschaften Tabelle](property-table.md)installiert oder angekündigt wurden.</span><span class="sxs-lookup"><span data-stu-id="8b9a7-104">The read-only **RelatedProducts** property returns a [**StringList**](stringlist-object.md) object enumerating the set of all products installed or advertised for the current user and machine with a specified [**UpgradeCode**](upgradecode.md) property in their [Property table](property-table.md).</span></span>

<span data-ttu-id="8b9a7-105">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="8b9a7-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b9a7-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="8b9a7-106">Syntax</span></span>


```JScript
propVal = Installer.RelatedProducts
```



## <a name="property-value"></a><span data-ttu-id="8b9a7-107">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="8b9a7-107">Property value</span></span>

<span data-ttu-id="8b9a7-108">Der UpgradeCode verwandter Produkte, die das Installationsprogramm auflistet.</span><span class="sxs-lookup"><span data-stu-id="8b9a7-108">The upgrade code of related products that the installer enumerates.</span></span>

## <a name="remarks"></a><span data-ttu-id="8b9a7-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8b9a7-109">Remarks</span></span>

<span data-ttu-id="8b9a7-110">Zum Auflisten der zugehörigen Produkte durchläuft eine Anwendung die [**stringlist**](stringlist-object.md) mithilfe eines for Each-Konstrukts.</span><span class="sxs-lookup"><span data-stu-id="8b9a7-110">To enumerate the related products, an application iterates through the [**StringList**](stringlist-object.md) using a For Each construct.</span></span> <span data-ttu-id="8b9a7-111">Da Verwandte Produkte nicht geordnet sind, weist jedes neue verwandte Produkt einen beliebigen Index auf.</span><span class="sxs-lookup"><span data-stu-id="8b9a7-111">Because related products are not ordered, any new related product has an arbitrary index.</span></span> <span data-ttu-id="8b9a7-112">Dies bedeutet, dass die Funktion Verwandte Produkte in beliebiger Reihenfolge zurückgeben kann.</span><span class="sxs-lookup"><span data-stu-id="8b9a7-112">This means that the function can return related products in any order.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b9a7-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8b9a7-113">Requirements</span></span>



| <span data-ttu-id="8b9a7-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8b9a7-114">Requirement</span></span> | <span data-ttu-id="8b9a7-115">Wert</span><span class="sxs-lookup"><span data-stu-id="8b9a7-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b9a7-116">Version</span><span class="sxs-lookup"><span data-stu-id="8b9a7-116">Version</span></span><br/> | <span data-ttu-id="8b9a7-117">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="8b9a7-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="8b9a7-118">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="8b9a7-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="8b9a7-119">Windows Installer unter Windows Server 2003 oder Windows XP</span><span class="sxs-lookup"><span data-stu-id="8b9a7-119">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="8b9a7-120">DLL</span><span class="sxs-lookup"><span data-stu-id="8b9a7-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="8b9a7-121"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8b9a7-121"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="8b9a7-122">IID</span><span class="sxs-lookup"><span data-stu-id="8b9a7-122">IID</span></span><br/>     | <span data-ttu-id="8b9a7-123">IID \_ iinstaller ist definiert als 000c1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="8b9a7-123">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="8b9a7-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8b9a7-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b9a7-125">**Msienumrelatedproducts**</span><span class="sxs-lookup"><span data-stu-id="8b9a7-125">**MsiEnumRelatedProducts**</span></span>](/windows/desktop/api/Msi/nf-msi-msienumrelatedproductsa)
</dt> </dl>

 

 




