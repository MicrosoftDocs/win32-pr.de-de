---
description: Eine Verleger Konfigurationsdatei ist eine XML-Datei, die Anwendungen und Assemblys global von der Verwendung einer Version einer parallelen Assembly zu einer anderen Version derselben Assembly umleitet.
ms.assetid: b10752af-80a7-4027-b525-90333d0d010a
title: Verleger Konfigurationsdateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cc5d7d7b7ffdad3d1179a7f8c66a347d91e0a03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867888"
---
# <a name="publisher-configuration-files"></a><span data-ttu-id="2dc46-103">Verleger Konfigurationsdateien</span><span class="sxs-lookup"><span data-stu-id="2dc46-103">Publisher Configuration Files</span></span>

<span data-ttu-id="2dc46-104">Eine Verleger Konfigurationsdatei ist eine XML-Datei, die Anwendungen und Assemblys global von der Verwendung einer Version einer parallelen Assembly zu einer anderen Version derselben Assembly umleitet.</span><span class="sxs-lookup"><span data-stu-id="2dc46-104">A publisher configuration file is an XML file that globally redirects applications and assemblies from using one version of a side-by-side assembly to another version of the same assembly.</span></span> <span data-ttu-id="2dc46-105">In der Regel gibt der Verleger der Assembly ein kompatibles Update oder eine Sicherheitskorrektur pro Assembly aus, indem eine zu installierende Verleger Konfigurationsdatei zusammen mit einem Service Pack Update ausgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="2dc46-105">Typically, the publisher of the assembly issues a compatible update or security fix on a per-assembly basis by issuing a publisher configuration file to be installed along with a service pack update.</span></span> <span data-ttu-id="2dc46-106">Dies wird als [Verleger Konfiguration](publisher-configuration.md)bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="2dc46-106">This is referred to as [publisher configuration](publisher-configuration.md).</span></span> <span data-ttu-id="2dc46-107">Weitere Informationen zu diesem [Konfigurationstyp](configuration.md) finden Sie unter Verleger Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="2dc46-107">For more information about this type of [configuration](configuration.md) see Publisher Configuration.</span></span>

<span data-ttu-id="2dc46-108">Die Verleger Konfigurationsdateien haben die folgenden Elemente und Attribute.</span><span class="sxs-lookup"><span data-stu-id="2dc46-108">Publisher configuration files have the following elements and attributes.</span></span> <span data-ttu-id="2dc46-109">Eine umfassende Liste des XML-Schemas finden Sie unter [Schema der Verleger Konfigurationsdatei](publisher-configuration-file-schema.md).</span><span class="sxs-lookup"><span data-stu-id="2dc46-109">For a complete listing of the XML schema, see [Publisher Configuration File Schema](publisher-configuration-file-schema.md).</span></span>



