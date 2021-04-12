---
description: Die Get-Methode ruft eine Eigenschaft ab, die durch eine Eigenschaften Satz-GUID und eine eigen schafts-ID identifiziert wird.
ms.assetid: f39862db-0659-4533-8cee-aee2f778e085
title: 'Ikspropertyset:: Get-Methode (ksproxy. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IKsPropertySet.Get
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
ms.openlocfilehash: 9c4461e8c5886d84bcf3b7faa6675b749bc0c37d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481763"
---
# <a name="ikspropertysetget-method"></a><span data-ttu-id="5bdb0-103">Ikspropertyset:: Get-Methode</span><span class="sxs-lookup"><span data-stu-id="5bdb0-103">IKsPropertySet::Get method</span></span>

<span data-ttu-id="5bdb0-104">Die **Get** -Methode ruft eine Eigenschaft ab, die durch eine Eigenschaften Satz-GUID und eine eigen schafts-ID identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="5bdb0-104">The **Get** method retrieves a property identified by a property set GUID and a property ID.</span></span>

## <a name="syntax"></a><span data-ttu-id="5bdb0-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5bdb0-105">Syntax</span></span>


```C++
HRESULT Get(
  [in]  REFGUID guidPropSet,
  [in]  DWORD   dwPropID,
  [in]  LPVOID  pInstanceData,
  [in]  DWORD   cbInstanceData,
  [out] LPVOID  pPropData,
  [in]  DWORD   cbPropData,
  [out] DWORD   *pcbReturned
);
```



## <a name="parameters"></a><span data-ttu-id="5bdb0-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5bdb0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5bdb0-107">*guidpropset* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5bdb0-107">*guidPropSet* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5bdb0-108">Die GUID des Eigenschaften Satzes.</span><span class="sxs-lookup"><span data-stu-id="5bdb0-108">The GUID of the property set .</span></span>

</dd> <dt>

<span data-ttu-id="5bdb0-109">*dwpropid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5bdb0-109">*dwPropID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5bdb0-110">Der Bezeichner der Eigenschaft innerhalb des Eigenschaften Satzes.</span><span class="sxs-lookup"><span data-stu-id="5bdb0-110">The identifier of the property within the property set.</span></span>

</dd> <dt>

<span data-ttu-id="5bdb0-111">*pinstancedata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5bdb0-111">*pInstanceData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5bdb0-112">Ein Zeiger auf ein Bytearray, das Instanzdaten für die Eigenschaft enthält.</span><span class="sxs-lookup"><span data-stu-id="5bdb0-112">A pointer to an array of bytes that contains instance data for the property.</span></span>

</dd> <dt>

<span data-ttu-id="5bdb0-113">*cbinstancedata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5bdb0-113">*cbInstanceData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5bdb0-114">Die Größe des in *pinstancedata* angegebenen Arrays in Bytes.</span><span class="sxs-lookup"><span data-stu-id="5bdb0-114">The size of the array given in *pInstanceData*, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="5bdb0-115">*ppropdata* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="5bdb0-115">*pPropData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5bdb0-116">Ein Zeiger auf ein Bytearray, das die Eigenschaften Daten empfängt.</span><span class="sxs-lookup"><span data-stu-id="5bdb0-116">A pointer to an array of bytes that receives the property data.</span></span>

</dd> <dt>

<span data-ttu-id="5bdb0-117">*cbpropdata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5bdb0-117">*cbPropData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5bdb0-118">Die Größe des in *ppropdata* angegebenen Arrays in Bytes.</span><span class="sxs-lookup"><span data-stu-id="5bdb0-118">The size of the array given in *pPropData*, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="5bdb0-119">*pcbreturned* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="5bdb0-119">*pcbReturned* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5bdb0-120">Empfängt die Anzahl von Bytes, die von der Methode in das *ppropdata* -Array kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="5bdb0-120">Receives the number of bytes the method copies to the *pPropData* array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5bdb0-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5bdb0-121">Return value</span></span>

<span data-ttu-id="5bdb0-122">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="5bdb0-122">Returns an **HRESULT** value.</span></span> <span data-ttu-id="5bdb0-123">Die folgenden Werte sind möglich.</span><span class="sxs-lookup"><span data-stu-id="5bdb0-123">Possible values include the following.</span></span>



| <span data-ttu-id="5bdb0-124">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="5bdb0-124">Return code</span></span>                                                                                              | <span data-ttu-id="5bdb0-125">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5bdb0-125">Description</span></span>                                                                 |
|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5bdb0-126"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="5bdb0-126"><dt>**S\_OK**</dt></span></span> </dl>                     | <span data-ttu-id="5bdb0-127">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="5bdb0-127">Success.</span></span><br/>                                                         |
| <dl> <span data-ttu-id="5bdb0-128"><dt>**E- \_ Prop- \_ Satz \_ nicht unterstützt**</dt></span><span class="sxs-lookup"><span data-stu-id="5bdb0-128"><dt>**E\_PROP\_SET\_UNSUPPORTED**</dt></span></span> </dl> | <span data-ttu-id="5bdb0-129">Der Eigenschaften Satz wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5bdb0-129">The property set is not supported.</span></span><br/>                               |
| <dl> <span data-ttu-id="5bdb0-130"><dt>**E- \_ Prop- \_ ID \_ nicht unterstützt**</dt></span><span class="sxs-lookup"><span data-stu-id="5bdb0-130"><dt>**E\_PROP\_ID\_UNSUPPORTED**</dt></span></span> </dl>  | <span data-ttu-id="5bdb0-131">Die eigen schafts-ID wird für den angegebenen Eigenschaften Satz nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5bdb0-131">The property ID is not supported for the specified property set.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5bdb0-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5bdb0-132">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="5bdb0-133">Eine weitere Schnittstelle mit diesem Namen ist in der Header Datei "DSound. h" vorhanden.</span><span class="sxs-lookup"><span data-stu-id="5bdb0-133">Another interface by this name exists in the dsound.h header file.</span></span> <span data-ttu-id="5bdb0-134">Die beiden Schnittstellen sind nicht kompatibel.</span><span class="sxs-lookup"><span data-stu-id="5bdb0-134">The two interfaces are not compatible.</span></span> <span data-ttu-id="5bdb0-135">Die im DirectShow-DDK dokumentierte " [ikscontrol](/windows-hardware/drivers/ddi/ksproxy/nn-ksproxy-ikscontrol) "-Schnittstelle ist nun die empfohlene Schnittstelle zum Übergeben von Eigenschafts Sätzen zwischen WDM-Treibern und Benutzermoduskomponenten.</span><span class="sxs-lookup"><span data-stu-id="5bdb0-135">The [IKsControl](/windows-hardware/drivers/ddi/ksproxy/nn-ksproxy-ikscontrol) interface, documented in the DirectShow DDK, is now the recommended interface for passing property sets between WDM drivers and user mode components.</span></span>

 

