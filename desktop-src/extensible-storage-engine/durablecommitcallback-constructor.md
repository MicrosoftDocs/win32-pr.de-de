---
description: 'Weitere Informationen über: durablecommitcallback-Konstruktor'
title: Durablecommitcallback-Konstruktor (Microsoft. ISAM. ESENT. Interop. Windows8)
TOCTitle: 'DurableCommitCallback constructor '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.DurableCommitCallback.#ctor(Microsoft.Isam.Esent.Interop.JET_INSTANCE,Microsoft.Isam.Esent.Interop.Windows8.JET_PFNDURABLECOMMITCALLBACK)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.durablecommitcallback.durablecommitcallback(v=EXCHG.10)
ms:contentKeyID: 55104290
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.DurableCommitCallback.DurableCommitCallback
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.DurableCommitCallback..ctor
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ade1952615b98d9ea41a7a1b83d0bf1a3c6fc8d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759414"
---
# <a name="durablecommitcallback-constructor"></a><span data-ttu-id="515be-103">Durablecommitcallback-Konstruktor</span><span class="sxs-lookup"><span data-stu-id="515be-103">DurableCommitCallback constructor</span></span>

<span data-ttu-id="515be-104">Initialisiert eine neue Instanz der [durablecommitcallback](./durablecommitcallback-class.md) -Klasse.</span><span class="sxs-lookup"><span data-stu-id="515be-104">Initializes a new instance of the [DurableCommitCallback](./durablecommitcallback-class.md) class.</span></span>

<span data-ttu-id="515be-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="515be-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="515be-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="515be-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="515be-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="515be-107">Syntax</span></span>

``` vb
'Declaration
Public Sub New ( _
    instance As JET_INSTANCE, _
    wrappedCallback As JET_PFNDURABLECOMMITCALLBACK _
)
'Usage
Dim instance As JET_INSTANCE
Dim wrappedCallback As JET_PFNDURABLECOMMITCALLBACK

Dim instance As New DurableCommitCallback(instance, _
    wrappedCallback)
```

``` csharp
public DurableCommitCallback(
    JET_INSTANCE instance,
    JET_PFNDURABLECOMMITCALLBACK wrappedCallback
)
```

#### <a name="parameters"></a><span data-ttu-id="515be-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="515be-108">Parameters</span></span>

  - <span data-ttu-id="515be-109">instance</span><span class="sxs-lookup"><span data-stu-id="515be-109">instance</span></span>  
    <span data-ttu-id="515be-110">Typ: [Microsoft.ISAM.ESENT.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="515be-110">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="515be-111">Die-Instanz, mit der der Rückruf verknüpft werden soll.</span><span class="sxs-lookup"><span data-stu-id="515be-111">The instance with which to associate the callback.</span></span>

<!-- end list -->

  - <span data-ttu-id="515be-112">wrappedcallback</span><span class="sxs-lookup"><span data-stu-id="515be-112">wrappedCallback</span></span>  
    <span data-ttu-id="515be-113">Typ: [Microsoft.ISAM.ESENT.Interop.Windows8.JET_PFNDURABLECOMMITCALLBACK](./jet-pfndurablecommitcallback-delegate.md)</span><span class="sxs-lookup"><span data-stu-id="515be-113">Type: [Microsoft.Isam.Esent.Interop.Windows8.JET_PFNDURABLECOMMITCALLBACK](./jet-pfndurablecommitcallback-delegate.md)</span></span>  
    
    <span data-ttu-id="515be-114">Der Rückruf des verwalteten Codes, der aufgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="515be-114">The managed code callback to call.</span></span>

## <a name="see-also"></a><span data-ttu-id="515be-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="515be-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="515be-116">Referenz</span><span class="sxs-lookup"><span data-stu-id="515be-116">Reference</span></span>

[<span data-ttu-id="515be-117">Durablecommitcallback-Klasse</span><span class="sxs-lookup"><span data-stu-id="515be-117">DurableCommitCallback class</span></span>](./durablecommitcallback-class.md)

[<span data-ttu-id="515be-118">Durablecommitcallback-Member</span><span class="sxs-lookup"><span data-stu-id="515be-118">DurableCommitCallback members</span></span>](./durablecommitcallback-members.md)

[<span data-ttu-id="515be-119">Microsoft. ISAM. ESENT. Interop. Windows8-Namespace</span><span class="sxs-lookup"><span data-stu-id="515be-119">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
