---
description: Erfassen von Videos in einer AVI-Datei
ms.assetid: 0f5f4a82-4a2e-4c48-b201-bda641cb8619
title: Erfassen von Videos in einer AVI-Datei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f5ec58c021c5f37fed992959b33965efddb5603798ff756909879d307bca1f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119689035"
---
# <a name="capturing-video-to-an-avi-file"></a>Erfassen von Videos in einer AVI-Datei

Die folgende Abbildung zeigt das einfachste mögliche Diagramm zum Erfassen von Videos in einer AVI-Datei.

![Avi Video Capture Graph](images/vidcap02.png)

Der [AVI Mux-Filter](avi-mux-filter.md) verwendet den Videostream aus dem Aufnahmepin und packt ihn in einen AVI-Stream. Ein Audiostream kann auch mit dem AVI Mux-Filter verbunden werden. In diesem Fall verwebt der Mux die beiden Streams. Der [File Writer-Filter](file-writer-filter.md) schreibt den AVI-Stream auf den Datenträger.

Um das Diagramm zu erstellen, rufen Sie zunächst die [**ICaptureGraphBuilder2::SetOutputFileName-Methode**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename) wie folgt auf:


```C++
IBaseFilter *pMux;
hr = pBuild->SetOutputFileName(
    &MEDIASUBTYPE_Avi,  // Specifies AVI for the target file.
    L"C:\\Example.avi", // File name.
    &pMux,              // Receives a pointer to the mux.
    NULL);              // (Optional) Receives a pointer to the file sink.
```



Der erste Parameter gibt den Dateityp an – in diesem Fall AVI. Der zweite Parameter gibt den Dateinamen an. Für AVI erstellt die SetOutputFileName-Methode den AVI Mux-Filter und den File Writer-Filter zusammen und fügt sie dem Diagramm hinzu. Außerdem wird der Dateiname für den File Writer-Filter festgelegt, indem die [**IFileSinkFilter::SetFileName-Methode**](/windows/desktop/api/Strmif/nf-strmif-ifilesinkfilter-setfilename) aufgerufen wird, und die beiden Filter werden miteinander verknüpft. Die -Methode gibt einen Zeiger auf den AVI Mux im dritten Parameter zurück. Optional wird im vierten Parameter ein Zeiger auf die [**IFileSinkFilter-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter) zurückgegeben. Wenn Sie diese Schnittstelle nicht benötigen, können Sie diesen Parameter auf **NULL** festlegen, wie im vorherigen Beispiel gezeigt.

Rufen Sie als Nächstes die [**ICaptureGraphBuilder2::RenderStream-Methode**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) auf, um den Erfassungsfilter wie folgt mit DER AVI Mux zu verbinden:


```C++
hr = pBuild->RenderStream(
    &PIN_CATEGORY_CAPTURE, // Pin category.
    &MEDIATYPE_Video,      // Media type.
    pCap,                  // Capture filter.
    NULL,                  // Intermediate filter (optional).
    pMux);                 // Mux or file sink filter.

// Release the mux filter.
pMux->Release();
```



Der erste Parameter gibt die Pinkategorie an, bei der es sich um PIN \_ CATEGORY CAPTURE für die Erfassung \_ handelt. Der zweite Parameter gibt den Medientyp an. Der dritte Parameter ist ein Zeiger auf die [**IBaseFilter-Schnittstelle des Erfassungsfilters.**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) Der vierte Parameter ist optional. Sie können den Videostream über einen Zwischenfilter wie einen Encoder routen, bevor Sie ihn an den Mux-Filter übergeben. Legen Sie andernfalls diesen Parameter auf **NULL** fest, wie im vorherigen Beispiel gezeigt. Der fünfte Parameter ist der Zeiger auf den Muxfilter. Dieser Zeiger wird durch Aufrufen der SetOutputFileName-Methode erhalten.

