---
description: 'Weitere Informationen finden Sie hier: JET_OBJECTINFO Struktur'
title: JET_OBJECTINFO-Struktur
TOCTitle: JET_OBJECTINFO Structure
ms:assetid: 9d348ab3-d453-4316-9233-681f165e8ef1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269353(v=EXCHG.10)
ms:contentKeyID: 32765640
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cd1f8a876153b5b457cfb153cbf35fa2d388b0f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042659"
---
# <a name="jet_objectinfo-structure"></a><span data-ttu-id="3d3f8-103">JET_OBJECTINFO-Struktur</span><span class="sxs-lookup"><span data-stu-id="3d3f8-103">JET_OBJECTINFO Structure</span></span>


<span data-ttu-id="3d3f8-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="3d3f8-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_objectinfo-structure"></a><span data-ttu-id="3d3f8-105">JET_OBJECTINFO-Struktur</span><span class="sxs-lookup"><span data-stu-id="3d3f8-105">JET_OBJECTINFO Structure</span></span>

<span data-ttu-id="3d3f8-106">Die **JET_OBJECTINFO** -Struktur enthält Informationen zu einem-Objekt.</span><span class="sxs-lookup"><span data-stu-id="3d3f8-106">The **JET_OBJECTINFO** structure holds information about an object.</span></span> <span data-ttu-id="3d3f8-107">Tabellen sind die einzigen Objekttypen, die derzeit unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="3d3f8-107">Tables are the only object types that are currently supported.</span></span>

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_OBJTYP objtyp;
      JET_DATESERIAL dtCreate;
      JET_DATESERIAL dtUpdate;
      JET_GRBIT grbit;
      unsigned long flags;
      unsigned long cRecord;
      unsigned long cPage;
    } JET_OBJECTINFO;
