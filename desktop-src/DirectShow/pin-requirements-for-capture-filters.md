---
description: In diesem Thema werden die Anforderungen für die Implementierung einer Ausgabepin für einen DirectShow-Erfassungs Filter beschrieben.
ms.assetid: cb9cda1c-efa2-4abb-934b-21ba8cb80f30
title: PIN-Anforderungen für Erfassungs Filter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2a97d3e5c0f7fe0f5a9a341899651685df1cdd3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106344160"
---
# <a name="pin-requirements-for-capture-filters"></a><span data-ttu-id="b4474-103">PIN-Anforderungen für Erfassungs Filter</span><span class="sxs-lookup"><span data-stu-id="b4474-103">Pin Requirements for Capture Filters</span></span>

<span data-ttu-id="b4474-104">In diesem Thema werden die Anforderungen für die Implementierung einer Ausgabepin für einen DirectShow-Erfassungs Filter beschrieben.</span><span class="sxs-lookup"><span data-stu-id="b4474-104">This topic describes the requirements for implementing an output pin on a DirectShow capture filter.</span></span>

## <a name="pin-name"></a><span data-ttu-id="b4474-105">Pin-Name</span><span class="sxs-lookup"><span data-stu-id="b4474-105">Pin Name</span></span>

<span data-ttu-id="b4474-106">Sie können eine PIN mit einem beliebigen Namen versehen.</span><span class="sxs-lookup"><span data-stu-id="b4474-106">You can give a pin any name.</span></span> <span data-ttu-id="b4474-107">Wenn der PIN-Name mit dem Tildezeichen (~) beginnt, wird diese PIN vom Filter Diagramm-Manager nicht automatisch renderserver, wenn eine Anwendung [**igraphbuilder:: RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile)aufruft.</span><span class="sxs-lookup"><span data-stu-id="b4474-107">If the pin name begins with the tilde (~) character, the Filter Graph Manager does not automatically render that pin when an application calls [**IGraphBuilder::RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile).</span></span> <span data-ttu-id="b4474-108">Wenn der Filter beispielsweise über eine Erfassungs-PIN und eine Vorschau-Pin verfügt, können Sie Sie mit "~ Capture" bzw. "Preview" benennen.</span><span class="sxs-lookup"><span data-stu-id="b4474-108">For example, if the filter has a capture pin and a preview pin, you might name them "~Capture" and "Preview," respectively.</span></span> <span data-ttu-id="b4474-109">Wenn eine Anwendung diesen Filter in einem Diagramm rendert, stellt die Vorschau-Pin eine Verbindung mit dem Standard-Renderer her, und es wird keine Verbindung mit der Erfassungs-Pin hergestellt, was ein vernünftiges Standardverhalten ist.</span><span class="sxs-lookup"><span data-stu-id="b4474-109">If an application renders that filter in a graph, the preview pin will connect to its default renderer, and nothing will connect to the capture pin, which is a reasonable default behavior.</span></span> <span data-ttu-id="b4474-110">Dies gilt auch für Pins, die Informationsdaten liefern, die nicht gerendert werden sollen, oder für Pins, für die benutzerdefinierte Eigenschaften festgelegt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="b4474-110">This can also apply to pins that deliver informational data that is not meant to be rendered, or pins that need custom properties set.</span></span> <span data-ttu-id="b4474-111">Beachten Sie, dass Pins mit dem Tilde (~)-Präfix weiterhin manuell von der Anwendung verbunden werden können.</span><span class="sxs-lookup"><span data-stu-id="b4474-111">Note that pins with the tilde (~) prefix can still be connected manually by the application.</span></span>

## <a name="pin-category"></a><span data-ttu-id="b4474-112">PIN-Kategorie</span><span class="sxs-lookup"><span data-stu-id="b4474-112">Pin Category</span></span>

