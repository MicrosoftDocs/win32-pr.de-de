---
description: 'Weitere Informationen zu: jetgettablecolumninfo-Funktion'
title: Jetgettablecolumninfo-Funktion
TOCTitle: JetGetTableColumnInfo Function
ms:assetid: b1c1df22-ad33-4320-9f08-baf2a3e7bd7d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294061(v=EXCHG.10)
ms:contentKeyID: 32765676
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetTableColumnInfoW
- JetGetTableColumnInfoA
- JetGetTableColumnInfo
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f8c7b073ca9be90e89a1c6b99c010707e6405323
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "104219739"
---
# <a name="jetgettablecolumninfo-function"></a><span data-ttu-id="c6e55-103">Jetgettablecolumninfo-Funktion</span><span class="sxs-lookup"><span data-stu-id="c6e55-103">JetGetTableColumnInfo Function</span></span>


<span data-ttu-id="c6e55-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="c6e55-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgettablecolumninfo-function"></a><span data-ttu-id="c6e55-105">Jetgettablecolumninfo-Funktion</span><span class="sxs-lookup"><span data-stu-id="c6e55-105">JetGetTableColumnInfo Function</span></span>

<span data-ttu-id="c6e55-106">Die **jetgettablecolumninfo** -Funktion Ruft Informationen über eine Tabellenspalte ab.</span><span class="sxs-lookup"><span data-stu-id="c6e55-106">The **JetGetTableColumnInfo** function retrieves information about a table column.</span></span>

```cpp
JET_ERR JET_API JetGetTableColumnInfo(
  __in          JET_SESID sesid,
  __in          JET_TABLEID tableid,
  __in          const tchar* szColumnName,
  __out         void* pvResult,
  __in          unsigned long cbMax,
  __in          unsigned long InfoLevel
);
```

### <a name="parameters"></a><span data-ttu-id="c6e55-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="c6e55-107">Parameters</span></span>

<span data-ttu-id="c6e55-108">*-sid*</span><span class="sxs-lookup"><span data-stu-id="c6e55-108">*sesid*</span></span>

<span data-ttu-id="c6e55-109">Der für den API-Befehl zu verwendende Daten Bank Sitzungs Kontext.</span><span class="sxs-lookup"><span data-stu-id="c6e55-109">The database session context to use for the API call.</span></span>

<span data-ttu-id="c6e55-110">*TableID*</span><span class="sxs-lookup"><span data-stu-id="c6e55-110">*tableid*</span></span>

<span data-ttu-id="c6e55-111">Die Tabelle, die die Spalte enthält, für die Informationen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c6e55-111">The table that contains the column to fetch information for.</span></span>

<span data-ttu-id="c6e55-112">*szcolumnname*</span><span class="sxs-lookup"><span data-stu-id="c6e55-112">*szColumnName*</span></span>

<span data-ttu-id="c6e55-113">Der Name der Spalte, für die Informationen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c6e55-113">The name of the column to fetch information for.</span></span>

<span data-ttu-id="c6e55-114">*pvresult*</span><span class="sxs-lookup"><span data-stu-id="c6e55-114">*pvResult*</span></span>

<span data-ttu-id="c6e55-115">Zeiger auf einen Puffer, der die Informationen empfängt.</span><span class="sxs-lookup"><span data-stu-id="c6e55-115">Pointer to a buffer that will receive the information.</span></span> <span data-ttu-id="c6e55-116">Der Typ des Puffers ist von *infolevel* abhängig.</span><span class="sxs-lookup"><span data-stu-id="c6e55-116">The type of the buffer is dependent on *InfoLevel*.</span></span> <span data-ttu-id="c6e55-117">Der Aufrufer muss so konfiguriert werden, dass der Puffer entsprechend ausgerichtet wird.</span><span class="sxs-lookup"><span data-stu-id="c6e55-117">The caller must be configured to align the buffer appropriately.</span></span>

<span data-ttu-id="c6e55-118">*cbmax*</span><span class="sxs-lookup"><span data-stu-id="c6e55-118">*cbMax*</span></span>

