---
description: Die Funktion "expertmemorysize" gibt die Menge an Arbeitsspeicher zurück, die von der Funktion "expertenlocmemory" zugeordnet wird.
ms.assetid: 60d3f33d-dc03-4c39-98fa-ec093398b51b
title: Expertmemorysize-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExpertMemorySize
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 57c83bc3e9535550086c9732b33a71a357e4da42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862019"
---
# <a name="expertmemorysize-function"></a><span data-ttu-id="7aa32-103">Expertmemorysize-Funktion</span><span class="sxs-lookup"><span data-stu-id="7aa32-103">ExpertMemorySize function</span></span>

<span data-ttu-id="7aa32-104">Die Funktion " **expertmemorysize** " gibt die Menge an Arbeitsspeicher zurück, die von der Funktion " [expertenlocmemory](expertallocmemory.md) " zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="7aa32-104">The **ExpertMemorySize** function returns the amount of memory allocated by the [ExpertAllocMemory](expertallocmemory.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="7aa32-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7aa32-105">Syntax</span></span>


```C++
SIZE_T WINAPI ExpertMemorySize(
  _In_ HEXPERTKEY hExpertKey,
  _In_ LPVOID     pOriginalMemory
);
```



## <a name="parameters"></a><span data-ttu-id="7aa32-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7aa32-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7aa32-107">*hexpertkey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7aa32-107">*hExpertKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7aa32-108">Eindeutige expertenkennung.</span><span class="sxs-lookup"><span data-stu-id="7aa32-108">Unique expert identifier.</span></span> <span data-ttu-id="7aa32-109">Netzwerkmonitor übergibt *hexpertkey* an den Experten, wenn die Funktion [Run](run.md) aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="7aa32-109">Network Monitor passes *hExpertKey* to the expert when it calls the [Run](run.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="7aa32-110">*poriginalmemory* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7aa32-110">*pOriginalMemory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7aa32-111">Ein Zeiger auf die Speicheradresse des von " [sachtallocmemory](expertallocmemory.md)" zugewiesenen Experten.</span><span class="sxs-lookup"><span data-stu-id="7aa32-111">Pointer to the memory address of the expert allocated by [ExpertAllocMemory](expertallocmemory.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7aa32-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7aa32-112">Return value</span></span>

<span data-ttu-id="7aa32-113">Die-Funktion gibt die Menge an zugeordnetem Arbeitsspeicher in Bytes zurück.</span><span class="sxs-lookup"><span data-stu-id="7aa32-113">The function returns the amount of allocated memory   in bytes.</span></span>

## <a name="remarks"></a><span data-ttu-id="7aa32-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7aa32-114">Remarks</span></span>

<span data-ttu-id="7aa32-115">Informationen über den Datentyp " **size \_ T** ", der von " **expertenmemorysize** " zurückgegeben wird, finden Sie unter Datentypen.</span><span class="sxs-lookup"><span data-stu-id="7aa32-115">For information on the **SIZE\_T** data type that **ExpertMemorySize** returns, see Data Types.</span></span>

## <a name="requirements"></a><span data-ttu-id="7aa32-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7aa32-116">Requirements</span></span>



| <span data-ttu-id="7aa32-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7aa32-117">Requirement</span></span> | <span data-ttu-id="7aa32-118">Wert</span><span class="sxs-lookup"><span data-stu-id="7aa32-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="7aa32-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7aa32-119">Minimum supported client</span></span><br/> | <span data-ttu-id="7aa32-120">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7aa32-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="7aa32-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7aa32-121">Minimum supported server</span></span><br/> | <span data-ttu-id="7aa32-122">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7aa32-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="7aa32-123">Header</span><span class="sxs-lookup"><span data-stu-id="7aa32-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="7aa32-124"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="7aa32-124"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="7aa32-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="7aa32-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="7aa32-126"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7aa32-126"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="7aa32-127">DLL</span><span class="sxs-lookup"><span data-stu-id="7aa32-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7aa32-128"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7aa32-128"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




