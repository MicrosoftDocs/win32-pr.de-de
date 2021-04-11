---
description: 'Weitere Informationen finden Sie unter: API. RetrieveColumnAsUInt16-Methode (JET_SESID, JET_TABLEID, JET_COLUMNID)'
title: API. RetrieveColumnAsUInt16-Methode (JET_SESID, JET_TABLEID, JET_COLUMNID)
TOCTitle: RetrieveColumnAsUInt16 method (JET_SESID, JET_TABLEID, JET_COLUMNID)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsUInt16(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievecolumnasuint16(v=EXCHG.10)
ms:contentKeyID: 55100861
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsUInt16
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8a89ed851d54d142d5a8253fe94707848b6df7de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217735"
---
# <a name="apiretrievecolumnasuint16-method-jet_sesid-jet_tableid-jet_columnid"></a><span data-ttu-id="5c734-103">API. RetrieveColumnAsUInt16-Methode (JET_SESID, JET_TABLEID, JET_COLUMNID)</span><span class="sxs-lookup"><span data-stu-id="5c734-103">Api.RetrieveColumnAsUInt16 method (JET_SESID, JET_TABLEID, JET_COLUMNID)</span></span>

<span data-ttu-id="5c734-104">Ruft einen UInt16-Spaltenwert aus dem aktuellen Datensatz ab.</span><span class="sxs-lookup"><span data-stu-id="5c734-104">Retrieves a uint16 column value from the current record.</span></span> <span data-ttu-id="5c734-105">Der Datensatz ist der Datensatz, der mit dem Index Eintrag an der aktuellen Position des Cursors verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="5c734-105">The record is that record associated with the index entry at the current position of the cursor.</span></span>

<span data-ttu-id="5c734-106">Diese API ist nicht CLS-kompatibel.</span><span class="sxs-lookup"><span data-stu-id="5c734-106">This API is not CLS-compliant.</span></span> 

<span data-ttu-id="5c734-107">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="5c734-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="5c734-108">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="5c734-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="5c734-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="5c734-109">Syntax</span></span>

``` vb
'Declaration
<CLSCompliantAttribute(False)> _
Public Shared Function RetrieveColumnAsUInt16 ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID _
) As Nullable(Of UShort)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim returnValue As Nullable(Of UShort)

returnValue = Api.RetrieveColumnAsUInt16(sesid, _
    tableid, columnid)
```

``` csharp
[CLSCompliantAttribute(false)]
public static Nullable<ushort> RetrieveColumnAsUInt16(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid
)
```

#### <a name="parameters"></a><span data-ttu-id="5c734-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="5c734-110">Parameters</span></span>

  - <span data-ttu-id="5c734-111">-sid</span><span class="sxs-lookup"><span data-stu-id="5c734-111">sesid</span></span>  
    <span data-ttu-id="5c734-112">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="5c734-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="5c734-113">Die zu verwendende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="5c734-113">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="5c734-114">TableID</span><span class="sxs-lookup"><span data-stu-id="5c734-114">tableid</span></span>  
    <span data-ttu-id="5c734-115">Typ: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="5c734-115">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="5c734-116">Der Cursor, von dem die Spalte abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="5c734-116">The cursor to retrieve the column from.</span></span>

<!-- end list -->

  - <span data-ttu-id="5c734-117">columnid</span><span class="sxs-lookup"><span data-stu-id="5c734-117">columnid</span></span>  
    <span data-ttu-id="5c734-118">Typ: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="5c734-118">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="5c734-119">Das abzurufende ColumnID.</span><span class="sxs-lookup"><span data-stu-id="5c734-119">The columnid to retrieve.</span></span>

#### <a name="return-value"></a><span data-ttu-id="5c734-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5c734-120">Return value</span></span>

<span data-ttu-id="5c734-121">Typ: [System. Nullable](/dotnet/api/system.nullable-1)\<[UInt16](/dotnet/api/system.uint16)\></span><span class="sxs-lookup"><span data-stu-id="5c734-121">Type: [System.Nullable](/dotnet/api/system.nullable-1)\<[UInt16](/dotnet/api/system.uint16)\></span></span>  
<span data-ttu-id="5c734-122">Die Daten, die aus der Spalte als UInt16 abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="5c734-122">The data retrieved from the column as an UInt16.</span></span> <span data-ttu-id="5c734-123">NULL, wenn die Spalte NULL ist.</span><span class="sxs-lookup"><span data-stu-id="5c734-123">Null if the column is null.</span></span>  

## <a name="see-also"></a><span data-ttu-id="5c734-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5c734-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="5c734-125">Referenz</span><span class="sxs-lookup"><span data-stu-id="5c734-125">Reference</span></span>

[<span data-ttu-id="5c734-126">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="5c734-126">Api class</span></span>](./api-class.md)

[<span data-ttu-id="5c734-127">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="5c734-127">Api members</span></span>](./api-members.md)

[<span data-ttu-id="5c734-128">RetrieveColumnAsUInt16-Überladung</span><span class="sxs-lookup"><span data-stu-id="5c734-128">RetrieveColumnAsUInt16 overload</span></span>](./api.retrievecolumnasuint16-method.md)

[<span data-ttu-id="5c734-129">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="5c734-129">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
