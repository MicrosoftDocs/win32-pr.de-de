---
description: Ein Anwendungsmanifest ist eine XML-Datei, die die freigegebenen und privaten parallelen Assemblys beschreibt und identifiziert, an die sich eine Anwendung zur Laufzeit binden soll.
ms.assetid: c5016251-db7a-4edc-9be9-3acb03d495f8
title: Anwendungsmanifeste
ms.topic: article
ms.date: 10/08/2020
ms.custom: 19H1
ms.openlocfilehash: 2fb7297310102134dfcacf0e5f0d907fbf3a3e0b
ms.sourcegitcommit: 7eadd92b1da5eb4eab7d516a5a768e7f7fc02d4c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/16/2021
ms.locfileid: "112230247"
---
# <a name="application-manifests"></a><span data-ttu-id="9e398-103">Anwendungsmanifeste</span><span class="sxs-lookup"><span data-stu-id="9e398-103">Application Manifests</span></span>

<span data-ttu-id="9e398-104">Ein Anwendungsmanifest ist eine XML-Datei, die die freigegebenen und privaten parallelen Assemblys beschreibt und identifiziert, an die sich eine Anwendung zur Laufzeit binden soll.</span><span class="sxs-lookup"><span data-stu-id="9e398-104">An application manifest is an XML file that describes and identifies the shared and private side-by-side assemblies that an application should bind to at run time.</span></span> <span data-ttu-id="9e398-105">Dabei sollte es sich um die gleichen Assemblyversionen handeln, die zum Testen der Anwendung verwendet wurden.</span><span class="sxs-lookup"><span data-stu-id="9e398-105">These should be the same assembly versions that were used to test the application.</span></span> <span data-ttu-id="9e398-106">Anwendungsmanifeste können auch Metadaten für private Anwendungsdateien beschreiben.</span><span class="sxs-lookup"><span data-stu-id="9e398-106">Application manifests may also describe metadata for files that are private to the application.</span></span>

<span data-ttu-id="9e398-107">Eine vollständige Liste des XML-Schemas finden Sie unter [Manifestdateischema](manifest-file-schema.md).</span><span class="sxs-lookup"><span data-stu-id="9e398-107">For a complete listing of the XML schema, see [Manifest File Schema](manifest-file-schema.md).</span></span>

<span data-ttu-id="9e398-108">Anwendungsmanifesten verfügen über die folgenden Elemente und Attribute.</span><span class="sxs-lookup"><span data-stu-id="9e398-108">Application manifests have the following elements and attributes.</span></span>

| <span data-ttu-id="9e398-109">Element</span><span class="sxs-lookup"><span data-stu-id="9e398-109">Element</span></span>                               | <span data-ttu-id="9e398-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="9e398-110">Attributes</span></span>                | <span data-ttu-id="9e398-111">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="9e398-111">Required</span></span> |
|---------------------------------------|---------------------------|----------|
| <span data-ttu-id="9e398-112">**Assembly**</span><span class="sxs-lookup"><span data-stu-id="9e398-112">**assembly**</span></span>                          |                           | <span data-ttu-id="9e398-113">Ja</span><span class="sxs-lookup"><span data-stu-id="9e398-113">Yes</span></span>      |
|                                       | <span data-ttu-id="9e398-114">**manifestVersion**</span><span class="sxs-lookup"><span data-stu-id="9e398-114">**manifestVersion**</span></span>       | <span data-ttu-id="9e398-115">Ja</span><span class="sxs-lookup"><span data-stu-id="9e398-115">Yes</span></span>      |
| <span data-ttu-id="9e398-116">**noInherit**</span><span class="sxs-lookup"><span data-stu-id="9e398-116">**noInherit**</span></span>                         |                           | <span data-ttu-id="9e398-117">Nein</span><span class="sxs-lookup"><span data-stu-id="9e398-117">No</span></span>       |
| <span data-ttu-id="9e398-118">**Assemblyidentity**</span><span class="sxs-lookup"><span data-stu-id="9e398-118">**assemblyIdentity**</span></span>                  |                           | <span data-ttu-id="9e398-119">Ja</span><span class="sxs-lookup"><span data-stu-id="9e398-119">Yes</span></span>      |
|                                       | <span data-ttu-id="9e398-120">**type**</span><span class="sxs-lookup"><span data-stu-id="9e398-120">**type**</span></span>                  | <span data-ttu-id="9e398-121">Ja</span><span class="sxs-lookup"><span data-stu-id="9e398-121">Yes</span></span>      |
|                                       | <span data-ttu-id="9e398-122">**name**</span><span class="sxs-lookup"><span data-stu-id="9e398-122">**name**</span></span>                  | <span data-ttu-id="9e398-123">Ja</span><span class="sxs-lookup"><span data-stu-id="9e398-123">Yes</span></span>      |
|                                       | <span data-ttu-id="9e398-124">**language**</span><span class="sxs-lookup"><span data-stu-id="9e398-124">**language**</span></span>              | <span data-ttu-id="9e398-125">Nein</span><span class="sxs-lookup"><span data-stu-id="9e398-125">No</span></span>       |
|                                       | <span data-ttu-id="9e398-126">**processorArchitecture**</span><span class="sxs-lookup"><span data-stu-id="9e398-126">**processorArchitecture**</span></span> | <span data-ttu-id="9e398-127">Nein</span><span class="sxs-lookup"><span data-stu-id="9e398-127">No</span></span>       |
|                                       | <span data-ttu-id="9e398-128">**version**</span><span class="sxs-lookup"><span data-stu-id="9e398-128">**version**</span></span>               | <span data-ttu-id="9e398-129">Ja</span><span class="sxs-lookup"><span data-stu-id="9e398-129">Yes</span></span>      |
|                                       | <span data-ttu-id="9e398-130">**Publickeytoken**</span><span class="sxs-lookup"><span data-stu-id="9e398-130">**publicKeyToken**</span></span>        | <span data-ttu-id="9e398-131">Nein</span><span class="sxs-lookup"><span data-stu-id="9e398-131">No</span></span>       |
| <span data-ttu-id="9e398-132">**Kompatibilität**</span><span class="sxs-lookup"><span data-stu-id="9e398-132">**compatibility**</span></span>                     |                           | <span data-ttu-id="9e398-133">Nein</span><span class="sxs-lookup"><span data-stu-id="9e398-133">No</span></span>       |
| <span data-ttu-id="9e398-134">**application**</span><span class="sxs-lookup"><span data-stu-id="9e398-134">**application**</span></span>                       |                           | <span data-ttu-id="9e398-135">Nein</span><span class="sxs-lookup"><span data-stu-id="9e398-135">No</span></span>       |
| <span data-ttu-id="9e398-136">**supportedOS**</span><span class="sxs-lookup"><span data-stu-id="9e398-136">**supportedOS**</span></span>                       | <span data-ttu-id="9e398-137">**Id**</span><span class="sxs-lookup"><span data-stu-id="9e398-137">**Id**</span></span>                    | <span data-ttu-id="9e398-138">Nein</span><span class="sxs-lookup"><span data-stu-id="9e398-138">No</span></span>       |
| <span data-ttu-id="9e398-139">**maxversiontested**</span><span class="sxs-lookup"><span data-stu-id="9e398-139">**maxversiontested**</span></span>                  | <span data-ttu-id="9e398-140">**Id**</span><span class="sxs-lookup"><span data-stu-id="9e398-140">**Id**</span></span>                    | <span data-ttu-id="9e398-141">Nein</span><span class="sxs-lookup"><span data-stu-id="9e398-141">No</span></span>       |
| <span data-ttu-id="9e398-142">**Abhängigkeit**</span><span class="sxs-lookup"><span data-stu-id="9e398-142">**dependency**</span></span>                        |                           | <span data-ttu-id="9e398-143">Nein</span><span class="sxs-lookup"><span data-stu-id="9e398-143">No</span></span>       |
| <span data-ttu-id="9e398-144">**Dependentassembly**</span><span class="sxs-lookup"><span data-stu-id="9e398-144">**dependentAssembly**</span></span>                 |                           | <span data-ttu-id="9e398-145">Nein</span><span class="sxs-lookup"><span data-stu-id="9e398-145">No</span></span>       |
| <span data-ttu-id="9e398-146">**datei**</span><span class="sxs-lookup"><span data-stu-id="9e398-146">**file**</span></span>                              |                           | <span data-ttu-id="9e398-147">Nein</span><span class="sxs-lookup"><span data-stu-id="9e398-147">No</span></span>       |
|                                       | <span data-ttu-id="9e398-148">**name**</span><span class="sxs-lookup"><span data-stu-id="9e398-148">**name**</span></span>                  | <span data-ttu-id="9e398-149">Nein</span><span class="sxs-lookup"><span data-stu-id="9e398-149">No</span></span>       |
|                                       | <span data-ttu-id="9e398-150">**Hashalg**</span><span class="sxs-lookup"><span data-stu-id="9e398-150">**hashalg**</span></span>               | <span data-ttu-id="9e398-151">Nein</span><span class="sxs-lookup"><span data-stu-id="9e398-151">No</span></span>       |
|                                       | <span data-ttu-id="9e398-152">**hash**</span><span class="sxs-lookup"><span data-stu-id="9e398-152">**hash**</span></span>                  | <span data-ttu-id="9e398-153">Nein</span><span class="sxs-lookup"><span data-stu-id="9e398-153">No</span></span>       |
| <span data-ttu-id="9e398-154">**activeCodePage**</span><span class="sxs-lookup"><span data-stu-id="9e398-154">**activeCodePage**</span></span>                    |                           | <span data-ttu-id="9e398-155">Nein</span><span class="sxs-lookup"><span data-stu-id="9e398-155">No</span></span>       |
| <span data-ttu-id="9e398-156">**autoElevate**</span><span class="sxs-lookup"><span data-stu-id="9e398-156">**autoElevate**</span></span>                       |                           | <span data-ttu-id="9e398-157">Nein</span><span class="sxs-lookup"><span data-stu-id="9e398-157">No</span></span>       |
| <span data-ttu-id="9e398-158">**disableTheming**</span><span class="sxs-lookup"><span data-stu-id="9e398-158">**disableTheming**</span></span>                    |                           | <span data-ttu-id="9e398-159">Nein</span><span class="sxs-lookup"><span data-stu-id="9e398-159">No</span></span>       |
| <span data-ttu-id="9e398-160">**disableWindowFiltering**</span><span class="sxs-lookup"><span data-stu-id="9e398-160">**disableWindowFiltering**</span></span>            |                           | <span data-ttu-id="9e398-161">Nein</span><span class="sxs-lookup"><span data-stu-id="9e398-161">No</span></span>       |
| <span data-ttu-id="9e398-162">**dpiAware**</span><span class="sxs-lookup"><span data-stu-id="9e398-162">**dpiAware**</span></span>                          |                           | <span data-ttu-id="9e398-163">Nein</span><span class="sxs-lookup"><span data-stu-id="9e398-163">No</span></span>       |
| <span data-ttu-id="9e398-164">**dpiAwareness**</span><span class="sxs-lookup"><span data-stu-id="9e398-164">**dpiAwareness**</span></span>                      |                           | <span data-ttu-id="9e398-165">Nein</span><span class="sxs-lookup"><span data-stu-id="9e398-165">No</span></span>       |
| <span data-ttu-id="9e398-166">**gdiScaling**</span><span class="sxs-lookup"><span data-stu-id="9e398-166">**gdiScaling**</span></span>                        |                           | <span data-ttu-id="9e398-167">Nein</span><span class="sxs-lookup"><span data-stu-id="9e398-167">No</span></span>       |
| <span data-ttu-id="9e398-168">**highResolutionScrollingAware**</span><span class="sxs-lookup"><span data-stu-id="9e398-168">**highResolutionScrollingAware**</span></span>      |                           | <span data-ttu-id="9e398-169">Nein</span><span class="sxs-lookup"><span data-stu-id="9e398-169">No</span></span>       |
| <span data-ttu-id="9e398-170">**longPathAware**</span><span class="sxs-lookup"><span data-stu-id="9e398-170">**longPathAware**</span></span>                     |                           | <span data-ttu-id="9e398-171">Nein</span><span class="sxs-lookup"><span data-stu-id="9e398-171">No</span></span>       |
| <span data-ttu-id="9e398-172">**printerDriverIsolation**</span><span class="sxs-lookup"><span data-stu-id="9e398-172">**printerDriverIsolation**</span></span>            |                           | <span data-ttu-id="9e398-173">Nein</span><span class="sxs-lookup"><span data-stu-id="9e398-173">No</span></span>       |
| <span data-ttu-id="9e398-174">**ultraHighResolutionScrollingAware**</span><span class="sxs-lookup"><span data-stu-id="9e398-174">**ultraHighResolutionScrollingAware**</span></span> |                           | <span data-ttu-id="9e398-175">Nein</span><span class="sxs-lookup"><span data-stu-id="9e398-175">No</span></span>       |
| <span data-ttu-id="9e398-176">**msix**</span><span class="sxs-lookup"><span data-stu-id="9e398-176">**msix**</span></span>                              |                           | <span data-ttu-id="9e398-177">Nein</span><span class="sxs-lookup"><span data-stu-id="9e398-177">No</span></span>       |
| <span data-ttu-id="9e398-178">**heapType**</span><span class="sxs-lookup"><span data-stu-id="9e398-178">**heapType**</span></span>                          |                           | <span data-ttu-id="9e398-179">Nein</span><span class="sxs-lookup"><span data-stu-id="9e398-179">No</span></span>       |

