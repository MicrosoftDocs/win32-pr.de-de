---
description: In diesem Beispiel wird gezeigt, wie Sie mit der Ink-Analyse eine Anwendung zum Ausfüllen von Formularen erstellen, bei der das Formular auf einem gescannten Papierformular basiert.
ms.assetid: 1eae5962-b4e0-4947-a6d2-63713a68198c
title: Gescanntes Papierformular für die Ink-Analyse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4069efd5ba8763e00e9b3170ffb0a39a4a70c4d66d07d3c8bf08bc3688f57ed0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118718646"
---
# <a name="ink-analysis-scanned-paper-form"></a>Gescanntes Papierformular für die Ink-Analyse

In diesem Beispiel wird gezeigt, wie Sie mit der Ink-Analyse eine Anwendung zum Ausfüllen von Formularen erstellen, bei der das Formular auf einem gescannten Papierformular basiert.

## <a name="features-demonstrated"></a>Gezeigte Features

Diese Beispielanwendung veranschaulicht die folgenden Funktionen der Freihandanalyse-API und der Windows Forms-Freihandsteuerelemente:

-   Laden eines gescannten Papierformulars. Im Beispiel wird das Formular aus einem Bild im .png Format importiert.
-   Sammeln und Rendern von Ink auf dem gescannten Formular.
-   Verwenden eines [InkAnalyzer-Objekts](/previous-versions/ms583671(v=vs.100)) zum Analysieren der Handschrift.
-   Generieren von [AnalysisHintNode-Objekten](/previous-versions/ms573018(v=vs.100)) zur Verbesserung der Handschriftergebnisse.
-   Auffüllen von Textfeldern aus Analysehinweisen.
-   Erstellen einer einfachen Textkorrektur.

## <a name="project-references"></a>Projektverweise

Das Beispiel ist als Windows Forms- oder Windows Presentation Foundation-Anwendung verfügbar. Die Windows Forms-Versionsverweise:

-   Microsoft.Ink.dll
-   Microsoft.Ink.Analysis.dll

Die Windows Presentation Foundation Version verweist IAWinFX.dll zusätzlich zu den Kern-Windows Presentation Foundation-DLLs.

> [!Note]  
> Die Windows Presentation Foundation Version dieses Beispiels (im XAML-Verzeichnis zu finden) erfordert, dass die Windows Presentation Foundation-Erweiterungen für Microsoft Visual Studio 2005 auf dem System installiert sind.

 

## <a name="user-interface"></a>Benutzeroberfläche

Die Benutzeroberfläche für diese Anwendung besteht aus einem [TabControl-Objekt,](/dotnet/api/system.windows.forms.tabcontrol?view=netcore-3.1) dem zwei [TabPage-Objekte](/dotnet/api/system.windows.forms.tabpage?view=netcore-3.1) zugeordnet sind: Freihandformular und konvertiertes Textformular. Die Registerkarte "Ink Form" enthält

-   Ein Bereich, der ein Bild eines gescannten Papierformulars enthält, das für die Aufnahme von Telefonnachrichten verwendet wird.
-   Ein Kontrollkästchen, in dem die Anwendung die Begrenzungen der Analysehinweise zeigt, wenn diese ausgewählt sind.
-   Ein Paar von Schaltflächen ,Löschen und Analysieren', mit denen die Freihand aus dem Formular gelöscht und die Freihandanalyse initialisiert wird.

Das Formular für konvertierten Text enthält das gleiche Bild und ist die Seite, auf der die Anwendung den erkannten Text anzeigt. Wenn Sie auf Analysieren klicken, führt die Anwendung synchron eine Ink-Analyse durch, und die Erkennungsergebnisse werden auf der Registerkarte Konvertiertes Textformular angezeigt.

## <a name="functionality"></a>Funktionalität

Diese Anwendung verwendet [inkOverlay,](/previous-versions/ms552322(v=vs.100)) um das Schreiben zu ermöglichen. Das InkOverlay-Objekt eignet sich gut für Notizaufnahme und einfaches Scribbling. Die primäre Verwendung dieses Objekts besteht darin, Ink als Ink anzuzeigen. Die Hauptklasse für die Ink-Analyse ist die [InkAnalyzer-Klasse.](/previous-versions/ms583671(v=vs.100)) Wenn Sie die [Analyze-Methode](/previous-versions/ms568971(v=vs.100)) des InkAnalyzer-Objekts aufrufen, erfolgt die Ink-Analyse synchron.

Die Anwendung initialisiert zwei Arrays, eines von Zeichenfolgen und eines von Rechtecke. Das Zeichenfolgenarray `factoidStrings` besteht aus [Factoid-Objekten,](/previous-versions/ms583657(v=vs.100)) die als [AnalysisHintNode-Objekte](/previous-versions/ms573018(v=vs.100)) an [InkAnalyzer](/previous-versions/ms583671(v=vs.100)) übergeben werden. Die AnalysisHintNode-Objekte verzerren den InkAnalyzer auf eine bestimmte Eingabe. In diesem Beispiel werden datums-, uhrzeit- und telefon-Hinweise sowie einige andere Hinweise verwendet.

Jeder [AnalysisHintNode](/previous-versions/ms573018(v=vs.100)) ist einem bestimmten Bereich des Formulars zugeordnet. Die Bereiche werden durch das Array von Rechtecke dargestellt, `rects` . Durch Erstellen eines [TextBox-Felds](/dotnet/api/system.windows.forms.textbox?view=netcore-3.1) für jedes Rechteck gibt das Beispiel den erkannten Text an der richtigen Position aus.


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



Danach geht es lediglich darum, einen Ereignishandler zu erstellen, der die Ink-Analyse auslöst, wenn der Benutzer auf Analysieren klickt.


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



 

 
