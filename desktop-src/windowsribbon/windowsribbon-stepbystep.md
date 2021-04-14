---
title: Erstellen einer Menü Bandanwendung
description: Das Windows-Menüband-Framework besteht aus zwei unterschiedlichen, aber abhängigen Entwicklungsplattformen, eine Markup Sprache, die auf Extensible Application Markup Language (XAML) basiert, um Steuerelemente und deren visuelles Layout zu deklarieren, sowie einen auf C++ Component Object Model (com) basierenden Satz von Schnittstellen zum Definieren von Befehls Funktionalität und anwendungshooks. Diese Arbeitsabteilung innerhalb der Multifunktionsleisten-Framework-Architektur erfordert, dass ein Entwickler, der die umfassenden Benutzeroberflächen Funktionen des Frameworks nutzen möchte, die Benutzeroberfläche im Markup entwerfen und beschreiben muss und dann die COM-Schnittstellen des Menüband-Frameworks verwenden, um das Framework mit der Host Anwendung zu verbinden.
ms.assetid: 1bd3dbb5-822b-4551-8330-8b202a4cecdf
keywords:
- Windows-Menüband, Erstellen von Anwendungen
- Multifunktionsleiste, Erstellen von Anwendungen
- Windows-Menüband, Roadmap
- Menüband, Roadmap
- Windows-Menüband, Markup
- Menüband, Markup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a10f683c7fbb07b9992e418a4c09dc9aecba280
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390740"
---
# <a name="creating-a-ribbon-application"></a><span data-ttu-id="171c3-110">Erstellen einer Menü Bandanwendung</span><span class="sxs-lookup"><span data-stu-id="171c3-110">Creating a Ribbon Application</span></span>

<span data-ttu-id="171c3-111">Das Windows-Menüband-Framework besteht aus zwei unterschiedlichen, aber abhängigen Entwicklungsplattformen: einer Markup Sprache, die auf Extensible Application Markup Language (XAML) basiert, um Steuerelemente und deren visuelles Layout zu deklarieren, und einem auf C++ Component Object Model (com) basierenden Satz von Schnittstellen zum Definieren von Befehls Funktionalität und anwendungshooks.</span><span class="sxs-lookup"><span data-stu-id="171c3-111">The Windows Ribbon framework is composed of two distinct, yet dependent, development platforms: a markup language based on Extensible Application Markup Language (XAML) to declare controls and their visual layout, and a C++ Component Object Model (COM)-based set of interfaces to define command functionality and application hooks.</span></span> <span data-ttu-id="171c3-112">Diese Arbeitsabteilung innerhalb der Multifunktionsleisten-Framework-Architektur erfordert, dass ein Entwickler, der die umfassenden Benutzeroberflächen Funktionen des Frameworks nutzen möchte, die Benutzeroberfläche im Markup entwerfen und beschreiben muss und dann die COM-Schnittstellen des Menüband-Frameworks verwenden, um das Framework mit der Host Anwendung zu verbinden.</span><span class="sxs-lookup"><span data-stu-id="171c3-112">This division of labor within the Ribbon framework architecture requires that a developer who wants to take advantage of the rich UI capabilities offered by the framework must design and describe the UI in markup, and then use the Ribbon framework COM interfaces to connect the framework to the host application.</span></span>

