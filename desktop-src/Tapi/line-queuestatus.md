---
description: Die Zeile \_ QueueStatus-Nachricht wird gesendet, wenn sich der Status einer ACD in der Warteschlange auf einem Agent-Handler ändert, für den die Anwendung zurzeit über eine geöffnete Zeile verfügt. Diese Meldung wird mithilfe der lineproxymess-Funktion generiert.
ms.assetid: 9baacfc5-f26c-41c7-a1f8-f48ec8aa844c
title: LINE_QUEUESTATUS Meldung (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a89785b92009a7531ae693545febaf153cf19bb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368457"
---
# <a name="line_queuestatus-message"></a><span data-ttu-id="3d3dd-104">Zeile \_ QueueStatus-Meldung</span><span class="sxs-lookup"><span data-stu-id="3d3dd-104">LINE\_QUEUESTATUS message</span></span>

<span data-ttu-id="3d3dd-105">Die **Zeile \_ QueueStatus** -Nachricht wird gesendet, wenn sich der Status einer ACD in der Warteschlange auf einem Agent-Handler ändert, für den die Anwendung zurzeit über eine geöffnete Zeile verfügt.</span><span class="sxs-lookup"><span data-stu-id="3d3dd-105">The **LINE\_QUEUESTATUS** message is sent when the status of an ACD queue changes on an agent handler for which the application currently has an open line.</span></span> <span data-ttu-id="3d3dd-106">Diese Meldung wird mithilfe der [**lineproxymess**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage) -Funktion generiert.</span><span class="sxs-lookup"><span data-stu-id="3d3dd-106">This message is generated using the [**lineProxyMessage**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage) function.</span></span>


```C++
        
```



## <a name="parameters"></a><span data-ttu-id="3d3dd-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="3d3dd-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d3dd-108">*dwdevice*</span><span class="sxs-lookup"><span data-stu-id="3d3dd-108">*dwDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="3d3dd-109">Das Handle der Anwendung für das liniengerät.</span><span class="sxs-lookup"><span data-stu-id="3d3dd-109">The application's handle to the line device.</span></span> <span data-ttu-id="3d3dd-110">Dies bezieht sich auf den-Agent-Handler.</span><span class="sxs-lookup"><span data-stu-id="3d3dd-110">This relates to the agent handler.</span></span>

</dd> <dt>

<span data-ttu-id="3d3dd-111">*dwcallbackinstance*</span><span class="sxs-lookup"><span data-stu-id="3d3dd-111">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="3d3dd-112">Die beim Öffnen der Zeile angegebene Rückruf Instanz.</span><span class="sxs-lookup"><span data-stu-id="3d3dd-112">The callback instance supplied when opening the line.</span></span>

</dd> <dt>

<span data-ttu-id="3d3dd-113">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="3d3dd-113">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="3d3dd-114">Der Bezeichner der Warteschlange, deren Status sich geändert hat.</span><span class="sxs-lookup"><span data-stu-id="3d3dd-114">The identifier of the queue whose status has changed.</span></span>

</dd> <dt>

<span data-ttu-id="3d3dd-115">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="3d3dd-115">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="3d3dd-116">Gibt den Status der Warteschlange an, der geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="3d3dd-116">Specifies the queue status that has changed.</span></span> <span data-ttu-id="3d3dd-117">Kann eine oder mehrere der [**linequeuestatus- \_ Konstanten**](linequeuestatus--constants.md)sein.</span><span class="sxs-lookup"><span data-stu-id="3d3dd-117">Can be one or more of the [**LINEQUEUESTATUS\_ constants**](linequeuestatus--constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="3d3dd-118">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="3d3dd-118">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="3d3dd-119">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="3d3dd-119">Reserved.</span></span> <span data-ttu-id="3d3dd-120">Auf NULL festlegen.</span><span class="sxs-lookup"><span data-stu-id="3d3dd-120">Set to zero.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3d3dd-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3d3dd-121">Requirements</span></span>



| <span data-ttu-id="3d3dd-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3d3dd-122">Requirement</span></span> | <span data-ttu-id="3d3dd-123">Wert</span><span class="sxs-lookup"><span data-stu-id="3d3dd-123">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="3d3dd-124">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="3d3dd-124">TAPI version</span></span><br/> | <span data-ttu-id="3d3dd-125">Erfordert TAPI 2,2</span><span class="sxs-lookup"><span data-stu-id="3d3dd-125">Requires TAPI 2.2</span></span><br/>                                                      |
| <span data-ttu-id="3d3dd-126">Header</span><span class="sxs-lookup"><span data-stu-id="3d3dd-126">Header</span></span><br/>       | <dl> <span data-ttu-id="3d3dd-127"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="3d3dd-127"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d3dd-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3d3dd-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d3dd-129">**lineproxymess**</span><span class="sxs-lookup"><span data-stu-id="3d3dd-129">**lineProxyMessage**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage)
</dt> </dl>

 

 




