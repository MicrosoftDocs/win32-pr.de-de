---
description: 'Weitere Informationen finden Sie unter: API. retrievecolennsize-Methode (JET_SESID, JET_TABLEID, JET_COLUMNID)'
title: API. retrievecolennsize-Methode (JET_SESID, JET_TABLEID, JET_COLUMNID)
TOCTitle: RetrieveColumnSize method (JET_SESID, JET_TABLEID, JET_COLUMNID)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.RetrieveColumnSize(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievecolumnsize(v=EXCHG.10)
ms:contentKeyID: 55100868
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
ms.openlocfilehash: 6f75ce51e942cfde7fddc4f9ec0154feae985e02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351552"
---
# <a name="apiretrievecolumnsize-method-jet_sesid-jet_tableid-jet_columnid"></a><span data-ttu-id="6c559-103">API. retrievecolennsize-Methode (JET_SESID, JET_TABLEID, JET_COLUMNID)</span><span class="sxs-lookup"><span data-stu-id="6c559-103">Api.RetrieveColumnSize method (JET_SESID, JET_TABLEID, JET_COLUMNID)</span></span>

<span data-ttu-id="6c559-104">Ruft die Größe eines einzelnen Spaltenwerts aus dem aktuellen Datensatz ab.</span><span class="sxs-lookup"><span data-stu-id="6c559-104">Retrieves the size of a single column value from the current record.</span></span> <span data-ttu-id="6c559-105">Der Datensatz ist der Datensatz, der mit dem Index Eintrag an der aktuellen Position des Cursors verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="6c559-105">The record is that record associated with the index entry at the current position of the cursor.</span></span> <span data-ttu-id="6c559-106">Alternativ kann diese Funktion eine Spalte aus einem Datensatz abrufen, der im Cursor Kopier Puffer erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="6c559-106">Alternatively, this function can retrieve a column from a record being created in the cursor copy buffer.</span></span> <span data-ttu-id="6c559-107">Diese Funktion kann auch Spaltendaten aus einem Index Eintrag abrufen, der auf den aktuellen Datensatz verweist.</span><span class="sxs-lookup"><span data-stu-id="6c559-107">This function can also retrieve column data from an index entry that references the current record.</span></span>

<span data-ttu-id="6c559-108">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="6c559-108">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="6c559-109">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="6c559-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="6c559-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="6c559-110">Syntax</span></span>

``` vb
'Declaration
Public Shared Function RetrieveColumnSize ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID _
) As Nullable(Of Integer)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim returnValue As Nullable(Of Integer)

returnValue = Api.RetrieveColumnSize(sesid, _
    tableid, columnid)
```

``` csharp
public static Nullable<int> RetrieveColumnSize(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid
)
```

#### <a name="parameters"></a><span data-ttu-id="6c559-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="6c559-111">Parameters</span></span>

  - <span data-ttu-id="6c559-112">-sid</span><span class="sxs-lookup"><span data-stu-id="6c559-112">sesid</span></span>  
    <span data-ttu-id="6c559-113">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="6c559-113">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="6c559-114">Die zu verwendende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="6c559-114">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="6c559-115">TableID</span><span class="sxs-lookup"><span data-stu-id="6c559-115">tableid</span></span>  
    <span data-ttu-id="6c559-116">Typ: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="6c559-116">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="6c559-117">Der Cursor, von dem die Spalte abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="6c559-117">The cursor to retrieve the column from.</span></span>

<!-- end list -->

  - <span data-ttu-id="6c559-118">columnid</span><span class="sxs-lookup"><span data-stu-id="6c559-118">columnid</span></span>  
    <span data-ttu-id="6c559-119">Typ: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="6c559-119">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="6c559-120">Das abzurufende ColumnID.</span><span class="sxs-lookup"><span data-stu-id="6c559-120">The columnid to retrieve.</span></span>

#### <a name="return-value"></a><span data-ttu-id="6c559-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6c559-121">Return value</span></span>

<span data-ttu-id="6c559-122">Typ: [System. Nullable](/dotnet/api/system.nullable-1)\<[Int32](/dotnet/api/system.int32)\></span><span class="sxs-lookup"><span data-stu-id="6c559-122">Type: [System.Nullable](/dotnet/api/system.nullable-1)\<[Int32](/dotnet/api/system.int32)\></span></span>  
<span data-ttu-id="6c559-123">Die Größe der Spalte.</span><span class="sxs-lookup"><span data-stu-id="6c559-123">The size of the column.</span></span> <span data-ttu-id="6c559-124">0, wenn die Spalte NULL ist.</span><span class="sxs-lookup"><span data-stu-id="6c559-124">0 if the column is null.</span></span>  

## <a name="see-also"></a><span data-ttu-id="6c559-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6c559-125">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="6c559-126">Referenz</span><span class="sxs-lookup"><span data-stu-id="6c559-126">Reference</span></span>

[<span data-ttu-id="6c559-127">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="6c559-127">Api class</span></span>](./api-class.md)

[<span data-ttu-id="6c559-128">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="6c559-128">Api members</span></span>](./api-members.md)

[<span data-ttu-id="6c559-129">Retrievecolübernsize-Überladung</span><span class="sxs-lookup"><span data-stu-id="6c559-129">RetrieveColumnSize overload</span></span>](./api.retrievecolumnsize-method.md)

[<span data-ttu-id="6c559-130">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="6c559-130">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
