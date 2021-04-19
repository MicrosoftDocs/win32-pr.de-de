---
description: 'Weitere Informationen zu: jetretrievecolenn-Funktion'
title: JetRetrieveColumn-Funktion
TOCTitle: JetRetrieveColumn Function
ms:assetid: 1e55063f-6033-4416-a9a6-894032fed069
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269198(v=EXCHG.10)
ms:contentKeyID: 32765501
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRetrieveColumn
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 074fb2471733afac40f76dcae1a4ce3ff38edc0d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362943"
---
# <a name="jetretrievecolumn-function"></a><span data-ttu-id="d72b1-103">JetRetrieveColumn-Funktion</span><span class="sxs-lookup"><span data-stu-id="d72b1-103">JetRetrieveColumn Function</span></span>


<span data-ttu-id="d72b1-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="d72b1-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetretrievecolumn-function"></a><span data-ttu-id="d72b1-105">JetRetrieveColumn-Funktion</span><span class="sxs-lookup"><span data-stu-id="d72b1-105">JetRetrieveColumn Function</span></span>

<span data-ttu-id="d72b1-106">Die **jetretrievecolenn** -Funktion Ruft einen einzelnen Spaltenwert aus dem aktuellen Datensatz ab.</span><span class="sxs-lookup"><span data-stu-id="d72b1-106">The **JetRetrieveColumn** function retrieves a single column value from the current record.</span></span> <span data-ttu-id="d72b1-107">Der Datensatz ist der Datensatz, der mit dem Index Eintrag an der aktuellen Position des Cursors verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="d72b1-107">The record is that record associated with the index entry at the current position of the cursor.</span></span> <span data-ttu-id="d72b1-108">Alternativ kann diese Funktion eine Spalte aus einem Datensatz abrufen, der im Cursor Kopier Puffer erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="d72b1-108">Alternatively, this function can retrieve a column from a record being created in the cursor copy buffer.</span></span> <span data-ttu-id="d72b1-109">Diese Funktion kann auch Spaltendaten aus einem Index Eintrag abrufen, der auf den aktuellen Datensatz verweist.</span><span class="sxs-lookup"><span data-stu-id="d72b1-109">This function can also retrieve column data from an index entry that references the current record.</span></span> <span data-ttu-id="d72b1-110">Zusätzlich zum Abrufen des tatsächlichen Spaltenwerts kann **jetretrievecolumschlag** auch verwendet werden, um die Größe einer Spalte abzurufen, bevor die Spaltendaten selbst abgerufen werden, sodass die Größe der Anwendungs Puffer entsprechend angepasst werden kann.</span><span class="sxs-lookup"><span data-stu-id="d72b1-110">In addition to retrieving the actual column value, **JetRetrieveColumn** can also be used to retrieve the size of a column, before retrieving the column data itself so that application buffers can be sized appropriately.</span></span>

```cpp
    JET_ERR JET_API JetRetrieveColumn(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_COLUMNID columnid,
      __out_opt     void* pvData,
      __in          unsigned long cbData,
      __out_opt     unsigned long* pcbActual,
      __in          JET_GRBIT grbit,
      __in_out_opt  JET_RETINFO* pretinfo
    );
```

### <a name="parameters"></a><span data-ttu-id="d72b1-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="d72b1-111">Parameters</span></span>

<span data-ttu-id="d72b1-112">*-sid*</span><span class="sxs-lookup"><span data-stu-id="d72b1-112">*sesid*</span></span>

<span data-ttu-id="d72b1-113">Die Sitzung, die für diesen-Befehl verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d72b1-113">The session to use for this call.</span></span>

<span data-ttu-id="d72b1-114">*TableID*</span><span class="sxs-lookup"><span data-stu-id="d72b1-114">*tableid*</span></span>

<span data-ttu-id="d72b1-115">Der Cursor, der für diesen-Befehl verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d72b1-115">The cursor to use for this call.</span></span>

<span data-ttu-id="d72b1-116">*ColumnID*</span><span class="sxs-lookup"><span data-stu-id="d72b1-116">*columnid*</span></span>

<span data-ttu-id="d72b1-117">Der [JET_COLUMNID](./jet-columnid.md) der abzurufenden Spalte.</span><span class="sxs-lookup"><span data-stu-id="d72b1-117">The [JET_COLUMNID](./jet-columnid.md) of the column to retrieve.</span></span>

<span data-ttu-id="d72b1-118">Ein *ColumnID* -Wert von 0 (null) kann angegeben werden, der sich nicht selbst auf eine einzelne Spalte bezieht.</span><span class="sxs-lookup"><span data-stu-id="d72b1-118">A *columnid* value of 0 (zero) can be given which does not itself refer to any individual column.</span></span> <span data-ttu-id="d72b1-119">Wenn *ColumnID* 0 (null) angegeben wird, werden alle markierten Spalten, sparsespalten und mehrwertigen Spalten als einzelne Spalte behandelt.</span><span class="sxs-lookup"><span data-stu-id="d72b1-119">When *columnid* 0 (zero) is given, all tagged columns, sparse, and multi-valued columns are treated as a single column.</span></span> <span data-ttu-id="d72b1-120">Dadurch wird das Abrufen aller sparsespalten ermöglicht, die in einem Datensatz vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="d72b1-120">This facilitates retrieving all sparse columns that are present in a record.</span></span>

