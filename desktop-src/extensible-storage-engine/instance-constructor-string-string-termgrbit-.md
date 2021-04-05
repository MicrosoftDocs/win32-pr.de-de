---
description: 'Weitere Informationen finden Sie unter: Instanzkonstruktor (String, String, termgrbit)'
title: Instanzkonstruktor (String, String, termgrbit)
TOCTitle: Instance constructor (String, String, TermGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Instance.#ctor(System.String,System.String,Microsoft.Isam.Esent.Interop.TermGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instance.instance(v=EXCHG.10)
ms:contentKeyID: 55103289
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Instance..ctor
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b9cf90f9678db1074594c7772eb67d895a8a5b8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753304"
---
# <a name="instance-constructor-string-string-termgrbit"></a><span data-ttu-id="17ce9-103">Instanzkonstruktor (String, String, termgrbit)</span><span class="sxs-lookup"><span data-stu-id="17ce9-103">Instance constructor (String, String, TermGrbit)</span></span>

<span data-ttu-id="17ce9-104">Initialisiert eine neue Instanz der Instanzklasse.</span><span class="sxs-lookup"><span data-stu-id="17ce9-104">Initializes a new instance of the Instance class.</span></span> <span data-ttu-id="17ce9-105">Die zugrunde liegende JET_INSTANCE ist zugeordnet, aber nicht initialisiert.</span><span class="sxs-lookup"><span data-stu-id="17ce9-105">The underlying JET_INSTANCE is allocated, but not initialized.</span></span>

<span data-ttu-id="17ce9-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="17ce9-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="17ce9-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="17ce9-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="17ce9-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="17ce9-108">Syntax</span></span>

``` vb
'Declaration
Public Sub New ( _
    name As String, _
    displayName As String, _
    termGrbit As TermGrbit _
)
'Usage
Dim name As String
Dim displayName As String
Dim termGrbit As TermGrbit

Dim instance As New Instance(name, displayName, _
    termGrbit)
```

``` csharp
public Instance(
    string name,
    string displayName,
    TermGrbit termGrbit
)
```

#### <a name="parameters"></a><span data-ttu-id="17ce9-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="17ce9-109">Parameters</span></span>

  - <span data-ttu-id="17ce9-110">name</span><span class="sxs-lookup"><span data-stu-id="17ce9-110">name</span></span>  
    <span data-ttu-id="17ce9-111">Typ: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="17ce9-111">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="17ce9-112">Der Name der Instanz.</span><span class="sxs-lookup"><span data-stu-id="17ce9-112">The name of the instance.</span></span> <span data-ttu-id="17ce9-113">Diese Zeichenfolge muss innerhalb eines bestimmten Prozesses, der die Datenbank-Engine gehostet, eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="17ce9-113">This string must be unique within a given process hosting the database engine.</span></span>

<!-- end list -->

  - <span data-ttu-id="17ce9-114">displayName</span><span class="sxs-lookup"><span data-stu-id="17ce9-114">displayName</span></span>  
    <span data-ttu-id="17ce9-115">Typ: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="17ce9-115">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="17ce9-116">Ein Anzeige Name für die-Instanz.</span><span class="sxs-lookup"><span data-stu-id="17ce9-116">A display name for the instance.</span></span> <span data-ttu-id="17ce9-117">Diese wird in EventLog-Einträgen verwendet.</span><span class="sxs-lookup"><span data-stu-id="17ce9-117">This will be used in eventlog entries.</span></span>

<!-- end list -->

  - <span data-ttu-id="17ce9-118">termgrbit</span><span class="sxs-lookup"><span data-stu-id="17ce9-118">termGrbit</span></span>  
    <span data-ttu-id="17ce9-119">Typ: [Microsoft. ISAM. ESENT. Interop. termgrbit](./termgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="17ce9-119">Type: [Microsoft.Isam.Esent.Interop.TermGrbit](./termgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="17ce9-120">Das termgrbit, das zur jetterm-Zeit verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="17ce9-120">The TermGrbit to be used at JetTerm time.</span></span>

## <a name="see-also"></a><span data-ttu-id="17ce9-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="17ce9-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="17ce9-122">Referenz</span><span class="sxs-lookup"><span data-stu-id="17ce9-122">Reference</span></span>

[<span data-ttu-id="17ce9-123">Instanzklasse</span><span class="sxs-lookup"><span data-stu-id="17ce9-123">Instance class</span></span>](./instance-class.md)

[<span data-ttu-id="17ce9-124">Instanzmember</span><span class="sxs-lookup"><span data-stu-id="17ce9-124">Instance members</span></span>](./instance-members.md)

[<span data-ttu-id="17ce9-125">Instanzüberladung</span><span class="sxs-lookup"><span data-stu-id="17ce9-125">Instance overload</span></span>](./instance-constructor.md)

[<span data-ttu-id="17ce9-126">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="17ce9-126">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
