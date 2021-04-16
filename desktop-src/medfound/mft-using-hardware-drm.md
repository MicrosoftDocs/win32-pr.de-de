---
description: Gibt an, ob IMF Transform Hardware DRM verwendet.
title: MFT_USING_HARDWARE_DRM (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e6dbacedbf5fd9298e4da5154bd82fcc9f39bde
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485347"
---
# <a name="mft_using_hardware_drm-attribute"></a><span data-ttu-id="605a4-103">MFT \_ mithilfe des \_ Hardware-DRM- \_ Attributs</span><span class="sxs-lookup"><span data-stu-id="605a4-103">MFT\_USING\_HARDWARE\_DRM attribute</span></span>

<span data-ttu-id="605a4-104">Gibt an, ob IMF Transform Hardware DRM verwendet.</span><span class="sxs-lookup"><span data-stu-id="605a4-104">Specifies whether the IMFTransform is using hardware DRM.</span></span>

## <a name="data-type"></a><span data-ttu-id="605a4-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="605a4-105">Data type</span></span>

<span data-ttu-id="605a4-106">**UInt32** (als **bool** behandelt)</span><span class="sxs-lookup"><span data-stu-id="605a4-106">**UINT32** (treated as **BOOL**)</span></span>

## <a name="getset"></a><span data-ttu-id="605a4-107">Abrufen/Festlegen</span><span class="sxs-lookup"><span data-stu-id="605a4-107">Get/set</span></span>

<span data-ttu-id="605a4-108">Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT32**](/windows/win32/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="605a4-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/win32/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="605a4-109">Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT32**](/windows/win32/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="605a4-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/win32/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="605a4-110">Gilt für:</span><span class="sxs-lookup"><span data-stu-id="605a4-110">Applies to</span></span>

[<span data-ttu-id="605a4-111">**Imtransfrom**</span><span class="sxs-lookup"><span data-stu-id="605a4-111">**IMTransfrom**</span></span>](/windows/win32/api/mftransform/nn-mftransform-imftransform)

## <a name="remarks"></a><span data-ttu-id="605a4-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="605a4-112">Remarks</span></span>

<span data-ttu-id="605a4-113">Wenn eine MFT-Entschlüsselung angibt, dass dieses Attribut auf 1 festgelegt ist, wird Hardware-DRM verwendet.</span><span class="sxs-lookup"><span data-stu-id="605a4-113">If an MFT decrypter specifies this attribute set to 1, then it is using hardware DRM.</span></span> <span data-ttu-id="605a4-114">Wenn eine MFT-Entschlüsselung angibt, dass dieses Attribut auf 0 festgelegt ist, wird das Hardware-DRM nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="605a4-114">If an MFT decrypter specifies this attribute set to 0, then it is not using hardware DRM.</span></span> <span data-ttu-id="605a4-115">Wenn eine MFT-Entschlüsselung dieses Attribut nicht angibt oder es mit einem anderen Wert angibt, kann Sie nicht angeben, ob Sie Hardware-DRM verwendet.</span><span class="sxs-lookup"><span data-stu-id="605a4-115">If an MFT decrypter does not specify this attribute or specifies it with a different value, then it does not (or is unable to) indicate whether it is using hardware DRM.</span></span>


<span data-ttu-id="605a4-116">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="605a4-116">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="605a4-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="605a4-117">Requirements</span></span>



| <span data-ttu-id="605a4-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="605a4-118">Requirement</span></span> | <span data-ttu-id="605a4-119">Wert</span><span class="sxs-lookup"><span data-stu-id="605a4-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="605a4-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="605a4-120">Minimum supported client</span></span><br/> | <span data-ttu-id="605a4-121">Windows 10 April 2020-Update</span><span class="sxs-lookup"><span data-stu-id="605a4-121">Windows 10 April 2020 Update</span></span>   <br/>                                       |
| <span data-ttu-id="605a4-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="605a4-122">Minimum supported server</span></span><br/> | <span data-ttu-id="605a4-123">Windows Server 2008 R2 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="605a4-123">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="605a4-124">Header</span><span class="sxs-lookup"><span data-stu-id="605a4-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="605a4-125"><dt>"MF Transform. h"</dt></span><span class="sxs-lookup"><span data-stu-id="605a4-125"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="605a4-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="605a4-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="605a4-127">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="605a4-127">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt>  <dt>

[<span data-ttu-id="605a4-128">Transformations Attribute</span><span class="sxs-lookup"><span data-stu-id="605a4-128">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 




