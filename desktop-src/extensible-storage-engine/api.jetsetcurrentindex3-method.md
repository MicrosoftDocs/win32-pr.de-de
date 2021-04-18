---
description: Weitere Informationen finden Sie in der API. JetSetCurrentIndex3-Methode.
title: API. JetSetCurrentIndex3-Methode
TOCTitle: 'JetSetCurrentIndex3 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetSetCurrentIndex3(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.String,Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetsetcurrentindex3(v=EXCHG.10)
ms:contentKeyID: 55100805
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetSetCurrentIndex3
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetSetCurrentIndex3
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c56f259a35026bb47a5e58b7b364b52d9bedbc5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106368018"
---
# <a name="apijetsetcurrentindex3-method"></a><span data-ttu-id="45134-103">API. JetSetCurrentIndex3-Methode</span><span class="sxs-lookup"><span data-stu-id="45134-103">Api.JetSetCurrentIndex3 method</span></span>

<span data-ttu-id="45134-104">Legen Sie den aktuellen Index eines Cursors fest.</span><span class="sxs-lookup"><span data-stu-id="45134-104">Set the current index of a cursor.</span></span>

<span data-ttu-id="45134-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="45134-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="45134-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="45134-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="45134-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="45134-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetSetCurrentIndex3 ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    index As String, _
    grbit As SetCurrentIndexGrbit, _
    itagSequence As Integer _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim index As String
Dim grbit As SetCurrentIndexGrbit
Dim itagSequence As IntegerApi.JetSetCurrentIndex3(sesid, _
    tableid, index, grbit, itagSequence)
```

``` csharp
public static void JetSetCurrentIndex3(
    JET_SESID sesid,
    JET_TABLEID tableid,
    string index,
    SetCurrentIndexGrbit grbit,
    int itagSequence
)
```

#### <a name="parameters"></a><span data-ttu-id="45134-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="45134-108">Parameters</span></span>

  - <span data-ttu-id="45134-109">-sid</span><span class="sxs-lookup"><span data-stu-id="45134-109">sesid</span></span>  
    <span data-ttu-id="45134-110">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="45134-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="45134-111">Die zu verwendende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="45134-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="45134-112">TableID</span><span class="sxs-lookup"><span data-stu-id="45134-112">tableid</span></span>  
    <span data-ttu-id="45134-113">Typ: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="45134-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="45134-114">Der Cursor, für den der Index festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="45134-114">The cursor to set the index on.</span></span>

<!-- end list -->

  - <span data-ttu-id="45134-115">Index</span><span class="sxs-lookup"><span data-stu-id="45134-115">index</span></span>  
    <span data-ttu-id="45134-116">Typ: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="45134-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="45134-117">Der Name des Indexes, der ausgewählt werden soll.</span><span class="sxs-lookup"><span data-stu-id="45134-117">The name of the index to be selected.</span></span> <span data-ttu-id="45134-118">Wenn dieser Wert NULL oder leer ist, wird der primäre Index ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="45134-118">If this is null or empty the primary index will be selected.</span></span>

<!-- end list -->

  - <span data-ttu-id="45134-119">grbit</span><span class="sxs-lookup"><span data-stu-id="45134-119">grbit</span></span>  
    <span data-ttu-id="45134-120">Typ: [Microsoft. ISAM. ESENT. Interop. setcurrentindexgrbit](./setcurrentindexgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="45134-120">Type: [Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit](./setcurrentindexgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="45134-121">Legen Sie Index Optionen fest.</span><span class="sxs-lookup"><span data-stu-id="45134-121">Set index options.</span></span>

<!-- end list -->

  - <span data-ttu-id="45134-122">itagsequence</span><span class="sxs-lookup"><span data-stu-id="45134-122">itagSequence</span></span>  
    <span data-ttu-id="45134-123">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="45134-123">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="45134-124">Sequenznummer des Werts für mehrwertige Spalten, der verwendet wird, um den Cursor auf dem neuen Index zu positionieren.</span><span class="sxs-lookup"><span data-stu-id="45134-124">Sequence number of the multi-valued column value which will be used to position the cursor on the new index.</span></span> <span data-ttu-id="45134-125">Dieser Parameter wird nur in Verbindung mit [nomove](./setcurrentindexgrbit-enumeration.md)verwendet.</span><span class="sxs-lookup"><span data-stu-id="45134-125">This parameter is only used in conjunction with [NoMove](./setcurrentindexgrbit-enumeration.md).</span></span> <span data-ttu-id="45134-126">Wenn dieser Parameter nicht vorhanden oder auf 0 (null) festgelegt ist, wird als Wert 1 angenommen.</span><span class="sxs-lookup"><span data-stu-id="45134-126">When this parameter is not present or is set to zero, its value is presumed to be 1.</span></span>

## <a name="see-also"></a><span data-ttu-id="45134-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="45134-127">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="45134-128">Referenz</span><span class="sxs-lookup"><span data-stu-id="45134-128">Reference</span></span>

[<span data-ttu-id="45134-129">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="45134-129">Api class</span></span>](./api-class.md)

[<span data-ttu-id="45134-130">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="45134-130">Api members</span></span>](./api-members.md)

[<span data-ttu-id="45134-131">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="45134-131">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
