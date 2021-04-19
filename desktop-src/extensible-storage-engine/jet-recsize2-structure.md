---
description: 'Weitere Informationen finden Sie hier: JET_RECSIZE2 Struktur'
title: JET_RECSIZE2 Struktur
TOCTitle: JET_RECSIZE2 Structure
ms:assetid: 02a13b5b-d904-49b2-baaa-c60328d70290
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269174(v=EXCHG.10)
ms:contentKeyID: 32765477
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
ms.openlocfilehash: 2fd16480f0ec059c977d07f8e445a35094c5f2fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362355"
---
# <a name="jet_recsize2-structure"></a><span data-ttu-id="71f93-103">JET_RECSIZE2 Struktur</span><span class="sxs-lookup"><span data-stu-id="71f93-103">JET_RECSIZE2 Structure</span></span>


<span data-ttu-id="71f93-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="71f93-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_recsize2-structure"></a><span data-ttu-id="71f93-105">JET_RECSIZE2 Struktur</span><span class="sxs-lookup"><span data-stu-id="71f93-105">JET_RECSIZE2 Structure</span></span>

<span data-ttu-id="71f93-106">Die **JET_RECSIZE2** Struktur wird von [JetGetRecordSize2](./jetgetrecordsize2-function.md) verwendet, um Informationen über die Verwendungs Anforderungen eines Datensatzes im Benutzerdaten Bereich, die Anzahl der Satz Spalten, die Anzahl der Werte und den mehr Aufwand für die ESE-Daten Satzstruktur zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="71f93-106">The **JET_RECSIZE2** structure is used by [JetGetRecordSize2](./jetgetrecordsize2-function.md) to return information about a record's usage requirements in user data space, number of set columns, number of values, and ESE record structure overhead space.</span></span>

<span data-ttu-id="71f93-107">**Windows 7:** Die **JET_RECSIZE2** Struktur wird im Windows 7-Betriebssystem eingeführt.</span><span class="sxs-lookup"><span data-stu-id="71f93-107">**Windows 7:** The **JET_RECSIZE2** structure is introduced in the Windows 7 operating system.</span></span>

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
      unsigned __int64 cCompressedColumns;
      unsigned __int64 cbDataCompressed;
      unsigned __int64 cbLongValueDataCompressed;
    } JET_RECSIZE2;
