---
description: Die onframes-Methode muss vom Monitor implementiert werden. Die mcsvc ruft diese Methode auf, wenn entweder der Erfassungs Puffer voll ist oder die Aktualisierungszeit abgelaufen ist.
ms.assetid: 243bd35b-2527-463e-b3d2-4bd840fe9c3f
title: 'Imonitor:: onframes-Methode (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitor.OnFrames
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: c5b6ff3e9d5b97a228e6e1d865fe4d8f1b5bfc9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751088"
---
# <a name="imonitoronframes-method"></a><span data-ttu-id="44356-104">Imonitor:: onframes-Methode</span><span class="sxs-lookup"><span data-stu-id="44356-104">IMonitor::OnFrames method</span></span>

<span data-ttu-id="44356-105">Die **onframes** -Methode muss vom Monitor implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="44356-105">The **OnFrames** method must be implemented by the monitor.</span></span> <span data-ttu-id="44356-106">Die mcsvc ruft diese Methode auf, wenn entweder der Erfassungs Puffer voll ist oder die Aktualisierungszeit abgelaufen ist.</span><span class="sxs-lookup"><span data-stu-id="44356-106">The MCSVC calls this method when either the capture buffer is full or the update time has passed.</span></span>

## <a name="syntax"></a><span data-ttu-id="44356-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="44356-107">Syntax</span></span>


```C++
HRESULT OnFrames(
  [in] UPDATE_EVENT Event
);
```



## <a name="parameters"></a><span data-ttu-id="44356-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="44356-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44356-109">*Ereignis* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="44356-109">*Event* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44356-110">[Aktualisieren \_ Ereignis](update-event.md) Struktur, die zum Aktualisieren von Ereignissen verwendete Frame Informationen enthält.</span><span class="sxs-lookup"><span data-stu-id="44356-110">[UPDATE\_EVENT](update-event.md) structure that holds frame information used to update events.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="44356-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="44356-111">Return value</span></span>

<span data-ttu-id="44356-112">Wenn die Methode erfolgreich ist, lautet der Rückgabewert S \_ OK (entspricht noError).</span><span class="sxs-lookup"><span data-stu-id="44356-112">If the method is successful, the return value is S\_OK (which is the same as NOERROR).</span></span> <span data-ttu-id="44356-113">Der mcsvc übergibt den zurückgegebenen Wert zur Verarbeitung an den NPP zurück.</span><span class="sxs-lookup"><span data-stu-id="44356-113">The MCSVC passes the returned value back to the NPP for processing.</span></span>

<span data-ttu-id="44356-114">Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="44356-114">If the method is unsuccessful, the return value is an error code.</span></span> <span data-ttu-id="44356-115">Der mcsvc übergibt den zurückgegebenen Wert zur Verarbeitung an den NPP zurück.</span><span class="sxs-lookup"><span data-stu-id="44356-115">The MCSVC passes the returned value back to the NPP for processing.</span></span>

## <a name="requirements"></a><span data-ttu-id="44356-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="44356-116">Requirements</span></span>



| <span data-ttu-id="44356-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="44356-117">Requirement</span></span> | <span data-ttu-id="44356-118">Wert</span><span class="sxs-lookup"><span data-stu-id="44356-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="44356-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="44356-119">Minimum supported client</span></span><br/> | <span data-ttu-id="44356-120">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="44356-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="44356-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="44356-121">Minimum supported server</span></span><br/> | <span data-ttu-id="44356-122">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="44356-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="44356-123">Header</span><span class="sxs-lookup"><span data-stu-id="44356-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="44356-124"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="44356-124"><dt>Netmon.h</dt></span></span> </dl> |



 

 




