---
description: Gibt an, ob der Encoder Inverse Telecine ausführt.
ms.assetid: 3467b0c8-c27d-448a-8cbf-971307e4c408
title: Avencvideoinverabtelecineenable-Eigenschaft (codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31eac80651eb80d933c4f40ef22303c4858783d2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124994"
---
# <a name="avencvideoinversetelecineenable-property"></a><span data-ttu-id="48601-103">Avencvideoinverabtelecineenable (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="48601-103">AVEncVideoInverseTelecineEnable property</span></span>

<span data-ttu-id="48601-104">Gibt an, ob der Encoder Inverse Telecine ausführt.</span><span class="sxs-lookup"><span data-stu-id="48601-104">Specifies whether the encoder performs inverse telecine.</span></span>

<span data-ttu-id="48601-105">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="48601-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="48601-106">Datentyp</span><span class="sxs-lookup"><span data-stu-id="48601-106">Data type</span></span>

<span data-ttu-id="48601-107">**Variant \_ bool** (**VT \_ bool**)</span><span class="sxs-lookup"><span data-stu-id="48601-107">**VARIANT\_BOOL** (**VT\_BOOL**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="48601-108">Eigenschaften-GUID</span><span class="sxs-lookup"><span data-stu-id="48601-108">Property GUID</span></span>

<span data-ttu-id="48601-109">**Codecapi \_ avencvideoinverabtelecineenable**</span><span class="sxs-lookup"><span data-stu-id="48601-109">**CODECAPI\_AVEncVideoInverseTelecineEnable**</span></span>

## <a name="remarks"></a><span data-ttu-id="48601-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="48601-110">Remarks</span></span>

<span data-ttu-id="48601-111">Wenn der Wert **Variant \_ true** ist, führt der Encoder Inverse Telecine aus.</span><span class="sxs-lookup"><span data-stu-id="48601-111">If the value is **VARIANT\_TRUE**, the encoder performs inverse telecine.</span></span> <span data-ttu-id="48601-112">Wenn Inverse Telecine nicht erforderlich ist, legen Sie diese Eigenschaft auf **Variant \_ false** fest.</span><span class="sxs-lookup"><span data-stu-id="48601-112">If inverse telecine is not required, set this property to **VARIANT\_FALSE**.</span></span> <span data-ttu-id="48601-113">Wenn Sie Inverse Telecine außerhalb des Encoders ausführen möchten, legen Sie diese Eigenschaft auf **Variant \_ false** fest, und legen Sie die Eigenschaft [**avencvideooutputscantype**](avencvideooutputscantype-property.md) auf eavencvideooutputscan \_ sameasinput fest.</span><span class="sxs-lookup"><span data-stu-id="48601-113">To perform inverse telecine outside of the encoder, set this property to **VARIANT\_FALSE** and set the [**AVEncVideoOutputScanType**](avencvideooutputscantype-property.md) property to eAVEncVideoOutputScan\_SameAsInput.</span></span>

## <a name="requirements"></a><span data-ttu-id="48601-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="48601-114">Requirements</span></span>



| <span data-ttu-id="48601-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="48601-115">Requirement</span></span> | <span data-ttu-id="48601-116">Wert</span><span class="sxs-lookup"><span data-stu-id="48601-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="48601-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="48601-117">Minimum supported client</span></span><br/> | <span data-ttu-id="48601-118">Windows 2000 Professional \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="48601-118">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="48601-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="48601-119">Minimum supported server</span></span><br/> | <span data-ttu-id="48601-120">Windows 2000 Server \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="48601-120">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="48601-121">Header</span><span class="sxs-lookup"><span data-stu-id="48601-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="48601-122"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="48601-122"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48601-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="48601-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48601-124">Eigenschaften der Codec-API</span><span class="sxs-lookup"><span data-stu-id="48601-124">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="48601-125">**Icodecapi-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="48601-125">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




