---
description: Dies ist eine Computer spezifische System Richtlinie, mit der upgradekomponentenregeln bei kleinen Updates und geringfügigen Upgrades angewendet werden können.
ms.assetid: 0d39c059-d936-454c-aed8-efedd3da7473
title: Enforceupgradecomponentrules
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5a2fc093c2f0beb4167374f93447d978bbca8eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103959931"
---
# <a name="enforceupgradecomponentrules"></a><span data-ttu-id="c705f-103">Enforceupgradecomponentrules</span><span class="sxs-lookup"><span data-stu-id="c705f-103">EnforceUpgradeComponentRules</span></span>

<span data-ttu-id="c705f-104">Dies ist eine Computer spezifische [System Richtlinie](system-policy.md) , mit der upgradekomponentenregeln bei [kleinen Updates](small-updates.md) und [geringfügigen Upgrades](minor-upgrades.md)angewendet werden können.</span><span class="sxs-lookup"><span data-stu-id="c705f-104">This is a per-machine [system policy](system-policy.md) that can be used to apply upgrade component rules during [small updates](small-updates.md) and [minor upgrades](minor-upgrades.md).</span></span>

<span data-ttu-id="c705f-105">Legen Sie die enforceupgradecomponentrules-Richtlinie auf 1 fest, um upgradekomponentenregeln bei [kleinen Updates](small-updates.md) und [geringfügigen Upgrades](minor-upgrades.md) aller Produkte auf dem Computer anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="c705f-105">Set the EnforceUpgradeComponentRules policy to 1 to apply upgrade component rules during [small updates](small-updates.md) and [minor upgrades](minor-upgrades.md) of all products on the computer.</span></span> <span data-ttu-id="c705f-106">Legen Sie die Eigenschaft [**msienforceupgradecomponentrules**](msienforceupgradecomponentrules.md) in der Befehlszeile oder in der [Eigenschaften Tabelle](property-table.md)auf 1 fest, um die Regeln bei kleinen Updates und geringfügigen Upgrades eines bestimmten Produkts anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="c705f-106">To apply the rules during small updates and minor upgrades of a particular product, set the [**MSIENFORCEUPGRADECOMPONENTRULES**](msienforceupgradecomponentrules.md) property to 1 on the command line or in the [Property table](property-table.md).</span></span>

<span data-ttu-id="c705f-107">Wenn die Eigenschaft oder die Richtlinie auf 1 festgelegt wurde, können [kleine Updates](small-updates.md) und [kleinere Upgrades](minor-upgrades.md) fehlschlagen, da das Update versucht, Folgendes zu tun:</span><span class="sxs-lookup"><span data-stu-id="c705f-107">When the property or policy has been set to 1, [small updates](small-updates.md) and [minor upgrades](minor-upgrades.md) can fail because the update attempts to do the following:</span></span>

-   <span data-ttu-id="c705f-108">Fügen Sie am Anfang oder in der Mitte einer vorhandenen Funktionsstruktur ein neues Feature hinzu.</span><span class="sxs-lookup"><span data-stu-id="c705f-108">Add a new feature to the top or middle of an existing feature tree.</span></span>

    <span data-ttu-id="c705f-109">Die neue Funktion muss als neue Blatt Funktion zu einer vorhandenen Funktionsstruktur hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="c705f-109">The new feature must be added as a new leaf feature to an existing feature tree.</span></span>

    <span data-ttu-id="c705f-110">In diesem Fall kann der [**ProductCode**](productcode.md) des Produkts geändert werden, und die Updates können als [großes Upgrade](major-upgrades.md)behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="c705f-110">In this case, the [**ProductCode**](productcode.md) of the product can be changed and the updates can be treated as a [major upgrade](major-upgrades.md).</span></span>

-   <span data-ttu-id="c705f-111">Entfernen einer Komponente aus einer Funktion.</span><span class="sxs-lookup"><span data-stu-id="c705f-111">Remove a component from a feature.</span></span>

    <span data-ttu-id="c705f-112">Dies kann auch vorkommen, wenn Sie die GUID einer Komponente ändern.</span><span class="sxs-lookup"><span data-stu-id="c705f-112">This can also occur if you change the GUID of a component.</span></span> <span data-ttu-id="c705f-113">Die von der ursprünglichen GUID identifizierte Komponente scheint entfernt zu werden, und die von der neuen GUID identifizierte Komponente wird als neue Komponente angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c705f-113">The component identified by the original GUID appears to be removed and the component as identified by the new GUID appears as a new component.</span></span>

    <span data-ttu-id="c705f-114">**Windows Installer 4,5 und höher:** Die Komponente kann mithilfe von Windows Installer 4,5 oder höher ordnungsgemäß entfernt werden, indem das **msidbcomponentattributesuninstallonabgelöst** -Attribut in der [Component-Tabelle](component-table.md) festgelegt oder die [**msiuninstallablösung dedcomponents**](msiuninstallsupersededcomponents.md) -Eigenschaft festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="c705f-114">**Windows Installer 4.5 and later:** The component can be removed correctly using Windows Installer 4.5 or later by setting the **msidbComponentAttributesUninstallOnSupersedence** attribute in the [Component table](component-table.md) or by setting the [**MSIUNINSTALLSUPERSEDEDCOMPONENTS**](msiuninstallsupersededcomponents.md) property.</span></span>

    <span data-ttu-id="c705f-115">Alternativ kann der [**ProductCode**](productcode.md) des Produkts geändert werden, und die Updates können als [großes Upgrade](major-upgrades.md)behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="c705f-115">Alternatively, the [**ProductCode**](productcode.md) of the product can be changed and the updates can be treated as a [major upgrade](major-upgrades.md).</span></span>

## <a name="registry-key"></a><span data-ttu-id="c705f-116">Registrierungsschlüssel</span><span class="sxs-lookup"><span data-stu-id="c705f-116">Registry Key</span></span>

<span data-ttu-id="c705f-117">**HKEY \_ Software Richtlinien für lokale \_ Computer** \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="c705f-117">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="c705f-118">Datentyp</span><span class="sxs-lookup"><span data-stu-id="c705f-118">Data Type</span></span>

<span data-ttu-id="c705f-119">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="c705f-119">**REG\_DWORD**</span></span>

## <a name="related-topics"></a><span data-ttu-id="c705f-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c705f-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c705f-121">Wird in Windows Installer 2,0 und früher nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c705f-121">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 



