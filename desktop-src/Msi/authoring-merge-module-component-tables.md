---
description: Eine Komponenten Tabelle ist in jedem Mergemodul erforderlich.
ms.assetid: ef4a0678-bf6b-47c9-89e8-40e12da52d9b
title: Erstellen von Komponenten Tabellen für Mergemodule
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46557541b3a6b89841fe3e26cef7c00e59dc3911
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104042155"
---
# <a name="authoring-merge-module-component-tables"></a><span data-ttu-id="169ee-103">Erstellen von Komponenten Tabellen für Mergemodule</span><span class="sxs-lookup"><span data-stu-id="169ee-103">Authoring Merge Module Component Tables</span></span>

<span data-ttu-id="169ee-104">Eine [Komponenten Tabelle](component-table.md) ist in jedem Mergemodul erforderlich.</span><span class="sxs-lookup"><span data-stu-id="169ee-104">A [Component table](component-table.md) is required in every merge module.</span></span> <span data-ttu-id="169ee-105">Diese Tabelle enthält einen Datensatz für jede Komponente, die vom Mergemodul an die MSI-Datei des Ziels geliefert wird.</span><span class="sxs-lookup"><span data-stu-id="169ee-105">This table contains a record for each component delivered by the merge module to the target .msi file.</span></span> <span data-ttu-id="169ee-106">Beachten Sie, dass jede dieser Komponenten auch in der [modulecomponents-Tabelle](modulecomponents-table.md) angegeben werden muss, die unter [Erstellen von modulecomponents-Tabellen](authoring-modulecomponents-tables.md)beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="169ee-106">Note that each of these components must also be specified in the [ModuleComponents table](modulecomponents-table.md) described in [Authoring ModuleComponents Tables](authoring-modulecomponents-tables.md).</span></span>

<span data-ttu-id="169ee-107">Verwenden Sie die standardmäßige Benennungs Konvention, wenn Sie Namen in die Komponenten Spalte eingeben, um sicherzustellen, dass der Bezeichner für jede Komponente für alle Mergemodule und Installations Datenbanken eindeutig ist.</span><span class="sxs-lookup"><span data-stu-id="169ee-107">Use the standard naming convention when entering names into the Component column to ensure that the identifier for each component is unique for all merge modules and installation databases.</span></span> <span data-ttu-id="169ee-108">Weitere Informationen finden Sie unter [Benennen von primär Schlüsseln in mergemoduldatenbanken](naming-primary-keys-in-merge-module-databases.md).</span><span class="sxs-lookup"><span data-stu-id="169ee-108">For more information, see [Naming Primary Keys in Merge Module Databases](naming-primary-keys-in-merge-module-databases.md).</span></span>

<span data-ttu-id="169ee-109">Füllen Sie die restlichen Felder in jedem Datensatz aus, wie für eine Installations Datenbank in der [Component-Tabelle](component-table.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="169ee-109">Complete the remaining fields in each record as described for an installation database in [Component table](component-table.md).</span></span> <span data-ttu-id="169ee-110">Die Komponenten, die von einem Mergemodul einem Paket hinzugefügt werden, müssen den Richtlinien für gültige Windows Installer Komponenten entsprechen, die in den folgenden Abschnitten beschrieben werden:</span><span class="sxs-lookup"><span data-stu-id="169ee-110">The components added to a package by a merge module must adhere to the guidelines for valid Windows Installer Components described in the following sections:</span></span>

-   [<span data-ttu-id="169ee-111">Windows Installer Komponenten</span><span class="sxs-lookup"><span data-stu-id="169ee-111">Windows Installer Components</span></span>](windows-installer-components.md)
-   [<span data-ttu-id="169ee-112">Organisieren von Anwendungen in Komponenten</span><span class="sxs-lookup"><span data-stu-id="169ee-112">Organizing Applications into Components</span></span>](organizing-applications-into-components.md)

 

 



