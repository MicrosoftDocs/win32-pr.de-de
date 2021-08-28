---
description: In diesem Thema werden die Ink Analysis-APIs vorgestellt.
ms.assetid: a3126930-2802-43c7-9e98-3a73498ac3f5
title: Grundlegende Erkennung und Ink-Analyse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c4bdfa0d93c25e397caf0f116f0f47b303e9571d342825673572011534404de
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120111325"
---
# <a name="basic-recognition-and-ink-analysis"></a>Grundlegende Erkennung und Ink-Analyse

In diesem Thema werden die Ink Analysis-APIs vorgestellt.

## <a name="simple-recognition"></a>Einfache Erkennung

Die grundlegende Funktionalität, die von der Freihandanalyse-API verfügbar gemacht wird, ist der Zugriff auf die Erkennungsergebnisse für einen bestimmten Freihandteil. Dies ist einfach und einfach, wie im folgenden Beispielcode gezeigt.


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



Die Ergebnisse des Erkennungsvorgangs sind einfach ein Zeichenfolgenwert, der den erkannten Wert der handschriftlichen Ink darstellt. Die Freihandanalyse-API stellt viel mehr Erkennungsfunktionen bereit als nur die erkannte Zeichenfolge, aber dies ist der gängigste Vorgang.

## <a name="incremental-recognition"></a>Inkrementelle Erkennung

Der Erkennungsprozess nimmt Zeit in Anspruch und blockiert den Zugriff auf die Anwendung, indem der UI-Thread der Anwendung blockiert wird. Daher kann es für den Endbenutzer kostspielig und frustrierend sein, synchron auf Ergebnisse zu warten. Viele Tablet PC-Anwendungen erfordern die Erkennung mehrerer Ink-Zeilen, und ein inkrementeller Ansatz zum Erkennen von Strichen in einem Hintergrundthread ist die optimale Strategie. Der Vorteil eines inkrementellen Ansatzes anstelle eines Massenvorgangs besteht darin, dass er die Erkennung der Striche über einen bestimmten Zeitraum ermöglicht, sodass die Arbeit im Hintergrundthread anstatt synchron auf dem Vordergrundthread verteilt wird. Zur Unterstützung der inkrementellen Analyse verfügt das [**InkAnalyzer-Objekt**](inkanalyzer.md) über eine [**BackgroundAnalyze-Methode,**](iinkanalyzer-backgroundanalyze.md) die die Erstellung und Verwaltung eines Hintergrundthreads für die Anwendung übernimmt. **InkAnalyzer** übernimmt auch automatisch die Verwaltung, was erkannt werden muss und was bereits erkannt wurde.

Daher gibt es zwei Mechanismen zum Erzielen von Erkennungsergebnissen:

-   Die [**Analyze-Methode**](iinkanalyzer-analyze.md) (synchrone Analyse), die am besten für Folgendes geeignet ist:

    -   Kleine Mengen an Ink.
    -   Wenn Ergebnisse erforderlich sind, bevor mit dem nächsten Vorgang in der Anwendung fortgefahren wird, z. B. beim Anzeigen einer Korrekturbenutzeroberfläche.

-   Die [**BackgroundAnalyze-Methode**](iinkanalyzer-backgroundanalyze.md) (asynchrone Analyse), die am besten für Folgendes geeignet ist:

    -   Beliebige Menge an Ink.
    -   Bei Verwendung mit einem Timer, der ungefähr alle 600 Millisekunden pulsiert.

> [!Note]  
> 600 Millisekunden ist die aktuelle Empfehlung, aber diese Zeitliche Steuerung kann geändert werden, wenn weitere Tests ausstehen.

 

Um den [**BackgroundAnalyze-Vorgang**](iinkanalyzer-backgroundanalyze.md) zu verwenden, verwaltet das [**InkCollector-Objekt**](inkcollector-class.md) (oder ähnliche Objekte oder Steuerelemente wie [**RealTimeStylus**](realtimestylus-class.md) (RTS), [**InkOverlay**](inkoverlay-class.md)oder [InkCanvas](/dotnet/api/system.windows.controls.inkcanvas?view=netcore-3.1) in Windows Presentation Foundation) die Auflistung und das Rendering der Ink-Striche. Wenn **InkCollector** mit den Ink-Analyse-APIs gekoppelt ist, können Anwendungen die Erkennungsergebnisse aktualisieren, indem [**sie den InkAnalyzer**](inkanalyzer.md) über jeden neuen Strich informieren, der der Anwendung hinzugefügt wird. Dadurch kann **InkAnalyzer** die Striche inkrementell und in einem Hintergrundthread erkennen.

