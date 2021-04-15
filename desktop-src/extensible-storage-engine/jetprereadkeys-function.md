---
description: 'Weitere Informationen finden Sie unter: jetprereadkeys-Funktion'
title: Jetprereadkeys-Funktion
TOCTitle: JetPrereadKeys Function
ms:assetid: fc2f46bc-1f81-4af2-aa63-9757e819efc2
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294143(v=EXCHG.10)
ms:contentKeyID: 32765757
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetPrereadKeys
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d35407c171bdcd54eb44e9830f382c08a1e6c6c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484875"
---
# <a name="jetprereadkeys-function"></a><span data-ttu-id="0f29e-103">Jetprereadkeys-Funktion</span><span class="sxs-lookup"><span data-stu-id="0f29e-103">JetPrereadKeys Function</span></span>


<span data-ttu-id="0f29e-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="0f29e-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetprereadkeys-function"></a><span data-ttu-id="0f29e-105">Jetprereadkeys-Funktion</span><span class="sxs-lookup"><span data-stu-id="0f29e-105">JetPrereadKeys Function</span></span>

<span data-ttu-id="0f29e-106">Die **jetprereadkeys** -Funktion liest Schlüsselwerte, um die Leistung der Bereinigung des Versionsspeicher zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="0f29e-106">The **JetPrereadKeys** function reads key values to improve the performance of version store cleanup.</span></span>

<span data-ttu-id="0f29e-107">**Windows 7: die prereadkeys** -Funktion wurde in Windows 7 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="0f29e-107">**Windows 7:  PrereadKeys** function is introduced in Windows 7.</span></span>

```cpp
    JET_ERR JET_API JetPrereadKeys(
      __in JET_SESID sesid,
      __in JET_TABLEID tableid,
      __in_ecount(ckeys) const void ** rgpvKeys,
      __in_ecount(ckeys) const unsigned long * rgcbKeys,
      __in long ckeys,
      __out_opt long * pckeysPreread,
      __in JET_GRBIT grbit
     );
```

### <a name="parameters"></a><span data-ttu-id="0f29e-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="0f29e-108">Parameters</span></span>

<span data-ttu-id="0f29e-109">*-sid*</span><span class="sxs-lookup"><span data-stu-id="0f29e-109">*sesid*</span></span>

<span data-ttu-id="0f29e-110">Der für den API-Befehl zu verwendende Daten Bank Sitzungs Kontext.</span><span class="sxs-lookup"><span data-stu-id="0f29e-110">The database session context to use for the API call.</span></span>

<span data-ttu-id="0f29e-111">*TableID*</span><span class="sxs-lookup"><span data-stu-id="0f29e-111">*tableid*</span></span>

<span data-ttu-id="0f29e-112">Der Cursor, der für diesen-Befehl verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="0f29e-112">The cursor to use for this call.</span></span>

<span data-ttu-id="0f29e-113">*rgpvkeys*</span><span class="sxs-lookup"><span data-stu-id="0f29e-113">*rgpvKeys*</span></span>

<span data-ttu-id="0f29e-114">Ein Array von Zeigern zu Schlüsseln.</span><span class="sxs-lookup"><span data-stu-id="0f29e-114">An array of pointers to keys.</span></span> <span data-ttu-id="0f29e-115">Schlüssel können mit [jetmakekey](./jetmakekey-function.md) erstellt oder mit [jetgetbookmark](./jetgetbookmark-function.md)abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="0f29e-115">Keys can be made with [JetMakeKey](./jetmakekey-function.md) or retrieved with [JetGetBookmark](./jetgetbookmark-function.md).</span></span> <span data-ttu-id="0f29e-116">Die Schlüssel müssen in aufsteigender oder absteigender Reihenfolge sortiert werden, je nach dem bestandenen grbit.</span><span class="sxs-lookup"><span data-stu-id="0f29e-116">The keys must be sorted in ascending or descending order, depending on the grbit passed.</span></span> <span data-ttu-id="0f29e-117">Schlüssel können mit memcmp sortiert werden.</span><span class="sxs-lookup"><span data-stu-id="0f29e-117">Keys can be sorted with memcmp.</span></span>

