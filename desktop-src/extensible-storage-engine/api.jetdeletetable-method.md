---
description: 'Weitere Informationen finden Sie unter: API. jetdeletetable-Methode'
title: API. jetdeletetable-Methode
TOCTitle: 'JetDeleteTable method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetDeleteTable(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetdeletetable(v=EXCHG.10)
ms:contentKeyID: 55100683
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetDeleteTable
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetDeleteTable
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3b4128ae81484343bec7fb4f52a736db149f0eb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128716"
---
# <a name="apijetdeletetable-method"></a><span data-ttu-id="c7880-103">API. jetdeletetable-Methode</span><span class="sxs-lookup"><span data-stu-id="c7880-103">Api.JetDeleteTable method</span></span>

<span data-ttu-id="c7880-104">Löscht eine Tabelle aus einer Datenbank.</span><span class="sxs-lookup"><span data-stu-id="c7880-104">Deletes a table from a database.</span></span>

<span data-ttu-id="c7880-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="c7880-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="c7880-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="c7880-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="c7880-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="c7880-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetDeleteTable ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    table As String _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim table As StringApi.JetDeleteTable(sesid, dbid, _
    table)
```

``` csharp
public static void JetDeleteTable(
    JET_SESID sesid,
    JET_DBID dbid,
    string table
)
```

#### <a name="parameters"></a><span data-ttu-id="c7880-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="c7880-108">Parameters</span></span>

  - <span data-ttu-id="c7880-109">-sid</span><span class="sxs-lookup"><span data-stu-id="c7880-109">sesid</span></span>  
    <span data-ttu-id="c7880-110">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="c7880-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="c7880-111">Die zu verwendende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="c7880-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="c7880-112">dbid</span><span class="sxs-lookup"><span data-stu-id="c7880-112">dbid</span></span>  
    <span data-ttu-id="c7880-113">Typ: [Microsoft.ISAM.ESENT.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="c7880-113">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="c7880-114">Die Datenbank, aus der die Tabelle gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="c7880-114">The database to delete the table from.</span></span>

<!-- end list -->

  - <span data-ttu-id="c7880-115">table</span><span class="sxs-lookup"><span data-stu-id="c7880-115">table</span></span>  
    <span data-ttu-id="c7880-116">Typ: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="c7880-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="c7880-117">Der Name der zu löschenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="c7880-117">The name of the table to delete.</span></span>

## <a name="see-also"></a><span data-ttu-id="c7880-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c7880-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c7880-119">Referenz</span><span class="sxs-lookup"><span data-stu-id="c7880-119">Reference</span></span>

[<span data-ttu-id="c7880-120">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="c7880-120">Api class</span></span>](./api-class.md)

[<span data-ttu-id="c7880-121">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="c7880-121">Api members</span></span>](./api-members.md)

[<span data-ttu-id="c7880-122">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="c7880-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
