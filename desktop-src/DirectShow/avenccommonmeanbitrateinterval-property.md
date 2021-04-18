---
description: Gibt das Zeitintervall an, für das die durchschnittliche Bitrate gilt. Diese Eigenschaft wird in Verbindung mit der Eigenschaft "avenccommonmeanbitrate" verwendet.
ms.assetid: 3cf26f46-e8ac-448a-a031-800915cad1ef
title: Avenccommonmeanbitrateingeterval-Eigenschaft (codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ffee31b0ac54d195051f1cc973d2fdcb058f202
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482523"
---
# <a name="avenccommonmeanbitrateinterval-property"></a><span data-ttu-id="5ef72-104">Avenccommonmeanbitrateingeterval (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="5ef72-104">AVEncCommonMeanBitRateInterval property</span></span>

<span data-ttu-id="5ef72-105">Gibt das Zeitintervall an, für das die durchschnittliche Bitrate gilt.</span><span class="sxs-lookup"><span data-stu-id="5ef72-105">Specifies the time interval over which the average bit rate applies.</span></span> <span data-ttu-id="5ef72-106">Diese Eigenschaft wird in Verbindung mit der Eigenschaft " [**avenccommonmeanbitrate**](avenccommonmeanbitrate-property.md) " verwendet.</span><span class="sxs-lookup"><span data-stu-id="5ef72-106">This property is used in conjunction with the [**AVEncCommonMeanBitRate**](avenccommonmeanbitrate-property.md) property.</span></span>

<span data-ttu-id="5ef72-107">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="5ef72-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="5ef72-108">Datentyp</span><span class="sxs-lookup"><span data-stu-id="5ef72-108">Data type</span></span>

<span data-ttu-id="5ef72-109">**UINT64** (**VT \_ UI8**)</span><span class="sxs-lookup"><span data-stu-id="5ef72-109">**UINT64** (**VT\_UI8**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="5ef72-110">Eigenschaften-GUID</span><span class="sxs-lookup"><span data-stu-id="5ef72-110">Property GUID</span></span>

<span data-ttu-id="5ef72-111">**Codecapi \_ avenccommonmeanbitrateingeterval**</span><span class="sxs-lookup"><span data-stu-id="5ef72-111">**CODECAPI\_AVEncCommonMeanBitRateInterval**</span></span>

## <a name="property-value"></a><span data-ttu-id="5ef72-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="5ef72-112">Property value</span></span>

<span data-ttu-id="5ef72-113">Diese Eigenschaft verfügt über einen linearen Wertebereich.</span><span class="sxs-lookup"><span data-stu-id="5ef72-113">This property has a linear range of values.</span></span> <span data-ttu-id="5ef72-114">Um den unterstützten Bereich abzurufen, nennen Sie [**icodecapi:: getparameterrange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span><span class="sxs-lookup"><span data-stu-id="5ef72-114">To get the supported range, call [**ICodecAPI::GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span></span>

## <a name="remarks"></a><span data-ttu-id="5ef72-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5ef72-115">Remarks</span></span>

<span data-ttu-id="5ef72-116">Bei der bidirektionalen VBR-Codierung (Two-Pass Variable Bitrate) gibt der Wert 0 (null) an, dass das Zeitintervall die gesamte Dauer des Inhalts ist.</span><span class="sxs-lookup"><span data-stu-id="5ef72-116">For two-pass variable bit rate (VBR) encoding, the value zero indicates that the time interval is the entire duration of the content.</span></span> <span data-ttu-id="5ef72-117">Bei einer CBR-Codierung (Single-Pass Constant Bit Rate) gibt der Wert 0 (null) an, dass der Encoder das Intervall (in der Regel 0,5 Sekunden) auswählt.</span><span class="sxs-lookup"><span data-stu-id="5ef72-117">For single-pass constant bit rate (CBR) encoding, the value zero indicates that the encoder selects the interval (typically 0.5 seconds).</span></span>

## <a name="requirements"></a><span data-ttu-id="5ef72-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5ef72-118">Requirements</span></span>



| <span data-ttu-id="5ef72-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5ef72-119">Requirement</span></span> | <span data-ttu-id="5ef72-120">Wert</span><span class="sxs-lookup"><span data-stu-id="5ef72-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5ef72-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5ef72-121">Minimum supported client</span></span><br/> | <span data-ttu-id="5ef72-122">Windows 2000 Professional \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="5ef72-122">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="5ef72-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5ef72-123">Minimum supported server</span></span><br/> | <span data-ttu-id="5ef72-124">Windows 2000 Server \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="5ef72-124">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="5ef72-125">Header</span><span class="sxs-lookup"><span data-stu-id="5ef72-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="5ef72-126"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="5ef72-126"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ef72-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5ef72-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ef72-128">Eigenschaften der Codec-API</span><span class="sxs-lookup"><span data-stu-id="5ef72-128">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="5ef72-129">**Icodecapi-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="5ef72-129">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




