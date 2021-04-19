---
description: 'Weitere Informationen zu: jetopentemporarytable-Funktion'
title: Jetopentemporarytable-Funktion
TOCTitle: JetOpenTemporaryTable Function
ms:assetid: feacd0b8-2298-4ec6-aa59-0fede08474bc
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294144(v=EXCHG.10)
ms:contentKeyID: 32765758
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOpenTemporaryTable
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2335f6d6426b321d5db55b4ed005c6220484d509
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353837"
---
# <a name="jetopentemporarytable-function"></a><span data-ttu-id="18411-103">Jetopentemporarytable-Funktion</span><span class="sxs-lookup"><span data-stu-id="18411-103">JetOpenTemporaryTable Function</span></span>


<span data-ttu-id="18411-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="18411-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetopentemporarytable-function"></a><span data-ttu-id="18411-105">Jetopentemporarytable-Funktion</span><span class="sxs-lookup"><span data-stu-id="18411-105">JetOpenTemporaryTable Function</span></span>

<span data-ttu-id="18411-106">Die **jetopentemporarytable** -Funktion erstellt eine flüchtige Tabelle mit einem einzelnen Index, der zum Speichern und Abrufen von Datensätzen verwendet werden kann, genau wie eine gewöhnliche Tabelle, die über [jetkreatetablecolumnindex](./jetcreatetablecolumnindex-function.md)erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="18411-106">The **JetOpenTemporaryTable** function creates a volatile table with a single index that can be used to store and retrieve records, just like an ordinary table that is created via [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md).</span></span>

<span data-ttu-id="18411-107">**Windows Vista:**  **jetopertemporarytable** wird in Windows Vista eingeführt.</span><span class="sxs-lookup"><span data-stu-id="18411-107">**Windows Vista:**  **JetOpenTemporaryTable** is introduced in Windows Vista.</span></span>

<span data-ttu-id="18411-108">Temporäre Tabellen sind aufgrund ihrer flüchtigen Natur schneller als normale Tabellen.</span><span class="sxs-lookup"><span data-stu-id="18411-108">Temporary tables are faster than ordinary tables due to their volatile nature.</span></span> <span data-ttu-id="18411-109">Sie können eine doppelte Entfernung von Daten Satz Gruppen schnell Sortieren und durchführen, wenn auf Sie in einer rein sequenziellen Weise darauf zugegriffen wird.</span><span class="sxs-lookup"><span data-stu-id="18411-109">They can quickly sort and perform duplicate removal on record sets when they are accessed in a purely sequential manner.</span></span>

```cpp
    JET_ERR JET_API JetOpenTemporaryTable(
      __in          JET_SESID sesid,
      __in          JET_OPENTEMPORARYTABLE* popentemporarytable
    );
```

### <a name="parameters"></a><span data-ttu-id="18411-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="18411-110">Parameters</span></span>

<span data-ttu-id="18411-111">*-sid*</span><span class="sxs-lookup"><span data-stu-id="18411-111">*sesid*</span></span>

<span data-ttu-id="18411-112">Die Sitzung, die für diesen-Befehl verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="18411-112">The session that will be used for this call.</span></span>

<span data-ttu-id="18411-113">*popendtemporarytable*</span><span class="sxs-lookup"><span data-stu-id="18411-113">*popentemporarytable*</span></span>

<span data-ttu-id="18411-114">Ein Zeiger auf eine [JET_OPENTEMPORARYTABLE](./jet-opentemporarytable-structure.md) -Struktur, die die Beschreibung der in der Eingabe zu erstellenden temporären Tabelle enthält.</span><span class="sxs-lookup"><span data-stu-id="18411-114">A pointer to a [JET_OPENTEMPORARYTABLE](./jet-opentemporarytable-structure.md) structure that contains the description of the temporary table to create on input.</span></span> <span data-ttu-id="18411-115">Nach einem erfolgreichen-Vorgang enthält die-Struktur das Handle für die temporären Tabellen-und Spalten Identifizierungen.</span><span class="sxs-lookup"><span data-stu-id="18411-115">After a successful call, the structure contains the handle to the temporary table and column identifications.</span></span>

### <a name="return-value"></a><span data-ttu-id="18411-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="18411-116">Return Value</span></span>

