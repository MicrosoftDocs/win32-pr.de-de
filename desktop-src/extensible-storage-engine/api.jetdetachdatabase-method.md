---
description: Weitere Informationen finden Sie in der API. jetdetachdatabase-Methode.
title: API. jetdetachdatabase-Methode
TOCTitle: 'JetDetachDatabase method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetDetachDatabase(Microsoft.Isam.Esent.Interop.JET_SESID,System.String)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetdetachdatabase(v=EXCHG.10)
ms:contentKeyID: 55100687
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetDetachDatabase
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetDetachDatabase
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8881021d619bac1dae83a4a001e6b88e94e57256
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348757"
---
# <a name="apijetdetachdatabase-method"></a><span data-ttu-id="2727a-103">API. jetdetachdatabase-Methode</span><span class="sxs-lookup"><span data-stu-id="2727a-103">Api.JetDetachDatabase method</span></span>

<span data-ttu-id="2727a-104">Gibt eine Datenbankdatei frei, die zuvor an eine Daten banksitzung angefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="2727a-104">Releases a database file that was previously attached to a database session.</span></span>

<span data-ttu-id="2727a-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="2727a-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="2727a-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="2727a-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="2727a-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="2727a-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetDetachDatabase ( _
    sesid As JET_SESID, _
    database As String _
)
'Usage
Dim sesid As JET_SESID
Dim database As StringApi.JetDetachDatabase(sesid, database)
```

``` csharp
public static void JetDetachDatabase(
    JET_SESID sesid,
    string database
)
```

#### <a name="parameters"></a><span data-ttu-id="2727a-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="2727a-108">Parameters</span></span>

  - <span data-ttu-id="2727a-109">-sid</span><span class="sxs-lookup"><span data-stu-id="2727a-109">sesid</span></span>  
    <span data-ttu-id="2727a-110">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="2727a-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="2727a-111">Die zu verwendende Daten banksitzung.</span><span class="sxs-lookup"><span data-stu-id="2727a-111">The database session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="2727a-112">database</span><span class="sxs-lookup"><span data-stu-id="2727a-112">database</span></span>  
    <span data-ttu-id="2727a-113">Typ: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="2727a-113">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="2727a-114">Die Datenbank, die getrennt werden soll.</span><span class="sxs-lookup"><span data-stu-id="2727a-114">The database to detach.</span></span>

## <a name="see-also"></a><span data-ttu-id="2727a-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2727a-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="2727a-116">Referenz</span><span class="sxs-lookup"><span data-stu-id="2727a-116">Reference</span></span>

[<span data-ttu-id="2727a-117">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="2727a-117">Api class</span></span>](./api-class.md)

[<span data-ttu-id="2727a-118">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="2727a-118">Api members</span></span>](./api-members.md)

[<span data-ttu-id="2727a-119">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="2727a-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
