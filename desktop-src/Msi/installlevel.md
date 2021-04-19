---
description: Die INSTALLLEVEL-Eigenschaft ist die Anfangsstufe, bei der die Features &\# 0034; auf&\# 0034; standardmäßig für die Installation ausgewählt werden.
ms.assetid: 5051cc46-837a-4446-a54c-4bd4081a424c
title: INSTALLLEVEL-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebc0616fdf49e2c713c65017a202320fa6ea9622
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354185"
---
# <a name="installlevel-property"></a><span data-ttu-id="5607f-103">INSTALLLEVEL-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="5607f-103">INSTALLLEVEL property</span></span>

<span data-ttu-id="5607f-104">Die **INSTALLLEVEL** -Eigenschaft ist die Anfangsstufe, bei der die Features standardmäßig für die Installation ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="5607f-104">The **INSTALLLEVEL** property is the initial level at which features are selected "ON" for installation by default.</span></span> <span data-ttu-id="5607f-105">Eine Funktion wird nur installiert, wenn der Wert im Ebenenfeld der [Funktions Tabelle](feature-table.md) kleiner oder gleich dem aktuellen INSTALLLEVEL-Wert ist.</span><span class="sxs-lookup"><span data-stu-id="5607f-105">A feature is installed only if the value in the Level field of the [Feature table](feature-table.md) is less than or equal to the current INSTALLLEVEL value.</span></span> <span data-ttu-id="5607f-106">Die Installations Ebene für jede Installation wird durch die **INSTALLLEVEL** -Eigenschaft angegeben und kann eine Ganzzahl zwischen 1 und 32.767 sein.</span><span class="sxs-lookup"><span data-stu-id="5607f-106">The installation level for any installation is specified by the **INSTALLLEVEL** property, and can be an integral from 1 to 32,767.</span></span> <span data-ttu-id="5607f-107">Weitere Informationen zu Installations Ebenen finden Sie unter [Feature Table](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="5607f-107">For further discussion of installation levels, see [Feature Table](feature-table.md).</span></span>

## <a name="default-value"></a><span data-ttu-id="5607f-108">Standardwert</span><span class="sxs-lookup"><span data-stu-id="5607f-108">Default Value</span></span>

<span data-ttu-id="5607f-109">Wenn kein Wert angegeben wird, wird für die Installations Ebene der Standardwert 1 verwendet.</span><span class="sxs-lookup"><span data-stu-id="5607f-109">If no value is specified, the install level defaults to 1.</span></span>

## <a name="remarks"></a><span data-ttu-id="5607f-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5607f-110">Remarks</span></span>

<span data-ttu-id="5607f-111">Die von der **INSTALLLEVEL** -Eigenschaft angegebene Installations Ebene kann durch die folgenden Eigenschaften überschrieben werden:</span><span class="sxs-lookup"><span data-stu-id="5607f-111">The installation level specified by the **INSTALLLEVEL** property can be overridden by the following properties:</span></span>

-   [<span data-ttu-id="5607f-112">**ADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="5607f-112">**ADDLOCAL**</span></span>](addlocal.md)
-   [<span data-ttu-id="5607f-113">**Addsource**</span><span class="sxs-lookup"><span data-stu-id="5607f-113">**ADDSOURCE**</span></span>](addsource.md)
-   [<span data-ttu-id="5607f-114">**Adddefault**</span><span class="sxs-lookup"><span data-stu-id="5607f-114">**ADDDEFAULT**</span></span>](adddefault.md)
-   [<span data-ttu-id="5607f-115">**Compaddlocal**</span><span class="sxs-lookup"><span data-stu-id="5607f-115">**COMPADDLOCAL**</span></span>](compaddlocal.md)
-   [<span data-ttu-id="5607f-116">**Compaddsource**</span><span class="sxs-lookup"><span data-stu-id="5607f-116">**COMPADDSOURCE**</span></span>](compaddsource.md)
-   [<span data-ttu-id="5607f-117">**Fileaddlocal**</span><span class="sxs-lookup"><span data-stu-id="5607f-117">**FILEADDLOCAL**</span></span>](fileaddlocal.md)
-   [<span data-ttu-id="5607f-118">**Fileaddsource**</span><span class="sxs-lookup"><span data-stu-id="5607f-118">**FILEADDSOURCE**</span></span>](fileaddsource.md)
-   [<span data-ttu-id="5607f-119">**Aufgeh**</span><span class="sxs-lookup"><span data-stu-id="5607f-119">**REMOVE**</span></span>](remove.md)
-   [<span data-ttu-id="5607f-120">**Installieren Sie**</span><span class="sxs-lookup"><span data-stu-id="5607f-120">**REINSTALL**</span></span>](reinstall.md)
-   [<span data-ttu-id="5607f-121">**Benen**</span><span class="sxs-lookup"><span data-stu-id="5607f-121">**ADVERTISE**</span></span>](advertise.md)

<span data-ttu-id="5607f-122">Wenn Sie z. b. "ADDLOCAL = ALL" festlegen, werden alle Features unabhängig vom Wert der Eigenschaft " **INSTALLLEVEL** " lokal installiert.</span><span class="sxs-lookup"><span data-stu-id="5607f-122">For example, setting ADDLOCAL=ALL installs all features locally regardless of the value of the **INSTALLLEVEL** property.</span></span> <span data-ttu-id="5607f-123">Wenn der Wert der Spalte Ebene in der [Featuretabelle](feature-table.md) auf 0 festgelegt ist, ist das Feature nicht installiert und wird nicht auf der Benutzeroberfläche angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5607f-123">If the value of the Level column in the [Feature table](feature-table.md) is 0, that feature is not installed and not displayed in the UI.</span></span>

<span data-ttu-id="5607f-124">Ein Administrator kann eine Funktion dauerhaft deaktivieren, indem er eine Anpassungs Transformation anwendet, die in der Spalte Ebene für diese Funktion 0 (null) festlegt.</span><span class="sxs-lookup"><span data-stu-id="5607f-124">An administrator can permanently disable a feature by applying a customization transform that sets a 0 in the Level column for that feature.</span></span> <span data-ttu-id="5607f-125">Die Anwendung der Anpassungs Transformation verhindert die Installation und Anzeige des Features, auch wenn der Benutzer eine vollständige Installation mithilfe der Benutzeroberfläche auswählt oder ADDLOCAL in der Befehlszeile auf alle festgelegt hat.</span><span class="sxs-lookup"><span data-stu-id="5607f-125">The application of the customization transform prevents the installation and display of the feature even if the user selects a complete installation using the UI or by setting ADDLOCAL to ALL on the command line.</span></span> <span data-ttu-id="5607f-126">[Ein Beispiel für eine Anpassungs Transformation](a-customization-transform-example.md)finden Sie hier.</span><span class="sxs-lookup"><span data-stu-id="5607f-126">See [A Customization Transform Example](a-customization-transform-example.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5607f-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5607f-127">Requirements</span></span>



| <span data-ttu-id="5607f-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5607f-128">Requirement</span></span> | <span data-ttu-id="5607f-129">Wert</span><span class="sxs-lookup"><span data-stu-id="5607f-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5607f-130">Version</span><span class="sxs-lookup"><span data-stu-id="5607f-130">Version</span></span><br/> | <span data-ttu-id="5607f-131">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="5607f-131">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="5607f-132">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="5607f-132">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="5607f-133">Windows Installer unter Windows Server 2003 oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="5607f-133">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="5607f-134">Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="5607f-134">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5607f-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5607f-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5607f-136">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5607f-136">Properties</span></span>](properties.md)
</dt> </dl>

 

 




