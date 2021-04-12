---
description: 'Weitere Informationen zu: jetenreeratecolumschlag-Funktion'
title: JetEnumerateColumns-Funktion
TOCTitle: JetEnumerateColumns Function
ms:assetid: 8413d056-cdb1-420e-9dd3-7280ad510165
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269321(v=EXCHG.10)
ms:contentKeyID: 32765611
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetEnumerateColumns
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b913fb970232ca6f0fc21eb846df85e1db684f45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217053"
---
# <a name="jetenumeratecolumns-function"></a><span data-ttu-id="83bdd-103">JetEnumerateColumns-Funktion</span><span class="sxs-lookup"><span data-stu-id="83bdd-103">JetEnumerateColumns Function</span></span>


<span data-ttu-id="83bdd-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="83bdd-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetenumeratecolumns-function"></a><span data-ttu-id="83bdd-105">JetEnumerateColumns-Funktion</span><span class="sxs-lookup"><span data-stu-id="83bdd-105">JetEnumerateColumns Function</span></span>

<span data-ttu-id="83bdd-106">Die **jetenenumeratecolumschlag** -Funktion ruft effizient eine Gruppe von Spalten und deren Werten aus dem aktuellen Datensatz eines Cursors oder dem Kopier Puffer dieses Cursors ab.</span><span class="sxs-lookup"><span data-stu-id="83bdd-106">The **JetEnumerateColumns** function efficiently retrieves a set of columns and their values from the current record of a cursor or the copy buffer of that cursor.</span></span> <span data-ttu-id="83bdd-107">Die abgerufenen Spalten und Werte können durch eine Liste von Spalten-IDs, *itagsequence* -Nummern und anderen Merkmalen eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="83bdd-107">The columns and values retrieved can be restricted by a list of column IDs, *itagSequence* numbers, and other characteristics.</span></span> <span data-ttu-id="83bdd-108">Diese Spalten Abruf-API ist eindeutig, da Sie Informationen in dynamisch zugewiesener Speicher zurückgibt, die mit einem vom Benutzer bereitgestellten [rezuordnungskompatiblen](/cpp/c-runtime-library/reference/realloc?view=vs-2019) Rückruf abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="83bdd-108">This column retrieval API is unique in that it returns information in dynamically allocated memory that is obtained using a user-provided [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) compatible callback.</span></span> <span data-ttu-id="83bdd-109">Diese neue Flexibilität ermöglicht das effiziente Abrufen von Spaltendaten mit bestimmten Merkmalen (z. b. Größe und Multiplizität), die dem Aufrufer unbekannt sind.</span><span class="sxs-lookup"><span data-stu-id="83bdd-109">This new flexibility permits the efficient retrieval of column data with specific characteristics (such as size and multiplicity) that are unknown to the caller.</span></span> <span data-ttu-id="83bdd-110">Dadurch ist es nicht mehr erforderlich, die Ermittlungs Modi [jetretrievecolumgen](./jetretrievecolumn-function.md) zu verwenden, um die Eigenschaften zu bestimmen, um einen letzten Rückruf für [jetretrievecolumschlag](./jetretrievecolumn-function.md) einzurichten, mit dem die gewünschten Daten erfolgreich abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="83bdd-110">This eliminates the need for the use of the discovery modes of [JetRetrieveColumn](./jetretrievecolumn-function.md) to determine those characteristics in order to setup a final call to [JetRetrieveColumn](./jetretrievecolumn-function.md) that will successfully retrieve the desired data.</span></span>

