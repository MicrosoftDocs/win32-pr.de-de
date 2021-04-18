---
description: 'Weitere Informationen finden Sie hier: JET_CONDITIONALCOLUMN Struktur'
title: JET_CONDITIONALCOLUMN Struktur
TOCTitle: JET_CONDITIONALCOLUMN Structure
ms:assetid: 2ca6b4ba-0dc4-47d5-b072-324e5a381d0d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269214(v=EXCHG.10)
ms:contentKeyID: 32765517
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
ms.openlocfilehash: 27d0add64adeb7b609e84d6102a06230df55ebbf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343362"
---
# <a name="jet_conditionalcolumn-structure"></a><span data-ttu-id="0b094-103">JET_CONDITIONALCOLUMN Struktur</span><span class="sxs-lookup"><span data-stu-id="0b094-103">JET_CONDITIONALCOLUMN Structure</span></span>


<span data-ttu-id="0b094-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="0b094-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_conditionalcolumn-structure"></a><span data-ttu-id="0b094-105">JET_CONDITIONALCOLUMN Struktur</span><span class="sxs-lookup"><span data-stu-id="0b094-105">JET_CONDITIONALCOLUMN Structure</span></span>

<span data-ttu-id="0b094-106">Die **JET_CONDITIONALCOLUMN** Struktur definiert, wie die bedingte Indizierung für einen bestimmten Index ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0b094-106">The **JET_CONDITIONALCOLUMN** structure defines how conditional indexing is performed for a given index.</span></span> <span data-ttu-id="0b094-107">Ein bedingter Index enthält einen Index Eintrag für nur die Zeilen, die der angegebenen Bedingung entsprechen.</span><span class="sxs-lookup"><span data-stu-id="0b094-107">A conditional index contains an index entry for only those rows that match the specified condition.</span></span> <span data-ttu-id="0b094-108">Die bedingte Spalte ist jedoch nicht Teil des Index Schlüssels, sondern nur das vorhanden sein des Index Eintrags.</span><span class="sxs-lookup"><span data-stu-id="0b094-108">However, the conditional column is not part of the index's key, it only controls the presence of the index entry.</span></span>

```cpp
    typedef struct tagJET_CONDITIONALCOLUMN {
      unsigned long cbStruct;
      tchar* szColumnName;
      JET_GRBIT grbit;
    } JET_CONDITIONALCOLUMN;
```

### <a name="members"></a><span data-ttu-id="0b094-109">Member</span><span class="sxs-lookup"><span data-stu-id="0b094-109">Members</span></span>

<span data-ttu-id="0b094-110">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="0b094-110">**cbStruct**</span></span>

<span data-ttu-id="0b094-111">Dieses Feld muss mit sizeof (JET_CONDITIONALCOLUMN) initialisiert werden (in Bytes).</span><span class="sxs-lookup"><span data-stu-id="0b094-111">This field must be initialized to sizeof( JET_CONDITIONALCOLUMN ), in bytes.</span></span>

<span data-ttu-id="0b094-112">**szcolumnname**</span><span class="sxs-lookup"><span data-stu-id="0b094-112">**szColumnName**</span></span>

<span data-ttu-id="0b094-113">Der Name der Spalte, die die Daten enthält, auf denen die Datenbank-Engine die Zeile bedingt indiziert.</span><span class="sxs-lookup"><span data-stu-id="0b094-113">The name of the column that contains the data on which the database engine is conditionally indexing the row.</span></span>