<span data-ttu-id="c6e55-119">Die Größe (in Bytes) des Puffers, der in *pvresult* übergeben wurde.</span><span class="sxs-lookup"><span data-stu-id="c6e55-119">The size, in bytes, of the buffer that was passed in *pvResult*.</span></span>

<span data-ttu-id="c6e55-120">*Infolevel*</span><span class="sxs-lookup"><span data-stu-id="c6e55-120">*InfoLevel*</span></span>

<span data-ttu-id="c6e55-121">Der Typ der Informationen, die für die durch *szcolumnname* angegebene Spalte abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="c6e55-121">The type of information that will be retrieved for the column that is specified by *szColumnName*.</span></span> <span data-ttu-id="c6e55-122">Das Format der Daten, die in *pvresult* gespeichert sind, ist von *infolevel* abhängig.</span><span class="sxs-lookup"><span data-stu-id="c6e55-122">The format of the data that is stored in *pvResult* is dependent on *InfoLevel*.</span></span> <span data-ttu-id="c6e55-123">Das Schema der temporären Tabelle finden Sie unter [JET_COLUMNLIST](./jet-columnlist-structure.md).</span><span class="sxs-lookup"><span data-stu-id="c6e55-123">For the schema of the temporary table, see [JET_COLUMNLIST](./jet-columnlist-structure.md).</span></span>

  - <span data-ttu-id="c6e55-124">JET_ColInfoListSortColumnid sortiert die temporäre Tabelle nach *ColumnID*.</span><span class="sxs-lookup"><span data-stu-id="c6e55-124">JET_ColInfoListSortColumnid will sort the temporary table by *columnid*.</span></span>

  - <span data-ttu-id="c6e55-125">Mit JET_ColInfoListCompact wird die Ausgabe komprimiert.</span><span class="sxs-lookup"><span data-stu-id="c6e55-125">JET_ColInfoListCompact will compact the output.</span></span> <span data-ttu-id="c6e55-126">Weitere Informationen zur Compact-Ausgabe finden Sie unter [JET_COLUMNLIST](./jet-columnlist-structure.md).</span><span class="sxs-lookup"><span data-stu-id="c6e55-126">For more information about the compact output, see [JET_COLUMNLIST](./jet-columnlist-structure.md).</span></span>