<span data-ttu-id="d72b1-121">*pvData*</span><span class="sxs-lookup"><span data-stu-id="d72b1-121">*pvData*</span></span>

<span data-ttu-id="d72b1-122">Der Ausgabepuffer, der den Spaltenwert empfängt.</span><span class="sxs-lookup"><span data-stu-id="d72b1-122">The output buffer that receives the column value.</span></span>

<span data-ttu-id="d72b1-123">*cbData*</span><span class="sxs-lookup"><span data-stu-id="d72b1-123">*cbData*</span></span>

<span data-ttu-id="d72b1-124">Die maximale Größe des Ausgabepuffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="d72b1-124">The maximum size, in bytes, of the output buffer.</span></span>

<span data-ttu-id="d72b1-125">*pcbactual*</span><span class="sxs-lookup"><span data-stu-id="d72b1-125">*pcbActual*</span></span>

<span data-ttu-id="d72b1-126">Empfängt die tatsächliche Größe (in Bytes) des Spaltenwerts.</span><span class="sxs-lookup"><span data-stu-id="d72b1-126">Receives the actual size, in bytes, of the column value.</span></span>

<span data-ttu-id="d72b1-127">Wenn dieser Parameter **null** ist, wird die tatsächliche Größe des Spaltenwerts nicht zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d72b1-127">If this parameter is **NULL**, then the actual size of the column value will not be returned.</span></span>

<span data-ttu-id="d72b1-128">*grbit*</span><span class="sxs-lookup"><span data-stu-id="d72b1-128">*grbit*</span></span>

