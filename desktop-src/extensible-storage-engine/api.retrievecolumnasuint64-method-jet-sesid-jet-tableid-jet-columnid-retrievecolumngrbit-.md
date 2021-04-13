---
description: 'Weitere Informationen finden Sie unter: API. RetrieveColumnAsUInt64-Methode (JET_SESID, JET_TABLEID, JET_COLUMNID, retrievecolenngrbit)'
title: API. RetrieveColumnAsUInt64-Methode (JET_SESID, JET_TABLEID, JET_COLUMNID, retrievecolenngrbit)
TOCTitle: RetrieveColumnAsUInt64 method (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsUInt64(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievecolumnasuint64(v=EXCHG.10)
ms:contentKeyID: 55100907
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsUInt64
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cb4de0dc72493d0b28716b5a0859aa19adfe62e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484166"
---
# <a name="apiretrievecolumnasuint64-method-jet_sesid-jet_tableid-jet_columnid-retrievecolumngrbit"></a><span data-ttu-id="43891-103">API. RetrieveColumnAsUInt64-Methode (JET_SESID, JET_TABLEID, JET_COLUMNID, retrievecolenngrbit)</span><span class="sxs-lookup"><span data-stu-id="43891-103">Api.RetrieveColumnAsUInt64 method (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)</span></span>

<span data-ttu-id="43891-104">Ruft einen UInt64-Spaltenwert aus dem aktuellen Datensatz ab.</span><span class="sxs-lookup"><span data-stu-id="43891-104">Retrieves a uint64 column value from the current record.</span></span> <span data-ttu-id="43891-105">Der Datensatz ist der Datensatz, der mit dem Index Eintrag an der aktuellen Position des Cursors verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="43891-105">The record is that record associated with the index entry at the current position of the cursor.</span></span>

<span data-ttu-id="43891-106">Diese API ist nicht CLS-kompatibel.</span><span class="sxs-lookup"><span data-stu-id="43891-106">This API is not CLS-compliant.</span></span> 

<span data-ttu-id="43891-107">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="43891-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="43891-108">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="43891-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="43891-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="43891-109">Syntax</span></span>

``` vb
'Declaration
<CLSCompliantAttribute(False)> _
Public Shared Function RetrieveColumnAsUInt64 ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    grbit As RetrieveColumnGrbit _
) As Nullable(Of ULong)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim grbit As RetrieveColumnGrbit
Dim returnValue As Nullable(Of ULong)

returnValue = Api.RetrieveColumnAsUInt64(sesid, _
    tableid, columnid, grbit)
```

``` csharp
[CLSCompliantAttribute(false)]
public static Nullable<ulong> RetrieveColumnAsUInt64(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    RetrieveColumnGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="43891-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="43891-110">Parameters</span></span>

  - <span data-ttu-id="43891-111">-sid</span><span class="sxs-lookup"><span data-stu-id="43891-111">sesid</span></span>  
    <span data-ttu-id="43891-112">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="43891-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="43891-113">Die zu verwendende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="43891-113">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="43891-114">TableID</span><span class="sxs-lookup"><span data-stu-id="43891-114">tableid</span></span>  
    <span data-ttu-id="43891-115">Typ: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="43891-115">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="43891-116">Der Cursor, von dem die Spalte abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="43891-116">The cursor to retrieve the column from.</span></span>

<!-- end list -->

  - <span data-ttu-id="43891-117">columnid</span><span class="sxs-lookup"><span data-stu-id="43891-117">columnid</span></span>  
    <span data-ttu-id="43891-118">Typ: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="43891-118">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="43891-119">Das abzurufende ColumnID.</span><span class="sxs-lookup"><span data-stu-id="43891-119">The columnid to retrieve.</span></span>

<!-- end list -->

  - <span data-ttu-id="43891-120">grbit</span><span class="sxs-lookup"><span data-stu-id="43891-120">grbit</span></span>  
    <span data-ttu-id="43891-121">Typ: [Microsoft. ISAM. ESENT. Interop. retrievecolenngrbit](./retrievecolumngrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="43891-121">Type: [Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit](./retrievecolumngrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="43891-122">Abruf Optionen.</span><span class="sxs-lookup"><span data-stu-id="43891-122">Retrieval options.</span></span>

#### <a name="return-value"></a><span data-ttu-id="43891-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="43891-123">Return value</span></span>

<span data-ttu-id="43891-124">Typ: [System. Nullable](/dotnet/api/system.nullable-1)\<[UInt64](/dotnet/api/system.uint64)\></span><span class="sxs-lookup"><span data-stu-id="43891-124">Type: [System.Nullable](/dotnet/api/system.nullable-1)\<[UInt64](/dotnet/api/system.uint64)\></span></span>  
<span data-ttu-id="43891-125">Die Daten, die aus der Spalte als UInt64 abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="43891-125">The data retrieved from the column as an UInt64.</span></span> <span data-ttu-id="43891-126">NULL, wenn die Spalte NULL ist.</span><span class="sxs-lookup"><span data-stu-id="43891-126">Null if the column is null.</span></span>  

## <a name="see-also"></a><span data-ttu-id="43891-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="43891-127">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="43891-128">Referenz</span><span class="sxs-lookup"><span data-stu-id="43891-128">Reference</span></span>

[<span data-ttu-id="43891-129">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="43891-129">Api class</span></span>](./api-class.md)

[<span data-ttu-id="43891-130">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="43891-130">Api members</span></span>](./api-members.md)

[<span data-ttu-id="43891-131">RetrieveColumnAsUInt64-Überladung</span><span class="sxs-lookup"><span data-stu-id="43891-131">RetrieveColumnAsUInt64 overload</span></span>](./api.retrievecolumnasuint64-method.md)

[<span data-ttu-id="43891-132">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="43891-132">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
