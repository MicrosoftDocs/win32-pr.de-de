---
description: Gibt an, ob der Decoder innerhalb von Frames mit fehlenden Verweis Rahmen löscht.
ms.assetid: 9007d5a8-f498-4394-a4e6-02a7616f3e2a
title: Avdecvideodroppicwithmissingref-Eigenschaft (codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e0c3e435ab685fca2f23fa9d0268a5e48d5387e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104213884"
---
# <a name="avdecvideodroppicwithmissingref-property"></a><span data-ttu-id="48121-103">Avdecvideodroppicwithmissingref (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="48121-103">AVDecVideoDropPicWithMissingRef property</span></span>

<span data-ttu-id="48121-104">Gibt an, ob der Decoder innerhalb von Frames mit fehlenden Verweis Rahmen löscht.</span><span class="sxs-lookup"><span data-stu-id="48121-104">Specifies whether the decoder drops intra frames with missing reference frames.</span></span>

<span data-ttu-id="48121-105">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="48121-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="48121-106">Datentyp</span><span class="sxs-lookup"><span data-stu-id="48121-106">Data type</span></span>

<span data-ttu-id="48121-107">**Variant \_ bool** (**VT \_ bool**)</span><span class="sxs-lookup"><span data-stu-id="48121-107">**VARIANT\_BOOL** (**VT\_BOOL**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="48121-108">Eigenschaften-GUID</span><span class="sxs-lookup"><span data-stu-id="48121-108">Property GUID</span></span>

<span data-ttu-id="48121-109">**Codecapi \_ avdecvideodroppicwithmissingref**</span><span class="sxs-lookup"><span data-stu-id="48121-109">**CODECAPI\_AVDecVideoDropPicWithMissingRef**</span></span>

## <a name="remarks"></a><span data-ttu-id="48121-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="48121-110">Remarks</span></span>

<span data-ttu-id="48121-111">Wenn der Bitstrom beschädigt ist, weist ein Frame möglicherweise fehlende Verweis Rahmen auf.</span><span class="sxs-lookup"><span data-stu-id="48121-111">If the bitstream is corrupted, a frame might have missing reference frames.</span></span> <span data-ttu-id="48121-112">Wenn der Wert dieser Eigenschaft **Variant \_ true** ist, löscht der Decoder den Frame.</span><span class="sxs-lookup"><span data-stu-id="48121-112">If the value of this property is **VARIANT\_TRUE**, the decoder drops the frame.</span></span> <span data-ttu-id="48121-113">Wenn der Wert **Variant \_ false** ist, versucht der Decoder, den Frame zu decodieren, wobei ein oder mehrere nahe gelegene Frames als Bezugsrahmen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="48121-113">If the value is **VARIANT\_FALSE**, the decoder attempts to decode the frame, using one or more nearby frames as reference frames.</span></span> <span data-ttu-id="48121-114">Der sich ergebende decodierte Frame verfügt über blockierende Artefakte.</span><span class="sxs-lookup"><span data-stu-id="48121-114">The resulting decoded frame will have blocking artifacts.</span></span>

## <a name="requirements"></a><span data-ttu-id="48121-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="48121-115">Requirements</span></span>



| <span data-ttu-id="48121-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="48121-116">Requirement</span></span> | <span data-ttu-id="48121-117">Wert</span><span class="sxs-lookup"><span data-stu-id="48121-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="48121-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="48121-118">Minimum supported client</span></span><br/> | <span data-ttu-id="48121-119">Windows 2000 Professional \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="48121-119">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="48121-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="48121-120">Minimum supported server</span></span><br/> | <span data-ttu-id="48121-121">Windows 2000 Server \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="48121-121">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="48121-122">Header</span><span class="sxs-lookup"><span data-stu-id="48121-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="48121-123"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="48121-123"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48121-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="48121-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48121-125">Eigenschaften der Codec-API</span><span class="sxs-lookup"><span data-stu-id="48121-125">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="48121-126">**Icodecapi-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="48121-126">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




