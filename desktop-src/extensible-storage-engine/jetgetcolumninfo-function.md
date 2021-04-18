---
description: 'Weitere Informationen: jetgetcolumninfo-Funktion'
title: JetGetColumnInfo-Funktion
TOCTitle: JetGetColumnInfo Function
ms:assetid: 2db024e9-2784-4fb2-84b2-fef7ae518938
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269215(v=EXCHG.10)
ms:contentKeyID: 32765518
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetColumnInfoA
- JetGetColumnInfoW
- JetGetColumnInfo
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d96d5860f4b10f9294ab210e4e41d78cede202f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351804"
---
# <a name="jetgetcolumninfo-function"></a><span data-ttu-id="0ba77-103">JetGetColumnInfo-Funktion</span><span class="sxs-lookup"><span data-stu-id="0ba77-103">JetGetColumnInfo Function</span></span>


<span data-ttu-id="0ba77-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="0ba77-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetcolumninfo-function"></a><span data-ttu-id="0ba77-105">JetGetColumnInfo-Funktion</span><span class="sxs-lookup"><span data-stu-id="0ba77-105">JetGetColumnInfo Function</span></span>

<span data-ttu-id="0ba77-106">Die **jetgetcolumninfo** -Funktion Ruft Informationen zu einer Spalte ab.</span><span class="sxs-lookup"><span data-stu-id="0ba77-106">The **JetGetColumnInfo** function retrieves information about a column.</span></span>

