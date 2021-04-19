---
description: 'Weitere Informationen finden Sie unter: API. jetgetdatabaseingefo-Methode (JET_SESID, JET_DBID, Zeichenfolge, JET_DbInfo)'
title: API. jetgetdatabaseingefo-Methode (JET_SESID, JET_DBID, Zeichenfolge, JET_DbInfo)
TOCTitle: JetGetDatabaseInfo method (JET_SESID, JET_DBID, String, JET_DbInfo)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetDatabaseInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String@,Microsoft.Isam.Esent.Interop.JET_DbInfo)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetdatabaseinfo(v=EXCHG.10)
ms:contentKeyID: 55100714
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetDatabaseInfo
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d07ce09ac97a59936a47103067b32f348ed2ff56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106339765"
---
# <a name="apijetgetdatabaseinfo-method-jet_sesid-jet_dbid-string-jet_dbinfo"></a><span data-ttu-id="09266-103">API. jetgetdatabaseingefo-Methode (JET_SESID, JET_DBID, Zeichenfolge, JET_DbInfo)</span><span class="sxs-lookup"><span data-stu-id="09266-103">Api.JetGetDatabaseInfo method (JET_SESID, JET_DBID, String, JET_DbInfo)</span></span>

<span data-ttu-id="09266-104">Ruft bestimmte Informationen über die angegebene Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="09266-104">Retrieves certain information about the given database.</span></span>

<span data-ttu-id="09266-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="09266-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="09266-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="09266-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="09266-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="09266-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetDatabaseInfo ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    <OutAttribute> ByRef value As String, _
    infoLevel As JET_DbInfo _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim value As String
Dim infoLevel As JET_DbInfoApi.JetGetDatabaseInfo(sesid, dbid, _
    value, infoLevel)
```

``` csharp
public static void JetGetDatabaseInfo(
    JET_SESID sesid,
    JET_DBID dbid,
    out string value,
    JET_DbInfo infoLevel
)
```

#### <a name="parameters"></a><span data-ttu-id="09266-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="09266-108">Parameters</span></span>

  - <span data-ttu-id="09266-109">-sid</span><span class="sxs-lookup"><span data-stu-id="09266-109">sesid</span></span>  
    <span data-ttu-id="09266-110">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="09266-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="09266-111">Die zu verwendende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="09266-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="09266-112">dbid</span><span class="sxs-lookup"><span data-stu-id="09266-112">dbid</span></span>  
    <span data-ttu-id="09266-113">Typ: [Microsoft.ISAM.ESENT.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="09266-113">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="09266-114">Der Datenbankbezeichner.</span><span class="sxs-lookup"><span data-stu-id="09266-114">The database identifier.</span></span>

<!-- end list -->

  - <span data-ttu-id="09266-115">value</span><span class="sxs-lookup"><span data-stu-id="09266-115">value</span></span>  
    <span data-ttu-id="09266-116">Typ: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="09266-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="09266-117">Der abzurufende Wert.</span><span class="sxs-lookup"><span data-stu-id="09266-117">The value to be retrieved.</span></span>

<!-- end list -->

  - <span data-ttu-id="09266-118">infolevel</span><span class="sxs-lookup"><span data-stu-id="09266-118">infoLevel</span></span>  
    <span data-ttu-id="09266-119">Typ: [Microsoft.ISAM.ESENT.Interop.JET_DbInfo](./jet-dbinfo-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="09266-119">Type: [Microsoft.Isam.Esent.Interop.JET_DbInfo](./jet-dbinfo-enumeration.md)</span></span>  
    
    <span data-ttu-id="09266-120">Die Daten, die abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="09266-120">The specific data to retrieve.</span></span>

## <a name="see-also"></a><span data-ttu-id="09266-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="09266-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="09266-122">Referenz</span><span class="sxs-lookup"><span data-stu-id="09266-122">Reference</span></span>

[<span data-ttu-id="09266-123">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="09266-123">Api class</span></span>](./api-class.md)

[<span data-ttu-id="09266-124">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="09266-124">Api members</span></span>](./api-members.md)

[<span data-ttu-id="09266-125">Jetgetdatabaseingefo-Überladung</span><span class="sxs-lookup"><span data-stu-id="09266-125">JetGetDatabaseInfo overload</span></span>](./api.jetgetdatabaseinfo-method.md)

[<span data-ttu-id="09266-126">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="09266-126">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
