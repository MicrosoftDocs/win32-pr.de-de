---
description: 'Weitere Informationen finden Sie unter: API. jetgetindexinfo-Methode (JET_SESID, JET_DBID, String, String, UInt16, JET_IdxInfo)'
title: API. jetgetindexinfo-Methode (JET_SESID, JET_DBID, String, String, UInt16, JET_IdxInfo)
TOCTitle: JetGetIndexInfo method (JET_SESID, JET_DBID, String, String, UInt16, JET_IdxInfo)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetIndexInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String,System.String,System.UInt16@,Microsoft.Isam.Esent.Interop.JET_IdxInfo)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetindexinfo(v=EXCHG.10)
ms:contentKeyID: 55100771
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetIndexInfo
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 762437dba9e502de5c0650e4ae6df53d4629d791
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347126"
---
# <a name="apijetgetindexinfo-method-jet_sesid-jet_dbid-string-string-uint16-jet_idxinfo"></a><span data-ttu-id="cc70a-103">API. jetgetindexinfo-Methode (JET_SESID, JET_DBID, String, String, UInt16, JET_IdxInfo)</span><span class="sxs-lookup"><span data-stu-id="cc70a-103">Api.JetGetIndexInfo method (JET_SESID, JET_DBID, String, String, UInt16, JET_IdxInfo)</span></span>

<span data-ttu-id="cc70a-104">Ruft Informationen zu Indizes in einer Tabelle ab.</span><span class="sxs-lookup"><span data-stu-id="cc70a-104">Retrieves information about indexes on a table.</span></span>

<span data-ttu-id="cc70a-105">Diese API ist nicht CLS-kompatibel.</span><span class="sxs-lookup"><span data-stu-id="cc70a-105">This API is not CLS-compliant.</span></span> 

<span data-ttu-id="cc70a-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="cc70a-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="cc70a-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="cc70a-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="cc70a-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="cc70a-108">Syntax</span></span>

``` vb
'Declaration
<CLSCompliantAttribute(False)> _
Public Shared Sub JetGetIndexInfo ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tablename As String, _
    indexname As String, _
    <OutAttribute> ByRef result As UShort, _
    infoLevel As JET_IdxInfo _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim tablename As String
Dim indexname As String
Dim result As UShort
Dim infoLevel As JET_IdxInfoApi.JetGetIndexInfo(sesid, dbid, _
    tablename, indexname, result, infoLevel)
```

``` csharp
[CLSCompliantAttribute(false)]
public static void JetGetIndexInfo(
    JET_SESID sesid,
    JET_DBID dbid,
    string tablename,
    string indexname,
    out ushort result,
    JET_IdxInfo infoLevel
)
```

#### <a name="parameters"></a><span data-ttu-id="cc70a-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="cc70a-109">Parameters</span></span>

  - <span data-ttu-id="cc70a-110">-sid</span><span class="sxs-lookup"><span data-stu-id="cc70a-110">sesid</span></span>  
    <span data-ttu-id="cc70a-111">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="cc70a-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="cc70a-112">Die zu verwendende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="cc70a-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="cc70a-113">dbid</span><span class="sxs-lookup"><span data-stu-id="cc70a-113">dbid</span></span>  
    <span data-ttu-id="cc70a-114">Typ: [Microsoft.ISAM.ESENT.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="cc70a-114">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="cc70a-115">Die zu verwendende Datenbank.</span><span class="sxs-lookup"><span data-stu-id="cc70a-115">The database to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="cc70a-116">Tabellenname</span><span class="sxs-lookup"><span data-stu-id="cc70a-116">tablename</span></span>  
    <span data-ttu-id="cc70a-117">Typ: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="cc70a-117">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="cc70a-118">Der Name der Tabelle, zu der Indexinformationen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="cc70a-118">The name of the table to retrieve index information about.</span></span>

<!-- end list -->

  - <span data-ttu-id="cc70a-119">Indexname</span><span class="sxs-lookup"><span data-stu-id="cc70a-119">indexname</span></span>  
    <span data-ttu-id="cc70a-120">Typ: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="cc70a-120">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="cc70a-121">Der Name des Indexes, über den Informationen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="cc70a-121">The name of the index to retrieve information about.</span></span>

<!-- end list -->

  - <span data-ttu-id="cc70a-122">result</span><span class="sxs-lookup"><span data-stu-id="cc70a-122">result</span></span>  
    <span data-ttu-id="cc70a-123">Typ: [System. UInt16](/dotnet/api/system.uint16)</span><span class="sxs-lookup"><span data-stu-id="cc70a-123">Type: [System.UInt16](/dotnet/api/system.uint16)</span></span>  
    
    <span data-ttu-id="cc70a-124">Wird mit Informationen zu Indizes für die Tabelle ausgefüllt.</span><span class="sxs-lookup"><span data-stu-id="cc70a-124">Filled in with information about indexes on the table.</span></span>

<!-- end list -->

  - <span data-ttu-id="cc70a-125">infolevel</span><span class="sxs-lookup"><span data-stu-id="cc70a-125">infoLevel</span></span>  
    <span data-ttu-id="cc70a-126">Typ: [Microsoft.ISAM.ESENT.Interop.JET_IdxInfo](./jet-idxinfo-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="cc70a-126">Type: [Microsoft.Isam.Esent.Interop.JET_IdxInfo](./jet-idxinfo-enumeration.md)</span></span>  
    
    <span data-ttu-id="cc70a-127">Der Typ der abzurufenden Informationen.</span><span class="sxs-lookup"><span data-stu-id="cc70a-127">The type of information to retrieve.</span></span>

## <a name="see-also"></a><span data-ttu-id="cc70a-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cc70a-128">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="cc70a-129">Referenz</span><span class="sxs-lookup"><span data-stu-id="cc70a-129">Reference</span></span>

[<span data-ttu-id="cc70a-130">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="cc70a-130">Api class</span></span>](./api-class.md)

[<span data-ttu-id="cc70a-131">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="cc70a-131">Api members</span></span>](./api-members.md)

[<span data-ttu-id="cc70a-132">Jetgetindexinfo-Überladung</span><span class="sxs-lookup"><span data-stu-id="cc70a-132">JetGetIndexInfo overload</span></span>](./api.jetgetindexinfo-method.md)

[<span data-ttu-id="cc70a-133">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="cc70a-133">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
