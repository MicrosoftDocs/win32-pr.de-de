---
description: Weitere Informationen zum folgenden Diagramm finden Sie unter Entity Relationship Diagram-Legende.
ms.assetid: ec4f585d-cbd5-4c25-aaf4-1c1333fd4587
title: Kern Tabellen Gruppe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5a5cc87e80c60505025825353272699db574bd1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960644"
---
# <a name="core-tables-group"></a><span data-ttu-id="5f2dd-103">Kern Tabellen Gruppe</span><span class="sxs-lookup"><span data-stu-id="5f2dd-103">Core Tables Group</span></span>

<span data-ttu-id="5f2dd-104">Weitere Informationen zum folgenden Diagramm finden Sie unter [Entity Relationship Diagram-Legende](entity-relationship-diagram-legend.md).</span><span class="sxs-lookup"><span data-stu-id="5f2dd-104">For more information about the following diagram, see the [entity relationship diagram legend](entity-relationship-diagram-legend.md).</span></span>

![Kern Tabellen Gruppe](images/core.png)

<span data-ttu-id="5f2dd-106">Die Kerngruppe besteht aus Tabellen, in denen die grundlegenden Features und Komponenten der Anwendung und des Installationspakets beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="5f2dd-106">The core group consists of tables describing the fundamental features and components of the application and the installer package.</span></span> <span data-ttu-id="5f2dd-107">Entwickler von Installationspaketen sollten daher berücksichtigen, wie diese Tabellen zuerst aufgefüllt werden, da die Organisation eines Großteil der Datenbank aus dem Inhalt dieser Gruppe ersichtlich wird.</span><span class="sxs-lookup"><span data-stu-id="5f2dd-107">Developers of install packages should therefore consider how to populate these tables first because the organization of much of the database will become apparent from the content of this group.</span></span>

-   <span data-ttu-id="5f2dd-108">In der [Featuretabelle](feature-table.md) werden alle Funktionen aufgelistet, die zur Anwendung gehören.</span><span class="sxs-lookup"><span data-stu-id="5f2dd-108">The [Feature table](feature-table.md) lists all features belonging to the application.</span></span>
-   <span data-ttu-id="5f2dd-109">Die Bedingungs [Tabelle](condition-table.md) enthält die bedingten Ausdrücke, die bestimmen, ob ein bestimmtes Feature installiert wird.</span><span class="sxs-lookup"><span data-stu-id="5f2dd-109">The [Condition table](condition-table.md) contains the conditional expressions that determine whether or not a particular feature will be installed.</span></span>
-   <span data-ttu-id="5f2dd-110">In der [FeatureComponents-Tabelle](featurecomponents-table.md) wird beschrieben, welche Komponenten zu den einzelnen Features gehören.</span><span class="sxs-lookup"><span data-stu-id="5f2dd-110">The [FeatureComponents table](featurecomponents-table.md) describes which components belong to each feature.</span></span>
-   <span data-ttu-id="5f2dd-111">In der [Komponenten Tabelle](component-table.md) werden alle Komponenten aufgelistet, die zur Installation gehören.</span><span class="sxs-lookup"><span data-stu-id="5f2dd-111">The [Component table](component-table.md) lists all components belonging to the installation.</span></span>
-   <span data-ttu-id="5f2dd-112">In der [Verzeichnis Tabelle](directory-table.md) sind die Verzeichnisse aufgelistet, die während der Installation benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="5f2dd-112">The [Directory table](directory-table.md) lists the directories that are needed during the installation.</span></span> <span data-ttu-id="5f2dd-113">Da jede Komponente nur einem Verzeichnis zugeordnet werden muss, ist die Komponenten Tabelle eng mit dieser Tabelle verknüpft und weist einen externen Schlüssel für die Verzeichnis Tabelle auf.</span><span class="sxs-lookup"><span data-stu-id="5f2dd-113">Because each component must be associated with one and only one directory, the Component table is closely related to this table and has an external key to the Directory table.</span></span>
-   <span data-ttu-id="5f2dd-114">In der [Tabelle PublishComponent](publishcomponent-table.md) werden die Features und Komponenten aufgelistet, die für die Verwendung durch andere Anwendungen veröffentlicht werden.</span><span class="sxs-lookup"><span data-stu-id="5f2dd-114">The [PublishComponent table](publishcomponent-table.md) lists the features and components that are published for use by other applications.</span></span> <span data-ttu-id="5f2dd-115">[Komponenten und Funktionen](components-and-features.md) sind die zwei Arten von featureankündigungen.</span><span class="sxs-lookup"><span data-stu-id="5f2dd-115">[Components and Features](components-and-features.md) are the two types of feature advertisement.</span></span>
-   <span data-ttu-id="5f2dd-116">Die [MsiAssembly-Tabelle](msiassembly-table.md) gibt Windows Installer Einstellungen für .NET Framework Common Language Runtime Assemblys und Win32-Assemblys an.</span><span class="sxs-lookup"><span data-stu-id="5f2dd-116">The [MsiAssembly table](msiassembly-table.md) specifies Windows Installer settings for .NET Framework common language runtime assemblies and Win32 assemblies.</span></span>
-   <span data-ttu-id="5f2dd-117">Die [MsiAssemblyName-Tabelle](msiassemblyname-table.md) gibt das Schema für die Elemente eines starken Assemblycache-namens für eine Common Language Runtime-oder Win32-Assembly an.</span><span class="sxs-lookup"><span data-stu-id="5f2dd-117">The [MsiAssemblyName table](msiassemblyname-table.md) specifies the schema for the elements of a strong assembly cache name for a common language runtime or Win32 assembly.</span></span>
-   <span data-ttu-id="5f2dd-118">Die [complus-Tabelle](complus-table.md) enthält Informationen, die zum Installieren von com+-Anwendungen erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="5f2dd-118">The [Complus table](complus-table.md) contains information needed to install COM+ applications.</span></span>
-   <span data-ttu-id="5f2dd-119">Die [isolatedcomponent-Tabelle](isolatedcomponent-table.md) ordnet die in der Spalte Komponenten \_ Anwendung angegebene Komponente (i. a. exe) der Komponente zu, die in der freigegebenen Spalte der Komponente angegeben ist \_ (häufig eine freigegebene DLL).</span><span class="sxs-lookup"><span data-stu-id="5f2dd-119">The [IsolatedComponent table](isolatedcomponent-table.md) associates the component specified in the Component\_Application column (commonly an .exe) with the component specified in the Component\_Shared column (commonly a shared DLL).</span></span>
-   <span data-ttu-id="5f2dd-120">Die [upgradetabelle](upgrade-table.md) enthält Informationen, die bei [größeren Upgrades](major-upgrades.md)erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="5f2dd-120">The [Upgrade table](upgrade-table.md) contains information required during [major upgrades](major-upgrades.md).</span></span>

 

 



