---
description: Mit der Option zum Deinstallieren von benutzerdefinierten Aktionen können Sie angeben, dass das Installationsprogramm die benutzerdefinierte Aktion nur dann ausführen soll, wenn ein Patch deinstalliert wird.
ms.assetid: c741aa40-ba4c-459e-936a-19c002620c30
title: Patch zum Deinstallieren benutzerdefinierter Aktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b90cfffbdb37f1f2fab046b794010a790e9a5212
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106340187"
---
# <a name="patch-uninstall-custom-actions"></a><span data-ttu-id="a96e7-103">Patch zum Deinstallieren benutzerdefinierter Aktionen</span><span class="sxs-lookup"><span data-stu-id="a96e7-103">Patch Uninstall Custom Actions</span></span>

<span data-ttu-id="a96e7-104">Mit der Option zum [Deinstallieren von benutzerdefinierten Aktionen](custom-action-patch-uninstall-option.md) können Sie angeben, dass das Installationsprogramm die benutzerdefinierte Aktion nur dann ausführen soll, wenn ein Patch deinstalliert wird.</span><span class="sxs-lookup"><span data-stu-id="a96e7-104">You can use the [Custom Action Patch Uninstall option](custom-action-patch-uninstall-option.md) to specify that the installer run the custom action only when a patch is uninstalled.</span></span>

<span data-ttu-id="a96e7-105">**Windows Installer 4,5 und höher:** Sie können die [Option zum Deinstallieren von benutzerdefinierten Aktionen](custom-action-patch-uninstall-option.md) verwenden, um anzugeben, dass das Installationsprogramm nur die benutzerdefinierte Aktion ausführen soll, wenn ein Patch deinstalliert wird.</span><span class="sxs-lookup"><span data-stu-id="a96e7-105">**Windows Installer 4.5 and later:** You can use the [Custom Action Patch Uninstall Option](custom-action-patch-uninstall-option.md) to specify that the installer only run the custom action when a patch is uninstalled.</span></span>

<span data-ttu-id="a96e7-106">\*\*[Windows Installer 4,0 und früher](not-supported-in-windows-installer-4-0.md): \* \*</span><span class="sxs-lookup"><span data-stu-id="a96e7-106">\*\*[Windows Installer 4.0 and earlier](not-supported-in-windows-installer-4-0.md):  \*\*</span></span>

<span data-ttu-id="a96e7-107">Die [Option zum Deinstallieren des benutzerdefinierten Aktions Patches](custom-action-patch-uninstall-option.md) ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a96e7-107">The [Custom Action Patch Uninstall option](custom-action-patch-uninstall-option.md) is not available.</span></span> <span data-ttu-id="a96e7-108">Es gibt keine Möglichkeit, eine [benutzerdefinierte Aktion](custom-actions.md) innerhalb eines Patchpakets zu markieren, die ausgeführt wird, wenn der Patch deinstalliert wird, da das Installationsprogramm nicht die zu installierenden Patchpakete anwendet.</span><span class="sxs-lookup"><span data-stu-id="a96e7-108">There is no method for marking a [custom action](custom-actions.md) within a patch package to be run when the patch is uninstalled because the installer does not apply the patch packages being uninstalled.</span></span>

<span data-ttu-id="a96e7-109">Um eine [benutzerdefinierte Aktion](custom-actions.md) auszuführen, wenn ein bestimmter Patch deinstalliert wird, muss die benutzerdefinierte Aktion entweder in der ursprünglichen Anwendung vorhanden sein oder sich in einem Patch für das Produkt befinden, das immer angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="a96e7-109">To have a [custom action](custom-actions.md) run when a particular patch is uninstalled, the custom action must either be present in the original application or be in a patch for the product that is always applied.</span></span>

<span data-ttu-id="a96e7-110">Entwickler können die [**msipatchremovallist**](msipatchremovallist.md) -Eigenschaft verwenden, um ein Windows Installer Paket oder einen Patch zu erstellen, der beim Entfernen eines Patches [benutzerdefinierte Aktionen](custom-actions.md) ausführt.</span><span class="sxs-lookup"><span data-stu-id="a96e7-110">Developers can use the [**MsiPatchRemovalList**](msipatchremovallist.md) property to author a Windows Installer package or patch that performs [custom actions](custom-actions.md) on the removal of a patch.</span></span> <span data-ttu-id="a96e7-111">Die benutzerdefinierte Aktion kann im ursprünglichen Installationspaket, einem Patch, der bereits auf das Paket angewendet wurde, oder einem Patch, bei dem es sich nicht um einen nicht [installierbaren Patch](uninstallable-patches.md)handelt, erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="a96e7-111">The custom action can be authored into the original installation package, a patch that has already been applied to the package, or a patch that is not an [uninstallable patch](uninstallable-patches.md).</span></span> <span data-ttu-id="a96e7-112">Die benutzerdefinierte Aktion kann für die **msipatchremovallist** -Eigenschaft in den Sequenz Tabellen conditionalisiert werden.</span><span class="sxs-lookup"><span data-stu-id="a96e7-112">The custom action can be conditionalized on the **MsiPatchRemovalList** property in the sequence tables.</span></span> <span data-ttu-id="a96e7-113">Weitere Informationen zu conditionalisierungsaktionen finden [Sie unter Verwenden von Eigenschaften in Bedingungs Anweisungen](using-properties-in-conditional-statements.md) .</span><span class="sxs-lookup"><span data-stu-id="a96e7-113">See [Using Properties in Conditional Statements](using-properties-in-conditional-statements.md) for more information about conditionalizing actions.</span></span>