<span data-ttu-id="d72b1-129">Eine Gruppe von Bits, die die für diesen-Befehl zu verwendenden Optionen enthalten, die NULL oder mehr der folgenden Elemente enthalten:</span><span class="sxs-lookup"><span data-stu-id="d72b1-129">A group of bits that contain the options to be used for this call, which include zero or more of the following:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d72b1-130">Wert</span><span class="sxs-lookup"><span data-stu-id="d72b1-130">Value</span></span></p></th>
<th><p><span data-ttu-id="d72b1-131">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="d72b1-131">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d72b1-132">JET_bitRetrieveCopy</span><span class="sxs-lookup"><span data-stu-id="d72b1-132">JET_bitRetrieveCopy</span></span></p></td>
<td><p><span data-ttu-id="d72b1-133">Dieses Flag bewirkt, dass die Spalte "abrufen" den geänderten Wert anstelle des ursprünglichen Werts abruft.</span><span class="sxs-lookup"><span data-stu-id="d72b1-133">This flag causes retrieve column to retrieve the modified value instead of the original value.</span></span> <span data-ttu-id="d72b1-134">Wenn der Wert nicht geändert wurde, wird der ursprüngliche Wert abgerufen.</span><span class="sxs-lookup"><span data-stu-id="d72b1-134">If the value has not been modified, then the original value is retrieved.</span></span> <span data-ttu-id="d72b1-135">Auf diese Weise kann ein Wert, der noch nicht eingefügt oder aktualisiert wurde, beim Einfügen oder Aktualisieren eines Datensatzes abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="d72b1-135">In this way, a value that has not yet been inserted or updated may be retrieved during the operation of inserting or updating a record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d72b1-136">JET_bitRetrieveFromIndex</span><span class="sxs-lookup"><span data-stu-id="d72b1-136">JET_bitRetrieveFromIndex</span></span></p></td>
<td><p><span data-ttu-id="d72b1-137">Diese Option wird verwendet, um nach Möglichkeit Spaltenwerte aus dem Index abzurufen, ohne auf den Datensatz zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="d72b1-137">This option is used to retrieve column values from the index, if possible, without accessing the record.</span></span> <span data-ttu-id="d72b1-138">Auf diese Weise kann das unnötige Laden von Datensätzen vermieden werden, wenn benötigte Daten aus Indexeinträgen selbst verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="d72b1-138">In this way, unnecessary loading of records can be avoided when needed data is available from index entries themselves.</span></span> <span data-ttu-id="d72b1-139">In Fällen, in denen der ursprüngliche Spaltenwert nicht aus dem Index abgerufen werden kann, wird auf den Datensatz zugegriffen, und die Daten werden als normal abgerufen, weil Sie nicht rückgängig gemacht werden.</span><span class="sxs-lookup"><span data-stu-id="d72b1-139">In cases where the original column value cannot be retrieved from the index, because of irreversible transformations or data truncation, the record will be accessed and the data retrieved as normal.</span></span> <span data-ttu-id="d72b1-140">Dies ist eine Leistungs Option und sollte nur angegeben werden, wenn es wahrscheinlich ist, dass der Spaltenwert aus dem Index abgerufen werden kann.</span><span class="sxs-lookup"><span data-stu-id="d72b1-140">This is a performance option and should only be specified when it is likely that the column value can be retrieved from the index.</span></span> <span data-ttu-id="d72b1-141">Diese Option sollte nicht angegeben werden, wenn der aktuelle Index der gruppierte Index ist, da die Indexeinträge für den gruppierten Index bzw. den primären Index die Datensätze selbst sind.</span><span class="sxs-lookup"><span data-stu-id="d72b1-141">This option should not be specified if the current index is the clustered index, since the index entries for the clustered, or primary, index are the records themselves.</span></span> <span data-ttu-id="d72b1-142">Dieses Bit kann nicht festgelegt werden, wenn JET_bitRetrieveFromPrimaryBookmark ebenfalls festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="d72b1-142">This bit cannot be set if JET_bitRetrieveFromPrimaryBookmark is also set.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d72b1-143">JET_bitRetrieveFromPrimaryBookmark</span><span class="sxs-lookup"><span data-stu-id="d72b1-143">JET_bitRetrieveFromPrimaryBookmark</span></span></p></td>
<td><p><span data-ttu-id="d72b1-144">Diese Option wird zum Abrufen von Spaltenwerten aus dem Index-Lesezeichen verwendet und unterscheidet sich möglicherweise vom Indexwert, wenn eine Spalte sowohl im primären Index als auch im aktuellen Index angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="d72b1-144">This option is used to retrieve column values from the index bookmark, and may differ from the index value when a column appears both in the primary index and the current index.</span></span> <span data-ttu-id="d72b1-145">Diese Option sollte nicht angegeben werden, wenn der aktuelle Index der gruppierte Index oder der primäre Index ist.</span><span class="sxs-lookup"><span data-stu-id="d72b1-145">This option should not be specified if the current index is the clustered, or primary, index.</span></span> <span data-ttu-id="d72b1-146">Dieses Bit kann nicht festgelegt werden, wenn JET_bitRetrieveFromIndex ebenfalls festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="d72b1-146">This bit cannot be set if JET_bitRetrieveFromIndex is also set.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d72b1-147">JET_bitRetrieveTag</span><span class="sxs-lookup"><span data-stu-id="d72b1-147">JET_bitRetrieveTag</span></span></p></td>
<td><p><span data-ttu-id="d72b1-148">Diese Option wird verwendet, um die Sequenznummer eines mehrwertigen Spaltenwerts in pretinfo- &gt; itagsequence abzurufen.</span><span class="sxs-lookup"><span data-stu-id="d72b1-148">This option is used to retrieve the sequence number of a multi-valued column value in pretinfo-&gt;itagSequence.</span></span> <span data-ttu-id="d72b1-149">Das Feld itagsequence ist häufig eine Eingabe zum Abrufen von Werten mit mehrwertigen Spalten aus einem Datensatz.</span><span class="sxs-lookup"><span data-stu-id="d72b1-149">The itagSequence field is commonly an input for retrieving multi-valued column values from a record.</span></span> <span data-ttu-id="d72b1-150">Beim Abrufen von Werten aus einem Index ist es jedoch auch möglich, den Index Eintrag einer bestimmten Sequenznummer zuzuordnen und auch diese Sequenznummer abzurufen.</span><span class="sxs-lookup"><span data-stu-id="d72b1-150">However, when retrieving values from an index, it is also possible to associate the index entry with a particular sequence number and retrieve this sequence number as well.</span></span> <span data-ttu-id="d72b1-151">Das Abrufen der Sequenznummer kann ein kostspieliger Vorgang sein und sollte nur bei Bedarf ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="d72b1-151">Retrieving the sequence number can be a costly operation and should only be done if necessary.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d72b1-152">JET_bitRetrieveNull</span><span class="sxs-lookup"><span data-stu-id="d72b1-152">JET_bitRetrieveNull</span></span></p></td>
<td><p><span data-ttu-id="d72b1-153">Diese Option wird verwendet, um <strong>null</strong> -Werte für mehrwertige Spalten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="d72b1-153">This option is used to retrieve multi-valued column <strong>NULL</strong> values.</span></span> <span data-ttu-id="d72b1-154">Wenn diese Option nicht angegeben ist, werden <strong>null</strong> -Werte für mehrwertige Spalten automatisch übersprungen.</span><span class="sxs-lookup"><span data-stu-id="d72b1-154">If this option is not specified, multi-valued column <strong>NULL</strong> values will automatically be skipped.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d72b1-155">JET_bitRetrieveIgnoreDefault</span><span class="sxs-lookup"><span data-stu-id="d72b1-155">JET_bitRetrieveIgnoreDefault</span></span></p></td>
<td><p><span data-ttu-id="d72b1-156">Diese Option wirkt sich nur auf mehrwertige Spalten aus und bewirkt, dass ein <strong>null</strong> -Wert zurückgegeben wird, wenn die angeforderte Sequenznummer 1 ist und für die Spalte im Datensatz keine Werte festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="d72b1-156">This option affects only multi-valued columns and causes a <strong>NULL</strong> value to be returned when the requested sequence number is 1 and there are no set values for the column in the record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d72b1-157">JET_bitRetrieveLongId</span><span class="sxs-lookup"><span data-stu-id="d72b1-157">JET_bitRetrieveLongId</span></span></p></td>
<td><p><span data-ttu-id="d72b1-158">Dieses Flag ist nur für die interne Verwendung bestimmt und nicht für die Verwendung in der Anwendung bestimmt.</span><span class="sxs-lookup"><span data-stu-id="d72b1-158">This flag is for internal use only and is not intended to be used in your application.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d72b1-159">JET_bitRetrieveLongValueRefCount</span><span class="sxs-lookup"><span data-stu-id="d72b1-159">JET_bitRetrieveLongValueRefCount</span></span></p></td>
<td><p><span data-ttu-id="d72b1-160">Dieses Flag ist nur für die interne Verwendung bestimmt und nicht für die Verwendung in der Anwendung bestimmt.</span><span class="sxs-lookup"><span data-stu-id="d72b1-160">This flag is for internal use only and is not intended to be used in your application.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d72b1-161">JET_bitRetrieveTuple</span><span class="sxs-lookup"><span data-stu-id="d72b1-161">JET_bitRetrieveTuple</span></span></p></td>
<td><p><span data-ttu-id="d72b1-162">Dieses Flag ermöglicht das Abrufen eines tupelsegments des Indexes.</span><span class="sxs-lookup"><span data-stu-id="d72b1-162">This flag will allow the retrieval of a tuple segment of the index.</span></span> <span data-ttu-id="d72b1-163">Dieses Bit muss mit JET_bitRetrieveFromIndex angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="d72b1-163">This bit must be specified with JET_bitRetrieveFromIndex.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d72b1-164">*pretinfo*</span><span class="sxs-lookup"><span data-stu-id="d72b1-164">*pretinfo*</span></span>

