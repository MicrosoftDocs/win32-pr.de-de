---
description: Weitere Informationen finden Sie in der API. JetSetCurrentIndex4-Methode.
title: API. JetSetCurrentIndex4-Methode
TOCTitle: 'JetSetCurrentIndex4 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetSetCurrentIndex4(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.String,Microsoft.Isam.Esent.Interop.JET_INDEXID,Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetsetcurrentindex4(v=EXCHG.10)
ms:contentKeyID: 55100806
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetSetCurrentIndex4
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetSetCurrentIndex4
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d2b9319554b998175b3f533c6cd5f4c2d05ba02f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346500"
---
# <a name="apijetsetcurrentindex4-method"></a><span data-ttu-id="6013f-103">API. JetSetCurrentIndex4-Methode</span><span class="sxs-lookup"><span data-stu-id="6013f-103">Api.JetSetCurrentIndex4 method</span></span>

<span data-ttu-id="6013f-104">Legen Sie den aktuellen Index eines Cursors fest.</span><span class="sxs-lookup"><span data-stu-id="6013f-104">Set the current index of a cursor.</span></span>

<span data-ttu-id="6013f-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="6013f-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="6013f-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="6013f-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="6013f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="6013f-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetSetCurrentIndex4 ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    index As String, _
    indexid As JET_INDEXID, _
    grbit As SetCurrentIndexGrbit, _
    itagSequence As Integer _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim index As String
Dim indexid As JET_INDEXID
Dim grbit As SetCurrentIndexGrbit
Dim itagSequence As IntegerApi.JetSetCurrentIndex4(sesid, _
    tableid, index, indexid, grbit, itagSequence)
```

``` csharp
public static void JetSetCurrentIndex4(
    JET_SESID sesid,
    JET_TABLEID tableid,
    string index,
    JET_INDEXID indexid,
    SetCurrentIndexGrbit grbit,
    int itagSequence
)
```

#### <a name="parameters"></a><span data-ttu-id="6013f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="6013f-108">Parameters</span></span>

  - <span data-ttu-id="6013f-109">-sid</span><span class="sxs-lookup"><span data-stu-id="6013f-109">sesid</span></span>  
    <span data-ttu-id="6013f-110">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="6013f-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="6013f-111">Die zu verwendende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="6013f-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="6013f-112">TableID</span><span class="sxs-lookup"><span data-stu-id="6013f-112">tableid</span></span>  
    <span data-ttu-id="6013f-113">Typ: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="6013f-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="6013f-114">Der Cursor, für den der Index festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="6013f-114">The cursor to set the index on.</span></span>

<!-- end list -->

  - <span data-ttu-id="6013f-115">Index</span><span class="sxs-lookup"><span data-stu-id="6013f-115">index</span></span>  
    <span data-ttu-id="6013f-116">Typ: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="6013f-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="6013f-117">Der Name des Indexes, der ausgewählt werden soll.</span><span class="sxs-lookup"><span data-stu-id="6013f-117">The name of the index to be selected.</span></span> <span data-ttu-id="6013f-118">Wenn dieser Wert NULL oder leer ist, wird der primäre Index ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="6013f-118">If this is null or empty the primary index will be selected.</span></span>

<!-- end list -->

  - <span data-ttu-id="6013f-119">indexid</span><span class="sxs-lookup"><span data-stu-id="6013f-119">indexid</span></span>  
    <span data-ttu-id="6013f-120">Typ: [Microsoft.ISAM.ESENT.Interop.JET_INDEXID](./jet-indexid-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="6013f-120">Type: [Microsoft.Isam.Esent.Interop.JET_INDEXID](./jet-indexid-structure2.md)</span></span>  
    
    <span data-ttu-id="6013f-121">Die ID des Indexes, der ausgewählt werden soll.</span><span class="sxs-lookup"><span data-stu-id="6013f-121">The id of the index to select.</span></span> <span data-ttu-id="6013f-122">Diese ID kann mithilfe von jetgetindexinfo oder jetgettableindexinfo mit der [IndexID](./jet-idxinfo-enumeration.md) -Option abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="6013f-122">This id can be obtained using JetGetIndexInfo or JetGetTableIndexInfo with the [IndexId](./jet-idxinfo-enumeration.md) option.</span></span>

<!-- end list -->

  - <span data-ttu-id="6013f-123">grbit</span><span class="sxs-lookup"><span data-stu-id="6013f-123">grbit</span></span>  
    <span data-ttu-id="6013f-124">Typ: [Microsoft. ISAM. ESENT. Interop. setcurrentindexgrbit](./setcurrentindexgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="6013f-124">Type: [Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit](./setcurrentindexgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="6013f-125">Legen Sie Index Optionen fest.</span><span class="sxs-lookup"><span data-stu-id="6013f-125">Set index options.</span></span>

<!-- end list -->

  - <span data-ttu-id="6013f-126">itagsequence</span><span class="sxs-lookup"><span data-stu-id="6013f-126">itagSequence</span></span>  
    <span data-ttu-id="6013f-127">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="6013f-127">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="6013f-128">Sequenznummer des Werts für mehrwertige Spalten, der verwendet wird, um den Cursor auf dem neuen Index zu positionieren.</span><span class="sxs-lookup"><span data-stu-id="6013f-128">Sequence number of the multi-valued column value which will be used to position the cursor on the new index.</span></span> <span data-ttu-id="6013f-129">Dieser Parameter wird nur in Verbindung mit [nomove](./setcurrentindexgrbit-enumeration.md)verwendet.</span><span class="sxs-lookup"><span data-stu-id="6013f-129">This parameter is only used in conjunction with [NoMove](./setcurrentindexgrbit-enumeration.md).</span></span> <span data-ttu-id="6013f-130">Wenn dieser Parameter nicht vorhanden oder auf 0 (null) festgelegt ist, wird als Wert 1 angenommen.</span><span class="sxs-lookup"><span data-stu-id="6013f-130">When this parameter is not present or is set to zero, its value is presumed to be 1.</span></span>

## <a name="see-also"></a><span data-ttu-id="6013f-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6013f-131">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="6013f-132">Referenz</span><span class="sxs-lookup"><span data-stu-id="6013f-132">Reference</span></span>

[<span data-ttu-id="6013f-133">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="6013f-133">Api class</span></span>](./api-class.md)

[<span data-ttu-id="6013f-134">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="6013f-134">Api members</span></span>](./api-members.md)

[<span data-ttu-id="6013f-135">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="6013f-135">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
