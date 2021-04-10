---
description: Weitere Informationen finden Sie in der API. jetenreeratecolumschlag-Methode.
title: API. jetenreeratecolumschlag-Methode
TOCTitle: 'JetEnumerateColumns method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetEnumerateColumns(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Int32,Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID[],System.Int32@,Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN[]@,Microsoft.Isam.Esent.Interop.JET_PFNREALLOC,System.IntPtr,System.Int32,Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetenumeratecolumns(v=EXCHG.10)
ms:contentKeyID: 55100695
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetEnumerateColumns
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetEnumerateColumns
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c9a9848d4470d54cc2a146098343b664c9bd3419
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041662"
---
# <a name="apijetenumeratecolumns-method"></a><span data-ttu-id="7d48e-103">API. jetenreeratecolumschlag-Methode</span><span class="sxs-lookup"><span data-stu-id="7d48e-103">Api.JetEnumerateColumns method</span></span>

<span data-ttu-id="7d48e-104">Ruft effizient eine Gruppe von Spalten und deren Werten aus dem aktuellen Datensatz eines Cursors oder dem Kopier Puffer dieses Cursors ab.</span><span class="sxs-lookup"><span data-stu-id="7d48e-104">Efficiently retrieves a set of columns and their values from the current record of a cursor or the copy buffer of that cursor.</span></span> <span data-ttu-id="7d48e-105">Die abgerufenen Spalten und Werte können durch eine Liste von Spalten-IDs, itagsequence-Nummern und anderen Merkmalen eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="7d48e-105">The columns and values retrieved can be restricted by a list of column IDs, itagSequence numbers, and other characteristics.</span></span> <span data-ttu-id="7d48e-106">Diese Spalten Abruf-API ist eindeutig, da Sie Informationen in dynamisch zugewiesener Speicher zurückgibt, die mit einem vom Benutzer bereitgestellten rezuordnungskompatiblen Rückruf abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="7d48e-106">This column retrieval API is unique in that it returns information in dynamically allocated memory that is obtained using a user-provided realloc compatible callback.</span></span> <span data-ttu-id="7d48e-107">Diese neue Flexibilität ermöglicht das effiziente Abrufen von Spaltendaten mit bestimmten Merkmalen (z. b. Größe und Multiplizität), die dem Aufrufer unbekannt sind.</span><span class="sxs-lookup"><span data-stu-id="7d48e-107">This new flexibility permits the efficient retrieval of column data with specific characteristics (such as size and multiplicity) that are unknown to the caller.</span></span> <span data-ttu-id="7d48e-108">Dadurch ist es nicht mehr erforderlich, die Ermittlungs Modi jetretrievecolumgen zu verwenden, um die Eigenschaften zu bestimmen, um einen letzten Rückruf für jetretrievecolumschlag einzurichten, mit dem die gewünschten Daten erfolgreich abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="7d48e-108">This eliminates the need for the use of the discovery modes of JetRetrieveColumn to determine those characteristics in order to setup a final call to JetRetrieveColumn that will successfully retrieve the desired data.</span></span>

<span data-ttu-id="7d48e-109">Diese API ist nicht CLS-kompatibel.</span><span class="sxs-lookup"><span data-stu-id="7d48e-109">This API is not CLS-compliant.</span></span> 

<span data-ttu-id="7d48e-110">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="7d48e-110">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="7d48e-111">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="7d48e-111">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="7d48e-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="7d48e-112">Syntax</span></span>

