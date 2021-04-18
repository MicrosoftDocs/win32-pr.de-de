---
description: 'Weitere Informationen finden Sie hier: JetSetCurrentIndex2-Funktion'
title: JetSetCurrentIndex2-Funktion
TOCTitle: JetSetCurrentIndex2 Function
ms:assetid: da94465e-bd35-45c2-9ccc-1d2e8c34aa9a
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294110(v=EXCHG.10)
ms:contentKeyID: 32765725
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetCurrentIndex2W
- JetSetCurrentIndex2A
- JetSetCurrentIndex2
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2c95e665b549fff82e0beaaca9682329217ebb0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345470"
---
# <a name="jetsetcurrentindex2-function"></a><span data-ttu-id="9866e-103">JetSetCurrentIndex2-Funktion</span><span class="sxs-lookup"><span data-stu-id="9866e-103">JetSetCurrentIndex2 Function</span></span>


<span data-ttu-id="9866e-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="9866e-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetsetcurrentindex2-function"></a><span data-ttu-id="9866e-105">JetSetCurrentIndex2-Funktion</span><span class="sxs-lookup"><span data-stu-id="9866e-105">JetSetCurrentIndex2 Function</span></span>

<span data-ttu-id="9866e-106">Die **JetSetCurrentIndex2** -Funktion legt den aktuellen Index eines Cursors fest, der definiert, welche Datensätze in einer Tabelle für diesen Cursor sichtbar sind, und die Reihenfolge, in der Sie angezeigt werden, indem Sie den Satz von Indexeinträgen auswählen, der zum verfügbar machen dieser Datensätze verwendet wird</span><span class="sxs-lookup"><span data-stu-id="9866e-106">The **JetSetCurrentIndex2** function sets the current index of a cursor that defines which records in a table are visible to that cursor and the order in which they appear by selecting the set of index entries to use to expose those records.</span></span>

