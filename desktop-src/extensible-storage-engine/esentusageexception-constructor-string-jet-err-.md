---
description: 'Weitere Informationen finden Sie unter: esentusageexception-Konstruktor (String, JET_err)'
title: Esentusageexception-Konstruktor (Zeichenfolge, JET_err)
TOCTitle: EsentUsageException constructor (String, JET_err)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentUsageException.#ctor(System.String,Microsoft.Isam.Esent.Interop.JET_err)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentusageexception.esentusageexception(v=EXCHG.10)
ms:contentKeyID: 55103223
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentUsageException..ctor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4f9d38ebc5be25eb8f036583404d340a8882de6f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104350459"
---
# <a name="esentusageexception-constructor-string-jet_err"></a><span data-ttu-id="6c39a-103">Esentusageexception-Konstruktor (Zeichenfolge, JET_err)</span><span class="sxs-lookup"><span data-stu-id="6c39a-103">EsentUsageException constructor (String, JET_err)</span></span>

<span data-ttu-id="6c39a-104">Initialisiert eine neue Instanz der esentusageexception-Klasse.</span><span class="sxs-lookup"><span data-stu-id="6c39a-104">Initializes a new instance of the EsentUsageException class.</span></span>

<span data-ttu-id="6c39a-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="6c39a-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="6c39a-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="6c39a-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="6c39a-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="6c39a-107">Syntax</span></span>

``` vb
'Declaration
Protected Sub New ( _
    description As String, _
    err As JET_err _
)
'Usage
Dim description As String
Dim err As JET_err

Dim instance As New EsentUsageException(description, _
    err)
```

``` csharp
protected EsentUsageException(
    string description,
    JET_err err
)
```

#### <a name="parameters"></a><span data-ttu-id="6c39a-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="6c39a-108">Parameters</span></span>

  - <span data-ttu-id="6c39a-109">description</span><span class="sxs-lookup"><span data-stu-id="6c39a-109">description</span></span>  
    <span data-ttu-id="6c39a-110">Typ: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="6c39a-110">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="6c39a-111">Die Beschreibung des Fehlers.</span><span class="sxs-lookup"><span data-stu-id="6c39a-111">The description of the error.</span></span>

<!-- end list -->

  - <span data-ttu-id="6c39a-112">irre</span><span class="sxs-lookup"><span data-stu-id="6c39a-112">err</span></span>  
    <span data-ttu-id="6c39a-113">Typ: [Microsoft.ISAM.ESENT.Interop.JET_err](./jet-err-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="6c39a-113">Type: [Microsoft.Isam.Esent.Interop.JET_err](./jet-err-enumeration.md)</span></span>  
    
    <span data-ttu-id="6c39a-114">Der Fehlercode der Ausnahme.</span><span class="sxs-lookup"><span data-stu-id="6c39a-114">The error code of the exception.</span></span>

## <a name="see-also"></a><span data-ttu-id="6c39a-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6c39a-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="6c39a-116">Referenz</span><span class="sxs-lookup"><span data-stu-id="6c39a-116">Reference</span></span>

[<span data-ttu-id="6c39a-117">EsentUsageException-Klasse</span><span class="sxs-lookup"><span data-stu-id="6c39a-117">EsentUsageException class</span></span>](./esentusageexception-class.md)

[<span data-ttu-id="6c39a-118">Esentusageexception-Member</span><span class="sxs-lookup"><span data-stu-id="6c39a-118">EsentUsageException members</span></span>](./esentusageexception-members.md)

[<span data-ttu-id="6c39a-119">Esentusageexception-Überladung</span><span class="sxs-lookup"><span data-stu-id="6c39a-119">EsentUsageException overload</span></span>](./esentusageexception-constructor.md)

[<span data-ttu-id="6c39a-120">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="6c39a-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
