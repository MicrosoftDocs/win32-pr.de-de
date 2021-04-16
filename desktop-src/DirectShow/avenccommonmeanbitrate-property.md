---
description: Gibt die durchschnittliche codierte Bitrate in Bits pro Sekunde an. Diese Eigenschaft gilt nur für die Konstante Bitrate (CBR) und die Variablen Bitrate (VBR)-Codierungs Modi.
ms.assetid: 8519685a-4f5b-44af-ad46-09eba7a198c6
title: Avenccommonmeanbitrate-Eigenschaft (codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4eaec7fc6578e6e69a45616ee6de059bb7a378b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522472"
---
# <a name="avenccommonmeanbitrate-property"></a><span data-ttu-id="cda15-104">Avenccommonmeanbitrate (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="cda15-104">AVEncCommonMeanBitRate property</span></span>

<span data-ttu-id="cda15-105">Gibt die durchschnittliche codierte Bitrate in Bits pro Sekunde an.</span><span class="sxs-lookup"><span data-stu-id="cda15-105">Specifies the average encoded bit rate, in bits per second.</span></span> <span data-ttu-id="cda15-106">Diese Eigenschaft gilt nur für die Konstante Bitrate (CBR) und die Variablen Bitrate (VBR)-Codierungs Modi.</span><span class="sxs-lookup"><span data-stu-id="cda15-106">This property applies only to constant bit rate (CBR) and variable bit rate (VBR) encoding modes.</span></span>

<span data-ttu-id="cda15-107">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="cda15-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="cda15-108">Datentyp</span><span class="sxs-lookup"><span data-stu-id="cda15-108">Data type</span></span>

<span data-ttu-id="cda15-109">**UInt32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="cda15-109">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="cda15-110">Eigenschaften-GUID</span><span class="sxs-lookup"><span data-stu-id="cda15-110">Property GUID</span></span>

<span data-ttu-id="cda15-111">**Codecapi \_ avenccommonmeanbitrate**</span><span class="sxs-lookup"><span data-stu-id="cda15-111">**CODECAPI\_AVEncCommonMeanBitRate**</span></span>

## <a name="property-value"></a><span data-ttu-id="cda15-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="cda15-112">Property value</span></span>

<span data-ttu-id="cda15-113">Encoder können diese Eigenschaft als enumerationsset oder als linearen Bereich implementieren.</span><span class="sxs-lookup"><span data-stu-id="cda15-113">Encoders can implement this property as an enumerated set or as a linear range.</span></span>

## <a name="remarks"></a><span data-ttu-id="cda15-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cda15-114">Remarks</span></span>

<span data-ttu-id="cda15-115">Diese Eigenschaft wird auch mit [H. 264 UVC 1,5-Kamera Codierern](/windows/desktop/medfound/camera-encoder-h264-uvc-1-5)verwendet.</span><span class="sxs-lookup"><span data-stu-id="cda15-115">This property is also used with [H.264 UVC 1.5 camera encoders](/windows/desktop/medfound/camera-encoder-h264-uvc-1-5).</span></span>

## <a name="requirements"></a><span data-ttu-id="cda15-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cda15-116">Requirements</span></span>



| <span data-ttu-id="cda15-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cda15-117">Requirement</span></span> | <span data-ttu-id="cda15-118">Wert</span><span class="sxs-lookup"><span data-stu-id="cda15-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cda15-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cda15-119">Minimum supported client</span></span><br/> | <span data-ttu-id="cda15-120">Windows 2000 Professional \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="cda15-120">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="cda15-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cda15-121">Minimum supported server</span></span><br/> | <span data-ttu-id="cda15-122">Windows 2000 Server \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="cda15-122">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="cda15-123">Header</span><span class="sxs-lookup"><span data-stu-id="cda15-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="cda15-124"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="cda15-124"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cda15-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cda15-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cda15-126">Eigenschaften der Codec-API</span><span class="sxs-lookup"><span data-stu-id="cda15-126">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="cda15-127">**Icodecapi-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="cda15-127">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

