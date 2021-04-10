---
description: Diese Anwendung veranschaulicht, wie Sie eine einfache Handschrift Erkennungs Anwendung erstellen können. Dieses Programm erstellt ein InkCollector-Objekt, um das Fenster freizusetzen und ein Standardkontext Objekt für die Erkennung zu aktivieren.
ms.assetid: 6dc94293-cdf7-4b90-a5e8-559f376add26
title: Grundlegendes Erkennungs Beispiel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19679a6d1642a94ed813ba0428654b6e03009ea6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867739"
---
# <a name="basic-recognition-sample"></a>Grundlegendes Erkennungs Beispiel

Diese Anwendung veranschaulicht, wie Sie eine einfache *Handschrift* Erkennungs Anwendung erstellen können.

Dieses Programm erstellt ein [**InkCollector**](inkcollector-class.md) *-Objekt*, um das Fenster freizusetzen und ein Standardkontext Objekt für die *Erkennung* zu aktivieren. Beim Empfang der "erkennen!" der Befehl, der im Menü der Anwendung ausgelöst wird, werden die gesammelten Hand Striche an den Erkennungs Kontext übergeben. Die beste Ergebnis Zeichenfolge wird in einem Meldungs Feld dargestellt.

## <a name="creating-the-recognizercontext-object"></a>Erstellen des erkenzercontext-Objekts

Wenn in der WndProc-Prozedur für die Anwendung beim Start die WM \_ Create-Meldung empfangen wird, wird ein neuer Erkennungs Kontext erstellt, der die Standard Erkennung verwendet. Dieser Kontext wird für alle Erkennungs in der Anwendung verwendet.


```C++
case WM_CREATE:
{
    HRESULT hr;
    hr = CoCreateInstance(CLSID_InkRecognizerContext,
             NULL, CLSCTX_INPROC_SERVER, IID_IInkRecognizerContext,
             (void **) &g_pIInkRecoContext);
    if (FAILED(hr))
    {
        ::MessageBox(NULL, TEXT("There are no handwriting recognizers installed.\n"
            "You need to have at least one in order to run this sample.\nExiting."),
            gc_szAppName, MB_ICONERROR);
        return -1;
    }
  //...
```



## <a name="recognizing-the-strokes"></a>Erkennen der Striche

Der Befehl "erkennen" wird empfangen, wenn der Benutzer auf "erkennen" klickt. auf Updates zugreifen. Der Code erhält einen Zeiger auf die frei Hand [**Eingaben (piinkstrokes)**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) des [**InkDisp**](inkdisp-class.md) -Objekts und übergibt dann die **inkstriche** mithilfe eines Aufrufes PutRef-Taktes an den Erkennungs Kontext \_ .


```C++
 case WM_COMMAND:
  //...
  else if (wParam == ID_RECOGNIZE)
  {
      // change cursor to the system's Hourglass
      HCURSOR hCursor = ::SetCursor(::LoadCursor(NULL, IDC_WAIT));
      // Get a pointer to the ink stroke collection
      // This collection is a snapshot of the entire ink object
      IInkStrokes* pIInkStrokes = NULL;
      HRESULT hr = g_pIInkDisp->get_Strokes(&pIInkStrokes);
      if (SUCCEEDED(hr)) 
      {
          // Pass the stroke collection to the recognizer context
          hr = g_pIInkRecoContext->putref_Strokes(pIInkStrokes);
          if (SUCCEEDED(hr)) 
          {
```



Der Code ruft dann die [**Erkennungs**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-recognize) Methode des [**inkrecognizercontext**](inkrecognizercontext-class.md) -Objekts auf und übergibt einen Zeiger auf ein [**iinkrecognitionresult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) -Objekt, um die Ergebnisse zu speichern.


```C++
              // Recognize
              IInkRecognitionResult* pIInkRecoResult = NULL;
              hr = g_pIInkRecoContext->Recognize(&pIInkRecoResult);
              if (SUCCEEDED(hr)) 
              {
```



Schließlich verwendet der Code die [**TopString**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionresult-get_topstring) -Eigenschaft des [**iinkrecognitionresult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) -Objekts, wobei das Top-Erkennungs Ergebnis in eine Zeichen folgen Variable abgerufen wird, das **iinkrecognitionresult** -Objekt freigegeben wird und die Zeichenfolge in einem Meldungs Feld angezeigt wird.


```C++
                  // Get the best result of the recognition 
                  BSTR bstrBestResult = NULL;
                  hr = pIInkRecoResult->get_TopString(&bstrBestResult);
                  pIInkRecoResult->Release();
                  pIInkRecoResult = NULL;

                  // Show the result string
                  if (SUCCEEDED(hr) && bstrBestResult)
                  {
                      MessageBoxW(hwnd, bstrBestResult, 
                                  L"Recognition Results", MB_OK);
                      SysFreeString(bstrBestResult);
                  }  }
        
```



Stellen Sie sicher, dass Sie den Erkennungs Kontext zwischen Verwendungen zurücksetzen.


```
              // Reset the recognizer context
              g_pIInkRecoContext->putref_Strokes(NULL);
          }
          pIInkStrokes->Release();
      }
      // restore the cursor
      ::SetCursor(hCursor);
  }
```



 

 
