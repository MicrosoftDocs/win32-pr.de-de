---
description: In diesem Thema werden die Anforderungen für die Implementierung eines Ausgabepins für einen DirectShow-Erfassungsfilter beschrieben.
ms.assetid: cb9cda1c-efa2-4abb-934b-21ba8cb80f30
title: Anforderungen für Erfassungsfilter anheften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e72c74f06970bf6124d0e5dffea458bb41bcd0a19db44acc71a51615aa2fee8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119316110"
---
# <a name="pin-requirements-for-capture-filters"></a>Anforderungen für Erfassungsfilter anheften

In diesem Thema werden die Anforderungen für die Implementierung eines Ausgabepins für einen DirectShow-Erfassungsfilter beschrieben.

## <a name="pin-name"></a>Pin-Name

Sie können einen beliebigen Namen für eine Stecknadel vergeben. Wenn der Pinname mit dem Tildezeichen (~) beginnt, rendert der Filter Graph Manager diesen Pin nicht automatisch, wenn eine Anwendung [**IGraphBuilder::RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile)aufruft. Wenn der Filter beispielsweise über einen Erfassungspin und einen Vorschaupin verfügt, können Sie ihnen den Namen "~Capture" bzw. "Preview" geben. Wenn eine Anwendung diesen Filter in einem Diagramm rendert, stellt der Vorschaupin eine Verbindung mit dem Standardrenderer her, und es wird keine Verbindung mit dem Erfassungspin hergestellt. Dies ist ein angemessenes Standardverhalten. Dies kann auch für Pins gelten, die Informationsdaten liefern, die nicht gerendert werden sollen, oder für Stecknadeln, für die benutzerdefinierte Eigenschaften festgelegt werden müssen. Beachten Sie, dass Stecknadeln mit dem Tildepräfix (~) weiterhin manuell von der Anwendung verbunden werden können.

## <a name="pin-category"></a>Kategorie anheften

Ein Erfassungsfilter verfügt immer über einen Erfassungspin und kann über einen Vorschaupin verfügen. Einige Erfassungsfilter verfügen möglicherweise über andere Ausgabepins, um andere Arten von Daten bereitzustellen, z. B. Steuerelementinformationen. Jeder Ausgabepin muss die [**IKsPropertySet-Schnittstelle**](ikspropertyset.md) verfügbar machen. Anwendungen verwenden diese Schnittstelle, um die Stecknadelkategorie zu bestimmen. Der Pin gibt in der Regel entweder PIN \_ CATEGORY CAPTURE oder PIN CATEGORY PREVIEW \_ \_ \_ zurück. Weitere Informationen finden Sie unter [Anheften von Eigenschaftensatz.](pin-property-set.md)

Das folgende Beispiel zeigt, wie [**IKsPropertySet**](ikspropertyset.md) implementiert wird, um die Pinkategorie auf einem Erfassungspin zurückzugeben:


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

[Schreiben von Erfassungsfiltern](writing-capture-filters.md)
</dt> </dl>

 

 



