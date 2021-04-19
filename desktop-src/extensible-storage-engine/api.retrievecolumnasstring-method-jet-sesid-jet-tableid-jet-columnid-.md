---
description: 'Weitere Informationen finden Sie unter: API. retrievecolennasstring-Methode (JET_SESID, JET_TABLEID, JET_COLUMNID)'
title: API. retrievecolennasstring-Methode (JET_SESID, JET_TABLEID, JET_COLUMNID)
TOCTitle: RetrieveColumnAsString method (JET_SESID, JET_TABLEID, JET_COLUMNID)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsString(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievecolumnasstring(v=EXCHG.10)
ms:contentKeyID: 55100860
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsString
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 64500e9827d55fab4771963b95dbfd0efffdc5c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350097"
---
# <a name="apiretrievecolumnasstring-method-jet_sesid-jet_tableid-jet_columnid"></a><span data-ttu-id="6020f-103">API. retrievecolennasstring-Methode (JET_SESID, JET_TABLEID, JET_COLUMNID)</span><span class="sxs-lookup"><span data-stu-id="6020f-103">Api.RetrieveColumnAsString method (JET_SESID, JET_TABLEID, JET_COLUMNID)</span></span>

<span data-ttu-id="6020f-104">Ruft einen einzelnen Spaltenwert aus dem aktuellen Datensatz ab.</span><span class="sxs-lookup"><span data-stu-id="6020f-104">Retrieves a single column value from the current record.</span></span> <span data-ttu-id="6020f-105">Der Datensatz ist der Datensatz, der mit dem Index Eintrag an der aktuellen Position des Cursors verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="6020f-105">The record is that record associated with the index entry at the current position of the cursor.</span></span> <span data-ttu-id="6020f-106">Die Unicode-Codierung wird verwendet.</span><span class="sxs-lookup"><span data-stu-id="6020f-106">The Unicode encoding is used.</span></span>

<span data-ttu-id="6020f-107">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="6020f-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="6020f-108">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="6020f-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="6020f-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="6020f-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Function RetrieveColumnAsString ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID _
) As String
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim returnValue As String

returnValue = Api.RetrieveColumnAsString(sesid, _
    tableid, columnid)
```

``` csharp
public static string RetrieveColumnAsString(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid
)
```

#### <a name="parameters"></a><span data-ttu-id="6020f-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="6020f-110">Parameters</span></span>

  - <span data-ttu-id="6020f-111">-sid</span><span class="sxs-lookup"><span data-stu-id="6020f-111">sesid</span></span>  
    <span data-ttu-id="6020f-112">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="6020f-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="6020f-113">Die zu verwendende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="6020f-113">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="6020f-114">TableID</span><span class="sxs-lookup"><span data-stu-id="6020f-114">tableid</span></span>  
    <span data-ttu-id="6020f-115">Typ: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="6020f-115">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="6020f-116">Der Cursor, von dem die Spalte abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="6020f-116">The cursor to retrieve the column from.</span></span>

<!-- end list -->

  - <span data-ttu-id="6020f-117">columnid</span><span class="sxs-lookup"><span data-stu-id="6020f-117">columnid</span></span>  
    <span data-ttu-id="6020f-118">Typ: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="6020f-118">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="6020f-119">Das abzurufende ColumnID.</span><span class="sxs-lookup"><span data-stu-id="6020f-119">The columnid to retrieve.</span></span>

#### <a name="return-value"></a><span data-ttu-id="6020f-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6020f-120">Return value</span></span>

<span data-ttu-id="6020f-121">Typ: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="6020f-121">Type: [System.String](/dotnet/api/system.string)</span></span>  
<span data-ttu-id="6020f-122">Die aus der Spalte abgerufenen Daten als Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="6020f-122">The data retrieved from the column as a string.</span></span> <span data-ttu-id="6020f-123">NULL, wenn die Spalte NULL ist.</span><span class="sxs-lookup"><span data-stu-id="6020f-123">Null if the column is null.</span></span>  

## <a name="see-also"></a><span data-ttu-id="6020f-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6020f-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="6020f-125">Referenz</span><span class="sxs-lookup"><span data-stu-id="6020f-125">Reference</span></span>

[<span data-ttu-id="6020f-126">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="6020f-126">Api class</span></span>](./api-class.md)

[<span data-ttu-id="6020f-127">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="6020f-127">Api members</span></span>](./api-members.md)

[<span data-ttu-id="6020f-128">Retrievecolübernasstring-Überladung</span><span class="sxs-lookup"><span data-stu-id="6020f-128">RetrieveColumnAsString overload</span></span>](./api.retrievecolumnasstring-method.md)

[<span data-ttu-id="6020f-129">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="6020f-129">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
