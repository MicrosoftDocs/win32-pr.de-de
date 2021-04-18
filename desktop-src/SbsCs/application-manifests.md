---
description: Ein Anwendungsmanifest ist eine XML-Datei, die die freigegebenen und privaten parallelen Assemblys beschreibt und identifiziert, an die sich eine Anwendung zur Laufzeit binden soll.
ms.assetid: c5016251-db7a-4edc-9be9-3acb03d495f8
title: Anwendungs Manifeste
ms.topic: article
ms.date: 10/08/2020
ms.custom: 19H1
ms.openlocfilehash: cb065bc4d6d29f4142c23cdd91c83769e2fb9b87
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/05/2021
ms.locfileid: "106365208"
---
# <a name="application-manifests"></a><span data-ttu-id="63f20-103">Anwendungs Manifeste</span><span class="sxs-lookup"><span data-stu-id="63f20-103">Application Manifests</span></span>

<span data-ttu-id="63f20-104">Ein Anwendungsmanifest ist eine XML-Datei, die die freigegebenen und privaten parallelen Assemblys beschreibt und identifiziert, an die sich eine Anwendung zur Laufzeit binden soll.</span><span class="sxs-lookup"><span data-stu-id="63f20-104">An application manifest is an XML file that describes and identifies the shared and private side-by-side assemblies that an application should bind to at run time.</span></span> <span data-ttu-id="63f20-105">Dabei sollte es sich um die gleichen Assemblyversionen handeln, die zum Testen der Anwendung verwendet wurden.</span><span class="sxs-lookup"><span data-stu-id="63f20-105">These should be the same assembly versions that were used to test the application.</span></span> <span data-ttu-id="63f20-106">Anwendungsmanifeste können auch Metadaten für private Anwendungsdateien beschreiben.</span><span class="sxs-lookup"><span data-stu-id="63f20-106">Application manifests may also describe metadata for files that are private to the application.</span></span>

<span data-ttu-id="63f20-107">Eine umfassende Liste des XML-Schemas finden Sie unter [Manifest-Datei Schema](manifest-file-schema.md).</span><span class="sxs-lookup"><span data-stu-id="63f20-107">For a complete listing of the XML schema, see [Manifest File Schema](manifest-file-schema.md).</span></span>

<span data-ttu-id="63f20-108">Anwendungs Manifeste verfügen über die folgenden Elemente und Attribute.</span><span class="sxs-lookup"><span data-stu-id="63f20-108">Application manifests have the following elements and attributes.</span></span>

| <span data-ttu-id="63f20-109">Element</span><span class="sxs-lookup"><span data-stu-id="63f20-109">Element</span></span>                               | <span data-ttu-id="63f20-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="63f20-110">Attributes</span></span>                | <span data-ttu-id="63f20-111">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="63f20-111">Required</span></span> |
|---------------------------------------|---------------------------|----------|
| <span data-ttu-id="63f20-112">**Stadtverordneten**</span><span class="sxs-lookup"><span data-stu-id="63f20-112">**assembly**</span></span>                          |                           | <span data-ttu-id="63f20-113">Ja</span><span class="sxs-lookup"><span data-stu-id="63f20-113">Yes</span></span>      |
|                                       | <span data-ttu-id="63f20-114">**manifestVersion**</span><span class="sxs-lookup"><span data-stu-id="63f20-114">**manifestVersion**</span></span>       | <span data-ttu-id="63f20-115">Ja</span><span class="sxs-lookup"><span data-stu-id="63f20-115">Yes</span></span>      |
| <span data-ttu-id="63f20-116">**NoInherit**</span><span class="sxs-lookup"><span data-stu-id="63f20-116">**noInherit**</span></span>                         |                           | <span data-ttu-id="63f20-117">Nein</span><span class="sxs-lookup"><span data-stu-id="63f20-117">No</span></span>       |
| <span data-ttu-id="63f20-118">**AssemblyIdentity**</span><span class="sxs-lookup"><span data-stu-id="63f20-118">**assemblyIdentity**</span></span>                  |                           | <span data-ttu-id="63f20-119">Ja</span><span class="sxs-lookup"><span data-stu-id="63f20-119">Yes</span></span>      |
|                                       | <span data-ttu-id="63f20-120">**type**</span><span class="sxs-lookup"><span data-stu-id="63f20-120">**type**</span></span>                  | <span data-ttu-id="63f20-121">Ja</span><span class="sxs-lookup"><span data-stu-id="63f20-121">Yes</span></span>      |
|                                       | <span data-ttu-id="63f20-122">**name**</span><span class="sxs-lookup"><span data-stu-id="63f20-122">**name**</span></span>                  | <span data-ttu-id="63f20-123">Ja</span><span class="sxs-lookup"><span data-stu-id="63f20-123">Yes</span></span>      |
|                                       | <span data-ttu-id="63f20-124">**language**</span><span class="sxs-lookup"><span data-stu-id="63f20-124">**language**</span></span>              | <span data-ttu-id="63f20-125">Nein</span><span class="sxs-lookup"><span data-stu-id="63f20-125">No</span></span>       |
|                                       | <span data-ttu-id="63f20-126">**processorArchitecture**</span><span class="sxs-lookup"><span data-stu-id="63f20-126">**processorArchitecture**</span></span> | <span data-ttu-id="63f20-127">Nein</span><span class="sxs-lookup"><span data-stu-id="63f20-127">No</span></span>       |
|                                       | <span data-ttu-id="63f20-128">**version**</span><span class="sxs-lookup"><span data-stu-id="63f20-128">**version**</span></span>               | <span data-ttu-id="63f20-129">Ja</span><span class="sxs-lookup"><span data-stu-id="63f20-129">Yes</span></span>      |
|                                       | <span data-ttu-id="63f20-130">**PublicKeyToken**</span><span class="sxs-lookup"><span data-stu-id="63f20-130">**publicKeyToken**</span></span>        | <span data-ttu-id="63f20-131">Nein</span><span class="sxs-lookup"><span data-stu-id="63f20-131">No</span></span>       |
| <span data-ttu-id="63f20-132">**glichkeits**</span><span class="sxs-lookup"><span data-stu-id="63f20-132">**compatibility**</span></span>                     |                           | <span data-ttu-id="63f20-133">Nein</span><span class="sxs-lookup"><span data-stu-id="63f20-133">No</span></span>       |
| <span data-ttu-id="63f20-134">**application**</span><span class="sxs-lookup"><span data-stu-id="63f20-134">**application**</span></span>                       |                           | <span data-ttu-id="63f20-135">Nein</span><span class="sxs-lookup"><span data-stu-id="63f20-135">No</span></span>       |
| <span data-ttu-id="63f20-136">**supportedOS**</span><span class="sxs-lookup"><span data-stu-id="63f20-136">**supportedOS**</span></span>                       | <span data-ttu-id="63f20-137">**Id**</span><span class="sxs-lookup"><span data-stu-id="63f20-137">**Id**</span></span>                    | <span data-ttu-id="63f20-138">Nein</span><span class="sxs-lookup"><span data-stu-id="63f20-138">No</span></span>       |
| <span data-ttu-id="63f20-139">**"maxversiontested"**</span><span class="sxs-lookup"><span data-stu-id="63f20-139">**maxversiontested**</span></span>                  | <span data-ttu-id="63f20-140">**Id**</span><span class="sxs-lookup"><span data-stu-id="63f20-140">**Id**</span></span>                    | <span data-ttu-id="63f20-141">Nein</span><span class="sxs-lookup"><span data-stu-id="63f20-141">No</span></span>       |
| <span data-ttu-id="63f20-142">**gkeit**</span><span class="sxs-lookup"><span data-stu-id="63f20-142">**dependency**</span></span>                        |                           | <span data-ttu-id="63f20-143">Nein</span><span class="sxs-lookup"><span data-stu-id="63f20-143">No</span></span>       |
| <span data-ttu-id="63f20-144">**dependentAssembly**</span><span class="sxs-lookup"><span data-stu-id="63f20-144">**dependentAssembly**</span></span>                 |                           | <span data-ttu-id="63f20-145">Nein</span><span class="sxs-lookup"><span data-stu-id="63f20-145">No</span></span>       |
| <span data-ttu-id="63f20-146">**datei**</span><span class="sxs-lookup"><span data-stu-id="63f20-146">**file**</span></span>                              |                           | <span data-ttu-id="63f20-147">Nein</span><span class="sxs-lookup"><span data-stu-id="63f20-147">No</span></span>       |
|                                       | <span data-ttu-id="63f20-148">**name**</span><span class="sxs-lookup"><span data-stu-id="63f20-148">**name**</span></span>                  | <span data-ttu-id="63f20-149">Nein</span><span class="sxs-lookup"><span data-stu-id="63f20-149">No</span></span>       |
|                                       | <span data-ttu-id="63f20-150">**HashAlg**</span><span class="sxs-lookup"><span data-stu-id="63f20-150">**hashalg**</span></span>               | <span data-ttu-id="63f20-151">Nein</span><span class="sxs-lookup"><span data-stu-id="63f20-151">No</span></span>       |
|                                       | <span data-ttu-id="63f20-152">**hash**</span><span class="sxs-lookup"><span data-stu-id="63f20-152">**hash**</span></span>                  | <span data-ttu-id="63f20-153">Nein</span><span class="sxs-lookup"><span data-stu-id="63f20-153">No</span></span>       |
| <span data-ttu-id="63f20-154">**activecodepage**</span><span class="sxs-lookup"><span data-stu-id="63f20-154">**activeCodePage**</span></span>                    |                           | <span data-ttu-id="63f20-155">Nein</span><span class="sxs-lookup"><span data-stu-id="63f20-155">No</span></span>       |
| <span data-ttu-id="63f20-156">**automatische Erhöhung**</span><span class="sxs-lookup"><span data-stu-id="63f20-156">**autoElevate**</span></span>                       |                           | <span data-ttu-id="63f20-157">Nein</span><span class="sxs-lookup"><span data-stu-id="63f20-157">No</span></span>       |
| <span data-ttu-id="63f20-158">**wird deaktiviert**</span><span class="sxs-lookup"><span data-stu-id="63f20-158">**disableTheming**</span></span>                    |                           | <span data-ttu-id="63f20-159">Nein</span><span class="sxs-lookup"><span data-stu-id="63f20-159">No</span></span>       |
| <span data-ttu-id="63f20-160">**disablewindowfiltering**</span><span class="sxs-lookup"><span data-stu-id="63f20-160">**disableWindowFiltering**</span></span>            |                           | <span data-ttu-id="63f20-161">Nein</span><span class="sxs-lookup"><span data-stu-id="63f20-161">No</span></span>       |
| <span data-ttu-id="63f20-162">**dpiaware**</span><span class="sxs-lookup"><span data-stu-id="63f20-162">**dpiAware**</span></span>                          |                           | <span data-ttu-id="63f20-163">Nein</span><span class="sxs-lookup"><span data-stu-id="63f20-163">No</span></span>       |
| <span data-ttu-id="63f20-164">**dpiawareness**</span><span class="sxs-lookup"><span data-stu-id="63f20-164">**dpiAwareness**</span></span>                      |                           | <span data-ttu-id="63f20-165">Nein</span><span class="sxs-lookup"><span data-stu-id="63f20-165">No</span></span>       |
| <span data-ttu-id="63f20-166">**gdiskretihl**</span><span class="sxs-lookup"><span data-stu-id="63f20-166">**gdiScaling**</span></span>                        |                           | <span data-ttu-id="63f20-167">Nein</span><span class="sxs-lookup"><span data-stu-id="63f20-167">No</span></span>       |
| <span data-ttu-id="63f20-168">**highresolutionscrollingaware**</span><span class="sxs-lookup"><span data-stu-id="63f20-168">**highResolutionScrollingAware**</span></span>      |                           | <span data-ttu-id="63f20-169">Nein</span><span class="sxs-lookup"><span data-stu-id="63f20-169">No</span></span>       |
| <span data-ttu-id="63f20-170">**longpathaware**</span><span class="sxs-lookup"><span data-stu-id="63f20-170">**longPathAware**</span></span>                     |                           | <span data-ttu-id="63f20-171">Nein</span><span class="sxs-lookup"><span data-stu-id="63f20-171">No</span></span>       |
| <span data-ttu-id="63f20-172">**printerdriverisolation**</span><span class="sxs-lookup"><span data-stu-id="63f20-172">**printerDriverIsolation**</span></span>            |                           | <span data-ttu-id="63f20-173">Nein</span><span class="sxs-lookup"><span data-stu-id="63f20-173">No</span></span>       |
| <span data-ttu-id="63f20-174">**ultrahighresolutionscrollingaware**</span><span class="sxs-lookup"><span data-stu-id="63f20-174">**ultraHighResolutionScrollingAware**</span></span> |                           | <span data-ttu-id="63f20-175">Nein</span><span class="sxs-lookup"><span data-stu-id="63f20-175">No</span></span>       |
| <span data-ttu-id="63f20-176">**msix**</span><span class="sxs-lookup"><span data-stu-id="63f20-176">**msix**</span></span>                              |                           | <span data-ttu-id="63f20-177">Nein</span><span class="sxs-lookup"><span data-stu-id="63f20-177">No</span></span>       |
| <span data-ttu-id="63f20-178">**heaptype**</span><span class="sxs-lookup"><span data-stu-id="63f20-178">**heapType**</span></span>                          |                           | <span data-ttu-id="63f20-179">Nein</span><span class="sxs-lookup"><span data-stu-id="63f20-179">No</span></span>       |

