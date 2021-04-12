---
description: 'Weitere Informationen finden Sie hier: JET_OBJECTLIST Struktur'
title: JET_OBJECTLIST-Struktur
TOCTitle: JET_OBJECTLIST Structure
ms:assetid: 95f12f2a-13da-48d4-a254-fc0cb718b17d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269348(v=EXCHG.10)
ms:contentKeyID: 32765635
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- kbArticle
- apiref
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a7a66bb3b7f7dfbbfd1087d1fe0ce32c4144a8bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347518"
---
# <a name="jet_objectlist-structure"></a><span data-ttu-id="21949-103">JET_OBJECTLIST-Struktur</span><span class="sxs-lookup"><span data-stu-id="21949-103">JET_OBJECTLIST Structure</span></span>


<span data-ttu-id="21949-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="21949-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_objectlist-structure"></a><span data-ttu-id="21949-105">JET_OBJECTLIST-Struktur</span><span class="sxs-lookup"><span data-stu-id="21949-105">JET_OBJECTLIST Structure</span></span>

<span data-ttu-id="21949-106">Die **JET_OBJECTLIST** -Struktur durchläuft eine temporäre Tabelle, die mit [jetgetobjectinfo](./jetgetobjectinfo-function.md)erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="21949-106">The **JET_OBJECTLIST** structure traverses a temporary table that was created with [JetGetObjectInfo](./jetgetobjectinfo-function.md).</span></span> <span data-ttu-id="21949-107">Jede Zeile in der temporären Tabelle beschreibt ein Objekt in der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="21949-107">Each row in the temporary table describes an object in the database.</span></span>

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_TABLEID tableid;
      unsigned long cRecord;
      JET_COLUMNID columnidcontainername;
      JET_COLUMNID columnidobjectname;
      JET_COLUMNID columnidobjtyp;
      JET_COLUMNID columniddtCreate;
      JET_COLUMNID columniddtUpdate;
      JET_COLUMNID columnidgrbit;
      JET_COLUMNID columnidflags;
      JET_COLUMNID columnidcRecord;
      JET_COLUMNID columnidcPage;
    } JET_OBJECTLIST;
