---
description: Diese Anwendung veranschaulicht die Verwendung der RealTimeStylus-Klasse.
ms.assetid: 0ba753d1-d81a-4f7a-942c-2967c46febec
title: RealTimeStylus-Plug-In-Beispiel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a05fd9c70c11130011352d8c16d30abee672e4cd56c000c21b7fbfd2704babe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118966879"
---
# <a name="realtimestylus-plug-in-sample"></a>RealTimeStylus-Plug-In-Beispiel

Diese Anwendung veranschaulicht die Verwendung der [**RealTimeStylus-Klasse.**](realtimestylus-class.md) Eine ausführliche Übersicht über die StylusInput-APIs, einschließlich der **RealTimeStylus-Klasse,** finden Sie unter Zugreifen auf und Bearbeiten [von Stifteingaben.](accessing-and-manipulating-stylus-input.md) Informationen zu synchronen und asynchronen Plug-Ins finden Sie unter [Plug-Ins und die RealTimeStylus-Klasse](plug-ins-and-the-realtimestylus-class.md).

## <a name="overview-of-the-sample"></a>Übersicht über das Beispiel

Plug-Ins, Objekte, die die [**IStylusSyncPlugin-**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) oder [**IStylusAsyncPlugin-Schnittstelle**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) implementieren, können einem [**RealTimeStylus-Objekt hinzugefügt**](realtimestylus-class.md) werden. Diese Beispielanwendung verwendet mehrere Arten von Plug-Ins:

-   Paketfilter-Plug-In: Ändert Pakete. Das Paketfilter-Plug-In in diesem Beispiel ändert Paketinformationen, indem es alle (x,y)-Paketdaten innerhalb eines rechteckigen Bereichs einschränkt.
-   Benutzerdefiniertes Dynamisches Renderer-Plug-In: Ändert dynamische Renderingqualitäten. Das benutzerdefinierte Dynamische Rendering-Plug-In in diesem Beispiel ändert die Art und Weise, wie Ink gerendert wird, indem ein kleiner Kreis um jeden (x,y)-Punkt eines Strichs gezeichnunget wird.
-   Dynamisches Renderer-Plug-In: Ändert dynamische Renderingqualitäten. In diesem Beispiel wird die Verwendung des [**DynamicRenderer-Objekts**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) als Plug-In zum Verarbeiten des dynamischen Renderings von Ink veranschaulicht.
-   Gestenerkennungs-Plug-In: Erkennt Anwendungsgesten. In diesem Beispiel wird veranschaulicht, wie das [**GestureRecognizer-Objekt**](gesturerecognizer-class.md) als Plug-In verwendet wird, um Anwendungsgesten zu erkennen (wenn die Gestenerkennung von Microsoft auf einem System ausgeführt wird).

Darüber hinaus stellt dieses Beispiel eine Benutzeroberfläche bereit, die es dem Benutzer ermöglicht, die Reihenfolge der einzelnen Plug-Ins in der Auflistung hinzuzufügen, zu entfernen und zu ändern. Die Beispiellösung enthält zwei Projekte: RealTimeStylusPluginApp und RealTimeStylusPlugins. RealTimeStylusPluginApp enthält die Benutzeroberfläche für das Beispiel. RealTimeStylusPlugins enthält die Implementierungen der Plug-Ins. Das RealTimeStylusPlugins-Projekt definiert den RealTimeStylusPlugins-Namespace, der den Paketfilter und benutzerdefinierte Plug-Ins für dynamische Renderer enthält. Auf diesen Namespace wird vom RealTimeStylusPluginApp-Projekt verwiesen. Das RealTimeStylusPlugins-Projekt verwendet die [Namespaces Microsoft.Ink,](/previous-versions/ms826516(v=msdn.10)) [Microsoft.StylusInput](/previous-versions/ms824750(v=msdn.10))und [Microsoft.StylusInput.PluginData.](/previous-versions/ms823992(v=msdn.10))

Eine Übersicht über die [Namespaces Microsoft.StylusInput](/previous-versions/ms824750(v=msdn.10)) und [Microsoft.StylusInput.PluginData](/previous-versions/ms823992(v=msdn.10)) finden Sie unter Architektur der [StylusInput-APIs](architecture-of-the-stylusinput-apis.md).

## <a name="packet-filter-plug-in"></a>Paketfilter-Plug-In