<span data-ttu-id="c6e55-127">Die folgenden Optionen können für diesen Parameter festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="c6e55-127">The following options can be set for this parameter:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c6e55-128">Wert</span><span class="sxs-lookup"><span data-stu-id="c6e55-128">Value</span></span></p></th>
<th><p><span data-ttu-id="c6e55-129">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c6e55-129">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c6e55-130">JET_ColInfo</span><span class="sxs-lookup"><span data-stu-id="c6e55-130">JET_ColInfo</span></span></p></td>
<td><p><span data-ttu-id="c6e55-131"><em>pvresult</em> wird als <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a>interpretiert, und die Felder der <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> Struktur werden entsprechend ausgefüllt.</span><span class="sxs-lookup"><span data-stu-id="c6e55-131"><em>pvResult</em> is interpreted as a <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a>, and the fields of the <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> structure are filled in appropriately.</span></span> <span data-ttu-id="c6e55-132">JET_ColInfo und JET_ColInfoByColid beide die gleichen Informationen abrufen.</span><span class="sxs-lookup"><span data-stu-id="c6e55-132">JET_ColInfo and JET_ColInfoByColid both retrieve the same information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6e55-133">JET_ColInfoBase</span><span class="sxs-lookup"><span data-stu-id="c6e55-133">JET_ColInfoBase</span></span></p></td>
<td><p><span data-ttu-id="c6e55-134"><em>pvresult</em> wird als <a href="gg269194(v=exchg.10).md">JET_COLUMNBASE</a> Struktur interpretiert.</span><span class="sxs-lookup"><span data-stu-id="c6e55-134"><em>pvResult</em> is interpreted as a <a href="gg269194(v=exchg.10).md">JET_COLUMNBASE</a> structure.</span></span> <span data-ttu-id="c6e55-135">Dies ähnelt einer <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> -Struktur.</span><span class="sxs-lookup"><span data-stu-id="c6e55-135">This is similar to a <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> structure.</span></span> <span data-ttu-id="c6e55-136">Wenn diese Funktion erfolgreich ausgeführt wird, wird die Struktur mit entsprechenden Werten aufgefüllt.</span><span class="sxs-lookup"><span data-stu-id="c6e55-136">If this function succeeds, the structure is populated with appropriate values.</span></span> <span data-ttu-id="c6e55-137">Wenn diese Funktion fehlschlägt, enthält die Struktur nicht definierte Daten.</span><span class="sxs-lookup"><span data-stu-id="c6e55-137">If this function fails, the structure contains undefined data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6e55-138">JET_ColInfoByColid</span><span class="sxs-lookup"><span data-stu-id="c6e55-138">JET_ColInfoByColid</span></span></p></td>
<td><p><span data-ttu-id="c6e55-139"><em>pvresult</em> wird als <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a>interpretiert, mit dem Unterschied, dass die angeforderte Spalte (<em>szcolumname</em>) nicht der Zeichen <em>folgen</em> Spaltenname, sondern ein Zeiger auf einen <a href="gg294104(v=exchg.10).md">JET_COLUMNID</a>ist.</span><span class="sxs-lookup"><span data-stu-id="c6e55-139"><em>pvResult</em> is interpreted as a <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a>, except this <em>InfoLevel</em> indicates that the requested column (<em>szColumName</em>) is not the string column name, but a pointer to a <a href="gg294104(v=exchg.10).md">JET_COLUMNID</a>.</span></span> <span data-ttu-id="c6e55-140">JET_ColInfo und JET_ColInfoByColid beide die gleichen Informationen abrufen.</span><span class="sxs-lookup"><span data-stu-id="c6e55-140">JET_ColInfo and JET_ColInfoByColid both retrieve the same information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6e55-141">JET_ColInfoList</span><span class="sxs-lookup"><span data-stu-id="c6e55-141">JET_ColInfoList</span></span></p></td>
<td><p><span data-ttu-id="c6e55-142"><em>pvresult</em> wird als <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a> Struktur interpretiert.</span><span class="sxs-lookup"><span data-stu-id="c6e55-142"><em>pvResult</em> is interpreted as a <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a> structure.</span></span> <span data-ttu-id="c6e55-143">Wenn diese Funktion erfolgreich ausgeführt wird, wird die Struktur mit entsprechenden Werten aufgefüllt.</span><span class="sxs-lookup"><span data-stu-id="c6e55-143">If this function succeeds, the structure is populated with appropriate values.</span></span> <span data-ttu-id="c6e55-144">Eine temporäre Tabelle wird geöffnet und wird durch das <em>TableID</em> -Element von <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a>identifiziert.</span><span class="sxs-lookup"><span data-stu-id="c6e55-144">A temporary table is opened and is identified by the <em>tableid</em> member of <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a>.</span></span> <span data-ttu-id="c6e55-145">Die Tabelle muss mit <a href="gg294087(v=exchg.10).md">jetclosetable</a>geschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="c6e55-145">The table must be closed with <a href="gg294087(v=exchg.10).md">JetCloseTable</a>.</span></span> <span data-ttu-id="c6e55-146">Wenn diese Funktion fehlschlägt, enthält die Struktur nicht definierte Daten.</span><span class="sxs-lookup"><span data-stu-id="c6e55-146">If this function fails, the structure contains undefined data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6e55-147">JET_ColInfoListCompact</span><span class="sxs-lookup"><span data-stu-id="c6e55-147">JET_ColInfoListCompact</span></span></p></td>
<td><p><span data-ttu-id="c6e55-148"><em>pvresult</em> wird als <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a> Struktur interpretiert.</span><span class="sxs-lookup"><span data-stu-id="c6e55-148"><em>pvResult</em> is interpreted as a <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a> structure.</span></span> <span data-ttu-id="c6e55-149">Wenn diese Funktion erfolgreich ausgeführt wird, wird die Struktur mit entsprechenden Werten aufgefüllt.</span><span class="sxs-lookup"><span data-stu-id="c6e55-149">If this function succeeds, the structure is populated with appropriate values.</span></span> <span data-ttu-id="c6e55-150">Eine temporäre Tabelle wird geöffnet und wird durch das <em>TableID</em> -Element von <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a>identifiziert.</span><span class="sxs-lookup"><span data-stu-id="c6e55-150">A temporary table is opened and is identified by the <em>tableid</em> member of <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a>.</span></span> <span data-ttu-id="c6e55-151">Die Tabelle muss mit <a href="gg294087(v=exchg.10).md">jetclosetable</a>geschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="c6e55-151">The table must be closed with <a href="gg294087(v=exchg.10).md">JetCloseTable</a>.</span></span> <span data-ttu-id="c6e55-152">Wenn diese Funktion fehlschlägt, enthält die Struktur nicht definierte Daten.</span><span class="sxs-lookup"><span data-stu-id="c6e55-152">If this function fails, the structure contains undefined data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6e55-153">JET_ColInfoListSortColumnid</span><span class="sxs-lookup"><span data-stu-id="c6e55-153">JET_ColInfoListSortColumnid</span></span></p></td>
<td><p><span data-ttu-id="c6e55-154">Identisch mit JET_ColInfoList, die sich ergebende Tabelle wird jedoch nach <em>ColumnID</em>sortiert, anstelle des Spaltennamens.</span><span class="sxs-lookup"><span data-stu-id="c6e55-154">Same as JET_ColInfoList, however the resulting table is sorted by <em>columnid</em>, instead of column name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6e55-155">JET_ColInfoSysTabCursor</span><span class="sxs-lookup"><span data-stu-id="c6e55-155">JET_ColInfoSysTabCursor</span></span></p></td>
<td><p><span data-ttu-id="c6e55-156">JET_ColInfoSysTabCursor ist veraltet, und die Verwendung von wird JET_errFeatureNotAvailable zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c6e55-156">JET_ColInfoSysTabCursor is deprecated, and use of it will return JET_errFeatureNotAvailable.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6e55-157">JET_ColInfoBaseByColId</span><span class="sxs-lookup"><span data-stu-id="c6e55-157">JET_ColInfoBaseByColId</span></span></p></td>
<td><p><span data-ttu-id="c6e55-158">Wie JET_ColInfoBase wird <em>pvresult</em> als <a href="gg269194(v=exchg.10).md">JET_COLUMNBASE</a>interpretiert, mit dem Unterschied, dass die angeforderte Spalte (<em>szcolumname</em>) nicht der Name der Zeichen <em>folgen</em> Spalte, sondern ein Zeiger auf eine <a href="gg294104(v=exchg.10).md">JET_COLUMNID</a>ist.</span><span class="sxs-lookup"><span data-stu-id="c6e55-158">Same as JET_ColInfoBase, <em>pvResult</em> is interpreted as a <a href="gg269194(v=exchg.10).md">JET_COLUMNBASE</a>, except this <em>InfoLevel</em> indicates that requested column (<em>szColumName</em>) is not the string column name, but a pointer to a <a href="gg294104(v=exchg.10).md">JET_COLUMNID</a>.</span></span></p>
<p><span data-ttu-id="c6e55-159"><strong>Windows Vista:  </strong> Diese ist in Windows Vista und höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c6e55-159"><strong>Windows Vista:  </strong>This is available in Windows Vista and later.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6e55-160">JET_ColInfoGrbitNonDerivedColumnsOnly</span><span class="sxs-lookup"><span data-stu-id="c6e55-160">JET_ColInfoGrbitNonDerivedColumnsOnly</span></span></p></td>
<td><p><span data-ttu-id="c6e55-161">Gibt nur nicht abgeleitete Spalten zurück (wenn die Tabelle von einer Vorlage abgeleitet ist).</span><span class="sxs-lookup"><span data-stu-id="c6e55-161">Only return non-derived columns (if the table is derived from a template).</span></span></p>
<p><span data-ttu-id="c6e55-162">Dieser Wert kann logisch oder in <em>infolevel</em>sein, wenn die Basis- <em>infolevel</em> JET_ColInfoList ist.</span><span class="sxs-lookup"><span data-stu-id="c6e55-162">This value can be logically or'd into the <em>InfoLevel</em>, when the base <em>InfoLevel</em> is JET_ColInfoList.</span></span></p>
<p><span data-ttu-id="c6e55-163"><strong>Windows Vista:  </strong> Dieser Wert wird in Windows Vista eingeführt.</span><span class="sxs-lookup"><span data-stu-id="c6e55-163"><strong>Windows Vista:  </strong>This value is introduced in Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6e55-164">JET_ColInfoGrbitMinimalInfo</span><span class="sxs-lookup"><span data-stu-id="c6e55-164">JET_ColInfoGrbitMinimalInfo</span></span></p></td>
<td><p><span data-ttu-id="c6e55-165">Gibt nur den Spaltennamen und den Spaltennamen für jede Spalte zurück.</span><span class="sxs-lookup"><span data-stu-id="c6e55-165">Only return the column name and columnid of each column.</span></span></p>
<p><span data-ttu-id="c6e55-166">Dieser Wert kann logisch oder in <em>infolevel</em>sein, wenn die Basis- <em>infolevel</em> JET_ColInfoList ist.</span><span class="sxs-lookup"><span data-stu-id="c6e55-166">This value can be logically or'd into the <em>InfoLevel</em>, when the base <em>InfoLevel</em> is JET_ColInfoList.</span></span></p>
<p><span data-ttu-id="c6e55-167"><strong>Windows Vista:  </strong> Dieser Wert wird in Windows Vista eingeführt.</span><span class="sxs-lookup"><span data-stu-id="c6e55-167"><strong>Windows Vista:  </strong>This value is introduced in Windows Vista.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6e55-168">JET_ColInfoGrbitSortByColumnid</span><span class="sxs-lookup"><span data-stu-id="c6e55-168">JET_ColInfoGrbitSortByColumnid</span></span></p></td>
<td><p><span data-ttu-id="c6e55-169">Dient zum Sortieren der zurückgegebenen Spaltenliste nach ColumnID (Standardmäßig wird die Liste nach Spaltennamen sortiert).</span><span class="sxs-lookup"><span data-stu-id="c6e55-169">Sort returned column list by columnid (default is to sort list by column name).</span></span></p>
<p><span data-ttu-id="c6e55-170">Dieser Wert kann logisch oder in <em>infolevel</em>sein, wenn die Basis- <em>infolevel</em> JET_ColInfoList ist.</span><span class="sxs-lookup"><span data-stu-id="c6e55-170">This value can be logically or'd into the <em>InfoLevel</em>, when the base <em>InfoLevel</em> is JET_ColInfoList.</span></span></p>
<p><span data-ttu-id="c6e55-171"><strong>Windows Vista:  </strong> Dieser Wert wird in Windows Vista eingeführt.</span><span class="sxs-lookup"><span data-stu-id="c6e55-171"><strong>Windows Vista:  </strong>This value is introduced in Windows Vista.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="c6e55-172">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c6e55-172">Return Value</span></span>

