---
description: 'Weitere Informationen finden Sie hier: API. jetgetsecondaryindexbookmark-Methode'
title: API. jetgetsecondaryindexbookmark-Methode
TOCTitle: 'JetGetSecondaryIndexBookmark method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetSecondaryIndexBookmark(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Byte[],System.Int32,System.Int32@,System.Byte[],System.Int32,System.Int32@,Microsoft.Isam.Esent.Interop.GetSecondaryIndexBookmarkGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetsecondaryindexbookmark(v=EXCHG.10)
ms:contentKeyID: 55100725
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGetSecondaryIndexBookmark
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetSecondaryIndexBookmark
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b0a25e78ca291271a96d06e5c0bf61c691acd4de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041656"
---
# <a name="apijetgetsecondaryindexbookmark-method"></a><span data-ttu-id="eb78e-103">API. jetgetsecondaryindexbookmark-Methode</span><span class="sxs-lookup"><span data-stu-id="eb78e-103">Api.JetGetSecondaryIndexBookmark method</span></span>

<span data-ttu-id="eb78e-104">Ruft ein spezielles Lesezeichen für den sekundären Index Eintrag an der aktuellen Position eines Cursors ab.</span><span class="sxs-lookup"><span data-stu-id="eb78e-104">Retrieves a special bookmark for the secondary index entry at the current position of a cursor.</span></span> <span data-ttu-id="eb78e-105">Dieses Lesezeichen kann dann verwendet werden, um den Cursor mithilfe von jetgoysecondaryindexbookmark effizient wieder in denselben Index Eintrag zu positionieren.</span><span class="sxs-lookup"><span data-stu-id="eb78e-105">This bookmark can then be used to efficiently reposition that cursor back to the same index entry using JetGotoSecondaryIndexBookmark.</span></span> <span data-ttu-id="eb78e-106">Dies ist besonders nützlich, wenn Sie einen sekundären Index neu positionieren, der doppelte Schlüssel enthält oder mehrere Indexeinträge für denselben Datensatz enthält.</span><span class="sxs-lookup"><span data-stu-id="eb78e-106">This is most useful when repositioning on a secondary index that contains duplicate keys or that contains multiple index entries for the same record.</span></span>

<span data-ttu-id="eb78e-107">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="eb78e-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="eb78e-108">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="eb78e-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="eb78e-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="eb78e-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetSecondaryIndexBookmark ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    secondaryKey As Byte(), _
    secondaryKeySize As Integer, _
    <OutAttribute> ByRef actualSecondaryKeySize As Integer, _
    primaryKey As Byte(), _
    primaryKeySize As Integer, _
    <OutAttribute> ByRef actualPrimaryKeySize As Integer, _
    grbit As GetSecondaryIndexBookmarkGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim secondaryKey As Byte()
Dim secondaryKeySize As Integer
Dim actualSecondaryKeySize As Integer
Dim primaryKey As Byte()
Dim primaryKeySize As Integer
Dim actualPrimaryKeySize As Integer
Dim grbit As GetSecondaryIndexBookmarkGrbitApi.JetGetSecondaryIndexBookmark(sesid, _
    tableid, secondaryKey, secondaryKeySize, _
    actualSecondaryKeySize, primaryKey, _
    primaryKeySize, actualPrimaryKeySize, _
    grbit)
