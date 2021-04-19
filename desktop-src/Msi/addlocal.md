---
description: Der Wert der ADDLOCAL-Eigenschaft ist eine Liste von Funktionen, die durch Kommas getrennt sind und lokal installiert werden sollen.
ms.assetid: d408986d-7889-4fd9-8202-1d2e59673a2f
title: ADDLOCAL (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9618389d6e409829dce1eb7bb3a38c1269a2e06d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372761"
---
# <a name="addlocal-property"></a><span data-ttu-id="2a278-103">ADDLOCAL (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="2a278-103">ADDLOCAL property</span></span>

<span data-ttu-id="2a278-104">Der Wert der **ADDLOCAL** -Eigenschaft ist eine Liste von Funktionen, die durch Kommas getrennt sind und lokal installiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="2a278-104">The value of the **ADDLOCAL** property is a list of features that are delimited by commas, and are to be installed locally.</span></span> <span data-ttu-id="2a278-105">Die Funktionen müssen in der featurespalte der [Funktions Tabelle](feature-table.md)vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="2a278-105">The features must be present in the Feature column of the [Feature Table](feature-table.md).</span></span> <span data-ttu-id="2a278-106">Wenn Sie alle Features lokal installieren möchten, verwenden Sie ADDLOCAL = all in der Befehlszeile.</span><span class="sxs-lookup"><span data-stu-id="2a278-106">To install all features locally, use ADDLOCAL=ALL on the command line.</span></span> <span data-ttu-id="2a278-107">Geben Sie ADDLOCAL = ALL nicht in die [Eigenschaften Tabelle](property-table.md)ein, da dadurch ein lokal installiertes Paket generiert wird, das nicht ordnungsgemäß entfernt werden kann.</span><span class="sxs-lookup"><span data-stu-id="2a278-107">Do not enter ADDLOCAL=ALL into the [Property Table](property-table.md), because this generates a locally installed package that cannot be correctly removed.</span></span>

## <a name="remarks"></a><span data-ttu-id="2a278-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2a278-108">Remarks</span></span>

<span data-ttu-id="2a278-109">Bei Funktionsnamen wird die Groß-/Kleinschreibung</span><span class="sxs-lookup"><span data-stu-id="2a278-109">Feature names are case sensitive.</span></span> <span data-ttu-id="2a278-110">Wenn das sourceOnly-Bitflag in der Spalte Attribute der [Komponenten Tabelle](component-table.md) für eine Komponente eines Features in der Liste festgelegt ist, wird diese Komponente als aus Quelle ausgeführt installiert.</span><span class="sxs-lookup"><span data-stu-id="2a278-110">If the SourceOnly bit flag is set in the Attributes column of the [Component Table](component-table.md) for a component of a feature in the list, that component is installed as run from source.</span></span>

<span data-ttu-id="2a278-111">Das Installationsprogramm wertet die folgenden Eigenschaften immer in der folgenden Reihenfolge aus:</span><span class="sxs-lookup"><span data-stu-id="2a278-111">The installer always evaluates the following properties in the following order:</span></span>

1.  <span data-ttu-id="2a278-112">**ADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="2a278-112">**ADDLOCAL**</span></span>
2.  [<span data-ttu-id="2a278-113">**Aufgeh**</span><span class="sxs-lookup"><span data-stu-id="2a278-113">**REMOVE**</span></span>](remove.md)
3.  [<span data-ttu-id="2a278-114">**Addsource**</span><span class="sxs-lookup"><span data-stu-id="2a278-114">**ADDSOURCE**</span></span>](addsource.md)
4.  [<span data-ttu-id="2a278-115">**Adddefault**</span><span class="sxs-lookup"><span data-stu-id="2a278-115">**ADDDEFAULT**</span></span>](adddefault.md)
5.  [<span data-ttu-id="2a278-116">**Installieren Sie**</span><span class="sxs-lookup"><span data-stu-id="2a278-116">**REINSTALL**</span></span>](reinstall.md)
6.  [<span data-ttu-id="2a278-117">**Benen**</span><span class="sxs-lookup"><span data-stu-id="2a278-117">**ADVERTISE**</span></span>](advertise.md)
7.  [<span data-ttu-id="2a278-118">**Compaddlocal**</span><span class="sxs-lookup"><span data-stu-id="2a278-118">**COMPADDLOCAL**</span></span>](compaddlocal.md)
8.  [<span data-ttu-id="2a278-119">**Compaddsource**</span><span class="sxs-lookup"><span data-stu-id="2a278-119">**COMPADDSOURCE**</span></span>](compaddsource.md)
9.  [<span data-ttu-id="2a278-120">**Compadddefault**</span><span class="sxs-lookup"><span data-stu-id="2a278-120">**COMPADDDEFAULT**</span></span>](compadddefault.md)
10. [<span data-ttu-id="2a278-121">**Fileaddlocal**</span><span class="sxs-lookup"><span data-stu-id="2a278-121">**FILEADDLOCAL**</span></span>](fileaddlocal.md)
11. [<span data-ttu-id="2a278-122">**Fileaddsource**</span><span class="sxs-lookup"><span data-stu-id="2a278-122">**FILEADDSOURCE**</span></span>](fileaddsource.md)
12. [<span data-ttu-id="2a278-123">**Fileadddefault**</span><span class="sxs-lookup"><span data-stu-id="2a278-123">**FILEADDDEFAULT**</span></span>](fileadddefault.md)

<span data-ttu-id="2a278-124">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="2a278-124">For example:</span></span>

-   <span data-ttu-id="2a278-125">Wenn in der Befehlszeile Folgendes angegeben wird: ADDLOCAL = ALL, addsource = **myfeature**, werden alle Features zuerst auf Run-Local festgelegt, und **myfeature** wird auf Run-From-Source festgelegt.</span><span class="sxs-lookup"><span data-stu-id="2a278-125">If the command line specifies: ADDLOCAL=ALL, ADDSOURCE = **MyFeature**, all the features are first set to run-local and then **MyFeature** is set to run-from-source.</span></span>
-   <span data-ttu-id="2a278-126">Wenn die Befehlszeile "ADDSOURCE = ALL", "ADDLOCAL =**myfeature**" lautet, ist "First **myfeature** " auf "Run-local" festgelegt, und wenn "ADDSOURCE = ALL" ausgewertet wird, werden alle Funktionen (einschließlich " **myfeature**") auf "Run-From-Source" zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="2a278-126">If the command line is: ADDSOURCE=ALL, ADDLOCAL=**MyFeature**, first **MyFeature** is set to run-local, and then when ADDSOURCE=ALL is evaluated, all features (including **MyFeature**) are reset to run-from-source.</span></span>

<span data-ttu-id="2a278-127">Der Installer legt die [**vorab ausgewählte**](preselected.md) Eigenschaft während der Wiederaufnahme einer angehaltenen Installation auf den Wert "1" fest, oder wenn eine der vorherigen Eigenschaften in der Befehlszeile angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="2a278-127">The installer sets the [**Preselected**](preselected.md) Property to a value of "1" during the resumption of a suspended installation, or when any of the previous properties are specified on the command line.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a278-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2a278-128">Requirements</span></span>



| <span data-ttu-id="2a278-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2a278-129">Requirement</span></span> | <span data-ttu-id="2a278-130">Wert</span><span class="sxs-lookup"><span data-stu-id="2a278-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a278-131">Version</span><span class="sxs-lookup"><span data-stu-id="2a278-131">Version</span></span><br/> | <span data-ttu-id="2a278-132">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="2a278-132">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="2a278-133">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="2a278-133">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="2a278-134">Windows Installer unter Windows Server 2003 oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="2a278-134">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="2a278-135">Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="2a278-135">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2a278-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2a278-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a278-137">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2a278-137">Properties</span></span>](properties.md)
</dt> </dl>

 

 




