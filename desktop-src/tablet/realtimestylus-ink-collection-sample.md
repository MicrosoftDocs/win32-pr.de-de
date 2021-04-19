---
description: Diese Anwendung veranschaulicht die frei Hand Erfassung und das Rendering bei Verwendung der RealTimeStylus-Klasse.
ms.assetid: f8bce153-cc5d-4087-896f-3f60afc80bc8
title: RealTimeStylus Ink Collection-Beispiel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24fe67ed59ea1a69f5d0d9a2656169f2df88a450
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359419"
---
# <a name="realtimestylus-ink-collection-sample"></a><span data-ttu-id="b8a50-103">RealTimeStylus Ink Collection-Beispiel</span><span class="sxs-lookup"><span data-stu-id="b8a50-103">RealTimeStylus Ink Collection Sample</span></span>

<span data-ttu-id="b8a50-104">Diese Anwendung veranschaulicht die frei Hand Erfassung und das Rendering bei Verwendung der [**RealTimeStylus**](realtimestylus-class.md) -Klasse.</span><span class="sxs-lookup"><span data-stu-id="b8a50-104">This application demonstrates ink collection and rendering when using the [**RealTimeStylus**](realtimestylus-class.md) class.</span></span>

## <a name="the-inkcollection-project"></a><span data-ttu-id="b8a50-105">Das InkCollection-Projekt</span><span class="sxs-lookup"><span data-stu-id="b8a50-105">The InkCollection Project</span></span>

