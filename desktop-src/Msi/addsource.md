---
description: Der Wert der addsource-Eigenschaft ist eine Liste von Funktionen, die durch Kommas getrennt sind und zum Ausführen von der Quelle installiert werden müssen.
ms.assetid: 7bc38b49-72d8-4b0c-bd71-284a638e7860
title: Addsource (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd51d6f86060def1a7536134a0041f1e15178a91
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106374024"
---
# <a name="addsource-property"></a><span data-ttu-id="cc95f-103">Addsource (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="cc95f-103">ADDSOURCE property</span></span>

<span data-ttu-id="cc95f-104">Der Wert der **addsource** -Eigenschaft ist eine Liste von Funktionen, die durch Kommas getrennt sind und zum Ausführen von der Quelle installiert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="cc95f-104">The value of the **ADDSOURCE** property is a list of features that are delimited by commas, and are to be installed to run from the source.</span></span> <span data-ttu-id="cc95f-105">Die Funktionen müssen in der featurespalte der [Funktions Tabelle](feature-table.md)vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="cc95f-105">The features must be present in the Feature column of the [Feature Table](feature-table.md).</span></span> <span data-ttu-id="cc95f-106">Verwenden Sie addsource = all in der Befehlszeile, um alle Features zu installieren, die von der Quelle ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="cc95f-106">To install all features as run from source, use ADDSOURCE=ALL on the command line.</span></span> <span data-ttu-id="cc95f-107">Geben Sie addsource = all nicht in die [Eigenschaften Tabelle](property-table.md)ein, da hierdurch ein Paket aus der Quelle generiert wird, das nicht ordnungsgemäß entfernt werden kann.</span><span class="sxs-lookup"><span data-stu-id="cc95f-107">Do not enter ADDSOURCE=ALL into the [Property Table](property-table.md), because this generates a run-from-source package that cannot be correctly removed.</span></span>

## <a name="remarks"></a><span data-ttu-id="cc95f-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cc95f-108">Remarks</span></span>

<span data-ttu-id="cc95f-109">Bei den Funktionsnamen wird Groß-/Kleinschreibung beachtet.</span><span class="sxs-lookup"><span data-stu-id="cc95f-109">The feature names are case sensitive.</span></span> <span data-ttu-id="cc95f-110">Wenn das LocalOnly-Bitflag in der Spalte Attribute der [Komponenten Tabelle](component-table.md) für eine Komponente eines Features in der Liste festgelegt ist, wird diese Komponente zur lokalen Installation installiert.</span><span class="sxs-lookup"><span data-stu-id="cc95f-110">If the LocalOnly bit flag is set in the Attributes column of the [Component Table](component-table.md) for a component of a feature in the list, that component is installed to run locally.</span></span>

<span data-ttu-id="cc95f-111">Das Installationsprogramm wertet die folgenden Eigenschaften immer in der folgenden Reihenfolge aus:</span><span class="sxs-lookup"><span data-stu-id="cc95f-111">The installer always evaluates the following properties in the following order:</span></span>

1.  [<span data-ttu-id="cc95f-112">**ADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="cc95f-112">**ADDLOCAL**</span></span>](addlocal.md)
2.  [<span data-ttu-id="cc95f-113">**Aufgeh**</span><span class="sxs-lookup"><span data-stu-id="cc95f-113">**REMOVE**</span></span>](remove.md)
3.  <span data-ttu-id="cc95f-114">**Addsource**</span><span class="sxs-lookup"><span data-stu-id="cc95f-114">**ADDSOURCE**</span></span>
4.  [<span data-ttu-id="cc95f-115">**Adddefault**</span><span class="sxs-lookup"><span data-stu-id="cc95f-115">**ADDDEFAULT**</span></span>](adddefault.md)
5.  [<span data-ttu-id="cc95f-116">**Installieren Sie**</span><span class="sxs-lookup"><span data-stu-id="cc95f-116">**REINSTALL**</span></span>](reinstall.md)
6.  [<span data-ttu-id="cc95f-117">**Benen**</span><span class="sxs-lookup"><span data-stu-id="cc95f-117">**ADVERTISE**</span></span>](advertise.md)
7.  [<span data-ttu-id="cc95f-118">**Compaddlocal**</span><span class="sxs-lookup"><span data-stu-id="cc95f-118">**COMPADDLOCAL**</span></span>](compaddlocal.md)
8.  [<span data-ttu-id="cc95f-119">**Compaddsource**</span><span class="sxs-lookup"><span data-stu-id="cc95f-119">**COMPADDSOURCE**</span></span>](compaddsource.md)
9.  [<span data-ttu-id="cc95f-120">**Compadddefault**</span><span class="sxs-lookup"><span data-stu-id="cc95f-120">**COMPADDDEFAULT**</span></span>](compadddefault.md)
10. [<span data-ttu-id="cc95f-121">**Fileaddlocal**</span><span class="sxs-lookup"><span data-stu-id="cc95f-121">**FILEADDLOCAL**</span></span>](fileaddlocal.md)
11. [<span data-ttu-id="cc95f-122">**Fileaddsource**</span><span class="sxs-lookup"><span data-stu-id="cc95f-122">**FILEADDSOURCE**</span></span>](fileaddsource.md)
12. [<span data-ttu-id="cc95f-123">**Fileadddefault**</span><span class="sxs-lookup"><span data-stu-id="cc95f-123">**FILEADDDEFAULT**</span></span>](fileadddefault.md)

<span data-ttu-id="cc95f-124">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="cc95f-124">For example:</span></span>

-   <span data-ttu-id="cc95f-125">Wenn in der Befehlszeile Folgendes angegeben wird: ADDLOCAL = ALL, addsource = **myfeature**, werden alle Features zuerst auf Run-Local festgelegt, und **myfeature** wird auf Run-From-Source festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cc95f-125">If the command line specifies: ADDLOCAL=ALL, ADDSOURCE = **MyFeature**, all the features are first set to run-local and then **MyFeature** is set to run-from-source.</span></span>
-   <span data-ttu-id="cc95f-126">Wenn die Befehlszeile "ADDSOURCE = ALL", "ADDLOCAL =**myfeature**" lautet, ist "First **myfeature** " auf "Run-local" festgelegt, und wenn "ADDSOURCE = ALL" ausgewertet wird, werden alle Funktionen (einschließlich " **myfeature**") auf "Run-From-Source" zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="cc95f-126">If the command line is: ADDSOURCE=ALL, ADDLOCAL=**MyFeature**, first **MyFeature** is set to run-local, and then when ADDSOURCE=ALL is evaluated, all features (including **MyFeature**) are reset to run-from-source.</span></span>

<span data-ttu-id="cc95f-127">Der Installer legt die [**vorab ausgewählte**](preselected.md) Eigenschaft während der Wiederaufnahme einer angehaltenen Installation auf den Wert "1" fest, oder wenn eine der oben aufgeführten Eigenschaften in der Befehlszeile angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="cc95f-127">The installer sets the [**Preselected**](preselected.md) Property to a value of "1" during the resumption of a suspended installation, or when any of the above properties are specified on the command line.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc95f-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cc95f-128">Requirements</span></span>



| <span data-ttu-id="cc95f-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cc95f-129">Requirement</span></span> | <span data-ttu-id="cc95f-130">Wert</span><span class="sxs-lookup"><span data-stu-id="cc95f-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc95f-131">Version</span><span class="sxs-lookup"><span data-stu-id="cc95f-131">Version</span></span><br/> | <span data-ttu-id="cc95f-132">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="cc95f-132">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="cc95f-133">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="cc95f-133">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="cc95f-134">Windows Installer unter Windows Server 2003 oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="cc95f-134">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="cc95f-135">Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="cc95f-135">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="cc95f-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cc95f-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc95f-137">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="cc95f-137">Properties</span></span>](properties.md)
</dt> </dl>

 

 




