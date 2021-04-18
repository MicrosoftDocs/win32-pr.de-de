---
description: 'Weitere Informationen finden Sie hier: backupgrbit-Enumeration'
title: Backupgrbit-Enumeration
TOCTitle: BackupGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.BackupGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.backupgrbit(v=EXCHG.10)
ms:contentKeyID: 39512196
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.BackupGrbit
- Microsoft.Isam.Esent.Interop.BackupGrbit.Atomic
- Microsoft.Isam.Esent.Interop.BackupGrbit.Incremental
- Microsoft.Isam.Esent.Interop.BackupGrbit.None
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.BackupGrbit.Incremental
- Microsoft.Isam.Esent.Interop.BackupGrbit
- Microsoft.Isam.Esent.Interop.BackupGrbit.Atomic
- Microsoft.Isam.Esent.Interop.BackupGrbit.None
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bda9754efcae8ebe353b8272ba57c5640ecdf946
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351551"
---
# <a name="backupgrbit-enumeration"></a><span data-ttu-id="0c345-103">Backupgrbit-Enumeration</span><span class="sxs-lookup"><span data-stu-id="0c345-103">BackupGrbit enumeration</span></span>

<span data-ttu-id="0c345-104">Optionen für [jetbackupinstance (JET_INSTANCE, String, backupgrbit JET_PFNSTATUS)](./api.jetbackupinstance-method.md).</span><span class="sxs-lookup"><span data-stu-id="0c345-104">Options for [JetBackupInstance(JET_INSTANCE, String, BackupGrbit, JET_PFNSTATUS)](./api.jetbackupinstance-method.md).</span></span>

<span data-ttu-id="0c345-105">Diese Enumeration enthält ein [FlagsAttribute](/dotnet/api/system.flagsattribute)-Attribut, das eine bitweise Kombination der Memberwerte zulässt.</span><span class="sxs-lookup"><span data-stu-id="0c345-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="0c345-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="0c345-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="0c345-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="0c345-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="0c345-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="0c345-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration BackupGrbit
'Usage
Dim instance As BackupGrbit
```

``` csharp
[FlagsAttribute]
public enum BackupGrbit
```

## <a name="members"></a><span data-ttu-id="0c345-109">Member</span><span class="sxs-lookup"><span data-stu-id="0c345-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="0c345-110">Membername</span><span class="sxs-lookup"><span data-stu-id="0c345-110">Member name</span></span></th>
<th><span data-ttu-id="0c345-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0c345-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="0c345-112">Keine</span><span class="sxs-lookup"><span data-stu-id="0c345-112">None</span></span></td>
<td><span data-ttu-id="0c345-113">Standardoptionen.</span><span class="sxs-lookup"><span data-stu-id="0c345-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="0c345-114">Inkrementell</span><span class="sxs-lookup"><span data-stu-id="0c345-114">Incremental</span></span></td>
<td><span data-ttu-id="0c345-115">Erstellt im Gegensatz zu einer vollständigen Sicherung eine inkrementelle Sicherung.</span><span class="sxs-lookup"><span data-stu-id="0c345-115">Creates an incremental backup as opposed to a full backup.</span></span> <span data-ttu-id="0c345-116">Dies bedeutet, dass nur die Protokolldateien gesichert werden, die seit der letzten vollständigen oder inkrementellen Sicherung erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="0c345-116">This means that only the log files created since the last full or incremental backup will be backed up.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="0c345-117">Atomarisch</span><span class="sxs-lookup"><span data-stu-id="0c345-117">Atomic</span></span></td>
<td><span data-ttu-id="0c345-118">Erstellt eine vollständige Sicherung der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="0c345-118">Creates a full backup of the database.</span></span> <span data-ttu-id="0c345-119">Dies ermöglicht die Beibehaltung einer vorhandenen Sicherung im gleichen Verzeichnis, wenn die neue Sicherung nicht ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="0c345-119">This allows the preservation of an existing backup in the same directory if the new backup fails.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="0c345-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0c345-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="0c345-121">Referenz</span><span class="sxs-lookup"><span data-stu-id="0c345-121">Reference</span></span>

[<span data-ttu-id="0c345-122">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="0c345-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
