---
description: 'Weitere Informationen finden Sie unter: esentresourceexception-Konstruktor (String, JET_err)'
title: Esentresourceexception-Konstruktor (Zeichenfolge, JET_err)
TOCTitle: EsentResourceException constructor (String, JET_err)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentResourceException.#ctor(System.String,Microsoft.Isam.Esent.Interop.JET_err)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentresourceexception.esentresourceexception(v=EXCHG.10)
ms:contentKeyID: 55107307
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentResourceException..ctor
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 458b12a80fdc0e6d7883d966f2e50aa8c1f6d69b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529459"
---
# <a name="esentresourceexception-constructor-string-jet_err"></a><span data-ttu-id="8ca0f-103">Esentresourceexception-Konstruktor (Zeichenfolge, JET_err)</span><span class="sxs-lookup"><span data-stu-id="8ca0f-103">EsentResourceException constructor (String, JET_err)</span></span>

<span data-ttu-id="8ca0f-104">Initialisiert eine neue Instanz der esentresourceexception-Klasse.</span><span class="sxs-lookup"><span data-stu-id="8ca0f-104">Initializes a new instance of the EsentResourceException class.</span></span>

<span data-ttu-id="8ca0f-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="8ca0f-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="8ca0f-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="8ca0f-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="8ca0f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="8ca0f-107">Syntax</span></span>

``` vb
'Declaration
Protected Sub New ( _
    description As String, _
    err As JET_err _
)
'Usage
Dim description As String
Dim err As JET_err

Dim instance As New EsentResourceException(description, _
    err)
```

``` csharp
protected EsentResourceException(
    string description,
    JET_err err
)
```

#### <a name="parameters"></a><span data-ttu-id="8ca0f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="8ca0f-108">Parameters</span></span>

  - <span data-ttu-id="8ca0f-109">description</span><span class="sxs-lookup"><span data-stu-id="8ca0f-109">description</span></span>  
    <span data-ttu-id="8ca0f-110">Typ: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="8ca0f-110">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="8ca0f-111">Die Beschreibung des Fehlers.</span><span class="sxs-lookup"><span data-stu-id="8ca0f-111">The description of the error.</span></span>

<!-- end list -->

  - <span data-ttu-id="8ca0f-112">irre</span><span class="sxs-lookup"><span data-stu-id="8ca0f-112">err</span></span>  
    <span data-ttu-id="8ca0f-113">Typ: [Microsoft.ISAM.ESENT.Interop.JET_err](./jet-err-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="8ca0f-113">Type: [Microsoft.Isam.Esent.Interop.JET_err](./jet-err-enumeration.md)</span></span>  
    
    <span data-ttu-id="8ca0f-114">Der Fehlercode der Ausnahme.</span><span class="sxs-lookup"><span data-stu-id="8ca0f-114">The error code of the exception.</span></span>

## <a name="see-also"></a><span data-ttu-id="8ca0f-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8ca0f-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="8ca0f-116">Referenz</span><span class="sxs-lookup"><span data-stu-id="8ca0f-116">Reference</span></span>

[<span data-ttu-id="8ca0f-117">EsentResourceException-Klasse</span><span class="sxs-lookup"><span data-stu-id="8ca0f-117">EsentResourceException class</span></span>](./esentresourceexception-class.md)

[<span data-ttu-id="8ca0f-118">Esentresourceexception-Member</span><span class="sxs-lookup"><span data-stu-id="8ca0f-118">EsentResourceException members</span></span>](./esentresourceexception-members.md)

[<span data-ttu-id="8ca0f-119">Esentresourceexception-Überladung</span><span class="sxs-lookup"><span data-stu-id="8ca0f-119">EsentResourceException overload</span></span>](./esentresourceexception-constructor.md)

[<span data-ttu-id="8ca0f-120">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="8ca0f-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
