---
description: Weitere Informationen finden Sie in der API. jetopedatabase-Methode.
title: API. jetopdendatabase-Methode
TOCTitle: 'JetOpenDatabase method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetOpenDatabase(Microsoft.Isam.Esent.Interop.JET_SESID,System.String,System.String,Microsoft.Isam.Esent.Interop.JET_DBID@,Microsoft.Isam.Esent.Interop.OpenDatabaseGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetopendatabase(v=EXCHG.10)
ms:contentKeyID: 55100768
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetOpenDatabase
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetOpenDatabase
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: faaff0eec2b5bc8a2c2f2a72a61f9f6a23f7d972
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218285"
---
# <a name="apijetopendatabase-method"></a><span data-ttu-id="9918d-103">API. jetopdendatabase-Methode</span><span class="sxs-lookup"><span data-stu-id="9918d-103">Api.JetOpenDatabase method</span></span>

<span data-ttu-id="9918d-104">Öffnet eine Datenbank, die zuvor mit [jetattachdatabase (JET_SESID, String, attachdatabasegrbit)](./api.jetattachdatabase-method.md)angefügt wurde, damit Sie mit einer Daten banksitzung verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="9918d-104">Opens a database previously attached with [JetAttachDatabase(JET_SESID, String, AttachDatabaseGrbit)](./api.jetattachdatabase-method.md), for use with a database session.</span></span> <span data-ttu-id="9918d-105">Diese Funktion kann für dieselbe Datenbank mehrmals aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="9918d-105">This function can be called multiple times for the same database.</span></span>

<span data-ttu-id="9918d-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="9918d-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="9918d-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="9918d-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="9918d-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="9918d-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function JetOpenDatabase ( _
    sesid As JET_SESID, _
    database As String, _
    connect As String, _
    <OutAttribute> ByRef dbid As JET_DBID, _
    grbit As OpenDatabaseGrbit _
) As JET_wrn
'Usage
Dim sesid As JET_SESID
Dim database As String
Dim connect As String
Dim dbid As JET_DBID
Dim grbit As OpenDatabaseGrbit
Dim returnValue As JET_wrn

returnValue = Api.JetOpenDatabase(sesid, _
    database, connect, dbid, grbit)
```

``` csharp
public static JET_wrn JetOpenDatabase(
    JET_SESID sesid,
    string database,
    string connect,
    out JET_DBID dbid,
    OpenDatabaseGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="9918d-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="9918d-109">Parameters</span></span>

  - <span data-ttu-id="9918d-110">-sid</span><span class="sxs-lookup"><span data-stu-id="9918d-110">sesid</span></span>  
    <span data-ttu-id="9918d-111">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="9918d-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="9918d-112">Die Sitzung, von der die Datenbank geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="9918d-112">The session that is opening the database.</span></span>

<!-- end list -->

  - <span data-ttu-id="9918d-113">database</span><span class="sxs-lookup"><span data-stu-id="9918d-113">database</span></span>  
    <span data-ttu-id="9918d-114">Typ: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="9918d-114">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="9918d-115">Die Datenbank, die geöffnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="9918d-115">The database to open.</span></span>

<!-- end list -->

  - <span data-ttu-id="9918d-116">Verbinden</span><span class="sxs-lookup"><span data-stu-id="9918d-116">connect</span></span>  
    <span data-ttu-id="9918d-117">Typ: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="9918d-117">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="9918d-118">Für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="9918d-118">Reserved for future use.</span></span>

<!-- end list -->

  - <span data-ttu-id="9918d-119">dbid</span><span class="sxs-lookup"><span data-stu-id="9918d-119">dbid</span></span>  
    <span data-ttu-id="9918d-120">Typ: [Microsoft.ISAM.ESENT.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="9918d-120">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="9918d-121">Gibt das dbid der angefügten Datenbank zurück.</span><span class="sxs-lookup"><span data-stu-id="9918d-121">Returns the dbid of the attached database.</span></span>

<!-- end list -->

  - <span data-ttu-id="9918d-122">grbit</span><span class="sxs-lookup"><span data-stu-id="9918d-122">grbit</span></span>  
    <span data-ttu-id="9918d-123">Typ: [Microsoft. ISAM. ESENT. Interop. opendatabasegrbit](./opendatabasegrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="9918d-123">Type: [Microsoft.Isam.Esent.Interop.OpenDatabaseGrbit](./opendatabasegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="9918d-124">Öffnen Sie Daten Bankoptionen.</span><span class="sxs-lookup"><span data-stu-id="9918d-124">Open database options.</span></span>

#### <a name="return-value"></a><span data-ttu-id="9918d-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9918d-125">Return value</span></span>

<span data-ttu-id="9918d-126">Typ: [Microsoft.ISAM.ESENT.Interop.JET_wrn](./jet-wrn-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="9918d-126">Type: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span></span>  
<span data-ttu-id="9918d-127">Ein ESENT-Warnungs Code.</span><span class="sxs-lookup"><span data-stu-id="9918d-127">An ESENT warning code.</span></span>  

## <a name="see-also"></a><span data-ttu-id="9918d-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9918d-128">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="9918d-129">Referenz</span><span class="sxs-lookup"><span data-stu-id="9918d-129">Reference</span></span>

[<span data-ttu-id="9918d-130">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="9918d-130">Api class</span></span>](./api-class.md)

[<span data-ttu-id="9918d-131">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="9918d-131">Api members</span></span>](./api-members.md)

[<span data-ttu-id="9918d-132">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="9918d-132">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