Um inkrementelle Hintergrundanalysen durchzuführen, müssen Anwendungen drei Schritte implementieren (für verwalteten Code dargestellt):

1. Fügen Sie den Strich dem [**InkAnalyzer**](inkanalyzer.md) hinzu, wenn das [**Stroke-Ereignis**](inkoverlay-stroke.md) des [**InkOverlay-Objekts**](inkoverlay-class.md) ausgelöst wird:


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



2. Rufen Sie die [**BackgroundAnalyze-Vorgänge**](iinkanalyzer-backgroundanalyze.md) in einem festgelegten Intervall auf.


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
> Hinweis Anwendungen sollten nicht einfach den Hintergrundanalysevorgang nach jedem neuen Strich aufrufen. Dies schlägt fehl (und gibt den Wert **false** zurück), wenn bereits ein Hintergrundvorgang ausgeführt wird. Der Grund für dieses Verhalten ist die Beschränkung der Anzahl der erforderlichen Hintergrundthreads und Abstimmungsvorgänge.

 

3. Lauschen Sie auf das [ResultsUpdated-Ereignis](/previous-versions/ms567607(v=vs.100)) (verwalteter Code) oder [**das Results-Ereignis**](-ianalysisevents-results.md) (C++-Code), um zu bestimmen, wann der Hintergrundprozess abgeschlossen wurde:


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



Nachdem die Verarbeitung der Ink-Funktion nun in einem Hintergrundthread erfolgt, kann die Anwendung Änderungen an der Ink akzeptieren, während der Hintergrundvorgang funktioniert. Wenn wir einen synchronen Thread verwenden, ist dies nicht möglich. Die Arbeit wird im UI-Thread ausgeführt und blockiert die Möglichkeit, Änderungen vorzunehmen. Zu den Änderungen gehören das Hinzufügen weiterer Ink-Dateien zum Dokument, das Löschen von Ink oder das Transformieren des Speicherorts oder der Darstellung der vorhandenen Ink. Änderungen, die während des Hintergrundvorgangs auftreten, können die Ergebnisse ungültig werden. Wenn Sie beispielsweise einen Strich aus einem Wort löschen, ändert sich der Erkennungswert dieses Worts. Die [**InkAnalyzer-API**](inkanalyzer.md) verfügt über einen integrierten Abstimmungsprozess, der automatisch bestimmt, welche Teile des Hintergrundvorgangs ungültig werden, wenn sich die Ink während der Analyse ändert.

Der automatische Abstimmungsprozess wird aufgrund von drei Faktoren durchgeführt:

1.  Die [**DirtyRegion-Eigenschaft.**](iinkanalyzer-getdirtyregion.md)

    -   Jedes Mal, wenn die Anwendung einen Strich zu oder aus der [**InkAnalyzer-Methode**](inkanalyzer.md)hinzufügt ([**AddStroke-Methode)**](iinkanalyzer-addstroke.md) oder entfernt ([**RemoveStroke-Methode),**](iinkanalyzer-removestroke.md) wird die physische Position des Strichs erfasst, und beim nächsten Aufruf eines Analysevorgangs stellt **inkAnalyzer** sicher, dass der Strich oder der von diesem Strich belegte Bereich analysiert wird.
    -   Wenn die Anwendung vorhandene Ink ändert, die Position ändert oder andere Zeichnungsattribute der Ink-Eigenschaft ändert, kann der Speicherort der Änderung (die Begrenzungen der Ink) der [**DirtyRegion-Eigenschaft**](iinkanalyzer-getdirtyregion.md) von [**InkAnalyzer**](inkanalyzer.md)hinzugefügt werden. Dadurch wird sichergestellt, dass diese Bereiche beim nächsten Start des Analysevorgangs durch die Anwendung auf korrekte Ergebnisse überprüft werden.
    -   Daher verfolgt die [**DirtyRegion-Eigenschaft**](iinkanalyzer-getdirtyregion.md) zwischen den Analyseläufen, welche Bereiche des Dokuments und welche Striche überprüft werden müssen, um die richtigen Ergebnisse der Ink-Analyse und Erkennung zu erhalten.

