---
description: Die Richtlinien \_ -DevSpecific-Nachricht wird gesendet, um die Anwendung über gerätespezifische Ereignisse zu benachrichtigen, die in einer Zeile, Adresse oder einem Rückruf auftreten. Die Bedeutung der Nachricht und die Interpretation der Parameter sind gerätespezifisch.
ms.assetid: 6a58e77b-6ee2-4d2d-aca2-71b239f6a1dc
title: LINE_DEVSPECIFIC Meldung (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91907b10c0176258648fa165bbeb922a61a402ed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359671"
---
# <a name="line_devspecific-message"></a><span data-ttu-id="4c50d-104">Zeilen- \_ DevSpecific-Nachricht</span><span class="sxs-lookup"><span data-stu-id="4c50d-104">LINE\_DEVSPECIFIC message</span></span>

<span data-ttu-id="4c50d-105">Die Richt **Linien- \_ DevSpecific** -Nachricht wird gesendet, um die Anwendung über gerätespezifische Ereignisse zu benachrichtigen, die in einer Zeile, Adresse oder einem Rückruf auftreten.</span><span class="sxs-lookup"><span data-stu-id="4c50d-105">The TAPI **LINE\_DEVSPECIFIC** message is sent to notify the application about device-specific events occurring on a line, address, or call.</span></span> <span data-ttu-id="4c50d-106">Die Bedeutung der Nachricht und die Interpretation der Parameter sind gerätespezifisch.</span><span class="sxs-lookup"><span data-stu-id="4c50d-106">The meaning of the message and the interpretation of the parameters are device specific.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="4c50d-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="4c50d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c50d-108">*hdevice*</span><span class="sxs-lookup"><span data-stu-id="4c50d-108">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="4c50d-109">Ein Handle für ein Zeilen Gerät oder einen-Befehl.</span><span class="sxs-lookup"><span data-stu-id="4c50d-109">A handle to either a line device or call.</span></span> <span data-ttu-id="4c50d-110">Dies ist gerätespezifisch.</span><span class="sxs-lookup"><span data-stu-id="4c50d-110">This is device specific.</span></span>

</dd> <dt>

<span data-ttu-id="4c50d-111">*dwcallbackinstance*</span><span class="sxs-lookup"><span data-stu-id="4c50d-111">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="4c50d-112">Die beim Öffnen der Zeile angegebene Rückruf Instanz.</span><span class="sxs-lookup"><span data-stu-id="4c50d-112">The callback instance supplied when opening the line.</span></span>

</dd> <dt>

<span data-ttu-id="4c50d-113">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="4c50d-113">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="4c50d-114">Gerätespezifisch.</span><span class="sxs-lookup"><span data-stu-id="4c50d-114">Device specific.</span></span>

</dd> <dt>

<span data-ttu-id="4c50d-115">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="4c50d-115">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="4c50d-116">Gerätespezifisch.</span><span class="sxs-lookup"><span data-stu-id="4c50d-116">Device specific.</span></span>

</dd> <dt>

<span data-ttu-id="4c50d-117">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="4c50d-117">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="4c50d-118">Gerätespezifisch.</span><span class="sxs-lookup"><span data-stu-id="4c50d-118">Device specific.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4c50d-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4c50d-119">Return value</span></span>

<span data-ttu-id="4c50d-120">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="4c50d-120">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4c50d-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4c50d-121">Remarks</span></span>

<span data-ttu-id="4c50d-122">Die **\_ DevSpecific-Zeilen** Meldung wird von einem Dienstanbieter in Verbindung mit der [**linedevspecific**](/windows/desktop/api/Tapi/nf-tapi-linedevspecific) -Funktion verwendet.</span><span class="sxs-lookup"><span data-stu-id="4c50d-122">The **LINE\_DEVSPECIFIC** message is used by a service provider in conjunction with the [**lineDevSpecific**](/windows/desktop/api/Tapi/nf-tapi-linedevspecific) function.</span></span> <span data-ttu-id="4c50d-123">Seine Bedeutung ist gerätespezifisch.</span><span class="sxs-lookup"><span data-stu-id="4c50d-123">Its meaning is device specific.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c50d-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4c50d-124">Requirements</span></span>



| <span data-ttu-id="4c50d-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4c50d-125">Requirement</span></span> | <span data-ttu-id="4c50d-126">Wert</span><span class="sxs-lookup"><span data-stu-id="4c50d-126">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="4c50d-127">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="4c50d-127">TAPI version</span></span><br/> | <span data-ttu-id="4c50d-128">Erfordert TAPI 2,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="4c50d-128">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="4c50d-129">Header</span><span class="sxs-lookup"><span data-stu-id="4c50d-129">Header</span></span><br/>       | <dl> <span data-ttu-id="4c50d-130"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="4c50d-130"><dt>Tapi.h</dt></span></span> </dl> |



 

 




