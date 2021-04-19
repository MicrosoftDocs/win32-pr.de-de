---
description: Ein Wert, der angibt, ob ein Frame mithilfe der aktiven Infrarotbeleuchtung (IR) erfasst wurde.
ms.assetid: D84772C8-902F-4302-8288-0430892A1896
title: MF_CAPTURE_METADATA_FRAME_ILLUMINATION-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb9aa60b5e921e99ac4f4c56cb4643af8389aa91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348811"
---
# <a name="mf_capture_metadata_frame_illumination-attribute"></a><span data-ttu-id="a75f6-103">MF- \_ Attribut zur Erfassung von \_ \_ metadatenframe \_</span><span class="sxs-lookup"><span data-stu-id="a75f6-103">MF\_CAPTURE\_METADATA\_FRAME\_ILLUMINATION attribute</span></span>

<span data-ttu-id="a75f6-104">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="a75f6-104">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="a75f6-105">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="a75f6-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="a75f6-106">Ein Wert, der angibt, ob ein Frame mithilfe der aktiven Infrarotbeleuchtung (IR) erfasst wurde.</span><span class="sxs-lookup"><span data-stu-id="a75f6-106">A value indicating whether a frame was captured using active infrared (IR) illumination.</span></span>

## <a name="data-type"></a><span data-ttu-id="a75f6-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="a75f6-107">Data type</span></span>

<span data-ttu-id="a75f6-108">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="a75f6-108">**UINT64**</span></span>

## <a name="remarks"></a><span data-ttu-id="a75f6-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a75f6-109">Remarks</span></span>

<span data-ttu-id="a75f6-110">Dieses Attribut ist eine Bitmaske.</span><span class="sxs-lookup"><span data-stu-id="a75f6-110">This attribute is a bitmask.</span></span> <span data-ttu-id="a75f6-111">Es handelt sich um einen 64-Bit-Wert für die Abwärtskompatibilität.</span><span class="sxs-lookup"><span data-stu-id="a75f6-111">It is a 64 bit value for backward compatibility.</span></span>

<span data-ttu-id="a75f6-112">Die aktive Beleuchtung ist, wenn ein Gerät einen Licht Emitter hat, der sich in der Nähe der IR-Kamera befindet und einen Lichtstrahl ausgibt, um die Szene zu beleuchten</span><span class="sxs-lookup"><span data-stu-id="a75f6-112">Active illumination is when a device has a light emitter close to the IR camera emitting a beam of light to illuminate the scene, typically emitting IR light so it won’t disturb human eyes.</span></span> <span data-ttu-id="a75f6-113">Legen Sie Value auf (Wert & 0x1)! = 0 fest, wenn Frame aufgezeichnet wurde, als die aktive Beleuchtung aktiviert war, und legen Sie (Wert & 0x1) = = 0 fest, wenn die aktive Beleuchtung deaktiviert war.</span><span class="sxs-lookup"><span data-stu-id="a75f6-113">Set value to (value & 0x1) != 0 if frame was captured when active illumination was on and set (value & 0x1) == 0 if active illumination was off.</span></span>

## <a name="requirements"></a><span data-ttu-id="a75f6-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a75f6-114">Requirements</span></span>



| <span data-ttu-id="a75f6-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a75f6-115">Requirement</span></span> | <span data-ttu-id="a75f6-116">Wert</span><span class="sxs-lookup"><span data-stu-id="a75f6-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a75f6-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a75f6-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a75f6-118">Windows 10, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a75f6-118">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="a75f6-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a75f6-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a75f6-120">Windows Server, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a75f6-120">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                      |
| <span data-ttu-id="a75f6-121">Header</span><span class="sxs-lookup"><span data-stu-id="a75f6-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="a75f6-122"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="a75f6-122"><dt>Mfapi.h</dt></span></span> </dl> |



 

 




