---
description: 'Weitere Informationen finden Sie unter: API. jetretrievekey-Methode'
title: API. jetretrievekey-Methode
TOCTitle: 'JetRetrieveKey method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetRetrieveKey(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Byte[],System.Int32,System.Int32@,Microsoft.Isam.Esent.Interop.RetrieveKeyGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetretrievekey(v=EXCHG.10)
ms:contentKeyID: 55100795
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetRetrieveKey
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetRetrieveKey
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ebf130b4542992e18de49d58801f789d40106fef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369868"
---
# <a name="apijetretrievekey-method"></a><span data-ttu-id="c6180-103">API. jetretrievekey-Methode</span><span class="sxs-lookup"><span data-stu-id="c6180-103">Api.JetRetrieveKey method</span></span>

<span data-ttu-id="c6180-104">Ruft den Schlüssel für den Index Eintrag an der aktuellen Position eines Cursors ab.</span><span class="sxs-lookup"><span data-stu-id="c6180-104">Retrieves the key for the index entry at the current position of a cursor.</span></span> <span data-ttu-id="c6180-105">Siehe auch [retrievekey (JET_SESID, JET_TABLEID, retrievekeygrbit)](./api.retrievekey-method.md).</span><span class="sxs-lookup"><span data-stu-id="c6180-105">Also see [RetrieveKey(JET_SESID, JET_TABLEID, RetrieveKeyGrbit)](./api.retrievekey-method.md).</span></span>

<span data-ttu-id="c6180-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="c6180-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="c6180-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="c6180-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="c6180-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="c6180-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetRetrieveKey ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    data As Byte(), _
    dataSize As Integer, _
    <OutAttribute> ByRef actualDataSize As Integer, _
    grbit As RetrieveKeyGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim data As Byte()
Dim dataSize As Integer
Dim actualDataSize As Integer
Dim grbit As RetrieveKeyGrbitApi.JetRetrieveKey(sesid, tableid, _
    data, dataSize, actualDataSize, grbit)
```

``` csharp
public static void JetRetrieveKey(
    JET_SESID sesid,
    JET_TABLEID tableid,
    byte[] data,
    int dataSize,
    out int actualDataSize,
    RetrieveKeyGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="c6180-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="c6180-109">Parameters</span></span>

  - <span data-ttu-id="c6180-110">-sid</span><span class="sxs-lookup"><span data-stu-id="c6180-110">sesid</span></span>  
    <span data-ttu-id="c6180-111">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="c6180-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="c6180-112">Die zu verwendende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="c6180-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="c6180-113">TableID</span><span class="sxs-lookup"><span data-stu-id="c6180-113">tableid</span></span>  
    <span data-ttu-id="c6180-114">Typ: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="c6180-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="c6180-115">Der Cursor, aus dem der Schlüssel abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="c6180-115">The cursor to retrieve the key from.</span></span>

<!-- end list -->

  - <span data-ttu-id="c6180-116">Daten</span><span class="sxs-lookup"><span data-stu-id="c6180-116">data</span></span>  
    <span data-ttu-id="c6180-117">Sorte \[\]</span><span class="sxs-lookup"><span data-stu-id="c6180-117">Type: \[\]</span></span>  
    
    <span data-ttu-id="c6180-118">Der Puffer, in den der Schlüssel abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="c6180-118">The buffer to retrieve the key into.</span></span>

<!-- end list -->

  - <span data-ttu-id="c6180-119">dataSize</span><span class="sxs-lookup"><span data-stu-id="c6180-119">dataSize</span></span>  
    <span data-ttu-id="c6180-120">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="c6180-120">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="c6180-121">Die Größe des Puffers.</span><span class="sxs-lookup"><span data-stu-id="c6180-121">The size of the buffer.</span></span>

<!-- end list -->

  - <span data-ttu-id="c6180-122">actualdatasize</span><span class="sxs-lookup"><span data-stu-id="c6180-122">actualDataSize</span></span>  
    <span data-ttu-id="c6180-123">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="c6180-123">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="c6180-124">Gibt die tatsächliche Größe der Daten zurück.</span><span class="sxs-lookup"><span data-stu-id="c6180-124">Returns the actual size of the data.</span></span>

<!-- end list -->

  - <span data-ttu-id="c6180-125">grbit</span><span class="sxs-lookup"><span data-stu-id="c6180-125">grbit</span></span>  
    <span data-ttu-id="c6180-126">Typ: [Microsoft. ISAM. ESENT. Interop. retrievekeygrbit](./retrievekeygrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="c6180-126">Type: [Microsoft.Isam.Esent.Interop.RetrieveKeyGrbit](./retrievekeygrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="c6180-127">Abrufen von Schlüsseloptionen</span><span class="sxs-lookup"><span data-stu-id="c6180-127">Retrieve key options.</span></span>

## <a name="see-also"></a><span data-ttu-id="c6180-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c6180-128">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c6180-129">Referenz</span><span class="sxs-lookup"><span data-stu-id="c6180-129">Reference</span></span>

[<span data-ttu-id="c6180-130">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="c6180-130">Api class</span></span>](./api-class.md)

[<span data-ttu-id="c6180-131">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="c6180-131">Api members</span></span>](./api-members.md)

[<span data-ttu-id="c6180-132">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="c6180-132">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
