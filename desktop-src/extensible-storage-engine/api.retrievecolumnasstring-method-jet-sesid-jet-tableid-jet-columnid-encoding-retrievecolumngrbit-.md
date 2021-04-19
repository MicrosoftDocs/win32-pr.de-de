---
description: 'Weitere Informationen finden Sie unter: API. retrievecolennasstring-Methode (JET_SESID, JET_TABLEID, JET_COLUMNID, Encoding, retrievecolenngrbit)'
title: API. retrievecolennasstring-Methode (JET_SESID, JET_TABLEID, JET_COLUMNID, Encoding, retrievecolenngrbit)
TOCTitle: RetrieveColumnAsString method (JET_SESID, JET_TABLEID, JET_COLUMNID, Encoding, RetrieveColumnGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsString(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,System.Text.Encoding,Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievecolumnasstring(v=EXCHG.10)
ms:contentKeyID: 55100862
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsString
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2008726577bac37e129a887af2d8b1747323c81c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106361724"
---
# <a name="apiretrievecolumnasstring-method-jet_sesid-jet_tableid-jet_columnid-encoding-retrievecolumngrbit"></a><span data-ttu-id="bfa32-103">API. retrievecolennasstring-Methode (JET_SESID, JET_TABLEID, JET_COLUMNID, Encoding, retrievecolenngrbit)</span><span class="sxs-lookup"><span data-stu-id="bfa32-103">Api.RetrieveColumnAsString method (JET_SESID, JET_TABLEID, JET_COLUMNID, Encoding, RetrieveColumnGrbit)</span></span>

<span data-ttu-id="bfa32-104">Ruft einen Zeichen folgen Spaltenwert aus dem aktuellen Datensatz ab.</span><span class="sxs-lookup"><span data-stu-id="bfa32-104">Retrieves a string column value from the current record.</span></span> <span data-ttu-id="bfa32-105">Der Datensatz ist der Datensatz, der mit dem Index Eintrag an der aktuellen Position des Cursors verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="bfa32-105">The record is that record associated with the index entry at the current position of the cursor.</span></span>

<span data-ttu-id="bfa32-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="bfa32-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="bfa32-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="bfa32-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="bfa32-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="bfa32-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function RetrieveColumnAsString ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    encoding As Encoding, _
    grbit As RetrieveColumnGrbit _
) As String
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim encoding As Encoding
Dim grbit As RetrieveColumnGrbit
Dim returnValue As String

returnValue = Api.RetrieveColumnAsString(sesid, _
    tableid, columnid, encoding, grbit)
```

``` csharp
public static string RetrieveColumnAsString(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    Encoding encoding,
    RetrieveColumnGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="bfa32-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="bfa32-109">Parameters</span></span>

  - <span data-ttu-id="bfa32-110">-sid</span><span class="sxs-lookup"><span data-stu-id="bfa32-110">sesid</span></span>  
    <span data-ttu-id="bfa32-111">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="bfa32-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="bfa32-112">Die zu verwendende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="bfa32-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="bfa32-113">TableID</span><span class="sxs-lookup"><span data-stu-id="bfa32-113">tableid</span></span>  
    <span data-ttu-id="bfa32-114">Typ: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="bfa32-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="bfa32-115">Der Cursor, von dem die Spalte abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="bfa32-115">The cursor to retrieve the column from.</span></span>

<!-- end list -->

  - <span data-ttu-id="bfa32-116">columnid</span><span class="sxs-lookup"><span data-stu-id="bfa32-116">columnid</span></span>  
    <span data-ttu-id="bfa32-117">Typ: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="bfa32-117">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="bfa32-118">Das abzurufende ColumnID.</span><span class="sxs-lookup"><span data-stu-id="bfa32-118">The columnid to retrieve.</span></span>

<!-- end list -->

  - <span data-ttu-id="bfa32-119">encoding</span><span class="sxs-lookup"><span data-stu-id="bfa32-119">encoding</span></span>  
    <span data-ttu-id="bfa32-120">Typ: [System. Text. Encoding](/dotnet/api/system.text.encoding)</span><span class="sxs-lookup"><span data-stu-id="bfa32-120">Type: [System.Text.Encoding](/dotnet/api/system.text.encoding)</span></span>  
    
    <span data-ttu-id="bfa32-121">Die Zeichen folgen Codierung, die beim wandeln von Daten verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="bfa32-121">The string encoding to use when converting data.</span></span>

<!-- end list -->

  - <span data-ttu-id="bfa32-122">grbit</span><span class="sxs-lookup"><span data-stu-id="bfa32-122">grbit</span></span>  
    <span data-ttu-id="bfa32-123">Typ: [Microsoft. ISAM. ESENT. Interop. retrievecolenngrbit](./retrievecolumngrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="bfa32-123">Type: [Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit](./retrievecolumngrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="bfa32-124">Abruf Optionen.</span><span class="sxs-lookup"><span data-stu-id="bfa32-124">Retrieval options.</span></span>

#### <a name="return-value"></a><span data-ttu-id="bfa32-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bfa32-125">Return value</span></span>

<span data-ttu-id="bfa32-126">Typ: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="bfa32-126">Type: [System.String](/dotnet/api/system.string)</span></span>  
<span data-ttu-id="bfa32-127">Die aus der Spalte abgerufenen Daten als Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="bfa32-127">The data retrieved from the column as a string.</span></span> <span data-ttu-id="bfa32-128">NULL, wenn die Spalte NULL ist.</span><span class="sxs-lookup"><span data-stu-id="bfa32-128">Null if the column is null.</span></span>  

## <a name="see-also"></a><span data-ttu-id="bfa32-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bfa32-129">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="bfa32-130">Referenz</span><span class="sxs-lookup"><span data-stu-id="bfa32-130">Reference</span></span>

[<span data-ttu-id="bfa32-131">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="bfa32-131">Api class</span></span>](./api-class.md)

[<span data-ttu-id="bfa32-132">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="bfa32-132">Api members</span></span>](./api-members.md)

[<span data-ttu-id="bfa32-133">Retrievecolübernasstring-Überladung</span><span class="sxs-lookup"><span data-stu-id="bfa32-133">RetrieveColumnAsString overload</span></span>](./api.retrievecolumnasstring-method.md)

[<span data-ttu-id="bfa32-134">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="bfa32-134">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