## <a name="file-location"></a><span data-ttu-id="9e398-180">Dateispeicherort</span><span class="sxs-lookup"><span data-stu-id="9e398-180">File Location</span></span>

<span data-ttu-id="9e398-181">Anwendungsmanifeste sollten als Ressource in der EXE-Datei oder DLL der Anwendung enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="9e398-181">Application manifests should be included as a resource in the application's EXE file or DLL.</span></span>

<span data-ttu-id="9e398-182">Weitere Informationen finden Sie unter [Installieren von nebenseitigen Assemblys.](installing-side-by-side-assemblies.md)</span><span class="sxs-lookup"><span data-stu-id="9e398-182">For more information, see [Installing Side-by-side Assemblies](installing-side-by-side-assemblies.md).</span></span>

## <a name="file-name-syntax"></a><span data-ttu-id="9e398-183">Dateinamensyntax</span><span class="sxs-lookup"><span data-stu-id="9e398-183">File Name Syntax</span></span>

<span data-ttu-id="9e398-184">Der Name einer Anwendungsmanifestdatei ist der Name der ausführbaren Datei der Anwendung gefolgt von .manifest.</span><span class="sxs-lookup"><span data-stu-id="9e398-184">The name of an application manifest file is the name of the application's executable followed by .manifest.</span></span>

<span data-ttu-id="9e398-185">Beispielsweise würde ein Anwendungsmanifest, das auf example.exe oder example.dll, die folgende Dateinamensyntax verwenden.</span><span class="sxs-lookup"><span data-stu-id="9e398-185">For example, an application manifest that refers to example.exe or example.dll would use the following file name syntax.</span></span> <span data-ttu-id="9e398-186">Sie können die Ressourcen-ID <*Felds>,* wenn die Ressourcen-ID 1 ist.</span><span class="sxs-lookup"><span data-stu-id="9e398-186">You can omit the <*resource ID*> field if resource ID is 1.</span></span>

<span data-ttu-id="9e398-187">\***example.exe.<-Ressourcen-ID\*>.manifest**</span><span class="sxs-lookup"><span data-stu-id="9e398-187">**example.exe.<*resource ID*>.manifest**</span></span>

<span data-ttu-id="9e398-188">\***example.dll.<-Ressourcen-ID\*>.manifest**</span><span class="sxs-lookup"><span data-stu-id="9e398-188">**example.dll.<*resource ID*>.manifest**</span></span>

## <a name="elements"></a><span data-ttu-id="9e398-189">Elemente</span><span class="sxs-lookup"><span data-stu-id="9e398-189">Elements</span></span>

<span data-ttu-id="9e398-190">Bei Namen von Elementen und Attributen wird die Kleinschreibung beachtet.</span><span class="sxs-lookup"><span data-stu-id="9e398-190">Names of elements and attributes are case-sensitive.</span></span> <span data-ttu-id="9e398-191">Bei den Werten von Elementen und Attributen wird die Groß-/Kleinschreibung nicht beachtet, mit Ausnahme des Werts des Typattributs.</span><span class="sxs-lookup"><span data-stu-id="9e398-191">The values of elements and attributes are case-insensitive, except for the value of the type attribute.</span></span>

<span id="assembly"></span><span id="ASSEMBLY"></span>

### <a name="assembly"></a><span data-ttu-id="9e398-192">Assembly</span><span class="sxs-lookup"><span data-stu-id="9e398-192">assembly</span></span>

<span data-ttu-id="9e398-193">Ein Containerelement.</span><span class="sxs-lookup"><span data-stu-id="9e398-193">A container element.</span></span> <span data-ttu-id="9e398-194">Das erste Unterelement muss ein **noInherit- oder** **assemblyIdentity-Element** sein.</span><span class="sxs-lookup"><span data-stu-id="9e398-194">Its first subelement must be a **noInherit** or **assemblyIdentity** element.</span></span> <span data-ttu-id="9e398-195">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="9e398-195">Required.</span></span>

<span data-ttu-id="9e398-196">Das **Assemblyelement** muss sich im Namespace "urn:schemas-microsoft-com:asm.v1" befinden.</span><span class="sxs-lookup"><span data-stu-id="9e398-196">The **assembly** element must be in the namespace "urn:schemas-microsoft-com:asm.v1".</span></span> <span data-ttu-id="9e398-197">Untergeordnete Elemente der Assembly müssen sich ebenfalls in diesem Namespace befinden, durch Vererbung oder durch Tagging.</span><span class="sxs-lookup"><span data-stu-id="9e398-197">Child elements of the assembly must also be in this namespace, by inheritance or by tagging.</span></span>

<span data-ttu-id="9e398-198">Das **Assemblyelement** verfügt über die folgenden Attribute.</span><span class="sxs-lookup"><span data-stu-id="9e398-198">The **assembly** element has the following attributes.</span></span>



| <span data-ttu-id="9e398-199">attribute</span><span class="sxs-lookup"><span data-stu-id="9e398-199">Attribute</span></span>           | <span data-ttu-id="9e398-200">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9e398-200">Description</span></span>                                           |
|---------------------|-------------------------------------------------------|
| <span data-ttu-id="9e398-201">**manifestVersion**</span><span class="sxs-lookup"><span data-stu-id="9e398-201">**manifestVersion**</span></span> | <span data-ttu-id="9e398-202">Das **manifestVersion-Attribut** muss auf 1.0 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="9e398-202">The **manifestVersion** attribute must be set to 1.0.</span></span> |


<span id="noInherit"></span><span id="noinherit"></span><span id="NOINHERIT"></span>

### <a name="noinherit"></a><span data-ttu-id="9e398-203">noInherit</span><span class="sxs-lookup"><span data-stu-id="9e398-203">noInherit</span></span>

<span data-ttu-id="9e398-204">Schließen Sie dieses Element in ein Anwendungsmanifest ein, um die [aktivierungskontexte,](activation-contexts.md) die aus dem Manifest generiert werden, mit dem Flag "no inherit" festzulegen.</span><span class="sxs-lookup"><span data-stu-id="9e398-204">Include this element in an application manifest to set the [activation contexts](activation-contexts.md) generated from the manifest with the "no inherit" flag.</span></span> <span data-ttu-id="9e398-205">Wenn dieses Flag nicht in einem Aktivierungskontext festgelegt ist und der Aktivierungskontext aktiv ist, wird es von neuen Threads im gleichen Prozess, fenster, fensterprozeduren und [asynchronen Prozeduraufrufen](/windows/desktop/Sync/asynchronous-procedure-calls)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9e398-205">When this flag is not set in an activation context, and the activation context is active, it is inherited by new threads in the same process, windows, window procedures, and [Asynchronous Procedure Calls](/windows/desktop/Sync/asynchronous-procedure-calls).</span></span> <span data-ttu-id="9e398-206">Durch Festlegen dieses Flags wird verhindert, dass das neue Objekt den aktiven Kontext erbt.</span><span class="sxs-lookup"><span data-stu-id="9e398-206">Setting this flag prevents the new object from inheriting the active context.</span></span>

