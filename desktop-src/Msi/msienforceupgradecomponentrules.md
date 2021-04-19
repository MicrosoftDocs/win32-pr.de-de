---
description: Legen Sie die Eigenschaft msienforceupgradecomponentrules in der Befehlszeile oder in der Eigenschaften Tabelle auf 1 fest, um die upgradekomponentenregeln bei kleinen Updates und geringfügigen Upgrades eines bestimmten Produkts anzuwenden.
ms.assetid: 0c8424c7-ab9b-4a09-aaa8-6a3f44c2789f
title: Msienforceupgradecomponentrules (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85d5946ba3a0001c988ddfe76eeaf95c008205b7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368575"
---
# <a name="msienforceupgradecomponentrules-property"></a><span data-ttu-id="c5290-103">Msienforceupgradecomponentrules (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="c5290-103">MSIENFORCEUPGRADECOMPONENTRULES property</span></span>

<span data-ttu-id="c5290-104">Legen Sie die Eigenschaft **msienforceupgradecomponentrules** in der Befehlszeile oder in der [Eigenschaften Tabelle](property-table.md) auf 1 fest, um die upgradekomponentenregeln bei [kleinen Updates](small-updates.md) und [geringfügigen Upgrades](minor-upgrades.md) eines bestimmten Produkts anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="c5290-104">Set the **MSIENFORCEUPGRADECOMPONENTRULES** property to 1 on the command line or in the [Property table](property-table.md) to apply the upgrade component rules during [small updates](small-updates.md) and [minor upgrades](minor-upgrades.md) of a particular product.</span></span> <span data-ttu-id="c5290-105">Wenn Sie die Regeln bei kleinen Updates und geringfügigen Upgrades aller Produkte auf dem Computer anwenden möchten, legen Sie die [enforceupgradecomponentrules](enforceupgradecomponentrules.md) -Richtlinie auf 1 fest.</span><span class="sxs-lookup"><span data-stu-id="c5290-105">To apply the rules during small updates and minor upgrades of all products on the computer, set the [EnforceUpgradeComponentRules](enforceupgradecomponentrules.md) policy to 1.</span></span>

<span data-ttu-id="c5290-106">Wenn die Eigenschaft oder die Richtlinie auf 1 festgelegt ist, können [kleine Updates](small-updates.md) und [kleinere Upgrades](minor-upgrades.md) fehlschlagen, da das Update versucht, Folgendes auszuführen, das gegen die Regeln der upgradekomponente verstößt:</span><span class="sxs-lookup"><span data-stu-id="c5290-106">When the property or policy is set to 1, [small updates](small-updates.md) and [minor upgrades](minor-upgrades.md) can fail because the update tries to do the following that violates the upgrade component rules:</span></span>

-   <span data-ttu-id="c5290-107">Fügen Sie am Anfang oder in der Mitte einer vorhandenen Funktionsstruktur ein neues Feature hinzu.</span><span class="sxs-lookup"><span data-stu-id="c5290-107">Add a new feature to the top or middle of an existing feature tree.</span></span>

    <span data-ttu-id="c5290-108">Die neue Funktion muss als neue Blatt Funktion zu einer vorhandenen Funktionsstruktur hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="c5290-108">The new feature must be added as a new leaf feature to an existing feature tree.</span></span>

    <span data-ttu-id="c5290-109">In diesem Fall kann der [**ProductCode**](productcode.md) des Produkts geändert werden, und das Update kann als [großes Upgrade](major-upgrades.md)behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="c5290-109">In this case, the [**ProductCode**](productcode.md) of the product can be changed and the update can be treated as a [major upgrade](major-upgrades.md).</span></span>

-   <span data-ttu-id="c5290-110">Entfernen einer Komponente aus einer Funktion.</span><span class="sxs-lookup"><span data-stu-id="c5290-110">Remove a component from a feature.</span></span>

    <span data-ttu-id="c5290-111">Dies kann auch vorkommen, wenn Sie die GUID einer Komponente ändern.</span><span class="sxs-lookup"><span data-stu-id="c5290-111">This can also occur if you change the GUID of a component.</span></span> <span data-ttu-id="c5290-112">Die von der ursprünglichen GUID identifizierte Komponente scheint entfernt zu werden, und die von der neuen GUID identifizierte Komponente wird als neue Komponente angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c5290-112">The component identified by the original GUID appears to be removed and the component as identified by the new GUID appears as a new component.</span></span>

    <span data-ttu-id="c5290-113">**Windows Installer 4,5 und höher:** Die Komponente kann mithilfe von Windows Installer 4,5 und höher ordnungsgemäß entfernt werden, indem das **msidbcomponentattributesuninstallonabgelöst** -Attribut in der [Component-Tabelle](component-table.md) festgelegt oder die [**msiuninstallablösung dedcomponents**](msiuninstallsupersededcomponents.md) -Eigenschaft festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="c5290-113">**Windows Installer 4.5 and later:** The component can be removed correctly using Windows Installer 4.5 and later by setting the **msidbComponentAttributesUninstallOnSupersedence** attribute in the [Component Table](component-table.md) or by setting the [**MSIUNINSTALLSUPERSEDEDCOMPONENTS**](msiuninstallsupersededcomponents.md) property.</span></span>

    <span data-ttu-id="c5290-114">Alternativ kann der [**ProductCode**](productcode.md) des Produkts geändert werden, und das Update kann als [großes Upgrade](major-upgrades.md)behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="c5290-114">Alternatively, the [**ProductCode**](productcode.md) of the product can be changed and the update can be treated as a [major upgrade](major-upgrades.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c5290-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c5290-115">Requirements</span></span>



| <span data-ttu-id="c5290-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c5290-116">Requirement</span></span> | <span data-ttu-id="c5290-117">Wert</span><span class="sxs-lookup"><span data-stu-id="c5290-117">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5290-118">Version</span><span class="sxs-lookup"><span data-stu-id="c5290-118">Version</span></span><br/> | <span data-ttu-id="c5290-119">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="c5290-119">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="c5290-120">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="c5290-120">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="c5290-121">Windows Installer 3,0 oder höher unter Windows Server 2003 oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="c5290-121">Windows Installer 3.0 or later on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="c5290-122">Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="c5290-122">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c5290-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c5290-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5290-124">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c5290-124">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="c5290-125">Wird in Windows Installer 2,0 und früher nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c5290-125">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




