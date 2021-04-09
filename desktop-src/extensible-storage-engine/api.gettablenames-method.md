---
description: Weitere Informationen finden Sie in der API. gettablenames-Methode.
title: API. gettablenames-Methode
TOCTitle: 'GetTableNames method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.GetTableNames(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.gettablenames(v=EXCHG.10)
ms:contentKeyID: 55100650
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.GetTableNames
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.GetTableNames
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 39a52d62ae5271353350df15c4c00833266094cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128725"
---
# <a name="apigettablenames-method"></a><span data-ttu-id="d81b7-103">API. gettablenames-Methode</span><span class="sxs-lookup"><span data-stu-id="d81b7-103">Api.GetTableNames method</span></span>

<span data-ttu-id="d81b7-104">Gibt die Namen der Tabellen in der Datenbank zurück.</span><span class="sxs-lookup"><span data-stu-id="d81b7-104">Returns the names of the tables in the database.</span></span>

<span data-ttu-id="d81b7-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="d81b7-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="d81b7-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="d81b7-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="d81b7-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="d81b7-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Function GetTableNames ( _
    sesid As JET_SESID, _
    dbid As JET_DBID _
) As IEnumerable(Of String)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim returnValue As IEnumerable(Of String)

returnValue = Api.GetTableNames(sesid, _
    dbid)
```

``` csharp
public static IEnumerable<string> GetTableNames(
    JET_SESID sesid,
    JET_DBID dbid
)
```

#### <a name="parameters"></a><span data-ttu-id="d81b7-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="d81b7-108">Parameters</span></span>

  - <span data-ttu-id="d81b7-109">-sid</span><span class="sxs-lookup"><span data-stu-id="d81b7-109">sesid</span></span>  
    <span data-ttu-id="d81b7-110">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="d81b7-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="d81b7-111">Die zu verwendende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="d81b7-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="d81b7-112">dbid</span><span class="sxs-lookup"><span data-stu-id="d81b7-112">dbid</span></span>  
    <span data-ttu-id="d81b7-113">Typ: [Microsoft.ISAM.ESENT.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="d81b7-113">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="d81b7-114">Die Datenbank, die die Tabelle enthält.</span><span class="sxs-lookup"><span data-stu-id="d81b7-114">The database containing the table.</span></span>

#### <a name="return-value"></a><span data-ttu-id="d81b7-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d81b7-115">Return value</span></span>

<span data-ttu-id="d81b7-116">Typ: [System. Collections. Generic. IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1)\<[String](/dotnet/api/system.string)\></span><span class="sxs-lookup"><span data-stu-id="d81b7-116">Type: [System.Collections.Generic.IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1)\<[String](/dotnet/api/system.string)\></span></span>  
<span data-ttu-id="d81b7-117">Ein Iterator für die Namen der Tabellen in der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="d81b7-117">An iterator over the names of the tables in the database.</span></span>  

## <a name="see-also"></a><span data-ttu-id="d81b7-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d81b7-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d81b7-119">Referenz</span><span class="sxs-lookup"><span data-stu-id="d81b7-119">Reference</span></span>

[<span data-ttu-id="d81b7-120">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="d81b7-120">Api class</span></span>](./api-class.md)

[<span data-ttu-id="d81b7-121">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="d81b7-121">Api members</span></span>](./api-members.md)

[<span data-ttu-id="d81b7-122">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="d81b7-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
