---
description: Weitere Informationen finden Sie in der API. jetdupcursor-Methode.
title: API. jetdupcursor-Methode
TOCTitle: 'JetDupCursor method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetDupCursor(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_TABLEID@,Microsoft.Isam.Esent.Interop.DupCursorGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetdupcursor(v=EXCHG.10)
ms:contentKeyID: 55100686
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetDupCursor
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetDupCursor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5fce19d23838f3dfeab5317bfa7ea1aaacfcb508
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525631"
---
# <a name="apijetdupcursor-method"></a><span data-ttu-id="545d8-103">API. jetdupcursor-Methode</span><span class="sxs-lookup"><span data-stu-id="545d8-103">Api.JetDupCursor method</span></span>

<span data-ttu-id="545d8-104">Dupliziert einen geöffneten Cursor und gibt ein Handle für den duplizierten Cursor zurück.</span><span class="sxs-lookup"><span data-stu-id="545d8-104">Duplicates an open cursor and returns a handle to the duplicated cursor.</span></span> <span data-ttu-id="545d8-105">Wenn der duplizierte Cursor ein Schreib geschützter Cursor war, ist der duplizierte Cursor ebenfalls ein Schreib geschützter Cursor.</span><span class="sxs-lookup"><span data-stu-id="545d8-105">If the cursor that was duplicated was a read-only cursor then the duplicated cursor is also a read-only cursor.</span></span> <span data-ttu-id="545d8-106">Jeder Status im Zusammenhang mit dem Erstellen eines Suchschlüssels oder dem Aktualisieren eines Datensatzes wird nicht in den doppelten Cursor kopiert.</span><span class="sxs-lookup"><span data-stu-id="545d8-106">Any state related to constructing a search key or updating a record is not copied into the duplicated cursor.</span></span> <span data-ttu-id="545d8-107">Außerdem wird der Speicherort des ursprünglichen Cursors nicht in den doppelten Cursor dupliziert.</span><span class="sxs-lookup"><span data-stu-id="545d8-107">In addition, the location of the original cursor is not duplicated into the duplicated cursor.</span></span> <span data-ttu-id="545d8-108">Der doppelte Cursor wird immer auf dem gruppierten Index geöffnet, und sein Speicherort ist immer in der ersten Zeile der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="545d8-108">The duplicated cursor is always opened on the clustered index and its location is always on the first row of the table.</span></span>

<span data-ttu-id="545d8-109">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="545d8-109">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="545d8-110">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="545d8-110">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="545d8-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="545d8-111">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetDupCursor ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    <OutAttribute> ByRef newTableid As JET_TABLEID, _
    grbit As DupCursorGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim newTableid As JET_TABLEID
Dim grbit As DupCursorGrbitApi.JetDupCursor(sesid, tableid, _
    newTableid, grbit)
```

``` csharp
public static void JetDupCursor(
    JET_SESID sesid,
    JET_TABLEID tableid,
    out JET_TABLEID newTableid,
    DupCursorGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="545d8-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="545d8-112">Parameters</span></span>

  - <span data-ttu-id="545d8-113">-sid</span><span class="sxs-lookup"><span data-stu-id="545d8-113">sesid</span></span>  
    <span data-ttu-id="545d8-114">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="545d8-114">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="545d8-115">Die zu verwendende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="545d8-115">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="545d8-116">TableID</span><span class="sxs-lookup"><span data-stu-id="545d8-116">tableid</span></span>  
    <span data-ttu-id="545d8-117">Typ: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="545d8-117">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="545d8-118">Der zu duplizierende Cursor.</span><span class="sxs-lookup"><span data-stu-id="545d8-118">The cursor to duplicate.</span></span>

<!-- end list -->

  - <span data-ttu-id="545d8-119">newtableid</span><span class="sxs-lookup"><span data-stu-id="545d8-119">newTableid</span></span>  
    <span data-ttu-id="545d8-120">Typ: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="545d8-120">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="545d8-121">Der doppelte Cursor.</span><span class="sxs-lookup"><span data-stu-id="545d8-121">The duplicated cursor.</span></span>

<!-- end list -->

  - <span data-ttu-id="545d8-122">grbit</span><span class="sxs-lookup"><span data-stu-id="545d8-122">grbit</span></span>  
    <span data-ttu-id="545d8-123">Typ: [Microsoft. ISAM. ESENT. Interop. dupcurrsorgrbit](./dupcursorgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="545d8-123">Type: [Microsoft.Isam.Esent.Interop.DupCursorGrbit](./dupcursorgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="545d8-124">Für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="545d8-124">Reserved for future use.</span></span>

## <a name="see-also"></a><span data-ttu-id="545d8-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="545d8-125">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="545d8-126">Referenz</span><span class="sxs-lookup"><span data-stu-id="545d8-126">Reference</span></span>

[<span data-ttu-id="545d8-127">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="545d8-127">Api class</span></span>](./api-class.md)

[<span data-ttu-id="545d8-128">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="545d8-128">Api members</span></span>](./api-members.md)

[<span data-ttu-id="545d8-129">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="545d8-129">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
