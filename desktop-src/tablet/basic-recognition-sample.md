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
# <a name="basic-recognition-sample"></a><span data-ttu-id="bcbd3-103">Grundlegendes Erkennungs Beispiel</span><span class="sxs-lookup"><span data-stu-id="bcbd3-103">Basic Recognition Sample</span></span>

<span data-ttu-id="bcbd3-104">Diese Anwendung veranschaulicht, wie Sie eine einfache *Handschrift* Erkennungs Anwendung erstellen können.</span><span class="sxs-lookup"><span data-stu-id="bcbd3-104">This application demonstrates how you can build a simple *handwriting* recognition application.</span></span>

<span data-ttu-id="bcbd3-105">Dieses Programm erstellt ein [**InkCollector**](inkcollector-class.md) *-Objekt*, um das Fenster freizusetzen und ein Standardkontext Objekt für die *Erkennung* zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="bcbd3-105">This program creates an [**InkCollector**](inkcollector-class.md) object to *ink*-enable the window and a default *recognizer context* object.</span></span> <span data-ttu-id="bcbd3-106">Beim Empfang der "erkennen!"</span><span class="sxs-lookup"><span data-stu-id="bcbd3-106">Upon receiving the "Recognize!"</span></span> <span data-ttu-id="bcbd3-107">der Befehl, der im Menü der Anwendung ausgelöst wird, werden die gesammelten Hand Striche an den Erkennungs Kontext übergeben.</span><span class="sxs-lookup"><span data-stu-id="bcbd3-107">command, fired from the application's menu, the collected ink strokes are passed to the recognizer context.</span></span> <span data-ttu-id="bcbd3-108">Die beste Ergebnis Zeichenfolge wird in einem Meldungs Feld dargestellt.</span><span class="sxs-lookup"><span data-stu-id="bcbd3-108">The best result string is presented in a message box.</span></span>

## <a name="creating-the-recognizercontext-object"></a><span data-ttu-id="bcbd3-109">Erstellen des erkenzercontext-Objekts</span><span class="sxs-lookup"><span data-stu-id="bcbd3-109">Creating the RecognizerContext Object</span></span>

<span data-ttu-id="bcbd3-110">Wenn in der WndProc-Prozedur für die Anwendung beim Start die WM \_ Create-Meldung empfangen wird, wird ein neuer Erkennungs Kontext erstellt, der die Standard Erkennung verwendet.</span><span class="sxs-lookup"><span data-stu-id="bcbd3-110">In the WndProc procedure for the application, when the WM\_CREATE message is received on startup, a new recognizer context that uses the default recognizer is created.</span></span> <span data-ttu-id="bcbd3-111">Dieser Kontext wird für alle Erkennungs in der Anwendung verwendet.</span><span class="sxs-lookup"><span data-stu-id="bcbd3-111">This context is used for all recognition in the application.</span></span>


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



## <a name="recognizing-the-strokes"></a><span data-ttu-id="bcbd3-112">Erkennen der Striche</span><span class="sxs-lookup"><span data-stu-id="bcbd3-112">Recognizing the Strokes</span></span>

<span data-ttu-id="bcbd3-113">Der Befehl "erkennen" wird empfangen, wenn der Benutzer auf "erkennen" klickt.</span><span class="sxs-lookup"><span data-stu-id="bcbd3-113">The recognize command is received when the user clicks the Recognize!</span></span> <span data-ttu-id="bcbd3-114">auf Updates zugreifen.</span><span class="sxs-lookup"><span data-stu-id="bcbd3-114">menu item.</span></span> <span data-ttu-id="bcbd3-115">Der Code erhält einen Zeiger auf die frei Hand [**Eingaben (piinkstrokes)**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) des [**InkDisp**](inkdisp-class.md) -Objekts und übergibt dann die **inkstriche** mithilfe eines Aufrufes PutRef-Taktes an den Erkennungs Kontext \_ .</span><span class="sxs-lookup"><span data-stu-id="bcbd3-115">The code gets a pointer to the ink [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) (pIInkStrokes) off of the [**InkDisp**](inkdisp-class.md) object, and then passes the **InkStrokes** to the recognizer context using a call to putref\_Strokes.</span></span>


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



<span data-ttu-id="bcbd3-116">Der Code ruft dann die [**Erkennungs**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-recognize) Methode des [**inkrecognizercontext**](inkrecognizercontext-class.md) -Objekts auf und übergibt einen Zeiger auf ein [**iinkrecognitionresult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) -Objekt, um die Ergebnisse zu speichern.</span><span class="sxs-lookup"><span data-stu-id="bcbd3-116">The code then calls the [**Recognize**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-recognize) method of the [**InkRecognizerContext**](inkrecognizercontext-class.md) object, passing in a pointer to an [**IInkRecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) object to hold the results.</span></span>


```C++
              // Recognize
              IInkRecognitionResult* pIInkRecoResult = NULL;
              hr = g_pIInkRecoContext->Recognize(&pIInkRecoResult);
              if (SUCCEEDED(hr)) 
              {
```



<span data-ttu-id="bcbd3-117">Schließlich verwendet der Code die [**TopString**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionresult-get_topstring) -Eigenschaft des [**iinkrecognitionresult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) -Objekts, wobei das Top-Erkennungs Ergebnis in eine Zeichen folgen Variable abgerufen wird, das **iinkrecognitionresult** -Objekt freigegeben wird und die Zeichenfolge in einem Meldungs Feld angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="bcbd3-117">Finally, the code uses the [**IInkRecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) object's [**TopString**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionresult-get_topstring) property retrieve the top recognition result into a string variable, releases the **IInkRecognitionResult** object, and displays the string in a message box.</span></span>


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



<span data-ttu-id="bcbd3-118">Stellen Sie sicher, dass Sie den Erkennungs Kontext zwischen Verwendungen zurücksetzen.</span><span class="sxs-lookup"><span data-stu-id="bcbd3-118">Be sure to reset the recognizer context between usages.</span></span>


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



 

 
