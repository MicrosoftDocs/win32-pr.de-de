---
description: Weitere Informationen finden Sie in der API. jetgetcurrentindex-Methode.
title: API. jetgetcurrentindex-Methode
TOCTitle: 'JetGetCurrentIndex method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetCurrentIndex(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.String@,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetcurrentindex(v=EXCHG.10)
ms:contentKeyID: 55100699
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGetCurrentIndex
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetCurrentIndex
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bacc6973b1a105e128533a1116abdeb4c6cfafa4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106340175"
---
# <a name="apijetgetcurrentindex-method"></a><span data-ttu-id="066fd-103">API. jetgetcurrentindex-Methode</span><span class="sxs-lookup"><span data-stu-id="066fd-103">Api.JetGetCurrentIndex method</span></span>

<span data-ttu-id="066fd-104">Dlegt den Namen des aktuellen Indexes eines angegebenen Cursors fest.</span><span class="sxs-lookup"><span data-stu-id="066fd-104">Ddetermines the name of the current index of a given cursor.</span></span> <span data-ttu-id="066fd-105">Dieser Name wird auch verwendet, um den Index später mithilfe von [jetsetcurrentindex (JET_SESID, JET_TABLEID, String)](./api.jetsetcurrentindex-method.md)als aktuellen Index erneut auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="066fd-105">This name is also used to later re-select that index as the current index using [JetSetCurrentIndex(JET_SESID, JET_TABLEID, String)](./api.jetsetcurrentindex-method.md).</span></span> <span data-ttu-id="066fd-106">Sie kann auch verwendet werden, um die Eigenschaften dieses Indexes mithilfe von jetgettableindexinfo zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="066fd-106">It can also be used to discover the properties of that index using JetGetTableIndexInfo.</span></span>

<span data-ttu-id="066fd-107">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="066fd-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="066fd-108">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="066fd-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="066fd-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="066fd-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetCurrentIndex ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    <OutAttribute> ByRef indexName As String, _
    maxNameLength As Integer _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim indexName As String
Dim maxNameLength As IntegerApi.JetGetCurrentIndex(sesid, tableid, _
    indexName, maxNameLength)
```

``` csharp
public static void JetGetCurrentIndex(
    JET_SESID sesid,
    JET_TABLEID tableid,
    out string indexName,
    int maxNameLength
)
```

#### <a name="parameters"></a><span data-ttu-id="066fd-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="066fd-110">Parameters</span></span>

  - <span data-ttu-id="066fd-111">-sid</span><span class="sxs-lookup"><span data-stu-id="066fd-111">sesid</span></span>  
    <span data-ttu-id="066fd-112">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="066fd-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="066fd-113">Die zu verwendende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="066fd-113">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="066fd-114">TableID</span><span class="sxs-lookup"><span data-stu-id="066fd-114">tableid</span></span>  
    <span data-ttu-id="066fd-115">Typ: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="066fd-115">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="066fd-116">Der Cursor, für den der Indexname angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="066fd-116">The cursor to get the index name for.</span></span>

<!-- end list -->

  - <span data-ttu-id="066fd-117">indexName</span><span class="sxs-lookup"><span data-stu-id="066fd-117">indexName</span></span>  
    <span data-ttu-id="066fd-118">Typ: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="066fd-118">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="066fd-119">Gibt den Namen des Indexes zurück.</span><span class="sxs-lookup"><span data-stu-id="066fd-119">Returns the name of the index.</span></span>

<!-- end list -->

  - <span data-ttu-id="066fd-120">maxNameLength</span><span class="sxs-lookup"><span data-stu-id="066fd-120">maxNameLength</span></span>  
    <span data-ttu-id="066fd-121">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="066fd-121">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="066fd-122">Die maximale Länge des Index namens.</span><span class="sxs-lookup"><span data-stu-id="066fd-122">The maximum length of the index name.</span></span> <span data-ttu-id="066fd-123">Indexnamen sind nicht mehr als [namemost](./systemparameters.namemost-field.md) -Zeichen.</span><span class="sxs-lookup"><span data-stu-id="066fd-123">Index names are no more than [NameMost](./systemparameters.namemost-field.md) characters.</span></span>

## <a name="see-also"></a><span data-ttu-id="066fd-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="066fd-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="066fd-125">Referenz</span><span class="sxs-lookup"><span data-stu-id="066fd-125">Reference</span></span>

[<span data-ttu-id="066fd-126">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="066fd-126">Api class</span></span>](./api-class.md)

[<span data-ttu-id="066fd-127">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="066fd-127">Api members</span></span>](./api-members.md)

[<span data-ttu-id="066fd-128">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="066fd-128">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
