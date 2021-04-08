---
description: Weitere Informationen finden Sie in der API. JetCreateIndex2-Methode.
title: API. JetCreateIndex2-Methode
TOCTitle: 'JetCreateIndex2 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetCreateIndex2(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_INDEXCREATE[],System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetcreateindex2(v=EXCHG.10)
ms:contentKeyID: 55100673
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetCreateIndex2
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetCreateIndex2
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b5fa690ed127c41b8a84f5d8aa012510f3a9c3e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862247"
---
# <a name="apijetcreateindex2-method"></a><span data-ttu-id="15a79-103">API. JetCreateIndex2-Methode</span><span class="sxs-lookup"><span data-stu-id="15a79-103">Api.JetCreateIndex2 method</span></span>

<span data-ttu-id="15a79-104">Erstellt Indizes für Daten in einer ESE-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="15a79-104">Creates indexes over data in an ESE database.</span></span>

<span data-ttu-id="15a79-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="15a79-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="15a79-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="15a79-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="15a79-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="15a79-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetCreateIndex2 ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    indexcreates As JET_INDEXCREATE(), _
    numIndexCreates As Integer _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim indexcreates As JET_INDEXCREATE()
Dim numIndexCreates As IntegerApi.JetCreateIndex2(sesid, tableid, _
    indexcreates, numIndexCreates)
```

``` csharp
public static void JetCreateIndex2(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_INDEXCREATE[] indexcreates,
    int numIndexCreates
)
```

#### <a name="parameters"></a><span data-ttu-id="15a79-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="15a79-108">Parameters</span></span>

  - <span data-ttu-id="15a79-109">-sid</span><span class="sxs-lookup"><span data-stu-id="15a79-109">sesid</span></span>  
    <span data-ttu-id="15a79-110">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="15a79-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="15a79-111">Die zu verwendende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="15a79-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="15a79-112">TableID</span><span class="sxs-lookup"><span data-stu-id="15a79-112">tableid</span></span>  
    <span data-ttu-id="15a79-113">Typ: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="15a79-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="15a79-114">Die Tabelle, für die der Index erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="15a79-114">The table to create the index on.</span></span>

<!-- end list -->

  - <span data-ttu-id="15a79-115">indexerererstellung</span><span class="sxs-lookup"><span data-stu-id="15a79-115">indexcreates</span></span>  
    <span data-ttu-id="15a79-116">Sorte \[\]</span><span class="sxs-lookup"><span data-stu-id="15a79-116">Type: \[\]</span></span>  
    
    <span data-ttu-id="15a79-117">Array von-Objekten, die die zu erstellenden Indizes beschreiben.</span><span class="sxs-lookup"><span data-stu-id="15a79-117">Array of objects describing the indexes to be created.</span></span>

<!-- end list -->

  - <span data-ttu-id="15a79-118">numindexererererstellung</span><span class="sxs-lookup"><span data-stu-id="15a79-118">numIndexCreates</span></span>  
    <span data-ttu-id="15a79-119">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="15a79-119">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="15a79-120">Anzahl der Index Beschreibungs Objekte.</span><span class="sxs-lookup"><span data-stu-id="15a79-120">Number of index description objects.</span></span>

## <a name="remarks"></a><span data-ttu-id="15a79-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="15a79-121">Remarks</span></span>

<span data-ttu-id="15a79-122">Wenn Sie mehrere Indizes erstellen (d. h. mit numindexerzes größer als 1), muss diese Methode außerhalb von Transaktionen und mit exklusivem Zugriff auf die Tabelle aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="15a79-122">When creating multiple indexes (i.e. with numIndexCreates greater than 1) this method MUST be called outside of any transactions and with exclusive access to the table.</span></span> <span data-ttu-id="15a79-123">Der von "jetkreatetable" zurückgegebene JET_TABLEID hat einen exlusiven Zugriff, oder die Tabelle kann für exklusiven Zugriff geöffnet werden, indem [denyread](./opentablegrbit-enumeration.md) an [jetopentable (JET_SESID, JET_DBID, String, \[ \] , Int32, opentablegrbit, JET_TABLEID)](./api.jetopentable-method.md)übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="15a79-123">The JET_TABLEID returned by "JetCreateTable" will have exlusive access or the table can be opened for exclusive access by passing [DenyRead](./opentablegrbit-enumeration.md) to [JetOpenTable(JET_SESID, JET_DBID, String, \[\], Int32, OpenTableGrbit, JET_TABLEID)](./api.jetopentable-method.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="15a79-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="15a79-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="15a79-125">Referenz</span><span class="sxs-lookup"><span data-stu-id="15a79-125">Reference</span></span>

[<span data-ttu-id="15a79-126">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="15a79-126">Api class</span></span>](./api-class.md)

[<span data-ttu-id="15a79-127">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="15a79-127">Api members</span></span>](./api-members.md)

[<span data-ttu-id="15a79-128">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="15a79-128">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
