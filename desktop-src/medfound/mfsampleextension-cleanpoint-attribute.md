---
description: Gibt an, ob ein Beispiel ein zufälliger Zugriffspunkt ist.
ms.assetid: 03d4bfd8-1148-4551-8e71-05cfba2e15fa
title: MFSampleExtension_CleanPoint-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a54ea9bf4f1ca207a6ab12bac331c57db63136a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527947"
---
# <a name="mfsampleextension_cleanpoint-attribute"></a><span data-ttu-id="6daea-103">MF Sample Extension- \_ cleanpointattribut</span><span class="sxs-lookup"><span data-stu-id="6daea-103">MFSampleExtension\_CleanPoint attribute</span></span>

<span data-ttu-id="6daea-104">Gibt an, ob ein Beispiel ein zufälliger Zugriffspunkt ist.</span><span class="sxs-lookup"><span data-stu-id="6daea-104">Indicates whether a sample is a random access point.</span></span>

## <a name="data-type"></a><span data-ttu-id="6daea-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="6daea-105">Data type</span></span>

<span data-ttu-id="6daea-106">**Bool** gespeichert als **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6daea-106">**BOOL** stored as **UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="6daea-107">Abrufen/Festlegen</span><span class="sxs-lookup"><span data-stu-id="6daea-107">Get/set</span></span>

<span data-ttu-id="6daea-108">Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="6daea-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="6daea-109">Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="6daea-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="6daea-110">Gilt für:</span><span class="sxs-lookup"><span data-stu-id="6daea-110">Applies to</span></span>

[<span data-ttu-id="6daea-111">**IMF Sample**</span><span class="sxs-lookup"><span data-stu-id="6daea-111">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a><span data-ttu-id="6daea-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6daea-112">Remarks</span></span>

<span data-ttu-id="6daea-113">Dieses Attribut gilt für-Beispiele.</span><span class="sxs-lookup"><span data-stu-id="6daea-113">This attribute applies to samples.</span></span> <span data-ttu-id="6daea-114">Wenn das Attribut **true** ist, ist das Beispiel ein zufälliger Zugriffspunkt, und die Decodierung kann mit diesem Beispiel beginnen.</span><span class="sxs-lookup"><span data-stu-id="6daea-114">If the attribute is **TRUE**, the sample is a random access point and decoding can begin from this sample.</span></span> <span data-ttu-id="6daea-115">Andernfalls ist das Beispiel kein zufälliger Zugriffspunkt.</span><span class="sxs-lookup"><span data-stu-id="6daea-115">Otherwise, the sample is not a random access point.</span></span>

<span data-ttu-id="6daea-116">Wenn dieses Attribut nicht festgelegt ist, ist der Standardwert **false**.</span><span class="sxs-lookup"><span data-stu-id="6daea-116">If this attribute is not set, the default value is **FALSE**.</span></span>

<span data-ttu-id="6daea-117">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="6daea-117">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="examples"></a><span data-ttu-id="6daea-118">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6daea-118">Examples</span></span>


```C++
inline BOOL IsRandomAccessPoint(IMFSample *pSample)
{
    // Check for the "clean point" attribute. Default to FALSE.
    return MFGetAttributeUINT32(pSample, MFSampleExtension_CleanPoint, FALSE);
}
```



## <a name="requirements"></a><span data-ttu-id="6daea-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6daea-119">Requirements</span></span>



| <span data-ttu-id="6daea-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6daea-120">Requirement</span></span> | <span data-ttu-id="6daea-121">Wert</span><span class="sxs-lookup"><span data-stu-id="6daea-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6daea-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6daea-122">Minimum supported client</span></span><br/> | <span data-ttu-id="6daea-123">Windows Vista \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="6daea-123">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="6daea-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6daea-124">Minimum supported server</span></span><br/> | <span data-ttu-id="6daea-125">Windows Server 2008 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="6daea-125">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="6daea-126">Header</span><span class="sxs-lookup"><span data-stu-id="6daea-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="6daea-127"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="6daea-127"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6daea-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6daea-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6daea-129">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="6daea-129">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="6daea-130">Beispiel Attribute</span><span class="sxs-lookup"><span data-stu-id="6daea-130">Sample Attributes</span></span>](sample-attributes.md)
</dt> <dt>

[<span data-ttu-id="6daea-131">Medien Beispiele</span><span class="sxs-lookup"><span data-stu-id="6daea-131">Media Samples</span></span>](media-samples.md)
</dt> </dl>

 

 




