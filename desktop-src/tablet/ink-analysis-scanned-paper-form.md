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
# <a name="ink-analysis-scanned-paper-form"></a><span data-ttu-id="d465a-103">Papierformular für die frei Hand Analyse</span><span class="sxs-lookup"><span data-stu-id="d465a-103">Ink Analysis Scanned Paper Form</span></span>

<span data-ttu-id="d465a-104">In diesem Beispiel wird gezeigt, wie die frei Hand Analyse zum Erstellen einer Formular füllenden Anwendung verwendet wird, wobei das Formular auf einem gescannten Papierformular basiert.</span><span class="sxs-lookup"><span data-stu-id="d465a-104">This sample shows how to use Ink Analysis to create a form-filling application, where the form is based on a scanned paper form.</span></span>

## <a name="features-demonstrated"></a><span data-ttu-id="d465a-105">Gezeigte Features</span><span class="sxs-lookup"><span data-stu-id="d465a-105">Features Demonstrated</span></span>

<span data-ttu-id="d465a-106">Diese Beispielanwendung veranschaulicht die folgenden Features der frei Hand Analyse-API und der Windows Forms Ink-Steuerelemente:</span><span class="sxs-lookup"><span data-stu-id="d465a-106">This sample application demonstrates the following features of the Ink Analysis API and the Windows Forms Ink Controls:</span></span>

-   <span data-ttu-id="d465a-107">Ein gescanntes Papierformular wird geladen.</span><span class="sxs-lookup"><span data-stu-id="d465a-107">Loading a scanned paper form.</span></span> <span data-ttu-id="d465a-108">Im Beispiel wird das Formular aus einem Bild im PNG-Format importiert.</span><span class="sxs-lookup"><span data-stu-id="d465a-108">The sample imports the form from an image in .png format.</span></span>
-   <span data-ttu-id="d465a-109">Sammeln und Rendern von frei Hand Eingaben über das gescannte Formular.</span><span class="sxs-lookup"><span data-stu-id="d465a-109">Collecting and rendering ink on top of the scanned form.</span></span>
-   <span data-ttu-id="d465a-110">Verwenden eines [InkAnalyzer](/previous-versions/ms583671(v=vs.100)) -Objekts zum Analysieren der Handschrift.</span><span class="sxs-lookup"><span data-stu-id="d465a-110">Using an [InkAnalyzer](/previous-versions/ms583671(v=vs.100)) object to parse handwriting.</span></span>
-   <span data-ttu-id="d465a-111">Erstellen von [AnalysisHintNode](/previous-versions/ms573018(v=vs.100)) -Objekten zur Verbesserung der Handschrift Ergebnisse.</span><span class="sxs-lookup"><span data-stu-id="d465a-111">Generating [AnalysisHintNode](/previous-versions/ms573018(v=vs.100)) objects to improve handwriting results.</span></span>
-   <span data-ttu-id="d465a-112">Auffüllen von Textfeldern aus Analyse hinweisen.</span><span class="sxs-lookup"><span data-stu-id="d465a-112">Populating text boxes from analysis hints.</span></span>
-   <span data-ttu-id="d465a-113">Erstellen einer grundlegenden Textkorrektur.</span><span class="sxs-lookup"><span data-stu-id="d465a-113">Creating a basic text correction experience.</span></span>

## <a name="project-references"></a><span data-ttu-id="d465a-114">Projektverweise</span><span class="sxs-lookup"><span data-stu-id="d465a-114">Project References</span></span>

<span data-ttu-id="d465a-115">Das Beispiel ist als Windows Forms oder Windows Presentation Foundation Anwendung verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d465a-115">The sample is available as a Windows Forms or Windows Presentation Foundation application.</span></span> <span data-ttu-id="d465a-116">Die Verweise auf die Windows Forms-Version:</span><span class="sxs-lookup"><span data-stu-id="d465a-116">The Windows Forms version references:</span></span>

-   <span data-ttu-id="d465a-117">Microsoft.Ink.dll</span><span class="sxs-lookup"><span data-stu-id="d465a-117">Microsoft.Ink.dll</span></span>
-   <span data-ttu-id="d465a-118">Microsoft.Ink.Analysis.dll</span><span class="sxs-lookup"><span data-stu-id="d465a-118">Microsoft.Ink.Analysis.dll</span></span>

