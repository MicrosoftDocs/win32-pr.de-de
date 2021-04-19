---
description: 'Weitere Informationen zu: jetgetdatabasefileingefo-Funktion'
title: Jetgetdatabasefilinput Info-Funktion
TOCTitle: JetGetDatabaseFileInfo Function
ms:assetid: 457079d9-46c9-4da0-a35b-0c11fca7ed5b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269239(v=EXCHG.10)
ms:contentKeyID: 32765541
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetDatabaseFileInfo
- JetGetDatabaseFileInfoW
- JetGetDatabaseFileInfoA
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2ac94dd6f088a82c932aaca5b60ec16f49644f92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362778"
---
# <a name="jetgetdatabasefileinfo-function"></a><span data-ttu-id="f2c6c-103">Jetgetdatabasefilinput Info-Funktion</span><span class="sxs-lookup"><span data-stu-id="f2c6c-103">JetGetDatabaseFileInfo Function</span></span>


<span data-ttu-id="f2c6c-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="f2c6c-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetdatabasefileinfo-function"></a><span data-ttu-id="f2c6c-105">Jetgetdatabasefilinput Info-Funktion</span><span class="sxs-lookup"><span data-stu-id="f2c6c-105">JetGetDatabaseFileInfo Function</span></span>

<span data-ttu-id="f2c6c-106">Die **jetgetdatabasefileinfo** -Funktion Ruft verschiedene Arten von Informationen über die Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="f2c6c-106">The **JetGetDatabaseFileInfo** function retrieves various types of information about the database.</span></span> <span data-ttu-id="f2c6c-107">Diese API kann aufgerufen werden, während eine Datenbank angefügt oder Online ist (mit [jetgetdatabaseinfo](./jetgetdatabaseinfo-function.md)) oder wenn die Datenbank oder Datenbank-Engine offline ist (mit **jetgetdatabasefileinfo**).</span><span class="sxs-lookup"><span data-stu-id="f2c6c-107">This API can be called while a database is attached or online (with [JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md)) or while the database or database engine is offline (with **JetGetDatabaseFileInfo**).</span></span>

