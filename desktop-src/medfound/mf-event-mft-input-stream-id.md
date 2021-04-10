---
description: Gibt einen Eingabestream für eine Media Foundation Transformation (MFT) an.
ms.assetid: 2922af62-3fcc-4153-a26a-aba3c4121a0b
title: MF_EVENT_MFT_INPUT_STREAM_ID-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59d3966c33dc563fc9e38ad367cc675ba6616c03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214772"
---
# <a name="mf_event_mft_input_stream_id-attribute"></a><span data-ttu-id="9d72a-103">ID-Attribut des MF- \_ \_ MFT- \_ Eingabedaten \_ Stroms \_</span><span class="sxs-lookup"><span data-stu-id="9d72a-103">MF\_EVENT\_MFT\_INPUT\_STREAM\_ID attribute</span></span>

<span data-ttu-id="9d72a-104">Gibt einen Eingabestream für eine Media Foundation Transformation (MFT) an.</span><span class="sxs-lookup"><span data-stu-id="9d72a-104">Specifies an input stream on a Media Foundation transform (MFT).</span></span>

## <a name="data-type"></a><span data-ttu-id="9d72a-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="9d72a-105">Data type</span></span>

<span data-ttu-id="9d72a-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="9d72a-106">**UINT32**</span></span>

<span data-ttu-id="9d72a-107">Der Wert ist ein Eingabedaten Strom Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="9d72a-107">The value is an input stream identifier.</span></span>

## <a name="getset"></a><span data-ttu-id="9d72a-108">Abrufen/Festlegen</span><span class="sxs-lookup"><span data-stu-id="9d72a-108">Get/set</span></span>

<span data-ttu-id="9d72a-109">Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="9d72a-109">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="9d72a-110">Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="9d72a-110">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="9d72a-111">Gilt für:</span><span class="sxs-lookup"><span data-stu-id="9d72a-111">Applies to</span></span>

[<span data-ttu-id="9d72a-112">**IMF Media Event**</span><span class="sxs-lookup"><span data-stu-id="9d72a-112">**IMFMediaEvent**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent)

## <a name="remarks"></a><span data-ttu-id="9d72a-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9d72a-113">Remarks</span></span>

<span data-ttu-id="9d72a-114">Dieses Attribut wird mit den folgenden Ereignissen verwendet:</span><span class="sxs-lookup"><span data-stu-id="9d72a-114">This attribute is used with the following events:</span></span>

-   [<span data-ttu-id="9d72a-115">Metransformdraunvollständig</span><span class="sxs-lookup"><span data-stu-id="9d72a-115">METransformDrainComplete</span></span>](metransformdraincomplete.md)
-   [<span data-ttu-id="9d72a-116">Metransformneedinput</span><span class="sxs-lookup"><span data-stu-id="9d72a-116">METransformNeedInput</span></span>](metransformneedinput.md)

<span data-ttu-id="9d72a-117">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="9d72a-117">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="9d72a-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9d72a-118">Requirements</span></span>



| <span data-ttu-id="9d72a-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9d72a-119">Requirement</span></span> | <span data-ttu-id="9d72a-120">Wert</span><span class="sxs-lookup"><span data-stu-id="9d72a-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9d72a-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9d72a-121">Minimum supported client</span></span><br/> | <span data-ttu-id="9d72a-122">Windows 7 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="9d72a-122">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="9d72a-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9d72a-123">Minimum supported server</span></span><br/> | <span data-ttu-id="9d72a-124">Windows Server 2008 R2 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="9d72a-124">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="9d72a-125">Header</span><span class="sxs-lookup"><span data-stu-id="9d72a-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="9d72a-126"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="9d72a-126"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9d72a-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9d72a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d72a-128">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="9d72a-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="9d72a-129">Asynchrone MFTs</span><span class="sxs-lookup"><span data-stu-id="9d72a-129">Asynchronous MFTs</span></span>](asynchronous-mfts.md)
</dt> <dt>

[<span data-ttu-id="9d72a-130">Ereignisattribute</span><span class="sxs-lookup"><span data-stu-id="9d72a-130">Event Attributes</span></span>](event-attributes.md)
</dt> </dl>

 

 