2.  Eingeschränkte Analyse.

    -   Jedes Mal, wenn die Anwendung den Analysevorgang aufruft, identifiziert die [**DirtyRegion-Eigenschaft,**](iinkanalyzer-getdirtyregion.md) welche Striche analysiert werden müssen. Dies ermöglicht es dem Analysevorgang, den Vorgang auf die geänderten Regionen zu beschränken und alle anderen Regionen zu ignorieren, wodurch der Zeitaufwand für die erneute Analyse von Ink optimiert wird.
    -   [**InkAnalyzer**](inkanalyzer.md) ignoriert nicht alle anderen Regionen auf der Seite vollständig, sondern untersucht stattdessen benachbarte Bereiche, um zu ermitteln, ob sich die änderungen an der geänderten Region auf diese benachbarten Regionen auswirken. Beispielsweise klassifiziert das Analyseprogramm "Is" im folgenden Freihandbeispiel als einzelnen **InkWord-Typ** der [**ContextNode-Klasse:**](icontextnode.md)

![handgeschriebenes "is"](images/b0e45d31-a0e5-4157-a345-a3a32de2566e.jpg)

Das Löschen der "s" führt zu einem geänderten Bereich (mit einem roten Feld gekennzeichnet).

![handschriftliches "i"](images/272a25a7-c730-40e6-b7d8-214ccbb85569.jpg)

Nach der Analyse ändert das Analyseprogramm die Klassifizierung für das "I" in einen **InkDrawing-Typ,** obwohl er sich außerhalb des geänderten Bereichs befindet, da das Freihandanalysegerät ohne den unterstützenden "s"-Strich eine Wahrscheinlichkeit von 50/50 hat, dass die Freihand als Zeichnung oder Wort klassifiziert wird.

-   Intern zwischengespeicherter Zustand.

    -   Wenn eine Anwendung einen Hintergrundanalysevorgang aufruft, speichert [**InkAnalyzer**](inkanalyzer.md) eine Momentaufnahme der gelöschten Daten zwischen. Durch das Erstellen einer Momentaufnahme kann **InkAnalyzer** die Daten unabhängig von den von der Anwendung verwendeten Daten analysieren oder die Momentaufnahme als Vergleichspunkt verwenden, um zu bestimmen, welche Änderungen von der Anwendung während der Hintergrundanalyse vorgenommen wurden.
    -   Das Zwischenspeichern des Zustands und das Vergleichen von Änderungen ist besser, als eine Liste aller Änderungen zu speichern, die aus einem der wichtigsten Gründe aufgetreten sind: dem Datenproxy. Dies ist ein erweitertes Szenario, das weiter unten in diesem Dokument beschrieben wird. Es umfasst jedoch die Anwendung, die [**InkAnalyzer**](inkanalyzer.md) vor dem aufgerufenen Analysevorgang und vor der Verarbeitung der Ergebnisse eines Analysevorgangs nur mit den aktuellen Ink- und Nicht-Ink-Daten aktualisiert.

## <a name="simple-ink-analysis"></a>Einfache Ink-Analyse

In den beiden vorherigen Szenarien (einfache Erkennung und inkrementelle Erkennung) wird beschrieben, wie auf Erkennungswerte zugegriffen wird, aber nicht erwähnt, wie auf die Ink-Analyse- oder Klassifizierungsergebnisse zugegriffen wird. Die Standardkonfiguration von [**InkAnalyzer**](inkanalyzer.md)führt sowohl Ink-Analysealgorithmen als auch Erkennungsalgorithmen aus. Diese Konfiguration liefert die genauesten Ergebnisse, da die beiden Technologien zusammenarbeiten, um die Genauigkeit zu erhöhen. Das heißt, die Ink-Analyse-Engines tragen dazu bei, das Zeichnen vom Schreiben zu trennen und das gewinkelte Schreiben in eine horizontale Ebene zu normalisieren. Dies ist die optimale Eingabeebene für die Erkennungs-Engines.

Um auf die Ergebnisse der Ink-Analyse zuzugreifen, verwendet Ihre Anwendung die [**Analyze-**](iinkanalyzer-analyze.md) oder [**BackgroundAnalyze-Methoden**](iinkanalyzer-backgroundanalyze.md) genau wie in den vorherigen beiden Erkennungsszenarien beschrieben. Nichts ändert sich, da die Ink-Analyse- und Erkennungsalgorithmen bereits ausgeführt werden, wenn diese Methoden aufgerufen werden. Der Zugriff auf die Ergebnisse ist jedoch komplizierter als das Lesen des Werts einer Zeichenfolge. Als Beispiel zeigt das folgende Codebeispiel die Gruppierung und Positionen aller **InkWord-Segmente** und **InkDrawing-Segmente,** indem ein Rechteck um die Gruppe von Strichen gerendert wird, die die Klassifizierung bilden.

