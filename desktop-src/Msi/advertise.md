---
description: Der Wert der Ankündigungs Eigenschaft ist eine Liste von Funktionen, die durch Kommas getrennt sind, die angekündigt werden sollen.
ms.assetid: ef97f70b-e4bf-4eb3-b643-046a9c348823
title: Ankündigungs Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e768f22f86dacf35009ca0e0e3ef9337ef84ab70
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367697"
---
# <a name="advertise-property"></a><span data-ttu-id="8e271-103">Ankündigungs Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="8e271-103">ADVERTISE property</span></span>

<span data-ttu-id="8e271-104">Der **Wert der Ankündigungs Eigenschaft ist** eine Liste von Funktionen, die durch Kommas getrennt sind, die angekündigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="8e271-104">The value of the **ADVERTISE** property is a list of features delimited by commas that are to be advertised.</span></span> <span data-ttu-id="8e271-105">Die Funktionen müssen in der featurespalte der [Funktions](feature-table.md) Tabelle vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="8e271-105">The features must be present in the Feature column of the [Feature](feature-table.md) table.</span></span> <span data-ttu-id="8e271-106">Wenn Sie alle Features wie angekündigt installieren möchten, verwenden Sie Ankündigungs = alle in der Befehlszeile.</span><span class="sxs-lookup"><span data-stu-id="8e271-106">To install all features as advertised, use ADVERTISE=ALL on the command line.</span></span> <span data-ttu-id="8e271-107">Geben Sie ankündigen = all nicht in die [Eigenschaften Tabelle](property-table.md) ein, da dadurch ein angekündigtes Paket generiert wird, das nicht installiert oder entfernt werden kann.</span><span class="sxs-lookup"><span data-stu-id="8e271-107">Do not enter ADVERTISE=ALL into the [Property table](property-table.md) because this generates an advertised package that cannot be installed or removed.</span></span>

## <a name="remarks"></a><span data-ttu-id="8e271-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8e271-108">Remarks</span></span>

<span data-ttu-id="8e271-109">Beachten Sie, dass bei Funktionsnamen die Groß-/Kleinschreibung beachtet</span><span class="sxs-lookup"><span data-stu-id="8e271-109">Note that feature names are case-sensitive.</span></span>

<span data-ttu-id="8e271-110">Das Installationsprogramm wertet die folgenden Eigenschaften immer in der folgenden Reihenfolge aus:</span><span class="sxs-lookup"><span data-stu-id="8e271-110">The installer always evaluates the following properties in the following order.</span></span>

1.  [<span data-ttu-id="8e271-111">**ADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="8e271-111">**ADDLOCAL**</span></span>](addlocal.md)
2.  [<span data-ttu-id="8e271-112">**Aufgeh**</span><span class="sxs-lookup"><span data-stu-id="8e271-112">**REMOVE**</span></span>](remove.md)
3.  [<span data-ttu-id="8e271-113">**Addsource**</span><span class="sxs-lookup"><span data-stu-id="8e271-113">**ADDSOURCE**</span></span>](addsource.md)
4.  [<span data-ttu-id="8e271-114">**Adddefault**</span><span class="sxs-lookup"><span data-stu-id="8e271-114">**ADDDEFAULT**</span></span>](adddefault.md)
5.  [<span data-ttu-id="8e271-115">**Installieren Sie**</span><span class="sxs-lookup"><span data-stu-id="8e271-115">**REINSTALL**</span></span>](reinstall.md)
6.  <span data-ttu-id="8e271-116">**Benen**</span><span class="sxs-lookup"><span data-stu-id="8e271-116">**ADVERTISE**</span></span>
7.  [<span data-ttu-id="8e271-117">**Compaddlocal**</span><span class="sxs-lookup"><span data-stu-id="8e271-117">**COMPADDLOCAL**</span></span>](compaddlocal.md)
8.  [<span data-ttu-id="8e271-118">**Compaddsource**</span><span class="sxs-lookup"><span data-stu-id="8e271-118">**COMPADDSOURCE**</span></span>](compaddsource.md)
9.  [<span data-ttu-id="8e271-119">**Compadddefault**</span><span class="sxs-lookup"><span data-stu-id="8e271-119">**COMPADDDEFAULT**</span></span>](compadddefault.md)
10. [<span data-ttu-id="8e271-120">**Fileaddlocal**</span><span class="sxs-lookup"><span data-stu-id="8e271-120">**FILEADDLOCAL**</span></span>](fileaddlocal.md)
11. [<span data-ttu-id="8e271-121">**Fileaddsource**</span><span class="sxs-lookup"><span data-stu-id="8e271-121">**FILEADDSOURCE**</span></span>](fileaddsource.md)
12. [<span data-ttu-id="8e271-122">**Fileadddefault**</span><span class="sxs-lookup"><span data-stu-id="8e271-122">**FILEADDDEFAULT**</span></span>](fileadddefault.md)

<span data-ttu-id="8e271-123">Wenn die Befehlszeile z. b. Folgendes angibt: ADDLOCAL = ALL, addsource = myfeature, werden alle Features zuerst auf Run-Local festgelegt, und myfeature wird auf Run-From-Source festgelegt.</span><span class="sxs-lookup"><span data-stu-id="8e271-123">For example, if the command line specifies: ADDLOCAL=ALL, ADDSOURCE = MyFeature, all the features are first set to run-local and then MyFeature is set to run-from-source.</span></span> <span data-ttu-id="8e271-124">Wenn die Befehlszeile "ADDSOURCE = ALL", "ADDLOCAL = myfeature" lautet, ist "First myfeature" auf "Run-local" festgelegt, und wenn "ADDSOURCE = ALL" ausgewertet wird, werden alle Funktionen (einschließlich "myfeature") auf "Run-From-Source" zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="8e271-124">If the command line is: ADDSOURCE=ALL, ADDLOCAL=MyFeature, first MyFeature is set to run-local, and then when ADDSOURCE=ALL is evaluated, all features (including MyFeature) are reset to run-from-source.</span></span>

<span data-ttu-id="8e271-125">Der Installer legt die [**vorab ausgewählte**](preselected.md) Eigenschaft während der Wiederaufnahme einer angehaltenen Installation auf den Wert "1" fest, oder wenn eine der oben aufgeführten Eigenschaften in der Befehlszeile angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="8e271-125">The installer sets the [**Preselected**](preselected.md) property to a value of "1" during the resumption of a suspended installation or when any of the above properties are specified on the command line.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e271-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8e271-126">Requirements</span></span>



| <span data-ttu-id="8e271-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8e271-127">Requirement</span></span> | <span data-ttu-id="8e271-128">Wert</span><span class="sxs-lookup"><span data-stu-id="8e271-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e271-129">Version</span><span class="sxs-lookup"><span data-stu-id="8e271-129">Version</span></span><br/> | <span data-ttu-id="8e271-130">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="8e271-130">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="8e271-131">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="8e271-131">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="8e271-132">Windows Installer unter Windows Server 2003 oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="8e271-132">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="8e271-133">Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="8e271-133">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8e271-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8e271-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e271-135">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8e271-135">Properties</span></span>](properties.md)
</dt> </dl>

 

 




