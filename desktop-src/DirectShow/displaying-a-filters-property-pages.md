---
description: Anzeigen der Eigenschaftenseiten eines Filters
ms.assetid: 4a5f6938-7b33-4350-b8fa-cf78c5c44bcd
title: Anzeigen der Eigenschaftenseiten eines Filters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f0e29654983ee51b98666411a11f7130eb896c380ec754b5576862c313dcbc2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016137"
---
# <a name="displaying-a-filters-property-pages"></a>Anzeigen der Eigenschaftenseiten eines Filters

Eine Eigenschaftenseite ist eine Möglichkeit für einen Filter, Eigenschaften zu unterstützen, die der Benutzer festlegen kann. In diesem Artikel wird beschrieben, wie Die Eigenschaftenseiten eines Filters in einer Anwendung angezeigt werden. Weitere Informationen zu Eigenschaftenseiten finden Sie in der Platform SDK-Dokumentation.

> [!Note]  
> Obwohl viele der mit DirectShow bereitgestellten Filter Eigenschaftenseiten unterstützen, sind sie für Debugzwecke vorgesehen und werden nicht für die Anwendungsnutzung empfohlen. In den meisten Fällen wird die entsprechende Funktionalität über eine benutzerdefinierte Schnittstelle für den Filter bereitgestellt. Eine Anwendung sollte diese Filter programmgesteuert steuern, anstatt ihre Eigenschaftenseiten für Benutzer verfügbar zu machen.

 

Filter mit Eigenschaftenseiten machen die **ISpecifyPropertyPages-Schnittstelle** verfügbar. Um zu bestimmen, ob ein Filter eine Eigenschaftenseite definiert, fragen Sie den Filter für diese Schnittstelle mit **QueryInterface ab.**

Wenn Sie direkt eine Instanz eines Filters erstellt haben (durch Aufrufen von **CoCreateInstance),** verfügen Sie bereits über einen Zeiger auf den Filter. Falls nicht, können Sie die Filter im Diagramm mithilfe der [**IFilterGraph::EnumFilters-Methode**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-enumfilters) aufzählen. Weitere Informationen finden Sie unter [Enumerating Objects in a Filter Graph.](enumerating-objects-in-a-filter-graph.md)

Sobald Sie über den **ISpecifyPropertyPages-Schnittstellenzeiger** verfügen, rufen Sie die Eigenschaftenseiten des Filters ab, indem Sie die **ISpecifyPropertyPages::GetPages-Methode** aufrufen. Diese Methode füllt ein gezähltes Array global eindeutiger Bezeichner (GLOBALLY UNIQUE Identifier, GUIDs) mit dem Klassenbezeichner (CLSID) jeder Eigenschaftenseite auf. Ein gezähltes Array wird durch eine **CAUUID-Struktur** definiert, die Sie zuordnen, aber nicht initialisieren müssen. Die **GetPages-Methode** ordnet das Array zu, das im **pElems-Member** der **CAUUID-Struktur enthalten** ist. Wenn Sie fertig sind, geben Sie das Array frei, indem Sie die **CoTaskMemFree-Funktion** aufrufen.

Die **OleCreatePropertyFrame-Funktion** bietet eine einfache Möglichkeit, die Eigenschaftenseiten in einem modalen Dialogfeld anzuzeigen.


```C++
IBaseFilter *pFilter;
/* Obtain the filter's IBaseFilter interface. (Not shown) */
ISpecifyPropertyPages *pProp;
HRESULT hr = pFilter->QueryInterface(IID_ISpecifyPropertyPages, (void **)&pProp);
if (SUCCEEDED(hr)) 
{
    // Get the filter's name and IUnknown pointer.
    FILTER_INFO FilterInfo;
    hr = pFilter->QueryFilterInfo(&FilterInfo); 
    IUnknown *pFilterUnk;
    pFilter->QueryInterface(IID_IUnknown, (void **)&pFilterUnk);

    // Show the page. 
    CAUUID caGUID;
    pProp->GetPages(&caGUID);
    pProp->Release();
    OleCreatePropertyFrame(
        hWnd,                   // Parent window
        0, 0,                   // Reserved
        FilterInfo.achName,     // Caption for the dialog box
        1,                      // Number of objects (just the filter)
        &pFilterUnk,            // Array of object pointers. 
        caGUID.cElems,          // Number of property pages
        caGUID.pElems,          // Array of property page CLSIDs
        0,                      // Locale identifier
        0, NULL                 // Reserved
    );

    // Clean up.
    pFilterUnk->Release();
    FilterInfo.pGraph->Release(); 
    CoTaskMemFree(caGUID.pElems);
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Grundlegende DirectShow-Aufgaben](basic-directshow-tasks.md)
</dt> </dl>

 

 



