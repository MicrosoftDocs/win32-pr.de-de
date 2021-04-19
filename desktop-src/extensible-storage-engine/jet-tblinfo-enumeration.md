---
description: 'Weitere Informationen finden Sie hier: JET_TblInfo-Enumeration'
title: JET_TblInfo-Enumeration
TOCTitle: JET_TblInfo enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_TblInfo
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_tblinfo(v=EXCHG.10)
ms:contentKeyID: 39512198
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_TblInfo
- Microsoft.Isam.Esent.Interop.JET_TblInfo.Dbid
- Microsoft.Isam.Esent.Interop.JET_TblInfo.TemplateTableName
- Microsoft.Isam.Esent.Interop.JET_TblInfo.SpaceUsage
- Microsoft.Isam.Esent.Interop.JET_TblInfo.SpaceAlloc
- Microsoft.Isam.Esent.Interop.JET_TblInfo.Name
- Microsoft.Isam.Esent.Interop.JET_TblInfo.Default
- Microsoft.Isam.Esent.Interop.JET_TblInfo.SpaceAvailable
- Microsoft.Isam.Esent.Interop.JET_TblInfo.SpaceOwned
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_TblInfo
- Microsoft.Isam.Esent.Interop.JET_TblInfo.Dbid
- Microsoft.Isam.Esent.Interop.JET_TblInfo.Default
- Microsoft.Isam.Esent.Interop.JET_TblInfo.TemplateTableName
- Microsoft.Isam.Esent.Interop.JET_TblInfo.Name
- Microsoft.Isam.Esent.Interop.JET_TblInfo.SpaceAvailable
- Microsoft.Isam.Esent.Interop.JET_TblInfo.SpaceOwned
- Microsoft.Isam.Esent.Interop.JET_TblInfo.SpaceUsage
- Microsoft.Isam.Esent.Interop.JET_TblInfo.SpaceAlloc
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ad43dcecf65fdc9fb8dd53bdf686a077e6bdfa8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349455"
---
# <a name="jet_tblinfo-enumeration"></a><span data-ttu-id="d57c7-103">JET_TblInfo-Enumeration</span><span class="sxs-lookup"><span data-stu-id="d57c7-103">JET_TblInfo enumeration</span></span>

<span data-ttu-id="d57c7-104">Informationsebenen zum Abrufen von Tabellen Informationen mit jetgettableinfo.</span><span class="sxs-lookup"><span data-stu-id="d57c7-104">Info levels for retrieving table info with JetGetTableInfo.</span></span>

<span data-ttu-id="d57c7-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="d57c7-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="d57c7-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="d57c7-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="d57c7-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="d57c7-107">Syntax</span></span>

``` vb
'Declaration
Public Enumeration JET_TblInfo
'Usage
Dim instance As JET_TblInfo
```

``` csharp
public enum JET_TblInfo
```

