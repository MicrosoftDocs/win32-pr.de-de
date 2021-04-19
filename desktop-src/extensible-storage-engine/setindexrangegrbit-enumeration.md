---
description: 'Weitere Informationen finden Sie hier: setindexrangegrbit-Enumeration'
title: Setindexrangegrbit-Enumeration
TOCTitle: SetIndexRangeGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.setindexrangegrbit(v=EXCHG.10)
ms:contentKeyID: 39515181
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit
- Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit.None
- Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit.RangeInclusive
- Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit.RangeInstantDuration
- Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit.RangeRemove
- Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit.RangeUpperLimit
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit.RangeInstantDuration
- Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit.RangeUpperLimit
- Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit.None
- Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit.RangeInclusive
- Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit
- Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit.RangeRemove
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6cda73597f88d2c8fca911ebb96d7a3c6399ed9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106355509"
---
# <a name="setindexrangegrbit-enumeration"></a><span data-ttu-id="975a5-103">Setindexrangegrbit-Enumeration</span><span class="sxs-lookup"><span data-stu-id="975a5-103">SetIndexRangeGrbit enumeration</span></span>

<span data-ttu-id="975a5-104">Optionen für jetsetindexrange.</span><span class="sxs-lookup"><span data-stu-id="975a5-104">Options for JetSetIndexRange.</span></span>

<span data-ttu-id="975a5-105">Diese Enumeration enthält ein [FlagsAttribute](/dotnet/api/system.flagsattribute)-Attribut, das eine bitweise Kombination der Memberwerte zulässt.</span><span class="sxs-lookup"><span data-stu-id="975a5-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="975a5-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="975a5-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="975a5-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="975a5-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="975a5-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="975a5-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration SetIndexRangeGrbit
'Usage
Dim instance As SetIndexRangeGrbit
```

``` csharp
[FlagsAttribute]
public enum SetIndexRangeGrbit
```

## <a name="members"></a><span data-ttu-id="975a5-109">Member</span><span class="sxs-lookup"><span data-stu-id="975a5-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="975a5-110">Membername</span><span class="sxs-lookup"><span data-stu-id="975a5-110">Member name</span></span></th>
<th><span data-ttu-id="975a5-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="975a5-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="975a5-112">Keine</span><span class="sxs-lookup"><span data-stu-id="975a5-112">None</span></span></td>
<td><span data-ttu-id="975a5-113">Standardoptionen.</span><span class="sxs-lookup"><span data-stu-id="975a5-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="975a5-114">Rangeinen clusive</span><span class="sxs-lookup"><span data-stu-id="975a5-114">RangeInclusive</span></span></td>
<td><span data-ttu-id="975a5-115">Diese Option gibt an, dass die Beschränkung des Index Bereichs inklusiv ist.</span><span class="sxs-lookup"><span data-stu-id="975a5-115">This option indicates that the limit of the index range is inclusive.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="975a5-116">Rangeupperlimit</span><span class="sxs-lookup"><span data-stu-id="975a5-116">RangeUpperLimit</span></span></td>
<td><span data-ttu-id="975a5-117">Der Suchschlüssel im Cursor stellt die Suchkriterien für den Index Eintrag dar, der am nächsten am Ende des Indexes liegt, der mit dem Index Bereich übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="975a5-117">The search key in the cursor represents the search criteria for the index entry closest to the end of the index that will match the index range.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="975a5-118">Rangeinstantduration</span><span class="sxs-lookup"><span data-stu-id="975a5-118">RangeInstantDuration</span></span></td>
<td><span data-ttu-id="975a5-119">Der Index Bereich sollte entfernt werden, sobald er eingerichtet wurde.</span><span class="sxs-lookup"><span data-stu-id="975a5-119">The index range should be removed as soon as it has been established.</span></span> <span data-ttu-id="975a5-120">Dies ist hilfreich, um zu testen, ob Indexeinträge vorhanden sind, die mit den Suchkriterien übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="975a5-120">This is useful for testing for the existence of index entries that match the search criteria.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="975a5-121">Rangeremove</span><span class="sxs-lookup"><span data-stu-id="975a5-121">RangeRemove</span></span></td>
<td><span data-ttu-id="975a5-122">Abbrechen und vorhandener Index Bereich.</span><span class="sxs-lookup"><span data-stu-id="975a5-122">Cancel and existing index range.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="975a5-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="975a5-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="975a5-124">Referenz</span><span class="sxs-lookup"><span data-stu-id="975a5-124">Reference</span></span>

[<span data-ttu-id="975a5-125">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="975a5-125">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
