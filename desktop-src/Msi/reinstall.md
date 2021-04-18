---
description: Der Wert der Eigenschaft neu installieren ist eine Liste von Funktionen, die durch Kommas getrennt sind, die neu installiert werden sollen. Die aufgeführten Features müssen in der featurespalte der Funktions Tabelle vorhanden sein. Verwenden Sie zum erneuten Installieren aller Features installieren Sie = all in der Befehlszeile.
ms.assetid: 14346fef-7923-4f30-bca8-96a29c0f820d
title: Eigenschaft neu installieren
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5147b4120968991aa3cb6caf438b7565281fc6f7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357694"
---
# <a name="reinstall-property"></a><span data-ttu-id="cfb3b-105">Eigenschaft neu installieren</span><span class="sxs-lookup"><span data-stu-id="cfb3b-105">REINSTALL property</span></span>

<span data-ttu-id="cfb3b-106">Der Wert der Eigenschaft **neu installieren** ist eine Liste von Funktionen, die durch Kommas getrennt sind, die neu installiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="cfb3b-106">The value of the **REINSTALL** property is a list of features delimited by commas that are to be reinstalled.</span></span> <span data-ttu-id="cfb3b-107">Die aufgeführten Features müssen in der featurespalte der [Funktions](feature-table.md) Tabelle vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="cfb3b-107">The features listed must be present in the Feature column of the [Feature](feature-table.md) table.</span></span> <span data-ttu-id="cfb3b-108">Verwenden Sie zum erneuten Installieren aller Features installieren Sie = all in der Befehlszeile.</span><span class="sxs-lookup"><span data-stu-id="cfb3b-108">To reinstall all features use REINSTALL=ALL on the command line.</span></span>

## <a name="remarks"></a><span data-ttu-id="cfb3b-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cfb3b-109">Remarks</span></span>

<span data-ttu-id="cfb3b-110">Beachten Sie, dass die Funktionsnamen die Groß-/Kleinschreibung beachten.</span><span class="sxs-lookup"><span data-stu-id="cfb3b-110">Note that the feature names are case-sensitive.</span></span>

<span data-ttu-id="cfb3b-111">Wenn die Eigenschaft **neu installieren** festgelegt ist, sollte auch die Eigenschaft [**REINSTALLMODE**](reinstallmode.md) festgelegt werden, um die Art der erneuten Installation anzugeben, die ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="cfb3b-111">If the **REINSTALL** property is set, the [**REINSTALLMODE**](reinstallmode.md) property should also be set, to indicate the type of reinstall to be performed.</span></span> <span data-ttu-id="cfb3b-112">Wenn die Eigenschaft **REINSTALLMODE** nicht festgelegt ist, werden standardmäßig alle Dateien, die derzeit installiert sind, neu installiert, wenn die aktuell installierte Datei eine geringere Version (oder nicht vorhanden) ist.</span><span class="sxs-lookup"><span data-stu-id="cfb3b-112">If the **REINSTALLMODE** property is not set, then by default all files that are currently installed are reinstalled, IF the currently installed file is a lesser version (or is not present).</span></span> <span data-ttu-id="cfb3b-113">Standardmäßig werden keine Registrierungseinträge umgeschrieben.</span><span class="sxs-lookup"><span data-stu-id="cfb3b-113">By default, no registry entries are rewritten.</span></span>

<span data-ttu-id="cfb3b-114">Beachten Sie, dass auch dann, wenn die **Neuinstallation** auf alle festgelegt ist, nur die Features, die bereits zuvor installiert waren, neu installiert werden.</span><span class="sxs-lookup"><span data-stu-id="cfb3b-114">Note that even if **REINSTALL** is set to ALL, only those features that were already installed previously are reinstalled.</span></span> <span data-ttu-id="cfb3b-115">Wenn für ein Produkt, das noch installiert werden soll, die **Neuinstallation** festgelegt ist, wird daher überhaupt keine Installations Aktion durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="cfb3b-115">Thus, if **REINSTALL** is set for a product that is yet to be installed, no installation action will take place at all.</span></span>

<span data-ttu-id="cfb3b-116">Das Installationsprogramm wertet die folgenden Eigenschaften immer in der folgenden Reihenfolge aus:</span><span class="sxs-lookup"><span data-stu-id="cfb3b-116">The installer always evaluates the following properties in the following order:</span></span>

