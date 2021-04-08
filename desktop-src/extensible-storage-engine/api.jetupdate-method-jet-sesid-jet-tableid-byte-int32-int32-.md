---
description: 'Weitere Informationen finden Sie unter: API. jetupdate-Methode (JET_SESID, JET_TABLEID, Byte, Int32, Int32)'
title: API. jetupdate-Methode (JET_SESID, JET_TABLEID, Byte, Int32, Int32)
TOCTitle: JetUpdate method (JET_SESID, JET_TABLEID, Byte , Int32, Int32)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetUpdate(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Byte[],System.Int32,System.Int32@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetupdate(v=EXCHG.10)
ms:contentKeyID: 55100814
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetUpdate
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2c85e424fc9b672944801da3d03cbaff0ca48017
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863219"
---
# <a name="apijetupdate-method-jet_sesid-jet_tableid-byte--int32-int32"></a><span data-ttu-id="4e707-103">API. jetupdate-Methode (JET_SESID, JET_TABLEID, Byte, Int32, Int32)</span><span class="sxs-lookup"><span data-stu-id="4e707-103">Api.JetUpdate method (JET_SESID, JET_TABLEID, Byte , Int32, Int32)</span></span>

<span data-ttu-id="4e707-104">Die jetupdate-Funktion führt einen Aktualisierungs Vorgang aus, einschließlich des Einfügens einer neuen Zeile in eine Tabelle oder der Aktualisierung einer vorhandenen Zeile.</span><span class="sxs-lookup"><span data-stu-id="4e707-104">The JetUpdate function performs an update operation including inserting a new row into a table or updating an existing row.</span></span> <span data-ttu-id="4e707-105">Das Löschen einer Tabellenzeile erfolgt durch Aufrufen von [jetdelete (JET_SESID JET_TABLEID)](./api.jetdelete-method.md).</span><span class="sxs-lookup"><span data-stu-id="4e707-105">Deleting a table row is performed by calling [JetDelete(JET_SESID, JET_TABLEID)](./api.jetdelete-method.md).</span></span>

<span data-ttu-id="4e707-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="4e707-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="4e707-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="4e707-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="4e707-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="4e707-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetUpdate ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    bookmark As Byte(), _
    bookmarkSize As Integer, _
    <OutAttribute> ByRef actualBookmarkSize As Integer _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim bookmark As Byte()
Dim bookmarkSize As Integer
Dim actualBookmarkSize As IntegerApi.JetUpdate(sesid, tableid, bookmark, _
    bookmarkSize, actualBookmarkSize)
```

``` csharp
public static void JetUpdate(
    JET_SESID sesid,
    JET_TABLEID tableid,
    byte[] bookmark,
    int bookmarkSize,
    out int actualBookmarkSize
)
```

#### <a name="parameters"></a><span data-ttu-id="4e707-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="4e707-109">Parameters</span></span>

  - <span data-ttu-id="4e707-110">-sid</span><span class="sxs-lookup"><span data-stu-id="4e707-110">sesid</span></span>  
    <span data-ttu-id="4e707-111">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="4e707-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="4e707-112">Die Sitzung, von der das Update gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="4e707-112">The session which started the update.</span></span>

<!-- end list -->

  - <span data-ttu-id="4e707-113">TableID</span><span class="sxs-lookup"><span data-stu-id="4e707-113">tableid</span></span>  
    <span data-ttu-id="4e707-114">Typ: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="4e707-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="4e707-115">Der Cursor, der aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="4e707-115">The cursor to update.</span></span> <span data-ttu-id="4e707-116">Ein Update sollte vorbereitet werden.</span><span class="sxs-lookup"><span data-stu-id="4e707-116">An update should be prepared.</span></span>

<!-- end list -->

  - <span data-ttu-id="4e707-117">Lesezeichen (bookmark)</span><span class="sxs-lookup"><span data-stu-id="4e707-117">bookmark</span></span>  
    <span data-ttu-id="4e707-118">Sorte \[\]</span><span class="sxs-lookup"><span data-stu-id="4e707-118">Type: \[\]</span></span>  
    
    <span data-ttu-id="4e707-119">Gibt das Lesezeichen des aktualisierten Datensatzes zurück.</span><span class="sxs-lookup"><span data-stu-id="4e707-119">Returns the bookmark of the updated record.</span></span> <span data-ttu-id="4e707-120">Diese kann NULL sein.</span><span class="sxs-lookup"><span data-stu-id="4e707-120">This can be null.</span></span>

<!-- end list -->

  - <span data-ttu-id="4e707-121">bookmarksize</span><span class="sxs-lookup"><span data-stu-id="4e707-121">bookmarkSize</span></span>  
    <span data-ttu-id="4e707-122">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="4e707-122">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="4e707-123">Die Größe des Lesezeichen Puffers.</span><span class="sxs-lookup"><span data-stu-id="4e707-123">The size of the bookmark buffer.</span></span>

<!-- end list -->

  - <span data-ttu-id="4e707-124">actualbookmarksize</span><span class="sxs-lookup"><span data-stu-id="4e707-124">actualBookmarkSize</span></span>  
    <span data-ttu-id="4e707-125">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="4e707-125">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="4e707-126">Gibt die tatsächliche Größe des Lesezeichens zurück.</span><span class="sxs-lookup"><span data-stu-id="4e707-126">Returns the actual size of the bookmark.</span></span>

## <a name="remarks"></a><span data-ttu-id="4e707-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4e707-127">Remarks</span></span>

<span data-ttu-id="4e707-128">Jetupdate ist der letzte Schritt beim Ausführen eines Einfügevorgangs oder eines Updates.</span><span class="sxs-lookup"><span data-stu-id="4e707-128">JetUpdate is the final step in performing an insert or an update.</span></span> <span data-ttu-id="4e707-129">Das Update wird durch Aufrufen von [jetprepareupdate (JET_SESID, JET_TABLEID, JET_prep)](./api.jetprepareupdate-method.md) und anschließendes Aufrufen von [jetsetcolumn (JET_SESID, JET_TABLEID, JET_COLUMNID, \[ \] , Int32, setcolumngrbit, JET_SETINFO)](./api.jetsetcolumn-method-jet-sesid-jet-tableid-jet-columnid-byte-int32-setcolumngrbit-jet-setinfo-.md) zum Festlegen des Daten Satz Zustands gestartet.</span><span class="sxs-lookup"><span data-stu-id="4e707-129">The update is begun by calling [JetPrepareUpdate(JET_SESID, JET_TABLEID, JET_prep)](./api.jetprepareupdate-method.md) and then by calling [JetSetColumn(JET_SESID, JET_TABLEID, JET_COLUMNID, \[\], Int32, SetColumnGrbit, JET_SETINFO)](./api.jetsetcolumn-method-jet-sesid-jet-tableid-jet-columnid-byte-int32-setcolumngrbit-jet-setinfo-.md) one or more times to set the record state.</span></span> <span data-ttu-id="4e707-130">Zum Schluss wird jetupdate (JET_SESID, JET_TABLEID, \[ \] , Int32, Int32) aufgerufen, um den Aktualisierungs Vorgang abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="4e707-130">Finally, JetUpdate(JET_SESID, JET_TABLEID, \[\], Int32, Int32) is called to complete the update operation.</span></span> <span data-ttu-id="4e707-131">Indizes werden nur von jetupdate oder und nicht von jetsetcolumn aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="4e707-131">Indexes are updated only by JetUpdate or and not during JetSetColumn.</span></span>

## <a name="see-also"></a><span data-ttu-id="4e707-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4e707-132">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="4e707-133">Referenz</span><span class="sxs-lookup"><span data-stu-id="4e707-133">Reference</span></span>

[<span data-ttu-id="4e707-134">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="4e707-134">Api class</span></span>](./api-class.md)

[<span data-ttu-id="4e707-135">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="4e707-135">Api members</span></span>](./api-members.md)

[<span data-ttu-id="4e707-136">Jetupdate-Überladung</span><span class="sxs-lookup"><span data-stu-id="4e707-136">JetUpdate overload</span></span>](./api.jetupdate-method.md)

[<span data-ttu-id="4e707-137">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="4e707-137">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
