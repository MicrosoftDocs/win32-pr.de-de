---
description: Fügt am Anfang der Liste der zuletzt verwendeten (MRU) eine Zeichenfolge hinzu.
title: Addmrustringw-Funktion
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
ms.openlocfilehash: 0d0d65187105f4ad844b349c6ac60b030c464716
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041618"
---
# <a name="addmrustringw-function"></a><span data-ttu-id="426ac-103">Addmrustringw-Funktion</span><span class="sxs-lookup"><span data-stu-id="426ac-103">AddMRUStringW function</span></span>

<span data-ttu-id="426ac-104">\[Diese Funktion ist über Windows XP mit Service Pack 2 (SP2) und Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="426ac-104">\[This function is available through Windows XP with Service Pack 2 (SP2) and Windows Server 2003.</span></span> <span data-ttu-id="426ac-105">Sie wird möglicherweise in nachfolgenden Versionen von Windows geändert oder ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="426ac-105">It might be altered or unavailable in subsequent versions of Windows.</span></span> <span data-ttu-id="426ac-106">\]</span><span class="sxs-lookup"><span data-stu-id="426ac-106">\]</span></span>

<span data-ttu-id="426ac-107">Fügt am Anfang der Liste der zuletzt verwendeten (MRU) eine Zeichenfolge hinzu.</span><span class="sxs-lookup"><span data-stu-id="426ac-107">Adds a string to the top of the most recently used (MRU) list.</span></span>

## <a name="syntax"></a><span data-ttu-id="426ac-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="426ac-108">Syntax</span></span>


```C++
int AddMRUStringW(
  _In_ HANDLE  hMRU,
  _In_ LPCTSTR szString
);
```



## <a name="parameters"></a><span data-ttu-id="426ac-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="426ac-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="426ac-110">*hmru* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="426ac-110">*hMRU* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="426ac-111">Typ: **handle**</span><span class="sxs-lookup"><span data-stu-id="426ac-111">Type: **HANDLE**</span></span>

<span data-ttu-id="426ac-112">Das Handle der MRU-Liste.</span><span class="sxs-lookup"><span data-stu-id="426ac-112">The handle of the MRU list.</span></span>

</dd> <dt>

<span data-ttu-id="426ac-113">*szString* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="426ac-113">*szString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="426ac-114">Typ: **LPCTSTR**</span><span class="sxs-lookup"><span data-stu-id="426ac-114">Type: **LPCTSTR**</span></span>

<span data-ttu-id="426ac-115">Ein Zeiger auf die Daten.</span><span class="sxs-lookup"><span data-stu-id="426ac-115">A pointer to the data.</span></span> <span data-ttu-id="426ac-116">Dabei kann es sich entweder um eine Zeichenfolge handeln oder, wenn die MRU-Liste mit dem **MRU- \_ Binärflag** erstellt wurde, Binärdaten.</span><span class="sxs-lookup"><span data-stu-id="426ac-116">This can be either a string or, if the MRU list was created with the **MRU\_BINARY** flag, binary data.</span></span> <span data-ttu-id="426ac-117">Im Fall von Binärdaten gibt das erste **DWORD** die Größe an.</span><span class="sxs-lookup"><span data-stu-id="426ac-117">In the case of binary data, the first **DWORD** indicates its size.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="426ac-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="426ac-118">Return value</span></span>

<span data-ttu-id="426ac-119">Typ: **int**</span><span class="sxs-lookup"><span data-stu-id="426ac-119">Type: **int**</span></span>

<span data-ttu-id="426ac-120">Gibt bei erfolgreicher Ausführung einen nicht negativen Wert zurück, andernfalls-1.</span><span class="sxs-lookup"><span data-stu-id="426ac-120">Returns a non-negative value if successful, -1 otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="426ac-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="426ac-121">Remarks</span></span>

<span data-ttu-id="426ac-122">Diese Funktion ist nicht in einem öffentlichen Header oder einer Bibliothek enthalten.</span><span class="sxs-lookup"><span data-stu-id="426ac-122">This function is not included in a public header or library.</span></span> <span data-ttu-id="426ac-123">Der Zugriff darauf erfolgt über [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) oder das Extrahieren aus comctl32.dll durch die Ordnungszahl, die 401 für **addmrustringw** ist.</span><span class="sxs-lookup"><span data-stu-id="426ac-123">It can be accessed through [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) or extracted from comctl32.dll by its ordinal, which is 401 for **AddMRUStringW**.</span></span>

## <a name="requirements"></a><span data-ttu-id="426ac-124">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="426ac-124">Requirements</span></span>



| <span data-ttu-id="426ac-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="426ac-125">Requirement</span></span> | <span data-ttu-id="426ac-126">Wert</span><span class="sxs-lookup"><span data-stu-id="426ac-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="426ac-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="426ac-127">Minimum supported client</span></span><br/> | <span data-ttu-id="426ac-128">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="426ac-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="426ac-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="426ac-129">Minimum supported server</span></span><br/> | <span data-ttu-id="426ac-130">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="426ac-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="426ac-131">DLL</span><span class="sxs-lookup"><span data-stu-id="426ac-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="426ac-132"><dt>Comctl32.dll (Version 5,0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="426ac-132"><dt>Comctl32.dll (version 5.0 or later)</dt></span></span> </dl> |
| <span data-ttu-id="426ac-133">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="426ac-133">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="426ac-134">**Addmrustringw** (Unicode)</span><span class="sxs-lookup"><span data-stu-id="426ac-134">**AddMRUStringW** (Unicode)</span></span><br/>                                                                         |



 

