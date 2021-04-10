---
description: Verwenden Sie das folgende Verfahren, um eine neue Anwendung zu entwickeln oder eine vorhandene Anwendung zu aktualisieren, um die parallelen Assemblys zu verwenden, die von Microsoft oder anderen parallelen assemblyverlegern verfügbar sind.
ms.assetid: da6b6767-8a30-4a76-a030-615067a2cb17
title: Verwenden paralleler Assemblys
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1992562a0868918de2901a7ca88033784af6ef1c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862331"
---
# <a name="using-side-by-side-assemblies"></a><span data-ttu-id="4368c-103">Verwenden paralleler Assemblys</span><span class="sxs-lookup"><span data-stu-id="4368c-103">Using Side-by-side Assemblies</span></span>

<span data-ttu-id="4368c-104">Verwenden Sie das folgende Verfahren, um eine neue Anwendung zu entwickeln oder eine vorhandene Anwendung zu aktualisieren, [um die parallelen](about-side-by-side-assemblies-.md) Assemblys zu verwenden, die von Microsoft oder anderen parallelen assemblyverlegern verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="4368c-104">Use the following procedure to develop a new application, or update an existing application, to use the [side-by-side assemblies](about-side-by-side-assemblies-.md) available from Microsoft or other side-by-side assembly publishers.</span></span> <span data-ttu-id="4368c-105">Eine Liste der parallelen Assemblys, die derzeit von Microsoft bereitgestellt werden, finden Sie [unter Unterstützte](supported-microsoft-side-by-side-assemblies.md)parallele Assemblys von Microsoft.</span><span class="sxs-lookup"><span data-stu-id="4368c-105">For a list of the side-by-side assemblies currently provided by Microsoft, see [Supported Microsoft Side-by-side Assemblies](supported-microsoft-side-by-side-assemblies.md).</span></span> <span data-ttu-id="4368c-106">Beachten Sie, dass die Anwendung auf mindestens Windows XP ausgeführt werden muss, um die Assemblys als parallele Assemblys zu installieren.</span><span class="sxs-lookup"><span data-stu-id="4368c-106">Note that the application must be run on at least Windows XP to install the assemblies as side-by-side assemblies.</span></span> <span data-ttu-id="4368c-107">Weitere Informationen finden Sie unter [Richtlinien zum Erstellen](guidelines-for-creating-side-by-side-assemblies.md)paralleler Assemblys.</span><span class="sxs-lookup"><span data-stu-id="4368c-107">For more information, see [Guidelines for Creating Side-by-side Assemblies](guidelines-for-creating-side-by-side-assemblies.md).</span></span>

<span data-ttu-id="4368c-108">**So fügen Sie einer Anwendung eine Seite-an-Seite-Assembly hinzu**</span><span class="sxs-lookup"><span data-stu-id="4368c-108">**To add a side-by-side assembly to an application**</span></span>

