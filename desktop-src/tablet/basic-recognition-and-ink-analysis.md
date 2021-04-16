---
description: In diesem Thema werden die frei Hand Analyse-APIs vorgestellt.
ms.assetid: a3126930-2802-43c7-9e98-3a73498ac3f5
title: Grundlegende Erkennungs-und Handschrift Analyse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9858ceedba245a733d4dc0055dd0747507654f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393241"
---
# <a name="basic-recognition-and-ink-analysis"></a>Grundlegende Erkennungs-und Handschrift Analyse

In diesem Thema werden die frei Hand Analyse-APIs vorgestellt.

## <a name="simple-recognition"></a>Einfache Erkennung

Die grundlegende Funktionalität, die von der frei Hand Analyse-API verfügbar gemacht wird, ist der Zugriff auf die Erkennungsergebnisse für eine bestimmte Freihand. Dies ist unkompliziert und einfach, wie im folgenden Beispielcode gezeigt.


```C++
// Instantiate a new InkAnalyzer object, passing in an Ink object and
// the synchronizing object.
InkAnalyzer ia = new InkAnalyzer(myInkOverlay.Ink, this);

// Associate the Strokes to be recognized with the InkAnalyzer.
ia.AddStrokes(myInkOverlay.Ink.Strokes);

// Synchronously recognize the Strokes.
ia.Analyze();

// Access the results and display.
string myResults = ia.GetRecognizedString();
MessageBox.Show(myResults);
```



Bei den Ergebnissen des Erkennungs Vorgangs handelt es sich einfach um einen Zeichen folgen Wert, der den erkannten Wert des handschriftlichen frei Hand Zeichens darstellt. Die frei Hand Analyse-API macht viel mehr Erkennungsfunktionen als nur die erkannte Zeichenfolge, aber dies ist der häufigste Vorgang.

## <a name="incremental-recognition"></a>Krementelle Erkennung

Der Erkennungsprozess dauert eine Weile und blockiert den Zugriff auf die Anwendung, indem der UI-Thread der Anwendung blockiert wird. Daher kann es teuer und frustrierend sein, dass der Endbenutzer synchron auf Ergebnisse wartet. Viele Tablet PC-Anwendungen erfordern das Erkennen von mehr als wenigen Zeilen Freihand, und ein inkrementeller Ansatz zum Erkennen von Strichen in einem Hintergrund Thread ist die optimale Strategie. Der Vorteil eines inkrementellen Ansatzes anstelle eines Massen Vorgangs besteht darin, dass es die Erkennung der Striche über einen Zeitraum hinweg ermöglicht, wobei die Arbeit im Hintergrund Thread statt synchron im Vordergrund Thread verteilt wird. Um die inkrementelle Analyse zu unterstützen, verfügt das [**InkAnalyzer**](inkanalyzer.md) -Objekt über eine [**BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) -Methode, die die Erstellung und Verwaltung eines Hintergrundthreads für die Anwendung behandelt. Der **InkAnalyzer** übernimmt auch automatisch die Verwaltung der erkannten und bereits erkannten Anforderungen.

Daher gibt es zwei Mechanismen zum Erreichen von Erkennungs Ergebnissen:

-   Die [**Analyse**](iinkanalyzer-analyze.md) Methode (synchrone Analyse), die am besten für Folgendes funktioniert:

    -   Kleine Menge an frei Hand Eingaben.
    -   Wenn Ergebnisse erforderlich sind, bevor mit dem nächsten Vorgang in der Anwendung fortgefahren wird, z. b. Wenn eine Korrektur Benutzeroberfläche angezeigt wird.

-   Die [**BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) -Methode (asynchrone Analyse), die am besten für Folgendes funktioniert:

    -   Eine beliebige Menge an frei Hand Eingaben.
    -   Bei Verwendung eines Zeit Geber-Pulas ungefähr alle 600 Millisekunden.

> [!Note]  
> 600 Millisekunden ist die aktuelle Empfehlung. diese zeitliche Steuerung unterliegt jedoch Änderungen, die noch weiter getestet werden müssen.

 

