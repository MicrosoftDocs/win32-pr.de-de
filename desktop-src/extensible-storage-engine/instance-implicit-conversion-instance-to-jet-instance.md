---
description: Weitere Informationen finden Sie unter implizite instanzkonvertierung (Instance to JET_INSTANCE)
title: Implizite instanzkonvertierung (Instanz in JET_INSTANCE)
TOCTitle: Implicit conversion (Instance to JET_INSTANCE)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Instance.op_Implicit(Microsoft.Isam.Esent.Interop.Instance)~Microsoft.Isam.Esent.Interop.JET_INSTANCE
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instance.op_implicit(v=EXCHG.10)
ms:contentKeyID: 55103290
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Instance.Implicit
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Instance.Implicit
- Microsoft.Isam.Esent.Interop.Instance.op_Implicit
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8c7dbac9f0b5736970cf51aef9e99f2877cfd488
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353178"
---
# <a name="instance-implicit-conversion-instance-to-jet_instance"></a><span data-ttu-id="b8f7d-103">Implizite instanzkonvertierung (Instanz in JET_INSTANCE)</span><span class="sxs-lookup"><span data-stu-id="b8f7d-103">Instance Implicit conversion (Instance to JET_INSTANCE)</span></span>

<span data-ttu-id="b8f7d-104">Bereitstellen der impliziten Konvertierung eines Instanzobjekts in eine JET_INSTANCE Struktur.</span><span class="sxs-lookup"><span data-stu-id="b8f7d-104">Provide implicit conversion of an Instance object to a JET_INSTANCE structure.</span></span> <span data-ttu-id="b8f7d-105">Dies geschieht, damit eine-Instanz überall dort verwendet werden kann, wo eine JET_INSTANCE erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="b8f7d-105">This is done so that an Instance can be used anywhere a JET_INSTANCE is required.</span></span>

<span data-ttu-id="b8f7d-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b8f7d-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="b8f7d-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="b8f7d-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b8f7d-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="b8f7d-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Widening Operator CType ( _
    instance As Instance _
) As JET_INSTANCE
'Usage
Dim input As Instance
Dim output As JET_INSTANCE

output = CType(input, JET_INSTANCE)
```

``` csharp
public static implicit operator JET_INSTANCE (
    Instance instance
)
```

#### <a name="parameters"></a><span data-ttu-id="b8f7d-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="b8f7d-109">Parameters</span></span>

  - <span data-ttu-id="b8f7d-110">instance</span><span class="sxs-lookup"><span data-stu-id="b8f7d-110">instance</span></span>  
    <span data-ttu-id="b8f7d-111">Typ: [Microsoft. ISAM. ESENT. Interop. Instance](./instance-class.md)</span><span class="sxs-lookup"><span data-stu-id="b8f7d-111">Type: [Microsoft.Isam.Esent.Interop.Instance](./instance-class.md)</span></span>  
    
    <span data-ttu-id="b8f7d-112">Die zu konvertierende-Instanz.</span><span class="sxs-lookup"><span data-stu-id="b8f7d-112">The instance to convert.</span></span>

#### <a name="return-value"></a><span data-ttu-id="b8f7d-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b8f7d-113">Return value</span></span>

<span data-ttu-id="b8f7d-114">Typ: [Microsoft.ISAM.ESENT.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="b8f7d-114">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
<span data-ttu-id="b8f7d-115">Der von der-Instanz umschließende JET_INSTANCE.</span><span class="sxs-lookup"><span data-stu-id="b8f7d-115">The JET_INSTANCE wrapped by the instance.</span></span>  

## <a name="see-also"></a><span data-ttu-id="b8f7d-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b8f7d-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b8f7d-117">Referenz</span><span class="sxs-lookup"><span data-stu-id="b8f7d-117">Reference</span></span>

[<span data-ttu-id="b8f7d-118">Instanzklasse</span><span class="sxs-lookup"><span data-stu-id="b8f7d-118">Instance class</span></span>](./instance-class.md)

[<span data-ttu-id="b8f7d-119">Instanzmember</span><span class="sxs-lookup"><span data-stu-id="b8f7d-119">Instance members</span></span>](./instance-members.md)

[<span data-ttu-id="b8f7d-120">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="b8f7d-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