-   [<span data-ttu-id="171c3-113">Menüband-Roadmap</span><span class="sxs-lookup"><span data-stu-id="171c3-113">Ribbon Roadmap</span></span>](#ribbon-roadmap)
-   [<span data-ttu-id="171c3-114">Schreiben des Markups</span><span class="sxs-lookup"><span data-stu-id="171c3-114">Write the Markup</span></span>](#write-the-markup)
    -   [<span data-ttu-id="171c3-115">Markup kompilieren</span><span class="sxs-lookup"><span data-stu-id="171c3-115">Compile the Markup</span></span>](#compile-the-markup)
-   [<span data-ttu-id="171c3-116">Erstellen der Anwendung</span><span class="sxs-lookup"><span data-stu-id="171c3-116">Build the Application</span></span>](#build-the-application)
    -   [<span data-ttu-id="171c3-117">Initialisieren der Multifunktionsleiste</span><span class="sxs-lookup"><span data-stu-id="171c3-117">Initialize the Ribbon</span></span>](#initialize-the-ribbon)
    -   [<span data-ttu-id="171c3-118">Das Markup mit der Anwendung verknüpfen</span><span class="sxs-lookup"><span data-stu-id="171c3-118">Link the Markup to the Application</span></span>](#link-the-markup-to-the-application)
    -   [<span data-ttu-id="171c3-119">Kompilieren der Anwendung</span><span class="sxs-lookup"><span data-stu-id="171c3-119">Compile the Application</span></span>](#link-the-markup-to-the-application)
-   [<span data-ttu-id="171c3-120">Lauf Zeit Updates und Ausführungen</span><span class="sxs-lookup"><span data-stu-id="171c3-120">Run Time Updates and Executions</span></span>](#run-time-updates-and-executions)
-   [<span data-ttu-id="171c3-121">OLE-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="171c3-121">OLE Support</span></span>](#ole-support)
-   [<span data-ttu-id="171c3-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="171c3-122">Related topics</span></span>](#related-topics)

## <a name="ribbon-roadmap"></a><span data-ttu-id="171c3-123">Menüband-Roadmap</span><span class="sxs-lookup"><span data-stu-id="171c3-123">Ribbon Roadmap</span></span>

<span data-ttu-id="171c3-124">Die visuellen Aspekte einer Menü Bandanwendung, wie z. b. welche Steuerelemente angezeigt werden und wo Sie platziert werden, werden im Markup deklariert (siehe [Deklarieren von Befehlen und Steuerelementen mit Menüband-Markup](windowsribbon-schema.md)).</span><span class="sxs-lookup"><span data-stu-id="171c3-124">The visual aspects of a Ribbon application, such as what controls are displayed and where they are placed, are declared in markup (see [Declaring Commands and Controls with Ribbon Markup](windowsribbon-schema.md)).</span></span> <span data-ttu-id="171c3-125">Die Anwendungs Befehls Logik, z. b. Was geschieht, wenn eine Schaltfläche gedrückt wird, wird im Code implementiert.</span><span class="sxs-lookup"><span data-stu-id="171c3-125">The application command logic, such as what happens when a button is pressed, is implemented in code.</span></span>

<span data-ttu-id="171c3-126">Der Prozess der Implementierung eines Menübands und der Einbindung in eine Windows-Anwendung erfordert vier grundlegende Aufgaben: Schreiben Sie das Markup, kompilieren Sie das Markup, schreiben Sie den Code, und kompilieren und verknüpfen Sie die gesamte Anwendung.</span><span class="sxs-lookup"><span data-stu-id="171c3-126">The process of implementing a Ribbon and incorporating it into a Windows application requires four basic tasks: write the markup, compile the markup, write the code, and compile and link the entire application.</span></span>

<span data-ttu-id="171c3-127">Das folgende Diagramm veranschaulicht den Workflow für eine typische multifunktionsleistenimplementierung.</span><span class="sxs-lookup"><span data-stu-id="171c3-127">The following diagram illustrates the workflow for a typical Ribbon implementation.</span></span>

![das Diagramm zeigt den Workflow für eine typische Multifunktionsleisten Implementierung.](images/overviews/ribbonroadmap.png)

<span data-ttu-id="171c3-129">In den folgenden Abschnitten wird dieser Prozess ausführlicher beschrieben.</span><span class="sxs-lookup"><span data-stu-id="171c3-129">The following sections describe this process in more detail.</span></span>

## <a name="write-the-markup"></a><span data-ttu-id="171c3-130">Schreiben des Markups</span><span class="sxs-lookup"><span data-stu-id="171c3-130">Write the Markup</span></span>

<span data-ttu-id="171c3-131">Nachdem die Multifunktionsleisten-Benutzeroberfläche entworfen wurde, besteht die erste Aufgabe für einen Anwendungsentwickler darin, die Benutzeroberfläche mit Menüband-Markup zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="171c3-131">After the Ribbon UI has been designed, the first task for an application developer is to describe the UI with Ribbon markup.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="171c3-132">Die Markup Schema Datei uicc. xsd von Ribbon Framework wird mit dem Microsoft Windows Software Development Kit (SDK) für Windows 7 und .NET Framework 4,0 installiert.</span><span class="sxs-lookup"><span data-stu-id="171c3-132">The Ribbon framework markup schema file, UICC.xsd, is installed with the Microsoft Windows Software Development Kit (SDK) for Windows 7 and .NET Framework 4.0.</span></span> <span data-ttu-id="171c3-133">Wenn Sie den Standard Installationspfad verwenden, befindet sich die Datei im Ordner% Program Files% \\ Microsoft sdert \\ Windows \\ \[ Version Number bin, in \] \\ dem von vielen XML-Editoren auf Sie verwiesen werden kann, um Hinweise und automatische Vervollständigung bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="171c3-133">Using the standard installation path, the file is located in the %ProgramFiles%\\Microsoft SDKs\\Windows\\\[version number\]\\Bin folder where it can be referenced by many XML editors to provide hinting and auto-completion.</span></span>

 

<span data-ttu-id="171c3-134">Menü Band Steuerelemente, Menü Band Befehle (die Steuerelement unabhängigen Elemente, die die Basisfunktionalität für Menüband-Steuerelemente bereitstellen), und das gesamte Steuerelement Layout und visuelle Beziehungen werden im Markup deklariert.</span><span class="sxs-lookup"><span data-stu-id="171c3-134">Ribbon controls, Ribbon Commands (the control-independent elements that provide the base functionality for Ribbon controls), and all control layout and visual relationships are declared in markup.</span></span> <span data-ttu-id="171c3-135">Die Struktur des Menü Band Markups hebt den Unterschied zwischen Menüband-Steuerelementen und Befehlen durch zwei primäre Knoten Hierarchien hervor: eine Struktur von [Befehlen und Ressourcen](windowsribbon-reference-elements-command.md) [sowie eine](windowsribbon-reference-elements-view.md) Ansichts Struktur.</span><span class="sxs-lookup"><span data-stu-id="171c3-135">The structure of the Ribbon markup emphasizes the distinction between Ribbon controls and Commands through two primary node hierarchies: a [Commands and Resources](windowsribbon-reference-elements-command.md) tree and a [Views](windowsribbon-reference-elements-view.md) tree.</span></span>

<span data-ttu-id="171c3-136">Alle Container und Aktionen, die über das Menüband verfügbar gemacht werden, werden in der Struktur " [Befehle und Ressourcen](windowsribbon-reference-elements-command.md) " deklariert.</span><span class="sxs-lookup"><span data-stu-id="171c3-136">All containers and actions that are exposed by the Ribbon are declared in the [Commands and Resources](windowsribbon-reference-elements-command.md) tree.</span></span> <span data-ttu-id="171c3-137">Jedes Command-Element ist einem Satz von Ressourcen zugeordnet, die vom Benutzeroberflächen Entwurf benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="171c3-137">Each Command element is associated with a set of resources, as required by the UI design.</span></span>

<span data-ttu-id="171c3-138">Nachdem Sie die Befehle für eine Anwendung erstellt haben, deklarieren Sie Steuerelemente in der Struktur [Sichten](windowsribbon-reference-elements-view.md) und binden jedes Steuerelement an einen Befehl, um die Befehls Funktionalität verfügbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="171c3-138">After you create the Commands for an application, you declare controls in the [Views](windowsribbon-reference-elements-view.md) tree and bind each control to a Command to expose the Command functionality.</span></span> <span data-ttu-id="171c3-139">Das Menüband-Framework bestimmt die tatsächliche Positionierung der Steuerelemente auf der Grundlage der hier deklarierten Steuerelement Hierarchie.</span><span class="sxs-lookup"><span data-stu-id="171c3-139">The Ribbon framework determines the actual positioning of the controls based on the Control hierarchy declared here.</span></span>

<span data-ttu-id="171c3-140">Im folgenden Codebeispiel wird veranschaulicht, wie Sie ein Schaltflächen-Steuerelement mit der Bezeichnung Exit Application deklarieren und einem Exit-Befehl zuordnen.</span><span class="sxs-lookup"><span data-stu-id="171c3-140">The following code example illustrates how to declare a Button control, labeled Exit application, and associate it with an Exit Command.</span></span>


```
<Application xmlns="http://schemas.microsoft.com/windows/2009/Ribbon">
  <Application.Commands>
    <Command Name="cmdExit" LabelTitle="Exit application" />
  </Application.Commands>

  <Application.Views>
    <Ribbon>
      <Ribbon.Tabs>
        <Tab>
          <Group>
            <Button CommandName="cmdExit" />
          </Group>
        </Tab>
      </Ribbon.Tabs>
    </Ribbon>
  </Application.Views>
</Application>
        
```



> [!TIP]
> <span data-ttu-id="171c3-141">Obwohl es möglich ist, eine beliebige Dateinamenerweiterung für die Menüband-Markup Datei zu verwenden, ist XML die empfohlene Erweiterung, die in der gesamten Dokumentation verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="171c3-141">While it is possible to use any file name extension for the Ribbon markup file, .xml is the recommended extension that is used throughout the documentation.</span></span>

 

### <a name="compile-the-markup"></a><span data-ttu-id="171c3-142">Markup kompilieren</span><span class="sxs-lookup"><span data-stu-id="171c3-142">Compile the Markup</span></span>

<span data-ttu-id="171c3-143">Nachdem die Menüband-Markup Datei erstellt wurde, muss Sie vom Menüband-Markup Compiler (UICC), der im Windows-Software Development Kit (SDK) enthalten ist, in ein binäres Format kompiliert werden.</span><span class="sxs-lookup"><span data-stu-id="171c3-143">After the Ribbon markup file is created, it must be compiled into a binary format by the Ribbon markup compiler, UI Command Compiler (UICC), that is included with the Windows software development kit (SDK).</span></span> <span data-ttu-id="171c3-144">Ein Verweis auf diese Binärdatei wird während der Initialisierung des Menüband-Frameworks von der Host Anwendung an die [**iuiframework:: loadui**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-loadui) -Methode übermittelt.</span><span class="sxs-lookup"><span data-stu-id="171c3-144">A reference to this binary file is passed to the [**IUIFramework::LoadUI**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-loadui) method during initialization of the Ribbon framework by the host application.</span></span>

<span data-ttu-id="171c3-145">UICC kann direkt über ein Befehlszeilenfenster ausgeführt oder als "benutzerdefinierter Buildschritt" in Visual Studio hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="171c3-145">UICC can be executed directly from a command-line window or added as a "Custom Build Step" in Visual Studio.</span></span>

<span data-ttu-id="171c3-146">In der folgenden Abbildung wird der UICC Markup Compiler im Windows 7 SDK-cmd-Shellfenster gezeigt.</span><span class="sxs-lookup"><span data-stu-id="171c3-146">The following image shows the UICC markup compiler in the Windows 7 SDK CMD Shell window.</span></span>

![Screenshot, der uicc.exe in einem Befehlszeilenfenster anzeigt.](images/overviews/screenshot-intentcl-commandline.png)

<span data-ttu-id="171c3-148">Die folgende Abbildung zeigt UICC, das als benutzerdefinierter Buildschritt in Visual Studio hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="171c3-148">The following image shows UICC added as a Custom Build Step in Visual Studio.</span></span>

![Screenshot, der zeigt, uicc.exe als benutzerdefinierter Buildschritt in Visual Studio hinzugefügt wurde.](images/overviews/screenshot-vs-intentcl-custombuildstep.png)

<span data-ttu-id="171c3-150">Das UICC generiert drei Dateien: eine binäre Version des Markups (. BML), einen ID-Definitions Header (h-Datei) zum verfügbar machen von Markup Elementen für die Menüband-Host Anwendung und ein [Ressourcen Definitions Skript](../menurc/about-resource-files.md) (RC-Datei), um das Menüband Bild und die Zeichen folgen Ressourcen zur Kompilierzeit mit der Host Anwendung zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="171c3-150">The UICC generates three files: a binary version of the markup (.bml), an ID definition header (.h file) to expose markup elements to the Ribbon host application, and a [resource-definition script](../menurc/about-resource-files.md) (.rc file) to link Ribbon image and string resources to the host application at compile time.</span></span>

<span data-ttu-id="171c3-151">Ausführlichere Informationen zum Kompilieren von Multifunktionsleisten-Frameworks finden Sie unter Kompilieren von Menü [Band Markup](windowsribbon-intentcl.md).</span><span class="sxs-lookup"><span data-stu-id="171c3-151">For more detail on compiling Ribbon framework markup, see [Compiling Ribbon Markup](windowsribbon-intentcl.md).</span></span>

## <a name="build-the-application"></a><span data-ttu-id="171c3-152">Erstellen der Anwendung</span><span class="sxs-lookup"><span data-stu-id="171c3-152">Build the Application</span></span>

<span data-ttu-id="171c3-153">Nachdem die vorläufige Benutzeroberfläche für eine Multifunktionsleistenanwendung im Markup entworfen und implementiert wurde, muss der Anwendungscode geschrieben werden, der das Framework initialisiert, das Markup nutzt und die im Markup deklarierten Befehle an die entsprechenden Befehls Handler in der Anwendung bindet.</span><span class="sxs-lookup"><span data-stu-id="171c3-153">Once the preliminary UI for a Ribbon application has been designed and implemented in markup, application code must be written that initializes the framework, consumes the markup, and binds the Commands declared in the markup to the appropriate Command handlers in the application.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="171c3-154">Da das Multifunktionsleisten-Framework com-basiert ist, wird empfohlen, dass Menü Bandprojekte den \_ \_ uuidof ()-Operator verwenden, um auf die GUIDs für Menüband Framework-Schnittstellen (IIDs) zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="171c3-154">Since the Ribbon framework is COM-based, it is recommended that Ribbon projects use the \_\_uuidof() operator to reference the GUIDs for Ribbon framework interfaces (IIDs).</span></span> <span data-ttu-id="171c3-155">In Fällen, in denen es nicht möglich ist, den \_ \_ uuidof ()-Operator zu verwenden, z. b. Wenn ein nicht-Microsoft-Compiler verwendet oder die Host Anwendung C-basiert ist, müssen die IIDs von der Anwendung definiert werden, da Sie nicht in UUID. lib enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="171c3-155">In those cases where it is not possible to use the \_\_uuidof() operator, such as when a non-Microsoft compiler is used or the host application is C-based, the IIDs must be defined by the application since they are not contained in uuid.lib.</span></span>
>
> <span data-ttu-id="171c3-156">Wenn die IIDs von der Anwendung definiert werden, müssen die in uiribbon. idl angegebenen GUIDs verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="171c3-156">If the IIDs are defined by the application then the GUIDs specified in UIRibbon.idl must be used.</span></span>
>
> <span data-ttu-id="171c3-157">Uiribbon. idl ist Teil des [Windows Software Development Kit (SDK)](https://msdn.microsoft.com/windows/bb980924.aspx) und befindet sich im Standard Installationspfad von% Program Files% \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ include.</span><span class="sxs-lookup"><span data-stu-id="171c3-157">UIRibbon.idl ships as part of the [Windows Software Development Kit (SDK)](https://msdn.microsoft.com/windows/bb980924.aspx) and can be found at the standard installation path of %ProgramFiles%\\Microsoft SDKs\\Windows\\v7.0\\Include.</span></span>

 

### <a name="initialize-the-ribbon"></a><span data-ttu-id="171c3-158">Initialisieren der Multifunktionsleiste</span><span class="sxs-lookup"><span data-stu-id="171c3-158">Initialize the Ribbon</span></span>

<span data-ttu-id="171c3-159">Das folgende Diagramm veranschaulicht die Schritte, die zum Implementieren einer einfachen Multifunktionsleistenanwendung erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="171c3-159">The following diagram illustrates the steps required to implement a simple Ribbon application.</span></span>

![Diagramm mit den Schritten, die zum Implementieren einer einfachen Multifunktionsleisten-Implementierung erforderlich sind.](images/overviews/initializationsteps.png)

<span data-ttu-id="171c3-161">In den folgenden Schritten wird ausführlich beschrieben, wie eine einfache Menü Bandanwendung implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="171c3-161">The following steps describe in detail how to implement a simple Ribbon application.</span></span>

1.  <span data-ttu-id="171c3-162">CoCreateInstance</span><span class="sxs-lookup"><span data-stu-id="171c3-162">CoCreateInstance</span></span>

    <span data-ttu-id="171c3-163">Die Anwendung ruft die com-Standard-cokreateinstance-Funktion mit der Multifunktionsleisten-Framework-Klassen-ID auf, um einen Zeiger auf das Framework abzurufen.</span><span class="sxs-lookup"><span data-stu-id="171c3-163">The application calls the standard COM CoCreateInstance function with the Ribbon framework class ID to obtain a pointer to the framework.</span></span>

    ```
    IUIFramework* pFramework = NULL;
    HRESULT hr = ::CoCreateInstance(
                CLSID_UIRibbonFramework, 
                NULL,
                CLSCTX_INPROC_SERVER, 
                IID_PPV_ARGS(&pFramework));
    if (FAILED(hr))
    {
      return hr;
    }
    ```

    

2.  <span data-ttu-id="171c3-164">Initialisieren (HWND, iuiapplication \* )</span><span class="sxs-lookup"><span data-stu-id="171c3-164">Initialize(hwnd, IUIApplication\*)</span></span>

    <span data-ttu-id="171c3-165">Die Anwendung ruft [**iuiframework:: Initialize**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-initialize)auf und übergibt zwei Parameter: das Handle für das Fenster auf oberster Ebene, das das Menüband enthält, und einen Zeiger auf die [**iuiapplication**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication) -Implementierung, die es dem Framework ermöglicht, Rückrufe für die Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="171c3-165">The application calls [**IUIFramework::Initialize**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-initialize), passing in two parameters: the handle to the top-level window that will contain the Ribbon and a pointer to the [**IUIApplication**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication) implementation that allows the framework to make callbacks to the application.</span></span>

    > <span data-ttu-id="171c3-166">\[! Wichtig\]</span><span class="sxs-lookup"><span data-stu-id="171c3-166">\[!Important\]</span></span>  
    > <span data-ttu-id="171c3-167">Das Menüband-Framework wird als Single Thread-Apartment (STA) initialisiert.</span><span class="sxs-lookup"><span data-stu-id="171c3-167">The Ribbon framework is initialized as a single-threaded apartment (STA).</span></span>

     

    ```
    hr = pFramework->Initialize(hWndHost, pApplication);
    if (FAILED(hr))
    {
      return hr;
    }
    ```

    

3.  <span data-ttu-id="171c3-168">Loadui (Instanz, resourceName)</span><span class="sxs-lookup"><span data-stu-id="171c3-168">LoadUI(instance, resourceName)</span></span>

    <span data-ttu-id="171c3-169">Die Anwendung ruft [**iuiframework:: loadui**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-loadui) auf, um die Markup Ressource zu binden.</span><span class="sxs-lookup"><span data-stu-id="171c3-169">The application calls [**IUIFramework::LoadUI**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-loadui) to bind the markup resource.</span></span> <span data-ttu-id="171c3-170">Der erste Parameter dieser Funktion ist ein Handle für die Menüband-Anwendungs Instanz.</span><span class="sxs-lookup"><span data-stu-id="171c3-170">The first parameter of this function is a handle to the Ribbon application instance.</span></span> <span data-ttu-id="171c3-171">Der zweite Parameter ist der Name der zuvor kompilierten binären Markup Ressource.</span><span class="sxs-lookup"><span data-stu-id="171c3-171">The second parameter is the name of the binary markup resource that was compiled previously.</span></span> <span data-ttu-id="171c3-172">Indem das binäre Markup an das Multifunktionsleisten-Framework übergeben wird, signalisiert die Anwendung, wie die Menüband-Struktur lauten soll und wie Steuerelemente angeordnet werden sollten.</span><span class="sxs-lookup"><span data-stu-id="171c3-172">By passing the binary markup to the Ribbon framework, the application signals what the Ribbon structure should be and how controls should be arranged.</span></span> <span data-ttu-id="171c3-173">Außerdem bietet das Framework ein Manifest von Befehlen, die verfügbar gemacht werden (z. b. einfügen, Ausschneiden, suchen), die vom Framework verwendet werden, wenn es Befehls bezogene Rückrufe zur Laufzeit ausführt.</span><span class="sxs-lookup"><span data-stu-id="171c3-173">It also provides the framework with a manifest of commands to expose (such as Paste, Cut, Find), which are used by the framework when it makes Command-related callbacks at run time.</span></span>

    ```
    hr = pFramework->LoadUI(GetModuleHandle(NULL), L"APPLICATION_RIBBON");
    if (FAILED(hr))
    {
      return hr;
    }
    ```

    

4.  <span data-ttu-id="171c3-174">[**Iuiapplication:: onkreateuicommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-oncreateuicommand) -Rückrufe</span><span class="sxs-lookup"><span data-stu-id="171c3-174">[**IUIApplication::OnCreateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-oncreateuicommand) callbacks</span></span>

    <span data-ttu-id="171c3-175">Nachdem die Schritte 1 bis 3 abgeschlossen sind, weiß das Menüband-Framework, welche Befehle im Menüband verfügbar gemacht werden sollen.</span><span class="sxs-lookup"><span data-stu-id="171c3-175">After steps 1 through 3 are completed, the Ribbon framework knows which Commands to expose in the Ribbon.</span></span> <span data-ttu-id="171c3-176">Das Framework benötigt jedoch noch zwei Dinge, bevor das Menüband voll funktionsfähig ist: eine Methode, um der Anwendung mitzuteilen, wann Befehle ausgeführt werden und wie Sie zur Laufzeit Befehls Ressourcen oder Eigenschaften erhalten.</span><span class="sxs-lookup"><span data-stu-id="171c3-176">However, the framework still needs two things before the Ribbon is fully functional: a way to tell the application when Commands are executed and a way to get Command resources, or properties, at run time.</span></span> <span data-ttu-id="171c3-177">Wenn z. b. ein Kombinations Feld in der Benutzeroberfläche angezeigt werden soll, muss das Framework die Elemente Abfragen, mit denen das Kombinations Feld aufgefüllt werden soll.</span><span class="sxs-lookup"><span data-stu-id="171c3-177">For example, if a combo box is to appear in the UI, then the framework needs to ask for the items with which to populate the combo box.</span></span>

    <span data-ttu-id="171c3-178">Diese beiden Funktionen werden über die [**iuicommandhandler**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler) -Schnittstelle behandelt.</span><span class="sxs-lookup"><span data-stu-id="171c3-178">These two pieces of functionality are handled through the [**IUICommandHandler**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler) interface.</span></span> <span data-ttu-id="171c3-179">Insbesondere für jeden Befehl, der im binären Markup deklariert ist (siehe Schritt 3 oben), ruft das Framework [**iuiapplication:: onforateuicommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-oncreateuicommand) auf, um die Anwendung nach einem **iuicommandhandler** -Objekt für diesen Befehl zu Fragen.</span><span class="sxs-lookup"><span data-stu-id="171c3-179">Specifically, for each command declared in the binary markup (see Step 3 above), the framework calls [**IUIApplication::OnCreateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-oncreateuicommand) to ask the application for an **IUICommandHandler** object for that command</span></span>

    > [!Note]  
    > <span data-ttu-id="171c3-180">Mit der [**iuicommandhandler**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler) -Schnittstelle kann ein Befehls Handler an einen oder mehrere Befehle gebunden werden.</span><span class="sxs-lookup"><span data-stu-id="171c3-180">The [**IUICommandHandler**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler) interface allows a Command handler to be bound to one or more Commands.</span></span>

     

<span data-ttu-id="171c3-181">Die Anwendung muss mindestens [**iuiapplication**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication) Methodenstub implementieren, die E \_ notimpl zurückgeben, wie im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="171c3-181">At a minimum, the application is required to implement [**IUIApplication**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication) methods stubs that return E\_NOTIMPL as shown in the following example.</span></span>


```
STDMETHOD(OnViewChanged)(UINT32 viewId,
                         UI_VIEWTYPE typeID,
                         IUnknown *view,
                         UI_VIEWVERB verb,
                         INT32 uReasonCode)
{ 
  return E_NOTIMPL; 
}

STDMETHOD(OnCreateUICommand)(UINT32 commandId,
                             UI_COMMANDTYPE typeID,
                             IUICommandHandler **commandHandler)
{ 
  return E_NOTIMPL; 
}

STDMETHOD(OnDestroyUICommand)(UINT32 commandId,
                              UI_COMMANDTYPE typeID,
                              IUICommandHandler *commandHandler) 
{ 
  return E_NOTIMPL; 
}
```



### <a name="link-the-markup-to-the-application"></a><span data-ttu-id="171c3-182">Das Markup mit der Anwendung verknüpfen</span><span class="sxs-lookup"><span data-stu-id="171c3-182">Link the Markup to the Application</span></span>

<span data-ttu-id="171c3-183">An diesem Punkt müssen die Markup Ressourcen Dateien mit der Host Anwendung verknüpft werden, indem ein Verweis auf die Markup Ressourcen Definitionsdatei (die einen Verweis auf die Markup Header Datei enthält) in der Anwendungs Ressourcen Datei eingeschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="171c3-183">At this point, the markup resource files must be linked to the host application by including a reference to the markup resource-definition file (which contains a reference to the markup header file) in the application resource file.</span></span> <span data-ttu-id="171c3-184">Beispielsweise ist für eine Anwendung mit dem Namen "ribbonapp" mit der Ressourcen Datei "ribbonui. RC" die folgende Zeile in der Datei "ribbonapp. RC" erforderlich.</span><span class="sxs-lookup"><span data-stu-id="171c3-184">For example, an application called RibbonApp with a resource file called ribbonUI.rc requires the following line in the RibbonApp.rc file.</span></span>


```C++
#include "ribbonUI.rc"
```



<span data-ttu-id="171c3-185">Abhängig vom verwendeten Compiler und Linker kann das Ressourcen Definitions Skript auch kompiliert werden, bevor die Multifunktionsleistenanwendung kompiliert werden kann.</span><span class="sxs-lookup"><span data-stu-id="171c3-185">Depending on the compiler and linker being used, the resource-definition script may also require compiling before the Ribbon application can be compiled.</span></span> <span data-ttu-id="171c3-186">Das Befehlszeilen Tool des [Ressourcen Compilers (RC)](../menurc/using-rc-the-rc-command-line-.md) , das im Lieferumfang von Microsoft Visual Studio und der Windows SDK enthalten ist, kann für diese Aufgabe verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="171c3-186">The [resource compiler (RC)](../menurc/using-rc-the-rc-command-line-.md) command line tool that ships with Microsoft Visual Studio and the Windows SDK can be used for this task.</span></span>

### <a name="compile-the-application"></a><span data-ttu-id="171c3-187">Kompilieren der Anwendung</span><span class="sxs-lookup"><span data-stu-id="171c3-187">Compile the Application</span></span>

<span data-ttu-id="171c3-188">Nachdem die Menüband-Anwendung kompiliert wurde, kann Sie ausgeführt und die Benutzeroberfläche getestet werden.</span><span class="sxs-lookup"><span data-stu-id="171c3-188">Once the Ribbon application is compiled, it can be run and the UI tested.</span></span> <span data-ttu-id="171c3-189">Wenn die Benutzeroberfläche optimiert werden muss und keine Änderungen an zugeordneten Befehls Handlern im Kern Anwendungscode vorgenommen werden, überarbeiten Sie die Markup Quelldatei, kompilieren Sie das Markup mit UICC.exe neu, und verknüpfen Sie die neuen Markup Ressourcen Dateien.</span><span class="sxs-lookup"><span data-stu-id="171c3-189">If the UI requires tweaking and there are no changes to any associated Command handlers in the core application code, revise the markup source file, recompile the markup with UICC.exe, and link the new markup resource files.</span></span> <span data-ttu-id="171c3-190">Wenn die Anwendung neu gestartet wird, wird die geänderte Benutzeroberfläche angezeigt.</span><span class="sxs-lookup"><span data-stu-id="171c3-190">When the application is restarted, the modified UI is displayed.</span></span>

<span data-ttu-id="171c3-191">All dies ist möglich, ohne den Kern Anwendungscode zu berühren – eine bedeutende Verbesserung im Vergleich zur standardmäßigen Anwendungsentwicklung und-Verteilung.</span><span class="sxs-lookup"><span data-stu-id="171c3-191">All this is possible without touching the core application code—a significant improvement over standard application development and distribution.</span></span>

## <a name="run-time-updates-and-executions"></a><span data-ttu-id="171c3-192">Lauf Zeit Updates und Ausführungen</span><span class="sxs-lookup"><span data-stu-id="171c3-192">Run Time Updates and Executions</span></span>

<span data-ttu-id="171c3-193">Die Lauf Zeit Kommunikationsstruktur des Menüband-Frameworks basiert auf einem Push-und Pull-oder bidirektionalen Aufrufer-Modell.</span><span class="sxs-lookup"><span data-stu-id="171c3-193">The run-time communication structure of the Ribbon framework is based on a push and pull, or two-way caller, model.</span></span>

<span data-ttu-id="171c3-194">Dieses Modell ermöglicht es dem Framework, die Anwendung zu informieren, wenn ein Befehl ausgeführt wird, und ermöglicht sowohl dem Framework als auch der Anwendung das Abfragen, aktualisieren und ungültig machen von Eigenschafts Werten und Menü Band Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="171c3-194">This model allows the framework to inform the application when a Command is executed and allows both the framework and the application to query, update, and invalidate property values and Ribbon resources.</span></span> <span data-ttu-id="171c3-195">Diese Funktionalität wird durch eine Reihe von Schnittstellen und Methoden bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="171c3-195">This functionality is provided through a number of interfaces and methods.</span></span>

<span data-ttu-id="171c3-196">Das Framework ruft aktualisierte Eigenschaften Informationen mithilfe der [**iuicommandhandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) -Rückruf Methode aus der Multifunktionsleisten-Anwendung ab.</span><span class="sxs-lookup"><span data-stu-id="171c3-196">The framework pulls updated property information from the Ribbon application through the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span> <span data-ttu-id="171c3-197">Eine Befehls-ID und ein Eigenschafts Schlüssel, der die zu Aktualisier Endes Befehls Eigenschaft identifiziert, werden an die Methode weitergegeben, die dann einen Wert für diesen Eigenschafts Schlüssel an das Framework zurückgibt oder diesen überträgt.</span><span class="sxs-lookup"><span data-stu-id="171c3-197">A Command ID and a property key, which identifies the Command property to update, are passed to the method which then returns, or pushes, a value for that property key to the framework.</span></span>

<span data-ttu-id="171c3-198">Das Framework ruft [**iuicommandhandler:: Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) auf, wenn ein Befehl ausgeführt wird, wobei sowohl die Befehls-ID als auch der aufgetretene Typ der Ausführung ([**UI \_ executionverb**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_executionverb)) identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="171c3-198">The framework calls [**IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) when a Command is executed, identifying both the Command ID and the type of execution that occurred ([**UI\_EXECUTIONVERB**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_executionverb)).</span></span> <span data-ttu-id="171c3-199">An dieser Stelle gibt die Anwendung die Ausführungs Logik für einen Befehl an.</span><span class="sxs-lookup"><span data-stu-id="171c3-199">This is where the application specifies the execution logic for a command.</span></span>

<span data-ttu-id="171c3-200">Das folgende Diagramm veranschaulicht die Lauf Zeit Kommunikation für die Befehlsausführung zwischen dem Framework und der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="171c3-200">The following diagram illustrates the run-time communication for Command execution between the framework and the application.</span></span>

![das Diagramm zeigt ein Beispiel für die Lauf Zeit Kommunikation zwischen dem Menüband-Framework und einer Host Anwendung.](images/overviews/updatesandexecutions.png)

> [!Note]  
> <span data-ttu-id="171c3-202">Das Implementieren der [**iuicommandhandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) -Funktion und der [**iuicommandhandler:: Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) -Funktion ist nicht erforderlich, um anfänglich ein Menüband in einer Anwendung anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="171c3-202">Implementing the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) and [**IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) functions is not necessary to initially display a Ribbon in an application.</span></span> <span data-ttu-id="171c3-203">Diese Methoden sind jedoch erforderlich, um sicherzustellen, dass die Anwendung ordnungsgemäß funktioniert, wenn Befehle vom Benutzer ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="171c3-203">However, these methods are necessary to ensure that the application functions correctly when commands are executed by the user.</span></span>

 

## <a name="ole-support"></a><span data-ttu-id="171c3-204">OLE-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="171c3-204">OLE Support</span></span>

<span data-ttu-id="171c3-205">Eine Menüband-Anwendung kann als OLE-Server konfiguriert werden, um die Out-of-Place-OLE-Aktivierung zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="171c3-205">A Ribbon application can be configured as an OLE server to support out-of-place OLE activation.</span></span>

<span data-ttu-id="171c3-206">Objekte, die in einer OLE-Serveranwendung erstellt wurden, behalten ihre Zuordnung mit der Serveranwendung bei, wenn Sie in eine OLE-Client Anwendung (oder in einen Container) eingefügt (oder eingefügt) werden.</span><span class="sxs-lookup"><span data-stu-id="171c3-206">Objects created in an OLE server application maintain their association with the server application when inserted (either pasted or placed) into an OLE client application (or container).</span></span> <span data-ttu-id="171c3-207">Bei der Out-of-Place-OLE-Aktivierung wird durch Doppelklicken auf das Objekt in der Client Anwendung eine dedizierte Instanz der Serveranwendung geöffnet, und das Objekt wird zur Bearbeitung geladen.</span><span class="sxs-lookup"><span data-stu-id="171c3-207">In out-of-place OLE activation, double clicking the object in the client application opens a dedicated instance of the server application and loads the object for editing.</span></span> <span data-ttu-id="171c3-208">Wenn die Serveranwendung geschlossen wird, werden alle an dem Objekt vorgenommenen Änderungen in der Client Anwendung übernommen.</span><span class="sxs-lookup"><span data-stu-id="171c3-208">When the server application is closed, all changes made to the object are reflected in the client application.</span></span>

> [!Note]  
> <span data-ttu-id="171c3-209">Das Menüband-Framework unterstützt keine direkte OLE-Aktivierung.</span><span class="sxs-lookup"><span data-stu-id="171c3-209">The Ribbon framework does not support in-place OLE activation.</span></span> <span data-ttu-id="171c3-210">Objekte, die in einem Menüband-basierten OLE-Server erstellt werden, können nicht innerhalb der OLE-Client Anwendung bearbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="171c3-210">Objects created in a Ribbon-based OLE server cannot be edited from within the OLE client application.</span></span> <span data-ttu-id="171c3-211">Eine externe dedizierte Instanz der Serveranwendung ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="171c3-211">An external dedicated instance of the server application is required.</span></span>


## <a name="related-topics"></a><span data-ttu-id="171c3-212">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="171c3-212">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="171c3-213">Deklarieren von Befehlen und Steuerelementen mit Menüband-Markup</span><span class="sxs-lookup"><span data-stu-id="171c3-213">Declaring Commands and Controls with Ribbon Markup</span></span>](./windowsribbon-schema.md)
</dt> <dt>

[<span data-ttu-id="171c3-214">Multifunktionsleisten-Benutzeroberflächen Richtlinien</span><span class="sxs-lookup"><span data-stu-id="171c3-214">Ribbon User Experience Guidelines</span></span>](https://msdn.microsoft.com/library/cc872782.aspx)
</dt> <dt>

[<span data-ttu-id="171c3-215">Menüband-Entwurfsprozess</span><span class="sxs-lookup"><span data-stu-id="171c3-215">Ribbon Design Process</span></span>](https://msdn.microsoft.com/library/cc872781.aspx)
</dt> </dl>

 

 




