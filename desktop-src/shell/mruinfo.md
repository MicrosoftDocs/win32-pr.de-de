---
description: Enthält Informationen, die eine neue Liste der zuletzt verwendeten (MRU) definieren. Wird von "kreatemrulistw" verwendet.
title: Mruinfo-Struktur
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
ms.openlocfilehash: 91c0b1a2c10f4ac77afa5f8af2380b3d14ced8f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104993790"
---
# <a name="mruinfo-structure"></a><span data-ttu-id="0ed1e-104">Mruinfo-Struktur</span><span class="sxs-lookup"><span data-stu-id="0ed1e-104">MRUINFO structure</span></span>

<span data-ttu-id="0ed1e-105">Enthält Informationen, die eine neue Liste der zuletzt verwendeten (MRU) definieren.</span><span class="sxs-lookup"><span data-stu-id="0ed1e-105">Contains information that defines a new most recently used (MRU) list.</span></span> <span data-ttu-id="0ed1e-106">Wird von " [**kreatemrulistw**](createmrulist.md)" verwendet.</span><span class="sxs-lookup"><span data-stu-id="0ed1e-106">Used by [**CreateMRUListW**](createmrulist.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="0ed1e-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="0ed1e-107">Syntax</span></span>


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



## <a name="members"></a><span data-ttu-id="0ed1e-108">Member</span><span class="sxs-lookup"><span data-stu-id="0ed1e-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="0ed1e-109">**CBSIZE**</span><span class="sxs-lookup"><span data-stu-id="0ed1e-109">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="0ed1e-110">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="0ed1e-110">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="0ed1e-111">Die Größe der-Struktur.</span><span class="sxs-lookup"><span data-stu-id="0ed1e-111">The size of the structure.</span></span>

</dd> <dt>

<span data-ttu-id="0ed1e-112">**Umax**</span><span class="sxs-lookup"><span data-stu-id="0ed1e-112">**uMax**</span></span>
</dt> <dd>

<span data-ttu-id="0ed1e-113">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="0ed1e-113">Type: **UINT**</span></span>

</dd> <dd>

<span data-ttu-id="0ed1e-114">Die maximale Anzahl von Einträgen in der MRU-Liste.</span><span class="sxs-lookup"><span data-stu-id="0ed1e-114">The maximum number of entries in the MRU list.</span></span>

</dd> <dt>

<span data-ttu-id="0ed1e-115">**fFlags**</span><span class="sxs-lookup"><span data-stu-id="0ed1e-115">**fFlags**</span></span>
</dt> <dd>

<span data-ttu-id="0ed1e-116">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="0ed1e-116">Type: **UINT**</span></span>

</dd> <dd>

<span data-ttu-id="0ed1e-117">Mindestens eines der folgenden Flags.</span><span class="sxs-lookup"><span data-stu-id="0ed1e-117">One or more of the following flags.</span></span>

<dt>

<span id="MRU_BINARY"></span><span id="mru_binary"></span>

<span data-ttu-id="0ed1e-118"><span id="MRU_BINARY"></span><span id="mru_binary"></span>**MRU \_ Binary** (0x0001)</span><span class="sxs-lookup"><span data-stu-id="0ed1e-118"><span id="MRU_BINARY"></span><span id="mru_binary"></span>**MRU\_BINARY** (0x0001)</span></span>


</dt> <dd>

<span data-ttu-id="0ed1e-119">Daten werden in der Registrierung als Binärdaten und nicht als Zeichen folgen Daten gespeichert.</span><span class="sxs-lookup"><span data-stu-id="0ed1e-119">Data is stored in the registry as binary data rather than string data.</span></span>

</dd> <dt>

<span id="MRU_CACHEWRITE"></span><span id="mru_cachewrite"></span>

<span data-ttu-id="0ed1e-120"><span id="MRU_CACHEWRITE"></span><span id="mru_cachewrite"></span>**MRU \_ Cachewrite** (0x0002)</span><span class="sxs-lookup"><span data-stu-id="0ed1e-120"><span id="MRU_CACHEWRITE"></span><span id="mru_cachewrite"></span>**MRU\_CACHEWRITE** (0x0002)</span></span>


</dt> <dd>

<span data-ttu-id="0ed1e-121">Schreiben Sie Änderungen an der MRU-Version, die in der Registrierung gespeichert ist, nur dann, wenn ein neues Element hinzugefügt wird oder die Ressourcen der MRU-Liste aus dem Arbeitsspeicher freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="0ed1e-121">Write changes to the version of the MRU stored in the registry only when a new item is added or the MRU list's resources are freed from memory.</span></span> <span data-ttu-id="0ed1e-122">Beachten Sie, dass die aktive Version der MRU im Arbeitsspeicher sofort als Reaktion auf eine Änderung des Inhalts oder der Reihenfolge aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="0ed1e-122">Note that the active version of the MRU in memory is updated immediately in response to any change in contents or ordering.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="0ed1e-123">**HKEY**</span><span class="sxs-lookup"><span data-stu-id="0ed1e-123">**hKey**</span></span>
</dt> <dd>

<span data-ttu-id="0ed1e-124">Typ: **HKEY**</span><span class="sxs-lookup"><span data-stu-id="0ed1e-124">Type: **HKEY**</span></span>

</dd> <dd>

<span data-ttu-id="0ed1e-125">Ein Handle für den aktuell geöffneten Schlüssel oder einen der folgenden vordefinierten Werte, unter denen die MRU-Daten gespeichert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="0ed1e-125">A handle to the currently open key, or one of the following predefined values under which to store the MRU data.</span></span>

<dl><span id="HKEY_CURRENT_USER"></span><span id="hkey_current_user"></span><dt>

<span data-ttu-id="0ed1e-126">**Aktueller HKEY- \_ \_ Benutzer**</span><span class="sxs-lookup"><span data-stu-id="0ed1e-126">**HKEY\_CURRENT\_USER**</span></span>
</dt><span id="HKEY_LOCAL_MACHINE"></span><span id="hkey_local_machine"></span><dt>

<span data-ttu-id="0ed1e-127">**lokaler HKEY- \_ \_ Computer**</span><span class="sxs-lookup"><span data-stu-id="0ed1e-127">**HKEY\_LOCAL\_MACHINE**</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="0ed1e-128">**lpszSubKey**</span><span class="sxs-lookup"><span data-stu-id="0ed1e-128">**lpszSubKey**</span></span>
</dt> <dd>

<span data-ttu-id="0ed1e-129">Typ: **LPCTSTR**</span><span class="sxs-lookup"><span data-stu-id="0ed1e-129">Type: **LPCTSTR**</span></span>

</dd> <dd>

<span data-ttu-id="0ed1e-130">Der Unterschlüssel, unter dem die MRU-Daten gespeichert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="0ed1e-130">The subkey under which to store the MRU data.</span></span>

</dd> <dt>

<span data-ttu-id="0ed1e-131">**lpfncompare**</span><span class="sxs-lookup"><span data-stu-id="0ed1e-131">**lpfnCompare**</span></span>
</dt> <dd>

<span data-ttu-id="0ed1e-132">Typ: **[ **mrucmpproc**](mrucmpproc.md)**</span><span class="sxs-lookup"><span data-stu-id="0ed1e-132">Type: **[**MRUCMPPROC**](mrucmpproc.md)**</span></span>

</dd> <dd>

<span data-ttu-id="0ed1e-133">Ein Zeiger auf eine optionale Daten Vergleichsfunktion, die verwendet werden kann, um zu bestimmen, ob ein Element in der MRU-Liste vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="0ed1e-133">A pointer to an optional data comparison function that can be used to determine whether an item is present in the MRU list.</span></span> <span data-ttu-id="0ed1e-134">Dies ist hilfreich, wenn die MRU-Liste mit dem **MRU- \_ Binärflag** erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="0ed1e-134">This is useful when the MRU list was created with the **MRU\_BINARY** flag.</span></span> <span data-ttu-id="0ed1e-135">Wenn dieser Member **null** ist, werden standardmäßige Zeichen folgen Vergleichsfunktionen verwendet. für Binärdaten wird ein direkter Speicher Vergleich verwendet.</span><span class="sxs-lookup"><span data-stu-id="0ed1e-135">If this member is **NULL**, standard string comparison functions are used; for binary data, a direct memory comparison is used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0ed1e-136">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0ed1e-136">Remarks</span></span>

<span data-ttu-id="0ed1e-137">Diese Struktur ist nicht in einer Header Datei definiert.</span><span class="sxs-lookup"><span data-stu-id="0ed1e-137">This structure is not defined in a header file.</span></span> <span data-ttu-id="0ed1e-138">Sie müssen Sie selbst definieren.</span><span class="sxs-lookup"><span data-stu-id="0ed1e-138">You must define it yourself.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ed1e-139">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="0ed1e-139">Requirements</span></span>



| <span data-ttu-id="0ed1e-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0ed1e-140">Requirement</span></span> | <span data-ttu-id="0ed1e-141">Wert</span><span class="sxs-lookup"><span data-stu-id="0ed1e-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="0ed1e-142">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0ed1e-142">Minimum supported client</span></span><br/> | <span data-ttu-id="0ed1e-143">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0ed1e-143">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="0ed1e-144">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0ed1e-144">Minimum supported server</span></span><br/> | <span data-ttu-id="0ed1e-145">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0ed1e-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="0ed1e-146">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="0ed1e-146">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="0ed1e-147">**Mruinfow** (Unicode) und **mruinfoa** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="0ed1e-147">**MRUINFOW** (Unicode) and **MRUINFOA** (ANSI)</span></span><br/>  |



 

 




