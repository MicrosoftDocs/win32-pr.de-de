---
description: 'Weitere Informationen finden Sie hier: API. jetgodesecondaryindexbookmark-Methode'
title: API. jetgodesecondaryindexbookmark-Methode
TOCTitle: 'JetGotoSecondaryIndexBookmark method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGotoSecondaryIndexBookmark(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Byte[],System.Int32,System.Byte[],System.Int32,Microsoft.Isam.Esent.Interop.GotoSecondaryIndexBookmarkGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgotosecondaryindexbookmark(v=EXCHG.10)
ms:contentKeyID: 55100755
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGotoSecondaryIndexBookmark
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGotoSecondaryIndexBookmark
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: af146236a2a5398dfb0b7b81f42dcfc6227a6de9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359569"
---
# <a name="apijetgotosecondaryindexbookmark-method"></a><span data-ttu-id="68854-103">API. jetgodesecondaryindexbookmark-Methode</span><span class="sxs-lookup"><span data-stu-id="68854-103">Api.JetGotoSecondaryIndexBookmark method</span></span>

<span data-ttu-id="68854-104">Positioniert einen Cursor auf einen Index Eintrag, der dem angegebenen sekundären Index Lesezeichen zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="68854-104">Positions a cursor to an index entry that is associated with the specified secondary index bookmark.</span></span> <span data-ttu-id="68854-105">Das sekundäre Index Lesezeichen muss mit demselben Index für dieselbe Tabelle verwendet werden, aus der es ursprünglich abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="68854-105">The secondary index bookmark must be used with the same index over the same table from which it was originally retrieved.</span></span> <span data-ttu-id="68854-106">Das sekundäre Index Lesezeichen für einen Index Eintrag kann mithilfe von jetgoessecondaryindexbookmark (JET_SESID, JET_TABLEID, \[ \] , Int32, \[ \] , Int32, GOTO secondaryindexbookmarkgrbit) abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="68854-106">The secondary index bookmark for an index entry can be retrieved using JetGotoSecondaryIndexBookmark(JET_SESID, JET_TABLEID, \[\], Int32, \[\], Int32, GotoSecondaryIndexBookmarkGrbit).</span></span>

<span data-ttu-id="68854-107">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="68854-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="68854-108">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="68854-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="68854-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="68854-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGotoSecondaryIndexBookmark ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    secondaryKey As Byte(), _
    secondaryKeySize As Integer, _
    primaryKey As Byte(), _
    primaryKeySize As Integer, _
    grbit As GotoSecondaryIndexBookmarkGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim secondaryKey As Byte()
Dim secondaryKeySize As Integer
Dim primaryKey As Byte()
Dim primaryKeySize As Integer
Dim grbit As GotoSecondaryIndexBookmarkGrbitApi.JetGotoSecondaryIndexBookmark(sesid, _
    tableid, secondaryKey, secondaryKeySize, _
    primaryKey, primaryKeySize, grbit)
```

``` csharp
public static void JetGotoSecondaryIndexBookmark(
    JET_SESID sesid,
    JET_TABLEID tableid,
    byte[] secondaryKey,
    int secondaryKeySize,
    byte[] primaryKey,
    int primaryKeySize,
    GotoSecondaryIndexBookmarkGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="68854-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="68854-110">Parameters</span></span>

  - <span data-ttu-id="68854-111">-sid</span><span class="sxs-lookup"><span data-stu-id="68854-111">sesid</span></span>  
    <span data-ttu-id="68854-112">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="68854-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="68854-113">Die zu verwendende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="68854-113">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="68854-114">TableID</span><span class="sxs-lookup"><span data-stu-id="68854-114">tableid</span></span>  
    <span data-ttu-id="68854-115">Typ: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="68854-115">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="68854-116">Der zu positiongende Tabellen Cursor.</span><span class="sxs-lookup"><span data-stu-id="68854-116">The table cursor to position.</span></span>

<!-- end list -->

  - <span data-ttu-id="68854-117">secondaryKey</span><span class="sxs-lookup"><span data-stu-id="68854-117">secondaryKey</span></span>  
    <span data-ttu-id="68854-118">Sorte \[\]</span><span class="sxs-lookup"><span data-stu-id="68854-118">Type: \[\]</span></span>  
    
    <span data-ttu-id="68854-119">Der Puffer, der den sekundären Schlüssel enthält.</span><span class="sxs-lookup"><span data-stu-id="68854-119">The buffer that contains the secondary key.</span></span>

<!-- end list -->

  - <span data-ttu-id="68854-120">secondarykeysize</span><span class="sxs-lookup"><span data-stu-id="68854-120">secondaryKeySize</span></span>  
    <span data-ttu-id="68854-121">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="68854-121">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="68854-122">Die Größe des sekundären Schlüssels.</span><span class="sxs-lookup"><span data-stu-id="68854-122">The size of the secondary key.</span></span>

<!-- end list -->

  - <span data-ttu-id="68854-123">primaryKey</span><span class="sxs-lookup"><span data-stu-id="68854-123">primaryKey</span></span>  
    <span data-ttu-id="68854-124">Sorte \[\]</span><span class="sxs-lookup"><span data-stu-id="68854-124">Type: \[\]</span></span>  
    
    <span data-ttu-id="68854-125">Der Puffer, der den Primärschlüssel enthält.</span><span class="sxs-lookup"><span data-stu-id="68854-125">The buffer that contains the primary key.</span></span>

<!-- end list -->

  - <span data-ttu-id="68854-126">primarykeysize</span><span class="sxs-lookup"><span data-stu-id="68854-126">primaryKeySize</span></span>  
    <span data-ttu-id="68854-127">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="68854-127">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="68854-128">Die Größe des Primärschlüssels.</span><span class="sxs-lookup"><span data-stu-id="68854-128">The size of the primary key.</span></span>

<!-- end list -->

  - <span data-ttu-id="68854-129">grbit</span><span class="sxs-lookup"><span data-stu-id="68854-129">grbit</span></span>  
    <span data-ttu-id="68854-130">Typ: [Microsoft. ISAM. ESENT. Interop. goessecondaryindexbookmarkgrbit](./gotosecondaryindexbookmarkgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="68854-130">Type: [Microsoft.Isam.Esent.Interop.GotoSecondaryIndexBookmarkGrbit](./gotosecondaryindexbookmarkgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="68854-131">Optionen zum Positionieren des Lesezeichens.</span><span class="sxs-lookup"><span data-stu-id="68854-131">Options for positioning the bookmark.</span></span>

## <a name="see-also"></a><span data-ttu-id="68854-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="68854-132">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="68854-133">Referenz</span><span class="sxs-lookup"><span data-stu-id="68854-133">Reference</span></span>

[<span data-ttu-id="68854-134">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="68854-134">Api class</span></span>](./api-class.md)

[<span data-ttu-id="68854-135">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="68854-135">Api members</span></span>](./api-members.md)

[<span data-ttu-id="68854-136">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="68854-136">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