| <span data-ttu-id="2dc46-110">Element</span><span class="sxs-lookup"><span data-stu-id="2dc46-110">Element</span></span>               | <span data-ttu-id="2dc46-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="2dc46-111">Attributes</span></span>                | <span data-ttu-id="2dc46-112">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="2dc46-112">Required</span></span> |
|-----------------------|---------------------------|----------|
| <span data-ttu-id="2dc46-113">**Stadtverordneten**</span><span class="sxs-lookup"><span data-stu-id="2dc46-113">**assembly**</span></span>          |                           | <span data-ttu-id="2dc46-114">Ja</span><span class="sxs-lookup"><span data-stu-id="2dc46-114">Yes</span></span>      |
|                       | <span data-ttu-id="2dc46-115">**manifestVersion**</span><span class="sxs-lookup"><span data-stu-id="2dc46-115">**manifestVersion**</span></span>       | <span data-ttu-id="2dc46-116">Ja</span><span class="sxs-lookup"><span data-stu-id="2dc46-116">Yes</span></span>      |
| <span data-ttu-id="2dc46-117">**AssemblyIdentity**</span><span class="sxs-lookup"><span data-stu-id="2dc46-117">**assemblyIdentity**</span></span>  |                           | <span data-ttu-id="2dc46-118">Ja</span><span class="sxs-lookup"><span data-stu-id="2dc46-118">Yes</span></span>      |
|                       | <span data-ttu-id="2dc46-119">**type**</span><span class="sxs-lookup"><span data-stu-id="2dc46-119">**type**</span></span>                  | <span data-ttu-id="2dc46-120">Ja</span><span class="sxs-lookup"><span data-stu-id="2dc46-120">Yes</span></span>      |
|                       | <span data-ttu-id="2dc46-121">**name**</span><span class="sxs-lookup"><span data-stu-id="2dc46-121">**name**</span></span>                  | <span data-ttu-id="2dc46-122">Ja</span><span class="sxs-lookup"><span data-stu-id="2dc46-122">Yes</span></span>      |
|                       | <span data-ttu-id="2dc46-123">**language**</span><span class="sxs-lookup"><span data-stu-id="2dc46-123">**language**</span></span>              | <span data-ttu-id="2dc46-124">Nein</span><span class="sxs-lookup"><span data-stu-id="2dc46-124">No</span></span>       |
|                       | <span data-ttu-id="2dc46-125">**processorArchitecture**</span><span class="sxs-lookup"><span data-stu-id="2dc46-125">**processorArchitecture**</span></span> | <span data-ttu-id="2dc46-126">Nein</span><span class="sxs-lookup"><span data-stu-id="2dc46-126">No</span></span>       |
|                       | <span data-ttu-id="2dc46-127">**version**</span><span class="sxs-lookup"><span data-stu-id="2dc46-127">**version**</span></span>               | <span data-ttu-id="2dc46-128">Ja</span><span class="sxs-lookup"><span data-stu-id="2dc46-128">Yes</span></span>      |
|                       | <span data-ttu-id="2dc46-129">**PublicKeyToken**</span><span class="sxs-lookup"><span data-stu-id="2dc46-129">**publicKeyToken**</span></span>        | <span data-ttu-id="2dc46-130">Nein</span><span class="sxs-lookup"><span data-stu-id="2dc46-130">No</span></span>       |
| <span data-ttu-id="2dc46-131">**gkeit**</span><span class="sxs-lookup"><span data-stu-id="2dc46-131">**dependency**</span></span>        |                           | <span data-ttu-id="2dc46-132">Nein</span><span class="sxs-lookup"><span data-stu-id="2dc46-132">No</span></span>       |
| <span data-ttu-id="2dc46-133">**dependentAssembly**</span><span class="sxs-lookup"><span data-stu-id="2dc46-133">**dependentAssembly**</span></span> |                           | <span data-ttu-id="2dc46-134">Nein</span><span class="sxs-lookup"><span data-stu-id="2dc46-134">No</span></span>       |
| <span data-ttu-id="2dc46-135">**bindingRedirect**</span><span class="sxs-lookup"><span data-stu-id="2dc46-135">**bindingRedirect**</span></span>   |                           | <span data-ttu-id="2dc46-136">Ja</span><span class="sxs-lookup"><span data-stu-id="2dc46-136">Yes</span></span>      |
|                       | <span data-ttu-id="2dc46-137">**OldVersion**</span><span class="sxs-lookup"><span data-stu-id="2dc46-137">**oldVersion**</span></span>            | <span data-ttu-id="2dc46-138">Ja</span><span class="sxs-lookup"><span data-stu-id="2dc46-138">Yes</span></span>      |
|                       | <span data-ttu-id="2dc46-139">**NewVersion**</span><span class="sxs-lookup"><span data-stu-id="2dc46-139">**newVersion**</span></span>            | <span data-ttu-id="2dc46-140">Ja</span><span class="sxs-lookup"><span data-stu-id="2dc46-140">Yes</span></span>      |



 

## <a name="file-location"></a><span data-ttu-id="2dc46-141">Dateispeicherort</span><span class="sxs-lookup"><span data-stu-id="2dc46-141">File Location</span></span>

<span data-ttu-id="2dc46-142">Die Verleger Konfigurationsdateien müssen im Ordner WinSxS installiert sein.</span><span class="sxs-lookup"><span data-stu-id="2dc46-142">Publisher configuration files must be installed in the WinSxS folder.</span></span> <span data-ttu-id="2dc46-143">Sie werden normalerweise als separate Datei installiert, aber Verleger Konfigurationsdateien können auch als Ressource in eine DLL eingeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="2dc46-143">They are commonly installed as a separate file but publisher configuration files can also be included as a resource in a DLL.</span></span> <span data-ttu-id="2dc46-144">Eine Verleger Konfigurationsdatei kann nicht als Ressource in eine exe-Datei eingeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="2dc46-144">A publisher configuration file cannot be included as a resource in an EXE file.</span></span> <span data-ttu-id="2dc46-145">Eine exe-Datei kann ein [Anwendungs Manifest](application-manifests.md) als Ressource enthalten.</span><span class="sxs-lookup"><span data-stu-id="2dc46-145">An EXE file may include an [application manifest](application-manifests.md) as a resource.</span></span>

