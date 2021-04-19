---
description: 'Weitere Informationen finden Sie unter: API. RetrieveColumnAsInt16-Methode (JET_SESID, JET_TABLEID, JET_COLUMNID, retrievecolenngrbit)'
title: API. RetrieveColumnAsInt16-Methode (JET_SESID, JET_TABLEID, JET_COLUMNID, retrievecolenngrbit)
TOCTitle: RetrieveColumnAsInt16 method (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsInt16(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievecolumnasint16(v=EXCHG.10)
ms:contentKeyID: 55100890
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsInt16
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1972d3cc8ac75d25b140f00e6ff215c7d1a47106
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360801"
---
# <a name="apiretrievecolumnasint16-method-jet_sesid-jet_tableid-jet_columnid-retrievecolumngrbit"></a><span data-ttu-id="dce70-103">API. RetrieveColumnAsInt16-Methode (JET_SESID, JET_TABLEID, JET_COLUMNID, retrievecolenngrbit)</span><span class="sxs-lookup"><span data-stu-id="dce70-103">Api.RetrieveColumnAsInt16 method (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)</span></span>

<span data-ttu-id="dce70-104">Ruft einen Int16-Spaltenwert aus dem aktuellen Datensatz ab.</span><span class="sxs-lookup"><span data-stu-id="dce70-104">Retrieves an int16 column value from the current record.</span></span> <span data-ttu-id="dce70-105">Der Datensatz ist der Datensatz, der mit dem Index Eintrag an der aktuellen Position des Cursors verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="dce70-105">The record is that record associated with the index entry at the current position of the cursor.</span></span>

<span data-ttu-id="dce70-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="dce70-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="dce70-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="dce70-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="dce70-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="dce70-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function RetrieveColumnAsInt16 ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    grbit As RetrieveColumnGrbit _
) As Nullable(Of Short)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim grbit As RetrieveColumnGrbit
Dim returnValue As Nullable(Of Short)

returnValue = Api.RetrieveColumnAsInt16(sesid, _
    tableid, columnid, grbit)
```

``` csharp
public static Nullable<short> RetrieveColumnAsInt16(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    RetrieveColumnGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="dce70-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="dce70-109">Parameters</span></span>

  - <span data-ttu-id="dce70-110">-sid</span><span class="sxs-lookup"><span data-stu-id="dce70-110">sesid</span></span>  
    <span data-ttu-id="dce70-111">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="dce70-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="dce70-112">Die zu verwendende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="dce70-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="dce70-113">TableID</span><span class="sxs-lookup"><span data-stu-id="dce70-113">tableid</span></span>  
    <span data-ttu-id="dce70-114">Typ: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="dce70-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="dce70-115">Der Cursor, von dem die Spalte abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="dce70-115">The cursor to retrieve the column from.</span></span>

<!-- end list -->

  - <span data-ttu-id="dce70-116">columnid</span><span class="sxs-lookup"><span data-stu-id="dce70-116">columnid</span></span>  
    <span data-ttu-id="dce70-117">Typ: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="dce70-117">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="dce70-118">Das abzurufende ColumnID.</span><span class="sxs-lookup"><span data-stu-id="dce70-118">The columnid to retrieve.</span></span>

<!-- end list -->

  - <span data-ttu-id="dce70-119">grbit</span><span class="sxs-lookup"><span data-stu-id="dce70-119">grbit</span></span>  
    <span data-ttu-id="dce70-120">Typ: [Microsoft. ISAM. ESENT. Interop. retrievecolenngrbit](./retrievecolumngrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="dce70-120">Type: [Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit](./retrievecolumngrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="dce70-121">Abruf Optionen.</span><span class="sxs-lookup"><span data-stu-id="dce70-121">Retrieval options.</span></span>

#### <a name="return-value"></a><span data-ttu-id="dce70-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="dce70-122">Return value</span></span>

<span data-ttu-id="dce70-123">Typ: [System. Nullable](/dotnet/api/system.nullable-1)\<[Int16](/dotnet/api/system.int16)\></span><span class="sxs-lookup"><span data-stu-id="dce70-123">Type: [System.Nullable](/dotnet/api/system.nullable-1)\<[Int16](/dotnet/api/system.int16)\></span></span>  
<span data-ttu-id="dce70-124">Die Daten, die aus der Spalte als kurz abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="dce70-124">The data retrieved from the column as a short.</span></span> <span data-ttu-id="dce70-125">NULL, wenn die Spalte NULL ist.</span><span class="sxs-lookup"><span data-stu-id="dce70-125">Null if the column is null.</span></span>  

## <a name="see-also"></a><span data-ttu-id="dce70-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dce70-126">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="dce70-127">Referenz</span><span class="sxs-lookup"><span data-stu-id="dce70-127">Reference</span></span>

[<span data-ttu-id="dce70-128">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="dce70-128">Api class</span></span>](./api-class.md)

[<span data-ttu-id="dce70-129">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="dce70-129">Api members</span></span>](./api-members.md)

[<span data-ttu-id="dce70-130">RetrieveColumnAsInt16-Überladung</span><span class="sxs-lookup"><span data-stu-id="dce70-130">RetrieveColumnAsInt16 overload</span></span>](./api.retrievecolumnasint16-method.md)

[<span data-ttu-id="dce70-131">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="dce70-131">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
