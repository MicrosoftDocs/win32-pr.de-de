---
UID: ''
title: InterlockedPushListSList-Funktion
description: Fügt eine einzeln verknüpfte Liste an der Vorderseite einer anderen verknüpften Liste ein.
old-location: ''
ms.assetid: na
ms.date: 04/10/2019
ms.keywords: InterlockedPushListSListEx
ms.topic: reference
req.header:
- WinBase.h on Windows Vista, Windows 7, Windows Server 2008 and Windows Server 2008 R2
- InterlockedAPI.h on Windows 8 and Windows Server 2012
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: Kernel32.lib
req.dll: API-MS-Win-Core-interlocked-l1-1-0.dll
req.irql: ''
topic_type:
- APIRef
api_type: ''
api_location:
- API-MS-Win-Core-interlocked-l1-1-0.dll
api_name:
- InterlockedPushListSList
targetos: Windows
req.typenames: ''
req.redist: ''
ms.openlocfilehash: ccecdae3af5119a86594c31856dac11ecb4507bc
ms.sourcegitcommit: be77ed1f97d3be57a2f42070589de21b66034adf
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2020
ms.locfileid: "104390073"
---
# <a name="interlockedpushlistslist-function"></a><span data-ttu-id="5d412-103">InterlockedPushListSList-Funktion</span><span class="sxs-lookup"><span data-stu-id="5d412-103">InterlockedPushListSList function</span></span>

## <a name="description"></a><span data-ttu-id="5d412-104">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5d412-104">Description</span></span>

<span data-ttu-id="5d412-105">Fügt eine einzeln verknüpfte Liste an der Vorderseite einer anderen verknüpften Liste ein.</span><span class="sxs-lookup"><span data-stu-id="5d412-105">Inserts a singly-linked list at the front of another singly linked list.</span></span>
<span data-ttu-id="5d412-106">Der Zugriff auf die Listen wird auf einem Multiprozessorsystem synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="5d412-106">Access to the lists is synchronized on a multiprocessor system.</span></span>

```cpp
PSLIST_ENTRY  FASTCALL InterlockedPushListSList(
  _Inout_ PSLIST_HEADER ListHead,
  _Inout_ PSLIST_ENTRY  List,
  _Inout_ PSLIST_ENTRY  ListEnd,
  _In_    ULONG         Count
);
```

## <a name="parameters"></a><span data-ttu-id="5d412-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="5d412-107">Parameters</span></span>

### <a name="listhead-in-out"></a><span data-ttu-id="5d412-108">Lisder AD [in, out]</span><span class="sxs-lookup"><span data-stu-id="5d412-108">ListHead [in, out]</span></span>

<span data-ttu-id="5d412-109">Ein Zeiger auf eine **SLIST_HEADER** -Struktur, die die Kopfzeile einer einzeln verknüpften Liste darstellt.</span><span class="sxs-lookup"><span data-stu-id="5d412-109">Pointer to an **SLIST_HEADER** structure that represents the head of a singly linked list.</span></span>
<span data-ttu-id="5d412-110">Die Liste, die von den Parametern *List* und *listend* angegeben wird, wird am Anfang der Liste eingefügt.</span><span class="sxs-lookup"><span data-stu-id="5d412-110">The list specified by the *List* and *ListEnd* parameters is inserted at the front of this list.</span></span>

### <a name="list-in-out"></a><span data-ttu-id="5d412-111">List [in, out]</span><span class="sxs-lookup"><span data-stu-id="5d412-111">List [in, out]</span></span>

<span data-ttu-id="5d412-112">Ein Zeiger auf eine [SLIST_ENTRY](/windows/win32/api/winnt/ns-winnt-slist_entry) -Struktur, die das erste Element in der Liste darstellt, das eingefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="5d412-112">Pointer to an [SLIST_ENTRY](/windows/win32/api/winnt/ns-winnt-slist_entry) structure that represents the first item in the list to be inserted.</span></span>

### <a name="listend-in-out"></a><span data-ttu-id="5d412-113">Listend [in, out]</span><span class="sxs-lookup"><span data-stu-id="5d412-113">ListEnd [in, out]</span></span>

<span data-ttu-id="5d412-114">Ein Zeiger auf eine [SLIST_ENTRY](/windows/win32/api/winnt/ns-winnt-slist_entry) -Struktur, die das letzte Element in der Liste darstellt, das eingefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="5d412-114">Pointer to an [SLIST_ENTRY](/windows/win32/api/winnt/ns-winnt-slist_entry) structure that represents the last item in the list to be inserted.</span></span>

