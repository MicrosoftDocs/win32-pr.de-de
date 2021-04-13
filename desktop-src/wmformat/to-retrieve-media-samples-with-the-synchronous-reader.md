---
title: So rufen Sie Medien Beispiele mit dem synchronen Reader ab
description: So rufen Sie Medien Beispiele mit dem synchronen Reader ab
ms.assetid: 7e228a0b-e29d-485e-b2ef-81c0311ca828
keywords:
- Advanced Systems Format (ASF), Abrufen von Medien Beispielen
- ASF (Advanced Systems Format), Abrufen von Medien Beispielen
- Advanced Systems Format (ASF), synchrone Reader
- ASF (Advanced Systems Format), synchrone Reader
- synchrone Leser, Abrufen von Medien Beispielen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1fd341ea9616b18a5e65cfa8c1134e0f1be44b5
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104389875"
---
# <a name="to-retrieve-media-samples-with-the-synchronous-reader"></a>So rufen Sie Medien Beispiele mit dem synchronen Reader ab

Sie müssen jede Stichprobe einzeln vom synchronen Reader anfordern. Dadurch erhalten Sie mehr Kontrolle über die Beispiele, die Sie erhalten und wann Sie empfangen werden.

Verwenden Sie die [**iwmsynkreader:: getnextsample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample) -Methode, um ein Beispiel abzurufen. Sie müssen hauptsächlich Zeiger auf Variablen übergeben, die mit Informationen zu dem Beispiel gefüllt werden, das als Parameter abgerufen wird. Der einzige Eingabeparameter ist *wstreamnum*. Wenn Sie eine streamnummer übergeben, ruft **getnextsample** das nächste Beispiel mit der angegebenen streamnummer ab. Wenn Sie 0 (null) für *wstreamnum* übergeben, wird das nächste Beispiel, das in der Datei chronologisch vorkommt, abgerufen.

Standardmäßig ruft der synchrone Reader alle Beispiele aus den Ausgaben in einer Datei in chronologischer Reihenfolge ab. Wenn Sie **getnextsample** aufrufen und keine weiteren abzurufenden Beispiele vorhanden sind, werden keine weiteren Beispiele zurückgegeben, bei denen es sich um \_ \_ \_ \_ einen Fehlercode handelt. Wenn Sie daher codieren, können Sie einfach Beispiele durchlaufen, bis die Methode fehlschlägt.

> [!Note]  
> Um sicherzustellen, dass der synchrone Reader korrekte Beispiel dauern für Videostreams bereitstellt, müssen Sie zuerst die Datenstrom Ausgabe konfigurieren. Nennen Sie die [**iwmsyncreader:: setoutputsetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setoutputsetting) -Methode, um die g \_ wszvideosampledurations-Einstellung auf " **true**" festzulegen.

 

Beispielcode

Im folgenden Beispielcode wird gezeigt, wie **getnextsample** zum Abrufen aller Beispiele in einer Datei verwendet wird.


```C++
// Loop through all the samples in the file.
do
{
   // Get the next sample.
   hr = pSyncReader->GetNextSample(0,
                                   &pMyBuffer,
                                   &cnsSampleTime,
                                   &cnsSampleDuration,
                                   &dwFlags,
                                   &dwOutputNumber,
                                   NULL);

   if(SUCCEEDED(hr))
   {
      // TODO: Process the sample in whatever way is appropriate 
      // to your application. When finished, clean up.
      pMyBuffer->Release();
      pMyBuffer = NULL;
      cnsSampleTime     = 0;
      cnsSampleDuration = 0;
      dwFlags           = 0;
      dwOutputNumber    = 0;
   }
} 
while (SUCCEEDED(hr));

```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Iwmsynkreader-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[**Lesen von Dateien mit dem synchronen Reader**](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




