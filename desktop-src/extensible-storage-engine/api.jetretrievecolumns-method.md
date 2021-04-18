---
description: Weitere Informationen finden Sie in der API. jetretrievecolumschlag-Methode.
title: API. jetretrievecolumschlag-Methode
TOCTitle: 'JetRetrieveColumns method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetRetrieveColumns(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_RETRIEVECOLUMN[],System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetretrievecolumns(v=EXCHG.10)
ms:contentKeyID: 55100797
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetRetrieveColumns
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetRetrieveColumns
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d3fd4db2ce8cbcad5f74db7d4c95363aa68e9b38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106341194"
---
# <a name="apijetretrievecolumns-method"></a><span data-ttu-id="0b3c2-103">API. jetretrievecolumschlag-Methode</span><span class="sxs-lookup"><span data-stu-id="0b3c2-103">Api.JetRetrieveColumns method</span></span>

<span data-ttu-id="0b3c2-104">Ruft in einem einzelnen Vorgang mehrere Spaltenwerte aus dem aktuellen Datensatz ab.</span><span class="sxs-lookup"><span data-stu-id="0b3c2-104">Retrieves multiple column values from the current record in a single operation.</span></span> <span data-ttu-id="0b3c2-105">Ein Array von JET_RETRIEVECOLUMN Strukturen wird verwendet, um den Satz von Spaltenwerten zu beschreiben, die abgerufen werden sollen, und um Ausgabepuffer für jeden abzurufenden Spaltenwert zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="0b3c2-105">An array of JET_RETRIEVECOLUMN structures is used to describe the set of column values to be retrieved, and to describe output buffers for each column value to be retrieved.</span></span>

<span data-ttu-id="0b3c2-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="0b3c2-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="0b3c2-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="0b3c2-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="0b3c2-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="0b3c2-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function JetRetrieveColumns ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    retrievecolumns As JET_RETRIEVECOLUMN(), _
    numColumns As Integer _
) As JET_wrn
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim retrievecolumns As JET_RETRIEVECOLUMN()
Dim numColumns As Integer
Dim returnValue As JET_wrn

returnValue = Api.JetRetrieveColumns(sesid, _
    tableid, retrievecolumns, numColumns)
```

``` csharp
public static JET_wrn JetRetrieveColumns(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_RETRIEVECOLUMN[] retrievecolumns,
    int numColumns
)
```

#### <a name="parameters"></a><span data-ttu-id="0b3c2-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="0b3c2-109">Parameters</span></span>

  - <span data-ttu-id="0b3c2-110">-sid</span><span class="sxs-lookup"><span data-stu-id="0b3c2-110">sesid</span></span>  
    <span data-ttu-id="0b3c2-111">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="0b3c2-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="0b3c2-112">Die zu verwendende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="0b3c2-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="0b3c2-113">TableID</span><span class="sxs-lookup"><span data-stu-id="0b3c2-113">tableid</span></span>  
    <span data-ttu-id="0b3c2-114">Typ: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="0b3c2-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="0b3c2-115">Der Cursor, von dem die Daten abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="0b3c2-115">The cursor to retrieve the data from.</span></span>

<!-- end list -->

  - <span data-ttu-id="0b3c2-116">Abruf Ereignisse</span><span class="sxs-lookup"><span data-stu-id="0b3c2-116">retrievecolumns</span></span>  
    <span data-ttu-id="0b3c2-117">Sorte \[\]</span><span class="sxs-lookup"><span data-stu-id="0b3c2-117">Type: \[\]</span></span>  
    
    <span data-ttu-id="0b3c2-118">Ein Array aus einem oder mehreren [JET_RETRIEVECOLUMN](./jet-retrievecolumn-class.md) -Objekten, die die abzurufenden Daten beschreiben.</span><span class="sxs-lookup"><span data-stu-id="0b3c2-118">An array of one or more [JET_RETRIEVECOLUMN](./jet-retrievecolumn-class.md) objects describing the data to be retrieved.</span></span>

<!-- end list -->

  - <span data-ttu-id="0b3c2-119">NumColumns</span><span class="sxs-lookup"><span data-stu-id="0b3c2-119">numColumns</span></span>  
    <span data-ttu-id="0b3c2-120">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="0b3c2-120">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="0b3c2-121">Die Anzahl der Einträge im Spalten Array.</span><span class="sxs-lookup"><span data-stu-id="0b3c2-121">The number of entries in the columns array.</span></span>

#### <a name="return-value"></a><span data-ttu-id="0b3c2-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0b3c2-122">Return value</span></span>

<span data-ttu-id="0b3c2-123">Typ: [Microsoft.ISAM.ESENT.Interop.JET_wrn](./jet-wrn-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="0b3c2-123">Type: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span></span>  
<span data-ttu-id="0b3c2-124">Wenn eine abgerufene Spalte aufgrund eines unzureichenden Längen Puffers abgeschnitten wird, gibt die API [buffertruncated](./jet-wrn-enumeration.md)zurück.</span><span class="sxs-lookup"><span data-stu-id="0b3c2-124">If any column retrieved is truncated due to an insufficient length buffer, then the API will return [BufferTruncated](./jet-wrn-enumeration.md).</span></span> <span data-ttu-id="0b3c2-125">Andere Fehler JET_wrnColumnNull werden jedoch nur im Fehler Feld des [JET_RETRIEVECOLUMN](./jet-retrievecolumn-class.md) Objekts zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="0b3c2-125">However other errors JET_wrnColumnNull are returned only in the error field of the [JET_RETRIEVECOLUMN](./jet-retrievecolumn-class.md) object.</span></span>  

## <a name="see-also"></a><span data-ttu-id="0b3c2-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0b3c2-126">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="0b3c2-127">Referenz</span><span class="sxs-lookup"><span data-stu-id="0b3c2-127">Reference</span></span>

[<span data-ttu-id="0b3c2-128">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="0b3c2-128">Api class</span></span>](./api-class.md)

[<span data-ttu-id="0b3c2-129">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="0b3c2-129">Api members</span></span>](./api-members.md)

[<span data-ttu-id="0b3c2-130">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="0b3c2-130">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
