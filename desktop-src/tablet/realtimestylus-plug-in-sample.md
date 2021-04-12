---
description: Diese Anwendung veranschaulicht das Arbeiten mit der RealTimeStylus-Klasse.
ms.assetid: 0ba753d1-d81a-4f7a-942c-2967c46febec
title: Plug-in-Beispiel für RealTimeStylus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f593bf9e4fe0fb3d8ab12674047d6c05f28617a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218575"
---
# <a name="realtimestylus-plug-in-sample"></a><span data-ttu-id="79630-103">Plug-in-Beispiel für RealTimeStylus</span><span class="sxs-lookup"><span data-stu-id="79630-103">RealTimeStylus Plug-in Sample</span></span>

<span data-ttu-id="79630-104">Diese Anwendung veranschaulicht das Arbeiten mit der [**RealTimeStylus**](realtimestylus-class.md) -Klasse.</span><span class="sxs-lookup"><span data-stu-id="79630-104">This application demonstrates working with the [**RealTimeStylus**](realtimestylus-class.md) class.</span></span> <span data-ttu-id="79630-105">Eine ausführliche Übersicht über die StylusInput-APIs, einschließlich der **RealTimeStylus** -Klasse, finden Sie unter [zugreifen auf und](accessing-and-manipulating-stylus-input.md)Bearbeiten von Tablettstifteingaben.</span><span class="sxs-lookup"><span data-stu-id="79630-105">For a detailed overview of the StylusInput APIs, including the **RealTimeStylus** class, see [Accessing and Manipulating Stylus Input](accessing-and-manipulating-stylus-input.md).</span></span> <span data-ttu-id="79630-106">Weitere Informationen über synchrone und asynchrone Plug-Ins finden Sie unter [Plug-ins und RealTimeStylus-Klasse](plug-ins-and-the-realtimestylus-class.md).</span><span class="sxs-lookup"><span data-stu-id="79630-106">For information about synchronous and asynchronous plug-ins, see [Plug-ins and the RealTimeStylus Class](plug-ins-and-the-realtimestylus-class.md).</span></span>

## <a name="overview-of-the-sample"></a><span data-ttu-id="79630-107">Übersicht über das Beispiel</span><span class="sxs-lookup"><span data-stu-id="79630-107">Overview of the Sample</span></span>

<span data-ttu-id="79630-108">Plug-ins, Objekte, die die [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) -oder [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) -Schnittstelle implementieren, können einem [**RealTimeStylus**](realtimestylus-class.md) -Objekt hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="79630-108">Plug-ins, objects that implement the [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) or [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) interface can be added to a [**RealTimeStylus**](realtimestylus-class.md) object.</span></span> <span data-ttu-id="79630-109">Diese Beispielanwendung verwendet verschiedene Plug-in-Typen:</span><span class="sxs-lookup"><span data-stu-id="79630-109">This sample application uses several types of plug-in:</span></span>

