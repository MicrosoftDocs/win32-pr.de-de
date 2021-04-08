---
description: Weitere Informationen finden Sie in der API. JetCreateDatabase2-Methode.
title: API. JetCreateDatabase2-Methode
TOCTitle: 'JetCreateDatabase2 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetCreateDatabase2(Microsoft.Isam.Esent.Interop.JET_SESID,System.String,System.Int32,Microsoft.Isam.Esent.Interop.JET_DBID@,Microsoft.Isam.Esent.Interop.CreateDatabaseGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetcreatedatabase2(v=EXCHG.10)
ms:contentKeyID: 55100671
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetCreateDatabase2
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetCreateDatabase2
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8293a7c98451b0fd8bc46fbc13dde6b477a0ad09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749497"
---
# <a name="apijetcreatedatabase2-method"></a><span data-ttu-id="efb29-103">API. JetCreateDatabase2-Methode</span><span class="sxs-lookup"><span data-stu-id="efb29-103">Api.JetCreateDatabase2 method</span></span>

<span data-ttu-id="efb29-104">Erstellt eine Datenbankdatei mit einer angegebenen maximalen Datenbankgröße und fügt Sie an.</span><span class="sxs-lookup"><span data-stu-id="efb29-104">Creates and attaches a database file with a maximum database size specified.</span></span>

<span data-ttu-id="efb29-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="efb29-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="efb29-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="efb29-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="efb29-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="efb29-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetCreateDatabase2 ( _
    sesid As JET_SESID, _
    database As String, _
    maxPages As Integer, _
    <OutAttribute> ByRef dbid As JET_DBID, _
    grbit As CreateDatabaseGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim database As String
Dim maxPages As Integer
Dim dbid As JET_DBID
Dim grbit As CreateDatabaseGrbitApi.JetCreateDatabase2(sesid, database, _
    maxPages, dbid, grbit)
```

``` csharp
public static void JetCreateDatabase2(
    JET_SESID sesid,
    string database,
    int maxPages,
    out JET_DBID dbid,
    CreateDatabaseGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="efb29-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="efb29-108">Parameters</span></span>

  - <span data-ttu-id="efb29-109">-sid</span><span class="sxs-lookup"><span data-stu-id="efb29-109">sesid</span></span>  
    <span data-ttu-id="efb29-110">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="efb29-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="efb29-111">Die zu verwendende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="efb29-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="efb29-112">database</span><span class="sxs-lookup"><span data-stu-id="efb29-112">database</span></span>  
    <span data-ttu-id="efb29-113">Typ: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="efb29-113">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="efb29-114">Der Pfad zur Datenbankdatei, die erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="efb29-114">The path to the database file to create.</span></span>

<!-- end list -->

  - <span data-ttu-id="efb29-115">maxpages</span><span class="sxs-lookup"><span data-stu-id="efb29-115">maxPages</span></span>  
    <span data-ttu-id="efb29-116">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="efb29-116">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="efb29-117">Die maximale Größe der Datenbank auf Datenbankseiten.</span><span class="sxs-lookup"><span data-stu-id="efb29-117">The maximum size, in database pages, of the database.</span></span> <span data-ttu-id="efb29-118">Das übergeben von 0 bedeutet, dass kein erzwungenes Maximum vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="efb29-118">Passing 0 means there is no enforced maximum.</span></span>

<!-- end list -->

  - <span data-ttu-id="efb29-119">dbid</span><span class="sxs-lookup"><span data-stu-id="efb29-119">dbid</span></span>  
    <span data-ttu-id="efb29-120">Typ: [Microsoft.ISAM.ESENT.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="efb29-120">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="efb29-121">Gibt die dbid der neuen Datenbank zurück.</span><span class="sxs-lookup"><span data-stu-id="efb29-121">Returns the dbid of the new database.</span></span>

<!-- end list -->

  - <span data-ttu-id="efb29-122">grbit</span><span class="sxs-lookup"><span data-stu-id="efb29-122">grbit</span></span>  
    <span data-ttu-id="efb29-123">Typ: [Microsoft. ISAM. ESENT. Interop. kreatedatabasegrbit](./createdatabasegrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="efb29-123">Type: [Microsoft.Isam.Esent.Interop.CreateDatabaseGrbit](./createdatabasegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="efb29-124">Optionen für die Daten Bank Erstellung.</span><span class="sxs-lookup"><span data-stu-id="efb29-124">Database creation options.</span></span>

## <a name="see-also"></a><span data-ttu-id="efb29-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="efb29-125">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="efb29-126">Referenz</span><span class="sxs-lookup"><span data-stu-id="efb29-126">Reference</span></span>

[<span data-ttu-id="efb29-127">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="efb29-127">Api class</span></span>](./api-class.md)

[<span data-ttu-id="efb29-128">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="efb29-128">Api members</span></span>](./api-members.md)

[<span data-ttu-id="efb29-129">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="efb29-129">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
