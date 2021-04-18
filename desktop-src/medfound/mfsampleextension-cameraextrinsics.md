---
description: Enthält die Kamera (extrinsics) für das Beispiel.
ms.assetid: C970E958-3866-491A-9806-DB300834360E
title: MFSampleExtension_CameraExtrinsics-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3340f1ab84061fa00e12fa65960f1b2902690816
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368178"
---
# <a name="mfsampleextension_cameraextrinsics-attribute"></a><span data-ttu-id="7e2cb-103">MF Sample Extension- \_ Attribut "cameraextrinsics"</span><span class="sxs-lookup"><span data-stu-id="7e2cb-103">MFSampleExtension\_CameraExtrinsics attribute</span></span>

<span data-ttu-id="7e2cb-104">Enthält die Kamera (extrinsics) für das Beispiel.</span><span class="sxs-lookup"><span data-stu-id="7e2cb-104">Contains the camera extrinsics for the sample.</span></span>

## <a name="data-type"></a><span data-ttu-id="7e2cb-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="7e2cb-105">Data type</span></span>

<span data-ttu-id="7e2cb-106">Bytearray</span><span class="sxs-lookup"><span data-stu-id="7e2cb-106">Byte array</span></span>

## <a name="getset"></a><span data-ttu-id="7e2cb-107">Abrufen/Festlegen</span><span class="sxs-lookup"><span data-stu-id="7e2cb-107">Get/set</span></span>

<span data-ttu-id="7e2cb-108">Zum Abrufen dieses Attributs müssen Sie [**imfattributes:: GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="7e2cb-108">To get this attribute, call [**IMFAttributes::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).</span></span>

<span data-ttu-id="7e2cb-109">Um dieses Attribut festzulegen, müssen Sie [**imfattributes:: setBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="7e2cb-109">To set this attribute, call [**IMFAttributes::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).</span></span>

## <a name="applies-to"></a><span data-ttu-id="7e2cb-110">Gilt für:</span><span class="sxs-lookup"><span data-stu-id="7e2cb-110">Applies to</span></span>

[<span data-ttu-id="7e2cb-111">**IMF Sample**</span><span class="sxs-lookup"><span data-stu-id="7e2cb-111">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a><span data-ttu-id="7e2cb-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7e2cb-112">Remarks</span></span>

<span data-ttu-id="7e2cb-113">Der Wert des Attributs ist [**MF cameraextrinsics**](/windows/desktop/api/mfapi/ns-mfapi-mfcameraextrinsics).</span><span class="sxs-lookup"><span data-stu-id="7e2cb-113">The value of the attribute is a [**MFCameraExtrinsics**](/windows/desktop/api/mfapi/ns-mfapi-mfcameraextrinsics).</span></span>

<span data-ttu-id="7e2cb-114">Dieses Attribut ist optional, um Kameras zu unterstützen, die nicht kalibriert sind.</span><span class="sxs-lookup"><span data-stu-id="7e2cb-114">This attribute is optional to support cameras that are not calibrated.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e2cb-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7e2cb-115">Requirements</span></span>



| <span data-ttu-id="7e2cb-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7e2cb-116">Requirement</span></span> | <span data-ttu-id="7e2cb-117">Wert</span><span class="sxs-lookup"><span data-stu-id="7e2cb-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7e2cb-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7e2cb-118">Minimum supported client</span></span><br/> | <span data-ttu-id="7e2cb-119">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7e2cb-119">Windows 10 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7e2cb-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7e2cb-120">Minimum supported server</span></span><br/> | <span data-ttu-id="7e2cb-121">Nur Windows Server 2012 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7e2cb-121">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="7e2cb-122">Header</span><span class="sxs-lookup"><span data-stu-id="7e2cb-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="7e2cb-123"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="7e2cb-123"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7e2cb-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7e2cb-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e2cb-125">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="7e2cb-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




