---
description: Aktiviert den Modus mit niedriger Latenz in einem Codec.
ms.assetid: 15E8FF6F-AD8C-436F-B3C0-5062B1F86E32
title: CODECAPI_AVLowLatencyMode-Eigenschaft (codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f159045f6b40d531495338b1598c214926a59612
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346666"
---
# <a name="codecapi_avlowlatencymode-property"></a><span data-ttu-id="567d7-103">Codecapi \_ avlowlatencymode-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="567d7-103">CODECAPI\_AVLowLatencyMode property</span></span>

<span data-ttu-id="567d7-104">Aktiviert den Modus mit niedriger Latenz in einem Codec.</span><span class="sxs-lookup"><span data-stu-id="567d7-104">Enables low-latency mode in a codec.</span></span>

## <a name="data-type"></a><span data-ttu-id="567d7-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="567d7-105">Data type</span></span>

<span data-ttu-id="567d7-106">**ulong** (**VT \_ bool**)</span><span class="sxs-lookup"><span data-stu-id="567d7-106">**ULONG** (**VT\_BOOL**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="567d7-107">Eigenschaften-GUID</span><span class="sxs-lookup"><span data-stu-id="567d7-107">Property GUID</span></span>

<span data-ttu-id="567d7-108">**Codecapi \_ avlowlatencymode**</span><span class="sxs-lookup"><span data-stu-id="567d7-108">**CODECAPI\_AVLowLatencyMode**</span></span>

## <a name="property-value"></a><span data-ttu-id="567d7-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="567d7-109">Property value</span></span>

<span data-ttu-id="567d7-110">Wenn der Wert ungleich 0 (null) ist, ist der Modus mit niedriger Latenzzeit aktiviert.</span><span class="sxs-lookup"><span data-stu-id="567d7-110">If the value is nonzero, low-latency mode is enabled.</span></span> <span data-ttu-id="567d7-111">Wenn der Wert 0 (null) ist, ist der Modus mit niedriger Latenz deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="567d7-111">If the value is zero, low-latency mode is disabled.</span></span>

## <a name="remarks"></a><span data-ttu-id="567d7-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="567d7-112">Remarks</span></span>

<span data-ttu-id="567d7-113">Diese Eigenschaft gilt sowohl für Encoder als auch für Decoders.</span><span class="sxs-lookup"><span data-stu-id="567d7-113">This property applies to both encoders and decoders.</span></span>

<span data-ttu-id="567d7-114">Der Modus mit niedriger Latenz ist für Echtzeitkommunikation oder Live Erfassung nützlich, wenn die Latenz minimiert werden sollte.</span><span class="sxs-lookup"><span data-stu-id="567d7-114">Low-latency mode is useful for real-time communications or live capture, when latency should be minimized.</span></span> <span data-ttu-id="567d7-115">Der Modus mit niedriger Latenz kann jedoch auch die Decodierung oder Codierungsqualität verringern.</span><span class="sxs-lookup"><span data-stu-id="567d7-115">However, low-latency mode might also reduce the decoding or encoding quality.</span></span>

<span data-ttu-id="567d7-116">Es wird erwartet, dass der Encoder keine Stichproben Verzögerung aufgrund der Neuanordnung von Frames im Codierungsprozess hinzufügt, und ein Eingabe Beispiel erstellt ein Ausgabe Beispiel.</span><span class="sxs-lookup"><span data-stu-id="567d7-116">The encoder is expected to not add any sample delay due to frame reordering in encoding process, and one input sample shall produce one output sample.</span></span> <span data-ttu-id="567d7-117">B Slices/Frames können vorhanden sein, solange Sie keine Neuanordnung von Frames im Encoder einleiten.</span><span class="sxs-lookup"><span data-stu-id="567d7-117">B slices/frames can be present as long as they do not introduce any frame re-ordering in the encoder.</span></span>

## <a name="requirements"></a><span data-ttu-id="567d7-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="567d7-118">Requirements</span></span>



| <span data-ttu-id="567d7-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="567d7-119">Requirement</span></span> | <span data-ttu-id="567d7-120">Wert</span><span class="sxs-lookup"><span data-stu-id="567d7-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="567d7-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="567d7-121">Minimum supported client</span></span><br/> | <span data-ttu-id="567d7-122">Windows 8 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="567d7-122">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="567d7-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="567d7-123">Minimum supported server</span></span><br/> | <span data-ttu-id="567d7-124">Windows Server 2012 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="567d7-124">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="567d7-125">Header</span><span class="sxs-lookup"><span data-stu-id="567d7-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="567d7-126"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="567d7-126"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="567d7-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="567d7-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="567d7-128">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="567d7-128">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="567d7-129">**Icodecapi**</span><span class="sxs-lookup"><span data-stu-id="567d7-129">**ICodecAPI**</span></span>](/windows/desktop/api/strmif/nn-strmif-icodecapi)
</dt> </dl>

 

