---
description: Gibt an, ob der Codec versuchen soll, laute Rahmen Ränder zu erkennen und zu entfernen.
ms.assetid: fdb4f3a8-1447-4e1e-a208-0f9b717f7626
title: MFPKEY_NOISEEDGEREMOVAL-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30acd92bae7693d0714e42d6b4f832a521557bf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215508"
---
# <a name="mfpkey_noiseedgeremoval-property"></a><span data-ttu-id="cfa9f-103">Mfpkey \_ noiseedgeremuval-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="cfa9f-103">MFPKEY\_NOISEEDGEREMOVAL Property</span></span>

<span data-ttu-id="cfa9f-104">Gibt an, ob der Codec versuchen soll, laute Rahmen Ränder zu erkennen und zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="cfa9f-104">Specifies whether the codec should attempt to detect noisy frame edges and remove them.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="cfa9f-105">Konstante für IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="cfa9f-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="cfa9f-106">g \_ wszwmvcnoiseedgeremuval</span><span class="sxs-lookup"><span data-stu-id="cfa9f-106">g\_wszWMVCNoiseEdgeRemoval</span></span>

## <a name="data-type"></a><span data-ttu-id="cfa9f-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="cfa9f-107">Data Type</span></span>

<span data-ttu-id="cfa9f-108">VT \_ bool</span><span class="sxs-lookup"><span data-stu-id="cfa9f-108">VT\_BOOL</span></span>

## <a name="default-value"></a><span data-ttu-id="cfa9f-109">Standardwert</span><span class="sxs-lookup"><span data-stu-id="cfa9f-109">Default Value</span></span>

<span data-ttu-id="cfa9f-110">false</span><span class="sxs-lookup"><span data-stu-id="cfa9f-110">FALSE</span></span>

## <a name="remarks"></a><span data-ttu-id="cfa9f-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cfa9f-111">Remarks</span></span>

<span data-ttu-id="cfa9f-112">Eine laute Rahmen Kante ist normalerweise die VBI-Daten (Vertical Blank Interval) aus einem Broadcast-TV-Rahmen.</span><span class="sxs-lookup"><span data-stu-id="cfa9f-112">A noisy frame edge is usually the vertical blanking interval (VBI) data from a frame of broadcast television.</span></span> <span data-ttu-id="cfa9f-113">VBI stellt die ersten 21 Überprüfungs Linien des Fernseh Rahmens dar.</span><span class="sxs-lookup"><span data-stu-id="cfa9f-113">The VBI is the first 21 scan lines of the television frame.</span></span> <span data-ttu-id="cfa9f-114">Diese Scan Zeilen enthalten keine Videodaten – Sie enthalten Daten über den Broadcast.</span><span class="sxs-lookup"><span data-stu-id="cfa9f-114">These scan lines do not contain video data—they contain data about the broadcast.</span></span> <span data-ttu-id="cfa9f-115">Wenn ein Fernsehsignal von einer aufzeichnungskarte aufgezeichnet wird, wird die VBI normalerweise aus dem Frame entfernt.</span><span class="sxs-lookup"><span data-stu-id="cfa9f-115">When a television signal is recorded by a capture card, the VBI is usually removed from the frame.</span></span> <span data-ttu-id="cfa9f-116">Die vom Codec ausgeführte Erkennung und Korrektur von Noisy Edge kann nur einen Rand korrigieren, der drei oder weniger Rauschen enthält.</span><span class="sxs-lookup"><span data-stu-id="cfa9f-116">The noisy edge detection and correction performed by the codec can only correct an edge that has three or fewer lines of noise.</span></span> <span data-ttu-id="cfa9f-117">Wenn das erfasste Video mehr als drei Laute Zeilen enthält, besteht ein Problem mit der Hardware, die zum Erfassen des Videos verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="cfa9f-117">If captured video contains more than three noisy lines, there is a problem with the hardware used to capture the video.</span></span>

<span data-ttu-id="cfa9f-118">Wenn der Codec darauf festgelegt ist, laute Ränder zu entfernen, werden die Linien, die sich neben dem lärmenden Rand befinden, zum Auffüllen des Frames dupliziert.</span><span class="sxs-lookup"><span data-stu-id="cfa9f-118">If the codec is set to remove noisy edges, it duplicates lines adjacent to the noisy edge to fill in the frame.</span></span>

## <a name="requirements"></a><span data-ttu-id="cfa9f-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cfa9f-119">Requirements</span></span>



| <span data-ttu-id="cfa9f-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cfa9f-120">Requirement</span></span> | <span data-ttu-id="cfa9f-121">Wert</span><span class="sxs-lookup"><span data-stu-id="cfa9f-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cfa9f-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cfa9f-122">Minimum supported client</span></span><br/> | <span data-ttu-id="cfa9f-123">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cfa9f-123">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="cfa9f-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cfa9f-124">Minimum supported server</span></span><br/> | <span data-ttu-id="cfa9f-125">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cfa9f-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="cfa9f-126">Header</span><span class="sxs-lookup"><span data-stu-id="cfa9f-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="cfa9f-127"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="cfa9f-127"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cfa9f-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cfa9f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cfa9f-129">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="cfa9f-129">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




