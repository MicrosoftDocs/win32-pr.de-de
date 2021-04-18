---
description: 'Weitere Informationen finden Sie unter: Windows8Api. jettryprereadindexranges-Methode'
title: Windows8Api. jettryprereadindexranges-Methode (Microsoft. ISAM. ESENT. Interop. Windows8)
TOCTitle: 'JetTryPrereadIndexRanges method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetTryPrereadIndexRanges(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.Windows8.JET_INDEX_RANGE[],System.Int32,System.Int32,System.Int32@,Microsoft.Isam.Esent.Interop.JET_COLUMNID[],Microsoft.Isam.Esent.Interop.Windows8.PrereadIndexRangesGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.windows8api.jettryprereadindexranges(v=EXCHG.10)
ms:contentKeyID: 55104421
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetTryPrereadIndexRanges
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetTryPrereadIndexRanges
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9a9664e658254de057b0e3aa8ae86813eb996a14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106354557"
---
# <a name="windows8apijettryprereadindexranges-method"></a><span data-ttu-id="419ec-103">Windows8Api. jettryprereadindexranges-Methode</span><span class="sxs-lookup"><span data-stu-id="419ec-103">Windows8Api.JetTryPrereadIndexRanges method</span></span>

<span data-ttu-id="419ec-104">Wenn sich die Datensätze mit den angegebenen Schlüsselbereichen nicht im Puffer Cache befinden, starten Sie asynchrone Lesevorgänge, um die Datensätze in den Daten Bank Puffer Cache zu übertragen.</span><span class="sxs-lookup"><span data-stu-id="419ec-104">If the records with the specified key ranges are not in the buffer cache, then start asynchronous reads to bring the records into the database buffer cache.</span></span>

<span data-ttu-id="419ec-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="419ec-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="419ec-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="419ec-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="419ec-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="419ec-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Function JetTryPrereadIndexRanges ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    indexRanges As JET_INDEX_RANGE(), _
    rangeIndex As Integer, _
    rangeCount As Integer, _
    <OutAttribute> ByRef rangesPreread As Integer, _
    columnsPreread As JET_COLUMNID(), _
    grbit As PrereadIndexRangesGrbit _
) As Boolean
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim indexRanges As JET_INDEX_RANGE()
Dim rangeIndex As Integer
Dim rangeCount As Integer
Dim rangesPreread As Integer
Dim columnsPreread As JET_COLUMNID()
Dim grbit As PrereadIndexRangesGrbit
Dim returnValue As Boolean

returnValue = Windows8Api.JetTryPrereadIndexRanges(sesid, _
    tableid, indexRanges, rangeIndex, _
    rangeCount, rangesPreread, columnsPreread, _
    grbit)