<span data-ttu-id="18411-117">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="18411-117">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="18411-118">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="18411-118">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="18411-119">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="18411-119">Return code</span></span></p></th>
<th><p><span data-ttu-id="18411-120">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="18411-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="18411-121">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="18411-121">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="18411-122">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="18411-122">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18411-123">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="18411-123">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="18411-124">Der Vorgang ist fehlgeschlagen, da nicht genügend Arbeitsspeicher zugeordnet werden konnte, um den Vorgang abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="18411-124">The operation failed because not enough memory could be allocated to complete it.</span></span></p>
<p><span data-ttu-id="18411-125"><strong>Jetopumtemporarytable</strong> kann JET_errOutOfMemory zurückgeben, wenn der Adressraum des Host Prozesses zu fragmentiert wird.</span><span class="sxs-lookup"><span data-stu-id="18411-125"><strong>JetOpenTemporaryTable</strong> can return JET_errOutOfMemory if the address space of the host process becomes too fragmented.</span></span> <span data-ttu-id="18411-126">Der temporäre Tabellen-Manager weist für jede temporäre Tabelle, die unabhängig von der gespeicherten Datenmenge erstellt wird, 1 MB Adressraum zu.</span><span class="sxs-lookup"><span data-stu-id="18411-126">The temporary table manager will allocates a 1 MB chunk of address space for every temporary table created regardless of the amount of data is stored.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="18411-127">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="18411-127">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="18411-128">Einer der angegebenen Parameter enthielt einen unerwarteten Wert, oder die Kombination mehrerer Parameterwerte führte zu einem unerwarteten Ergebnis.</span><span class="sxs-lookup"><span data-stu-id="18411-128">One of the provided parameters contained an unexpected value or the combination of several parameter values resulted in an unexpected result.</span></span></p>
<p><span data-ttu-id="18411-129">Dieser Fehler wird von <strong>jetopertemporarytable</strong> unter den folgenden Bedingungen zurückgegeben:</span><span class="sxs-lookup"><span data-stu-id="18411-129">This error is returned by <strong>JetOpenTemporaryTable</strong> under the following conditions:</span></span></p>
<ul>
<li><p><span data-ttu-id="18411-130">Der <strong>cbStruct</strong> -Member der <a href="gg269206(v=exchg.10).md">JET_OPENTEMPORARYTABLE</a> Struktur entspricht keiner Version dieser Struktur, die von dieser Version der Datenbank-Engine unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="18411-130">The <strong>cbStruct</strong> member of the <a href="gg269206(v=exchg.10).md">JET_OPENTEMPORARYTABLE</a> structure does not correspond to a version of this structure that is supported by that version of the database engine</span></span></p></li>
<li><p><span data-ttu-id="18411-131">Der <strong>cbkeymost</strong> -Member der <a href="gg269206(v=exchg.10).md">JET_OPENTEMPORARYTABLE</a> -Struktur ist kleiner als JET_cbKeyMostMin.</span><span class="sxs-lookup"><span data-stu-id="18411-131">The <strong>cbKeyMost</strong> member of the <a href="gg269206(v=exchg.10).md">JET_OPENTEMPORARYTABLE</a> structure is less than JET_cbKeyMostMin.</span></span></p></li>
<li><p><span data-ttu-id="18411-132">Der <strong>cbkeymost</strong> -Member der <a href="gg269206(v=exchg.10).md">JET_OPENTEMPORARYTABLE</a> -Struktur ist größer als der größte unterstützte Wert für die Datenbankseiten Größe für die-Instanz (JET_paramDatabasePageSize).</span><span class="sxs-lookup"><span data-stu-id="18411-132">The <strong>cbKeyMost</strong> member of the <a href="gg269206(v=exchg.10).md">JET_OPENTEMPORARYTABLE</a> structure is larger than the largest supported value for the database page size for the instance (JET_paramDatabasePageSize).</span></span> <span data-ttu-id="18411-133">Weitere Informationen finden Sie unter dem JET_paramKeyMost-Parameter in der Liste mit <a href="gg269241(v=exchg.10).md">Informations Parametern</a> .</span><span class="sxs-lookup"><span data-stu-id="18411-133">See the JET_paramKeyMost parameter in the list of <a href="gg269241(v=exchg.10).md">Informational Parameters</a> for more information.</span></span></p></li>
<li><p><span data-ttu-id="18411-134">Der cbvarsegmac-Member der <a href="gg269206(v=exchg.10).md">JET_OPENTEMPORARYTABLE</a> Struktur ist größer als der <strong>cbkeymost</strong> -Member.</span><span class="sxs-lookup"><span data-stu-id="18411-134">The cbVarSegMac member of the <a href="gg269206(v=exchg.10).md">JET_OPENTEMPORARYTABLE</a> structure is larger than The <strong>cbKeyMost</strong> member.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18411-135">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="18411-135">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="18411-136">Der Vorgang kann nicht abgeschlossen werden, da die-Instanz, die der Sitzung zugeordnet war, noch nicht initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="18411-136">The operation cannot complete because the instance that was associated with the session has not yet been initialized.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="18411-137">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="18411-137">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="18411-138">Der Vorgang kann nicht ausgeführt werden, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufens von <a href="gg269240(v=exchg.10).md">jetstopservice</a>beendet wurden.</span><span class="sxs-lookup"><span data-stu-id="18411-138">The operation cannot complete because all activity on the instance that is associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18411-139">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="18411-139">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="18411-140">Der Vorgang kann nicht ausgeführt werden, da der-Instanz, die der Sitzung zugeordnet ist, ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten gesperrt wird, um die Integrität der Daten zu schützen.</span><span class="sxs-lookup"><span data-stu-id="18411-140">The operation cannot complete because the instance that is associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="18411-141"><strong>Windows XP:</strong>  Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="18411-141"><strong>Windows XP:</strong>  This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="18411-142">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="18411-142">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="18411-143">Der Vorgang kann nicht ausgeführt werden, da die-Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="18411-143">The operation cannot complete because the instance that is associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18411-144">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="18411-144">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="18411-145">Der Vorgang kann nicht abgeschlossen werden, da für die-Instanz, die der Sitzung zugeordnet ist, ein Wiederherstellungs Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="18411-145">The operation cannot complete because a restore operation is in progress on the instance that is associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="18411-146">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="18411-146">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="18411-147">Dieselbe Sitzung kann nicht für mehr als einen Thread gleichzeitig verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="18411-147">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="18411-148"><strong>Windows XP:</strong>  Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="18411-148"><strong>Windows XP:</strong>  This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18411-149">JET_errInvalidSesid</span><span class="sxs-lookup"><span data-stu-id="18411-149">JET_errInvalidSesid</span></span></p></td>
<td><p><span data-ttu-id="18411-150">Das Sitzungs Handle ist ungültig oder verweist auf eine geschlossene Sitzung.</span><span class="sxs-lookup"><span data-stu-id="18411-150">The session handle is invalid or refers to a closed session.</span></span></p>
<p><span data-ttu-id="18411-151"><strong>Hinweis</strong>  Dieser Fehler wird unter allen Umständen nicht zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="18411-151"><strong>Note</strong>  This error is not returned under all circumstances.</span></span> <span data-ttu-id="18411-152">Handles werden nur auf Grundlage der bestmöglichen Leistung überprüft.</span><span class="sxs-lookup"><span data-stu-id="18411-152">Handles are validated on a best effort basis only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="18411-153">JET_errOutOfCursors</span><span class="sxs-lookup"><span data-stu-id="18411-153">JET_errOutOfCursors</span></span></p></td>
<td><p><span data-ttu-id="18411-154">Der Vorgang ist fehlgeschlagen, da die Engine die zum Öffnen eines neuen Cursors erforderlichen Ressourcen nicht zuordnen kann.</span><span class="sxs-lookup"><span data-stu-id="18411-154">The operation failed because the engine cannot allocate the resources that are required to open a new cursor.</span></span> <span data-ttu-id="18411-155">Cursor Ressourcen werden mithilfe von <a href="gg294044(v=exchg.10).md">jetsetsystemparameter</a> mit <a href="gg269201(v=exchg.10).md">JET_paramMaxCursors</a>konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="18411-155">Cursor resources are configured using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <a href="gg269201(v=exchg.10).md">JET_paramMaxCursors</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18411-156">JET_errTooManySorts</span><span class="sxs-lookup"><span data-stu-id="18411-156">JET_errTooManySorts</span></span></p></td>
<td><p><span data-ttu-id="18411-157">Der Vorgang ist fehlgeschlagen, da die Engine die zum Erstellen einer temporären Tabelle erforderlichen Ressourcen nicht zuordnen kann.</span><span class="sxs-lookup"><span data-stu-id="18411-157">The operation failed because the engine cannot allocate the resources that are required to create a temporary table.</span></span> <span data-ttu-id="18411-158">Temporäre Tabellen Ressourcen werden mithilfe von <a href="gg294044(v=exchg.10).md">jetsetsystemparameter</a> mit <a href="gg294140(v=exchg.10).md">JET_paramMaxTemporaryTables</a>konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="18411-158">Temporary table resources are configured using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <a href="gg294140(v=exchg.10).md">JET_paramMaxTemporaryTables</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="18411-159">JET_errCannotMaterializeForwardOnlySort</span><span class="sxs-lookup"><span data-stu-id="18411-159">JET_errCannotMaterializeForwardOnlySort</span></span></p></td>
<td><p><span data-ttu-id="18411-160">Fehler bei <strong>jetopentemporarytable</strong> , weil JET_bitTTForwardOnly angegeben wurde und die angegebene temporäre Tabelle nicht mithilfe der vorwärts Optimierung erstellt werden konnte.</span><span class="sxs-lookup"><span data-stu-id="18411-160"><strong>JetOpenTemporaryTable</strong> failed because JET_bitTTForwardOnly was specified and the temporary table that was specified could not be created using the forward-only optimization.</span></span></p>
<p><span data-ttu-id="18411-161"><strong>Windows Server 2003:</strong>  Dieser Fehler wird nur von Windows Server 2003 und höheren Versionen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="18411-161"><strong>Windows Server 2003:</strong>  This error will only be returned by Windows Server 2003 and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18411-162">JET_errTooManyColumns</span><span class="sxs-lookup"><span data-stu-id="18411-162">JET_errTooManyColumns</span></span></p></td>
<td><p><span data-ttu-id="18411-163">Es wurde versucht, der Tabelle zu viele Spalten hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="18411-163">An attempt was made to add too many columns to the table.</span></span> <span data-ttu-id="18411-164">Eine Tabelle kann nicht mehr als JET_ccolFixedMost fester Spalten, nicht mehr als JET_ccolVarMost Spalten variabler Länge und nicht mehr als JET_ccolTaggedMost markierte Spalten aufweisen.</span><span class="sxs-lookup"><span data-stu-id="18411-164">A table can have no more than JET_ccolFixedMost fixed columns, no more than JET_ccolVarMost variable-length columns, and no more than JET_ccolTaggedMost tagged columns.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="18411-165">JET_errTooManyOpenTables</span><span class="sxs-lookup"><span data-stu-id="18411-165">JET_errTooManyOpenTables</span></span></p></td>
<td><p><span data-ttu-id="18411-166">Der Vorgang ist fehlgeschlagen, da die Engine die zum Zwischenspeichern des Schemas der Tabelle erforderlichen Ressourcen nicht zuordnen kann.</span><span class="sxs-lookup"><span data-stu-id="18411-166">The operation failed because the engine cannot allocate the resources that are required to cache the schema of the table.</span></span> <span data-ttu-id="18411-167">Um die Anzahl der Tabellen zu konfigurieren, die Schemas aufweisen, die zwischengespeichert werden können, verwenden Sie <a href="gg294044(v=exchg.10).md">jetsetsystemparameter</a> mit <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>.</span><span class="sxs-lookup"><span data-stu-id="18411-167">To configure the number of tables that have schemas that can be cached, use <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18411-168">JET_errInvalidCodePage</span><span class="sxs-lookup"><span data-stu-id="18411-168">JET_errInvalidCodePage</span></span></p></td>
<td><p><span data-ttu-id="18411-169">Der <strong>CP</strong> -Member der <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> Struktur wurde nicht auf eine gültige Codepage festgelegt.</span><span class="sxs-lookup"><span data-stu-id="18411-169">The <strong>cp</strong> member of the <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> structure was not set to a valid code page.</span></span> <span data-ttu-id="18411-170">Die einzigen gültigen Werte für Textspalten sind Englisch (1252) und Unicode (1200).</span><span class="sxs-lookup"><span data-stu-id="18411-170">The only valid values for text columns are English (1252) and Unicode (1200).</span></span> <span data-ttu-id="18411-171">Der Wert 0 bedeutet, dass der Standardwert verwendet wird (Englisch, 1252).</span><span class="sxs-lookup"><span data-stu-id="18411-171">A value of 0 means the default will be used (English, 1252).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="18411-172">JET_errInvalidColumnType</span><span class="sxs-lookup"><span data-stu-id="18411-172">JET_errInvalidColumnType</span></span></p></td>
<td><p><span data-ttu-id="18411-173">Der <strong>colttmember</strong> des <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> wurde nicht auf einen gültigen Spaltentyp festgelegt.</span><span class="sxs-lookup"><span data-stu-id="18411-173">The <strong>coltyp</strong> member of the <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> was not set to a valid column type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18411-174">JET_errInvalidLanguageId</span><span class="sxs-lookup"><span data-stu-id="18411-174">JET_errInvalidLanguageId</span></span></p></td>
<td><p><span data-ttu-id="18411-175">Der Index konnte nicht erstellt werden, da versucht wurde, eine ungültige Gebiets Schema-ID zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="18411-175">The index could not be created because an attempt was made to use an invalid locale ID.</span></span> <span data-ttu-id="18411-176">Die Gebiets Schema-ID ist möglicherweise vollständig ungültig, oder das zugehörige Sprachpaket ist möglicherweise nicht installiert.</span><span class="sxs-lookup"><span data-stu-id="18411-176">The locale ID might be either completely invalid or the associated language pack might not be installed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="18411-177">JET_errInvalidLCMapStringFlags</span><span class="sxs-lookup"><span data-stu-id="18411-177">JET_errInvalidLCMapStringFlags</span></span></p></td>
<td><p><span data-ttu-id="18411-178">Der Index konnte nicht erstellt werden, da versucht wurde, einen ungültigen Satz von normalisierungs Flags zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="18411-178">The index could not be created because an attempt was made to use an invalid set of normalization flags.</span></span></p>
<p><span data-ttu-id="18411-179"><strong>Windows XP:</strong>  Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="18411-179"><strong>Windows XP:</strong>  This error will only be returned by Windows XP and later releases.</span></span></p>
<p><span data-ttu-id="18411-180"><strong>Windows 2000:</strong>  Unter Windows 2000 führen ungültige normalisierungs Flags zu JET_errIndexInvalidDef.</span><span class="sxs-lookup"><span data-stu-id="18411-180"><strong>Windows 2000:</strong>  On Windows 2000, invalid normalization flags will result in JET_errIndexInvalidDef.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18411-181">JET_errIndexInvalidDef</span><span class="sxs-lookup"><span data-stu-id="18411-181">JET_errIndexInvalidDef</span></span></p></td>
<td><p><span data-ttu-id="18411-182">Der Index konnte nicht erstellt werden, da eine ungültige Index Definition angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="18411-182">The index could not be created because an invalid index definition was specified.</span></span> <span data-ttu-id="18411-183"><strong>Jetopumtemporarytable</strong> gibt diesen Fehler unter den folgenden Bedingungen zurück:</span><span class="sxs-lookup"><span data-stu-id="18411-183"><strong>JetOpenTemporaryTable</strong> will return this error under the following conditions:</span></span></p>
<ul>
<li><p><span data-ttu-id="18411-184">Das sprachneutrale Gebiets Schema ist angegeben.</span><span class="sxs-lookup"><span data-stu-id="18411-184">The Language Neutral locale is specified.</span></span></p></li>
<li><p><span data-ttu-id="18411-185">Es wurde ein ungültiger Satz von normalisierungs Flags angegeben.</span><span class="sxs-lookup"><span data-stu-id="18411-185">An invalid set of normalization flags is specified.</span></span></p></li>
</ul>
<p><span data-ttu-id="18411-186"><strong>Windows 2000:</strong>  Dieser Fehler wird nur von Windows 2000 zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="18411-186"><strong>Windows 2000:</strong>  This error will only be returned by Windows 2000.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="18411-187">JET_errTooManyOpenIndexes</span><span class="sxs-lookup"><span data-stu-id="18411-187">JET_errTooManyOpenIndexes</span></span></p></td>
<td><p><span data-ttu-id="18411-188">Der Vorgang ist fehlgeschlagen, da die Engine die zum Zwischenspeichern der Indizes der Tabelle erforderlichen Ressourcen nicht zuordnen kann.</span><span class="sxs-lookup"><span data-stu-id="18411-188">The operation failed because the engine cannot allocate the resources that are required to cache the indexes of the table.</span></span> <span data-ttu-id="18411-189">Um die Anzahl der Indizes zu konfigurieren, die Schemas aufweisen, die zwischengespeichert werden können, verwenden Sie <a href="gg294044(v=exchg.10).md">jetsetsystemparameter</a> mit <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>.</span><span class="sxs-lookup"><span data-stu-id="18411-189">To configure the number of indexes that have schemas that can be cached, use <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="18411-190">Bei Erfolg wird ein Cursor zurückgegeben, der für die neu erstellte temporäre Tabelle geöffnet wurde.</span><span class="sxs-lookup"><span data-stu-id="18411-190">On success, a cursor opened on the newly created temporary table will be returned.</span></span> <span data-ttu-id="18411-191">Der Status der temporären Datenbank wird darauf vorbereitet, die neue temporäre Tabelle zu enthalten.</span><span class="sxs-lookup"><span data-stu-id="18411-191">The state of the temporary database will be prepared to contain the new temporary table.</span></span> <span data-ttu-id="18411-192">Der Status aller normalen Datenbanken, die von der Datenbank-Engine verwendet werden, bleibt unverändert.</span><span class="sxs-lookup"><span data-stu-id="18411-192">The state of any ordinary databases in use by the database engine will remain unchanged.</span></span>

