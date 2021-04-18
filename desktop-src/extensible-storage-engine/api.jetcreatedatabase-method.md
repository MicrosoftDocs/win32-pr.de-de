---
description: Weitere Informationen finden Sie in der API. jetkreatedatabase-Methode.
title: API. jetkreatedatabase-Methode
TOCTitle: 'JetCreateDatabase method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetCreateDatabase(Microsoft.Isam.Esent.Interop.JET_SESID,System.String,System.String,Microsoft.Isam.Esent.Interop.JET_DBID@,Microsoft.Isam.Esent.Interop.CreateDatabaseGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetcreatedatabase(v=EXCHG.10)
ms:contentKeyID: 55100748
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetCreateDatabase
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetCreateDatabase
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fe427c270baf8a6d05e5d0ae99e1dc393208da01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106354445"
---
# <a name="apijetcreatedatabase-method"></a><span data-ttu-id="02e11-103">API. jetkreatedatabase-Methode</span><span class="sxs-lookup"><span data-stu-id="02e11-103">Api.JetCreateDatabase method</span></span>

<span data-ttu-id="02e11-104">Erstellt eine Datenbankdatei und fügt Sie an.</span><span class="sxs-lookup"><span data-stu-id="02e11-104">Creates and attaches a database file.</span></span>

<span data-ttu-id="02e11-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="02e11-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="02e11-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="02e11-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="02e11-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="02e11-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetCreateDatabase ( _
    sesid As JET_SESID, _
    database As String, _
    connect As String, _
    <OutAttribute> ByRef dbid As JET_DBID, _
    grbit As CreateDatabaseGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim database As String
Dim connect As String
Dim dbid As JET_DBID
Dim grbit As CreateDatabaseGrbitApi.JetCreateDatabase(sesid, database, _
    connect, dbid, grbit)
```

``` csharp
public static void JetCreateDatabase(
    JET_SESID sesid,
    string database,
    string connect,
    out JET_DBID dbid,
    CreateDatabaseGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="02e11-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="02e11-108">Parameters</span></span>

  - <span data-ttu-id="02e11-109">-sid</span><span class="sxs-lookup"><span data-stu-id="02e11-109">sesid</span></span>  
    <span data-ttu-id="02e11-110">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="02e11-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="02e11-111">Die zu verwendende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="02e11-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="02e11-112">database</span><span class="sxs-lookup"><span data-stu-id="02e11-112">database</span></span>  
    <span data-ttu-id="02e11-113">Typ: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="02e11-113">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="02e11-114">Der Pfad zur Datenbankdatei, die erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="02e11-114">The path to the database file to create.</span></span>

<!-- end list -->

  - <span data-ttu-id="02e11-115">Verbinden</span><span class="sxs-lookup"><span data-stu-id="02e11-115">connect</span></span>  
    <span data-ttu-id="02e11-116">Typ: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="02e11-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="02e11-117">Der-Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="02e11-117">The parameter is not used.</span></span>

<!-- end list -->

  - <span data-ttu-id="02e11-118">dbid</span><span class="sxs-lookup"><span data-stu-id="02e11-118">dbid</span></span>  
    <span data-ttu-id="02e11-119">Typ: [Microsoft.ISAM.ESENT.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="02e11-119">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="02e11-120">Gibt die dbid der neuen Datenbank zurück.</span><span class="sxs-lookup"><span data-stu-id="02e11-120">Returns the dbid of the new database.</span></span>

<!-- end list -->

  - <span data-ttu-id="02e11-121">grbit</span><span class="sxs-lookup"><span data-stu-id="02e11-121">grbit</span></span>  
    <span data-ttu-id="02e11-122">Typ: [Microsoft. ISAM. ESENT. Interop. kreatedatabasegrbit](./createdatabasegrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="02e11-122">Type: [Microsoft.Isam.Esent.Interop.CreateDatabaseGrbit](./createdatabasegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="02e11-123">Optionen für die Daten Bank Erstellung.</span><span class="sxs-lookup"><span data-stu-id="02e11-123">Database creation options.</span></span>

## <a name="see-also"></a><span data-ttu-id="02e11-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="02e11-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="02e11-125">Referenz</span><span class="sxs-lookup"><span data-stu-id="02e11-125">Reference</span></span>

[<span data-ttu-id="02e11-126">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="02e11-126">Api class</span></span>](./api-class.md)

[<span data-ttu-id="02e11-127">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="02e11-127">Api members</span></span>](./api-members.md)

[<span data-ttu-id="02e11-128">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="02e11-128">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