<span data-ttu-id="d72b1-165">Wenn *pretinfo* als **null** angegeben wird, verhält sich die Funktion so, als ob eine *itagsequence* von 1 und ein *iblongvalue-Wert* von 0 (null) angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="d72b1-165">If *pretinfo* is give as **NULL** then the function behaves as though an *itagSequence* of 1 and an *ibLongValue* of 0 (zero) were given.</span></span> <span data-ttu-id="d72b1-166">Dies bewirkt, dass der Spalten Abruf den ersten Wert einer mehrwertigen Spalte abruft und lange Daten bei Offset 0 (null) abruft.</span><span class="sxs-lookup"><span data-stu-id="d72b1-166">This causes column retrieval to retrieve the first value of a multi-valued column, and to retrieve long data at offset 0 (zero).</span></span>

<span data-ttu-id="d72b1-167">Dieser Parameter wird verwendet, um eine oder mehrere der folgenden Punkte bereitzustellen:</span><span class="sxs-lookup"><span data-stu-id="d72b1-167">This parameter is used to provide one or more of the following:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d72b1-168">Wert</span><span class="sxs-lookup"><span data-stu-id="d72b1-168">Value</span></span></p></th>
<th><p><span data-ttu-id="d72b1-169">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="d72b1-169">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d72b1-170">iblongvalue</span><span class="sxs-lookup"><span data-stu-id="d72b1-170">ibLongValue</span></span></p></td>
<td><p><span data-ttu-id="d72b1-171">Gibt beim Abrufen eines Teils eines Spaltenwerts einen binären Offset in einen Long-Spaltenwert an.</span><span class="sxs-lookup"><span data-stu-id="d72b1-171">Gives a binary offset into a long column value when retrieving a portion of a column value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d72b1-172">itagsequence</span><span class="sxs-lookup"><span data-stu-id="d72b1-172">itagSequence</span></span></p></td>
<td><p><span data-ttu-id="d72b1-173">Gibt die Sequenznummer des gewünschten Werts für mehrwertige Spalten an.</span><span class="sxs-lookup"><span data-stu-id="d72b1-173">Gives the sequence number of the desired multi-valued column value.</span></span> <span data-ttu-id="d72b1-174">Beachten Sie, dass dieses Feld nur festgelegt wird, wenn das JET_bitRetrieveTag angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="d72b1-174">Note that this field is only set if the JET_bitRetrieveTag is specified.</span></span> <span data-ttu-id="d72b1-175">Andernfalls ist die Änderung unverändert.</span><span class="sxs-lookup"><span data-stu-id="d72b1-175">Otherwise, it is unmodified.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d72b1-176">columnidnexttaging</span><span class="sxs-lookup"><span data-stu-id="d72b1-176">columnidNextTagged</span></span></p></td>
<td><p><span data-ttu-id="d72b1-177">Gibt die Spalten-ID des zurückgegebenen Spaltenwerts zurück, wenn alle markierten Spalten, Spalten mit geringer Dichte und mehrwertigen Spalten abgerufen werden. dabei wird die Spalten-ID 0 (NULL <em>) übergeben.</em></span><span class="sxs-lookup"><span data-stu-id="d72b1-177">Returns the column ID of the returned column value when retrieving all tagged, sparse and multi-valued, columns using passing <em>columnid</em> of 0 (zero).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="d72b1-178">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d72b1-178">Return Value</span></span>

