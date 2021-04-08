---
description: 'Weitere Informationen finden Sie hier: JET_RECSIZE Struktur'
title: JET_RECSIZE Struktur
TOCTitle: JET_RECSIZE Structure
ms:assetid: bb2a63bb-7956-46c2-9791-0d0678a6c366
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294072(v=EXCHG.10)
ms:contentKeyID: 32765687
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- kbArticle
- apiref
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e4e6b2f313a5411ba5bfeea73db3b01afe007612
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749856"
---
# <a name="jet_recsize-structure"></a><span data-ttu-id="9f71f-103">JET_RECSIZE Struktur</span><span class="sxs-lookup"><span data-stu-id="9f71f-103">JET_RECSIZE Structure</span></span>


<span data-ttu-id="9f71f-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="9f71f-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_recsize-structure"></a><span data-ttu-id="9f71f-105">JET_RECSIZE Struktur</span><span class="sxs-lookup"><span data-stu-id="9f71f-105">JET_RECSIZE Structure</span></span>

<span data-ttu-id="9f71f-106">Die **JET_RECSIZE** Struktur wird von [jetgetrecordsize](./jetgetrecordsize-function.md) verwendet, um Informationen über die Verwendungs Anforderungen eines Datensatzes im Benutzerdaten Bereich, die Anzahl der Mengen Spalten, die Anzahl der Werte und den mehr Aufwand der ESE-Daten Satzstruktur zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="9f71f-106">The **JET_RECSIZE** structure is used by [JetGetRecordSize](./jetgetrecordsize-function.md) to return information about a record's usage requirements in user data space, number of set columns, number of values, and ESE record structure overhead space.</span></span>

<span data-ttu-id="9f71f-107">**Windows Vista:** Die **JET_RECSIZE** Struktur wird in Windows Vista eingeführt.</span><span class="sxs-lookup"><span data-stu-id="9f71f-107">**Windows Vista:** The **JET_RECSIZE** structure is introduced in Windows Vista.</span></span>

```cpp
    typedef struct {
      unsigned __int64 cbData;
      unsigned __int64 cbLongValueData;
      unsigned __int64 cbOverhead;
      unsigned __int64 cbLongValueOverhead;
      unsigned __int64 cNonTaggedColumns;
      unsigned __int64 cTaggedColumns;
      unsigned __int64 cLongValues;
      unsigned __int64 cMultiValues;
    } JET_RECSIZE;
```

### <a name="members"></a><span data-ttu-id="9f71f-108">Member</span><span class="sxs-lookup"><span data-stu-id="9f71f-108">Members</span></span>

<span data-ttu-id="9f71f-109">**cbData**</span><span class="sxs-lookup"><span data-stu-id="9f71f-109">**cbData**</span></span>

<span data-ttu-id="9f71f-110">Benutzer DataSet im Datensatz.</span><span class="sxs-lookup"><span data-stu-id="9f71f-110">User data set in the record.</span></span>

<span data-ttu-id="9f71f-111">**Hinweis**  Die Schlüsselgröße ist in diesem nicht enthalten.</span><span class="sxs-lookup"><span data-stu-id="9f71f-111">**Note**  The key size is not included in this.</span></span>

<span data-ttu-id="9f71f-112">**cblongvaluedata**</span><span class="sxs-lookup"><span data-stu-id="9f71f-112">**cbLongValueData**</span></span>

<span data-ttu-id="9f71f-113">Benutzerdaten, die dem Datensatz zugeordnet sind, aber in der Struktur mit langem Wert gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="9f71f-113">User data associated with the record but stored in the long-value tree.</span></span>

<span data-ttu-id="9f71f-114">**Hinweis**  Dabei werden keine systeminternen langen Werte gezählt.</span><span class="sxs-lookup"><span data-stu-id="9f71f-114">**Note**  This does not count intrinsic long-values.</span></span>

<span data-ttu-id="9f71f-115">**cboverhead**</span><span class="sxs-lookup"><span data-stu-id="9f71f-115">**cbOverhead**</span></span>

