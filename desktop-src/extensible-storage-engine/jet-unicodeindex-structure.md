---
description: 'Weitere Informationen finden Sie hier: JET_UNICODEINDEX Struktur'
title: JET_UNICODEINDEX Struktur
TOCTitle: JET_UNICODEINDEX Structure
ms:assetid: d0b8ef74-850e-4e21-9f71-b56ec472aa0f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294097(v=EXCHG.10)
ms:contentKeyID: 32765712
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c4a2332551fb1f624b75e32596b2941d97ffa47d
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "104394278"
---
# <a name="jet_unicodeindex-structure"></a><span data-ttu-id="8c761-103">JET_UNICODEINDEX Struktur</span><span class="sxs-lookup"><span data-stu-id="8c761-103">JET_UNICODEINDEX Structure</span></span>


<span data-ttu-id="8c761-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="8c761-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_unicodeindex-structure"></a><span data-ttu-id="8c761-105">JET_UNICODEINDEX Struktur</span><span class="sxs-lookup"><span data-stu-id="8c761-105">JET_UNICODEINDEX Structure</span></span>

<span data-ttu-id="8c761-106">Mit der **JET_UNICODEINDEX** -Struktur wird angepasst, wie Unicode-Daten normalisiert werden, wenn ein Index für eine Unicode-Spalte erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="8c761-106">The **JET_UNICODEINDEX** structure customizes how Unicode data gets normalized when an index is created over a Unicode column.</span></span>

```cpp
typedef struct tagJET_UNICODEINDEX {
  unsigned long lcid;
  unsigned long dwMapFlags;
} JET_UNICODEINDEX;
```

### <a name="members"></a><span data-ttu-id="8c761-107">Member</span><span class="sxs-lookup"><span data-stu-id="8c761-107">Members</span></span>

<span data-ttu-id="8c761-108">**lcid**</span><span class="sxs-lookup"><span data-stu-id="8c761-108">**lcid**</span></span>

<span data-ttu-id="8c761-109">Die Gebiets Schema-ID, die beim Normalisieren der Daten verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="8c761-109">The Locale ID to use when normalizing the data.</span></span> <span data-ttu-id="8c761-110">Jedes Gebiets Schema kann verwendet werden, solange das entsprechende Sprachpaket auf dem Computer installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="8c761-110">Any locale may be used as long as the appropriate language pack has been installed on the machine.</span></span> <span data-ttu-id="8c761-111">Die einzige Ausnahme ist, dass das sprachneutrale Gebiets Schema (LCID of Zero) unzulässig ist.</span><span class="sxs-lookup"><span data-stu-id="8c761-111">The one exception is that the Language Neutral locale (LCID of zero) is illegal.</span></span>

<span data-ttu-id="8c761-112">**dwMapFlags**</span><span class="sxs-lookup"><span data-stu-id="8c761-112">**dwMapFlags**</span></span>

<span data-ttu-id="8c761-113">Diese Flags werden an [LCMapString](/windows/win32/api/winnls/nf-winnls-lcmapstringa) übergeben, wenn Unicode-Daten zu einem Schlüssel normalisiert werden, sodass benutzerdefinierte Flags den Standardwert überschreiben können.</span><span class="sxs-lookup"><span data-stu-id="8c761-113">These flags get passed to [LCMapString](/windows/win32/api/winnls/nf-winnls-lcmapstringa) when Unicode data gets normalized to a key, which enables user-defined flags to override the default.</span></span>

<span data-ttu-id="8c761-114">**Windows 2000**: die einzigen beiden gültigen Werte für **dwFlags** lauten:</span><span class="sxs-lookup"><span data-stu-id="8c761-114">**Windows 2000**:  The only two legal values for **dwFlags** are:</span></span>

  - <span data-ttu-id="8c761-115">(LCMAP_SORTKEY | NORM_IGNORECASE | NORM_IGNOREKANATYPE | NORM_IGNOREWIDTH | NORM_IGNORENONSPACE)</span><span class="sxs-lookup"><span data-stu-id="8c761-115">( LCMAP_SORTKEY | NORM_IGNORECASE | NORM_IGNOREKANATYPE | NORM_IGNOREWIDTH | NORM_IGNORENONSPACE )</span></span>

