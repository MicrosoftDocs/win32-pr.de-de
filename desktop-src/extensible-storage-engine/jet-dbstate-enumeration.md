---
description: 'Weitere Informationen finden Sie hier: JET_dbstate-Enumeration'
title: JET_dbstate-Enumeration
TOCTitle: JET_dbstate enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_dbstate
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_dbstate(v=EXCHG.10)
ms:contentKeyID: 39511841
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_dbstate
- Microsoft.Isam.Esent.Interop.JET_dbstate.BeingConverted
- Microsoft.Isam.Esent.Interop.JET_dbstate.CleanShutdown
- Microsoft.Isam.Esent.Interop.JET_dbstate.DirtyShutdown
- Microsoft.Isam.Esent.Interop.JET_dbstate.ForceDetach
- Microsoft.Isam.Esent.Interop.JET_dbstate.JustCreated
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_dbstate.JustCreated
- Microsoft.Isam.Esent.Interop.JET_dbstate.BeingConverted
- Microsoft.Isam.Esent.Interop.JET_dbstate.CleanShutdown
- Microsoft.Isam.Esent.Interop.JET_dbstate.ForceDetach
- Microsoft.Isam.Esent.Interop.JET_dbstate.DirtyShutdown
- Microsoft.Isam.Esent.Interop.JET_dbstate
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a83c8a4313e5e6f21ee885ee7936c90503bfbd3c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749881"
---
# <a name="jet_dbstate-enumeration"></a><span data-ttu-id="5fae2-103">JET_dbstate-Enumeration</span><span class="sxs-lookup"><span data-stu-id="5fae2-103">JET_dbstate enumeration</span></span>

<span data-ttu-id="5fae2-104">Daten Bank Status (wird in [JET_DBINFOMISC](./jet-dbinfomisc-class.md)verwendet).</span><span class="sxs-lookup"><span data-stu-id="5fae2-104">Database states (used in [JET_DBINFOMISC](./jet-dbinfomisc-class.md)).</span></span>

<span data-ttu-id="5fae2-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="5fae2-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="5fae2-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="5fae2-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="5fae2-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="5fae2-107">Syntax</span></span>

``` vb
'Declaration
Public Enumeration JET_dbstate
'Usage
Dim instance As JET_dbstate
```

``` csharp
public enum JET_dbstate
```

## <a name="members"></a><span data-ttu-id="5fae2-108">Member</span><span class="sxs-lookup"><span data-stu-id="5fae2-108">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="5fae2-109">Membername</span><span class="sxs-lookup"><span data-stu-id="5fae2-109">Member name</span></span></th>
<th><span data-ttu-id="5fae2-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5fae2-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="5fae2-111">Justcreated</span><span class="sxs-lookup"><span data-stu-id="5fae2-111">JustCreated</span></span></td>
<td><span data-ttu-id="5fae2-112">Die Datenbank wurde soeben erstellt.</span><span class="sxs-lookup"><span data-stu-id="5fae2-112">The database was just created.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="5fae2-113">Dirtyshutdown</span><span class="sxs-lookup"><span data-stu-id="5fae2-113">DirtyShutdown</span></span></td>
<td><span data-ttu-id="5fae2-114">Fehlerhafte Herunterfahren (inkonsistente) Datenbank.</span><span class="sxs-lookup"><span data-stu-id="5fae2-114">Dirty shutdown (inconsistent) database.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="5fae2-115">Cleanshutdown</span><span class="sxs-lookup"><span data-stu-id="5fae2-115">CleanShutdown</span></span></td>
<td><span data-ttu-id="5fae2-116">Clean Shutdown (konsistente) Datenbank.</span><span class="sxs-lookup"><span data-stu-id="5fae2-116">Clean shutdown (consistent) database.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="5fae2-117">"Beingkonvertiert"</span><span class="sxs-lookup"><span data-stu-id="5fae2-117">BeingConverted</span></span></td>
<td><span data-ttu-id="5fae2-118">Die Datenbank wird konvertiert.</span><span class="sxs-lookup"><span data-stu-id="5fae2-118">Database is being converted.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="5fae2-119">Forcedetach</span><span class="sxs-lookup"><span data-stu-id="5fae2-119">ForceDetach</span></span></td>
<td><span data-ttu-id="5fae2-120">Die Datenbank wurde Zwangs seitig getrennt.</span><span class="sxs-lookup"><span data-stu-id="5fae2-120">Database was force-detached.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="5fae2-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5fae2-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="5fae2-122">Referenz</span><span class="sxs-lookup"><span data-stu-id="5fae2-122">Reference</span></span>

[<span data-ttu-id="5fae2-123">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="5fae2-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