<span data-ttu-id="18411-193">Bei einem Fehler wird die temporäre Tabelle nicht erstellt, und ein Cursor wird nicht zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="18411-193">On failure, the temporary table will not be created and a cursor will not be returned.</span></span> <span data-ttu-id="18411-194">Der Status der temporären Datenbank kann geändert werden.</span><span class="sxs-lookup"><span data-stu-id="18411-194">The state of the temporary database can be changed.</span></span> <span data-ttu-id="18411-195">Der Status aller normalen Datenbanken, die von der Datenbank-Engine verwendet werden, bleibt unverändert.</span><span class="sxs-lookup"><span data-stu-id="18411-195">The state of any ordinary databases in use by the database engine will remain unchanged.</span></span>

#### <a name="remarks"></a><span data-ttu-id="18411-196">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="18411-196">Remarks</span></span>

<span data-ttu-id="18411-197">Temporäre Tabellen unterstützen nicht die vollständige Ergänzung der Spalten Definitions Optionen, die normalerweise von der Datenbank-Engine unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="18411-197">Temporary tables do not support the full complement of column definition options that are ordinarily supported by the database engine.</span></span> <span data-ttu-id="18411-198">Tatsächlich werden nur JET_bitColumnFixed und JET_bitColumnTagged unterstützt.</span><span class="sxs-lookup"><span data-stu-id="18411-198">In fact, only JET_bitColumnFixed and JET_bitColumnTagged are supported.</span></span> <span data-ttu-id="18411-199">Dies bedeutet, dass es nicht möglich ist, eine automatische Inkrement-, Versions-oder mehrwertige Spalte in einer temporären Tabelle zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="18411-199">This means that it is not possible to create an auto-increment, version, or multi-valued column in a temporary table.</span></span> <span data-ttu-id="18411-200">Zum Schluss werden die Spalten zum Aktualisieren von Spalten nicht unterstützt, da Sie nur von einer Sitzung gleichzeitig verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="18411-200">Finally, escrow update columns are not supported because they can only be used by one session at a time.</span></span> <span data-ttu-id="18411-201">Wenn eine dieser Optionen angefordert wird, werden Sie ignoriert.</span><span class="sxs-lookup"><span data-stu-id="18411-201">If any of these options are requested then they will be ignored.</span></span>

