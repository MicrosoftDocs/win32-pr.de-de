---
description: Ab Windows XP können Sie eine private Assembly erstellen und für eine bestimmte Anwendung verfügbar machen.
ms.assetid: 08cebffc-6856-4dac-8600-5e7fecb5c69b
title: Beheben einer vorhandenen Anwendung mit einer privaten Assembly
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 095c3eefc5f166ad09643a363ec4308d190e6586
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041672"
---
# <a name="fixing-an-existing-application-using-a-private-assembly"></a><span data-ttu-id="34d87-103">Beheben einer vorhandenen Anwendung mit einer privaten Assembly</span><span class="sxs-lookup"><span data-stu-id="34d87-103">Fixing an Existing Application Using a Private Assembly</span></span>

<span data-ttu-id="34d87-104">Ab Windows XP können Sie eine private Assembly erstellen und für eine bestimmte Anwendung verfügbar machen.</span><span class="sxs-lookup"><span data-stu-id="34d87-104">Beginning with Windows XP, you can create a private assembly and make it available to a specific application.</span></span> <span data-ttu-id="34d87-105">Diese Funktion kann verwendet werden, um eine Anwendung zu beheben, die mit einem Update nicht kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="34d87-105">This capability can be used to fix an application that becomes incompatible with an update.</span></span> <span data-ttu-id="34d87-106">Ein Beispiel hierfür ist eine Anwendung, die nach dem Upgrade des Betriebssystems nicht mit der neuesten Version von MSVCRT.DLL kompatibel wird.</span><span class="sxs-lookup"><span data-stu-id="34d87-106">An example would be an application that becomes incompatible with the latest version of MSVCRT.DLL after upgrading the operating system.</span></span> <span data-ttu-id="34d87-107">In diesem Fall haben Sie nicht die Möglichkeit, die System Version zu ersetzen, da MSVCRT.DLL eine geschützte Windows-Datei ist.</span><span class="sxs-lookup"><span data-stu-id="34d87-107">In this case, you do not have the option of replacing the system version because MSVCRT.DLL is a Windows Protected File.</span></span> <span data-ttu-id="34d87-108">Anstatt die Anwendung für die Verwendung der neuen msvcrt-Version neu schreiben zu müssen, können Sie eine private Assembly für msvcrt erstellen und diese im Anwendungsordner installieren.</span><span class="sxs-lookup"><span data-stu-id="34d87-108">Rather than having to rewrite the application to work with the new version of MSVCRT, you can create a private assembly for MSVCRT and install this in your application folder.</span></span> <span data-ttu-id="34d87-109">Beachten Sie, dass nicht jede freigegebene Komponente ein geeigneter Kandidat für eine private parallele Assembly ist, und dass einige Komponenten über Lizenzierungs Einschränkungen verfügen, in denen die Komponenten installiert werden können.</span><span class="sxs-lookup"><span data-stu-id="34d87-109">Note that not every shared component is a suitable candidate for a private side-by-side assembly, and some components have licensing restrictions about where their components can be installed.</span></span> <span data-ttu-id="34d87-110">Die Komponente muss die Kriterien für eine Seite-an-Seite-Komponente erfüllen.</span><span class="sxs-lookup"><span data-stu-id="34d87-110">The component needs to meet the criteria for a side-by-side component.</span></span> <span data-ttu-id="34d87-111">Fragen Sie den Herausgeber der Komponente, wenn Sie eine passende Assembly bereitstellen können.</span><span class="sxs-lookup"><span data-stu-id="34d87-111">Ask the publisher of the component if they can provide a suitable assembly.</span></span>

<span data-ttu-id="34d87-112">Das Manifest des private Assembly und das Manifest der Anwendung müssen beide im selben Ordner wie die ausführbare Datei der Anwendung installiert werden.</span><span class="sxs-lookup"><span data-stu-id="34d87-112">The private assembly's manifest and the application's manifest should both be installed in the same folder as the application's executable.</span></span> <span data-ttu-id="34d87-113">Wenn die Anwendung ausgeführt wird, wird das Anwendungs Manifest konsultiert und die Version von msvcrt geladen, die für die Anwendung privat ist.</span><span class="sxs-lookup"><span data-stu-id="34d87-113">When the application runs, it consults the application manifest and load the version of MSVCRT that is private to the application.</span></span>

<span data-ttu-id="34d87-114">In diesem Beispiel enthält die private Assembly sowohl MSVCRT.DLL als auch MSVCIRT.DLL wie im folgenden Assemblymanifest:</span><span class="sxs-lookup"><span data-stu-id="34d87-114">For this example, the private assembly would include both MSVCRT.DLL and MSVCIRT.DLL as in the following assembly manifest:</span></span>

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <assemblyIdentity type="win32"
      name="Microsoft.Windows.PrivateCPlusPlusRuntime" 
version="6.0.0.0" 
processorArchitecture="x86"/>
    <file name="msvcrt.dll"/>
    <file name="msvcirt.dll"/>
</assembly>
```

<span data-ttu-id="34d87-115">Im folgenden finden Sie ein Beispiel für ein mögliches Anwendungs Manifest.</span><span class="sxs-lookup"><span data-stu-id="34d87-115">The following is an example of a possible application manifest.</span></span>

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0"> 
<assemblyIdentity 
    version="1.0.0.0" 
    processorArchitecture="x86" 
    name="APPLICATION" 
    type="win32" 
/> 
<description>Description of Application</description> 
<dependency> 
    <dependentAssembly> 
       <assemblyIdentity 
           type="win32"
           name="Microsoft.Windows.PrivateCPlusPlusRuntime" 
           version="6.0.0.0" 
           processorArchitecture="x86"/> 
    </dependentAssembly> 
</dependency> 
</assembly>
```

 

 