Um den [**BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) -Vorgang zu verwenden, verwaltet das [**InkCollector**](inkcollector-class.md) -Objekt (oder ähnliche Objekte oder Steuerelemente wie das [**RealTimeStylus**](realtimestylus-class.md) (RTS), [**InkOverlay**](inkoverlay-class.md)oder [InkCanvas](/dotnet/api/system.windows.controls.inkcanvas?view=netcore-3.1) in Windows Presentation Foundation) die Erfassung und das Rendering der Hand Striche. Wenn **InkCollector** mit den frei Hand Analyse-APIs gekoppelt ist, können Anwendungen die Erkennungsergebnisse aktualisieren, indem Sie den [**InkAnalyzer**](inkanalyzer.md) über jeden neuen, der Anwendung hinzugefügten Strich informieren. Dadurch kann der **InkAnalyzer** die Striche inkrementell und in einem Hintergrund Thread erkennen.

Um inkrementelle Hintergrundanalysen durchzuführen, müssen Anwendungen drei Schritte implementieren (für verwalteten Code angezeigt):

1. Fügen Sie den Strich immer dann dem [**InkAnalyzer**](inkanalyzer.md) hinzu, wenn das [**Stroke**](inkoverlay-stroke.md) -Ereignis des [**InkOverlay**](inkoverlay-class.md) -Objekts ausgelöst wird:


```C++
/// Event Handler from InkOverlay's Stroke event
/// This event is fired when a new stroke is drawn. 
/// In this case, it is necessary to update the ink analyzer's 
/// Strokes collection. The event is fired even when the eraser 
/// stroke is created.
/// The event handler must filter out the eraser strokes.
/// <param name="sender">The control that raised the event.</param>
/// <param name="e">The event arguments.</param>
private void myInkOverlay_Stroke(object sender, InkCollectorStrokeEventArgs e)
{
        // Add the new stroke to the InkAnalyzer's stroke collection
        theInkAnalyzer.AddStroke(e.Stroke);
        this.Refresh();
}
```



2. Aufrufen von [**BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) -Vorgängen in einem festgelegten Intervall.


```C++
//Setup a timer tick handler
private System.Windows.Forms.Timer analysisTimer;
analysisTimer = new Timer();
analysisTimer.Tick += new System.EventHandler(this.analysisTimer_Tick);

// The timer is enabled and set to tick every 600 milliseconds.
analysisTimer.Enabled = true;
analysisTimer.Interval = 600;
// ...
//The background analysis operation is invoked with every tick
private void analysisTimer_Tick(object sender, System.EventArgs e)
{
    theInkAnalyzer.BackgroundAnalyze();
}
```



> [!Note]  
> Hinweis Anwendungen sollten nicht einfach den Hintergrundanalyse Vorgang nach jedem neuen Strich aufrufen. Dies schlägt fehl (gibt den Wert **false** zurück), wenn bereits ein Hintergrund Vorgang ausgeführt wird. Der Grund für dieses Verhalten besteht darin, die Anzahl der erforderlichen Hintergrundthreads und Abstimmungs Vorgänge einzuschränken.

 

3. Lauschen Sie auf das [resultsupveralteten](/previous-versions/ms567607(v=vs.100)) -Ereignis (verwalteter Code) oder das [**Ergebnis**](-ianalysisevents-results.md) Ereignis (C++-Code), um zu bestimmen, wann der Hintergrundprozess abgeschlossen wurde:


```C++
// ...
theInkAnalyzer.Results += new ResultsEventHandler(ia_Results);
// ...

private void ia_Results(object sender, ResultsEventArgs e)
{
    String myResults = e.InkAnalyzer.GetRecognizedString();
    MessageBox.Show(myResults);
}
```