```cpp
    JET_ERR JET_API JetGetDatabaseFileInfo(
      __in          const tchar* szDatabaseName,
      __out         void* pvResult,
      __in          unsigned long cbMax,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a><span data-ttu-id="f2c6c-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="f2c6c-108">Parameters</span></span>

<span data-ttu-id="f2c6c-109">*szdatabasename*</span><span class="sxs-lookup"><span data-stu-id="f2c6c-109">*szDatabaseName*</span></span>

<span data-ttu-id="f2c6c-110">Der Pfad der Datenbank, aus der die Informationen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="f2c6c-110">The path of the database from which to retrieve the information.</span></span>

<span data-ttu-id="f2c6c-111">*pvresult*</span><span class="sxs-lookup"><span data-stu-id="f2c6c-111">*pvResult*</span></span>

<span data-ttu-id="f2c6c-112">Zeiger auf einen Puffer, der die angegebenen Informationen empfängt.</span><span class="sxs-lookup"><span data-stu-id="f2c6c-112">Pointer to a buffer that will receive the specified information.</span></span> <span data-ttu-id="f2c6c-113">Die Größe des Puffers in Bytes wird in *cbmax* übermittelt.</span><span class="sxs-lookup"><span data-stu-id="f2c6c-113">The size of the buffer, in bytes, is passed in *cbMax*.</span></span>

<span data-ttu-id="f2c6c-114">Wenn diese Funktion fehlschlägt, ist der Inhalt von *pvresult* nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="f2c6c-114">If this function fails, the contents of *pvResult* are undefined.</span></span>

<span data-ttu-id="f2c6c-115">Die in *pvresult* gespeicherten Informationen hängen von *infolevel* ab.</span><span class="sxs-lookup"><span data-stu-id="f2c6c-115">The information stored in *pvResult* depends on *InfoLevel*.</span></span>

<span data-ttu-id="f2c6c-116">*cbmax*</span><span class="sxs-lookup"><span data-stu-id="f2c6c-116">*cbMax*</span></span>

<span data-ttu-id="f2c6c-117">Die Größe (in Bytes) des Puffers, der in *pvresult* übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="f2c6c-117">The size, in bytes, of the buffer passed in *pvResult*.</span></span>

<span data-ttu-id="f2c6c-118">*Infolevel*</span><span class="sxs-lookup"><span data-stu-id="f2c6c-118">*InfoLevel*</span></span>

<span data-ttu-id="f2c6c-119">*Infolevel* gibt an, welche Art von Informationen über die angegebene Datenbank abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="f2c6c-119">*InfoLevel* specifies which type of information should be retrieved about the specified database.</span></span> <span data-ttu-id="f2c6c-120">Dies wirkt sich darauf aus, wie *pvresult* interpretiert wird.</span><span class="sxs-lookup"><span data-stu-id="f2c6c-120">It affects how *pvResult* is interpreted.</span></span> <span data-ttu-id="f2c6c-121">Einige *infolevel* -Objekte sind nur in der Offline Version (**jetgetdatabasefileinfo**) oder Online ([jetgetdatabaseinfo](./jetgetdatabaseinfo-function.md)) der API verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f2c6c-121">Some *InfoLevel* objects are available only in the offline (**JetGetDatabaseFileInfo**) or online ([JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md)) version of the API.</span></span>

<span data-ttu-id="f2c6c-122">Wenn der bereitgestellte *pvresult* -Puffer zu klein ist, werden je nach *infolevel* entweder JET_errInvalidBufferSize oder JET_errBufferTooSmall zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f2c6c-122">If the *pvResult* buffer provided is too small, either JET_errInvalidBufferSize or JET_errBufferTooSmall will be returned, depending on the *InfoLevel*.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f2c6c-123">Wert</span><span class="sxs-lookup"><span data-stu-id="f2c6c-123">Value</span></span></p></th>
<th><p><span data-ttu-id="f2c6c-124">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="f2c6c-124">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f2c6c-125">JET_DbInfoFilesize</span><span class="sxs-lookup"><span data-stu-id="f2c6c-125">JET_DbInfoFilesize</span></span></p></td>
<td><p><span data-ttu-id="f2c6c-126"><em>pvresult</em> wird als QWORD (8 Bytes) interpretiert.</span><span class="sxs-lookup"><span data-stu-id="f2c6c-126"><em>pvResult</em> will be interpreted as a QWORD (8 bytes).</span></span> <span data-ttu-id="f2c6c-127">Gibt die Größe der Datenbank in Bytes zurück.</span><span class="sxs-lookup"><span data-stu-id="f2c6c-127">Returns the size of the database in bytes.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2c6c-128">JET_DbInfoUpgrade</span><span class="sxs-lookup"><span data-stu-id="f2c6c-128">JET_DbInfoUpgrade</span></span></p></td>
<td><p><span data-ttu-id="f2c6c-129"><em>pvresult</em> wird als <a href="gg294114(v=exchg.10).md">JET_DBINFOUPGRADE</a>interpretiert.</span><span class="sxs-lookup"><span data-stu-id="f2c6c-129"><em>pvResult</em> will be interpreted as a <a href="gg294114(v=exchg.10).md">JET_DBINFOUPGRADE</a>.</span></span> <span data-ttu-id="f2c6c-130">Die <a href="gg294114(v=exchg.10).md">JET_DBINFOUPGRADE</a> Struktur wird mit Informationen aufgefüllt, die sich auf die angegebene Datenbank beziehen.</span><span class="sxs-lookup"><span data-stu-id="f2c6c-130">The <a href="gg294114(v=exchg.10).md">JET_DBINFOUPGRADE</a> structure will be populated with information pertaining to the specified database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2c6c-131">JET_DbInfoMisc</span><span class="sxs-lookup"><span data-stu-id="f2c6c-131">JET_DbInfoMisc</span></span></p></td>
<td><p><span data-ttu-id="f2c6c-132"><em>pvresult</em> wird als <a href="gg294147(v=exchg.10).md">JET_DBINFOMISC</a>interpretiert.</span><span class="sxs-lookup"><span data-stu-id="f2c6c-132"><em>pvResult</em> will be interpreted as a <a href="gg294147(v=exchg.10).md">JET_DBINFOMISC</a>.</span></span> <span data-ttu-id="f2c6c-133">Die <a href="gg294147(v=exchg.10).md">JET_DBINFOMISC</a> Struktur wird mit Informationen aufgefüllt, die sich auf die angegebene Datenbank beziehen.</span><span class="sxs-lookup"><span data-stu-id="f2c6c-133">The <a href="gg294147(v=exchg.10).md">JET_DBINFOMISC</a> structure will be populated with information pertaining to the specified database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2c6c-134">JET_DbInfoDBInUse</span><span class="sxs-lookup"><span data-stu-id="f2c6c-134">JET_DbInfoDBInUse</span></span></p></td>
<td><p><span data-ttu-id="f2c6c-135"><em>pvresult</em> wird als bool (4 Bytes) interpretiert.</span><span class="sxs-lookup"><span data-stu-id="f2c6c-135"><em>pvResult</em> will be interpreted as a BOOL (4 bytes).</span></span> <span data-ttu-id="f2c6c-136">Dadurch wird zurückgegeben, ob die Datenbank-Engine zurzeit über geöffnete oder angefügte Datenbanken verfügt.</span><span class="sxs-lookup"><span data-stu-id="f2c6c-136">This will return whether the database engine currently has any open or attached databases.</span></span></p>
<p><span data-ttu-id="f2c6c-137"><strong>Windows XP:  </strong> Dieser Wert wird in Windows XP eingeführt.</span><span class="sxs-lookup"><span data-stu-id="f2c6c-137"><strong>Windows XP:  </strong>This value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2c6c-138">JET_DbInfoPageSize</span><span class="sxs-lookup"><span data-stu-id="f2c6c-138">JET_DbInfoPageSize</span></span></p></td>
<td><p><span data-ttu-id="f2c6c-139"><em>pvresult</em> wird als Ganzzahl ohne Vorzeichen long interpretiert.</span><span class="sxs-lookup"><span data-stu-id="f2c6c-139"><em>pvResult</em> will be interpreted as a unsigned long.</span></span> <span data-ttu-id="f2c6c-140">Dadurch wird die Seitengröße der Datenbank in Bytes zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f2c6c-140">This will return the page size of the database in bytes.</span></span></p>
<p><span data-ttu-id="f2c6c-141"><strong>Windows XP:  </strong> Dieser Wert wird in Windows XP eingeführt.</span><span class="sxs-lookup"><span data-stu-id="f2c6c-141"><strong>Windows XP:  </strong>This value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2c6c-142">JET_DbInfoCp</span><span class="sxs-lookup"><span data-stu-id="f2c6c-142">JET_DbInfoCp</span></span></p></td>
<td><p><span data-ttu-id="f2c6c-143">Diese <em>infolevels</em> werden noch nicht unterstützt, und es werden Standardwerte zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f2c6c-143">These <em>InfoLevels</em> are not yet supported and return default values.</span></span> <span data-ttu-id="f2c6c-144">Verwenden Sie diese <em>infolevels</em>nicht.</span><span class="sxs-lookup"><span data-stu-id="f2c6c-144">Do not use these <em>InfoLevels</em>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2c6c-145">JET_DbInfoCountry</span><span class="sxs-lookup"><span data-stu-id="f2c6c-145">JET_DbInfoCountry</span></span></p></td>
<td><p><span data-ttu-id="f2c6c-146">Diese <em>infolevels</em> werden noch nicht unterstützt, und es werden Standardwerte zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f2c6c-146">These <em>InfoLevels</em> are not yet supported and return default values.</span></span> <span data-ttu-id="f2c6c-147">Verwenden Sie diese <em>infolevels</em>nicht.</span><span class="sxs-lookup"><span data-stu-id="f2c6c-147">Do not use these <em>InfoLevels</em>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2c6c-148">JET_DbInfoCollate</span><span class="sxs-lookup"><span data-stu-id="f2c6c-148">JET_DbInfoCollate</span></span></p></td>
<td><p><span data-ttu-id="f2c6c-149">Identisch mit JET_DbInfoCp.</span><span class="sxs-lookup"><span data-stu-id="f2c6c-149">Same as JET_DbInfoCp.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2c6c-150">JET_DbInfoIsam</span><span class="sxs-lookup"><span data-stu-id="f2c6c-150">JET_DbInfoIsam</span></span></p></td>
<td><p><span data-ttu-id="f2c6c-151">Diese <em>infolevels</em> sind veraltet und werden zurzeit nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f2c6c-151">These <em>InfoLevels</em> are deprecated and are not currently supported.</span></span> <span data-ttu-id="f2c6c-152">Verwenden Sie diese <em>infolevels</em>nicht.</span><span class="sxs-lookup"><span data-stu-id="f2c6c-152">Do not use these <em>InfoLevels</em>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2c6c-153">JET_DbInfoConnect</span><span class="sxs-lookup"><span data-stu-id="f2c6c-153">JET_DbInfoConnect</span></span></p></td>
<td><p><span data-ttu-id="f2c6c-154">Identisch mit JET_DbInfoIsam.</span><span class="sxs-lookup"><span data-stu-id="f2c6c-154">Same as JET_DbInfoIsam.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2c6c-155">JET_DbInfoFileType</span><span class="sxs-lookup"><span data-stu-id="f2c6c-155">JET_DbInfoFileType</span></span></p></td>
<td><p><span data-ttu-id="f2c6c-156"><strong>Windows Vista:  </strong> Dieser <em>infolevel</em> -Wert wird in Windows Vista eingeführt.</span><span class="sxs-lookup"><span data-stu-id="f2c6c-156"><strong>Windows Vista:  </strong>This <em>InfoLevel</em> value is introduced in Windows Vista.</span></span></p>
<p><span data-ttu-id="f2c6c-157"><em>pvresult</em> wird als Zeiger auf ein DWORD behandelt.</span><span class="sxs-lookup"><span data-stu-id="f2c6c-157"><em>pvResult</em> will be treated as a pointer to a DWORD.</span></span> <span data-ttu-id="f2c6c-158">Gibt einen Enumerationswert zurück, der angibt, welche Art von Datei das Modul als ist.</span><span class="sxs-lookup"><span data-stu-id="f2c6c-158">Returns an enumeration value, indicating what kind of file the engine considers this to be.</span></span> <span data-ttu-id="f2c6c-159">Dateitypen sind in der folgenden Tabelle aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="f2c6c-159">File types are listed in the following table.</span></span> <span data-ttu-id="f2c6c-160">Weitere Informationen zu diesen Dateitypen und deren Verwendung für die-Engine finden Sie unter <a href="gg294069(v=exchg.10).md">Extensible Storage Engine Files</a>.</span><span class="sxs-lookup"><span data-stu-id="f2c6c-160">For more information about these types of files and their usage to the engine, see <a href="gg294069(v=exchg.10).md">Extensible Storage Engine Files</a>.</span></span></p>
<div class="tableSection">
<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f2c6c-161">Wert</span><span class="sxs-lookup"><span data-stu-id="f2c6c-161">Value</span></span></p></th>
<th><p><span data-ttu-id="f2c6c-162">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="f2c6c-162">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f2c6c-163">JET_filetypeUnknown</span><span class="sxs-lookup"><span data-stu-id="f2c6c-163">JET_filetypeUnknown</span></span></p></td>
<td><p><span data-ttu-id="f2c6c-164">Der Dateityp ist unbekannt, oder es handelt sich nicht um einen ESE-Dateityp.</span><span class="sxs-lookup"><span data-stu-id="f2c6c-164">The type of file is unknown, or not an ESE file type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2c6c-165">JET_filetypeDatabase</span><span class="sxs-lookup"><span data-stu-id="f2c6c-165">JET_filetypeDatabase</span></span></p></td>
<td><p><span data-ttu-id="f2c6c-166">Bei der Datei handelt es sich um eine Datenbankdatei.</span><span class="sxs-lookup"><span data-stu-id="f2c6c-166">The file is a database file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2c6c-167">JET_filetypeLog</span><span class="sxs-lookup"><span data-stu-id="f2c6c-167">JET_filetypeLog</span></span></p></td>
<td><p><span data-ttu-id="f2c6c-168">Bei der Datei handelt es sich um eine Transaktionsprotokoll Datei.</span><span class="sxs-lookup"><span data-stu-id="f2c6c-168">The file is a transaction log file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2c6c-169">JET_filetypeCheckpoint</span><span class="sxs-lookup"><span data-stu-id="f2c6c-169">JET_filetypeCheckpoint</span></span></p></td>
<td><p><span data-ttu-id="f2c6c-170">Die Datei ist eine Prüf Punkt Datei.</span><span class="sxs-lookup"><span data-stu-id="f2c6c-170">The file is a checkpoint file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2c6c-171">JET_filetypeTempDatabase</span><span class="sxs-lookup"><span data-stu-id="f2c6c-171">JET_filetypeTempDatabase</span></span></p></td>
<td><p><span data-ttu-id="f2c6c-172">Die Datei ist eine temporäre Datenbankdatei.</span><span class="sxs-lookup"><span data-stu-id="f2c6c-172">The file is a temporary database file.</span></span></p></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="f2c6c-173">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f2c6c-173">Return Value</span></span>

<span data-ttu-id="f2c6c-174">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="f2c6c-174">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="f2c6c-175">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="f2c6c-175">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f2c6c-176">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="f2c6c-176">Return code</span></span></p></th>
<th><p><span data-ttu-id="f2c6c-177">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f2c6c-177">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f2c6c-178">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="f2c6c-178">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="f2c6c-179">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="f2c6c-179">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2c6c-180">JET_errFeatureNotAvailable</span><span class="sxs-lookup"><span data-stu-id="f2c6c-180">JET_errFeatureNotAvailable</span></span></p></td>
<td><p><span data-ttu-id="f2c6c-181">Die angeforderte <em>infolevel</em> wurde JET_DbInfoIsam.</span><span class="sxs-lookup"><span data-stu-id="f2c6c-181">The <em>InfoLevel</em> requested was JET_DbInfoIsam.</span></span> <span data-ttu-id="f2c6c-182">Dieser Vorgang wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f2c6c-182">This is not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2c6c-183">JET_errBufferTooSmall</span><span class="sxs-lookup"><span data-stu-id="f2c6c-183">JET_errBufferTooSmall</span></span></p></td>
<td><p><span data-ttu-id="f2c6c-184">Der in <em>cbmax</em> angegebene Puffer ist zu klein für die gewünschten Informationen.</span><span class="sxs-lookup"><span data-stu-id="f2c6c-184">The buffer that is given in <em>cbMax</em> is too small for the desired information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2c6c-185">JET_errInvalidBufferSize</span><span class="sxs-lookup"><span data-stu-id="f2c6c-185">JET_errInvalidBufferSize</span></span></p></td>
<td><p><span data-ttu-id="f2c6c-186">Der in <em>cbmax</em> angegebene Puffer weist nicht die richtige Größe für die gewünschten Informationen auf.</span><span class="sxs-lookup"><span data-stu-id="f2c6c-186">The buffer that is given in <em>cbMax</em> is not the correct size for the desired information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2c6c-187">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="f2c6c-187">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="f2c6c-188">Einer der Parameter, die bereitgestellt wurden, enthielt einen unerwarteten Wert, oder die Kombination mehrerer Parameterwerte hat ein unerwartetes Ergebnis zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f2c6c-188">One of the parameters that was provided contained an unexpected value, or the combination of several parameter values yielded an unexpected result.</span></span> <span data-ttu-id="f2c6c-189">Dieser Fehler wird von <a href="gg294076(v=exchg.10).md">jetgetdatabaseinfo</a> zurückgegeben, wenn es sich bei der bereitgestellten DBID nicht um eine gültige (angefügte) Datenbank handelt.</span><span class="sxs-lookup"><span data-stu-id="f2c6c-189">This error will be returned by <a href="gg294076(v=exchg.10).md">JetGetDatabaseInfo</a> when the DBID provided is not a valid (attached) database.</span></span> <span data-ttu-id="f2c6c-190">Dieser Fehler wird von <strong>jetgetdatabasefileinfo</strong> und <a href="gg294076(v=exchg.10).md">jetgetdatabaseinfo</a> zurückgegeben, wenn ein angefordertes <em>infolevel</em> von dieser Version der Funktion nicht unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="f2c6c-190">This error will be returned by <strong>JetGetDatabaseFileInfo</strong> and <a href="gg294076(v=exchg.10).md">JetGetDatabaseInfo</a> when an <em>InfoLevel</em> requested is not supported by that version of the function.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f2c6c-191">Wenn diese Funktion erfolgreich ausgeführt wird, werden die angeforderten Daten im Ausgabepuffer zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f2c6c-191">If this function succeeds, the requested data will be returned in the output buffer.</span></span>

<span data-ttu-id="f2c6c-192">Wenn diese Funktion fehlschlägt, befindet sich der Ausgabepuffer in einem nicht definierten Zustand.</span><span class="sxs-lookup"><span data-stu-id="f2c6c-192">If this function fails, the output buffer will be in an undefined state.</span></span>

#### <a name="requirements"></a><span data-ttu-id="f2c6c-193">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f2c6c-193">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f2c6c-194"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="f2c6c-194"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="f2c6c-195">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="f2c6c-195">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2c6c-196"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="f2c6c-196"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="f2c6c-197">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="f2c6c-197">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2c6c-198"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="f2c6c-198"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="f2c6c-199">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="f2c6c-199">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2c6c-200"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="f2c6c-200"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="f2c6c-201">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="f2c6c-201">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2c6c-202"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="f2c6c-202"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="f2c6c-203">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="f2c6c-203">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2c6c-204"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="f2c6c-204"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="f2c6c-205">Implementiert als <strong>jetgetdatabasefileingefow</strong> (Unicode) und <strong>jetgetdatabasefileingefoa</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="f2c6c-205">Implemented as <strong>JetGetDatabaseFileInfoW</strong> (Unicode) and <strong>JetGetDatabaseFileInfoA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="f2c6c-206">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="f2c6c-206">See Also</span></span>

[<span data-ttu-id="f2c6c-207">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="f2c6c-207">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="f2c6c-208">JET_DBINFOMISC</span><span class="sxs-lookup"><span data-stu-id="f2c6c-208">JET_DBINFOMISC</span></span>](./jet-dbinfomisc-structure.md)  
[<span data-ttu-id="f2c6c-209">JET_DBINFOUPGRADE</span><span class="sxs-lookup"><span data-stu-id="f2c6c-209">JET_DBINFOUPGRADE</span></span>](./jet-dbinfoupgrade-structure.md)  
[<span data-ttu-id="f2c6c-210">Jetgetdatabaseingefo</span><span class="sxs-lookup"><span data-stu-id="f2c6c-210">JetGetDatabaseInfo</span></span>](./jetgetdatabaseinfo-function.md)
