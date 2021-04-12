---
description: Sie können steuern, welche featureinstallationsoptionen für Benutzer und Anwendungen verfügbar sind, indem Sie die Featuretabelle und die Komponenten Tabelle erstellen.
ms.assetid: 3ce441e0-e709-415c-af64-b1ded7b04f6b
title: Steuern von Funktionsauswahl Zuständen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fadedf4b6038f8257d06671e0774afc258391898
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218204"
---
# <a name="controlling-feature-selection-states"></a><span data-ttu-id="56372-103">Steuern von Funktionsauswahl Zuständen</span><span class="sxs-lookup"><span data-stu-id="56372-103">Controlling Feature Selection States</span></span>

<span data-ttu-id="56372-104">Sie können steuern, welche featureinstallationsoptionen für Benutzer und Anwendungen verfügbar sind, indem Sie die [Featuretabelle](feature-table.md) und die [Komponenten Tabelle](component-table.md)erstellen.</span><span class="sxs-lookup"><span data-stu-id="56372-104">You can control which feature installation options are available for users and applications to select by authoring the [Feature table](feature-table.md) and [Component table](component-table.md).</span></span>

-   <span data-ttu-id="56372-105">Um die Auswahl des Ankündigungs Status für eine Funktion zu verhindern, schließen Sie " **msidbfeatureattributesdisallowankündigungs** " in das Feld "Attribute" der Funktion in der [Featuretabelle](feature-table.md)ein.</span><span class="sxs-lookup"><span data-stu-id="56372-105">To prevent selection of the advertise state for a feature, include **msidbFeatureAttributesDisallowAdvertise** in the feature's Attributes field in the [Feature table](feature-table.md).</span></span>
-   <span data-ttu-id="56372-106">Um zu verhindern, dass die Zustände "Run-From-Source" oder "run-from-Network" für eine Funktion ausgewählt werden, schließen Sie " **msidbcomponentattributeslocalonly** " in die Attribute-Felder in der [Komponenten Tabelle](component-table.md) für jede Komponente ein, die zur Funktion gehört.</span><span class="sxs-lookup"><span data-stu-id="56372-106">To prevent selection of the run-from-source or run-from-network states for a feature, include **msidbComponentAttributesLocalOnly** in the Attributes fields in the [Component table](component-table.md) for every component belonging to the feature.</span></span> <span data-ttu-id="56372-107">Wenn für eine Funktion keine Komponenten vorhanden sind, sind in der Funktion immer die Optionen "ausführen" und "ausführen-aus" für den Computer verfügbar.</span><span class="sxs-lookup"><span data-stu-id="56372-107">If a feature has no components, the feature always has the run-from-source and run-from-my-computer options available.</span></span>
-   <span data-ttu-id="56372-108">Um die Auswahl des Status "Run-From-My-Computer" für eine Funktion zu verhindern, schließen Sie " **msidbcomponentattributessourceonly** " in die Attribute-Felder in der [Komponenten Tabelle](component-table.md) für jede Komponente ein, die zur Funktion gehört.</span><span class="sxs-lookup"><span data-stu-id="56372-108">To prevent selection of the run-from-my-computer state for a feature, include **msidbComponentAttributesSourceOnly** in the Attributes fields in the [Component table](component-table.md) for every component belonging to the feature.</span></span> <span data-ttu-id="56372-109">Wenn für eine Funktion keine Komponenten vorhanden sind, sind in der Funktion immer die Optionen "ausführen" und "ausführen-aus" für den Computer verfügbar.</span><span class="sxs-lookup"><span data-stu-id="56372-109">If a feature has no components, the feature always has the run-from-source and run-from-my-computer options available.</span></span>
-   <span data-ttu-id="56372-110">Neue untergeordnete Funktionen können erstellt werden, indem " **msidbfeatureattributesfollowparent** " und " **msidbfeatureattributesuidisallowmissing** " in das Feld "Attribute" der [Funktions Tabelle](feature-table.md)eingeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="56372-110">New child features can be authored by including **msidbFeatureAttributesFollowParent** and **msidbFeatureAttributesUIDisallowAbsent** in the Attributes field of the [Feature table](feature-table.md).</span></span>

 

 



