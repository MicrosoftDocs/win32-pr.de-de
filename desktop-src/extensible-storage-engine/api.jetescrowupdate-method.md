---
description: 'Weitere Informationen finden Sie hier: API. jetescrowupdate-Methode'
title: API. jetescrowupdate-Methode
TOCTitle: 'JetEscrowUpdate method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetEscrowUpdate(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,System.Byte[],System.Int32,System.Byte[],System.Int32,System.Int32@,Microsoft.Isam.Esent.Interop.EscrowUpdateGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetescrowupdate(v=EXCHG.10)
ms:contentKeyID: 55100740
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetEscrowUpdate
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetEscrowUpdate
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 09e74f964fd6018248a3cfc594621bed96f92e60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106339767"
---
# <a name="apijetescrowupdate-method"></a><span data-ttu-id="b7c12-103">API. jetescrowupdate-Methode</span><span class="sxs-lookup"><span data-stu-id="b7c12-103">Api.JetEscrowUpdate method</span></span>

<span data-ttu-id="b7c12-104">Führt eine atomarische Additions Operation für eine Spalte aus.</span><span class="sxs-lookup"><span data-stu-id="b7c12-104">Performs an atomic addition operation on one column.</span></span> <span data-ttu-id="b7c12-105">Diese Funktion ermöglicht es mehreren Sitzungen, denselben Datensatz gleichzeitig zu aktualisieren, ohne dass Konflikte auftreten.</span><span class="sxs-lookup"><span data-stu-id="b7c12-105">This function allows multiple sessions to update the same record concurrently without conflicts.</span></span> <span data-ttu-id="b7c12-106">Siehe auch [escrowupdate (JET_SESID, JET_TABLEID, JET_COLUMNID, Int32)](./api.escrowupdate-method.md).</span><span class="sxs-lookup"><span data-stu-id="b7c12-106">Also see [EscrowUpdate(JET_SESID, JET_TABLEID, JET_COLUMNID, Int32)](./api.escrowupdate-method.md).</span></span>

<span data-ttu-id="b7c12-107">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b7c12-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="b7c12-108">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="b7c12-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b7c12-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="b7c12-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetEscrowUpdate ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    delta As Byte(), _
    deltaSize As Integer, _
    previousValue As Byte(), _
    previousValueLength As Integer, _
    <OutAttribute> ByRef actualPreviousValueLength As Integer, _
    grbit As EscrowUpdateGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim delta As Byte()
Dim deltaSize As Integer
Dim previousValue As Byte()
Dim previousValueLength As Integer
Dim actualPreviousValueLength As Integer
Dim grbit As EscrowUpdateGrbitApi.JetEscrowUpdate(sesid, tableid, _
    columnid, delta, deltaSize, previousValue, _
    previousValueLength, actualPreviousValueLength, _
    grbit)
