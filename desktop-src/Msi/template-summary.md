---
description: Bei einem Installationspaket gibt die Eigenschaft Vorlagen Zusammenfassung die Plattform-und Sprachversionen an, die mit dieser Installations Datenbank kompatibel sind.
ms.assetid: a1015ddb-8d5c-40f7-97ac-4a1347644ae6
title: Vorlagen Zusammenfassungs Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36b3949e7028fd0b1b5f9ff3112f1a3d03c9b87e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373682"
---
# <a name="template-summary-property"></a><span data-ttu-id="0305b-103">Vorlagen Zusammenfassungs Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="0305b-103">Template Summary property</span></span>

<span data-ttu-id="0305b-104">Bei einem Installationspaket gibt die Eigenschaft **Vorlagen Zusammenfassung** die Plattform-und Sprachversionen an, die mit dieser Installations Datenbank kompatibel sind.</span><span class="sxs-lookup"><span data-stu-id="0305b-104">For an installation package, the **Template Summary** property indicates the platform and language versions that are compatible with this installation database.</span></span> <span data-ttu-id="0305b-105">Die Syntax der Eigenschaften Informationen für die **Vorlagen Zusammenfassung** für eine Installations Datenbank lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="0305b-105">The syntax of the **Template Summary** property information for an installation database is the following:</span></span>

<span data-ttu-id="0305b-106">\[*Platt Form Eigenschaft* \] ; \[ *Sprach-ID* \] \[ ,*Sprach-ID* \] \[ ,... \] .</span><span class="sxs-lookup"><span data-stu-id="0305b-106">\[*platform property*\];\[*language id*\]\[,*language id*\]\[,...\].</span></span>

<span data-ttu-id="0305b-107">Die folgenden Beispiele sind gültige Werte für die Eigenschaft **Vorlagen Zusammenfassung** :</span><span class="sxs-lookup"><span data-stu-id="0305b-107">The following examples are valid values for the **Template Summary** property:</span></span>

-   <span data-ttu-id="0305b-108">x64; 1033</span><span class="sxs-lookup"><span data-stu-id="0305b-108">x64;1033</span></span>
-   <span data-ttu-id="0305b-109">Intel; 1033</span><span class="sxs-lookup"><span data-stu-id="0305b-109">Intel;1033</span></span>
-   <span data-ttu-id="0305b-110">Intel64; 1033</span><span class="sxs-lookup"><span data-stu-id="0305b-110">Intel64;1033</span></span>
-   <span data-ttu-id="0305b-111">; 1033</span><span class="sxs-lookup"><span data-stu-id="0305b-111">;1033</span></span>
-   <span data-ttu-id="0305b-112">Intel; 1033, 2046</span><span class="sxs-lookup"><span data-stu-id="0305b-112">Intel ;1033,2046</span></span>
-   <span data-ttu-id="0305b-113">Intel64; 1033, 2046</span><span class="sxs-lookup"><span data-stu-id="0305b-113">Intel64;1033,2046</span></span>
-   <span data-ttu-id="0305b-114">Intel; 0</span><span class="sxs-lookup"><span data-stu-id="0305b-114">Intel;0</span></span>
-   <span data-ttu-id="0305b-115">Arm; 1033, 2046</span><span class="sxs-lookup"><span data-stu-id="0305b-115">Arm;1033,2046</span></span>
-   <span data-ttu-id="0305b-116">Arm; 0</span><span class="sxs-lookup"><span data-stu-id="0305b-116">Arm;0</span></span>
-   <span data-ttu-id="0305b-117">Arm64; 1033, 2046</span><span class="sxs-lookup"><span data-stu-id="0305b-117">Arm64;1033,2046</span></span>
-   <span data-ttu-id="0305b-118">Arm64; 0</span><span class="sxs-lookup"><span data-stu-id="0305b-118">Arm64;0</span></span>

<span data-ttu-id="0305b-119">Die **Vorlagen Zusammenfassungs** Eigenschaft einer Transformation gibt die Plattform-und Sprachversionen an, die mit der Transformation kompatibel sind.</span><span class="sxs-lookup"><span data-stu-id="0305b-119">The **Template Summary** property of a transform indicates the platform and language versions compatible with the transform.</span></span> <span data-ttu-id="0305b-120">In einer Transformations Datei kann nur eine Sprache angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="0305b-120">In a transform file, only one language may be specified.</span></span> <span data-ttu-id="0305b-121">Die angegebene Plattform und Sprache bestimmen, ob eine Transformation auf eine bestimmte Datenbank angewendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="0305b-121">The specified platform and language determine whether a transform can be applied to a particular database.</span></span> <span data-ttu-id="0305b-122">Die Platform-Eigenschaft und die Language-Eigenschaft können leer gelassen werden, wenn keine Transformations Einschränkung zur Validierung der Transformation erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="0305b-122">The platform property and the language property can be left blank if no transform restriction relies on them to validate the transform.</span></span>

