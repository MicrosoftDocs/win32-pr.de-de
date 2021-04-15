---
description: 'Weitere Informationen finden Sie unter: API. jetretrievecolumschlag-Methode (JET_SESID, JET_TABLEID, JET_COLUMNID, Byte, Int32, Int32, Int32, retrievecolumgengrbit, JET_RETINFO)'
title: API. jetretrievecolumschlag-Methode (JET_SESID, JET_TABLEID, JET_COLUMNID, Byte, Int32, Int32, Int32, retrievecolumgengrbit, JET_RETINFO)
TOCTitle: JetRetrieveColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, Byte , Int32, Int32, Int32, RetrieveColumnGrbit, JET_RETINFO)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetRetrieveColumn(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,System.Byte[],System.Int32,System.Int32,System.Int32@,Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit,Microsoft.Isam.Esent.Interop.JET_RETINFO)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetretrievecolumn(v=EXCHG.10)
ms:contentKeyID: 55100792
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetRetrieveColumn
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 832e6d6cc123e4a85a2cacb2df688348732fcc0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349599"
---
# <a name="apijetretrievecolumn-method-jet_sesid-jet_tableid-jet_columnid-byte--int32-int32-int32-retrievecolumngrbit-jet_retinfo"></a><span data-ttu-id="e8aae-103">API. jetretrievecolumschlag-Methode (JET_SESID, JET_TABLEID, JET_COLUMNID, Byte, Int32, Int32, Int32, retrievecolumgengrbit, JET_RETINFO)</span><span class="sxs-lookup"><span data-stu-id="e8aae-103">Api.JetRetrieveColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, Byte , Int32, Int32, Int32, RetrieveColumnGrbit, JET_RETINFO)</span></span>

<span data-ttu-id="e8aae-104">Ruft einen einzelnen Spaltenwert aus dem aktuellen Datensatz ab.</span><span class="sxs-lookup"><span data-stu-id="e8aae-104">Retrieves a single column value from the current record.</span></span> <span data-ttu-id="e8aae-105">Der Datensatz ist der Datensatz, der mit dem Index Eintrag an der aktuellen Position des Cursors verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="e8aae-105">The record is that record associated with the index entry at the current position of the cursor.</span></span> <span data-ttu-id="e8aae-106">Alternativ kann diese Funktion eine Spalte aus einem Datensatz abrufen, der im Cursor Kopier Puffer erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="e8aae-106">Alternatively, this function can retrieve a column from a record being created in the cursor copy buffer.</span></span> <span data-ttu-id="e8aae-107">Diese Funktion kann auch Spaltendaten aus einem Index Eintrag abrufen, der auf den aktuellen Datensatz verweist.</span><span class="sxs-lookup"><span data-stu-id="e8aae-107">This function can also retrieve column data from an index entry that references the current record.</span></span> <span data-ttu-id="e8aae-108">Zusätzlich zum Abrufen des tatsächlichen Spaltenwerts kann jetretrievecolumschlag auch verwendet werden, um die Größe einer Spalte abzurufen, bevor die Spaltendaten selbst abgerufen werden, sodass die Größe der Anwendungs Puffer entsprechend angepasst werden kann.</span><span class="sxs-lookup"><span data-stu-id="e8aae-108">In addition to retrieving the actual column value, JetRetrieveColumn can also be used to retrieve the size of a column, before retrieving the column data itself so that application buffers can be sized appropriately.</span></span>

<span data-ttu-id="e8aae-109">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e8aae-109">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="e8aae-110">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="e8aae-110">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e8aae-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="e8aae-111">Syntax</span></span>

``` vb
'Declaration
Public Shared Function JetRetrieveColumn ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    data As Byte(), _
    dataSize As Integer, _
    dataOffset As Integer, _
    <OutAttribute> ByRef actualDataSize As Integer, _
    grbit As RetrieveColumnGrbit, _
    retinfo As JET_RETINFO _
) As JET_wrn
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim data As Byte()
Dim dataSize As Integer
Dim dataOffset As Integer
Dim actualDataSize As Integer
Dim grbit As RetrieveColumnGrbit
Dim retinfo As JET_RETINFO
Dim returnValue As JET_wrn

returnValue = Api.JetRetrieveColumn(sesid, _
    tableid, columnid, data, dataSize, _
    dataOffset, actualDataSize, grbit, _
    retinfo)
```

``` csharp
public static JET_wrn JetRetrieveColumn(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    byte[] data,
    int dataSize,
    int dataOffset,
    out int actualDataSize,
    RetrieveColumnGrbit grbit,
    JET_RETINFO retinfo
)
```

#### <a name="parameters"></a><span data-ttu-id="e8aae-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="e8aae-112">Parameters</span></span>

  - <span data-ttu-id="e8aae-113">-sid</span><span class="sxs-lookup"><span data-stu-id="e8aae-113">sesid</span></span>  
    <span data-ttu-id="e8aae-114">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="e8aae-114">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="e8aae-115">Die zu verwendende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="e8aae-115">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="e8aae-116">TableID</span><span class="sxs-lookup"><span data-stu-id="e8aae-116">tableid</span></span>  
    <span data-ttu-id="e8aae-117">Typ: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="e8aae-117">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="e8aae-118">Der Cursor, von dem die Spalte abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="e8aae-118">The cursor to retrieve the column from.</span></span>

<!-- end list -->

  - <span data-ttu-id="e8aae-119">columnid</span><span class="sxs-lookup"><span data-stu-id="e8aae-119">columnid</span></span>  
    <span data-ttu-id="e8aae-120">Typ: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="e8aae-120">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="e8aae-121">Das abzurufende ColumnID.</span><span class="sxs-lookup"><span data-stu-id="e8aae-121">The columnid to retrieve.</span></span>

