---
description: Die Features-Eigenschaft ist eine schreibgeschützte Eigenschaft, die ein stringlist-Objekt zurückgibt, das den Satz veröffentlichter Funktionen für das angegebene Produkt auflistet.
ms.assetid: feb8f09a-fa97-4fee-9082-8f04288af22f
title: Installer. Features (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.Features
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 4f63ce80249fb8bd24d70f92e72c44420a13d798
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360285"
---
# <a name="installerfeatures-property"></a><span data-ttu-id="37092-103">Installer. Features (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="37092-103">Installer.Features property</span></span>

<span data-ttu-id="37092-104">Die **Features** -Eigenschaft ist eine schreibgeschützte Eigenschaft, die ein [**stringlist**](stringlist-object.md) -Objekt zurückgibt, das den Satz veröffentlichter Funktionen für das angegebene Produkt auflistet.</span><span class="sxs-lookup"><span data-stu-id="37092-104">The **Features** property is a read-only property that returns a [**StringList**](stringlist-object.md) object enumerating the set of published features for the specified product.</span></span>

<span data-ttu-id="37092-105">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="37092-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="37092-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="37092-106">Syntax</span></span>


```JScript
propVal = Installer.Features
```



## <a name="property-value"></a><span data-ttu-id="37092-107">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="37092-107">Property value</span></span>

<span data-ttu-id="37092-108">Gibt den Produktcode des Produkts an.</span><span class="sxs-lookup"><span data-stu-id="37092-108">Specifies the product code of the product.</span></span>

## <a name="remarks"></a><span data-ttu-id="37092-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="37092-109">Remarks</span></span>

<span data-ttu-id="37092-110">Um die Funktionen aufzulisten, durchläuft eine Anwendung das [**stringlist**](stringlist-object.md) -Objekt mithilfe eines for Each-Konstrukts.</span><span class="sxs-lookup"><span data-stu-id="37092-110">To enumerate the features, an application iterates through the [**StringList**](stringlist-object.md) object using a For Each construct.</span></span> <span data-ttu-id="37092-111">Da Features nicht sortiert sind, verfügt jede neue Funktion über einen beliebigen Index, was bedeutet, dass die Funktion Funktionen in beliebiger Reihenfolge zurückgeben kann.</span><span class="sxs-lookup"><span data-stu-id="37092-111">Because features are not ordered, any new feature has an arbitrary index, meaning the function can return features in any order.</span></span>

## <a name="requirements"></a><span data-ttu-id="37092-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="37092-112">Requirements</span></span>



| <span data-ttu-id="37092-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="37092-113">Requirement</span></span> | <span data-ttu-id="37092-114">Wert</span><span class="sxs-lookup"><span data-stu-id="37092-114">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37092-115">Version</span><span class="sxs-lookup"><span data-stu-id="37092-115">Version</span></span><br/> | <span data-ttu-id="37092-116">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="37092-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="37092-117">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="37092-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="37092-118">Windows Installer unter Windows Server 2003 oder Windows XP</span><span class="sxs-lookup"><span data-stu-id="37092-118">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="37092-119">DLL</span><span class="sxs-lookup"><span data-stu-id="37092-119">DLL</span></span><br/>     | <dl> <span data-ttu-id="37092-120"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="37092-120"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="37092-121">IID</span><span class="sxs-lookup"><span data-stu-id="37092-121">IID</span></span><br/>     | <span data-ttu-id="37092-122">IID \_ iinstaller ist definiert als 000c1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="37092-122">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="37092-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="37092-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37092-124">**Msienumschlag-Features**</span><span class="sxs-lookup"><span data-stu-id="37092-124">**MsiEnumFeatures**</span></span>](/windows/desktop/api/Msi/nf-msi-msienumfeaturesa)
</dt> <dt>

[<span data-ttu-id="37092-125">System Status Funktionen</span><span class="sxs-lookup"><span data-stu-id="37092-125">System Status Functions</span></span>](installer-function-reference.md)
</dt> </dl>

 

 




