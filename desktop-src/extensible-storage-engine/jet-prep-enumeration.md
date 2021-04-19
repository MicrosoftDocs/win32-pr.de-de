---
description: 'Weitere Informationen finden Sie hier: JET_prep-Enumeration'
title: JET_prep-Enumeration
TOCTitle: JET_prep enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_prep
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_prep(v=EXCHG.10)
ms:contentKeyID: 39510193
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_prep.Replace
- Microsoft.Isam.Esent.Interop.JET_prep.InsertCopy
- Microsoft.Isam.Esent.Interop.JET_prep.Cancel
- Microsoft.Isam.Esent.Interop.JET_prep.Insert
- Microsoft.Isam.Esent.Interop.JET_prep.InsertCopyDeleteOriginal
- Microsoft.Isam.Esent.Interop.JET_prep
- Microsoft.Isam.Esent.Interop.JET_prep.ReplaceNoLock
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_prep.InsertCopyDeleteOriginal
- Microsoft.Isam.Esent.Interop.JET_prep.ReplaceNoLock
- Microsoft.Isam.Esent.Interop.JET_prep
- Microsoft.Isam.Esent.Interop.JET_prep.Cancel
- Microsoft.Isam.Esent.Interop.JET_prep.InsertCopy
- Microsoft.Isam.Esent.Interop.JET_prep.Insert
- Microsoft.Isam.Esent.Interop.JET_prep.Replace
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: edeaef8144fe6e13674ec6d3dfcb8adf7522e148
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106368964"
---
# <a name="jet_prep-enumeration"></a><span data-ttu-id="5fd38-103">JET_prep-Enumeration</span><span class="sxs-lookup"><span data-stu-id="5fd38-103">JET_prep enumeration</span></span>

<span data-ttu-id="5fd38-104">Update Typen für jetprepareupdate.</span><span class="sxs-lookup"><span data-stu-id="5fd38-104">Update types for JetPrepareUpdate.</span></span>

<span data-ttu-id="5fd38-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="5fd38-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="5fd38-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="5fd38-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="5fd38-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="5fd38-107">Syntax</span></span>

``` vb
'Declaration
Public Enumeration JET_prep
'Usage
Dim instance As JET_prep
```

``` csharp
public enum JET_prep
```