<!-- end list -->

  - <span data-ttu-id="8c761-116">(LCMAP_SORTKEY | NORM_IGNORECASE | NORM_IGNOREKANATYPE | NORM_IGNOREWIDTH)</span><span class="sxs-lookup"><span data-stu-id="8c761-116">( LCMAP_SORTKEY | NORM_IGNORECASE | NORM_IGNOREKANATYPE | NORM_IGNOREWIDTH )</span></span>

<span data-ttu-id="8c761-117">für **dwmapflags** gelten die folgenden Einschränkungen.</span><span class="sxs-lookup"><span data-stu-id="8c761-117">**dwMapFlags** has the following restrictions.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8c761-118">Wert</span><span class="sxs-lookup"><span data-stu-id="8c761-118">Value</span></span></p></th>
<th><p><span data-ttu-id="8c761-119">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="8c761-119">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8c761-120">LCMAP_SORTKEY</span><span class="sxs-lookup"><span data-stu-id="8c761-120">LCMAP_SORTKEY</span></span></p></td>
<td><p><span data-ttu-id="8c761-121">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="8c761-121">Mandatory.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c761-122">LCMAP_BYTEREV</span><span class="sxs-lookup"><span data-stu-id="8c761-122">LCMAP_BYTEREV</span></span></p></td>
<td><p><span data-ttu-id="8c761-123">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="8c761-123">Optional.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8c761-124">NORM_IGNORECASE</span><span class="sxs-lookup"><span data-stu-id="8c761-124">NORM_IGNORECASE</span></span></p></td>
<td><p><span data-ttu-id="8c761-125">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="8c761-125">Optional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c761-126">NORM_IGNORENONSPACE</span><span class="sxs-lookup"><span data-stu-id="8c761-126">NORM_IGNORENONSPACE</span></span></p></td>
<td><p><span data-ttu-id="8c761-127">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="8c761-127">Optional.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8c761-128">NORM_IGNORESYMBOLS</span><span class="sxs-lookup"><span data-stu-id="8c761-128">NORM_IGNORESYMBOLS</span></span></p></td>
<td><p><span data-ttu-id="8c761-129">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="8c761-129">Optional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c761-130">NORM_IGNOREKANATYPE</span><span class="sxs-lookup"><span data-stu-id="8c761-130">NORM_IGNOREKANATYPE</span></span></p></td>
<td><p><span data-ttu-id="8c761-131">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="8c761-131">Optional.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8c761-132">NORM_IGNOREWIDTH</span><span class="sxs-lookup"><span data-stu-id="8c761-132">NORM_IGNOREWIDTH</span></span></p></td>
<td><p><span data-ttu-id="8c761-133">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="8c761-133">Optional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c761-134">SORT_STRINGSORT</span><span class="sxs-lookup"><span data-stu-id="8c761-134">SORT_STRINGSORT</span></span></p></td>
<td><p><span data-ttu-id="8c761-135">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="8c761-135">Optional.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="8c761-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8c761-136">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8c761-137"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="8c761-137"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="8c761-138">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="8c761-138">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c761-139"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="8c761-139"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="8c761-140">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="8c761-140">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8c761-141"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="8c761-141"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="8c761-142">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="8c761-142">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="8c761-143">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="8c761-143">See Also</span></span>

[<span data-ttu-id="8c761-144">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="8c761-144">JET_COLTYP</span></span>](./jet-coltyp.md)  
[<span data-ttu-id="8c761-145">JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="8c761-145">JET_INDEXCREATE</span></span>](./jet-indexcreate-structure.md)  
[<span data-ttu-id="8c761-146">JetOpenTempTable3</span><span class="sxs-lookup"><span data-stu-id="8c761-146">JetOpenTempTable3</span></span>](./jetopentemptable3-function.md)
