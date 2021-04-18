---
description: Die TAPI-Linien- \_ devspecificex-Nachricht wird gesendet, um die Anwendung über gerätespezifische Ereignisse zu benachrichtigen, die in einer Zeile, Adresse oder einem Rückruf auftreten. Die Bedeutung der Nachricht und die Interpretation der Parameter sind gerätespezifisch.
ms.assetid: 137e91fd-a09e-430c-9d46-8e5be65f03d1
title: LINE_DEVSPECIFICEX Meldung (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba25047858c641ea4c6cec7d15ba06df24e8ee39
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360932"
---
# <a name="line_devspecificex-message"></a><span data-ttu-id="fad58-104">Zeilen- \_ devspecificex-Meldung</span><span class="sxs-lookup"><span data-stu-id="fad58-104">LINE\_DEVSPECIFICEX message</span></span>

<span data-ttu-id="fad58-105">Die TAPI- **Linien- \_ devspecificex** -Nachricht wird gesendet, um die Anwendung über gerätespezifische Ereignisse zu benachrichtigen, die in einer Zeile, Adresse oder einem Rückruf auftreten.</span><span class="sxs-lookup"><span data-stu-id="fad58-105">The TAPI **LINE\_DEVSPECIFICEX** message is sent to notify the application about device-specific events occurring on a line, address, or call.</span></span> <span data-ttu-id="fad58-106">Die Bedeutung der Nachricht und die Interpretation der Parameter sind gerätespezifisch.</span><span class="sxs-lookup"><span data-stu-id="fad58-106">The meaning of the message and the interpretation of the parameters are device specific.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="fad58-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="fad58-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fad58-108">*hdevice*</span><span class="sxs-lookup"><span data-stu-id="fad58-108">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="fad58-109">Ein Handle für ein Zeilen Gerät oder einen-Befehl.</span><span class="sxs-lookup"><span data-stu-id="fad58-109">A handle to either a line device or call.</span></span> <span data-ttu-id="fad58-110">Dieser Parameter ist gerätespezifisch.</span><span class="sxs-lookup"><span data-stu-id="fad58-110">This parameter is device specific.</span></span>

</dd> <dt>

<span data-ttu-id="fad58-111">*dwcallbackinstance*</span><span class="sxs-lookup"><span data-stu-id="fad58-111">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="fad58-112">Die beim Öffnen der Zeile angegebene Rückruf Instanz.</span><span class="sxs-lookup"><span data-stu-id="fad58-112">The callback instance supplied when opening the line.</span></span>

</dd> <dt>

<span data-ttu-id="fad58-113">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="fad58-113">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="fad58-114">Gerätespezifisch.</span><span class="sxs-lookup"><span data-stu-id="fad58-114">Device specific.</span></span>

</dd> <dt>

<span data-ttu-id="fad58-115">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="fad58-115">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="fad58-116">Gerätespezifisch.</span><span class="sxs-lookup"><span data-stu-id="fad58-116">Device specific.</span></span>

</dd> <dt>

<span data-ttu-id="fad58-117">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="fad58-117">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="fad58-118">Gerätespezifisch.</span><span class="sxs-lookup"><span data-stu-id="fad58-118">Device specific.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fad58-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fad58-119">Return value</span></span>

<span data-ttu-id="fad58-120">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="fad58-120">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fad58-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fad58-121">Remarks</span></span>

<span data-ttu-id="fad58-122">Die **Zeile \_ devspecificex** -Meldung wird von einem Dienstanbieter in Verbindung mit der [**linedevspecific**](/windows/desktop/api/Tapi/nf-tapi-linedevspecific) -Funktion verwendet.</span><span class="sxs-lookup"><span data-stu-id="fad58-122">The **LINE\_DEVSPECIFICEX** message is used by a service provider in conjunction with the [**lineDevSpecific**](/windows/desktop/api/Tapi/nf-tapi-linedevspecific) function.</span></span> <span data-ttu-id="fad58-123">Seine Bedeutung ist gerätespezifisch.</span><span class="sxs-lookup"><span data-stu-id="fad58-123">Its meaning is device specific.</span></span>

## <a name="requirements"></a><span data-ttu-id="fad58-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fad58-124">Requirements</span></span>



| <span data-ttu-id="fad58-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fad58-125">Requirement</span></span> | <span data-ttu-id="fad58-126">Wert</span><span class="sxs-lookup"><span data-stu-id="fad58-126">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="fad58-127">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="fad58-127">TAPI version</span></span><br/> | <span data-ttu-id="fad58-128">Erfordert TAPI 2,2</span><span class="sxs-lookup"><span data-stu-id="fad58-128">Requires TAPI 2.2</span></span><br/>                                                      |
| <span data-ttu-id="fad58-129">Header</span><span class="sxs-lookup"><span data-stu-id="fad58-129">Header</span></span><br/>       | <dl> <span data-ttu-id="fad58-130"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="fad58-130"><dt>Tapi.h</dt></span></span> </dl> |



 

 




