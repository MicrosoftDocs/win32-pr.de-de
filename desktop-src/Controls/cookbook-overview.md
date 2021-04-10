---
title: Aktivieren von visuellen Stilen
description: In diesem Thema wird erläutert, wie Sie Ihre Anwendung konfigurieren, um sicherzustellen, dass allgemeine Steuerelemente im bevorzugten visuellen Stil des Benutzers angezeigt werden.
ms.assetid: eb6c2469-25b9-43c4-a6ca-391a7b2859b3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39339c0535767011a59730534486604389f62468
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103949180"
---
# <a name="enabling-visual-styles"></a><span data-ttu-id="15e9f-103">Aktivieren von visuellen Stilen</span><span class="sxs-lookup"><span data-stu-id="15e9f-103">Enabling Visual Styles</span></span>

<span data-ttu-id="15e9f-104">In diesem Thema wird erläutert, wie Sie Ihre Anwendung konfigurieren, um sicherzustellen, dass allgemeine Steuerelemente im bevorzugten visuellen Stil des Benutzers angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="15e9f-104">This topic explains how to configure your application to ensure that common controls are displayed in the user's preferred visual style.</span></span>

<span data-ttu-id="15e9f-105">Das Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="15e9f-105">This topic includes the following sections.</span></span>

-   [<span data-ttu-id="15e9f-106">Verwenden von Manifesten oder Direktiven, um sicherzustellen, dass visuelle Stile auf Anwendungen angewendet werden können</span><span class="sxs-lookup"><span data-stu-id="15e9f-106">Using Manifests or Directives to Ensure That Visual Styles Can Be Applied to Applications</span></span>](#using-manifests-or-directives-to-ensure-that-visual-styles-can-be-applied-to-applications)
-   [<span data-ttu-id="15e9f-107">Verwenden von ComCtl32.dll Version 6 in einer Anwendung, die nur Standard Erweiterungen verwendet</span><span class="sxs-lookup"><span data-stu-id="15e9f-107">Using ComCtl32.dll Version 6 in an Application That Uses Only Standard Extensions</span></span>](#using-comctl32dll-version-6-in-an-application-that-uses-only-standard-extensions)
-   [<span data-ttu-id="15e9f-108">Verwenden von ComCtl32 Version 6 in der Systemsteuerung oder einer DLL, die von RunDll32.exeausgeführt wird </span><span class="sxs-lookup"><span data-stu-id="15e9f-108">Using ComCtl32 Version 6 in Control Panel or a DLL That Is Run by RunDll32.exe</span></span>](#using-comctl32-version-6-in-control-panel-or-a-dll-that-is-run-by-rundll32exe)
-   [<span data-ttu-id="15e9f-109">Hinzufügen von Unterstützung für visuelle Stile zu einer Erweiterung, einem Plug-in, einem MMC-Snap-in oder einer DLL, die in einen Prozess integriert wird</span><span class="sxs-lookup"><span data-stu-id="15e9f-109">Adding Visual Style Support to an Extension, Plug-in, MMC Snap-in or a DLL That Is Brought into a Process</span></span>](#adding-visual-style-support-to-an-extension-plug-in-mmc-snap-in-or-a-dll-that-is-brought-into-a-process)
-   [<span data-ttu-id="15e9f-110">Ausschalten visueller Stile</span><span class="sxs-lookup"><span data-stu-id="15e9f-110">Turning Off Visual Styles</span></span>](#turning-off-visual-styles)
-   [<span data-ttu-id="15e9f-111">Verwenden von visuellen Stilen mit HTML-Inhalten</span><span class="sxs-lookup"><span data-stu-id="15e9f-111">Using Visual Styles with HTML Content</span></span>](#using-visual-styles-with-html-content)
-   [<span data-ttu-id="15e9f-112">Wenn visuelle Stile nicht angewendet werden</span><span class="sxs-lookup"><span data-stu-id="15e9f-112">When Visual Styles are not Applied</span></span>](#when-visual-styles-are-not-applied)
-   [<span data-ttu-id="15e9f-113">Kompatibilität Ihrer Anwendung mit früheren Versionen von Windows</span><span class="sxs-lookup"><span data-stu-id="15e9f-113">Making Your Application Compatible with Earlier Versions of Windows</span></span>](#making-your-application-compatible-with-earlier-versions-of-windows)
-   [<span data-ttu-id="15e9f-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="15e9f-114">Related topics</span></span>](#related-topics)

## <a name="using-manifests-or-directives-to-ensure-that-visual-styles-can-be-applied-to-applications"></a><span data-ttu-id="15e9f-115">Verwenden von Manifesten oder Direktiven, um sicherzustellen, dass visuelle Stile auf Anwendungen angewendet werden können</span><span class="sxs-lookup"><span data-stu-id="15e9f-115">Using Manifests or Directives to Ensure That Visual Styles Can Be Applied to Applications</span></span>

<span data-ttu-id="15e9f-116">Um der Anwendung die Verwendung visueller Stile zu ermöglichen, müssen Sie ComCtl32.dll Version 6 oder höher verwenden.</span><span class="sxs-lookup"><span data-stu-id="15e9f-116">To enable your application to use visual styles, you must use ComCtl32.dll version 6 or later.</span></span> <span data-ttu-id="15e9f-117">Da Version 6 nicht weitervertreibbar ist, ist Sie nur verfügbar, wenn Ihre Anwendung unter einer Windows-Version ausgeführt wird, in der Sie enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="15e9f-117">Because version 6 is not redistributable, it is available only when your application is running on a version of Windows that contains it.</span></span> <span data-ttu-id="15e9f-118">Windows ist sowohl mit Version 5 als auch mit Version 6 ausgeliefert.</span><span class="sxs-lookup"><span data-stu-id="15e9f-118">Windows ships with both version 5 and version 6.</span></span> <span data-ttu-id="15e9f-119">ComCtl32.dll Version 6 enthält sowohl die Benutzer Steuerelemente als auch die allgemeinen Steuerelemente.</span><span class="sxs-lookup"><span data-stu-id="15e9f-119">ComCtl32.dll version 6 contains both the user controls and the common controls.</span></span> <span data-ttu-id="15e9f-120">Standardmäßig verwenden Anwendungen die in User32.dll definierten Benutzer Steuerelemente und die allgemeinen Steuerelemente, die in ComCtl32.dll Version 5 definiert sind.</span><span class="sxs-lookup"><span data-stu-id="15e9f-120">By default, applications use the user controls defined in User32.dll and the common controls defined in ComCtl32.dll version 5.</span></span> <span data-ttu-id="15e9f-121">Eine Liste der DLL-Versionen und deren Verteilungs Plattformen finden Sie unter [allgemeine Steuerelement Versionen](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="15e9f-121">For a list of DLL versions and their distribution platforms, see [Common Control Versions](common-control-versions.md).</span></span>

<span data-ttu-id="15e9f-122">Wenn Sie möchten, dass Ihre Anwendung visuelle Stile verwendet, müssen Sie ein Anwendungs Manifest oder eine Compilerdirektive hinzufügen, die angibt, dass ComCtl32.dll Version 6 verwendet werden soll, wenn Sie verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="15e9f-122">If you want your application to use visual styles, you must add an application manifest or compiler directive that indicates that ComCtl32.dll version 6 should be used if it is available.</span></span>

<span data-ttu-id="15e9f-123">Ein Anwendungs Manifest ermöglicht einer Anwendung, anzugeben, welche Versionen einer Assembly benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="15e9f-123">An application manifest enables an application to specify which versions of an assembly it requires.</span></span> <span data-ttu-id="15e9f-124">In Microsoft Win32 ist eine Assembly ein Satz von DLLs und eine Liste mit Versions fähigen Objekten, die in diesen DLLs enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="15e9f-124">In Microsoft Win32, an assembly is a set of DLLs and a list of versionable objects that are contained within those DLLs.</span></span>

<span data-ttu-id="15e9f-125">Manifeste werden in XML geschrieben.</span><span class="sxs-lookup"><span data-stu-id="15e9f-125">Manifests are written in XML.</span></span> <span data-ttu-id="15e9f-126">Der Name der Anwendungs Manifest-Datei ist der Name der ausführbaren Datei, gefolgt von der Dateinamenerweiterung. Manifest; beispielsweise MyApp.exe. manifest.</span><span class="sxs-lookup"><span data-stu-id="15e9f-126">The name of the application manifest file is the name of your executable followed by the file name extension .manifest; for example, MyApp.exe.manifest.</span></span> <span data-ttu-id="15e9f-127">Das folgende Beispiel Manifest zeigt, dass im ersten Abschnitt das Manifest selbst beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="15e9f-127">The following sample manifest shows that the first section describes the manifest itself.</span></span> <span data-ttu-id="15e9f-128">In der folgenden Tabelle sind die Attribute aufgeführt, die vom Element **assemblyIdentity** im Abschnitt Beschreibung des Manifests festgelegt wurden.</span><span class="sxs-lookup"><span data-stu-id="15e9f-128">The following table shows the attributes set by the **assemblyIdentity** element in the manifest description section.</span></span>



| <span data-ttu-id="15e9f-129">Attribut</span><span class="sxs-lookup"><span data-stu-id="15e9f-129">Attribute</span></span>             | <span data-ttu-id="15e9f-130">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="15e9f-130">Description</span></span>                                                                                                                 |
|-----------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15e9f-131">version</span><span class="sxs-lookup"><span data-stu-id="15e9f-131">version</span></span>               | <span data-ttu-id="15e9f-132">Version des Manifests.</span><span class="sxs-lookup"><span data-stu-id="15e9f-132">Version of the manifest.</span></span> <span data-ttu-id="15e9f-133">Die Version muss im Format major. Minor. Revision. Build vorliegen (d. h. n. n, wobei n <= 65535).</span><span class="sxs-lookup"><span data-stu-id="15e9f-133">The version must be in the form major.minor.revision.build (that is, n.n.n.n, where n <=65535).</span></span> |
| <span data-ttu-id="15e9f-134">processorArchitecture</span><span class="sxs-lookup"><span data-stu-id="15e9f-134">processorArchitecture</span></span> | <span data-ttu-id="15e9f-135">Der Prozessor, für den die Anwendung entwickelt wird.</span><span class="sxs-lookup"><span data-stu-id="15e9f-135">Processor for which your application is developed.</span></span>                                                                          |
| <span data-ttu-id="15e9f-136">name</span><span class="sxs-lookup"><span data-stu-id="15e9f-136">name</span></span>                  | <span data-ttu-id="15e9f-137">Schließt den Firmennamen, den Produktnamen und den Anwendungsnamen ein.</span><span class="sxs-lookup"><span data-stu-id="15e9f-137">Includes company name, product name and application name.</span></span>                                                                   |
| <span data-ttu-id="15e9f-138">type</span><span class="sxs-lookup"><span data-stu-id="15e9f-138">type</span></span>                  | <span data-ttu-id="15e9f-139">Der Typ der Anwendung, z. b. Win32.</span><span class="sxs-lookup"><span data-stu-id="15e9f-139">Type of your application, such as Win32.</span></span>                                                                                    |



 

<span data-ttu-id="15e9f-140">Das Beispiel Manifest enthält außerdem eine Beschreibung Ihrer Anwendung und gibt Anwendungsabhängigkeiten an.</span><span class="sxs-lookup"><span data-stu-id="15e9f-140">The sample manifest also provides a description of your application and specifies application dependencies.</span></span> <span data-ttu-id="15e9f-141">In der folgenden Tabelle sind die Attribute aufgeführt, die vom **assemblyIdentity** -Element im Abhängigkeits Abschnitt festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="15e9f-141">The following table shows the attributes set by the **assemblyIdentity** element in the dependency section.</span></span>



| <span data-ttu-id="15e9f-142">Attribut</span><span class="sxs-lookup"><span data-stu-id="15e9f-142">Attribute</span></span>             | <span data-ttu-id="15e9f-143">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="15e9f-143">Description</span></span>                                      |
|-----------------------|--------------------------------------------------|
| <span data-ttu-id="15e9f-144">type</span><span class="sxs-lookup"><span data-stu-id="15e9f-144">type</span></span>                  | <span data-ttu-id="15e9f-145">Der Typ der Abhängigkeits Komponente, z. b. Win32.</span><span class="sxs-lookup"><span data-stu-id="15e9f-145">Type of the dependency component, such as Win32.</span></span> |
| <span data-ttu-id="15e9f-146">name</span><span class="sxs-lookup"><span data-stu-id="15e9f-146">name</span></span>                  | <span data-ttu-id="15e9f-147">Der Name der Komponente.</span><span class="sxs-lookup"><span data-stu-id="15e9f-147">Name of the component.</span></span>                           |
| <span data-ttu-id="15e9f-148">version</span><span class="sxs-lookup"><span data-stu-id="15e9f-148">version</span></span>               | <span data-ttu-id="15e9f-149">Version der Komponente.</span><span class="sxs-lookup"><span data-stu-id="15e9f-149">Version of the component.</span></span>                        |
| <span data-ttu-id="15e9f-150">processorArchitecture</span><span class="sxs-lookup"><span data-stu-id="15e9f-150">processorArchitecture</span></span> | <span data-ttu-id="15e9f-151">Prozessor, für den die Komponente entworfen wurde.</span><span class="sxs-lookup"><span data-stu-id="15e9f-151">Processor that the component is designed for.</span></span>    |
| <span data-ttu-id="15e9f-152">PublicKeyToken</span><span class="sxs-lookup"><span data-stu-id="15e9f-152">publicKeyToken</span></span>        | <span data-ttu-id="15e9f-153">Schlüssel Token, das mit dieser Komponente verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="15e9f-153">Key token used with this component.</span></span>              |
| <span data-ttu-id="15e9f-154">language</span><span class="sxs-lookup"><span data-stu-id="15e9f-154">language</span></span>              | <span data-ttu-id="15e9f-155">Die Sprache der Komponente.</span><span class="sxs-lookup"><span data-stu-id="15e9f-155">Language of the component.</span></span>                       |



 

<span data-ttu-id="15e9f-156">Im folgenden finden Sie ein Beispiel für eine Manifest-Datei.</span><span class="sxs-lookup"><span data-stu-id="15e9f-156">Following is an example of a manifest file.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="15e9f-157">Legen Sie den Eintrag **ProcessorArchitecture** auf **"x86"** fest, wenn Ihre Anwendung auf die 32-Bit-Windows-Plattform ausgerichtet ist, oder auf **"amd64"** , wenn die Anwendung auf die Windows-Plattform mit dem 64 Bit</span><span class="sxs-lookup"><span data-stu-id="15e9f-157">Set the **processorArchitecture** entry to **"X86"** if your application targets the 32 bit Windows platform, or to **"amd64"** if your application targets the 64 bit Windows platform.</span></span> <span data-ttu-id="15e9f-158">Sie können auch **" \* "** angeben. Dadurch wird sichergestellt, dass alle Plattformen als Ziel festgelegt werden, wie in den folgenden Beispielen gezeigt.</span><span class="sxs-lookup"><span data-stu-id="15e9f-158">You can also specify **"\*"**, which ensures that all platforms are targeted, as shown in the following examples.</span></span>

 


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



<span data-ttu-id="15e9f-159">Wenn Sie Microsoft Visual C++ 2005 oder höher verwenden, können Sie die folgende Compilerdirektive in Ihren Quellcode einfügen, anstatt ein Manifest manuell zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="15e9f-159">If you are using Microsoft Visual C++ 2005 or later, you can add the following compiler directive to your source code instead of manually creating a manifest.</span></span> <span data-ttu-id="15e9f-160">Zur besseren Lesbarkeit wird die-Direktive hier in mehrere Zeilen aufgeteilt.</span><span class="sxs-lookup"><span data-stu-id="15e9f-160">For readability, the directive is broken into several lines here.</span></span>


```C++
#pragma comment(linker,"\"/manifestdependency:type='win32' \
name='Microsoft.Windows.Common-Controls' version='6.0.0.0' \
processorArchitecture='*' publicKeyToken='6595b64144ccf1df' language='*'\"")
```



<span data-ttu-id="15e9f-161">In den folgenden Themen werden die Schritte zum Anwenden visueller Stile auf verschiedene Anwendungs Typen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="15e9f-161">The following topics describe the steps for applying visual styles to different types of applications.</span></span> <span data-ttu-id="15e9f-162">Beachten Sie, dass das Manifest-Format in jedem Fall identisch ist.</span><span class="sxs-lookup"><span data-stu-id="15e9f-162">Notice that the manifest format is the same in each case.</span></span>

## <a name="using-comctl32dll-version-6-in-an-application-that-uses-only-standard-extensions"></a><span data-ttu-id="15e9f-163">Verwenden von ComCtl32.dll Version 6 in einer Anwendung, die nur Standard Erweiterungen verwendet</span><span class="sxs-lookup"><span data-stu-id="15e9f-163">Using ComCtl32.dll Version 6 in an Application That Uses Only Standard Extensions</span></span>

<span data-ttu-id="15e9f-164">Im folgenden finden Sie Beispiele für Anwendungen, die keine Erweiterungen von Drittanbietern verwenden.</span><span class="sxs-lookup"><span data-stu-id="15e9f-164">The following are examples of applications that do not use third-party extensions.</span></span>

-   <span data-ttu-id="15e9f-165">Rechner</span><span class="sxs-lookup"><span data-stu-id="15e9f-165">Calculator</span></span>
-   <span data-ttu-id="15e9f-166">Freecell</span><span class="sxs-lookup"><span data-stu-id="15e9f-166">FreeCell</span></span>
-   <span data-ttu-id="15e9f-167">Minesweeper</span><span class="sxs-lookup"><span data-stu-id="15e9f-167">Minesweeper</span></span>
-   <span data-ttu-id="15e9f-168">Editor</span><span class="sxs-lookup"><span data-stu-id="15e9f-168">Notepad</span></span>
-   <span data-ttu-id="15e9f-169">Solitär</span><span class="sxs-lookup"><span data-stu-id="15e9f-169">Solitaire</span></span>

<span data-ttu-id="15e9f-170">**, Um ein Manifest zu erstellen und die Anwendung für die Verwendung visueller Stile zu aktivieren.**</span><span class="sxs-lookup"><span data-stu-id="15e9f-170">**To create a manifest and enable your application to use visual styles.**</span></span>

1.  <span data-ttu-id="15e9f-171">Verknüpfung mit Comctl32. lib und [**callinitcommoncontrols**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols).</span><span class="sxs-lookup"><span data-stu-id="15e9f-171">Link to ComCtl32.lib and call [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols).</span></span>
2.  <span data-ttu-id="15e9f-172">Fügen Sie der Quell Struktur, die das XML-Manifest-Format aufweist, eine Datei mit dem Namen YourApp.exe. Manifest hinzu.</span><span class="sxs-lookup"><span data-stu-id="15e9f-172">Add a file called YourApp.exe.manifest to your source tree that has the XML manifest format.</span></span>
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

    

3.  <span data-ttu-id="15e9f-173">Fügen Sie das Manifest wie folgt der Ressourcen Datei Ihrer Anwendung hinzu:</span><span class="sxs-lookup"><span data-stu-id="15e9f-173">Add the manifest to your application's resource file as follows:</span></span>
    ```C++
    CREATEPROCESS_MANIFEST_RESOURCE_ID RT_MANIFEST "YourApp.exe.manifest"
    ```

    

    > [!Note]  
    > <span data-ttu-id="15e9f-174">Wenn Sie den vorherigen Eintrag der Ressource hinzufügen, müssen Sie ihn in einer Zeile formatieren.</span><span class="sxs-lookup"><span data-stu-id="15e9f-174">When you add the previous entry to the resource you must format it on one line.</span></span> <span data-ttu-id="15e9f-175">Alternativ können Sie die XML-Manifest-Datei im gleichen Verzeichnis wie die ausführbare Datei der Anwendung platzieren.</span><span class="sxs-lookup"><span data-stu-id="15e9f-175">Alternatively, you can place the XML manifest file in the same directory as your application's executable file.</span></span> <span data-ttu-id="15e9f-176">Das Betriebssystem lädt das Manifest zuerst aus dem Dateisystem und überprüft dann den Ressourcenabschnitt der ausführbaren Datei.</span><span class="sxs-lookup"><span data-stu-id="15e9f-176">The operating system will load the manifest from the file system first, then check the resource section of the executable.</span></span> <span data-ttu-id="15e9f-177">Die Dateisystem Version hat Vorrang.</span><span class="sxs-lookup"><span data-stu-id="15e9f-177">The file system version takes precedence.</span></span>

     

<span data-ttu-id="15e9f-178">Wenn Sie die Anwendung erstellen, wird das Manifest als binäre Ressource hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="15e9f-178">When you build your application, the manifest will be added as a binary resource.</span></span>

## <a name="using-comctl32-version-6-in-control-panel-or-a-dll-that-is-run-by-rundll32exe"></a><span data-ttu-id="15e9f-179">Verwenden von ComCtl32 Version 6 in der Systemsteuerung oder einer DLL, die von RunDll32.exe ausgeführt wird</span><span class="sxs-lookup"><span data-stu-id="15e9f-179">Using ComCtl32 Version 6 in Control Panel or a DLL That Is Run by RunDll32.exe</span></span>

<span data-ttu-id="15e9f-180">**, Um ein Manifest zu erstellen und die Anwendung für die Verwendung visueller Stile zu aktivieren.**</span><span class="sxs-lookup"><span data-stu-id="15e9f-180">**To create a manifest and enable your application to use visual styles.**</span></span>

1.  <span data-ttu-id="15e9f-181">Verknüpfung mit Comctl32. lib und [**callinitcommoncontrols**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols).</span><span class="sxs-lookup"><span data-stu-id="15e9f-181">Link to ComCtl32.lib and call [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols).</span></span>
2.  <span data-ttu-id="15e9f-182">Fügen Sie der Quell Struktur, die das XML-Manifest-Format aufweist, eine Datei mit dem Namen YourApp.cpl. Manifest hinzu.</span><span class="sxs-lookup"><span data-stu-id="15e9f-182">Add a file called YourApp.cpl.manifest to your source tree that has the XML manifest format.</span></span>
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

    

3.  <span data-ttu-id="15e9f-183">Fügen Sie das Manifest der Ressourcen Datei Ihrer Anwendung als Ressourcen-ID 123 hinzu.</span><span class="sxs-lookup"><span data-stu-id="15e9f-183">Add the manifest to your application's resource file as resource ID 123.</span></span>

> [!Note]  
> <span data-ttu-id="15e9f-184">Wenn Sie eine System Steuerungsanwendung erstellen, platzieren Sie Sie in der entsprechenden Kategorie.</span><span class="sxs-lookup"><span data-stu-id="15e9f-184">When you author a Control Panel application, place it in the appropriate category.</span></span> <span data-ttu-id="15e9f-185">Die Systemsteuerung unterstützt jetzt die Kategorisierung von System Steuerungsanwendungen.</span><span class="sxs-lookup"><span data-stu-id="15e9f-185">Control Panel now supports categorization of Control Panel applications.</span></span> <span data-ttu-id="15e9f-186">Dies bedeutet, dass System Steuerungsanwendungen IDs zugewiesen und in Aufgabenbereiche wie z. b. hinzufügen oder Entfernen von Programmen, Darstellung und Designs oder Datums-, Uhrzeit-, sprach-und Regions Optionen aufgeteilt werden können.</span><span class="sxs-lookup"><span data-stu-id="15e9f-186">This means that Control Panel applications can be assigned identifiers and separated into task areas such as Add or Remove Programs, Appearance and Themes, or Date, Time, Language, and Regional Options.</span></span>

 

## <a name="adding-visual-style-support-to-an-extension-plug-in-mmc-snap-in-or-a-dll-that-is-brought-into-a-process"></a><span data-ttu-id="15e9f-187">Hinzufügen von Unterstützung für visuelle Stile zu einer Erweiterung, einem Plug-in, einem MMC-Snap-in oder einer DLL, die in einen Prozess integriert wird</span><span class="sxs-lookup"><span data-stu-id="15e9f-187">Adding Visual Style Support to an Extension, Plug-in, MMC Snap-in or a DLL That Is Brought into a Process</span></span>

<span data-ttu-id="15e9f-188">Die Unterstützung für visuelle Stile kann zu einer Erweiterung, einem Plug-in, einem MMC-Snap-in oder einer DLL hinzugefügt werden, die in einen Prozess eingebunden wird.</span><span class="sxs-lookup"><span data-stu-id="15e9f-188">Support for visual styles can be added to an extension, plug-in, MMC snap-in, or a DLL that is brought into a process.</span></span> <span data-ttu-id="15e9f-189">Verwenden Sie beispielsweise die folgenden Schritte, um Unterstützung für visuelle Stile für ein Microsoft Management Console (MMC)-Snap-in hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="15e9f-189">For example, use the following steps to add visual styles support for an Microsoft Management Console (MMC) snap-in.</span></span>

1.  <span data-ttu-id="15e9f-190">Kompilieren Sie das Snap-in mit dem Flag "-disolations- \_ \_ fähig", oder fügen Sie die folgende Anweisung vor der \# include-Anweisung "Windows. h" ein.</span><span class="sxs-lookup"><span data-stu-id="15e9f-190">Compile your snap-in with the -DISOLATION\_AWARE\_ENABLED flag or insert the following statement before the \#include "windows.h" statement.</span></span>

    ```C++
    #define ISOLATION_AWARE_ENABLED 1
    ```

    

    <span data-ttu-id="15e9f-191">Weitere Informationen zur \_ \_ aktivierten Isolation finden Sie unter [Isolieren von Komponenten](/windows/desktop/SbsCs/isolating-components).</span><span class="sxs-lookup"><span data-stu-id="15e9f-191">For more information about ISOLATION\_AWARE\_ENABLED, see [Isolating Components](/windows/desktop/SbsCs/isolating-components).</span></span>

2.  <span data-ttu-id="15e9f-192">Schließen Sie die allgemeine Steuerungs Header Datei in die Snap-in-Quelle ein.</span><span class="sxs-lookup"><span data-stu-id="15e9f-192">Include the common control header file in your snap-in source.</span></span>
    ```C++
    #include <commctrl.h>
    ```

    

3.  <span data-ttu-id="15e9f-193">Fügen Sie der Quell Struktur, die das XML-Manifest-Format verwendet, eine Datei namens yourapp. Manifest hinzu.</span><span class="sxs-lookup"><span data-stu-id="15e9f-193">Add a file called YourApp.manifest to your source tree that uses the XML manifest format.</span></span>
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

    

4.  <span data-ttu-id="15e9f-194">Fügen Sie das Manifest der Ressourcen Datei Ihres Snap-Ins hinzu.</span><span class="sxs-lookup"><span data-stu-id="15e9f-194">Add the manifest to your snap-in's resource file.</span></span> <span data-ttu-id="15e9f-195">Weitere Informationen zum Hinzufügen eines Manifests zu einer Ressourcen Datei finden [Sie unter Verwenden von ComCtl32 Version 6 in einer Anwendung, die Erweiterungen, Plug-ins oder eine DLL verwendet, die in einen Prozess eingefügt wird](/previous-versions//ms649781(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="15e9f-195">See [Using ComCtl32 Version 6 in an Application That Uses Extensions, Plug-ins, or a DLL That Is Brought into a Process](/previous-versions//ms649781(v=vs.85)) for details on adding a manifest to a resource file.</span></span>

## <a name="turning-off-visual-styles"></a><span data-ttu-id="15e9f-196">Ausschalten visueller Stile</span><span class="sxs-lookup"><span data-stu-id="15e9f-196">Turning Off Visual Styles</span></span>

<span data-ttu-id="15e9f-197">Sie können visuelle Stile für ein-Steuerelement oder für alle Steuerelemente in einem Fenster deaktivieren, indem Sie die [**SetWindowTheme**](/windows/desktop/api/Uxtheme/nf-uxtheme-setwindowtheme) -Funktion wie folgt aufrufen:</span><span class="sxs-lookup"><span data-stu-id="15e9f-197">You can turn off visual styles for a control or for all controls in a window by calling the [**SetWindowTheme**](/windows/desktop/api/Uxtheme/nf-uxtheme-setwindowtheme) function as follows:</span></span>


```C++
SetWindowTheme(hwnd, L" ", L" ");
```



<span data-ttu-id="15e9f-198">Im vorherigen Beispiel ist *HWND* das Handle des Fensters, in dem visuelle Stile deaktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="15e9f-198">In the previous example, *hwnd* is the handle of the window in which to disable visual styles.</span></span> <span data-ttu-id="15e9f-199">Nach dem-Befehl wird das-Steuerelement ohne visuelle Stile gerendert.</span><span class="sxs-lookup"><span data-stu-id="15e9f-199">After the call, the control renders without visual styles.</span></span>

## <a name="using-visual-styles-with-html-content"></a><span data-ttu-id="15e9f-200">Verwenden von visuellen Stilen mit HTML-Inhalten</span><span class="sxs-lookup"><span data-stu-id="15e9f-200">Using Visual Styles with HTML Content</span></span>

<span data-ttu-id="15e9f-201">Auf HTML-Seiten, die die Eigenschaften des Cascading Stylesheets (CSS) ändern (z. b. Hintergrund oder Rahmen), werden keine visuellen Stile auf Sie angewendet.</span><span class="sxs-lookup"><span data-stu-id="15e9f-201">HTML pages that modify the Cascading Style Sheets (CSS) properties such as background or border do not have visual styles applied to them.</span></span> <span data-ttu-id="15e9f-202">Sie zeigen das angegebene CSS-Attribut an.</span><span class="sxs-lookup"><span data-stu-id="15e9f-202">They display the specified CSS attribute.</span></span> <span data-ttu-id="15e9f-203">Wenn die meisten CSS-Eigenschaften als Teil des Inhalts angegeben werden, gelten die meisten CSS-Eigenschaften für Elemente, auf die visuelle Stile angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="15e9f-203">When specified as part of the content, most CSS properties do apply to elements that have visual styles applied.</span></span>

<span data-ttu-id="15e9f-204">Standardmäßig werden visuelle Stile auf die systeminternen HTML-Steuerelemente auf Seiten angewendet, die in Microsoft Internet Explorer 6 und höheren Versionen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="15e9f-204">By default, visual styles are applied to intrinsic HTML controls on pages displayed in Microsoft Internet Explorer 6 and later versions.</span></span> <span data-ttu-id="15e9f-205">Um visuelle Stile für eine HTML-Seite zu deaktivieren, fügen Sie ein Meta-Tag zum</span><span class="sxs-lookup"><span data-stu-id="15e9f-205">To turn off visual styles for an HTML page, add a META tag to the</span></span> <head> <span data-ttu-id="15e9f-206">-Abschnitt.</span><span class="sxs-lookup"><span data-stu-id="15e9f-206">section.</span></span> <span data-ttu-id="15e9f-207">Dieses Verfahren gilt auch für Inhalte, die als HTML-Anwendungen (HTAs) verpackt sind.</span><span class="sxs-lookup"><span data-stu-id="15e9f-207">This technique also applies to content packaged as HTML Applications (HTAs).</span></span> <span data-ttu-id="15e9f-208">Um visuelle Stile zu deaktivieren, muss das Meta-Tag wie folgt lauten:</span><span class="sxs-lookup"><span data-stu-id="15e9f-208">To turn off visual styles, the META tag must be as follows:</span></span>


```
<META HTTP-EQUIV="MSThemeCompatible" CONTENT="no">
```



> [!Note]  
> <span data-ttu-id="15e9f-209">Wenn die Browsereinstellung und die tageinstellung nicht übereinstimmen, werden auf der Seite keine visuellen Stile angewendet.</span><span class="sxs-lookup"><span data-stu-id="15e9f-209">If the browser setting and the tag setting do not agree, the page will not apply visual styles.</span></span> <span data-ttu-id="15e9f-210">Wenn das Meta-Tag beispielsweise auf "No" festgelegt ist und der Browser so festgelegt ist, dass visuelle Stile aktiviert werden, werden visuelle Stile nicht auf die Seite angewendet.</span><span class="sxs-lookup"><span data-stu-id="15e9f-210">For example, if the META tag is set to "no" and the browser is set to enable visual styles, visual styles will not be applied to the page.</span></span> <span data-ttu-id="15e9f-211">Wenn jedoch entweder der Browser oder das Meta-Tag auf "yes" festgelegt ist und das andere Element nicht angegeben ist, werden visuelle Stile angewendet.</span><span class="sxs-lookup"><span data-stu-id="15e9f-211">However, if either the browser or META tag is set to "yes" and the other item is not specified, visual styles will be applied.</span></span>

 

<span data-ttu-id="15e9f-212">Visuelle Stile können das Layout Ihrer Inhalte ändern.</span><span class="sxs-lookup"><span data-stu-id="15e9f-212">Visual styles might change the layout of your content.</span></span> <span data-ttu-id="15e9f-213">Wenn Sie bestimmte Attribute auf systeminternen HTML-Steuerelementen festlegen, wie z. b. die Breite einer Schaltfläche, können Sie feststellen, dass die Bezeichnung auf der Schaltfläche unter bestimmte visuelle Stile nicht lesbar ist.</span><span class="sxs-lookup"><span data-stu-id="15e9f-213">Also, if you set certain attributes on intrinsic HTML controls, such as the width of a button, you might find that the label on the button is unreadable under certain visual styles.</span></span>

<span data-ttu-id="15e9f-214">Sie müssen Ihre Inhalte mit visuellen Stilen gründlich testen, um zu bestimmen, ob das Anwenden visueller Stile eine negative Auswirkung auf ihren Inhalt und Ihr Layout hat.</span><span class="sxs-lookup"><span data-stu-id="15e9f-214">You must thoroughly test your content using visual styles to determine whether applying visual styles has an adverse effect on your content and layout.</span></span>

## <a name="when-visual-styles-are-not-applied"></a><span data-ttu-id="15e9f-215">Wenn visuelle Stile nicht angewendet werden</span><span class="sxs-lookup"><span data-stu-id="15e9f-215">When Visual Styles are not Applied</span></span>

<span data-ttu-id="15e9f-216">Um zu vermeiden, dass visuelle Stile auf ein Fenster der obersten Ebene angewendet werden, weisen Sie dem Fenster einen nicht-NULL-Bereich (**setwindowrgn**) zu.</span><span class="sxs-lookup"><span data-stu-id="15e9f-216">To avoid applying visual styles to a top level window, give the window a non-null region (**SetWindowRgn**).</span></span> <span data-ttu-id="15e9f-217">Das System geht davon aus, dass ein Fenster mit einer nicht-NULL-Region ein spezielles Fenster ist, in dem keine visuellen Stile verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="15e9f-217">The system assumes that a window with a non-NULL region is a specialized window that does not use visual styles.</span></span> <span data-ttu-id="15e9f-218">Ein untergeordnetes Fenster, das einem Fenster auf oberster Ebene der nicht visuellen Stile zugeordnet ist, kann dennoch visuelle Stile anwenden, auch wenn das übergeordnete Fenster dies nicht tut.</span><span class="sxs-lookup"><span data-stu-id="15e9f-218">A child window associated with a non-visual-styles top level window may still apply visual styles even though the parent window does not.</span></span>

<span data-ttu-id="15e9f-219">Wenn Sie die Verwendung visueller Stile für alle Fenster in der Anwendung deaktivieren möchten, rufen Sie [**settemeappproperties**](/windows/desktop/api/Uxtheme/nf-uxtheme-setthemeappproperties) auf, und übergeben Sie das Flag "STAP \_ Allow \_ nonclient" nicht.</span><span class="sxs-lookup"><span data-stu-id="15e9f-219">If you want to disable the use of visual styles for all windows in your application, call [**SetThemeAppProperties**](/windows/desktop/api/Uxtheme/nf-uxtheme-setthemeappproperties) and do not pass the STAP\_ALLOW\_NONCLIENT flag.</span></span> <span data-ttu-id="15e9f-220">Wenn eine Anwendung **settemeappproperties** nicht aufruft, werden die angenommenen Flagwerte STAP \_ Allow \_ nonclient STAP Allow Control STAP Allow \| \_ \_ \| \_ \_ Webcontent.</span><span class="sxs-lookup"><span data-stu-id="15e9f-220">If an application does not call **SetThemeAppProperties**, the assumed flag values are STAP\_ALLOW\_NONCLIENT \| STAP\_ALLOW\_CONTROLS \| STAP\_ALLOW\_WEBCONTENT.</span></span> <span data-ttu-id="15e9f-221">Die angenommenen Werte bewirken, dass der nicht-Client Bereich, die Steuerelemente und Webinhalte auf einen visuellen Stil angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="15e9f-221">The assumed values cause the nonclient area, the controls, and web content to have a visual style applied.</span></span>

## <a name="making-your-application-compatible-with-earlier-versions-of-windows"></a><span data-ttu-id="15e9f-222">Kompatibilität Ihrer Anwendung mit früheren Versionen von Windows</span><span class="sxs-lookup"><span data-stu-id="15e9f-222">Making Your Application Compatible with Earlier Versions of Windows</span></span>

<span data-ttu-id="15e9f-223">Ein Großteil der Architektur des visuellen Stils ist so konzipiert, dass es einfach ist, Ihr Produkt in früheren Versionen von Windows bereitzustellen, die das Ändern der Darstellung von Steuerelementen nicht unterstützen.</span><span class="sxs-lookup"><span data-stu-id="15e9f-223">Much of the visual style architecture is designed to make it simple to continue to ship your product on earlier versions of Windows that do not support changing the appearance of controls.</span></span> <span data-ttu-id="15e9f-224">Beachten Sie Folgendes, wenn Sie eine Anwendung für mehr als ein Betriebssystem versenden:</span><span class="sxs-lookup"><span data-stu-id="15e9f-224">When shipping an application for more than one operating system, be aware of the following:</span></span>

-   <span data-ttu-id="15e9f-225">In Windows-Versionen vor Windows 8 sind visuelle Stile deaktiviert, wenn ein hoher Kontrast auf on steht.</span><span class="sxs-lookup"><span data-stu-id="15e9f-225">In versions of Windows prior to Windows 8, visual styles are off when high contrast is on.</span></span> <span data-ttu-id="15e9f-226">Um einen hohen Kontrast zu unterstützen, muss eine ältere Anwendung, die visuelle Stile unterstützt, einen separaten Codepfad bereitstellen, um Benutzeroberflächen Elemente im hohen Kontrast korrekt zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="15e9f-226">To support high contrast, a legacy application that supports visual styles needs to provide a separate code path to properly draw UI elements in high contrast.</span></span> <span data-ttu-id="15e9f-227">In Windows 8 ist der hohe Kontrast ein Teil von visuellen Stilen. eine Windows 8-Anwendung (eine mit der Windows 8-GUID im Kompatibilitäts Abschnitt des Anwendungs Manifests) muss jedoch immer noch einen separaten Codepfad bereitstellen, um im hohen Kontrast zu Windows 7 einem früheren Zeitpunkt ordnungsgemäß zu Rendering.</span><span class="sxs-lookup"><span data-stu-id="15e9f-227">In Windows 8, high contrast is a part of visual styles; however, a Windows 8 application (one that includes the Windows 8 GUID in compatibility section of its application manifest) still needs to provide a separate code path to render correctly in high contrast on Windows 7 an earlier.</span></span>
-   <span data-ttu-id="15e9f-228">Wenn Sie die Funktionen in ComCtl32.dll Version 6 verwenden (z. b. die Kachel Ansicht oder das Link Steuerelement), müssen Sie den Fall behandeln, in dem diese Steuerelemente auf dem Computer des Benutzers nicht verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="15e9f-228">If you use the features in ComCtl32.dll version 6, such as the tile view or link control, you must handle the case where those controls are not available on your user's computer.</span></span> <span data-ttu-id="15e9f-229">ComCtl32.dll Version 6 ist nicht Verteil Bar.</span><span class="sxs-lookup"><span data-stu-id="15e9f-229">ComCtl32.dll version 6 is not redistributable.</span></span>
-   <span data-ttu-id="15e9f-230">Testen Sie Ihre Anwendung, um sicherzustellen, dass Sie sich nicht auf Features von ComCtl32.dll Version 6 verlassen, ohne zuerst die aktuelle Version zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="15e9f-230">Test your application to make sure you are not relying on features of ComCtl32.dll version 6 without first checking for the current version.</span></span>
-   <span data-ttu-id="15e9f-231">Nicht mit "uxtheme. lib" verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="15e9f-231">Do not link to UxTheme.lib.</span></span>
-   <span data-ttu-id="15e9f-232">Schreiben Sie Fehler Behandlungs Code für-Instanzen, wenn visuelle Stile nicht erwartungsgemäß funktionieren.</span><span class="sxs-lookup"><span data-stu-id="15e9f-232">Write error-handling code for instances when visual styles do not work as expected.</span></span>
-   <span data-ttu-id="15e9f-233">Wenn Sie das Manifest der Anwendung in früheren Versionen installieren, wirkt sich dies nicht auf das Rendering von Steuerelementen aus.</span><span class="sxs-lookup"><span data-stu-id="15e9f-233">Installing your application's manifest in earlier versions will not affect the rendering of controls.</span></span>

## <a name="related-topics"></a><span data-ttu-id="15e9f-234">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="15e9f-234">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="15e9f-235">Visuelle Stile</span><span class="sxs-lookup"><span data-stu-id="15e9f-235">Visual Styles</span></span>](themes-overview.md)
</dt> </dl>

 

 