-   <span data-ttu-id="79630-110">Paket Filter-Plug-in: ändert Pakete.</span><span class="sxs-lookup"><span data-stu-id="79630-110">Packet Filter Plug-in: Modifies packets.</span></span> <span data-ttu-id="79630-111">Mit dem Paketfilter-Plug-in in diesem Beispiel werden Paketinformationen geändert, indem alle (x, y)-Paketdaten innerhalb eines rechteckigen Bereichs eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="79630-111">The packet filter plug-in in this sample modifies packet information by constraining all (x,y) packet data within a rectangular area.</span></span>
-   <span data-ttu-id="79630-112">Benutzerdefiniertes Plug-in für dynamisches Renderer: ändert dynamische renderingqualitäten.</span><span class="sxs-lookup"><span data-stu-id="79630-112">Custom Dynamic Renderer Plug-in: Modifies dynamic rendering qualities.</span></span> <span data-ttu-id="79630-113">Das benutzerdefinierte Dynamic Rendering-Plug-in in diesem Beispiel ändert die Art und Weise, wie frei Hand Eingaben gerendert werden, indem ein kleiner Kreis um jeden (x, y) Punkt auf einem Strich gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="79630-113">The custom dynamic rendering plug-in in this sample modifies the way ink is rendered by drawing a small circle around each (x,y) point on a stroke.</span></span>
-   <span data-ttu-id="79630-114">Dynamic Renderer-Plug-in: ändert dynamische renderingqualitäten.</span><span class="sxs-lookup"><span data-stu-id="79630-114">Dynamic Renderer Plug-in: Modifies dynamic rendering qualities.</span></span> <span data-ttu-id="79630-115">In diesem Beispiel wird veranschaulicht, wie das [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) -Objekt als Plug-in verwendet wird, um das dynamische Rendering von frei Hand Eingaben zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="79630-115">This sample demonstrates use of the [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) object as a plug-in to handle dynamic rendering of ink.</span></span>
-   <span data-ttu-id="79630-116">Gesten Erkennungs-Plug-in: erkennt Anwendungs Gesten.</span><span class="sxs-lookup"><span data-stu-id="79630-116">Gesture Recognizer Plug-in: Recognizes application gestures.</span></span> <span data-ttu-id="79630-117">Dieses Beispiel veranschaulicht die Verwendung des [**GestureRecognizer**](gesturerecognizer-class.md) -Objekts als Plug-in, um Anwendungs Gesten zu erkennen (bei Ausführung auf einem System mit der Microsoft Gestenerkennung).</span><span class="sxs-lookup"><span data-stu-id="79630-117">This sample demonstrates use of the [**GestureRecognizer**](gesturerecognizer-class.md) object as a plug-in to recognize application gestures (when running on a system with the Microsoft gesture recognizer present).</span></span>

