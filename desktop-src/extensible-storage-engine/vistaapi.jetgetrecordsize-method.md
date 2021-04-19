---
description: 'Weitere Informationen finden Sie hier: vistaapi. jetgetrecordsize-Methode'
title: Vistaapi. jetgetrecordsize-Methode (Microsoft. ISAM. ESENT. Interop. Vista)
TOCTitle: 'JetGetRecordSize method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetGetRecordSize(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE@,Microsoft.Isam.Esent.Interop.GetRecordSizeGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaapi.jetgetrecordsize(v=EXCHG.10)
ms:contentKeyID: 55104285
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetGetRecordSize
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetGetRecordSize
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 37576e39d83270dcac3333e4d1f78fce32bb2669
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349026"
---
# <a name="vistaapijetgetrecordsize-method"></a><span data-ttu-id="37530-103">Vistaapi. jetgetrecordsize-Methode</span><span class="sxs-lookup"><span data-stu-id="37530-103">VistaApi.JetGetRecordSize method</span></span>

<span data-ttu-id="37530-104">Ruft Informationen zur Daten Satz Größe vom gewünschten Speicherort ab.</span><span class="sxs-lookup"><span data-stu-id="37530-104">Retrieves record size information from the desired location.</span></span>

<span data-ttu-id="37530-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="37530-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="37530-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="37530-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="37530-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="37530-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetRecordSize ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    ByRef recsize As JET_RECSIZE, _
    grbit As GetRecordSizeGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim recsize As JET_RECSIZE
Dim grbit As GetRecordSizeGrbitVistaApi.JetGetRecordSize(sesid, tableid, _
    recsize, grbit)
```

``` csharp
public static void JetGetRecordSize(
    JET_SESID sesid,
    JET_TABLEID tableid,
    ref JET_RECSIZE recsize,
    GetRecordSizeGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="37530-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="37530-108">Parameters</span></span>

  - <span data-ttu-id="37530-109">-sid</span><span class="sxs-lookup"><span data-stu-id="37530-109">sesid</span></span>  
    <span data-ttu-id="37530-110">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="37530-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="37530-111">Die zu verwendende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="37530-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="37530-112">TableID</span><span class="sxs-lookup"><span data-stu-id="37530-112">tableid</span></span>  
    <span data-ttu-id="37530-113">Typ: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="37530-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="37530-114">Der Cursor, der für den API-Befehl verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="37530-114">The cursor that will be used for the API call.</span></span> <span data-ttu-id="37530-115">Der Cursor muss auf einem Datensatz positioniert werden, oder es muss ein Update vorbereitet werden.</span><span class="sxs-lookup"><span data-stu-id="37530-115">The cursor must be positioned on a record, or have an update prepared.</span></span>

<!-- end list -->

  - <span data-ttu-id="37530-116">neugröße</span><span class="sxs-lookup"><span data-stu-id="37530-116">recsize</span></span>  
    <span data-ttu-id="37530-117">Typ: [Microsoft.ISAM.ESENT.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="37530-117">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)</span></span>  
    
    <span data-ttu-id="37530-118">Gibt die Größe des Datensatzes zurück.</span><span class="sxs-lookup"><span data-stu-id="37530-118">Returns the size of the record.</span></span>

<!-- end list -->

  - <span data-ttu-id="37530-119">grbit</span><span class="sxs-lookup"><span data-stu-id="37530-119">grbit</span></span>  
    <span data-ttu-id="37530-120">Typ: [Microsoft. ISAM. ESENT. Interop. getrecordsizegrbit](./getrecordsizegrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="37530-120">Type: [Microsoft.Isam.Esent.Interop.GetRecordSizeGrbit](./getrecordsizegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="37530-121">Ruft Optionen auf.</span><span class="sxs-lookup"><span data-stu-id="37530-121">Call options.</span></span>

## <a name="see-also"></a><span data-ttu-id="37530-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="37530-122">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="37530-123">Referenz</span><span class="sxs-lookup"><span data-stu-id="37530-123">Reference</span></span>

[<span data-ttu-id="37530-124">Vistaapi-Klasse</span><span class="sxs-lookup"><span data-stu-id="37530-124">VistaApi class</span></span>](./vistaapi-class.md)

[<span data-ttu-id="37530-125">Vistaapi-Member</span><span class="sxs-lookup"><span data-stu-id="37530-125">VistaApi members</span></span>](./vistaapi-members.md)

[<span data-ttu-id="37530-126">Microsoft. ISAM. ESENT. Interop. Vista-Namespace</span><span class="sxs-lookup"><span data-stu-id="37530-126">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
