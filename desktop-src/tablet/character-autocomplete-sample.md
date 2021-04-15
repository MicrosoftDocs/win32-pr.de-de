---
description: Das Auto Vervollständigen-Beispiel veranschaulicht die Implementierung von Zeichen AutoComplete in Japanisch mithilfe der Erkennungs-APIs (Application Programming Interfaces).
ms.assetid: 237e33bc-3708-4128-8749-d3d031f7237a
title: Beispiel für automatische Vervollständigung von Zeichen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4853cdef72a087aff3b9b726f0c83af9038ef5bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524400"
---
# <a name="character-autocomplete-sample"></a>Beispiel für automatische Vervollständigung von Zeichen

Das Auto Vervollständigen-Beispiel veranschaulicht die Implementierung von Zeichen AutoComplete in Japanisch mithilfe der Erkennungs-APIs (Application Programming Interfaces).

In diesem Beispiel werden die folgenden Funktionen verwendet:

-   Verwenden eines *Ink Collector*
-   Verwenden eines *erkentekontexts*

## <a name="initializing-the-ink-collector-and-recognizer-context"></a>Initialisieren des Auflistungs Auflistungs-und Erkennungs Kontexts

Die [**InkCollector**](inkcollector-class.md) -und [**inkrecognizercontext**](inkrecognizercontext-class.md) -Objekte werden als Klassen deklariert, die Ereignisse auslassen können.


```C++
Dim WithEvents ic As InkCollector
Dim WithEvents rc As InkRecognizerContext
```



Der Lade Ereignishandler des Formulars erstellt einen frei Hand Sammler, ordnet dem Bild Feld "Ink Collector" zu und aktiviert die frei Hand Auflistung. Der Ereignishandler lädt dann die standardmäßige japanische Erkennung und initialisiert die Eigenschaften für das Erkennungs Programm und die Striche-Eigenschaften.


```C++
Private Sub Form_Load()
   ' Set the ink collector to work in the small frame window
    Set ic = New InkCollector    ic.hWnd = fraBox.hWnd    ic.Enabled = True
    
    ' Get the Japanese recognizer
    LoadRecognizer

    ' Initialize the recognizer context
    Dim Guide As New InkRecognizerGuide
    Dim FrameRectangle As New InkRectangle
    Dim Top As Long
    Dim Bottom As Long
    Dim Left As Long
    Dim Right As Long
    Top = 0
    Left = 0
    Bottom = fraBox.ScaleHeight
    Right = fraBox.ScaleWidth
    ic.Renderer.PixelToInkSpace Me.hdc, Top, Left
    ic.Renderer.PixelToInkSpace Me.hdc, Bottom, Right
    FrameRectangle.Bottom = Bottom
    FrameRectangle.Top = Top
    FrameRectangle.Left = Left
    FrameRectangle.Right = Right
    Guide.Columns = 1
    Guide.Rows = 1
    Guide.Midline = -1 ' Do not use midline
    Guide.DrawnBox = FrameRectangle
    Guide.WritingBox = FrameRectangle
    Set rc.Guide = Guide
    
    ' Set the strokes collection on the recognizer context
    Set ink = ic.ink    Set rc.Strokes = ic.ink.Strokes
End Sub
```



## <a name="loading-the-default-japanese-recognizer"></a>Laden der japanischen Standard Erkennung

Die [**GetDefaultRecognizer**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizers-getdefaultrecognizer) -Methode von [**inkrecognizers**](/previous-versions/windows/desktop/legacy/ms702438(v=vs.85)) wird aufgerufen, um die Standard Erkennung für die japanische Sprache abzurufen. Anschließend wird die [**Language-Eigenschaft des**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_languages) iinkrecognizer-Objekts geprüft, um zu bestimmen, ob die Erkennung die japanische Sprache unterstützt. Wenn dies der Fall ist, wird die Methode " [**kreaterecognizercontext**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-createrecognizercontext) " der Erkennung verwendet, um einen Erkennungs Kontext für das Formular zu generieren.


```C++
Private Sub LoadRecognizer()
    On Error GoTo NoRecognizer
    ' Get a Japanese recognizer context
    Dim recos As New InkRecognizers
    Dim JapaneseReco As IInkRecognizer
    Set JapaneseReco = recos.GetDefaultRecognizer(&H411)
    If JapaneseReco Is Nothing Then
        MsgBox "Japanese Recognizers are not installed on this system. Exiting."
        End
    End If
    
    ' Check that this is indeed a Japanese recognizer
    Dim IsJapanese As Boolean
    Dim lan As Integer
    IsJapanese = False
    For lan = LBound(JapaneseReco.Languages) To UBound(JapaneseReco.Languages)
        If JapaneseReco.Languages(lan) = &H411 Then
            IsJapanese = True
        End If
    Next lan
    If Not IsJapanese Then
        MsgBox "Japanese Recognizers are not installed on this system. Exiting."
        End
    End If
    Set rc = JapaneseReco.CreateRecognizerContext
    Exit Sub
NoRecognizer:
    MsgBox "Japanese Recognizers are not installed on this system. Exiting."
    End
End Sub
```



## <a name="handling-the-stroke-event"></a>Behandeln des Stroke-Ereignisses

