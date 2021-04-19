---
description: Der Wert der Remove-Eigenschaft ist eine Liste von Funktionen, die durch Kommas getrennt sind, die entfernt werden sollen.
ms.assetid: 39f4609a-7bf8-42b3-b23e-0d6a40b69fd3
title: REMOVE-Eigenschaft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8f46bcd5547abdefd67f98dff312bfdf1dff41e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359788"
---
# <a name="remove-property"></a><span data-ttu-id="5bb27-103">REMOVE-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="5bb27-103">REMOVE property</span></span>

<span data-ttu-id="5bb27-104">Der Wert der **Remove** -Eigenschaft ist eine Liste von Funktionen, die durch Kommas getrennt sind, die entfernt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="5bb27-104">The value of the **REMOVE** property is a list of features delimited by commas that are to be removed.</span></span> <span data-ttu-id="5bb27-105">Die Funktionen müssen in der featurespalte der [Funktions Tabelle](feature-table.md)vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="5bb27-105">The features must be present in the Feature column of the [Feature table](feature-table.md).</span></span> <span data-ttu-id="5bb27-106">Beachten Sie Folgendes: Wenn Sie "Remove = All" in der Befehlszeile verwenden, entfernt das Installationsprogramm alle Features, deren Installations Ebene größer als 0 ist.</span><span class="sxs-lookup"><span data-stu-id="5bb27-106">Note that if you use REMOVE=ALL on the command line, the installer removes all features having an install level greater than 0.</span></span> <span data-ttu-id="5bb27-107">In diesem Fall entfernt das Installationsprogramm keine Features, die den Installations Grad 0 aufweisen.</span><span class="sxs-lookup"><span data-stu-id="5bb27-107">In this case, the installer does not remove features having an install level of 0.</span></span> <span data-ttu-id="5bb27-108">Weitere Informationen zur Installations Ebene der Features finden Sie unter [Featuretabelle](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="5bb27-108">For more information about the install level of features see [Feature table](feature-table.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="5bb27-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5bb27-109">Remarks</span></span>

<span data-ttu-id="5bb27-110">Um zu ermitteln, ob ein Produkt vollständig deinstalliert wurde, kann ein Paket Autor einen bedingten Ausdruck verwenden, um zu überprüfen, ob Remove = All.</span><span class="sxs-lookup"><span data-stu-id="5bb27-110">To determine whether a product has been set to be completely uninstalled, a package author may use a conditional expression to check whether REMOVE=ALL.</span></span> <span data-ttu-id="5bb27-111">Beachten Sie Folgendes: Wenn das Produkt durch Festlegen seines Top-Features auf "Missing" entfernt wird, ist die **Remove** -Eigenschaft möglicherweise erst nach der [InstallValidate-Aktion](installvalidate-action.md)gleich.</span><span class="sxs-lookup"><span data-stu-id="5bb27-111">Note that if the product is removed by setting its top feature to absent, the **REMOVE** property may not equal ALL until after the [InstallValidate action](installvalidate-action.md).</span></span> <span data-ttu-id="5bb27-112">Dies bedeutet, dass alle benutzerdefinierten Aktionen, die von Remove = All abhängen, nach der InstallValidate sequenziert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="5bb27-112">This means that any custom action that depends upon REMOVE=ALL must be sequenced after the InstallValidate.</span></span> <span data-ttu-id="5bb27-113">Weitere Informationen finden Sie auch [im Rahmen](conditioning-actions-to-run-during-removal.md)der Durchsetzung auszuführenden Anlagen Aktionen.</span><span class="sxs-lookup"><span data-stu-id="5bb27-113">For more information see also [Conditioning Actions to Run During Removal](conditioning-actions-to-run-during-removal.md).</span></span> <span data-ttu-id="5bb27-114">Beachten Sie, dass die Funktionsnamen die Groß-/Kleinschreibung beachten.</span><span class="sxs-lookup"><span data-stu-id="5bb27-114">Note that the feature names are case-sensitive.</span></span>

<span data-ttu-id="5bb27-115">Das Installationsprogramm wertet die folgenden Eigenschaften immer in der folgenden Reihenfolge aus:</span><span class="sxs-lookup"><span data-stu-id="5bb27-115">The installer always evaluates the following properties in the following order:</span></span>

1.  [<span data-ttu-id="5bb27-116">**ADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="5bb27-116">**ADDLOCAL**</span></span>](addlocal.md)
2.  <span data-ttu-id="5bb27-117">**Aufgeh**</span><span class="sxs-lookup"><span data-stu-id="5bb27-117">**REMOVE**</span></span>
3.  [<span data-ttu-id="5bb27-118">**Addsource**</span><span class="sxs-lookup"><span data-stu-id="5bb27-118">**ADDSOURCE**</span></span>](addsource.md)
4.  [<span data-ttu-id="5bb27-119">**Adddefault**</span><span class="sxs-lookup"><span data-stu-id="5bb27-119">**ADDDEFAULT**</span></span>](adddefault.md)
5.  [<span data-ttu-id="5bb27-120">**Installieren Sie**</span><span class="sxs-lookup"><span data-stu-id="5bb27-120">**REINSTALL**</span></span>](reinstall.md)
6.  [<span data-ttu-id="5bb27-121">**Benen**</span><span class="sxs-lookup"><span data-stu-id="5bb27-121">**ADVERTISE**</span></span>](advertise.md)
7.  [<span data-ttu-id="5bb27-122">**Compaddlocal**</span><span class="sxs-lookup"><span data-stu-id="5bb27-122">**COMPADDLOCAL**</span></span>](compaddlocal.md)
8.  [<span data-ttu-id="5bb27-123">**Compaddsource**</span><span class="sxs-lookup"><span data-stu-id="5bb27-123">**COMPADDSOURCE**</span></span>](compaddsource.md)
9.  [<span data-ttu-id="5bb27-124">**Compadddefault**</span><span class="sxs-lookup"><span data-stu-id="5bb27-124">**COMPADDDEFAULT**</span></span>](compadddefault.md)
10. [<span data-ttu-id="5bb27-125">**Fileaddlocal**</span><span class="sxs-lookup"><span data-stu-id="5bb27-125">**FILEADDLOCAL**</span></span>](fileaddlocal.md)
11. [<span data-ttu-id="5bb27-126">**Fileaddsource**</span><span class="sxs-lookup"><span data-stu-id="5bb27-126">**FILEADDSOURCE**</span></span>](fileaddsource.md)
12. [<span data-ttu-id="5bb27-127">**Fileadddefault**</span><span class="sxs-lookup"><span data-stu-id="5bb27-127">**FILEADDDEFAULT**</span></span>](fileadddefault.md)

<span data-ttu-id="5bb27-128">Wenn die Befehlszeile z. b. ADDLOCAL = ALL, addsource = myfeature angibt, werden alle Features zuerst auf Run-Local festgelegt, und myfeature wird auf Run-From-Source festgelegt.</span><span class="sxs-lookup"><span data-stu-id="5bb27-128">For example, if the command line specifies ADDLOCAL=ALL, ADDSOURCE = MyFeature, all the features are first set to run-local and then MyFeature is set to run-from-source.</span></span> <span data-ttu-id="5bb27-129">Wenn die Befehlszeile addsource = all, ADDLOCAL = myfeature, First myfeature auf Run-Local festgelegt ist, dann werden bei der Auswertung von addsource = All alle Funktionen (einschließlich myfeature) auf Run-From-Source zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="5bb27-129">If the command line is ADDSOURCE=ALL, ADDLOCAL=MyFeature, first MyFeature is set to run-local, then when ADDSOURCE=ALL is evaluated, all features (including MyFeature) are reset to run-from-source.</span></span>

<span data-ttu-id="5bb27-130">Der Installer legt die [**vorab ausgewählte**](preselected.md) Eigenschaft während der Wiederaufnahme einer angehaltenen Installation auf den Wert "1" fest, oder wenn eine der oben aufgeführten Eigenschaften in der Befehlszeile angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="5bb27-130">The installer sets the [**Preselected**](preselected.md) property to a value of "1" during the resumption of a suspended installation or when any of the above properties are specified on the command line.</span></span>

## <a name="requirements"></a><span data-ttu-id="5bb27-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5bb27-131">Requirements</span></span>



| <span data-ttu-id="5bb27-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5bb27-132">Requirement</span></span> | <span data-ttu-id="5bb27-133">Wert</span><span class="sxs-lookup"><span data-stu-id="5bb27-133">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5bb27-134">Version</span><span class="sxs-lookup"><span data-stu-id="5bb27-134">Version</span></span><br/> | <span data-ttu-id="5bb27-135">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="5bb27-135">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="5bb27-136">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="5bb27-136">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="5bb27-137">Windows Installer unter Windows Server 2003 oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="5bb27-137">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="5bb27-138">Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="5bb27-138">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5bb27-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5bb27-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5bb27-140">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5bb27-140">Properties</span></span>](properties.md)
</dt> </dl>

 

 




