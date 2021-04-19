---
description: Die Eigenschaft schreibgeschützte Komponenten gibt ein stringlist-Objekt zurück, das den Satz der installierten Komponenten für alle Produkte auflistet.
ms.assetid: c84e4329-428a-440a-bd65-097588a86932
title: Installer. Components (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.Components
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e6767be5182b15836c071bf8b00ed8441f6031dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368651"
---
# <a name="installercomponents-property"></a><span data-ttu-id="7c5c8-103">Installer. Components (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="7c5c8-103">Installer.Components property</span></span>

<span data-ttu-id="7c5c8-104">Die Eigenschaft schreibgeschützte **Komponenten** gibt ein [**stringlist**](stringlist-object.md) -Objekt zurück, das den Satz der installierten Komponenten für alle Produkte auflistet.</span><span class="sxs-lookup"><span data-stu-id="7c5c8-104">The read-only **Components** property returns a [**StringList**](stringlist-object.md) object enumerating the set of installed components for all products.</span></span>

<span data-ttu-id="7c5c8-105">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="7c5c8-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c5c8-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="7c5c8-106">Syntax</span></span>


```JScript
propVal = Installer.Components
```



## <a name="property-value"></a><span data-ttu-id="7c5c8-107">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="7c5c8-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="7c5c8-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7c5c8-108">Remarks</span></span>

<span data-ttu-id="7c5c8-109">Zum Auflisten der Komponenten kann eine Anwendung das [**stringlist**](stringlist-object.md) -Objekt durchlaufen, indem ein-Objekt für jedes Konstrukt verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7c5c8-109">To enumerate the components, an application can iterate through the [**StringList**](stringlist-object.md) object using a For Each construct.</span></span> <span data-ttu-id="7c5c8-110">Da Komponenten nicht geordnet sind, haben alle neuen Komponenten einen beliebigen Index.</span><span class="sxs-lookup"><span data-stu-id="7c5c8-110">Because components are not ordered, any new components has an arbitrary index.</span></span> <span data-ttu-id="7c5c8-111">Dies bedeutet, dass die Funktion Komponenten in beliebiger Reihenfolge zurückgeben kann.</span><span class="sxs-lookup"><span data-stu-id="7c5c8-111">This means that the function can return components in any order.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c5c8-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7c5c8-112">Requirements</span></span>



| <span data-ttu-id="7c5c8-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7c5c8-113">Requirement</span></span> | <span data-ttu-id="7c5c8-114">Wert</span><span class="sxs-lookup"><span data-stu-id="7c5c8-114">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c5c8-115">Version</span><span class="sxs-lookup"><span data-stu-id="7c5c8-115">Version</span></span><br/> | <span data-ttu-id="7c5c8-116">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="7c5c8-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="7c5c8-117">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="7c5c8-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="7c5c8-118">Windows Installer unter Windows Server 2003 oder Windows XP</span><span class="sxs-lookup"><span data-stu-id="7c5c8-118">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="7c5c8-119">DLL</span><span class="sxs-lookup"><span data-stu-id="7c5c8-119">DLL</span></span><br/>     | <dl> <span data-ttu-id="7c5c8-120"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7c5c8-120"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="7c5c8-121">IID</span><span class="sxs-lookup"><span data-stu-id="7c5c8-121">IID</span></span><br/>     | <span data-ttu-id="7c5c8-122">IID \_ iinstaller ist definiert als 000c1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="7c5c8-122">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="7c5c8-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7c5c8-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c5c8-124">**Msienumschlag Components**</span><span class="sxs-lookup"><span data-stu-id="7c5c8-124">**MsiEnumComponents**</span></span>](/windows/desktop/api/Msi/nf-msi-msienumcomponentsa)
</dt> </dl>

 

 




