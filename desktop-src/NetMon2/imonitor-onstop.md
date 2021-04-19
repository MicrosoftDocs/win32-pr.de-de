---
description: Die onstoppt-Methode muss vom Monitor implementiert werden. Mscvc ruft diese Methode auf, um den Monitor zu benachrichtigen, dass die Erfassung beendet wird.
ms.assetid: 5988bfb8-2068-42a1-a774-6f6be9828568
title: 'Imonitor:: onstoppt-Methode (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitor.OnStop
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: a737aa5bede443b63f2074239eec17ea8a205cc8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343038"
---
# <a name="imonitoronstop-method"></a><span data-ttu-id="97795-104">Imonitor:: onstoppt-Methode</span><span class="sxs-lookup"><span data-stu-id="97795-104">IMonitor::OnStop method</span></span>

<span data-ttu-id="97795-105">Die **onstoppt** -Methode muss vom Monitor implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="97795-105">The **OnStop** method must be implemented by the monitor.</span></span> <span data-ttu-id="97795-106">Mscvc ruft diese Methode auf, um den Monitor zu benachrichtigen, dass die Erfassung beendet wird.</span><span class="sxs-lookup"><span data-stu-id="97795-106">The MSCVC calls this method to notify the monitor that the capture will be stopped.</span></span>

## <a name="syntax"></a><span data-ttu-id="97795-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="97795-107">Syntax</span></span>


```C++
HRESULT OnStop();
```



## <a name="parameters"></a><span data-ttu-id="97795-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="97795-108">Parameters</span></span>

<span data-ttu-id="97795-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="97795-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="97795-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="97795-110">Return value</span></span>

<span data-ttu-id="97795-111">Wenn die Methode erfolgreich ist, lautet der Rückgabewert S \_ OK (entspricht noError).</span><span class="sxs-lookup"><span data-stu-id="97795-111">If the method is successful, the return value is S\_OK (which is the same as NOERROR).</span></span>

<span data-ttu-id="97795-112">Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="97795-112">If the method is unsuccessful, the return value is an error code.</span></span> <span data-ttu-id="97795-113">Wenn ein Fehlercode zurückgegeben wird, kann der Monitor nicht neu gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="97795-113">When an error code is returned, the monitor cannot be restarted.</span></span>

## <a name="remarks"></a><span data-ttu-id="97795-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="97795-114">Remarks</span></span>

<span data-ttu-id="97795-115">Die mcsvc ruft diese Methode auf, nachdem " [iritc:: Beendigung](irtc-stop.md) " aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="97795-115">The MCSVC calls this method after [IRTC::Stop](irtc-stop.md) is called.</span></span>

## <a name="requirements"></a><span data-ttu-id="97795-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="97795-116">Requirements</span></span>



| <span data-ttu-id="97795-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="97795-117">Requirement</span></span> | <span data-ttu-id="97795-118">Wert</span><span class="sxs-lookup"><span data-stu-id="97795-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="97795-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="97795-119">Minimum supported client</span></span><br/> | <span data-ttu-id="97795-120">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="97795-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="97795-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="97795-121">Minimum supported server</span></span><br/> | <span data-ttu-id="97795-122">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="97795-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="97795-123">Header</span><span class="sxs-lookup"><span data-stu-id="97795-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="97795-124"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="97795-124"><dt>Netmon.h</dt></span></span> </dl> |



 

 




