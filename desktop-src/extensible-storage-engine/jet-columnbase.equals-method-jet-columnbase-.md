---
description: 'Weitere Informationen finden Sie hier: JET_COLUMNBASE. Gleichheits Methode (JET_COLUMNBASE)'
title: JET_COLUMNBASE. Gleichheits Methode (JET_COLUMNBASE)
TOCTitle: Equals method (JET_COLUMNBASE)
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_COLUMNBASE.Equals(Microsoft.Isam.Esent.Interop.JET_COLUMNBASE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_columnbase.equals(v=EXCHG.10)
ms:contentKeyID: 55103355
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.JET_COLUMNBASE.Equals
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ada65f03966ebd5f0bf7142d3953117734c2f3cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868963"
---
# <a name="jet_columnbaseequals-method-jet_columnbase"></a><span data-ttu-id="e2d93-103">JET_COLUMNBASE. Gleichheits Methode (JET_COLUMNBASE)</span><span class="sxs-lookup"><span data-stu-id="e2d93-103">JET_COLUMNBASE.Equals method (JET_COLUMNBASE)</span></span>

<span data-ttu-id="e2d93-104">Gibt einen Wert zurück, der angibt, ob diese Instanz gleich einer anderen Instanz ist.</span><span class="sxs-lookup"><span data-stu-id="e2d93-104">Returns a value indicating whether this instance is equal to another instance.</span></span>

<span data-ttu-id="e2d93-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e2d93-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="e2d93-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="e2d93-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e2d93-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e2d93-107">Syntax</span></span>

``` vb
'Declaration
Public Function Equals ( _
    other As JET_COLUMNBASE _
) As Boolean
'Usage
Dim instance As JET_COLUMNBASE
Dim other As JET_COLUMNBASE
Dim returnValue As Boolean

returnValue = instance.Equals(other)
```

``` csharp
public bool Equals(
    JET_COLUMNBASE other
)
```

#### <a name="parameters"></a><span data-ttu-id="e2d93-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="e2d93-108">Parameters</span></span>

  - <span data-ttu-id="e2d93-109">andere</span><span class="sxs-lookup"><span data-stu-id="e2d93-109">other</span></span>  
    <span data-ttu-id="e2d93-110">Typ: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNBASE](./jet-columnbase-class.md)</span><span class="sxs-lookup"><span data-stu-id="e2d93-110">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNBASE](./jet-columnbase-class.md)</span></span>  
    
    <span data-ttu-id="e2d93-111">Eine-Instanz, die mit dieser Instanz verglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="e2d93-111">An instance to compare with this instance.</span></span>

#### <a name="return-value"></a><span data-ttu-id="e2d93-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e2d93-112">Return value</span></span>

<span data-ttu-id="e2d93-113">Typ: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="e2d93-113">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="e2d93-114">True, wenn die beiden Instanzen gleich sind.</span><span class="sxs-lookup"><span data-stu-id="e2d93-114">True if the two instances are equal.</span></span>  

#### <a name="implements"></a><span data-ttu-id="e2d93-115">Implementiert</span><span class="sxs-lookup"><span data-stu-id="e2d93-115">Implements</span></span>

[<span data-ttu-id="e2d93-116">IEquatable \<T\> . Ist gleich(T)</span><span class="sxs-lookup"><span data-stu-id="e2d93-116">IEquatable\<T\>.Equals(T)</span></span>](/dotnet/api/system.iequatable-1.equals#System_IEquatable_1_Equals__0_)  

## <a name="see-also"></a><span data-ttu-id="e2d93-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e2d93-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e2d93-118">Referenz</span><span class="sxs-lookup"><span data-stu-id="e2d93-118">Reference</span></span>

[<span data-ttu-id="e2d93-119">JET_COLUMNBASE-Klasse</span><span class="sxs-lookup"><span data-stu-id="e2d93-119">JET_COLUMNBASE class</span></span>](./jet-columnbase-class.md)

[<span data-ttu-id="e2d93-120">Mitglieder JET_COLUMNBASE</span><span class="sxs-lookup"><span data-stu-id="e2d93-120">JET_COLUMNBASE members</span></span>](./jet-columnbase-members.md)

[<span data-ttu-id="e2d93-121">Gleichheits Überladung</span><span class="sxs-lookup"><span data-stu-id="e2d93-121">Equals overload</span></span>](./jet-columnbase.equals-method.md)

[<span data-ttu-id="e2d93-122">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="e2d93-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
