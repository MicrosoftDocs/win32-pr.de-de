---
description: 'Weitere Informationen finden Sie unter: API. RetrieveColumnAsUInt32-Methode (JET_SESID, JET_TABLEID, JET_COLUMNID)'
title: API. RetrieveColumnAsUInt32-Methode (JET_SESID, JET_TABLEID, JET_COLUMNID)
TOCTitle: RetrieveColumnAsUInt32 method (JET_SESID, JET_TABLEID, JET_COLUMNID)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsUInt32(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievecolumnasuint32(v=EXCHG.10)
ms:contentKeyID: 55100903
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsUInt32
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b889245cd2e2f37907a15e3ec31b04a4d932dd02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524720"
---
# <a name="apiretrievecolumnasuint32-method-jet_sesid-jet_tableid-jet_columnid"></a><span data-ttu-id="fd9d2-103">API. RetrieveColumnAsUInt32-Methode (JET_SESID, JET_TABLEID, JET_COLUMNID)</span><span class="sxs-lookup"><span data-stu-id="fd9d2-103">Api.RetrieveColumnAsUInt32 method (JET_SESID, JET_TABLEID, JET_COLUMNID)</span></span>

<span data-ttu-id="fd9d2-104">Ruft einen UInt32-Spaltenwert aus dem aktuellen Datensatz ab.</span><span class="sxs-lookup"><span data-stu-id="fd9d2-104">Retrieves a uint32 column value from the current record.</span></span> <span data-ttu-id="fd9d2-105">Der Datensatz ist der Datensatz, der mit dem Index Eintrag an der aktuellen Position des Cursors verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="fd9d2-105">The record is that record associated with the index entry at the current position of the cursor.</span></span>

<span data-ttu-id="fd9d2-106">Diese API ist nicht CLS-kompatibel.</span><span class="sxs-lookup"><span data-stu-id="fd9d2-106">This API is not CLS-compliant.</span></span> 

<span data-ttu-id="fd9d2-107">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="fd9d2-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="fd9d2-108">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="fd9d2-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="fd9d2-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="fd9d2-109">Syntax</span></span>

``` vb
'Declaration
<CLSCompliantAttribute(False)> _
Public Shared Function RetrieveColumnAsUInt32 ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID _
) As Nullable(Of UInteger)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim returnValue As Nullable(Of UInteger)

returnValue = Api.RetrieveColumnAsUInt32(sesid, _
    tableid, columnid)
```

``` csharp
[CLSCompliantAttribute(false)]
public static Nullable<uint> RetrieveColumnAsUInt32(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid
)
```

#### <a name="parameters"></a><span data-ttu-id="fd9d2-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="fd9d2-110">Parameters</span></span>

  - <span data-ttu-id="fd9d2-111">-sid</span><span class="sxs-lookup"><span data-stu-id="fd9d2-111">sesid</span></span>  
    <span data-ttu-id="fd9d2-112">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="fd9d2-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="fd9d2-113">Die zu verwendende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="fd9d2-113">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="fd9d2-114">TableID</span><span class="sxs-lookup"><span data-stu-id="fd9d2-114">tableid</span></span>  
    <span data-ttu-id="fd9d2-115">Typ: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="fd9d2-115">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="fd9d2-116">Der Cursor, von dem die Spalte abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="fd9d2-116">The cursor to retrieve the column from.</span></span>

<!-- end list -->

  - <span data-ttu-id="fd9d2-117">columnid</span><span class="sxs-lookup"><span data-stu-id="fd9d2-117">columnid</span></span>  
    <span data-ttu-id="fd9d2-118">Typ: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="fd9d2-118">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="fd9d2-119">Das abzurufende ColumnID.</span><span class="sxs-lookup"><span data-stu-id="fd9d2-119">The columnid to retrieve.</span></span>

#### <a name="return-value"></a><span data-ttu-id="fd9d2-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fd9d2-120">Return value</span></span>

<span data-ttu-id="fd9d2-121">Typ: [System. Nullable](/dotnet/api/system.nullable-1)\<[UInt32](/dotnet/api/system.uint32)\></span><span class="sxs-lookup"><span data-stu-id="fd9d2-121">Type: [System.Nullable](/dotnet/api/system.nullable-1)\<[UInt32](/dotnet/api/system.uint32)\></span></span>  
<span data-ttu-id="fd9d2-122">Die Daten, die aus der Spalte als UInt32 abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="fd9d2-122">The data retrieved from the column as an UInt32.</span></span> <span data-ttu-id="fd9d2-123">NULL, wenn die Spalte NULL ist.</span><span class="sxs-lookup"><span data-stu-id="fd9d2-123">Null if the column is null.</span></span>  

## <a name="see-also"></a><span data-ttu-id="fd9d2-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fd9d2-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="fd9d2-125">Referenz</span><span class="sxs-lookup"><span data-stu-id="fd9d2-125">Reference</span></span>

[<span data-ttu-id="fd9d2-126">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="fd9d2-126">Api class</span></span>](./api-class.md)

[<span data-ttu-id="fd9d2-127">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="fd9d2-127">Api members</span></span>](./api-members.md)

[<span data-ttu-id="fd9d2-128">RetrieveColumnAsUInt32-Überladung</span><span class="sxs-lookup"><span data-stu-id="fd9d2-128">RetrieveColumnAsUInt32 overload</span></span>](./api.retrievecolumnasuint32-method.md)

[<span data-ttu-id="fd9d2-129">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="fd9d2-129">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
