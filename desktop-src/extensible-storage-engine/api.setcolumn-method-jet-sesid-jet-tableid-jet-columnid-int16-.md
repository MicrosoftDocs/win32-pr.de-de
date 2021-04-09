---
description: 'Weitere Informationen finden Sie unter: API. SetColumn-Methode (JET_SESID, JET_TABLEID, JET_COLUMNID, Int16)'
title: API. SetColumn-Methode (JET_SESID, JET_TABLEID, JET_COLUMNID, Int16)
TOCTitle: SetColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, Int16)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.SetColumn(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,System.Int16)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.setcolumn(v=EXCHG.10)
ms:contentKeyID: 55100922
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.SetColumn
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1f15c9b9340effdab5949d34c58393d3bc58a416
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050423"
---
# <a name="apisetcolumn-method-jet_sesid-jet_tableid-jet_columnid-int16"></a><span data-ttu-id="9842b-103">API. SetColumn-Methode (JET_SESID, JET_TABLEID, JET_COLUMNID, Int16)</span><span class="sxs-lookup"><span data-stu-id="9842b-103">Api.SetColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, Int16)</span></span>

<span data-ttu-id="9842b-104">Ändert den Wert einer einzelnen Spalte in einem geänderten Datensatz, der eingefügt werden soll, oder, um den aktuellen Datensatz zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="9842b-104">Modifies a single column value in a modified record to be inserted or to update the current record.</span></span>

<span data-ttu-id="9842b-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="9842b-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="9842b-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="9842b-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="9842b-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="9842b-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub SetColumn ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    data As Short _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim data As ShortApi.SetColumn(sesid, tableid, columnid, _
    data)
```

``` csharp
public static void SetColumn(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    short data
)
```

#### <a name="parameters"></a><span data-ttu-id="9842b-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="9842b-108">Parameters</span></span>

  - <span data-ttu-id="9842b-109">-sid</span><span class="sxs-lookup"><span data-stu-id="9842b-109">sesid</span></span>  
    <span data-ttu-id="9842b-110">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="9842b-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="9842b-111">Die zu verwendende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="9842b-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="9842b-112">TableID</span><span class="sxs-lookup"><span data-stu-id="9842b-112">tableid</span></span>  
    <span data-ttu-id="9842b-113">Typ: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="9842b-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="9842b-114">Der Cursor, der aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="9842b-114">The cursor to update.</span></span> <span data-ttu-id="9842b-115">Ein Update sollte vorbereitet werden.</span><span class="sxs-lookup"><span data-stu-id="9842b-115">An update should be prepared.</span></span>

<!-- end list -->

  - <span data-ttu-id="9842b-116">columnid</span><span class="sxs-lookup"><span data-stu-id="9842b-116">columnid</span></span>  
    <span data-ttu-id="9842b-117">Typ: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="9842b-117">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="9842b-118">Das festzulegende ColumnID.</span><span class="sxs-lookup"><span data-stu-id="9842b-118">The columnid to set.</span></span>

<!-- end list -->

  - <span data-ttu-id="9842b-119">Daten</span><span class="sxs-lookup"><span data-stu-id="9842b-119">data</span></span>  
    <span data-ttu-id="9842b-120">Typ: [System. Int16](/dotnet/api/system.int16)</span><span class="sxs-lookup"><span data-stu-id="9842b-120">Type: [System.Int16](/dotnet/api/system.int16)</span></span>  
    
    <span data-ttu-id="9842b-121">Die festzulegenden Daten.</span><span class="sxs-lookup"><span data-stu-id="9842b-121">The data to set.</span></span>

## <a name="see-also"></a><span data-ttu-id="9842b-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9842b-122">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="9842b-123">Referenz</span><span class="sxs-lookup"><span data-stu-id="9842b-123">Reference</span></span>

[<span data-ttu-id="9842b-124">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="9842b-124">Api class</span></span>](./api-class.md)

[<span data-ttu-id="9842b-125">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="9842b-125">Api members</span></span>](./api-members.md)

[<span data-ttu-id="9842b-126">SetColumn-Überladung</span><span class="sxs-lookup"><span data-stu-id="9842b-126">SetColumn overload</span></span>](./api.setcolumn-method.md)

[<span data-ttu-id="9842b-127">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="9842b-127">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
