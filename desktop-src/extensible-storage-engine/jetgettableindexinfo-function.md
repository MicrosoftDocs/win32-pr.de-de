---
description: 'Weitere Informationen zu: jetgettableindexinfo-Funktion'
title: JetGetTableIndexInfo-Funktion
TOCTitle: JetGetTableIndexInfo Function
ms:assetid: d250d254-2b10-4fe7-bbb1-72bb967f22dd
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294102(v=EXCHG.10)
ms:contentKeyID: 32765717
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetTableIndexInfoW
- JetGetTableIndexInfoA
- JetGetTableIndexInfo
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 904391218fbd073cd273655ce74fdec116b6a22e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218588"
---
# <a name="jetgettableindexinfo-function"></a><span data-ttu-id="608d5-103">JetGetTableIndexInfo-Funktion</span><span class="sxs-lookup"><span data-stu-id="608d5-103">JetGetTableIndexInfo Function</span></span>


<span data-ttu-id="608d5-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="608d5-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgettableindexinfo-function"></a><span data-ttu-id="608d5-105">JetGetTableIndexInfo-Funktion</span><span class="sxs-lookup"><span data-stu-id="608d5-105">JetGetTableIndexInfo Function</span></span>

<span data-ttu-id="608d5-106">Die **jetgettableindexinfo** -Funktion Ruft Informationen zu einem Index ab.</span><span class="sxs-lookup"><span data-stu-id="608d5-106">The **JetGetTableIndexInfo** function retrieves information about an index.</span></span>

