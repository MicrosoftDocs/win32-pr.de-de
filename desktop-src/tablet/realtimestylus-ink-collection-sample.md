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
# <a name="realtimestylus-ink-collection-sample"></a>RealTimeStylus Ink Collection-Beispiel

Diese Anwendung veranschaulicht die frei Hand Erfassung und das Rendering bei Verwendung der [**RealTimeStylus**](realtimestylus-class.md) -Klasse.

## <a name="the-inkcollection-project"></a>Das InkCollection-Projekt

Dieses Beispiel besteht aus einer einzelnen Projekt Mappe, die ein Projekt (InkCollection) enthält. Die Anwendung definiert den `InkCollection` Namespace, der eine einzelne Klasse enthält, die auch als bezeichnet wird `InkCollection` . Die Klasse erbt von der [Form](/dotnet/api/system.windows.forms.form?view=netcore-3.1) -Klasse und implementiert die [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) -Schnittstelle.


```C++
namespace InkCollection
{
    public class InkCollection : Form, IStylusAsyncPlugin
    {
        //...
      
```



Die InkCollection-Klasse definiert einen Satz privater Konstanten, die verwendet werden, um verschiedene frei Handstärke anzugeben. Die-Klasse deklariert auch private Instanzen der [**RealTimeStylus**](realtimestylus-class.md) -Klasse, `myRealTimeStylus` , der [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) -Klasse, `myDynamicRenderer` und der [Renderer](/previous-versions/ms828481(v=msdn.10)) -Klasse `myRenderer` . Der **DynamicRenderer** rendert den aktuell erfassten [Strich](/previous-versions/ms552692(v=vs.100)) . Das Rendererobjekt, `myRenderer` , rendert Stroke-Objekte, die bereits gesammelt wurden.


```C++
private const float ThinInkWidth = 10;
private const float MediumInkWidth = 100;
private const float ThickInkWidth = 200;

private RealTimeStylus myRealTimeStylus;

private DynamicRenderer myDynamicRenderer;
private Renderer myRenderer;
```



Die-Klasse deklariert auch ein [Hashtable](/previous-versions/windows/embedded/hh435144(v=msdn.10)) -Objekt, `myPackets` , das zum Speichern von Paketdaten verwendet wird, die von einem oder mehreren [Cursor](/previous-versions/ms552104(v=vs.100)) Objekten gesammelt werden. Die [ID](/previous-versions/ms824826(v=msdn.10)) -Werte des [Tablettstifts](/previous-versions/ms824824(v=msdn.10)) werden als Hash Tabellenschlüssel verwendet, um die für ein bestimmtes Cursor Objekt gesammelten Paketdaten eindeutig zu identifizieren.

Eine private [Instanz des frei Hand Objekts](/previous-versions/aa515768(v=msdn.10)) , `myInk` , speichert die von erfassten [Stroke](/previous-versions/ms552692(v=vs.100)) -Objekte `myRealTimeStylus` .


```C++
private Hashtable myPackets;
        
private Ink myInk;
```



## <a name="the-form-load-event"></a>Das Formular Lade Ereignis.

Im [Load](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) -Ereignishandler für das Formular `myDynamicRenderer` wird mit dem [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) instanziiert, der ein-Steuerelement als Argument annimmt, und `myRenderer` wird mit einem No-Argument-Konstruktor erstellt.


```C++
private void InkCollection_Load(object sender, System.EventArgs e)
{
    myDynamicRenderer = new DynamicRenderer(this);
    myRenderer = new Renderer();
    // ...
```



Beachten Sie den Kommentar, der der Instanziierung der Renderer folgt, da beim `myDynamicRenderer` Rendern der frei Hand Eingaben die Standardwerte für [DrawingAttributes](/previous-versions/ms837931(v=msdn.10)) verwendet. Dies ist das Standardverhalten. Wenn Sie jedoch die frei Hand Eingaben durch `myDynamicRenderer` ein anderes Aussehen von frei Hand Eingaben, die von gerendert `myRenderer` werden, übergeben möchten, können Sie die [DrawingAttributes](/previous-versions/ms826347(v=msdn.10)) -Eigenschaft in ändern `myDynamicRenderer` . Entfernen Sie hierzu die Auskommentierung der folgenden Zeilen, bevor Sie die Anwendung erstellen und ausführen.


