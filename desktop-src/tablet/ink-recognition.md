---
description: Nicht alle Anwendungen erfordern die Verwendung der Erkennung, aber da die meisten Anwendungen mit Text als primärer Datentyp entworfen wurden, ist die Möglichkeit, frei Hand Eingaben in Text umzuwandeln, sehr wertvoll.
ms.assetid: 70d25839-6ddd-40db-8891-92da074d17b0
title: Frei Handerkennung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ca4ec6f897c797d86df96c5d9c2cfd5d80f16c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104568895"
---
# <a name="ink-recognition"></a>Frei Handerkennung

Nicht alle Anwendungen erfordern die Verwendung der Erkennung, aber da die meisten Anwendungen mit Text als primärer Datentyp entworfen wurden, ist die Möglichkeit, frei Hand Eingaben in Text umzuwandeln, sehr wertvoll. Mithilfe der Erkennungs Features der Tablet PC Platform-API können Sie Informationen zu den verfügbaren Erkennungs Modulen Abfragen, z. b. welche Sprachen Sie erkennen. Sie können dann eine [**Striche**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) -Auflistung von einem frei Hand Objekt an eine Erkennungs-Engine senden und ein [**erkentionresult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) [**-Objekt zurück**](inkdisp-class.md) geben lassen.

## <a name="recognizercontext-object"></a>Erkenzercontext-Objekt

Ein [**erkenzercontext**](inkrecognizercontext-class.md) -Objekt ist die Instanziierung einer angegebenen Erkennung. Das **erkenzercontext** -Objekt ermöglicht es Ihnen, eine angegebene Auflistung von Strichen synchron oder asynchron zu erkennen. Beim asynchronen erkennen gibt das **erkenzercontext** -Objekt das [**erkentionresult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) -Objekt in einem Ereignis Rückruf an die Anwendung zurück.

## <a name="recognizers-and-recognizer-objects"></a>Erkenzer und Erkennungs Objekte

Auf einem einzelnen Tablet PC ist möglicherweise mindestens ein Erkennungs Modul verfügbar. Sie können die Auflistung der Erkennungs Modul Abfragen, um zu bestimmen, welche Erkennungsfunktion verwendet werden soll. Eine Erkennung stellt spezifische Informationen über ihre Funktionen bereit, z. b. die erkannte Sprache und den Hersteller.

Um zu ermitteln, ob mindestens eine Erkennung installiert ist, instanziieren Sie ein [**inkrecognizercontext**](inkrecognizercontext-class.md) -Objekt, wie in den folgenden C++-und C- \# Codebeispielen gezeigt. Wenn eine Erkennung nicht vorhanden ist, schlägt dieser [**cokreateinstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) -Befehl fehl.


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



## <a name="recognitionresult-and-recognitionalternate-objects"></a>Erkennungs Ergebnis und erkenntionalternate-Objekte

Die Ergebnisse der Erkennung werden in einem [**erkentionresult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) -Objekt zurückgegeben. Die Ergebnisse enthalten eine beste Ergebnis Zeichenfolge in der [TopString](/previous-versions/ms829602(v=msdn.10)) -Eigenschaft sowie eine Auflistung alternativer Ergebnisse in einer " [**erkenntionalternativen**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternates) "-Auflistung. Das **erkentionresult** -Objekt kann mit der ursprünglichen [**Strokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) -Auflistung persistent gespeichert werden, aus der es generiert wurde.

## <a name="recognizerguide-structure"></a>Erkenn-Guide-Struktur

Das Erkennungs Handbuch kann aus Zeilen und Spalten bestehen und ermöglicht der Erkennung einen besseren Kontext, in dem die Erkennung durchgeführt werden kann. Sie können z. b. horizontale Linien auf dem Bildschirm eines Benutzers zeichnen, ähnlich wie ein gezeichnetes Papier Stück, das anzeigt, wo die Handschrift auftreten soll (dieser Richtlinientyp würde nur aus Zeilen bestehen und keine Spalten). Wenn ein Benutzer anstelle eines beliebigen Speicherplatzes in den Zeilen schreibt, verbessert sich die Erkennungsgenauigkeit.

Die folgende Abbildung zeigt eine [**Erkennungs Leit Faden**](inkrecognizerguide-class.md) Struktur mit zwei Zeilen für die Eingabe.

![Abbildung der zweizeiligen Erkennungs Leit Faden](images/9791100b-8279-4dd0-823f-0a38a0308a74.jpg)

Die folgende Abbildung zeigt eine [**Erkennungs Leit Faden**](inkrecognizerguide-class.md) Struktur mit vier Spalten und drei Zeilen.

![Abbildung der drei-bis vier Erkennungs Leit Faden](images/d1bbf2d3-9653-49d7-bf48-c1b26645074c.jpg)

Weitere Informationen zum Verwenden der [**Erkennungs Leit Faden**](inkrecognizerguide-class.md) Struktur finden Sie im Thema zur **Erkennungs** -und Erkennungs Anleitung.

 

 
