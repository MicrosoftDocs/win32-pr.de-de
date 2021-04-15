---
description: Enthält einen Medientyp, der in einem anderen Medientyp umschließt wurde.
ms.assetid: 3bd94523-0206-44d8-83a2-e569e4ab7815
title: MF_MT_WRAPPED_TYPE-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ad09c69f7b99c2c376a207270cadb034e735546
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393258"
---
# <a name="mf_mt_wrapped_type-attribute"></a><span data-ttu-id="a2a83-103">In das MF- \_ \_ Attribut umschließtes \_</span><span class="sxs-lookup"><span data-stu-id="a2a83-103">MF\_MT\_WRAPPED\_TYPE attribute</span></span>

<span data-ttu-id="a2a83-104">Enthält einen Medientyp, der in einem anderen Medientyp umschließt wurde.</span><span class="sxs-lookup"><span data-stu-id="a2a83-104">Contains a media type that has been wrapped in another media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="a2a83-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="a2a83-105">Data type</span></span>

<span data-ttu-id="a2a83-106">Bytearray</span><span class="sxs-lookup"><span data-stu-id="a2a83-106">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="a2a83-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a2a83-107">Remarks</span></span>

<span data-ttu-id="a2a83-108">Dieses Attribut wird in der [**MF wrapmediatype**](/windows/desktop/api/mfapi/nf-mfapi-mfwrapmediatype) -Funktion verwendet, die einen Medientyp in einem anderen Medientyp umschließt.</span><span class="sxs-lookup"><span data-stu-id="a2a83-108">This attribute is used in the [**MFWrapMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfwrapmediatype) function, which wraps a media type inside another media type.</span></span>

<span data-ttu-id="a2a83-109">Die Funktion [**MF wrapmediatype**](/windows/desktop/api/mfapi/nf-mfapi-mfwrapmediatype) führt folgende Aktionen aus:</span><span class="sxs-lookup"><span data-stu-id="a2a83-109">The [**MFWrapMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfwrapmediatype) function does the following:</span></span>

1.  <span data-ttu-id="a2a83-110">Konvertiert den ursprünglichen Medientyp in ein binäres Array.</span><span class="sxs-lookup"><span data-stu-id="a2a83-110">Converts the original media type into a binary array.</span></span>
2.  <span data-ttu-id="a2a83-111">Legt das vom MF-Attribut **\_ \_ umschließte \_ Type** -Attribut für den neuen Medientyp fest.</span><span class="sxs-lookup"><span data-stu-id="a2a83-111">Sets the **MF\_MT\_WRAPPED\_TYPE** attribute on the new media type.</span></span> <span data-ttu-id="a2a83-112">Der Wert des-Attributs ist das binäre Array.</span><span class="sxs-lookup"><span data-stu-id="a2a83-112">The value of the attribute is the binary array.</span></span>

<span data-ttu-id="a2a83-113">Anwendungen verwenden dieses Attribut in der Regel nicht direkt.</span><span class="sxs-lookup"><span data-stu-id="a2a83-113">Applications typically do not use this attribute directly.</span></span> <span data-ttu-id="a2a83-114">Um den ursprünglichen Medientyp zu entpacken, nennen Sie [**mfunwrapmediatype**](/windows/desktop/api/mfapi/nf-mfapi-mfunwrapmediatype).</span><span class="sxs-lookup"><span data-stu-id="a2a83-114">To unwrap the original media type, call [**MFUnwrapMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfunwrapmediatype).</span></span>

<span data-ttu-id="a2a83-115">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="a2a83-115">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2a83-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a2a83-116">Requirements</span></span>



| <span data-ttu-id="a2a83-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a2a83-117">Requirement</span></span> | <span data-ttu-id="a2a83-118">Wert</span><span class="sxs-lookup"><span data-stu-id="a2a83-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a2a83-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a2a83-119">Minimum supported client</span></span><br/> | <span data-ttu-id="a2a83-120">Windows Vista \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="a2a83-120">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="a2a83-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a2a83-121">Minimum supported server</span></span><br/> | <span data-ttu-id="a2a83-122">Windows Server 2008 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="a2a83-122">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="a2a83-123">Header</span><span class="sxs-lookup"><span data-stu-id="a2a83-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="a2a83-124"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="a2a83-124"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2a83-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a2a83-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2a83-126">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="a2a83-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="a2a83-127">**Imfattributes:: GetBlob**</span><span class="sxs-lookup"><span data-stu-id="a2a83-127">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="a2a83-128">**Imfattributes:: setBlob**</span><span class="sxs-lookup"><span data-stu-id="a2a83-128">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="a2a83-129">**IMF MediaType**</span><span class="sxs-lookup"><span data-stu-id="a2a83-129">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="a2a83-130">Medientyp Attribute</span><span class="sxs-lookup"><span data-stu-id="a2a83-130">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




