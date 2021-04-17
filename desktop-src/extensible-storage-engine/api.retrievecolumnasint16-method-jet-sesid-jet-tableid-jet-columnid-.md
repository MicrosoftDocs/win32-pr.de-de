---
description: 'Weitere Informationen finden Sie unter: API. RetrieveColumnAsInt16-Methode (JET_SESID, JET_TABLEID, JET_COLUMNID)'
title: API. RetrieveColumnAsInt16-Methode (JET_SESID, JET_TABLEID, JET_COLUMNID)
TOCTitle: RetrieveColumnAsInt16 method (JET_SESID, JET_TABLEID, JET_COLUMNID)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsInt16(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievecolumnasint16(v=EXCHG.10)
ms:contentKeyID: 55100855
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
ms.openlocfilehash: 3590dcc9d646d0596d611553b8fbcd374bab7bbb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524744"
---
# <a name="apiretrievecolumnasint16-method-jet_sesid-jet_tableid-jet_columnid"></a><span data-ttu-id="fda37-103">API. RetrieveColumnAsInt16-Methode (JET_SESID, JET_TABLEID, JET_COLUMNID)</span><span class="sxs-lookup"><span data-stu-id="fda37-103">Api.RetrieveColumnAsInt16 method (JET_SESID, JET_TABLEID, JET_COLUMNID)</span></span>

<span data-ttu-id="fda37-104">Ruft einen einzelnen Spaltenwert aus dem aktuellen Datensatz ab.</span><span class="sxs-lookup"><span data-stu-id="fda37-104">Retrieves a single column value from the current record.</span></span> <span data-ttu-id="fda37-105">Der Datensatz ist der Datensatz, der mit dem Index Eintrag an der aktuellen Position des Cursors verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="fda37-105">The record is that record associated with the index entry at the current position of the cursor.</span></span>

<span data-ttu-id="fda37-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="fda37-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="fda37-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="fda37-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="fda37-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="fda37-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function RetrieveColumnAsInt16 ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID _
) As Nullable(Of Short)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim returnValue As Nullable(Of Short)

returnValue = Api.RetrieveColumnAsInt16(sesid, _
    tableid, columnid)
```

``` csharp
public static Nullable<short> RetrieveColumnAsInt16(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid
)
```

#### <a name="parameters"></a><span data-ttu-id="fda37-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="fda37-109">Parameters</span></span>

  - <span data-ttu-id="fda37-110">-sid</span><span class="sxs-lookup"><span data-stu-id="fda37-110">sesid</span></span>  
    <span data-ttu-id="fda37-111">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="fda37-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="fda37-112">Die zu verwendende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="fda37-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="fda37-113">TableID</span><span class="sxs-lookup"><span data-stu-id="fda37-113">tableid</span></span>  
    <span data-ttu-id="fda37-114">Typ: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="fda37-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="fda37-115">Der Cursor, von dem die Spalte abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="fda37-115">The cursor to retrieve the column from.</span></span>

<!-- end list -->

  - <span data-ttu-id="fda37-116">columnid</span><span class="sxs-lookup"><span data-stu-id="fda37-116">columnid</span></span>  
    <span data-ttu-id="fda37-117">Typ: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="fda37-117">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="fda37-118">Das abzurufende ColumnID.</span><span class="sxs-lookup"><span data-stu-id="fda37-118">The columnid to retrieve.</span></span>

#### <a name="return-value"></a><span data-ttu-id="fda37-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fda37-119">Return value</span></span>

<span data-ttu-id="fda37-120">Typ: [System. Nullable](/dotnet/api/system.nullable-1)\<[Int16](/dotnet/api/system.int16)\></span><span class="sxs-lookup"><span data-stu-id="fda37-120">Type: [System.Nullable](/dotnet/api/system.nullable-1)\<[Int16](/dotnet/api/system.int16)\></span></span>  
<span data-ttu-id="fda37-121">Die Daten, die aus der Spalte als kurz abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="fda37-121">The data retrieved from the column as a short.</span></span> <span data-ttu-id="fda37-122">NULL, wenn die Spalte NULL ist.</span><span class="sxs-lookup"><span data-stu-id="fda37-122">Null if the column is null.</span></span>  

## <a name="see-also"></a><span data-ttu-id="fda37-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fda37-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="fda37-124">Referenz</span><span class="sxs-lookup"><span data-stu-id="fda37-124">Reference</span></span>

[<span data-ttu-id="fda37-125">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="fda37-125">Api class</span></span>](./api-class.md)

[<span data-ttu-id="fda37-126">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="fda37-126">Api members</span></span>](./api-members.md)

[<span data-ttu-id="fda37-127">RetrieveColumnAsInt16-Überladung</span><span class="sxs-lookup"><span data-stu-id="fda37-127">RetrieveColumnAsInt16 overload</span></span>](./api.retrievecolumnasint16-method.md)

[<span data-ttu-id="fda37-128">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="fda37-128">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