<span data-ttu-id="b8a50-106">Dieses Beispiel besteht aus einer einzelnen Projekt Mappe, die ein Projekt (InkCollection) enthält.</span><span class="sxs-lookup"><span data-stu-id="b8a50-106">This sample consists of a single solution that contains one project, InkCollection.</span></span> <span data-ttu-id="b8a50-107">Die Anwendung definiert den `InkCollection` Namespace, der eine einzelne Klasse enthält, die auch als bezeichnet wird `InkCollection` .</span><span class="sxs-lookup"><span data-stu-id="b8a50-107">The application defines the `InkCollection` namespace that contains a single class, also called `InkCollection`.</span></span> <span data-ttu-id="b8a50-108">Die Klasse erbt von der [Form](/dotnet/api/system.windows.forms.form?view=netcore-3.1) -Klasse und implementiert die [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="b8a50-108">The class inherits from the [Form](/dotnet/api/system.windows.forms.form?view=netcore-3.1) class and implements the [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) interface.</span></span>


```C++
namespace InkCollection
{
    public class InkCollection : Form, IStylusAsyncPlugin
    {
        //...
      
```



<span data-ttu-id="b8a50-109">Die InkCollection-Klasse definiert einen Satz privater Konstanten, die verwendet werden, um verschiedene frei Handstärke anzugeben.</span><span class="sxs-lookup"><span data-stu-id="b8a50-109">The InkCollection Class defines a set of private constants used to specify various ink thickness.</span></span> <span data-ttu-id="b8a50-110">Die-Klasse deklariert auch private Instanzen der [**RealTimeStylus**](realtimestylus-class.md) -Klasse, `myRealTimeStylus` , der [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) -Klasse, `myDynamicRenderer` und der [Renderer](/previous-versions/ms828481(v=msdn.10)) -Klasse `myRenderer` .</span><span class="sxs-lookup"><span data-stu-id="b8a50-110">The class also declares private instances of the [**RealTimeStylus**](realtimestylus-class.md) class, `myRealTimeStylus`, the [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) class, `myDynamicRenderer`, and the [Renderer](/previous-versions/ms828481(v=msdn.10)) class `myRenderer`.</span></span> <span data-ttu-id="b8a50-111">Der **DynamicRenderer** rendert den aktuell erfassten [Strich](/previous-versions/ms552692(v=vs.100)) .</span><span class="sxs-lookup"><span data-stu-id="b8a50-111">The **DynamicRenderer** renders the [Stroke](/previous-versions/ms552692(v=vs.100)) that is currently being collected.</span></span> <span data-ttu-id="b8a50-112">Das Rendererobjekt, `myRenderer` , rendert Stroke-Objekte, die bereits gesammelt wurden.</span><span class="sxs-lookup"><span data-stu-id="b8a50-112">The Renderer object, `myRenderer`, renders Stroke objects that have already been collected.</span></span>


```C++
private const float ThinInkWidth = 10;
private const float MediumInkWidth = 100;
private const float ThickInkWidth = 200;

private RealTimeStylus myRealTimeStylus;

private DynamicRenderer myDynamicRenderer;
private Renderer myRenderer;
```



<span data-ttu-id="b8a50-113">Die-Klasse deklariert auch ein [Hashtable](/previous-versions/windows/embedded/hh435144(v=msdn.10)) -Objekt, `myPackets` , das zum Speichern von Paketdaten verwendet wird, die von einem oder mehreren [Cursor](/previous-versions/ms552104(v=vs.100)) Objekten gesammelt werden.</span><span class="sxs-lookup"><span data-stu-id="b8a50-113">The class also declares a [Hashtable](/previous-versions/windows/embedded/hh435144(v=msdn.10)) object, `myPackets`, which is used to store packet data that is being collected by one or more [Cursor](/previous-versions/ms552104(v=vs.100)) objects.</span></span> <span data-ttu-id="b8a50-114">Die [ID](/previous-versions/ms824826(v=msdn.10)) -Werte des [Tablettstifts](/previous-versions/ms824824(v=msdn.10)) werden als Hash Tabellenschlüssel verwendet, um die für ein bestimmtes Cursor Objekt gesammelten Paketdaten eindeutig zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="b8a50-114">The [Stylus](/previous-versions/ms824824(v=msdn.10)) object's [Id](/previous-versions/ms824826(v=msdn.10)) values are used as the hashtable key to uniquely identify the packet data collected for a given Cursor object.</span></span>

<span data-ttu-id="b8a50-115">Eine private [Instanz des frei Hand Objekts](/previous-versions/aa515768(v=msdn.10)) , `myInk` , speichert die von erfassten [Stroke](/previous-versions/ms552692(v=vs.100)) -Objekte `myRealTimeStylus` .</span><span class="sxs-lookup"><span data-stu-id="b8a50-115">A private instance of the [Ink](/previous-versions/aa515768(v=msdn.10)) object, `myInk`, stores [Stroke](/previous-versions/ms552692(v=vs.100)) objects collected by `myRealTimeStylus`.</span></span>


```C++
private Hashtable myPackets;
        
private Ink myInk;
```



## <a name="the-form-load-event"></a><span data-ttu-id="b8a50-116">Das Formular Lade Ereignis.</span><span class="sxs-lookup"><span data-stu-id="b8a50-116">The Form Load Event</span></span>

<span data-ttu-id="b8a50-117">Im [Load](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) -Ereignishandler für das Formular `myDynamicRenderer` wird mit dem [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) instanziiert, der ein-Steuerelement als Argument annimmt, und `myRenderer` wird mit einem No-Argument-Konstruktor erstellt.</span><span class="sxs-lookup"><span data-stu-id="b8a50-117">In the [Load](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) event handler for the form, `myDynamicRenderer` is instantiated by using the [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) that takes a control as an argument, and `myRenderer` is constructed with a no-argument constructor.</span></span>


```C++
private void InkCollection_Load(object sender, System.EventArgs e)
{
    myDynamicRenderer = new DynamicRenderer(this);
    myRenderer = new Renderer();
    // ...
```



<span data-ttu-id="b8a50-118">Beachten Sie den Kommentar, der der Instanziierung der Renderer folgt, da beim `myDynamicRenderer` Rendern der frei Hand Eingaben die Standardwerte für [DrawingAttributes](/previous-versions/ms837931(v=msdn.10)) verwendet.</span><span class="sxs-lookup"><span data-stu-id="b8a50-118">Pay attention to the comment that follows the instantiation of the renderers, because `myDynamicRenderer` uses the default values for [DrawingAttributes](/previous-versions/ms837931(v=msdn.10)) when rendering the ink.</span></span> <span data-ttu-id="b8a50-119">Dies ist das Standardverhalten.</span><span class="sxs-lookup"><span data-stu-id="b8a50-119">This is standard behavior.</span></span> <span data-ttu-id="b8a50-120">Wenn Sie jedoch die frei Hand Eingaben durch `myDynamicRenderer` ein anderes Aussehen von frei Hand Eingaben, die von gerendert `myRenderer` werden, übergeben möchten, können Sie die [DrawingAttributes](/previous-versions/ms826347(v=msdn.10)) -Eigenschaft in ändern `myDynamicRenderer` .</span><span class="sxs-lookup"><span data-stu-id="b8a50-120">However, if you wish to give the ink rendered by `myDynamicRenderer` a different look from ink rendered by `myRenderer`, you can change the [DrawingAttributes](/previous-versions/ms826347(v=msdn.10)) property on `myDynamicRenderer`.</span></span> <span data-ttu-id="b8a50-121">Entfernen Sie hierzu die Auskommentierung der folgenden Zeilen, bevor Sie die Anwendung erstellen und ausführen.</span><span class="sxs-lookup"><span data-stu-id="b8a50-121">To do so, uncomment the following lines before you build and run the application.</span></span>


```C++
    // myDynamicRenderer.DrawingAttributes.PenTip = PenTip.Rectangle;
    // myDynamicRenderer.DrawingAttributes.Height = (.5F)*MediumInkWidth;
    // myDynamicRenderer.DrawingAttributes.Transparency = 128;
```



<span data-ttu-id="b8a50-122">Als Nächstes erstellt die Anwendung das [**RealTimeStylus**](realtimestylus-class.md) -Objekt, das zum Empfangen von tablettstiftbenachrichtigungen verwendet wird, und fügt das [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) -Objekt der synchronen Plug-in-Benachrichtigungs Warteschlange hinzu.</span><span class="sxs-lookup"><span data-stu-id="b8a50-122">Next, the application creates the [**RealTimeStylus**](realtimestylus-class.md) object that is used to receive stylus notifications and adds the [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) object to the synchronous plug-in notification queue.</span></span> <span data-ttu-id="b8a50-123">Insbesondere wird `myRealTimeStylus` `myDynamicRenderer` der [SyncPluginCollection](/previous-versions/ms824833(v=msdn.10)) -Eigenschaft hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="b8a50-123">Specifically, `myRealTimeStylus` adds `myDynamicRenderer` to the [SyncPluginCollection](/previous-versions/ms824833(v=msdn.10)) property.</span></span>


```C++
    myRealTimeStylus = new RealTimeStylus(this, true);

    myRealTimeStylus.SyncPluginCollection.Add(myDynamicRenderer);
```



<span data-ttu-id="b8a50-124">Das Formular wird dann der asynchronen Plug-in-Benachrichtigungs Warteschlange hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="b8a50-124">The form is then added to the asynchronous plug-in notification queue.</span></span> <span data-ttu-id="b8a50-125">Insbesondere `InkCollection` wird der [AsyncPluginCollection](/previous-versions/ms824831(v=msdn.10)) -Eigenschaft hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="b8a50-125">Specifically, `InkCollection` is added to the [AsyncPluginCollection](/previous-versions/ms824831(v=msdn.10)) property.</span></span> <span data-ttu-id="b8a50-126">Schließlich werden `myRealTimeStylus` und `myDynamicRenderer` aktiviert, und mypakete und myink werden instanziiert.</span><span class="sxs-lookup"><span data-stu-id="b8a50-126">Finally, `myRealTimeStylus` and `myDynamicRenderer` are enabled, and myPackets and myInk are instantiated.</span></span>


```C++
    myRealTimeStylus.AsyncPluginCollection.Add(this);

    myRealTimeStylus.Enabled = true;
    myDynamicRenderer.Enabled = true;  
      
    myPackets = new Hashtable();
    myInk = new Ink();
}
```



<span data-ttu-id="b8a50-127">Abgesehen vom Einbinden der Menü Handler zum Ändern der frei Hand Farbe und-Größe ist vor der Implementierung der-Schnittstelle ein kurzer Codeblock erforderlich.</span><span class="sxs-lookup"><span data-stu-id="b8a50-127">Aside from hooking up the menu handlers for changing ink color and size, one more brief block of code is required before implementing the interface.</span></span> <span data-ttu-id="b8a50-128">Im Beispiel muss das [Paint](/dotnet/api/system.windows.forms.control.paint?view=netcore-3.1) -Ereignis des Formulars behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="b8a50-128">The sample must handle the form's [Paint](/dotnet/api/system.windows.forms.control.paint?view=netcore-3.1) event.</span></span> <span data-ttu-id="b8a50-129">Im-Ereignishandler muss die Anwendung aktualisiert werden, `myDynamicRenderer` da es möglich ist, dass ein [Stroke](/previous-versions/ms552692(v=vs.100)) -Objekt zu dem Zeitpunkt erfasst wird, zu dem das Paint-Ereignis auftritt.</span><span class="sxs-lookup"><span data-stu-id="b8a50-129">In the event handler, the application must refresh `myDynamicRenderer` because it is possible that a [Stroke](/previous-versions/ms552692(v=vs.100)) object is being collected at the time the Paint event occurs.</span></span> <span data-ttu-id="b8a50-130">In diesem Fall muss der Teil des bereits gesammelten Stroke-Objekts neu gezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="b8a50-130">In that case, the portion of the Stroke object that has already been collected needs to be redrawn.</span></span> <span data-ttu-id="b8a50-131">Der statische [Renderer](/previous-versions/ms828481(v=msdn.10)) wird zum erneuten Zeichnen von bereits gesammelten hubobjekten verwendet.</span><span class="sxs-lookup"><span data-stu-id="b8a50-131">The static [Renderer](/previous-versions/ms828481(v=msdn.10)) is used to re-draw Stroke objects that have already been collected.</span></span> <span data-ttu-id="b8a50-132">Diese Striche befinden sich im [Ink](/previous-versions/aa515768(v=msdn.10)) -Objekt, da Sie dort platziert werden, wenn Sie gezeichnet werden, wie im nächsten Abschnitt gezeigt.</span><span class="sxs-lookup"><span data-stu-id="b8a50-132">These strokes are in the [Ink](/previous-versions/aa515768(v=msdn.10)) object because they are placed there when drawn, as shown in the next section.</span></span>


```C++
private void InkCollection_Paint(object sender, System.Windows.Forms.PaintEventArgs e)
{
    myDynamicRenderer.Refresh();

    myRenderer.Draw(e.Graphics, myInk.Strokes);
} 
```



## <a name="implementing-the-istylusasyncplugin-interface"></a><span data-ttu-id="b8a50-133">Implementieren der IStylusAsyncPlugin-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="b8a50-133">Implementing the IStylusAsyncPlugin Interface</span></span>

<span data-ttu-id="b8a50-134">Die Beispielanwendung definiert die Benachrichtigungs Typen, die für die Implementierung der [DataInterest](/previous-versions/ms824769(v=msdn.10)) -Eigenschaft von Interesse sind.</span><span class="sxs-lookup"><span data-stu-id="b8a50-134">The sample application defines the types of notifications it has interest in receiving in the implementation of the [DataInterest](/previous-versions/ms824769(v=msdn.10)) property.</span></span> <span data-ttu-id="b8a50-135">Die DataInterest-Eigenschaft definiert daher, welche Benachrichtigungen das [**RealTimeStylus**](realtimestylus-class.md) -Objekt an das Formular weiterleitet.</span><span class="sxs-lookup"><span data-stu-id="b8a50-135">The DataInterest property therefore defines which notifications that the [**RealTimeStylus**](realtimestylus-class.md) object forwards to the form.</span></span> <span data-ttu-id="b8a50-136">In diesem Beispiel definiert die DataInterest-Eigenschaft das Interesse an den **StylusDown**-, **Paketen**-, **StylusUp**-und **Fehler** Benachrichtigungen durch die [datainteressanmask](/previous-versions/ms824787(v=msdn.10)) -Enumeration.</span><span class="sxs-lookup"><span data-stu-id="b8a50-136">For this sample, the DataInterest property defines interest in the **StylusDown**, **Packets**, **StylusUp**, and **Error** notifications through the [DataInterestMask](/previous-versions/ms824787(v=msdn.10)) enumeration.</span></span>


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
```



<span data-ttu-id="b8a50-137">Die [StylusDown](/previous-versions/ms824779(v=msdn.10)) -Benachrichtigung tritt auf, wenn der Stift die Digitalisierungs Oberfläche berührt.</span><span class="sxs-lookup"><span data-stu-id="b8a50-137">The [StylusDown](/previous-versions/ms824779(v=msdn.10)) notification occurs when the pen touches the digitizer surface.</span></span> <span data-ttu-id="b8a50-138">Wenn [dies der Fall](/previous-versions/ms824824(v=msdn.10)) ist, ordnet das Beispiel ein Array zu, das zum Speichern der Paketdaten für das tablettstiftobjekt verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b8a50-138">When this happens, the sample allocates an array that is used to store the packet data for the [Stylus](/previous-versions/ms824824(v=msdn.10)) object.</span></span> <span data-ttu-id="b8a50-139">Die [StylusDownData](/previous-versions/ms824107(v=msdn.10)) -Methode aus der StylusDown-Methode wird dem Array hinzugefügt, und das Array wird mithilfe der [ID](/previous-versions/ms824826(v=msdn.10)) -Eigenschaft des tablettstiftobjekts als Schlüssel in die Hash Tabelle eingefügt.</span><span class="sxs-lookup"><span data-stu-id="b8a50-139">The [StylusDownData](/previous-versions/ms824107(v=msdn.10)) from the StylusDown method is added to the array, and the array is inserted into the hashtable by using the Stylus object's [Id](/previous-versions/ms824826(v=msdn.10)) property as a key.</span></span>


```C++
public void StylusDown(RealTimeStylus sender, StylusDownData data)
{
    ArrayList collectedPackets = new ArrayList();

    collectedPackets.AddRange(data.GetData());

    myPackets.Add(data.Stylus.Id, collectedPackets);
}
```



<span data-ttu-id="b8a50-140">Die Benachrichtigung über [Pakete](/previous-versions/ms824773(v=msdn.10)) tritt auf, wenn sich der Stift auf der Digitalisierungs Oberfläche bewegt.</span><span class="sxs-lookup"><span data-stu-id="b8a50-140">The [Packets](/previous-versions/ms824773(v=msdn.10)) notification occurs when the pen moves on the digitizer surface.</span></span> <span data-ttu-id="b8a50-141">In diesem Fall fügt die [Anwendung dem Paket](/previous-versions/ms824824(v=msdn.10)) Array für das tablettstiftobjekt neue [StylusDownData](/previous-versions/ms824107(v=msdn.10)) hinzu.</span><span class="sxs-lookup"><span data-stu-id="b8a50-141">When this occurs, the application adds new [StylusDownData](/previous-versions/ms824107(v=msdn.10)) into the packet array for the [Stylus](/previous-versions/ms824824(v=msdn.10)) object.</span></span> <span data-ttu-id="b8a50-142">Dies erfolgt mithilfe der [ID](/previous-versions/ms824826(v=msdn.10)) -Eigenschaft des Tablettstifts Objekts als Schlüssel zum Abrufen des Paket Arrays für den Tablettstift aus der Hash Tabelle.</span><span class="sxs-lookup"><span data-stu-id="b8a50-142">It does this by using the Stylus object's [Id](/previous-versions/ms824826(v=msdn.10)) property as the key to retrieve the packet array for the stylus from the hashtable.</span></span> <span data-ttu-id="b8a50-143">Die neuen Paketdaten werden dann in das abgerufene Array eingefügt.</span><span class="sxs-lookup"><span data-stu-id="b8a50-143">The new packet data is then inserted into the retrieved array.</span></span>


```C++
public void Packets(RealTimeStylus sender, PacketsData data)
{
    ((ArrayList)(myPackets[data.Stylus.Id])).AddRange(data.GetData());
}
```



<span data-ttu-id="b8a50-144">Die [StylusUp](/previous-versions/ms824782(v=msdn.10)) -Benachrichtigung tritt auf, wenn der Stift die Digitalisierungs Oberfläche verlässt.</span><span class="sxs-lookup"><span data-stu-id="b8a50-144">The [StylusUp](/previous-versions/ms824782(v=msdn.10)) notification occurs when the pen leaves the digitizer surface.</span></span> <span data-ttu-id="b8a50-145">Wenn diese Benachrichtigung auftritt, ruft das [Beispiel das Paket Array für dieses](/previous-versions/ms824824(v=msdn.10)) tablettstiftobjekt aus der Hash Tabelle ab und entfernt es aus der Hash Tabelle, da es nicht mehr benötigt wird, fügt die neuen Paketdaten hinzu und verwendet das Array von Paketdaten, um ein neues [Stroke](/previous-versions/ms552692(v=vs.100)) -Objekt,, zu erstellen `stroke` .</span><span class="sxs-lookup"><span data-stu-id="b8a50-145">When this notification occurs, the sample retrieves the packet array for this [Stylus](/previous-versions/ms824824(v=msdn.10)) object from the hashtable-removing it from the hashtable as it is no longer needed, adds in the new packet data, and uses the array of packet data to create a new [Stroke](/previous-versions/ms552692(v=vs.100)) object, `stroke`.</span></span>


```C++
public void StylusUp(RealTimeStylus sender, StylusUpData data)
{
    ArrayList collectedPackets = (ArrayList)myPackets[data.Stylus.Id];
    myPackets.Remove(data.Stylus.Id);

    collectedPackets.AddRange(data.GetData());

    int[] packets = (int[])(collectedPackets.ToArray(typeof(int)));
    TabletPropertyDescriptionCollection tabletProperties =
        myRealTimeStylus.GetTabletPropertyDescriptionCollection(data.Stylus.TabletContextId);

    Stroke stroke = myInk.CreateStroke(packets, tabletProperties);
    if (stroke != null) 
    {
         stroke.DrawingAttributes.Color = myDynamicRenderer.DrawingAttributes.Color;
         stroke.DrawingAttributes.Width = myDynamicRenderer.DrawingAttributes.Width;
    } 
}
```



<span data-ttu-id="b8a50-146">Ein Beispiel für eine stabilere Verwendung der [**RealTimeStylus**](realtimestylus-class.md) -Klasse, einschließlich der Verwendung der benutzerdefinierten Plug-in-Erstellung, finden Sie unter Beispiel für das [RealTimeStylus-Plug-in](realtimestylus-plug-in-sample.md).</span><span class="sxs-lookup"><span data-stu-id="b8a50-146">For an example that shows more robust use of the [**RealTimeStylus**](realtimestylus-class.md) class, including the use of custom plug-in creation, see [RealTimeStylus Plug-in Sample](realtimestylus-plug-in-sample.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b8a50-147">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b8a50-147">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="b8a50-148">[Microsoft. Ink. Renderer](/previous-versions/ms552630(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="b8a50-148">[Microsoft.Ink.Renderer](/previous-versions/ms552630(v=vs.100))</span></span>
</dt> <dt>

<span data-ttu-id="b8a50-149">[Microsoft. StylusInput. DynamicRenderer](/previous-versions/ms826345(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="b8a50-149">[Microsoft.StylusInput.DynamicRenderer](/previous-versions/ms826345(v=msdn.10))</span></span>
</dt> <dt>

<span data-ttu-id="b8a50-150">[Microsoft. StylusInput. RealTimeStylus](/previous-versions/ms824830(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="b8a50-150">[Microsoft.StylusInput.RealTimeStylus](/previous-versions/ms824830(v=msdn.10))</span></span>
</dt> <dt>

<span data-ttu-id="b8a50-151">[Microsoft. StylusInput. IStylusAsyncPlugin](/previous-versions/ms824768(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="b8a50-151">[Microsoft.StylusInput.IStylusAsyncPlugin](/previous-versions/ms824768(v=msdn.10))</span></span>
</dt> <dt>

[<span data-ttu-id="b8a50-152">Zugreifen auf und Bearbeiten von Tablettstifteingaben</span><span class="sxs-lookup"><span data-stu-id="b8a50-152">Accessing and Manipulating Stylus Input</span></span>](accessing-and-manipulating-stylus-input.md)
</dt> </dl>

 

 
