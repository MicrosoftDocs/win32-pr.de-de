---
title: Windows-Ereignis Sammler Konstanten (evcoll. h)
description: Das Windows-Ereignis Sammler-SDK enthält die folgenden Konstanten.
ms.assetid: 2ba862f9-6849-43b3-8914-e18ede1d63c0
ms.tgt_platform: multiple
topic_type:
- apiref
api_name:
- EC_VARIANT_TYPE_MASK
- EC_VARIANT_TYPE_ARRAY
- EC_READ_ACCESS
- EC_WRITE_ACCESS
- EC_OPEN_ALWAYS
- EC_CREATE_NEW
- EC_OPEN_EXISTING
api_location:
- Evcoll.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf6e7e99186e2148bf6ec3400aadf760a79a2331
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739744"
---
# <a name="windows-event-collector-constants"></a><span data-ttu-id="50a87-103">Windows-Ereignis Sammler Konstanten</span><span class="sxs-lookup"><span data-stu-id="50a87-103">Windows Event Collector Constants</span></span>

<span data-ttu-id="50a87-104">Das Windows-Ereignis Sammler-SDK enthält die folgenden Konstanten.</span><span class="sxs-lookup"><span data-stu-id="50a87-104">The Windows Event Collector SDK contains the following constants.</span></span>

<dl> <dt>

<span data-ttu-id="50a87-105"><span id="EC_VARIANT_TYPE_MASK"></span><span id="ec_variant_type_mask"></span>**EC \_ Variant \_ Type \_ Mask**</span><span class="sxs-lookup"><span data-stu-id="50a87-105"><span id="EC_VARIANT_TYPE_MASK"></span><span id="ec_variant_type_mask"></span>**EC\_VARIANT\_TYPE\_MASK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50a87-106">0x7F</span><span class="sxs-lookup"><span data-stu-id="50a87-106">0x7f</span></span>
</dt> <dt>



<span data-ttu-id="50a87-107">Wird verwendet, um das arraybit aus der **Type** -Eigenschaft einer [**EC- \_ Variante**](/windows/desktop/api/Evcoll/ns-evcoll-ec_variant) zu maskieren, um den Typ des Variant-Werts zu extrahieren.</span><span class="sxs-lookup"><span data-stu-id="50a87-107">Used to mask out the array bit from the **Type** property of an [**EC\_VARIANT**](/windows/desktop/api/Evcoll/ns-evcoll-ec_variant) to extract the type of the variant value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="50a87-108"><span id="EC_VARIANT_TYPE_ARRAY"></span><span id="ec_variant_type_array"></span>**Type-Array der EC- \_ Variante \_ \_**</span><span class="sxs-lookup"><span data-stu-id="50a87-108"><span id="EC_VARIANT_TYPE_ARRAY"></span><span id="ec_variant_type_array"></span>**EC\_VARIANT\_TYPE\_ARRAY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50a87-109">128 (0x80)</span><span class="sxs-lookup"><span data-stu-id="50a87-109">128 (0x80)</span></span>
</dt> <dt>



<span data-ttu-id="50a87-110">Wenn dieses Bit in der **Type** -Eigenschaft einer EC- [**\_ Variante**](/windows/desktop/api/Evcoll/ns-evcoll-ec_variant)festgelegt wird, enthält die Variante einen Zeiger auf ein Array von Werten anstatt auf den Wert selbst.</span><span class="sxs-lookup"><span data-stu-id="50a87-110">When this bit is set in the **Type** property of an [**EC\_VARIANT**](/windows/desktop/api/Evcoll/ns-evcoll-ec_variant), the variant contains a pointer to an array of values, rather than the value itself.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="50a87-111"><span id="EC_READ_ACCESS"></span><span id="ec_read_access"></span>**EC- \_ Lese \_ Zugriff**</span><span class="sxs-lookup"><span data-stu-id="50a87-111"><span id="EC_READ_ACCESS"></span><span id="ec_read_access"></span>**EC\_READ\_ACCESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50a87-112">1</span><span class="sxs-lookup"><span data-stu-id="50a87-112">1</span></span>
</dt> <dt>



