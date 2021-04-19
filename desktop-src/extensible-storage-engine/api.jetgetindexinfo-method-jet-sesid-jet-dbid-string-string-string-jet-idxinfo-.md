---
description: 'Weitere Informationen finden Sie unter: API. jetgetindexinfo-Methode (JET_SESID, JET_DBID, Zeichenfolge, Zeichenfolge, Zeichenfolge, JET_IdxInfo)'
title: API. jetgetindexinfo-Methode (JET_SESID, JET_DBID, String, String, String, JET_IdxInfo)
TOCTitle: JetGetIndexInfo method (JET_SESID, JET_DBID, String, String, String, JET_IdxInfo)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetIndexInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String,System.String,System.String@,Microsoft.Isam.Esent.Interop.JET_IdxInfo)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetindexinfo(v=EXCHG.10)
ms:contentKeyID: 55100769
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetIndexInfo
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: eed2ba4a3f578dda966b2b4530f26de25089681e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346287"
---
# <a name="apijetgetindexinfo-method-jet_sesid-jet_dbid-string-string-string-jet_idxinfo"></a><span data-ttu-id="afa90-103">API. jetgetindexinfo-Methode (JET_SESID, JET_DBID, String, String, String, JET_IdxInfo)</span><span class="sxs-lookup"><span data-stu-id="afa90-103">Api.JetGetIndexInfo method (JET_SESID, JET_DBID, String, String, String, JET_IdxInfo)</span></span>

<span data-ttu-id="afa90-104">Ruft Informationen zu Indizes in einer Tabelle ab.</span><span class="sxs-lookup"><span data-stu-id="afa90-104">Retrieves information about indexes on a table.</span></span>

<span data-ttu-id="afa90-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="afa90-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="afa90-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="afa90-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="afa90-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="afa90-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetIndexInfo ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tablename As String, _
    indexname As String, _
    <OutAttribute> ByRef result As String, _
    infoLevel As JET_IdxInfo _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim tablename As String
Dim indexname As String
Dim result As String
Dim infoLevel As JET_IdxInfoApi.JetGetIndexInfo(sesid, dbid, _
    tablename, indexname, result, infoLevel)
```

``` csharp
public static void JetGetIndexInfo(
    JET_SESID sesid,
    JET_DBID dbid,
    string tablename,
    string indexname,
    out string result,
    JET_IdxInfo infoLevel
)
```

#### <a name="parameters"></a><span data-ttu-id="afa90-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="afa90-108">Parameters</span></span>

  - <span data-ttu-id="afa90-109">-sid</span><span class="sxs-lookup"><span data-stu-id="afa90-109">sesid</span></span>  
    <span data-ttu-id="afa90-110">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="afa90-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="afa90-111">Die zu verwendende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="afa90-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="afa90-112">dbid</span><span class="sxs-lookup"><span data-stu-id="afa90-112">dbid</span></span>  
    <span data-ttu-id="afa90-113">Typ: [Microsoft.ISAM.ESENT.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="afa90-113">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="afa90-114">Die zu verwendende Datenbank.</span><span class="sxs-lookup"><span data-stu-id="afa90-114">The database to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="afa90-115">Tabellenname</span><span class="sxs-lookup"><span data-stu-id="afa90-115">tablename</span></span>  
    <span data-ttu-id="afa90-116">Typ: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="afa90-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="afa90-117">Der Name der Tabelle, zu der Indexinformationen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="afa90-117">The name of the table to retrieve index information about.</span></span>

<!-- end list -->

  - <span data-ttu-id="afa90-118">Indexname</span><span class="sxs-lookup"><span data-stu-id="afa90-118">indexname</span></span>  
    <span data-ttu-id="afa90-119">Typ: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="afa90-119">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="afa90-120">Der Name des Indexes, über den Informationen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="afa90-120">The name of the index to retrieve information about.</span></span>

<!-- end list -->

  - <span data-ttu-id="afa90-121">result</span><span class="sxs-lookup"><span data-stu-id="afa90-121">result</span></span>  
    <span data-ttu-id="afa90-122">Typ: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="afa90-122">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="afa90-123">Wird mit Informationen zu Indizes für die Tabelle ausgefüllt.</span><span class="sxs-lookup"><span data-stu-id="afa90-123">Filled in with information about indexes on the table.</span></span>

<!-- end list -->

  - <span data-ttu-id="afa90-124">infolevel</span><span class="sxs-lookup"><span data-stu-id="afa90-124">infoLevel</span></span>  
    <span data-ttu-id="afa90-125">Typ: [Microsoft.ISAM.ESENT.Interop.JET_IdxInfo](./jet-idxinfo-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="afa90-125">Type: [Microsoft.Isam.Esent.Interop.JET_IdxInfo](./jet-idxinfo-enumeration.md)</span></span>  
    
    <span data-ttu-id="afa90-126">Der Typ der abzurufenden Informationen.</span><span class="sxs-lookup"><span data-stu-id="afa90-126">The type of information to retrieve.</span></span>

## <a name="see-also"></a><span data-ttu-id="afa90-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="afa90-127">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="afa90-128">Referenz</span><span class="sxs-lookup"><span data-stu-id="afa90-128">Reference</span></span>

[<span data-ttu-id="afa90-129">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="afa90-129">Api class</span></span>](./api-class.md)

[<span data-ttu-id="afa90-130">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="afa90-130">Api members</span></span>](./api-members.md)

[<span data-ttu-id="afa90-131">Jetgetindexinfo-Überladung</span><span class="sxs-lookup"><span data-stu-id="afa90-131">JetGetIndexInfo overload</span></span>](./api.jetgetindexinfo-method.md)

[<span data-ttu-id="afa90-132">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="afa90-132">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
