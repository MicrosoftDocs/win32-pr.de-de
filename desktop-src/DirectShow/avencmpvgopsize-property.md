---
description: Gibt die maximale Anzahl von Bildern eines GOP-Headers (Group of Pictures) zum nächsten GOP-Header an.
ms.assetid: 90433df4-5a96-4bc2-a780-93306abcb0a4
title: Avencmpvgopsize-Eigenschaft (codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c8907d0992153039b1af9a9a0e82ee5782b525d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104041266"
---
# <a name="avencmpvgopsize-property"></a><span data-ttu-id="ae2ae-103">Avencmpvgopsize (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="ae2ae-103">AVEncMPVGOPSize property</span></span>

<span data-ttu-id="ae2ae-104">Gibt die maximale Anzahl von Bildern eines GOP-Headers (Group of Pictures) zum nächsten GOP-Header an.</span><span class="sxs-lookup"><span data-stu-id="ae2ae-104">Specifies the maximum number of pictures from one group-of-pictures (GOP) header to the next GOP header.</span></span>

<span data-ttu-id="ae2ae-105">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="ae2ae-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="ae2ae-106">Datentyp</span><span class="sxs-lookup"><span data-stu-id="ae2ae-106">Data type</span></span>

<span data-ttu-id="ae2ae-107">**UInt32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="ae2ae-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="ae2ae-108">Eigenschaften-GUID</span><span class="sxs-lookup"><span data-stu-id="ae2ae-108">Property GUID</span></span>

<span data-ttu-id="ae2ae-109">**Codecapi \_ avencmpvgopsize**</span><span class="sxs-lookup"><span data-stu-id="ae2ae-109">**CODECAPI\_AVEncMPVGOPSize**</span></span>

## <a name="property-value"></a><span data-ttu-id="ae2ae-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="ae2ae-110">Property value</span></span>

<span data-ttu-id="ae2ae-111">Encoder können diese Eigenschaft als enumerationsset oder als linearen Bereich implementieren.</span><span class="sxs-lookup"><span data-stu-id="ae2ae-111">Encoders can implement this property as an enumerated set or as a linear range.</span></span>

## <a name="remarks"></a><span data-ttu-id="ae2ae-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ae2ae-112">Remarks</span></span>

<span data-ttu-id="ae2ae-113">Legen Sie diese Eigenschaft fest, bevor Sie eine Aufzeichnung starten.</span><span class="sxs-lookup"><span data-stu-id="ae2ae-113">Set this property before starting a recording.</span></span>

<span data-ttu-id="ae2ae-114">**Gilt für Windows 8:** Die codierte GOP-Größe muss mit dieser Eigenschaft kleiner oder gleich der angegebenen Zahl sein, um das gleiche B-Frame-Muster im gesamten GOP oder aufgrund von Szenen Änderungen durch [codecapi \_ avencmpvdefaultbpicturecount](avencmpvdefaultbpicturecount-property.md) festzulegen.</span><span class="sxs-lookup"><span data-stu-id="ae2ae-114">**Applies to Windows 8:** The encoded GOP size shall be smaller than or equal to the specified number through this property, in order to keep the same B frame pattern set by [CODECAPI\_AVEncMPVDefaultBPictureCount](avencmpvdefaultbpicturecount-property.md) throughout the GOP or due to scene change.</span></span> <span data-ttu-id="ae2ae-115">Wenn z. B. die Anzahl der B-Frames in einem GOP als 2 angegeben wird und die GOP-Größe 11 beträgt, erzeugt der Encoder eine GOP-Größe von 10 Frames oder weniger.</span><span class="sxs-lookup"><span data-stu-id="ae2ae-115">For example, when the number of B frames in a GOP is specified to be 2, and GOP size is 11, then encoder shall produce GOP size of 10 frames or less.</span></span> <span data-ttu-id="ae2ae-116">Wenn Szenen Änderungen in der Mitte eines GOP stattfinden, fügt der Encoder möglicherweise auch einen Keyframe ein und erzeugt kleinere GOP.</span><span class="sxs-lookup"><span data-stu-id="ae2ae-116">When scene change happens in the middle of a GOP, encoder might also insert key frame and produce smaller GOP.</span></span>

<span data-ttu-id="ae2ae-117">GOP size 0 ist Codierungs abhängig, und Encoder können basierend auf Ihrer Implementierung/Qualität/Leistung verschiedene GOP-Größen auswählen.</span><span class="sxs-lookup"><span data-stu-id="ae2ae-117">GOP size 0 is encoder dependent and encoders can choose different GOP sizes based on their implementation/quality/performance.</span></span> <span data-ttu-id="ae2ae-118">Encoder sollten die GOP-Größe berücksichtigen und in diesem Fall B-Frames kürzen.</span><span class="sxs-lookup"><span data-stu-id="ae2ae-118">Encoders should honor the GOP size and truncate B frames in this case.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae2ae-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ae2ae-119">Requirements</span></span>



| <span data-ttu-id="ae2ae-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ae2ae-120">Requirement</span></span> | <span data-ttu-id="ae2ae-121">Wert</span><span class="sxs-lookup"><span data-stu-id="ae2ae-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ae2ae-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ae2ae-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ae2ae-123">Windows 2000 Professional \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="ae2ae-123">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="ae2ae-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ae2ae-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ae2ae-125">Windows 2000 Server \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="ae2ae-125">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="ae2ae-126">Header</span><span class="sxs-lookup"><span data-stu-id="ae2ae-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="ae2ae-127"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="ae2ae-127"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ae2ae-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ae2ae-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae2ae-129">Eigenschaften der Codec-API</span><span class="sxs-lookup"><span data-stu-id="ae2ae-129">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="ae2ae-130">**Icodecapi-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="ae2ae-130">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




