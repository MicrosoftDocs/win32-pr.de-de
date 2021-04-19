---
description: 'Weitere Informationen zu: jetgetindexinfo-Funktion'
title: JetGetIndexInfo-Funktion
TOCTitle: JetGetIndexInfo Function
ms:assetid: c6235281-e208-4966-bc66-ec1ab27333c0
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294084(v=EXCHG.10)
ms:contentKeyID: 32765699
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetIndexInfoW
- JetGetIndexInfoA
- JetGetIndexInfo
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4a0fd506390ba9f228c115d0b9142baffdbe1587
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362611"
---
# <a name="jetgetindexinfo-function"></a><span data-ttu-id="82d51-103">JetGetIndexInfo-Funktion</span><span class="sxs-lookup"><span data-stu-id="82d51-103">JetGetIndexInfo Function</span></span>


<span data-ttu-id="82d51-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="82d51-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetindexinfo-function"></a><span data-ttu-id="82d51-105">JetGetIndexInfo-Funktion</span><span class="sxs-lookup"><span data-stu-id="82d51-105">JetGetIndexInfo Function</span></span>

<span data-ttu-id="82d51-106">Die **jetgetindexinfo** -Funktion Ruft Informationen zu einem Index ab.</span><span class="sxs-lookup"><span data-stu-id="82d51-106">The **JetGetIndexInfo** function retrieves information about an index.</span></span>

