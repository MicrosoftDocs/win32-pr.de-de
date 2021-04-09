---
description: Weitere Informationen finden Sie in der API. escrowupdate-Methode.
title: API. escrowupdate-Methode
TOCTitle: 'EscrowUpdate method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.EscrowUpdate(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.escrowupdate(v=EXCHG.10)
ms:contentKeyID: 55100668
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.EscrowUpdate
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.EscrowUpdate
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: dde632f01bd7ac9cbdf8bc4dc09e1337f32014b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749505"
---
# <a name="apiescrowupdate-method"></a><span data-ttu-id="2beec-103">API. escrowupdate-Methode</span><span class="sxs-lookup"><span data-stu-id="2beec-103">Api.EscrowUpdate method</span></span>

<span data-ttu-id="2beec-104">Durchführen einer atomaren Addition für eine Spalte</span><span class="sxs-lookup"><span data-stu-id="2beec-104">Perform atomic addition on one column.</span></span> <span data-ttu-id="2beec-105">Die Spalte muss den Typ " [Long](./jet-coltyp-enumeration.md)" aufweisen.</span><span class="sxs-lookup"><span data-stu-id="2beec-105">The column must be of type [Long](./jet-coltyp-enumeration.md).</span></span> <span data-ttu-id="2beec-106">Diese Funktion ermöglicht es mehreren Sitzungen, denselben Datensatz gleichzeitig zu aktualisieren, ohne dass Konflikte auftreten.</span><span class="sxs-lookup"><span data-stu-id="2beec-106">This function allows multiple sessions to update the same record concurrently without conflicts.</span></span>

<span data-ttu-id="2beec-107">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="2beec-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="2beec-108">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="2beec-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="2beec-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="2beec-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Function EscrowUpdate ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    delta As Integer _
) As Integer
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim delta As Integer
Dim returnValue As Integer

returnValue = Api.EscrowUpdate(sesid, _
    tableid, columnid, delta)
```

``` csharp
public static int EscrowUpdate(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    int delta
)
```

#### <a name="parameters"></a><span data-ttu-id="2beec-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="2beec-110">Parameters</span></span>

  - <span data-ttu-id="2beec-111">-sid</span><span class="sxs-lookup"><span data-stu-id="2beec-111">sesid</span></span>  
    <span data-ttu-id="2beec-112">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="2beec-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="2beec-113">Die zu verwendende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="2beec-113">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="2beec-114">TableID</span><span class="sxs-lookup"><span data-stu-id="2beec-114">tableid</span></span>  
    <span data-ttu-id="2beec-115">Typ: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="2beec-115">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="2beec-116">Der Cursor, der aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="2beec-116">The cursor to update.</span></span>

<!-- end list -->

  - <span data-ttu-id="2beec-117">columnid</span><span class="sxs-lookup"><span data-stu-id="2beec-117">columnid</span></span>  
    <span data-ttu-id="2beec-118">Typ: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="2beec-118">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="2beec-119">Die zu Aktualisier gende Spalte.</span><span class="sxs-lookup"><span data-stu-id="2beec-119">The column to update.</span></span> <span data-ttu-id="2beec-120">Dabei muss es sich um eine Spalte mit Hinterlegungs Aktualisierbarkeit handeln.</span><span class="sxs-lookup"><span data-stu-id="2beec-120">This must be an escrow-updatable column.</span></span>

<!-- end list -->

  - <span data-ttu-id="2beec-121">delta</span><span class="sxs-lookup"><span data-stu-id="2beec-121">delta</span></span>  
    <span data-ttu-id="2beec-122">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="2beec-122">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="2beec-123">Das Delta, das auf die Spalte angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="2beec-123">The delta to apply to the column.</span></span>

#### <a name="return-value"></a><span data-ttu-id="2beec-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2beec-124">Return value</span></span>

<span data-ttu-id="2beec-125">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="2beec-125">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
<span data-ttu-id="2beec-126">Der aktuelle Wert der Spalte, wie er in der Datenbank gespeichert wird (die Versionsverwaltung wird ignoriert).</span><span class="sxs-lookup"><span data-stu-id="2beec-126">The current value of the column as stored in the database (versioning is ignored).</span></span>  

## <a name="remarks"></a><span data-ttu-id="2beec-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2beec-127">Remarks</span></span>

<span data-ttu-id="2beec-128">Diese Methode umschließt [jetescrowupdate (JET_SESID, JET_TABLEID, JET_COLUMNID, \[ \] , Int32, \[ \] , Int32, Int32, escrowupdategrbit)](./api.jetescrowupdate-method.md).</span><span class="sxs-lookup"><span data-stu-id="2beec-128">This method wraps [JetEscrowUpdate(JET_SESID, JET_TABLEID, JET_COLUMNID, \[\], Int32, \[\], Int32, Int32, EscrowUpdateGrbit)](./api.jetescrowupdate-method.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="2beec-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2beec-129">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="2beec-130">Referenz</span><span class="sxs-lookup"><span data-stu-id="2beec-130">Reference</span></span>

[<span data-ttu-id="2beec-131">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="2beec-131">Api class</span></span>](./api-class.md)

[<span data-ttu-id="2beec-132">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="2beec-132">Api members</span></span>](./api-members.md)

[<span data-ttu-id="2beec-133">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="2beec-133">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
