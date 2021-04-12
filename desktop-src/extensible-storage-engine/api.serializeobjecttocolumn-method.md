---
description: Weitere Informationen finden Sie in der API. serializeobjecttocolumn-Methode.
title: API. serializeobjecttocolumn-Methode
TOCTitle: 'SerializeObjectToColumn method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.SerializeObjectToColumn(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,System.Object)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.serializeobjecttocolumn(v=EXCHG.10)
ms:contentKeyID: 55100915
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.SerializeObjectToColumn
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.SerializeObjectToColumn
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 21b0e421b68287b983fc43482e3a2385b2a160f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216696"
---
# <a name="apiserializeobjecttocolumn-method"></a><span data-ttu-id="5362b-103">API. serializeobjecttocolumn-Methode</span><span class="sxs-lookup"><span data-stu-id="5362b-103">Api.SerializeObjectToColumn method</span></span>

<span data-ttu-id="5362b-104">Schreibt eine serialisierte Form eines Objekts in eine Spalte.</span><span class="sxs-lookup"><span data-stu-id="5362b-104">Write a serialized form of an object to a column.</span></span>

<span data-ttu-id="5362b-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="5362b-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="5362b-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="5362b-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="5362b-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="5362b-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub SerializeObjectToColumn ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    value As Object _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim value As ObjectApi.SerializeObjectToColumn(sesid, _
    tableid, columnid, value)
```

``` csharp
public static void SerializeObjectToColumn(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    Object value
)
```

#### <a name="parameters"></a><span data-ttu-id="5362b-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="5362b-108">Parameters</span></span>

  - <span data-ttu-id="5362b-109">-sid</span><span class="sxs-lookup"><span data-stu-id="5362b-109">sesid</span></span>  
    <span data-ttu-id="5362b-110">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="5362b-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="5362b-111">Die zu verwendende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="5362b-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="5362b-112">TableID</span><span class="sxs-lookup"><span data-stu-id="5362b-112">tableid</span></span>  
    <span data-ttu-id="5362b-113">Typ: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="5362b-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="5362b-114">Die Tabelle, in die geschrieben werden soll.</span><span class="sxs-lookup"><span data-stu-id="5362b-114">The table to write to.</span></span> <span data-ttu-id="5362b-115">Ein Update sollte vorbereitet werden.</span><span class="sxs-lookup"><span data-stu-id="5362b-115">An update should be prepared.</span></span>

<!-- end list -->

  - <span data-ttu-id="5362b-116">columnid</span><span class="sxs-lookup"><span data-stu-id="5362b-116">columnid</span></span>  
    <span data-ttu-id="5362b-117">Typ: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="5362b-117">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="5362b-118">Die Spalte, in die geschrieben werden soll.</span><span class="sxs-lookup"><span data-stu-id="5362b-118">The column to write to.</span></span>

<!-- end list -->

  - <span data-ttu-id="5362b-119">value</span><span class="sxs-lookup"><span data-stu-id="5362b-119">value</span></span>  
    <span data-ttu-id="5362b-120">Type: [System. Object](/dotnet/api/system.object)</span><span class="sxs-lookup"><span data-stu-id="5362b-120">Type: [System.Object](/dotnet/api/system.object)</span></span>  
    
    <span data-ttu-id="5362b-121">Das zu schreibende Objekt.</span><span class="sxs-lookup"><span data-stu-id="5362b-121">The object to write.</span></span> <span data-ttu-id="5362b-122">Das Objekt muss serialisierbar sein.</span><span class="sxs-lookup"><span data-stu-id="5362b-122">The object must be serializable.</span></span>

## <a name="see-also"></a><span data-ttu-id="5362b-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5362b-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="5362b-124">Referenz</span><span class="sxs-lookup"><span data-stu-id="5362b-124">Reference</span></span>

[<span data-ttu-id="5362b-125">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="5362b-125">Api class</span></span>](./api-class.md)

[<span data-ttu-id="5362b-126">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="5362b-126">Api members</span></span>](./api-members.md)

[<span data-ttu-id="5362b-127">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="5362b-127">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
