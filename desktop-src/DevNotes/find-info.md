---
description: Enthält Such Kontextinformationen.
ms.assetid: 4b865563-98c2-459b-bb2b-75420d51d6a7
title: FIND_INFO Struktur
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FIND_INFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: 7d6b6dea42c008178c22f6e342a64b2f8d193ec5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345609"
---
# <a name="find_info-structure"></a><span data-ttu-id="95e5c-103">\_Informationsstruktur suchen</span><span class="sxs-lookup"><span data-stu-id="95e5c-103">FIND\_INFO structure</span></span>

<span data-ttu-id="95e5c-104">Enthält Such Kontextinformationen.</span><span class="sxs-lookup"><span data-stu-id="95e5c-104">Contains search context information.</span></span>

## <a name="syntax"></a><span data-ttu-id="95e5c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="95e5c-105">Syntax</span></span>


```C++
typedef struct _FIND_INFO {
  TAGID     tiIndex;
  TAGID     tiCurrent;
  TAGID     tiEndIndex;
  TAG       tName;
  DWORD     dwIndexRec;
  DWORD     dwFlags;
  ULONGLONG ullKey;
  union {
    LPCTSTR szName;
    DWORD   dwName;
    GUID    *pguidName;
  };
} FIND_INFO, *PFIND_INFO;
```



## <a name="members"></a><span data-ttu-id="95e5c-106">Member</span><span class="sxs-lookup"><span data-stu-id="95e5c-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="95e5c-107">**tiindex**</span><span class="sxs-lookup"><span data-stu-id="95e5c-107">**tiIndex**</span></span>
</dt> <dd>

<span data-ttu-id="95e5c-108">Die **TagID** für den Index, der gesucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="95e5c-108">The **TAGID** for the index to be searched.</span></span>

</dd> <dt>

<span data-ttu-id="95e5c-109">**ticurrent**</span><span class="sxs-lookup"><span data-stu-id="95e5c-109">**tiCurrent**</span></span>
</dt> <dd>

<span data-ttu-id="95e5c-110">Die **TagID** für das aktuelle Element, das gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="95e5c-110">The **TAGID** for the current item that was located.</span></span>

</dd> <dt>

<span data-ttu-id="95e5c-111">**tikodindex**</span><span class="sxs-lookup"><span data-stu-id="95e5c-111">**tiEndIndex**</span></span>
</dt> <dd>

<span data-ttu-id="95e5c-112">Die **TagID** für den letzten Datensatz nach FindFirst, wenn der Index eindeutig ist.</span><span class="sxs-lookup"><span data-stu-id="95e5c-112">The **TAGID** for the last record after FindFirst if the index is UNIQUE.</span></span>

</dd> <dt>

<span data-ttu-id="95e5c-113">**tName**</span><span class="sxs-lookup"><span data-stu-id="95e5c-113">**tName**</span></span>
</dt> <dd>

<span data-ttu-id="95e5c-114">Der Typ des zu suchenden Elements.</span><span class="sxs-lookup"><span data-stu-id="95e5c-114">The type of the item to be located.</span></span> <span data-ttu-id="95e5c-115">Siehe [Tagtypen](tag-types.md).</span><span class="sxs-lookup"><span data-stu-id="95e5c-115">See [TAG Types](tag-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="95e5c-116">**dwindexrec**</span><span class="sxs-lookup"><span data-stu-id="95e5c-116">**dwIndexRec**</span></span>
</dt> <dd>

<span data-ttu-id="95e5c-117">Ein interner Indikator, mit dem nachverfolgt wird, wo im Index der nächste Suchvorgang beginnen soll.</span><span class="sxs-lookup"><span data-stu-id="95e5c-117">An internal counter used to track where in the index the next find operation should start.</span></span>

</dd> <dt>

<span data-ttu-id="95e5c-118">**dwFlags**</span><span class="sxs-lookup"><span data-stu-id="95e5c-118">**dwFlags**</span></span>
</dt> <dd>

<span data-ttu-id="95e5c-119">Dieser Member kann 0 oder ein eindeutiger **shimdb- \_ Index \_ \_** (0x00000001) sein, was darauf hinweist, dass es sich hierbei um einen eindeutigen Schlüssel Index handelt.</span><span class="sxs-lookup"><span data-stu-id="95e5c-119">This member can be 0 or **SHIMDB\_INDEX\_UNIQUE\_KEY** (0x00000001), which indicates that this is a unique-key index.</span></span>

</dd> <dt>

<span data-ttu-id="95e5c-120">**ullkey**</span><span class="sxs-lookup"><span data-stu-id="95e5c-120">**ullKey**</span></span>
</dt> <dd>

<span data-ttu-id="95e5c-121">Der Schlüssel für den aktuellen Eintrag.</span><span class="sxs-lookup"><span data-stu-id="95e5c-121">The key for the current entry.</span></span>

</dd> <dt>

<span data-ttu-id="95e5c-122">**szName**</span><span class="sxs-lookup"><span data-stu-id="95e5c-122">**szName**</span></span>
</dt> <dd>

<span data-ttu-id="95e5c-123">Die aktuelle Zeichenfolge (wenn der Tagtyp **" \_ TagType \_**" ist).</span><span class="sxs-lookup"><span data-stu-id="95e5c-123">The current string (if the tag type is **TAG\_TYPE\_STRINGREF**).</span></span>

</dd> <dt>

<span data-ttu-id="95e5c-124">**dwname**</span><span class="sxs-lookup"><span data-stu-id="95e5c-124">**dwName**</span></span>
</dt> <dd>

<span data-ttu-id="95e5c-125">Der aktuelle **DWORD** -Wert (wenn der Tagtyp **\_ \_ DWORD** ist).</span><span class="sxs-lookup"><span data-stu-id="95e5c-125">The current **DWORD** value (if the tag type is **TAG\_TYPE\_DWORD**).</span></span>

</dd> <dt>

<span data-ttu-id="95e5c-126">**pguidname**</span><span class="sxs-lookup"><span data-stu-id="95e5c-126">**pguidName**</span></span>
</dt> <dd>

<span data-ttu-id="95e5c-127">Der aktuelle GUID-Wert (wenn der Tagtyp **\_ \_ Binär** ist und das Tag eine **\_ Tagdatenbank- \_ ID** ist).</span><span class="sxs-lookup"><span data-stu-id="95e5c-127">The current GUID value (if the tag type is **TAG\_TYPE\_BINARY** and the TAG is **TAG\_DATABASE\_ID**).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="95e5c-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="95e5c-128">Requirements</span></span>



| <span data-ttu-id="95e5c-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="95e5c-129">Requirement</span></span> | <span data-ttu-id="95e5c-130">Wert</span><span class="sxs-lookup"><span data-stu-id="95e5c-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="95e5c-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="95e5c-131">Minimum supported client</span></span><br/> | <span data-ttu-id="95e5c-132">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="95e5c-132">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="95e5c-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="95e5c-133">Minimum supported server</span></span><br/> | <span data-ttu-id="95e5c-134">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="95e5c-134">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="95e5c-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="95e5c-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95e5c-136">**Sdbfindfirstdwordindexedtag**</span><span class="sxs-lookup"><span data-stu-id="95e5c-136">**SdbFindFirstDWORDIndexedTag**</span></span>](sdbfindfirstdwordindexedtag.md)
</dt> </dl>

 

 




