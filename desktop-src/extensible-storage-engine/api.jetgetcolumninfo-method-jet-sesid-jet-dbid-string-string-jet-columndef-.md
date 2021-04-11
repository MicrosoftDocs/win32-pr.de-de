---
description: 'Weitere Informationen finden Sie unter: API. jetgetcolumninfo-Methode (JET_SESID, JET_DBID, Zeichenfolge, Zeichenfolge, JET_COLUMNDEF)'
title: API. jetgetcolumninfo-Methode (JET_SESID, JET_DBID, String, String, JET_COLUMNDEF)
TOCTitle: JetGetColumnInfo method (JET_SESID, JET_DBID, String, String, JET_COLUMNDEF)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetColumnInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String,System.String,Microsoft.Isam.Esent.Interop.JET_COLUMNDEF@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetcolumninfo(v=EXCHG.10)
ms:contentKeyID: 55100708
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetColumnInfo
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e4af99e7cfdc9f2f1fe83095ad92797ce0b34bf0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128704"
---
# <a name="apijetgetcolumninfo-method-jet_sesid-jet_dbid-string-string-jet_columndef"></a><span data-ttu-id="a9418-103">API. jetgetcolumninfo-Methode (JET_SESID, JET_DBID, String, String, JET_COLUMNDEF)</span><span class="sxs-lookup"><span data-stu-id="a9418-103">Api.JetGetColumnInfo method (JET_SESID, JET_DBID, String, String, JET_COLUMNDEF)</span></span>

<span data-ttu-id="a9418-104">Ruft Informationen über eine Tabellenspalte ab.</span><span class="sxs-lookup"><span data-stu-id="a9418-104">Retrieves information about a table column.</span></span>

<span data-ttu-id="a9418-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="a9418-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="a9418-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="a9418-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="a9418-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="a9418-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetColumnInfo ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tablename As String, _
    columnName As String, _
    <OutAttribute> ByRef columndef As JET_COLUMNDEF _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim tablename As String
Dim columnName As String
Dim columndef As JET_COLUMNDEFApi.JetGetColumnInfo(sesid, dbid, _
    tablename, columnName, columndef)
```

``` csharp
public static void JetGetColumnInfo(
    JET_SESID sesid,
    JET_DBID dbid,
    string tablename,
    string columnName,
    out JET_COLUMNDEF columndef
)
```

#### <a name="parameters"></a><span data-ttu-id="a9418-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="a9418-108">Parameters</span></span>

  - <span data-ttu-id="a9418-109">-sid</span><span class="sxs-lookup"><span data-stu-id="a9418-109">sesid</span></span>  
    <span data-ttu-id="a9418-110">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="a9418-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="a9418-111">Die zu verwendende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="a9418-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="a9418-112">dbid</span><span class="sxs-lookup"><span data-stu-id="a9418-112">dbid</span></span>  
    <span data-ttu-id="a9418-113">Typ: [Microsoft.ISAM.ESENT.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="a9418-113">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="a9418-114">Die Datenbank, die die Tabelle enthält.</span><span class="sxs-lookup"><span data-stu-id="a9418-114">The database that contains the table.</span></span>

<!-- end list -->

  - <span data-ttu-id="a9418-115">Tabellenname</span><span class="sxs-lookup"><span data-stu-id="a9418-115">tablename</span></span>  
    <span data-ttu-id="a9418-116">Typ: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="a9418-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="a9418-117">Der Name der Tabelle, die die Spalte enthält.</span><span class="sxs-lookup"><span data-stu-id="a9418-117">The name of the table containing the column.</span></span>

<!-- end list -->

  - <span data-ttu-id="a9418-118">columnName</span><span class="sxs-lookup"><span data-stu-id="a9418-118">columnName</span></span>  
    <span data-ttu-id="a9418-119">Typ: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="a9418-119">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="a9418-120">Der Name der Spalte.</span><span class="sxs-lookup"><span data-stu-id="a9418-120">The name of the column.</span></span>

<!-- end list -->

  - <span data-ttu-id="a9418-121">columndef</span><span class="sxs-lookup"><span data-stu-id="a9418-121">columndef</span></span>  
    <span data-ttu-id="a9418-122">Typ: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNDEF](./jet-columndef-class.md)</span><span class="sxs-lookup"><span data-stu-id="a9418-122">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNDEF](./jet-columndef-class.md)</span></span>  
    
    <span data-ttu-id="a9418-123">Wird mit Informationen über die Spalte ausgefüllt.</span><span class="sxs-lookup"><span data-stu-id="a9418-123">Filled in with information about the column.</span></span>

## <a name="see-also"></a><span data-ttu-id="a9418-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a9418-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a9418-125">Referenz</span><span class="sxs-lookup"><span data-stu-id="a9418-125">Reference</span></span>

[<span data-ttu-id="a9418-126">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="a9418-126">Api class</span></span>](./api-class.md)

[<span data-ttu-id="a9418-127">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="a9418-127">Api members</span></span>](./api-members.md)

[<span data-ttu-id="a9418-128">Jetgetcolumninfo-Überladung</span><span class="sxs-lookup"><span data-stu-id="a9418-128">JetGetColumnInfo overload</span></span>](./api.jetgetcolumninfo-method.md)

[<span data-ttu-id="a9418-129">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="a9418-129">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
