---
description: Weitere Informationen finden Sie in der API. jetrenamecolumschlag-Methode.
title: API. jetrenamecolumschlag-Methode
TOCTitle: 'JetRenameColumn method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetRenameColumn(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.String,System.String,Microsoft.Isam.Esent.Interop.RenameColumnGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetrenamecolumn(v=EXCHG.10)
ms:contentKeyID: 55100786
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetRenameColumn
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetRenameColumn
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 007bce82d8749611f0fe2b0eae28b54ddedab98f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759750"
---
# <a name="apijetrenamecolumn-method"></a><span data-ttu-id="22362-103">API. jetrenamecolumschlag-Methode</span><span class="sxs-lookup"><span data-stu-id="22362-103">Api.JetRenameColumn method</span></span>

<span data-ttu-id="22362-104">Ändert den Namen einer vorhandenen Spalte.</span><span class="sxs-lookup"><span data-stu-id="22362-104">Changes the name of an existing column.</span></span>

<span data-ttu-id="22362-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="22362-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="22362-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="22362-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="22362-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="22362-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetRenameColumn ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    name As String, _
    newName As String, _
    grbit As RenameColumnGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim name As String
Dim newName As String
Dim grbit As RenameColumnGrbitApi.JetRenameColumn(sesid, tableid, _
    name, newName, grbit)
```

``` csharp
public static void JetRenameColumn(
    JET_SESID sesid,
    JET_TABLEID tableid,
    string name,
    string newName,
    RenameColumnGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="22362-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="22362-108">Parameters</span></span>

  - <span data-ttu-id="22362-109">-sid</span><span class="sxs-lookup"><span data-stu-id="22362-109">sesid</span></span>  
    <span data-ttu-id="22362-110">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="22362-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="22362-111">Die zu verwendende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="22362-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="22362-112">TableID</span><span class="sxs-lookup"><span data-stu-id="22362-112">tableid</span></span>  
    <span data-ttu-id="22362-113">Typ: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="22362-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="22362-114">Die Tabelle, die die Spalte enthält.</span><span class="sxs-lookup"><span data-stu-id="22362-114">The table containing the column.</span></span>

<!-- end list -->

  - <span data-ttu-id="22362-115">name</span><span class="sxs-lookup"><span data-stu-id="22362-115">name</span></span>  
    <span data-ttu-id="22362-116">Typ: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="22362-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="22362-117">Der Name der Spalte.</span><span class="sxs-lookup"><span data-stu-id="22362-117">The name of the column.</span></span>

<!-- end list -->

  - <span data-ttu-id="22362-118">newName</span><span class="sxs-lookup"><span data-stu-id="22362-118">newName</span></span>  
    <span data-ttu-id="22362-119">Typ: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="22362-119">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="22362-120">Der neue Name der Spalte.</span><span class="sxs-lookup"><span data-stu-id="22362-120">The new name of the column.</span></span>

<!-- end list -->

  - <span data-ttu-id="22362-121">grbit</span><span class="sxs-lookup"><span data-stu-id="22362-121">grbit</span></span>  
    <span data-ttu-id="22362-122">Typ: [Microsoft. ISAM. ESENT. Interop. renamecolumngrbit](./renamecolumngrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="22362-122">Type: [Microsoft.Isam.Esent.Interop.RenameColumnGrbit](./renamecolumngrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="22362-123">Optionen für die Spalten umbenennen.</span><span class="sxs-lookup"><span data-stu-id="22362-123">Column rename options.</span></span>

## <a name="see-also"></a><span data-ttu-id="22362-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="22362-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="22362-125">Referenz</span><span class="sxs-lookup"><span data-stu-id="22362-125">Reference</span></span>

[<span data-ttu-id="22362-126">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="22362-126">Api class</span></span>](./api-class.md)

[<span data-ttu-id="22362-127">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="22362-127">Api members</span></span>](./api-members.md)

[<span data-ttu-id="22362-128">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="22362-128">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