Nun, da die Verarbeitung der frei Hand Eingaben in einem Hintergrund Thread erfolgt, kann die Anwendung Änderungen an der frei Hand Eingabe annehmen, während der Hintergrund Vorgang funktioniert. Wenn wir einen synchronen Thread verwenden, ist dies nicht möglich. Die Arbeit wird im UI-Thread ausgeführt, was die Fähigkeit zum vornehmen von Änderungen blockiert. Zu den Änderungen gehören das Hinzufügen von mehr Freihand zum Dokument, das Löschen von frei Hand Eingaben oder das Transformieren der Position oder Darstellung der vorhandenen frei Hand Eingabe Bei Änderungen, die während des Hintergrund Vorgangs auftreten, werden die Ergebnisse möglicherweise ungültig. Wenn Sie z. b. einen Strich aus einem Wort löschen, wird der Erkennungswert dieses Worts geändert. Die [**InkAnalyzer**](inkanalyzer.md) -API verfügt über einen integrierten Abstimmungsprozess, der automatisch bestimmt, welche Teile des Hintergrund Vorgangs ungültig werden, wenn das Ergebnis der frei Hand Eingaben während der Analyse geändert wird.

Der automatische Abstimmungs Vorgang wird aufgrund von drei Faktoren durchgeführt:

1.  Die [**DirtyRegion**](iinkanalyzer-getdirtyregion.md) -Eigenschaft.

    -   Jedes Mal, wenn die Anwendung ([**AddStroke**](iinkanalyzer-addstroke.md) [**-Methode)**](iinkanalyzer-removestroke.md) einen Strich zum oder aus dem [**InkAnalyzer**](inkanalyzer.md)hinzufügt, wird der physische Speicherort des Strichs aufgezeichnet, und beim nächsten Aufrufen eines Analyse Vorgangs wird vom **InkAnalyzer** sichergestellt, dass der Strich bzw. der von diesem Strich belegte Bereich analysiert wird.
    -   Wenn die Anwendung vorhandene frei Hand Eingaben ändert, den Speicherort ändert oder andere Zeichnungs Attribute der frei Hand Eingabe ändert, kann der Speicherort der Änderung (die Begrenzungen der frei Hand Eingabe) der [**DirtyRegion**](iinkanalyzer-getdirtyregion.md) -Eigenschaft des [**InkAnalyzer**](inkanalyzer.md)-Objekts hinzugefügt werden. Dadurch wird sichergestellt, dass die Bereiche beim nächsten Start des Analyse Vorgangs auf richtige Ergebnisse geprüft werden.
    -   Daher verfolgt die [**DirtyRegion**](iinkanalyzer-getdirtyregion.md) -Eigenschaft zwischen Analyse Ausführungen, welche Bereiche des Dokuments und welche Striche geprüft werden müssen, um die korrekte Handschrift Analyse und die Erkennungsergebnisse zu überprüfen.

2.  Eingeschränkte Analyse.

    -   Jedes Mal, wenn die Anwendung den Analyse Vorgang aufruft, identifiziert die [**DirtyRegion**](iinkanalyzer-getdirtyregion.md) -Eigenschaft, welche Striche analysiert werden müssen. Dadurch kann der Vorgang durch den Analyse Vorgang auf die geänderten Bereiche beschränkt werden, und alle anderen Regionen werden ignoriert, und es wird der Zeitaufwand für die erneute Analyse von frei Hand Eingaben optimiert.
    -   Der [**InkAnalyzer**](inkanalyzer.md) ignoriert nicht vollständig alle anderen Bereiche auf der Seite, sondern kann stattdessen benachbarte Bereiche überprüfen, um festzustellen, ob sich die Änderungen, die in der geänderten Region vorgenommen wurden, auf diese benachbarten Regionen auswirken. Beispielsweise klassifiziert der Analyzer "is" im folgenden Ink-Beispiel als einzelnen **InkWord** -Typ der [**ContextNode**](icontextnode.md) -Klasse:

!["ist" Hand geschrieben](images/b0e45d31-a0e5-4157-a345-a3a32de2566e.jpg)

Das Löschen der "s" führt zu einem geänderten Bereich (markiert mit einem roten Feld).

![Handgeschriebenes "i"](images/272a25a7-c730-40e6-b7d8-214ccbb85569.jpg)

Nach der Analyse ändert der Analyzer die Klassifizierung für das "I" in einen **inkzeichentyp** , auch wenn er sich außerhalb des geänderten Bereichs befindet, denn ohne den unterstützenden "s"-Strich hat der Ink Analyzer eine 50/50-Wahrscheinlichkeit, dass die frei Hand Eingaben als Zeichen oder Wort klassifiziert werden.

