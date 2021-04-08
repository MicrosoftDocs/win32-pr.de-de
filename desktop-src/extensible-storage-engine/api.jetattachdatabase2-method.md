---
description: Weitere Informationen finden Sie in der API. JetAttachDatabase2-Methode.
title: API. JetAttachDatabase2-Methode
TOCTitle: 'JetAttachDatabase2 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetAttachDatabase2(Microsoft.Isam.Esent.Interop.JET_SESID,System.String,System.Int32,Microsoft.Isam.Esent.Interop.AttachDatabaseGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetattachdatabase2(v=EXCHG.10)
ms:contentKeyID: 55107224
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetAttachDatabase2
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetAttachDatabase2
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 33d91f0746b3ebf178bd61de58919ab99d85b1f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750769"
---
# <a name="apijetattachdatabase2-method"></a><span data-ttu-id="5701b-103">API. JetAttachDatabase2-Methode</span><span class="sxs-lookup"><span data-stu-id="5701b-103">Api.JetAttachDatabase2 method</span></span>

<span data-ttu-id="5701b-104">Fügt eine Datenbankdatei für die Verwendung mit einer Daten Bank Instanz an.</span><span class="sxs-lookup"><span data-stu-id="5701b-104">Attaches a database file for use with a database instance.</span></span> <span data-ttu-id="5701b-105">Damit die Datenbank verwendet werden kann, muss Sie anschließend mit [jetopendatabase (JET_SESID, String, String, JET_DBID, opendatabasegrbit)](./api.jetopendatabase-method.md)geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="5701b-105">In order to use the database, it will need to be subsequently opened with [JetOpenDatabase(JET_SESID, String, String, JET_DBID, OpenDatabaseGrbit)](./api.jetopendatabase-method.md).</span></span>

<span data-ttu-id="5701b-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="5701b-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="5701b-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="5701b-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="5701b-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="5701b-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function JetAttachDatabase2 ( _
    sesid As JET_SESID, _
    database As String, _
    maxPages As Integer, _
    grbit As AttachDatabaseGrbit _
) As JET_wrn
'Usage
Dim sesid As JET_SESID
Dim database As String
Dim maxPages As Integer
Dim grbit As AttachDatabaseGrbit
Dim returnValue As JET_wrn

returnValue = Api.JetAttachDatabase2(sesid, _
    database, maxPages, grbit)
```

``` csharp
public static JET_wrn JetAttachDatabase2(
    JET_SESID sesid,
    string database,
    int maxPages,
    AttachDatabaseGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="5701b-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="5701b-109">Parameters</span></span>

  - <span data-ttu-id="5701b-110">-sid</span><span class="sxs-lookup"><span data-stu-id="5701b-110">sesid</span></span>  
    <span data-ttu-id="5701b-111">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="5701b-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="5701b-112">Die zu verwendende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="5701b-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="5701b-113">database</span><span class="sxs-lookup"><span data-stu-id="5701b-113">database</span></span>  
    <span data-ttu-id="5701b-114">Typ: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="5701b-114">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="5701b-115">Die anzufügende Datenbank.</span><span class="sxs-lookup"><span data-stu-id="5701b-115">The database to attach.</span></span>

<!-- end list -->

  - <span data-ttu-id="5701b-116">maxpages</span><span class="sxs-lookup"><span data-stu-id="5701b-116">maxPages</span></span>  
    <span data-ttu-id="5701b-117">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="5701b-117">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="5701b-118">Die maximale Größe der Datenbank auf Datenbankseiten.</span><span class="sxs-lookup"><span data-stu-id="5701b-118">The maximum size, in database pages, of the database.</span></span> <span data-ttu-id="5701b-119">Das übergeben von 0 bedeutet, dass kein erzwungenes Maximum vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="5701b-119">Passing 0 means there is no enforced maximum.</span></span>

<!-- end list -->

  - <span data-ttu-id="5701b-120">grbit</span><span class="sxs-lookup"><span data-stu-id="5701b-120">grbit</span></span>  
    <span data-ttu-id="5701b-121">Typ: [Microsoft. ISAM. ESENT. Interop. attachdatabasegrbit](./attachdatabasegrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="5701b-121">Type: [Microsoft.Isam.Esent.Interop.AttachDatabaseGrbit](./attachdatabasegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="5701b-122">Optionen anfügen.</span><span class="sxs-lookup"><span data-stu-id="5701b-122">Attach options.</span></span>

#### <a name="return-value"></a><span data-ttu-id="5701b-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5701b-123">Return value</span></span>

<span data-ttu-id="5701b-124">Typ: [Microsoft.ISAM.ESENT.Interop.JET_wrn](./jet-wrn-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="5701b-124">Type: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span></span>  
<span data-ttu-id="5701b-125">Ein ESENT-Warnungs Code.</span><span class="sxs-lookup"><span data-stu-id="5701b-125">An ESENT warning code.</span></span>  

## <a name="see-also"></a><span data-ttu-id="5701b-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5701b-126">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="5701b-127">Referenz</span><span class="sxs-lookup"><span data-stu-id="5701b-127">Reference</span></span>

[<span data-ttu-id="5701b-128">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="5701b-128">Api class</span></span>](./api-class.md)

[<span data-ttu-id="5701b-129">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="5701b-129">Api members</span></span>](./api-members.md)

[<span data-ttu-id="5701b-130">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="5701b-130">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
