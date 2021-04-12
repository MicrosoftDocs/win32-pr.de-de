---
description: Aufzeichnen von Videos in einer Windows Media-Datei
ms.assetid: cc23bfce-34b9-4976-8602-e0602c7da2af
title: Aufzeichnen von Videos in einer Windows Media-Datei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6442c1cf3751beac8d4eba751452d9573e9eede
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "104218996"
---
# <a name="capturing-video-to-a-windows-media-file"></a>Aufzeichnen von Videos in einer Windows Media-Datei

Um Videos aufzuzeichnen und in eine Windows Media Video Datei (WMV) zu codieren, verbinden Sie die Erfassungs-PIN mit dem [WM-ASF-Writer](wm-asf-writer-filter.md) -Filter, wie im folgenden Diagramm dargestellt.

![Windows Media Capture-Diagramm](images/vidcap03.png)

Die einfachste Möglichkeit zum Erstellen dieses Diagramms besteht darin, mediasubtype \_ ASF in der [**ICaptureGraphBuilder2:: setoutputfilename**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename) -Methode anzugeben:


```C++
IBaseFilter* pASFWriter = 0;
hr = pBuild->SetOutputFileName(
    &MEDIASUBTYPE_Asf,   // Create a Windows Media file.
    L"C:\\VidCap.wmv",   // File name.
    &pASFWriter,         // Receives a pointer to the filter.
    NULL);  // Receives an IFileSinkFilter interface pointer (optional).
```



Der Wert mediasubtype \_ ASF weist den Erfassungs Diagramm-Generator an, den WM-ASF-Writer-Filter als Datei-Senke zu verwenden. Mit dem Erfassungs Diagramm-Generator wird der Filter erstellt, dem Diagramm hinzugefügt und [**ifilesink Filter:: setFileName**](/windows/desktop/api/Strmif/nf-strmif-ifilesinkfilter-setfilename) aufgerufen, um den Namen der Ausgabedatei festzulegen. Er gibt einen Zeiger auf den Filter als ausgehenden Parameter zurück (


```
pASFWriter
```



im vorherigen Beispiel).

Verwenden Sie die [**iconfigasfwriter**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iconfigasfwriter) -Schnittstelle auf dem WM-ASF-Writer, um das Windows Media-Profil festzulegen. Dies müssen Sie tun, bevor Sie eine Verbindung mit Pins im WM-ASF-Writer herstellen.


```C++
IConfigAsfWriter *pConfig = 0;
hr = pASFWriter->QueryInterface(IID_IConfigAsfWriter, (void**)&pConfig);
if (SUCCEEDED(hr))
{
     // Configure the ASF Writer filter.
    pConfig->Release();
}
```



Weitere Informationen zum Festlegen des Profils finden Sie unter [Erstellen von ASF-Dateien in DirectShow](creating-asf-files-in-directshow.md).

Nennen Sie [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) , um den Erfassungs Filter mit dem ASF-Writer zu verbinden:


```C++
hr = pBuild->RenderStream(
    &PIN_CATEGORY_CAPTURE,   // Capture pin.
    &MEDIATYPE_Video,        // Video. Use MEDIATYPE_Audio for audio.
    pCap,                    // Pointer to the capture filter. 
    0, 
    pASFWriter);             // Pointer to the sink filter (ASF Writer).
```



Jede Eingabe-PIN für den WM-ASF-Writer-Filter entspricht einem Stream im Windows Media-Profil. Sie müssen jede Pin verbinden, damit der Inhalt der Datei mit dem Profil übereinstimmt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Aufzeichnen von Videos in einer Datei](capturing-video-to-a-file.md)
</dt> </dl>

 

 



