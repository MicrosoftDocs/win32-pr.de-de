---
description: 'Weitere Informationen finden Sie hier: vistaapi. jedessnapshottruneurelog-Methode'
title: Vistaapi. jedessnapshottruneurelog-Methode (Microsoft. ISAM. ESENT. Interop. Vista)
TOCTitle: 'JetOSSnapshotTruncateLog method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOSSnapshotTruncateLog(Microsoft.Isam.Esent.Interop.JET_OSSNAPID,Microsoft.Isam.Esent.Interop.Vista.SnapshotTruncateLogGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaapi.jetossnapshottruncatelog(v=EXCHG.10)
ms:contentKeyID: 55104308
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOSSnapshotTruncateLog
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOSSnapshotTruncateLog
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0af8054bc414ea5dbd6c7225fa9e2cd7117c74c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346887"
---
# <a name="vistaapijetossnapshottruncatelog-method"></a><span data-ttu-id="e109b-103">Vistaapi. jedessnapshottruneurelog-Methode</span><span class="sxs-lookup"><span data-stu-id="e109b-103">VistaApi.JetOSSnapshotTruncateLog method</span></span>

<span data-ttu-id="e109b-104">Ermöglicht das Abschneiden von Protokollen für alle Instanzen, die Teil der Momentaufnahme Sitzung sind.</span><span class="sxs-lookup"><span data-stu-id="e109b-104">Enables log truncation for all instances that are part of the snapshot session.</span></span>

<span data-ttu-id="e109b-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e109b-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="e109b-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="e109b-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e109b-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e109b-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetOSSnapshotTruncateLog ( _
    snapshot As JET_OSSNAPID, _
    grbit As SnapshotTruncateLogGrbit _
)
'Usage
Dim snapshot As JET_OSSNAPID
Dim grbit As SnapshotTruncateLogGrbitVistaApi.JetOSSnapshotTruncateLog(snapshot, _
    grbit)
```

``` csharp
public static void JetOSSnapshotTruncateLog(
    JET_OSSNAPID snapshot,
    SnapshotTruncateLogGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="e109b-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="e109b-108">Parameters</span></span>

  - <span data-ttu-id="e109b-109">Momentaufnahme</span><span class="sxs-lookup"><span data-stu-id="e109b-109">snapshot</span></span>  
    <span data-ttu-id="e109b-110">Typ: [Microsoft.ISAM.ESENT.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="e109b-110">Type: [Microsoft.Isam.Esent.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)</span></span>  
    
    <span data-ttu-id="e109b-111">Der Momentaufnahme Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="e109b-111">The snapshot identifier.</span></span>

<!-- end list -->

  - <span data-ttu-id="e109b-112">grbit</span><span class="sxs-lookup"><span data-stu-id="e109b-112">grbit</span></span>  
    <span data-ttu-id="e109b-113">Typ: [Microsoft. ISAM. ESENT. Interop. Vista. snapshottruneureloggrbit](./snapshottruncateloggrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="e109b-113">Type: [Microsoft.Isam.Esent.Interop.Vista.SnapshotTruncateLogGrbit](./snapshottruncateloggrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="e109b-114">Optionen für diesen-Befehl.</span><span class="sxs-lookup"><span data-stu-id="e109b-114">Options for this call.</span></span>

## <a name="remarks"></a><span data-ttu-id="e109b-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e109b-115">Remarks</span></span>

<span data-ttu-id="e109b-116">Diese Funktion sollte nur aufgerufen werden, wenn die Momentaufnahme mit der Option [continueafterthaw](./vistagrbits.continueafterthaw-field.md) erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="e109b-116">This function should be called only if the snapshot was created with the [ContinueAfterThaw](./vistagrbits.continueafterthaw-field.md) option.</span></span> <span data-ttu-id="e109b-117">Andernfalls wird die Momentaufnahme Sitzung nach dem Aufrufe von [jedessnapshotthaw (JET_OSSNAPID, snapshotthawgrbit)](./api.jetossnapshotthaw-method.md)beendet.</span><span class="sxs-lookup"><span data-stu-id="e109b-117">Otherwise, the snapshot session ends after the call to [JetOSSnapshotThaw(JET_OSSNAPID, SnapshotThawGrbit)](./api.jetossnapshotthaw-method.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="e109b-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e109b-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e109b-119">Referenz</span><span class="sxs-lookup"><span data-stu-id="e109b-119">Reference</span></span>

[<span data-ttu-id="e109b-120">Vistaapi-Klasse</span><span class="sxs-lookup"><span data-stu-id="e109b-120">VistaApi class</span></span>](./vistaapi-class.md)

[<span data-ttu-id="e109b-121">Vistaapi-Member</span><span class="sxs-lookup"><span data-stu-id="e109b-121">VistaApi members</span></span>](./vistaapi-members.md)

[<span data-ttu-id="e109b-122">Microsoft. ISAM. ESENT. Interop. Vista-Namespace</span><span class="sxs-lookup"><span data-stu-id="e109b-122">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
