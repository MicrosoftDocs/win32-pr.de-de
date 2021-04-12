---
description: 'Weitere Informationen: Instanzkonstruktor (Zeichenfolge)'
title: Instanzkonstruktor (Zeichenfolge)
TOCTitle: Instance constructor (String)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Instance.#ctor(System.String)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instance.instance(v=EXCHG.10)
ms:contentKeyID: 55103263
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Instance..ctor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8cf184fc9b8d921b1d8bd1003b960bc65a6ffb75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218747"
---
# <a name="instance-constructor-string"></a><span data-ttu-id="c4bea-103">Instanzkonstruktor (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="c4bea-103">Instance constructor (String)</span></span>

<span data-ttu-id="c4bea-104">Initialisiert eine neue Instanz der Instanzklasse.</span><span class="sxs-lookup"><span data-stu-id="c4bea-104">Initializes a new instance of the Instance class.</span></span> <span data-ttu-id="c4bea-105">Die zugrunde liegende JET_INSTANCE ist zugeordnet, aber nicht initialisiert.</span><span class="sxs-lookup"><span data-stu-id="c4bea-105">The underlying JET_INSTANCE is allocated, but not initialized.</span></span>

<span data-ttu-id="c4bea-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="c4bea-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="c4bea-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="c4bea-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="c4bea-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="c4bea-108">Syntax</span></span>

``` vb
'Declaration
Public Sub New ( _
    name As String _
)
'Usage
Dim name As String

Dim instance As New Instance(name)
```

``` csharp
public Instance(
    string name
)
```

#### <a name="parameters"></a><span data-ttu-id="c4bea-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="c4bea-109">Parameters</span></span>

  - <span data-ttu-id="c4bea-110">name</span><span class="sxs-lookup"><span data-stu-id="c4bea-110">name</span></span>  
    <span data-ttu-id="c4bea-111">Typ: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="c4bea-111">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="c4bea-112">Der Name der Instanz.</span><span class="sxs-lookup"><span data-stu-id="c4bea-112">The name of the instance.</span></span> <span data-ttu-id="c4bea-113">Diese Zeichenfolge muss innerhalb eines bestimmten Prozesses, der die Datenbank-Engine gehostet, eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="c4bea-113">This string must be unique within a given process hosting the database engine.</span></span>

## <a name="see-also"></a><span data-ttu-id="c4bea-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c4bea-114">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c4bea-115">Referenz</span><span class="sxs-lookup"><span data-stu-id="c4bea-115">Reference</span></span>

[<span data-ttu-id="c4bea-116">Instanzklasse</span><span class="sxs-lookup"><span data-stu-id="c4bea-116">Instance class</span></span>](./instance-class.md)

[<span data-ttu-id="c4bea-117">Instanzmember</span><span class="sxs-lookup"><span data-stu-id="c4bea-117">Instance members</span></span>](./instance-members.md)

[<span data-ttu-id="c4bea-118">Instanzüberladung</span><span class="sxs-lookup"><span data-stu-id="c4bea-118">Instance overload</span></span>](./instance-constructor.md)

[<span data-ttu-id="c4bea-119">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="c4bea-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