## <a name="file-name-syntax"></a><span data-ttu-id="2dc46-146">Dateinamensyntax</span><span class="sxs-lookup"><span data-stu-id="2dc46-146">File Name Syntax</span></span>

<span data-ttu-id="2dc46-147">Der Dateiname einer Verleger Konfigurationsdatei hat die Formular *Richtlinie*. *Haupt* Version. *neben* Version. *AssemblyName* , wobei " *Major* " und " *Minor* " auf die Haupt-und neben Teile der Assemblyversion verweisen, die betroffen ist. [](assembly-versions.md)</span><span class="sxs-lookup"><span data-stu-id="2dc46-147">The file name of a publisher configuration file has the form *policy*.*major*.*minor*.*assemblyname* where *major* and *minor* refer to the major and minor parts of the [assembly version](assembly-versions.md) that is being affected.</span></span> <span data-ttu-id="2dc46-148">*AssemblyName* verweist auf den Namen der Assembly.</span><span class="sxs-lookup"><span data-stu-id="2dc46-148">The *assemblyname* refers to the name of the assembly.</span></span>

<span data-ttu-id="2dc46-149">Eine Verleger Konfigurationsdatei für Version 6,0 der Microsoft. Windows. Common-Controls-Assembly hätte z. b. den folgenden Namen:</span><span class="sxs-lookup"><span data-stu-id="2dc46-149">For example, a publisher configuration file for version 6.0 of the Microsoft.Windows.Common-Controls assembly would have the following name:</span></span>

<dl> <span data-ttu-id="2dc46-150">Policy. 6.0. Microsoft. Windows. Common-Controls</span><span class="sxs-lookup"><span data-stu-id="2dc46-150">policy.6.0.Microsoft.Windows.Common-Controls</span></span>  
</dl>

<span data-ttu-id="2dc46-151">Verwenden Sie keine Richtlinien Konfigurationsdateien, um die Haupt-oder neben Version einer Assembly zu erhöhen.</span><span class="sxs-lookup"><span data-stu-id="2dc46-151">Do not use policy configuration files to increment the major or minor version of an assembly.</span></span> <span data-ttu-id="2dc46-152">Umleiten Sie z. b. Version 6.0.0.0 nicht zu 7.0.0.0 oder 6.1.0.0.</span><span class="sxs-lookup"><span data-stu-id="2dc46-152">For example, do not redirect version 6.0.0.0 to 7.0.0.0 or 6.1.0.0.</span></span> <span data-ttu-id="2dc46-153">Wenn eine Anwendung auf eine Assemblyversion, z. b. 6.0.0.0, verweist, prüft parallel, ob Richtlinien Konfigurationsdateien mit den angegebenen Haupt-und neben Versionen vorhanden sind, z. b. 6,0.</span><span class="sxs-lookup"><span data-stu-id="2dc46-153">When an application references an assembly version, such as 6.0.0.0, side-by-side checks for the presence of any policy configuration files with the specified major and minor versions, e.g. 6.0.</span></span> <span data-ttu-id="2dc46-154">Die Anwendung wird dann an eine andere Version der Assembly umgeleitet, z. b. 6.0.1.0.</span><span class="sxs-lookup"><span data-stu-id="2dc46-154">The application is then redirected to another version of the assembly, for example 6.0.1.0.</span></span> <span data-ttu-id="2dc46-155">Wenn eine Verleger Konfigurationsdatei die Haupt-oder neben Version einer Assembly Inkremente erhöht, müssen bei der nachfolgenden Umleitung der Assembly möglicherweise mehrere Richtlinien Konfigurationsdateien ausgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="2dc46-155">If a publisher configuration file increments the major or minor version of an assembly, subsequent redirection of the assembly may require issuing multiple policy configuration files.</span></span>

## <a name="elements"></a><span data-ttu-id="2dc46-156">Elemente</span><span class="sxs-lookup"><span data-stu-id="2dc46-156">Elements</span></span>

<dl> <dt>

<span data-ttu-id="2dc46-157"><span id="assembly"></span><span id="ASSEMBLY"></span>**Stadtverordneten**</span><span class="sxs-lookup"><span data-stu-id="2dc46-157"><span id="assembly"></span><span id="ASSEMBLY"></span>**assembly**</span></span>
</dt> <dd>

