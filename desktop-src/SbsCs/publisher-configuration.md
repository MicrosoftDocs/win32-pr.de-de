---
description: Eine Verleger Konfigurationsdatei leitet Anwendungen und Assemblys mit Abhängigkeit von einer Version einer parallelen Assembly Global um, um eine andere Version derselben Assembly zu verwenden.
ms.assetid: 9146c81e-8f43-4854-bbc4-1daaeb5fdda8
title: Herausgeber Konfiguration
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c50ceb5263830cb1778aaaede673974cd7faca75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217793"
---
# <a name="publisher-configuration"></a><span data-ttu-id="a011a-103">Herausgeber Konfiguration</span><span class="sxs-lookup"><span data-stu-id="a011a-103">Publisher Configuration</span></span>

<span data-ttu-id="a011a-104">Eine [Verleger Konfigurationsdatei](publisher-configuration-files.md) leitet Anwendungen und Assemblys mit Abhängigkeit von einer Version einer parallelen Assembly Global um, um eine andere Version derselben Assembly zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="a011a-104">A [publisher configuration file](publisher-configuration-files.md) globally redirects applications and assemblies having a dependence on one version of a side-by-side assembly to use another version of the same assembly.</span></span> <span data-ttu-id="a011a-105">Dies ermöglicht es Anwendungen und Assemblys, die aktualisierte Assembly zu verwenden, ohne alle betroffenen Anwendungen neu erstellen zu müssen.</span><span class="sxs-lookup"><span data-stu-id="a011a-105">This enables applications and assemblies to use the updated assembly without having to rebuild all of the affected applications.</span></span>

<span data-ttu-id="a011a-106">Die [Verleger Konfigurationsdateien](publisher-configuration-files.md) können vom Verleger einer Assembly bereitgestellt werden, wenn eine neue Version der Assembly mit kompatiblen Fehlerbehebungen oder Sicherheitsupdates ausgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="a011a-106">[Publisher configuration files](publisher-configuration-files.md) may be provided by the publisher of an assembly when issuing a new version of the assembly with compatible bug fixes or security updates.</span></span> <span data-ttu-id="a011a-107">Die aktualisierte Version sollte vollständig abwärts kompatibel sein.</span><span class="sxs-lookup"><span data-stu-id="a011a-107">The updated version should be fully backward compatible.</span></span> <span data-ttu-id="a011a-108">Eine Verleger Konfigurationsdatei sollte nie zum Hinzufügen neuer Features verwendet werden, es sei denn, das Update ist vollständig abwärts kompatibel.</span><span class="sxs-lookup"><span data-stu-id="a011a-108">A publisher configuration file should never be used to add new features unless the update is fully backward compatible.</span></span> <span data-ttu-id="a011a-109">Die Verleger Konfigurationsdateien sollten niemals verwendet werden, um die Haupt-oder neben Version einer Assembly zu erhöhen.</span><span class="sxs-lookup"><span data-stu-id="a011a-109">Publisher configuration files should never be used to increment the major or minor version of an assembly.</span></span> <span data-ttu-id="a011a-110">Umleiten Sie z. b. die Assemblyversion 6.0.0.0 nicht an 7.0.0.0 oder 6.1.0.0.</span><span class="sxs-lookup"><span data-stu-id="a011a-110">For example, do not redirect assembly version 6.0.0.0 to 7.0.0.0 or to 6.1.0.0.</span></span>

