---
description: 'Weitere Informationen finden Sie unter: API. jetsetcolumn-Methode (JET_SESID, JET_TABLEID, JET_COLUMNID, Byte, Int32, Int32, setcolumngrbit, JET_SETINFO)'
title: API. jetsetcolumn-Methode (JET_SESID, JET_TABLEID, JET_COLUMNID, Byte, Int32, Int32, setcolumngrbit, JET_SETINFO)
TOCTitle: JetSetColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, Byte , Int32, Int32, SetColumnGrbit, JET_SETINFO)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetSetColumn(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,System.Byte[],System.Int32,System.Int32,Microsoft.Isam.Esent.Interop.SetColumnGrbit,Microsoft.Isam.Esent.Interop.JET_SETINFO)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetsetcolumn(v=EXCHG.10)
ms:contentKeyID: 55100801
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetSetColumn
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8f52c900521d28c82245db53b98ab376dd82faec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106354443"
---
# <a name="apijetsetcolumn-method-jet_sesid-jet_tableid-jet_columnid-byte--int32-int32-setcolumngrbit-jet_setinfo"></a><span data-ttu-id="99281-103">API. jetsetcolumn-Methode (JET_SESID, JET_TABLEID, JET_COLUMNID, Byte, Int32, Int32, setcolumngrbit, JET_SETINFO)</span><span class="sxs-lookup"><span data-stu-id="99281-103">Api.JetSetColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, Byte , Int32, Int32, SetColumnGrbit, JET_SETINFO)</span></span>

<span data-ttu-id="99281-104">Die jetsetcolumn-Funktion ändert den Wert einer einzelnen Spalte in einem geänderten Datensatz, um eingefügt zu werden, oder um den aktuellen Datensatz zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="99281-104">The JetSetColumn function modifies a single column value in a modified record to be inserted or to update the current record.</span></span> <span data-ttu-id="99281-105">Es kann einen vorhandenen Wert überschreiben, einen neuen Wert zu einer Sequenz von Werten in einer mehrwertigen Spalte hinzufügen, einen Wert aus einer Sequenz von Werten in einer mehrwertigen Spalte entfernen oder den gesamten oder einen Teil eines Long-Werts aktualisieren (eine Spalte vom Typ [LONGTEXT](./jet-coltyp-enumeration.md) oder [LONGBINARY](./jet-coltyp-enumeration.md)).</span><span class="sxs-lookup"><span data-stu-id="99281-105">It can overwrite an existing value, add a new value to a sequence of values in a multi-valued column, remove a value from a sequence of values in a multi-valued column, or update all or part of a long value (a column of type [LongText](./jet-coltyp-enumeration.md) or [LongBinary](./jet-coltyp-enumeration.md)).</span></span>

<span data-ttu-id="99281-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="99281-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="99281-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="99281-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="99281-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="99281-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function JetSetColumn ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    data As Byte(), _
    dataSize As Integer, _
    dataOffset As Integer, _
    grbit As SetColumnGrbit, _
    setinfo As JET_SETINFO _
) As JET_wrn
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim data As Byte()
Dim dataSize As Integer
Dim dataOffset As Integer
Dim grbit As SetColumnGrbit
Dim setinfo As JET_SETINFO
Dim returnValue As JET_wrn

returnValue = Api.JetSetColumn(sesid, _
    tableid, columnid, data, dataSize, _
    dataOffset, grbit, setinfo)