<span data-ttu-id="2dc46-158">Ein Containerelement.</span><span class="sxs-lookup"><span data-stu-id="2dc46-158">A container element.</span></span> <span data-ttu-id="2dc46-159">Das erste untergeordnete Element muss eine **assemblyIdentity** sein.</span><span class="sxs-lookup"><span data-stu-id="2dc46-159">Its first subelement must be an **assemblyIdentity**.</span></span> <span data-ttu-id="2dc46-160">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="2dc46-160">Required.</span></span>

<span data-ttu-id="2dc46-161">Das Assembly-Element muss sich im Namespace **urn: Schemas-Microsoft-com: ASM. v1** befinden.</span><span class="sxs-lookup"><span data-stu-id="2dc46-161">The assembly element must be in the namespace **urn:schemas-microsoft-com:asm.v1**.</span></span> <span data-ttu-id="2dc46-162">Untergeordnete Elemente der Assembly müssen sich ebenfalls in diesem Namespace befinden, durch Vererbung oder durch Tagging.</span><span class="sxs-lookup"><span data-stu-id="2dc46-162">Child elements of the assembly must also be in this namespace, by inheritance or by tagging.</span></span>

<span data-ttu-id="2dc46-163">Das **Assembly** -Element weist die folgenden Attribute auf.</span><span class="sxs-lookup"><span data-stu-id="2dc46-163">The **assembly** element has the following attributes.</span></span>



| <span data-ttu-id="2dc46-164">Attribut</span><span class="sxs-lookup"><span data-stu-id="2dc46-164">Attribute</span></span>           | <span data-ttu-id="2dc46-165">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2dc46-165">Description</span></span>                                           |
|---------------------|-------------------------------------------------------|
| <span data-ttu-id="2dc46-166">**manifestVersion**</span><span class="sxs-lookup"><span data-stu-id="2dc46-166">**manifestVersion**</span></span> | <span data-ttu-id="2dc46-167">Das **manifestVersion** -Attribut muss auf 1,0 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="2dc46-167">The **manifestVersion** attribute must be set to 1.0.</span></span> |



 

</dd> <dt>

<span data-ttu-id="2dc46-168"><span id="assemblyIdentity"></span><span id="assemblyidentity"></span><span id="ASSEMBLYIDENTITY"></span>**AssemblyIdentity**</span><span class="sxs-lookup"><span data-stu-id="2dc46-168"><span id="assemblyIdentity"></span><span id="assemblyidentity"></span><span id="ASSEMBLYIDENTITY"></span>**assemblyIdentity**</span></span>
</dt> <dd>

<span data-ttu-id="2dc46-169">Beschreibt eine parallele Assembly und identifiziert diese eindeutig.</span><span class="sxs-lookup"><span data-stu-id="2dc46-169">Describes and uniquely identifies a side-by-side assembly.</span></span>

<span data-ttu-id="2dc46-170">Als erstes Unterelement eines **Assemblyelements beschreibt die assemblyIdentity** die parallele Assembly, für die mindestens **eine Assembly-** Abhängigkeit geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="2dc46-170">As the first subelement of an **assembly** element, the **assemblyIdentity** describes the side-by-side assembly that is having one or more of its assembly dependencies changed.</span></span> <span data-ttu-id="2dc46-171">Die Verleger Konfigurationsdatei leitet die Abhängigkeiten der identifizierten Assembly um.</span><span class="sxs-lookup"><span data-stu-id="2dc46-171">The publisher configuration file redirects the dependencies of the assembly identified.</span></span> <span data-ttu-id="2dc46-172">Beispielsweise gibt die folgende **assemblyIdentity** an, dass sich die Verleger Konfigurationsdatei auf die Abhängigkeiten der x86-Assembly Microsoft. Windows. Pop 6.0.0.0 auswirkt.</span><span class="sxs-lookup"><span data-stu-id="2dc46-172">For example, the following **assemblyIdentity** indicates that the publisher configuration file affects the dependencies of the x86 Microsoft.Windows.Pop 6.0.0.0 assembly.</span></span>

``` syntax
<assemblyIdentity 
     type="win32-policy" 
     publicKeyToken="0000000000000000" 
     name="policy.6.0.Microsoft.Windows.Pop" 
     version="2.1.0.0" 
     processorArchitecture="x86"/>
```

