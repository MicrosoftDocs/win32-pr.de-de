---
description: 'Weitere Informationen finden Sie unter: API. retrievecolennasstring-Methode (JET_SESID, JET_TABLEID, JET_COLUMNID, Codierung)'
title: API. retrievecolennasstring-Methode (JET_SESID, JET_TABLEID, JET_COLUMNID, Codierung)
TOCTitle: RetrieveColumnAsString method (JET_SESID, JET_TABLEID, JET_COLUMNID, Encoding)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsString(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,System.Text.Encoding)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievecolumnasstring(v=EXCHG.10)
ms:contentKeyID: 55100899
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsString
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1d7ec3bac73f5b82f82d2762a34084de25b63f82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106341164"
---
# <a name="apiretrievecolumnasstring-method-jet_sesid-jet_tableid-jet_columnid-encoding"></a><span data-ttu-id="9bb47-103">API. retrievecolennasstring-Methode (JET_SESID, JET_TABLEID, JET_COLUMNID, Codierung)</span><span class="sxs-lookup"><span data-stu-id="9bb47-103">Api.RetrieveColumnAsString method (JET_SESID, JET_TABLEID, JET_COLUMNID, Encoding)</span></span>

<span data-ttu-id="9bb47-104">Ruft einen Zeichen folgen Spaltenwert aus dem aktuellen Datensatz ab.</span><span class="sxs-lookup"><span data-stu-id="9bb47-104">Retrieves a string column value from the current record.</span></span> <span data-ttu-id="9bb47-105">Der Datensatz ist der Datensatz, der mit dem Index Eintrag an der aktuellen Position des Cursors verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="9bb47-105">The record is that record associated with the index entry at the current position of the cursor.</span></span>

<span data-ttu-id="9bb47-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="9bb47-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="9bb47-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="9bb47-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="9bb47-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="9bb47-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function RetrieveColumnAsString ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    encoding As Encoding _
) As String
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim encoding As Encoding
Dim returnValue As String

returnValue = Api.RetrieveColumnAsString(sesid, _
    tableid, columnid, encoding)
```

``` csharp
public static string RetrieveColumnAsString(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    Encoding encoding
)
```

#### <a name="parameters"></a><span data-ttu-id="9bb47-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="9bb47-109">Parameters</span></span>

  - <span data-ttu-id="9bb47-110">-sid</span><span class="sxs-lookup"><span data-stu-id="9bb47-110">sesid</span></span>  
    <span data-ttu-id="9bb47-111">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="9bb47-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="9bb47-112">Die zu verwendende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="9bb47-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="9bb47-113">TableID</span><span class="sxs-lookup"><span data-stu-id="9bb47-113">tableid</span></span>  
    <span data-ttu-id="9bb47-114">Typ: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="9bb47-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="9bb47-115">Der Cursor, von dem die Spalte abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="9bb47-115">The cursor to retrieve the column from.</span></span>

<!-- end list -->

  - <span data-ttu-id="9bb47-116">columnid</span><span class="sxs-lookup"><span data-stu-id="9bb47-116">columnid</span></span>  
    <span data-ttu-id="9bb47-117">Typ: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="9bb47-117">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="9bb47-118">Das abzurufende ColumnID.</span><span class="sxs-lookup"><span data-stu-id="9bb47-118">The columnid to retrieve.</span></span>

<!-- end list -->

  - <span data-ttu-id="9bb47-119">encoding</span><span class="sxs-lookup"><span data-stu-id="9bb47-119">encoding</span></span>  
    <span data-ttu-id="9bb47-120">Typ: [System. Text. Encoding](/dotnet/api/system.text.encoding)</span><span class="sxs-lookup"><span data-stu-id="9bb47-120">Type: [System.Text.Encoding](/dotnet/api/system.text.encoding)</span></span>  
    
    <span data-ttu-id="9bb47-121">Die Zeichen folgen Codierung, die beim wandeln von Daten verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="9bb47-121">The string encoding to use when converting data.</span></span>

#### <a name="return-value"></a><span data-ttu-id="9bb47-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9bb47-122">Return value</span></span>

<span data-ttu-id="9bb47-123">Typ: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="9bb47-123">Type: [System.String](/dotnet/api/system.string)</span></span>  
<span data-ttu-id="9bb47-124">Die aus der Spalte abgerufenen Daten als Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="9bb47-124">The data retrieved from the column as a string.</span></span> <span data-ttu-id="9bb47-125">NULL, wenn die Spalte NULL ist.</span><span class="sxs-lookup"><span data-stu-id="9bb47-125">Null if the column is null.</span></span>  

## <a name="see-also"></a><span data-ttu-id="9bb47-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9bb47-126">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="9bb47-127">Referenz</span><span class="sxs-lookup"><span data-stu-id="9bb47-127">Reference</span></span>

[<span data-ttu-id="9bb47-128">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="9bb47-128">Api class</span></span>](./api-class.md)

[<span data-ttu-id="9bb47-129">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="9bb47-129">Api members</span></span>](./api-members.md)

[<span data-ttu-id="9bb47-130">Retrievecolübernasstring-Überladung</span><span class="sxs-lookup"><span data-stu-id="9bb47-130">RetrieveColumnAsString overload</span></span>](./api.retrievecolumnasstring-method.md)

[<span data-ttu-id="9bb47-131">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="9bb47-131">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
