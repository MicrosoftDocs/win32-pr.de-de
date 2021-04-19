---
description: 'Weitere Informationen finden Sie unter: esentmemoryexception-Konstruktor (String, JET_err)'
title: Esentmemoryexception-Konstruktor (Zeichenfolge, JET_err)
TOCTitle: EsentMemoryException constructor (String, JET_err)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentMemoryException.#ctor(System.String,Microsoft.Isam.Esent.Interop.JET_err)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentmemoryexception.esentmemoryexception(v=EXCHG.10)
ms:contentKeyID: 55102199
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentMemoryException..ctor
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 60cdb6fda03695a4afb41d82e83aaeeb9415f421
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349804"
---
# <a name="esentmemoryexception-constructor-string-jet_err"></a><span data-ttu-id="6a944-103">Esentmemoryexception-Konstruktor (Zeichenfolge, JET_err)</span><span class="sxs-lookup"><span data-stu-id="6a944-103">EsentMemoryException constructor (String, JET_err)</span></span>

<span data-ttu-id="6a944-104">Initialisiert eine neue Instanz der esentmemoryexception-Klasse.</span><span class="sxs-lookup"><span data-stu-id="6a944-104">Initializes a new instance of the EsentMemoryException class.</span></span>

<span data-ttu-id="6a944-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="6a944-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="6a944-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="6a944-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="6a944-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="6a944-107">Syntax</span></span>

``` vb
'Declaration
Protected Sub New ( _
    description As String, _
    err As JET_err _
)
'Usage
Dim description As String
Dim err As JET_err

Dim instance As New EsentMemoryException(description, _
    err)
```

``` csharp
protected EsentMemoryException(
    string description,
    JET_err err
)
```

#### <a name="parameters"></a><span data-ttu-id="6a944-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="6a944-108">Parameters</span></span>

  - <span data-ttu-id="6a944-109">description</span><span class="sxs-lookup"><span data-stu-id="6a944-109">description</span></span>  
    <span data-ttu-id="6a944-110">Typ: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="6a944-110">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="6a944-111">Die Beschreibung des Fehlers.</span><span class="sxs-lookup"><span data-stu-id="6a944-111">The description of the error.</span></span>

<!-- end list -->

  - <span data-ttu-id="6a944-112">irre</span><span class="sxs-lookup"><span data-stu-id="6a944-112">err</span></span>  
    <span data-ttu-id="6a944-113">Typ: [Microsoft.ISAM.ESENT.Interop.JET_err](./jet-err-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="6a944-113">Type: [Microsoft.Isam.Esent.Interop.JET_err](./jet-err-enumeration.md)</span></span>  
    
    <span data-ttu-id="6a944-114">Der Fehlercode der Ausnahme.</span><span class="sxs-lookup"><span data-stu-id="6a944-114">The error code of the exception.</span></span>

## <a name="see-also"></a><span data-ttu-id="6a944-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6a944-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="6a944-116">Referenz</span><span class="sxs-lookup"><span data-stu-id="6a944-116">Reference</span></span>

[<span data-ttu-id="6a944-117">EsentMemoryException-Klasse</span><span class="sxs-lookup"><span data-stu-id="6a944-117">EsentMemoryException class</span></span>](./esentmemoryexception-class.md)

[<span data-ttu-id="6a944-118">Esentmemoryexception-Member</span><span class="sxs-lookup"><span data-stu-id="6a944-118">EsentMemoryException members</span></span>](./esentmemoryexception-members.md)

[<span data-ttu-id="6a944-119">Esentmemoryexception-Überladung</span><span class="sxs-lookup"><span data-stu-id="6a944-119">EsentMemoryException overload</span></span>](./esentmemoryexception-constructor.md)

[<span data-ttu-id="6a944-120">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="6a944-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
