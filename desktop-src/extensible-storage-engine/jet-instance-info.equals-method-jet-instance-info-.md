---
description: 'Weitere Informationen finden Sie hier: JET_INSTANCE_INFO. Gleichheits Methode (JET_INSTANCE_INFO)'
title: JET_INSTANCE_INFO. Gleichheits Methode (JET_INSTANCE_INFO)
TOCTitle: Equals method (JET_INSTANCE_INFO)
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_INSTANCE_INFO.Equals(Microsoft.Isam.Esent.Interop.JET_INSTANCE_INFO)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_instance_info.equals(v=EXCHG.10)
ms:contentKeyID: 55103697
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.JET_INSTANCE_INFO.Equals
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b601e018b51e6e95162478ff6c5fe12e77f7b469
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103959901"
---
# <a name="jet_instance_infoequals-method-jet_instance_info"></a><span data-ttu-id="dc546-103">JET_INSTANCE_INFO. Gleichheits Methode (JET_INSTANCE_INFO)</span><span class="sxs-lookup"><span data-stu-id="dc546-103">JET_INSTANCE_INFO.Equals method (JET_INSTANCE_INFO)</span></span>

<span data-ttu-id="dc546-104">Gibt einen Wert zurück, der angibt, ob diese Instanz gleich einer anderen Instanz ist.</span><span class="sxs-lookup"><span data-stu-id="dc546-104">Returns a value indicating whether this instance is equal to another instance.</span></span>

<span data-ttu-id="dc546-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="dc546-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="dc546-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="dc546-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="dc546-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="dc546-107">Syntax</span></span>

``` vb
'Declaration
Public Function Equals ( _
    other As JET_INSTANCE_INFO _
) As Boolean
'Usage
Dim instance As JET_INSTANCE_INFO
Dim other As JET_INSTANCE_INFO
Dim returnValue As Boolean

returnValue = instance.Equals(other)
```

``` csharp
public bool Equals(
    JET_INSTANCE_INFO other
)
```

#### <a name="parameters"></a><span data-ttu-id="dc546-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="dc546-108">Parameters</span></span>

  - <span data-ttu-id="dc546-109">andere</span><span class="sxs-lookup"><span data-stu-id="dc546-109">other</span></span>  
    <span data-ttu-id="dc546-110">Typ: [Microsoft.ISAM.ESENT.Interop.JET_INSTANCE_INFO](./jet-instance-info-class.md)</span><span class="sxs-lookup"><span data-stu-id="dc546-110">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE_INFO](./jet-instance-info-class.md)</span></span>  
    
    <span data-ttu-id="dc546-111">Eine-Instanz, die mit dieser Instanz verglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="dc546-111">An instance to compare with this instance.</span></span>

#### <a name="return-value"></a><span data-ttu-id="dc546-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="dc546-112">Return value</span></span>

<span data-ttu-id="dc546-113">Typ: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="dc546-113">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="dc546-114">True, wenn die beiden Instanzen gleich sind.</span><span class="sxs-lookup"><span data-stu-id="dc546-114">True if the two instances are equal.</span></span>  

#### <a name="implements"></a><span data-ttu-id="dc546-115">Implementiert</span><span class="sxs-lookup"><span data-stu-id="dc546-115">Implements</span></span>

[<span data-ttu-id="dc546-116">IEquatable \<T\> . Ist gleich(T)</span><span class="sxs-lookup"><span data-stu-id="dc546-116">IEquatable\<T\>.Equals(T)</span></span>](/dotnet/api/system.iequatable-1.equals#System_IEquatable_1_Equals__0_)  

## <a name="see-also"></a><span data-ttu-id="dc546-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dc546-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="dc546-118">Referenz</span><span class="sxs-lookup"><span data-stu-id="dc546-118">Reference</span></span>

[<span data-ttu-id="dc546-119">JET_INSTANCE_INFO-Klasse</span><span class="sxs-lookup"><span data-stu-id="dc546-119">JET_INSTANCE_INFO class</span></span>](./jet-instance-info-class.md)

[<span data-ttu-id="dc546-120">Mitglieder JET_INSTANCE_INFO</span><span class="sxs-lookup"><span data-stu-id="dc546-120">JET_INSTANCE_INFO members</span></span>](./jet-instance-info-members.md)

[<span data-ttu-id="dc546-121">Gleichheits Überladung</span><span class="sxs-lookup"><span data-stu-id="dc546-121">Equals overload</span></span>](./jet-instance-info.equals-method.md)

[<span data-ttu-id="dc546-122">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="dc546-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
