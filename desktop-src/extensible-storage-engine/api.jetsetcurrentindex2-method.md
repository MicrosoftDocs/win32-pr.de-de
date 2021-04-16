---
description: Weitere Informationen finden Sie in der API. JetSetCurrentIndex2-Methode.
title: API. JetSetCurrentIndex2-Methode
TOCTitle: 'JetSetCurrentIndex2 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetSetCurrentIndex2(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.String,Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetsetcurrentindex2(v=EXCHG.10)
ms:contentKeyID: 55100798
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetSetCurrentIndex2
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetSetCurrentIndex2
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7e08e1fe5027641348259381d74b34ce16b034e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393485"
---
# <a name="apijetsetcurrentindex2-method"></a><span data-ttu-id="02b2d-103">API. JetSetCurrentIndex2-Methode</span><span class="sxs-lookup"><span data-stu-id="02b2d-103">Api.JetSetCurrentIndex2 method</span></span>

<span data-ttu-id="02b2d-104">Legen Sie den aktuellen Index eines Cursors fest.</span><span class="sxs-lookup"><span data-stu-id="02b2d-104">Set the current index of a cursor.</span></span>

<span data-ttu-id="02b2d-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="02b2d-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="02b2d-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="02b2d-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="02b2d-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="02b2d-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetSetCurrentIndex2 ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    index As String, _
    grbit As SetCurrentIndexGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim index As String
Dim grbit As SetCurrentIndexGrbitApi.JetSetCurrentIndex2(sesid, _
    tableid, index, grbit)
```

``` csharp
public static void JetSetCurrentIndex2(
    JET_SESID sesid,
    JET_TABLEID tableid,
    string index,
    SetCurrentIndexGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="02b2d-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="02b2d-108">Parameters</span></span>

  - <span data-ttu-id="02b2d-109">-sid</span><span class="sxs-lookup"><span data-stu-id="02b2d-109">sesid</span></span>  
    <span data-ttu-id="02b2d-110">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="02b2d-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="02b2d-111">Die zu verwendende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="02b2d-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="02b2d-112">TableID</span><span class="sxs-lookup"><span data-stu-id="02b2d-112">tableid</span></span>  
    <span data-ttu-id="02b2d-113">Typ: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="02b2d-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="02b2d-114">Der Cursor, für den der Index festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="02b2d-114">The cursor to set the index on.</span></span>

<!-- end list -->

  - <span data-ttu-id="02b2d-115">Index</span><span class="sxs-lookup"><span data-stu-id="02b2d-115">index</span></span>  
    <span data-ttu-id="02b2d-116">Typ: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="02b2d-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="02b2d-117">Der Name des Indexes, der ausgewählt werden soll.</span><span class="sxs-lookup"><span data-stu-id="02b2d-117">The name of the index to be selected.</span></span> <span data-ttu-id="02b2d-118">Wenn dieser Wert NULL oder leer ist, wird der primäre Index ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="02b2d-118">If this is null or empty the primary index will be selected.</span></span>

<!-- end list -->

  - <span data-ttu-id="02b2d-119">grbit</span><span class="sxs-lookup"><span data-stu-id="02b2d-119">grbit</span></span>  
    <span data-ttu-id="02b2d-120">Typ: [Microsoft. ISAM. ESENT. Interop. setcurrentindexgrbit](./setcurrentindexgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="02b2d-120">Type: [Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit](./setcurrentindexgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="02b2d-121">Legen Sie Index Optionen fest.</span><span class="sxs-lookup"><span data-stu-id="02b2d-121">Set index options.</span></span>

## <a name="see-also"></a><span data-ttu-id="02b2d-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="02b2d-122">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="02b2d-123">Referenz</span><span class="sxs-lookup"><span data-stu-id="02b2d-123">Reference</span></span>

[<span data-ttu-id="02b2d-124">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="02b2d-124">Api class</span></span>](./api-class.md)

[<span data-ttu-id="02b2d-125">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="02b2d-125">Api members</span></span>](./api-members.md)

[<span data-ttu-id="02b2d-126">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="02b2d-126">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
