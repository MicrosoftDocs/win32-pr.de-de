---
description: 'Weitere Informationen finden Sie unter: API. retrievecolaufnasfloat-Methode (JET_SESID, JET_TABLEID, JET_COLUMNID)'
title: API. retrievecolaufnasfloat-Methode (JET_SESID, JET_TABLEID, JET_COLUMNID)
TOCTitle: RetrieveColumnAsFloat method (JET_SESID, JET_TABLEID, JET_COLUMNID)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsFloat(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievecolumnasfloat(v=EXCHG.10)
ms:contentKeyID: 55100846
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsFloat
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9022c53d384b6d92911a02797a684d11077987d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484174"
---
# <a name="apiretrievecolumnasfloat-method-jet_sesid-jet_tableid-jet_columnid"></a><span data-ttu-id="6e8eb-103">API. retrievecolaufnasfloat-Methode (JET_SESID, JET_TABLEID, JET_COLUMNID)</span><span class="sxs-lookup"><span data-stu-id="6e8eb-103">Api.RetrieveColumnAsFloat method (JET_SESID, JET_TABLEID, JET_COLUMNID)</span></span>

<span data-ttu-id="6e8eb-104">Ruft einen float-Spaltenwert aus dem aktuellen Datensatz ab.</span><span class="sxs-lookup"><span data-stu-id="6e8eb-104">Retrieves a float column value from the current record.</span></span> <span data-ttu-id="6e8eb-105">Der Datensatz ist der Datensatz, der mit dem Index Eintrag an der aktuellen Position des Cursors verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="6e8eb-105">The record is that record associated with the index entry at the current position of the cursor.</span></span>

<span data-ttu-id="6e8eb-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="6e8eb-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="6e8eb-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="6e8eb-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="6e8eb-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="6e8eb-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function RetrieveColumnAsFloat ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID _
) As Nullable(Of Single)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim returnValue As Nullable(Of Single)

returnValue = Api.RetrieveColumnAsFloat(sesid, _
    tableid, columnid)
```

``` csharp
public static Nullable<float> RetrieveColumnAsFloat(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid
)
```

#### <a name="parameters"></a><span data-ttu-id="6e8eb-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="6e8eb-109">Parameters</span></span>

  - <span data-ttu-id="6e8eb-110">-sid</span><span class="sxs-lookup"><span data-stu-id="6e8eb-110">sesid</span></span>  
    <span data-ttu-id="6e8eb-111">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="6e8eb-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="6e8eb-112">Die zu verwendende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="6e8eb-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="6e8eb-113">TableID</span><span class="sxs-lookup"><span data-stu-id="6e8eb-113">tableid</span></span>  
    <span data-ttu-id="6e8eb-114">Typ: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="6e8eb-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="6e8eb-115">Der Cursor, von dem die Spalte abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="6e8eb-115">The cursor to retrieve the column from.</span></span>

<!-- end list -->

  - <span data-ttu-id="6e8eb-116">columnid</span><span class="sxs-lookup"><span data-stu-id="6e8eb-116">columnid</span></span>  
    <span data-ttu-id="6e8eb-117">Typ: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="6e8eb-117">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="6e8eb-118">Das abzurufende ColumnID.</span><span class="sxs-lookup"><span data-stu-id="6e8eb-118">The columnid to retrieve.</span></span>

#### <a name="return-value"></a><span data-ttu-id="6e8eb-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6e8eb-119">Return value</span></span>

<span data-ttu-id="6e8eb-120">Typ: [System. Nullable](/dotnet/api/system.nullable-1)\<[Single](/dotnet/api/system.single)\></span><span class="sxs-lookup"><span data-stu-id="6e8eb-120">Type: [System.Nullable](/dotnet/api/system.nullable-1)\<[Single](/dotnet/api/system.single)\></span></span>  
<span data-ttu-id="6e8eb-121">Die Daten, die aus der Spalte als float abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="6e8eb-121">The data retrieved from the column as a float.</span></span> <span data-ttu-id="6e8eb-122">NULL, wenn die Spalte NULL ist.</span><span class="sxs-lookup"><span data-stu-id="6e8eb-122">Null if the column is null.</span></span>  

## <a name="see-also"></a><span data-ttu-id="6e8eb-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6e8eb-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="6e8eb-124">Referenz</span><span class="sxs-lookup"><span data-stu-id="6e8eb-124">Reference</span></span>

[<span data-ttu-id="6e8eb-125">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="6e8eb-125">Api class</span></span>](./api-class.md)

[<span data-ttu-id="6e8eb-126">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="6e8eb-126">Api members</span></span>](./api-members.md)

[<span data-ttu-id="6e8eb-127">Retrievecolübernasfloat-Überladung</span><span class="sxs-lookup"><span data-stu-id="6e8eb-127">RetrieveColumnAsFloat overload</span></span>](./api.retrievecolumnasfloat-method.md)

[<span data-ttu-id="6e8eb-128">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="6e8eb-128">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