<!-- end list -->

  - <span data-ttu-id="e8aae-122">Daten</span><span class="sxs-lookup"><span data-stu-id="e8aae-122">data</span></span>  
    <span data-ttu-id="e8aae-123">Sorte \[\]</span><span class="sxs-lookup"><span data-stu-id="e8aae-123">Type: \[\]</span></span>  
    
    <span data-ttu-id="e8aae-124">Der Datenpuffer, in den der abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="e8aae-124">The data buffer to be retrieved into.</span></span>

<!-- end list -->

  - <span data-ttu-id="e8aae-125">dataSize</span><span class="sxs-lookup"><span data-stu-id="e8aae-125">dataSize</span></span>  
    <span data-ttu-id="e8aae-126">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="e8aae-126">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="e8aae-127">Die Größe des Daten Puffers.</span><span class="sxs-lookup"><span data-stu-id="e8aae-127">The size of the data buffer.</span></span>

<!-- end list -->

  - <span data-ttu-id="e8aae-128">dataOffset</span><span class="sxs-lookup"><span data-stu-id="e8aae-128">dataOffset</span></span>  
    <span data-ttu-id="e8aae-129">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="e8aae-129">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="e8aae-130">Offset im Datenpuffer, in den Daten gelesen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e8aae-130">Offset into the data buffer to read data into.</span></span>

<!-- end list -->

  - <span data-ttu-id="e8aae-131">actualdatasize</span><span class="sxs-lookup"><span data-stu-id="e8aae-131">actualDataSize</span></span>  
    <span data-ttu-id="e8aae-132">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="e8aae-132">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="e8aae-133">Gibt die tatsächliche Größe des Daten Puffers zurück.</span><span class="sxs-lookup"><span data-stu-id="e8aae-133">Returns the actual size of the data buffer.</span></span>

<!-- end list -->

  - <span data-ttu-id="e8aae-134">grbit</span><span class="sxs-lookup"><span data-stu-id="e8aae-134">grbit</span></span>  
    <span data-ttu-id="e8aae-135">Typ: [Microsoft. ISAM. ESENT. Interop. retrievecolenngrbit](./retrievecolumngrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="e8aae-135">Type: [Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit](./retrievecolumngrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="e8aae-136">Abrufen von Spalten Optionen.</span><span class="sxs-lookup"><span data-stu-id="e8aae-136">Retrieve column options.</span></span>

<!-- end list -->

  - <span data-ttu-id="e8aae-137">retinfo</span><span class="sxs-lookup"><span data-stu-id="e8aae-137">retinfo</span></span>  
    <span data-ttu-id="e8aae-138">Typ: [Microsoft.ISAM.ESENT.Interop.JET_RETINFO](./jet-retinfo-class.md)</span><span class="sxs-lookup"><span data-stu-id="e8aae-138">Type: [Microsoft.Isam.Esent.Interop.JET_RETINFO](./jet-retinfo-class.md)</span></span>  
    
    <span data-ttu-id="e8aae-139">Wenn pretinfo als NULL angegeben wird, verhält sich die Funktion so, als ob eine itagsequence von 1 und ein iblongvalue-Wert von 0 (null) angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="e8aae-139">If pretinfo is give as NULL then the function behaves as though an itagSequence of 1 and an ibLongValue of 0 (zero) were given.</span></span> <span data-ttu-id="e8aae-140">Dies bewirkt, dass der Spalten Abruf den ersten Wert einer mehrwertigen Spalte abruft und lange Daten bei Offset 0 (null) abruft.</span><span class="sxs-lookup"><span data-stu-id="e8aae-140">This causes column retrieval to retrieve the first value of a multi-valued column, and to retrieve long data at offset 0 (zero).</span></span>

#### <a name="return-value"></a><span data-ttu-id="e8aae-141">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e8aae-141">Return value</span></span>

<span data-ttu-id="e8aae-142">Typ: [Microsoft.ISAM.ESENT.Interop.JET_wrn](./jet-wrn-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="e8aae-142">Type: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span></span>  
<span data-ttu-id="e8aae-143">Ein ESENT-Warnungs Code.</span><span class="sxs-lookup"><span data-stu-id="e8aae-143">An ESENT warning code.</span></span>  

## <a name="remarks"></a><span data-ttu-id="e8aae-144">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e8aae-144">Remarks</span></span>

<span data-ttu-id="e8aae-145">Dies ist eine interne Methode, die einen Puffer Offset und eine Größe einnimmt.</span><span class="sxs-lookup"><span data-stu-id="e8aae-145">This is an internal method that takes a buffer offset as well as size.</span></span>

## <a name="see-also"></a><span data-ttu-id="e8aae-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e8aae-146">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e8aae-147">Referenz</span><span class="sxs-lookup"><span data-stu-id="e8aae-147">Reference</span></span>

[<span data-ttu-id="e8aae-148">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="e8aae-148">Api class</span></span>](./api-class.md)

[<span data-ttu-id="e8aae-149">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="e8aae-149">Api members</span></span>](./api-members.md)

[<span data-ttu-id="e8aae-150">Jetretrievecolübern-Überladung</span><span class="sxs-lookup"><span data-stu-id="e8aae-150">JetRetrieveColumn overload</span></span>](./api.jetretrievecolumn-method.md)

[<span data-ttu-id="e8aae-151">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="e8aae-151">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
