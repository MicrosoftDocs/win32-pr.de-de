---
description: Das Installationsprogramm legt den Wert der msipatchremovallist-Eigenschaft auf eine Liste von Patches fest, die während der Installation entfernt werden.
ms.assetid: 6e0b391a-d840-4f01-af12-4708ce6c9ce8
title: Msipatchremovallist (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2af522d9570297f2ff911b501bc543cf4b5971c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354089"
---
# <a name="msipatchremovallist-property"></a><span data-ttu-id="ce9bf-103">Msipatchremovallist (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="ce9bf-103">MsiPatchRemovalList property</span></span>

<span data-ttu-id="ce9bf-104">Das Installationsprogramm legt den Wert der **msipatchremovallist** -Eigenschaft auf eine Liste von Patches fest, die während der Installation entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="ce9bf-104">The installer sets the value of the **MsiPatchRemovalList** property to a list of patches that are being removed during the installation.</span></span> <span data-ttu-id="ce9bf-105">Die Patches werden in der Liste durch die durch Semikolons getrennten patchcodeguids dargestellt.</span><span class="sxs-lookup"><span data-stu-id="ce9bf-105">The patches are represented in the list by their patch code GUIDs separated by semicolons.</span></span>

<span data-ttu-id="ce9bf-106">Entwickler können die **msipatchremovallist** -Eigenschaft verwenden, um ein Windows Installer Paket oder einen Patch zu erstellen, der beim Entfernen eines Patches [benutzerdefinierte Aktionen](custom-actions.md) ausführt.</span><span class="sxs-lookup"><span data-stu-id="ce9bf-106">Developers can use the **MsiPatchRemovalList** property to author a Windows Installer package or patch that performs [custom actions](custom-actions.md) on the removal of a patch.</span></span> <span data-ttu-id="ce9bf-107">Die benutzerdefinierte Aktion kann im ursprünglichen Installationspaket, einem Patch, der bereits auf das Paket angewendet wurde, oder einem Patch, bei dem es sich nicht um einen nicht [installierbaren Patch](uninstallable-patches.md)handelt, erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="ce9bf-107">The custom action can be authored into the original installation package, a patch that has already been applied to the package, or a patch that is not an [uninstallable patch](uninstallable-patches.md).</span></span> <span data-ttu-id="ce9bf-108">Die benutzerdefinierte Aktion kann für die **msipatchremovallist** -Eigenschaft in den Sequenz Tabellen conditionalisiert werden.</span><span class="sxs-lookup"><span data-stu-id="ce9bf-108">The custom action can be conditionalized on the **MsiPatchRemovalList** property in the sequence tables.</span></span> <span data-ttu-id="ce9bf-109">Weitere Informationen zu conditionalisierungsaktionen finden [Sie unter Verwenden von Eigenschaften in Bedingungs Anweisungen](using-properties-in-conditional-statements.md) .</span><span class="sxs-lookup"><span data-stu-id="ce9bf-109">See [Using Properties in Conditional Statements](using-properties-in-conditional-statements.md) for more information about conditionalizing actions.</span></span>

<span data-ttu-id="ce9bf-110">Die benutzerdefinierte Aktion kann die GUIDs von Patches abrufen, die aus dem Wert der **msipatchremovallist** -Eigenschaft entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="ce9bf-110">The custom action can obtain the GUIDs of patches being removed from the value of the **MsiPatchRemovalList** property.</span></span> <span data-ttu-id="ce9bf-111">Die benutzerdefinierte Aktion kann ermitteln, ob der Installationsstatus des Patches angewendet, veraltet oder ersetzt wird, indem die [**msigetpatchinfoex**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa) -Funktion oder die [**patchproperty**](patch-patchproperty.md) -Eigenschaft des [Patch-Objekts](patch-object.md)aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="ce9bf-111">The custom action can determine whether the installation state of the patch is applied, obsolete, or superseded by calling the [**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa) function or the [**PatchProperty**](patch-patchproperty.md) property of the [Patch object](patch-object.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ce9bf-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ce9bf-112">Remarks</span></span>

<span data-ttu-id="ce9bf-113">Weitere Informationen zum Entfernen von Patches finden Sie unter [Entfernen von Patches](removing-patches.md).</span><span class="sxs-lookup"><span data-stu-id="ce9bf-113">For more information about removing patches, see [Removing Patches](removing-patches.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ce9bf-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ce9bf-114">Requirements</span></span>



| <span data-ttu-id="ce9bf-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ce9bf-115">Requirement</span></span> | <span data-ttu-id="ce9bf-116">Wert</span><span class="sxs-lookup"><span data-stu-id="ce9bf-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce9bf-117">Version</span><span class="sxs-lookup"><span data-stu-id="ce9bf-117">Version</span></span><br/> | <span data-ttu-id="ce9bf-118">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="ce9bf-118">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="ce9bf-119">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="ce9bf-119">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="ce9bf-120">Windows Installer 3,0 oder höher unter Windows Server 2003 oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="ce9bf-120">Windows Installer 3.0 or later on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="ce9bf-121">Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="ce9bf-121">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ce9bf-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ce9bf-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce9bf-123">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ce9bf-123">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="ce9bf-124">Wird in Windows Installer 2,0 und früher nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ce9bf-124">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