-   Intern zwischen gespeicherter Zustand.

    -   Wenn eine Anwendung einen Hintergrundanalyse Vorgang aufruft, speichert der [**InkAnalyzer**](inkanalyzer.md) eine Momentaufnahme der aufgeschnittenen Daten zwischen. Wenn Sie eine Momentaufnahme erstellen, kann der **InkAnalyzer** entweder daran arbeiten, die Daten unabhängig von den Daten zu analysieren, die von der Anwendung verwendet werden, oder die Momentaufnahme als Vergleichspunkt verwenden, um zu bestimmen, welche Änderungen von der Anwendung während der Hintergrundanalyse vorgenommen wurden.
    -   Das Zwischenspeichern des Zustands und das Vergleichen von Änderungen ist besser als das Beibehalten einer Liste aller Änderungen, die aus einem primären Grund aufgetreten sind: Daten Proxy. Dabei handelt es sich um ein erweitertes Szenario, das weiter unten in diesem Dokument beschrieben wird. Es umfasst aber auch die Anwendung, die den [**InkAnalyzer**](inkanalyzer.md) nur mit den aktuellen Freihand-und nicht-frei Hand Daten aktualisiert, bevor der aufgerufene Analyse Vorgang und die Ergebnisse eines Analyse Vorgangs verarbeitet werden.

## <a name="simple-ink-analysis"></a>Einfache Handschrift Analyse

In den beiden vorherigen Szenarien (einfache Erkennung und inkrementelle Erkennung) wird beschrieben, wie auf Erkennungswerte zugegriffen wird Die Standardkonfiguration von [**InkAnalyzer**](inkanalyzer.md)führt sowohl frei Hand Analysealgorithmen als auch Erkennungsalgorithmen aus. Diese Konfiguration ergibt die genauesten Ergebnisse, da die beiden Technologien zusammenarbeiten, um die Genauigkeit zu erhöhen. Das heißt, die frei Hand Analyse-Engines helfen dabei, die Zeichnung von der Schreibweise zu trennen und das Schreiben in eine horizontale Ebene zu normalisieren. Dies ist die optimale Eingabe Ebene für die Erkennungs-Engines.

Für den Zugriff auf die Ergebnisse der frei Hand Analyse verwendet Ihre Anwendung die Methoden " [**analysieren**](iinkanalyzer-analyze.md) " oder " [**BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) " genau wie in den vorherigen beiden Erkennungs Szenarien beschrieben. Nichts ändert sich, weil die Handschrift Analyse und Erkennungsalgorithmen bereits ausgeführt werden, wenn diese Methoden aufgerufen werden. Allerdings ist der Zugriff auf die Ergebnisse komplizierter als das Lesen des Werts einer Zeichenfolge. Im folgenden Codebeispiel werden z. b. die Gruppierung und die Speicherorte aller **InkWord** -Segmente und **InkDrawing** -Segmente veranschaulicht, indem ein Rechteck um die Gruppe der Striche gerendert wird, aus denen die Klassifizierung besteht.

Dieses Beispiel verwendet einfach das **Paint** -Ereignis des Formulars, um Farbige Rechtecke um die Wörter oder Zeichnungen zu gestalten. Die [**findnodesoft ype**](iinkanalyzer-findnodesoftype.md) -Methode gibt eine Auflistung von-Objekten zurück, die nur vorhanden ist, wenn der Analyse Vorgang ausgeführt wurde und die Ergebnisse Klassifizierungen mit dem angegebenen [**ContextNode**](icontextnode.md) -Typ enthalten. Wenn kein **ContextNode** des gewünschten Typs im Dokument vorhanden ist, werden die Schritte zum Zeichnen der Rechtecke übersprungen.

