---
description: In diesem Abschnitt wird beschrieben, wie Sie aus einem nativen Windows-Desktop Programm drucken.
ms.assetid: C1EDBE38-9D18-41BB-961C-12CF2283C639
title: Drucken von Desktop-Apps
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbecbac997d000f50e7c912e57be42cc8fe239b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353919"
---
# <a name="desktop-app-printing"></a><span data-ttu-id="935e2-103">Drucken von Desktop-Apps</span><span class="sxs-lookup"><span data-stu-id="935e2-103">Desktop App Printing</span></span>

<span data-ttu-id="935e2-104">In diesem Abschnitt wird beschrieben, wie Sie aus einem nativen Windows-Desktop Programm drucken.</span><span class="sxs-lookup"><span data-stu-id="935e2-104">This section describes how to print from a native Windows desktop program.</span></span>

## <a name="overview"></a><span data-ttu-id="935e2-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="935e2-105">Overview</span></span>

<span data-ttu-id="935e2-106">Um die beste Benutzer Leistung beim Drucken von einem systemeigenen Windows-Programm zu gewährleisten, muss das Programm so entworfen werden, dass es aus einem dedizierten Thread gedruckt wird.</span><span class="sxs-lookup"><span data-stu-id="935e2-106">To provide the best user experience when you print from a native Windows program, the program must be designed to print from a dedicated thread.</span></span> <span data-ttu-id="935e2-107">In einem systemeigenen Windows-Programm ist das Programm für die Verwaltung von Ereignissen und Nachrichten von Benutzeroberflächen zuständig.</span><span class="sxs-lookup"><span data-stu-id="935e2-107">In a native Windows program, the program is responsible for managing user interface events and messages.</span></span> <span data-ttu-id="935e2-108">Druckvorgänge können Zeiträume intensiver Berechnungen erfordern, da der Anwendungs Inhalt für den Drucker gerendert wird. Dies kann verhindern, dass das Programm auf Benutzerinteraktionen reagiert, wenn diese Verarbeitung im gleichen Thread ausgeführt wird wie die Ereignisverarbeitung der Benutzerinteraktion.</span><span class="sxs-lookup"><span data-stu-id="935e2-108">Printing operations can require periods of intense computation as the application content is rendered for the printer, which can prevent the program from responding to user interaction if this processing is performed in the same thread as event processing of the user interaction.</span></span>

<span data-ttu-id="935e2-109">Wenn Sie bereits wissen, wie Sie ein System eigenes Windows-Programm mit mehreren Threads schreiben, gehen Sie direkt zum [Drucken aus einer Windows-Anwendung](how-to--print-from-a-windows-application.md) , und erfahren Sie, wie Sie dem Programm Druckfunktionen hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="935e2-109">If you are already familiar with how to write a multi-threaded native Windows program, you go directly to [How to print from a Windows application](how-to--print-from-a-windows-application.md) and learn how to add printing functionality to your program.</span></span>

### <a name="basic-windows-program-requirements"></a><span data-ttu-id="935e2-110">Grundlegende Windows-Programmanforderungen</span><span class="sxs-lookup"><span data-stu-id="935e2-110">Basic Windows Program Requirements</span></span>

<span data-ttu-id="935e2-111">Um eine optimale Leistung und Programm Reaktionsfähigkeit zu erzielen, sollten Sie die Druckauftrags Verarbeitung eines Programms nicht in dem Thread ausführen, der die Benutzerinteraktion verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="935e2-111">For best performance and program responsiveness, do not perform a program's print job processing in the thread that processes user interaction.</span></span>

<span data-ttu-id="935e2-112">Diese Trennung von Druck von Benutzerinteraktion wirkt sich darauf aus, wie das Programm die Anwendungsdaten verwaltet.</span><span class="sxs-lookup"><span data-stu-id="935e2-112">This separation of printing from user interaction will influence how the program manages the application data.</span></span> <span data-ttu-id="935e2-113">Sie sollten diese Implikationen gründlich verstehen, bevor Sie mit dem Schreiben der Anwendung beginnen.</span><span class="sxs-lookup"><span data-stu-id="935e2-113">You should thoroughly understand these implications before you start writing the application.</span></span> <span data-ttu-id="935e2-114">In den folgenden Themen werden die grundlegenden Anforderungen für die Handhabung von Druck Vorgängen in einem separaten Thread eines Programms beschrieben.</span><span class="sxs-lookup"><span data-stu-id="935e2-114">The following topics describe the basic requirements of handling printing in a separate thread of a program.</span></span>

### <a name="windows-program-basics"></a><span data-ttu-id="935e2-115">Windows-Programm Grundlagen</span><span class="sxs-lookup"><span data-stu-id="935e2-115">Windows Program Basics</span></span>