```

### <a name="members"></a><span data-ttu-id="3d3f8-108">Member</span><span class="sxs-lookup"><span data-stu-id="3d3f8-108">Members</span></span>

<span data-ttu-id="3d3f8-109">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="3d3f8-109">**cbStruct**</span></span>

<span data-ttu-id="3d3f8-110">Die Größe der **JET_OBJECTINFO** Struktur in Bytes.</span><span class="sxs-lookup"><span data-stu-id="3d3f8-110">The size, in bytes, of the **JET_OBJECTINFO** structure.</span></span>

<span data-ttu-id="3d3f8-111">**objyp**</span><span class="sxs-lookup"><span data-stu-id="3d3f8-111">**objtyp**</span></span>

<span data-ttu-id="3d3f8-112">Enthält die [JET_OBJTYP](./jet-objtyp.md) der-Struktur.</span><span class="sxs-lookup"><span data-stu-id="3d3f8-112">Holds the [JET_OBJTYP](./jet-objtyp.md) of the structure.</span></span> <span data-ttu-id="3d3f8-113">Zurzeit werden nur Tabellen zurückgegeben (d. h. JET_objtypTable).</span><span class="sxs-lookup"><span data-stu-id="3d3f8-113">Currently only tables will be returned (that is, JET_objtypTable).</span></span>

<span data-ttu-id="3d3f8-114">**dtcreate**</span><span class="sxs-lookup"><span data-stu-id="3d3f8-114">**dtCreate**</span></span>

<span data-ttu-id="3d3f8-115">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="3d3f8-115">Obsolete.</span></span> <span data-ttu-id="3d3f8-116">Darf nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3d3f8-116">Do not use.</span></span>

<span data-ttu-id="3d3f8-117">**dtupdate**</span><span class="sxs-lookup"><span data-stu-id="3d3f8-117">**dtUpdate**</span></span>

<span data-ttu-id="3d3f8-118">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="3d3f8-118">Obsolete.</span></span> <span data-ttu-id="3d3f8-119">Darf nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3d3f8-119">Do not use.</span></span>

<span data-ttu-id="3d3f8-120">**grbit**</span><span class="sxs-lookup"><span data-stu-id="3d3f8-120">**grbit**</span></span>

<span data-ttu-id="3d3f8-121">Eine Gruppe von Bits, die die für diesen-Befehl verfügbaren Optionen enthalten, die NULL oder mehr der folgenden Elemente enthalten.</span><span class="sxs-lookup"><span data-stu-id="3d3f8-121">A group of bits that contain the options that are available for this call, which include zero or more of the following.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3d3f8-122">Wert</span><span class="sxs-lookup"><span data-stu-id="3d3f8-122">Value</span></span></p></th>
<th><p><span data-ttu-id="3d3f8-123">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="3d3f8-123">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3d3f8-124">JET_bitTableInfoBookmark</span><span class="sxs-lookup"><span data-stu-id="3d3f8-124">JET_bitTableInfoBookmark</span></span></p></td>
<td><p><span data-ttu-id="3d3f8-125">Die Tabelle kann Lesezeichen enthalten.</span><span class="sxs-lookup"><span data-stu-id="3d3f8-125">The table can have bookmarks.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3d3f8-126">JET_bitTableInfoRollback</span><span class="sxs-lookup"><span data-stu-id="3d3f8-126">JET_bitTableInfoRollback</span></span></p></td>
<td><p><span data-ttu-id="3d3f8-127">Für die Tabelle kann ein Rollback ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="3d3f8-127">The table can be rolled back.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3d3f8-128">JET_bitTableInfoUpdatable</span><span class="sxs-lookup"><span data-stu-id="3d3f8-128">JET_bitTableInfoUpdatable</span></span></p></td>
<td><p><span data-ttu-id="3d3f8-129">Die Tabelle kann aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="3d3f8-129">The table can be updated.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="3d3f8-130">**flags**</span><span class="sxs-lookup"><span data-stu-id="3d3f8-130">**flags**</span></span>

<span data-ttu-id="3d3f8-131">Ein Bitfeld, das NULL oder mehr der folgenden Flags enthält.</span><span class="sxs-lookup"><span data-stu-id="3d3f8-131">A bit field that contains zero or more of the following flags.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3d3f8-132">Wert</span><span class="sxs-lookup"><span data-stu-id="3d3f8-132">Value</span></span></p></th>
<th><p><span data-ttu-id="3d3f8-133">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="3d3f8-133">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3d3f8-134">JET_bitObjectSystem</span><span class="sxs-lookup"><span data-stu-id="3d3f8-134">JET_bitObjectSystem</span></span></p></td>
<td><p><span data-ttu-id="3d3f8-135">Die Tabelle ist eine System Tabelle und nur für die interne Verwendung vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="3d3f8-135">The table is a System Table and is for internal use only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3d3f8-136">JET_bitObjectTableDerived</span><span class="sxs-lookup"><span data-stu-id="3d3f8-136">JET_bitObjectTableDerived</span></span></p></td>
<td><p><span data-ttu-id="3d3f8-137">Die Tabelle hat DDL aus einer Vorlagen Tabelle geerbt.</span><span class="sxs-lookup"><span data-stu-id="3d3f8-137">The table inherited DDL from a template table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3d3f8-138">JET_bitObjectTableFixedDDL</span><span class="sxs-lookup"><span data-stu-id="3d3f8-138">JET_bitObjectTableFixedDDL</span></span></p></td>
<td><p><span data-ttu-id="3d3f8-139">Die DDL für die Tabelle kann nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="3d3f8-139">The DDL for the table cannot be modified.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3d3f8-140">JET_bitObjectTableNoFixedVarColumnsInDerivedTables</span><span class="sxs-lookup"><span data-stu-id="3d3f8-140">JET_bitObjectTableNoFixedVarColumnsInDerivedTables</span></span></p></td>
<td><p><span data-ttu-id="3d3f8-141">Wird in Verbindung mit JET_bitObjectTableTemplate verwendet, um die festgelegten oder Variablen Spalten in abgeleiteten Tabellen nicht zuzulassen (sodass der Vorlage in Zukunft festgelegte oder Variablen Spalten hinzugefügt werden können).</span><span class="sxs-lookup"><span data-stu-id="3d3f8-141">Used in conjunction with JET_bitObjectTableTemplate to disallow fixed or variable columns in derived tables (so that fixed or variable columns can be added to the template in the future).</span></span></p>
<p><span data-ttu-id="3d3f8-142"><strong>Windows XP:  </strong> Dieser Wert wird in Windows XP eingeführt.</span><span class="sxs-lookup"><span data-stu-id="3d3f8-142"><strong>Windows XP:  </strong>This value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3d3f8-143">JET_bitObjectTableTemplate</span><span class="sxs-lookup"><span data-stu-id="3d3f8-143">JET_bitObjectTableTemplate</span></span></p></td>
<td><p><span data-ttu-id="3d3f8-144">Die Tabelle ist eine Vorlagen Tabelle.</span><span class="sxs-lookup"><span data-stu-id="3d3f8-144">The table is a template table.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="3d3f8-145">**crecord**</span><span class="sxs-lookup"><span data-stu-id="3d3f8-145">**cRecord**</span></span>

<span data-ttu-id="3d3f8-146">Die Anzahl der Datensätze in der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="3d3f8-146">The number of records in the table.</span></span>

<span data-ttu-id="3d3f8-147">Dieser Wert wird nur abgerufen, wenn **JET_OBJECTINFO** an [jetgetobjectinfo](./jetgetobjectinfo-function.md)übermittelt wurde.</span><span class="sxs-lookup"><span data-stu-id="3d3f8-147">This value is retrieved only if **JET_OBJECTINFO** was passed to [JetGetObjectInfo](./jetgetobjectinfo-function.md).</span></span>

<span data-ttu-id="3d3f8-148">**cpage**</span><span class="sxs-lookup"><span data-stu-id="3d3f8-148">**cPage**</span></span>

<span data-ttu-id="3d3f8-149">Die Anzahl der Seiten, die von der Tabelle verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3d3f8-149">The number of pages that are being used by the table.</span></span>

<span data-ttu-id="3d3f8-150">Dieser Wert wird nur abgerufen, wenn **JET_OBJECTINFO** an [jetgetobjectinfo](./jetgetobjectinfo-function.md)übermittelt wurde.</span><span class="sxs-lookup"><span data-stu-id="3d3f8-150">This value is retrieved only if **JET_OBJECTINFO** was passed to [JetGetObjectInfo](./jetgetobjectinfo-function.md).</span></span>

### <a name="remarks"></a><span data-ttu-id="3d3f8-151">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3d3f8-151">Remarks</span></span>

<span data-ttu-id="3d3f8-152">Eine **JET_OBJECTINFO** Struktur wird durch einen Aufrufen von [jetgetobjectinfo](./jetgetobjectinfo-function.md) oder [jetgettableinfo](./jetgettableinfo-function.md)aufgefüllt.</span><span class="sxs-lookup"><span data-stu-id="3d3f8-152">A **JET_OBJECTINFO** structure gets populated by a call to [JetGetObjectInfo](./jetgetobjectinfo-function.md) or [JetGetTableInfo](./jetgettableinfo-function.md).</span></span> <span data-ttu-id="3d3f8-153">Wenn der API-Befehl nicht erfolgreich ist, ist der Inhalt der Struktur nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="3d3f8-153">If the API call does not succeed, the contents of the structure are undefined.</span></span>

<span data-ttu-id="3d3f8-154">Falls zutreffend, enthält die Tabellen Statistik die Anzahl der Datensätze und die Anzahl der Seiten im gruppierten Index (d. h. den Index, der die Daten des Datensatzes enthält).</span><span class="sxs-lookup"><span data-stu-id="3d3f8-154">If applicable, the table statistics include the number of records and the number of pages that are in the clustered index (that is, the index containing the record data).</span></span> <span data-ttu-id="3d3f8-155">Der Zugriff auf die Index Statistiken erfolgt separat über den Namen, mithilfe von [jetgetindexinfo](./jetgetindexinfo-function.md) oder [jetgettableindexinfo](./jetgettableindexinfo-function.md).</span><span class="sxs-lookup"><span data-stu-id="3d3f8-155">The index statistics are accessed separately by name, using [JetGetIndexInfo](./jetgetindexinfo-function.md) or [JetGetTableIndexInfo](./jetgettableindexinfo-function.md).</span></span>

### <a name="requirements"></a><span data-ttu-id="3d3f8-156">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3d3f8-156">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3d3f8-157"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="3d3f8-157"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="3d3f8-158">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="3d3f8-158">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3d3f8-159"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="3d3f8-159"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="3d3f8-160">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="3d3f8-160">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3d3f8-161"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="3d3f8-161"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="3d3f8-162">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="3d3f8-162">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="3d3f8-163">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="3d3f8-163">See Also</span></span>

[<span data-ttu-id="3d3f8-164">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="3d3f8-164">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="3d3f8-165">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="3d3f8-165">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="3d3f8-166">JET_OBJTYP</span><span class="sxs-lookup"><span data-stu-id="3d3f8-166">JET_OBJTYP</span></span>](./jet-objtyp.md)  
[<span data-ttu-id="3d3f8-167">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="3d3f8-167">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="3d3f8-168">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="3d3f8-168">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="3d3f8-169">Jetgetindexinfo</span><span class="sxs-lookup"><span data-stu-id="3d3f8-169">JetGetIndexInfo</span></span>](./jetgetindexinfo-function.md)  
[<span data-ttu-id="3d3f8-170">Jetgetobjectinfo</span><span class="sxs-lookup"><span data-stu-id="3d3f8-170">JetGetObjectInfo</span></span>](./jetgetobjectinfo-function.md)  
[<span data-ttu-id="3d3f8-171">Jetgettableindexinfo</span><span class="sxs-lookup"><span data-stu-id="3d3f8-171">JetGetTableIndexInfo</span></span>](./jetgettableindexinfo-function.md)  
[<span data-ttu-id="3d3f8-172">Jetgettableinfo</span><span class="sxs-lookup"><span data-stu-id="3d3f8-172">JetGetTableInfo</span></span>](./jetgettableinfo-function.md)
