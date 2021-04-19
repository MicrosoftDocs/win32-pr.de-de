---
description: 'Weitere Informationen zu: jetgetobjectinfo-Funktion'
title: JetGetObjectInfo-Funktion
TOCTitle: JetGetObjectInfo Function
ms:assetid: 3e069c61-6dab-4b79-8bf2-7844d017598f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269232(v=EXCHG.10)
ms:contentKeyID: 32765534
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetObjectInfo
- JetGetObjectInfoA
- JetGetObjectInfoW
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cf4c3c9806d4dcf898d6daeb903eb6fc4322fee7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106358945"
---
# <a name="jetgetobjectinfo-function"></a><span data-ttu-id="eb17f-103">JetGetObjectInfo-Funktion</span><span class="sxs-lookup"><span data-stu-id="eb17f-103">JetGetObjectInfo Function</span></span>


<span data-ttu-id="eb17f-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="eb17f-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetobjectinfo-function"></a><span data-ttu-id="eb17f-105">JetGetObjectInfo-Funktion</span><span class="sxs-lookup"><span data-stu-id="eb17f-105">JetGetObjectInfo Function</span></span>

<span data-ttu-id="eb17f-106">Die **jetgetobjectinfo** -Funktion Ruft Informationen zu Datenbankobjekten ab.</span><span class="sxs-lookup"><span data-stu-id="eb17f-106">The **JetGetObjectInfo** function retrieves information about database objects.</span></span> <span data-ttu-id="eb17f-107">Derzeit werden nur Tabellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="eb17f-107">Currently, only tables are supported.</span></span> <span data-ttu-id="eb17f-108">[Jetgettableinfo](./jetgettableinfo-function.md) kann zum Abrufen von mehr Informationen als **jetgetobjectinfo** verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="eb17f-108">[JetGetTableInfo](./jetgettableinfo-function.md) can be used to fetch more information than **JetGetObjectInfo**.</span></span>

