---
description: 'Weitere Informationen finden Sie hier: vistaapi. jedessnapshotprepareinzelstance-Methode'
title: Vistaapi. jedessnapshotpreparinstance-Methode (Microsoft. ISAM. ESENT. Interop. Vista)
TOCTitle: 'JetOSSnapshotPrepareInstance method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOSSnapshotPrepareInstance(Microsoft.Isam.Esent.Interop.JET_OSSNAPID,Microsoft.Isam.Esent.Interop.JET_INSTANCE,Microsoft.Isam.Esent.Interop.Vista.SnapshotPrepareInstanceGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaapi.jetossnapshotprepareinstance(v=EXCHG.10)
ms:contentKeyID: 55104304
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOSSnapshotPrepareInstance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOSSnapshotPrepareInstance
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 46151e2b11c669ac9635ce5974757999a8636b56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131756"
---
# <a name="vistaapijetossnapshotprepareinstance-method"></a><span data-ttu-id="5b36f-103">Vistaapi. jedessnapshotprepareinzelstance-Methode</span><span class="sxs-lookup"><span data-stu-id="5b36f-103">VistaApi.JetOSSnapshotPrepareInstance method</span></span>

<span data-ttu-id="5b36f-104">Wählt eine bestimmte-Instanz aus, die Teil der Momentaufnahme Sitzung sein soll.</span><span class="sxs-lookup"><span data-stu-id="5b36f-104">Selects a specific instance to be part of the snapshot session.</span></span>

<span data-ttu-id="5b36f-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="5b36f-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="5b36f-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="5b36f-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="5b36f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="5b36f-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetOSSnapshotPrepareInstance ( _
    snapshot As JET_OSSNAPID, _
    instance As JET_INSTANCE, _
    grbit As SnapshotPrepareInstanceGrbit _
)
'Usage
Dim snapshot As JET_OSSNAPID
Dim instance As JET_INSTANCE
Dim grbit As SnapshotPrepareInstanceGrbitVistaApi.JetOSSnapshotPrepareInstance(snapshot, _
    instance, grbit)
```

``` csharp
public static void JetOSSnapshotPrepareInstance(
    JET_OSSNAPID snapshot,
    JET_INSTANCE instance,
    SnapshotPrepareInstanceGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="5b36f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="5b36f-108">Parameters</span></span>

  - <span data-ttu-id="5b36f-109">Momentaufnahme</span><span class="sxs-lookup"><span data-stu-id="5b36f-109">snapshot</span></span>  
    <span data-ttu-id="5b36f-110">Typ: [Microsoft.ISAM.ESENT.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="5b36f-110">Type: [Microsoft.Isam.Esent.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)</span></span>  
    
    <span data-ttu-id="5b36f-111">Der Momentaufnahme Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="5b36f-111">The snapshot identifier.</span></span>

<!-- end list -->

  - <span data-ttu-id="5b36f-112">instance</span><span class="sxs-lookup"><span data-stu-id="5b36f-112">instance</span></span>  
    <span data-ttu-id="5b36f-113">Typ: [Microsoft.ISAM.ESENT.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="5b36f-113">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="5b36f-114">Die-Instanz, die der Momentaufnahme hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="5b36f-114">The instance to add to the snapshot.</span></span>

<!-- end list -->

  - <span data-ttu-id="5b36f-115">grbit</span><span class="sxs-lookup"><span data-stu-id="5b36f-115">grbit</span></span>  
    <span data-ttu-id="5b36f-116">Typ: [Microsoft. ISAM. ESENT. Interop. Vista. snapshotprepareinstancegrbit](./snapshotprepareinstancegrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="5b36f-116">Type: [Microsoft.Isam.Esent.Interop.Vista.SnapshotPrepareInstanceGrbit](./snapshotprepareinstancegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="5b36f-117">Optionen für diesen-Befehl.</span><span class="sxs-lookup"><span data-stu-id="5b36f-117">Options for this call.</span></span>

## <a name="see-also"></a><span data-ttu-id="5b36f-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5b36f-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="5b36f-119">Referenz</span><span class="sxs-lookup"><span data-stu-id="5b36f-119">Reference</span></span>

[<span data-ttu-id="5b36f-120">Vistaapi-Klasse</span><span class="sxs-lookup"><span data-stu-id="5b36f-120">VistaApi class</span></span>](./vistaapi-class.md)

[<span data-ttu-id="5b36f-121">Vistaapi-Member</span><span class="sxs-lookup"><span data-stu-id="5b36f-121">VistaApi members</span></span>](./vistaapi-members.md)

[<span data-ttu-id="5b36f-122">Microsoft. ISAM. ESENT. Interop. Vista-Namespace</span><span class="sxs-lookup"><span data-stu-id="5b36f-122">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
