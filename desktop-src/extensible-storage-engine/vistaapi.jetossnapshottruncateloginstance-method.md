---
description: 'Weitere Informationen finden Sie hier: vistaapi. jedessnapshottruneureloginstance-Methode'
title: Vistaapi. jedessnapshottruneureloginstance-Methode (Microsoft. ISAM. ESENT. Interop. Vista)
TOCTitle: 'JetOSSnapshotTruncateLogInstance method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOSSnapshotTruncateLogInstance(Microsoft.Isam.Esent.Interop.JET_OSSNAPID,Microsoft.Isam.Esent.Interop.JET_INSTANCE,Microsoft.Isam.Esent.Interop.Vista.SnapshotTruncateLogGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaapi.jetossnapshottruncateloginstance(v=EXCHG.10)
ms:contentKeyID: 55104197
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOSSnapshotTruncateLogInstance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOSSnapshotTruncateLogInstance
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 75d694629585a730f5c1c7b9b08bb7b06e735cb0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103869128"
---
# <a name="vistaapijetossnapshottruncateloginstance-method"></a><span data-ttu-id="7d157-103">Vistaapi. jedessnapshottruneureloginstance-Methode</span><span class="sxs-lookup"><span data-stu-id="7d157-103">VistaApi.JetOSSnapshotTruncateLogInstance method</span></span>

<span data-ttu-id="7d157-104">Verkürzt das Protokoll für eine angegebene-Instanz während einer Momentaufnahme Sitzung.</span><span class="sxs-lookup"><span data-stu-id="7d157-104">Truncates the log for a specified instance during a snapshot session.</span></span>

<span data-ttu-id="7d157-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="7d157-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="7d157-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="7d157-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="7d157-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="7d157-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetOSSnapshotTruncateLogInstance ( _
    snapshot As JET_OSSNAPID, _
    instance As JET_INSTANCE, _
    grbit As SnapshotTruncateLogGrbit _
)
'Usage
Dim snapshot As JET_OSSNAPID
Dim instance As JET_INSTANCE
Dim grbit As SnapshotTruncateLogGrbitVistaApi.JetOSSnapshotTruncateLogInstance(snapshot, _
    instance, grbit)
```

``` csharp
public static void JetOSSnapshotTruncateLogInstance(
    JET_OSSNAPID snapshot,
    JET_INSTANCE instance,
    SnapshotTruncateLogGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="7d157-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="7d157-108">Parameters</span></span>

  - <span data-ttu-id="7d157-109">Momentaufnahme</span><span class="sxs-lookup"><span data-stu-id="7d157-109">snapshot</span></span>  
    <span data-ttu-id="7d157-110">Typ: [Microsoft.ISAM.ESENT.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="7d157-110">Type: [Microsoft.Isam.Esent.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)</span></span>  
    
    <span data-ttu-id="7d157-111">Der Momentaufnahme Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="7d157-111">The snapshot identifier.</span></span>

<!-- end list -->

  - <span data-ttu-id="7d157-112">instance</span><span class="sxs-lookup"><span data-stu-id="7d157-112">instance</span></span>  
    <span data-ttu-id="7d157-113">Typ: [Microsoft.ISAM.ESENT.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="7d157-113">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="7d157-114">Die-Instanz, für die das Protokoll abgeschnitten werden soll.</span><span class="sxs-lookup"><span data-stu-id="7d157-114">The instance to truncat the log for.</span></span>

<!-- end list -->

  - <span data-ttu-id="7d157-115">grbit</span><span class="sxs-lookup"><span data-stu-id="7d157-115">grbit</span></span>  
    <span data-ttu-id="7d157-116">Typ: [Microsoft. ISAM. ESENT. Interop. Vista. snapshottruneureloggrbit](./snapshottruncateloggrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="7d157-116">Type: [Microsoft.Isam.Esent.Interop.Vista.SnapshotTruncateLogGrbit](./snapshottruncateloggrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="7d157-117">Optionen für diesen-Befehl.</span><span class="sxs-lookup"><span data-stu-id="7d157-117">Options for this call.</span></span>

## <a name="remarks"></a><span data-ttu-id="7d157-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7d157-118">Remarks</span></span>

<span data-ttu-id="7d157-119">Diese Funktion sollte nur aufgerufen werden, wenn die Momentaufnahme mit der Option [continueafterthaw](./vistagrbits.continueafterthaw-field.md) erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="7d157-119">This function should be called only if the snapshot was created with the [ContinueAfterThaw](./vistagrbits.continueafterthaw-field.md) option.</span></span> <span data-ttu-id="7d157-120">Andernfalls wird die Momentaufnahme Sitzung nach dem Aufrufe von [jedessnapshotthaw (JET_OSSNAPID, snapshotthawgrbit)](./api.jetossnapshotthaw-method.md)beendet.</span><span class="sxs-lookup"><span data-stu-id="7d157-120">Otherwise, the snapshot session ends after the call to [JetOSSnapshotThaw(JET_OSSNAPID, SnapshotThawGrbit)](./api.jetossnapshotthaw-method.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="7d157-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7d157-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="7d157-122">Referenz</span><span class="sxs-lookup"><span data-stu-id="7d157-122">Reference</span></span>

[<span data-ttu-id="7d157-123">Vistaapi-Klasse</span><span class="sxs-lookup"><span data-stu-id="7d157-123">VistaApi class</span></span>](./vistaapi-class.md)

[<span data-ttu-id="7d157-124">Vistaapi-Member</span><span class="sxs-lookup"><span data-stu-id="7d157-124">VistaApi members</span></span>](./vistaapi-members.md)

[<span data-ttu-id="7d157-125">Microsoft. ISAM. ESENT. Interop. Vista-Namespace</span><span class="sxs-lookup"><span data-stu-id="7d157-125">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
