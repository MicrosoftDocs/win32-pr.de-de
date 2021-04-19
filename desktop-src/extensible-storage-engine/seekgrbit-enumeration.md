---
description: Weitere Informationen finden Sie in der seekgrbit-Enumeration.
title: Seekgrbit-Enumeration
TOCTitle: SeekGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.SeekGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.seekgrbit(v=EXCHG.10)
ms:contentKeyID: 39515862
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SeekGrbit
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekEQ
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekGE
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekGT
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekLE
- Microsoft.Isam.Esent.Interop.SeekGrbit.SetIndexRange
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekLT
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekGT
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekLT
- Microsoft.Isam.Esent.Interop.SeekGrbit.SetIndexRange
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekGE
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekLE
- Microsoft.Isam.Esent.Interop.SeekGrbit
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekEQ
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9e59072055710676f5f7647130f42ad5acf50527
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106356202"
---
# <a name="seekgrbit-enumeration"></a><span data-ttu-id="05161-103">Seekgrbit-Enumeration</span><span class="sxs-lookup"><span data-stu-id="05161-103">SeekGrbit enumeration</span></span>

<span data-ttu-id="05161-104">Optionen für JetSeek.</span><span class="sxs-lookup"><span data-stu-id="05161-104">Options for JetSeek.</span></span>

<span data-ttu-id="05161-105">Diese Enumeration enthält ein [FlagsAttribute](/dotnet/api/system.flagsattribute)-Attribut, das eine bitweise Kombination der Memberwerte zulässt.</span><span class="sxs-lookup"><span data-stu-id="05161-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="05161-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="05161-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="05161-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="05161-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="05161-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="05161-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration SeekGrbit
'Usage
Dim instance As SeekGrbit
```

``` csharp
[FlagsAttribute]
public enum SeekGrbit
```

## <a name="members"></a><span data-ttu-id="05161-109">Member</span><span class="sxs-lookup"><span data-stu-id="05161-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="05161-110">Membername</span><span class="sxs-lookup"><span data-stu-id="05161-110">Member name</span></span></th>
<th><span data-ttu-id="05161-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="05161-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="05161-112">Seekeq</span><span class="sxs-lookup"><span data-stu-id="05161-112">SeekEQ</span></span></td>
<td><span data-ttu-id="05161-113">Der Cursor wird am Index Eintrag positioniert, der am nächsten am Anfang des Indexes liegt, der exakt mit dem Suchschlüssel übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="05161-113">The cursor will be positioned at the index entry closest to the start of the index that exactly matches the search key.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="05161-114">Seeklt</span><span class="sxs-lookup"><span data-stu-id="05161-114">SeekLT</span></span></td>
<td><span data-ttu-id="05161-115">Der Cursor wird am Index Eintrag positioniert, der am nächsten am Ende des Indexes liegt, der kleiner als ein Index Eintrag ist, der genau mit den Suchkriterien übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="05161-115">The cursor will be positioned at the index entry closest to the end of the index that is less than an index entry that would exactly match the search criteria.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="05161-116">SeekLE</span><span class="sxs-lookup"><span data-stu-id="05161-116">SeekLE</span></span></td>
<td><span data-ttu-id="05161-117">Der Cursor wird am Index Eintrag positioniert, der am nächsten am Ende des Indexes liegt, der kleiner oder gleich einem Index Eintrag ist, der genau mit den Suchkriterien übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="05161-117">The cursor will be positioned at the index entry closest to the end of the index that is less than or equal to an index entry that would exactly match the search criteria.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="05161-118">SeekGE</span><span class="sxs-lookup"><span data-stu-id="05161-118">SeekGE</span></span></td>
<td><span data-ttu-id="05161-119">Der Cursor wird am Index Eintrag positioniert, der dem Anfang des Indexes am nächsten liegt, der größer als oder gleich einem Index Eintrag ist, der genau mit den Suchkriterien übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="05161-119">The cursor will be positioned at the index entry closest to the start of the index that is greater than or equal to an index entry that would exactly match the search criteria.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="05161-120">Seekgt</span><span class="sxs-lookup"><span data-stu-id="05161-120">SeekGT</span></span></td>
<td><span data-ttu-id="05161-121">Der Cursor wird am Index Eintrag positioniert, der dem Anfang des Indexes am nächsten liegt, der größer als ein Index Eintrag ist, der genau mit den Suchkriterien übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="05161-121">The cursor will be positioned at the index entry closest to the start of the index that is greater than an index entry that would exactly match the search criteria.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="05161-122">Setindexrange</span><span class="sxs-lookup"><span data-stu-id="05161-122">SetIndexRange</span></span></td>
<td><span data-ttu-id="05161-123">Ein Index Bereich wird automatisch für alle Schlüssel eingerichtet, die exakt mit dem Suchschlüssel übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="05161-123">An index range will automatically be setup for all keys that exactly match the search key.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="05161-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="05161-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="05161-125">Referenz</span><span class="sxs-lookup"><span data-stu-id="05161-125">Reference</span></span>

[<span data-ttu-id="05161-126">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="05161-126">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
