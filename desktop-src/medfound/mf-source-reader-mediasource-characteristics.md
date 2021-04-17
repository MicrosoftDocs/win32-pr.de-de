---
description: Ruft die Merkmale der Medienquelle vom Quell Leser ab.
ms.assetid: 4cd48b69-6f7b-4b13-86f3-b38969025f70
title: MF_SOURCE_READER_MEDIASOURCE_CHARACTERISTICS-Attribut (mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de4d1ed026f7b74f290446af74a6cf9947612617
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "104351709"
---
# <a name="mf_source_reader_mediasource_characteristics-attribute"></a><span data-ttu-id="4dcee-103">MF- \_ Quell \_ Leser \_ MediaSource- \_ Merkmale-Attribut</span><span class="sxs-lookup"><span data-stu-id="4dcee-103">MF\_SOURCE\_READER\_MEDIASOURCE\_CHARACTERISTICS attribute</span></span>

<span data-ttu-id="4dcee-104">Ruft die Merkmale der Medienquelle vom [Quell Leser](source-reader.md)ab.</span><span class="sxs-lookup"><span data-stu-id="4dcee-104">Gets the characteristics of the media source from the [Source Reader](source-reader.md).</span></span>

## <a name="data-type"></a><span data-ttu-id="4dcee-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="4dcee-105">Data type</span></span>

<span data-ttu-id="4dcee-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="4dcee-106">**UINT32**</span></span>

<span data-ttu-id="4dcee-107">Der Wert ist eine bitweise **or** -from-Flags aus der [**mfmediasource- \_ Eigenschaften**](/windows/desktop/api/mfidl/ne-mfidl-mfmediasource_characteristics) -Enumeration.</span><span class="sxs-lookup"><span data-stu-id="4dcee-107">The value is a bitwise **OR** of flags from the [**MFMEDIASOURCE\_CHARACTERISTICS**](/windows/desktop/api/mfidl/ne-mfidl-mfmediasource_characteristics) enumeration.</span></span>

## <a name="remarks"></a><span data-ttu-id="4dcee-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4dcee-108">Remarks</span></span>

<span data-ttu-id="4dcee-109">Um dieses Attribut abzurufen, nennen Sie die [**imfsourcereader:: getpresentationattribute**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getpresentationattribute) -Methode für den Quell-Reader.</span><span class="sxs-lookup"><span data-stu-id="4dcee-109">To get this attribute, call the [**IMFSourceReader::GetPresentationAttribute**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getpresentationattribute) method on the source reader.</span></span> <span data-ttu-id="4dcee-110">Legen Sie den Parameter " *dwstreamindex* " auf den **MF- \_ Quell \_ Leser " \_ MediaSource** " und den *GuidAttribute* -Parameter auf "MF \_ Source \_ Reader \_ MediaSource" fest \_ .</span><span class="sxs-lookup"><span data-stu-id="4dcee-110">Set the *dwStreamIndex* parameter to **MF\_SOURCE\_READER\_MEDIASOURCE** and the *guidAttribute* parameter to MF\_SOURCE\_READER\_MEDIASOURCE\_CHARACTERISTICS.</span></span>

<span data-ttu-id="4dcee-111">Der **PROPVARIANT** -Typ für dieses Attribut ist " **VT \_ UI4**".</span><span class="sxs-lookup"><span data-stu-id="4dcee-111">The **PROPVARIANT** type for this attribute is **VT\_UI4**.</span></span>

## <a name="examples"></a><span data-ttu-id="4dcee-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4dcee-112">Examples</span></span>


```C++
HRESULT GetSourceFlags(IMFSourceReader *pReader, ULONG *pulFlags)
{
    ULONG flags = 0;

    PROPVARIANT var;
    PropVariantInit(&var);

    HRESULT hr = pReader->GetPresentationAttribute(
        MF_SOURCE_READER_MEDIASOURCE, 
        MF_SOURCE_READER_MEDIASOURCE_CHARACTERISTICS, 
        &var);

    if (SUCCEEDED(hr))
    {
        hr = PropVariantToUInt32(var, &flags);
    }
    if (SUCCEEDED(hr))
    {
        *pulFlags = flags;
    }

    PropVariantClear(&var);
    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="4dcee-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4dcee-113">Requirements</span></span>



| <span data-ttu-id="4dcee-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4dcee-114">Requirement</span></span> | <span data-ttu-id="4dcee-115">Wert</span><span class="sxs-lookup"><span data-stu-id="4dcee-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="4dcee-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4dcee-116">Minimum supported client</span></span><br/> | <span data-ttu-id="4dcee-117">Windows 7 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="4dcee-117">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="4dcee-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4dcee-118">Minimum supported server</span></span><br/> | <span data-ttu-id="4dcee-119">Windows Server 2008 R2 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="4dcee-119">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="4dcee-120">Header</span><span class="sxs-lookup"><span data-stu-id="4dcee-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="4dcee-121"><dt>"Mfreadwrite. h"</dt></span><span class="sxs-lookup"><span data-stu-id="4dcee-121"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4dcee-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4dcee-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4dcee-123">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="4dcee-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="4dcee-124">Quell Leser</span><span class="sxs-lookup"><span data-stu-id="4dcee-124">Source Reader</span></span>](source-reader.md)
</dt> </dl>

 

 




