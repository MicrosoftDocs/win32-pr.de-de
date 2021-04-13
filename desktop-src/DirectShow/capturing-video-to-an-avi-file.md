---
description: Aufzeichnen von Videos in einer AVI-Datei
ms.assetid: 0f5f4a82-4a2e-4c48-b201-bda641cb8619
title: Aufzeichnen von Videos in einer AVI-Datei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86504e9ce149f495e1ea31664f56382340d33887
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104568390"
---
# <a name="capturing-video-to-an-avi-file"></a>Aufzeichnen von Videos in einer AVI-Datei

Die folgende Abbildung zeigt das einfachste mögliche Diagramm für die Erfassung von Videos in einer AVI-Datei.

![AVI-Video Erfassungs Diagramm](images/vidcap02.png)

Der [AVI MUX](avi-mux-filter.md) -Filter nimmt den Videostream aus der Erfassungs-PIN und verpackt ihn in einen AVI-Stream. Ein Audiodatenstrom kann auch mit dem AVI MUX-Filter verbunden werden. in diesem Fall würde die MUX die beiden Streams überlassen. Der [dateiwriter](file-writer-filter.md) -Filter schreibt den AVI-Stream auf den Datenträger.

Um das Diagramm zu erstellen, rufen Sie zunächst die [**ICaptureGraphBuilder2:: setoutputfilename**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename) -Methode wie folgt auf:


```C++
IBaseFilter *pMux;
hr = pBuild->SetOutputFileName(
    &MEDIASUBTYPE_Avi,  // Specifies AVI for the target file.
    L"C:\\Example.avi", // File name.
    &pMux,              // Receives a pointer to the mux.
    NULL);              // (Optional) Receives a pointer to the file sink.
```



Der erste Parameter gibt den Dateityp an – in diesem Fall AVI. Der zweite Parameter gibt den Dateinamen an. Für AVI erstellt die setoutputfilename-Methode den AVI MUX-Filter und den dateiwriter-Filter und fügt Sie dem Diagramm hinzu. Außerdem wird der Dateiname im Datei Schreiber Filter festgelegt, indem die [**ifilesink Filter:: setFileName**](/windows/desktop/api/Strmif/nf-strmif-ifilesinkfilter-setfilename) -Methode aufgerufen und die beiden Filter miteinander verbunden werden. Die-Methode gibt einen Zeiger auf die AVI MUX im dritten Parameter zurück. Optional wird ein Zeiger auf die [**ifilesinkfilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter) -Schnittstelle im vierten Parameter zurückgegeben. Wenn Sie diese Schnittstelle nicht benötigen, können Sie diesen Parameter auf **null** festlegen, wie im vorherigen Beispiel gezeigt.

Als nächstes wird die [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) -Methode aufgerufen, um den Erfassungs Filter wie folgt mit der AVI-MUX-Datei zu verbinden:


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



Der erste Parameter gibt die PIN-Kategorie an, die PIN- \_ kategorieerfassung \_ für die Erfassung ist. Der zweite Parameter gibt den Medientyp an. Der dritte Parameter ist ein Zeiger auf die [**ibasefilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) -Schnittstelle des Erfassungs Filters. Der vierte Parameter ist optional. Sie können den Videostream über einen zwischen Filter, z. b. einen Encoder, weiterleiten, bevor Sie ihn an den MUX-Filter übergeben. Andernfalls legen Sie diesen Parameter auf **null** fest, wie im vorherigen Beispiel gezeigt. Der fünfte Parameter ist der Zeiger auf den MUX-Filter. Dieser Zeiger wird durch Aufrufen der setoutputfilename-Methode abgerufen.

Um Audiodaten aufzuzeichnen, nennen Sie RenderStream mit dem Medientyp MediaType \_ -Audiodatei. Wenn Sie Audiodaten und Videos von zwei separaten Geräten erfassen, empfiehlt es sich, den Audiostream in den Masterstream zu legen. Dadurch wird die Abweichung zwischen den beiden Streams verhindert, da der AVI MUX-Filter die Wiedergabe Rate für den Videostream entsprechend dem Audiostream anpasst. Um den Masterstream festzulegen, müssen Sie die [**iconfigavimux:: setmasterstream**](/windows/desktop/api/Strmif/nf-strmif-iconfigavimux-setmasterstream) -Methode für den AVI MUX-Filter aufrufen:


```C++
IConfigAviMux *pConfigMux = NULL;
hr = pMux->QueryInterface(IID_IConfigAviMux, (void**)&pConfigMux);
if (SUCCEEDED(hr))
{
    pConfigMux->SetMasterStream(1);
    pConfigMux->Release();
}
```



Der Parameter für setmasterstream ist die streamnummer, die durch die Reihenfolge bestimmt wird, in der Sie RenderStream aufrufen. Wenn Sie z. b. RenderStream zuerst für Video und dann für Audiodaten aufzurufen, ist das Video Stream 0 und das Audioformat Stream 1.

Sie können auch festlegen, wie der AVI MUX-Filter die Audio-und Videostreams interverlässt, indem Sie die [**iconfiginterleaving::p UT \_ Mode**](/windows/desktop/api/Strmif/nf-strmif-iconfiginterleaving-put_mode) -Methode aufrufen.


```C++
IConfigInterleaving *pInterleave = NULL;
hr = pMux->QueryInterface(IID_IConfigInterleaving, (void**)&pInterleave);
if (SUCCEEDED(hr))
{
    pInterleave->put_Mode(INTERLEAVE_CAPTURE);
    pInterleave->Release();
}
```



Mit dem Interleave- \_ Erfassungs Kennzeichen führt der AVI MUX eine Überlappungs Rate mit einer Rate aus, die für die Video Erfassung geeignet ist. Sie können auch Interleave \_ None verwenden, was bedeutet, dass kein Austausch erfolgt – die AVI-MUX schreibt die Daten einfach in der Reihenfolge, in der Sie ankommt. Das Interleave- \_ vollständige Flag bedeutet, dass die AVI-MUX vollständige überlappende Vorgänge ausführt. dieser Modus ist jedoch für die Video Erfassung weniger geeignet, da er die am meisten übergefasste erfordert.

Codieren des Video Datenstroms

Sie können den Videostream codieren, indem Sie einen encoderfilter zwischen dem Erfassungs Filter und dem AVI MUX-Filter einfügen. Verwenden Sie den [Enumerator für System Geräte](system-device-enumerator.md) oder den [Filter-Mapper](filter-mapper.md) , um einen encoderfilter auszuwählen. (Weitere Informationen finden Sie unter Auflisten von [Geräten und Filtern](enumerating-devices-and-filters.md).)

Geben Sie den encoderfilter als vierten Parameter für RenderStream an, wie im folgenden Beispiel fett dargestellt:


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



Der Encoder-Filter unterstützt möglicherweise [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) oder andere Schnittstellen zum Festlegen der Codierungs Parameter. Eine Liste möglicher Schnittstellen finden Sie unter [Schnittstellen für die Datei Codierung und-Decodierung](file-encoding-and-decoding-interfaces.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Aufzeichnen von Videos in einer Datei](capturing-video-to-a-file.md)
</dt> </dl>

 

 



