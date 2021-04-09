---
description: Gibt an, wie der decodierte Videostream mit Zeilen Sprung verknüpft ist.
ms.assetid: a2b95b90-1c58-47f3-b6a8-0f3f6f1a416c
title: Avdecvideoinputscantype-Eigenschaft (codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 560db1cd1cf0238fc9e50257f2f24559e9a94c8f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103860383"
---
# <a name="avdecvideoinputscantype-property"></a><span data-ttu-id="56cda-103">Avdecvideoinputscantype (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="56cda-103">AVDecVideoInputScanType property</span></span>

<span data-ttu-id="56cda-104">Gibt an, wie der decodierte Videostream mit Zeilen Sprung verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="56cda-104">Specifies how the decoded video stream is interlaced.</span></span>

<span data-ttu-id="56cda-105">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="56cda-105">This property is read-only.</span></span>

## <a name="data-type"></a><span data-ttu-id="56cda-106">Datentyp</span><span class="sxs-lookup"><span data-stu-id="56cda-106">Data type</span></span>

<span data-ttu-id="56cda-107">**UInt32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="56cda-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="56cda-108">Eigenschaften-GUID</span><span class="sxs-lookup"><span data-stu-id="56cda-108">Property GUID</span></span>

<span data-ttu-id="56cda-109">**Codecapi \_ avdecvideoinputscantype**</span><span class="sxs-lookup"><span data-stu-id="56cda-109">**CODECAPI\_AVDecVideoInputScanType**</span></span>

## <a name="property-value"></a><span data-ttu-id="56cda-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="56cda-110">Property value</span></span>

<span data-ttu-id="56cda-111">Der Wert dieser Eigenschaft ist ein Member der [**eavdecvideoinputscantype**](/windows/win32/api/codecapi/ne-codecapi-eavdecvideoinputscantype) -Enumeration.</span><span class="sxs-lookup"><span data-stu-id="56cda-111">The value of this property is a member of the [**eAVDecVideoInputScanType**](/windows/win32/api/codecapi/ne-codecapi-eavdecvideoinputscantype) enumeration.</span></span>

## <a name="remarks"></a><span data-ttu-id="56cda-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="56cda-112">Remarks</span></span>

<span data-ttu-id="56cda-113">Die oberen 16 Bits des Werts enthalten die Breite, und die unteren 16 Bits enthalten die Höhe.</span><span class="sxs-lookup"><span data-stu-id="56cda-113">The upper 16 bits of the value contain the width, and the lower 16 bits contain the height.</span></span>

## <a name="requirements"></a><span data-ttu-id="56cda-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="56cda-114">Requirements</span></span>



| <span data-ttu-id="56cda-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="56cda-115">Requirement</span></span> | <span data-ttu-id="56cda-116">Wert</span><span class="sxs-lookup"><span data-stu-id="56cda-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="56cda-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="56cda-117">Minimum supported client</span></span><br/> | <span data-ttu-id="56cda-118">Windows 2000 Professional \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="56cda-118">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="56cda-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="56cda-119">Minimum supported server</span></span><br/> | <span data-ttu-id="56cda-120">Windows 2000 Server \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="56cda-120">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="56cda-121">Header</span><span class="sxs-lookup"><span data-stu-id="56cda-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="56cda-122"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="56cda-122"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56cda-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="56cda-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56cda-124">Eigenschaften der Codec-API</span><span class="sxs-lookup"><span data-stu-id="56cda-124">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="56cda-125">**Icodecapi-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="56cda-125">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

