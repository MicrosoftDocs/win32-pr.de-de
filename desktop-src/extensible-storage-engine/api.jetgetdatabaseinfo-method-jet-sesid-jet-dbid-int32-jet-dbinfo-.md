---
description: 'Weitere Informationen finden Sie unter: API. jetgetdatabaseingefo-Methode (JET_SESID, JET_DBID, Int32, JET_DbInfo)'
title: API. jetgetdatabaseingefo-Methode (JET_SESID, JET_DBID, Int32, JET_DbInfo)
TOCTitle: JetGetDatabaseInfo method (JET_SESID, JET_DBID, Int32, JET_DbInfo)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetDatabaseInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.Int32@,Microsoft.Isam.Esent.Interop.JET_DbInfo)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetdatabaseinfo(v=EXCHG.10)
ms:contentKeyID: 55100711
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetDatabaseInfo
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 522b0bff93fe1bc224da4175725c89642547270f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484531"
---
# <a name="apijetgetdatabaseinfo-method-jet_sesid-jet_dbid-int32-jet_dbinfo"></a><span data-ttu-id="eb7d2-103">API. jetgetdatabaseingefo-Methode (JET_SESID, JET_DBID, Int32, JET_DbInfo)</span><span class="sxs-lookup"><span data-stu-id="eb7d2-103">Api.JetGetDatabaseInfo method (JET_SESID, JET_DBID, Int32, JET_DbInfo)</span></span>

<span data-ttu-id="eb7d2-104">Ruft bestimmte Informationen über die angegebene Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="eb7d2-104">Retrieves certain information about the given database.</span></span>

<span data-ttu-id="eb7d2-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="eb7d2-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="eb7d2-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="eb7d2-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="eb7d2-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="eb7d2-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetDatabaseInfo ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    <OutAttribute> ByRef value As Integer, _
    infoLevel As JET_DbInfo _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim value As Integer
Dim infoLevel As JET_DbInfoApi.JetGetDatabaseInfo(sesid, dbid, _
    value, infoLevel)
```

``` csharp
public static void JetGetDatabaseInfo(
    JET_SESID sesid,
    JET_DBID dbid,
    out int value,
    JET_DbInfo infoLevel
)
```

#### <a name="parameters"></a><span data-ttu-id="eb7d2-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="eb7d2-108">Parameters</span></span>

  - <span data-ttu-id="eb7d2-109">-sid</span><span class="sxs-lookup"><span data-stu-id="eb7d2-109">sesid</span></span>  
    <span data-ttu-id="eb7d2-110">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="eb7d2-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="eb7d2-111">Die zu verwendende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="eb7d2-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="eb7d2-112">dbid</span><span class="sxs-lookup"><span data-stu-id="eb7d2-112">dbid</span></span>  
    <span data-ttu-id="eb7d2-113">Typ: [Microsoft.ISAM.ESENT.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="eb7d2-113">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="eb7d2-114">Der Datenbankbezeichner.</span><span class="sxs-lookup"><span data-stu-id="eb7d2-114">The database identifier.</span></span>

<!-- end list -->

  - <span data-ttu-id="eb7d2-115">value</span><span class="sxs-lookup"><span data-stu-id="eb7d2-115">value</span></span>  
    <span data-ttu-id="eb7d2-116">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="eb7d2-116">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="eb7d2-117">Der abzurufende Wert.</span><span class="sxs-lookup"><span data-stu-id="eb7d2-117">The value to be retrieved.</span></span>

<!-- end list -->

  - <span data-ttu-id="eb7d2-118">infolevel</span><span class="sxs-lookup"><span data-stu-id="eb7d2-118">infoLevel</span></span>  
    <span data-ttu-id="eb7d2-119">Typ: [Microsoft.ISAM.ESENT.Interop.JET_DbInfo](./jet-dbinfo-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="eb7d2-119">Type: [Microsoft.Isam.Esent.Interop.JET_DbInfo](./jet-dbinfo-enumeration.md)</span></span>  
    
    <span data-ttu-id="eb7d2-120">Die Daten, die abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="eb7d2-120">The specific data to retrieve.</span></span>

## <a name="see-also"></a><span data-ttu-id="eb7d2-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eb7d2-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="eb7d2-122">Referenz</span><span class="sxs-lookup"><span data-stu-id="eb7d2-122">Reference</span></span>

[<span data-ttu-id="eb7d2-123">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="eb7d2-123">Api class</span></span>](./api-class.md)

[<span data-ttu-id="eb7d2-124">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="eb7d2-124">Api members</span></span>](./api-members.md)

[<span data-ttu-id="eb7d2-125">Jetgetdatabaseingefo-Überladung</span><span class="sxs-lookup"><span data-stu-id="eb7d2-125">JetGetDatabaseInfo overload</span></span>](./api.jetgetdatabaseinfo-method.md)

[<span data-ttu-id="eb7d2-126">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="eb7d2-126">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