1.  <span data-ttu-id="4368c-109">Identifizieren Sie die parallelen Assemblys, die für die Anwendung erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="4368c-109">Identify the side-by-side assemblies that your application requires.</span></span> <span data-ttu-id="4368c-110">Ab Windows XP werden diese parallelen Assemblys und ihre Assemblymanifeste mit dem Betriebssystem installiert, aber nicht global registriert.</span><span class="sxs-lookup"><span data-stu-id="4368c-110">Starting with Windows XP, these side-by-side assemblies and their assembly manifests are installed with the operating system but are not globally registered.</span></span>
2.  <span data-ttu-id="4368c-111">Verwenden Sie einen XML-Editor, um ein [Anwendungs Manifest](application-manifests.md)zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="4368c-111">Use an XML editor to create an [application manifest](application-manifests.md).</span></span> <span data-ttu-id="4368c-112">Weitere Informationen finden Sie unten im Beispiel Anwendungs Manifest.</span><span class="sxs-lookup"><span data-stu-id="4368c-112">See the example application manifest below.</span></span> <span data-ttu-id="4368c-113">Weitere Informationen finden Sie unter [Anwendungs Manifeste](application-manifests.md) in der [Manifest-Dateireferenz](manifest-files-reference.md).</span><span class="sxs-lookup"><span data-stu-id="4368c-113">For more information, see [Application Manifests](application-manifests.md) in the [Manifest Files Reference](manifest-files-reference.md).</span></span>
3.  <span data-ttu-id="4368c-114">Geben Sie die Attributwerte im [*DEF-Context-Unterelement assemblyIdentity*](d-sbscs-gly.md) des Anwendungs Manifests ein, das die Anwendung eindeutig definiert.</span><span class="sxs-lookup"><span data-stu-id="4368c-114">Enter attribute values in the [*DEF-context assemblyIdentity*](d-sbscs-gly.md) subelement of the application manifest that uniquely defines the application.</span></span> <span data-ttu-id="4368c-115">Weitere Informationen zum DEF-Kontext **assemblyIdentity** finden Sie unter [Anwendungs Manifeste](application-manifests.md).</span><span class="sxs-lookup"><span data-stu-id="4368c-115">For more information about the DEF-context **assemblyIdentity**, see [Application Manifests](application-manifests.md).</span></span>
4.  <span data-ttu-id="4368c-116">Wenn die Assembly abhängige Assemblys enthält, geben Sie Attributwerte in die entsprechenden untergeordneten Elemente der [*ref-Context-Assemblyidentität*](r-sbscs-gly.md) des Anwendungs Manifests ein.</span><span class="sxs-lookup"><span data-stu-id="4368c-116">If the assembly contains any dependent assemblies, enter attribute values into the corresponding [*REF-context assemblyIdentity*](r-sbscs-gly.md) subelements of the application manifest.</span></span> <span data-ttu-id="4368c-117">Weitere Informationen zum Verweis Kontext **assemblyIdentity** finden Sie unter [Anwendungs Manifeste](application-manifests.md).</span><span class="sxs-lookup"><span data-stu-id="4368c-117">For more information about the REF-context **assemblyIdentity**, see [Application Manifests](application-manifests.md).</span></span>

    ``` syntax
    <dependentAssembly>
      <assemblyIdentity type="win32"
                        name="Microsoft.Windows.SampleAssembly"
                        version="6.0.0.0" processorArchitecture="x86"
                        publicKeyToken="a5aaf5ba15723d5"/>
    ```

5.  <span data-ttu-id="4368c-118">Sie können das Anwendungs Manifest in die binäre ausführbare Header Datei der Anwendung einschließen.</span><span class="sxs-lookup"><span data-stu-id="4368c-118">You may include the application manifest in the application's binary executable header file.</span></span>

    <span data-ttu-id="4368c-119">Fügen Sie in diesem Fall auch die folgende Zeile zur Anwendungs Header Datei hinzu:</span><span class="sxs-lookup"><span data-stu-id="4368c-119">In this case, also add the following line to the application header file:</span></span>

    <dl> <span data-ttu-id="4368c-120">Die Ressourcen- \_ \_ ID RT-Manifest der Ressourcen- \_ ID RT \_ "YourApp.exe. Manifest".</span><span class="sxs-lookup"><span data-stu-id="4368c-120">CREATEPROCESS\_MANIFEST\_RESOURCE\_ID RT\_MANIFEST "YourApp.exe.manifest"</span></span>  
    </dl>

    <span data-ttu-id="4368c-121">Als Alternative können Sie eine separate Manifest-Datei im gleichen Verzeichnis wie die ausführbare Datei der Anwendung platzieren.</span><span class="sxs-lookup"><span data-stu-id="4368c-121">As an alternative, you can place a separate manifest file in the same directory as your application's executable file.</span></span> <span data-ttu-id="4368c-122">Das Betriebssystem lädt das Manifest zuerst aus dem Dateisystem und überprüft dann den Ressourcenabschnitt der ausführbaren Datei.</span><span class="sxs-lookup"><span data-stu-id="4368c-122">The operating system loads the manifest from the file system first, and then checks the resource section of the executable.</span></span> <span data-ttu-id="4368c-123">Die Dateisystem Version hat Vorrang.</span><span class="sxs-lookup"><span data-stu-id="4368c-123">The file system version takes precedence.</span></span>