Jedes Objekt, das von der [**findnodesoft ype**](iinkanalyzer-findnodesoftype.md) -Methode zurückgegeben wird, verfügt über Eigenschaften, die sich auf diese Art von Klassifizierung beziehen. Beispielsweise verweist der **InkWordNode** auf alle Striche, die ein einzelnes Wort im Dokument bilden, und verweist auf die erkannte Zeichenfolge für dieses Wort. **InkDrawingNode** verweist auf alle Striche, die das einzelne zeichnen im Dokument bilden, und verweist auf den Namen der Form für diese Zeichnung.

Die [**findnodesoft ype**](iinkanalyzer-findnodesoftype.md) -Methode ähnelt der [**DivisionResult:: ResultByType**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-resultbytype) -Methode, die Auflistungen von [**DivisionUnits**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionunits) entweder von Schreib-oder Zeichnungs Typen zurückgegeben hat.


```C++
private void Form1_Paint(object sender, PaintEventArgs e)
{
    //Setup the pen to draw
    using(Pen penBox = new Pen(Color.Red, 1))
    {
        // Find all the InkWord ContextNodes in the results
        ContextNodeCollection InkWordNodes = theInkAnalyzer.FindNodesOfType(ContextNodeType.InkWord);
        // For each InkWord node found, cast the ContextNode to a type specific
        // "InkWordNode" to easily access the rotated bounding box property.
        foreach (ContextNode InkWord in InkWordNodes)
        {
            //Draw the rotated bounding box.
            e.Graphics.DrawPolygon(penBox,
                    ((InkWordNode)InkWord).GetRotatedBoundingBox());
        }

        // Find all the InkDrawing ContextNodes in the results
        ContextNodeBaseCollection InkDrawingNodes = theInkAnalyzer.FindNodesOfType(ContextNodeType.InkDrawing);

        penBox.Color = Color.Green;

        // For each InkDrawing node found, access the node's location property to
        // draw a rectangle around the drawing.
        foreach (ContextNode InkDrawing in InkDrawingNodes)
        {
            e.Graphics.DrawRectangle(penBox, InkDrawing.Location.GetBounds());
        }
    }
}
```



Um das vorherige Codebeispiel in die Perspektive zu versetzen, betrachten Sie das folgende Ink-Beispiel:

![Ink Sample "This is some Ink". mit einem Kreis darunter](images/f11cc578-d2eb-4246-af77-6bc768b0b91c.jpg)

Wenn Sie die [**findnodesoft ype**](iinkanalyzer-findnodesoftype.md) -Methode aufzurufen und das statische Feld für **InkWord** übergeben, gibt die Analyse eine Auflistung von vier **InkWordNode** -Objekten zurück:

![Ausgabe des Analyzers "This is some Ink"](images/16ae768a-d97c-494e-9e3d-16bce1bcb432.jpg)

Wenn Sie die [**findnodesoft ype**](iinkanalyzer-findnodesoftype.md) -Methode aufzurufen und das statische Feld für **InkDrawing** übergeben, gibt die Analyse eine Auflistung von einem **InkDrawingNode** -Objekt zurück:

![Bild, das "Oval" anzeigt, das Ergebnis des InkDrawing-Analyzers](images/624b6a53-b6b9-4ccf-9bb8-c4c5629b88cf.jpg)

Nachdem das **Paint** -Ereignis ausgelöst wurde, rendert der Beispielcode Rechtecke um jedes der-Objekte:

![ursprüngliches zeichnen mit Rechtecke um das Objekt und Wörter gerendert](images/7fd9bcc3-8d7c-4cab-aa36-ba5ed78a25c0.jpg)

In diesem Beispiel wird nur die [**findnodesoft ype**](iinkanalyzer-findnodesoftype.md) -Methode behandelt, aber da die frei Hand Analyse-Engines einen umfassenderen Satz von Freihand Typen erkennen können, entspricht die-Methode auch allen Typen von Knoten, die von den frei Hand Analysemodulen (z. b. Zeilen, Absätzen und anderen Strukturen) erkennbar sind.

## <a name="using-ink-analysis-with-point-erase"></a>Verwenden der Ink-Analyse mit Punkt Löschung