Um Audio zu erfassen, rufen Sie RenderStream mit dem Medientyp MEDIATYPE \_ Audio auf. Wenn Sie Audio- und Videodaten von zwei separaten Geräten erfassen, ist es eine gute Idee, den Audiostream zum Masterstream zu machen. Dies hilft, Abweichungen zwischen den beiden Streams zu verhindern, da der AVI Mux-Filter die Wiedergaberate im Videostream an den Audiostream an passt. Rufen Sie zum Festlegen des Masterstreams die [**IConfigAviMux::SetMasterStream-Methode**](/windows/desktop/api/Strmif/nf-strmif-iconfigavimux-setmasterstream) für den AVI Mux-Filter auf:


```C++
IConfigAviMux *pConfigMux = NULL;
hr = pMux->QueryInterface(IID_IConfigAviMux, (void**)&pConfigMux);
if (SUCCEEDED(hr))
{
    pConfigMux->SetMasterStream(1);
    pConfigMux->Release();
}
```



Der Parameter für SetMasterStream ist die Streamnummer, die durch die Reihenfolge bestimmt wird, in der Sie RenderStream aufrufen. Wenn Sie renderStream beispielsweise zuerst für Video und dann für Audio aufrufen, ist das Video Stream 0 und das Audio Stream 1.

Sie können auch festlegen, wie der AVI Mux-Filter die Audio- und Videostreams überlagert, indem Sie die [**IConfigInterleaving::p ut \_ Mode-Methode**](/windows/desktop/api/Strmif/nf-strmif-iconfiginterleaving-put_mode) aufrufen.


```C++
IConfigInterleaving *pInterleave = NULL;
hr = pMux->QueryInterface(IID_IConfigInterleaving, (void**)&pInterleave);
if (SUCCEEDED(hr))
{
    pInterleave->put_Mode(INTERLEAVE_CAPTURE);
    pInterleave->Release();
}
```



Mit dem INTERLEAVE CAPTURE-Flag führt der AVI Mux eine Überlappung mit einer Rate durch, die \_ für die Videoaufnahme geeignet ist. Sie können auch INTERLEAVE NONE verwenden, was bedeutet, dass keine Überlappung möglich ist. Der AVI Mux schreibt die Daten einfach in der Reihenfolge, in der \_ sie eintreffen. Das INTERLEAVE FULL-Flag bedeutet, dass der AVI Mux eine vollständige Überlappung ausführt. Dieser Modus eignet sich jedoch weniger für die Videoaufnahme, da er den überhebbarsten \_ erfordert.

Codieren des Videostreams

Sie können den Videostream codieren, indem Sie einen Encoderfilter zwischen dem Erfassungsfilter und dem AVI Mux-Filter einfügen. Verwenden Sie [den Systemgeräte-Enumerator](system-device-enumerator.md) oder die [Filterzuordnung,](filter-mapper.md) um einen Encoderfilter auszuwählen. (Weitere Informationen finden Sie unter [Aufzählen von Geräten und Filtern](enumerating-devices-and-filters.md).)

Geben Sie den Encoderfilter als vierten Parameter für RenderStream an, der im folgenden Beispiel fett dargestellt wird:


```C++
IBaseFilter *pEncoder;
/* Create the encoder filter (not shown). */
// Add it to the filter graph.
pGraph->AddFilter(pEncoder, L"Encoder");

/* Call SetOutputFileName as shown previously. */

// Render the stream.
hr = pBuild->RenderStream(&PIN_CATEGORY_CAPTURE, &MEDIATYPE_Video, 
    pCap, 
pEncoder, pMux);
pEncoder->Release();
```



Der Encoderfilter unterstützt möglicherweise [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) oder andere Schnittstellen zum Festlegen der Codierungsparameter. Eine Liste der möglichen Schnittstellen finden Sie unter [Dateicodierungs- und Decodierungsschnittstellen.](file-encoding-and-decoding-interfaces.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erfassen von Videos in einer Datei](capturing-video-to-a-file.md)
</dt> </dl>

 

 