<span data-ttu-id="2dc46-173">Als erstes Unterelement eines **dependentAssembly** -Elements beschreibt **assemblyIdentity eine parallele Assemblyabhängigkeit** .</span><span class="sxs-lookup"><span data-stu-id="2dc46-173">As the first subelement of a **dependentAssembly** element, **assemblyIdentity** describes a side-by-side assembly dependency.</span></span> <span data-ttu-id="2dc46-174">Die Verleger Konfigurationsdatei konfiguriert die Identität dieser erforderlichen parallelen Assembly neu.</span><span class="sxs-lookup"><span data-stu-id="2dc46-174">The publisher configuration file reconfigures the identity of this required side-by-side assembly.</span></span> <span data-ttu-id="2dc46-175">Die Änderung wird in einem **bindingRedirect**-Wert angegeben.</span><span class="sxs-lookup"><span data-stu-id="2dc46-175">The change is specified in a **bindingRedirect**.</span></span> <span data-ttu-id="2dc46-176">Beispielsweise wird durch die folgende **assemblyIdentity** jede Abhängigkeit von Microsoft. Windows. SampleAssembly Version 2.0.0.0 in eine Abhängigkeit von Microsoft. Windows. SampleAssembly Version 2.0.1.0 geändert.</span><span class="sxs-lookup"><span data-stu-id="2dc46-176">For example, the following **assemblyIdentity** changes any dependency on Microsoft.Windows.SampleAssembly version 2.0.0.0 to a dependency on Microsoft.Windows.SampleAssembly version 2.0.1.0.</span></span>

``` syntax
<dependency>
      <dependentAssembly>
         <assemblyIdentity 
type="win32" 
name="Microsoft.Windows.SampleAssembly"  
processorArchitecture="x86"
publicKeyToken="0000000000000000"/>
         <bindingRedirect oldVersion="2.0.0.0" newVersion="2.0.1.0"/>
      </dependentAssembly>
</dependency>
```

<span data-ttu-id="2dc46-177">Das **assemblyIdentity** -Element verfügt über die folgenden Attribute.</span><span class="sxs-lookup"><span data-stu-id="2dc46-177">The **assemblyIdentity** element has the following attributes.</span></span> <span data-ttu-id="2dc46-178">Sie verfügt über keine untergeordneten Elemente.</span><span class="sxs-lookup"><span data-stu-id="2dc46-178">It has no sub-elements.</span></span>



