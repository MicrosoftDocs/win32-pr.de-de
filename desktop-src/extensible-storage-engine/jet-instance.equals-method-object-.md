---
description: 'Weitere Informationen finden Sie hier: JET_INSTANCE. Gleichheits Methode (Objekt)'
title: JET_INSTANCE. Gleichheits Methode (Objekt)
TOCTitle: Equals method (Object)
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_INSTANCE.Equals(System.Object)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_instance.equals(v=EXCHG.10)
ms:contentKeyID: 39515717
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
ms.openlocfilehash: 2b13393b487abb4de65360f5199ae1123d3f076e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042667"
---
# <a name="jet_instanceequals-method-object"></a><span data-ttu-id="350db-103">JET_INSTANCE. Gleichheits Methode (Objekt)</span><span class="sxs-lookup"><span data-stu-id="350db-103">JET_INSTANCE.Equals method (Object)</span></span>

<span data-ttu-id="350db-104">Gibt einen Wert zurück, der angibt, ob diese Instanz gleich einer anderen Instanz ist.</span><span class="sxs-lookup"><span data-stu-id="350db-104">Returns a value indicating whether this instance is equal to another instance.</span></span>

<span data-ttu-id="350db-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="350db-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="350db-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="350db-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="350db-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="350db-107">Syntax</span></span>

``` vb
'Declaration
Public Overrides Function Equals ( _
    obj As Object _
) As Boolean
'Usage
Dim instance As JET_INSTANCE
Dim obj As Object
Dim returnValue As Boolean

returnValue = instance.Equals(obj)
```

``` csharp
public override bool Equals(
    Object obj
)
```

#### <a name="parameters"></a><span data-ttu-id="350db-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="350db-108">Parameters</span></span>

  - <span data-ttu-id="350db-109">obj</span><span class="sxs-lookup"><span data-stu-id="350db-109">obj</span></span>  
    <span data-ttu-id="350db-110">Type: [System. Object](/dotnet/api/system.object)</span><span class="sxs-lookup"><span data-stu-id="350db-110">Type: [System.Object](/dotnet/api/system.object)</span></span>  
    
    <span data-ttu-id="350db-111">Ein Objekt, das mit dieser Instanz verglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="350db-111">An object to compare with this instance.</span></span>

#### <a name="return-value"></a><span data-ttu-id="350db-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="350db-112">Return value</span></span>

<span data-ttu-id="350db-113">Typ: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="350db-113">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="350db-114">True, wenn die beiden Instanzen gleich sind.</span><span class="sxs-lookup"><span data-stu-id="350db-114">True if the two instances are equal.</span></span>  

## <a name="see-also"></a><span data-ttu-id="350db-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="350db-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="350db-116">Referenz</span><span class="sxs-lookup"><span data-stu-id="350db-116">Reference</span></span>

[<span data-ttu-id="350db-117">JET_INSTANCE Struktur</span><span class="sxs-lookup"><span data-stu-id="350db-117">JET_INSTANCE structure</span></span>](./jet-instance-structure.md)

[<span data-ttu-id="350db-118">Mitglieder JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="350db-118">JET_INSTANCE members</span></span>](./jet-instance-members.md)

[<span data-ttu-id="350db-119">Gleichheits Überladung</span><span class="sxs-lookup"><span data-stu-id="350db-119">Equals overload</span></span>](./jet-instance.equals-method.md)

[<span data-ttu-id="350db-120">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="350db-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