<span data-ttu-id="935e2-116">Ein System eigenes Windows-Programm muss die Hauptfenster Prozedur bereitstellen, um die Fenster Meldungen zu verarbeiten, die vom Betriebssystem empfangen werden.</span><span class="sxs-lookup"><span data-stu-id="935e2-116">A native Windows program must provide the main window procedure to process the window messages that it receives from the operating system.</span></span> <span data-ttu-id="935e2-117">Jedes Fenster in einem Windows-Programm verfügt über eine entsprechende **WndProc** -Funktion, die diese Fenster Meldungen verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="935e2-117">Every window in a Windows program has a corresponding **WndProc** function that processes these window messages.</span></span> <span data-ttu-id="935e2-118">Der Thread, in dem diese Funktion ausgeführt wird, wird als Benutzeroberfläche oder UI-Thread bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="935e2-118">The thread in which this function runs is called the user interface, or UI, thread.</span></span>

<span data-ttu-id="935e2-119">**Verwenden Sie Ressourcen für Zeichen folgen.**</span><span class="sxs-lookup"><span data-stu-id="935e2-119">**Use resources for strings.**</span></span>  
<span data-ttu-id="935e2-120">Verwenden Sie Zeichen folgen Ressourcen aus der Ressourcen Datei des Programms anstelle von Zeichen folgen Konstanten für Zeichen folgen, die möglicherweise geändert werden müssen, wenn Sie eine andere Sprache unterstützen.</span><span class="sxs-lookup"><span data-stu-id="935e2-120">Use string resources from the program's resource file instead of string constants for strings that might need to be changed when you support another language.</span></span> <span data-ttu-id="935e2-121">Bevor ein Programm eine Zeichen folgen Ressource als Zeichenfolge verwenden kann, muss das Programm die Ressource aus der Ressourcen Datei abrufen und in einen lokalen Speicherpuffer kopieren.</span><span class="sxs-lookup"><span data-stu-id="935e2-121">Before a program can use a string resource as a string, the program must retrieve the resource from the resource file and copy it to a local memory buffer.</span></span> <span data-ttu-id="935e2-122">Dies erfordert einige zusätzliche Programmierung am Anfang, ermöglicht aber eine einfachere Änderung, Übersetzung und Lokalisierung des Programms in der Zukunft.</span><span class="sxs-lookup"><span data-stu-id="935e2-122">This requires some additional programming in the beginning, but allows for easier modification, translation, and localization of the program in the future.</span></span>  
<span data-ttu-id="935e2-123">**Verarbeiten von Daten in Schritten.**</span><span class="sxs-lookup"><span data-stu-id="935e2-123">**Process data in steps.**</span></span>  
<span data-ttu-id="935e2-124">Verarbeiten Sie den Druckauftrag in Schritten, die unterbrochen werden können.</span><span class="sxs-lookup"><span data-stu-id="935e2-124">Process the print job in steps that can be interrupted.</span></span> <span data-ttu-id="935e2-125">Dieser Entwurf ermöglicht dem Benutzer, einen langen Verarbeitungsvorgang abzubrechen, bevor er abgeschlossen wird, und verhindert, dass das Programm andere Programme blockiert, die möglicherweise gleichzeitig ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="935e2-125">This design makes it possible for the user to cancel a long processing operation before it completes and prevents the program from blocking other programs that might be running at the same time.</span></span>  
<span data-ttu-id="935e2-126">**Verwenden von Windows-Benutzerdaten.**</span><span class="sxs-lookup"><span data-stu-id="935e2-126">**Use window user data.**</span></span>  
<span data-ttu-id="935e2-127">Das Drucken von Anwendungen hat häufig mehrere Fenster und Threads.</span><span class="sxs-lookup"><span data-stu-id="935e2-127">Printing applications often have several windows and threads.</span></span> <span data-ttu-id="935e2-128">Um die Daten zwischen Threads und Verarbeitungsschritten verfügbar zu halten, ohne statische, globale Variablen zu verwenden, verweisen Sie auf die Datenstrukturen durch einen Datenzeiger, der Teil des Fensters ist, in dem Sie verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="935e2-128">To keep the data available between threads and processing steps without using static, global variables, reference the data structures by a data pointer that is part of the window in which they are used.</span></span>  