<span data-ttu-id="18411-202">Temporäre Tabellen unterstützen keine Standardwerte.</span><span class="sxs-lookup"><span data-stu-id="18411-202">Temporary tables do not support default values.</span></span> <span data-ttu-id="18411-203">Wenn eine Spaltendefinition bereitgestellt wird, die eine Standardwert Spezifikation enthält, wird diese Angabe ignoriert.</span><span class="sxs-lookup"><span data-stu-id="18411-203">If a column definition is provided that contains a default value specification then that specification will be ignored.</span></span>

<span data-ttu-id="18411-204">Temporäre Tabellen werden als Ergebnis vieler unterschiedlicher ESE-Funktionen an den Aufrufer zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="18411-204">Temporary tables are returned to the caller as a result of many different ESE functions.</span></span> <span data-ttu-id="18411-205">Beispielsweise gibt [jetgetindexinfo](./jetgetindexinfo-function.md) mit dem JET_IdxInfo Options Satz eine temporäre Tabelle zurück, die eine Liste aller Schlüssel Spalten in einem bestimmten Index enthält.</span><span class="sxs-lookup"><span data-stu-id="18411-205">For example, [JetGetIndexInfo](./jetgetindexinfo-function.md) with the JET_IdxInfo option set will return a temporary table containing a list of all the key columns in a given index.</span></span> <span data-ttu-id="18411-206">Die temporären Tabellen folgen den gleichen Lebenszyklus Regeln wie gewöhnliche temporäre Tabellen, wie hier beschrieben.</span><span class="sxs-lookup"><span data-stu-id="18411-206">The temporary tables follow the same lifecycle rules as ordinary temporary tables as described here.</span></span>

