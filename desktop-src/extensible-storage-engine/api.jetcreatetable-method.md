---
description: Weitere Informationen finden Sie in der API. jetkreatetable-Methode.
title: API. jetkreatetable-Methode
TOCTitle: 'JetCreateTable method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetCreateTable(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String,System.Int32,System.Int32,Microsoft.Isam.Esent.Interop.JET_TABLEID@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetcreatetable(v=EXCHG.10)
ms:contentKeyID: 55100676
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetCreateTable
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetCreateTable
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8025e35746d921fda3b601d289a9b361aefefb83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484539"
---
# <a name="apijetcreatetable-method"></a><span data-ttu-id="e3fb5-103">API. jetkreatetable-Methode</span><span class="sxs-lookup"><span data-stu-id="e3fb5-103">Api.JetCreateTable method</span></span>

<span data-ttu-id="e3fb5-104">Erstellen Sie eine leere Tabelle.</span><span class="sxs-lookup"><span data-stu-id="e3fb5-104">Create an empty table.</span></span> <span data-ttu-id="e3fb5-105">Die neu erstellte Tabelle wird exklusiv geöffnet.</span><span class="sxs-lookup"><span data-stu-id="e3fb5-105">The newly created table is opened exclusively.</span></span>

<span data-ttu-id="e3fb5-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e3fb5-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="e3fb5-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="e3fb5-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e3fb5-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="e3fb5-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetCreateTable ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    table As String, _
    pages As Integer, _
    density As Integer, _
    <OutAttribute> ByRef tableid As JET_TABLEID _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim table As String
Dim pages As Integer
Dim density As Integer
Dim tableid As JET_TABLEIDApi.JetCreateTable(sesid, dbid, _
    table, pages, density, tableid)
```

``` csharp
public static void JetCreateTable(
    JET_SESID sesid,
    JET_DBID dbid,
    string table,
    int pages,
    int density,
    out JET_TABLEID tableid
)
```

#### <a name="parameters"></a><span data-ttu-id="e3fb5-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="e3fb5-109">Parameters</span></span>

  - <span data-ttu-id="e3fb5-110">-sid</span><span class="sxs-lookup"><span data-stu-id="e3fb5-110">sesid</span></span>  
    <span data-ttu-id="e3fb5-111">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="e3fb5-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="e3fb5-112">Die zu verwendende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="e3fb5-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="e3fb5-113">dbid</span><span class="sxs-lookup"><span data-stu-id="e3fb5-113">dbid</span></span>  
    <span data-ttu-id="e3fb5-114">Typ: [Microsoft.ISAM.ESENT.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="e3fb5-114">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="e3fb5-115">Die Datenbank, in der die Tabelle erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="e3fb5-115">The database to create the table in.</span></span>

<!-- end list -->

  - <span data-ttu-id="e3fb5-116">table</span><span class="sxs-lookup"><span data-stu-id="e3fb5-116">table</span></span>  
    <span data-ttu-id="e3fb5-117">Typ: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="e3fb5-117">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="e3fb5-118">Der Name der zu erstellenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="e3fb5-118">The name of the table to create.</span></span>

<!-- end list -->

  - <span data-ttu-id="e3fb5-119">Seiten</span><span class="sxs-lookup"><span data-stu-id="e3fb5-119">pages</span></span>  
    <span data-ttu-id="e3fb5-120">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="e3fb5-120">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="e3fb5-121">Anfängliche Anzahl der Seiten in der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="e3fb5-121">Initial number of pages in the table.</span></span>

<!-- end list -->

  - <span data-ttu-id="e3fb5-122">Dichte (density)</span><span class="sxs-lookup"><span data-stu-id="e3fb5-122">density</span></span>  
    <span data-ttu-id="e3fb5-123">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="e3fb5-123">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="e3fb5-124">Die Standard Dichte der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="e3fb5-124">The default density of the table.</span></span> <span data-ttu-id="e3fb5-125">Dies wird bei sequenziellen Einfügungen verwendet.</span><span class="sxs-lookup"><span data-stu-id="e3fb5-125">This is used when doing sequential inserts.</span></span>

<!-- end list -->

  - <span data-ttu-id="e3fb5-126">TableID</span><span class="sxs-lookup"><span data-stu-id="e3fb5-126">tableid</span></span>  
    <span data-ttu-id="e3fb5-127">Typ: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="e3fb5-127">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="e3fb5-128">Gibt die TableID der neuen Tabelle zurück.</span><span class="sxs-lookup"><span data-stu-id="e3fb5-128">Returns the tableid of the new table.</span></span>

## <a name="see-also"></a><span data-ttu-id="e3fb5-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e3fb5-129">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e3fb5-130">Referenz</span><span class="sxs-lookup"><span data-stu-id="e3fb5-130">Reference</span></span>

[<span data-ttu-id="e3fb5-131">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="e3fb5-131">Api class</span></span>](./api-class.md)

[<span data-ttu-id="e3fb5-132">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="e3fb5-132">Api members</span></span>](./api-members.md)

[<span data-ttu-id="e3fb5-133">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="e3fb5-133">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
