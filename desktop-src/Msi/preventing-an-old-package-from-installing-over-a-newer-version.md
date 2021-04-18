---
description: Windows Installer Upgradepakete können erstellt werden, damit größere Upgrades nicht installiert werden, wenn ein Benutzer bereits eine neuere Version installiert hat.
ms.assetid: f46e82bd-70b3-46a2-8246-a1eadfdc589d
title: Verhindern, dass ein altes Paket über eine neuere Version installiert wird
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 320ab062c4ffbc740d85c59ece3d3baaa63f4209
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106357513"
---
# <a name="preventing-an-old-package-from-installing-over-a-newer-version"></a><span data-ttu-id="e5512-103">Verhindern, dass ein altes Paket über eine neuere Version installiert wird</span><span class="sxs-lookup"><span data-stu-id="e5512-103">Preventing an Old Package from Installing Over a Newer Version</span></span>

<span data-ttu-id="e5512-104">Windows Installer Upgradepakete können erstellt werden, damit größere Upgrades nicht installiert werden, wenn ein Benutzer bereits eine neuere Version installiert hat.</span><span class="sxs-lookup"><span data-stu-id="e5512-104">Windows Installer upgrade packages can be authored to have major upgrades not install if a user already has a newer version installed.</span></span> <span data-ttu-id="e5512-105">Mit dem in diesem Thema beschriebenen Verfahren können nur Herabstufungen verhindert werden, die möglicherweise durch Ausführen eines größeren upgradepakets verursacht werden.</span><span class="sxs-lookup"><span data-stu-id="e5512-105">The procedure in this topic can only prevent downgrades that might be caused by running a major upgrade package.</span></span> <span data-ttu-id="e5512-106">Dieses Verfahren basiert auf der [Aktion "FindRelatedProducts](findrelatedproducts-action.md)", die nur während einer erstmaligen Installation ausgeführt wird und nicht im Wartungsmodus (Neuinstallation) ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e5512-106">This procedure relies on the [FindRelatedProducts Action](findrelatedproducts-action.md), which only runs during a first-time installation and does not run in maintenance mode (reinstallation).</span></span> <span data-ttu-id="e5512-107">Da kleinere Upgrades mithilfe der erneuten Installation durchgeführt werden, kann mit diesem Verfahren nicht bestimmt werden, ob ein geringfügiges Upgradepaket versucht, ein Downgrade für eine Anwendung durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="e5512-107">Because minor upgrades are performed using reinstallation, this procedure cannot be used to determine whether a minor upgrade package is attempting to downgrade an application.</span></span> <span data-ttu-id="e5512-108">Weitere Informationen finden Sie unter [Vorbereiten einer Anwendung für zukünftige größere Upgrades](preparing-an-application-for-future-major-upgrades.md).</span><span class="sxs-lookup"><span data-stu-id="e5512-108">For more information, see [Preparing an Application for Future Major Upgrades](preparing-an-application-for-future-major-upgrades.md).</span></span>

<span data-ttu-id="e5512-109">**So verhindern Sie, dass ein altes Paket über eine neuere Version installiert wird**</span><span class="sxs-lookup"><span data-stu-id="e5512-109">**To prevent an old package from installing over a newer version**</span></span>

1.  <span data-ttu-id="e5512-110">Geben Sie die [**UpgradeCode**](upgradecode.md) -Eigenschaft für die Gruppe verwandter Produkte ein, die möglicherweise berechtigt sind, dieses Upgrade in der UpgradeCode-Spalte der [upgradetabelle](upgrade-table.md)zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="e5512-110">Enter the [**UpgradeCode**](upgradecode.md) Property for the group of related products that may be eligible to receive this upgrade into the UpgradeCode column of the [Upgrade Table](upgrade-table.md).</span></span>
2.  <span data-ttu-id="e5512-111">Geben Sie das Bitflag **msidbupgradeattributesonlydetect** in der Spalte Attribute der [upgradetabelle](upgrade-table.md)ein.</span><span class="sxs-lookup"><span data-stu-id="e5512-111">Enter the **msidbUpgradeAttributesOnlyDetect** bit flag in the Attributes column of the [Upgrade Table](upgrade-table.md).</span></span>
3.  <span data-ttu-id="e5512-112">Geben Sie die Version des Upgrades, das von diesem Paket bereitgestellt wird, in die Spalte versionmin der [upgradetabelle](upgrade-table.md)ein.</span><span class="sxs-lookup"><span data-stu-id="e5512-112">Enter the version of the upgrade provided by this package into the VersionMin column of the [Upgrade Table](upgrade-table.md).</span></span> <span data-ttu-id="e5512-113">Lassen Sie die Spalte versionmax leer.</span><span class="sxs-lookup"><span data-stu-id="e5512-113">Leave the VersionMax column blank.</span></span>
4.  <span data-ttu-id="e5512-114">Geben Sie den Namen der Eigenschaft ein, die von der [FindRelatedProducts-Aktion](findrelatedproducts-action.md) in der Action Property-Spalte der [upgradetabelle](upgrade-table.md)festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="e5512-114">Enter the name of the property that is to be set by the [FindRelatedProducts Action](findrelatedproducts-action.md) into the ActionProperty column of the [Upgrade Table](upgrade-table.md).</span></span>
5.  <span data-ttu-id="e5512-115">Fügen Sie der Eigenschaften [Tabelle](property-table.md)die [**securecustomproperties**](securecustomproperties.md) -Eigenschaft und die-Eigenschaft in der Spalte "Aktions Eigenschaft" der [upgradetabelle](upgrade-table.md) hinzu.</span><span class="sxs-lookup"><span data-stu-id="e5512-115">Add the [**SecureCustomProperties**](securecustomproperties.md) property and the property named in the ActionProperty column of the [Upgrade Table](upgrade-table.md) to the [Property Table](property-table.md).</span></span>
6.  <span data-ttu-id="e5512-116">Fügen Sie nach der Aktion FindRelatedProducts in der [Tabelle InstallExecuteSequence](installexecutesequence-table.md)einen [benutzerdefinierten Aktionstyp 19](custom-action-type-19.md) hinzu.</span><span class="sxs-lookup"><span data-stu-id="e5512-116">Add a [Custom Action Type 19](custom-action-type-19.md) after the FindRelatedProducts action in the [InstallExecuteSequence Table](installexecutesequence-table.md).</span></span> <span data-ttu-id="e5512-117">Fügen Sie für diese Aktion einen Datensatz in die [Tabelle "CustomAction](customaction-table.md) " ein, und geben Sie den Text ein, der in der Ziel Spalte angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="e5512-117">Include a record in the [CustomAction Table](customaction-table.md) for this action and enter the text to be displayed in the Target column.</span></span> <span data-ttu-id="e5512-118">Die benutzerdefinierte Aktion vom Typ 19 ist in das Installationsprogramm integriert, sodass kein Code geschrieben werden kann.</span><span class="sxs-lookup"><span data-stu-id="e5512-118">The type 19 custom action is built into the installer, so there is no code to write.</span></span>
7.  <span data-ttu-id="e5512-119">Geben Sie den Namen der Action Property in die Spalte Bedingung des Datensatzes in der [InstallExecuteSequence-Tabelle](installexecutesequence-table.md) ein, die den [benutzerdefinierten Aktionstyp 19](custom-action-type-19.md)enthält.</span><span class="sxs-lookup"><span data-stu-id="e5512-119">Enter the name of the ActionProperty into the Condition column of the record in [InstallExecuteSequence Table](installexecutesequence-table.md) that contains the [Custom Action Type 19](custom-action-type-19.md).</span></span> <span data-ttu-id="e5512-120">Dadurch wird die benutzerdefinierte Aktion nur ausgeführt, wenn die [upgradetabelle](upgrade-table.md) erkennt, dass eine neuere Version bereits installiert ist.</span><span class="sxs-lookup"><span data-stu-id="e5512-120">This conditions the custom action to only be executed when the [Upgrade Table](upgrade-table.md) detects that a newer version is already installed.</span></span>

    <span data-ttu-id="e5512-121">Beispielsweise kann ein Windows Installer Paket, das eine Gruppe verwandter Produkte auf Version 3,0 aktualisiert, in den Tabellen [Upgrade](upgrade-table.md), [CustomAction](customaction-table.md), [InstallExecuteSequence](installexecutesequence-table.md)und [Property](property-table.md) die folgenden Datensätze enthalten.</span><span class="sxs-lookup"><span data-stu-id="e5512-121">For example, a Windows Installer package that upgrades a group of related products to version 3.0 may include the following records in its [Upgrade](upgrade-table.md), [CustomAction](customaction-table.md), [InstallExecuteSequence](installexecutesequence-table.md), and [Property](property-table.md) tables.</span></span> <span data-ttu-id="e5512-122">Alle zugehörigen Produkte in der Gruppe verfügen über denselben UpgradeCode, aber das Installationsprogramm installiert dieses Upgradepaket nicht, wenn eine Version, die höher als 3,0 ist, bereits auf dem Computer installiert ist.</span><span class="sxs-lookup"><span data-stu-id="e5512-122">All the related products in the group have the same UpgradeCode, but the installer does not install this upgrade package if a version later than 3.0 is already installed on the computer.</span></span> <span data-ttu-id="e5512-123">In diesem Fall zeigt das Installationsprogramm eine Fehlermeldung an, und die Installation schlägt fehl.</span><span class="sxs-lookup"><span data-stu-id="e5512-123">In this case, the Installer presents an error message and the installation fails.</span></span> <span data-ttu-id="e5512-124">Das Upgradepaket der Version 3,0 wird über die Versionen 1,0 und 2,0 installiert.</span><span class="sxs-lookup"><span data-stu-id="e5512-124">The version 3.0 upgrade package installs over versions 1.0 and 2.0.</span></span>

    [<span data-ttu-id="e5512-125">Upgradetabelle</span><span class="sxs-lookup"><span data-stu-id="e5512-125">Upgrade Table</span></span>](upgrade-table.md)

    

    | <span data-ttu-id="e5512-126">UpgradeCode auch</span><span class="sxs-lookup"><span data-stu-id="e5512-126">UpgradeCode</span></span>                            | <span data-ttu-id="e5512-127">Versionmin</span><span class="sxs-lookup"><span data-stu-id="e5512-127">VersionMin</span></span> | <span data-ttu-id="e5512-128">Versionmax</span><span class="sxs-lookup"><span data-stu-id="e5512-128">VersionMax</span></span> | <span data-ttu-id="e5512-129">Sprache</span><span class="sxs-lookup"><span data-stu-id="e5512-129">Language</span></span> | <span data-ttu-id="e5512-130">Attribute</span><span class="sxs-lookup"><span data-stu-id="e5512-130">Attributes</span></span>                                | <span data-ttu-id="e5512-131">Entfernen</span><span class="sxs-lookup"><span data-stu-id="e5512-131">Remove</span></span> | <span data-ttu-id="e5512-132">Aktions Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="e5512-132">ActionProperty</span></span>  |
    |----------------------------------------|------------|------------|----------|-------------------------------------------|--------|-----------------|
    | <span data-ttu-id="e5512-133">{E7BE6D45-49ff-4701-A17E-BDCC98CE180D}</span><span class="sxs-lookup"><span data-stu-id="e5512-133">{E7BE6D45-49FF-4701-A17E-BDCC98CE180D}</span></span> | <span data-ttu-id="e5512-134">3.0</span><span class="sxs-lookup"><span data-stu-id="e5512-134">3.0</span></span>        |            |          | <span data-ttu-id="e5512-135">msidbupgraabattributesonlydetect</span><span class="sxs-lookup"><span data-stu-id="e5512-135">msidbUpgradeAttributesOnlyDetect</span></span>          |        | <span data-ttu-id="e5512-136">Newproductfound</span><span class="sxs-lookup"><span data-stu-id="e5512-136">NEWPRODUCTFOUND</span></span> |
    | <span data-ttu-id="e5512-137">{E7BE6D45-49ff-4701-A17E-BDCC98CE180D}</span><span class="sxs-lookup"><span data-stu-id="e5512-137">{E7BE6D45-49FF-4701-A17E-BDCC98CE180D}</span></span> | <span data-ttu-id="e5512-138">1.0</span><span class="sxs-lookup"><span data-stu-id="e5512-138">1.0</span></span>        | <span data-ttu-id="e5512-139">3.0</span><span class="sxs-lookup"><span data-stu-id="e5512-139">3.0</span></span>        |          | <span data-ttu-id="e5512-140">msidbupgraabattributesversionmininclusive</span><span class="sxs-lookup"><span data-stu-id="e5512-140">msidbUpgradeAttributesVersionMinInclusive</span></span> |        | <span data-ttu-id="e5512-141">Upgrade gefunden</span><span class="sxs-lookup"><span data-stu-id="e5512-141">UPGRADEFOUND</span></span>    |

    

     

    [<span data-ttu-id="e5512-142">Tabelle "CustomAction"</span><span class="sxs-lookup"><span data-stu-id="e5512-142">CustomAction Table</span></span>](customaction-table.md)

    

    | <span data-ttu-id="e5512-143">Aktion</span><span class="sxs-lookup"><span data-stu-id="e5512-143">Action</span></span> | <span data-ttu-id="e5512-144">type</span><span class="sxs-lookup"><span data-stu-id="e5512-144">Type</span></span> | <span data-ttu-id="e5512-145">`Source`</span><span class="sxs-lookup"><span data-stu-id="e5512-145">Source</span></span> | <span data-ttu-id="e5512-146">Ziel</span><span class="sxs-lookup"><span data-stu-id="e5512-146">Target</span></span>                                 |
    |--------|------|--------|----------------------------------------|
    | <span data-ttu-id="e5512-147">KA1</span><span class="sxs-lookup"><span data-stu-id="e5512-147">CA1</span></span>    | <span data-ttu-id="e5512-148">19</span><span class="sxs-lookup"><span data-stu-id="e5512-148">19</span></span>   |        | <span data-ttu-id="e5512-149">Ein höheres Upgrade ist bereits installiert.</span><span class="sxs-lookup"><span data-stu-id="e5512-149">A higher upgrade is already installed.</span></span> |

    

     

    [<span data-ttu-id="e5512-150">InstallExecuteSequence-Tabelle</span><span class="sxs-lookup"><span data-stu-id="e5512-150">InstallExecuteSequence Table</span></span>](installexecutesequence-table.md)

    

    | <span data-ttu-id="e5512-151">Aktion</span><span class="sxs-lookup"><span data-stu-id="e5512-151">Action</span></span>              | <span data-ttu-id="e5512-152">Bedingung</span><span class="sxs-lookup"><span data-stu-id="e5512-152">Condition</span></span>       | <span data-ttu-id="e5512-153">Sequenz</span><span class="sxs-lookup"><span data-stu-id="e5512-153">Sequence</span></span> |
    |---------------------|-----------------|----------|
    | <span data-ttu-id="e5512-154">FindRelatedProducts</span><span class="sxs-lookup"><span data-stu-id="e5512-154">FindRelatedProducts</span></span> |                 | <span data-ttu-id="e5512-155">200</span><span class="sxs-lookup"><span data-stu-id="e5512-155">200</span></span>      |
    | <span data-ttu-id="e5512-156">KA1</span><span class="sxs-lookup"><span data-stu-id="e5512-156">CA1</span></span>                 | <span data-ttu-id="e5512-157">Newproductfound</span><span class="sxs-lookup"><span data-stu-id="e5512-157">NEWPRODUCTFOUND</span></span> | <span data-ttu-id="e5512-158">201</span><span class="sxs-lookup"><span data-stu-id="e5512-158">201</span></span>      |

    

     

    [<span data-ttu-id="e5512-159">Eigenschaften Tabelle</span><span class="sxs-lookup"><span data-stu-id="e5512-159">Property Table</span></span>](property-table.md)

    

    | <span data-ttu-id="e5512-160">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="e5512-160">Property</span></span>                                                 | <span data-ttu-id="e5512-161">Wert</span><span class="sxs-lookup"><span data-stu-id="e5512-161">Value</span></span>                        |
    |----------------------------------------------------------|------------------------------|
    | [<span data-ttu-id="e5512-162">**Securecustomproperties**</span><span class="sxs-lookup"><span data-stu-id="e5512-162">**SecureCustomProperties**</span></span>](securecustomproperties.md) | <span data-ttu-id="e5512-163">Newproductfound; Upgrade gefunden</span><span class="sxs-lookup"><span data-stu-id="e5512-163">NEWPRODUCTFOUND;UPGRADEFOUND</span></span> |

    

     

 

 



