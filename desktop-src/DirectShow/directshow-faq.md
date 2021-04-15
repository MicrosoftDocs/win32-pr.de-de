---
description: FAQ zu DirectShow
ms.assetid: 198758b9-025a-44af-958c-9ddea8cbb12d
title: FAQ zu DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a7d0959c4abb24509edd9c26d111e80a5af221d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521795"
---
# <a name="directshow-faq"></a><span data-ttu-id="7fc47-103">FAQ zu DirectShow</span><span class="sxs-lookup"><span data-stu-id="7fc47-103">DirectShow FAQ</span></span>

<span data-ttu-id="7fc47-104">In diesem Artikel werden viele häufig gestellte Fragen zu Microsoft DirectShow beantwortet.</span><span class="sxs-lookup"><span data-stu-id="7fc47-104">This article answers many frequently asked questions about Microsoft DirectShow.</span></span>

<span data-ttu-id="7fc47-105">**Welche Betriebssysteme werden von DirectShow unterstützt?**</span><span class="sxs-lookup"><span data-stu-id="7fc47-105">**What operating systems does DirectShow support?**</span></span>

<span data-ttu-id="7fc47-106">DirectShow ist in allen unterstützten Versionen von Windows verfügbar.</span><span class="sxs-lookup"><span data-stu-id="7fc47-106">DirectShow is available in all supported versions of Windows.</span></span>

<span data-ttu-id="7fc47-107">**Wie viel com-wissen muss ich mit DirectShow programmieren?**</span><span class="sxs-lookup"><span data-stu-id="7fc47-107">**How much COM knowledge do I need to program with DirectShow?**</span></span>

<span data-ttu-id="7fc47-108">Für die Anwendungsentwicklung müssen Sie die Grundlagen der Arbeit mit COM-Objekten verstehen: wie instanziieren Sie, greifen Sie auf die von Ihnen verfügbar gemachten Schnittstellen zu, und verwalten Sie Verweis Zähler für diese Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="7fc47-108">For application development, you need to understand the basics of working with COM objects: how to instantiate them, access the interfaces they expose, and manage reference counts on those interfaces.</span></span> <span data-ttu-id="7fc47-109">Die Filter Entwicklung erfordert mehr com-wissen.</span><span class="sxs-lookup"><span data-stu-id="7fc47-109">Filter development requires more COM knowledge.</span></span>

<span data-ttu-id="7fc47-110">**Welche Formate werden von DirectShow unterstützt?**</span><span class="sxs-lookup"><span data-stu-id="7fc47-110">**What formats does DirectShow support?**</span></span>

