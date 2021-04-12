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
# <a name="realtimestylus-plug-in-sample"></a>Plug-in-Beispiel für RealTimeStylus

Diese Anwendung veranschaulicht das Arbeiten mit der [**RealTimeStylus**](realtimestylus-class.md) -Klasse. Eine ausführliche Übersicht über die StylusInput-APIs, einschließlich der **RealTimeStylus** -Klasse, finden Sie unter [zugreifen auf und](accessing-and-manipulating-stylus-input.md)Bearbeiten von Tablettstifteingaben. Weitere Informationen über synchrone und asynchrone Plug-Ins finden Sie unter [Plug-ins und RealTimeStylus-Klasse](plug-ins-and-the-realtimestylus-class.md).

## <a name="overview-of-the-sample"></a>Übersicht über das Beispiel

Plug-ins, Objekte, die die [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) -oder [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) -Schnittstelle implementieren, können einem [**RealTimeStylus**](realtimestylus-class.md) -Objekt hinzugefügt werden. Diese Beispielanwendung verwendet verschiedene Plug-in-Typen:

-   Paket Filter-Plug-in: ändert Pakete. Mit dem Paketfilter-Plug-in in diesem Beispiel werden Paketinformationen geändert, indem alle (x, y)-Paketdaten innerhalb eines rechteckigen Bereichs eingeschränkt werden.
-   Benutzerdefiniertes Plug-in für dynamisches Renderer: ändert dynamische renderingqualitäten. Das benutzerdefinierte Dynamic Rendering-Plug-in in diesem Beispiel ändert die Art und Weise, wie frei Hand Eingaben gerendert werden, indem ein kleiner Kreis um jeden (x, y) Punkt auf einem Strich gezeichnet wird.
-   Dynamic Renderer-Plug-in: ändert dynamische renderingqualitäten. In diesem Beispiel wird veranschaulicht, wie das [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) -Objekt als Plug-in verwendet wird, um das dynamische Rendering von frei Hand Eingaben zu verarbeiten.
-   Gesten Erkennungs-Plug-in: erkennt Anwendungs Gesten. Dieses Beispiel veranschaulicht die Verwendung des [**GestureRecognizer**](gesturerecognizer-class.md) -Objekts als Plug-in, um Anwendungs Gesten zu erkennen (bei Ausführung auf einem System mit der Microsoft Gestenerkennung).

Außerdem wird in diesem Beispiel eine Benutzeroberfläche bereitstellt, mit der der Benutzer die Reihenfolge der einzelnen Plug-ins in der Sammlung hinzufügen, entfernen und ändern kann. Die Beispiel Projekt Mappe enthält zwei Projekte: realtimestyluspluginapp und realtimestylusplugins. Realtimestyluspluginapp enthält die Benutzeroberfläche für das Beispiel. Realtimestylusplugins enthält die Implementierungen der Plug-ins. Das realtimestylusplugins-Projekt definiert den realtimestylusplugins-Namespace, der den Paketfilter und die benutzerdefinierten dynamischen Renderer-Plug-Ins enthält. Auf diesen Namespace wird vom Projekt realtimestyluspluginapp verwiesen. Das Projekt realtimestylusplugins verwendet die Namespaces [Microsoft. Ink](/previous-versions/ms826516(v=msdn.10)), [Microsoft. StylusInput](/previous-versions/ms824750(v=msdn.10))und [Microsoft. StylusInput. PluginData](/previous-versions/ms823992(v=msdn.10)) .

Eine Übersicht über die Namespaces " [Microsoft. StylusInput](/previous-versions/ms824750(v=msdn.10)) " und " [Microsoft. StylusInput. PluginData](/previous-versions/ms823992(v=msdn.10)) " finden Sie unter [Architektur der StylusInput-APIs](architecture-of-the-stylusinput-apis.md).

## <a name="packet-filter-plug-in"></a>Paket Filter-Plug-in

Das Paketfilter-Plug-in ist ein synchrones Plug-in, das die Paket Änderung veranschaulicht. Insbesondere wird ein Rechteck im Formular definiert. Alle Pakete, die außerhalb des Bereichs gezeichnet werden, werden innerhalb des Bereichs gerendert. Die Plug-in-Klasse, `PacketFilterPlugin` , registriert sich für die Benachrichtigung von `StylusDown` `StylusUp` -,-und- `Packets` Stift Eingabe Ereignissen. Die-Klasse implementiert die [StylusDown](/previous-versions/ms824761(v=msdn.10))-, [StylusUp](/previous-versions/ms824764(v=msdn.10))-und [Pakete](/previous-versions/ms824756(v=msdn.10)) -Methoden, die für die [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) -Klasse definiert sind.

