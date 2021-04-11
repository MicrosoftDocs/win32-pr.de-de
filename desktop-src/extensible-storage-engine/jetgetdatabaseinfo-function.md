---
description: 'Weitere Informationen zu: jetgetdatabaseingefo-Funktion'
title: JetGetDatabaseInfo-Funktion
TOCTitle: JetGetDatabaseInfo Function
ms:assetid: bd3f92d0-7e98-4aa6-87c5-1c2760cbd1b5
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294076(v=EXCHG.10)
ms:contentKeyID: 32765691
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 81c414a1dd38f621ba86bf7b1c9ce87710801446
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216296"
---
# <a name="jetgetdatabaseinfo-function"></a><span data-ttu-id="6c628-103">JetGetDatabaseInfo-Funktion</span><span class="sxs-lookup"><span data-stu-id="6c628-103">JetGetDatabaseInfo Function</span></span>


<span data-ttu-id="6c628-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="6c628-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetdatabaseinfo-function"></a><span data-ttu-id="6c628-105">JetGetDatabaseInfo-Funktion</span><span class="sxs-lookup"><span data-stu-id="6c628-105">JetGetDatabaseInfo Function</span></span>

<span data-ttu-id="6c628-106">Die **jetgetdatabaseinfo** -Funktion Ruft verschiedene Arten von Informationen über die Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="6c628-106">The **JetGetDatabaseInfo** function retrieves various types of information about the database.</span></span> <span data-ttu-id="6c628-107">Diese API kann aufgerufen werden, während eine Datenbank angefügt oder Online ist (mit **jetgetdatabaseinfo**) oder wenn die Datenbank oder Datenbank-Engine offline ist (mit [jetgetdatabasefileinfo](./jetgetdatabasefileinfo-function.md)).</span><span class="sxs-lookup"><span data-stu-id="6c628-107">This API can be called while a database is attached or online (with **JetGetDatabaseInfo**) or while the database or database engine is offline (with [JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md)).</span></span>

