---
description: Gibt an, ob dem Frame Header eine zyklische Redundanz Überprüfung (CRC) hinzugefügt werden soll. Diese Eigenschaft gilt für MPEG-Audioencoder.
ms.assetid: 55f0de8b-26dd-4d48-b7ed-2ddcef630227
title: Avencmpenableredundancyprotection-Eigenschaft (codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2028b5adaad55d46cc53c61f9d65a73819cc899
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106339664"
---
# <a name="avencmpaenableredundancyprotection-property"></a><span data-ttu-id="44e7a-104">Avencmpfenableredundancyprotection (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="44e7a-104">AVEncMPAEnableRedundancyProtection property</span></span>

<span data-ttu-id="44e7a-105">Gibt an, ob dem Frame Header eine zyklische Redundanz Überprüfung (CRC) hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="44e7a-105">Specifies whether to add a cyclic redundancy check (CRC) to the frame header.</span></span> <span data-ttu-id="44e7a-106">Diese Eigenschaft gilt für MPEG-Audioencoder.</span><span class="sxs-lookup"><span data-stu-id="44e7a-106">This property applies to MPEG audio encoders.</span></span>

<span data-ttu-id="44e7a-107">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="44e7a-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="44e7a-108">Datentyp</span><span class="sxs-lookup"><span data-stu-id="44e7a-108">Data type</span></span>

<span data-ttu-id="44e7a-109">**Variant \_ bool** (**VT \_ bool**)</span><span class="sxs-lookup"><span data-stu-id="44e7a-109">**VARIANT\_BOOL** (**VT\_BOOL**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="44e7a-110">Eigenschaften-GUID</span><span class="sxs-lookup"><span data-stu-id="44e7a-110">Property GUID</span></span>

<span data-ttu-id="44e7a-111">**Codecapi \_ avencmpenableredundancyprotection**</span><span class="sxs-lookup"><span data-stu-id="44e7a-111">**CODECAPI\_AVEncMPAEnableRedundancyProtection**</span></span>

## <a name="property-value"></a><span data-ttu-id="44e7a-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="44e7a-112">Property value</span></span>

<span data-ttu-id="44e7a-113">Diese Eigenschaft kann die folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="44e7a-113">This property can have the following values.</span></span>



| <span data-ttu-id="44e7a-114">Wert</span><span class="sxs-lookup"><span data-stu-id="44e7a-114">Value</span></span>          | <span data-ttu-id="44e7a-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="44e7a-115">Description</span></span>                |
|----------------|----------------------------|
| <span data-ttu-id="44e7a-116">Variant \_ false</span><span class="sxs-lookup"><span data-stu-id="44e7a-116">VARIANT\_FALSE</span></span> | <span data-ttu-id="44e7a-117">Fügen Sie keine CRC-Prüfsumme hinzu.</span><span class="sxs-lookup"><span data-stu-id="44e7a-117">Do not add a CRC checksum.</span></span> |
| <span data-ttu-id="44e7a-118">Variant \_ true</span><span class="sxs-lookup"><span data-stu-id="44e7a-118">VARIANT\_TRUE</span></span>  | <span data-ttu-id="44e7a-119">Fügen Sie eine CRC-Prüfsumme hinzu.</span><span class="sxs-lookup"><span data-stu-id="44e7a-119">Add a CRC checksum.</span></span>        |



 

## <a name="requirements"></a><span data-ttu-id="44e7a-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="44e7a-120">Requirements</span></span>



| <span data-ttu-id="44e7a-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="44e7a-121">Requirement</span></span> | <span data-ttu-id="44e7a-122">Wert</span><span class="sxs-lookup"><span data-stu-id="44e7a-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="44e7a-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="44e7a-123">Minimum supported client</span></span><br/> | <span data-ttu-id="44e7a-124">Windows 2000 Professional \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="44e7a-124">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="44e7a-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="44e7a-125">Minimum supported server</span></span><br/> | <span data-ttu-id="44e7a-126">Windows 2000 Server \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="44e7a-126">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="44e7a-127">Header</span><span class="sxs-lookup"><span data-stu-id="44e7a-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="44e7a-128"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="44e7a-128"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44e7a-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="44e7a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44e7a-130">Eigenschaften der Codec-API</span><span class="sxs-lookup"><span data-stu-id="44e7a-130">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="44e7a-131">**Icodecapi-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="44e7a-131">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




