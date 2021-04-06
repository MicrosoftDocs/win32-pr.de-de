---
description: 'Weitere Informationen finden Sie hier: escrowupdategrbit-Enumeration'
title: Escrowupdategrbit-Enumeration
TOCTitle: EscrowUpdateGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.EscrowUpdateGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.escrowupdategrbit(v=EXCHG.10)
ms:contentKeyID: 39514160
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EscrowUpdateGrbit
- Microsoft.Isam.Esent.Interop.EscrowUpdateGrbit.None
- Microsoft.Isam.Esent.Interop.EscrowUpdateGrbit.NoRollback
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EscrowUpdateGrbit
- Microsoft.Isam.Esent.Interop.EscrowUpdateGrbit.None
- Microsoft.Isam.Esent.Interop.EscrowUpdateGrbit.NoRollback
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d301ef801a5685057a9e33beb794f3b6cf13e646
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960783"
---
# <a name="escrowupdategrbit-enumeration"></a><span data-ttu-id="88cce-103">Escrowupdategrbit-Enumeration</span><span class="sxs-lookup"><span data-stu-id="88cce-103">EscrowUpdateGrbit enumeration</span></span>

<span data-ttu-id="88cce-104">Optionen für jetescrowupdate.</span><span class="sxs-lookup"><span data-stu-id="88cce-104">Options for JetEscrowUpdate.</span></span>

<span data-ttu-id="88cce-105">Diese Enumeration enthält ein [FlagsAttribute](/dotnet/api/system.flagsattribute)-Attribut, das eine bitweise Kombination der Memberwerte zulässt.</span><span class="sxs-lookup"><span data-stu-id="88cce-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="88cce-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="88cce-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="88cce-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="88cce-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="88cce-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="88cce-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration EscrowUpdateGrbit
'Usage
Dim instance As EscrowUpdateGrbit
```

``` csharp
[FlagsAttribute]
public enum EscrowUpdateGrbit
```

## <a name="members"></a><span data-ttu-id="88cce-109">Member</span><span class="sxs-lookup"><span data-stu-id="88cce-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="88cce-110">Membername</span><span class="sxs-lookup"><span data-stu-id="88cce-110">Member name</span></span></th>
<th><span data-ttu-id="88cce-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="88cce-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="88cce-112">Keine</span><span class="sxs-lookup"><span data-stu-id="88cce-112">None</span></span></td>
<td><span data-ttu-id="88cce-113">Standardoptionen.</span><span class="sxs-lookup"><span data-stu-id="88cce-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="88cce-114">Norollback</span><span class="sxs-lookup"><span data-stu-id="88cce-114">NoRollback</span></span></td>
<td><span data-ttu-id="88cce-115">Auch wenn für die Sitzung, die das hinterlegter-Update ausführt, ein Rollback der Transaktion ausgeführt wird, wird dieses Update nicht rückgängig gemacht.</span><span class="sxs-lookup"><span data-stu-id="88cce-115">Even if the session performing the escrow update has its transaction rollback this update will not be undone.</span></span> <span data-ttu-id="88cce-116">Da die Protokolldaten Sätze möglicherweise nicht auf den Datenträger geleert werden, gehen aktuelle mit diesem Flag ausgeführte Hinterlegungs Aktualisierungen möglicherweise verloren, wenn ein Absturz vorliegt.</span><span class="sxs-lookup"><span data-stu-id="88cce-116">As the log records may not be flushed to disk, recent escrow updates done with this flag may be lost if there is a crash.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="88cce-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="88cce-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="88cce-118">Referenz</span><span class="sxs-lookup"><span data-stu-id="88cce-118">Reference</span></span>

[<span data-ttu-id="88cce-119">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="88cce-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
