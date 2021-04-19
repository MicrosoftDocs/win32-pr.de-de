---
description: 'Weitere Informationen finden Sie hier: JET_THREADSTATS Struktur'
title: JET_THREADSTATS Struktur
TOCTitle: JET_THREADSTATS Structure
ms:assetid: 37e86e14-7719-4991-aae8-bcff1baa80df
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269227(v=EXCHG.10)
ms:contentKeyID: 32765529
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
ms.openlocfilehash: 2b84de9a4f64db5dda261b8ee177787f62fd01ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106368963"
---
# <a name="jet_threadstats-structure"></a><span data-ttu-id="c2f41-103">JET_THREADSTATS Struktur</span><span class="sxs-lookup"><span data-stu-id="c2f41-103">JET_THREADSTATS Structure</span></span>


<span data-ttu-id="c2f41-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="c2f41-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_threadstats-structure"></a><span data-ttu-id="c2f41-105">JET_THREADSTATS Struktur</span><span class="sxs-lookup"><span data-stu-id="c2f41-105">JET_THREADSTATS Structure</span></span>

<span data-ttu-id="c2f41-106">Die **JET_THREADSTATS** Struktur enthält kumulative Statistiken für die Arbeit, die von der Datenbank-Engine auf dem aktuellen Thread ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c2f41-106">The **JET_THREADSTATS** structure contains cumulative statistics on the work performed by the database engine on the current thread.</span></span> <span data-ttu-id="c2f41-107">Diese Informationen werden über [jetgetthreadstats](./jetgetthreadstats-function.md)zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c2f41-107">This information is returned via [JetGetThreadStats](./jetgetthreadstats-function.md).</span></span>

<span data-ttu-id="c2f41-108">**Windows Vista:**  Die **JET_THREADSTATS** Struktur wird in Windows Vista eingeführt.</span><span class="sxs-lookup"><span data-stu-id="c2f41-108">**Windows Vista:**  The **JET_THREADSTATS** structure is introduced in Windows Vista.</span></span>

```cpp
    typedef struct {
      unsigned long cbStruct;
      unsigned long cPageReferenced;
      unsigned long cPageRead;
      unsigned long cPagePreread;
      unsigned long cPageDirtied;
      unsigned long cPageRedirtied;
      unsigned long cLogRecord;
      unsigned long cbLogRecord;
    } JET_THREADSTATS;
```

### <a name="members"></a><span data-ttu-id="c2f41-109">Member</span><span class="sxs-lookup"><span data-stu-id="c2f41-109">Members</span></span>

<span data-ttu-id="c2f41-110">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="c2f41-110">**cbStruct**</span></span>

<span data-ttu-id="c2f41-111">Die Größe der zurückgegebenen **JET_THREADSTATS** Struktur in Bytes.</span><span class="sxs-lookup"><span data-stu-id="c2f41-111">The size of the returned **JET_THREADSTATS** structure, in bytes.</span></span>

<span data-ttu-id="c2f41-112">**Hinweis**  Die **JET_THREADSTATS** Struktur wird in Zukunft erweitert, um mehr Statistiken zu enthalten.</span><span class="sxs-lookup"><span data-stu-id="c2f41-112">**Note**  The **JET_THREADSTATS** structure will expand in the future to contain more statistics.</span></span> <span data-ttu-id="c2f41-113">Neue Statistiken werden am Ende der Struktur hinzugefügt und können mit einer erweiterten Ausgabepuffergröße abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="c2f41-113">New statistics will be added to the end of the structure and can be retrieved with an increased output buffer size.</span></span> <span data-ttu-id="c2f41-114">Das vorhanden sein zusätzlicher Statistiken kann durch einen größeren **cbStruct** -Wert abgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="c2f41-114">The presence of additional statistics can be inferred by a larger **cbStruct** value.</span></span>

<span data-ttu-id="c2f41-115">**cpagereferenziert**</span><span class="sxs-lookup"><span data-stu-id="c2f41-115">**cPageReferenced**</span></span>

