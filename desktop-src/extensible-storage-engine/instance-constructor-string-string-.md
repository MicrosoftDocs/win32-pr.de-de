---
description: 'Weitere Informationen: Instanzkonstruktor (Zeichenfolge, Zeichenfolge)'
title: Instanzkonstruktor (Zeichenfolge, Zeichenfolge)
TOCTitle: Instance constructor (String, String)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Instance.#ctor(System.String,System.String)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instance.instance(v=EXCHG.10)
ms:contentKeyID: 55103267
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
ms.openlocfilehash: 02cb629cdfaba17ce9a137b52eb1a6d6fdbaa56b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344229"
---
# <a name="instance-constructor-string-string"></a><span data-ttu-id="129b4-103">Instanzkonstruktor (Zeichenfolge, Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="129b4-103">Instance constructor (String, String)</span></span>

<span data-ttu-id="129b4-104">Initialisiert eine neue Instanz der Instanzklasse.</span><span class="sxs-lookup"><span data-stu-id="129b4-104">Initializes a new instance of the Instance class.</span></span> <span data-ttu-id="129b4-105">Die zugrunde liegende JET_INSTANCE ist zugeordnet, aber nicht initialisiert.</span><span class="sxs-lookup"><span data-stu-id="129b4-105">The underlying JET_INSTANCE is allocated, but not initialized.</span></span>

<span data-ttu-id="129b4-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="129b4-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="129b4-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="129b4-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="129b4-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="129b4-108">Syntax</span></span>

``` vb
'Declaration
Public Sub New ( _
    name As String, _
    displayName As String _
)
'Usage
Dim name As String
Dim displayName As String

Dim instance As New Instance(name, displayName)
```

``` csharp
public Instance(
    string name,
    string displayName
)
```

#### <a name="parameters"></a><span data-ttu-id="129b4-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="129b4-109">Parameters</span></span>

  - <span data-ttu-id="129b4-110">name</span><span class="sxs-lookup"><span data-stu-id="129b4-110">name</span></span>  
    <span data-ttu-id="129b4-111">Typ: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="129b4-111">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="129b4-112">Der Name der Instanz.</span><span class="sxs-lookup"><span data-stu-id="129b4-112">The name of the instance.</span></span> <span data-ttu-id="129b4-113">Diese Zeichenfolge muss innerhalb eines bestimmten Prozesses, der die Datenbank-Engine gehostet, eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="129b4-113">This string must be unique within a given process hosting the database engine.</span></span>

<!-- end list -->

  - <span data-ttu-id="129b4-114">displayName</span><span class="sxs-lookup"><span data-stu-id="129b4-114">displayName</span></span>  
    <span data-ttu-id="129b4-115">Typ: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="129b4-115">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="129b4-116">Ein Anzeige Name für die-Instanz.</span><span class="sxs-lookup"><span data-stu-id="129b4-116">A display name for the instance.</span></span> <span data-ttu-id="129b4-117">Diese wird in EventLog-Einträgen verwendet.</span><span class="sxs-lookup"><span data-stu-id="129b4-117">This will be used in eventlog entries.</span></span>

## <a name="see-also"></a><span data-ttu-id="129b4-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="129b4-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="129b4-119">Referenz</span><span class="sxs-lookup"><span data-stu-id="129b4-119">Reference</span></span>

[<span data-ttu-id="129b4-120">Instanzklasse</span><span class="sxs-lookup"><span data-stu-id="129b4-120">Instance class</span></span>](./instance-class.md)

[<span data-ttu-id="129b4-121">Instanzmember</span><span class="sxs-lookup"><span data-stu-id="129b4-121">Instance members</span></span>](./instance-members.md)

[<span data-ttu-id="129b4-122">Instanzüberladung</span><span class="sxs-lookup"><span data-stu-id="129b4-122">Instance overload</span></span>](./instance-constructor.md)

[<span data-ttu-id="129b4-123">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="129b4-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
