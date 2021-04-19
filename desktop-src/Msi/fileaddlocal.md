---
description: Der Wert der fileaddlocal-Eigenschaft gibt eine Liste von Datei Schlüsseln an, die durch Kommas getrennt sind, die zum Ausführen vom lokalen Quell Medium installiert werden sollen.
ms.assetid: 89ae876e-53f0-4c1d-ba16-7513af79ee5e
title: Fileaddlocal (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01e3e05a35e5bcd4fc672a2feb6bd2f40619bfcb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352841"
---
# <a name="fileaddlocal-property"></a><span data-ttu-id="40f0c-103">Fileaddlocal (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="40f0c-103">FILEADDLOCAL property</span></span>

<span data-ttu-id="40f0c-104">Der Wert der **fileaddlocal** -Eigenschaft gibt eine Liste von Datei Schlüsseln an, die durch Kommas getrennt sind, die zum Ausführen vom lokalen Quell Medium installiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="40f0c-104">The value of the **FILEADDLOCAL** property denotes a list of file keys delimited by commas that are to be installed to run from the local source media.</span></span> <span data-ttu-id="40f0c-105">Für jeden Datei Schlüssel in der Liste bestimmt das Installationsprogramm die Komponente, die diese Datei steuert. Anschließend werden alle Features, die mit dieser Komponente verknüpft sind, von der [FeatureComponents](featurecomponents-table.md) -Tabelle überprüft und das Feature installiert, das den geringsten Speicherplatz benötigt.</span><span class="sxs-lookup"><span data-stu-id="40f0c-105">For each file key in the list, the installer determines the component that controls that file, then examines all features linked to that component by the [FeatureComponents](featurecomponents-table.md) table and installs the feature that requires the least amount of disk space.</span></span> <span data-ttu-id="40f0c-106">Die Datei Schlüssel in der Liste müssen in der Datei Spalte der [Datei](file-table.md) Tabelle vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="40f0c-106">The file keys in the list must be present in the File column of the [File](file-table.md) table.</span></span>

## <a name="remarks"></a><span data-ttu-id="40f0c-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="40f0c-107">Remarks</span></span>

<span data-ttu-id="40f0c-108">Beachten Sie, dass die Datei Schlüsselnamen die Groß-/Kleinschreibung beachten.</span><span class="sxs-lookup"><span data-stu-id="40f0c-108">Note that the file key names are case-sensitive.</span></span> <span data-ttu-id="40f0c-109">Beachten Sie auch Folgendes: Wenn das LocalOnly-Bitflag in der Attribute-Spalte der [Komponenten](component-table.md) Tabelle für eine Komponente festgelegt ist, wird die Komponente zur lokalen Installation installiert.</span><span class="sxs-lookup"><span data-stu-id="40f0c-109">Also note that if the LocalOnly bit flag is set in the Attributes column of the [Component](component-table.md) table for a component, then the component is installed to run locally.</span></span>

<span data-ttu-id="40f0c-110">Das Installationsprogramm wertet die folgenden Eigenschaften immer in der folgenden Reihenfolge aus:</span><span class="sxs-lookup"><span data-stu-id="40f0c-110">The installer always evaluates the following properties in the following order.</span></span>

1.  [<span data-ttu-id="40f0c-111">**ADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="40f0c-111">**ADDLOCAL**</span></span>](addlocal.md)
2.  [<span data-ttu-id="40f0c-112">**Aufgeh**</span><span class="sxs-lookup"><span data-stu-id="40f0c-112">**REMOVE**</span></span>](remove.md)
3.  [<span data-ttu-id="40f0c-113">**Addsource**</span><span class="sxs-lookup"><span data-stu-id="40f0c-113">**ADDSOURCE**</span></span>](addsource.md)
4.  [<span data-ttu-id="40f0c-114">**Adddefault**</span><span class="sxs-lookup"><span data-stu-id="40f0c-114">**ADDDEFAULT**</span></span>](adddefault.md)
5.  [<span data-ttu-id="40f0c-115">**Installieren Sie**</span><span class="sxs-lookup"><span data-stu-id="40f0c-115">**REINSTALL**</span></span>](reinstall.md)
6.  [<span data-ttu-id="40f0c-116">**Benen**</span><span class="sxs-lookup"><span data-stu-id="40f0c-116">**ADVERTISE**</span></span>](advertise.md)
7.  [<span data-ttu-id="40f0c-117">**Compaddlocal**</span><span class="sxs-lookup"><span data-stu-id="40f0c-117">**COMPADDLOCAL**</span></span>](compaddlocal.md)
8.  [<span data-ttu-id="40f0c-118">**Compaddsource**</span><span class="sxs-lookup"><span data-stu-id="40f0c-118">**COMPADDSOURCE**</span></span>](compaddsource.md)
9.  [<span data-ttu-id="40f0c-119">**Compadddefault**</span><span class="sxs-lookup"><span data-stu-id="40f0c-119">**COMPADDDEFAULT**</span></span>](compadddefault.md)
10. <span data-ttu-id="40f0c-120">**Fileaddlocal**</span><span class="sxs-lookup"><span data-stu-id="40f0c-120">**FILEADDLOCAL**</span></span>
11. [<span data-ttu-id="40f0c-121">**Fileaddsource**</span><span class="sxs-lookup"><span data-stu-id="40f0c-121">**FILEADDSOURCE**</span></span>](fileaddsource.md)
12. [<span data-ttu-id="40f0c-122">**Fileadddefault**</span><span class="sxs-lookup"><span data-stu-id="40f0c-122">**FILEADDDEFAULT**</span></span>](fileadddefault.md)

<span data-ttu-id="40f0c-123">Wenn die Befehlszeile z. b. Folgendes angibt: ADDLOCAL = ALL, addsource = myfeature, werden alle Features zuerst auf Run-Local festgelegt, und myfeature wird auf Run-From-Source festgelegt.</span><span class="sxs-lookup"><span data-stu-id="40f0c-123">For example, if the command line specifies: ADDLOCAL=ALL, ADDSOURCE = MyFeature, all the features are first set to run-local and then MyFeature is set to run-from-source.</span></span> <span data-ttu-id="40f0c-124">Wenn die Befehlszeile "ADDSOURCE = ALL", "ADDLOCAL = myfeature" lautet, ist "First myfeature" auf "Run-local" festgelegt, und wenn "ADDSOURCE = ALL" ausgewertet wird, werden alle Funktionen (einschließlich "myfeature") auf "Run-From-Source" zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="40f0c-124">If the command line is: ADDSOURCE=ALL, ADDLOCAL=MyFeature, first MyFeature is set to run-local, and then when ADDSOURCE=ALL is evaluated, all features (including MyFeature) are reset to run-from-source.</span></span>

<span data-ttu-id="40f0c-125">Der Installer legt die [**vorab ausgewählte**](preselected.md) Eigenschaft während der Wiederaufnahme einer angehaltenen Installation auf den Wert "1" fest, oder wenn eine der oben aufgeführten Eigenschaften in der Befehlszeile angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="40f0c-125">The installer sets the [**Preselected**](preselected.md) property to a value of "1" during the resumption of a suspended installation or when any of the above properties are specified on the command line.</span></span>

## <a name="requirements"></a><span data-ttu-id="40f0c-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="40f0c-126">Requirements</span></span>



| <span data-ttu-id="40f0c-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="40f0c-127">Requirement</span></span> | <span data-ttu-id="40f0c-128">Wert</span><span class="sxs-lookup"><span data-stu-id="40f0c-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="40f0c-129">Version</span><span class="sxs-lookup"><span data-stu-id="40f0c-129">Version</span></span><br/> | <span data-ttu-id="40f0c-130">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="40f0c-130">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="40f0c-131">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="40f0c-131">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="40f0c-132">Windows Installer unter Windows Server 2003 oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="40f0c-132">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="40f0c-133">Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="40f0c-133">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="40f0c-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="40f0c-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40f0c-135">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="40f0c-135">Properties</span></span>](properties.md)
</dt> </dl>

 

 




