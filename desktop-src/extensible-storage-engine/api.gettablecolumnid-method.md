---
description: 'Weitere Informationen finden Sie hier: API. gettablecolumnid-Methode'
title: API. gettablecolumnid-Methode
TOCTitle: 'GetTableColumnid method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.GetTableColumnid(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.String)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.gettablecolumnid(v=EXCHG.10)
ms:contentKeyID: 55107215
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.GetTableColumnid
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.GetTableColumnid
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ec91b014401709b6312b3363d8dae9e7da3d200e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524791"
---
# <a name="apigettablecolumnid-method"></a><span data-ttu-id="9bc3a-103">API. gettablecolumnid-Methode</span><span class="sxs-lookup"><span data-stu-id="9bc3a-103">Api.GetTableColumnid method</span></span>

<span data-ttu-id="9bc3a-104">Das ColumnID der angegebenen Spalte.</span><span class="sxs-lookup"><span data-stu-id="9bc3a-104">Get the columnid of the specified column.</span></span>

<span data-ttu-id="9bc3a-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="9bc3a-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="9bc3a-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="9bc3a-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="9bc3a-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="9bc3a-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Function GetTableColumnid ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnName As String _
) As JET_COLUMNID
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnName As String
Dim returnValue As JET_COLUMNID

returnValue = Api.GetTableColumnid(sesid, _
    tableid, columnName)
```

``` csharp
public static JET_COLUMNID GetTableColumnid(
    JET_SESID sesid,
    JET_TABLEID tableid,
    string columnName
)
```

#### <a name="parameters"></a><span data-ttu-id="9bc3a-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="9bc3a-108">Parameters</span></span>

  - <span data-ttu-id="9bc3a-109">-sid</span><span class="sxs-lookup"><span data-stu-id="9bc3a-109">sesid</span></span>  
    <span data-ttu-id="9bc3a-110">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="9bc3a-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="9bc3a-111">Die zu verwendende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="9bc3a-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="9bc3a-112">TableID</span><span class="sxs-lookup"><span data-stu-id="9bc3a-112">tableid</span></span>  
    <span data-ttu-id="9bc3a-113">Typ: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="9bc3a-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="9bc3a-114">Die Tabelle, die die Spalte enthält.</span><span class="sxs-lookup"><span data-stu-id="9bc3a-114">The table containing the column.</span></span>

<!-- end list -->

  - <span data-ttu-id="9bc3a-115">columnName</span><span class="sxs-lookup"><span data-stu-id="9bc3a-115">columnName</span></span>  
    <span data-ttu-id="9bc3a-116">Typ: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="9bc3a-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="9bc3a-117">Der Name der Spalte.</span><span class="sxs-lookup"><span data-stu-id="9bc3a-117">The name of the column.</span></span>

#### <a name="return-value"></a><span data-ttu-id="9bc3a-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9bc3a-118">Return value</span></span>

<span data-ttu-id="9bc3a-119">Typ: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="9bc3a-119">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
<span data-ttu-id="9bc3a-120">Die ID der Spalte.</span><span class="sxs-lookup"><span data-stu-id="9bc3a-120">The id of the column.</span></span>  

## <a name="see-also"></a><span data-ttu-id="9bc3a-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9bc3a-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="9bc3a-122">Referenz</span><span class="sxs-lookup"><span data-stu-id="9bc3a-122">Reference</span></span>

[<span data-ttu-id="9bc3a-123">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="9bc3a-123">Api class</span></span>](./api-class.md)

[<span data-ttu-id="9bc3a-124">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="9bc3a-124">Api members</span></span>](./api-members.md)

[<span data-ttu-id="9bc3a-125">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="9bc3a-125">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
