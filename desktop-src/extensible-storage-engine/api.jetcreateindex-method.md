---
description: Weitere Informationen finden Sie in der API. jetkreateingedex-Methode.
title: API. jetkreateingedex-Methode
TOCTitle: 'JetCreateIndex method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetCreateIndex(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.String,Microsoft.Isam.Esent.Interop.CreateIndexGrbit,System.String,System.Int32,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetcreateindex(v=EXCHG.10)
ms:contentKeyID: 55100693
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetCreateIndex
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetCreateIndex
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a9b3549461324f396408bb7d370531907248e8c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106339768"
---
# <a name="apijetcreateindex-method"></a><span data-ttu-id="b8e37-103">API. jetkreateingedex-Methode</span><span class="sxs-lookup"><span data-stu-id="b8e37-103">Api.JetCreateIndex method</span></span>

<span data-ttu-id="b8e37-104">Erstellt einen Index über Daten in einer ESE-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="b8e37-104">Creates an index over data in an ESE database.</span></span> <span data-ttu-id="b8e37-105">Ein Index kann verwendet werden, um bestimmte Daten schnell zu suchen.</span><span class="sxs-lookup"><span data-stu-id="b8e37-105">An index can be used to locate specific data quickly.</span></span>

<span data-ttu-id="b8e37-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b8e37-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="b8e37-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="b8e37-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b8e37-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="b8e37-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetCreateIndex ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    indexName As String, _
    grbit As CreateIndexGrbit, _
    keyDescription As String, _
    keyDescriptionLength As Integer, _
    density As Integer _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim indexName As String
Dim grbit As CreateIndexGrbit
Dim keyDescription As String
Dim keyDescriptionLength As Integer
Dim density As IntegerApi.JetCreateIndex(sesid, tableid, _
    indexName, grbit, keyDescription, _
    keyDescriptionLength, density)
```

``` csharp
public static void JetCreateIndex(
    JET_SESID sesid,
    JET_TABLEID tableid,
    string indexName,
    CreateIndexGrbit grbit,
    string keyDescription,
    int keyDescriptionLength,
    int density
)
```

#### <a name="parameters"></a><span data-ttu-id="b8e37-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="b8e37-109">Parameters</span></span>

  - <span data-ttu-id="b8e37-110">-sid</span><span class="sxs-lookup"><span data-stu-id="b8e37-110">sesid</span></span>  
    <span data-ttu-id="b8e37-111">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="b8e37-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="b8e37-112">Die zu verwendende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="b8e37-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="b8e37-113">TableID</span><span class="sxs-lookup"><span data-stu-id="b8e37-113">tableid</span></span>  
    <span data-ttu-id="b8e37-114">Typ: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="b8e37-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="b8e37-115">Die Tabelle, für die der Index erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="b8e37-115">The table to create the index on.</span></span>

<!-- end list -->

  - <span data-ttu-id="b8e37-116">indexName</span><span class="sxs-lookup"><span data-stu-id="b8e37-116">indexName</span></span>  
    <span data-ttu-id="b8e37-117">Typ: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="b8e37-117">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="b8e37-118">Ein Zeiger auf eine mit NULL endenden Zeichenfolge, die den Namen des zu erstellenden Indexes angibt.</span><span class="sxs-lookup"><span data-stu-id="b8e37-118">Pointer to a null-terminated string that specifies the name of the index to create.</span></span>

<!-- end list -->

  - <span data-ttu-id="b8e37-119">grbit</span><span class="sxs-lookup"><span data-stu-id="b8e37-119">grbit</span></span>  
    <span data-ttu-id="b8e37-120">Typ: [Microsoft. ISAM. ESENT. Interop. kreateindexgrbit](./createindexgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="b8e37-120">Type: [Microsoft.Isam.Esent.Interop.CreateIndexGrbit](./createindexgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="b8e37-121">Index Erstellungs Optionen.</span><span class="sxs-lookup"><span data-stu-id="b8e37-121">Index creation options.</span></span>

<!-- end list -->

  - <span data-ttu-id="b8e37-122">keydescription</span><span class="sxs-lookup"><span data-stu-id="b8e37-122">keyDescription</span></span>  
    <span data-ttu-id="b8e37-123">Typ: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="b8e37-123">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="b8e37-124">Zeiger auf eine Double-NULL-terminierte Zeichenfolge von NULL-getrennten Token.</span><span class="sxs-lookup"><span data-stu-id="b8e37-124">Pointer to a double null-terminated string of null-delimited tokens.</span></span>

<!-- end list -->

  - <span data-ttu-id="b8e37-125">keydescriptionlength</span><span class="sxs-lookup"><span data-stu-id="b8e37-125">keyDescriptionLength</span></span>  
    <span data-ttu-id="b8e37-126">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="b8e37-126">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="b8e37-127">Die Länge von szkey (in Zeichen), einschließlich der beiden abschließenden Nullen.</span><span class="sxs-lookup"><span data-stu-id="b8e37-127">The length, in characters, of szKey including the two terminating nulls.</span></span>

<!-- end list -->

  - <span data-ttu-id="b8e37-128">Dichte (density)</span><span class="sxs-lookup"><span data-stu-id="b8e37-128">density</span></span>  
    <span data-ttu-id="b8e37-129">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="b8e37-129">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="b8e37-130">Anfängliche B +-Struktur Dichte.</span><span class="sxs-lookup"><span data-stu-id="b8e37-130">Initial B+ tree density.</span></span>

## <a name="see-also"></a><span data-ttu-id="b8e37-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b8e37-131">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b8e37-132">Referenz</span><span class="sxs-lookup"><span data-stu-id="b8e37-132">Reference</span></span>

[<span data-ttu-id="b8e37-133">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="b8e37-133">Api class</span></span>](./api-class.md)

[<span data-ttu-id="b8e37-134">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="b8e37-134">Api members</span></span>](./api-members.md)

[<span data-ttu-id="b8e37-135">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="b8e37-135">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
