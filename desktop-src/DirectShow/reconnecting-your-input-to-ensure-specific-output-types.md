---
description: Erneutes Verbinden ihrer Eingabe, um bestimmte Ausgabetypen sicherzustellen
ms.assetid: c83d002e-59bf-4d03-9917-e39ceab9a4ce
title: Erneutes Verbinden ihrer Eingabe, um bestimmte Ausgabetypen sicherzustellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 299d8aa400619043cc0d79242e35065ac4fc8490aad4972a33be6aea8fc4e7b7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119747310"
---
# <a name="reconnecting-your-input-to-ensure-specific-output-types"></a>Erneutes Verbinden ihrer Eingabe, um bestimmte Ausgabetypen sicherzustellen

Filter implementieren die [**IAMStreamConfig::SetFormat-Methode,**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-setformat) um das Audio- oder Videoformat festzulegen, bevor die Pins des Filters verbunden werden. Wenn der Ausgabepin bereits verbunden ist und Sie einen neuen Typ angeben können, stellen Sie die Verbindung mit dem Pin wieder her. Dies gilt jedoch nur, wenn der andere Filter den neuen Typ akzeptieren kann. Wenn der andere Filter den Medientyp nicht akzeptieren kann, schlägt der Aufruf von **SetFormat** fehl, und lassen Sie die Verbindung in Ruhe.

Ein Transformationsfilter hat möglicherweise keine bevorzugten Ausgabetypen, es sei denn, der Eingabepin ist verbunden. In diesem Fall sollten die **Methoden SetFormat** und [**IAMStreamConfig::GetStreamCaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) VFW E NOT CONNECTED zurückgeben, \_ bis der \_ \_ Eingabepin verbunden ist. Andernfalls können diese Methoden wie gewohnt funktionieren.

In bestimmten Fällen ist es hilfreich, pins erneut zu verbinden, wenn Sie ein Format für eine hergestellte Verbindung anbieten. Angenommen, ein Filter kann 24-Bit-RGB-Videos im Format X komprimieren und 8-Bit-RGB-Videos im Format Y komprimieren. Der Ausgabepin kann eine der folgenden Schritte ausführen:

-   Bieten Sie in **GetStreamCaps** immer sowohl X als auch Y an, und akzeptieren Sie in **SetFormat** immer sowohl X als auch Y.
-   Angebots- und Annahmeformat X, wenn der Eingabetyp 24-Bit RGB ist. Sie können nur das Format Y anbieten und akzeptieren, wenn der Eingabetyp 8-Bit RGB ist. Fehler bei beiden Methoden, wenn der Eingabepin nicht verbunden ist.

In beiden Fällen benötigen Sie code, der wie folgt aussieht, um die Verbindung wiederherzustellen:


