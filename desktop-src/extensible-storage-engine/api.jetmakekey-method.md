---
description: 'Weitere Informationen finden Sie unter: API. jetmakekey-Methode'
title: API. jetmakekey-Methode
TOCTitle: 'JetMakeKey method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetMakeKey(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Byte[],System.Int32,Microsoft.Isam.Esent.Interop.MakeKeyGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetmakekey(v=EXCHG.10)
ms:contentKeyID: 55100764
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetMakeKey
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetMakeKey
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 13db6e7106f5312e03ffa5acfbd86c72d38c6edb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960609"
---
# <a name="apijetmakekey-method"></a><span data-ttu-id="8158f-103">API. jetmakekey-Methode</span><span class="sxs-lookup"><span data-stu-id="8158f-103">Api.JetMakeKey method</span></span>

<span data-ttu-id="8158f-104">Erstellt Suchschlüssel, die dann von [JetSeek (JET_SESID, JET_TABLEID, seekgrbit)](./api.jetseek-method.md) und [jetsetindexrange (JET_SESID, JET_TABLEID, setindexrangegrbit)](./api.jetsetindexrange-method.md)verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="8158f-104">Constructs search keys that may then be used by [JetSeek(JET_SESID, JET_TABLEID, SeekGrbit)](./api.jetseek-method.md) and [JetSetIndexRange(JET_SESID, JET_TABLEID, SetIndexRangeGrbit)](./api.jetsetindexrange-method.md).</span></span>

<span data-ttu-id="8158f-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="8158f-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="8158f-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="8158f-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="8158f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="8158f-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetMakeKey ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    data As Byte(), _
    dataSize As Integer, _
    grbit As MakeKeyGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim data As Byte()
Dim dataSize As Integer
Dim grbit As MakeKeyGrbitApi.JetMakeKey(sesid, tableid, data, _
    dataSize, grbit)
```

``` csharp
public static void JetMakeKey(
    JET_SESID sesid,
    JET_TABLEID tableid,
    byte[] data,
    int dataSize,
    MakeKeyGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="8158f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="8158f-108">Parameters</span></span>

  - <span data-ttu-id="8158f-109">-sid</span><span class="sxs-lookup"><span data-stu-id="8158f-109">sesid</span></span>  
    <span data-ttu-id="8158f-110">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="8158f-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="8158f-111">Die zu verwendende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="8158f-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="8158f-112">TableID</span><span class="sxs-lookup"><span data-stu-id="8158f-112">tableid</span></span>  
    <span data-ttu-id="8158f-113">Typ: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="8158f-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="8158f-114">Der Cursor, auf dem der Schlüssel erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="8158f-114">The cursor to create the key on.</span></span>

<!-- end list -->

  - <span data-ttu-id="8158f-115">Daten</span><span class="sxs-lookup"><span data-stu-id="8158f-115">data</span></span>  
    <span data-ttu-id="8158f-116">Sorte \[\]</span><span class="sxs-lookup"><span data-stu-id="8158f-116">Type: \[\]</span></span>  
    
    <span data-ttu-id="8158f-117">Spaltendaten für die aktuelle Schlüssel Spalte des aktuellen Index.</span><span class="sxs-lookup"><span data-stu-id="8158f-117">Column data for the current key column of the current index.</span></span>

<!-- end list -->

  - <span data-ttu-id="8158f-118">dataSize</span><span class="sxs-lookup"><span data-stu-id="8158f-118">dataSize</span></span>  
    <span data-ttu-id="8158f-119">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="8158f-119">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="8158f-120">Größe der Daten.</span><span class="sxs-lookup"><span data-stu-id="8158f-120">Size of the data.</span></span>

<!-- end list -->

  - <span data-ttu-id="8158f-121">grbit</span><span class="sxs-lookup"><span data-stu-id="8158f-121">grbit</span></span>  
    <span data-ttu-id="8158f-122">Typ: [Microsoft. ISAM. ESENT. Interop. makekeygrbit](./makekeygrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="8158f-122">Type: [Microsoft.Isam.Esent.Interop.MakeKeyGrbit](./makekeygrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="8158f-123">Schlüsseloptionen.</span><span class="sxs-lookup"><span data-stu-id="8158f-123">Key options.</span></span>

## <a name="remarks"></a><span data-ttu-id="8158f-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8158f-124">Remarks</span></span>

<span data-ttu-id="8158f-125">Die Makekey-Funktionen bieten DataType-spezifische Make Key-Funktionen.</span><span class="sxs-lookup"><span data-stu-id="8158f-125">The MakeKey functions provide datatype-specific make key functionality.</span></span>

## <a name="see-also"></a><span data-ttu-id="8158f-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8158f-126">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="8158f-127">Referenz</span><span class="sxs-lookup"><span data-stu-id="8158f-127">Reference</span></span>

[<span data-ttu-id="8158f-128">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="8158f-128">Api class</span></span>](./api-class.md)

[<span data-ttu-id="8158f-129">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="8158f-129">Api members</span></span>](./api-members.md)

[<span data-ttu-id="8158f-130">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="8158f-130">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
