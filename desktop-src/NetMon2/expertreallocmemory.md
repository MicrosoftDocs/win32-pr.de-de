---
description: Die Funktion "expertrebelegcmemory" erhöht oder verringert die Menge an Arbeitsspeicher, die von Netzwerkmonitor zugeordnet wird.
ms.assetid: 78b99a66-692a-4e83-8b0d-d68caf156bb6
title: Funktion "expertrebelegcmemory" (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExpertReallocMemory
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 8f562443f9ca66def7e053f5958b17e70af50140
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106342821"
---
# <a name="expertreallocmemory-function"></a><span data-ttu-id="995b9-103">Funktion "expertrebelegcmemory"</span><span class="sxs-lookup"><span data-stu-id="995b9-103">ExpertReallocMemory function</span></span>

<span data-ttu-id="995b9-104">Die Funktion " **expertrebelegcmemory** " erhöht oder verringert die Menge an Arbeitsspeicher, die von Netzwerkmonitor zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="995b9-104">The **ExpertReallocMemory** function increases or decreases the amount of memory allocated by Network Monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="995b9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="995b9-105">Syntax</span></span>


```C++
LPVOID WINAPI ExpertReallocMemory(
  _In_  HEXPERTKEY hExpertKey,
  _In_  LPVOID     pOriginalMemory,
  _In_  SIZE_T     nBytes,
  _Out_ LPDWORD    pError
);
```



## <a name="parameters"></a><span data-ttu-id="995b9-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="995b9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="995b9-107">*hexpertkey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="995b9-107">*hExpertKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="995b9-108">Eindeutiger Bezeichner, der beim [**Ausführen**](run.md) oder [**Konfigurieren**](configure.md)an den Experten übermittelt wird</span><span class="sxs-lookup"><span data-stu-id="995b9-108">Unique identifier passed to the expert at [**Run**](run.md) or [**Configure**](configure.md).</span></span>

</dd> <dt>

<span data-ttu-id="995b9-109">*poriginalmemory* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="995b9-109">*pOriginalMemory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="995b9-110">Zeiger auf den durch Netzwerkmonitor zugeordneten Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="995b9-110">Pointer to the memory allocated by Network Monitor.</span></span> <span data-ttu-id="995b9-111">Der *poriginalmemory* -Zeiger kann von einem vorherigen-Befehl von " [**expertenlocmemory**](expertallocmemory.md) " oder " **expertenspeicher**" zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="995b9-111">The *pOriginalMemory* pointer can be returned by a previous call to [**ExpertAllocMemory**](expertallocmemory.md) or **ExpertReallocMemory**.</span></span>

</dd> <dt>

<span data-ttu-id="995b9-112">*nbytes* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="995b9-112">*nBytes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="995b9-113">Größe des neu zugewiesenen Speichers.</span><span class="sxs-lookup"><span data-stu-id="995b9-113">Size of reallocated memory.</span></span>

</dd> <dt>

<span data-ttu-id="995b9-114">*perror* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="995b9-114">*pError* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="995b9-115">Bei der Rückgabe ein Fehlercode, wenn die Funktion fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="995b9-115">On return, an error code if the function fails.</span></span> <span data-ttu-id="995b9-116">Wenn der Fehlercode nmerr- \_ Experte \_ beendet ist, muss der Experte einen Cleanup durchsetzen und sofort zurückkehren.</span><span class="sxs-lookup"><span data-stu-id="995b9-116">If the error code is NMERR\_EXPERT\_TERMINATE, the expert must clean up and return immediately.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="995b9-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="995b9-117">Return value</span></span>

<span data-ttu-id="995b9-118">Wenn die Funktion erfolgreich ist, ist der Rückgabewert ein Zeiger auf den zugeordneten Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="995b9-118">If the function is successful, the return value is a pointer to the allocated memory.</span></span>

<span data-ttu-id="995b9-119">Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert **null**, und *perror* (wenn es sich um einen nicht-**null** -Wert handelt) gibt den Grund für den Fehler an.</span><span class="sxs-lookup"><span data-stu-id="995b9-119">If the function is unsuccessful, the return value is **NULL**, and *pError* (if it is a non-**NULL** value) indicates the reason for the failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="995b9-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="995b9-120">Remarks</span></span>

<span data-ttu-id="995b9-121">Es ist wichtig zu beachten, dass ein Experte die Netzwerkmonitor Speicher Belegungs Funktionen für die Speicherverwaltung verwenden sollte.</span><span class="sxs-lookup"><span data-stu-id="995b9-121">It is important to note that an expert should use the Network Monitor memory allocation functions for memory management.</span></span> <span data-ttu-id="995b9-122">Wenn Ihr Experte während der Laufzeit einen Fehler verursacht, ermöglicht die Verwendung dieser Funktionen Netzwerkmonitor, den zugeordneten Arbeitsspeicher freizugeben.</span><span class="sxs-lookup"><span data-stu-id="995b9-122">If your expert fails during run time, using these functions will allow Network Monitor to free the memory it has allocated.</span></span>

## <a name="requirements"></a><span data-ttu-id="995b9-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="995b9-123">Requirements</span></span>



| <span data-ttu-id="995b9-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="995b9-124">Requirement</span></span> | <span data-ttu-id="995b9-125">Wert</span><span class="sxs-lookup"><span data-stu-id="995b9-125">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="995b9-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="995b9-126">Minimum supported client</span></span><br/> | <span data-ttu-id="995b9-127">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="995b9-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="995b9-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="995b9-128">Minimum supported server</span></span><br/> | <span data-ttu-id="995b9-129">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="995b9-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="995b9-130">Header</span><span class="sxs-lookup"><span data-stu-id="995b9-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="995b9-131"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="995b9-131"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="995b9-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="995b9-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="995b9-133"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="995b9-133"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="995b9-134">DLL</span><span class="sxs-lookup"><span data-stu-id="995b9-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="995b9-135"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="995b9-135"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