In diesem Beispiel wird einfach das **Paint-Ereignis** des Formulars verwendet, um farbige Rechtecke um die Wörter oder Zeichnungen zu rendern. Die [**FindNodesOfType-Methode**](iinkanalyzer-findnodesoftype.md) gibt eine Auflistung von -Objekten zurück, die nur vorhanden sind, wenn der Analysevorgang ausgeführt wurde und die Ergebnisse Klassifizierungen mit dem angegebenen [**ContextNode-Typ**](icontextnode.md) enthalten. Wenn im Dokument kein **ContextNode** des gewünschten Typs vorhanden ist, werden die Schritte zum Zeichnen der Rechtecke übersprungen.

Jedes von der [**FindNodesOfType-Methode**](iinkanalyzer-findnodesoftype.md) zurückgegebene Objekt verfügt über Eigenschaften, die sich auf diese Art von Klassifizierung beziehen. **InkWordNode** verweist beispielsweise auf alle Striche, die ein einzelnes Wort im Dokument bilden, und verweist auf die erkannte Zeichenfolge für dieses Wort. **InkDrawingNode** verweist auf alle Striche, die die einzelne Zeichnung im Dokument bilden, und verweist auf den Formnamen für diese Zeichnung.

Die [**FindNodesOfType-Methode**](iinkanalyzer-findnodesoftype.md) ähnelt der [**DivisionResult::ResultByType-Methode,**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-resultbytype) die Auflistungen von [**DivisionUnits**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionunits) von Schreib- oder Zeichnungstypen zurückgegeben hat.


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



Betrachten Sie das folgende Freihandbeispiel, um das vorherige Codebeispiel zu betrachten:

![Ink-Beispiel "This is some ink". mit einem Kreis darunter](images/f11cc578-d2eb-4246-af77-6bc768b0b91c.jpg)

Wenn Sie die [**FindNodesOfType-Methode**](iinkanalyzer-findnodesoftype.md) aufrufen und das statische Feld für **InkWord** übergeben, gibt das Analyseprogramm eine Auflistung von vier **InkWordNode-Objekten** zurück:

![Ausgabe des Analysetools: "This is some ink"](images/16ae768a-d97c-494e-9e3d-16bce1bcb432.jpg)

Wenn Sie die [**FindNodesOfType-Methode**](iinkanalyzer-findnodesoftype.md) aufrufen und das statische Feld für **InkDrawing** übergeben, gibt das Analyseprogramm eine Auflistung eines **InkDrawingNode-Objekts** zurück:

![Abbildung von "oval", dem Ergebnis des Inkdrawing-Analysetools](images/624b6a53-b6b9-4ccf-9bb8-c4c5629b88cf.jpg)

Nachdem das **Paint** Ausgelöst wurde, rendert der Beispielcode Rechtecke um jedes der -Objekte:

![Ursprüngliches Zeichnen mit Rechtecke, die um das Objekt und die Wörter gerendert werden](images/7fd9bcc3-8d7c-4cab-aa36-ba5ed78a25c0.jpg)

Dieses Beispiel betrifft nur die [**FindNodesOfType-Methode.**](iinkanalyzer-findnodesoftype.md) Da die Ink-Analyse-Engines jedoch einen umfangreicheren Satz von Ink-Typen erkennen können, entspricht die Methode auch allen Knotentypen, die von den Ink-Analyse-Engines erkannt werden können (z. B. Linien, Absätze und andere Strukturen).

## <a name="using-ink-analysis-with-point-erase"></a>Verwenden der Ink-Analyse mit Punktlöschung

Ihre Anwendung muss Anpassungen an der Art und Weise vornehmen, wie sie Striche aktualisiert, wenn ein Punkt gelöscht wird, um eine gute Leistung sicherzustellen. Ersetzen Sie zunächst auf der Anwendungsschicht den Stiftpunkt des vorhandenen Strichs durch den Stiftpunkt des neuen Strichs, rufen Sie dann [**ClearStrokeData**](iinkanalyzer-clearstrokedata.md) für diesen Strich auf, und aktualisieren Sie den geänderten Bereich mit den Grenzen des Strichs. Dies führt dazu, dass [**InkAnalyzer**](inkanalyzer.md) die aktualisierten Strichdaten abruft, wenn die nächste Runde der Hintergrundanalyse beginnt. Dieses Verfahren wird im folgenden Beispiel veranschaulicht.


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

[Übersicht über die Ink-Analyse](ink-analysis-overview.md)
</dt> <dt>

[Nutzung der Ink-Analyse-API](ink-analysis-api-usage.md)
</dt> </dl>

 

 