```

### <a name="members"></a><span data-ttu-id="21949-108">Member</span><span class="sxs-lookup"><span data-stu-id="21949-108">Members</span></span>

<span data-ttu-id="21949-109">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="21949-109">**cbStruct**</span></span>

<span data-ttu-id="21949-110">Die Größe der-Struktur in Bytes.</span><span class="sxs-lookup"><span data-stu-id="21949-110">The size of the structure, in bytes.</span></span> <span data-ttu-id="21949-111">Der API-Aufruf aktualisiert dieses Feld, sodass der Aufrufer sicherstellen muss, dass dieser Wert sizeof (JET_INDEXLIST) entspricht.</span><span class="sxs-lookup"><span data-stu-id="21949-111">The API call will update this field, so the caller should ensure that this value matches sizeof( JET_INDEXLIST ).</span></span>

<span data-ttu-id="21949-112">**TableID**</span><span class="sxs-lookup"><span data-stu-id="21949-112">**tableid**</span></span>

<span data-ttu-id="21949-113">Der Tabellen Bezeichner der temporären Tabelle, die erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="21949-113">The table identifier of the temporary table that was created.</span></span> <span data-ttu-id="21949-114">Der Aufrufer muss Code enthalten, der die Tabelle schließt.</span><span class="sxs-lookup"><span data-stu-id="21949-114">The caller must contain code that will close the table.</span></span>

<span data-ttu-id="21949-115">**crecord**</span><span class="sxs-lookup"><span data-stu-id="21949-115">**cRecord**</span></span>

<span data-ttu-id="21949-116">Die Anzahl der Datensätze in der temporären Tabelle, die erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="21949-116">The number of records in the temporary table that was created.</span></span>

<span data-ttu-id="21949-117">**columnidcontainername**</span><span class="sxs-lookup"><span data-stu-id="21949-117">**columnidcontainername**</span></span>

<span data-ttu-id="21949-118">Der Spalten Bezeichner des Namens des Container Typs.</span><span class="sxs-lookup"><span data-stu-id="21949-118">The column identifier of the name of the type of container.</span></span>

<span data-ttu-id="21949-119">Die einzigen derzeit unterstützten Container sind Tabellen.</span><span class="sxs-lookup"><span data-stu-id="21949-119">The only containers that are currently supported are tables.</span></span> <span data-ttu-id="21949-120">Diese Spalte ist eine [JET_coltypText](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="21949-120">This column is a [JET_coltypText](./jet-coltyp.md).</span></span>

<span data-ttu-id="21949-121">**columnidobjectname**</span><span class="sxs-lookup"><span data-stu-id="21949-121">**columnidobjectname**</span></span>

<span data-ttu-id="21949-122">Der Spalten Bezeichner des Namens des Objekts.</span><span class="sxs-lookup"><span data-stu-id="21949-122">The column identifier of the name of the object.</span></span>

<span data-ttu-id="21949-123">Diese Spalte ist eine [JET_coltypText](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="21949-123">This column is a [JET_coltypText](./jet-coltyp.md).</span></span>

<span data-ttu-id="21949-124">**columnidobjyp**</span><span class="sxs-lookup"><span data-stu-id="21949-124">**columnidobjtyp**</span></span>

<span data-ttu-id="21949-125">Der Spalten Bezeichner des Typs des Objekts.</span><span class="sxs-lookup"><span data-stu-id="21949-125">The column identifier of the type of the object.</span></span> <span data-ttu-id="21949-126">Die einzigen derzeit unterstützten Container sind Tabellen, sodass dieses Feld JET_objtypTable wird.</span><span class="sxs-lookup"><span data-stu-id="21949-126">The only containers that are currently supported are tables, so this field will be JET_objtypTable.</span></span>

<span data-ttu-id="21949-127">Diese Spalte ist eine [JET_coltypLong](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="21949-127">This column is a [JET_coltypLong](./jet-coltyp.md).</span></span>

<span data-ttu-id="21949-128">**columniddtcreate**</span><span class="sxs-lookup"><span data-stu-id="21949-128">**columniddtCreate**</span></span>

<span data-ttu-id="21949-129">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="21949-129">Obsolete.</span></span> <span data-ttu-id="21949-130">Darf nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="21949-130">Do not use.</span></span>

<span data-ttu-id="21949-131">**columniddtupdate**</span><span class="sxs-lookup"><span data-stu-id="21949-131">**columniddtUpdate**</span></span>

<span data-ttu-id="21949-132">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="21949-132">Obsolete.</span></span> <span data-ttu-id="21949-133">Darf nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="21949-133">Do not use.</span></span>

<span data-ttu-id="21949-134">**columnidgrbit**</span><span class="sxs-lookup"><span data-stu-id="21949-134">**columnidgrbit**</span></span>

<span data-ttu-id="21949-135">Der Spalten Bezeichner der **grbits** , die auf das-Objekt anwendbar sind.</span><span class="sxs-lookup"><span data-stu-id="21949-135">The column identifier of the **grbits** that are applicable to the object.</span></span> <span data-ttu-id="21949-136">Eine Liste der anwendbaren **grbits** finden Sie unter [JET_TABLECREATE](./jet-tablecreate-structure.md).</span><span class="sxs-lookup"><span data-stu-id="21949-136">For a list of applicable **grbits**, see [JET_TABLECREATE](./jet-tablecreate-structure.md).</span></span>

<span data-ttu-id="21949-137">Diese Spalte ist eine [JET_coltypLong](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="21949-137">This column is a [JET_coltypLong](./jet-coltyp.md).</span></span>

<span data-ttu-id="21949-138">**columnidflags**</span><span class="sxs-lookup"><span data-stu-id="21949-138">**columnidflags**</span></span>

<span data-ttu-id="21949-139">Der Spalten Bezeichner der Flags, die auf das-Objekt anwendbar sind.</span><span class="sxs-lookup"><span data-stu-id="21949-139">The column identifier of the flags that are applicable to the object.</span></span> <span data-ttu-id="21949-140">Eine Liste der anwendbaren Flags finden Sie unter [JET_OBJECTINFO](./jet-objectinfo-structure.md).</span><span class="sxs-lookup"><span data-stu-id="21949-140">For a list of applicable flags, see [JET_OBJECTINFO](./jet-objectinfo-structure.md).</span></span>

<span data-ttu-id="21949-141">Diese Spalte ist eine [JET_coltypLong](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="21949-141">This column is a [JET_coltypLong](./jet-coltyp.md).</span></span>

<span data-ttu-id="21949-142">**columnidcrecord**</span><span class="sxs-lookup"><span data-stu-id="21949-142">**columnidcRecord**</span></span>

<span data-ttu-id="21949-143">Der Spalten Bezeichner der Anzahl von Datensätzen, die in der Tabelle vorhanden sind, die in **columnidobjectname** benannt ist.</span><span class="sxs-lookup"><span data-stu-id="21949-143">The column identifier of the number of records that are present in the table that is named in **columnidobjectname**.</span></span>

<span data-ttu-id="21949-144">Diese Spalte ist eine [JET_coltypLong](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="21949-144">This column is a [JET_coltypLong](./jet-coltyp.md).</span></span>

<span data-ttu-id="21949-145">**columnidcpage**</span><span class="sxs-lookup"><span data-stu-id="21949-145">**columnidcPage**</span></span>

<span data-ttu-id="21949-146">Der Spalten Bezeichner der Anzahl der Seiten, die vom-Objekt verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="21949-146">The column identifier of the number of pages the object uses.</span></span>

<span data-ttu-id="21949-147">Diese Spalte ist eine [JET_coltypLong](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="21949-147">This column is a [JET_coltypLong](./jet-coltyp.md).</span></span>

### <a name="remarks"></a><span data-ttu-id="21949-148">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="21949-148">Remarks</span></span>

<span data-ttu-id="21949-149">Jede Zeile in der temporären Tabelle entspricht einem Objekt in der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="21949-149">Each row in the temporary table corresponds to an object in the database.</span></span>

<span data-ttu-id="21949-150">Wenn die temporäre Tabelle mit dem *infolevel* -Parameter in der [jetgetobjectinfo](./jetgetobjectinfo-function.md) -Funktion auf JET_ObjInfoListNoStats festgelegt wird, enthalten die von **columnidcrecord** und **columnidcpage** identifizierten Spalten keine aussagekräftigen Informationen.</span><span class="sxs-lookup"><span data-stu-id="21949-150">When the temporary table is created with the *InfoLevel* parameter in the [JetGetObjectInfo](./jetgetobjectinfo-function.md) function set to JET_ObjInfoListNoStats, the columns identified by **columnidcRecord** and **columnidcPage** will not contain meaningful information.</span></span>

<span data-ttu-id="21949-151">Derzeit werden nur Informationen zu Tabellen in der temporären Tabelle angezeigt.</span><span class="sxs-lookup"><span data-stu-id="21949-151">Currently, only information about tables will be in the temporary table.</span></span>

### <a name="requirements"></a><span data-ttu-id="21949-152">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="21949-152">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="21949-153"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="21949-153"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="21949-154">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="21949-154">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="21949-155"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="21949-155"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="21949-156">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="21949-156">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="21949-157"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="21949-157"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="21949-158">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="21949-158">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="21949-159">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="21949-159">See Also</span></span>

[<span data-ttu-id="21949-160">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="21949-160">JET_COLTYP</span></span>](./jet-coltyp.md)  
[<span data-ttu-id="21949-161">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="21949-161">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="21949-162">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="21949-162">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="21949-163">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="21949-163">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="21949-164">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="21949-164">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="21949-165">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="21949-165">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="21949-166">JET_OBJECTINFO</span><span class="sxs-lookup"><span data-stu-id="21949-166">JET_OBJECTINFO</span></span>](./jet-objectinfo-structure.md)  
[<span data-ttu-id="21949-167">JET_TABLECREATE</span><span class="sxs-lookup"><span data-stu-id="21949-167">JET_TABLECREATE</span></span>](./jet-tablecreate-structure.md)  
[<span data-ttu-id="21949-168">Jetgetobjectinfo</span><span class="sxs-lookup"><span data-stu-id="21949-168">JetGetObjectInfo</span></span>](./jetgetobjectinfo-function.md)
