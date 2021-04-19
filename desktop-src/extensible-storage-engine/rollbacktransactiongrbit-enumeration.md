---
description: 'Weitere Informationen finden Sie hier: RollbackTransaction grbit-Enumeration'
title: RollbackTransaction grbit-Enumeration
TOCTitle: RollbackTransactionGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.RollbackTransactionGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.rollbacktransactiongrbit(v=EXCHG.10)
ms:contentKeyID: 39513584
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.RollbackTransactionGrbit
- Microsoft.Isam.Esent.Interop.RollbackTransactionGrbit.None
- Microsoft.Isam.Esent.Interop.RollbackTransactionGrbit.RollbackAll
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.RollbackTransactionGrbit.RollbackAll
- Microsoft.Isam.Esent.Interop.RollbackTransactionGrbit.None
- Microsoft.Isam.Esent.Interop.RollbackTransactionGrbit
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bf2635d94070fc47bebbd6cdd0e53deddeb4c5eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106358508"
---
# <a name="rollbacktransactiongrbit-enumeration"></a><span data-ttu-id="11244-103">RollbackTransaction grbit-Enumeration</span><span class="sxs-lookup"><span data-stu-id="11244-103">RollbackTransactionGrbit enumeration</span></span>

<span data-ttu-id="11244-104">Optionen für jetrollbacktransaction.</span><span class="sxs-lookup"><span data-stu-id="11244-104">Options for JetRollbackTransaction.</span></span>

<span data-ttu-id="11244-105">Diese Enumeration enthält ein [FlagsAttribute](/dotnet/api/system.flagsattribute)-Attribut, das eine bitweise Kombination der Memberwerte zulässt.</span><span class="sxs-lookup"><span data-stu-id="11244-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="11244-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="11244-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="11244-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="11244-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="11244-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="11244-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration RollbackTransactionGrbit
'Usage
Dim instance As RollbackTransactionGrbit
```

``` csharp
[FlagsAttribute]
public enum RollbackTransactionGrbit
```

## <a name="members"></a><span data-ttu-id="11244-109">Member</span><span class="sxs-lookup"><span data-stu-id="11244-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="11244-110">Membername</span><span class="sxs-lookup"><span data-stu-id="11244-110">Member name</span></span></th>
<th><span data-ttu-id="11244-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="11244-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="11244-112">Keine</span><span class="sxs-lookup"><span data-stu-id="11244-112">None</span></span></td>
<td><span data-ttu-id="11244-113">Standardoptionen.</span><span class="sxs-lookup"><span data-stu-id="11244-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="11244-114">Rollbackall</span><span class="sxs-lookup"><span data-stu-id="11244-114">RollbackAll</span></span></td>
<td><span data-ttu-id="11244-115">Mit dieser Option wird angefordert, dass alle Änderungen, die an dem Status der Datenbank vorgenommen wurden, bei allen Speicher Punkten rückgängig gemacht werden.</span><span class="sxs-lookup"><span data-stu-id="11244-115">This option requests that all changes made to the state of the database during all save points be undone.</span></span> <span data-ttu-id="11244-116">Dies führt dazu, dass die Sitzung die Transaktion beendet.</span><span class="sxs-lookup"><span data-stu-id="11244-116">As a result, the session will exit the transaction.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="11244-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="11244-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="11244-118">Referenz</span><span class="sxs-lookup"><span data-stu-id="11244-118">Reference</span></span>

[<span data-ttu-id="11244-119">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="11244-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
