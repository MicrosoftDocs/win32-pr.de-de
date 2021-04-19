---
description: 'Weitere Informationen finden Sie hier: JET_RETRIEVECOLUMN Struktur'
title: JET_RETRIEVECOLUMN-Struktur
TOCTitle: JET_RETRIEVECOLUMN Structure
ms:assetid: 8e23bed5-5279-4733-b787-a073a0e8d5a5
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269334(v=EXCHG.10)
ms:contentKeyID: 32765623
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
ms.openlocfilehash: 688728e74d81055922f9e7e748dea1f30faa3548
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348216"
---
# <a name="jet_retrievecolumn-structure"></a><span data-ttu-id="a1613-103">JET_RETRIEVECOLUMN-Struktur</span><span class="sxs-lookup"><span data-stu-id="a1613-103">JET_RETRIEVECOLUMN Structure</span></span>


<span data-ttu-id="a1613-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="a1613-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_retrievecolumn-structure"></a><span data-ttu-id="a1613-105">JET_RETRIEVECOLUMN-Struktur</span><span class="sxs-lookup"><span data-stu-id="a1613-105">JET_RETRIEVECOLUMN Structure</span></span>

<span data-ttu-id="a1613-106">Die **JET_RETRIEVECOLUMN** Struktur enthält Eingabe-und Ausgabeparameter für [jetretrievecolumschlag](./jetretrievecolumns-function.md).</span><span class="sxs-lookup"><span data-stu-id="a1613-106">The **JET_RETRIEVECOLUMN** structure contains input and output parameters for [JetRetrieveColumns](./jetretrievecolumns-function.md).</span></span> <span data-ttu-id="a1613-107">Felder in der Struktur beschreiben, welche Spaltenwerte abgerufen werden sollen, wie Sie abgerufen werden und wo die Ergebnisse gespeichert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a1613-107">Fields in the structure describe what column value to retrieve, how to retrieve it, and where to save results.</span></span>

```cpp
    typedef struct {
      JET_COLUMNID columnid;
      void* pvData;
      unsigned long cbData;
      unsigned long cbActual;
      JET_GRBIT grbit;
      unsigned long ibLongValue;
      unsigned long itagSequence;
      JET_COLUMNID columnidNextTagged;
      JET_ERR err;
    } JET_RETRIEVECOLUMN;
```

### <a name="members"></a><span data-ttu-id="a1613-108">Member</span><span class="sxs-lookup"><span data-stu-id="a1613-108">Members</span></span>

<span data-ttu-id="a1613-109">**ColumnID**</span><span class="sxs-lookup"><span data-stu-id="a1613-109">**columnid**</span></span>

<span data-ttu-id="a1613-110">Der Spalten Bezeichner für die abzurufende Spalte.</span><span class="sxs-lookup"><span data-stu-id="a1613-110">The column identifier for the column to retrieve.</span></span>

<span data-ttu-id="a1613-111">**pvData**</span><span class="sxs-lookup"><span data-stu-id="a1613-111">**pvData**</span></span>

<span data-ttu-id="a1613-112">Ein Zeiger zum beginnen der Speicherung von Daten, die aus dem Spaltenwert abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="a1613-112">A pointer to begin storing data that is retrieved from the column value.</span></span>

<span data-ttu-id="a1613-113">**cbData**</span><span class="sxs-lookup"><span data-stu-id="a1613-113">**cbData**</span></span>

<span data-ttu-id="a1613-114">Die Größe der Zuordnung, beginnend bei **pvData**, in Bytes.</span><span class="sxs-lookup"><span data-stu-id="a1613-114">The size of allocation beginning at **pvData**, in bytes.</span></span> <span data-ttu-id="a1613-115">Der Vorgang zum Abrufen von Spalten speichert keine weiteren Daten in **pvData** als **cbData**.</span><span class="sxs-lookup"><span data-stu-id="a1613-115">The retrieve column operation will not store more data at **pvData** than **cbData**.</span></span>

<span data-ttu-id="a1613-116">**cbactual**</span><span class="sxs-lookup"><span data-stu-id="a1613-116">**cbActual**</span></span>

<span data-ttu-id="a1613-117">Die Größe der Daten in Bytes, die durch einen Vorgang zum Abrufen einer Spalte abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="a1613-117">The size, in bytes, of data that is retrieved by a retrieve column operation.</span></span>

<span data-ttu-id="a1613-118">**grbit**</span><span class="sxs-lookup"><span data-stu-id="a1613-118">**grbit**</span></span>

