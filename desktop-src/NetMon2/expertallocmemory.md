---
description: Die Funktion "ExpertAllocMemory" ordnet dem Experten Arbeitsspeicher zu.
ms.assetid: 9ada5d3f-5f1d-4d3a-b79a-d51e021240f6
title: Funktion "ExpertAllocMemory" (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExpertAllocMemory
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: b30aba5e2b448df141d0c82e6ec5a2b0d9b3303f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750105"
---
# <a name="expertallocmemory-function"></a><span data-ttu-id="752ba-103">Funktion "ExpertAllocMemory"</span><span class="sxs-lookup"><span data-stu-id="752ba-103">ExpertAllocMemory function</span></span>

<span data-ttu-id="752ba-104">Die Funktion " **ExpertAllocMemory** " ordnet dem Experten Arbeitsspeicher zu.</span><span class="sxs-lookup"><span data-stu-id="752ba-104">The **ExpertAllocMemory** function allocates memory for the expert.</span></span>

## <a name="syntax"></a><span data-ttu-id="752ba-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="752ba-105">Syntax</span></span>


```C++
LPVOID WINAPI ExpertAllocMemory(
        HEXPERTKEY hExpertKey,
  _In_  SIZE_T     nBytes,
  _Out_ LPDWORD    pError
);
```



## <a name="parameters"></a><span data-ttu-id="752ba-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="752ba-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="752ba-107">*hexpertkey*</span><span class="sxs-lookup"><span data-stu-id="752ba-107">*hExpertKey*</span></span> 
</dt> <dd>

<span data-ttu-id="752ba-108">Eindeutige expertenkennung.</span><span class="sxs-lookup"><span data-stu-id="752ba-108">Unique expert identifier.</span></span> <span data-ttu-id="752ba-109">Netzwerkmonitor übergibt *hexpertkey* an den Experten, wenn die Funktion [Run](run.md) aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="752ba-109">Network Monitor passes *hExpertKey* to the expert when it calls the [Run](run.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="752ba-110">*nbytes* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="752ba-110">*nBytes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="752ba-111">Zugewiesener Arbeitsspeicher (gemessen in Bytes).</span><span class="sxs-lookup"><span data-stu-id="752ba-111">Allocated memory, measured in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="752ba-112">*perror* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="752ba-112">*pError* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="752ba-113">Fehler Indikator.</span><span class="sxs-lookup"><span data-stu-id="752ba-113">Error indicator.</span></span> <span data-ttu-id="752ba-114">Wenn die Funktion fehlschlägt, enthält der *nbytes* -Parameter den Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="752ba-114">If the function fails, the *nBytes* parameter contains the error code.</span></span> <span data-ttu-id="752ba-115">Wenn der Fehlercode nmerr \_ -Experte \_ beendet ist, muss der Experte eine Bereinigung durchsetzen und sofort zurückkehren.</span><span class="sxs-lookup"><span data-stu-id="752ba-115">If the error code is NMERR\_EXPERT\_TERMINATE, the expert must clean-up and return immediately.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="752ba-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="752ba-116">Return value</span></span>

<span data-ttu-id="752ba-117">Wenn die Funktion erfolgreich ist, ist der Rückgabewert ein Zeiger auf den zugeordneten Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="752ba-117">If the function is successful, the return value is a pointer to the allocated memory.</span></span>

<span data-ttu-id="752ba-118">Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert **null**, und *perror* bietet einen Fehlercode, der den Grund für den Fehler angibt.</span><span class="sxs-lookup"><span data-stu-id="752ba-118">If the function is unsuccessful, the return value is **NULL**, and *pError* provides an error code that indicates the reason for the failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="752ba-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="752ba-119">Remarks</span></span>

<span data-ttu-id="752ba-120">Es ist wichtig zu beachten, dass ein Experte die Netzwerkmonitor Speicher Belegungs Funktionen (einschließlich " [expertenspeicher](expertreallocmemory.md)") für die Speicherverwaltung verwenden sollte.</span><span class="sxs-lookup"><span data-stu-id="752ba-120">It is important to note that an expert should use the Network Monitor memory allocation functions (including [ExpertReallocMemory](expertreallocmemory.md)) for memory management.</span></span> <span data-ttu-id="752ba-121">Wenn Ihr Experte während der Laufzeit einen Fehler verursacht, ermöglicht die Verwendung dieser Funktionen Netzwerkmonitor, den zugeordneten Arbeitsspeicher freizugeben.</span><span class="sxs-lookup"><span data-stu-id="752ba-121">If your expert fails during run time, using these functions will allow Network Monitor to free the memory it has allocated.</span></span>

## <a name="requirements"></a><span data-ttu-id="752ba-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="752ba-122">Requirements</span></span>



| <span data-ttu-id="752ba-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="752ba-123">Requirement</span></span> | <span data-ttu-id="752ba-124">Wert</span><span class="sxs-lookup"><span data-stu-id="752ba-124">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="752ba-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="752ba-125">Minimum supported client</span></span><br/> | <span data-ttu-id="752ba-126">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="752ba-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="752ba-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="752ba-127">Minimum supported server</span></span><br/> | <span data-ttu-id="752ba-128">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="752ba-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="752ba-129">Header</span><span class="sxs-lookup"><span data-stu-id="752ba-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="752ba-130"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="752ba-130"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="752ba-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="752ba-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="752ba-132"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="752ba-132"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="752ba-133">DLL</span><span class="sxs-lookup"><span data-stu-id="752ba-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="752ba-134"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="752ba-134"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




