---
description: Wird verwendet, um zu bestimmen, ob ein Element in einer LISTE der zuletzt verwendeten Elemente (MRU) vorhanden ist.
title: MRUCMPPROC-Rückruffunktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MRUCMPPROC
- MRUCMPPROCA
- MRUCMPPROCW
api_type:
- UserDefined
api_location: ''
ms.assetid: 00f31d6b-2a96-4abd-9647-24a6e66aa22f
ms.openlocfilehash: 83020fbcd0d4cfcfbc643d1360e3671595de6f32
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109840781"
---
# <a name="mrucmpproc-callback-function"></a><span data-ttu-id="0f7af-103">MRUCMPPROC-Rückruffunktion</span><span class="sxs-lookup"><span data-stu-id="0f7af-103">MRUCMPPROC callback function</span></span>

<span data-ttu-id="0f7af-104">Wird verwendet, um zu bestimmen, ob ein Element in einer LISTE der zuletzt verwendeten Elemente (MRU) vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="0f7af-104">Used to determine whether an item is present in a most recently used (MRU) list.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f7af-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0f7af-105">Syntax</span></span>


```C++
int CALLBACK MRUCMPPROC(
   LPCTSTR pString1,
   LPCTSTR pString2
);
```



## <a name="parameters"></a><span data-ttu-id="0f7af-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0f7af-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f7af-107">*pString1*</span><span class="sxs-lookup"><span data-stu-id="0f7af-107">*pString1*</span></span> 
</dt> <dd>

<span data-ttu-id="0f7af-108">Typ: **LPCTSTR**</span><span class="sxs-lookup"><span data-stu-id="0f7af-108">Type: **LPCTSTR**</span></span>

<span data-ttu-id="0f7af-109">Die erste Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="0f7af-109">The first string.</span></span>

</dd> <dt>

<span data-ttu-id="0f7af-110">*pString2*</span><span class="sxs-lookup"><span data-stu-id="0f7af-110">*pString2*</span></span> 
</dt> <dd>

<span data-ttu-id="0f7af-111">Typ: **LPCTSTR**</span><span class="sxs-lookup"><span data-stu-id="0f7af-111">Type: **LPCTSTR**</span></span>

<span data-ttu-id="0f7af-112">Eine zweite Zeichenfolge, die mit der ersten verglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="0f7af-112">A second string to compare to the first.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f7af-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0f7af-113">Return value</span></span>

<span data-ttu-id="0f7af-114">Typ: **int**</span><span class="sxs-lookup"><span data-stu-id="0f7af-114">Type: **int**</span></span>

<span data-ttu-id="0f7af-115">Gibt 0 zurück, wenn die Elemente identisch sind, andernfalls ein Wert ungleich 0.</span><span class="sxs-lookup"><span data-stu-id="0f7af-115">Returns 0 if the items are identical, a nonzero value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="0f7af-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0f7af-116">Remarks</span></span>

<span data-ttu-id="0f7af-117">Diese Funktion kann optional für die Verwendung in der [**MRUINFO-Struktur**](mruinfo.md) angegeben werden, die an [**CreateMRUListW übergeben wird.**](createmrulist.md)</span><span class="sxs-lookup"><span data-stu-id="0f7af-117">This function can be optionally specified for use in the [**MRUINFO**](mruinfo.md) structure passed to [**CreateMRUListW**](createmrulist.md).</span></span> <span data-ttu-id="0f7af-118">Dies ist nützlich, wenn die MRU-Liste mit dem **MRU \_ BINARY-Flag erstellt** wurde.</span><span class="sxs-lookup"><span data-stu-id="0f7af-118">This is useful when the MRU list was created with the **MRU\_BINARY** flag.</span></span> <span data-ttu-id="0f7af-119">Wenn diese Funktion nicht angegeben wird, werden Standardfunktionen für den Zeichenfolgenvergleich verwendet.</span><span class="sxs-lookup"><span data-stu-id="0f7af-119">When this function is not specified, standard string comparison functions are used.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f7af-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0f7af-120">Requirements</span></span>



| <span data-ttu-id="0f7af-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0f7af-121">Requirement</span></span> | <span data-ttu-id="0f7af-122">Wert</span><span class="sxs-lookup"><span data-stu-id="0f7af-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="0f7af-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0f7af-123">Minimum supported client</span></span><br/> | <span data-ttu-id="0f7af-124">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0f7af-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>      |
| <span data-ttu-id="0f7af-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0f7af-125">Minimum supported server</span></span><br/> | <span data-ttu-id="0f7af-126">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0f7af-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="0f7af-127">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="0f7af-127">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="0f7af-128">**MRUCMPPROCW** (Unicode) und **MRUCMPPROCA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="0f7af-128">**MRUCMPPROCW** (Unicode) and **MRUCMPPROCA** (ANSI)</span></span><br/> |



 

 




