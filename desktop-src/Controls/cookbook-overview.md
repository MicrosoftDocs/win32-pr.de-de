---
title: Aktivieren von visuellen Stilen
description: In diesem Thema wird erläutert, wie Sie Ihre Anwendung konfigurieren, um sicherzustellen, dass allgemeine Steuerelemente im bevorzugten visuellen Stil des Benutzers angezeigt werden.
ms.assetid: eb6c2469-25b9-43c4-a6ca-391a7b2859b3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4673d0a47f42f557e09f4afe46131cd48bad1b0
ms.sourcegitcommit: 967ba3a2a618e6088cb607164a2a924530278645
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113102169"
---
# <a name="enabling-visual-styles"></a><span data-ttu-id="dabfa-103">Aktivieren von visuellen Stilen</span><span class="sxs-lookup"><span data-stu-id="dabfa-103">Enabling Visual Styles</span></span>

<span data-ttu-id="dabfa-104">In diesem Thema wird erläutert, wie Sie Ihre Anwendung konfigurieren, um sicherzustellen, dass allgemeine Steuerelemente im bevorzugten visuellen Stil des Benutzers angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="dabfa-104">This topic explains how to configure your application to ensure that common controls are displayed in the user's preferred visual style.</span></span>

<span data-ttu-id="dabfa-105">Das Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="dabfa-105">This topic includes the following sections.</span></span>