Das Paketfilter-Plug-In ist ein synchrones Plug-In, das die Paketänderung veranschaulicht. Insbesondere wird ein Rechteck auf dem Formular definiert. Alle Pakete, die außerhalb des -Bereich gezeichnet werden, werden innerhalb des -Bereich gerendert. Die Plug-In-Klasse `PacketFilterPlugin` registriert für die Benachrichtigung von `StylusDown` Stifteingabeereignissen `StylusUp` , und `Packets` . Die -Klasse implementiert die [Methoden StylusDown,](/previous-versions/ms824761(v=msdn.10)) [StylusUp](/previous-versions/ms824764(v=msdn.10))und [Packets,](/previous-versions/ms824756(v=msdn.10)) die für die [**IStylusSyncPlugin-Klasse definiert**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) sind.

Der öffentliche Konstruktor für `PacketFilterPlugin` erfordert eine [Rectangle-Struktur.](/dotnet/api/system.drawing.rectangle?view=netcore-3.1) Dieses Rechteck definiert den rechteckigen Bereich in Freiraumkoordinaten (.01mm = 1 HIMETRIC-Einheit), in dem Pakete enthalten sind. Das Rechteck wird in einem privaten Feld( ) `rectangle` gehalten.


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



Die `PacketFilterPlugin` -Klasse registriert sich für Ereignisbenachrichtigungen, indem sie den get-Accessor für die [DataInterest-Eigenschaft](/previous-versions/ms824752(v=msdn.10)) implementieren. In diesem Fall ist das Plug-In daran interessiert, auf die Benachrichtigungen `StylusDown` , , und zu `Packets` `StylusUp` `Error` reagieren. Das Beispiel gibt diese Werte zurück, wie in der [DataInterestMask-Enumeration](/previous-versions/ms824787(v=msdn.10)) definiert. Die [StylusDown-Methode](/previous-versions/ms824761(v=msdn.10)) wird aufgerufen, wenn die Stiftspitze die Digitizeroberfläche kontaktiert. Die [StylusUp-Methode](/previous-versions/ms824764(v=msdn.10)) wird aufgerufen, wenn die Stiftspitze die Digitizeroberfläche verlässt. Die [Packets-Methode](/previous-versions/ms824756(v=msdn.10)) wird aufgerufen, wenn das [**RealTimeStylus-Objekt**](realtimestylus-class.md) Pakete empfängt. Die [Error-Methode](/previous-versions/ms585069(v=vs.100)) wird aufgerufen, wenn das aktuelle Plug-In oder ein vorheriges Plug-In eine Ausnahme auslöst.


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



Die `PacketFilterPlugin` -Klasse verarbeitet die meisten dieser Benachrichtigungen in einer Hilfsmethode, `ModifyPacketData` . Die `ModifyPacketData` -Methode ruft die x- und y-Werte für jedes neue Paket aus der [PacketsData-Klasse](/previous-versions/ms824590(v=msdn.10)) ab. Wenn sich einer der Werte außerhalb des Rechtecks befindet, ersetzt die -Methode den Wert durch den nächstgelegenen Punkt, der weiterhin innerhalb des Rechtecks liegt. Dies ist ein Beispiel dafür, wie ein Plug-In Paketdaten ersetzen kann, wenn sie vom Stifteingabestream empfangen werden.


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



## <a name="custom-dynamic-renderer-plug-in"></a>Benutzerdefiniertes Dynamisches Renderer-Plug-In

Die `CustomDynamicRenderer` -Klasse implementiert auch die [**IStylusSyncPlugin-Klasse,**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) um Stifteingabebenachrichtigungen zu empfangen. Anschließend wird die Benachrichtigung verarbeitet, um einen kleinen Kreis um `Packets` jeden neuen Paketpunkt zu zeichnen.

Die -Klasse enthält eine [Graphics-Variable,](/dotnet/api/system.drawing.graphics?view=dotnet-plat-ext-3.1&preserve-view=true) die einen Verweis auf das Grafikobjekt enthält, das an den Klassenkonstruktor übergeben wird. Dies ist das Grafikobjekt, das für dynamisches Rendering verwendet wird.


```C++
private Graphics myGraphics;

public CustomDynamicRendererPlugin(Graphics g)
{
    myGraphics = g;
}
        //...
            
```



Wenn das benutzerdefinierte dynamische Renderer-Plug-In eine Paketbenachrichtigung empfängt, extrahiert es die (x,y)-Daten und zeichnet einen kleinen grünen Kreis um den Punkt. Dies ist ein Beispiel für benutzerdefiniertes Rendering, das auf dem Stifteingabestream basiert.


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



## <a name="the-realtimestyluspluginapp-project"></a>Die RealTimeStylusPluginApp-Project

Das RealTimeStylusPluginApp-Projekt veranschaulicht die zuvor beschriebenen Plug-Ins sowie die Plug-Ins [**GestureRecognizer**](gesturerecognizer-class.md) und [**DynamicRenderer.**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) Die Benutzeroberfläche des Projekts besteht aus:

