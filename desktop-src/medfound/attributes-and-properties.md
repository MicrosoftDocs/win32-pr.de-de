---
description: Ein Attribut ist ein Schlüssel-Wert-Paar, bei dem der Schlüssel eine GUID und der Wert ein PROPVARIANT ist. Attribute werden in der gesamten Microsoft Media Foundation, um Objekte zu konfigurieren, Medienformate, Abfrageobjekteigenschaften und andere Zwecke zu beschreiben.
ms.assetid: 44af5e03-5f0a-4564-b9d6-b8c935df35b2
title: Attribute in Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f46cc919f426ff7b0862de73d8852291d25b7e31f2b5d67d7a4955369be6d17
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119943300"
---
# <a name="attributes-in-media-foundation"></a>Attribute in Media Foundation

Ein Attribut ist ein Schlüssel-Wert-Paar, bei dem der Schlüssel eine GUID und der Wert ein **PROPVARIANT-Wert ist.** Attribute werden in der gesamten Microsoft Media Foundation, um Objekte zu konfigurieren, Medienformate, Abfrageobjekteigenschaften und andere Zwecke zu beschreiben.

Dieses Thema enthält folgende Abschnitte:

-   [Info zu Attributen](#about-attributes)
-   [Serialisieren von Attributen](#serializing-attributes)
-   [Implementieren von ATTRIBUTEN](#implementing-imfattributes)
-   [Zugehörige Themen](#related-topics)

## <a name="about-attributes"></a>Info zu Attributen

Ein Attribut ist ein Schlüssel-Wert-Paar, bei dem der Schlüssel eine GUID und der Wert ein **PROPVARIANT-Wert ist.** Attributwerte sind auf die folgenden Datentypen beschränkt:

-   32-Bit-Ganzzahl ohne Vorzeichen (**UINT32**).
-   64-Bit-Ganzzahl ohne Vorzeichen (**UINT64**).
-   64-Bit-Gleitkommazahl.
-   GUID.
-   Auf NULL endende Zeichenfolge für breite Zeichen.
-   Bytearray.
-   **IUnknown-Zeiger.**

Diese Typen werden in der [**MF \_ ATTRIBUTE \_ TYPE-Enumeration**](/windows/desktop/api/mfobjects/ne-mfobjects-mf_attribute_type) definiert. Verwenden Sie zum Festlegen oder Abrufen von Attributwerten [**die SCHNITTSTELLE ATTRIBUTEAttributes.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) Diese Schnittstelle enthält typsichere Methoden zum Erhalten und Festlegen von Werten nach Datentyp. Rufen Sie z. B. ZUM Festlegen einer 32-Bit-Ganzzahl [**DIE ATTRIBUTEs::SetUINT32 auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) Attributschlüssel sind innerhalb eines Objekts eindeutig. Wenn Sie zwei verschiedene Werte mit demselben Schlüssel festlegen, überschreibt der zweite Wert den ersten Wert.

Mehrere Media Foundation erben die [**INTERFACE DER ATTRIBUTEAttributes.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) Objekte, die diese Schnittstelle verfügbar machen, verfügen über optionale oder obligatorische Attribute, die die Anwendung für das Objekt festlegen soll, oder über Attribute, die die Anwendung abrufen kann. Außerdem verwenden einige Methoden und Funktionen einen **ATTRIBUTEAttributes-Zeiger** als Parameter, wodurch die Anwendung Konfigurationsinformationen festlegen kann. Die Anwendung muss einen Attributspeicher erstellen, um die Konfigurationsattribute zu speichern. Um einen leeren Attributspeicher zu erstellen, rufen [**Sie MFCreateAttributes auf.**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes)

Der folgende Code zeigt zwei Funktionen. Der erste erstellt einen neuen Attributspeicher und legt ein hypothetisches Attribut namens MY \_ ATTRIBUTE mit einem Zeichenfolgenwert fest. Die zweite Funktion ruft den Wert dieses Attributs ab.


```C++
extern const GUID MY_ATTRIBUTE;

HRESULT ShowCreateAttributeStore(IMFAttributes **ppAttributes)
{
    IMFAttributes *pAttributes = NULL;
    const UINT32 cElements = 10;  // Starting size.

    // Create the empty attribute store.
    HRESULT hr = MFCreateAttributes(&pAttributes, cElements);

    // Set the MY_ATTRIBUTE attribute with a string value.
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetString(
            MY_ATTRIBUTE,
            L"This is a string value"
            );
    }

    // Return the IMFAttributes pointer to the caller.
    if (SUCCEEDED(hr))
    {
        *ppAttributes = pAttributes;
        (*ppAttributes)->AddRef();
    }

    SAFE_RELEASE(pAttributes);

    return hr;
}

HRESULT ShowGetAttributes()
{
    IMFAttributes *pAttributes = NULL;
    WCHAR *pwszValue = NULL;
    UINT32 cchLength = 0;

    // Create the attribute store.
    HRESULT hr = ShowCreateAttributeStore(&pAttributes);

    // Get the attribute.
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->GetAllocatedString(
            MY_ATTRIBUTE,
            &pwszValue,
            &cchLength
            );
    }

    CoTaskMemFree(pwszValue);
    SAFE_RELEASE(pAttributes);

    return hr;
}
```



Eine vollständige Liste der Media Foundation Attribute finden Sie unter [Media Foundation Attribute.](media-foundation-attributes.md) Der erwartete Datentyp für jedes Attribut ist dort dokumentiert.

## <a name="serializing-attributes"></a>Serialisieren von Attributen

Media Foundation verfügt über zwei Funktionen zum Serialisieren von Attributspeichern. Eines schreibt die Attribute in ein Bytearray, das andere schreibt sie in einen Stream, der die **IStream-Schnittstelle** unterstützt. Jede Funktion verfügt über eine entsprechende Funktion, die die Daten lädt.



| Vorgang | Bytearray                                                   | Istream                                                                        |
|-----------|--------------------------------------------------------------|--------------------------------------------------------------------------------|
| Speichern      | [**MFGetAttributesAsBlob**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributesasblob)       | [**MFSerializeAttributesToStream**](/windows/desktop/api/mfobjects/nf-mfobjects-mfserializeattributestostream)         |
| Laden      | [**MFInitAttributesFromBlob**](/windows/desktop/api/mfapi/nf-mfapi-mfinitattributesfromblob) | [**MFDeserializeAttributesFromStream**](/windows/desktop/api/mfobjects/nf-mfobjects-mfdeserializeattributesfromstream) |



 

Um den Inhalt eines Attributspeichers in ein Bytearray zu schreiben, rufen Sie [**MFGetAttributesAsBlob auf.**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributesasblob) Attribute mit **IUnknown-Zeigerwerten** werden ignoriert. Rufen Sie [**MFInitAttributesFromBlob**](/windows/desktop/api/mfapi/nf-mfapi-mfinitattributesfromblob)auf, um die Attribute wieder in einen Attributspeicher zu laden.

Um einen Attributspeicher in einen Stream zu schreiben, rufen Sie [**MFSerializeAttributesToStream auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-mfserializeattributestostream) Diese Funktion kann **IUnknown-Zeigerwerte** marshallen. Der Aufrufer muss ein Streamobjekt bereitstellen, das die **IStream-Schnittstelle** implementiert. Um einen Attributspeicher aus einem Stream zu laden, rufen Sie [**MFDeserializeAttributesFromStream auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-mfdeserializeattributesfromstream)

## <a name="implementing-imfattributes"></a>Implementieren von ATTRIBUTEN

Media Foundation stellt eine Vorratimplementierung von [**ATTRIBUTEAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)zur Anwendung, die durch Aufrufen der [**MFCreateAttributes-Funktion abgerufen**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) wird. In den meisten Fällen sollten Sie diese Implementierung verwenden und keine eigene benutzerdefinierte Implementierung bereitstellen.

Es gibt eine Situation, in der Sie möglicherweise die [**BESCHRIFTUNGAttributes-Schnittstelle**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) implementieren müssen: Wenn Sie eine zweite Schnittstelle implementieren, die **DIE ATTRIBUTEs erbt.** In diesem Fall müssen Sie Implementierungen für die VON der zweiten Schnittstelle geerbten **METHODEN DER ATTRIBUTEAttributes** bereitstellen.

In diesem Fall empfiehlt es sich, die vorhandene [**Media Foundation-Implementierung von ATTRIBUTEAttributes zu umschließen.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) Der folgende Code zeigt eine Klassenvorlage, die einen **ATTRIBUTEAttributes-Zeiger** enthält und mit Ausnahme der **IUnknown-Methoden** jede **METHODE DES ATTRIBUTEAttributes** umschließt.


```C++
#include <assert.h>

// Helper class to implement IMFAttributes. 

// This is an abstract class; the derived class must implement the IUnknown 
// methods. This class is a wrapper for the standard attribute store provided 
// in Media Foundation.

// template parameter: 
// The interface you are implementing, either IMFAttributes or an interface 
// that inherits IMFAttributes, such as IMFActivate

template <class IFACE=IMFAttributes>
class CBaseAttributes : public IFACE
{
protected:
    IMFAttributes *m_pAttributes;

    // This version of the constructor does not initialize the 
    // attribute store. The derived class must call Initialize() in 
    // its own constructor.
    CBaseAttributes() : m_pAttributes(NULL)
    {
    }

    // This version of the constructor initializes the attribute 
    // store, but the derived class must pass an HRESULT parameter 
    // to the constructor.

    CBaseAttributes(HRESULT& hr, UINT32 cInitialSize = 0) : m_pAttributes(NULL)
    {
        hr = Initialize(cInitialSize);
    }

    // The next version of the constructor uses a caller-provided 
    // implementation of IMFAttributes.

    // (Sometimes you want to delegate IMFAttributes calls to some 
    // other object that implements IMFAttributes, rather than using 
    // MFCreateAttributes.)

    CBaseAttributes(HRESULT& hr, IUnknown *pUnk)
    {
        hr = Initialize(pUnk);
    }

    virtual ~CBaseAttributes()
    {
        if (m_pAttributes)
        {
            m_pAttributes->Release();
        }
    }

    // Initializes the object by creating the standard Media Foundation attribute store.
    HRESULT Initialize(UINT32 cInitialSize = 0)
    {
        if (m_pAttributes == NULL)
        {
            return MFCreateAttributes(&m_pAttributes, cInitialSize); 
        }
        else
        {
            return S_OK;
        }
    }

    // Initializes this object from a caller-provided attribute store.
    // pUnk: Pointer to an object that exposes IMFAttributes.
    HRESULT Initialize(IUnknown *pUnk)
    {
        if (m_pAttributes)
        {
            m_pAttributes->Release();
            m_pAttributes = NULL;
        }


        return pUnk->QueryInterface(IID_PPV_ARGS(&m_pAttributes));
    }

public:

    // IMFAttributes methods

    STDMETHODIMP GetItem(REFGUID guidKey, PROPVARIANT* pValue)
    {
        assert(m_pAttributes);
        return m_pAttributes->GetItem(guidKey, pValue);
    }

    STDMETHODIMP GetItemType(REFGUID guidKey, MF_ATTRIBUTE_TYPE* pType)
    {
        assert(m_pAttributes);
        return m_pAttributes->GetItemType(guidKey, pType);
    }

    STDMETHODIMP CompareItem(REFGUID guidKey, REFPROPVARIANT Value, BOOL* pbResult)
    {
        assert(m_pAttributes);
        return m_pAttributes->CompareItem(guidKey, Value, pbResult);
    }

    STDMETHODIMP Compare(
        IMFAttributes* pTheirs, 
        MF_ATTRIBUTES_MATCH_TYPE MatchType, 
        BOOL* pbResult
        )
    {
        assert(m_pAttributes);
        return m_pAttributes->Compare(pTheirs, MatchType, pbResult);
    }

    STDMETHODIMP GetUINT32(REFGUID guidKey, UINT32* punValue)
    {
        assert(m_pAttributes);
        return m_pAttributes->GetUINT32(guidKey, punValue);
    }

    STDMETHODIMP GetUINT64(REFGUID guidKey, UINT64* punValue)
    {
        assert(m_pAttributes);
        return m_pAttributes->GetUINT64(guidKey, punValue);
    }

    STDMETHODIMP GetDouble(REFGUID guidKey, double* pfValue)
    {
        assert(m_pAttributes);
        return m_pAttributes->GetDouble(guidKey, pfValue);
    }

    STDMETHODIMP GetGUID(REFGUID guidKey, GUID* pguidValue)
    {
        assert(m_pAttributes);
        return m_pAttributes->GetGUID(guidKey, pguidValue);
    }

    STDMETHODIMP GetStringLength(REFGUID guidKey, UINT32* pcchLength)
    {
        assert(m_pAttributes);
        return m_pAttributes->GetStringLength(guidKey, pcchLength);
    }

    STDMETHODIMP GetString(REFGUID guidKey, LPWSTR pwszValue, UINT32 cchBufSize, UINT32* pcchLength)
    {
        assert(m_pAttributes);
        return m_pAttributes->GetString(guidKey, pwszValue, cchBufSize, pcchLength);
    }

    STDMETHODIMP GetAllocatedString(REFGUID guidKey, LPWSTR* ppwszValue, UINT32* pcchLength)
    {
        assert(m_pAttributes);
        return m_pAttributes->GetAllocatedString(guidKey, ppwszValue, pcchLength);
    }

    STDMETHODIMP GetBlobSize(REFGUID guidKey, UINT32* pcbBlobSize)
    {
        assert(m_pAttributes);
        return m_pAttributes->GetBlobSize(guidKey, pcbBlobSize);
    }

    STDMETHODIMP GetBlob(REFGUID guidKey, UINT8* pBuf, UINT32 cbBufSize, UINT32* pcbBlobSize)
    {
        assert(m_pAttributes);
        return m_pAttributes->GetBlob(guidKey, pBuf, cbBufSize, pcbBlobSize);
    }

    STDMETHODIMP GetAllocatedBlob(REFGUID guidKey, UINT8** ppBuf, UINT32* pcbSize)
    {
        assert(m_pAttributes);
        return m_pAttributes->GetAllocatedBlob(guidKey, ppBuf, pcbSize);
    }

    STDMETHODIMP GetUnknown(REFGUID guidKey, REFIID riid, LPVOID* ppv)
    {
        assert(m_pAttributes);
        return m_pAttributes->GetUnknown(guidKey, riid, ppv);
    }

    STDMETHODIMP SetItem(REFGUID guidKey, REFPROPVARIANT Value)
    {
        assert(m_pAttributes);
        return m_pAttributes->SetItem(guidKey, Value);
    }

    STDMETHODIMP DeleteItem(REFGUID guidKey)
    {
        assert(m_pAttributes);
        return m_pAttributes->DeleteItem(guidKey);
    }

    STDMETHODIMP DeleteAllItems()
    {
        assert(m_pAttributes);
        return m_pAttributes->DeleteAllItems();
    }

    STDMETHODIMP SetUINT32(REFGUID guidKey, UINT32 unValue)
    {
        assert(m_pAttributes);
        return m_pAttributes->SetUINT32(guidKey, unValue);
    }

    STDMETHODIMP SetUINT64(REFGUID guidKey,UINT64 unValue)
    {
        assert(m_pAttributes);
        return m_pAttributes->SetUINT64(guidKey, unValue);
    }

    STDMETHODIMP SetDouble(REFGUID guidKey, double fValue)
    {
        assert(m_pAttributes);
        return m_pAttributes->SetDouble(guidKey, fValue);
    }

    STDMETHODIMP SetGUID(REFGUID guidKey, REFGUID guidValue)
    {
        assert(m_pAttributes);
        return m_pAttributes->SetGUID(guidKey, guidValue);
    }

    STDMETHODIMP SetString(REFGUID guidKey, LPCWSTR wszValue)
    {
        assert(m_pAttributes);
        return m_pAttributes->SetString(guidKey, wszValue);
    }

    STDMETHODIMP SetBlob(REFGUID guidKey, const UINT8* pBuf, UINT32 cbBufSize)
    {
        assert(m_pAttributes);
        return m_pAttributes->SetBlob(guidKey, pBuf, cbBufSize);
    }

    STDMETHODIMP SetUnknown(REFGUID guidKey, IUnknown* pUnknown)
    {
        assert(m_pAttributes);
        return m_pAttributes->SetUnknown(guidKey, pUnknown);
    }

    STDMETHODIMP LockStore()
    {
        assert(m_pAttributes);
        return m_pAttributes->LockStore();
    }

    STDMETHODIMP UnlockStore()
    {
        assert(m_pAttributes);
        return m_pAttributes->UnlockStore();
    }

    STDMETHODIMP GetCount(UINT32* pcItems)
    {
        assert(m_pAttributes);
        return m_pAttributes->GetCount(pcItems);
    }

    STDMETHODIMP GetItemByIndex(UINT32 unIndex, GUID* pguidKey, PROPVARIANT* pValue)
    {
        assert(m_pAttributes);
        return m_pAttributes->GetItemByIndex(unIndex, pguidKey, pValue);
    }

    STDMETHODIMP CopyAllItems(IMFAttributes* pDest)
    {
        assert(m_pAttributes);
        return m_pAttributes->CopyAllItems(pDest);
    }

    // Helper functions
    
    HRESULT SerializeToStream(DWORD dwOptions, IStream* pStm)      
        // dwOptions: Flags from MF_ATTRIBUTE_SERIALIZE_OPTIONS
    {
        assert(m_pAttributes);
        return MFSerializeAttributesToStream(m_pAttributes, dwOptions, pStm);
    }

    HRESULT DeserializeFromStream(DWORD dwOptions, IStream* pStm)
    {
        assert(m_pAttributes);
        return MFDeserializeAttributesFromStream(m_pAttributes, dwOptions, pStm);
    }

    // SerializeToBlob: Stores the attributes in a byte array. 
    // 
    // ppBuf: Receives a pointer to the byte array. 
    // pcbSize: Receives the size of the byte array.
    //
    // The caller must free the array using CoTaskMemFree.
    HRESULT SerializeToBlob(UINT8 **ppBuffer, UINT32 *pcbSize)
    {
        assert(m_pAttributes);

        if (ppBuffer == NULL)
        {
            return E_POINTER;
        }
        if (pcbSize == NULL)
        {
            return E_POINTER;
        }

        *ppBuffer = NULL;
        *pcbSize = 0;

        UINT32 cbSize = 0;
        BYTE *pBuffer = NULL;

        HRESULT hr = MFGetAttributesAsBlobSize(m_pAttributes, &cbSize);

        if (FAILED(hr))
        {
            return hr;
        }

        pBuffer = (BYTE*)CoTaskMemAlloc(cbSize);
        if (pBuffer == NULL)
        {
            return E_OUTOFMEMORY;
        }

        hr = MFGetAttributesAsBlob(m_pAttributes, pBuffer, cbSize);

        if (SUCCEEDED(hr))
        {
            *ppBuffer = pBuffer;
            *pcbSize = cbSize;
        }
        else
        {
            CoTaskMemFree(pBuffer);
        }
        return hr;
    }
    
    HRESULT DeserializeFromBlob(const UINT8* pBuffer, UINT cbSize)
    {
        assert(m_pAttributes);
        return MFInitAttributesFromBlob(m_pAttributes, pBuffer, cbSize);
    }

    HRESULT GetRatio(REFGUID guidKey, UINT32* pnNumerator, UINT32* punDenominator)
    {
        assert(m_pAttributes);
        return MFGetAttributeRatio(m_pAttributes, guidKey, pnNumerator, punDenominator);
    }

    HRESULT SetRatio(REFGUID guidKey, UINT32 unNumerator, UINT32 unDenominator)
    {
        assert(m_pAttributes);
        return MFSetAttributeRatio(m_pAttributes, guidKey, unNumerator, unDenominator);
    }

    // Gets an attribute whose value represents the size of something (eg a video frame).
    HRESULT GetSize(REFGUID guidKey, UINT32* punWidth, UINT32* punHeight)
    {
        assert(m_pAttributes);
        return MFGetAttributeSize(m_pAttributes, guidKey, punWidth, punHeight);
    }

    // Sets an attribute whose value represents the size of something (eg a video frame).
    HRESULT SetSize(REFGUID guidKey, UINT32 unWidth, UINT32 unHeight)
    {
        assert(m_pAttributes);
        return MFSetAttributeSize (m_pAttributes, guidKey, unWidth, unHeight);
    }
};
```



Der folgende Code zeigt, wie sie eine Klasse von dieser Vorlage ableiten:


```C++
#include <shlwapi.h>

class MyObject : public CBaseAttributes<>
{
    MyObject() : m_nRefCount(1) { }
    ~MyObject() { }

    long m_nRefCount;

public:

    // IUnknown
    STDMETHODIMP MyObject::QueryInterface(REFIID riid, void** ppv)
    {
        static const QITAB qit[] = 
        {
            QITABENT(MyObject, IMFAttributes),
            { 0 },
        };
        return QISearch(this, qit, riid, ppv);
    }

    STDMETHODIMP_(ULONG) MyObject::AddRef()
    {
        return InterlockedIncrement(&m_nRefCount);
    }

    STDMETHODIMP_(ULONG) MyObject::Release()
    {
        ULONG uCount = InterlockedDecrement(&m_nRefCount);
        if (uCount == 0)
        {
            delete this;
        }
        return uCount;
    }

    // Static function to create an instance of the object.

    static HRESULT CreateInstance(MyObject **ppObject)
    {
        HRESULT hr = S_OK;

        MyObject *pObject = new MyObject();
        if (pObject == NULL)
        {
            return E_OUTOFMEMORY;
        }

        // Initialize the attribute store.
        hr = pObject->Initialize();

        if (FAILED(hr))
        {
            delete pObject;
            return hr;
        }

        *ppObject = pObject;
        (*ppObject)->AddRef();

        return S_OK;
    }
};
```



Sie müssen `CBaseAttributes::Initialize` aufrufen, um den Attributspeicher zu erstellen. Im vorherigen Beispiel erfolgt dies innerhalb einer statischen Erstellungsfunktion.

Das Vorlagenargument ist ein Schnittstellentyp, der standardmäßig [**AUF ATTRIBUTEs festgelegt ist.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) Wenn Ihr -Objekt eine Schnittstelle implementiert, die **DIE ATTRIBUTE erbt**, z. B. [**DURCHAKTIVIeren,**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)legen Sie das Vorlagenargument auf den Namen der abgeleiteten Schnittstelle fest.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Media Foundation Primitive](media-foundation-primitives.md)
</dt> </dl>

 

 



