---
description: Weitere Informationen zur API. jetgetcurrsorinfo-Methode
title: API. jetgetcurrsorinfo-Methode
TOCTitle: 'JetGetCursorInfo method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetCursorInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetcursorinfo(v=EXCHG.10)
ms:contentKeyID: 55100707
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGetCursorInfo
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetCursorInfo
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7144283a062b0097d6866e74d1c263bb130c5e19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041660"
---
# <a name="apijetgetcursorinfo-method"></a><span data-ttu-id="7674e-103">API. jetgetcurrsorinfo-Methode</span><span class="sxs-lookup"><span data-stu-id="7674e-103">Api.JetGetCursorInfo method</span></span>

<span data-ttu-id="7674e-104">Bestimmen, ob ein Update des aktuellen Datensatzes eines Cursors zu einem Schreib Konflikt führt, basierend auf dem aktuellen Update Status des Datensatzes.</span><span class="sxs-lookup"><span data-stu-id="7674e-104">Determine whether an update of the current record of a cursor will result in a write conflict, based on the current update status of the record.</span></span> <span data-ttu-id="7674e-105">Es ist möglich, dass ein Schreib Konflikt letztendlich zurückgegeben wird, auch wenn jetgetcurrsorinfo erfolgreich zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="7674e-105">It is possible that a write conflict will ultimately be returned even if JetGetCursorInfo returns successfully.</span></span> <span data-ttu-id="7674e-106">Da eine andere Sitzung den Datensatz aktualisieren kann, bevor die aktuelle Sitzung denselben Datensatz aktualisieren kann.</span><span class="sxs-lookup"><span data-stu-id="7674e-106">because another session may update the record before the current session is able to update the same record.</span></span>

<span data-ttu-id="7674e-107">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="7674e-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="7674e-108">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="7674e-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="7674e-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="7674e-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetCursorInfo ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEIDApi.JetGetCursorInfo(sesid, tableid)
```

``` csharp
public static void JetGetCursorInfo(
    JET_SESID sesid,
    JET_TABLEID tableid
)
```

#### <a name="parameters"></a><span data-ttu-id="7674e-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="7674e-110">Parameters</span></span>

  - <span data-ttu-id="7674e-111">-sid</span><span class="sxs-lookup"><span data-stu-id="7674e-111">sesid</span></span>  
    <span data-ttu-id="7674e-112">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="7674e-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="7674e-113">Die zu verwendende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="7674e-113">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="7674e-114">TableID</span><span class="sxs-lookup"><span data-stu-id="7674e-114">tableid</span></span>  
    <span data-ttu-id="7674e-115">Typ: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="7674e-115">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="7674e-116">Der zu Überprüfung Ende Cursor.</span><span class="sxs-lookup"><span data-stu-id="7674e-116">The cursor to check.</span></span>

## <a name="see-also"></a><span data-ttu-id="7674e-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7674e-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="7674e-118">Referenz</span><span class="sxs-lookup"><span data-stu-id="7674e-118">Reference</span></span>

[<span data-ttu-id="7674e-119">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="7674e-119">Api class</span></span>](./api-class.md)

[<span data-ttu-id="7674e-120">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="7674e-120">Api members</span></span>](./api-members.md)

[<span data-ttu-id="7674e-121">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="7674e-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