<span data-ttu-id="9e398-207">Das **noInherit-Element** ist optional und wird in der Regel ausgelassen.</span><span class="sxs-lookup"><span data-stu-id="9e398-207">The **noInherit** element is optional and typically omitted.</span></span> <span data-ttu-id="9e398-208">Die meisten Assemblys funktionieren nicht ordnungsgemäß mithilfe eines Aktivierungskontexts ohne Erben, da die Assembly explizit entworfen werden muss, um die Weitergabe ihres eigenen Aktivierungskontexts zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="9e398-208">Most assemblies do not work correctly using a no-inherit activation context because the assembly must be explicitly designed to manage the propagation of their own activation context.</span></span> <span data-ttu-id="9e398-209">Die Verwendung des **noInherit-Elements** erfordert, dass alle abhängigen Assemblys, auf die vom Anwendungsmanifest verwiesen wird, über ein **noInherit-Element** im [Assemblymanifest verfügen.](assembly-manifests.md)</span><span class="sxs-lookup"><span data-stu-id="9e398-209">The use of the **noInherit** element requires that any dependent assemblies referenced by the application manifest have a **noInherit** element in their [assembly manifest](assembly-manifests.md).</span></span>

<span data-ttu-id="9e398-210">Wenn **noInherit** in einem Manifest verwendet wird, muss es das erste Unterelement des **Assemblyelements** sein.</span><span class="sxs-lookup"><span data-stu-id="9e398-210">If **noInherit** is used in a manifest, it must be the first subelement of the **assembly** element.</span></span> <span data-ttu-id="9e398-211">Das **assemblyIdentity-Element** sollte unmittelbar nach dem **noInherit-Element** vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="9e398-211">The **assemblyIdentity** element should come immediately after the **noInherit** element.</span></span> <span data-ttu-id="9e398-212">Wenn **noInherit** nicht verwendet wird, muss **assemblyIdentity** das erste Unterelement des **Assemblyelements** sein.</span><span class="sxs-lookup"><span data-stu-id="9e398-212">If **noInherit** is not used, **assemblyIdentity** must be the first subelement of the **assembly** element.</span></span> <span data-ttu-id="9e398-213">Das **noInherit-Element** verfügt über keine untergeordneten Elemente.</span><span class="sxs-lookup"><span data-stu-id="9e398-213">The **noInherit** element has no child elements.</span></span> <span data-ttu-id="9e398-214">Es ist kein gültiges Element in [Assemblymanifesten.](assembly-manifests.md)</span><span class="sxs-lookup"><span data-stu-id="9e398-214">It is not a valid element in [assembly manifests](assembly-manifests.md).</span></span>

<span id="assemblyIdentity"></span><span id="assemblyidentity"></span><span id="ASSEMBLYIDENTITY"></span>

### <a name="assemblyidentity"></a><span data-ttu-id="9e398-215">assemblyIdentity</span><span class="sxs-lookup"><span data-stu-id="9e398-215">assemblyIdentity</span></span>

<span data-ttu-id="9e398-216">Als erstes Unterelement eines **Assemblyelements** beschreibt **assemblyIdentity** die Anwendung, die dieses Anwendungsmanifest besitzt, und identifiziert sie eindeutig.</span><span class="sxs-lookup"><span data-stu-id="9e398-216">As the first subelement of an **assembly** element, **assemblyIdentity** describes and uniquely identifies the application owning this application manifest.</span></span> <span data-ttu-id="9e398-217">**AssemblyIdentity** beschreibt als erstes Unterelement eines **dependentAssembly-Elements** eine für die Anwendung erforderliche nebenseitige Assembly.</span><span class="sxs-lookup"><span data-stu-id="9e398-217">As the first subelement of a **dependentAssembly** element, **assemblyIdentity** describes a side-by-side assembly required by the application.</span></span> <span data-ttu-id="9e398-218">Beachten Sie, dass jede Assembly, auf die im Anwendungsmanifest verwiesen wird, eine **assemblyIdentity** erfordert, die genau der **assemblyIdentity** im eigenen Assemblymanifest der Assembly entspricht, auf die verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="9e398-218">Note that every assembly referenced in the application manifest requires an **assemblyIdentity** that exactly matches the **assemblyIdentity** in the referenced assembly's own assembly manifest.</span></span>

<span data-ttu-id="9e398-219">Das **assemblyIdentity-Element** verfügt über die folgenden Attribute.</span><span class="sxs-lookup"><span data-stu-id="9e398-219">The **assemblyIdentity** element has the following attributes.</span></span> <span data-ttu-id="9e398-220">Sie verfügt über keine Unterelemente.</span><span class="sxs-lookup"><span data-stu-id="9e398-220">It has no subelements.</span></span>

| <span data-ttu-id="9e398-221">attribute</span><span class="sxs-lookup"><span data-stu-id="9e398-221">Attribute</span></span>                 | <span data-ttu-id="9e398-222">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9e398-222">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e398-223">**type**</span><span class="sxs-lookup"><span data-stu-id="9e398-223">**type**</span></span>                  | <span data-ttu-id="9e398-224">Gibt den Anwendungs- oder Assemblytyp an.</span><span class="sxs-lookup"><span data-stu-id="9e398-224">Specifies the application or assembly type.</span></span> <span data-ttu-id="9e398-225">Der Wert muss Win32 und alle in Kleinbuchstaben sein.</span><span class="sxs-lookup"><span data-stu-id="9e398-225">The value must be Win32 and all in lower case.</span></span> <span data-ttu-id="9e398-226">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="9e398-226">Required.</span></span>                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="9e398-227">**name**</span><span class="sxs-lookup"><span data-stu-id="9e398-227">**name**</span></span>                  | <span data-ttu-id="9e398-228">Benennt die Anwendung oder Assembly eindeutig.</span><span class="sxs-lookup"><span data-stu-id="9e398-228">Uniquely names the application or assembly.</span></span> <span data-ttu-id="9e398-229">Verwenden Sie das folgende Format für den Namen: Organization.Division.Name.</span><span class="sxs-lookup"><span data-stu-id="9e398-229">Use the following format for the name: Organization.Division.Name.</span></span> <span data-ttu-id="9e398-230">Beispiel: Microsoft.Windows.mysampleApp.</span><span class="sxs-lookup"><span data-stu-id="9e398-230">For example Microsoft.Windows.mysampleApp.</span></span> <span data-ttu-id="9e398-231">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="9e398-231">Required.</span></span>                                                                                                                                                                                                                                                               |
| <span data-ttu-id="9e398-232">**language**</span><span class="sxs-lookup"><span data-stu-id="9e398-232">**language**</span></span>              | <span data-ttu-id="9e398-233">Identifiziert die Sprache der Anwendung oder Assembly.</span><span class="sxs-lookup"><span data-stu-id="9e398-233">Identifies the language of the application or assembly.</span></span> <span data-ttu-id="9e398-234">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="9e398-234">Optional.</span></span> <span data-ttu-id="9e398-235">Wenn die Anwendung oder Assembly sprachspezifisch ist, geben Sie den DHTML-Sprachcode an.</span><span class="sxs-lookup"><span data-stu-id="9e398-235">If the application or assembly is language-specific, specify the DHTML language code.</span></span> <span data-ttu-id="9e398-236">In der **assemblyIdentity** einer Anwendung, die für die weltweite Verwendung vorgesehen ist (sprachneutral), wird das Sprachattribut weggelassen.</span><span class="sxs-lookup"><span data-stu-id="9e398-236">In the **assemblyIdentity** of an application intended for worldwide use (language neutral) omit the language attribute.</span></span><br/> <span data-ttu-id="9e398-237">Legen Sie in einer **assemblyIdentity** einer Assembly für die weltweite Verwendung (sprachneutral) den Wert der Sprache auf \* fest.</span><span class="sxs-lookup"><span data-stu-id="9e398-237">In an **assemblyIdentity** of an assembly intended for worldwide use (language neutral) set the value of language to "\*".</span></span><br/> |
| <span data-ttu-id="9e398-238">**processorArchitecture**</span><span class="sxs-lookup"><span data-stu-id="9e398-238">**processorArchitecture**</span></span> | <span data-ttu-id="9e398-239">Gibt den Prozessor an.</span><span class="sxs-lookup"><span data-stu-id="9e398-239">Specifies the processor.</span></span> <span data-ttu-id="9e398-240">Gültige Werte sind `x86`, `amd64`, `arm` und `arm64`.</span><span class="sxs-lookup"><span data-stu-id="9e398-240">Valid values include `x86`, `amd64`, `arm` and `arm64`.</span></span> <span data-ttu-id="9e398-241">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="9e398-241">Optional.</span></span>                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="9e398-242">**version**</span><span class="sxs-lookup"><span data-stu-id="9e398-242">**version**</span></span>               | <span data-ttu-id="9e398-243">Gibt die Anwendungs- oder Assemblyversion an.</span><span class="sxs-lookup"><span data-stu-id="9e398-243">Specifies the application or assembly version.</span></span> <span data-ttu-id="9e398-244">Verwenden Sie das vierteilige Versionsformat: mmmmm.nnnnn.ooooo.apkpp.</span><span class="sxs-lookup"><span data-stu-id="9e398-244">Use the four-part version format: mmmmm.nnnnn.ooooo.ppppp.</span></span> <span data-ttu-id="9e398-245">Jeder teil, der durch Zeiträume getrennt ist, kann 0-65535 einschließlich sein.</span><span class="sxs-lookup"><span data-stu-id="9e398-245">Each of the parts separated by periods can be 0-65535 inclusive.</span></span> <span data-ttu-id="9e398-246">Weitere Informationen finden Sie unter [Assemblyversionen.](assembly-versions.md)</span><span class="sxs-lookup"><span data-stu-id="9e398-246">For more information, see [Assembly Versions](assembly-versions.md).</span></span> <span data-ttu-id="9e398-247">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="9e398-247">Required.</span></span>                                                                                                                                                                        |
| <span data-ttu-id="9e398-248">**Publickeytoken**</span><span class="sxs-lookup"><span data-stu-id="9e398-248">**publicKeyToken**</span></span>        | <span data-ttu-id="9e398-249">Eine Hexadezimalzeichenfolge mit 16 Zeichen, die die letzten 8 Bytes des SHA-1-Hashs des öffentlichen Schlüssels darstellt, unter dem die Anwendung oder Assembly signiert ist.</span><span class="sxs-lookup"><span data-stu-id="9e398-249">A 16-character hexadecimal string representing the last 8 bytes of the SHA-1 hash of the public key under which the application or assembly is signed.</span></span> <span data-ttu-id="9e398-250">Der zum Signieren des Katalogs verwendete öffentliche Schlüssel muss 2048 Bit oder höher sein.</span><span class="sxs-lookup"><span data-stu-id="9e398-250">The public key used to sign the catalog must be 2048 bits or greater.</span></span> <span data-ttu-id="9e398-251">Erforderlich für alle freigegebenen nebeneinander verwendeten Assemblys.</span><span class="sxs-lookup"><span data-stu-id="9e398-251">Required for all shared side-by-side assemblies.</span></span>                                                                                                                                                     |

