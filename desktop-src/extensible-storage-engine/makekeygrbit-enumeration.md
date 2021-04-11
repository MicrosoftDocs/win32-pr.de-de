---
description: 'Weitere Informationen finden Sie hier: makekeygrbit-Enumeration'
title: Makekeygrbit-Enumeration
TOCTitle: MakeKeyGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.MakeKeyGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.makekeygrbit(v=EXCHG.10)
ms:contentKeyID: 39511453
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.FullColumnEndLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.SubStrLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.FullColumnStartLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.PartialColumnStartLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.PartialColumnEndLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.None
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.NewKey
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.StrLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.NormalizedKey
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.KeyDataZeroLength
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.FullColumnEndLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.None
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.NormalizedKey
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.FullColumnStartLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.StrLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.KeyDataZeroLength
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.NewKey
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.PartialColumnEndLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.SubStrLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.PartialColumnStartLimit
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1c19a8c24b5adc4e8655c5372bd9c374e8674e9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128625"
---
# <a name="makekeygrbit-enumeration"></a><span data-ttu-id="fadd7-103">Makekeygrbit-Enumeration</span><span class="sxs-lookup"><span data-stu-id="fadd7-103">MakeKeyGrbit enumeration</span></span>

<span data-ttu-id="fadd7-104">Optionen für jetmakekey.</span><span class="sxs-lookup"><span data-stu-id="fadd7-104">Options for JetMakeKey.</span></span>

