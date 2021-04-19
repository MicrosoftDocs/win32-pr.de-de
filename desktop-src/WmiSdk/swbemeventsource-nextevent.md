---
description: Wenn ein Ereignis verfügbar ist, ruft die NextEvent-Methode des Objekts "slibemeventsource" das Ereignis aus einer Ereignis Abfrage ab.
ms.assetid: ff2d54d4-b8ee-4bb8-b6f7-081a1ca20489
ms.tgt_platform: multiple
title: Errbemeventsource. NextEvent-Methode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemEventSource.NextEvent
- ISWbemEventSource.NextEvent
- ISWbemEventSource.NextEvent
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 02fbc32557ab29c66849a4249d26cc2ca41564e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106357046"
---
# <a name="swbemeventsourcenextevent-method"></a><span data-ttu-id="0e15b-103">Errbemeventsource. NextEvent-Methode</span><span class="sxs-lookup"><span data-stu-id="0e15b-103">SWbemEventSource.NextEvent method</span></span>

<span data-ttu-id="0e15b-104">Wenn ein Ereignis verfügbar ist, ruft die **NextEvent** -Methode des Objekts " [**slibemeventsource**](swbemeventsource.md) " das Ereignis aus einer Ereignis Abfrage ab.</span><span class="sxs-lookup"><span data-stu-id="0e15b-104">If an event is available, the **NextEvent** method of the [**SWbemEventSource**](swbemeventsource.md) object retrieves the event from an event query.</span></span>

<span data-ttu-id="0e15b-105">Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="0e15b-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="0e15b-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="0e15b-106">Syntax</span></span>


```VB
objWbemObject = .NextEvent( _
  [ ByVal iTimeoutMs ] _
)
```



## <a name="parameters"></a><span data-ttu-id="0e15b-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="0e15b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e15b-108">*itimeoutms* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="0e15b-108">*iTimeoutMs* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="0e15b-109">Anzahl der Millisekunden, die der Aufruf auf ein Ereignis wartet, bevor ein Timeout Fehler zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="0e15b-109">Number of milliseconds the call waits for an event before returning a time-out error.</span></span> <span data-ttu-id="0e15b-110">Der Standardwert für diesen Parameter ist **wbemtimeoutinfinite** (-1), der den-Vorgang anweist, unbegrenzt zu warten.</span><span class="sxs-lookup"><span data-stu-id="0e15b-110">The default value for this parameter is **wbemTimeoutInfinite** (-1), which directs the call to wait indefinitely.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e15b-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0e15b-111">Return value</span></span>

<span data-ttu-id="0e15b-112">Wenn die **NextEvent** -Methode erfolgreich ist, gibt Sie ein " [**errbemujebject**](swbemobject.md) "-Objekt zurück, das das angeforderte Ereignis enthält.</span><span class="sxs-lookup"><span data-stu-id="0e15b-112">If the **NextEvent** method is successful, it returns an [**SWbemObject**](swbemobject.md) object that contains the requested event.</span></span> <span data-ttu-id="0e15b-113">Wenn für den-Rückruf ein Timeout auftritt, ist das zurückgegebene-Objekt **null** , und es wird ein Fehler ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="0e15b-113">If the call times out, the returned object is **NULL** and an error is raised.</span></span>

## <a name="error-codes"></a><span data-ttu-id="0e15b-114">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="0e15b-114">Error codes</span></span>

<span data-ttu-id="0e15b-115">Nach dem Abschluss der **NextEvent** -Methode kann das **Err** -Objekt den Fehlercode in der folgenden Liste enthalten.</span><span class="sxs-lookup"><span data-stu-id="0e15b-115">Upon the completion of the **NextEvent** method, the **Err** object may contain the error code in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="0e15b-116">**wbemErrTimedOut** -0x80043001</span><span class="sxs-lookup"><span data-stu-id="0e15b-116">**wbemErrTimedOut** - 0x80043001</span></span>
</dt> <dd>

<span data-ttu-id="0e15b-117">Das angeforderte Ereignis wurde nicht in der in *itimeoutms* angegebenen Zeit erreicht.</span><span class="sxs-lookup"><span data-stu-id="0e15b-117">Requested event did not arrive in the amount of time specified in *iTimeoutMs.*</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0e15b-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0e15b-118">Requirements</span></span>



| <span data-ttu-id="0e15b-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0e15b-119">Requirement</span></span> | <span data-ttu-id="0e15b-120">Wert</span><span class="sxs-lookup"><span data-stu-id="0e15b-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0e15b-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0e15b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="0e15b-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0e15b-122">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0e15b-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0e15b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="0e15b-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0e15b-124">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0e15b-125">Header</span><span class="sxs-lookup"><span data-stu-id="0e15b-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="0e15b-126"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="0e15b-126"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="0e15b-127">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="0e15b-127">Type library</span></span><br/>             | <dl> <span data-ttu-id="0e15b-128"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="0e15b-128"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="0e15b-129">DLL</span><span class="sxs-lookup"><span data-stu-id="0e15b-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0e15b-130"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0e15b-130"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="0e15b-131">CLSID</span><span class="sxs-lookup"><span data-stu-id="0e15b-131">CLSID</span></span><br/>                    | <span data-ttu-id="0e15b-132">CLSID-austauschen von " \_ errbemeventsource"</span><span class="sxs-lookup"><span data-stu-id="0e15b-132">CLSID\_SWbemEventSource</span></span><br/>                                                      |
| <span data-ttu-id="0e15b-133">IID</span><span class="sxs-lookup"><span data-stu-id="0e15b-133">IID</span></span><br/>                      | <span data-ttu-id="0e15b-134">IID \_ iswbemeventsource</span><span class="sxs-lookup"><span data-stu-id="0e15b-134">IID\_ISWbemEventSource</span></span><br/>                                                       |



 

 