<span data-ttu-id="50a87-113">Lese Zugriffs Steuerungs Berechtigung, die das Lesen von Informationen aus dem Ereignis Sammler ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="50a87-113">Read access control permission that allows information to be read from the event collector.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="50a87-114"><span id="EC_WRITE_ACCESS"></span><span id="ec_write_access"></span>**EC- \_ Schreib \_ Zugriff**</span><span class="sxs-lookup"><span data-stu-id="50a87-114"><span id="EC_WRITE_ACCESS"></span><span id="ec_write_access"></span>**EC\_WRITE\_ACCESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50a87-115">2</span><span class="sxs-lookup"><span data-stu-id="50a87-115">2</span></span>
</dt> <dt>



<span data-ttu-id="50a87-116">Berechtigung zum Schreiben der Zugriffs Steuerung, die das Schreiben von Informationen in den Ereignis Sammler ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="50a87-116">Write access control permission that allows information to be written to the event collector.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="50a87-117"><span id="EC_OPEN_ALWAYS"></span><span id="ec_open_always"></span>**EC \_ \_ immer öffnen**</span><span class="sxs-lookup"><span data-stu-id="50a87-117"><span id="EC_OPEN_ALWAYS"></span><span id="ec_open_always"></span>**EC\_OPEN\_ALWAYS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50a87-118">0</span><span class="sxs-lookup"><span data-stu-id="50a87-118">0</span></span>
</dt> <dt>



<span data-ttu-id="50a87-119">Öffnet ein vorhandenes Abonnement oder erstellt das Abonnement, wenn es nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="50a87-119">Opens an existing subscription or creates the subscription if it does not exist.</span></span> <span data-ttu-id="50a87-120">Wird von der [**ecopenabonnementmethode**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription) verwendet.</span><span class="sxs-lookup"><span data-stu-id="50a87-120">Used by the [**EcOpenSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription) method.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="50a87-121"><span id="EC_CREATE_NEW"></span><span id="ec_create_new"></span>**EC \_ Create \_ New**</span><span class="sxs-lookup"><span data-stu-id="50a87-121"><span id="EC_CREATE_NEW"></span><span id="ec_create_new"></span>**EC\_CREATE\_NEW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50a87-122">1</span><span class="sxs-lookup"><span data-stu-id="50a87-122">1</span></span>
</dt> <dt>



<span data-ttu-id="50a87-123">Ein Flag, das an die Funktion [**ecopenabonnement**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription) übermittelt wird und angibt, dass ein neues Abonnement erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="50a87-123">A flag passed to the [**EcOpenSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription) function specifying that a new subscription should be created.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="50a87-124"><span id="EC_OPEN_EXISTING"></span><span id="ec_open_existing"></span>**EC \_ Open \_ vorhanden**</span><span class="sxs-lookup"><span data-stu-id="50a87-124"><span id="EC_OPEN_EXISTING"></span><span id="ec_open_existing"></span>**EC\_OPEN\_EXISTING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50a87-125">2</span><span class="sxs-lookup"><span data-stu-id="50a87-125">2</span></span>
</dt> <dt>



<span data-ttu-id="50a87-126">Ein Flag, das an die Funktion [**ecopenabonnement**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription) übermittelt wird und angibt, dass ein vorhandenes Abonnement geöffnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="50a87-126">A flag passed to the [**EcOpenSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription) function specifying that an existing subscription should be opened.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="50a87-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="50a87-127">Requirements</span></span>



| <span data-ttu-id="50a87-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="50a87-128">Requirement</span></span> | <span data-ttu-id="50a87-129">Wert</span><span class="sxs-lookup"><span data-stu-id="50a87-129">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="50a87-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="50a87-130">Minimum supported client</span></span><br/> | <span data-ttu-id="50a87-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="50a87-131">Windows Vista</span></span><br/>                                                            |
| <span data-ttu-id="50a87-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="50a87-132">Minimum supported server</span></span><br/> | <span data-ttu-id="50a87-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="50a87-133">Windows Server 2008</span></span><br/>                                                      |
| <span data-ttu-id="50a87-134">Header</span><span class="sxs-lookup"><span data-stu-id="50a87-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="50a87-135"><dt>Evcoll. h</dt></span><span class="sxs-lookup"><span data-stu-id="50a87-135"><dt>Evcoll.h</dt></span></span> </dl> |



 

 