<span data-ttu-id="a1613-119">Eine Gruppe von Bits, die die Optionen für den Spalten Abruf enthalten, die NULL oder mehr der folgenden Werte enthalten.</span><span class="sxs-lookup"><span data-stu-id="a1613-119">A group of bits that contain the options for column retrieval, which include zero or more of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a1613-120">Wert</span><span class="sxs-lookup"><span data-stu-id="a1613-120">Value</span></span></p></th>
<th><p><span data-ttu-id="a1613-121">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="a1613-121">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a1613-122">JET_bitRetrieveCopy</span><span class="sxs-lookup"><span data-stu-id="a1613-122">JET_bitRetrieveCopy</span></span></p></td>
<td><p><span data-ttu-id="a1613-123">Ruft den geänderten Wert anstelle des ursprünglichen Werts ab.</span><span class="sxs-lookup"><span data-stu-id="a1613-123">Retrieves the modified value instead of the original value.</span></span> <span data-ttu-id="a1613-124">Wenn der Wert nicht geändert wurde, wird der ursprüngliche Wert abgerufen.</span><span class="sxs-lookup"><span data-stu-id="a1613-124">If the value has not been modified, then the original value is retrieved.</span></span> <span data-ttu-id="a1613-125">Auf diese Weise kann ein Wert, der noch nicht eingefügt oder aktualisiert wurde, abgerufen werden, wenn ein Datensatz eingefügt oder aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="a1613-125">In this way, a value that has not yet been inserted or updated can be retrieved when a record is inserted or updated.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1613-126">JET_bitRetrieveFromIndex</span><span class="sxs-lookup"><span data-stu-id="a1613-126">JET_bitRetrieveFromIndex</span></span></p></td>
<td><p><span data-ttu-id="a1613-127">Ruft nach Möglichkeit Spaltenwerte aus dem Index ab, ohne auf den Datensatz zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="a1613-127">Retrieves column values from the index without accessing the record, if possible.</span></span> <span data-ttu-id="a1613-128">Auf diese Weise kann das unnötige Laden von Datensätzen vermieden werden, wenn benötigte Daten aus Indexeinträgen selbst verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="a1613-128">In this way, unnecessary loading of records can be avoided when needed data is available from index entries themselves.</span></span> <span data-ttu-id="a1613-129">In Fällen, in denen der ursprüngliche Spaltenwert nicht aus dem Index abgerufen werden kann, wird auf den Datensatz zugegriffen, und die Daten werden als normal abgerufen, weil Sie nicht rückgängig gemacht werden.</span><span class="sxs-lookup"><span data-stu-id="a1613-129">In cases where the original column value cannot be retrieved from the index, because of irreversible transformations or data truncation, the record will be accessed and the data retrieved as normal.</span></span> <span data-ttu-id="a1613-130">Dies ist eine Leistungs Option und sollte nur angegeben werden, wenn es wahrscheinlich ist, dass der Spaltenwert aus dem Index abgerufen werden kann.</span><span class="sxs-lookup"><span data-stu-id="a1613-130">This is a performance option and should only be specified when it is likely that the column value can be retrieved from the index.</span></span> <span data-ttu-id="a1613-131">Diese Option sollte nicht angegeben werden, wenn der aktuelle Index der gruppierte Index ist, da die Indexeinträge für den gruppierten Index bzw. den primären Index die Datensätze selbst sind.</span><span class="sxs-lookup"><span data-stu-id="a1613-131">This option should not be specified if the current index is the clustered index, since the index entries for the clustered, or primary, index are the records themselves.</span></span> <span data-ttu-id="a1613-132">Dieses Bit kann nicht festgelegt werden, wenn JET_bitRetrieveFromPrimaryBookmark ebenfalls festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="a1613-132">This bit cannot be set if JET_bitRetrieveFromPrimaryBookmark is also set.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1613-133">JET_bitRetrieveFromPrimaryBookmark</span><span class="sxs-lookup"><span data-stu-id="a1613-133">JET_bitRetrieveFromPrimaryBookmark</span></span></p></td>
<td><p><span data-ttu-id="a1613-134">Ruft Spaltenwerte aus dem Index-Lesezeichen ab und kann sich vom Indexwert unterscheiden, wenn eine Spalte sowohl im primären Index als auch im aktuellen Index angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="a1613-134">Retrieves column values from the index bookmark, and can differ from the index value when a column appears both in the primary index and the current index.</span></span> <span data-ttu-id="a1613-135">Diese Option sollte nicht angegeben werden, wenn der aktuelle Index der gruppierte Index oder der primäre Index ist.</span><span class="sxs-lookup"><span data-stu-id="a1613-135">This option should not be specified if the current index is the clustered, or primary, index.</span></span> <span data-ttu-id="a1613-136">Dieses Bit kann nicht festgelegt werden, wenn JET_bitRetrieveFromIndex ebenfalls festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="a1613-136">This bit cannot be set if JET_bitRetrieveFromIndex is also set.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1613-137">JET_bitRetrieveTag</span><span class="sxs-lookup"><span data-stu-id="a1613-137">JET_bitRetrieveTag</span></span></p></td>
<td><p><span data-ttu-id="a1613-138">Ruft die Sequenznummer eines mehrwertigen Spaltenwerts in pretinfo- &gt; itagsequence ab.</span><span class="sxs-lookup"><span data-stu-id="a1613-138">Retrieves the sequence number of a multi-valued column value in pretinfo-&gt;itagSequence.</span></span> <span data-ttu-id="a1613-139">Das Feld "itagsequence" wird häufig als Eingabe zum Abrufen von mehrwertigen Spaltenwerten aus einem Datensatz verwendet.</span><span class="sxs-lookup"><span data-stu-id="a1613-139">The itagSequence field is often used an input for retrieving multi-valued column values from a record.</span></span> <span data-ttu-id="a1613-140">Beim Abrufen von Werten aus einem Index ist es jedoch auch möglich, den Index Eintrag einer bestimmten Sequenznummer zuzuordnen und auch diese Sequenznummer abzurufen.</span><span class="sxs-lookup"><span data-stu-id="a1613-140">However, when retrieving values from an index, it is also possible to associate the index entry with a particular sequence number and retrieve this sequence number as well.</span></span> <span data-ttu-id="a1613-141">Das Abrufen der Sequenznummer kann ein kostspieliger Vorgang sein und sollte nur bei Bedarf ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="a1613-141">Retrieving the sequence number can be a costly operation and should only be done if necessary.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1613-142">JET_ bitretrievenull</span><span class="sxs-lookup"><span data-stu-id="a1613-142">JET_ bitRetrieveNull</span></span></p></td>
<td><p><span data-ttu-id="a1613-143">Ruft NULL-Werte für mehrwertige Spalten ab.</span><span class="sxs-lookup"><span data-stu-id="a1613-143">Retrieves multi-valued column NULL values.</span></span> <span data-ttu-id="a1613-144">Wenn diese Option nicht angegeben ist, werden NULL-Werte für mehrwertige Spalten automatisch übersprungen.</span><span class="sxs-lookup"><span data-stu-id="a1613-144">If this option is not specified, multi-valued column NULL values will automatically be skipped.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1613-145">JET_bitRetrieveIgnoreDefault</span><span class="sxs-lookup"><span data-stu-id="a1613-145">JET_bitRetrieveIgnoreDefault</span></span></p></td>
<td><p><span data-ttu-id="a1613-146">Bewirkt, dass ein NULL-Wert zurückgegeben wird, wenn die angeforderte Sequenznummer 1 ist und für die Spalte im Datensatz keine Werte festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="a1613-146">Causes a NULL value to be returned when the requested sequence number is 1 and there are no set values for the column in the record.</span></span> <span data-ttu-id="a1613-147">Diese Option wirkt sich nur auf mehrwertige Spalten aus.</span><span class="sxs-lookup"><span data-stu-id="a1613-147">This option affects only multi-valued columns.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1613-148">JET_bitRetrieveLongId</span><span class="sxs-lookup"><span data-stu-id="a1613-148">JET_bitRetrieveLongId</span></span></p></td>
<td><p><span data-ttu-id="a1613-149">Dieses Flag ist nur für die interne Verwendung bestimmt und nicht für die Verwendung in der Anwendung bestimmt.</span><span class="sxs-lookup"><span data-stu-id="a1613-149">This flag is for internal use only and is not intended to be used in your application.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1613-150">JET_bitRetrieveLongValueRefCount</span><span class="sxs-lookup"><span data-stu-id="a1613-150">JET_bitRetrieveLongValueRefCount</span></span></p></td>
<td><p><span data-ttu-id="a1613-151">Dieses Flag ist nur für die interne Verwendung bestimmt und nicht für die Verwendung in der Anwendung bestimmt.</span><span class="sxs-lookup"><span data-stu-id="a1613-151">This flag is for internal use only and is not intended to be used in your application.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a1613-152">**iblongvalue**</span><span class="sxs-lookup"><span data-stu-id="a1613-152">**ibLongValue**</span></span>

