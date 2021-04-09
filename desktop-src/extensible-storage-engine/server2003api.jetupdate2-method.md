---
description: 'Weitere Informationen über: Server2003Api. JetUpdate2-Methode'
title: Server2003Api. JetUpdate2-Methode (Microsoft. ISAM. ESENT. Interop. Server2003)
TOCTitle: 'JetUpdate2 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Server2003.Server2003Api.JetUpdate2(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Byte[],System.Int32,System.Int32@,Microsoft.Isam.Esent.Interop.Server2003.UpdateGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.server2003.server2003api.jetupdate2(v=EXCHG.10)
ms:contentKeyID: 55104110
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Server2003.Server2003Api.JetUpdate2
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Server2003.Server2003Api.JetUpdate2
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fff3687d42160df331bfe52660be232fe3b41d5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128156"
---
# <a name="server2003apijetupdate2-method"></a><span data-ttu-id="73e9f-103">Server2003Api. JetUpdate2-Methode</span><span class="sxs-lookup"><span data-stu-id="73e9f-103">Server2003Api.JetUpdate2 method</span></span>

<span data-ttu-id="73e9f-104">Die jetupdate-Funktion führt einen Aktualisierungs Vorgang aus, einschließlich des Einfügens einer neuen Zeile in eine Tabelle oder der Aktualisierung einer vorhandenen Zeile.</span><span class="sxs-lookup"><span data-stu-id="73e9f-104">The JetUpdate function performs an update operation including inserting a new row into a table or updating an existing row.</span></span> <span data-ttu-id="73e9f-105">Das Löschen einer Tabellenzeile erfolgt durch Aufrufen von [jetdelete (JET_SESID JET_TABLEID)](./api.jetdelete-method.md).</span><span class="sxs-lookup"><span data-stu-id="73e9f-105">Deleting a table row is performed by calling [JetDelete(JET_SESID, JET_TABLEID)](./api.jetdelete-method.md).</span></span>

<span data-ttu-id="73e9f-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop. Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="73e9f-106">**Namespace:**  [Microsoft.Isam.Esent.Interop.Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)</span></span>  
<span data-ttu-id="73e9f-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="73e9f-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="73e9f-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="73e9f-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetUpdate2 ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    bookmark As Byte(), _
    bookmarkSize As Integer, _
    <OutAttribute> ByRef actualBookmarkSize As Integer, _
    grbit As UpdateGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim bookmark As Byte()
Dim bookmarkSize As Integer
Dim actualBookmarkSize As Integer
Dim grbit As UpdateGrbitServer2003Api.JetUpdate2(sesid, tableid, bookmark, _
    bookmarkSize, actualBookmarkSize, _
    grbit)
