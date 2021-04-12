---
description: 'Weitere Informationen finden Sie hier: detachdatabasegrbit-Enumeration'
title: Detachdatabasegrbit-Enumeration
TOCTitle: DetachDatabaseGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.DetachDatabaseGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.detachdatabasegrbit(v=EXCHG.10)
ms:contentKeyID: 55100985
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.DetachDatabaseGrbit
- Microsoft.Isam.Esent.Interop.DetachDatabaseGrbit.ForceClose
- Microsoft.Isam.Esent.Interop.DetachDatabaseGrbit.ForceCloseAndDetach
- Microsoft.Isam.Esent.Interop.DetachDatabaseGrbit.ForceDetach
- Microsoft.Isam.Esent.Interop.DetachDatabaseGrbit.None
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.DetachDatabaseGrbit.None
- Microsoft.Isam.Esent.Interop.DetachDatabaseGrbit.ForceClose
- Microsoft.Isam.Esent.Interop.DetachDatabaseGrbit.ForceCloseAndDetach
- Microsoft.Isam.Esent.Interop.DetachDatabaseGrbit
- Microsoft.Isam.Esent.Interop.DetachDatabaseGrbit.ForceDetach
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8e67962420ee0179571da8262f17ea5279f59016
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218270"
---
# <a name="detachdatabasegrbit-enumeration"></a><span data-ttu-id="3524a-103">Detachdatabasegrbit-Enumeration</span><span class="sxs-lookup"><span data-stu-id="3524a-103">DetachDatabaseGrbit enumeration</span></span>

<span data-ttu-id="3524a-104">Optionen für [JetDetachDatabase2 (JET_SESID, String, detachdatabasegrbit)](./api.jetdetachdatabase2-method.md).</span><span class="sxs-lookup"><span data-stu-id="3524a-104">Options for [JetDetachDatabase2(JET_SESID, String, DetachDatabaseGrbit)](./api.jetdetachdatabase2-method.md).</span></span>

<span data-ttu-id="3524a-105">Diese Enumeration enthält ein [FlagsAttribute](/dotnet/api/system.flagsattribute)-Attribut, das eine bitweise Kombination der Memberwerte zulässt.</span><span class="sxs-lookup"><span data-stu-id="3524a-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="3524a-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="3524a-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="3524a-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="3524a-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="3524a-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="3524a-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration DetachDatabaseGrbit
'Usage
Dim instance As DetachDatabaseGrbit
```

``` csharp
[FlagsAttribute]
public enum DetachDatabaseGrbit
```

## <a name="members"></a><span data-ttu-id="3524a-109">Member</span><span class="sxs-lookup"><span data-stu-id="3524a-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="3524a-110">Membername</span><span class="sxs-lookup"><span data-stu-id="3524a-110">Member name</span></span></th>
<th><span data-ttu-id="3524a-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3524a-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="3524a-112">Keine</span><span class="sxs-lookup"><span data-stu-id="3524a-112">None</span></span></td>
<td><span data-ttu-id="3524a-113">Standardoptionen.</span><span class="sxs-lookup"><span data-stu-id="3524a-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="3524a-114">Forcedetach</span><span class="sxs-lookup"><span data-stu-id="3524a-114">ForceDetach</span></span></td>
<td><span data-ttu-id="3524a-115"><strong>Veraltet.</strong></span><span class="sxs-lookup"><span data-stu-id="3524a-115"><strong>Obsolete.</strong></span></span> <span data-ttu-id="3524a-116">Wenn forcedetach verwendet wird, wird <a href="dn350463(v=exchg.10).md">esentforcedetachnotallowedexception</a> zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="3524a-116">If ForceDetach is used, <a href="dn350463(v=exchg.10).md">EsentForceDetachNotAllowedException</a> will be returned.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="3524a-117">Die erzwungene Schließung</span><span class="sxs-lookup"><span data-stu-id="3524a-117">ForceClose</span></span></td>
<td><span data-ttu-id="3524a-118"><strong>Veraltet.</strong></span><span class="sxs-lookup"><span data-stu-id="3524a-118"><strong>Obsolete.</strong></span></span> <span data-ttu-id="3524a-119">Forceclose wird nicht mehr verwendet.</span><span class="sxs-lookup"><span data-stu-id="3524a-119">ForceClose is no longer used.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="3524a-120">Forcecloseanddetach</span><span class="sxs-lookup"><span data-stu-id="3524a-120">ForceCloseAndDetach</span></span></td>
<td><span data-ttu-id="3524a-121"><strong>Veraltet.</strong></span><span class="sxs-lookup"><span data-stu-id="3524a-121"><strong>Obsolete.</strong></span></span> <span data-ttu-id="3524a-122">Wenn forcecloseanddetach verwendet wird, wird <a href="dn350463(v=exchg.10).md">esentforcedetachnotallowedexception</a> zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="3524a-122">If ForceCloseAndDetach is used, <a href="dn350463(v=exchg.10).md">EsentForceDetachNotAllowedException</a> will be returned.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="3524a-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3524a-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="3524a-124">Referenz</span><span class="sxs-lookup"><span data-stu-id="3524a-124">Reference</span></span>

[<span data-ttu-id="3524a-125">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="3524a-125">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
