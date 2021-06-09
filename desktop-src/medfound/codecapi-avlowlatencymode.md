---
description: Aktiviert den Modus mit geringer Latenz in einem Codec.
ms.assetid: 15E8FF6F-AD8C-436F-B3C0-5062B1F86E32
title: CODECAPI_AVLowLatencyMode (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5be7e23a29e9dd5f88f7a96e6c32fd42b68a7204
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/09/2021
ms.locfileid: "111826904"
---
# <a name="codecapi_avlowlatencymode-property"></a><span data-ttu-id="4d52d-103">\_CODECAPI-Eigenschaft "AVLowLatencyMode"</span><span class="sxs-lookup"><span data-stu-id="4d52d-103">CODECAPI\_AVLowLatencyMode property</span></span>

<span data-ttu-id="4d52d-104">Aktiviert den Modus mit geringer Latenz in einem Codec.</span><span class="sxs-lookup"><span data-stu-id="4d52d-104">Enables low-latency mode in a codec.</span></span>

## <a name="data-type"></a><span data-ttu-id="4d52d-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="4d52d-105">Data type</span></span>

<span data-ttu-id="4d52d-106">**ULONG** (**VT \_ BOOL**)</span><span class="sxs-lookup"><span data-stu-id="4d52d-106">**ULONG** (**VT\_BOOL**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="4d52d-107">Eigenschaften-GUID</span><span class="sxs-lookup"><span data-stu-id="4d52d-107">Property GUID</span></span>

<span data-ttu-id="4d52d-108">**CODECAPI \_ AVLowLatencyMode**</span><span class="sxs-lookup"><span data-stu-id="4d52d-108">**CODECAPI\_AVLowLatencyMode**</span></span>

## <a name="property-value"></a><span data-ttu-id="4d52d-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="4d52d-109">Property value</span></span>

<span data-ttu-id="4d52d-110">Wenn der Wert ungleich 0 (null) ist, wird der Modus mit geringer Latenz aktiviert.</span><span class="sxs-lookup"><span data-stu-id="4d52d-110">If the value is nonzero, low-latency mode is enabled.</span></span> <span data-ttu-id="4d52d-111">Wenn der Wert 0 (null) ist, wird der Modus mit geringer Latenz deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="4d52d-111">If the value is zero, low-latency mode is disabled.</span></span>

## <a name="remarks"></a><span data-ttu-id="4d52d-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="4d52d-112">Remarks</span></span>

<span data-ttu-id="4d52d-113">Diese Eigenschaft gilt sowohl für Encoder als auch für Decoder.</span><span class="sxs-lookup"><span data-stu-id="4d52d-113">This property applies to both encoders and decoders.</span></span>

<span data-ttu-id="4d52d-114">Der Modus mit geringer Latenz ist für die Echtzeitkommunikation oder Liveerfassung nützlich, wenn die Latenz minimiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="4d52d-114">Low-latency mode is useful for real-time communications or live capture, when latency should be minimized.</span></span> <span data-ttu-id="4d52d-115">Der Modus mit geringer Latenz kann jedoch auch die Decodierungs- oder Codierungsqualität verringern.</span><span class="sxs-lookup"><span data-stu-id="4d52d-115">However, low-latency mode might also reduce the decoding or encoding quality.</span></span>

<span data-ttu-id="4d52d-116">Es wird erwartet, dass der Encoder keine Beispielverzögerung aufgrund einer Frame-Neuanordnung im Codierungsprozess hinzufüge, und ein Eingabebeispiel sollte ein Ausgabebeispiel erzeugen.</span><span class="sxs-lookup"><span data-stu-id="4d52d-116">The encoder is expected to not add any sample delay due to frame reordering in encoding process, and one input sample shall produce one output sample.</span></span> <span data-ttu-id="4d52d-117">B-Slices/Frames können vorhanden sein, solange sie keine Frame-Neubestellung im Encoder einführen.</span><span class="sxs-lookup"><span data-stu-id="4d52d-117">B slices/frames can be present as long as they do not introduce any frame re-ordering in the encoder.</span></span>

> [!WARNING] 
> <span data-ttu-id="4d52d-118">In der aktuellen Implementierung verwendet der Media Foundation H.264-Decoder den VT_UI4 **für** diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="4d52d-118">In the current implementation, the Media Foundation H.264 decoder uses the type **VT_UI4** for this property.</span></span> <span data-ttu-id="4d52d-119">Alle anderen Implementierungen, einschließlich des H.264-Encoders, verwenden den Typ **VT_BOOL.**</span><span class="sxs-lookup"><span data-stu-id="4d52d-119">All other implementations, including the H.264 encoder, use the type **VT_BOOL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="4d52d-120">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="4d52d-120">Requirements</span></span>



| <span data-ttu-id="4d52d-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4d52d-121">Requirement</span></span> | <span data-ttu-id="4d52d-122">Wert</span><span class="sxs-lookup"><span data-stu-id="4d52d-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4d52d-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4d52d-123">Minimum supported client</span></span><br/> | <span data-ttu-id="4d52d-124">Windows 8 \[ Desktop-Apps \| UWP-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4d52d-124">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="4d52d-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4d52d-125">Minimum supported server</span></span><br/> | <span data-ttu-id="4d52d-126">UWP-Apps für Windows Server \[ 2012-Desktop-Apps \|\]</span><span class="sxs-lookup"><span data-stu-id="4d52d-126">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="4d52d-127">Header</span><span class="sxs-lookup"><span data-stu-id="4d52d-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="4d52d-128"><dt>Codecapi.h</dt></span><span class="sxs-lookup"><span data-stu-id="4d52d-128"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4d52d-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4d52d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d52d-130">Media Foundation Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4d52d-130">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="4d52d-131">**ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="4d52d-131">**ICodecAPI**</span></span>](/windows/desktop/api/strmif/nn-strmif-icodecapi)
</dt> </dl>

 

