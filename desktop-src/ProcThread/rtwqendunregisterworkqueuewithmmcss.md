---
description: Schließt eine asynchrone Anforderung zum Aufheben der Registrierung einer Arbeits Warteschlange bei einem Multimedia Class Scheduler Service-Task (MMCSS) ab.
ms.assetid: 0E8F9BF6-AC1E-4FC0-BFAE-F292C4859F1F
title: Rtwqendunregisterworkqueuewithmmcss-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtwqEndUnregisterWorkQueueWithMMCSS
api_type:
- DllExport
api_location:
- RTWorkQ.dll
ms.openlocfilehash: b55386b2a018b0e311a1d4dbb2084b136d49c2f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865736"
---
# <a name="rtwqendunregisterworkqueuewithmmcss-function"></a><span data-ttu-id="5d7aa-103">Rtwqendunregisterworkqueuewithmmcss-Funktion</span><span class="sxs-lookup"><span data-stu-id="5d7aa-103">RtwqEndUnregisterWorkQueueWithMMCSS function</span></span>

<span data-ttu-id="5d7aa-104">Schließt eine asynchrone Anforderung zum Aufheben der Registrierung einer Arbeits Warteschlange bei einem Multimedia Class Scheduler Service-Task (MMCSS) ab.</span><span class="sxs-lookup"><span data-stu-id="5d7aa-104">Completes an asynchronous request to unregister a work queue with a Multimedia Class Scheduler Service (MMCSS) task.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d7aa-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5d7aa-105">Syntax</span></span>


```C++
HRESULT WINAPI RtwqEndUnregisterWorkQueueWithMMCSS(
    IMFAsyncResult  *pResult 
);
```



## <a name="parameters"></a><span data-ttu-id="5d7aa-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5d7aa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d7aa-107">*pResult*</span><span class="sxs-lookup"><span data-stu-id="5d7aa-107">*pResult*</span></span> 
</dt> <dd>

<span data-ttu-id="5d7aa-108">Zeiger auf die [**imfasynkresult**](/windows/win32/api/mfobjects/nn-mfobjects-imfasyncresult) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="5d7aa-108">Pointer to the [**IMFAsyncResult**](/windows/win32/api/mfobjects/nn-mfobjects-imfasyncresult) interface.</span></span> <span data-ttu-id="5d7aa-109">Übergeben Sie denselben Zeiger, den das Rückruf Objekt in der Methode " [**untwqasynccallback:: Aufrufen**](/windows/win32/api/rtworkq/nf-rtworkq-irtwqasynccallback-invoke) " erhalten hat.</span><span class="sxs-lookup"><span data-stu-id="5d7aa-109">Pass in the same pointer that your callback object received in the [**IRtwqAsyncCallback::Invoke**](/windows/win32/api/rtworkq/nf-rtworkq-irtwqasynccallback-invoke) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d7aa-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5d7aa-110">Return value</span></span>

<span data-ttu-id="5d7aa-111">Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="5d7aa-111">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5d7aa-112">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5d7aa-112">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d7aa-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5d7aa-113">Requirements</span></span>



| <span data-ttu-id="5d7aa-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5d7aa-114">Requirement</span></span> | <span data-ttu-id="5d7aa-115">Wert</span><span class="sxs-lookup"><span data-stu-id="5d7aa-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5d7aa-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5d7aa-116">Minimum supported client</span></span><br/> | <span data-ttu-id="5d7aa-117">\[Nur Desktop-Apps Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="5d7aa-117">Windows 8.1 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="5d7aa-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5d7aa-118">Minimum supported server</span></span><br/> | <span data-ttu-id="5d7aa-119">Nur Windows Server 2012 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5d7aa-119">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="5d7aa-120">Header</span><span class="sxs-lookup"><span data-stu-id="5d7aa-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="5d7aa-121"><dt>None</dt></span><span class="sxs-lookup"><span data-stu-id="5d7aa-121"><dt>None</dt></span></span> </dl>        |
| <span data-ttu-id="5d7aa-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="5d7aa-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="5d7aa-123"><dt>Rtworkq. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5d7aa-123"><dt>Rtworkq.lib</dt></span></span> </dl> |
| <span data-ttu-id="5d7aa-124">DLL</span><span class="sxs-lookup"><span data-stu-id="5d7aa-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5d7aa-125"><dt>RTWorkQ.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5d7aa-125"><dt>RTWorkQ.dll</dt></span></span> </dl> |



 

 
