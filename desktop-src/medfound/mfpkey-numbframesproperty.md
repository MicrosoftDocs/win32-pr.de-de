---
description: Gibt die Anzahl der bidirektionalen Vorhersage Rahmen (B-Frames) an.
ms.assetid: 8bd95baa-c130-4616-8ab7-7d902162e4ed
title: MFPKEY_NUMBFRAMES-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc3b0655a4a5e24b92f9699b198f10232de8edf8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106372985"
---
# <a name="mfpkey_numbframes-property"></a><span data-ttu-id="666c2-103">Mfpkey- \_ numbframes (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="666c2-103">MFPKEY\_NUMBFRAMES Property</span></span>

<span data-ttu-id="666c2-104">Gibt die Anzahl der bidirektionalen Vorhersage Rahmen (B-Frames) an.</span><span class="sxs-lookup"><span data-stu-id="666c2-104">Specifies the number of bidirectional predictive frames (B-frames).</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="666c2-105">Konstante für IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="666c2-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="666c2-106">g \_ wszwmvcnumbframes</span><span class="sxs-lookup"><span data-stu-id="666c2-106">g\_wszWMVCNumBFrames</span></span>

## <a name="data-type"></a><span data-ttu-id="666c2-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="666c2-107">Data Type</span></span>

<span data-ttu-id="666c2-108">VT-I4</span><span class="sxs-lookup"><span data-stu-id="666c2-108">VT-I4</span></span>

## <a name="default-value"></a><span data-ttu-id="666c2-109">Standardwert</span><span class="sxs-lookup"><span data-stu-id="666c2-109">Default Value</span></span>

<span data-ttu-id="666c2-110">0</span><span class="sxs-lookup"><span data-stu-id="666c2-110">0</span></span>

## <a name="remarks"></a><span data-ttu-id="666c2-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="666c2-111">Remarks</span></span>

<span data-ttu-id="666c2-112">Standardmäßig verwendet Windows Media Video 9 nur die Rahmen (I-Frames) (I-Frames), die auch als Keyframes oder Anker Frames bezeichnet werden, bei denen es sich um vollständig codierte Frames und Vorhersage Rahmen (P-Frames) handelt, die als Unterschied zum vorherigen I-Frame codiert werden.</span><span class="sxs-lookup"><span data-stu-id="666c2-112">By default, Windows Media Video 9 uses only intraframes (I-frames), also known as key frames or anchor frames, which are fully encoded frames, and predictive frames (P-frames), which are encoded as a difference from the previous I-frame.</span></span> <span data-ttu-id="666c2-113">B-Frames unterscheiden sich von P-Frames, da Sie sowohl die Unterschiede zwischen dem vorherigen Frame als auch die Unterschiede zwischen dem folgenden Frame speichern.</span><span class="sxs-lookup"><span data-stu-id="666c2-113">B-frames are different from P-frames because they store both the differences from the previous frame and the differences from the following frame.</span></span>

<span data-ttu-id="666c2-114">Wenn Sie den Codec so konfigurieren, dass er b-Frames verwendet, wird die angegebene Anzahl von b-Frames zwischen jedem Paar von Frames des Typs I oder P verwendet.</span><span class="sxs-lookup"><span data-stu-id="666c2-114">When you configure the codec to uses B-frames, it will use the specified number of B-frames between each pair of frames of either I or P type.</span></span>

<span data-ttu-id="666c2-115">Wenn eine Sequenz von Frames ohne b-Frames z. b. "ippppppppi" ist, wäre dieselbe Sequenz Codierung mit zwei b-Frames "ibbpbbpbbi".</span><span class="sxs-lookup"><span data-stu-id="666c2-115">For example, if a sequence of frames without B-frames is "IPPPPPPPPI" then the same sequence encoding with two B-frames would be "IBBPBBPBBI".</span></span>

<span data-ttu-id="666c2-116">Für die meisten Inhalte sind entweder ein oder zwei B-Frames geeignet.</span><span class="sxs-lookup"><span data-stu-id="666c2-116">For most content either one or two B-frames are appropriate.</span></span> <span data-ttu-id="666c2-117">Bei höheren Datenraten ist ein B-Frame normalerweise die optimale Wahl.</span><span class="sxs-lookup"><span data-stu-id="666c2-117">At higher data rates, one B-frame is normally the optimal choice.</span></span> <span data-ttu-id="666c2-118">Drei oder mehr sind selten nützlich.</span><span class="sxs-lookup"><span data-stu-id="666c2-118">Three or more are rarely useful.</span></span>

<span data-ttu-id="666c2-119">Der gültige Wertebereich für diese Eigenschaft ist 0 bis 7.</span><span class="sxs-lookup"><span data-stu-id="666c2-119">The valid range of values for this property is 0 to 7.</span></span>

## <a name="requirements"></a><span data-ttu-id="666c2-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="666c2-120">Requirements</span></span>



| <span data-ttu-id="666c2-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="666c2-121">Requirement</span></span> | <span data-ttu-id="666c2-122">Wert</span><span class="sxs-lookup"><span data-stu-id="666c2-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="666c2-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="666c2-123">Minimum supported client</span></span><br/> | <span data-ttu-id="666c2-124">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="666c2-124">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="666c2-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="666c2-125">Minimum supported server</span></span><br/> | <span data-ttu-id="666c2-126">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="666c2-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="666c2-127">Header</span><span class="sxs-lookup"><span data-stu-id="666c2-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="666c2-128"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="666c2-128"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="666c2-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="666c2-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="666c2-130">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="666c2-130">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