<span data-ttu-id="d72b1-179">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="d72b1-179">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="d72b1-180">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="d72b1-180">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d72b1-181">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="d72b1-181">Return code</span></span></p></th>
<th><p><span data-ttu-id="d72b1-182">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d72b1-182">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d72b1-183">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="d72b1-183">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="d72b1-184">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="d72b1-184">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d72b1-185">JET_errBadColumnId</span><span class="sxs-lookup"><span data-stu-id="d72b1-185">JET_errBadColumnId</span></span></p></td>
<td><p><span data-ttu-id="d72b1-186">Die angegebene Spalten-ID liegt außerhalb der zulässigen Beschränkungen einer Spalten-ID.</span><span class="sxs-lookup"><span data-stu-id="d72b1-186">The column ID given is outside the legal limits of a column ID.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d72b1-187">JET_errBadItagSequence</span><span class="sxs-lookup"><span data-stu-id="d72b1-187">JET_errBadItagSequence</span></span></p></td>
<td><p><span data-ttu-id="d72b1-188">Ein ungültiger Wert für eine mehrwertige spaltensequenznummer wurde in "pretinfo- &gt; itagsequence" übergeben.</span><span class="sxs-lookup"><span data-stu-id="d72b1-188">An invalid multi-valued column sequence number value has been passed in pretinfo-&gt;itagSequence.</span></span> <span data-ttu-id="d72b1-189">Gültige Werte für die Sequenznummern der mehrwertigen Spaltenwerte sind 1 oder höher.</span><span class="sxs-lookup"><span data-stu-id="d72b1-189">Valid values for the multi-valued column value sequence numbers are 1 or greater.</span></span> <span data-ttu-id="d72b1-190">Der Wert 0 (null) ist für diese Funktion ungültig.</span><span class="sxs-lookup"><span data-stu-id="d72b1-190">A value of 0 (zero) is invalid for this function.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d72b1-191">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="d72b1-191">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="d72b1-192">Der Vorgang kann nicht ausgeführt werden, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufens von <a href="gg269240(v=exchg.10).md">jetstopservice</a>beendet wurden.</span><span class="sxs-lookup"><span data-stu-id="d72b1-192">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d72b1-193">JET_errColumnNotFound</span><span class="sxs-lookup"><span data-stu-id="d72b1-193">JET_errColumnNotFound</span></span></p></td>
<td><p><span data-ttu-id="d72b1-194">Die von der angegebenen Spalte beschriebene Spalte ist in der <em>Tabelle nicht vorhanden</em> .</span><span class="sxs-lookup"><span data-stu-id="d72b1-194">The column described by the given <em>columnid</em> does not exist in the table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d72b1-195">JET_errIndexTuplesCannotRetrieveFromIndex</span><span class="sxs-lookup"><span data-stu-id="d72b1-195">JET_errIndexTuplesCannotRetrieveFromIndex</span></span></p></td>
<td><p><span data-ttu-id="d72b1-196">Als Teil Zeichenfolgen indizierte Spalten können nicht aus dem Index abgerufen werden, da in jedem Index Eintrag normalerweise nur ein kleiner Teil der Spalte vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="d72b1-196">Columns indexed as substrings cannot be retrieved from the index, since only a small portion of the column is typically present in each index entry.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d72b1-197">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="d72b1-197">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="d72b1-198">Der Vorgang kann nicht ausgeführt werden, da bei der der Sitzung zugeordneten Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität der Daten zu schützen.</span><span class="sxs-lookup"><span data-stu-id="d72b1-198">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="d72b1-199">Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d72b1-199">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d72b1-200">JET_errInvalidBufferSize</span><span class="sxs-lookup"><span data-stu-id="d72b1-200">JET_errInvalidBufferSize</span></span></p></td>
<td><p><span data-ttu-id="d72b1-201">In einigen Fällen muss der für die Spalte abrufen angegebene Puffer ausreichend groß sein, um eine beliebige Menge an Spaltenwerten zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="d72b1-201">In some cases, the buffer given for the retrieve column must be sufficiently sized in order to return any amount of the column value.</span></span> <span data-ttu-id="d72b1-202">So werden z. b. die aktualisierbaren Spalten für die Spalten Anpassung angepasst, damit Sie für den Transaktionskontext der aufrufenden Sitzung konsistent sind. diese Anpassung erfordert den vom Aufrufer bereitgestellten Puffer.</span><span class="sxs-lookup"><span data-stu-id="d72b1-202">For example, escrow updatable columns are adjusted to be consistent for the transactional context of the calling session and this adjustment requires the buffer provided by the caller.</span></span> <span data-ttu-id="d72b1-203">Wenn nicht genügend Pufferspeicher bereitgestellt wird, wird JET_errInvalidBufferSize zurückgegeben, und es werden keine Spaltendaten zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d72b1-203">If insufficient buffer space is supplied, then JET_errInvalidBufferSize is returned and no column data whatsoever is returned.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d72b1-204">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="d72b1-204">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="d72b1-205">Mindestens einer der angegebenen Parameter ist falsch.</span><span class="sxs-lookup"><span data-stu-id="d72b1-205">One or more of the parameters given is incorrect.</span></span> <span data-ttu-id="d72b1-206">Dies kann vorkommen, wenn "retinfo. cbStruct" kleiner ist als die Größe der <a href="gg294049(v=exchg.10).md">JET_RETINFO</a>.</span><span class="sxs-lookup"><span data-stu-id="d72b1-206">This can happen if the retinfo.cbStruct is smaller that the size of <a href="gg294049(v=exchg.10).md">JET_RETINFO</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d72b1-207">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="d72b1-207">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="d72b1-208">Die angegebenen Optionen sind unbekannt oder eine ungültige Kombination bekannter Biteinstellungen.</span><span class="sxs-lookup"><span data-stu-id="d72b1-208">The options supplied are unknown or an illegal combination of known bit settings.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d72b1-209">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="d72b1-209">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="d72b1-210">Der Cursor ist nicht in einem Datensatz positioniert.</span><span class="sxs-lookup"><span data-stu-id="d72b1-210">The cursor is not positioned on a record.</span></span> <span data-ttu-id="d72b1-211">Dafür sind viele verschiedene Gründe möglich.</span><span class="sxs-lookup"><span data-stu-id="d72b1-211">This can happen for many different reasons.</span></span> <span data-ttu-id="d72b1-212">Dies ist beispielsweise der Fall, wenn der Cursor aktuell nach dem letzten Datensatz im aktuellen Index positioniert ist.</span><span class="sxs-lookup"><span data-stu-id="d72b1-212">For example, this will happen if the cursor is currently positioned after the last record on the current index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d72b1-213">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="d72b1-213">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="d72b1-214">Der Vorgang kann nicht abgeschlossen werden, da die Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="d72b1-214">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d72b1-215">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="d72b1-215">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="d72b1-216">Der Vorgang kann nicht abgeschlossen werden, da für die-Instanz, die der Sitzung zugeordnet ist, ein Wiederherstellungs Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d72b1-216">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d72b1-217">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="d72b1-217">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="d72b1-218">Dieselbe Sitzung kann nicht für mehr als einen Thread gleichzeitig verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d72b1-218">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="d72b1-219"><strong>Windows XP:</strong>  Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d72b1-219"><strong>Windows XP:</strong>  This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d72b1-220">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="d72b1-220">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="d72b1-221">Der Vorgang kann nicht ausgeführt werden, da die Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="d72b1-221">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d72b1-222">JET_wrnBufferTruncated</span><span class="sxs-lookup"><span data-stu-id="d72b1-222">JET_wrnBufferTruncated</span></span></p></td>
<td><p><span data-ttu-id="d72b1-223">Der gesamte Spaltenwert konnte nicht abgerufen werden, da der angegebene Puffer kleiner ist als die Größe der Spalte.</span><span class="sxs-lookup"><span data-stu-id="d72b1-223">The entire column value could not be retrieved because the given buffer is smaller than the size of the column.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d72b1-224">JET_wrnColumnNull</span><span class="sxs-lookup"><span data-stu-id="d72b1-224">JET_wrnColumnNull</span></span></p></td>
<td><p><span data-ttu-id="d72b1-225">Der abgerufene Spaltenwert ist <strong>null</strong>.</span><span class="sxs-lookup"><span data-stu-id="d72b1-225">The column value retrieved is <strong>NULL</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d72b1-226">Bei Erfolg wird der Spaltenwert für die angegebene Spalte in den angegebenen Puffer kopiert.</span><span class="sxs-lookup"><span data-stu-id="d72b1-226">On success, the column value for the given column, is copied into the given buffer.</span></span> <span data-ttu-id="d72b1-227">Weniger als alle Spaltenwerte werden mit der Warnung kopiert, JET_wrnBufferTruncated zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="d72b1-227">Less than all of the column value is copied with the warning JET_wrnBufferTruncated is returned.</span></span> <span data-ttu-id="d72b1-228">Wenn *pcbactual* angegeben wurde, wird die tatsächliche Größe des Spaltenwerts zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d72b1-228">If the *pcbActual* was given, the actual size of the column value is returned.</span></span> <span data-ttu-id="d72b1-229">Beachten Sie, dass **null** -Werte eine Länge von 0 (null) aufweisen und die zurückgegebene Größe somit auf 0 (null) festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="d72b1-229">Note that **NULL** values have 0 (zero) length and will thus set the returned size to 0 (zero).</span></span> <span data-ttu-id="d72b1-230">Wenn es sich bei der abgerufenen Spalte um eine mehrwertige Spalte handelt und *pretinfo* angegeben wurde und JET_bitReturnTag als Option festgelegt wurde, wird die Sequenznummer des Spaltenwerts in pretinfo- \> itagsequence zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d72b1-230">If the column retrieved was a multi-valued column, and *pretinfo* was given, and JET_bitReturnTag was set as an option, then the sequence number of the column value is returned in pretinfo-\>itagSequence.</span></span>

