---
description: Die componentqualifizierereigenschaft ist eine schreibgeschützte Eigenschaft, die ein stringlist-Objekt zurückgibt, das den Satz registrierter Qualifizierer für die angegebene Komponente auflistet.
ms.assetid: 49b16c9a-ce84-42ff-af1d-f4ecf7dbe23a
title: Installer. componentqualifizierereigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ComponentQualifiers
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 0e6f58850974eaa2021578f0d56015ea0ef6d9e1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365478"
---
# <a name="installercomponentqualifiers-property"></a><span data-ttu-id="96d5c-103">Installer. componentqualifizierereigenschaft</span><span class="sxs-lookup"><span data-stu-id="96d5c-103">Installer.ComponentQualifiers property</span></span>

<span data-ttu-id="96d5c-104">Die **componentqualifizierereigenschaft** ist eine schreibgeschützte Eigenschaft, die ein [**stringlist**](stringlist-object.md) -Objekt zurückgibt, das den Satz registrierter Qualifizierer für die angegebene Komponente auflistet.</span><span class="sxs-lookup"><span data-stu-id="96d5c-104">The **ComponentQualifiers** property is a read-only property that returns a [**StringList**](stringlist-object.md) object enumerating the set of registered qualifiers for the specified component.</span></span>

<span data-ttu-id="96d5c-105">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="96d5c-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="96d5c-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="96d5c-106">Syntax</span></span>


```JScript
propVal = Installer.ComponentQualifiers
```



## <a name="property-value"></a><span data-ttu-id="96d5c-107">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="96d5c-107">Property value</span></span>

<span data-ttu-id="96d5c-108">Eine Zeichen folgen-GUID, die die Kategorie der [Komponente](publishcomponent-table.md)darstellt.</span><span class="sxs-lookup"><span data-stu-id="96d5c-108">A string GUID that represents the category of [component](publishcomponent-table.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="96d5c-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="96d5c-109">Remarks</span></span>

<span data-ttu-id="96d5c-110">Zum Auflisten der Qualifizierer durchläuft die Anwendung das [**stringlist**](stringlist-object.md) -Objekt mithilfe eines for Each-Konstrukts.</span><span class="sxs-lookup"><span data-stu-id="96d5c-110">To enumerate qualifiers the application iterates through the [**StringList**](stringlist-object.md) object using a For Each construct.</span></span> <span data-ttu-id="96d5c-111">Da Qualifizierer nicht sortiert sind, verfügt jeder neue Qualifizierer über einen beliebigen Index, was bedeutet, dass die Funktion Qualifizierer in beliebiger Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="96d5c-111">Because qualifiers are not ordered, any new qualifier has an arbitrary index, meaning the function can return qualifiers in any order.</span></span>

## <a name="requirements"></a><span data-ttu-id="96d5c-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="96d5c-112">Requirements</span></span>



| <span data-ttu-id="96d5c-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="96d5c-113">Requirement</span></span> | <span data-ttu-id="96d5c-114">Wert</span><span class="sxs-lookup"><span data-stu-id="96d5c-114">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="96d5c-115">Version</span><span class="sxs-lookup"><span data-stu-id="96d5c-115">Version</span></span><br/> | <span data-ttu-id="96d5c-116">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="96d5c-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="96d5c-117">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="96d5c-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="96d5c-118">Windows Installer unter Windows Server 2003 oder Windows XP</span><span class="sxs-lookup"><span data-stu-id="96d5c-118">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="96d5c-119">DLL</span><span class="sxs-lookup"><span data-stu-id="96d5c-119">DLL</span></span><br/>     | <dl> <span data-ttu-id="96d5c-120"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="96d5c-120"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="96d5c-121">IID</span><span class="sxs-lookup"><span data-stu-id="96d5c-121">IID</span></span><br/>     | <span data-ttu-id="96d5c-122">IID \_ iinstaller ist definiert als 000c1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="96d5c-122">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="96d5c-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="96d5c-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96d5c-124">**Msienumschlag componentqualifizierer**</span><span class="sxs-lookup"><span data-stu-id="96d5c-124">**MsiEnumComponentQualifiers**</span></span>](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa)
</dt> </dl>

 

 