<span data-ttu-id="fadd7-105">Diese Enumeration enthält ein [FlagsAttribute](/dotnet/api/system.flagsattribute)-Attribut, das eine bitweise Kombination der Memberwerte zulässt.</span><span class="sxs-lookup"><span data-stu-id="fadd7-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="fadd7-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="fadd7-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="fadd7-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="fadd7-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="fadd7-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="fadd7-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration MakeKeyGrbit
'Usage
Dim instance As MakeKeyGrbit
```

``` csharp
[FlagsAttribute]
public enum MakeKeyGrbit
```

## <a name="members"></a><span data-ttu-id="fadd7-109">Member</span><span class="sxs-lookup"><span data-stu-id="fadd7-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="fadd7-110">Membername</span><span class="sxs-lookup"><span data-stu-id="fadd7-110">Member name</span></span></th>
<th><span data-ttu-id="fadd7-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fadd7-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="fadd7-112">Keine</span><span class="sxs-lookup"><span data-stu-id="fadd7-112">None</span></span></td>
<td><span data-ttu-id="fadd7-113">Standardoptionen.</span><span class="sxs-lookup"><span data-stu-id="fadd7-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="fadd7-114">NewKey</span><span class="sxs-lookup"><span data-stu-id="fadd7-114">NewKey</span></span></td>
<td><span data-ttu-id="fadd7-115">Es muss ein neuer Suchschlüssel erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="fadd7-115">A new search key should be constructed.</span></span> <span data-ttu-id="fadd7-116">Alle bereits vorhandenen Suchschlüssel werden verworfen.</span><span class="sxs-lookup"><span data-stu-id="fadd7-116">Any previously existing search key is discarded.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="fadd7-117">Normalizedkey</span><span class="sxs-lookup"><span data-stu-id="fadd7-117">NormalizedKey</span></span></td>
<td><span data-ttu-id="fadd7-118">Wenn diese Option angegeben wird, werden alle anderen Optionen ignoriert, alle bereits vorhandenen Suchschlüssel werden verworfen, und der Inhalt des Eingabe Puffers wird als neuer Suchschlüssel geladen.</span><span class="sxs-lookup"><span data-stu-id="fadd7-118">When this option is specified, all other options are ignored, any previously existing search key is discarded, and the contents of the input buffer are loaded as the new search key.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="fadd7-119">Keydatazerolength</span><span class="sxs-lookup"><span data-stu-id="fadd7-119">KeyDataZeroLength</span></span></td>
<td><span data-ttu-id="fadd7-120">Wenn die Größe des Eingabe Puffers NULL und die aktuelle Schlüssel Spalte eine Spalte variabler Länge ist, gibt diese Option an, dass der Eingabepuffer den Wert 0 (null) enthält.</span><span class="sxs-lookup"><span data-stu-id="fadd7-120">If the size of the input buffer is zero and the current key column is a variable length column, this option indicates that the input buffer contains a zero length value.</span></span> <span data-ttu-id="fadd7-121">Andernfalls würde eine Eingabepuffergröße von NULL einen NULL-Wert angeben.</span><span class="sxs-lookup"><span data-stu-id="fadd7-121">Otherwise, an input buffer size of zero would indicate a NULL value.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="fadd7-122">Obergrenze</span><span class="sxs-lookup"><span data-stu-id="fadd7-122">StrLimit</span></span></td>
<td><span data-ttu-id="fadd7-123">Diese Option gibt an, dass der Suchschlüssel so erstellt werden soll, dass alle Schlüssel Spalten, die nach der aktuellen Schlüssel Spalte liegen, als Platzhalter betrachtet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="fadd7-123">This option indicates that the search key should be constructed such that any key columns that come after the current key column should be considered to be wildcards.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="fadd7-124">SubStrLimit</span><span class="sxs-lookup"><span data-stu-id="fadd7-124">SubStrLimit</span></span></td>
<td><span data-ttu-id="fadd7-125">Diese Option gibt an, dass der Suchschlüssel so erstellt werden soll, dass die aktuelle Schlüssel Spalte als Präfix-Platzhalter angesehen wird und dass alle Schlüssel Spalten, die nach der aktuellen Schlüssel Spalte liegen, als Platzhalter betrachtet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="fadd7-125">This option indicates that the search key should be constructed such that the current key column is considered to be a prefix wildcard and that any key columns that come after the current key column should be considered to be wildcards.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="fadd7-126">Fullcolumnstartlimit</span><span class="sxs-lookup"><span data-stu-id="fadd7-126">FullColumnStartLimit</span></span></td>
<td><span data-ttu-id="fadd7-127">Der Suchschlüssel sollte so erstellt werden, dass alle Schlüssel Spalten, die nach der aktuellen Schlüssel Spalte liegen, als Platzhalter betrachtet werden.</span><span class="sxs-lookup"><span data-stu-id="fadd7-127">The search key should be constructed such that any key columns that come after the current key column should be considered to be wildcards.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="fadd7-128">Fullcolumnendlimit</span><span class="sxs-lookup"><span data-stu-id="fadd7-128">FullColumnEndLimit</span></span></td>
<td><span data-ttu-id="fadd7-129">Der Suchschlüssel sollte so erstellt werden, dass alle Schlüssel Spalten, die nach der aktuellen Schlüssel Spalte liegen, als Platzhalter betrachtet werden.</span><span class="sxs-lookup"><span data-stu-id="fadd7-129">The search key should be constructed in such a way that any key columns that come after the current key column are considered to be wildcards.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="fadd7-130">Partialcolumnstartlimit</span><span class="sxs-lookup"><span data-stu-id="fadd7-130">PartialColumnStartLimit</span></span></td>
<td><span data-ttu-id="fadd7-131">Der Suchschlüssel sollte so erstellt werden, dass die aktuelle Schlüssel Spalte als Präfix-Platzhalter angesehen wird und dass alle Schlüssel Spalten, die nach der aktuellen Schlüssel Spalte liegen, als Platzhalter betrachtet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="fadd7-131">The search key should be constructed such that the current key column is considered to be a prefix wildcard and that any key columns that come after the current key column should be considered to be wildcards.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="fadd7-132">Partialcolumnendlimit</span><span class="sxs-lookup"><span data-stu-id="fadd7-132">PartialColumnEndLimit</span></span></td>
<td><span data-ttu-id="fadd7-133">Der Suchschlüssel sollte so erstellt werden, dass die aktuelle Schlüssel Spalte als Präfix-Platzhalter angesehen wird und dass alle Schlüssel Spalten, die nach der aktuellen Schlüssel Spalte liegen, als Platzhalter betrachtet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="fadd7-133">The search key should be constructed such that the current key column is considered to be a prefix wildcard and that any key columns that come after the current key column should be considered to be wildcards.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="fadd7-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fadd7-134">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="fadd7-135">Referenz</span><span class="sxs-lookup"><span data-stu-id="fadd7-135">Reference</span></span>

[<span data-ttu-id="fadd7-136">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="fadd7-136">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
