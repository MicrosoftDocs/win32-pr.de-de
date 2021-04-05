---
description: Wenn Sie möchten, dass Benutzer Ihrer Anwendung bzw. Kern-dll die Sprache der Benutzeroberfläche ändern können, sollten Sie erwägen, Sprachressourcen in separaten Satelliten Ressourcen-DLLs zu platzieren.
ms.assetid: fcadd7e8-cab8-43cb-9c67-af8ebe0e3a5b
title: Verwenden von Assemblys mit einer mehrsprachigen Benutzeroberfläche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77f501f40715dc2335f02c044aa48ada9741411d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750945"
---
# <a name="using-assemblies-with-a-multilanguage-user-interface"></a><span data-ttu-id="2d74b-103">Verwenden von Assemblys mit einer mehrsprachigen Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="2d74b-103">Using Assemblies with a Multilanguage User Interface</span></span>

<span data-ttu-id="2d74b-104">Wenn Sie möchten, dass Benutzer Ihrer Anwendung bzw. Kern-dll die Sprache der Benutzeroberfläche ändern können, sollten Sie erwägen, Sprachressourcen in separaten Satelliten Ressourcen-DLLs zu platzieren.</span><span class="sxs-lookup"><span data-stu-id="2d74b-104">If you want users of your application, or core DLL, to be capable of changing the language of the user interface, you should consider placing language resources into separate satellite resource DLLs.</span></span> <span data-ttu-id="2d74b-105">Weitere Informationen zum Verwenden von Satelliten Ressourcen-DLLs finden Sie unter [Multilanguage User Interface (MUI)](/windows/desktop/Intl/multilingual-user-interface).</span><span class="sxs-lookup"><span data-stu-id="2d74b-105">For more information about using satellite resource DLLs, see [Multilanguage User Interface (MUI)](/windows/desktop/Intl/multilingual-user-interface).</span></span>

<span data-ttu-id="2d74b-106">Jede Satelliten-DLL enthält die Ressourcen für eine andere Sprache.</span><span class="sxs-lookup"><span data-stu-id="2d74b-106">Each satellite DLL contains the resources for a different language.</span></span> <span data-ttu-id="2d74b-107">Die Core-dll kann als Assembly bereitgestellt werden, und jede der Satelliten-DLLs kann als separate Satellitenassemblys bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="2d74b-107">The core DLL may be provided as an assembly and each of the satellite DLLs may be provided as separate satellite assemblies.</span></span> <span data-ttu-id="2d74b-108">In diesem Fall sollte jede Satellitenassembly über ein eigenes selbst beschreibendes Assemblymanifest verfügen.</span><span class="sxs-lookup"><span data-stu-id="2d74b-108">In this case, each satellite assembly should have its own self-describing assembly manifest.</span></span> <span data-ttu-id="2d74b-109">Das Manifest der Satellitenassembly sollte keine Abhängigkeit von anderen Assemblys beschreiben.</span><span class="sxs-lookup"><span data-stu-id="2d74b-109">The satellite assembly's manifest should not describe any dependency on other assemblies.</span></span> <span data-ttu-id="2d74b-110">Eine beliebige Abhängigkeit von Satellitenassemblys für andere Assemblys sollte stattdessen im Manifest der Kernassembly beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="2d74b-110">Any dependency of satellite assemblies on other assemblies should instead be described in the core assembly's manifest.</span></span>

<span data-ttu-id="2d74b-111">Mithilfe der [MUI-Version (Multilanguage User Interface)](/windows/desktop/Intl/multilingual-user-interface) von Windows können Benutzer die Benutzeroberflächen Sprache gemäß Ihren Einstellungen angeben, vorausgesetzt, die erforderliche Sprache wurde dem System hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="2d74b-111">The [Multilanguage User Interface (MUI)](/windows/desktop/Intl/multilingual-user-interface) version of Windows enables users to specify the user-interface language according to their preferences, provided the required language has been added to the system.</span></span> <span data-ttu-id="2d74b-112">Eine Kernassembly kann mehrere Sprachen unterstützen, indem mehrere MUI-Assemblys verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2d74b-112">A core assembly can support multiple languages by using multiple MUI assemblies.</span></span> <span data-ttu-id="2d74b-113">In diesem Fall sollte jede MUI-Assembly über ein eigenes Manifest verfügen, und alle Abhängigkeiten von anderen Assemblys sollten nur im Manifest der Kernassembly beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="2d74b-113">In this case, each MUI assembly should have its own manifest and any dependencies on other assemblies should only be described in the core assembly's manifest.</span></span>