Der öffentliche Konstruktor für `PacketFilterPlugin` erfordert eine [Rechteck](/dotnet/api/system.drawing.rectangle?view=netcore-3.1) Struktur. Dieses Rechteck definiert den rechteckigen Bereich in Freihand Raumkoordinaten (01mm = 1 HIMETRIC Unit), in denen Pakete enthalten sein werden. Das Rechteck wird in einem privaten Feld gespeichert `rectangle` .


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



Die `PacketFilterPlugin` Klasse registriert sich für Ereignis Benachrichtigungen, indem Sie den Get-Accessor für die [DataInterest](/previous-versions/ms824752(v=msdn.10)) -Eigenschaft implementiert. In diesem Fall ist das Plug-in an der Reaktion auf die `StylusDown` Benachrichtigungen, `Packets` , `StylusUp` und interessiert `Error` . Im Beispiel werden diese Werte entsprechend der Definition in der [datainteressanmask](/previous-versions/ms824787(v=msdn.10)) -Enumeration zurückgegeben. Die [StylusDown](/previous-versions/ms824761(v=msdn.10)) -Methode wird aufgerufen, wenn der Stift Tipp die Digitalisierungs Oberfläche kontaktiert. Die [StylusUp](/previous-versions/ms824764(v=msdn.10)) -Methode wird aufgerufen, wenn die Stift Spitze die Digitalisierungs Oberfläche verlässt. Die [Paketen](/previous-versions/ms824756(v=msdn.10)) -Methode wird aufgerufen, wenn das [**RealTimeStylus**](realtimestylus-class.md) -objektpakete empfängt. Die [Error](/previous-versions/ms585069(v=vs.100)) -Methode wird aufgerufen, wenn das aktuelle Plug-in oder ein vorheriges Plug-in eine Ausnahme auslöst.


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



Die- `PacketFilterPlugin` Klasse verarbeitet die meisten dieser Benachrichtigungen in einer Hilfsmethode, `ModifyPacketData` . Die `ModifyPacketData` -Methode ruft die x-und y-Werte für jedes neue Paket aus der [PacketsData](/previous-versions/ms824590(v=msdn.10)) -Klasse ab. Wenn einer der beiden Werte außerhalb des Rechtecks liegt, ersetzt die Methode den Wert durch den nächstgelegenen Punkt, der noch innerhalb des Rechtecks liegt. Dies ist ein Beispiel dafür, wie ein Plug-in Paketdaten ersetzen kann, wenn Sie vom Stift Eingabedaten Strom empfangen werden.


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



## <a name="custom-dynamic-renderer-plug-in"></a>Benutzerdefiniertes Plug-in für dynamisches Renderer

Die `CustomDynamicRenderer` -Klasse implementiert auch die [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) -Klasse, um Stift Eingabe Benachrichtigungen zu empfangen. Anschließend wird die `Packets` Benachrichtigung verarbeitet, um einen kleinen Kreis um jeden neuen Paket Punkt zu zeichnen.

Die-Klasse enthält eine [Grafik](/dotnet/api/system.drawing.graphics?view=dotnet-plat-ext-3.1&preserve-view=true) Variable, die einen Verweis auf das Grafik Objekt enthält, das an den-Klassenkonstruktor übergeben wird. Dies ist das Grafik Objekt, das für das dynamische Rendering verwendet wird.


```C++
private Graphics myGraphics;

public CustomDynamicRendererPlugin(Graphics g)
{
    myGraphics = g;
}
        //...
            
```



Wenn das Plug-in für den benutzerdefinierten dynamischen Renderer eine Benachrichtigung über Pakete empfängt, werden die (x, y)-Daten extrahiert und ein kleiner grüner Kreis um den Punkt gezeichnet. Dies ist ein Beispiel für ein benutzerdefiniertes Rendering, das auf dem Stift Eingabedaten Strom basiert.


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



## <a name="the-realtimestyluspluginapp-project"></a>Das realtimestyluspluginapp-Projekt

Das Projekt realtimestyluspluginapp veranschaulicht die zuvor beschriebenen Plug-ins sowie die Plug-ins " [**GestureRecognizer**](gesturerecognizer-class.md) " und " [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) ". Die Benutzeroberfläche des Projekts besteht aus folgendem:

-   Ein Formular, das ein [GroupBox](/dotnet/api/system.windows.forms.groupbox?view=netcore-3.1) -Steuerelement enthält, mit dem der frei Hand Eingabebereich definiert wird.
-   Ein [CheckedListBox](/dotnet/api/system.windows.forms.checkedlistbox?view=netcore-3.1) -Steuerelement zum Auflisten und Auswählen der verfügbaren Plug-ins.
-   Ein paar von [Schaltflächen Objekten](/dotnet/api/system.windows.forms.button?view=netcore-3.1) , um die Neuanordnung der Plug-ins zu aktivieren.

Das Projekt definiert eine Struktur, `PlugInListItem` , um die Verwaltung der im Projekt verwendeten Plug-ins zu vereinfachen. Die `PlugInListItem` -Struktur enthält das Plug-in und eine Beschreibung.

Die `RealTimeStylusPluginApp` Klasse selbst implementiert die Klasse [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) . Dies ist erforderlich, damit die- `RealTimeStylusPluginApp` Klasse benachrichtigt werden kann, wenn das [**GestureRecognizer**](gesturerecognizer-class.md) -Plug-in der Ausgabe Warteschlange Gesten Daten hinzufügt. Die Anwendung wird für die Benachrichtigung von [CustomStylusDataAdded](/previous-versions/ms824753(v=msdn.10))registriert. Wenn Gesten Daten empfangen werden, wird `RealTimeStylusPluginApp` eine Beschreibung dieser in der Statusleiste am unteren Rand des Formulars platziert.


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
> In der [CustomStylusDataAdded](/previous-versions/ms824753(v=msdn.10)) -Implementierung ist es interessant, dass Sie die benutzerdefinierten Gesten Daten in der Ausgabe Warteschlange entweder mithilfe der GUID (mit dem Feld " [GestureRecognitionDataGuid](/previous-versions/ms826344(v=msdn.10)) ") oder nach Typ (mit dem Ergebnis der AS-Anweisung) identifizieren können. In diesem Beispiel werden beide Identifikationstechniken zu Demonstrationszwecken verwendet. Beide Ansätze sind ebenfalls gültig.

 

Im Lade Ereignishandler des Formulars erstellt die Anwendung Instanzen der `PacketFilter` -Klasse und der- `CustomDynamicRenderer` Klasse und fügt Sie dem Listenfeld hinzu. Die Anwendung versucht dann, eine Instanz der [**GestureRecognizer**](gesturerecognizer-class.md) -Klasse zu erstellen, und fügt Sie, wenn erfolgreich, dem Listenfeld hinzu. Dies schlägt fehl, wenn die Gestenerkennung nicht auf dem System vorhanden ist. Als nächstes instanziiert die Anwendung ein [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) -Objekt und fügt es dem Listenfeld hinzu. Schließlich aktiviert die Anwendung alle Plug-ins und das [**RealTimeStylus**](realtimestylus-class.md) -Objekt selbst.

Ein weiterer wichtiger Aspekt für das Beispiel ist, dass in den Hilfsmethoden das [**RealTimeStylus**](realtimestylus-class.md) -Objekt zuerst deaktiviert wird, bevor Plug-Ins hinzugefügt oder entfernt und dann wieder aktiviert werden, nachdem das Hinzufügen oder Entfernen beendet wurde.


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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Microsoft. StylusInput. DynamicRenderer](/previous-versions/ms575176(v=vs.100))
</dt> <dt>

[Microsoft. StylusInput. GestureRecognizer](/previous-versions/ms826046(v=msdn.10))
</dt> <dt>

[Microsoft. StylusInput. RealTimeStylus](/previous-versions/ms824830(v=msdn.10))
</dt> <dt>

[Microsoft. StylusInput. datainteressanmask](/previous-versions/ms575174(v=vs.100))
</dt> <dt>

[Microsoft. StylusInput. IStylusSyncPlugin](/previous-versions/ms824751(v=msdn.10))
</dt> <dt>

[Microsoft. StylusInput. IStylusAsyncPlugin](/previous-versions/ms824768(v=msdn.10))
</dt> <dt>

[Microsoft. StylusInput. PluginData. packegsdata](/previous-versions/ms575281(v=vs.100))
</dt> <dt>

[Zugreifen auf und Bearbeiten von Tablettstifteingaben](accessing-and-manipulating-stylus-input.md)
</dt> <dt>

[Plug-ins und die RealTimeStylus-Klasse](plug-ins-and-the-realtimestylus-class.md)
</dt> <dt>

[RealTimeStylus Ink Collection-Beispiel](realtimestylus-ink-collection-sample.md)
</dt> </dl>

 

 
