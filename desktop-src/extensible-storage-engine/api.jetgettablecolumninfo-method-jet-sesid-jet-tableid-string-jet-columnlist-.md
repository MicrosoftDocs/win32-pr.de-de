---
description: 'Weitere Informationen finden Sie unter: API. jetgettablecolumninfo-Methode (JET_SESID, JET_TABLEID, Zeichenfolge, JET_COLUMNLIST)'
title: API. jetgettablecolumninfo-Methode (JET_SESID, JET_TABLEID, String, JET_COLUMNLIST)
TOCTitle: JetGetTableColumnInfo method (JET_SESID, JET_TABLEID, String, JET_COLUMNLIST)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetTableColumnInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.String,Microsoft.Isam.Esent.Interop.JET_COLUMNLIST@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgettablecolumninfo(v=EXCHG.10)
ms:contentKeyID: 55100723
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetTableColumnInfo
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 516dad3bbc93a12ec216c5c3caa35617ea989bbb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758983"
---
# <a name="apijetgettablecolumninfo-method-jet_sesid-jet_tableid-string-jet_columnlist"></a><span data-ttu-id="e45ff-103">API. jetgettablecolumninfo-Methode (JET_SESID, JET_TABLEID, String, JET_COLUMNLIST)</span><span class="sxs-lookup"><span data-stu-id="e45ff-103">Api.JetGetTableColumnInfo method (JET_SESID, JET_TABLEID, String, JET_COLUMNLIST)</span></span>

<span data-ttu-id="e45ff-104">Ruft Informationen zu allen Spalten in der Tabelle ab.</span><span class="sxs-lookup"><span data-stu-id="e45ff-104">Retrieves information about all columns in the table.</span></span>

<span data-ttu-id="e45ff-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e45ff-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="e45ff-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="e45ff-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e45ff-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e45ff-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetTableColumnInfo ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnName As String, _
    <OutAttribute> ByRef columnlist As JET_COLUMNLIST _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnName As String
Dim columnlist As JET_COLUMNLISTApi.JetGetTableColumnInfo(sesid, _
    tableid, columnName, columnlist)
```

``` csharp
public static void JetGetTableColumnInfo(
    JET_SESID sesid,
    JET_TABLEID tableid,
    string columnName,
    out JET_COLUMNLIST columnlist
)
```

#### <a name="parameters"></a><span data-ttu-id="e45ff-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="e45ff-108">Parameters</span></span>

  - <span data-ttu-id="e45ff-109">-sid</span><span class="sxs-lookup"><span data-stu-id="e45ff-109">sesid</span></span>  
    <span data-ttu-id="e45ff-110">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="e45ff-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="e45ff-111">Die zu verwendende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="e45ff-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="e45ff-112">TableID</span><span class="sxs-lookup"><span data-stu-id="e45ff-112">tableid</span></span>  
    <span data-ttu-id="e45ff-113">Typ: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="e45ff-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="e45ff-114">Die Tabelle, die die Spalte enthält.</span><span class="sxs-lookup"><span data-stu-id="e45ff-114">The table containing the column.</span></span>

<!-- end list -->

  - <span data-ttu-id="e45ff-115">columnName</span><span class="sxs-lookup"><span data-stu-id="e45ff-115">columnName</span></span>  
    <span data-ttu-id="e45ff-116">Typ: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="e45ff-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="e45ff-117">Der Parameter wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="e45ff-117">The parameter is ignored.</span></span>

<!-- end list -->

  - <span data-ttu-id="e45ff-118">ColumnList</span><span class="sxs-lookup"><span data-stu-id="e45ff-118">columnlist</span></span>  
    <span data-ttu-id="e45ff-119">Typ: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNLIST](./jet-columnlist-class.md)</span><span class="sxs-lookup"><span data-stu-id="e45ff-119">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNLIST](./jet-columnlist-class.md)</span></span>  
    
    <span data-ttu-id="e45ff-120">Wird mit Informationen über die Spalten in der Tabelle ausgefüllt.</span><span class="sxs-lookup"><span data-stu-id="e45ff-120">Filled in with information about the columns in the table.</span></span>

## <a name="see-also"></a><span data-ttu-id="e45ff-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e45ff-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e45ff-122">Referenz</span><span class="sxs-lookup"><span data-stu-id="e45ff-122">Reference</span></span>

[<span data-ttu-id="e45ff-123">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="e45ff-123">Api class</span></span>](./api-class.md)

[<span data-ttu-id="e45ff-124">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="e45ff-124">Api members</span></span>](./api-members.md)

[<span data-ttu-id="e45ff-125">Jetgettablecolumninfo-Überladung</span><span class="sxs-lookup"><span data-stu-id="e45ff-125">JetGetTableColumnInfo overload</span></span>](./api.jetgettablecolumninfo-method.md)

[<span data-ttu-id="e45ff-126">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="e45ff-126">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