<span data-ttu-id="18411-207">Temporäre Tabellen werden auch intern von der Datenbank-Engine für viele Tasks verwendet.</span><span class="sxs-lookup"><span data-stu-id="18411-207">Temporary tables are also used internally by the database engine for many tasks.</span></span> <span data-ttu-id="18411-208">Die wichtigsten dieser Aufgaben sind die Erstellung eines Indexes für eine vorhandene Tabelle.</span><span class="sxs-lookup"><span data-stu-id="18411-208">The most important of these tasks is the creation of an index over an existing table.</span></span> <span data-ttu-id="18411-209">Eine temporäre Tabelle wird zum Sortieren der Index Schlüssel verwendet, die zum Erstellen dieses Indexes verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="18411-209">A temporary table will be used to sort the index keys that are used to construct that index.</span></span>

<span data-ttu-id="18411-210">Alle temporären Tabellen werden in der temporären Datenbank gespeichert.</span><span class="sxs-lookup"><span data-stu-id="18411-210">All temporary tables are stored in the temporary database.</span></span> <span data-ttu-id="18411-211">Die temporäre Datenbank ist eine spezielle Datenbankdatei, die während der Lebensdauer einer ESE-Instanz verwaltet wird und gelöscht wird, wenn diese Instanz heruntergefahren oder neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="18411-211">The temporary database is a special database file that is maintained during the lifetime of an ESE instance and is deleted when that instance is shut down or restarted.</span></span> <span data-ttu-id="18411-212">Der Speicherort der temporären Datenbank kann mithilfe von [jetsetsystemparameter](./jetsetsystemparameter-function.md) mit [JET_paramTempPath](./temporary-database-parameters.md)konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="18411-212">The location of the temporary database can be configured using [JetSetSystemParameter](./jetsetsystemparameter-function.md) with [JET_paramTempPath](./temporary-database-parameters.md).</span></span> <span data-ttu-id="18411-213">Die Platzierung der temporären Datenbank auf dem Datenträger in Relation zu den Transaktionsprotokoll Dateien und Datenbankdateien ist möglicherweise wichtig, wenn die Anwendung temporäre Tabellen stark nutzt oder häufig Indizes erstellt.</span><span class="sxs-lookup"><span data-stu-id="18411-213">Placement of the temporary database on disk relative to your transaction log files and database files may be important if your application makes heavy use of temporary tables or creates indexes frequently.</span></span>

<span data-ttu-id="18411-214">Der Lebenszyklus einer temporären Tabelle ist an die Cursor gebunden, die auf diese Tabelle verweisen.</span><span class="sxs-lookup"><span data-stu-id="18411-214">The lifecycle of a temporary table is tied to the cursors that reference it.</span></span> <span data-ttu-id="18411-215">Wenn alle Cursor, die auf eine temporäre Tabelle verweisen, entweder implizit oder explizit geschlossen werden, wird die temporäre Tabelle gelöscht.</span><span class="sxs-lookup"><span data-stu-id="18411-215">If all the cursors that reference a temporary table are closed, either implicitly or explicitly, then the temporary table will be deleted.</span></span> <span data-ttu-id="18411-216">Wenn eine temporäre Tabelle innerhalb einer Transaktion erstellt wird und anschließend ein Rollback für diese Transaktion ausgeführt wird, wird die temporäre Tabelle gelöscht, da alle Cursor, auf die Sie zu diesem Zeitpunkt verwiesen hat, implizit geschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="18411-216">If a temporary table is created inside a transaction and that transaction is subsequently rolled back then the temporary table will be deleted because any cursors that referenced it at this time will be implicitly closed.</span></span> <span data-ttu-id="18411-217">Neue Cursor können nur durch die Verwendung von [jetdupcursor](./jetdupcursor-function.md)auf eine temporäre Tabelle verweisen.</span><span class="sxs-lookup"><span data-stu-id="18411-217">New cursors can reference a temporary table only through the use of [JetDupCursor](./jetdupcursor-function.md).</span></span> <span data-ttu-id="18411-218">In diesem Fall werden die neuen Cursor auf dem ersten Index Eintrag der temporären Tabelle positioniert.</span><span class="sxs-lookup"><span data-stu-id="18411-218">In this case, the new cursors will be positioned on the first index entry of the temporary table.</span></span> <span data-ttu-id="18411-219">[Jetdupcursor](./jetdupcursor-function.md) funktioniert nur in bestimmten Phasen der Verwendung für die temporäre Tabelle.</span><span class="sxs-lookup"><span data-stu-id="18411-219">[JetDupCursor](./jetdupcursor-function.md) will only work during certain phases of use for the temporary table.</span></span> <span data-ttu-id="18411-220">Weitere Informationen finden Sie in den Hinweisen zu den Cursor Funktionen für temporäre Tabellen.</span><span class="sxs-lookup"><span data-stu-id="18411-220">See the remarks concerning temporary table cursor capabilities for more information.</span></span> <span data-ttu-id="18411-221">Es ist nicht möglich, auf eine temporäre Tabelle von mehreren Sitzungen gleichzeitig zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="18411-221">It is not possible to reference a temporary table from more than one session at a time.</span></span>

<span data-ttu-id="18411-222">**Vorsicht**  In [jetdupcursor](./jetdupcursor-function.md) liegt ein wichtiges Problem vor, das sich auf temporäre Tabellen auswirkt.</span><span class="sxs-lookup"><span data-stu-id="18411-222">**Caution**  There is an important problem in [JetDupCursor](./jetdupcursor-function.md) that affects temporary tables.</span></span> <span data-ttu-id="18411-223">Wenn versucht wird, eine temporäre Tabelle zu duplizieren, die sich im vorwärts Modus befindet, wird der resultierende Cursor nicht ordnungsgemäß erstellt und funktioniert nicht.</span><span class="sxs-lookup"><span data-stu-id="18411-223">If an attempt is made to duplicate a temporary table that is in forward-only mode then the resulting cursor will not be created properly and will malfunction.</span></span> <span data-ttu-id="18411-224">Es ist immer noch sicher, einen Cursor über eine materialisierte temporäre Tabelle zu duplizieren.</span><span class="sxs-lookup"><span data-stu-id="18411-224">It is still safe to duplicate a cursor over a materialized temporary table.</span></span>