-   Ein Formular, das ein [GroupBox-Steuerelement](/dotnet/api/system.windows.forms.groupbox?view=netcore-3.1) enthält, das zum Definieren des Freieingabebereichs verwendet wird.
-   Ein [CheckedListBox-Steuerelement](/dotnet/api/system.windows.forms.checkedlistbox?view=netcore-3.1) zum Auflisten und Auswählen der verfügbaren Plug-Ins.
-   Ein Paar von [Button-Objekten,](/dotnet/api/system.windows.forms.button?view=netcore-3.1) um die Neubestellung der Plug-Ins zu ermöglichen.

Das Projekt definiert eine -Struktur, , um die Verwaltung der im Projekt `PlugInListItem` verwendeten Plug-Ins zu vereinfachen. Die `PlugInListItem` -Struktur enthält das Plug-In und eine Beschreibung.

Die `RealTimeStylusPluginApp` Klasse selbst implementiert die [**IStylusAsyncPlugin-Klasse.**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) Dies ist erforderlich, damit die Klasse benachrichtigt werden kann, wenn das `RealTimeStylusPluginApp` [**GestureRecognizer-Plug-In**](gesturerecognizer-class.md) Gestendaten zur Ausgabewarteschlange hinzufügt. Die Anwendung registriert sich für die Benachrichtigung [von CustomStylusDataAdded.](/previous-versions/ms824753(v=msdn.10)) Wenn Gestendaten empfangen werden, platziert eine Beschreibung davon auf der `RealTimeStylusPluginApp` Statusleiste am unteren Rand des Formulars.


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
> In der [CustomStylusDataAdded-Implementierung](/previous-versions/ms824753(v=msdn.10)) ist es interessant, dass Sie die benutzerdefinierten Gestendaten in der Ausgabewarteschlange entweder anhand der GUID (mithilfe des [Felds GestureRecognitionDataGuid)](/previous-versions/ms826344(v=msdn.10)) oder nach Typ (mithilfe des Ergebnisses aus der as-Anweisung) identifizieren können. Im Beispiel werden beide Identifikationstechniken zu Demonstrationszwecken verwendet. Beide Ansätze allein sind ebenfalls gültig.

 

Im Load-Ereignishandler des Formulars erstellt die Anwendung Instanzen der -Klasse und der -Klasse und fügt `PacketFilter` `CustomDynamicRenderer` sie dem Listenfeld hinzu. Die Anwendung versucht dann, eine Instanz der [**GestureRecognizer-Klasse**](gesturerecognizer-class.md) zu erstellen, und fügt sie bei Erfolg dem Listenfeld hinzu. Dies schlägt fehl, wenn die Gestenerkennung auf dem System nicht vorhanden ist. Als Nächstes instanziiert die Anwendung ein [**DynamicRenderer-Objekt**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) und fügt es dem Listenfeld hinzu. Schließlich aktiviert die Anwendung jedes der Plug-Ins und das [**RealTimeStylus-Objekt**](realtimestylus-class.md) selbst.

Ein weiterer wichtiger Aspekt des Beispiels ist, dass das [**RealTimeStylus-Objekt**](realtimestylus-class.md) in den Hilfsmethoden zuerst deaktiviert wird, bevor Plug-Ins hinzugefügt oder entfernt und dann wieder aktiviert werden, nachdem das Additions- oder Entfernungs-Objekt abgeschlossen ist.


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

[Microsoft.StylusInput.DynamicRenderer](/previous-versions/ms575176(v=vs.100))
</dt> <dt>

[Microsoft.StylusInput.GestureRecognizer](/previous-versions/ms826046(v=msdn.10))
</dt> <dt>

[Microsoft.StylusInput.RealTimeStylus](/previous-versions/ms824830(v=msdn.10))
</dt> <dt>

[Microsoft.StylusInput.DataInterestMask](/previous-versions/ms575174(v=vs.100))
</dt> <dt>

[Microsoft.StylusInput.IStylusSyncPlugin](/previous-versions/ms824751(v=msdn.10))
</dt> <dt>

[Microsoft.StylusInput.IStylusAsyncPlugin](/previous-versions/ms824768(v=msdn.10))
</dt> <dt>

[Microsoft.StylusInput.PluginData.PacketsData](/previous-versions/ms575281(v=vs.100))
</dt> <dt>

[Zugreifen auf und Bearbeiten von Stifteingaben](accessing-and-manipulating-stylus-input.md)
</dt> <dt>

[Plug-Ins und die RealTimeStylus-Klasse](plug-ins-and-the-realtimestylus-class.md)
</dt> <dt>

[RealTimeStylus Ink Collection Sample](realtimestylus-ink-collection-sample.md)
</dt> </dl>

 

 
