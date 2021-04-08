---
description: Weitere Informationen finden Sie in der API. tryseek-Methode.
title: API. tryseek-Methode
TOCTitle: 'TrySeek method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.TrySeek(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.SeekGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.tryseek(v=EXCHG.10)
ms:contentKeyID: 55100941
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.TrySeek
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.TrySeek
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 46472c59c14bd515e744a7ccfa908752783d27fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862223"
---
# <a name="apitryseek-method"></a><span data-ttu-id="f76b8-103">API. tryseek-Methode</span><span class="sxs-lookup"><span data-stu-id="f76b8-103">Api.TrySeek method</span></span>

<span data-ttu-id="f76b8-104">Positioniert einen Cursor effizient auf einen Index Eintrag, der den Suchkriterien entspricht, die durch den Suchschlüssel in diesem Cursor und die angegebene Ungleichheit angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="f76b8-104">Efficiently positions a cursor to an index entry that matches the search criteria specified by the search key in that cursor and the specified inequality.</span></span> <span data-ttu-id="f76b8-105">Ein Suchschlüssel muss zuvor mithilfe von jetmakekey erstellt worden sein.</span><span class="sxs-lookup"><span data-stu-id="f76b8-105">A search key must have been previously constructed using JetMakeKey.</span></span>

<span data-ttu-id="f76b8-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f76b8-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="f76b8-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="f76b8-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f76b8-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="f76b8-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function TrySeek ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    grbit As SeekGrbit _
) As Boolean
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim grbit As SeekGrbit
Dim returnValue As Boolean

returnValue = Api.TrySeek(sesid, _
    tableid, grbit)
```

``` csharp
public static bool TrySeek(
    JET_SESID sesid,
    JET_TABLEID tableid,
    SeekGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="f76b8-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="f76b8-109">Parameters</span></span>

  - <span data-ttu-id="f76b8-110">-sid</span><span class="sxs-lookup"><span data-stu-id="f76b8-110">sesid</span></span>  
    <span data-ttu-id="f76b8-111">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="f76b8-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="f76b8-112">Die zu verwendende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="f76b8-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="f76b8-113">TableID</span><span class="sxs-lookup"><span data-stu-id="f76b8-113">tableid</span></span>  
    <span data-ttu-id="f76b8-114">Typ: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="f76b8-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="f76b8-115">Der Cursor, der positioniert werden soll.</span><span class="sxs-lookup"><span data-stu-id="f76b8-115">The cursor to position.</span></span>

<!-- end list -->

  - <span data-ttu-id="f76b8-116">grbit</span><span class="sxs-lookup"><span data-stu-id="f76b8-116">grbit</span></span>  
    <span data-ttu-id="f76b8-117">Typ: [Microsoft. ISAM. ESENT. Interop. seekgrbit](./seekgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="f76b8-117">Type: [Microsoft.Isam.Esent.Interop.SeekGrbit](./seekgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="f76b8-118">Seek-Option.</span><span class="sxs-lookup"><span data-stu-id="f76b8-118">Seek option.</span></span>

#### <a name="return-value"></a><span data-ttu-id="f76b8-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f76b8-119">Return value</span></span>

<span data-ttu-id="f76b8-120">Typ: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="f76b8-120">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="f76b8-121">True, wenn ein Datensatz gefunden wurde, der mit den Kriterien übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="f76b8-121">True if a record matching the criteria was found.</span></span>  

## <a name="see-also"></a><span data-ttu-id="f76b8-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f76b8-122">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f76b8-123">Referenz</span><span class="sxs-lookup"><span data-stu-id="f76b8-123">Reference</span></span>

[<span data-ttu-id="f76b8-124">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="f76b8-124">Api class</span></span>](./api-class.md)

[<span data-ttu-id="f76b8-125">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="f76b8-125">Api members</span></span>](./api-members.md)

[<span data-ttu-id="f76b8-126">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="f76b8-126">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
