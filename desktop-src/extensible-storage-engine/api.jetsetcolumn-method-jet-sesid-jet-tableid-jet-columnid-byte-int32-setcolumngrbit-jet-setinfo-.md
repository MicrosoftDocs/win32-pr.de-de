---
description: 'Weitere Informationen finden Sie unter: API. jetsetcolumn-Methode (JET_SESID, JET_TABLEID, JET_COLUMNID, Byte, Int32, setcolumngrbit, JET_SETINFO)'
title: API. jetsetcolumn-Methode (JET_SESID, JET_TABLEID, JET_COLUMNID, Byte, Int32, setcolumngrbit, JET_SETINFO)
TOCTitle: JetSetColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, Byte , Int32, SetColumnGrbit, JET_SETINFO)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetSetColumn(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,System.Byte[],System.Int32,Microsoft.Isam.Esent.Interop.SetColumnGrbit,Microsoft.Isam.Esent.Interop.JET_SETINFO)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetsetcolumn(v=EXCHG.10)
ms:contentKeyID: 55100804
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetSetColumn
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5afebba00c784abf5bf71ac0f524376bd0f3b066
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106357067"
---
# <a name="apijetsetcolumn-method-jet_sesid-jet_tableid-jet_columnid-byte--int32-setcolumngrbit-jet_setinfo"></a><span data-ttu-id="ab0d4-103">API. jetsetcolumn-Methode (JET_SESID, JET_TABLEID, JET_COLUMNID, Byte, Int32, setcolumngrbit, JET_SETINFO)</span><span class="sxs-lookup"><span data-stu-id="ab0d4-103">Api.JetSetColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, Byte , Int32, SetColumnGrbit, JET_SETINFO)</span></span>

<span data-ttu-id="ab0d4-104">Die jetsetcolumn-Funktion ändert den Wert einer einzelnen Spalte in einem geänderten Datensatz, um eingefügt zu werden, oder um den aktuellen Datensatz zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="ab0d4-104">The JetSetColumn function modifies a single column value in a modified record to be inserted or to update the current record.</span></span> <span data-ttu-id="ab0d4-105">Es kann einen vorhandenen Wert überschreiben, einen neuen Wert zu einer Sequenz von Werten in einer mehrwertigen Spalte hinzufügen, einen Wert aus einer Sequenz von Werten in einer mehrwertigen Spalte entfernen oder den gesamten oder einen Teil eines Long-Werts aktualisieren (eine Spalte vom Typ [LONGTEXT](./jet-coltyp-enumeration.md) oder [LONGBINARY](./jet-coltyp-enumeration.md)).</span><span class="sxs-lookup"><span data-stu-id="ab0d4-105">It can overwrite an existing value, add a new value to a sequence of values in a multi-valued column, remove a value from a sequence of values in a multi-valued column, or update all or part of a long value (a column of type [LongText](./jet-coltyp-enumeration.md) or [LongBinary](./jet-coltyp-enumeration.md)).</span></span>

<span data-ttu-id="ab0d4-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="ab0d4-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="ab0d4-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="ab0d4-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="ab0d4-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="ab0d4-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function JetSetColumn ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    data As Byte(), _
    dataSize As Integer, _
    grbit As SetColumnGrbit, _
    setinfo As JET_SETINFO _
) As JET_wrn
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim data As Byte()
Dim dataSize As Integer
Dim grbit As SetColumnGrbit
Dim setinfo As JET_SETINFO
Dim returnValue As JET_wrn

returnValue = Api.JetSetColumn(sesid, _
    tableid, columnid, data, dataSize, _
    grbit, setinfo)
