---
description: Gibt den postverarbeitungs Modus für den Decoder an.
ms.assetid: c6dab7f6-4a3e-45bb-b81c-5f4c39f9e954
title: MFPKEY_POSTPROCESSMODE-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4002deae63f1bdaea09ca31dd95bfec1cb594fc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361046"
---
# <a name="mfpkey_postprocessmode-property"></a><span data-ttu-id="095f2-103">Mfpkey- \_ postprocessmode-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="095f2-103">MFPKEY\_POSTPROCESSMODE Property</span></span>

<span data-ttu-id="095f2-104">Gibt den postverarbeitungs Modus für den Decoder an.</span><span class="sxs-lookup"><span data-stu-id="095f2-104">Specifies the post processing mode for the decoder.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="095f2-105">Konstante für IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="095f2-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="095f2-106">**g \_ wszwmvcforcepostprocessmode**</span><span class="sxs-lookup"><span data-stu-id="095f2-106">**g\_wszWMVCForcePostProcessMode**</span></span>

## <a name="data-type"></a><span data-ttu-id="095f2-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="095f2-107">Data Type</span></span>

<span data-ttu-id="095f2-108">**VT \_ I4**</span><span class="sxs-lookup"><span data-stu-id="095f2-108">**VT\_I4**</span></span>

## <a name="remarks"></a><span data-ttu-id="095f2-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="095f2-109">Remarks</span></span>

<span data-ttu-id="095f2-110">Legen Sie diese Eigenschaft auf einen der folgenden Werte fest.</span><span class="sxs-lookup"><span data-stu-id="095f2-110">Set this property to one of the following values.</span></span>



| <span data-ttu-id="095f2-111">Wert</span><span class="sxs-lookup"><span data-stu-id="095f2-111">Value</span></span> | <span data-ttu-id="095f2-112">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="095f2-112">Meaning</span></span>                                                                                |
|-------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="095f2-113">-1</span><span class="sxs-lookup"><span data-stu-id="095f2-113">-1</span></span>    | <span data-ttu-id="095f2-114">Der Decoder legt den postverarbeitungs Modus basierend auf verfügbaren CPU-Ressourcen adaptiv fest.</span><span class="sxs-lookup"><span data-stu-id="095f2-114">The decoder sets the post processing mode adaptively based on available CPU resources.</span></span> |
| <span data-ttu-id="095f2-115">0</span><span class="sxs-lookup"><span data-stu-id="095f2-115">0</span></span>     | <span data-ttu-id="095f2-116">Der Decoder führt keine nach Verarbeitung aus.</span><span class="sxs-lookup"><span data-stu-id="095f2-116">The decoder performs no post processing.</span></span>                                               |
| <span data-ttu-id="095f2-117">1</span><span class="sxs-lookup"><span data-stu-id="095f2-117">1</span></span>     | <span data-ttu-id="095f2-118">der-Decoder führt eine schnelle Blockierung aus.</span><span class="sxs-lookup"><span data-stu-id="095f2-118">fThe decoder performs fast deblocking.</span></span>                                                 |
| <span data-ttu-id="095f2-119">2</span><span class="sxs-lookup"><span data-stu-id="095f2-119">2</span></span>     | <span data-ttu-id="095f2-120">Der Decoder führt vollständige Blockierung aus.</span><span class="sxs-lookup"><span data-stu-id="095f2-120">The decoder performs full deblocking.</span></span>                                                  |
| <span data-ttu-id="095f2-121">3</span><span class="sxs-lookup"><span data-stu-id="095f2-121">3</span></span>     | <span data-ttu-id="095f2-122">Der Decoder führt eine schnelle Blockierung und einen deringing aus.</span><span class="sxs-lookup"><span data-stu-id="095f2-122">The decoder performs fast deblocking and deringing.</span></span>                                    |
| <span data-ttu-id="095f2-123">4</span><span class="sxs-lookup"><span data-stu-id="095f2-123">4</span></span>     | <span data-ttu-id="095f2-124">Der Decoder führt vollständige Blockierung und Aufhebung aus.</span><span class="sxs-lookup"><span data-stu-id="095f2-124">The decoder performs full deblocking and deringing.</span></span>                                    |



 

<span data-ttu-id="095f2-125">Da der Wert dieser Eigenschaft zwischen 0 und 4 liegt, erhöht sich die Decodierungs Komplexität, die Verwendung von CPU-Ressourcen und die Bildqualität.</span><span class="sxs-lookup"><span data-stu-id="095f2-125">As the value of this property goes from 0 to 4, the decoding complexity, use of CPU resources, and picture quality all increase.</span></span>

## <a name="requirements"></a><span data-ttu-id="095f2-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="095f2-126">Requirements</span></span>



| <span data-ttu-id="095f2-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="095f2-127">Requirement</span></span> | <span data-ttu-id="095f2-128">Wert</span><span class="sxs-lookup"><span data-stu-id="095f2-128">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="095f2-129">Client</span><span class="sxs-lookup"><span data-stu-id="095f2-129">Client</span></span><br/> | <span data-ttu-id="095f2-130">Windows Vista oder Windows 7</span><span class="sxs-lookup"><span data-stu-id="095f2-130">Windows Vista or Windows 7</span></span><br/>                                                   |
| <span data-ttu-id="095f2-131">Header</span><span class="sxs-lookup"><span data-stu-id="095f2-131">Header</span></span><br/> | <dl> <span data-ttu-id="095f2-132"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="095f2-132"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="095f2-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="095f2-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="095f2-134">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="095f2-134">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




