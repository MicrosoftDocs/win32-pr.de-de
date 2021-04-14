---
description: Weitere Informationen finden Sie in der API. tryopentable-Methode.
title: API. tryopentable-Methode
TOCTitle: 'TryOpenTable method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.TryOpenTable(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String,Microsoft.Isam.Esent.Interop.OpenTableGrbit,Microsoft.Isam.Esent.Interop.JET_TABLEID@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.tryopentable(v=EXCHG.10)
ms:contentKeyID: 55100889
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.TryOpenTable
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.TryOpenTable
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 556d3f12f24229326a6b26f357e5b19801119b74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393481"
---
# <a name="apitryopentable-method"></a><span data-ttu-id="39aa8-103">API. tryopentable-Methode</span><span class="sxs-lookup"><span data-stu-id="39aa8-103">Api.TryOpenTable method</span></span>

<span data-ttu-id="39aa8-104">Versuchen Sie, eine Tabelle zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="39aa8-104">Try to open a table.</span></span>

<span data-ttu-id="39aa8-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="39aa8-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="39aa8-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="39aa8-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="39aa8-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="39aa8-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Function TryOpenTable ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tablename As String, _
    grbit As OpenTableGrbit, _
    <OutAttribute> ByRef tableid As JET_TABLEID _
) As Boolean
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim tablename As String
Dim grbit As OpenTableGrbit
Dim tableid As JET_TABLEID
Dim returnValue As Boolean

returnValue = Api.TryOpenTable(sesid, _
    dbid, tablename, grbit, tableid)
```

``` csharp
public static bool TryOpenTable(
    JET_SESID sesid,
    JET_DBID dbid,
    string tablename,
    OpenTableGrbit grbit,
    out JET_TABLEID tableid
)
```

#### <a name="parameters"></a><span data-ttu-id="39aa8-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="39aa8-108">Parameters</span></span>

  - <span data-ttu-id="39aa8-109">-sid</span><span class="sxs-lookup"><span data-stu-id="39aa8-109">sesid</span></span>  
    <span data-ttu-id="39aa8-110">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="39aa8-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="39aa8-111">Die zu verwendende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="39aa8-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="39aa8-112">dbid</span><span class="sxs-lookup"><span data-stu-id="39aa8-112">dbid</span></span>  
    <span data-ttu-id="39aa8-113">Typ: [Microsoft.ISAM.ESENT.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="39aa8-113">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="39aa8-114">Die Datenbank, in der die Tabelle gesucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="39aa8-114">The database to look for the table in.</span></span>

<!-- end list -->

  - <span data-ttu-id="39aa8-115">Tabellenname</span><span class="sxs-lookup"><span data-stu-id="39aa8-115">tablename</span></span>  
    <span data-ttu-id="39aa8-116">Typ: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="39aa8-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="39aa8-117">Der Name der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="39aa8-117">The name of the table.</span></span>

<!-- end list -->

  - <span data-ttu-id="39aa8-118">grbit</span><span class="sxs-lookup"><span data-stu-id="39aa8-118">grbit</span></span>  
    <span data-ttu-id="39aa8-119">Typ: [Microsoft. ISAM. ESENT. Interop. opentablegrbit](./opentablegrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="39aa8-119">Type: [Microsoft.Isam.Esent.Interop.OpenTableGrbit](./opentablegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="39aa8-120">Tabellen Öffnungs Optionen.</span><span class="sxs-lookup"><span data-stu-id="39aa8-120">Table open options.</span></span>

<!-- end list -->

  - <span data-ttu-id="39aa8-121">TableID</span><span class="sxs-lookup"><span data-stu-id="39aa8-121">tableid</span></span>  
    <span data-ttu-id="39aa8-122">Typ: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="39aa8-122">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="39aa8-123">Gibt die geöffnete TableID zurück.</span><span class="sxs-lookup"><span data-stu-id="39aa8-123">Returns the opened tableid.</span></span>

#### <a name="return-value"></a><span data-ttu-id="39aa8-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="39aa8-124">Return value</span></span>

<span data-ttu-id="39aa8-125">Typ: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="39aa8-125">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="39aa8-126">True, wenn die Tabelle geöffnet wurde, false, wenn die Tabelle nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="39aa8-126">True if the table was opened, false if the table doesn't exist.</span></span>  

## <a name="see-also"></a><span data-ttu-id="39aa8-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="39aa8-127">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="39aa8-128">Referenz</span><span class="sxs-lookup"><span data-stu-id="39aa8-128">Reference</span></span>

[<span data-ttu-id="39aa8-129">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="39aa8-129">Api class</span></span>](./api-class.md)

[<span data-ttu-id="39aa8-130">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="39aa8-130">Api members</span></span>](./api-members.md)

[<span data-ttu-id="39aa8-131">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="39aa8-131">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