1.  [<span data-ttu-id="cfb3b-117">**ADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="cfb3b-117">**ADDLOCAL**</span></span>](addlocal.md)
2.  [<span data-ttu-id="cfb3b-118">**Aufgeh**</span><span class="sxs-lookup"><span data-stu-id="cfb3b-118">**REMOVE**</span></span>](remove.md)
3.  [<span data-ttu-id="cfb3b-119">**Addsource**</span><span class="sxs-lookup"><span data-stu-id="cfb3b-119">**ADDSOURCE**</span></span>](addsource.md)
4.  [<span data-ttu-id="cfb3b-120">**Adddefault**</span><span class="sxs-lookup"><span data-stu-id="cfb3b-120">**ADDDEFAULT**</span></span>](adddefault.md)
5.  <span data-ttu-id="cfb3b-121">**Installieren Sie**</span><span class="sxs-lookup"><span data-stu-id="cfb3b-121">**REINSTALL**</span></span>
6.  [<span data-ttu-id="cfb3b-122">**Benen**</span><span class="sxs-lookup"><span data-stu-id="cfb3b-122">**ADVERTISE**</span></span>](advertise.md)
7.  [<span data-ttu-id="cfb3b-123">**Compaddlocal**</span><span class="sxs-lookup"><span data-stu-id="cfb3b-123">**COMPADDLOCAL**</span></span>](compaddlocal.md)
8.  [<span data-ttu-id="cfb3b-124">**Compaddsource**</span><span class="sxs-lookup"><span data-stu-id="cfb3b-124">**COMPADDSOURCE**</span></span>](compaddsource.md)
9.  [<span data-ttu-id="cfb3b-125">**Fileaddlocal**</span><span class="sxs-lookup"><span data-stu-id="cfb3b-125">**FILEADDLOCAL**</span></span>](fileaddlocal.md)
10. [<span data-ttu-id="cfb3b-126">**Fileaddsource**</span><span class="sxs-lookup"><span data-stu-id="cfb3b-126">**FILEADDSOURCE**</span></span>](fileaddsource.md)
11. [<span data-ttu-id="cfb3b-127">**Fileadddefault**</span><span class="sxs-lookup"><span data-stu-id="cfb3b-127">**FILEADDDEFAULT**</span></span>](fileadddefault.md)

<span data-ttu-id="cfb3b-128">Wenn die Befehlszeile z. b. Folgendes angibt: ADDLOCAL = ALL, addsource = myfeature, werden alle Features zuerst auf Run-Local festgelegt, und myfeature wird auf Run-From-Source festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cfb3b-128">For example, if the command line specifies: ADDLOCAL=ALL, ADDSOURCE = MyFeature, all the features are first set to run-local and then MyFeature is set to run-from-source.</span></span> <span data-ttu-id="cfb3b-129">Wenn die Befehlszeile "ADDSOURCE = ALL", "ADDLOCAL = myfeature" lautet, ist "First myfeature" auf "Run-local" festgelegt, und wenn "ADDSOURCE = ALL" ausgewertet wird, werden alle Funktionen (einschließlich "myfeature") auf "Run-From-Source" zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="cfb3b-129">If the command line is: ADDSOURCE=ALL, ADDLOCAL=MyFeature, first MyFeature is set to run-local, and then when ADDSOURCE=ALL is evaluated, all features (including MyFeature) are reset to run-from-source.</span></span>

<span data-ttu-id="cfb3b-130">Der Installer legt die [**vorab ausgewählte**](preselected.md) Eigenschaft während der Wiederaufnahme einer angehaltenen Installation auf den Wert "1" fest, oder wenn eine der oben aufgeführten Eigenschaften in der Befehlszeile angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="cfb3b-130">The installer sets the [**Preselected**](preselected.md) property to a value of "1" during the resumption of a suspended installation or when any of the above properties are specified on the command line.</span></span>

## <a name="requirements"></a><span data-ttu-id="cfb3b-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cfb3b-131">Requirements</span></span>



| <span data-ttu-id="cfb3b-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cfb3b-132">Requirement</span></span> | <span data-ttu-id="cfb3b-133">Wert</span><span class="sxs-lookup"><span data-stu-id="cfb3b-133">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cfb3b-134">Version</span><span class="sxs-lookup"><span data-stu-id="cfb3b-134">Version</span></span><br/> | <span data-ttu-id="cfb3b-135">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="cfb3b-135">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="cfb3b-136">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="cfb3b-136">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="cfb3b-137">Windows Installer unter Windows Server 2003 oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="cfb3b-137">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="cfb3b-138">Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="cfb3b-138">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="cfb3b-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cfb3b-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cfb3b-140">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="cfb3b-140">Properties</span></span>](properties.md)
</dt> </dl>

 

 




