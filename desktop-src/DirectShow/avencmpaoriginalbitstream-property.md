---
description: Gibt die Standardeinstellung für das ursprüngliche Bit im MPEG-1-Audiodatenstrom an. Diese Eigenschaft gilt für MPEG-Audioencoder.
ms.assetid: 62b56868-684f-4f28-90da-dac19cb07946
title: Avencmteioriginalbitstream-Eigenschaft (codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a1a49fda5bb605ac8735ebac4be758e7f73efb9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103860381"
---
# <a name="avencmpaoriginalbitstream-property"></a><span data-ttu-id="25677-104">Avencmteioriginalbitstream (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="25677-104">AVEncMPAOriginalBitstream property</span></span>

<span data-ttu-id="25677-105">Gibt die Standardeinstellung für das ursprüngliche Bit im MPEG-1-Audiodatenstrom an.</span><span class="sxs-lookup"><span data-stu-id="25677-105">Specifies the default setting for the original bit in the MPEG-1 audio stream.</span></span> <span data-ttu-id="25677-106">Diese Eigenschaft gilt für MPEG-Audioencoder.</span><span class="sxs-lookup"><span data-stu-id="25677-106">This property applies to MPEG audio encoders.</span></span>

<span data-ttu-id="25677-107">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="25677-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="25677-108">Datentyp</span><span class="sxs-lookup"><span data-stu-id="25677-108">Data type</span></span>

<span data-ttu-id="25677-109">**Variant \_ bool** (**VT \_ bool**)</span><span class="sxs-lookup"><span data-stu-id="25677-109">**VARIANT\_BOOL** (**VT\_BOOL**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="25677-110">Eigenschaften-GUID</span><span class="sxs-lookup"><span data-stu-id="25677-110">Property GUID</span></span>

<span data-ttu-id="25677-111">**Codecapi \_ avencmporiginalbitstream**</span><span class="sxs-lookup"><span data-stu-id="25677-111">**CODECAPI\_AVEncMPAOriginalBitstream**</span></span>

## <a name="property-value"></a><span data-ttu-id="25677-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="25677-112">Property value</span></span>

<span data-ttu-id="25677-113">Diese Eigenschaft kann die folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="25677-113">This property can have the following values.</span></span>



| <span data-ttu-id="25677-114">Wert</span><span class="sxs-lookup"><span data-stu-id="25677-114">Value</span></span>          | <span data-ttu-id="25677-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="25677-115">Description</span></span>          |
|----------------|----------------------|
| <span data-ttu-id="25677-116">Variant \_ false</span><span class="sxs-lookup"><span data-stu-id="25677-116">VARIANT\_FALSE</span></span> | <span data-ttu-id="25677-117">Ursprüngliches Bit ist off.</span><span class="sxs-lookup"><span data-stu-id="25677-117">Original bit is off.</span></span> |
| <span data-ttu-id="25677-118">Variant \_ true</span><span class="sxs-lookup"><span data-stu-id="25677-118">VARIANT\_TRUE</span></span>  | <span data-ttu-id="25677-119">Ursprüngliches Bit ist on.</span><span class="sxs-lookup"><span data-stu-id="25677-119">Original bit is on.</span></span>  |



 

## <a name="remarks"></a><span data-ttu-id="25677-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="25677-120">Remarks</span></span>

<span data-ttu-id="25677-121">Der Encoder kann diese Einstellung basierend auf dem Inhalt des Eingabestreams überschreiben.</span><span class="sxs-lookup"><span data-stu-id="25677-121">The encoder might override this setting, based on the contents of the input stream.</span></span>

## <a name="requirements"></a><span data-ttu-id="25677-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="25677-122">Requirements</span></span>



| <span data-ttu-id="25677-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="25677-123">Requirement</span></span> | <span data-ttu-id="25677-124">Wert</span><span class="sxs-lookup"><span data-stu-id="25677-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="25677-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="25677-125">Minimum supported client</span></span><br/> | <span data-ttu-id="25677-126">Windows 2000 Professional \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="25677-126">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="25677-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="25677-127">Minimum supported server</span></span><br/> | <span data-ttu-id="25677-128">Windows 2000 Server \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="25677-128">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="25677-129">Header</span><span class="sxs-lookup"><span data-stu-id="25677-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="25677-130"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="25677-130"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25677-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="25677-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25677-132">Eigenschaften der Codec-API</span><span class="sxs-lookup"><span data-stu-id="25677-132">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="25677-133">**Icodecapi-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="25677-133">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




