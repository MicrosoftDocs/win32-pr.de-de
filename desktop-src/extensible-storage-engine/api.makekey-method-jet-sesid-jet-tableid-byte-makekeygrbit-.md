---
description: 'Weitere Informationen finden Sie unter: API. Makekey-Methode (JET_SESID, JET_TABLEID, Byte, makekeygrbit)'
title: API. Makekey-Methode (JET_SESID, JET_TABLEID, Byte, makekeygrbit)
TOCTitle: MakeKey method (JET_SESID, JET_TABLEID, Byte, MakeKeyGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.MakeKey(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Byte,Microsoft.Isam.Esent.Interop.MakeKeyGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.makekey(v=EXCHG.10)
ms:contentKeyID: 55100821
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
ms.openlocfilehash: 0d638c3f63cf99a65e363ca13d1347cced4f1962
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348388"
---
# <a name="apimakekey-method-jet_sesid-jet_tableid-byte-makekeygrbit"></a><span data-ttu-id="fa4aa-103">API. Makekey-Methode (JET_SESID, JET_TABLEID, Byte, makekeygrbit)</span><span class="sxs-lookup"><span data-stu-id="fa4aa-103">Api.MakeKey method (JET_SESID, JET_TABLEID, Byte, MakeKeyGrbit)</span></span>

<span data-ttu-id="fa4aa-104">Erstellt einen Suchschlüssel, der von [JetSeek (JET_SESID, JET_TABLEID, seekgrbit)](./api.jetseek-method.md) und [jetsetindexrange (JET_SESID, JET_TABLEID, setindexrangegrbit)](./api.jetsetindexrange-method.md)verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="fa4aa-104">Constructs a search key that may then be used by [JetSeek(JET_SESID, JET_TABLEID, SeekGrbit)](./api.jetseek-method.md) and [JetSetIndexRange(JET_SESID, JET_TABLEID, SetIndexRangeGrbit)](./api.jetsetindexrange-method.md).</span></span>

<span data-ttu-id="fa4aa-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="fa4aa-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="fa4aa-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="fa4aa-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="fa4aa-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="fa4aa-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub MakeKey ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    data As Byte, _
    grbit As MakeKeyGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim data As Byte
Dim grbit As MakeKeyGrbitApi.MakeKey(sesid, tableid, data, _
    grbit)
```

``` csharp
public static void MakeKey(
    JET_SESID sesid,
    JET_TABLEID tableid,
    byte data,
    MakeKeyGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="fa4aa-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="fa4aa-108">Parameters</span></span>

  - <span data-ttu-id="fa4aa-109">-sid</span><span class="sxs-lookup"><span data-stu-id="fa4aa-109">sesid</span></span>  
    <span data-ttu-id="fa4aa-110">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="fa4aa-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="fa4aa-111">Die zu verwendende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="fa4aa-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="fa4aa-112">TableID</span><span class="sxs-lookup"><span data-stu-id="fa4aa-112">tableid</span></span>  
    <span data-ttu-id="fa4aa-113">Typ: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="fa4aa-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="fa4aa-114">Der Cursor, auf dem der Schlüssel erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="fa4aa-114">The cursor to create the key on.</span></span>

<!-- end list -->

  - <span data-ttu-id="fa4aa-115">Daten</span><span class="sxs-lookup"><span data-stu-id="fa4aa-115">data</span></span>  
    <span data-ttu-id="fa4aa-116">Typ: [System. Byte](/dotnet/api/system.byte)</span><span class="sxs-lookup"><span data-stu-id="fa4aa-116">Type: [System.Byte](/dotnet/api/system.byte)</span></span>  
    
    <span data-ttu-id="fa4aa-117">Spaltendaten für die aktuelle Schlüssel Spalte des aktuellen Index.</span><span class="sxs-lookup"><span data-stu-id="fa4aa-117">Column data for the current key column of the current index.</span></span>

<!-- end list -->

  - <span data-ttu-id="fa4aa-118">grbit</span><span class="sxs-lookup"><span data-stu-id="fa4aa-118">grbit</span></span>  
    <span data-ttu-id="fa4aa-119">Typ: [Microsoft. ISAM. ESENT. Interop. makekeygrbit](./makekeygrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="fa4aa-119">Type: [Microsoft.Isam.Esent.Interop.MakeKeyGrbit](./makekeygrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="fa4aa-120">Schlüsseloptionen.</span><span class="sxs-lookup"><span data-stu-id="fa4aa-120">Key options.</span></span>

## <a name="see-also"></a><span data-ttu-id="fa4aa-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fa4aa-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="fa4aa-122">Referenz</span><span class="sxs-lookup"><span data-stu-id="fa4aa-122">Reference</span></span>

[<span data-ttu-id="fa4aa-123">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="fa4aa-123">Api class</span></span>](./api-class.md)

[<span data-ttu-id="fa4aa-124">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="fa4aa-124">Api members</span></span>](./api-members.md)

[<span data-ttu-id="fa4aa-125">Makekey-Überladung</span><span class="sxs-lookup"><span data-stu-id="fa4aa-125">MakeKey overload</span></span>](./api.makekey-method.md)

[<span data-ttu-id="fa4aa-126">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="fa4aa-126">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
