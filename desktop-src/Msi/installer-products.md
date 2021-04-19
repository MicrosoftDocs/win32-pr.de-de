---
description: Die Products-Eigenschaft ist eine schreibgeschützte Eigenschaft, die ein stringlist-Objekt zurückgibt, das den Satz aller Produkte auflistet, die für den aktuellen Benutzer und Computer installiert oder angekündigt wurden.
ms.assetid: 5c210827-a7cc-4358-bfe6-4d8e9767bd8c
title: Installer. Products (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.Products
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 8d5b20a770154382e7e7a68cc3fe4d81c350fb1f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354183"
---
# <a name="installerproducts-property"></a><span data-ttu-id="43193-103">Installer. Products (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="43193-103">Installer.Products property</span></span>

<span data-ttu-id="43193-104">Die **Products** -Eigenschaft ist eine schreibgeschützte Eigenschaft, die ein [**stringlist**](stringlist-object.md) -Objekt zurückgibt, das den Satz aller Produkte auflistet, die für den aktuellen Benutzer und Computer installiert oder angekündigt wurden.</span><span class="sxs-lookup"><span data-stu-id="43193-104">The **Products** property is a read-only property that returns a [**StringList**](stringlist-object.md) object enumerating the set of all products installed or advertised for the current user and machine.</span></span>

<span data-ttu-id="43193-105">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="43193-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="43193-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="43193-106">Syntax</span></span>


```JScript
propVal = Installer.Products
```



## <a name="property-value"></a><span data-ttu-id="43193-107">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="43193-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="43193-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="43193-108">Remarks</span></span>

<span data-ttu-id="43193-109">Zum Auflisten der Produkte durchläuft eine Anwendung das [**stringlist**](stringlist-object.md) -Objekt mithilfe eines for Each-Konstrukts.</span><span class="sxs-lookup"><span data-stu-id="43193-109">To enumerate the products, an application iterates through the [**StringList**](stringlist-object.md) object using a For Each construct.</span></span> <span data-ttu-id="43193-110">Da Produkte nicht geordnet sind, weist jedes neue Produkt einen beliebigen Index auf.</span><span class="sxs-lookup"><span data-stu-id="43193-110">Because products are not ordered, any new product has an arbitrary index.</span></span> <span data-ttu-id="43193-111">Dies bedeutet, dass die Funktion Produkte in beliebiger Reihenfolge zurückgeben kann.</span><span class="sxs-lookup"><span data-stu-id="43193-111">This means that the function can return products in any order.</span></span>

## <a name="requirements"></a><span data-ttu-id="43193-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="43193-112">Requirements</span></span>



| <span data-ttu-id="43193-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="43193-113">Requirement</span></span> | <span data-ttu-id="43193-114">Wert</span><span class="sxs-lookup"><span data-stu-id="43193-114">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="43193-115">Version</span><span class="sxs-lookup"><span data-stu-id="43193-115">Version</span></span><br/> | <span data-ttu-id="43193-116">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="43193-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="43193-117">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="43193-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="43193-118">Windows Installer unter Windows Server 2003 oder Windows XP</span><span class="sxs-lookup"><span data-stu-id="43193-118">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="43193-119">DLL</span><span class="sxs-lookup"><span data-stu-id="43193-119">DLL</span></span><br/>     | <dl> <span data-ttu-id="43193-120"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="43193-120"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="43193-121">IID</span><span class="sxs-lookup"><span data-stu-id="43193-121">IID</span></span><br/>     | <span data-ttu-id="43193-122">IID \_ iinstaller ist definiert als 000c1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="43193-122">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="43193-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="43193-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43193-124">**Msienumschlag Produkte**</span><span class="sxs-lookup"><span data-stu-id="43193-124">**MsiEnumProducts**</span></span>](/windows/desktop/api/Msi/nf-msi-msienumproductsa)
</dt> </dl>

 

 




