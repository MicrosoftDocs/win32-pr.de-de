---
description: 'Weitere Informationen finden Sie hier: Windows8Api. jetsetcurrsorfilter-Methode'
title: Windows8Api. jetsetcurrsorfilter-Methode (Microsoft. ISAM. ESENT. Interop. Windows8)
TOCTitle: 'JetSetCursorFilter method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetSetCursorFilter(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.Windows8.JET_INDEX_COLUMN[],Microsoft.Isam.Esent.Interop.Windows8.CursorFilterGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.windows8api.jetsetcursorfilter(v=EXCHG.10)
ms:contentKeyID: 55104447
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetSetCursorFilter
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetSetCursorFilter
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0137c25ee6ab548537d797af0a00a7ffcd1f6d5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106359921"
---
# <a name="windows8apijetsetcursorfilter-method"></a><span data-ttu-id="da1fb-103">Windows8Api. jetsetcurrsorfilter-Methode</span><span class="sxs-lookup"><span data-stu-id="da1fb-103">Windows8Api.JetSetCursorFilter method</span></span>

<span data-ttu-id="da1fb-104">Legen Sie ein Array einfacher Filter für [jetmove (JET_SESID, JET_TABLEID, Int32, movegrbit)](./api.jetmove-method-jet-sesid-jet-tableid-int32-movegrbit-.md)fest.</span><span class="sxs-lookup"><span data-stu-id="da1fb-104">Set an array of simple filters for [JetMove(JET_SESID, JET_TABLEID, Int32, MoveGrbit)](./api.jetmove-method-jet-sesid-jet-tableid-int32-movegrbit-.md).</span></span>

<span data-ttu-id="da1fb-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="da1fb-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="da1fb-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="da1fb-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="da1fb-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="da1fb-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetSetCursorFilter ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    filters As JET_INDEX_COLUMN(), _
    grbit As CursorFilterGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim filters As JET_INDEX_COLUMN()
Dim grbit As CursorFilterGrbitWindows8Api.JetSetCursorFilter(sesid, tableid, _
    filters, grbit)
```

``` csharp
public static void JetSetCursorFilter(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_INDEX_COLUMN[] filters,
    CursorFilterGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="da1fb-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="da1fb-108">Parameters</span></span>

  - <span data-ttu-id="da1fb-109">-sid</span><span class="sxs-lookup"><span data-stu-id="da1fb-109">sesid</span></span>  
    <span data-ttu-id="da1fb-110">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="da1fb-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="da1fb-111">Die für den-Befehl zu verwendende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="da1fb-111">The session to use for the call.</span></span>

<!-- end list -->

  - <span data-ttu-id="da1fb-112">TableID</span><span class="sxs-lookup"><span data-stu-id="da1fb-112">tableid</span></span>  
    <span data-ttu-id="da1fb-113">Typ: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="da1fb-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="da1fb-114">Der Cursor, der positioniert werden soll.</span><span class="sxs-lookup"><span data-stu-id="da1fb-114">The cursor to position.</span></span>

<!-- end list -->

  - <span data-ttu-id="da1fb-115">Filter</span><span class="sxs-lookup"><span data-stu-id="da1fb-115">filters</span></span>  
    <span data-ttu-id="da1fb-116">Sorte \[\]</span><span class="sxs-lookup"><span data-stu-id="da1fb-116">Type: \[\]</span></span>  
    
    <span data-ttu-id="da1fb-117">Einfache Daten Satz Filter.</span><span class="sxs-lookup"><span data-stu-id="da1fb-117">Simple record filters.</span></span>

<!-- end list -->

  - <span data-ttu-id="da1fb-118">grbit</span><span class="sxs-lookup"><span data-stu-id="da1fb-118">grbit</span></span>  
    <span data-ttu-id="da1fb-119">Typ: [Microsoft. ISAM. ESENT. Interop. Windows8. currsorfiltergrbit](./cursorfiltergrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="da1fb-119">Type: [Microsoft.Isam.Esent.Interop.Windows8.CursorFilterGrbit](./cursorfiltergrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="da1fb-120">Verschieben von Optionen.</span><span class="sxs-lookup"><span data-stu-id="da1fb-120">Move options.</span></span>

## <a name="see-also"></a><span data-ttu-id="da1fb-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="da1fb-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="da1fb-122">Referenz</span><span class="sxs-lookup"><span data-stu-id="da1fb-122">Reference</span></span>

[<span data-ttu-id="da1fb-123">Windows8Api-Klasse</span><span class="sxs-lookup"><span data-stu-id="da1fb-123">Windows8Api class</span></span>](./windows8api-class.md)

[<span data-ttu-id="da1fb-124">Windows8Api-Member</span><span class="sxs-lookup"><span data-stu-id="da1fb-124">Windows8Api members</span></span>](./windows8api-members.md)

[<span data-ttu-id="da1fb-125">Microsoft. ISAM. ESENT. Interop. Windows8-Namespace</span><span class="sxs-lookup"><span data-stu-id="da1fb-125">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
