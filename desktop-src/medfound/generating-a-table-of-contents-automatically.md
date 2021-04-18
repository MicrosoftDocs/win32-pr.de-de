---
description: Automatisches Erstellen eines Inhaltsverzeichnisses
ms.assetid: 3acb9c12-0158-4b89-87c4-4abd35ae8c2f
title: Automatisches Erstellen eines Inhaltsverzeichnisses
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22adc4d48ad7f4b1d89a446eb28c25d6011804a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106341160"
---
# <a name="generating-a-table-of-contents-automatically"></a>Automatisches Erstellen eines Inhaltsverzeichnisses

In diesem Thema wird veranschaulicht, wie die Komponente "Inhalts [**Generator**](/previous-versions/ee264297(v=vs.85)) " (TOC Generator) zum automatischen Generieren eines Inhaltsverzeichnisses für eine Videodatei verwendet wird.

Der TOC-Generator ist ein DirectX-Medienobjekt (DMO). Um den TOC-Generator DMO zu verwenden, erstellen Sie ein DirectX-Filter Diagramm, das eine Videodatei als Quelle hat. Fügen Sie den TOC-Generator DMO in das Filter Diagramm ein, und führen Sie das Diagramm aus. Anschließend können Sie das automatisch generierte Inhaltsverzeichnis aus dem TOC-Generator DMO abrufen.

Die Schritte werden im folgenden Verfahren ausführlicher erläutert.

1.  Rufen Sie [**cokreateinstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) auf, um ein Filter Diagramm Objekt (**CLSID \_ Filtergraph**) zu erstellen und eine [**igraphbuilder**](/windows/win32/api/strmif/nn-strmif-igraphbuilder) -Schnittstelle zu erhalten.
2.  Rufen Sie [**cokreateinstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) auf, um ein DMO-Wrapper Filter Objekt (**CLSID \_ dmowrapperfilter**) zu erstellen, und rufen Sie eine [**idmowrapperfilter**](/previous-versions/windows/desktop/api/dmodshow/nn-dmodshow-idmowrapperfilter) -Schnittstelle ab.
3.  Übergeben Sie **CLSID \_ cdecgeneratordmo** an die [**Init**](/previous-versions/windows/desktop/api/dmodshow/nf-dmodshow-idmowrapperfilter-init) -Methode des DMO-Wrapper Filters. Dadurch wird ein TOC-Generator-DMO erstellt und in den DMO-Wrapper Filter umschlossen.
4.  Wenden Sie die [**addFilter**](/windows/win32/api/strmif/nf-strmif-ifiltergraph-addfilter) -Methode der [**igraphbuilder**](/windows/win32/api/strmif/nn-strmif-igraphbuilder) -Schnittstelle an, um den umschließenden TOC-Generator DMO dem Filter Diagramm hinzuzufügen.
    > [!Note]  
    > [**Igraphbuilder**](/windows/win32/api/strmif/nn-strmif-igraphbuilder) erbt von [**ifiltergraph**](/windows/win32/api/strmif/nn-strmif-ifiltergraph).

     

5.  Rufen Sie die [**addsourcefilter**](/windows/win32/api/strmif/nf-strmif-igraphbuilder-addsourcefilter) -Methode der [**igraphbuilder**](/windows/win32/api/strmif/nn-strmif-igraphbuilder) -Schnittstelle auf, um einen Quelle-Filter zu erstellen und ihn dem Diagramm hinzuzufügen.
6.  Auflisten von Pins für den DMO-Wrapper Filter und den Quell Filter. Dies umfasst das Abrufen von [**iumumpins**](/windows/win32/api/strmif/nn-strmif-ienumpins) -Schnittstellen und [**IPin**](/windows/win32/api/strmif/nn-strmif-ipin) -Schnittstellen.
7.  Verbinden Sie den Quell Filter und den Wrapper Filter, indem Sie die [**Connect**](/windows/win32/api/strmif/nf-strmif-igraphbuilder-connect) -Methode Ihrer [**igraphbuilder**](/windows/win32/api/strmif/nn-strmif-igraphbuilder) -Schnittstelle aufrufen.
8.  Vervollständigen Sie das Diagramm, indem Sie die Methode " [**Rendering**](/windows/win32/api/strmif/nf-strmif-igraphbuilder-render) " Ihrer [**igraphbuilder**](/windows/win32/api/strmif/nn-strmif-igraphbuilder) -Schnittstelle aufrufen.
9.  Führen Sie das Diagramm ([**IMediaControl:: Run**](/windows/win32/api/control/nf-control-imediacontrol-run)) aus, und warten Sie, bis es abgeschlossen ist ([**imediaevent:: waitforcompletion**](/windows/win32/api/control/nf-control-imediaevent-waitforcompletion)).
10. Rufen Sie eine [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) -Schnittstelle für den DMO-Filter-Wrapper ab, und rufen Sie den Wert der [**mfpkey \_ tocgenerator \_ tokready**](/previous-versions/ee264297(v=vs.85)) -Eigenschaft ab. Wiederholen Sie dies bei Bedarf, bis das Inhaltsverzeichnis bereit ist.
11. Verwenden Sie die [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) -Schnittstelle zum Aufrufen des Werts der Eigenschaft " [**mfpkey \_ tocgenerator \_ tocobject**](/previous-versions/ee264297(v=vs.85)) ". Diese Eigenschaft ist eine [**IYC**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itoc) -Schnittstelle, die das automatisch generierte Inhaltsverzeichnis darstellt.