<span data-ttu-id="5bdb0-136">Um eine Eigenschaft abzurufen, weisen Sie einen Puffer zu, der von dieser Methode ausgefüllt wird.</span><span class="sxs-lookup"><span data-stu-id="5bdb0-136">To retrieve a property, allocate a buffer which this method will then fill in.</span></span> <span data-ttu-id="5bdb0-137">Um die erforderliche Puffergröße zu ermitteln, **Geben Sie** für " *ppropdata* " den Wert NULL und für *cbpropdata* den Wert 0 (null) an.</span><span class="sxs-lookup"><span data-stu-id="5bdb0-137">To determine the necessary buffer size, specify **NULL** for *pPropData* and zero (0) for *cbPropData*.</span></span> <span data-ttu-id="5bdb0-138">Diese Methode gibt die erforderliche Puffergröße in *pcbreturned* zurück.</span><span class="sxs-lookup"><span data-stu-id="5bdb0-138">This method returns the necessary buffer size in *pcbReturned*.</span></span>

<span data-ttu-id="5bdb0-139">Sie müssen "KS. h" vor "ksproxy. h" einschließen.</span><span class="sxs-lookup"><span data-stu-id="5bdb0-139">You must include Ks.h before Ksproxy.h.</span></span>

## <a name="examples"></a><span data-ttu-id="5bdb0-140">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5bdb0-140">Examples</span></span>

<span data-ttu-id="5bdb0-141">Im folgenden Beispiel wird eine PIN für die PIN-Kategorie durch Abrufen der Eigenschaft **amproperty- \_ Pin- \_ Kategorie** abgefragt.</span><span class="sxs-lookup"><span data-stu-id="5bdb0-141">The following example queries a pin for its pin category, by retrieving the **AMPROPERTY\_PIN\_CATEGORY** property.</span></span> <span data-ttu-id="5bdb0-142">(Siehe [PIN-Eigenschaften Satz](pin-property-set.md).)</span><span class="sxs-lookup"><span data-stu-id="5bdb0-142">(See [Pin Property Set](pin-property-set.md).)</span></span>


```C++
HRESULT GetPinCategory(IPin *pPin, GUID *pPinCategory)
{
    IKsPropertySet *pKs = NULL;

    HRESULT hr = pPin->QueryInterface(IID_PPV_ARGS(&pKs));
    if (FAILED(hr))
    {
        return hr;
    }

    // Try to retrieve the pin category.
    DWORD cbReturned = 0;
    hr = pKs->Get(AMPROPSETID_Pin, AMPROPERTY_PIN_CATEGORY, NULL, 0, 
        pPinCategory, sizeof(GUID), &cbReturned);
    
    // If this succeeded, pPinCategory now contains the category GUID.

    SafeRelease(&pKs);
    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="5bdb0-143">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5bdb0-143">Requirements</span></span>



| <span data-ttu-id="5bdb0-144">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5bdb0-144">Requirement</span></span> | <span data-ttu-id="5bdb0-145">Wert</span><span class="sxs-lookup"><span data-stu-id="5bdb0-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5bdb0-146">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5bdb0-146">Minimum supported client</span></span><br/> | <span data-ttu-id="5bdb0-147">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5bdb0-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="5bdb0-148">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5bdb0-148">Minimum supported server</span></span><br/> | <span data-ttu-id="5bdb0-149">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5bdb0-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="5bdb0-150">Header</span><span class="sxs-lookup"><span data-stu-id="5bdb0-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="5bdb0-151"><dt>Ksproxy. h</dt></span><span class="sxs-lookup"><span data-stu-id="5bdb0-151"><dt>Ksproxy.h</dt></span></span> </dl>    |
| <span data-ttu-id="5bdb0-152">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="5bdb0-152">Library</span></span><br/>                  | <dl> <span data-ttu-id="5bdb0-153"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="5bdb0-153"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5bdb0-154">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5bdb0-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5bdb0-155">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="5bdb0-155">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> <dt>

[<span data-ttu-id="5bdb0-156">**"Ikspropertyset"-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="5bdb0-156">**IKsPropertySet Interface**</span></span>](ikspropertyset.md)
</dt> <dt>

[<span data-ttu-id="5bdb0-157">Eigenschaftensätze</span><span class="sxs-lookup"><span data-stu-id="5bdb0-157">Property Sets</span></span>](property-sets.md)
</dt> </dl>

 

 
