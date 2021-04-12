---
description: Die Datenbank eines Mergemoduls enthält alle Installations Eigenschaften und die Setup Logik für das Modul.
ms.assetid: 72e42392-54e6-4be8-9a43-04158552be3d
title: Modul Datenbank zusammenführen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74158e38d10b302c28520f6c1736e9cc6d823641
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347158"
---
# <a name="merge-module-database"></a><span data-ttu-id="d195c-103">Modul Datenbank zusammenführen</span><span class="sxs-lookup"><span data-stu-id="d195c-103">Merge Module Database</span></span>

<span data-ttu-id="d195c-104">Die Datenbank eines Mergemoduls enthält alle Installations Eigenschaften und die Setup Logik für das Modul.</span><span class="sxs-lookup"><span data-stu-id="d195c-104">The database of a merge module contains all the installation properties and setup logic for the module.</span></span> <span data-ttu-id="d195c-105">Es handelt sich im Wesentlichen um eine vereinfachte [Installer-Datenbank](installer-database.md) oder MSI-Datei.</span><span class="sxs-lookup"><span data-stu-id="d195c-105">It is essentially a simplified [installer database](installer-database.md) or .msi file.</span></span> <span data-ttu-id="d195c-106">Standard mäßige Mergemodul-Datenbankdateien werden durch eine MSM-Erweiterung angegeben.</span><span class="sxs-lookup"><span data-stu-id="d195c-106">Standard merge module database files are indicated by an .msm extension.</span></span> <span data-ttu-id="d195c-107">Eine Liste aller Datenbanktabellen, die in Mergemodulen vorhanden sein können, finden Sie unter [Merge Module Database Tables](merge-module-database-tables.md).</span><span class="sxs-lookup"><span data-stu-id="d195c-107">For a list of all database tables that can exist in merge modules, see [Merge Module Database Tables](merge-module-database-tables.md).</span></span> <span data-ttu-id="d195c-108">Die folgenden Tabellen sind in der-Datenbank jeder MSM-Datei erforderlich:</span><span class="sxs-lookup"><span data-stu-id="d195c-108">The following tables are required in the database of every .msm file:</span></span>

[<span data-ttu-id="d195c-109">Komponente</span><span class="sxs-lookup"><span data-stu-id="d195c-109">Component</span></span>](component-table.md)

[<span data-ttu-id="d195c-110">Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="d195c-110">Directory</span></span>](directory-table.md)

[<span data-ttu-id="d195c-111">FeatureComponents</span><span class="sxs-lookup"><span data-stu-id="d195c-111">FeatureComponents</span></span>](featurecomponents-table.md)

[<span data-ttu-id="d195c-112">File</span><span class="sxs-lookup"><span data-stu-id="d195c-112">File</span></span>](file-table.md)

[<span data-ttu-id="d195c-113">ModuleSignature</span><span class="sxs-lookup"><span data-stu-id="d195c-113">ModuleSignature</span></span>](modulesignature-table.md)

[<span data-ttu-id="d195c-114">Modulecomponents</span><span class="sxs-lookup"><span data-stu-id="d195c-114">ModuleComponents</span></span>](modulecomponents-table.md)

<span data-ttu-id="d195c-115">Beachten Sie, dass die Komponenten "Component", "Directory", "FeatureComponents" und "file" auch in allen MSI-Dateien vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="d195c-115">Note that the Component, Directory, FeatureComponents, and File tables are also present in all .msi files.</span></span> <span data-ttu-id="d195c-116">Eine mergemoduldatenbank enthält keine [Featuretabelle](feature-table.md) , sodass die MSM-Datei nicht allein installiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="d195c-116">A merge module database does not contain a [Feature table](feature-table.md) and so the .msm file cannot be installed alone.</span></span> <span data-ttu-id="d195c-117">Zum Installieren eines Mergemoduls muss es zuerst mithilfe eines Merge-Tools in einer MSI-Datei zusammengeführt werden.</span><span class="sxs-lookup"><span data-stu-id="d195c-117">To install a merge module, it must first be merged by using a merge tool into an .msi file.</span></span>

<span data-ttu-id="d195c-118">Die [ModuleSignature-Tabelle](modulesignature-table.md) ist nur in MSI-Dateien vorhanden, die mit mindestens einer MSM-Datei zusammengeführt wurden.</span><span class="sxs-lookup"><span data-stu-id="d195c-118">The [ModuleSignature Table](modulesignature-table.md) is only present in .msi files that has been merged with at least one .msm file.</span></span> <span data-ttu-id="d195c-119">Wenn diese Tabelle in einer MSI-Datei vorhanden ist, enthält Sie einen Datensatz für jedes Mergemodul, das zuvor in der Installations Datenbank zusammengeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="d195c-119">If this table is present in an .msi file, it contains one record for each merge module that has been previously merged into the installation database.</span></span>

<span data-ttu-id="d195c-120">Mergemodule können optionale Mergemodule-Sequenz Tabellen enthalten.</span><span class="sxs-lookup"><span data-stu-id="d195c-120">Merge modules may contain optional MergeModule Sequence tables.</span></span> <span data-ttu-id="d195c-121">Diese Tabellen treten nur in MSM-Dateien auf.</span><span class="sxs-lookup"><span data-stu-id="d195c-121">These tables occur only in .msm files.</span></span> <span data-ttu-id="d195c-122">Wenn die MSM-Dateien in einer MSI-Datei zusammengeführt werden, ändern diese Tabellen die Aktions [*Sequenz Tabellen*](s-gly.md) der MSI-Datei.</span><span class="sxs-lookup"><span data-stu-id="d195c-122">When the .msm files are merged into an .msi file, these tables modify the action [*sequence tables*](s-gly.md) of the .msi file.</span></span>

<span data-ttu-id="d195c-123">Mergemodule können benutzerdefinierte Tabellen enthalten.</span><span class="sxs-lookup"><span data-stu-id="d195c-123">Merge modules may contain custom tables.</span></span> <span data-ttu-id="d195c-124">Diese Tabellen werden von [benutzerdefinierten Aktionen](custom-actions.md) verwendet, die im Mergemodul definiert sind.</span><span class="sxs-lookup"><span data-stu-id="d195c-124">These tables are used by [custom actions](custom-actions.md) defined in the merge module.</span></span>

<span data-ttu-id="d195c-125">Mergemodule erfordern selten Benutzeroberflächen Tabellen.</span><span class="sxs-lookup"><span data-stu-id="d195c-125">Merge modules rarely require user interface tables.</span></span> <span data-ttu-id="d195c-126">Diese Tabellen müssen nur in seltenen Fällen vorhanden sein, in denen das Mergemodul während der Installation Eingaben vom Benutzer erfordert.</span><span class="sxs-lookup"><span data-stu-id="d195c-126">These tables need to be present only in rare cases where the merge module requires input from the user during installation.</span></span> <span data-ttu-id="d195c-127">Weitere Informationen finden Sie unter [Erstellen von Benutzeroberflächen in Mergemodulen](authoring-user-interfaces-in-merge-modules.md).</span><span class="sxs-lookup"><span data-stu-id="d195c-127">For more information, see [Authoring User Interfaces in Merge Modules](authoring-user-interfaces-in-merge-modules.md).</span></span>

 

 



