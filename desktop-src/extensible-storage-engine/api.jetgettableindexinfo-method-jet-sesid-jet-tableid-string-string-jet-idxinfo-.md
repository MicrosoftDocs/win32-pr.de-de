---
description: 'Weitere Informationen finden Sie unter: API. jetgettableindexinfo-Methode (JET_SESID, JET_TABLEID, Zeichenfolge, Zeichenfolge, JET_IdxInfo)'
title: API. jetgettableindexinfo-Methode (JET_SESID, JET_TABLEID, Zeichenfolge, Zeichenfolge, JET_IdxInfo)
TOCTitle: JetGetTableIndexInfo method (JET_SESID, JET_TABLEID, String, String, JET_IdxInfo)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetTableIndexInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.String,System.String@,Microsoft.Isam.Esent.Interop.JET_IdxInfo)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgettableindexinfo(v=EXCHG.10)
ms:contentKeyID: 55100750
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetTableIndexInfo
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 62291587ca1c07da74c2b646870751f3b8af981b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350507"
---
# <a name="apijetgettableindexinfo-method-jet_sesid-jet_tableid-string-string-jet_idxinfo"></a><span data-ttu-id="a06b2-103">API. jetgettableindexinfo-Methode (JET_SESID, JET_TABLEID, Zeichenfolge, Zeichenfolge, JET_IdxInfo)</span><span class="sxs-lookup"><span data-stu-id="a06b2-103">Api.JetGetTableIndexInfo method (JET_SESID, JET_TABLEID, String, String, JET_IdxInfo)</span></span>

<span data-ttu-id="a06b2-104">Ruft Informationen zu Indizes in einer Tabelle ab.</span><span class="sxs-lookup"><span data-stu-id="a06b2-104">Retrieves information about indexes on a table.</span></span>

<span data-ttu-id="a06b2-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="a06b2-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="a06b2-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="a06b2-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="a06b2-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="a06b2-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetTableIndexInfo ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    indexname As String, _
    <OutAttribute> ByRef result As String, _
    infoLevel As JET_IdxInfo _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim indexname As String
Dim result As String
Dim infoLevel As JET_IdxInfoApi.JetGetTableIndexInfo(sesid, _
    tableid, indexname, result, infoLevel)
```

``` csharp
public static void JetGetTableIndexInfo(
    JET_SESID sesid,
    JET_TABLEID tableid,
    string indexname,
    out string result,
    JET_IdxInfo infoLevel
)
```

#### <a name="parameters"></a><span data-ttu-id="a06b2-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="a06b2-108">Parameters</span></span>

  - <span data-ttu-id="a06b2-109">-sid</span><span class="sxs-lookup"><span data-stu-id="a06b2-109">sesid</span></span>  
    <span data-ttu-id="a06b2-110">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="a06b2-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="a06b2-111">Die zu verwendende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="a06b2-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="a06b2-112">TableID</span><span class="sxs-lookup"><span data-stu-id="a06b2-112">tableid</span></span>  
    <span data-ttu-id="a06b2-113">Typ: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="a06b2-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="a06b2-114">Die Tabelle, für die Indexinformationen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a06b2-114">The table to retrieve index information about.</span></span>

<!-- end list -->

  - <span data-ttu-id="a06b2-115">Indexname</span><span class="sxs-lookup"><span data-stu-id="a06b2-115">indexname</span></span>  
    <span data-ttu-id="a06b2-116">Typ: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="a06b2-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="a06b2-117">Der Name des Index.</span><span class="sxs-lookup"><span data-stu-id="a06b2-117">The name of the index.</span></span>

<!-- end list -->

  - <span data-ttu-id="a06b2-118">result</span><span class="sxs-lookup"><span data-stu-id="a06b2-118">result</span></span>  
    <span data-ttu-id="a06b2-119">Typ: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="a06b2-119">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="a06b2-120">Wird mit Informationen zu Indizes für die Tabelle ausgefüllt.</span><span class="sxs-lookup"><span data-stu-id="a06b2-120">Filled in with information about indexes on the table.</span></span>

<!-- end list -->

  - <span data-ttu-id="a06b2-121">infolevel</span><span class="sxs-lookup"><span data-stu-id="a06b2-121">infoLevel</span></span>  
    <span data-ttu-id="a06b2-122">Typ: [Microsoft.ISAM.ESENT.Interop.JET_IdxInfo](./jet-idxinfo-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="a06b2-122">Type: [Microsoft.Isam.Esent.Interop.JET_IdxInfo](./jet-idxinfo-enumeration.md)</span></span>  
    
    <span data-ttu-id="a06b2-123">Der Typ der abzurufenden Informationen.</span><span class="sxs-lookup"><span data-stu-id="a06b2-123">The type of information to retrieve.</span></span>

## <a name="see-also"></a><span data-ttu-id="a06b2-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a06b2-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a06b2-125">Referenz</span><span class="sxs-lookup"><span data-stu-id="a06b2-125">Reference</span></span>

[<span data-ttu-id="a06b2-126">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="a06b2-126">Api class</span></span>](./api-class.md)

[<span data-ttu-id="a06b2-127">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="a06b2-127">Api members</span></span>](./api-members.md)

[<span data-ttu-id="a06b2-128">Jetgettableindexinfo-Überladung</span><span class="sxs-lookup"><span data-stu-id="a06b2-128">JetGetTableIndexInfo overload</span></span>](./api.jetgettableindexinfo-method.md)

[<span data-ttu-id="a06b2-129">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="a06b2-129">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
