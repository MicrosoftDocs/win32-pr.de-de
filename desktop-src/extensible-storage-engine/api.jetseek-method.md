---
description: 'Weitere Informationen über: API. JetSeek-Methode'
title: API. JetSeek-Methode
TOCTitle: 'JetSeek method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetSeek(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.SeekGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetseek(v=EXCHG.10)
ms:contentKeyID: 55100796
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetSeek
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetSeek
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 85c8c61bd4e56b342b33d26f22ae3946967640e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960791"
---
# <a name="apijetseek-method"></a><span data-ttu-id="64e71-103">API. JetSeek-Methode</span><span class="sxs-lookup"><span data-stu-id="64e71-103">Api.JetSeek method</span></span>

<span data-ttu-id="64e71-104">Positioniert einen Cursor effizient auf einen Index Eintrag, der den Suchkriterien entspricht, die durch den Suchschlüssel in diesem Cursor und die angegebene Ungleichheit angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="64e71-104">Efficiently positions a cursor to an index entry that matches the search criteria specified by the search key in that cursor and the specified inequality.</span></span> <span data-ttu-id="64e71-105">Ein Suchschlüssel muss zuvor mithilfe von [jetmakekey (JET_SESID, JET_TABLEID, \[ \] , Int32, makekeygrbit)](./api.jetmakekey-method.md)erstellt worden sein.</span><span class="sxs-lookup"><span data-stu-id="64e71-105">A search key must have been previously constructed using [JetMakeKey(JET_SESID, JET_TABLEID, \[\], Int32, MakeKeyGrbit)](./api.jetmakekey-method.md).</span></span> <span data-ttu-id="64e71-106">Siehe auch [tryseek (JET_SESID, JET_TABLEID, seekgrbit)](./api.tryseek-method.md).</span><span class="sxs-lookup"><span data-stu-id="64e71-106">Also see [TrySeek(JET_SESID, JET_TABLEID, SeekGrbit)](./api.tryseek-method.md).</span></span>

<span data-ttu-id="64e71-107">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="64e71-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="64e71-108">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="64e71-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="64e71-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="64e71-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Function JetSeek ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    grbit As SeekGrbit _
) As JET_wrn
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim grbit As SeekGrbit
Dim returnValue As JET_wrn

returnValue = Api.JetSeek(sesid, _
    tableid, grbit)
```

``` csharp
public static JET_wrn JetSeek(
    JET_SESID sesid,
    JET_TABLEID tableid,
    SeekGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="64e71-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="64e71-110">Parameters</span></span>

  - <span data-ttu-id="64e71-111">-sid</span><span class="sxs-lookup"><span data-stu-id="64e71-111">sesid</span></span>  
    <span data-ttu-id="64e71-112">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="64e71-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="64e71-113">Die zu verwendende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="64e71-113">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="64e71-114">TableID</span><span class="sxs-lookup"><span data-stu-id="64e71-114">tableid</span></span>  
    <span data-ttu-id="64e71-115">Typ: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="64e71-115">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="64e71-116">Der Cursor, der positioniert werden soll.</span><span class="sxs-lookup"><span data-stu-id="64e71-116">The cursor to position.</span></span>

<!-- end list -->

  - <span data-ttu-id="64e71-117">grbit</span><span class="sxs-lookup"><span data-stu-id="64e71-117">grbit</span></span>  
    <span data-ttu-id="64e71-118">Typ: [Microsoft. ISAM. ESENT. Interop. seekgrbit](./seekgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="64e71-118">Type: [Microsoft.Isam.Esent.Interop.SeekGrbit](./seekgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="64e71-119">Suchoptionen.</span><span class="sxs-lookup"><span data-stu-id="64e71-119">Seek options.</span></span>

#### <a name="return-value"></a><span data-ttu-id="64e71-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="64e71-120">Return value</span></span>

<span data-ttu-id="64e71-121">Typ: [Microsoft.ISAM.ESENT.Interop.JET_wrn](./jet-wrn-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="64e71-121">Type: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span></span>  
<span data-ttu-id="64e71-122">Eine ESENT-Warnung.</span><span class="sxs-lookup"><span data-stu-id="64e71-122">An ESENT warning.</span></span>  

## <a name="see-also"></a><span data-ttu-id="64e71-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="64e71-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="64e71-124">Referenz</span><span class="sxs-lookup"><span data-stu-id="64e71-124">Reference</span></span>

[<span data-ttu-id="64e71-125">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="64e71-125">Api class</span></span>](./api-class.md)

[<span data-ttu-id="64e71-126">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="64e71-126">Api members</span></span>](./api-members.md)

[<span data-ttu-id="64e71-127">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="64e71-127">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
