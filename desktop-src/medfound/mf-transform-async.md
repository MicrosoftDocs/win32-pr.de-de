---
description: Gibt an, ob eine Media Foundation Transformation (MFT) asynchrone Verarbeitung durchführt.
ms.assetid: fcc70282-cfac-487c-b9ff-39e62c836f8b
title: MF_TRANSFORM_ASYNC-Attribut (MF Transform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89622bd7bb7fa3e8306c94b02f90217b6367d21b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753152"
---
# <a name="mf_transform_async-attribute"></a><span data-ttu-id="0ac97-103">Asynchrones \_ Transform- \_ Attribut</span><span class="sxs-lookup"><span data-stu-id="0ac97-103">MF\_TRANSFORM\_ASYNC attribute</span></span>

<span data-ttu-id="0ac97-104">Gibt an, ob eine Media Foundation Transformation (MFT) asynchrone Verarbeitung durchführt.</span><span class="sxs-lookup"><span data-stu-id="0ac97-104">Specifies whether a Media Foundation transform (MFT) performs asynchronous processing.</span></span>

## <a name="data-type"></a><span data-ttu-id="0ac97-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="0ac97-105">Data type</span></span>

<span data-ttu-id="0ac97-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="0ac97-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="0ac97-107">Abrufen/Festlegen</span><span class="sxs-lookup"><span data-stu-id="0ac97-107">Get/set</span></span>

<span data-ttu-id="0ac97-108">Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="0ac97-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="0ac97-109">Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="0ac97-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="0ac97-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0ac97-110">Remarks</span></span>

<span data-ttu-id="0ac97-111">Das-Attribut ist ein boolescher Wert:</span><span class="sxs-lookup"><span data-stu-id="0ac97-111">The attribute is a Boolean value:</span></span>

-   <span data-ttu-id="0ac97-112">Wenn das-Attribut ungleich 0 (null) ist, führt die MFT die asynchrone Verarbeitung aus.</span><span class="sxs-lookup"><span data-stu-id="0ac97-112">If the attribute is nonzero, the MFT performs asynchronous processing.</span></span>
-   <span data-ttu-id="0ac97-113">Wenn das Attribut 0 oder nicht festgelegt ist, ist der MFT synchron.</span><span class="sxs-lookup"><span data-stu-id="0ac97-113">If the attribute is 0 or not set, the MFT is synchronous.</span></span>

<span data-ttu-id="0ac97-114">Zum Abrufen dieses Attributs müssen Sie zuerst [**imftransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) aufrufen, um den MFT-Attribut Speicher zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="0ac97-114">To get this attribute, first call [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) to get the MFT's attribute store.</span></span> <span data-ttu-id="0ac97-115">Wenn diese Methode erfolgreich ausgeführt wird, müssen Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) abrufen, um den Attribut Wert zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="0ac97-115">If that method succeeds, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) to get the attribute value.</span></span> <span data-ttu-id="0ac97-116">Wenn eine der beiden Methoden fehlschlägt, ist die MFT synchron.</span><span class="sxs-lookup"><span data-stu-id="0ac97-116">If either of the two methods fails, the MFT is synchronous.</span></span>

<span data-ttu-id="0ac97-117">Für asynchrone MFTs muss dieses Attribut auf einen Wert ungleich 0 (null) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="0ac97-117">For asynchronous MFTs, this attribute must be set to a nonzero value.</span></span> <span data-ttu-id="0ac97-118">Bei synchronen MFTs ist dieses Attribut optional, muss jedoch auf 0 (null) festgelegt werden, wenn es vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="0ac97-118">For synchronous MFTs, this attribute is optional, but must be set to 0 if present.</span></span>

<span data-ttu-id="0ac97-119">Asynchrone MFTs sind nicht kompatibel mit früheren Versionen von Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="0ac97-119">Asynchronous MFTs are not compatible with earlier versions of Media Foundation.</span></span> <span data-ttu-id="0ac97-120">Um eine asynchrone MFT zu verwenden, muss der Client das Attribut " [**MF \_ Transform \_ Async \_ Unlock**](mf-transform-async-unlock.md) " auf dem MFT festlegen.</span><span class="sxs-lookup"><span data-stu-id="0ac97-120">To use an asynchronous MFT, the client must set the [**MF\_TRANSFORM\_ASYNC\_UNLOCK**](mf-transform-async-unlock.md) attribute on the MFT.</span></span> <span data-ttu-id="0ac97-121">(Die Microsoft Media Foundation Pipeline führt diesen Schritt automatisch aus.)</span><span class="sxs-lookup"><span data-stu-id="0ac97-121">(The Microsoft Media Foundation pipeline performs this step automatically.)</span></span>

## <a name="examples"></a><span data-ttu-id="0ac97-122">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0ac97-122">Examples</span></span>

<span data-ttu-id="0ac97-123">Der folgende Code testet, ob eine MFT asynchrone Verarbeitung durchführt.</span><span class="sxs-lookup"><span data-stu-id="0ac97-123">The following code tests whether an MFT performs asynchronous processing.</span></span>


```C++
BOOL IsTransformAsync(IMFTransform *pMFT)
{
    BOOL bAsync = FALSE;
    IMFAttributes *pAttributes = NULL;

    HRESULT hr = pMFT->GetAttributes(&pAttributes);
    if (SUCCEEDED(hr))
    {
        bAsync = MFGetAttributeUINT32(pAttributes, MF_TRANSFORM_ASYNC, FALSE);
        pAttributes->Release();
    }

    return (bAsync != FALSE);
}
```



## <a name="requirements"></a><span data-ttu-id="0ac97-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0ac97-124">Requirements</span></span>



| <span data-ttu-id="0ac97-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0ac97-125">Requirement</span></span> | <span data-ttu-id="0ac97-126">Wert</span><span class="sxs-lookup"><span data-stu-id="0ac97-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ac97-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0ac97-127">Minimum supported client</span></span><br/> | <span data-ttu-id="0ac97-128">Windows 7 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="0ac97-128">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="0ac97-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0ac97-129">Minimum supported server</span></span><br/> | <span data-ttu-id="0ac97-130">Windows Server 2008 R2 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="0ac97-130">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="0ac97-131">Header</span><span class="sxs-lookup"><span data-stu-id="0ac97-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="0ac97-132"><dt>"MF Transform. h"</dt></span><span class="sxs-lookup"><span data-stu-id="0ac97-132"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ac97-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0ac97-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ac97-134">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="0ac97-134">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="0ac97-135">Asynchrone MFTs</span><span class="sxs-lookup"><span data-stu-id="0ac97-135">Asynchronous MFTs</span></span>](asynchronous-mfts.md)
</dt> <dt>

[<span data-ttu-id="0ac97-136">Transformations Attribute</span><span class="sxs-lookup"><span data-stu-id="0ac97-136">Transform Attributes</span></span>](transform-attributes.md)
</dt> <dt>

[<span data-ttu-id="0ac97-137">**MF- \_ Transformation \_ Async \_ Unlock**</span><span class="sxs-lookup"><span data-stu-id="0ac97-137">**MF\_TRANSFORM\_ASYNC\_UNLOCK**</span></span>](mf-transform-async-unlock.md)
</dt> </dl>

 

 




