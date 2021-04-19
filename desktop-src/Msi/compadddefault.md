---
description: Der Wert der compadddefault-Eigenschaft ist eine Liste der Komponenten-GUIDs aus der ComponentID-Spalte der Komponenten Tabelle, die in der Standardkonfiguration als Trennzeichen getrennt sind.
ms.assetid: 1bf05680-fcba-4fbb-8f8c-4203a90346ce
title: Compadddefault (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0e96d2259f0610a3030e79f8685c498a0fb2d83
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356420"
---
# <a name="compadddefault-property"></a><span data-ttu-id="a6f32-103">Compadddefault (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="a6f32-103">COMPADDDEFAULT property</span></span>

<span data-ttu-id="a6f32-104">Der Wert der **compadddefault** -Eigenschaft ist eine Liste der Komponenten-GUIDs aus der ComponentID-Spalte der [Komponenten Tabelle](component-table.md), die in der Standardkonfiguration als Trennzeichen getrennt sind.</span><span class="sxs-lookup"><span data-stu-id="a6f32-104">The value of the **COMPADDDEFAULT** property is a list of component GUIDs from the ComponentId column of the [Component table](component-table.md), delimited by commas, that are installed in their default configuration.</span></span> <span data-ttu-id="a6f32-105">Für jede Komponenten-ID in der Liste installiert das Installationsprogramm die-Funktion, die den geringsten Speicherplatz benötigt.</span><span class="sxs-lookup"><span data-stu-id="a6f32-105">For each component ID in the list, the installer installs the feature that requires the least disk space.</span></span> <span data-ttu-id="a6f32-106">Die Komponenten-IDs in der Liste müssen in der ComponentID-Spalte der [Component-Tabelle](component-table.md)vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="a6f32-106">The component IDs in the list must be present in the ComponentId column of the [Component table](component-table.md).</span></span> <span data-ttu-id="a6f32-107">Eine Funktion wird in demselben Installationsstatus installiert, als ob der Benutzer eine Installation bei Bedarf der Funktion angefordert hätte.</span><span class="sxs-lookup"><span data-stu-id="a6f32-107">A feature is installed in the same installation state as if the user had requested an installation-on-demand of the feature.</span></span> <span data-ttu-id="a6f32-108">Der Status wird durch die Bits festgelegt, die für die Funktion in der Spalte Attribute der [Funktions Tabelle](feature-table.md)festgelegt sind, und welche Bits für die Komponenten der Funktion in der Spalte Attribute der Komponenten Tabelle festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="a6f32-108">The state is determined by which bits are set for the feature in the Attributes column of the [Feature table](feature-table.md), and which bits are set for the feature's components in the Attributes column of the Component table.</span></span>

## <a name="remarks"></a><span data-ttu-id="a6f32-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a6f32-109">Remarks</span></span>

<span data-ttu-id="a6f32-110">Beachten Sie Folgendes: Wenn das sourceOnly-Bitflag in der Attribute-Spalte der [Komponenten](component-table.md) Tabelle für eine Komponente festgelegt ist, wird die Komponente installiert, um von der Quelle ausgeführt zu werden.</span><span class="sxs-lookup"><span data-stu-id="a6f32-110">Note that if the SourceOnly bit flag is set in the Attributes column of the [Component](component-table.md) table for a component, then the component is installed to run from source.</span></span>

<span data-ttu-id="a6f32-111">Das Installationsprogramm wertet die folgenden Eigenschaften immer in der folgenden Reihenfolge aus:</span><span class="sxs-lookup"><span data-stu-id="a6f32-111">The installer always evaluates the following properties in the following order.</span></span>

1.  [<span data-ttu-id="a6f32-112">**ADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="a6f32-112">**ADDLOCAL**</span></span>](addlocal.md)
2.  [<span data-ttu-id="a6f32-113">**Aufgeh**</span><span class="sxs-lookup"><span data-stu-id="a6f32-113">**REMOVE**</span></span>](remove.md)
3.  [<span data-ttu-id="a6f32-114">**Addsource**</span><span class="sxs-lookup"><span data-stu-id="a6f32-114">**ADDSOURCE**</span></span>](addsource.md)
4.  [<span data-ttu-id="a6f32-115">**Adddefault**</span><span class="sxs-lookup"><span data-stu-id="a6f32-115">**ADDDEFAULT**</span></span>](adddefault.md)
5.  [<span data-ttu-id="a6f32-116">**Installieren Sie**</span><span class="sxs-lookup"><span data-stu-id="a6f32-116">**REINSTALL**</span></span>](reinstall.md)
6.  [<span data-ttu-id="a6f32-117">**Benen**</span><span class="sxs-lookup"><span data-stu-id="a6f32-117">**ADVERTISE**</span></span>](advertise.md)
7.  [<span data-ttu-id="a6f32-118">**Compaddlocal**</span><span class="sxs-lookup"><span data-stu-id="a6f32-118">**COMPADDLOCAL**</span></span>](compaddlocal.md)
8.  [<span data-ttu-id="a6f32-119">**Compaddsource**</span><span class="sxs-lookup"><span data-stu-id="a6f32-119">**COMPADDSOURCE**</span></span>](compaddsource.md)
9.  <span data-ttu-id="a6f32-120">**Compadddefault**</span><span class="sxs-lookup"><span data-stu-id="a6f32-120">**COMPADDDEFAULT**</span></span>
10. [<span data-ttu-id="a6f32-121">**Fileaddlocal**</span><span class="sxs-lookup"><span data-stu-id="a6f32-121">**FILEADDLOCAL**</span></span>](fileaddlocal.md)
11. [<span data-ttu-id="a6f32-122">**Fileaddsource**</span><span class="sxs-lookup"><span data-stu-id="a6f32-122">**FILEADDSOURCE**</span></span>](fileaddsource.md)
12. [<span data-ttu-id="a6f32-123">**Fileadddefault**</span><span class="sxs-lookup"><span data-stu-id="a6f32-123">**FILEADDDEFAULT**</span></span>](fileadddefault.md)

<span data-ttu-id="a6f32-124">Wenn die Befehlszeile z. b. Folgendes angibt: ADDLOCAL = ALL, addsource = myfeature, werden alle Features zuerst auf Run-Local festgelegt, und myfeature wird auf Run-From-Source festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a6f32-124">For example, if the command line specifies: ADDLOCAL=ALL, ADDSOURCE = MyFeature, all the features are first set to run-local and then MyFeature is set to run-from-source.</span></span> <span data-ttu-id="a6f32-125">Wenn die Befehlszeile "ADDSOURCE = ALL", "ADDLOCAL = myfeature" lautet, ist "First myfeature" auf "Run-local" festgelegt, und wenn "ADDSOURCE = ALL" ausgewertet wird, werden alle Funktionen (einschließlich "myfeature") auf "Run-From-Source" zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="a6f32-125">If the command line is: ADDSOURCE=ALL, ADDLOCAL=MyFeature, first MyFeature is set to run-local, and then when ADDSOURCE=ALL is evaluated, all features (including MyFeature) are reset to run-from-source.</span></span>

<span data-ttu-id="a6f32-126">Der Installer legt die [**vorab ausgewählte**](preselected.md) Eigenschaft während der Wiederaufnahme einer angehaltenen Installation auf den Wert "1" fest, oder wenn eine der oben aufgeführten Eigenschaften in der Befehlszeile angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="a6f32-126">The installer sets the [**Preselected**](preselected.md) property to a value of "1" during the resumption of a suspended installation or when any of the above properties are specified on the command line.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6f32-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a6f32-127">Requirements</span></span>



| <span data-ttu-id="a6f32-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a6f32-128">Requirement</span></span> | <span data-ttu-id="a6f32-129">Wert</span><span class="sxs-lookup"><span data-stu-id="a6f32-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6f32-130">Version</span><span class="sxs-lookup"><span data-stu-id="a6f32-130">Version</span></span><br/> | <span data-ttu-id="a6f32-131">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="a6f32-131">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="a6f32-132">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="a6f32-132">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="a6f32-133">Windows Installer unter Windows Server 2003 oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a6f32-133">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="a6f32-134">Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="a6f32-134">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a6f32-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a6f32-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6f32-136">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a6f32-136">Properties</span></span>](properties.md)
</dt> </dl>

 

 




