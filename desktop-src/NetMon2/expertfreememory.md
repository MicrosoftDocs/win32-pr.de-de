---
description: Die Funktion "expertfrememory" gibt Speicher frei, der durch Aufrufe der Funktionen "ExpertAllocMemory" und "expertrebelegcmemory" abgerufen wurde.
ms.assetid: 0e7cc791-98dd-4522-afab-76ac9e74c715
title: Funktion "expertfrememory" (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExpertFreeMemory
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: cc26056a3ec3e8820c363d97f92c7eb382cd0622
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345663"
---
# <a name="expertfreememory-function"></a><span data-ttu-id="4e8f5-103">Funktion "expertfrememory"</span><span class="sxs-lookup"><span data-stu-id="4e8f5-103">ExpertFreeMemory function</span></span>

<span data-ttu-id="4e8f5-104">Die Funktion " **expertfrememory** " gibt Speicher frei, der durch Aufrufe der Funktionen " [**ExpertAllocMemory**](expertallocmemory.md) " und " [**expertrebelegcmemory**](expertreallocmemory.md) " abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="4e8f5-104">The **ExpertFreeMemory** function frees memory acquired by calls to the [**ExpertAllocMemory**](expertallocmemory.md) and [**ExpertReallocMemory**](expertreallocmemory.md) functions.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e8f5-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4e8f5-105">Syntax</span></span>


```C++
SIZE_T WINAPI ExpertFreeMemory(
       HEXPERTKEY hExpertKey,
  _In_ LPVOID     pMemory
);
```



## <a name="parameters"></a><span data-ttu-id="4e8f5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4e8f5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e8f5-107">*hexpertkey*</span><span class="sxs-lookup"><span data-stu-id="4e8f5-107">*hExpertKey*</span></span> 
</dt> <dd>

<span data-ttu-id="4e8f5-108">Eindeutige expertenkennung.</span><span class="sxs-lookup"><span data-stu-id="4e8f5-108">Unique expert identifier.</span></span> <span data-ttu-id="4e8f5-109">Netzwerkmonitor übergibt *hexpertkey* an den Experten, wenn die Funktion [Run](run.md) aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="4e8f5-109">Network Monitor passes *hExpertKey* to the expert when it calls the [Run](run.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="4e8f5-110">*pmemory* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4e8f5-110">*pMemory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e8f5-111">Zeiger auf den Arbeitsspeicher, der von Netzwerkmonitor zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="4e8f5-111">Pointer to the memory that Network Monitor allocates.</span></span> <span data-ttu-id="4e8f5-112">Der *pmemory* -Zeiger kann von einem vorherigen-Befehl von " [**expertenlocmemory**](expertallocmemory.md) " oder " [**expertenspeicher**](expertreallocmemory.md)" zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="4e8f5-112">The *pMemory* pointer can be returned by a previous call to [**ExpertAllocMemory**](expertallocmemory.md) or [**ExpertReallocMemory**](expertreallocmemory.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e8f5-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4e8f5-113">Return value</span></span>

<span data-ttu-id="4e8f5-114">, Wenn die Funktion erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="4e8f5-114">If the function is successful.</span></span> <span data-ttu-id="4e8f5-115">der Rückgabewert ist "nmerr \_ Success".</span><span class="sxs-lookup"><span data-stu-id="4e8f5-115">the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="4e8f5-116">Wenn die Funktion nicht erfolgreich ist, gibt der Rückgabewert den Grund für den Fehler an.</span><span class="sxs-lookup"><span data-stu-id="4e8f5-116">If the function is unsuccessful, the return value indicates the reason for the failure.</span></span> <span data-ttu-id="4e8f5-117">Wenn der Rückgabewert nmerr- \_ Experte \_ beendet ist, bereinigt der Experte sofort und gibt ihn zurück.</span><span class="sxs-lookup"><span data-stu-id="4e8f5-117">If the return value is NMERR\_EXPERT\_TERMINATE, the expert immediately cleans up and returns.</span></span>

## <a name="remarks"></a><span data-ttu-id="4e8f5-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4e8f5-118">Remarks</span></span>

<span data-ttu-id="4e8f5-119">Es ist wichtig zu beachten, dass ein Experte die Netzwerkmonitor Speicher Belegungs Funktionen für die Speicherverwaltung verwenden sollte.</span><span class="sxs-lookup"><span data-stu-id="4e8f5-119">It is important to note that an expert should use the Network Monitor memory allocation functions for memory management.</span></span> <span data-ttu-id="4e8f5-120">Wenn Ihr Experte während der Laufzeit einen Fehler verursacht, ermöglicht die Verwendung dieser Funktionen Netzwerkmonitor, den zugeordneten Arbeitsspeicher freizugeben.</span><span class="sxs-lookup"><span data-stu-id="4e8f5-120">If your expert fails during run time, using these functions will allow Network Monitor to free the memory it has allocated.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e8f5-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4e8f5-121">Requirements</span></span>



| <span data-ttu-id="4e8f5-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4e8f5-122">Requirement</span></span> | <span data-ttu-id="4e8f5-123">Wert</span><span class="sxs-lookup"><span data-stu-id="4e8f5-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="4e8f5-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4e8f5-124">Minimum supported client</span></span><br/> | <span data-ttu-id="4e8f5-125">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4e8f5-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="4e8f5-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4e8f5-126">Minimum supported server</span></span><br/> | <span data-ttu-id="4e8f5-127">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4e8f5-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="4e8f5-128">Header</span><span class="sxs-lookup"><span data-stu-id="4e8f5-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="4e8f5-129"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="4e8f5-129"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="4e8f5-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="4e8f5-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="4e8f5-131"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4e8f5-131"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="4e8f5-132">DLL</span><span class="sxs-lookup"><span data-stu-id="4e8f5-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4e8f5-133"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4e8f5-133"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




