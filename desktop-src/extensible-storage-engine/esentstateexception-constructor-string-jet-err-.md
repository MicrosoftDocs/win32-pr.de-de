---
description: 'Weitere Informationen finden Sie unter: esentstateexception-Konstruktor (String, JET_err)'
title: Esentstateexception-Konstruktor (Zeichenfolge, JET_err)
TOCTitle: EsentStateException constructor (String, JET_err)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentStateException.#ctor(System.String,Microsoft.Isam.Esent.Interop.JET_err)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentstateexception.esentstateexception(v=EXCHG.10)
ms:contentKeyID: 55102995
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentStateException..ctor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 611671bb488d4804fd31569f15ab89e3ddfed462
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360797"
---
# <a name="esentstateexception-constructor-string-jet_err"></a><span data-ttu-id="0e8e7-103">Esentstateexception-Konstruktor (Zeichenfolge, JET_err)</span><span class="sxs-lookup"><span data-stu-id="0e8e7-103">EsentStateException constructor (String, JET_err)</span></span>

<span data-ttu-id="0e8e7-104">Initialisiert eine neue Instanz der esentstateexception-Klasse.</span><span class="sxs-lookup"><span data-stu-id="0e8e7-104">Initializes a new instance of the EsentStateException class.</span></span>

<span data-ttu-id="0e8e7-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="0e8e7-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="0e8e7-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="0e8e7-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="0e8e7-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="0e8e7-107">Syntax</span></span>

``` vb
'Declaration
Protected Sub New ( _
    description As String, _
    err As JET_err _
)
'Usage
Dim description As String
Dim err As JET_err

Dim instance As New EsentStateException(description, _
    err)
```

``` csharp
protected EsentStateException(
    string description,
    JET_err err
)
```

#### <a name="parameters"></a><span data-ttu-id="0e8e7-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="0e8e7-108">Parameters</span></span>

  - <span data-ttu-id="0e8e7-109">description</span><span class="sxs-lookup"><span data-stu-id="0e8e7-109">description</span></span>  
    <span data-ttu-id="0e8e7-110">Typ: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="0e8e7-110">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="0e8e7-111">Die Beschreibung des Fehlers.</span><span class="sxs-lookup"><span data-stu-id="0e8e7-111">The description of the error.</span></span>

<!-- end list -->

  - <span data-ttu-id="0e8e7-112">irre</span><span class="sxs-lookup"><span data-stu-id="0e8e7-112">err</span></span>  
    <span data-ttu-id="0e8e7-113">Typ: [Microsoft.ISAM.ESENT.Interop.JET_err](./jet-err-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="0e8e7-113">Type: [Microsoft.Isam.Esent.Interop.JET_err](./jet-err-enumeration.md)</span></span>  
    
    <span data-ttu-id="0e8e7-114">Der Fehlercode der Ausnahme.</span><span class="sxs-lookup"><span data-stu-id="0e8e7-114">The error code of the exception.</span></span>

## <a name="see-also"></a><span data-ttu-id="0e8e7-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0e8e7-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="0e8e7-116">Referenz</span><span class="sxs-lookup"><span data-stu-id="0e8e7-116">Reference</span></span>

[<span data-ttu-id="0e8e7-117">EsentStateException-Klasse</span><span class="sxs-lookup"><span data-stu-id="0e8e7-117">EsentStateException class</span></span>](./esentstateexception-class.md)

[<span data-ttu-id="0e8e7-118">Esentstateexception-Member</span><span class="sxs-lookup"><span data-stu-id="0e8e7-118">EsentStateException members</span></span>](./esentstateexception-members.md)

[<span data-ttu-id="0e8e7-119">Esentstateexception-Überladung</span><span class="sxs-lookup"><span data-stu-id="0e8e7-119">EsentStateException overload</span></span>](./esentstateexception-constructor.md)

[<span data-ttu-id="0e8e7-120">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="0e8e7-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
