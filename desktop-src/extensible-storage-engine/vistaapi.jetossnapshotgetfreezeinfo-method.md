---
description: 'Weitere Informationen finden Sie hier: vistaapi. jedessnapshotgetfrezeinfo-Methode'
title: Vistaapi. jedessnapshotgetfrezeinfo-Methode (Microsoft. ISAM. ESENT. Interop. Vista)
TOCTitle: 'JetOSSnapshotGetFreezeInfo method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOSSnapshotGetFreezeInfo(Microsoft.Isam.Esent.Interop.JET_OSSNAPID,System.Int32@,Microsoft.Isam.Esent.Interop.JET_INSTANCE_INFO[]@,Microsoft.Isam.Esent.Interop.Vista.SnapshotGetFreezeInfoGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaapi.jetossnapshotgetfreezeinfo(v=EXCHG.10)
ms:contentKeyID: 55104199
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOSSnapshotGetFreezeInfo
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOSSnapshotGetFreezeInfo
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 84b8f33f1fcac280e8fee65c1092c8fccdec3b0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347057"
---
# <a name="vistaapijetossnapshotgetfreezeinfo-method"></a><span data-ttu-id="2dd26-103">Vistaapi. jedessnapshotgetfrezeinfo-Methode</span><span class="sxs-lookup"><span data-stu-id="2dd26-103">VistaApi.JetOSSnapshotGetFreezeInfo method</span></span>

<span data-ttu-id="2dd26-104">Ruft die Liste der-Instanzen und-Datenbanken ab, die zu einem beliebigen Zeitpunkt Teil der Momentaufnahme Sitzung sind.</span><span class="sxs-lookup"><span data-stu-id="2dd26-104">Retrieves the list of instances and databases that are part of the snapshot session at any given moment.</span></span>

<span data-ttu-id="2dd26-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="2dd26-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="2dd26-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="2dd26-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="2dd26-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="2dd26-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetOSSnapshotGetFreezeInfo ( _
    snapshot As JET_OSSNAPID, _
    <OutAttribute> ByRef numInstances As Integer, _
    <OutAttribute> ByRef instances As JET_INSTANCE_INFO(), _
    grbit As SnapshotGetFreezeInfoGrbit _
)
'Usage
Dim snapshot As JET_OSSNAPID
Dim numInstances As Integer
Dim instances As JET_INSTANCE_INFO()
Dim grbit As SnapshotGetFreezeInfoGrbitVistaApi.JetOSSnapshotGetFreezeInfo(snapshot, _
    numInstances, instances, grbit)
```

``` csharp
public static void JetOSSnapshotGetFreezeInfo(
    JET_OSSNAPID snapshot,
    out int numInstances,
    out JET_INSTANCE_INFO[] instances,
    SnapshotGetFreezeInfoGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="2dd26-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="2dd26-108">Parameters</span></span>

  - <span data-ttu-id="2dd26-109">Momentaufnahme</span><span class="sxs-lookup"><span data-stu-id="2dd26-109">snapshot</span></span>  
    <span data-ttu-id="2dd26-110">Typ: [Microsoft.ISAM.ESENT.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="2dd26-110">Type: [Microsoft.Isam.Esent.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)</span></span>  
    
    <span data-ttu-id="2dd26-111">Der Bezeichner der Momentaufnahme Sitzung.</span><span class="sxs-lookup"><span data-stu-id="2dd26-111">The identifier of the snapshot session.</span></span>

<!-- end list -->

  - <span data-ttu-id="2dd26-112">numinstance</span><span class="sxs-lookup"><span data-stu-id="2dd26-112">numInstances</span></span>  
    <span data-ttu-id="2dd26-113">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="2dd26-113">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="2dd26-114">Gibt die Anzahl von-Instanzen zurück.</span><span class="sxs-lookup"><span data-stu-id="2dd26-114">Returns the number of instances.</span></span>

<!-- end list -->

  - <span data-ttu-id="2dd26-115">instances</span><span class="sxs-lookup"><span data-stu-id="2dd26-115">instances</span></span>  
    <span data-ttu-id="2dd26-116">Sorte \[\]</span><span class="sxs-lookup"><span data-stu-id="2dd26-116">Type: \[\]</span></span>  
    
    <span data-ttu-id="2dd26-117">Gibt Informationen zu den-Instanzen zurück.</span><span class="sxs-lookup"><span data-stu-id="2dd26-117">Returns information about the instances.</span></span>

<!-- end list -->

  - <span data-ttu-id="2dd26-118">grbit</span><span class="sxs-lookup"><span data-stu-id="2dd26-118">grbit</span></span>  
    <span data-ttu-id="2dd26-119">Typ: [Microsoft. ISAM. ESENT. Interop. Vista. snapshotgetfrezeinfogrbit](./snapshotgetfreezeinfogrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="2dd26-119">Type: [Microsoft.Isam.Esent.Interop.Vista.SnapshotGetFreezeInfoGrbit](./snapshotgetfreezeinfogrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="2dd26-120">Optionen für diesen-Befehl.</span><span class="sxs-lookup"><span data-stu-id="2dd26-120">Options for this call.</span></span>

## <a name="see-also"></a><span data-ttu-id="2dd26-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2dd26-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="2dd26-122">Referenz</span><span class="sxs-lookup"><span data-stu-id="2dd26-122">Reference</span></span>

[<span data-ttu-id="2dd26-123">Vistaapi-Klasse</span><span class="sxs-lookup"><span data-stu-id="2dd26-123">VistaApi class</span></span>](./vistaapi-class.md)

[<span data-ttu-id="2dd26-124">Vistaapi-Member</span><span class="sxs-lookup"><span data-stu-id="2dd26-124">VistaApi members</span></span>](./vistaapi-members.md)

[<span data-ttu-id="2dd26-125">Microsoft. ISAM. ESENT. Interop. Vista-Namespace</span><span class="sxs-lookup"><span data-stu-id="2dd26-125">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