## <a name="file-location"></a><span data-ttu-id="63f20-180">Dateispeicherort</span><span class="sxs-lookup"><span data-stu-id="63f20-180">File Location</span></span>

<span data-ttu-id="63f20-181">Anwendungs Manifeste sollten als Ressource in die exe-Datei oder DLL-Datei der Anwendung eingeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="63f20-181">Application manifests should be included as a resource in the application's EXE file or DLL.</span></span>

<span data-ttu-id="63f20-182">Weitere Informationen finden Sie unter [Installieren](installing-side-by-side-assemblies.md)paralleler Assemblys.</span><span class="sxs-lookup"><span data-stu-id="63f20-182">For more information, see [Installing Side-by-side Assemblies](installing-side-by-side-assemblies.md).</span></span>

## <a name="file-name-syntax"></a><span data-ttu-id="63f20-183">Dateinamensyntax</span><span class="sxs-lookup"><span data-stu-id="63f20-183">File Name Syntax</span></span>

<span data-ttu-id="63f20-184">Der Name einer Anwendungs Manifest-Datei ist der Name der ausführbaren Datei der Anwendung gefolgt von ". Manifest".</span><span class="sxs-lookup"><span data-stu-id="63f20-184">The name of an application manifest file is the name of the application's executable followed by .manifest.</span></span>

<span data-ttu-id="63f20-185">Beispielsweise würde ein Anwendungs Manifest, das auf example.exe oder example.dll verweist, die folgende Dateiname-Syntax verwenden.</span><span class="sxs-lookup"><span data-stu-id="63f20-185">For example, an application manifest that refers to example.exe or example.dll would use the following file name syntax.</span></span> <span data-ttu-id="63f20-186">Wenn die Ressourcen-ID 1 ist, können Sie die <*Ressourcen-ID*> Feld weglassen.</span><span class="sxs-lookup"><span data-stu-id="63f20-186">You can omit the <*resource ID*> field if resource ID is 1.</span></span>

<span data-ttu-id="63f20-187">**example.exe. <*Ressourcen-ID*>. Manifest**</span><span class="sxs-lookup"><span data-stu-id="63f20-187">**example.exe.<*resource ID*>.manifest**</span></span>

<span data-ttu-id="63f20-188">**example.dll. <*Ressourcen-ID*>. Manifest**</span><span class="sxs-lookup"><span data-stu-id="63f20-188">**example.dll.<*resource ID*>.manifest**</span></span>

## <a name="elements"></a><span data-ttu-id="63f20-189">Elemente</span><span class="sxs-lookup"><span data-stu-id="63f20-189">Elements</span></span>

<span data-ttu-id="63f20-190">Bei Namen von Elementen und Attributen wird die Groß-/Kleinschreibung beachtet.</span><span class="sxs-lookup"><span data-stu-id="63f20-190">Names of elements and attributes are case-sensitive.</span></span> <span data-ttu-id="63f20-191">Bei den Werten von Elementen und Attributen wird die Groß-/Kleinschreibung nicht beachtet, außer dem Wert des Type-Attributs.</span><span class="sxs-lookup"><span data-stu-id="63f20-191">The values of elements and attributes are case-insensitive, except for the value of the type attribute.</span></span>

<span id="assembly"></span><span id="ASSEMBLY"></span>

### <a name="assembly"></a><span data-ttu-id="63f20-192">Assembly</span><span class="sxs-lookup"><span data-stu-id="63f20-192">assembly</span></span>

<span data-ttu-id="63f20-193">Ein Containerelement.</span><span class="sxs-lookup"><span data-stu-id="63f20-193">A container element.</span></span> <span data-ttu-id="63f20-194">Das erste Unterelement muss ein **novererbungs** -oder **assemblyIdentity** -Element sein.</span><span class="sxs-lookup"><span data-stu-id="63f20-194">Its first subelement must be a **noInherit** or **assemblyIdentity** element.</span></span> <span data-ttu-id="63f20-195">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="63f20-195">Required.</span></span>

<span data-ttu-id="63f20-196">Das **Assembly** -Element muss sich im Namespace "urn: Schemas-Microsoft-com: ASM. v1" befinden.</span><span class="sxs-lookup"><span data-stu-id="63f20-196">The **assembly** element must be in the namespace "urn:schemas-microsoft-com:asm.v1".</span></span> <span data-ttu-id="63f20-197">Untergeordnete Elemente der Assembly müssen sich ebenfalls in diesem Namespace befinden, durch Vererbung oder durch Tagging.</span><span class="sxs-lookup"><span data-stu-id="63f20-197">Child elements of the assembly must also be in this namespace, by inheritance or by tagging.</span></span>

<span data-ttu-id="63f20-198">Das **Assembly** -Element weist die folgenden Attribute auf.</span><span class="sxs-lookup"><span data-stu-id="63f20-198">The **assembly** element has the following attributes.</span></span>



| <span data-ttu-id="63f20-199">Attribut</span><span class="sxs-lookup"><span data-stu-id="63f20-199">Attribute</span></span>           | <span data-ttu-id="63f20-200">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="63f20-200">Description</span></span>                                           |
|---------------------|-------------------------------------------------------|
| <span data-ttu-id="63f20-201">**manifestVersion**</span><span class="sxs-lookup"><span data-stu-id="63f20-201">**manifestVersion**</span></span> | <span data-ttu-id="63f20-202">Das **manifestVersion** -Attribut muss auf 1,0 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="63f20-202">The **manifestVersion** attribute must be set to 1.0.</span></span> |


<span id="noInherit"></span><span id="noinherit"></span><span id="NOINHERIT"></span>

### <a name="noinherit"></a><span data-ttu-id="63f20-203">NoInherit</span><span class="sxs-lookup"><span data-stu-id="63f20-203">noInherit</span></span>

<span data-ttu-id="63f20-204">Fügen Sie dieses Element in ein Anwendungs Manifest ein, um die aus dem Manifest generierten [Aktivierungs Kontexte](activation-contexts.md) mit dem Flag "No Erben" festzulegen.</span><span class="sxs-lookup"><span data-stu-id="63f20-204">Include this element in an application manifest to set the [activation contexts](activation-contexts.md) generated from the manifest with the "no inherit" flag.</span></span> <span data-ttu-id="63f20-205">Wenn dieses Flag nicht in einem Aktivierungs Kontext festgelegt ist und der Aktivierungs Kontext aktiv ist, wird es von neuen Threads im gleichen Prozess, in Fenstern, in Fenster Prozeduren und [asynchronen Prozedur aufrufen](/windows/desktop/Sync/asynchronous-procedure-calls)geerbt.</span><span class="sxs-lookup"><span data-stu-id="63f20-205">When this flag is not set in an activation context, and the activation context is active, it is inherited by new threads in the same process, windows, window procedures, and [Asynchronous Procedure Calls](/windows/desktop/Sync/asynchronous-procedure-calls).</span></span> <span data-ttu-id="63f20-206">Durch Festlegen dieses Flags wird verhindert, dass das neue-Objekt den aktiven Kontext erbt.</span><span class="sxs-lookup"><span data-stu-id="63f20-206">Setting this flag prevents the new object from inheriting the active context.</span></span>