Der [**Stroke**](inkcollector-stroke.md) -Ereignishandler stoppt zuerst die Hintergrund Erkennung im Erkennungs Kontext. Anschließend wird der neue Strich der Eigenschaft [**Striche**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes) des Erkennungs Moduls hinzugefügt. Schließlich wird die [**inkrecognizercharakteriautocompletionmode**](/windows/desktop/api/msinkaut/ne-msinkaut-inkrecognizercharacterautocompletionmode) -Eigenschaft der Erkennungsfunktion festgelegt und die [**backgrounderkennzewithalternativen**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates) -Methode der Erkennungsfunktion für jeden der drei Zeichen für den Auto Vervollständigen-Modus aufgerufen. Der *CustomData* -Parameter des **backgrounderkennzewithalternativen** -Methoden Aufrufes wird verwendet, um zu identifizieren, welche Erkennungsergebnisse im Ereignis " [**erkenntionwithalternativen**](inkrecognizercontext-recognitionwithalternates.md) " zurückgegeben werden.


```C++
Private Sub ic_Stroke(ByVal Cursor As MSINKAUTLib.IInkCursor, ByVal Stroke As MSINKAUTLib.IInkStrokeDisp, Cancel As Boolean)

    ' Stop the unfinished recognition processes
    rc.StopBackgroundRecognition

    ' Add the new stroke
    rc.Strokes.Add Stroke

    ' Get a result for all three CAC modes
    rc.CharacterAutoCompletionMode = IRCACM_Full rc.BackgroundRecognizeWithAlternates 0 rc.CharacterAutoCompletionMode = IRCACM_Prefix rc.BackgroundRecognizeWithAlternates 1 rc.CharacterAutoCompletionMode = IRCACM_Random rc.BackgroundRecognizeWithAlternates 2
End Sub
```



## <a name="handling-the-recognition-with-alternates-event"></a>Behandeln der Erkennung mit alternativen Ereignissen

Der-Handler für das Ereignis " [**erkenntionwithalternativen**](inkrecognizercontext-recognitionwithalternates.md) " überprüft zuerst den *Erkennungs Status* -Parameter. Wenn bei der Erkennung ein Fehler auftritt, ignoriert der Ereignishandler die Erkennungsergebnisse. Andernfalls fügt der Ereignishandler den *Erkennungs Ergebnis* Parameter dem entsprechenden Bildfeld hinzu und speichert die Ergebnis Zeichenfolge. Der *CustomData* -Parameter wird im Aufrufen der [**backgrounderkennzewithalternativen**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates) -Methode festgelegt und identifiziert, welcher Zeichen Auto Vervollständigen-Modus vom Erkennungs Kontext verwendet wurde.


```C++
Private Sub rc_RecognitionWithAlternates(ByVal RecognitionResult As MSINKAUTLib.IInkRecognitionResult, ByVal vCustomParam As Variant, ByVal RecognitionStatus As MSINKAUTLib.InkRecognitionStatus)
    ' Get the alternates from the recognition result
    ' and display them in the right place
    Dim ResultString As String
    Dim alts As IInkRecognitionAlternates
    Dim alt As IInkRecognitionAlternate
        
    On Error GoTo EndFunc

    If RecognitionStatus = IRS_NoError Then
        ' Fill a string with all the characters for this CAC mode
        Set alts = RecognitionResult.AlternatesFromSelection
        For Each alt In alts
            ResultString = ResultString + alt.String
        Next alt
        ' Display the string
        Dim r As RECT
        r.Left = 0
        r.Top = 0
        r.Right = 1000
        r.Bottom = 1000
        PctResult(vCustomParam).Cls
        DrawText PctResult(vCustomParam).hdc, StrPtr(ResultString), Len(ResultString), r, 0
        If vCustomParam = 0 Then
            FullCACText = ResultString
        Else
            If vCustomParam = 1 Then
                PrefixCACText = ResultString
            Else
                If vCustomParam = 2 Then
                    RandomCACText = ResultString
                End If
            End If
        End If
    End If
    Exit Sub
EndFunc:
    MsgBox Err.Description
End Sub
```



## <a name="painting-the-form"></a>Zeichnen des Formulars

Der Paint-Ereignishandler löscht die Ergebnisbild Felder und fügt ihnen die gespeicherten Erkennungsergebnisse hinzu.

## <a name="deleting-the-strokes"></a>Löschen der Striche

Die-Methode des Formulars `CmdClear_Click` verarbeitet den Clear-Befehl. Wenn der [**InkCollector**](inkcollector-class.md) derzeit frei Hand Eingaben sammelt, wird ein Meldungs Feld angezeigt, und der Befehl wird ignoriert. Andernfalls beendet der Ereignishandler die Hintergrund Erkennung, löscht die [**Strokes**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes) -Eigenschaft des Erkennungs Kontexts und löscht die Striche aus dem [**InkDisp**](inkdisp-class.md) -Objekt des Formulars. Anschließend zeichnet der Ereignishandler das Bildfeld neu, dem der frei Hand Sammler zugeordnet ist, und löscht die Erkennungs Zeichenfolgen und Bildfelder.


```C++
If Not (ic.CollectingInk) Then

    ' Stop the unfinished recognition processes
    rc.StopBackgroundRecognition

    ' ...
    Set rc.Strokes = Nothing

    ' Delete all the strokes from the ink object
    ic.Ink.DeleteStrokes strokesToDelete

    ' Refresh the window
    fraBox.Refresh

    ' refresh the recognizer context
    Set rc.Strokes = ic.Ink.Strokes

    ' Clear the result strings
    FullCACText = ""
    PrefixCACText = ""
    RandomCACText = ""

    ' Clear the result windows
    PctResult(0).Cls
    PctResult(1).Cls
    PctResult(2).Cls

Else
    MsgBox "Cannot clear ink while the ink collector is busy."
End If
```



 

 
