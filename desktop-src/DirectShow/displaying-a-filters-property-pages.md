---
description: Anzeigen der Eigenschaften Seiten eines Filters
ms.assetid: 4a5f6938-7b33-4350-b8fa-cf78c5c44bcd
title: Anzeigen der Eigenschaften Seiten eines Filters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0845a12b73363dc6ed93654439fd31826bf9cfc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392369"
---
# <a name="displaying-a-filters-property-pages"></a>Anzeigen der Eigenschaften Seiten eines Filters

Eine Eigenschaften Seite ist eine Möglichkeit für einen Filter, um Eigenschaften zu unterstützen, die vom Benutzer festgelegt werden können. In diesem Artikel wird beschrieben, wie die Eigenschaften Seiten eines Filters in einer Anwendung angezeigt werden. Weitere Informationen zu Eigenschaften Seiten finden Sie in der Platform SDK-Dokumentation.

> [!Note]  
> Obwohl viele der mit DirectShow bereitgestellten Filtereigenschaften Seiten unterstützen, sind Sie für das Debuggen vorgesehen und werden für die Anwendungs Verwendung nicht empfohlen. In den meisten Fällen wird die entsprechende Funktionalität über eine benutzerdefinierte Schnittstelle für den Filter bereitgestellt. Eine Anwendung sollte diese Filterprogramm gesteuert steuern, anstatt ihre Eigenschaften Seiten für Benutzer verfügbar zu machen.

 

Filter mit Eigenschaften Seiten machen die **ISpecifyPropertyPages** -Schnittstelle verfügbar. Um zu ermitteln, ob ein Filter eine Eigenschaften Seite definiert, Fragen Sie mithilfe von **QueryInterface** den Filter für diese Schnittstelle ab.

Wenn Sie eine Instanz eines Filters (durch Aufrufen von **CoCreateInstance**) direkt erstellt haben, verfügen Sie bereits über einen Zeiger auf den Filter. Wenn dies nicht der Fall ist, können Sie die Filter im Diagramm mithilfe der [**ifiltergraph:: enumfilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-enumfilters) -Methode auflisten. Weitere Informationen finden Sie unter Auflisten von [Objekten in einem Filter Diagramm](enumerating-objects-in-a-filter-graph.md).

Sobald Sie über den **ISpecifyPropertyPages** -Schnittstellen Zeiger verfügen, rufen Sie die Eigenschaften Seiten des Filters ab, indem Sie die **ISpecifyPropertyPages:: GetPages** -Methode aufrufen. Diese Methode füllt ein Gezähltes Array von global eindeutigen Bezeichnern (GUIDs) mit der Klassen-ID (CLSID) der einzelnen Eigenschaften Seiten. Ein Gezähltes Array wird durch eine **cauuid** -Struktur definiert, die Sie zuordnen müssen, aber nicht initialisieren müssen. Die **GetPages** -Methode ordnet das Array zu, das im **pelems** -Member der **cauuid** -Struktur enthalten ist. Wenn Sie den Vorgang abgeschlossen haben, können Sie das Array freigeben, indem Sie die **CoTaskMemFree** -Funktion aufrufen.

Die **OleCreatePropertyFrame** -Funktion bietet eine einfache Möglichkeit, die Eigenschaften Seiten in einem modalen Dialogfeld anzuzeigen.


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

 

 