<span data-ttu-id="a1613-153">Der Offset zum ersten Byte, der aus einer Spalte vom Typ [JET_coltypLongBinary](./jet-coltyp.md) oder [JET_coltypLongText](./jet-coltyp.md)abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="a1613-153">The offset to the first byte to be retrieved from a column of type [JET_coltypLongBinary](./jet-coltyp.md) or [JET_coltypLongText](./jet-coltyp.md).</span></span>

<span data-ttu-id="a1613-154">**itagsequence**</span><span class="sxs-lookup"><span data-stu-id="a1613-154">**itagSequence**</span></span>

<span data-ttu-id="a1613-155">Die Sequenznummer der Werte, die in einer mehrwertigen Spalte enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="a1613-155">The sequence number of the values that are contained in a multi-valued column.</span></span> <span data-ttu-id="a1613-156">die **itagsequence** hier in der **JET_RETRIEVECOLUMN** kann 0 sein.</span><span class="sxs-lookup"><span data-stu-id="a1613-156">**itagSequence** here in the **JET_RETRIEVECOLUMN** can be 0.</span></span> <span data-ttu-id="a1613-157">Wenn **itagsequence** den Wert 0 hat, wird anstelle von Spaltendaten die Anzahl der Instanzen einer mehrwertigen Spalte zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a1613-157">If the **itagSequence** is 0 then the number of instances of a multi-valued column are returned instead of any column data.</span></span> <span data-ttu-id="a1613-158">Ein **itagsequence** -Wert von 0 kann in Aufrufen von [jetretrievecolumschlag](./jetretrievecolumn-function.md)nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a1613-158">An **itagSequence** value of 0 cannot be used in calls to [JetRetrieveColumn](./jetretrievecolumn-function.md).</span></span>