```

``` csharp
public static void JetEscrowUpdate(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    byte[] delta,
    int deltaSize,
    byte[] previousValue,
    int previousValueLength,
    out int actualPreviousValueLength,
    EscrowUpdateGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="b7c12-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="b7c12-110">Parameters</span></span>

  - <span data-ttu-id="b7c12-111">-sid</span><span class="sxs-lookup"><span data-stu-id="b7c12-111">sesid</span></span>  
    <span data-ttu-id="b7c12-112">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="b7c12-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="b7c12-113">Die zu verwendende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="b7c12-113">The session to use.</span></span> <span data-ttu-id="b7c12-114">Die Sitzung muss sich in einer Transaktion befinden.</span><span class="sxs-lookup"><span data-stu-id="b7c12-114">The session must be in a transaction.</span></span>

<!-- end list -->

  - <span data-ttu-id="b7c12-115">TableID</span><span class="sxs-lookup"><span data-stu-id="b7c12-115">tableid</span></span>  
    <span data-ttu-id="b7c12-116">Typ: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="b7c12-116">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="b7c12-117">Der Cursor, der aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="b7c12-117">The cursor to update.</span></span>

<!-- end list -->

  - <span data-ttu-id="b7c12-118">columnid</span><span class="sxs-lookup"><span data-stu-id="b7c12-118">columnid</span></span>  
    <span data-ttu-id="b7c12-119">Typ: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="b7c12-119">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="b7c12-120">Die zu Aktualisier gende Spalte.</span><span class="sxs-lookup"><span data-stu-id="b7c12-120">The column to update.</span></span> <span data-ttu-id="b7c12-121">Dabei muss es sich um eine aktualisierbare Spalte für die Hinterlegung</span><span class="sxs-lookup"><span data-stu-id="b7c12-121">This must be an escrow updatable column.</span></span>

<!-- end list -->

  - <span data-ttu-id="b7c12-122">delta</span><span class="sxs-lookup"><span data-stu-id="b7c12-122">delta</span></span>  
    <span data-ttu-id="b7c12-123">Sorte \[\]</span><span class="sxs-lookup"><span data-stu-id="b7c12-123">Type: \[\]</span></span>  
    
    <span data-ttu-id="b7c12-124">Der Puffer, der den Addend enthält.</span><span class="sxs-lookup"><span data-stu-id="b7c12-124">The buffer containing the addend.</span></span>

<!-- end list -->

  - <span data-ttu-id="b7c12-125">Delta size</span><span class="sxs-lookup"><span data-stu-id="b7c12-125">deltaSize</span></span>  
    <span data-ttu-id="b7c12-126">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="b7c12-126">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="b7c12-127">Die Größe des Addend.</span><span class="sxs-lookup"><span data-stu-id="b7c12-127">The size of the addend.</span></span>

<!-- end list -->

  - <span data-ttu-id="b7c12-128">previousValue</span><span class="sxs-lookup"><span data-stu-id="b7c12-128">previousValue</span></span>  
    <span data-ttu-id="b7c12-129">Sorte \[\]</span><span class="sxs-lookup"><span data-stu-id="b7c12-129">Type: \[\]</span></span>  
    
    <span data-ttu-id="b7c12-130">Ein Ausgabepuffer, der den aktuellen Wert der Spalte empfängt.</span><span class="sxs-lookup"><span data-stu-id="b7c12-130">An output buffer that will recieve the current value of the column.</span></span> <span data-ttu-id="b7c12-131">Dieser Puffer kann NULL sein.</span><span class="sxs-lookup"><span data-stu-id="b7c12-131">This buffer can be null.</span></span>

<!-- end list -->

  - <span data-ttu-id="b7c12-132">previousvaluelength</span><span class="sxs-lookup"><span data-stu-id="b7c12-132">previousValueLength</span></span>  
    <span data-ttu-id="b7c12-133">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="b7c12-133">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="b7c12-134">Die Größe des previousValue-Puffers.</span><span class="sxs-lookup"><span data-stu-id="b7c12-134">The size of the previousValue buffer.</span></span>

<!-- end list -->

  - <span data-ttu-id="b7c12-135">actualpreviousvaluelength</span><span class="sxs-lookup"><span data-stu-id="b7c12-135">actualPreviousValueLength</span></span>  
    <span data-ttu-id="b7c12-136">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="b7c12-136">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="b7c12-137">Gibt die tatsächliche Größe von previousValue zurück.</span><span class="sxs-lookup"><span data-stu-id="b7c12-137">Returns the actual size of the previousValue.</span></span>

<!-- end list -->

  - <span data-ttu-id="b7c12-138">grbit</span><span class="sxs-lookup"><span data-stu-id="b7c12-138">grbit</span></span>  
    <span data-ttu-id="b7c12-139">Typ: [Microsoft. ISAM. ESENT. Interop. escrowupdategrbit](./escrowupdategrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="b7c12-139">Type: [Microsoft.Isam.Esent.Interop.EscrowUpdateGrbit](./escrowupdategrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="b7c12-140">Optionen zum Aktualisieren von Optionen.</span><span class="sxs-lookup"><span data-stu-id="b7c12-140">Escrow update options.</span></span>

## <a name="see-also"></a><span data-ttu-id="b7c12-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b7c12-141">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b7c12-142">Referenz</span><span class="sxs-lookup"><span data-stu-id="b7c12-142">Reference</span></span>

[<span data-ttu-id="b7c12-143">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="b7c12-143">Api class</span></span>](./api-class.md)

[<span data-ttu-id="b7c12-144">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="b7c12-144">Api members</span></span>](./api-members.md)

[<span data-ttu-id="b7c12-145">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="b7c12-145">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
