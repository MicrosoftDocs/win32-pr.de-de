---
description: 'Weitere Informationen finden Sie unter: API. RetrieveColumnAsInt32-Methode (JET_SESID, JET_TABLEID, JET_COLUMNID, retrievecolenngrbit)'
title: API. RetrieveColumnAsInt32-Methode (JET_SESID, JET_TABLEID, JET_COLUMNID, retrievecolenngrbit)
TOCTitle: RetrieveColumnAsInt32 method (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsInt32(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievecolumnasint32(v=EXCHG.10)
ms:contentKeyID: 55100859
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsInt32
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5e9f963d298610fb36f6b1f9c9ff3a0bfbfa2501
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524739"
---
# <a name="apiretrievecolumnasint32-method-jet_sesid-jet_tableid-jet_columnid-retrievecolumngrbit"></a><span data-ttu-id="d3512-103">API. RetrieveColumnAsInt32-Methode (JET_SESID, JET_TABLEID, JET_COLUMNID, retrievecolenngrbit)</span><span class="sxs-lookup"><span data-stu-id="d3512-103">Api.RetrieveColumnAsInt32 method (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)</span></span>

<span data-ttu-id="d3512-104">Ruft einen Int32-Spaltenwert aus dem aktuellen Datensatz ab.</span><span class="sxs-lookup"><span data-stu-id="d3512-104">Retrieves an int32 column value from the current record.</span></span> <span data-ttu-id="d3512-105">Der Datensatz ist der Datensatz, der mit dem Index Eintrag an der aktuellen Position des Cursors verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="d3512-105">The record is that record associated with the index entry at the current position of the cursor.</span></span>

<span data-ttu-id="d3512-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="d3512-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="d3512-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="d3512-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="d3512-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="d3512-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function RetrieveColumnAsInt32 ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    grbit As RetrieveColumnGrbit _
) As Nullable(Of Integer)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim grbit As RetrieveColumnGrbit
Dim returnValue As Nullable(Of Integer)

returnValue = Api.RetrieveColumnAsInt32(sesid, _
    tableid, columnid, grbit)
```

``` csharp
public static Nullable<int> RetrieveColumnAsInt32(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    RetrieveColumnGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="d3512-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="d3512-109">Parameters</span></span>

  - <span data-ttu-id="d3512-110">-sid</span><span class="sxs-lookup"><span data-stu-id="d3512-110">sesid</span></span>  
    <span data-ttu-id="d3512-111">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="d3512-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="d3512-112">Die zu verwendende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="d3512-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="d3512-113">TableID</span><span class="sxs-lookup"><span data-stu-id="d3512-113">tableid</span></span>  
    <span data-ttu-id="d3512-114">Typ: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="d3512-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="d3512-115">Der Cursor, von dem die Spalte abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="d3512-115">The cursor to retrieve the column from.</span></span>

<!-- end list -->

  - <span data-ttu-id="d3512-116">columnid</span><span class="sxs-lookup"><span data-stu-id="d3512-116">columnid</span></span>  
    <span data-ttu-id="d3512-117">Typ: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="d3512-117">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="d3512-118">Das abzurufende ColumnID.</span><span class="sxs-lookup"><span data-stu-id="d3512-118">The columnid to retrieve.</span></span>

<!-- end list -->

  - <span data-ttu-id="d3512-119">grbit</span><span class="sxs-lookup"><span data-stu-id="d3512-119">grbit</span></span>  
    <span data-ttu-id="d3512-120">Typ: [Microsoft. ISAM. ESENT. Interop. retrievecolenngrbit](./retrievecolumngrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="d3512-120">Type: [Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit](./retrievecolumngrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="d3512-121">Abruf Optionen.</span><span class="sxs-lookup"><span data-stu-id="d3512-121">Retrieval options.</span></span>

#### <a name="return-value"></a><span data-ttu-id="d3512-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d3512-122">Return value</span></span>

<span data-ttu-id="d3512-123">Typ: [System. Nullable](/dotnet/api/system.nullable-1)\<[Int32](/dotnet/api/system.int32)\></span><span class="sxs-lookup"><span data-stu-id="d3512-123">Type: [System.Nullable](/dotnet/api/system.nullable-1)\<[Int32](/dotnet/api/system.int32)\></span></span>  
<span data-ttu-id="d3512-124">Die Daten, die aus der Spalte als int abgerufen werden. NULL, wenn die Spalte NULL ist.</span><span class="sxs-lookup"><span data-stu-id="d3512-124">The data retrieved from the column as an int. Null if the column is null.</span></span>  

## <a name="see-also"></a><span data-ttu-id="d3512-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d3512-125">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d3512-126">Referenz</span><span class="sxs-lookup"><span data-stu-id="d3512-126">Reference</span></span>

[<span data-ttu-id="d3512-127">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="d3512-127">Api class</span></span>](./api-class.md)

[<span data-ttu-id="d3512-128">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="d3512-128">Api members</span></span>](./api-members.md)

[<span data-ttu-id="d3512-129">RetrieveColumnAsInt32-Überladung</span><span class="sxs-lookup"><span data-stu-id="d3512-129">RetrieveColumnAsInt32 overload</span></span>](./api.retrievecolumnasint32-method.md)

[<span data-ttu-id="d3512-130">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="d3512-130">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