Die Anwendung muss Anpassungen bei der Aktualisierung von Strichen durchführen, um eine gute Leistung zu gewährleisten. Ersetzen Sie zunächst auf der Anwendungsebene den Tablettstiftpunkt des vorhandenen Strichs durch den Tablettstiftpunkt des neuen Strichs, und aktualisieren Sie dann [**ClearStrokeData**](iinkanalyzer-clearstrokedata.md) auf diesem Strich, und aktualisieren Sie den geänderten Bereich mit den Begrenzungen des Strichs. Dies bewirkt, dass der [**InkAnalyzer**](inkanalyzer.md) die aktualisierten hubdaten abruft, wenn die nächste Runde der Hintergrundanalyse beginnt. Dieses Verfahren wird im folgenden Beispiel veranschaulicht.


```C++
using System;
using System.Diagnostics;
using System.Windows;
using System.Windows.Controls;
using System.Windows.Ink;
using System.Windows.Input;
using System.Windows.Media;

class PointEraseAnalysisSample : Application
{
  InkAnalyzer _analyzer;
  InkCanvas _canvas;
  bool _isPointErasing = false;
  bool _strokesManipulated = false;

  protected override void OnStartup(StartupEventArgs e)
  {
      base.OnStartup(e);
      Window win = new Window();

      _canvas = new InkCanvas();
      _canvas.Background = new LinearGradientBrush(Colors.Yellow, Colors.LightYellow, 60d);
      _canvas.EditingModeInverted = InkCanvasEditingMode.EraseByPoint;
      _canvas.Strokes.StrokesChanged += new StrokeCollectionChangedEventHandler(Strokes_StrokesChanged);
      _canvas.AddHandler(InkCanvas.MouseUpEvent, new MouseButtonEventHandler(_canvas_MouseUp), true);

      _analyzer = new InkAnalyzer(this.Dispatcher);
      _analyzer.ResultsUpdated += new ResultsUpdatedEventHandler(_analyzer_ResultsUpdated);

      win.Content = _canvas;
      win.Show();
  }

  void _analyzer_ResultsUpdated(object sender, ResultsUpdatedEventArgs e)
  {
      if (!_analyzer.DirtyRegion.IsEmpty)
      {
          _analyzer.BackgroundAnalyze();
          return;
      }

      Console.WriteLine(_analyzer.GetRecognizedString());
  }

  void _canvas_MouseUp(object sender, MouseButtonEventArgs e)
  {
      if (_isPointErasing)
      {
          _isPointErasing = false;
          _analyzer.BackgroundAnalyze();
      }
  }

  void Strokes_StrokesChanged(object sender, StrokeCollectionChangedEventArgs e)
  {
      if (_strokesManipulated)
      {
          // ignore StrokesChanged if we changed them ourselves
          _strokesManipulated = false;
          return;
      }

      if (_canvas.ActiveEditingMode == InkCanvasEditingMode.EraseByPoint &&
          e.Added.Count == 1 && e.Removed.Count == 1)
      {
          // set flag so we call BackgroundAnalyze in MouseUp
          _isPointErasing = true;

          // set flag so we ignore the next StrokesChanged
          _strokesManipulated = true;

          // replace the stylus points on the removed stroke with the added stroke
          e.Removed[0].StylusPoints = e.Added[0].StylusPoints;
          
          // force IA to update the stroke data for the removed stroke
          _analyzer.ClearStrokeData(e.Removed[0]);

          // replace the added stroke with the updated removed stroke back into InkCanvas
          _canvas.Strokes.Replace(e.Added[0], new StrokeCollection(new Stroke[] {e.Removed[0]})); 
          
          return;
      }

      if (e.Added.Count > 0)
      {
          _analyzer.AddStrokes(e.Added);
      }

      if (e.Removed.Count > 0)
      {
          _analyzer.RemoveStrokes(e.Removed);
      }

      _analyzer.BackgroundAnalyze();
  }

  [STAThread]
  static void Main(string[] args)
  {
      new PointEraseAnalysisSample().Run();
  }
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Übersicht über die Link Analyse](ink-analysis-overview.md)
</dt> <dt>

[Verwendung der frei Hand Analyse-API](ink-analysis-api-usage.md)
</dt> </dl>

 

 
