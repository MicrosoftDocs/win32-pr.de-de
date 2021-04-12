---
description: 'Weitere Informationen finden Sie hier: vistaapi. jetgetcolumninfo-Methode'
title: Vistaapi. jetgetcolumninfo-Methode (Microsoft. ISAM. ESENT. Interop. Vista)
TOCTitle: 'JetGetColumnInfo method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetGetColumnInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String,Microsoft.Isam.Esent.Interop.JET_COLUMNID,Microsoft.Isam.Esent.Interop.JET_COLUMNBASE@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaapi.jetgetcolumninfo(v=EXCHG.10)
ms:contentKeyID: 55104283
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetGetColumnInfo
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetGetColumnInfo
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3ae090fa5279b9ec60a3be88b4ebda393322b1f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129701"
---
# <a name="vistaapijetgetcolumninfo-method"></a><span data-ttu-id="8e2d7-103">Vistaapi. jetgetcolumninfo-Methode</span><span class="sxs-lookup"><span data-stu-id="8e2d7-103">VistaApi.JetGetColumnInfo method</span></span>

<span data-ttu-id="8e2d7-104">Ruft Informationen zu einer Spalte in einer Tabelle ab.</span><span class="sxs-lookup"><span data-stu-id="8e2d7-104">Retrieves information about a column in a table.</span></span>

<span data-ttu-id="8e2d7-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="8e2d7-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="8e2d7-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="8e2d7-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="8e2d7-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="8e2d7-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetColumnInfo ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tablename As String, _
    columnid As JET_COLUMNID, _
    <OutAttribute> ByRef columnbase As JET_COLUMNBASE _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim tablename As String
Dim columnid As JET_COLUMNID
Dim columnbase As JET_COLUMNBASEVistaApi.JetGetColumnInfo(sesid, dbid, _
    tablename, columnid, columnbase)
```

``` csharp
public static void JetGetColumnInfo(
    JET_SESID sesid,
    JET_DBID dbid,
    string tablename,
    JET_COLUMNID columnid,
    out JET_COLUMNBASE columnbase
)
```

#### <a name="parameters"></a><span data-ttu-id="8e2d7-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="8e2d7-108">Parameters</span></span>

  - <span data-ttu-id="8e2d7-109">-sid</span><span class="sxs-lookup"><span data-stu-id="8e2d7-109">sesid</span></span>  
    <span data-ttu-id="8e2d7-110">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="8e2d7-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="8e2d7-111">Die zu verwendende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="8e2d7-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="8e2d7-112">dbid</span><span class="sxs-lookup"><span data-stu-id="8e2d7-112">dbid</span></span>  
    <span data-ttu-id="8e2d7-113">Typ: [Microsoft.ISAM.ESENT.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="8e2d7-113">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="8e2d7-114">Die Datenbank, die die Tabelle enthält.</span><span class="sxs-lookup"><span data-stu-id="8e2d7-114">The database that contains the table.</span></span>

<!-- end list -->

  - <span data-ttu-id="8e2d7-115">Tabellenname</span><span class="sxs-lookup"><span data-stu-id="8e2d7-115">tablename</span></span>  
    <span data-ttu-id="8e2d7-116">Typ: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="8e2d7-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="8e2d7-117">Der Name der Tabelle, die die Spalte enthält.</span><span class="sxs-lookup"><span data-stu-id="8e2d7-117">The name of the table containing the column.</span></span>

<!-- end list -->

  - <span data-ttu-id="8e2d7-118">columnid</span><span class="sxs-lookup"><span data-stu-id="8e2d7-118">columnid</span></span>  
    <span data-ttu-id="8e2d7-119">Typ: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="8e2d7-119">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="8e2d7-120">Die ID der Spalte.</span><span class="sxs-lookup"><span data-stu-id="8e2d7-120">The ID of the column.</span></span>

<!-- end list -->

  - <span data-ttu-id="8e2d7-121">columnbase</span><span class="sxs-lookup"><span data-stu-id="8e2d7-121">columnbase</span></span>  
    <span data-ttu-id="8e2d7-122">Typ: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNBASE](./jet-columnbase-class.md)</span><span class="sxs-lookup"><span data-stu-id="8e2d7-122">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNBASE](./jet-columnbase-class.md)</span></span>  
    
    <span data-ttu-id="8e2d7-123">Wird mit Informationen über die Spalten in der Tabelle ausgefüllt.</span><span class="sxs-lookup"><span data-stu-id="8e2d7-123">Filled in with information about the columns in the table.</span></span>

## <a name="see-also"></a><span data-ttu-id="8e2d7-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8e2d7-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="8e2d7-125">Referenz</span><span class="sxs-lookup"><span data-stu-id="8e2d7-125">Reference</span></span>

[<span data-ttu-id="8e2d7-126">Vistaapi-Klasse</span><span class="sxs-lookup"><span data-stu-id="8e2d7-126">VistaApi class</span></span>](./vistaapi-class.md)

[<span data-ttu-id="8e2d7-127">Vistaapi-Member</span><span class="sxs-lookup"><span data-stu-id="8e2d7-127">VistaApi members</span></span>](./vistaapi-members.md)

[<span data-ttu-id="8e2d7-128">Microsoft. ISAM. ESENT. Interop. Vista-Namespace</span><span class="sxs-lookup"><span data-stu-id="8e2d7-128">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
