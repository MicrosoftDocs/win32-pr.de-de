---
description: 'Weitere Informationen finden Sie unter: API. retrievecolumschlag-Methode (JET_SESID, JET_TABLEID, JET_COLUMNID)'
title: API. retrievecolumschlag-Methode (JET_SESID, JET_TABLEID, JET_COLUMNID)
TOCTitle: RetrieveColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.RetrieveColumn(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievecolumn(v=EXCHG.10)
ms:contentKeyID: 55100833
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.RetrieveColumn
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2c29a591064c573e168903aaf83dcdd15f5b9a5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366316"
---
# <a name="apiretrievecolumn-method-jet_sesid-jet_tableid-jet_columnid"></a><span data-ttu-id="6ea94-103">API. retrievecolumschlag-Methode (JET_SESID, JET_TABLEID, JET_COLUMNID)</span><span class="sxs-lookup"><span data-stu-id="6ea94-103">Api.RetrieveColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID)</span></span>

<span data-ttu-id="6ea94-104">Ruft einen einzelnen Spaltenwert aus dem aktuellen Datensatz ab.</span><span class="sxs-lookup"><span data-stu-id="6ea94-104">Retrieves a single column value from the current record.</span></span> <span data-ttu-id="6ea94-105">Der Datensatz ist der Datensatz, der mit dem Index Eintrag an der aktuellen Position des Cursors verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="6ea94-105">The record is that record associated with the index entry at the current position of the cursor.</span></span>

<span data-ttu-id="6ea94-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="6ea94-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="6ea94-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="6ea94-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="6ea94-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="6ea94-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function RetrieveColumn ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID _
) As Byte()
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim returnValue As Byte()

returnValue = Api.RetrieveColumn(sesid, _
    tableid, columnid)
```

``` csharp
public static byte[] RetrieveColumn(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid
)
```

#### <a name="parameters"></a><span data-ttu-id="6ea94-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="6ea94-109">Parameters</span></span>

  - <span data-ttu-id="6ea94-110">-sid</span><span class="sxs-lookup"><span data-stu-id="6ea94-110">sesid</span></span>  
    <span data-ttu-id="6ea94-111">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="6ea94-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="6ea94-112">Die zu verwendende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="6ea94-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="6ea94-113">TableID</span><span class="sxs-lookup"><span data-stu-id="6ea94-113">tableid</span></span>  
    <span data-ttu-id="6ea94-114">Typ: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="6ea94-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="6ea94-115">Der Cursor, von dem die Spalte abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="6ea94-115">The cursor to retrieve the column from.</span></span>

<!-- end list -->

  - <span data-ttu-id="6ea94-116">columnid</span><span class="sxs-lookup"><span data-stu-id="6ea94-116">columnid</span></span>  
    <span data-ttu-id="6ea94-117">Typ: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="6ea94-117">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="6ea94-118">Das abzurufende ColumnID.</span><span class="sxs-lookup"><span data-stu-id="6ea94-118">The columnid to retrieve.</span></span>

#### <a name="return-value"></a><span data-ttu-id="6ea94-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6ea94-119">Return value</span></span>

<span data-ttu-id="6ea94-120">Sorte \[\]</span><span class="sxs-lookup"><span data-stu-id="6ea94-120">Type: \[\]</span></span>  
<span data-ttu-id="6ea94-121">Die Daten, die aus der Spalte abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="6ea94-121">The data retrieved from the column.</span></span> <span data-ttu-id="6ea94-122">NULL, wenn die Spalte NULL ist.</span><span class="sxs-lookup"><span data-stu-id="6ea94-122">Null if the column is null.</span></span>  

## <a name="see-also"></a><span data-ttu-id="6ea94-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6ea94-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="6ea94-124">Referenz</span><span class="sxs-lookup"><span data-stu-id="6ea94-124">Reference</span></span>

[<span data-ttu-id="6ea94-125">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="6ea94-125">Api class</span></span>](./api-class.md)

[<span data-ttu-id="6ea94-126">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="6ea94-126">Api members</span></span>](./api-members.md)

[<span data-ttu-id="6ea94-127">Retrievecolübern-Überladung</span><span class="sxs-lookup"><span data-stu-id="6ea94-127">RetrieveColumn overload</span></span>](./api.retrievecolumn-method.md)

[<span data-ttu-id="6ea94-128">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="6ea94-128">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
