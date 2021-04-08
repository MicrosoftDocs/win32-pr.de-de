---
description: 'Weitere Informationen finden Sie unter: API. retrievekey-Methode'
title: API. retrievekey-Methode
TOCTitle: 'RetrieveKey method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.RetrieveKey(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.RetrieveKeyGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievekey(v=EXCHG.10)
ms:contentKeyID: 55100880
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.RetrieveKey
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.RetrieveKey
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fcabab7639a9cf3128b0b2c314ba60c2de8f8e09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749489"
---
# <a name="apiretrievekey-method"></a><span data-ttu-id="76a0f-103">API. retrievekey-Methode</span><span class="sxs-lookup"><span data-stu-id="76a0f-103">Api.RetrieveKey method</span></span>

<span data-ttu-id="76a0f-104">Ruft den Schlüssel für den Index Eintrag an der aktuellen Position eines Cursors ab.</span><span class="sxs-lookup"><span data-stu-id="76a0f-104">Retrieves the key for the index entry at the current position of a cursor.</span></span>

<span data-ttu-id="76a0f-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="76a0f-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="76a0f-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="76a0f-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="76a0f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="76a0f-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Function RetrieveKey ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    grbit As RetrieveKeyGrbit _
) As Byte()
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim grbit As RetrieveKeyGrbit
Dim returnValue As Byte()

returnValue = Api.RetrieveKey(sesid, _
    tableid, grbit)
```

``` csharp
public static byte[] RetrieveKey(
    JET_SESID sesid,
    JET_TABLEID tableid,
    RetrieveKeyGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="76a0f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="76a0f-108">Parameters</span></span>

  - <span data-ttu-id="76a0f-109">-sid</span><span class="sxs-lookup"><span data-stu-id="76a0f-109">sesid</span></span>  
    <span data-ttu-id="76a0f-110">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="76a0f-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="76a0f-111">Die zu verwendende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="76a0f-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="76a0f-112">TableID</span><span class="sxs-lookup"><span data-stu-id="76a0f-112">tableid</span></span>  
    <span data-ttu-id="76a0f-113">Typ: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="76a0f-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="76a0f-114">Der Cursor, aus dem der Schlüssel abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="76a0f-114">The cursor to retrieve the key from.</span></span>

<!-- end list -->

  - <span data-ttu-id="76a0f-115">grbit</span><span class="sxs-lookup"><span data-stu-id="76a0f-115">grbit</span></span>  
    <span data-ttu-id="76a0f-116">Typ: [Microsoft. ISAM. ESENT. Interop. retrievekeygrbit](./retrievekeygrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="76a0f-116">Type: [Microsoft.Isam.Esent.Interop.RetrieveKeyGrbit](./retrievekeygrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="76a0f-117">Abrufen von Schlüsseloptionen</span><span class="sxs-lookup"><span data-stu-id="76a0f-117">Retrieve key options.</span></span>

#### <a name="return-value"></a><span data-ttu-id="76a0f-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="76a0f-118">Return value</span></span>

<span data-ttu-id="76a0f-119">Sorte \[\]</span><span class="sxs-lookup"><span data-stu-id="76a0f-119">Type: \[\]</span></span>  
<span data-ttu-id="76a0f-120">Der abgerufene Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="76a0f-120">The retrieved key.</span></span>  

## <a name="see-also"></a><span data-ttu-id="76a0f-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="76a0f-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="76a0f-122">Referenz</span><span class="sxs-lookup"><span data-stu-id="76a0f-122">Reference</span></span>

[<span data-ttu-id="76a0f-123">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="76a0f-123">Api class</span></span>](./api-class.md)

[<span data-ttu-id="76a0f-124">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="76a0f-124">Api members</span></span>](./api-members.md)

[<span data-ttu-id="76a0f-125">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="76a0f-125">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