<span data-ttu-id="0305b-123">Die **Vorlagen Zusammenfassungs** Eigenschaft eines Patchpakets ist eine durch Semikolons getrennte Liste der Produktcodes, die den Patch akzeptieren können.</span><span class="sxs-lookup"><span data-stu-id="0305b-123">The **Template Summary** property of a patch package is a semicolon-delimited list of the product codes that can accept the patch.</span></span> <span data-ttu-id="0305b-124">Wenn Sie [Msimsp.exe](msimsp-exe.md) und [Patchwiz.dll](patchwiz-dll.md) verwenden, um das Patchpaket zu generieren, wird diese Liste aus der [TargetImages-Tabelle](targetimages-table-patchwiz-dll-.md) der patcherstellungs-Datei abgerufen.</span><span class="sxs-lookup"><span data-stu-id="0305b-124">If you use [Msimsp.exe](msimsp-exe.md) and [Patchwiz.dll](patchwiz-dll.md) to generate the patch package, this list is obtained from the [TargetImages table](targetimages-table-patchwiz-dll-.md) of the patch creation file.</span></span>

<span data-ttu-id="0305b-125">Diese Zusammenfassungs Eigenschaft ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="0305b-125">This summary property is required.</span></span>

## <a name="remarks"></a><span data-ttu-id="0305b-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0305b-126">Remarks</span></span>

<span data-ttu-id="0305b-127">Wenn die aktuelle Plattform nicht mit einer der in der **Vorlagen Zusammenfassungs** Eigenschaft angegebenen Plattformen identisch ist, wird das Paket vom Installationsprogramm nicht verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="0305b-127">If the current platform does not match one of the platforms specified in the **Template Summary** property then the installer does not process the package.</span></span>

<span data-ttu-id="0305b-128">Wenn die Platt Form Spezifikation im Eigenschafts Wert für die **Vorlagen Zusammenfassung** fehlt, nimmt das Installationsprogramm die Intel-Architektur an.</span><span class="sxs-lookup"><span data-stu-id="0305b-128">If the platform specification is missing in the **Template Summary** property value, the installer assumes the Intel architecture.</span></span>

<span data-ttu-id="0305b-129">Wenn es sich um ein 64-Bit-Windows Installer Paket handelt, das auf einer Itanium-Plattform (Intel64) ausgeführt wird, geben Sie in der Eigenschaft **Vorlagen Zusammenfassung** Intel64 ein.</span><span class="sxs-lookup"><span data-stu-id="0305b-129">If this is a 64-bit Windows Installer package being run on an Intel64 (Itanium) platform, enter Intel64 in the **Template Summary** property.</span></span>

<span data-ttu-id="0305b-130">Wenn es sich um ein 64-Bit-Windows Installer Paket handelt, das auf einer x64-Plattform ausgeführt wird, geben Sie x64 in der Eigenschaft **Vorlagen Zusammenfassung** ein.</span><span class="sxs-lookup"><span data-stu-id="0305b-130">If this is a 64-bit Windows Installer package being run on a x64 platform, enter x64 in the **Template Summary** property.</span></span>

<span data-ttu-id="0305b-131">Wenn es sich um ein 64-Bit-Windows Installer Paket handelt, das auf einer Arm64-Plattform ausgeführt wird, geben Sie in der Eigenschaft **Vorlagen Zusammenfassung** Arm64 ein.</span><span class="sxs-lookup"><span data-stu-id="0305b-131">If this is a 64-bit Windows Installer package being run on an Arm64 platform, enter Arm64 in the **Template Summary** property.</span></span>

<span data-ttu-id="0305b-132">Ein Windows Installer Paket kann nicht als Unterstützung sowohl für Intel64 als auch für x64 gekennzeichnet werden. Beispielsweise ist der Wert für die **Vorlagen Zusammenfassungs** Eigenschaft Intel64, x64 ungültig.</span><span class="sxs-lookup"><span data-stu-id="0305b-132">A Windows Installer package cannot be marked as supporting both Intel64 and x64; for example, the **Template Summary** property value of Intel64,x64 is invalid.</span></span>

<span data-ttu-id="0305b-133">Ein Windows Installer Paket kann nicht als Unterstützung für 32-Bit-und 64-Bit-Plattformen gekennzeichnet werden. Beispielsweise sind **Vorlagen Zusammenfassungs** Eigenschaftswerte wie Intel, x64 oder Intel, Intel64 ungültig.</span><span class="sxs-lookup"><span data-stu-id="0305b-133">A Windows Installer package cannot be marked as supporting both 32-bit and 64-bit platforms; for example, **Template Summary** property values such as Intel,x64 or Intel,Intel64 are invalid.</span></span>