<span data-ttu-id="83bdd-111">**Windows XP: jetenreeratecolumschlag** wird in Windows XP eingeführt.</span><span class="sxs-lookup"><span data-stu-id="83bdd-111">**Windows XP:  JetEnumerateColumns** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetEnumerateColumns(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          unsigned long cEnumColumnId,
      __in_opt      JET_ENUMCOLUMNID* rgEnumColumnId,
      __out         unsigned long* pcEnumColumn,
      __out         JET_ENUMCOLUMN** prgEnumColumn,
      __in          JET_PFNREALLOC pfnRealloc,
      __in          void* pvReallocContext,
      __in          unsigned long cbDataMost,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="83bdd-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="83bdd-112">Parameters</span></span>

<span data-ttu-id="83bdd-113">*-sid*</span><span class="sxs-lookup"><span data-stu-id="83bdd-113">*sesid*</span></span>

<span data-ttu-id="83bdd-114">Die Sitzung, die für diesen-Befehl verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="83bdd-114">The session to use for this call.</span></span>

<span data-ttu-id="83bdd-115">*TableID*</span><span class="sxs-lookup"><span data-stu-id="83bdd-115">*tableid*</span></span>

<span data-ttu-id="83bdd-116">Der Cursor, der für diesen-Befehl verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="83bdd-116">The cursor to use for this call.</span></span>

<span data-ttu-id="83bdd-117">*cenum ColumnID*</span><span class="sxs-lookup"><span data-stu-id="83bdd-117">*cEnumColumnId*</span></span>

<span data-ttu-id="83bdd-118">Ein Array von Spalten-IDs, von denen jedes ein optionales Array von *itagsequence* -Zahlen auflistet.</span><span class="sxs-lookup"><span data-stu-id="83bdd-118">An array of column IDs, each with an optional array of *itagSequence* numbers to enumerate.</span></span>

<span data-ttu-id="83bdd-119">Wenn *cenumcolumnid* gleich 0 (null) ist, wird *rgenumcolumnid* ignoriert, und alle Spaltenwerte werden aufgezählt und an den Aufrufer zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="83bdd-119">If *cEnumColumnId* is 0 (zero) then *rgEnumColumnId* is ignored and all column values are enumerated and returned to the caller.</span></span> <span data-ttu-id="83bdd-120">Wenn ein Element des Spalten-ID-Arrays auf eine Spalten-ID von 0 (null) verweist, wird die Enumeration dieser Spalte übersprungen, und ein entsprechender Slot in der Ausgabe wird mit dem Spalten Status JET_wrnColumnSkipped generiert.</span><span class="sxs-lookup"><span data-stu-id="83bdd-120">If an element of the column ID array refers to a column ID of 0 (zero) then enumeration of that column is skipped and a corresponding slot in the output will be generated with a column status of JET_wrnColumnSkipped.</span></span>

<span data-ttu-id="83bdd-121">Wenn *ctagsequence* für ein angegebenes Element des Spalten-ID-Arrays 0 (null) ist, wird *rgtagsequence* ignoriert, und alle Spaltenwerte für diese Spalten-ID werden aufgezählt und an den Aufrufer zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="83bdd-121">If *ctagSequence* is 0 (zero) for a given element of the column ID array then *rgtagSequence* is ignored and all column values for that column ID are enumerated and returned to the caller.</span></span> <span data-ttu-id="83bdd-122">Wenn ein Element eines *itagsequence* -Zahlen Arrays auf eine *itagsequence* -Nummer von 0 (null) verweist, wird die Enumeration dieser *itagsequence* -Nummer ausgelassen, und ein entsprechender Slot in der Ausgabe wird mit dem Spaltenwert Status JET_wrnColumnSkipped generiert.</span><span class="sxs-lookup"><span data-stu-id="83bdd-122">If an element of an *itagSequence* number array refers to a *itagSequence* number of 0 (zero) then the enumeration of that *itagSequence* number is skipped and a corresponding slot in the output will be generated with a column value status of JET_wrnColumnSkipped.</span></span>

<span data-ttu-id="83bdd-123">*rgenum ColumnID*</span><span class="sxs-lookup"><span data-stu-id="83bdd-123">*rgEnumColumnId*</span></span>

<span data-ttu-id="83bdd-124">Siehe *cenum ColumnID*.</span><span class="sxs-lookup"><span data-stu-id="83bdd-124">See *cEnumColumnId*.</span></span>

<span data-ttu-id="83bdd-125">*pcenumcolumn*</span><span class="sxs-lookup"><span data-stu-id="83bdd-125">*pcEnumColumn*</span></span>

<span data-ttu-id="83bdd-126">Gibt das aufgelistete Array von Spalten und deren Werten im Arbeitsspeicher zurück, die über den bereitgestellten *itagsequence* -kompatiblen Rückruf zugeordnet wurden.</span><span class="sxs-lookup"><span data-stu-id="83bdd-126">Returns the enumerated array of columns and their values in memory allocated through the provided *itagSequence* compatible callback.</span></span>

<span data-ttu-id="83bdd-127">Wenn bei der Eingabe ein Array von Spalten-IDs angefordert wird, entsprechen die Reihenfolge und Größe des Ausgabe Arrays der Reihenfolge und Größe des Eingabe Arrays.</span><span class="sxs-lookup"><span data-stu-id="83bdd-127">If an array of column IDs is requested on input then the order and size of the output array will reflect the order and size of the input array.</span></span> <span data-ttu-id="83bdd-128">Wenn ein Array von *itagsequence* -Nummern für eine bestimmte Spalten-ID bei der Eingabe angefordert wird, entsprechen die Reihenfolge und Größe des Ausgabe Arrays der Spaltenwerte für diese Spalte der Reihenfolge und Größe des Eingabe Arrays.</span><span class="sxs-lookup"><span data-stu-id="83bdd-128">Similarly, if an array of *itagSequence* numbers is requested for a particular column ID on input then the order and size of the output array of column values for that column will reflect the order and size of the input array.</span></span>

<span data-ttu-id="83bdd-129">Die Ausgabeparameter werden bei jedem Fehler auf 0 (null) und **null** festgelegt, ausgenommen JET_errBadColumnId und JET_errColumnNotFound.</span><span class="sxs-lookup"><span data-stu-id="83bdd-129">The output parameters are set to 0 (zero) and **NULL** on any error except for JET_errBadColumnId and JET_errColumnNotFound.</span></span> <span data-ttu-id="83bdd-130">Wenn diese Fehler zurückgegeben werden, sind die Ausgabedaten gültig und für alle außer den betroffenen Spalten-IDs vollständig.</span><span class="sxs-lookup"><span data-stu-id="83bdd-130">When these errors are returned, the output data is valid and complete for all but the affected column IDs.</span></span> <span data-ttu-id="83bdd-131">Der Statuscode für jede der betroffenen Spalten-IDs wird auf einen der folgenden Fehler festgelegt, damit der Aufrufer ermitteln kann, welche Spalten-IDs schlecht waren, und möglicherweise Korrekturmaßnahmen ergreifen.</span><span class="sxs-lookup"><span data-stu-id="83bdd-131">The status code for each of the affected column IDs is set to one of these errors so that the caller may determine which column IDs were bad and potentially take corrective action.</span></span>

<span data-ttu-id="83bdd-132">*prgenencolumn*</span><span class="sxs-lookup"><span data-stu-id="83bdd-132">*prgEnumColumn*</span></span>

<span data-ttu-id="83bdd-133">Siehe *pcenumcolumn*.</span><span class="sxs-lookup"><span data-stu-id="83bdd-133">See *pcEnumColumn*.</span></span>

<span data-ttu-id="83bdd-134">*pfnrezuweisung*</span><span class="sxs-lookup"><span data-stu-id="83bdd-134">*pfnRealloc*</span></span>

<span data-ttu-id="83bdd-135">Identifiziert einen [erneut zuordnenden](/cpp/c-runtime-library/reference/realloc?view=vs-2019) kompatiblen Rückruf und einen optionalen Kontext Zeiger, der zum Zuordnen von Arbeitsspeicher für das Ausgabe Array von Spalten und deren Werten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="83bdd-135">Identifies a [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) compatible callback and an optional context pointer used to allocate memory for the output array of columns and their values.</span></span>

<span data-ttu-id="83bdd-136">*pvrezuccontext*</span><span class="sxs-lookup"><span data-stu-id="83bdd-136">*pvReallocContext*</span></span>

<span data-ttu-id="83bdd-137">Weitere Informationen finden Sie unter *pfnrezuweisung*.</span><span class="sxs-lookup"><span data-stu-id="83bdd-137">See *pfnRealloc*.</span></span>

<span data-ttu-id="83bdd-138">*cbdatamost*</span><span class="sxs-lookup"><span data-stu-id="83bdd-138">*cbDataMost*</span></span>

<span data-ttu-id="83bdd-139">Legt eine Obergrenze für die Menge der Daten fest, die von einer Long-Text-oder Long Binary-Spalte zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="83bdd-139">Sets a cap on the amount of data to return from a long text or long binary column.</span></span>

<span data-ttu-id="83bdd-140">Dieser Parameter kann verwendet werden, um die Enumeration eines extrem großen Spaltenwerts zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="83bdd-140">This parameter can be used to prevent the enumeration of an extremely large column value.</span></span> <span data-ttu-id="83bdd-141">Normalerweise kann eine solche Enumeration beim API-Befehl mit JET_errOutOfMemory fehlschlagen.</span><span class="sxs-lookup"><span data-stu-id="83bdd-141">Ordinarily, such an enumeration might fail the API call with JET_errOutOfMemory.</span></span> <span data-ttu-id="83bdd-142">Wenn ein großer Spaltenwert auf diese Weise abgeschnitten wird, wird der Status des Spaltenwerts JET_wrnColumnTruncated.</span><span class="sxs-lookup"><span data-stu-id="83bdd-142">If a large column value is truncated in such a manner then the column value's status will be JET_wrnColumnTruncated.</span></span>

<span data-ttu-id="83bdd-143">*grbit*</span><span class="sxs-lookup"><span data-stu-id="83bdd-143">*grbit*</span></span>

<span data-ttu-id="83bdd-144">Eine Gruppe von Bits, die NULL oder mehr der folgenden Optionen angibt.</span><span class="sxs-lookup"><span data-stu-id="83bdd-144">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="83bdd-145">Wert</span><span class="sxs-lookup"><span data-stu-id="83bdd-145">Value</span></span></p></th>
<th><p><span data-ttu-id="83bdd-146">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="83bdd-146">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="83bdd-147">JET_bitEnumerateCompressOutput</span><span class="sxs-lookup"><span data-stu-id="83bdd-147">JET_bitEnumerateCompressOutput</span></span></p></td>
<td><p><span data-ttu-id="83bdd-148">Beim Aufzählen von Spaltenwerten können alle Spalten, für die wir alle Werte abrufen und nur einen nicht-NULL-Spaltenwert aufweisen, in einem komprimierten Format zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="83bdd-148">When enumerating column values, all columns for which we are retrieving all values and that have only one non-NULL column value may be returned in a compressed format.</span></span> <span data-ttu-id="83bdd-149">Der Status dieser Spalten wird auf JET_wrnColumnSingleValue festgelegt, und die Größe des Spaltenwerts und der Arbeitsspeicher, der den Spaltenwert enthält, werden direkt in der <a href="gg294138(v=exchg.10).md">JET_ENUMCOLUMN</a> Struktur zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="83bdd-149">The status for such columns will be set to JET_wrnColumnSingleValue and the size of the column value and the memory containing the column value will be returned directly in the <a href="gg294138(v=exchg.10).md">JET_ENUMCOLUMN</a> structure.</span></span> <span data-ttu-id="83bdd-150">Es ist nicht sichergestellt, dass alle berechtigten Spalten auf diese Weise komprimiert werden.</span><span class="sxs-lookup"><span data-stu-id="83bdd-150">It is not guaranteed that all eligible columns are compressed in this manner.</span></span> <span data-ttu-id="83bdd-151">Weitere Informationen finden Sie unter <a href="gg294138(v=exchg.10).md">JET_ENUMCOLUMN</a> .</span><span class="sxs-lookup"><span data-stu-id="83bdd-151">See <a href="gg294138(v=exchg.10).md">JET_ENUMCOLUMN</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83bdd-152">JET_bitEnumerateCopy</span><span class="sxs-lookup"><span data-stu-id="83bdd-152">JET_bitEnumerateCopy</span></span></p></td>
<td><p><span data-ttu-id="83bdd-153">Diese Option gibt an, dass die geänderten Spaltenwerte des Datensatzes anstelle der ursprünglichen Spaltenwerte aufgezählt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="83bdd-153">This option indicates that the modified column values of the record should be enumerated rather than the original column values.</span></span> <span data-ttu-id="83bdd-154">Wenn ein Spaltenwert nicht geändert wurde, wird der ursprüngliche Spaltenwert aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="83bdd-154">If a column value has not been modified, the original column value is enumerated.</span></span> <span data-ttu-id="83bdd-155">Auf diese Weise kann ein Spaltenwert, der noch nicht eingefügt oder aktualisiert wurde, beim Einfügen oder Aktualisieren eines Datensatzes aufgezählt werden.</span><span class="sxs-lookup"><span data-stu-id="83bdd-155">In this way, a column value that has not yet been inserted or updated may be enumerated when inserting or updating a record.</span></span></p>
<p><span data-ttu-id="83bdd-156">Diese Option ist mit JET_bitRetrieveCopy identisch, wenn Sie mit <a href="gg269198(v=exchg.10).md">jetretrievecolumschlag</a> oder <a href="gg294135(v=exchg.10).md">jetretrievecolumschlag</a>verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="83bdd-156">This option is identical to JET_bitRetrieveCopy when used with <a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a> or <a href="gg294135(v=exchg.10).md">JetRetrieveColumns</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83bdd-157">JET_bitEnumerateIgnoreDefault</span><span class="sxs-lookup"><span data-stu-id="83bdd-157">JET_bitEnumerateIgnoreDefault</span></span></p></td>
<td><p><span data-ttu-id="83bdd-158">Wenn eine bestimmte Spalte nicht im Datensatz vorhanden ist, wird kein Spaltenwert zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="83bdd-158">If a given column is not present in the record then no column value will be returned.</span></span> <span data-ttu-id="83bdd-159">Normalerweise würde der Standardwert für die Spalte, sofern vorhanden, in diesem Fall zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="83bdd-159">Ordinarily, the default value for the column, if any, would be returned in this case.</span></span> <span data-ttu-id="83bdd-160">Wenn die Spalte auf einen anderen Wert als den Standardwert festgelegt ist, wird ein anderer Wert zurückgegeben (d. h., wenn eine Spalte mit einem Standardwert explizit auf <strong>null</strong> festgelegt ist, wird ein <strong>null</strong> -Wert als Wert für diese Spalte zurückgegeben).</span><span class="sxs-lookup"><span data-stu-id="83bdd-160">It is guaranteed that if the column is set to a value different than the default value then that different value will be returned (that is, if a column with a default value is explicitly set to <strong>NULL</strong> then a <strong>NULL</strong> will be returned as the value for that column).</span></span> <span data-ttu-id="83bdd-161">Beachten Sie, dass auch dann, wenn diese Option angefordert wird, immer noch ein Spaltenwert angezeigt wird, der dem Standardwert entspricht.</span><span class="sxs-lookup"><span data-stu-id="83bdd-161">Note that, even if this option is requested, it is still possible to see a column value that happens to be equal to the default value.</span></span> <span data-ttu-id="83bdd-162">Es wird nicht versucht, Spaltenwerte zu entfernen, die ihren Standardwerten entsprechen.</span><span class="sxs-lookup"><span data-stu-id="83bdd-162">No effort is made to remove column values that match their default values.</span></span></p>
<p><span data-ttu-id="83bdd-163">Beachten Sie, dass sich diese Option auf die Ausgabe von <strong>jetenreeratecolumschlag</strong> auswirkt, wenn Sie mit JET_bitEnumeratePresenceOnly oder JET_bitEnumerateTaggedOnly verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="83bdd-163">It is important to note that this option affects the output of <strong>JetEnumerateColumns</strong> when used with JET_bitEnumeratePresenceOnly or JET_bitEnumerateTaggedOnly.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83bdd-164">JET_bitEnumerateIgnoreUserDefinedDefault</span><span class="sxs-lookup"><span data-stu-id="83bdd-164">JET_bitEnumerateIgnoreUserDefinedDefault</span></span></p></td>
<td><p><span data-ttu-id="83bdd-165">Wenn eine bestimmte Spalte nicht im Datensatz vorhanden ist und über einen benutzerdefinierten Standardwert verfügt, wird kein Spaltenwert zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="83bdd-165">If a given column is not present in the record and it has a user defined default value then no column value will be returned.</span></span> <span data-ttu-id="83bdd-166">Mit dieser Option wird verhindert, dass der Rückruf, der den benutzerdefinierten Standardwert für die Spalte berechnet, beim Auflisten der Werte für diese Spalte aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="83bdd-166">This option will prevent the callback that computes the user defined default value for the column from being called when enumerating the values for that column.</span></span></p>
<p><span data-ttu-id="83bdd-167"><strong>Windows Server 2003 und früher:  </strong> Für Windows Server 2003 und frühere Versionen schlägt der Vorgang mit JET_errCallbackFailed fehl.</span><span class="sxs-lookup"><span data-stu-id="83bdd-167"><strong>Windows Server 2003 and earlier:  </strong>For Windows Server 2003 and earlier releases, the operation will fail with JET_errCallbackFailed.</span></span></p>
<p><span data-ttu-id="83bdd-168"><strong>Windows Server 2003 SP1:  </strong> Dieser mögliche Wert ist nur für Windows Server 2003 SP1 und spätere Betriebssysteme verfügbar.</span><span class="sxs-lookup"><span data-stu-id="83bdd-168"><strong>Windows Server 2003 SP1:  </strong>This possible value is only available for Windows Server 2003 SP1 and later operating systems.</span></span> <span data-ttu-id="83bdd-169">Wenn dieser mögliche Wert angegeben wird und die Tabelle eine Spalte mit einem benutzerdefinierten Standardwert enthält, schlägt der Vorgang mit JET_errCallbackFailed fehl.</span><span class="sxs-lookup"><span data-stu-id="83bdd-169">If this possible value is specified and the table contains a column that has a user defined default value, then the operation will fail with JET_errCallbackFailed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83bdd-170">JET_bitEnumeratePresenceOnly</span><span class="sxs-lookup"><span data-stu-id="83bdd-170">JET_bitEnumeratePresenceOnly</span></span></p></td>
<td><p><span data-ttu-id="83bdd-171">Wenn ein nicht-NULL-Wert für den angeforderten Spalten-oder Spaltenwert vorhanden ist, werden die zugehörigen Daten nicht zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="83bdd-171">If a non-NULL value exists for the requested column or column value then the associated data is not returned.</span></span> <span data-ttu-id="83bdd-172">Stattdessen wird der zugehörige Status für diesen Spalten-oder Spaltenwert auf JET_wrnColumnPresent festgelegt.</span><span class="sxs-lookup"><span data-stu-id="83bdd-172">Instead, the associated status for that column or column value will be set to JET_wrnColumnPresent.</span></span> <span data-ttu-id="83bdd-173">Wenn der Spalten-oder Spaltenwert <strong>null</strong> ist, werden JET_wrnColumnNull wie gewohnt zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="83bdd-173">If the column or column value is <strong>NULL</strong> then JET_wrnColumnNull will be returned as usual.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83bdd-174">JET_bitEnumerateTaggedOnly</span><span class="sxs-lookup"><span data-stu-id="83bdd-174">JET_bitEnumerateTaggedOnly</span></span></p></td>
<td><p><span data-ttu-id="83bdd-175">Wenn Sie alle Spaltenwerte im Datensatz auflisten (z. b. Wenn <em>cenumcolumnid</em> NULL ist), werden nur markierte Spaltenwerte zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="83bdd-175">When enumerating all column values in the record (for example,that is when <em>cEnumColumnId</em> is zero), only tagged column values will be returned.</span></span> <span data-ttu-id="83bdd-176">Diese Option ist beim Auflisten eines bestimmten Arrays von Spalten-IDs nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="83bdd-176">This option is not allowed when enumerating a specific array of column IDs.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83bdd-177">JET_bitEnumerateInRecordOnly</span><span class="sxs-lookup"><span data-stu-id="83bdd-177">JET_bitEnumerateInRecordOnly</span></span></p></td>
<td><p><span data-ttu-id="83bdd-178"><strong>Windows 7:  </strong> JET_bitEnumerateInRecordOnly wurde in Windows 7 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="83bdd-178"><strong>Windows 7:  </strong>JET_bitEnumerateInRecordOnly is introduced in Windows 7.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="83bdd-179">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="83bdd-179">Return Value</span></span>

<span data-ttu-id="83bdd-180">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="83bdd-180">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="83bdd-181">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="83bdd-181">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="83bdd-182">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="83bdd-182">Return code</span></span></p></th>
<th><p><span data-ttu-id="83bdd-183">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="83bdd-183">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="83bdd-184">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="83bdd-184">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="83bdd-185">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="83bdd-185">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83bdd-186">JET_errBadColumnId</span><span class="sxs-lookup"><span data-stu-id="83bdd-186">JET_errBadColumnId</span></span></p></td>
<td><p><span data-ttu-id="83bdd-187">Die angegebene Spalten-ID liegt außerhalb der zulässigen Beschränkungen einer Spalten-ID.</span><span class="sxs-lookup"><span data-stu-id="83bdd-187">The column ID given is outside the legal limits of a column ID.</span></span> <span data-ttu-id="83bdd-188">Dieser Fehler wird von <strong>jetenreeratecolumschlag</strong> zurückgegeben, wenn bestimmte Spalten-IDs angefordert wurden, eine dieser Spalten-IDs ungültig war und die erste ungültige Spalten-ID mit diesem Fehler für den zugehörigen Spalten Statuscode fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="83bdd-188">This error will be returned by <strong>JetEnumerateColumns</strong> if specific column ids were requested, one of those column ids was invalid, and the first invalid column ID failed with this error for its column status code.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83bdd-189">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="83bdd-189">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="83bdd-190">Der Vorgang kann nicht ausgeführt werden, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufens von <a href="gg269240(v=exchg.10).md">jetstopservice</a>beendet wurden.</span><span class="sxs-lookup"><span data-stu-id="83bdd-190">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83bdd-191">JET_errColumnNotFound</span><span class="sxs-lookup"><span data-stu-id="83bdd-191">JET_errColumnNotFound</span></span></p></td>
<td><p><span data-ttu-id="83bdd-192">Die von der angegebenen Spalten-ID beschriebene Spalte ist in der Tabelle nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="83bdd-192">The column described by the given column ID does not exist in the table.</span></span> <span data-ttu-id="83bdd-193">Dieser Fehler wird von <strong>jetenreeratecolumschlag</strong> zurückgegeben, wenn bestimmte Spalten-IDs angefordert wurden, eine dieser Spalten-IDs ungültig war und die erste ungültige Spalten-ID mit diesem Fehler für den zugehörigen Spalten Statuscode fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="83bdd-193">This error will be returned by <strong>JetEnumerateColumns</strong> if specific column IDs were requested, one of those column IDs was invalid, and the first invalid column ID failed with this error for its column status code.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83bdd-194">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="83bdd-194">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="83bdd-195">Der Vorgang kann nicht ausgeführt werden, da bei der der Sitzung zugeordneten Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität der Daten zu schützen.</span><span class="sxs-lookup"><span data-stu-id="83bdd-195">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="83bdd-196"><strong>Windows XP:  </strong> Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="83bdd-196"><strong>Windows XP:  </strong>This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83bdd-197">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="83bdd-197">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="83bdd-198">Eine der angeforderten Optionen war ungültig oder nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="83bdd-198">One of the options requested was invalid or not implemented.</span></span> <span data-ttu-id="83bdd-199">Dieser Fehler wird von <strong>jetenreeratecolumschlag</strong> zurückgegeben, wenn Folgendes gilt:</span><span class="sxs-lookup"><span data-stu-id="83bdd-199">This error will be returned by <strong>JetEnumerateColumns</strong> when:</span></span></p>
<ul>
<li><p><span data-ttu-id="83bdd-200">JET_bitEnumerateLocal wird angegeben.</span><span class="sxs-lookup"><span data-stu-id="83bdd-200">JET_bitEnumerateLocal is specified.</span></span></p></li>
<li><p><span data-ttu-id="83bdd-201">Es wurde ein ungültiges <em>grbit</em> angegeben.</span><span class="sxs-lookup"><span data-stu-id="83bdd-201">An illegal <em>grbit</em> is specified.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83bdd-202">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="83bdd-202">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="83bdd-203">Einer der angegebenen Parameter enthielt einen unerwarteten Wert oder enthielt einen Wert, der nicht sinnvoll war, wenn er mit dem Wert eines anderen Parameters kombiniert wurde.</span><span class="sxs-lookup"><span data-stu-id="83bdd-203">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="83bdd-204">Dieser Fehler wird von <strong>jetenreeratecolumschlag</strong> zurückgegeben, wenn Folgendes gilt:</span><span class="sxs-lookup"><span data-stu-id="83bdd-204">This error will be returned by <strong>JetEnumerateColumns</strong> when:</span></span></p>
<ul>
<li><p><span data-ttu-id="83bdd-205"><em>pcenumcolumn</em> ist <strong>null</strong>.</span><span class="sxs-lookup"><span data-stu-id="83bdd-205"><em>pcEnumColumn</em> is <strong>NULL</strong>.</span></span></p></li>
<li><p><span data-ttu-id="83bdd-206"><em>prgenencolumn</em> ist <strong>null</strong>.</span><span class="sxs-lookup"><span data-stu-id="83bdd-206"><em>prgEnumColumn</em> is <strong>NULL</strong>.</span></span></p></li>
<li><p><span data-ttu-id="83bdd-207"><em>pfnrezuweisung</em> ist <strong>null</strong>.</span><span class="sxs-lookup"><span data-stu-id="83bdd-207"><em>pfnRealloc</em> is <strong>NULL</strong>.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83bdd-208">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="83bdd-208">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="83bdd-209">Der Cursor ist nicht in einem Datensatz positioniert.</span><span class="sxs-lookup"><span data-stu-id="83bdd-209">The cursor is not positioned on a record.</span></span> <span data-ttu-id="83bdd-210">Dafür sind viele verschiedene Gründe möglich.</span><span class="sxs-lookup"><span data-stu-id="83bdd-210">This can happen for many different reasons.</span></span> <span data-ttu-id="83bdd-211">Dies ist beispielsweise der Fall, wenn der Cursor aktuell nach dem letzten Datensatz im aktuellen Index positioniert ist.</span><span class="sxs-lookup"><span data-stu-id="83bdd-211">For example, this will happen if the cursor is currently positioned after the last record on the current index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83bdd-212">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="83bdd-212">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="83bdd-213">Der Vorgang kann nicht abgeschlossen werden, da die Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="83bdd-213">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83bdd-214">JET_errRecordDeleted</span><span class="sxs-lookup"><span data-stu-id="83bdd-214">JET_errRecordDeleted</span></span></p></td>
<td><p><span data-ttu-id="83bdd-215">Der Cursor wird auf einem Datensatz positioniert, der gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="83bdd-215">The cursor is positioned on a record that has been deleted.</span></span> <span data-ttu-id="83bdd-216">Dafür sind viele verschiedene Gründe möglich.</span><span class="sxs-lookup"><span data-stu-id="83bdd-216">This can happen for many different reasons.</span></span> <span data-ttu-id="83bdd-217">Der häufigste Grund ist, dass sich die Sitzung nicht in einer Transaktion befindet, der Cursor auf einem Datensatz positioniert wurde, dass der Datensatz gelöscht wurde und der Cursor dann versucht hat, auf diesen Datensatz zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="83bdd-217">The most common reason is that the session is not in a transaction, the cursor was positioned on a record, that record was deleted, and then the cursor attempted to reference that record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83bdd-218">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="83bdd-218">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="83bdd-219">Der Vorgang kann nicht abgeschlossen werden, da für die-Instanz, die der Sitzung zugeordnet ist, ein Wiederherstellungs Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="83bdd-219">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83bdd-220">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="83bdd-220">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="83bdd-221">Dieselbe Sitzung kann nicht für mehr als einen Thread gleichzeitig verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="83bdd-221">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="83bdd-222"><strong>Windows XP:  </strong> Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="83bdd-222"><strong>Windows XP:  </strong>This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83bdd-223">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="83bdd-223">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="83bdd-224">Der Vorgang kann nicht ausgeführt werden, da die Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="83bdd-224">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="83bdd-225">Bei Erfolg werden die angeforderten Daten in den Ausgabe Puffern zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="83bdd-225">On success, the requested data will be returned in the output buffers.</span></span> <span data-ttu-id="83bdd-226">Es ist Aufgabe des Aufrufers, den von diesem Rückruf zugeordneten Arbeitsspeicher freizugeben und in den Ausgabe Puffern zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="83bdd-226">It is the caller's responsibility to free any memory allocated by this callback and returned in the output buffers.</span></span> <span data-ttu-id="83bdd-227">Dieser Speicher sollte durch den bereitgestellten [rezuordnungskompatiblen](/cpp/c-runtime-library/reference/realloc?view=vs-2019) Rückruf freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="83bdd-227">That memory should be freed through the provided [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) compatible callback.</span></span> <span data-ttu-id="83bdd-228">Es erfolgt keine Änderung des Daten Bank Status.</span><span class="sxs-lookup"><span data-stu-id="83bdd-228">No change to the database state will occur.</span></span>

<span data-ttu-id="83bdd-229">Bei einem Fehler wird keine der angeforderten Daten zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="83bdd-229">On failure, none of the requested data will be returned.</span></span> <span data-ttu-id="83bdd-230">Arbeitsspeicher, der während des Aufrufs zugewiesen wurde, wird automatisch mit dem bereitgestellten [rezubelegungskompatiblen](/cpp/c-runtime-library/reference/realloc?view=vs-2019) Rückruf freigegeben.</span><span class="sxs-lookup"><span data-stu-id="83bdd-230">Any memory that was allocated during the call will be freed automatically using the provided [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) compatible callback.</span></span> <span data-ttu-id="83bdd-231">Es erfolgt keine Änderung des Daten Bank Status.</span><span class="sxs-lookup"><span data-stu-id="83bdd-231">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="83bdd-232">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="83bdd-232">Remarks</span></span>

<span data-ttu-id="83bdd-233">Wenn Sie alle Spaltenwerte im Datensatz auflisten und JET_bitEnumerateIgnoreDefaults nicht angegeben haben, können Sie nicht davon ausgehen, dass Ihnen nie ein Spalten-oder Spaltenwert mit dem Statuscode JET_wrnColumnNull angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="83bdd-233">If you are enumerating all column values in the record and you did not specify JET_bitEnumerateIgnoreDefaults then you cannot assume that you will never see a column or column value with a status code of JET_wrnColumnNull.</span></span> <span data-ttu-id="83bdd-234">Dieser Statuscode kann angezeigt werden, wenn eine Spalte einen Standardwert hat und explizit auf **null** festgelegt wurde oder wenn die Spalte eine nicht-sparsespalte ist (z. b. eine Spalte mit fester oder variabler Größe).</span><span class="sxs-lookup"><span data-stu-id="83bdd-234">You can see this status code if a column has a default value and was explicitly set to **NULL** or if the column is a non-sparse column (for example, a fixed or variable column).</span></span>

<span data-ttu-id="83bdd-235">Der *cbdatamost* -Parameter gilt nicht für alle Spaltenwerte.</span><span class="sxs-lookup"><span data-stu-id="83bdd-235">The *cbDataMost* parameter does not apply to all column values.</span></span> <span data-ttu-id="83bdd-236">Mit diesem Parameter werden nur lange Text-und lange binäre Spaltenwerte gekürzt, die so groß sind, dass Sie separat vom Datensatz gespeichert wurden.</span><span class="sxs-lookup"><span data-stu-id="83bdd-236">This parameter will only truncate long text and long binary column values that are so large that they have been stored separately from the record.</span></span>

<span data-ttu-id="83bdd-237">Wenn **jetentoeratecolumschlag** Daten in den Ausgabeparametern zurückgibt, ist der Aufrufer für die Freigabe des Arbeitsspeichers im Array sowie für jeden Speicher verantwortlich, auf den in diesem Array eingebettete Zeiger verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="83bdd-237">If **JetEnumerateColumns** returns data in its output parameters then the caller is responsible for freeing the memory in the array as well as any memory referred to by pointers embedded in that array.</span></span>

#### <a name="requirements"></a><span data-ttu-id="83bdd-238">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="83bdd-238">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="83bdd-239"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="83bdd-239"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="83bdd-240">Erfordert Windows Vista oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="83bdd-240">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83bdd-241"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="83bdd-241"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="83bdd-242">Erfordert Windows Server 2008 oder Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="83bdd-242">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83bdd-243"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="83bdd-243"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="83bdd-244">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="83bdd-244">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83bdd-245"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="83bdd-245"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="83bdd-246">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="83bdd-246">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83bdd-247"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="83bdd-247"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="83bdd-248">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="83bdd-248">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="83bdd-249">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="83bdd-249">See Also</span></span>

[<span data-ttu-id="83bdd-250">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="83bdd-250">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="83bdd-251">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="83bdd-251">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="83bdd-252">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="83bdd-252">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="83bdd-253">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="83bdd-253">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="83bdd-254">JET_ENUMCOLUMNID</span><span class="sxs-lookup"><span data-stu-id="83bdd-254">JET_ENUMCOLUMNID</span></span>](./jet-enumcolumnid-structure.md)  
[<span data-ttu-id="83bdd-255">JET_ENUMCOLUMN</span><span class="sxs-lookup"><span data-stu-id="83bdd-255">JET_ENUMCOLUMN</span></span>](./jet-enumcolumn-structure.md)  
[<span data-ttu-id="83bdd-256">JET_ENUMCOLUMNVALUE</span><span class="sxs-lookup"><span data-stu-id="83bdd-256">JET_ENUMCOLUMNVALUE</span></span>](./jet-enumcolumnvalue-structure.md)  
[<span data-ttu-id="83bdd-257">JET_PFNREALLOC</span><span class="sxs-lookup"><span data-stu-id="83bdd-257">JET_PFNREALLOC</span></span>](./jet-pfnrealloc-callback-function.md)  
[<span data-ttu-id="83bdd-258">realloc</span><span class="sxs-lookup"><span data-stu-id="83bdd-258">realloc</span></span>](/cpp/c-runtime-library/reference/realloc?view=vs-2019)  
[<span data-ttu-id="83bdd-259">Jetretrievecolumschlag</span><span class="sxs-lookup"><span data-stu-id="83bdd-259">JetRetrieveColumn</span></span>](./jetretrievecolumn-function.md)  
[<span data-ttu-id="83bdd-260">Jetretrievecolumschlag</span><span class="sxs-lookup"><span data-stu-id="83bdd-260">JetRetrieveColumns</span></span>](./jetretrievecolumns-function.md)
