---
description: Der Wert der Eigenschaft adddefault ist eine Liste von Funktionen, die durch Kommas getrennt sind und in der Standardkonfiguration installiert werden sollen.
ms.assetid: 78cec3fc-c653-487a-b41c-a43c42e3a157
title: Adddefault (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43960b6d70d704337f373031ab4972bcb95dada7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372294"
---
# <a name="adddefault-property"></a><span data-ttu-id="76c92-103">Adddefault (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="76c92-103">ADDDEFAULT property</span></span>

<span data-ttu-id="76c92-104">Der Wert der Eigenschaft **adddefault** ist eine Liste von Funktionen, die durch Kommas getrennt sind und in der Standardkonfiguration installiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="76c92-104">The value of the **ADDDEFAULT** property is a list of features delimited by commas, which are to be installed in their default configuration.</span></span> <span data-ttu-id="76c92-105">Die Funktionen müssen in der featurespalte der [Funktions Tabelle](feature-table.md) vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="76c92-105">The features must be present in the Feature column of the [Feature Table.](feature-table.md)</span></span> <span data-ttu-id="76c92-106">Verwenden Sie zum Installieren aller Features in ihren Standardkonfigurationen adddefault = all in der Befehlszeile.</span><span class="sxs-lookup"><span data-stu-id="76c92-106">To install all features in their default configurations, use ADDDEFAULT=ALL on the command line.</span></span>

<span data-ttu-id="76c92-107">Eine Funktion, die in der Eigenschaft **adddefault** aufgeführt ist, wird in demselben Installationsstatus installiert, als ob der Benutzer eine Installation bei Bedarf des Features angefordert hat.</span><span class="sxs-lookup"><span data-stu-id="76c92-107">A feature listed in the **ADDDEFAULT** property is installed in the same installation state as if the user requested an installation-on-demand of the feature.</span></span> <span data-ttu-id="76c92-108">Der Status wird durch die Bits bestimmt, die für die Funktion in der Spalte Attribute der [Featuretabelle](feature-table.md)festgelegt sind, und welche Bits für die Featurekomponenten in der Spalte Attribute der [Komponenten Tabelle](component-table.md)festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="76c92-108">The state is determined by the bits that are set for the feature in the Attributes column of the [Feature Table](feature-table.md), and which bits are set for the feature components in the Attributes column of the [Component Table](component-table.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="76c92-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="76c92-109">Remarks</span></span>

<span data-ttu-id="76c92-110">Bei den Funktionsnamen wird Groß-/Kleinschreibung beachtet.</span><span class="sxs-lookup"><span data-stu-id="76c92-110">The feature names are case sensitive.</span></span>

<span data-ttu-id="76c92-111">Das Installationsprogramm wertet die folgenden Eigenschaften immer in der folgenden Reihenfolge aus:</span><span class="sxs-lookup"><span data-stu-id="76c92-111">The installer always evaluates the following properties in the following order:</span></span>

1.  [<span data-ttu-id="76c92-112">**ADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="76c92-112">**ADDLOCAL**</span></span>](addlocal.md)
2.  [<span data-ttu-id="76c92-113">**Aufgeh**</span><span class="sxs-lookup"><span data-stu-id="76c92-113">**REMOVE**</span></span>](remove.md)
3.  [<span data-ttu-id="76c92-114">**Addsource**</span><span class="sxs-lookup"><span data-stu-id="76c92-114">**ADDSOURCE**</span></span>](addsource.md)
4.  <span data-ttu-id="76c92-115">**Adddefault**</span><span class="sxs-lookup"><span data-stu-id="76c92-115">**ADDDEFAULT**</span></span>
5.  [<span data-ttu-id="76c92-116">**Installieren Sie**</span><span class="sxs-lookup"><span data-stu-id="76c92-116">**REINSTALL**</span></span>](reinstall.md)
6.  [<span data-ttu-id="76c92-117">**Benen**</span><span class="sxs-lookup"><span data-stu-id="76c92-117">**ADVERTISE**</span></span>](advertise.md)
7.  [<span data-ttu-id="76c92-118">**Compaddlocal**</span><span class="sxs-lookup"><span data-stu-id="76c92-118">**COMPADDLOCAL**</span></span>](compaddlocal.md)
8.  [<span data-ttu-id="76c92-119">**Compaddsource**</span><span class="sxs-lookup"><span data-stu-id="76c92-119">**COMPADDSOURCE**</span></span>](compaddsource.md)
9.  [<span data-ttu-id="76c92-120">**Compadddefault**</span><span class="sxs-lookup"><span data-stu-id="76c92-120">**COMPADDDEFAULT**</span></span>](compadddefault.md)
10. [<span data-ttu-id="76c92-121">**Fileaddlocal**</span><span class="sxs-lookup"><span data-stu-id="76c92-121">**FILEADDLOCAL**</span></span>](fileaddlocal.md)
11. [<span data-ttu-id="76c92-122">**Fileaddsource**</span><span class="sxs-lookup"><span data-stu-id="76c92-122">**FILEADDSOURCE**</span></span>](fileaddsource.md)
12. [<span data-ttu-id="76c92-123">**Fileadddefault**</span><span class="sxs-lookup"><span data-stu-id="76c92-123">**FILEADDDEFAULT**</span></span>](fileadddefault.md)

<span data-ttu-id="76c92-124">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="76c92-124">For example:</span></span>

-   <span data-ttu-id="76c92-125">Wenn in der Befehlszeile Folgendes angegeben wird: ADDLOCAL = ALL, addsource = myfeature, werden alle Features zuerst auf Run-Local festgelegt, und **myfeature** wird auf Run-From-Source festgelegt.</span><span class="sxs-lookup"><span data-stu-id="76c92-125">If the command line specifies: ADDLOCAL=ALL, ADDSOURCE = MyFeature, all the features are first set to run-local and then **MyFeature** is set to run-from-source.</span></span>
-   <span data-ttu-id="76c92-126">Wenn die Befehlszeile "ADDSOURCE = ALL", "ADDLOCAL = myfeature" lautet, ist "First **myfeature** " auf "Run-local" festgelegt, und wenn "ADDSOURCE = ALL" ausgewertet wird, werden alle Funktionen (einschließlich " **myfeature**") auf "Run-From-Source" zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="76c92-126">If the command line is: ADDSOURCE=ALL, ADDLOCAL=MyFeature, first **MyFeature** is set to run-local, and then when ADDSOURCE=ALL is evaluated, all features (including **MyFeature**) are reset to run-from-source.</span></span>

<span data-ttu-id="76c92-127">Der Installer legt die [**vorab ausgewählte**](preselected.md) Eigenschaft während der Wiederaufnahme einer angehaltenen Installation auf den Wert "1" fest, oder wenn eine der oben aufgeführten Eigenschaften in der Befehlszeile angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="76c92-127">The installer sets the [**Preselected**](preselected.md) property to a value of "1" during the resumption of a suspended installation, or when any of the above properties are specified on the command line.</span></span>

## <a name="requirements"></a><span data-ttu-id="76c92-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="76c92-128">Requirements</span></span>



| <span data-ttu-id="76c92-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="76c92-129">Requirement</span></span> | <span data-ttu-id="76c92-130">Wert</span><span class="sxs-lookup"><span data-stu-id="76c92-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="76c92-131">Version</span><span class="sxs-lookup"><span data-stu-id="76c92-131">Version</span></span><br/> | <span data-ttu-id="76c92-132">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="76c92-132">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="76c92-133">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="76c92-133">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="76c92-134">Windows Installer unter Windows Server 2003 oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="76c92-134">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="76c92-135">Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="76c92-135">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="76c92-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="76c92-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76c92-137">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="76c92-137">Properties</span></span>](properties.md)
</dt> </dl>

 

 