<span data-ttu-id="0305b-134">Wenn Sie im Feld "Sprache-ID" der Eigenschaft " **Vorlagen Zusammenfassung** " den Wert 0 (null) eingeben oder dieses Feld leer gelassen wird, wird angegeben, dass das Paket sprachneutral ist.</span><span class="sxs-lookup"><span data-stu-id="0305b-134">Entering 0 (zero) in the language ID field of the **Template Summary** property, or leaving this field empty, indicates that the package is language neutral.</span></span>

<span data-ttu-id="0305b-135">Wenn dies ein Windows Installer Paket ist, das unter Windows RT ausgeführt wird, geben Sie den Wert Arm in der Eigenschaft **Vorlagen Zusammenfassung** ein.</span><span class="sxs-lookup"><span data-stu-id="0305b-135">If this is a Windows Installer package being run on Windows RT, enter the value Arm in the **Template Summary** property.</span></span>

<span data-ttu-id="0305b-136">Mergemodule sind die einzigen Pakete, die mehrere Sprachen aufweisen können.</span><span class="sxs-lookup"><span data-stu-id="0305b-136">Merge Modules are the only packages that may have multiple languages.</span></span> <span data-ttu-id="0305b-137">In einer quellinstallerdatenbank kann nur eine Sprache angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="0305b-137">Only one language can be specified in a source installer database.</span></span> <span data-ttu-id="0305b-138">Weitere Informationen finden Sie unter [mehrere sprachmergemodule](multiple-language-merge-modules.md).</span><span class="sxs-lookup"><span data-stu-id="0305b-138">For more information, see [Multiple Language Merge Modules](multiple-language-merge-modules.md).</span></span>

<span data-ttu-id="0305b-139">Die Alpha Plattform wird von Windows Installer nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0305b-139">The Alpha platform is not supported by Windows Installer.</span></span>

<span data-ttu-id="0305b-140">**Windows Installer:** Die folgende Syntax wird nicht unterstützt:</span><span class="sxs-lookup"><span data-stu-id="0305b-140">**Windows Installer:** The following syntax is not supported:</span></span>

<span data-ttu-id="0305b-141">\[*Platt Form Eigenschaft* \] \[ ,*Platt Form Eigenschaft* \] \[ ,... \] \[ *Sprach-ID* \] \[ ,*Sprach-ID* \] \[ ,... \] .</span><span class="sxs-lookup"><span data-stu-id="0305b-141">\[*platform property*\]\[,*platform property*\]\[,...\]\[*language id*\]\[,*language id*\]\[,...\].</span></span>

<span data-ttu-id="0305b-142">Die folgenden Beispiele sind keine gültigen Werte für die **Vorlagen Zusammenfassungs** Eigenschaft:</span><span class="sxs-lookup"><span data-stu-id="0305b-142">The following examples are not valid values for the **Template Summary** property:</span></span>

-   <span data-ttu-id="0305b-143">Alpha, Intel; 1033</span><span class="sxs-lookup"><span data-stu-id="0305b-143">Alpha,Intel;1033</span></span>
-   <span data-ttu-id="0305b-144">Intel, Alpha; 1033</span><span class="sxs-lookup"><span data-stu-id="0305b-144">Intel,Alpha;1033</span></span>
-   <span data-ttu-id="0305b-145">Alpha; 1033</span><span class="sxs-lookup"><span data-stu-id="0305b-145">Alpha;1033</span></span>
-   <span data-ttu-id="0305b-146">Alpha; 1033, 2046</span><span class="sxs-lookup"><span data-stu-id="0305b-146">Alpha;1033,2046</span></span>

## <a name="requirements"></a><span data-ttu-id="0305b-147">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0305b-147">Requirements</span></span>



| <span data-ttu-id="0305b-148">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0305b-148">Requirement</span></span> | <span data-ttu-id="0305b-149">Wert</span><span class="sxs-lookup"><span data-stu-id="0305b-149">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0305b-150">Version</span><span class="sxs-lookup"><span data-stu-id="0305b-150">Version</span></span><br/> | <span data-ttu-id="0305b-151">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="0305b-151">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="0305b-152">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="0305b-152">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="0305b-153">Windows Installer unter Windows Server 2003 oder Windows XP</span><span class="sxs-lookup"><span data-stu-id="0305b-153">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0305b-154">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0305b-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0305b-155">Beschreibungen der Zusammenfassungs Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0305b-155">Summary Property Descriptions</span></span>](summary-property-descriptions.md)
</dt> </dl>

 

 




