---
description: Enthält die intrinsie-Kamera-Funktionen für das Beispiel.
ms.assetid: AF7EA6A0-90C5-49A8-AD68-776BF770A448
title: MFSampleExtension_PinholeCameraIntrinsics-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bb9e78641c0baab0e9eda3083aafaf8fe92229f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106351613"
---
# <a name="mfsampleextension_pinholecameraintrinsics-attribute"></a><span data-ttu-id="125c8-103">MF Sample Extension \_ pinholecameraintrinsics-Attribut</span><span class="sxs-lookup"><span data-stu-id="125c8-103">MFSampleExtension\_PinholeCameraIntrinsics attribute</span></span>

<span data-ttu-id="125c8-104">Enthält die intrinsie-Kamera-Funktionen für das Beispiel.</span><span class="sxs-lookup"><span data-stu-id="125c8-104">Contains the pinhole camera intrinsics for the sample.</span></span>

## <a name="data-type"></a><span data-ttu-id="125c8-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="125c8-105">Data type</span></span>

<span data-ttu-id="125c8-106">Bytearray</span><span class="sxs-lookup"><span data-stu-id="125c8-106">Byte array</span></span>

## <a name="getset"></a><span data-ttu-id="125c8-107">Abrufen/Festlegen</span><span class="sxs-lookup"><span data-stu-id="125c8-107">Get/set</span></span>

<span data-ttu-id="125c8-108">Zum Abrufen dieses Attributs müssen Sie [**imfattributes:: GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="125c8-108">To get this attribute, call [**IMFAttributes::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).</span></span>

<span data-ttu-id="125c8-109">Um dieses Attribut festzulegen, müssen Sie [**imfattributes:: setBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="125c8-109">To set this attribute, call [**IMFAttributes::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).</span></span>

## <a name="applies-to"></a><span data-ttu-id="125c8-110">Gilt für:</span><span class="sxs-lookup"><span data-stu-id="125c8-110">Applies to</span></span>

[<span data-ttu-id="125c8-111">**IMF Sample**</span><span class="sxs-lookup"><span data-stu-id="125c8-111">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a><span data-ttu-id="125c8-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="125c8-112">Remarks</span></span>

<span data-ttu-id="125c8-113">Der Wert des Attributs ist " [**MF**](/windows/desktop/api/mfapi/ns-mfapi-mfpinholecameraintrinsics)".</span><span class="sxs-lookup"><span data-stu-id="125c8-113">The value of the attribute is a [**MFPinholeCameraIntrinsics**](/windows/desktop/api/mfapi/ns-mfapi-mfpinholecameraintrinsics).</span></span>

<span data-ttu-id="125c8-114">Dieses Attribut ist optional, um Kameras zu unterstützen, die nicht kalibriert sind.</span><span class="sxs-lookup"><span data-stu-id="125c8-114">This attribute is optional to support cameras that are not calibrated.</span></span>

## <a name="requirements"></a><span data-ttu-id="125c8-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="125c8-115">Requirements</span></span>



| <span data-ttu-id="125c8-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="125c8-116">Requirement</span></span> | <span data-ttu-id="125c8-117">Wert</span><span class="sxs-lookup"><span data-stu-id="125c8-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="125c8-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="125c8-118">Minimum supported client</span></span><br/> | <span data-ttu-id="125c8-119">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="125c8-119">Windows 10 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="125c8-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="125c8-120">Minimum supported server</span></span><br/> | <span data-ttu-id="125c8-121">Nur Windows Server 2012 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="125c8-121">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="125c8-122">Header</span><span class="sxs-lookup"><span data-stu-id="125c8-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="125c8-123"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="125c8-123"><dt>Mfapi.h</dt></span></span> </dl> |



 

 




