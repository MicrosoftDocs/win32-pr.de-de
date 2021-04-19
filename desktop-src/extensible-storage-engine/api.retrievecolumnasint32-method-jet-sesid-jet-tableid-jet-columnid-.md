---
description: 'Weitere Informationen finden Sie unter: API. RetrieveColumnAsInt32-Methode (JET_SESID, JET_TABLEID, JET_COLUMNID)'
title: API. RetrieveColumnAsInt32-Methode (JET_SESID, JET_TABLEID, JET_COLUMNID)
TOCTitle: RetrieveColumnAsInt32 method (JET_SESID, JET_TABLEID, JET_COLUMNID)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsInt32(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievecolumnasint32(v=EXCHG.10)
ms:contentKeyID: 55100894
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
ms.openlocfilehash: c2e6bb69ca1b278cbb930de7c20611645283ee59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364213"
---
# <a name="apiretrievecolumnasint32-method-jet_sesid-jet_tableid-jet_columnid"></a><span data-ttu-id="3e22a-103">API. RetrieveColumnAsInt32-Methode (JET_SESID, JET_TABLEID, JET_COLUMNID)</span><span class="sxs-lookup"><span data-stu-id="3e22a-103">Api.RetrieveColumnAsInt32 method (JET_SESID, JET_TABLEID, JET_COLUMNID)</span></span>

<span data-ttu-id="3e22a-104">Ruft einen einzelnen Spaltenwert aus dem aktuellen Datensatz ab.</span><span class="sxs-lookup"><span data-stu-id="3e22a-104">Retrieves a single column value from the current record.</span></span> <span data-ttu-id="3e22a-105">Der Datensatz ist der Datensatz, der mit dem Index Eintrag an der aktuellen Position des Cursors verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="3e22a-105">The record is that record associated with the index entry at the current position of the cursor.</span></span>

<span data-ttu-id="3e22a-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="3e22a-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="3e22a-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="3e22a-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="3e22a-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="3e22a-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function RetrieveColumnAsInt32 ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID _
) As Nullable(Of Integer)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim returnValue As Nullable(Of Integer)

returnValue = Api.RetrieveColumnAsInt32(sesid, _
    tableid, columnid)
```

``` csharp
public static Nullable<int> RetrieveColumnAsInt32(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid
)
```

#### <a name="parameters"></a><span data-ttu-id="3e22a-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="3e22a-109">Parameters</span></span>

  - <span data-ttu-id="3e22a-110">-sid</span><span class="sxs-lookup"><span data-stu-id="3e22a-110">sesid</span></span>  
    <span data-ttu-id="3e22a-111">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="3e22a-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="3e22a-112">Die zu verwendende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="3e22a-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="3e22a-113">TableID</span><span class="sxs-lookup"><span data-stu-id="3e22a-113">tableid</span></span>  
    <span data-ttu-id="3e22a-114">Typ: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="3e22a-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="3e22a-115">Der Cursor, von dem die Spalte abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="3e22a-115">The cursor to retrieve the column from.</span></span>

<!-- end list -->

  - <span data-ttu-id="3e22a-116">columnid</span><span class="sxs-lookup"><span data-stu-id="3e22a-116">columnid</span></span>  
    <span data-ttu-id="3e22a-117">Typ: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="3e22a-117">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="3e22a-118">Das abzurufende ColumnID.</span><span class="sxs-lookup"><span data-stu-id="3e22a-118">The columnid to retrieve.</span></span>

#### <a name="return-value"></a><span data-ttu-id="3e22a-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3e22a-119">Return value</span></span>

<span data-ttu-id="3e22a-120">Typ: [System. Nullable](/dotnet/api/system.nullable-1)\<[Int32](/dotnet/api/system.int32)\></span><span class="sxs-lookup"><span data-stu-id="3e22a-120">Type: [System.Nullable](/dotnet/api/system.nullable-1)\<[Int32](/dotnet/api/system.int32)\></span></span>  
<span data-ttu-id="3e22a-121">Die Daten, die aus der Spalte als int abgerufen werden. NULL, wenn die Spalte NULL ist.</span><span class="sxs-lookup"><span data-stu-id="3e22a-121">The data retrieved from the column as an int. Null if the column is null.</span></span>  

## <a name="see-also"></a><span data-ttu-id="3e22a-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3e22a-122">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="3e22a-123">Referenz</span><span class="sxs-lookup"><span data-stu-id="3e22a-123">Reference</span></span>

[<span data-ttu-id="3e22a-124">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="3e22a-124">Api class</span></span>](./api-class.md)

[<span data-ttu-id="3e22a-125">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="3e22a-125">Api members</span></span>](./api-members.md)

[<span data-ttu-id="3e22a-126">RetrieveColumnAsInt32-Überladung</span><span class="sxs-lookup"><span data-stu-id="3e22a-126">RetrieveColumnAsInt32 overload</span></span>](./api.retrievecolumnasint32-method.md)

[<span data-ttu-id="3e22a-127">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="3e22a-127">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