```C++
HRESULT MyOutputPin::CheckMediaType(const CMediaType *pmtOut)
{
    // Fail if the input pin is not connected.
    if (!m_pFilter->m_pInput->IsConnected()) {
        return VFW_E_NOT_CONNECTED;
    }

    // (Not shown: Reject any media types that you know in advance your 
    // filter cannot use. Check the major type and subtype GUIDs.)

    // (Not shown: If SetFormat was previously called, check whether
    // pmtOut exactly matches the format that was specified in SetFormat.
    // Return S_OK if they match, or VFW_E_INVALIDMEDIATYPE otherwise.)
   
    // Now do the normal check for this media type.
    HRESULT hr;
    hr = m_pFilter->CheckTransform(
        &m_pFilter->m_pInput->CurrentMediaType(),  // The input type.
        pmtOut  // The proposed output type.
    );
    if (hr == S_OK)
    {
        // This format is compatible with the current input type.
        return S_OK;
    }
 
    // This format is not compatible with the current input type. 
    // Maybe we can reconnect the input pin with a new input type.
    
    // Enumerate the upstream filter's preferred output types, and 
    // see if one of them will work.
    CMediaType *pmtEnum;
    BOOL fFound = FALSE;
    IEnumMediaTypes *pEnum;
    hr = m_pFilter->m_pInput->GetConnected()->EnumMediaTypes(&pEnum);
    if (hr != S_OK)
    {
        return E_FAIL;
    }
    while (hr = pEnum->Next(1, (AM_MEDIA_TYPE **)&pmtEnum, NULL), hr == S_OK)
    {
        // Check this input type against the proposed output type.
        hr = m_pFilter->CheckTransform(pmtEnum, pmtOut);
        if (hr != S_OK) 
        {
            DeleteMediaType(pmtEnum);
            continue; // Try the next one.
        }

        // This input type is a possible candidate. But, we have to make
        // sure that the upstream filter can switch to this type. 
        hr = m_pFilter->m_pInput->GetConnected()->QueryAccept(pmtEnum);
        if (hr != S_OK) 
        {
            // The upstream filter will not switch to this type.
            DeleteMediaType(pmtEnum);
            continue; // Try the next one.
        }
        fFound = TRUE;
        DeleteMediaType(pmtEnum);
        break;
    }
    pEnum->Release();

    if (fFound)
    {
        // This output type is OK, but if we are asked to use it, we will
        // need to reconnect our input pin. (See SetFormat, below.)
        return S_OK;
    }
    else
    {
        return VFW_E_INVALIDMEDIATYPE;
    }
}

HRESULT MyOutputPin::SetFormat(AM_MEDIA_TYPE *pmt)
{
    CheckPointer(pmt, E_POINTER);
    HRESULT hr;

    // Hold the filter state lock, to make sure that streaming isn't 
    // in the middle of starting or stopping:
    CAutoLock cObjectLock(&m_pFilter->m_csFilter);

    // Cannot set the format unless the filter is stopped.
    if (m_pFilter->m_State != State_Stopped)
    {
        return VFW_E_NOT_STOPPED;
    }

    // The set of possible output formats depends on the input format,
    // so if the input pin is not connected, return a failure code.
    if (!m_pFilter->m_pInput->IsConnected())
    {
        return VFW_E_NOT_CONNECTED;
    }

    // If the pin is already using this format, there's nothing to do.
    if (IsConnected() && CurrentMediaType() == *pmt)
    {
        return S_OK;
    }

    // See if this media type is acceptable.
    if ((hr = CheckMediaType((CMediaType *)pmt)) != S_OK) 
    {
        return hr;
    }

    // If we're connected to a downstream filter, we have to make
    // sure that the downstream filter accepts this media type.
    if (IsConnected()) 
    {
        hr = GetConnected()->QueryAccept(pmt);
        if (hr != S_OK)
        {
            return VFW_E_INVALIDMEDIATYPE;
        }
    }

    // Now make a note that from now on, this is the only format allowed,
    // and refuse anything but this in the CheckMediaType code above.

    // Changing the format means reconnecting if necessary.
    if (IsConnected())
    {
        m_pFilter->m_pGraph->Reconnect(this);
    }

    return NOERROR;
}


// Override CTransformFilter::SetMediaType to reconnect the input pin. 
// This method is called immediately after the media type is set on a pin.
HRESULT MyFilter::SetMediaType(
    PIN_DIRECTION direction, 
    const CMediaType *pmt
)
{
    HRESULT hr;
    if (direction == PINDIR_OUTPUT) 
    {
        // Before we set the output type, we might need to reconnect 
        // the input pin with a new type.
        if (m_pInput && m_pInput->IsConnected()) 
        {
            // Check if the current input type is compatible.
            hr = CheckTransform(
                    &m_pInput->CurrentMediaType(),
                    &m_pOutput->CurrentMediaType());
            if (SUCCEEDED(hr))
            {
                return S_OK;
            }
            // Otherwise, we need to reconnect the input pin.
            // Note: The CheckMediaType method has already called 
            // QueryAccept on the upstream filter. 
            hr = m_pGraph->Reconnect(m_pInput);
            return hr;
        }
    }
    return S_OK;
}
```



 

 