<span data-ttu-id="18411-225">Der temporäre Tabellen-Manager kann auf drei Arten eine temporäre Tabelle implementieren.</span><span class="sxs-lookup"><span data-stu-id="18411-225">The temporary table manager can implement a temporary table in three ways.</span></span> <span data-ttu-id="18411-226">Die erste Methode besteht darin, eine in-Memory-Tabelle beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="18411-226">The first method is to maintain an in-memory table.</span></span> <span data-ttu-id="18411-227">Diese Strategie ist der schnellste, kann aber nur für kleine, einfache, temporäre Tabellen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="18411-227">This strategy is the fastest but can only be used for small, simple, temporary tables.</span></span> <span data-ttu-id="18411-228">Die zweite Methode besteht darin, eine Datenträger basierte Sortierung zu erstellen, die mit einem vorwärts-Iterator gesteuert werden kann.</span><span class="sxs-lookup"><span data-stu-id="18411-228">The second method is to create a disk-based sort that can be driven using a forward-only iterator.</span></span> <span data-ttu-id="18411-229">Diese Strategie kann nur unter bestimmten Umständen verwendet werden und ist die schnellste Möglichkeit, Duplikate aus einem sehr großen Dataset zu sortieren und zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="18411-229">This strategy can only be used under certain circumstances and is the fastest way to sort and remove duplicates from a very large data set.</span></span> <span data-ttu-id="18411-230">Die dritte Methode ist das Erstellen einer B +-Struktur in der temporären Datenbank, um die temporäre Tabelle zu speichern.</span><span class="sxs-lookup"><span data-stu-id="18411-230">The third method is to create a B+ Tree in the temporary database to hold the temporary table.</span></span> <span data-ttu-id="18411-231">Diese Strategie ist die langsamste, aber die vielseitigste und wird als materialisierte temporäre Tabelle bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="18411-231">This strategy is the slowest, but the most versatile, and is referred to as a materialized temporary table.</span></span> <span data-ttu-id="18411-232">Diese Strategien können in Kombination verwendet werden, um letztendlich die Funktionalität zu erreichen, die für die temporäre Tabelle angefordert wird.</span><span class="sxs-lookup"><span data-stu-id="18411-232">These strategies can be used in combination to ultimately achieve the functionality that is requested of the temporary table.</span></span>

<span data-ttu-id="18411-233">Wenn die temporäre Tabelle nicht materialisiert ist, wird Sie in erster Linie in zwei Hauptphasen verwendet.</span><span class="sxs-lookup"><span data-stu-id="18411-233">When the temporary table is not materialized then it is used primarily in two major phases.</span></span> <span data-ttu-id="18411-234">Die erste Phase ist die Einfügungs Phase, in der die Tabelle mit dem ersten DataSet aufgefüllt wird.</span><span class="sxs-lookup"><span data-stu-id="18411-234">The first phase is the insertion phase where the table is populated with its initial data set.</span></span> <span data-ttu-id="18411-235">In dieser Phase ist nur die Daten Einfügung zulässig.</span><span class="sxs-lookup"><span data-stu-id="18411-235">During this phase, only data insertion is allowed.</span></span> <span data-ttu-id="18411-236">Diese Phase endet, wenn versucht wird, den Cursor mithilfe von [jetmove](./jetmove-function.md) oder [JetSeek](./jetseek-function.md)zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="18411-236">This phase ends when an attempt is made to move the cursor using [JetMove](./jetmove-function.md) or [JetSeek](./jetseek-function.md).</span></span> <span data-ttu-id="18411-237">Die zweite Phase ist die Daten Extraktions Phase.</span><span class="sxs-lookup"><span data-stu-id="18411-237">The second phase is the data extraction phase.</span></span> <span data-ttu-id="18411-238">In dieser Phase können die in der temporären Tabelle gespeicherten Daten anhand der Funktionen extrahiert werden, die beim Erstellen der temporären Tabelle angefordert wurden.</span><span class="sxs-lookup"><span data-stu-id="18411-238">During this phase, the data that is stored in the temporary table can be extracted according to the capabilities that were requested when the temporary table was created.</span></span>

<span data-ttu-id="18411-239">**Cursor Funktionen für temporäre Tabellen**</span><span class="sxs-lookup"><span data-stu-id="18411-239">**Temporary Table Cursor Capabilities**</span></span>

