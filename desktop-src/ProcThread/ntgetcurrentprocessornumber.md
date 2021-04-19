---
description: Ruft die Nummer des Prozessors ab, auf dem der aktuelle Thread während des Aufrufens dieser Funktion ausgeführt wurde.
ms.assetid: f0141550-58e2-421a-934d-9a6c488d2b81
title: Ntgetcurrentprocessornumber-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGetCurrentProcessorNumber
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 96862836d3f9c16034ce1c2e751aebea2884d114
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370790"
---
# <a name="ntgetcurrentprocessornumber-function"></a><span data-ttu-id="253bb-103">Ntgetcurrentprocessornumber-Funktion</span><span class="sxs-lookup"><span data-stu-id="253bb-103">NtGetCurrentProcessorNumber function</span></span>

<span data-ttu-id="253bb-104">\[**Ntgetcurrentprocessornumber** kann geändert werden oder ist in zukünftigen Versionen von Windows nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="253bb-104">\[**NtGetCurrentProcessorNumber** may be altered or unavailable in future versions of Windows.</span></span> <span data-ttu-id="253bb-105">Anwendungen sollten stattdessen die [**getcurrentprocessornumber**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocessornumber) -Funktion verwenden.\]</span><span class="sxs-lookup"><span data-stu-id="253bb-105">Applications should use the [**GetCurrentProcessorNumber**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocessornumber) function instead.\]</span></span>

<span data-ttu-id="253bb-106">Ruft die Nummer des Prozessors ab, auf dem der aktuelle Thread während des Aufrufens dieser Funktion ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="253bb-106">Retrieves the number of the processor the current thread was running on during the call to this function.</span></span>

## <a name="syntax"></a><span data-ttu-id="253bb-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="253bb-107">Syntax</span></span>


```C++
ULONG WINAPI NtGetCurrentProcessorNumber(void);
```



## <a name="parameters"></a><span data-ttu-id="253bb-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="253bb-108">Parameters</span></span>

<span data-ttu-id="253bb-109">Diese Funktion besitzt keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="253bb-109">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="253bb-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="253bb-110">Return value</span></span>

<span data-ttu-id="253bb-111">Die-Funktion gibt die aktuelle Prozessornummer zurück.</span><span class="sxs-lookup"><span data-stu-id="253bb-111">The function returns the current processor number.</span></span>

## <a name="remarks"></a><span data-ttu-id="253bb-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="253bb-112">Remarks</span></span>

<span data-ttu-id="253bb-113">Diese Funktion dient zum Bereitstellen von Informationen zum Schätzen der Prozessleistung.</span><span class="sxs-lookup"><span data-stu-id="253bb-113">This function is used to provide information for estimating process performance.</span></span>

<span data-ttu-id="253bb-114">Diese Funktion verfügt über keine zugeordnete Import Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="253bb-114">This function has no associated import library.</span></span> <span data-ttu-id="253bb-115">Sie müssen die [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und die [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion verwenden, um dynamisch mit Ntdll.dll zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="253bb-115">You must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Ntdll.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="253bb-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="253bb-116">Requirements</span></span>



| <span data-ttu-id="253bb-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="253bb-117">Requirement</span></span> | <span data-ttu-id="253bb-118">Wert</span><span class="sxs-lookup"><span data-stu-id="253bb-118">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="253bb-119">DLL</span><span class="sxs-lookup"><span data-stu-id="253bb-119">DLL</span></span><br/> | <dl> <span data-ttu-id="253bb-120"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="253bb-120"><dt>Ntdll.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="253bb-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="253bb-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="253bb-122">Mehrere Prozessoren</span><span class="sxs-lookup"><span data-stu-id="253bb-122">Multiple Processors</span></span>](multiple-processors.md)
</dt> <dt>

[<span data-ttu-id="253bb-123">Prozess- und Threadfunktionen</span><span class="sxs-lookup"><span data-stu-id="253bb-123">Process and Thread Functions</span></span>](process-and-thread-functions.md)
</dt> <dt>

[<span data-ttu-id="253bb-124">Prozesse</span><span class="sxs-lookup"><span data-stu-id="253bb-124">Processes</span></span>](child-processes.md)
</dt> </dl>

 

 
