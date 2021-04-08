---
description: Ein Attribut ist ein Schlüssel-Wert-Paar, bei dem der Schlüssel eine GUID und der Wert eine PROPVARIANT ist. Attribute werden in Microsoft Media Foundation zum Konfigurieren von Objekten, zum Beschreiben von Medienformaten, zum Abfragen von Objekteigenschaften und zu anderen Zwecken verwendet.
ms.assetid: 44af5e03-5f0a-4564-b9d6-b8c935df35b2
title: Attribute in Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6e7893586aa1e966b95c1af5d04246bbb0c82ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749384"
---
# <a name="attributes-in-media-foundation"></a><span data-ttu-id="6ea4c-104">Attribute in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="6ea4c-104">Attributes in Media Foundation</span></span>

<span data-ttu-id="6ea4c-105">Ein Attribut ist ein Schlüssel-Wert-Paar, bei dem der Schlüssel eine GUID und der Wert eine **PROPVARIANT** ist.</span><span class="sxs-lookup"><span data-stu-id="6ea4c-105">An attribute is a key/value pair, where the key is a GUID and the value is a **PROPVARIANT**.</span></span> <span data-ttu-id="6ea4c-106">Attribute werden in Microsoft Media Foundation zum Konfigurieren von Objekten, zum Beschreiben von Medienformaten, zum Abfragen von Objekteigenschaften und zu anderen Zwecken verwendet.</span><span class="sxs-lookup"><span data-stu-id="6ea4c-106">Attributes are used throughout Microsoft Media Foundation to configure objects, describe media formats, query object properties, and other purposes.</span></span>

