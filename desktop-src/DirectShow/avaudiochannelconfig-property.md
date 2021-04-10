---
description: Ruft die sprecherkonfigurationskonfiguration für die Audiokanäle im audiobit-Stream ab.
ms.assetid: ec13bb55-47af-4d79-9560-d297bce8e236
title: Avaudiochannelconfig-Eigenschaft (codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52ee1bc7897d92f7efa1b6d351d2f73c32867529
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104041188"
---
# <a name="avaudiochannelconfig-property"></a><span data-ttu-id="d4233-103">Avaudiochannelconfig (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="d4233-103">AVAudioChannelConfig property</span></span>

<span data-ttu-id="d4233-104">Ruft die sprecherkonfigurationskonfiguration für die Audiokanäle im audiobit-Stream ab.</span><span class="sxs-lookup"><span data-stu-id="d4233-104">Gets the speaker configuration for the audio channels in the audio bit stream.</span></span>

<span data-ttu-id="d4233-105">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="d4233-105">This property is read-only.</span></span>

## <a name="data-type"></a><span data-ttu-id="d4233-106">Datentyp</span><span class="sxs-lookup"><span data-stu-id="d4233-106">Data type</span></span>

<span data-ttu-id="d4233-107">**UInt32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="d4233-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="d4233-108">Eigenschaften-GUID</span><span class="sxs-lookup"><span data-stu-id="d4233-108">Property GUID</span></span>

<span data-ttu-id="d4233-109">**Codecapi \_ avaudiochannelconfig**</span><span class="sxs-lookup"><span data-stu-id="d4233-109">**CODECAPI\_AVAudioChannelConfig**</span></span>

## <a name="property-value"></a><span data-ttu-id="d4233-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="d4233-110">Property value</span></span>

<span data-ttu-id="d4233-111">Der Wert dieser Eigenschaft ist ein bitweises OR von Membern der [**eavaudiochannelconfig**](/windows/desktop/api/codecapi/ne-codecapi-eavaudiochannelconfig) -Enumeration.</span><span class="sxs-lookup"><span data-stu-id="d4233-111">The value of this property is a bitwise OR of members of the [**eAVAudioChannelConfig**](/windows/desktop/api/codecapi/ne-codecapi-eavaudiochannelconfig) enumeration.</span></span>

## <a name="remarks"></a><span data-ttu-id="d4233-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d4233-112">Remarks</span></span>

<span data-ttu-id="d4233-113">Die Anzahl der Kanäle umfasst den LFE-Kanal (Low Frequency Effect), falls vorhanden.</span><span class="sxs-lookup"><span data-stu-id="d4233-113">The number of channels includes the low frequency effect (LFE) channel, if present.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4233-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d4233-114">Requirements</span></span>



| <span data-ttu-id="d4233-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d4233-115">Requirement</span></span> | <span data-ttu-id="d4233-116">Wert</span><span class="sxs-lookup"><span data-stu-id="d4233-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d4233-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d4233-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d4233-118">Windows 2000 Professional \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="d4233-118">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="d4233-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d4233-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d4233-120">Windows 2000 Server \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="d4233-120">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="d4233-121">Header</span><span class="sxs-lookup"><span data-stu-id="d4233-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="d4233-122"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="d4233-122"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4233-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d4233-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4233-124">Eigenschaften der Codec-API</span><span class="sxs-lookup"><span data-stu-id="d4233-124">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="d4233-125">**Icodecapi-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="d4233-125">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




