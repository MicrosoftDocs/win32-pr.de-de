---
description: 'Weitere Informationen finden Sie hier: JET_THREADSTATS. Create-Methode'
title: JET_THREADSTATS. Create-Methode (Microsoft. ISAM. ESENT. Interop. Vista)
TOCTitle: 'Create method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Create(System.Int32,System.Int32,System.Int32,System.Int32,System.Int32,System.Int32,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_threadstats.create(v=EXCHG.10)
ms:contentKeyID: 39509886
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Create
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Create
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: beaaee85fc0f6c331db1d813280d4b900e39fb54
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758491"
---
# <a name="jet_threadstatscreate-method"></a><span data-ttu-id="e71b8-103">JET_THREADSTATS. Create-Methode</span><span class="sxs-lookup"><span data-stu-id="e71b8-103">JET_THREADSTATS.Create method</span></span>

<span data-ttu-id="e71b8-104">Erstellen Sie eine neue [JET_THREADSTATS](./jet-threadstats-structure2.md) Struktur mit dem angegebenen Wert.</span><span class="sxs-lookup"><span data-stu-id="e71b8-104">Create a new [JET_THREADSTATS](./jet-threadstats-structure2.md) struct with the specified valued.</span></span>

<span data-ttu-id="e71b8-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e71b8-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="e71b8-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="e71b8-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e71b8-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e71b8-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Function Create ( _
    cPageReferenced As Integer, _
    cPageRead As Integer, _
    cPagePreread As Integer, _
    cPageDirtied As Integer, _
    cPageRedirtied As Integer, _
    cLogRecord As Integer, _
    cbLogRecord As Integer _
) As JET_THREADSTATS
'Usage
Dim cPageReferenced As Integer
Dim cPageRead As Integer
Dim cPagePreread As Integer
Dim cPageDirtied As Integer
Dim cPageRedirtied As Integer
Dim cLogRecord As Integer
Dim cbLogRecord As Integer
Dim returnValue As JET_THREADSTATS

returnValue = JET_THREADSTATS.Create(cPageReferenced, _
    cPageRead, cPagePreread, cPageDirtied, _
    cPageRedirtied, cLogRecord, cbLogRecord)
```

``` csharp
public static JET_THREADSTATS Create(
    int cPageReferenced,
    int cPageRead,
    int cPagePreread,
    int cPageDirtied,
    int cPageRedirtied,
    int cLogRecord,
    int cbLogRecord
)
```

#### <a name="parameters"></a><span data-ttu-id="e71b8-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="e71b8-108">Parameters</span></span>

  - <span data-ttu-id="e71b8-109">cpagereferenziert</span><span class="sxs-lookup"><span data-stu-id="e71b8-109">cPageReferenced</span></span>  
    <span data-ttu-id="e71b8-110">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="e71b8-110">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="e71b8-111">Anzahl der besuchten Seiten.</span><span class="sxs-lookup"><span data-stu-id="e71b8-111">Number of pages visited.</span></span>

<!-- end list -->

  - <span data-ttu-id="e71b8-112">cpageread</span><span class="sxs-lookup"><span data-stu-id="e71b8-112">cPageRead</span></span>  
    <span data-ttu-id="e71b8-113">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="e71b8-113">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="e71b8-114">Anzahl der gelesenen Seiten.</span><span class="sxs-lookup"><span data-stu-id="e71b8-114">Number of pages read.</span></span>

<!-- end list -->

  - <span data-ttu-id="e71b8-115">cpagepreread</span><span class="sxs-lookup"><span data-stu-id="e71b8-115">cPagePreread</span></span>  
    <span data-ttu-id="e71b8-116">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="e71b8-116">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="e71b8-117">Die Anzahl der Seiten, die Voraussetzungen sind.</span><span class="sxs-lookup"><span data-stu-id="e71b8-117">Number of pages preread.</span></span>

<!-- end list -->

  - <span data-ttu-id="e71b8-118">cpagedirtied</span><span class="sxs-lookup"><span data-stu-id="e71b8-118">cPageDirtied</span></span>  
    <span data-ttu-id="e71b8-119">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="e71b8-119">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="e71b8-120">Tnumber der Seiten, für die ein Pfad verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="e71b8-120">TNumber of pages dirtied.</span></span>

<!-- end list -->

  - <span data-ttu-id="e71b8-121">cPageRedirtied</span><span class="sxs-lookup"><span data-stu-id="e71b8-121">cPageRedirtied</span></span>  
    <span data-ttu-id="e71b8-122">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="e71b8-122">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="e71b8-123">Anzahl der Seiten, für die ein erneuter Versuch besteht.</span><span class="sxs-lookup"><span data-stu-id="e71b8-123">Number of pages redirtied.</span></span>

<!-- end list -->

  - <span data-ttu-id="e71b8-124">clogrecord</span><span class="sxs-lookup"><span data-stu-id="e71b8-124">cLogRecord</span></span>  
    <span data-ttu-id="e71b8-125">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="e71b8-125">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="e71b8-126">Anzahl der generierten Protokolldaten Sätze.</span><span class="sxs-lookup"><span data-stu-id="e71b8-126">Number of log records generated.</span></span>

<!-- end list -->

  - <span data-ttu-id="e71b8-127">cblogdatensatz</span><span class="sxs-lookup"><span data-stu-id="e71b8-127">cbLogRecord</span></span>  
    <span data-ttu-id="e71b8-128">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="e71b8-128">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="e71b8-129">Bytes der geschriebenen Protokolldaten Sätze.</span><span class="sxs-lookup"><span data-stu-id="e71b8-129">Bytes of log records written.</span></span>

#### <a name="return-value"></a><span data-ttu-id="e71b8-130">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e71b8-130">Return value</span></span>

<span data-ttu-id="e71b8-131">Typ: [Microsoft.ISAM.ESENT.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="e71b8-131">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span></span>  
<span data-ttu-id="e71b8-132">Eine neue [JET_THREADSTATS](./jet-threadstats-structure2.md) Struktur mit den angegebenen Werten.</span><span class="sxs-lookup"><span data-stu-id="e71b8-132">A new [JET_THREADSTATS](./jet-threadstats-structure2.md) struct with the specified values.</span></span>  

## <a name="see-also"></a><span data-ttu-id="e71b8-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e71b8-133">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e71b8-134">Referenz</span><span class="sxs-lookup"><span data-stu-id="e71b8-134">Reference</span></span>

[<span data-ttu-id="e71b8-135">JET_THREADSTATS Struktur</span><span class="sxs-lookup"><span data-stu-id="e71b8-135">JET_THREADSTATS structure</span></span>](./jet-threadstats-structure2.md)

[<span data-ttu-id="e71b8-136">Mitglieder JET_THREADSTATS</span><span class="sxs-lookup"><span data-stu-id="e71b8-136">JET_THREADSTATS members</span></span>](./jet-threadstats-members.md)

[<span data-ttu-id="e71b8-137">Microsoft. ISAM. ESENT. Interop. Vista-Namespace</span><span class="sxs-lookup"><span data-stu-id="e71b8-137">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