``` vb
'Declaration
<CLSCompliantAttribute(False)> _
Public Shared Function JetEnumerateColumns ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    numColumnids As Integer, _
    columnids As JET_ENUMCOLUMNID(), _
    <OutAttribute> ByRef numColumnValues As Integer, _
    <OutAttribute> ByRef columnValues As JET_ENUMCOLUMN(), _
    allocator As JET_PFNREALLOC, _
    allocatorContext As IntPtr, _
    maxDataSize As Integer, _
    grbit As EnumerateColumnsGrbit _
) As JET_wrn
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim numColumnids As Integer
Dim columnids As JET_ENUMCOLUMNID()
Dim numColumnValues As Integer
Dim columnValues As JET_ENUMCOLUMN()
Dim allocator As JET_PFNREALLOC
Dim allocatorContext As IntPtr
Dim maxDataSize As Integer
Dim grbit As EnumerateColumnsGrbit
Dim returnValue As JET_wrn

returnValue = Api.JetEnumerateColumns(sesid, _
    tableid, numColumnids, columnids, _
    numColumnValues, columnValues, allocator, _
    allocatorContext, maxDataSize, grbit)
```

``` csharp
[CLSCompliantAttribute(false)]
public static JET_wrn JetEnumerateColumns(
    JET_SESID sesid,
    JET_TABLEID tableid,
    int numColumnids,
    JET_ENUMCOLUMNID[] columnids,
    out int numColumnValues,
    out JET_ENUMCOLUMN[] columnValues,
    JET_PFNREALLOC allocator,
    IntPtr allocatorContext,
    int maxDataSize,
    EnumerateColumnsGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="7d48e-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="7d48e-113">Parameters</span></span>

  - <span data-ttu-id="7d48e-114">-sid</span><span class="sxs-lookup"><span data-stu-id="7d48e-114">sesid</span></span>  
    <span data-ttu-id="7d48e-115">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="7d48e-115">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="7d48e-116">Die zu verwendende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="7d48e-116">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="7d48e-117">TableID</span><span class="sxs-lookup"><span data-stu-id="7d48e-117">tableid</span></span>  
    <span data-ttu-id="7d48e-118">Typ: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="7d48e-118">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="7d48e-119">Der Cursor, von dem Daten abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="7d48e-119">The cursor to retrieve data from.</span></span>

<!-- end list -->

  - <span data-ttu-id="7d48e-120">numcolumnids</span><span class="sxs-lookup"><span data-stu-id="7d48e-120">numColumnids</span></span>  
    <span data-ttu-id="7d48e-121">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="7d48e-121">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="7d48e-122">Die Anzahl der JET_ENUMCOLUMNIDS.</span><span class="sxs-lookup"><span data-stu-id="7d48e-122">The numbers of JET_ENUMCOLUMNIDS.</span></span>

<!-- end list -->

  - <span data-ttu-id="7d48e-123">columnIds</span><span class="sxs-lookup"><span data-stu-id="7d48e-123">columnids</span></span>  
    <span data-ttu-id="7d48e-124">Sorte \[\]</span><span class="sxs-lookup"><span data-stu-id="7d48e-124">Type: \[\]</span></span>  
    
    <span data-ttu-id="7d48e-125">Ein optionales Array von Spalten-IDs, von denen jedes ein optionales Array von itagsequence-Zahlen auflistet.</span><span class="sxs-lookup"><span data-stu-id="7d48e-125">An optional array of column IDs, each with an optional array of itagSequence numbers to enumerate.</span></span>

<!-- end list -->

  - <span data-ttu-id="7d48e-126">numcolumnvalues</span><span class="sxs-lookup"><span data-stu-id="7d48e-126">numColumnValues</span></span>  
    <span data-ttu-id="7d48e-127">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="7d48e-127">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="7d48e-128">Gibt die Anzahl der abgerufenen Spaltenwerte zurück.</span><span class="sxs-lookup"><span data-stu-id="7d48e-128">Returns the number of column values retrieved.</span></span>

<!-- end list -->

  - <span data-ttu-id="7d48e-129">columnvalues</span><span class="sxs-lookup"><span data-stu-id="7d48e-129">columnValues</span></span>  
    <span data-ttu-id="7d48e-130">Sorte \[\]</span><span class="sxs-lookup"><span data-stu-id="7d48e-130">Type: \[\]</span></span>  
    
    <span data-ttu-id="7d48e-131">Gibt die aufgelisteten Spaltenwerte zurück.</span><span class="sxs-lookup"><span data-stu-id="7d48e-131">Returns the enumerated column values.</span></span>

<!-- end list -->

  - <span data-ttu-id="7d48e-132">allocator</span><span class="sxs-lookup"><span data-stu-id="7d48e-132">allocator</span></span>  
    <span data-ttu-id="7d48e-133">Typ: [Microsoft.ISAM.ESENT.Interop.JET_PFNREALLOC](./jet-pfnrealloc-delegate.md)</span><span class="sxs-lookup"><span data-stu-id="7d48e-133">Type: [Microsoft.Isam.Esent.Interop.JET_PFNREALLOC](./jet-pfnrealloc-delegate.md)</span></span>  
    
    <span data-ttu-id="7d48e-134">Rückruf, der zum Zuordnen von Speicher verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7d48e-134">Callback used to allocate memory.</span></span>

<!-- end list -->

  - <span data-ttu-id="7d48e-135">' Zuweisung '</span><span class="sxs-lookup"><span data-stu-id="7d48e-135">allocatorContext</span></span>  
    <span data-ttu-id="7d48e-136">Typ: [System. IntPtr](/dotnet/api/system.intptr)</span><span class="sxs-lookup"><span data-stu-id="7d48e-136">Type: [System.IntPtr](/dotnet/api/system.intptr)</span></span>  
    
    <span data-ttu-id="7d48e-137">Der Kontext für den Zuordnungs Rückruf.</span><span class="sxs-lookup"><span data-stu-id="7d48e-137">Context for the allocation callback.</span></span>

<!-- end list -->

  - <span data-ttu-id="7d48e-138">maxdatasize</span><span class="sxs-lookup"><span data-stu-id="7d48e-138">maxDataSize</span></span>  
    <span data-ttu-id="7d48e-139">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="7d48e-139">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="7d48e-140">Legt eine Obergrenze für die Menge der Daten fest, die von einer Long-Text-oder Long Binary-Spalte zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="7d48e-140">Sets a cap on the amount of data to return from a long text or long binary column.</span></span> <span data-ttu-id="7d48e-141">Dieser Parameter kann verwendet werden, um die Enumeration eines extrem großen Spaltenwerts zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="7d48e-141">This parameter can be used to prevent the enumeration of an extremely large column value.</span></span>

<!-- end list -->

  - <span data-ttu-id="7d48e-142">grbit</span><span class="sxs-lookup"><span data-stu-id="7d48e-142">grbit</span></span>  
    <span data-ttu-id="7d48e-143">Typ: [Microsoft. ISAM. ESENT. Interop. enumeratecolumnsgrbit](./enumeratecolumnsgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="7d48e-143">Type: [Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit](./enumeratecolumnsgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="7d48e-144">Abrufen von Optionen.</span><span class="sxs-lookup"><span data-stu-id="7d48e-144">Retrieve options.</span></span>

#### <a name="return-value"></a><span data-ttu-id="7d48e-145">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7d48e-145">Return value</span></span>

<span data-ttu-id="7d48e-146">Typ: [Microsoft.ISAM.ESENT.Interop.JET_wrn](./jet-wrn-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="7d48e-146">Type: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span></span>  
<span data-ttu-id="7d48e-147">Eine Warnung oder ein Erfolg.</span><span class="sxs-lookup"><span data-stu-id="7d48e-147">A warning or success.</span></span>  

## <a name="see-also"></a><span data-ttu-id="7d48e-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7d48e-148">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="7d48e-149">Referenz</span><span class="sxs-lookup"><span data-stu-id="7d48e-149">Reference</span></span>

[<span data-ttu-id="7d48e-150">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="7d48e-150">Api class</span></span>](./api-class.md)

[<span data-ttu-id="7d48e-151">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="7d48e-151">Api members</span></span>](./api-members.md)

[<span data-ttu-id="7d48e-152">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="7d48e-152">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
