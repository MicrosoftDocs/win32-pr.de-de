---
description: Weitere Informationen finden Sie in der API. jedessnapshotfreeze-Methode.
title: API. jedessnapshotfreeze-Methode
TOCTitle: 'JetOSSnapshotFreeze method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetOSSnapshotFreeze(Microsoft.Isam.Esent.Interop.JET_OSSNAPID,System.Int32@,Microsoft.Isam.Esent.Interop.JET_INSTANCE_INFO[]@,Microsoft.Isam.Esent.Interop.SnapshotFreezeGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetossnapshotfreeze(v=EXCHG.10)
ms:contentKeyID: 55100793
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetOSSnapshotFreeze
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetOSSnapshotFreeze
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b7434cb79e90f99ab946c86a97559079352956fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218279"
---
# <a name="apijetossnapshotfreeze-method"></a><span data-ttu-id="7a12a-103">API. jedessnapshotfreeze-Methode</span><span class="sxs-lookup"><span data-stu-id="7a12a-103">Api.JetOSSnapshotFreeze method</span></span>

<span data-ttu-id="7a12a-104">Startet eine Momentaufnahme.</span><span class="sxs-lookup"><span data-stu-id="7a12a-104">Starts a snapshot.</span></span> <span data-ttu-id="7a12a-105">Während der Momentaufnahme kann keine Aktivität zum Schreiben von Datenträgern durch die Engine durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="7a12a-105">While the snapshot is in progress, no write-to-disk activity by the engine can take place.</span></span>

<span data-ttu-id="7a12a-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="7a12a-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="7a12a-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="7a12a-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="7a12a-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="7a12a-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetOSSnapshotFreeze ( _
    snapshot As JET_OSSNAPID, _
    <OutAttribute> ByRef numInstances As Integer, _
    <OutAttribute> ByRef instances As JET_INSTANCE_INFO(), _
    grbit As SnapshotFreezeGrbit _
)
'Usage
Dim snapshot As JET_OSSNAPID
Dim numInstances As Integer
Dim instances As JET_INSTANCE_INFO()
Dim grbit As SnapshotFreezeGrbitApi.JetOSSnapshotFreeze(snapshot, _
    numInstances, instances, grbit)
```

``` csharp
public static void JetOSSnapshotFreeze(
    JET_OSSNAPID snapshot,
    out int numInstances,
    out JET_INSTANCE_INFO[] instances,
    SnapshotFreezeGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="7a12a-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="7a12a-109">Parameters</span></span>

  - <span data-ttu-id="7a12a-110">Momentaufnahme</span><span class="sxs-lookup"><span data-stu-id="7a12a-110">snapshot</span></span>  
    <span data-ttu-id="7a12a-111">Typ: [Microsoft.ISAM.ESENT.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="7a12a-111">Type: [Microsoft.Isam.Esent.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)</span></span>  
    
    <span data-ttu-id="7a12a-112">Die Momentaufnahme Sitzung.</span><span class="sxs-lookup"><span data-stu-id="7a12a-112">The snapshot session.</span></span>

<!-- end list -->

  - <span data-ttu-id="7a12a-113">numinstance</span><span class="sxs-lookup"><span data-stu-id="7a12a-113">numInstances</span></span>  
    <span data-ttu-id="7a12a-114">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="7a12a-114">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="7a12a-115">Gibt die Anzahl der-Instanzen zurück, die Teil der Momentaufnahme Sitzung sind.</span><span class="sxs-lookup"><span data-stu-id="7a12a-115">Returns the number of instances that are part of the snapshot session.</span></span>

<!-- end list -->

  - <span data-ttu-id="7a12a-116">instances</span><span class="sxs-lookup"><span data-stu-id="7a12a-116">instances</span></span>  
    <span data-ttu-id="7a12a-117">Sorte \[\]</span><span class="sxs-lookup"><span data-stu-id="7a12a-117">Type: \[\]</span></span>  
    
    <span data-ttu-id="7a12a-118">Gibt Informationen zu den-Instanzen zurück, die Teil der Momentaufnahme Sitzung sind.</span><span class="sxs-lookup"><span data-stu-id="7a12a-118">Returns information about the instances that are part of the snapshot session.</span></span>

<!-- end list -->

  - <span data-ttu-id="7a12a-119">grbit</span><span class="sxs-lookup"><span data-stu-id="7a12a-119">grbit</span></span>  
    <span data-ttu-id="7a12a-120">Typ: [Microsoft. ISAM. ESENT. Interop. snapshotfrezegrbit](./snapshotfreezegrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="7a12a-120">Type: [Microsoft.Isam.Esent.Interop.SnapshotFreezeGrbit](./snapshotfreezegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="7a12a-121">Optionen für Momentaufnahme einfrieren.</span><span class="sxs-lookup"><span data-stu-id="7a12a-121">Snapshot freeze options.</span></span>

## <a name="see-also"></a><span data-ttu-id="7a12a-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7a12a-122">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="7a12a-123">Referenz</span><span class="sxs-lookup"><span data-stu-id="7a12a-123">Reference</span></span>

[<span data-ttu-id="7a12a-124">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="7a12a-124">Api class</span></span>](./api-class.md)

[<span data-ttu-id="7a12a-125">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="7a12a-125">Api members</span></span>](./api-members.md)

[<span data-ttu-id="7a12a-126">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="7a12a-126">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
