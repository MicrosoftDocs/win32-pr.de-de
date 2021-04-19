---
description: 'Weitere Informationen finden Sie unter: API. retrievecolaufnasguid-Methode (JET_SESID, JET_TABLEID, JET_COLUMNID)'
title: API. retrievecolaufnasguid-Methode (JET_SESID, JET_TABLEID, JET_COLUMNID)
TOCTitle: RetrieveColumnAsGuid method (JET_SESID, JET_TABLEID, JET_COLUMNID)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsGuid(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievecolumnasguid(v=EXCHG.10)
ms:contentKeyID: 55100876
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsGuid
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a496d5f0ce45a1f2f8d43072ac5d311e7e7a9c29
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360802"
---
# <a name="apiretrievecolumnasguid-method-jet_sesid-jet_tableid-jet_columnid"></a><span data-ttu-id="b6b73-103">API. retrievecolaufnasguid-Methode (JET_SESID, JET_TABLEID, JET_COLUMNID)</span><span class="sxs-lookup"><span data-stu-id="b6b73-103">Api.RetrieveColumnAsGuid method (JET_SESID, JET_TABLEID, JET_COLUMNID)</span></span>

<span data-ttu-id="b6b73-104">Ruft einen GUID-Spaltenwert aus dem aktuellen Datensatz ab.</span><span class="sxs-lookup"><span data-stu-id="b6b73-104">Retrieves a guid column value from the current record.</span></span> <span data-ttu-id="b6b73-105">Der Datensatz ist der Datensatz, der mit dem Index Eintrag an der aktuellen Position des Cursors verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="b6b73-105">The record is that record associated with the index entry at the current position of the cursor.</span></span>

<span data-ttu-id="b6b73-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b6b73-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="b6b73-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="b6b73-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b6b73-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="b6b73-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function RetrieveColumnAsGuid ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID _
) As Nullable(Of Guid)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim returnValue As Nullable(Of Guid)

returnValue = Api.RetrieveColumnAsGuid(sesid, _
    tableid, columnid)
```

``` csharp
public static Nullable<Guid> RetrieveColumnAsGuid(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid
)
```

#### <a name="parameters"></a><span data-ttu-id="b6b73-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="b6b73-109">Parameters</span></span>

  - <span data-ttu-id="b6b73-110">-sid</span><span class="sxs-lookup"><span data-stu-id="b6b73-110">sesid</span></span>  
    <span data-ttu-id="b6b73-111">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="b6b73-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="b6b73-112">Die zu verwendende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="b6b73-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="b6b73-113">TableID</span><span class="sxs-lookup"><span data-stu-id="b6b73-113">tableid</span></span>  
    <span data-ttu-id="b6b73-114">Typ: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="b6b73-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="b6b73-115">Der Cursor, von dem die Spalte abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="b6b73-115">The cursor to retrieve the column from.</span></span>

<!-- end list -->

  - <span data-ttu-id="b6b73-116">columnid</span><span class="sxs-lookup"><span data-stu-id="b6b73-116">columnid</span></span>  
    <span data-ttu-id="b6b73-117">Typ: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="b6b73-117">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="b6b73-118">Das abzurufende ColumnID.</span><span class="sxs-lookup"><span data-stu-id="b6b73-118">The columnid to retrieve.</span></span>

#### <a name="return-value"></a><span data-ttu-id="b6b73-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b6b73-119">Return value</span></span>

<span data-ttu-id="b6b73-120">Typ: [System. Nullable](/dotnet/api/system.nullable-1)\<[Guid](/dotnet/api/system.guid)\></span><span class="sxs-lookup"><span data-stu-id="b6b73-120">Type: [System.Nullable](/dotnet/api/system.nullable-1)\<[Guid](/dotnet/api/system.guid)\></span></span>  
<span data-ttu-id="b6b73-121">Die aus der Spalte abgerufenen Daten als GUID.</span><span class="sxs-lookup"><span data-stu-id="b6b73-121">The data retrieved from the column as a guid.</span></span> <span data-ttu-id="b6b73-122">NULL, wenn die Spalte NULL ist.</span><span class="sxs-lookup"><span data-stu-id="b6b73-122">Null if the column is null.</span></span>  

## <a name="see-also"></a><span data-ttu-id="b6b73-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b6b73-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b6b73-124">Referenz</span><span class="sxs-lookup"><span data-stu-id="b6b73-124">Reference</span></span>

[<span data-ttu-id="b6b73-125">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="b6b73-125">Api class</span></span>](./api-class.md)

[<span data-ttu-id="b6b73-126">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="b6b73-126">Api members</span></span>](./api-members.md)

[<span data-ttu-id="b6b73-127">Retrievecolübernasguid-Überladung</span><span class="sxs-lookup"><span data-stu-id="b6b73-127">RetrieveColumnAsGuid overload</span></span>](./api.retrievecolumnasguid-method.md)

[<span data-ttu-id="b6b73-128">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="b6b73-128">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