<span data-ttu-id="b4474-113">Ein Erfassungs Filter hat immer eine Aufzeichnungs-PIN und verfügt möglicherweise über eine Vorschau-PIN.</span><span class="sxs-lookup"><span data-stu-id="b4474-113">A capture filter always has a capture pin, and might have a preview pin.</span></span> <span data-ttu-id="b4474-114">Einige Erfassungs Filter verfügen möglicherweise über andere Ausgabe Pins, um andere Arten von Daten, z. b. Steuerungsinformationen, bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="b4474-114">Some capture filters might have other output pins, to deliver other types of data, such as control information.</span></span> <span data-ttu-id="b4474-115">Jede Ausgabepin muss die Schnittstelle " [**ikspropertyset**](ikspropertyset.md) " verfügbar machen.</span><span class="sxs-lookup"><span data-stu-id="b4474-115">Each output pin must expose the [**IKsPropertySet**](ikspropertyset.md) interface.</span></span> <span data-ttu-id="b4474-116">Anwendungen verwenden diese Schnittstelle, um die PIN-Kategorie zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="b4474-116">Applications use this interface to determine the pin category.</span></span> <span data-ttu-id="b4474-117">Die PIN gibt in der Regel entweder Pin \_ Category \_ Capture oder PIN \_ Category \_ Preview zurück.</span><span class="sxs-lookup"><span data-stu-id="b4474-117">The pin typically returns either PIN\_CATEGORY\_CAPTURE or PIN\_CATEGORY\_PREVIEW.</span></span> <span data-ttu-id="b4474-118">Weitere Informationen finden Sie unter [PIN-Eigenschaften Satz](pin-property-set.md).</span><span class="sxs-lookup"><span data-stu-id="b4474-118">For more information, see [Pin Property Set](pin-property-set.md).</span></span>

<span data-ttu-id="b4474-119">Im folgenden Beispiel wird gezeigt, wie " [**ikspropertyset**](ikspropertyset.md) " implementiert wird, um die PIN-Kategorie für eine Aufzeichnungs-Pin zurückzugeben:</span><span class="sxs-lookup"><span data-stu-id="b4474-119">The following example shows how to implement [**IKsPropertySet**](ikspropertyset.md) to return the pin category on a capture pin:</span></span>


```C++
// Set: Cannot set any properties.
HRESULT CMyCapturePin::Set(REFGUID guidPropSet, DWORD dwID,
    void *pInstanceData, DWORD cbInstanceData, void *pPropData, 
    DWORD cbPropData)
{
    return E_NOTIMPL;
}

// Get: Return the pin category (our only property). 
HRESULT CMyCapturePin::Get(
    REFGUID guidPropSet,   // Which property set.
    DWORD dwPropID,        // Which property in that set.
    void *pInstanceData,   // Instance data (ignore).
    DWORD cbInstanceData,  // Size of the instance data (ignore).
    void *pPropData,       // Buffer to receive the property data.
    DWORD cbPropData,      // Size of the buffer.
    DWORD *pcbReturned     // Return the size of the property.
)
{
    if (guidPropSet != AMPROPSETID_Pin) 
        return E_PROP_SET_UNSUPPORTED;
    if (dwPropID != AMPROPERTY_PIN_CATEGORY)
        return E_PROP_ID_UNSUPPORTED;
    if (pPropData == NULL && pcbReturned == NULL)
        return E_POINTER;
    if (pcbReturned)
        *pcbReturned = sizeof(GUID);
    if (pPropData == NULL)  // Caller just wants to know the size.
        return S_OK;
    if (cbPropData < sizeof(GUID)) // The buffer is too small.
        return E_UNEXPECTED;
    *(GUID *)pPropData = PIN_CATEGORY_CAPTURE;
    return S_OK;
}

// QuerySupported: Query whether the pin supports the specified property.
HRESULT CMyCapturePin::QuerySupported(REFGUID guidPropSet, DWORD dwPropID,
    DWORD *pTypeSupport)
{
    if (guidPropSet != AMPROPSETID_Pin)
        return E_PROP_SET_UNSUPPORTED;
    if (dwPropID != AMPROPERTY_PIN_CATEGORY)
        return E_PROP_ID_UNSUPPORTED;
    if (pTypeSupport)
        // We support getting this property, but not setting it.
        *pTypeSupport = KSPROPERTY_SUPPORT_GET; 
    return S_OK;
}
```



## <a name="related-topics"></a><span data-ttu-id="b4474-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b4474-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b4474-121">Schreiben von Erfassungs Filtern</span><span class="sxs-lookup"><span data-stu-id="b4474-121">Writing Capture Filters</span></span>](writing-capture-filters.md)
</dt> </dl>

 

 



