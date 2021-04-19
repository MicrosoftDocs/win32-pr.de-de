---
description: Der Wert der compaddsource-Eigenschaft ist eine Liste von Komponenten-GUIDs aus der Spalte "ComponentId" der Komponenten Tabelle, die durch Kommas getrennt sind, die zur Installation vom Quell Medium installiert werden sollen.
ms.assetid: ee1e0650-674d-4189-8ef7-3d2ece89cc28
title: Compaddsource (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f59526196a75599dbd2a535db6dcda4fb733936
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356419"
---
# <a name="compaddsource-property"></a><span data-ttu-id="dcd8a-103">Compaddsource (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="dcd8a-103">COMPADDSOURCE property</span></span>

<span data-ttu-id="dcd8a-104">Der Wert der **compaddsource** -Eigenschaft ist eine Liste von Komponenten-GUIDs aus der Spalte "ComponentId" der [Komponenten](component-table.md) Tabelle, die durch Kommas getrennt sind, die zur Installation vom Quell Medium installiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="dcd8a-104">The value of the **COMPADDSOURCE** property is a list of component GUIDs from the ComponentId column of the [Component](component-table.md) table, delimited by commas, that are to be installed to run from the source media.</span></span> <span data-ttu-id="dcd8a-105">Das Installationsprogramm verwendet diesen Wert, um zu bestimmen, welche Funktionen auf der Grundlage der angegebenen Komponenten zum Ausführen aus der Quelle installiert werden.</span><span class="sxs-lookup"><span data-stu-id="dcd8a-105">The installer uses this value to determine which features are set to be installed to run from source, based on the specified components.</span></span> <span data-ttu-id="dcd8a-106">Für jede aufgelistete Komponenten-ID überprüft das Installationsprogramm alle Features, die (über die Tabelle " [FeatureComponents](featurecomponents-table.md) ") mit dieser Komponente verknüpft sind, und installiert die Funktion, die den geringsten Speicherplatz für die Installation erfordert.</span><span class="sxs-lookup"><span data-stu-id="dcd8a-106">For each listed component ID, the installer examines all features linked (through the [FeatureComponents](featurecomponents-table.md) table) to that component, and installs the feature that requires the least amount of disk space to install.</span></span> <span data-ttu-id="dcd8a-107">Die aufgeführten Komponenten müssen in der Component-Spalte der [Component](component-table.md) -Tabelle vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="dcd8a-107">The components listed must be present in the Component column of the [Component](component-table.md) table.</span></span>

## <a name="remarks"></a><span data-ttu-id="dcd8a-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dcd8a-108">Remarks</span></span>

<span data-ttu-id="dcd8a-109">Beachten Sie, dass bei den Komponentennamen die Groß-/Kleinschreibung beachtet</span><span class="sxs-lookup"><span data-stu-id="dcd8a-109">Note that the component names are case-sensitive.</span></span> <span data-ttu-id="dcd8a-110">Beachten Sie auch Folgendes: Wenn das LocalOnly-Bitflag in der Attribute-Spalte der [Komponenten](component-table.md) Tabelle für eine Komponente festgelegt ist, wird die Komponente zur lokalen Installation installiert.</span><span class="sxs-lookup"><span data-stu-id="dcd8a-110">Also note that if the LocalOnly bit flag is set in the Attributes column of the [Component](component-table.md) table for a component, then the component is installed to run locally.</span></span>

<span data-ttu-id="dcd8a-111">Das Installationsprogramm wertet die folgenden Eigenschaften immer in der folgenden Reihenfolge aus:</span><span class="sxs-lookup"><span data-stu-id="dcd8a-111">The installer always evaluates the following properties in the following order:</span></span>

1.  [<span data-ttu-id="dcd8a-112">**ADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="dcd8a-112">**ADDLOCAL**</span></span>](addlocal.md)
2.  [<span data-ttu-id="dcd8a-113">**Aufgeh**</span><span class="sxs-lookup"><span data-stu-id="dcd8a-113">**REMOVE**</span></span>](remove.md)
3.  [<span data-ttu-id="dcd8a-114">**Addsource**</span><span class="sxs-lookup"><span data-stu-id="dcd8a-114">**ADDSOURCE**</span></span>](addsource.md)
4.  [<span data-ttu-id="dcd8a-115">**Adddefault**</span><span class="sxs-lookup"><span data-stu-id="dcd8a-115">**ADDDEFAULT**</span></span>](adddefault.md)
5.  [<span data-ttu-id="dcd8a-116">**Installieren Sie**</span><span class="sxs-lookup"><span data-stu-id="dcd8a-116">**REINSTALL**</span></span>](reinstall.md)
6.  [<span data-ttu-id="dcd8a-117">**Benen**</span><span class="sxs-lookup"><span data-stu-id="dcd8a-117">**ADVERTISE**</span></span>](advertise.md)
7.  [<span data-ttu-id="dcd8a-118">**Compaddlocal**</span><span class="sxs-lookup"><span data-stu-id="dcd8a-118">**COMPADDLOCAL**</span></span>](compaddlocal.md)
8.  <span data-ttu-id="dcd8a-119">**Compaddsource**</span><span class="sxs-lookup"><span data-stu-id="dcd8a-119">**COMPADDSOURCE**</span></span>
9.  [<span data-ttu-id="dcd8a-120">**Compadddefault**</span><span class="sxs-lookup"><span data-stu-id="dcd8a-120">**COMPADDDEFAULT**</span></span>](compadddefault.md)
10. [<span data-ttu-id="dcd8a-121">**Fileaddlocal**</span><span class="sxs-lookup"><span data-stu-id="dcd8a-121">**FILEADDLOCAL**</span></span>](fileaddlocal.md)
11. [<span data-ttu-id="dcd8a-122">**Fileaddsource**</span><span class="sxs-lookup"><span data-stu-id="dcd8a-122">**FILEADDSOURCE**</span></span>](fileaddsource.md)
12. [<span data-ttu-id="dcd8a-123">**Fileadddefault**</span><span class="sxs-lookup"><span data-stu-id="dcd8a-123">**FILEADDDEFAULT**</span></span>](fileadddefault.md)

<span data-ttu-id="dcd8a-124">Wenn die Befehlszeile z. b. Folgendes angibt: ADDLOCAL = ALL, addsource = myfeature, werden alle Features zuerst auf Run-Local festgelegt, und myfeature wird auf Run-From-Source festgelegt.</span><span class="sxs-lookup"><span data-stu-id="dcd8a-124">For example, if the command line specifies: ADDLOCAL=ALL, ADDSOURCE = MyFeature, all the features are first set to run-local and then MyFeature is set to run-from-source.</span></span> <span data-ttu-id="dcd8a-125">Wenn die Befehlszeile "ADDSOURCE = ALL", "ADDLOCAL = myfeature" lautet, ist "First myfeature" auf "Run-local" festgelegt, und wenn "ADDSOURCE = ALL" ausgewertet wird, werden alle Funktionen (einschließlich "myfeature") auf "Run-From-Source" zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="dcd8a-125">If the command line is: ADDSOURCE=ALL, ADDLOCAL=MyFeature, first MyFeature is set to run-local, and then when ADDSOURCE=ALL is evaluated, all features (including MyFeature) are reset to run-from-source.</span></span>

<span data-ttu-id="dcd8a-126">Der Installer legt die [**vorab ausgewählte**](preselected.md) Eigenschaft während der Wiederaufnahme einer angehaltenen Installation auf den Wert "1" fest, oder wenn eine der oben aufgeführten Eigenschaften in der Befehlszeile angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="dcd8a-126">The installer sets the [**Preselected**](preselected.md) property to a value of "1" during the resumption of a suspended installation or when any of the above properties are specified on the command line.</span></span>

## <a name="requirements"></a><span data-ttu-id="dcd8a-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dcd8a-127">Requirements</span></span>



| <span data-ttu-id="dcd8a-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dcd8a-128">Requirement</span></span> | <span data-ttu-id="dcd8a-129">Wert</span><span class="sxs-lookup"><span data-stu-id="dcd8a-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dcd8a-130">Version</span><span class="sxs-lookup"><span data-stu-id="dcd8a-130">Version</span></span><br/> | <span data-ttu-id="dcd8a-131">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="dcd8a-131">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="dcd8a-132">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="dcd8a-132">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="dcd8a-133">Windows Installer unter Windows Server 2003 oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="dcd8a-133">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="dcd8a-134">Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="dcd8a-134">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="dcd8a-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dcd8a-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dcd8a-136">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="dcd8a-136">Properties</span></span>](properties.md)
</dt> </dl>

 

 




