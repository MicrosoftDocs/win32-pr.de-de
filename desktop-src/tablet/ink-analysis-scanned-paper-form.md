---
description: In diesem Beispiel wird gezeigt, wie die frei Hand Analyse zum Erstellen einer Formular füllenden Anwendung verwendet wird, wobei das Formular auf einem gescannten Papierformular basiert.
ms.assetid: 1eae5962-b4e0-4947-a6d2-63713a68198c
title: Papierformular für die frei Hand Analyse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e94d366c77e19bd5c32d3d1e4efa286cb3b089ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214423"
---
# <a name="ink-analysis-scanned-paper-form"></a>Papierformular für die frei Hand Analyse

In diesem Beispiel wird gezeigt, wie die frei Hand Analyse zum Erstellen einer Formular füllenden Anwendung verwendet wird, wobei das Formular auf einem gescannten Papierformular basiert.

## <a name="features-demonstrated"></a>Gezeigte Features

Diese Beispielanwendung veranschaulicht die folgenden Features der frei Hand Analyse-API und der Windows Forms Ink-Steuerelemente:

-   Ein gescanntes Papierformular wird geladen. Im Beispiel wird das Formular aus einem Bild im PNG-Format importiert.
-   Sammeln und Rendern von frei Hand Eingaben über das gescannte Formular.
-   Verwenden eines [InkAnalyzer](/previous-versions/ms583671(v=vs.100)) -Objekts zum Analysieren der Handschrift.
-   Erstellen von [AnalysisHintNode](/previous-versions/ms573018(v=vs.100)) -Objekten zur Verbesserung der Handschrift Ergebnisse.
-   Auffüllen von Textfeldern aus Analyse hinweisen.
-   Erstellen einer grundlegenden Textkorrektur.

## <a name="project-references"></a>Projektverweise

Das Beispiel ist als Windows Forms oder Windows Presentation Foundation Anwendung verfügbar. Die Verweise auf die Windows Forms-Version:

-   Microsoft.Ink.dll
-   Microsoft.Ink.Analysis.dll

Die Windows Presentation Foundation Versions Verweise IAWinFX.dll zusätzlich zu den wichtigsten Windows Presentation Foundation-DLLs.

> [!Note]  
> Die Windows Presentation Foundation Version dieses Beispiels (im XAML-Verzeichnis gefunden) erfordert, dass die Windows Presentation Foundation Erweiterungen für Microsoft Visual Studio 2005 auf dem System installiert sind.

 

## <a name="user-interface"></a>Benutzeroberfläche

Die Benutzeroberfläche für diese Anwendung besteht aus einem [TabControl](/dotnet/api/system.windows.forms.tabcontrol?view=netcore-3.1) -Objekt mit zwei zugeordneten [TabPage](/dotnet/api/system.windows.forms.tabpage?view=netcore-3.1) -Objekten: frei Hand Formular und konvertiertes Textformular. Die Registerkarte frei Hand Formular enthält

-   Ein Bereich, der ein Bild eines gescannten Papier Formulars enthält, das zum Übernehmen von Telefonnachrichten verwendet wird.
-   Ein Kontrollkästchen, bei dem die Anwendung die Grenzen des Analyse Hinweises anzeigt, wenn diese Option ausgewählt ist.
-   Ein paar von Schaltflächen, löschen und analysieren, die frei Hand Eingaben aus dem Formular löschen und die Ink-Analyse initialisieren.

Das konvertierte Textformular enthält dasselbe Bild und ist die Seite, auf der der erkannte Text von der Anwendung angezeigt wird. Wenn Sie auf analysieren klicken, führt die Anwendung die Handschrift Daten synchron aus, und die Erkennungsergebnisse werden auf der Registerkarte konvertierte Text Formulare angezeigt.

## <a name="functionality"></a>Funktionalität

Diese Anwendung verwendet ein [InkOverlay](/previous-versions/ms552322(v=vs.100)) , um Schreibvorgänge zu ermöglichen. Das InkOverlay-Objekt eignet sich gut für die Aufnahme und das einfache schreiben. Der primäre Verwendungszweck dieses Objekts besteht darin, frei Hand Eingaben als frei Hand Eingaben anzuzeigen. Die Hauptklasse für die Ink-Analyse ist die [InkAnalyzer](/previous-versions/ms583671(v=vs.100)) -Klasse. Wenn Sie die [Analyse](/previous-versions/ms568971(v=vs.100)) Methode des InkAnalyzer-Objekts aufzurufen, erfolgt die Handschrifterkennung synchron.

Die Anwendung initialisiert zwei Arrays, eine der Zeichen folgen und eine der Rechtecke. Das Zeichen folgen Array, `factoidStrings` , besteht aus [Faktoid](/previous-versions/ms583657(v=vs.100)) -Objekten, die als [AnalysisHintNode](/previous-versions/ms573018(v=vs.100)) -Objekte an den [InkAnalyzer](/previous-versions/ms583671(v=vs.100)) übermittelt werden. Die AnalysisHintNode-Objekte übertragen den InkAnalyzer in Bezug auf bestimmte Eingaben. In diesem Beispiel werden die Datums-, Uhrzeit-und Telefon Hinweise sowie einige andere verwendet.

Jeder [AnalysisHintNode](/previous-versions/ms573018(v=vs.100)) ist einem bestimmten Bereich der Form zugeordnet. Die Bereiche werden durch das Array der Rechtecke dargestellt `rects` . Wenn Sie für jedes Rechteck ein [Textfeld](/dotnet/api/system.windows.forms.textbox?view=netcore-3.1) erstellen, gibt das Beispiel den erkannten Text an der richtigen Position aus.


```C++
        private void InitHints()
        {
            // Instantiate the collection of TextBoxes.
            this.textBoxes = new ArrayList();

            // For each Rectangle in Rectangles
            for (int i = 0; i < rects.Length; i++)
            {

                Rectangle rectangle = rects[i];

                // Create an AnalysisHintNode with the bounds of the Rectangle.  The bounds
                // of an AnalysisHintNode gives clues to the handwriting recognizer about
                // the way Strokes are grouped together.
                AnalysisHintNode hint = this.analyzer.CreateAnalysisHint(rectangle);

                // Set the corresponding Factoid on the AnalysisHintNode.  This gives the 
                // recognizer clues about the meaning of the strokes within the 
                // AnalysisHintNode's region.
                hint.Factoid = factoidStrings[i];

                // Create a corresponding TextBox where the results of the analysis
                // associated with this AnalysisHintNode will be displayed.  Store the reference
                // to the TextBox in the textBoxes Collection.
                this.textBoxes.Add(InitTextBox(hint));
            }
        }
```



Danach ist es lediglich wichtig, einen Ereignishandler zu erstellen, der die Handschrift Analyse auslöst, wenn der Benutzer auf "analysieren" klickt.


```C++
        private void UpdateTextBoxes()
        {
            // Get the AnalysisHintNodes that we previously added to the InkAnalyzer.
            ContextNodeCollection hints = this.analyzer.GetAnalysisHints();

            for (int i = 0; i < hints.Count; i++)
            {
                // Get the recognized string from the AnalysisHintNode
                string analyzedString = ((AnalysisHintNode)hints[i]).GetRecognizedString();

                // If we found a string, set the contents of the TextBox
                // to that string.
                if (analyzedString != null)
                {
                    ((TextBox)this.textBoxes[i]).Text = analyzedString;
                }
            }
        }
```



 

 