<span data-ttu-id="a011a-111">Die Verleger Konfigurationsdateien sollten nur vom Verleger der Assembly ausgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="a011a-111">Publisher configuration files should only be issued by the publisher of the assembly.</span></span> <span data-ttu-id="a011a-112">Assemblyentwickler sollten freigegebene parallele Assemblys und Verleger Konfigurationsdateien signieren.</span><span class="sxs-lookup"><span data-stu-id="a011a-112">Assembly developers should sign shared side-by-side assemblies and publisher configuration files.</span></span> <span data-ttu-id="a011a-113">Verwenden Sie den gleichen Schlüssel, um die Assembly und die zugehörigen Verleger Konfigurationsdateien zu signieren.</span><span class="sxs-lookup"><span data-stu-id="a011a-113">Use the same key to sign the assembly and the associated publisher configuration files.</span></span> <span data-ttu-id="a011a-114">Die Verleger Konfigurationsdateien sollten mithilfe der gleichen Tools wie für Assemblys signiert werden. Informationen hierzu finden Sie unter [Beispiel für Assemblysignierung](assembly-signing-example.md) und [Erstellen signierter Dateien](creating-signed-files-and-catalogs.md)</span><span class="sxs-lookup"><span data-stu-id="a011a-114">Publisher configuration files should be signed using the same tools as used for assemblies, see [Assembly Signing Example](assembly-signing-example.md) and [Creating Signed Files and Catalogs](creating-signed-files-and-catalogs.md).</span></span>

<span data-ttu-id="a011a-115">In der Regel werden die neue Version einer Assembly und die zugehörige Verleger Konfigurationsdatei in einem Service Pack Update installiert.</span><span class="sxs-lookup"><span data-stu-id="a011a-115">Typically, the new version of an assembly and the associated publisher configuration file will be installed in a service pack update.</span></span> <span data-ttu-id="a011a-116">Die Verleger Konfigurationsdateien sollten nie als verteilbare Anwendungen mit Anwendungen bereitgestellt werden, da die Installation einer Verleger Konfigurationsdatei die Assemblys auf dem System Global umleitet.</span><span class="sxs-lookup"><span data-stu-id="a011a-116">Publisher configuration files should never be provided with applications as a redistributable because installing a publisher configuration file globally redirects assemblies on the system.</span></span> <span data-ttu-id="a011a-117">Wenn die zu Aktualisier Ende Assembly als verteilbare Komponente bereitgestellt wird, sollte der Herausgeber beide der folgenden Optionen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="a011a-117">If the assembly being updated is provided as a redistributable, the publisher should provide both of the following.</span></span>

-   <span data-ttu-id="a011a-118">Ein Windows Installer Paket (MSI-Datei), das die neue Version der Assembly mit der Verleger Konfiguration enthält.</span><span class="sxs-lookup"><span data-stu-id="a011a-118">A Windows Installer package (.msi file) that includes the new version of the assembly with publisher configuration.</span></span> <span data-ttu-id="a011a-119">Dies kann als Service Pack oder QFE installiert werden, da der Kunde in diesem Fall das System global aktualisieren möchte.</span><span class="sxs-lookup"><span data-stu-id="a011a-119">This may be installed as a service pack or QFE because in this case the customer has chosen to globally update the system.</span></span> <span data-ttu-id="a011a-120">Diese Version des Pakets sollte nie von Anwendungen installiert werden.</span><span class="sxs-lookup"><span data-stu-id="a011a-120">This version of the package should never be installed by applications.</span></span>
-   <span data-ttu-id="a011a-121">Ein Windows Installer Mergemodul (MSM-Datei), das nur die neue Version der Assembly enthält.</span><span class="sxs-lookup"><span data-stu-id="a011a-121">A Windows Installer merge module (.msm file) that only includes the new version of the assembly.</span></span> <span data-ttu-id="a011a-122">Diese Version ist möglicherweise in-Anwendungen enthalten.</span><span class="sxs-lookup"><span data-stu-id="a011a-122">This version may be included with applications.</span></span>

<span data-ttu-id="a011a-123">Anwendungen, die eine Mindestversion der Assembly benötigen, sollten ihre Abhängigkeit von der Mindestversion angeben. wenn die Mindestversion auf einem System nicht verfügbar ist, kann die Anwendung nicht gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="a011a-123">Applications requiring a minimum version of the assembly should state their dependency on the minimum version, if the minimum version is unavailable on a system then the application will fail to start.</span></span> <span data-ttu-id="a011a-124">Wenn Sie als verteilbare Komponente verfügbar ist, sollte Sie in das Setup der Anwendung eingeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="a011a-124">If it is available as a redistributable then it should be included in the application setup.</span></span>