```cpp
    JET_ERR JET_API JetGetDatabaseInfo(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __out         void* pvResult,
      __in          unsigned long cbMax,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a><span data-ttu-id="6c628-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="6c628-108">Parameters</span></span>

<span data-ttu-id="6c628-109">*-sid*</span><span class="sxs-lookup"><span data-stu-id="6c628-109">*sesid*</span></span>

<span data-ttu-id="6c628-110">Die Sitzung, die für diesen-Befehl verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="6c628-110">The session to use for this call.</span></span>

<span data-ttu-id="6c628-111">*DBID*</span><span class="sxs-lookup"><span data-stu-id="6c628-111">*dbid*</span></span>

<span data-ttu-id="6c628-112">Die [JET_DBID](./jet-dbid.md) für die Datenbank, aus der die Informationen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="6c628-112">The [JET_DBID](./jet-dbid.md) for the database to retrieve the information from.</span></span>

<span data-ttu-id="6c628-113">*pvresult*</span><span class="sxs-lookup"><span data-stu-id="6c628-113">*pvResult*</span></span>

<span data-ttu-id="6c628-114">Zeiger auf einen Puffer, der die angegebenen Informationen empfängt.</span><span class="sxs-lookup"><span data-stu-id="6c628-114">Pointer to a buffer which will receive the specified information.</span></span> <span data-ttu-id="6c628-115">Die Größe des Puffers in Bytes wird in *cbmax* übermittelt.</span><span class="sxs-lookup"><span data-stu-id="6c628-115">The size of the buffer, in bytes, is passed in *cbMax*.</span></span>

<span data-ttu-id="6c628-116">Bei einem Fehler ist der Inhalt von *pvresult* nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="6c628-116">On failure the contents of *pvResult* are undefined.</span></span>

<span data-ttu-id="6c628-117">Die in *pvresult* gespeicherten Informationen hängen von *infolevel* ab.</span><span class="sxs-lookup"><span data-stu-id="6c628-117">The information stored in *pvResult* depends on *InfoLevel*.</span></span>

<span data-ttu-id="6c628-118">*cbmax*</span><span class="sxs-lookup"><span data-stu-id="6c628-118">*cbMax*</span></span>

<span data-ttu-id="6c628-119">Die Größe (in Bytes) des Puffers, der in *pvresult* übergeben wurde.</span><span class="sxs-lookup"><span data-stu-id="6c628-119">The size, in bytes, of the buffer that was passed in *pvResult*.</span></span>

<span data-ttu-id="6c628-120">*Infolevel*</span><span class="sxs-lookup"><span data-stu-id="6c628-120">*InfoLevel*</span></span>

<span data-ttu-id="6c628-121">*Infolevel* gibt an, welche Art von Informationen über die angegebene Datenbank abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="6c628-121">*InfoLevel* specifies which type of information should be retrieved about the specified database.</span></span> <span data-ttu-id="6c628-122">Dies wirkt sich darauf aus, wie *pvresult* interpretiert wird.</span><span class="sxs-lookup"><span data-stu-id="6c628-122">It affects how *pvResult* is interpreted.</span></span> <span data-ttu-id="6c628-123">Einige *infolevel* sind nur in der Offline Version ([jetgetdatabasefileinfo](./jetgetdatabasefileinfo-function.md)) oder Online (**jetgetdatabaseinfo**) der API verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6c628-123">Some *InfoLevel* are available only in the offline ([JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md)) or online (**JetGetDatabaseInfo**) version of the API.</span></span>

<span data-ttu-id="6c628-124">Wenn der bereitgestellte *pvresult* -Puffer zu klein ist, wird entweder JET_errInvalidBufferSize oder JET_errBufferTooSmall abhängig von *infolevel* zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6c628-124">If the *pvResult* buffer provided is too small, either JET_errInvalidBufferSize or JET_errBufferTooSmall will be returned depending on the *InfoLevel*.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6c628-125">Wert</span><span class="sxs-lookup"><span data-stu-id="6c628-125">Value</span></span></p></th>
<th><p><span data-ttu-id="6c628-126">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="6c628-126">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6c628-127">JET_DbInfoCollate</span><span class="sxs-lookup"><span data-stu-id="6c628-127">JET_DbInfoCollate</span></span></p></td>
<td><p><span data-ttu-id="6c628-128">Wird noch nicht unterstützt und gibt Standardwerte zurück.</span><span class="sxs-lookup"><span data-stu-id="6c628-128">Not yet supported and return default values.</span></span> <span data-ttu-id="6c628-129">Darf nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6c628-129">Do not use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c628-130">JET_DbInfoConnect</span><span class="sxs-lookup"><span data-stu-id="6c628-130">JET_DbInfoConnect</span></span></p></td>
<td><p><span data-ttu-id="6c628-131">Diese <em>infolevels</em> sind veraltet und werden zurzeit nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6c628-131">These <em>InfoLevels</em> are deprecated and are not currently supported.</span></span> <span data-ttu-id="6c628-132">Darf nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6c628-132">Do not use.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c628-133">JET_DbInfoCountry</span><span class="sxs-lookup"><span data-stu-id="6c628-133">JET_DbInfoCountry</span></span></p></td>
<td><p><span data-ttu-id="6c628-134">Wird noch nicht unterstützt und gibt Standardwerte zurück.</span><span class="sxs-lookup"><span data-stu-id="6c628-134">Not yet supported and return default values.</span></span> <span data-ttu-id="6c628-135">Darf nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6c628-135">Do not use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c628-136">JET_DbInfoCp</span><span class="sxs-lookup"><span data-stu-id="6c628-136">JET_DbInfoCp</span></span></p></td>
<td><p><span data-ttu-id="6c628-137">Wird noch nicht unterstützt und gibt Standardwerte zurück.</span><span class="sxs-lookup"><span data-stu-id="6c628-137">Not yet supported and return default values.</span></span> <span data-ttu-id="6c628-138">Darf nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6c628-138">Do not use.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c628-139">JET_DbInfoFilename</span><span class="sxs-lookup"><span data-stu-id="6c628-139">JET_DbInfoFilename</span></span></p></td>
<td><p><span data-ttu-id="6c628-140"><em>pvresult</em> wird als Zeichen folgen Puffer (Char \*) interpretiert.</span><span class="sxs-lookup"><span data-stu-id="6c628-140"><em>pvResult</em> will be interpreted as a string buffer (char \*).</span></span> <span data-ttu-id="6c628-141">Es wird ein MAX_PATH Puffer vorgeschlagen, jedoch nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="6c628-141">A MAX_PATH buffer is suggested, however not required.</span></span> <span data-ttu-id="6c628-142">Wenn der Puffer nicht lang genug ist, werden JET_errBufferTooSmall zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6c628-142">If the buffer is not long enough, JET_errBufferTooSmall will be returned.</span></span> <span data-ttu-id="6c628-143">Die Zeichenfolge wird mit dem Pfad der Datenbank für diese DBID aufgefüllt.</span><span class="sxs-lookup"><span data-stu-id="6c628-143">The string will be populated with the path of the database for this DBID.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c628-144">JET_DbInfoFilesize</span><span class="sxs-lookup"><span data-stu-id="6c628-144">JET_DbInfoFilesize</span></span></p></td>
<td><p><span data-ttu-id="6c628-145"><em>pvresult</em> wird als DWORD (4 Bytes) interpretiert.</span><span class="sxs-lookup"><span data-stu-id="6c628-145"><em>pvResult</em> will be interpreted as a DWORD (4 bytes).</span></span> <span data-ttu-id="6c628-146">Gibt die Größe der Datenbank auf Seiten zurück.</span><span class="sxs-lookup"><span data-stu-id="6c628-146">Returns the size of the database in pages.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c628-147">JET_DbInfoIsam</span><span class="sxs-lookup"><span data-stu-id="6c628-147">JET_DbInfoIsam</span></span></p></td>
<td><p><span data-ttu-id="6c628-148">Diese <em>infolevels</em> sind veraltet und werden zurzeit nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6c628-148">These <em>InfoLevels</em> are deprecated and are not currently supported.</span></span> <span data-ttu-id="6c628-149">Darf nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6c628-149">Do not use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c628-150">JET_DbInfoLCID</span><span class="sxs-lookup"><span data-stu-id="6c628-150">JET_DbInfoLCID</span></span></p></td>
<td><p><span data-ttu-id="6c628-151">(Windows XP und höher) Diese <em>infolevel</em> wurde ursprünglich wie folgt angegeben: JET_DbInfoLangid (Windows 2000)</span><span class="sxs-lookup"><span data-stu-id="6c628-151">(Windows XP and later) This <em>InfoLevel</em> was originally specified as: JET_DbInfoLangid (Windows 2000)</span></span></p>
<p><span data-ttu-id="6c628-152"><em>pvresult</em> wird als Long interpretiert.</span><span class="sxs-lookup"><span data-stu-id="6c628-152"><em>pvResult</em> will be interpreted as a long.</span></span> <span data-ttu-id="6c628-153">Dadurch wird der mit dieser Datenbank verknüpfte Gebiets Schema Bezeichner (LCID) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6c628-153">This returns the Locale identifier (LCID) associate with this database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c628-154">JET_DbInfoMisc</span><span class="sxs-lookup"><span data-stu-id="6c628-154">JET_DbInfoMisc</span></span></p></td>
<td><p><span data-ttu-id="6c628-155"><em>pvresult</em> wird als <a href="gg294147(v=exchg.10).md">JET_DBINFOMISC</a>interpretiert.</span><span class="sxs-lookup"><span data-stu-id="6c628-155"><em>pvResult</em> will be interpreted as a <a href="gg294147(v=exchg.10).md">JET_DBINFOMISC</a>.</span></span> <span data-ttu-id="6c628-156">Die <a href="gg294147(v=exchg.10).md">JET_DBINFOMISC</a> Struktur wird mit Informationen zu der angegebenen Datenbank aufgefüllt.</span><span class="sxs-lookup"><span data-stu-id="6c628-156">The <a href="gg294147(v=exchg.10).md">JET_DBINFOMISC</a> structure will be populated with information pertaining to the database specified.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c628-157">JET_DbInfoOptions</span><span class="sxs-lookup"><span data-stu-id="6c628-157">JET_DbInfoOptions</span></span></p></td>
<td><p><span data-ttu-id="6c628-158"><em>pvresult</em> wird als <a href="gg294066(v=exchg.10).md">JET_GRBIT</a> (DWORD) interpretiert.</span><span class="sxs-lookup"><span data-stu-id="6c628-158"><em>pvResult</em> will be interpreted as a <a href="gg294066(v=exchg.10).md">JET_GRBIT</a> (DWORD).</span></span> <span data-ttu-id="6c628-159">Hiermit wird zurückgegeben, ob die Datenbank im exklusiven Modus geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="6c628-159">This returns whether the database is opened in exclusive mode.</span></span> <span data-ttu-id="6c628-160">Wenn sich die Datenbank im exklusiven Modus befindet JET_bitDbExclusive in der bereitgestellten <a href="gg294066(v=exchg.10).md">JET_GRBIT</a> festgelegt werden, andernfalls wird 0 (null) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6c628-160">If the database is in exclusive mode JET_bitDbExclusive will be set in the <a href="gg294066(v=exchg.10).md">JET_GRBIT</a> provided, otherwise zero is set.</span></span> <span data-ttu-id="6c628-161">Beachten Sie, dass keine anderen Datenbank- <em>grbit</em> -Optionen für <a href="gg294074(v=exchg.10).md">jetattachdatabase</a> und <a href="gg269299(v=exchg.10).md">jetopendatabase</a> zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="6c628-161">Note other database <em>grbit</em> options for <a href="gg294074(v=exchg.10).md">JetAttachDatabase</a> and <a href="gg269299(v=exchg.10).md">JetOpenDatabase</a> are not returned.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c628-162">JET_DbInfoPageSize</span><span class="sxs-lookup"><span data-stu-id="6c628-162">JET_DbInfoPageSize</span></span></p></td>
<td><p><span data-ttu-id="6c628-163">Nur unter Windows XP und höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6c628-163">Available only on Windows XP and later.</span></span> <span data-ttu-id="6c628-164"><em>pvresult</em> wird als Ganzzahl ohne Vorzeichen long interpretiert.</span><span class="sxs-lookup"><span data-stu-id="6c628-164"><em>pvResult</em> will be interpreted as a unsigned long.</span></span> <span data-ttu-id="6c628-165">Dadurch wird die Seitengröße der Datenbank in Bytes zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6c628-165">This will return the page size of the database in bytes.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c628-166">JET_DbInfoSpaceAvailable</span><span class="sxs-lookup"><span data-stu-id="6c628-166">JET_DbInfoSpaceAvailable</span></span></p></td>
<td><p><span data-ttu-id="6c628-167"><em>pvresult</em> wird als DWORD interpretiert.</span><span class="sxs-lookup"><span data-stu-id="6c628-167"><em>pvResult</em> will be interpreted as a DWORD.</span></span> <span data-ttu-id="6c628-168">Dadurch wird der verfügbare Speicherplatz für die Datenbank auf Seiten zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6c628-168">This returns the available space for the database in pages.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c628-169">JET_DbInfoSpaceOwned</span><span class="sxs-lookup"><span data-stu-id="6c628-169">JET_DbInfoSpaceOwned</span></span></p></td>
<td><p><span data-ttu-id="6c628-170"><em>pvresult</em> wird als DWORD interpretiert.</span><span class="sxs-lookup"><span data-stu-id="6c628-170"><em>pvResult</em> will be interpreted as a DWORD.</span></span> <span data-ttu-id="6c628-171">Dadurch wird der im Besitz befindliche Speicherplatz für die Datenbank auf Seiten zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6c628-171">This returns the owned space for the database in pages.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c628-172">JET_DbInfoTransactions</span><span class="sxs-lookup"><span data-stu-id="6c628-172">JET_DbInfoTransactions</span></span></p></td>
<td><p><span data-ttu-id="6c628-173"><em>pvresult</em> wird als Long interpretiert.</span><span class="sxs-lookup"><span data-stu-id="6c628-173"><em>pvResult</em> will be interpreted as a long.</span></span> <span data-ttu-id="6c628-174">Dadurch wird ein Wert zurückgegeben, der größer ist als die maximale Ebene, auf die Transaktionen eingefügt werden können.</span><span class="sxs-lookup"><span data-stu-id="6c628-174">This will return one greater than the maximum level to which transactions can be nested.</span></span> <span data-ttu-id="6c628-175">Wenn <a href="gg294083(v=exchg.10).md">jetbegintransaction</a> (Schachtelungs Weise, d. h. in derselben Sitzung, ohne Commit oder Rollback) so oft wie dieser Wert aufgerufen wird, wird beim letzten Aufruf JET_errTransTooDeep von <a href="gg294083(v=exchg.10).md">jetbegintransaction</a>zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6c628-175">If <a href="gg294083(v=exchg.10).md">JetBeginTransaction</a> is called (in a nesting fashion, that is, on the same session, without a commit or rollback) as many times as this value, on the last call JET_errTransTooDeep will be returned from <a href="gg294083(v=exchg.10).md">JetBeginTransaction</a>.</span></span> <span data-ttu-id="6c628-176">Beachten Sie, dass der Wert in Windows 2000, Windows XP und Windows Server 2003 7 ist.</span><span class="sxs-lookup"><span data-stu-id="6c628-176">Note the value in Windows 2000, Windows XP, and Windows Server 2003 is 7.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c628-177">JET_DbInfoVersion</span><span class="sxs-lookup"><span data-stu-id="6c628-177">JET_DbInfoVersion</span></span></p></td>
<td><p><span data-ttu-id="6c628-178"><em>pvresult</em> wird als Long interpretiert.</span><span class="sxs-lookup"><span data-stu-id="6c628-178"><em>pvResult</em> will be interpreted as a long.</span></span> <span data-ttu-id="6c628-179">Dadurch wird die native Hauptversion der Datenbank-Engine zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6c628-179">This returns the database engine's native major version.</span></span> <span data-ttu-id="6c628-180">Dieser Wert ist 0x620 für Windows 2000, Windows XP und Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="6c628-180">This value is 0x620 for Windows 2000, Windows XP, and Windows Server 2003.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="6c628-181">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6c628-181">Return Value</span></span>

<span data-ttu-id="6c628-182">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="6c628-182">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="6c628-183">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="6c628-183">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6c628-184">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="6c628-184">Return code</span></span></p></th>
<th><p><span data-ttu-id="6c628-185">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6c628-185">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6c628-186">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="6c628-186">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="6c628-187">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="6c628-187">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c628-188">JET_errBufferTooSmall</span><span class="sxs-lookup"><span data-stu-id="6c628-188">JET_errBufferTooSmall</span></span></p></td>
<td><p><span data-ttu-id="6c628-189">Die Größe des in <em>cbmax</em> angegebenen Puffers war zu klein (oder nicht korrekt), um die gewünschten Informationen zu speichern.</span><span class="sxs-lookup"><span data-stu-id="6c628-189">The size of the buffer given in <em>cbMax</em> was too small (or not correct) to hold the desired information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c628-190">JET_errFeatureNotAvailable</span><span class="sxs-lookup"><span data-stu-id="6c628-190">JET_errFeatureNotAvailable</span></span></p></td>
<td><p><span data-ttu-id="6c628-191">Die angeforderte <em>infolevel</em> wurde JET_DbInfoIsam.</span><span class="sxs-lookup"><span data-stu-id="6c628-191">The <em>InfoLevel</em> requested was JET_DbInfoIsam.</span></span> <span data-ttu-id="6c628-192">Dieser Vorgang wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6c628-192">This is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c628-193">JET_errInvalidBufferSize</span><span class="sxs-lookup"><span data-stu-id="6c628-193">JET_errInvalidBufferSize</span></span></p></td>
<td><p><span data-ttu-id="6c628-194">Die Größe des in <em>cbmax</em> angegebenen Puffers war zu klein (oder nicht korrekt), um die gewünschten Informationen zu speichern.</span><span class="sxs-lookup"><span data-stu-id="6c628-194">The size of the buffer given in <em>cbMax</em> was too small (or not correct) to hold the desired information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c628-195">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="6c628-195">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="6c628-196">Einer der angegebenen Parameter enthielt einen unerwarteten Wert oder enthielt einen Wert, der nicht sinnvoll war, wenn er mit dem Wert eines anderen Parameters kombiniert wurde.</span><span class="sxs-lookup"><span data-stu-id="6c628-196">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="6c628-197">Dieser Fehler wird von <strong>jetgetdatabaseingefo</strong> zurückgegeben, wenn der bereitgestellte <a href="gg269248(v=exchg.10).md">JET_DBID</a> keine gültige (angefügte) Datenbank ist.</span><span class="sxs-lookup"><span data-stu-id="6c628-197">This error will be returned by <strong>JetGetDatabaseInfo</strong> when the <a href="gg269248(v=exchg.10).md">JET_DBID</a> provided is not a valid (attached) database.</span></span> <span data-ttu-id="6c628-198">Dieser Fehler wird von <a href="gg269239(v=exchg.10).md">jetgetdatabasefileinfo</a> und <strong>jetgetdatabaseinfo</strong> zurückgegeben, wenn ein angefordertes <em>infolevel</em> von dieser Version der Funktion nicht unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="6c628-198">This error will be returned by <a href="gg269239(v=exchg.10).md">JetGetDatabaseFileInfo</a> and <strong>JetGetDatabaseInfo</strong> when an <em>InfoLevel</em> requested is not supported by that version of the function.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6c628-199">Bei Erfolg werden die angeforderten Daten im Ausgabepuffer zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6c628-199">On success, the requested data will be returned in the output buffer.</span></span>

<span data-ttu-id="6c628-200">Bei einem Fehler befindet sich der Ausgabepuffer in einem nicht definierten Zustand.</span><span class="sxs-lookup"><span data-stu-id="6c628-200">On failure, the output buffer will be in an undefined state.</span></span>

#### <a name="requirements"></a><span data-ttu-id="6c628-201">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6c628-201">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6c628-202"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="6c628-202"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="6c628-203">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="6c628-203">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c628-204"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="6c628-204"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="6c628-205">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="6c628-205">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c628-206"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="6c628-206"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="6c628-207">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="6c628-207">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c628-208"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="6c628-208"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="6c628-209">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="6c628-209">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c628-210"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="6c628-210"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="6c628-211">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="6c628-211">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c628-212"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="6c628-212"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="6c628-213">Implementiert als <strong>jetgetdatabasanfow</strong> (Unicode) und <strong>jetgetdatabaseingefoa</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="6c628-213">Implemented as <strong>JetGetDatabaseInfoW</strong> (Unicode) and <strong>JetGetDatabaseInfoA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="6c628-214">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="6c628-214">See Also</span></span>

[<span data-ttu-id="6c628-215">JET_DBID</span><span class="sxs-lookup"><span data-stu-id="6c628-215">JET_DBID</span></span>](./jet-dbid.md)  
[<span data-ttu-id="6c628-216">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="6c628-216">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="6c628-217">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="6c628-217">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="6c628-218">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="6c628-218">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="6c628-219">JET_DBINFOMISC</span><span class="sxs-lookup"><span data-stu-id="6c628-219">JET_DBINFOMISC</span></span>](./jet-dbinfomisc-structure.md)  
[<span data-ttu-id="6c628-220">JET_DBINFOUPGRADE</span><span class="sxs-lookup"><span data-stu-id="6c628-220">JET_DBINFOUPGRADE</span></span>](./jet-dbinfoupgrade-structure.md)  
[<span data-ttu-id="6c628-221">Jetgetdatabasefileingefo</span><span class="sxs-lookup"><span data-stu-id="6c628-221">JetGetDatabaseFileInfo</span></span>](./jetgetdatabasefileinfo-function.md)
