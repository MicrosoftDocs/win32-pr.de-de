---
description: Gibt den Typ der Einheit an, die in einem IMF Sample in einer MF SampleExtension \_ forwardeddecodeunits-Auflistung enthalten ist.
ms.assetid: B74890ED-9586-475B-8C77-457ECB893980
title: MF_CUSTOM_DECODE_UNIT_TYPE-Enumeration (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MF_CUSTOM_DECODE_UNIT_TYPE
api_type:
- HeaderDef
api_location:
- mfapi.h
ms.openlocfilehash: 406f6b3f6b93ced212ccf06910b69761ac0dfd9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215153"
---
# <a name="mf_custom_decode_unit_type-enumeration"></a><span data-ttu-id="9c48a-103">\_Benutzerdefinierte benutzerdefinierte \_ \_ \_ Benutzertyp-Enumeration</span><span class="sxs-lookup"><span data-stu-id="9c48a-103">MF\_CUSTOM\_DECODE\_UNIT\_TYPE enumeration</span></span>

<span data-ttu-id="9c48a-104">Gibt den Typ der Einheit an, die in einem [**IMF Sample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) in einer [MF SampleExtension \_ forwardeddecodeunits](mfsampleextension-forwardeddecodeunits.md) -Auflistung enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="9c48a-104">Specifies the type of unit contained in an [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) in a [MFSampleExtension\_ForwardedDecodeUnits](mfsampleextension-forwardeddecodeunits.md) collection.</span></span>

## <a name="members"></a><span data-ttu-id="9c48a-105">Member</span><span class="sxs-lookup"><span data-stu-id="9c48a-105">Members</span></span>



| <span data-ttu-id="9c48a-106">Member</span><span class="sxs-lookup"><span data-stu-id="9c48a-106">Member</span></span>                    | <span data-ttu-id="9c48a-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9c48a-107">Description</span></span>                                                             | <span data-ttu-id="9c48a-108">Wert</span><span class="sxs-lookup"><span data-stu-id="9c48a-108">Value</span></span> |
|---------------------------|-------------------------------------------------------------------------|-------|
| <span data-ttu-id="9c48a-109">**MF- \_ decodierungseinheit- \_ \_ nal**</span><span class="sxs-lookup"><span data-stu-id="9c48a-109">**MF\_DECODE\_UNIT\_NAL**</span></span> | <span data-ttu-id="9c48a-110">Der Einheitstyp ist "Network Abstraktion Layer Unit (nalu)".</span><span class="sxs-lookup"><span data-stu-id="9c48a-110">The unit type is network abstraction layer unit (NALU).</span></span> <br/>     | <span data-ttu-id="9c48a-111">0</span><span class="sxs-lookup"><span data-stu-id="9c48a-111">0</span></span>     |
| <span data-ttu-id="9c48a-112">**MF- \_ Decodierung ( \_ Einheit) \_**</span><span class="sxs-lookup"><span data-stu-id="9c48a-112">**MF\_DECODE\_UNIT\_SEI**</span></span> | <span data-ttu-id="9c48a-113">Der Einheitstyp ist ergänzende Erweiterungs Informationen (ist).</span><span class="sxs-lookup"><span data-stu-id="9c48a-113">The unit type is Supplemental Enhancement Information (SEI).</span></span><br/> | <span data-ttu-id="9c48a-114">1</span><span class="sxs-lookup"><span data-stu-id="9c48a-114">1</span></span>     |



## <a name="remarks"></a><span data-ttu-id="9c48a-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9c48a-115">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="9c48a-116">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="9c48a-116">Requirements</span></span>



| <span data-ttu-id="9c48a-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9c48a-117">Requirement</span></span> | <span data-ttu-id="9c48a-118">Wert</span><span class="sxs-lookup"><span data-stu-id="9c48a-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9c48a-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9c48a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="9c48a-120">Windows 10, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9c48a-120">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="9c48a-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9c48a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="9c48a-122">Nur Windows Server 2016 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9c48a-122">Windows Server 2016 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="9c48a-123">Header</span><span class="sxs-lookup"><span data-stu-id="9c48a-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="9c48a-124"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="9c48a-124"><dt>Mfapi.h</dt></span></span> </dl> |



 

 




