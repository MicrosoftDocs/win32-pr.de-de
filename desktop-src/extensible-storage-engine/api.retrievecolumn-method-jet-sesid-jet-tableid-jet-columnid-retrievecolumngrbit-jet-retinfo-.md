---
description: 'Weitere Informationen finden Sie unter: API. retrievecolenn-Methode (JET_SESID, JET_TABLEID, JET_COLUMNID, retrievecolenngrbit, JET_RETINFO)'
title: API. retrievecolenn-Methode (JET_SESID, JET_TABLEID, JET_COLUMNID, retrievecolenngrbit, JET_RETINFO)
TOCTitle: RetrieveColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit, JET_RETINFO)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.RetrieveColumn(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit,Microsoft.Isam.Esent.Interop.JET_RETINFO)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievecolumn(v=EXCHG.10)
ms:contentKeyID: 55100853
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.RetrieveColumn
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 43657ec60e521795ba4d474306de9380618cd21f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346472"
---
# <a name="apiretrievecolumn-method-jet_sesid-jet_tableid-jet_columnid-retrievecolumngrbit-jet_retinfo"></a><span data-ttu-id="e2bab-103">API. retrievecolenn-Methode (JET_SESID, JET_TABLEID, JET_COLUMNID, retrievecolenngrbit, JET_RETINFO)</span><span class="sxs-lookup"><span data-stu-id="e2bab-103">Api.RetrieveColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit, JET_RETINFO)</span></span>

<span data-ttu-id="e2bab-104">Ruft einen einzelnen Spaltenwert aus dem aktuellen Datensatz ab.</span><span class="sxs-lookup"><span data-stu-id="e2bab-104">Retrieves a single column value from the current record.</span></span> <span data-ttu-id="e2bab-105">Der Datensatz ist der Datensatz, der mit dem Index Eintrag an der aktuellen Position des Cursors verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="e2bab-105">The record is that record associated with the index entry at the current position of the cursor.</span></span> <span data-ttu-id="e2bab-106">Alternativ kann diese Funktion eine Spalte aus einem Datensatz abrufen, der im Cursor Kopier Puffer erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="e2bab-106">Alternatively, this function can retrieve a column from a record being created in the cursor copy buffer.</span></span> <span data-ttu-id="e2bab-107">Diese Funktion kann auch Spaltendaten aus einem Index Eintrag abrufen, der auf den aktuellen Datensatz verweist.</span><span class="sxs-lookup"><span data-stu-id="e2bab-107">This function can also retrieve column data from an index entry that references the current record.</span></span> <span data-ttu-id="e2bab-108">Zusätzlich zum Abrufen des tatsächlichen Spaltenwerts kann jetretrievecolumschlag auch verwendet werden, um die Größe einer Spalte abzurufen, bevor die Spaltendaten selbst abgerufen werden, sodass die Größe der Anwendungs Puffer entsprechend angepasst werden kann.</span><span class="sxs-lookup"><span data-stu-id="e2bab-108">In addition to retrieving the actual column value, JetRetrieveColumn can also be used to retrieve the size of a column, before retrieving the column data itself so that application buffers can be sized appropriately.</span></span>

<span data-ttu-id="e2bab-109">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e2bab-109">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="e2bab-110">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="e2bab-110">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e2bab-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="e2bab-111">Syntax</span></span>

``` vb
'Declaration
Public Shared Function RetrieveColumn ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    grbit As RetrieveColumnGrbit, _
    retinfo As JET_RETINFO _
) As Byte()
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim grbit As RetrieveColumnGrbit
Dim retinfo As JET_RETINFO
Dim returnValue As Byte()

returnValue = Api.RetrieveColumn(sesid, _
    tableid, columnid, grbit, retinfo)
```

``` csharp
public static byte[] RetrieveColumn(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    RetrieveColumnGrbit grbit,
    JET_RETINFO retinfo
)
```