| <span data-ttu-id="2dc46-179">Attribut</span><span class="sxs-lookup"><span data-stu-id="2dc46-179">Attribute</span></span>                 | <span data-ttu-id="2dc46-180">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2dc46-180">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2dc46-181">**type**</span><span class="sxs-lookup"><span data-stu-id="2dc46-181">**type**</span></span>                  | <span data-ttu-id="2dc46-182">Gibt den Assemblytyp an.</span><span class="sxs-lookup"><span data-stu-id="2dc46-182">Specifies the assembly type.</span></span> <span data-ttu-id="2dc46-183">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="2dc46-183">Required.</span></span> <span data-ttu-id="2dc46-184">In der **assemblyIdentity** für die betroffene Assembly muss der Wert des **Type** -Attributs auf Win32-Policy festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="2dc46-184">In the **assemblyIdentity** for the assembly being affected, the value of the **type** attribute must be set to win32-policy.</span></span> <span data-ttu-id="2dc46-185">Der Wert Win32-Policy muss in Kleinbuchstaben angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="2dc46-185">The value win32-policy must be in all lowercase letters.</span></span><br/> <span data-ttu-id="2dc46-186">In der **assemblyIdentity für die veränderliche Assemblyabhängigkeit** muss der Wert des **Type** -Attributs auf Win32 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="2dc46-186">In the **assemblyIdentity** for the changing assembly dependency, the value of the **type** attribute must be set to win32.</span></span> <span data-ttu-id="2dc46-187">Der Wert Win32 muss in Kleinbuchstaben angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="2dc46-187">The value win32 must be in all lowercase letters.</span></span><br/>                                                                                                                                                                                                             |
| <span data-ttu-id="2dc46-188">**name**</span><span class="sxs-lookup"><span data-stu-id="2dc46-188">**name**</span></span>                  | <span data-ttu-id="2dc46-189">Benennt eine Assembly eindeutig.</span><span class="sxs-lookup"><span data-stu-id="2dc46-189">Uniquely names an assembly.</span></span> <span data-ttu-id="2dc46-190">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="2dc46-190">Required.</span></span> <span data-ttu-id="2dc46-191">In der **assemblyIdentity** für die betroffene Assembly weist Name die Formular *Richtlinie* auf. *Haupt* Version. *neben* Version. *AssemblyName* , wobei " *Major* " und " *Minor* " auf die Haupt-und neben Teile der Assemblyversion verweisen. [](assembly-versions.md)</span><span class="sxs-lookup"><span data-stu-id="2dc46-191">In the **assemblyIdentity** for the assembly being affected, name has the form *policy*.*major*.*minor*.*assemblyname* where *major* and *minor* refer to the major and minor parts of the [assembly version](assembly-versions.md).</span></span><br/> <span data-ttu-id="2dc46-192">In der **assemblyIdentity für die veränderliche Assemblyabhängigkeit** hat der Name das Format Organization.Division.Name.</span><span class="sxs-lookup"><span data-stu-id="2dc46-192">In the **assemblyIdentity** for the changing assembly dependency, name has the form Organization.Division.Name.</span></span> <span data-ttu-id="2dc46-193">Beispiel: Microsoft. Windows. MySampleApp.</span><span class="sxs-lookup"><span data-stu-id="2dc46-193">For example, Microsoft.Windows.MysampleApp.</span></span><br/>                                                                                                                                                                                 |
| <span data-ttu-id="2dc46-194">**language**</span><span class="sxs-lookup"><span data-stu-id="2dc46-194">**language**</span></span>              | <span data-ttu-id="2dc46-195">Gibt die Sprache der Assembly an.</span><span class="sxs-lookup"><span data-stu-id="2dc46-195">Identifies the language of the assembly.</span></span> <span data-ttu-id="2dc46-196">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="2dc46-196">Optional.</span></span> <span data-ttu-id="2dc46-197">Geben Sie in der **assemblyIdentity** für die betroffene Assembly den DHTML-Sprachcode an, wenn die Assembly sprachspezifisch ist.</span><span class="sxs-lookup"><span data-stu-id="2dc46-197">In the **assemblyIdentity** for the assembly being affected, if the assembly is language-specific, specify the DHTML language code.</span></span> <span data-ttu-id="2dc46-198">Wenn die Assembly für die weltweite Verwendung (Sprachneutral) verwendet wird, lassen Sie dieses Attribut aus.</span><span class="sxs-lookup"><span data-stu-id="2dc46-198">If the assembly is for worldwide use (language neutral), omit this attribute.</span></span><br/> <span data-ttu-id="2dc46-199">Geben Sie in der **assemblyIdentity für die Änderung der Assemblyabhängigkeit** , wenn die Assembly sprachspezifisch ist, den Code der DHTML-Sprache an.</span><span class="sxs-lookup"><span data-stu-id="2dc46-199">In the **assemblyIdentity** for the changing assembly dependency, if the assembly is language-specific, specify the DHTML language code.</span></span> <span data-ttu-id="2dc46-200">Wenn die Assembly für den weltweiten Gebrauch (Sprachneutral) verwendet wird, legen Sie den Wert auf " \* " fest.</span><span class="sxs-lookup"><span data-stu-id="2dc46-200">If the assembly is for worldwide use (language neutral) set the value as "\*".</span></span><br/>                                                                                                                            |
| <span data-ttu-id="2dc46-201">**processorArchitecture**</span><span class="sxs-lookup"><span data-stu-id="2dc46-201">**processorArchitecture**</span></span> | <span data-ttu-id="2dc46-202">Gibt den Prozessor an, auf dem die Anwendung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2dc46-202">Specifies the processor running the application.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="2dc46-203">**version**</span><span class="sxs-lookup"><span data-stu-id="2dc46-203">**version**</span></span>               | <span data-ttu-id="2dc46-204">Gibt die Assemblyversion an.</span><span class="sxs-lookup"><span data-stu-id="2dc46-204">Specifies the assembly version.</span></span> <span data-ttu-id="2dc46-205">Verwenden Sie die vierteilige Versions Syntax: mmmm. nnnn. oooo. pppp</span><span class="sxs-lookup"><span data-stu-id="2dc46-205">Use four-part version syntax: mmmm.nnnn.oooo.pppp</span></span> <span data-ttu-id="2dc46-206">Nur in der "Def-Context"- **Assemblyidentität** erforderlich.</span><span class="sxs-lookup"><span data-stu-id="2dc46-206">Required only in the DEF-context **assemblyIdentity**.</span></span> <span data-ttu-id="2dc46-207">Geben Sie das Versions Attribut nicht in der Ref-Context- **Assemblyidentität** an.</span><span class="sxs-lookup"><span data-stu-id="2dc46-207">Do not specify the version attribute in the REF-context **assemblyIdentity**.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="2dc46-208">**PublicKeyToken**</span><span class="sxs-lookup"><span data-stu-id="2dc46-208">**publicKeyToken**</span></span>        | <span data-ttu-id="2dc46-209">Eine hexadezimale Zeichenfolge mit 16 Zeichen, die die letzten 8 Bytes des SHA-1-Hashs des öffentlichen Schlüssels darstellt, unter dem die Assembly signiert ist.</span><span class="sxs-lookup"><span data-stu-id="2dc46-209">A 16-character hexadecimal string representing the last 8 bytes of the SHA-1 hash of the public key under which the assembly is signed.</span></span> <span data-ttu-id="2dc46-210">Der öffentliche Schlüssel, der zum Signieren des Katalogs verwendet wird, muss 2048 Bit oder größer sein.</span><span class="sxs-lookup"><span data-stu-id="2dc46-210">The public key used to sign the catalog must be 2048 bits or greater.</span></span> <span data-ttu-id="2dc46-211">Ein PublicKeyToken ist für alle freigegebenen parallelen Assemblys erforderlich.</span><span class="sxs-lookup"><span data-stu-id="2dc46-211">A publicKeyToken is required for all shared side-by-side assemblies.</span></span> <span data-ttu-id="2dc46-212">Das für die Verleger Konfigurationsdatei verwendete PublicKeyToken muss der gleiche Schlüssel sein, der für die signierte Assembly verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="2dc46-212">The publicKeyToken used for the publisher configuration file should be the same key used for the signed assembly.</span></span> <span data-ttu-id="2dc46-213">Die Verleger Konfigurationsdateien können mit denselben Tools signiert werden, [die auch mit](assembly-signing-example.md) Assemblys verwendet werden [](creating-signed-files-and-catalogs.md)</span><span class="sxs-lookup"><span data-stu-id="2dc46-213">Publisher configuration files can be signed using the same tools as used with assemblies, see [Assembly Signing Example](assembly-signing-example.md) and [Creating Signed Files and Catalogs](creating-signed-files-and-catalogs.md).</span></span> |



 

