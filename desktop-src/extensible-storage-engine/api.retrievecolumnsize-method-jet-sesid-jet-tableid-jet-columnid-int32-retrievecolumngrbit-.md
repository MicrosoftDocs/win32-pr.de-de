---
description: 'Weitere Informationen finden Sie unter: API. retrievecolennsize-Methode (JET_SESID, JET_TABLEID, JET_COLUMNID, Int32, retrievecolenngrbit)'
title: API. retrievecolennsize-Methode (JET_SESID, JET_TABLEID, JET_COLUMNID, Int32, retrievecolenngrbit)
TOCTitle: RetrieveColumnSize method (JET_SESID, JET_TABLEID, JET_COLUMNID, Int32, RetrieveColumnGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.RetrieveColumnSize(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,System.Int32,Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievecolumnsize(v=EXCHG.10)
ms:contentKeyID: 55100912
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.RetrieveColumnSize
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: afd09ecca0362487d6c8e78f8e7c8d943f2f3269
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958663"
---
# <a name="apiretrievecolumnsize-method-jet_sesid-jet_tableid-jet_columnid-int32-retrievecolumngrbit"></a><span data-ttu-id="5ddad-103">API. retrievecolennsize-Methode (JET_SESID, JET_TABLEID, JET_COLUMNID, Int32, retrievecolenngrbit)</span><span class="sxs-lookup"><span data-stu-id="5ddad-103">Api.RetrieveColumnSize method (JET_SESID, JET_TABLEID, JET_COLUMNID, Int32, RetrieveColumnGrbit)</span></span>

<span data-ttu-id="5ddad-104">Ruft die Größe eines einzelnen Spaltenwerts aus dem aktuellen Datensatz ab.</span><span class="sxs-lookup"><span data-stu-id="5ddad-104">Retrieves the size of a single column value from the current record.</span></span> <span data-ttu-id="5ddad-105">Der Datensatz ist der Datensatz, der mit dem Index Eintrag an der aktuellen Position des Cursors verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="5ddad-105">The record is that record associated with the index entry at the current position of the cursor.</span></span> <span data-ttu-id="5ddad-106">Alternativ kann diese Funktion eine Spalte aus einem Datensatz abrufen, der im Cursor Kopier Puffer erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="5ddad-106">Alternatively, this function can retrieve a column from a record being created in the cursor copy buffer.</span></span> <span data-ttu-id="5ddad-107">Diese Funktion kann auch Spaltendaten aus einem Index Eintrag abrufen, der auf den aktuellen Datensatz verweist.</span><span class="sxs-lookup"><span data-stu-id="5ddad-107">This function can also retrieve column data from an index entry that references the current record.</span></span>

<span data-ttu-id="5ddad-108">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="5ddad-108">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="5ddad-109">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="5ddad-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="5ddad-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="5ddad-110">Syntax</span></span>

``` vb
'Declaration
Public Shared Function RetrieveColumnSize ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    itagSequence As Integer, _
    grbit As RetrieveColumnGrbit _
) As Nullable(Of Integer)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim itagSequence As Integer
Dim grbit As RetrieveColumnGrbit
Dim returnValue As Nullable(Of Integer)

returnValue = Api.RetrieveColumnSize(sesid, _
    tableid, columnid, itagSequence, _
    grbit)
```

``` csharp
public static Nullable<int> RetrieveColumnSize(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    int itagSequence,
    RetrieveColumnGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="5ddad-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="5ddad-111">Parameters</span></span>

  - <span data-ttu-id="5ddad-112">-sid</span><span class="sxs-lookup"><span data-stu-id="5ddad-112">sesid</span></span>  
    <span data-ttu-id="5ddad-113">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="5ddad-113">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="5ddad-114">Die zu verwendende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="5ddad-114">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="5ddad-115">TableID</span><span class="sxs-lookup"><span data-stu-id="5ddad-115">tableid</span></span>  
    <span data-ttu-id="5ddad-116">Typ: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="5ddad-116">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="5ddad-117">Der Cursor, von dem die Spalte abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="5ddad-117">The cursor to retrieve the column from.</span></span>

<!-- end list -->

  - <span data-ttu-id="5ddad-118">columnid</span><span class="sxs-lookup"><span data-stu-id="5ddad-118">columnid</span></span>  
    <span data-ttu-id="5ddad-119">Typ: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="5ddad-119">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="5ddad-120">Das abzurufende ColumnID.</span><span class="sxs-lookup"><span data-stu-id="5ddad-120">The columnid to retrieve.</span></span>

<!-- end list -->

  - <span data-ttu-id="5ddad-121">itagsequence</span><span class="sxs-lookup"><span data-stu-id="5ddad-121">itagSequence</span></span>  
    <span data-ttu-id="5ddad-122">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="5ddad-122">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="5ddad-123">Die Sequenznummer des Werts in einer mehrwertigen Spalte.</span><span class="sxs-lookup"><span data-stu-id="5ddad-123">The sequence number of value in a multi-valued column.</span></span> <span data-ttu-id="5ddad-124">Das Array von Werten ist 1-basiert.</span><span class="sxs-lookup"><span data-stu-id="5ddad-124">The array of values is one-based.</span></span> <span data-ttu-id="5ddad-125">Der erste Wert ist Sequenz 1, nicht 0.</span><span class="sxs-lookup"><span data-stu-id="5ddad-125">The first value is sequence 1, not 0.</span></span> <span data-ttu-id="5ddad-126">Wenn die Daten Satz Spalte nur über einen Wert verfügt, sollte 1 als itagsequence übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="5ddad-126">If the record column has only one value then 1 should be passed as the itagSequence.</span></span>

<!-- end list -->

  - <span data-ttu-id="5ddad-127">grbit</span><span class="sxs-lookup"><span data-stu-id="5ddad-127">grbit</span></span>  
    <span data-ttu-id="5ddad-128">Typ: [Microsoft. ISAM. ESENT. Interop. retrievecolenngrbit](./retrievecolumngrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="5ddad-128">Type: [Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit](./retrievecolumngrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="5ddad-129">Abrufen von Spalten Optionen.</span><span class="sxs-lookup"><span data-stu-id="5ddad-129">Retrieve column options.</span></span>

#### <a name="return-value"></a><span data-ttu-id="5ddad-130">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5ddad-130">Return value</span></span>

<span data-ttu-id="5ddad-131">Typ: [System. Nullable](/dotnet/api/system.nullable-1)\<[Int32](/dotnet/api/system.int32)\></span><span class="sxs-lookup"><span data-stu-id="5ddad-131">Type: [System.Nullable](/dotnet/api/system.nullable-1)\<[Int32](/dotnet/api/system.int32)\></span></span>  
<span data-ttu-id="5ddad-132">Die Größe der Spalte.</span><span class="sxs-lookup"><span data-stu-id="5ddad-132">The size of the column.</span></span> <span data-ttu-id="5ddad-133">0, wenn die Spalte NULL ist.</span><span class="sxs-lookup"><span data-stu-id="5ddad-133">0 if the column is null.</span></span>  

## <a name="see-also"></a><span data-ttu-id="5ddad-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5ddad-134">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="5ddad-135">Referenz</span><span class="sxs-lookup"><span data-stu-id="5ddad-135">Reference</span></span>

[<span data-ttu-id="5ddad-136">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="5ddad-136">Api class</span></span>](./api-class.md)

[<span data-ttu-id="5ddad-137">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="5ddad-137">Api members</span></span>](./api-members.md)

[<span data-ttu-id="5ddad-138">Retrievecolübernsize-Überladung</span><span class="sxs-lookup"><span data-stu-id="5ddad-138">RetrieveColumnSize overload</span></span>](./api.retrievecolumnsize-method.md)

[<span data-ttu-id="5ddad-139">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="5ddad-139">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
