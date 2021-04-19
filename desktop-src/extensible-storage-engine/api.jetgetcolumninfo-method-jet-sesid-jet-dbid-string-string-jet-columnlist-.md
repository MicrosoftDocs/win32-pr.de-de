---
description: 'Weitere Informationen finden Sie unter: API. jetgetcolumninfo-Methode (JET_SESID, JET_DBID, Zeichenfolge, Zeichenfolge, JET_COLUMNLIST)'
title: API. jetgetcolumninfo-Methode (JET_SESID, JET_DBID, String, String, JET_COLUMNLIST)
TOCTitle: JetGetColumnInfo method (JET_SESID, JET_DBID, String, String, JET_COLUMNLIST)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetColumnInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String,System.String,Microsoft.Isam.Esent.Interop.JET_COLUMNLIST@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetcolumninfo(v=EXCHG.10)
ms:contentKeyID: 55100703
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetColumnInfo
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6f3f0ea95e82217f0d9b44e6a00558d3530a7616
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348363"
---
# <a name="apijetgetcolumninfo-method-jet_sesid-jet_dbid-string-string-jet_columnlist"></a><span data-ttu-id="3cc86-103">API. jetgetcolumninfo-Methode (JET_SESID, JET_DBID, String, String, JET_COLUMNLIST)</span><span class="sxs-lookup"><span data-stu-id="3cc86-103">Api.JetGetColumnInfo method (JET_SESID, JET_DBID, String, String, JET_COLUMNLIST)</span></span>

<span data-ttu-id="3cc86-104">Ruft Informationen zu allen Spalten in einer Tabelle ab.</span><span class="sxs-lookup"><span data-stu-id="3cc86-104">Retrieves information about all columns in a table.</span></span>

<span data-ttu-id="3cc86-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="3cc86-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="3cc86-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="3cc86-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="3cc86-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="3cc86-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetColumnInfo ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tablename As String, _
    columnName As String, _
    <OutAttribute> ByRef columnlist As JET_COLUMNLIST _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim tablename As String
Dim columnName As String
Dim columnlist As JET_COLUMNLISTApi.JetGetColumnInfo(sesid, dbid, _
    tablename, columnName, columnlist)
```

``` csharp
public static void JetGetColumnInfo(
    JET_SESID sesid,
    JET_DBID dbid,
    string tablename,
    string columnName,
    out JET_COLUMNLIST columnlist
)
```

#### <a name="parameters"></a><span data-ttu-id="3cc86-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="3cc86-108">Parameters</span></span>

  - <span data-ttu-id="3cc86-109">-sid</span><span class="sxs-lookup"><span data-stu-id="3cc86-109">sesid</span></span>  
    <span data-ttu-id="3cc86-110">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="3cc86-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="3cc86-111">Die zu verwendende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="3cc86-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="3cc86-112">dbid</span><span class="sxs-lookup"><span data-stu-id="3cc86-112">dbid</span></span>  
    <span data-ttu-id="3cc86-113">Typ: [Microsoft.ISAM.ESENT.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="3cc86-113">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="3cc86-114">Die Datenbank, die die Tabelle enthält.</span><span class="sxs-lookup"><span data-stu-id="3cc86-114">The database that contains the table.</span></span>

<!-- end list -->

  - <span data-ttu-id="3cc86-115">Tabellenname</span><span class="sxs-lookup"><span data-stu-id="3cc86-115">tablename</span></span>  
    <span data-ttu-id="3cc86-116">Typ: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="3cc86-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="3cc86-117">Der Name der Tabelle, die die Spalte enthält.</span><span class="sxs-lookup"><span data-stu-id="3cc86-117">The name of the table containing the column.</span></span>

<!-- end list -->

  - <span data-ttu-id="3cc86-118">columnName</span><span class="sxs-lookup"><span data-stu-id="3cc86-118">columnName</span></span>  
    <span data-ttu-id="3cc86-119">Typ: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="3cc86-119">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="3cc86-120">Konvertiert die Zeichenfolgendarstellung einer Zahl in einem angegebenen Stil und einem kulturspezifischen Format in die entsprechende 32-Bit-Ganzzahl mit Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="3cc86-120">This parameter is ignored.</span></span>

<!-- end list -->

  - <span data-ttu-id="3cc86-121">ColumnList</span><span class="sxs-lookup"><span data-stu-id="3cc86-121">columnlist</span></span>  
    <span data-ttu-id="3cc86-122">Typ: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNLIST](./jet-columnlist-class.md)</span><span class="sxs-lookup"><span data-stu-id="3cc86-122">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNLIST](./jet-columnlist-class.md)</span></span>  
    
    <span data-ttu-id="3cc86-123">Wird mit Informationen über die Spalten in der Tabelle ausgefüllt.</span><span class="sxs-lookup"><span data-stu-id="3cc86-123">Filled in with information about the columns in the table.</span></span>

## <a name="see-also"></a><span data-ttu-id="3cc86-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3cc86-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="3cc86-125">Referenz</span><span class="sxs-lookup"><span data-stu-id="3cc86-125">Reference</span></span>

[<span data-ttu-id="3cc86-126">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="3cc86-126">Api class</span></span>](./api-class.md)

[<span data-ttu-id="3cc86-127">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="3cc86-127">Api members</span></span>](./api-members.md)

[<span data-ttu-id="3cc86-128">Jetgetcolumninfo-Überladung</span><span class="sxs-lookup"><span data-stu-id="3cc86-128">JetGetColumnInfo overload</span></span>](./api.jetgetcolumninfo-method.md)

[<span data-ttu-id="3cc86-129">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="3cc86-129">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
