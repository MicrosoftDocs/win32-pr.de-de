---
description: 'AVEncAudioDualMono-Eigenschaft: Gibt an, ob 2-Kanal-Audio als Stereo oder Dual Mono codiert wird.'
ms.assetid: 37f25590-69c2-43bd-a5d4-2262457cb39d
title: AVEncAudioDualMono-Eigenschaft (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b58cbd901079d8f4dede1efae140791ae99c7fed
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096578"
---
# <a name="avencaudiodualmono-property"></a><span data-ttu-id="6bb21-103">AVEncAudioDualMono (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="6bb21-103">AVEncAudioDualMono property</span></span>

<span data-ttu-id="6bb21-104">Gibt an, ob 2-Kanal-Audio als Stereo oder Dual Mono codiert wird.</span><span class="sxs-lookup"><span data-stu-id="6bb21-104">Specifies whether 2-channel audio is encoded as stereo or dual mono.</span></span>

<span data-ttu-id="6bb21-105">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="6bb21-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="6bb21-106">Datentyp</span><span class="sxs-lookup"><span data-stu-id="6bb21-106">Data type</span></span>

<span data-ttu-id="6bb21-107">**UINT32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="6bb21-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="6bb21-108">Eigenschaften-GUID</span><span class="sxs-lookup"><span data-stu-id="6bb21-108">Property GUID</span></span>

<span data-ttu-id="6bb21-109">**CODECAPI \_ AVEncAudioDualMono**</span><span class="sxs-lookup"><span data-stu-id="6bb21-109">**CODECAPI\_AVEncAudioDualMono**</span></span>

## <a name="property-value"></a><span data-ttu-id="6bb21-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="6bb21-110">Property value</span></span>

<span data-ttu-id="6bb21-111">Der Wert dieser Eigenschaft ist ein Member der [**eAVEncAudioDualMono-Enumeration.**](/windows/win32/api/codecapi/ne-codecapi-eavencaudiodualmono)</span><span class="sxs-lookup"><span data-stu-id="6bb21-111">The value of this property is a member of the [**eAVEncAudioDualMono**](/windows/win32/api/codecapi/ne-codecapi-eavencaudiodualmono) enumeration.</span></span>

## <a name="remarks"></a><span data-ttu-id="6bb21-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6bb21-112">Remarks</span></span>

<span data-ttu-id="6bb21-113">Diese Eigenschaft gilt nicht für MPEG-Audioencoder.</span><span class="sxs-lookup"><span data-stu-id="6bb21-113">This property does not apply to MPEG audio encoders.</span></span> <span data-ttu-id="6bb21-114">Verwenden Sie für MPEG-Audio die [**EIGENSCHAFT AVEncMPACodingMode.**](avencmpacodingmode-property.md)</span><span class="sxs-lookup"><span data-stu-id="6bb21-114">For MPEG audio, use the [**AVEncMPACodingMode**](avencmpacodingmode-property.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="6bb21-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6bb21-115">Requirements</span></span>



| <span data-ttu-id="6bb21-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6bb21-116">Requirement</span></span> | <span data-ttu-id="6bb21-117">Wert</span><span class="sxs-lookup"><span data-stu-id="6bb21-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6bb21-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6bb21-118">Minimum supported client</span></span><br/> | <span data-ttu-id="6bb21-119">UWP-Apps für Windows 2000 \[ \| Professional-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6bb21-119">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="6bb21-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6bb21-120">Minimum supported server</span></span><br/> | <span data-ttu-id="6bb21-121">Windows 2000 \[ Server-Desktop-Apps \| UWP-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6bb21-121">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="6bb21-122">Header</span><span class="sxs-lookup"><span data-stu-id="6bb21-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="6bb21-123"><dt>Codecapi.h</dt></span><span class="sxs-lookup"><span data-stu-id="6bb21-123"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6bb21-124">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="6bb21-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6bb21-125">Codec-API-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6bb21-125">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="6bb21-126">**ICodecAPI-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="6bb21-126">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

