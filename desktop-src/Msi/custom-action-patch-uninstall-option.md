---
description: Verwenden Sie das folgende Optionsflag, um anzugeben, dass das Installationsprogramm die benutzerdefinierte Aktion nur dann durchführt, wenn ein Patch deinstalliert wird. Fügen Sie den Wert in dieser Tabelle dem Wert im Feld "extendedtype" der Tabelle "CustomAction" hinzu, um die Option festzulegen.
ms.assetid: aa4d9e21-5316-42b5-a22e-c7a5becd3cae
title: Option zum Deinstallieren von benutzerdefinierten Aktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 108365876393733f7cc520ae565bb2c5ea7ff3df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352587"
---
# <a name="custom-action-patch-uninstall-option"></a><span data-ttu-id="6e5a9-104">Option zum Deinstallieren von benutzerdefinierten Aktionen</span><span class="sxs-lookup"><span data-stu-id="6e5a9-104">Custom Action Patch Uninstall Option</span></span>

<span data-ttu-id="6e5a9-105">Verwenden Sie das folgende Optionsflag, um anzugeben, dass das Installationsprogramm die benutzerdefinierte Aktion nur dann durchführt, wenn ein Patch deinstalliert wird.</span><span class="sxs-lookup"><span data-stu-id="6e5a9-105">Use the following option flag to specify that the installer run the custom action only when a patch is being uninstalled.</span></span> <span data-ttu-id="6e5a9-106">Fügen Sie den Wert in dieser Tabelle dem Wert im Feld "extendedtype" der [Tabelle "CustomAction](customaction-table.md)" hinzu, um die Option festzulegen.</span><span class="sxs-lookup"><span data-stu-id="6e5a9-106">To set the option, add the value in this table to the value in the ExtendedType field of the [CustomAction table](customaction-table.md).</span></span>

<span data-ttu-id="6e5a9-107">**[Windows Installer 4,0 und früher](not-supported-in-windows-installer-4-0.md):** Nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6e5a9-107">**[Windows Installer 4.0 and earlier](not-supported-in-windows-installer-4-0.md):** Not supported.</span></span> <span data-ttu-id="6e5a9-108">Diese Option ist ab Windows Installer 4,5 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6e5a9-108">This option is available beginning with Windows Installer 4.5.</span></span>



| <span data-ttu-id="6e5a9-109">Konstante</span><span class="sxs-lookup"><span data-stu-id="6e5a9-109">Constant</span></span>                                | <span data-ttu-id="6e5a9-110">Hexadezimal</span><span class="sxs-lookup"><span data-stu-id="6e5a9-110">Hexadecimal</span></span> | <span data-ttu-id="6e5a9-111">Decimal</span><span class="sxs-lookup"><span data-stu-id="6e5a9-111">Decimal</span></span> | <span data-ttu-id="6e5a9-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6e5a9-112">Description</span></span>                                                    |
|-----------------------------------------|-------------|---------|----------------------------------------------------------------|
| <span data-ttu-id="6e5a9-113">**msidbcustomaktiontypepatchuninstall**</span><span class="sxs-lookup"><span data-stu-id="6e5a9-113">**msidbCustomActionTypePatchUninstall**</span></span> | <span data-ttu-id="6e5a9-114">0x8000</span><span class="sxs-lookup"><span data-stu-id="6e5a9-114">0x8000</span></span>      | <span data-ttu-id="6e5a9-115">32768</span><span class="sxs-lookup"><span data-stu-id="6e5a9-115">32768</span></span>   | <span data-ttu-id="6e5a9-116">Die benutzerdefinierte Aktion wird nur ausgeführt, wenn ein Patch deinstalliert wird.</span><span class="sxs-lookup"><span data-stu-id="6e5a9-116">The custom action runs only when a patch is being uninstalled.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="6e5a9-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6e5a9-117">Remarks</span></span>

<span data-ttu-id="6e5a9-118">Dieses Attribut kann einer benutzerdefinierten Aktion hinzugefügt werden, indem es im Windows Installer Paket (MSI-Datei) gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="6e5a9-118">This attribute can be added to a custom action by authoring it in the Windows Installer package (.msi file).</span></span> <span data-ttu-id="6e5a9-119">Eine neue benutzerdefinierte Aktion mit diesem Attribut kann von einem Patch hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="6e5a9-119">A new custom action with this attribute can be added by a patch.</span></span> <span data-ttu-id="6e5a9-120">Eine benutzerdefinierte Aktion, in der dieses Attribut vorhanden ist, kann durch einen Patch aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="6e5a9-120">A custom action having this attribute can be updated by a patch.</span></span> <span data-ttu-id="6e5a9-121">Dieses Attribut kann einer vorhandenen benutzerdefinierten Aktion nicht durch einen Patch hinzugefügt oder daraus entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="6e5a9-121">This attribute cannot be added or removed by a patch to an existing custom action.</span></span>

<span data-ttu-id="6e5a9-122">Wenn ein Patch eine benutzerdefinierte Aktion mit diesem Attribut hinzufügt oder aktualisiert, Windows Installer die neue oder aktualisierte benutzerdefinierte Aktion ausführt, wenn der Patch deinstalliert wird.</span><span class="sxs-lookup"><span data-stu-id="6e5a9-122">If a patch adds or updates a custom action with this attribute, Windows Installer runs the new or updated custom action when the patch is uninstalled.</span></span> <span data-ttu-id="6e5a9-123">Durch Windows Installer werden die Updates, die im Patch deinstalliert werden, für die benutzerdefinierte Aktion zum Deinstallieren von Patches verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6e5a9-123">Windows Installer makes the updates within the patch being uninstalled available to the patch uninstall custom action.</span></span> <span data-ttu-id="6e5a9-124">Der Patch muss eine [msitransformview *<PatchGUID>*](msitransformview.md) -Tabelle enthalten, um diese Informationen für Windows Installer bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="6e5a9-124">The patch must include a [MsiTransformView *<PatchGUID>*](msitransformview.md) table to provide this information to Windows Installer.</span></span>

<span data-ttu-id="6e5a9-125">Wenn ein Paket, das eine benutzerdefinierte Aktion mit dem **msidbcustomaction typepatchuninstall** -Attribut enthält, unter Verwendung einer Installerversion vor Windows Installer 4,0 installiert wird, ruft das Installationsprogramm die benutzerdefinierte Aktion nicht auf, wenn der Patch deinstalliert wird.</span><span class="sxs-lookup"><span data-stu-id="6e5a9-125">When a package that contains a custom action with the **msidbCustomActionTypePatchUninstall** attribute is installed using an installer version earlier than Windows Installer 4.0, the installer does not call the custom action when the patch is uninstalled.</span></span> <span data-ttu-id="6e5a9-126">Die Installation kann die benutzerdefinierte Aktion während der Installation, Reparatur oder Aktualisierung des Pakets ausführen.</span><span class="sxs-lookup"><span data-stu-id="6e5a9-126">The install can run the custom action during the installation, repair, or update of the package.</span></span>

<span data-ttu-id="6e5a9-127">Benutzerdefinierte Aktionen mit dem **msidbcustomaction typepatchuninstall** -Attribut sollten mithilfe der [**msipatchremove**](msipatchremove.md) -Eigenschaft bedingt werden, um zu verhindern, dass die benutzerdefinierte Aktion beim Installieren, reparieren oder aktualisieren mit einem System mit Windows Installer 4,0 oder früher ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6e5a9-127">Custom actions with the **msidbCustomActionTypePatchUninstall** attribute should be conditioned using the [**MSIPATCHREMOVE**](msipatchremove.md) property to prevent the custom action from running when installing, repairing, or updating using a system with Windows Installer 4.0 or earlier.</span></span> <span data-ttu-id="6e5a9-128">Wenn Windows Installer 4,5 und höher installiert ist, wird bei der Deinstallation des Patches für alle Patches auf dem System, die mit dem **msidbcustomaction typepatchuninstall** -Attribut gekennzeichnet sind, die benutzerdefinierte Aktion ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6e5a9-128">When Windows Installer 4.5 and later is installed, all the patches on the system having custom actions marked with the **msidbCustomActionTypePatchUninstall** attribute run the custom action during patch uninstallation.</span></span> <span data-ttu-id="6e5a9-129">Wenn Windows Installer 4,5 oder höher aus dem System entfernt wird, verlieren Patches die Funktion zum Deinstallieren von benutzerdefinierten Aktions Patches.</span><span class="sxs-lookup"><span data-stu-id="6e5a9-129">If Windows Installer 4.5 or later is removed from the system, patches lose the custom action patch uninstall functionality.</span></span>

<span data-ttu-id="6e5a9-130">Informationen zum Ausführen einer benutzerdefinierten Aktion während der Deinstallation eines Patches mit einer früheren Version als Windows Installer 4,5 finden Sie unter [Patch Uninstall Custom Actions](patch-uninstall-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="6e5a9-130">For information about running a custom action during the uninstallation of a patch using a version earlier than Windows Installer 4.5, see [Patch Uninstall Custom Actions](patch-uninstall-custom-actions.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="6e5a9-131">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6e5a9-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6e5a9-132">Benutzerdefinierte Aktion In-Script Ausführungs Optionen</span><span class="sxs-lookup"><span data-stu-id="6e5a9-132">Custom Action In-Script Execution Options</span></span>](custom-action-in-script-execution-options.md)
</dt> <dt>

[<span data-ttu-id="6e5a9-133">Referenz zu benutzerdefinierten Aktionen</span><span class="sxs-lookup"><span data-stu-id="6e5a9-133">Custom Action Reference</span></span>](custom-action-reference.md)
</dt> <dt>

[<span data-ttu-id="6e5a9-134">Informationen zu benutzerdefinierten Aktionen</span><span class="sxs-lookup"><span data-stu-id="6e5a9-134">About Custom Actions</span></span>](about-custom-actions.md)
</dt> <dt>

[<span data-ttu-id="6e5a9-135">Verwenden von benutzerdefinierten Aktionen</span><span class="sxs-lookup"><span data-stu-id="6e5a9-135">Using Custom Actions</span></span>](using-custom-actions.md)
</dt> <dt>

[<span data-ttu-id="6e5a9-136">Msitransformview *<PatchGUID>*</span><span class="sxs-lookup"><span data-stu-id="6e5a9-136">MsiTransformView *<PatchGUID>*</span></span>](msitransformview.md)
</dt> </dl>

 

 



