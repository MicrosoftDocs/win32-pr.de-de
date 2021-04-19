---
description: 'Weitere Informationen finden Sie unter: prereadindexrangesgrbit-Enumeration'
title: Prereadindexrangesgrbit-Enumeration (Microsoft. ISAM. ESENT. Interop. Windows8)
TOCTitle: PrereadIndexRangesGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.Windows8.PrereadIndexRangesGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.prereadindexrangesgrbit(v=EXCHG.10)
ms:contentKeyID: 55104328
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.PrereadIndexRangesGrbit
- Microsoft.Isam.Esent.Interop.Windows8.PrereadIndexRangesGrbit.Backwards
- Microsoft.Isam.Esent.Interop.Windows8.PrereadIndexRangesGrbit.FirstPageOnly
- Microsoft.Isam.Esent.Interop.Windows8.PrereadIndexRangesGrbit.Forward
- Microsoft.Isam.Esent.Interop.Windows8.PrereadIndexRangesGrbit.NormalizedKey
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.PrereadIndexRangesGrbit.FirstPageOnly
- Microsoft.Isam.Esent.Interop.Windows8.PrereadIndexRangesGrbit
- Microsoft.Isam.Esent.Interop.Windows8.PrereadIndexRangesGrbit.Forward
- Microsoft.Isam.Esent.Interop.Windows8.PrereadIndexRangesGrbit.Backwards
- Microsoft.Isam.Esent.Interop.Windows8.PrereadIndexRangesGrbit.NormalizedKey
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d4bc1b9877d4548a68aa71ea4def536af09d9693
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353516"
---
# <a name="prereadindexrangesgrbit-enumeration"></a><span data-ttu-id="d1825-103">Prereadindexrangesgrbit-Enumeration</span><span class="sxs-lookup"><span data-stu-id="d1825-103">PrereadIndexRangesGrbit enumeration</span></span>

<span data-ttu-id="d1825-104">Optionen für [jetprereadindexranges (JET_SESID, JET_TABLEID, \[ \] , Int32, Int32, Int32, \[ \] , prereadindexrangesgrbit)](./windows8api.jetprereadindexranges-method.md).</span><span class="sxs-lookup"><span data-stu-id="d1825-104">Options for [JetPrereadIndexRanges(JET_SESID, JET_TABLEID, \[\], Int32, Int32, Int32, \[\], PrereadIndexRangesGrbit)](./windows8api.jetprereadindexranges-method.md).</span></span>

<span data-ttu-id="d1825-105">Diese Enumeration enthält ein [FlagsAttribute](/dotnet/api/system.flagsattribute)-Attribut, das eine bitweise Kombination der Memberwerte zulässt.</span><span class="sxs-lookup"><span data-stu-id="d1825-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="d1825-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="d1825-106">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="d1825-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="d1825-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="d1825-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="d1825-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration PrereadIndexRangesGrbit
'Usage
Dim instance As PrereadIndexRangesGrbit
```

``` csharp
[FlagsAttribute]
public enum PrereadIndexRangesGrbit
```

## <a name="members"></a><span data-ttu-id="d1825-109">Member</span><span class="sxs-lookup"><span data-stu-id="d1825-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="d1825-110">Membername</span><span class="sxs-lookup"><span data-stu-id="d1825-110">Member name</span></span></th>
<th><span data-ttu-id="d1825-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d1825-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="d1825-112">Weiter</span><span class="sxs-lookup"><span data-stu-id="d1825-112">Forward</span></span></td>
<td><span data-ttu-id="d1825-113">Preread Forward.</span><span class="sxs-lookup"><span data-stu-id="d1825-113">Preread forward.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="d1825-114">Rückwärts</span><span class="sxs-lookup"><span data-stu-id="d1825-114">Backwards</span></span></td>
<td><span data-ttu-id="d1825-115">Preread rückwärts.</span><span class="sxs-lookup"><span data-stu-id="d1825-115">Preread backwards.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="d1825-116">Firstpageonly</span><span class="sxs-lookup"><span data-stu-id="d1825-116">FirstPageOnly</span></span></td>
<td><span data-ttu-id="d1825-117">Nur die erste Seite einer langen Spalte wird vorab registriert.</span><span class="sxs-lookup"><span data-stu-id="d1825-117">Preread only first page of any long column.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="d1825-118">Normalizedkey</span><span class="sxs-lookup"><span data-stu-id="d1825-118">NormalizedKey</span></span></td>
<td><span data-ttu-id="d1825-119">Normalisierter Schlüssel/Lesezeichen anstelle von Spaltenwert angegeben.</span><span class="sxs-lookup"><span data-stu-id="d1825-119">Normalized key/bookmark provided instead of column value.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="d1825-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d1825-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d1825-121">Referenz</span><span class="sxs-lookup"><span data-stu-id="d1825-121">Reference</span></span>

[<span data-ttu-id="d1825-122">Microsoft. ISAM. ESENT. Interop. Windows8-Namespace</span><span class="sxs-lookup"><span data-stu-id="d1825-122">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