<span data-ttu-id="79630-118">Außerdem wird in diesem Beispiel eine Benutzeroberfläche bereitstellt, mit der der Benutzer die Reihenfolge der einzelnen Plug-ins in der Sammlung hinzufügen, entfernen und ändern kann.</span><span class="sxs-lookup"><span data-stu-id="79630-118">In addition, this sample provides a user interface that enables the user to add, remove, and change the order of each plug-in in the collection.</span></span> <span data-ttu-id="79630-119">Die Beispiel Projekt Mappe enthält zwei Projekte: realtimestyluspluginapp und realtimestylusplugins.</span><span class="sxs-lookup"><span data-stu-id="79630-119">The sample solution contains two projects, RealTimeStylusPluginApp and RealTimeStylusPlugins.</span></span> <span data-ttu-id="79630-120">Realtimestyluspluginapp enthält die Benutzeroberfläche für das Beispiel.</span><span class="sxs-lookup"><span data-stu-id="79630-120">RealTimeStylusPluginApp contains the user interface for the sample.</span></span> <span data-ttu-id="79630-121">Realtimestylusplugins enthält die Implementierungen der Plug-ins. Das realtimestylusplugins-Projekt definiert den realtimestylusplugins-Namespace, der den Paketfilter und die benutzerdefinierten dynamischen Renderer-Plug-Ins enthält. Auf diesen Namespace wird vom Projekt realtimestyluspluginapp verwiesen.</span><span class="sxs-lookup"><span data-stu-id="79630-121">RealTimeStylusPlugins contains the implementations of the plug-ins. The RealTimeStylusPlugins project defines the RealTimeStylusPlugins namespace, which contains the packet filter and custom dynamic renderer plug-ins. This namespace is referenced by the RealTimeStylusPluginApp project.</span></span> <span data-ttu-id="79630-122">Das Projekt realtimestylusplugins verwendet die Namespaces [Microsoft. Ink](/previous-versions/ms826516(v=msdn.10)), [Microsoft. StylusInput](/previous-versions/ms824750(v=msdn.10))und [Microsoft. StylusInput. PluginData](/previous-versions/ms823992(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="79630-122">The RealTimeStylusPlugins project uses the [Microsoft.Ink](/previous-versions/ms826516(v=msdn.10)), [Microsoft.StylusInput](/previous-versions/ms824750(v=msdn.10)), and [Microsoft.StylusInput.PluginData](/previous-versions/ms823992(v=msdn.10)) namespaces.</span></span>

<span data-ttu-id="79630-123">Eine Übersicht über die Namespaces " [Microsoft. StylusInput](/previous-versions/ms824750(v=msdn.10)) " und " [Microsoft. StylusInput. PluginData](/previous-versions/ms823992(v=msdn.10)) " finden Sie unter [Architektur der StylusInput-APIs](architecture-of-the-stylusinput-apis.md).</span><span class="sxs-lookup"><span data-stu-id="79630-123">For an overview of the [Microsoft.StylusInput](/previous-versions/ms824750(v=msdn.10)) and [Microsoft.StylusInput.PluginData](/previous-versions/ms823992(v=msdn.10)) namespaces see [Architecture of the StylusInput APIs](architecture-of-the-stylusinput-apis.md).</span></span>

## <a name="packet-filter-plug-in"></a><span data-ttu-id="79630-124">Paket Filter-Plug-in</span><span class="sxs-lookup"><span data-stu-id="79630-124">Packet Filter Plug-in</span></span>

<span data-ttu-id="79630-125">Das Paketfilter-Plug-in ist ein synchrones Plug-in, das die Paket Änderung veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="79630-125">The packet filter plug-in is a synchronous plug-in that demonstrates packet modification.</span></span> <span data-ttu-id="79630-126">Insbesondere wird ein Rechteck im Formular definiert.</span><span class="sxs-lookup"><span data-stu-id="79630-126">Specifically, it defines a rectangle on the form.</span></span> <span data-ttu-id="79630-127">Alle Pakete, die außerhalb des Bereichs gezeichnet werden, werden innerhalb des Bereichs gerendert.</span><span class="sxs-lookup"><span data-stu-id="79630-127">Any packets that are drawn outside the region are rendered inside the region.</span></span> <span data-ttu-id="79630-128">Die Plug-in-Klasse, `PacketFilterPlugin` , registriert sich für die Benachrichtigung von `StylusDown` `StylusUp` -,-und- `Packets` Stift Eingabe Ereignissen.</span><span class="sxs-lookup"><span data-stu-id="79630-128">The plug-in class, `PacketFilterPlugin`, registers for notification of `StylusDown`, `StylusUp`, and `Packets` pen input events.</span></span> <span data-ttu-id="79630-129">Die-Klasse implementiert die [StylusDown](/previous-versions/ms824761(v=msdn.10))-, [StylusUp](/previous-versions/ms824764(v=msdn.10))-und [Pakete](/previous-versions/ms824756(v=msdn.10)) -Methoden, die für die [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) -Klasse definiert sind.</span><span class="sxs-lookup"><span data-stu-id="79630-129">The class implements the [StylusDown](/previous-versions/ms824761(v=msdn.10)), [StylusUp](/previous-versions/ms824764(v=msdn.10)), and [Packets](/previous-versions/ms824756(v=msdn.10)) methods defined on [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) class.</span></span>

<span data-ttu-id="79630-130">Der öffentliche Konstruktor für `PacketFilterPlugin` erfordert eine [Rechteck](/dotnet/api/system.drawing.rectangle?view=netcore-3.1) Struktur.</span><span class="sxs-lookup"><span data-stu-id="79630-130">The public constructor for `PacketFilterPlugin` requires a [Rectangle](/dotnet/api/system.drawing.rectangle?view=netcore-3.1) structure.</span></span> <span data-ttu-id="79630-131">Dieses Rechteck definiert den rechteckigen Bereich in Freihand Raumkoordinaten (01mm = 1 HIMETRIC Unit), in denen Pakete enthalten sein werden.</span><span class="sxs-lookup"><span data-stu-id="79630-131">This rectangle defines the rectangular area, in ink space coordinates (.01mm = 1 HIMETRIC unit), in which packets will be contained.</span></span> <span data-ttu-id="79630-132">Das Rechteck wird in einem privaten Feld gespeichert `rectangle` .</span><span class="sxs-lookup"><span data-stu-id="79630-132">The rectangle is held in a private field, `rectangle`.</span></span>


```C++
public class PacketFilterPlugin:IStylusSyncPlugin  
{
    private System.Drawing.Rectangle rectangle = System.Drawing.Rectangle.Empty;
    public PacketFilterPlugin(Rectangle r)
    {
        rectangle = r;
    }
    // ...
```



<span data-ttu-id="79630-133">Die `PacketFilterPlugin` Klasse registriert sich für Ereignis Benachrichtigungen, indem Sie den Get-Accessor für die [DataInterest](/previous-versions/ms824752(v=msdn.10)) -Eigenschaft implementiert.</span><span class="sxs-lookup"><span data-stu-id="79630-133">The `PacketFilterPlugin` class registers for event notifications by implementing the get accessor for the [DataInterest](/previous-versions/ms824752(v=msdn.10)) property.</span></span> <span data-ttu-id="79630-134">In diesem Fall ist das Plug-in an der Reaktion auf die `StylusDown` Benachrichtigungen, `Packets` , `StylusUp` und interessiert `Error` .</span><span class="sxs-lookup"><span data-stu-id="79630-134">In this case, the plug-in has interested in responding to the `StylusDown`, `Packets`, `StylusUp`, and `Error` notifications.</span></span> <span data-ttu-id="79630-135">Im Beispiel werden diese Werte entsprechend der Definition in der [datainteressanmask](/previous-versions/ms824787(v=msdn.10)) -Enumeration zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="79630-135">The sample returns these values as defined in the [DataInterestMask](/previous-versions/ms824787(v=msdn.10)) enumeration.</span></span> <span data-ttu-id="79630-136">Die [StylusDown](/previous-versions/ms824761(v=msdn.10)) -Methode wird aufgerufen, wenn der Stift Tipp die Digitalisierungs Oberfläche kontaktiert.</span><span class="sxs-lookup"><span data-stu-id="79630-136">The [StylusDown](/previous-versions/ms824761(v=msdn.10)) method is called when the pen tip contacts the digitizer surface.</span></span> <span data-ttu-id="79630-137">Die [StylusUp](/previous-versions/ms824764(v=msdn.10)) -Methode wird aufgerufen, wenn die Stift Spitze die Digitalisierungs Oberfläche verlässt.</span><span class="sxs-lookup"><span data-stu-id="79630-137">The [StylusUp](/previous-versions/ms824764(v=msdn.10)) method is called when the pen tip leaves the digitizer surface.</span></span> <span data-ttu-id="79630-138">Die [Paketen](/previous-versions/ms824756(v=msdn.10)) -Methode wird aufgerufen, wenn das [**RealTimeStylus**](realtimestylus-class.md) -objektpakete empfängt.</span><span class="sxs-lookup"><span data-stu-id="79630-138">The [Packets](/previous-versions/ms824756(v=msdn.10)) method is called when the [**RealTimeStylus**](realtimestylus-class.md) object receives packets.</span></span> <span data-ttu-id="79630-139">Die [Error](/previous-versions/ms585069(v=vs.100)) -Methode wird aufgerufen, wenn das aktuelle Plug-in oder ein vorheriges Plug-in eine Ausnahme auslöst.</span><span class="sxs-lookup"><span data-stu-id="79630-139">The [Error](/previous-versions/ms585069(v=vs.100)) method is called when the current plug-in or a previous plug-in throws an exception.</span></span>


```C++
public DataInterestMask DataInterest
{
    get
    {
        return DataInterestMask.StylusDown | 
               DataInterestMask.Packets | 
               DataInterestMask.StylusUp | 
               DataInterestMask.Error;
    }
}           
    //...
```



<span data-ttu-id="79630-140">Die- `PacketFilterPlugin` Klasse verarbeitet die meisten dieser Benachrichtigungen in einer Hilfsmethode, `ModifyPacketData` .</span><span class="sxs-lookup"><span data-stu-id="79630-140">The `PacketFilterPlugin` class handles most of these notifications in a helper method, `ModifyPacketData`.</span></span> <span data-ttu-id="79630-141">Die `ModifyPacketData` -Methode ruft die x-und y-Werte für jedes neue Paket aus der [PacketsData](/previous-versions/ms824590(v=msdn.10)) -Klasse ab.</span><span class="sxs-lookup"><span data-stu-id="79630-141">The `ModifyPacketData` method gets the x and y values for each new packet from the [PacketsData](/previous-versions/ms824590(v=msdn.10)) class.</span></span> <span data-ttu-id="79630-142">Wenn einer der beiden Werte außerhalb des Rechtecks liegt, ersetzt die Methode den Wert durch den nächstgelegenen Punkt, der noch innerhalb des Rechtecks liegt.</span><span class="sxs-lookup"><span data-stu-id="79630-142">If either value is outside the rectangle, the method replaces the value with the nearest point that still falls within the rectangle.</span></span> <span data-ttu-id="79630-143">Dies ist ein Beispiel dafür, wie ein Plug-in Paketdaten ersetzen kann, wenn Sie vom Stift Eingabedaten Strom empfangen werden.</span><span class="sxs-lookup"><span data-stu-id="79630-143">This is an example of how a plug-in can replace packet data as it is received from the pen-input stream.</span></span>


```C++
private void ModifyPacketData(StylusDataBase data)
{
    for (int i = 0; i < data.Count ; i += data.PacketPropertyCount)
    {
        // packet data always has x followed by y followed by the rest
        int x = data[i];
        int y = data[i+1];

        // Constrain points to the input rectangle
        x = Math.Max(x, rectangle.Left);
        x = Math.Min(x, rectangle.Right);
        y = Math.Max(y, rectangle.Top);
        y = Math.Min(y, rectangle.Bottom);

        // If necessary, modify the x,y packet data
        if (x != data[i])
        {
            data[i] = x;
        }
        if (y != data[i+1])
        {
            data[i+1] = y;
        } 
    }
}
```



## <a name="custom-dynamic-renderer-plug-in"></a><span data-ttu-id="79630-144">Benutzerdefiniertes Plug-in für dynamisches Renderer</span><span class="sxs-lookup"><span data-stu-id="79630-144">Custom Dynamic Renderer Plug-in</span></span>

<span data-ttu-id="79630-145">Die `CustomDynamicRenderer` -Klasse implementiert auch die [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) -Klasse, um Stift Eingabe Benachrichtigungen zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="79630-145">The `CustomDynamicRenderer` class also implements the [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) class to receive pen-input notifications.</span></span> <span data-ttu-id="79630-146">Anschließend wird die `Packets` Benachrichtigung verarbeitet, um einen kleinen Kreis um jeden neuen Paket Punkt zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="79630-146">It then handles the `Packets` notification to draw a small circle around each new packet point.</span></span>

<span data-ttu-id="79630-147">Die-Klasse enthält eine [Grafik](/dotnet/api/system.drawing.graphics?view=dotnet-plat-ext-3.1&preserve-view=true) Variable, die einen Verweis auf das Grafik Objekt enthält, das an den-Klassenkonstruktor übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="79630-147">The class contains a [Graphics](/dotnet/api/system.drawing.graphics?view=dotnet-plat-ext-3.1&preserve-view=true) variable that holds a reference to the graphics object passed into the class constructor.</span></span> <span data-ttu-id="79630-148">Dies ist das Grafik Objekt, das für das dynamische Rendering verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="79630-148">This is the graphics object used for dynamic rendering.</span></span>


```C++
private Graphics myGraphics;

public CustomDynamicRendererPlugin(Graphics g)
{
    myGraphics = g;
}
        //...
            
```



<span data-ttu-id="79630-149">Wenn das Plug-in für den benutzerdefinierten dynamischen Renderer eine Benachrichtigung über Pakete empfängt, werden die (x, y)-Daten extrahiert und ein kleiner grüner Kreis um den Punkt gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="79630-149">When the custom dynamic renderer plug-in receives a Packets notification, it extracts the (x,y) data and draws a small green circle around the point.</span></span> <span data-ttu-id="79630-150">Dies ist ein Beispiel für ein benutzerdefiniertes Rendering, das auf dem Stift Eingabedaten Strom basiert.</span><span class="sxs-lookup"><span data-stu-id="79630-150">This is an example of custom rendering based on the pen-input stream.</span></span>


```C++
public void Packets(RealTimeStylus sender,  PacketsData data)
{           
    for (int i = 0; i < data.Count; i += data.PacketPropertyCount)
    {
        // Packet data always has x followed by y followed by the rest
        Point point = new Point(data[i], data[i+1]);

        // Since the packet data is in Ink Space coordinates, we need to convert to Pixels...
        point.X = (int)Math.Round((float)point.X * (float)myGraphics.DpiX/2540.0F);
        point.Y = (int)Math.Round((float)point.Y * (float)myGraphics.DpiY/2540.0F);

        // Draw a circle corresponding to the packet
        myGraphics.DrawEllipse(Pens.Green, point.X - 2, point.Y - 2, 4, 4);
    }
}
```



## <a name="the-realtimestyluspluginapp-project"></a><span data-ttu-id="79630-151">Das realtimestyluspluginapp-Projekt</span><span class="sxs-lookup"><span data-stu-id="79630-151">The RealTimeStylusPluginApp Project</span></span>

<span data-ttu-id="79630-152">Das Projekt realtimestyluspluginapp veranschaulicht die zuvor beschriebenen Plug-ins sowie die Plug-ins " [**GestureRecognizer**](gesturerecognizer-class.md) " und " [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) ". Die Benutzeroberfläche des Projekts besteht aus folgendem:</span><span class="sxs-lookup"><span data-stu-id="79630-152">The RealTimeStylusPluginApp project demonstrates the plug-ins previously described, as well as the [**GestureRecognizer**](gesturerecognizer-class.md) and [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) plug-ins. The project's user interface consists of:</span></span>

-   <span data-ttu-id="79630-153">Ein Formular, das ein [GroupBox](/dotnet/api/system.windows.forms.groupbox?view=netcore-3.1) -Steuerelement enthält, mit dem der frei Hand Eingabebereich definiert wird.</span><span class="sxs-lookup"><span data-stu-id="79630-153">A Form that contains a [GroupBox](/dotnet/api/system.windows.forms.groupbox?view=netcore-3.1) control used to define the ink entry area.</span></span>
-   <span data-ttu-id="79630-154">Ein [CheckedListBox](/dotnet/api/system.windows.forms.checkedlistbox?view=netcore-3.1) -Steuerelement zum Auflisten und Auswählen der verfügbaren Plug-ins.</span><span class="sxs-lookup"><span data-stu-id="79630-154">A [CheckedListBox](/dotnet/api/system.windows.forms.checkedlistbox?view=netcore-3.1) control to list and select the available plug-ins.</span></span>
-   <span data-ttu-id="79630-155">Ein paar von [Schaltflächen Objekten](/dotnet/api/system.windows.forms.button?view=netcore-3.1) , um die Neuanordnung der Plug-ins zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="79630-155">A pair of [Button objects](/dotnet/api/system.windows.forms.button?view=netcore-3.1) to enable re-ordering the plug-ins.</span></span>

<span data-ttu-id="79630-156">Das Projekt definiert eine Struktur, `PlugInListItem` , um die Verwaltung der im Projekt verwendeten Plug-ins zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="79630-156">The project defines a structure, `PlugInListItem`, to make managing the plug-ins used in the project easier.</span></span> <span data-ttu-id="79630-157">Die `PlugInListItem` -Struktur enthält das Plug-in und eine Beschreibung.</span><span class="sxs-lookup"><span data-stu-id="79630-157">The `PlugInListItem` structure contains the plug-in and a description.</span></span>

<span data-ttu-id="79630-158">Die `RealTimeStylusPluginApp` Klasse selbst implementiert die Klasse [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) .</span><span class="sxs-lookup"><span data-stu-id="79630-158">The `RealTimeStylusPluginApp` class itself implements the [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) class.</span></span> <span data-ttu-id="79630-159">Dies ist erforderlich, damit die- `RealTimeStylusPluginApp` Klasse benachrichtigt werden kann, wenn das [**GestureRecognizer**](gesturerecognizer-class.md) -Plug-in der Ausgabe Warteschlange Gesten Daten hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="79630-159">This is necessary so that the `RealTimeStylusPluginApp` class can be notified when the [**GestureRecognizer**](gesturerecognizer-class.md) plug-in adds gesture data to the output queue.</span></span> <span data-ttu-id="79630-160">Die Anwendung wird für die Benachrichtigung von [CustomStylusDataAdded](/previous-versions/ms824753(v=msdn.10))registriert.</span><span class="sxs-lookup"><span data-stu-id="79630-160">The application registers for notification of [CustomStylusDataAdded](/previous-versions/ms824753(v=msdn.10)).</span></span> <span data-ttu-id="79630-161">Wenn Gesten Daten empfangen werden, wird `RealTimeStylusPluginApp` eine Beschreibung dieser in der Statusleiste am unteren Rand des Formulars platziert.</span><span class="sxs-lookup"><span data-stu-id="79630-161">When gesture data is received, `RealTimeStylusPluginApp` places a description of it on the status bar at the bottom of the form.</span></span>


```C++
public void CustomStylusDataAdded(RealTimeStylus sender, CustomStylusData data)
{
    if (data.CustomDataId == GestureRecognizer.GestureRecognitionDataGuid)
    {
        GestureRecognitionData grd = data.Data as GestureRecognitionData;
        if (grd != null)
        {
            if (grd.Count > 0)
            {
                GestureAlternate ga = grd[0];
                sbGesture.Text = "Gesture=" + ga.Id + ", Confidence=" + ga.Confidence;
            }
        }
    }
}
```



> [!Note]  
> In der [CustomStylusDataAdded](/previous-versions/ms824753(v=msdn.10)) -Implementierung ist es interessant, dass Sie die benutzerdefinierten Gesten Daten in der Ausgabe Warteschlange entweder mithilfe der GUID (mit dem Feld " [GestureRecognitionDataGuid](/previous-versions/ms826344(v=msdn.10)) ") oder nach Typ (mit dem Ergebnis der AS-Anweisung) identifizieren können. <span data-ttu-id="79630-163">In diesem Beispiel werden beide Identifikationstechniken zu Demonstrationszwecken verwendet.</span><span class="sxs-lookup"><span data-stu-id="79630-163">The sample uses both identification techniques for demonstration purposes.</span></span> <span data-ttu-id="79630-164">Beide Ansätze sind ebenfalls gültig.</span><span class="sxs-lookup"><span data-stu-id="79630-164">Either approach alone is also valid.</span></span>

 

<span data-ttu-id="79630-165">Im Lade Ereignishandler des Formulars erstellt die Anwendung Instanzen der `PacketFilter` -Klasse und der- `CustomDynamicRenderer` Klasse und fügt Sie dem Listenfeld hinzu.</span><span class="sxs-lookup"><span data-stu-id="79630-165">In the Form's Load event handler, the application creates instances of the `PacketFilter` and `CustomDynamicRenderer` classes and adds them to the list box.</span></span> <span data-ttu-id="79630-166">Die Anwendung versucht dann, eine Instanz der [**GestureRecognizer**](gesturerecognizer-class.md) -Klasse zu erstellen, und fügt Sie, wenn erfolgreich, dem Listenfeld hinzu.</span><span class="sxs-lookup"><span data-stu-id="79630-166">The application then attempts to create an instance of the [**GestureRecognizer**](gesturerecognizer-class.md) class and, if successful, adds it to the list box.</span></span> <span data-ttu-id="79630-167">Dies schlägt fehl, wenn die Gestenerkennung nicht auf dem System vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="79630-167">This fails if the gesture recognizer is not present on the system.</span></span> <span data-ttu-id="79630-168">Als nächstes instanziiert die Anwendung ein [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) -Objekt und fügt es dem Listenfeld hinzu.</span><span class="sxs-lookup"><span data-stu-id="79630-168">Next, the application instantiates a [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) object and adds it to the list box.</span></span> <span data-ttu-id="79630-169">Schließlich aktiviert die Anwendung alle Plug-ins und das [**RealTimeStylus**](realtimestylus-class.md) -Objekt selbst.</span><span class="sxs-lookup"><span data-stu-id="79630-169">Finally, the application enables each of the plug-ins and the [**RealTimeStylus**](realtimestylus-class.md) object itself.</span></span>

<span data-ttu-id="79630-170">Ein weiterer wichtiger Aspekt für das Beispiel ist, dass in den Hilfsmethoden das [**RealTimeStylus**](realtimestylus-class.md) -Objekt zuerst deaktiviert wird, bevor Plug-Ins hinzugefügt oder entfernt und dann wieder aktiviert werden, nachdem das Hinzufügen oder Entfernen beendet wurde.</span><span class="sxs-lookup"><span data-stu-id="79630-170">Another important thing to note about the sample is that in the helper methods, the [**RealTimeStylus**](realtimestylus-class.md) object is first disabled before plug-ins are added or removed and then re-enabled after the addition or removal is complete.</span></span>


```C++
private void RemoveFromPluginCollection(int index)
{
    IStylusSyncPlugin plugin = ((PluginListItem)chklbPlugins.Items[index]).Plugin;

    bool rtsEnabled = myRealTimeStylus.Enabled;
    myRealTimeStylus.Enabled = false;
    myRealTimeStylus.SyncPluginCollection.Remove(plugin);
    myRealTimeStylus.Enabled = rtsEnabled;
}
```



## <a name="related-topics"></a><span data-ttu-id="79630-171">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="79630-171">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="79630-172">[Microsoft. StylusInput. DynamicRenderer](/previous-versions/ms575176(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="79630-172">[Microsoft.StylusInput.DynamicRenderer](/previous-versions/ms575176(v=vs.100))</span></span>
</dt> <dt>

<span data-ttu-id="79630-173">[Microsoft. StylusInput. GestureRecognizer](/previous-versions/ms826046(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="79630-173">[Microsoft.StylusInput.GestureRecognizer](/previous-versions/ms826046(v=msdn.10))</span></span>
</dt> <dt>

<span data-ttu-id="79630-174">[Microsoft. StylusInput. RealTimeStylus](/previous-versions/ms824830(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="79630-174">[Microsoft.StylusInput.RealTimeStylus](/previous-versions/ms824830(v=msdn.10))</span></span>
</dt> <dt>

<span data-ttu-id="79630-175">[Microsoft. StylusInput. datainteressanmask](/previous-versions/ms575174(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="79630-175">[Microsoft.StylusInput.DataInterestMask](/previous-versions/ms575174(v=vs.100))</span></span>
</dt> <dt>

<span data-ttu-id="79630-176">[Microsoft. StylusInput. IStylusSyncPlugin](/previous-versions/ms824751(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="79630-176">[Microsoft.StylusInput.IStylusSyncPlugin](/previous-versions/ms824751(v=msdn.10))</span></span>
</dt> <dt>

<span data-ttu-id="79630-177">[Microsoft. StylusInput. IStylusAsyncPlugin](/previous-versions/ms824768(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="79630-177">[Microsoft.StylusInput.IStylusAsyncPlugin](/previous-versions/ms824768(v=msdn.10))</span></span>
</dt> <dt>

<span data-ttu-id="79630-178">[Microsoft. StylusInput. PluginData. packegsdata](/previous-versions/ms575281(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="79630-178">[Microsoft.StylusInput.PluginData.PacketsData](/previous-versions/ms575281(v=vs.100))</span></span>
</dt> <dt>

[<span data-ttu-id="79630-179">Zugreifen auf und Bearbeiten von Tablettstifteingaben</span><span class="sxs-lookup"><span data-stu-id="79630-179">Accessing and Manipulating Stylus Input</span></span>](accessing-and-manipulating-stylus-input.md)
</dt> <dt>

[<span data-ttu-id="79630-180">Plug-ins und die RealTimeStylus-Klasse</span><span class="sxs-lookup"><span data-stu-id="79630-180">Plug-ins and the RealTimeStylus Class</span></span>](plug-ins-and-the-realtimestylus-class.md)
</dt> <dt>

[<span data-ttu-id="79630-181">RealTimeStylus Ink Collection-Beispiel</span><span class="sxs-lookup"><span data-stu-id="79630-181">RealTimeStylus Ink Collection Sample</span></span>](realtimestylus-ink-collection-sample.md)
</dt> </dl>

 

 
