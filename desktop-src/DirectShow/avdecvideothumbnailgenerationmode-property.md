---
description: Aktiviert oder deaktiviert den Miniatur Ansichts Generierungs Modus in einem Video Decoder.
ms.assetid: c640d915-585b-481d-aa49-0d4a559d291c
title: Avdecvideothumbnailgenerationmode-Eigenschaft (codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5aa2a9c8b095c0fdb0d44a5a12fdfe954b89ba49
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103958073"
---
# <a name="avdecvideothumbnailgenerationmode-property"></a><span data-ttu-id="d4fcb-103">Avdecvideothumbnailgenerationmode-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d4fcb-103">AVDecVideoThumbnailGenerationMode property</span></span>

<span data-ttu-id="d4fcb-104">Aktiviert oder deaktiviert den Miniatur Ansichts Generierungs Modus in einem Video Decoder.</span><span class="sxs-lookup"><span data-stu-id="d4fcb-104">Enables or disables thumbnail generation mode in a video decoder.</span></span>

<span data-ttu-id="d4fcb-105">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="d4fcb-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="d4fcb-106">Datentyp</span><span class="sxs-lookup"><span data-stu-id="d4fcb-106">Data type</span></span>

<span data-ttu-id="d4fcb-107">**Variant \_ bool** (**VT \_ bool**)</span><span class="sxs-lookup"><span data-stu-id="d4fcb-107">**VARIANT\_BOOL** (**VT\_BOOL**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="d4fcb-108">Eigenschaften-GUID</span><span class="sxs-lookup"><span data-stu-id="d4fcb-108">Property GUID</span></span>

<span data-ttu-id="d4fcb-109">**Codecapi \_ avdecvideothumbnailgenerationmode**</span><span class="sxs-lookup"><span data-stu-id="d4fcb-109">**CODECAPI\_AVDecVideoThumbnailGenerationMode**</span></span>

## <a name="remarks"></a><span data-ttu-id="d4fcb-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d4fcb-110">Remarks</span></span>

<span data-ttu-id="d4fcb-111">Wenn der Wert **Variant \_ true** ist, verwendet der Decoder eine Einstellung, die für die schnelle Generierung von Miniaturbildern optimiert ist.</span><span class="sxs-lookup"><span data-stu-id="d4fcb-111">If the value is **VARIANT\_TRUE**, the decoder uses a setting that is optimized to generate thumbnail images quickly.</span></span> <span data-ttu-id="d4fcb-112">(Beispielsweise können B-oder P-Frames übersprungen werden.) Andernfalls verwendet der Decoder die normalen Decodierungs Einstellungen, wenn der Wert **Variant \_ false** ist.</span><span class="sxs-lookup"><span data-stu-id="d4fcb-112">(For example, it might skip B or P frames.) Otherwise, if the value is **VARIANT\_FALSE**, the decoder uses its normal decoding settings.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4fcb-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d4fcb-113">Requirements</span></span>



| <span data-ttu-id="d4fcb-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d4fcb-114">Requirement</span></span> | <span data-ttu-id="d4fcb-115">Wert</span><span class="sxs-lookup"><span data-stu-id="d4fcb-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d4fcb-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d4fcb-116">Minimum supported client</span></span><br/> | <span data-ttu-id="d4fcb-117">Windows 2000 Professional \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="d4fcb-117">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="d4fcb-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d4fcb-118">Minimum supported server</span></span><br/> | <span data-ttu-id="d4fcb-119">Windows 2000 Server \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="d4fcb-119">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="d4fcb-120">Header</span><span class="sxs-lookup"><span data-stu-id="d4fcb-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="d4fcb-121"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="d4fcb-121"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4fcb-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d4fcb-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4fcb-123">Eigenschaften der Codec-API</span><span class="sxs-lookup"><span data-stu-id="d4fcb-123">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="d4fcb-124">**Icodecapi-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="d4fcb-124">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