```cpp
    JET_ERR JET_API JetGetTableIndexInfo(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          const tchar* szIndexName,
      __out         void* pvResult,
      __in          unsigned long cbResult,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a><span data-ttu-id="608d5-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="608d5-107">Parameters</span></span>

<span data-ttu-id="608d5-108">*-sid*</span><span class="sxs-lookup"><span data-stu-id="608d5-108">*sesid*</span></span>

<span data-ttu-id="608d5-109">Der für den API-Befehl zu verwendende Daten Bank Sitzungs Kontext.</span><span class="sxs-lookup"><span data-stu-id="608d5-109">The database session context to use for the API call.</span></span>

<span data-ttu-id="608d5-110">*TableID*</span><span class="sxs-lookup"><span data-stu-id="608d5-110">*tableid*</span></span>

<span data-ttu-id="608d5-111">Die Datenbanktabelle, die den Index enthält, der die erforderlichen Informationen enthält.</span><span class="sxs-lookup"><span data-stu-id="608d5-111">The database table that contains the index that holds the needed information.</span></span>

<span data-ttu-id="608d5-112">*szindexname*</span><span class="sxs-lookup"><span data-stu-id="608d5-112">*szIndexName*</span></span>

<span data-ttu-id="608d5-113">Der Name des Indexes, der Informationen enthält, die abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="608d5-113">The name of the index that contains information that will be retrieved.</span></span>

<span data-ttu-id="608d5-114">*pvresult*</span><span class="sxs-lookup"><span data-stu-id="608d5-114">*pvResult*</span></span>

<span data-ttu-id="608d5-115">Zeiger auf einen Puffer, der die Informationen empfängt.</span><span class="sxs-lookup"><span data-stu-id="608d5-115">Pointer to a buffer which will receive the information.</span></span> <span data-ttu-id="608d5-116">Der Puffer muss so ausgerichtet werden, dass er den erforderlichen Typ enthält.</span><span class="sxs-lookup"><span data-stu-id="608d5-116">The buffer should be aligned to hold the type required.</span></span> <span data-ttu-id="608d5-117">Der Typ des Puffers ist abhängig vom *infolevel* -Parameter.</span><span class="sxs-lookup"><span data-stu-id="608d5-117">The type of the buffer is dependent on the *InfoLevel* parameter.</span></span>

<span data-ttu-id="608d5-118">*cbresult*</span><span class="sxs-lookup"><span data-stu-id="608d5-118">*cbResult*</span></span>

<span data-ttu-id="608d5-119">Die Größe (in Bytes) des Puffers, der im *pvresult* -Parameter übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="608d5-119">The size, in bytes, of the buffer passed in the *pvResult* parameter.</span></span>

<span data-ttu-id="608d5-120">*Infolevel*</span><span class="sxs-lookup"><span data-stu-id="608d5-120">*InfoLevel*</span></span>

<span data-ttu-id="608d5-121">Gibt an, welche Informationen in *pvresult* gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="608d5-121">Specifies which information will be stored in *pvResult*.</span></span> <span data-ttu-id="608d5-122">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="608d5-122">The valid values are:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="608d5-123">Wert</span><span class="sxs-lookup"><span data-stu-id="608d5-123">Value</span></span></p></th>
<th><p><span data-ttu-id="608d5-124">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="608d5-124">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="608d5-125">JET_IdxInfo</span><span class="sxs-lookup"><span data-stu-id="608d5-125">JET_IdxInfo</span></span></p></td>
<td><p><span data-ttu-id="608d5-126"><em>pvresult</em> wird als <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> Struktur interpretiert.</span><span class="sxs-lookup"><span data-stu-id="608d5-126"><em>pvResult</em> is interpreted as a <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> structure.</span></span> <span data-ttu-id="608d5-127">Bei Erfolg empfängt die <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> Strukturinformationen über den Index.</span><span class="sxs-lookup"><span data-stu-id="608d5-127">On success, the <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> structure receives information about the index.</span></span> <span data-ttu-id="608d5-128">Bei einem Fehler ist der Inhalt von <em>pvbuffer</em> nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="608d5-128">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="608d5-129">JET_IdxInfoLCID</span><span class="sxs-lookup"><span data-stu-id="608d5-129">JET_IdxInfoLCID</span></span></p></td>
<td><p><span data-ttu-id="608d5-130"><em>pvresult</em> wird als LCID interpretiert.</span><span class="sxs-lookup"><span data-stu-id="608d5-130"><em>pvResult</em> is interpreted as an LCID.</span></span> <span data-ttu-id="608d5-131">Bei Erfolg enthält die LCID den Gebiets Schema Bezeichner des Indexes.</span><span class="sxs-lookup"><span data-stu-id="608d5-131">On success, the LCID holds the Locale Identifier of the index.</span></span> <span data-ttu-id="608d5-132">Bei einem Fehler ist der Inhalt von <em>pvbuffer</em> nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="608d5-132">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="608d5-133">JET_IdxInfoList</span><span class="sxs-lookup"><span data-stu-id="608d5-133">JET_IdxInfoList</span></span></p></td>
<td><p><span data-ttu-id="608d5-134"><em>pvresult</em> wird als <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> Struktur interpretiert.</span><span class="sxs-lookup"><span data-stu-id="608d5-134"><em>pvResult</em> is interpreted as a <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> structure.</span></span> <span data-ttu-id="608d5-135">Bei Erfolg empfängt die <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> Strukturinformationen über den Index.</span><span class="sxs-lookup"><span data-stu-id="608d5-135">On success, the <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> structure receives information about the index.</span></span> <span data-ttu-id="608d5-136">Bei einem Fehler ist der Inhalt von <em>pvbuffer</em> nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="608d5-136">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="608d5-137">JET_IdxInfoOLC</span><span class="sxs-lookup"><span data-stu-id="608d5-137">JET_IdxInfoOLC</span></span></p></td>
<td><p><span data-ttu-id="608d5-138">JET_IdxInfoOLC ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="608d5-138">JET_IdxInfoOLC is obsolete.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="608d5-139">JET_IdxInfoResetOLC</span><span class="sxs-lookup"><span data-stu-id="608d5-139">JET_IdxInfoResetOLC</span></span></p></td>
<td><p><span data-ttu-id="608d5-140">JET_IdxInfoResetOLC ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="608d5-140">JET_IdxInfoResetOLC is obsolete.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="608d5-141">JET_IdxInfoSpaceAlloc</span><span class="sxs-lookup"><span data-stu-id="608d5-141">JET_IdxInfoSpaceAlloc</span></span></p></td>
<td><p><span data-ttu-id="608d5-142"><em>pvresult</em> wird als ULONG interpretiert.</span><span class="sxs-lookup"><span data-stu-id="608d5-142"><em>pvResult</em> is interpreted as a ULONG.</span></span> <span data-ttu-id="608d5-143">Bei Erfolg enthält der ULONG die Speicherplatz Verwendung des Indexes.</span><span class="sxs-lookup"><span data-stu-id="608d5-143">On success, the ULONG holds the space usage of the index.</span></span> <span data-ttu-id="608d5-144">Bei einem Fehler ist der Inhalt von <em>pvbuffer</em> nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="608d5-144">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="608d5-145">JET_IdxInfoSysTabCursor</span><span class="sxs-lookup"><span data-stu-id="608d5-145">JET_IdxInfoSysTabCursor</span></span></p></td>
<td><p><span data-ttu-id="608d5-146">JET_IdxInfoSysTabCursor ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="608d5-146">JET_IdxInfoSysTabCursor is obsolete.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="608d5-147">JET_IdxInfoLangid</span><span class="sxs-lookup"><span data-stu-id="608d5-147">JET_IdxInfoLangid</span></span></p></td>
<td><p><span data-ttu-id="608d5-148">JET_IdxInfoLangid ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="608d5-148">JET_IdxInfoLangid is deprecated.</span></span> <span data-ttu-id="608d5-149">Verwenden Sie stattdessen JET_IdxInfoLCID und das-Makro <a href="/windows/win32/api/winnt/nf-winnt-langidfromlcid">langidfromlcid</a> .</span><span class="sxs-lookup"><span data-stu-id="608d5-149">Use JET_IdxInfoLCID instead, and the <a href="/windows/win32/api/winnt/nf-winnt-langidfromlcid">LANGIDFROMLCID</a> macro instead.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="608d5-150">JET_IdxInfoCount</span><span class="sxs-lookup"><span data-stu-id="608d5-150">JET_IdxInfoCount</span></span></p></td>
<td><p><span data-ttu-id="608d5-151"><em>pvresult</em> wird als ULONG interpretiert.</span><span class="sxs-lookup"><span data-stu-id="608d5-151"><em>pvResult</em> is interpreted as a ULONG.</span></span> <span data-ttu-id="608d5-152">Bei Erfolg enthält der ULONG die Anzahl der Indizes für die angegebene Tabelle.</span><span class="sxs-lookup"><span data-stu-id="608d5-152">On success, the ULONG holds the count of indexes on the specified table.</span></span> <span data-ttu-id="608d5-153"><em>szindexname</em> wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="608d5-153"><em>szIndexName</em> is ignored.</span></span> <span data-ttu-id="608d5-154">Bei einem Fehler ist der Inhalt von <em>pvbuffer</em> nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="608d5-154">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="608d5-155">JET_IdxInfoVarSegMac</span><span class="sxs-lookup"><span data-stu-id="608d5-155">JET_IdxInfoVarSegMac</span></span></p></td>
<td><p><span data-ttu-id="608d5-156"><em>pvresult</em> wird als ushort interpretiert.</span><span class="sxs-lookup"><span data-stu-id="608d5-156"><em>pvResult</em> is interpreted as a USHORT.</span></span> <span data-ttu-id="608d5-157">Bei Erfolg enthält der ushort den Wert von <em>cbvarsegmac</em> , der beim Erstellen des Indexes verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="608d5-157">On success, the USHORT holds the value of <em>cbVarSegMac</em> used when the index was created.</span></span> <span data-ttu-id="608d5-158">Unter <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> finden Sie eine Beschreibung von <em>cbvarsegmac</em>.</span><span class="sxs-lookup"><span data-stu-id="608d5-158">See <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> for a description of <em>cbVarSegMac</em>.</span></span> <span data-ttu-id="608d5-159">Bei einem Fehler ist der Inhalt von <em>pvbuffer</em> nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="608d5-159">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="608d5-160">JET_IdxInfoIndexId</span><span class="sxs-lookup"><span data-stu-id="608d5-160">JET_IdxInfoIndexId</span></span></p></td>
<td><p><span data-ttu-id="608d5-161"><em>pvresult</em> wird als <a href="gg269327(v=exchg.10).md">JET_INDEXID</a>interpretiert.</span><span class="sxs-lookup"><span data-stu-id="608d5-161"><em>pvResult</em> is interpreted as a <a href="gg269327(v=exchg.10).md">JET_INDEXID</a>.</span></span> <span data-ttu-id="608d5-162">Bei Erfolg empfängt die <a href="gg269327(v=exchg.10).md">JET_INDEXID</a> Strukturinformationen über den Index.</span><span class="sxs-lookup"><span data-stu-id="608d5-162">On success, the <a href="gg269327(v=exchg.10).md">JET_INDEXID</a> structure receives information about the index.</span></span> <span data-ttu-id="608d5-163">Bei einem Fehler ist der Inhalt von <em>pvbuffer</em> nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="608d5-163">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="608d5-164">JET_IdxInfoKeyMost</span><span class="sxs-lookup"><span data-stu-id="608d5-164">JET_IdxInfoKeyMost</span></span></p></td>
<td><p><span data-ttu-id="608d5-165"><em>pvresult</em> wird als ushort interpretiert.</span><span class="sxs-lookup"><span data-stu-id="608d5-165"><em>pvResult</em> is interpreted as a USHORT.</span></span> <span data-ttu-id="608d5-166">Bei Erfolg enthält der ushort den Wert von cbkeymost, der beim Erstellen des Indexes verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="608d5-166">On success, the USHORT holds the value of cbKeyMost used when the index was created.</span></span> <span data-ttu-id="608d5-167">Eine Beschreibung von cbkeymost finden Sie in der <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> -Struktur.</span><span class="sxs-lookup"><span data-stu-id="608d5-167">See the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure for a description of cbKeyMost.</span></span> <span data-ttu-id="608d5-168">Bei einem Fehler ist der Inhalt von <em>pvbuffer</em> nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="608d5-168">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="608d5-169">JET_IdxInfoCreateIndex</span><span class="sxs-lookup"><span data-stu-id="608d5-169">JET_IdxInfoCreateIndex</span></span></p></td>
<td><p><span data-ttu-id="608d5-170"><em>pvresult</em> wird als <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> Struktur interpretiert.</span><span class="sxs-lookup"><span data-stu-id="608d5-170"><em>pvResult</em> is interpreted as a <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure.</span></span> <span data-ttu-id="608d5-171">Bei einem Fehler ist der Inhalt von <em>pvbuffer</em> nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="608d5-171">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p>
<p><span data-ttu-id="608d5-172"><strong>Windows 7:  </strong> JET_IdxInfoCreateIndex wurde in Windows 7 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="608d5-172"><strong>Windows 7:  </strong>JET_IdxInfoCreateIndex is introduced in Windows 7.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="608d5-173">JET_IdxInfoCreateIndex2</span><span class="sxs-lookup"><span data-stu-id="608d5-173">JET_IdxInfoCreateIndex2</span></span></p></td>
<td><p><span data-ttu-id="608d5-174"><em>pvresult</em> wird als <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> Struktur interpretiert.</span><span class="sxs-lookup"><span data-stu-id="608d5-174"><em>pvResult</em> is interpreted as a <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure.</span></span> <span data-ttu-id="608d5-175">Bei einem Fehler ist der Inhalt von <em>pvbuffer</em> nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="608d5-175">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p>
<p><span data-ttu-id="608d5-176"><strong>Windows 7:  </strong> JET_IdxInfoCreateIndex2 wurde in Windows 7 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="608d5-176"><strong>Windows 7:  </strong>JET_IdxInfoCreateIndex2 is introduced in Windows 7.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="608d5-177">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="608d5-177">Return Value</span></span>

<span data-ttu-id="608d5-178">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="608d5-178">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="608d5-179">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="608d5-179">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="608d5-180">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="608d5-180">Return code</span></span></p></th>
<th><p><span data-ttu-id="608d5-181">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="608d5-181">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="608d5-182">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="608d5-182">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="608d5-183">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="608d5-183">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="608d5-184">JET_errIndexNotFound</span><span class="sxs-lookup"><span data-stu-id="608d5-184">JET_errIndexNotFound</span></span></p></td>
<td><p><span data-ttu-id="608d5-185">Der angegebene Index wurde in der angegebenen Tabelle nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="608d5-185">The specified index cannot be found in the specified table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="608d5-186">JET_wrnBufferTruncated</span><span class="sxs-lookup"><span data-stu-id="608d5-186">JET_wrnBufferTruncated</span></span></p></td>
<td><p><span data-ttu-id="608d5-187">Der als <em>pvresult</em> weiter gegebene Puffer war zu klein.</span><span class="sxs-lookup"><span data-stu-id="608d5-187">The buffer passed in as <em>pvResult</em> was too small.</span></span> <span data-ttu-id="608d5-188">Der Inhalt des Puffers ist nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="608d5-188">The contents of the buffer are undefined.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="608d5-189">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="608d5-189">Remarks</span></span>

<span data-ttu-id="608d5-190">[Jetgetindexinfo](./jetgetindexinfo-function.md) und **jetgettableindexinfo** rufen identische Informationen zu einem Index ab.</span><span class="sxs-lookup"><span data-stu-id="608d5-190">[JetGetIndexInfo](./jetgetindexinfo-function.md) and **JetGetTableIndexInfo** retrieve identical information about an index.</span></span> <span data-ttu-id="608d5-191">Der Unterschied besteht darin, wie die Tabelle angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="608d5-191">The difference is in how the table is specified.</span></span> <span data-ttu-id="608d5-192">[Jetgetindexinfo](./jetgetindexinfo-function.md) erwartet eine Datenbank (*DBID*) und den Namen einer Tabelle (*sztablename*), während **jetgettableindexinfo** einen Tabellen Bezeichner (*TableID*) erwartet.</span><span class="sxs-lookup"><span data-stu-id="608d5-192">[JetGetIndexInfo](./jetgetindexinfo-function.md) expects a database (*dbid*) and name of a table (*szTableName*), while **JetGetTableIndexInfo** expects a table identifier (*tableid*).</span></span>

#### <a name="requirements"></a><span data-ttu-id="608d5-193">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="608d5-193">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="608d5-194"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="608d5-194"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="608d5-195">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="608d5-195">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="608d5-196"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="608d5-196"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="608d5-197">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="608d5-197">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="608d5-198"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="608d5-198"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="608d5-199">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="608d5-199">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="608d5-200"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="608d5-200"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="608d5-201">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="608d5-201">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="608d5-202"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="608d5-202"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="608d5-203">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="608d5-203">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="608d5-204"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="608d5-204"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="608d5-205">Implementiert als <strong>jetgettableindexinfow</strong> (Unicode) und <strong>jetgettableindexinfoa</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="608d5-205">Implemented as <strong>JetGetTableIndexInfoW</strong> (Unicode) and <strong>JetGetTableIndexInfoA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="608d5-206">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="608d5-206">See Also</span></span>

[<span data-ttu-id="608d5-207">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="608d5-207">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="608d5-208">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="608d5-208">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="608d5-209">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="608d5-209">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="608d5-210">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="608d5-210">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="608d5-211">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="608d5-211">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="608d5-212">JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="608d5-212">JET_INDEXCREATE</span></span>](./jet-indexcreate-structure.md)  
[<span data-ttu-id="608d5-213">JET_INDEXID</span><span class="sxs-lookup"><span data-stu-id="608d5-213">JET_INDEXID</span></span>](./jet-indexid-structure.md)  
[<span data-ttu-id="608d5-214">Jetgetindexinfo</span><span class="sxs-lookup"><span data-stu-id="608d5-214">JetGetIndexInfo</span></span>](./jetgetindexinfo-function.md)