```cpp
    JET_ERR JET_API JetGetColumnInfo(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          const tchar* szTableName,
      __in          const tchar* szColumnName,
      __out         void* pvResult,
      __in          unsigned long cbMax,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a><span data-ttu-id="0ba77-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="0ba77-107">Parameters</span></span>

<span data-ttu-id="0ba77-108">*-sid*</span><span class="sxs-lookup"><span data-stu-id="0ba77-108">*sesid*</span></span>

<span data-ttu-id="0ba77-109">Der für den API-Befehl zu verwendende Daten Bank Sitzungs Kontext.</span><span class="sxs-lookup"><span data-stu-id="0ba77-109">The database session context to use for the API call.</span></span>

<span data-ttu-id="0ba77-110">*DBID*</span><span class="sxs-lookup"><span data-stu-id="0ba77-110">*dbid*</span></span>

<span data-ttu-id="0ba77-111">Identifiziert zusammen mit *sztablename* die Tabelle, die die Spalte enthält, aus der die Informationen abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="0ba77-111">Identifies, along with *szTableName*, the table that contains the column from which the information is retrieved.</span></span>

<span data-ttu-id="0ba77-112">*sztablename*</span><span class="sxs-lookup"><span data-stu-id="0ba77-112">*szTableName*</span></span>

<span data-ttu-id="0ba77-113">Identifiziert zusammen mit *DBID* die Tabelle, die die Spalte enthält, aus der die Informationen abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="0ba77-113">Identifies, along with *dbid*, the table that contains the column from which the information is retrieved.</span></span>

<span data-ttu-id="0ba77-114">*szcolumnname*</span><span class="sxs-lookup"><span data-stu-id="0ba77-114">*szColumnName*</span></span>

<span data-ttu-id="0ba77-115">Der Name der Spalte, für die Informationen abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="0ba77-115">The name of the column that information is fetched for.</span></span>

<span data-ttu-id="0ba77-116">*pvresult*</span><span class="sxs-lookup"><span data-stu-id="0ba77-116">*pvResult*</span></span>

<span data-ttu-id="0ba77-117">Zeiger auf einen Puffer, der die Informationen empfängt.</span><span class="sxs-lookup"><span data-stu-id="0ba77-117">Pointer to a buffer that will receive the information.</span></span> <span data-ttu-id="0ba77-118">Der Typ des Puffers ist von *infolevel* abhängig.</span><span class="sxs-lookup"><span data-stu-id="0ba77-118">The type of the buffer is dependent on *InfoLevel*.</span></span> <span data-ttu-id="0ba77-119">Der Aufrufer muss so konfiguriert werden, dass der Puffer entsprechend ausgerichtet wird.</span><span class="sxs-lookup"><span data-stu-id="0ba77-119">The caller must be configured to align the buffer appropriately.</span></span>

<span data-ttu-id="0ba77-120">*cbmax*</span><span class="sxs-lookup"><span data-stu-id="0ba77-120">*cbMax*</span></span>

<span data-ttu-id="0ba77-121">Die Größe (in Bytes) des Puffers, der in *pvresult* übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="0ba77-121">The size, in bytes, of the buffer that is passed in *pvResult*.</span></span>

<span data-ttu-id="0ba77-122">*Infolevel*</span><span class="sxs-lookup"><span data-stu-id="0ba77-122">*InfoLevel*</span></span>

<span data-ttu-id="0ba77-123">Der Typ der Informationen, die für die durch *szcolumnname* angegebene Spalte abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="0ba77-123">The type of information to retrieve for the column that is specified by *szColumnName*.</span></span> <span data-ttu-id="0ba77-124">Das Format der in *pvresult* gespeicherten Daten hängt von diesem Parameter ab.</span><span class="sxs-lookup"><span data-stu-id="0ba77-124">The format of the data stored in *pvResult* is dependent on this parameter.</span></span> <span data-ttu-id="0ba77-125">Das Schema der temporären Tabelle finden Sie unter [JET_COLUMNLIST](./jet-columnlist-structure.md).</span><span class="sxs-lookup"><span data-stu-id="0ba77-125">For the schema of the temporary table, see [JET_COLUMNLIST](./jet-columnlist-structure.md).</span></span>

<span data-ttu-id="0ba77-126">Diese *infolevels* unterscheiden sich durch:</span><span class="sxs-lookup"><span data-stu-id="0ba77-126">These *InfoLevels* are differentiated by:</span></span>

  - <span data-ttu-id="0ba77-127">JET_ColInfoListSortColumnid sortiert die temporäre Tabelle nach *ColumnID*.</span><span class="sxs-lookup"><span data-stu-id="0ba77-127">JET_ColInfoListSortColumnid will sort the temporary table by *columnid*.</span></span>

  - <span data-ttu-id="0ba77-128">Mit JET_ColInfoListCompact wird die Ausgabe komprimiert.</span><span class="sxs-lookup"><span data-stu-id="0ba77-128">JET_ColInfoListCompact will compact the output.</span></span> <span data-ttu-id="0ba77-129">Weitere Informationen zur Compact-Ausgabe finden Sie unter [JET_COLUMNLIST](./jet-columnlist-structure.md).</span><span class="sxs-lookup"><span data-stu-id="0ba77-129">For more information about the compact output, see [JET_COLUMNLIST](./jet-columnlist-structure.md).</span></span>

<span data-ttu-id="0ba77-130">Die folgenden Optionen sind für die Verwendung mit diesem Parameter verfügbar.</span><span class="sxs-lookup"><span data-stu-id="0ba77-130">The following options are available for use with this parameter.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0ba77-131">Wert</span><span class="sxs-lookup"><span data-stu-id="0ba77-131">Value</span></span></p></th>
<th><p><span data-ttu-id="0ba77-132">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="0ba77-132">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0ba77-133">JET_ColInfo</span><span class="sxs-lookup"><span data-stu-id="0ba77-133">JET_ColInfo</span></span></p></td>
<td><p><span data-ttu-id="0ba77-134">JET_ColInfo und JET_ColInfoByColid beide die gleichen Informationen abrufen.</span><span class="sxs-lookup"><span data-stu-id="0ba77-134">JET_ColInfo and JET_ColInfoByColid both retrieve the same information.</span></span> <span data-ttu-id="0ba77-135"><em>pvresult</em> wird als <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a>interpretiert, und die Felder der <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> Struktur werden entsprechend ausgefüllt.</span><span class="sxs-lookup"><span data-stu-id="0ba77-135"><em>pvResult</em> is interpreted as a <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a>, and the fields of the <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> structure are filled in appropriately.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ba77-136">JET_ColInfoBase</span><span class="sxs-lookup"><span data-stu-id="0ba77-136">JET_ColInfoBase</span></span></p></td>
<td><p><span data-ttu-id="0ba77-137"><em>pvresult</em> wird als <a href="gg269194(v=exchg.10).md">JET_COLUMNBASE</a> Struktur interpretiert.</span><span class="sxs-lookup"><span data-stu-id="0ba77-137"><em>pvResult</em> is interpreted as a <a href="gg269194(v=exchg.10).md">JET_COLUMNBASE</a> structure.</span></span> <span data-ttu-id="0ba77-138">Dies ähnelt einer <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> -Struktur.</span><span class="sxs-lookup"><span data-stu-id="0ba77-138">This is similar to a <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> structure.</span></span> <span data-ttu-id="0ba77-139">Wenn diese Funktion erfolgreich ausgeführt wird, wird die Struktur mit entsprechenden Werten aufgefüllt.</span><span class="sxs-lookup"><span data-stu-id="0ba77-139">If this function succeeds, the structure is populated with appropriate values.</span></span> <span data-ttu-id="0ba77-140">Wenn diese Funktion fehlschlägt, enthält die Struktur nicht definierte Daten.</span><span class="sxs-lookup"><span data-stu-id="0ba77-140">If this function fails, the structure contains undefined data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ba77-141">JET_ColInfoByColid</span><span class="sxs-lookup"><span data-stu-id="0ba77-141">JET_ColInfoByColid</span></span></p></td>
<td><p><span data-ttu-id="0ba77-142">Wie JET_ColInfo wird <em>pvresult</em> als <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a>interpretiert, mit dem Unterschied, dass die angeforderte Spalte (<em>szcolumname</em>) nicht der Zeichen <em>folgen</em> Spaltenname, sondern ein Zeiger auf eine <a href="gg294104(v=exchg.10).md">JET_COLUMNID</a>ist.</span><span class="sxs-lookup"><span data-stu-id="0ba77-142">Like JET_ColInfo, <em>pvResult</em> is interpreted as a <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a>, except this <em>InfoLevel</em> indicates that the requested column (<em>szColumName</em>) is not the string column name, but a pointer to a <a href="gg294104(v=exchg.10).md">JET_COLUMNID</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ba77-143">JET_ColInfoList</span><span class="sxs-lookup"><span data-stu-id="0ba77-143">JET_ColInfoList</span></span></p></td>
<td><p><span data-ttu-id="0ba77-144"><em>pvresult</em> wird als <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a> Struktur interpretiert.</span><span class="sxs-lookup"><span data-stu-id="0ba77-144"><em>pvResult</em> is interpreted as a <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a> structure.</span></span> <span data-ttu-id="0ba77-145">Wenn diese Funktion erfolgreich ausgeführt wird, wird die Struktur mit entsprechenden Werten aufgefüllt.</span><span class="sxs-lookup"><span data-stu-id="0ba77-145">If this function succeeds, the structure is populated with appropriate values.</span></span> <span data-ttu-id="0ba77-146">Eine temporäre Tabelle wird geöffnet und wird vom <strong>TableID</strong> -Member der <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a> Struktur identifiziert.</span><span class="sxs-lookup"><span data-stu-id="0ba77-146">A temporary table is opened and is identified by the <strong>tableid</strong> member of the <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a> structure.</span></span> <span data-ttu-id="0ba77-147">Die Tabelle muss mit <a href="gg294087(v=exchg.10).md">jetclosetable</a>geschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="0ba77-147">The table must be closed with <a href="gg294087(v=exchg.10).md">JetCloseTable</a>.</span></span> <span data-ttu-id="0ba77-148">Wenn diese Funktion fehlschlägt, enthält die Struktur nicht definierte Daten.</span><span class="sxs-lookup"><span data-stu-id="0ba77-148">If this function fails, the structure contains undefined data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ba77-149">JET_ColInfoListCompact</span><span class="sxs-lookup"><span data-stu-id="0ba77-149">JET_ColInfoListCompact</span></span></p></td>
<td><p><span data-ttu-id="0ba77-150">Identisch mit JET_ColInfoList.</span><span class="sxs-lookup"><span data-stu-id="0ba77-150">Same as JET_ColInfoList.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ba77-151">JET_ColInfoListSortColumnid</span><span class="sxs-lookup"><span data-stu-id="0ba77-151">JET_ColInfoListSortColumnid</span></span></p></td>
<td><p><span data-ttu-id="0ba77-152">Identisch mit JET_ColInfoList; die resultierende Tabelle wird jedoch nach ColumnID sortiert, anstelle des Spaltennamens.</span><span class="sxs-lookup"><span data-stu-id="0ba77-152">Same as JET_ColInfoList; however the resulting table is sorted by columnid, instead of column name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ba77-153">JET_ColInfoSysTabCursor</span><span class="sxs-lookup"><span data-stu-id="0ba77-153">JET_ColInfoSysTabCursor</span></span></p></td>
<td><p><span data-ttu-id="0ba77-154">JET_ColInfoSysTabCursor ist veraltet, und die Verwendung von wird JET_errFeatureNotAvailable zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="0ba77-154">JET_ColInfoSysTabCursor is deprecated, and use of it will return JET_errFeatureNotAvailable.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ba77-155">JET_ColInfoBaseByColId</span><span class="sxs-lookup"><span data-stu-id="0ba77-155">JET_ColInfoBaseByColId</span></span></p></td>
<td><p><span data-ttu-id="0ba77-156">Wie JET_ColInfoBase wird <em>pvresult</em> als <a href="gg269194(v=exchg.10).md">JET_COLUMNBASE</a>interpretiert, mit dem Unterschied, dass die angeforderte Spalte (<em>szcolumname</em>) nicht der Name der Zeichen <em>folgen</em> Spalte, sondern ein Zeiger auf eine <a href="gg294104(v=exchg.10).md">JET_COLUMNID</a>ist.</span><span class="sxs-lookup"><span data-stu-id="0ba77-156">Like JET_ColInfoBase, <em>pvResult</em> is interpreted as a <a href="gg269194(v=exchg.10).md">JET_COLUMNBASE</a>, except this <em>InfoLevel</em> indicates that requested column (<em>szColumName</em>) is not the string column name, but a pointer to a <a href="gg294104(v=exchg.10).md">JET_COLUMNID</a>.</span></span></p>
<p><span data-ttu-id="0ba77-157"><strong>Windows Vista:  </strong> Dieser Wert wird in Windows Vista eingeführt.</span><span class="sxs-lookup"><span data-stu-id="0ba77-157"><strong>Windows Vista:  </strong>This value is introduced in Windows Vista.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ba77-158">JET_ColInfoGrbitNonDerivedColumnsOnly</span><span class="sxs-lookup"><span data-stu-id="0ba77-158">JET_ColInfoGrbitNonDerivedColumnsOnly</span></span></p></td>
<td><p><span data-ttu-id="0ba77-159">Gibt nur nicht abgeleitete Spalten zurück (wenn die Tabelle von einer Vorlage abgeleitet ist).</span><span class="sxs-lookup"><span data-stu-id="0ba77-159">Only return non-derived columns (if the table is derived from a template).</span></span></p>
<p><span data-ttu-id="0ba77-160">Dieser Wert kann logisch oder in <em>infolevel</em>sein, wenn die Basis- <em>infolevel</em> JET_ColInfoList ist.</span><span class="sxs-lookup"><span data-stu-id="0ba77-160">This value can be logically or'd into the <em>InfoLevel</em>, when the base <em>InfoLevel</em> is JET_ColInfoList.</span></span></p>
<p><span data-ttu-id="0ba77-161"><strong>Windows Vista:  </strong> Dieser Wert wird in Windows Vista eingeführt.</span><span class="sxs-lookup"><span data-stu-id="0ba77-161"><strong>Windows Vista:  </strong>This value is introduced Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ba77-162">JET_ColInfoGrbitMinimalInfo</span><span class="sxs-lookup"><span data-stu-id="0ba77-162">JET_ColInfoGrbitMinimalInfo</span></span></p></td>
<td><p><span data-ttu-id="0ba77-163">Gibt nur den Spaltennamen und den Spaltennamen für jede Spalte zurück.</span><span class="sxs-lookup"><span data-stu-id="0ba77-163">Only return the column name and columnid of each column.</span></span></p>
<p><span data-ttu-id="0ba77-164">Dieser Wert kann logisch oder in <em>infolevel</em>sein, wenn die Basis- <em>infolevel</em> JET_ColInfoList ist.</span><span class="sxs-lookup"><span data-stu-id="0ba77-164">This value can be logically or'd into the <em>InfoLevel</em>, when the base <em>InfoLevel</em> is JET_ColInfoList.</span></span></p>
<p><span data-ttu-id="0ba77-165"><strong>Windows Vista:  </strong> Dieser Wert wird in Windows Vista eingeführt.</span><span class="sxs-lookup"><span data-stu-id="0ba77-165"><strong>Windows Vista:  </strong>This value is introduced in Windows Vista.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ba77-166">JET_ColInfoGrbitSortByColumnid</span><span class="sxs-lookup"><span data-stu-id="0ba77-166">JET_ColInfoGrbitSortByColumnid</span></span></p></td>
<td><p><span data-ttu-id="0ba77-167">Dient zum Sortieren der zurückgegebenen Spaltenliste nach ColumnID (Standardmäßig wird die Liste nach Spaltennamen sortiert).</span><span class="sxs-lookup"><span data-stu-id="0ba77-167">Sort returned column list by columnid (default is to sort list by column name).</span></span></p>
<p><span data-ttu-id="0ba77-168">Dieser Wert kann logisch oder in <em>infolevel</em>sein, wenn die Basis- <em>infolevel</em> JET_ColInfoList ist.</span><span class="sxs-lookup"><span data-stu-id="0ba77-168">This value can be logically or'd into the <em>InfoLevel</em>, when the base <em>InfoLevel</em> is JET_ColInfoList.</span></span></p>
<p><span data-ttu-id="0ba77-169"><strong>Windows Vista:  </strong> Dieser Wert wird in Windows Vista eingeführt.</span><span class="sxs-lookup"><span data-stu-id="0ba77-169"><strong>Windows Vista:  </strong>This value is introduced in Windows Vista.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="0ba77-170">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0ba77-170">Return Value</span></span>

<span data-ttu-id="0ba77-171">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="0ba77-171">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="0ba77-172">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="0ba77-172">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0ba77-173">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="0ba77-173">Return code</span></span></p></th>
<th><p><span data-ttu-id="0ba77-174">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0ba77-174">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0ba77-175">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="0ba77-175">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="0ba77-176">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="0ba77-176">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ba77-177">JET_errColumnNotFound</span><span class="sxs-lookup"><span data-stu-id="0ba77-177">JET_errColumnNotFound</span></span></p></td>
<td><p><span data-ttu-id="0ba77-178">Die Spalte mit dem Namen <em>szcolumnname</em> wurde in der Tabelle nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="0ba77-178">The column named <em>szColumnName</em> was not found in the table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ba77-179">JET_errFeatureNotAvailable</span><span class="sxs-lookup"><span data-stu-id="0ba77-179">JET_errFeatureNotAvailable</span></span></p></td>
<td><p><span data-ttu-id="0ba77-180">Es wurde eine ungültige <em>infolevel</em> angegeben.</span><span class="sxs-lookup"><span data-stu-id="0ba77-180">A bad <em>InfoLevel</em> was specified.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ba77-181">JET_errInvalidName</span><span class="sxs-lookup"><span data-stu-id="0ba77-181">JET_errInvalidName</span></span></p></td>
<td><p><span data-ttu-id="0ba77-182">Dieser Fehler kann zurückgegeben werden, wenn Folgendes gilt:</span><span class="sxs-lookup"><span data-stu-id="0ba77-182">This error can be returned if:</span></span></p>
<ul>
<li><p><span data-ttu-id="0ba77-183">Es wurde ein ungültiger Name für <em>sztablename</em> angegeben.</span><span class="sxs-lookup"><span data-stu-id="0ba77-183">A bad name for <em>szTableName</em> was given.</span></span></p></li>
<li><p><span data-ttu-id="0ba77-184">Ein ungültiger Name für <em>szcolumnname</em> wurde angegeben.</span><span class="sxs-lookup"><span data-stu-id="0ba77-184">A bad name for <em>szColumnName</em> was given.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ba77-185">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="0ba77-185">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="0ba77-186">Dieser Fehler kann zurückgegeben werden, wenn Folgendes gilt:</span><span class="sxs-lookup"><span data-stu-id="0ba77-186">This error can be returned if:</span></span></p>
<ul>
<li><p><span data-ttu-id="0ba77-187">Es wurde eine ungültige <em>infolevel</em> angegeben.</span><span class="sxs-lookup"><span data-stu-id="0ba77-187">A bad <em>InfoLevel</em> was specified.</span></span></p></li>
<li><p><span data-ttu-id="0ba77-188">Ein NULL- <em>sztablename</em> -Wert wurde übermittelt.</span><span class="sxs-lookup"><span data-stu-id="0ba77-188">A NULL <em>szTableName</em> was passed in.</span></span></p></li>
<li><p><span data-ttu-id="0ba77-189">Der Puffer ist zu klein.</span><span class="sxs-lookup"><span data-stu-id="0ba77-189">The buffer is too small.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="0ba77-190">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0ba77-190">Remarks</span></span>

<span data-ttu-id="0ba77-191">[Jetgettablecolumninfo](./jetgettablecolumninfo-function.md) und **jetgetcolumninfo** rufen Informationen zu einer Spalte ab.</span><span class="sxs-lookup"><span data-stu-id="0ba77-191">[JetGetTableColumnInfo](./jetgettablecolumninfo-function.md) and **JetGetColumnInfo** both retrieve information about a column.</span></span> <span data-ttu-id="0ba77-192">Der Unterschied besteht darin, wie die Tabelle identifiziert wird:</span><span class="sxs-lookup"><span data-stu-id="0ba77-192">The difference between them is how the table is identified:</span></span>

  - <span data-ttu-id="0ba77-193">[Jetgettablecolumninfo](./jetgettablecolumninfo-function.md) identifiziert eine Tabelle nach *TableID*.</span><span class="sxs-lookup"><span data-stu-id="0ba77-193">[JetGetTableColumnInfo](./jetgettablecolumninfo-function.md) identifies a table by *tableid*.</span></span>

  - <span data-ttu-id="0ba77-194">**Jetgetcolumninfo** identifiziert eine Tabelle mit der Kombination aus *DBID* und *sztablename* .</span><span class="sxs-lookup"><span data-stu-id="0ba77-194">**JetGetColumnInfo** identifies a table by *dbid* and *szTableName* combination.</span></span>

<span data-ttu-id="0ba77-195">Beim Abrufen von Daten mit JET_ColInfoList, JET_ColInfoListSortColumnid oder JET_ColInfoListCompact wird eine temporäre Tabelle geöffnet.</span><span class="sxs-lookup"><span data-stu-id="0ba77-195">When retrieving data with JET_ColInfoList, JET_ColInfoListSortColumnid, or JET_ColInfoListCompact, a temporary table will be opened.</span></span> <span data-ttu-id="0ba77-196">Die temporäre Tabelle enthält Daten, und die [JET_COLUMNLIST](./jet-columnlist-structure.md) Struktur enthält ausreichende Informationen, um die temporäre Tabelle zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="0ba77-196">The temporary table contains data, and the [JET_COLUMNLIST](./jet-columnlist-structure.md) structure contains sufficient information to traverse the temporary table.</span></span> <span data-ttu-id="0ba77-197">Die temporäre Tabelle muss mit [jetclosetable](./jetclosetable-function.md)geschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="0ba77-197">The temporary table must be closed with [JetCloseTable](./jetclosetable-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="0ba77-198">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0ba77-198">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0ba77-199"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="0ba77-199"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="0ba77-200">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="0ba77-200">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ba77-201"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="0ba77-201"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="0ba77-202">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="0ba77-202">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ba77-203"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="0ba77-203"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="0ba77-204">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="0ba77-204">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ba77-205"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="0ba77-205"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="0ba77-206">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="0ba77-206">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ba77-207"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="0ba77-207"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="0ba77-208">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="0ba77-208">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ba77-209"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="0ba77-209"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="0ba77-210">Implementiert als <strong>jetgetcolumninfow</strong> (Unicode) und <strong>jetgetcolumninfoa</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="0ba77-210">Implemented as <strong>JetGetColumnInfoW</strong> (Unicode) and <strong>JetGetColumnInfoA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="0ba77-211">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="0ba77-211">See Also</span></span>

[<span data-ttu-id="0ba77-212">Fehler Behandlungsparameter</span><span class="sxs-lookup"><span data-stu-id="0ba77-212">Error Handling Parameters</span></span>](./error-handling-parameters.md)  
[<span data-ttu-id="0ba77-213">Erweiterbare Speicher-Engine-Fehler</span><span class="sxs-lookup"><span data-stu-id="0ba77-213">Extensible Storage Engine Errors</span></span>](./extensible-storage-engine-errors.md)  
[<span data-ttu-id="0ba77-214">JET_COLUMNBASE</span><span class="sxs-lookup"><span data-stu-id="0ba77-214">JET_COLUMNBASE</span></span>](./jet-columnbase-structure.md)  
[<span data-ttu-id="0ba77-215">JET_COLUMNDEF</span><span class="sxs-lookup"><span data-stu-id="0ba77-215">JET_COLUMNDEF</span></span>](./jet-columndef-structure.md)  
[<span data-ttu-id="0ba77-216">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="0ba77-216">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="0ba77-217">JET_COLUMNLIST</span><span class="sxs-lookup"><span data-stu-id="0ba77-217">JET_COLUMNLIST</span></span>](./jet-columnlist-structure.md)  
[<span data-ttu-id="0ba77-218">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="0ba77-218">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="0ba77-219">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="0ba77-219">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="0ba77-220">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="0ba77-220">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="0ba77-221">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="0ba77-221">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="0ba77-222">Jetclosetable</span><span class="sxs-lookup"><span data-stu-id="0ba77-222">JetCloseTable</span></span>](./jetclosetable-function.md)  
[<span data-ttu-id="0ba77-223">Jetgettablecolumninfo</span><span class="sxs-lookup"><span data-stu-id="0ba77-223">JetGetTableColumnInfo</span></span>](./jetgettablecolumninfo-function.md)
