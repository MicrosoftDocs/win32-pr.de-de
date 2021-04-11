---
description: Die mcsvc-Methode ruft die OnStatus-Methode auf, um den Monitor zu benachrichtigen, dass ein NPP-Status Ereignis vorhanden ist. Diese Methode muss vom Monitor implementiert werden.
ms.assetid: 771852b1-77d8-4d7d-b3fb-03eb3ea593b8
title: 'Imonitor:: OnStatus-Methode (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitor.OnStatus
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: fc2716a10673cc1178591b14a335b1d8559aa35a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130261"
---
# <a name="imonitoronstatus-method"></a><span data-ttu-id="ffa3d-104">Imonitor:: OnStatus-Methode</span><span class="sxs-lookup"><span data-stu-id="ffa3d-104">IMonitor::OnStatus method</span></span>

<span data-ttu-id="ffa3d-105">Die mcsvc-Methode ruft die **OnStatus** -Methode auf, um den Monitor zu benachrichtigen, dass ein NPP-Status Ereignis vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="ffa3d-105">The MCSVC method calls the **OnStatus** method to notify the monitor that an NPP status event exists.</span></span> <span data-ttu-id="ffa3d-106">Diese Methode muss vom Monitor implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="ffa3d-106">This method must be implemented by the monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="ffa3d-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="ffa3d-107">Syntax</span></span>


```C++
HRESULT OnStatus(
  [in] UPDATE_EVENT Event
);
```



## <a name="parameters"></a><span data-ttu-id="ffa3d-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="ffa3d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ffa3d-109">*Ereignis* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ffa3d-109">*Event* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ffa3d-110">Eine [Update- \_ Ereignis](update-event.md) Struktur.</span><span class="sxs-lookup"><span data-stu-id="ffa3d-110">An [UPDATE\_EVENT](update-event.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ffa3d-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ffa3d-111">Return value</span></span>

<span data-ttu-id="ffa3d-112">Wenn die Methode erfolgreich ist, lautet der Rückgabewert S \_ OK (entspricht noError), und der mcsvc übergibt den zurückgegebenen Wert zur Verarbeitung an den NPP zurück.</span><span class="sxs-lookup"><span data-stu-id="ffa3d-112">If the method is successful, the return value is S\_OK (which is the same as NOERROR), and the MCSVC passes the returned value back to the NPP for processing.</span></span>

<span data-ttu-id="ffa3d-113">Wenn die Methode nicht erfolgreich ist, wird ein Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ffa3d-113">If the method is unsuccessful, return an error code.</span></span> <span data-ttu-id="ffa3d-114">Bei einem Fehler übergibt der mcsvc den zurückgegebenen Wert zur Verarbeitung an den NPP zurück.</span><span class="sxs-lookup"><span data-stu-id="ffa3d-114">On error, the MCSVC passes the returned value back to the NPP for processing.</span></span>

## <a name="requirements"></a><span data-ttu-id="ffa3d-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ffa3d-115">Requirements</span></span>



| <span data-ttu-id="ffa3d-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ffa3d-116">Requirement</span></span> | <span data-ttu-id="ffa3d-117">Wert</span><span class="sxs-lookup"><span data-stu-id="ffa3d-117">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="ffa3d-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ffa3d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ffa3d-119">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ffa3d-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="ffa3d-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ffa3d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ffa3d-121">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ffa3d-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="ffa3d-122">Header</span><span class="sxs-lookup"><span data-stu-id="ffa3d-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="ffa3d-123"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="ffa3d-123"><dt>Netmon.h</dt></span></span> </dl> |



 

 




