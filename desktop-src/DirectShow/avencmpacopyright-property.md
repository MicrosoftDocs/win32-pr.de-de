---
description: Gibt die Standardeinstellung für das Copyright-Bit im MPEG-1-Audiodatenstrom an. Diese Eigenschaft gilt für MPEG-Audioencoder.
ms.assetid: 6029c96f-b1dd-402f-9bac-9021bd897ee4
title: Avencmpacopyright-Eigenschaft (codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4449c41448d59ce673e667be7400d4a713236dd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392758"
---
# <a name="avencmpacopyright-property"></a><span data-ttu-id="b34ea-104">Avencmpacopyright (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="b34ea-104">AVEncMPACopyright property</span></span>

<span data-ttu-id="b34ea-105">Gibt die Standardeinstellung für das Copyright-Bit im MPEG-1-Audiodatenstrom an.</span><span class="sxs-lookup"><span data-stu-id="b34ea-105">Specifies the default setting for the copyright bit in the MPEG-1 audio stream.</span></span> <span data-ttu-id="b34ea-106">Diese Eigenschaft gilt für MPEG-Audioencoder.</span><span class="sxs-lookup"><span data-stu-id="b34ea-106">This property applies to MPEG audio encoders.</span></span>

<span data-ttu-id="b34ea-107">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="b34ea-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="b34ea-108">Datentyp</span><span class="sxs-lookup"><span data-stu-id="b34ea-108">Data type</span></span>

<span data-ttu-id="b34ea-109">**Variant \_ bool** (**VT \_ bool**)</span><span class="sxs-lookup"><span data-stu-id="b34ea-109">**VARIANT\_BOOL** (**VT\_BOOL**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="b34ea-110">Eigenschaften-GUID</span><span class="sxs-lookup"><span data-stu-id="b34ea-110">Property GUID</span></span>

<span data-ttu-id="b34ea-111">**Codecapi \_ avencmpacopyright**</span><span class="sxs-lookup"><span data-stu-id="b34ea-111">**CODECAPI\_AVEncMPACopyright**</span></span>

## <a name="property-value"></a><span data-ttu-id="b34ea-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="b34ea-112">Property value</span></span>

<span data-ttu-id="b34ea-113">Diese Eigenschaft kann die folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="b34ea-113">This property can have the following values.</span></span>



| <span data-ttu-id="b34ea-114">Wert</span><span class="sxs-lookup"><span data-stu-id="b34ea-114">Value</span></span>          | <span data-ttu-id="b34ea-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b34ea-115">Description</span></span>           |
|----------------|-----------------------|
| <span data-ttu-id="b34ea-116">Variant \_ false</span><span class="sxs-lookup"><span data-stu-id="b34ea-116">VARIANT\_FALSE</span></span> | <span data-ttu-id="b34ea-117">Copyright-Bit ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="b34ea-117">Copyright bit is off.</span></span> |
| <span data-ttu-id="b34ea-118">Variant \_ true</span><span class="sxs-lookup"><span data-stu-id="b34ea-118">VARIANT\_TRUE</span></span>  | <span data-ttu-id="b34ea-119">Copyright-Bit ist on.</span><span class="sxs-lookup"><span data-stu-id="b34ea-119">Copyright bit is on.</span></span>  |



 

## <a name="remarks"></a><span data-ttu-id="b34ea-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b34ea-120">Remarks</span></span>

<span data-ttu-id="b34ea-121">Der Encoder kann diese Einstellung basierend auf dem Inhalt des Eingabestreams überschreiben.</span><span class="sxs-lookup"><span data-stu-id="b34ea-121">The encoder might override this setting, based on the contents of the input stream.</span></span>

## <a name="requirements"></a><span data-ttu-id="b34ea-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b34ea-122">Requirements</span></span>



| <span data-ttu-id="b34ea-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b34ea-123">Requirement</span></span> | <span data-ttu-id="b34ea-124">Wert</span><span class="sxs-lookup"><span data-stu-id="b34ea-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b34ea-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b34ea-125">Minimum supported client</span></span><br/> | <span data-ttu-id="b34ea-126">Windows 2000 Professional \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="b34ea-126">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="b34ea-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b34ea-127">Minimum supported server</span></span><br/> | <span data-ttu-id="b34ea-128">Windows 2000 Server \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="b34ea-128">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="b34ea-129">Header</span><span class="sxs-lookup"><span data-stu-id="b34ea-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="b34ea-130"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="b34ea-130"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b34ea-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b34ea-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b34ea-132">Eigenschaften der Codec-API</span><span class="sxs-lookup"><span data-stu-id="b34ea-132">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="b34ea-133">**Icodecapi-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="b34ea-133">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