<span data-ttu-id="9f71f-116">Der Aufwand der ESE-Daten Satzstruktur für diesen Datensatz.</span><span class="sxs-lookup"><span data-stu-id="9f71f-116">The overhead of the ESE record structure for this record.</span></span> <span data-ttu-id="9f71f-117">Dazu gehört auch die Schlüsselgröße des Datensatzes.</span><span class="sxs-lookup"><span data-stu-id="9f71f-117">This includes the record's key size.</span></span>

<span data-ttu-id="9f71f-118">**cblongvalueoverhead**</span><span class="sxs-lookup"><span data-stu-id="9f71f-118">**cbLongValueOverhead**</span></span>

<span data-ttu-id="9f71f-119">Der Aufwand für die Daten mit langen Werten.</span><span class="sxs-lookup"><span data-stu-id="9f71f-119">The overhead of the long-value data.</span></span>

<span data-ttu-id="9f71f-120">**Hinweis**  Dabei werden keine systeminternen langen Werte gezählt.</span><span class="sxs-lookup"><span data-stu-id="9f71f-120">**Note**  This does not count intrinsic long-values.</span></span>

<span data-ttu-id="9f71f-121">**cnontaggedcolumns**</span><span class="sxs-lookup"><span data-stu-id="9f71f-121">**cNonTaggedColumns**</span></span>

<span data-ttu-id="9f71f-122">Die Gesamtanzahl der in diesem Datensatz festgelegten Fixed-und variable-Spalten.</span><span class="sxs-lookup"><span data-stu-id="9f71f-122">Total number of fixed and variable columns set in this record.</span></span>

<span data-ttu-id="9f71f-123">**ctaggedcolumns**</span><span class="sxs-lookup"><span data-stu-id="9f71f-123">**cTaggedColumns**</span></span>

<span data-ttu-id="9f71f-124">Die Gesamtanzahl der in diesem Datensatz festgelegten markierten Spalten.</span><span class="sxs-lookup"><span data-stu-id="9f71f-124">Total number of tagged columns set in this record.</span></span>

<span data-ttu-id="9f71f-125">**clongvalues**</span><span class="sxs-lookup"><span data-stu-id="9f71f-125">**cLongValues**</span></span>

<span data-ttu-id="9f71f-126">Gesamtzahl der langen Werte, die in der Struktur mit langem Wert für diesen Datensatz gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="9f71f-126">Total number of long values stored in the long-value tree for this record.</span></span>

<span data-ttu-id="9f71f-127">**Hinweis**  Dabei werden keine systeminternen langen Werte gezählt.</span><span class="sxs-lookup"><span data-stu-id="9f71f-127">**Note**  This does not count intrinsic long-values.</span></span>

<span data-ttu-id="9f71f-128">**cmultivalues**</span><span class="sxs-lookup"><span data-stu-id="9f71f-128">**cMultiValues**</span></span>

<span data-ttu-id="9f71f-129">Die Ansammlung der Gesamtzahl der Werte, die über den ersten für alle Spalten im Datensatz hinausgehen.</span><span class="sxs-lookup"><span data-stu-id="9f71f-129">The accumulation of the total number of values beyond the first for all columns in the record.</span></span>

### <a name="remarks"></a><span data-ttu-id="9f71f-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9f71f-130">Remarks</span></span>

<span data-ttu-id="9f71f-131">Die Gesamtanzahl der Werte im Datensatz wäre **cmultivalues**  +  **cnontaggedcolumns**  +  **ctaggedcolumns**.</span><span class="sxs-lookup"><span data-stu-id="9f71f-131">The total number of values in the record would be **cMultiValues** + **cNonTaggedColumns** + **cTaggedColumns**.</span></span>

### <a name="requirements"></a><span data-ttu-id="9f71f-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9f71f-132">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9f71f-133"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="9f71f-133"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="9f71f-134">Erfordert Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="9f71f-134">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f71f-135"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="9f71f-135"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="9f71f-136">Erfordert Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="9f71f-136">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f71f-137"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="9f71f-137"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="9f71f-138">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="9f71f-138">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="9f71f-139">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="9f71f-139">See Also</span></span>

[<span data-ttu-id="9f71f-140">Jetgetrecordsize</span><span class="sxs-lookup"><span data-stu-id="9f71f-140">JetGetRecordSize</span></span>](./jetgetrecordsize-function.md)
