---
description: Der Wert der ProductVersion-Eigenschaft ist die Version des Produkts im Zeichen folgen Format.
ms.assetid: 551fca7e-a827-482d-bc56-ff2fe5a17025
title: ProductVersion-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01f82fcbd28c4a4132e4c3f76adfd68e33c43b36
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354678"
---
# <a name="productversion-property"></a><span data-ttu-id="517c0-103">ProductVersion-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="517c0-103">ProductVersion property</span></span>

<span data-ttu-id="517c0-104">Der Wert der **ProductVersion** -Eigenschaft ist die Version des Produkts im Zeichen folgen Format.</span><span class="sxs-lookup"><span data-stu-id="517c0-104">The value of the **ProductVersion** property is the version of the product in string format.</span></span> <span data-ttu-id="517c0-105">Diese Eigenschaft ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="517c0-105">This property is REQUIRED.</span></span>

<span data-ttu-id="517c0-106">Das Format der Zeichenfolge lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="517c0-106">The format of the string is as follows:</span></span>

<dl> <span data-ttu-id="517c0-107">Hauptversion.Nebenversion.Build</span><span class="sxs-lookup"><span data-stu-id="517c0-107">major.minor.build</span></span>  
</dl>

<span data-ttu-id="517c0-108">Das erste Feld ist die Hauptversion und hat einen maximalen Wert von 255.</span><span class="sxs-lookup"><span data-stu-id="517c0-108">The first field is the major version and has a maximum value of 255.</span></span> <span data-ttu-id="517c0-109">Das zweite Feld ist die neben Version und hat einen maximalen Wert von 255.</span><span class="sxs-lookup"><span data-stu-id="517c0-109">The second field is the minor version and has a maximum value of 255.</span></span> <span data-ttu-id="517c0-110">Das dritte Feld wird als Buildversion oder Update Version bezeichnet und hat den maximalen Wert 65.535.</span><span class="sxs-lookup"><span data-stu-id="517c0-110">The third field is called the build version or the update version and has a maximum value of 65,535.</span></span>

## <a name="remarks"></a><span data-ttu-id="517c0-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="517c0-111">Remarks</span></span>

<span data-ttu-id="517c0-112">Mindestens eines der drei Felder von **ProductVersion** muss sich bei einem Upgrade mithilfe der [upgradetabelle](upgrade-table.md)ändern.</span><span class="sxs-lookup"><span data-stu-id="517c0-112">At least one of the three fields of **ProductVersion** must change for an upgrade using the [Upgrade table](upgrade-table.md).</span></span> <span data-ttu-id="517c0-113">Alle Updates, die nur den Paketcode ändern, aber " **ProductVersion** " und " [**ProductCode**](productcode.md) " unverändert bleiben, werden als [kleines Update](small-updates.md)bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="517c0-113">Any update that changes only the package code, but leaves **ProductVersion** and [**ProductCode**](productcode.md) unchanged is called a [small update](small-updates.md).</span></span> <span data-ttu-id="517c0-114">Die drei Versions Felder werden hauptsächlich zur einfacheren Bereitstellung bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="517c0-114">The three versions fields are provided primarily for convenience.</span></span> <span data-ttu-id="517c0-115">Wenn Sie z. **b. ProductVersion** ändern, aber weder die Haupt-noch die neben Version ändern möchten, können Sie die Buildversion ändern.</span><span class="sxs-lookup"><span data-stu-id="517c0-115">For example, if you want to change **ProductVersion**, but do not want to change either the major or minor versions, you can change the build version.</span></span>

<span data-ttu-id="517c0-116">Beachten Sie, dass Windows Installer nur die ersten drei Felder der Produktversion verwendet.</span><span class="sxs-lookup"><span data-stu-id="517c0-116">Note that Windows Installer uses only the first three fields of the product version.</span></span> <span data-ttu-id="517c0-117">Wenn Sie ein viertes Feld in Ihre Produktversion einschließen, wird das vierte Feld vom Installationsprogramm ignoriert.</span><span class="sxs-lookup"><span data-stu-id="517c0-117">If you include a fourth field in your product version, the installer ignores the fourth field.</span></span>

## <a name="requirements"></a><span data-ttu-id="517c0-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="517c0-118">Requirements</span></span>



| <span data-ttu-id="517c0-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="517c0-119">Requirement</span></span> | <span data-ttu-id="517c0-120">Wert</span><span class="sxs-lookup"><span data-stu-id="517c0-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="517c0-121">Version</span><span class="sxs-lookup"><span data-stu-id="517c0-121">Version</span></span><br/> | <span data-ttu-id="517c0-122">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="517c0-122">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="517c0-123">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="517c0-123">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="517c0-124">Windows Installer unter Windows Server 2003 oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="517c0-124">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="517c0-125">Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="517c0-125">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="517c0-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="517c0-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="517c0-127">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="517c0-127">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="517c0-128">Patchen und Upgrades</span><span class="sxs-lookup"><span data-stu-id="517c0-128">Patching and Upgrades</span></span>](patching-and-upgrades.md)
</dt> <dt>

[<span data-ttu-id="517c0-129">kleines Update</span><span class="sxs-lookup"><span data-stu-id="517c0-129">small update</span></span>](small-updates.md)
</dt> </dl>

 

 




