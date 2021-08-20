---
description: Aufzeichnen von Videos in einer Windows Mediendatei
ms.assetid: cc23bfce-34b9-4976-8602-e0602c7da2af
title: Aufzeichnen von Videos in einer Windows Mediendatei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3268d3a3df4a24c5836dba81f7ef4cf0b872907f09367d3212d27c38c0dd4414
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118158704"
---
# <a name="capturing-video-to-a-windows-media-file"></a>Aufzeichnen von Videos in einer Windows Mediendatei

Um Videos zu erfassen und in eine WMV-Datei (Windows Media Video) zu codieren, verbinden Sie den Aufnahmepin mit dem [WM ASF](wm-asf-writer-filter.md) Writer-Filter, wie im folgenden Diagramm dargestellt.

![Windows-Medienerfassungsdiagramm](images/vidcap03.png)

Die einfachste Möglichkeit zum Erstellen dieses Diagramms besteht darin, MEDIASUBTYPE \_ Asf in der [**ICaptureGraphBuilder2::SetOutputFileName-Methode**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename) zu angeben:


```C++
IBaseFilter* pASFWriter = 0;
hr = pBuild->SetOutputFileName(
    &MEDIASUBTYPE_Asf,   // Create a Windows Media file.
    L"C:\\VidCap.wmv",   // File name.
    &pASFWriter,         // Receives a pointer to the filter.
    NULL);  // Receives an IFileSinkFilter interface pointer (optional).
```



Der Wert MEDIASUBTYPE \_ Asf weist den Capture Graph Builder an, den WM ASF Writer-Filter als Dateisenke zu verwenden. Der Capture Graph Builder erstellt den Filter, fügt ihn dem Diagramm hinzu und ruft [**IFileSinkFilter::SetFileName**](/windows/desktop/api/Strmif/nf-strmif-ifilesinkfilter-setfilename) auf, um den Namen der Ausgabedatei festzulegen. Es gibt einen Zeiger auf den Filter als ausgehenden Parameter zurück (


```
pASFWriter
```



im vorherigen Beispiel).

Verwenden Sie die [**IConfigAsfWriter-Schnittstelle**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iconfigasfwriter) auf dem WM ASF Writer, um das Windows Medienprofil festzulegen. Sie müssen dies tun, bevor Sie an den WM ASF Writer anheften.


```C++
IConfigAsfWriter *pConfig = 0;
hr = pASFWriter->QueryInterface(IID_IConfigAsfWriter, (void**)&pConfig);
if (SUCCEEDED(hr))
{
     // Configure the ASF Writer filter.
    pConfig->Release();
}
```



Weitere Informationen zum Festlegen des Profils finden Sie unter [Erstellen von ASF-Dateien in DirectShow.](creating-asf-files-in-directshow.md)

Rufen Sie [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) auf, um den Erfassungsfilter mit dem ASF Writer zu verbinden:


```C++
hr = pBuild->RenderStream(
    &PIN_CATEGORY_CAPTURE,   // Capture pin.
    &MEDIATYPE_Video,        // Video. Use MEDIATYPE_Audio for audio.
    pCap,                    // Pointer to the capture filter. 
    0, 
    pASFWriter);             // Pointer to the sink filter (ASF Writer).
```



Jeder Eingabepin im WM ASF Writer-Filter entspricht einem Stream im Windows Medienprofil. Sie müssen jede Stecknadel verbinden, damit der Dateiinhalt mit dem Profil übereinstimmt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Aufzeichnen von Videos in einer Datei](capturing-video-to-a-file.md)
</dt> </dl>

 

 