<span data-ttu-id="d72b1-231">Bei einem Fehler wird die Cursorposition unverändert bleiben, und es werden keine Daten in den bereitgestellten Puffer kopiert.</span><span class="sxs-lookup"><span data-stu-id="d72b1-231">On failure, the cursor location is left unchanged and no data is copied into the provided buffer.</span></span>

#### <a name="remarks"></a><span data-ttu-id="d72b1-232">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d72b1-232">Remarks</span></span>

<span data-ttu-id="d72b1-233">Dieser-Befehl wird nur einmal zum Abrufen von Daten mit fester oder bekannter Größe für nicht mehrwertige Spalten verwendet.</span><span class="sxs-lookup"><span data-stu-id="d72b1-233">This call is used just once to retrieve data of fixed or known size for non-multi-valued columns.</span></span> <span data-ttu-id="d72b1-234">Wenn die Größe der Spaltendaten jedoch unbekannt ist, wird dieser Befehl in der Regel zweimal verwendet.</span><span class="sxs-lookup"><span data-stu-id="d72b1-234">However, when column data is of unknown size, this call is typically used twice.</span></span> <span data-ttu-id="d72b1-235">Sie wird zuerst aufgerufen, um die Größe der Daten zu ermitteln, damit Sie den erforderlichen Speicherplatz zuordnen kann.</span><span class="sxs-lookup"><span data-stu-id="d72b1-235">It is called first to determine the size of the data so it can allocate the necessary storage space.</span></span> <span data-ttu-id="d72b1-236">Der gleiche Rückruf wird dann erneut zum Abrufen der Spaltendaten durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="d72b1-236">Then, the same call is made again to retrieve the column data.</span></span> <span data-ttu-id="d72b1-237">Wenn die tatsächliche Anzahl von Werten unbekannt ist, weil eine Spalte mehr wertig ist, wird der-Befehl in der Regel dreimal verwendet.</span><span class="sxs-lookup"><span data-stu-id="d72b1-237">When the actual number of values is unknown, because a column is multi-valued, the call is typically used three times.</span></span> <span data-ttu-id="d72b1-238">Rufen Sie zuerst die Anzahl der Werte ab, und wiederholen Sie dann den Speicher, und rufen Sie die eigentlichen Daten ab.</span><span class="sxs-lookup"><span data-stu-id="d72b1-238">First to get the number of values and then twice more to allocate storage and retrieve the actual data.</span></span>