<span data-ttu-id="c6e55-173">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="c6e55-173">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="c6e55-174">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="c6e55-174">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c6e55-175">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="c6e55-175">Return code</span></span></p></th>
<th><p><span data-ttu-id="c6e55-176">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c6e55-176">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c6e55-177">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="c6e55-177">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="c6e55-178">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="c6e55-178">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6e55-179">JET_errColumnNotFound</span><span class="sxs-lookup"><span data-stu-id="c6e55-179">JET_errColumnNotFound</span></span></p></td>
<td><p><span data-ttu-id="c6e55-180">Die Spalte mit dem Namen <em>szcolumnname</em> wurde in der Tabelle nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="c6e55-180">The column named <em>szColumnName</em> was not found in the table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6e55-181">JET_errFeatureNotAvailable</span><span class="sxs-lookup"><span data-stu-id="c6e55-181">JET_errFeatureNotAvailable</span></span></p></td>
<td><p><span data-ttu-id="c6e55-182">Es wurde eine ungültige <em>infolevel</em> angegeben.</span><span class="sxs-lookup"><span data-stu-id="c6e55-182">A bad <em>InfoLevel</em> was specified.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6e55-183">JET_errInvalidName</span><span class="sxs-lookup"><span data-stu-id="c6e55-183">JET_errInvalidName</span></span></p></td>
<td><p><span data-ttu-id="c6e55-184">Dieser Fehler kann zurückgegeben werden, wenn Folgendes gilt:</span><span class="sxs-lookup"><span data-stu-id="c6e55-184">This error can be returned if:</span></span></p>
<ul>
<li><p><span data-ttu-id="c6e55-185">Es wurde ein ungültiger Name für <em>sztablename</em> angegeben.</span><span class="sxs-lookup"><span data-stu-id="c6e55-185">A bad name for <em>szTableName</em> was given.</span></span></p></li>
<li><p><span data-ttu-id="c6e55-186">Ein ungültiger Name für <em>szcolumnname</em> wurde angegeben.</span><span class="sxs-lookup"><span data-stu-id="c6e55-186">A bad name for <em>szColumnName</em> was given.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6e55-187">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="c6e55-187">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="c6e55-188">Dieser Fehler kann zurückgegeben werden, wenn Folgendes gilt:</span><span class="sxs-lookup"><span data-stu-id="c6e55-188">This error can be returned if:</span></span></p>
<ul>
<li><p><span data-ttu-id="c6e55-189">Es wurde eine ungültige <em>infolevel</em> angegeben.</span><span class="sxs-lookup"><span data-stu-id="c6e55-189">A bad <em>InfoLevel</em> was specified.</span></span></p></li>
<li><p><span data-ttu-id="c6e55-190">Ein NULL- <em>sztablename</em> -Wert wurde übermittelt.</span><span class="sxs-lookup"><span data-stu-id="c6e55-190">A NULL <em>szTableName</em> was passed in.</span></span></p></li>
<li><p><span data-ttu-id="c6e55-191">Der Puffer ist zu klein.</span><span class="sxs-lookup"><span data-stu-id="c6e55-191">The buffer is too small.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="c6e55-192">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c6e55-192">Remarks</span></span>

