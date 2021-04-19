---
description: Die sendnmevent-Methode übermittelt Ereignisse an Windows-Verwaltungsinstrumentation (WMI).
ms.assetid: 85c33a71-72aa-4b0a-8e8b-3a220a080bb2
title: 'Imonitoreventer:: sendnmevent-Methode (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitorEventer.SendNMEvent
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: 3286fca4d5b852d4562c13446699c1a6b40f3efe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356560"
---
# <a name="imonitoreventersendnmevent-method"></a><span data-ttu-id="9b90f-103">Imonitoreventer:: sendnmevent-Methode</span><span class="sxs-lookup"><span data-stu-id="9b90f-103">IMonitorEventer::SendNMEvent method</span></span>

<span data-ttu-id="9b90f-104">Die **sendnmevent** -Methode übermittelt Ereignisse an Windows-Verwaltungsinstrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="9b90f-104">The **SendNMEvent** method submits events to Windows Management Instrumentation (WMI).</span></span>

## <a name="syntax"></a><span data-ttu-id="9b90f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9b90f-105">Syntax</span></span>


```C++
HRESULT SendNMEvent(
  [in] PNMEVENTDATA pNMEventData
);
```



## <a name="parameters"></a><span data-ttu-id="9b90f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9b90f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b90f-107">*pnmeventdata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9b90f-107">*pNMEventData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b90f-108">Zeiger auf das Ereignis, das an WMI gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="9b90f-108">Pointer to the event submitted to WMI.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9b90f-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9b90f-109">Return value</span></span>

<span data-ttu-id="9b90f-110">Wenn die Methode erfolgreich ist, lautet der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="9b90f-110">If the method is successful, the return value is S\_OK.</span></span>

<span data-ttu-id="9b90f-111">Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert nmerr nicht genügend Arbeits \_ \_ \_ Speicher.</span><span class="sxs-lookup"><span data-stu-id="9b90f-111">If the method is unsuccessful, the return value is NMERR\_OUT\_OF\_MEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b90f-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9b90f-112">Requirements</span></span>



| <span data-ttu-id="9b90f-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9b90f-113">Requirement</span></span> | <span data-ttu-id="9b90f-114">Wert</span><span class="sxs-lookup"><span data-stu-id="9b90f-114">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="9b90f-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9b90f-115">Minimum supported client</span></span><br/> | <span data-ttu-id="9b90f-116">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9b90f-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="9b90f-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9b90f-117">Minimum supported server</span></span><br/> | <span data-ttu-id="9b90f-118">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9b90f-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="9b90f-119">Header</span><span class="sxs-lookup"><span data-stu-id="9b90f-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="9b90f-120"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="9b90f-120"><dt>Netmon.h</dt></span></span> </dl> |



 

 