<span data-ttu-id="0f29e-118">*rgcbkeys*</span><span class="sxs-lookup"><span data-stu-id="0f29e-118">*rgcbKeys*</span></span>

<span data-ttu-id="0f29e-119">Ein Array von Schlüssellängen.</span><span class="sxs-lookup"><span data-stu-id="0f29e-119">An array of key lengths.</span></span> <span data-ttu-id="0f29e-120">rgpvkeys \[ n \] sollte auf einen Schlüssel der Länge rgcbkeys n zeigen. \[\]</span><span class="sxs-lookup"><span data-stu-id="0f29e-120">rgpvKeys\[n\] should point to a key of length rgcbKeys\[n\]</span></span>

<span data-ttu-id="0f29e-121">*ckeys*</span><span class="sxs-lookup"><span data-stu-id="0f29e-121">*ckeys*</span></span>

<span data-ttu-id="0f29e-122">Die Anzahl der Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="0f29e-122">The number of keys.</span></span> <span data-ttu-id="0f29e-123">rgpvkeys und rgcbkeys müssen jeweils auf ein Array mit mindestens "ckeys"-Elementen zeigen.</span><span class="sxs-lookup"><span data-stu-id="0f29e-123">rgpvKeys and rgcbKeys must each point to an array with at least ckeys elements.</span></span>

<span data-ttu-id="0f29e-124">*pckeyspreread*</span><span class="sxs-lookup"><span data-stu-id="0f29e-124">*pckeysPreread*</span></span>

<span data-ttu-id="0f29e-125">Gibt die Anzahl der Schlüssel zurück, für die prereads tatsächlich ausgestellt wurden.</span><span class="sxs-lookup"><span data-stu-id="0f29e-125">Returns the number of keys that prereads were actually issued for.</span></span> <span data-ttu-id="0f29e-126">Dieser Parameter kann NULL sein.</span><span class="sxs-lookup"><span data-stu-id="0f29e-126">This parameter can be NULL.</span></span>

<span data-ttu-id="0f29e-127">*grbit*</span><span class="sxs-lookup"><span data-stu-id="0f29e-127">*grbit*</span></span>

<span data-ttu-id="0f29e-128">Dies muss entweder JET_bitPrereadForward oder JET_bitPrereadBackward sein.</span><span class="sxs-lookup"><span data-stu-id="0f29e-128">This must be either JET_bitPrereadForward or JET_bitPrereadBackward.</span></span> <span data-ttu-id="0f29e-129">Wenn grbit JET_bitPrereadForward ist, müssen die Schlüssel in aufsteigender Reihenfolge sortiert werden.</span><span class="sxs-lookup"><span data-stu-id="0f29e-129">If grbit is JET_bitPrereadForward, the keys must be sorted in ascending order.</span></span> <span data-ttu-id="0f29e-130">Wenn grbit JET_bitPrereadBackward ist, müssen die Schlüssel in absteigender Reihenfolge sortiert werden.</span><span class="sxs-lookup"><span data-stu-id="0f29e-130">If grbit is JET_bitPrereadBackward, the keys must be sorted in descending order.</span></span>

### <a name="return-value"></a><span data-ttu-id="0f29e-131">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0f29e-131">Return Value</span></span>

