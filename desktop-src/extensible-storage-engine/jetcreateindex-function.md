---
description: 'Weitere Informationen zu: jetkreateinzudex-Funktion'
title: JetCreateIndex-Funktion
TOCTitle: JetCreateIndex Function
ms:assetid: d164e74a-7719-4587-9059-8fb18b365133
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294099(v=EXCHG.10)
ms:contentKeyID: 32765714
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateIndexA
- JetCreateIndex
- JetCreateIndexW
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c0208a5f0adac4ff5128b506123f3b68589cd0d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106367984"
---
# <a name="jetcreateindex-function"></a><span data-ttu-id="1ea40-103">JetCreateIndex-Funktion</span><span class="sxs-lookup"><span data-stu-id="1ea40-103">JetCreateIndex Function</span></span>


<span data-ttu-id="1ea40-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="1ea40-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetcreateindex-function"></a><span data-ttu-id="1ea40-105">JetCreateIndex-Funktion</span><span class="sxs-lookup"><span data-stu-id="1ea40-105">JetCreateIndex Function</span></span>

<span data-ttu-id="1ea40-106">Mithilfe der **jetkreateindex** -Funktion können Sie einen Index von Daten in einer ESE-Datenbank (Extensible Storage Engine) erstellen, die Sie verwenden können, um bestimmte Daten schnell zu suchen.</span><span class="sxs-lookup"><span data-stu-id="1ea40-106">The **JetCreateIndex** function enables you to create an index of data in an Extensible Storage Engine (ESE) database, which you can use to locate specific data quickly.</span></span>

```cpp
    JET_ERR JET_API JetCreateIndex(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_PCSTR szIndexName,
      __in          JET_GRBIT grbit,
      __in          const tchar* szKey,
      __in          unsigned long cbKey,
      __in          unsigned long lDensity
    );
```

### <a name="parameters"></a><span data-ttu-id="1ea40-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="1ea40-107">Parameters</span></span>

<span data-ttu-id="1ea40-108">*-sid*</span><span class="sxs-lookup"><span data-stu-id="1ea40-108">*sesid*</span></span>

<span data-ttu-id="1ea40-109">Der Daten Bank Sitzungs Kontext, der für einen bestimmten API-Befehl verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="1ea40-109">The database session context to use for a particular API call.</span></span>

<span data-ttu-id="1ea40-110">*TableID*</span><span class="sxs-lookup"><span data-stu-id="1ea40-110">*tableid*</span></span>

<span data-ttu-id="1ea40-111">Die Tabelle, für die ein Index erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="1ea40-111">The table that an index will be created for.</span></span>

<span data-ttu-id="1ea40-112">*szindexname*</span><span class="sxs-lookup"><span data-stu-id="1ea40-112">*szIndexName*</span></span>

<span data-ttu-id="1ea40-113">Ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Namen des zu erstellenden Indexes angibt.</span><span class="sxs-lookup"><span data-stu-id="1ea40-113">A pointer to a null-terminated string that specifies the name of the index to be created.</span></span>

<span data-ttu-id="1ea40-114">Der Indexname muss den folgenden Richtlinien entsprechen:</span><span class="sxs-lookup"><span data-stu-id="1ea40-114">The index name must conform to the following guidelines:</span></span>

  - <span data-ttu-id="1ea40-115">Es muss weniger Zeichen als JET_cbNameMost enthalten, ohne das abschließende Null Zeichen.</span><span class="sxs-lookup"><span data-stu-id="1ea40-115">It must contain fewer characters than JET_cbNameMost, not including the terminating null character.</span></span>

  - <span data-ttu-id="1ea40-116">Er darf nur Zeichen aus den folgenden Kategorien enthalten: 0 bis 9, a bis z, a bis z und alle Interpunktions Zeichen mit Ausnahme von " \! ".</span><span class="sxs-lookup"><span data-stu-id="1ea40-116">It must contain only characters from the following categories: 0 through 9, A through Z, a through z, and all punctuation characters except for "\!"</span></span> <span data-ttu-id="1ea40-117">(Ausrufezeichen), "," (Komma), " \[ " (öffnende eckige Klammer) und " \] " (schließende Klammer) – d. h. die ASCII-Zeichen 0x20, 0x22 bis 0x2D, 0x2F bis 0x5A, 0x5c und 0x5d bis 0x7F.</span><span class="sxs-lookup"><span data-stu-id="1ea40-117">(exclamation point), "," (comma), "\[" (opening bracket), and "\]" (closing bracket) — that is, the ASCII characters 0x20, 0x22 through 0x2d, 0x2f through 0x5a, 0x5c, and 0x5d through 0x7f.</span></span>

  - <span data-ttu-id="1ea40-118">Er darf nicht mit einem Leerzeichen beginnen.</span><span class="sxs-lookup"><span data-stu-id="1ea40-118">It must not begin with a space.</span></span>

  - <span data-ttu-id="1ea40-119">Sie muss mindestens ein Zeichen enthalten, das kein Leerzeichen ist.</span><span class="sxs-lookup"><span data-stu-id="1ea40-119">It must contain at least one non-space character.</span></span>

