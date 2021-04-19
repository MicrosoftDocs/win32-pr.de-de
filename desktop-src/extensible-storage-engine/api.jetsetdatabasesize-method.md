---
description: Weitere Informationen finden Sie in der API. jetsetdatabasesize-Methode
title: API. jetsetdatabasesize-Methode
TOCTitle: 'JetSetDatabaseSize method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetSetDatabaseSize(Microsoft.Isam.Esent.Interop.JET_SESID,System.String,System.Int32,System.Int32@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetsetdatabasesize(v=EXCHG.10)
ms:contentKeyID: 55100807
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetSetDatabaseSize
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetSetDatabaseSize
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c90ba5ef2ebc96cbe6d50fa6c0888db9a09a0a99
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349566"
---
# <a name="apijetsetdatabasesize-method"></a><span data-ttu-id="cf848-103">API. jetsetdatabasesize-Methode</span><span class="sxs-lookup"><span data-stu-id="cf848-103">Api.JetSetDatabaseSize method</span></span>

<span data-ttu-id="cf848-104">Legt die Größe einer nicht geöffneten Datenbankdatei fest.</span><span class="sxs-lookup"><span data-stu-id="cf848-104">Sets the size of an unopened database file.</span></span>

<span data-ttu-id="cf848-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="cf848-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="cf848-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="cf848-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="cf848-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="cf848-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetSetDatabaseSize ( _
    sesid As JET_SESID, _
    database As String, _
    desiredPages As Integer, _
    <OutAttribute> ByRef actualPages As Integer _
)
'Usage
Dim sesid As JET_SESID
Dim database As String
Dim desiredPages As Integer
Dim actualPages As IntegerApi.JetSetDatabaseSize(sesid, database, _
    desiredPages, actualPages)
```

``` csharp
public static void JetSetDatabaseSize(
    JET_SESID sesid,
    string database,
    int desiredPages,
    out int actualPages
)
```

#### <a name="parameters"></a><span data-ttu-id="cf848-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="cf848-108">Parameters</span></span>

  - <span data-ttu-id="cf848-109">-sid</span><span class="sxs-lookup"><span data-stu-id="cf848-109">sesid</span></span>  
    <span data-ttu-id="cf848-110">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="cf848-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="cf848-111">Die zu verwendende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="cf848-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="cf848-112">database</span><span class="sxs-lookup"><span data-stu-id="cf848-112">database</span></span>  
    <span data-ttu-id="cf848-113">Typ: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="cf848-113">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="cf848-114">Der Name der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="cf848-114">The name of the database.</span></span>

<!-- end list -->

  - <span data-ttu-id="cf848-115">desiredpages</span><span class="sxs-lookup"><span data-stu-id="cf848-115">desiredPages</span></span>  
    <span data-ttu-id="cf848-116">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="cf848-116">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="cf848-117">Die gewünschte Größe der Datenbank in Seiten.</span><span class="sxs-lookup"><span data-stu-id="cf848-117">The desired size of the database, in pages.</span></span>

<!-- end list -->

  - <span data-ttu-id="cf848-118">actualpages</span><span class="sxs-lookup"><span data-stu-id="cf848-118">actualPages</span></span>  
    <span data-ttu-id="cf848-119">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="cf848-119">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="cf848-120">Die Größe der Datenbank in Seiten nach dem-Befehl.</span><span class="sxs-lookup"><span data-stu-id="cf848-120">The size of the database, in pages, after the call.</span></span>

## <a name="see-also"></a><span data-ttu-id="cf848-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cf848-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="cf848-122">Referenz</span><span class="sxs-lookup"><span data-stu-id="cf848-122">Reference</span></span>

[<span data-ttu-id="cf848-123">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="cf848-123">Api class</span></span>](./api-class.md)

[<span data-ttu-id="cf848-124">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="cf848-124">Api members</span></span>](./api-members.md)

[<span data-ttu-id="cf848-125">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="cf848-125">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
