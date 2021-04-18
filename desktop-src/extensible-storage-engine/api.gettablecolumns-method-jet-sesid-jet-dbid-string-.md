---
description: 'Weitere Informationen finden Sie unter: API. gettablecolumns-Methode (JET_SESID, JET_DBID, Zeichenfolge)'
title: API. gettablecolumns-Methode (JET_SESID, JET_DBID, Zeichenfolge)
TOCTitle: GetTableColumns method (JET_SESID, JET_DBID, String)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.GetTableColumns(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.gettablecolumns(v=EXCHG.10)
ms:contentKeyID: 55107216
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.GetTableColumns
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 68a05ee3d0887f4396df0b2ba3159737791c413d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524784"
---
# <a name="apigettablecolumns-method-jet_sesid-jet_dbid-string"></a><span data-ttu-id="c3953-103">API. gettablecolumns-Methode (JET_SESID, JET_DBID, Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="c3953-103">Api.GetTableColumns method (JET_SESID, JET_DBID, String)</span></span>

<span data-ttu-id="c3953-104">Durchläuft alle Spalten in der Tabelle, wobei Informationen zu den einzelnen Spalten zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="c3953-104">Iterates over all the columns in the table, returning information about each one.</span></span>

<span data-ttu-id="c3953-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="c3953-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="c3953-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="c3953-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="c3953-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="c3953-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Function GetTableColumns ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tablename As String _
) As IEnumerable(Of ColumnInfo)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim tablename As String
Dim returnValue As IEnumerable(Of ColumnInfo)

returnValue = Api.GetTableColumns(sesid, _
    dbid, tablename)
```

``` csharp
public static IEnumerable<ColumnInfo> GetTableColumns(
    JET_SESID sesid,
    JET_DBID dbid,
    string tablename
)
```

#### <a name="parameters"></a><span data-ttu-id="c3953-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="c3953-108">Parameters</span></span>

  - <span data-ttu-id="c3953-109">-sid</span><span class="sxs-lookup"><span data-stu-id="c3953-109">sesid</span></span>  
    <span data-ttu-id="c3953-110">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="c3953-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="c3953-111">Die zu verwendende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="c3953-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="c3953-112">dbid</span><span class="sxs-lookup"><span data-stu-id="c3953-112">dbid</span></span>  
    <span data-ttu-id="c3953-113">Typ: [Microsoft.ISAM.ESENT.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="c3953-113">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="c3953-114">Die Datenbank, die die Tabelle enthält.</span><span class="sxs-lookup"><span data-stu-id="c3953-114">The database containing the table.</span></span>

<!-- end list -->

  - <span data-ttu-id="c3953-115">Tabellenname</span><span class="sxs-lookup"><span data-stu-id="c3953-115">tablename</span></span>  
    <span data-ttu-id="c3953-116">Typ: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="c3953-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="c3953-117">Der Name der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="c3953-117">The name of the table.</span></span>

#### <a name="return-value"></a><span data-ttu-id="c3953-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c3953-118">Return value</span></span>

<span data-ttu-id="c3953-119">Typ: [System. Collections. Generic. IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1)\<[ColumnInfo](./columninfo-class.md)\></span><span class="sxs-lookup"><span data-stu-id="c3953-119">Type: [System.Collections.Generic.IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1)\<[ColumnInfo](./columninfo-class.md)\></span></span>  
<span data-ttu-id="c3953-120">Ein Iterator über ColumnInfo für jede Spalte in der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="c3953-120">An iterator over ColumnInfo for each column in the table.</span></span>  

## <a name="see-also"></a><span data-ttu-id="c3953-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c3953-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c3953-122">Referenz</span><span class="sxs-lookup"><span data-stu-id="c3953-122">Reference</span></span>

[<span data-ttu-id="c3953-123">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="c3953-123">Api class</span></span>](./api-class.md)

[<span data-ttu-id="c3953-124">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="c3953-124">Api members</span></span>](./api-members.md)

[<span data-ttu-id="c3953-125">Gettablecolumns-Überladung</span><span class="sxs-lookup"><span data-stu-id="c3953-125">GetTableColumns overload</span></span>](./api.gettablecolumns-method.md)

[<span data-ttu-id="c3953-126">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="c3953-126">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