<span data-ttu-id="1ea40-120">*grbit*</span><span class="sxs-lookup"><span data-stu-id="1ea40-120">*grbit*</span></span>

<span data-ttu-id="1ea40-121">Eine Gruppe von Bits, die die Optionen enthält, die für einen bestimmten-aufrufbedarf verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="1ea40-121">A group of bits that contains the options to be used for a particular call.</span></span> <span data-ttu-id="1ea40-122">Dieser Parameter kann NULL oder mehr der Optionen enthalten, die in der [JET_INDEXCREATE](./jet-indexcreate-structure.md) Struktur gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="1ea40-122">This parameter can include zero or more of the options found in the [JET_INDEXCREATE](./jet-indexcreate-structure.md) structure.</span></span>

<span data-ttu-id="1ea40-123">*szkey*</span><span class="sxs-lookup"><span data-stu-id="1ea40-123">*szKey*</span></span>

<span data-ttu-id="1ea40-124">Ein Zeiger auf eine Double-NULL-terminierte Zeichenfolge von NULL-getrennten Token.</span><span class="sxs-lookup"><span data-stu-id="1ea40-124">A pointer to a double null-terminated string of null-delimited tokens.</span></span>

<span data-ttu-id="1ea40-125">Weitere Informationen zu diesem Parameter finden Sie in der [JET_INDEXCREATE](./jet-indexcreate-structure.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="1ea40-125">For more information about this parameter, see the [JET_INDEXCREATE](./jet-indexcreate-structure.md) structure.</span></span>

<span data-ttu-id="1ea40-126">*cbKey*</span><span class="sxs-lookup"><span data-stu-id="1ea40-126">*cbKey*</span></span>

<span data-ttu-id="1ea40-127">Die Länge des *szkey* -Parameters in Bytes, einschließlich der beiden abschließenden NULL Zeichen.</span><span class="sxs-lookup"><span data-stu-id="1ea40-127">The length, in bytes, of the *szKey* parameter, including the two terminating null characters.</span></span>

<span data-ttu-id="1ea40-128">*ldensity*</span><span class="sxs-lookup"><span data-stu-id="1ea40-128">*lDensity*</span></span>

<span data-ttu-id="1ea40-129">Die prozentuale Dichte des ersten Index B +-Baums.</span><span class="sxs-lookup"><span data-stu-id="1ea40-129">The percentage density of the initial index B+ tree.</span></span>

<span data-ttu-id="1ea40-130">Weitere Informationen zu diesem Parameter finden Sie in der [JET_INDEXCREATE](./jet-indexcreate-structure.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="1ea40-130">For more information about this parameter, see the [JET_INDEXCREATE](./jet-indexcreate-structure.md) structure.</span></span>

### <a name="return-value"></a><span data-ttu-id="1ea40-131">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1ea40-131">Return Value</span></span>

<span data-ttu-id="1ea40-132">Diese Funktion gibt den [JET_ERR](./jet-err.md) -Datentyp mit einem der in der folgenden Tabelle aufgelisteten Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="1ea40-132">This function returns the [JET_ERR](./jet-err.md) data type with one of the return codes listed in the following table.</span></span> <span data-ttu-id="1ea40-133">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="1ea40-133">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1ea40-134">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="1ea40-134">Return code</span></span></p></th>
<th><p><span data-ttu-id="1ea40-135">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="1ea40-135">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1ea40-136">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="1ea40-136">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="1ea40-137">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="1ea40-137">The operation completed successfully.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="1ea40-138">Eine Liste mit zusätzlichen Fehlern, die von der **jetkreateinzudex** -Funktion zurückgegeben werden können, finden Sie unter [JetCreateIndex2](./jetcreateindex2-function.md).</span><span class="sxs-lookup"><span data-stu-id="1ea40-138">For a list of additional errors that can be returned by the **JetCreateIndex** function, see [JetCreateIndex2](./jetcreateindex2-function.md).</span></span>

#### <a name="remarks"></a><span data-ttu-id="1ea40-139">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1ea40-139">Remarks</span></span>

<span data-ttu-id="1ea40-140">Das Aufrufen der **jetcreateindex** -Funktion ist identisch mit dem Aufruf der [JetCreateIndex2](./jetcreateindex2-function.md) -Funktion mit einer [JET_INDEXCREATE](./jet-indexcreate-structure.md) -Struktur, die die gleichen Einstellungen wie die Parameter von **jetcreateindex** und einen *cindexcreate* -Parameter gleich 1 enthält.</span><span class="sxs-lookup"><span data-stu-id="1ea40-140">Calling the **JetCreateIndex** function is identical to calling the [JetCreateIndex2](./jetcreateindex2-function.md) function with a [JET_INDEXCREATE](./jet-indexcreate-structure.md) structure containing the same settings as the parameters of **JetCreateIndex**, and a *cIndexCreate* parameter equal to 1.</span></span> <span data-ttu-id="1ea40-141">Für die Felder der [JET_INDEXCREATE](./jet-indexcreate-structure.md) Struktur, die keine entsprechenden Parameter in **jetkreatandex** aufweisen, wird der Wert 0 angenommen.</span><span class="sxs-lookup"><span data-stu-id="1ea40-141">For the fields of the [JET_INDEXCREATE](./jet-indexcreate-structure.md) structure that do not have corresponding parameters in **JetCreateIndex**, a value of 0 is assumed.</span></span>

<span data-ttu-id="1ea40-142">Beachten Sie, dass **jetkreatandex** durch [JetCreateIndex2](./jetcreateindex2-function.md)abgelöst wurde.</span><span class="sxs-lookup"><span data-stu-id="1ea40-142">Note that **JetCreateIndex** has been superseded by [JetCreateIndex2](./jetcreateindex2-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="1ea40-143">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1ea40-143">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1ea40-144">Client</span><span class="sxs-lookup"><span data-stu-id="1ea40-144">Client</span></span></p></td>
<td><p><span data-ttu-id="1ea40-145">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="1ea40-145">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1ea40-146">Server</span><span class="sxs-lookup"><span data-stu-id="1ea40-146">Server</span></span></p></td>
<td><p><span data-ttu-id="1ea40-147">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="1ea40-147">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1ea40-148">Header</span><span class="sxs-lookup"><span data-stu-id="1ea40-148">Header</span></span></p></td>
<td><p><span data-ttu-id="1ea40-149">Wird in "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="1ea40-149">Is declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1ea40-150">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1ea40-150">Library</span></span></p></td>
<td><p><span data-ttu-id="1ea40-151">Verwendet ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="1ea40-151">Uses ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1ea40-152">DLL</span><span class="sxs-lookup"><span data-stu-id="1ea40-152">DLL</span></span></p></td>
<td><p><span data-ttu-id="1ea40-153">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="1ea40-153">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1ea40-154">Unicode</span><span class="sxs-lookup"><span data-stu-id="1ea40-154">Unicode</span></span></p></td>
<td><p><span data-ttu-id="1ea40-155">Ist als <strong>jetkreateingedexw</strong> (Unicode) und <strong>jetkreateingedexa</strong> (ANSI) implementiert.</span><span class="sxs-lookup"><span data-stu-id="1ea40-155">Is implemented as <strong>JetCreateIndexW</strong> (Unicode) and <strong>JetCreateIndexA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="1ea40-156">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="1ea40-156">See Also</span></span>

[<span data-ttu-id="1ea40-157">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="1ea40-157">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="1ea40-158">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="1ea40-158">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="1ea40-159">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="1ea40-159">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="1ea40-160">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="1ea40-160">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="1ea40-161">JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="1ea40-161">JET_INDEXCREATE</span></span>](./jet-indexcreate-structure.md)  
[<span data-ttu-id="1ea40-162">JetCreateIndex2</span><span class="sxs-lookup"><span data-stu-id="1ea40-162">JetCreateIndex2</span></span>](./jetcreateindex2-function.md)  
[<span data-ttu-id="1ea40-163">Jetkreatetablecolumnindex</span><span class="sxs-lookup"><span data-stu-id="1ea40-163">JetCreateTableColumnIndex</span></span>](./jetcreatetablecolumnindex-function.md)  
[<span data-ttu-id="1ea40-164">JetCreateTableColumnIndex2</span><span class="sxs-lookup"><span data-stu-id="1ea40-164">JetCreateTableColumnIndex2</span></span>](./jetcreatetablecolumnindex2-function.md)
