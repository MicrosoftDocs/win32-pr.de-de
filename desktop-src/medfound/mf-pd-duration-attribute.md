---
description: Gibt die Dauer einer Präsentation in 100-Nanosecond-Einheiten an.
ms.assetid: abc21696-ea97-41ff-9341-6d9e9dcb19ec
title: MF_PD_DURATION-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ace7bd4f897de0220c2c449ce4fa891ac52eb200
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351781"
---
# <a name="mf_pd_duration-attribute"></a><span data-ttu-id="c2afb-103">MF \_ PD \_ Duration-Attribut</span><span class="sxs-lookup"><span data-stu-id="c2afb-103">MF\_PD\_DURATION attribute</span></span>

<span data-ttu-id="c2afb-104">Gibt die Dauer einer Präsentation in 100-Nanosecond-Einheiten an.</span><span class="sxs-lookup"><span data-stu-id="c2afb-104">Specifies the duration of a presentation, in 100-nanosecond units.</span></span>

## <a name="data-type"></a><span data-ttu-id="c2afb-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="c2afb-105">Data type</span></span>

<span data-ttu-id="c2afb-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="c2afb-106">**UINT64**</span></span>

<span data-ttu-id="c2afb-107">Als **Longlong** -Wert behandeln.</span><span class="sxs-lookup"><span data-stu-id="c2afb-107">Treat as a **LONGLONG** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c2afb-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c2afb-108">Remarks</span></span>

<span data-ttu-id="c2afb-109">Medienquellen können dieses Attribut für einen Präsentations Deskriptor festlegen, um die Dauer der Präsentation anzugeben.</span><span class="sxs-lookup"><span data-stu-id="c2afb-109">Media sources can set this attribute on a presentation descriptor to indicate the duration of the presentation.</span></span>

<span data-ttu-id="c2afb-110">Dieses Attribut ist ein Wert mit Vorzeichen, obwohl er als **UINT64** gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="c2afb-110">This attribute is a signed value, although it is stored as a **UINT64**.</span></span> <span data-ttu-id="c2afb-111">Das Attribut sollte jedoch nie einen negativen Wert enthalten.</span><span class="sxs-lookup"><span data-stu-id="c2afb-111">However, the attribute should never contain a negative value.</span></span>

<span data-ttu-id="c2afb-112">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="c2afb-112">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="examples"></a><span data-ttu-id="c2afb-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c2afb-113">Examples</span></span>

<span data-ttu-id="c2afb-114">Im folgenden Beispiel wird gezeigt, wie Sie die Präsentations Dauer aus einer Medienquelle erhalten.</span><span class="sxs-lookup"><span data-stu-id="c2afb-114">The following example shows how to get the presentation duration from a media source.</span></span>


```C++
HRESULT GetSourceDuration(IMFMediaSource *pSource, MFTIME *pDuration)
{
    *pDuration = 0;

    IMFPresentationDescriptor *pPD = NULL;

    HRESULT hr = pSource->CreatePresentationDescriptor(&pPD);
    if (SUCCEEDED(hr))
    {
        hr = pPD->GetUINT64(MF_PD_DURATION, (UINT64*)pDuration);
        pPD->Release();
    }
    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="c2afb-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c2afb-115">Requirements</span></span>



| <span data-ttu-id="c2afb-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c2afb-116">Requirement</span></span> | <span data-ttu-id="c2afb-117">Wert</span><span class="sxs-lookup"><span data-stu-id="c2afb-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c2afb-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c2afb-118">Minimum supported client</span></span><br/> | <span data-ttu-id="c2afb-119">Windows Vista \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="c2afb-119">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="c2afb-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c2afb-120">Minimum supported server</span></span><br/> | <span data-ttu-id="c2afb-121">Windows Server 2008 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="c2afb-121">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="c2afb-122">Header</span><span class="sxs-lookup"><span data-stu-id="c2afb-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="c2afb-123"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c2afb-123"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2afb-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c2afb-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2afb-125">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="c2afb-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="c2afb-126">**Imfattributes:: GetUINT64**</span><span class="sxs-lookup"><span data-stu-id="c2afb-126">**IMFAttributes::GetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[<span data-ttu-id="c2afb-127">**Imfattributes:: SetUINT64**</span><span class="sxs-lookup"><span data-stu-id="c2afb-127">**IMFAttributes::SetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> <dt>

[<span data-ttu-id="c2afb-128">**IMF presentationdescriptor**</span><span class="sxs-lookup"><span data-stu-id="c2afb-128">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="c2afb-129">Präsentations deskriptorattribute</span><span class="sxs-lookup"><span data-stu-id="c2afb-129">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="c2afb-130">Präsentations Deskriptoren</span><span class="sxs-lookup"><span data-stu-id="c2afb-130">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