<span data-ttu-id="63f20-207">Das **noerben** -Element ist optional und wird in der Regel ausgelassen.</span><span class="sxs-lookup"><span data-stu-id="63f20-207">The **noInherit** element is optional and typically omitted.</span></span> <span data-ttu-id="63f20-208">Die meisten Assemblys funktionieren nicht ordnungsgemäß mit einem Aktivierungs Kontext ohne Vererbung, da die Assembly explizit für die Verwaltung der Propagierung Ihres eigenen Aktivierungs Kontexts entworfen werden muss.</span><span class="sxs-lookup"><span data-stu-id="63f20-208">Most assemblies do not work correctly using a no-inherit activation context because the assembly must be explicitly designed to manage the propagation of their own activation context.</span></span> <span data-ttu-id="63f20-209">Die Verwendung des **noerben** -Elements erfordert, dass alle abhängigen Assemblys, auf die das Anwendungs Manifest verweist, über ein **noerben** -Element in Ihrem Assemblymanifest verfügen [](assembly-manifests.md)</span><span class="sxs-lookup"><span data-stu-id="63f20-209">The use of the **noInherit** element requires that any dependent assemblies referenced by the application manifest have a **noInherit** element in their [assembly manifest](assembly-manifests.md).</span></span>

<span data-ttu-id="63f20-210">Wenn **novererbung** in einem Manifest verwendet wird, muss es das erste Unterelement des **Assembly** -Elements sein.</span><span class="sxs-lookup"><span data-stu-id="63f20-210">If **noInherit** is used in a manifest, it must be the first subelement of the **assembly** element.</span></span> <span data-ttu-id="63f20-211">Das **assemblyIdentity** -Element sollte direkt hinter dem **noerben** -Element stehen.</span><span class="sxs-lookup"><span data-stu-id="63f20-211">The **assemblyIdentity** element should come immediately after the **noInherit** element.</span></span> <span data-ttu-id="63f20-212">Wenn **noerben** nicht verwendet wird, muss **assemblyIdentity** das erste untergeordnete Element des **Assembly** -Elements sein.</span><span class="sxs-lookup"><span data-stu-id="63f20-212">If **noInherit** is not used, **assemblyIdentity** must be the first subelement of the **assembly** element.</span></span> <span data-ttu-id="63f20-213">Das **noerben** -Element weist keine untergeordneten Elemente auf.</span><span class="sxs-lookup"><span data-stu-id="63f20-213">The **noInherit** element has no child elements.</span></span> <span data-ttu-id="63f20-214">Es ist kein gültiges Element in [Assemblymanifesten](assembly-manifests.md).</span><span class="sxs-lookup"><span data-stu-id="63f20-214">It is not a valid element in [assembly manifests](assembly-manifests.md).</span></span>

<span id="assemblyIdentity"></span><span id="assemblyidentity"></span><span id="ASSEMBLYIDENTITY"></span>

### <a name="assemblyidentity"></a><span data-ttu-id="63f20-215">assemblyIdentity</span><span class="sxs-lookup"><span data-stu-id="63f20-215">assemblyIdentity</span></span>

<span data-ttu-id="63f20-216">Als erstes **Unterelement eines** **Assemblyelements beschreibt assemblyIdentity** die Anwendung, die dieses Anwendungs Manifest besitzt, und identifiziert Sie eindeutig.</span><span class="sxs-lookup"><span data-stu-id="63f20-216">As the first subelement of an **assembly** element, **assemblyIdentity** describes and uniquely identifies the application owning this application manifest.</span></span> <span data-ttu-id="63f20-217">Als erstes Unterelement eines **dependentAssembly** -Elements beschreibt **assemblyIdentity** eine parallele Assembly, die für die Anwendung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="63f20-217">As the first subelement of a **dependentAssembly** element, **assemblyIdentity** describes a side-by-side assembly required by the application.</span></span> <span data-ttu-id="63f20-218">Beachten Sie, dass für jede Assembly, auf die im Anwendungs Manifest verwiesen wird, eine **assemblyIdentity** erforderlich ist, die exakt der **assemblyIdentity im eigenen Assemblymanifest** der referenzierten Assembly entspricht.</span><span class="sxs-lookup"><span data-stu-id="63f20-218">Note that every assembly referenced in the application manifest requires an **assemblyIdentity** that exactly matches the **assemblyIdentity** in the referenced assembly's own assembly manifest.</span></span>

<span data-ttu-id="63f20-219">Das **assemblyIdentity** -Element verfügt über die folgenden Attribute.</span><span class="sxs-lookup"><span data-stu-id="63f20-219">The **assemblyIdentity** element has the following attributes.</span></span> <span data-ttu-id="63f20-220">Sie hat keine unter Elemente.</span><span class="sxs-lookup"><span data-stu-id="63f20-220">It has no subelements.</span></span>

| <span data-ttu-id="63f20-221">Attribut</span><span class="sxs-lookup"><span data-stu-id="63f20-221">Attribute</span></span>                 | <span data-ttu-id="63f20-222">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="63f20-222">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63f20-223">**type**</span><span class="sxs-lookup"><span data-stu-id="63f20-223">**type**</span></span>                  | <span data-ttu-id="63f20-224">Gibt den Anwendungs-oder Assemblytyp an.</span><span class="sxs-lookup"><span data-stu-id="63f20-224">Specifies the application or assembly type.</span></span> <span data-ttu-id="63f20-225">Der Wert muss Win32 und in Kleinbuchstaben sein.</span><span class="sxs-lookup"><span data-stu-id="63f20-225">The value must be Win32 and all in lower case.</span></span> <span data-ttu-id="63f20-226">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="63f20-226">Required.</span></span>                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="63f20-227">**name**</span><span class="sxs-lookup"><span data-stu-id="63f20-227">**name**</span></span>                  | <span data-ttu-id="63f20-228">Benennt die Anwendung oder Assembly eindeutig.</span><span class="sxs-lookup"><span data-stu-id="63f20-228">Uniquely names the application or assembly.</span></span> <span data-ttu-id="63f20-229">Verwenden Sie das folgende Format für den Namen: Organization.Division.Name.</span><span class="sxs-lookup"><span data-stu-id="63f20-229">Use the following format for the name: Organization.Division.Name.</span></span> <span data-ttu-id="63f20-230">Beispiel: Microsoft. Windows. MySampleApp.</span><span class="sxs-lookup"><span data-stu-id="63f20-230">For example Microsoft.Windows.mysampleApp.</span></span> <span data-ttu-id="63f20-231">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="63f20-231">Required.</span></span>                                                                                                                                                                                                                                                               |
| <span data-ttu-id="63f20-232">**language**</span><span class="sxs-lookup"><span data-stu-id="63f20-232">**language**</span></span>              | <span data-ttu-id="63f20-233">Identifiziert die Sprache der Anwendung oder Assembly.</span><span class="sxs-lookup"><span data-stu-id="63f20-233">Identifies the language of the application or assembly.</span></span> <span data-ttu-id="63f20-234">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="63f20-234">Optional.</span></span> <span data-ttu-id="63f20-235">Wenn die Anwendung oder Assembly sprachspezifisch ist, geben Sie den Code der DHTML-Sprache an.</span><span class="sxs-lookup"><span data-stu-id="63f20-235">If the application or assembly is language-specific, specify the DHTML language code.</span></span> <span data-ttu-id="63f20-236">Lassen Sie in der **Assemblyidentität** einer Anwendung, die für die weltweite Verwendung vorgesehen ist (Sprachneutral), das Language-Attribut aus.</span><span class="sxs-lookup"><span data-stu-id="63f20-236">In the **assemblyIdentity** of an application intended for worldwide use (language neutral) omit the language attribute.</span></span><br/> <span data-ttu-id="63f20-237">Legen Sie in einer **Assemblyidentität** einer Assembly, die für die weltweite Verwendung vorgesehen ist (Sprachneutral), den Wert der Sprache auf " \* " fest.</span><span class="sxs-lookup"><span data-stu-id="63f20-237">In an **assemblyIdentity** of an assembly intended for worldwide use (language neutral) set the value of language to "\*".</span></span><br/> |
| <span data-ttu-id="63f20-238">**processorArchitecture**</span><span class="sxs-lookup"><span data-stu-id="63f20-238">**processorArchitecture**</span></span> | <span data-ttu-id="63f20-239">Gibt den Prozessor an.</span><span class="sxs-lookup"><span data-stu-id="63f20-239">Specifies the processor.</span></span> <span data-ttu-id="63f20-240">Gültige Werte sind `x86`, `amd64`, `arm` und `arm64`.</span><span class="sxs-lookup"><span data-stu-id="63f20-240">Valid values include `x86`, `amd64`, `arm` and `arm64`.</span></span> <span data-ttu-id="63f20-241">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="63f20-241">Optional.</span></span>                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="63f20-242">**version**</span><span class="sxs-lookup"><span data-stu-id="63f20-242">**version**</span></span>               | <span data-ttu-id="63f20-243">Gibt die Anwendungs-oder Assemblyversion an.</span><span class="sxs-lookup"><span data-stu-id="63f20-243">Specifies the application or assembly version.</span></span> <span data-ttu-id="63f20-244">Verwenden Sie das vierteilige Versions Format: mmmmm. nnnnn. Ooooo. ppppp.</span><span class="sxs-lookup"><span data-stu-id="63f20-244">Use the four-part version format: mmmmm.nnnnn.ooooo.ppppp.</span></span> <span data-ttu-id="63f20-245">Alle durch Zeiträume getrennten Teile können 0-65535 einschließlich sein.</span><span class="sxs-lookup"><span data-stu-id="63f20-245">Each of the parts separated by periods can be 0-65535 inclusive.</span></span> <span data-ttu-id="63f20-246">Weitere Informationen finden Sie unter [Assemblyversionen](assembly-versions.md).</span><span class="sxs-lookup"><span data-stu-id="63f20-246">For more information, see [Assembly Versions](assembly-versions.md).</span></span> <span data-ttu-id="63f20-247">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="63f20-247">Required.</span></span>                                                                                                                                                                        |
| <span data-ttu-id="63f20-248">**PublicKeyToken**</span><span class="sxs-lookup"><span data-stu-id="63f20-248">**publicKeyToken**</span></span>        | <span data-ttu-id="63f20-249">Eine hexadezimale Zeichenfolge mit 16 Zeichen, die die letzten 8 Bytes des SHA-1-Hashs des öffentlichen Schlüssels darstellt, unter dem die Anwendung oder Assembly signiert ist.</span><span class="sxs-lookup"><span data-stu-id="63f20-249">A 16-character hexadecimal string representing the last 8 bytes of the SHA-1 hash of the public key under which the application or assembly is signed.</span></span> <span data-ttu-id="63f20-250">Der öffentliche Schlüssel, der zum Signieren des Katalogs verwendet wird, muss 2048 Bit oder größer sein.</span><span class="sxs-lookup"><span data-stu-id="63f20-250">The public key used to sign the catalog must be 2048 bits or greater.</span></span> <span data-ttu-id="63f20-251">Erforderlich für alle freigegebenen parallelen Assemblys.</span><span class="sxs-lookup"><span data-stu-id="63f20-251">Required for all shared side-by-side assemblies.</span></span>                                                                                                                                                     |

