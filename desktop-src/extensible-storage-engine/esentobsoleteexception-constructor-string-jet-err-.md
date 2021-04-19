---
description: 'Weitere Informationen finden Sie unter: esentobsoleteexception-Konstruktor (String, JET_err)'
title: Esentobsoleteexception-Konstruktor (Zeichenfolge, JET_err)
TOCTitle: EsentObsoleteException constructor (String, JET_err)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentObsoleteException.#ctor(System.String,Microsoft.Isam.Esent.Interop.JET_err)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentobsoleteexception.esentobsoleteexception(v=EXCHG.10)
ms:contentKeyID: 55102363
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentObsoleteException..ctor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 435a3db75cb09a47bccc311733b90fae30563c86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348937"
---
# <a name="esentobsoleteexception-constructor-string-jet_err"></a><span data-ttu-id="dd6fd-103">Esentobsoleteexception-Konstruktor (Zeichenfolge, JET_err)</span><span class="sxs-lookup"><span data-stu-id="dd6fd-103">EsentObsoleteException constructor (String, JET_err)</span></span>

<span data-ttu-id="dd6fd-104">Initialisiert eine neue Instanz der esentobsoleteexception-Klasse.</span><span class="sxs-lookup"><span data-stu-id="dd6fd-104">Initializes a new instance of the EsentObsoleteException class.</span></span>

<span data-ttu-id="dd6fd-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="dd6fd-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="dd6fd-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="dd6fd-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="dd6fd-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="dd6fd-107">Syntax</span></span>

``` vb
'Declaration
Protected Sub New ( _
    description As String, _
    err As JET_err _
)
'Usage
Dim description As String
Dim err As JET_err

Dim instance As New EsentObsoleteException(description, _
    err)
```

``` csharp
protected EsentObsoleteException(
    string description,
    JET_err err
)
```

#### <a name="parameters"></a><span data-ttu-id="dd6fd-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="dd6fd-108">Parameters</span></span>

  - <span data-ttu-id="dd6fd-109">description</span><span class="sxs-lookup"><span data-stu-id="dd6fd-109">description</span></span>  
    <span data-ttu-id="dd6fd-110">Typ: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="dd6fd-110">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="dd6fd-111">Die Beschreibung des Fehlers.</span><span class="sxs-lookup"><span data-stu-id="dd6fd-111">The description of the error.</span></span>

<!-- end list -->

  - <span data-ttu-id="dd6fd-112">irre</span><span class="sxs-lookup"><span data-stu-id="dd6fd-112">err</span></span>  
    <span data-ttu-id="dd6fd-113">Typ: [Microsoft.ISAM.ESENT.Interop.JET_err](./jet-err-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="dd6fd-113">Type: [Microsoft.Isam.Esent.Interop.JET_err](./jet-err-enumeration.md)</span></span>  
    
    <span data-ttu-id="dd6fd-114">Der Fehlercode der Ausnahme.</span><span class="sxs-lookup"><span data-stu-id="dd6fd-114">The error code of the exception.</span></span>

## <a name="see-also"></a><span data-ttu-id="dd6fd-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dd6fd-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="dd6fd-116">Referenz</span><span class="sxs-lookup"><span data-stu-id="dd6fd-116">Reference</span></span>

[<span data-ttu-id="dd6fd-117">EsentObsoleteException-Klasse</span><span class="sxs-lookup"><span data-stu-id="dd6fd-117">EsentObsoleteException class</span></span>](./esentobsoleteexception-class.md)

[<span data-ttu-id="dd6fd-118">Esentobsoleteexception-Member</span><span class="sxs-lookup"><span data-stu-id="dd6fd-118">EsentObsoleteException members</span></span>](./esentobsoleteexception-members.md)

[<span data-ttu-id="dd6fd-119">Esentobsoleteexception-Überladung</span><span class="sxs-lookup"><span data-stu-id="dd6fd-119">EsentObsoleteException overload</span></span>](./esentobsoleteexception-constructor.md)

[<span data-ttu-id="dd6fd-120">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="dd6fd-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
