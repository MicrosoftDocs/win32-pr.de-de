---
description: Wird verwendet, um zu bestimmen, ob ein Element in einer zuletzt verwendeten (MRU-) Liste vorhanden ist.
title: Mrucmpproc-Rückruffunktion
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
ms.openlocfilehash: f95856f6508ad728a15b3df3d6f5eafa4f5bd2ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959124"
---
# <a name="mrucmpproc-callback-function"></a><span data-ttu-id="17393-103">Mrucmpproc-Rückruffunktion</span><span class="sxs-lookup"><span data-stu-id="17393-103">MRUCMPPROC callback function</span></span>

<span data-ttu-id="17393-104">Wird verwendet, um zu bestimmen, ob ein Element in einer zuletzt verwendeten (MRU-) Liste vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="17393-104">Used to determine whether an item is present in a most recently used (MRU) list.</span></span>

## <a name="syntax"></a><span data-ttu-id="17393-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="17393-105">Syntax</span></span>


```C++
int CALLBACK MRUCMPPROC(
   LPCTSTR pString1,
   LPCTSTR pString2
);
```



## <a name="parameters"></a><span data-ttu-id="17393-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="17393-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17393-107">*pString1*</span><span class="sxs-lookup"><span data-stu-id="17393-107">*pString1*</span></span> 
</dt> <dd>

<span data-ttu-id="17393-108">Typ: **LPCTSTR**</span><span class="sxs-lookup"><span data-stu-id="17393-108">Type: **LPCTSTR**</span></span>

<span data-ttu-id="17393-109">Die erste Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="17393-109">The first string.</span></span>

</dd> <dt>

<span data-ttu-id="17393-110">*pString2*</span><span class="sxs-lookup"><span data-stu-id="17393-110">*pString2*</span></span> 
</dt> <dd>

<span data-ttu-id="17393-111">Typ: **LPCTSTR**</span><span class="sxs-lookup"><span data-stu-id="17393-111">Type: **LPCTSTR**</span></span>

<span data-ttu-id="17393-112">Eine zweite Zeichenfolge, die mit der ersten verglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="17393-112">A second string to compare to the first.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17393-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="17393-113">Return value</span></span>

<span data-ttu-id="17393-114">Typ: **int**</span><span class="sxs-lookup"><span data-stu-id="17393-114">Type: **int**</span></span>

<span data-ttu-id="17393-115">Gibt 0 zurück, wenn die Elemente identisch sind, andernfalls ein Wert ungleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="17393-115">Returns 0 if the items are identical, a nonzero value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="17393-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="17393-116">Remarks</span></span>

<span data-ttu-id="17393-117">Diese Funktion kann optional für die Verwendung in der [**mruinfo**](mruinfo.md) -Struktur angegeben werden, die an " [**kreatemrulistw**](createmrulist.md)" übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="17393-117">This function can be optionally specified for use in the [**MRUINFO**](mruinfo.md) structure passed to [**CreateMRUListW**](createmrulist.md).</span></span> <span data-ttu-id="17393-118">Dies ist hilfreich, wenn die MRU-Liste mit dem **MRU- \_ Binärflag** erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="17393-118">This is useful when the MRU list was created with the **MRU\_BINARY** flag.</span></span> <span data-ttu-id="17393-119">Wenn diese Funktion nicht angegeben wird, werden standardmäßige Zeichen folgen Vergleichsfunktionen verwendet.</span><span class="sxs-lookup"><span data-stu-id="17393-119">When this function is not specified, standard string comparison functions are used.</span></span>

## <a name="requirements"></a><span data-ttu-id="17393-120">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="17393-120">Requirements</span></span>



| <span data-ttu-id="17393-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="17393-121">Requirement</span></span> | <span data-ttu-id="17393-122">Wert</span><span class="sxs-lookup"><span data-stu-id="17393-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="17393-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="17393-123">Minimum supported client</span></span><br/> | <span data-ttu-id="17393-124">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="17393-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>      |
| <span data-ttu-id="17393-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="17393-125">Minimum supported server</span></span><br/> | <span data-ttu-id="17393-126">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="17393-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="17393-127">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="17393-127">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="17393-128">**Mrucmpprocw** (Unicode) und **mrucmpproca** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="17393-128">**MRUCMPPROCW** (Unicode) and **MRUCMPPROCA** (ANSI)</span></span><br/> |



 

 