<span data-ttu-id="d72b1-239">Zum Abrufen aller Werte für eine mehrwertige Spalte können Sie diese Funktion wiederholt mit einem pretinfo- \> itagsequence-Wert aufrufen, beginnend bei 1 und bei jedem nachfolgenden Aufruf.</span><span class="sxs-lookup"><span data-stu-id="d72b1-239">Retrieving all the values for a multi-valued column can be done by repeatedly calling this function with a pretinfo-\>itagSequence value beginning at 1 and increasing on each subsequent call.</span></span> <span data-ttu-id="d72b1-240">Der letzte Spaltenwert muss abgerufen werden, wenn ein JET_wrnColumnNull von der Funktion zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="d72b1-240">The last column value is known to be retrieved when a JET_wrnColumnNull is returned from the function.</span></span> <span data-ttu-id="d72b1-241">Beachten Sie, dass diese Methode nicht ausgeführt werden kann, wenn die Spalte mit mehreren Werten explizite **null** -Werte enthält, die in der Wert Sequenz festgelegt sind, da diese Werte übersprungen werden.</span><span class="sxs-lookup"><span data-stu-id="d72b1-241">Note that this method cannot be done if the multi-value column has explicit **NULL** values set in its value sequence, since these values would be skipped.</span></span> <span data-ttu-id="d72b1-242">Wenn eine Anwendung alle mehrwertigen Spaltenwerte abrufen möchte, einschließlich derjenigen, die explizit auf **null** festgelegt sind, muss [jetretrievecolenumns](./jetretrievecolumns-function.md) anstelle von **jetretrievecolbin** verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d72b1-242">If an application desires to retrieve all multi-valued column values, including those explicitly set to **NULL**, then [JetRetrieveColumns](./jetretrievecolumns-function.md) must be used instead of **JetRetrieveColumn**.</span></span> <span data-ttu-id="d72b1-243">Beachten Sie, dass diese Funktion nicht die Anzahl der Werte für eine mehrwertige Funktion zurückgibt, wenn ein *itagsequence* -Wert von 0 (null) angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="d72b1-243">Note that this function does not return the number of values for a multi-valued function when an *itagSequence* value of 0 (zero) is given.</span></span> <span data-ttu-id="d72b1-244">Nur [jetretrievecolenumns](./jetretrievecolumns-function.md) gibt die Anzahl der Werte eines Spaltenwerts zurück, wenn ein *itagsequence* -Wert von 0 (null) übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="d72b1-244">Only [JetRetrieveColumns](./jetretrievecolumns-function.md) will return the number of values of a column value when an *itagSequence* value of 0 (zero) is passed.</span></span>

