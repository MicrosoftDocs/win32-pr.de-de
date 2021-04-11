---
description: Weitere Informationen finden Sie in der API. JetDetachDatabase2-Methode.
title: API. JetDetachDatabase2-Methode
TOCTitle: 'JetDetachDatabase2 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetDetachDatabase2(Microsoft.Isam.Esent.Interop.JET_SESID,System.String,Microsoft.Isam.Esent.Interop.DetachDatabaseGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetdetachdatabase2(v=EXCHG.10)
ms:contentKeyID: 55100685
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetDetachDatabase2
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetDetachDatabase2
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 44cc8b5d03ba720f1acb7d0e8603bf29906a611e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128712"
---
# <a name="apijetdetachdatabase2-method"></a><span data-ttu-id="b8d7c-103">API. JetDetachDatabase2-Methode</span><span class="sxs-lookup"><span data-stu-id="b8d7c-103">Api.JetDetachDatabase2 method</span></span>

<span data-ttu-id="b8d7c-104">Gibt eine Datenbankdatei frei, die zuvor an eine Daten banksitzung angefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="b8d7c-104">Releases a database file that was previously attached to a database session.</span></span>

<span data-ttu-id="b8d7c-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b8d7c-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="b8d7c-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="b8d7c-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b8d7c-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="b8d7c-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetDetachDatabase2 ( _
    sesid As JET_SESID, _
    database As String, _
    grbit As DetachDatabaseGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim database As String
Dim grbit As DetachDatabaseGrbitApi.JetDetachDatabase2(sesid, database, _
    grbit)
```

``` csharp
public static void JetDetachDatabase2(
    JET_SESID sesid,
    string database,
    DetachDatabaseGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="b8d7c-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b8d7c-108">Parameters</span></span>

  - <span data-ttu-id="b8d7c-109">-sid</span><span class="sxs-lookup"><span data-stu-id="b8d7c-109">sesid</span></span>  
    <span data-ttu-id="b8d7c-110">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="b8d7c-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="b8d7c-111">Die zu verwendende Daten banksitzung.</span><span class="sxs-lookup"><span data-stu-id="b8d7c-111">The database session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="b8d7c-112">database</span><span class="sxs-lookup"><span data-stu-id="b8d7c-112">database</span></span>  
    <span data-ttu-id="b8d7c-113">Typ: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="b8d7c-113">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="b8d7c-114">Die Datenbank, die getrennt werden soll.</span><span class="sxs-lookup"><span data-stu-id="b8d7c-114">The database to detach.</span></span>

<!-- end list -->

  - <span data-ttu-id="b8d7c-115">grbit</span><span class="sxs-lookup"><span data-stu-id="b8d7c-115">grbit</span></span>  
    <span data-ttu-id="b8d7c-116">Typ: [Microsoft. ISAM. ESENT. Interop. detachdatabasegrbit](./detachdatabasegrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="b8d7c-116">Type: [Microsoft.Isam.Esent.Interop.DetachDatabaseGrbit](./detachdatabasegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="b8d7c-117">Optionen trennen.</span><span class="sxs-lookup"><span data-stu-id="b8d7c-117">Detach options.</span></span>

## <a name="see-also"></a><span data-ttu-id="b8d7c-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b8d7c-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b8d7c-119">Referenz</span><span class="sxs-lookup"><span data-stu-id="b8d7c-119">Reference</span></span>

[<span data-ttu-id="b8d7c-120">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="b8d7c-120">Api class</span></span>](./api-class.md)

[<span data-ttu-id="b8d7c-121">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="b8d7c-121">Api members</span></span>](./api-members.md)

[<span data-ttu-id="b8d7c-122">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="b8d7c-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