```

``` csharp
public static void JetGetSecondaryIndexBookmark(
    JET_SESID sesid,
    JET_TABLEID tableid,
    byte[] secondaryKey,
    int secondaryKeySize,
    out int actualSecondaryKeySize,
    byte[] primaryKey,
    int primaryKeySize,
    out int actualPrimaryKeySize,
    GetSecondaryIndexBookmarkGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="eb78e-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="eb78e-110">Parameters</span></span>

  - <span data-ttu-id="eb78e-111">-sid</span><span class="sxs-lookup"><span data-stu-id="eb78e-111">sesid</span></span>  
    <span data-ttu-id="eb78e-112">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="eb78e-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="eb78e-113">Die zu verwendende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="eb78e-113">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="eb78e-114">TableID</span><span class="sxs-lookup"><span data-stu-id="eb78e-114">tableid</span></span>  
    <span data-ttu-id="eb78e-115">Typ: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="eb78e-115">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="eb78e-116">Der Cursor, von dem das Lesezeichen abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="eb78e-116">The cursor to retrieve the bookmark from.</span></span>

<!-- end list -->

  - <span data-ttu-id="eb78e-117">secondaryKey</span><span class="sxs-lookup"><span data-stu-id="eb78e-117">secondaryKey</span></span>  
    <span data-ttu-id="eb78e-118">Sorte \[\]</span><span class="sxs-lookup"><span data-stu-id="eb78e-118">Type: \[\]</span></span>  
    
    <span data-ttu-id="eb78e-119">Ausgabepuffer für den sekundären Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="eb78e-119">Output buffer for the secondary key.</span></span>

<!-- end list -->

  - <span data-ttu-id="eb78e-120">secondarykeysize</span><span class="sxs-lookup"><span data-stu-id="eb78e-120">secondaryKeySize</span></span>  
    <span data-ttu-id="eb78e-121">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="eb78e-121">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="eb78e-122">Größe des sekundären Schlüssel Puffers.</span><span class="sxs-lookup"><span data-stu-id="eb78e-122">Size of the secondary key buffer.</span></span>

<!-- end list -->

  - <span data-ttu-id="eb78e-123">actualsecondarykeysize</span><span class="sxs-lookup"><span data-stu-id="eb78e-123">actualSecondaryKeySize</span></span>  
    <span data-ttu-id="eb78e-124">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="eb78e-124">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="eb78e-125">Gibt die Größe des sekundären Schlüssels zurück.</span><span class="sxs-lookup"><span data-stu-id="eb78e-125">Returns the size of the secondary key.</span></span>

<!-- end list -->

  - <span data-ttu-id="eb78e-126">primaryKey</span><span class="sxs-lookup"><span data-stu-id="eb78e-126">primaryKey</span></span>  
    <span data-ttu-id="eb78e-127">Sorte \[\]</span><span class="sxs-lookup"><span data-stu-id="eb78e-127">Type: \[\]</span></span>  
    
    <span data-ttu-id="eb78e-128">Ausgabepuffer für den Primärschlüssel.</span><span class="sxs-lookup"><span data-stu-id="eb78e-128">Output buffer for the primary key.</span></span>

<!-- end list -->

  - <span data-ttu-id="eb78e-129">primarykeysize</span><span class="sxs-lookup"><span data-stu-id="eb78e-129">primaryKeySize</span></span>  
    <span data-ttu-id="eb78e-130">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="eb78e-130">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="eb78e-131">Größe des Primärschlüssel Puffers.</span><span class="sxs-lookup"><span data-stu-id="eb78e-131">Size of the primary key buffer.</span></span>

<!-- end list -->

  - <span data-ttu-id="eb78e-132">actualprimarykeysize</span><span class="sxs-lookup"><span data-stu-id="eb78e-132">actualPrimaryKeySize</span></span>  
    <span data-ttu-id="eb78e-133">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="eb78e-133">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="eb78e-134">Gibt die Größe des Primärschlüssels zurück.</span><span class="sxs-lookup"><span data-stu-id="eb78e-134">Returns the size of the primary key.</span></span>

<!-- end list -->

  - <span data-ttu-id="eb78e-135">grbit</span><span class="sxs-lookup"><span data-stu-id="eb78e-135">grbit</span></span>  
    <span data-ttu-id="eb78e-136">Typ: [Microsoft. ISAM. ESENT. Interop. getsecondaryindexbookmarkgrbit](./getsecondaryindexbookmarkgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="eb78e-136">Type: [Microsoft.Isam.Esent.Interop.GetSecondaryIndexBookmarkGrbit](./getsecondaryindexbookmarkgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="eb78e-137">Optionen für den-Befehl.</span><span class="sxs-lookup"><span data-stu-id="eb78e-137">Options for the call.</span></span>

## <a name="see-also"></a><span data-ttu-id="eb78e-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eb78e-138">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="eb78e-139">Referenz</span><span class="sxs-lookup"><span data-stu-id="eb78e-139">Reference</span></span>

[<span data-ttu-id="eb78e-140">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="eb78e-140">Api class</span></span>](./api-class.md)

[<span data-ttu-id="eb78e-141">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="eb78e-141">Api members</span></span>](./api-members.md)

[<span data-ttu-id="eb78e-142">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="eb78e-142">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
