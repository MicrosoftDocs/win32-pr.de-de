---
description: 'Weitere Informationen finden Sie unter: API. jetgetdatabasefileingefo-Methode (String, JET_DBINFOMISC JET_DbInfo)'
title: API. jetgetdatabasefileingefo-Methode (String, JET_DBINFOMISC JET_DbInfo)
TOCTitle: JetGetDatabaseFileInfo method (String, JET_DBINFOMISC, JET_DbInfo)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetDatabaseFileInfo(System.String,Microsoft.Isam.Esent.Interop.JET_DBINFOMISC@,Microsoft.Isam.Esent.Interop.JET_DbInfo)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetdatabasefileinfo(v=EXCHG.10)
ms:contentKeyID: 55100709
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetDatabaseFileInfo
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d72711314312c843d9e456a5194cb6133b4f491f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128697"
---
# <a name="apijetgetdatabasefileinfo-method-string-jet_dbinfomisc-jet_dbinfo"></a><span data-ttu-id="82373-103">API. jetgetdatabasefileingefo-Methode (String, JET_DBINFOMISC JET_DbInfo)</span><span class="sxs-lookup"><span data-stu-id="82373-103">Api.JetGetDatabaseFileInfo method (String, JET_DBINFOMISC, JET_DbInfo)</span></span>

<span data-ttu-id="82373-104">Ruft bestimmte Informationen über die angegebene Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="82373-104">Retrieves certain information about the given database.</span></span>

<span data-ttu-id="82373-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="82373-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="82373-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="82373-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="82373-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="82373-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetDatabaseFileInfo ( _
    databaseName As String, _
    <OutAttribute> ByRef dbinfomisc As JET_DBINFOMISC, _
    infoLevel As JET_DbInfo _
)
'Usage
Dim databaseName As String
Dim dbinfomisc As JET_DBINFOMISC
Dim infoLevel As JET_DbInfoApi.JetGetDatabaseFileInfo(databaseName, _
    dbinfomisc, infoLevel)
```

``` csharp
public static void JetGetDatabaseFileInfo(
    string databaseName,
    out JET_DBINFOMISC dbinfomisc,
    JET_DbInfo infoLevel
)
```

#### <a name="parameters"></a><span data-ttu-id="82373-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="82373-108">Parameters</span></span>

  - <span data-ttu-id="82373-109">databaseName</span><span class="sxs-lookup"><span data-stu-id="82373-109">databaseName</span></span>  
    <span data-ttu-id="82373-110">Typ: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="82373-110">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="82373-111">Der Dateiname der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="82373-111">The file name of the database.</span></span>

<!-- end list -->

  - <span data-ttu-id="82373-112">dbinfomisc</span><span class="sxs-lookup"><span data-stu-id="82373-112">dbinfomisc</span></span>  
    <span data-ttu-id="82373-113">Typ: [Microsoft.ISAM.ESENT.Interop.JET_DBINFOMISC](./jet-dbinfomisc-class.md)</span><span class="sxs-lookup"><span data-stu-id="82373-113">Type: [Microsoft.Isam.Esent.Interop.JET_DBINFOMISC](./jet-dbinfomisc-class.md)</span></span>  
    
    <span data-ttu-id="82373-114">Der abzurufende Wert.</span><span class="sxs-lookup"><span data-stu-id="82373-114">The value to be retrieved.</span></span>

<!-- end list -->

  - <span data-ttu-id="82373-115">infolevel</span><span class="sxs-lookup"><span data-stu-id="82373-115">infoLevel</span></span>  
    <span data-ttu-id="82373-116">Typ: [Microsoft.ISAM.ESENT.Interop.JET_DbInfo](./jet-dbinfo-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="82373-116">Type: [Microsoft.Isam.Esent.Interop.JET_DbInfo](./jet-dbinfo-enumeration.md)</span></span>  
    
    <span data-ttu-id="82373-117">Die Daten, die abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="82373-117">The specific data to retrieve.</span></span>

## <a name="see-also"></a><span data-ttu-id="82373-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="82373-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="82373-119">Referenz</span><span class="sxs-lookup"><span data-stu-id="82373-119">Reference</span></span>

[<span data-ttu-id="82373-120">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="82373-120">Api class</span></span>](./api-class.md)

[<span data-ttu-id="82373-121">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="82373-121">Api members</span></span>](./api-members.md)

[<span data-ttu-id="82373-122">Jetgetdatabasefileingefo-Überladung</span><span class="sxs-lookup"><span data-stu-id="82373-122">JetGetDatabaseFileInfo overload</span></span>](./api.jetgetdatabasefileinfo-method.md)

[<span data-ttu-id="82373-123">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="82373-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