<span data-ttu-id="935e2-129">Das folgende Codebeispiel zeigt einen Haupteinstiegspunkt für eine Druckanwendung.</span><span class="sxs-lookup"><span data-stu-id="935e2-129">The following code example shows a main entry point for a printing application.</span></span> <span data-ttu-id="935e2-130">In diesem Beispiel wird gezeigt, wie Zeichen folgen Ressourcen anstelle von Zeichen folgen Konstanten verwendet werden und wie die Hauptnachrichten Schleife zum Verarbeiten der Fenster Meldungen des Programms angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="935e2-130">This example shows how to use string resources instead of string constants and also shows the main message loop that processes the program's window messages.</span></span>


```C++
int APIENTRY 
wWinMain(
        HINSTANCE hInstance, 
        HINSTANCE hPrevInstance, 
        LPWSTR lpCmdLine, 
        int nCmdShow
)
{
    UNREFERENCED_PARAMETER(hPrevInstance);
    UNREFERENCED_PARAMETER(lpCmdLine);

    MSG msg;
    HACCEL hAccelTable;
    HRESULT hr = S_OK;

    // Register the main window class name
    WCHAR szWindowClass[MAXIMUM_RESOURCE_STRING_LENGTH];            
    LoadString(
        hInstance, 
        IDC_PRINTSAMPLE, 
        szWindowClass, 
        MAXIMUM_RESOURCE_STRING_LENGTH);
    MyRegisterClass(hInstance, szWindowClass);

    // Perform application initialization:
    if (!InitInstance (hInstance, nCmdShow))
    {
        // Unable to initialize this instance of the application
        //  so display error message and exit
        MessageBoxWithResourceString (
            hInstance, 
            GetDesktopWindow(), 
            IDS_ERROR_INSTINITFAIL, 
            IDS_CAPTION_ERROR, 
            (MB_OK | MB_ICONEXCLAMATION));
        return FALSE;
    }    
    
    // Init COM for printing interfaces
    if (FAILED(hr = CoInitializeEx(0, COINIT_MULTITHREADED)))
    {
        // Unable to initialize COM
        //  so display error message and exit
        MessageBoxWithResourceString (
            hInstance, 
            GetDesktopWindow(), 
            IDS_ERROR_COMINITFAIL, 
            IDS_CAPTION_ERROR, 
            (MB_OK | MB_ICONEXCLAMATION));
        return FALSE;
    }

    hAccelTable = LoadAccelerators(
                    hInstance, 
                    MAKEINTRESOURCE(IDC_PRINTSAMPLE));

    // Main message handling loop
    while (GetMessage(&msg, NULL, 0, 0))
    {
        if (!TranslateAccelerator(msg.hwnd, hAccelTable, &msg))
        {
            TranslateMessage(&msg);
            DispatchMessage(&msg);
        }
    }

    // Uninitialize (close) the COM interface
    CoUninitialize();

    return (int) msg.wParam;
}
```



### <a name="document-information"></a><span data-ttu-id="935e2-131">Dokument Informationen</span><span class="sxs-lookup"><span data-stu-id="935e2-131">Document Information</span></span>

<span data-ttu-id="935e2-132">Systemeigene Windows-Programme, die drucken, sollten für die Verarbeitung mit mehreren Threads entwickelt werden.</span><span class="sxs-lookup"><span data-stu-id="935e2-132">Native Windows programs that print should be designed for multi-threaded processing.</span></span> <span data-ttu-id="935e2-133">Eine der Anforderungen eines Multithreaddesigns besteht darin, die Datenelemente des Programms so zu schützen, dass Sie sicher sind, dass mehrere Threads gleichzeitig verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="935e2-133">One of the requirements of a multi-threaded design is to protect the program's data elements so that they are safe for multiple threads to use at the same time.</span></span> <span data-ttu-id="935e2-134">Sie können Datenelemente mithilfe von Synchronisierungs Objekten schützen und die Daten so organisieren, dass Konflikte zwischen den Threads vermieden werden.</span><span class="sxs-lookup"><span data-stu-id="935e2-134">You can protect data elements by using synchronization objects and organizing the data to avoid conflicts between the threads.</span></span> <span data-ttu-id="935e2-135">Gleichzeitig muss das Programmänderungen an den Programm Daten beim Drucken verhindern.</span><span class="sxs-lookup"><span data-stu-id="935e2-135">At the same time, the program must prevent changes to the program data while it is being printed.</span></span> <span data-ttu-id="935e2-136">Das Beispielprogramm verwendet mehrere verschiedene multithreadprogrammierungstechniken.</span><span class="sxs-lookup"><span data-stu-id="935e2-136">The sample program uses several different multi-threaded programming techniques.</span></span>

 <span data-ttu-id="935e2-137">**Synchronisierungs Ereignisse**</span><span class="sxs-lookup"><span data-stu-id="935e2-137">**Synchronization Events**</span></span>  