<span id="compatibility"></span><span id="COMPATIBILITY"></span>

### <a name="compatibility"></a><span data-ttu-id="9e398-252">Kompatibilität</span><span class="sxs-lookup"><span data-stu-id="9e398-252">compatibility</span></span>

<span data-ttu-id="9e398-253">Enthält mindestens eine **Anwendung.**</span><span class="sxs-lookup"><span data-stu-id="9e398-253">Contains at least one **application**.</span></span> <span data-ttu-id="9e398-254">Sie verfügt über keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="9e398-254">It has no attributes.</span></span> <span data-ttu-id="9e398-255">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="9e398-255">Optional.</span></span> <span data-ttu-id="9e398-256">Anwendungsmanifeste ohne Kompatibilitätselement verwenden standardmäßig Windows Vista-Kompatibilität unter Windows 7.</span><span class="sxs-lookup"><span data-stu-id="9e398-256">Application manifests without a compatibility element default to Windows Vista compatibility on Windows 7.</span></span>

<span id="application"></span><span id="APPLICATION"></span>

### <a name="application"></a><span data-ttu-id="9e398-257">application</span><span class="sxs-lookup"><span data-stu-id="9e398-257">application</span></span>

<span data-ttu-id="9e398-258">Enthält mindestens ein **supportedOS-Element.**</span><span class="sxs-lookup"><span data-stu-id="9e398-258">Contains at least one **supportedOS** element.</span></span> <span data-ttu-id="9e398-259">Ab Windows 10 Version 1903 kann es auch ein optionales **maxversiontested-Element** enthalten.</span><span class="sxs-lookup"><span data-stu-id="9e398-259">Starting in Windows 10, version 1903, it can also contain one optional **maxversiontested** element.</span></span> <span data-ttu-id="9e398-260">Sie verfügt über keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="9e398-260">It has no attributes.</span></span> <span data-ttu-id="9e398-261">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="9e398-261">Optional.</span></span>

<span id="supportedOS"></span><span id="supportedos"></span><span id="SUPPORTEDOS"></span>

### <a name="supportedos"></a><span data-ttu-id="9e398-262">supportedOS</span><span class="sxs-lookup"><span data-stu-id="9e398-262">supportedOS</span></span>

<span data-ttu-id="9e398-263">Das **supportedOS-Element** weist das folgende Attribut auf.</span><span class="sxs-lookup"><span data-stu-id="9e398-263">The **supportedOS** element has the following attribute.</span></span> <span data-ttu-id="9e398-264">Sie verfügt über keine Unterelemente.</span><span class="sxs-lookup"><span data-stu-id="9e398-264">It has no subelements.</span></span>

