---
description: Gibt an, ob ein AAC-Decoder standardmäßige MPEG-2/MPEG-4-Stereo Abmischungs Gleichungen verwendet oder eine nicht standardmäßige downmischungs-verwendet.
ms.assetid: a384d24e-07e2-45e7-84b8-e791feb64a83
title: Avdecaacdownmixmode-Eigenschaft (codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 388d1437dfe396d5072ef09082c4ad17ddb75953
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106340088"
---
# <a name="avdecaacdownmixmode-property"></a><span data-ttu-id="ca127-103">Avdecaacdownmixmode (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="ca127-103">AVDecAACDownmixMode property</span></span>

<span data-ttu-id="ca127-104">Gibt an, ob ein AAC-Decoder standardmäßige MPEG-2/MPEG-4-Stereo Abmischungs Gleichungen verwendet oder eine nicht standardmäßige downmischungs-verwendet.</span><span class="sxs-lookup"><span data-stu-id="ca127-104">Specifies whether an AAC decoder uses standard MPEG-2/MPEG-4 stereo downmix equations, or uses a non-standard downmix.</span></span>

<span data-ttu-id="ca127-105">Ein Beispiel für eine nicht standardmäßige Downmix ist die, die durch das ARIB-Dokument Std-B21 Version 4,4 definiert wird.</span><span class="sxs-lookup"><span data-stu-id="ca127-105">An example of a non-standard downmix is the one defined by ARIB document STD-B21 version 4.4.</span></span>

<span data-ttu-id="ca127-106">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="ca127-106">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="ca127-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="ca127-107">Data type</span></span>

<span data-ttu-id="ca127-108">**UInt32** (**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="ca127-108">**UINT32** (**VT\_UI4**</span></span>

## <a name="property-guid"></a><span data-ttu-id="ca127-109">Eigenschaften-GUID</span><span class="sxs-lookup"><span data-stu-id="ca127-109">Property GUID</span></span>

<span data-ttu-id="ca127-110">**Codecapi \_ avdecaacdownmixmode**</span><span class="sxs-lookup"><span data-stu-id="ca127-110">**CODECAPI\_AVDecAACDownmixMode**</span></span>

## <a name="property-value"></a><span data-ttu-id="ca127-111">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="ca127-111">Property value</span></span>

<span data-ttu-id="ca127-112">Der Wert dieser Eigenschaft ist ein Member der [**eavdecaacdownmixmode**](/windows/win32/api/codecapi/ne-codecapi-eavdecaacdownmixmode) -Enumeration.</span><span class="sxs-lookup"><span data-stu-id="ca127-112">The value of this property is a member of the [**eAVDecAACDownmixMode**](/windows/win32/api/codecapi/ne-codecapi-eavdecaacdownmixmode) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca127-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ca127-113">Requirements</span></span>



| <span data-ttu-id="ca127-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ca127-114">Requirement</span></span> | <span data-ttu-id="ca127-115">Wert</span><span class="sxs-lookup"><span data-stu-id="ca127-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ca127-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ca127-116">Minimum supported client</span></span><br/> | <span data-ttu-id="ca127-117">Windows 2000 Professional \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="ca127-117">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="ca127-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ca127-118">Minimum supported server</span></span><br/> | <span data-ttu-id="ca127-119">Windows 2000 Server \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="ca127-119">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="ca127-120">Header</span><span class="sxs-lookup"><span data-stu-id="ca127-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="ca127-121"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="ca127-121"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca127-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ca127-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca127-123">Eigenschaften der Codec-API</span><span class="sxs-lookup"><span data-stu-id="ca127-123">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="ca127-124">**Icodecapi-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="ca127-124">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