Der folgende Code veranschaulicht das Verfahren zum automatischen Erstellen eines Inhaltsverzeichnisses. Der Code verwendet drei Hilfsfunktionen ([**buildgraph**](buildgraph-method-for-generating-a-table-of-contents.md), [**rungraphandwait**](rungraphandwait-method-for-generating-a-table-of-contents.md)und [**gettoc**](gettoc-method-for-generating-a-table-of-contents.md)), die auf anderen Seiten dieser Dokumentation angezeigt werden.


```C++
#include <dshow.h>
#include <dmodshow.h>
#include <wmcodecdsp.h>
#include <dmoreg.h>
#include <propsys.h>
#include <propidl.h>
#include <initguid.h>

HRESULT GetToc(IDMOWrapperFilter* pWrap, IToc** ppToc);
HRESULT RunGraphAndWait(IGraphBuilder* pGraph);
HRESULT BuildGraph(IGraphBuilder* pGraph, IDMOWrapperFilter* pWrap);

WCHAR g_sourceFile[] = L"c:\\experiment\\Seattle.wmv";

void main()
{
   HRESULT hr = E_FAIL;
   hr = CoInitialize(NULL);

   if(SUCCEEDED(hr))
   {
      IGraphBuilder* pBuilder = NULL;
      hr = CoCreateInstance(CLSID_FilterGraph, NULL, CLSCTX_INPROC_SERVER, 
         IID_IGraphBuilder, (VOID**)&pBuilder);

      if(SUCCEEDED(hr))
      {
         IDMOWrapperFilter* pWrap = NULL;
         hr = CoCreateInstance(CLSID_DMOWrapperFilter, NULL, CLSCTX_INPROC, 
            IID_IDMOWrapperFilter, (VOID**)&pWrap);

         if(SUCCEEDED(hr))
         {
            hr = pWrap->Init(CLSID_CTocGeneratorDmo, DMOCATEGORY_VIDEO_EFFECT); 

            if(SUCCEEDED(hr))
            {
               hr = BuildGraph(pBuilder, pWrap);

               if(SUCCEEDED(hr))
               {
                  hr = RunGraphAndWait(pBuilder);

                  if(SUCCEEDED(hr))
                  {
                     IToc* pToc = NULL;
                     hr = GetToc(pWrap, &pToc);

                     if(SUCCEEDED(hr))
                     {
                        // Inspect the table of contents by calling IToc methods.

                        pToc->Release();
                        pToc = NULL;
                     }
                  }
               }
            }

            pWrap->Release();
            pWrap = NULL;
         }

         pBuilder->Release();
         pBuilder = NULL;
      }

      CoUninitialize();
   }
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Buildgraph-Funktion zum Erstellen eines Inhaltsverzeichnisses](buildgraph-method-for-generating-a-table-of-contents.md)
</dt> <dt>

[Getdec-Funktion zum Erstellen eines Inhaltsverzeichnisses](gettoc-method-for-generating-a-table-of-contents.md)
</dt> <dt>

[Rungraphandwait-Funktion zum Erstellen eines Inhaltsverzeichnisses](rungraphandwait-method-for-generating-a-table-of-contents.md)
</dt> <dt>

[Programmier Handbuch für das Inhaltsverzeichnis des Parsers](toc-parser-programming-guide.md)
</dt> </dl>

 

 