<span data-ttu-id="0b094-114">**grbit** Eine Gruppe von Bits, die die Optionen für den bedingten Index enthält.</span><span class="sxs-lookup"><span data-stu-id="0b094-114">**grbit** A group of bits that gives the options for the conditional index.</span></span> <span data-ttu-id="0b094-115">Das übergeben von NULL-oder logisch-**oder** Ed-Werten ist für **JET_CONDITIONALCOLUMN** ungültig.</span><span class="sxs-lookup"><span data-stu-id="0b094-115">Passing in zero or logically-**OR** ed values is not valid for **JET_CONDITIONALCOLUMN**.</span></span> <span data-ttu-id="0b094-116">Das Bitfeld muss genau eines der folgenden sein:</span><span class="sxs-lookup"><span data-stu-id="0b094-116">The bit field must be exactly one of the following:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0b094-117">Wert</span><span class="sxs-lookup"><span data-stu-id="0b094-117">Value</span></span></p></th>
<th><p><span data-ttu-id="0b094-118">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="0b094-118">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0b094-119">JET_bitIndexColumnMustBeNull</span><span class="sxs-lookup"><span data-stu-id="0b094-119">JET_bitIndexColumnMustBeNull</span></span></p></td>
<td><p><span data-ttu-id="0b094-120">Die durch den <em>szcolumnname</em> -Parameter angegebene Spalte muss NULL sein, damit ein Index Eintrag für eine bestimmte Zeile in diesem Index angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="0b094-120">The column specified by the <em>szColumnName</em> parameter must be NULL for an index entry for a given row to appear in this index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0b094-121">JET_bitIndexColumnMustBeNonNull</span><span class="sxs-lookup"><span data-stu-id="0b094-121">JET_bitIndexColumnMustBeNonNull</span></span></p></td>
<td><p><span data-ttu-id="0b094-122">Die vom <em>szcolumnname</em> -Parameter angegebene Spalte muss für einen Index Eintrag ungleich NULL sein, damit eine bestimmte Zeile in diesem Index angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="0b094-122">The column specified by the <em>szColumnName</em> parameter must be non-NULL for an index entry in order for a given row to appear in this index.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="remarks"></a><span data-ttu-id="0b094-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0b094-123">Remarks</span></span>

<span data-ttu-id="0b094-124">Ein bedingter Index enthält einen Index Eintrag für nur die Zeilen, die der angegebenen Bedingung entsprechen.</span><span class="sxs-lookup"><span data-stu-id="0b094-124">A conditional index contains an index entry for only those rows that match the specified condition.</span></span> <span data-ttu-id="0b094-125">Beispielsweise kann eine Spalte mit dem Namen "markiert" benannt werden, und wenn eine Zeile markiert ist, wird die Spalte auf einen Wert festgelegt, der nicht NULL ist.</span><span class="sxs-lookup"><span data-stu-id="0b094-125">For example, a column could be named "Marked", and when a row is marked, the column is set to a non-NULL value.</span></span> <span data-ttu-id="0b094-126">Mit einem JET_bitIndexColumnMustBeNonNull bedingten Index für diese Spalte werden alle Zeilen angezeigt, die als gekennzeichnet sind, und ein JET_bitIndexColumnMustBeNull bedingter Index zeigt Zeilen an, die nicht als markiert sind.</span><span class="sxs-lookup"><span data-stu-id="0b094-126">A JET_bitIndexColumnMustBeNonNull conditional index on this column will show all rows that are marked, and a JET_bitIndexColumnMustBeNull conditional index will show rows that are not marked.</span></span> <span data-ttu-id="0b094-127">Dies ist auch eine bequeme Möglichkeit zum Löschen von Flags und zum Garbage Collection-Index.</span><span class="sxs-lookup"><span data-stu-id="0b094-127">This is also a convenient way to perform a flag deletion and garbage collecting index.</span></span>

### <a name="requirements"></a><span data-ttu-id="0b094-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0b094-128">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0b094-129"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="0b094-129"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="0b094-130">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="0b094-130">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0b094-131"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="0b094-131"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="0b094-132">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="0b094-132">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0b094-133"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="0b094-133"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="0b094-134">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="0b094-134">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0b094-135"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="0b094-135"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="0b094-136">Wird als <strong>JET_CONDITIONALCOLUMN_W</strong> (Unicode) und <strong>JET_CONDITIONALCOLUMN_A</strong> (ANSI) implementiert.</span><span class="sxs-lookup"><span data-stu-id="0b094-136">Implemented as <strong>JET_CONDITIONALCOLUMN_W</strong> (Unicode) and <strong>JET_CONDITIONALCOLUMN_A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="0b094-137">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="0b094-137">See Also</span></span>

[<span data-ttu-id="0b094-138">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="0b094-138">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="0b094-139">JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="0b094-139">JET_INDEXCREATE</span></span>](./jet-indexcreate-structure.md)