<span data-ttu-id="0f29e-132">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="0f29e-132">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="0f29e-133">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="0f29e-133">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<span data-ttu-id="0f29e-134">Verschiedene e/a-Fehler können zusammen mit den folgenden API-Verwendungs Fehlern zurückgegeben werden:</span><span class="sxs-lookup"><span data-stu-id="0f29e-134">Various I/O errors can be returned along with these API usage errors:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0f29e-135">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="0f29e-135">Return code</span></span></p></th>
<th><p><span data-ttu-id="0f29e-136">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0f29e-136">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0f29e-137">JET_errInvalidGrbit</span><span class="sxs-lookup"><span data-stu-id="0f29e-137">JET_errInvalidGrbit</span></span></p></td>
<td><p><span data-ttu-id="0f29e-138">Grbit war weder JET_bitPrereadForward noch JET_bitPrereadBackward.</span><span class="sxs-lookup"><span data-stu-id="0f29e-138">Grbit was neither JET_bitPrereadForward nor JET_bitPrereadBackward.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0f29e-139">JET_errInvalidBufferSize</span><span class="sxs-lookup"><span data-stu-id="0f29e-139">JET_errInvalidBufferSize</span></span></p></td>
<td><p><span data-ttu-id="0f29e-140">Es wurde eine falsche Schlüsselgröße übermittelt.</span><span class="sxs-lookup"><span data-stu-id="0f29e-140">An incorrect key size has been passed in.</span></span> <span data-ttu-id="0f29e-141">Schlüssel können weder 0 noch länger als die maximale Schlüssellänge der Tabelle sein.</span><span class="sxs-lookup"><span data-stu-id="0f29e-141">Keys can neither be 0 nor longer than the maximum key length for the table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0f29e-142">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="0f29e-142">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="0f29e-143">Ein ungültiger Parameter wurde übergeben.</span><span class="sxs-lookup"><span data-stu-id="0f29e-143">An invalid parameter has been passed in.</span></span> <span data-ttu-id="0f29e-144">Dies kann durch einen NULL-Wert für einen erforderlichen Parameter verursacht werden, oder es kann darauf hingewiesen werden, dass das Schlüssel Array nicht ordnungsgemäß sortiert ist.</span><span class="sxs-lookup"><span data-stu-id="0f29e-144">This can be caused by a null value for a required parameter or can indicate that the key array is not sorted properly.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="0f29e-145">**Jetprereadkeys** durchläuft die internen Seiten der b-Struktur, um zu bestimmen, welche Blattseiten die von rgpvkeys/rgcbkeys angegebenen Schlüssel enthalten.</span><span class="sxs-lookup"><span data-stu-id="0f29e-145">**JetPrereadKeys** traverses the internal pages of the b-tree to determine which leaf pages contain the keys specified by rgpvKeys/rgcbKeys.</span></span> <span data-ttu-id="0f29e-146">Die Liste der Blattseiten wird sortiert, und dann werden die Seitenbereiche für die Seitenbereiche ausgegeben.</span><span class="sxs-lookup"><span data-stu-id="0f29e-146">The list of leaf pages is sorted and then prereads are issued for the ranges of pages.</span></span> <span data-ttu-id="0f29e-147">Die Anzahl der Seiten, die auf "Preread" feststellen können, ist begrenzt, daher ist es möglich, dass nicht alle Schlüssel vorab registriert werden.</span><span class="sxs-lookup"><span data-stu-id="0f29e-147">The number of pages that can be preread is limited so it is possible that not all keys may be preread.</span></span> <span data-ttu-id="0f29e-148">In diesem Fall wird die Anzahl der Schlüssel, die tatsächlich in "pckeyspreread" geschrieben werden, zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="0f29e-148">In that case, the number of keys actually preread is returned in pckeysPreread.</span></span>

#### <a name="requirements"></a><span data-ttu-id="0f29e-149">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0f29e-149">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0f29e-150"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="0f29e-150"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="0f29e-151">Erfordert Windows 7.</span><span class="sxs-lookup"><span data-stu-id="0f29e-151">Requires Windows 7.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0f29e-152"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="0f29e-152"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="0f29e-153">Erfordert Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="0f29e-153">Requires Windows Server 2008 R2.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0f29e-154"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="0f29e-154"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="0f29e-155">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="0f29e-155">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0f29e-156"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="0f29e-156"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="0f29e-157">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="0f29e-157">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0f29e-158"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="0f29e-158"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="0f29e-159">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="0f29e-159">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>
