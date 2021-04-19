---
description: Zum Erstellen eines Anwendungs Wörterbuchs muss die WordList-Eigenschaft des erkennzercontext-Objekts festgelegt werden.
ms.assetid: 24dbf617-fa16-44f1-ba59-d4d99b8f1375
title: Verwenden eines Anwendungs Wörterbuchs mit InkEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4bc919fc071f249611d42b8decb6ce4fb0b0f88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345047"
---
# <a name="using-an-application-dictionary-with-inkedit"></a>Verwenden eines Anwendungs Wörterbuchs mit InkEdit

Zum Erstellen eines Anwendungs Wörterbuchs muss die [**WordList**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) -Eigenschaft des [**erkennzercontext**](inkrecognizercontext-class.md) -Objekts festgelegt werden. Das **Erkennungs Kontext** Objekt wird vom [InkEdit](inkedit-control-reference.md) -Steuerelement nicht verfügbar gemacht, daher ist es nicht möglich, die **WordList** -Eigenschaft des **Erkennungs Kontext** Objekts des InkEdit-Steuer Elements direkt festzulegen.

Wenn Sie ein Anwendungs Wörterbuch mit einem [InkEdit](inkedit-control-reference.md) -Steuerelement verwenden möchten, müssen Sie die Striche aus dem InkEdit-Steuerelement entfernen, Sie an ein neues [**erkenzercontext**](inkrecognizercontext-class.md) **-Objekt übergeben** , wobei die [**WordList**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) -Eigenschaft auf eine [**WordList**](inkwordlist-class.md) mit dem Anwendungs Wörterbuch festgelegt ist

## <a name="example"></a>Beispiel

Der folgende C- \# Code zeigt ein Beispiel für diese Technik.


```C++
private RecognizerContext rc;
private WordList wl;
private int wlSelStart;
private int wlSelLen;
private bool isRecoPending = false;

private void Form1_Load(object sender, EventArgs e)
{
  //event handlers must be attached for dictionary to work.
  inkEdit1.Recognition += new Microsoft.Ink.InkEditRecognitionEventHandler(inkEdit1_Recognition);
  inkEdit1.TextChanged += new EventHandler(inkEdit1_TextChanged);

  //create a WordList that contains the application dictionary
  wl = new WordList();
  //...
  //Add dictionary terms to the WordList
  //...

  // create a RecognizerContext for the WordList
  rc = inkEdit1.Recognizer.CreateRecognizerContext();
  rc.Factoid = Factoid.WordList;

  //set the RecognizerContext WordList to the newly created WordList
  rc.WordList = wl;

  //create a delegate for the new RecognizerContext
  rc.RecognitionWithAlternates += new

  RecognizerContextRecognitionWithAlternatesEventHandler(rc_Recognition);
}

void inkEdit1_TextChanged(object sender, EventArgs e)
{
  if (isRecoPending)
  {
    isRecoPending = false;
    rc.BackgroundRecognizeWithAlternates();
  }
}

private void inkEdit1_Recognition(object sender,
Microsoft.Ink.InkEditRecognitionEventArgs e)
{
  //store the start of the selection in wlSelStart
  wlSelStart = inkEdit1.SelectionStart;

  //store the length of the selection in wlSelLen
  wlSelLen = e.RecognitionResult.TopString.Length;

  //copy the strokes from the InkEdit control into the new
  // RecognizerContext
  rc.Strokes = e.RecognitionResult.Strokes.Ink.Clone().Strokes;
  isRecoPending = true;
}

private void rc_Recognition(object sender,
Microsoft.Ink.RecognizerContextRecognitionWithAlternatesEventArgs e)
{
  if (inkEdit1.InvokeRequired)
  {
    inkEdit1.Invoke(new RecognizerContextRecognitionWithAlternatesEventHandler(rc_Recognition),
      new object[] { sender, e });
    return;
  }

  //set the insertion point in the InkEdit control
  inkEdit1.SelectionStart = wlSelStart;
  inkEdit1.SelectionLength = wlSelLen;
  //insert the result from the new RecognizerContext 
  //into the InkEdit control
  inkEdit1.SelectedText = e.Result.TopString;
  inkEdit1.SelectionStart = inkEdit1.SelectionStart +
  e.Result.TopString.Length;
}

// Event handler for the form's closed event
private void Form1_Closed(object sender, System.EventArgs e)
{
  inkEdit1.Dispose();
  inkEdit1 = null;
  rc.Dispose();
  rc = null;
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[InkEdit-Steuerelement](/previous-versions/ms552265(v=vs.100))
</dt> <dt>

[Microsoft. Ink. erkenzercontext-Klasse](/previous-versions/ms552546(v=vs.100))
</dt> <dt>

[Microsoft. Ink. WordList-Klasse](/previous-versions/ms827589(v=msdn.10))
</dt> </dl>

 

 