<span id="compatibility"></span><span id="COMPATIBILITY"></span>

### <a name="compatibility"></a><span data-ttu-id="63f20-252">Kompatibilität</span><span class="sxs-lookup"><span data-stu-id="63f20-252">compatibility</span></span>

<span data-ttu-id="63f20-253">Enthält mindestens eine **Anwendung**.</span><span class="sxs-lookup"><span data-stu-id="63f20-253">Contains at least one **application**.</span></span> <span data-ttu-id="63f20-254">Sie besitzt keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="63f20-254">It has no attributes.</span></span> <span data-ttu-id="63f20-255">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="63f20-255">Optional.</span></span> <span data-ttu-id="63f20-256">Anwendungs Manifeste ohne Kompatibilitäts Element sind standardmäßig Windows Vista-Kompatibilität unter Windows 7.</span><span class="sxs-lookup"><span data-stu-id="63f20-256">Application manifests without a compatibility element default to Windows Vista compatibility on Windows 7.</span></span>

<span id="application"></span><span id="APPLICATION"></span>

### <a name="application"></a><span data-ttu-id="63f20-257">application</span><span class="sxs-lookup"><span data-stu-id="63f20-257">application</span></span>

<span data-ttu-id="63f20-258">Enthält mindestens ein **SupportedOS** -Element.</span><span class="sxs-lookup"><span data-stu-id="63f20-258">Contains at least one **supportedOS** element.</span></span> <span data-ttu-id="63f20-259">Ab Windows 10, Version 1903, kann es auch ein optionales **maxversiongeteteelement** enthalten.</span><span class="sxs-lookup"><span data-stu-id="63f20-259">Starting in Windows 10, version 1903, it can also contain one optional **maxversiontested** element.</span></span> <span data-ttu-id="63f20-260">Sie besitzt keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="63f20-260">It has no attributes.</span></span> <span data-ttu-id="63f20-261">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="63f20-261">Optional.</span></span>

<span id="supportedOS"></span><span id="supportedos"></span><span id="SUPPORTEDOS"></span>

### <a name="supportedos"></a><span data-ttu-id="63f20-262">supportedOS</span><span class="sxs-lookup"><span data-stu-id="63f20-262">supportedOS</span></span>

<span data-ttu-id="63f20-263">Das **SupportedOS** -Element verfügt über das folgende Attribut.</span><span class="sxs-lookup"><span data-stu-id="63f20-263">The **supportedOS** element has the following attribute.</span></span> <span data-ttu-id="63f20-264">Sie hat keine unter Elemente.</span><span class="sxs-lookup"><span data-stu-id="63f20-264">It has no subelements.</span></span>