<span data-ttu-id="d465a-119">Die Windows Presentation Foundation Versions Verweise IAWinFX.dll zusätzlich zu den wichtigsten Windows Presentation Foundation-DLLs.</span><span class="sxs-lookup"><span data-stu-id="d465a-119">The Windows Presentation Foundation version references IAWinFX.dll in addition to the core Windows Presentation Foundation dlls.</span></span>

> [!Note]  
> <span data-ttu-id="d465a-120">Die Windows Presentation Foundation Version dieses Beispiels (im XAML-Verzeichnis gefunden) erfordert, dass die Windows Presentation Foundation Erweiterungen für Microsoft Visual Studio 2005 auf dem System installiert sind.</span><span class="sxs-lookup"><span data-stu-id="d465a-120">The Windows Presentation Foundation version of this sample (found in the XAML directory) requires that the Windows Presentation Foundation extensions for Microsoft Visual Studio 2005 is installed on the system.</span></span>

 

## <a name="user-interface"></a><span data-ttu-id="d465a-121">Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="d465a-121">User Interface</span></span>

<span data-ttu-id="d465a-122">Die Benutzeroberfläche für diese Anwendung besteht aus einem [TabControl](/dotnet/api/system.windows.forms.tabcontrol?view=netcore-3.1) -Objekt mit zwei zugeordneten [TabPage](/dotnet/api/system.windows.forms.tabpage?view=netcore-3.1) -Objekten: frei Hand Formular und konvertiertes Textformular.</span><span class="sxs-lookup"><span data-stu-id="d465a-122">The UI for this application consists of a [TabControl](/dotnet/api/system.windows.forms.tabcontrol?view=netcore-3.1) with two [TabPage](/dotnet/api/system.windows.forms.tabpage?view=netcore-3.1) objects associated with it: Ink Form and Converted Text Form.</span></span> <span data-ttu-id="d465a-123">Die Registerkarte frei Hand Formular enthält</span><span class="sxs-lookup"><span data-stu-id="d465a-123">The Ink Form tab contains</span></span>

-   <span data-ttu-id="d465a-124">Ein Bereich, der ein Bild eines gescannten Papier Formulars enthält, das zum Übernehmen von Telefonnachrichten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d465a-124">A panel that contains an image of a scanned paper form used for taking telephone messages.</span></span>
-   <span data-ttu-id="d465a-125">Ein Kontrollkästchen, bei dem die Anwendung die Grenzen des Analyse Hinweises anzeigt, wenn diese Option ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="d465a-125">A check box that has the application show the analysis hint bounds when selected.</span></span>
-   <span data-ttu-id="d465a-126">Ein paar von Schaltflächen, löschen und analysieren, die frei Hand Eingaben aus dem Formular löschen und die Ink-Analyse initialisieren.</span><span class="sxs-lookup"><span data-stu-id="d465a-126">A pair of buttons, Clear and Analyze, that clear the ink from the form and initialize ink analysis.</span></span>

<span data-ttu-id="d465a-127">Das konvertierte Textformular enthält dasselbe Bild und ist die Seite, auf der der erkannte Text von der Anwendung angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="d465a-127">The Converted Text Form contains the same image and is the page on which the application displays the recognized text.</span></span> <span data-ttu-id="d465a-128">Wenn Sie auf analysieren klicken, führt die Anwendung die Handschrift Daten synchron aus, und die Erkennungsergebnisse werden auf der Registerkarte konvertierte Text Formulare angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d465a-128">When you click Analyze, the application performs ink analysis synchronously, and the recognition results appear on the Converted Text Form tab.</span></span>

## <a name="functionality"></a><span data-ttu-id="d465a-129">Funktionalität</span><span class="sxs-lookup"><span data-stu-id="d465a-129">Functionality</span></span>

