---
description: Die TSPI-Zeilen- \_ qosinfo-Nachricht bewirkt, dass TAPI ein QoS-Ereignis auslöst. Weitere Informationen finden Sie unter itqoabvent.
ms.assetid: b2844d12-c524-42ab-aeb9-8daf4e07a436
title: LINE_QOSINFO Meldung (TSPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d35ff19601ab6acd9a3d8e8aebf1e59b06a4f17e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106351354"
---
# <a name="line_qosinfo-message"></a><span data-ttu-id="0b194-104">Zeilen- \_ qosinfo-Meldung</span><span class="sxs-lookup"><span data-stu-id="0b194-104">LINE\_QOSINFO message</span></span>

<span data-ttu-id="0b194-105">Die TSPI- **Zeilen- \_ qosinfo** -Nachricht bewirkt, dass TAPI ein QoS-Ereignis auslöst.</span><span class="sxs-lookup"><span data-stu-id="0b194-105">The TSPI **LINE\_QOSINFO** message causes TAPI to fire a QOS event.</span></span> <span data-ttu-id="0b194-106">Weitere Informationen finden Sie unter [**itqoabvent**](/windows/win32/api/tapi3if/nn-tapi3if-itqosevent) .</span><span class="sxs-lookup"><span data-stu-id="0b194-106">See [**ITQOSEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itqosevent) for additional information.</span></span>


```C++
        
```



## <a name="parameters"></a><span data-ttu-id="0b194-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="0b194-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b194-108">*htline*</span><span class="sxs-lookup"><span data-stu-id="0b194-108">*htLine*</span></span> 
</dt> <dd>

<span data-ttu-id="0b194-109">Der TAPI-Handle für die Zeile.</span><span class="sxs-lookup"><span data-stu-id="0b194-109">The TAPI handle for the line.</span></span>

</dd> <dt>

<span data-ttu-id="0b194-110">*"htcall"*</span><span class="sxs-lookup"><span data-stu-id="0b194-110">*htCall*</span></span> 
</dt> <dd>

<span data-ttu-id="0b194-111">Der TAPI-Handle für den-Befehl.</span><span class="sxs-lookup"><span data-stu-id="0b194-111">The TAPI handle for the call.</span></span>

</dd> <dt>

<span data-ttu-id="0b194-112">*dwmsg*</span><span class="sxs-lookup"><span data-stu-id="0b194-112">*dwMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="0b194-113">Die Wert Zeile \_ qosinfo.</span><span class="sxs-lookup"><span data-stu-id="0b194-113">The value LINE\_QOSINFO.</span></span>

</dd> <dt>

<span data-ttu-id="0b194-114">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="0b194-114">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="0b194-115">Ein Member des [**QoS- \_ Ereignis**](/windows/win32/api/tapi3if/ne-tapi3if-qos_event) Enumerators, der den Ereignistyp identifiziert.</span><span class="sxs-lookup"><span data-stu-id="0b194-115">A member of the [**QOS\_EVENT**](/windows/win32/api/tapi3if/ne-tapi3if-qos_event) enumerator that identifies the type of event.</span></span>

</dd> <dt>

<span data-ttu-id="0b194-116">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="0b194-116">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="0b194-117">Eine [Medientyp](./tapiprotocol--constants.md) Konstante, die die Medien des diesem Ereignis zugeordneten Aufrufes angibt.</span><span class="sxs-lookup"><span data-stu-id="0b194-117">A [media type](./tapiprotocol--constants.md) constant that identifies the media of the call associated with this event.</span></span>

</dd> <dt>

<span data-ttu-id="0b194-118">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="0b194-118">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="0b194-119">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="0b194-119">Unused.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0b194-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0b194-120">Requirements</span></span>



| <span data-ttu-id="0b194-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0b194-121">Requirement</span></span> | <span data-ttu-id="0b194-122">Wert</span><span class="sxs-lookup"><span data-stu-id="0b194-122">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="0b194-123">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="0b194-123">TAPI version</span></span><br/> | <span data-ttu-id="0b194-124">Erfordert TAPI 2,2</span><span class="sxs-lookup"><span data-stu-id="0b194-124">Requires TAPI 2.2</span></span><br/>                                                      |
| <span data-ttu-id="0b194-125">Header</span><span class="sxs-lookup"><span data-stu-id="0b194-125">Header</span></span><br/>       | <dl> <span data-ttu-id="0b194-126"><dt>TSPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="0b194-126"><dt>Tspi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b194-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0b194-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b194-128">**QoS- \_ Ereignis**</span><span class="sxs-lookup"><span data-stu-id="0b194-128">**QOS\_EVENT**</span></span>](/windows/win32/api/tapi3if/ne-tapi3if-qos_event)
</dt> <dt>

[<span data-ttu-id="0b194-129">**Itqoabvent**</span><span class="sxs-lookup"><span data-stu-id="0b194-129">**ITQOSEvent**</span></span>](/windows/win32/api/tapi3if/nn-tapi3if-itqosevent)
</dt> </dl>

 

