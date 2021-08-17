---
description: Nicht alle Anwendungen erfordern die Verwendung der Erkennung, aber da die meisten Anwendungen mit Text als primären Datentyp entworfen wurden, ist die Möglichkeit, Ink in Text zu konvertieren, sehr wertvoll.
ms.assetid: 70d25839-6ddd-40db-8891-92da074d17b0
title: Ink-Erkennung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26c3f1431aca97f41b4de9aef64108f3e619ef7b6f9239f46fdde9f7bf4ff3da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118718294"
---
# <a name="ink-recognition"></a>Ink-Erkennung

Nicht alle Anwendungen erfordern die Verwendung der Erkennung, aber da die meisten Anwendungen mit Text als primären Datentyp entworfen wurden, ist die Möglichkeit, Ink in Text zu konvertieren, sehr wertvoll. Sie können die Erkennungsfeatures der Plattform-API für Tablet-PCs verwenden, um Informationen zu den verfügbaren Erkennungs-Engines zu abfragen, z. B. welche Sprachen sie erkennen. Sie können dann eine [**Strokes-Auflistung**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) aus einem [**Ink-Objekt**](inkdisp-class.md) an eine Erkennungs-Engine senden und ein [**RecognitionResult-Objekt zurückgeben**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) lassen.

## <a name="recognizercontext-object"></a>RecognizerContext-Objekt

Ein [**RecognizerContext-Objekt**](inkrecognizercontext-class.md) ist die Instanziierung einer bestimmten Erkannten. Mit **dem RecognizerContext-Objekt** können Sie eine bestimmte Auflistung von Strichen synchron oder asynchron erkennen. Bei der asynchronen Erkennung gibt das **RecognizerContext-Objekt** das [**RecognitionResult-Objekt**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) in einem Ereignisrückruf an die Anwendung zurück.

## <a name="recognizers-and-recognizer-objects"></a>Recognizers and Recognizer Objects

Auf einem einzelnen Tablet-PC ist möglicherweise eine oder mehrere Recognizer verfügbar. Sie können die Sammlung der Recognizer abfragen, um zu bestimmen, welche Recognizer verwendet werden soll. Eine Recognizer stellt spezifische Informationen zu ihren Funktionen bereit, z. B. die Sprache, die sie erkennen kann, und den Hersteller.

Instanziieren Sie ein [**InkRecognizerContext-Objekt**](inkrecognizercontext-class.md) wie in den folgenden C++- und C-Codebeispielen gezeigt, um zu bestimmen, ob mindestens eine Recognizer-Instanz \# installiert ist. Wenn keine Erkennen vorhanden ist, schlägt dieser Aufruf von [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) fehl.


```C++
CComPtr<IInkRecognizerContext> g_pIInkRecoContext;
hr = CoCreateInstance(CLSID_InkRecognizerContext, 
      NULL, CLSCTX_INPROC_SERVER,
      IID_IInkRecognizerContext, 
(void **) &g_pIInkRecoContext);
if (FAILED(hr)) 
{
      ::MessageBox(NULL, TEXT("No recognizers installed.\nExiting."), 
      gc_szAppName, MB_ICONERROR);
      return -1;
}
```




```CSharp
try
{
  Recognizers recos = new Recognizers();//Check for recognizer.
  Recognizer defReco = recos.GetDefaultRecognizer();
  recoContext = defReco.CreateRecognizerContext();
}
catch
{
  MessageBox.Show("No recognizers installed.");
}
```



## <a name="recognitionresult-and-recognitionalternate-objects"></a>RecognitionResult- und RecognitionAlternate-Objekte

Die Ergebnisse der Erkennung werden in einem [**RecognitionResult-Objekt**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) zurückgegeben. Die Ergebnisse enthalten eine optimale Ergebniszeichenfolge in der [TopString-Eigenschaft](/previous-versions/ms829602(v=msdn.10)) sowie eine Auflistung alternativer Ergebnisse in einer [**RecognitionAlternates-Auflistung.**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternates) Das **RecognitionResult-Objekt** kann mit der ursprünglichen [**Strokes-Auflistung**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) beibehalten werden, aus der es generiert wurde.

## <a name="recognizerguide-structure"></a>RecognizerGuide-Struktur

Die Erkennungsanleitung kann aus Zeilen und Spalten bestehen und der Erkennung einen besseren Kontext für die Erkennung geben. Sie können z. B. horizontale Linien auf dem Bildschirm eines Benutzers zeichnen, die fast wie ein regelrechtes Papier zeigen, wo Handschriften auftreten sollen (diese Art von Leitfaden würde nur aus Zeilen bestehen und keine Spalten). Wenn ein Benutzer in die Zeilen schreibt, verbessert sich die Erkennungsgenauigkeit anstelle von beliebigem Platz.

Die folgende Abbildung zeigt eine [**RecognizerGuide-Struktur**](inkrecognizerguide-class.md) mit zwei Zeilen für die Eingabe.

![Abbildung mit Zweizeilen-Recognizer-Leitfaden](images/9791100b-8279-4dd0-823f-0a38a0308a74.jpg)

Die folgende Abbildung zeigt eine [**RecognizerGuide-Struktur**](inkrecognizerguide-class.md) mit vier Spalten und drei Zeilen.

![Abbildung, die eine Drei-mal-vier-Anleitung zur Wiedererkennung zeigt](images/d1bbf2d3-9653-49d7-bf48-c1b26645074c.jpg)

Weitere Informationen zur Verwendung der [**RecognizerGuide-Struktur**](inkrecognizerguide-class.md) finden Sie im **Referenzthema RecognizerGuide.**

 

 