### <a name="count-in"></a><span data-ttu-id="5d412-115">Count [in]</span><span class="sxs-lookup"><span data-stu-id="5d412-115">Count [in]</span></span>

<span data-ttu-id="5d412-116">Die Anzahl der Elemente in der Liste, die eingefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="5d412-116">The number of items in the list to be inserted.</span></span>

## <a name="returns"></a><span data-ttu-id="5d412-117">Gibt zurück</span><span class="sxs-lookup"><span data-stu-id="5d412-117">Returns</span></span>

<span data-ttu-id="5d412-118">Der Rückgabewert ist das vorherige erste Element in der Liste, die durch den *listead* -Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="5d412-118">The return value is the previous first item in the list specified by the *ListHead* parameter.</span></span>
<span data-ttu-id="5d412-119">Wenn die Liste zuvor leer war, ist der Rückgabewert **null**.</span><span class="sxs-lookup"><span data-stu-id="5d412-119">If the list was previously empty, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="5d412-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5d412-120">Remarks</span></span>

<span data-ttu-id="5d412-121">Alle Listenelemente müssen an einer **MEMORY_ALLOCATION_ALIGNMENT** Grenze ausgerichtet werden. Andernfalls verhält sich diese Funktion unvorhersehbar.</span><span class="sxs-lookup"><span data-stu-id="5d412-121">All list items must be aligned on a **MEMORY_ALLOCATION_ALIGNMENT** boundary; otherwise, this function will behave unpredictably.</span></span>
<span data-ttu-id="5d412-122">Siehe **_aligned_malloc**.</span><span class="sxs-lookup"><span data-stu-id="5d412-122">See **_aligned_malloc**.</span></span>

<span data-ttu-id="5d412-123">**Windows 8 und Windows Server 2012:**  Diese Funktion wurde durch [interlockedpushlistslistex](/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedpushlistslistex)ersetzt.</span><span class="sxs-lookup"><span data-stu-id="5d412-123">**Windows 8 and Windows Server 2012:**  This function has been superceded by [InterlockedPushListSListEx](/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedpushlistslistex).</span></span>
<span data-ttu-id="5d412-124">Bei der Kompilierung mit **NTDDI_VERSION** auf **NTDDI_WIN8** oder höher festgelegt, werden Aufrufe von **interlockedpushlistslist** stattdessen an **interlockedpushlistslistex** weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="5d412-124">When compiling with **NTDDI_VERSION** set to **NTDDI_WIN8** or greater, calls to **InterlockedPushListSList** will go to **InterlockedPushListSListEx** instead.</span></span>

## <a name="see-also"></a><span data-ttu-id="5d412-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5d412-125">See also</span></span>

[<span data-ttu-id="5d412-126">Miteinander verknüpfte, einzeln verknüpfte Listen</span><span class="sxs-lookup"><span data-stu-id="5d412-126">Interlocked Singly Linked Lists</span></span>](/windows/desktop/Sync/interlocked-singly-linked-lists)

[<span data-ttu-id="5d412-127">Interlockedpopentryslist</span><span class="sxs-lookup"><span data-stu-id="5d412-127">InterlockedPopEntrySList</span></span>](/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedpopentryslist)

[<span data-ttu-id="5d412-128">Interlockedpushentryslist</span><span class="sxs-lookup"><span data-stu-id="5d412-128">InterlockedPushEntrySList</span></span>](/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedpushentryslist)

[<span data-ttu-id="5d412-129">Interlockedpushlistslistex</span><span class="sxs-lookup"><span data-stu-id="5d412-129">InterlockedPushListSListEx</span></span>](/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedpushlistslistex)

[<span data-ttu-id="5d412-130">Interlockedflushslist</span><span class="sxs-lookup"><span data-stu-id="5d412-130">InterlockedFlushSList</span></span>](/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedflushslist)

[<span data-ttu-id="5d412-131">SLIST_ENTRY</span><span class="sxs-lookup"><span data-stu-id="5d412-131">SLIST_ENTRY</span></span>](/windows/win32/api/winnt/ns-winnt-slist_entry)

[<span data-ttu-id="5d412-132">Verwenden von einzeln verknüpften Listen</span><span class="sxs-lookup"><span data-stu-id="5d412-132">Using Singly Linked Lists</span></span>](/windows/desktop/Sync/using-singly-linked-lists)
