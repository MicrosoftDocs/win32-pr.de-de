---
description: Erstellt eine neue Liste der zuletzt verwendeten (MRU).
title: Funktion "anatemrulistw"
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
ms.openlocfilehash: 572e52f1461e3d48ab9eba1aa903c7fb690636d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750248"
---
# <a name="createmrulistw-function"></a><span data-ttu-id="4cabc-103">Funktion "anatemrulistw"</span><span class="sxs-lookup"><span data-stu-id="4cabc-103">CreateMRUListW function</span></span>

<span data-ttu-id="4cabc-104">Erstellt eine neue Liste der zuletzt verwendeten (MRU).</span><span class="sxs-lookup"><span data-stu-id="4cabc-104">Creates a new most recently used (MRU) list.</span></span>

## <a name="syntax"></a><span data-ttu-id="4cabc-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4cabc-105">Syntax</span></span>


```C++
int CreateMRUListW(
  _In_ LPMRUINFO lpmi
);
```



## <a name="parameters"></a><span data-ttu-id="4cabc-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4cabc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4cabc-107">*lpmi* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4cabc-107">*lpmi* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4cabc-108">Typ: **lpmruinfo**</span><span class="sxs-lookup"><span data-stu-id="4cabc-108">Type: **LPMRUINFO**</span></span>

<span data-ttu-id="4cabc-109">Ein Zeiger auf eine [**mruinfo**](mruinfo.md) -Struktur, die die MRU-Liste definiert.</span><span class="sxs-lookup"><span data-stu-id="4cabc-109">A pointer to an [**MRUINFO**](mruinfo.md) structure defining the MRU list.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4cabc-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4cabc-110">Return value</span></span>

<span data-ttu-id="4cabc-111">Typ: **int**</span><span class="sxs-lookup"><span data-stu-id="4cabc-111">Type: **int**</span></span>

<span data-ttu-id="4cabc-112">Gibt ein Handle für die neue MRU-Liste oder bei einem Fehler 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="4cabc-112">Returns a handle to the new MRU list, or 0 in case of an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="4cabc-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4cabc-113">Remarks</span></span>

<span data-ttu-id="4cabc-114">Diese Funktion ist nicht in einem öffentlichen Header oder einer Bibliothek enthalten.</span><span class="sxs-lookup"><span data-stu-id="4cabc-114">This function is not included in a public header or library.</span></span> <span data-ttu-id="4cabc-115">Der Zugriff darauf erfolgt über [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) oder das Extrahieren aus comctl32.dll durch die Ordnungszahl, die 400 für " **featemrulistw**" ist.</span><span class="sxs-lookup"><span data-stu-id="4cabc-115">It can be accessed through [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) or extracted from comctl32.dll by its ordinal, which is 400 for **CreateMRUListW**.</span></span>

## <a name="requirements"></a><span data-ttu-id="4cabc-116">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="4cabc-116">Requirements</span></span>



| <span data-ttu-id="4cabc-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4cabc-117">Requirement</span></span> | <span data-ttu-id="4cabc-118">Wert</span><span class="sxs-lookup"><span data-stu-id="4cabc-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4cabc-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4cabc-119">Minimum supported client</span></span><br/> | <span data-ttu-id="4cabc-120">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4cabc-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="4cabc-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4cabc-121">Minimum supported server</span></span><br/> | <span data-ttu-id="4cabc-122">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4cabc-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="4cabc-123">DLL</span><span class="sxs-lookup"><span data-stu-id="4cabc-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4cabc-124"><dt>Comctl32.dll (Version 5,0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="4cabc-124"><dt>Comctl32.dll (version 5.0 or later)</dt></span></span> </dl> |
| <span data-ttu-id="4cabc-125">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="4cabc-125">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="4cabc-126">" **Anatemrulistw** " (Unicode)</span><span class="sxs-lookup"><span data-stu-id="4cabc-126">**CreateMRUListW** (Unicode)</span></span><br/>                                                                        |



 

 