<span data-ttu-id="a1613-159">**columnidnexttaging**</span><span class="sxs-lookup"><span data-stu-id="a1613-159">**columnidNextTagged**</span></span>

<span data-ttu-id="a1613-160">Das **ColumnID** der markierten Spalte, der mehrwertigen Spalte oder der sparsespalte, wenn alle markierten Spalten abgerufen werden, indem 0 als **ColumnID** an [jetretrievecolbin](./jetretrievecolumn-function.md)übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="a1613-160">The **columnid** of the tagged, multi-valued, or sparse column when all tagged columns are retrieved by passing 0 as the **columnid** to [JetRetrieveColumn](./jetretrievecolumn-function.md).</span></span>

<span data-ttu-id="a1613-161">**irre**</span><span class="sxs-lookup"><span data-stu-id="a1613-161">**err**</span></span>

<span data-ttu-id="a1613-162">Fehlercodes und Warnungen, die beim Abrufen der Spalte zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="a1613-162">Error codes and warnings returned from the retrieval of the column.</span></span>

### <a name="requirements"></a><span data-ttu-id="a1613-163">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a1613-163">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a1613-164"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="a1613-164"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="a1613-165">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="a1613-165">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1613-166"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="a1613-166"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="a1613-167">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="a1613-167">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1613-168"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="a1613-168"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="a1613-169">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="a1613-169">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="a1613-170">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="a1613-170">See Also</span></span>

[<span data-ttu-id="a1613-171">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="a1613-171">JET_COLTYP</span></span>](./jet-coltyp.md)  
[<span data-ttu-id="a1613-172">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="a1613-172">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="a1613-173">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="a1613-173">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="a1613-174">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="a1613-174">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="a1613-175">JET_RETRIEVECOLUMN</span><span class="sxs-lookup"><span data-stu-id="a1613-175">JET_RETRIEVECOLUMN</span></span>]()  
[<span data-ttu-id="a1613-176">Jetretrievecolumschlag</span><span class="sxs-lookup"><span data-stu-id="a1613-176">JetRetrieveColumn</span></span>](./jetretrievecolumn-function.md)  
[<span data-ttu-id="a1613-177">Jetretrievecolumschlag</span><span class="sxs-lookup"><span data-stu-id="a1613-177">JetRetrieveColumns</span></span>](./jetretrievecolumns-function.md)