<span data-ttu-id="2d74b-114">Proseware. Sample. Pop kann z. b. eine zentrale parallele Assembly sein, die von der Proseware. Research. SampleAssembly-Assembly abhängig ist.</span><span class="sxs-lookup"><span data-stu-id="2d74b-114">For example, Proseware.Sample.Pop may be a core side-by-side assembly which happens to be dependent on the Proseware.Research.SampleAssembly assembly.</span></span> <span data-ttu-id="2d74b-115">Wenn "Proseware. Sample. Pop" MUI verwendet, um mehrere Sprachen zu unterstützen, können separate MUI-Assemblys für jede Sprache bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="2d74b-115">If Proseware.Sample.Pop uses MUI to support multiple languages, separate MUI assemblies can be provided for each language.</span></span> <span data-ttu-id="2d74b-116">Jede MUI-Assembly sollte über ein eigenes Manifest verfügen, das diese spezielle Satelliten Ressourcen-DLL beschreibt.</span><span class="sxs-lookup"><span data-stu-id="2d74b-116">Each MUI assembly should have its own manifest describing this particular satellite resource DLL.</span></span> <span data-ttu-id="2d74b-117">Die MUI-Assemblymanifeste sollten keinen Verweis auf Abhängigkeiten von anderen Assemblys enthalten.</span><span class="sxs-lookup"><span data-stu-id="2d74b-117">The MUI assembly manifests should not include any reference to dependencies on other assemblies.</span></span> <span data-ttu-id="2d74b-118">Das Manifest, in dem die Kernassembly "Proseware. Sample. Pop" beschrieben wird, sollte die Abhängigkeit von "Proseware. Sample. Pop" in der Assembly "Proseware. Research. SampleAssembly" beschreiben.</span><span class="sxs-lookup"><span data-stu-id="2d74b-118">The manifest describing the core assembly, Proseware.Sample.Pop, should describe the dependency of Proseware.Sample.Pop on the Proseware.Research.SampleAssembly assembly.</span></span>

<span data-ttu-id="2d74b-119">Die Attribute des **assemblyIdentity** -Elements einer Satellitenassembly ähneln denen im Manifest der basisassembly.</span><span class="sxs-lookup"><span data-stu-id="2d74b-119">The attributes of the **assemblyIdentity** element of a satellite assembly are similar to those in the manifest of the base assembly.</span></span> <span data-ttu-id="2d74b-120">Das **Name** -Attribut muss mit dem Hinzufügen von "Resources" identisch mit der basisassembly sein.</span><span class="sxs-lookup"><span data-stu-id="2d74b-120">The **name** attribute should be the same as the base assembly with the addition of "Resources."</span></span> <span data-ttu-id="2d74b-121">Wenn der Name z. b. "Proseware. Tools. Rechtschreib Check. Runtime-Libraries" in der basisassembly lautet, lautet der Name in der Ressourcenassembly "Proseware. Tools. Rechtschreib Check. Runtime-Libraries. Resources".</span><span class="sxs-lookup"><span data-stu-id="2d74b-121">For example, if the name is "Proseware.Tools.SpellCheck.Runtime-Libraries" in the base assembly, the name in the resource assembly would be "Proseware.Tools.SpellCheck.Runtime-Libraries.Resources."</span></span> <span data-ttu-id="2d74b-122">Mit dem **Language** -Attribut sollte die Sprache der Ressourcenassembly identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="2d74b-122">The **language** attribute should identify the language of the resource assembly.</span></span> <span data-ttu-id="2d74b-123">Das **File** -Attribut sollte die Liste der Dateien enthalten, bei denen es sich um Ressourcen-DLLs handelt.</span><span class="sxs-lookup"><span data-stu-id="2d74b-123">The **file** attribute should include the list of files that are resource DLLs.</span></span>

<span data-ttu-id="2d74b-124">Im folgenden finden Sie ein Beispiel für das Manifest für die Ressourcenassembly Proseware. Tools. SpellCheck. Runtime-Libraries.</span><span class="sxs-lookup"><span data-stu-id="2d74b-124">The following is an example of the manifest for Proseware.Tools.SpellCheck.Runtime-Libraries resources assembly.</span></span>

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <assemblyIdentity
        type="win32"
        name="Proseware.Tools.SpellCheck.Runtime-Libraries.Resources"
        version="6.0.0.0"
        processorArchitecture="X86"
        language="DE"
        publicKeyToken="0000000000000000"
    />
    <file name="sample.dll"/>
</assembly>
```

<span data-ttu-id="2d74b-125">Die basisassembly beschreibt eine optionale Abhängigkeit von der Ressourcenassembly.</span><span class="sxs-lookup"><span data-stu-id="2d74b-125">The base assembly describes an optional dependency on the resource assembly.</span></span> <span data-ttu-id="2d74b-126">Wenn ein Benutzer in diesem Beispiel Windows mit dem als Deutsch bezeichneten Gebiets Schema ausgeführt wird, würde eine Anwendung, die die Proseware. Tools. SpellCheck-Assembly verwendet, Text in Deutsch anzeigen.</span><span class="sxs-lookup"><span data-stu-id="2d74b-126">In this example, if a user is running Windows with the locale designated as German, an application using the Proseware.Tools.SpellCheck assembly would display text in German.</span></span>

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <assemblyIdentity type="win32" 
    name="Proseware.Tools.SpellCheck.Runtime-Libraries"
    version="6.0.0.0" processorArchitecture="x86"
    publicKeyToken="0000000000000000"/>
    <dependency optional="yes">
        <dependentAssembly>
            <assemblyIdentity type="win32" 
                              name="Proseware.Tools.SpellCheck.Runtime-Libraries.Resources" 
                              version="6.0.0.0" 
                              processorArchitecture="x86" 
                              publicKeyToken="0000000000000000" 
                              language="*"
            />
        </dependentAssembly>
    </dependency>
```

 

 