<span data-ttu-id="c6e55-193">**Jetgettablecolumninfo** und [jetgetcolumninfo](./jetgetcolumninfo-function.md) rufen Informationen zu einer Spalte ab.</span><span class="sxs-lookup"><span data-stu-id="c6e55-193">**JetGetTableColumnInfo** and [JetGetColumnInfo](./jetgetcolumninfo-function.md) both retrieve information about a column.</span></span> <span data-ttu-id="c6e55-194">Der Unterschied besteht darin, wie die Tabelle identifiziert wird:</span><span class="sxs-lookup"><span data-stu-id="c6e55-194">The difference between them is how the table is identified:</span></span>

  - <span data-ttu-id="c6e55-195">**Jetgettablecolumninfo** identifiziert eine Tabelle nach *TableID*.</span><span class="sxs-lookup"><span data-stu-id="c6e55-195">**JetGetTableColumnInfo** identifies a table by *tableid*.</span></span>

  - <span data-ttu-id="c6e55-196">[Jetgetcolumninfo](./jetgetcolumninfo-function.md) identifiziert eine Tabelle mit der Kombination aus *DBID* und *sztablename* .</span><span class="sxs-lookup"><span data-stu-id="c6e55-196">[JetGetColumnInfo](./jetgetcolumninfo-function.md) identifies a table by *dbid* and *szTableName* combination.</span></span>

