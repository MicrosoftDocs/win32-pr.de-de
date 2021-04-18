---
description: Gibt die minimale Bitrate in Bits pro Sekunde an. Diese Eigenschaft gilt nur für die Konstante Bitrate (CBR) und die Variablen Bitrate (VBR)-Codierungs Modi.
ms.assetid: 57ef6c08-3bad-4d8d-8daf-61041b878802
title: Avenccommonminbitrate-Eigenschaft (codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95c9b6e84675994d2aca7548f6c13d6558ebc020
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106343948"
---
# <a name="avenccommonminbitrate-property"></a><span data-ttu-id="0cfa9-104">Avenccommonminbitrate (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="0cfa9-104">AVEncCommonMinBitRate property</span></span>

<span data-ttu-id="0cfa9-105">Gibt die minimale Bitrate in Bits pro Sekunde an.</span><span class="sxs-lookup"><span data-stu-id="0cfa9-105">Specifies the minimum bit rate, in bits per second.</span></span> <span data-ttu-id="0cfa9-106">Diese Eigenschaft gilt nur für die Konstante Bitrate (CBR) und die Variablen Bitrate (VBR)-Codierungs Modi.</span><span class="sxs-lookup"><span data-stu-id="0cfa9-106">This property applies only to constant bit rate (CBR) and variable bit rate (VBR) encoding modes.</span></span>

<span data-ttu-id="0cfa9-107">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="0cfa9-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="0cfa9-108">Datentyp</span><span class="sxs-lookup"><span data-stu-id="0cfa9-108">Data type</span></span>

<span data-ttu-id="0cfa9-109">**UInt32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="0cfa9-109">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="0cfa9-110">Eigenschaften-GUID</span><span class="sxs-lookup"><span data-stu-id="0cfa9-110">Property GUID</span></span>

<span data-ttu-id="0cfa9-111">**Codecapi \_ avenccommonminbitrate**</span><span class="sxs-lookup"><span data-stu-id="0cfa9-111">**CODECAPI\_AVEncCommonMinBitRate**</span></span>

## <a name="property-value"></a><span data-ttu-id="0cfa9-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="0cfa9-112">Property value</span></span>

<span data-ttu-id="0cfa9-113">Diese Eigenschaft verfügt über einen linearen Wertebereich.</span><span class="sxs-lookup"><span data-stu-id="0cfa9-113">This property has a linear range of values.</span></span> <span data-ttu-id="0cfa9-114">Um den unterstützten Bereich abzurufen, nennen Sie [**icodecapi:: getparameterrange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span><span class="sxs-lookup"><span data-stu-id="0cfa9-114">To get the supported range, call [**ICodecAPI::GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span></span>

## <a name="remarks"></a><span data-ttu-id="0cfa9-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0cfa9-115">Remarks</span></span>

<span data-ttu-id="0cfa9-116">Der Encoder erzwingt die minimale Bitrate durch Erhöhen der Codierungsqualität nach Bedarf.</span><span class="sxs-lookup"><span data-stu-id="0cfa9-116">The encoder enforces the minimum bit rate by increasing the encoding quality as necessary.</span></span>

## <a name="requirements"></a><span data-ttu-id="0cfa9-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0cfa9-117">Requirements</span></span>



| <span data-ttu-id="0cfa9-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0cfa9-118">Requirement</span></span> | <span data-ttu-id="0cfa9-119">Wert</span><span class="sxs-lookup"><span data-stu-id="0cfa9-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0cfa9-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0cfa9-120">Minimum supported client</span></span><br/> | <span data-ttu-id="0cfa9-121">Windows 2000 Professional \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="0cfa9-121">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="0cfa9-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0cfa9-122">Minimum supported server</span></span><br/> | <span data-ttu-id="0cfa9-123">Windows 2000 Server \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="0cfa9-123">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="0cfa9-124">Header</span><span class="sxs-lookup"><span data-stu-id="0cfa9-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="0cfa9-125"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="0cfa9-125"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0cfa9-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0cfa9-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0cfa9-127">Eigenschaften der Codec-API</span><span class="sxs-lookup"><span data-stu-id="0cfa9-127">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="0cfa9-128">**Icodecapi-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="0cfa9-128">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