<span data-ttu-id="18411-240">Wenn die temporäre Tabelle materialisiert ist, verfügt der Cursor über die folgenden Funktionen, kann jedoch durch die angeforderten Optionen weiter eingeschränkt werden:</span><span class="sxs-lookup"><span data-stu-id="18411-240">When the temporary table is materialized, the cursor has the following capabilities but might be further limited by the options that are requested:</span></span>

  - [<span data-ttu-id="18411-241">Jetclosetable</span><span class="sxs-lookup"><span data-stu-id="18411-241">JetCloseTable</span></span>](./jetclosetable-function.md)

  - [<span data-ttu-id="18411-242">Jetdelete</span><span class="sxs-lookup"><span data-stu-id="18411-242">JetDelete</span></span>](./jetdelete-function.md)

  - [<span data-ttu-id="18411-243">Jetdupcursor</span><span class="sxs-lookup"><span data-stu-id="18411-243">JetDupCursor</span></span>](./jetdupcursor-function.md)

  - [<span data-ttu-id="18411-244">Jetenreeratecolumschlag</span><span class="sxs-lookup"><span data-stu-id="18411-244">JetEnumerateColumns</span></span>](./jetenumeratecolumns-function.md)

  - [<span data-ttu-id="18411-245">Jetescrowupdate</span><span class="sxs-lookup"><span data-stu-id="18411-245">JetEscrowUpdate</span></span>](./jetescrowupdate-function.md)

  - [<span data-ttu-id="18411-246">Jetgetbookmark</span><span class="sxs-lookup"><span data-stu-id="18411-246">JetGetBookmark</span></span>](./jetgetbookmark-function.md)

  - [<span data-ttu-id="18411-247">Jetgetcursor Info</span><span class="sxs-lookup"><span data-stu-id="18411-247">JetGetCursorInfo</span></span>](./jetgetcursorinfo-function.md)

  - [<span data-ttu-id="18411-248">Jetgetls</span><span class="sxs-lookup"><span data-stu-id="18411-248">JetGetLS</span></span>](./jetgetls-function.md)

  - [<span data-ttu-id="18411-249">Jetgetrecordsize</span><span class="sxs-lookup"><span data-stu-id="18411-249">JetGetRecordSize</span></span>](./jetgetrecordsize-function.md)

  - [<span data-ttu-id="18411-250">Jetgettableinfo</span><span class="sxs-lookup"><span data-stu-id="18411-250">JetGetTableInfo</span></span>](./jetgettableinfo-function.md)

  - [<span data-ttu-id="18411-251">Jetgojebookmark</span><span class="sxs-lookup"><span data-stu-id="18411-251">JetGotoBookmark</span></span>](./jetgotobookmark-function.md)

  - [<span data-ttu-id="18411-252">Jetmakekey</span><span class="sxs-lookup"><span data-stu-id="18411-252">JetMakeKey</span></span>](./jetmakekey-function.md)

  - [<span data-ttu-id="18411-253">Jetmove</span><span class="sxs-lookup"><span data-stu-id="18411-253">JetMove</span></span>](./jetmove-function.md)

  - [<span data-ttu-id="18411-254">Jetprepareupdate</span><span class="sxs-lookup"><span data-stu-id="18411-254">JetPrepareUpdate</span></span>](./jetprepareupdate-function.md)

  - [<span data-ttu-id="18411-255">Jetretrievecolumschlag</span><span class="sxs-lookup"><span data-stu-id="18411-255">JetRetrieveColumn</span></span>](./jetretrievecolumn-function.md)

  - [<span data-ttu-id="18411-256">Jetretrievecolumschlag</span><span class="sxs-lookup"><span data-stu-id="18411-256">JetRetrieveColumns</span></span>](./jetretrievecolumns-function.md)

  - [<span data-ttu-id="18411-257">Jetretrievekey</span><span class="sxs-lookup"><span data-stu-id="18411-257">JetRetrieveKey</span></span>](./jetretrievekey-function.md)

  - [<span data-ttu-id="18411-258">JetSeek</span><span class="sxs-lookup"><span data-stu-id="18411-258">JetSeek</span></span>](./jetseek-function.md)

  - [<span data-ttu-id="18411-259">Jetsetcolumn</span><span class="sxs-lookup"><span data-stu-id="18411-259">JetSetColumn</span></span>](./jetsetcolumn-function.md)

  - [<span data-ttu-id="18411-260">Jetsetcolumns</span><span class="sxs-lookup"><span data-stu-id="18411-260">JetSetColumns</span></span>](./jetsetcolumns-function.md)

  - [<span data-ttu-id="18411-261">Jetsetindexrange</span><span class="sxs-lookup"><span data-stu-id="18411-261">JetSetIndexRange</span></span>](./jetsetindexrange-function.md)

  - [<span data-ttu-id="18411-262">Jetsetls</span><span class="sxs-lookup"><span data-stu-id="18411-262">JetSetLS</span></span>](./jetsetls-function.md)

  - [<span data-ttu-id="18411-263">Jetupdate</span><span class="sxs-lookup"><span data-stu-id="18411-263">JetUpdate</span></span>](./jetupdate-function.md)

<span data-ttu-id="18411-264">Wenn die temporäre Tabelle nicht materialisiert ist und sich in der einfügephase befindet, verfügt der Cursor über die folgenden Funktionen, kann jedoch durch die angeforderten Optionen weiter eingeschränkt werden:</span><span class="sxs-lookup"><span data-stu-id="18411-264">When the temporary table is not materialized and is in the insert phase, the cursor has the following capabilities but might be further limited by the options that are requested:</span></span>

  - [<span data-ttu-id="18411-265">Jetclosetable</span><span class="sxs-lookup"><span data-stu-id="18411-265">JetCloseTable</span></span>](./jetclosetable-function.md)

  - [<span data-ttu-id="18411-266">Jetescrowupdate</span><span class="sxs-lookup"><span data-stu-id="18411-266">JetEscrowUpdate</span></span>](./jetescrowupdate-function.md)

  - [<span data-ttu-id="18411-267">Jetmakekey</span><span class="sxs-lookup"><span data-stu-id="18411-267">JetMakeKey</span></span>](./jetmakekey-function.md)

  - [<span data-ttu-id="18411-268">Jetmove</span><span class="sxs-lookup"><span data-stu-id="18411-268">JetMove</span></span>](./jetmove-function.md)
    
    <span data-ttu-id="18411-269">**Hinweis**  Bewirkt einen Übergang zur Extrahierungs Phase.</span><span class="sxs-lookup"><span data-stu-id="18411-269">**Note**  Causes transition to the extract phase.</span></span>

  - [<span data-ttu-id="18411-270">Jetprepareupdate</span><span class="sxs-lookup"><span data-stu-id="18411-270">JetPrepareUpdate</span></span>](./jetprepareupdate-function.md)

  - [<span data-ttu-id="18411-271">Jetretrievekey</span><span class="sxs-lookup"><span data-stu-id="18411-271">JetRetrieveKey</span></span>](./jetretrievekey-function.md)

  - [<span data-ttu-id="18411-272">JetSeek</span><span class="sxs-lookup"><span data-stu-id="18411-272">JetSeek</span></span>](./jetseek-function.md)
    
    <span data-ttu-id="18411-273">**Hinweis**  Bewirkt einen Übergang zur Extrahierungs Phase.</span><span class="sxs-lookup"><span data-stu-id="18411-273">**Note**  Causes transition to the extract phase.</span></span>

  - [<span data-ttu-id="18411-274">Jetsetcolumn</span><span class="sxs-lookup"><span data-stu-id="18411-274">JetSetColumn</span></span>](./jetsetcolumn-function.md)

  - [<span data-ttu-id="18411-275">Jetsetcolumns</span><span class="sxs-lookup"><span data-stu-id="18411-275">JetSetColumns</span></span>](./jetsetcolumns-function.md)

  - [<span data-ttu-id="18411-276">Jetupdate</span><span class="sxs-lookup"><span data-stu-id="18411-276">JetUpdate</span></span>](./jetupdate-function.md)

