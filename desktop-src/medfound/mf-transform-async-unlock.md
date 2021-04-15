---
description: Aktiviert die Verwendung einer asynchronen Media Foundation Transformation (MFT).
ms.assetid: e12ab57e-ebc2-46af-afdf-d78d4db16fcf
title: MF_TRANSFORM_ASYNC_UNLOCK-Attribut (MF Transform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e7876b3f1fca80e881414399d40e69112a64d8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527401"
---
# <a name="mf_transform_async_unlock-attribute"></a><span data-ttu-id="0f3b7-103">MF \_ Transform \_ Async \_ Unlock Attribute</span><span class="sxs-lookup"><span data-stu-id="0f3b7-103">MF\_TRANSFORM\_ASYNC\_UNLOCK attribute</span></span>

<span data-ttu-id="0f3b7-104">Aktiviert die Verwendung einer asynchronen Media Foundation Transformation (MFT).</span><span class="sxs-lookup"><span data-stu-id="0f3b7-104">Enables the use of an asynchronous Media Foundation transform (MFT).</span></span>

## <a name="data-type"></a><span data-ttu-id="0f3b7-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="0f3b7-105">Data type</span></span>

<span data-ttu-id="0f3b7-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="0f3b7-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="0f3b7-107">Abrufen/Festlegen</span><span class="sxs-lookup"><span data-stu-id="0f3b7-107">Get/set</span></span>

<span data-ttu-id="0f3b7-108">Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="0f3b7-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="0f3b7-109">Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="0f3b7-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="0f3b7-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0f3b7-110">Remarks</span></span>

<span data-ttu-id="0f3b7-111">Asynchrone MFTs sind nicht kompatibel mit früheren Versionen von Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="0f3b7-111">Asynchronous MFTs are not compatible with earlier versions of Microsoft Media Foundation.</span></span> <span data-ttu-id="0f3b7-112">Um zu verhindern, dass vorhandene Anwendungen versehentlich ein asynchrones MFT verwenden, muss dieses Attribut auf einen Wert ungleich 0 (null) festgelegt werden, bevor ein asynchroner MFT verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="0f3b7-112">To prevent existing applications from accidentally using an asynchronous MFT, this attribute must be set to a nonzero value before an asynchronous MFT can be used.</span></span> <span data-ttu-id="0f3b7-113">Das-Attribut wird von der Media Foundation Pipeline automatisch festgelegt, sodass die meisten Anwendungen dieses Attribut nicht verwenden müssen.</span><span class="sxs-lookup"><span data-stu-id="0f3b7-113">The Media Foundation pipeline automatically sets the attribute, so that most applications do not need to use this attribute.</span></span> <span data-ttu-id="0f3b7-114">Wenn eine Anwendung jedoch ein asynchrones MFT außerhalb der Media Foundation Pipeline verwendet, muss die Anwendung dieses Attribut festlegen.</span><span class="sxs-lookup"><span data-stu-id="0f3b7-114">However, if an application uses an asynchronous MFT outside of the Media Foundation pipeline, the application must set this attribute.</span></span>

<span data-ttu-id="0f3b7-115">Synchrone MFTs benötigen dieses Attribut nicht.</span><span class="sxs-lookup"><span data-stu-id="0f3b7-115">Synchronous MFTs do not require this attribute.</span></span>

<span data-ttu-id="0f3b7-116">Um zu testen, ob eine MFT asynchron ist, erhalten Sie den Wert des " [MF \_ Transform \_ Async](mf-transform-async.md) "-Attributs für die MFT.</span><span class="sxs-lookup"><span data-stu-id="0f3b7-116">To test whether an MFT is asynchronous, get the value of the [MF\_TRANSFORM\_ASYNC](mf-transform-async.md) attribute on the MFT.</span></span>

## <a name="examples"></a><span data-ttu-id="0f3b7-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0f3b7-117">Examples</span></span>

<span data-ttu-id="0f3b7-118">Mit dem folgenden Code wird ein asynchroner MFT entsperrt.</span><span class="sxs-lookup"><span data-stu-id="0f3b7-118">The following code unlocks an asynchronous MFT.</span></span>


```C++
HRESULT UnlockAsyncMFT(IMFTransform *pMFT)
{
    IMFAttributes *pAttributes = NULL;

    HRESULT hr = hr = pMFT->GetAttributes(&pAttributes);

    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetUINT32(MF_TRANSFORM_ASYNC_UNLOCK, TRUE);
        pAttributes->Release();
    }
    
    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="0f3b7-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0f3b7-119">Requirements</span></span>



| <span data-ttu-id="0f3b7-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0f3b7-120">Requirement</span></span> | <span data-ttu-id="0f3b7-121">Wert</span><span class="sxs-lookup"><span data-stu-id="0f3b7-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f3b7-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0f3b7-122">Minimum supported client</span></span><br/> | <span data-ttu-id="0f3b7-123">Windows 7 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="0f3b7-123">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="0f3b7-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0f3b7-124">Minimum supported server</span></span><br/> | <span data-ttu-id="0f3b7-125">Windows Server 2008 R2 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="0f3b7-125">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="0f3b7-126">Header</span><span class="sxs-lookup"><span data-stu-id="0f3b7-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="0f3b7-127"><dt>"MF Transform. h"</dt></span><span class="sxs-lookup"><span data-stu-id="0f3b7-127"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f3b7-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0f3b7-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f3b7-129">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="0f3b7-129">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="0f3b7-130">Asynchrone MFTs</span><span class="sxs-lookup"><span data-stu-id="0f3b7-130">Asynchronous MFTs</span></span>](asynchronous-mfts.md)
</dt> <dt>

[<span data-ttu-id="0f3b7-131">Transformations Attribute</span><span class="sxs-lookup"><span data-stu-id="0f3b7-131">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 




