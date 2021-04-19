---
description: 'Weitere Informationen finden Sie unter: API. Makekey-Methode (JET_SESID, JET_TABLEID, Zeichenfolge, Codierung, makekeygrbit)'
title: API. Makekey-Methode (JET_SESID, JET_TABLEID, String, Encoding, makekeygrbit)
TOCTitle: MakeKey method (JET_SESID, JET_TABLEID, String, Encoding, MakeKeyGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.MakeKey(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.String,System.Text.Encoding,Microsoft.Isam.Esent.Interop.MakeKeyGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.makekey(v=EXCHG.10)
ms:contentKeyID: 55100830
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.MakeKey
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d5f4fa9dfd848ff6aef858533501891e08ef8972
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353151"
---
# <a name="apimakekey-method-jet_sesid-jet_tableid-string-encoding-makekeygrbit"></a><span data-ttu-id="be5e8-103">API. Makekey-Methode (JET_SESID, JET_TABLEID, String, Encoding, makekeygrbit)</span><span class="sxs-lookup"><span data-stu-id="be5e8-103">Api.MakeKey method (JET_SESID, JET_TABLEID, String, Encoding, MakeKeyGrbit)</span></span>

<span data-ttu-id="be5e8-104">Erstellt einen Suchschlüssel, der von [JetSeek (JET_SESID, JET_TABLEID, seekgrbit)](./api.jetseek-method.md) und [jetsetindexrange (JET_SESID, JET_TABLEID, setindexrangegrbit)](./api.jetsetindexrange-method.md)verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="be5e8-104">Constructs a search key that may then be used by [JetSeek(JET_SESID, JET_TABLEID, SeekGrbit)](./api.jetseek-method.md) and [JetSetIndexRange(JET_SESID, JET_TABLEID, SetIndexRangeGrbit)](./api.jetsetindexrange-method.md).</span></span>

<span data-ttu-id="be5e8-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="be5e8-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="be5e8-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="be5e8-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="be5e8-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="be5e8-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub MakeKey ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    data As String, _
    encoding As Encoding, _
    grbit As MakeKeyGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim data As String
Dim encoding As Encoding
Dim grbit As MakeKeyGrbitApi.MakeKey(sesid, tableid, data, _
    encoding, grbit)
```

``` csharp
public static void MakeKey(
    JET_SESID sesid,
    JET_TABLEID tableid,
    string data,
    Encoding encoding,
    MakeKeyGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="be5e8-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="be5e8-108">Parameters</span></span>

  - <span data-ttu-id="be5e8-109">-sid</span><span class="sxs-lookup"><span data-stu-id="be5e8-109">sesid</span></span>  
    <span data-ttu-id="be5e8-110">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="be5e8-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="be5e8-111">Die zu verwendende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="be5e8-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="be5e8-112">TableID</span><span class="sxs-lookup"><span data-stu-id="be5e8-112">tableid</span></span>  
    <span data-ttu-id="be5e8-113">Typ: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="be5e8-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="be5e8-114">Der Cursor, auf dem der Schlüssel erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="be5e8-114">The cursor to create the key on.</span></span>

<!-- end list -->

  - <span data-ttu-id="be5e8-115">Daten</span><span class="sxs-lookup"><span data-stu-id="be5e8-115">data</span></span>  
    <span data-ttu-id="be5e8-116">Typ: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="be5e8-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="be5e8-117">Spaltendaten für die aktuelle Schlüssel Spalte des aktuellen Index.</span><span class="sxs-lookup"><span data-stu-id="be5e8-117">Column data for the current key column of the current index.</span></span>

<!-- end list -->

  - <span data-ttu-id="be5e8-118">encoding</span><span class="sxs-lookup"><span data-stu-id="be5e8-118">encoding</span></span>  
    <span data-ttu-id="be5e8-119">Typ: [System. Text. Encoding](/dotnet/api/system.text.encoding)</span><span class="sxs-lookup"><span data-stu-id="be5e8-119">Type: [System.Text.Encoding](/dotnet/api/system.text.encoding)</span></span>  
    
    <span data-ttu-id="be5e8-120">Die Codierung, die zum Konvertieren der Zeichenfolge verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="be5e8-120">The encoding used to convert the string.</span></span>

<!-- end list -->

  - <span data-ttu-id="be5e8-121">grbit</span><span class="sxs-lookup"><span data-stu-id="be5e8-121">grbit</span></span>  
    <span data-ttu-id="be5e8-122">Typ: [Microsoft. ISAM. ESENT. Interop. makekeygrbit](./makekeygrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="be5e8-122">Type: [Microsoft.Isam.Esent.Interop.MakeKeyGrbit](./makekeygrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="be5e8-123">Schlüsseloptionen.</span><span class="sxs-lookup"><span data-stu-id="be5e8-123">Key options.</span></span>

## <a name="see-also"></a><span data-ttu-id="be5e8-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="be5e8-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="be5e8-125">Referenz</span><span class="sxs-lookup"><span data-stu-id="be5e8-125">Reference</span></span>

[<span data-ttu-id="be5e8-126">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="be5e8-126">Api class</span></span>](./api-class.md)

[<span data-ttu-id="be5e8-127">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="be5e8-127">Api members</span></span>](./api-members.md)

[<span data-ttu-id="be5e8-128">Makekey-Überladung</span><span class="sxs-lookup"><span data-stu-id="be5e8-128">MakeKey overload</span></span>](./api.makekey-method.md)

[<span data-ttu-id="be5e8-129">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="be5e8-129">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
