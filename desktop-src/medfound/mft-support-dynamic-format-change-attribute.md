---
description: Gibt an, ob eine Media Foundation Transformation (MFT) dynamische Formatänderungen unterstützt.
ms.assetid: 64d32c78-8bee-4d3c-a770-5a097cb71b13
title: MFT_SUPPORT_DYNAMIC_FORMAT_CHANGE-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8224e9b7f0f05f430afac464e61900c7ce879fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106354621"
---
# <a name="mft_support_dynamic_format_change-attribute"></a><span data-ttu-id="011bc-103">MFT- \_ Unterstützung des \_ dynamischen \_ Format \_ Änderungs Attributs</span><span class="sxs-lookup"><span data-stu-id="011bc-103">MFT\_SUPPORT\_DYNAMIC\_FORMAT\_CHANGE attribute</span></span>

<span data-ttu-id="011bc-104">Gibt an, ob eine Media Foundation Transformation (MFT) dynamische Formatänderungen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="011bc-104">Specifies whether a Media Foundation transform (MFT) supports dynamic format changes.</span></span>

## <a name="data-type"></a><span data-ttu-id="011bc-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="011bc-105">Data type</span></span>

<span data-ttu-id="011bc-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="011bc-106">**UINT32**</span></span>

<span data-ttu-id="011bc-107">Als booleschen Wert behandeln.</span><span class="sxs-lookup"><span data-stu-id="011bc-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="011bc-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="011bc-108">Remarks</span></span>

<span data-ttu-id="011bc-109">Dieses Attribut kann die folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="011bc-109">This attribute can have the following values.</span></span>



| <span data-ttu-id="011bc-110">Wert</span><span class="sxs-lookup"><span data-stu-id="011bc-110">Value</span></span>     | <span data-ttu-id="011bc-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="011bc-111">Description</span></span>                                                            |
|-----------|------------------------------------------------------------------------|
| <span data-ttu-id="011bc-112">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="011bc-112">**TRUE**</span></span>  | <span data-ttu-id="011bc-113">Der Client kann beim Streaming das Eingabeformat ändern.</span><span class="sxs-lookup"><span data-stu-id="011bc-113">The client can change the input format during streaming.</span></span>               |
| <span data-ttu-id="011bc-114">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="011bc-114">**FALSE**</span></span> | <span data-ttu-id="011bc-115">Der MFT muss entladen werden, bevor der Client das Eingabeformat ändern kann.</span><span class="sxs-lookup"><span data-stu-id="011bc-115">The MFT must be drained before the client can change the input format.</span></span> |



 

<span data-ttu-id="011bc-116">Zum Abrufen dieses Attributs müssen Sie zuerst [**imftransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) aufrufen, um den globalen Attribut Speicher für die MFT zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="011bc-116">To get this attribute, first call [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) to get the global attribute store for the MFT.</span></span> <span data-ttu-id="011bc-117">Anschließend können Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) abrufen, um den Attribut Wert zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="011bc-117">Then call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) to get the attribute value.</span></span>

<span data-ttu-id="011bc-118">Wenn [**GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) fehlschlägt oder das-Attribut nicht vorhanden ist, ist der Standardwert **false**.</span><span class="sxs-lookup"><span data-stu-id="011bc-118">If [**GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) fails or the attribute is not present, the default value if **FALSE**.</span></span>

<span data-ttu-id="011bc-119">[Asynchrone MFTs](asynchronous-mfts.md) müssen den Wert " **true**" zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="011bc-119">[Asynchronous MFTs](asynchronous-mfts.md) must return the value **TRUE**.</span></span>

<span data-ttu-id="011bc-120">Weitere Informationen finden Sie unter [Handling Stream Changes](handling-stream-changes.md).</span><span class="sxs-lookup"><span data-stu-id="011bc-120">For more information, see [Handling Stream Changes](handling-stream-changes.md).</span></span>

<span data-ttu-id="011bc-121">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="011bc-121">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="011bc-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="011bc-122">Requirements</span></span>



| <span data-ttu-id="011bc-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="011bc-123">Requirement</span></span> | <span data-ttu-id="011bc-124">Wert</span><span class="sxs-lookup"><span data-stu-id="011bc-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="011bc-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="011bc-125">Minimum supported client</span></span><br/> | <span data-ttu-id="011bc-126">Windows Vista \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="011bc-126">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="011bc-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="011bc-127">Minimum supported server</span></span><br/> | <span data-ttu-id="011bc-128">Windows Server 2008 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="011bc-128">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="011bc-129">Header</span><span class="sxs-lookup"><span data-stu-id="011bc-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="011bc-130"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="011bc-130"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="011bc-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="011bc-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="011bc-132">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="011bc-132">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="011bc-133">Asynchrone MFTs</span><span class="sxs-lookup"><span data-stu-id="011bc-133">Asynchronous MFTs</span></span>](asynchronous-mfts.md)
</dt> <dt>

[<span data-ttu-id="011bc-134">Transformations Attribute</span><span class="sxs-lookup"><span data-stu-id="011bc-134">Transform Attributes</span></span>](transform-attributes.md)
</dt> <dt>

[<span data-ttu-id="011bc-135">**Imfattributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="011bc-135">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="011bc-136">**Imfattributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="011bc-136">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="011bc-137">**IMF-Transformation**</span><span class="sxs-lookup"><span data-stu-id="011bc-137">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
</dt> </dl>

 

 




