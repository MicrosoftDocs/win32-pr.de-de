---
description: 'Weitere Informationen finden Sie hier: JET_INSTANCE. Gleichheits Methode (JET_INSTANCE)'
title: JET_INSTANCE. Gleichheits Methode (JET_INSTANCE)
TOCTitle: Equals method (JET_INSTANCE)
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_INSTANCE.Equals(Microsoft.Isam.Esent.Interop.JET_INSTANCE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_instance.equals(v=EXCHG.10)
ms:contentKeyID: 39512490
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.JET_INSTANCE.Equals
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: be4f2a172da5fc0d7670e7e87464eac04df3cfa3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217254"
---
# <a name="jet_instanceequals-method-jet_instance"></a><span data-ttu-id="43870-103">JET_INSTANCE. Gleichheits Methode (JET_INSTANCE)</span><span class="sxs-lookup"><span data-stu-id="43870-103">JET_INSTANCE.Equals method (JET_INSTANCE)</span></span>

<span data-ttu-id="43870-104">Gibt einen Wert zurück, der angibt, ob diese Instanz gleich einer anderen Instanz ist.</span><span class="sxs-lookup"><span data-stu-id="43870-104">Returns a value indicating whether this instance is equal to another instance.</span></span>

<span data-ttu-id="43870-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="43870-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="43870-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="43870-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="43870-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="43870-107">Syntax</span></span>

``` vb
'Declaration
Public Function Equals ( _
    other As JET_INSTANCE _
) As Boolean
'Usage
Dim instance As JET_INSTANCE
Dim other As JET_INSTANCE
Dim returnValue As Boolean

returnValue = instance.Equals(other)
```

``` csharp
public bool Equals(
    JET_INSTANCE other
)
```

#### <a name="parameters"></a><span data-ttu-id="43870-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="43870-108">Parameters</span></span>

  - <span data-ttu-id="43870-109">andere</span><span class="sxs-lookup"><span data-stu-id="43870-109">other</span></span>  
    <span data-ttu-id="43870-110">Typ: [Microsoft.ISAM.ESENT.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="43870-110">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="43870-111">Eine-Instanz, die mit dieser Instanz verglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="43870-111">An instance to compare with this instance.</span></span>

#### <a name="return-value"></a><span data-ttu-id="43870-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="43870-112">Return value</span></span>

<span data-ttu-id="43870-113">Typ: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="43870-113">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="43870-114">True, wenn die beiden Instanzen gleich sind.</span><span class="sxs-lookup"><span data-stu-id="43870-114">True if the two instances are equal.</span></span>  

#### <a name="implements"></a><span data-ttu-id="43870-115">Implementiert</span><span class="sxs-lookup"><span data-stu-id="43870-115">Implements</span></span>

[<span data-ttu-id="43870-116">IEquatable \<T\> . Ist gleich(T)</span><span class="sxs-lookup"><span data-stu-id="43870-116">IEquatable\<T\>.Equals(T)</span></span>](/dotnet/api/system.iequatable-1.equals#System_IEquatable_1_Equals__0_)  

## <a name="see-also"></a><span data-ttu-id="43870-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="43870-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="43870-118">Referenz</span><span class="sxs-lookup"><span data-stu-id="43870-118">Reference</span></span>

[<span data-ttu-id="43870-119">JET_INSTANCE Struktur</span><span class="sxs-lookup"><span data-stu-id="43870-119">JET_INSTANCE structure</span></span>](./jet-instance-structure.md)

[<span data-ttu-id="43870-120">Mitglieder JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="43870-120">JET_INSTANCE members</span></span>](./jet-instance-members.md)

[<span data-ttu-id="43870-121">Gleichheits Überladung</span><span class="sxs-lookup"><span data-stu-id="43870-121">Equals overload</span></span>](./jet-instance.equals-method.md)

[<span data-ttu-id="43870-122">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="43870-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