```C++
    // myDynamicRenderer.DrawingAttributes.PenTip = PenTip.Rectangle;
    // myDynamicRenderer.DrawingAttributes.Height = (.5F)*MediumInkWidth;
    // myDynamicRenderer.DrawingAttributes.Transparency = 128;
```



Als Nächstes erstellt die Anwendung das [**RealTimeStylus**](realtimestylus-class.md) -Objekt, das zum Empfangen von tablettstiftbenachrichtigungen verwendet wird, und fügt das [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) -Objekt der synchronen Plug-in-Benachrichtigungs Warteschlange hinzu. Insbesondere wird `myRealTimeStylus` `myDynamicRenderer` der [SyncPluginCollection](/previous-versions/ms824833(v=msdn.10)) -Eigenschaft hinzugefügt.


```C++
    myRealTimeStylus = new RealTimeStylus(this, true);

    myRealTimeStylus.SyncPluginCollection.Add(myDynamicRenderer);
```



Das Formular wird dann der asynchronen Plug-in-Benachrichtigungs Warteschlange hinzugefügt. Insbesondere `InkCollection` wird der [AsyncPluginCollection](/previous-versions/ms824831(v=msdn.10)) -Eigenschaft hinzugefügt. Schließlich werden `myRealTimeStylus` und `myDynamicRenderer` aktiviert, und mypakete und myink werden instanziiert.


```C++
    myRealTimeStylus.AsyncPluginCollection.Add(this);

    myRealTimeStylus.Enabled = true;
    myDynamicRenderer.Enabled = true;  
      
    myPackets = new Hashtable();
    myInk = new Ink();
}
```



Abgesehen vom Einbinden der Menü Handler zum Ändern der frei Hand Farbe und-Größe ist vor der Implementierung der-Schnittstelle ein kurzer Codeblock erforderlich. Im Beispiel muss das [Paint](/dotnet/api/system.windows.forms.control.paint?view=netcore-3.1) -Ereignis des Formulars behandelt werden. Im-Ereignishandler muss die Anwendung aktualisiert werden, `myDynamicRenderer` da es möglich ist, dass ein [Stroke](/previous-versions/ms552692(v=vs.100)) -Objekt zu dem Zeitpunkt erfasst wird, zu dem das Paint-Ereignis auftritt. In diesem Fall muss der Teil des bereits gesammelten Stroke-Objekts neu gezeichnet werden. Der statische [Renderer](/previous-versions/ms828481(v=msdn.10)) wird zum erneuten Zeichnen von bereits gesammelten hubobjekten verwendet. Diese Striche befinden sich im [Ink](/previous-versions/aa515768(v=msdn.10)) -Objekt, da Sie dort platziert werden, wenn Sie gezeichnet werden, wie im nächsten Abschnitt gezeigt.


```C++
private void InkCollection_Paint(object sender, System.Windows.Forms.PaintEventArgs e)
{
    myDynamicRenderer.Refresh();

    myRenderer.Draw(e.Graphics, myInk.Strokes);
} 
```



## <a name="implementing-the-istylusasyncplugin-interface"></a>Implementieren der IStylusAsyncPlugin-Schnittstelle

Die Beispielanwendung definiert die Benachrichtigungs Typen, die für die Implementierung der [DataInterest](/previous-versions/ms824769(v=msdn.10)) -Eigenschaft von Interesse sind. Die DataInterest-Eigenschaft definiert daher, welche Benachrichtigungen das [**RealTimeStylus**](realtimestylus-class.md) -Objekt an das Formular weiterleitet. In diesem Beispiel definiert die DataInterest-Eigenschaft das Interesse an den **StylusDown**-, **Paketen**-, **StylusUp**-und **Fehler** Benachrichtigungen durch die [datainteressanmask](/previous-versions/ms824787(v=msdn.10)) -Enumeration.


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