<span data-ttu-id="c2f41-116">Die Gesamtanzahl der Datenbankseiten, die von der Datenbank-Engine im aktuellen Thread besucht wurden.</span><span class="sxs-lookup"><span data-stu-id="c2f41-116">The total number of database pages visited by the database engine on the current thread.</span></span>

<span data-ttu-id="c2f41-117">**cpageread**</span><span class="sxs-lookup"><span data-stu-id="c2f41-117">**cPageRead**</span></span>

<span data-ttu-id="c2f41-118">Die Gesamtanzahl der Datenbankseiten, die von der Datenbank-Engine auf dem aktuellen Thread von der Festplatte abgerufen wurden.</span><span class="sxs-lookup"><span data-stu-id="c2f41-118">The total number of database pages fetched from disk by the database engine on the current thread.</span></span>

<span data-ttu-id="c2f41-119">**cpagepreread**</span><span class="sxs-lookup"><span data-stu-id="c2f41-119">**cPagePreread**</span></span>

<span data-ttu-id="c2f41-120">Die Gesamtanzahl der Datenbankseiten, die von der Datenbank-Engine im aktuellen Thread vorab von der Festplatte abgerufen wurden.</span><span class="sxs-lookup"><span data-stu-id="c2f41-120">The total number of database pages prefetched from disk by the database engine on the current thread.</span></span>

<span data-ttu-id="c2f41-121">**cpagedirtied**</span><span class="sxs-lookup"><span data-stu-id="c2f41-121">**cPageDirtied**</span></span>

<span data-ttu-id="c2f41-122">Die Gesamtanzahl der Datenbankseiten ohne Änderungen, die von der Datenbank-Engine im aktuellen Thread geändert wurden.</span><span class="sxs-lookup"><span data-stu-id="c2f41-122">The total number of database pages, with no unwritten changes, that have been modified by the database engine on the current thread.</span></span>

<span data-ttu-id="c2f41-123">**cPageRedirtied**</span><span class="sxs-lookup"><span data-stu-id="c2f41-123">**cPageRedirtied**</span></span>

<span data-ttu-id="c2f41-124">Die Gesamtanzahl der Datenbankseiten, bei denen Änderungen vorgenommen wurden, die von der Datenbank-Engine im aktuellen Thread geändert wurden.</span><span class="sxs-lookup"><span data-stu-id="c2f41-124">The total number of database pages, with unwritten changes, that have been modified by the database engine on the current thread.</span></span>

<span data-ttu-id="c2f41-125">**clogrecord**</span><span class="sxs-lookup"><span data-stu-id="c2f41-125">**cLogRecord**</span></span>

<span data-ttu-id="c2f41-126">Die Gesamtanzahl der Transaktionsprotokoll-Datensätze, die von der Datenbank-Engine im aktuellen Thread generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="c2f41-126">The total number of transaction log records that have been generated by the database engine on the current thread.</span></span>

<span data-ttu-id="c2f41-127">**cblogdatensatz**</span><span class="sxs-lookup"><span data-stu-id="c2f41-127">**cbLogRecord**</span></span>

<span data-ttu-id="c2f41-128">Die Gesamtgröße der Transaktionsprotokoll Datensätze in Bytes, die von der Datenbank-Engine im aktuellen Thread generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="c2f41-128">The total size in bytes of transaction log records that have been generated by the database engine on the current thread.</span></span>

### <a name="requirements"></a><span data-ttu-id="c2f41-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c2f41-129">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c2f41-130"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="c2f41-130"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="c2f41-131">Erfordert Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="c2f41-131">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c2f41-132"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="c2f41-132"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="c2f41-133">Erfordert Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="c2f41-133">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c2f41-134"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="c2f41-134"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="c2f41-135">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="c2f41-135">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="c2f41-136">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c2f41-136">See Also</span></span>

[<span data-ttu-id="c2f41-137">Jetgetthreadstats</span><span class="sxs-lookup"><span data-stu-id="c2f41-137">JetGetThreadStats</span></span>](./jetgetthreadstats-function.md)