6.  <span data-ttu-id="4368c-124">Frei [gegebene](/windows/desktop/Msi/shared-assemblies) Assemblys sollten mit dem [Windows Installer](../msi/windows-installer-portal.md) Version 2,0 installiert werden.</span><span class="sxs-lookup"><span data-stu-id="4368c-124">[Shared assemblies](/windows/desktop/Msi/shared-assemblies) should be installed using the [Windows Installer](../msi/windows-installer-portal.md) version 2.0.</span></span> <span data-ttu-id="4368c-125">Erstellen Sie ein Windows Installer Paket, wie unter Gewusst wie: Installieren von Win32-Assemblys für die parallele [Freigabe unter Windows XP](../msi/installing-win32-assemblies-for-side-by-side-sharing-on-windows-xp.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="4368c-125">Author a Windows Installer package as described in [How Do I Install Win32 Assemblies for Side-by-side Sharing on Windows XP?](../msi/installing-win32-assemblies-for-side-by-side-sharing-on-windows-xp.md).</span></span>
7.  <span data-ttu-id="4368c-126">[Private](/windows/desktop/Msi/private-assemblies) Assemblys können mit der [Windows Installer](../msi/windows-installer-portal.md) Version 2,0 installiert werden.</span><span class="sxs-lookup"><span data-stu-id="4368c-126">[Private assemblies](/windows/desktop/Msi/private-assemblies) can be installed using the [Windows Installer](../msi/windows-installer-portal.md) version 2.0.</span></span> <span data-ttu-id="4368c-127">Erstellen Sie ein Windows Installer Paket, wie unter Gewusst wie: Installieren von Win32-Assemblys [für die private Verwendung einer Anwendung unter Windows XP](../msi/installing-win32-assemblies-for-the-private-use-of-an-application-on-windows-xp.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="4368c-127">Author a Windows Installer package as described in [How Do I Install Win32 Assemblies for the Private Use of an Application on Windows XP?](../msi/installing-win32-assemblies-for-the-private-use-of-an-application-on-windows-xp.md).</span></span> <span data-ttu-id="4368c-128">Sie können auch ein beliebiges anderes Installationsprogramm verwenden, um eine private Assembly und das zugehörige Manifest in denselben Ordner wie die ausführbare Datei der Anwendung zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="4368c-128">You can also use any other installer to copy a private assembly and its manifest into the same folder as the application's executable file.</span></span>
8.  <span data-ttu-id="4368c-129">Testen Sie Ihre Anwendung, um die Ergebnisse sicherzustellen.</span><span class="sxs-lookup"><span data-stu-id="4368c-129">Test your application to ensure the results.</span></span> <span data-ttu-id="4368c-130">Beachten Sie, dass auf dem Testcomputer nicht die parallele Assembly registriert sein sollte.</span><span class="sxs-lookup"><span data-stu-id="4368c-130">Note that your test computer should not have the side-by-side assembly registered.</span></span>
9.  <span data-ttu-id="4368c-131">Stellen Sie die Anwendung bereit, oder aktualisieren Sie Sie als Windows Installer Paket.</span><span class="sxs-lookup"><span data-stu-id="4368c-131">Deploy your application or update as a Windows Installer package.</span></span>

## <a name="example-application-manifest"></a><span data-ttu-id="4368c-132">Beispiel für ein Anwendungs Manifest</span><span class="sxs-lookup"><span data-stu-id="4368c-132">Example Application Manifest</span></span>

<span data-ttu-id="4368c-133">Im folgenden finden Sie ein Beispiel für ein Anwendungs Manifest:</span><span class="sxs-lookup"><span data-stu-id="4368c-133">The following is an example of an application manifest:</span></span>

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
  <assemblyIdentity type="win32" name="Microsoft.Windows.mysampleapp" version="1.0.0.0" processorArchitecture="x86"/>
  <dependency>
    <dependentAssembly>
      <assemblyIdentity type="win32" name="Microsoft.Windows.SampleAssembly" version="6.0.0.0" processorArchitecture="x86" publicKeyToken="a5aaf5ba15723d5"/>
    </dependentAssembly>
  </dependency>
  <dependency>
    <dependentAssembly>
      <assemblyIdentity type="win32" name="Microsoft.Tools.MyPrivateDll" version="2.5.0.0" processorArchitecture="x86"/>
    </dependentAssembly>
  </dependency>
</assembly>
```

 

 
