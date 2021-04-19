---
description: Weitere Informationen finden Sie in der stopservicegrbit-Enumeration.
title: Stopservicegrbit-Enumeration (Microsoft. ISAM. ESENT. Interop. Windows8)
TOCTitle: StopServiceGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.stopservicegrbit(v=EXCHG.10)
ms:contentKeyID: 55104330
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.All
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.BackgroundUserTasks
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.QuiesceCaches
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.Resume
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.BackgroundUserTasks
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.All
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.QuiesceCaches
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.Resume
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 54e54576dfb1023ec4e3bc55ddd198a77f0ddf25
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348213"
---
# <a name="stopservicegrbit-enumeration"></a><span data-ttu-id="9cfd3-103">Stopservicegrbit-Enumeration</span><span class="sxs-lookup"><span data-stu-id="9cfd3-103">StopServiceGrbit enumeration</span></span>

<span data-ttu-id="9cfd3-104">Optionen für [JetStopServiceInstance2 (JET_INSTANCE, stopservicegrbit)](./windows8api.jetstopserviceinstance2-method.md).</span><span class="sxs-lookup"><span data-stu-id="9cfd3-104">Options for [JetStopServiceInstance2(JET_INSTANCE, StopServiceGrbit)](./windows8api.jetstopserviceinstance2-method.md).</span></span>

<span data-ttu-id="9cfd3-105">Diese Enumeration enthält ein [FlagsAttribute](/dotnet/api/system.flagsattribute)-Attribut, das eine bitweise Kombination der Memberwerte zulässt.</span><span class="sxs-lookup"><span data-stu-id="9cfd3-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="9cfd3-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="9cfd3-106">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="9cfd3-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="9cfd3-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="9cfd3-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="9cfd3-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration StopServiceGrbit
'Usage
Dim instance As StopServiceGrbit
```

``` csharp
[FlagsAttribute]
public enum StopServiceGrbit
```

## <a name="members"></a><span data-ttu-id="9cfd3-109">Member</span><span class="sxs-lookup"><span data-stu-id="9cfd3-109">Members</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="9cfd3-110">Membername</span><span class="sxs-lookup"><span data-stu-id="9cfd3-110">Member name</span></span></th>
<th><span data-ttu-id="9cfd3-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9cfd3-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="9cfd3-112">Alle</span><span class="sxs-lookup"><span data-stu-id="9cfd3-112">All</span></span></td>
<td><span data-ttu-id="9cfd3-113">Beendet alle ESE-Dienste für die angegebene-Instanz.</span><span class="sxs-lookup"><span data-stu-id="9cfd3-113">Stops all ESE services for the specified instance.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="9cfd3-114">Backgroundusertasks</span><span class="sxs-lookup"><span data-stu-id="9cfd3-114">BackgroundUserTasks</span></span></td>
<td><span data-ttu-id="9cfd3-115">Beendet neu startable-Client spezifische Hintergrund Wartungs Tasks (B +-Struktur Defragmentierung).</span><span class="sxs-lookup"><span data-stu-id="9cfd3-115">Stops restartable client specificed background maintenance tasks (B+ Tree Defrag).</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="9cfd3-116">Stilllegung</span><span class="sxs-lookup"><span data-stu-id="9cfd3-116">QuiesceCaches</span></span></td>
<td><span data-ttu-id="9cfd3-117">Versetzt alle Dirty Caches auf den Datenträger.</span><span class="sxs-lookup"><span data-stu-id="9cfd3-117">Quiesces all dirty caches to disk.</span></span> <span data-ttu-id="9cfd3-118">Asynchron.</span><span class="sxs-lookup"><span data-stu-id="9cfd3-118">Asynchronous.</span></span> <span data-ttu-id="9cfd3-119">Der inaktiven Vorgang wird abgebrochen, wenn das Fortsetzungs Bit später aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="9cfd3-119">Quiescing is cancelled if the Resume bit is called subsequently.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="9cfd3-120">Fortsetzen</span><span class="sxs-lookup"><span data-stu-id="9cfd3-120">Resume</span></span></td>
<td><span data-ttu-id="9cfd3-121">Setzt zuvor ausgestellte Stopp Dienst Vorgänge fort, d. h., der &quot; Dienst wird neu gestartet &quot; .</span><span class="sxs-lookup"><span data-stu-id="9cfd3-121">Resumes previously issued StopService operations, i.e. &quot;restarts service&quot;.</span></span> <span data-ttu-id="9cfd3-122">Kann mit oberhalb von grbits kombiniert werden, um bestimmte Dienste fortzusetzen, oder mit 0x0 werden alle vorherigen beendeten Dienste fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="9cfd3-122">Can be combined with above grbits to Resume specific services, or with 0x0 Resumes all previous stopped services.</span></span>
<p><span data-ttu-id="9cfd3-123">Warnung: dieses Bit kann nur verwendet werden, um JET_bitStopServiceBackground und JET_bitStopServiceQuiesceCaches fortzusetzen, wenn Sie eine JET_bitStopServiceAll oder JET_bitStopServiceAPI durchgeführt haben, schlägt der Versuch, JET_bitStopServiceResume zu verwenden, fehl.</span><span class="sxs-lookup"><span data-stu-id="9cfd3-123">Warning: This bit can only be used to resume JET_bitStopServiceBackground and JET_bitStopServiceQuiesceCaches, if you did a JET_bitStopServiceAll or JET_bitStopServiceAPI, attempting to use JET_bitStopServiceResume will fail.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="9cfd3-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9cfd3-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="9cfd3-125">Referenz</span><span class="sxs-lookup"><span data-stu-id="9cfd3-125">Reference</span></span>

[<span data-ttu-id="9cfd3-126">Microsoft. ISAM. ESENT. Interop. Windows8-Namespace</span><span class="sxs-lookup"><span data-stu-id="9cfd3-126">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
