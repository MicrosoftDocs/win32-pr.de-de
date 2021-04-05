---
description: 'Weitere Informationen finden Sie hier: Aufzählung von "kreatedatabasegrbit"'
title: Kreatedatabasegrbit-Enumeration
TOCTitle: CreateDatabaseGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.CreateDatabaseGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.createdatabasegrbit(v=EXCHG.10)
ms:contentKeyID: 39515634
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.CreateDatabaseGrbit
- Microsoft.Isam.Esent.Interop.CreateDatabaseGrbit.None
- Microsoft.Isam.Esent.Interop.CreateDatabaseGrbit.OverwriteExisting
- Microsoft.Isam.Esent.Interop.CreateDatabaseGrbit.RecoveryOff
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.CreateDatabaseGrbit.OverwriteExisting
- Microsoft.Isam.Esent.Interop.CreateDatabaseGrbit.RecoveryOff
- Microsoft.Isam.Esent.Interop.CreateDatabaseGrbit.None
- Microsoft.Isam.Esent.Interop.CreateDatabaseGrbit
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8e23b7b875863b747fc5d2ba021c90d5f7f71048
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041858"
---
# <a name="createdatabasegrbit-enumeration"></a><span data-ttu-id="85331-103">Kreatedatabasegrbit-Enumeration</span><span class="sxs-lookup"><span data-stu-id="85331-103">CreateDatabaseGrbit enumeration</span></span>

<span data-ttu-id="85331-104">Optionen für [jetkreatedatabase (JET_SESID, String, String, JET_DBID, kreatedatabasegrbit)](./api.jetcreatedatabase-method.md).</span><span class="sxs-lookup"><span data-stu-id="85331-104">Options for [JetCreateDatabase(JET_SESID, String, String, JET_DBID, CreateDatabaseGrbit)](./api.jetcreatedatabase-method.md).</span></span>

<span data-ttu-id="85331-105">Diese Enumeration enthält ein [FlagsAttribute](/dotnet/api/system.flagsattribute)-Attribut, das eine bitweise Kombination der Memberwerte zulässt.</span><span class="sxs-lookup"><span data-stu-id="85331-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="85331-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="85331-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="85331-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="85331-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="85331-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="85331-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration CreateDatabaseGrbit
'Usage
Dim instance As CreateDatabaseGrbit
```

``` csharp
[FlagsAttribute]
public enum CreateDatabaseGrbit
```

## <a name="members"></a><span data-ttu-id="85331-109">Member</span><span class="sxs-lookup"><span data-stu-id="85331-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="85331-110">Membername</span><span class="sxs-lookup"><span data-stu-id="85331-110">Member name</span></span></th>
<th><span data-ttu-id="85331-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="85331-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="85331-112">Keine</span><span class="sxs-lookup"><span data-stu-id="85331-112">None</span></span></td>
<td><span data-ttu-id="85331-113">Standardoptionen.</span><span class="sxs-lookup"><span data-stu-id="85331-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="85331-114">Überschreiben vorhanden</span><span class="sxs-lookup"><span data-stu-id="85331-114">OverwriteExisting</span></span></td>
<td><span data-ttu-id="85331-115">Wenn jetkreatedatabase aufgerufen wird und die Datenbank bereits vorhanden ist, schlägt der API-Aufruf standardmäßig fehl, und die ursprüngliche Datenbank wird nicht überschrieben.</span><span class="sxs-lookup"><span data-stu-id="85331-115">By default, if JetCreateDatabase is called and the database already exists, the Api call will fail and the original database will not be overwritten.</span></span> <span data-ttu-id="85331-116">Über Schreibbarkeit ändert dieses Verhalten, und die alte Datenbank wird mit einer neuen überschrieben.</span><span class="sxs-lookup"><span data-stu-id="85331-116">OverwriteExisting changes this behavior, and the old database will be overwritten with a new one.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="85331-117">Wiederherstellung</span><span class="sxs-lookup"><span data-stu-id="85331-117">RecoveryOff</span></span></td>
<td><span data-ttu-id="85331-118">Schaltet die Protokollierung aus.</span><span class="sxs-lookup"><span data-stu-id="85331-118">Turns off logging.</span></span> <span data-ttu-id="85331-119">Das Festlegen dieses Bits verliert die Möglichkeit, Protokolldateien wiederzugeben und die Datenbank nach einem Absturz in einem konsistenten verwendbaren Zustand wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="85331-119">Setting this bit loses the ability to replay log files and recover the database to a consistent usable state after a crash.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="85331-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="85331-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="85331-121">Referenz</span><span class="sxs-lookup"><span data-stu-id="85331-121">Reference</span></span>

[<span data-ttu-id="85331-122">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="85331-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
