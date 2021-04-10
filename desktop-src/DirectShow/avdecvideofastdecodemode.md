---
description: Ruft die videodecodierungs Geschwindigkeit ab oder legt Sie fest
ms.assetid: 76F7013D-C172-4D31-93BC-EA3D186EB14C
title: Avdecvideofastdecodemode-Eigenschaft (codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 355c085731befedbcb9245a67870d9d609a92c6f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125264"
---
# <a name="avdecvideofastdecodemode-property"></a><span data-ttu-id="c6ca3-103">Avdecvideofastdecodemode (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="c6ca3-103">AVDecVideoFastDecodeMode property</span></span>

<span data-ttu-id="c6ca3-104">Ruft die videodecodierungs Geschwindigkeit ab oder legt Sie fest</span><span class="sxs-lookup"><span data-stu-id="c6ca3-104">Gets or sets the video decoding speed.</span></span>

## <a name="data-type"></a><span data-ttu-id="c6ca3-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="c6ca3-105">Data type</span></span>

<span data-ttu-id="c6ca3-106">**UInt32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="c6ca3-106">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="c6ca3-107">Eigenschaften-GUID</span><span class="sxs-lookup"><span data-stu-id="c6ca3-107">Property GUID</span></span>

<span data-ttu-id="c6ca3-108">**Codecapi \_ avdecvideofastdecodemode**</span><span class="sxs-lookup"><span data-stu-id="c6ca3-108">**CODECAPI\_AVDecVideoFastDecodeMode**</span></span>

## <a name="property-value"></a><span data-ttu-id="c6ca3-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="c6ca3-109">Property value</span></span>

<span data-ttu-id="c6ca3-110">Der Wert dieser Eigenschaft kann zwischen 0 und 32 liegen. der Wert 0 gibt eine normale Decodierung an, und 32 ist der schnellste Decodierungs Modus.</span><span class="sxs-lookup"><span data-stu-id="c6ca3-110">The value of this property can range from 0 to 32, where 0 indicates normal decoding and 32 is the fastest decoding mode.</span></span> <span data-ttu-id="c6ca3-111">Das genaue Verhalten hängt von der Decoder-Implementierung ab.</span><span class="sxs-lookup"><span data-stu-id="c6ca3-111">The exact behavior depends on the decoder implementation.</span></span> <span data-ttu-id="c6ca3-112">Nicht jedes Inkrement zwischen 1 und 32 definiert notwendigerweise einen eindeutigen Modus.</span><span class="sxs-lookup"><span data-stu-id="c6ca3-112">Not every increment between 1 and 32 necessarily defines is a distinct mode.</span></span>

<span data-ttu-id="c6ca3-113">Die [**eavfastdecodemode**](/windows/desktop/api/codecapi/ne-codecapi-eavfastdecodemode) -Enumeration enthält einige vordefinierte Modi für diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="c6ca3-113">The [**eAVFastDecodeMode**](/windows/desktop/api/codecapi/ne-codecapi-eavfastdecodemode) enumeration contains some predefined modes for this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6ca3-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c6ca3-114">Requirements</span></span>



| <span data-ttu-id="c6ca3-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c6ca3-115">Requirement</span></span> | <span data-ttu-id="c6ca3-116">Wert</span><span class="sxs-lookup"><span data-stu-id="c6ca3-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c6ca3-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c6ca3-117">Minimum supported client</span></span><br/> | <span data-ttu-id="c6ca3-118">Windows 2000 Professional \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="c6ca3-118">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="c6ca3-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c6ca3-119">Minimum supported server</span></span><br/> | <span data-ttu-id="c6ca3-120">Windows 2000 Server \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="c6ca3-120">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="c6ca3-121">Header</span><span class="sxs-lookup"><span data-stu-id="c6ca3-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="c6ca3-122"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="c6ca3-122"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6ca3-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c6ca3-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6ca3-124">Eigenschaften der Codec-API</span><span class="sxs-lookup"><span data-stu-id="c6ca3-124">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="c6ca3-125">**Icodecapi-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="c6ca3-125">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




