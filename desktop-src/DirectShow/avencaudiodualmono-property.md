---
description: Gibt an, ob die zwei-Kanal-Audiodaten als Stereo oder Dual Mono codiert werden.
ms.assetid: 37f25590-69c2-43bd-a5d4-2262457cb39d
title: Avencaudiodualmono-Eigenschaft (codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0a5b684638133a1449fc849348cdfd8627533fe
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106341111"
---
# <a name="avencaudiodualmono-property"></a><span data-ttu-id="49f1e-103">Avencaudiodualmono (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="49f1e-103">AVEncAudioDualMono property</span></span>

<span data-ttu-id="49f1e-104">Gibt an, ob die zwei-Kanal-Audiodaten als Stereo oder Dual Mono codiert werden.</span><span class="sxs-lookup"><span data-stu-id="49f1e-104">Specifies whether 2-channel audio is encoded as stereo or dual mono.</span></span>

<span data-ttu-id="49f1e-105">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="49f1e-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="49f1e-106">Datentyp</span><span class="sxs-lookup"><span data-stu-id="49f1e-106">Data type</span></span>

<span data-ttu-id="49f1e-107">**UInt32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="49f1e-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="49f1e-108">Eigenschaften-GUID</span><span class="sxs-lookup"><span data-stu-id="49f1e-108">Property GUID</span></span>

<span data-ttu-id="49f1e-109">**Codecapi \_ avencaudiodualmono**</span><span class="sxs-lookup"><span data-stu-id="49f1e-109">**CODECAPI\_AVEncAudioDualMono**</span></span>

## <a name="property-value"></a><span data-ttu-id="49f1e-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="49f1e-110">Property value</span></span>

<span data-ttu-id="49f1e-111">Der Wert dieser Eigenschaft ist ein Member der [**eavencaudiodualmono**](/windows/win32/api/codecapi/ne-codecapi-eavencaudiodualmono) -Enumeration.</span><span class="sxs-lookup"><span data-stu-id="49f1e-111">The value of this property is a member of the [**eAVEncAudioDualMono**](/windows/win32/api/codecapi/ne-codecapi-eavencaudiodualmono) enumeration.</span></span>

## <a name="remarks"></a><span data-ttu-id="49f1e-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="49f1e-112">Remarks</span></span>

<span data-ttu-id="49f1e-113">Diese Eigenschaft gilt nicht für MPEG-Audioencoder.</span><span class="sxs-lookup"><span data-stu-id="49f1e-113">This property does not apply to MPEG audio encoders.</span></span> <span data-ttu-id="49f1e-114">Verwenden Sie für MPEG-Audiodaten die Eigenschaft " [**avencmpacodingmode**](avencmpacodingmode-property.md) ".</span><span class="sxs-lookup"><span data-stu-id="49f1e-114">For MPEG audio, use the [**AVEncMPACodingMode**](avencmpacodingmode-property.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="49f1e-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="49f1e-115">Requirements</span></span>



| <span data-ttu-id="49f1e-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="49f1e-116">Requirement</span></span> | <span data-ttu-id="49f1e-117">Wert</span><span class="sxs-lookup"><span data-stu-id="49f1e-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="49f1e-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="49f1e-118">Minimum supported client</span></span><br/> | <span data-ttu-id="49f1e-119">Windows 2000 Professional \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="49f1e-119">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="49f1e-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="49f1e-120">Minimum supported server</span></span><br/> | <span data-ttu-id="49f1e-121">Windows 2000 Server \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="49f1e-121">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="49f1e-122">Header</span><span class="sxs-lookup"><span data-stu-id="49f1e-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="49f1e-123"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="49f1e-123"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49f1e-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="49f1e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49f1e-125">Eigenschaften der Codec-API</span><span class="sxs-lookup"><span data-stu-id="49f1e-125">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="49f1e-126">**Icodecapi-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="49f1e-126">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