```

``` csharp
public static JET_wrn JetSetColumn(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    byte[] data,
    int dataSize,
    SetColumnGrbit grbit,
    JET_SETINFO setinfo
)
```

#### <a name="parameters"></a><span data-ttu-id="ab0d4-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="ab0d4-109">Parameters</span></span>

  - <span data-ttu-id="ab0d4-110">-sid</span><span class="sxs-lookup"><span data-stu-id="ab0d4-110">sesid</span></span>  
    <span data-ttu-id="ab0d4-111">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="ab0d4-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="ab0d4-112">Die Sitzung, von der das Update durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ab0d4-112">The session which is performing the update.</span></span>

<!-- end list -->

  - <span data-ttu-id="ab0d4-113">TableID</span><span class="sxs-lookup"><span data-stu-id="ab0d4-113">tableid</span></span>  
    <span data-ttu-id="ab0d4-114">Typ: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="ab0d4-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="ab0d4-115">Der Cursor, der aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="ab0d4-115">The cursor to update.</span></span> <span data-ttu-id="ab0d4-116">Ein Update sollte vorbereitet werden.</span><span class="sxs-lookup"><span data-stu-id="ab0d4-116">An update should be prepared.</span></span>

<!-- end list -->

  - <span data-ttu-id="ab0d4-117">columnid</span><span class="sxs-lookup"><span data-stu-id="ab0d4-117">columnid</span></span>  
    <span data-ttu-id="ab0d4-118">Typ: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="ab0d4-118">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="ab0d4-119">Das festzulegende ColumnID.</span><span class="sxs-lookup"><span data-stu-id="ab0d4-119">The columnid to set.</span></span>

<!-- end list -->

  - <span data-ttu-id="ab0d4-120">Daten</span><span class="sxs-lookup"><span data-stu-id="ab0d4-120">data</span></span>  
    <span data-ttu-id="ab0d4-121">Sorte \[\]</span><span class="sxs-lookup"><span data-stu-id="ab0d4-121">Type: \[\]</span></span>  
    
    <span data-ttu-id="ab0d4-122">Die festzulegenden Daten.</span><span class="sxs-lookup"><span data-stu-id="ab0d4-122">The data to set.</span></span>

<!-- end list -->

  - <span data-ttu-id="ab0d4-123">dataSize</span><span class="sxs-lookup"><span data-stu-id="ab0d4-123">dataSize</span></span>  
    <span data-ttu-id="ab0d4-124">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="ab0d4-124">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="ab0d4-125">Die Größe der festzulegenden Daten.</span><span class="sxs-lookup"><span data-stu-id="ab0d4-125">The size of data to set.</span></span>

<!-- end list -->

  - <span data-ttu-id="ab0d4-126">grbit</span><span class="sxs-lookup"><span data-stu-id="ab0d4-126">grbit</span></span>  
    <span data-ttu-id="ab0d4-127">Typ: [Microsoft. ISAM. ESENT. Interop. setcolumngrbit](./setcolumngrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="ab0d4-127">Type: [Microsoft.Isam.Esent.Interop.SetColumnGrbit](./setcolumngrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="ab0d4-128">SetColumn-Optionen.</span><span class="sxs-lookup"><span data-stu-id="ab0d4-128">SetColumn options.</span></span>

<!-- end list -->

  - <span data-ttu-id="ab0d4-129">SetInfo</span><span class="sxs-lookup"><span data-stu-id="ab0d4-129">setinfo</span></span>  
    <span data-ttu-id="ab0d4-130">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SETINFO](./jet-setinfo-class.md)</span><span class="sxs-lookup"><span data-stu-id="ab0d4-130">Type: [Microsoft.Isam.Esent.Interop.JET_SETINFO](./jet-setinfo-class.md)</span></span>  
    
    <span data-ttu-id="ab0d4-131">Wird verwendet, um ITAG oder einen Offset mit langen Werten anzugeben.</span><span class="sxs-lookup"><span data-stu-id="ab0d4-131">Used to specify itag or long-value offset.</span></span>

#### <a name="return-value"></a><span data-ttu-id="ab0d4-132">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ab0d4-132">Return value</span></span>

<span data-ttu-id="ab0d4-133">Typ: [Microsoft.ISAM.ESENT.Interop.JET_wrn](./jet-wrn-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="ab0d4-133">Type: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span></span>  
<span data-ttu-id="ab0d4-134">Ein Warnungs Code.</span><span class="sxs-lookup"><span data-stu-id="ab0d4-134">A warning code.</span></span>  

## <a name="remarks"></a><span data-ttu-id="ab0d4-135">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ab0d4-135">Remarks</span></span>

<span data-ttu-id="ab0d4-136">Die SetColumn-Methoden bieten DataType-spezifische über schreibungen, die möglicherweise effizienter sind.</span><span class="sxs-lookup"><span data-stu-id="ab0d4-136">The SetColumn methods provide datatype-specific overrides which may be more efficient.</span></span>

## <a name="see-also"></a><span data-ttu-id="ab0d4-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ab0d4-137">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ab0d4-138">Referenz</span><span class="sxs-lookup"><span data-stu-id="ab0d4-138">Reference</span></span>

[<span data-ttu-id="ab0d4-139">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="ab0d4-139">Api class</span></span>](./api-class.md)

[<span data-ttu-id="ab0d4-140">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="ab0d4-140">Api members</span></span>](./api-members.md)

[<span data-ttu-id="ab0d4-141">Jetsetcolumn-Überladung</span><span class="sxs-lookup"><span data-stu-id="ab0d4-141">JetSetColumn overload</span></span>](./api.jetsetcolumn-method.md)

[<span data-ttu-id="ab0d4-142">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="ab0d4-142">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