<span data-ttu-id="935e2-138">Das Beispielprogramm verwendet Ereignisse, Thread Handles und Wait-Funktionen, um die Verarbeitung zwischen dem Druck Thread und dem Hauptprogramm zu synchronisieren und anzugeben, dass die Daten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="935e2-138">The sample program uses events, thread handles, and wait functions to synchronize the processing between the print thread and the main program and to indicate that the data is in use.</span></span>  
<span data-ttu-id="935e2-139">**Anwendungsspezifische Windows-Meldungen**</span><span class="sxs-lookup"><span data-stu-id="935e2-139">**Application-Specific Windows Messages**</span></span>  
<span data-ttu-id="935e2-140">Das Beispielprogramm verwendet anwendungsspezifische Fenster Meldungen, um das Programm mit anderen systemeigenen Windows-Programmen kompatibler zu gestalten.</span><span class="sxs-lookup"><span data-stu-id="935e2-140">The sample program uses application-specific window messages to make the program more compatible with other native Windows programs.</span></span> <span data-ttu-id="935e2-141">Wenn Sie die Verarbeitung in kleinere Schritte aufteilen und diese Schritte in der Fenster Nachrichten Schleife in eine Warteschlange stellen, erleichtert Windows die Verwaltung der Verarbeitung, ohne dass andere Anwendungen blockiert werden müssen, die möglicherweise auch auf dem Computer ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="935e2-141">Breaking the processing into smaller steps and queuing those steps in the window message loop makes it easier for Windows to manage the processing without blocking other applications that might also be running on the computer.</span></span>  
<span data-ttu-id="935e2-142">**Datenstrukturen**</span><span class="sxs-lookup"><span data-stu-id="935e2-142">**Data Structures**</span></span>  
<span data-ttu-id="935e2-143">Das Beispielprogramm wird nicht in einem objektorientierten Stil mithilfe von-Objekten und-Klassen geschrieben, obwohl Datenelemente in Datenstrukturen gruppiert werden.</span><span class="sxs-lookup"><span data-stu-id="935e2-143">The sample program is not written in an object-oriented style using objects and classes, although it does group data elements into data structures.</span></span> <span data-ttu-id="935e2-144">Das Beispiel verwendet keinen objektorientierten Ansatz, um zu verhindern, dass ein Ansatz besser oder schlechter als ein anderer Ansatz ist.</span><span class="sxs-lookup"><span data-stu-id="935e2-144">The sample does not use an object-oriented approach to avoid implying that one approach is better or worse than another.</span></span>  
<span data-ttu-id="935e2-145">Sie können die Funktionen und Datenstrukturen des Beispiel Programms als Ausgangspunkt verwenden, wenn Sie das Programm entwerfen.</span><span class="sxs-lookup"><span data-stu-id="935e2-145">You can use the functions and data structures of the sample program as a starting point when you design your program.</span></span> <span data-ttu-id="935e2-146">Unabhängig davon, ob Sie ein objektorientiertes Programm entwerfen oder nicht, ist es wichtig, sich daran zu erinnern, die zugehörigen Datenelemente zu gruppieren, damit Sie Sie bei Bedarf sicher in verschiedenen Threads verwenden können.</span><span class="sxs-lookup"><span data-stu-id="935e2-146">Whether you decide to design an object-oriented program or not, the important design consideration to remember is to group the related data elements so that you can use them safely in different threads as necessary.</span></span>  


### <a name="printer-device-context"></a><span data-ttu-id="935e2-147">Drucker Gerätekontext</span><span class="sxs-lookup"><span data-stu-id="935e2-147">Printer Device Context</span></span>

<span data-ttu-id="935e2-148">Beim drucken möchten Sie möglicherweise den zu druckenden Inhalt in einem Gerätekontext darstellen.</span><span class="sxs-lookup"><span data-stu-id="935e2-148">When printing, you might want to render the content to be printed to a device context.</span></span> <span data-ttu-id="935e2-149">Gewusst [wie: Abrufen eines Drucker Geräte Kontexts](retrieving-a-printer-device-context.md) beschreibt die verschiedenen Methoden, mit denen Sie einen Drucker Gerätekontext abrufen können.</span><span class="sxs-lookup"><span data-stu-id="935e2-149">[How To: Retrieve a Printer Device Context](retrieving-a-printer-device-context.md) describes the different ways that you can obtain a printer device context.</span></span>

## <a name="related-topics"></a><span data-ttu-id="935e2-150">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="935e2-150">Related topics</span></span>



[<span data-ttu-id="935e2-151">Drucken aus einer Windows-Anwendung</span><span class="sxs-lookup"><span data-stu-id="935e2-151">How to print from a Windows application</span></span>](how-to--print-from-a-windows-application.md)


 

 



