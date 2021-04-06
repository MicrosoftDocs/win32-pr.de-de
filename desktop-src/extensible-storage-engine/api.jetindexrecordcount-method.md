---
description: Weitere Informationen finden Sie in der API. jetindexrecordcount-Methode.
title: API. jetindexrecordcount-Methode
TOCTitle: 'JetIndexRecordCount method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetIndexRecordCount(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Int32@,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetindexrecordcount(v=EXCHG.10)
ms:contentKeyID: 55100758
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetIndexRecordCount
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetIndexRecordCount
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 429239ab7734a594fd2c5a3510650d8f410e94f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759427"
---
# <a name="apijetindexrecordcount-method"></a><span data-ttu-id="37ad6-103">API. jetindexrecordcount-Methode</span><span class="sxs-lookup"><span data-stu-id="37ad6-103">Api.JetIndexRecordCount method</span></span>

<span data-ttu-id="37ad6-104">Zählt die Anzahl der Einträge im aktuellen Index von der aktuellen Position nach vorne.</span><span class="sxs-lookup"><span data-stu-id="37ad6-104">Counts the number of entries in the current index from the current position forward.</span></span> <span data-ttu-id="37ad6-105">Die aktuelle Position ist in der Anzahl enthalten.</span><span class="sxs-lookup"><span data-stu-id="37ad6-105">The current position is included in the count.</span></span> <span data-ttu-id="37ad6-106">Die Anzahl kann größer als die Gesamtanzahl der Datensätze in der Tabelle sein, wenn der aktuelle Index eine mehrwertige Spalte überschreitet und Instanzen der Spalte mehrere Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="37ad6-106">The count can be greater than the total number of records in the table if the current index is over a multi-valued column and instances of the column have multiple-values.</span></span> <span data-ttu-id="37ad6-107">Wenn die Tabelle leer ist, wird 0 für die Anzahl zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="37ad6-107">If the table is empty, then 0 will be returned for the count.</span></span>

<span data-ttu-id="37ad6-108">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="37ad6-108">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="37ad6-109">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="37ad6-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="37ad6-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="37ad6-110">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetIndexRecordCount ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    <OutAttribute> ByRef numRecords As Integer, _
    maxRecordsToCount As Integer _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim numRecords As Integer
Dim maxRecordsToCount As IntegerApi.JetIndexRecordCount(sesid, _
    tableid, numRecords, maxRecordsToCount)
```

``` csharp
public static void JetIndexRecordCount(
    JET_SESID sesid,
    JET_TABLEID tableid,
    out int numRecords,
    int maxRecordsToCount
)
```

#### <a name="parameters"></a><span data-ttu-id="37ad6-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="37ad6-111">Parameters</span></span>

  - <span data-ttu-id="37ad6-112">-sid</span><span class="sxs-lookup"><span data-stu-id="37ad6-112">sesid</span></span>  
    <span data-ttu-id="37ad6-113">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="37ad6-113">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="37ad6-114">Die zu verwendende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="37ad6-114">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="37ad6-115">TableID</span><span class="sxs-lookup"><span data-stu-id="37ad6-115">tableid</span></span>  
    <span data-ttu-id="37ad6-116">Typ: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="37ad6-116">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="37ad6-117">Der Cursor, in dem die Datensätze gezählt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="37ad6-117">The cursor to count the records in.</span></span>

<!-- end list -->

  - <span data-ttu-id="37ad6-118">numrecords</span><span class="sxs-lookup"><span data-stu-id="37ad6-118">numRecords</span></span>  
    <span data-ttu-id="37ad6-119">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="37ad6-119">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="37ad6-120">Gibt die Anzahl von Datensätzen zurück.</span><span class="sxs-lookup"><span data-stu-id="37ad6-120">Returns the number of records.</span></span>

<!-- end list -->

  - <span data-ttu-id="37ad6-121">maxrecordstocount</span><span class="sxs-lookup"><span data-stu-id="37ad6-121">maxRecordsToCount</span></span>  
    <span data-ttu-id="37ad6-122">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="37ad6-122">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="37ad6-123">Die maximale Anzahl der zu zählenden Datensätze.</span><span class="sxs-lookup"><span data-stu-id="37ad6-123">The maximum number of records to count.</span></span> <span data-ttu-id="37ad6-124">Der Wert 0 gibt an, dass die Anzahl unbegrenzt ist.</span><span class="sxs-lookup"><span data-stu-id="37ad6-124">A value of 0 indicates that the count is unlimited.</span></span>

## <a name="see-also"></a><span data-ttu-id="37ad6-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="37ad6-125">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="37ad6-126">Referenz</span><span class="sxs-lookup"><span data-stu-id="37ad6-126">Reference</span></span>

[<span data-ttu-id="37ad6-127">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="37ad6-127">Api class</span></span>](./api-class.md)

[<span data-ttu-id="37ad6-128">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="37ad6-128">Api members</span></span>](./api-members.md)

[<span data-ttu-id="37ad6-129">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="37ad6-129">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