<span data-ttu-id="a011a-125">Wenn Sie beispielsweise die folgende [Verleger Konfigurationsdatei](publisher-configuration-files.md) installieren, wird die Bindung von Version 2.0.0.0 von Microsoft. Windows. SampleAssembly an Version 2.0.1.0 umgeleitet.</span><span class="sxs-lookup"><span data-stu-id="a011a-125">For example, installing the following [publisher configuration file](publisher-configuration-files.md) redirects binding from version 2.0.0.0 of the Microsoft.Windows.SampleAssembly to version 2.0.1.0.</span></span> <span data-ttu-id="a011a-126">Dadurch wird eine neue Richtlinie mit dem Namen 1.1.0.0. Policy unter% System Drive% \\ Windows \\ WinSxS \\ Policies \\ x86 \_ Policy. 2.0. Microsoft. Windows. SampleAssembly \_ 75e377300ab7b886 \_ x-WW \_ < *HashValue*> hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a011a-126">This adds a new policy, named 1.1.0.0.Policy, under %systemDrive%\\windows\\winsxs\\policies\\x86\_policy.2.0.Microsoft.Windows.SampleAssembly\_75e377300ab7b886\_x-ww\_<*hashvalue*>.</span></span>

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
   <assemblyIdentity type="win32-policy" publicKeyToken="0000000000000000" name="policy.2.0.Microsoft.Windows.SampleAssembly" version="1.1.0.0" processorArchitecture="x86"/>
   <dependency>
      <dependentAssembly>
         <assemblyIdentity type="win32" name="Microsoft.Windows.SampleAssembly"  processorArchitecture="x86" publicKeyToken="75e377300ab7b886"/>
         <bindingRedirect oldVersion="2.0.0.0" newVersion="2.0.1.0"/>
      </dependentAssembly>
   </dependency>
</assembly>
```

<span data-ttu-id="a011a-127">Wenn Sie die folgende Verleger Konfigurationsdatei für dieselbe Assembly installieren, wird die Bindung von der 2.0.0.0-Version von Microsoft. Windows. SampleAssembly an Version 2.0.3.0 umgeleitet.</span><span class="sxs-lookup"><span data-stu-id="a011a-127">Installing the following publisher configuration file for the same assembly redirects binding from version 2.0.0.0 of the Microsoft.Windows.SampleAssembly to version 2.0.3.0.</span></span> <span data-ttu-id="a011a-128">Dadurch wird eine weitere Richtlinie mit dem Namen 2.1.0.0. Policy unter% System Drive% \\ Windows \\ WinSxS \\ Policies \\ x86 \_ Policy. 2.0. Microsoft. Windows. SampleAssembly \_ 75e377300ab7b886 \_ x-WW \_ < *HashValue*> hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a011a-128">This adds another policy, named 2.1.0.0.Policy, under %systemDrive%\\windows\\winsxs\\policies\\x86\_policy.2.0.Microsoft.Windows.SampleAssembly\_75e377300ab7b886\_x-ww\_<*hashvalue*>.</span></span>

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
   <assemblyIdentity type="win32-policy" publicKeyToken="0000000000000000" name="policy.2.0.Microsoft.Windows.SampleAssembly" version="2.1.0.0" processorArchitecture="x86"/>
   <dependency>
      <dependentAssembly>
         <assemblyIdentity type="win32" name="Microsoft.Windows.SampleAssembly"  processorArchitecture="x86" publicKeyToken="75e377300ab7b886"/>
         <bindingRedirect oldVersion="2.0.0.0" newVersion="2.0.3.0"/>
      </dependentAssembly>
   </dependency>
</assembly>
```

 

 