```

``` csharp
public static bool JetTryPrereadIndexRanges(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_INDEX_RANGE[] indexRanges,
    int rangeIndex,
    int rangeCount,
    out int rangesPreread,
    JET_COLUMNID[] columnsPreread,
    PrereadIndexRangesGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="419ec-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="419ec-108">Parameters</span></span>

  - <span data-ttu-id="419ec-109">-sid</span><span class="sxs-lookup"><span data-stu-id="419ec-109">sesid</span></span>  
    <span data-ttu-id="419ec-110">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="419ec-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="419ec-111">Die zu verwendende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="419ec-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="419ec-112">TableID</span><span class="sxs-lookup"><span data-stu-id="419ec-112">tableid</span></span>  
    <span data-ttu-id="419ec-113">Typ: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="419ec-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="419ec-114">Die Tabelle, für die die prereads ausgestellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="419ec-114">The table to issue the prereads against.</span></span>

<!-- end list -->

  - <span data-ttu-id="419ec-115">Indexbereiche</span><span class="sxs-lookup"><span data-stu-id="419ec-115">indexRanges</span></span>  
    <span data-ttu-id="419ec-116">Sorte \[\]</span><span class="sxs-lookup"><span data-stu-id="419ec-116">Type: \[\]</span></span>  
    
    <span data-ttu-id="419ec-117">Die Schlüsselbereiche für die Voraussetzungen.</span><span class="sxs-lookup"><span data-stu-id="419ec-117">The key ranges to preread.</span></span>

<!-- end list -->

  - <span data-ttu-id="419ec-118">rangeIndex</span><span class="sxs-lookup"><span data-stu-id="419ec-118">rangeIndex</span></span>  
    <span data-ttu-id="419ec-119">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="419ec-119">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="419ec-120">Der Index des ersten zu lesenden Schlüsselbereichs im Array.</span><span class="sxs-lookup"><span data-stu-id="419ec-120">The index of the first key range in the array to read.</span></span>

<!-- end list -->

  - <span data-ttu-id="419ec-121">rangecount</span><span class="sxs-lookup"><span data-stu-id="419ec-121">rangeCount</span></span>  
    <span data-ttu-id="419ec-122">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="419ec-122">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="419ec-123">Die maximale Anzahl von Schlüsselbereichen, die Voraussetzungen für die Voraussetzungen sind.</span><span class="sxs-lookup"><span data-stu-id="419ec-123">The maximum number of key ranges to preread.</span></span>

<!-- end list -->

  - <span data-ttu-id="419ec-124">rangespreread</span><span class="sxs-lookup"><span data-stu-id="419ec-124">rangesPreread</span></span>  
    <span data-ttu-id="419ec-125">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="419ec-125">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="419ec-126">Gibt die Anzahl der Schlüssel zurück, die tatsächlich vorab registriert werden.</span><span class="sxs-lookup"><span data-stu-id="419ec-126">Returns the number of keys actually preread.</span></span>

<!-- end list -->

  - <span data-ttu-id="419ec-127">columnspreread</span><span class="sxs-lookup"><span data-stu-id="419ec-127">columnsPreread</span></span>  
    <span data-ttu-id="419ec-128">Sorte \[\]</span><span class="sxs-lookup"><span data-stu-id="419ec-128">Type: \[\]</span></span>  
    
    <span data-ttu-id="419ec-129">Liste der Spalten-IDs für lange Wert Spalten, die vorab registriert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="419ec-129">List of column ids for long value columns to preread.</span></span>

<!-- end list -->

  - <span data-ttu-id="419ec-130">grbit</span><span class="sxs-lookup"><span data-stu-id="419ec-130">grbit</span></span>  
    <span data-ttu-id="419ec-131">Typ: [Microsoft. ISAM. ESENT. Interop. Windows8. prereadindexrangesgrbit](./prereadindexrangesgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="419ec-131">Type: [Microsoft.Isam.Esent.Interop.Windows8.PrereadIndexRangesGrbit](./prereadindexrangesgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="419ec-132">Preread-Optionen.</span><span class="sxs-lookup"><span data-stu-id="419ec-132">Preread options.</span></span> <span data-ttu-id="419ec-133">Wird verwendet, um die Richtung der Preread anzugeben.</span><span class="sxs-lookup"><span data-stu-id="419ec-133">Used to specify the direction of the preread.</span></span>

#### <a name="return-value"></a><span data-ttu-id="419ec-134">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="419ec-134">Return value</span></span>

<span data-ttu-id="419ec-135">Typ: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="419ec-135">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="419ec-136">**\[ true \]** , wenn einige Voraussetzungen erfüllt sind, andernfalls **\[ false \]** .</span><span class="sxs-lookup"><span data-stu-id="419ec-136">**\[true\]** if some preread done, **\[false\]** otherwise.</span></span>  

## <a name="see-also"></a><span data-ttu-id="419ec-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="419ec-137">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="419ec-138">Referenz</span><span class="sxs-lookup"><span data-stu-id="419ec-138">Reference</span></span>

[<span data-ttu-id="419ec-139">Windows8Api-Klasse</span><span class="sxs-lookup"><span data-stu-id="419ec-139">Windows8Api class</span></span>](./windows8api-class.md)

[<span data-ttu-id="419ec-140">Windows8Api-Member</span><span class="sxs-lookup"><span data-stu-id="419ec-140">Windows8Api members</span></span>](./windows8api-members.md)

[<span data-ttu-id="419ec-141">Microsoft. ISAM. ESENT. Interop. Windows8-Namespace</span><span class="sxs-lookup"><span data-stu-id="419ec-141">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
