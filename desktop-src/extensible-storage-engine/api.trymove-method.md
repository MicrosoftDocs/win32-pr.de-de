---
description: Weitere Informationen finden Sie in der API. trymove-Methode.
title: API. trymove-Methode
TOCTitle: 'TryMove method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.TryMove(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_Move,Microsoft.Isam.Esent.Interop.MoveGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.trymove(v=EXCHG.10)
ms:contentKeyID: 55100883
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.TryMove
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.TryMove
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6d4b3aa596bb5e813d87dcc6f278112fe1e4cbdb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343630"
---
# <a name="apitrymove-method"></a><span data-ttu-id="1e5c0-103">API. trymove-Methode</span><span class="sxs-lookup"><span data-stu-id="1e5c0-103">Api.TryMove method</span></span>

<span data-ttu-id="1e5c0-104">Versuchen Sie, durch einen Index zu navigieren.</span><span class="sxs-lookup"><span data-stu-id="1e5c0-104">Try to navigate through an index.</span></span> <span data-ttu-id="1e5c0-105">Wenn die Navigation erfolgreich ist, gibt diese Methode true zurück.</span><span class="sxs-lookup"><span data-stu-id="1e5c0-105">If the navigation succeeds this method returns true.</span></span> <span data-ttu-id="1e5c0-106">Wenn kein Datensatz vorhanden ist, um zu dieser Methode zu navigieren, wird false zurückgegeben. für andere Fehler wird eine Ausnahme ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="1e5c0-106">If there is no record to navigate to this method returns false; an exception will be thrown for other errors.</span></span>

<span data-ttu-id="1e5c0-107">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="1e5c0-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="1e5c0-108">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="1e5c0-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="1e5c0-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="1e5c0-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Function TryMove ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    move As JET_Move, _
    grbit As MoveGrbit _
) As Boolean
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim move As JET_Move
Dim grbit As MoveGrbit
Dim returnValue As Boolean

returnValue = Api.TryMove(sesid, _
    tableid, move, grbit)
```

``` csharp
public static bool TryMove(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_Move move,
    MoveGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="1e5c0-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="1e5c0-110">Parameters</span></span>

  - <span data-ttu-id="1e5c0-111">-sid</span><span class="sxs-lookup"><span data-stu-id="1e5c0-111">sesid</span></span>  
    <span data-ttu-id="1e5c0-112">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="1e5c0-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="1e5c0-113">Die zu verwendende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="1e5c0-113">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="1e5c0-114">TableID</span><span class="sxs-lookup"><span data-stu-id="1e5c0-114">tableid</span></span>  
    <span data-ttu-id="1e5c0-115">Typ: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="1e5c0-115">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="1e5c0-116">Der Cursor, der positioniert werden soll.</span><span class="sxs-lookup"><span data-stu-id="1e5c0-116">The cursor to position.</span></span>

<!-- end list -->

  - <span data-ttu-id="1e5c0-117">Verschieben</span><span class="sxs-lookup"><span data-stu-id="1e5c0-117">move</span></span>  
    <span data-ttu-id="1e5c0-118">Typ: [Microsoft.ISAM.ESENT.Interop.JET_Move](./jet-move-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="1e5c0-118">Type: [Microsoft.Isam.Esent.Interop.JET_Move](./jet-move-enumeration.md)</span></span>  
    
    <span data-ttu-id="1e5c0-119">Die Richtung, in die verschoben werden soll.</span><span class="sxs-lookup"><span data-stu-id="1e5c0-119">The direction to move in.</span></span>

<!-- end list -->

  - <span data-ttu-id="1e5c0-120">grbit</span><span class="sxs-lookup"><span data-stu-id="1e5c0-120">grbit</span></span>  
    <span data-ttu-id="1e5c0-121">Typ: [Microsoft. ISAM. ESENT. Interop. muvegrbit](./movegrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="1e5c0-121">Type: [Microsoft.Isam.Esent.Interop.MoveGrbit](./movegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="1e5c0-122">Verschieben von Optionen.</span><span class="sxs-lookup"><span data-stu-id="1e5c0-122">Move options.</span></span>

#### <a name="return-value"></a><span data-ttu-id="1e5c0-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1e5c0-123">Return value</span></span>

<span data-ttu-id="1e5c0-124">Typ: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="1e5c0-124">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="1e5c0-125">True, wenn die Verschiebung erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="1e5c0-125">True if the move was successful.</span></span>  

## <a name="see-also"></a><span data-ttu-id="1e5c0-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1e5c0-126">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="1e5c0-127">Referenz</span><span class="sxs-lookup"><span data-stu-id="1e5c0-127">Reference</span></span>

[<span data-ttu-id="1e5c0-128">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="1e5c0-128">Api class</span></span>](./api-class.md)

[<span data-ttu-id="1e5c0-129">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="1e5c0-129">Api members</span></span>](./api-members.md)

[<span data-ttu-id="1e5c0-130">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="1e5c0-130">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
