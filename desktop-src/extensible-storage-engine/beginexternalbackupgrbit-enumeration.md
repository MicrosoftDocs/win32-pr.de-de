---
description: 'Weitere Informationen finden Sie hier: beginexternalbackupgrbit-Enumeration'
title: Beginexternalbackupgrbit-Enumeration
TOCTitle: BeginExternalBackupGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.BeginExternalBackupGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.beginexternalbackupgrbit(v=EXCHG.10)
ms:contentKeyID: 39509773
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.BeginExternalBackupGrbit
- Microsoft.Isam.Esent.Interop.BeginExternalBackupGrbit.Incremental
- Microsoft.Isam.Esent.Interop.BeginExternalBackupGrbit.None
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.BeginExternalBackupGrbit.None
- Microsoft.Isam.Esent.Interop.BeginExternalBackupGrbit.Incremental
- Microsoft.Isam.Esent.Interop.BeginExternalBackupGrbit
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b68cbfc75d0a71eacedb4bbd462fcd8a93d43690
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351092"
---
# <a name="beginexternalbackupgrbit-enumeration"></a><span data-ttu-id="0fbab-103">Beginexternalbackupgrbit-Enumeration</span><span class="sxs-lookup"><span data-stu-id="0fbab-103">BeginExternalBackupGrbit enumeration</span></span>

<span data-ttu-id="0fbab-104">Optionen für [jetbeginexternalbackupinstance (JET_INSTANCE, beginexternalbackupgrbit)](./api.jetbeginexternalbackupinstance-method.md).</span><span class="sxs-lookup"><span data-stu-id="0fbab-104">Options for [JetBeginExternalBackupInstance(JET_INSTANCE, BeginExternalBackupGrbit)](./api.jetbeginexternalbackupinstance-method.md).</span></span>

<span data-ttu-id="0fbab-105">Diese Enumeration enthält ein [FlagsAttribute](/dotnet/api/system.flagsattribute)-Attribut, das eine bitweise Kombination der Memberwerte zulässt.</span><span class="sxs-lookup"><span data-stu-id="0fbab-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="0fbab-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="0fbab-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="0fbab-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="0fbab-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="0fbab-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="0fbab-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration BeginExternalBackupGrbit
'Usage
Dim instance As BeginExternalBackupGrbit
```

``` csharp
[FlagsAttribute]
public enum BeginExternalBackupGrbit
```

## <a name="members"></a><span data-ttu-id="0fbab-109">Member</span><span class="sxs-lookup"><span data-stu-id="0fbab-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="0fbab-110">Membername</span><span class="sxs-lookup"><span data-stu-id="0fbab-110">Member name</span></span></th>
<th><span data-ttu-id="0fbab-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0fbab-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="0fbab-112">Keine</span><span class="sxs-lookup"><span data-stu-id="0fbab-112">None</span></span></td>
<td><span data-ttu-id="0fbab-113">Standardoptionen.</span><span class="sxs-lookup"><span data-stu-id="0fbab-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="0fbab-114">Inkrementell</span><span class="sxs-lookup"><span data-stu-id="0fbab-114">Incremental</span></span></td>
<td><span data-ttu-id="0fbab-115">Erstellt im Gegensatz zu einer vollständigen Sicherung eine inkrementelle Sicherung.</span><span class="sxs-lookup"><span data-stu-id="0fbab-115">Creates an incremental backup as opposed to a full backup.</span></span> <span data-ttu-id="0fbab-116">Dies bedeutet, dass nur die Protokolldateien seit der letzten vollständigen oder inkrementellen Sicherung gesichert werden.</span><span class="sxs-lookup"><span data-stu-id="0fbab-116">This means that only the log files since the last full or incremental backup will be backed up.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="0fbab-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0fbab-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="0fbab-118">Referenz</span><span class="sxs-lookup"><span data-stu-id="0fbab-118">Reference</span></span>

[<span data-ttu-id="0fbab-119">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="0fbab-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
