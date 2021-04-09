---
description: Unter Windows Server 2003 wird WinHTTP als parallele Assembly implementiert und muss als solche verknüpft werden. Beachten Sie, dass dies nicht für Windows Vista und höher gilt.
ms.assetid: 524d926d-4d8a-4576-96fd-c533517ba28e
title: Verwenden von WinHTTP als parallele Assembly
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a74a0e5cf842fdd1e20c6d6d271de482e361c4af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751512"
---
# <a name="using-winhttp-as-a-side-by-side-assembly"></a><span data-ttu-id="eb944-104">Verwenden von WinHTTP als parallele Assembly</span><span class="sxs-lookup"><span data-stu-id="eb944-104">Using WinHTTP as a Side-by-side Assembly</span></span>

<span data-ttu-id="eb944-105">Unter Windows Server 2003 wird WinHTTP als parallele Assembly implementiert und muss als solche verknüpft werden.</span><span class="sxs-lookup"><span data-stu-id="eb944-105">On Windows Server 2003, WinHTTP is implemented as a side-by-side assembly, and must be linked to as such.</span></span> <span data-ttu-id="eb944-106">Beachten Sie, dass dies nicht für Windows Vista und höher gilt.</span><span class="sxs-lookup"><span data-stu-id="eb944-106">Note that this does not apply to Windows Vista and later.</span></span>

## <a name="side-by-side-assemblies"></a><span data-ttu-id="eb944-107">Parallele Assemblys</span><span class="sxs-lookup"><span data-stu-id="eb944-107">Side-by-side Assemblies</span></span>

<span data-ttu-id="eb944-108">Ab Microsoft Windows XP wurde ein paralleler assemblymechanismus bereitgestellt, um die Lauf Zeit Verknüpfung zu steuern und Konflikte mit der dll (Dynamic Link Library) zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="eb944-108">Starting with Microsoft Windows XP, a side-by-side assemblies mechanism was provided to control run-time linking to avoid dynamic-link-library (DLL) versioning conflicts.</span></span> <span data-ttu-id="eb944-109">Weitere Informationen zu parallelen Assemblys finden Sie unter Informationen [zu isolierten Anwendungen und](/windows/desktop/SbsCs/about-isolated-applications-and-side-by-side-assemblies)parallelen Assemblys.</span><span class="sxs-lookup"><span data-stu-id="eb944-109">For information about side-by-side assemblies, see [About Isolated Applications and Side-by-side Assemblies](/windows/desktop/SbsCs/about-isolated-applications-and-side-by-side-assemblies).</span></span>

<span data-ttu-id="eb944-110">Um diesen Mechanismus zum Verknüpfen mit WinHTTP-Version 5,1 unter Windows Server 2003 zu verwenden, muss eine Anwendung ein Manifest einschließen, das WinHTTP als abhängige Assembly angibt.</span><span class="sxs-lookup"><span data-stu-id="eb944-110">To use this mechanism to link to WinHTTP version 5.1 on Windows Server 2003, an application must incorporate a manifest that specifies WinHTTP as a dependent assembly.</span></span> <span data-ttu-id="eb944-111">Weitere Informationen hierzu finden Sie unter [verwenden](/windows/desktop/SbsCs/using-side-by-side-assemblies) paralleler Assemblys.</span><span class="sxs-lookup"><span data-stu-id="eb944-111">See [Using Side-by-side Assemblies](/windows/desktop/SbsCs/using-side-by-side-assemblies) for more information about how to do this.</span></span>

## <a name="a-sample-winhttp-application-manifest"></a><span data-ttu-id="eb944-112">Ein WinHTTP-Beispiel Anwendungs Manifest</span><span class="sxs-lookup"><span data-stu-id="eb944-112">A Sample WinHTTP Application Manifest</span></span>

<span data-ttu-id="eb944-113">Das folgende Beispiel Manifest veranschaulicht ein Anwendungs Manifest, das zum Verknüpfen mit WinHTTP verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="eb944-113">The sample manifest below illustrates an application manifest that can be used for linking to WinHTTP.</span></span>

<span data-ttu-id="eb944-114">Alle Attribute außer "Type" von " <assembly> <assemblyIdentity> " müssen entsprechend Ihren Anwendungen geändert werden.</span><span class="sxs-lookup"><span data-stu-id="eb944-114">All attributes except "type" of the "<assembly><assemblyIdentity>" must be modified as appropriate for your particular application.</span></span> <span data-ttu-id="eb944-115">Das gleiche gilt für den Inhalt des " &lt; Description &gt; "-Elements.</span><span class="sxs-lookup"><span data-stu-id="eb944-115">The same goes for the contents of the "&lt;description&gt;" element.</span></span>

<span data-ttu-id="eb944-116">Stellen Sie außerdem sicher, dass das Attribut "ProcessorArchitecture" von " <dependentAssembly> <assemblyIdentity> " mit dem Attribut "ProcessorArchitecture" von "" übereinstimmt <assembly> <assemblyIdentity> .</span><span class="sxs-lookup"><span data-stu-id="eb944-116">In addition, make sure that the "processorArchitecture" attribute of the "<dependentAssembly><assemblyIdentity>" matches the "processorArchitecture" attribute of the "<assembly><assemblyIdentity>".</span></span> <span data-ttu-id="eb944-117">Im folgenden Beispiel werden beide auf "x86" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="eb944-117">Below, for example, both are set to "x86".</span></span>

<span data-ttu-id="eb944-118">Alle Werte, die nicht spezifisch für Ihre Anwendung sind, sollten die unten gezeigten Formen annehmen.</span><span class="sxs-lookup"><span data-stu-id="eb944-118">All values not specific to your application should take the forms shown below.</span></span>

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
  <assemblyIdentity
                    version="1.0.0.0"
                    processorArchitecture="x86"
                    name="Microsoft.Windows.Sample"
                    type="win32" />
  <description>Sample WinHttp Application</description>
  <dependency>
    <dependentAssembly>
      <assemblyIdentity 
                    type="win32" 
                    name="Microsoft.Windows.WinHTTP" 
                    version="5.1.0.0"
                    processorArchitecture="x86" 
                    publicKeyToken="6595b64144ccf1df"
                    language="*" />
    </dependentAssembly>
  </dependency>
</assembly>
```

 

 
