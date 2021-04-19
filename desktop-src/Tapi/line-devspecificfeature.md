---
description: Die TAPI-Linien- \_ devspecificfeature-Nachricht wird gesendet, um die Anwendung über gerätespezifische Ereignisse zu benachrichtigen, die in einer Zeile, Adresse oder einem Rückruf auftreten. Die Bedeutung der Nachricht und die Interpretation der Parameter sind gerätespezifisch.
ms.assetid: 5f1a4da2-1a2a-4a18-8a69-82d27ddca9cf
title: LINE_DEVSPECIFICFEATURE Meldung (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d45f91f4b3d45b52a345827e6535b054e9cf2c2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360438"
---
# <a name="line_devspecificfeature-message"></a><span data-ttu-id="51ee9-104">LINE \_ devspecificfeature-Meldung</span><span class="sxs-lookup"><span data-stu-id="51ee9-104">LINE\_DEVSPECIFICFEATURE message</span></span>

<span data-ttu-id="51ee9-105">Die TAPI- **Linien- \_ devspecificfeature** -Nachricht wird gesendet, um die Anwendung über gerätespezifische Ereignisse zu benachrichtigen, die in einer Zeile, Adresse oder einem Rückruf auftreten.</span><span class="sxs-lookup"><span data-stu-id="51ee9-105">The TAPI **LINE\_DEVSPECIFICFEATURE** message is sent to notify the application about device-specific events occurring on a line, address, or call.</span></span> <span data-ttu-id="51ee9-106">Die Bedeutung der Nachricht und die Interpretation der Parameter sind gerätespezifisch.</span><span class="sxs-lookup"><span data-stu-id="51ee9-106">The meaning of the message and the interpretation of the parameters are device specific.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="51ee9-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="51ee9-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51ee9-108">*hdevice*</span><span class="sxs-lookup"><span data-stu-id="51ee9-108">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="51ee9-109">Ein Handle für ein Zeilen Gerät oder einen-Befehl.</span><span class="sxs-lookup"><span data-stu-id="51ee9-109">A handle to either a line device or call.</span></span> <span data-ttu-id="51ee9-110">Dies ist gerätespezifisch.</span><span class="sxs-lookup"><span data-stu-id="51ee9-110">This is device specific.</span></span>

</dd> <dt>

<span data-ttu-id="51ee9-111">*dwcallbackinstance*</span><span class="sxs-lookup"><span data-stu-id="51ee9-111">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="51ee9-112">Die beim Öffnen der Zeile angegebene Rückruf Instanz.</span><span class="sxs-lookup"><span data-stu-id="51ee9-112">The callback instance supplied when opening the line.</span></span>

</dd> <dt>

<span data-ttu-id="51ee9-113">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="51ee9-113">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="51ee9-114">Gerätespezifisch.</span><span class="sxs-lookup"><span data-stu-id="51ee9-114">Device specific.</span></span>

</dd> <dt>

<span data-ttu-id="51ee9-115">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="51ee9-115">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="51ee9-116">Gerätespezifisch.</span><span class="sxs-lookup"><span data-stu-id="51ee9-116">Device specific.</span></span>

</dd> <dt>

<span data-ttu-id="51ee9-117">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="51ee9-117">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="51ee9-118">Gerätespezifisch.</span><span class="sxs-lookup"><span data-stu-id="51ee9-118">Device specific.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="51ee9-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="51ee9-119">Return value</span></span>

<span data-ttu-id="51ee9-120">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="51ee9-120">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="51ee9-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="51ee9-121">Remarks</span></span>

<span data-ttu-id="51ee9-122">Die **Zeile \_ devspecificfeature** -Nachricht wird von einem Dienstanbieter in Verbindung mit der Funktion [**linedevspecificfeature**](/windows/desktop/api/Tapi/nf-tapi-linedevspecificfeature) verwendet.</span><span class="sxs-lookup"><span data-stu-id="51ee9-122">The **LINE\_DEVSPECIFICFEATURE** message is used by a service provider in conjunction with the [**lineDevSpecificFeature**](/windows/desktop/api/Tapi/nf-tapi-linedevspecificfeature) function.</span></span> <span data-ttu-id="51ee9-123">Seine Bedeutung ist gerätespezifisch.</span><span class="sxs-lookup"><span data-stu-id="51ee9-123">Its meaning is device specific.</span></span>

## <a name="requirements"></a><span data-ttu-id="51ee9-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="51ee9-124">Requirements</span></span>



| <span data-ttu-id="51ee9-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="51ee9-125">Requirement</span></span> | <span data-ttu-id="51ee9-126">Wert</span><span class="sxs-lookup"><span data-stu-id="51ee9-126">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="51ee9-127">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="51ee9-127">TAPI version</span></span><br/> | <span data-ttu-id="51ee9-128">Erfordert TAPI 2,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="51ee9-128">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="51ee9-129">Header</span><span class="sxs-lookup"><span data-stu-id="51ee9-129">Header</span></span><br/>       | <dl> <span data-ttu-id="51ee9-130"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="51ee9-130"><dt>Tapi.h</dt></span></span> </dl> |



 

 




