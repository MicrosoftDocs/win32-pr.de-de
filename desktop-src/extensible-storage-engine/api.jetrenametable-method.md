---
description: Weitere Informationen finden Sie in der API. jetrenametable-Methode.
title: API. jetrenametable-Methode
TOCTitle: 'JetRenameTable method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetRenameTable(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String,System.String)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetrenametable(v=EXCHG.10)
ms:contentKeyID: 55100788
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetRenameTable
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetRenameTable
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6bb108498501df50a43964f5b069860d10c39258
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041654"
---
# <a name="apijetrenametable-method"></a><span data-ttu-id="681e7-103">API. jetrenametable-Methode</span><span class="sxs-lookup"><span data-stu-id="681e7-103">Api.JetRenameTable method</span></span>

<span data-ttu-id="681e7-104">Ändert den Namen einer vorhandenen Tabelle.</span><span class="sxs-lookup"><span data-stu-id="681e7-104">Changes the name of an existing table.</span></span>

<span data-ttu-id="681e7-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="681e7-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="681e7-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="681e7-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="681e7-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="681e7-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetRenameTable ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tableName As String, _
    newTableName As String _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim tableName As String
Dim newTableName As StringApi.JetRenameTable(sesid, dbid, _
    tableName, newTableName)
```

``` csharp
public static void JetRenameTable(
    JET_SESID sesid,
    JET_DBID dbid,
    string tableName,
    string newTableName
)
```

#### <a name="parameters"></a><span data-ttu-id="681e7-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="681e7-108">Parameters</span></span>

  - <span data-ttu-id="681e7-109">-sid</span><span class="sxs-lookup"><span data-stu-id="681e7-109">sesid</span></span>  
    <span data-ttu-id="681e7-110">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="681e7-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="681e7-111">Die zu verwendende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="681e7-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="681e7-112">dbid</span><span class="sxs-lookup"><span data-stu-id="681e7-112">dbid</span></span>  
    <span data-ttu-id="681e7-113">Typ: [Microsoft.ISAM.ESENT.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="681e7-113">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="681e7-114">Die Datenbank, die die Tabelle enthält.</span><span class="sxs-lookup"><span data-stu-id="681e7-114">The database containing the table.</span></span>

<!-- end list -->

  - <span data-ttu-id="681e7-115">tableName</span><span class="sxs-lookup"><span data-stu-id="681e7-115">tableName</span></span>  
    <span data-ttu-id="681e7-116">Typ: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="681e7-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="681e7-117">Der Name der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="681e7-117">The name of the table.</span></span>

<!-- end list -->

  - <span data-ttu-id="681e7-118">newtablename</span><span class="sxs-lookup"><span data-stu-id="681e7-118">newTableName</span></span>  
    <span data-ttu-id="681e7-119">Typ: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="681e7-119">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="681e7-120">Der neue Name der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="681e7-120">The new name of the table.</span></span>

## <a name="see-also"></a><span data-ttu-id="681e7-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="681e7-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="681e7-122">Referenz</span><span class="sxs-lookup"><span data-stu-id="681e7-122">Reference</span></span>

[<span data-ttu-id="681e7-123">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="681e7-123">Api class</span></span>](./api-class.md)

[<span data-ttu-id="681e7-124">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="681e7-124">Api members</span></span>](./api-members.md)

[<span data-ttu-id="681e7-125">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="681e7-125">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
