---
title: So rufen Sie Medienbeispiele mit dem synchronen Reader ab
description: So rufen Sie Medienbeispiele mit dem synchronen Reader ab
ms.assetid: 7e228a0b-e29d-485e-b2ef-81c0311ca828
keywords:
- Advanced Systems Format (ASF), Abrufen von Medienbeispielen
- ASF (Advanced Systems Format), Abrufen von Medienbeispielen
- Advanced Systems Format (ASF), synchrone Reader
- ASF (Advanced Systems Format), synchrone Reader
- Synchrone Reader,Abrufen von Medienbeispielen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e1ec4fc7e8a894de304ea828cef9d8e019f4cdedfd2fbd851a427382ba741a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807430"
---
# <a name="to-retrieve-media-samples-with-the-synchronous-reader"></a>So rufen Sie Medienbeispiele mit dem synchronen Reader ab

Sie müssen jedes Beispiel nacheinander vom synchronen Reader anfordern. Dies bietet Ihnen mehr Kontrolle über die Beispiele, die Sie erhalten, und wann Sie sie erhalten.

Verwenden Sie [**die IWMSyncReader::GetNextSample-Methode,**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample) um ein Beispiel abzurufen. Sie müssen hauptsächlich Zeiger auf Variablen übergeben, die mit Informationen über das als Parameter abgerufene Beispiel gefüllt werden. Der einzige Eingabeparameter ist *wStreamNum.* Wenn Sie eine Streamnummer übergeben, **ruft GetNextSample** das nächste Beispiel mit der angegebenen Streamnummer ab. Wenn Sie 0 (null) für *wStreamNum übergeben,* wird das nächste Beispiel abgerufen, das chronologisch in der Datei auftritt.

Standardmäßig ruft der synchrone Reader alle Stichproben aus den Ausgaben in einer Datei in chronologischer Reihenfolge ab. Wenn Sie **GetNextSample** aufrufen und keine Beispiele mehr zu erhalten sind, wird NS E NO MORE SAMPLES zurückgegeben. Dies ist ein \_ \_ \_ \_ Fehlercode. Beim Codieren können Sie daher einfach Stichproben durchschleifen, bis die Methode fehlschlägt.

> [!Note]  
> Um sicherzustellen, dass der synchrone Reader die richtige Beispieldauer für Videostreams liefert, müssen Sie zuerst die Streamausgabe konfigurieren. Rufen Sie [**die IWMSyncReader::SetOutputSetting-Methode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setoutputsetting) auf, um die g \_ wszVideoSampleDurations-Einstellung auf **TRUE zu setzen.**

 

Beispielcode

Der folgende Beispielcode zeigt, wie **GetNextSample verwendet** wird, um alle Beispiele in einer Datei abzurufen.


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

[**IWMSyncReader-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[**Lesen von Dateien mit dem synchronen Reader**](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