<span data-ttu-id="7fc47-111">Siehe [Unterstützte Formate in DirectShow](supported-formats-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="7fc47-111">See [Supported Formats in DirectShow](supported-formats-in-directshow.md).</span></span>

<span data-ttu-id="7fc47-112">**Gibt es eine DirectShow-Hardware Kompatibilitätsliste (HCL)?**</span><span class="sxs-lookup"><span data-stu-id="7fc47-112">**Is there a DirectShow Hardware Compatibility List (HCL)?**</span></span>

<span data-ttu-id="7fc47-113">Nein.</span><span class="sxs-lookup"><span data-stu-id="7fc47-113">No.</span></span> <span data-ttu-id="7fc47-114">In DirectShow werden die Hardwarefunktionen von Microsoft DirectDraw und Microsoft DirectSound verwendet, sofern diese verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="7fc47-114">DirectShow uses Microsoft DirectDraw and Microsoft DirectSound hardware capabilities if they are available.</span></span> <span data-ttu-id="7fc47-115">Wenn keine spezielle Hardware verfügbar ist, verwendet DirectShow GDI zum Zeichnen von Video-und **waveout** \* -Multimedia-APIs zur Wiedergabe von Audiodaten.</span><span class="sxs-lookup"><span data-stu-id="7fc47-115">When no special hardware is available, DirectShow uses GDI to draw video and the **waveOut** \* multimedia APIs to play audio.</span></span>

<span data-ttu-id="7fc47-116">**Welche Sprachen kann ich verwenden, um eine DirectShow-Anwendung zu schreiben?**</span><span class="sxs-lookup"><span data-stu-id="7fc47-116">**What languages can I use to write a DirectShow application?**</span></span>

<span data-ttu-id="7fc47-117">DirectShow ist hauptsächlich für die C++-Entwicklung konzipiert.</span><span class="sxs-lookup"><span data-stu-id="7fc47-117">DirectShow is designed primarily for C++ development.</span></span> <span data-ttu-id="7fc47-118">Eine kleine Teilmenge der DirectShow-API wird durch Visual Basic 6,0 verfügbar gemacht; Diese Funktion ist jedoch veraltet.</span><span class="sxs-lookup"><span data-stu-id="7fc47-118">A small sub-set of the DirectShow API is exposed through Visual Basic 6.0; however, this feature is deprecated.</span></span>

<span data-ttu-id="7fc47-119">**Ist DirectShow immer über verwalteten Code zugänglich?**</span><span class="sxs-lookup"><span data-stu-id="7fc47-119">**Will DirectShow ever be accessible through managed code?**</span></span>

<span data-ttu-id="7fc47-120">Microsoft hat keine aktuellen Pläne, eine verwaltete DirectShow-API zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="7fc47-120">Microsoft has no current plans to implement a managed DirectShow API.</span></span>

<span data-ttu-id="7fc47-121">**Welchen Compiler benötige ich für die DirectShow-Entwicklung?**</span><span class="sxs-lookup"><span data-stu-id="7fc47-121">**What compiler do I need for DirectShow development?**</span></span>

<span data-ttu-id="7fc47-122">Alle Compiler, die Component Object Model (com)-Objekte erstellen können, sollten funktionieren, wenn die Umgebung des Compilers ordnungsgemäß konfiguriert wurde.</span><span class="sxs-lookup"><span data-stu-id="7fc47-122">Any compiler capable of generating Component Object Model (COM) objects should work once the compiler's environment has been configured correctly.</span></span>

<span data-ttu-id="7fc47-123">**Wie verhält sich DirectShow mit Microsoft DirectX?**</span><span class="sxs-lookup"><span data-stu-id="7fc47-123">**How does DirectShow relate to Microsoft DirectX?**</span></span>

<span data-ttu-id="7fc47-124">Intern verwendet DirectShow DirectSound und DirectDraw, wenn dies von der Hardware unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="7fc47-124">Internally, DirectShow uses DirectSound and DirectDraw when the hardware supports it.</span></span> <span data-ttu-id="7fc47-125">Der Videorenderer und die Überlagerungs Filter Filter verwenden DirectDraw 3 und DirectDraw 5-Oberflächen.</span><span class="sxs-lookup"><span data-stu-id="7fc47-125">The Video Renderer and Overlay Mixer filters use DirectDraw 3 and DirectDraw 5 surfaces.</span></span> <span data-ttu-id="7fc47-126">Der Video Mischungs-Renderer 7 (nur Windows XP) verwendet DirectDraw 7-Oberflächen.</span><span class="sxs-lookup"><span data-stu-id="7fc47-126">The Video Mixing Renderer 7 (Windows XP only) uses DirectDraw 7 surfaces.</span></span> <span data-ttu-id="7fc47-127">Der Video Mischungs-Renderer 9 und der erweiterte Videorenderer verwenden die neuesten Microsoft Direct3D-APIs.</span><span class="sxs-lookup"><span data-stu-id="7fc47-127">The Video Mixing Renderer 9 and the Enhanced Video Renderer use the latest Microsoft Direct3D APIs.</span></span> <span data-ttu-id="7fc47-128">Sie müssen nicht die anderen DirectX-APIs verwenden, um eine DirectShow-Anwendung zu schreiben, obwohl es möglich ist, diese zu kombinieren.</span><span class="sxs-lookup"><span data-stu-id="7fc47-128">You do not need to use the other DirectX APIs to write a DirectShow application, although it is possible to combine them.</span></span>

<span data-ttu-id="7fc47-129">**Wie verhält sich DirectShow mit Microsoft ActiveMovie?**</span><span class="sxs-lookup"><span data-stu-id="7fc47-129">**How does DirectShow relate to Microsoft ActiveMovie?**</span></span>

<span data-ttu-id="7fc47-130">ActiveMovie war der ursprüngliche Name für DirectShow.</span><span class="sxs-lookup"><span data-stu-id="7fc47-130">ActiveMovie was the original name for DirectShow.</span></span> <span data-ttu-id="7fc47-131">Der Begriff "ActiveMovie" wird nicht mehr verwendet.</span><span class="sxs-lookup"><span data-stu-id="7fc47-131">The term ActiveMovie is no longer used.</span></span>

<span data-ttu-id="7fc47-132">**Ist der Quellcode für das Hilfsprogramm "GraphEdit" verfügbar? Kann GraphEdit neu verteilt werden?**</span><span class="sxs-lookup"><span data-stu-id="7fc47-132">**Is the source code to the GraphEdit utility available? Can GraphEdit be redistributed?**</span></span>

<span data-ttu-id="7fc47-133">Nein, die Quelle ist nicht verfügbar, und Graphedt.exe ist nicht Verteil Bar.</span><span class="sxs-lookup"><span data-stu-id="7fc47-133">No, the source is not available, and Graphedt.exe is not redistributable.</span></span>

<span data-ttu-id="7fc47-134">**Ersetzen DMOS DirectShow-Filter?**</span><span class="sxs-lookup"><span data-stu-id="7fc47-134">**Do DMOs replace DirectShow filters?**</span></span>

<span data-ttu-id="7fc47-135">Microsoft DirectX Media Objects (DMOs) kann in einer DirectShow-Anwendung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7fc47-135">Microsoft DirectX Media Objects (DMOs) can be used in a DirectShow application.</span></span> <span data-ttu-id="7fc47-136">Bei Encodern, Decodern und Effekten wird empfohlen, einen DMO anstelle eines DirectShow-Filters zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="7fc47-136">For encoders, decoders, and effects, you are encouraged to write a DMO instead of a DirectShow filter.</span></span> <span data-ttu-id="7fc47-137">(Hinweis: Wenn Sie die DirectX-Video Beschleunigung in Ihrem Decoder verwenden möchten, müssen Sie Sie als Filter implementieren.) Für andere Zwecke kann ein DirectShow-Filter besser geeignet sein.</span><span class="sxs-lookup"><span data-stu-id="7fc47-137">(Note: If you want to use DirectX Video Acceleration in your decoder, you must implement it as a filter.) For other purposes, a DirectShow filter might be more appropriate.</span></span> <span data-ttu-id="7fc47-138">Weitere Informationen zu DMOS finden Sie unter [DirectX-Medienobjekte](directx-media-objects.md).</span><span class="sxs-lookup"><span data-stu-id="7fc47-138">For more information about DMOs, see [DirectX Media Objects](directx-media-objects.md).</span></span>

<span data-ttu-id="7fc47-139">**Ich Spiele eine AVI-Format Datei mit Windows Media Player. Ich kann das Audiovideo hören, aber es scheint kein Video zu sein, sondern ich sehe nur schwarz. Was ist los?**</span><span class="sxs-lookup"><span data-stu-id="7fc47-139">**I'm playing an AVI format file with Windows Media Player. I can hear the audio, but there doesn't seem to be any video-instead, I just see black. What's wrong?**</span></span>

<span data-ttu-id="7fc47-140">Wahrscheinlich wurde die Datei mit einem Codec codiert, der nicht auf Ihrem System vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="7fc47-140">Probably the file was encoded with a codec that is not present on your system.</span></span> <span data-ttu-id="7fc47-141">Obwohl das AVI-Dateiformat Common ist, können AVI-Dateien mit vielen verschiedenen Komprimierungs Formaten (Codecs) erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="7fc47-141">Although the AVI file format is common, AVI files can be created with many different compression formats (codecs).</span></span> <span data-ttu-id="7fc47-142">Wenn Sie versuchen, eine AVI-Datei wiederzugeben, die einen nicht unterstützten Codec verwendet, werden Sie möglicherweise die Audiokomponente hören, aber das Video wird als schwarzer Bildschirm angezeigt, oder die Bildschirminhalte bleiben unverändert.</span><span class="sxs-lookup"><span data-stu-id="7fc47-142">If you try to play an AVI file that uses an unsupported codec, you might hear the audio component, but the video will display as a black screen or the screen contents will remain unchanged.</span></span>

> [!Note]  
> <span data-ttu-id="7fc47-143">Windows Media Player versucht häufig, einen Codec herunterzuladen und zu installieren, wenn er nicht auf Ihrem System vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="7fc47-143">Windows Media Player often attempts to download and install a codec if it is not present on your system.</span></span>

 

<span data-ttu-id="7fc47-144">**Gewusst wie meine Anwendung erstellen? Welche Bibliotheken und Header Dateien benötige ich?**</span><span class="sxs-lookup"><span data-stu-id="7fc47-144">**How do I build my application? What libraries and header files do I need?**</span></span>

<span data-ttu-id="7fc47-145">Weitere Informationen finden [Sie unter Einrichten der Buildumgebung](setting-up-the-build-environment.md).</span><span class="sxs-lookup"><span data-stu-id="7fc47-145">See [Setting Up the Build Environment](setting-up-the-build-environment.md).</span></span>

<span data-ttu-id="7fc47-146">**GraphEdit zeigt viele Filter an, die nicht dokumentiert sind. Was sind diese Filter?**</span><span class="sxs-lookup"><span data-stu-id="7fc47-146">**GraphEdit displays a lot of filters that aren't documented. What are these filters?**</span></span>

<span data-ttu-id="7fc47-147">GraphEdit listet alle Filter auf, die auf Ihrem System in einer Filterkategorie registriert sind.</span><span class="sxs-lookup"><span data-stu-id="7fc47-147">GraphEdit enumerates all of the filters that are registered on your system in a filter category.</span></span> <span data-ttu-id="7fc47-148">Dies kann Filter enthalten, die von Drittanbieter Anwendungen installiert oder von anderen Microsoft-Technologien, wie z. b. Windows Media oder NetMeeting, installiert werden.</span><span class="sxs-lookup"><span data-stu-id="7fc47-148">This might include filters installed by third-party applications, or installed by other Microsoft technologies, such as Windows Media or NetMeeting.</span></span> <span data-ttu-id="7fc47-149">Außerdem fungieren einige DirectShow-Filter als Wrapper für Codecs oder Hardware Geräte, wobei jeder Codec oder jedes Gerät als eindeutiger Filter angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="7fc47-149">Also, some DirectShow filters act as wrappers for codecs or hardware devices, with each codec or device appearing as a distinct filter.</span></span> <span data-ttu-id="7fc47-150">Der Video-Codec von Microsoft H. 263 wird von NetMeeting verwendet und wird in DirectShow nicht mehr unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7fc47-150">The Microsoft H.263 Video Codec is used by NetMeeting and is no longer supported in DirectShow.</span></span> <span data-ttu-id="7fc47-151">Weitere Informationen finden Sie unter Auflisten von [Geräten und Filtern](enumerating-devices-and-filters.md).</span><span class="sxs-lookup"><span data-stu-id="7fc47-151">For more information, see [Enumerating Devices and Filters](enumerating-devices-and-filters.md).</span></span>

<span data-ttu-id="7fc47-152">**Ich habe Probleme, das benutzerdefinierte Diagramm Programm gesteuert zu entwickeln.**</span><span class="sxs-lookup"><span data-stu-id="7fc47-152">**I'm having trouble building my custom graph programmatically.**</span></span>

<span data-ttu-id="7fc47-153">Versuchen Sie zunächst, das Filter Diagramm mit GraphEdit zu entwickeln.</span><span class="sxs-lookup"><span data-stu-id="7fc47-153">First try building the filter graph with GraphEdit.</span></span> <span data-ttu-id="7fc47-154">Mit diesem Tool können Sie schnell viele Möglichkeiten simulieren.</span><span class="sxs-lookup"><span data-stu-id="7fc47-154">This tool enables you to simulate lots of possibilities quickly.</span></span> <span data-ttu-id="7fc47-155">GraphEdit ist immer ein guter Ausgangspunkt, um das Diagramm zu testen, bevor versucht wird, es mit Quellcode zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="7fc47-155">GraphEdit is always a great place to test out the graph before attempting to build it with source code.</span></span>

<span data-ttu-id="7fc47-156">Weitere Informationen zur Diagramm Bildung finden Sie in den folgenden Artikeln:</span><span class="sxs-lookup"><span data-stu-id="7fc47-156">For more information about graph building, see the following articles:</span></span>

-   [<span data-ttu-id="7fc47-157">Aufbauen des Filter Diagramms</span><span class="sxs-lookup"><span data-stu-id="7fc47-157">Building the Filter Graph</span></span>](building-the-filter-graph.md)
-   [<span data-ttu-id="7fc47-158">Auflisten von Objekten in einem Filter Diagramm</span><span class="sxs-lookup"><span data-stu-id="7fc47-158">Enumerating Objects in a Filter Graph</span></span>](enumerating-objects-in-a-filter-graph.md)

<span data-ttu-id="7fc47-159">**Wie kann ich erkennen, ob DirectShow auf einem bestimmten Computer installiert ist?**</span><span class="sxs-lookup"><span data-stu-id="7fc47-159">**How can I detect whether DirectShow is installed on a given machine?**</span></span>

<span data-ttu-id="7fc47-160">Rufen Sie **cokreateinstance** auf, um eine Instanz des Filter Graph-Managers zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="7fc47-160">Call **CoCreateInstance** to create an instance of the Filter Graph Manager.</span></span> <span data-ttu-id="7fc47-161">Wenn dieser Vorgang erfolgreich ist, wird DirectShow auf dem Computer installiert.</span><span class="sxs-lookup"><span data-stu-id="7fc47-161">If this call succeeds, DirectShow is installed on the machine.</span></span> <span data-ttu-id="7fc47-162">Dies wird im folgenden Code veranschaulicht:</span><span class="sxs-lookup"><span data-stu-id="7fc47-162">The following code shows how to do this:</span></span>


```C++
IGraphBuilder *pGraph;

HRESULT hr = CoCreateInstance(CLSID_FilterGraph,
    NULL, CLSCTX_INPROC_SERVER,
    IID_IGraphBuilder, (void **) &pGraph);
```



<span data-ttu-id="7fc47-163">**Gewusst wie die Einstellungen eines Filters ändern, ohne die Eigenschaften Seite anzuzeigen?**</span><span class="sxs-lookup"><span data-stu-id="7fc47-163">**How do I change a filter's settings without displaying the property page?**</span></span>

<span data-ttu-id="7fc47-164">Die meisten Filter machen eine oder mehrere Schnittstellen für das Festlegen von Eigenschaften für den Filter verfügbar.</span><span class="sxs-lookup"><span data-stu-id="7fc47-164">Most filters expose one or more interfaces for setting properties on the filter.</span></span> <span data-ttu-id="7fc47-165">Weitere Informationen finden Sie auf der Referenzseite für den fraglichen Filter.</span><span class="sxs-lookup"><span data-stu-id="7fc47-165">Consult the reference page for the filter in question.</span></span> <span data-ttu-id="7fc47-166">(Siehe [DirectShow-Filter](directshow-filters.md).)</span><span class="sxs-lookup"><span data-stu-id="7fc47-166">(See [DirectShow Filters](directshow-filters.md).)</span></span>

<span data-ttu-id="7fc47-167">**Kann ich meinen Filter mit GraphEdit testen?**</span><span class="sxs-lookup"><span data-stu-id="7fc47-167">**Can I test my filter with GraphEdit?**</span></span>

<span data-ttu-id="7fc47-168">Wenn Sie einen Filter entwickeln, kann GraphEdit Ihnen helfen, die Verbindungen zwischen den Filtern visuell darzustellen.</span><span class="sxs-lookup"><span data-stu-id="7fc47-168">While you are developing a filter, GraphEdit can help you to visualize the connections between filters.</span></span> <span data-ttu-id="7fc47-169">Sie kann auch einen schnellen Test der Funktionalität eines Filters bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="7fc47-169">It can also provide a quick test of a filter's functionality.</span></span> <span data-ttu-id="7fc47-170">Es ist jedoch nicht als stabile Testplattform gemeint.</span><span class="sxs-lookup"><span data-stu-id="7fc47-170">However, it is not meant as a robust test platform.</span></span>

<span data-ttu-id="7fc47-171">**An welchem Berechtigungs Ring werden Filter ausgeführt?**</span><span class="sxs-lookup"><span data-stu-id="7fc47-171">**At what privilege ring do filters run?**</span></span>

<span data-ttu-id="7fc47-172">Filter werden in Ring 3 ausgeführt, obwohl einige Filter Streaminggeräte steuern, die mit Ring 0 ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="7fc47-172">Filters run at ring 3, although some filters control streaming devices that run at ring 0.</span></span> <span data-ttu-id="7fc47-173">Weitere Informationen finden Sie unter [wie Hardware Geräte am Filter Diagramm teilnehmen](how-hardware-devices-participate-in-the-filter-graph.md).</span><span class="sxs-lookup"><span data-stu-id="7fc47-173">For more information, see [How Hardware Devices Participate in the Filter Graph](how-hardware-devices-participate-in-the-filter-graph.md).</span></span>

<span data-ttu-id="7fc47-174">**Muss ich einen Kernel Debugger verwenden?**</span><span class="sxs-lookup"><span data-stu-id="7fc47-174">**Do I need to use a kernel debugger?**</span></span>

<span data-ttu-id="7fc47-175">Das hängt von ihrem jeweiligen Projekt ab.</span><span class="sxs-lookup"><span data-stu-id="7fc47-175">That depends on your specific project.</span></span> <span data-ttu-id="7fc47-176">Die Installation der DirectX-Debug-Laufzeitbibliotheken bedeutet, dass Sie debugtreiber und andere Kernelmoduskomponenten installieren. Wenn Ihre Anwendung in einer dieser Komponenten eine debuggingbestätigung auslöst, wird der Computer automatisch neu gestartet, es sei denn, Sie haben einen Kernel Debugger an den Prozess angefügt.</span><span class="sxs-lookup"><span data-stu-id="7fc47-176">Installing the DirectX debug runtime libraries means that you are installing debug drivers and other kernel mode components, and that if your application causes a debug assert in one of these components, your machine will automatically reboot unless you have a kernel debugger attached to your process.</span></span>

<span data-ttu-id="7fc47-177">**Beim Ausführen der Anwendung im Debugger stürzt Sie ab.**</span><span class="sxs-lookup"><span data-stu-id="7fc47-177">**When I run my application in the debugger, it crashes.**</span></span>

<span data-ttu-id="7fc47-178">Einige Decoder sind so konzipiert, dass Sie nicht funktionieren, während die Anwendung an den Debugger angefügt wird.</span><span class="sxs-lookup"><span data-stu-id="7fc47-178">Some decoders are designed not to work while the application is attached to the debugger.</span></span> <span data-ttu-id="7fc47-179">Versuchen Sie, die Anwendung außerhalb des Debuggers auszuführen.</span><span class="sxs-lookup"><span data-stu-id="7fc47-179">Try running the application outside the debugger.</span></span>

<span data-ttu-id="7fc47-180">**Wie \_ funktioniert das GUID-Makro definieren?**</span><span class="sxs-lookup"><span data-stu-id="7fc47-180">**How does the DEFINE\_GUID macro work?**</span></span>

<span data-ttu-id="7fc47-181">Das **\_ GUID** -Makro definieren löst das Problem `extern` , dass Verweise auf GUID-Werte im Quellcode deklariert werden.</span><span class="sxs-lookup"><span data-stu-id="7fc47-181">The **DEFINE\_GUID** macro solves the problem of declaring `extern` references to GUID values in your source code.</span></span> <span data-ttu-id="7fc47-182">Nehmen Sie beispielsweise an, dass das Projekt über drei Quelldateien verfügt: Quelle1. cpp, Quelle2. cpp und Src3. cpp, und alle drei Dateien verwenden einen bestimmten GUID-Wert, den Sie definiert haben.</span><span class="sxs-lookup"><span data-stu-id="7fc47-182">For example, suppose that your project has three source files, Src1.cpp, Src2.cpp, and Src3.cpp, and all three files use a certain GUID value that you have defined.</span></span> <span data-ttu-id="7fc47-183">Der GUID-Wert muss im Projekt genau einmal definiert werden, und die anderen Quelldateien müssen `extern` Verweise darauf deklarieren.</span><span class="sxs-lookup"><span data-stu-id="7fc47-183">The GUID value must be defined exactly once in your project, and the other source files must declare `extern` references to it.</span></span> <span data-ttu-id="7fc47-184">Mit dem **\_ GUID** -Makro definieren können Sie für beide Zwecke dieselbe Header Datei verwenden.</span><span class="sxs-lookup"><span data-stu-id="7fc47-184">With the **DEFINE\_GUID** macro, you can use the same header file for both purposes.</span></span> <span data-ttu-id="7fc47-185">Deklarieren Sie die GUID in der Header Datei wie folgt:</span><span class="sxs-lookup"><span data-stu-id="7fc47-185">In your header file, declare the GUID as follows:</span></span>


```C++
DEFINE_GUID(CLSID_MyObject, 
0x00000000, 0x0000, 0x0000, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00);
```



<span data-ttu-id="7fc47-186">(Wenn dieses Beispiel Nullen enthält, platzieren Sie die eigentlichen GUID-Werte.) Mit dem Guidgen.exe-Hilfsprogramm können Sie eine neue GUID erstellen und Sie in die Header Datei im **definierenden \_ GUID** -Format einfügen.</span><span class="sxs-lookup"><span data-stu-id="7fc47-186">(Where this example has zeroes, put the actual GUID values.) You can use the Guidgen.exe utility to create a new GUID and paste it into the header file in the **DEFINE\_GUID** format.</span></span> <span data-ttu-id="7fc47-187">Schließen Sie diese Header Datei in jede Quelldatei ein, die auf die GUID verweist.</span><span class="sxs-lookup"><span data-stu-id="7fc47-187">Include this header file in every source file that references the GUID.</span></span> <span data-ttu-id="7fc47-188">Fügen Sie in genau einer der Quelldateien die Header Datei Initguid. h vor der Header Datei ein.</span><span class="sxs-lookup"><span data-stu-id="7fc47-188">In exactly one of the source files, include the header file Initguid.h before your header file.</span></span> <span data-ttu-id="7fc47-189">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="7fc47-189">For example:</span></span>


```C++
// Src1.cpp
#include <initguid.h>
#include "MyGuids.h"

// Src2.cpp
#include "MyGuids.h"

// Src3.cpp
#include "MyGuids.h"
```



<span data-ttu-id="7fc47-190">Wenn die Header Datei "Initguid. h" nicht eingeschlossen ist, erstellt das **\_ GUID** -Makro definieren einen `extern` Verweis auf den GUID-Wert.</span><span class="sxs-lookup"><span data-stu-id="7fc47-190">Wherever the Initguid.h header file is not included, the **DEFINE\_GUID** macro creates an `extern` reference to the GUID value.</span></span> <span data-ttu-id="7fc47-191">Wenn die Header Datei "Initguid. h" enthalten ist, wird das **definierende \_ GUID** -Makro neu definiert, sodass mit **define \_ GUID** eine definierende Deklaration der GUID erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="7fc47-191">When the Initguid.h header file is included, it redefines the **DEFINE\_GUID** macro so that **DEFINE\_GUID** creates a defining declaration of the GUID.</span></span>

<span data-ttu-id="7fc47-192">Wenn Sie Initguid. h nicht in eine der Quelldateien einschließen, wird der Link Fehler "nicht aufgelöstes externes Symbol" angezeigt.</span><span class="sxs-lookup"><span data-stu-id="7fc47-192">If you do not include Initguid.h in any of the source files, you will get a link error "unresolved external symbol."</span></span> <span data-ttu-id="7fc47-193">Wenn Sie Initguid. h zweimal für dieselbe GUID einschließen, erhalten Sie den Kompilierungsfehler "Neudefinition; mehrfache Initialisierung. "</span><span class="sxs-lookup"><span data-stu-id="7fc47-193">If you include Initguid.h twice for the same GUID, you will get a compile error "redefinition; multiple initialization."</span></span> <span data-ttu-id="7fc47-194">Stellen Sie sicher, dass Initguid. h genau einmal enthalten ist, um diese Fehler zu beheben.</span><span class="sxs-lookup"><span data-stu-id="7fc47-194">To resolve these errors, make sure that Initguid.h is included exactly once.</span></span> <span data-ttu-id="7fc47-195">Fügen Sie außerdem Initguid. h nicht in eine vorkompilierte Header Datei ein, da der vorkompilierte Header in jeder Quelldatei enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="7fc47-195">Also, do not include Initguid.h inside a precompiled header file, because in effect the precompiled header is included in every source file.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7fc47-196">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7fc47-196">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7fc47-197">Einführung in DirectShow</span><span class="sxs-lookup"><span data-stu-id="7fc47-197">Introduction to DirectShow</span></span>](introduction-to-directshow.md)
</dt> </dl>

 

 