```

``` csharp
public static JET_wrn JetSetColumn(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    byte[] data,
    int dataSize,
    int dataOffset,
    SetColumnGrbit grbit,
    JET_SETINFO setinfo
)
```

#### <a name="parameters"></a><span data-ttu-id="99281-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="99281-109">Parameters</span></span>

  - <span data-ttu-id="99281-110">-sid</span><span class="sxs-lookup"><span data-stu-id="99281-110">sesid</span></span>  
    <span data-ttu-id="99281-111">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="99281-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="99281-112">Die Sitzung, von der das Update durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="99281-112">The session which is performing the update.</span></span>

<!-- end list -->

  - <span data-ttu-id="99281-113">TableID</span><span class="sxs-lookup"><span data-stu-id="99281-113">tableid</span></span>  
    <span data-ttu-id="99281-114">Typ: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="99281-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="99281-115">Der Cursor, der aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="99281-115">The cursor to update.</span></span> <span data-ttu-id="99281-116">Ein Update sollte vorbereitet werden.</span><span class="sxs-lookup"><span data-stu-id="99281-116">An update should be prepared.</span></span>

<!-- end list -->

  - <span data-ttu-id="99281-117">columnid</span><span class="sxs-lookup"><span data-stu-id="99281-117">columnid</span></span>  
    <span data-ttu-id="99281-118">Typ: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="99281-118">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="99281-119">Das festzulegende ColumnID.</span><span class="sxs-lookup"><span data-stu-id="99281-119">The columnid to set.</span></span>

<!-- end list -->

  - <span data-ttu-id="99281-120">Daten</span><span class="sxs-lookup"><span data-stu-id="99281-120">data</span></span>  
    <span data-ttu-id="99281-121">Sorte \[\]</span><span class="sxs-lookup"><span data-stu-id="99281-121">Type: \[\]</span></span>  
    
    <span data-ttu-id="99281-122">Die festzulegenden Daten.</span><span class="sxs-lookup"><span data-stu-id="99281-122">The data to set.</span></span>

<!-- end list -->

  - <span data-ttu-id="99281-123">dataSize</span><span class="sxs-lookup"><span data-stu-id="99281-123">dataSize</span></span>  
    <span data-ttu-id="99281-124">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="99281-124">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="99281-125">Die Größe der festzulegenden Daten.</span><span class="sxs-lookup"><span data-stu-id="99281-125">The size of data to set.</span></span>

<!-- end list -->

  - <span data-ttu-id="99281-126">dataOffset</span><span class="sxs-lookup"><span data-stu-id="99281-126">dataOffset</span></span>  
    <span data-ttu-id="99281-127">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="99281-127">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="99281-128">Der Offset im Datenpuffer, aus dem Daten festgelegt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="99281-128">The offset in the data buffer to set data from.</span></span>

<!-- end list -->

  - <span data-ttu-id="99281-129">grbit</span><span class="sxs-lookup"><span data-stu-id="99281-129">grbit</span></span>  
    <span data-ttu-id="99281-130">Typ: [Microsoft. ISAM. ESENT. Interop. setcolumngrbit](./setcolumngrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="99281-130">Type: [Microsoft.Isam.Esent.Interop.SetColumnGrbit](./setcolumngrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="99281-131">SetColumn-Optionen.</span><span class="sxs-lookup"><span data-stu-id="99281-131">SetColumn options.</span></span>

<!-- end list -->

  - <span data-ttu-id="99281-132">SetInfo</span><span class="sxs-lookup"><span data-stu-id="99281-132">setinfo</span></span>  
    <span data-ttu-id="99281-133">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SETINFO](./jet-setinfo-class.md)</span><span class="sxs-lookup"><span data-stu-id="99281-133">Type: [Microsoft.Isam.Esent.Interop.JET_SETINFO](./jet-setinfo-class.md)</span></span>  
    
    <span data-ttu-id="99281-134">Wird verwendet, um ITAG oder einen Offset mit langen Werten anzugeben.</span><span class="sxs-lookup"><span data-stu-id="99281-134">Used to specify itag or long-value offset.</span></span>

#### <a name="return-value"></a><span data-ttu-id="99281-135">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="99281-135">Return value</span></span>

<span data-ttu-id="99281-136">Typ: [Microsoft.ISAM.ESENT.Interop.JET_wrn](./jet-wrn-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="99281-136">Type: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span></span>  
<span data-ttu-id="99281-137">Ein Warnungs Wert.</span><span class="sxs-lookup"><span data-stu-id="99281-137">A warning value.</span></span>  

## <a name="remarks"></a><span data-ttu-id="99281-138">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="99281-138">Remarks</span></span>

<span data-ttu-id="99281-139">Hierbei handelt es sich um eine interne Version der API, die einen Datenpuffer und einen Offset im Puffer einnimmt.</span><span class="sxs-lookup"><span data-stu-id="99281-139">This is an internal-only version of the API that takes a data buffer and an offset into the buffer.</span></span>

## <a name="see-also"></a><span data-ttu-id="99281-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="99281-140">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="99281-141">Referenz</span><span class="sxs-lookup"><span data-stu-id="99281-141">Reference</span></span>

[<span data-ttu-id="99281-142">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="99281-142">Api class</span></span>](./api-class.md)

[<span data-ttu-id="99281-143">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="99281-143">Api members</span></span>](./api-members.md)

[<span data-ttu-id="99281-144">Jetsetcolumn-Überladung</span><span class="sxs-lookup"><span data-stu-id="99281-144">JetSetColumn overload</span></span>](./api.jetsetcolumn-method.md)

[<span data-ttu-id="99281-145">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="99281-145">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
