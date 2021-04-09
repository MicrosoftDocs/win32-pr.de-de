---
description: 'Weitere Informationen über: Windows8Api. JetCreateIndex4-Methode'
title: Windows8Api. JetCreateIndex4-Methode (Microsoft. ISAM. ESENT. Interop. Windows8)
TOCTitle: 'JetCreateIndex4 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetCreateIndex4(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_INDEXCREATE[],System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.windows8api.jetcreateindex4(v=EXCHG.10)
ms:contentKeyID: 55104455
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetCreateIndex4
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetCreateIndex4
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8cc06fa47b8463c6c3b731a7e0e06b7ba13ae687
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130373"
---
# <a name="windows8apijetcreateindex4-method"></a><span data-ttu-id="551e5-103">Windows8Api. JetCreateIndex4-Methode</span><span class="sxs-lookup"><span data-stu-id="551e5-103">Windows8Api.JetCreateIndex4 method</span></span>

<span data-ttu-id="551e5-104">Erstellt Indizes für Daten in einer ESE-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="551e5-104">Creates indexes over data in an ESE database.</span></span>

<span data-ttu-id="551e5-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="551e5-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="551e5-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="551e5-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="551e5-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="551e5-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetCreateIndex4 ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    indexcreates As JET_INDEXCREATE(), _
    numIndexCreates As Integer _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim indexcreates As JET_INDEXCREATE()
Dim numIndexCreates As IntegerWindows8Api.JetCreateIndex4(sesid, tableid, _
    indexcreates, numIndexCreates)
```

``` csharp
public static void JetCreateIndex4(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_INDEXCREATE[] indexcreates,
    int numIndexCreates
)
```

#### <a name="parameters"></a><span data-ttu-id="551e5-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="551e5-108">Parameters</span></span>

  - <span data-ttu-id="551e5-109">-sid</span><span class="sxs-lookup"><span data-stu-id="551e5-109">sesid</span></span>  
    <span data-ttu-id="551e5-110">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="551e5-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="551e5-111">Die zu verwendende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="551e5-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="551e5-112">TableID</span><span class="sxs-lookup"><span data-stu-id="551e5-112">tableid</span></span>  
    <span data-ttu-id="551e5-113">Typ: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="551e5-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="551e5-114">Die Tabelle, für die der Index erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="551e5-114">The table to create the index on.</span></span>

<!-- end list -->

  - <span data-ttu-id="551e5-115">indexerererstellung</span><span class="sxs-lookup"><span data-stu-id="551e5-115">indexcreates</span></span>  
    <span data-ttu-id="551e5-116">Sorte \[\]</span><span class="sxs-lookup"><span data-stu-id="551e5-116">Type: \[\]</span></span>  
    
    <span data-ttu-id="551e5-117">Array von-Objekten, die die zu erstellenden Indizes beschreiben.</span><span class="sxs-lookup"><span data-stu-id="551e5-117">Array of objects describing the indexes to be created.</span></span>

<!-- end list -->

  - <span data-ttu-id="551e5-118">numindexererererstellung</span><span class="sxs-lookup"><span data-stu-id="551e5-118">numIndexCreates</span></span>  
    <span data-ttu-id="551e5-119">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="551e5-119">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="551e5-120">Anzahl der Index Beschreibungs Objekte.</span><span class="sxs-lookup"><span data-stu-id="551e5-120">Number of index description objects.</span></span>

## <a name="remarks"></a><span data-ttu-id="551e5-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="551e5-121">Remarks</span></span>

<span data-ttu-id="551e5-122">Wenn Sie mehrere Indizes erstellen (d. h. mit numindexerzes größer als 1), muss diese Methode außerhalb von Transaktionen und mit exklusivem Zugriff auf die Tabelle aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="551e5-122">When creating multiple indexes (i.e. with numIndexCreates greater than 1) this method MUST be called outside of any transactions and with exclusive access to the table.</span></span> <span data-ttu-id="551e5-123">Der von "API. jetkreatetable" zurückgegebene JET_TABLEID hat einen exlusiven Zugriff, oder die Tabelle kann für exklusiven Zugriff geöffnet werden, indem [denyread](./opentablegrbit-enumeration.md) an [jetopentable (JET_SESID, JET_DBID, String, \[ \] , Int32, opentablegrbit, JET_TABLEID)](./api.jetopentable-method.md)übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="551e5-123">The JET_TABLEID returned by "Api.JetCreateTable" will have exlusive access or the table can be opened for exclusive access by passing [DenyRead](./opentablegrbit-enumeration.md) to [JetOpenTable(JET_SESID, JET_DBID, String, \[\], Int32, OpenTableGrbit, JET_TABLEID)](./api.jetopentable-method.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="551e5-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="551e5-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="551e5-125">Referenz</span><span class="sxs-lookup"><span data-stu-id="551e5-125">Reference</span></span>

[<span data-ttu-id="551e5-126">Windows8Api-Klasse</span><span class="sxs-lookup"><span data-stu-id="551e5-126">Windows8Api class</span></span>](./windows8api-class.md)

[<span data-ttu-id="551e5-127">Windows8Api-Member</span><span class="sxs-lookup"><span data-stu-id="551e5-127">Windows8Api members</span></span>](./windows8api-members.md)

[<span data-ttu-id="551e5-128">Microsoft. ISAM. ESENT. Interop. Windows8-Namespace</span><span class="sxs-lookup"><span data-stu-id="551e5-128">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