| <span data-ttu-id="9e398-265">attribute</span><span class="sxs-lookup"><span data-stu-id="9e398-265">Attribute</span></span> | <span data-ttu-id="9e398-266">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9e398-266">Description</span></span>   |
|-----------|-----------------------|
| <span data-ttu-id="9e398-267">**Id**</span><span class="sxs-lookup"><span data-stu-id="9e398-267">**Id**</span></span>    | <span data-ttu-id="9e398-268">Legen Sie das Id-Attribut auf **{e2011457-1546-43c5-a5fe-008deee3d3f0}** fest, um die Anwendung mit vista-Funktionalität auszuführen.</span><span class="sxs-lookup"><span data-stu-id="9e398-268">Set the Id attribute to **{e2011457-1546-43c5-a5fe-008deee3d3f0}** to run the application using Vista functionality.</span></span> <span data-ttu-id="9e398-269">Dadurch kann eine Anwendung, die für Windows Vista entwickelt wurde, auf einem späteren Betriebssystem ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="9e398-269">This can enable an application designed for Windows Vista to run on a later operating system.</span></span> <br/> <span data-ttu-id="9e398-270">Legen Sie das Id-Attribut auf **{35138b9a-5d96-4fbd-8e2d-a2440225f93a}** fest, um die Anwendung mithilfe der Windows 7-Funktionalität auszuführen.</span><span class="sxs-lookup"><span data-stu-id="9e398-270">Set the Id attribute to **{35138b9a-5d96-4fbd-8e2d-a2440225f93a}** to run the application using Windows 7 functionality.</span></span><br/> <span data-ttu-id="9e398-271">Anwendungen, die Windows Vista, Windows 7 und Windows 8 Funktionalität unterstützen, erfordern keine separaten Manifeste.</span><span class="sxs-lookup"><span data-stu-id="9e398-271">Applications that support Windows Vista, Windows 7, and Windows 8 functionality do not require separate manifests.</span></span> <span data-ttu-id="9e398-272">Fügen Sie in diesem Fall die GUIDs für alle Windows-Betriebssysteme hinzu.</span><span class="sxs-lookup"><span data-stu-id="9e398-272">In this case, add the GUIDs for all the Windows operating systems.</span></span><br/> <span data-ttu-id="9e398-273">Informationen zum **Id-Attributverhalten** in Windows finden Sie im [Windows 8 und windows Server 2012 Compatibility Cookbook](https://www.microsoft.com/download/details.aspx?id=27416).</span><span class="sxs-lookup"><span data-stu-id="9e398-273">For info about the **Id** attribute behavior in Windows, see the [Windows 8 and Windows Server 2012 Compatibility Cookbook](https://www.microsoft.com/download/details.aspx?id=27416).</span></span><br/> <span data-ttu-id="9e398-274">Die folgenden GUIDs entsprechen den angegebenen Betriebssystemen:</span><span class="sxs-lookup"><span data-stu-id="9e398-274">The following GUIDs correspond with the indicated operating systems:</span></span><br/> <span data-ttu-id="9e398-275">**{8e0f7a12-bfb3-4fe8-b9a5-48fd50a15a9a}** -> Windows 10, Windows Server 2016 und Windows Server 2019</span><span class="sxs-lookup"><span data-stu-id="9e398-275">**{8e0f7a12-bfb3-4fe8-b9a5-48fd50a15a9a}** -> Windows 10, Windows Server 2016 and Windows Server 2019</span></span><br/> <span data-ttu-id="9e398-276">**{1f676c76-80e1-4239-95bb-83d0f6d0da78}** -> Windows 8.1 und Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="9e398-276">**{1f676c76-80e1-4239-95bb-83d0f6d0da78}** -> Windows 8.1 and Windows Server 2012 R2</span></span><br/> <span data-ttu-id="9e398-277">**{4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}** -> Windows 8 und Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9e398-277">**{4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}** -> Windows 8 and Windows Server 2012</span></span><br/> <span data-ttu-id="9e398-278">**{35138b9a-5d96-4fbd-8e2d-a2440225f93a}** -> Windows 7 und Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9e398-278">**{35138b9a-5d96-4fbd-8e2d-a2440225f93a}** -> Windows 7 and Windows Server 2008 R2</span></span><br/> <span data-ttu-id="9e398-279">**{e2011457-1546-43c5-a5fe-008deee3d3f0}** -> Windows Vista und Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9e398-279">**{e2011457-1546-43c5-a5fe-008deee3d3f0}** -> Windows Vista and Windows Server 2008</span></span><br/> <span data-ttu-id="9e398-280">Sie können dies unter Windows 7 oder Windows 8.x testen, indem Sie Ressourcenmonitor (Resmon) ausführen, zur Registerkarte CPU gelangen, mit der rechten Maustaste auf die Spaltenbezeichnungen "Spalte auswählen..." klicken und "Betriebssystemkontext" aktivieren.</span><span class="sxs-lookup"><span data-stu-id="9e398-280">You can test this on Windows 7 or Windows 8.x by running Resource Monitor (resmon), going to the CPU tab, right-clicking on the column labels, "Select Column...", and check "Operating System Context".</span></span> <span data-ttu-id="9e398-281">Auf Windows 8.x finden Sie diese Spalte auch im Task-Manager (taskmgr).</span><span class="sxs-lookup"><span data-stu-id="9e398-281">On Windows 8.x, you can also find this column available in the Task Manager (taskmgr).</span></span> <span data-ttu-id="9e398-282">Der Inhalt der Spalte zeigt den höchsten gefundenen Wert oder "Windows Vista" als Standard an.</span><span class="sxs-lookup"><span data-stu-id="9e398-282">The content of the column shows the highest value found or "Windows Vista" as the default.</span></span> <br/> |

<span id="maxVersionTested"></span><span id="maxversiontested"></span><span id="MAXVERSIONTESTED"></span>

### <a name="maxversiontested"></a><span data-ttu-id="9e398-283">maxversiontested</span><span class="sxs-lookup"><span data-stu-id="9e398-283">maxversiontested</span></span>

<span data-ttu-id="9e398-284">Das **maxversiontested-Element** gibt die Windows-Versionen an, für die die Anwendung getestet wurde, beginnend mit der minimalen Betriebssystemversion, die die Anwendung bis zur maximalen Version unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9e398-284">The **maxversiontested** element specifies the versions of Windows that the application was tested against starting with the minimum OS version the application supports up to the maximum version.</span></span> <span data-ttu-id="9e398-285">Den vollständigen Satz von Versionen finden Sie [hier.](https://developer.microsoft.com/windows/downloads/sdk-archive/)</span><span class="sxs-lookup"><span data-stu-id="9e398-285">The complete set of versions can be found [here](https://developer.microsoft.com/windows/downloads/sdk-archive/).</span></span> <span data-ttu-id="9e398-286">Dies ist für Desktopanwendungen vorgesehen, die [XAML Islands](/windows/apps/desktop/modernize/xaml-islands) verwenden und nicht in einem MSIX-Paket bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="9e398-286">This is intended to be used by desktop applications that use [XAML Islands](/windows/apps/desktop/modernize/xaml-islands) and that are not deployed in an MSIX package.</span></span> <span data-ttu-id="9e398-287">Dieses Element wird in Windows 10 Version 1903 und höher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9e398-287">This element is supported in Windows 10, version 1903, and later versions.</span></span>

<span data-ttu-id="9e398-288">Das **maxversiontested-Element** weist das folgende Attribut auf.</span><span class="sxs-lookup"><span data-stu-id="9e398-288">The **maxversiontested** element has the following attribute.</span></span> <span data-ttu-id="9e398-289">Sie verfügt über keine Unterelemente.</span><span class="sxs-lookup"><span data-stu-id="9e398-289">It has no subelements.</span></span>

| <span data-ttu-id="9e398-290">attribute</span><span class="sxs-lookup"><span data-stu-id="9e398-290">Attribute</span></span> | <span data-ttu-id="9e398-291">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9e398-291">Description</span></span>    |
|-----------|----------------|
| <span data-ttu-id="9e398-292">**Id**</span><span class="sxs-lookup"><span data-stu-id="9e398-292">**Id**</span></span>    | <span data-ttu-id="9e398-293">Legen Sie das Id-Attribut auf eine vierteilige Versionszeichenfolge fest, die die maximale Version von Windows angibt, für die die Anwendung getestet wurde.</span><span class="sxs-lookup"><span data-stu-id="9e398-293">Set the Id attribute to a 4-part version string that specifies the maximum version of Windows that the application was tested against.</span></span> <span data-ttu-id="9e398-294">Beispiel: "10.0.18226.0".</span><span class="sxs-lookup"><span data-stu-id="9e398-294">For example, "10.0.18226.0".</span></span> |

<span id="dependency"></span><span id="DEPENDENCY"></span>

### <a name="dependency"></a><span data-ttu-id="9e398-295">dependency</span><span class="sxs-lookup"><span data-stu-id="9e398-295">dependency</span></span>

<span data-ttu-id="9e398-296">Enthält mindestens eine **dependentAssembly-**.</span><span class="sxs-lookup"><span data-stu-id="9e398-296">Contains at least one **dependentAssembly**.</span></span> <span data-ttu-id="9e398-297">Sie verfügt über keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="9e398-297">It has no attributes.</span></span> <span data-ttu-id="9e398-298">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="9e398-298">Optional.</span></span>

<span id="dependentAssembly"></span><span id="dependentassembly"></span><span id="DEPENDENTASSEMBLY"></span>

### <a name="dependentassembly"></a><span data-ttu-id="9e398-299">dependentAssembly</span><span class="sxs-lookup"><span data-stu-id="9e398-299">dependentAssembly</span></span>

<span data-ttu-id="9e398-300">Das erste Unterelement von **dependentAssembly** muss ein **assemblyIdentity-Element** sein, das eine für die Anwendung erforderliche side-by-side-Assembly beschreibt.</span><span class="sxs-lookup"><span data-stu-id="9e398-300">The first subelement of **dependentAssembly** must be an **assemblyIdentity** element that describes a side-by-side assembly required by the application.</span></span> <span data-ttu-id="9e398-301">Jede **dependentAssembly** muss sich innerhalb genau einer **Abhängigkeit** befinden.</span><span class="sxs-lookup"><span data-stu-id="9e398-301">Every **dependentAssembly** must be inside exactly one **dependency**.</span></span> <span data-ttu-id="9e398-302">Sie verfügt über keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="9e398-302">It has no attributes.</span></span>

<span id="file"></span><span id="FILE"></span>

### <a name="file"></a><span data-ttu-id="9e398-303">file</span><span class="sxs-lookup"><span data-stu-id="9e398-303">file</span></span>

<span data-ttu-id="9e398-304">Gibt Dateien an, die für die Anwendung privat sind.</span><span class="sxs-lookup"><span data-stu-id="9e398-304">Specifies files that are private to the application.</span></span> <span data-ttu-id="9e398-305">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="9e398-305">Optional.</span></span>

<span data-ttu-id="9e398-306">Das **Dateielement** verfügt über die In der folgenden Tabelle gezeigten Attribute.</span><span class="sxs-lookup"><span data-stu-id="9e398-306">The **file** element has the attributes shown in the following table.</span></span>



| <span data-ttu-id="9e398-307">attribute</span><span class="sxs-lookup"><span data-stu-id="9e398-307">Attribute</span></span>   | <span data-ttu-id="9e398-308">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9e398-308">Description</span></span>                                                                                             |
|-------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e398-309">**name**</span><span class="sxs-lookup"><span data-stu-id="9e398-309">**name**</span></span>    | <span data-ttu-id="9e398-310">Der Name der Datei.</span><span class="sxs-lookup"><span data-stu-id="9e398-310">Name of the file.</span></span> <span data-ttu-id="9e398-311">Beispiel: Comctl32.dll.</span><span class="sxs-lookup"><span data-stu-id="9e398-311">For example, Comctl32.dll.</span></span>                                                            |
| <span data-ttu-id="9e398-312">**Hashalg**</span><span class="sxs-lookup"><span data-stu-id="9e398-312">**hashalg**</span></span> | <span data-ttu-id="9e398-313">Algorithmus, der zum Erstellen eines Hashs der Datei verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9e398-313">Algorithm used to create a hash of the file.</span></span> <span data-ttu-id="9e398-314">Dieser Wert sollte SHA1 sein.</span><span class="sxs-lookup"><span data-stu-id="9e398-314">This value should be SHA1.</span></span>                                 |
| <span data-ttu-id="9e398-315">**hash**</span><span class="sxs-lookup"><span data-stu-id="9e398-315">**hash**</span></span>    | <span data-ttu-id="9e398-316">Ein Hash der Datei, auf die anhand des Namens verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="9e398-316">A hash of the file referred to by name.</span></span> <span data-ttu-id="9e398-317">Eine hexadezimale Zeichenfolge der Länge, die vom Hashalgorithmus abhängt.</span><span class="sxs-lookup"><span data-stu-id="9e398-317">A hexadecimal string of length depending on the hash algorithm.</span></span> |

<span id="activeCodePage"></span><span id="activecodepage"></span><span id="ACTIVECODEPAGE"></span>

### <a name="activecodepage"></a><span data-ttu-id="9e398-318">activeCodePage</span><span class="sxs-lookup"><span data-stu-id="9e398-318">activeCodePage</span></span>

<span data-ttu-id="9e398-319">Erzwingen Sie, dass ein Prozess UTF-8 als Prozesscodepage verwendet.</span><span class="sxs-lookup"><span data-stu-id="9e398-319">Force a process to use UTF-8 as the process code page.</span></span>

<span data-ttu-id="9e398-320">**activeCodePage** wurde in Windows Version 1903 (Update vom Mai 2019) hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="9e398-320">**activeCodePage** was added in Windows Version 1903 (May 2019 Update).</span></span> <span data-ttu-id="9e398-321">Sie können diese Eigenschaft deklarieren und in früheren Windows-Builds als Ziel bzw. ausführung verwenden, aber Sie müssen die Erkennung und Konvertierung von Legacycodeseiten wie gewohnt behandeln.</span><span class="sxs-lookup"><span data-stu-id="9e398-321">You can declare this property and target/run on earlier Windows builds, but you must handle legacy code page detection and conversion as usual.</span></span> <span data-ttu-id="9e398-322">Weitere Informationen finden [Sie unter Verwenden der UTF-8-Codepage.](/windows/uwp/design/globalizing/use-utf8-code-page)</span><span class="sxs-lookup"><span data-stu-id="9e398-322">See [Use the UTF-8 code page](/windows/uwp/design/globalizing/use-utf8-code-page) for details.</span></span>

<span data-ttu-id="9e398-323">Dieses Element weist keine Attribute auf.</span><span class="sxs-lookup"><span data-stu-id="9e398-323">This element has no attributes.</span></span> <span data-ttu-id="9e398-324">**UTF-8** ist nur ein gültiger Wert für **das activeCodePage-Element.**</span><span class="sxs-lookup"><span data-stu-id="9e398-324">**UTF-8** is only valid value for **activeCodePage** element.</span></span>

```XML
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
 ...
  <asmv3:application>
    <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2019/WindowsSettings"> 
      <activeCodePage>UTF-8</activeCodePage> 
    </asmv3:windowsSettings>
  </asmv3:application>
 ...
</assembly>
```

<span id="autoElevate"></span><span id="autoelevate"></span><span id="AUTOELEVATE"></span>

### <a name="autoelevate"></a><span data-ttu-id="9e398-325">autoElevate</span><span class="sxs-lookup"><span data-stu-id="9e398-325">autoElevate</span></span>

<span data-ttu-id="9e398-326">Gibt an, ob die automatische Erhöhung von Rechten aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="9e398-326">Specifies whether auto elevate is enabled.</span></span> <span data-ttu-id="9e398-327">**TRUE** gibt an, dass sie aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="9e398-327">**TRUE** indicates that it is enabled.</span></span> <span data-ttu-id="9e398-328">Sie verfügt über keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="9e398-328">It has no attributes.</span></span>

<span id="disableTheming"></span><span id="disabletheming"></span><span id="DISABLETHEMING"></span>

### <a name="disabletheming"></a><span data-ttu-id="9e398-329">disableTheming</span><span class="sxs-lookup"><span data-stu-id="9e398-329">disableTheming</span></span>

<span data-ttu-id="9e398-330">Gibt an, ob das Angeben von Benutzeroberflächenelementen in einem Design deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="9e398-330">Specifies whether giving UI elements a theme is disabled.</span></span> <span data-ttu-id="9e398-331">**TRUE** gibt an, dass deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="9e398-331">**TRUE** indicates disabled.</span></span> <span data-ttu-id="9e398-332">Sie verfügt über keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="9e398-332">It has no attributes.</span></span>

<span id="disableWindowFiltering"></span><span id="disablewindowfiltering"></span><span id="DISABLEWINDOWFILTERING"></span>

### <a name="disablewindowfiltering"></a><span data-ttu-id="9e398-333">disableWindowFiltering</span><span class="sxs-lookup"><span data-stu-id="9e398-333">disableWindowFiltering</span></span>

<span data-ttu-id="9e398-334">Gibt an, ob die Fensterfilterung deaktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="9e398-334">Specifies whether to disable window filtering.</span></span> <span data-ttu-id="9e398-335">**TRUE** deaktiviert die Fensterfilterung, sodass Sie immersive Fenster auf dem Desktop aufzählen können.</span><span class="sxs-lookup"><span data-stu-id="9e398-335">**TRUE** disables window filtering so you can enumerate immersive windows from the desktop.</span></span> <span data-ttu-id="9e398-336">**disableWindowFiltering** wurde in Windows 8 hinzugefügt und weist keine Attribute auf.</span><span class="sxs-lookup"><span data-stu-id="9e398-336">**disableWindowFiltering** was added in Windows 8 and has no attributes.</span></span>

```XML
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
 ...
  <asmv3:application>
    <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2011/WindowsSettings">
      <disableWindowFiltering>true</disableWindowFiltering>
    </asmv3:windowsSettings>
  </asmv3:application>
 ...
</assembly>
```

<span id="dpiAware"></span><span id="dpiaware"></span><span id="DPIAWARE"></span>

### <a name="dpiaware"></a><span data-ttu-id="9e398-337">dpiAware</span><span class="sxs-lookup"><span data-stu-id="9e398-337">dpiAware</span></span>

<span data-ttu-id="9e398-338">Gibt an, ob der aktuelle Prozess Punkt pro Zoll (DPI) erkennt.</span><span class="sxs-lookup"><span data-stu-id="9e398-338">Specifies whether the current process is dots per inch (dpi) aware.</span></span>

<span data-ttu-id="9e398-339">**Windows 10, Version 1607:** Das **dpiAware-Element** wird ignoriert, wenn das **dpiAwareness-Element** vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="9e398-339">**Windows 10, version 1607:** The **dpiAware** element is ignored if the **dpiAwareness** element is present.</span></span> <span data-ttu-id="9e398-340">Sie können beide Elemente in ein Manifest einschließen, wenn Sie ein anderes Verhalten für Windows 10, Version 1607, als für eine frühere Version des Betriebssystems angeben möchten.</span><span class="sxs-lookup"><span data-stu-id="9e398-340">You can include both elements in a manifest if you want to specify a different behavior for Windows 10, version 1607 than for an earlier version of the operating system.</span></span>

<span data-ttu-id="9e398-341">In der folgenden Tabelle wird das Verhalten beschrieben, das sich basierend auf dem Vorhandensein des **dpiAware-Elements** und des darin enthaltenen Texts ergibt.</span><span class="sxs-lookup"><span data-stu-id="9e398-341">The following table describes the behavior that results based upon the presence of the **dpiAware** element and the text that it contains.</span></span> <span data-ttu-id="9e398-342">Beim Text innerhalb des Elements wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="9e398-342">The text within the element is not case-sensitive.</span></span>

| <span data-ttu-id="9e398-343">Status des **dpiAware-Elements**</span><span class="sxs-lookup"><span data-stu-id="9e398-343">State of the **dpiAware** element</span></span> | <span data-ttu-id="9e398-344">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9e398-344">Description</span></span>     |
|-----------------------------------|---------|
| <span data-ttu-id="9e398-345">„Absent“</span><span class="sxs-lookup"><span data-stu-id="9e398-345">Absent</span></span>                            | <span data-ttu-id="9e398-346">Der aktuelle Prozess ist standardmäßig nicht dpi.</span><span class="sxs-lookup"><span data-stu-id="9e398-346">The current process is dpi unaware by default.</span></span> <span data-ttu-id="9e398-347">Sie können diese Einstellung programmgesteuert ändern, indem Sie die [**Funktion SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) oder [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="9e398-347">You can programmatically change this setting by calling the [**SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) or [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) function.</span></span>                                                                                                                                                            |
| <span data-ttu-id="9e398-348">Enthält "true"</span><span class="sxs-lookup"><span data-stu-id="9e398-348">Contains "true"</span></span>                   | <span data-ttu-id="9e398-349">Der aktuelle Prozess ist systemdpi-fähigen.</span><span class="sxs-lookup"><span data-stu-id="9e398-349">The current process is system dpi aware.</span></span>                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="9e398-350">Enthält "false"</span><span class="sxs-lookup"><span data-stu-id="9e398-350">Contains "false"</span></span>                  | <span data-ttu-id="9e398-351">**Windows Vista, Windows 7 und Windows 8:** Das Verhalten ist identisch mit dem, wenn **dpiAware** nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="9e398-351">**Windows Vista, Windows 7 and Windows 8:** The behavior is the same as when the **dpiAware** is absent.</span></span><br/> <span data-ttu-id="9e398-352">**Windows 8.1 und Windows 10:** Der aktuelle Prozess ist nicht dpi-basiert, und Sie können diese Einstellung nicht programmgesteuert ändern, indem Sie die [**Funktion SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) oder [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="9e398-352">**Windows 8.1 and Windows 10:** The current process is dpi unaware, and you cannot programmatically change this setting by calling the [**SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) or [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) function.</span></span><br/> |
| <span data-ttu-id="9e398-353">Enthält "true/pm"</span><span class="sxs-lookup"><span data-stu-id="9e398-353">Contains "true/pm"</span></span>                | <span data-ttu-id="9e398-354">**Windows Vista, Windows 7 und Windows 8:** Der aktuelle Prozess ist systemdpi-fähigen.</span><span class="sxs-lookup"><span data-stu-id="9e398-354">**Windows Vista, Windows 7 and Windows 8:** The current process is system dpi aware.</span></span><br/> <span data-ttu-id="9e398-355">**Windows 8.1 und Windows 10:** Der aktuelle Prozess ist monitorspezifische dpi-fähige Prozesse.</span><span class="sxs-lookup"><span data-stu-id="9e398-355">**Windows 8.1 and Windows 10:** The current process is per-monitor dpi aware.</span></span><br/>                                                                                                                                                                                                          |
| <span data-ttu-id="9e398-356">Enthält "pro Monitor"</span><span class="sxs-lookup"><span data-stu-id="9e398-356">Contains "per monitor"</span></span>            | <span data-ttu-id="9e398-357">**Windows Vista, Windows 7 und Windows 8:** Das Verhalten ist identisch mit dem, wenn **dpiAware** nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="9e398-357">**Windows Vista, Windows 7 and Windows 8:** The behavior is the same as when the **dpiAware** is absent.</span></span><br/> <span data-ttu-id="9e398-358">**Windows 8.1 und Windows 10:** Der aktuelle Prozess ist monitorspezifische dpi-fähige Prozesse.</span><span class="sxs-lookup"><span data-stu-id="9e398-358">**Windows 8.1 and Windows 10:** The current process is per-monitor dpi aware.</span></span><br/>                                                                                                                                                                                      |
| <span data-ttu-id="9e398-359">Enthält eine beliebige andere Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="9e398-359">Contains any other string</span></span>         | <span data-ttu-id="9e398-360">**Windows Vista, Windows 7 und Windows 8:** Das Verhalten ist identisch mit dem, wenn **dpiAware** nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="9e398-360">**Windows Vista, Windows 7 and Windows 8:** The behavior is the same as when the **dpiAware** is absent.</span></span><br/> <span data-ttu-id="9e398-361">**Windows 8.1 und Windows 10:** Der aktuelle Prozess ist nicht dpi-basiert, und Sie können diese Einstellung nicht programmgesteuert ändern, indem Sie die [**Funktion SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) oder [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="9e398-361">**Windows 8.1 and Windows 10:** The current process is dpi unaware, and you cannot programmatically change this setting by calling the [**SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) or [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) function.</span></span><br/> |

<span data-ttu-id="9e398-362">Weitere Informationen zu DPI-Einstellungen finden Sie unter [Vergleich der DPI-Wahrnehmungsebenen.](https://msdn.microsoft.com/library/windows/desktop/mt843498(v=vs.85).aspx(d=robot))</span><span class="sxs-lookup"><span data-stu-id="9e398-362">For more information about dpi awareness settings, see [Comparison of DPI Awareness Levels](https://msdn.microsoft.com/library/windows/desktop/mt843498(v=vs.85).aspx(d=robot)).</span></span>

<span data-ttu-id="9e398-363">**dpiAware** weist keine Attribute auf.</span><span class="sxs-lookup"><span data-stu-id="9e398-363">**dpiAware** has no attributes.</span></span>

```XML
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
 ...
  <asmv3:application>
    <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2005/WindowsSettings">
      <dpiAware>true</dpiAware>
    </asmv3:windowsSettings>
  </asmv3:application>
 ...
</assembly>
```

<span id="dpiAwareness"></span><span id="dpiawareness"></span><span id="DPIAWARENESS"></span>

### <a name="dpiawareness"></a><span data-ttu-id="9e398-364">dpiAwareness</span><span class="sxs-lookup"><span data-stu-id="9e398-364">dpiAwareness</span></span>

<span data-ttu-id="9e398-365">Gibt an, ob der aktuelle Prozess Punkt pro Zoll (DPI) erkennt.</span><span class="sxs-lookup"><span data-stu-id="9e398-365">Specifies whether the current process is dots per inch (dpi) aware.</span></span>

<span data-ttu-id="9e398-366">Die Mindestversion des Betriebssystems, das das **dpiAwareness-Element** unterstützt, ist Windows 10 Version 1607.</span><span class="sxs-lookup"><span data-stu-id="9e398-366">The minimum version of the operating system that supports the **dpiAwareness** element is Windows 10, version 1607.</span></span> <span data-ttu-id="9e398-367">Bei Versionen, die das **dpiAwareness-Element** unterstützen, überschreibt **dpiAwareness** das **dpiAware-Element.**</span><span class="sxs-lookup"><span data-stu-id="9e398-367">For versions that support the **dpiAwareness** element, the **dpiAwareness** overrides the **dpiAware** element.</span></span> <span data-ttu-id="9e398-368">Sie können beide Elemente in ein Manifest einschließen, wenn Sie ein anderes Verhalten für Windows 10, Version 1607, als für eine frühere Version des Betriebssystems angeben möchten.</span><span class="sxs-lookup"><span data-stu-id="9e398-368">You can include both elements in a manifest if you want to specify a different behavior for Windows 10, version 1607 than for an earlier version of the operating system.</span></span>

<span data-ttu-id="9e398-369">Das **dpiAwareness-Element** kann ein einzelnes Element oder eine Liste von durch Trennzeichen getrennten Elementen enthalten.</span><span class="sxs-lookup"><span data-stu-id="9e398-369">The **dpiAwareness** element can contain a single item or a list of comma-separated items.</span></span> <span data-ttu-id="9e398-370">Im letzteren Fall wird das erste (ganz links) Element in der Liste verwendet, das vom Betriebssystem erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="9e398-370">In the latter case, the first (leftmost) item in the list recognized by the operating system is used.</span></span> <span data-ttu-id="9e398-371">Auf diese Weise können Sie unterschiedliche Verhaltensweisen angeben, die in zukünftigen Windows-Betriebssystemversionen unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="9e398-371">In this way, you can specify different behaviors supported in future Windows operating system versions.</span></span>

<span data-ttu-id="9e398-372">In der folgenden Tabelle wird das Verhalten beschrieben, das sich auf grundlage des Vorhandenseins des **dpiAwareness-Elements** und des Texts ergibt, der in seinem am weitesten links erkannten Element enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="9e398-372">The following table describes the behavior that results based upon the presence of the **dpiAwareness** element and the text that it contains in its leftmost recognized item.</span></span> <span data-ttu-id="9e398-373">Beim Text innerhalb des Elements wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="9e398-373">The text within the element is not case-sensitive.</span></span>

| <span data-ttu-id="9e398-374">**dpiAwareness-Elementstatus:**</span><span class="sxs-lookup"><span data-stu-id="9e398-374">**dpiAwareness** element status:</span></span>        | <span data-ttu-id="9e398-375">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9e398-375">Description</span></span>                          |
|-----------------------------------------|-------------------------------------------|
| <span data-ttu-id="9e398-376">Das Element ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="9e398-376">Element is absent</span></span>                       | <span data-ttu-id="9e398-377">Das **dpiAware-Element** gibt an, ob der Prozess dpi-fähigen Ist.</span><span class="sxs-lookup"><span data-stu-id="9e398-377">The **dpiAware** element specifies whether the process is dpi aware.</span></span>                                                                                                                                                                   |
| <span data-ttu-id="9e398-378">Enthält keine erkannten Elemente</span><span class="sxs-lookup"><span data-stu-id="9e398-378">Contains no recognized items</span></span>            | <span data-ttu-id="9e398-379">Der aktuelle Prozess ist standardmäßig nicht dpi.</span><span class="sxs-lookup"><span data-stu-id="9e398-379">The current process is dpi unaware by default.</span></span> <span data-ttu-id="9e398-380">Sie können diese Einstellung programmgesteuert ändern, indem Sie die [**Funktion SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) oder [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="9e398-380">You can programmatically change this setting by calling the [**SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) or [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) function.</span></span> |
| <span data-ttu-id="9e398-381">Das erste erkannte Element ist "system".</span><span class="sxs-lookup"><span data-stu-id="9e398-381">First recognized item is "system"</span></span>       | <span data-ttu-id="9e398-382">Der aktuelle Prozess ist systemdpi-fähigen.</span><span class="sxs-lookup"><span data-stu-id="9e398-382">The current process is system dpi aware.</span></span>                                                                                                                                                                                               |
| <span data-ttu-id="9e398-383">Das erste erkannte Element ist "permonitor".</span><span class="sxs-lookup"><span data-stu-id="9e398-383">First recognized item is "permonitor"</span></span>   | <span data-ttu-id="9e398-384">Der aktuelle Prozess ist monitorspezifische dpi-fähige Prozesse.</span><span class="sxs-lookup"><span data-stu-id="9e398-384">The current process is per-monitor dpi aware.</span></span>                                                                                                                                                                                          |
| <span data-ttu-id="9e398-385">Das erste erkannte Element ist "permonitorv2".</span><span class="sxs-lookup"><span data-stu-id="9e398-385">First recognized item is "permonitorv2"</span></span> | <span data-ttu-id="9e398-386">Im aktuellen Prozess wird der DPI-Kontext pro Monitor-v2 verwendet.</span><span class="sxs-lookup"><span data-stu-id="9e398-386">The current process uses the per-monitor-v2 dpi awareness context.</span></span> <span data-ttu-id="9e398-387">Dieses Element wird nur in Windows 10 Version 1703 oder höher erkannt.</span><span class="sxs-lookup"><span data-stu-id="9e398-387">This item will only be recognized on Windows 10 version 1703 or later.</span></span>                                                                                              |
| <span data-ttu-id="9e398-388">Das erste erkannte Element ist "nicht bekannt".</span><span class="sxs-lookup"><span data-stu-id="9e398-388">First recognized item is "unaware"</span></span>      | <span data-ttu-id="9e398-389">Der aktuelle Prozess ist dpi nicht bekannt.</span><span class="sxs-lookup"><span data-stu-id="9e398-389">The current process is dpi unaware.</span></span> <span data-ttu-id="9e398-390">Sie können diese Einstellung **nicht** programmgesteuert ändern, indem Sie die [**Funktion SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) oder [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="9e398-390">You **cannot** programmatically change this setting by calling the [**SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) or [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) function.</span></span>      |

<span data-ttu-id="9e398-391">Weitere Informationen zu DPI-Einstellungen, die von diesem Element unterstützt werden, finden Sie unter [DPI \_ AWARENESS](/windows/desktop/api/windef/ne-windef-dpi_awareness) und [DPI \_ AWARENESS \_ CONTEXT](/windows/desktop/hidpi/dpi-awareness-context).</span><span class="sxs-lookup"><span data-stu-id="9e398-391">For more information about dpi awareness settings supported by this element, see [DPI\_AWARENESS](/windows/desktop/api/windef/ne-windef-dpi_awareness) and [DPI\_AWARENESS\_CONTEXT](/windows/desktop/hidpi/dpi-awareness-context).</span></span>

<span data-ttu-id="9e398-392">**dpiAwareness** weist keine Attribute auf.</span><span class="sxs-lookup"><span data-stu-id="9e398-392">**dpiAwareness** has no attributes.</span></span>

```XML
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
 ...
  <asmv3:application>
    <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2016/WindowsSettings">
      <dpiAwareness>PerMonitorV2, unaware</dpiAwareness>
    </asmv3:windowsSettings>
  </asmv3:application>
 ...
</assembly>
```

<span id="gdiScaling"></span><span id="gdiscaling"></span><span id="GDISCALING"></span>

### <a name="gdiscaling"></a><span data-ttu-id="9e398-393">gdiScaling</span><span class="sxs-lookup"><span data-stu-id="9e398-393">gdiScaling</span></span>

<span data-ttu-id="9e398-394">Gibt an, ob die GDI-Skalierung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="9e398-394">Specifies whether GDI scaling is enabled.</span></span> <span data-ttu-id="9e398-395">Die Mindestversion des Betriebssystems, das das **gdiScaling-Element** unterstützt, ist Windows 10 Version 1703.</span><span class="sxs-lookup"><span data-stu-id="9e398-395">The minimum version of the operating system that supports the **gdiScaling** element is Windows 10 version 1703.</span></span>

<span data-ttu-id="9e398-396">Das GDI-Framework (Grafikgeräteschnittstelle) kann die DPI-Skalierung auf Primitive und Text pro Monitor anwenden, ohne die Anwendung selbst zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="9e398-396">The GDI (graphics device interface) framework can apply DPI scaling to primitives and text on a per-monitor basis without updates to the application itself.</span></span> <span data-ttu-id="9e398-397">Dies kann nützlich sein, wenn GDI-Anwendungen nicht mehr aktiv aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="9e398-397">This can be useful for GDI applications no longer being actively updated.</span></span>

<span data-ttu-id="9e398-398">Nichtvektorgrafiken (z. B. Bitmaps, Symbole oder Symbolleisten) können von diesem Element nicht skaliert werden.</span><span class="sxs-lookup"><span data-stu-id="9e398-398">Non-vector graphics (such as bitmaps, icons, or toolbars) cannot be scaled by this element.</span></span> <span data-ttu-id="9e398-399">Darüber hinaus können Grafiken und Text, die in Bitmaps angezeigt werden, die dynamisch von Anwendungen erstellt werden, auch nicht von diesem Element skaliert werden.</span><span class="sxs-lookup"><span data-stu-id="9e398-399">In addition, graphics and text appearing within bitmaps dynamically constructed by applications also cannot be scaled by this element.</span></span>

<span data-ttu-id="9e398-400">**TRUE** gibt an, dass dieses Element aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="9e398-400">**TRUE** indicates that this element is enabled.</span></span> <span data-ttu-id="9e398-401">Sie verfügt über keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="9e398-401">It has no attributes.</span></span>


```XML
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
 ...
  <asmv3:application>
    <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2017/WindowsSettings">
      <gdiScaling>true</gdiScaling>
    </asmv3:windowsSettings>
  </asmv3:application>
 ...
</assembly>
```

<span id="highResolutionScrollingAware"></span><span id="highresolutionscrollingaware"></span><span id="HIGHRESOLUTIONSCROLLINGAWARE"></span>

### <a name="highresolutionscrollingaware"></a><span data-ttu-id="9e398-402">highResolutionScrollingAware</span><span class="sxs-lookup"><span data-stu-id="9e398-402">highResolutionScrollingAware</span></span>

<span data-ttu-id="9e398-403">Gibt an, ob bildlauffähiges Scrollen mit hoher Auflösung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="9e398-403">Specifies whether high-resolution-scrolling aware is enabled.</span></span> <span data-ttu-id="9e398-404">**TRUE gibt** an, dass es aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="9e398-404">**TRUE** indicates that it is enabled.</span></span> <span data-ttu-id="9e398-405">Sie verfügt über keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="9e398-405">It has no attributes.</span></span>

<span id="longPathAware"></span><span id="longpathaware"></span><span id="LONGPATHAWARE"></span>

### <a name="longpathaware"></a><span data-ttu-id="9e398-406">longPathAware</span><span class="sxs-lookup"><span data-stu-id="9e398-406">longPathAware</span></span>

<span data-ttu-id="9e398-407">Ermöglicht lange Pfade, die **die** MAX_PATH überschreiten.</span><span class="sxs-lookup"><span data-stu-id="9e398-407">Enables long paths that exceed **MAX_PATH** in length.</span></span> <span data-ttu-id="9e398-408">Dieses Element wird in Windows 10 Version 1607 und höher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9e398-408">This element is supported in Windows 10, version 1607, and later.</span></span> <span data-ttu-id="9e398-409">[hier finden Sie weitere Informationen](../fileio/maximum-file-path-limitation.md)</span><span class="sxs-lookup"><span data-stu-id="9e398-409">For more information, see [this article](../fileio/maximum-file-path-limitation.md).</span></span>

```XML
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
 ...
  <asmv3:application>
    <asmv3:windowsSettings xmlns:ws2="http://schemas.microsoft.com/SMI/2016/WindowsSettings">
      <ws2:longPathAware>true</ws2:longPathAware>
    </asmv3:windowsSettings>
  </asmv3:application>
 ...
</assembly>
```

<span id="printerDriverIsolation"></span><span id="printerdriverisolation"></span><span id="PRINTERDRIVERISOLATION"></span>

### <a name="printerdriverisolation"></a><span data-ttu-id="9e398-410">printerDriverIsolation</span><span class="sxs-lookup"><span data-stu-id="9e398-410">printerDriverIsolation</span></span>

<span data-ttu-id="9e398-411">Gibt an, ob die Druckertreiberisolation aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="9e398-411">Specifies whether printer driver isolation is enabled.</span></span> <span data-ttu-id="9e398-412">**TRUE gibt** an, dass es aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="9e398-412">**TRUE** indicates that it is enabled.</span></span> <span data-ttu-id="9e398-413">Sie verfügt über keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="9e398-413">It has no attributes.</span></span> <span data-ttu-id="9e398-414">Die Druckertreiberisolation verbessert die Zuverlässigkeit des Windows-Druckdiensts, da Druckertreiber in Prozessen ausgeführt werden können, die von dem Prozess getrennt sind, in dem der Druckspooler ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9e398-414">Printer driver isolation improves the reliability of the Windows print service by enabling printer drivers to run in processes that are separate from the process in which the print spooler runs.</span></span> <span data-ttu-id="9e398-415">Die Unterstützung der Druckertreiberisolation wurde in Windows 7 und Windows Server 2008 R2 gestartet.</span><span class="sxs-lookup"><span data-stu-id="9e398-415">Support for printer driver isolation started in Windows 7 and Windows Server 2008 R2.</span></span> <span data-ttu-id="9e398-416">Eine App kann die Druckertreiberisolation in ihrem App-Manifest deklarieren, um sich vom Druckertreiber zu isolieren und die Zuverlässigkeit zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="9e398-416">An app can declare printer driver isolation in its app manifest to isolate itself from the printer driver and improve its reliability.</span></span> <span data-ttu-id="9e398-417">Das heißt, die App stürzt nicht ab, wenn der Druckertreiber einen Fehler hat.</span><span class="sxs-lookup"><span data-stu-id="9e398-417">That is, the app won't crash if the printer driver has an error.</span></span>


```XML
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
 ...
  <asmv3:application>
    <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2011/WindowsSettings">
      <printerDriverIsolation>true</printerDriverIsolation>
    </asmv3:windowsSettings>
  </asmv3:application>
 ...
</assembly>
```

<span id="ultraHighResolutionScrollingAware"></span><span id="ultrahighresolutionscrollingaware"></span><span id="ULTRAHIGHRESOLUTIONSCROLLINGAWARE"></span>

### <a name="ultrahighresolutionscrollingaware"></a><span data-ttu-id="9e398-418">ultraHighResolutionScrollingAware</span><span class="sxs-lookup"><span data-stu-id="9e398-418">ultraHighResolutionScrollingAware</span></span>

<span data-ttu-id="9e398-419">Gibt an, ob bildlauffähiges Ultra-Bildlauf mit hoher Auflösung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="9e398-419">Specifies whether ultra-high-resolution-scrolling aware is enabled.</span></span> <span data-ttu-id="9e398-420">**TRUE gibt** an, dass es aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="9e398-420">**TRUE** indicates that it is enabled.</span></span> <span data-ttu-id="9e398-421">Sie verfügt über keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="9e398-421">It has no attributes.</span></span>

<span id="msix"></span><span id="MSIX"></span>

### <a name="msix"></a><span data-ttu-id="9e398-422">MSIX</span><span class="sxs-lookup"><span data-stu-id="9e398-422">msix</span></span>

<span data-ttu-id="9e398-423">Gibt die Identitätsinformationen eines [MSIX-Sparsepakets für](/windows/apps/desktop/modernize/grant-identity-to-nonpackaged-apps) die aktuelle Anwendung an.</span><span class="sxs-lookup"><span data-stu-id="9e398-423">Specifies the identity info of a [sparse MSIX package](/windows/apps/desktop/modernize/grant-identity-to-nonpackaged-apps) for the current application.</span></span> <span data-ttu-id="9e398-424">Dieses Element wird in Windows 10 Version 2004 und höher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9e398-424">This element is supported in Windows 10, version 2004, and later versions.</span></span>

<span data-ttu-id="9e398-425">Das **msix-Element** muss sich im Namespace `urn:schemas-microsoft-com:msix.v1` befinden.</span><span class="sxs-lookup"><span data-stu-id="9e398-425">The **msix** element must be in the namespace `urn:schemas-microsoft-com:msix.v1`.</span></span> <span data-ttu-id="9e398-426">Sie enthält die in der folgenden Tabelle gezeigten Attribute.</span><span class="sxs-lookup"><span data-stu-id="9e398-426">It has the attributes shown in the following table.</span></span>

| <span data-ttu-id="9e398-427">attribute</span><span class="sxs-lookup"><span data-stu-id="9e398-427">Attribute</span></span>   | <span data-ttu-id="9e398-428">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9e398-428">Description</span></span>                                                                                             |
|-------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e398-429">**publisher**</span><span class="sxs-lookup"><span data-stu-id="9e398-429">**publisher**</span></span>    | <span data-ttu-id="9e398-430">Beschreibt die Herausgeberinformationen.</span><span class="sxs-lookup"><span data-stu-id="9e398-430">Describes the publisher information.</span></span> <span data-ttu-id="9e398-431">Dieser Wert muss mit dem **Publisher-Attribut** im [Identity-Element](/uwp/schemas/appxpackage/uapmanifestschema/element-identity) in Ihrem Sparsepaketmanifest übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="9e398-431">This value must match the **Publisher** attribute in the [Identity](/uwp/schemas/appxpackage/uapmanifestschema/element-identity) element in your sparse package manifest.</span></span> |
| <span data-ttu-id="9e398-432">**packageName**</span><span class="sxs-lookup"><span data-stu-id="9e398-432">**packageName**</span></span> | <span data-ttu-id="9e398-433">Beschreibt den Inhalt des Pakets.</span><span class="sxs-lookup"><span data-stu-id="9e398-433">Describes the contents of the package.</span></span> <span data-ttu-id="9e398-434">Dieser Wert muss mit dem **Name-Attribut** im [Identity-Element](/uwp/schemas/appxpackage/uapmanifestschema/element-identity) in Ihrem Sparsepaketmanifest übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="9e398-434">This value must match the **Name** attribute in the [Identity](/uwp/schemas/appxpackage/uapmanifestschema/element-identity) element in your sparse package manifest.</span></span>    |
| <span data-ttu-id="9e398-435">**applicationId**</span><span class="sxs-lookup"><span data-stu-id="9e398-435">**applicationId**</span></span>    | <span data-ttu-id="9e398-436">Der eindeutige Bezeichner der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="9e398-436">The unique identifier of the application.</span></span> <span data-ttu-id="9e398-437">Dieser Wert muss mit dem **ID-Attribut** im [Application-Element](/uwp/schemas/appxpackage/uapmanifestschema/element-application) in Ihrem Sparsepaketmanifest übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="9e398-437">This value must match the **Id** attribute in the [Application](/uwp/schemas/appxpackage/uapmanifestschema/element-application) element in your sparse package manifest.</span></span>  |

```xml
<?xml version="1.0" encoding="utf-8"?>
<assembly manifestVersion="1.0" xmlns="urn:schemas-microsoft-com:asm.v1">
  <assemblyIdentity version="1.0.0.0" name="Contoso.PhotoStoreApp"/>
  <msix xmlns="urn:schemas-microsoft-com:msix.v1"
          publisher="CN=Contoso"
          packageName="ContosoPhotoStore"
          applicationId="ContosoPhotoStore"
        />
</assembly>
```

### <a name="heaptype"></a><span data-ttu-id="9e398-438">heapType</span><span class="sxs-lookup"><span data-stu-id="9e398-438">heapType</span></span>

<span data-ttu-id="9e398-439">Überschreibt die Standardmäßige Heapimplementierung für die zu verwendenden [Win32-Heap-APIs.](../Memory/heap-functions.md)</span><span class="sxs-lookup"><span data-stu-id="9e398-439">Overrides the default heap implementation for the [Win32 heap APIs](../Memory/heap-functions.md) to use.</span></span>

* <span data-ttu-id="9e398-440">Der Wert **SegmentHeap gibt** an, dass der Segmentheap verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9e398-440">The value **SegmentHeap** indicates that segment heap will be used.</span></span> <span data-ttu-id="9e398-441">Segment heap ist eine moderne Heapimplementierung, die im Allgemeinen die Gesamtspeicherauslastung reduziert.</span><span class="sxs-lookup"><span data-stu-id="9e398-441">Segment heap is a modern heap implementation that will generally reduce your overall memory usage.</span></span> <span data-ttu-id="9e398-442">Dieses Element wird in Windows 10 Version 2004 (Build 19041) und höher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9e398-442">This element is supported in Windows 10, version 2004 (build 19041) and later.</span></span>
* <span data-ttu-id="9e398-443">Alle anderen Werte werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="9e398-443">All other values are ignored.</span></span>

<span data-ttu-id="9e398-444">Dieses Element weist keine Attribute auf.</span><span class="sxs-lookup"><span data-stu-id="9e398-444">This element has no attributes.</span></span>

```XML
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
 ...
  <asmv3:application>
    <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2020/WindowsSettings">
      <heapType>SegmentHeap</heapType>
    </asmv3:windowsSettings>
  </asmv3:application>
 ...
</assembly>
```

## <a name="example"></a><span data-ttu-id="9e398-445">Beispiel</span><span class="sxs-lookup"><span data-stu-id="9e398-445">Example</span></span>

<span data-ttu-id="9e398-446">Im Folgenden finden Sie ein Beispiel für ein Anwendungsmanifest für eine Anwendung namens MySampleApp.exe.</span><span class="sxs-lookup"><span data-stu-id="9e398-446">The following is an example of an application manifest for an application named MySampleApp.exe.</span></span> <span data-ttu-id="9e398-447">Die Anwendung verwendet die seiteseitige SampleAssembly-Assembly.</span><span class="sxs-lookup"><span data-stu-id="9e398-447">The application consumes the SampleAssembly side-by-side assembly.</span></span>

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">

  <compatibility xmlns="urn:schemas-microsoft-com:compatibility.v1"> 
      <application> 
        <!--This Id value indicates the application supports Windows Vista functionality -->
          <supportedOS Id="{e2011457-1546-43c5-a5fe-008deee3d3f0}"/> 
        <!--This Id value indicates the application supports Windows 7 functionality-->
          <supportedOS Id="{35138b9a-5d96-4fbd-8e2d-a2440225f93a}"/>
        <!--This Id value indicates the application supports Windows 8 functionality-->
          <supportedOS Id="{4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}"/>
        <!--This Id value indicates the application supports Windows 8.1 functionality-->
          <supportedOS Id="{1f676c76-80e1-4239-95bb-83d0f6d0da78}"/>
      </application> 
  </compatibility>

  <assemblyIdentity type="win32" 
                    name="myOrganization.myDivision.mySampleApp" 
                    version="6.0.0.0" 
                    processorArchitecture="x86" 
                    publicKeyToken="0000000000000000"
  />
  <dependency>
    <dependentAssembly>
      <assemblyIdentity type="win32" 
                        name="Proseware.Research.SampleAssembly" 
                        version="6.0.0.0" 
                        processorArchitecture="X86" 
                        publicKeyToken="0000000000000000" 
                        language="*"
      />
    </dependentAssembly>
  </dependency>
</assembly>
```
