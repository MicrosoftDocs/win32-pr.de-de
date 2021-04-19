---
description: Der Wert der fileaddsource-Eigenschaft gibt eine Liste von Datei Schlüsseln an, die durch Kommas getrennt sind, die zur Laufzeit vom Quell Medium installiert werden sollen.
ms.assetid: 52e328e7-7a98-4762-86a1-48e52fd55882
title: Fileaddsource (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24b99ea1d9f4d6e212b74d6c4ee54655dce98c60
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369948"
---
# <a name="fileaddsource-property"></a><span data-ttu-id="7b3ec-103">Fileaddsource (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="7b3ec-103">FILEADDSOURCE property</span></span>

<span data-ttu-id="7b3ec-104">Der Wert der **fileaddsource** -Eigenschaft gibt eine Liste von Datei Schlüsseln an, die durch Kommas getrennt sind, die zur Laufzeit vom Quell Medium installiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="7b3ec-104">The value of the **FILEADDSOURCE** property denotes a list of file keys delimited by commas that are to be installed to run from the source media.</span></span> <span data-ttu-id="7b3ec-105">Für jeden Datei Schlüssel in der Liste bestimmt das Installationsprogramm die Komponente, die diese Datei steuert. Anschließend werden alle Features, die mit dieser Komponente verknüpft sind, von der [FeatureComponents](featurecomponents-table.md) -Tabelle überprüft und das Feature installiert, das den geringsten Speicherplatz benötigt.</span><span class="sxs-lookup"><span data-stu-id="7b3ec-105">For each file key in the list, the installer determines the component that controls that file, then examines all features linked to that component by the [FeatureComponents](featurecomponents-table.md) table and installs the feature that requires the least amount of disk space.</span></span> <span data-ttu-id="7b3ec-106">Die Datei Schlüssel in der Liste müssen in der Datei Spalte der [Datei](file-table.md) Tabelle vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="7b3ec-106">The file keys in the list must be present in the File column of the [File](file-table.md) table.</span></span>

## <a name="remarks"></a><span data-ttu-id="7b3ec-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7b3ec-107">Remarks</span></span>

<span data-ttu-id="7b3ec-108">Beachten Sie, dass die Datei Schlüsselnamen die Groß-/Kleinschreibung beachten.</span><span class="sxs-lookup"><span data-stu-id="7b3ec-108">Note that the file key names are case-sensitive.</span></span> <span data-ttu-id="7b3ec-109">Beachten Sie auch Folgendes: Wenn das LocalOnly-Bitflag in der Attribute-Spalte der [Komponenten](component-table.md) Tabelle für eine Komponente festgelegt ist, wird die Komponente zur lokalen Installation installiert.</span><span class="sxs-lookup"><span data-stu-id="7b3ec-109">Also note that if the LocalOnly bit flag is set in the Attributes column of the [Component](component-table.md) table for a component, then the component is installed to run locally.</span></span>

<span data-ttu-id="7b3ec-110">Das Installationsprogramm wertet die folgenden Eigenschaften immer in der folgenden Reihenfolge aus:</span><span class="sxs-lookup"><span data-stu-id="7b3ec-110">The installer always evaluates the following properties in the following order.</span></span>

1.  [<span data-ttu-id="7b3ec-111">**ADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="7b3ec-111">**ADDLOCAL**</span></span>](addlocal.md)
2.  [<span data-ttu-id="7b3ec-112">**Aufgeh**</span><span class="sxs-lookup"><span data-stu-id="7b3ec-112">**REMOVE**</span></span>](remove.md)
3.  [<span data-ttu-id="7b3ec-113">**Addsource**</span><span class="sxs-lookup"><span data-stu-id="7b3ec-113">**ADDSOURCE**</span></span>](addsource.md)
4.  [<span data-ttu-id="7b3ec-114">**Adddefault**</span><span class="sxs-lookup"><span data-stu-id="7b3ec-114">**ADDDEFAULT**</span></span>](adddefault.md)
5.  [<span data-ttu-id="7b3ec-115">**Installieren Sie**</span><span class="sxs-lookup"><span data-stu-id="7b3ec-115">**REINSTALL**</span></span>](reinstall.md)
6.  [<span data-ttu-id="7b3ec-116">**Benen**</span><span class="sxs-lookup"><span data-stu-id="7b3ec-116">**ADVERTISE**</span></span>](advertise.md)
7.  [<span data-ttu-id="7b3ec-117">**Compaddlocal**</span><span class="sxs-lookup"><span data-stu-id="7b3ec-117">**COMPADDLOCAL**</span></span>](compaddlocal.md)
8.  [<span data-ttu-id="7b3ec-118">**Compaddsource**</span><span class="sxs-lookup"><span data-stu-id="7b3ec-118">**COMPADDSOURCE**</span></span>](compaddsource.md)
9.  [<span data-ttu-id="7b3ec-119">**Compadddefault**</span><span class="sxs-lookup"><span data-stu-id="7b3ec-119">**COMPADDDEFAULT**</span></span>](compadddefault.md)
10. [<span data-ttu-id="7b3ec-120">**Fileaddlocal**</span><span class="sxs-lookup"><span data-stu-id="7b3ec-120">**FILEADDLOCAL**</span></span>](fileaddlocal.md)
11. <span data-ttu-id="7b3ec-121">**Fileaddsource**</span><span class="sxs-lookup"><span data-stu-id="7b3ec-121">**FILEADDSOURCE**</span></span>
12. [<span data-ttu-id="7b3ec-122">**Fileadddefault**</span><span class="sxs-lookup"><span data-stu-id="7b3ec-122">**FILEADDDEFAULT**</span></span>](fileadddefault.md)

<span data-ttu-id="7b3ec-123">Wenn die Befehlszeile z. b. Folgendes angibt: ADDLOCAL = ALL, addsource = myfeature, werden alle Features zuerst auf Run-Local festgelegt, und myfeature wird auf Run-From-Source festgelegt.</span><span class="sxs-lookup"><span data-stu-id="7b3ec-123">For example, if the command line specifies: ADDLOCAL=ALL, ADDSOURCE = MyFeature, all the features are first set to run-local and then MyFeature is set to run-from-source.</span></span> <span data-ttu-id="7b3ec-124">Wenn die Befehlszeile "ADDSOURCE = ALL", "ADDLOCAL = myfeature" lautet, ist "First myfeature" auf "Run-local" festgelegt, und wenn "ADDSOURCE = ALL" ausgewertet wird, werden alle Funktionen (einschließlich "myfeature") auf "Run-From-Source" zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="7b3ec-124">If the command line is: ADDSOURCE=ALL, ADDLOCAL=MyFeature, first MyFeature is set to run-local, and then when ADDSOURCE=ALL is evaluated, all features (including MyFeature) are reset to run-from-source.</span></span>

<span data-ttu-id="7b3ec-125">Der Installer legt die [**vorab ausgewählte**](preselected.md) Eigenschaft während der Wiederaufnahme einer angehaltenen Installation auf den Wert "1" fest, oder wenn eine der oben aufgeführten Eigenschaften in der Befehlszeile angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="7b3ec-125">The installer sets the [**Preselected**](preselected.md) property to a value of "1" during the resumption of a suspended installation or when any of the above properties are specified on the command line.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b3ec-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7b3ec-126">Requirements</span></span>



| <span data-ttu-id="7b3ec-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7b3ec-127">Requirement</span></span> | <span data-ttu-id="7b3ec-128">Wert</span><span class="sxs-lookup"><span data-stu-id="7b3ec-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b3ec-129">Version</span><span class="sxs-lookup"><span data-stu-id="7b3ec-129">Version</span></span><br/> | <span data-ttu-id="7b3ec-130">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="7b3ec-130">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="7b3ec-131">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="7b3ec-131">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="7b3ec-132">Windows Installer unter Windows Server 2003 oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="7b3ec-132">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="7b3ec-133">Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="7b3ec-133">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7b3ec-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7b3ec-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b3ec-135">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7b3ec-135">Properties</span></span>](properties.md)
</dt> </dl>

 

 




