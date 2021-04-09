---
description: 'Weitere Informationen finden Sie unter: Windows8Api. prereadkeyranges-Methode'
title: Windows8Api. prereadkeyranges-Methode (Microsoft. ISAM. ESENT. Interop. Windows8)
TOCTitle: 'PrereadKeyRanges method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.PrereadKeyRanges(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Byte[][],System.Int32[],System.Byte[][],System.Int32[],System.Int32,System.Int32,System.Int32@,Microsoft.Isam.Esent.Interop.JET_COLUMNID[],Microsoft.Isam.Esent.Interop.Windows8.PrereadIndexRangesGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.windows8api.prereadkeyranges(v=EXCHG.10)
ms:contentKeyID: 55104465
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.PrereadKeyRanges
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.PrereadKeyRanges
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 091c1f92512fd9a55bb4acd4d824567acc19fdde
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959197"
---
# <a name="windows8apiprereadkeyranges-method"></a><span data-ttu-id="369af-103">Windows8Api. prereadkeyranges-Methode</span><span class="sxs-lookup"><span data-stu-id="369af-103">Windows8Api.PrereadKeyRanges method</span></span>

<span data-ttu-id="369af-104">Wenn sich die Datensätze mit den angegebenen Schlüsselbereichen nicht im Puffer Cache befinden, starten Sie asynchrone Lesevorgänge, um die Datensätze in den Daten Bank Puffer Cache zu übertragen.</span><span class="sxs-lookup"><span data-stu-id="369af-104">If the records with the specified key ranges are not in the buffer cache then start asynchronous reads to bring the records into the database buffer cache.</span></span>

<span data-ttu-id="369af-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="369af-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="369af-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="369af-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="369af-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="369af-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub PrereadKeyRanges ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    keysStart As Byte()(), _
    keyStartLengths As Integer(), _
    keysEnd As Byte()(), _
    keyEndLengths As Integer(), _
    rangeIndex As Integer, _
    rangeCount As Integer, _
    <OutAttribute> ByRef rangesPreread As Integer, _
    columnsPreread As JET_COLUMNID(), _
    grbit As PrereadIndexRangesGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim keysStart As Byte()()
Dim keyStartLengths As Integer()
Dim keysEnd As Byte()()
Dim keyEndLengths As Integer()
Dim rangeIndex As Integer
Dim rangeCount As Integer
Dim rangesPreread As Integer
Dim columnsPreread As JET_COLUMNID()
Dim grbit As PrereadIndexRangesGrbitWindows8Api.PrereadKeyRanges(sesid, tableid, _
    keysStart, keyStartLengths, keysEnd, _
    keyEndLengths, rangeIndex, rangeCount, _
    rangesPreread, columnsPreread, grbit)
