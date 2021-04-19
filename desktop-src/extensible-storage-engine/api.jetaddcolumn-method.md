---
description: 'Weitere Informationen finden Sie hier: API. jetaddcolumn-Methode'
title: API. jetaddcolumn-Methode
TOCTitle: 'JetAddColumn method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetAddColumn(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.String,Microsoft.Isam.Esent.Interop.JET_COLUMNDEF,System.Byte[],System.Int32,Microsoft.Isam.Esent.Interop.JET_COLUMNID@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetaddcolumn(v=EXCHG.10)
ms:contentKeyID: 55100651
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetAddColumn
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetAddColumn
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a864bab9c3b888622640e6226c3e7ee542a096d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346291"
---
# <a name="apijetaddcolumn-method"></a><span data-ttu-id="b1844-103">API. jetaddcolumn-Methode</span><span class="sxs-lookup"><span data-stu-id="b1844-103">Api.JetAddColumn method</span></span>

<span data-ttu-id="b1844-104">Fügen Sie einer vorhandenen Tabelle eine neue Spalte hinzu.</span><span class="sxs-lookup"><span data-stu-id="b1844-104">Add a new column to an existing table.</span></span>

<span data-ttu-id="b1844-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b1844-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="b1844-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="b1844-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b1844-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="b1844-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetAddColumn ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    column As String, _
    columndef As JET_COLUMNDEF, _
    defaultValue As Byte(), _
    defaultValueSize As Integer, _
    <OutAttribute> ByRef columnid As JET_COLUMNID _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim column As String
Dim columndef As JET_COLUMNDEF
Dim defaultValue As Byte()
Dim defaultValueSize As Integer
Dim columnid As JET_COLUMNIDApi.JetAddColumn(sesid, tableid, _
    column, columndef, defaultValue, _
    defaultValueSize, columnid)
```

``` csharp
public static void JetAddColumn(
    JET_SESID sesid,
    JET_TABLEID tableid,
    string column,
    JET_COLUMNDEF columndef,
    byte[] defaultValue,
    int defaultValueSize,
    out JET_COLUMNID columnid
)
```

#### <a name="parameters"></a><span data-ttu-id="b1844-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b1844-108">Parameters</span></span>

  - <span data-ttu-id="b1844-109">-sid</span><span class="sxs-lookup"><span data-stu-id="b1844-109">sesid</span></span>  
    <span data-ttu-id="b1844-110">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="b1844-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="b1844-111">Die zu verwendende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="b1844-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="b1844-112">TableID</span><span class="sxs-lookup"><span data-stu-id="b1844-112">tableid</span></span>  
    <span data-ttu-id="b1844-113">Typ: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="b1844-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="b1844-114">Die Tabelle, der die Spalte hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="b1844-114">The table to add the column to.</span></span>

<!-- end list -->

  - <span data-ttu-id="b1844-115">column</span><span class="sxs-lookup"><span data-stu-id="b1844-115">column</span></span>  
    <span data-ttu-id="b1844-116">Typ: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="b1844-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="b1844-117">Der Name der Spalte.</span><span class="sxs-lookup"><span data-stu-id="b1844-117">The name of the column.</span></span>

<!-- end list -->

  - <span data-ttu-id="b1844-118">columndef</span><span class="sxs-lookup"><span data-stu-id="b1844-118">columndef</span></span>  
    <span data-ttu-id="b1844-119">Typ: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNDEF](./jet-columndef-class.md)</span><span class="sxs-lookup"><span data-stu-id="b1844-119">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNDEF](./jet-columndef-class.md)</span></span>  
    
    <span data-ttu-id="b1844-120">Die Definition der Spalte.</span><span class="sxs-lookup"><span data-stu-id="b1844-120">The definition of the column.</span></span>

<!-- end list -->

  - <span data-ttu-id="b1844-121">defaultValue</span><span class="sxs-lookup"><span data-stu-id="b1844-121">defaultValue</span></span>  
    <span data-ttu-id="b1844-122">Sorte \[\]</span><span class="sxs-lookup"><span data-stu-id="b1844-122">Type: \[\]</span></span>  
    
    <span data-ttu-id="b1844-123">Der Standardwert der Spalte.</span><span class="sxs-lookup"><span data-stu-id="b1844-123">The default value of the column.</span></span>

<!-- end list -->

  - <span data-ttu-id="b1844-124">defaultvaluesize</span><span class="sxs-lookup"><span data-stu-id="b1844-124">defaultValueSize</span></span>  
    <span data-ttu-id="b1844-125">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="b1844-125">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="b1844-126">Die Größe des Standardwerts.</span><span class="sxs-lookup"><span data-stu-id="b1844-126">The size of the default value.</span></span>

<!-- end list -->

  - <span data-ttu-id="b1844-127">columnid</span><span class="sxs-lookup"><span data-stu-id="b1844-127">columnid</span></span>  
    <span data-ttu-id="b1844-128">Typ: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="b1844-128">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="b1844-129">Gibt das ColumnID der neuen Spalte zurück.</span><span class="sxs-lookup"><span data-stu-id="b1844-129">Returns the columnid of the new column.</span></span>

## <a name="see-also"></a><span data-ttu-id="b1844-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b1844-130">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b1844-131">Referenz</span><span class="sxs-lookup"><span data-stu-id="b1844-131">Reference</span></span>

[<span data-ttu-id="b1844-132">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="b1844-132">Api class</span></span>](./api-class.md)

[<span data-ttu-id="b1844-133">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="b1844-133">Api members</span></span>](./api-members.md)

[<span data-ttu-id="b1844-134">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="b1844-134">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
