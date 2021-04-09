---
description: 'Weitere Informationen zu: jetgettableinfo-Funktion'
title: JetGetTableInfo-Funktion
TOCTitle: JetGetTableInfo Function
ms:assetid: 0602186c-b5c3-44b5-87df-482680442afd
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269177(v=EXCHG.10)
ms:contentKeyID: 32765480
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetTableInfoW
- JetGetTableInfo
- JetGetTableInfoA
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3362b5da8c6a79d78782e37920b9761b9888b15f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960680"
---
# <a name="jetgettableinfo-function"></a><span data-ttu-id="cd912-103">JetGetTableInfo-Funktion</span><span class="sxs-lookup"><span data-stu-id="cd912-103">JetGetTableInfo Function</span></span>


<span data-ttu-id="cd912-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="cd912-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgettableinfo-function"></a><span data-ttu-id="cd912-105">JetGetTableInfo-Funktion</span><span class="sxs-lookup"><span data-stu-id="cd912-105">JetGetTableInfo Function</span></span>

<span data-ttu-id="cd912-106">Die **jetgettableinfo** -Funktion Ruft verschiedene Informationen zu einer Tabelle in einer Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="cd912-106">The **JetGetTableInfo** function retrieves various pieces of information about a table in a database.</span></span>

```cpp
    JET_ERR JET_API JetGetTableInfo(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         void* pvResult,
      __in          unsigned long cbMax,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a><span data-ttu-id="cd912-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="cd912-107">Parameters</span></span>

<span data-ttu-id="cd912-108">*-sid*</span><span class="sxs-lookup"><span data-stu-id="cd912-108">*sesid*</span></span>

<span data-ttu-id="cd912-109">Der für den API-Befehl zu verwendende Daten Bank Sitzungs Kontext.</span><span class="sxs-lookup"><span data-stu-id="cd912-109">The database session context to use for the API call.</span></span>

<span data-ttu-id="cd912-110">*TableID*</span><span class="sxs-lookup"><span data-stu-id="cd912-110">*tableid*</span></span>

<span data-ttu-id="cd912-111">Die Tabelle, auf die die Informationen angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="cd912-111">The table that the information applies to.</span></span>

<span data-ttu-id="cd912-112">*pvresult*</span><span class="sxs-lookup"><span data-stu-id="cd912-112">*pvResult*</span></span>

<span data-ttu-id="cd912-113">Zeiger auf einen Puffer, der die Informationen empfängt.</span><span class="sxs-lookup"><span data-stu-id="cd912-113">Pointer to a buffer that will receive the information.</span></span> <span data-ttu-id="cd912-114">Der Typ des Puffers ist von *infolevel* abhängig.</span><span class="sxs-lookup"><span data-stu-id="cd912-114">The type of the buffer is dependent on *InfoLevel*.</span></span> <span data-ttu-id="cd912-115">Es liegt in der Verantwortung des Aufrufers, den Puffer entsprechend auszurichten.</span><span class="sxs-lookup"><span data-stu-id="cd912-115">It is the responsibility of the caller to align the buffer appropriately.</span></span>

<span data-ttu-id="cd912-116">*cbmax*</span><span class="sxs-lookup"><span data-stu-id="cd912-116">*cbMax*</span></span>

<span data-ttu-id="cd912-117">Die Größe (in Bytes) des Puffers, der in *pvresult* übergeben wurde.</span><span class="sxs-lookup"><span data-stu-id="cd912-117">The size, in bytes, of the buffer that was passed in *pvResult*.</span></span>

<span data-ttu-id="cd912-118">*Infolevel*</span><span class="sxs-lookup"><span data-stu-id="cd912-118">*InfoLevel*</span></span>

<span data-ttu-id="cd912-119">Der Typ der Informationen, die für die durch *TableID* angegebene Tabelle abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="cd912-119">The type of information that will be retrieved for the table that is specified by *tableid*.</span></span> <span data-ttu-id="cd912-120">Das Format der Daten, die in *pvresult* gespeichert sind, ist von *infolevel* abhängig.</span><span class="sxs-lookup"><span data-stu-id="cd912-120">The format of the data that is stored in *pvResult* is dependent on *InfoLevel*.</span></span>

<span data-ttu-id="cd912-121">Die folgenden Optionen können für diesen Parameter festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="cd912-121">The following options can be set for this parameter:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="cd912-122">Wert</span><span class="sxs-lookup"><span data-stu-id="cd912-122">Value</span></span></p></th>
<th><p><span data-ttu-id="cd912-123">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="cd912-123">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cd912-124">JET_TblInfo</span><span class="sxs-lookup"><span data-stu-id="cd912-124">JET_TblInfo</span></span></p></td>
<td><p><span data-ttu-id="cd912-125"><em>pvresult</em> wird als <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a> Struktur interpretiert.</span><span class="sxs-lookup"><span data-stu-id="cd912-125"><em>pvResult</em> is interpreted as a <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a> structure.</span></span> <span data-ttu-id="cd912-126">Wenn die Methode erfolgreich ist, wird die <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a> Struktur mit den entsprechenden Daten ausgefüllt.</span><span class="sxs-lookup"><span data-stu-id="cd912-126">If the method succeeds, the <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a> structure is filled in with the appropriate data.</span></span> <span data-ttu-id="cd912-127">Wenn ein Fehler auftritt, ist der Inhalt nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="cd912-127">If it fails, the contents are undefined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd912-128">JET_TblInfoDbid</span><span class="sxs-lookup"><span data-stu-id="cd912-128">JET_TblInfoDbid</span></span></p></td>
<td><p><span data-ttu-id="cd912-129"><em>pvresult</em> wird als ein Array von zwei <a href="gg269248(v=exchg.10).md">JET_DBID</a> Objekten behandelt.</span><span class="sxs-lookup"><span data-stu-id="cd912-129"><em>pvResult</em> is treated as an array of two <a href="gg269248(v=exchg.10).md">JET_DBID</a> objects.</span></span> <span data-ttu-id="cd912-130">Der Daten Bank Bezeichner der Datenbank, die Besitzer der Tabelle ist, wird in diesem Array zweimal gespeichert.</span><span class="sxs-lookup"><span data-stu-id="cd912-130">The database identifier of the database that owns the table is stored in this array twice.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cd912-131">JET_TblInfoDumpTable</span><span class="sxs-lookup"><span data-stu-id="cd912-131">JET_TblInfoDumpTable</span></span></p></td>
<td><p><span data-ttu-id="cd912-132">JET_TblInfoDumpTable ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="cd912-132">JET_TblInfoDumpTable is deprecated.</span></span> <span data-ttu-id="cd912-133">Die API gibt JET_errFeatureNotAvailable zurück.</span><span class="sxs-lookup"><span data-stu-id="cd912-133">The API will return JET_errFeatureNotAvailable.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd912-134">JET_TblInfoName</span><span class="sxs-lookup"><span data-stu-id="cd912-134">JET_TblInfoName</span></span></p></td>
<td><p><span data-ttu-id="cd912-135">JET_TblInfoName Ruft den Namen der Tabelle ab und speichert Sie in <em>pvresult</em>.</span><span class="sxs-lookup"><span data-stu-id="cd912-135">JET_TblInfoName retrieves the name of the table and stores it in <em>pvResult</em>.</span></span> <span data-ttu-id="cd912-136">Wenn der Puffer zu klein ist, ist das Verhalten nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="cd912-136">If the buffer is too small, the behavior is undefined.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cd912-137">JET_TblInfoMostMany</span><span class="sxs-lookup"><span data-stu-id="cd912-137">JET_TblInfoMostMany</span></span></p></td>
<td><p><span data-ttu-id="cd912-138">JET_TblInfoMostMany Ruft den Namen der Tabelle ab und speichert Sie in <em>pvresult</em>.</span><span class="sxs-lookup"><span data-stu-id="cd912-138">JET_TblInfoMostMany retrieves the name of the table and stores it in <em>pvResult</em>.</span></span> <span data-ttu-id="cd912-139">Wenn der Puffer zu klein ist, ist das Verhalten nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="cd912-139">If the buffer is too small, the behavior is undefined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd912-140">JET_TblInfoOLC</span><span class="sxs-lookup"><span data-stu-id="cd912-140">JET_TblInfoOLC</span></span></p></td>
<td><p><span data-ttu-id="cd912-141">JET_TblInfoOLC ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="cd912-141">JET_TblInfoOLC is deprecated.</span></span> <span data-ttu-id="cd912-142">Die API gibt JET_errFeatureNotAvailable zurück.</span><span class="sxs-lookup"><span data-stu-id="cd912-142">The API will return JET_errFeatureNotAvailable.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cd912-143">JET_TblInfoRvt</span><span class="sxs-lookup"><span data-stu-id="cd912-143">JET_TblInfoRvt</span></span></p></td>
<td><p><span data-ttu-id="cd912-144">JET_TblInfoRvt ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="cd912-144">JET_TblInfoRvt is deprecated.</span></span> <span data-ttu-id="cd912-145">Die API gibt JET_errQueryNotSupported zurück.</span><span class="sxs-lookup"><span data-stu-id="cd912-145">The API will return JET_errQueryNotSupported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd912-146">JET_TblInfoResetOLC</span><span class="sxs-lookup"><span data-stu-id="cd912-146">JET_TblInfoResetOLC</span></span></p></td>
<td><p><span data-ttu-id="cd912-147">JET_TblInfoResetOLC ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="cd912-147">JET_TblInfoResetOLC is deprecated.</span></span> <span data-ttu-id="cd912-148">Die API gibt JET_errFeatureNotAvailable zurück.</span><span class="sxs-lookup"><span data-stu-id="cd912-148">The API will return JET_errFeatureNotAvailable.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cd912-149">JET_TblInfoSpaceAlloc</span><span class="sxs-lookup"><span data-stu-id="cd912-149">JET_TblInfoSpaceAlloc</span></span></p></td>
<td><p><span data-ttu-id="cd912-150"><em>pvresult</em> wird als ein Array aus zwei ulongs interpretiert:</span><span class="sxs-lookup"><span data-stu-id="cd912-150"><em>pvResult</em> is interpreted as an array of two ULONGs:</span></span></p>
<ul>
<li><p><span data-ttu-id="cd912-151">Der erste <strong>ulong</strong> -Wert ist die Anzahl der Seiten in der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="cd912-151">The first <strong>ULONG</strong> is the number of pages in the table.</span></span></p></li>
<li><p><span data-ttu-id="cd912-152">Der zweite <strong>ulong</strong> -Wert ist die zieldichte von Seiten für die Tabelle.</span><span class="sxs-lookup"><span data-stu-id="cd912-152">The second <strong>ULONG</strong> is the target density of pages for the table.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd912-153">JET_TblInfoSpaceAvailable</span><span class="sxs-lookup"><span data-stu-id="cd912-153">JET_TblInfoSpaceAvailable</span></span></p></td>
<td><p><span data-ttu-id="cd912-154"><em>pvresult</em> wird als <strong>ulong</strong>interpretiert.</span><span class="sxs-lookup"><span data-stu-id="cd912-154"><em>pvResult</em> is interpreted as a <strong>ULONG</strong>.</span></span> <span data-ttu-id="cd912-155">Der <strong>ulong</strong> ist die Summe aus der Anzahl der Seiten, die in der Tabelle, den Indizes und der Struktur für lange Werte verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="cd912-155">The <strong>ULONG</strong> is the sum of the number of pages that are available in the table, its indexes, and the long value tree.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cd912-156">JET_TblInfoSpaceOwned</span><span class="sxs-lookup"><span data-stu-id="cd912-156">JET_TblInfoSpaceOwned</span></span></p></td>
<td><p><span data-ttu-id="cd912-157"><em>pvresult</em> wird als <strong>ulong</strong>interpretiert.</span><span class="sxs-lookup"><span data-stu-id="cd912-157"><em>pvResult</em> is interpreted as a <strong>ULONG</strong>.</span></span> <span data-ttu-id="cd912-158"><strong>Ulong</strong> ist die Summe der Anzahl der Seiten, die im Besitz der Tabelle sind (einschließlich der Indizes und der Long-Wert-Struktur und sämtlicher verfügbarer Seiten).</span><span class="sxs-lookup"><span data-stu-id="cd912-158">The <strong>ULONG</strong> is the sum of the number of pages that are owned by the table (including its indexes, and the long value tree and any available pages therein).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd912-159">JET_TblInfoSpaceUsage</span><span class="sxs-lookup"><span data-stu-id="cd912-159">JET_TblInfoSpaceUsage</span></span></p></td>
<td><p><span data-ttu-id="cd912-160">Das Verhalten der API hängt davon ab, wie groß der an die API weiter gegebene Puffer ist.</span><span class="sxs-lookup"><span data-stu-id="cd912-160">The behavior of the API depends on how large the buffer that is passed to the API is.</span></span> <span data-ttu-id="cd912-161">Zwei <em>cbmax</em> -Werte müssen mindestens (2 \* sizeof (ULONG)) sein.</span><span class="sxs-lookup"><span data-stu-id="cd912-161">Two <em>cbMax</em> values must be at least ( 2 \* sizeof( ULONG ) ).</span></span></p>
<ul>
<li><p><span data-ttu-id="cd912-162">Wenn <em>cbmax</em> (2 \* sizeof (ULONG)) ist, wird <em>pvresult</em> als ein Array aus zwei ulongs interpretiert:</span><span class="sxs-lookup"><span data-stu-id="cd912-162">If <em>cbMax</em> is ( 2 \* sizeof( ULONG ) ), <em>pvResult</em> is interpreted as an array of two ULONGs:</span></span></p>
<ul>
<li><p><span data-ttu-id="cd912-163">Der erste <strong>ulong</strong> -Wert ist die Anzahl der im Besitz befindlichen Blöcke der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="cd912-163">The first <strong>ULONG</strong> is the number of Owned Extents of the table.</span></span></p></li>
<li><p><span data-ttu-id="cd912-164">Der zweite <strong>ulong</strong> -Wert ist die Anzahl der verfügbaren Blöcke der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="cd912-164">The second <strong>ULONG</strong> is the number of Available Extents of the table.</span></span></p></li>
</ul></li>
<li><p><span data-ttu-id="cd912-165"><em>pvresult</em> wird als ein Array von interpretiert:</span><span class="sxs-lookup"><span data-stu-id="cd912-165"><em>pvResult</em> is interpreted as an array of:</span></span></p>
<ul>
<li><p><span data-ttu-id="cd912-166">Der erste <strong>ulong</strong> -Wert ist die Anzahl der im Besitz befindlichen Blöcke der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="cd912-166">The first <strong>ULONG</strong> is the number of Owned Extents of the table.</span></span></p></li>
<li><p><span data-ttu-id="cd912-167">Der zweite <strong>ulong</strong> -Wert ist die Anzahl der verfügbaren Blöcke der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="cd912-167">The second <strong>ULONG</strong> is the number of Available Extents of the table.</span></span></p></li>
</ul></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cd912-168">JET_TblInfoTemplateTableName</span><span class="sxs-lookup"><span data-stu-id="cd912-168">JET_TblInfoTemplateTableName</span></span></p></td>
<td><p><span data-ttu-id="cd912-169"><em>pvresult</em> wird als Zeichen folgen Puffer interpretiert.</span><span class="sxs-lookup"><span data-stu-id="cd912-169"><em>pvResult</em> is interpreted as a string buffer.</span></span> <span data-ttu-id="cd912-170">Der Puffer muss mindestens JET_cbNameMost + 1 sein, einschließlich des abschließenden <strong>null</strong>-Werte.</span><span class="sxs-lookup"><span data-stu-id="cd912-170">The buffer must be at least JET_cbNameMost + 1, including the terminating <strong>NULL</strong>.</span></span> <span data-ttu-id="cd912-171">Wenn die Tabelle eine abgeleitete Tabelle ist, wird der Puffer mit dem Namen der Tabelle ausgefüllt, von der die abgeleitete Tabelle Ihre DDL geerbt hat.</span><span class="sxs-lookup"><span data-stu-id="cd912-171">If the table is a derived table, the buffer will be filled in with the name of the table from which the derived table inherited its DDL.</span></span> <span data-ttu-id="cd912-172">Wenn die Tabelle keine abgeleitete Tabelle ist, wird für den Puffer eine leere Zeichenfolge verwendet.</span><span class="sxs-lookup"><span data-stu-id="cd912-172">If the table is not a derived table, the buffer will an empty string.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="cd912-173">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cd912-173">Return Value</span></span>

<span data-ttu-id="cd912-174">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="cd912-174">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="cd912-175">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="cd912-175">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="cd912-176">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="cd912-176">Return code</span></span></p></th>
<th><p><span data-ttu-id="cd912-177">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cd912-177">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cd912-178">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="cd912-178">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="cd912-179">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="cd912-179">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd912-180">JET_errBufferTooSmall</span><span class="sxs-lookup"><span data-stu-id="cd912-180">JET_errBufferTooSmall</span></span></p></td>
<td><p><span data-ttu-id="cd912-181">Der Puffer war zu klein.</span><span class="sxs-lookup"><span data-stu-id="cd912-181">The buffer was too small.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cd912-182">JET_errFeatureNotAvailable</span><span class="sxs-lookup"><span data-stu-id="cd912-182">JET_errFeatureNotAvailable</span></span></p></td>
<td><p><span data-ttu-id="cd912-183">Es wurde eine veraltete <em>infolevel</em> angegeben.</span><span class="sxs-lookup"><span data-stu-id="cd912-183">A deprecated <em>InfoLevel</em> was specified.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd912-184">JET_errInvalidBufferSize</span><span class="sxs-lookup"><span data-stu-id="cd912-184">JET_errInvalidBufferSize</span></span></p></td>
<td><p><span data-ttu-id="cd912-185">Der Puffer war nicht die richtige Größe.</span><span class="sxs-lookup"><span data-stu-id="cd912-185">The buffer was not the right size.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cd912-186">JET_errInvalidOperation</span><span class="sxs-lookup"><span data-stu-id="cd912-186">JET_errInvalidOperation</span></span></p></td>
<td><p><span data-ttu-id="cd912-187">Die Tabelle, die in die Tabelle übertragen wurde, war eine temporäre Tabelle, und die angeforderte <em>infolevel</em> kann für eine temporäre Tabelle nicht abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="cd912-187">The table that was passed in was a temporary table, and the requested <em>InfoLevel</em> cannot be retrieved for a temporary table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd912-188">JET_errObjectNotFound</span><span class="sxs-lookup"><span data-stu-id="cd912-188">JET_errObjectNotFound</span></span></p></td>
<td><p><span data-ttu-id="cd912-189">Die Tabelle, die in die Tabelle übertragen wurde, war eine temporäre Tabelle, und die angeforderte <em>infolevel</em> kann für eine temporäre Tabelle nicht abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="cd912-189">The table that was passed in was a temporary table, and the requested <em>InfoLevel</em> cannot be retrieved for a temporary table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cd912-190">JET_errQueryNotSupported</span><span class="sxs-lookup"><span data-stu-id="cd912-190">JET_errQueryNotSupported</span></span></p></td>
<td><p><span data-ttu-id="cd912-191"><em>Infolevel</em> wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="cd912-191">The <em>InfoLevel</em> is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd912-192">JET_errTableInUse</span><span class="sxs-lookup"><span data-stu-id="cd912-192">JET_errTableInUse</span></span></p></td>
<td><p><span data-ttu-id="cd912-193">Die Tabelle wird von einem anderen Daten Bank Vorgang verwendet.</span><span class="sxs-lookup"><span data-stu-id="cd912-193">The table is being used by another database operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cd912-194">JET_errTableLocked</span><span class="sxs-lookup"><span data-stu-id="cd912-194">JET_errTableLocked</span></span></p></td>
<td><p><span data-ttu-id="cd912-195">Die Tabelle wird durch einen anderen Daten Bank Vorgang gesperrt.</span><span class="sxs-lookup"><span data-stu-id="cd912-195">The table is locked by another database operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd912-196">JET_wrnTableInUseBySystem</span><span class="sxs-lookup"><span data-stu-id="cd912-196">JET_wrnTableInUseBySystem</span></span></p></td>
<td><p><span data-ttu-id="cd912-197">Die Tabelle wird vom System verwendet.</span><span class="sxs-lookup"><span data-stu-id="cd912-197">The table is being used by the system.</span></span> <span data-ttu-id="cd912-198">Diese Warnung ist nicht schwerwiegend.</span><span class="sxs-lookup"><span data-stu-id="cd912-198">This warning is nonfatal.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="cd912-199">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cd912-199">Remarks</span></span>

<span data-ttu-id="cd912-200">Einige Informationen sind für temporäre Tabellen ungültig (siehe [jetopdtemptable](./jetopentemptable-function.md)).</span><span class="sxs-lookup"><span data-stu-id="cd912-200">Some pieces of information are not valid for temporary tables (See [JetOpenTempTable](./jetopentemptable-function.md)).</span></span>

<span data-ttu-id="cd912-201">Die Tabellenstatistiken enthalten die Anzahl der Datensätze und die Anzahl der Seiten im gruppierten Index (d. h. den Index, der die Daten des Datensatzes enthält).</span><span class="sxs-lookup"><span data-stu-id="cd912-201">The table statistics include the number of records and the number of pages in the clustered index (that is, the index containing the record data).</span></span> <span data-ttu-id="cd912-202">Der Zugriff auf die Index Statistiken erfolgt separat über den Namen, mithilfe von [jetgetindexinfo](./jetgetindexinfo-function.md) oder [jetgettableindexinfo](./jetgettableindexinfo-function.md).</span><span class="sxs-lookup"><span data-stu-id="cd912-202">The index statistics are accessed separately by name, using [JetGetIndexInfo](./jetgetindexinfo-function.md) or [JetGetTableIndexInfo](./jetgettableindexinfo-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="cd912-203">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cd912-203">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cd912-204"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="cd912-204"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="cd912-205">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="cd912-205">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd912-206"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="cd912-206"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="cd912-207">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="cd912-207">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cd912-208"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="cd912-208"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="cd912-209">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="cd912-209">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd912-210"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="cd912-210"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="cd912-211">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="cd912-211">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cd912-212"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="cd912-212"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="cd912-213">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="cd912-213">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd912-214"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="cd912-214"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="cd912-215">Implementiert als <strong>jetgettableinfow</strong> (Unicode) und <strong>jetgettableinfoa</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="cd912-215">Implemented as <strong>JetGetTableInfoW</strong> (Unicode) and <strong>JetGetTableInfoA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="cd912-216">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="cd912-216">See Also</span></span>

[<span data-ttu-id="cd912-217">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="cd912-217">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="cd912-218">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="cd912-218">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="cd912-219">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="cd912-219">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="cd912-220">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="cd912-220">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="cd912-221">JET_OBJECTINFO</span><span class="sxs-lookup"><span data-stu-id="cd912-221">JET_OBJECTINFO</span></span>](./jet-objectinfo-structure.md)  
[<span data-ttu-id="cd912-222">Jetgetindexinfo</span><span class="sxs-lookup"><span data-stu-id="cd912-222">JetGetIndexInfo</span></span>](./jetgetindexinfo-function.md)  
[<span data-ttu-id="cd912-223">Jetgetobjectinfo</span><span class="sxs-lookup"><span data-stu-id="cd912-223">JetGetObjectInfo</span></span>](./jetgetobjectinfo-function.md)  
[<span data-ttu-id="cd912-224">Jetgettableindexinfo</span><span class="sxs-lookup"><span data-stu-id="cd912-224">JetGetTableIndexInfo</span></span>](./jetgettableindexinfo-function.md)  
[<span data-ttu-id="cd912-225">Jetopumtemptable</span><span class="sxs-lookup"><span data-stu-id="cd912-225">JetOpenTempTable</span></span>](./jetopentemptable-function.md)
