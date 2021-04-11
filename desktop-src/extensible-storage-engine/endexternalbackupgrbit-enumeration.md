---
description: 'Weitere Informationen finden Sie hier: endexternalbackupgrbit-Enumeration'
title: Endexternalbackupgrbit-Enumeration
TOCTitle: EndExternalBackupGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.EndExternalBackupGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.endexternalbackupgrbit(v=EXCHG.10)
ms:contentKeyID: 39516835
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EndExternalBackupGrbit
- Microsoft.Isam.Esent.Interop.EndExternalBackupGrbit.Abort
- Microsoft.Isam.Esent.Interop.EndExternalBackupGrbit.None
- Microsoft.Isam.Esent.Interop.EndExternalBackupGrbit.Normal
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EndExternalBackupGrbit
- Microsoft.Isam.Esent.Interop.EndExternalBackupGrbit.Abort
- Microsoft.Isam.Esent.Interop.EndExternalBackupGrbit.None
- Microsoft.Isam.Esent.Interop.EndExternalBackupGrbit.Normal
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0bb3fb2f3e959d41c042589f3a280e6466fe4970
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218455"
---
# <a name="endexternalbackupgrbit-enumeration"></a><span data-ttu-id="13ba9-103">Endexternalbackupgrbit-Enumeration</span><span class="sxs-lookup"><span data-stu-id="13ba9-103">EndExternalBackupGrbit enumeration</span></span>

<span data-ttu-id="13ba9-104">Optionen für [jetendexternalbackupinstance (JET_INSTANCE)](./api.jetendexternalbackupinstance-method.md).</span><span class="sxs-lookup"><span data-stu-id="13ba9-104">Options for [JetEndExternalBackupInstance(JET_INSTANCE)](./api.jetendexternalbackupinstance-method.md).</span></span>

<span data-ttu-id="13ba9-105">Diese Enumeration enthält ein [FlagsAttribute](/dotnet/api/system.flagsattribute)-Attribut, das eine bitweise Kombination der Memberwerte zulässt.</span><span class="sxs-lookup"><span data-stu-id="13ba9-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="13ba9-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="13ba9-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="13ba9-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="13ba9-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="13ba9-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="13ba9-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration EndExternalBackupGrbit
'Usage
Dim instance As EndExternalBackupGrbit
```

``` csharp
[FlagsAttribute]
public enum EndExternalBackupGrbit
```

## <a name="members"></a><span data-ttu-id="13ba9-109">Member</span><span class="sxs-lookup"><span data-stu-id="13ba9-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="13ba9-110">Membername</span><span class="sxs-lookup"><span data-stu-id="13ba9-110">Member name</span></span></th>
<th><span data-ttu-id="13ba9-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="13ba9-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="13ba9-112">Keine</span><span class="sxs-lookup"><span data-stu-id="13ba9-112">None</span></span></td>
<td><span data-ttu-id="13ba9-113">Standardoptionen.</span><span class="sxs-lookup"><span data-stu-id="13ba9-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="13ba9-114">Normal</span><span class="sxs-lookup"><span data-stu-id="13ba9-114">Normal</span></span></td>
<td><span data-ttu-id="13ba9-115">Die Client Anwendung hat die Sicherung vollständig abgeschlossen und wird normal beendet.</span><span class="sxs-lookup"><span data-stu-id="13ba9-115">The client application finished the backup completely, and is ending normally.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="13ba9-116">Abbrechen</span><span class="sxs-lookup"><span data-stu-id="13ba9-116">Abort</span></span></td>
<td><span data-ttu-id="13ba9-117">Die Sicherung wird von der Client Anwendung abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="13ba9-117">The client application is aborting the backup.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="13ba9-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="13ba9-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="13ba9-119">Referenz</span><span class="sxs-lookup"><span data-stu-id="13ba9-119">Reference</span></span>

[<span data-ttu-id="13ba9-120">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="13ba9-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
