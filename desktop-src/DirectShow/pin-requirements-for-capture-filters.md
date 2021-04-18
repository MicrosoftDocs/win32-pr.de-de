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
# <a name="pin-requirements-for-capture-filters"></a>PIN-Anforderungen für Erfassungs Filter

In diesem Thema werden die Anforderungen für die Implementierung einer Ausgabepin für einen DirectShow-Erfassungs Filter beschrieben.

## <a name="pin-name"></a>Pin-Name

Sie können eine PIN mit einem beliebigen Namen versehen. Wenn der PIN-Name mit dem Tildezeichen (~) beginnt, wird diese PIN vom Filter Diagramm-Manager nicht automatisch renderserver, wenn eine Anwendung [**igraphbuilder:: RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile)aufruft. Wenn der Filter beispielsweise über eine Erfassungs-PIN und eine Vorschau-Pin verfügt, können Sie Sie mit "~ Capture" bzw. "Preview" benennen. Wenn eine Anwendung diesen Filter in einem Diagramm rendert, stellt die Vorschau-Pin eine Verbindung mit dem Standard-Renderer her, und es wird keine Verbindung mit der Erfassungs-Pin hergestellt, was ein vernünftiges Standardverhalten ist. Dies gilt auch für Pins, die Informationsdaten liefern, die nicht gerendert werden sollen, oder für Pins, für die benutzerdefinierte Eigenschaften festgelegt werden müssen. Beachten Sie, dass Pins mit dem Tilde (~)-Präfix weiterhin manuell von der Anwendung verbunden werden können.

## <a name="pin-category"></a>PIN-Kategorie

Ein Erfassungs Filter hat immer eine Aufzeichnungs-PIN und verfügt möglicherweise über eine Vorschau-PIN. Einige Erfassungs Filter verfügen möglicherweise über andere Ausgabe Pins, um andere Arten von Daten, z. b. Steuerungsinformationen, bereitzustellen. Jede Ausgabepin muss die Schnittstelle " [**ikspropertyset**](ikspropertyset.md) " verfügbar machen. Anwendungen verwenden diese Schnittstelle, um die PIN-Kategorie zu bestimmen. Die PIN gibt in der Regel entweder Pin \_ Category \_ Capture oder PIN \_ Category \_ Preview zurück. Weitere Informationen finden Sie unter [PIN-Eigenschaften Satz](pin-property-set.md).

Im folgenden Beispiel wird gezeigt, wie " [**ikspropertyset**](ikspropertyset.md) " implementiert wird, um die PIN-Kategorie für eine Aufzeichnungs-Pin zurückzugeben:


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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Schreiben von Erfassungs Filtern](writing-capture-filters.md)
</dt> </dl>

 

 