## <a name="members"></a><span data-ttu-id="d57c7-108">Member</span><span class="sxs-lookup"><span data-stu-id="d57c7-108">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="d57c7-109">Membername</span><span class="sxs-lookup"><span data-stu-id="d57c7-109">Member name</span></span></th>
<th><span data-ttu-id="d57c7-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d57c7-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="d57c7-111">Standard</span><span class="sxs-lookup"><span data-stu-id="d57c7-111">Default</span></span></td>
<td><span data-ttu-id="d57c7-112">Standardoption</span><span class="sxs-lookup"><span data-stu-id="d57c7-112">Default option.</span></span> <span data-ttu-id="d57c7-113">Ruft ein <a href="dn335219(v=exchg.10).md">JET_OBJECTINFO</a> ab, das Informationen zur Tabelle enthält.</span><span class="sxs-lookup"><span data-stu-id="d57c7-113">Retrieves a <a href="dn335219(v=exchg.10).md">JET_OBJECTINFO</a> containing information about the table.</span></span> <span data-ttu-id="d57c7-114">Verwenden Sie diese Option mit <a href="dn292198(v=exchg.10).md">jetgettableinfo (JET_SESID, JET_TABLEID, JET_OBJECTINFO, JET_TblInfo)</a>.</span><span class="sxs-lookup"><span data-stu-id="d57c7-114">Use this option with <a href="dn292198(v=exchg.10).md">JetGetTableInfo(JET_SESID, JET_TABLEID, JET_OBJECTINFO, JET_TblInfo)</a>.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="d57c7-115">Name</span><span class="sxs-lookup"><span data-stu-id="d57c7-115">Name</span></span></td>
<td><span data-ttu-id="d57c7-116">Ruft den Namen der Tabelle ab.</span><span class="sxs-lookup"><span data-stu-id="d57c7-116">Retrieves the name of the table.</span></span> <span data-ttu-id="d57c7-117">Verwenden Sie diese Option mit <a href="dn292204(v=exchg.10).md">jetgettableinfo (JET_SESID, JET_TABLEID, String, JET_TblInfo)</a>.</span><span class="sxs-lookup"><span data-stu-id="d57c7-117">Use this option with <a href="dn292204(v=exchg.10).md">JetGetTableInfo(JET_SESID, JET_TABLEID, String, JET_TblInfo)</a>.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="d57c7-118">Dbid</span><span class="sxs-lookup"><span data-stu-id="d57c7-118">Dbid</span></span></td>
<td><span data-ttu-id="d57c7-119">Ruft den <a href="hh596176(v=exchg.10).md">JET_DBID</a> der Datenbank ab, die die Tabelle enthält.</span><span class="sxs-lookup"><span data-stu-id="d57c7-119">Retrieves the <a href="hh596176(v=exchg.10).md">JET_DBID</a> of the database containing the table.</span></span> <span data-ttu-id="d57c7-120">Verwenden Sie diese Option mit <a href="dn292197(v=exchg.10).md">jetgettableinfo (JET_SESID, JET_TABLEID, JET_DBID, JET_TblInfo)</a>.</span><span class="sxs-lookup"><span data-stu-id="d57c7-120">Use this option with <a href="dn292197(v=exchg.10).md">JetGetTableInfo(JET_SESID, JET_TABLEID, JET_DBID, JET_TblInfo)</a>.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="d57c7-121">Spaceusage</span><span class="sxs-lookup"><span data-stu-id="d57c7-121">SpaceUsage</span></span></td>
<td><span data-ttu-id="d57c7-122">Das Verhalten der-Methode hängt von der Größe des Arrays ab, das an die-Methode weitergegeben wird.</span><span class="sxs-lookup"><span data-stu-id="d57c7-122">The behavior of the method depends on how large the array that is passed to the method is.</span></span> <span data-ttu-id="d57c7-123">Das Array muss mindestens zwei Einträge enthalten.</span><span class="sxs-lookup"><span data-stu-id="d57c7-123">The array must have at least two entries.</span></span> <span data-ttu-id="d57c7-124">Der erste Eintrag enthält die Anzahl der im Besitz befindlichen Blöcke in der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="d57c7-124">The first entry will contain the number of Owned Extents in the table.</span></span> <span data-ttu-id="d57c7-125">Der zweite Eintrag enthält die Anzahl der verfügbaren Blöcke in der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="d57c7-125">The second entry will contain the number of Available Extents in the table.</span></span> <span data-ttu-id="d57c7-126">Wenn das Array mehr als zwei Einträge enthält, bestehen die verbleibenden Bytes des Puffers aus einem Array von-Strukturen, die eine Liste von Blöcken darstellen.</span><span class="sxs-lookup"><span data-stu-id="d57c7-126">If the array has more than two entries then the remaining bytes of the buffer will consist of an array of structures that represent a list of extents.</span></span> <span data-ttu-id="d57c7-127">Diese Struktur enthält zwei Member: die letzte Seitenzahl im Block und die Anzahl der Seiten im Wertebereich.</span><span class="sxs-lookup"><span data-stu-id="d57c7-127">This structure contains two members: the last page number in the extent and the number of pages in the extent.</span></span> <span data-ttu-id="d57c7-128">Verwenden Sie diese Option mit <a href="dn292202(v=exchg.10).md">jetgettableinfo (JET_SESID, JET_TABLEID, [], JET_TblInfo)</a>.</span><span class="sxs-lookup"><span data-stu-id="d57c7-128">Use this option with <a href="dn292202(v=exchg.10).md">JetGetTableInfo(JET_SESID, JET_TABLEID, [], JET_TblInfo)</a>.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="d57c7-129">Spacezuweisung</span><span class="sxs-lookup"><span data-stu-id="d57c7-129">SpaceAlloc</span></span></td>
<td><span data-ttu-id="d57c7-130">Das an jetgettableinfo über gegebene Array muss über zwei Einträge verfügen.</span><span class="sxs-lookup"><span data-stu-id="d57c7-130">The array passed to JetGetTableInfo must have two entries.</span></span> <span data-ttu-id="d57c7-131">Der erste Eintrag wird auf die Anzahl der Seiten in der Tabelle festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d57c7-131">The first entry will be set to the number of pages in the table.</span></span> <span data-ttu-id="d57c7-132">Der zweite Eintrag wird auf die zieldichte von Seiten für die Tabelle festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d57c7-132">The second entry will be set to the target density of pages for the table.</span></span> <span data-ttu-id="d57c7-133">Verwenden Sie diese Option mit <a href="dn292202(v=exchg.10).md">jetgettableinfo (JET_SESID, JET_TABLEID, [], JET_TblInfo)</a>.</span><span class="sxs-lookup"><span data-stu-id="d57c7-133">Use this option with <a href="dn292202(v=exchg.10).md">JetGetTableInfo(JET_SESID, JET_TABLEID, [], JET_TblInfo)</a>.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="d57c7-134">Leerraum</span><span class="sxs-lookup"><span data-stu-id="d57c7-134">SpaceOwned</span></span></td>
<td><span data-ttu-id="d57c7-135">Ruft die Anzahl der eigenen Seiten in der Tabelle ab.</span><span class="sxs-lookup"><span data-stu-id="d57c7-135">Gets the number of owned pages in the table.</span></span> <span data-ttu-id="d57c7-136">Verwenden Sie diese Option mit <a href="dn292201(v=exchg.10).md">jetgettableinfo (JET_SESID, JET_TABLEID, Int32, JET_TblInfo)</a>.</span><span class="sxs-lookup"><span data-stu-id="d57c7-136">Use this option with <a href="dn292201(v=exchg.10).md">JetGetTableInfo(JET_SESID, JET_TABLEID, Int32, JET_TblInfo)</a>.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="d57c7-137">Leerraum verfügbar</span><span class="sxs-lookup"><span data-stu-id="d57c7-137">SpaceAvailable</span></span></td>
<td><span data-ttu-id="d57c7-138">Ruft die Anzahl der verfügbaren Seiten in der Tabelle ab.</span><span class="sxs-lookup"><span data-stu-id="d57c7-138">Gets the number of available pages in the table.</span></span> <span data-ttu-id="d57c7-139">Verwenden Sie diese Option mit <a href="dn292201(v=exchg.10).md">jetgettableinfo (JET_SESID, JET_TABLEID, Int32, JET_TblInfo)</a>.</span><span class="sxs-lookup"><span data-stu-id="d57c7-139">Use this option with <a href="dn292201(v=exchg.10).md">JetGetTableInfo(JET_SESID, JET_TABLEID, Int32, JET_TblInfo)</a>.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="d57c7-140">Templatetablename</span><span class="sxs-lookup"><span data-stu-id="d57c7-140">TemplateTableName</span></span></td>
<td><span data-ttu-id="d57c7-141">Wenn die Tabelle eine abgeleitete Tabelle ist, wird das Ergebnis mit dem Namen der Tabelle ausgefüllt, von der die abgeleitete Tabelle Ihre DDL geerbt hat.</span><span class="sxs-lookup"><span data-stu-id="d57c7-141">If the table is a derived table, the result will be filled in with the name of the table from which the derived table inherited its DDL.</span></span> <span data-ttu-id="d57c7-142">Wenn die Tabelle keine abgeleitete Tabelle ist, wird für den Puffer eine leere Zeichenfolge verwendet.</span><span class="sxs-lookup"><span data-stu-id="d57c7-142">If the table is not a derived table, the buffer will an empty string.</span></span> <span data-ttu-id="d57c7-143">Verwenden Sie diese Option mit <a href="dn292204(v=exchg.10).md">jetgettableinfo (JET_SESID, JET_TABLEID, String, JET_TblInfo)</a>.</span><span class="sxs-lookup"><span data-stu-id="d57c7-143">Use this option with <a href="dn292204(v=exchg.10).md">JetGetTableInfo(JET_SESID, JET_TABLEID, String, JET_TblInfo)</a>.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="d57c7-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d57c7-144">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d57c7-145">Referenz</span><span class="sxs-lookup"><span data-stu-id="d57c7-145">Reference</span></span>

[<span data-ttu-id="d57c7-146">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="d57c7-146">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