</dd> <dt>

<span data-ttu-id="2dc46-214"><span id="dependency"></span><span id="DEPENDENCY"></span>**gkeit**</span><span class="sxs-lookup"><span data-stu-id="2dc46-214"><span id="dependency"></span><span id="DEPENDENCY"></span>**dependency**</span></span>
</dt> <dd>

<span data-ttu-id="2dc46-215">Ein optionales Containerelement für mindestens eine **dependentAssembly**.</span><span class="sxs-lookup"><span data-stu-id="2dc46-215">An optional container element for at least one **dependentAssembly**.</span></span> <span data-ttu-id="2dc46-216">Sie besitzt keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="2dc46-216">It has no attributes.</span></span>

</dd> <dt>

<span data-ttu-id="2dc46-217"><span id="dependentAssembly"></span><span id="dependentassembly"></span><span id="DEPENDENTASSEMBLY"></span>**dependentAssembly**</span><span class="sxs-lookup"><span data-stu-id="2dc46-217"><span id="dependentAssembly"></span><span id="dependentassembly"></span><span id="DEPENDENTASSEMBLY"></span>**dependentAssembly**</span></span>
</dt> <dd>

<span data-ttu-id="2dc46-218">Jede **dependentAssembly** muss sich in genau einer **Abhängigkeit** befinden.</span><span class="sxs-lookup"><span data-stu-id="2dc46-218">Every **dependentAssembly** must be inside exactly one **dependency**.</span></span> <span data-ttu-id="2dc46-219">Eine **dependentAssembly** weist keine Attribute auf.</span><span class="sxs-lookup"><span data-stu-id="2dc46-219">A **dependentAssembly** has no attributes.</span></span> <span data-ttu-id="2dc46-220">Das erste untergeordnete Element von **dependentAssembly** muss eine **assemblyIdentity** sein, damit die parallele Assembly von der Verleger Konfiguration neu konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="2dc46-220">The first subelement of **dependentAssembly** must be an **assemblyIdentity** for the side-by-side assembly being reconfigured by the publisher configuration.</span></span>

</dd> <dt>

<span data-ttu-id="2dc46-221"><span id="bindingRedirect"></span><span id="bindingredirect"></span><span id="BINDINGREDIRECT"></span>**bindingRedirect**</span><span class="sxs-lookup"><span data-stu-id="2dc46-221"><span id="bindingRedirect"></span><span id="bindingredirect"></span><span id="BINDINGREDIRECT"></span>**bindingRedirect**</span></span>
</dt> <dd>

