---
description: 'Weitere Informationen finden Sie unter: API. gettablecolumns-Methode (JET_SESID JET_TABLEID)'
title: API. gettablecolumns-Methode (JET_SESID, JET_TABLEID)
TOCTitle: GetTableColumns method (JET_SESID, JET_TABLEID)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.GetTableColumns(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.gettablecolumns(v=EXCHG.10)
ms:contentKeyID: 55107218
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.GetTableColumns
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 393f730920ce7abb3ef24916c9e1c9e9591ba020
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128069"
---
# <a name="apigettablecolumns-method-jet_sesid-jet_tableid"></a><span data-ttu-id="0630c-103">API. gettablecolumns-Methode (JET_SESID, JET_TABLEID)</span><span class="sxs-lookup"><span data-stu-id="0630c-103">Api.GetTableColumns method (JET_SESID, JET_TABLEID)</span></span>

<span data-ttu-id="0630c-104">Durchläuft alle Spalten in der Tabelle, wobei Informationen zu den einzelnen Spalten zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="0630c-104">Iterates over all the columns in the table, returning information about each one.</span></span>

<span data-ttu-id="0630c-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="0630c-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="0630c-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="0630c-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="0630c-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="0630c-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Function GetTableColumns ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID _
) As IEnumerable(Of ColumnInfo)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim returnValue As IEnumerable(Of ColumnInfo)

returnValue = Api.GetTableColumns(sesid, _
    tableid)
```

``` csharp
public static IEnumerable<ColumnInfo> GetTableColumns(
    JET_SESID sesid,
    JET_TABLEID tableid
)
```

#### <a name="parameters"></a><span data-ttu-id="0630c-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="0630c-108">Parameters</span></span>

  - <span data-ttu-id="0630c-109">-sid</span><span class="sxs-lookup"><span data-stu-id="0630c-109">sesid</span></span>  
    <span data-ttu-id="0630c-110">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="0630c-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="0630c-111">Die zu verwendende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="0630c-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="0630c-112">TableID</span><span class="sxs-lookup"><span data-stu-id="0630c-112">tableid</span></span>  
    <span data-ttu-id="0630c-113">Typ: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="0630c-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="0630c-114">Die Tabelle, für die Spalten Informationen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="0630c-114">The table to retrieve column information for.</span></span>

#### <a name="return-value"></a><span data-ttu-id="0630c-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0630c-115">Return value</span></span>

<span data-ttu-id="0630c-116">Typ: [System. Collections. Generic. IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1)\<[ColumnInfo](./columninfo-class.md)\></span><span class="sxs-lookup"><span data-stu-id="0630c-116">Type: [System.Collections.Generic.IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1)\<[ColumnInfo](./columninfo-class.md)\></span></span>  
<span data-ttu-id="0630c-117">Ein Iterator über ColumnInfo für jede Spalte in der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="0630c-117">An iterator over ColumnInfo for each column in the table.</span></span>  

## <a name="see-also"></a><span data-ttu-id="0630c-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0630c-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="0630c-119">Referenz</span><span class="sxs-lookup"><span data-stu-id="0630c-119">Reference</span></span>

[<span data-ttu-id="0630c-120">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="0630c-120">Api class</span></span>](./api-class.md)

[<span data-ttu-id="0630c-121">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="0630c-121">Api members</span></span>](./api-members.md)

[<span data-ttu-id="0630c-122">Gettablecolumns-Überladung</span><span class="sxs-lookup"><span data-stu-id="0630c-122">GetTableColumns overload</span></span>](./api.gettablecolumns-method.md)

[<span data-ttu-id="0630c-123">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="0630c-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
