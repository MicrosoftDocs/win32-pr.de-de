---
description: Fügt am Anfang der Liste der zuletzt verwendeten (MRU) eine Zeichenfolge hinzu.
title: AddMRUStringW-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddMRUStringW
- AddMRUStringW
api_type:
- DllExport
api_location:
- Comctl32.dll
ms.assetid: ad94a442-8492-412c-a4f2-ac6e7c5327d7
ms.openlocfilehash: b62e23cd0604273559e36e561970dd62f117c11d
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841191"
---
# <a name="addmrustringw-function"></a><span data-ttu-id="bc51c-103">AddMRUStringW-Funktion</span><span class="sxs-lookup"><span data-stu-id="bc51c-103">AddMRUStringW function</span></span>

<span data-ttu-id="bc51c-104">\[Diese Funktion ist über Windows XP mit Service Pack 2 (SP2) und Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="bc51c-104">\[This function is available through Windows XP with Service Pack 2 (SP2) and Windows Server 2003.</span></span> <span data-ttu-id="bc51c-105">Sie kann in nachfolgenden Versionen von Windows geändert oder nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="bc51c-105">It might be altered or unavailable in subsequent versions of Windows.</span></span> <span data-ttu-id="bc51c-106">\]</span><span class="sxs-lookup"><span data-stu-id="bc51c-106">\]</span></span>

<span data-ttu-id="bc51c-107">Fügt am Anfang der Liste der zuletzt verwendeten (MRU) eine Zeichenfolge hinzu.</span><span class="sxs-lookup"><span data-stu-id="bc51c-107">Adds a string to the top of the most recently used (MRU) list.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc51c-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="bc51c-108">Syntax</span></span>


```C++
int AddMRUStringW(
  _In_ HANDLE  hMRU,
  _In_ LPCTSTR szString
);
```



## <a name="parameters"></a><span data-ttu-id="bc51c-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="bc51c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc51c-110">*hMRU* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="bc51c-110">*hMRU* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc51c-111">Typ: **HANDLE**</span><span class="sxs-lookup"><span data-stu-id="bc51c-111">Type: **HANDLE**</span></span>

<span data-ttu-id="bc51c-112">Das Handle der MRU-Liste.</span><span class="sxs-lookup"><span data-stu-id="bc51c-112">The handle of the MRU list.</span></span>

</dd> <dt>

<span data-ttu-id="bc51c-113">*szString* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="bc51c-113">*szString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc51c-114">Typ: **LPCTSTR**</span><span class="sxs-lookup"><span data-stu-id="bc51c-114">Type: **LPCTSTR**</span></span>

<span data-ttu-id="bc51c-115">Ein Zeiger auf die Daten.</span><span class="sxs-lookup"><span data-stu-id="bc51c-115">A pointer to the data.</span></span> <span data-ttu-id="bc51c-116">Dies kann entweder eine Zeichenfolge oder binäre Daten sein, wenn die MRU-Liste mit dem **MRU \_ BINARY-Flag** erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="bc51c-116">This can be either a string or, if the MRU list was created with the **MRU\_BINARY** flag, binary data.</span></span> <span data-ttu-id="bc51c-117">Bei binären Daten gibt das erste **DWORD** seine Größe an.</span><span class="sxs-lookup"><span data-stu-id="bc51c-117">In the case of binary data, the first **DWORD** indicates its size.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc51c-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bc51c-118">Return value</span></span>

<span data-ttu-id="bc51c-119">Typ: **int**</span><span class="sxs-lookup"><span data-stu-id="bc51c-119">Type: **int**</span></span>

<span data-ttu-id="bc51c-120">Gibt bei Erfolg einen nicht negativen Wert zurück, andernfalls -1.</span><span class="sxs-lookup"><span data-stu-id="bc51c-120">Returns a non-negative value if successful, -1 otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="bc51c-121">Hinweise</span><span class="sxs-lookup"><span data-stu-id="bc51c-121">Remarks</span></span>

<span data-ttu-id="bc51c-122">Diese Funktion ist nicht in einem öffentlichen Header oder einer öffentlichen Bibliothek enthalten.</span><span class="sxs-lookup"><span data-stu-id="bc51c-122">This function is not included in a public header or library.</span></span> <span data-ttu-id="bc51c-123">Der Zugriff kann über [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) erfolgen oder aus comctl32.dll durch die Ordnungszahl 401 für **AddMRUStringW** extrahiert werden.</span><span class="sxs-lookup"><span data-stu-id="bc51c-123">It can be accessed through [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) or extracted from comctl32.dll by its ordinal, which is 401 for **AddMRUStringW**.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc51c-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bc51c-124">Requirements</span></span>



| <span data-ttu-id="bc51c-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bc51c-125">Requirement</span></span> | <span data-ttu-id="bc51c-126">Wert</span><span class="sxs-lookup"><span data-stu-id="bc51c-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc51c-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bc51c-127">Minimum supported client</span></span><br/> | <span data-ttu-id="bc51c-128">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bc51c-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="bc51c-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bc51c-129">Minimum supported server</span></span><br/> | <span data-ttu-id="bc51c-130">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bc51c-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="bc51c-131">DLL</span><span class="sxs-lookup"><span data-stu-id="bc51c-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bc51c-132"><dt>Comctl32.dll (Version 5.0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="bc51c-132"><dt>Comctl32.dll (version 5.0 or later)</dt></span></span> </dl> |
| <span data-ttu-id="bc51c-133">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="bc51c-133">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="bc51c-134">**AddMRUStringW** (Unicode)</span><span class="sxs-lookup"><span data-stu-id="bc51c-134">**AddMRUStringW** (Unicode)</span></span><br/>                                                                         |



 

