---
description: Weitere Informationen finden Sie in der guidcolumnvalue. Size-Eigenschaft.
title: Guidcolumnvalue. Size-Eigenschaft
TOCTitle: 'Size property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.GuidColumnValue.Size
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.guidcolumnvalue.size(v=EXCHG.10)
ms:contentKeyID: 55107387
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.GuidColumnValue.Size
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.GuidColumnValue.get_Size
- Microsoft.Isam.Esent.Interop.GuidColumnValue.Size
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b973638ac8caa4848ed5ecc65468c363ebd2f866
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347865"
---
# <a name="guidcolumnvaluesize-property"></a><span data-ttu-id="5f9e6-103">Guidcolumnvalue. Size-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="5f9e6-103">GuidColumnValue.Size property</span></span>

<span data-ttu-id="5f9e6-104">Ruft die Größe des Werts in der Spalte ab.</span><span class="sxs-lookup"><span data-stu-id="5f9e6-104">Gets the size of the value in the column.</span></span> <span data-ttu-id="5f9e6-105">Dadurch wird 0 für Spalten variabler Größen (z. b. Binär und Zeichenfolge) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5f9e6-105">This returns 0 for variable sized columns (i.e. binary and string).</span></span>

<span data-ttu-id="5f9e6-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="5f9e6-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="5f9e6-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="5f9e6-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="5f9e6-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="5f9e6-108">Syntax</span></span>

``` vb
'Declaration
Protected Overrides ReadOnly Property Size As Integer
    Get
'Usage
Dim value As Integer

value = Me.Size
```

``` csharp
protected override int Size { get; }
```

#### <a name="property-value"></a><span data-ttu-id="5f9e6-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="5f9e6-109">Property value</span></span>

<span data-ttu-id="5f9e6-110">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="5f9e6-110">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="5f9e6-111">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5f9e6-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="5f9e6-112">Referenz</span><span class="sxs-lookup"><span data-stu-id="5f9e6-112">Reference</span></span>

[<span data-ttu-id="5f9e6-113">Guidcolumnvalue-Klasse</span><span class="sxs-lookup"><span data-stu-id="5f9e6-113">GuidColumnValue class</span></span>](./guidcolumnvalue-class.md)

[<span data-ttu-id="5f9e6-114">Guidcolumnvalue-Member</span><span class="sxs-lookup"><span data-stu-id="5f9e6-114">GuidColumnValue members</span></span>](./guidcolumnvalue-members.md)

[<span data-ttu-id="5f9e6-115">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="5f9e6-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
