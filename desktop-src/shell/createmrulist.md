---
description: Erstellt eine neue MRU-Liste (Most Recently Used).
title: CreateMRUListW-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateMRUListW
- CreateMRUListW
api_type:
- DllExport
api_location:
- Comctl32.dll
ms.assetid: b2d9e3c7-8151-45ef-9658-bd33a87b4c9c
ms.openlocfilehash: 34cd3dd9e5b9e62bbdd13b31d95e7205e4427de6
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109843381"
---
# <a name="createmrulistw-function"></a><span data-ttu-id="5ef5e-103">CreateMRUListW-Funktion</span><span class="sxs-lookup"><span data-stu-id="5ef5e-103">CreateMRUListW function</span></span>

<span data-ttu-id="5ef5e-104">Erstellt eine neue MRU-Liste (Most Recently Used).</span><span class="sxs-lookup"><span data-stu-id="5ef5e-104">Creates a new most recently used (MRU) list.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ef5e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5ef5e-105">Syntax</span></span>


```C++
int CreateMRUListW(
  _In_ LPMRUINFO lpmi
);
```



## <a name="parameters"></a><span data-ttu-id="5ef5e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5ef5e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ef5e-107">*lpmi* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="5ef5e-107">*lpmi* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ef5e-108">Typ: **LPMRUINFO**</span><span class="sxs-lookup"><span data-stu-id="5ef5e-108">Type: **LPMRUINFO**</span></span>

<span data-ttu-id="5ef5e-109">Ein Zeiger auf eine [**MRUINFO-Struktur,**](mruinfo.md) die die MRU-Liste definiert.</span><span class="sxs-lookup"><span data-stu-id="5ef5e-109">A pointer to an [**MRUINFO**](mruinfo.md) structure defining the MRU list.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ef5e-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5ef5e-110">Return value</span></span>

<span data-ttu-id="5ef5e-111">Typ: **int**</span><span class="sxs-lookup"><span data-stu-id="5ef5e-111">Type: **int**</span></span>

<span data-ttu-id="5ef5e-112">Gibt ein Handle für die neue MRU-Liste oder 0 (bei einem Fehler) zurück.</span><span class="sxs-lookup"><span data-stu-id="5ef5e-112">Returns a handle to the new MRU list, or 0 in case of an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="5ef5e-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5ef5e-113">Remarks</span></span>

<span data-ttu-id="5ef5e-114">Diese Funktion ist nicht in einem öffentlichen Header oder einer öffentlichen Bibliothek enthalten.</span><span class="sxs-lookup"><span data-stu-id="5ef5e-114">This function is not included in a public header or library.</span></span> <span data-ttu-id="5ef5e-115">Der Zugriff kann über [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) erfolgen oder aus comctl32.dll durch die Ordnungszahl 400 für **CreateMRUListW** extrahiert werden.</span><span class="sxs-lookup"><span data-stu-id="5ef5e-115">It can be accessed through [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) or extracted from comctl32.dll by its ordinal, which is 400 for **CreateMRUListW**.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ef5e-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5ef5e-116">Requirements</span></span>



| <span data-ttu-id="5ef5e-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5ef5e-117">Requirement</span></span> | <span data-ttu-id="5ef5e-118">Wert</span><span class="sxs-lookup"><span data-stu-id="5ef5e-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ef5e-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5ef5e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="5ef5e-120">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5ef5e-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5ef5e-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5ef5e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="5ef5e-122">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5ef5e-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="5ef5e-123">DLL</span><span class="sxs-lookup"><span data-stu-id="5ef5e-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5ef5e-124"><dt>Comctl32.dll (Version 5.0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="5ef5e-124"><dt>Comctl32.dll (version 5.0 or later)</dt></span></span> </dl> |
| <span data-ttu-id="5ef5e-125">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="5ef5e-125">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="5ef5e-126">**CreateMRUListW** (Unicode)</span><span class="sxs-lookup"><span data-stu-id="5ef5e-126">**CreateMRUListW** (Unicode)</span></span><br/>                                                                        |



 

 