Die [StylusDown](/previous-versions/ms824779(v=msdn.10)) -Benachrichtigung tritt auf, wenn der Stift die Digitalisierungs Oberfläche berührt. Wenn [dies der Fall](/previous-versions/ms824824(v=msdn.10)) ist, ordnet das Beispiel ein Array zu, das zum Speichern der Paketdaten für das tablettstiftobjekt verwendet wird. Die [StylusDownData](/previous-versions/ms824107(v=msdn.10)) -Methode aus der StylusDown-Methode wird dem Array hinzugefügt, und das Array wird mithilfe der [ID](/previous-versions/ms824826(v=msdn.10)) -Eigenschaft des tablettstiftobjekts als Schlüssel in die Hash Tabelle eingefügt.


```C++
public void StylusDown(RealTimeStylus sender, StylusDownData data)
{
    ArrayList collectedPackets = new ArrayList();

    collectedPackets.AddRange(data.GetData());

    myPackets.Add(data.Stylus.Id, collectedPackets);
}
```



Die Benachrichtigung über [Pakete](/previous-versions/ms824773(v=msdn.10)) tritt auf, wenn sich der Stift auf der Digitalisierungs Oberfläche bewegt. In diesem Fall fügt die [Anwendung dem Paket](/previous-versions/ms824824(v=msdn.10)) Array für das tablettstiftobjekt neue [StylusDownData](/previous-versions/ms824107(v=msdn.10)) hinzu. Dies erfolgt mithilfe der [ID](/previous-versions/ms824826(v=msdn.10)) -Eigenschaft des Tablettstifts Objekts als Schlüssel zum Abrufen des Paket Arrays für den Tablettstift aus der Hash Tabelle. Die neuen Paketdaten werden dann in das abgerufene Array eingefügt.


```C++
public void Packets(RealTimeStylus sender, PacketsData data)
{
    ((ArrayList)(myPackets[data.Stylus.Id])).AddRange(data.GetData());
}
```



Die [StylusUp](/previous-versions/ms824782(v=msdn.10)) -Benachrichtigung tritt auf, wenn der Stift die Digitalisierungs Oberfläche verlässt. Wenn diese Benachrichtigung auftritt, ruft das [Beispiel das Paket Array für dieses](/previous-versions/ms824824(v=msdn.10)) tablettstiftobjekt aus der Hash Tabelle ab und entfernt es aus der Hash Tabelle, da es nicht mehr benötigt wird, fügt die neuen Paketdaten hinzu und verwendet das Array von Paketdaten, um ein neues [Stroke](/previous-versions/ms552692(v=vs.100)) -Objekt,, zu erstellen `stroke` .


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



Ein Beispiel für eine stabilere Verwendung der [**RealTimeStylus**](realtimestylus-class.md) -Klasse, einschließlich der Verwendung der benutzerdefinierten Plug-in-Erstellung, finden Sie unter Beispiel für das [RealTimeStylus-Plug-in](realtimestylus-plug-in-sample.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Microsoft. Ink. Renderer](/previous-versions/ms552630(v=vs.100))
</dt> <dt>

[Microsoft. StylusInput. DynamicRenderer](/previous-versions/ms826345(v=msdn.10))
</dt> <dt>

[Microsoft. StylusInput. RealTimeStylus](/previous-versions/ms824830(v=msdn.10))
</dt> <dt>

[Microsoft. StylusInput. IStylusAsyncPlugin](/previous-versions/ms824768(v=msdn.10))
</dt> <dt>

[Zugreifen auf und Bearbeiten von Tablettstifteingaben](accessing-and-manipulating-stylus-input.md)
</dt> </dl>

 

 