<span data-ttu-id="d465a-130">Diese Anwendung verwendet ein [InkOverlay](/previous-versions/ms552322(v=vs.100)) , um Schreibvorgänge zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="d465a-130">This application uses an [InkOverlay](/previous-versions/ms552322(v=vs.100)) to enable writing.</span></span> <span data-ttu-id="d465a-131">Das InkOverlay-Objekt eignet sich gut für die Aufnahme und das einfache schreiben.</span><span class="sxs-lookup"><span data-stu-id="d465a-131">The InkOverlay object is well suited for note taking and basic scribbling.</span></span> <span data-ttu-id="d465a-132">Der primäre Verwendungszweck dieses Objekts besteht darin, frei Hand Eingaben als frei Hand Eingaben anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="d465a-132">The primary intended use of this object is to display ink as ink.</span></span> <span data-ttu-id="d465a-133">Die Hauptklasse für die Ink-Analyse ist die [InkAnalyzer](/previous-versions/ms583671(v=vs.100)) -Klasse.</span><span class="sxs-lookup"><span data-stu-id="d465a-133">The main class for ink analysis is the [InkAnalyzer](/previous-versions/ms583671(v=vs.100)) class.</span></span> <span data-ttu-id="d465a-134">Wenn Sie die [Analyse](/previous-versions/ms568971(v=vs.100)) Methode des InkAnalyzer-Objekts aufzurufen, erfolgt die Handschrifterkennung synchron.</span><span class="sxs-lookup"><span data-stu-id="d465a-134">When you call the InkAnalyzer object's [Analyze](/previous-versions/ms568971(v=vs.100)) method, the ink analysis occurs synchronously.</span></span>

<span data-ttu-id="d465a-135">Die Anwendung initialisiert zwei Arrays, eine der Zeichen folgen und eine der Rechtecke.</span><span class="sxs-lookup"><span data-stu-id="d465a-135">The application initializes two arrays, one of strings and one of rectangles.</span></span> <span data-ttu-id="d465a-136">Das Zeichen folgen Array, `factoidStrings` , besteht aus [Faktoid](/previous-versions/ms583657(v=vs.100)) -Objekten, die als [AnalysisHintNode](/previous-versions/ms573018(v=vs.100)) -Objekte an den [InkAnalyzer](/previous-versions/ms583671(v=vs.100)) übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="d465a-136">The string array, `factoidStrings`, is made of [Factoid](/previous-versions/ms583657(v=vs.100)) objects that are passed into the [InkAnalyzer](/previous-versions/ms583671(v=vs.100)) as [AnalysisHintNode](/previous-versions/ms573018(v=vs.100)) objects.</span></span> <span data-ttu-id="d465a-137">Die AnalysisHintNode-Objekte übertragen den InkAnalyzer in Bezug auf bestimmte Eingaben.</span><span class="sxs-lookup"><span data-stu-id="d465a-137">The AnalysisHintNode objects bias the InkAnalyzer toward particular input.</span></span> <span data-ttu-id="d465a-138">In diesem Beispiel werden die Datums-, Uhrzeit-und Telefon Hinweise sowie einige andere verwendet.</span><span class="sxs-lookup"><span data-stu-id="d465a-138">This sample uses the date, time, and telephone hints, as well as some others.</span></span>

<span data-ttu-id="d465a-139">Jeder [AnalysisHintNode](/previous-versions/ms573018(v=vs.100)) ist einem bestimmten Bereich der Form zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="d465a-139">Each [AnalysisHintNode](/previous-versions/ms573018(v=vs.100)) is associated with a specific area of the form.</span></span> <span data-ttu-id="d465a-140">Die Bereiche werden durch das Array der Rechtecke dargestellt `rects` .</span><span class="sxs-lookup"><span data-stu-id="d465a-140">The areas are represented by the array of rectangles, `rects`.</span></span> <span data-ttu-id="d465a-141">Wenn Sie für jedes Rechteck ein [Textfeld](/dotnet/api/system.windows.forms.textbox?view=netcore-3.1) erstellen, gibt das Beispiel den erkannten Text an der richtigen Position aus.</span><span class="sxs-lookup"><span data-stu-id="d465a-141">By creating a [TextBox](/dotnet/api/system.windows.forms.textbox?view=netcore-3.1) for each rectangle, the sample outputs the recognized text in the correct location.</span></span>


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



<span data-ttu-id="d465a-142">Danach ist es lediglich wichtig, einen Ereignishandler zu erstellen, der die Handschrift Analyse auslöst, wenn der Benutzer auf "analysieren" klickt.</span><span class="sxs-lookup"><span data-stu-id="d465a-142">After that, it is merely a matter of creating an event handler that triggers the ink analysis when the user clicks Analyze.</span></span>


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



 

 