```

``` csharp
public static void PrereadKeyRanges(
    JET_SESID sesid,
    JET_TABLEID tableid,
    byte[][] keysStart,
    int[] keyStartLengths,
    byte[][] keysEnd,
    int[] keyEndLengths,
    int rangeIndex,
    int rangeCount,
    out int rangesPreread,
    JET_COLUMNID[] columnsPreread,
    PrereadIndexRangesGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="369af-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="369af-108">Parameters</span></span>

  - <span data-ttu-id="369af-109">-sid</span><span class="sxs-lookup"><span data-stu-id="369af-109">sesid</span></span>  
    <span data-ttu-id="369af-110">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="369af-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="369af-111">Die zu verwendende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="369af-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="369af-112">TableID</span><span class="sxs-lookup"><span data-stu-id="369af-112">tableid</span></span>  
    <span data-ttu-id="369af-113">Typ: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="369af-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="369af-114">Die Tabelle, für die die prereads ausgestellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="369af-114">The table to issue the prereads against.</span></span>

<!-- end list -->

  - <span data-ttu-id="369af-115">keysstart</span><span class="sxs-lookup"><span data-stu-id="369af-115">keysStart</span></span>  
    <span data-ttu-id="369af-116">Sorte \[\]</span><span class="sxs-lookup"><span data-stu-id="369af-116">Type: \[\]</span></span>  
    
    <span data-ttu-id="369af-117">Der Anfang der Schlüsselbereiche, die Voraussetzungen für die Voraussetzungen sind.</span><span class="sxs-lookup"><span data-stu-id="369af-117">The start of key ranges to preread.</span></span>

<!-- end list -->

  - <span data-ttu-id="369af-118">keystartlängen</span><span class="sxs-lookup"><span data-stu-id="369af-118">keyStartLengths</span></span>  
    <span data-ttu-id="369af-119">Sorte \[\]</span><span class="sxs-lookup"><span data-stu-id="369af-119">Type: \[\]</span></span>  
    
    <span data-ttu-id="369af-120">Die Längen der Start Tasten, die Voraussetzungen sind.</span><span class="sxs-lookup"><span data-stu-id="369af-120">The lengths of the start keys to preread.</span></span>

<!-- end list -->

  - <span data-ttu-id="369af-121">keysend</span><span class="sxs-lookup"><span data-stu-id="369af-121">keysEnd</span></span>  
    <span data-ttu-id="369af-122">Sorte \[\]</span><span class="sxs-lookup"><span data-stu-id="369af-122">Type: \[\]</span></span>  
    
    <span data-ttu-id="369af-123">Das Ende des rangess-Schlüssels, der sich im Voraus registriert.</span><span class="sxs-lookup"><span data-stu-id="369af-123">The end of key rangess to preread.</span></span>

<!-- end list -->

  - <span data-ttu-id="369af-124">keyendlängen</span><span class="sxs-lookup"><span data-stu-id="369af-124">keyEndLengths</span></span>  
    <span data-ttu-id="369af-125">Sorte \[\]</span><span class="sxs-lookup"><span data-stu-id="369af-125">Type: \[\]</span></span>  
    
    <span data-ttu-id="369af-126">Die Länge der zu Preread enden Endschlüssel.</span><span class="sxs-lookup"><span data-stu-id="369af-126">The lengths of the end keys to preread.</span></span>

<!-- end list -->

  - <span data-ttu-id="369af-127">rangeIndex</span><span class="sxs-lookup"><span data-stu-id="369af-127">rangeIndex</span></span>  
    <span data-ttu-id="369af-128">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="369af-128">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="369af-129">Der Index des ersten zu lesenden Schlüsselbereichs im Array.</span><span class="sxs-lookup"><span data-stu-id="369af-129">The index of the first key range in the array to read.</span></span>

<!-- end list -->

  - <span data-ttu-id="369af-130">rangecount</span><span class="sxs-lookup"><span data-stu-id="369af-130">rangeCount</span></span>  
    <span data-ttu-id="369af-131">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="369af-131">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="369af-132">Die maximale Anzahl von Schlüsselbereichen, die Voraussetzungen für die Voraussetzungen sind.</span><span class="sxs-lookup"><span data-stu-id="369af-132">The maximum number of key ranges to preread.</span></span>

<!-- end list -->

  - <span data-ttu-id="369af-133">rangespreread</span><span class="sxs-lookup"><span data-stu-id="369af-133">rangesPreread</span></span>  
    <span data-ttu-id="369af-134">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="369af-134">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="369af-135">Gibt die Anzahl der Schlüssel zurück, die tatsächlich vorab registriert werden.</span><span class="sxs-lookup"><span data-stu-id="369af-135">Returns the number of keys actually preread.</span></span>

<!-- end list -->

  - <span data-ttu-id="369af-136">columnspreread</span><span class="sxs-lookup"><span data-stu-id="369af-136">columnsPreread</span></span>  
    <span data-ttu-id="369af-137">Sorte \[\]</span><span class="sxs-lookup"><span data-stu-id="369af-137">Type: \[\]</span></span>  
    
    <span data-ttu-id="369af-138">Liste der Spalten-IDs für lange Wert Spalten, die vorab registriert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="369af-138">List of column ids for long value columns to preread.</span></span>

<!-- end list -->

  - <span data-ttu-id="369af-139">grbit</span><span class="sxs-lookup"><span data-stu-id="369af-139">grbit</span></span>  
    <span data-ttu-id="369af-140">Typ: [Microsoft. ISAM. ESENT. Interop. Windows8. prereadindexrangesgrbit](./prereadindexrangesgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="369af-140">Type: [Microsoft.Isam.Esent.Interop.Windows8.PrereadIndexRangesGrbit](./prereadindexrangesgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="369af-141">Preread-Optionen.</span><span class="sxs-lookup"><span data-stu-id="369af-141">Preread options.</span></span> <span data-ttu-id="369af-142">Wird verwendet, um die Richtung der Preread anzugeben.</span><span class="sxs-lookup"><span data-stu-id="369af-142">Used to specify the direction of the preread.</span></span>

## <a name="see-also"></a><span data-ttu-id="369af-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="369af-143">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="369af-144">Referenz</span><span class="sxs-lookup"><span data-stu-id="369af-144">Reference</span></span>

[<span data-ttu-id="369af-145">Windows8Api-Klasse</span><span class="sxs-lookup"><span data-stu-id="369af-145">Windows8Api class</span></span>](./windows8api-class.md)

[<span data-ttu-id="369af-146">Windows8Api-Member</span><span class="sxs-lookup"><span data-stu-id="369af-146">Windows8Api members</span></span>](./windows8api-members.md)

[<span data-ttu-id="369af-147">Microsoft. ISAM. ESENT. Interop. Windows8-Namespace</span><span class="sxs-lookup"><span data-stu-id="369af-147">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
