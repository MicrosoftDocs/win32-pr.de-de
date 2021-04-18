---
description: Der Wert der Eigenschaft fileadddefault ist eine Liste von Datei Schlüsseln, die durch Kommas getrennt sind, die in der Standardkonfiguration installiert sind.
ms.assetid: 089b8dd9-1841-4b6d-8da8-d5aa5de85a68
title: File adddefault (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1c1afc9658c58b048c4e75232d7e550acb36e57
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357934"
---
# <a name="fileadddefault-property"></a><span data-ttu-id="cc7e9-103">File adddefault (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="cc7e9-103">FILEADDDEFAULT property</span></span>

<span data-ttu-id="cc7e9-104">Der Wert der Eigenschaft **fileadddefault** ist eine Liste von Datei Schlüsseln, die durch Kommas getrennt sind, die in der Standardkonfiguration installiert sind.</span><span class="sxs-lookup"><span data-stu-id="cc7e9-104">The value of the **FILEADDDEFAULT** property is a list of file keys delimited by commas that are installed in their default configuration.</span></span> <span data-ttu-id="cc7e9-105">Für jeden Datei Schlüssel in der Liste bestimmt das Installationsprogramm die Komponente, die diese Datei steuert, und installiert die Funktion, die den geringsten Speicherplatz benötigt.</span><span class="sxs-lookup"><span data-stu-id="cc7e9-105">For each file key in the list, the installer determines the component that controls that file and installs the feature that requires the least disk space.</span></span> <span data-ttu-id="cc7e9-106">Die Datei Schlüssel in der Liste müssen in der Datei Spalte der [Datei](file-table.md) Tabelle vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="cc7e9-106">The file keys in the list must be present in the File column of the [File](file-table.md) table.</span></span> <span data-ttu-id="cc7e9-107">Eine Funktion wird in demselben Installationsstatus installiert, als ob der Benutzer eine Installation bei Bedarf der Funktion angefordert hätte.</span><span class="sxs-lookup"><span data-stu-id="cc7e9-107">A feature is installed in the same installation state as if the user had requested an installation-on-demand of the feature.</span></span> <span data-ttu-id="cc7e9-108">Der Status wird durch die Bits festgelegt, die für die Funktion in der Spalte Attribute der [Funktions Tabelle](feature-table.md)festgelegt sind, und welche Bits für die Komponenten der Funktion in der Spalte Attribute der Komponenten [Tabelle](component-table.md)festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="cc7e9-108">The state is determined by which bits are set for the feature in the Attributes column of the [Feature table](feature-table.md), and which bits are set for the feature's components in the Attributes column of the [Component table](component-table.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="cc7e9-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cc7e9-109">Remarks</span></span>

<span data-ttu-id="cc7e9-110">Beachten Sie, dass die Datei Schlüsselnamen die Groß-/Kleinschreibung beachten.</span><span class="sxs-lookup"><span data-stu-id="cc7e9-110">Note that the file key names are case-sensitive.</span></span> <span data-ttu-id="cc7e9-111">Beachten Sie auch Folgendes: Wenn das sourceOnly-Bitflag in der Attribute-Spalte der [Komponenten](component-table.md) Tabelle für eine Komponente festgelegt ist, wird die Komponente installiert, um von der Quelle ausgeführt zu werden.</span><span class="sxs-lookup"><span data-stu-id="cc7e9-111">Also note that if the SourceOnly bit flag is set in the Attributes column of the [Component](component-table.md) table for a component, then the component is installed to run from source.</span></span>

<span data-ttu-id="cc7e9-112">Das Installationsprogramm wertet die folgenden Eigenschaften immer in der folgenden Reihenfolge aus:</span><span class="sxs-lookup"><span data-stu-id="cc7e9-112">The installer always evaluates the following properties in the following order.</span></span>

1.  [<span data-ttu-id="cc7e9-113">**ADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="cc7e9-113">**ADDLOCAL**</span></span>](addlocal.md)
2.  [<span data-ttu-id="cc7e9-114">**Aufgeh**</span><span class="sxs-lookup"><span data-stu-id="cc7e9-114">**REMOVE**</span></span>](remove.md)
3.  [<span data-ttu-id="cc7e9-115">**Addsource**</span><span class="sxs-lookup"><span data-stu-id="cc7e9-115">**ADDSOURCE**</span></span>](addsource.md)
4.  [<span data-ttu-id="cc7e9-116">**Adddefault**</span><span class="sxs-lookup"><span data-stu-id="cc7e9-116">**ADDDEFAULT**</span></span>](adddefault.md)
5.  [<span data-ttu-id="cc7e9-117">**Installieren Sie**</span><span class="sxs-lookup"><span data-stu-id="cc7e9-117">**REINSTALL**</span></span>](reinstall.md)
6.  [<span data-ttu-id="cc7e9-118">**Benen**</span><span class="sxs-lookup"><span data-stu-id="cc7e9-118">**ADVERTISE**</span></span>](advertise.md)
7.  [<span data-ttu-id="cc7e9-119">**Compaddlocal**</span><span class="sxs-lookup"><span data-stu-id="cc7e9-119">**COMPADDLOCAL**</span></span>](compaddlocal.md)
8.  [<span data-ttu-id="cc7e9-120">**Compaddsource**</span><span class="sxs-lookup"><span data-stu-id="cc7e9-120">**COMPADDSOURCE**</span></span>](compaddsource.md)
9.  [<span data-ttu-id="cc7e9-121">**Compadddefault**</span><span class="sxs-lookup"><span data-stu-id="cc7e9-121">**COMPADDDEFAULT**</span></span>](compadddefault.md)
10. [<span data-ttu-id="cc7e9-122">**Fileaddlocal**</span><span class="sxs-lookup"><span data-stu-id="cc7e9-122">**FILEADDLOCAL**</span></span>](fileaddlocal.md)
11. [<span data-ttu-id="cc7e9-123">**Fileaddsource**</span><span class="sxs-lookup"><span data-stu-id="cc7e9-123">**FILEADDSOURCE**</span></span>](fileaddsource.md)
12. <span data-ttu-id="cc7e9-124">**Fileadddefault**</span><span class="sxs-lookup"><span data-stu-id="cc7e9-124">**FILEADDDEFAULT**</span></span>

<span data-ttu-id="cc7e9-125">Wenn die Befehlszeile z. b. Folgendes angibt: ADDLOCAL = ALL, addsource = myfeature, werden alle Features zuerst auf Run-Local festgelegt, und myfeature wird auf Run-From-Source festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cc7e9-125">For example, if the command line specifies: ADDLOCAL=ALL, ADDSOURCE = MyFeature, all the features are first set to run-local and then MyFeature is set to run-from-source.</span></span> <span data-ttu-id="cc7e9-126">Wenn die Befehlszeile "ADDSOURCE = ALL", "ADDLOCAL = myfeature" lautet, ist "First myfeature" auf "Run-local" festgelegt, und wenn "ADDSOURCE = ALL" ausgewertet wird, werden alle Funktionen (einschließlich "myfeature") auf "Run-From-Source" zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="cc7e9-126">If the command line is: ADDSOURCE=ALL, ADDLOCAL=MyFeature, first MyFeature is set to run-local, and then when ADDSOURCE=ALL is evaluated, all features (including MyFeature) are reset to run-from-source.</span></span>

<span data-ttu-id="cc7e9-127">Der Installer legt die [**vorab ausgewählte**](preselected.md) Eigenschaft während der Wiederaufnahme einer angehaltenen Installation auf den Wert "1" fest, oder wenn eine der oben aufgeführten Eigenschaften in der Befehlszeile angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="cc7e9-127">The installer sets the [**Preselected**](preselected.md) property to a value of "1" during the resumption of a suspended installation or when any of the above properties are specified on the command line.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc7e9-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cc7e9-128">Requirements</span></span>



| <span data-ttu-id="cc7e9-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cc7e9-129">Requirement</span></span> | <span data-ttu-id="cc7e9-130">Wert</span><span class="sxs-lookup"><span data-stu-id="cc7e9-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc7e9-131">Version</span><span class="sxs-lookup"><span data-stu-id="cc7e9-131">Version</span></span><br/> | <span data-ttu-id="cc7e9-132">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="cc7e9-132">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="cc7e9-133">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="cc7e9-133">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="cc7e9-134">Windows Installer unter Windows Server 2003 oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="cc7e9-134">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="cc7e9-135">Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="cc7e9-135">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="cc7e9-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cc7e9-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc7e9-137">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="cc7e9-137">Properties</span></span>](properties.md)
</dt> </dl>

 

 




