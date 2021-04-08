---
description: Gibt an, ob eine Media Foundation Transformation (MFT) Attribute aus Eingabe Beispielen in Ausgabe Beispiele kopiert.
ms.assetid: 039ecb35-9aa9-4e8a-bbbc-042b9c4c874c
title: MFPKEY_EXATTRIBUTE_SUPPORTED-Eigenschaft (MF Transform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33017111eba95f54e88671cbcf026b3f40812a08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864160"
---
# <a name="mfpkey_exattribute_supported-property"></a><span data-ttu-id="1e50d-103">\_Unterstützte Eigenschaft "mfpkey exattribute" \_</span><span class="sxs-lookup"><span data-stu-id="1e50d-103">MFPKEY\_EXATTRIBUTE\_SUPPORTED property</span></span>

<span data-ttu-id="1e50d-104">Gibt an, ob eine Media Foundation Transformation (MFT) Attribute aus Eingabe Beispielen in Ausgabe Beispiele kopiert.</span><span class="sxs-lookup"><span data-stu-id="1e50d-104">Specifies whether a Media Foundation transform (MFT) copies attributes from input samples to output samples.</span></span>



<span data-ttu-id="1e50d-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="1e50d-105">Data type</span></span>

<span data-ttu-id="1e50d-106">PROPVARIANT-Typ (VT)</span><span class="sxs-lookup"><span data-stu-id="1e50d-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="1e50d-107">PROPVARIANT-Member</span><span class="sxs-lookup"><span data-stu-id="1e50d-107">PROPVARIANT member</span></span>

<span data-ttu-id="1e50d-108">**Variant \_ bool**</span><span class="sxs-lookup"><span data-stu-id="1e50d-108">**VARIANT\_BOOL**</span></span>

<span data-ttu-id="1e50d-109">VT \_ bool</span><span class="sxs-lookup"><span data-stu-id="1e50d-109">VT\_BOOL</span></span>

<span data-ttu-id="1e50d-110">**Boolesche Werte**</span><span class="sxs-lookup"><span data-stu-id="1e50d-110">**boolVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="1e50d-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1e50d-111">Remarks</span></span>

<span data-ttu-id="1e50d-112">Dieses Attribut kann die folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="1e50d-112">This attribute can have the following values.</span></span>



| <span data-ttu-id="1e50d-113">Wert</span><span class="sxs-lookup"><span data-stu-id="1e50d-113">Value</span></span>              | <span data-ttu-id="1e50d-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1e50d-114">Description</span></span>                                                                                                                                             |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e50d-115">**Variant \_ true**</span><span class="sxs-lookup"><span data-stu-id="1e50d-115">**VARIANT\_TRUE**</span></span>  | <span data-ttu-id="1e50d-116">Die MFT kopiert Attribute aus den Eingabe Beispielen in die Ausgabe Beispiele.</span><span class="sxs-lookup"><span data-stu-id="1e50d-116">The MFT copies attributes from the input samples to the output samples.</span></span>                                                                                 |
| <span data-ttu-id="1e50d-117">**Variant \_ false**</span><span class="sxs-lookup"><span data-stu-id="1e50d-117">**VARIANT\_FALSE**</span></span> | <span data-ttu-id="1e50d-118">Die Medien Sitzung kopiert Attribute aus Eingabe Beispielen in Ausgabe Beispiele.</span><span class="sxs-lookup"><span data-stu-id="1e50d-118">The Media Session copies attributes from input samples to output samples.</span></span> <span data-ttu-id="1e50d-119">Er überschreibt keine Attribute, die der MFT für die Ausgabe Beispiele festlegt.</span><span class="sxs-lookup"><span data-stu-id="1e50d-119">It does not overwrite any attributes that the MFT sets on the output samples.</span></span> |



 

<span data-ttu-id="1e50d-120">Zum Abrufen dieses Attributs aufrufen Sie **QueryInterface** für die **IPropertyStore** -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="1e50d-120">To get this attribute, call **QueryInterface** on the MFT for the **IPropertyStore** interface.</span></span>

<span data-ttu-id="1e50d-121">Der Standardwert ist **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="1e50d-121">The default value is **VARIANT\_FALSE**.</span></span> <span data-ttu-id="1e50d-122">Wenn die MFT die **IPropertyStore** -Schnittstelle nicht verfügbar macht oder diese Eigenschaft nicht festgelegt ist, wird der Wert als **Variant \_ false** behandelt.</span><span class="sxs-lookup"><span data-stu-id="1e50d-122">If the MFT does not expose the **IPropertyStore** interface, or if this property is not set, treat the value as **VARIANT\_FALSE**.</span></span>

<span data-ttu-id="1e50d-123">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="1e50d-123">This property is read-only.</span></span>

> [!NOTE] 
> <span data-ttu-id="1e50d-124">Dieses Attribut gilt nicht für asynchrone MFTs.</span><span class="sxs-lookup"><span data-stu-id="1e50d-124">This attribute does not apply to asynchronous MFTs.</span></span> <span data-ttu-id="1e50d-125">Attribute werden nicht unabhängig vom Wert dieses Attributs aus den Eingabe Beispielen in die Ausgabe Beispiele für asynchrone MFTs kopiert.</span><span class="sxs-lookup"><span data-stu-id="1e50d-125">Attributes will not be copied from the input samples to the output samples for asynchronous MFTs, regardless of the value of this attribute.</span></span>

## <a name="examples"></a><span data-ttu-id="1e50d-126">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1e50d-126">Examples</span></span>

<span data-ttu-id="1e50d-127">Im folgenden Beispiel wird Variant true zurückgegeben, \_ Wenn ein MFT Beispiel Attribute kopiert.</span><span class="sxs-lookup"><span data-stu-id="1e50d-127">The following example returns VARIANT\_TRUE if an MFT copies sample attributes.</span></span>


```C++
BOOL TransformCopiesSampleAttributes(IMFTransform *pMFT)
{
    BOOL bCopiesAttributes = FALSE;

    IPropertyStore *pProps = NULL;

    HRESULT hr = pMFT->QueryInterface(IID_PPV_ARGS(&pProps));
    
    if (SUCCEEDED(hr))
    {
        PROPVARIANT var;
        hr = pProps->GetValue(MFPKEY_EXATTRIBUTE_SUPPORTED, &var);

        if (SUCCEEDED(hr))
        {
            bCopiesAttributes = 
                (var.vt == VT_BOOL && var.boolVal == VARIANT_TRUE);

            PropVariantClear(&var);
        }
        pProps->Release();
    }
    return bCopiesAttributes;
}
```



## <a name="requirements"></a><span data-ttu-id="1e50d-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1e50d-128">Requirements</span></span>



| <span data-ttu-id="1e50d-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1e50d-129">Requirement</span></span> | <span data-ttu-id="1e50d-130">Wert</span><span class="sxs-lookup"><span data-stu-id="1e50d-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e50d-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1e50d-131">Minimum supported client</span></span><br/> | <span data-ttu-id="1e50d-132">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1e50d-132">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="1e50d-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1e50d-133">Minimum supported server</span></span><br/> | <span data-ttu-id="1e50d-134">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1e50d-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="1e50d-135">Header</span><span class="sxs-lookup"><span data-stu-id="1e50d-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="1e50d-136"><dt>"MF Transform. h"</dt></span><span class="sxs-lookup"><span data-stu-id="1e50d-136"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e50d-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1e50d-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e50d-138">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1e50d-138">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="1e50d-139">Beispiel Attribute</span><span class="sxs-lookup"><span data-stu-id="1e50d-139">Sample Attributes</span></span>](sample-attributes.md)
</dt> <dt>

[<span data-ttu-id="1e50d-140">**IMF Transform::P rocess Output**</span><span class="sxs-lookup"><span data-stu-id="1e50d-140">**IMFTransform::ProcessOutput**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput)
</dt> </dl>

 

 




