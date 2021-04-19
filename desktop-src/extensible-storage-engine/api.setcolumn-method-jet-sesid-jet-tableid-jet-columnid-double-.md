---
description: 'Weitere Informationen finden Sie unter: API. SetColumn-Methode (JET_SESID, JET_TABLEID, JET_COLUMNID, Double)'
title: API. SetColumn-Methode (JET_SESID, JET_TABLEID, JET_COLUMNID, Double)
TOCTitle: SetColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, Double)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.SetColumn(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,System.Double)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.setcolumn(v=EXCHG.10)
ms:contentKeyID: 55100921
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.SetColumn
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4a3d47b42e08a524a20d337abc40da974866ba1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353995"
---
# <a name="apisetcolumn-method-jet_sesid-jet_tableid-jet_columnid-double"></a><span data-ttu-id="d65a2-103">API. SetColumn-Methode (JET_SESID, JET_TABLEID, JET_COLUMNID, Double)</span><span class="sxs-lookup"><span data-stu-id="d65a2-103">Api.SetColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, Double)</span></span>

<span data-ttu-id="d65a2-104">Ändert den Wert einer einzelnen Spalte in einem geänderten Datensatz, der eingefügt werden soll, oder, um den aktuellen Datensatz zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="d65a2-104">Modifies a single column value in a modified record to be inserted or to update the current record.</span></span>

<span data-ttu-id="d65a2-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="d65a2-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="d65a2-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="d65a2-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="d65a2-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="d65a2-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub SetColumn ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    data As Double _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim data As DoubleApi.SetColumn(sesid, tableid, columnid, _
    data)
```

``` csharp
public static void SetColumn(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    double data
)
```

#### <a name="parameters"></a><span data-ttu-id="d65a2-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="d65a2-108">Parameters</span></span>

  - <span data-ttu-id="d65a2-109">-sid</span><span class="sxs-lookup"><span data-stu-id="d65a2-109">sesid</span></span>  
    <span data-ttu-id="d65a2-110">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="d65a2-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="d65a2-111">Die zu verwendende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="d65a2-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="d65a2-112">TableID</span><span class="sxs-lookup"><span data-stu-id="d65a2-112">tableid</span></span>  
    <span data-ttu-id="d65a2-113">Typ: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="d65a2-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="d65a2-114">Der Cursor, der aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="d65a2-114">The cursor to update.</span></span> <span data-ttu-id="d65a2-115">Ein Update sollte vorbereitet werden.</span><span class="sxs-lookup"><span data-stu-id="d65a2-115">An update should be prepared.</span></span>

<!-- end list -->

  - <span data-ttu-id="d65a2-116">columnid</span><span class="sxs-lookup"><span data-stu-id="d65a2-116">columnid</span></span>  
    <span data-ttu-id="d65a2-117">Typ: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="d65a2-117">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="d65a2-118">Das festzulegende ColumnID.</span><span class="sxs-lookup"><span data-stu-id="d65a2-118">The columnid to set.</span></span>

<!-- end list -->

  - <span data-ttu-id="d65a2-119">Daten</span><span class="sxs-lookup"><span data-stu-id="d65a2-119">data</span></span>  
    <span data-ttu-id="d65a2-120">Typ: [System. Double](/dotnet/api/system.double)</span><span class="sxs-lookup"><span data-stu-id="d65a2-120">Type: [System.Double](/dotnet/api/system.double)</span></span>  
    
    <span data-ttu-id="d65a2-121">Die festzulegenden Daten.</span><span class="sxs-lookup"><span data-stu-id="d65a2-121">The data to set.</span></span>

## <a name="see-also"></a><span data-ttu-id="d65a2-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d65a2-122">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d65a2-123">Referenz</span><span class="sxs-lookup"><span data-stu-id="d65a2-123">Reference</span></span>

[<span data-ttu-id="d65a2-124">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="d65a2-124">Api class</span></span>](./api-class.md)

[<span data-ttu-id="d65a2-125">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="d65a2-125">Api members</span></span>](./api-members.md)

[<span data-ttu-id="d65a2-126">SetColumn-Überladung</span><span class="sxs-lookup"><span data-stu-id="d65a2-126">SetColumn overload</span></span>](./api.setcolumn-method.md)

[<span data-ttu-id="d65a2-127">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="d65a2-127">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
