---
description: 'Weitere Informationen finden Sie unter: API. jetupdate-Methode (JET_SESID JET_TABLEID)'
title: API. jetupdate-Methode (JET_SESID, JET_TABLEID)
TOCTitle: JetUpdate method (JET_SESID, JET_TABLEID)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetUpdate(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetupdate(v=EXCHG.10)
ms:contentKeyID: 55100831
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
ms.openlocfilehash: f1875353e8a5b4a23302a5f008af2cfa42a89b11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349588"
---
# <a name="apijetupdate-method-jet_sesid-jet_tableid"></a><span data-ttu-id="6373e-103">API. jetupdate-Methode (JET_SESID, JET_TABLEID)</span><span class="sxs-lookup"><span data-stu-id="6373e-103">Api.JetUpdate method (JET_SESID, JET_TABLEID)</span></span>

<span data-ttu-id="6373e-104">Die jetupdate-Funktion führt einen Aktualisierungs Vorgang aus, einschließlich des Einfügens einer neuen Zeile in eine Tabelle oder der Aktualisierung einer vorhandenen Zeile.</span><span class="sxs-lookup"><span data-stu-id="6373e-104">The JetUpdate function performs an update operation including inserting a new row into a table or updating an existing row.</span></span> <span data-ttu-id="6373e-105">Das Löschen einer Tabellenzeile erfolgt durch Aufrufen von [jetdelete (JET_SESID JET_TABLEID)](./api.jetdelete-method.md).</span><span class="sxs-lookup"><span data-stu-id="6373e-105">Deleting a table row is performed by calling [JetDelete(JET_SESID, JET_TABLEID)](./api.jetdelete-method.md).</span></span>

<span data-ttu-id="6373e-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="6373e-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="6373e-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="6373e-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="6373e-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="6373e-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetUpdate ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEIDApi.JetUpdate(sesid, tableid)
```

``` csharp
public static void JetUpdate(
    JET_SESID sesid,
    JET_TABLEID tableid
)
```

#### <a name="parameters"></a><span data-ttu-id="6373e-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="6373e-109">Parameters</span></span>

  - <span data-ttu-id="6373e-110">-sid</span><span class="sxs-lookup"><span data-stu-id="6373e-110">sesid</span></span>  
    <span data-ttu-id="6373e-111">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="6373e-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="6373e-112">Die Sitzung, von der das Update gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="6373e-112">The session which started the update.</span></span>

<!-- end list -->

  - <span data-ttu-id="6373e-113">TableID</span><span class="sxs-lookup"><span data-stu-id="6373e-113">tableid</span></span>  
    <span data-ttu-id="6373e-114">Typ: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="6373e-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="6373e-115">Der Cursor, der aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="6373e-115">The cursor to update.</span></span> <span data-ttu-id="6373e-116">Ein Update sollte vorbereitet werden.</span><span class="sxs-lookup"><span data-stu-id="6373e-116">An update should be prepared.</span></span>

## <a name="remarks"></a><span data-ttu-id="6373e-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6373e-117">Remarks</span></span>

<span data-ttu-id="6373e-118">Jetupdate ist der letzte Schritt beim Ausführen eines Einfügevorgangs oder eines Updates.</span><span class="sxs-lookup"><span data-stu-id="6373e-118">JetUpdate is the final step in performing an insert or an update.</span></span> <span data-ttu-id="6373e-119">Das Update wird durch Aufrufen von [jetprepareupdate (JET_SESID, JET_TABLEID, JET_prep)](./api.jetprepareupdate-method.md) und anschließendes Aufrufen von [jetsetcolumn (JET_SESID, JET_TABLEID, JET_COLUMNID, \[ \] , Int32, setcolumngrbit, JET_SETINFO)](./api.jetsetcolumn-method-jet-sesid-jet-tableid-jet-columnid-byte-int32-setcolumngrbit-jet-setinfo-.md) zum Festlegen des Daten Satz Zustands gestartet.</span><span class="sxs-lookup"><span data-stu-id="6373e-119">The update is begun by calling [JetPrepareUpdate(JET_SESID, JET_TABLEID, JET_prep)](./api.jetprepareupdate-method.md) and then by calling [JetSetColumn(JET_SESID, JET_TABLEID, JET_COLUMNID, \[\], Int32, SetColumnGrbit, JET_SETINFO)](./api.jetsetcolumn-method-jet-sesid-jet-tableid-jet-columnid-byte-int32-setcolumngrbit-jet-setinfo-.md) one or more times to set the record state.</span></span> <span data-ttu-id="6373e-120">Zum Schluss wird [jetupdate (JET_SESID, JET_TABLEID, \[ \] , Int32, Int32)](./api.jetupdate-method-jet-sesid-jet-tableid-byte-int32-int32-.md) aufgerufen, um den Aktualisierungs Vorgang abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="6373e-120">Finally, [JetUpdate(JET_SESID, JET_TABLEID, \[\], Int32, Int32)](./api.jetupdate-method-jet-sesid-jet-tableid-byte-int32-int32-.md) is called to complete the update operation.</span></span> <span data-ttu-id="6373e-121">Indizes werden nur von jetupdate oder und nicht von jetsetcolumn aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="6373e-121">Indexes are updated only by JetUpdate or and not during JetSetColumn.</span></span>

## <a name="see-also"></a><span data-ttu-id="6373e-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6373e-122">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="6373e-123">Referenz</span><span class="sxs-lookup"><span data-stu-id="6373e-123">Reference</span></span>

[<span data-ttu-id="6373e-124">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="6373e-124">Api class</span></span>](./api-class.md)

[<span data-ttu-id="6373e-125">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="6373e-125">Api members</span></span>](./api-members.md)

[<span data-ttu-id="6373e-126">Jetupdate-Überladung</span><span class="sxs-lookup"><span data-stu-id="6373e-126">JetUpdate overload</span></span>](./api.jetupdate-method.md)

[<span data-ttu-id="6373e-127">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="6373e-127">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
