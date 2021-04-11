---
description: Gibt den Raten Steuerungs Modus an.
ms.assetid: 4a0d49b1-30da-4ebe-abff-3fceef6dd94a
title: Avenccommonratecontrolmode-Eigenschaft (codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d18d0d7cb68936326fb4c4ba08188e362fdc91d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104213985"
---
# <a name="avenccommonratecontrolmode-property"></a><span data-ttu-id="5d778-103">Avenccommonratecontrolmode (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="5d778-103">AVEncCommonRateControlMode property</span></span>

<span data-ttu-id="5d778-104">Gibt den Raten Steuerungs Modus an.</span><span class="sxs-lookup"><span data-stu-id="5d778-104">Specifies the rate control mode.</span></span>

<span data-ttu-id="5d778-105">Anwendungen können diese Eigenschaft festlegen, um den Raten Steuerungs Modus anzugeben.</span><span class="sxs-lookup"><span data-stu-id="5d778-105">Applications can set this property to specify the rate control mode.</span></span> <span data-ttu-id="5d778-106">Encoder können diese Eigenschaft auch als Funktion zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="5d778-106">Encoders can also return this property as a capability.</span></span>

<span data-ttu-id="5d778-107">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="5d778-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="5d778-108">Datentyp</span><span class="sxs-lookup"><span data-stu-id="5d778-108">Data type</span></span>

<span data-ttu-id="5d778-109">**UInt32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="5d778-109">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="5d778-110">Eigenschaften-GUID</span><span class="sxs-lookup"><span data-stu-id="5d778-110">Property GUID</span></span>

<span data-ttu-id="5d778-111">**Codecapi \_ avenccommonratecontrolmode**</span><span class="sxs-lookup"><span data-stu-id="5d778-111">**CODECAPI\_AVEncCommonRateControlMode**</span></span>

## <a name="property-value"></a><span data-ttu-id="5d778-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="5d778-112">Property value</span></span>

<span data-ttu-id="5d778-113">Der Wert dieser Eigenschaft ist ein Member der [**eavenccommonratecontrolmode**](/windows/win32/api/codecapi/ne-codecapi-eavenccommonratecontrolmode) -Enumeration.</span><span class="sxs-lookup"><span data-stu-id="5d778-113">The value of this property is a member of the [**eAVEncCommonRateControlMode**](/windows/win32/api/codecapi/ne-codecapi-eavenccommonratecontrolmode) enumeration.</span></span>

## <a name="remarks"></a><span data-ttu-id="5d778-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5d778-114">Remarks</span></span>

<span data-ttu-id="5d778-115">Diese Eigenschaft wird auch mit [H. 264 UVC 1,5-Kamera Codierern](/windows/desktop/medfound/camera-encoder-h264-uvc-1-5)verwendet.</span><span class="sxs-lookup"><span data-stu-id="5d778-115">This property is also used with [H.264 UVC 1.5 camera encoders](/windows/desktop/medfound/camera-encoder-h264-uvc-1-5).</span></span>

<span data-ttu-id="5d778-116">[Codecapi \_ Avencvideotemporallayercount](/windows/desktop/medfound/codecapi-avencvideotemporallayercount), [codecapi \_ avencvideousage](/windows/desktop/medfound/codecapi-avencvideousage)und codecapi \_ avenccommonratecontrolmode sind statische Codierungs Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="5d778-116">[CODECAPI\_AVEncVideoTemporalLayerCount](/windows/desktop/medfound/codecapi-avencvideotemporallayercount), [CODECAPI\_AVEncVideoUsage](/windows/desktop/medfound/codecapi-avencvideousage), and CODECAPI\_AVEncCommonRateControlMode are static encoder properties.</span></span> <span data-ttu-id="5d778-117">Nachdem Sie festgelegt wurden, werden diese nur wirksam, nachdem ein Set Media Type auf der Ausgabe-PIN der Kamera aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="5d778-117">Once set, these will only take effect after a set media type is called on the camera’s output pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d778-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5d778-118">Requirements</span></span>



| <span data-ttu-id="5d778-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5d778-119">Requirement</span></span> | <span data-ttu-id="5d778-120">Wert</span><span class="sxs-lookup"><span data-stu-id="5d778-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5d778-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5d778-121">Minimum supported client</span></span><br/> | <span data-ttu-id="5d778-122">Windows 2000 Professional \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="5d778-122">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="5d778-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5d778-123">Minimum supported server</span></span><br/> | <span data-ttu-id="5d778-124">Windows 2000 Server \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="5d778-124">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="5d778-125">Header</span><span class="sxs-lookup"><span data-stu-id="5d778-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="5d778-126"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="5d778-126"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d778-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5d778-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d778-128">Eigenschaften der Codec-API</span><span class="sxs-lookup"><span data-stu-id="5d778-128">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="5d778-129">**Icodecapi-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="5d778-129">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

