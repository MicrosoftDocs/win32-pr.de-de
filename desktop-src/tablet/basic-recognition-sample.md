---
description: Diese Anwendung veranschaulicht, wie Sie eine einfache Handschrifterkennungsanwendung erstellen können. Dieses Programm erstellt ein InkCollector-Objekt, um das Fenster und ein Standarderkennungskontextobjekt zu aktivieren.
ms.assetid: 6dc94293-cdf7-4b90-a5e8-559f376add26
title: Grundlegendes Erkennungsbeispiel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcf45aa7695866e1cf413ea42b7c377b07ea84984ecf2cc3f44da93ff868072d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120111140"
---
# <a name="basic-recognition-sample"></a>Grundlegendes Erkennungsbeispiel

Diese Anwendung veranschaulicht, wie Sie  eine einfache Handschrifterkennungsanwendung erstellen können.

Dieses Programm erstellt ein [**InkCollector-Objekt,**](inkcollector-class.md) um das Fenster und ein *Standarderkennungskontextobjekt* zu aktivieren. Nach dem Empfang von "Recognize!" -Befehl, der über das Menü der Anwendung ausgelöst wird, werden die gesammelten Ink-Striche an den Erkennungskontext übergeben. Die beste Ergebniszeichenfolge wird in einem Meldungsfeld angezeigt.

## <a name="creating-the-recognizercontext-object"></a>Erstellen des RecognizerContext-Objekts

Wenn die WM CREATE-Nachricht beim Start in der WndProc-Prozedur für die Anwendung \_ empfangen wird, wird ein neuer Erkennungskontext erstellt, der die Standarderkennung verwendet. Dieser Kontext wird für die gesamte Erkennung in der Anwendung verwendet.


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

Der Recognize-Befehl wird empfangen, wenn der Benutzer auf Recognize! klickt. auf Updates zugreifen. Der Code ruft einen Zeiger auf die [**Freihandeingaben**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) (pIInkStrokes) aus dem [**InkDisp-Objekt**](inkdisp-class.md) ab und übergibt dann die **InkStrokes** mithilfe eines Aufrufs von putref-Strichen an den \_ Erkennungskontext.


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



Der Code ruft dann die [**Recognize-Methode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-recognize) des [**InkRecognizerContext-Objekts**](inkrecognizercontext-class.md) auf und übergibt einen Zeiger auf ein [**IInkRecognitionResult-Objekt,**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) um die Ergebnisse zu speichern.


```C++
              // Recognize
              IInkRecognitionResult* pIInkRecoResult = NULL;
              hr = g_pIInkRecoContext->Recognize(&pIInkRecoResult);
              if (SUCCEEDED(hr)) 
              {
```



Schließlich verwendet der Code die [**TopString-Eigenschaft**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionresult-get_topstring) des [**IInkRecognitionResult-Objekts,**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) ruft das oberste Erkennungsergebnis in eine Zeichenfolgenvariable ab, gibt das **IInkRecognitionResult-Objekt** frei und zeigt die Zeichenfolge in einem Meldungsfeld an.


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



Stellen Sie sicher, dass Sie den Erkennungskontext zwischen Verwendungen zurücksetzen.


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



 

 
