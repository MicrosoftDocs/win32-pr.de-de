---
description: Weitere Informationen finden Sie in der API. jetsetcolumndefaultvalue-Methode.
title: API. jetsetcolumndefaultvalue-Methode
TOCTitle: 'JetSetColumnDefaultValue method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetSetColumnDefaultValue(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String,System.String,System.Byte[],System.Int32,Microsoft.Isam.Esent.Interop.SetColumnDefaultValueGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetsetcolumndefaultvalue(v=EXCHG.10)
ms:contentKeyID: 55100802
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetSetColumnDefaultValue
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetSetColumnDefaultValue
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 24fdb3a885e7aa558e1b3db3c4014fc65a28fcde
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366210"
---
# <a name="apijetsetcolumndefaultvalue-method"></a><span data-ttu-id="8ffe1-103">API. jetsetcolumndefaultvalue-Methode</span><span class="sxs-lookup"><span data-stu-id="8ffe1-103">Api.JetSetColumnDefaultValue method</span></span>

<span data-ttu-id="8ffe1-104">Ändert den Standardwert einer vorhandenen Spalte.</span><span class="sxs-lookup"><span data-stu-id="8ffe1-104">Changes the default value of an existing column.</span></span>

<span data-ttu-id="8ffe1-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="8ffe1-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="8ffe1-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="8ffe1-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="8ffe1-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="8ffe1-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetSetColumnDefaultValue ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tableName As String, _
    columnName As String, _
    data As Byte(), _
    dataSize As Integer, _
    grbit As SetColumnDefaultValueGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim tableName As String
Dim columnName As String
Dim data As Byte()
Dim dataSize As Integer
Dim grbit As SetColumnDefaultValueGrbitApi.JetSetColumnDefaultValue(sesid, _
    dbid, tableName, columnName, data, _
    dataSize, grbit)
```

``` csharp
public static void JetSetColumnDefaultValue(
    JET_SESID sesid,
    JET_DBID dbid,
    string tableName,
    string columnName,
    byte[] data,
    int dataSize,
    SetColumnDefaultValueGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="8ffe1-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="8ffe1-108">Parameters</span></span>

  - <span data-ttu-id="8ffe1-109">-sid</span><span class="sxs-lookup"><span data-stu-id="8ffe1-109">sesid</span></span>  
    <span data-ttu-id="8ffe1-110">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="8ffe1-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="8ffe1-111">Die zu verwendende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="8ffe1-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="8ffe1-112">dbid</span><span class="sxs-lookup"><span data-stu-id="8ffe1-112">dbid</span></span>  
    <span data-ttu-id="8ffe1-113">Typ: [Microsoft.ISAM.ESENT.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="8ffe1-113">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="8ffe1-114">Die Datenbank, die die Spalte enthält.</span><span class="sxs-lookup"><span data-stu-id="8ffe1-114">The database containing the column.</span></span>

<!-- end list -->

  - <span data-ttu-id="8ffe1-115">tableName</span><span class="sxs-lookup"><span data-stu-id="8ffe1-115">tableName</span></span>  
    <span data-ttu-id="8ffe1-116">Typ: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="8ffe1-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="8ffe1-117">Der Name der Tabelle, die die Spalte enthält.</span><span class="sxs-lookup"><span data-stu-id="8ffe1-117">The name of the table containing the column.</span></span>

<!-- end list -->

  - <span data-ttu-id="8ffe1-118">columnName</span><span class="sxs-lookup"><span data-stu-id="8ffe1-118">columnName</span></span>  
    <span data-ttu-id="8ffe1-119">Typ: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="8ffe1-119">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="8ffe1-120">Der Name der Spalte.</span><span class="sxs-lookup"><span data-stu-id="8ffe1-120">The name of the column.</span></span>

<!-- end list -->

  - <span data-ttu-id="8ffe1-121">Daten</span><span class="sxs-lookup"><span data-stu-id="8ffe1-121">data</span></span>  
    <span data-ttu-id="8ffe1-122">Sorte \[\]</span><span class="sxs-lookup"><span data-stu-id="8ffe1-122">Type: \[\]</span></span>  
    
    <span data-ttu-id="8ffe1-123">Der neue Standardwert.</span><span class="sxs-lookup"><span data-stu-id="8ffe1-123">The new default value.</span></span>

<!-- end list -->

  - <span data-ttu-id="8ffe1-124">dataSize</span><span class="sxs-lookup"><span data-stu-id="8ffe1-124">dataSize</span></span>  
    <span data-ttu-id="8ffe1-125">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="8ffe1-125">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="8ffe1-126">Größe des neuen Standardwerts.</span><span class="sxs-lookup"><span data-stu-id="8ffe1-126">Size of the new default value.</span></span>

<!-- end list -->

  - <span data-ttu-id="8ffe1-127">grbit</span><span class="sxs-lookup"><span data-stu-id="8ffe1-127">grbit</span></span>  
    <span data-ttu-id="8ffe1-128">Typ: [Microsoft. ISAM. ESENT. Interop. setcolumndefaultvaluegrbit](./setcolumndefaultvaluegrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="8ffe1-128">Type: [Microsoft.Isam.Esent.Interop.SetColumnDefaultValueGrbit](./setcolumndefaultvaluegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="8ffe1-129">Optionen für Spalten Standardwert.</span><span class="sxs-lookup"><span data-stu-id="8ffe1-129">Column default value options.</span></span>

## <a name="see-also"></a><span data-ttu-id="8ffe1-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8ffe1-130">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="8ffe1-131">Referenz</span><span class="sxs-lookup"><span data-stu-id="8ffe1-131">Reference</span></span>

[<span data-ttu-id="8ffe1-132">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="8ffe1-132">Api class</span></span>](./api-class.md)

[<span data-ttu-id="8ffe1-133">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="8ffe1-133">Api members</span></span>](./api-members.md)

[<span data-ttu-id="8ffe1-134">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="8ffe1-134">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