#### <a name="parameters"></a><span data-ttu-id="e2bab-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="e2bab-112">Parameters</span></span>

  - <span data-ttu-id="e2bab-113">-sid</span><span class="sxs-lookup"><span data-stu-id="e2bab-113">sesid</span></span>  
    <span data-ttu-id="e2bab-114">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="e2bab-114">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="e2bab-115">Die zu verwendende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="e2bab-115">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="e2bab-116">TableID</span><span class="sxs-lookup"><span data-stu-id="e2bab-116">tableid</span></span>  
    <span data-ttu-id="e2bab-117">Typ: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="e2bab-117">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="e2bab-118">Der Cursor, von dem die Spalte abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="e2bab-118">The cursor to retrieve the column from.</span></span>

<!-- end list -->

  - <span data-ttu-id="e2bab-119">columnid</span><span class="sxs-lookup"><span data-stu-id="e2bab-119">columnid</span></span>  
    <span data-ttu-id="e2bab-120">Typ: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="e2bab-120">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="e2bab-121">Das abzurufende ColumnID.</span><span class="sxs-lookup"><span data-stu-id="e2bab-121">The columnid to retrieve.</span></span>

<!-- end list -->

  - <span data-ttu-id="e2bab-122">grbit</span><span class="sxs-lookup"><span data-stu-id="e2bab-122">grbit</span></span>  
    <span data-ttu-id="e2bab-123">Typ: [Microsoft. ISAM. ESENT. Interop. retrievecolenngrbit](./retrievecolumngrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="e2bab-123">Type: [Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit](./retrievecolumngrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="e2bab-124">Abrufen von Spalten Optionen.</span><span class="sxs-lookup"><span data-stu-id="e2bab-124">Retrieve column options.</span></span>

<!-- end list -->

  - <span data-ttu-id="e2bab-125">retinfo</span><span class="sxs-lookup"><span data-stu-id="e2bab-125">retinfo</span></span>  
    <span data-ttu-id="e2bab-126">Typ: [Microsoft.ISAM.ESENT.Interop.JET_RETINFO](./jet-retinfo-class.md)</span><span class="sxs-lookup"><span data-stu-id="e2bab-126">Type: [Microsoft.Isam.Esent.Interop.JET_RETINFO](./jet-retinfo-class.md)</span></span>  
    
    <span data-ttu-id="e2bab-127">Wenn pretinfo als NULL angegeben wird, verhält sich die Funktion so, als ob eine itagsequence von 1 und ein iblongvalue-Wert von 0 (null) angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="e2bab-127">If pretinfo is give as NULL then the function behaves as though an itagSequence of 1 and an ibLongValue of 0 (zero) were given.</span></span> <span data-ttu-id="e2bab-128">Dies bewirkt, dass der Spalten Abruf den ersten Wert einer mehrwertigen Spalte abruft und lange Daten bei Offset 0 (null) abruft.</span><span class="sxs-lookup"><span data-stu-id="e2bab-128">This causes column retrieval to retrieve the first value of a multi-valued column, and to retrieve long data at offset 0 (zero).</span></span>

#### <a name="return-value"></a><span data-ttu-id="e2bab-129">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e2bab-129">Return value</span></span>

<span data-ttu-id="e2bab-130">Sorte \[\]</span><span class="sxs-lookup"><span data-stu-id="e2bab-130">Type: \[\]</span></span>  
<span data-ttu-id="e2bab-131">Die Daten, die aus der Spalte abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="e2bab-131">The data retrieved from the column.</span></span> <span data-ttu-id="e2bab-132">NULL, wenn die Spalte NULL ist.</span><span class="sxs-lookup"><span data-stu-id="e2bab-132">Null if the column is null.</span></span>  

## <a name="see-also"></a><span data-ttu-id="e2bab-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e2bab-133">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e2bab-134">Referenz</span><span class="sxs-lookup"><span data-stu-id="e2bab-134">Reference</span></span>

[<span data-ttu-id="e2bab-135">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="e2bab-135">Api class</span></span>](./api-class.md)

[<span data-ttu-id="e2bab-136">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="e2bab-136">Api members</span></span>](./api-members.md)

[<span data-ttu-id="e2bab-137">Retrievecolübern-Überladung</span><span class="sxs-lookup"><span data-stu-id="e2bab-137">RetrieveColumn overload</span></span>](./api.retrievecolumn-method.md)

[<span data-ttu-id="e2bab-138">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="e2bab-138">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