<span data-ttu-id="18411-277">Wenn die temporäre Tabelle nicht materialisiert wird und sich in der Extrahierungs Phase befindet, verfügt der Cursor über die folgenden Funktionen, kann jedoch durch die angeforderten Optionen weiter eingeschränkt werden:</span><span class="sxs-lookup"><span data-stu-id="18411-277">When the temporary table is not materialized and is in the extract phase, the cursor has the following capabilities but may be further limited by the options that are requested:</span></span>

  - [<span data-ttu-id="18411-278">Jetclosetable</span><span class="sxs-lookup"><span data-stu-id="18411-278">JetCloseTable</span></span>](./jetclosetable-function.md)

  - [<span data-ttu-id="18411-279">Jetdupcursor</span><span class="sxs-lookup"><span data-stu-id="18411-279">JetDupCursor</span></span>](./jetdupcursor-function.md)
    
    <span data-ttu-id="18411-280">**Hinweis**  Wenn versucht wird, eine temporäre Tabelle zu duplizieren, die sich im vorwärts Modus befindet, wird der resultierende Cursor nicht ordnungsgemäß erstellt und funktioniert nicht.</span><span class="sxs-lookup"><span data-stu-id="18411-280">**Note**  If an attempt is made to duplicate a temporary table that is in forward-only mode then the resulting cursor will not be created properly and will malfunction.</span></span> <span data-ttu-id="18411-281">Es ist immer noch sicher, einen Cursor über eine materialisierte temporäre Tabelle zu duplizieren.</span><span class="sxs-lookup"><span data-stu-id="18411-281">It is still safe to duplicate a cursor over a materialized temporary table.</span></span>

  - [<span data-ttu-id="18411-282">Jetenreeratecolumschlag</span><span class="sxs-lookup"><span data-stu-id="18411-282">JetEnumerateColumns</span></span>](./jetenumeratecolumns-function.md)

  - [<span data-ttu-id="18411-283">Jetgetbookmark</span><span class="sxs-lookup"><span data-stu-id="18411-283">JetGetBookmark</span></span>](./jetgetbookmark-function.md)

  - [<span data-ttu-id="18411-284">Jetgetls</span><span class="sxs-lookup"><span data-stu-id="18411-284">JetGetLS</span></span>](./jetgetls-function.md)

  - [<span data-ttu-id="18411-285">Jetgetrecordsize</span><span class="sxs-lookup"><span data-stu-id="18411-285">JetGetRecordSize</span></span>](./jetgetrecordsize-function.md)

  - [<span data-ttu-id="18411-286">Jetgettableinfo</span><span class="sxs-lookup"><span data-stu-id="18411-286">JetGetTableInfo</span></span>](./jetgettableinfo-function.md)

  - [<span data-ttu-id="18411-287">Jetgojebookmark</span><span class="sxs-lookup"><span data-stu-id="18411-287">JetGotoBookmark</span></span>](./jetgotobookmark-function.md)

  - [<span data-ttu-id="18411-288">Jetmakekey</span><span class="sxs-lookup"><span data-stu-id="18411-288">JetMakeKey</span></span>](./jetmakekey-function.md)

  - [<span data-ttu-id="18411-289">Jetmove</span><span class="sxs-lookup"><span data-stu-id="18411-289">JetMove</span></span>](./jetmove-function.md)

  - [<span data-ttu-id="18411-290">Jetretrievecolumschlag</span><span class="sxs-lookup"><span data-stu-id="18411-290">JetRetrieveColumn</span></span>](./jetretrievecolumn-function.md)

  - [<span data-ttu-id="18411-291">Jetretrievecolumschlag</span><span class="sxs-lookup"><span data-stu-id="18411-291">JetRetrieveColumns</span></span>](./jetretrievecolumns-function.md)

  - [<span data-ttu-id="18411-292">Jetretrievekey</span><span class="sxs-lookup"><span data-stu-id="18411-292">JetRetrieveKey</span></span>](./jetretrievekey-function.md)

  - [<span data-ttu-id="18411-293">JetSeek</span><span class="sxs-lookup"><span data-stu-id="18411-293">JetSeek</span></span>](./jetseek-function.md)

  - [<span data-ttu-id="18411-294">Jetsetindexrange</span><span class="sxs-lookup"><span data-stu-id="18411-294">JetSetIndexRange</span></span>](./jetsetindexrange-function.md)

  - [<span data-ttu-id="18411-295">Jetsetls</span><span class="sxs-lookup"><span data-stu-id="18411-295">JetSetLS</span></span>](./jetsetls-function.md)

#### <a name="requirements"></a><span data-ttu-id="18411-296">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="18411-296">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="18411-297"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="18411-297"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="18411-298">Erfordert Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="18411-298">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18411-299"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="18411-299"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="18411-300">Erfordert Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="18411-300">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="18411-301"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="18411-301"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="18411-302">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="18411-302">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18411-303"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="18411-303"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="18411-304">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="18411-304">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="18411-305"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="18411-305"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="18411-306">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="18411-306">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="18411-307">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="18411-307">See Also</span></span>

[<span data-ttu-id="18411-308">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="18411-308">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="18411-309">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="18411-309">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="18411-310">JET_OPENTEMPORARYTABLE</span><span class="sxs-lookup"><span data-stu-id="18411-310">JET_OPENTEMPORARYTABLE</span></span>](./jet-opentemporarytable-structure.md)  
[<span data-ttu-id="18411-311">Jetclosetable</span><span class="sxs-lookup"><span data-stu-id="18411-311">JetCloseTable</span></span>](./jetclosetable-function.md)  
[<span data-ttu-id="18411-312">Jetkreatetablecolumnindex</span><span class="sxs-lookup"><span data-stu-id="18411-312">JetCreateTableColumnIndex</span></span>](./jetcreatetablecolumnindex-function.md)  
[<span data-ttu-id="18411-313">Jetdupcursor</span><span class="sxs-lookup"><span data-stu-id="18411-313">JetDupCursor</span></span>](./jetdupcursor-function.md)  
[<span data-ttu-id="18411-314">Jetmove</span><span class="sxs-lookup"><span data-stu-id="18411-314">JetMove</span></span>](./jetmove-function.md)  
[<span data-ttu-id="18411-315">Jetrollback</span><span class="sxs-lookup"><span data-stu-id="18411-315">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="18411-316">JetSeek</span><span class="sxs-lookup"><span data-stu-id="18411-316">JetSeek</span></span>](./jetseek-function.md)  
[<span data-ttu-id="18411-317">Jetsetsystemparameter</span><span class="sxs-lookup"><span data-stu-id="18411-317">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="18411-318">Informations Parameter</span><span class="sxs-lookup"><span data-stu-id="18411-318">Informational Parameters</span></span>](./informational-parameters.md)  
[<span data-ttu-id="18411-319">Temporäre Daten Bank Parameter</span><span class="sxs-lookup"><span data-stu-id="18411-319">Temporary Database Parameters</span></span>](./temporary-database-parameters.md)