```cpp
    JET_ERR JET_API JetSetCurrentIndex2(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in_opt      JET_PCSTR szIndexName,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="9866e-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="9866e-107">Parameters</span></span>

<span data-ttu-id="9866e-108">*-sid*</span><span class="sxs-lookup"><span data-stu-id="9866e-108">*sesid*</span></span>

<span data-ttu-id="9866e-109">Die Sitzung, die für diesen-Befehl verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="9866e-109">The session to use for this call.</span></span>

<span data-ttu-id="9866e-110">*TableID*</span><span class="sxs-lookup"><span data-stu-id="9866e-110">*tableid*</span></span>

<span data-ttu-id="9866e-111">Der Cursor, der für diesen-Befehl verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="9866e-111">The cursor to use for this call.</span></span>

<span data-ttu-id="9866e-112">*szindexname*</span><span class="sxs-lookup"><span data-stu-id="9866e-112">*szIndexName*</span></span>

<span data-ttu-id="9866e-113">Der Name des Indexes, der für den Cursor ausgewählt werden soll.</span><span class="sxs-lookup"><span data-stu-id="9866e-113">The name of the index to be selected for the cursor.</span></span>

<span data-ttu-id="9866e-114">Wenn dieser Parameter NULL oder eine leere Zeichenfolge ist, wird der gruppierte Index ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="9866e-114">If this parameter is NULL or an empty string then the clustered index will be selected.</span></span> <span data-ttu-id="9866e-115">Wenn ein primärer Index für die Tabelle definiert ist, wird dieser Index ausgewählt, da er mit dem gruppierten Index identisch ist.</span><span class="sxs-lookup"><span data-stu-id="9866e-115">If a primary index is defined for the table then that index will be selected because it is the same as the clustered index.</span></span> <span data-ttu-id="9866e-116">Wenn kein primärer Index für die Tabelle definiert ist, wird der sequenzielle Index ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="9866e-116">If no primary index is defined for the table then the sequential index will be selected.</span></span> <span data-ttu-id="9866e-117">Der sequenzielle Index hat keine Index Definition.</span><span class="sxs-lookup"><span data-stu-id="9866e-117">The sequential index has no index definition.</span></span> <span data-ttu-id="9866e-118">Weitere Informationen finden Sie unter [jetkreateindex](./jetcreateindex-function.md) .</span><span class="sxs-lookup"><span data-stu-id="9866e-118">See [JetCreateIndex](./jetcreateindex-function.md) for more information.</span></span>

<span data-ttu-id="9866e-119">Wenn *pIndexID* nicht NULL ist, wird der Indexname ignoriert, und der Index wird durch die Index-ID ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="9866e-119">If *pindexid* is not NULL then the index name will be ignored and the index will be selected by its index ID.</span></span>

<span data-ttu-id="9866e-120">*grbit*</span><span class="sxs-lookup"><span data-stu-id="9866e-120">*grbit*</span></span>

<span data-ttu-id="9866e-121">Eine Gruppe von Bits, die die für diesen-Befehl zu verwendenden Optionen enthalten, die NULL oder mehr der folgenden Elemente enthalten.</span><span class="sxs-lookup"><span data-stu-id="9866e-121">A group of bits that contain the options to be used for this call, which include zero or more of the following.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9866e-122">Wert</span><span class="sxs-lookup"><span data-stu-id="9866e-122">Value</span></span></p></th>
<th><p><span data-ttu-id="9866e-123">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="9866e-123">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9866e-124">JET_bitMoveFirst</span><span class="sxs-lookup"><span data-stu-id="9866e-124">JET_bitMoveFirst</span></span></p></td>
<td><p><span data-ttu-id="9866e-125">Diese Option gibt an, dass der Cursor auf dem ersten Eintrag des angegebenen Indexes positioniert werden soll.</span><span class="sxs-lookup"><span data-stu-id="9866e-125">This option indicates that the cursor should be positioned on the first entry of the specified index.</span></span> <span data-ttu-id="9866e-126">Wenn der gruppierte Index ausgewählt wird (primärer Index oder sequenzieller Index) und der aktuelle Index ein sekundärer Index ist, wird JET_bitMoveFirst angenommen.</span><span class="sxs-lookup"><span data-stu-id="9866e-126">If the clustered index is being selected (primary index or sequential index) and the current index is a secondary index then JET_bitMoveFirst is assumed.</span></span> <span data-ttu-id="9866e-127">Wenn der aktuelle Index ausgewählt wird, wird diese Option ignoriert, und es erfolgt keine Änderung an der Cursorposition.</span><span class="sxs-lookup"><span data-stu-id="9866e-127">If the current index is being selected then this option is ignored and no change to the cursor position is made.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9866e-128">JET_bitNoMove</span><span class="sxs-lookup"><span data-stu-id="9866e-128">JET_bitNoMove</span></span></p></td>
<td><p><span data-ttu-id="9866e-129">Diese Option gibt an, dass der Cursor auf dem Index Eintrag des neuen Indexes positioniert werden soll, der dem Datensatz entspricht, der mit dem Index Eintrag an der aktuellen Position des Cursors auf dem alten Index verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="9866e-129">This option indicates that the cursor should be positioned on the index entry of the new index that corresponds to the record associated with the index entry at the current position of the cursor on the old index.</span></span></p>
<p><span data-ttu-id="9866e-130">Wenn die Definition für den neuen Index mindestens eine mehrwertige Schlüssel Spalte enthält, ist der Ziel Index Eintrag mehrdeutig.</span><span class="sxs-lookup"><span data-stu-id="9866e-130">If the definition for the new index contains at least one multi-valued key column then the destination index entry is ambiguous.</span></span> <span data-ttu-id="9866e-131">In diesem Fall wird die angegebene <em>itagsequence</em> verwendet, um auszuwählen, welcher mehrwertige Wert der signifikantesten mehrwertigen Schlüssel Spalte zum Positionieren des Cursors verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9866e-131">In this case, the specified <em>itagSequence</em> is used to select which multi-value of the most significant multi-valued key column is used to position the cursor.</span></span> <span data-ttu-id="9866e-132">Es ist nur notwendig, eine einzelne <em>itagsequence</em> zu übergeben, auch wenn es mehrere mehrwertige Schlüssel Spalten gibt, da die Engine nur alle Werte für die signifikanteste mehrwertige Schlüssel Spalte erweitert.</span><span class="sxs-lookup"><span data-stu-id="9866e-132">It is only necessary to pass a single <em>itagSequence</em> even in the case of multiple multi-valued key columns because the engine only expands all values for the most significant multi-valued key column.</span></span> <span data-ttu-id="9866e-133">Weitere Informationen finden Sie unter <a href="gg294099(v=exchg.10).md">jetkreateingedex</a> .</span><span class="sxs-lookup"><span data-stu-id="9866e-133">See <a href="gg294099(v=exchg.10).md">JetCreateIndex</a> for more details.</span></span></p>
<p><span data-ttu-id="9866e-134">Wenn JET_bitMoveFirst angegeben wird, wird diese Option ignoriert.</span><span class="sxs-lookup"><span data-stu-id="9866e-134">If JET_bitMoveFirst is specified then this option is ignored.</span></span></p>
<p><span data-ttu-id="9866e-135">Wenn der aktuelle Index ausgewählt wird, wird diese Option ignoriert, und es erfolgt keine Änderung an der Cursorposition.</span><span class="sxs-lookup"><span data-stu-id="9866e-135">If the current index is being selected then this option is ignored and no change to the cursor position is made.</span></span> <span data-ttu-id="9866e-136">Wenn dieser Parameter nicht vorhanden ist, wird davon ausgegangen, dass sein Wert JET_bitMoveFirst wird.</span><span class="sxs-lookup"><span data-stu-id="9866e-136">When this parameter is not present, its value is presumed to be JET_bitMoveFirst.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="9866e-137">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9866e-137">Return Value</span></span>

<span data-ttu-id="9866e-138">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="9866e-138">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="9866e-139">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="9866e-139">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9866e-140">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="9866e-140">Return code</span></span></p></th>
<th><p><span data-ttu-id="9866e-141">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9866e-141">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9866e-142">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="9866e-142">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="9866e-143">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="9866e-143">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9866e-144">JET_errBadItagSequence</span><span class="sxs-lookup"><span data-stu-id="9866e-144">JET_errBadItagSequence</span></span></p></td>
<td><p><span data-ttu-id="9866e-145">Ein sekundärer Index wird mit der JET_bitNoMove-Option ausgewählt, und es gibt keinen Wert für die erste mehrwertige Schlüssel Spalte in der neuen Definition für den Index, der der angegebenen Sequenznummer entspricht.</span><span class="sxs-lookup"><span data-stu-id="9866e-145">A secondary index is being selected with the JET_bitNoMove option and there is no value for the first multi-valued key column in the new definition for the index that corresponds to the specified sequence number.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9866e-146">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="9866e-146">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="9866e-147">Der Vorgang kann nicht ausgeführt werden, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufens von <a href="gg269240(v=exchg.10).md">jetstopservice</a>beendet wurden.</span><span class="sxs-lookup"><span data-stu-id="9866e-147">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9866e-148">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="9866e-148">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="9866e-149">Der Vorgang kann nicht ausgeführt werden, da bei der der Sitzung zugeordneten Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität der Daten zu schützen.</span><span class="sxs-lookup"><span data-stu-id="9866e-149">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="9866e-150">Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9866e-150">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9866e-151">JET_errInvalidIndexId</span><span class="sxs-lookup"><span data-stu-id="9866e-151">JET_errInvalidIndexId</span></span></p></td>
<td><p><span data-ttu-id="9866e-152">Der Inhalt der Index-ID war ungültig oder abgelaufen und muss aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="9866e-152">The contents of the index ID were not valid or have expired and need to be refreshed.</span></span> <span data-ttu-id="9866e-153">Dies kann für <strong>JetSetCurrentIndex2</strong> vorkommen, wenn:</span><span class="sxs-lookup"><span data-stu-id="9866e-153">This can happen for <strong>JetSetCurrentIndex2</strong> when:</span></span></p>
<ul>
<li><p><span data-ttu-id="9866e-154">pIndexID- &gt; cbStruct weist nicht die erwartete Größe auf (Windows Server 2003 und spätere Releases).</span><span class="sxs-lookup"><span data-stu-id="9866e-154">pindexid-&gt;cbStruct is not of the expected size (Windows Server 2003 and later releases).</span></span></p></li>
<li><p><span data-ttu-id="9866e-155">Die Engine wurde heruntergefahren, seit die Index-ID abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="9866e-155">The engine has been shut down since the index ID was fetched.</span></span></p></li>
<li><p><span data-ttu-id="9866e-156">Alle Cursor, die auf die Tabelle verweisen, die den Index enthält, der der Index-ID entspricht, wurden geschlossen, und die Engine hat die Definition für den Index aus dem Schema Cache entfernt.</span><span class="sxs-lookup"><span data-stu-id="9866e-156">All cursors referencing the table containing the index corresponding to the index ID have been closed and the engine has evicted the definition for the index from the schema cache.</span></span></p></li>
<li><p><span data-ttu-id="9866e-157">Die Index-ID wird mit einem Cursor verwendet, der für die falsche Tabelle geöffnet ist.</span><span class="sxs-lookup"><span data-stu-id="9866e-157">The index ID is being used with a cursor opened on the wrong table.</span></span></p></li>
<li><p><span data-ttu-id="9866e-158">Der Index wurde gelöscht oder ist für die Sitzung noch nicht sichtbar.</span><span class="sxs-lookup"><span data-stu-id="9866e-158">The index has been dropped or is not yet visible to the session.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9866e-159">JET_errInvalidName</span><span class="sxs-lookup"><span data-stu-id="9866e-159">JET_errInvalidName</span></span></p></td>
<td><p><span data-ttu-id="9866e-160">Einer der angegebenen Objektnamen war ungültig.</span><span class="sxs-lookup"><span data-stu-id="9866e-160">One of the specified object names was invalid.</span></span> <span data-ttu-id="9866e-161">Alle Objektnamen müssen mit demselben Regelsatz übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="9866e-161">All object names must conform to the same set of rules.</span></span> <span data-ttu-id="9866e-162">Nachfolgend sind diese Regeln aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="9866e-162">These rules are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="9866e-163">Objektnamen müssen aus ASCII-Zeichen bestehen.</span><span class="sxs-lookup"><span data-stu-id="9866e-163">Object names must be composed of ASCII characters.</span></span></p></li>
<li><p><span data-ttu-id="9866e-164">Objektnamen müssen mindestens ein Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="9866e-164">Object names must be at least one character in length.</span></span></p></li>
<li><p><span data-ttu-id="9866e-165">Objektnamen dürfen nicht mehr als JET_cbNameMost (64) Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="9866e-165">Object names may not exceed JET_cbNameMost (64) characters in length.</span></span></p></li>
<li><p><span data-ttu-id="9866e-166">Objektnamen dürfen nicht mit einem Leerzeichen beginnen.</span><span class="sxs-lookup"><span data-stu-id="9866e-166">Object names may not begin with a space.</span></span></p></li>
<li><p><span data-ttu-id="9866e-167">Objektnamen dürfen keine ASCII-Steuerzeichen (0x00 bis 0x1F) enthalten.</span><span class="sxs-lookup"><span data-stu-id="9866e-167">Object names may not contain ASCII control characters (0x00 through 0x1F).</span></span></p></li>
<li><p><span data-ttu-id="9866e-168">Objektnamen dürfen keine Ausrufezeichen (!), Punkte (.), linke eckige Klammer ([) oder rechte eckige Klammer (]) enthalten.</span><span class="sxs-lookup"><span data-stu-id="9866e-168">Object names may not contain an exclamation point (!), period (.), left bracket ([), or right bracket (]) character.</span></span></p></li>
<li><p><span data-ttu-id="9866e-169">Nach der Validierung wird nur der Teil der Zeichenfolge bis zum ersten Leerzeichen (sofern vorhanden) für den Objektnamen verwendet.</span><span class="sxs-lookup"><span data-stu-id="9866e-169">Once validated, only the portion of the string up to the first space (if any) will be used for the object name.</span></span> <span data-ttu-id="9866e-170">Dies bedeutet, dass Objektnamen keine Leerzeichen enthalten dürfen.</span><span class="sxs-lookup"><span data-stu-id="9866e-170">This effectively means that object names may not contain a space either.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9866e-171">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="9866e-171">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="9866e-172">Einer der angegebenen Parameter enthielt einen unerwarteten Wert oder enthielt einen Wert, der nicht sinnvoll war, wenn er mit dem Wert eines anderen Parameters kombiniert wurde.</span><span class="sxs-lookup"><span data-stu-id="9866e-172">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="9866e-173">Dies kann bei <strong>JetSetCurrentIndex2</strong> vorkommen, wenn <em>pIndexID</em> nicht NULL ist und pIndexID- &gt; cbStruct nicht die erwartete Größe aufweist (Windows XP und frühere Versionen).</span><span class="sxs-lookup"><span data-stu-id="9866e-173">This can happen for <strong>JetSetCurrentIndex2</strong> when <em>pindexid</em> is not NULL and pindexid-&gt;cbStruct is not of the expected size (Windows XP and earlier releases).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9866e-174">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="9866e-174">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="9866e-175">Ein sekundärer Index wird mit der JET_bitNoMove-Option ausgewählt, und es gibt keinen Index Eintrag im neuen Index, der dem Datensatz entspricht, der mit dem Index Eintrag an der aktuellen Position des Cursors auf dem alten Index verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="9866e-175">A secondary index is being selected with the JET_bitNoMove option and there is no index entry in the new index that corresponds to the record associated with the index entry at the current position of the cursor on the old index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9866e-176">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="9866e-176">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="9866e-177">Der Vorgang kann nicht abgeschlossen werden, da die Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="9866e-177">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9866e-178">JET_errOutOfCursors</span><span class="sxs-lookup"><span data-stu-id="9866e-178">JET_errOutOfCursors</span></span></p></td>
<td><p><span data-ttu-id="9866e-179">Die Engine hat den Ressourcenpool erschöpft, der zum Öffnen von Cursorn verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9866e-179">The engine has exhausted its pool of resources used to open cursors.</span></span> <span data-ttu-id="9866e-180">Die maximale Anzahl von Cursorn, die zu einem beliebigen Zeitpunkt geöffnet werden können, wird mit <a href="gg269201(v=exchg.10).md">JET_paramMaxCursors</a>gesteuert.</span><span class="sxs-lookup"><span data-stu-id="9866e-180">The maximum number of cursors that can be opened at any one time is controlled using <a href="gg269201(v=exchg.10).md">JET_paramMaxCursors</a>.</span></span> <span data-ttu-id="9866e-181">Weitere Informationen finden Sie unter <a href="gg294044(v=exchg.10).md">jetsetsystemparameter</a> .</span><span class="sxs-lookup"><span data-stu-id="9866e-181">See <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> for more information.</span></span> <span data-ttu-id="9866e-182">Dies kann bei <strong>JetSetCurrentIndex2</strong> vorkommen, wenn ein sekundärer Index ausgewählt wurde und die Engine keinen internen Cursor öffnen kann, um diesen Index zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="9866e-182">This can happen for <strong>JetSetCurrentIndex2</strong> when a secondary index has been selected and the engine cannot open an internal cursor to use that index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9866e-183">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="9866e-183">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="9866e-184">Der Vorgang kann nicht abgeschlossen werden, da für die-Instanz, die der Sitzung zugeordnet ist, ein Wiederherstellungs Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9866e-184">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9866e-185">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="9866e-185">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="9866e-186">Dieselbe Sitzung kann nicht für mehr als einen Thread gleichzeitig verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9866e-186">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="9866e-187">Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9866e-187">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9866e-188">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="9866e-188">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="9866e-189">Der Vorgang kann nicht ausgeführt werden, da die Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="9866e-189">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="9866e-190">Bei Erfolg wird der aktuelle Index des Cursors auf den angeforderten Index festgelegt.</span><span class="sxs-lookup"><span data-stu-id="9866e-190">On success, the current index of the cursor is set to the requested index.</span></span> <span data-ttu-id="9866e-191">Indexeinträge können nun mithilfe von [JetSeek](./jetseek-function.md) entsprechend der Index Definition des angeforderten Indexes gesucht werden.</span><span class="sxs-lookup"><span data-stu-id="9866e-191">Index entries may now be sought using [JetSeek](./jetseek-function.md) according to the index definition of the requested index.</span></span> <span data-ttu-id="9866e-192">Index Einträge können auch mithilfe von [jetmove](./jetmove-function.md) in der von dieser Index Definition angegebenen Reihenfolge aufgelistet werden.</span><span class="sxs-lookup"><span data-stu-id="9866e-192">Index entries may also be enumerated using [JetMove](./jetmove-function.md) in the order specified by that index definition.</span></span> <span data-ttu-id="9866e-193">Die aktuelle Position des Cursors ist entweder auf den ersten Index Eintrag im Index (JET_bitMoveFirst) oder auf einen bestimmten Index Eintrag festgelegt, der mit der aktuellen Position des Cursors im alten Index (JET_bitNoMove) verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="9866e-193">The current position of the cursor is either set to the first index entry on the index (JET_bitMoveFirst) or to a specific index entry that is related to the current position of the cursor on the old index (JET_bitNoMove).</span></span> <span data-ttu-id="9866e-194">Es erfolgt keine Änderung des Daten Bank Status.</span><span class="sxs-lookup"><span data-stu-id="9866e-194">No change to the database state will occur.</span></span>

<span data-ttu-id="9866e-195">Bei einem Fehler sind der aktuelle Index und die aktuelle Position des Cursors in einem nicht definierten Zustand.</span><span class="sxs-lookup"><span data-stu-id="9866e-195">On failure, the current index and current position of the cursor are in an undefined state.</span></span> <span data-ttu-id="9866e-196">Es erfolgt keine Änderung des Daten Bank Status.</span><span class="sxs-lookup"><span data-stu-id="9866e-196">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="9866e-197">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9866e-197">Remarks</span></span>

<span data-ttu-id="9866e-198">Wenn der Index-ID-Hinweis veraltet ist, schlägt die API einfach fehl.</span><span class="sxs-lookup"><span data-stu-id="9866e-198">If the index ID hint is stale then the API simply fails.</span></span> <span data-ttu-id="9866e-199">Es gibt in diesem Fall keinen Fall Back auf den Textnamen des Indexes, wie dies zu erwarten ist.</span><span class="sxs-lookup"><span data-stu-id="9866e-199">There is no fallback to the text name of the index in this case as one might expect.</span></span> <span data-ttu-id="9866e-200">Dieser Fall Back muss manuell vom Aufrufer der API durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="9866e-200">This fallback must be done manually by the caller of the API.</span></span>

#### <a name="requirements"></a><span data-ttu-id="9866e-201">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9866e-201">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9866e-202"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="9866e-202"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="9866e-203">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="9866e-203">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9866e-204"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="9866e-204"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="9866e-205">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="9866e-205">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9866e-206"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="9866e-206"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="9866e-207">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="9866e-207">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9866e-208"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="9866e-208"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="9866e-209">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="9866e-209">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9866e-210"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="9866e-210"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="9866e-211">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="9866e-211">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9866e-212"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="9866e-212"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="9866e-213">Implementiert als <strong>JetSetCurrentIndex2W</strong> (Unicode) und <strong>JetSetCurrentIndex2A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="9866e-213">Implemented as <strong>JetSetCurrentIndex2W</strong> (Unicode) and <strong>JetSetCurrentIndex2A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="9866e-214">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="9866e-214">See Also</span></span>

[<span data-ttu-id="9866e-215">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="9866e-215">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="9866e-216">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="9866e-216">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="9866e-217">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="9866e-217">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="9866e-218">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="9866e-218">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="9866e-219">JET_INDEXID</span><span class="sxs-lookup"><span data-stu-id="9866e-219">JET_INDEXID</span></span>](./jet-indexid-structure.md)  
[<span data-ttu-id="9866e-220">Jetkreateingedex</span><span class="sxs-lookup"><span data-stu-id="9866e-220">JetCreateIndex</span></span>](./jetcreateindex-function.md)  
[<span data-ttu-id="9866e-221">Jetgetcurrentindex</span><span class="sxs-lookup"><span data-stu-id="9866e-221">JetGetCurrentIndex</span></span>](./jetgetcurrentindex-function.md)  
[<span data-ttu-id="9866e-222">Jetgetindexinfo</span><span class="sxs-lookup"><span data-stu-id="9866e-222">JetGetIndexInfo</span></span>](./jetgetindexinfo-function.md)  
[<span data-ttu-id="9866e-223">Jetgettableindexinfo</span><span class="sxs-lookup"><span data-stu-id="9866e-223">JetGetTableIndexInfo</span></span>](./jetgettableindexinfo-function.md)  
[<span data-ttu-id="9866e-224">Jetmove</span><span class="sxs-lookup"><span data-stu-id="9866e-224">JetMove</span></span>](./jetmove-function.md)  
[<span data-ttu-id="9866e-225">Jetsetsystemparameter</span><span class="sxs-lookup"><span data-stu-id="9866e-225">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="9866e-226">JetSeek</span><span class="sxs-lookup"><span data-stu-id="9866e-226">JetSeek</span></span>](./jetseek-function.md)  
[<span data-ttu-id="9866e-227">Jetstopservice</span><span class="sxs-lookup"><span data-stu-id="9866e-227">JetStopService</span></span>](./jetstopservice-function.md)
