---
description: 'Weitere Informationen finden Sie unter: API. Makekey-Methode (JET_SESID, JET_TABLEID, UInt32, makekeygrbit)'
title: API. Makekey-Methode (JET_SESID, JET_TABLEID, UInt32, makekeygrbit)
TOCTitle: MakeKey method (JET_SESID, JET_TABLEID, UInt32, MakeKeyGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.MakeKey(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.UInt32,Microsoft.Isam.Esent.Interop.MakeKeyGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.makekey(v=EXCHG.10)
ms:contentKeyID: 55100848
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.MakeKey
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 45edbf959058ccb1c50b82a13f0ca84cdd16a7dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349630"
---
# <a name="apimakekey-method-jet_sesid-jet_tableid-uint32-makekeygrbit"></a><span data-ttu-id="0ef42-103">API. Makekey-Methode (JET_SESID, JET_TABLEID, UInt32, makekeygrbit)</span><span class="sxs-lookup"><span data-stu-id="0ef42-103">Api.MakeKey method (JET_SESID, JET_TABLEID, UInt32, MakeKeyGrbit)</span></span>

<span data-ttu-id="0ef42-104">Erstellt einen Suchschlüssel, der von [JetSeek (JET_SESID, JET_TABLEID, seekgrbit)](./api.jetseek-method.md) und [jetsetindexrange (JET_SESID, JET_TABLEID, setindexrangegrbit)](./api.jetsetindexrange-method.md)verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="0ef42-104">Constructs a search key that may then be used by [JetSeek(JET_SESID, JET_TABLEID, SeekGrbit)](./api.jetseek-method.md) and [JetSetIndexRange(JET_SESID, JET_TABLEID, SetIndexRangeGrbit)](./api.jetsetindexrange-method.md).</span></span>

<span data-ttu-id="0ef42-105">Diese API ist nicht CLS-kompatibel.</span><span class="sxs-lookup"><span data-stu-id="0ef42-105">This API is not CLS-compliant.</span></span> 

<span data-ttu-id="0ef42-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="0ef42-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="0ef42-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="0ef42-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="0ef42-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="0ef42-108">Syntax</span></span>

``` vb
'Declaration
<CLSCompliantAttribute(False)> _
Public Shared Sub MakeKey ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    data As UInteger, _
    grbit As MakeKeyGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim data As UInteger
Dim grbit As MakeKeyGrbitApi.MakeKey(sesid, tableid, data, _
    grbit)
```

``` csharp
[CLSCompliantAttribute(false)]
public static void MakeKey(
    JET_SESID sesid,
    JET_TABLEID tableid,
    uint data,
    MakeKeyGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="0ef42-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="0ef42-109">Parameters</span></span>

  - <span data-ttu-id="0ef42-110">-sid</span><span class="sxs-lookup"><span data-stu-id="0ef42-110">sesid</span></span>  
    <span data-ttu-id="0ef42-111">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="0ef42-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="0ef42-112">Die zu verwendende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="0ef42-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="0ef42-113">TableID</span><span class="sxs-lookup"><span data-stu-id="0ef42-113">tableid</span></span>  
    <span data-ttu-id="0ef42-114">Typ: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="0ef42-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="0ef42-115">Der Cursor, auf dem der Schlüssel erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="0ef42-115">The cursor to create the key on.</span></span>

<!-- end list -->

  - <span data-ttu-id="0ef42-116">Daten</span><span class="sxs-lookup"><span data-stu-id="0ef42-116">data</span></span>  
    <span data-ttu-id="0ef42-117">Typ: [System. UInt32](/dotnet/api/system.uint32)</span><span class="sxs-lookup"><span data-stu-id="0ef42-117">Type: [System.UInt32](/dotnet/api/system.uint32)</span></span>  
    
    <span data-ttu-id="0ef42-118">Spaltendaten für die aktuelle Schlüssel Spalte des aktuellen Index.</span><span class="sxs-lookup"><span data-stu-id="0ef42-118">Column data for the current key column of the current index.</span></span>

<!-- end list -->

  - <span data-ttu-id="0ef42-119">grbit</span><span class="sxs-lookup"><span data-stu-id="0ef42-119">grbit</span></span>  
    <span data-ttu-id="0ef42-120">Typ: [Microsoft. ISAM. ESENT. Interop. makekeygrbit](./makekeygrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="0ef42-120">Type: [Microsoft.Isam.Esent.Interop.MakeKeyGrbit](./makekeygrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="0ef42-121">Schlüsseloptionen.</span><span class="sxs-lookup"><span data-stu-id="0ef42-121">Key options.</span></span>

## <a name="see-also"></a><span data-ttu-id="0ef42-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0ef42-122">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="0ef42-123">Referenz</span><span class="sxs-lookup"><span data-stu-id="0ef42-123">Reference</span></span>

[<span data-ttu-id="0ef42-124">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="0ef42-124">Api class</span></span>](./api-class.md)

[<span data-ttu-id="0ef42-125">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="0ef42-125">Api members</span></span>](./api-members.md)

[<span data-ttu-id="0ef42-126">Makekey-Überladung</span><span class="sxs-lookup"><span data-stu-id="0ef42-126">MakeKey overload</span></span>](./api.makekey-method.md)

[<span data-ttu-id="0ef42-127">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="0ef42-127">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
