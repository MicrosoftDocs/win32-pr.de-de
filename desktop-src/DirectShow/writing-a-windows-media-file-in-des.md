---
description: Schreiben einer Windows-Mediendatei in des
ms.assetid: 741ebcbc-62fb-4c7f-845f-a361f5b63f8c
title: Schreiben einer Windows-Mediendatei in des
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0626a3ef609dee87d90a6d3c2caa023e9ac9a29a
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106357155"
---
# <a name="writing-a-windows-media-file-in-des"></a>Schreiben einer Windows-Mediendatei in des

\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein.\]

In diesem Abschnitt wird beschrieben, wie Sie eine Windows Media-Datei mithilfe von [DirectShow-Bearbeitungs Diensten](directshow-editing-services.md) (de) schreiben.

> [!IMPORTANT]
> Verwenden Sie die Smart-Rendering-Engine nicht zum Schreiben von Windows Media-Dateien. Verwenden Sie immer die einfache Renderengine (CLSID- \_ Renderengine).

 

Gehen Sie folgendermaßen vor, um eine Windows Media-Datei zu schreiben:

1.  Aufrufen von **SetSite** für die Rendering-Engine mit einem Zeiger auf den Schlüssel Anbieter.
2.  Erstellen Sie das Front-End des Diagramms. (Siehe [Rendern eines Projekts](rendering-a-project.md).)
3.  Erstellen Sie den [WM-ASF-Writer](wm-asf-writer-filter.md) -Filter, und fügen Sie ihn dem Diagramm hinzu.
4.  Verwenden Sie die [**ifilesink Filter**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter) -Schnittstelle für den WM-ASF-Writer-Filter, um den Dateinamen festzulegen.
5.  Konfigurieren Sie den WM-ASF-Writer für die Verwendung eines Windows Media-Profils. Jedes Profil verfügt über eine vordefinierte Anzahl von Streams. Sie müssen ein Profil auswählen, das den Gruppen im Projekt entspricht.

    Die [**iconfigasfwriter**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iconfigasfwriter) -Schnittstelle enthält verschiedene Methoden zum Festlegen des Profils. Beispielsweise gibt die Methode " **konfigurifisingprofileguid** " ein Systemprofil als GUID an. Oder Sie können Windows Media-Methoden verwenden, um einen **iwmprofile** -Zeiger zu erhalten, und dann [**iconfigasfwriter:: konfigurifisingprofile**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter-configurefilterusingprofile)aufzurufen. Weitere Informationen finden Sie unter [Konfigurieren des ASF-Writers](configuring-the-asf-writer.md).

6.  Verbinden Sie das Front-End mit dem ASF-Writer. Das Front-End des Diagramms enthält eine Ausgabe-PIN für jede Gruppe. Angenommen, Sie haben ein kompatibles Profil angegeben, muss der ASF-Writer über einen passenden Satz von Eingabe Pins verfügen. Verbinden Sie jede Ausgabe-PIN mit der entsprechenden Eingabe-PIN. Die einfachste Möglichkeit hierfür ist die Verwendung der [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) -Methode. Erstellen Sie zunächst eine neue Instanz des [Erfassungs Diagramm](capture-graph-builder.md) -Generators, und initialisieren Sie Sie mit einem Zeiger auf den Filter Graph-Manager:

    ```C++
    ICaptureGraphBuilder2 *pBuild = 0;
    hr = CoCreateInstance(CLSID_CaptureGraphBuilder2, 0, CLSCTX_INPROC_SERVER,
        IID_ICaptureGraphBuilder2, (void**)&pBuild);
    pBuild->SetFiltergraph(pGraph); 
    ```

    

    Rufen Sie als nächstes die Ausgabe-PIN für jede Gruppe ab, indem Sie die Methode " [**irienderengine:: getgroupoutputpin**](irenderengine-getgroupoutputpin.md) " aufrufen. **RenderStream** zum Verbinden der PIN mit dem ASF-Writer aufzurufen:

    ```C++
    long cGroups = 0;
    hr = pTimeline->GetGroupCount(&cGroups);
    for (long i = 0; i < cGroups; i++)
    {
        IPin *pPin;
        hr = pRenderEngine->GetGroupOutputPin(i, &pPin);
        if (SUCCEEDED(hr))
        {
            hr = pBuild->RenderStream(0, 0, pPin, 0, pASF);
        }
        pPin->Release();
    }
    pBuild->Release
    ```

    

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Windows Media mit DirectShow-Bearbeitungs Diensten](using-windows-media-with-directshow-editing-services.md)
</dt> </dl>

 

 



