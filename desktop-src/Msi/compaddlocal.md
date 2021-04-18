---
description: Der Wert der compaddlocal-Eigenschaft ist eine Liste der Komponenten-GUIDs aus der ComponentID-Spalte der Komponenten Tabelle, die durch Kommas getrennt werden, die lokal installiert werden sollen.
ms.assetid: 10c178c5-1eae-4191-b79c-9285810efb6a
title: Compaddlocal (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e403459f0355c28d66da00170b9c649084afbb1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364549"
---
# <a name="compaddlocal-property"></a><span data-ttu-id="6d237-103">Compaddlocal (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="6d237-103">COMPADDLOCAL property</span></span>

<span data-ttu-id="6d237-104">Der Wert der **compaddlocal** -Eigenschaft ist eine Liste der Komponenten-GUIDs aus der ComponentID-Spalte der [Komponenten Tabelle](component-table.md), die durch Kommas getrennt werden, die lokal installiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="6d237-104">The value of the **COMPADDLOCAL** property is a list of component GUIDs from the ComponentId column of the [Component table](component-table.md), delimited by commas, that are to be installed locally.</span></span> <span data-ttu-id="6d237-105">Das Installationsprogramm verwendet diese Liste, um zu bestimmen, welche-Funktionen für die lokale Installation basierend auf den angegebenen Komponenten festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="6d237-105">The installer uses this list to determine which features are set to be installed locally, based on the specified components.</span></span> <span data-ttu-id="6d237-106">Für jede aufgelistete Komponenten-ID überprüft das Installationsprogramm alle Features, die mit dieser Komponente verknüpft sind, über die [FeatureComponents](featurecomponents-table.md) -Tabelle und installiert das Feature, das den geringsten Speicherplatz für die Installation erfordert.</span><span class="sxs-lookup"><span data-stu-id="6d237-106">For each listed component ID, the installer examines all features linked to that component through the [FeatureComponents](featurecomponents-table.md) table, and installs the feature that requires the least amount of disk space to install.</span></span> <span data-ttu-id="6d237-107">Die aufgeführten Komponenten müssen in der Component-Spalte der [Component](component-table.md) -Tabelle vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="6d237-107">The components listed must be present in the Component column of the [Component](component-table.md) table.</span></span>

## <a name="remarks"></a><span data-ttu-id="6d237-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6d237-108">Remarks</span></span>

<span data-ttu-id="6d237-109">Beachten Sie, dass bei den Komponentennamen die Groß-/Kleinschreibung beachtet</span><span class="sxs-lookup"><span data-stu-id="6d237-109">Note that the component names are case-sensitive.</span></span> <span data-ttu-id="6d237-110">Beachten Sie auch Folgendes: Wenn das sourceOnly-Bitflag in der Attribute-Spalte der [Komponenten](component-table.md) Tabelle für eine Komponente festgelegt ist, wird die Komponente installiert, um von der Quelle ausgeführt zu werden.</span><span class="sxs-lookup"><span data-stu-id="6d237-110">Also note that if the SourceOnly bit flag is set in the Attributes column of the [Component](component-table.md) table for a component, then the component is installed to run from source.</span></span>

<span data-ttu-id="6d237-111">Das Installationsprogramm wertet die folgenden Eigenschaften immer in der folgenden Reihenfolge aus:</span><span class="sxs-lookup"><span data-stu-id="6d237-111">The installer always evaluates the following properties in the following order.</span></span>

1.  [<span data-ttu-id="6d237-112">**ADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="6d237-112">**ADDLOCAL**</span></span>](addlocal.md)
2.  [<span data-ttu-id="6d237-113">**Aufgeh**</span><span class="sxs-lookup"><span data-stu-id="6d237-113">**REMOVE**</span></span>](remove.md)
3.  [<span data-ttu-id="6d237-114">**Addsource**</span><span class="sxs-lookup"><span data-stu-id="6d237-114">**ADDSOURCE**</span></span>](addsource.md)
4.  [<span data-ttu-id="6d237-115">**Adddefault**</span><span class="sxs-lookup"><span data-stu-id="6d237-115">**ADDDEFAULT**</span></span>](adddefault.md)
5.  [<span data-ttu-id="6d237-116">**Installieren Sie**</span><span class="sxs-lookup"><span data-stu-id="6d237-116">**REINSTALL**</span></span>](reinstall.md)
6.  [<span data-ttu-id="6d237-117">**Benen**</span><span class="sxs-lookup"><span data-stu-id="6d237-117">**ADVERTISE**</span></span>](advertise.md)
7.  <span data-ttu-id="6d237-118">**Compaddlocal**</span><span class="sxs-lookup"><span data-stu-id="6d237-118">**COMPADDLOCAL**</span></span>
8.  [<span data-ttu-id="6d237-119">**Compaddsource**</span><span class="sxs-lookup"><span data-stu-id="6d237-119">**COMPADDSOURCE**</span></span>](compaddsource.md)
9.  [<span data-ttu-id="6d237-120">**Compadddefault**</span><span class="sxs-lookup"><span data-stu-id="6d237-120">**COMPADDDEFAULT**</span></span>](compadddefault.md)
10. [<span data-ttu-id="6d237-121">**Fileaddlocal**</span><span class="sxs-lookup"><span data-stu-id="6d237-121">**FILEADDLOCAL**</span></span>](fileaddlocal.md)
11. [<span data-ttu-id="6d237-122">**Fileaddsource**</span><span class="sxs-lookup"><span data-stu-id="6d237-122">**FILEADDSOURCE**</span></span>](fileaddsource.md)
12. [<span data-ttu-id="6d237-123">**Fileadddefault**</span><span class="sxs-lookup"><span data-stu-id="6d237-123">**FILEADDDEFAULT**</span></span>](fileadddefault.md)

<span data-ttu-id="6d237-124">Wenn die Befehlszeile z. b. Folgendes angibt: ADDLOCAL = ALL, addsource = myfeature, werden alle Features zuerst auf Run-Local festgelegt, und myfeature wird auf Run-From-Source festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6d237-124">For example, if the command line specifies: ADDLOCAL=ALL, ADDSOURCE = MyFeature, all the features are first set to run-local and then MyFeature is set to run-from-source.</span></span> <span data-ttu-id="6d237-125">Wenn die Befehlszeile "ADDSOURCE = ALL", "ADDLOCAL = myfeature" lautet, ist "First myfeature" auf "Run-local" festgelegt, und wenn "ADDSOURCE = ALL" ausgewertet wird, werden alle Funktionen (einschließlich "myfeature") auf "Run-From-Source" zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="6d237-125">If the command line is: ADDSOURCE=ALL, ADDLOCAL=MyFeature, first MyFeature is set to run-local, and then when ADDSOURCE=ALL is evaluated, all features (including MyFeature) are reset to run-from-source.</span></span>

<span data-ttu-id="6d237-126">Der Installer legt die [**vorab ausgewählte**](preselected.md) Eigenschaft während der Wiederaufnahme einer angehaltenen Installation auf den Wert "1" fest, oder wenn eine der oben aufgeführten Eigenschaften in der Befehlszeile angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="6d237-126">The installer sets the [**Preselected**](preselected.md) property to a value of "1" during the resumption of a suspended installation or when any of the above properties are specified on the command line.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d237-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6d237-127">Requirements</span></span>



| <span data-ttu-id="6d237-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6d237-128">Requirement</span></span> | <span data-ttu-id="6d237-129">Wert</span><span class="sxs-lookup"><span data-stu-id="6d237-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d237-130">Version</span><span class="sxs-lookup"><span data-stu-id="6d237-130">Version</span></span><br/> | <span data-ttu-id="6d237-131">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="6d237-131">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="6d237-132">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="6d237-132">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="6d237-133">Windows Installer unter Windows Server 2003 oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="6d237-133">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="6d237-134">Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="6d237-134">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6d237-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6d237-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d237-136">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6d237-136">Properties</span></span>](properties.md)
</dt> </dl>

 

 




