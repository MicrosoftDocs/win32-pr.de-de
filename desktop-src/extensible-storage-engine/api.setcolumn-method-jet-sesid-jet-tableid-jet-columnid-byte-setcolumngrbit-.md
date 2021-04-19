---
description: 'Weitere Informationen finden Sie unter: API. SetColumn-Methode (JET_SESID, JET_TABLEID, JET_COLUMNID, Byte, setcolumngrbit)'
title: API. SetColumn-Methode (JET_SESID, JET_TABLEID, JET_COLUMNID, Byte, setcolumngrbit)
TOCTitle: SetColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, Byte , SetColumnGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.SetColumn(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,System.Byte[],Microsoft.Isam.Esent.Interop.SetColumnGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.setcolumn(v=EXCHG.10)
ms:contentKeyID: 55100881
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
ms.openlocfilehash: e345db028422733d37d50f51cfd0c940823f9f3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362915"
---
# <a name="apisetcolumn-method-jet_sesid-jet_tableid-jet_columnid-byte--setcolumngrbit"></a><span data-ttu-id="bed39-103">API. SetColumn-Methode (JET_SESID, JET_TABLEID, JET_COLUMNID, Byte, setcolumngrbit)</span><span class="sxs-lookup"><span data-stu-id="bed39-103">Api.SetColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, Byte , SetColumnGrbit)</span></span>

<span data-ttu-id="bed39-104">Ändert den Wert einer einzelnen Spalte in einem geänderten Datensatz, der eingefügt werden soll, oder, um den aktuellen Datensatz zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="bed39-104">Modifies a single column value in a modified record to be inserted or to update the current record.</span></span>

<span data-ttu-id="bed39-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="bed39-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="bed39-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="bed39-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="bed39-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="bed39-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub SetColumn ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    data As Byte(), _
    grbit As SetColumnGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim data As Byte()
Dim grbit As SetColumnGrbitApi.SetColumn(sesid, tableid, columnid, _
    data, grbit)
```

``` csharp
public static void SetColumn(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    byte[] data,
    SetColumnGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="bed39-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="bed39-108">Parameters</span></span>

  - <span data-ttu-id="bed39-109">-sid</span><span class="sxs-lookup"><span data-stu-id="bed39-109">sesid</span></span>  
    <span data-ttu-id="bed39-110">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="bed39-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="bed39-111">Die zu verwendende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="bed39-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="bed39-112">TableID</span><span class="sxs-lookup"><span data-stu-id="bed39-112">tableid</span></span>  
    <span data-ttu-id="bed39-113">Typ: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="bed39-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="bed39-114">Der Cursor, der aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="bed39-114">The cursor to update.</span></span> <span data-ttu-id="bed39-115">Ein Update sollte vorbereitet werden.</span><span class="sxs-lookup"><span data-stu-id="bed39-115">An update should be prepared.</span></span>

<!-- end list -->

  - <span data-ttu-id="bed39-116">columnid</span><span class="sxs-lookup"><span data-stu-id="bed39-116">columnid</span></span>  
    <span data-ttu-id="bed39-117">Typ: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="bed39-117">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="bed39-118">Das festzulegende ColumnID.</span><span class="sxs-lookup"><span data-stu-id="bed39-118">The columnid to set.</span></span>

<!-- end list -->

  - <span data-ttu-id="bed39-119">Daten</span><span class="sxs-lookup"><span data-stu-id="bed39-119">data</span></span>  
    <span data-ttu-id="bed39-120">Sorte \[\]</span><span class="sxs-lookup"><span data-stu-id="bed39-120">Type: \[\]</span></span>  
    
    <span data-ttu-id="bed39-121">Die festzulegenden Daten.</span><span class="sxs-lookup"><span data-stu-id="bed39-121">The data to set.</span></span>

<!-- end list -->

  - <span data-ttu-id="bed39-122">grbit</span><span class="sxs-lookup"><span data-stu-id="bed39-122">grbit</span></span>  
    <span data-ttu-id="bed39-123">Typ: [Microsoft. ISAM. ESENT. Interop. setcolumngrbit](./setcolumngrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="bed39-123">Type: [Microsoft.Isam.Esent.Interop.SetColumnGrbit](./setcolumngrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="bed39-124">SetColumn-Optionen.</span><span class="sxs-lookup"><span data-stu-id="bed39-124">SetColumn options.</span></span>

## <a name="see-also"></a><span data-ttu-id="bed39-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bed39-125">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="bed39-126">Referenz</span><span class="sxs-lookup"><span data-stu-id="bed39-126">Reference</span></span>

[<span data-ttu-id="bed39-127">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="bed39-127">Api class</span></span>](./api-class.md)

[<span data-ttu-id="bed39-128">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="bed39-128">Api members</span></span>](./api-members.md)

[<span data-ttu-id="bed39-129">SetColumn-Überladung</span><span class="sxs-lookup"><span data-stu-id="bed39-129">SetColumn overload</span></span>](./api.setcolumn-method.md)

[<span data-ttu-id="bed39-130">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="bed39-130">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