<span data-ttu-id="c6e55-197">Beim Abrufen von Daten mit JET_ColInfoList, JET_ColInfoListSortColumnid oder JET_ColInfoListCompact wird eine temporäre Tabelle geöffnet.</span><span class="sxs-lookup"><span data-stu-id="c6e55-197">When retrieving data with JET_ColInfoList, JET_ColInfoListSortColumnid, or JET_ColInfoListCompact, a temporary table will be opened.</span></span> <span data-ttu-id="c6e55-198">Die temporäre Tabelle enthält Daten, und die [JET_COLUMNLIST](./jet-columnlist-structure.md) Struktur enthält ausreichende Informationen, um die temporäre Tabelle zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="c6e55-198">The temporary table contains data, and the [JET_COLUMNLIST](./jet-columnlist-structure.md) structure contains sufficient information to traverse the temporary table.</span></span> <span data-ttu-id="c6e55-199">Die temporäre Tabelle muss mit [jetclosetable](./jetclosetable-function.md)geschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="c6e55-199">The temporary table must be closed with [JetCloseTable](./jetclosetable-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="c6e55-200">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c6e55-200">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c6e55-201"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="c6e55-201"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="c6e55-202">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="c6e55-202">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6e55-203"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="c6e55-203"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="c6e55-204">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="c6e55-204">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6e55-205"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="c6e55-205"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="c6e55-206">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="c6e55-206">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6e55-207"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="c6e55-207"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="c6e55-208">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="c6e55-208">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6e55-209"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="c6e55-209"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="c6e55-210">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="c6e55-210">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6e55-211"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="c6e55-211"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="c6e55-212">Implementiert als <strong>jetgettablecolumninfow</strong> (Unicode) und <strong>jetgettablecolumninfoa</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="c6e55-212">Implemented as <strong>JetGetTableColumnInfoW</strong> (Unicode) and <strong>JetGetTableColumnInfoA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="c6e55-213">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c6e55-213">See Also</span></span>

[<span data-ttu-id="c6e55-214">Erweiterbare Speicher-Engine-Fehler</span><span class="sxs-lookup"><span data-stu-id="c6e55-214">Extensible Storage Engine Errors</span></span>](./extensible-storage-engine-errors.md)  
[<span data-ttu-id="c6e55-215">Fehler Behandlungsparameter</span><span class="sxs-lookup"><span data-stu-id="c6e55-215">Error Handling Parameters</span></span>](./error-handling-parameters.md)  
[<span data-ttu-id="c6e55-216">JET_COLUMNBASE</span><span class="sxs-lookup"><span data-stu-id="c6e55-216">JET_COLUMNBASE</span></span>](./jet-columnbase-structure.md)  
[<span data-ttu-id="c6e55-217">JET_COLUMNDEF</span><span class="sxs-lookup"><span data-stu-id="c6e55-217">JET_COLUMNDEF</span></span>](./jet-columndef-structure.md)  
[<span data-ttu-id="c6e55-218">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="c6e55-218">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="c6e55-219">JET_COLUMNLIST</span><span class="sxs-lookup"><span data-stu-id="c6e55-219">JET_COLUMNLIST</span></span>](./jet-columnlist-structure.md)  
[<span data-ttu-id="c6e55-220">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="c6e55-220">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="c6e55-221">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="c6e55-221">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="c6e55-222">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="c6e55-222">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="c6e55-223">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="c6e55-223">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="c6e55-224">Jetclosetable</span><span class="sxs-lookup"><span data-stu-id="c6e55-224">JetCloseTable</span></span>](./jetclosetable-function.md)  
[<span data-ttu-id="c6e55-225">Jetgetcolumninfo</span><span class="sxs-lookup"><span data-stu-id="c6e55-225">JetGetColumnInfo</span></span>](./jetgetcolumninfo-function.md)  
[<span data-ttu-id="c6e55-226">Jetgettablecolumninfo</span><span class="sxs-lookup"><span data-stu-id="c6e55-226">JetGetTableColumnInfo</span></span>]()