<span data-ttu-id="d72b1-245">Wenn diese Funktion auf Transaktionsebene 0 (null) aufgerufen wird, z. b. wenn sich die Aufruf Sitzung nicht selbst in einer Transaktion befindet, wird eine Transaktion in der Funktion geöffnet und geschlossen.</span><span class="sxs-lookup"><span data-stu-id="d72b1-245">If this function is called at transaction level 0 (zero), for example, the calling session is not itself in a transaction, then a transaction is opened and closed within the function.</span></span> <span data-ttu-id="d72b1-246">Der Zweck dieses Werts besteht darin, konsistente Ergebnisse zurückzugeben, wenn ein Long-Wert Datenbankseiten umfasst.</span><span class="sxs-lookup"><span data-stu-id="d72b1-246">The purpose of this is to return consistent results in the case that a long value spans database pages.</span></span> <span data-ttu-id="d72b1-247">Beachten Sie, dass die Transaktion zwischen Funktionsaufrufen und einer Reihe von Aufrufen dieser Funktion freigegeben wird, wenn die Sitzung nicht in einer Transaktion ausgeführt wird und nach dem ersten Aufruf dieser Funktion aktualisierte Daten zurückgeben kann.</span><span class="sxs-lookup"><span data-stu-id="d72b1-247">Note that the transaction is released between function calls and a series of calls to this function when the session is not in a transaction may return data updated after the first call to this function.</span></span>

<span data-ttu-id="d72b1-248">Der Standard Spaltenwert wird abgerufen, wenn die Spalte nicht explizit auf einen anderen Wert festgelegt wurde, es sei denn, die JET_bitRetrieveIgnoreDefault-Option ist festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d72b1-248">The default column value will be retrieved when the column has not been set explicitly to another value, unless the JET_bitRetrieveIgnoreDefault option is set.</span></span>

<span data-ttu-id="d72b1-249">Das Abrufen des Werts der AUTOINCREMENT-Spalte aus dem Kopier Puffer vor dem Einfügen ist ein gängiges Mittel, einen Datensatz eindeutig für die Verknüpfung zu identifizieren, wenn normalisierte Daten in mehrere Tabellen eingefügt werden.</span><span class="sxs-lookup"><span data-stu-id="d72b1-249">Retrieving the autoincrement column value from the copy buffer prior to insert is a common means of identifying a record uniquely for linkage when inserting normalized data into multiple tables.</span></span> <span data-ttu-id="d72b1-250">Der AutoIncrement-Wert wird zugewiesen, wenn der Einfügevorgang beginnt und jederzeit aus dem Kopier Puffer abgerufen werden kann, bis das Update beendet ist.</span><span class="sxs-lookup"><span data-stu-id="d72b1-250">The autoincrement value is allocated when the insert operation begins and can be retrieved from the copy buffer at any time until the update is complete.</span></span>

<span data-ttu-id="d72b1-251">Wenn Sie alle markierten Spalten mit mehreren Werten und geringer Dichte abrufen, indem Sie *ColumnID* auf 0 (null) festlegen, werden die Spalten in der *ColumnID* -Reihenfolge vom niedrigsten *ColumnID* zum höchsten *ColumnID* abgerufen.</span><span class="sxs-lookup"><span data-stu-id="d72b1-251">When retrieving all tagged, multi-valued, and sparse columns, by setting *columnid* to 0 (zero), columns are retrieved in *columnid* order from lowest *columnid* to highest *columnid*.</span></span> <span data-ttu-id="d72b1-252">Die gleiche Reihenfolge von Spaltenwerten wird jedes Mal zurückgegeben, wenn Spaltenwerte abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="d72b1-252">The same order of column values is returned each time column values are retrieved.</span></span> <span data-ttu-id="d72b1-253">Die Reihenfolge ist deterministisch.</span><span class="sxs-lookup"><span data-stu-id="d72b1-253">The order is deterministic.</span></span>

#### <a name="requirements"></a><span data-ttu-id="d72b1-254">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d72b1-254">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d72b1-255"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="d72b1-255"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="d72b1-256">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="d72b1-256">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d72b1-257"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="d72b1-257"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="d72b1-258">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="d72b1-258">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d72b1-259"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="d72b1-259"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="d72b1-260">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="d72b1-260">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d72b1-261"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="d72b1-261"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="d72b1-262">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="d72b1-262">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d72b1-263"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="d72b1-263"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="d72b1-264">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="d72b1-264">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="d72b1-265">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="d72b1-265">See Also</span></span>

[<span data-ttu-id="d72b1-266">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="d72b1-266">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="d72b1-267">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="d72b1-267">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="d72b1-268">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="d72b1-268">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="d72b1-269">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="d72b1-269">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="d72b1-270">JET_RETINFO</span><span class="sxs-lookup"><span data-stu-id="d72b1-270">JET_RETINFO</span></span>](./jet-retinfo-structure.md)  
[<span data-ttu-id="d72b1-271">Jetsetcolumn</span><span class="sxs-lookup"><span data-stu-id="d72b1-271">JetSetColumn</span></span>](./jetretrievekey-function.md)  
[<span data-ttu-id="d72b1-272">Jetretrievecolumschlag</span><span class="sxs-lookup"><span data-stu-id="d72b1-272">JetRetrieveColumns</span></span>](./jetretrievecolumns-function.md)