-   [<span data-ttu-id="dabfa-106">Verwenden von Manifesten oder Direktiven, um sicherzustellen, dass visuelle Stile auf Anwendungen angewendet werden können</span><span class="sxs-lookup"><span data-stu-id="dabfa-106">Using Manifests or Directives to Ensure That Visual Styles Can Be Applied to Applications</span></span>](#using-manifests-or-directives-to-ensure-that-visual-styles-can-be-applied-to-applications)
-   [<span data-ttu-id="dabfa-107">Verwenden ComCtl32.dll Version 6 in einer Anwendung, die nur Standarderweiterungen verwendet</span><span class="sxs-lookup"><span data-stu-id="dabfa-107">Using ComCtl32.dll Version 6 in an Application That Uses Only Standard Extensions</span></span>](#using-comctl32dll-version-6-in-an-application-that-uses-only-standard-extensions)
-   [<span data-ttu-id="dabfa-108">Verwenden von ComCtl32 Version 6 in Systemsteuerung oder einer DLL, die von RunDll32.exe</span><span class="sxs-lookup"><span data-stu-id="dabfa-108">Using ComCtl32 Version 6 in Control Panel or a DLL That Is Run by RunDll32.exe</span></span>](#using-comctl32-version-6-in-control-panel-or-a-dll-that-is-run-by-rundll32exe)
-   [<span data-ttu-id="dabfa-109">Hinzufügen der Unterstützung visueller Stile zu einer Erweiterung, einem Plug-In, einem MMC-Snap-In oder einer DLL, die in einen Prozess eingebunden wird</span><span class="sxs-lookup"><span data-stu-id="dabfa-109">Adding Visual Style Support to an Extension, Plug-in, MMC Snap-in or a DLL That Is Brought into a Process</span></span>](#adding-visual-style-support-to-an-extension-plug-in-mmc-snap-in-or-a-dll-that-is-brought-into-a-process)
-   [<span data-ttu-id="dabfa-110">Deaktivieren visueller Stile</span><span class="sxs-lookup"><span data-stu-id="dabfa-110">Turning Off Visual Styles</span></span>](#turning-off-visual-styles)
-   [<span data-ttu-id="dabfa-111">Verwenden von visuellen Stilen mit HTML-Inhalt</span><span class="sxs-lookup"><span data-stu-id="dabfa-111">Using Visual Styles with HTML Content</span></span>](#using-visual-styles-with-html-content)
-   [<span data-ttu-id="dabfa-112">Wenn visuelle Stile nicht angewendet werden</span><span class="sxs-lookup"><span data-stu-id="dabfa-112">When Visual Styles are not Applied</span></span>](#when-visual-styles-are-not-applied)
-   [<span data-ttu-id="dabfa-113">Herstellen der Kompatibilität Ihrer Anwendung mit früheren Versionen von Windows</span><span class="sxs-lookup"><span data-stu-id="dabfa-113">Making Your Application Compatible with Earlier Versions of Windows</span></span>](#making-your-application-compatible-with-earlier-versions-of-windows)
-   [<span data-ttu-id="dabfa-114">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="dabfa-114">Related topics</span></span>](#related-topics)

## <a name="using-manifests-or-directives-to-ensure-that-visual-styles-can-be-applied-to-applications"></a><span data-ttu-id="dabfa-115">Verwenden von Manifesten oder Direktiven, um sicherzustellen, dass visuelle Stile auf Anwendungen angewendet werden können</span><span class="sxs-lookup"><span data-stu-id="dabfa-115">Using Manifests or Directives to Ensure That Visual Styles Can Be Applied to Applications</span></span>

<span data-ttu-id="dabfa-116">Damit Ihre Anwendung visuelle Stile verwenden kann, müssen Sie ComCtl32.dll Version 6 oder höher verwenden.</span><span class="sxs-lookup"><span data-stu-id="dabfa-116">To enable your application to use visual styles, you must use ComCtl32.dll version 6 or later.</span></span> <span data-ttu-id="dabfa-117">Da Version 6 nicht weiterverteilbar ist, ist sie nur verfügbar, wenn Ihre Anwendung unter einer Windows-Version ausgeführt wird, die sie enthält.</span><span class="sxs-lookup"><span data-stu-id="dabfa-117">Because version 6 is not redistributable, it is available only when your application is running on a version of Windows that contains it.</span></span> <span data-ttu-id="dabfa-118">Windows wird sowohl mit Version 5 als auch mit Version 6 ausgeliefert.</span><span class="sxs-lookup"><span data-stu-id="dabfa-118">Windows ships with both version 5 and version 6.</span></span> <span data-ttu-id="dabfa-119">ComCtl32.dll Version 6 enthält sowohl die Benutzersteuerelemente als auch die allgemeinen Steuerelemente.</span><span class="sxs-lookup"><span data-stu-id="dabfa-119">ComCtl32.dll version 6 contains both the user controls and the common controls.</span></span> <span data-ttu-id="dabfa-120">Standardmäßig verwenden Anwendungen die in User32.dll definierten Benutzersteuerelemente und die allgemeinen Steuerelemente, die in ComCtl32.dll Version 5 definiert sind.</span><span class="sxs-lookup"><span data-stu-id="dabfa-120">By default, applications use the user controls defined in User32.dll and the common controls defined in ComCtl32.dll version 5.</span></span> <span data-ttu-id="dabfa-121">Eine Liste der DLL-Versionen und deren Verteilungsplattformen finden Sie unter [Allgemeine Steuerungsversionen.](common-control-versions.md)</span><span class="sxs-lookup"><span data-stu-id="dabfa-121">For a list of DLL versions and their distribution platforms, see [Common Control Versions](common-control-versions.md).</span></span>

<span data-ttu-id="dabfa-122">Wenn Ihre Anwendung visuelle Stile verwenden soll, müssen Sie ein Anwendungsmanifest oder eine Compilerdirektive hinzufügen, die angibt, dass ComCtl32.dll Version 6 verwendet werden soll, wenn sie verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="dabfa-122">If you want your application to use visual styles, you must add an application manifest or compiler directive that indicates that ComCtl32.dll version 6 should be used if it is available.</span></span>

<span data-ttu-id="dabfa-123">Mit einem Anwendungsmanifest kann eine Anwendung angeben, welche Versionen einer Assembly erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="dabfa-123">An application manifest enables an application to specify which versions of an assembly it requires.</span></span> <span data-ttu-id="dabfa-124">In Microsoft Win32 besteht eine Assembly aus einem Satz von DLLs und einer Liste von versionsfähigen Objekten, die in diesen DLLs enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="dabfa-124">In Microsoft Win32, an assembly is a set of DLLs and a list of versionable objects that are contained within those DLLs.</span></span>

<span data-ttu-id="dabfa-125">Manifeste werden in XML geschrieben.</span><span class="sxs-lookup"><span data-stu-id="dabfa-125">Manifests are written in XML.</span></span> <span data-ttu-id="dabfa-126">Der Name der Anwendungsmanifestdatei ist der Name Ihrer ausführbaren Datei gefolgt von der Dateinamenerweiterung .manifest. beispiel: MyApp.exe.manifest.</span><span class="sxs-lookup"><span data-stu-id="dabfa-126">The name of the application manifest file is the name of your executable followed by the file name extension .manifest; for example, MyApp.exe.manifest.</span></span> <span data-ttu-id="dabfa-127">Das folgende Beispielmanifest zeigt, dass im ersten Abschnitt das Manifest selbst beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="dabfa-127">The following sample manifest shows that the first section describes the manifest itself.</span></span> <span data-ttu-id="dabfa-128">Die folgende Tabelle zeigt die Attribute, die vom **assemblyIdentity-Element** im Abschnitt manifest description festgelegt wurden.</span><span class="sxs-lookup"><span data-stu-id="dabfa-128">The following table shows the attributes set by the **assemblyIdentity** element in the manifest description section.</span></span>



| <span data-ttu-id="dabfa-129">attribute</span><span class="sxs-lookup"><span data-stu-id="dabfa-129">Attribute</span></span>             | <span data-ttu-id="dabfa-130">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dabfa-130">Description</span></span>                                                                                                                 |
|-----------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dabfa-131">version</span><span class="sxs-lookup"><span data-stu-id="dabfa-131">version</span></span>               | <span data-ttu-id="dabfa-132">Version des Manifests.</span><span class="sxs-lookup"><span data-stu-id="dabfa-132">Version of the manifest.</span></span> <span data-ttu-id="dabfa-133">Die Version muss das Format major.minor.revision.build haben (d.h. n.n.n.n, wobei n <=65535).</span><span class="sxs-lookup"><span data-stu-id="dabfa-133">The version must be in the form major.minor.revision.build (that is, n.n.n.n, where n <=65535).</span></span> |
| <span data-ttu-id="dabfa-134">processorArchitecture</span><span class="sxs-lookup"><span data-stu-id="dabfa-134">processorArchitecture</span></span> | <span data-ttu-id="dabfa-135">Prozessor, für den Ihre Anwendung entwickelt wird.</span><span class="sxs-lookup"><span data-stu-id="dabfa-135">Processor for which your application is developed.</span></span>                                                                          |
| <span data-ttu-id="dabfa-136">name</span><span class="sxs-lookup"><span data-stu-id="dabfa-136">name</span></span>                  | <span data-ttu-id="dabfa-137">Enthält den Firmennamen, den Produktnamen und den Anwendungsnamen.</span><span class="sxs-lookup"><span data-stu-id="dabfa-137">Includes company name, product name and application name.</span></span>                                                                   |
| <span data-ttu-id="dabfa-138">type</span><span class="sxs-lookup"><span data-stu-id="dabfa-138">type</span></span>                  | <span data-ttu-id="dabfa-139">Typ Ihrer Anwendung, z. B. Win32.</span><span class="sxs-lookup"><span data-stu-id="dabfa-139">Type of your application, such as Win32.</span></span>                                                                                    |



 

<span data-ttu-id="dabfa-140">Das Beispielmanifest enthält auch eine Beschreibung Ihrer Anwendung und gibt Anwendungsabhängigkeiten an.</span><span class="sxs-lookup"><span data-stu-id="dabfa-140">The sample manifest also provides a description of your application and specifies application dependencies.</span></span> <span data-ttu-id="dabfa-141">Die folgende Tabelle zeigt die Attribute, die vom **assemblyIdentity-Element** im Abhängigkeitsabschnitt festgelegt wurden.</span><span class="sxs-lookup"><span data-stu-id="dabfa-141">The following table shows the attributes set by the **assemblyIdentity** element in the dependency section.</span></span>



| <span data-ttu-id="dabfa-142">attribute</span><span class="sxs-lookup"><span data-stu-id="dabfa-142">Attribute</span></span>             | <span data-ttu-id="dabfa-143">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dabfa-143">Description</span></span>                                      |
|-----------------------|--------------------------------------------------|
| <span data-ttu-id="dabfa-144">type</span><span class="sxs-lookup"><span data-stu-id="dabfa-144">type</span></span>                  | <span data-ttu-id="dabfa-145">Typ der Abhängigkeitskomponente, z. B. Win32.</span><span class="sxs-lookup"><span data-stu-id="dabfa-145">Type of the dependency component, such as Win32.</span></span> |
| <span data-ttu-id="dabfa-146">name</span><span class="sxs-lookup"><span data-stu-id="dabfa-146">name</span></span>                  | <span data-ttu-id="dabfa-147">Der Name der Komponente.</span><span class="sxs-lookup"><span data-stu-id="dabfa-147">Name of the component.</span></span>                           |
| <span data-ttu-id="dabfa-148">version</span><span class="sxs-lookup"><span data-stu-id="dabfa-148">version</span></span>               | <span data-ttu-id="dabfa-149">Version der Komponente.</span><span class="sxs-lookup"><span data-stu-id="dabfa-149">Version of the component.</span></span>                        |
| <span data-ttu-id="dabfa-150">processorArchitecture</span><span class="sxs-lookup"><span data-stu-id="dabfa-150">processorArchitecture</span></span> | <span data-ttu-id="dabfa-151">Prozessor, für den die Komponente entworfen wurde.</span><span class="sxs-lookup"><span data-stu-id="dabfa-151">Processor that the component is designed for.</span></span>    |
| <span data-ttu-id="dabfa-152">Publickeytoken</span><span class="sxs-lookup"><span data-stu-id="dabfa-152">publicKeyToken</span></span>        | <span data-ttu-id="dabfa-153">Schlüsseltoken, das mit dieser Komponente verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="dabfa-153">Key token used with this component.</span></span>              |
| <span data-ttu-id="dabfa-154">language</span><span class="sxs-lookup"><span data-stu-id="dabfa-154">language</span></span>              | <span data-ttu-id="dabfa-155">Sprache der Komponente.</span><span class="sxs-lookup"><span data-stu-id="dabfa-155">Language of the component.</span></span>                       |



 

<span data-ttu-id="dabfa-156">Es folgt ein Beispiel für eine Manifestdatei.</span><span class="sxs-lookup"><span data-stu-id="dabfa-156">Following is an example of a manifest file.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="dabfa-157">Legen Sie den Eintrag **processorArchitecture** auf **"X86"** fest, wenn Ihre Anwendung auf die 32-Bit-Windows-Plattform abzielt, oder auf **"amd64",** wenn Ihre Anwendung auf die 64-Bit-Windows-Plattform abzielt.</span><span class="sxs-lookup"><span data-stu-id="dabfa-157">Set the **processorArchitecture** entry to **"X86"** if your application targets the 32 bit Windows platform, or to **"amd64"** if your application targets the 64 bit Windows platform.</span></span> <span data-ttu-id="dabfa-158">Sie können auch **" \* " "** angeben, um sicherzustellen, dass alle Plattformen als Ziel verwendet werden, wie in den folgenden Beispielen gezeigt.</span><span class="sxs-lookup"><span data-stu-id="dabfa-158">You can also specify **"\*"**, which ensures that all platforms are targeted, as shown in the following examples.</span></span>

 


```C++
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
<assemblyIdentity
    version="1.0.0.0"
    processorArchitecture="*"
    name="CompanyName.ProductName.YourApplication"
    type="win32"
/>
<description>Your application description here.</description>
<dependency>
    <dependentAssembly>
        <assemblyIdentity
            type="win32"
            name="Microsoft.Windows.Common-Controls"
            version="6.0.0.0"
            processorArchitecture="*"
            publicKeyToken="6595b64144ccf1df"
            language="*"
        />
    </dependentAssembly>
</dependency>
</assembly>
```



<span data-ttu-id="dabfa-159">Wenn Sie Microsoft Visual C++ 2005 oder höher verwenden, können Sie dem Quellcode die folgende Compilerdirektive hinzufügen, anstatt manuell ein Manifest zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="dabfa-159">If you are using Microsoft Visual C++ 2005 or later, you can add the following compiler directive to your source code instead of manually creating a manifest.</span></span> <span data-ttu-id="dabfa-160">Aus Gründen der Lesbarkeit ist die -Direktive hier in mehrere Zeilen unterteilt.</span><span class="sxs-lookup"><span data-stu-id="dabfa-160">For readability, the directive is broken into several lines here.</span></span>


```C++
#pragma comment(linker,"\"/manifestdependency:type='win32' \
name='Microsoft.Windows.Common-Controls' version='6.0.0.0' \
processorArchitecture='*' publicKeyToken='6595b64144ccf1df' language='*'\"")
```



<span data-ttu-id="dabfa-161">In den folgenden Themen werden die Schritte zum Anwenden visueller Stile auf verschiedene Anwendungstypen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="dabfa-161">The following topics describe the steps for applying visual styles to different types of applications.</span></span> <span data-ttu-id="dabfa-162">Beachten Sie, dass das Manifestformat in jedem Fall identisch ist.</span><span class="sxs-lookup"><span data-stu-id="dabfa-162">Notice that the manifest format is the same in each case.</span></span>

## <a name="using-comctl32dll-version-6-in-an-application-that-uses-only-standard-extensions"></a><span data-ttu-id="dabfa-163">Verwenden ComCtl32.dll Version 6 in einer Anwendung, die nur Standarderweiterungen verwendet</span><span class="sxs-lookup"><span data-stu-id="dabfa-163">Using ComCtl32.dll Version 6 in an Application That Uses Only Standard Extensions</span></span>

<span data-ttu-id="dabfa-164">Im Folgenden sind Beispiele für Anwendungen aufgeführt, die keine Erweiterungen von Drittanbietern verwenden.</span><span class="sxs-lookup"><span data-stu-id="dabfa-164">The following are examples of applications that do not use third-party extensions.</span></span>

-   <span data-ttu-id="dabfa-165">Rechner</span><span class="sxs-lookup"><span data-stu-id="dabfa-165">Calculator</span></span>
-   <span data-ttu-id="dabfa-166">FreeCell (in Windows Vista und Windows 7)</span><span class="sxs-lookup"><span data-stu-id="dabfa-166">FreeCell (in Windows Vista and Windows 7)</span></span>
-   <span data-ttu-id="dabfa-167">Auswendungsweeper (in Windows Vista und Windows 7)</span><span class="sxs-lookup"><span data-stu-id="dabfa-167">Minesweeper (in Windows Vista and Windows 7)</span></span>
-   <span data-ttu-id="dabfa-168">Editor</span><span class="sxs-lookup"><span data-stu-id="dabfa-168">Notepad</span></span>
-   <span data-ttu-id="dabfa-169">Solitair (in Windows Vista und Windows 7)</span><span class="sxs-lookup"><span data-stu-id="dabfa-169">Solitaire (in Windows Vista and Windows 7)</span></span>

<span data-ttu-id="dabfa-170">**So erstellen Sie ein Manifest und ermöglichen Ihrer Anwendung die Verwendung visueller Stile.**</span><span class="sxs-lookup"><span data-stu-id="dabfa-170">**To create a manifest and enable your application to use visual styles.**</span></span>

1.  <span data-ttu-id="dabfa-171">Stellen Sie einen Link zu ComCtl32.lib her, und rufen Sie [**InitCommonControls auf.**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols)</span><span class="sxs-lookup"><span data-stu-id="dabfa-171">Link to ComCtl32.lib and call [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols).</span></span>
2.  <span data-ttu-id="dabfa-172">Fügen Sie ihrer Quellstruktur eine Datei mit dem Namen YourApp.exe.manifest hinzu, die das XML-Manifestformat auf hat.</span><span class="sxs-lookup"><span data-stu-id="dabfa-172">Add a file called YourApp.exe.manifest to your source tree that has the XML manifest format.</span></span>
    ```C++
    <?xml version="1.0" encoding="UTF-8" standalone="yes"?>
    <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <assemblyIdentity
        version="1.0.0.0"
        processorArchitecture="*"
        name="CompanyName.ProductName.YourApplication"
        type="win32"
    />
    <description>Your application description here.</description>
    <dependency>
        <dependentAssembly>
            <assemblyIdentity
                type="win32"
                name="Microsoft.Windows.Common-Controls"
                version="6.0.0.0"
                processorArchitecture="*"
                publicKeyToken="6595b64144ccf1df"
                language="*"
            />
        </dependentAssembly>
    </dependency>
    </assembly>
    ```

    

3.  <span data-ttu-id="dabfa-173">Fügen Sie das Manifest wie folgt der Ressourcendatei Ihrer Anwendung hinzu:</span><span class="sxs-lookup"><span data-stu-id="dabfa-173">Add the manifest to your application's resource file as follows:</span></span>
    ```C++
    CREATEPROCESS_MANIFEST_RESOURCE_ID RT_MANIFEST "YourApp.exe.manifest"
    ```

    

    > [!Note]  
    > <span data-ttu-id="dabfa-174">Wenn Sie der Ressource den vorherigen Eintrag hinzufügen, müssen Sie ihn in einer Zeile formatieren.</span><span class="sxs-lookup"><span data-stu-id="dabfa-174">When you add the previous entry to the resource you must format it on one line.</span></span> <span data-ttu-id="dabfa-175">Alternativ können Sie die XML-Manifestdatei im selben Verzeichnis wie die ausführbare Datei Ihrer Anwendung platzieren.</span><span class="sxs-lookup"><span data-stu-id="dabfa-175">Alternatively, you can place the XML manifest file in the same directory as your application's executable file.</span></span> <span data-ttu-id="dabfa-176">Das Betriebssystem lädt zuerst das Manifest aus dem Dateisystem und überprüft dann den Ressourcenabschnitt der ausführbaren Datei.</span><span class="sxs-lookup"><span data-stu-id="dabfa-176">The operating system will load the manifest from the file system first, then check the resource section of the executable.</span></span> <span data-ttu-id="dabfa-177">Die Dateisystemversion hat Vorrang.</span><span class="sxs-lookup"><span data-stu-id="dabfa-177">The file system version takes precedence.</span></span>

     

<span data-ttu-id="dabfa-178">Wenn Sie Ihre Anwendung erstellen, wird das Manifest als binäre Ressource hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="dabfa-178">When you build your application, the manifest will be added as a binary resource.</span></span>

## <a name="using-comctl32-version-6-in-control-panel-or-a-dll-that-is-run-by-rundll32exe"></a><span data-ttu-id="dabfa-179">Verwenden von ComCtl32 Version 6 in Systemsteuerung oder einer DLL, die von RunDll32.exe</span><span class="sxs-lookup"><span data-stu-id="dabfa-179">Using ComCtl32 Version 6 in Control Panel or a DLL That Is Run by RunDll32.exe</span></span>

<span data-ttu-id="dabfa-180">**So erstellen Sie ein Manifest und ermöglichen Ihrer Anwendung die Verwendung visueller Stile.**</span><span class="sxs-lookup"><span data-stu-id="dabfa-180">**To create a manifest and enable your application to use visual styles.**</span></span>

1.  <span data-ttu-id="dabfa-181">Stellen Sie einen Link zu ComCtl32.lib her, und rufen Sie [**InitCommonControls auf.**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols)</span><span class="sxs-lookup"><span data-stu-id="dabfa-181">Link to ComCtl32.lib and call [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols).</span></span>
2.  <span data-ttu-id="dabfa-182">Fügen Sie ihrer Quellstruktur eine Datei mit dem Namen YourApp.cpl.manifest hinzu, die das XML-Manifestformat auf hat.</span><span class="sxs-lookup"><span data-stu-id="dabfa-182">Add a file called YourApp.cpl.manifest to your source tree that has the XML manifest format.</span></span>
    ```C++
    <?xml version="1.0" encoding="UTF-8" standalone="yes"?>
    <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <assemblyIdentity
        version="1.0.0.0"
        processorArchitecture="*"
        name="CompanyName.ProductName.YourApplication"
        type="win32"
    />
    <description>Your application description here.</description>
    <dependency>
        <dependentAssembly>
            <assemblyIdentity
                type="win32"
                name="Microsoft.Windows.Common-Controls"
                version="6.0.0.0"
                processorArchitecture="*"
                publicKeyToken="6595b64144ccf1df"
                language="*"
            />
        </dependentAssembly>
    </dependency>
    </assembly>
    ```

    

3.  <span data-ttu-id="dabfa-183">Fügen Sie das Manifest der Ressourcendatei Ihrer Anwendung als Ressourcen-ID 123 hinzu.</span><span class="sxs-lookup"><span data-stu-id="dabfa-183">Add the manifest to your application's resource file as resource ID 123.</span></span>

> [!Note]  
> <span data-ttu-id="dabfa-184">Wenn Sie eine Systemsteuerung Anwendung erstellen, platzieren Sie sie in der entsprechenden Kategorie.</span><span class="sxs-lookup"><span data-stu-id="dabfa-184">When you author a Control Panel application, place it in the appropriate category.</span></span> <span data-ttu-id="dabfa-185">Systemsteuerung unterstützt jetzt die Kategorisierung Systemsteuerung Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="dabfa-185">Control Panel now supports categorization of Control Panel applications.</span></span> <span data-ttu-id="dabfa-186">Dies bedeutet, dass Systemsteuerung Anwendungen Bezeichner zugewiesen und in Aufgabenbereiche wie Programme hinzufügen oder entfernen, Darstellung und Designs oder Datum, Uhrzeit, Sprache und regionale Optionen unterteilt werden können.</span><span class="sxs-lookup"><span data-stu-id="dabfa-186">This means that Control Panel applications can be assigned identifiers and separated into task areas such as Add or Remove Programs, Appearance and Themes, or Date, Time, Language, and Regional Options.</span></span>

 

## <a name="adding-visual-style-support-to-an-extension-plug-in-mmc-snap-in-or-a-dll-that-is-brought-into-a-process"></a><span data-ttu-id="dabfa-187">Hinzufügen der Unterstützung visueller Stile zu einer Erweiterung, einem Plug-In, einem MMC-Snap-In oder einer DLL, die in einen Prozess eingebunden wird</span><span class="sxs-lookup"><span data-stu-id="dabfa-187">Adding Visual Style Support to an Extension, Plug-in, MMC Snap-in or a DLL That Is Brought into a Process</span></span>

<span data-ttu-id="dabfa-188">Unterstützung für visuelle Stile kann einer Erweiterung, einem Plug-In, einem MMC-Snap-In oder einer DLL hinzugefügt werden, die in einen Prozess eingefügt wird.</span><span class="sxs-lookup"><span data-stu-id="dabfa-188">Support for visual styles can be added to an extension, plug-in, MMC snap-in, or a DLL that is brought into a process.</span></span> <span data-ttu-id="dabfa-189">Verwenden Sie beispielsweise die folgenden Schritte, um visuelle Stile für ein mmc-Snap-In (Microsoft Management Console) hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="dabfa-189">For example, use the following steps to add visual styles support for an Microsoft Management Console (MMC) snap-in.</span></span>

1.  <span data-ttu-id="dabfa-190">Kompilieren Sie das Snap-In mit dem Flag -DISOLATION \_ AWARE \_ ENABLED, oder fügen Sie die folgende Anweisung vor der \# include -Anweisung "windows.h" ein.</span><span class="sxs-lookup"><span data-stu-id="dabfa-190">Compile your snap-in with the -DISOLATION\_AWARE\_ENABLED flag or insert the following statement before the \#include "windows.h" statement.</span></span>

    ```C++
    #define ISOLATION_AWARE_ENABLED 1
    ```

    

    <span data-ttu-id="dabfa-191">Weitere Informationen zu ISOLATION \_ AWARE ENABLED finden Sie unter Isolieren von \_ [Komponenten.](/windows/desktop/SbsCs/isolating-components)</span><span class="sxs-lookup"><span data-stu-id="dabfa-191">For more information about ISOLATION\_AWARE\_ENABLED, see [Isolating Components](/windows/desktop/SbsCs/isolating-components).</span></span>

2.  <span data-ttu-id="dabfa-192">Schließen Sie die allgemeine Steuerelementheaderdatei in die Snap-In-Quelle ein.</span><span class="sxs-lookup"><span data-stu-id="dabfa-192">Include the common control header file in your snap-in source.</span></span>
    ```C++
    #include <commctrl.h>
    ```

    

3.  <span data-ttu-id="dabfa-193">Fügen Sie Ihrer Quellstruktur eine Datei namens YourApp.manifest hinzu, die das XML-Manifestformat verwendet.</span><span class="sxs-lookup"><span data-stu-id="dabfa-193">Add a file called YourApp.manifest to your source tree that uses the XML manifest format.</span></span>
    ```C++
    <?xml version="1.0" encoding="UTF-8" standalone="yes"?>
    <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <assemblyIdentity
        version="1.0.0.0"
        processorArchitecture="*"
        name="CompanyName.ProductName.YourApplication"
        type="win32"
    />
    <description>Your application description here.</description>
    <dependency>
        <dependentAssembly>
            <assemblyIdentity
                type="win32"
                name="Microsoft.Windows.Common-Controls"
                version="6.0.0.0"
                processorArchitecture="*"
                publicKeyToken="6595b64144ccf1df"
                language="*"
            />
        </dependentAssembly>
    </dependency>
    </assembly>
    ```

    

4.  <span data-ttu-id="dabfa-194">Fügen Sie das Manifest der Ressourcendatei Ihres Snap-Ins hinzu.</span><span class="sxs-lookup"><span data-stu-id="dabfa-194">Add the manifest to your snap-in's resource file.</span></span> <span data-ttu-id="dabfa-195">Ausführliche Informationen zum Hinzufügen eines Manifests zu einer Ressourcendatei finden Sie unter [Verwenden von ComCtl32 Version 6 in einer Anwendung, die Erweiterungen, Plug-Ins oder eine DLL verwendet, die in einen Prozess eingebunden wird.](/previous-versions//ms649781(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="dabfa-195">See [Using ComCtl32 Version 6 in an Application That Uses Extensions, Plug-ins, or a DLL That Is Brought into a Process](/previous-versions//ms649781(v=vs.85)) for details on adding a manifest to a resource file.</span></span>

## <a name="turning-off-visual-styles"></a><span data-ttu-id="dabfa-196">Deaktivieren von visuellen Stilen</span><span class="sxs-lookup"><span data-stu-id="dabfa-196">Turning Off Visual Styles</span></span>

<span data-ttu-id="dabfa-197">Sie können visuelle Stile für ein Steuerelement oder für alle Steuerelemente in einem Fenster deaktivieren, indem Sie die [**SetWindowTheme-Funktion**](/windows/desktop/api/Uxtheme/nf-uxtheme-setwindowtheme) wie folgt aufrufen:</span><span class="sxs-lookup"><span data-stu-id="dabfa-197">You can turn off visual styles for a control or for all controls in a window by calling the [**SetWindowTheme**](/windows/desktop/api/Uxtheme/nf-uxtheme-setwindowtheme) function as follows:</span></span>


```C++
SetWindowTheme(hwnd, L" ", L" ");
```



<span data-ttu-id="dabfa-198">Im vorherigen Beispiel ist *hwnd* das Handle des Fensters, in dem visuelle Stile deaktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="dabfa-198">In the previous example, *hwnd* is the handle of the window in which to disable visual styles.</span></span> <span data-ttu-id="dabfa-199">Nach dem Aufruf wird das Steuerelement ohne visuelle Stile gerendert.</span><span class="sxs-lookup"><span data-stu-id="dabfa-199">After the call, the control renders without visual styles.</span></span>

## <a name="using-visual-styles-with-html-content"></a><span data-ttu-id="dabfa-200">Verwenden von visuellen Stilen mit HTML-Inhalt</span><span class="sxs-lookup"><span data-stu-id="dabfa-200">Using Visual Styles with HTML Content</span></span>

<span data-ttu-id="dabfa-201">Auf HTML-Seiten, die Cascading Stylesheets (CSS)-Eigenschaften wie Hintergrund oder Rahmen ändern, werden keine visuellen Stile angewendet.</span><span class="sxs-lookup"><span data-stu-id="dabfa-201">HTML pages that modify the Cascading Style Sheets (CSS) properties such as background or border do not have visual styles applied to them.</span></span> <span data-ttu-id="dabfa-202">Sie zeigen das angegebene CSS-Attribut an.</span><span class="sxs-lookup"><span data-stu-id="dabfa-202">They display the specified CSS attribute.</span></span> <span data-ttu-id="dabfa-203">Wenn sie als Teil des Inhalts angegeben werden, gelten die meisten CSS-Eigenschaften für Elemente, auf die visuelle Stile angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="dabfa-203">When specified as part of the content, most CSS properties do apply to elements that have visual styles applied.</span></span>

<span data-ttu-id="dabfa-204">Standardmäßig werden visuelle Stile auf systeminterne HTML-Steuerelemente auf Seiten angewendet, die in Microsoft Internet Explorer 6 und höher angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="dabfa-204">By default, visual styles are applied to intrinsic HTML controls on pages displayed in Microsoft Internet Explorer 6 and later versions.</span></span> <span data-ttu-id="dabfa-205">Um visuelle Stile für eine HTML-Seite zu deaktivieren, fügen Sie dem -Element ein META-Tag hinzu.</span><span class="sxs-lookup"><span data-stu-id="dabfa-205">To turn off visual styles for an HTML page, add a META tag to the</span></span> <head> <span data-ttu-id="dabfa-206">-Abschnitt.</span><span class="sxs-lookup"><span data-stu-id="dabfa-206">section.</span></span> <span data-ttu-id="dabfa-207">Diese Technik gilt auch für Inhalte, die als HTML-Anwendungen (HTAs) verpackt sind.</span><span class="sxs-lookup"><span data-stu-id="dabfa-207">This technique also applies to content packaged as HTML Applications (HTAs).</span></span> <span data-ttu-id="dabfa-208">Um visuelle Stile zu deaktivieren, muss das META-Tag wie folgt lauten:</span><span class="sxs-lookup"><span data-stu-id="dabfa-208">To turn off visual styles, the META tag must be as follows:</span></span>


```
<META HTTP-EQUIV="MSThemeCompatible" CONTENT="no">
```



> [!Note]  
> <span data-ttu-id="dabfa-209">Wenn die Browsereinstellung und die Tageinstellung nicht stimmen, werden auf der Seite keine visuellen Stile angewendet.</span><span class="sxs-lookup"><span data-stu-id="dabfa-209">If the browser setting and the tag setting do not agree, the page will not apply visual styles.</span></span> <span data-ttu-id="dabfa-210">Wenn das META-Tag beispielsweise auf "no" festgelegt ist und der Browser so festgelegt ist, dass visuelle Stile aktiviert werden, werden visuelle Stile nicht auf die Seite angewendet.</span><span class="sxs-lookup"><span data-stu-id="dabfa-210">For example, if the META tag is set to "no" and the browser is set to enable visual styles, visual styles will not be applied to the page.</span></span> <span data-ttu-id="dabfa-211">Wenn jedoch entweder der Browser oder das META-Tag auf "yes" festgelegt ist und das andere Element nicht angegeben ist, werden visuelle Stile angewendet.</span><span class="sxs-lookup"><span data-stu-id="dabfa-211">However, if either the browser or META tag is set to "yes" and the other item is not specified, visual styles will be applied.</span></span>

 

<span data-ttu-id="dabfa-212">Visuelle Stile können das Layout Ihres Inhalts ändern.</span><span class="sxs-lookup"><span data-stu-id="dabfa-212">Visual styles might change the layout of your content.</span></span> <span data-ttu-id="dabfa-213">Wenn Sie bestimmte Attribute für systeminterne HTML-Steuerelemente festlegen, z. B. die Breite einer Schaltfläche, stellen Sie möglicherweise fest, dass die Bezeichnung auf der Schaltfläche unter bestimmten visuellen Stilen nicht lesbar ist.</span><span class="sxs-lookup"><span data-stu-id="dabfa-213">Also, if you set certain attributes on intrinsic HTML controls, such as the width of a button, you might find that the label on the button is unreadable under certain visual styles.</span></span>

<span data-ttu-id="dabfa-214">Sie müssen Ihre Inhalte gründlich mit visuellen Stilen testen, um festzustellen, ob die Anwendung visueller Stile negative Auswirkungen auf Ihren Inhalt und Ihr Layout hat.</span><span class="sxs-lookup"><span data-stu-id="dabfa-214">You must thoroughly test your content using visual styles to determine whether applying visual styles has an adverse effect on your content and layout.</span></span>

## <a name="when-visual-styles-are-not-applied"></a><span data-ttu-id="dabfa-215">Wenn visuelle Stile nicht angewendet werden</span><span class="sxs-lookup"><span data-stu-id="dabfa-215">When Visual Styles are not Applied</span></span>

<span data-ttu-id="dabfa-216">Um das Anwenden visueller Stile auf ein Fenster der obersten Ebene zu vermeiden, geben Sie dem Fenster einen Nicht-NULL-Bereich (**SetWindowRgn**).</span><span class="sxs-lookup"><span data-stu-id="dabfa-216">To avoid applying visual styles to a top level window, give the window a non-null region (**SetWindowRgn**).</span></span> <span data-ttu-id="dabfa-217">Das System geht davon aus, dass ein Fenster mit einem Nicht-NULL-Bereich ein spezialisiertes Fenster ist, das keine visuellen Stile verwendet.</span><span class="sxs-lookup"><span data-stu-id="dabfa-217">The system assumes that a window with a non-NULL region is a specialized window that does not use visual styles.</span></span> <span data-ttu-id="dabfa-218">Ein untergeordnetes Fenster, das einem Fenster der obersten Ebene nicht visueller Stile zugeordnet ist, kann auch dann visuelle Stile anwenden, wenn das übergeordnete Fenster dies nicht tut.</span><span class="sxs-lookup"><span data-stu-id="dabfa-218">A child window associated with a non-visual-styles top level window may still apply visual styles even though the parent window does not.</span></span>

<span data-ttu-id="dabfa-219">Wenn Sie die Verwendung visueller Stile für alle Fenster in Ihrer Anwendung deaktivieren möchten, rufen Sie [**SetThemeAppProperties**](/windows/desktop/api/Uxtheme/nf-uxtheme-setthemeappproperties) auf, und übergeben Sie nicht das Flag STAP \_ ALLOW \_ NONCLIENT.</span><span class="sxs-lookup"><span data-stu-id="dabfa-219">If you want to disable the use of visual styles for all windows in your application, call [**SetThemeAppProperties**](/windows/desktop/api/Uxtheme/nf-uxtheme-setthemeappproperties) and do not pass the STAP\_ALLOW\_NONCLIENT flag.</span></span> <span data-ttu-id="dabfa-220">Wenn eine Anwendung **SetThemeAppProperties** nicht aufruft, werden als Flagwerte STAP \_ ALLOW \_ NONCLIENT \| STAP \_ ALLOW CONTROLS \_ \| STAP ALLOW \_ \_ WEBCONTENT angenommen.</span><span class="sxs-lookup"><span data-stu-id="dabfa-220">If an application does not call **SetThemeAppProperties**, the assumed flag values are STAP\_ALLOW\_NONCLIENT \| STAP\_ALLOW\_CONTROLS \| STAP\_ALLOW\_WEBCONTENT.</span></span> <span data-ttu-id="dabfa-221">Die angenommenen Werte bewirken, dass für den Nichtclientbereich, die Steuerelemente und den Webinhalt ein visueller Stil angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="dabfa-221">The assumed values cause the nonclient area, the controls, and web content to have a visual style applied.</span></span>

## <a name="making-your-application-compatible-with-earlier-versions-of-windows"></a><span data-ttu-id="dabfa-222">Kompatibilität Ihrer Anwendung mit früheren Versionen von Windows</span><span class="sxs-lookup"><span data-stu-id="dabfa-222">Making Your Application Compatible with Earlier Versions of Windows</span></span>

<span data-ttu-id="dabfa-223">Ein Teil der visuellen Stilarchitektur ist darauf ausgelegt, es einfach zu machen, Ihr Produkt weiterhin in früheren Versionen von Windows zu liefern, die das Ändern der Darstellung von Steuerelementen nicht unterstützen.</span><span class="sxs-lookup"><span data-stu-id="dabfa-223">Much of the visual style architecture is designed to make it simple to continue to ship your product on earlier versions of Windows that do not support changing the appearance of controls.</span></span> <span data-ttu-id="dabfa-224">Beachten Sie beim Versand einer Anwendung für mehrere Betriebssysteme Folgendes:</span><span class="sxs-lookup"><span data-stu-id="dabfa-224">When shipping an application for more than one operating system, be aware of the following:</span></span>

-   <span data-ttu-id="dabfa-225">In Windows-Versionen vor Windows 8 sind visuelle Stile deaktiviert, wenn hoher Kontrast eingeschaltet ist.</span><span class="sxs-lookup"><span data-stu-id="dabfa-225">In versions of Windows prior to Windows 8, visual styles are off when high contrast is on.</span></span> <span data-ttu-id="dabfa-226">Um hohen Kontrast zu unterstützen, muss eine Legacyanwendung, die visuelle Stile unterstützt, einen separaten Codepfad bereitstellen, um Benutzeroberflächenelemente mit hohem Kontrast ordnungsgemäß zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="dabfa-226">To support high contrast, a legacy application that supports visual styles needs to provide a separate code path to properly draw UI elements in high contrast.</span></span> <span data-ttu-id="dabfa-227">In Windows 8 ist hoher Kontrast ein Teil visueller Stile. Eine Windows 8-Anwendung (eine, die die Windows 8-GUID im Kompatibilitätsabschnitt des Anwendungsmanifests enthält) muss jedoch weiterhin einen separaten Codepfad bereitstellen, um unter Windows 7 an einem früheren Punkt ordnungsgemäß in hohem Kontrast gerendert zu werden.</span><span class="sxs-lookup"><span data-stu-id="dabfa-227">In Windows 8, high contrast is a part of visual styles; however, a Windows 8 application (one that includes the Windows 8 GUID in compatibility section of its application manifest) still needs to provide a separate code path to render correctly in high contrast on Windows 7 an earlier.</span></span>
-   <span data-ttu-id="dabfa-228">Wenn Sie die Features in ComCtl32.dll Version 6 verwenden, z. B. die Kachelansicht oder das Linksteuerelemente, müssen Sie den Fall behandeln, in dem diese Steuerelemente auf dem Computer Ihres Benutzers nicht verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="dabfa-228">If you use the features in ComCtl32.dll version 6, such as the tile view or link control, you must handle the case where those controls are not available on your user's computer.</span></span> <span data-ttu-id="dabfa-229">ComCtl32.dll Version 6 ist nicht verteilbar.</span><span class="sxs-lookup"><span data-stu-id="dabfa-229">ComCtl32.dll version 6 is not redistributable.</span></span>
-   <span data-ttu-id="dabfa-230">Testen Sie Ihre Anwendung, um sicherzustellen, dass Sie sich nicht auf Features ComCtl32.dll Version 6 verlassen, ohne zuerst nach der aktuellen Version zu suchen.</span><span class="sxs-lookup"><span data-stu-id="dabfa-230">Test your application to make sure you are not relying on features of ComCtl32.dll version 6 without first checking for the current version.</span></span>
-   <span data-ttu-id="dabfa-231">Verknüpfen Sie nicht mit UxTheme.lib.</span><span class="sxs-lookup"><span data-stu-id="dabfa-231">Do not link to UxTheme.lib.</span></span>
-   <span data-ttu-id="dabfa-232">Schreiben Sie Fehlerbehandlungscode für Instanzen, wenn visuelle Stile nicht wie erwartet funktionieren.</span><span class="sxs-lookup"><span data-stu-id="dabfa-232">Write error-handling code for instances when visual styles do not work as expected.</span></span>
-   <span data-ttu-id="dabfa-233">Das Installieren des Anwendungsmanifests in früheren Versionen wirkt sich nicht auf das Rendering von Steuerelementen aus.</span><span class="sxs-lookup"><span data-stu-id="dabfa-233">Installing your application's manifest in earlier versions will not affect the rendering of controls.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dabfa-234">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="dabfa-234">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dabfa-235">Visuelle Stile</span><span class="sxs-lookup"><span data-stu-id="dabfa-235">Visual Styles</span></span>](themes-overview.md)
</dt> </dl>

 

 
