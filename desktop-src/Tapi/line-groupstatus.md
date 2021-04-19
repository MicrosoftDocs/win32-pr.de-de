---
description: Die Meldung "line \_ groupstatus" wird gesendet, wenn sich der Status einer ACD-Gruppe in einem Agent-Handler ändert, für den die Anwendung zurzeit über eine geöffnete Zeile verfügt. Diese Meldung wird mithilfe der lineproxymess-Funktion generiert.
ms.assetid: 1f3210fe-a7c8-4cfa-8e36-3a88e93d68bb
title: LINE_GROUPSTATUS Meldung (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22fec7c4701ee7140c02cede1901ef7998e5b60d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360409"
---
# <a name="line_groupstatus-message"></a><span data-ttu-id="b76d9-104">Zeilen \_ Gruppenstatus-Meldung</span><span class="sxs-lookup"><span data-stu-id="b76d9-104">LINE\_GROUPSTATUS message</span></span>

<span data-ttu-id="b76d9-105">Die Meldung " **line \_ groupstatus** " wird gesendet, wenn sich der Status einer ACD-Gruppe in einem Agent-Handler ändert, für den die Anwendung zurzeit über eine geöffnete Zeile verfügt.</span><span class="sxs-lookup"><span data-stu-id="b76d9-105">The **LINE\_GROUPSTATUS** message is sent when the status of an ACD group changes on an agent handler for which the application currently has an open line.</span></span> <span data-ttu-id="b76d9-106">Diese Meldung wird mithilfe der [**lineproxymess**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage) -Funktion generiert.</span><span class="sxs-lookup"><span data-stu-id="b76d9-106">This message is generated using the [**lineProxyMessage**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage) function.</span></span>


```C++
        
```



## <a name="parameters"></a><span data-ttu-id="b76d9-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="b76d9-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b76d9-108">*dwdevice*</span><span class="sxs-lookup"><span data-stu-id="b76d9-108">*dwDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="b76d9-109">Das Handle der Anwendung für das liniengerät.</span><span class="sxs-lookup"><span data-stu-id="b76d9-109">The application's handle to the line device.</span></span> <span data-ttu-id="b76d9-110">Dies bezieht sich auf den-Agent-Handler.</span><span class="sxs-lookup"><span data-stu-id="b76d9-110">This relates to the agent handler.</span></span>

</dd> <dt>

<span data-ttu-id="b76d9-111">*dwcallbackinstance*</span><span class="sxs-lookup"><span data-stu-id="b76d9-111">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="b76d9-112">Die beim Öffnen der Zeile angegebene Rückruf Instanz.</span><span class="sxs-lookup"><span data-stu-id="b76d9-112">The callback instance supplied when opening the line.</span></span>

</dd> <dt>

<span data-ttu-id="b76d9-113">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="b76d9-113">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="b76d9-114">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="b76d9-114">Reserved.</span></span> <span data-ttu-id="b76d9-115">Auf NULL festlegen.</span><span class="sxs-lookup"><span data-stu-id="b76d9-115">Set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="b76d9-116">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="b76d9-116">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="b76d9-117">Gibt den Gruppenstatus an, der geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="b76d9-117">Specifies the group status that has changed.</span></span> <span data-ttu-id="b76d9-118">Die Anwendung kann [**linegetgrouplist**](/windows/desktop/api/Tapi/nf-tapi-linegetgrouplista) aufrufen, um die Änderungen in verfügbaren Gruppen zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="b76d9-118">The application can invoke [**lineGetGroupList**](/windows/desktop/api/Tapi/nf-tapi-linegetgrouplista) to determine the changes in available groups.</span></span> <span data-ttu-id="b76d9-119">Der *dwParam2* -Parameter ist eine oder mehrere der [**linegroupstatus- \_ Konstanten**](linegroupstatus--constants.md).</span><span class="sxs-lookup"><span data-stu-id="b76d9-119">The *dwParam2* parameter is one or more of the [**LINEGROUPSTATUS\_ constants**](linegroupstatus--constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="b76d9-120">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="b76d9-120">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="b76d9-121">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="b76d9-121">Reserved.</span></span> <span data-ttu-id="b76d9-122">Auf NULL festlegen.</span><span class="sxs-lookup"><span data-stu-id="b76d9-122">Set to zero.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b76d9-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b76d9-123">Requirements</span></span>



| <span data-ttu-id="b76d9-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b76d9-124">Requirement</span></span> | <span data-ttu-id="b76d9-125">Wert</span><span class="sxs-lookup"><span data-stu-id="b76d9-125">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="b76d9-126">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="b76d9-126">TAPI version</span></span><br/> | <span data-ttu-id="b76d9-127">Erfordert TAPI 2,2</span><span class="sxs-lookup"><span data-stu-id="b76d9-127">Requires TAPI 2.2</span></span><br/>                                                      |
| <span data-ttu-id="b76d9-128">Header</span><span class="sxs-lookup"><span data-stu-id="b76d9-128">Header</span></span><br/>       | <dl> <span data-ttu-id="b76d9-129"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="b76d9-129"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b76d9-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b76d9-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b76d9-131">**linegetgrouplist**</span><span class="sxs-lookup"><span data-stu-id="b76d9-131">**lineGetGroupList**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetgrouplista)
</dt> </dl>

 

 