```

``` csharp
public static void JetUpdate2(
    JET_SESID sesid,
    JET_TABLEID tableid,
    byte[] bookmark,
    int bookmarkSize,
    out int actualBookmarkSize,
    UpdateGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="73e9f-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="73e9f-109">Parameters</span></span>

  - <span data-ttu-id="73e9f-110">-sid</span><span class="sxs-lookup"><span data-stu-id="73e9f-110">sesid</span></span>  
    <span data-ttu-id="73e9f-111">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="73e9f-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="73e9f-112">Die Sitzung, von der das Update gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="73e9f-112">The session which started the update.</span></span>

<!-- end list -->

  - <span data-ttu-id="73e9f-113">TableID</span><span class="sxs-lookup"><span data-stu-id="73e9f-113">tableid</span></span>  
    <span data-ttu-id="73e9f-114">Typ: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="73e9f-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="73e9f-115">Der Cursor, der aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="73e9f-115">The cursor to update.</span></span> <span data-ttu-id="73e9f-116">Ein Update sollte vorbereitet werden.</span><span class="sxs-lookup"><span data-stu-id="73e9f-116">An update should be prepared.</span></span>

<!-- end list -->

  - <span data-ttu-id="73e9f-117">Lesezeichen (bookmark)</span><span class="sxs-lookup"><span data-stu-id="73e9f-117">bookmark</span></span>  
    <span data-ttu-id="73e9f-118">Sorte \[\]</span><span class="sxs-lookup"><span data-stu-id="73e9f-118">Type: \[\]</span></span>  
    
    <span data-ttu-id="73e9f-119">Gibt das Lesezeichen des aktualisierten Datensatzes zurück.</span><span class="sxs-lookup"><span data-stu-id="73e9f-119">Returns the bookmark of the updated record.</span></span> <span data-ttu-id="73e9f-120">Diese kann NULL sein.</span><span class="sxs-lookup"><span data-stu-id="73e9f-120">This can be null.</span></span>

<!-- end list -->

  - <span data-ttu-id="73e9f-121">bookmarksize</span><span class="sxs-lookup"><span data-stu-id="73e9f-121">bookmarkSize</span></span>  
    <span data-ttu-id="73e9f-122">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="73e9f-122">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="73e9f-123">Die Größe des Lesezeichen Puffers.</span><span class="sxs-lookup"><span data-stu-id="73e9f-123">The size of the bookmark buffer.</span></span>

<!-- end list -->

  - <span data-ttu-id="73e9f-124">actualbookmarksize</span><span class="sxs-lookup"><span data-stu-id="73e9f-124">actualBookmarkSize</span></span>  
    <span data-ttu-id="73e9f-125">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="73e9f-125">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="73e9f-126">Gibt die tatsächliche Größe des Lesezeichens zurück.</span><span class="sxs-lookup"><span data-stu-id="73e9f-126">Returns the actual size of the bookmark.</span></span>

<!-- end list -->

  - <span data-ttu-id="73e9f-127">grbit</span><span class="sxs-lookup"><span data-stu-id="73e9f-127">grbit</span></span>  
    <span data-ttu-id="73e9f-128">Typ: [Microsoft. ISAM. ESENT. Interop. Server2003. updategrbit](./updategrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="73e9f-128">Type: [Microsoft.Isam.Esent.Interop.Server2003.UpdateGrbit](./updategrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="73e9f-129">Aktualisierungs Optionen.</span><span class="sxs-lookup"><span data-stu-id="73e9f-129">Update options.</span></span>

## <a name="remarks"></a><span data-ttu-id="73e9f-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="73e9f-130">Remarks</span></span>

<span data-ttu-id="73e9f-131">Jetupdate ist der letzte Schritt beim Ausführen eines Einfügevorgangs oder eines Updates.</span><span class="sxs-lookup"><span data-stu-id="73e9f-131">JetUpdate is the final step in performing an insert or an update.</span></span> <span data-ttu-id="73e9f-132">Das Update wird durch Aufrufen von [jetprepareupdate (JET_SESID, JET_TABLEID, JET_prep)](./api.jetprepareupdate-method.md) und anschließendes Aufrufen von [jetsetcolumn (JET_SESID, JET_TABLEID, JET_COLUMNID, \[ \] , Int32, setcolumngrbit, JET_SETINFO)](./api.jetsetcolumn-method-jet-sesid-jet-tableid-jet-columnid-byte-int32-setcolumngrbit-jet-setinfo-.md) zum Festlegen des Daten Satz Zustands gestartet.</span><span class="sxs-lookup"><span data-stu-id="73e9f-132">The update is begun by calling [JetPrepareUpdate(JET_SESID, JET_TABLEID, JET_prep)](./api.jetprepareupdate-method.md) and then by calling [JetSetColumn(JET_SESID, JET_TABLEID, JET_COLUMNID, \[\], Int32, SetColumnGrbit, JET_SETINFO)](./api.jetsetcolumn-method-jet-sesid-jet-tableid-jet-columnid-byte-int32-setcolumngrbit-jet-setinfo-.md) one or more times to set the record state.</span></span> <span data-ttu-id="73e9f-133">Schließlich wird JetUpdate2 (JET_SESID, JET_TABLEID, \[ \] , Int32, Int32, updategrbit) aufgerufen, um den Aktualisierungs Vorgang abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="73e9f-133">Finally, JetUpdate2(JET_SESID, JET_TABLEID, \[\], Int32, Int32, UpdateGrbit) is called to complete the update operation.</span></span> <span data-ttu-id="73e9f-134">Indizes werden nur von jetupdate oder und nicht von jetsetcolumn aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="73e9f-134">Indexes are updated only by JetUpdate or and not during JetSetColumn.</span></span>

## <a name="see-also"></a><span data-ttu-id="73e9f-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="73e9f-135">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="73e9f-136">Referenz</span><span class="sxs-lookup"><span data-stu-id="73e9f-136">Reference</span></span>

[<span data-ttu-id="73e9f-137">Server2003Api-Klasse</span><span class="sxs-lookup"><span data-stu-id="73e9f-137">Server2003Api class</span></span>](./server2003api-class.md)

[<span data-ttu-id="73e9f-138">Server2003Api-Member</span><span class="sxs-lookup"><span data-stu-id="73e9f-138">Server2003Api members</span></span>](./server2003api-members.md)

[<span data-ttu-id="73e9f-139">Microsoft. ISAM. ESENT. Interop. Server2003-Namespace</span><span class="sxs-lookup"><span data-stu-id="73e9f-139">Microsoft.Isam.Esent.Interop.Server2003 namespace</span></span>](./microsoft.isam.esent.interop.server2003-namespace.md)
