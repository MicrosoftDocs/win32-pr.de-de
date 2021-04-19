---
description: 'Weitere Informationen finden Sie unter: API. retrievecolaufnasdouble-Methode (JET_SESID, JET_TABLEID, JET_COLUMNID)'
title: API. retrievecolaufnasdouble-Methode (JET_SESID, JET_TABLEID, JET_COLUMNID)
TOCTitle: RetrieveColumnAsDouble method (JET_SESID, JET_TABLEID, JET_COLUMNID)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsDouble(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievecolumnasdouble(v=EXCHG.10)
ms:contentKeyID: 55100847
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsDouble
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a9bf86595870b03447dd8a859ac66f0aa0c5f9a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349938"
---
# <a name="apiretrievecolumnasdouble-method-jet_sesid-jet_tableid-jet_columnid"></a><span data-ttu-id="6425c-103">API. retrievecolaufnasdouble-Methode (JET_SESID, JET_TABLEID, JET_COLUMNID)</span><span class="sxs-lookup"><span data-stu-id="6425c-103">Api.RetrieveColumnAsDouble method (JET_SESID, JET_TABLEID, JET_COLUMNID)</span></span>

<span data-ttu-id="6425c-104">Ruft einen Double-Spaltenwert aus dem aktuellen Datensatz ab.</span><span class="sxs-lookup"><span data-stu-id="6425c-104">Retrieves a double column value from the current record.</span></span> <span data-ttu-id="6425c-105">Der Datensatz ist der Datensatz, der mit dem Index Eintrag an der aktuellen Position des Cursors verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="6425c-105">The record is that record associated with the index entry at the current position of the cursor.</span></span>

<span data-ttu-id="6425c-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="6425c-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="6425c-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="6425c-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="6425c-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="6425c-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function RetrieveColumnAsDouble ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID _
) As Nullable(Of Double)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim returnValue As Nullable(Of Double)

returnValue = Api.RetrieveColumnAsDouble(sesid, _
    tableid, columnid)
```

``` csharp
public static Nullable<double> RetrieveColumnAsDouble(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid
)
```

#### <a name="parameters"></a><span data-ttu-id="6425c-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="6425c-109">Parameters</span></span>

  - <span data-ttu-id="6425c-110">-sid</span><span class="sxs-lookup"><span data-stu-id="6425c-110">sesid</span></span>  
    <span data-ttu-id="6425c-111">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="6425c-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="6425c-112">Die zu verwendende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="6425c-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="6425c-113">TableID</span><span class="sxs-lookup"><span data-stu-id="6425c-113">tableid</span></span>  
    <span data-ttu-id="6425c-114">Typ: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="6425c-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="6425c-115">Der Cursor, von dem die Spalte abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="6425c-115">The cursor to retrieve the column from.</span></span>

<!-- end list -->

  - <span data-ttu-id="6425c-116">columnid</span><span class="sxs-lookup"><span data-stu-id="6425c-116">columnid</span></span>  
    <span data-ttu-id="6425c-117">Typ: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="6425c-117">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="6425c-118">Das abzurufende ColumnID.</span><span class="sxs-lookup"><span data-stu-id="6425c-118">The columnid to retrieve.</span></span>

#### <a name="return-value"></a><span data-ttu-id="6425c-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6425c-119">Return value</span></span>

<span data-ttu-id="6425c-120">Typ: [System. Nullable](/dotnet/api/system.nullable-1)\<[Double](/dotnet/api/system.double)\></span><span class="sxs-lookup"><span data-stu-id="6425c-120">Type: [System.Nullable](/dotnet/api/system.nullable-1)\<[Double](/dotnet/api/system.double)\></span></span>  
<span data-ttu-id="6425c-121">Die aus der Spalte abgerufenen Daten als Double-Wert.</span><span class="sxs-lookup"><span data-stu-id="6425c-121">The data retrieved from the column as a double.</span></span> <span data-ttu-id="6425c-122">NULL, wenn die Spalte NULL ist.</span><span class="sxs-lookup"><span data-stu-id="6425c-122">Null if the column is null.</span></span>  

## <a name="see-also"></a><span data-ttu-id="6425c-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6425c-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="6425c-124">Referenz</span><span class="sxs-lookup"><span data-stu-id="6425c-124">Reference</span></span>

[<span data-ttu-id="6425c-125">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="6425c-125">Api class</span></span>](./api-class.md)

[<span data-ttu-id="6425c-126">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="6425c-126">Api members</span></span>](./api-members.md)

[<span data-ttu-id="6425c-127">Retrievecolübernasdouble-Überladung</span><span class="sxs-lookup"><span data-stu-id="6425c-127">RetrieveColumnAsDouble overload</span></span>](./api.retrievecolumnasdouble-method.md)

[<span data-ttu-id="6425c-128">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="6425c-128">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