<span data-ttu-id="a96e7-114">Die benutzerdefinierte Aktion kann die GUIDs von Patches abrufen, die aus dem Wert der [**msipatchremovallist**](msipatchremovallist.md) -Eigenschaft entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="a96e7-114">The custom action can obtain the GUIDs of patches being removed from the value of the [**MsiPatchRemovalList**](msipatchremovallist.md) property.</span></span> <span data-ttu-id="a96e7-115">Die benutzerdefinierte Aktion kann ermitteln, ob der Installationsstatus des Patches angewendet, veraltet oder ersetzt wird, indem die [**msigetpatchinfoex**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa) -Eigenschaft oder die [**patchproperty**](patch-patchproperty.md) -Eigenschaft des [Patch-Objekts](patch-object.md)aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="a96e7-115">The custom action can determine whether the installation state of the patch is applied, obsolete, or superseded by calling the [**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa) or the [**PatchProperty**](patch-patchproperty.md) property of the [Patch object](patch-object.md).</span></span>

<span data-ttu-id="a96e7-116">Wenn für die benutzerdefinierte Aktion besondere Metadaten aus dem Patch erforderlich sind, sollte der Patch eine benutzerdefinierte Aktion enthalten, die die Metadaten in einen Registrierungs-oder Datei Speicherort schreibt, wenn der Patch angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="a96e7-116">If the custom action requires special metadata from the patch, the patch should contain a custom action that writes the metadata to a registry or file location when the patch is applied.</span></span> <span data-ttu-id="a96e7-117">Die benutzerdefinierte Aktion in der ursprünglichen Anwendung oder ein Patch, das immer angewendet wird, kann die zum Entfernen der Änderungen des Patches benötigten Informationen abrufen.</span><span class="sxs-lookup"><span data-stu-id="a96e7-117">The custom action in the original application or a patch that is always applied can obtain the information needed to remove the patch's changes.</span></span>

<span data-ttu-id="a96e7-118">Patches, die Änderungen vornehmen, die nur schwer rückgängig gemacht werden können, sollten nicht als [nicht installierbare Patches](uninstallable-patches.md)gekennzeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="a96e7-118">Patches making changes that are difficult to undo correctly should not be marked as [uninstallable patches](uninstallable-patches.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a96e7-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a96e7-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a96e7-120">Patchsequenzierung</span><span class="sxs-lookup"><span data-stu-id="a96e7-120">Patch Sequencing</span></span>](sequencing-patches.md)
</dt> <dt>

[<span data-ttu-id="a96e7-121">Entfernen von Patches</span><span class="sxs-lookup"><span data-stu-id="a96e7-121">Removing Patches</span></span>](removing-patches.md)
</dt> <dt>

[<span data-ttu-id="a96e7-122">Nicht installierbare Patches</span><span class="sxs-lookup"><span data-stu-id="a96e7-122">Uninstallable Patches</span></span>](uninstallable-patches.md)
</dt> <dt>

[<span data-ttu-id="a96e7-123">Patches werden deinstalliert.</span><span class="sxs-lookup"><span data-stu-id="a96e7-123">Uninstalling Patches</span></span>](uninstalling-patches.md)
</dt> <dt>

[<span data-ttu-id="a96e7-124">**Msipatchremove**</span><span class="sxs-lookup"><span data-stu-id="a96e7-124">**MSIPATCHREMOVE**</span></span>](msipatchremove.md)
</dt> <dt>

[<span data-ttu-id="a96e7-125">**Msienumapplicationsex**</span><span class="sxs-lookup"><span data-stu-id="a96e7-125">**MsiEnumapplicationsEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msienumproductsexa)
</dt> <dt>

[<span data-ttu-id="a96e7-126">**Msigetpatchinfoex**</span><span class="sxs-lookup"><span data-stu-id="a96e7-126">**MsiGetPatchInfoEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa)
</dt> <dt>

[<span data-ttu-id="a96e7-127">**Msiremovepatches**</span><span class="sxs-lookup"><span data-stu-id="a96e7-127">**MsiRemovePatches**</span></span>](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa)
</dt> </dl>

 

 