<span data-ttu-id="6ea4c-107">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="6ea4c-107">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="6ea4c-108">Info zu Attributen</span><span class="sxs-lookup"><span data-stu-id="6ea4c-108">About Attributes</span></span>](#about-attributes)
-   [<span data-ttu-id="6ea4c-109">Serialisieren von Attributen</span><span class="sxs-lookup"><span data-stu-id="6ea4c-109">Serializing Attributes</span></span>](#serializing-attributes)
-   [<span data-ttu-id="6ea4c-110">Implementieren von imfattributes</span><span class="sxs-lookup"><span data-stu-id="6ea4c-110">Implementing IMFAttributes</span></span>](#implementing-imfattributes)
-   [<span data-ttu-id="6ea4c-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6ea4c-111">Related topics</span></span>](#related-topics)

## <a name="about-attributes"></a><span data-ttu-id="6ea4c-112">Info zu Attributen</span><span class="sxs-lookup"><span data-stu-id="6ea4c-112">About Attributes</span></span>

<span data-ttu-id="6ea4c-113">Ein Attribut ist ein Schlüssel-Wert-Paar, bei dem der Schlüssel eine GUID und der Wert eine **PROPVARIANT** ist.</span><span class="sxs-lookup"><span data-stu-id="6ea4c-113">An attribute is a key/value pair, where the key is a GUID and the value is a **PROPVARIANT**.</span></span> <span data-ttu-id="6ea4c-114">Attributwerte sind auf die folgenden Datentypen beschränkt:</span><span class="sxs-lookup"><span data-stu-id="6ea4c-114">Attribute values are restricted to the following data types:</span></span>

-   <span data-ttu-id="6ea4c-115">32-Bit-Ganzzahl ohne Vorzeichen (**UInt32**).</span><span class="sxs-lookup"><span data-stu-id="6ea4c-115">Unsigned 32-bit integer (**UINT32**).</span></span>
-   <span data-ttu-id="6ea4c-116">64-Bit-Ganzzahl ohne Vorzeichen (**UINT64**).</span><span class="sxs-lookup"><span data-stu-id="6ea4c-116">Unsigned 64-bit integer (**UINT64**).</span></span>
-   <span data-ttu-id="6ea4c-117">64-Bit-Gleit Komma Zahl.</span><span class="sxs-lookup"><span data-stu-id="6ea4c-117">64-bit floating-point number.</span></span>
-   <span data-ttu-id="6ea4c-118">GUID.</span><span class="sxs-lookup"><span data-stu-id="6ea4c-118">GUID.</span></span>
-   <span data-ttu-id="6ea4c-119">Auf NULL endende Zeichenfolge für breite Zeichen.</span><span class="sxs-lookup"><span data-stu-id="6ea4c-119">Null-terminated wide-character string.</span></span>
-   <span data-ttu-id="6ea4c-120">Bytearray.</span><span class="sxs-lookup"><span data-stu-id="6ea4c-120">Byte array.</span></span>
-   <span data-ttu-id="6ea4c-121">**IUnknown** -Zeiger.</span><span class="sxs-lookup"><span data-stu-id="6ea4c-121">**IUnknown** pointer.</span></span>

<span data-ttu-id="6ea4c-122">Diese Typen werden in der [**MF- \_ \_ Attributtyp**](/windows/desktop/api/mfobjects/ne-mfobjects-mf_attribute_type) -Enumeration definiert.</span><span class="sxs-lookup"><span data-stu-id="6ea4c-122">These types are defined in the [**MF\_ATTRIBUTE\_TYPE**](/windows/desktop/api/mfobjects/ne-mfobjects-mf_attribute_type) enumeration.</span></span> <span data-ttu-id="6ea4c-123">Um Attributwerte festzulegen oder abzurufen, verwenden Sie die [**imfattributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="6ea4c-123">To set or retrieve attribute values, use the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span> <span data-ttu-id="6ea4c-124">Diese Schnittstelle enthält typsichere Methoden, um Werte nach dem Datentyp zu erhalten und festzulegen.</span><span class="sxs-lookup"><span data-stu-id="6ea4c-124">This interface contains type-safe methods to get and set values by data type.</span></span> <span data-ttu-id="6ea4c-125">Um z. b. eine 32-Bit-Ganzzahl festzulegen, nennen Sie [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="6ea4c-125">For example, to set a 32-bit integer, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span> <span data-ttu-id="6ea4c-126">Attribut Schlüssel sind innerhalb eines Objekts eindeutig.</span><span class="sxs-lookup"><span data-stu-id="6ea4c-126">Attribute keys are unique within an object.</span></span> <span data-ttu-id="6ea4c-127">Wenn Sie zwei verschiedene Werte mit demselben Schlüssel festlegen, überschreibt der zweite Wert den ersten.</span><span class="sxs-lookup"><span data-stu-id="6ea4c-127">If you set two different values with the same key, the second value overwrites the first.</span></span>

<span data-ttu-id="6ea4c-128">Mehrere Media Foundation Schnittstellen erben die [**imfattributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="6ea4c-128">Several Media Foundation interfaces inherit the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span> <span data-ttu-id="6ea4c-129">Objekte, die diese Schnittstelle verfügbar machen, verfügen über optionale oder obligatorische Attribute, die von der Anwendung für das Objekt festgelegt werden sollen, oder über Attribute, die die Anwendung abrufen kann.</span><span class="sxs-lookup"><span data-stu-id="6ea4c-129">Objects that expose this interface have optional or mandatory attributes that the application should set on the object, or have attributes that the application can retrieve.</span></span> <span data-ttu-id="6ea4c-130">Außerdem akzeptieren einige Methoden und Funktionen einen **imfattributes** -Zeiger als Parameter, der es der Anwendung ermöglicht, Konfigurationsinformationen festzulegen.</span><span class="sxs-lookup"><span data-stu-id="6ea4c-130">Also, some methods and functions take an **IMFAttributes** pointer as a parameter, which enables the application to set configuration information.</span></span> <span data-ttu-id="6ea4c-131">Die Anwendung muss einen Attribut Speicher zum Speichern der Konfigurations Attribute erstellen.</span><span class="sxs-lookup"><span data-stu-id="6ea4c-131">The application must create an attribute store to hold the configuration attributes.</span></span> <span data-ttu-id="6ea4c-132">Um einen leeren Attribut Speicher zu erstellen, rufen Sie [**mfkreateattributs**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes)auf.</span><span class="sxs-lookup"><span data-stu-id="6ea4c-132">To create an empty attribute store, call [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes).</span></span>

<span data-ttu-id="6ea4c-133">Der folgende Code zeigt zwei Funktionen.</span><span class="sxs-lookup"><span data-stu-id="6ea4c-133">The following code shows two functions.</span></span> <span data-ttu-id="6ea4c-134">Der erste erstellt einen neuen Attribut Speicher und legt ein hypothetisches Attribut \_ mit dem Namen My Attribute mit einem Zeichen folgen Wert fest.</span><span class="sxs-lookup"><span data-stu-id="6ea4c-134">The first creates a new attribute store and sets a hypothetical attribute named MY\_ATTRIBUTE with a string value.</span></span> <span data-ttu-id="6ea4c-135">Die zweite Funktion Ruft den Wert dieses Attributs ab.</span><span class="sxs-lookup"><span data-stu-id="6ea4c-135">The second function retrieves the value of this attribute.</span></span>


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



<span data-ttu-id="6ea4c-136">Eine umfassende Liste der Media Foundation Attribute finden Sie unter [Media Foundation Attribute](media-foundation-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="6ea4c-136">For a complete list of Media Foundation attributes, see [Media Foundation Attributes](media-foundation-attributes.md).</span></span> <span data-ttu-id="6ea4c-137">Der erwartete Datentyp für jedes Attribut ist hier dokumentiert.</span><span class="sxs-lookup"><span data-stu-id="6ea4c-137">The expected data type for each attribute is documented there.</span></span>

## <a name="serializing-attributes"></a><span data-ttu-id="6ea4c-138">Serialisieren von Attributen</span><span class="sxs-lookup"><span data-stu-id="6ea4c-138">Serializing Attributes</span></span>

<span data-ttu-id="6ea4c-139">Media Foundation verfügt über zwei Funktionen zum Serialisieren von Attribut speichern.</span><span class="sxs-lookup"><span data-stu-id="6ea4c-139">Media Foundation has two functions for serializing attribute stores.</span></span> <span data-ttu-id="6ea4c-140">Eine schreibt die Attribute in ein Bytearray, das andere schreibt Sie in einen Stream, der die **IStream** -Schnittstelle unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6ea4c-140">One writes the attributes to a byte array, the other writes them to a stream that supports the **IStream** interface.</span></span> <span data-ttu-id="6ea4c-141">Jede Funktion verfügt über eine entsprechende Funktion, mit der die Daten geladen werden.</span><span class="sxs-lookup"><span data-stu-id="6ea4c-141">Each function has a corresponding function that loads the data.</span></span>



| <span data-ttu-id="6ea4c-142">Vorgang</span><span class="sxs-lookup"><span data-stu-id="6ea4c-142">Operation</span></span> | <span data-ttu-id="6ea4c-143">Bytearray</span><span class="sxs-lookup"><span data-stu-id="6ea4c-143">Byte Array</span></span>                                                   | <span data-ttu-id="6ea4c-144">IStream</span><span class="sxs-lookup"><span data-stu-id="6ea4c-144">IStream</span></span>                                                                        |
|-----------|--------------------------------------------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="6ea4c-145">Speichern</span><span class="sxs-lookup"><span data-stu-id="6ea4c-145">Save</span></span>      | [<span data-ttu-id="6ea4c-146">**Mfgetattributesasblob**</span><span class="sxs-lookup"><span data-stu-id="6ea4c-146">**MFGetAttributesAsBlob**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributesasblob)       | [<span data-ttu-id="6ea4c-147">**MF serializeattributestostream**</span><span class="sxs-lookup"><span data-stu-id="6ea4c-147">**MFSerializeAttributesToStream**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-mfserializeattributestostream)         |
| <span data-ttu-id="6ea4c-148">Laden</span><span class="sxs-lookup"><span data-stu-id="6ea4c-148">Load</span></span>      | [<span data-ttu-id="6ea4c-149">**Mfinitattributesfromblob**</span><span class="sxs-lookup"><span data-stu-id="6ea4c-149">**MFInitAttributesFromBlob**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfinitattributesfromblob) | [<span data-ttu-id="6ea4c-150">**MF deserializeattributesfromstream**</span><span class="sxs-lookup"><span data-stu-id="6ea4c-150">**MFDeserializeAttributesFromStream**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-mfdeserializeattributesfromstream) |



 

<span data-ttu-id="6ea4c-151">Um den Inhalt eines Attribut Speichers in ein Bytearray zu schreiben, müssen Sie [**mfgetattributesasblob**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributesasblob)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="6ea4c-151">To write the contents of an attribute store into a byte array, call [**MFGetAttributesAsBlob**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributesasblob).</span></span> <span data-ttu-id="6ea4c-152">Attribute mit **IUnknown** -Zeiger Werten werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="6ea4c-152">Attributes with **IUnknown** pointer values are ignored.</span></span> <span data-ttu-id="6ea4c-153">Um die Attribute wieder in einen Attribut Speicher zu laden, müssen Sie [**mfinitattributesfromblob**](/windows/desktop/api/mfapi/nf-mfapi-mfinitattributesfromblob)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="6ea4c-153">To load the attributes back into an attribute store, call [**MFInitAttributesFromBlob**](/windows/desktop/api/mfapi/nf-mfapi-mfinitattributesfromblob).</span></span>

<span data-ttu-id="6ea4c-154">Um einen Attribut Speicher in einen Stream zu schreiben, nennen Sie [**mfserializeattributestostream**](/windows/desktop/api/mfobjects/nf-mfobjects-mfserializeattributestostream).</span><span class="sxs-lookup"><span data-stu-id="6ea4c-154">To write an attribute store to a stream, call [**MFSerializeAttributesToStream**](/windows/desktop/api/mfobjects/nf-mfobjects-mfserializeattributestostream).</span></span> <span data-ttu-id="6ea4c-155">Diese Funktion kann **IUnknown** -Zeiger Werte Mars Hallen.</span><span class="sxs-lookup"><span data-stu-id="6ea4c-155">This function can marshal **IUnknown** pointer values.</span></span> <span data-ttu-id="6ea4c-156">Der Aufrufer muss ein Streamobjekt bereitstellen, das die **IStream** -Schnittstelle implementiert.</span><span class="sxs-lookup"><span data-stu-id="6ea4c-156">The caller must provide a stream object that implements the **IStream** interface.</span></span> <span data-ttu-id="6ea4c-157">Um einen Attribut Speicher aus einem Stream zu laden, müssen Sie [**mfdeserializeattributesfromstream**](/windows/desktop/api/mfobjects/nf-mfobjects-mfdeserializeattributesfromstream)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="6ea4c-157">To load an attribute store from a stream, call [**MFDeserializeAttributesFromStream**](/windows/desktop/api/mfobjects/nf-mfobjects-mfdeserializeattributesfromstream).</span></span>

## <a name="implementing-imfattributes"></a><span data-ttu-id="6ea4c-158">Implementieren von imfattributes</span><span class="sxs-lookup"><span data-stu-id="6ea4c-158">Implementing IMFAttributes</span></span>

<span data-ttu-id="6ea4c-159">Media Foundation stellt eine Aktien Implementierung von [**imfattributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)bereit, die durch Aufrufen der Funktion [**mfcreateattributs**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="6ea4c-159">Media Foundation provides a stock implementation of [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes), which is obtained by calling the [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) function.</span></span> <span data-ttu-id="6ea4c-160">In den meisten Fällen sollten Sie diese Implementierung verwenden und keine eigene benutzerdefinierte Implementierung bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="6ea4c-160">In most situations, you should use this implementation, and not provide your own custom implementation.</span></span>

<span data-ttu-id="6ea4c-161">Es gibt eine Situation, in der Sie die [**imfattributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) -Schnittstelle implementieren müssen, wenn Sie eine zweite Schnittstelle implementieren, die **imfattributes** erbt.</span><span class="sxs-lookup"><span data-stu-id="6ea4c-161">There is one situation when you might need to implement the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface: If you implement a second interface that inherits **IMFAttributes**.</span></span> <span data-ttu-id="6ea4c-162">In diesem Fall müssen Sie Implementierungen für die **imfattributes** -Methoden bereitstellen, die von der zweiten Schnittstelle geerbt werden.</span><span class="sxs-lookup"><span data-stu-id="6ea4c-162">In that case, you must provide implementations for the **IMFAttributes** methods inherited by the second interface.</span></span>

<span data-ttu-id="6ea4c-163">In dieser Situation wird empfohlen, die vorhandene Media Foundation Implementierung von [**imfattributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)einzubinden.</span><span class="sxs-lookup"><span data-stu-id="6ea4c-163">In this situation, it is recommended to wrap the existing Media Foundation implementation of [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes).</span></span> <span data-ttu-id="6ea4c-164">Der folgende Code zeigt eine Klassen Vorlage, die einen **imfattributes** -Zeiger enthält und jede **imfattributes** -Methode umschließt, mit Ausnahme der **IUnknown** -Methoden.</span><span class="sxs-lookup"><span data-stu-id="6ea4c-164">The following code shows a class template that holds an **IMFAttributes** pointer and wraps every **IMFAttributes** method, except for the **IUnknown** methods.</span></span>


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



<span data-ttu-id="6ea4c-165">Der folgende Code zeigt, wie Sie eine Klasse von dieser Vorlage ableiten:</span><span class="sxs-lookup"><span data-stu-id="6ea4c-165">The following code shows how to derive a class from this template:</span></span>


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



<span data-ttu-id="6ea4c-166">Sie müssen aufzurufen `CBaseAttributes::Initialize` , um den Attribut Speicher zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="6ea4c-166">You must call `CBaseAttributes::Initialize` to create the attribute store.</span></span> <span data-ttu-id="6ea4c-167">Im vorherigen Beispiel wird dies innerhalb einer statischen Erstellungs Funktion durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="6ea4c-167">In the previous example, that is done inside a static creation function.</span></span>

<span data-ttu-id="6ea4c-168">Das Vorlagen Argument ist ein Schnittstellentyp, der standardmäßig auf " [**imfattributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="6ea4c-168">The template argument is an interface type, which defaults to [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes).</span></span> <span data-ttu-id="6ea4c-169">Wenn das Objekt eine Schnittstelle implementiert, die **imfattributes** erbt (z. b. [**imfaktivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)), legen Sie das Vorlagen Argument auf den Namen der abgeleiteten Schnittstelle fest.</span><span class="sxs-lookup"><span data-stu-id="6ea4c-169">If your object implements an interface that inherits **IMFAttributes**, such as [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate), set the template argument equal to name of the derived interface.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6ea4c-170">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6ea4c-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6ea4c-171">Media Foundation primitiver</span><span class="sxs-lookup"><span data-stu-id="6ea4c-171">Media Foundation Primitives</span></span>](media-foundation-primitives.md)
</dt> </dl>

 

 



