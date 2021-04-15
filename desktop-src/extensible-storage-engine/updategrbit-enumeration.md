---
description: 'Weitere Informationen finden Sie hier: updategrbit-Enumeration'
title: Updategrbit-Enumeration (Microsoft. ISAM. ESENT. Interop. Server2003)
TOCTitle: UpdateGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.Server2003.UpdateGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.server2003.updategrbit(v=EXCHG.10)
ms:contentKeyID: 39514938
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Server2003.UpdateGrbit
- Microsoft.Isam.Esent.Interop.Server2003.UpdateGrbit.CheckESE97Compatibility
- Microsoft.Isam.Esent.Interop.Server2003.UpdateGrbit.None
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Server2003.UpdateGrbit
- Microsoft.Isam.Esent.Interop.Server2003.UpdateGrbit.None
- Microsoft.Isam.Esent.Interop.Server2003.UpdateGrbit.CheckESE97Compatibility
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e27809ef16fb00fd538e4c37826d10fefa3b396c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526792"
---
# <a name="updategrbit-enumeration"></a><span data-ttu-id="a9271-103">Updategrbit-Enumeration</span><span class="sxs-lookup"><span data-stu-id="a9271-103">UpdateGrbit enumeration</span></span>

<span data-ttu-id="a9271-104">Optionen für [JetUpdate2 (JET_SESID, JET_TABLEID, \[ \] , Int32, Int32, updategrbit)](./server2003api.jetupdate2-method.md).</span><span class="sxs-lookup"><span data-stu-id="a9271-104">Options for [JetUpdate2(JET_SESID, JET_TABLEID, \[\], Int32, Int32, UpdateGrbit)](./server2003api.jetupdate2-method.md).</span></span>

<span data-ttu-id="a9271-105">Diese Enumeration enthält ein [FlagsAttribute](/dotnet/api/system.flagsattribute)-Attribut, das eine bitweise Kombination der Memberwerte zulässt.</span><span class="sxs-lookup"><span data-stu-id="a9271-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="a9271-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop. Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="a9271-106">**Namespace:**  [Microsoft.Isam.Esent.Interop.Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)</span></span>  
<span data-ttu-id="a9271-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="a9271-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="a9271-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="a9271-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration UpdateGrbit
'Usage
Dim instance As UpdateGrbit
```

``` csharp
[FlagsAttribute]
public enum UpdateGrbit
```

## <a name="members"></a><span data-ttu-id="a9271-109">Member</span><span class="sxs-lookup"><span data-stu-id="a9271-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="a9271-110">Membername</span><span class="sxs-lookup"><span data-stu-id="a9271-110">Member name</span></span></th>
<th><span data-ttu-id="a9271-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a9271-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="a9271-112">Keine</span><span class="sxs-lookup"><span data-stu-id="a9271-112">None</span></span></td>
<td><span data-ttu-id="a9271-113">Standardoptionen.</span><span class="sxs-lookup"><span data-stu-id="a9271-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="a9271-114">CheckESE97Compatibility</span><span class="sxs-lookup"><span data-stu-id="a9271-114">CheckESE97Compatibility</span></span></td>
<td><span data-ttu-id="a9271-115"><strong>Veraltet.</strong></span><span class="sxs-lookup"><span data-stu-id="a9271-115"><strong>Obsolete.</strong></span></span> <span data-ttu-id="a9271-116">Dieses Flag bewirkt, dass das Update einen Fehler zurückgibt, wenn das Update in der Windows 2000-Version von ESE nicht möglich wäre, was eine geringere maximale Anzahl von mehrwertigen Spalten Instanzen in jedem Datensatz erzwungen hat als spätere Versionen von ESE.</span><span class="sxs-lookup"><span data-stu-id="a9271-116">This flag causes the update to return an error if the update would not have been possible in the Windows 2000 version of ESE, which enforced a smaller maximum number of multi-valued column instances in each record than later versions of ESE.</span></span> <span data-ttu-id="a9271-117">Dies ist nur für Anwendungen wichtig, die Daten zwischen Anwendungen replizieren möchten, die unter Windows 2000 gehostet werden, und Anwendungen, die unter Windows 2003 oder höheren Versionen von ESE gehostet werden.</span><span class="sxs-lookup"><span data-stu-id="a9271-117">This is important only for applications that wish to replicate data between applications hosted on Windows 2000 and applications hosted on Windows 2003, or later versions of ESE.</span></span> <span data-ttu-id="a9271-118">Dies sollte für die meisten Anwendungen nicht erforderlich sein.</span><span class="sxs-lookup"><span data-stu-id="a9271-118">It should not be necessary for most applications.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="a9271-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a9271-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a9271-120">Referenz</span><span class="sxs-lookup"><span data-stu-id="a9271-120">Reference</span></span>

[<span data-ttu-id="a9271-121">Microsoft. ISAM. ESENT. Interop. Server2003-Namespace</span><span class="sxs-lookup"><span data-stu-id="a9271-121">Microsoft.Isam.Esent.Interop.Server2003 namespace</span></span>](./microsoft.isam.esent.interop.server2003-namespace.md)