## <a name="members"></a><span data-ttu-id="5fd38-108">Member</span><span class="sxs-lookup"><span data-stu-id="5fd38-108">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="5fd38-109">Membername</span><span class="sxs-lookup"><span data-stu-id="5fd38-109">Member name</span></span></th>
<th><span data-ttu-id="5fd38-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5fd38-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="5fd38-111">Einfügen</span><span class="sxs-lookup"><span data-stu-id="5fd38-111">Insert</span></span></td>
<td><span data-ttu-id="5fd38-112">Dieses Flag bewirkt, dass der Cursor eine Einfügung eines neuen Datensatzes vorbereitet.</span><span class="sxs-lookup"><span data-stu-id="5fd38-112">This flag causes the cursor to prepare for an insert of a new record.</span></span> <span data-ttu-id="5fd38-113">Alle Daten werden auf den Standardstatus für den Datensatz initialisiert.</span><span class="sxs-lookup"><span data-stu-id="5fd38-113">All the data is initialized to the default state for the record.</span></span> <span data-ttu-id="5fd38-114">Wenn die Tabelle eine automatische Inkrement-Spalte aufweist, wird diesem Datensatz ein neuer Wert zugewiesen, unabhängig davon, ob das Update letztendlich erfolgreich ist, fehlschlägt oder abgebrochen wird.</span><span class="sxs-lookup"><span data-stu-id="5fd38-114">If the table has an auto-increment column, then a new value is assigned to this record regardless of whether the update ultimately succeeds, fails or is cancelled.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="5fd38-115">Replace</span><span class="sxs-lookup"><span data-stu-id="5fd38-115">Replace</span></span></td>
<td><span data-ttu-id="5fd38-116">Dieses Flag bewirkt, dass der Cursor eine Ersetzung des aktuellen Datensatzes vorbereitet.</span><span class="sxs-lookup"><span data-stu-id="5fd38-116">This flag causes the cursor to prepare for a replace of the current record.</span></span> <span data-ttu-id="5fd38-117">Wenn die Tabelle eine Versions Spalte aufweist, wird die Versions Spalte auf den nächsten Wert in der zugehörigen Reihenfolge festgelegt.</span><span class="sxs-lookup"><span data-stu-id="5fd38-117">If the table has a version column, then the version column is set to the next value in its sequence.</span></span> <span data-ttu-id="5fd38-118">Wenn dieses Update nicht vollständig ausgeführt wird, ist der Versions Wert im Datensatz nicht betroffen.</span><span class="sxs-lookup"><span data-stu-id="5fd38-118">If this update does not complete, then the version value in the record will be unaffected.</span></span> <span data-ttu-id="5fd38-119">Es wird eine Update Sperre für den Datensatz erstellt, um zu verhindern, dass dieser Datensatz von anderen Sitzungen aktualisiert wird, bevor diese Sitzung abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="5fd38-119">An update lock is taken on the record to prevent other sessions from updating this record before this session completes.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="5fd38-120">Abbrechen</span><span class="sxs-lookup"><span data-stu-id="5fd38-120">Cancel</span></span></td>
<td><span data-ttu-id="5fd38-121">Dieses Flag bewirkt, dass jetprepareupdate das Update für diesen Cursor abbricht.</span><span class="sxs-lookup"><span data-stu-id="5fd38-121">This flag causes JetPrepareUpdate to cancel the update for this cursor.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="5fd38-122">Replacumolock</span><span class="sxs-lookup"><span data-stu-id="5fd38-122">ReplaceNoLock</span></span></td>
<td><span data-ttu-id="5fd38-123">Dieses Flag ähnelt JET_prepReplace, es wird jedoch keine Sperre erstellt, um zu verhindern, dass andere Sitzungen diesen Datensatz aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="5fd38-123">This flag is similar to JET_prepReplace, but no lock is taken to prevent other sessions from updating this record.</span></span> <span data-ttu-id="5fd38-124">Stattdessen erhält diese Sitzung möglicherweise JET_errWriteConflict, wenn jetupdate aufgerufen wird, um das Update abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="5fd38-124">Instead, this session may receive JET_errWriteConflict when it calls JetUpdate to complete the update.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="5fd38-125">InsertCopy</span><span class="sxs-lookup"><span data-stu-id="5fd38-125">InsertCopy</span></span></td>
<td><span data-ttu-id="5fd38-126">Dieses Flag bewirkt, dass der Cursor eine Einfügung einer Kopie des vorhandenen Datensatzes vorbereitet.</span><span class="sxs-lookup"><span data-stu-id="5fd38-126">This flag causes the cursor to prepare for an insert of a copy of the existing record.</span></span> <span data-ttu-id="5fd38-127">Wenn diese Option verwendet wird, muss ein aktueller Datensatz vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="5fd38-127">There must be a current record if this option is used.</span></span> <span data-ttu-id="5fd38-128">Der ursprüngliche Zustand des neuen Datensatzes wird aus dem aktuellen Datensatz kopiert.</span><span class="sxs-lookup"><span data-stu-id="5fd38-128">The initial state of the new record is copied from the current record.</span></span> <span data-ttu-id="5fd38-129">Lange Werte, die außerhalb des Datensatzes gespeichert werden, werden virtuell kopiert.</span><span class="sxs-lookup"><span data-stu-id="5fd38-129">Long values that are stored off-record are virtually copied.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="5fd38-130">Insertcopydeleteoriginal</span><span class="sxs-lookup"><span data-stu-id="5fd38-130">InsertCopyDeleteOriginal</span></span></td>
<td><span data-ttu-id="5fd38-131">Dieses Flag bewirkt, dass der Cursor eine Einfügung desselben Datensatzes und einen Löschvorgang oder den ursprünglichen Datensatz vorbereitet.</span><span class="sxs-lookup"><span data-stu-id="5fd38-131">This flag causes the cursor to prepare for an insert of the same record, and a delete or the original record.</span></span> <span data-ttu-id="5fd38-132">Sie wird in Fällen verwendet, in denen sich der Primärschlüssel geändert hat.</span><span class="sxs-lookup"><span data-stu-id="5fd38-132">It is used in cases in which the primary key has changed.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="5fd38-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5fd38-133">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="5fd38-134">Referenz</span><span class="sxs-lookup"><span data-stu-id="5fd38-134">Reference</span></span>

[<span data-ttu-id="5fd38-135">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="5fd38-135">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