```cpp
    JET_ERR JET_API JetGetIndexInfo(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          const tchar* szTableName,
      __in          const tchar* szIndexName,
      __out         void* pvResult,
      __in          unsigned long cbResult,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a><span data-ttu-id="82d51-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="82d51-107">Parameters</span></span>

<span data-ttu-id="82d51-108">*-sid*</span><span class="sxs-lookup"><span data-stu-id="82d51-108">*sesid*</span></span>

<span data-ttu-id="82d51-109">Der für den API-Befehl zu verwendende Daten Bank Sitzungs Kontext.</span><span class="sxs-lookup"><span data-stu-id="82d51-109">The database session context to use for the API call.</span></span>

<span data-ttu-id="82d51-110">*DBID*</span><span class="sxs-lookup"><span data-stu-id="82d51-110">*dbid*</span></span>

<span data-ttu-id="82d51-111">Der für den API-Befehl zu verwendende Daten Bank Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="82d51-111">The database identifier to use for the API call.</span></span>

<span data-ttu-id="82d51-112">*sztablename*</span><span class="sxs-lookup"><span data-stu-id="82d51-112">*szTableName*</span></span>

<span data-ttu-id="82d51-113">Der Name der Tabelle mit dem Index, der die abzurufenden Informationen enthält.</span><span class="sxs-lookup"><span data-stu-id="82d51-113">The name of the table containing the index with the information to retrieve.</span></span>

<span data-ttu-id="82d51-114">*szindexname*</span><span class="sxs-lookup"><span data-stu-id="82d51-114">*szIndexName*</span></span>

<span data-ttu-id="82d51-115">Der Name des Indexes mit den abzurufenden Informationen.</span><span class="sxs-lookup"><span data-stu-id="82d51-115">The name of the index with the information to retrieve.</span></span>

<span data-ttu-id="82d51-116">*pvresult*</span><span class="sxs-lookup"><span data-stu-id="82d51-116">*pvResult*</span></span>

<span data-ttu-id="82d51-117">Zeiger auf einen Puffer, der die gewünschten Informationen empfängt.</span><span class="sxs-lookup"><span data-stu-id="82d51-117">Pointer to a buffer that will receive the desired information.</span></span> <span data-ttu-id="82d51-118">Der Puffer muss so ausgerichtet werden, dass er den erforderlichen Typ enthält.</span><span class="sxs-lookup"><span data-stu-id="82d51-118">The buffer should be aligned to hold the type required.</span></span> <span data-ttu-id="82d51-119">Der Typ des Puffers ist abhängig vom *infolevel* -Parameter.</span><span class="sxs-lookup"><span data-stu-id="82d51-119">The type of the buffer is dependent on the *InfoLevel* parameter.</span></span>

<span data-ttu-id="82d51-120">*cbresult*</span><span class="sxs-lookup"><span data-stu-id="82d51-120">*cbResult*</span></span>

<span data-ttu-id="82d51-121">Die Größe (in Bytes) des Puffers, der als *pvresult* übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="82d51-121">The size, in bytes, of the buffer passed as *pvResult*.</span></span>

<span data-ttu-id="82d51-122">*Infolevel*</span><span class="sxs-lookup"><span data-stu-id="82d51-122">*InfoLevel*</span></span>

<span data-ttu-id="82d51-123">Die Informationen, die in *pvresult* gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="82d51-123">The information that will be stored in *pvResult*.</span></span> <span data-ttu-id="82d51-124">Die folgenden Optionen können für diesen Parameter verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="82d51-124">The following options can be used for this parameter.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="82d51-125">Wert</span><span class="sxs-lookup"><span data-stu-id="82d51-125">Value</span></span></p></th>
<th><p><span data-ttu-id="82d51-126">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="82d51-126">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="82d51-127">JET_IdxInfo</span><span class="sxs-lookup"><span data-stu-id="82d51-127">JET_IdxInfo</span></span></p></td>
<td><p><span data-ttu-id="82d51-128"><em>pvresult</em> wird als <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> Struktur interpretiert.</span><span class="sxs-lookup"><span data-stu-id="82d51-128"><em>pvResult</em> is interpreted as a <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> structure.</span></span> <span data-ttu-id="82d51-129">Bei Erfolg empfängt die <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> Strukturinformationen über den Index.</span><span class="sxs-lookup"><span data-stu-id="82d51-129">On success, the <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> structure receives information about the index.</span></span> <span data-ttu-id="82d51-130">Bei einem Fehler ist der Inhalt von <em>pvbuffer</em> nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="82d51-130">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="82d51-131">JET_IdxInfoCount</span><span class="sxs-lookup"><span data-stu-id="82d51-131">JET_IdxInfoCount</span></span></p></td>
<td><p><span data-ttu-id="82d51-132"><em>pvresult</em> wird als ULONG interpretiert.</span><span class="sxs-lookup"><span data-stu-id="82d51-132"><em>pvResult</em> is interpreted as a ULONG.</span></span> <span data-ttu-id="82d51-133">Bei Erfolg enthält der ULONG die Anzahl der Indizes für die angegebene Tabelle.</span><span class="sxs-lookup"><span data-stu-id="82d51-133">On success, the ULONG holds the count of indexes on the specified table.</span></span> <span data-ttu-id="82d51-134"><em>szindexname</em> wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="82d51-134"><em>szIndexName</em> is ignored.</span></span> <span data-ttu-id="82d51-135">Bei einem Fehler ist der Inhalt von <em>pvbuffer</em> nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="82d51-135">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="82d51-136">JET_IdxInfoIndexId</span><span class="sxs-lookup"><span data-stu-id="82d51-136">JET_IdxInfoIndexId</span></span></p></td>
<td><p><span data-ttu-id="82d51-137"><em>pvresult</em> wird als <a href="gg269327(v=exchg.10).md">JET_INDEXID</a>interpretiert.</span><span class="sxs-lookup"><span data-stu-id="82d51-137"><em>pvResult</em> is interpreted as a <a href="gg269327(v=exchg.10).md">JET_INDEXID</a>.</span></span> <span data-ttu-id="82d51-138">Bei Erfolg empfängt die <a href="gg269327(v=exchg.10).md">JET_INDEXID</a> Strukturinformationen über den Index.</span><span class="sxs-lookup"><span data-stu-id="82d51-138">On success, the <a href="gg269327(v=exchg.10).md">JET_INDEXID</a> structure receives information about the index.</span></span> <span data-ttu-id="82d51-139">Bei einem Fehler ist der Inhalt von <em>pvbuffer</em> nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="82d51-139">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="82d51-140">JET_IdxInfoLangid</span><span class="sxs-lookup"><span data-stu-id="82d51-140">JET_IdxInfoLangid</span></span></p></td>
<td><p><span data-ttu-id="82d51-141">JET_IdxInfoLangid ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="82d51-141">JET_IdxInfoLangid is deprecated.</span></span> <span data-ttu-id="82d51-142">Verwenden Sie stattdessen JET_IdxInfoLCID und das <a href="/windows/win32/api/winnt/nf-winnt-langidfromlcid">langidfromlcid</a> -Makro.</span><span class="sxs-lookup"><span data-stu-id="82d51-142">Use JET_IdxInfoLCID and the <a href="/windows/win32/api/winnt/nf-winnt-langidfromlcid">LANGIDFROMLCID</a> macro instead.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="82d51-143">JET_IdxInfoLCID</span><span class="sxs-lookup"><span data-stu-id="82d51-143">JET_IdxInfoLCID</span></span></p></td>
<td><p><span data-ttu-id="82d51-144"><em>pvresult</em> wird als LCID interpretiert.</span><span class="sxs-lookup"><span data-stu-id="82d51-144"><em>pvResult</em> is interpreted as an LCID.</span></span> <span data-ttu-id="82d51-145">Bei Erfolg enthält die LCID den Gebiets Schema Bezeichner des Indexes.</span><span class="sxs-lookup"><span data-stu-id="82d51-145">On success, the LCID holds the Locale Identifier of the index.</span></span> <span data-ttu-id="82d51-146">Bei einem Fehler ist der Inhalt von <em>pvbuffer</em> nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="82d51-146">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p>
<p><span data-ttu-id="82d51-147"><strong>Windows XP:  </strong> JET_IdxInfoLCID wird in Windows XP eingeführt.</span><span class="sxs-lookup"><span data-stu-id="82d51-147"><strong>Windows XP:  </strong>JET_IdxInfoLCID is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="82d51-148">JET_IdxInfoList</span><span class="sxs-lookup"><span data-stu-id="82d51-148">JET_IdxInfoList</span></span></p></td>
<td><p><span data-ttu-id="82d51-149"><em>pvresult</em> wird als <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> Struktur interpretiert.</span><span class="sxs-lookup"><span data-stu-id="82d51-149"><em>pvResult</em> is interpreted as a <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> structure.</span></span> <span data-ttu-id="82d51-150">Bei Erfolg empfängt die <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> Strukturinformationen über den Index.</span><span class="sxs-lookup"><span data-stu-id="82d51-150">On success, the <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> structure receives information about the index.</span></span> <span data-ttu-id="82d51-151">Bei einem Fehler ist der Inhalt von <em>pvbuffer</em> nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="82d51-151">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="82d51-152">JET_IdxInfoOLC</span><span class="sxs-lookup"><span data-stu-id="82d51-152">JET_IdxInfoOLC</span></span></p></td>
<td><p><span data-ttu-id="82d51-153">JET_IdxInfoOLC ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="82d51-153">JET_IdxInfoOLC is obsolete.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="82d51-154">JET_IdxInfoResetOLC</span><span class="sxs-lookup"><span data-stu-id="82d51-154">JET_IdxInfoResetOLC</span></span></p></td>
<td><p><span data-ttu-id="82d51-155">JET_IdxInfoResetOLC ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="82d51-155">JET_IdxInfoResetOLC is obsolete.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="82d51-156">JET_IdxInfoSpaceAlloc</span><span class="sxs-lookup"><span data-stu-id="82d51-156">JET_IdxInfoSpaceAlloc</span></span></p></td>
<td><p><span data-ttu-id="82d51-157"><em>pvresult</em> wird als ULONG interpretiert.</span><span class="sxs-lookup"><span data-stu-id="82d51-157"><em>pvResult</em> is interpreted as a ULONG.</span></span> <span data-ttu-id="82d51-158">Bei Erfolg enthält der ULONG die Speicherplatz Verwendung des Indexes.</span><span class="sxs-lookup"><span data-stu-id="82d51-158">On success, the ULONG holds the space usage of the index.</span></span> <span data-ttu-id="82d51-159">Bei einem Fehler ist der Inhalt von <em>pvbuffer</em> nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="82d51-159">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="82d51-160">JET_IdxInfoSysTabCursor</span><span class="sxs-lookup"><span data-stu-id="82d51-160">JET_IdxInfoSysTabCursor</span></span></p></td>
<td><p><span data-ttu-id="82d51-161">JET_IdxInfoSysTabCursor ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="82d51-161">JET_IdxInfoSysTabCursor is obsolete.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="82d51-162">JET_IdxInfoVarSegMac</span><span class="sxs-lookup"><span data-stu-id="82d51-162">JET_IdxInfoVarSegMac</span></span></p></td>
<td><p><span data-ttu-id="82d51-163"><em>pvresult</em> wird als ushort interpretiert.</span><span class="sxs-lookup"><span data-stu-id="82d51-163"><em>pvResult</em> is interpreted as a USHORT.</span></span> <span data-ttu-id="82d51-164">Bei Erfolg enthält der ushort den Wert von <em>cbvarsegmac</em> , der beim Erstellen des Indexes verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="82d51-164">On success, the USHORT holds the value of <em>cbVarSegMac</em> used when the index was created.</span></span> <span data-ttu-id="82d51-165">Unter <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> finden Sie eine Beschreibung von <em>cbvarsegmac</em>.</span><span class="sxs-lookup"><span data-stu-id="82d51-165">See <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> for a description of <em>cbVarSegMac</em>.</span></span> <span data-ttu-id="82d51-166">Bei einem Fehler ist der Inhalt von <em>pvbuffer</em> nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="82d51-166">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="82d51-167">JET_IdxInfoKeyMost</span><span class="sxs-lookup"><span data-stu-id="82d51-167">JET_IdxInfoKeyMost</span></span></p></td>
<td><p><span data-ttu-id="82d51-168"><em>pvresult</em> wird als ushort interpretiert.</span><span class="sxs-lookup"><span data-stu-id="82d51-168"><em>pvResult</em> is interpreted as a USHORT.</span></span> <span data-ttu-id="82d51-169">Bei Erfolg enthält der ushort den Wert von <em>cbkeymost</em> , der beim Erstellen des Indexes verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="82d51-169">On success, the USHORT holds the value of <em>cbKeyMost</em> used when the index was created.</span></span> <span data-ttu-id="82d51-170">Eine Beschreibung von <em>cbkeymost</em>finden Sie unter <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> .</span><span class="sxs-lookup"><span data-stu-id="82d51-170">See <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> for a description of <em>cbKeyMost</em>.</span></span> <span data-ttu-id="82d51-171">Bei einem Fehler ist der Inhalt von <em>pvbuffer</em> nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="82d51-171">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p>
<p><span data-ttu-id="82d51-172"><strong>Windows Vista:  </strong> JET_IdxInfoKeyMost wird in Windows Vista eingeführt.</span><span class="sxs-lookup"><span data-stu-id="82d51-172"><strong>Windows Vista:  </strong>JET_IdxInfoKeyMost is introduced in Windows Vista.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="82d51-173">JET_IdxInfoCreateIndex</span><span class="sxs-lookup"><span data-stu-id="82d51-173">JET_IdxInfoCreateIndex</span></span></p></td>
<td><p><span data-ttu-id="82d51-174"><em>pvresult</em> wird als <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> Struktur interpretiert.</span><span class="sxs-lookup"><span data-stu-id="82d51-174"><em>pvResult</em> is interpreted as a <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure.</span></span> <span data-ttu-id="82d51-175">Bei einem Fehler ist der Inhalt von <em>pvbuffer</em> nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="82d51-175">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p>
<p><span data-ttu-id="82d51-176"><strong>Windows 7:  </strong> JET_IdxInfoCreateIndex wurde in Windows 7 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="82d51-176"><strong>Windows 7:  </strong>JET_IdxInfoCreateIndex is introduced in Windows 7.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="82d51-177">JET_IdxInfoCreateIndex2</span><span class="sxs-lookup"><span data-stu-id="82d51-177">JET_IdxInfoCreateIndex2</span></span></p></td>
<td><p><span data-ttu-id="82d51-178"><em>pvresult</em> wird als <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> Struktur interpretiert.</span><span class="sxs-lookup"><span data-stu-id="82d51-178"><em>pvResult</em> is interpreted as a <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure.</span></span> <span data-ttu-id="82d51-179">Bei einem Fehler ist der Inhalt von <em>pvbuffer</em> nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="82d51-179">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p>
<p><span data-ttu-id="82d51-180"><strong>Windows 7:  </strong> JET_IdxInfoCreateIndex2 wurde in Windows 7 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="82d51-180"><strong>Windows 7:  </strong>JET_IdxInfoCreateIndex2 is introduced in Windows 7.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="82d51-181">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="82d51-181">Return Value</span></span>

<span data-ttu-id="82d51-182">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="82d51-182">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="82d51-183">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="82d51-183">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="82d51-184">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="82d51-184">Return code</span></span></p></th>
<th><p><span data-ttu-id="82d51-185">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="82d51-185">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="82d51-186">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="82d51-186">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="82d51-187">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="82d51-187">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="82d51-188">JET_errIndexNotFound</span><span class="sxs-lookup"><span data-stu-id="82d51-188">JET_errIndexNotFound</span></span></p></td>
<td><p><span data-ttu-id="82d51-189">Der angegebene Index wurde in der angegebenen Tabelle nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="82d51-189">The specified index cannot be found in the specified table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="82d51-190">JET_wrnBufferTruncated</span><span class="sxs-lookup"><span data-stu-id="82d51-190">JET_wrnBufferTruncated</span></span></p></td>
<td><p><span data-ttu-id="82d51-191">Der als <em>pvresult</em> weiter gegebene Puffer war zu klein.</span><span class="sxs-lookup"><span data-stu-id="82d51-191">The buffer passed in as <em>pvResult</em> was too small.</span></span> <span data-ttu-id="82d51-192">Der Inhalt des Puffers ist nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="82d51-192">The contents of the buffer are undefined.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="82d51-193">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="82d51-193">Remarks</span></span>

<span data-ttu-id="82d51-194">**Jetgetindexinfo** und [jetgettableindexinfo](./jetgettableindexinfo-function.md) rufen identische Informationen zu einem Index ab.</span><span class="sxs-lookup"><span data-stu-id="82d51-194">**JetGetIndexInfo** and [JetGetTableIndexInfo](./jetgettableindexinfo-function.md) retrieve identical information about an index.</span></span> <span data-ttu-id="82d51-195">Der Unterschied besteht darin, wie die Tabelle angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="82d51-195">The difference is in how the table is specified.</span></span> <span data-ttu-id="82d51-196">**Jetgetindexinfo** erwartet eine Datenbank (*DBID*) und den Namen einer Tabelle (*sztablename*), während [jetgettableindexinfo](./jetgettableindexinfo-function.md) einen Tabellen Bezeichner (*TableID*) erwartet.</span><span class="sxs-lookup"><span data-stu-id="82d51-196">**JetGetIndexInfo** expects a database (*dbid*) and name of a table (*szTableName*), while [JetGetTableIndexInfo](./jetgettableindexinfo-function.md) expects a table identifier (*tableid*).</span></span>

#### <a name="requirements"></a><span data-ttu-id="82d51-197">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="82d51-197">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="82d51-198"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="82d51-198"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="82d51-199">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="82d51-199">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="82d51-200"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="82d51-200"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="82d51-201">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="82d51-201">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="82d51-202"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="82d51-202"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="82d51-203">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="82d51-203">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="82d51-204"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="82d51-204"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="82d51-205">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="82d51-205">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="82d51-206"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="82d51-206"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="82d51-207">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="82d51-207">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="82d51-208"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="82d51-208"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="82d51-209">Implementiert als <strong>jetgetindexinfow</strong> (Unicode) und <strong>jetgetindexinfoa</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="82d51-209">Implemented as <strong>JetGetIndexInfoW</strong> (Unicode) and <strong>JetGetIndexInfoA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="82d51-210">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="82d51-210">See Also</span></span>

[<span data-ttu-id="82d51-211">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="82d51-211">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="82d51-212">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="82d51-212">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="82d51-213">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="82d51-213">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="82d51-214">JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="82d51-214">JET_INDEXCREATE</span></span>](./jet-indexcreate-structure.md)  
[<span data-ttu-id="82d51-215">JET_INDEXID</span><span class="sxs-lookup"><span data-stu-id="82d51-215">JET_INDEXID</span></span>](./jet-indexid-structure.md)  
[<span data-ttu-id="82d51-216">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="82d51-216">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="82d51-217">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="82d51-217">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="82d51-218">Jetgettableindexinfo</span><span class="sxs-lookup"><span data-stu-id="82d51-218">JetGetTableIndexInfo</span></span>](./jetgettableindexinfo-function.md)
