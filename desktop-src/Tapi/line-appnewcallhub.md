---
description: Die TAPI-Zeile \_ appnewcallhub-Nachricht wird gesendet, um eine Anwendung zu informieren, wenn ein neuer callhub erstellt wurde.
ms.assetid: cf693d95-9abb-4999-81b6-7d2aa06d0f58
title: LINE_APPNEWCALLHUB Meldung (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 634dd82aadd5e3c8a7664572136b54f8bbdf8a52
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369183"
---
# <a name="line_appnewcallhub-message"></a><span data-ttu-id="2e0e0-103">Zeile \_ appnewcallhub-Nachricht</span><span class="sxs-lookup"><span data-stu-id="2e0e0-103">LINE\_APPNEWCALLHUB message</span></span>

<span data-ttu-id="2e0e0-104">Die TAPI- **Zeile \_ appnewcallhub** -Nachricht wird gesendet, um eine Anwendung zu informieren, wenn ein neuer callhub erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="2e0e0-104">The TAPI **LINE\_APPNEWCALLHUB** message is sent to inform an application when a new call hub has been created.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="2e0e0-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="2e0e0-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e0e0-106">*hdevice*</span><span class="sxs-lookup"><span data-stu-id="2e0e0-106">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="2e0e0-107">Ein Handle für den-Befehl.</span><span class="sxs-lookup"><span data-stu-id="2e0e0-107">A handle to the call.</span></span>

</dd> <dt>

<span data-ttu-id="2e0e0-108">*dwcallbackinstance*</span><span class="sxs-lookup"><span data-stu-id="2e0e0-108">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="2e0e0-109">Die beim Öffnen der Zeile des Aufrufs angegebene Rückruf Instanz.</span><span class="sxs-lookup"><span data-stu-id="2e0e0-109">The callback instance supplied when opening the call's line.</span></span>

</dd> <dt>

<span data-ttu-id="2e0e0-110">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="2e0e0-110">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="2e0e0-111">Die nach Verfolgungs Ebene für den neuen Hub, wie von einer der [**linecallhubtracking- \_ Konstanten**](linecallhubtracking--constants.md)definiert.</span><span class="sxs-lookup"><span data-stu-id="2e0e0-111">The tracking level on the new hub, as defined by one of the [**LINECALLHUBTRACKING\_ Constants**](linecallhubtracking--constants.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e0e0-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2e0e0-112">Return value</span></span>

<span data-ttu-id="2e0e0-113">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="2e0e0-113">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2e0e0-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2e0e0-114">Remarks</span></span>

<span data-ttu-id="2e0e0-115">Diese Nachricht stammt von TAPI anstelle eines Dienstanbieters, sodass keine entsprechende TSPI-Nachricht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="2e0e0-115">This message originates with TAPI rather than with a service provider, so there is no corresponding TSPI message.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e0e0-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2e0e0-116">Requirements</span></span>



| <span data-ttu-id="2e0e0-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2e0e0-117">Requirement</span></span> | <span data-ttu-id="2e0e0-118">Wert</span><span class="sxs-lookup"><span data-stu-id="2e0e0-118">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="2e0e0-119">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="2e0e0-119">TAPI version</span></span><br/> | <span data-ttu-id="2e0e0-120">Erfordert TAPI 2,2</span><span class="sxs-lookup"><span data-stu-id="2e0e0-120">Requires TAPI 2.2</span></span><br/>                                                      |
| <span data-ttu-id="2e0e0-121">Header</span><span class="sxs-lookup"><span data-stu-id="2e0e0-121">Header</span></span><br/>       | <dl> <span data-ttu-id="2e0e0-122"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="2e0e0-122"><dt>Tapi.h</dt></span></span> </dl> |



 

 




