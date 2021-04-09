---
description: 'Weitere Informationen finden Sie unter: API. jetgetdatabasefileingefo-Methode (String, Int64, JET_DbInfo)'
title: API. jetgetdatabasefileingefo-Methode (String, Int64, JET_DbInfo)
TOCTitle: JetGetDatabaseFileInfo method (String, Int64, JET_DbInfo)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetDatabaseFileInfo(System.String,System.Int64@,Microsoft.Isam.Esent.Interop.JET_DbInfo)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetdatabasefileinfo(v=EXCHG.10)
ms:contentKeyID: 55100700
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetDatabaseFileInfo
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cc036a1c1eceedd39fd265bcf85a2dbaf779a432
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128700"
---
# <a name="apijetgetdatabasefileinfo-method-string-int64-jet_dbinfo"></a><span data-ttu-id="e8ec5-103">API. jetgetdatabasefileingefo-Methode (String, Int64, JET_DbInfo)</span><span class="sxs-lookup"><span data-stu-id="e8ec5-103">Api.JetGetDatabaseFileInfo method (String, Int64, JET_DbInfo)</span></span>

<span data-ttu-id="e8ec5-104">Ruft bestimmte Informationen über die angegebene Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="e8ec5-104">Retrieves certain information about the given database.</span></span>

<span data-ttu-id="e8ec5-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e8ec5-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="e8ec5-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="e8ec5-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e8ec5-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e8ec5-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetDatabaseFileInfo ( _
    databaseName As String, _
    <OutAttribute> ByRef value As Long, _
    infoLevel As JET_DbInfo _
)
'Usage
Dim databaseName As String
Dim value As Long
Dim infoLevel As JET_DbInfoApi.JetGetDatabaseFileInfo(databaseName, _
    value, infoLevel)
```

``` csharp
public static void JetGetDatabaseFileInfo(
    string databaseName,
    out long value,
    JET_DbInfo infoLevel
)
```

#### <a name="parameters"></a><span data-ttu-id="e8ec5-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="e8ec5-108">Parameters</span></span>

  - <span data-ttu-id="e8ec5-109">databaseName</span><span class="sxs-lookup"><span data-stu-id="e8ec5-109">databaseName</span></span>  
    <span data-ttu-id="e8ec5-110">Typ: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="e8ec5-110">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="e8ec5-111">Der Dateiname der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="e8ec5-111">The file name of the database.</span></span>

<!-- end list -->

  - <span data-ttu-id="e8ec5-112">value</span><span class="sxs-lookup"><span data-stu-id="e8ec5-112">value</span></span>  
    <span data-ttu-id="e8ec5-113">Typ: [System. Int64](/dotnet/api/system.int64)</span><span class="sxs-lookup"><span data-stu-id="e8ec5-113">Type: [System.Int64](/dotnet/api/system.int64)</span></span>  
    
    <span data-ttu-id="e8ec5-114">Der abzurufende Wert.</span><span class="sxs-lookup"><span data-stu-id="e8ec5-114">The value to be retrieved.</span></span>

<!-- end list -->

  - <span data-ttu-id="e8ec5-115">infolevel</span><span class="sxs-lookup"><span data-stu-id="e8ec5-115">infoLevel</span></span>  
    <span data-ttu-id="e8ec5-116">Typ: [Microsoft.ISAM.ESENT.Interop.JET_DbInfo](./jet-dbinfo-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="e8ec5-116">Type: [Microsoft.Isam.Esent.Interop.JET_DbInfo](./jet-dbinfo-enumeration.md)</span></span>  
    
    <span data-ttu-id="e8ec5-117">Die Daten, die abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e8ec5-117">The specific data to retrieve.</span></span>

## <a name="see-also"></a><span data-ttu-id="e8ec5-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e8ec5-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e8ec5-119">Referenz</span><span class="sxs-lookup"><span data-stu-id="e8ec5-119">Reference</span></span>

[<span data-ttu-id="e8ec5-120">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="e8ec5-120">Api class</span></span>](./api-class.md)

[<span data-ttu-id="e8ec5-121">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="e8ec5-121">Api members</span></span>](./api-members.md)

[<span data-ttu-id="e8ec5-122">Jetgetdatabasefileingefo-Überladung</span><span class="sxs-lookup"><span data-stu-id="e8ec5-122">JetGetDatabaseFileInfo overload</span></span>](./api.jetgetdatabasefileinfo-method.md)

[<span data-ttu-id="e8ec5-123">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="e8ec5-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
