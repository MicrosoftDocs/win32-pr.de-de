---
description: 'Weitere Informationen finden Sie unter: esentdataexception-Konstruktor (String, JET_err)'
title: Esentdataexception-Konstruktor (Zeichenfolge, JET_err)
TOCTitle: EsentDataException constructor (String, JET_err)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentDataException.#ctor(System.String,Microsoft.Isam.Esent.Interop.JET_err)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdataexception.esentdataexception(v=EXCHG.10)
ms:contentKeyID: 55101571
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentDataException..ctor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9e39638d6e5458c0dcc555f31bec12e752d84337
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130920"
---
# <a name="esentdataexception-constructor-string-jet_err"></a><span data-ttu-id="dca1b-103">Esentdataexception-Konstruktor (Zeichenfolge, JET_err)</span><span class="sxs-lookup"><span data-stu-id="dca1b-103">EsentDataException constructor (String, JET_err)</span></span>

<span data-ttu-id="dca1b-104">Initialisiert eine neue Instanz der esentdataexception-Klasse.</span><span class="sxs-lookup"><span data-stu-id="dca1b-104">Initializes a new instance of the EsentDataException class.</span></span>

<span data-ttu-id="dca1b-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="dca1b-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="dca1b-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="dca1b-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="dca1b-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="dca1b-107">Syntax</span></span>

``` vb
'Declaration
Protected Sub New ( _
    description As String, _
    err As JET_err _
)
'Usage
Dim description As String
Dim err As JET_err

Dim instance As New EsentDataException(description, _
    err)
```

``` csharp
protected EsentDataException(
    string description,
    JET_err err
)
```

#### <a name="parameters"></a><span data-ttu-id="dca1b-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="dca1b-108">Parameters</span></span>

  - <span data-ttu-id="dca1b-109">description</span><span class="sxs-lookup"><span data-stu-id="dca1b-109">description</span></span>  
    <span data-ttu-id="dca1b-110">Typ: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="dca1b-110">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="dca1b-111">Die Beschreibung des Fehlers.</span><span class="sxs-lookup"><span data-stu-id="dca1b-111">The description of the error.</span></span>

<!-- end list -->

  - <span data-ttu-id="dca1b-112">irre</span><span class="sxs-lookup"><span data-stu-id="dca1b-112">err</span></span>  
    <span data-ttu-id="dca1b-113">Typ: [Microsoft.ISAM.ESENT.Interop.JET_err](./jet-err-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="dca1b-113">Type: [Microsoft.Isam.Esent.Interop.JET_err](./jet-err-enumeration.md)</span></span>  
    
    <span data-ttu-id="dca1b-114">Der Fehlercode der Ausnahme.</span><span class="sxs-lookup"><span data-stu-id="dca1b-114">The error code of the exception.</span></span>

## <a name="see-also"></a><span data-ttu-id="dca1b-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dca1b-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="dca1b-116">Referenz</span><span class="sxs-lookup"><span data-stu-id="dca1b-116">Reference</span></span>

[<span data-ttu-id="dca1b-117">Esentdataexception-Klasse</span><span class="sxs-lookup"><span data-stu-id="dca1b-117">EsentDataException class</span></span>](./esentdataexception-class.md)

[<span data-ttu-id="dca1b-118">Esentdataexception-Member</span><span class="sxs-lookup"><span data-stu-id="dca1b-118">EsentDataException members</span></span>](./esentdataexception-members.md)

[<span data-ttu-id="dca1b-119">Esentdataexception-Überladung</span><span class="sxs-lookup"><span data-stu-id="dca1b-119">EsentDataException overload</span></span>](./esentdataexception-constructor.md)

[<span data-ttu-id="dca1b-120">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="dca1b-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