<span data-ttu-id="2dc46-222">Das **bindingRedirect** -Element enthält Umleitungs Informationen für die Bindung der Assembly.</span><span class="sxs-lookup"><span data-stu-id="2dc46-222">The **bindingRedirect** element contains redirection information for the binding of the assembly.</span></span>

<span data-ttu-id="2dc46-223">Dieses Element verfügt über die in der folgenden Tabelle aufgeführten Attribute.</span><span class="sxs-lookup"><span data-stu-id="2dc46-223">This element has the attributes shown in the following table.</span></span>



| <span data-ttu-id="2dc46-224">Attribut</span><span class="sxs-lookup"><span data-stu-id="2dc46-224">Attribute</span></span>      | <span data-ttu-id="2dc46-225">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2dc46-225">Description</span></span>                                                                                                                                                                                                                           |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2dc46-226">**OldVersion**</span><span class="sxs-lookup"><span data-stu-id="2dc46-226">**oldVersion**</span></span> | <span data-ttu-id="2dc46-227">Gibt die Assemblyversion an, die überschrieben und umgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="2dc46-227">Specifies the assembly version being overridden and redirected.</span></span> <span data-ttu-id="2dc46-228">Verwenden Sie die vierteilige Versions Syntax nnnnn. nnnnn. nnnnn. nnnnn.</span><span class="sxs-lookup"><span data-stu-id="2dc46-228">Use the four-part version syntax nnnnn.nnnnn.nnnnn.nnnnn.</span></span> <span data-ttu-id="2dc46-229">Geben Sie einen Bereich von Versionen durch einen Bindestrich ohne Leerzeichen an.</span><span class="sxs-lookup"><span data-stu-id="2dc46-229">Specify a range of versions by a dash with no spaces.</span></span> <span data-ttu-id="2dc46-230">Beispielsweise 2.14.3.0 oder 2.14.3.0 2.16.0.0.</span><span class="sxs-lookup"><span data-stu-id="2dc46-230">For example, 2.14.3.0 or 2.14.3.0 2.16.0.0.</span></span> <span data-ttu-id="2dc46-231">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="2dc46-231">Required.</span></span> |
| <span data-ttu-id="2dc46-232">**NewVersion**</span><span class="sxs-lookup"><span data-stu-id="2dc46-232">**newVersion**</span></span> | <span data-ttu-id="2dc46-233">Gibt die Version der Ersetzungs-Assembly an.</span><span class="sxs-lookup"><span data-stu-id="2dc46-233">Specifies the replacement assembly version.</span></span> <span data-ttu-id="2dc46-234">Verwenden Sie die vierteilige Versions Syntax nnnnn. nnnnn. nnnnn. nnnnn.</span><span class="sxs-lookup"><span data-stu-id="2dc46-234">Use four-part version syntax nnnnn.nnnnn.nnnnn.nnnnn.</span></span>                                                                                                                                     |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2dc46-235">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2dc46-235">Remarks</span></span>

<span data-ttu-id="2dc46-236">In den Verleger Konfigurationsdateien werden keine Dateien angegeben.</span><span class="sxs-lookup"><span data-stu-id="2dc46-236">Publisher configuration files do not specify files.</span></span> <span data-ttu-id="2dc46-237">Beachten Sie, dass sprachspezifische Richtlinien Dateien von der Verleger Konfigurationsdatei getrennt sind.</span><span class="sxs-lookup"><span data-stu-id="2dc46-237">Note that language-specific policy files are separate from the publisher configuration file.</span></span>

## <a name="example"></a><span data-ttu-id="2dc46-238">Beispiel</span><span class="sxs-lookup"><span data-stu-id="2dc46-238">Example</span></span>

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
<assemblyIdentity type="win32-policy" publicKeyToken="0000000000000000" name="policy.6.0.Proseware.Research.SampleAssembly" version="1.0.1.0" language="en-us" processorArchitecture="x86"/>
<dependency>
<dependentAssembly>
<assemblyIdentity type="win32" publicKeyToken="0000000000000000" name="Proseware.Research.SampleAssembly" language="en-us" processorArchitecture="x86"/>
<bindingRedirect oldVersion="1.0.0.0" newVersion="1.0.1.0"/>
</dependentAssembly>
</dependency>
</assembly>
```

 

 




