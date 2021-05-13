---
description: Enthält Informationen, die eine neue LISTE der zuletzt verwendeten (MRU) definieren. Wird von CreateMRUListW verwendet.
title: MRUINFO-Struktur
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _MRUINFO
- MRUINFOA
- MRUINFOW
api_type:
- NA
api_location: ''
ms.assetid: 31d5831d-9a19-4bd9-8439-ce844966c414
ms.openlocfilehash: 652168e6a4e61ac754aac3202e0681ec6b7d9e66
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109840761"
---
# <a name="mruinfo-structure"></a><span data-ttu-id="64af1-104">MRUINFO-Struktur</span><span class="sxs-lookup"><span data-stu-id="64af1-104">MRUINFO structure</span></span>

<span data-ttu-id="64af1-105">Enthält Informationen, die eine neue LISTE der zuletzt verwendeten (MRU) definieren.</span><span class="sxs-lookup"><span data-stu-id="64af1-105">Contains information that defines a new most recently used (MRU) list.</span></span> <span data-ttu-id="64af1-106">Wird von [**CreateMRUListW verwendet.**](createmrulist.md)</span><span class="sxs-lookup"><span data-stu-id="64af1-106">Used by [**CreateMRUListW**](createmrulist.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="64af1-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="64af1-107">Syntax</span></span>


```C++
typedef struct {
  DWORD      cbSize;
  UINT       uMax;
  UINT       fFlags;
  HKEY       hKey;
  LPCTSTR    lpszSubKey;
  MRUCMPPROC lpfnCompare;
} _MRUINFO;
```



## <a name="members"></a><span data-ttu-id="64af1-108">Member</span><span class="sxs-lookup"><span data-stu-id="64af1-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="64af1-109">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="64af1-109">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="64af1-110">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="64af1-110">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="64af1-111">Die Größe der -Struktur.</span><span class="sxs-lookup"><span data-stu-id="64af1-111">The size of the structure.</span></span>

</dd> <dt>

<span data-ttu-id="64af1-112">**Umax**</span><span class="sxs-lookup"><span data-stu-id="64af1-112">**uMax**</span></span>
</dt> <dd>

<span data-ttu-id="64af1-113">Typ: **UINT**</span><span class="sxs-lookup"><span data-stu-id="64af1-113">Type: **UINT**</span></span>

</dd> <dd>

<span data-ttu-id="64af1-114">Die maximale Anzahl von Einträgen in der MRU-Liste.</span><span class="sxs-lookup"><span data-stu-id="64af1-114">The maximum number of entries in the MRU list.</span></span>

</dd> <dt>

<span data-ttu-id="64af1-115">**fFlags**</span><span class="sxs-lookup"><span data-stu-id="64af1-115">**fFlags**</span></span>
</dt> <dd>

<span data-ttu-id="64af1-116">Typ: **UINT**</span><span class="sxs-lookup"><span data-stu-id="64af1-116">Type: **UINT**</span></span>

</dd> <dd>

<span data-ttu-id="64af1-117">Mindestens eines der folgenden Flags.</span><span class="sxs-lookup"><span data-stu-id="64af1-117">One or more of the following flags.</span></span>

<dt>

<span id="MRU_BINARY"></span><span id="mru_binary"></span>

<span data-ttu-id="64af1-118"><span id="MRU_BINARY"></span><span id="mru_binary"></span>**MRU \_ BINARY** (0x0001)</span><span class="sxs-lookup"><span data-stu-id="64af1-118"><span id="MRU_BINARY"></span><span id="mru_binary"></span>**MRU\_BINARY** (0x0001)</span></span>


</dt> <dd>

<span data-ttu-id="64af1-119">Daten werden in der Registrierung als Binärdaten und nicht als Zeichenfolgendaten gespeichert.</span><span class="sxs-lookup"><span data-stu-id="64af1-119">Data is stored in the registry as binary data rather than string data.</span></span>

</dd> <dt>

<span id="MRU_CACHEWRITE"></span><span id="mru_cachewrite"></span>

<span data-ttu-id="64af1-120"><span id="MRU_CACHEWRITE"></span><span id="mru_cachewrite"></span>**MRU \_ CACHEWRITE** (0x0002)</span><span class="sxs-lookup"><span data-stu-id="64af1-120"><span id="MRU_CACHEWRITE"></span><span id="mru_cachewrite"></span>**MRU\_CACHEWRITE** (0x0002)</span></span>


</dt> <dd>

<span data-ttu-id="64af1-121">Schreiben Sie Änderungen an der in der Registrierung gespeicherten MRU-Version nur, wenn ein neues Element hinzugefügt oder die Ressourcen der MRU-Liste aus dem Arbeitsspeicher frei werden.</span><span class="sxs-lookup"><span data-stu-id="64af1-121">Write changes to the version of the MRU stored in the registry only when a new item is added or the MRU list's resources are freed from memory.</span></span> <span data-ttu-id="64af1-122">Beachten Sie, dass die aktive Version der MRU im Arbeitsspeicher sofort aktualisiert wird, wenn sich der Inhalt oder die Reihenfolge ändert.</span><span class="sxs-lookup"><span data-stu-id="64af1-122">Note that the active version of the MRU in memory is updated immediately in response to any change in contents or ordering.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="64af1-123">**Hkey**</span><span class="sxs-lookup"><span data-stu-id="64af1-123">**hKey**</span></span>
</dt> <dd>

<span data-ttu-id="64af1-124">Typ: **HKEY**</span><span class="sxs-lookup"><span data-stu-id="64af1-124">Type: **HKEY**</span></span>

</dd> <dd>

<span data-ttu-id="64af1-125">Ein Handle für den derzeit geöffneten Schlüssel oder einen der folgenden vordefinierten Werte, unter denen die MRU-Daten gespeichert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="64af1-125">A handle to the currently open key, or one of the following predefined values under which to store the MRU data.</span></span>

<dl><span id="HKEY_CURRENT_USER"></span><span id="hkey_current_user"></span><dt>

<span data-ttu-id="64af1-126">**AKTUELLER \_ \_ HKEY-BENUTZER**</span><span class="sxs-lookup"><span data-stu-id="64af1-126">**HKEY\_CURRENT\_USER**</span></span>
</dt><span id="HKEY_LOCAL_MACHINE"></span><span id="hkey_local_machine"></span><dt>

<span data-ttu-id="64af1-127">**HKEY \_ LOCAL \_ MACHINE**</span><span class="sxs-lookup"><span data-stu-id="64af1-127">**HKEY\_LOCAL\_MACHINE**</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="64af1-128">**lpszSubKey**</span><span class="sxs-lookup"><span data-stu-id="64af1-128">**lpszSubKey**</span></span>
</dt> <dd>

<span data-ttu-id="64af1-129">Typ: **LPCTSTR**</span><span class="sxs-lookup"><span data-stu-id="64af1-129">Type: **LPCTSTR**</span></span>

</dd> <dd>

<span data-ttu-id="64af1-130">Der Unterschlüssel, unter dem die MRU-Daten gespeichert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="64af1-130">The subkey under which to store the MRU data.</span></span>

</dd> <dt>

<span data-ttu-id="64af1-131">**lpfnCompare**</span><span class="sxs-lookup"><span data-stu-id="64af1-131">**lpfnCompare**</span></span>
</dt> <dd>

<span data-ttu-id="64af1-132">Typ: **[ **MRUCMPPROC**](mrucmpproc.md)**</span><span class="sxs-lookup"><span data-stu-id="64af1-132">Type: **[**MRUCMPPROC**](mrucmpproc.md)**</span></span>

</dd> <dd>

<span data-ttu-id="64af1-133">Ein Zeiger auf eine optionale Datenvergleichsfunktion, mit der bestimmt werden kann, ob ein Element in der MRU-Liste vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="64af1-133">A pointer to an optional data comparison function that can be used to determine whether an item is present in the MRU list.</span></span> <span data-ttu-id="64af1-134">Dies ist nützlich, wenn die MRU-Liste mit dem **MRU \_ BINARY-Flag** erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="64af1-134">This is useful when the MRU list was created with the **MRU\_BINARY** flag.</span></span> <span data-ttu-id="64af1-135">Wenn dieser Member **NULL** ist, werden Standardmäßige Zeichenfolgenvergleichsfunktionen verwendet. für Binärdaten wird ein direkter Speichervergleich verwendet.</span><span class="sxs-lookup"><span data-stu-id="64af1-135">If this member is **NULL**, standard string comparison functions are used; for binary data, a direct memory comparison is used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="64af1-136">Hinweise</span><span class="sxs-lookup"><span data-stu-id="64af1-136">Remarks</span></span>

<span data-ttu-id="64af1-137">Diese Struktur ist in einer Headerdatei nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="64af1-137">This structure is not defined in a header file.</span></span> <span data-ttu-id="64af1-138">Sie müssen es selbst definieren.</span><span class="sxs-lookup"><span data-stu-id="64af1-138">You must define it yourself.</span></span>

## <a name="requirements"></a><span data-ttu-id="64af1-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="64af1-139">Requirements</span></span>



| <span data-ttu-id="64af1-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="64af1-140">Requirement</span></span> | <span data-ttu-id="64af1-141">Wert</span><span class="sxs-lookup"><span data-stu-id="64af1-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="64af1-142">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="64af1-142">Minimum supported client</span></span><br/> | <span data-ttu-id="64af1-143">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="64af1-143">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="64af1-144">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="64af1-144">Minimum supported server</span></span><br/> | <span data-ttu-id="64af1-145">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="64af1-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="64af1-146">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="64af1-146">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="64af1-147">**MRUINFOW** (Unicode) und **MRUINFOA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="64af1-147">**MRUINFOW** (Unicode) and **MRUINFOA** (ANSI)</span></span><br/>  |



 

 




