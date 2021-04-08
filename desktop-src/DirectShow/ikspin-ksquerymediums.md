---
description: Die ksquerymediums-Methode ruft die von einer PIN unterstützten Medien ab.
ms.assetid: 554bf968-6054-4f9d-95db-facf0444641f
title: 'Ikspin:: ksquerymediums-Methode (ksproxy. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IKsPin.KsQueryMediums
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
ms.openlocfilehash: f037317b49bc54f5ea9db5b7a4ae039ec0a9970d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746576"
---
# <a name="ikspinksquerymediums-method"></a><span data-ttu-id="e3d03-103">Ikspin:: ksquerymediums-Methode</span><span class="sxs-lookup"><span data-stu-id="e3d03-103">IKsPin::KsQueryMediums method</span></span>

<span data-ttu-id="e3d03-104">Die- `KsQueryMediums` Methode ruft die von einer PIN unterstützten Medien ab.</span><span class="sxs-lookup"><span data-stu-id="e3d03-104">The `KsQueryMediums` method retrieves the mediums supported by a pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3d03-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e3d03-105">Syntax</span></span>


```C++
HRESULT KsQueryMediums(
  [out] KSMULTIPLE_ITEM **ppmi
);
```



## <a name="parameters"></a><span data-ttu-id="e3d03-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e3d03-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3d03-107">*ppmi* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="e3d03-107">*ppmi* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e3d03-108">Adresse eines Zeigers auf eine [**ksmultiple- \_ Element**](ksmultiple-item.md) Struktur.</span><span class="sxs-lookup"><span data-stu-id="e3d03-108">Address of a pointer to a [**KSMULTIPLE\_ITEM**](ksmultiple-item.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3d03-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e3d03-109">Return value</span></span>

<span data-ttu-id="e3d03-110">Wenn die Methode erfolgreich ausgeführt wird, gibt Sie S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="e3d03-110">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="e3d03-111">Wenn ein Fehler auftritt, wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e3d03-111">If it fails, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e3d03-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e3d03-112">Remarks</span></span>

<span data-ttu-id="e3d03-113">Diese Methode gibt eine Aufgabe zugeordnete [**ksmultiple- \_ Element**](ksmultiple-item.md) Struktur zurück, auf die 0 (null) oder mehr [**regpinmedium**](/windows/desktop/api/strmif/ns-strmif-regpinmedium) -Strukturen folgt.</span><span class="sxs-lookup"><span data-stu-id="e3d03-113">This method returns a task-allocated [**KSMULTIPLE\_ITEM**](ksmultiple-item.md) structure, which is followed by zero or more [**REGPINMEDIUM**](/windows/desktop/api/strmif/ns-strmif-regpinmedium) structures.</span></span> <span data-ttu-id="e3d03-114">Der **count** -Member der **ksmultiple- \_ Element** Struktur gibt die Anzahl der **regpinmedium** -Strukturen an.</span><span class="sxs-lookup"><span data-stu-id="e3d03-114">The **Count** member of the **KSMULTIPLE\_ITEM** structure specifies the number of **REGPINMEDIUM** structures.</span></span> <span data-ttu-id="e3d03-115">Jede **regpinmedium** -Struktur definiert ein Medium, das von der PIN unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="e3d03-115">Each **REGPINMEDIUM** structure defines a medium supported by the pin.</span></span>

<span data-ttu-id="e3d03-116">Der Aufrufer muss die zurückgegebenen Strukturen mit der **CoTaskMemFree** -Funktion freigeben.</span><span class="sxs-lookup"><span data-stu-id="e3d03-116">The caller must free the returned structures, using the **CoTaskMemFree** function.</span></span>

<span data-ttu-id="e3d03-117">Sie müssen "KS. h" vor "ksproxy. h" einschließen.</span><span class="sxs-lookup"><span data-stu-id="e3d03-117">You must include Ks.h before Ksproxy.h.</span></span>

## <a name="examples"></a><span data-ttu-id="e3d03-118">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e3d03-118">Examples</span></span>

<span data-ttu-id="e3d03-119">Die folgende Hilfsfunktion versucht, eine PIN mit einem angegebenen Medium abzugleichen.</span><span class="sxs-lookup"><span data-stu-id="e3d03-119">The following helper function attempts to match a pin against a specified medium.</span></span>


```C++
HRESULT FindMatchingMedium(
    IPin *pPin, 
    REGPINMEDIUM *pMedium, 
    bool *pfMatch)
{
    IKsPin* pKsPin = NULL;
    KSMULTIPLE_ITEM *pmi;

    *pfMatch = false;
    HRESULT hr = pPin->QueryInterface(IID_IKsPin, (void **)&pKsPin);
    if (FAILED(hr)) 
        return hr;  // Pin does not support IKsPin.

    hr = pKsPin->KsQueryMediums(&pmi);
    pKsPin->Release();
    if (FAILED(hr))
        return hr;  // Pin does not support mediums.

    if (pmi->Count) 
    {
        // Use pointer arithmetic to reference the first medium structure.
        REGPINMEDIUM *pTemp = (REGPINMEDIUM*)(pmi + 1);
        for (ULONG i = 0; i < pmi->Count; i++, pTemp++) 
        {
            if (pMedium->clsMedium == pTemp->clsMedium) 
            {
                *pfMatch = true;
                break;
            }
        }
    }        
    CoTaskMemFree(pmi);
    return S_OK;
}
```



## <a name="requirements"></a><span data-ttu-id="e3d03-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e3d03-120">Requirements</span></span>



| <span data-ttu-id="e3d03-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e3d03-121">Requirement</span></span> | <span data-ttu-id="e3d03-122">Wert</span><span class="sxs-lookup"><span data-stu-id="e3d03-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e3d03-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e3d03-123">Minimum supported client</span></span><br/> | <span data-ttu-id="e3d03-124">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e3d03-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="e3d03-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e3d03-125">Minimum supported server</span></span><br/> | <span data-ttu-id="e3d03-126">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e3d03-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e3d03-127">Header</span><span class="sxs-lookup"><span data-stu-id="e3d03-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="e3d03-128"><dt>Ksproxy. h</dt></span><span class="sxs-lookup"><span data-stu-id="e3d03-128"><dt>Ksproxy.h</dt></span></span> </dl>    |
| <span data-ttu-id="e3d03-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e3d03-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="e3d03-130"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="e3d03-130"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3d03-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e3d03-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3d03-132">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="e3d03-132">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> <dt>

[<span data-ttu-id="e3d03-133">**Ikspin-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="e3d03-133">**IKsPin Interface**</span></span>](ikspin.md)
</dt> <dt>

[<span data-ttu-id="e3d03-134">WDM-Klassen Treiber Filter</span><span class="sxs-lookup"><span data-stu-id="e3d03-134">WDM Class Driver Filters</span></span>](wdm-class-driver-filters.md)
</dt> </dl>

 

 




