---
description: 'Weitere Informationen finden Sie unter: API. RetrieveColumnAsInt64-Methode (JET_SESID, JET_TABLEID, JET_COLUMNID)'
title: API. RetrieveColumnAsInt64-Methode (JET_SESID, JET_TABLEID, JET_COLUMNID)
TOCTitle: RetrieveColumnAsInt64 method (JET_SESID, JET_TABLEID, JET_COLUMNID)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsInt64(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievecolumnasint64(v=EXCHG.10)
ms:contentKeyID: 55100858
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsInt64
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4edd9c8a8495a56e14c655357397c5a693239062
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861835"
---
# <a name="apiretrievecolumnasint64-method-jet_sesid-jet_tableid-jet_columnid"></a><span data-ttu-id="b74a0-103">API. RetrieveColumnAsInt64-Methode (JET_SESID, JET_TABLEID, JET_COLUMNID)</span><span class="sxs-lookup"><span data-stu-id="b74a0-103">Api.RetrieveColumnAsInt64 method (JET_SESID, JET_TABLEID, JET_COLUMNID)</span></span>

<span data-ttu-id="b74a0-104">Ruft einen einzelnen Spaltenwert aus dem aktuellen Datensatz ab.</span><span class="sxs-lookup"><span data-stu-id="b74a0-104">Retrieves a single column value from the current record.</span></span> <span data-ttu-id="b74a0-105">Der Datensatz ist der Datensatz, der mit dem Index Eintrag an der aktuellen Position des Cursors verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="b74a0-105">The record is that record associated with the index entry at the current position of the cursor.</span></span>

<span data-ttu-id="b74a0-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b74a0-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="b74a0-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="b74a0-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b74a0-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="b74a0-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function RetrieveColumnAsInt64 ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID _
) As Nullable(Of Long)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim returnValue As Nullable(Of Long)

returnValue = Api.RetrieveColumnAsInt64(sesid, _
    tableid, columnid)
```

``` csharp
public static Nullable<long> RetrieveColumnAsInt64(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid
)
```

#### <a name="parameters"></a><span data-ttu-id="b74a0-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="b74a0-109">Parameters</span></span>

  - <span data-ttu-id="b74a0-110">-sid</span><span class="sxs-lookup"><span data-stu-id="b74a0-110">sesid</span></span>  
    <span data-ttu-id="b74a0-111">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="b74a0-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="b74a0-112">Die zu verwendende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="b74a0-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="b74a0-113">TableID</span><span class="sxs-lookup"><span data-stu-id="b74a0-113">tableid</span></span>  
    <span data-ttu-id="b74a0-114">Typ: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="b74a0-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="b74a0-115">Der Cursor, von dem die Spalte abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="b74a0-115">The cursor to retrieve the column from.</span></span>

<!-- end list -->

  - <span data-ttu-id="b74a0-116">columnid</span><span class="sxs-lookup"><span data-stu-id="b74a0-116">columnid</span></span>  
    <span data-ttu-id="b74a0-117">Typ: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="b74a0-117">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="b74a0-118">Das abzurufende ColumnID.</span><span class="sxs-lookup"><span data-stu-id="b74a0-118">The columnid to retrieve.</span></span>

#### <a name="return-value"></a><span data-ttu-id="b74a0-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b74a0-119">Return value</span></span>

<span data-ttu-id="b74a0-120">Typ: [System. Nullable](/dotnet/api/system.nullable-1)\<[Int64](/dotnet/api/system.int64)\></span><span class="sxs-lookup"><span data-stu-id="b74a0-120">Type: [System.Nullable](/dotnet/api/system.nullable-1)\<[Int64](/dotnet/api/system.int64)\></span></span>  
<span data-ttu-id="b74a0-121">Die Daten, die aus der Spalte als Long abgerufen wurden.</span><span class="sxs-lookup"><span data-stu-id="b74a0-121">The data retrieved from the column as a long.</span></span> <span data-ttu-id="b74a0-122">NULL, wenn die Spalte NULL ist.</span><span class="sxs-lookup"><span data-stu-id="b74a0-122">Null if the column is null.</span></span>  

## <a name="see-also"></a><span data-ttu-id="b74a0-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b74a0-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b74a0-124">Referenz</span><span class="sxs-lookup"><span data-stu-id="b74a0-124">Reference</span></span>

[<span data-ttu-id="b74a0-125">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="b74a0-125">Api class</span></span>](./api-class.md)

[<span data-ttu-id="b74a0-126">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="b74a0-126">Api members</span></span>](./api-members.md)

[<span data-ttu-id="b74a0-127">RetrieveColumnAsInt64-Überladung</span><span class="sxs-lookup"><span data-stu-id="b74a0-127">RetrieveColumnAsInt64 overload</span></span>](./api.retrievecolumnasint64-method.md)

[<span data-ttu-id="b74a0-128">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="b74a0-128">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