| <span data-ttu-id="63f20-265">Attribut</span><span class="sxs-lookup"><span data-stu-id="63f20-265">Attribute</span></span> | <span data-ttu-id="63f20-266">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="63f20-266">Description</span></span>   |
|-----------|-----------------------|
| <span data-ttu-id="63f20-267">**Id**</span><span class="sxs-lookup"><span data-stu-id="63f20-267">**Id**</span></span>    | <span data-ttu-id="63f20-268">Legen Sie das ID-Attribut auf **{e2011457-1546-43c5-a5fe-008deee3d3f0}** fest, um die Anwendung mit der Vista-Funktionalität auszuführen.</span><span class="sxs-lookup"><span data-stu-id="63f20-268">Set the Id attribute to **{e2011457-1546-43c5-a5fe-008deee3d3f0}** to run the application using Vista functionality.</span></span> <span data-ttu-id="63f20-269">Dadurch kann eine Anwendung, die für Windows Vista entwickelt wurde, unter einem späteren Betriebssystem ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="63f20-269">This can enable an application designed for Windows Vista to run on a later operating system.</span></span> <br/> <span data-ttu-id="63f20-270">Legen Sie das ID-Attribut auf **{35138b9a-5d96-4fbd-8e2d-a2440225f93a}** fest, um die Anwendung mit der Windows 7-Funktionalität auszuführen.</span><span class="sxs-lookup"><span data-stu-id="63f20-270">Set the Id attribute to **{35138b9a-5d96-4fbd-8e2d-a2440225f93a}** to run the application using Windows 7 functionality.</span></span><br/> <span data-ttu-id="63f20-271">Anwendungen, die die Funktionen Windows Vista, Windows 7 und Windows 8 unterstützen, erfordern keine separaten Manifeste.</span><span class="sxs-lookup"><span data-stu-id="63f20-271">Applications that support Windows Vista, Windows 7, and Windows 8 functionality do not require separate manifests.</span></span> <span data-ttu-id="63f20-272">Fügen Sie in diesem Fall die GUIDs für alle Windows-Betriebssysteme hinzu.</span><span class="sxs-lookup"><span data-stu-id="63f20-272">In this case, add the GUIDs for all the Windows operating systems.</span></span><br/> <span data-ttu-id="63f20-273">Informationen zum Verhalten des **ID** -Attributs in Windows finden [Sie im Cookbook Windows 8 und Windows Server 2012 Compatibility](https://www.microsoft.com/download/details.aspx?id=27416).</span><span class="sxs-lookup"><span data-stu-id="63f20-273">For info about the **Id** attribute behavior in Windows, see the [Windows 8 and Windows Server 2012 Compatibility Cookbook](https://www.microsoft.com/download/details.aspx?id=27416).</span></span><br/> <span data-ttu-id="63f20-274">Die folgenden GUIDs entsprechen den folgenden Betriebssystemen:</span><span class="sxs-lookup"><span data-stu-id="63f20-274">The following GUIDs correspond with the indicated operating systems:</span></span><br/> <span data-ttu-id="63f20-275">**{8e0f 12-bsb3-4 FE8-b9a5-48sd50a15a9a}** -> Windows 10, Windows Server 2016 und Windows Server 2019</span><span class="sxs-lookup"><span data-stu-id="63f20-275">**{8e0f7a12-bfb3-4fe8-b9a5-48fd50a15a9a}** -> Windows 10, Windows Server 2016 and Windows Server 2019</span></span><br/> <span data-ttu-id="63f20-276">**{1f676c76-80E1-4239-95bb-83d0f6d0da78}** -> Windows 8.1 und Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="63f20-276">**{1f676c76-80e1-4239-95bb-83d0f6d0da78}** -> Windows 8.1 and Windows Server 2012 R2</span></span><br/> <span data-ttu-id="63f20-277">**{4a2s28e3-53b9-4441-ba9c-d69d4a4a6e38}** -> Windows 8 und Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="63f20-277">**{4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}** -> Windows 8 and Windows Server 2012</span></span><br/> <span data-ttu-id="63f20-278">**{35138b9a-5d96-4f BD-8e2d-a2440225b93a}** -> Windows 7 und Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="63f20-278">**{35138b9a-5d96-4fbd-8e2d-a2440225f93a}** -> Windows 7 and Windows Server 2008 R2</span></span><br/> <span data-ttu-id="63f20-279">**{e2011457-1546-43c5-a5fe-008deee3d3f0}** -> Windows Vista und Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="63f20-279">**{e2011457-1546-43c5-a5fe-008deee3d3f0}** -> Windows Vista and Windows Server 2008</span></span><br/> <span data-ttu-id="63f20-280">Sie können dies unter Windows 7 oder Windows 8. x testen, indem Sie Ressourcenmonitor (resmon) ausführen, auf die Registerkarte CPU klicken, mit der rechten Maustaste auf die Spalten Bezeichnungen, "Select column..." und dann auf "Operating System Context" klicken.</span><span class="sxs-lookup"><span data-stu-id="63f20-280">You can test this on Windows 7 or Windows 8.x by running Resource Monitor (resmon), going to the CPU tab, right-clicking on the column labels, "Select Column...", and check "Operating System Context".</span></span> <span data-ttu-id="63f20-281">Unter Windows 8. x können Sie diese Spalte auch im Task-Manager (Taskmgr) finden.</span><span class="sxs-lookup"><span data-stu-id="63f20-281">On Windows 8.x, you can also find this column available in the Task Manager (taskmgr).</span></span> <span data-ttu-id="63f20-282">Der Inhalt der Spalte zeigt den höchsten gefundenen Wert oder "Windows Vista" als Standardwert an.</span><span class="sxs-lookup"><span data-stu-id="63f20-282">The content of the column shows the highest value found or "Windows Vista" as the default.</span></span> <br/> |

<span id="maxVersionTested"></span><span id="maxversiontested"></span><span id="MAXVERSIONTESTED"></span>

### <a name="maxversiontested"></a><span data-ttu-id="63f20-283">"maxversiontested"</span><span class="sxs-lookup"><span data-stu-id="63f20-283">maxversiontested</span></span>

<span data-ttu-id="63f20-284">Das **maxversiongetestete** -Element gibt die maximale Windows-Version an, für die die Anwendung getestet wurde.</span><span class="sxs-lookup"><span data-stu-id="63f20-284">The **maxversiontested** element specifies the maximum version of Windows that the application was tested against.</span></span> <span data-ttu-id="63f20-285">Diese soll von Desktop Anwendungen verwendet werden, die [XAML-Inseln](/windows/apps/desktop/modernize/xaml-islands) verwenden und nicht in einem msix-Paket bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="63f20-285">This is intended to be used by desktop applications that use [XAML Islands](/windows/apps/desktop/modernize/xaml-islands) and that are not deployed in an MSIX package.</span></span> <span data-ttu-id="63f20-286">Dieses Element wird in Windows 10, Version 1903 und höheren Versionen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="63f20-286">This element is supported in Windows 10, version 1903, and later versions.</span></span>

<span data-ttu-id="63f20-287">Das **maxversiongetestete** -Element weist das folgende Attribut auf.</span><span class="sxs-lookup"><span data-stu-id="63f20-287">The **maxversiontested** element has the following attribute.</span></span> <span data-ttu-id="63f20-288">Sie hat keine unter Elemente.</span><span class="sxs-lookup"><span data-stu-id="63f20-288">It has no subelements.</span></span>

| <span data-ttu-id="63f20-289">Attribut</span><span class="sxs-lookup"><span data-stu-id="63f20-289">Attribute</span></span> | <span data-ttu-id="63f20-290">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="63f20-290">Description</span></span>    |
|-----------|----------------|
| <span data-ttu-id="63f20-291">**Id**</span><span class="sxs-lookup"><span data-stu-id="63f20-291">**Id**</span></span>    | <span data-ttu-id="63f20-292">Legen Sie das ID-Attribut auf eine 4-teilige Versions Zeichenfolge fest, die die maximale Version von Windows angibt, mit der die Anwendung getestet wurde.</span><span class="sxs-lookup"><span data-stu-id="63f20-292">Set the Id attribute to a 4-part version string that specifies the maximum version of Windows that the application was tested against.</span></span> <span data-ttu-id="63f20-293">Beispiel: "10.0.18226.0".</span><span class="sxs-lookup"><span data-stu-id="63f20-293">For example, "10.0.18226.0".</span></span> |

<span id="dependency"></span><span id="DEPENDENCY"></span>

### <a name="dependency"></a><span data-ttu-id="63f20-294">dependency</span><span class="sxs-lookup"><span data-stu-id="63f20-294">dependency</span></span>

<span data-ttu-id="63f20-295">Enthält mindestens eine **dependentAssembly**.</span><span class="sxs-lookup"><span data-stu-id="63f20-295">Contains at least one **dependentAssembly**.</span></span> <span data-ttu-id="63f20-296">Sie besitzt keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="63f20-296">It has no attributes.</span></span> <span data-ttu-id="63f20-297">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="63f20-297">Optional.</span></span>

<span id="dependentAssembly"></span><span id="dependentassembly"></span><span id="DEPENDENTASSEMBLY"></span>

### <a name="dependentassembly"></a><span data-ttu-id="63f20-298">dependentAssembly</span><span class="sxs-lookup"><span data-stu-id="63f20-298">dependentAssembly</span></span>

<span data-ttu-id="63f20-299">Das erste Unterelement von **dependentAssembly** muss ein **assemblyIdentity** -Element sein, das eine parallele Assembly beschreibt, die für die Anwendung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="63f20-299">The first subelement of **dependentAssembly** must be an **assemblyIdentity** element that describes a side-by-side assembly required by the application.</span></span> <span data-ttu-id="63f20-300">Jede **dependentAssembly** muss sich in genau einer **Abhängigkeit** befinden.</span><span class="sxs-lookup"><span data-stu-id="63f20-300">Every **dependentAssembly** must be inside exactly one **dependency**.</span></span> <span data-ttu-id="63f20-301">Sie besitzt keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="63f20-301">It has no attributes.</span></span>

<span id="file"></span><span id="FILE"></span>

### <a name="file"></a><span data-ttu-id="63f20-302">file</span><span class="sxs-lookup"><span data-stu-id="63f20-302">file</span></span>

<span data-ttu-id="63f20-303">Gibt die Dateien an, die für die Anwendung privat sind.</span><span class="sxs-lookup"><span data-stu-id="63f20-303">Specifies files that are private to the application.</span></span> <span data-ttu-id="63f20-304">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="63f20-304">Optional.</span></span>

<span data-ttu-id="63f20-305">Das **File** -Element verfügt über die in der folgenden Tabelle aufgeführten Attribute.</span><span class="sxs-lookup"><span data-stu-id="63f20-305">The **file** element has the attributes shown in the following table.</span></span>



| <span data-ttu-id="63f20-306">Attribut</span><span class="sxs-lookup"><span data-stu-id="63f20-306">Attribute</span></span>   | <span data-ttu-id="63f20-307">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="63f20-307">Description</span></span>                                                                                             |
|-------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63f20-308">**name**</span><span class="sxs-lookup"><span data-stu-id="63f20-308">**name**</span></span>    | <span data-ttu-id="63f20-309">Der Name der Datei.</span><span class="sxs-lookup"><span data-stu-id="63f20-309">Name of the file.</span></span> <span data-ttu-id="63f20-310">Beispielsweise Comctl32.dll.</span><span class="sxs-lookup"><span data-stu-id="63f20-310">For example, Comctl32.dll.</span></span>                                                            |
| <span data-ttu-id="63f20-311">**HashAlg**</span><span class="sxs-lookup"><span data-stu-id="63f20-311">**hashalg**</span></span> | <span data-ttu-id="63f20-312">Der Algorithmus, der zum Erstellen eines Hashwerts der Datei verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="63f20-312">Algorithm used to create a hash of the file.</span></span> <span data-ttu-id="63f20-313">Dieser Wert muss SHA1 lauten.</span><span class="sxs-lookup"><span data-stu-id="63f20-313">This value should be SHA1.</span></span>                                 |
| <span data-ttu-id="63f20-314">**hash**</span><span class="sxs-lookup"><span data-stu-id="63f20-314">**hash**</span></span>    | <span data-ttu-id="63f20-315">Ein Hash der Datei, auf die nach Name verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="63f20-315">A hash of the file referred to by name.</span></span> <span data-ttu-id="63f20-316">Eine hexadezimale Zeichenfolge der Länge, abhängig vom Hash Algorithmus.</span><span class="sxs-lookup"><span data-stu-id="63f20-316">A hexadecimal string of length depending on the hash algorithm.</span></span> |

<span id="activeCodePage"></span><span id="activecodepage"></span><span id="ACTIVECODEPAGE"></span>

### <a name="activecodepage"></a><span data-ttu-id="63f20-317">activecodepage</span><span class="sxs-lookup"><span data-stu-id="63f20-317">activeCodePage</span></span>

<span data-ttu-id="63f20-318">Erzwingen Sie, dass ein Prozess UTF-8 als Prozess Codepage verwendet.</span><span class="sxs-lookup"><span data-stu-id="63f20-318">Force a process to use UTF-8 as the process code page.</span></span>

<span data-ttu-id="63f20-319">**activecodepage** wurde in Windows, Version 1903 (Mai 2019 Update) hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="63f20-319">**activeCodePage** was added in Windows Version 1903 (May 2019 Update).</span></span> <span data-ttu-id="63f20-320">Sie können diese Eigenschaft deklarieren und für frühere Windows-Builds ausführen/ausführen, aber Sie müssen die Legacy-Code Page Erkennung und-Konvertierung wie gewohnt behandeln.</span><span class="sxs-lookup"><span data-stu-id="63f20-320">You can declare this property and target/run on earlier Windows builds, but you must handle legacy code page detection and conversion as usual.</span></span> <span data-ttu-id="63f20-321">Weitere Informationen finden Sie [unter Verwenden der UTF-8-Codepage](/windows/uwp/design/globalizing/use-utf8-code-page) .</span><span class="sxs-lookup"><span data-stu-id="63f20-321">See [Use the UTF-8 code page](/windows/uwp/design/globalizing/use-utf8-code-page) for details.</span></span>

<span data-ttu-id="63f20-322">Dieses Element weist keine Attribute auf.</span><span class="sxs-lookup"><span data-stu-id="63f20-322">This element has no attributes.</span></span> <span data-ttu-id="63f20-323">**UTF-8** ist nur ein gültiger Wert für das **activecodepage** -Element.</span><span class="sxs-lookup"><span data-stu-id="63f20-323">**UTF-8** is only valid value for **activeCodePage** element.</span></span>

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

### <a name="autoelevate"></a><span data-ttu-id="63f20-324">automatische Erhöhung</span><span class="sxs-lookup"><span data-stu-id="63f20-324">autoElevate</span></span>

<span data-ttu-id="63f20-325">Gibt an, ob die automatische Erhöhung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="63f20-325">Specifies whether auto elevate is enabled.</span></span> <span data-ttu-id="63f20-326">**True** gibt an, dass es aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="63f20-326">**TRUE** indicates that it is enabled.</span></span> <span data-ttu-id="63f20-327">Sie besitzt keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="63f20-327">It has no attributes.</span></span>

<span id="disableTheming"></span><span id="disabletheming"></span><span id="DISABLETHEMING"></span>

### <a name="disabletheming"></a><span data-ttu-id="63f20-328">wird deaktiviert</span><span class="sxs-lookup"><span data-stu-id="63f20-328">disableTheming</span></span>

<span data-ttu-id="63f20-329">Gibt an, ob das Festlegen von Benutzeroberflächen Elementen ein Design deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="63f20-329">Specifies whether giving UI elements a theme is disabled.</span></span> <span data-ttu-id="63f20-330">**True** weist auf deaktiviert hin.</span><span class="sxs-lookup"><span data-stu-id="63f20-330">**TRUE** indicates disabled.</span></span> <span data-ttu-id="63f20-331">Sie besitzt keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="63f20-331">It has no attributes.</span></span>

<span id="disableWindowFiltering"></span><span id="disablewindowfiltering"></span><span id="DISABLEWINDOWFILTERING"></span>

### <a name="disablewindowfiltering"></a><span data-ttu-id="63f20-332">disablewindowfiltering</span><span class="sxs-lookup"><span data-stu-id="63f20-332">disableWindowFiltering</span></span>

<span data-ttu-id="63f20-333">Gibt an, ob die Fenster Filterung deaktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="63f20-333">Specifies whether to disable window filtering.</span></span> <span data-ttu-id="63f20-334">**True** deaktiviert die Fenster Filterung, sodass Sie die immersiven Fenster vom Desktop aufzählen können.</span><span class="sxs-lookup"><span data-stu-id="63f20-334">**TRUE** disables window filtering so you can enumerate immersive windows from the desktop.</span></span> <span data-ttu-id="63f20-335">**disablewindowfiltering** wurde in Windows 8 hinzugefügt und weist keine Attribute auf.</span><span class="sxs-lookup"><span data-stu-id="63f20-335">**disableWindowFiltering** was added in Windows 8 and has no attributes.</span></span>

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

### <a name="dpiaware"></a><span data-ttu-id="63f20-336">dpiaware</span><span class="sxs-lookup"><span data-stu-id="63f20-336">dpiAware</span></span>

<span data-ttu-id="63f20-337">Gibt an, ob der aktuelle Prozess Punkte pro Zoll (dpi) unterstützt.</span><span class="sxs-lookup"><span data-stu-id="63f20-337">Specifies whether the current process is dots per inch (dpi) aware.</span></span>

<span data-ttu-id="63f20-338">**Windows 10, Version 1607:** Das **dpiaware** -Element wird ignoriert, wenn das **dpiawareness** -Element vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="63f20-338">**Windows 10, version 1607:** The **dpiAware** element is ignored if the **dpiAwareness** element is present.</span></span> <span data-ttu-id="63f20-339">Wenn Sie ein anderes Verhalten für Windows 10, Version 1607, als für eine frühere Version des Betriebssystems angeben möchten, können Sie beide Elemente in ein Manifest einschließen.</span><span class="sxs-lookup"><span data-stu-id="63f20-339">You can include both elements in a manifest if you want to specify a different behavior for Windows 10, version 1607 than for an earlier version of the operating system.</span></span>

<span data-ttu-id="63f20-340">In der folgenden Tabelle wird das Verhalten beschrieben, das sich basierend auf dem vorhanden sein des Elements **dpiaware** und dem darin enthaltenen Text ergibt.</span><span class="sxs-lookup"><span data-stu-id="63f20-340">The following table describes the behavior that results based upon the presence of the **dpiAware** element and the text that it contains.</span></span> <span data-ttu-id="63f20-341">Bei dem Text im-Element wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="63f20-341">The text within the element is not case-sensitive.</span></span>

| <span data-ttu-id="63f20-342">Status des **dpiaware** -Elements</span><span class="sxs-lookup"><span data-stu-id="63f20-342">State of the **dpiAware** element</span></span> | <span data-ttu-id="63f20-343">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="63f20-343">Description</span></span>     |
|-----------------------------------|---------|
| <span data-ttu-id="63f20-344">„Absent“</span><span class="sxs-lookup"><span data-stu-id="63f20-344">Absent</span></span>                            | <span data-ttu-id="63f20-345">Im aktuellen Prozess ist dpi standardmäßig nicht bekannt.</span><span class="sxs-lookup"><span data-stu-id="63f20-345">The current process is dpi unaware by default.</span></span> <span data-ttu-id="63f20-346">Sie können diese Einstellung Programm gesteuert ändern, indem Sie die Funktion [**setprocessdpiawareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) oder [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="63f20-346">You can programmatically change this setting by calling the [**SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) or [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) function.</span></span>                                                                                                                                                            |
| <span data-ttu-id="63f20-347">Enthält "true"</span><span class="sxs-lookup"><span data-stu-id="63f20-347">Contains "true"</span></span>                   | <span data-ttu-id="63f20-348">Der aktuelle Prozess ist System-dpi-fähig.</span><span class="sxs-lookup"><span data-stu-id="63f20-348">The current process is system dpi aware.</span></span>                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="63f20-349">Enthält "false"</span><span class="sxs-lookup"><span data-stu-id="63f20-349">Contains "false"</span></span>                  | <span data-ttu-id="63f20-350">**Windows Vista, Windows 7 und Windows 8:** Das Verhalten ist identisch mit dem, wenn **dpiaware** nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="63f20-350">**Windows Vista, Windows 7 and Windows 8:** The behavior is the same as when the **dpiAware** is absent.</span></span><br/> <span data-ttu-id="63f20-351">**Windows 8.1 und Windows 10:** Der aktuelle Prozess ist dpi-Wert, und Sie können diese Einstellung nicht Programm gesteuert ändern, indem Sie die Funktion [**setprocessdpiawareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) oder [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="63f20-351">**Windows 8.1 and Windows 10:** The current process is dpi unaware, and you cannot programmatically change this setting by calling the [**SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) or [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) function.</span></span><br/> |
| <span data-ttu-id="63f20-352">Enthält "true/pm".</span><span class="sxs-lookup"><span data-stu-id="63f20-352">Contains "true/pm"</span></span>                | <span data-ttu-id="63f20-353">**Windows Vista, Windows 7 und Windows 8:** Der aktuelle Prozess ist System-dpi-fähig.</span><span class="sxs-lookup"><span data-stu-id="63f20-353">**Windows Vista, Windows 7 and Windows 8:** The current process is system dpi aware.</span></span><br/> <span data-ttu-id="63f20-354">**Windows 8.1 und Windows 10:** Beim aktuellen Prozess handelt es sich um einen dpi-Wert pro Monitor.</span><span class="sxs-lookup"><span data-stu-id="63f20-354">**Windows 8.1 and Windows 10:** The current process is per-monitor dpi aware.</span></span><br/>                                                                                                                                                                                                          |
| <span data-ttu-id="63f20-355">Enthält "pro Monitor"</span><span class="sxs-lookup"><span data-stu-id="63f20-355">Contains "per monitor"</span></span>            | <span data-ttu-id="63f20-356">**Windows Vista, Windows 7 und Windows 8:** Das Verhalten ist identisch mit dem, wenn **dpiaware** nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="63f20-356">**Windows Vista, Windows 7 and Windows 8:** The behavior is the same as when the **dpiAware** is absent.</span></span><br/> <span data-ttu-id="63f20-357">**Windows 8.1 und Windows 10:** Beim aktuellen Prozess handelt es sich um einen dpi-Wert pro Monitor.</span><span class="sxs-lookup"><span data-stu-id="63f20-357">**Windows 8.1 and Windows 10:** The current process is per-monitor dpi aware.</span></span><br/>                                                                                                                                                                                      |
| <span data-ttu-id="63f20-358">Enthält eine beliebige andere Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="63f20-358">Contains any other string</span></span>         | <span data-ttu-id="63f20-359">**Windows Vista, Windows 7 und Windows 8:** Das Verhalten ist identisch mit dem, wenn **dpiaware** nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="63f20-359">**Windows Vista, Windows 7 and Windows 8:** The behavior is the same as when the **dpiAware** is absent.</span></span><br/> <span data-ttu-id="63f20-360">**Windows 8.1 und Windows 10:** Der aktuelle Prozess ist dpi-Wert, und Sie können diese Einstellung nicht Programm gesteuert ändern, indem Sie die Funktion [**setprocessdpiawareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) oder [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="63f20-360">**Windows 8.1 and Windows 10:** The current process is dpi unaware, and you cannot programmatically change this setting by calling the [**SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) or [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) function.</span></span><br/> |

<span data-ttu-id="63f20-361">Weitere Informationen zu den dpi-Einstellungen finden Sie unter [Vergleich der dpi-Bekanntheits Grade](https://msdn.microsoft.com/library/windows/desktop/mt843498(v=vs.85).aspx(d=robot)).</span><span class="sxs-lookup"><span data-stu-id="63f20-361">For more information about dpi awareness settings, see [Comparison of DPI Awareness Levels](https://msdn.microsoft.com/library/windows/desktop/mt843498(v=vs.85).aspx(d=robot)).</span></span>

<span data-ttu-id="63f20-362">**dpiaware** weist keine Attribute auf.</span><span class="sxs-lookup"><span data-stu-id="63f20-362">**dpiAware** has no attributes.</span></span>

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

### <a name="dpiawareness"></a><span data-ttu-id="63f20-363">dpiawareness</span><span class="sxs-lookup"><span data-stu-id="63f20-363">dpiAwareness</span></span>

<span data-ttu-id="63f20-364">Gibt an, ob der aktuelle Prozess Punkte pro Zoll (dpi) unterstützt.</span><span class="sxs-lookup"><span data-stu-id="63f20-364">Specifies whether the current process is dots per inch (dpi) aware.</span></span>

<span data-ttu-id="63f20-365">Die Mindestversion des Betriebssystems, das das **dpiawareness** -Element unterstützt, ist Windows 10, Version 1607.</span><span class="sxs-lookup"><span data-stu-id="63f20-365">The minimum version of the operating system that supports the **dpiAwareness** element is Windows 10, version 1607.</span></span> <span data-ttu-id="63f20-366">Für Versionen, die das **dpiawareness** -Element unterstützen, überschreibt **dpiawareness** das **dpiaware** -Element.</span><span class="sxs-lookup"><span data-stu-id="63f20-366">For versions that support the **dpiAwareness** element, the **dpiAwareness** overrides the **dpiAware** element.</span></span> <span data-ttu-id="63f20-367">Wenn Sie ein anderes Verhalten für Windows 10, Version 1607, als für eine frühere Version des Betriebssystems angeben möchten, können Sie beide Elemente in ein Manifest einschließen.</span><span class="sxs-lookup"><span data-stu-id="63f20-367">You can include both elements in a manifest if you want to specify a different behavior for Windows 10, version 1607 than for an earlier version of the operating system.</span></span>

<span data-ttu-id="63f20-368">Das **dpiawareness** -Element kann ein einzelnes Element oder eine Liste mit durch Trennzeichen getrennten Elementen enthalten.</span><span class="sxs-lookup"><span data-stu-id="63f20-368">The **dpiAwareness** element can contain a single item or a list of comma-separated items.</span></span> <span data-ttu-id="63f20-369">Im letzteren Fall wird das erste (am weitesten links stehende) Element in der Liste verwendet, das vom Betriebssystem erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="63f20-369">In the latter case, the first (leftmost) item in the list recognized by the operating system is used.</span></span> <span data-ttu-id="63f20-370">Auf diese Weise können Sie verschiedene Verhalten angeben, die in zukünftigen Windows-Betriebssystemversionen unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="63f20-370">In this way, you can specify different behaviors supported in future Windows operating system versions.</span></span>

<span data-ttu-id="63f20-371">In der folgenden Tabelle wird das Verhalten beschrieben, das sich auf der Grundlage des Vorhandenseins des **dpiawareness** -Elements und des darin enthaltenen Texts in seinem am weitesten links erkannten Element ergibt.</span><span class="sxs-lookup"><span data-stu-id="63f20-371">The following table describes the behavior that results based upon the presence of the **dpiAwareness** element and the text that it contains in its leftmost recognized item.</span></span> <span data-ttu-id="63f20-372">Bei dem Text im-Element wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="63f20-372">The text within the element is not case-sensitive.</span></span>

| <span data-ttu-id="63f20-373">Status des **dpiawareness** -Elements:</span><span class="sxs-lookup"><span data-stu-id="63f20-373">**dpiAwareness** element status:</span></span>        | <span data-ttu-id="63f20-374">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="63f20-374">Description</span></span>                          |
|-----------------------------------------|-------------------------------------------|
| <span data-ttu-id="63f20-375">Das Element fehlt.</span><span class="sxs-lookup"><span data-stu-id="63f20-375">Element is absent</span></span>                       | <span data-ttu-id="63f20-376">Das **dpiaware** -Element gibt an, ob der Prozess dpi-fähig ist.</span><span class="sxs-lookup"><span data-stu-id="63f20-376">The **dpiAware** element specifies whether the process is dpi aware.</span></span>                                                                                                                                                                   |
| <span data-ttu-id="63f20-377">Enthält keine erkannten Elemente</span><span class="sxs-lookup"><span data-stu-id="63f20-377">Contains no recognized items</span></span>            | <span data-ttu-id="63f20-378">Im aktuellen Prozess ist dpi standardmäßig nicht bekannt.</span><span class="sxs-lookup"><span data-stu-id="63f20-378">The current process is dpi unaware by default.</span></span> <span data-ttu-id="63f20-379">Sie können diese Einstellung Programm gesteuert ändern, indem Sie die Funktion [**setprocessdpiawareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) oder [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="63f20-379">You can programmatically change this setting by calling the [**SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) or [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) function.</span></span> |
| <span data-ttu-id="63f20-380">Das erste erkannte Element ist "System".</span><span class="sxs-lookup"><span data-stu-id="63f20-380">First recognized item is "system"</span></span>       | <span data-ttu-id="63f20-381">Der aktuelle Prozess ist System-dpi-fähig.</span><span class="sxs-lookup"><span data-stu-id="63f20-381">The current process is system dpi aware.</span></span>                                                                                                                                                                                               |
| <span data-ttu-id="63f20-382">Das erste erkannte Element ist "permonitor".</span><span class="sxs-lookup"><span data-stu-id="63f20-382">First recognized item is "permonitor"</span></span>   | <span data-ttu-id="63f20-383">Beim aktuellen Prozess handelt es sich um einen dpi-Wert pro Monitor.</span><span class="sxs-lookup"><span data-stu-id="63f20-383">The current process is per-monitor dpi aware.</span></span>                                                                                                                                                                                          |
| <span data-ttu-id="63f20-384">Das erste erkannte Element ist "permonitorv2".</span><span class="sxs-lookup"><span data-stu-id="63f20-384">First recognized item is "permonitorv2"</span></span> | <span data-ttu-id="63f20-385">Der aktuelle Prozess verwendet den dpi-Kontext für den dpi-Kontext pro Monitor.</span><span class="sxs-lookup"><span data-stu-id="63f20-385">The current process uses the per-monitor-v2 dpi awareness context.</span></span> <span data-ttu-id="63f20-386">Dieses Element wird nur unter Windows 10, Version 1703 oder höher, erkannt.</span><span class="sxs-lookup"><span data-stu-id="63f20-386">This item will only be recognized on Windows 10 version 1703 or later.</span></span>                                                                                              |
| <span data-ttu-id="63f20-387">Das erste erkannte Element ist "nicht bekannt".</span><span class="sxs-lookup"><span data-stu-id="63f20-387">First recognized item is "unaware"</span></span>      | <span data-ttu-id="63f20-388">Beim aktuellen Prozess ist dpi nicht bekannt.</span><span class="sxs-lookup"><span data-stu-id="63f20-388">The current process is dpi unaware.</span></span> <span data-ttu-id="63f20-389">Sie **können** diese Einstellung nicht Programm gesteuert ändern, indem Sie die Funktion [**setprocessdpiawareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) oder [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="63f20-389">You **cannot** programmatically change this setting by calling the [**SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) or [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) function.</span></span>      |

<span data-ttu-id="63f20-390">Weitere Informationen zu den von diesem Element unterstützten dpi-Informationen finden Sie unter dpi-Informationen und [ \_ \_ Kontext](/windows/desktop/hidpi/dpi-awareness-context)für dpi-Informationen. [ \_ ](/windows/desktop/api/windef/ne-windef-dpi_awareness)</span><span class="sxs-lookup"><span data-stu-id="63f20-390">For more information about dpi awareness settings supported by this element, see [DPI\_AWARENESS](/windows/desktop/api/windef/ne-windef-dpi_awareness) and [DPI\_AWARENESS\_CONTEXT](/windows/desktop/hidpi/dpi-awareness-context).</span></span>

<span data-ttu-id="63f20-391">**dpiawareness** weist keine Attribute auf.</span><span class="sxs-lookup"><span data-stu-id="63f20-391">**dpiAwareness** has no attributes.</span></span>

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

### <a name="gdiscaling"></a><span data-ttu-id="63f20-392">gdiskretihl</span><span class="sxs-lookup"><span data-stu-id="63f20-392">gdiScaling</span></span>

<span data-ttu-id="63f20-393">Gibt an, ob GDI-Skalierung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="63f20-393">Specifies whether GDI scaling is enabled.</span></span> <span data-ttu-id="63f20-394">Die Mindestversion des Betriebssystems, das das **gdiscement** -Element unterstützt, ist Windows 10, Version 1703.</span><span class="sxs-lookup"><span data-stu-id="63f20-394">The minimum version of the operating system that supports the **gdiScaling** element is Windows 10 version 1703.</span></span>

<span data-ttu-id="63f20-395">Das GDI-Framework (Graphics Device Interface) kann die DPI-Skalierung auf primitive und Text pro Monitor anwenden, ohne dass Aktualisierungen an der Anwendung selbst erfolgen.</span><span class="sxs-lookup"><span data-stu-id="63f20-395">The GDI (graphics device interface) framework can apply DPI scaling to primitives and text on a per-monitor basis without updates to the application itself.</span></span> <span data-ttu-id="63f20-396">Dies kann für GDI-Anwendungen nützlich sein, die nicht mehr aktiv aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="63f20-396">This can be useful for GDI applications no longer being actively updated.</span></span>

<span data-ttu-id="63f20-397">Nicht Vektorgrafiken (z. b. Bitmaps, Symbole oder Symbolleisten) können nicht von diesem Element skaliert werden.</span><span class="sxs-lookup"><span data-stu-id="63f20-397">Non-vector graphics (such as bitmaps, icons, or toolbars) cannot be scaled by this element.</span></span> <span data-ttu-id="63f20-398">Darüber hinaus können Grafiken und Text, die in Bitmaps angezeigt werden, die dynamisch von Anwendungen erstellt werden, auch nicht von diesem Element skaliert werden.</span><span class="sxs-lookup"><span data-stu-id="63f20-398">In addition, graphics and text appearing within bitmaps dynamically constructed by applications also cannot be scaled by this element.</span></span>

<span data-ttu-id="63f20-399">**True** gibt an, dass dieses Element aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="63f20-399">**TRUE** indicates that this element is enabled.</span></span> <span data-ttu-id="63f20-400">Sie besitzt keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="63f20-400">It has no attributes.</span></span>


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

### <a name="highresolutionscrollingaware"></a><span data-ttu-id="63f20-401">highresolutionscrollingaware</span><span class="sxs-lookup"><span data-stu-id="63f20-401">highResolutionScrollingAware</span></span>

<span data-ttu-id="63f20-402">Gibt an, ob das hochauflösende Scrollen aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="63f20-402">Specifies whether high-resolution-scrolling aware is enabled.</span></span> <span data-ttu-id="63f20-403">**True** gibt an, dass es aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="63f20-403">**TRUE** indicates that it is enabled.</span></span> <span data-ttu-id="63f20-404">Sie besitzt keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="63f20-404">It has no attributes.</span></span>

<span id="longPathAware"></span><span id="longpathaware"></span><span id="LONGPATHAWARE"></span>

### <a name="longpathaware"></a><span data-ttu-id="63f20-405">longpathaware</span><span class="sxs-lookup"><span data-stu-id="63f20-405">longPathAware</span></span>

<span data-ttu-id="63f20-406">Aktiviert lange Pfade, die **MAX_PATH** Länge überschreiten.</span><span class="sxs-lookup"><span data-stu-id="63f20-406">Enables long paths that exceed **MAX_PATH** in length.</span></span> <span data-ttu-id="63f20-407">Dieses Element wird in Windows 10, Version 1607 und höher, unterstützt.</span><span class="sxs-lookup"><span data-stu-id="63f20-407">This element is supported in Windows 10, version 1607, and later.</span></span> <span data-ttu-id="63f20-408">[hier finden Sie weitere Informationen](../fileio/maximum-file-path-limitation.md)</span><span class="sxs-lookup"><span data-stu-id="63f20-408">For more information, see [this article](../fileio/maximum-file-path-limitation.md).</span></span>

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

### <a name="printerdriverisolation"></a><span data-ttu-id="63f20-409">printerdriverisolation</span><span class="sxs-lookup"><span data-stu-id="63f20-409">printerDriverIsolation</span></span>

<span data-ttu-id="63f20-410">Gibt an, ob die Druckertreiber Isolation aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="63f20-410">Specifies whether printer driver isolation is enabled.</span></span> <span data-ttu-id="63f20-411">**True** gibt an, dass es aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="63f20-411">**TRUE** indicates that it is enabled.</span></span> <span data-ttu-id="63f20-412">Sie besitzt keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="63f20-412">It has no attributes.</span></span> <span data-ttu-id="63f20-413">Die Druckertreiber Isolation verbessert die Zuverlässigkeit des Windows-Druck Diensts, indem Druckertreiber in Prozessen ausgeführt werden können, die von dem Prozess getrennt sind, in dem der Druck Spooler ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="63f20-413">Printer driver isolation improves the reliability of the Windows print service by enabling printer drivers to run in processes that are separate from the process in which the print spooler runs.</span></span> <span data-ttu-id="63f20-414">Unterstützung für die Druckertreiber Isolation in Windows 7 und Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="63f20-414">Support for printer driver isolation started in Windows 7 and Windows Server 2008 R2.</span></span> <span data-ttu-id="63f20-415">Eine APP kann die Druckertreiber Isolation in Ihrem App-Manifest deklarieren, um sich selbst vom Druckertreiber zu isolieren und seine Zuverlässigkeit zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="63f20-415">An app can declare printer driver isolation in its app manifest to isolate itself from the printer driver and improve its reliability.</span></span> <span data-ttu-id="63f20-416">Das heißt, die APP stürzt nicht ab, wenn der Druckertreiber einen Fehler aufweist.</span><span class="sxs-lookup"><span data-stu-id="63f20-416">That is, the app won't crash if the printer driver has an error.</span></span>


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

### <a name="ultrahighresolutionscrollingaware"></a><span data-ttu-id="63f20-417">ultrahighresolutionscrollingaware</span><span class="sxs-lookup"><span data-stu-id="63f20-417">ultraHighResolutionScrollingAware</span></span>

<span data-ttu-id="63f20-418">Gibt an, ob die hochauflösende Bild lauffunktion aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="63f20-418">Specifies whether ultra-high-resolution-scrolling aware is enabled.</span></span> <span data-ttu-id="63f20-419">**True** gibt an, dass es aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="63f20-419">**TRUE** indicates that it is enabled.</span></span> <span data-ttu-id="63f20-420">Sie besitzt keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="63f20-420">It has no attributes.</span></span>

<span id="msix"></span><span id="MSIX"></span>

### <a name="msix"></a><span data-ttu-id="63f20-421">MSIX</span><span class="sxs-lookup"><span data-stu-id="63f20-421">msix</span></span>

<span data-ttu-id="63f20-422">Gibt die Identitätsinformationen eines [sparsemsix-Pakets](/windows/apps/desktop/modernize/grant-identity-to-nonpackaged-apps) für die aktuelle Anwendung an.</span><span class="sxs-lookup"><span data-stu-id="63f20-422">Specifies the identity info of a [sparse MSIX package](/windows/apps/desktop/modernize/grant-identity-to-nonpackaged-apps) for the current application.</span></span> <span data-ttu-id="63f20-423">Dieses Element wird in Windows 10, Version 2004 und höheren Versionen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="63f20-423">This element is supported in Windows 10, version 2004, and later versions.</span></span>

<span data-ttu-id="63f20-424">Das **msix** -Element muss sich im-Namespace befinden `urn:schemas-microsoft-com:msix.v1` .</span><span class="sxs-lookup"><span data-stu-id="63f20-424">The **msix** element must be in the namespace `urn:schemas-microsoft-com:msix.v1`.</span></span> <span data-ttu-id="63f20-425">Die Attribute sind in der folgenden Tabelle aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="63f20-425">It has the attributes shown in the following table.</span></span>

| <span data-ttu-id="63f20-426">Attribut</span><span class="sxs-lookup"><span data-stu-id="63f20-426">Attribute</span></span>   | <span data-ttu-id="63f20-427">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="63f20-427">Description</span></span>                                                                                             |
|-------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63f20-428">**publisher**</span><span class="sxs-lookup"><span data-stu-id="63f20-428">**publisher**</span></span>    | <span data-ttu-id="63f20-429">Beschreibt die Verleger Informationen.</span><span class="sxs-lookup"><span data-stu-id="63f20-429">Describes the publisher information.</span></span> <span data-ttu-id="63f20-430">Dieser Wert muss mit dem **Verleger** Attribut im [Identity](/uwp/schemas/appxpackage/uapmanifestschema/element-identity) -Element in Ihrem Paket mit geringer Dichte identisch sein.</span><span class="sxs-lookup"><span data-stu-id="63f20-430">This value must match the **Publisher** attribute in the [Identity](/uwp/schemas/appxpackage/uapmanifestschema/element-identity) element in your sparse package manifest.</span></span> |
| <span data-ttu-id="63f20-431">**packageName**</span><span class="sxs-lookup"><span data-stu-id="63f20-431">**packageName**</span></span> | <span data-ttu-id="63f20-432">Beschreibt den Inhalt des Pakets.</span><span class="sxs-lookup"><span data-stu-id="63f20-432">Describes the contents of the package.</span></span> <span data-ttu-id="63f20-433">Dieser Wert muss mit dem **Name** -Attribut im [Identity](/uwp/schemas/appxpackage/uapmanifestschema/element-identity) -Element im Sparse-Paket Manifest identisch sein.</span><span class="sxs-lookup"><span data-stu-id="63f20-433">This value must match the **Name** attribute in the [Identity](/uwp/schemas/appxpackage/uapmanifestschema/element-identity) element in your sparse package manifest.</span></span>    |
| <span data-ttu-id="63f20-434">**applicationId**</span><span class="sxs-lookup"><span data-stu-id="63f20-434">**applicationId**</span></span>    | <span data-ttu-id="63f20-435">Der eindeutige Bezeichner der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="63f20-435">The unique identifier of the application.</span></span> <span data-ttu-id="63f20-436">Dieser Wert muss mit dem **ID** -Attribut im [Anwendungs](/uwp/schemas/appxpackage/uapmanifestschema/element-application) Element im Sparse-Paket Manifest identisch sein.</span><span class="sxs-lookup"><span data-stu-id="63f20-436">This value must match the **Id** attribute in the [Application](/uwp/schemas/appxpackage/uapmanifestschema/element-application) element in your sparse package manifest.</span></span>  |

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

### <a name="heaptype"></a><span data-ttu-id="63f20-437">heaptype</span><span class="sxs-lookup"><span data-stu-id="63f20-437">heapType</span></span>

<span data-ttu-id="63f20-438">Überschreibt die standardmäßige Heap Implementierung für die zu verwendenden [Win32-Heap-APIs](../Memory/heap-functions.md) .</span><span class="sxs-lookup"><span data-stu-id="63f20-438">Overrides the default heap implementation for the [Win32 heap APIs](../Memory/heap-functions.md) to use.</span></span>

* <span data-ttu-id="63f20-439">Der Wert **segmentheiap** gibt an, dass der Segment Heap verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="63f20-439">The value **SegmentHeap** indicates that segment heap will be used.</span></span> <span data-ttu-id="63f20-440">Der Segment Heap ist eine moderne Heap Implementierung, die in der Regel die Gesamtspeicher Auslastung reduziert.</span><span class="sxs-lookup"><span data-stu-id="63f20-440">Segment heap is a modern heap implementation that will generally reduce your overall memory usage.</span></span> <span data-ttu-id="63f20-441">Dieses Element wird in Windows 10, Version 2004 (Build 19041) und höher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="63f20-441">This element is supported in Windows 10, version 2004 (build 19041) and later.</span></span>
* <span data-ttu-id="63f20-442">Alle anderen Werte werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="63f20-442">All other values are ignored.</span></span>

<span data-ttu-id="63f20-443">Dieses Element weist keine Attribute auf.</span><span class="sxs-lookup"><span data-stu-id="63f20-443">This element has no attributes.</span></span>

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

## <a name="example"></a><span data-ttu-id="63f20-444">Beispiel</span><span class="sxs-lookup"><span data-stu-id="63f20-444">Example</span></span>

<span data-ttu-id="63f20-445">Im folgenden finden Sie ein Beispiel für ein Anwendungs Manifest für eine Anwendung mit dem Namen MySampleApp.exe.</span><span class="sxs-lookup"><span data-stu-id="63f20-445">The following is an example of an application manifest for an application named MySampleApp.exe.</span></span> <span data-ttu-id="63f20-446">Die Anwendung verwendet die parallele Assembly von SampleAssembly.</span><span class="sxs-lookup"><span data-stu-id="63f20-446">The application consumes the SampleAssembly side-by-side assembly.</span></span>

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