```cpp
    JET_ERR JET_API JetGetObjectInfo(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          JET_OBJTYP objtyp,
      __in_opt      const tchar* szContainerName,
      __in_opt      const tchar* szObjectName,
      __out         void* pvResult,
      __in          unsigned long cbMax,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a><span data-ttu-id="eb17f-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="eb17f-109">Parameters</span></span>

<span data-ttu-id="eb17f-110">*-sid*</span><span class="sxs-lookup"><span data-stu-id="eb17f-110">*sesid*</span></span>

<span data-ttu-id="eb17f-111">Der zu verwendende Daten Bank Sitzungs Kontext.</span><span class="sxs-lookup"><span data-stu-id="eb17f-111">The database session context to use.</span></span>

<span data-ttu-id="eb17f-112">*DBID*</span><span class="sxs-lookup"><span data-stu-id="eb17f-112">*dbid*</span></span>

<span data-ttu-id="eb17f-113">Die Datenbank, aus der die Informationen abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="eb17f-113">The database from which the information is retrieved.</span></span>

<span data-ttu-id="eb17f-114">*objyp*</span><span class="sxs-lookup"><span data-stu-id="eb17f-114">*objtyp*</span></span>

<span data-ttu-id="eb17f-115">Die-Objekte, die Informationen enthalten, die abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="eb17f-115">The objects that contain information to be retrieved.</span></span> <span data-ttu-id="eb17f-116">Derzeit werden nur JET_objtypNil und JET_objtypTable unterstützt, die beide identisch sind.</span><span class="sxs-lookup"><span data-stu-id="eb17f-116">Currently, only JET_objtypNil and JET_objtypTable are supported, both of which behave identically.</span></span> <span data-ttu-id="eb17f-117">Es werden nur Tabellen abgerufen.</span><span class="sxs-lookup"><span data-stu-id="eb17f-117">Only tables will be retrieved.</span></span>

<span data-ttu-id="eb17f-118">*szcontainername*</span><span class="sxs-lookup"><span data-stu-id="eb17f-118">*szContainerName*</span></span>

<span data-ttu-id="eb17f-119">Dieser Parameter ist für die zukünftige Verwendung reserviert und übergibt **null**.</span><span class="sxs-lookup"><span data-stu-id="eb17f-119">This parameter is reserved for future use and passes **NULL**.</span></span> <span data-ttu-id="eb17f-120">Der Name der Objekttypen, für die Informationen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="eb17f-120">The name of the types of objects about which to retrieve information.</span></span>

<span data-ttu-id="eb17f-121">*szobjectname*</span><span class="sxs-lookup"><span data-stu-id="eb17f-121">*szObjectName*</span></span>

<span data-ttu-id="eb17f-122">Der Name des Objekts, das Informationen enthält, die abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="eb17f-122">The name of the object that contains information to retrieve.</span></span> <span data-ttu-id="eb17f-123">Wenn *infolevel* die Optionen JET_ObjInfoList oder JET_ObjInfoListNoStats verwendet, um eine Liste aller Objekte abzurufen, muss dieser Wert **null** oder eine leere Zeichenfolge sein.</span><span class="sxs-lookup"><span data-stu-id="eb17f-123">When *InfoLevel* uses the JET_ObjInfoList or JET_ObjInfoListNoStats options to retrieve a list of all objects, this value should be **NULL** or an empty string.</span></span>

<span data-ttu-id="eb17f-124">Zurzeit werden nur Tabellennamen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="eb17f-124">Only table names are currently supported.</span></span>

<span data-ttu-id="eb17f-125">*pvresult*</span><span class="sxs-lookup"><span data-stu-id="eb17f-125">*pvResult*</span></span>

<span data-ttu-id="eb17f-126">Zeiger auf einen Puffer, der die angegebenen Informationen empfängt.</span><span class="sxs-lookup"><span data-stu-id="eb17f-126">Pointer to a buffer which receives the specified information.</span></span>

<span data-ttu-id="eb17f-127">Die Größe des Puffers in Bytes wird in *cbmax* übermittelt.</span><span class="sxs-lookup"><span data-stu-id="eb17f-127">The size of the buffer, in bytes, is passed in *cbMax*.</span></span> <span data-ttu-id="eb17f-128">Bei einem Fehler ist der Inhalt von *pvresult* nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="eb17f-128">On failure the contents of *pvResult* are undefined.</span></span>

<span data-ttu-id="eb17f-129">Die in *pvresult* gespeicherten Informationen hängen von *infolevel* ab.</span><span class="sxs-lookup"><span data-stu-id="eb17f-129">The information that is stored in *pvResult* depends on *InfoLevel*.</span></span>

<span data-ttu-id="eb17f-130">*cbmax*</span><span class="sxs-lookup"><span data-stu-id="eb17f-130">*cbMax*</span></span>

<span data-ttu-id="eb17f-131">Die Größe (in Bytes) des Puffers, der in *pvresult* übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="eb17f-131">The size, in bytes, of the buffer passed in *pvResult*.</span></span>

<span data-ttu-id="eb17f-132">*Infolevel*</span><span class="sxs-lookup"><span data-stu-id="eb17f-132">*InfoLevel*</span></span>

<span data-ttu-id="eb17f-133">Gibt an, welche Art von Informationen für das angegebene Objekt abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="eb17f-133">Specifies which type of information to retrieve for the specified object.</span></span> <span data-ttu-id="eb17f-134">Dies wirkt sich darauf aus, wie *pvresult* interpretiert wird.</span><span class="sxs-lookup"><span data-stu-id="eb17f-134">It affects how *pvResult* is interpreted.</span></span>

<span data-ttu-id="eb17f-135">Die folgenden Optionen können für diesen Parameter festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="eb17f-135">The following options are available to set for this parameter.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="eb17f-136">Wert</span><span class="sxs-lookup"><span data-stu-id="eb17f-136">Value</span></span></p></th>
<th><p><span data-ttu-id="eb17f-137">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="eb17f-137">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="eb17f-138">JET_ObjInfo</span><span class="sxs-lookup"><span data-stu-id="eb17f-138">JET_ObjInfo</span></span></p></td>
<td><p><span data-ttu-id="eb17f-139"><em>pvresult</em> wird als <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a> Struktur interpretiert.</span><span class="sxs-lookup"><span data-stu-id="eb17f-139"><em>pvResult</em> is interpreted as a <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a> structure.</span></span></p>
<p><span data-ttu-id="eb17f-140">Die <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a> -Struktur wird mit Informationen zu dem Objekt aufgefüllt, das in <em>szobjectname</em>benannt ist.</span><span class="sxs-lookup"><span data-stu-id="eb17f-140">The <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a> structure is populated with information pertaining to the object that is named in <em>szObjectName</em>.</span></span></p>
<p><span data-ttu-id="eb17f-141">Wenn der Aufrufer nicht die Anzahl der Datensätze und Seiten für das Objekt kennen möchte, sollten Sie JET_ObjInfoNoStats Informationsebene verwenden, die möglicherweise schneller ist, da keine Statistik enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="eb17f-141">If the caller does not want to know the number of records and pages for the object, consider using JET_ObjInfoNoStats information level, which might be faster since statistics are not included.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eb17f-142">JET_ObjInfoList</span><span class="sxs-lookup"><span data-stu-id="eb17f-142">JET_ObjInfoList</span></span></p></td>
<td><p><span data-ttu-id="eb17f-143"><em>pvresult</em> wird als <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a> Struktur interpretiert.</span><span class="sxs-lookup"><span data-stu-id="eb17f-143"><em>pvResult</em> is interpreted as a <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a> structure.</span></span> <span data-ttu-id="eb17f-144">Informationen zu allen Objekten werden abgerufen.</span><span class="sxs-lookup"><span data-stu-id="eb17f-144">Information about all objects is retrieved.</span></span> <span data-ttu-id="eb17f-145">Es wird eine temporäre Tabelle erstellt, und die Informationen, die für die Durchführung der temporären Tabelle erforderlich sind, werden in der <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a> Struktur beschrieben.</span><span class="sxs-lookup"><span data-stu-id="eb17f-145">A temporary table will be created, and the information that is necessary to traverse the temporary table is described in the <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a> structure.</span></span> <span data-ttu-id="eb17f-146">Weitere Informationen finden Sie unter <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a>.</span><span class="sxs-lookup"><span data-stu-id="eb17f-146">For more information, see <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a>.</span></span> <span data-ttu-id="eb17f-147">Wenn der Aufrufer nicht die Anzahl der Datensätze und Seiten für das Objekt kennen möchte, sollten Sie JET_ObjInfoListNoStats verwenden, die möglicherweise schneller ist.</span><span class="sxs-lookup"><span data-stu-id="eb17f-147">If the caller does not want to know the number of records and pages for the object, consider using JET_ObjInfoListNoStats, which might be faster.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eb17f-148">JET_ObjInfoListACM</span><span class="sxs-lookup"><span data-stu-id="eb17f-148">JET_ObjInfoListACM</span></span></p></td>
<td><p><span data-ttu-id="eb17f-149">Veraltet und wird derzeit nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="eb17f-149">Deprecated and not currently supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eb17f-150">JET_ObjInfoListNoStats</span><span class="sxs-lookup"><span data-stu-id="eb17f-150">JET_ObjInfoListNoStats</span></span></p></td>
<td><p><span data-ttu-id="eb17f-151"><em>pvresult</em> wird als <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a> Struktur interpretiert.</span><span class="sxs-lookup"><span data-stu-id="eb17f-151"><em>pvResult</em> is interpreted as a <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a> structure.</span></span> <span data-ttu-id="eb17f-152">Informationen zu allen Objekten werden abgerufen.</span><span class="sxs-lookup"><span data-stu-id="eb17f-152">Information about all objects is retrieved.</span></span> <span data-ttu-id="eb17f-153">Es wird eine temporäre Tabelle erstellt, und die Informationen, die für die Durchführung der temporären Tabelle erforderlich sind, werden in der <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a> Struktur beschrieben.</span><span class="sxs-lookup"><span data-stu-id="eb17f-153">A temporary table will be created, and the information that is necessary to traverse the temporary table is described in the <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a> structure.</span></span> <span data-ttu-id="eb17f-154">Weitere Informationen finden Sie unter <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a>.</span><span class="sxs-lookup"><span data-stu-id="eb17f-154">For more information, see <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a>.</span></span> <span data-ttu-id="eb17f-155">JET_ObjInfoListNoStats ist mit JET_ObjInfoList identisch, mit der Ausnahme, dass die Spalten, die die Anzahl von Datensätzen (<em>columnidcrecord</em>) und Pages (<em>columnidcpage</em>) melden, nicht aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="eb17f-155">JET_ObjInfoListNoStats is identical to JET_ObjInfoList, except that the columns that report the number of records (<em>columnidcRecord</em>) and pages (<em>columnidcPage</em>) will not be updated.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eb17f-156">JET_ObjInfoMax</span><span class="sxs-lookup"><span data-stu-id="eb17f-156">JET_ObjInfoMax</span></span></p></td>
<td><p><span data-ttu-id="eb17f-157"><em>pvresult</em> wird als <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a>interpretiert.</span><span class="sxs-lookup"><span data-stu-id="eb17f-157"><em>pvResult</em> is interpreted as a <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a>.</span></span> <span data-ttu-id="eb17f-158">Die maximale Größe des Objekts befindet sich auf Seiten.</span><span class="sxs-lookup"><span data-stu-id="eb17f-158">The maximum size of the object is in pages.</span></span> <span data-ttu-id="eb17f-159">Zurzeit werden nur Tabellen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="eb17f-159">Currently only tables will be returned.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eb17f-160">JET_ObjInfoNoStats</span><span class="sxs-lookup"><span data-stu-id="eb17f-160">JET_ObjInfoNoStats</span></span></p></td>
<td><p><span data-ttu-id="eb17f-161"><em>pvresult</em> wird als <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a>interpretiert.</span><span class="sxs-lookup"><span data-stu-id="eb17f-161"><em>pvResult</em> is interpreted as a <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a>.</span></span> <span data-ttu-id="eb17f-162">Informationen zu nur dem in " <em>szobjectname</em> " angegebenen Objekt werden abgerufen.</span><span class="sxs-lookup"><span data-stu-id="eb17f-162">Information about only the object given in <em>szObjectName</em> will be retrieved.</span></span></p>
<p><span data-ttu-id="eb17f-163">Die <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a> Struktur wird mit Informationen zu dem Objekt aufgefüllt, das in <em>szobjectname</em>benannt ist.</span><span class="sxs-lookup"><span data-stu-id="eb17f-163">The <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a> structure will be populated with information pertaining to the object that is named in <em>szObjectName</em>.</span></span></p>
<p><span data-ttu-id="eb17f-164">JET_ObjInfoNoStats ist mit JET_ObjInfo identisch, mit dem Unterschied, dass die Felder, die die Anzahl von Datensätzen und Seiten melden, auf NULL festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="eb17f-164">JET_ObjInfoNoStats is identical to JET_ObjInfo, except that the fields that report the number of records and pages are set to zero.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eb17f-165">JET_ObjInfoRulesLoaded</span><span class="sxs-lookup"><span data-stu-id="eb17f-165">JET_ObjInfoRulesLoaded</span></span></p></td>
<td><p><span data-ttu-id="eb17f-166">Veraltet und wird derzeit nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="eb17f-166">Deprecated and not currently supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eb17f-167">JET_ObjInfoSysTabCursor</span><span class="sxs-lookup"><span data-stu-id="eb17f-167">JET_ObjInfoSysTabCursor</span></span></p></td>
<td><p><span data-ttu-id="eb17f-168">Veraltet und wird derzeit nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="eb17f-168">Deprecated and not currently supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eb17f-169">JET_ObjInfoSysTabReadOnly</span><span class="sxs-lookup"><span data-stu-id="eb17f-169">JET_ObjInfoSysTabReadOnly</span></span></p></td>
<td><p><span data-ttu-id="eb17f-170">Veraltet und wird derzeit nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="eb17f-170">Deprecated and not currently supported.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="eb17f-171">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="eb17f-171">Return Value</span></span>

<span data-ttu-id="eb17f-172">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="eb17f-172">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="eb17f-173">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="eb17f-173">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="eb17f-174">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="eb17f-174">Return code</span></span></p></th>
<th><p><span data-ttu-id="eb17f-175">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="eb17f-175">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="eb17f-176">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="eb17f-176">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="eb17f-177">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="eb17f-177">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eb17f-178">JET_errBufferTooSmall</span><span class="sxs-lookup"><span data-stu-id="eb17f-178">JET_errBufferTooSmall</span></span></p></td>
<td><p><span data-ttu-id="eb17f-179">Die Größe des in <em>cbmax</em> angegebenen Puffers war zu klein, um die gewünschten Informationen zu speichern.</span><span class="sxs-lookup"><span data-stu-id="eb17f-179">The size of the buffer given in <em>cbMax</em> was too small to hold the desired information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eb17f-180">JET_errInvalidName</span><span class="sxs-lookup"><span data-stu-id="eb17f-180">JET_errInvalidName</span></span></p></td>
<td><p><span data-ttu-id="eb17f-181">In " <em>szobjectname</em> " oder " <em>szcontainername</em>" wurde ein ungültiger Name angegeben.</span><span class="sxs-lookup"><span data-stu-id="eb17f-181">An invalid name was given in <em>szObjectName</em> or <em>szContainerName</em>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eb17f-182">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="eb17f-182">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="eb17f-183">Ein ungültiger Parameter wurde angegeben.</span><span class="sxs-lookup"><span data-stu-id="eb17f-183">A bad parameter was given.</span></span> <span data-ttu-id="eb17f-184">Es ist möglich, dass eine ungültige Ebene an <em>infolevel</em>übermittelt wurde.</span><span class="sxs-lookup"><span data-stu-id="eb17f-184">It is possible that a bad level was passed in to <em>InfoLevel</em>.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="eb17f-185">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="eb17f-185">Remarks</span></span>

<span data-ttu-id="eb17f-186">Wenn **jetgetobjectinfo** erfolgreich eine temporäre Tabelle erstellt (z. b. JET_ObjInfoList oder JET_ObjInfoNoStats), ist der Aufrufer für das Schließen der temporären Tabelle mit [jetclosetable](./jetclosetable-function.md)verantwortlich.</span><span class="sxs-lookup"><span data-stu-id="eb17f-186">If **JetGetObjectInfo** successfully creates a temporary table (for example, JET_ObjInfoList or JET_ObjInfoNoStats), the caller is responsible for closing the temporary table with [JetCloseTable](./jetclosetable-function.md).</span></span>

<span data-ttu-id="eb17f-187">**Jetgetobjectinfo** unterstützt derzeit nur das Abrufen von Informationen zu Tabellen.</span><span class="sxs-lookup"><span data-stu-id="eb17f-187">**JetGetObjectInfo** currently only supports retrieving information about tables.</span></span>

#### <a name="requirements"></a><span data-ttu-id="eb17f-188">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="eb17f-188">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="eb17f-189"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="eb17f-189"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="eb17f-190">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="eb17f-190">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eb17f-191"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="eb17f-191"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="eb17f-192">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="eb17f-192">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eb17f-193"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="eb17f-193"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="eb17f-194">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="eb17f-194">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eb17f-195"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="eb17f-195"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="eb17f-196">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="eb17f-196">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eb17f-197"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="eb17f-197"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="eb17f-198">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="eb17f-198">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eb17f-199"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="eb17f-199"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="eb17f-200">Implementiert als <strong>jetgetobjectinfow</strong> (Unicode) und <strong>jetgetobjectinfoa</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="eb17f-200">Implemented as <strong>JetGetObjectInfoW</strong> (Unicode) and <strong>JetGetObjectInfoA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="eb17f-201">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="eb17f-201">See Also</span></span>

[<span data-ttu-id="eb17f-202">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="eb17f-202">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="eb17f-203">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="eb17f-203">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="eb17f-204">JET_OBJTYP</span><span class="sxs-lookup"><span data-stu-id="eb17f-204">JET_OBJTYP</span></span>](./jet-objtyp.md)  
[<span data-ttu-id="eb17f-205">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="eb17f-205">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="eb17f-206">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="eb17f-206">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="eb17f-207">JET_OBJECTINFO</span><span class="sxs-lookup"><span data-stu-id="eb17f-207">JET_OBJECTINFO</span></span>](./jet-objectinfo-structure.md)  
[<span data-ttu-id="eb17f-208">JET_OBJECTLIST</span><span class="sxs-lookup"><span data-stu-id="eb17f-208">JET_OBJECTLIST</span></span>](./jet-objectlist-structure.md)  
[<span data-ttu-id="eb17f-209">Jetclosetable</span><span class="sxs-lookup"><span data-stu-id="eb17f-209">JetCloseTable</span></span>](./jetclosetable-function.md)  
[<span data-ttu-id="eb17f-210">Jetgettableinfo</span><span class="sxs-lookup"><span data-stu-id="eb17f-210">JetGetTableInfo</span></span>](./jetgettableinfo-function.md)