```

### <a name="members"></a><span data-ttu-id="71f93-108">Member</span><span class="sxs-lookup"><span data-stu-id="71f93-108">Members</span></span>

<span data-ttu-id="71f93-109">**cbData**</span><span class="sxs-lookup"><span data-stu-id="71f93-109">**cbData**</span></span>

<span data-ttu-id="71f93-110">Benutzer DataSet im Datensatz.</span><span class="sxs-lookup"><span data-stu-id="71f93-110">User data set in the record.</span></span>

<span data-ttu-id="71f93-111">**Hinweis**  Die Schlüsselgröße ist in diesem nicht enthalten.</span><span class="sxs-lookup"><span data-stu-id="71f93-111">**Note**  The key size is not included in this.</span></span>

<span data-ttu-id="71f93-112">**cblongvaluedata**</span><span class="sxs-lookup"><span data-stu-id="71f93-112">**cbLongValueData**</span></span>

<span data-ttu-id="71f93-113">Benutzerdaten, die dem Datensatz zugeordnet sind, aber in der Struktur mit langem Wert gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="71f93-113">User data associated with the record but stored in the long-value tree.</span></span>

<span data-ttu-id="71f93-114">**Hinweis**  Dabei werden keine systeminternen langen Werte gezählt.</span><span class="sxs-lookup"><span data-stu-id="71f93-114">**Note**  This does not count intrinsic long-values.</span></span>

<span data-ttu-id="71f93-115">**cboverhead**</span><span class="sxs-lookup"><span data-stu-id="71f93-115">**cbOverhead**</span></span>

<span data-ttu-id="71f93-116">Der Aufwand der ESE-Daten Satzstruktur für diesen Datensatz.</span><span class="sxs-lookup"><span data-stu-id="71f93-116">The overhead of the ESE record structure for this record.</span></span> <span data-ttu-id="71f93-117">Dazu gehört auch die Schlüsselgröße des Datensatzes.</span><span class="sxs-lookup"><span data-stu-id="71f93-117">This includes the record's key size.</span></span>

<span data-ttu-id="71f93-118">**cblongvalueoverhead**</span><span class="sxs-lookup"><span data-stu-id="71f93-118">**cbLongValueOverhead**</span></span>

<span data-ttu-id="71f93-119">Der Aufwand für die Daten mit langen Werten.</span><span class="sxs-lookup"><span data-stu-id="71f93-119">The overhead of the long-value data.</span></span>

<span data-ttu-id="71f93-120">**Hinweis**  Dabei werden keine systeminternen langen Werte gezählt.</span><span class="sxs-lookup"><span data-stu-id="71f93-120">**Note**  This does not count intrinsic long-values.</span></span>

<span data-ttu-id="71f93-121">**cnontaggedcolumns**</span><span class="sxs-lookup"><span data-stu-id="71f93-121">**cNonTaggedColumns**</span></span>

<span data-ttu-id="71f93-122">Die Gesamtanzahl der in diesem Datensatz festgelegten Fixed-und variable-Spalten.</span><span class="sxs-lookup"><span data-stu-id="71f93-122">Total number of fixed and variable columns set in this record.</span></span>

<span data-ttu-id="71f93-123">**ctaggedcolumns**</span><span class="sxs-lookup"><span data-stu-id="71f93-123">**cTaggedColumns**</span></span>

<span data-ttu-id="71f93-124">Die Gesamtanzahl der in diesem Datensatz festgelegten markierten Spalten.</span><span class="sxs-lookup"><span data-stu-id="71f93-124">Total number of tagged columns set in this record.</span></span>

<span data-ttu-id="71f93-125">**clongvalues**</span><span class="sxs-lookup"><span data-stu-id="71f93-125">**cLongValues**</span></span>

<span data-ttu-id="71f93-126">Gesamtzahl der langen Werte, die in der Struktur mit langem Wert für diesen Datensatz gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="71f93-126">Total number of long values stored in the long-value tree for this record.</span></span>

<span data-ttu-id="71f93-127">**Hinweis**  Dabei werden keine systeminternen langen Werte gezählt.</span><span class="sxs-lookup"><span data-stu-id="71f93-127">**Note**  This does not count intrinsic long-values.</span></span>

<span data-ttu-id="71f93-128">**cmultivalues**</span><span class="sxs-lookup"><span data-stu-id="71f93-128">**cMultiValues**</span></span>

<span data-ttu-id="71f93-129">Die Ansammlung der Gesamtzahl der Werte, die über den ersten für alle Spalten im Datensatz hinausgehen.</span><span class="sxs-lookup"><span data-stu-id="71f93-129">The accumulation of the total number of values beyond the first for all columns in the record.</span></span>

<span data-ttu-id="71f93-130">**ccompressedcolumns**</span><span class="sxs-lookup"><span data-stu-id="71f93-130">**cCompressedColumns**</span></span>

<span data-ttu-id="71f93-131">Die Gesamtanzahl der komprimierten Spalten.</span><span class="sxs-lookup"><span data-stu-id="71f93-131">The total number of compressed columns.</span></span>

<span data-ttu-id="71f93-132">**cbdatacompressed**</span><span class="sxs-lookup"><span data-stu-id="71f93-132">**cbDataCompressed**</span></span>

<span data-ttu-id="71f93-133">Die komprimierte Größe der Benutzerdaten in diesem Datensatz.</span><span class="sxs-lookup"><span data-stu-id="71f93-133">The compressed size of user data in this record.</span></span> <span data-ttu-id="71f93-134">Dies ist das gleiche wie bei cbData, wenn keine systeminternen langen Werte komprimiert werden.</span><span class="sxs-lookup"><span data-stu-id="71f93-134">This is the same as cbData if no intrinsic long-values are compressed.</span></span>

<span data-ttu-id="71f93-135">**cblongvaluedatacompressed**</span><span class="sxs-lookup"><span data-stu-id="71f93-135">**cbLongValueDataCompressed**</span></span>

<span data-ttu-id="71f93-136">Die komprimierte Größe von Benutzerdaten in der Struktur mit langem Wert.</span><span class="sxs-lookup"><span data-stu-id="71f93-136">The compressed size of user data in the long-value tree.</span></span> <span data-ttu-id="71f93-137">Dies entspricht den cblongvalue-Daten, wenn keine getrennten Long-Werte komprimiert werden.</span><span class="sxs-lookup"><span data-stu-id="71f93-137">This is the same as cbLongValue data if no separated long values are compressed.</span></span>

### <a name="remarks"></a><span data-ttu-id="71f93-138">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="71f93-138">Remarks</span></span>

<span data-ttu-id="71f93-139">Die Gesamtanzahl der Werte im Datensatz wäre **cmultivalues**  +  **cnontaggedcolumns**  +  **ctaggedcolumns**.</span><span class="sxs-lookup"><span data-stu-id="71f93-139">The total number of values in the record would be **cMultiValues** + **cNonTaggedColumns** + **cTaggedColumns**.</span></span>

<span data-ttu-id="71f93-140">Die logischen Daten im Datensatz sind (cbData + cblongvaluedata), und die physische Größe der Daten ist (cbdatacompressed + cblongvaluedatacompressed).</span><span class="sxs-lookup"><span data-stu-id="71f93-140">The logical data in the record is (cbData+cbLongValueData) and the physical size of the data is (cbDataCompressed+cbLongValueDataCompressed).</span></span> <span data-ttu-id="71f93-141">Dies kann zum Berechnen des Komprimierungs Verhältnisses gespeicherter Daten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="71f93-141">This can be used to calculate the compression ratio of stored data.</span></span>

### <a name="requirements"></a><span data-ttu-id="71f93-142">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="71f93-142">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="71f93-143"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="71f93-143"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="71f93-144">Erfordert das Windows Vista-Betriebssystem.</span><span class="sxs-lookup"><span data-stu-id="71f93-144">Requires Windows Vista operating system.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71f93-145"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="71f93-145"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="71f93-146">Erfordert das Betriebssystem Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="71f93-146">Requires Windows Server 2008 operating system.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="71f93-147"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="71f93-147"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="71f93-148">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="71f93-148">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="71f93-149">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="71f93-149">See Also</span></span>

[<span data-ttu-id="71f93-150">Jetgetrecordsize</span><span class="sxs-lookup"><span data-stu-id="71f93-150">JetGetRecordSize</span></span>](./jetgetrecordsize-function.md)  
[<span data-ttu-id="71f93-151">JetGetRecordSize2</span><span class="sxs-lookup"><span data-stu-id="71f93-151">JetGetRecordSize2</span></span>](./jetgetrecordsize2-function.md)
